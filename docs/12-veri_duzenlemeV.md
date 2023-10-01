# Veri duzenleme  - V




- **tiydr** paketi
- **gather()** fonksiyonu
- **separete()** fonksiyonu
- **spread()** fonksiyonu
- **unite()** fonksiyonu 



## Veriyi İnceleme

- Bir veriyi R ortamamına aktardıktan sonra

  - Veri setinizde yer alan tüm satırlar/sütunlar doğru bir şekilde aktarılmış mı?
  
  - Sütun isimleri düzgün mü? 
  
  - Özellikle sütun adlarında boşluk olması ya da farklı      karakterler bulunması sıkıntı yaratabilir.



- Aktarılan boş satır ve sütunlar var mı?

  - **filter()** ve **select()** gibi fonksiyonlarla            incelebilir. 
   
- Eksik veriler nasıl temsil ediliyor?

  - **NA**,**" "** (bosluk), **.**, **999** ,  **9999**
  
  - eksik veriler **mutate()** ve **ifelse()** ile             düzenlebilir.
  
- character ve factor değişkenler düzgün tanımlanımış mı?
  
## Dağınık Veri

.pull-left-narrow[
  
    
| **Program**     | **Kadın** | **Erkek**|
|-----------------|----------:|---------:|
| Olcme           |      6    |    6     |
| Program         |      5    |    5     |
| Yonetim         |      7    |    8     |
| PDR             |      5    |    3     |


- Gözlem nedir?
  - Her bir programda yer alan öğrencilerin cinsiyeti
- Değişkenler nelerdir?
  - Program, Cinsiyet, Frekans
- Değerler nelerdir?
    + Program: Olcme, Program, Yonetim, PDR
    + Cinsiyet: Kadın, Erkek 
- Bunların degisken değeri olması gerekiyor, sutun baslığı değil!
    + Frekans: ***Frekanslar iki sütuna dağılmış !!!**


## Düzgün Veri


| **Program**     | **Cinsiyet** | **Frekans** |
|-----------------|-------------:|------------:|
| Olcme           |     Kadın    |    6        |
| Olcme           |     Erkek    |    6        |
| Program         |     Kadın    |    5        |
| Program         |     Erkek    |    5        |
| Yonetim         |     Kadın    |    7        |
| Yonetim         |     Erkek    |    8        |
| PDR             |     Kadın    |    5        |
| PDR             |     Erkek    |    3        |


- Değişkenler sütunda



- Gözlemler Satırlarda olmalıdır !


- Çok sayıda **satırı** anlamlandırmak, çok sayıda **sütunu** anlamlandırmaktan daha kolaydır.

- **ggplot2**,**plotly**,**lattice** gibi paketleri rahat kullanabilmek için düzenli veri gereklidir.

- hiyerarşik ve karma modeller için de verinin düzgün olması önemlidir.

- Değişken adları mümkün olduğunca anlamlı olmalıdır.

- Eksik değerler ve **dengesiz** tekrarlanan ölçüm verileriyle ilgili daha az sorun sağlar.



- **tidyr** paketi **reshape** paketi gibi veri düzenlemede kullanılabilir.

- **gather()**: bir dizi sütun alır ve onları iki yeni sütuna (kendi adını verebileceğin) dönüştürür.

  - A key:  Orijinal sütun adlarını saklayan bir anahtar
  - A value: Bu orijinal sütunlardaki değerlere sahip bir değer.

## **gather()** fonksiyonu

- Fonksiyonun kullanım şekli

```r
gather(data, key, value, ..., na.rm = FALSE, 
       convert = FALSE, factor_key = FALSE)
```

- Fonksiyonun kullanımı göstermek için veri seti oluşturma


```r
n=20
genisveri <- data.frame(
  ID = paste("ID",101:120,sep=""),
  Sure_1 = sample(50:60,20,replace=TRUE),
  Sure_2 = sample(40:55,20,replace=TRUE),
  Sure_3 = sample(35:50,20,replace=TRUE)
)
```




```r
genisveri %>% head(6)
```

<div class="kable-table">

|ID    | Sure_1| Sure_2| Sure_3|
|:-----|------:|------:|------:|
|ID101 |     56|     52|     44|
|ID102 |     60|     48|     35|
|ID103 |     58|     47|     46|
|ID104 |     59|     41|     45|
|ID105 |     56|     55|     40|
|ID106 |     59|     52|     46|

</div>


- gather() fonksiyonu geniş veriyi, uzun veri haline getirir.


```r
uzun <- genisveri %>% gather(Sure, Zaman, Sure_1:Sure_3)
```

- Olusan veride Sure_1,Sure_2 ve Sure_3, Sure değişkenin değerleri haline geldi.



```r
uzun %>% head(3)
```

<div class="kable-table">

|ID    |Sure   | Zaman|
|:-----|:------|-----:|
|ID101 |Sure_1 |    56|
|ID102 |Sure_1 |    60|
|ID103 |Sure_1 |    58|

</div>


```r
uzun %>% tail(3)
```

<div class="kable-table">

|   |ID    |Sure   | Zaman|
|:--|:-----|:------|-----:|
|58 |ID118 |Sure_3 |    46|
|59 |ID119 |Sure_3 |    47|
|60 |ID120 |Sure_3 |    39|

</div>

- Gördüğünüz gibi, şimdi iki sütunumuz var: Biri *Sure* için, diğeri **Zaman** için. Her katılımcı icin üc farkli süre degeri olduğu için her bir ID değeri üç kere tekrarlamaktadır.


## **separate()**

- **separate()** bir sütunu birden çok sütuna ayırır.

- değerlerin sütun adlarına gömüldüğü toplanmış verilerde ortaktır.

- Olusan veride Sure_1,Sure_2 ve Sure_3 değerlerinin karakter ve sayısal değerlerini ayırmak için **separate():** fonkisyonu kullanabilirsiniz.



```r
uzun_ayrı <- uzun %>% 
            separate(Sure, c("Sure","Sayı"),"_") 

uzun_ayrı %>% head(3)
```

<div class="kable-table">

|ID    |Sure |Sayı | Zaman|
|:-----|:----|:----|-----:|
|ID101 |Sure |1    |    56|
|ID102 |Sure |1    |    60|
|ID103 |Sure |1    |    58|

</div>


## **unite()** fonksiyonu

- **gather*()** fonksiyonun tam tersi olarak iki sütunu alıp
tek sutunda birlestirir.


```r
uzun_birles <- uzun_ayrı %>% unite(SURE, Sure, Sayı, sep = ".")
uzun_birles %>% head(3)
```

<div class="kable-table">

|ID    |SURE   | Zaman|
|:-----|:------|-----:|
|ID101 |Sure.1 |    56|
|ID102 |Sure.1 |    60|
|ID103 |Sure.1 |    58|

</div>


## **spread()** fonksiyonu

- **spread():**  **gather*()** fonksiyonun tam tersini yaparak uzun veriden genis veri olusturmaya yarar.


```r
tekrar_genis <- uzun_birles %>% spread(SURE, Zaman)
tekrar_genis %>% head(6)
```

<div class="kable-table">

|ID    | Sure.1| Sure.2| Sure.3|
|:-----|------:|------:|------:|
|ID101 |     56|     52|     44|
|ID102 |     60|     48|     35|
|ID103 |     58|     47|     46|
|ID104 |     59|     41|     45|
|ID105 |     56|     55|     40|
|ID106 |     59|     52|     46|

</div>







