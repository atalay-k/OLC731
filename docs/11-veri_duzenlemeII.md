# Veri duzenleme  - II

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
midiPISA %>% count()
```

<div class="kable-table">

|    n|
|----:|
| 6890|

</div>

- Cinsiyete göre dağılım
👦 👧

```r
midiPISA %>% count(CINSIYET)
```

<div class="kable-table">

|CINSIYET |    n|
|:--------|----:|
|Kiz      | 3396|
|Erkek    | 3494|

</div>

- Cinsiyete göre dağılım - **sort** argümanı ile sıralanabilir.
👦 👧


```r
midiPISA %>% count(CINSIYET,sort=TRUE)
```

<div class="kable-table">

|CINSIYET |    n|
|:--------|----:|
|Erkek    | 3494|
|Kiz      | 3396|

</div>

- midiPISA öğrenci verisindeki değişken adlarının türkçeleştirilmiş halidir.

- Bu veri setini kullanarak öğrencilerin sınıf düzeyleri ve cinsiyetlere göre dağılımını inceleyelim.


```r
midiPISA %>% count(CINSIYET,SINIF)
```

<div class="kable-table">

|CINSIYET |SINIF    |    n|
|:--------|:--------|----:|
|Kiz      |SINIF 7  |    1|
|Kiz      |SINIF 8  |   11|
|Kiz      |SINIF 9  |  548|
|Kiz      |SINIF 10 | 2707|
|Kiz      |SINIF 11 |  124|
|Kiz      |SINIF 12 |    5|
|Erkek    |SINIF 7  |    2|
|Erkek    |SINIF 8  |    8|
|Erkek    |SINIF 9  |  747|
|Erkek    |SINIF 10 | 2653|
|Erkek    |SINIF 11 |   83|
|Erkek    |SINIF 12 |    1|

</div>


- `midiPISA %>% count(CINSIYET,SINIF) %>% ...` birey sayısını büyükten küçüğe sıralayınız. 
<input class='webex-solveme nospaces' size='11' data-answer='["arrange(-n)"]'/>

<div class="kable-table">

|CINSIYET |SINIF    |    n|
|:--------|:--------|----:|
|Kiz      |SINIF 10 | 2707|
|Erkek    |SINIF 10 | 2653|
|Erkek    |SINIF 9  |  747|
|Kiz      |SINIF 9  |  548|
|Kiz      |SINIF 11 |  124|
|Erkek    |SINIF 11 |   83|
|Kiz      |SINIF 8  |   11|
|Erkek    |SINIF 8  |    8|
|Kiz      |SINIF 12 |    5|
|Erkek    |SINIF 7  |    2|
|Kiz      |SINIF 7  |    1|
|Erkek    |SINIF 12 |    1|

</div>



```r
midiPISA %>% count(SINIF, sort=TRUE)
```

<div class="kable-table">

|SINIF    |    n|
|:--------|----:|
|SINIF 10 | 5360|
|SINIF 9  | 1295|
|SINIF 11 |  207|
|SINIF 8  |   19|
|SINIF 12 |    6|
|SINIF 7  |    3|

</div>

- `midiPISA %>% count(.....)` siz de  SINIF ve CINSIYET'e göre dağılımı bulunuz? <input class='webex-solveme nospaces' size='24' data-answer='["SINIF,CINSIYET,sort=TRUE"]'/>

<div class="kable-table">

|SINIF    |CINSIYET |    n|
|:--------|:--------|----:|
|SINIF 10 |Kiz      | 2707|
|SINIF 10 |Erkek    | 2653|
|SINIF 9  |Erkek    |  747|
|SINIF 9  |Kiz      |  548|
|SINIF 11 |Kiz      |  124|
|SINIF 11 |Erkek    |   83|
|SINIF 8  |Kiz      |   11|
|SINIF 8  |Erkek    |    8|
|SINIF 12 |Kiz      |    5|
|SINIF 7  |Erkek    |    2|
|SINIF 7  |Kiz      |    1|
|SINIF 12 |Erkek    |    1|

</div>

- **count()** fonksiyonunun yardım sayfasını inceleyiniz **wt** argümanını ne amaçala kullanılmıştır açıklayınız. 




## summarise() fonksiyonları

- **summarise()** seçilen sütunlar için her satırı kullanarak istatistikler hesaplar.

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
midiPISA %>% 
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
midiPISA %>%
  summarise(ortalama=mean(ODOKUMA1))
```

