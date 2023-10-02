# R Nesneler 

- Örnek bir veri seti


```r
library(tidyverse)
data(diamonds)
head(diamonds)
```

```
## # A tibble: 6 x 10
##   carat cut       color clarity depth table price     x     y     z
##   <dbl> <ord>     <ord> <ord>   <dbl> <dbl> <int> <dbl> <dbl> <dbl>
## 1  0.23 Ideal     E     SI2      61.5    55   326  3.95  3.98  2.43
## 2  0.21 Premium   E     SI1      59.8    61   326  3.89  3.84  2.31
## 3  0.23 Good      E     VS1      56.9    65   327  4.05  4.07  2.31
## 4  0.29 Premium   I     VS2      62.4    58   334  4.2   4.23  2.63
## 5  0.31 Good      J     SI2      63.3    58   335  4.34  4.35  2.75
## 6  0.24 Very Good J     VVS2     62.8    57   336  3.94  3.96  2.48
```


R nesne (object) yönelimli bir programlama dilidir.

-   Karakter (character)
-   Sayısal (numeric)
    -   tam sayı (integer)
    -   ondalıklı sayı (double)
    -   karmaşık sayı (complex)
-   Mantıksal (logical)
-   Faktör (factor)
-   Liste (list)
-   Fonksiyon (function)


## tam sayi
- tamsayı nesnesi oluşturulması

```r
tamsayi <- 2L
```
- tamsayi nesnesinin türünün sorgulanması

```r
typeof(tamsayi)
```

```
## [1] "integer"
```
- tamsayı nesnesinin yazdırılması


```r
tamsayi
```

```
## [1] 2
```


## ondalık sayı

- ondaliksayi nesnesinin oluşturulması

```r
ondaliksayi <- 2.5
```
- ondaliksayi nesnesinin türünün sorgulanması

```r
typeof(ondaliksayi)
```

```
## [1] "double"
```
- ondaliksayi nesnesinin yazdırılması

```r
ondaliksayi
```

```
## [1] 2.5
```


## İşlemler
- tek elemanlı vektörler

```r
x <- 1
y <- 1
```



```r
x+y
```

```
## [1] 2
```
- çok elemanlı vektörler


```r
x <- c(3,4,5)
y <- c(1,2,3)
# vektör eleman sayıları aynı mı?
length(x)==length(y)
```

```
## [1] TRUE
```


```r
x+y
```

```
## [1] 4 6 8
```


```r
x-y
```

```
## [1] 2 2 2
```


- çok elemanlı vektörler

```r
x <- 1:9
y <- c(1,2,3)
# vektör eleman sayıları farklı mı?
length(x)/length(y)
```

```
## [1] 3
```



```r
x+y
```

```
## [1]  2  4  6  5  7  9  8 10 12
```



```r
x/y
```

```
## [1] 1.0 1.0 1.0 4.0 2.5 2.0 7.0 4.0 3.0
```



- çok elemanlı vektörler


```r
x <- 1:5
y <- c(1,2)
# vektör eleman sayıları farklı olduğunda
length(x)/length(y)
```

```
## [1] 2.5
```

-   `x+y` işleminin sonucu nedir? _________


<div class='webex-solution'><button>Çözüm</button>



```r
x + y
```

```
## Warning in x + y: longer object length is not a multiple of shorter object
## length
```

```
## [1] 2 4 4 6 6
```


</div>



## Karakter Nesneler

- karakter nesnesi oluşturulması

```r
karakter <- "olcme"
```
- Oluşturulan nesnenin türünün sorgulanmasa

```r
typeof(karakter)
```

```
## [1] "character"
```

-  nesne yazdırılması

```r
karakter
```

```
## [1] "olcme"
```



```r
# karakter nesnesi oluşturulması
ad <- "Su"
soyad <- "Sevim"
```

- iki nesneyi arada  boşluk bırakarak birleştirir.

```r
paste(ad,soyad)
```

```
## [1] "Su Sevim"
```

- sep argümanı farklı şekillerde özelleştirilebilir.

```r
paste(ad,soyad, sep="")
```

```
## [1] "SuSevim"
```



```r
paste(ad,soyad,sep="_")
```

```
## [1] "Su_Sevim"
```

- base pakette yer alan bazı karakter vektörler bulunmaktadır.

```r
letters
```

```
##  [1] "a" "b" "c" "d" "e" "f" "g" "h" "i" "j" "k" "l" "m" "n" "o" "p" "q" "r" "s"
## [20] "t" "u" "v" "w" "x" "y" "z"
```



```r
LETTERS
```

```
##  [1] "A" "B" "C" "D" "E" "F" "G" "H" "I" "J" "K" "L" "M" "N" "O" "P" "Q" "R" "S"
## [20] "T" "U" "V" "W" "X" "Y" "Z"
```


```r
month.name
```

```
##  [1] "January"   "February"  "March"     "April"     "May"       "June"     
##  [7] "July"      "August"    "September" "October"   "November"  "December"
```


```r
month.abb
```

```
##  [1] "Jan" "Feb" "Mar" "Apr" "May" "Jun" "Jul" "Aug" "Sep" "Oct" "Nov" "Dec"
```

- Nesne birleştirme fonksiyonlarından en sık kullananı `paste()`
- `paste()` fonksiyonunun temel argümanları ise `sep` ve `collapse`'dir.


```r
harf5<- letters[1:5]
(harf51 <- paste(harf5,1:5,sep="_"))
```

```
## [1] "a_1" "b_2" "c_3" "d_4" "e_5"
```

```r
length(harf51)
```

```
## [1] 5
```



