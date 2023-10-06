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

<div class="kable-table">

|    n|
|----:|
| 6890|

</div>

- Cinsiyete göre dağılım
👦 👧

```r
PISA_STU_2018 %>% count(ST004D01T)
```

<div class="kable-table">

| ST004D01T|    n|
|---------:|----:|
|         1| 3396|
|         2| 3494|

</div>

- Cinsiyete göre dağılım - **sort** argümanı ile sıralanabilir.
👦 👧


```r
PISA_STU_2018 %>% count(ST004D01T,sort=TRUE)
```

<div class="kable-table">

| ST004D01T|    n|
|---------:|----:|
|         2| 3494|
|         1| 3396|

</div>

- PISA_OGR_2018 öğrenci verisindeki değişken adlarının türkçeleştirilmiş halidir.

- Bu veri setini kullanarak öğrencilerin göçmenlik durumları ve cinsiyetlere göre dağılımını inceleyelim.


```r
PISA_OGR_2018 %>% count(CINSIYET,Gocmenlik)
```

<div class="kable-table">

| CINSIYET| Gocmenlik|    n|
|--------:|---------:|----:|
|        1|         1| 3306|
|        1|         2|   17|
|        1|         3|   10|
|        1|        NA|   63|
|        2|         1| 3357|
|        2|         2|   20|
|        2|         3|    7|
|        2|        NA|  110|

</div>


- `PISA_OGR_2018 %>% count(CINSIYET,Gocmenlik) %>% ...` birey sayısını büyükten küçüğe sıralayınız. 
<input class='webex-solveme nospaces' size='11' data-answer='["arrange(-n)"]'/>

<div class="kable-table">

| CINSIYET| Gocmenlik|    n|
|--------:|---------:|----:|
|        2|         1| 3357|
|        1|         1| 3306|
|        2|        NA|  110|
|        1|        NA|   63|
|        2|         2|   20|
|        1|         2|   17|
|        1|         3|   10|
|        2|         3|    7|

</div>



```r
PISA_OGR_2018 %>% count(SINIF, sort=TRUE)
```

<div class="kable-table">

| SINIF|    n|
|-----:|----:|
|    10| 5360|
|     9| 1295|
|    11|  207|
|     8|   19|
|    12|    6|
|     7|    3|

</div>

- `PISA_OGR_2018 %>% count(.....)` siz de  SINIF ve CINSIYET'e göre dağılımı bulunuz? <input class='webex-solveme nospaces' size='24' data-answer='["CINSIYET,SINIF,sort=TRUE"]'/>

<div class="kable-table">

| CINSIYET| SINIF|    n|
|--------:|-----:|----:|
|        1|    10| 2707|
|        2|    10| 2653|
|        2|     9|  747|
|        1|     9|  548|
|        1|    11|  124|
|        2|    11|   83|
|        1|     8|   11|
|        2|     8|    8|
|        1|    12|    5|
|        2|     7|    2|
|        1|     7|    1|
|        2|    12|    1|

</div>

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

<div class="kable-table">

| mean(ODOKUMA1)|
|--------------:|
|       464.2299|

</div>

- **summarise()** fonksiyonu içinde isimlendirme yapmazsanız, oluşan veri setinde isimlendirme fonksiyon adı/ları olacaktır.

- isimlendirilmiş çıktı


```r
PISA_OGR_2018 %>%
  summarise(ortalama=mean(ODOKUMA1))
```

<div class="kable-table">

| ortalama|
|--------:|
| 464.2299|

</div>


- Özet bilgiler elde etmek için birden fazla özetleyici fonksiyon kullanabilirsiniz.


```r
PISA_OGR_2018 %>%
  summarise(n = n(),
            ortalama=mean(ODOKUMA1),
            sd=sd(ODOKUMA1),
            min=min(ODOKUMA1),
            max=max(ODOKUMA1))
```

<div class="kable-table">

|    n| ortalama|       sd|     min|     max|
|----:|--------:|--------:|-------:|-------:|
| 6890| 464.2299| 87.78006| 175.608| 771.508|

</div>



- Özet bilgileri veri setinde yer alan alt gruplar için ise ayrı ayrı **group_by()** fonksiyonu ile hesaplayabilirsiniz.

- **group_by()** dan sonra kullanılan fonksiyonlar her grup için hesaplanır. Fonksiyonu içinde sürekli değişken **kullanılmaz.**

- Cinsiyete göre ODOKUMA1 puanlarına ilişkin istatistikler

```r
PISA_OGR_2018 %>%
  group_by(CINSIYET) %>%
  summarise(n = n(),ortalama=mean(ODOKUMA1),sd=sd(ODOKUMA1),min=min(ODOKUMA1),max=max(ODOKUMA1))
```

