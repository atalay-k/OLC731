# Veri duzenleme  - IV




- **join()** fonksiyonlari
  - **left_join()**
  - **right_join()**
  - **full_join()**
  - **inner_join()**
  - **semi_join()**
  - **anti_join()**


## **join()** fonksiyonu

- **join()** fonksiyonları iki veri setini istenilen şekilde birleştirme amacıyla kullanılırlar..

- **A** ve **B** veri setlerini birleştirmek istediğimizde 

  - Her iki veri setinden de hangi **satırları** almak istiyoruz?

  - Her iki veri setinden de hangi **sütunları** almak istiyoruz?

  - Satırların **eşleşip eşleşmeyeceğini** hangi değişkenlerle belirleyeceğiz?



## Join Türleri

- Çok sayıda **join()** fonksiyonu bulunmaktadır. 
- **A %>% left_join(B)**

`A` dan tüm satırları, mümkün olduğunda `B` ile eşleştir (olmadığında "NA" verir), hem `A` hem de `B` den gelen sütunları alır.


\begin{center}\includegraphics[width=0.6\linewidth]{images/left_join} \end{center}

- **A %>% right_join(B)**

`B` den tüm satırları, mümkün olduğunda `A` ile eşleştir (olmadığında "NA" verir), hem `A` hem de `B` den gelen sütunları alır.


\begin{center}\includegraphics[width=0.6\linewidth]{images/right_join} \end{center}

-  Pratikte genellike **left_join()** kullanılır.




- **A %>% inner_join(B)**
<br>
yanlızca `A` ve `B` nin eşleşen satırlarını birleştirir. Hem `A` hem de `B` den gelen sütunları alır.


\begin{center}\includegraphics[width=0.75\linewidth]{images/inner_join} \end{center}





- **A %>% full_join(B)** 

`A` ve `B` den tüm satırları birleştirir. Hem `A` hem de `B` den gelen sütunları alır.


\begin{center}\includegraphics[width=0.75\linewidth]{images/full_join} \end{center}







- **A %>% semi_join(B)**

`A` nın `B` ile eşleşen satırlarını alır.  Sadece `A` dan gelen sütunları alır.


\begin{center}\includegraphics[width=0.75\linewidth]{images/semi_join} \end{center}






-  **A %>% anti_join(B)**
<br>
`A` nın `B` ile eşleşemeyen satırlarını alır. Sadece `A` dan gelen sütunları alır.


\begin{center}\includegraphics[width=0.75\linewidth]{images/anti_join} \end{center}



- Aynı değerleri içeren satırların olduğu sütunların *eşleşmesi* gerektiğini söylüyoruz.

- Bunları birleştirme için bir **by =** argümanını kullanıyoruz.

- Eğer birleştirme yapmak istediğimiz sütun/ların isimleri aynı ise **by =** argümanını kullanmaya gerek yoktur. 



cinsiyet1



```r
cinsiyet1
```

```
##        ogrenci cinsiyet
## 1    Mert Kaya    Erkek
## 2 Zeynep Turan      Kiz
## 3  Zeynep Inal      Kiz
```

kangrubu1



```r
kangrubu1
```

```
##        ogrenci kangrubu
## 1 Zeynep Turan  A Rh(-)
## 2  Zeynep Inal 0 Rh (+)
## 3     Can Eser   ARh(+)
```


```r
left_join(cinsiyet1,kangrubu1)
```

```
## Joining with `by = join_by(ogrenci)`
```

```
##        ogrenci cinsiyet kangrubu
## 1    Mert Kaya    Erkek     <NA>
## 2 Zeynep Turan      Kiz  A Rh(-)
## 3  Zeynep Inal      Kiz 0 Rh (+)
```


```r
right_join(cinsiyet1,kangrubu1)
```

```
## Joining with `by = join_by(ogrenci)`
```

```
##        ogrenci cinsiyet kangrubu
## 1 Zeynep Turan      Kiz  A Rh(-)
## 2  Zeynep Inal      Kiz 0 Rh (+)
## 3     Can Eser     <NA>   ARh(+)
```



cinsiyet1

```r
cinsiyet1
```

```
##        ogrenci cinsiyet
## 1    Mert Kaya    Erkek
## 2 Zeynep Turan      Kiz
## 3  Zeynep Inal      Kiz
```

kangrubu1

```r
kangrubu1
```

```
##        ogrenci kangrubu
## 1 Zeynep Turan  A Rh(-)
## 2  Zeynep Inal 0 Rh (+)
## 3     Can Eser   ARh(+)
```



```r
inner_join(cinsiyet1,kangrubu1)
```

```
## Joining with `by = join_by(ogrenci)`
```

```
##        ogrenci cinsiyet kangrubu
## 1 Zeynep Turan      Kiz  A Rh(-)
## 2  Zeynep Inal      Kiz 0 Rh (+)
```



```r
full_join(cinsiyet1,kangrubu1)
```

```
## Joining with `by = join_by(ogrenci)`
```

```
##        ogrenci cinsiyet kangrubu
## 1    Mert Kaya    Erkek     <NA>
## 2 Zeynep Turan      Kiz  A Rh(-)
## 3  Zeynep Inal      Kiz 0 Rh (+)
## 4     Can Eser     <NA>   ARh(+)
```



cinsiyet1

```r
cinsiyet1
```

```
##        ogrenci cinsiyet
## 1    Mert Kaya    Erkek
## 2 Zeynep Turan      Kiz
## 3  Zeynep Inal      Kiz
```

kangrubu1

```r
kangrubu1
```

```
##        ogrenci kangrubu
## 1 Zeynep Turan  A Rh(-)
## 2  Zeynep Inal 0 Rh (+)
## 3     Can Eser   ARh(+)
```



