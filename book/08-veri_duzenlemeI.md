# Veri duzenleme - I




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



## **tuev** paketin yüklenmesi


- githubdan paket yükleyebilmek için yüklenmesi gereken paket 📦 <br>

```r
install.packages("devtools")
# devtools paketinin etkinleştirilmesi
library(devtools)
```

- tuev paketinin yüklenmesi 📦 <br>

```r
devtools::install_github("tuevpaket/tuev")
#paketin etkinleştirilmesi
library(tuev)
```

-

## PISA 2018 Verisi

- bilissel veri seti

```r
load("import/PISA_COG_2018.rda")
```
- ogrenci veri seti

```r
load("import/PISA_STU_2018.rda") # ogrenci verisi
```
- okul veri seti

```r
load("import/PISA_SCH_2018.rda") # okul verisi
```


## pipe **%>%**

- **dplyr()** paketindeki tüm fonksiyonlar daha az değişken oluşturmak amacıyla pipe operatorü **%>%** ile kullanılabilir.

- **%>%** operatorü sık kullanılan bir operatördür.
- kısa yolu: **Ctrl+Shift+M**
- kısa yolu(mac) :**Cmd + Shift + M**


- **%>%** operatorün yer aldığı paket ise **magrittr**


```r
library(magrittr)
```


- **%>%** solundaki nesneye sağındaki fonksiyonu uygular.

```r
x %>% f(y) = f(x, y)
```

- **%>%**  👉<br>





```r
library(gapminder)
gapminder %>%
  filter(country == "Canada") %>%
  head(2)
```

```
## # A tibble: 2 x 6
##   country continent  year lifeExp      pop gdpPercap
##   <fct>   <fct>     <int>   <dbl>    <int>     <dbl>
## 1 Canada  Americas   1952    68.8 14785584    11367.
## 2 Canada  Americas   1957    70.0 17010154    12490.
```

  - bizi fazla yazmaktan kurtarır.
  - kodu okunabilir kılar.
  - zincirlemeye/bağlamaya izin verir.
  - Veri düzenleme işlerinde her zaman kullanışlıdır.





- pipe, her bir fonksiyonu ayrı bir satırda bulundurduğunuzda en net şekilde okunur.


```r
veri %>%
  ilk_fonksiyon(.....) %>%
  ikinci_fonksiyon(.....) %>%
  ucuncu_fonksiyon(.....) %>% ...
```


- pipenin solundaki öğeler, sağdaki fonksiyonun ilk argümanına iletilir.

- Fonksiyon ilk argümanı olan veriyi pipenin **solundan** alır, kalan argümanlar fonksiyonun **sağındadır.**




- Bazı fonksiyonların, ilk argümanı veri seti olmayabilir. Bu durumda veri seti argüman değeri  **.**  olarak kullanılabilir.

- Veri seti regresyon modelinde ilk argüman değildir.



```r
veri %>% lm(degisken1 ~ degisken2, data= .)
```




- pipe kullanımı ile oluşan çıktıdan yeni bir nesne oluşturmak istiyorsanız, atama operatorü **<-**
kullanmalısınız 🔗.


```r
yeninesne <- veri %>% lm(degisken1 ~ degisken2, data= .)
```

Bağlama işlemleri ne kadar uzun olursa olsun **<-** operatorü en başta olmalıdır.




- Veri setlerinde yapı incelemek için **glimpse()**, **str()** gibi fonksiyonlar kullanılabilir.


```r
glimpse(PISA_COG_2018)
```


- Veri setlerinde yapı incelemek için **glimpse()**, **str()** gibi fonksiyonlar kullanılabilir.


```r
glimpse(PISA_STU_2018)
```



```r
glimpse(PISA_SCH_2018)
```


## **select()**

- Veri setinden sütun bazında seçim yapmak için **select()** fonksiyonu kullanılabilir.

- **select()** fonksiyonu kullanımı

```r
select(veri_seti, degisken_adi, degisken_adi,..)
```

- **select()** fonksiyonunun pipe ile kullanımı

