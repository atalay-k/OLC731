# Veri Düzenleme V

Bir veriyi R ortamamına aktardıktan sonra veri setinde yer alan tüm satır ya da sütunların doğru bir şekilde aktarılıp aktarılmadığı, değişken isimlerinin düzgün olup olmadığı yani özellikle sütun adlarında boşluk olmaması ya da farklı karakterler bulunmaması kontrol edilmelidir. İlk olarak R ortamına aktarılan boş satır ve sütunlar olup olmadığı **filter()** ve **select()** gibi fonksiyonlarla incelebilir. Eksik verilerin nasıl temsil edildiği kontrol edilmelidir. **NA**,**" "** (bosluk), **.**, **999** , **9999** vb. şekilde ifade edilen eksik veriler **mutate()** ve **ifelse()** ile düzenlebilir.  Ayrıca karakter (character) ve faktör (factor) değişkenlerinin de düzgün tanımlanıp tanımlanmadığı incelenmelidir.

## Dağınık veri

Sütunlarda program, kadın ve erkek isimleri olan dağınık bir veri seti üzerinden veri düzenlemesinin temel aşamalarını gerçekleştirelim:

| **Program** | **Kadın** | **Erkek** |
|-------------|----------:|----------:|
| Olcme       |         6 |         6 |
| Program     |         5 |         5 |
| Yonetim     |         7 |         8 |
| PDR         |         5 |         3 |

Bir veri setindeki gözlem, değişken ve değişken değerlerinin ne olduğu öncelikle belirlenmelidir. Örnekteki veri setinde her bir programda yer alan öğrencilerin cinsiyeti gözlem; program, cinsiyet, frekans ise değişkenleri oluşturmalıdır. Program: Olcme, Program, Yonetim, PDR; Cinsiyet: Kadın, Erkek ten oluşmalı ve bunların degişken değeri olması gerekiyor, örnekteki gibi sütun başlığı değil. Frekansların ise iki sütuna dağıldığı görülmektedir.

## Düzgün Veri

Yukarıdaki örnekte verilen dağınık verinin olması gereken düzgün veri hali aşağıda yer almaktadır.

| **Program** | **Cinsiyet** | **Frekans** |
|-------------|-------------:|------------:|
| Olcme       |        Kadın |           6 |
| Olcme       |        Erkek |           6 |
| Program     |        Kadın |           5 |
| Program     |        Erkek |           5 |
| Yonetim     |        Kadın |           7 |
| Yonetim     |        Erkek |           8 |
| PDR         |        Kadın |           5 |
| PDR         |        Erkek |           3 |

Düzgün veri seti incelendiğinde, değişkenlerin sütunlarda, gözlemlerin satırlarda olduğu görülmektedir. Bu veri setinde program, cinsiyet ve frekans olmak üzere üç farklı değişken bulunmaktadır. Değişken adları mümkün olduğunca örnekte olduğu gibi anlamlı olmalıdır.

Aslında çok sayıda **satırı** anlamlandırmak, çok sayıda **sütunu** anlamlandırmaktan daha kolaydır. Verinin bu şekilde düzenlenmesi **dplyr**, **ggplot2**, **plotly**, **lattice** gibi paketleri rahat kullanabilmek için oldukça önemlidir. Hiyerarşik ve karma modeller için de verinin düzgün olması gerekmektedir. Ayrıca düzgün bir veri seti, eksik değerler ve **dengesiz** tekrarlanan ölçüm verileriyle ilgili daha az sorun sağlar.

**tidyr**, **reshape** vb. paketler ve bu paketlerde yer alan fonksiyonlar veri düzenlemede kullanılabilir.


Aslında çok sayıda **satırı** anlamlandırmak, çok sayıda **sütunu** anlamlandırmaktan daha kolaydır. Verinin bu şekilde düzenlenmesi **dplyr**, **ggplot2**, **plotly**, **lattice** gibi paketleri rahat kullanabilmek için oldukça önemlidir. Hiyerarşik ve karma modeller için de verinin düzgün olması gerekmektedir. Ayrıca düzgün bir veri seti, eksik değerler ve dengesiz tekrarlanan ölçüm verileriyle ilgili daha az sorun sağlar.

