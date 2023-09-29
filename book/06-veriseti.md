# Veri Setleri

- Veri setleri iki boyutludur.

- R'da bir çok fonksiyonun veri setleri ile çalışmaktadır. 

- Veri setleri R ortamında `data.frame()` fonksiyonu ile oluşturulabilir.

- `data.frame()` fonksiyonu ile aynı uzunluktaki vektörlerden bir veri seti oluşturulabilir.



```r
ad  <-  c("Ali","Elif","Su","Deniz","Aras", "Berk","Can","Ece","Efe","Arda")
boy <- c(160,165,170,155,167,162, 169,158,160,164)
kilo <- c(55,55,57,50,48,65, 58,62,45,47)
beden <- c("S","M","S","M","S", "L","M","L","S","S")
beden <- factor(beden)


(df <- data.frame(ad,boy, kilo, beden))
```

```
##       ad boy kilo beden
## 1    Ali 160   55     S
## 2   Elif 165   55     M
## 3     Su 170   57     S
## 4  Deniz 155   50     M
## 5   Aras 167   48     S
## 6   Berk 162   65     L
## 7    Can 169   58     M
## 8    Ece 158   62     L
## 9    Efe 160   45     S
## 10  Arda 164   47     S
```

- Eğer uzunlukları farklı olan vektörlerle veri setleri oluşturulmaya çalışılırsa kısa vektör, uzun vektör uzunluğunda tekrar eder.


```r
# 4 farklı uzunlukta vektör oluşturulması
x <- 11:14; y <- 10; M <- c(10,35); N <- 2:4
```



```r
data.frame(x, y) # (4,1)
```

```
##    x  y
## 1 11 10
## 2 12 10
## 3 13 10
## 4 14 10
```



```r
data.frame(x, M) # (4,2)
```

```
##    x  M
## 1 11 10
## 2 12 35
## 3 13 10
## 4 14 35
```




```r
data.frame(x,N)  #(4,3) hata
```

```
## Error in data.frame(x, N): arguments imply differing number of rows: 4, 3
```



```r
data.frame(y, M) #(1,2)
```

```
##    y  M
## 1 10 10
## 2 10 35
```



```r
data.frame(y, N) #(1,3)
```

```
##    y N
## 1 10 2
## 2 10 3
## 3 10 4
```


```r
data.frame(M, N) #(2,3)
```

```
## Error in data.frame(M, N): arguments imply differing number of rows: 2, 3
```

## Hazır Veri Setleri

- Temel pakette yer alan veri setlerinin bir listesine aşağıdaki komutla ulaşabilirsiniz.


```r
data() # yeni bir pencerede açılır.
```

- Veri setlerinin yer aldığı paketlerde bulunmaktadır.


```r
# install.packages("datasets")
library (datasets)
# install.packages("dslabs")
library (dslabs)
```

- Hazır veri setleri çalışma ortamına `data()` fonksiyonu ile aktarılabilir.


```r
data(WorldPhones) # environmete kontrol ediniz. 
```

- hazır veri setlerini incelememek için aşağıdaki komutlar kullanılabilir. 


```r
data(cars) # enviromente ekler
iris      # enviromente eklemez!
```

## İnceleme

- Boyut sorgulamamak için farklı fonksiyonlar kullanılabilir.


```r
dim(cars) # satir Sutun
```

```
## [1] 50  2
```


```r
nrow(cars)
```

```
## [1] 50
```


```r
ncol(cars)
```

```
## [1] 2
```


- Veri setlerin ilk satırları `head()`, son satırları ise `tail()` fonksiyonu ile incelenebilir. `head()` fonksiyonu olağan olarak ilk 6 satırı yazdırır.


```r
head(WorldPhones)
```

```
##      N.Amer Europe Asia S.Amer Oceania Africa Mid.Amer
## 1951  45939  21574 2876   1815    1646     89      555
## 1956  60423  29990 4708   2568    2366   1411      733
## 1957  64721  32510 5230   2695    2526   1546      773
## 1958  68484  35218 6662   2845    2691   1663      836
## 1959  71799  37598 6856   3000    2868   1769      911
## 1960  76036  40341 8220   3145    3054   1905     1008
```

- Yazdırılacak satır sayısı `n` argümanı ile ayarlanır.

```r
head(WorldPhones,n=2)
```

```
##      N.Amer Europe Asia S.Amer Oceania Africa Mid.Amer
## 1951  45939  21574 2876   1815    1646     89      555
## 1956  60423  29990 4708   2568    2366   1411      733
```

- WorldPhones veri setinin son 8 satırını yazdıracak kodu yazınız. _____________________

- `datasets` paketinde yer alan veri setlerinde `examples()` bölümünde çeşitli örneklere yer verilmiştir. Örneğin `example(WorldPhones)`