```r
veri_seti %>% select(degisken_adi, degisken_adi,..)
```


-  6890 satır 1119 sütunlu veri seti
PISA_STU_2018'yı kullanarak yeni bir veri seti oluşturalım.


```r
PISA_STU_2018 %>% select(CNTSTUID,ST001D01T,ST004D01T,ESCS) %>%
head(6)
```

```
## # A tibble: 6 x 4
##   CNTSTUID ST001D01T     ST004D01T  ESCS     
##      <dbl> <dbl+lbl>     <dbl+lbl>  <dbl+lbl>
## 1 79200768 10 [Grade 10] 2 [Male]   -2.45    
## 2 79201064 10 [Grade 10] 2 [Male]   -2.10    
## 3 79201118 10 [Grade 10] 1 [Female] -2.27    
## 4 79201275  9 [Grade 9]  2 [Male]    0.0324  
## 5 79201481  9 [Grade 9]  2 [Male]   -0.0674  
## 6 79201556 10 [Grade 10] 2 [Male]    0.398
```

## **arrange()**

- **arrange()** veri setini satırlara göre tekrar sıralar.
- Bu sıralamayı alfabetik yapar.

- **arrange()** fonksiyonu kullanımı

```r
arrange(veri_seti, degisken_adi) %>% head(3)
```

- **arrange()** fonksiyonunun pipe ile kullanımı


```r
veri_seti %>% arrange(degisken_adi)
```

- Veri setinden dört değişken seçip yeni bir veri setine atama


```r
df1 <- PISA_STU_2018 %>% select(CNTSTUID,ST001D01T,ST004D01T,ESCS)
```

- Yeni oluşan df1 veri setini ESCS (sosyaekonomik düzey) puanlarına göre sıralama


```r
arrange(df1,ESCS) %>% head(6)
```

```
## # A tibble: 6 x 4
##   CNTSTUID ST001D01T     ST004D01T  ESCS     
##      <dbl> <dbl+lbl>     <dbl+lbl>  <dbl+lbl>
## 1 79201575 11 [Grade 11] 2 [Male]   -4.75    
## 2 79205397 10 [Grade 10] 1 [Female] -4.72    
## 3 79200690  8 [Grade 8]  2 [Male]   -4.29    
## 4 79201907 10 [Grade 10] 2 [Male]   -4.29    
## 5 79206542 10 [Grade 10] 2 [Male]   -4.20    
## 6 79200541 11 [Grade 11] 2 [Male]   -4.19
```


- **desc()** fonksiyonu ile sıralama büyükten küçüğe de yapılabilir.


```r
arrange(df1,desc(ESCS)) %>% head(6)
```

```
## # A tibble: 6 x 4
##   CNTSTUID ST001D01T     ST004D01T  ESCS     
##      <dbl> <dbl+lbl>     <dbl+lbl>  <dbl+lbl>
## 1 79201409 10 [Grade 10] 2 [Male]   2.76     
## 2 79207242 10 [Grade 10] 2 [Male]   2.62     
## 3 79203361 10 [Grade 10] 2 [Male]   2.28     
## 4 79206271 10 [Grade 10] 2 [Male]   2.18     
## 5 79203677  9 [Grade 9]  1 [Female] 1.99     
## 6 79200191  9 [Grade 9]  1 [Female] 1.92
```


- Yaptığımız işlemleri pipe operatoru ile bağlayabilirsiniz.


```r
PISA_STU_2018 %>%
  select(CNTSTUID,ST001D01T,ST004D01T,ESCS) %>%
  arrange(ESCS) %>%
  head(6)
```

```
## # A tibble: 6 x 4
##   CNTSTUID ST001D01T     ST004D01T  ESCS     
##      <dbl> <dbl+lbl>     <dbl+lbl>  <dbl+lbl>
## 1 79201575 11 [Grade 11] 2 [Male]   -4.75    
## 2 79205397 10 [Grade 10] 1 [Female] -4.72    
## 3 79200690  8 [Grade 8]  2 [Male]   -4.29    
## 4 79201907 10 [Grade 10] 2 [Male]   -4.29    
## 5 79206542 10 [Grade 10] 2 [Male]   -4.20    
## 6 79200541 11 [Grade 11] 2 [Male]   -4.19
```

