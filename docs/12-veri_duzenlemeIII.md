# Veri duzenleme  - III

- Bu bölümde pratiklik ve anlaşılabilirlik açısında **midiPISA** verisini kullanacağız.   Verinin oluşturulması aşağıdaki kodla sağlanabilir.


```r
library(tuev)
data(PISA_OGR_2018)
midiPISA <- PISA_OGR_2018 %>% 
  select(OGRENCIID,SINIF,CINSIYET,
         Anne_Egitim,Baba_Egitim,OKUMA_ZEVK,
         ST097Q01TA:ST097Q05TA,ODOKUMA1:ODOKUMA5)
```

- midiPISA veri seti; öğrenci id (OGRENCIID), sınıf düzeyi (SINIF), cinsiyet (CINSIYET), anne eğitim düzeyi (Anne_Egitim), baba eğitim düzeyi (Baba_Egitim), okumaktan zevk alma (OKUMA_ZEVK), ST097Q01TA, ST097Q02TA, ST097Q03TA, ST097Q04TA, ST097Q05TA, okuma puanı olası değer 1 (ODOKUMA1), okuma puanı olası değer 2 (ODOKUMA2), okuma puanı olası değer 3 (ODOKUMA3), okuma puanı olası değer 4 (ODOKUMA4), okuma puanı olası değer 5 (ODOKUMA5) değişkenleri olmak üzere toplam 16 değişkenden oluşmaktadır.




- PISA verileri OECD web adresinden SPSS formatında çekildiği için değişken etiketleri(label) ile birlikte gelmektedir. Bu etiket isimleri bazen R paketlerindeki fonksiyonlar ile birlikte çalışmamaktadır. Bu nedenle "`expss::drop_var_labs`" bu etiketlerin kaldırılmasını sağlar ve midiPISA veri seti üzerine kaydedilir.


```r
midiPISA <- expss::drop_var_labs(midiPISA)
```


- Bir diğer alternatif ise değişken etiketlerini faktör düzeyi olarak kaydetmektir. Bu işlem aşağıdaki kodlarla sağlanabilir.


```r
library(sjlabelled)
midiPISA <- midiPISA %>% mutate_if(is_labelled, as_factor)
# Faktor degiskenlere duzey atama amacıyla yazılan fonksiyon
levelsnames <- function(x){
  levels(x) <- names(attr(x,"labels"))
  x
}
# Yazılan fonkisyonun faktor degiskenlere uygulanması
midiPISA <-mutate_if(midiPISA,is.factor, levelsnames)
```

- Seçme ve dönüştürme amacıyla aşağıdaki fonksiyonlar kullanılabilir.

- **select()** fonksiyonu
- **select()** fonksiyonu içinde çalışan fonksiyonlar
- **rename()** fonksiyonu
- **mutate()** ve **transmute()** fonksiyonları

## select() fonksiyonu

- **select()** fonksiyonu ile sütun bazında seçim yapılabilir.

- Veri yapısının incelenmesi.


```r
library(dplyr)

dim(midiPISA)
```

```
## [1] 6890   16
```

- 16 sütunla çalışmayacaksanız, problem durumunuza uygun sütunları seçebilirsiniz. Fonksiyon içinde degişkenler tek tek virgül `,` ile ayrılarak seçim yapılabilir.


```r
select(veri seti, degisken adi, degisken adi,..)
veri seti %>% select(degisken adi, degisken adi,..)
```


- OGR_ID, CNSYT ,AED, BED değişkenlerinin seçimi


```r
midiPISA %>%
  select(OGRENCIID,ST097Q01TA,ST097Q04TA,OKUMA_ZEVK)%>% 
head(5) 
```

<div class="kable-table">

| OGRENCIID| ST097Q01TA| ST097Q04TA| OKUMA_ZEVK|
|---------:|----------:|----------:|----------:|
|  79200768|          1|          1|    -0.2891|
|  79201064|          3|          3|     0.6040|
|  79201118|          2|          3|     0.6380|
|  79201275|          2|          1|    -1.1538|
|  79201481|          3|          3|     0.6669|

</div>

- Aynı işlem `c()` fonksiyonu içinde de yapılabilir.


```r
select(midiPISA, c(OGRENCIID,ST097Q01TA,ST097Q04TA,OKUMA_ZEVK))
```

- **select()** fonksiyonu ile sütun bazında seçim yapılabilir.


```r
midiPISA %>% select(OGRENCIID,ST097Q01TA,ST097Q04TA,OKUMA_ZEVK) %>% head(6)
```

<div class="kable-table">

| OGRENCIID| ST097Q01TA| ST097Q04TA| OKUMA_ZEVK|
|---------:|----------:|----------:|----------:|
|  79200768|          1|          1|    -0.2891|
|  79201064|          3|          3|     0.6040|
|  79201118|          2|          3|     0.6380|
|  79201275|          2|          1|    -1.1538|
|  79201481|          3|          3|     0.6669|
|  79201556|          3|          2|     0.3568|

