# Veri duzenleme  - III

- Bu bölümde pratiklik ve anlaşılabilirlik açısında **miniPISA** verisini kullanacağız. Bunun için öncelikle _import_ adlı klasöre indirilen veri setini aşağıdaki komut ile R ortamına yüklenmelidir. 

- 🔗 [miniPISA.rda](import/miniPISA.rda)



- Seçme ve Dönüştürme 📊 amacıyla aşağıdaki fonksiyonlar kullanılabilir.

- **select()** fonksiyonu
- **select()** fonksiyonu içinde çalışan fonksiyonlar
- **rename()** fonksiyonu
- **mutate()** ve **transmute()** fonksiyonları

## select() fonksiyonu

- **select()** fonksiyonu ile sütun bazında seçim yapılabilir.

- Veri yapısının incelenmesi.


```r
library(dplyr)
load("import/miniPISA.rda") # ogrenci verisi
dim(miniPISA)
```

```
## [1] 6890   16
```

- 16 sütunla çalışmayacaksanız, problem durumunuza uygun sütunları seçebilirsiniz. Fonksiyon içinde degişkenler tek tek virgül `,` ile ayrılarak seçim yapılabilir.


```r
select(veri seti, degisken adi, degisken adi,..)
veri seti %>% select(degisken adi, degisken adi,..)
```


- OGR_ID, OGR_ID, CNSYT ,AED, BED değişkenlerinin seçimi


```r
select(miniPISA, OGR_ID, CNSYT,AED,BED) %>% head(6)
```

<div class="kable-table">

|   OGR_ID| CNSYT| AED| BED|
|--------:|-----:|---:|---:|
| 79200768|     2|   2|   2|
| 79201064|     2|   2|   2|
| 79201118|     1|   1|   2|
| 79201275|     2|   6|   6|
| 79201481|     2|   4|   4|
| 79201556|     2|   4|   6|

</div>

- Aynı işlem `c()` fonksiyonu içinde de yapılabilir.


```r
select(miniPISA, c(OGR_ID, CNSYT,AED,BED))
```

- **select()** fonksiyonu ile sütun bazında seçim yapılabilir.


```r
miniPISA %>% select(OGR_ID, CNSYT,AED,BED) %>% head(6)
```

<div class="kable-table">

|   OGR_ID| CNSYT| AED| BED|
|--------:|-----:|---:|---:|
| 79200768|     2|   2|   2|
| 79201064|     2|   2|   2|
| 79201118|     1|   1|   2|
| 79201275|     2|   6|   6|
| 79201481|     2|   4|   4|
| 79201556|     2|   4|   6|

</div>


- **select()** fonksiyonu belirli bir aralıktaki değişkenler iki nokta `:` opertorü ile seçilebilir.

- örneğin okumadan alınan zevke ilişkin maddeler aşağıdaki şekilde seçilebilir.


```r
miniPISA %>% select(ST097Q01TA:ST097Q05TA) %>% head(6)
```

<div class="kable-table">

| ST097Q01TA| ST097Q02TA| ST097Q03TA| ST097Q04TA| ST097Q05TA|
|----------:|----------:|----------:|----------:|----------:|
|          1|          2|          1|          1|          1|
|          3|          2|          3|          3|          3|
|          2|          3|          3|          3|          3|
|          2|          2|          3|          1|          1|
|          3|          3|          4|          3|          1|
|          3|          3|          2|          2|          3|

</div>


- **select()**  fonksiyonu belirli bir aralıkta yer alan değişkenler iki nokta **:** opertorü ile seçilirken, bu aralıkta dahil edilmek istenmeyen degişkenler kısa çizgi **-** operatorü ile hariç tutulabilir.


```r
miniPISA <- expss::drop_var_labs(miniPISA)
miniPISA %>% select(OGR_ID:BED,-SNF) %>% head(6)
```

<div class="kable-table">

|   OGR_ID| CNSYT| AED| BED|
|--------:|-----:|---:|---:|
| 79200768|     2|   2|   2|
| 79201064|     2|   2|   2|
| 79201118|     1|   1|   2|
| 79201275|     2|   6|   6|
| 79201481|     2|   4|   4|
| 79201556|     2|   4|   6|

