# Vektörler

-   R lineer cebir temelli bir programlama dilidir.

-   Vektörler tek boyutludur.

-   R'da vektörler birleştirmek (combine/concatenate) anlamına gelen `c()` fonksiyonu ile oluşturulmaktadır.

-   R da veriler bir araya gelerek veri yapılarını oluşturur.

    -   vektör (vector)
    -   liste (list)
    -   matris (matrix)
    -   veri seti (data.frame)
    -   dizi (array)

## Vektör Oluşturma


```r
(sayisal_vektor <-  c(1,2,3))
```

```
## [1] 1 2 3
```


```r
(karakter_vektor <-  c("a","b","c"))  ## cift tirnak
```

```
## [1] "a" "b" "c"
```


```r
(mantiksal_vektor <- c(TRUE,TRUE,FALSE))
```

```
## [1]  TRUE  TRUE FALSE
```

## Vektör İşlemleri

-   Vektör uzunluğu `length()` fonksiyonu ile vektör türleri ise `class()`, `mode()` ya da `typeof()` fonksiyonları ise tur belirlemek için kullanılmaktadır.

-   Vektörler bir veya daha fazla elemandan oluşabilmektedir.


```r
a <- 1  # tek elemandan oluşur.
# Vektör uzunluğunu öğrenmek icin length() fonksiyonu
length(a)
```

```
## [1] 1
```


```r
x <- 1:10
```

-   bir vektöründeki verilerin toplanması `sum(x)` 55

-   bir vektöründeki verilerin çarpılması `prod(x)` 3.6288\times 10^{6}

-   bir vektöründeki verilerin küçükten büyüğe sıralanması `sort(x)` 1, 2, 3, 4, 5, 6, 7, 8, 9, 10

-   bir vektörünün elemanların sıralarının tersine çevrilmesi `rev(x)` 10, 9, 8, 7, 6, 5, 4, 3, 2, 1

-   bir vektöründeki verilerin standart sapmasının hesaplanması `sd(x)` 3.0276504

-   bir vektöründeki en büyük verinin gösterilmesi `max(x)` 10

-   bir vektöründeki en küçük verinin gösterilmesi `min(x)` 1

-   En büyük verinin vektörün kaçıncı elemanı olduğunun gösterilmesi `which.max(x)` 10

-   En küçük verinin vektörün kaçıncı elemanı olduğunun gösterilmesi `which.min(x)` 1

-   Vektörlerden eleman sırası, isim ve mantıksal operatörler olmak üzere üç farklı yolla eleman seçilebilir.


```r
ad  <-  c("Ali","Elif","Su","Deniz",
"Aras","Berk","Can","Ece","Efe","Arda")
```

-   ad vektörünün 1. elemanı `ad[1]` Ali

-   ad vektörünün 5. elemanını yazdıracak kodu oluşturunuz. <input class='webex-solveme nospaces' size='5' data-answer='["ad[5]"]'/>

-   ad vektörünün son elemanını yazdıracak kodu oluşturunuz. <input class='webex-solveme nospaces' size='6' data-answer='["ad[10]"]'/>

-   ad vektörünün son elemanını yazdıracak kodu vektörün 10 elemanlı olduğunu bilmediğiniz de ne yaparsınız? <input class='webex-solveme nospaces' size='14' data-answer='["ad[length(ad)]"]'/>

-   Vektörün sadece 1., 5. 8 elemanının yazdıracak kodu oluşturunuz.<input class='webex-solveme nospaces' size='12' data-answer='["ad[c(1,5,8)]"]'/>

-   Vektörün sadece 1. elemanının hariç tutacak kodu oluşturunuz <input class='webex-solveme nospaces' size='6' data-answer='["ad[-1]"]'/>

-   Vektörün 1. ve 5. elemanının hariç tutacak kodu oluşturunuz <input class='webex-solveme nospaces' size='11' data-answer='["ad[-c(1,5)]"]'/>

-   Vektörün son üç elemanını yazdıracak kodu oluşturunuz <input class='webex-solveme nospaces' size='8' data-answer='["ad[8:10]"]'/>

