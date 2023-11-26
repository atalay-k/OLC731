# Veri duzenleme  - II

- Bu bölümde pratiklik ve anlaşılabilirlik açısında **miniPISA** verisini kullanacağız. Bunun için öncelikle _import_ adlı klasöre indirilen veri setini aşağıdaki komut ile R ortamına yüklenmelidir. 

- 🔗 [miniPISA.rda](import/miniPISA.rda)


```r
load("import/miniPISA.rda") # çalışılacak veri setinin data adlı klasörden R ortamına yüklenmesi
```

- miniPISA veri seti;  öğrenci ıd(OGR_ID), sınıf(SNF), cinsiyet(CNSYT), anne eğitim düzeyi(AED), baba eğitim düzeyi(BED), okumaktan zevk alma(O_ZEVK), ST097Q01TA, ST097Q02TA, ST097Q03TA, ST097Q04TA, ST097Q05TA, okuma olası değer 1 (O_OD1), okuma olası değer 2 (O_OD2), okuma olası değer 3 (O_OD3), okuma olası değer 4 (O_OD4), okuma olası değer 5 (O_OD5) değişkenleri olmak üzere toplam 16 değişkenden oluşmaktadır.



- Veriyi üst düzeyde toplama amacıyla aşağıdaki fonksiyonlar kullanılabilir.


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
load("import/miniPISA.rda") # ogrenci verisi
miniPISA %>% count()
```

<div class="kable-table">

|    n|
|----:|
| 6890|

</div>

- Cinsiyete göre dağılım
👦 👧

```r
miniPISA %>% count(CNSYT)
```

<div class="kable-table">

| CNSYT|    n|
|-----:|----:|
|     1| 3396|
|     2| 3494|

</div>

- Cinsiyete göre dağılım - **sort** argümanı ile sıralanabilir.
👦 👧


```r
miniPISA %>% count(CNSYT,sort=TRUE)
```

<div class="kable-table">

| CNSYT|    n|
|-----:|----:|
|     2| 3494|
|     1| 3396|

</div>

- miniPISA öğrenci verisindeki değişken adlarının türkçeleştirilmiş halidir.

- Bu veri setini kullanarak öğrencilerin sınıf düzeyleri ve cinsiyetlere göre dağılımını inceleyelim.


```r
miniPISA %>% count(CNSYT,SNF)
```

<div class="kable-table">

| CNSYT| SNF|    n|
|-----:|---:|----:|
|     1|   7|    1|
|     1|   8|   11|
|     1|   9|  548|
|     1|  10| 2707|
|     1|  11|  124|
|     1|  12|    5|
|     2|   7|    2|
|     2|   8|    8|
|     2|   9|  747|
|     2|  10| 2653|
|     2|  11|   83|
|     2|  12|    1|

</div>


- `miniPISA %>% count(CNSYT,SNF) %>% ...` birey sayısını büyükten küçüğe sıralayınız. 
<input class='webex-solveme nospaces' size='11' data-answer='["arrange(-n)"]'/>

<div class="kable-table">

| CNSYT| SNF|    n|
|-----:|---:|----:|
|     1|  10| 2707|
|     2|  10| 2653|
|     2|   9|  747|
|     1|   9|  548|
|     1|  11|  124|
|     2|  11|   83|
|     1|   8|   11|
|     2|   8|    8|
|     1|  12|    5|
|     2|   7|    2|
|     1|   7|    1|
|     2|  12|    1|

</div>



```r
miniPISA %>% count(SNF, sort=TRUE)
```

<div class="kable-table">

| SNF|    n|
|---:|----:|
|  10| 5360|
|   9| 1295|
|  11|  207|
|   8|   19|
|  12|    6|
|   7|    3|

</div>

- `miniPISA %>% count(.....)` siz de  SNF ve CNSYT'e göre dağılımı bulunuz? <input class='webex-solveme nospaces' size='19' data-answer='["CNSYT,SNF,sort=TRUE"]'/>

<div class="kable-table">

| SNF| CNSYT|    n|
|---:|-----:|----:|
|  10|     1| 2707|
|  10|     2| 2653|
|   9|     2|  747|
|   9|     1|  548|
|  11|     1|  124|
|  11|     2|   83|
|   8|     1|   11|
|   8|     2|    8|
|  12|     1|    5|
|   7|     2|    2|
|   7|     1|    1|
|  12|     2|    1|

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
  
- PISA veri setinde başarısı için  hesaplanan 10 olası puan değerinden (plausible value) ilki kullanılmıştır. 


```r
miniPISA %>% 
summarise(mean(O_OD1))
```

<div class="kable-table">

| mean(O_OD1)|
|-----------:|
|    464.2304|

</div>

- **summarise()** fonksiyonu içinde isimlendirme yapmazsanız, oluşan veri setinde isimlendirme fonksiyon adı/ları olacaktır.

- isimlendirilmiş çıktı


```r
miniPISA %>%
  summarise(ortalama=mean(O_OD1))