</div>


### **starts_with()**

- Sadece **select()** fonksiyonu içinde çalışan birtakım fonksiyonlar değişken seçim işini kolaylaştırır.

- **ST097** ile başlayan degişkenlerin seçilmesi


```r
select(miniPISA, starts_with("ST097")) %>% head(6)
```

<div class="kable-table">

| ST097Q01TA| ST097Q02TA| ST097Q03TA| ST097Q04TA| ST097Q05TA|
|----------:|----------:|----------:|----------:|----------:|
|          1|          2|          1|          1|          1|
|          3|          2|          3|          3|          3|
|          2|          3|          3|          3|          3|
|          2|          2|          3|          1|          1|
|          3|          3|          4|          3|          1|
|          3|          3|          2|          2|          3|

</div>


### **ends_with()**

- **TA** ile **biten** degişkenlerin seçilmesi


```r
select(miniPISA, ends_with("TA")) %>% head(6)
```

<div class="kable-table">

| ST097Q01TA| ST097Q02TA| ST097Q03TA| ST097Q04TA| ST097Q05TA|
|----------:|----------:|----------:|----------:|----------:|
|          1|          2|          1|          1|          1|
|          3|          2|          3|          3|          3|
|          2|          3|          3|          3|          3|
|          2|          2|          3|          1|          1|
|          3|          3|          4|          3|          1|
|          3|          3|          2|          2|          3|

</div>


### **contains()**

- içinde **ST** geçen değişkenlerin seçilmesi


```r
select(miniPISA,contains("ST")) %>% head(6)
```

<div class="kable-table">

| ST097Q01TA| ST097Q02TA| ST097Q03TA| ST097Q04TA| ST097Q05TA|
|----------:|----------:|----------:|----------:|----------:|
|          1|          2|          1|          1|          1|
|          3|          2|          3|          3|          3|
|          2|          3|          3|          3|          3|
|          2|          2|          3|          1|          1|
|          3|          3|          4|          3|          1|
|          3|          3|          2|          2|          3|

</div>


###  **matches()**

- içinde **02** geçen değişkenlerin seçilmesi


```r
select(miniPISA,matches("02")) %>% head(6)
```

<div class="kable-table">

| ST097Q02TA|
|----------:|
|          2|
|          2|
|          3|
|          2|
|          3|
|          3|

</div>


### **num_range()**

-  ardışık ilerleyen değişkenlerin seçilmesi


```r
select(miniPISA,num_range("O_OD",1:5)) %>% head(6)
```

<div class="kable-table">

|  O_OD1|  O_OD2|  O_OD3|  O_OD4|  O_OD5|
|------:|------:|------:|------:|------:|
| 376.02| 417.75| 420.63| 413.84| 434.43|
| 512.32| 473.23| 563.90| 485.40| 500.39|
| 396.38| 413.86| 423.12| 452.12| 392.43|
| 393.01| 428.76| 364.85| 382.52| 378.56|
| 552.46| 570.11| 562.96| 530.84| 532.49|
| 441.29| 415.68| 406.59| 437.00| 473.04|

</div>


###  Matıksal operatorler ile seçim

- farklı fonksiyonları aynı anda mantıksal operatörlerle kullanarak da seçim yapabilirsiniz.

- veya **|** operatorünün kullanılması


```r
miniPISA %>% 
select(contains("O_OD") | matches("2")) %>% 
  head(6)
```

<div class="kable-table">

|  O_OD1|  O_OD2|  O_OD3|  O_OD4|  O_OD5| ST097Q02TA|
|------:|------:|------:|------:|------:|----------:|
| 376.02| 417.75| 420.63| 413.84| 434.43|          2|
| 512.32| 473.23| 563.90| 485.40| 500.39|          2|
| 396.38| 413.86| 423.12| 452.12| 392.43|          3|
| 393.01| 428.76| 364.85| 382.52| 378.56|          2|
| 552.46| 570.11| 562.96| 530.84| 532.49|          3|
| 441.29| 415.68| 406.59| 437.00| 473.04|          3|

</div>