```r
(harf52 <- paste(harf5,1:5,sep="_",
                 collapse=" "))
```

```
## [1] "a_1 b_2 c_3 d_4 e_5"
```

```r
length(harf52)
```

```
## [1] 1
```



-   `paste()` fonksiyonun yardım sayfasını inceleyiniz.

### Günün Sorusu

-   Aşağıdaki çıktıyı oluşturacak olan kodu oluşturunuz.


```
##  [1] "1. maddenin guclugu: 0.25"  "2. maddenin guclugu: 0.74" 
##  [3] "3. maddenin guclugu: 0.02"  "4. maddenin guclugu: 0.87" 
##  [5] "5. maddenin guclugu: 0.46"  "6. maddenin guclugu: 0.27" 
##  [7] "7. maddenin guclugu: 0.25"  "8. maddenin guclugu: 0.95" 
##  [9] "9. maddenin guclugu: 0.59"  "10. maddenin guclugu: 0.15"
```

Bunun birden fazla yolu olabilir, farklı şekillerde yapabilirsiniz. 


**Büyük Küçük Harf Düzenleme Fonksiyonları** `toupper()` ve `tolower()`


```r
toupper(harf5)
```

```
## [1] "A" "B" "C" "D" "E"
```



```r
tolower(harf5)
```

```
## [1] "a" "b" "c" "d" "e"
```


`casefold()` fonksiyonu da upper argümanı ile birlikte kullanılabilir.



```r
casefold(harf5, upper = FALSE)
```

```
## [1] "a" "b" "c" "d" "e"
```



```r
casefold(harf5, upper = TRUE)
```

```
## [1] "A" "B" "C" "D" "E"
```

- Karakter nesnelerin kaç harften oluştuğu `nchar()` fonksiyonu ile belirlenebilir.

```r
nchar(month.name)
```

```
##  [1] 7 8 5 5 3 4 4 6 9 7 8 8
```
- Karakter nesneleri belli bir yerden bölmek icin `substr()` ve `substring()` fonksiyonları kullanılabilir.


```r
substr("YILMAZ", 1,3)
```

```
## [1] "YIL"
```


-  ```substring("YILMAZ", 1:.. , 1:6)``` kodunda  "Y" "I" "L" "M" "A" "Z" çıktısı oluşturacak kodu yazınız _

-   ````substring("YILMAZ", ... , 4:6)``` kodunda "ILM"   "ILMA"  "ILMAZ"` çıktınısı oluşturacak kodu yazınız _

- Karakter nesnelerde daha fazlası için aşağıdaki fonksiyonları inceleyebilirsiniz.

-   `strsplit()`
-   `noquote()`
-   `cat()`
-   `grep()`
-   `duplicated()`
-   `agrep()`


## Mantıksal Nesneler


```r
mantiksal1 <-TRUE
```



```r
typeof(mantiksal1)
```

```
## [1] "logical"
```



```r
mantiksal1
```

```
## [1] TRUE
```

Mantıksal operatörler programlamanın temeli ve vazgeçilmezidir.



```r
# eşitlik sınaması
T==TRUE
```

```
## [1] TRUE
```

-   `4==5` kodunun sonucu nedir? _____

-   `4<5` kodunun sonucu nedir? ____

-   `10>100` kodunun sonucu nedir? _____



- Mantıksal operatörlerle yapılan sınamalar ile mantıksal nesneler oluşturulur.


```r
sonuc <- 4<5
typeof(sonuc)
```

```
## [1] "logical"
```


- Nesne türleri arasındaki değişim uygunluk durumuna göre `as.*()`fonksiyonları ile sağlanır.


```r
# Karakter veri numerik veriye
as.numeric("3.14")
```

```
## [1] 3.14
```


```r
# ondalık verin tam sayıya
as.integer(pi)
```

```
## [1] 3
```


```r
# karakter veri numerik veriye (NA)
as.numeric("olcme")
```

```
## Warning: NAs introduced by coercion
```

```
## [1] NA
```




```r
# mantıksal veri karakter veriye (NA)
as.character(TRUE)
```

```
## [1] "TRUE"
```


```r
# numerik veri karakter veriye
as.character(10)
```

```
## [1] "10"
```


```r
# mantıksal veri numerik veriye
as.numeric(TRUE)
```

```
## [1] 1
```



## Nesne Türleri Sorgulama

- Nesne türleri sorgulamak için ise `class()` ya da `mode()` fonksiyonları kullanabilir. Ancak bir nesne türüne ait olup olmadığını sorgulamak için ise `is.*()` fonksiyonları kullanılır.


```r
x<- 3.14; class(x)
```

```
## [1] "numeric"
```

```r
is.numeric(x)
```

```
## [1] TRUE
```

```r
is.logical(x)
```

```
## [1] FALSE
```


- Sayısal nesnelerin türü için `typeof()` fonksiyonu da kullanılabilir.


```r
y <- 2L; typeof(y); class(y) # satir içi kod ayırma
```

```
## [1] "integer"
## [1] "integer"
```

```r
is.integer(y)
```

```
## [1] TRUE
```

```r
is.double(y)
```

```
## [1] FALSE
```


### Günün Sorusu 

- aşağıda yer alan **ad_soyad** nesnesini kullanarak


```r
ad_soyad<- c("Ayse-Sel","Can-Yucel","Cem-Togay","Banu-Cift")
```



aşağıdaki çıktıyı oluşturmaya calisiniz.


```
## [1] "Ayse" "Can"  "Cem"  "Banu"
## [1] "Sel"   "Yucel" "Togay" "Cift"
```