</div>


- **select()** fonksiyonu belirli bir aralıktaki değişkenler iki nokta `:` opertorü ile seçilebilir.

- örneğin okumadan alınan zevke ilişkin maddeler aşağıdaki şekilde seçilebilir.


```r
midiPISA %>% select(ST097Q01TA:ST097Q05TA) %>% head(6)
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
midiPISA %>% select(OGRENCIID:ST097Q04TA,-CINSIYET) %>% head(6)
```

<div class="kable-table">

| OGRENCIID| SINIF| Anne_Egitim| Baba_Egitim| OKUMA_ZEVK| ST097Q01TA| ST097Q02TA| ST097Q03TA| ST097Q04TA|
|---------:|-----:|-----------:|-----------:|----------:|----------:|----------:|----------:|----------:|
|  79200768|    10|           2|           2|    -0.2891|          1|          2|          1|          1|
|  79201064|    10|           2|           2|     0.6040|          3|          2|          3|          3|
|  79201118|    10|           1|           2|     0.6380|          2|          3|          3|          3|
|  79201275|     9|           6|           6|    -1.1538|          2|          2|          3|          1|
|  79201481|     9|           4|           4|     0.6669|          3|          3|          4|          3|
|  79201556|    10|           4|           6|     0.3568|          3|          3|          2|          2|

</div>


### **starts_with()**

- Sadece **select()** fonksiyonu içinde çalışan birtakım fonksiyonlar değişken seçim işini kolaylaştırır.

- **ST097** ile başlayan degişkenlerin seçilmesi


```r
select(midiPISA, starts_with("ST097")) %>% head(6)
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
select(midiPISA, ends_with("TA")) %>% head(6)
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
select(midiPISA,contains("ST")) %>% head(6)
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
select(midiPISA,matches("02")) %>% head(6)
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
select(midiPISA,num_range("ODOKUMA",1:5)) %>% head(6)
```

<div class="kable-table">

| ODOKUMA1| ODOKUMA2| ODOKUMA3| ODOKUMA4| ODOKUMA5|
|--------:|--------:|--------:|--------:|--------:|
|  376.022|  417.746|  420.630|  413.837|  434.434|
|  512.316|  473.229|  563.902|  485.396|  500.394|
|  396.383|  413.859|  423.121|  452.124|  392.434|
|  393.006|  428.757|  364.850|  382.522|  378.563|
|  552.457|  570.109|  562.955|  530.835|  532.487|
|  441.286|  415.682|  406.586|  437.001|  473.036|

</div>


###  Matıksal operatorler ile seçim

- farklı fonksiyonları aynı anda mantıksal operatörlerle kullanarak da seçim yapabilirsiniz.

- veya **|** operatorünün kullanılması


```r
midiPISA %>% 
select(contains("ODOKUMA") | matches("2")) %>% 
  head(6)
```

<div class="kable-table">

| ODOKUMA1| ODOKUMA2| ODOKUMA3| ODOKUMA4| ODOKUMA5| ST097Q02TA|
|--------:|--------:|--------:|--------:|--------:|----------:|
|  376.022|  417.746|  420.630|  413.837|  434.434|          2|
|  512.316|  473.229|  563.902|  485.396|  500.394|          2|
|  396.383|  413.859|  423.121|  452.124|  392.434|          3|
|  393.006|  428.757|  364.850|  382.522|  378.563|          2|
|  552.457|  570.109|  562.955|  530.835|  532.487|          3|
|  441.286|  415.682|  406.586|  437.001|  473.036|          3|

</div>


- ve **&** operatorunun kullanılması


```r
midiPISA %>% 
select(contains("ODOKUMA") & matches("2")) %>%
  head(6)
```

<div class="kable-table">

| ODOKUMA2|
|--------:|
|  417.746|
|  473.229|
|  413.859|
|  428.757|
|  570.109|
|  415.682|

</div>


- hariç tutmak amacıyla **-** operatorü kullanılabilir.


```r
select(midiPISA,-contains("ODOKUMA"),-matches("02"))  %>% head(5)
```

<div class="kable-table">

| OGRENCIID| SINIF| CINSIYET| Anne_Egitim| Baba_Egitim| OKUMA_ZEVK| ST097Q01TA| ST097Q03TA| ST097Q04TA| ST097Q05TA|
|---------:|-----:|--------:|-----------:|-----------:|----------:|----------:|----------:|----------:|----------:|
|  79200768|    10|        2|           2|           2|    -0.2891|          1|          1|          1|          1|
|  79201064|    10|        2|           2|           2|     0.6040|          3|          3|          3|          3|
|  79201118|    10|        1|           1|           2|     0.6380|          2|          3|          3|          3|
|  79201275|     9|        2|           6|           6|    -1.1538|          2|          3|          1|          1|
|  79201481|     9|        2|           4|           4|     0.6669|          3|          4|          3|          1|

