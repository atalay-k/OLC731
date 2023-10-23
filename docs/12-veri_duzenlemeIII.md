# Veri duzenleme  - III




- Seçme ve Dönüştürme 📊

- **select()** fonksiyonu
- **select()** fonksiyonu içinde çalışan fonksiyonlar
- **rename()** fonksiyonu
- **mutate()** ve **transmute()** fonksiyonları

## select() fonksiyonu

- **select()** fonksiyonu ile sütun bazında seçim yapılabilir.

- Veri yapısının incelenmesi.


```r
library(dplyr)
load("import/PISA_OGR_2018.rda") # ogrenci verisi
dim(PISA_OGR_2018)
```

```
## [1] 6890  673
```

- 673 sütunla çalışmayacaksanız, problem durumunuza uygun sütunları seçebilirsiniz. Fonksiyon içinde degişkenler tek tek virgül `,` ile ayrılarak seçim yapılabilir.


```r
select(veri seti, degisken adi, degisken adi,..)
veri seti %>% select(degisken adi, degisken adi,..)
```


- OKULID, OGRENCIID, CINSIYET ,SES değişkenlerinin seçimi


```r
select(PISA_OGR_2018, OKULID, OGRENCIID, CINSIYET ,SES) %>% head(6)
```

```
## # A tibble: 6 x 4
##     OKULID OGRENCIID   CINSIYET     SES
##      <dbl>     <dbl> <hvn_lbll>   <dbl>
## 1 79200001  79200768          2 -2.45  
## 2 79200001  79201064          2 -2.10  
## 3 79200001  79201118          1 -2.27  
## 4 79200001  79201275          2  0.0324
## 5 79200001  79201481          2 -0.0674
## 6 79200001  79201556          2  0.398
```

Aynı işlem `c()` fonksiyonu içinde de yapılabilir.


```r
select(PISA_OGR_2018, c(OKULID, OGRENCIID, CINSIYET ,SES))
```

- **select()** fonksiyonu ile sütun bazında seçim yapılabilir.


```r
PISA_OGR_2018 %>% select(OKULID, OGRENCIID, CINSIYET ,SES) %>% head(6)
```

```
## # A tibble: 6 x 4
##     OKULID OGRENCIID   CINSIYET     SES
##      <dbl>     <dbl> <hvn_lbll>   <dbl>
## 1 79200001  79200768          2 -2.45  
## 2 79200001  79201064          2 -2.10  
## 3 79200001  79201118          1 -2.27  
## 4 79200001  79201275          2  0.0324
## 5 79200001  79201481          2 -0.0674
## 6 79200001  79201556          2  0.398
```


- **select()** fonksiyonu belirli bir aralıktaki değişkenler iki nokta `:` opertorü ile seçilebilir.

- örneğin okumadan alınan zevke ilişkin maddeler aşağıdaki şekilde seçilebilir.


```r
PISA_OGR_2018 %>% select(ST097Q01TA:ST097Q05TA) %>% head(6)
```

```
## # A tibble: 6 x 5
##   ST097Q01TA ST097Q02TA ST097Q03TA ST097Q04TA ST097Q05TA
##   <hvn_lbll> <hvn_lbll> <hvn_lbll> <hvn_lbll> <hvn_lbll>
## 1          1          2          1          1          1
## 2          3          2          3          3          3
## 3          2          3          3          3          3
## 4          2          2          3          1          1
## 5          3          3          4          3          1
## 6          3          3          2          2          3
```


- **select()**  fonksiyonu belirli bir aralıkta yer alan değişkenler iki nokta **:** opertorü ile seçilirken, bu aralıkta dahil edilmek istenmeyen degişkenler kısa çizgi **-** operatorü ile hariç tutulabilir.


```r
PISA_OGR_2018 <- expss::drop_var_labs(PISA_OGR_2018)
PISA_OGR_2018 %>% select(OKULID:SINIF,-KITAPCIK) %>% head(6)
```

```
## # A tibble: 6 x 4
##     OKULID OGRENCIID OKUL_TUR SINIF
##      <dbl>     <dbl> <chr>    <dbl>
## 1 79200001  79200768 TUR0112     10
## 2 79200001  79201064 TUR0112     10
## 3 79200001  79201118 TUR0112     10
## 4 79200001  79201275 TUR0112      9
## 5 79200001  79201481 TUR0112      9
## 6 79200001  79201556 TUR0112     10
```


### **starts_with()**

- Sadece **select()** fonksiyonu içinde çalışan birtakım fonksiyonlar değişken seçim işini kolaylaştırır.