```r
semi_join(cinsiyet1,kangrubu1)
```

```
## Joining with `by = join_by(ogrenci)`
```

```
##        ogrenci cinsiyet
## 1 Zeynep Turan      Kiz
## 2  Zeynep Inal      Kiz
```



```r
anti_join(cinsiyet1,kangrubu1)
```

```
## Joining with `by = join_by(ogrenci)`
```

```
##     ogrenci cinsiyet
## 1 Mert Kaya    Erkek
```




cinsiyet1

```r
cinsiyet2
```

```
##        ogrenci cinsiyet
## 1    Mert Kaya    Erkek
## 2 Zeynep Turan      Kiz
## 3  Zeynep Inal      Kiz
```

kangrubu1

```r
kangrubu2
```

```
##             ad kangrubu
## 1 Zeynep Turan  A Rh(-)
## 2  Zeynep Inal 0 Rh (+)
## 3     Can Eser   ARh(+)
```



```r
cinsiyet2 %>% 
left_join(kangrubu2,by=c("ogrenci"="ad"))
```

```
##        ogrenci cinsiyet kangrubu
## 1    Mert Kaya    Erkek     <NA>
## 2 Zeynep Turan      Kiz  A Rh(-)
## 3  Zeynep Inal      Kiz 0 Rh (+)
```



```r
kangrubu2 %>% 
left_join(cinsiyet2,by=c("ad"="ogrenci"))
```

```
##             ad kangrubu cinsiyet
## 1 Zeynep Turan  A Rh(-)      Kiz
## 2  Zeynep Inal 0 Rh (+)      Kiz
## 3     Can Eser   ARh(+)     <NA>
```



\begin{center}\includegraphics[width=0.7\linewidth]{images/kumeislemleri} \end{center}


```r
intersect(1:5, 4:8)
union(1:5, 4:8)
setdiff(1:5, 4:8)
setdiff(4:8, 1:5)
```

```
## [1] 4 5
## [1] 1 2 3 4 5 6 7 8
## [1] 1 2 3
## [1] 6 7 8
```




## Aynı değişken adları


```r
load("import/PISA_STU_2018.rda")
load("import/PISA_SCH_2018.rda")
load("import/PISA_COG_2018.rda")
load("import/PISA_OGR_2018.rda")
intersect(names(PISA_STU_2018), names(PISA_SCH_2018))
```

```
##  [1] "CNTRYID"   "CNT"       "CNTSCHID"  "CYC"       "NatCen"    "STRATUM"  
##  [7] "SUBNATIO"  "OECD"      "ADMINMODE" "BOOKID"    "SENWT"     "VER_DAT"
```


```r
intersect(names(PISA_STU_2018), names(PISA_COG_2018))
```

```
##  [1] "CNTRYID"      "CNT"          "CNTSCHID"     "CNTSTUID"     "CYC"         
##  [6] "NatCen"       "STRATUM"      "SUBNATIO"     "OECD"         "ADMINMODE"   
## [11] "LANGTEST_QQQ" "LANGTEST_COG" "LANGTEST_PAQ" "BOOKID"       "VER_DAT"
```


## join 


```r
miniOGR <- PISA_OGR_2018 %>% select(OKULID,OGRENCIID,CINSIYET,KITAPSAYISI,ST196Q02HA:ST196Q07HA)
miniOGR %>% head(2)
```

```
## # A tibble: 2 x 10
##     OKULID OGRENCIID   CINSIYET KITAPSAYISI ST196Q02HA ST196Q03HA ST196Q04HA
##      <dbl>     <dbl> <hvn_lbll>  <hvn_lbll> <hvn_lbll> <hvn_lbll> <hvn_lbll>
## 1 79200001  79200768          2           2          3          3          4
## 2 79200001  79201064          2           3          3          3          4
## # i 3 more variables: ST196Q05HA <hvn_lbll>, ST196Q06HA <hvn_lbll>,
## #   ST196Q07HA <hvn_lbll>
```


```r
miniSCH <- PISA_SCH_2018 %>% select(CNTSCHID,okulbuyukluk = SCHSIZE,sinifbuyuk= CLSIZE)
miniSCH %>% head(2)
```

```
## # A tibble: 2 x 3
##   CNTSCHID okulbuyukluk sinifbuyuk
##      <dbl>   <hvn_lbll> <hvn_lbll>
## 1 79200001          775         33
## 2 79200002         1178         53
```



- veri setinde eşleştirme yapılması istenilen değişkenin farklı adları olduğunda 

```r
left_join(miniOGR,miniSCH,by=c("OKULID"="CNTSCHID")) %>% head(6)
```

```
## # A tibble: 6 x 12
##     OKULID OGRENCIID   CINSIYET KITAPSAYISI ST196Q02HA ST196Q03HA ST196Q04HA
##      <dbl>     <dbl> <hvn_lbll>  <hvn_lbll> <hvn_lbll> <hvn_lbll> <hvn_lbll>
## 1 79200001  79200768          2           2          3          3          4
## 2 79200001  79201064          2           3          3          3          4
## 3 79200001  79201118          1           1          1          2          3
## 4 79200001  79201275          2           1          1          1          1
## 5 79200001  79201481          2           2          1          4          4
## 6 79200001  79201556          2           2          1          1          1
## # i 5 more variables: ST196Q05HA <hvn_lbll>, ST196Q06HA <hvn_lbll>,
## #   ST196Q07HA <hvn_lbll>, okulbuyukluk <hvn_lbll>, sinifbuyuk <hvn_lbll>
```



- konu ile ilgili daha fazla alıştırma için [adresini](https://rpubs.com/williamsurles/293454) inceleyebilirsiniz.

teşekkürler !