## gather()

`gather()` fonksiyonu bir dizi sütun alır ve onları iki yeni sütuna (kendi adını verebileceğin) dönüştürür.

Fonksiyonun kullanım şekli;


```r
gather(data, key, value, ..., na.rm = FALSE, 
       convert = FALSE, factor_key = FALSE)
```

-   A key: Orijinal sütun adlarını saklayan bir anahtar.
-   A value: Bu orijinal sütunlardaki değerlere sahip bir değer.

Fonksiyonun kullanımını göstermek için örnek bir veri seti üzerinde çalışalım.


```r
library(tuev)
data(PISA_OGR_2018)
midiPISA <- PISA_OGR_2018 %>% 
  select(OGRENCIID,SINIF,CINSIYET,
         Anne_Egitim,Baba_Egitim,OKUMA_ZEVK,
         ST097Q01TA:ST097Q05TA,ODOKUMA1:ODOKUMA5)

genisveri<- midiPISA %>% select(OGRENCIID,ODOKUMA1:ODOKUMA5) #belli değişkenlerin seçilmesi
genisveri %>% head(6) # verinin ilk 6 satırının görüntülenmesi
```

<div class="kable-table">

| OGRENCIID| ODOKUMA1| ODOKUMA2| ODOKUMA3| ODOKUMA4| ODOKUMA5|
|---------:|--------:|--------:|--------:|--------:|--------:|
|  79200768|  376.022|  417.746|  420.630|  413.837|  434.434|
|  79201064|  512.316|  473.229|  563.902|  485.396|  500.394|
|  79201118|  396.383|  413.859|  423.121|  452.124|  392.434|
|  79201275|  393.006|  428.757|  364.850|  382.522|  378.563|
|  79201481|  552.457|  570.109|  562.955|  530.835|  532.487|
|  79201556|  441.286|  415.682|  406.586|  437.001|  473.036|

</div>

Elde edilen çıktıda öğrenci ıd ve beş okuma olası değerinin yer aldığı toplam altı değişkenden yer alan veri seti görüntülenmektedir. Bu değişkenler sütunlarda yer almaktadır. `gather()` fonksiyonu geniş veriyi, uzun veri haline getirir.


```r
uzun <- genisveri %>% gather(O_OD,okumapuan,ODOKUMA1:ODOKUMA5)
uzun %>%  arrange(OGRENCIID) %>% head(10)
```

<div class="kable-table">

| OGRENCIID|O_OD     | okumapuan|
|---------:|:--------|---------:|
|  79200001|ODOKUMA1 |   449.876|
|  79200001|ODOKUMA2 |   457.572|
|  79200001|ODOKUMA3 |   413.428|
|  79200001|ODOKUMA4 |   430.044|
|  79200001|ODOKUMA5 |   439.072|
|  79200002|ODOKUMA1 |   669.156|
|  79200002|ODOKUMA2 |   665.848|
|  79200002|ODOKUMA3 |   684.978|
|  79200002|ODOKUMA4 |   664.624|
|  79200002|ODOKUMA5 |   659.670|

</div>

Çıktı incelendiğinde, oluşan veride ODOKUMA1, ODOKUMA2, ODOKUMA3, ODOKUMA4 ve ODOKUMA5 okumapuanı değişkeninin değerleri hâline gelmiştir. Çıktıda görüldüğü gibi, şimdi ID dışında iki sütunumuz var: Biri kategorik diğeri sayısal değerleri içerir. Her katılımcı icin beş farklı okuma olası değeri olduğu için her bir ID değeri beş kere tekrarlanmaktadır. Burada veri setinin ilk on satırı görüntülendiğinden sadece 79200001 ve 79200002 id numaralı öğrenciler görüntülenmektedir.

## spread()

-   `spread()` fonksiyonu uzun veriden tekrar geniş veri olusturmaya yarar. `gather()` fonksiyonunun tersi olan işlevi yapar


```r
tekrar_genis <- uzun %>% spread(O_OD,okumapuan) # geniş veri oluşturulması
tekrar_genis %>% head(6) # ilk altı satırın görüntülenmesi
```

<div class="kable-table">

