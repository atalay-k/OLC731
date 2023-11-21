# Veri Düzenleme IV

Bir veriyi R ortamamına aktardıktan sonra veri setinde yer alan tüm satır ya da sütunların doğru bir şekilde aktarılıp aktarılmadığı, değişken isimlerinin düzgün olup olmadığı yani özellikle sütun adlarında boşluk olmaması ya da farklı karakterler bulunmaması kontrol edilmelidir. İlk olarak R ortamına aktarılan boş satır ve sütunlar olup olmadığı **filter()** ve **select()** gibi fonksiyonlarla incelebilir. Eksik verilerin nasıl temsil edildiği kontrol edilmelidir. **NA**,**" "** (bosluk), **.**, **999** , **9999** vb. şekilde ifade edilen eksik veriler **mutate()** ve **ifelse()** ile düzenlebilir.  Ayrıca karakter (character) ve faktör (factor) değişkenlerinin de düzgün tanımlanıp tanımlanmadığı incelenmelidir.
## Dağınık veri

Sütunlarda program, kadın ve erkek isimleri olan dağınık bir veri seti üzerinden veri düzenlemesinin temel aşamalarını gerçekleştirelim:

| **Program** | **Kadın** | **Erkek** |
|-------------|----------:|----------:|
| Olcme       |         6 |         6 |
| Program     |         5 |         5 |
| Yonetim     |         7 |         8 |
| PDR         |         5 |         3 |

Bir veri setindeki gözlem, değişken ve değişken değerlerinin ne olduğu öncelikle belirlenmelidir. Örnekteki veri setinde her bir programda yer alan öğrencilerin cinsiyeti gözlem; program, cinsiyet, frekans ise değişkenleri oluşturmalıdır.Program: Olcme, Program, Yonetim, PDR; Cinsiyet: Kadın, Erkek ten oluşmalı ve bunların degişken değeri olması gerekiyor, örnekteki gibi sütun başlığı değil. Frekansların ise iki sütuna dağıldığı görülmektedir.

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

## **gather()** fonksiyonu

**gather()** fonksiyonu bir dizi sütun alır ve onları iki yeni sütuna (kendi adını verebileceğin) dönüştürür.

Fonksiyonun kullanım şekli;


```r
gather(data, key, value, ..., na.rm = FALSE, 
       convert = FALSE, factor_key = FALSE)
```

-   A key: Orijinal sütun adlarını saklayan bir anahtar.
-   A value: Bu orijinal sütunlardaki değerlere sahip bir değer.

Fonksiyonun kullanımını göstermek için örnek bir veri seti üzerinde çalışalım.


```r
library(tidyr) #paketin aktifleştirilmessi
load("import/miniPISA.rda") # verinin yüklenmesi
genisveri<- miniPISA %>% select(OGR_ID,O_OD1:O_OD5) #belli değişkenlerin seçilmesi
genisveri %>% head(6) # verinin ilk 6 satırının görüntülenmesi
```

<div class="kable-table">

|   OGR_ID|  O_OD1|  O_OD2|  O_OD3|  O_OD4|  O_OD5|
|--------:|------:|------:|------:|------:|------:|
| 79200768| 376.02| 417.75| 420.63| 413.84| 434.43|
| 79201064| 512.32| 473.23| 563.90| 485.40| 500.39|
| 79201118| 396.38| 413.86| 423.12| 452.12| 392.43|
| 79201275| 393.01| 428.76| 364.85| 382.52| 378.56|
| 79201481| 552.46| 570.11| 562.96| 530.84| 532.49|
| 79201556| 441.29| 415.68| 406.59| 437.00| 473.04|

</div>

Elde edilen çıktıda öğrenci ıd ve beş okuma olasılık değerinin yer aldığı toplam altı değişkenden yer alan veri seti görüntülenmektedir.Bu değişkenler sütunlarda yer almaktadır. `gather()` fonksiyonu geniş veriyi, uzun veri haline getirir.


```r
uzun<- genisveri %>% gather(O_OD,okumapuanı,O_OD1:O_OD5)
uzun %>% head(3)
```

<div class="kable-table">

|   OGR_ID|O_OD  | okumapuanı|
|--------:|:-----|----------:|
| 79200768|O_OD1 |     376.02|
| 79201064|O_OD1 |     512.32|
| 79201118|O_OD1 |     396.38|

</div>