## **filter()**

- Satır bazında veri seçim işlemi yapmak amacıyla kullanılır.

- **filter()** fonksiyonu kullanımı

```r
filter(veri_seti, kosul ve/veya kosullar)
```

- **filter()** fonksiyonunun pipe ile kullanımı

```r
veri_seti %>% filter(kosul ve/veya kosullar)
```



- **filter()** fonksiyonunu **mantıksal operatorler** kullanarak satır bazında seçim yapar.

- **mantıksal operatorler** koşulları test eder.


```r
x <- 1
x==1
```

```
## [1] TRUE
```


```r
x <- 1
x!=1
```

```
## [1] FALSE
```

- TRUE, FALSE ve NA değerleri alırlar.
- **filter()** fonksiyonunu ise koşulun sağlandığı satırları seçer.

  - **==**         : eşittir.
  - **!= **        : eşit değildir.
  - **>,>=,<,<= ** : büyüktür, büyük eşittir,....
  - **%in%**       : bir ya da birden fazla değerin varlığını kontrol eder.

- Mantıksal Operatörlerin kombinasyonları da kullanılabilir.
  - **&**: ve
  - **|**: ve ya
  - **!**: değil



- PISA verisinde anne eğitim düzeyi lisansüstü olan öğrencilerin seçilmesi


```r
PISA_STU_2018 %>% filter(MISCED==6) %>% head(4)
```

```
## # A tibble: 4 x 1,119
##   CNTRYID     CNT       CNTSCHID CNTSTUID CYC   NatCen     STRATUM    SUBNATIO  
##   <dbl+lbl>   <chr+lbl>    <dbl>    <dbl> <chr> <chr+lbl>  <chr+lbl>  <chr+lbl> 
## 1 792 [Turke~ TUR [Tur~ 79200001 79201275 07MS  079~ [Tur~ TUR~ [TUR~ 792~ [Tur~
## 2 792 [Turke~ TUR [Tur~ 79200001 79202343 07MS  079~ [Tur~ TUR~ [TUR~ 792~ [Tur~
## 3 792 [Turke~ TUR [Tur~ 79200001 79203553 07MS  079~ [Tur~ TUR~ [TUR~ 792~ [Tur~
## 4 792 [Turke~ TUR [Tur~ 79200001 79204714 07MS  079~ [Tur~ TUR~ [TUR~ 792~ [Tur~
## # i 1,111 more variables: OECD <dbl+lbl>, ADMINMODE <dbl+lbl>,
## #   LANGTEST_QQQ <dbl+lbl>, LANGTEST_COG <dbl+lbl>, LANGTEST_PAQ <dbl+lbl>,
## #   BOOKID <dbl+lbl>, ST001D01T <dbl+lbl>, ST003D02T <dbl+lbl>,
## #   ST003D03T <dbl+lbl>, ST004D01T <dbl+lbl>, ST005Q01TA <dbl+lbl>,
## #   ST006Q01TA <dbl+lbl>, ST006Q02TA <dbl+lbl>, ST006Q03TA <dbl+lbl>,
## #   ST006Q04TA <dbl+lbl>, ST007Q01TA <dbl+lbl>, ST008Q01TA <dbl+lbl>,
## #   ST008Q02TA <dbl+lbl>, ST008Q03TA <dbl+lbl>, ST008Q04TA <dbl+lbl>, ...
```



- PISA verisinde anne eğitim düzeyi **ve** baba eğitim düzeyi lisansüstü olan öğrencilerin seçilmesi


```r
PISA_STU_2018 %>% filter(MISCED==6 & FISCED==6)  %>% head(4)
```

