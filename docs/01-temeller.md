# R ve Rstudio Temeller 





## R Temeller 📊

*  R ve Rstudionun yüklenmesi
*  Temel Özellikler
*  Fonksiyonlar
*  Çalışma alanı, çalışma dizini
*  Kaynak Tanıtımı

## R Nedir?

* R istatistiksel hesaplamalar yapabilen bir programlama dilidir.  

* 1996 yılında Auckland Universitesi'nde **R**oss Ihaka ve **R**obert Gentleman tarafından geliştirilmiştir.

* 1960 yılında Bell Laboratories'de John Chambers ve arkadaşları tarafından geliştirilen **S dilinin** açık kaynak kodlu halidir. 

* R yazılımı Genel Kamu Lisansi (GNU* General Public Licence) koşulları altında ücretsiz dağıtılmaktadır.  

* R ve Temel Gelistirme Takimi (R core team) ile ilgili bilgilere R'in internet sitesinden (<https://www.r* project.org/>) ulaşılabilir.  

* R dilinin ilk sürümü 29 Subat 2000 tarihinde yayınlanmıştır. Her iki* üç ayda bir sürümler güncellenmektedir.  

*  The latest release (2022* 06* 23, Funny* Looking Kid) R* 4.2.1.tar.gz, read what's new in the latest version

* R özgür istatiksel bir programa dilidir. 

* R aynı zamanda bir yorumlayıcıdır (interpreter).

* R, bir veri tabanı **değildir** ama veri tabanlarına bağlanabilir. 

* Önceki sürümleri kullancı dostu olmasa da, son zamanlarda kod editörlerine çok sayıda işlev eklenmiştir.  

* Ayrıca java gibi diller aracılığı ile ara yüz desteğine sahip bir yazılım geliştirme ortamıdır.  

* Tablolardan oluşan yazılım paketlerine (Excel, Minitab gibi) benzememekle birlikte, yeni geliştiren bazı paketler farklı ara yüzler sağlamaktadır.

* Ücretsiz olması nedeniyle, ticari desteğe tabi bir yazılım değildir. Ancak destek alınabilecek çok sayıda kaynağa erisilebilir. (stackoverflow, mail listeleri)  

## Neden R?

* R istatistiksel programlama, veri analizi ve grafiksel gösterim için kullanılan ve ticari bir amaç gütmeyen ücretsiz bir yazılımdır.

* R, UNIX, Windows ve MacOS gibi çeşitli platformlarda kodları derlemekte ve çalıştırmaktadır.

* SPSS, SAS gibi veri analizi programları ücretlidir, ayrıca bazı özel psikometri analizleri için yeterli değildir.

* R, açık kaynak kodlu olduğu için program kodlarına istenildiği zaman erişilebilir.

* Diğer istatistiksel yazılımlar ile karşılaştırıldığında R "komut satırı" ara yüzünü kullanmaktadır.

* Basit koşullar, döngüler ve kişi* tanımlı fonksiyonlar yazmaya uyumlu basit ve etkili bir yazım diline sahiptir.

* R'in ayrıca grafiksel imkânları oldukça fazladır; bu nedenle yayınlanabilir/basma uygun grafikler oluşturmak kolaydır.

* R ekibi birçok alanda ayrıntılı dokümantasyonu yapılmış R paketleri geliştirmektedir.

* Klasik istatistik yazılımlarında analiz sonuçları bir kez elde edilir. R yazılımında ise sonuçlar çalışma alanına kaydedilerek, ileriki analiz aşamalarında tekrar kullanabilir.

* R, psikometri alanında sıklıkla kullanılan simülasyon çalışmaları için (tekrarlı işlemler için) de avantaj sağlamaktadır.

* R, diğer programlama dilleri ve istatistik paket programları ile uyumludur.

## Dezavantajları

* Basta öğrenilmesi kolay görünse de, R'da uzmanlaşmak oldukça zordur.

* Menu ile kullanılan programlara alışkın olan kişiler için başlangıçta korkutucu olabilir.

* R ile bir analizi yapabilmek için planlama yapılması gerekmektedir.

* R kullanıcıları çoğunlukla programlamacı **değildir.**

* Programlamaya hâkim olmayan kişiler tarafından hazırlanan, okunması ve sürdürülebilirliği zor kodlar oluşturulabilir.

* Başlangıçta kodları yazmak yıldırıcı olabilir; ancak çalışmaların tekrarlanabilirliği açısından avantaj sağlamaktadır. 
.Bu duruma bir örnek vermek gerekirse, 20 adet regresyon denklemi kurulup regresyon katsayıları karşılaştırılmak istenirse,
 R yazılımı sadece regresyon kat sayılarını gösterebilir ve tek bir satırda tüm regresyon sonuçlarını karşılaştırmaya olanak verir. 
