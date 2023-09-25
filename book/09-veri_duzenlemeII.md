# Veri duzenleme  - II




- Veriyi üst düzeyde toplama 📊


- **count()** fonksiyonu

- **grup_by()** ve **summarize()**

- **summarize_all()** ve **summarize_if()** ve **summarize_at()**

- **top_n()**


## count() fonksiyonu

- **count()** fonksiyonu frekans tablosu oluşturmak için kullanılabilir.

- **count()** fonksiyonunun pipe ile kullanımıı

```r
veri_seti %>% count(degisken_adı)
```




```r
library(dplyr)
load("import/PISA_OGR_2018.rda") # ogrenci verisi
load("import/PISA_STU_2018.rda") # ogrenci verisi
PISA_STU_2018 %>% count()
```

```
## # A tibble: 1 x 1
##       n
##   <int>
## 1  6890
```

- Cinsiyete göre dağılım
👦 👧

```r
PISA_STU_2018 %>% count(ST004D01T)
```

```
## # A tibble: 2 x 2
##   ST004D01T      n
##   <dbl+lbl>  <int>
## 1 1 [Female]  3396
## 2 2 [Male]    3494
```

- Cinsiyete göre dağılım - **sort** argümanı ile sıralanabilir.
👦 👧


```r
PISA_STU_2018 %>% count(ST004D01T,sort=TRUE)
```

```
## # A tibble: 2 x 2
##   ST004D01T      n
##   <dbl+lbl>  <int>
## 1 2 [Male]    3494
## 2 1 [Female]  3396
```

- PISA_OGR_2018 öğrenci verisindeki değişken adlarının türkçeleştirilmiş halidir.

- Bu veri setini kullanarak öğrencilerin göçmenlik durumları ve cinsiyetlere göre dağılımını inceleyelim.


```r
PISA_OGR_2018 %>% count(CINSIYET,Gocmenlik)
```

```
## # A tibble: 8 x 3
##   CINSIYET  Gocmenlik              n
##   <dbl+lbl> <dbl+lbl>          <int>
## 1 1 [Kiz]    1 [Yerli]          3306
## 2 1 [Kiz]    2 [<dd>kinci Nesil]     17
## 3 1 [Kiz]    3 [Birinci Nesil]    10
## 4 1 [Kiz]   NA                    63
## 5 2 [Erkek]  1 [Yerli]          3357
## 6 2 [Erkek]  2 [<dd>kinci Nesil]     20
## 7 2 [Erkek]  3 [Birinci Nesil]     7
## 8 2 [Erkek] NA                   110
```


- `PISA_OGR_2018 %>% count(CINSIYET,Gocmenlik) %>% ...` birey sayısını büyükten küçüğe sıralayınız. 
___________


```
## # A tibble: 8 x 3
##   CINSIYET  Gocmenlik              n
##   <dbl+lbl> <dbl+lbl>          <int>
## 1 2 [Erkek]  1 [Yerli]          3357
## 2 1 [Kiz]    1 [Yerli]          3306
## 3 2 [Erkek] NA                   110
## 4 1 [Kiz]   NA                    63
## 5 2 [Erkek]  2 [<dd>kinci Nesil]     20
## 6 1 [Kiz]    2 [<dd>kinci Nesil]     17
## 7 1 [Kiz]    3 [Birinci Nesil]    10
## 8 2 [Erkek]  3 [Birinci Nesil]     7
```



```r
PISA_OGR_2018 %>% count(SINIF, sort=TRUE)
```

```
## # A tibble: 6 x 2
##   SINIF             n
##   <dbl+lbl>     <int>
## 1 10 [SINIF 10]  5360
## 2  9 [SINIF 9]   1295
## 3 11 [SINIF 11]   207
## 4  8 [SINIF 8]     19
## 5 12 [SINIF 12]     6
## 6  7 [SINIF 7]      3
```

- `PISA_OGR_2018 %>% count(.....)` siz de  SINIF ve CINSIYET'e göre dağılımı bulunuz? ________________________