- **ST097** ile başlayan degişkenlerin seçilmesi


```r
select(PISA_OGR_2018, starts_with("ST097")) %>% head(6)
```

```
## # A tibble: 6 x 5
##   ST097Q01TA ST097Q02TA ST097Q03TA ST097Q04TA ST097Q05TA
##        <dbl>      <dbl>      <dbl>      <dbl>      <dbl>
## 1          1          2          1          1          1
## 2          3          2          3          3          3
## 3          2          3          3          3          3
## 4          2          2          3          1          1
## 5          3          3          4          3          1
## 6          3          3          2          2          3
```


### **ends_with()**

- **NA** ile **biten** degişkenlerin seçilmesi


```r
select(PISA_OGR_2018, ends_with("NA")) %>% head(6)
```

```
## # A tibble: 6 x 48
##   ST104Q02NA ST104Q03NA ST104Q04NA ST016Q01NA ST123Q02NA ST123Q03NA ST123Q04NA
##        <dbl>      <dbl>      <dbl>      <dbl>      <dbl>      <dbl>      <dbl>
## 1          2          2          2         NA          4          4          4
## 2          2          2          3          7          4          3          1
## 3          2          2          2          4          3          3          3
## 4          3          2          3          3          3         NA          3
## 5          3          2          4          1          1          1          1
## 6          3          2          3          4          3          3          3
## # i 41 more variables: ST060Q01NA <dbl>, ST061Q01NA <dbl>, ST038Q03NA <dbl>,
## #   ST038Q04NA <dbl>, ST038Q05NA <dbl>, ST038Q06NA <dbl>, ST038Q07NA <dbl>,
## #   ST038Q08NA <dbl>, IC009Q05NA <dbl>, IC009Q06NA <dbl>, IC009Q07NA <dbl>,
## #   IC009Q10NA <dbl>, IC009Q11NA <dbl>, IC008Q07NA <dbl>, IC008Q13NA <dbl>,
## #   IC010Q02NA <dbl>, IC010Q05NA <dbl>, IC010Q06NA <dbl>, IC010Q09NA <dbl>,
## #   IC010Q10NA <dbl>, IC013Q01NA <dbl>, IC013Q04NA <dbl>, IC013Q05NA <dbl>,
## #   IC013Q11NA <dbl>, IC013Q12NA <dbl>, IC013Q13NA <dbl>, IC014Q03NA <dbl>, ...
```


### **contains()**

- **OKUMA** geçen değişkenlerin seçilmesi


```r
select(PISA_OGR_2018,contains("OKUMA")) %>% head(6)
```

```
## # A tibble: 6 x 12
##   OKUMA_BAGLILIGI OKUMA_ZEVK ODOKUMA1 ODOKUMA2 ODOKUMA3 ODOKUMA4 ODOKUMA5
##             <dbl>      <dbl>    <dbl>    <dbl>    <dbl>    <dbl>    <dbl>
## 1          -0.922     -0.289     376.     418.     421.     414.     434.
## 2           1.07       0.604     512.     473.     564.     485.     500.
## 3          -0.62       0.638     396.     414.     423.     452.     392.
## 4          -0.62      -1.15      393.     429.     365.     383.     379.
## 5           0.378      0.667     552.     570.     563.     531.     532.
## 6          -0.62       0.357     441.     416.     407.     437.     473.
## # i 5 more variables: ODOKUMA6 <dbl>, ODOKUMA7 <dbl>, ODOKUMA8 <dbl>,
## #   ODOKUMA9 <dbl>, ODOKUMA10 <dbl>
```


###  **matches()**

- içinde **02** geçen değişkenlerin seçilmesi


```r
select(PISA_OGR_2018,matches("02")) %>% head(6)
```

```
## # A tibble: 6 x 59
##   ST097Q02TA ST100Q02TA ST102Q01TA ST102Q02TA ST102Q03TA ST102Q04TA ST211Q02HA
##        <dbl>      <dbl>      <dbl>      <dbl>      <dbl>      <dbl>      <dbl>
## 1          2          2          2          2          3          2          3
## 2          2          3          2          3          2          2          2
## 3          3          2          2          2          3          3          2
## 4          2          2          2          3          4          3          2
## 5          3          3          3          1          2          2          2
## 6          3          3          3          3          3          3          3
## # i 52 more variables: ST212Q02HA <dbl>, ST104Q02NA <dbl>, ST213Q02HA <dbl>,
## #   ST150Q02IA <dbl>, ST153Q02HA <dbl>, ST158Q02HA <dbl>, ST160Q02IA <dbl>,
## #   ST167Q02IA <dbl>, ST176Q02IA <dbl>, ST161Q02HA <dbl>, ST163Q02HA <dbl>,
## #   ST164Q02IA <dbl>, ST165Q02IA <dbl>, ST166Q02HA <dbl>, ST225Q02HA <dbl>,
## #   ST181Q02HA <dbl>, ST183Q02HA <dbl>, ST185Q02HA <dbl>, ST186Q02HA <dbl>,
## #   ST208Q02HA <dbl>, ST188Q02HA <dbl>, ST034Q02TA <dbl>, ST196Q02HA <dbl>,
## #   ST197Q02HA <dbl>, ST215Q02HA <dbl>, ST216Q02HA <dbl>, ST218Q02HA <dbl>, ...
```