Aynı işlem için diğer istatistiksel yazılımlarda 20 ayrı pencereden elde edilen sonuçların elle yazılarak karşılaştırılması gerekecektir.

* R'da hata yapma olasılığı diğer programlara göre daha fazladır. Hata kaynağı için varsayımların iyi bilinmesi gerekmektedir.

* Hız konusunda SPSS ve SAS'a göre avantajlı olsa da diğer dillere göre (Python, Matlab gibi) daha yavaştır.

* Geliştirilen çok fazla paket olduğu icin, ihtiyaca uygun en iyi paketin seçimi zor olabilmektedir.

* Bu bir dezavantaj gibi görünse de istatistiksel işlemlerin arka planını anlamaya yardımcı olur.

* Bu tarz zayıf hazırlanmış kodlar farklı koşullarda yavaş çalışabilmektedir.

* Çoğu kullanıcı bu eksiklikleri gidermek için kodları değiştiremez.
Özellikle çok iyi yapılandırılmamış olan kodlar R’da yavaş çalışabilmektedir. 

## R Yazılımın Yüklenmesi

* Internet tarayıcısına R yazılımın internet sitesinin ana sayfasının adresi yazılır. <https://www.r-project.org/>

* Sol menüde yer alan "download CRAN" bölümüne tıkladıktan sonra ülke seçilir. Seçilen ülkenin yakinliği sadece yükleme hızını değiştirecektir.

* Çıkan sayfada "Download and Install R" baslığı altından işletim sistemine uygun olan bağlantı seçilir.

* R konsolda çalışmaya doğrudan başlanabilir; ancak konsol kullanımı bir kod editörü olmadığı için çok kullanışlı değildir.

* Rstudio hata ayıklama, görselleştirme araçları ile birlikte yüklenen modern bir kod editörüdür.

* <https://www.rstudio.com/> internet sitesinden kullanılan bilgisayar ve işletim sistemine uygun olarak seçilip indirilebilmektedir.

*  R ile daha üretken olmanıza yardımcı olacak bir dizi araç içerir, örneğin:
    * R kodlarınızı vurgulamak için bir sözdizimi vurgulama düzenleyicisi
    * R kodlarını yazmanıza yardımcı olacak işlevler (otomatik tamamlama)
    *Çeşitli grafikler oluşturmak ve kaydetmek için çeşitli araçlar (ör. histogramlar, dağılım grafiği)
    * Verileri içe veya dışa aktarmak için bir çalışma alanı yönetim aracı
    

## Diğer Gerekli Yüklemeler

