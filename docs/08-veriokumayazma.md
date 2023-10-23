# Veri Okuma ve Yazma

-   Veri girişi istatistiksel analiz sürecinin ilk adımıdır.

-   R'da veri girişi diğer yazılımlarla kıyaslandığında **çok kullanışlı değildir.**

-   Bu nedenle aktarma/import yolu tercih edilir.

-   Veri aktarımı için çok sayıda fonksiyon ve paket bulunmaktadır.

-   Ayrıca **menü ile de aktarma** yapılabilir.

-   Bilgisayardan internetten farklı formattaki veriler okunabilir.

-   Veri setleri genellikle Excel, SPSS veya metin dosyaları (.txt, .csv, .dat, vb.) gibi uygun veri biçimlerinde kaydedilir

-   R, çeşitli veri formatlarını içe aktarabilir (yani okuyabilir).

Bir veri setini R'ye aktarmanın iki yolu vardır:

1.  RStudio'da "Veri Kümesini İçe Aktar" menü seçeneğini kullanarak

![R studio](images/importmenu.png)

2.  Belirli bir R komutunu kullanarak

-   İçe aktarmak istediğiniz dosyaya göz atın.

-   Veri seti için bir isim verin.

-   İçe aktarılacak sayfayı seçin.

-   Değişken isimleri dosyanın ilk satırındaysa "First Row as Names".

![Excel dosylarını içe aktarma](images/excel1.png)

### SPSS dosylarını içe aktarma

-   İçe aktarmak istediğiniz dosyaya göz atın.

-   Veri seti için bir isim verin.

![SPSS dosylarını içe aktarma](images/spss1.png)

## Veri Okuma

-   En temel veri okuma/aktarma fonksiyonları

    -   `scan()`
    -   `read.*`
    -   `read.table()`
    -   `read.csv()`
    -   `read.csv2()`
    -   `read.delim()`
    -   `read.delim2()`
    -   `readLines()`

-   Verinin düzgün girilmiş olması okumayı kolaylaştırır.

-   İlk satırda genellikle değişken adlarına (header), ilk sütunda ise kimlik veya sıra numarasına yer verilir.

-   Gözlemlere ve değişkenlere ilişkin veri girilirken karakterler veya sayısal değerler arasında boşluk bırakmaktan kaçınmak gerekmektedir. Değişken adı boşluklu yazılmışsa ne olur?

-   Eksik veri boyunca aynı şekilde girilmelidir.

-   Değişkenlerin birinden nasıl ayrıldığı önemlidir. (, ; :  / )

-   Tercihimiz **.csv** uzantılı veriler ama büyük veri setleri az yer kalması icin **.txt,.prn** formatında karşımıza çıkabilmektedir.

-   Temel pakette **read.csv** ve **read.table** gibi bazı fonksiyonlar bulunmaktadır.

-   Ayrıca, belirli formatlarını içe aktarmak için R paketleri bulunmaktadır.Örneğin, SPSS dosyaları için **foreign** ve Excel dosyaları için **xlsx** gibi

## read.\*() fonksiyonları

| **Argüman**     | **Açıklama**                                                                                 |
|:-----------------------------------|:-----------------------------------|
| **header**      | Mantıksal değerler ile verinin ilk satırında değişken isimlerinin olup olmadığını test eder. |
| **sep**         | Sütun ayracıdır.                                                                             |
| **na.strings**  | Kayıp değerleri belirtmek için kullanılır.                                                   |
| **dec**         | Ondalık sayıların ne ile ayrıldığını gösteren argümandır.                                    |
| **nrows**       | Okunmak istenilen satır sayısını belirtmek için kullanılır.                                  |
| **skip**        | Bir dosya okunurken okunmadan atlanmak istenilen satır sayısı için kullanılır.               |

##  Excel dosyası aktarma


```r
# yükle ve aktive et 
install.packages("xlsx")
library("xlsx")

# read.xlsx fonksiyonunun kullanımı
my_excel_file <- read.xlsx("dizin/dosyaadi.xlsx",sheetName = "sheetname")
```

### SPSS dosyası aktarma


```r
# yükle ve aktive et 
install.packages("foreign")
library("foreign")

# read.spss fonksiyonunun kullanımı
my_spss_file <- read.spss("dizin/dosyaadi.sav",
                to.data.frame = TRUE)
```

### text dosyası aktarma

-   text dosyaları okumak için paket yüklemeye gerek yoktur.


```r
# , ile ayrılmış csv dosyaları
csv_dosya <- read.csv("dizin/dosyaadi.csv",header = TRUE)

# tab ile ayrılmış txt dosyaları
txt_dosya <- read.table("dizin/dosyaadi.txt",header = TRUE, sep = "\t")
```

-   Dikkat

-   `header = TRUE`

-   `sep="\t"`

-   `sep=","` for comma-separated files