- ve **&** operatorunun kullanılması


```r
miniPISA %>% 
select(contains("O_OD") & matches("2")) %>%
  head(6)
```

<div class="kable-table">

|  O_OD2|
|------:|
| 417.75|
| 473.23|
| 413.86|
| 428.76|
| 570.11|
| 415.68|

</div>


- hariç tutmak amacıyla **-** operatorü kullanılabilir.


```r
select(miniPISA,-contains("O_OD"),-matches("02"))  %>% head(5)
```

<div class="kable-table">

|   OGR_ID| SNF| CNSYT| AED| BED| O_ZEVK| ST097Q01TA| ST097Q03TA| ST097Q04TA| ST097Q05TA|
|--------:|---:|-----:|---:|---:|------:|----------:|----------:|----------:|----------:|
| 79200768|  10|     2|   2|   2|  -0.29|          1|          1|          1|          1|
| 79201064|  10|     2|   2|   2|   0.60|          3|          3|          3|          3|
| 79201118|  10|     1|   1|   2|   0.64|          2|          3|          3|          3|
| 79201275|   9|     2|   6|   6|  -1.15|          2|          3|          1|          1|
| 79201481|   9|     2|   4|   4|   0.67|          3|          4|          3|          1|

</div>


### **rename()** fonksiyonu

- **select()** fonksiyonu icinde değişken seçimi sırasında değişken adı değişimi yapılabilir.

- Örnekte **O_ZEVK** degişkeninin adını **okumazevk** olarak değiştirip seçebilirsiniz.


```r
miniPISA %>%
select(OGR_ID,SNF,CNSYT,AED,BED,okumazevk = O_ZEVK) %>%
head(2)
```

<div class="kable-table">

|   OGR_ID| SNF| CNSYT| AED| BED| okumazevk|
|--------:|---:|-----:|---:|---:|---------:|
| 79200768|  10|     2|   2|   2|     -0.29|
| 79201064|  10|     2|   2|   2|      0.60|

</div>


- Örnekte ise **O_ZEVK** degişkeninin adı okumazevk olarak **rename()** fonksiyonu ile de değiştirilebilir.


```r
miniPISA %>%
select(OGR_ID,SNF,CNSYT,AED,O_ZEVK) %>%
rename(okumazevk=O_ZEVK)%>%
head(2)
```

<div class="kable-table">

|   OGR_ID| SNF| CNSYT| AED| okumazevk|
|--------:|---:|-----:|---:|---------:|
| 79200768|  10|     2|   2|     -0.29|
| 79201064|  10|     2|   2|      0.60|

</div>


### mutate fonksiyonu

- **mutate()** fonksiyonu ile veri setine yeni değişken ekleyebilirsiniz.

- **transmute()** fonksiyonu ile veri setine yeni değişken eklenirken, eski değişken/ler veri setiden çıkarılır.

- Okumadan zevk alma maddelerinden bir veri seti oluşturup, bu veri setine toplam puan ekleme


```r
zevk  <- select(miniPISA, starts_with("ST097"))
zevk  <- expss::drop_var_labs(zevk)
zevk %>%
mutate(toplam =ST097Q01TA+ST097Q02TA+ST097Q03TA+ST097Q04TA+ ST097Q05TA) %>% head(2)
```

<div class="kable-table">

| ST097Q01TA| ST097Q02TA| ST097Q03TA| ST097Q04TA| ST097Q05TA| toplam|
|----------:|----------:|----------:|----------:|----------:|------:|
|          1|          2|          1|          1|          1|      6|
|          3|          2|          3|          3|          3|     14|

</div>



- Değişken değerleri bir önceki örnekteki gibi tek tek **+** ile toplanacağı gibi **rowSums()** fonksiyonu ile de aşağıdaki gibi toplanabilir

```r
zevk %>%
mutate(toplam=rowSums(select(., ST097Q01TA:ST097Q05TA))) %>%
head(2)
```

<div class="kable-table">

| ST097Q01TA| ST097Q02TA| ST097Q03TA| ST097Q04TA| ST097Q05TA| toplam|
|----------:|----------:|----------:|----------:|----------:|------:|
|          1|          2|          1|          1|          1|      6|
|          3|          2|          3|          3|          3|     14|