```
## # A tibble: 12 x 3
##    CINSIYET  SINIF             n
##    <dbl+lbl> <dbl+lbl>     <int>
##  1 1 [Kiz]   10 [SINIF 10]  2707
##  2 2 [Erkek] 10 [SINIF 10]  2653
##  3 2 [Erkek]  9 [SINIF 9]    747
##  4 1 [Kiz]    9 [SINIF 9]    548
##  5 1 [Kiz]   11 [SINIF 11]   124
##  6 2 [Erkek] 11 [SINIF 11]    83
##  7 1 [Kiz]    8 [SINIF 8]     11
##  8 2 [Erkek]  8 [SINIF 8]      8
##  9 1 [Kiz]   12 [SINIF 12]     5
## 10 2 [Erkek]  7 [SINIF 7]      2
## 11 1 [Kiz]    7 [SINIF 7]      1
## 12 2 [Erkek] 12 [SINIF 12]     1
```

- **count()** fonksiyonunun yardım sayfasını inceleyiniz **wt** argümanını ne amaçala kullanılmıştır açıklayınız. 




## summarize() fonksiyonları

- **summarize()** seçilen sütunlar için her satırı kullanarak istatistikler hesaplar.

- kaç satır olduğu

- ortalamanın ne olduğu

- toplamın ne olduğu

- minumum ve maksimum değerlerin ne olduğu gibi..



- Tek satırlık veri setini özetleyerek yeni bir veri seti oluşturan fonksiyondur.

  - **min(x)** x vektöründeki minumum değer
  - **max(x)** x vektöründeki maksimum değer
  - **mean(x)** x vektöründeki ortalama değer
  - **median(x)** x vektöründeki ortanca değer
  - **quantile(x, p)** x vektöründeki q. yuzdelik
  - **sd(x)** x vektöründeki standart sapma
  - **var(x)** x vektöründeki varyans
  - **diff(range(x))** x vektöründeki değiskenlik
  - **first(x)** x vektöründeki ilk eleman
  - **last(x)** x vektöründeki son eleman
  - **nth(x, n)** x vektöründeki n. eleman
  - **n()** x vektöründeki eleman sayısı
  - **n_distinct(x)** x vektöründeki farklı değerlerin sayısı
  
- PISA veri setindeki başarısı için  hesaplanan 10 olası puan değerinden (plausible value) ilki kullanılmıştır. 


```r
PISA_OGR_2018 %>% 
summarise(mean(ODOKUMA1))
```

```
## # A tibble: 1 x 1
##   `mean(ODOKUMA1)`
##              <dbl>
## 1             464.
```

- **summarise()** fonksiyonu içinde isimlendirme yapmazsanız, oluşan veri setinde isimlendirme fonksiyon adı/ları olacaktır.

- isimlendirilmiş çıktı


```r
PISA_OGR_2018 %>%
  summarise(ortalama=mean(ODOKUMA1))
```

```
## # A tibble: 1 x 1
##   ortalama
##      <dbl>
## 1     464.
```


- Özet bilgiler elde etmek için birden fazla özetleyici fonksiyon kullanabilirsiniz.


```r
PISA_OGR_2018 %>%
  summarise(n = n(),
            ortalama=mean(ODOKUMA1),
            sd=sd(ODOKUMA1),
            min=min(ODOKUMA1),
            max=max(ODOKUMA1))
```

```
## # A tibble: 1 x 5
##       n ortalama    sd   min   max
##   <int>    <dbl> <dbl> <dbl> <dbl>
## 1  6890     464.  87.8  176.  772.
```



- Özet bilgileri veri setinde yer alan alt gruplar için ise ayrı ayrı **group_by()** fonksiyonu ile hesaplayabilirsiniz.

- **group_by()** dan sonra kullanılan fonksiyonlar her grup için hesaplanır. Fonksiyonu içinde sürekli değişken **kullanılmaz.**

- Cinsiyete göre ODOKUMA1 puanlarına ilişkin istatistikler

```r
PISA_OGR_2018 %>%
  group_by(CINSIYET) %>%
  summarise(n = n(),ortalama=mean(ODOKUMA1),sd=sd(ODOKUMA1),min=min(ODOKUMA1),max=max(ODOKUMA1))
```