```r
matplot(rownames(WorldPhones), WorldPhones, type = "b", log = "y",
        xlab = "Year", ylab = "Number of telephones (1000's)")
legend("bottomright", colnames(WorldPhones), col = 1:6, lty = 1:5,
       pch = rep(21, 7))
title(main = "World phones data: log scale for response")
```



\begin{center}\includegraphics[width=1\linewidth]{06-veriseti_files/figure-latex/unnamed-chunk-18-1} \end{center}


-  Temel paket hariç diğer paketlerdeki veri setlerine `data(veriseti, package="packagename")` şeklinde ulaşılabilir.


```r
data(CTTdata, package="CTT") 
head(CTTdata)
```

- 🔗[sık kullanılan veri setleri ile ilgili bir yazı:](http://r-tutorials.com/famous-useful-pre-installed-exercise-datasets-r/)

- 🔗[tüm veri setlerine ulaşabilmek için ise:](https://vincentarelbundock.github.io/Rdatasets/datasets.html)



- Kullanışlı olmasa da excel, spps gibi veri girişi sağlayan bir arayüz bulunmaktadır.


- Ali, Su ve Ece'nin boylarının ve kilolarının seçilmesi

```r
df1<- data.frame() 
df1 <- edit(df1)
# duzenlemek icin
fix(df)
# gozatmak icin 
View(df)
```


## Elaman Seçme

Veri setlerinde eleman seçme matrislerdeki gibidir.

`df[satirindeks, sutunindeks]`



- df'nin birinci satir elemanlarının seçilmesi  ______


```
##    ad boy kilo beden
## 1 Ali 160   55     S
```

- df'nin birinci sütun elemanlarının seçilmesi  ______
 

```
##  [1] "Ali"   "Elif"  "Su"    "Deniz" "Aras"  "Berk"  "Can"   "Ece"   "Efe"  
## [10] "Arda"
```

- df'nin ikinci satir elemanlarının seçilmesi  ______

 

```
##     ad boy kilo beden
## 2 Elif 165   55     M
```

- df'nin ikinci sütun elemanlarının seçilmesi   ______


```
##  [1] 160 165 170 155 167 162 169 158 160 164
```

- df'nin birinci satir üçüncü sütun elemanlarının seçilmesi  _______


```
## [1] 55
```

- Veri setlerinde satır elemanları yazdırıldığında veri seti (`data.frame)`, sütun elemanları yazdırıldığında ise vektör (`vector)` oluşmaktadır.


```r
# satir secimi
is.data.frame(df[1,])
```

```
## [1] TRUE
```


```r
# sutun secimi
is.data.frame(df[,1])
```

```
## [1] FALSE
```

- Sütun seçimi veri seti (`data.frame`) olarak yapılmak istenirse, `drop` argümanı FALSE değeri ile kullanılır.


```r
df[,1,drop=FALSE]
```

```
##       ad
## 1    Ali
## 2   Elif
## 3     Su
## 4  Deniz
## 5   Aras
## 6   Berk
## 7    Can
## 8    Ece
## 9    Efe
## 10  Arda
```


- Veri seçim işlemi için `subset()` fonksiyonu kullanılabilir.

- `?subset` bir fonksiyonu ilk daha kullanıyorsanız, mutlaka yardım sayfasını inceleyin. 

`subset(veriseti, kosul/Kosullar)`

- Boyu 165cm den uzun öğrencilerin bilgilerinin seçilmesi


```r
subset(df, boy >165)
```

```
##     ad boy kilo beden
## 3   Su 170   57     S
## 5 Aras 167   48     S
## 7  Can 169   58     M
```


- `subset()` Fonksiyonun yardım sayfasındaki örnekleri inceleyebilirsiniz.


```r
subset(airquality, Temp > 90,select = c(Ozone, Temp))
```

```
##     Ozone Temp
## 42     NA   93
## 43     NA   92
## 69     97   92
## 70     97   92
## 75     NA   91
## 102    NA   92
## 120    76   97
## 121   118   94
## 122    84   96
## 123    85   94
## 124    96   91
## 125    78   92
## 126    73   93
## 127    91   93
```



```r
subset(airquality, Day == 1, select = -Temp)
```

```
##     Ozone Solar.R Wind Month Day
## 1      41     190  7.4     5   1
## 32     NA     286  8.6     6   1
## 62    135     269  4.1     7   1
## 93     39      83  6.9     8   1
## 124    96     167  6.9     9   1
```

- df verisinde beden değişkeni "S" olan satırların seçimi  `subset(df,beden =="S")` 


- df verisinde kilosu 50'in altında olan kişilerden oluşan veri seti oluşturma kodunu tamamlayınız `subset(df,.......)` _______


## Eleman ekleme 

- Veri setine yeni sütun ekleme isleme `$` operatörü ile `[[]]` operatörü ile `cbind()` fonksiyonları ile yapılabilmektedir.


```r
df2 <- data.frame(
      S1 = sample(0:100,20),
      S2 = runif(n=20 ,min= 50 , max=70)
)
head(df2)
```

```
##   S1       S2
## 1 74 59.14235
## 2 35 63.80176
## 3 73 58.80158
## 4  7 53.06840
## 5 95 61.69417
## 6 37 50.80832
```


- `$` operatörü ile sütun ekleme


```r
df2$S3 <- sample(60:80,20,replace = TRUE)
head(df2)
```

```
##   S1       S2 S3
## 1 74 59.14235 63
## 2 35 63.80176 74
## 3 73 58.80158 69
## 4  7 53.06840 80
## 5 95 61.69417 79
## 6 37 50.80832 67
```

- `[[]]` operatörü ile sütun ekleme

- df2 veri setinin ilk üç sütunun `rowMeans()` fonksiyonu ile ortalamasının alınarak ort isimi ile veri setine eklenmesi


```r
df2[["ort"]] <- round(rowMeans(df2),2)
head(df2)
```

```
##   S1       S2 S3   ort
## 1 74 59.14235 63 65.38
## 2 35 63.80176 74 57.60
## 3 73 58.80158 69 66.93
## 4  7 53.06840 80 46.69
## 5 95 61.69417 79 78.56
## 6 37 50.80832 67 51.60
```


- `cbind()` fonksiyonu ile sütun ekleme


```r
cbind( df2, S4 = 10)
```

```
##    S1       S2 S3   ort S4
## 1  74 59.14235 63 65.38 10
## 2  35 63.80176 74 57.60 10
## 3  73 58.80158 69 66.93 10
## 4   7 53.06840 80 46.69 10
## 5  95 61.69417 79 78.56 10
## 6  37 50.80832 67 51.60 10
## 7  20 63.49927 62 48.50 10
## 8  48 56.93782 77 60.65 10
## 9  78 69.27810 65 70.76 10
## 10  4 51.10366 77 44.03 10
## 11 76 52.59946 60 62.87 10
## 12 36 68.21928 77 60.41 10
## 13 60 58.42029 75 64.47 10
## 14 84 60.37701 65 69.79 10
## 15 63 51.02440 76 63.34 10
## 16  1 55.34202 62 39.45 10
## 17 38 58.90600 60 52.30 10
## 18 81 65.55860 65 70.52 10
## 19 34 59.16738 64 52.39 10
## 20 85 51.07855 79 71.69 10
```


## Eleman çıkarma 

- Veri setinden istenilen sütunun çıkarılabilir. Bu işlemi yapmak için iki farklı yol kullanılabilir. 

- `-` operatörü


```r
head(df2,3)
```

```
##   S1       S2 S3   ort
## 1 74 59.14235 63 65.38
## 2 35 63.80176 74 57.60
## 3 73 58.80158 69 66.93
```


```r
df2 <- df2[,-4] 
head(df2,3)
```

```
##   S1       S2 S3
## 1 74 59.14235 63
## 2 35 63.80176 74
## 3 73 58.80158 69
```

- `NULL` operatörü


```r
df2$S3 <- NULL
head(df2,3)
```

```
##   S1       S2
## 1 74 59.14235
## 2 35 63.80176
## 3 73 58.80158
```


## Satır ekleme 

- Veri setlerine değişken ekleyip, çıkarabileceğiniz gibi gözlem de ekleyip, çıkarabilirsiniz. Veri setine iki satır ekleme


```r
dim(df2)
```

```
## [1] 20  2
```


```r
# eklenecek iki satırlık veri seti oluşturma
df3 <- data.frame(S1=c(50,60),S2=c(55.3,65.5))
# yeni veri seti
df4 <- rbind (df2,df3)
dim(df4)
```

```
## [1] 22  2
```

## Veri yapısı inceleme

- Veri setlerinin yapısını incelemek icin `str()` fonksiyonundan yararlanılmaktadır.


```r
str(df)
```

```
## 'data.frame':	10 obs. of  4 variables:
##  $ ad   : chr  "Ali" "Elif" "Su" "Deniz" ...
##  $ boy  : num  160 165 170 155 167 162 169 158 160 164
##  $ kilo : num  55 55 57 50 48 65 58 62 45 47
##  $ beden: Factor w/ 3 levels "L","M","S": 3 2 3 2 3 1 2 1 3 3
```

- "df" veri seti 10 gözlemden, 4 değişken. Her bir değişkenin önünde `$` operatörü olduğuna dikkat ediniz.



- veri setinin incelenmek için kullanılabilecek diğer fonksiyon ise `attributes()`


```r
attributes(df)
```

```
## $names
## [1] "ad"    "boy"   "kilo"  "beden"
## 
## $class
## [1] "data.frame"
## 
## $row.names
##  [1]  1  2  3  4  5  6  7  8  9 10
```


## Isimlendirme

- Veri setleri vektör birleştirme üzerinden yapılırsa, vektör adları sütun ismi olarak kullanılır. Ancak bu isimler değiştirilebilir. Bu işlem `data.frame()` fonksiyonu içinde yapılabilir.


```r
df <- data.frame(isim = ad,
                 boyolcum = boy,
                 kiloolcum= kilo, 
                 bedenolcum=beden)
df
```

```
##     isim boyolcum kiloolcum bedenolcum
## 1    Ali      160        55          S
## 2   Elif      165        55          M
## 3     Su      170        57          S
## 4  Deniz      155        50          M
## 5   Aras      167        48          S
## 6   Berk      162        65          L
## 7    Can      169        58          M
## 8    Ece      158        62          L
## 9    Efe      160        45          S
## 10  Arda      164        47          S
```


- Veri seti isimlendirme de diğer bir yol ise `names()` ya da `colnames()` fonksiyonlarıdır.


```r
df <- data.frame(ad,boy,kilo,beden)
names(df) <- c("isim","boyolcum ","kiloolcum","bedenolcum")
df
```

```
##     isim boyolcum  kiloolcum bedenolcum
## 1    Ali       160        55          S
## 2   Elif       165        55          M
## 3     Su       170        57          S
## 4  Deniz       155        50          M
## 5   Aras       167        48          S
## 6   Berk       162        65          L
## 7    Can       169        58          M
## 8    Ece       158        62          L
## 9    Efe       160        45          S
## 10  Arda       164        47          S
```


## Betimsel istatistikler

- Veri setinin tümüne ilişkin betimsel istatistikler


```r
summary(cars)
```

```
##      speed           dist       
##  Min.   : 4.0   Min.   :  2.00  
##  1st Qu.:12.0   1st Qu.: 26.00  
##  Median :15.0   Median : 36.00  
##  Mean   :15.4   Mean   : 42.98  
##  3rd Qu.:19.0   3rd Qu.: 56.00  
##  Max.   :25.0   Max.   :120.00
```


- Veri setinin tek değişkenine ilişkin betimsel istatistikler


```r
summary(cars$speed)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##     4.0    12.0    15.0    15.4    19.0    25.0
```


`attach()` fonksiyonu ile bir veri setinin sütunları sütun isimi ile enviromente eklenir. Aynı işlem `detach()` fonksiyonu ile tersine alınabilir.


```r
summary(women$height)   
attach(women)
summary(height)   # Ayni nesne isimi ile çağırılır.
height <- height*2.54   # Bunu yapmamaya calisin!!
find("height")
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##    58.0    61.5    65.0    65.0    68.5    72.0 
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##    58.0    61.5    65.0    65.0    68.5    72.0 
## [1] ".GlobalEnv" "women"
```



```r
summary(height)         # Yeni değişken
rm(height)
detach("women")
summary(women$height)   # unchanged
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   147.3   156.2   165.1   165.1   174.0   182.9 
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##    58.0    61.5    65.0    65.0    68.5    72.0
```



### Kendinizi Test Edin

**S1.** Sırayla değişken adları TamSayi, OndalikSayi, Karakter, Mantıksal, Faktör olan 5 değişkenli hiçbir gözlemi olmayan bir data.frame oluşturmanızı ve bu data.framenin yapısını yazdırmanızı bekliyorum. Beklenen çıktı aşağıdaki gibi olmalıdır.


```r
[1] "Bos data.framenin yapısı:"
'data.frame':	0 obs. of  5 variables:  
 $ TamSayi    : int   
 $ OndalikSayi: num  
 $ Karakter   : chr  
 $ Mantiksal  : logi  
 $ Faktor     : Factor w/ 0 levels:  
NULL
```



**S2.** Aşağıda size verilen dört vektörden bir veri seti oluşturunuz. Oluşturduğunuz veri setinin deneme sütunundaki eksik veri sayısını hesaplayan komut yazınız.


```r
ad = c('Su','Pera','Sule','Can','Cem','Name','Aras','Mete','Kaan','Pelin')
puan = c(12.5, 9, 16.5, 12, 9, 20, 14.5, 13.5, 8, 19)
deneme = c(1, NA, 2, NA, 2, NA, 1, NA, 2, 1)
bonus = c(1,0,1, 0, 0, 1, 1, 0,0, 1)
```

"Deneme sütunundaki NA sayısı:"
[1] 4



## Odev

Lütfen aşağıdaki bölümleri haftaya kadar okuyunuz.

-   <http://adv-r.had.co.nz/Data-structures.html>

-   <http://adv-r.had.co.nz/Subsetting.html>

- Veri düzenleme konusunda 🔗 [**DataEditR**](https://dillonhammill.github.io/DataEditR/) paketini inceleyiniz. 