<div class="kable-table">

| ortalama|
|--------:|
| 464.2299|

</div>


- Özet bilgiler elde etmek için birden fazla özetleyici fonksiyon kullanabilirsiniz.


```r
midiPISA %>%
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
midiPISA %>%
  group_by(CINSIYET) %>%
  summarise(n = n(),
            ortalama=mean(ODOKUMA1),
            sd=sd(ODOKUMA1),
            min=min(ODOKUMA1),
            max=max(ODOKUMA1))
```

<div class="kable-table">

|CINSIYET |    n| ortalama|       sd|     min|     max|
|:--------|----:|--------:|--------:|-------:|-------:|
|Kiz      | 3396| 478.1378| 83.65322| 236.389| 771.508|
|Erkek    | 3494| 450.7121| 89.57864| 175.608| 747.491|

</div>


- siz de bu işlemi göçmenlik statüsüne göre  yapınız.


- Özet bilgileri veri setinde yer alan birden fazla kategorik değişken içinde hesaplayabilirsiniz.

- Öğrencilerin cinsiyet ve sınıf düzeylerine göre elde edilen betimsel istatistikleri ortalamaya göre sıralandırılmıştır.


```r
betimsel  <- midiPISA %>%
  group_by(CINSIYET,SINIF) %>%
  summarise(n = n(),ortalama=mean(ODOKUMA1),sd=sd(ODOKUMA1)) %>%  
  arrange(desc(ortalama)) 

betimsel
```

<div class="kable-table">

|CINSIYET |SINIF    |    n| ortalama|       sd|
|:--------|:--------|----:|--------:|--------:|
|Kiz      |SINIF 10 | 2707| 482.2966| 79.87708|
|Kiz      |SINIF 11 |  124| 472.6618| 84.95710|
|Kiz      |SINIF 9  |  548| 462.0539| 96.90558|
|Erkek    |SINIF 10 | 2653| 459.2322| 85.00155|
|Erkek    |SINIF 11 |   83| 447.9737| 87.87190|
|Erkek    |SINIF 9  |  747| 422.1915| 98.74913|
|Kiz      |SINIF 12 |    5| 421.8288| 96.60689|
|Erkek    |SINIF 8  |    8| 362.9183| 82.82819|
|Kiz      |SINIF 8  |   11| 355.5180| 62.47101|
|Kiz      |SINIF 7  |    1| 343.5010|       NA|
|Erkek    |SINIF 7  |    2| 330.3725| 62.13135|
|Erkek    |SINIF 12 |    1| 322.0710|       NA|

</div>



- **group_by()** fonksiyonu ile elde ettiğiniz çıktılarda aşağıdaki gibi 
gruplandırılmış veri **Groups**  çıktısı ile alınır.


```r
# A tibble: 12 x 5
# Groups:   CNSYT [2]
```



- Gruplandırılmış elde edilen veri setlerinde tekrar işlem yapmak istiyorsanız bunu **ungroup()** fonksiyonu ile yapabilirsiniz.


```r
midiPISA %>%
  group_by(CINSIYET,SINIF) %>%
  summarise(n = n(),
            ortalama=mean(ODOKUMA1),
            sd=sd(ODOKUMA1)) %>%
  arrange(desc(ortalama)) %>% 
  ungroup()
```

<div class="kable-table">