## Vektöre eleman eklenmesi


```r
ad[11] <- "Asu"; ad
```

```
##  [1] "Ali"   "Elif"  "Su"    "Deniz" "Aras"  "Berk"  "Can"   "Ece"   "Efe"  
## [10] "Arda"  "Asu"
```

-   vektöre birden fazla eleman eklenmesi


```r
ad[12:13] <- c("Ahu","Han"); ad
```

```
##  [1] "Ali"   "Elif"  "Su"    "Deniz" "Aras"  "Berk"  "Can"   "Ece"   "Efe"  
## [10] "Arda"  "Asu"   "Ahu"   "Han"
```

-   Vektörün ortasına eleman eklenmesi **append()** fonksiyonu ile yapılabilir. Fonksiyon yardım sayfasını inceleyiniz.


```r
(ad <- append(ad, "Taha", after = 3))
```

```
##  [1] "Ali"   "Elif"  "Su"    "Taha"  "Deniz" "Aras"  "Berk"  "Can"   "Ece"  
## [10] "Efe"   "Arda"  "Asu"   "Ahu"   "Han"
```

-   ya da `c()` fonksiyonu ile yapılabilir.


```r
ad <- c(ad[1:5],"Selim",ad[7:length(ad)]); ad
```

```
##  [1] "Ali"   "Elif"  "Su"    "Taha"  "Deniz" "Selim" "Berk"  "Can"   "Ece"  
## [10] "Efe"   "Arda"  "Asu"   "Ahu"   "Han"
```

## Alıştırma

-   10 kişiden oluşan bir gruptaki kişilerinin boy ve kilo ölçümleri için ise aşağıdaki vektör oluşturulmuştur.


```r
ad  <-  c("Ali","Elif","Su","Deniz",
"Aras","Berk","Can","Ece","Efe","Arda")
boy <- c(160,165,170,155,167,162,169,158,160,164)
kilo <-c(50,55,57,50,48,65,58,62,45,47)
```

-   Eğer elimizdeki vektör isimlendirilmiş bir vektör ise eleman seçimini isimle de yapabiliriz.


```r
#isimsiz boy vektoru
names(boy) # names() fonksiyonu ile isimlendirme yapılabilir.
```

```
## NULL
```

-   ad vektörünü boy vektörünü isimlendirirken nasıl kullanabiliriz? <input class='webex-solveme nospaces' size='16' data-answer='["names(boy) <- ad"]'/>

-   Arda 'nın boyunu isimlendirilmiş vektörü kullanarak nasıl yazdırırsınız? `r `fitb("boy["Arda"]")`

## Örüntülerle Vektör Oluşturma

-   Vektör oluşturmanın farklı yolları bulunmaktadır.

-   En basit yolu iki nokta `":"` operatörünü kullanmaktır.


```r
rakamlar <- 0:9
rakamlar
```

```
##  [1] 0 1 2 3 4 5 6 7 8 9
```

-   büyükten küçüğe rakamlardan vektör oluşturulması


```r
rakamlar <- 9:0
rakamlar
```

```
##  [1] 9 8 7 6 5 4 3 2 1 0
```

### seq()

-   Belirli bir kurala göre sayı dizileri oluşturmak için ise `seq()`, `rep()` ve `paste()` fonksiyonlarından yararlanılabilir. İlk olarak bu fonksiyonların yardım sayfalarını inceleyelim.

-   1'den 10'a kadar birer birer artan sayılardan dizi oluşturulacak kodu oluşturunuz. `seq(from=1,to=10,by=...)` <input class='webex-solveme nospaces' size='1' data-answer='["1"]'/>

-   Bir önceki işlemi argümansız olarak oluşturunuz. <input class='webex-solveme nospaces' size='11' data-answer='["seq(1,10,1)"]'/>

-   Aynı çıktıyı tek bir argümanla elde edebilir misiniz? <input class='webex-solveme nospaces' size='10' data-answer='["seq(to=10)"]'/>

