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
##   ST097Q01TA               ST097Q02TA           ST097Q03TA ST097Q04TA ST097Q05TA
##   <dbl+lbl>                <dbl+lbl>            <dbl+lbl>  <dbl+lbl>  <dbl+lbl> 
## 1 1 [Her ders]             2 [Derslerin cogund~ 1 [Her de~ 1 [Her de~ 1 [Her de~
## 2 3 [cogunlukla test dili] 2 [Derslerin cogund~ 3 [cogunl~ 3 [cogunl~ 3 [cogunl~
## 3 2 [Derslerin cogunda]    3 [cogunlukla test ~ 3 [cogunl~ 3 [cogunl~ 3 [cogunl~
## 4 2 [Derslerin cogunda]    2 [Derslerin cogund~ 3 [cogunl~ 1 [Her de~ 1 [Her de~
## 5 3 [cogunlukla test dili] 3 [cogunlukla test ~ 4 [Bazi d~ 3 [cogunl~ 1 [Her de~
## 6 3 [cogunlukla test dili] 3 [cogunlukla test ~ 2 [Dersle~ 2 [Dersle~ 3 [cogunl~
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
##   ST097Q01TA               ST097Q02TA           ST097Q03TA ST097Q04TA ST097Q05TA
##   <dbl+lbl>                <dbl+lbl>            <dbl+lbl>  <dbl+lbl>  <dbl+lbl> 
## 1 1 [Her ders]             2 [Derslerin cogund~ 1 [Her de~ 1 [Her de~ 1 [Her de~
## 2 3 [cogunlukla test dili] 2 [Derslerin cogund~ 3 [cogunl~ 3 [cogunl~ 3 [cogunl~
## 3 2 [Derslerin cogunda]    3 [cogunlukla test ~ 3 [cogunl~ 3 [cogunl~ 3 [cogunl~
## 4 2 [Derslerin cogunda]    2 [Derslerin cogund~ 3 [cogunl~ 1 [Her de~ 1 [Her de~
## 5 3 [cogunlukla test dili] 3 [cogunlukla test ~ 4 [Bazi d~ 3 [cogunl~ 1 [Her de~
## 6 3 [cogunlukla test dili] 3 [cogunlukla test ~ 2 [Dersle~ 2 [Dersle~ 3 [cogunl~
```


### **ends_with()**

- **NA** ile **biten** degişkenlerin seçilmesi


```r
select(PISA_OGR_2018, ends_with("NA")) %>% head(6)
```

```
## # A tibble: 6 x 48
##   ST104Q02NA   ST104Q03NA ST104Q04NA ST016Q01NA ST123Q02NA ST123Q03NA ST123Q04NA
##   <dbl+lbl>    <dbl+lbl>  <dbl+lbl>       <dbl> <dbl+lbl>  <dbl+lbl>  <dbl+lbl> 
## 1 2 [Bazi der~ 2 [Bazi d~ 2 [Bazi d~         NA 4 [Kesinl~  4 [Kesin~ 4 [Kesinl~
## 2 2 [Bazi der~ 2 [Bazi d~ 3 [Dersle~          7 4 [Kesinl~  3 [Katil~ 1 [Kesinl~
## 3 2 [Bazi der~ 2 [Bazi d~ 2 [Bazi d~          4 3 [Katili~  3 [Katil~ 3 [Katili~
## 4 3 [Dersleri~ 2 [Bazi d~ 3 [Dersle~          3 3 [Katili~ NA         3 [Katili~
## 5 3 [Dersleri~ 2 [Bazi d~ 4 [Her de~          1 1 [Kesinl~  1 [Kesin~ 1 [Kesinl~
## 6 3 [Dersleri~ 2 [Bazi d~ 3 [Dersle~          4 3 [Katili~  3 [Katil~ 3 [Katili~
## # i 41 more variables: ST060Q01NA <dbl>, ST061Q01NA <dbl>,
## #   ST038Q03NA <dbl+lbl>, ST038Q04NA <dbl+lbl>, ST038Q05NA <dbl+lbl>,
## #   ST038Q06NA <dbl+lbl>, ST038Q07NA <dbl+lbl>, ST038Q08NA <dbl+lbl>,
## #   IC009Q05NA <dbl+lbl>, IC009Q06NA <dbl+lbl>, IC009Q07NA <dbl+lbl>,
## #   IC009Q10NA <dbl+lbl>, IC009Q11NA <dbl+lbl>, IC008Q07NA <dbl+lbl>,
## #   IC008Q13NA <dbl+lbl>, IC010Q02NA <dbl+lbl>, IC010Q05NA <dbl+lbl>,
## #   IC010Q06NA <dbl+lbl>, IC010Q09NA <dbl+lbl>, IC010Q10NA <dbl+lbl>, ...
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
##   ST097Q02TA   ST100Q02TA ST102Q01TA ST102Q02TA ST102Q03TA ST102Q04TA ST211Q02HA
##   <dbl+lbl>    <dbl+lbl>  <dbl+lbl>  <dbl+lbl>  <dbl+lbl>  <dbl+lbl>  <dbl+lbl> 
## 1 2 [Dersleri~ 2 [Dersle~ 2 [Dersle~ 2 [Dersle~ 3 [cogunl~ 2 [Dersle~ 3 [Katili~
## 2 2 [Dersleri~ 3 [cogunl~ 2 [Dersle~ 3 [cogunl~ 2 [Dersle~ 2 [Dersle~ 2 [Katilm~
## 3 3 [cogunluk~ 2 [Dersle~ 2 [Dersle~ 2 [Dersle~ 3 [cogunl~ 3 [cogunl~ 2 [Katilm~
## 4 2 [Dersleri~ 2 [Dersle~ 2 [Dersle~ 3 [cogunl~ 4 [Bazi d~ 3 [cogunl~ 2 [Katilm~
## 5 3 [cogunluk~ 3 [cogunl~ 3 [cogunl~ 1 [Her de~ 2 [Dersle~ 2 [Dersle~ 2 [Katilm~
## 6 3 [cogunluk~ 3 [cogunl~ 3 [cogunl~ 3 [cogunl~ 3 [cogunl~ 3 [cogunl~ 3 [Katili~
## # i 52 more variables: ST212Q02HA <dbl+lbl>, ST104Q02NA <dbl+lbl>,
## #   ST213Q02HA <dbl+lbl>, ST150Q02IA <dbl+lbl>, ST153Q02HA <dbl+lbl>,
## #   ST158Q02HA <dbl+lbl>, ST160Q02IA <dbl+lbl>, ST167Q02IA <dbl+lbl>,
## #   ST176Q02IA <dbl+lbl>, ST161Q02HA <dbl+lbl>, ST163Q02HA <dbl+lbl>,
## #   ST164Q02IA <dbl+lbl>, ST165Q02IA <dbl+lbl>, ST166Q02HA <dbl+lbl>,
## #   ST225Q02HA <dbl+lbl>, ST181Q02HA <dbl+lbl>, ST183Q02HA <dbl+lbl>,
## #   ST185Q02HA <dbl+lbl>, ST186Q02HA <dbl+lbl>, ST208Q02HA <dbl+lbl>, ...
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
## #   ODOKUMA9 <dbl>, ODOKUMA10 <dbl>, ST097Q02TA <dbl+lbl>,
## #   ST100Q02TA <dbl+lbl>, ST102Q01TA <dbl+lbl>, ST102Q02TA <dbl+lbl>,
## #   ST102Q03TA <dbl+lbl>, ST102Q04TA <dbl+lbl>, ST211Q01HA <dbl+lbl>,
## #   ST211Q02HA <dbl+lbl>, ST211Q03HA <dbl+lbl>, ST212Q01HA <dbl+lbl>,
## #   ST212Q02HA <dbl+lbl>, ST212Q03HA <dbl+lbl>, ST104Q02NA <dbl+lbl>,
## #   ST213Q01HA <dbl+lbl>, ST213Q02HA <dbl+lbl>, ST213Q03HA <dbl+lbl>, ...
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































