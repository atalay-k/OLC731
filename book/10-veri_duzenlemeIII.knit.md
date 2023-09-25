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
##     OKULID OGRENCIID CINSIYET      SES
##      <dbl>     <dbl> <dbl+lbl>   <dbl>
## 1 79200001  79200768 2 [Erkek] -2.45  
## 2 79200001  79201064 2 [Erkek] -2.10  
## 3 79200001  79201118 1 [Kiz]   -2.27  
## 4 79200001  79201275 2 [Erkek]  0.0324
## 5 79200001  79201481 2 [Erkek] -0.0674
## 6 79200001  79201556 2 [Erkek]  0.398
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
##     OKULID OGRENCIID CINSIYET      SES
##      <dbl>     <dbl> <dbl+lbl>   <dbl>
## 1 79200001  79200768 2 [Erkek] -2.45  
## 2 79200001  79201064 2 [Erkek] -2.10  
## 3 79200001  79201118 1 [Kiz]   -2.27  
## 4 79200001  79201275 2 [Erkek]  0.0324
## 5 79200001  79201481 2 [Erkek] -0.0674
## 6 79200001  79201556 2 [Erkek]  0.398
```


- **select()** fonksiyonu belirli bir aralıktaki değişkenler iki nokta `:` opertorü ile seçilebilir.

- örneğin okumadan alınan zevke ilişkin maddeler aşağıdaki şekilde seçilebilir.


```r
PISA_OGR_2018 %>% select(ST097Q01TA:ST097Q05TA) %>% head(6)
```

```
## # A tibble: 6 x 5
##   ST097Q01TA               ST097Q02TA               ST097Q03TA   ST097~1 ST097~2
##   <dbl+lbl>                <dbl+lbl>                <dbl+lbl>    <dbl+l> <dbl+l>
## 1 1 [Her ders]             2 [Derslerin cogunda]    1 [Her ders] 1 [Her~ 1 [Her~
## 2 3 [cogunlukla test dili] 2 [Derslerin cogunda]    3 [cogunluk~ 3 [cog~ 3 [cog~
## 3 2 [Derslerin cogunda]    3 [cogunlukla test dili] 3 [cogunluk~ 3 [cog~ 3 [cog~
## 4 2 [Derslerin cogunda]    2 [Derslerin cogunda]    3 [cogunluk~ 1 [Her~ 1 [Her~
## 5 3 [cogunlukla test dili] 3 [cogunlukla test dili] 4 [Bazi der~ 3 [cog~ 1 [Her~
## 6 3 [cogunlukla test dili] 3 [cogunlukla test dili] 2 [Dersleri~ 2 [Der~ 3 [cog~
## # ... with abbreviated variable names 1: ST097Q04TA, 2: ST097Q05TA
```


- **select()**  fonksiyonu belirli bir aralıkta yer alan değişkenler iki nokta **:** opertorü ile seçilirken, bu aralıkta dahil edilmek istenmeyen degişkenler kısa çizgi **-** operatorü ile hariç tutulabilir.


```r
PISA_OGR_2018 %>% select(OKULID:SINIF,-KITAPCIK) %>% head(6)
```

```
## # A tibble: 6 x 4
##     OKULID OGRENCIID OKUL_TUR                     SINIF        
##      <dbl>     <dbl> <chr+lbl>                    <dbl+lbl>    
## 1 79200001  79200768 TUR0112 [Anadolu Lisesi - E] 10 [SINIF 10]
## 2 79200001  79201064 TUR0112 [Anadolu Lisesi - E] 10 [SINIF 10]
## 3 79200001  79201118 TUR0112 [Anadolu Lisesi - E] 10 [SINIF 10]
## 4 79200001  79201275 TUR0112 [Anadolu Lisesi - E]  9 [SINIF 9] 
## 5 79200001  79201481 TUR0112 [Anadolu Lisesi - E]  9 [SINIF 9] 
## 6 79200001  79201556 TUR0112 [Anadolu Lisesi - E] 10 [SINIF 10]
```


### **starts_with()**

- Sadece **select()** fonksiyonu içinde çalışan birtakım fonksiyonlar değişken seçim işini kolaylaştırır.

- **ST097** ile başlayan degişkenlerin seçilmesi


```r
select(PISA_OGR_2018, starts_with("ST097")) %>% head(6)
```

```
## # A tibble: 6 x 5
##   ST097Q01TA               ST097Q02TA               ST097Q03TA   ST097~1 ST097~2
##   <dbl+lbl>                <dbl+lbl>                <dbl+lbl>    <dbl+l> <dbl+l>
## 1 1 [Her ders]             2 [Derslerin cogunda]    1 [Her ders] 1 [Her~ 1 [Her~
## 2 3 [cogunlukla test dili] 2 [Derslerin cogunda]    3 [cogunluk~ 3 [cog~ 3 [cog~
## 3 2 [Derslerin cogunda]    3 [cogunlukla test dili] 3 [cogunluk~ 3 [cog~ 3 [cog~
## 4 2 [Derslerin cogunda]    2 [Derslerin cogunda]    3 [cogunluk~ 1 [Her~ 1 [Her~
## 5 3 [cogunlukla test dili] 3 [cogunlukla test dili] 4 [Bazi der~ 3 [cog~ 1 [Her~
## 6 3 [cogunlukla test dili] 3 [cogunlukla test dili] 2 [Dersleri~ 2 [Der~ 3 [cog~
## # ... with abbreviated variable names 1: ST097Q04TA, 2: ST097Q05TA
```


### **ends_with()**

- **NA** ile **biten** degişkenlerin seçilmesi


```r
select(PISA_OGR_2018, ends_with("NA")) %>% head(6)
```

```
## # A tibble: 6 x 48
##   ST104Q02NA    ST104~1 ST104~2 ST016~3 ST123~4 ST123Q~5 ST123~6 ST060~7 ST061~8
##   <dbl+lbl>     <dbl+l> <dbl+l>   <dbl> <dbl+l> <dbl+lb> <dbl+l>   <dbl>   <dbl>
## 1 2 [Bazi ders~ 2 [Baz~ 2 [Baz~      NA 4 [Kes~  4 [Kes~ 4 [Kes~      NA      NA
## 2 2 [Bazi ders~ 2 [Baz~ 3 [Der~       7 4 [Kes~  3 [Kat~ 1 [Kes~      60      35
## 3 2 [Bazi ders~ 2 [Baz~ 2 [Baz~       4 3 [Kat~  3 [Kat~ 3 [Kat~      41      70
## 4 3 [Derslerin~ 2 [Baz~ 3 [Der~       3 3 [Kat~ NA       3 [Kat~      40      40
## 5 3 [Derslerin~ 2 [Baz~ 4 [Her~       1 1 [Kes~  1 [Kes~ 1 [Kes~      44      40
## 6 3 [Derslerin~ 2 [Baz~ 3 [Der~       4 3 [Kat~  3 [Kat~ 3 [Kat~      30      20
## # ... with 39 more variables: ST038Q03NA <dbl+lbl>, ST038Q04NA <dbl+lbl>,
## #   ST038Q05NA <dbl+lbl>, ST038Q06NA <dbl+lbl>, ST038Q07NA <dbl+lbl>,
## #   ST038Q08NA <dbl+lbl>, IC009Q05NA <dbl+lbl>, IC009Q06NA <dbl+lbl>,
## #   IC009Q07NA <dbl+lbl>, IC009Q10NA <dbl+lbl>, IC009Q11NA <dbl+lbl>,
## #   IC008Q07NA <dbl+lbl>, IC008Q13NA <dbl+lbl>, IC010Q02NA <dbl+lbl>,
## #   IC010Q05NA <dbl+lbl>, IC010Q06NA <dbl+lbl>, IC010Q09NA <dbl+lbl>,
## #   IC010Q10NA <dbl+lbl>, IC013Q01NA <dbl+lbl>, IC013Q04NA <dbl+lbl>, ...
```


### **contains()**

- **OKUMA** geçen değişkenlerin seçilmesi


```r
select(PISA_OGR_2018,contains("OKUMA")) %>% head(6)
```

```
## # A tibble: 6 x 12
##   OKUMA_BAGLIL~1 OKUMA~2 ODOKU~3 ODOKU~4 ODOKU~5 ODOKU~6 ODOKU~7 ODOKU~8 ODOKU~9
##            <dbl>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>
## 1         -0.922  -0.289    376.    418.    421.    414.    434.    424.    470.
## 2          1.07    0.604    512.    473.    564.    485.    500.    495.    477.
## 3         -0.62    0.638    396.    414.    423.    452.    392.    433.    387.
## 4         -0.62   -1.15     393.    429.    365.    383.    379.    416.    396.
## 5          0.378   0.667    552.    570.    563.    531.    532.    522.    482.
## 6         -0.62    0.357    441.    416.    407.    437.    473.    416.    428.
## # ... with 3 more variables: ODOKUMA8 <dbl>, ODOKUMA9 <dbl>, ODOKUMA10 <dbl>,
## #   and abbreviated variable names 1: OKUMA_BAGLILIGI, 2: OKUMA_ZEVK,
## #   3: ODOKUMA1, 4: ODOKUMA2, 5: ODOKUMA3, 6: ODOKUMA4, 7: ODOKUMA5,
## #   8: ODOKUMA6, 9: ODOKUMA7
```


###  **matches()**

- içinde **02** geçen değişkenlerin seçilmesi


```r
select(PISA_OGR_2018,matches("02")) %>% head(6)
```

```
## # A tibble: 6 x 59
##   ST097Q02TA     ST100~1 ST102~2 ST102~3 ST102~4 ST102~5 ST211~6 ST212~7 ST104~8
##   <dbl+lbl>      <dbl+l> <dbl+l> <dbl+l> <dbl+l> <dbl+l> <dbl+l> <dbl+l> <dbl+l>
## 1 2 [Derslerin ~ 2 [Der~ 2 [Der~ 2 [Der~ 3 [cog~ 2 [Der~ 3 [Kat~ 2 [Baz~ 2 [Baz~
## 2 2 [Derslerin ~ 3 [cog~ 2 [Der~ 3 [cog~ 2 [Der~ 2 [Der~ 2 [Kat~ 2 [Baz~ 2 [Baz~
## 3 3 [cogunlukla~ 2 [Der~ 2 [Der~ 2 [Der~ 3 [cog~ 3 [cog~ 2 [Kat~ 2 [Baz~ 2 [Baz~
## 4 2 [Derslerin ~ 2 [Der~ 2 [Der~ 3 [cog~ 4 [Baz~ 3 [cog~ 2 [Kat~ 2 [Baz~ 3 [Der~
## 5 3 [cogunlukla~ 3 [cog~ 3 [cog~ 1 [Her~ 2 [Der~ 2 [Der~ 2 [Kat~ 1 [Hic~ 3 [Der~
## 6 3 [cogunlukla~ 3 [cog~ 3 [cog~ 3 [cog~ 3 [cog~ 3 [cog~ 3 [Kat~ 2 [Baz~ 3 [Der~
## # ... with 50 more variables: ST213Q02HA <dbl+lbl>, ST150Q02IA <dbl+lbl>,
## #   ST153Q02HA <dbl+lbl>, ST158Q02HA <dbl+lbl>, ST160Q02IA <dbl+lbl>,
## #   ST167Q02IA <dbl+lbl>, ST176Q02IA <dbl+lbl>, ST161Q02HA <dbl+lbl>,
## #   ST163Q02HA <dbl+lbl>, ST164Q02IA <dbl+lbl>, ST165Q02IA <dbl+lbl>,
## #   ST166Q02HA <dbl+lbl>, ST225Q02HA <dbl+lbl>, ST181Q02HA <dbl+lbl>,
## #   ST183Q02HA <dbl+lbl>, ST185Q02HA <dbl+lbl>, ST186Q02HA <dbl+lbl>,
## #   ST208Q02HA <dbl+lbl>, ST188Q02HA <dbl+lbl>, ST034Q02TA <dbl+lbl>, ...
```


### **num_range()**

-  ardışık ilerleyen değişkenlerin seçilmesi


```r
select(PISA_OGR_2018,num_range("AGIRLIKLANDIRMA",1:5)) %>% head(6)
```

```
## # A tibble: 6 x 5
##   AGIRLIKLANDIRMA1 AGIRLIKLANDIRMA2 AGIRLIKLANDIRMA3 AGIRLIKLANDIRMA4 AGIRLIKL~1
##              <dbl>            <dbl>            <dbl>            <dbl>      <dbl>
## 1             71.0             213.             71.0             213.       71.0
## 2             71.0             213.             71.0             213.       71.0
## 3             71.0             213.             71.0             213.       71.0
## 4             71.0             213.             71.0             213.       71.0
## 5             71.0             213.             71.0             213.       71.0
## 6             71.0             213.             71.0             213.       71.0
## # ... with abbreviated variable name 1: AGIRLIKLANDIRMA5
```


###  Matıksal operatorler ile seçim

- farklı fonksiyonları aynı anda mantıksal operatörlerle kullanarak da seçim yapabilirsiniz.

- veya **|** operatorünün kullanılması


```r
select(PISA_OGR_2018,contains("OKUMA") | matches("2")) %>% head(6)
```

```
## # A tibble: 6 x 198
##   OKUMA_BAGLIL~1 OKUMA~2 ODOKU~3 ODOKU~4 ODOKU~5 ODOKU~6 ODOKU~7 ODOKU~8 ODOKU~9
##            <dbl>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>   <dbl>
## 1         -0.922  -0.289    376.    418.    421.    414.    434.    424.    470.
## 2          1.07    0.604    512.    473.    564.    485.    500.    495.    477.
## 3         -0.62    0.638    396.    414.    423.    452.    392.    433.    387.
## 4         -0.62   -1.15     393.    429.    365.    383.    379.    416.    396.
## 5          0.378   0.667    552.    570.    563.    531.    532.    522.    482.
## 6         -0.62    0.357    441.    416.    407.    437.    473.    416.    428.
## # ... with 189 more variables: ODOKUMA8 <dbl>, ODOKUMA9 <dbl>, ODOKUMA10 <dbl>,
## #   ST097Q02TA <dbl+lbl>, ST100Q02TA <dbl+lbl>, ST102Q01TA <dbl+lbl>,
## #   ST102Q02TA <dbl+lbl>, ST102Q03TA <dbl+lbl>, ST102Q04TA <dbl+lbl>,
## #   ST211Q01HA <dbl+lbl>, ST211Q02HA <dbl+lbl>, ST211Q03HA <dbl+lbl>,
## #   ST212Q01HA <dbl+lbl>, ST212Q02HA <dbl+lbl>, ST212Q03HA <dbl+lbl>,
## #   ST104Q02NA <dbl+lbl>, ST213Q01HA <dbl+lbl>, ST213Q02HA <dbl+lbl>,
## #   ST213Q03HA <dbl+lbl>, ST213Q04HA <dbl+lbl>, ST150Q02IA <dbl+lbl>, ...
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