```
## # A tibble: 2 x 6
##   CINSIYET      n ortalama    sd   min   max
##   <dbl+lbl> <int>    <dbl> <dbl> <dbl> <dbl>
## 1 1 [Kiz]    3396     478.  83.7  236.  772.
## 2 2 [Erkek]  3494     451.  89.6  176.  747.
```


- siz de bu işlemi göçmenlik statüsüne göre  yapınız.


- Özet bilgileri veri setinde yer alan birden fazla kategorik değişken içinde hesaplayabilirsiniz.

- Öğrencilerin cinsiyet ve sınıf düzeylerine göre elde edilen betimsel istatistikleri ortalamaya göre sıralandırılmıştır.


```r
betimsel  <- PISA_OGR_2018 %>%
  group_by(CINSIYET,SINIF) %>%
  summarise(n = n(),ortalama=mean(ODOKUMA1),sd=sd(ODOKUMA1)) %>%  
  arrange(desc(ortalama)) 

betimsel
```

```
## # A tibble: 12 x 5
## # Groups:   CINSIYET [2]
##    CINSIYET  SINIF             n ortalama    sd
##    <dbl+lbl> <dbl+lbl>     <int>    <dbl> <dbl>
##  1 1 [Kiz]   10 [SINIF 10]  2707     482.  79.9
##  2 1 [Kiz]   11 [SINIF 11]   124     473.  85.0
##  3 1 [Kiz]    9 [SINIF 9]    548     462.  96.9
##  4 2 [Erkek] 10 [SINIF 10]  2653     459.  85.0
##  5 2 [Erkek] 11 [SINIF 11]    83     448.  87.9
##  6 2 [Erkek]  9 [SINIF 9]    747     422.  98.7
##  7 1 [Kiz]   12 [SINIF 12]     5     422.  96.6
##  8 2 [Erkek]  8 [SINIF 8]      8     363.  82.8
##  9 1 [Kiz]    8 [SINIF 8]     11     356.  62.5
## 10 1 [Kiz]    7 [SINIF 7]      1     344.  NA  
## 11 2 [Erkek]  7 [SINIF 7]      2     330.  62.1
## 12 2 [Erkek] 12 [SINIF 12]     1     322.  NA
```



- **group_by()** fonksiyonu ile elde ettiğiniz çıktılarda aşağıdaki gibi 
gruplandırılmış veri **Groups**  çıktısı ile alınır.


```r
# A tibble: 12 x 5
# Groups:   CINSIYET [2]
```



- Gruplandırılmış elde edilen veri setlerinde tekrar işlem yapmak istiyorsanız bunu **ungroup()** fonksiyonu ile yapabilirsiniz.


```r
PISA_OGR_2018 %>%
  group_by(CINSIYET,SINIF) %>%
  summarise(n = n(),ortalama=mean(ODOKUMA1),sd=sd(ODOKUMA1)) %>%
  arrange(desc(ortalama)) %>% 
  ungroup()
```

```
## # A tibble: 12 x 5
##    CINSIYET  SINIF             n ortalama    sd
##    <dbl+lbl> <dbl+lbl>     <int>    <dbl> <dbl>
##  1 1 [Kiz]   10 [SINIF 10]  2707     482.  79.9
##  2 1 [Kiz]   11 [SINIF 11]   124     473.  85.0
##  3 1 [Kiz]    9 [SINIF 9]    548     462.  96.9
##  4 2 [Erkek] 10 [SINIF 10]  2653     459.  85.0
##  5 2 [Erkek] 11 [SINIF 11]    83     448.  87.9
##  6 2 [Erkek]  9 [SINIF 9]    747     422.  98.7
##  7 1 [Kiz]   12 [SINIF 12]     5     422.  96.6
##  8 2 [Erkek]  8 [SINIF 8]      8     363.  82.8
##  9 1 [Kiz]    8 [SINIF 8]     11     356.  62.5
## 10 1 [Kiz]    7 [SINIF 7]      1     344.  NA  
## 11 2 [Erkek]  7 [SINIF 7]      2     330.  62.1
## 12 2 [Erkek] 12 [SINIF 12]     1     322.  NA
```


### summarize_at()

- dplyr paket fonksiyonlarının **_at**, **_if**, **_all** uzantılı varyasyonları bulunmaktadır.