Çıktı incelendiğinde, olusan veride O_OD1, O_OD2, O_OD3, O_OD4 ve O_OD5 okumapuanı değişkeninin değerleri haline gelmiştir. Çıktıda görüldüğü gibi, şimdi ID dışında iki sütunumuz var: Biri *O_OD* için, diğeri **okumapuanı** için. Her katılımcı icin beş farklı okuma olasılık değeri olduğu için her bir ID değeri beş kere tekrarlanmaktadır. Burada veri setinin ilk üç satırı görüntülendiğinden sadece O_OD1 görüntülenmektedir.


```r
uzun %>% tail(3) #son üç satırın görüntüleenmesi
```

<div class="kable-table">

|      |   OGR_ID|O_OD  | okumapuanı|
|:-----|--------:|:-----|----------:|
|34448 | 79205156|O_OD5 |     469.65|
|34449 | 79206039|O_OD5 |     437.95|
|34450 | 79206096|O_OD5 |     377.13|

</div>

Elde edilen çıktıda veri setinin son üç satırı görüntülendiğinden sadece O_OD5 görüntülenmektedir.

## **separate()**

**separate()** fonksiyonu bir sütunu birden çok sütuna ayırır. Değerlerin sütun adlarına gömüldüğü toplanmış verilerde ortaktır. Olusan veride O_OD1,O_OD2, O_OD3, O_OD4 ve O_OD5 değerlerinin karakter ve sayısal değerlerini ayırmak için **separate():** fonkisyonu kullanılabilir.


```r
uzun_ayrı <- uzun %>% 
            separate(O_OD, c("O_OD","Sayı"),"_") #bir sütunu iki sütuna ayırma

uzun_ayrı %>% head(3) #ilk üç satırın görüntülenmesi
```

<div class="kable-table">

|   OGR_ID|O_OD |Sayı | okumapuanı|
|--------:|:----|:----|----------:|
| 79200768|O    |OD1  |     376.02|
| 79201064|O    |OD1  |     512.32|
| 79201118|O    |OD1  |     396.38|

</div>

Elde edilen çıktıya göre, O_OD değerlerinin yer aldığı sütun ikiye ayrılarak O_OD sütunu (O) ve sayı (OD1,OD2,0D3,OD4, OD5) sütunundan oluşmaktadır. Çıktının ilk üç satırı görüntülendiği için sadece OD1(olasılık değeri 1) yer almaktadır.

## **unite()** fonksiyonu

\*\*gather\*()\*\* fonksiyonun tam tersi olarak iki sütunu alıp tek sutunda birlestirir.


```r
uzun_birles <- uzun_ayrı %>% unite(OD, O_OD, Sayı, sep = ".") # sütun birleştirmenin yapılması
uzun_birles %>% head(3)
```

<div class="kable-table">

|   OGR_ID|OD    | okumapuanı|
|--------:|:-----|----------:|
| 79200768|O.OD1 |     376.02|
| 79201064|O.OD1 |     512.32|
| 79201118|O.OD1 |     396.38|

</div>

Elde edilen çıktı incelendiğinde, öğrenci id değişkeni hariç iki sütunun olduğu görülmektedir. OD sütunu, okuma puanlarının isimlerinden, okuma puanı ise okuma olasılık değerlerinden oluşmaktadır. 

## **spread()** fonksiyonu

-   **spread():** fonksiyonu \*\*gather\*()\*\* fonksiyonun tam tersini yaparak uzun veriden genis veri olusturmaya yarar.


```r
tekrar_genis <- uzun_birles %>% spread(OD, okumapuanı) # geniş veri oluşturulması
tekrar_genis %>% head(6) # ilk altı satırın görüntülenmesi
```

<div class="kable-table">

|   OGR_ID|  O.OD1|  O.OD2|  O.OD3|  O.OD4|  O.OD5|
|--------:|------:|------:|------:|------:|------:|
| 79200001| 449.88| 457.57| 413.43| 430.04| 439.07|
| 79200002| 669.16| 665.85| 684.98| 664.62| 659.67|
| 79200003| 451.88| 502.21| 443.83| 456.08| 436.97|
| 79200004| 346.94| 317.13| 339.05| 325.05| 367.12|
| 79200005| 466.96| 497.88| 415.39| 470.79| 446.27|
| 79200006| 366.30| 364.38| 384.40| 420.32| 351.43|

</div>

Öğrenci id değişkeni ile birlikte okuma puanlarının isimlerinin ve değerlerinin yer aldığı iki sütundan oluşan (id hariç) uzun veri seti, beş olasılık değerinin de ayrı birer sütun olarak yer aldığı toplam beş sütundan(id hariç) oluşan geniş veri setine dönüştürülmüştür.