### **num_range()**

-  ardışık ilerleyen değişkenlerin seçilmesi


```r
select(PISA_OGR_2018,num_range("AGIRLIKLANDIRMA",1:5)) %>% head(6)
```

```
## # A tibble: 6 x 5
##   AGIRLIKLANDIRMA1 AGIRLIKLANDIRMA2 AGIRLIKLANDIRMA3 AGIRLIKLANDIRMA4
##              <dbl>            <dbl>            <dbl>            <dbl>
## 1             71.0             213.             71.0             213.
## 2             71.0             213.             71.0             213.
## 3             71.0             213.             71.0             213.
## 4             71.0             213.             71.0             213.
## 5             71.0             213.             71.0             213.
## 6             71.0             213.             71.0             213.
## # i 1 more variable: AGIRLIKLANDIRMA5 <dbl>
```


###  Matıksal operatorler ile seçim

- farklı fonksiyonları aynı anda mantıksal operatörlerle kullanarak da seçim yapabilirsiniz.

- veya **|** operatorünün kullanılması


```r
select(PISA_OGR_2018,contains("OKUMA") | matches("2")) %>% head(6)
```

```
## # A tibble: 6 x 198
##   OKUMA_BAGLILIGI OKUMA_ZEVK ODOKUMA1 ODOKUMA2 ODOKUMA3 ODOKUMA4 ODOKUMA5
##             <dbl>      <dbl>    <dbl>    <dbl>    <dbl>    <dbl>    <dbl>
## 1          -0.922     -0.289     376.     418.     421.     414.     434.
## 2           1.07       0.604     512.     473.     564.     485.     500.
## 3          -0.62       0.638     396.     414.     423.     452.     392.
## 4          -0.62      -1.15      393.     429.     365.     383.     379.
## 5           0.378      0.667     552.     570.     563.     531.     532.
## 6          -0.62       0.357     441.     416.     407.     437.     473.
## # i 191 more variables: ODOKUMA6 <dbl>, ODOKUMA7 <dbl>, ODOKUMA8 <dbl>,
## #   ODOKUMA9 <dbl>, ODOKUMA10 <dbl>, ST097Q02TA <dbl>, ST100Q02TA <dbl>,
## #   ST102Q01TA <dbl>, ST102Q02TA <dbl>, ST102Q03TA <dbl>, ST102Q04TA <dbl>,
## #   ST211Q01HA <dbl>, ST211Q02HA <dbl>, ST211Q03HA <dbl>, ST212Q01HA <dbl>,
## #   ST212Q02HA <dbl>, ST212Q03HA <dbl>, ST104Q02NA <dbl>, ST213Q01HA <dbl>,
## #   ST213Q02HA <dbl>, ST213Q03HA <dbl>, ST213Q04HA <dbl>, ST150Q02IA <dbl>,
## #   ST152Q05IA <dbl>, ST152Q06IA <dbl>, ST152Q07IA <dbl>, ST152Q08IA <dbl>, ...
```


- ve **&** operatorunun kullanılması


```r
select(PISA_OGR_2018,contains("OKUMA") & matches("2")) %>% head(6)
```

```
## # A tibble: 6 x 1
##   ODOKUMA2
##      <dbl>
## 1     418.
## 2     473.
## 3     414.
## 4     429.
## 5     570.
## 6     416.
```



- hariç tutmak amacıyla **-** operatorü kullanılabilir.


```r
select(PISA_OGR_2018,-contains("OKUMA"),-matches("02"))  %>% head(5)
```