- Sadece bir grup sütunun ortalamasını ve standart sapmasını hesaplamanız gerektiğinde **summarize_at()** fonksiyonunu kullanabilirsiniz.


- **summarize_at()** fonksiyonu ile secilecek değişkenler **vars()**
fonksiyonu içinde belirtilebilir. Bu işlem **select** işlemi yerine geçmektedir.

- Hesaplama işlemlerini ise **list()** fonksiyonu içinde tanımlayabilirsiniz.


```r
# adlandırmaya dikkat edin!
PISA_OGR_2018 %>%
    summarize_at(vars(ODOKUMA1, ODFEN1), list(~mean(.), ~sd(.)))
```

```
## # A tibble: 1 x 4
##   ODOKUMA1_mean ODFEN1_mean ODOKUMA1_sd ODFEN1_sd
##           <dbl>       <dbl>       <dbl>     <dbl>
## 1          464.        467.        87.8      83.1
```


### summarize_all() ve summarize_if()

- Elinizde tüm sütunları sayısal (numeric) olan bir veri seti olsun. Tüm sütunların ortalamasını **summarize_all()** fonksiyonu ile hesaplayabilirsiniz.


```r
veriseti %>% summarize_all(funs(mean, sd))
```

- Elinizdeki bir veri setinin sayısal (numeric) olan sütunlarının ortalamasını **summarize_if()** fonksiyonu ile hesaplayabilirsiniz.


```r
PISA_OGR_2018 %>% 
    select(CINSIYET,Gocmenlik,ODOKUMA1) %>% 
    summarize_if(is.numeric, funs(mean, sd))
```

```
## # A tibble: 1 x 6
##   CINSIYET_mean Gocmenlik_mean ODOKUMA1_mean CINSIYET_sd Gocmenlik_sd ODOKUMA1~1
##           <dbl>          <dbl>         <dbl>       <dbl>        <dbl>      <dbl>
## 1          1.51             NA          464.       0.500           NA       87.8
## # ... with abbreviated variable name 1: ODOKUMA1_sd
```


## top_n()

- **top_n()** fonksiyonu ile istediğiniz bir değişkenin **en yüksek** ya da **en düşük** değerlerine  göre verisetinde seçim yapılabilir.


```r
df <- data.frame(x = c(10, 4, 1, 6, 3, 1, 1))
df %>% top_n(2)
```

```
## Selecting by x
```

```
##    x
## 1 10
## 2  6
```



- Okuma puanı **en yüksek** olan üç kız ve üç erkek öğrencinin bilgileri

```r
PISA_OGR_2018 %>%
  select(CINSIYET,ODOKUMA1)%>% 
  arrange(desc(ODOKUMA1))%>% 
  group_by(CINSIYET) %>% 
  top_n(3,ODOKUMA1)
```

```
## # A tibble: 6 x 2
## # Groups:   CINSIYET [2]
##   CINSIYET  ODOKUMA1
##   <dbl+lbl>    <dbl>
## 1 1 [Kiz]       772.
## 2 1 [Kiz]       748.
## 3 2 [Erkek]     747.
## 4 1 [Kiz]       743.
## 5 2 [Erkek]     737.
## 6 2 [Erkek]     714.
```


## top_n() & - operatoru

- Okuma puanı **en düşük** olan üç kız ve beş erkek öğrencinin bilgileri


```r
PISA_OGR_2018 %>%
  select(CINSIYET,ODOKUMA1)%>% 
  arrange(desc(ODOKUMA1))%>% 
  group_by(CINSIYET) %>% 
  top_n(-3,ODOKUMA1)
```

```
## # A tibble: 6 x 2
## # Groups:   CINSIYET [2]
##   CINSIYET  ODOKUMA1
##   <dbl+lbl>    <dbl>
## 1 1 [Kiz]       250.
## 2 1 [Kiz]       242.
## 3 1 [Kiz]       236.
## 4 2 [Erkek]     199.
## 5 2 [Erkek]     177.
## 6 2 [Erkek]     176.
```



## DataEditR paketi

Bu paketi paketin [github sayfasından](https://github.com/DillonHammill/DataEditR) inceleyelim.



teşekkürler !




🍵