```

<div class="kable-table">

| ortalama|
|--------:|
| 464.2304|

</div>


- Özet bilgiler elde etmek için birden fazla özetleyici fonksiyon kullanabilirsiniz.


```r
miniPISA %>%
  summarise(n = n(),
            ortalama=mean(O_OD1),
            sd=sd(O_OD1),
            min=min(O_OD1),
            max=max(O_OD1))
```

<div class="kable-table">

|    n| ortalama|       sd|    min|    max|
|----:|--------:|--------:|------:|------:|
| 6890| 464.2304| 87.78009| 175.61| 771.51|

</div>



- Özet bilgileri veri setinde yer alan alt gruplar için ise ayrı ayrı **group_by()** fonksiyonu ile hesaplayabilirsiniz.

- **group_by()** dan sonra kullanılan fonksiyonlar her grup için hesaplanır. Fonksiyonu içinde sürekli değişken **kullanılmaz.**

- Cinsiyete göre ODOKUMA1 puanlarına ilişkin istatistikler

```r
miniPISA %>%
  group_by(CNSYT) %>%
  summarise(n = n(),
            ortalama=mean(O_OD1),
            sd=sd(O_OD1),
            min=min(O_OD1),
            max=max(O_OD1))
```

<div class="kable-table">

| CNSYT|    n| ortalama|       sd|    min|    max|
|-----:|----:|--------:|--------:|------:|------:|
|     1| 3396| 478.1383| 83.65325| 236.39| 771.51|
|     2| 3494| 450.7126| 89.57867| 175.61| 747.49|

</div>


- siz de bu işlemi göçmenlik statüsüne göre  yapınız.


- Özet bilgileri veri setinde yer alan birden fazla kategorik değişken içinde hesaplayabilirsiniz.

- Öğrencilerin cinsiyet ve sınıf düzeylerine göre elde edilen betimsel istatistikleri ortalamaya göre sıralandırılmıştır.


```r
betimsel  <- miniPISA %>%
  group_by(CNSYT,SNF) %>%
  summarise(n = n(),ortalama=mean(O_OD1),sd=sd(O_OD1)) %>%  
  arrange(desc(ortalama)) 

betimsel
```

<div class="kable-table">

| CNSYT| SNF|    n| ortalama|       sd|
|-----:|---:|----:|--------:|--------:|
|     1|  10| 2707| 482.2971| 79.87712|
|     1|  11|  124| 472.6626| 84.95732|
|     1|   9|  548| 462.0543| 96.90557|
|     2|  10| 2653| 459.2327| 85.00162|
|     2|  11|   83| 447.9740| 87.87190|
|     2|   9|  747| 422.1921| 98.74911|
|     1|  12|    5| 421.8300| 96.60434|
|     2|   8|    8| 362.9175| 82.82710|
|     1|   8|   11| 355.5200| 62.47043|
|     1|   7|    1| 343.5000|       NA|
|     2|   7|    2| 330.3750| 62.13347|
|     2|  12|    1| 322.0700|       NA|

</div>



- **group_by()** fonksiyonu ile elde ettiğiniz çıktılarda aşağıdaki gibi 
gruplandırılmış veri **Groups**  çıktısı ile alınır.


```r
# A tibble: 12 x 5
# Groups:   CNSYT [2]
```



- Gruplandırılmış elde edilen veri setlerinde tekrar işlem yapmak istiyorsanız bunu **ungroup()** fonksiyonu ile yapabilirsiniz.


```r
miniPISA %>%
  group_by(CNSYT,SNF) %>%
  summarise(n = n(),
            ortalama=mean(O_OD1),
            sd=sd(O_OD1)) %>%
  arrange(desc(ortalama)) %>% 
  ungroup()