|CINSIYET |SINIF    |    n| ortalama|       sd|
|:--------|:--------|----:|--------:|--------:|
|Kiz      |SINIF 10 | 2707| 482.2966| 79.87708|
|Kiz      |SINIF 11 |  124| 472.6618| 84.95710|
|Kiz      |SINIF 9  |  548| 462.0539| 96.90558|
|Erkek    |SINIF 10 | 2653| 459.2322| 85.00155|
|Erkek    |SINIF 11 |   83| 447.9737| 87.87190|
|Erkek    |SINIF 9  |  747| 422.1915| 98.74913|
|Kiz      |SINIF 12 |    5| 421.8288| 96.60689|
|Erkek    |SINIF 8  |    8| 362.9183| 82.82819|
|Kiz      |SINIF 8  |   11| 355.5180| 62.47101|
|Kiz      |SINIF 7  |    1| 343.5010|       NA|
|Erkek    |SINIF 7  |    2| 330.3725| 62.13135|
|Erkek    |SINIF 12 |    1| 322.0710|       NA|

</div>

## across()

Bir veri setinde aynı anda birden fazla sütuna aynı işlem uygulanmak istendiğinde dplyr paketi içindeki `across()` fonksiyonu sıklıkla kullanılmaktadır. Bu fonksiyon veri düzenleme ile ilgili birçok temel fonksiyon içinde düzgün çalışabilmektedir. Fakat genellikle `select()`, `mutate()`, `filter()` veya `summarise()` içinde kullanılır.

cols = argümanına sütunlar ve .fns = argümanına uygulanacak fonksiyonlar atanır.

midiPISA verisinde okuma puanı olası değer 1 ve 2 sütunlarına ait ortalama değerleri `across()` fonksiyonu ile hesaplayalım.


```r
midiPISA %>%
     summarise(across(.cols=c(ODOKUMA1,ODOKUMA2),.fns=mean, .names = "{col}_mean"))
```

<div class="kable-table">

| ODOKUMA1_mean| ODOKUMA2_mean|
|-------------:|-------------:|
|      464.2299|      464.4204|

</div>

ODOKUMA1 ve ODOKUMA2 sütunlarına ait ortalamalar hesaplanmış ve bu ortalama değerlerini veren sütunlar .names = "{col}\_mean" ile isimlendirilmiştir.

Birden fazla istatistiksel bilgi hesaplanmak istendiğinde list() argümanı kullanılabilir. "OD" ile başlayan sütunlara ait ortalama ve standart sapma değerlerini hesaplayalım.


```r
midiPISA %>%
       summarise(across(.cols=starts_with("OD"), .fns=list(mean = mean, sd = sd)))
```

<div class="kable-table">

| ODOKUMA1_mean| ODOKUMA1_sd| ODOKUMA2_mean| ODOKUMA2_sd| ODOKUMA3_mean| ODOKUMA3_sd| ODOKUMA4_mean| ODOKUMA4_sd| ODOKUMA5_mean| ODOKUMA5_sd|
|-------------:|-----------:|-------------:|-----------:|-------------:|-----------:|-------------:|-----------:|-------------:|-----------:|
|      464.2299|    87.78006|      464.4204|      87.696|      464.7147|    87.07692|      464.6129|    87.40305|      464.1982|    87.21323|

</div>


## summarise() and across()

dplyr paket fonksiyonlarının \*\*\_at,\_if,\_all\*\* uzantılı varyasyonları bulunmaktadır. Bunlardan biri olan `summarise_at()` fonksiyonunu bir grup sütunun ortalamasını ve standart sapmasını hesaplamak gerektiğinde kullanabilirsiniz. `summarise_at()` fonksiyonu ile seçilecek değişkenler `vars()` fonksiyonu içinde belirtilebilir. Bu işlem `select()` işlemi yerine geçmektedir. Hesaplama işlemlerini ise `list()` fonksiyonu içinde tanımlayabilirsiniz.


```r
midiPISA %>%
    summarise_at(vars(ODOKUMA1, ODOKUMA2), list(~mean(.), ~sd(.)))
```

<div class="kable-table">

| ODOKUMA1_mean| ODOKUMA2_mean| ODOKUMA1_sd| ODOKUMA2_sd|
|-------------:|-------------:|-----------:|-----------:|
|      464.2299|      464.4204|    87.78006|      87.696|