| OGRENCIID| ODOKUMA1| ODOKUMA2| ODOKUMA3| ODOKUMA4| ODOKUMA5|
|---------:|--------:|--------:|--------:|--------:|--------:|
|  79200001|  449.876|  457.572|  413.428|  430.044|  439.072|
|  79200002|  669.156|  665.848|  684.978|  664.624|  659.670|
|  79200003|  451.875|  502.208|  443.832|  456.082|  436.965|
|  79200004|  346.944|  317.129|  339.054|  325.048|  367.116|
|  79200005|  466.959|  497.879|  415.394|  470.793|  446.268|
|  79200006|  366.303|  364.383|  384.399|  420.318|  351.426|

</div>

Öğrenci id değişkeni ile birlikte okuma puanlarının isimlerinin ve değerlerinin yer aldığı iki sütundan oluşan (id hariç) uzun veri seti, beş olası değerinin de ayrı birer sütun olarak yer aldığı toplam beş sütundan(id hariç) oluşan geniş veri setine dönüştürülmüştür.

## pivot_longer() ve pivot_wider() 

Verilerin girilme şekli genellikle geniş ve uzun olmak üzere iki formattan oluşur. Geniş formatta veriler, bir gözlemin özellikleri veya yanıtlar tek bir satırda verilir. Genellikle veriler bu şekilde girilmesine rağmen geniş format her zaman kullanışlı olmayabilir. Geniş verinin uzun veriye dönüştürülmesini `gather()` ve uzun verinin geniş veriye dönüşütürülmesini `spread()`fonksiyonu ile gerçekleştirdik. Ancak bahsedilen iki fonksiyona alternatif yeni fonksiyonlar üretilmiştir. Bu bölümde bu iki fonksiyon açıklanacaktır.


midiPISA verisetinden daha az değişken içerecek şekilde bir geniş veri seti örneği oluşturalım.


```r
genisveri <- midiPISA %>% select(OGRENCIID,ODOKUMA1:ODOKUMA5) #belli değişkenlerin seçilmesi
genisveri %>% head(6) # verinin ilk 6 satırının görüntülenmesi
```

<div class="kable-table">

| OGRENCIID| ODOKUMA1| ODOKUMA2| ODOKUMA3| ODOKUMA4| ODOKUMA5|
|---------:|--------:|--------:|--------:|--------:|--------:|
|  79200768|  376.022|  417.746|  420.630|  413.837|  434.434|
|  79201064|  512.316|  473.229|  563.902|  485.396|  500.394|
|  79201118|  396.383|  413.859|  423.121|  452.124|  392.434|
|  79201275|  393.006|  428.757|  364.850|  382.522|  378.563|
|  79201481|  552.457|  570.109|  562.955|  530.835|  532.487|
|  79201556|  441.286|  415.682|  406.586|  437.001|  473.036|

</div>

Elde edilen çıktıda öğrenci ıd ve beş okuma olası değerinin yer aldığı toplam altı değişkenden yer alan veri seti görüntülenmektedir. Bu değişkenler sütunlarda yer almakta olup geniş veri formatındadır. `pivot_longer` fonksiyonu geniş veriyi, uzun veri haline getirir.


```r
uzun <- genisveri %>% pivot_longer(names_to="okumapuan",values_to="deger",cols=ODOKUMA1:ODOKUMA5)
uzun %>% head(5)
```

<div class="kable-table">

| OGRENCIID|okumapuan |   deger|
|---------:|:---------|-------:|
|  79200768|ODOKUMA1  | 376.022|
|  79200768|ODOKUMA2  | 417.746|
|  79200768|ODOKUMA3  | 420.630|
|  79200768|ODOKUMA4  | 413.837|
|  79200768|ODOKUMA5  | 434.434|

</div>