```

<div class="kable-table">

| CNSYT| SNF|    n| ortalama|       sd|
|-----:|---:|----:|--------:|--------:|
|     1|  10| 2707| 482.2971| 79.87712|
|     1|  11|  124| 472.6626| 84.95732|
|     1|   9|  548| 462.0543| 96.90557|
|     2|  10| 2653| 459.2327| 85.00162|
|     2|  11|   83| 447.9740| 87.87190|
|     2|   9|  747| 422.1921| 98.74911|
|     1|  12|    5| 421.8300| 96.60434|
|     2|   8|    8| 362.9175| 82.82710|
|     1|   8|   11| 355.5200| 62.47043|
|     1|   7|    1| 343.5000|       NA|
|     2|   7|    2| 330.3750| 62.13347|
|     2|  12|    1| 322.0700|       NA|

</div>


### summarize_at()

- dplyr paket fonksiyonlarının **_at,_if,_all** uzantılı varyasyonları bulunmaktadır.

- Sadece bir grup sütunun ortalamasını ve standart sapmasını hesaplamanız gerektiğinde **summarize_at()** fonksiyonunu kullanabilirsiniz.


- **summarize_at()** fonksiyonu ile seçilecek değişkenler **vars()**
fonksiyonu içinde belirtilebilir. Bu işlem **select** işlemi yerine geçmektedir.

- Hesaplama işlemlerini ise **list()** fonksiyonu içinde tanımlayabilirsiniz.


```r
# adlandırmaya dikkat edin!
miniPISA %>%
    summarize_at(vars(O_OD1, O_ZEVK), list(~mean(.), ~sd(.)))
```

<div class="kable-table">

| O_OD1_mean| O_ZEVK_mean| O_OD1_sd| O_ZEVK_sd|
|----------:|-----------:|--------:|---------:|
|   464.2304|          NA| 87.78009|        NA|

</div>
- eksik veriler olduğu için çıktıda NA görünüyor!

### summarize_all() ve summarize_if()

- Elinizde tüm sütunları sayısal (numeric) olan bir veri seti olsun. Tüm sütunların ortalamasını **summarize_all()** fonksiyonu ile hesaplayabilirsiniz.


```r
veriseti %>% summarize_all(funs(mean, sd))
```

- Elinizdeki bir veri setinin sayısal (numeric) olan sütunlarının ortalamasını **summarize_if()** fonksiyonu ile hesaplayabilirsiniz.


```r
expss::drop_var_labs(miniPISA) %>% 
    select(O_ZEVK,O_OD1) %>% 
    summarize_if(is.numeric, funs(mean, sd),na.rm=TRUE)
```

<div class="kable-table">

| O_ZEVK_mean| O_OD1_mean| O_ZEVK_sd| O_OD1_sd|
|-----------:|----------:|---------:|--------:|
|    0.682927|   464.2304| 0.9750422| 87.78009|

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
miniPISA %>%
  select(CNSYT,O_OD1)%>% 
  arrange(desc(O_OD1))%>% 
  group_by(CNSYT) %>% 
  top_n(3,O_OD1)
```

<div class="kable-table">

| CNSYT|  O_OD1|
|-----:|------:|
|     1| 771.51|
|     1| 748.37|
|     2| 747.49|
|     1| 742.97|
|     2| 737.45|
|     2| 713.53|

</div>


## top_n() & - operatoru

- Okuma puanı **en düşük** olan üç kız ve beş erkek öğrencinin bilgileri


```r
miniPISA %>%
  select(CNSYT,O_OD1)%>% 
  arrange(desc(O_OD1))%>% 
  group_by(CNSYT) %>% 
  top_n(-3,O_OD1)
```

<div class="kable-table">

| CNSYT|  O_OD1|
|-----:|------:|
|     1| 249.79|
|     1| 241.82|
|     1| 236.39|
|     2| 198.94|
|     2| 176.96|
|     2| 175.61|

</div>



teşekkürler !




🍵