-   

## Uygulama

-   🔗Dosyaları buradan klasör halinde indirebilirsiniz. [DOSYALAR](import/import.rar)

-   🔗[veri1.txt](import/veri1.txt)

<div class="kable-table">

|  no| m_1|  m_2| m_3|  m_4| m_5|
|---:|---:|----:|---:|----:|---:|
| 522|  12| 14.0|  16| 20.0|  10|
| 222|   5|   NA|  20| 10.0|  10|
| 454|   5| 10.2|   6|  4.0|  10|
| 567|  10| 20.0|  NA| 12.2|  20|

</div>


-   🔗[veri1.csv](import/veri1.csv)


<div class="kable-table">

|  no| m_1|  m_2| m_3|  m_4| m_5|
|---:|---:|----:|---:|----:|---:|
| 522|  12| 14.0|  16| 20.0|  10|
| 222|   5|   NA|  20| 10.0|  10|
| 454|   5| 10.2|   6|  4.0|  10|
| 567|  10| 20.0|  NA| 12.2|  20|

</div>

- 
<div class="kable-table">

|    |  No| M1|M2   | M3|M4   | M5|
|:---|---:|--:|:----|--:|:----|--:|
|001 | 522| 12|14   | 16|20   | 10|
|002 | 222|  5|NA   | 20|10   | 10|
|003 | 454|  5|10,2 |  6|4    | 10|
|004 | 567| 10|20   | NA|12,2 | 20|

</div>

- 
<div class="kable-table">

|    | M1|M2   | M3|M4   | M5|
|:---|--:|:----|--:|:----|--:|
|001 | 12|14   | 16|20   | 10|
|002 |  5|NA   | 20|10   | 10|
|003 |  5|10,2 |  6|4    | 10|
|004 | 10|20   | NA|12,2 | 20|

</div>


-   🔗[verifwf.txt](import/fwf.txt)
-

<div class="kable-table">

| V1|  V2|V3 | V4| V5| V6| V7| V8| V9| V10| V11| V12| V13|
|--:|---:|:--|--:|--:|--:|--:|--:|--:|---:|---:|---:|---:|
|  1| 689|A  |  1|  0|  1|  0|  1|  0|   1|   0|   1|   0|
|  2| 654|B  |  1|  1|  1|  1|  0|  1|   0|   1|   0|   1|
|  3| 436|A  |  1|  0|  1|  0|  1|  1|   1|   1|   1|   1|

</div>

- Değişkenlere isim verilmiş hali 

<div class="kable-table">

| sira|  no|kitapcik | m1| m2| m3| m4| m5| m6| m7| m8| m9| m10|
|----:|---:|:--------|--:|--:|--:|--:|--:|--:|--:|--:|--:|---:|
|    1| 689|A        |  1|  0|  1|  0|  1|  0|  1|  0|  1|   0|
|    2| 654|B        |  1|  1|  1|  1|  0|  1|  0|  1|  0|   1|
|    3| 436|A        |  1|  0|  1|  0|  1|  1|  1|  1|  1|   1|

</div>

-   🔗[factor.sav](import/factor.sav)

<div class="kable-table">

| id| bolge| puan|
|--:|-----:|----:|
|  1|     1|    9|
|  2|     1|    8|
|  3|     1|    6|
|  4|     1|    8|
|  5|     1|   10|
|  6|     1|    4|
|  7|     1|    6|
|  8|     1|    5|
|  9|     1|    7|
| 10|     1|    7|
| 11|     2|    7|
| 12|     2|    9|
| 13|     2|    6|
| 14|     2|    6|
| 15|     2|    6|
| 16|     2|   11|
| 17|     2|    6|
| 18|     2|    3|
| 19|     2|    8|
| 20|     2|    7|
| 21|     3|   11|
| 22|     3|   13|
| 23|     3|    8|
| 24|     3|    6|
| 25|     3|   14|
| 26|     3|   11|
| 27|     3|   13|
| 28|     3|   13|
| 29|     3|   10|
| 30|     3|   11|
| 31|     4|   12|
| 32|     4|   11|
| 33|     4|   16|
| 34|     4|   11|
| 35|     4|    9|
| 36|     4|   23|
| 37|     4|   12|
| 38|     4|   10|
| 39|     4|   19|
| 40|     4|   11|
| 41|     5|   10|
| 42|     5|   19|
| 43|     5|   14|
| 44|     5|    5|
| 45|     5|   10|
| 46|     5|   11|
| 47|     5|   14|
| 48|     5|   15|
| 49|     5|   11|
| 50|     5|   11|

</div>