*  [Java](https://javadl.oracle.com/webapps/download/AutoDL?BundleId=245479_4d5417147a92418ea8b615e228bb6935)
* [Rtools](https://cloud.r* project.org/bin/windows/Rtools)
Rtools, kaynak koddan derleme yapmaya yarayan araçları içeren bir R yardımcısıdır.
**Önemli:** Eğer Windows kullanıyorsanız, ayrıca Rtools yüklemeniz gerekir.

*  devtools 


```r
install.packages("devtools")
```

## R STUDIO

*  Rstudio'da panellerin yerlerini değiştirebiliriz.

*  Bunun yanı sıra yazı tipi, büyüklüğü gibi özellikleri de değiştirebiliriz.

*  Dönem boyunca Rstudio kullanımına aşina olacaksınız. Bu süreci kolaylaştırmak için
bağlantıları verilen dökümanlara göz atabilirsiniz. 

*  [Rstudio cheatsheet](Kaynaklar/rstudio* ide.pdf)  

*  [Oscar Torres* Reyna tutorial](Kaynaklar/rstudio_tutorial.pdf)
 




## R Temel Özellikler

R konsolda gorunen **>** isareti, R yaziliminin sizden komut bekledigini belirtir. R'in hesap makinesi olarak kullanim ornekleri sunulmustur.


```r
2+2
```

```
[1] 4
```
R boşluklara duyarlı değildir.

```r
2  +2 
```

```
[1] 4
```
R boşluklara duyarlı değildir.

```r
2+
  2
```

```
[1] 4
```


## Atama Operatoru

* Atama operatörü olarak "küçüktür" simgesi ile "kısa çizgi" simgesi **`<- `** simgeleri kullanılabilir.



* **`<- `** yerine "eşittir" **`=`** simgesi de atama operatörü olarak kullanılabilir.



* Ancak **`=`** operatörü programlama yaparken matematiksel eşitlikle karışabilmektedir.



## Nesne Isimleri

* Atama yapılacak nesne isimlendirilirken harflerle (A* Z veya a* z) başlamalıdır.



* İsimlendirmeye harfle başlandıktan sonra rakamlar (0* 9), nokta (.) ve alt cizgi (\_) ile devam edilebilmektedir.



* R harflerin küçük ve ya büyük olmasına karşı duyarlıdır.



* R fonksiyonlarına benzer isimlerde nesne ismi kullanmamaya **dikkat edilmelidir.**



* Ayrıca **c,C,D,F,I,q,t,T** gibi tek harfli nesne ismi kullanmaktan kaçınılmalıdır; bunların R'da özel anlamları bulunmaktadır.



## Yorum Satırları

*  R yazılımında **\#** işareti ile başlayan satir, yorum satırıdır.



*  Genellikle komutların anlamını açıklamak için kullanılmaktadır.



*  R, bu satırları dikkate almaz, bunlar sadece kullanıcılar için bilgi ve hatırlatıcı açıklamaları içermektedir.





```r
# Yorum satirlari kodlarinizi anlamli hale getirir.
a <-  2
y <-  a * a
y
```

```
[1] 4
```


## Basit İslemler

* toplama işlemi için **+**,



* çıkarma işlemi için *** **,



* çarpma işlemi için  **\***,



* bölme işlemi için **/**,



* üs alma işlemi için  **^** veya **\*\***



* mod alma icin ise **%%** operatorleri kullanılmaktadır.


## Basit İslemler

Eni 4 cm, boyu 10 cm bir dikdörtgenin alanı hesaplayınız.


```r
# en nesnesi tanimlama

# boy nesnesi tanimlama

# alan nesnesi tanimlama

# alan nesnesini yazdirma
```


```
[1] 40
```


## Basit İslemler

Eni 4 cm, boyu 10 cm bir dikdörtgenin köşegen uzunluğunu hesaplayınız.


```r
# en nesnesi tanimlama

# boy nesnesi tanimlama

# kosegen nesnesi tanimlama

# kosegen nesnesini yazdirma
```



```
[1] 10.77033
```


## R Paketler


*  R fonksiyonları ayrı paketler halinde düzenlenmişlerdir. Böylece gerekli paketlerle çalışarak daha az bellek kullanımı ve hızlı işlem gücü sağlanır.



*  Bu paketlerin bir başka avantajı da yazılan fonksiyonlardan oluşan paketlerin CRAN'den temin edilerek yüklenebilmesidir.



*  Her paketin bir yaratıcısı ve kendisine ait bir yardım dosyası bulunur.


```r
# paket yukleme
# install.packages("CTT")
# paket aktive etme
library(CTT)
```


*  Paket yükleme işlemi Rstudio'da yer alan menüler aracılığı ile de yapılabilmektedir.

## R Paketler

*  R yüklenirken temel (base) paket yüklenir.



*  R paketleri R fonksiyonlarının, verilerinin ve iyi derlenmiş bir formatta kodların kombinasyonlarından oluşmaktadır. `library()` komutu ile kişisel kütüphanenizdeki yüklü paketleri görebilirsiniz.

*   Sadece temel pakette 1000'den fazla fonksiyon bulunmaktadır.



```r
# temel paket fonksiyonlarina ulasimak icin  
fonksiyonlar <-  builtins()
length(fonksiyonlar)
fonksiyonlar[910:920]
```

```
[1] 1380
 [1] "Cstack_info"                "crossprod"                 
 [3] "cospi"                      "cosh"                      
 [5] "cos"                        "contributors"              
 [7] "Conj"                       "conflicts"                 
 [9] "conflictRules"              "conditionMessage.condition"
[11] "conditionMessage"          
```



## R Paketler

![yükle* etkinleştir)](figs/packagebulb.png)


## Yardım Sayfaları

*  R'da temel ve diğer paketlerde yer alan fonksiyonların işlevleri görmek için yardım sayfalarını inceleyebilirsiniz. `?` ve `help()` fonksiyonları ayni işleve sahiptir.




```r
?is.na

help(sqrt)
```

*  Örneğin CTT paketini hem yüklediniz hem de etkinleştirdiniz. Paket fonksiyon ve veri içeriğini aşağıdaki komutlarla görebilirsiniz.


```r
# install.packages(CTT)
library(CTT)
ls("package:CTT") 
data(package = "CTT") # yeni bir sekmede acilir.
?reliability
```



*  Etkinleştirdiğiniz paketlerde yer alan fonksiyonların yardım sayfalarına ulaşabilirsiniz.


## Fonksiyon nedir?

* Fonksiyon belli bir görevi yerine getirmek için yazılan bir grup komuttur.



* Fonksiyonların çalışması için girdilerinin olması gerekmektedir. Fonksiyonlar girdileri ile yaptıkları işlem sonucunda bir çıktı oluştururlar.



* Fonksiyonlar girdileri o fonksiyonun çalışması için önceden belirlenen argümanlar ve o argümanların değerlerinden oluşur.


* Fonksiyonların kullanımında uç noktaya dikkat edilmelidir.

1.  argümanların sırası
2.  argümanların olağan (default) değerleri
3.  bazı argümanların zorunlu, bazı argümanların opsiyonel olmasıdır



## Fonksiyon nedir?

Kişisel tanımlı fonksiyon yazılması şablonu aşağıdaki gibidir.


```r
fonksiyonadi<-  function(argumanlar ve olagan degerleri){
  kodlar
  return()
}
```



Oluşturulan fonksiyon çalıştırılırken ise aşağıdaki seklinde çalıştırılır.


```r
fonksiyonadi(argumanlar ve degerleri)
```


## Fonksiyon nedir?

*  Kare alma işlemi aşağıdaki şekilde yapılabilir.


```r
sayi <-  4
sayi * sayi
sayi ^2
```

```
[1] 16
[1] 16
```



*  Bu işlem sürekli yapılacaksa fonksiyon olarak yazılabilir.


```r
# kare alma fonksiyonu
kare_al <-  function(sayi){
  return(sayi*sayi)
  }
kare_al(4)
```

```
[1] 16
```


## Fonksiyon nedir?

Farklı dereceden üsler alabilen bir fonksiyon yazalım.


```r
#üs alma
üs_al<-  function(x,us){
  return(x^us)
  }
üs_al(3,4)
```

```
[1] 81
```


Argümanlardan birine olağan değer girilmesi


```r
#üs alma
üs_al<-  function(x,us=2){
  return(x^us)
  }
üs_al(3) # us argumanin olagan degeri olan 2 olduğu için argumana deger girilmediginde kare alir.
```

```
[1] 9
```


## Fonksiyon nedir?

Aşağıdaki fonksiyona 3 ve 4 değerleri girilirse çıktı ne olur?


```r
myfunc <-  function(x,y)
{
a <-  x+y
b <-  x* y
return(a*b)
}
myfunc(3,4)
```


## Fonksiyon nedir?

`mean()` fonksiyonu en sık kullandığımız fonksiyonlardan biridir.


```r
x <-  c(1,2,3)
mean(x)
```

```
[1] 2
```


## Fonksiyon nedir?

.pull* left[

R base pakette yer alan bu fonksiyonu kendiniz de yazabilirsiniz. 
R' da deneyim kazandıkça, yaptığınız işlemler karmaşıklaştıkça 
kendi fonksiyonlarınızı yazma ihtiyacı duyacaksınız.

`avg()` isminde vektör ortalaması hesaplayan fonksiyon yazınız.


]

.pull* right[

Yazdığınız fonksiyon ile aşağıdaki işlemi yapınız.


```r
x <-  1:1000
avg(x)
```

```
[1] 500.5
```

Yazdığınız fonksiyon temel pakette yer alan `mean()` fonksiyonu ile ayni sonucu verdi mi?


```r
identical(avg(x),mean(x))
```

```
[1] TRUE
```
]


## Fonksiyon nedir?

*  Fonksiyon içinde tanımlanan nesneler çalışma alanına kaydedilmezler.

*  Fonksiyonlar da R nesnesidir.



```r
ls()
```

```
 [1] "a"                 "alan"              "avg"              
 [4] "backtick"          "boy"               "en"               
 [7] "fonksiyonlar"      "hl"                "kare_al"          
[10] "kosegen"           "path"              "pkg"              
[13] "psyteachr_colors"  "psyteachr_colours" "sayi"             
[16] "üs_al"             "x"                 "y"                
```


## R Çalışma Alanı

* çalışma alanı, nesnelerin ve bilgilerin kaydedildiği alandır.



* `ls()` ve `objects()` fonksiyonları çalışma alanında kayıtlı nesneleri konsolda göstermektedir.



* `ls()` fonksiyonu ile nesneleri çağırma işlemi özelleştirilebilir.



* `ls.str()` fonksiyonu ise hafızadaki nesneleri ayrıntıları ile göstermektedir.



* Çalışma alanından nesne silmek için `rm("nesneadi")` fonksiyonu kullanılabilir.



* Çalışma alanındaki tüm nesneleri silmek icin **`rm`**`(list=ls())` ya da süpürge işareti kullanılabilir.



* Konsolda yer alan işlemleri silmek için ise: CTRL + L (clear console) ya da süpürge işareti kullanılabilir.


## R Çalışma Dizini

* R yazılımı Start/Baslangic menusu üzerinden çalıştırıldığında çalışma dizini **C:/Users/<kullanici adi>/Documents**



* Çalışma dizinini sorgulamak için kullanılacak olan fonksiyon



* `getwd()` (get working directory)



* Çalışma dizinini değiştirmek için kullanılacak olan fonksiyon



* `setwd()` (set working directory)



* Bu işlem Rstudio menusu **"Session"** sekmesinden ya da **CTRL +Shift + H** tuşları ile de yapılabilmektedir.


## R'i Kapatma


* Kaydet (Save) ya da CTLR + S `dosyadi.R` uzantısıyla kaydedilebilmektedir.



* Bu sayede tekrar kullanılabilmekte ya da başkaları ile kolaylıkla paylaşılabilmektedir.



* Tüm programlar gibi **"x"** işareti ile ya da **q()** fonksiyonunu ile sonlandırılabilir.

* R'dan çıkış yaparken, program çalışma alanının kaydedilip kaydedilmeyeceğini sormaktadır.



* Eger R'in çalışma alanını kaydetmesini istenirse, R çalışma dizinine `.Rdata uzantılı bir dosya kaydeder.
* Çalışma alanı kaydı için `save.image("dosyaadi")` komutu da kullanılabilmektedir.
* R'dan çıkış yapmadan yapılan işlem durdurulmak istenirse, konsol bölümündeki **"Stop"** işareti veya **Esc** tuşları kullanılabilir.



## R Kaynakları

* 🔗[Alana ozgu paketler](https://cran.r* project.org/web/views/Psychometrics.html)
* Paket yardım sayfaları ve paket vignetteleri
* e* posta gruplarindaki e* postalara `RSiteSearch ("sample.int")` "
* `ltm reliability` gibi fonskiyon isimler argumansiz kullanirlirsa icerigi gorunur. Karmasik gorunse de siz de yapabilirsiniz. Ogrenmek icin iyi bir yoldur.
* 🔗[https://www.learnr4free.com/tr/index.html](https://www.learnr4free.com/tr/index.html){.uri}
* 🔗[Referans kartları](http://cran.r* project.org/doc/contrib/Short* refcard.pdf)
* 🔗[Cheat Sheets](https://www.rstudio.com/resources/cheatsheets/)
* 🔗[Hadley Wickham](http://adv* r.had.co.nz/)
*   🔗[rforstats](http://r4stats.com/)
* 🔗[r is hot](https://blog.revolutionanalytics.com/r* is* hot/)
* 🔗[paralel programlama](http://www.matthewckeller.com/)




## Kaynaklar

Atar, B., Atalay Kabasakal, K, Ünsal Özberk, E. B., Özberk, E. H. Ve Kıbrıslıoğlu Uysal, N. (2020). R ile Veri Analizi ve Psikometri Uygulamaları, Editör, Pegem Akademi, Ankara.


## Ödev 

*  Sadece temel pakette 1500'e yakın fonksiyon bulunduğu için ders dışı alıştırmalar yapmanız gereklidir.

*  [R kurulumu ile ilgili](https://learnr* examples.shinyapps.io/ex* setup* r/#section* welcome) learnr paketi hazırlanmış bir interaktif alıştırma örneğini inceleyeniz.


* Kitap Bölüm 1 alıştırmalarını tamamlayınız.

* Datacamp da üzerine atanan bölüm alıştırmalarını tamamlayınız.

*  swirl package *  learn R in R paketi yükleyerek alıştırma yapmayı deneyiniz.

*  [Referens kart](https://cran.r* project.org/doc/contrib/Short* refcard.pdf) sayfasının çıktısını alarak duvarınıza asmanızı öneririm. 



## **S1** 

* İki farklı kişisel tanımlı fonksiyon yazabilirsiniz. Fonksiyon1, kullanıcının girdiği harfle başlayan çalışma alanındaki nesneleri listelesin. Fonksiyon2, kullanıcının girdiği harfi içeren çalışma alanındaki nesneleri listelesin. Eğer kendinizi biraz da zorlamak isterseniz, bu iki işlevi birlikte yapan bir fonksiyon yazmayı deneyebilirsiniz.




.large[.hand[Teşekkürler]]