```
## # A tibble: 5 x 602
##     OKULID OGRENCIID OKUL_TUR KITAPCIK SINIF DOGUMAY CINSIYET ANNE_OKUL
##      <dbl>     <dbl> <chr>       <dbl> <dbl>   <dbl>    <dbl>     <dbl>
## 1 79200001  79200768 TUR0112        20    10      10        2         3
## 2 79200001  79201064 TUR0112         5    10       2        2         3
## 3 79200001  79201118 TUR0112        16    10       1        1         4
## 4 79200001  79201275 TUR0112        21     9       9        2         1
## 5 79200001  79201481 TUR0112         1     9       9        2         1
## # i 594 more variables: ANNE_LISANSUSTU <dbl>, ANNE_LISANS <dbl>,
## #   ANNE_ONLISANS <dbl>, BABA_OKUL <dbl>, BABA_LISANSUSTU <dbl>,
## #   BABA_LISANS <dbl>, BABA_ONLISANS <dbl>, OLANAK_MASA <dbl>,
## #   OLANAK_ODA <dbl>, OLANAK_SESSIZYER <dbl>, OLANAK_BILGISAYAR <dbl>,
## #   OLANAK_YAZILIM <dbl>, OLANAK_INTERNET <dbl>, OLANAK_KLASIKKITAP <dbl>,
## #   OLANAK_SIIRKITAP <dbl>, OLANAK_SANATESER <dbl>, OLANAK_KAYNAKKITAP <dbl>,
## #   OLANAK_TEKNIKKITAP <dbl>, OLANAK_SOZLUK <dbl>, OLANAK_SANATKITAP <dbl>, ...
```


### **rename()** fonksiyonu

- **select()** fonksiyonu icinde değişken seçimi sırasında değişken adı değişimi yapılabilir.

- Örnekte **ODOKUMA1** degişkeninin adını **okumapuan** olarak değiştirip seçebilirsiniz.


```r
PISA_OGR_2018 %>%
select(OGRENCIID,OKUL_TUR,CINSIYET,SES,okumapuan = ODOKUMA1) %>%
head(2)
```

```
## # A tibble: 2 x 5
##   OGRENCIID OKUL_TUR CINSIYET   SES okumapuan
##       <dbl> <chr>       <dbl> <dbl>     <dbl>
## 1  79200768 TUR0112         2 -2.45      376.
## 2  79201064 TUR0112         2 -2.10      512.
```


- Örnekte ise **ODOKUMA1** degişkeninin adı okumapuan olarak **rename()** fonksiyonu ile de değiştirilebilir.


```r
PISA_OGR_2018 %>%
select(OGRENCIID,OKUL_TUR,CINSIYET,SES,ODOKUMA1) %>%
rename(okumapuan=ODOKUMA1)%>%
head(2)
```

```
## # A tibble: 2 x 5
##   OGRENCIID OKUL_TUR CINSIYET   SES okumapuan
##       <dbl> <chr>       <dbl> <dbl>     <dbl>
## 1  79200768 TUR0112         2 -2.45      376.
## 2  79201064 TUR0112         2 -2.10      512.
```


### mutate fonksiyonu

- **mutate()** fonksiyonu ile veri setine yeni değişken ekleyebilirsiniz.

- **transmute()** fonksiyonu ile veri setine yeni değişken eklenirken, eski değişken/ler veri setiden çıkarılır.

- Okumadan zevk alma maddelerinden bir veri seti oluşturup, bu veri setine toplam puan ekleme


```r
zevk  <- select(PISA_OGR_2018, starts_with("ST097"))
zevk  <- expss::drop_var_labs(zevk)
zevk %>%
mutate(toplam =ST097Q01TA+ST097Q02TA+ST097Q03TA+ST097Q04TA+ ST097Q05TA) %>% head(2)
```

```
## # A tibble: 2 x 6
##   ST097Q01TA ST097Q02TA ST097Q03TA ST097Q04TA ST097Q05TA toplam
##        <dbl>      <dbl>      <dbl>      <dbl>      <dbl>  <dbl>
## 1          1          2          1          1          1      6
## 2          3          2          3          3          3     14
```



- Değişken değerleri bir önceki örnekteki gibi tek tek **+** ile toplanacağı gibi **rowSums()** fonksiyonu ile de aşağıdaki gibi toplanabilir

```r
zevk %>%
mutate(toplam=rowSums(select(., ST097Q01TA:ST097Q05TA))) %>%
head(2)
```

```
## # A tibble: 2 x 6
##   ST097Q01TA ST097Q02TA ST097Q03TA ST097Q04TA ST097Q05TA toplam
##        <dbl>      <dbl>      <dbl>      <dbl>      <dbl>  <dbl>
## 1          1          2          1          1          1      6
## 2          3          2          3          3          3     14
```



- Yeni eklenecek yeri `.before` ya da `.after` argumanları ile düzenleyebilirsiniz.