-   length argümanını kullanarak aşağıdaki çıktıyı oluşturacak kodu oluşturunuz. <input class='webex-solveme nospaces' size='25' data-answer='["seq(from=1,to=3,length=6)"]'/>


```
## [1] 1.0 1.4 1.8 2.2 2.6 3.0
```

-   by argümanını ile artış miktarını kullanarak aşağıdaki çıktıyı oluşturacak kodu oluşturunuz. <input class='webex-solveme nospaces' size='23' data-answer='["seq(from=1,to=3,by=0.5)"]'/>


```
## [1] 1.0 1.5 2.0 2.5 3.0
```

-   Belirli bir aralıkta kaç elemanın yer alacağını length.out argümanı kullanarak aşağıdaki çıktıyı oluşturacak kodu oluşturunuz. <input class='webex-solveme nospaces' size='29' data-answer='["seq(from=1,to=3,length.out=5)"]'/>


```
## [1] 1.0 1.5 2.0 2.5 3.0
```

### rep()

`rep()` fonksiyonu için örnekler


```r
# üç elemanlı bir vektörün üç kere tekrar ettirilmesi
rep(c(3,4,5), 3)
```

```
## [1] 3 4 5 3 4 5 3 4 5
```


```r
# rakamların üç kere tekrar ettirilmesi
rep(0:9, times = 3) 
```

```
##  [1] 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9
```

-   `a <- c(3,5,7)` vektörünü kullanarak aşağıdaki çıktıyı elde edecek kodu hazırlayınız. <input class='webex-solveme nospaces' size='13' data-answer='["rep(a,each=3)"]'/>


```
## [1] 3 3 3 5 5 5 7 7 7
```

-   `a <- c(3,5,7)` vektörünü kullanarak aşağıdaki çıktıyı elde edecek kodu hazırlayınız. <input class='webex-solveme nospaces' size='21' data-answer='["rep(a,each=3,times=3)"]'/>


```
##  [1] 3 3 3 5 5 5 7 7 7 3 3 3 5 5 5 7 7 7 3 3 3 5 5 5 7 7 7
```

-   Çıktıyı elde edecek kodu hazırlayınız. <input class='webex-solveme nospaces' size='10' data-answer='["rep(1:4,2)"]'/>


```
## [1] 1 1 2 2 3 3 4 4
```

-   Çıktıyı elde edecek kodu hazırlayınız. <input class='webex-solveme nospaces' size='12' data-answer='["rep(1:3,1:3)"]'/>


```
## [1] 1 2 2 3 3 3
```

### paste()

-   `paste()`fonksiyonu çıktısı her zaman için karakterdir.


```r
paste(1:4) # çıktısı karakterdir
```

```
## [1] "1" "2" "3" "4"
```


```r
class(paste(1:4))
```

```
## [1] "character"
```
   
-   Çıktıyı elde edecek kodu tamamlayınız `paste("test",...)` <input class='webex-solveme nospaces' size='4' data-answer='["1:10"]'/>


```
##  [1] "test 1"  "test 2"  "test 3"  "test 4"  "test 5"  "test 6"  "test 7" 
##  [8] "test 8"  "test 9"  "test 10"
```


-   Çıktıyı elde edecek kodu tamamlayınız`paste("test",1:10,"...",sep="_")` <input class='webex-solveme nospaces' size='4' data-answer='["puan"]'/>


```
##  [1] "test_1_puan"  "test_2_puan"  "test_3_puan"  "test_4_puan"  "test_5_puan" 
##  [6] "test_6_puan"  "test_7_puan"  "test_8_puan"  "test_9_puan"  "test_10_puan"
```

-   Çıktıyı elde edecek kodu tamamlayınız `paste("test",c("A","B","C","D",...))`  <input class='webex-solveme nospaces' size='3' data-answer='["1:4"]'/> 


```
## [1] "test A" "test B" "test C" "test D" "test 1" "test 2" "test 3" "test 4"
```

## Rasgele Veri Oluşturma