<div class="kable-table">

| CINSIYET|    n| ortalama|       sd|     min|     max|
|--------:|----:|--------:|--------:|-------:|-------:|
|        1| 3396| 478.1378| 83.65322| 236.389| 771.508|
|        2| 3494| 450.7121| 89.57864| 175.608| 747.491|

</div>


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

<div class="kable-table">

| CINSIYET| SINIF|    n| ortalama|       sd|
|--------:|-----:|----:|--------:|--------:|
|        1|    10| 2707| 482.2966| 79.87708|
|        1|    11|  124| 472.6618| 84.95710|
|        1|     9|  548| 462.0539| 96.90558|
|        2|    10| 2653| 459.2322| 85.00155|
|        2|    11|   83| 447.9737| 87.87190|
|        2|     9|  747| 422.1915| 98.74913|
|        1|    12|    5| 421.8288| 96.60689|
|        2|     8|    8| 362.9183| 82.82819|
|        1|     8|   11| 355.5180| 62.47101|
|        1|     7|    1| 343.5010|       NA|
|        2|     7|    2| 330.3725| 62.13135|
|        2|    12|    1| 322.0710|       NA|

</div>



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

<div class="kable-table">

| CINSIYET| SINIF|    n| ortalama|       sd|
|--------:|-----:|----:|--------:|--------:|
|        1|    10| 2707| 482.2966| 79.87708|
|        1|    11|  124| 472.6618| 84.95710|
|        1|     9|  548| 462.0539| 96.90558|
|        2|    10| 2653| 459.2322| 85.00155|
|        2|    11|   83| 447.9737| 87.87190|
|        2|     9|  747| 422.1915| 98.74913|
|        1|    12|    5| 421.8288| 96.60689|
|        2|     8|    8| 362.9183| 82.82819|
|        1|     8|   11| 355.5180| 62.47101|
|        1|     7|    1| 343.5010|       NA|
|        2|     7|    2| 330.3725| 62.13135|
|        2|    12|    1| 322.0710|       NA|

</div>


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

<div class="kable-table">

| ODOKUMA1_mean| ODFEN1_mean| ODOKUMA1_sd| ODFEN1_sd|
|-------------:|-----------:|-----------:|---------:|
|      464.2299|    467.4865|    87.78006|  83.11351|

</div>


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

<div class="kable-table">

| CINSIYET_mean| Gocmenlik_mean| ODOKUMA1_mean| CINSIYET_sd| Gocmenlik_sd| ODOKUMA1_sd|
|-------------:|--------------:|-------------:|-----------:|------------:|-----------:|
|      1.507112|             NA|      464.2299|   0.4999857|           NA|    87.78006|

</div>


## top_n()

- **top_n()** fonksiyonu ile istediğiniz bir değişkenin **en yüksek** ya da **en düşük** değerlerine  göre verisetinde seçim yapılabilir.


```r
df <- data.frame(x = c(10, 4, 1, 6, 3, 1, 1))
df %>% top_n(2)
```

```
## Selecting by x
```

<div class="kable-table">

|  x|
|--:|
| 10|
|  6|

</div>



- Okuma puanı **en yüksek** olan üç kız ve üç erkek öğrencinin bilgileri

```r
PISA_OGR_2018 %>%
  select(CINSIYET,ODOKUMA1)%>% 
  arrange(desc(ODOKUMA1))%>% 
  group_by(CINSIYET) %>% 
  top_n(3,ODOKUMA1)
```

<div class="kable-table">

| CINSIYET| ODOKUMA1|
|--------:|--------:|
|        1|  771.508|
|        1|  748.371|
|        2|  747.491|
|        1|  742.969|
|        2|  737.448|
|        2|  713.531|

</div>


## top_n() & - operatoru

- Okuma puanı **en düşük** olan üç kız ve beş erkek öğrencinin bilgileri


```r
PISA_OGR_2018 %>%
  select(CINSIYET,ODOKUMA1)%>% 
  arrange(desc(ODOKUMA1))%>% 
  group_by(CINSIYET) %>% 
  top_n(-3,ODOKUMA1)
```

<div class="kable-table">

| CINSIYET| ODOKUMA1|
|--------:|--------:|
|        1|  249.789|
|        1|  241.820|
|        1|  236.389|
|        2|  198.944|
|        2|  176.962|
|        2|  175.608|

</div>



## DataEditR paketi

Bu paketi paketin [github sayfasından](https://github.com/DillonHammill/DataEditR) inceleyelim.



teşekkürler !




🍵