```
## # A tibble: 4 x 1,119
##   CNTRYID     CNT       CNTSCHID CNTSTUID CYC   NatCen     STRATUM    SUBNATIO  
##   <dbl+lbl>   <chr+lbl>    <dbl>    <dbl> <chr> <chr+lbl>  <chr+lbl>  <chr+lbl> 
## 1 792 [Turke~ TUR [Tur~ 79200001 79201275 07MS  079~ [Tur~ TUR~ [TUR~ 792~ [Tur~
## 2 792 [Turke~ TUR [Tur~ 79200001 79202343 07MS  079~ [Tur~ TUR~ [TUR~ 792~ [Tur~
## 3 792 [Turke~ TUR [Tur~ 79200002 79201796 07MS  079~ [Tur~ TUR~ [TUR~ 792~ [Tur~
## 4 792 [Turke~ TUR [Tur~ 79200002 79202928 07MS  079~ [Tur~ TUR~ [TUR~ 792~ [Tur~
## # i 1,111 more variables: OECD <dbl+lbl>, ADMINMODE <dbl+lbl>,
## #   LANGTEST_QQQ <dbl+lbl>, LANGTEST_COG <dbl+lbl>, LANGTEST_PAQ <dbl+lbl>,
## #   BOOKID <dbl+lbl>, ST001D01T <dbl+lbl>, ST003D02T <dbl+lbl>,
## #   ST003D03T <dbl+lbl>, ST004D01T <dbl+lbl>, ST005Q01TA <dbl+lbl>,
## #   ST006Q01TA <dbl+lbl>, ST006Q02TA <dbl+lbl>, ST006Q03TA <dbl+lbl>,
## #   ST006Q04TA <dbl+lbl>, ST007Q01TA <dbl+lbl>, ST008Q01TA <dbl+lbl>,
## #   ST008Q02TA <dbl+lbl>, ST008Q03TA <dbl+lbl>, ST008Q04TA <dbl+lbl>, ...
```


- PISA verisinde anne eğitim düzeyi **ve ya** baba eğitim düzeyi lisansüstü olan öğrencilerin seçilmesi


```r
PISA_STU_2018 %>% filter(MISCED==6 | FISCED==6) %>% head(4)
```

```
## # A tibble: 4 x 1,119
##   CNTRYID     CNT       CNTSCHID CNTSTUID CYC   NatCen     STRATUM    SUBNATIO  
##   <dbl+lbl>   <chr+lbl>    <dbl>    <dbl> <chr> <chr+lbl>  <chr+lbl>  <chr+lbl> 
## 1 792 [Turke~ TUR [Tur~ 79200001 79201275 07MS  079~ [Tur~ TUR~ [TUR~ 792~ [Tur~
## 2 792 [Turke~ TUR [Tur~ 79200001 79201556 07MS  079~ [Tur~ TUR~ [TUR~ 792~ [Tur~
## 3 792 [Turke~ TUR [Tur~ 79200001 79202343 07MS  079~ [Tur~ TUR~ [TUR~ 792~ [Tur~
## 4 792 [Turke~ TUR [Tur~ 79200001 79203553 07MS  079~ [Tur~ TUR~ [TUR~ 792~ [Tur~
## # i 1,111 more variables: OECD <dbl+lbl>, ADMINMODE <dbl+lbl>,
## #   LANGTEST_QQQ <dbl+lbl>, LANGTEST_COG <dbl+lbl>, LANGTEST_PAQ <dbl+lbl>,
## #   BOOKID <dbl+lbl>, ST001D01T <dbl+lbl>, ST003D02T <dbl+lbl>,
## #   ST003D03T <dbl+lbl>, ST004D01T <dbl+lbl>, ST005Q01TA <dbl+lbl>,
## #   ST006Q01TA <dbl+lbl>, ST006Q02TA <dbl+lbl>, ST006Q03TA <dbl+lbl>,
## #   ST006Q04TA <dbl+lbl>, ST007Q01TA <dbl+lbl>, ST008Q01TA <dbl+lbl>,
## #   ST008Q02TA <dbl+lbl>, ST008Q03TA <dbl+lbl>, ST008Q04TA <dbl+lbl>, ...
```



