# Veri duzenleme




## dplyr paket tanıtımı 

-   Veri düzenlemede en sık kullanılan paketlerden biri **dplyr** paketidir.

-   Veri manipulasyonunun `grammeri` paketin tanıtımında kullanılmıştır. 
  
-  Paketin en sık kullanılan fonksiyonları ise

    - `select():`   istenilen değişkenlere gore yeni bir veri seti oluşturma
    
    - `mutate():`   yeni degişkenlerin veri setine eklenmesi
    <br>
    
    - `filter():`   istenilen gözlemlerle yeni bir veri oluşturma
    
    - `arrange():`  gözlemlerin seçilen degişkenlere göre yeniden sıralanması
    
    - `group_by():`  veride grup bazinda işlem yapma
    
    - `summarise():` veriden özet istatisikleri elde etme
    
    - `baglama (pipe)` `%>%` - işlemleri bağlama
    
    - `join()` - veri birleştirme


## Paket vignetteleri 📊

- 🔗 [From base R to dplyr](https://cran.r-project.org/web/packages/dplyr/vignettes/base.html)

-  🔗 [colwise](https://cran.r-project.org/web/packages/dplyr/vignettes/colwise.html)

- 🔗 [dplyr compatibility](https://cran.r-project.org/web/packages/dplyr/vignettes/compatibility.html)

- 🔗 [Introduction to dplyr](https://cran.r-project.org/web/packages/dplyr/vignettes/dplyr.html)

- 🔗 [Grouped data](https://cran.r-project.org/web/packages/dplyr/vignettes/grouping.html)

- 🔗 [Programming with dplyr](https://cran.r-project.org/web/packages/dplyr/vignettes/programming.html)

- 🔗 [rowwise](https://cran.r-project.org/web/packages/dplyr/vignettes/rowwise.html)

- 🔗  [Two-table verbs](https://cran.r-project.org/web/packages/dplyr/vignettes/two-table.html)

- 🔗  [Window functions](https://cran.r-project.org/web/packages/dplyr/vignettes/window-functions.html)


- 🔗 paketin cran sayfası  [link](https://cran.r-project.org/web/packages/dplyr/index.html)

-  🔗 paketin indirilme  istatistikleri [link](https://ipub.com/dev-corner/apps/r-package-downloads/)


## Uluslararası Eğitim Araştırmaları

### PISA

- Program for International Student Assessment-PISA (Uluslararası Öğrenci Değerlendirme Programı)

- 15 yaş grubundaki öğrencilerin matematik, fen ve okuma
becerilerindeki durumlarını belirlemeye yönelik bir çalışmadır.

- Ekonomik İşbirliği ve Kalkınma Örgütü (OECD) tarafından düzenlenir.



### TIMSS

- Trends in International Mathematics and Science Study (Uluslararası Matematik ve Fen Eğilimleri Araştırması)

- Öğrencilerin matematik ve fen alanlarında kazandıkları bilgi ve becerilerin değerlendirilmesine yönelik bir tarama araştırmasıdır. 

- Uluslararası Eğitim Başarılarını Değerlendirme Kuruluşu'nun bir projesidir.


## Veri Setleri

- 🔗 [PISA database](https://www.oecd.org/pisa/data/) <br>


- 🔗 [TIMSS 2019 database](https://timss2019.org/international-database/) 

- 🔗 [TIMSS 2015 database](https://timssandpirls.bc.edu/timss2015/international-database/) 
- 🔗 [TIMSS 2015 database](https://timssandpirls.bc.edu/timss2011/international-database.html)

## Uluslararası Sınavlarla İlgili R paketleri

### **instvy** paketi: International Assessment Data Manager 
- **intsvy** paketi (Caro ve Biecek, 2017) TIMSS, PIRLS, PISA ve ICILS gibi uluslararası değerlendirme çalışmalarının verilerini aktarma, birleştirme ve analiz etme amacıyla geliştirilmiştir. 

- **intsvy** paketindeki **pisa.select.merge()** fonksiyonuyla aşağıdaki komutlar kullanılarak istenilen ülke/ülkelerin istenilen değişkenlerine ilişkin veri seti oluşturulabilir.

- İlgili fonksiyon bir SPSS dosyası okuduğu için **.sav** uzantılı dosyaların okunmasında kullanılan **foreign**  paketi  sistemde yüklü olmalıdır. 


- Türkiye öğrenci anketi veri dosyasında yer alan sekiz ve Türkiye okul anketi veri dosyasında yer alan üç değişken seçilerek ve “pisa2015” nesnesi oluşturmuştur.


```r
library("intsvy")
library("foreign")
pisa2015 <- pisa.select.merge(folder="F:\\PISA", # folder=getwd()
student.file="CY6_MS_CMB_STU_QQQ.sav",
school.file="CY6_MS_CMB_SCH_QQQ.sav",
student=c("ST001D01T","ST004D01T","STRATUM","MISCED","FISCED","IMMIG","LANGN","ESCS",)
school=c("SCHSIZE","CLSIZE","STRATIO"),
  countries=c("TUR"))
```

Komutların çalısması uzun zaman alabilir. Büyük dosyaların okunması sırasında, dosya büyüklüğüne ve bilgisayar özelliklerine bağlı olarak, mevcut  **bellek (memory)** hata mesajı alınabilir.

### **EdSurvey** paketi

- PISA, TALIS, PIAAC, TIMSS, PIRLS, ICILS gibi sınavların veri setlerini indirmede, karmaşık veri setlerini **olası puanları** dikkate alarak analiz etmede kullanılan bir pakettir. 


```r
library(EdSurvey)
```

- Örnek olarak aşağıda yer alan kod 2012 yılı PISA veri setini, bilgisayarınızda istediğiniz yere indirecektir.


```r
downloadPISA(years = 2012, database = c("INT"), root=getwd())
```

- bu işlem de bilgisayar özelliklerine bağlı da olsa **zaman alan** bir işlemdir.


- Aşağıdaki kod sgp olarak kodlu olan Singapur ülkesine ilişkin verileri çeker.
 

```r
sgp2012 <- readPISA(path = "sunum/PISA/2012", database = "INT", countries = "sgp")
```

- bu işlem de bilgisayar özelliklerine bağlı da olsa zaman alan bir işlemdir.

- Bu tarz uzun süren işlemleri tekrarlamamak için, oluşan veriyi daha sonra R  ortamına kolayca aktarmak için **saveRDS()** fonkisyonu ile **.Rds**, **save()** ile **.Rdata** bir dosyaya kaydedebilirsiniz.

- Oluşan dosya tekrar R ortamına **readRDS()** ya da **load()** fonksiyonu ile aktarılabilir.

- Oluşan sgp2012 verisinden istediğiniz sütunları **getData()** fonksiyonu ile seçebilirsiniz.


```r
# okuma ve agirlandirma degiskenlerini gg nesnesine atama
gg <- EdSurvey::getData(sgp2012, c("cnt","read","w_fstuwt"))  
head(gg)
```


```r
edsurveyTable(read ~ st04q01 + st20q01, data = sgp2012)
```


### RALSA

- 🔗 [RALSA](http://ralsa.ineri.org/user-guide/)

- The R Analyzer for Large-Scale Assessments (RALSA)

```r
library(RALSA)
```


## Olası Değer

- 450 kişilik bir grupta 150 kadın 300 erkek olduğu bir evrenden 60 kişinin oluşturduğu bir örneklemin rastgele seçildiğini düşünelim.

- Bu seçim sonucu 30 kadın 30 erkek seçilmiş olsun. 

- Evrende erkekler kadınlardan daha çok temsil edilirken örneklemde eşit temsil edilmektedirler. 

- Kadınların örnekleme seçilme olasılığı = 30/150=0.2
- Erkeklerin örnekleme seçilme olasılığı = 30/300=0.1

-  örnekleme ilişkin ölçümler

```r
set.seed(41)
kadin <- sample(50:90,30)
erkek <- sample(30:70,30)

kadin
```

```
##  [1] 89 84 54 81 57 78 55 71 80 62 87 67 70 83 82 61 66 53 50 69 79 64 85 51 73
## [26] 74 88 52 72 90
```


```r
erkek
```

```
##  [1] 45 56 57 39 37 42 47 50 68 49 62 63 58 69 31 59 52 64 65 66 55 48 30 33 46
## [26] 53 51 67 40 41
```



```r
mean(kadin)
```

```
## [1] 70.9
```


```r
mean(erkek)
```

```
## [1] 51.43333
```

- örneklem ağırlıklandırılması **kullanılmadan** ortalama

```r
(sum(kadin)+sum(erkek))/60
```

```
## [1] 61.16667
```

- örneklem ağırlıklandırılması **kullanılarak** ortalama

```r
(sum(kadin)*(1/0.2) + sum(erkek)*(1/0.1))/450
```

```
## [1] 57.92222
```


## Türkiye Veri Setleri

- Türkiye Uluslararası Eğitim Verisi **(tuev)** geniş kapsamlı uluslararası başarı değerlendirme programlarından **PISA** ve **TIMSS** Türkiye verilerini depolayan bir R kütüphanesidir. 

- Bu eğitimde 
  - **PISA 2018** (OECD, 2019) <br>      
  - **TIMSS 2019** (Mullis, Martin, Foy, Kelly, & Fishbein; 2020) <br>  
veri setleri kullanılacaktır. 

<!-- - -->

<!-- ## **tuev** paketin yüklenmesi -->


<!-- - githubdan paket yükleyebilmek için yüklenmesi gereken paket 📦 <br> -->
<!-- ```{r eval=FALSE} -->
<!-- install.packages("devtools") -->
<!-- # devtools paketinin etkinleştirilmesi -->
<!-- library(devtools) -->
<!-- ``` -->

<!-- - tuev paketinin yüklenmesi 📦 <br> -->
<!-- ```{r eval=FALSE} -->
<!-- devtools::install_github("tuevpaket/tuev") -->
<!-- #paketin etkinleştirilmesi -->
<!-- library(tuev) -->
<!-- ``` -->

<!-- - -->

<!-- ## PISA 2018 Verisi -->

<!-- - bilissel veri seti -->
<!-- ```{r} -->
<!-- data(PISA_COG_2018)  -->
<!-- ``` -->
<!-- - ogrenci veri seti -->
<!-- ```{r} -->
<!-- data(PISA_STU_2018) # ogrenci verisi -->
<!-- ``` -->
<!-- - okul veri seti -->
<!-- ```{r} -->
<!-- data(PISA_SCH_2018) # okul verisi -->
<!-- ``` -->

<!-- - -->

<!-- ## İlk önce pipe **%>%** -->

<!-- - **dplyr()** paketindeki tüm fonksiyonlar daha az değişken oluşturmak amacıyla pipe operatorü **%>%** ile kullanılabilir. -->

<!-- - **%>%** operatorü sık kullanılan bir operatördür. -->
<!-- - kısa yolu: **Ctrl+Shift+M** -->
<!-- - kısa yolu(mac) :**Cmd + Shift + M** -->


<!-- - **%>%** operatorün yer aldığı paket ise **magrittr**  -->

<!-- ```{r message=FALSE, warning=FALSE} -->
<!-- library(magrittr) -->
<!-- ``` -->

<!-- - -->

<!-- ## İlk önce pipe %>% -->
<!-- .pull-left-narrow[ -->

<!-- - **%>%** solundaki nesneye sağındaki fonksiyonu uygular. -->
<!-- ```{r eval=FALSE} -->
<!-- x %>% f(y) = f(x, y) -->
<!-- ``` -->

<!-- - **%>%**  👉<br>   -->

<!-- ] -->

<!-- .pull-right-wide[ -->

<!-- ```{r message=FALSE, warning=FALSE} -->
<!-- library(gapminder) -->
<!-- gapminder %>%  -->
<!--   filter(country == "Canada") %>%  -->
<!--   head(2) -->
<!-- ``` -->

<!--   - bizi fazla yazmaktan kurtarır. -->
<!--   - kodu okunabilir kılar. -->
<!--   - zincirlemeye/bağlamaya izin verir. -->
<!--   - Veri düzenleme işlerinde her zaman kullanışlıdır. -->
<!-- ] -->

<!-- - -->

<!-- ## **%>%** pipe kullanımı -->

<!-- - pipe, her bir fonksiyonu ayrı bir satırda bulundurduğunuzda en net şekilde okunur. -->

<!-- ```{r eval=FALSE} -->
<!-- veri %>%  -->
<!--   ilk_fonksiyon(.....) %>%  -->
<!--   ikinci_fonksiyon(.....) %>%  -->
<!--   ucuncu_fonksiyon(.....) %>% ... -->

<!-- ``` -->


<!-- - pipenin solundaki öğeler, sağdaki fonksiyonun ilk argümanına iletilir.  -->

<!-- - Fonksiyon ilk argümanı olan veriyi pipenin **solundan** alır, kalan argümanlar fonksiyonun **sağındadır.** -->

<!-- - -->

<!-- ## **%>%** pipe kullanımı -->


<!-- - Bazı fonksiyonların, ilk argümanı veri seti olmayabilir. Bu durumda veri seti argüman değeri  .large["**.**"]  olarak kullanılabilir. -->

<!-- - Veri seti regresyon modelinde ilk argüman değildir. -->


<!-- ```{r eval=FALSE} -->

<!-- veri %>% lm(degisken1 ~ degisken2, data= .) -->

<!-- ``` -->

<!-- - -->

<!-- ## **%>%** pipe kullanımı -->

<!-- pipe kullanımı ile oluşan çıktıdan yeni bir nesne oluşturmak istiyorsanız, atama operatorü **<-** -->
<!-- kullanmalısınız 🔗. -->

<!-- ```{r eval=FALSE} -->

<!-- yeninesne <- veri %>% lm(degisken1 ~ degisken2, data= .) -->

<!-- ``` -->

<!-- Bağlama işlemleri ne kadar uzun olursa olsun **<-** operatorü en başta olmalıdır. -->

<!-- - -->

<!-- ## Veri seti yapısını inceleme -->

<!-- Veri setlerinde yapı incelemek için **glimpse()**, **str()** gibi fonksiyonlar kullanılabilir. -->

<!-- ```{r} -->
<!-- glimpse(PISA_COG_2018) -->
<!-- ``` -->

<!-- - -->

<!-- ## Veri seti yapısını inceleme -->

<!-- Veri setlerinde yapı incelemek için **glimpse()**, **str()** gibi fonksiyonlar kullanılabilir. -->

<!-- ```{r} -->
<!-- glimpse(PISA_STU_2018) -->
<!-- ``` -->

<!-- - -->

<!-- ## Veri seti yapısını inceleme -->

<!-- Veri setlerinde yapı incelemek için **glimpse()**, **str()** gibi fonksiyonlar kullanılabilir. -->

<!-- ```{r} -->
<!-- glimpse(PISA_SCH_2018) -->
<!-- ``` -->

<!-- - -->

<!-- ## Yeni Veri Seti Oluşturma -->

<!-- - Veri setinden sütun bazında seçim yapmak için **select()** fonksiyonu kullanılabilir. -->

<!-- - **select()** fonksiyonu kullanımı -->
<!-- ```{r eval=FALSE} -->
<!-- select(veri_seti, degisken_adi, degisken_adi,..) -->
<!-- ``` -->

<!-- - **select()** fonksiyonunun pipe ile kullanımı -->
<!-- ```{r eval=FALSE} -->
<!-- veri_seti %>% select(degisken_adi, degisken_adi,..) -->
<!-- ``` -->

<!-- - -->

<!-- ## Yeni Veri Seti Oluşturma -->

<!-- -  6890 satır 1119 sütunlu veri seti -->
<!-- PISA_STU_2018'yı kullanarak yeni bir veri seti oluşturalım. -->

<!-- ```{r} -->
<!-- PISA_STU_2018 %>% select(CNTSTUID,ST001D01T,ST004D01T,ESCS) -->
<!-- ``` -->

<!-- - -->
<!-- ## **arrange()** fonksiyonu -->

<!-- - **arrange()** veri setini satırlara göre tekrar sıralar.  -->
<!-- - Bu sıralamayı alfabetik yapar.  -->

<!-- - **arrange()** fonksiyonu kullanımı -->
<!-- ```{r eval=FALSE} -->
<!-- arrange(veri_seti, degisken_adi) %>% head(3) -->
<!-- ``` -->

<!-- - **arrange()** fonksiyonunun pipe ile kullanımı -->

<!-- ```{r eval=FALSE} -->
<!-- veri_seti %>% arrange(degisken_adi) -->
<!-- ```   -->

<!-- - -->
<!-- ## **arrange()** fonksiyonu -->

<!-- - Veri setinden dört değişken seçip yeni bir veri setine atama  -->

<!-- ```{r} -->

<!-- df1 <- PISA_STU_2018 %>% select(CNTSTUID,ST001D01T,ST004D01T,ESCS) -->

<!-- ```   -->

<!-- - Yeni oluşan df1 veri setini ESCS (sosyaekonomik düzey) puanlarına göre sıralama -->

<!-- ```{r} -->
<!-- arrange(df1,ESCS) -->
<!-- ``` -->

<!-- - -->
<!-- ## **arrange()** fonksiyonu -->

<!-- - **desc()** fonksiyonu ile sıralama büyükten küçüğe de yapılabilir. -->

<!-- ```{r} -->
<!-- arrange(df1,desc(ESCS)) -->

<!-- ``` -->

<!-- - -->
<!-- ## **select()** ve **arrange()**  fonksiyonu -->

<!-- Yaptığımız işlemleri pipe operatoru ile bağlayabilirsiniz. -->

<!-- ```{r} -->
<!-- PISA_STU_2018 %>%  -->
<!--   select(CNTSTUID,ST001D01T,ST004D01T,ESCS) %>% -->
<!--   arrange(ESCS) -->
<!-- ``` -->

<!-- - -->
<!-- ## **filter()** fonksiyonu -->

<!-- - Satır bazında veri seçim işlemi yapmak amacıyla kullanılır. -->

<!-- - **filter()** fonksiyonu kullanımı -->
<!-- ```{r eval=FALSE} -->
<!-- filter(veri_seti, kosul ve/veya kosullar) -->
<!-- ``` -->

<!-- - **filter()** fonksiyonunun pipe ile kullanımı -->
<!-- ```{r eval=FALSE} -->
<!-- veri_seti %>% filter(kosul ve/veya kosullar) -->
<!-- ``` -->

<!-- - -->
<!-- ## Mantıksal Operatorler -->

<!-- - **filter()** fonksiyonunu **mantıksal operatorler** kullanarak satır bazında seçim yapar. -->

<!-- - **mantıksal operatorler** koşulları test eder.  -->

<!-- ```{r} -->
<!-- x <- 1 -->
<!-- x==1 -->
<!-- ``` -->

<!-- ```{r} -->
<!-- x <- 1 -->
<!-- x!=1 -->
<!-- ``` -->

<!-- - -->
<!-- ## Mantıksal Operatorler -->

<!-- - TRUE, FALSE ve NA değerleri alırlar. -->
<!-- - **filter()** fonksiyonunu ise koşulun sağlandığı satırları seçer. -->

<!--   - **==**         : eşittir. -->
<!--   - **!= **        : eşit değildir. -->
<!--   - **>,>=,<,<= ** : büyüktür, büyük eşittir,.... -->
<!--   - **%in%**       : bir ya da birden fazla değerin varlığını kontrol eder.  -->

<!-- - Mantıksal Operatörlerin kombinasyonları da kullanılabilir. -->
<!--   - **&**: ve -->
<!--   - **|**: ve ya -->
<!--   - **!**: değil -->


<!-- - -->
<!-- ## **filter()** fonksiyonu -->

<!-- PISA verisinde anne eğitim düzeyi lisansüstü olan öğrencilerin seçilmesi -->

<!-- ```{r} -->
<!-- PISA_STU_2018 %>% filter(MISCED==6) %>% head(4) -->
<!-- ``` -->

<!-- - -->
<!-- ## **filter()** fonksiyonu -->

<!-- PISA verisinde anne eğitim düzeyi **ve** baba eğitim düzeyi lisansüstü olan öğrencilerin seçilmesi -->

<!-- ```{r} -->
<!-- PISA_STU_2018 %>% filter(MISCED==6 & FISCED==6)  %>% head(4) -->

<!-- ``` -->

<!-- - -->
<!-- ## **filter()** fonksiyonu -->

<!-- PISA verisinde anne eğitim düzeyi **ve ya** baba eğitim düzeyi lisansüstü olan öğrencilerin seçilmesi -->

<!-- ```{r} -->
<!-- PISA_STU_2018 %>% filter(MISCED==6 | FISCED==6) -->

<!-- ``` -->



<!-- - -->

<!-- .hand-large[teşekkürler !] -->




<!-- .large[😕] -->

<!-- <br> -->
<!-- .large[😃] -->


<!-- - -->
<!-- ## KAYNAKLAR -->

<!-- - Caro, D. H. & Biecek, P. (2017). intsvy: An R Package for analyzing ınternational large-scale assessment data. Journal of Statistical Software, 81(7), 1-44. doi: 10.18637/jss.v081.i07 (URL:http://doi.org/10.18637/jss.v081.i07) -->

<!-- - Martin, M. O., von Davier, M., & Mullis, I. V. S. (Eds.). (2020). Methods and Procedures: TIMSS 2019 Technical Report. Boston College, TIMSS & PIRLS International Study Center website:   https://timssandpirls.bc.edu/timss2019/methods adresinden erişildi. -->

<!-- - Mullis, I. V. S., Martin, M. O., Foy, P., Kelly, D. L., & Fishbein, B. (2020). TIMSS 2019 International Results in Mathematics and Science. Boston College, TIMSS & PIRLS International Study Center website: https://timssandpirls.bc.edu/timss2019/international-results/ adresinden erişildi. -->

<!-- - -->
<!-- ## KAYNAKLAR -->

<!-- -  "Atar, B., Atalay Kabasakal, K., Ünsal Özberk, E. B. , Özberk, E.. H. ve Kıbrıslıoğlu Uysal, N. (2019). **R ile Veri Analizi ve Psikometri Uygulamaları**. PegemA Akademi -->
<!-- - OECD (2019). PISA 2018 Assessment and Analytical Framework. PISA, OECD Publishing, Paris, https://doi.org/10.1787/b25efab8-en adresinden erişildi. -->

<!-- - Wickham, H.  François, R., Henry L. & Müller, K. (2021). dplyr: A Grammar of Data   Manipulation. R package   version 1.0.7. https://CRAN.R-project.org/package=dplyr -->