</div>

`summarise_at()` fonksiyonu kullanılmak istenildiğinde kullanımdan kaldırılmış olduğu (deprecated) uyarısı görünür. Bir fonksiyonun daha iyi bir alternatifi mevcut ise kullanımdan kaldırılabilir. Daha önce de bahsedilen `across()` fonksiyonu değişken seçmek için yukarıdaki örnekte `vars()` fonksiyonu yerine aşağıdaki şekilde kullanılabilir. Bu sayede `summarise_at()` fonksiyonu yerine `summarise()` fonksiyonu kullanılmış olur.


```r
midiPISA %>%
  summarise(
    across(c(ODOKUMA1, ODOKUMA2), list(mean = ~mean(.), sd = ~sd(.)))
  )
```

<div class="kable-table">

| ODOKUMA1_mean| ODOKUMA1_sd| ODOKUMA2_mean| ODOKUMA2_sd|
|-------------:|-----------:|-------------:|-----------:|
|      464.2299|    87.78006|      464.4204|      87.696|

</div>


Elinizdeki bir veri setinin sayısal (numeric) olan sütunlarının ortalamasını `summarise_if()` fonksiyonu ile hesaplayabilirsiniz. Bu hesaplamanın  `summarise()` ve `across()` fonksiyonu ile nasıl yapıldığı gösterilmiştir.


```r
midiPISA %>%
  summarise(across(where(is.numeric), list(mean = mean, sd = sd), na.rm = TRUE))
```

<div class="kable-table">

| OGRENCIID_mean| OGRENCIID_sd| OKUMA_ZEVK_mean| OKUMA_ZEVK_sd| ODOKUMA1_mean| ODOKUMA1_sd| ODOKUMA2_mean| ODOKUMA2_sd| ODOKUMA3_mean| ODOKUMA3_sd| ODOKUMA4_mean| ODOKUMA4_sd| ODOKUMA5_mean| ODOKUMA5_sd|
|--------------:|------------:|---------------:|-------------:|-------------:|-----------:|-------------:|-----------:|-------------:|-----------:|-------------:|-----------:|-------------:|-----------:|
|       79203623|      2086.54|       0.6831396|     0.9756913|      464.2299|    87.78006|      464.4204|      87.696|      464.7147|    87.07692|      464.6129|    87.40305|      464.1982|    87.21323|

</div>

Mevcut kodunuzu _if, _at veya _all işlevleri yerine across() işlevini kullanacak şekilde güncellemek istiyorsanız `summarise_at()`, `summarise_all()` ve `summarise_if()` fonksiyonlarının yerini **`summarise()`** fonksiyonu içinde de kullanılabilen **`across()`** yardımcı fonksiyonunu kullanabilirsiniz.


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
midiPISA %>%
  select(CINSIYET,ODOKUMA1)%>% 
  arrange(desc(ODOKUMA1))%>% 
  group_by(CINSIYET) %>% 
  top_n(3,ODOKUMA1)
```

<div class="kable-table">

|CINSIYET | ODOKUMA1|
|:--------|--------:|
|Kiz      |  771.508|
|Kiz      |  748.371|
|Erkek    |  747.491|
|Kiz      |  742.969|
|Erkek    |  737.448|
|Erkek    |  713.531|

</div>

## top_n() & - operatoru

- Okuma puanı **en düşük** olan üç kız ve beş erkek öğrencinin bilgileri


```r
midiPISA %>%
  select(CINSIYET,ODOKUMA1)%>% 
  arrange(desc(ODOKUMA1))%>% 
  group_by(CINSIYET) %>% 
  top_n(-3,ODOKUMA1)
```

<div class="kable-table">

|CINSIYET | ODOKUMA1|
|:--------|--------:|
|Kiz      |  249.789|
|Kiz      |  241.820|
|Kiz      |  236.389|
|Erkek    |  198.944|
|Erkek    |  176.962|
|Erkek    |  175.608|

</div>



teşekkürler !




🍵