</div>



- Yeni eklenecek yeri `.before` ya da `.after` argumanları ile düzenleyebilirsiniz.


```r
zevk %>%
mutate(toplam=rowSums(select(., ST097Q01TA:ST097Q05TA)),.before= ST097Q01TA)%>%
  head(2)
```

<div class="kable-table">

| toplam| ST097Q01TA| ST097Q02TA| ST097Q03TA| ST097Q04TA| ST097Q05TA|
|------:|----------:|----------:|----------:|----------:|----------:|
|      6|          1|          2|          1|          1|          1|
|     14|          3|          2|          3|          3|          3|

</div>


### transmute() fonksiyonu

- **transmute()** fonksiyonu kullanılarak yeni değişken oluşturulduğunda, işlemde kullanılan değişkenler veri setinden çıkarılır.


```r
zevk %>%
transmute(toplam=rowSums(select(., ST097Q01TA:ST097Q05TA))) %>%
head(2)
```

<div class="kable-table">

| toplam|
|------:|
|      6|
|     14|

</div>



- Fonksiyonda üretilen ilk değişken kullanılarak da yeni değişken üretilebilir.

- Ilk olarak okumaktan alınan zevk ölçen maddelerden yeni bir veri oluşturulmuş, daha sonra bu puanların önce toplam puanları daha sonra toplam puanların kareleri alınmıştır.


```r
zevk <- miniPISA %>%
  expss::drop_var_labs() %>%
  select(ST097Q01TA:ST097Q05TA)

zevk%>%
  rowwise() %>%
  mutate(toplam = sum(across()))%>%
  mutate(toplam_kare=toplam*toplam) %>% 
  head(2)
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
table(miniPISA$SNF)
```

```
## 
##    7    8    9   10   11   12 
##    3   19 1295 5360  207    6
```

- **SNF** değişkenini kullanarak ortaokul ve lise olmak üzere iki düzeyli **OKUL** adlı bir değişken oluşturalım.




```r
miniPISA %>%
  select(1:5) %>%
  mutate(okul = ifelse(SNF == 7 | SNF == 8,
                       "Ortaokul", "Lise")) %>%
    head(3)
```

<div class="kable-table">

|   OGR_ID| SNF| CNSYT| AED| BED|okul |
|--------:|---:|-----:|---:|---:|:----|
| 79200768|  10|     2|   2|   2|Lise |
| 79201064|  10|     2|   2|   2|Lise |
| 79201118|  10|     1|   1|   2|Lise |

</div>


## case_when()

- **case_when()** fonksiyonu çoklu **ifelse() ** kullanımı ile benzer işlevi sağlar.

- **case_when()** birden fazla koşula dayalı karşılaştırmalarda yeni bir değişken oluşturmak amacıyla kullanılır.

- O_OD_1 düzeye ilişikin betimsel istatistikler

```r
summary(miniPISA$O_OD1)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   175.6   402.6   463.4   464.2   525.7   771.5
```


- O_OD1 değişkeninin kategorik hale getirilmesi


```r
v1 <- miniPISA %>%
  mutate(O_OD1_kategorik =
    case_when(
      O_OD1 <=  402.6  ~ "dusuk",
      O_OD1 > 402.6  & O_OD1 <  525.7 ~ "orta",
      O_OD1 >=525.7 ~ "yuksek" )) %>%
      select(O_OD1,O_OD1_kategorik)
```


- Olusturulan yeni O_OD1_kategorik degişkeninin veri setinde nasıl dağıldığını inceleme



```r
v1 %>% group_by(O_OD1_kategorik) %>% summarize(f=n())
```

<div class="kable-table">

|O_OD1_kategorik |    f|
|:---------------|----:|
|dusuk           | 1724|
|orta            | 3443|
|yuksek          | 1723|

</div>


teşekkürler !


- [Siz de yapın](https://learnr-examples.shinyapps.io/ex-data-filter/#section-welcome>)

- [Siz de yapın](https://learnr-examples.shinyapps.io/ex-data-summarise/)
--