-   Farklı fonksiyonlarla rastgele veri üretilebilir. Örneğin 0-100 arasında 20 farklı değer elde edilmek istenilsin. Bunu yapmak için `sample()`,`runif()` ya da `rnorm()` fonksiyonlarından yararlanılabilir.


```r
sample(0:100,5)
```

```
## [1] 61 63  7 60  2
```


```r
runif(10,  0, 5)
```

```
##  [1] 2.47451425 1.47840320 1.02943342 4.72612762 2.90453063 0.06331178
##  [7] 3.83463970 0.53442583 2.52640137 4.68727539
```


```r
rnorm(10,50,5)
```

```
##  [1] 54.42424 49.95763 37.96132 53.74404 45.71543 40.29669 41.73731 57.62644
##  [9] 54.51408 49.25207
```

-   Kullanılan üç fonksiyonun da yardım sayfalarını ve kullanım amaçlarını inceleyiniz.

## İşlemler

BKI vücut ağırlığınızın metre cinsinden boy uzunluğunun karesine bölünmesi ile elde edilmektedir. Her bir bireye ait BKI değerini hesaplayınız. BKI derğerlerinin ortalaması kaçtır(iki ondalığa yuvarlayınız)?  <input class='webex-solveme nospaces' size='5' data-answer='["20.44"]'/> 


```r
ad  <-  c("Ali","Elif","Su","Deniz","Aras","Berk","Can","Ece","Efe","Arda")
boy <- c(160,165,170,155,167,162,169,158,160,164)
kilo <- c(55,55,57,50,48,65,58,62,45,47)
```


<div class='webex-solution'><button>Çözüm!,bakmadan yapmalısın!</button>



```r
# BKI  hesaplanması
boy_m  <- boy/100
BKI <- kilo/( boy_m * boy_m)
BKI
round(mean(BKI),2)
```

```
##  [1] 21.48437 20.20202 19.72318 20.81165 17.21109 24.76757 20.30741 24.83576
##  [9] 17.57812 17.47472
## [1] 20.44
```

</div>


### Kendinizi Test Edin

**S1.** Aşağıdaki tabloda yer alan üç sütun için birer vektör oluşturunuz. Öğrencilerin geçme notu her iki sınavın ortalaması olarak hesaplanacaktır. Bu öğrencilerin geçme notlarını hesaplayınız. Geçme notlarının betimsel istatistiklerini hesaplayınız.

| Öğrenci | Vize | Final |
|---|---|---|
| Ogrenci1 | 50 | 45 | 
| Ogrenci2 | 55 | 65 | 
| Ogrenci3 | 60 | 85 | 
| Ogrenci4 | 70 | 90 | 
| Ogrenci5 | 80 | 85 |

Geçme notlarının minumum değeri: <input class='webex-solveme nospaces' size='4' data-answer='["47.5"]'/>

Geçme notlarının ortalama değeri: <input class='webex-solveme nospaces' size='4' data-answer='["68.5"]'/>

Geçme notlarının maksimum değeri: <input class='webex-solveme nospaces' size='4' data-answer='["82.5"]'/>





**S2.**  Birden n'e kadar olan sayların toplamını hesaplayan fonksiyon yazımı `toplam()` tek argümanlı fonksiyon oluşturunuz. Argüman değeri 5 olduğunda 1+2+3+4+5=15 değerini versin.

-   birden n'e kadar olan sayların toplamı: (n\*(n+1))/2


**S3.** 1'den n' e kadar olan sayıların toplamını hesaplayan fonksiyonu argümansız olarak aşağıdaki şekilde yazmayı deneyiniz. Fonksiyonu çalıştırdığınızda ekranda/konsolda kaça kadar olan sayların toplamı hesaplansın: yazsın, kullanıcının girdiği değere göre aşağıda çıktısı çıksın.


```r
toplam()

kaça kadar olan sayların toplamı hesaplansın: 10

[1 " 10 'e kadar olan sayların toplamı: 55
```


## **ODEV**

-   Kitap Bölüm 2 1. Soruyu tamamlayınız.

-   swirl package - learn R in R (Programming ilk 6 modul)

-   datacamp ödevinizi yapmayını unutmayın 😄