Çıktı incelendiğinde, oluşan veride ODOKUMA1, ODOKUMA2, ODOKUMA3, ODOKUMA4 ve ODOKUMA5 ayrı bir sütunun değerleri haline gelmiştir. Bu okuma puan türlerinin sütununun yer aldığı değişken names_to argümanı ile "okumapuan" olarak isimlendirilmiştir. Ayrıca values_to argümanı ise okuma puanı değerlerinin yer aldığı sütun isimlendirilmiştir. Çıktıda görüldüğü gibi, şimdi ID dışında iki sütunumuz var: Biri *okuma puanı türü* için, diğeri **okuma puanı türleri** için. Her katılımcı icin beş farklı okuma olası değeri olduğu için her bir ID değeri beş kere tekrarlanmaktadır. Burada veri setinin ilk beş satırı görüntülendiğinden sadece 792200768 id numaralı öğrencinin değerleri görüntülenmektedir.

Bir veri setini daha iyi yorumlayabilmek amacıyla uzun veri formatından geniş veri formatına dönüştürülür. Genellikle bir gözlem için değerlerin birden çok satırda yer aldığı durumlarda tercih edilir. Bunun için `pivot_wider()` fonksiyonu kullanılır.


```r
genis<- uzun %>% pivot_wider(names_from="okumapuan",values_from="deger")
genis %>% head(5)
```

<div class="kable-table">

| OGRENCIID| ODOKUMA1| ODOKUMA2| ODOKUMA3| ODOKUMA4| ODOKUMA5|
|---------:|--------:|--------:|--------:|--------:|--------:|
|  79200768|  376.022|  417.746|  420.630|  413.837|  434.434|
|  79201064|  512.316|  473.229|  563.902|  485.396|  500.394|
|  79201118|  396.383|  413.859|  423.121|  452.124|  392.434|
|  79201275|  393.006|  428.757|  364.850|  382.522|  378.563|
|  79201481|  552.457|  570.109|  562.955|  530.835|  532.487|

</div>

## separate()

`separate()` fonksiyonu bir sütunu birden çok sütuna ayırır. Değerlerin sütun adlarına gömüldüğü toplanmış verilerde ortaktır. Oluşan veride okuma puanı değerlerinin karakter ve sayısal değerlerini ayırmak için `separate()`fonkisyonu kullanılabilir.


```r
uzun_v1 <- uzun %>% separate(okumapuan, c("OD","Sayi"),"MA") # bir sütunu iki sütuna ayırma

uzun_v1 %>% head(3) #ilk üç satırın görüntülenmesi
```

<div class="kable-table">

| OGRENCIID|OD    |Sayi |   deger|
|---------:|:-----|:----|-------:|
|  79200768|ODOKU |1    | 376.022|
|  79200768|ODOKU |2    | 417.746|
|  79200768|ODOKU |3    | 420.630|

</div>

Elde edilen çıktıya göre, okuma puanı olası değerlerinin yer aldığı sütun ikiye ayrılarak OD sütunu ve sayı sütunundan oluşmaktadır. Çıktının ilk üç satırı görüntülendiği için tek bir öğrenciye ait üç olası değerler yer almaktadır.

## unite()

`separate()` fonksiyonunun tam tersi olarak iki sütunu alıp tek sütunda birleştirir.


```r
uzun_birles <- uzun_v1 %>% unite(ODOKUMA, OD, Sayi, sep = "_") # sütun birleştirmenin yapılması
uzun_birles %>% head(3) # ilk üç satırın görüntülenmesi
```

<div class="kable-table">

| OGRENCIID|ODOKUMA |   deger|
|---------:|:-------|-------:|
|  79200768|ODOKU_1 | 376.022|
|  79200768|ODOKU_2 | 417.746|
|  79200768|ODOKU_3 | 420.630|

</div>

Elde edilen çıktı incelendiğinde, öğrenci id değişkeni hariç iki sütunun olduğu görülmektedir. ODOKUMA sütunu, okuma puanlarının isimlerinden, değer ise okuma olası puanı değerlerinden oluşmaktadır.

`separate()` fonksiyonunun alternatifi `extract()`   ve `unite()`   fonksiyonunun ile yapılabilecek olan işlemler `mutate()` fonksiyonu ile de yapılabilir.

Bu alternatiflerin uygunluğunun özel kullanım durumunuza ve verilerinizin niteliğine bağlı olduğunu unutmayın. Paketler zaman içinde yeni fonksiyonlara veya iyileştirmelere sahip olabileceğinden, en son güncellemeler için her zaman fonksiyon yardım sayfalarını kontrol etmenizi öneriyoruz.