```
## tibble [50 × 3] (S3: tbl_df/tbl/data.frame)
##  $ id   : num [1:50] 1 2 3 4 5 6 7 8 9 10 ...
##   ..- attr(*, "format.spss")= chr "F6.2"
##  $ bolge: num [1:50] 1 1 1 1 1 1 1 1 1 1 ...
##   ..- attr(*, "format.spss")= chr "F6.2"
##  $ puan : num [1:50] 9 8 6 8 10 4 6 5 7 7 ...
##   ..- attr(*, "format.spss")= chr "F6.2"
```


-   🔗 <https://www.statmodel.com/usersguide/chap3/ex3.1.dat>


```
##  [1] -0.354517  0.561655  0.315551  3.347049 -0.122389 -0.251276 -0.517996
##  [8]  1.888854  0.461254  2.237483
```

- 

```
##  [1] "   -0.354517     0.573051    -0.175230"
##  [2] "    0.561655    -0.368095     1.090042"
##  [3] "    0.315551    -0.577052     0.425472"
##  [4] "    3.347049     1.088520     1.149353"
##  [5] "   -0.122389    -0.694153    -0.766538"
##  [6] "   -0.251276    -0.017487    -1.367410"
##  [7] "   -0.517996    -0.817974    -1.559255"
##  [8] "    1.888854    -0.658335     1.007614"
##  [9] "    0.461254     0.463916    -0.898300"
## [10] "    2.237483     1.533398     0.180512"
```

## Veri Yazma


```r
ad  <-  c("Ali","Elif","Su","Deniz","Aras","Berk","Can","Ece","Efe","Arda")
boy <- c(160,165,170,155,167,162,169,158,160,164)
kilo <- c(50,55,57,50,48,65,58,62,45,47)
beden <- c("S","M","S","M","S","L","M","L","S","S")
df <- data.frame(ad, boy, kilo, beden)
df
```

<div class="kable-table">

|ad    | boy| kilo|beden |
|:-----|---:|----:|:-----|
|Ali   | 160|   50|S     |
|Elif  | 165|   55|M     |
|Su    | 170|   57|S     |
|Deniz | 155|   50|M     |
|Aras  | 167|   48|S     |
|Berk  | 162|   65|L     |
|Can   | 169|   58|M     |
|Ece   | 158|   62|L     |
|Efe   | 160|   45|S     |
|Arda  | 164|   47|S     |

</div>



```r
write.table(df, file="df.txt")# df dosyasi nerede, gorunumu nasil
```


```r
write.table(df, file="df.txt",row.names = FALSE,col.names = FALSE)
# karakter nesnler tirnak icinde ne yapmali?
```


```r
write.table(df, file="df.txt",row.names = FALSE,col.names = FALSE,quote=FALSE)
```



yeni gözlem eklemek istiyorsaniz append argümanı kullanılabilir.


```r
 ek <- data.frame(ad=c("Ahmet","Ali"), boy=c(180,170), kilo=c(60,70), 
                 beden=c("S","L"))
```


```r
write.table(ek, "df.txt",row.names=FALSE,
            col.names=FALSE,
            quote=FALSE,append=TRUE)
```


- **write.csv()** fonksiyonu kullanılarak yazılan veri dosyaları "," ile,

- **write.csv2()** fonksiyonu kullanılarak yazılan veri dosyaları ise ";" ile ayrılır iki fonksiyonun bir diğer farkı ise ondalık sayı ayıracıdır.

- write.csv ile yazdırılan dosyaların excelde açılması


### **cat()** fonksiyonu

-   Döngülerde sıklıkla ekrana bilgi yazdırmak amacıyla kullanılır, ancak dosya yazdırmak amacıyla da kullanabilmektedir.
-   fonksiyonlarla yapılan hesaplama çıktısı da yazabilmektedir.
-   Bu nedenle bir R oturumu sırasında not alınmak istenilen bilgileri bir dosyaya yazdırmak için kullanılabilir.


```r
 cat("ogrencilerin boy ortalamasi ", mean(boy), "\n",
      "ogrencilerin kilo ortalamasi", mean(kilo), "\n",
     file="bilgi.txt")
```

- \n ne ise yaradi?

## writeLines fonksiyonu


```r
writeLines("ogrencilerin boy ortalamasi: 163 cm\n",
            "ogrencilerin kilo ortalamasi: 53.7 kg",
            con="bilgi2.txt")
```

## ODEV

- 🔗 [Linkte](https://psyteachr.github.io/data-skills-v1/getting-to-know-the-data.html) yer alan sayfayı inceleyiniz. Bu sayfada  bir veri setini incelemeniz ve bu veri seti ile ilgili sorulara cevap vermeniz beklenemketedir.


- 🔗[Linkte](https://psyteachr.github.io/data-skills-v1/loading-data.html)  yer alan sayfada sizden iki veri setini okumanız beklenmeketdir. Bu iki veri setini okuduktan sonra da hazır kodları incelemeniz ve bu kodlar ile ilgili sorulara cevap vermeniz beklenmektedir.


☕ 