```r
zevk %>%
mutate(toplam=rowSums(select(., ST097Q01TA:ST097Q05TA)),.before= ST097Q01TA)%>% head(2)
```

```
## # A tibble: 2 x 6
##   toplam ST097Q01TA ST097Q02TA ST097Q03TA ST097Q04TA ST097Q05TA
##    <dbl>      <dbl>      <dbl>      <dbl>      <dbl>      <dbl>
## 1      6          1          2          1          1          1
## 2     14          3          2          3          3          3
```


### transmute() fonksiyonu

- **transmute()** fonksiyonu kullanılarak yeni değişken oluşturulduğunda, işlemde kullanılan değişkenler veri setinden çıkarılır.


```r
zevk %>%
transmute(toplam=rowSums(select(., ST097Q01TA:ST097Q05TA))) %>%
head(2)
```

```
## # A tibble: 2 x 1
##   toplam
##    <dbl>
## 1      6
## 2     14
```



- Fonksiyonda üretilen ilk değişken kullanılarak da yeni değişken üretilebilir.

- Ilk olarak özyeterliği ölçen maddelerden yeni bir veri oluşturulmuş, daha sonra bu puanların önce toplam puanları daha sonra toplam puanların kareleri alınmıştır.


```r
ozyeterlik <- PISA_OGR_2018 %>%
  expss::drop_var_labs() %>%
  select(ST196Q02HA:ST196Q07HA)

ozyeterlik%>%
  rowwise() %>%
  mutate(toplam = sum(across()))%>%
  mutate(toplam_kare=toplam*toplam) %>% head(2)
```

### ifelse()

- **ifelse()** programlama dillerinde sıklıkla kullanılan koşullu önermelerden biridir.


```r
ifelse(test = x<0, evet = ilkdeger , hayır = ikincideger)
```


```r
x <- c(-2,1,-1,-3,3)
ifelse(x<0,"Negatif", "Pozitif")
```

```
## [1] "Negatif" "Pozitif" "Negatif" "Negatif" "Pozitif"
```



- Uygulama 7.,8.,9.,10.,11. ve 12. sınıf öğrencileri katılmaktadır.


```r
table(PISA_OGR_2018$SINIF)
```

```
## 
##    7    8    9   10   11   12 
##    3   19 1295 5360  207    6
```

- **SINIF** değişkenini kullanarak ortaokul ve lise olmak üzere iki düzeyli **OKUL** adlı bir değişken oluşturalım.




```r
PISA_OGR_2018 %>%
  select(1:5) %>%
  mutate(okul = ifelse(SINIF == 7 | SINIF == 8,
                       "Ortaokul", "Lise")) %>%
    head(3)
```

```
## # A tibble: 3 x 6
##     OKULID OGRENCIID OKUL_TUR KITAPCIK SINIF okul 
##      <dbl>     <dbl> <chr>       <dbl> <dbl> <chr>
## 1 79200001  79200768 TUR0112        20    10 Lise 
## 2 79200001  79201064 TUR0112         5    10 Lise 
## 3 79200001  79201118 TUR0112        16    10 Lise
```


## case_when()

- **case_when()** fonksiyonu çoklu **ifelse() ** kullanımı ile benzer işlevi sağlar.

- **case_when()** birden fazla koşula dayalı karşılaştırmalarda yeni bir değişken oluşturmak amacıyla kullanılır.

- Sosyoekomik düzeye ilişikin betimsel istatistikler

```r
summary(PISA_OGR_2018$SES)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max.    NA's 
## -4.7546 -2.0633 -1.3002 -1.1712 -0.3228  2.7617      35
```


- SES değişkeninin kategorik hale getirilmesi


```r
v1 <- PISA_OGR_2018 %>%
  mutate(SES_kategorik =
    case_when(
      SES <=  -2 ~ "dusuk",
      SES > -2 & SES <  0 ~ "orta",
      SES >=0 ~ "yuksek" )) %>%
      select(SES,SES_kategorik)
```


- Olusturulan yeni SES_kategorik degişkeninin veri setinde nasıl dağıldığını inceleme



```r
v1 %>% group_by(SES_kategorik) %>% summarize(f=n())
```

```
## # A tibble: 4 x 2
##   SES_kategorik     f
##   <chr>         <int>
## 1 dusuk          1856
## 2 orta           3676
## 3 yuksek         1323
## 4 <NA>             35
```


teşekkürler !


- [Siz de yapın](https://learnr-examples.shinyapps.io/ex-data-filter/#section-welcome>)

- [Siz de yapın](https://learnr-examples.shinyapps.io/ex-data-summarise/)
--