</div>


### **rename()** fonksiyonu

- **select()** fonksiyonu icinde değişken seçimi sırasında değişken adı değişimi yapılabilir.

- Örnekte **O_ZEVK** degişkeninin adını **okumazevk** olarak değiştirip seçebilirsiniz.


```r
midiPISA %>%
select(OGRENCIID,SINIF,CINSIYET,Anne_Egitim,Baba_Egitim,okumazevk = OKUMA_ZEVK) %>%
head(2)
```

<div class="kable-table">

| OGRENCIID| SINIF| CINSIYET| Anne_Egitim| Baba_Egitim| okumazevk|
|---------:|-----:|--------:|-----------:|-----------:|---------:|
|  79200768|    10|        2|           2|           2|   -0.2891|
|  79201064|    10|        2|           2|           2|    0.6040|

</div>


- Örnekte ise **O_ZEVK** degişkeninin adı okumazevk olarak **rename()** fonksiyonu ile de değiştirilebilir.


```r
midiPISA %>%
select(OGRENCIID,SINIF,CINSIYET,Anne_Egitim,Baba_Egitim,OKUMA_ZEVK) %>%
rename(okumazevk=OKUMA_ZEVK)%>%
head(2)
```

<div class="kable-table">

| OGRENCIID| SINIF| CINSIYET| Anne_Egitim| Baba_Egitim| okumazevk|
|---------:|-----:|--------:|-----------:|-----------:|---------:|
|  79200768|    10|        2|           2|           2|   -0.2891|
|  79201064|    10|        2|           2|           2|    0.6040|

</div>


### mutate fonksiyonu

- **mutate()** fonksiyonu ile veri setine yeni değişken ekleyebilirsiniz.

- **transmute()** fonksiyonu ile veri setine yeni değişken eklenirken, eski değişken/ler veri setiden çıkarılır.

- Okumadan zevk alma maddelerinden bir veri seti oluşturup, bu veri setine toplam puan ekleme


```r
zevk  <- select(midiPISA, starts_with("ST097"))
zevk  <- expss::drop_var_labs(zevk)
zevk %>%
mutate(toplam =ST097Q01TA+ST097Q02TA+ST097Q03TA+ST097Q04TA+ ST097Q05TA) %>%  
head(2)
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
mutate(toplam=rowSums(select(., ST097Q01TA:ST097Q05TA)),
       .before= ST097Q01TA)%>%
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
zevk <- midiPISA %>%
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
table(midiPISA$SINIF)
```

```
## 
##    7    8    9   10   11   12 
##    3   19 1295 5360  207    6
```

- **SNF** değişkenini kullanarak ortaokul ve lise olmak üzere iki düzeyli **OKUL** adlı bir değişken oluşturalım.




```r
midiPISA %>%
  select(1:5) %>%
  mutate(okul = ifelse(SINIF  == 7 | SINIF  == 8,
                       "Ortaokul", "Lise")) %>%
    head(3)
```

<div class="kable-table">

| OGRENCIID| SINIF| CINSIYET| Anne_Egitim| Baba_Egitim|okul |
|---------:|-----:|--------:|-----------:|-----------:|:----|
|  79200768|    10|        2|           2|           2|Lise |
|  79201064|    10|        2|           2|           2|Lise |
|  79201118|    10|        1|           1|           2|Lise |

</div>


## case_when()

- **case_when()** fonksiyonu çoklu **ifelse() ** kullanımı ile benzer işlevi sağlar.

- **case_when()** birden fazla koşula dayalı karşılaştırmalarda yeni bir değişken oluşturmak amacıyla kullanılır.

- O_OD_1 düzeye ilişikin betimsel istatistikler

```r
summary(midiPISA$ODOKUMA1)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   175.6   402.6   463.4   464.2   525.7   771.5
```


- ODOKUMA1 değişkeninin kategorik hale getirilmesi


```r
v1 <- midiPISA %>%
  mutate(ODOKUMA1_kat =
    case_when(
      ODOKUMA1 <=  402.6  ~ "dusuk",
      ODOKUMA1 > 402.6  & ODOKUMA1 <  525.7 ~ "orta",
      ODOKUMA1 >=525.7 ~ "yuksek" )) %>%
      select(ODOKUMA1,ODOKUMA1_kat)
```


- Olusturulan yeni ODOKUMA1_kat degişkeninin veri setinde nasıl dağıldığını inceleme



```r
v1 %>% group_by(ODOKUMA1_kat) %>% summarize(f=n())
```

<div class="kable-table">

|ODOKUMA1_kat |    f|
|:------------|----:|
|dusuk        | 1724|
|orta         | 3443|
|yuksek       | 1723|

</div>


teşekkürler !


- [Siz de yapın](https://learnr-examples.shinyapps.io/ex-data-filter/#section-welcome>)

- [Siz de yapın](https://learnr-examples.shinyapps.io/ex-data-summarise/)
--


