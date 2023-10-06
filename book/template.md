---
title: "OLC731" # edit
subtitle: "R YAZILIMI ILE VERI ANALIZI" 
author: "Kubra Atalay Kabasakal" # edit
date: "2023-10-06"
site: bookdown::bookdown_site
documentclass: book
classoption: oneside # for PDFs
geometry: margin=1in # for PDFs
bibliography: [book.bib, packages.bib]
csl: include/apa.csl
link-citations: yes
description: | # edit
  Bu notlar OLC731 dersi için hazırlanmıştır.
url: https://github.com/atalay-k/OLC731 # edit
github-repo: atalay-k/OLC731# edit
cover-image: images/logos/logo.png # replace with your logo
apple-touch-icon: images/logos/apple-touch-icon.png # replace with your logo
apple-touch-icon-size: 180
favicon: images/logos/favicon.ico # replace with your logo
---



::: small_right
<img src="images/logos/logo.png" alt="ADS Hex Logo"/>
:::



# Ders Hakkında {.unnumbered}

Bu dersin amacı, R yazılımını kullanarak veri üzerinde istenilen çok değişkenli istatistiksel ve psikometrik işlemlerin yapılabilmesini sağlamaktır.

Tez ve makale çalışmalarında öğrencilerimizin analizlerini R yazılımı ile hiçbir paket programa ihtiyaç duymadan kendi başlarına yapmalarını sağlamaktır.

(İzlence) [**İzlence**](Izlence.html).

## Eğitmen {.unnumbered}

`<svg aria-hidden="true" role="img" viewBox="0 0 448 512" style="height:1em;width:0.88em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:black;overflow:visible;position:relative;"><path d="M224 256A128 128 0 1 1 224 0a128 128 0 1 1 0 256zM209.1 359.2l-18.6-31c-6.4-10.7 1.3-24.2 13.7-24.2H224h19.7c12.4 0 20.1 13.6 13.7 24.2l-18.6 31 33.4 123.9 36-146.9c2-8.1 9.8-13.4 17.9-11.3c70.1 17.6 121.9 81 121.9 156.4c0 17-13.8 30.7-30.7 30.7H285.5c-2.1 0-4-.4-5.8-1.1l.3 1.1H168l.3-1.1c-1.8 .7-3.8 1.1-5.8 1.1H30.7C13.8 512 0 498.2 0 481.3c0-75.5 51.9-138.9 121.9-156.4c8.1-2 15.9 3.3 17.9 11.3l36 146.9 33.4-123.9z"/></svg>`{=html} [Dr. Kübra Atalay Kabasakal](https://avesis.hacettepe.edu.tr/katalay)

`<svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:1em;width:1em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:black;overflow:visible;position:relative;"><path d="M64 112c-8.8 0-16 7.2-16 16v22.1L220.5 291.7c20.7 17 50.4 17 71.1 0L464 150.1V128c0-8.8-7.2-16-16-16H64zM48 212.2V384c0 8.8 7.2 16 16 16H448c8.8 0 16-7.2 16-16V212.2L322 328.8c-38.4 31.5-93.7 31.5-132 0L48 212.2zM0 128C0 92.7 28.7 64 64 64H448c35.3 0 64 28.7 64 64V384c0 35.3-28.7 64-64 64H64c-35.3 0-64-28.7-64-64V128z"/></svg>`{=html} [kkatalay\@gmail.com](mailto:kkatalay@gmail.com){.email}

`<svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:1em;width:1em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:black;overflow:visible;position:relative;"><path d="M64 112c-8.8 0-16 7.2-16 16v22.1L220.5 291.7c20.7 17 50.4 17 71.1 0L464 150.1V128c0-8.8-7.2-16-16-16H64zM48 212.2V384c0 8.8 7.2 16 16 16H448c8.8 0 16-7.2 16-16V212.2L322 328.8c-38.4 31.5-93.7 31.5-132 0L48 212.2zM0 128C0 92.7 28.7 64 64 64H448c35.3 0 64 28.7 64 64V384c0 35.3-28.7 64-64 64H64c-35.3 0-64-28.7-64-64V128z"/></svg>`{=html} [katalay\@hacettepe.edu.tr](mailto:katalay@hacettepe.edu.tr){.email}

## Kitaplar {.unnumbered}

-   Atar, B., Atalay Kabasakal, K, Unsal Ozberk, E. B., Ozberk, E. H. & Kibrislioglu Uysal, N. (2020). R ile Veri Analizi ve Psikometri Uygulamaları, Pegem Akademi, Ankara.🔗 [📖](https://pegem.net/urun/R-ile-Veri-Analizi-ve-Psikometri-Uygulamalari/60801)


-   Desjardins, C. D., & Bulut, O. (2018). Handbook of educational measurement and psychometrics using R. Boca Raton, FL: CRC Press. 🔗[📖](https://www.routledge.com/Handbook-of-Educational-Measurement-and-Psychometrics-Using-R/Desjardins-Bulut/p/book/9780367734671)

- Demir, E. R Diliyle İstatistik Uygulamaları. Pegem Akademi, Ankara.(2021). 🔗[📖](https://pegem.net/urun/R-Diliyle-Istatistik-Uygulamalari/61912)


## Kaynaklar {.unnumbered}

* Bu ders materyallerine ek olarak, R öğrenmek için bir dizi mükemmel kaynak vardır:

- 🔗 [R kurulumu ile ilgili bilgiler içerir. ](https://psyteachr.github.io/data-skills-v2/installing-r.html)

- 🔗 [R studio ve güncellemeler ile ilgili bilgiler içerir. ](https://psyteachr.github.io/analysis-v2/updating-r-rstudio-and-packages.html)

-   * 🔗[Alana ozgu paketlerini inceleyebilirsiniz ](https://cran.r* project.org/web/views/Psychometrics.html)


-  🔗 📖[R Cookbook](http://www.cookbook-r.com/)

-  🔗📖[Veri Bilimi için R](https://r4ds.had.co.nz/)

* 🔗 👨 [Hadley Wickham](https://hadley.nz/)


-  🔗[StackOverflow soru-cevap platfromu](https://stackoverflow.com/)

-  Twitter'da [#rstats](https://twitter.com/search?f=tweets&q=%23rstats&src=typd) hashtag'ini arayın veya kullanın. 
  
  -  e-posta gruplarındaki e-postalara `RSiteSearch ("sample.int")` "

* 🔗[R ile ilgili farklı ücretsiz kaynakları bulabilirsiniz (kitaplar, videolar, websiteleri). Bu kaynakların bazıları başlangıç seviyesinde.](https://www.learnr4free.com/tr/index.html){.uri}
* 🔗[Referans kartları](https://cran.r-project.org/doc/contrib/Short-refcard.pdf)

* 🔗[Cheat Sheets](https://www.rstudio.com/resources/cheatsheets/)





<!--chapter:end:index.Rmd-->

# R ve Rstudio Temeller

Bu bölümde, **R ve RStudio'nun** nasıl kullanılacağının yanı sıra bazı temel programlama kavramları ve terminolojisi, yaygın tuzaklar, faydalı ipuçları ve nereden yardım alınabileceği konularını ele alacağız. Programlama deneyimi olmayanlar bu bölümü özellikle yararlı bulacaktır, ancak daha önce R kullanmış olsanız bile bazı yararlı ipuçları ve püf noktaları bulabilirsiniz.

<div class="info">
<p>Bu bölüm kendi kodunuzu yazmaya başlayana kadar bir anlam ifade
etmeyebilir:)</p>
<p>Biraz sabretmenizi bekliyorum !</p>
</div>



## R Nedir?

-   R istatistiksel hesaplamalar yapabilen bir programlama dilidir.

-   1996 yılında Auckland Universitesi'nde **R**oss Ihaka ve **R**obert Gentleman tarafından geliştirilmiştir.

-   1960 yılında Bell Laboratories'de John Chambers ve arkadaşları tarafından geliştirilen **S dilinin** açık kaynak kodlu halidir.

-   R yazılımı Genel Kamu Lisansi (GNU\* General Public Licence) koşulları altında ücretsiz dağıtılmaktadır.

-   R ve Temel Geliştirme Takımı (R core team) ile ilgili bilgilere R'in internet sitesinden (<https://www.r-project.org/>) ulaşılabilir.

-   R dilinin ilk sürümü 29 Subat 2000 tarihinde yayınlanmıştır. Her iki-üç ayda bir sürümler güncellenmektedir.

    -   [**R version 4.3.1 (Beagle Scouts)**](https://cran.r-project.org/src/base/R-4) has been released on 2023-06-16.

-   RStudio, R ile çalışmayı kolaylaştıran bir Entegre Geliştirme Ortamıdır (Integrated Development Environment[IDE]).

-   Bunu İngilizce bilmek ve kitap yazmak için NotePad gibi düz bir metin editörü kullanmak ile Microsoft Word gibi bir kelime işlemci kullanmak gibi düşünün. Bunu yapabilirsiniz, ancak bu kadar iyi görünmez ve yazım denetimi ve biçimlendirme gibi şeyler olmadan çok daha zor olur. Benzer bir şekilde, **R Studio olmadan da R kullanabilirsiniz ancak bunu tavsiye etmiyorum.**

-   Unutmamanız gereken en önemli şey, bu ders için tüm çalışmalarınızı RStudio kullanarak yapacak olsanız da, aslında iki yazılım parçası kullanıyorsunuz, bu da zaman zaman her ikisinin de **ayrı güncellemeleri** olabileceği anlamına geliyor.

-   R'yi ölçme için kullanmanın iki yolu vardır. İlk olarak, web tarayıcınız aracılığıyla R ve R'nin çevrimiçi bir sürümünü kullanabilirsiniz (**R server/sunucusu)**. İkincisi, R ve RStudio'yu dizüstü veya masaüstü bilgisayarınıza ücretsiz olarak indirip kurabilirsiniz.

## Avantajları

-   R özgür istatiksel bir programlama dilidir.

-   R aynı zamanda bir yorumlayıcıdır (interpreter).

-   R, bir veri tabanı **değildir** ama veri tabanlarına bağlanabilir.

-   Önceki sürümleri kullancı dostu olmasa da, son zamanlarda kod editörlerine çok sayıda işlev eklenmiştir.

-   Ayrıca java gibi diller aracılığı ile ara yüz desteğine sahip bir yazılım geliştirme ortamıdır.

-   Tablolardan oluşan yazılım paketlerine (Excel, Minitab gibi) benzememekle birlikte, yeni geliştiren bazı paketler farklı ara yüzler sağlamaktadır.

-   Ücretsiz olması nedeniyle, ticari desteğe tabi bir yazılım değildir. Ancak destek alınabilecek çok sayıda kaynağa erisilebilir. (stackoverflow, mail listeleri)

## Neden R?

-   R istatistiksel programlama, veri analizi ve grafiksel gösterim için kullanılan ve ticari bir amaç gütmeyen ücretsiz bir yazılımdır.

-   R, UNIX, Windows ve MacOS gibi çeşitli platformlarda kodları derlemekte ve çalıştırmaktadır.

-   SPSS, SAS gibi veri analizi programları ücretlidir, ayrıca bazı özel psikometri analizleri için yeterli değildir.

-   R, açık kaynak kodlu olduğu için program kodlarına istenildiği zaman erişilebilir.

-   Diğer istatistiksel yazılımlar ile karşılaştırıldığında R **komut satırı** ara yüzünü kullanmaktadır.

-   **Basit koşullar, döngüler ve kişi** tanımlı fonksiyonlar yazmaya uyumlu basit ve etkili bir yazım diline sahiptir.

-   R'in ayrıca **grafiksel imkânları** oldukça fazladır; bu nedenle yayınlanabilir/basma uygun grafikler oluşturmak kolaydır.

-   R ekibi birçok alanda ayrıntılı dokümantasyonu yapılmış R paketleri geliştirmektedir.

-   Klasik istatistik yazılımlarında analiz sonuçları bir kez elde edilir. R yazılımında ise sonuçlar çalışma alanına kaydedilerek, ileriki analiz aşamalarında tekrar kullanabilir.

-   R, psikometri alanında sıklıkla kullanılan simülasyon çalışmaları için (tekrarlı işlemler için) de avantaj sağlamaktadır.

-   R, diğer programlama dilleri ve istatistik paket programları ile uyumludur.

## Dezavantajları

-   Basta öğrenilmesi kolay görünse de, R'da uzmanlaşmak oldukça zordur.

-   Menu ile kullanılan programlara alışkın olan kişiler için başlangıçta korkutucu olabilir.

-   R ile bir analizi yapabilmek için planlama yapılması gerekmektedir.

-   R kullanıcıları çoğunlukla programlamacı **değildir.** Programlamaya hâkim olmayan kişiler tarafından hazırlanan, okunması ve sürdürülebilirliği zor kodlar oluşturulabilir.

-   Başlangıçta kodları yazmak yıldırıcı olabilir; ancak çalışmaların tekrarlanabilirliği açısından avantaj sağlamaktadır.

-   Bu duruma bir örnek vermek gerekirse, 20 adet regresyon denklemi kurulup regresyon katsayıları karşılaştırılmak istenirse, R yazılımı sadece regresyon kat sayılarını gösterebilir ve tek bir satırda tüm regresyon sonuçlarını karşılaştırmaya olanak verir. Aynı işlem için diğer istatistiksel yazılımlarda 20 ayrı pencereden elde edilen sonuçların elle yazılarak karşılaştırılması gerekecektir.

-   R'da hata yapma olasılığı diğer programlara göre daha fazladır. Hata kaynağı için varsayımların iyi bilinmesi gerekmektedir.

-   Hız konusunda SPSS ve SAS'a göre avantajlı olsa da diğer dillere göre (Python, Matlab gibi) daha yavaştır.

-   Geliştirilen çok fazla paket olduğu için, ihtiyaca uygun en iyi paketin seçimi zor olabilmektedir.

-   Bu bir dezavantaj gibi görünse de istatistiksel işlemlerin arka planını anlamaya yardımcı olur.

-   Bu tarz zayıf hazırlanmış kodlar farklı koşullarda yavaş çalışabilmektedir.

-   Çoğu kullanıcı bu eksiklikleri gidermek için kodları değiştiremez. Özellikle çok iyi yapılandırılmamış olan kodlar R'da yavaş çalışabilmektedir.

## R ve Rstudio Yüklenmesi

-   Internet tarayıcısına R yazılımın internet sitesinin ana sayfasının adresi yazılır. <https://www.r-project.org/>

-   Sol menüde yer alan "download CRAN" bölümüne tıkladıktan sonra ülke seçilir. Seçilen ülkenin yakınlığı sadece yükleme hızını değiştirecektir.

-   Çıkan sayfada "Download and Install R" baslığı altından işletim sistemine uygun olan bağlantı seçilir.

-   R konsolda çalışmaya doğrudan başlanabilir; ancak konsol kullanımı bir kod editörü olmadığı için çok kullanışlı değildir.

-   Rstudio hata ayıklama, görselleştirme araçları ile birlikte yüklenen modern bir kod editörüdür.

-   <https://www.rstudio.com/> internet sitesinden kullanılan bilgisayar ve işletim sistemine uygun olarak seçilip indirilebilmektedir.

-   Rstudio R ile daha üretken olmanıza yardımcı olacak bir dizi araç içerir, örneğin:

    -   R kodlarınızı vurgulamak için bir sözdizimi vurgulama düzenleyicisi

    -   R kodlarını yazmanıza yardımcı olacak işlevler (otomatik tamamlama)

    -   Çeşitli grafikler oluşturmak ve kaydetmek için çeşitli araçlar (ör. histogramlar, dağılım grafiği)

    -   Verileri içe veya dışa aktarmak için bir çalışma alanı yönetim aracı

## Diğer Gerekli Yüklemeler

-   Benim açıklamalarım yetmediyse R'yi bilgisayarınızda kullanmak için, lütfen daha ayrıntılı talimatlar ve indirmeniz gereken dosyaların bağlantılarının yanı sıra R'yi farklı bilgisayar türlerine yüklemek için bir dizi kılavuza bağlantılar içeren [Installing R](https://psyteachr.github.io/data-skills-v1/installing-r.html) adresine bakın!!

-   Yüklemeler konusunda daha da fazlasına ihtiyacımız var ise [R studio R](https://psyteachr.github.io/data-skills-v1/appendix-updating-r.html) !

-   Verilen linkte yer alsa da ayrıca eklemeye ihtiyaç duyduğum bağlantılar:

-   [Java](https://javadl.oracle.com/webapps/download/AutoDL?BundleId=245479_4d5417147a92418ea8b615e228bb6935)

-   [Rtools](https://cloud.r-project.org/bin/windows/Rtools/) Rtools, kaynak koddan derleme yapmaya yarayan araçları içeren bir R yardımcısıdır. **Önemli:** Eğer Windows kullanıyorsanız, ayrıca Rtools yüklemeniz gerekir.

-   devtools


```r
install.packages("devtools")
```

## R STUDIO

-   Rstudio'da panellerin yerlerini değiştirebiliriz.

-   Bunun yanı sıra yazı tipi, büyüklüğü gibi özellikleri de değiştirebiliriz.

-   Varsayılan olarak, R Studio'yu açtığınızda, kodunuz ve oluşturduğunuz tüm nesneler dahil olmak üzere en son ne üzerinde çalıştığınızı gösterir. Bu yararlı gibi görünebilir, ancak aslında değerinden daha fazla soruna neden olma eğilimindedir, çünkü yanlışlıkla bir nesnenin eski bir sürümünü kullanma riskiniz olduğu anlamına gelir. R Studio'yu her başlattığınızda yeni bir kopya açacak şekilde ayarları değiştirmenizi öneririz. Bunu `Araçlar` - `Global Seçenekler` seçeneğine tıklayarak ve ardından aşağıdaki gibi görünmesi için kutuların seçimini kaldırarak yapabilirsiniz.

<div class="figure" style="text-align: center">
<img src="images/global_options.jpg" alt="Global options" width="100%" />
<p class="caption">(\#fig:img-options)Global options</p>
</div>

-   Dönem boyunca Rstudio kullanımına aşina olacaksınız. Bu süreci kolaylaştırmak için bağlantıları verilen dökümanlara göz atabilirsiniz.

-   [Rstudio cheatsheet](Kaynaklar/rstudio-ide.pdf)

-   [Oscar Torres\* Reyna tutorial](Kaynaklar/rstudio_tutorial.pdf)

## Hangi R sürümünü kullanmalısınız?

-   R'yi bilgisayarınıza kurmanın avantajı, kullanmak için internete bağlı olmanız gerekmemesi, dosyalarınızı kaydetmenin ve yönetmenin daha kolay olması ve sunucunun çökmesi durumunda sorun yaşanmamasıdır (bu nadirdir, ancak olmuştur).

-   R sunucusunu kullanmanın avantajı, bilgisayarına herhangi bir şey yüklemenize gerek olmaması, sadece web tarayıcınız üzerinden erişebilmenizdir.

-   R'yi yükleyemeyeceğiniz bir bilgisayarınız varsa (örneğin Chromebook) veya R'yi bilgisayarınıza yüklemeyle ilgili ciddi sorunlarınız varsa sunucuyu kullanmanızı öneririz.

## R Studio Hakkında

-   R Studio, kodu deneyebileceğiniz bir konsola sahiptir (Şekil'de sol alt pencerede yer alır\@ref(fig:img-rstudio)).

-   Ayrıca kod editörü (sol üst), "Ortam" sekmesinde oluşturduğunuz fonksiyonları ve nesneleri gösteren bir pencere ( sağ üst pencere) ve grafikleri, dosya paketlerini ve yardım belgelerini gösteren bir pencere ise (sağ alt) bulunur.

<div class="figure" style="text-align: center">
<img src="images/Rstudio.png" alt="RStudio arayüzü" width="100%" />
<p class="caption">(\#fig:img-rstudio)RStudio arayüzü</p>
</div>

-   Bu ders boyunca R Studio'da bulunan özelliklerin nasıl kullanılacağı hakkında daha fazla bilgi edineceksiniz, ancak R Studio ekibinden [RStudio Essentials 1](https://rstudio.com/resources/webinars/programming-part-1-writing-code-in-rstudio/) izlemenizi şiddetle tavsiye ederim. Video yaklaşık 30 dakika sürmekte ve R Studio'nun ana bölümlerini tanıtmaktadır.

## R Temel Özellikler

-   R konsolda görünen **\>** işareti, R yazılımının sizden komut beklediğini belirtir. R'in hesap makinesi olarak kullanım örnekleri sunulmuştur.


```r
2+2
```

```
[1] 4
```

-   R boşluklara duyarlı değildir.


```r
2  +       2 
```

```
[1] 4
```


```r
2+
  2
```

```
[1] 4
```

## Atama Operatoru

-   Atama operatörü olarak "küçüktür" simgesi ile "kısa çizgi" simgesi **`<-`** simgeleri kullanılabilir.

-   **`<-`** yerine "eşittir" **`=`** simgesi de atama operatörü olarak kullanılabilir.

-   Ancak **`=`** operatörü programlama yaparken matematiksel eşitlikle karışabilmektedir.

-   Atama yapılacak nesne isimlendirilirken harflerle (A\* Z veya a\* z) başlamalıdır.

-   İsimlendirmeye harfle başlandıktan sonra rakamlar (0\* 9), nokta (.) ve alt cizgi (\_) ile devam edilebilmektedir.

-   R harflerin küçük ve ya büyük olmasına karşı duyarlıdır.

-   R fonksiyonlarına benzer isimlerde nesne ismi kullanmamaya **dikkat edilmelidir.**

-   Ayrıca **c,C,D,F,I,q,t,T** gibi tek harfli nesne ismi kullanmaktan kaçınılmalıdır; bunların R'da özel anlamları bulunmaktadır.

-   R yazılımında **\#** işareti ile başlayan satır, yorum satırıdır.

-   Genellikle komutların anlamını açıklamak için kullanılmaktadır.

-   R, bu satırları dikkate almaz, bunlar sadece kullanıcılar için bilgi ve hatırlatıcı açıklamaları içermektedir.


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

-   toplama işlemi için **+**,

-   çıkarma işlemi için **-**,

-   çarpma işlemi için **\***,

-   bölme işlemi için **/**,

-   üs alma işlemi için **\^** veya \*

-   mod alma icin ise **%%** operatorleri kullanılmaktadır.

-   Kodlamanızın büyük bir kısmı nesne oluşturmayı ve nesneleri manipüle etmeyi içerecektir. Nesneler bir şeyler içerir. Bu şeyler sayılar, kelimeler veya işlemlerin ve analizlerin sonucu olabilir

**Alıştırma Nesneler oluşturma**

-   Aşağıdaki kodu kopyalayıp konsola yapıştırın, kodu kendi adınızı ve yaşınızı kullanacak şekilde değiştirin ve çalıştırın. Enviroment bölmesinde `ad`, `yas`, `gun`, `yeniyil` ve `veri` nesnelerinin göründüğünü göreceksiniz.


```r
ad <- "ada"
yas <- 16 + 20 
gun <-Sys.Date()
yeniyil <- as.Date("2024-01-01")
veri <- rnorm(n = 10, mean = 15, sd = 3)
```

<div class="figure" style="text-align: center">
<img src="images/objects-enviro.png" alt="Calisma alanındaki nesneler" width="100%" />
<p class="caption">(\#fig:img-objects-enviro)Calisma alanındaki nesneler</p>
</div>

-   Bu örneklerde, `ad`, `yas` ve `yeniyil` her zaman `ada`, `36` değerlerini ve 2024 Yeni Yıl Günü tarihini içerecektir, ancak `gun` tarihi işletim sisteminden alacaktır ve `veri` rastgele oluşturulmuş bir veri kümesi olacaktır, bu nedenle bu nesnelerin değerleri statik olmayacaktır.

-   Daha da önemlisi, nesneler hesaplamalara dahil olabilir ve birbirleriyle etkileşime girebilir. Örneğin:


```r
yas + 10
yeniyil - gun
mean(veri)
```

```
[1] 46
Time difference of 87 days
[1] 14.83186
```

-   Son olarak, bu işlemlerin sonucunu yeni bir nesnede saklayabilirsiniz:


```r
n1 <- yas + 10
```

<div class="try">
<p>&lt;-<code>ifadesini</code>içerir<code>şeklinde okumak faydalı olabilir, örneğin</code>ad<code>ifadesi</code>ada`
metnini içerir.</p>
</div>

-   Bu ders boyunca sürekli olarak nesneler yaratacaksınız ve ilerledikçe onlar ve nasıl davrandıkları hakkında daha fazla bilgi edineceksiniz, ancak şimdilik bunların değerleri kaydetmenin bir yolu olduğunu, bu değerlerin sayı, metin veya işlemlerin sonucu olabileceğini ve yeni değişkenler oluşturmak için başka işlemlerde kullanılabileceğini anlamak yeterlidir.

<div class="info">
<p>Nesnelerin ‘değişkenler’ olarak adlandırıldığını da görebilirsiniz.
Programlama terimlerinde ikisi arasında fark vardır, ancak çok sık
eşanlamlı olarak kullanılırlar.</p>
</div>

**Alıştırma Nesneler oluşturma**

-   Aşağıdaki kodu kopyalayıp konsola yapıştırın.
-   Eni 4 cm, boyu 10 cm bir dikdörtgenin alanı hesaplayınız.


```r
# en nesnesi tanimlama

# boy nesnesi tanimlama

# alan nesnesi tanimlama

# alan nesnesini yazdirma
```


```
[1] 40
```

-   Eni 4 cm, boyu 10 cm bir dikdörtgenin köşegen uzunluğunu hesaplayınız.


```r
# en nesnesi tanimlama

# boy nesnesi tanimlama

# kosegen nesnesi tanimlama

# kosegen nesnesini yazdirma
```


```
[1] 10.77033
```

### Ödev

Datacamp hesapınızda yer alan 🔗 datacamptan size atanan bölümü tamamlayınız ve kitabın ilk bölümünü tamamlayınız.

<!--chapter:end:01-Kurulum.Rmd-->

# R Paketler

- R'yi yüklediğinizde, veri işleme ve istatistiksel analiz seçenekleri de dahil olmak üzere bir dizi fonksiyona erişebilirsiniz. Varsayılan kurulumda yer alan fonksiyonlar genellikle **Temel R/Base R** olarak adlandırılır ve birçok Temel R fonksiyonunu gösteren faydalı bir cheatsheet sayfası vardır 🔗[cheatsheet](https://github.com/rstudio/cheatsheets/raw/main/base-r.pdf) 

- **Temel R**  telefonunuzda gelen varsayılan uygulamalar, paketleri ise ayrıca indirmeniz gereken ek uygulamalar olarak düşünmek faydalı olabilir.

*  R fonksiyonları **ayrı paketler** halinde düzenlenmişlerdir. Böylece gerekli paketlerle çalışarak daha az bellek kullanımı ve hızlı işlem gücü sağlanır.

*  Bu paketlerin bir başka avantajı da yazılan fonksiyonlardan oluşan paketlerin CRAN'den temin edilerek yüklenebilmesidir.

*  Her paketin bir yaratıcısı ve kendisine ait bir yardım dosyası bulunur.


```r
# paket yukleme
install.packages("CTT")
# paket aktive etme
library(CTT)
```
*  Paket yükleme işlemi Rstudio'da yer alan menüler aracılığı ile de yapılabilmektedir.


*  R paketleri R fonksiyonlarının, verilerinin ve iyi derlenmiş bir formatta kodların kombinasyonlarından oluşmaktadır. `library()` komutu ile kişisel kütüphanenizdeki yüklü paketleri görebilirsiniz.

*   Sadece temel pakette 1000'den fazla fonksiyon bulunmaktadır.


```r
# temel paket fonksiyonlarina ulasimak icin  
fonksiyonlar <-  builtins()
length(fonksiyonlar)
```

```
## [1] 1380
```


```r
fonksiyonlar[910:920]
```

```
##  [1] "Cstack_info"                "crossprod"                 
##  [3] "cospi"                      "cosh"                      
##  [5] "cos"                        "contributors"              
##  [7] "Conj"                       "conflicts"                 
##  [9] "conflictRules"              "conditionMessage.condition"
## [11] "conditionMessage"
```



![yükle-etkinleştir](images/packagebulb.png){width=70%}


### Alıştırma :  tidyverse yükleme

- Bir paketi kullanabilmek için önce onu yüklemeniz gerekir. Aşağıdaki kod, bu derste çok sık kullanacağımız bir paket olan `tidyverse` paketini yükler.


```r
install.packages("tidyverse")
```

- Bir paketi yalnızca bir kez yüklemeniz gerekir, ancak R'yi her başlattığınızda kullanmak istediğiniz paketleri yüklemeniz gerekir, benzer şekilde telefonunuza bir uygulamayı bir kez yüklemeniz gerekir, ancak her kullanmak istediğinizde açmanız gerekir.

<div class="info">
<p><strong>UYARI: WARNING: Rtools is required to build R packages” gibi
bir hata mesajı alırsanız, [Rtools]
(https://cran.r-project.org/bin/windows/Rtools/) adlı ekstra bir yazılım
indirmeniz ve yüklemeniz gerekebilir.</strong></p>
</div>


### Alıştırma : tidyverse etkinleştir

* Tidyverse'i etkinleştirmek için aşağıdaki kodu çalıştırın.  


```r
library(tidyverse)
```

- Bir hata mesajı gibi görünen bir şey alacaksınız - öyle değil. Bu sadece R'nin size ne yaptığını anlatmasıdır.

- Şimdi `tidyverse` paketini etkinleştirdiğimize göre, içerdiği fonksiyonlardan herhangi birini kullanabiliriz, ancak unutmayın, R'yi her başlattığınızda `library()` fonksiyonunu çalıştırmanız gerekir.

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


## Paket çakışmaları {#conflicts}

- Daha da fazla fonksiyona sahip binlerce farklı R paketi vardır. Ne yazık ki, bazen farklı paketler aynı fonksiyon isimlerine sahiptir. Örneğin, `dplyr` ve `MASS` paketlerinin her ikisi de `select()` adında bir fonksiyona sahiptir. Bu paketlerin her ikisini de yüklerseniz, R size bir çakışma olduğunu söyleyen bir uyarı üretecektir.


```r
library(dplyr)
library(MASS)
```

```
## 
## Attaching package: 'MASS'
```

```
## The following object is masked from 'package:dplyr':
## 
##     select
```

- Bu durumda, R size `dplyr` paketindeki `select()` fonksiyonunun aynı isimli başka bir fonksiyon tarafından gizlendiğini (veya 'maskelendiğini') söylüyor. Eğer `select()` fonksiyonunu kullanmayı deneseydiniz, R en son yüklenen paketteki fonksiyonu kullanacaktı - bu durumda `MASS` fonksiyonunu kullanacaktı.

- Belirli bir fonksiyon için hangi paketi kullanmak istediğinizi belirtmek istiyorsanız, örneğin `package::function` biçiminde kod kullanabilirsiniz:


```r
dplyr::select()
MASS::select()
```

## Paket Güncelleme

- R ve R Studio güncellemelerine ek olarak, paketlerin yazarları da bazen kodlarını günceller. Bu, bir pakete fonksiyon eklemek için olabileceği gibi hataları düzeltmek için de olabilir. **Kaçınılması gereken bir şey, yüklü bir paketi istemeden güncellemektir.**

- `install.packages()` fonksiyonunu çalıştırdığınızda, her zaman paketin en son sürümü yüklenir ve yüklemiş olabileceğiniz eski sürümlerin üzerine yazılır. Bazen bu bir sorun teşkil etmez, ancak bazen paket önemli ölçüde değiştiği için güncellemenin kodunuzun artık çalışmadığı anlamına geldiğini görürsünüz. Bir paketin eski bir sürümüne geri dönmek mümkündür ancak yine de bundan kaçınmaya çalışın.

<div class="info">
<p>Bir paketin üzerine yanlışlıkla daha sonraki bir sürümün yazılmasını
önlemek için, sizin veya bir başkasının kodu yanlışlıkla çalıştırması
ihtimaline karşı analiz komut dosyalarınıza
<code>install.packages()</code> i <strong>asla</strong> dahil
etmemelisiniz.</p>
</div>


## R ve RStudio'ya nasıl alıntı yapılır

- R'a atıfta bulunmanız ve referans vermeniz gereken bilimsel bir rapor yazmaktan biraz uzak olabilirsiniz, ancak zamanı geldiğinde bunu onu geliştiren insanlara (çoğu ücretsiz!) kredi vermek için yapmak önemlidir. R, RStudio ve kullandığınız paketler için ayrı alıntılar sağlamalısınız.

- Kullandığınız R sürümü için atıf almak için, size her zaman en son atıfı sağlayacak olan `citation()` fonksiyonunu çalıştırmanız yeterlidir.


```r
citation()
```

```
## 
## To cite R in publications use:
## 
##   R Core Team (2022). R: A language and environment for statistical
##   computing. R Foundation for Statistical Computing, Vienna, Austria.
##   URL https://www.R-project.org/.
## 
## A BibTeX entry for LaTeX users is
## 
##   @Manual{,
##     title = {R: A Language and Environment for Statistical Computing},
##     author = {{R Core Team}},
##     organization = {R Foundation for Statistical Computing},
##     address = {Vienna, Austria},
##     year = {2022},
##     url = {https://www.R-project.org/},
##   }
## 
## We have invested a lot of time and effort in creating R, please cite it
## when using it for data analysis. See also 'citation("pkgname")' for
## citing R packages.
```

- Kullandığınız herhangi bir paket için atıf oluşturmak için, atıf yapmak istediğiniz paketin adıyla birlikte `citation()` işlevini de kullanabilirsiniz.


```r
citation("tidyverse")
```

```
## 
## To cite package 'tidyverse' in publications use:
## 
##   Wickham H, Averick M, Bryan J, Chang W, McGowan LD, François R,
##   Grolemund G, Hayes A, Henry L, Hester J, Kuhn M, Pedersen TL, Miller
##   E, Bache SM, Müller K, Ooms J, Robinson D, Seidel DP, Spinu V,
##   Takahashi K, Vaughan D, Wilke C, Woo K, Yutani H (2019). "Welcome to
##   the tidyverse." _Journal of Open Source Software_, *4*(43), 1686.
##   doi:10.21105/joss.01686 <https://doi.org/10.21105/joss.01686>.
## 
## A BibTeX entry for LaTeX users is
## 
##   @Article{,
##     title = {Welcome to the {tidyverse}},
##     author = {Hadley Wickham and Mara Averick and Jennifer Bryan and Winston Chang and Lucy D'Agostino McGowan and Romain François and Garrett Grolemund and Alex Hayes and Lionel Henry and Jim Hester and Max Kuhn and Thomas Lin Pedersen and Evan Miller and Stephan Milton Bache and Kirill Müller and Jeroen Ooms and David Robinson and Dana Paige Seidel and Vitalie Spinu and Kohske Takahashi and Davis Vaughan and Claus Wilke and Kara Woo and Hiroaki Yutani},
##     year = {2019},
##     journal = {Journal of Open Source Software},
##     volume = {4},
##     number = {43},
##     pages = {1686},
##     doi = {10.21105/joss.01686},
##   }
```

- Kullandığınız RStudio sürümüne ait alıntıyı oluşturmak için `RStudio.Vesion()` fonksiyonunu kullanabilirsiniz:


```r
RStudio.Version()
```

- Son olarak, yöntem bölümünüzün yazımında bunun nasıl görünebileceğine dair bir örnek:

> Analiz R (R Core Team, 2020), RStudio (Rstudio Team, 2020) ve tidyverse paketi (Wickham, 2017) kullanılarak gerçekleştirilmiştir.

- Belirtildiği gibi, bunu bir süre yapmak zorunda kalmayabilirsiniz, ancak yaptığınızda buna geri dönün çünkü açık kaynak topluluğuna çalışmaları için kredi vermek önemlidir.

<!--chapter:end:02-paketler.Rmd-->

# Fonksiyonlar

* Fonksiyon belli bir görevi yerine getirmek için yazılan bir grup komuttur.

* Fonksiyonların çalışması için girdilerinin olması gerekmektedir. Fonksiyonlar girdileri ile yaptıkları işlem sonucunda bir çıktı oluştururlar.

* Fonksiyonlar girdileri o fonksiyonun çalışması için önceden belirlenen **argümanlar** ve o argümanların değerlerinden oluşur. (dilbilimle ilgileniyorsanız, bunları bir özne ve nesne gerektiren fiiller olarak düşünmek isteyebilirsiniz)

* Fonksiyonların kullanımında üç noktaya dikkat edilmelidir.

  1.  argümanların sırası
  2.  argümanların olağan (default) değerleri
  3.  bazı argümanların zorunlu, bazı argümanların opsiyonel olmasıdır

- Bir fonksiyonun aldığı tüm argümanlara yardım dokümantasyonunu kullanarak `?function` formatını kullanarak bakabilirsiniz. Bazı argümanlar zorunlu, bazıları ise isteğe bağlıdır. İsteğe bağlı bağımsız değişkenler, herhangi bir değer girmezseniz genellikle varsayılan/olağan (normalde yardım belgelerinde belirtilen) bir değer kullanır.

- Örnek olarak, normal dağılıma sahip bir sayı kümesini rastgele üreten `rnorm()` fonksiyonunun yardım belgelerine bakalım. 

- Bir fonksiyonun aldığı tüm argümanlara yardım dokümantasyonunu kullanarak `?function` formatını kullanarak bakabilirsiniz. Bazı argümanlar zorunlu, bazıları ise isteğe bağlıdır. İsteğe bağlı bağımsız değişkenler, herhangi bir değer girmezseniz genellikle varsayılan/olağan (normalde yardım belgelerinde belirtilen) bir değer kullanır.

**Alıştırma **

* R Studio'yu açın ve konsola aşağıdaki kodu yazın:  


```r
?rnorm
```

- `rnorm()` için yardım belgeleri sağ alt yardım panelinde görünmelidir. Kullanım bölümünde, `rnorm()`un aşağıdaki formu aldığını görüyoruz:


```r
rnorm(n, mean = 0, sd = 1)
```

- Argümanlar bölümünde, her bir argüman için açıklamalar bulunmaktadır. `n` oluşturmak istediğimiz gözlem sayısı, `mean` oluşturacağımız veri noktalarının ortalaması ve `sd` verinin standart sapmasıdır. Ayrıntılar bölümünde, `mean` ve `sd` için herhangi bir değer girilmezse, bu değerler için varsayılan olarak 0 ve 1 kullanılacağı belirtilir. `n` için varsayılan bir değer olmadığından, belirtilmesi gerekir, aksi takdirde kod çalışmaz.

- Bir örnek deneyelim ve R'den 5 rastgele sayı üretmesini istemek için gerekli `n` argümanını değiştirelim. 

**Alıştırma II**

* Aşağıdaki kodu kopyalayıp konsola yapıştırın.  


```r
set.seed(12042016)
rnorm(n = 5)
```

```
## [1] -0.2896163 -0.6428964  0.5829221 -0.3286728 -0.5110101
```

- Bu sayıların ortalaması 0 ve SD'si 1'dir. Şimdi farklı bir sayı kümesi üretmek için ek argümanları değiştirebiliriz.


```r
rnorm(n = 5, mean = 10, sd = 2)
```

```
## [1] 13.320853  9.377956 10.235461  9.811793 13.019102
```

- Bu kez R yine 5 rastgele sayı üretti, ancak şimdi bu sayı kümesi belirtildiği gibi 10 ortalama ve 2 sd değerine sahip. Bir fonksiyonun hangi argümanları gerektirdiğini anlamanıza yardımcı olması için yardım belgelerini kullanmayı her zaman unutmayın.


<div class="info">
<p>Eğer internette kod örneklerine bakıyorsanız, sık sık
<code>set.seed()</code> fonksiyonu ile başlayan kodlar görebilirsiniz.
Bu fonksiyon rastgele sayı üretecini kontrol eder - rastgele sayı üreten
herhangi bir fonksiyon kullanıyorsanız (<code>rnorm()</code> gibi),
<code>set.seed()</code> fonksiyonunu çalıştırmak aynı sonucu almanızı
sağlayacaktır (bazı durumlarda yapmak istediğiniz şey bu olmayabilir).
Bu örnekte <code>set.seed()</code> diyoruz, bu aynı rastgele sayıları
alacağınız anlamına geliyor.</p>
</div>

## Argüman isimleri

- Yukarıdaki örneklerde, kodumuzdaki bağımsız değişken adlarını yazdık (örneğin, `n`, `mean`, `sd`), ancak bu kesinlikle gerekli değildir. Aşağıdaki iki kod satırının her ikisi de aynı sonucu üretecektir (`rnorm()` fonksiyonunu her çalıştırdığınızda rastgele olduğu için biraz farklı bir sayı kümesi üretecektir, ancak yine de aynı ortalama ve SD'ye sahip olacaklardır):


```r
rnorm(n = 6, mean = 3, sd = 1)
rnorm(6, 3, 1)
```

- Önemli olarak, eğer argüman isimlerini yazmazsanız, R argümanların varsayılan sırasını kullanacaktır, yani `rnorm` için girdiğiniz ilk sayının `n` olduğunu varsayacaktır. ikinci sayı `mean` ve üçüncü sayı `sd`dir. 

- Eğer argüman isimlerini yazarsanız, argümanları istediğiniz sırada yazabilirsiniz:


```r
rnorm(sd = 1, n = 6, mean = 3)
```

- R'yi ilk öğrenirken, fonksiyonun her bir parçasının ne yaptığını hatırlamanıza ve anlamanıza yardımcı olabileceğinden, argüman adlarını yazmayı yararlı bulabilirsiniz. Ancak, becerileriniz ilerledikçe argüman adlarını atlamayı daha hızlı bulabilirsiniz ve ayrıca argüman adlarını kullanmayan çevrimiçi kod örnekleri göreceksiniz, bu nedenle her bir kod parçasının hangi argümana atıfta bulunduğunu anlayabilmek önemlidir (veya kontrol etmek için yardım belgelerine bakın).

- Bu derste, her bir fonksiyonu ilk kez kullandığımızda argüman adlarını her zaman yazacağız, ancak sonraki kullanımlarda bunlar atlanabilir.


## TAB ile otomatik tamamlama

- R Studio'nun çok kullanışlı bir özelliği, fonksiyonlar için TAB otomatik tamamlama özelliğidir (bkz. Şekil \@ref(fig:img-autocomplete)). Fonksiyonun adını yazıp tab tuşuna basarsanız, R Studio size fonksiyonun aldığı argümanları kısa bir açıklama ile birlikte gösterecektir. Argüman adının üzerinde enter tuşuna basarsanız, tıpkı telefonunuzdaki otomatik tamamlama gibi adı sizin için dolduracaktır. Bu, R'yi ilk öğrenirken inanılmaz derecede kullanışlıdır ve bu özelliği sık sık kullanmayı **unutmamalısınız.** 

<div class="figure" style="text-align: center">
<img src="images/autocomplete.png" alt="Tab ile otomatik durdurma" width="100%" />
<p class="caption">(\#fig:img-autocomplete)Tab ile otomatik durdurma</p>
</div>
## Kişisel tanımlı fonksiyon

- Kişisel tanımlı fonksiyon yazılması şablonu aşağıdaki gibidir.


```r
fonksiyonadi<-  function(argumanlar ve olagan degerleri){
  kodlar
  return()
}
```

- Oluşturulan fonksiyon çalıştırılırken ise aşağıdaki şeklinde çalıştırılır.


```r
fonksiyonadi(argumanlar ve degerleri)
```

*  Kare alma işlemi aşağıdaki şekilde yapılabilir.


```r
sayi <-  4
sayi * sayi
sayi ^2
```

```
## [1] 16
## [1] 16
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
## [1] 16
```


- Farklı dereceden üsler alabilen bir fonksiyon yazalım.


```r
#üs alma
üs_al<-  function(x,us){
  return(x^us)
  }
üs_al(3,4)
```

```
## [1] 81
```

- Argümanlardan birine olağan değer girilmesi


```r
#üs alma
üs_al<-  function(x,us=2){
  return(x^us)
  }
üs_al(3) # us argumanin olagan degeri olan
# 2 olduğu için argumana 
# deger girilmediginde kare alir.
```

```
## [1] 9
```


- Aşağıdaki fonksiyona 3 ve 4 değerleri girilirse çıktı ne olur?


```r
myfunc <-  function(x,y)
{
a <-  x+y
b <-  x* y
return(a*b)
}
myfunc(3,4)
```


- `mean()` fonksiyonu en sık kullandığımız fonksiyonlardan biridir.


```r
x <-  c(1,2,3)
mean(x)
```

```
## [1] 2
```


- R base pakette yer alan bu fonksiyonu kendiniz de yazabilirsiniz. 
- R' da deneyim kazandıkça, yaptığınız işlemler karmaşıklaştıkça 
kendi fonksiyonlarınızı yazma ihtiyacı duyacaksınız.

- `avg()` isminde vektör ortalaması hesaplayan fonksiyon yazınız.




- Yazdığınız fonksiyon ile aşağıdaki işlemi yapınız.


```r
x <-  1:1000
avg(x)
```

```
## [1] 500.5
```

- Yazdığınız fonksiyon temel pakette yer alan `mean()` fonksiyonu ile aynı sonucu verdi mi?


```r
identical(avg(x),mean(x))
```

```
## [1] TRUE
```

*  Fonksiyon içinde tanımlanan nesneler çalışma alanına kaydedilmezler.

*  Fonksiyonlar da R nesnesidir.



```r
ls()
```

```
##  [1] "avg"               "backtick"          "hl"               
##  [4] "kare_al"           "path"              "pkg"              
##  [7] "psyteachr_colors"  "psyteachr_colours" "sayi"             
## [10] "üs_al"             "x"
```


## R Çalışma Alanı

* çalışma alanı, nesnelerin ve bilgilerin kaydedildiği alandır.

* `ls()` ve `objects()` fonksiyonları çalışma alanında kayıtlı nesneleri konsolda göstermektedir.

* `ls()` fonksiyonu ile nesneleri çağırma işlemi özelleştirilebilir.


* `ls.str()` fonksiyonu ise hafızadaki nesneleri ayrıntıları ile göstermektedir.




- Çok fazla kod yazıyorsanız, enviroment (veya çalışma alanının) birçok nesne ile darmadağın olduğunu fark edebilirsiniz. Bu, hangi nesneye ihtiyacınız olduğunu bulmanızı zorlaştırabilir ve bu nedenle yanlış veri seti kullanma riskiyle karşı karşıya kalabilirsiniz. Yeni bir veri kümesi üzerinde çalışıyorsanız veya son sürümü elde etmeden önce çok sayıda farklı kod denediyseniz, yanlış nesneyi kullanmaktan kaçınmak için ortamı/çalışma alanını temizlemeyi unutmamak iyi bir uygulamadır. Bunu birkaç şekilde yapabilirsiniz.

1. Nesneleri tek tek kaldırmak için konsola `rm(nesne_adı)` yazabilirsiniz. Önceki bölümde oluşturduğunuz nesnelerden birini kaldırmak için bunu şimdi deneyin. 
2. Ortamdaki tüm nesneleri temizlemek için konsolda `rm(liste = ls())` komutunu çalıştırın.
3. Ortamdaki tüm nesneleri temizlemek için ortam bölmesindeki süpürge simgesine de tıklayabilirsiniz. 

4. Konsolda yer alan işlemleri silmek için ise: CTRL + L (clear console) ya da süpürge işareti kullanılabilir.


<div class="figure" style="text-align: center">
<img src="images/broom.png" alt="Clearing the workspace" width="100%" />
<p class="caption">(\#fig:img-broom)Clearing the workspace</p>
</div>


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




## R oturumları

- R'yi açıp kod yazmaya, paketleri yüklemeye ve nesneler oluşturmaya başladığınızda, bunu yeni bir **oturumda** yaparsınız. Çalışma alanını temizlemeye ek olarak, bazen yeni bir oturum başlatmak yararlı olabilir. Bu, bilgisayarınızda R'yi her başlattığınızda otomatik olarak gerçekleşir, ancak oturumlar sunucuda kalıcı olabilir. Kodunuzun çalışmadığını fark ederseniz ve nedenini bulamazsanız, yeni bir oturum başlatmaya değer olabilir. Bu, ortamı temizleyecek ve yüklü tüm paketleri ayıracaktır - bunu telefonunuzu yeniden başlatmak gibi düşünün.

## Alıştırma

'Oturum - R'yi Yeniden Başlat'a tıklayın. 

<div class="figure" style="text-align: center">
<img src="images/new_session.png" alt="The truth about programming" width="100%" />
<p class="caption">(\#fig:img-session)The truth about programming</p>
</div>

## Hata ayıklama ipuçları

- Kodlamanın büyük bir kısmı kodunuzun neden çalışmadığını anlamaya çalışmaktır ve bu acemi ya da uzman olmanız fark etmeksizin geçerlidir. 

- Bu ders boyunca ilerlerken yaptığınız hataların ve bunları nasıl düzelttiğinizin kaydını tutmalısınız. 

- Her bölümde dikkat etmeniz gereken bir dizi yaygın hata sunacağız, ancak şüphesiz kendiniz de yeni hatalar yapacaksınız (ve düzelteceksiniz!).

* Kullanmaya çalıştığınız fonksiyonlar için doğru paketleri yüklediniz mi? Çok yaygın bir hata, paketi yüklemek için kodu yazmaktır, örneğin `library(tidyverse)` ancak daha sonra çalıştırmayı unutmaktır.

* Bir yazım hatası mı yaptınız? Unutmayın `data` ile `DATA` aynı şey değildir ve `t.test` ile `t_test` aynı şey değildir.

* Bir paket çakışması mı var? Paket ve fonksiyonu `package::function` ile belirtmeyi denediniz mi?

* Bu kesinlikle bir hata mı? R'deki tüm kırmızı metinler hata anlamına gelmez - bazen size sadece bilgi içeren bir mesaj verir. 

## Yardımcı Kaynaklar


Programlamada iyi olmak demek, bir şeyler denemek, internette yardım aramak ve kopyalanacak kod örnekleri bulmak demektir. 

-  etkili bir şekilde problem çözmeyi öğrenmek, bu kurs boyunca geliştirmeniz gereken temel bir beceridir. 

* Yardım belgelerini kullanın. Bir fonksiyonun nasıl çalıştığını anlamakta zorlanıyorsanız, `?function` komutunu hatırlayın.

* Bir hata mesajı alırsanız, kopyalayıp Google'a yapıştırın - büyük olasılıkla başka biri de aynı sorunu yaşamıştır.

* Bu ders materyallerine ek olarak, R öğrenmek için bir dizi mükemmel kaynak vardır:

  * [R Cookbook](http://www.cookbook-r.com/)
  * [StackOverflow](https://stackoverflow.com/)
  * [Veri Bilimi için R](https://r4ds.had.co.nz/)
  * Twitter'da [#rstats](https://twitter.com/search?f=tweets&q=%23rstats&src=typd) hashtag'ini arayın veya kullanın
  
  

## Alıştırma : Kendini test et

**Soru 1.** Neden `install.packages()` kodunu analiz kodlarında asla dahil **etmemelisiniz**? <select class='webex-select'><option value='blank'></option><option value=''>Bunun yerine library() kullanmalısınız</option><option value=''>Paketler zaten temel R'ın bir parçasıdır</option><option value='answer'>Siz (veya bir başkası) yanlışlıkla kodunuzun çalışmasını durduran bir paket güncellemesi yükleyebilirsiniz</option><option value=''>Paketin en son sürümüne zaten sahipsiniz</option></select> 


<div class='webex-solution'><button>Açıklama</button>

Unutmayın, `install.packages()` işlevini çalıştırdığınızda her zaman paketin en son sürümü yüklenir ve yüklemiş olabileceğiniz eski sürümlerin üzerine yazılır.

</div>
 
<br>
**Soru 2.**Aşağıdaki kod ne üretecektir?
  

```r
rnorm(6, 50, 10)
```


<select class='webex-select'><option value='blank'></option><option value=''>Ortalaması 6 ve SD'si 50 olan 10 sayıdan oluşan bir veri seti</option><option value='answer'>Ortalaması 50 ve SD'si 10 olan 6 sayıdan oluşan bir veri seti</option><option value=''>Ortalaması 10 ve SD'si 6 olan 50 sayıdan oluşan bir veri seti</option><option value=''>Ortalaması 10 ve SD'si 6 olan 50 sayıdan oluşan bir veri seti</option></select>  


<div class='webex-solution'><button>Açıklama</button>

`rnorm()` için varsayılan biçim `rnorm(n, mean, sd)` şeklindedir. Bir fonksiyonun her bir argümanının ne işe yaradığını hatırlamak için yardıma ihtiyacınız varsa, `?rnorm` komutunu çalıştırarak yardım belgelerine bakın

</div>
  
<br>
**Soru 3.** Aynı isimde fonksiyonlara sahip iki paketiniz varsa ve tam olarak hangi paketin kullanılacağını belirtmek istiyorsanız, hangi kodu kullanırsınız? 

<select class='webex-select'><option value='blank'></option><option value='answer'>package::function</option><option value=''>function::package</option><option value=''>library(package)</option><option value=''>install.packages(package)</option></select>  


<div class='webex-solution'><button>Açıklama</button>

Örneğin `dplyr::select` gibi `package::function` biçimini kullanmalısınız. Paketlerinizi ilk yüklediğinizde, herhangi bir fonksiyon aynı isme sahipse R'nin sizi uyaracağını unutmayın - buna dikkat etmeyi unutmayın!

</div>
  


**Soru 4.** Aşağıdakilerden hangisinin bir arguman olması en muhtemeldir? <select class='webex-select'><option value='blank'></option><option value='answer'>35</option><option value=''>read_csv()</option><option value=''><-</option></select>

**Soru 5.** Fonksiyonları oluşturmanın için aşağıdakilerden hangisini kullanmalıyız? <select class='webex-select'><option value='blank'></option><option value=''>()</option><option value=''>[]</option><option value='answer'>{}</option></select>.

**Soru 6.** <-`'nin görevi, fonksiyondan elde edilen çıktıyı bir/bir  ..................... atamaktır. <select class='webex-select'><option value='blank'></option><option value='answer'>nesne</option><option value=''>atama</option><option value=''>arguman</option></select>.



::: {.try data-latex=""}
🔗[Sıra Markdownda](https://atalay-k.github.io/OLC750/sunu/T_Dokumantasyon.html#1)
:::

::: {.try data-latex=""}
🔗[Codeacedemy](https://www.codecademy.com/learn)
:::


## Ödev 

*  Sadece temel pakette 1500'e yakın fonksiyon bulunduğu için ders dışı alıştırmalar yapmanız gereklidir.

*  [R kurulumu ile ilgili](https://learnr-examples.shinyapps.io/ex-setup-r/) learnr paketi hazırlanmış bir interaktif alıştırma örneğini inceleyeniz.

* Kitap Bölüm 1 alıştırmalarını tamamlayınız.

* Datacamp da üzerine atanan bölüm alıştırmalarını tamamlayınız.

*  swirl package **learn R in R** paketi yükleyerek alıştırma yapmayı deneyiniz.

*  [Referens kart](https://cran.r-project.org/doc/contrib/Short-refcard.pdf) sayfasının çıktısını alarak duvarınıza asmanızı öneririm. 


<!--chapter:end:03-fonksiyonlar.Rmd-->

# R Nesneler 

- Örnek bir veri seti


```r
library(tidyverse)
data(diamonds)
head(diamonds)
```

<div class="kable-table">

| carat|cut       |color |clarity | depth| table| price|    x|    y|    z|
|-----:|:---------|:-----|:-------|-----:|-----:|-----:|----:|----:|----:|
|  0.23|Ideal     |E     |SI2     |  61.5|    55|   326| 3.95| 3.98| 2.43|
|  0.21|Premium   |E     |SI1     |  59.8|    61|   326| 3.89| 3.84| 2.31|
|  0.23|Good      |E     |VS1     |  56.9|    65|   327| 4.05| 4.07| 2.31|
|  0.29|Premium   |I     |VS2     |  62.4|    58|   334| 4.20| 4.23| 2.63|
|  0.31|Good      |J     |SI2     |  63.3|    58|   335| 4.34| 4.35| 2.75|
|  0.24|Very Good |J     |VVS2    |  62.8|    57|   336| 3.94| 3.96| 2.48|

</div>


R nesne (object) yönelimli bir programlama dilidir.

-   Karakter (character)
-   Sayısal (numeric)
    -   tam sayı (integer)
    -   ondalıklı sayı (double)
    -   karmaşık sayı (complex)
-   Mantıksal (logical)
-   Faktör (factor)
-   Liste (list)
-   Fonksiyon (function)


## tam sayi
- tamsayı nesnesi oluşturulması

```r
tamsayi <- 2L
```
- tamsayi nesnesinin türünün sorgulanması

```r
typeof(tamsayi)
```

```
## [1] "integer"
```
- tamsayı nesnesinin yazdırılması


```r
tamsayi
```

```
## [1] 2
```


## ondalık sayı

- ondaliksayi nesnesinin oluşturulması

```r
ondaliksayi <- 2.5
```
- ondaliksayi nesnesinin türünün sorgulanması

```r
typeof(ondaliksayi)
```

```
## [1] "double"
```
- ondaliksayi nesnesinin yazdırılması

```r
ondaliksayi
```

```
## [1] 2.5
```


## İşlemler
- tek elemanlı vektörler

```r
x <- 1
y <- 1
```



```r
x+y
```

```
## [1] 2
```
- çok elemanlı vektörler


```r
x <- c(3,4,5)
y <- c(1,2,3)
# vektör eleman sayıları aynı mı?
length(x)==length(y)
```

```
## [1] TRUE
```


```r
x+y
```

```
## [1] 4 6 8
```


```r
x-y
```

```
## [1] 2 2 2
```


- çok elemanlı vektörler

```r
x <- 1:9
y <- c(1,2,3)
# vektör eleman sayıları farklı mı?
length(x)/length(y)
```

```
## [1] 3
```



```r
x+y
```

```
## [1]  2  4  6  5  7  9  8 10 12
```



```r
x/y
```

```
## [1] 1.0 1.0 1.0 4.0 2.5 2.0 7.0 4.0 3.0
```



- çok elemanlı vektörler


```r
x <- 1:5
y <- c(1,2)
# vektör eleman sayıları farklı olduğunda
length(x)/length(y)
```

```
## [1] 2.5
```

-   `x+y` işleminin sonucu nedir? <input class='webex-solveme nospaces' size='9' data-answer='["2 4 4 6 6"]'/>


<div class='webex-solution'><button>Çözüm</button>



```r
x + y
```

```
## Warning in x + y: longer object length is not a multiple of shorter object
## length
```

```
## [1] 2 4 4 6 6
```


</div>



## Karakter Nesneler

- karakter nesnesi oluşturulması

```r
karakter <- "olcme"
```
- Oluşturulan nesnenin türünün sorgulanmasa

```r
typeof(karakter)
```

```
## [1] "character"
```

-  nesne yazdırılması

```r
karakter
```

```
## [1] "olcme"
```



```r
# karakter nesnesi oluşturulması
ad <- "Su"
soyad <- "Sevim"
```

- iki nesneyi arada  boşluk bırakarak birleştirir.

```r
paste(ad,soyad)
```

```
## [1] "Su Sevim"
```

- sep argümanı farklı şekillerde özelleştirilebilir.

```r
paste(ad,soyad, sep="")
```

```
## [1] "SuSevim"
```



```r
paste(ad,soyad,sep="_")
```

```
## [1] "Su_Sevim"
```

- base pakette yer alan bazı karakter vektörler bulunmaktadır.

```r
letters
```

```
##  [1] "a" "b" "c" "d" "e" "f" "g" "h" "i" "j" "k" "l" "m" "n" "o" "p" "q" "r" "s"
## [20] "t" "u" "v" "w" "x" "y" "z"
```



```r
LETTERS
```

```
##  [1] "A" "B" "C" "D" "E" "F" "G" "H" "I" "J" "K" "L" "M" "N" "O" "P" "Q" "R" "S"
## [20] "T" "U" "V" "W" "X" "Y" "Z"
```


```r
month.name
```

```
##  [1] "January"   "February"  "March"     "April"     "May"       "June"     
##  [7] "July"      "August"    "September" "October"   "November"  "December"
```


```r
month.abb
```

```
##  [1] "Jan" "Feb" "Mar" "Apr" "May" "Jun" "Jul" "Aug" "Sep" "Oct" "Nov" "Dec"
```

- Nesne birleştirme fonksiyonlarından en sık kullananı `paste()`
- `paste()` fonksiyonunun temel argümanları ise `sep` ve `collapse`'dir.


```r
harf5<- letters[1:5]
(harf51 <- paste(harf5,1:5,sep="_"))
```

```
## [1] "a_1" "b_2" "c_3" "d_4" "e_5"
```

```r
length(harf51)
```

```
## [1] 5
```



```r
(harf52 <- paste(harf5,1:5,sep="_",
                 collapse=" "))
```

```
## [1] "a_1 b_2 c_3 d_4 e_5"
```

```r
length(harf52)
```

```
## [1] 1
```



-   `paste()` fonksiyonun yardım sayfasını inceleyiniz.

### Günün Sorusu

-   Aşağıdaki çıktıyı oluşturacak olan kodu oluşturunuz.


```
##  [1] "1. maddenin guclugu: 0.97"  "2. maddenin guclugu: 0.51" 
##  [3] "3. maddenin guclugu: 0.39"  "4. maddenin guclugu: 0.64" 
##  [5] "5. maddenin guclugu: 0.46"  "6. maddenin guclugu: 0.72" 
##  [7] "7. maddenin guclugu: 0.67"  "8. maddenin guclugu: 0.3"  
##  [9] "9. maddenin guclugu: 0.51"  "10. maddenin guclugu: 0.73"
```

Bunun birden fazla yolu olabilir, farklı şekillerde yapabilirsiniz. 


**Büyük Küçük Harf Düzenleme Fonksiyonları** `toupper()` ve `tolower()`


```r
toupper(harf5)
```

```
## [1] "A" "B" "C" "D" "E"
```



```r
tolower(harf5)
```

```
## [1] "a" "b" "c" "d" "e"
```


`casefold()` fonksiyonu da upper argümanı ile birlikte kullanılabilir.



```r
casefold(harf5, upper = FALSE)
```

```
## [1] "a" "b" "c" "d" "e"
```



```r
casefold(harf5, upper = TRUE)
```

```
## [1] "A" "B" "C" "D" "E"
```

- Karakter nesnelerin kaç harften oluştuğu `nchar()` fonksiyonu ile belirlenebilir.

```r
nchar(month.name)
```

```
##  [1] 7 8 5 5 3 4 4 6 9 7 8 8
```
- Karakter nesneleri belli bir yerden bölmek icin `substr()` ve `substring()` fonksiyonları kullanılabilir.


```r
substr("YILMAZ", 1,3)
```

```
## [1] "YIL"
```


-  ```substring("YILMAZ", 1:.. , 1:6)``` kodunda  "Y" "I" "L" "M" "A" "Z" çıktısı oluşturacak kodu yazınız <input class='webex-solveme nospaces' size='1' data-answer='["6"]'/>

-   ````substring("YILMAZ", ... , 4:6)``` kodunda "ILM"   "ILMA"  "ILMAZ"` çıktınısı oluşturacak kodu yazınız <input class='webex-solveme nospaces' size='1' data-answer='["2"]'/>

- Karakter nesnelerde daha fazlası için aşağıdaki fonksiyonları inceleyebilirsiniz.

-   `strsplit()`
-   `noquote()`
-   `cat()`
-   `grep()`
-   `duplicated()`
-   `agrep()`


## Mantıksal Nesneler


```r
mantiksal1 <-TRUE
```



```r
typeof(mantiksal1)
```

```
## [1] "logical"
```



```r
mantiksal1
```

```
## [1] TRUE
```

Mantıksal operatörler programlamanın temeli ve vazgeçilmezidir.



```r
# eşitlik sınaması
T==TRUE
```

```
## [1] TRUE
```

-   `4==5` kodunun sonucu nedir? <input class='webex-solveme nospaces' size='5' data-answer='["FALSE"]'/>

-   `4<5` kodunun sonucu nedir? <input class='webex-solveme nospaces' size='4' data-answer='["TRUE"]'/>

-   `10>100` kodunun sonucu nedir? <input class='webex-solveme nospaces' size='5' data-answer='["FALSE"]'/>



- Mantıksal operatörlerle yapılan sınamalar ile mantıksal nesneler oluşturulur.


```r
sonuc <- 4<5
typeof(sonuc)
```

```
## [1] "logical"
```


- Nesne türleri arasındaki değişim uygunluk durumuna göre `as.*()`fonksiyonları ile sağlanır.


```r
# Karakter veri numerik veriye
as.numeric("3.14")
```

```
## [1] 3.14
```


```r
# ondalık verin tam sayıya
as.integer(pi)
```

```
## [1] 3
```


```r
# karakter veri numerik veriye (NA)
as.numeric("olcme")
```

```
## Warning: NAs introduced by coercion
```

```
## [1] NA
```




```r
# mantıksal veri karakter veriye (NA)
as.character(TRUE)
```

```
## [1] "TRUE"
```


```r
# numerik veri karakter veriye
as.character(10)
```

```
## [1] "10"
```


```r
# mantıksal veri numerik veriye
as.numeric(TRUE)
```

```
## [1] 1
```



## Nesne Türleri Sorgulama

- Nesne türleri sorgulamak için ise `class()` ya da `mode()` fonksiyonları kullanabilir. Ancak bir nesne türüne ait olup olmadığını sorgulamak için ise `is.*()` fonksiyonları kullanılır.


```r
x<- 3.14; class(x)
```

```
## [1] "numeric"
```

```r
is.numeric(x)
```

```
## [1] TRUE
```

```r
is.logical(x)
```

```
## [1] FALSE
```


- Sayısal nesnelerin türü için `typeof()` fonksiyonu da kullanılabilir.


```r
y <- 2L; typeof(y); class(y) # satir içi kod ayırma
```

```
## [1] "integer"
## [1] "integer"
```

```r
is.integer(y)
```

```
## [1] TRUE
```

```r
is.double(y)
```

```
## [1] FALSE
```


### Günün Sorusu 

- aşağıda yer alan **ad_soyad** nesnesini kullanarak


```r
ad_soyad<- c("Ayse-Sel","Can-Yucel","Cem-Togay","Banu-Cift")
```



aşağıdaki çıktıyı oluşturmaya calisiniz.


```
## [1] "Ayse" "Can"  "Cem"  "Banu"
## [1] "Sel"   "Yucel" "Togay" "Cift"
```


<!--chapter:end:05-nesneler.Rmd-->

# Vektörler

-   R lineer cebir temelli bir programlama dilidir.

-   Vektörler tek boyutludur.

-   R'da vektörler birleştirmek (combine/concatenate) anlamına gelen `c()` fonksiyonu ile oluşturulmaktadır.

-   R da veriler bir araya gelerek veri yapılarını oluşturur.

    -   vektör (vector)
    -   liste (list)
    -   matris (matrix)
    -   veri seti (data.frame)
    -   dizi (array)

## Vektör Oluşturma


```r
(sayisal_vektor <-  c(1,2,3))
```

```
## [1] 1 2 3
```


```r
(karakter_vektor <-  c("a","b","c"))  ## cift tirnak
```

```
## [1] "a" "b" "c"
```


```r
(mantiksal_vektor <- c(TRUE,TRUE,FALSE))
```

```
## [1]  TRUE  TRUE FALSE
```

## Vektör İşlemleri

-   Vektör uzunluğu `length()` fonksiyonu ile vektör türleri ise `class()`, `mode()` ya da `typeof()` fonksiyonları ise tur belirlemek için kullanılmaktadır.

-   Vektörler bir veya daha fazla elemandan oluşabilmektedir.


```r
a <- 1  # tek elemandan oluşur.
# Vektör uzunluğunu öğrenmek icin length() fonksiyonu
length(a)
```

```
## [1] 1
```


```r
x <- 1:10
```

-   bir vektöründeki verilerin toplanması `sum(x)` 55

-   bir vektöründeki verilerin çarpılması `prod(x)` 3.6288\times 10^{6}

-   bir vektöründeki verilerin küçükten büyüğe sıralanması `sort(x)` 1, 2, 3, 4, 5, 6, 7, 8, 9, 10

-   bir vektörünün elemanların sıralarının tersine çevrilmesi `rev(x)` 10, 9, 8, 7, 6, 5, 4, 3, 2, 1

-   bir vektöründeki verilerin standart sapmasının hesaplanması `sd(x)` 3.0276504

-   bir vektöründeki en büyük verinin gösterilmesi `max(x)` 10

-   bir vektöründeki en küçük verinin gösterilmesi `min(x)` 1

-   En büyük verinin vektörün kaçıncı elemanı olduğunun gösterilmesi `which.max(x)` 10

-   En küçük verinin vektörün kaçıncı elemanı olduğunun gösterilmesi `which.min(x)` 1

-   Vektörlerden eleman sırası, isim ve mantıksal operatörler olmak üzere üç farklı yolla eleman seçilebilir.


```r
ad  <-  c("Ali","Elif","Su","Deniz",
"Aras","Berk","Can","Ece","Efe","Arda")
```

-   ad vektörünün 1. elemanı `ad[1]` Ali

-   ad vektörünün 5. elemanını yazdıracak kodu oluşturunuz. <input class='webex-solveme nospaces' size='5' data-answer='["ad[5]"]'/>

-   ad vektörünün son elemanını yazdıracak kodu oluşturunuz. <input class='webex-solveme nospaces' size='6' data-answer='["ad[10]"]'/>

-   ad vektörünün son elemanını yazdıracak kodu vektörün 10 elemanlı olduğunu bilmediğiniz de ne yaparsınız? <input class='webex-solveme nospaces' size='14' data-answer='["ad[length(ad)]"]'/>

-   Vektörün sadece 1., 5. 8 elemanının yazdıracak kodu oluşturunuz.<input class='webex-solveme nospaces' size='12' data-answer='["ad[c(1,5,8)]"]'/>

-   Vektörün sadece 1. elemanının hariç tutacak kodu oluşturunuz <input class='webex-solveme nospaces' size='6' data-answer='["ad[-1]"]'/>

-   Vektörün 1. ve 5. elemanının hariç tutacak kodu oluşturunuz <input class='webex-solveme nospaces' size='11' data-answer='["ad[-c(1,5)]"]'/>

-   Vektörün son üç elemanını yazdıracak kodu oluşturunuz `r `fitb("ad[8:10]")`

## Vektöre eleman eklenmesi


```r
ad[11] <- "Asu"; ad
```

```
##  [1] "Ali"   "Elif"  "Su"    "Deniz" "Aras"  "Berk"  "Can"   "Ece"   "Efe"  
## [10] "Arda"  "Asu"
```

-   vektöre birden fazla eleman eklenmesi


```r
ad[12:13] <- c("Ahu","Han"); ad
```

```
##  [1] "Ali"   "Elif"  "Su"    "Deniz" "Aras"  "Berk"  "Can"   "Ece"   "Efe"  
## [10] "Arda"  "Asu"   "Ahu"   "Han"
```

-   Vektörün ortasına eleman eklenmesi **append()** fonksiyonu ile yapılabilir. Fonksiyon yardım sayfasını inceleyiniz.


```r
(ad <- append(ad, "Taha", after = 3))
```

```
##  [1] "Ali"   "Elif"  "Su"    "Taha"  "Deniz" "Aras"  "Berk"  "Can"   "Ece"  
## [10] "Efe"   "Arda"  "Asu"   "Ahu"   "Han"
```

-   ya da `c()` fonksiyonu ile yapılabilir.


```r
ad <- c(ad[1:5],"Selim",ad[7:length(ad)]); ad
```

```
##  [1] "Ali"   "Elif"  "Su"    "Taha"  "Deniz" "Selim" "Berk"  "Can"   "Ece"  
## [10] "Efe"   "Arda"  "Asu"   "Ahu"   "Han"
```

## Alıştırma

-   10 kişiden oluşan bir gruptaki kişilerinin boy ve kilo ölçümleri için ise aşağıdaki vektör oluşturulmuştur.


```r
ad  <-  c("Ali","Elif","Su","Deniz",
"Aras","Berk","Can","Ece","Efe","Arda")
boy <- c(160,165,170,155,167,162,169,158,160,164)
kilo <-c(50,55,57,50,48,65,58,62,45,47)
```

-   Eğer elimizdeki vektör isimlendirilmiş bir vektör ise eleman seçimini isimle de yapabiliriz.


```r
#isimsiz boy vektoru
names(boy) # names() fonksiyonu ile isimlendirme yapılabilir.
```

```
## NULL
```

-   ad vektörünü boy vektörünü isimlendirirken nasıl kullanabiliriz? <input class='webex-solveme nospaces' size='16' data-answer='["names(boy) <- ad"]'/>

-   Arda 'nın boyunu isimlendirilmiş vektörü kullanarak nasıl yazdırırsınız? `r `fitb("boy["Arda"]")`

## Örüntülerle Vektör Oluşturma

-   Vektör oluşturmanın farklı yolları bulunmaktadır.

-   En basit yolu iki nokta `":"` operatörünü kullanmaktır.


```r
rakamlar <- 0:9
rakamlar
```

```
##  [1] 0 1 2 3 4 5 6 7 8 9
```

-   büyükten küçüğe rakamlardan vektör oluşturulması


```r
rakamlar <- 9:0
rakamlar
```

```
##  [1] 9 8 7 6 5 4 3 2 1 0
```

### seq()

-   Belirli bir kurala göre sayı dizileri oluşturmak için ise `seq()`, `rep()` ve `paste()` fonksiyonlarından yararlanılabilir. İlk olarak bu fonksiyonların yardım sayfalarını inceleyelim.

-   1'den 10'a kadar birer birer artan sayılardan dizi oluşturulacak kodu oluşturunuz. `seq(from=1,to=10,by=...)` <input class='webex-solveme nospaces' size='1' data-answer='["1"]'/>

-   Bir önceki işlemi argümansız olarak oluşturunuz. <input class='webex-solveme nospaces' size='11' data-answer='["seq(1,10,1)"]'/>

-   Aynı çıktıyı tek bir argümanla elde edebilir misiniz? <input class='webex-solveme nospaces' size='10' data-answer='["seq(to=10)"]'/>

-   length argümanını kullanarak aşağıdaki çıktıyı oluşturacak kodu oluşturunuz. <input class='webex-solveme nospaces' size='25' data-answer='["seq(from=1,to=3,length=6)"]'/>


```
## [1] 1.0 1.4 1.8 2.2 2.6 3.0
```

-   by argümanını ile artış miktarını kullanarak aşağıdaki çıktıyı oluşturacak kodu oluşturunuz. <input class='webex-solveme nospaces' size='23' data-answer='["seq(from=1,to=3,by=0.5)"]'/>


```
## [1] 1.0 1.5 2.0 2.5 3.0
```

-   Belirli bir aralıkta kaç elemanın yer alacağını length.out argümanı kullanarak aşağıdaki çıktıyı oluşturacak kodu oluşturunuz. <input class='webex-solveme nospaces' size='29' data-answer='["seq(from=1,to=3,length.out=5)"]'/>


```
## [1] 1.0 1.5 2.0 2.5 3.0
```

### rep()

`rep()` fonksiyonu için örnekler


```r
# üç elemanlı bir vektörün üç kere tekrar ettirilmesi
rep(c(3,4,5), 3)
```

```
## [1] 3 4 5 3 4 5 3 4 5
```


```r
# rakamların üç kere tekrar ettirilmesi
rep(0:9, times = 3) 
```

```
##  [1] 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9
```

-   `a <- c(3,5,7)` vektörünü kullanarak aşağıdaki çıktıyı elde edecek kodu hazırlayınız. <input class='webex-solveme nospaces' size='13' data-answer='["rep(a,each=3)"]'/>


```
## [1] 3 3 3 5 5 5 7 7 7
```

-   `a <- c(3,5,7)` vektörünü kullanarak aşağıdaki çıktıyı elde edecek kodu hazırlayınız. <input class='webex-solveme nospaces' size='21' data-answer='["rep(a,each=3,times=3)"]'/>


```
##  [1] 3 3 3 5 5 5 7 7 7 3 3 3 5 5 5 7 7 7 3 3 3 5 5 5 7 7 7
```

-   Çıktıyı elde edecek kodu hazırlayınız. <input class='webex-solveme nospaces' size='19' data-answer='["rep(1:4,c(2,2,2,2))"]'/>


```
## [1] 1 1 2 2 3 3 4 4
```

-   Çıktıyı elde edecek kodu hazırlayınız. <input class='webex-solveme nospaces' size='12' data-answer='["rep(1:3,1:3)"]'/>


```
## [1] 1 2 2 3 3 3
```

### paste()

-   `paste()`fonksiyonu çıktısı her zaman için karakterdir.


```r
paste(1:4) # çıktısı karakterdir
```

```
## [1] "1" "2" "3" "4"
```


```r
class(paste(1:4))
```

```
## [1] "character"
```
   
-   Çıktıyı elde edecek kodu tamamlayınız `paste("test",...)` <input class='webex-solveme nospaces' size='4' data-answer='["1:10"]'/>


```
##  [1] "test 1"  "test 2"  "test 3"  "test 4"  "test 5"  "test 6"  "test 7" 
##  [8] "test 8"  "test 9"  "test 10"
```


-   Çıktıyı elde edecek kodu tamamlayınız`paste("test",1:10,"...",sep="_")` <input class='webex-solveme nospaces' size='4' data-answer='["puan"]'/>


```
##  [1] "test_1_puan"  "test_2_puan"  "test_3_puan"  "test_4_puan"  "test_5_puan" 
##  [6] "test_6_puan"  "test_7_puan"  "test_8_puan"  "test_9_puan"  "test_10_puan"
```

-   Çıktıyı elde edecek kodu tamamlayınız `paste("test",c("A","B","C","D",...))`  <input class='webex-solveme nospaces' size='3' data-answer='["1:4"]'/> 


```
## [1] "test A" "test B" "test C" "test D" "test 1" "test 2" "test 3" "test 4"
```

## Rasgele Veri Oluşturma

-   Farklı fonksiyonlarla rastgele veri üretilebilir. Örneğin 0-100 arasında 20 farklı değer elde edilmek istenilsin. Bunu yapmak için `sample()`,`runif()` ya da `rnorm()` fonksiyonlarından yararlanılabilir.


```r
sample(0:100,5)
```

```
## [1] 58 45 43 14 60
```


```r
runif(10,  0, 5)
```

```
##  [1] 4.5213709 1.3811519 1.3178764 0.1933504 1.2378789 0.4194994 3.6760637
##  [8] 0.0867058 3.0685957 2.3767663
```


```r
rnorm(10,50,5)
```

```
##  [1] 47.50697 49.96323 43.76162 50.72525 46.73043 44.27729 52.50778 51.50835
##  [9] 56.27162 46.55452
```

-   Kullanılan üç fonksiyonun da yardım sayfalarını ve kullanım amaçlarını inceleyiniz.

## İşlemler

BKI vücut ağırlığınızın metre cinsinden boy uzunluğunun karesine bölünmesi ile elde edilmektedir. Her bir bireye ait BKI değerini hesaplayınız. BKI derğerlerinin ortalaması kaçtır(iki ondalığa yuvarlayınız)?  <input class='webex-solveme nospaces' size='5' data-answer='["20.44"]'/> 


```r
ad  <-  c("Ali","Elif","Su","Deniz","Aras","Berk","Can","Ece","Efe","Arda")
boy <- c(160,165,170,155,167,162,169,158,160,164)
kilo <- c(55,55,57,50,48,65,58,62,45,47)
```


<div class='webex-solution'><button>Çözüm!,bakmadan yapmalısın!</button>



```r
# BKI  hesaplanması
boy_m  <- boy/100
BKI <- kilo/( boy_m * boy_m)
BKI
round(mean(BKI),2)
```

```
##  [1] 21.48437 20.20202 19.72318 20.81165 17.21109 24.76757 20.30741 24.83576
##  [9] 17.57812 17.47472
## [1] 20.44
```

</div>


### Kendinizi Test Edin

**S1.** Aşağıdaki tabloda yer alan üç sütun için birer vektör oluşturunuz. Öğrencilerin geçme notu her iki sınavın ortalaması olarak hesaplanacaktır. Bu öğrencilerin geçme notlarını hesaplayınız. Geçme notlarının betimsel istatistiklerini hesaplayınız.

| Öğrenci | Vize | Final |
|---|---|---|
| Ogrenci1 | 50 | 45 | 
| Ogrenci2 | 55 | 65 | 
| Ogrenci3 | 60 | 85 | 
| Ogrenci4 | 70 | 90 | 
| Ogrenci5 | 80 | 85 |

Geçme notlarının minumum değeri: <input class='webex-solveme nospaces' size='4' data-answer='["47.5"]'/>

Geçme notlarının ortalama değeri: <input class='webex-solveme nospaces' size='4' data-answer='["68.5"]'/>

Geçme notlarının maksimum değeri: <input class='webex-solveme nospaces' size='4' data-answer='["82.5"]'/>





**S2.**  Birden n'e kadar olan sayların toplamını hesaplayan fonksiyon yazımı `toplam()` tek argümanlı fonksiyon oluşturunuz. Argüman değeri 5 olduğunda 1+2+3+4+5=15 değerini versin.

-   birden n'e kadar olan sayların toplamı: (n\*(n+1))/2


**S3.** 1'den n' e kadar olan sayıların toplamını hesaplayan fonksiyonu argümansız olarak aşağıdaki şekilde yazmayı deneyiniz. Fonksiyonu çalıştırdığınızda ekranda/konsolda kaça kadar olan sayların toplamı hesaplansın: yazsın, kullanıcının girdiği değere göre aşağıda çıktısı çıksın.


```r
toplam()

kaça kadar olan sayların toplamı hesaplansın: 10

[1 " 10 'e kadar olan sayların toplamı: 55
```


## **ODEV**

-   Kitap Bölüm 2 1. Soruyu tamamlayınız.

-   swirl package - learn R in R (Programming ilk 6 modul)

-   datacamp ödevinizi yapmayını unutmayın 😄

<!--chapter:end:06-vektorler.Rmd-->

# Veri Setleri

- Veri setleri iki boyutludur.

- R'da bir çok fonksiyonun veri setleri ile çalışmaktadır. 

- Veri setleri R ortamında `data.frame()` fonksiyonu ile oluşturulabilir.

- `data.frame()` fonksiyonu ile aynı uzunluktaki vektörlerden bir veri seti oluşturulabilir.



```r
ad  <-  c("Ali","Elif","Su","Deniz","Aras", "Berk","Can","Ece","Efe","Arda")
boy <- c(160,165,170,155,167,162, 169,158,160,164)
kilo <- c(55,55,57,50,48,65, 58,62,45,47)
beden <- c("S","M","S","M","S", "L","M","L","S","S")
beden <- factor(beden)


(df <- data.frame(ad,boy, kilo, beden))
```

<div class="kable-table">

|ad    | boy| kilo|beden |
|:-----|---:|----:|:-----|
|Ali   | 160|   55|S     |
|Elif  | 165|   55|M     |
|Su    | 170|   57|S     |
|Deniz | 155|   50|M     |
|Aras  | 167|   48|S     |
|Berk  | 162|   65|L     |
|Can   | 169|   58|M     |
|Ece   | 158|   62|L     |
|Efe   | 160|   45|S     |
|Arda  | 164|   47|S     |

</div>

- Eğer uzunlukları farklı olan vektörlerle veri setleri oluşturulmaya çalışılırsa kısa vektör, uzun vektör uzunluğunda tekrar eder.


```r
# 4 farklı uzunlukta vektör oluşturulması
x <- 11:14; y <- 10; M <- c(10,35); N <- 2:4
```



```r
data.frame(x, y) # (4,1)
```

<div class="kable-table">

|  x|  y|
|--:|--:|
| 11| 10|
| 12| 10|
| 13| 10|
| 14| 10|

</div>



```r
data.frame(x, M) # (4,2)
```

<div class="kable-table">

|  x|  M|
|--:|--:|
| 11| 10|
| 12| 35|
| 13| 10|
| 14| 35|

</div>




```r
data.frame(x,N)  #(4,3) hata
```

```
## Error in data.frame(x, N): arguments imply differing number of rows: 4, 3
```



```r
data.frame(y, M) #(1,2)
```

<div class="kable-table">

|  y|  M|
|--:|--:|
| 10| 10|
| 10| 35|

</div>



```r
data.frame(y, N) #(1,3)
```

<div class="kable-table">

|  y|  N|
|--:|--:|
| 10|  2|
| 10|  3|
| 10|  4|

</div>


```r
data.frame(M, N) #(2,3)
```

```
## Error in data.frame(M, N): arguments imply differing number of rows: 2, 3
```

## Hazır Veri Setleri

- Temel pakette yer alan veri setlerinin bir listesine aşağıdaki komutla ulaşabilirsiniz.


```r
data() # yeni bir pencerede açılır.
```

- Veri setlerinin yer aldığı paketlerde bulunmaktadır.


```r
# install.packages("datasets")
library (datasets)
# install.packages("dslabs")
library (dslabs)
```

- Hazır veri setleri çalışma ortamına `data()` fonksiyonu ile aktarılabilir.


```r
data(WorldPhones) # environmete kontrol ediniz. 
```

- hazır veri setlerini incelememek için aşağıdaki komutlar kullanılabilir. 


```r
data(cars) # enviromente ekler
iris      # enviromente eklemez!
```

## İnceleme

- Boyut sorgulamamak için farklı fonksiyonlar kullanılabilir.


```r
dim(cars) # satir Sutun
```

```
## [1] 50  2
```


```r
nrow(cars)
```

```
## [1] 50
```


```r
ncol(cars)
```

```
## [1] 2
```


- Veri setlerin ilk satırları `head()`, son satırları ise `tail()` fonksiyonu ile incelenebilir. `head()` fonksiyonu olağan olarak ilk 6 satırı yazdırır.


```r
head(WorldPhones)
```

```
##      N.Amer Europe Asia S.Amer Oceania Africa Mid.Amer
## 1951  45939  21574 2876   1815    1646     89      555
## 1956  60423  29990 4708   2568    2366   1411      733
## 1957  64721  32510 5230   2695    2526   1546      773
## 1958  68484  35218 6662   2845    2691   1663      836
## 1959  71799  37598 6856   3000    2868   1769      911
## 1960  76036  40341 8220   3145    3054   1905     1008
```

- Yazdırılacak satır sayısı `n` argümanı ile ayarlanır.

```r
head(WorldPhones,n=2)
```

```
##      N.Amer Europe Asia S.Amer Oceania Africa Mid.Amer
## 1951  45939  21574 2876   1815    1646     89      555
## 1956  60423  29990 4708   2568    2366   1411      733
```

- WorldPhones veri setinin son 8 satırını yazdıracak kodu yazınız. <input class='webex-solveme nospaces' size='21' data-answer='["tail(WorldPhones,n=8)"]'/>

- `datasets` paketinde yer alan veri setlerinde `examples()` bölümünde çeşitli örneklere yer verilmiştir. Örneğin `example(WorldPhones)`


```r
matplot(rownames(WorldPhones), WorldPhones, type = "b", log = "y",
        xlab = "Year", ylab = "Number of telephones (1000's)")
legend("bottomright", colnames(WorldPhones), col = 1:6, lty = 1:5,
       pch = rep(21, 7))
title(main = "World phones data: log scale for response")
```

<img src="07-veriseti_files/figure-html/unnamed-chunk-18-1.png" width="100%" style="display: block; margin: auto;" />


-  Temel paket hariç diğer paketlerdeki veri setlerine `data(veriseti, package="packagename")` şeklinde ulaşılabilir.


```r
data(CTTdata, package="CTT") 
head(CTTdata)
```

- 🔗[sık kullanılan veri setleri ile ilgili bir yazı:](http://r-tutorials.com/famous-useful-pre-installed-exercise-datasets-r/)

- 🔗[tüm veri setlerine ulaşabilmek için ise:](https://vincentarelbundock.github.io/Rdatasets/datasets.html)



- Kullanışlı olmasa da excel, spps gibi veri girişi sağlayan bir arayüz bulunmaktadır.


- Ali, Su ve Ece'nin boylarının ve kilolarının seçilmesi

```r
df1<- data.frame() 
df1 <- edit(df1)
# duzenlemek icin
fix(df)
# gozatmak icin 
View(df)
```


## Elaman Seçme

Veri setlerinde eleman seçme matrislerdeki gibidir.

`df[satirindeks, sutunindeks]`



- df'nin birinci satir elemanlarının seçilmesi  <input class='webex-solveme nospaces' size='6' data-answer='["df[1,]"]'/>

<div class="kable-table">

|ad  | boy| kilo|beden |
|:---|---:|----:|:-----|
|Ali | 160|   55|S     |

</div>

- df'nin birinci sütun elemanlarının seçilmesi  <input class='webex-solveme nospaces' size='6' data-answer='["df[,1]"]'/>
 

```
##  [1] "Ali"   "Elif"  "Su"    "Deniz" "Aras"  "Berk"  "Can"   "Ece"   "Efe"  
## [10] "Arda"
```

- df'nin ikinci satir elemanlarının seçilmesi  <input class='webex-solveme nospaces' size='6' data-answer='["df[2,]"]'/>

 
<div class="kable-table">

|   |ad   | boy| kilo|beden |
|:--|:----|---:|----:|:-----|
|2  |Elif | 165|   55|M     |

</div>

- df'nin ikinci sütun elemanlarının seçilmesi   <input class='webex-solveme nospaces' size='6' data-answer='["df[,2]"]'/>


```
##  [1] 160 165 170 155 167 162 169 158 160 164
```

- df'nin birinci satir üçüncü sütun elemanlarının seçilmesi  <input class='webex-solveme nospaces' size='7' data-answer='["df[1,3]"]'/>


```
## [1] 55
```

- Veri setlerinde satır elemanları yazdırıldığında veri seti (`data.frame)`, sütun elemanları yazdırıldığında ise vektör (`vector)` oluşmaktadır.


```r
# satir secimi
is.data.frame(df[1,])
```

```
## [1] TRUE
```


```r
# sutun secimi
is.data.frame(df[,1])
```

```
## [1] FALSE
```

- Sütun seçimi veri seti (`data.frame`) olarak yapılmak istenirse, `drop` argümanı FALSE değeri ile kullanılır.


```r
df[,1,drop=FALSE]
```

<div class="kable-table">

|ad    |
|:-----|
|Ali   |
|Elif  |
|Su    |
|Deniz |
|Aras  |
|Berk  |
|Can   |
|Ece   |
|Efe   |
|Arda  |

</div>


- Veri seçim işlemi için `subset()` fonksiyonu kullanılabilir.

- `?subset` bir fonksiyonu ilk daha kullanıyorsanız, mutlaka yardım sayfasını inceleyin. 

`subset(veriseti, kosul/Kosullar)`

- Boyu 165cm den uzun öğrencilerin bilgilerinin seçilmesi


```r
subset(df, boy >165)
```

<div class="kable-table">

|   |ad   | boy| kilo|beden |
|:--|:----|---:|----:|:-----|
|3  |Su   | 170|   57|S     |
|5  |Aras | 167|   48|S     |
|7  |Can  | 169|   58|M     |

</div>


- `subset()` Fonksiyonun yardım sayfasındaki örnekleri inceleyebilirsiniz.


```r
subset(airquality, Temp > 90,select = c(Ozone, Temp))
```

<div class="kable-table">

|    | Ozone| Temp|
|:---|-----:|----:|
|42  |    NA|   93|
|43  |    NA|   92|
|69  |    97|   92|
|70  |    97|   92|
|75  |    NA|   91|
|102 |    NA|   92|
|120 |    76|   97|
|121 |   118|   94|
|122 |    84|   96|
|123 |    85|   94|
|124 |    96|   91|
|125 |    78|   92|
|126 |    73|   93|
|127 |    91|   93|

</div>



```r
subset(airquality, Day == 1, select = -Temp)
```

<div class="kable-table">

|    | Ozone| Solar.R| Wind| Month| Day|
|:---|-----:|-------:|----:|-----:|---:|
|1   |    41|     190|  7.4|     5|   1|
|32  |    NA|     286|  8.6|     6|   1|
|62  |   135|     269|  4.1|     7|   1|
|93  |    39|      83|  6.9|     8|   1|
|124 |    96|     167|  6.9|     9|   1|

</div>

- df verisinde beden değişkeni "S" olan satırların seçimi  `subset(df,beden =="S")` 


- df verisinde kilosu 50'in altında olan kişilerden oluşan veri seti oluşturma kodunu tamamlayınız `subset(df,.......)` <input class='webex-solveme nospaces' size='7' data-answer='["kilo<50"]'/>


## Eleman ekleme 

- Veri setine yeni sütun ekleme isleme `$` operatörü ile `[[]]` operatörü ile `cbind()` fonksiyonları ile yapılabilmektedir.


```r
df2 <- data.frame(
      S1 = sample(0:100,20),
      S2 = runif(n=20 ,min= 50 , max=70)
)
head(df2)
```

<div class="kable-table">

| S1|       S2|
|--:|--------:|
| 87| 51.46013|
| 90| 52.32683|
| 98| 66.28715|
| 19| 54.57867|
|  1| 51.13694|
| 27| 64.47405|

</div>


- `$` operatörü ile sütun ekleme


```r
df2$S3 <- sample(60:80,20,replace = TRUE)
head(df2)
```

<div class="kable-table">

| S1|       S2| S3|
|--:|--------:|--:|
| 87| 51.46013| 72|
| 90| 52.32683| 66|
| 98| 66.28715| 79|
| 19| 54.57867| 80|
|  1| 51.13694| 79|
| 27| 64.47405| 74|

</div>

- `[[]]` operatörü ile sütun ekleme

- df2 veri setinin ilk üç sütunun `rowMeans()` fonksiyonu ile ortalamasının alınarak ort isimi ile veri setine eklenmesi


```r
df2[["ort"]] <- round(rowMeans(df2),2)
head(df2)
```

<div class="kable-table">

| S1|       S2| S3|   ort|
|--:|--------:|--:|-----:|
| 87| 51.46013| 72| 70.15|
| 90| 52.32683| 66| 69.44|
| 98| 66.28715| 79| 81.10|
| 19| 54.57867| 80| 51.19|
|  1| 51.13694| 79| 43.71|
| 27| 64.47405| 74| 55.16|

</div>


- `cbind()` fonksiyonu ile sütun ekleme


```r
cbind( df2, S4 = 10)
```

<div class="kable-table">

|  S1|       S2| S3|   ort| S4|
|---:|--------:|--:|-----:|--:|
|  87| 51.46013| 72| 70.15| 10|
|  90| 52.32683| 66| 69.44| 10|
|  98| 66.28715| 79| 81.10| 10|
|  19| 54.57867| 80| 51.19| 10|
|   1| 51.13694| 79| 43.71| 10|
|  27| 64.47405| 74| 55.16| 10|
|  60| 66.65722| 73| 66.55| 10|
|  56| 61.91237| 67| 61.64| 10|
|  24| 51.63865| 68| 47.88| 10|
|  99| 69.07148| 74| 80.69| 10|
|  59| 57.00088| 75| 63.67| 10|
|  66| 50.98540| 64| 60.33| 10|
|  55| 55.84279| 80| 63.61| 10|
|  34| 68.12742| 65| 55.71| 10|
|  38| 63.48967| 65| 55.50| 10|
|  30| 52.19375| 76| 52.73| 10|
|  94| 69.24475| 78| 80.41| 10|
|  17| 69.56106| 77| 54.52| 10|
|  50| 51.32422| 80| 60.44| 10|
| 100| 60.42800| 80| 80.14| 10|

</div>


## Eleman çıkarma 

- Veri setinden istenilen sütunun çıkarılabilir. Bu işlemi yapmak için iki farklı yol kullanılabilir. 

- `-` operatörü


```r
head(df2,3)
```

<div class="kable-table">

| S1|       S2| S3|   ort|
|--:|--------:|--:|-----:|
| 87| 51.46013| 72| 70.15|
| 90| 52.32683| 66| 69.44|
| 98| 66.28715| 79| 81.10|

</div>


```r
df2 <- df2[,-4] 
head(df2,3)
```

<div class="kable-table">

| S1|       S2| S3|
|--:|--------:|--:|
| 87| 51.46013| 72|
| 90| 52.32683| 66|
| 98| 66.28715| 79|

</div>

- `NULL` operatörü


```r
df2$S3 <- NULL
head(df2,3)
```

<div class="kable-table">

| S1|       S2|
|--:|--------:|
| 87| 51.46013|
| 90| 52.32683|
| 98| 66.28715|

</div>


## Satır ekleme 

- Veri setlerine değişken ekleyip, çıkarabileceğiniz gibi gözlem de ekleyip, çıkarabilirsiniz. Veri setine iki satır ekleme


```r
dim(df2)
```

```
## [1] 20  2
```


```r
# eklenecek iki satırlık veri seti oluşturma
df3 <- data.frame(S1=c(50,60),S2=c(55.3,65.5))
# yeni veri seti
df4 <- rbind (df2,df3)
dim(df4)
```

```
## [1] 22  2
```

## Veri yapısı inceleme

- Veri setlerinin yapısını incelemek icin `str()` fonksiyonundan yararlanılmaktadır.


```r
str(df)
```

```
## 'data.frame':	10 obs. of  4 variables:
##  $ ad   : chr  "Ali" "Elif" "Su" "Deniz" ...
##  $ boy  : num  160 165 170 155 167 162 169 158 160 164
##  $ kilo : num  55 55 57 50 48 65 58 62 45 47
##  $ beden: Factor w/ 3 levels "L","M","S": 3 2 3 2 3 1 2 1 3 3
```

- "df" veri seti 10 gözlemden, 4 değişken. Her bir değişkenin önünde `$` operatörü olduğuna dikkat ediniz.



- veri setinin incelenmek için kullanılabilecek diğer fonksiyon ise `attributes()`


```r
attributes(df)
```

```
## $names
## [1] "ad"    "boy"   "kilo"  "beden"
## 
## $class
## [1] "data.frame"
## 
## $row.names
##  [1]  1  2  3  4  5  6  7  8  9 10
```


## Isimlendirme

- Veri setleri vektör birleştirme üzerinden yapılırsa, vektör adları sütun ismi olarak kullanılır. Ancak bu isimler değiştirilebilir. Bu işlem `data.frame()` fonksiyonu içinde yapılabilir.


```r
df <- data.frame(isim = ad,
                 boyolcum = boy,
                 kiloolcum= kilo, 
                 bedenolcum=beden)
df
```

<div class="kable-table">

|isim  | boyolcum| kiloolcum|bedenolcum |
|:-----|--------:|---------:|:----------|
|Ali   |      160|        55|S          |
|Elif  |      165|        55|M          |
|Su    |      170|        57|S          |
|Deniz |      155|        50|M          |
|Aras  |      167|        48|S          |
|Berk  |      162|        65|L          |
|Can   |      169|        58|M          |
|Ece   |      158|        62|L          |
|Efe   |      160|        45|S          |
|Arda  |      164|        47|S          |

</div>


- Veri seti isimlendirme de diğer bir yol ise `names()` ya da `colnames()` fonksiyonlarıdır.


```r
df <- data.frame(ad,boy,kilo,beden)
names(df) <- c("isim","boyolcum ","kiloolcum","bedenolcum")
df
```

<div class="kable-table">

|isim  | boyolcum | kiloolcum|bedenolcum |
|:-----|---------:|---------:|:----------|
|Ali   |       160|        55|S          |
|Elif  |       165|        55|M          |
|Su    |       170|        57|S          |
|Deniz |       155|        50|M          |
|Aras  |       167|        48|S          |
|Berk  |       162|        65|L          |
|Can   |       169|        58|M          |
|Ece   |       158|        62|L          |
|Efe   |       160|        45|S          |
|Arda  |       164|        47|S          |

</div>


## Betimsel istatistikler

- Veri setinin tümüne ilişkin betimsel istatistikler


```r
summary(cars)
```

```
##      speed           dist       
##  Min.   : 4.0   Min.   :  2.00  
##  1st Qu.:12.0   1st Qu.: 26.00  
##  Median :15.0   Median : 36.00  
##  Mean   :15.4   Mean   : 42.98  
##  3rd Qu.:19.0   3rd Qu.: 56.00  
##  Max.   :25.0   Max.   :120.00
```


- Veri setinin tek değişkenine ilişkin betimsel istatistikler


```r
summary(cars$speed)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##     4.0    12.0    15.0    15.4    19.0    25.0
```


`attach()` fonksiyonu ile bir veri setinin sütunları sütun isimi ile enviromente eklenir. Aynı işlem `detach()` fonksiyonu ile tersine alınabilir.


```r
summary(women$height)   
attach(women)
summary(height)   # Ayni nesne isimi ile çağırılır.
height <- height*2.54   # Bunu yapmamaya calisin!!
find("height")
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##    58.0    61.5    65.0    65.0    68.5    72.0 
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##    58.0    61.5    65.0    65.0    68.5    72.0 
## [1] ".GlobalEnv" "women"
```



```r
summary(height)         # Yeni değişken
rm(height)
detach("women")
summary(women$height)   # unchanged
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   147.3   156.2   165.1   165.1   174.0   182.9 
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##    58.0    61.5    65.0    65.0    68.5    72.0
```



### Kendinizi Test Edin

**S1.** Sırayla değişken adları TamSayi, OndalikSayi, Karakter, Mantıksal, Faktör olan 5 değişkenli hiçbir gözlemi olmayan bir data.frame oluşturmanızı ve bu data.framenin yapısını yazdırmanızı bekliyorum. Beklenen çıktı aşağıdaki gibi olmalıdır.


```r
[1] "Bos data.framenin yapısı:"
'data.frame':	0 obs. of  5 variables:  
 $ TamSayi    : int   
 $ OndalikSayi: num  
 $ Karakter   : chr  
 $ Mantiksal  : logi  
 $ Faktor     : Factor w/ 0 levels:  
NULL
```



**S2.** Aşağıda size verilen dört vektörden bir veri seti oluşturunuz. Oluşturduğunuz veri setinin deneme sütunundaki eksik veri sayısını hesaplayan komut yazınız.


```r
ad = c('Su','Pera','Sule','Can','Cem','Name','Aras','Mete','Kaan','Pelin')
puan = c(12.5, 9, 16.5, 12, 9, 20, 14.5, 13.5, 8, 19)
deneme = c(1, NA, 2, NA, 2, NA, 1, NA, 2, 1)
bonus = c(1,0,1, 0, 0, 1, 1, 0,0, 1)
```

"Deneme sütunundaki NA sayısı:"
[1] 4



## Odev

Lütfen aşağıdaki bölümleri haftaya kadar okuyunuz.

-   <http://adv-r.had.co.nz/Data-structures.html>

-   <http://adv-r.had.co.nz/Subsetting.html>

- Veri düzenleme konusunda 🔗 [**DataEditR**](https://dillonhammill.github.io/DataEditR/) paketini inceleyiniz. 

<!--chapter:end:07-veriseti.Rmd-->

# Veri Okuma ve Yazma

-   Veri girişi istatistiksel analiz sürecinin ilk adımıdır.

-   R'da veri girişi diğer yazılımlarla kıyaslandığında **çok kullanışlı değildir.**

-   Bu nedenle aktarma/import yolu tercih edilir.

-   Veri aktarımı için çok sayıda fonksiyon ve paket bulunmaktadır.

-   Ayrıca **menü ile de aktarma** yapılabilir.

-   Bilgisayardan internetten farklı formattaki veriler okunabilir.

-   Veri setleri genellikle Excel, SPSS veya metin dosyaları (.txt, .csv, .dat, vb.) gibi uygun veri biçimlerinde kaydedilir

-   R, çeşitli veri formatlarını içe aktarabilir (yani okuyabilir).

Bir veri setini R'ye aktarmanın iki yolu vardır:

1.  RStudio'da "Veri Kümesini İçe Aktar" menü seçeneğini kullanarak

![R studio](images/importmenu.png)

2.  Belirli bir R komutunu kullanarak

-   İçe aktarmak istediğiniz dosyaya göz atın.

-   Veri seti için bir isim verin.

-   İçe aktarılacak sayfayı seçin.

-   Değişken isimleri dosyanın ilk satırındaysa "First Row as Names".

![Excel dosylarını içe aktarma](images/excel1.png)

### SPSS dosylarını içe aktarma

-   İçe aktarmak istediğiniz dosyaya göz atın.

-   Veri seti için bir isim verin.

![SPSS dosylarını içe aktarma](images/spss1.png)

## Veri Okuma

-   En temel veri okuma/aktarma fonksiyonları

    -   `scan()`
    -   `read.*`
    -   `read.table()`
    -   `read.csv()`
    -   `read.csv2()`
    -   `read.delim()`
    -   `read.delim2()`
    -   `readLines()`

-   Verinin düzgün girilmiş olması okumayı kolaylaştırır.

-   İlk satırda genellikle değişken adlarına (header), ilk sütunda ise kimlik veya sıra numarasına yer verilir.

-   Gözlemlere ve değişkenlere ilişkin veri girilirken karakterler veya sayısal değerler arasında boşluk bırakmaktan kaçınmak gerekmektedir. Değişken adı boşluklu yazılmışsa ne olur?

-   Eksik veri boyunca aynı şekilde girilmelidir.

-   Değişkenlerin birinden nasıl ayrıldığı önemlidir. (, ; :  / )

-   Tercihimiz **.csv** uzantılı veriler ama büyük veri setleri az yer kalması icin **.txt,.prn** formatında karşımıza çıkabilmektedir.

-   Temel pakette **read.csv** ve **read.table** gibi bazı fonksiyonlar bulunmaktadır.

-   Ayrıca, belirli formatlarını içe aktarmak için R paketleri bulunmaktadır.Örneğin, SPSS dosyaları için **foreign** ve Excel dosyaları için **xlsx** gibi

## read.\*() fonksiyonları

| **Argüman**     | **Açıklama**                                                                                 |
|:-----------------------------------|:-----------------------------------|
| **header**      | Mantıksal değerler ile verinin ilk satırında değişken isimlerinin olup olmadığını test eder. |
| **sep**         | Sütun ayracıdır.                                                                             |
| **na.strings**  | Kayıp değerleri belirtmek için kullanılır.                                                   |
| **dec**         | Ondalık sayıların ne ile ayrıldığını gösteren argümandır.                                    |
| **nrows**       | Okunmak istenilen satır sayısını belirtmek için kullanılır.                                  |
| **skip**        | Bir dosya okunurken okunmadan atlanmak istenilen satır sayısı için kullanılır.               |

##  Excel dosyası aktarma


```r
# yükle ve aktive et 
install.packages("xlsx")
library("xlsx")

# read.xlsx fonksiyonunun kullanımı
my_excel_file <- read.xlsx("dizin/dosyaadi.xlsx",sheetName = "sheetname")
```

### SPSS dosyası aktarma


```r
# yükle ve aktive et 
install.packages("foreign")
library("foreign")

# read.spss fonksiyonunun kullanımı
my_spss_file <- read.spss("dizin/dosyaadi.sav",
                to.data.frame = TRUE)
```

### text dosyası aktarma

-   text dosyaları okumak için paket yüklemeye gerek yoktur.


```r
# , ile ayrılmış csv dosyaları
csv_dosya <- read.csv("dizin/dosyaadi.csv",header = TRUE)

# tab ile ayrılmış txt dosyaları
txt_dosya <- read.table("dizin/dosyaadi.txt",header = TRUE, sep = "\t")
```

-   Dikkat

-   `header = TRUE`

-   `sep="\t"`

-   `sep=","` for comma-separated files

-   

## Uygulama

-   🔗Dosyaları buradan klasor halinde indirebilirsiniz. [DOSYALAR](import/import.rar)

-   🔗[veri1.txt](import/veri1.txt)

<div class="kable-table">

|  no| m_1|  m_2| m_3|  m_4| m_5|
|---:|---:|----:|---:|----:|---:|
| 522|  12| 14.0|  16| 20.0|  10|
| 222|   5|   NA|  20| 10.0|  10|
| 454|   5| 10.2|   6|  4.0|  10|
| 567|  10| 20.0|  NA| 12.2|  20|

</div>


-   🔗[veri1.csv](import/veri1.csv)


<div class="kable-table">

|  no| m_1|  m_2| m_3|  m_4| m_5|
|---:|---:|----:|---:|----:|---:|
| 522|  12| 14.0|  16| 20.0|  10|
| 222|   5|   NA|  20| 10.0|  10|
| 454|   5| 10.2|   6|  4.0|  10|
| 567|  10| 20.0|  NA| 12.2|  20|

</div>

- 
<div class="kable-table">

|    |  No| M1|M2   | M3|M4   | M5|
|:---|---:|--:|:----|--:|:----|--:|
|001 | 522| 12|14   | 16|20   | 10|
|002 | 222|  5|NA   | 20|10   | 10|
|003 | 454|  5|10,2 |  6|4    | 10|
|004 | 567| 10|20   | NA|12,2 | 20|

</div>

- 
<div class="kable-table">

|    | M1|M2   | M3|M4   | M5|
|:---|--:|:----|--:|:----|--:|
|001 | 12|14   | 16|20   | 10|
|002 |  5|NA   | 20|10   | 10|
|003 |  5|10,2 |  6|4    | 10|
|004 | 10|20   | NA|12,2 | 20|

</div>


-   🔗[verifwf.txt](import/fwf.txt)
-

<div class="kable-table">

| V1|  V2|V3 | V4| V5| V6| V7| V8| V9| V10| V11| V12| V13|
|--:|---:|:--|--:|--:|--:|--:|--:|--:|---:|---:|---:|---:|
|  1| 689|A  |  1|  0|  1|  0|  1|  0|   1|   0|   1|   0|
|  2| 654|B  |  1|  1|  1|  1|  0|  1|   0|   1|   0|   1|
|  3| 436|A  |  1|  0|  1|  0|  1|  1|   1|   1|   1|   1|

</div>

-
<div class="kable-table">

| sira|  no|kitapcik | m1| m2| m3| m4| m5| m6| m7| m8| m9| m10|
|----:|---:|:--------|--:|--:|--:|--:|--:|--:|--:|--:|--:|---:|
|    1| 689|A        |  1|  0|  1|  0|  1|  0|  1|  0|  1|   0|
|    2| 654|B        |  1|  1|  1|  1|  0|  1|  0|  1|  0|   1|
|    3| 436|A        |  1|  0|  1|  0|  1|  1|  1|  1|  1|   1|

</div>

-   🔗[factor.sav](import/factor.sav)


```
## tibble [50 × 3] (S3: tbl_df/tbl/data.frame)
##  $ id   : num [1:50] 1 2 3 4 5 6 7 8 9 10 ...
##   ..- attr(*, "format.spss")= chr "F6.2"
##  $ bolge: num [1:50] 1 1 1 1 1 1 1 1 1 1 ...
##   ..- attr(*, "format.spss")= chr "F6.2"
##  $ puan : num [1:50] 9 8 6 8 10 4 6 5 7 7 ...
##   ..- attr(*, "format.spss")= chr "F6.2"
```

-   🔗 <https://www.statmodel.com/usersguide/chap3/ex3.1.dat>


```
##  [1] -0.354517  0.561655  0.315551  3.347049 -0.122389 -0.251276 -0.517996
##  [8]  1.888854  0.461254  2.237483
```

- 

```
##  [1] "   -0.354517     0.573051    -0.175230"
##  [2] "    0.561655    -0.368095     1.090042"
##  [3] "    0.315551    -0.577052     0.425472"
##  [4] "    3.347049     1.088520     1.149353"
##  [5] "   -0.122389    -0.694153    -0.766538"
##  [6] "   -0.251276    -0.017487    -1.367410"
##  [7] "   -0.517996    -0.817974    -1.559255"
##  [8] "    1.888854    -0.658335     1.007614"
##  [9] "    0.461254     0.463916    -0.898300"
## [10] "    2.237483     1.533398     0.180512"
```

## Veri Yazma


```r
ad  <-  c("Ali","Elif","Su","Deniz","Aras","Berk","Can","Ece","Efe","Arda")
boy <- c(160,165,170,155,167,162,169,158,160,164)
kilo <- c(50,55,57,50,48,65,58,62,45,47)
beden <- c("S","M","S","M","S","L","M","L","S","S")
df <- data.frame(ad, boy, kilo, beden)
df
```

<div class="kable-table">

|ad    | boy| kilo|beden |
|:-----|---:|----:|:-----|
|Ali   | 160|   50|S     |
|Elif  | 165|   55|M     |
|Su    | 170|   57|S     |
|Deniz | 155|   50|M     |
|Aras  | 167|   48|S     |
|Berk  | 162|   65|L     |
|Can   | 169|   58|M     |
|Ece   | 158|   62|L     |
|Efe   | 160|   45|S     |
|Arda  | 164|   47|S     |

</div>



```r
write.table(df, file="df.txt")# df dosyasi nerede, gorunumu nasil
```


```r
write.table(df, file="df.txt",row.names = FALSE,col.names = FALSE)
# karakter nesnler tirnak icinde ne yapmali?
```


```r
write.table(df, file="df.txt",row.names = FALSE,col.names = FALSE,quote=FALSE)
```



yeni gözlem eklemek istiyorsaniz append argümanı kullanılabilir.


```r
 ek <- data.frame(ad=c("Ahmet","Ali"), boy=c(180,170), kilo=c(60,70), 
                 beden=c("S","L"))
```


```r
write.table(ek, "df.txt",row.names=FALSE,
            col.names=FALSE,
            quote=FALSE,append=TRUE)
```


- **write.csv()** fonksiyonu kullanılarak yazılan veri dosyaları "," ile,

- **write.csv2()** fonksiyonu kullanılarak yazılan veri dosyaları ise ";" ile ayrılır iki fonksiyonun bir diğer farkı ise ondalık sayı ayıracıdır.

- write.csv ile yazdırılan dosyaların excelde açılması


### **cat()** fonksiyonu

-   Döngülerde sıklıkla ekrana bilgi yazdırmak amacıyla kullanılır, ancak dosya yazdırmak amacıyla da kullanabilmektedir.
-   fonksiyonlarla yapılan hesaplama çıktısı da yazabilmektedir.
-   Bu nedenle bir R oturumu sırasında not alınmak istenilen bilgileri bir dosyaya yazdırmak için kullanılabilir.


```r
 cat("ogrencilerin boy ortalamasi ", mean(boy), "\n",
      "ogrencilerin kilo ortalamasi", mean(kilo), "\n",
     file="bilgi.txt")
```

- \n ne ise yaradi?

## writeLines fonksiyonu


```r
writeLines("ogrencilerin boy ortalamasi: 163 cm\n",
            "ogrencilerin kilo ortalamasi: 53.7 kg",
            con="bilgi2.txt")
```

## ODEV

- 🔗 [Linkte](https://psyteachr.github.io/data-skills-v1/getting-to-know-the-data.html) yer alan sayfayı inceleyiniz. Bu sayfada  bir veri setini incelemeniz ve bu veri seti ile ilgili sorulara cevap vermeniz beklenemketedir.


- 🔗[Linkte](https://psyteachr.github.io/data-skills-v1/loading-data.html)  yer alan sayfada sizden iki veri setini okumanız beklenmeketdir. Bu iki veri setini okuduktan sonra da hazır kodları incelemeniz ve bu kodlar ile ilgili sorulara cevap vermeniz beklenmektedir.


☕ 

<!--chapter:end:08-veriokumayazma.Rmd-->

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

<div class="kable-table">

|country |continent | year| lifeExp|      pop| gdpPercap|
|:-------|:---------|----:|-------:|--------:|---------:|
|Canada  |Americas  | 1952|   68.75| 14785584|  11367.16|
|Canada  |Americas  | 1957|   69.96| 17010154|  12489.95|

</div>

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

<div class="kable-table">

| CNTSTUID| ST001D01T| ST004D01T|    ESCS|
|--------:|---------:|---------:|-------:|
| 79200768|        10|         2| -2.4521|
| 79201064|        10|         2| -2.1042|
| 79201118|        10|         1| -2.2700|
| 79201275|         9|         2|  0.0324|
| 79201481|         9|         2| -0.0674|
| 79201556|        10|         2|  0.3978|

</div>

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

<div class="kable-table">

| CNTSTUID| ST001D01T| ST004D01T|    ESCS|
|--------:|---------:|---------:|-------:|
| 79201575|        11|         2| -4.7546|
| 79205397|        10|         1| -4.7171|
| 79200690|         8|         2| -4.2914|
| 79201907|        10|         2| -4.2855|
| 79206542|        10|         2| -4.1966|
| 79200541|        11|         2| -4.1934|

</div>


- **desc()** fonksiyonu ile sıralama büyükten küçüğe de yapılabilir.


```r
arrange(df1,desc(ESCS)) %>% head(6)
```

<div class="kable-table">

| CNTSTUID| ST001D01T| ST004D01T|   ESCS|
|--------:|---------:|---------:|------:|
| 79201409|        10|         2| 2.7617|
| 79207242|        10|         2| 2.6174|
| 79203361|        10|         2| 2.2757|
| 79206271|        10|         2| 2.1771|
| 79203677|         9|         1| 1.9913|
| 79200191|         9|         1| 1.9197|

</div>


- Yaptığımız işlemleri pipe operatoru ile bağlayabilirsiniz.


```r
PISA_STU_2018 %>%
  select(CNTSTUID,ST001D01T,ST004D01T,ESCS) %>%
  arrange(ESCS) %>%
  head(6)
```

<div class="kable-table">

| CNTSTUID| ST001D01T| ST004D01T|    ESCS|
|--------:|---------:|---------:|-------:|
| 79201575|        11|         2| -4.7546|
| 79205397|        10|         1| -4.7171|
| 79200690|         8|         2| -4.2914|
| 79201907|        10|         2| -4.2855|
| 79206542|        10|         2| -4.1966|
| 79200541|        11|         2| -4.1934|

</div>

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

<div class="kable-table">

| CNTRYID|CNT | CNTSCHID| CNTSTUID|CYC  |NatCen |STRATUM |SUBNATIO | OECD| ADMINMODE| LANGTEST_QQQ| LANGTEST_COG| LANGTEST_PAQ| BOOKID| ST001D01T| ST003D02T| ST003D03T| ST004D01T| ST005Q01TA| ST006Q01TA| ST006Q02TA| ST006Q03TA| ST006Q04TA| ST007Q01TA| ST008Q01TA| ST008Q02TA| ST008Q03TA| ST008Q04TA| ST011Q01TA| ST011Q02TA| ST011Q03TA| ST011Q04TA| ST011Q05TA| ST011Q06TA| ST011Q07TA| ST011Q08TA| ST011Q09TA| ST011Q10TA| ST011Q11TA| ST011Q12TA| ST011Q16NA|ST011D17TA |ST011D18TA |ST011D19TA | ST012Q01TA| ST012Q02TA| ST012Q03TA| ST012Q05NA| ST012Q06NA| ST012Q07NA| ST012Q08NA| ST012Q09NA| ST013Q01TA| ST019AQ01T| ST019BQ01T| ST019CQ01T| ST021Q01TA| ST125Q01NA| ST126Q01TA| ST127Q01TA| ST127Q02TA| ST127Q03TA| ST022Q01TA| ST023Q01TA| ST023Q02TA| ST023Q03TA| ST023Q04TA| ST023Q05TA| ST097Q01TA| ST097Q02TA| ST097Q03TA| ST097Q04TA| ST097Q05TA| ST100Q01TA| ST100Q02TA| ST100Q03TA| ST100Q04TA| ST102Q01TA| ST102Q02TA| ST102Q03TA| ST102Q04TA| ST211Q01HA| ST211Q02HA| ST211Q03HA| ST212Q01HA| ST212Q02HA| ST212Q03HA| ST104Q02NA| ST104Q03NA| ST104Q04NA| ST213Q01HA| ST213Q02HA| ST213Q03HA| ST213Q04HA| ST150Q01IA| ST150Q02IA| ST150Q03IA| ST150Q04HA| ST152Q05IA| ST152Q06IA| ST152Q07IA| ST152Q08IA| ST154Q01HA| ST153Q01HA| ST153Q02HA| ST153Q03HA| ST153Q04HA| ST153Q05HA| ST153Q06HA| ST153Q08HA| ST153Q09HA| ST153Q10HA| ST158Q01HA| ST158Q02HA| ST158Q03HA| ST158Q04HA| ST158Q05HA| ST158Q06HA| ST158Q07HA| ST160Q01IA| ST160Q02IA| ST160Q03IA| ST160Q04IA| ST160Q05IA| ST167Q01IA| ST167Q02IA| ST167Q03IA| ST167Q04IA| ST167Q05IA| ST168Q01HA| ST175Q01IA| ST176Q01IA| ST176Q02IA| ST176Q03IA| ST176Q05IA| ST176Q06IA| ST176Q07IA| ST161Q01HA| ST161Q02HA| ST161Q03HA| ST161Q06HA| ST161Q07HA| ST161Q08HA| ST163Q02HA| ST163Q03HA| ST163Q04HA| ST164Q01IA| ST164Q02IA| ST164Q03IA| ST164Q04IA| ST164Q05IA| ST164Q06IA| ST165Q01IA| ST165Q02IA| ST165Q03IA| ST165Q04IA| ST165Q05IA| ST166Q01HA| ST166Q02HA| ST166Q03HA| ST166Q04HA| ST166Q05HA| ST016Q01NA| ST036Q05TA| ST036Q06TA| ST036Q08TA| ST225Q01HA| ST225Q02HA| ST225Q03HA| ST225Q04HA| ST225Q05HA| ST225Q06HA| ST181Q02HA| ST181Q03HA| ST181Q04HA| ST182Q03HA| ST182Q04HA| ST182Q05HA| ST182Q06HA| ST183Q01HA| ST183Q02HA| ST183Q03HA| ST184Q01HA| ST185Q01HA| ST185Q02HA| ST185Q03HA| ST186Q05HA| ST186Q06HA| ST186Q07HA| ST186Q10HA| ST186Q09HA| ST186Q02HA| ST186Q01HA| ST186Q08HA| ST186Q03HA| ST208Q01HA| ST208Q02HA| ST208Q04HA| ST188Q01HA| ST188Q02HA| ST188Q03HA| ST188Q06HA| ST188Q07HA| ST034Q01TA| ST034Q02TA| ST034Q03TA| ST034Q04TA| ST034Q05TA| ST034Q06TA| ST196Q02HA| ST196Q03HA| ST196Q04HA| ST196Q05HA| ST196Q06HA| ST196Q07HA| ST197Q01HA| ST197Q02HA| ST197Q04HA| ST197Q07HA| ST197Q08HA| ST197Q09HA| ST197Q12HA| ST215Q01HA| ST215Q02HA| ST215Q03HA| ST215Q04HA| ST215Q05HA| ST216Q01HA| ST216Q02HA| ST216Q03HA| ST216Q04HA| ST216Q05HA| ST216Q06HA| ST218Q01HA| ST218Q02HA| ST218Q03HA| ST218Q04HA| ST218Q05HA| ST218Q06HA| ST218Q07HA| ST222Q01HA| ST222Q03HA| ST222Q04HA| ST222Q05HA| ST222Q06HA| ST222Q08HA| ST222Q09HA| ST222Q10HA| ST214Q01HA| ST214Q02HA| ST214Q03HA| ST214Q06HA| ST220Q01HA| ST220Q02HA| ST220Q03HA| ST220Q04HA| ST217Q01HA| ST217Q02HA| ST217Q03HA| ST217Q04HA| ST217Q05HA| ST219Q01HA| ST219Q02HA| ST219Q03HA| ST219Q04HA| ST219Q05HA| ST219Q06HA| ST204Q02HA| ST204Q03HA| ST204Q04HA| ST204Q05HA| ST177Q01HA| ST177Q02HA| ST177Q03HA| ST189Q01HA| ST221Q01HA| ST221Q02HA| ST221Q03HA| ST221Q04HA| ST221Q05HA| ST221Q06HA| ST221Q07HA| ST221Q08HA| ST221Q09HA| ST221Q11HA| ST223Q02HA| ST223Q04HA| ST223Q05HA| ST223Q08HA| ST123Q02NA| ST123Q03NA| ST123Q04NA| ST205Q01HA| ST205Q02HA| ST205Q03HA| ST205Q04HA| ST059Q01TA| ST059Q02TA| ST059Q03TA| ST059Q04HA| ST060Q01NA| ST061Q01NA| ST062Q01TA| ST062Q02TA| ST062Q03TA| ST038Q03NA| ST038Q04NA| ST038Q05NA| ST038Q06NA| ST038Q07NA| ST038Q08NA| ST207Q01HA| ST207Q02HA| ST207Q03HA| ST207Q04HA| ST207Q05HA| ST206Q01HA| ST206Q02HA| ST206Q03HA| ST206Q04HA| IC001Q01TA| IC001Q02TA| IC001Q03TA| IC001Q04TA| IC001Q05TA| IC001Q06TA| IC001Q07TA| IC001Q08TA| IC001Q09TA| IC001Q10TA| IC001Q11TA| IC009Q01TA| IC009Q02TA| IC009Q03TA| IC009Q05NA| IC009Q06NA| IC009Q07NA| IC009Q08TA| IC009Q09TA| IC009Q10NA| IC009Q11NA| IC002Q01HA| IC004Q01HA| IC005Q01TA| IC006Q01TA| IC007Q01TA| IC150Q01HA| IC150Q02HA| IC150Q03HA| IC150Q04HA| IC150Q05HA| IC150Q06HA| IC150Q07HA| IC150Q08HA| IC150Q09HA| IC151Q01HA| IC151Q02HA| IC151Q03HA| IC151Q04HA| IC151Q05HA| IC151Q06HA| IC151Q07HA| IC151Q08HA| IC151Q09HA| IC152Q01HA| IC152Q02HA| IC152Q03HA| IC152Q04HA| IC152Q05HA| IC152Q06HA| IC152Q07HA| IC152Q08HA| IC152Q09HA| IC008Q01TA| IC008Q02TA| IC008Q03TA| IC008Q04TA| IC008Q05TA| IC008Q07NA| IC008Q08TA| IC008Q09TA| IC008Q10TA| IC008Q11TA| IC008Q12TA| IC008Q13NA| IC010Q01TA| IC010Q02NA| IC010Q03TA| IC010Q04TA| IC010Q05NA| IC010Q06NA| IC010Q07TA| IC010Q08TA| IC010Q09NA| IC010Q10NA| IC010Q11HA| IC010Q12HA| IC011Q01TA| IC011Q02TA| IC011Q03TA| IC011Q04TA| IC011Q05TA| IC011Q06TA| IC011Q07TA| IC011Q08TA| IC011Q09TA| IC011Q10HA| IC013Q01NA| IC013Q04NA| IC013Q05NA| IC013Q11NA| IC013Q12NA| IC013Q13NA| IC014Q03NA| IC014Q04NA| IC014Q06NA| IC014Q08NA| IC014Q09NA| IC015Q02NA| IC015Q03NA| IC015Q05NA| IC015Q07NA| IC015Q09NA| IC016Q01NA| IC016Q02NA| IC016Q04NA| IC016Q05NA| IC016Q07NA| IC169Q01HA| EC031Q01TA| EC032Q01TA| EC033Q01NA| EC150Q01WA| EC150Q02WA| EC150Q03WA| EC150Q04WA| EC150Q05WA| EC150Q06WA| EC150Q07WA| EC150Q08WA| EC150Q09WA| EC150Q10WA| EC151Q01WA| EC151Q01WB| EC151Q01WC| EC151Q02WA| EC151Q02WB| EC151Q02WC| EC151Q03WA| EC151Q03WB| EC151Q03WC| EC151Q04WA| EC151Q04WB| EC151Q04WC| EC151Q05WA| EC151Q05WB| EC151Q05WC| EC152Q01HA| EC153Q01HA| EC153Q02HA| EC153Q03HA| EC153Q04HA| EC153Q05HA| EC153Q06HA| EC153Q07HA| EC153Q08HA| EC153Q09HA| EC153Q10HA| EC153Q11HA| EC160Q01HA| EC158Q01HA| EC158Q02HA| EC159Q01HA| EC159Q02HA| EC163Q01HA| EC163Q02HA| EC163Q03HA| EC163Q04HA| EC163Q05HA| EC163Q06HA| EC163Q07HA| EC162Q01HA| EC162Q02HA| EC162Q03HA| EC162Q04HA| EC162Q05HA| EC162Q06HA| EC162Q07HA| EC162Q08HA| EC154Q01IA| EC154Q02IA| EC154Q03IA| EC154Q04HA| EC154Q05IA| EC154Q06IA| EC154Q07IA| EC154Q08HA| EC154Q09IA| EC012Q01NA| EC012Q02NA| EC012Q04NA| EC012Q06NA| EC012Q07NA| EC012Q08NA| EC012Q13HA| EC012Q12NA| EC155Q01DA| EC155Q02DA| EC155Q03DA| EC155Q04HA| EC155Q05HA| WB150Q01HA| WB151Q01HA| WB152Q01HA| WB153Q01HA| WB153Q02HA| WB153Q03HA| WB153Q04HA| WB153Q05HA| WB154Q01HA| WB154Q02HA| WB154Q03HA| WB154Q04HA| WB154Q05HA| WB154Q06HA| WB154Q07HA| WB154Q08HA| WB154Q09HA| WB155Q01HA| WB155Q02HA| WB155Q03HA| WB155Q04HA| WB155Q05HA| WB155Q06HA| WB155Q07HA| WB155Q08HA| WB155Q09HA| WB155Q10HA| WB156Q01HA| WB158Q01HA| WB160Q01HA| WB161Q01HA| WB162Q01HA| WB162Q02HA| WB162Q03HA| WB162Q04HA| WB162Q05HA| WB162Q06HA| WB162Q07HA| WB162Q08HA| WB162Q09HA| WB163Q01HA| WB163Q02HA| WB163Q03HA| WB163Q04HA| WB163Q05HA| WB163Q06HA| WB163Q07HA| WB163Q08HA| WB164Q01HA| WB165Q01HA| WB166Q01HA| WB166Q02HA| WB166Q03HA| WB166Q04HA| WB167Q01HA| WB168Q01HA| WB168Q02HA| WB168Q03HA| WB168Q04HA| WB171Q01HA| WB171Q02HA| WB171Q03HA| WB171Q04HA| WB172Q01HA| WB173Q01HA| WB173Q02HA| WB173Q03HA| WB173Q04HA| WB176Q01HA| WB177Q01HA| WB177Q02HA| WB177Q03HA| WB177Q04HA| WB032Q01NA| WB032Q02NA| WB031Q01NA| WB178Q01HA| WB178Q02HA| WB178Q03HA| WB178Q04HA| WB178Q05HA| WB178Q06HA| WB178Q07HA| FL150Q01TA| FL150Q02TA| FL150Q03TA| FL151Q01HA| FL151Q02HA| FL164Q01HA| FL164Q02HA| FL164Q03HA| FL164Q04HA| FL164Q05HA| FL164Q06HA| FL164Q07HA| FL164Q08HA| FL164Q09HA| FL164Q10HA| FL164Q11HA| FL164Q12HA| FL164Q13HA| FL164Q14HA| FL164Q15HA| FL164Q16HA| FL164Q17HA| FL164Q18HA| FL165Q01HA| FL165Q02HA| FL165Q03HA| FL165Q04HA| FL166Q01HA| FL166Q02HA| FL166Q03HA| FL166Q05HA| FL166Q06HA| FL166Q07HA| FL153Q01HA| FL153Q02HA| FL153Q03HA| FL153Q04HA| FL153Q05HA| FL153Q06HA| FL167Q01HA| FL167Q02HA| FL167Q03HA| FL167Q04HA| FL167Q05HA| FL156Q01TA| FL156Q02TA| FL156Q03TA| FL156Q04TA| FL156Q05TA| FL156Q06TA| FL156Q07HA| FL159Q01HA| FL159Q02HA| FL159Q03HA| FL159Q04HA| FL160Q01HA| FL160Q02HA| FL160Q03HA| FL160Q04HA| FL161Q01HA| FL161Q02HA| FL161Q03HA| FL162Q01HA| FL162Q02HA| FL162Q03HA| FL162Q04HA| FL162Q05HA| FL162Q06HA| FL163Q01HA| FL163Q02HA| FL163Q03HA| FL163Q04HA| FL163Q05HA| FL168Q01HA| FL168Q02HA| FL168Q03HA| FL168Q04HA| FL168Q05HA| FL168Q06HA| FL168Q07HA| FL168Q08HA| FL169Q01HA| FL169Q02HA| FL169Q03HA| FL169Q04HA| PA001Q01TA| PA001Q02TA| PA001Q03TA| PA003Q01TA| PA003Q02TA| PA003Q03TA| PA003Q04HA| PA003Q05IA| PA003Q06IA| PA003Q07IA| PA154Q01IA| PA154Q02IA| PA154Q03IA| PA154Q04IA| PA154Q05IA| PA154Q06IA| PA154Q07IA| PA154Q08IA| PA154Q09IA| PA154Q10HA| PA155Q01IA| PA156Q01HA| PA156Q02HA| PA156Q03HA| PA156Q04HA| PA004Q02NA| PA004Q03NA| PA004Q04NA| PA008Q01TA| PA008Q02TA| PA008Q03TA| PA008Q04TA| PA008Q05TA| PA008Q06NA| PA008Q07NA| PA008Q08NA| PA008Q09NA| PA008Q10NA| PA009Q01NA| PA009Q02NA| PA009Q03NA| PA009Q04NA| PA009Q05NA| PA009Q06NA| PA009Q07NA| PA009Q08NA| PA009Q09NA| PA009Q10NA| PA009Q11NA| PA007Q01TA| PA007Q02TA| PA007Q03TA| PA007Q04TA| PA007Q05TA| PA007Q06TA| PA007Q07TA| PA007Q09NA| PA007Q11NA| PA007Q12NA| PA007Q13NA| PA007Q14NA| PA007Q15NA| PA005Q01TA| PA006Q01TA| PA006Q02TA| PA006Q03TA| PA006Q04TA| PA006Q05TA| PA006Q06TA| PA006Q07TA| PA006Q08TA| PA006Q09TA| PA006Q10TA| PA006Q11TA| PA006Q12HA| PA006Q13HA| PA006Q14HA| PA158Q01HA| PA158Q02IA| PA158Q03HA| PA158Q04IA| PA158Q05HA| PA159Q01HA| PA160Q01HA| PA160Q02HA| PA160Q03HA| PA160Q04HA| PA160Q05HA| PA161Q01HA| PA161Q02HA| PA161Q03HA| PA161Q05HA| PA161Q06HA| PA161Q07HA| PA162Q01HA| PA163Q01HA| PA166Q01HA| PA167Q02HA| PA167Q03HA| PA167Q04HA| PA167Q05HA| PA168Q01HA| PA168Q02HA| PA168Q03HA| PA168Q06HA| PA169Q01HA| PA169Q02HA| PA169Q03HA| PA169Q04HA| PA169Q05HA| PA169Q06HA| PA170Q01HA| PA170Q02HA| PA170Q04HA| PA170Q07HA| PA170Q08HA| PA170Q09HA| PA170Q12HA| PA171Q01HA| PA171Q03HA| PA171Q04HA| PA171Q05HA| PA171Q06HA| PA171Q08HA| PA171Q09HA| PA171Q10HA| PA172Q01WA| PA172Q02WA| PA172Q03WA| PA172Q04WA| PA172Q05WA| PA172Q06WA| PA018Q01NA| PA018Q02NA| PA018Q03NA| PA177Q01HA| PA177Q02HA| PA177Q03HA| PA177Q04HA| PA177Q05HA| PA177Q06HA| PA177Q07HA| PA177Q08HA| PA180Q01HA| PA182Q01HA| PA175Q01HA| PA175Q02HA| PA041Q01TA| PA042Q01TA| EFFORT1| EFFORT2|OCOD1 |OCOD2 |OCOD3 | GRADE|   AGE|PROGN    |COBN_S |COBN_M |COBN_F | LANGN| ISCEDL| ISCEDD| ISCEDO| MISCED| FISCED| HISCED| PARED| MISCED_D| FISCED_D| HISCED_D| PAREDINT| BMMJ1| BFMJ2| HISEI| LANGMOTHER| LANGFATHER| LANGSIBLINGS| LANGFRIEND| LANGSCHMATES| IMMIG| DURECEC| REPEAT|  BSMJ| MMINS| LMINS| SMINS| TMINS| FCFMLRTY| SCCHANGE| CHANGE| STUBMI|    ESCS| UNDREM| METASUM| METASPAM| ICTHOME| ICTSCH| HOMEPOS| CULTPOSS|  HEDRES|  WEALTH|  ICTRES| DISCLIMA| TEACHSUP|  DIRINS| PERFEED| EMOSUPS| STIMREAD| ADAPTIVITY| TEACHINT| JOYREAD| SCREADCOMP| SCREADDIFF| PISADIFF| PERCOMP| PERCOOP| ATTLNACT| COMPETE| WORKMAST| GFOFAIL|   EUDMO|    SWBP| RESILIENCE| MASTGOAL| GCSELFEFF| GCAWARE|  ATTIMM| INTCULT| PERSPECT| COGFLEX| RESPECT|  AWACOM| GLOBMIND| DISCRIM|  BELONG| BEINGBULLIED|  ENTUSE| HOMESCH|  USESCH|  INTICT| COMPICT|  AUTICT| SOIAICT| ICTCLASS| ICTOUTSIDE| INFOCAR| INFOJOB1| INFOJOB2| FLCONFIN| FLCONICT| FLSCHOOL| FLFAMILY| CURSUPP| EMOSUPP| PQSCHOOL| PASCHPOL| PRESUPP| JOYREADP| ATTIMMP| INTCULTP| GCAWAREP| BODYIMA| SOCONPA| W_FSTUWT| W_FSTURWT1| W_FSTURWT2| W_FSTURWT3| W_FSTURWT4| W_FSTURWT5| W_FSTURWT6| W_FSTURWT7| W_FSTURWT8| W_FSTURWT9| W_FSTURWT10| W_FSTURWT11| W_FSTURWT12| W_FSTURWT13| W_FSTURWT14| W_FSTURWT15| W_FSTURWT16| W_FSTURWT17| W_FSTURWT18| W_FSTURWT19| W_FSTURWT20| W_FSTURWT21| W_FSTURWT22| W_FSTURWT23| W_FSTURWT24| W_FSTURWT25| W_FSTURWT26| W_FSTURWT27| W_FSTURWT28| W_FSTURWT29| W_FSTURWT30| W_FSTURWT31| W_FSTURWT32| W_FSTURWT33| W_FSTURWT34| W_FSTURWT35| W_FSTURWT36| W_FSTURWT37| W_FSTURWT38| W_FSTURWT39| W_FSTURWT40| W_FSTURWT41| W_FSTURWT42| W_FSTURWT43| W_FSTURWT44| W_FSTURWT45| W_FSTURWT46| W_FSTURWT47| W_FSTURWT48| W_FSTURWT49| W_FSTURWT50| W_FSTURWT51| W_FSTURWT52| W_FSTURWT53| W_FSTURWT54| W_FSTURWT55| W_FSTURWT56| W_FSTURWT57| W_FSTURWT58| W_FSTURWT59| W_FSTURWT60| W_FSTURWT61| W_FSTURWT62| W_FSTURWT63| W_FSTURWT64| W_FSTURWT65| W_FSTURWT66| W_FSTURWT67| W_FSTURWT68| W_FSTURWT69| W_FSTURWT70| W_FSTURWT71| W_FSTURWT72| W_FSTURWT73| W_FSTURWT74| W_FSTURWT75| W_FSTURWT76| W_FSTURWT77| W_FSTURWT78| W_FSTURWT79| W_FSTURWT80| UNIT| WVARSTRR| PV1MATH| PV2MATH| PV3MATH| PV4MATH| PV5MATH| PV6MATH| PV7MATH| PV8MATH| PV9MATH| PV10MATH| PV1READ| PV2READ| PV3READ| PV4READ| PV5READ| PV6READ| PV7READ| PV8READ| PV9READ| PV10READ| PV1SCIE| PV2SCIE| PV3SCIE| PV4SCIE| PV5SCIE| PV6SCIE| PV7SCIE| PV8SCIE| PV9SCIE| PV10SCIE| PV1GLCM| PV2GLCM| PV3GLCM| PV4GLCM| PV5GLCM| PV6GLCM| PV7GLCM| PV8GLCM| PV9GLCM| PV10GLCM| PV1RCLI| PV2RCLI| PV3RCLI| PV4RCLI| PV5RCLI| PV6RCLI| PV7RCLI| PV8RCLI| PV9RCLI| PV10RCLI| PV1RCUN| PV2RCUN| PV3RCUN| PV4RCUN| PV5RCUN| PV6RCUN| PV7RCUN| PV8RCUN| PV9RCUN| PV10RCUN| PV1RCER| PV2RCER| PV3RCER| PV4RCER| PV5RCER| PV6RCER| PV7RCER| PV8RCER| PV9RCER| PV10RCER| PV1RTSN| PV2RTSN| PV3RTSN| PV4RTSN| PV5RTSN| PV6RTSN| PV7RTSN| PV8RTSN| PV9RTSN| PV10RTSN| PV1RTML| PV2RTML| PV3RTML| PV4RTML| PV5RTML| PV6RTML| PV7RTML| PV8RTML| PV9RTML| PV10RTML|   SENWT|VER_DAT          | test|
|-------:|:---|--------:|--------:|:----|:------|:-------|:--------|----:|---------:|------------:|------------:|------------:|------:|---------:|---------:|---------:|---------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|:----------|:----------|:----------|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|-------:|-------:|:-----|:-----|:-----|-----:|-----:|:--------|:------|:------|:------|-----:|------:|------:|------:|------:|------:|------:|-----:|--------:|--------:|--------:|--------:|-----:|-----:|-----:|----------:|----------:|------------:|----------:|------------:|-----:|-------:|------:|-----:|-----:|-----:|-----:|-----:|--------:|--------:|------:|------:|-------:|------:|-------:|--------:|-------:|------:|-------:|--------:|-------:|-------:|-------:|--------:|--------:|-------:|-------:|-------:|--------:|----------:|--------:|-------:|----------:|----------:|--------:|-------:|-------:|--------:|-------:|--------:|-------:|-------:|-------:|----------:|--------:|---------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|--------:|-------:|-------:|------------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|----------:|-------:|--------:|--------:|--------:|--------:|--------:|--------:|-------:|-------:|--------:|--------:|-------:|--------:|-------:|--------:|--------:|-------:|-------:|--------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|----:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|:----------------|----:|
|     792|TUR | 79200001| 79201275|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|     21|         9|         9|      2002|         2|          1|         NA|          1|         NA|         NA|          1|         NA|          1|         NA|         NA|          1|          1|          1|          1|          2|          1|          2|          2|          2|          1|          2|          1|          2|0792001    |0792002    |0792002    |          3|          1|          1|          2|          2|          1|          1|          1|          1|          1|          1|          1|         NA|          6|          5|          1|          1|          1|          1|          4|          4|          4|          4|          4|          2|          2|          3|          1|          1|          3|          2|          1|          4|          2|          3|          4|          3|          3|          2|          2|          2|          2|          2|          3|          2|          3|          2|          2|          2|          2|          4|          4|          4|          4|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          3|          1|          1|          3|          3|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          2|          2|          2|          1|          1|          1|          6|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|          2|          2|          2|          0|          0|          0|         NA|          0|          1|          4|          3|          4|          1|          1|          1|          1|          1|          1|          1|          3|          1|          1|          1|          4|          2|          1|          1|          4|          1|          2|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|          2|          3|          2|          2|          3|          1|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          3|          3|          1|          2|          1|          3|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|          1|          3|          2|          2|          1|          2|          1|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          2|          2|          2|          2|          1|          1|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|         NA|          3|          2|          2|          2|          2|          5|          6|          6|          4|         40|         40|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          2|          2|          3|          2|          2|          2|          2|          1|          1|          1|          1|          1|          3|          1|          2|          1|          2|          3|          1|          1|          1|          1|          2|          2|          2|          3|          2|          1|          1|          2|          1|          5|          5|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          3|          4|          4|          1|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|      10|      10|2330  |2330  |2211  |    -1| 15.58|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      6|      6|      6|    16|        6|        6|        6|       16| 82.41| 82.41| 82.41|         NA|         NA|           NA|         NA|           NA|     1|       1|      0| 88.70|   240|   200|   240|  1600|       NA|       NA|     NA|     NA|  0.0324|  -0.60|   -1.72|    -1.41|       9|      9| -2.1008|  -2.7469| -0.6853| -2.1121| -1.7005|  -1.1699|  -0.4060| -1.0499|  0.2682|      NA|  -0.6200|    -0.5786|  -1.0615| -1.1538|     -0.825|     1.2421|   0.2705| -0.6142| -0.9391|  -0.6583|  1.1811|  -2.7365| -1.8939| -2.1464| -1.2568|    -1.4832|  -1.3162|   -2.7142| -0.0549| -1.2083| -0.2157|  -0.3405|  1.3823| -1.2781| -1.3933|   0.2910| -1.1549| -0.4217|       1.1625| -2.7049| -0.5991| -1.0707| -2.9336| -2.6033| -2.5144|  0.2639|   1.0418|    -1.3048|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 417.314| 486.246| 419.767| 413.368| 508.158| 475.248| 527.383| 482.872| 477.418|  476.539| 393.006| 428.757| 364.850| 382.522| 378.563| 416.048| 395.846| 383.782| 374.509|  381.877| 402.112| 431.478| 384.063| 472.941| 420.800| 472.894| 460.407| 465.356| 439.954|  442.546|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 377.648| 346.106| 347.468| 351.544| 464.958| 406.800| 305.063| 415.645| 451.572|  332.146| 418.336| 387.692| 376.644| 348.832| 469.856| 438.034| 377.209| 433.141| 463.976|  390.554| 370.646| 356.020| 346.501| 346.212| 425.656| 396.229| 416.122| 421.807| 457.353|  390.627| 419.099| 390.744| 410.400| 377.828| 443.815| 406.021| 393.957| 420.428| 398.023|  462.478| 400.889| 416.115| 426.449| 396.449| 425.235| 391.150| 373.368| 416.023| 417.897|  416.855| 0.80261|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200001| 79202343|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|     22|        11|         3|      2002|         2|          1|          1|          1|          1|         NA|          1|         NA|          1|         NA|         NA|          1|          1|          1|          1|          2|          1|          2|          2|          2|          2|          2|          1|          1|0792001    |0792001    |0792001    |          3|          4|          3|          4|          3|          3|          1|          3|          1|          1|          1|          1|         NA|          6|          6|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          2|          2|          4|          3|          3|          4|          3|          2|          3|          2|          3|          3|          4|          1|          1|          2|          3|          3|          4|          1|          1|          1|          1|          2|          2|          2|          2|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          1|          2|         NA|          5|         NA|          1|          5|          5|          1|          4|          4|          4|          2|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          0|          4|          2|          3|          0|          0|          1|         NA|          0|          0|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          3|          4|          3|          4|          3|          2|          4|          1|          3|          1|          4|          2|          4|          1|          2|          2|          4|          3|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|         NA|          1|         NA|         NA|         NA|         NA|         NA|         NA|         NA|          1|          2|          3|          4|          5|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          5|          1|          1|          1|          1|          5|          5|          5|          5|          5|          3|         NA|         NA|         NA|         NA|         NA|          3|          3|          2|          3|          2|          1|          1|          3|          2|          2|          1|          2|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          0|          2|          0|         20|         30|          4|          4|          2|          1|          1|          1|          1|          1|          1|          4|          1|          1|          1|          1|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          5|          7|          7|          2|          1|          2|          1|          3|          4|          4|          4|          1|          4|          1|          2|          2|          5|          4|          4|          4|          5|          5|          5|          5|          5|          5|         NA|         NA|         NA|         NA|          5|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|          3|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          4|          4|          4|          4|          4|          4|          3|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          3|          3|          4|         NA|          3|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|       7|       9|9701  |6111  |2330  |     1| 16.08|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      6|      6|      6|    16|        6|        6|        6|       16| 17.00| 11.56| 17.00|         NA|         NA|           NA|         NA|           NA|     1|       2|      0| 82.41|     0|    60|    60|   600|       NA|       NA|     NA|     NA| -0.4280|  -1.64|   -1.72|    -1.41|      11|     10| -0.2441|  -1.2687| -1.0118|  0.6090| -0.1120|  -1.4882|  -1.5550| -0.5066|  1.1225| -2.4468|  -2.3003|    -1.6010|  -2.2177| -0.1119|     -0.314|     0.2426|   0.2705| -1.9892| -1.6237|  -1.6038|  2.0054|  -2.7365| -1.8939|  1.1963|  0.6502|     1.5900|  -1.4972|   -2.6739|      NA| -0.6155| -0.0180|  -0.2098| -0.8312| -3.1739| -2.7948|       NA| -1.1549| -1.2605|      -0.7823|      NA|  2.3702|  3.3041|  2.6186|  1.4987|  2.0258|  1.4359|   0.2764|     0.5477|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 319.885| 325.236| 298.124| 347.893| 344.137| 332.804| 309.840| 414.770| 310.236|  393.137| 319.453| 333.203| 345.495| 339.966| 346.631| 336.530| 325.728| 322.760| 315.270|  302.398| 366.331| 434.453| 385.126| 406.671| 436.551| 410.509| 382.595| 415.349| 392.922|  369.015|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 283.543| 366.617| 279.752| 300.736| 324.928| 291.124| 291.853| 289.940| 254.055|  227.516| 358.106| 363.373| 337.079| 305.745| 345.937| 316.643| 330.522| 345.601| 305.511|  333.845| 357.716| 390.257| 312.117| 343.106| 459.546| 320.759| 363.881| 368.221| 351.077|  367.712| 349.881| 326.972| 361.684| 320.697| 356.205| 366.312| 364.327| 303.503| 310.790|  355.886| 392.458| 301.654| 400.555| 347.418| 370.830| 351.170| 382.755| 390.538| 411.888|  355.742| 0.80261|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200001| 79203553|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|     15|        10|         1|      2002|         1|          2|         NA|          1|          1|         NA|          2|         NA|         NA|          1|         NA|          1|          1|          1|          1|         NA|          1|          1|          1|          1|          1|          2|          1|          1|0792001    |0792002    |0792001    |          3|          2|          1|          4|          3|          3|          1|          2|          5|          1|          1|          1|         NA|          2|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          3|          2|          2|          2|          1|          1|          1|          3|          1|          2|          2|          3|          3|          2|          1|          2|          2|          2|          2|          2|          2|          2|          3|          2|          1|          1|          1|          1|          2|          2|          2|          2|          4|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          3|          4|          1|          2|          1|          3|          4|          4|          1|          2|          3|          2|          5|          4|          4|          2|          3|          2|          3|          2|          2|          3|          2|          2|          3|          1|          5|          5|          4|          6|          6|          2|          2|          3|          4|          5|          6|          4|          4|          4|          4|          4|          1|          2|          2|          2|          0|          0|          0|         NA|          0|          1|          3|          4|          4|          3|          3|          3|          3|          1|          2|          4|          3|          3|          2|          3|          3|          4|          2|          2|          2|          4|          3|          3|          2|          2|          2|          3|          3|          4|          3|          2|          3|          2|          4|          4|          3|          4|          2|          4|          4|          3|          3|          3|          3|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          2|          1|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          4|          4|          4|          1|          1|          1|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          3|          3|          3|          3|          2|          2|          3|          5|          6|          7|          6|         40|         40|          2|          1|          1|          2|          2|          4|          1|          1|          4|          4|          4|          4|          4|          4|          3|          3|          3|          3|          2|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          3|          3|          3|          3|          2|          2|          2|          2|          2|          2|          3|          4|          2|          6|          7|          1|          1|          4|          4|          1|          1|          1|          1|          2|          2|          2|          2|          4|          2|          4|          2|          2|          2|          4|          4|          1|          1|          4|          5|          4|          5|          3|          1|          1|          2|          4|          1|          1|          4|          3|          1|          4|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          3|          2|          4|          3|          4|          2|          3|          3|          3|          2|          2|          3|          3|          2|          3|          3|          3|          3|          3|          2|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|       8|      10|2221  |9703  |5111  |     0| 16.25|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      6|      5|      6|    16|        6|        5|        6|       16| 68.70| 17.00| 68.70|         NA|         NA|           NA|         NA|           NA|     1|       4|      0| 46.76|   240|   200|   280|  1600|       NA|       NA|     NA|     NA|  0.6187|   0.80|    0.98|    -1.41|      11|      6| -0.0982|   0.6014| -0.5089| -0.6098|  0.0154|   0.1625|   0.7628|  0.0351| -0.3253| -0.6576|  -0.6200|    -1.0467|  -0.8687|  1.1914|     -0.849|     0.4090|   0.7323| -0.2309|  0.6012|  -0.6583|  1.2643|  -0.1015| -0.3288| -0.3121| -1.1176|    -0.0960|  -1.0266|    0.5471|  2.3015|  0.9840|  0.2865|  -1.7137| -1.6677|  0.9289| -0.1577|   0.2910|  0.5881| -1.2487|       1.7757| -0.6642| -0.0861|  0.3558| -0.1436| -0.1996| -0.7462|  0.5149|   0.5207|     0.5761|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 415.225| 440.810| 484.132| 443.869| 465.435| 439.322| 541.338| 560.146| 499.883|  442.704| 518.787| 519.112| 502.570| 460.873| 493.765| 487.487| 545.821| 533.014| 560.481|  512.165| 497.778| 498.176| 496.351| 481.535| 446.003| 471.244| 488.351| 485.299| 488.595|  487.027|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 473.410| 503.853| 410.128| 449.512| 456.477| 465.956| 490.658| 481.180| 502.043|  510.345| 479.546| 544.253| 451.091| 449.859| 515.263| 495.030| 507.116| 502.315| 500.315|  511.370| 533.638| 567.418| 490.035| 544.260| 518.100| 541.488| 551.262| 545.764| 505.330|  547.064| 476.441| 511.302| 466.972| 513.422| 511.897| 507.532| 495.385| 513.871| 537.022|  463.353| 503.396| 524.080| 483.114| 521.571| 534.724| 546.075| 496.663| 530.087| 597.237|  532.370| 0.80261|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200001| 79204714|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|      6|        10|         1|      2002|         2|          1|         NA|          1|         NA|         NA|          1|          2|          2|          2|         NA|          1|          1|          1|          2|          1|          1|          2|          2|          2|          1|          1|          1|          2|0792001    |0792002    |0792001    |          2|          2|          2|          2|          1|          1|          1|          1|          2|          1|          1|          1|         NA|          8|          5|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          4|          4|          3|          4|          2|          1|          1|          1|          1|          1|          3|         NA|          2|          4|          4|          2|          4|          3|          4|          4|          4|          4|          2|          3|          3|          2|          2|          3|          4|          4|          4|          4|          2|          2|          1|          1|          2|          2|          1|          2|         NA|          2|          1|          1|          1|          2|          1|          1|          1|          2|          2|          2|          3|          1|          3|          2|          4|          4|          2|          1|          1|          2|          3|          3|          3|          3|          2|          2|          2|          2|          3|          1|          3|          3|          3|          2|          2|          2|          2|          3|          6|          2|          2|          3|          2|          6|          6|          6|          3|          1|          2|          1|          1|          0|          1|          1|          1|          0|          0|          0|         NA|          0|          1|          4|          4|          4|          3|          3|          4|          3|          4|          4|          4|          2|          4|          2|          4|          1|          1|          1|         NA|          4|          3|          2|          2|          2|          3|          3|         NA|          3|          3|          3|          3|          4|          2|          2|          2|          3|          2|         NA|          2|          3|          2|          3|          3|          3|          3|          3|          3|          3|         NA|          2|          2|          1|          1|          2|          1|          1|         NA|          2|          2|          3|          3|          3|         NA|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          4|          3|          5|          1|         18|         40|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          2|          2|          2|          2|          3|          1|          1|          1|          1|          1|          2|          3|          2|          1|          1|          1|          1|          1|          3|          4|          3|          3|          4|          4|          4|          4|         NA|          2|          1|          1|          3|          3|          2|          3|         NA|          3|          2|          1|          2|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          1|          1|          2|          1|          3|          1|          5|          1|          1|          1|          1|          1|          1|          4|          4|          3|          2|          1|          3|          3|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|      10|       1|9701  |6111  |0210  |     0| 16.25|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      6|      4|      6|    16|        6|        4|        6|       16| 17.00| 11.56| 17.00|         NA|         NA|           NA|         NA|           NA|     1|      NA|      0| 51.63|   120|   160|   200|   720|       NA|       NA|     NA|     NA| -1.1286|   0.45|    0.59|    -1.41|      11|      4| -1.8994|  -2.7469| -0.5492| -1.7679| -1.9751|   1.0573|   0.7628|  0.5733|  2.0165| -1.5824|   1.1469|     0.4599|   0.2984|  0.3379|     -0.825|     0.5371|   0.8232| -1.9892| -2.1428|   1.0844|  2.0054|   0.5693|  1.8905|  0.7522| -2.1239|     0.4558|       NA|   -0.1574| -0.6249| -2.2640|  1.6052|   1.1388| -0.2971| -0.4401| -2.7378|  -2.8778|  0.5881| -0.6438|      -0.7823| -0.7876| -0.5155|  0.0799| -1.0898| -0.9849| -1.1563| -0.7345|   0.5334|     0.1104|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 442.186| 421.606| 412.709| 403.498| 377.077| 371.637| 421.356| 390.840| 399.156|  381.943| 335.574| 416.818| 344.729| 350.298| 354.592| 387.800| 337.228| 407.309| 386.681|  390.544| 381.356| 421.542| 445.520| 439.429| 385.339| 475.421| 444.895| 394.340| 374.706|  447.245|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 337.812| 353.395| 349.774| 346.927| 339.210| 349.795| 301.194| 333.122| 357.030|  359.683| 364.114| 438.537| 350.288| 383.715| 322.637| 364.979| 354.316| 383.064| 409.538|  413.415| 389.701| 394.063| 343.933| 348.001| 321.249| 360.455| 352.890| 334.809| 377.431|  388.909| 362.999| 362.142| 394.866| 339.167| 340.977| 376.489| 317.589| 369.271| 337.621|  347.858| 377.158| 379.792| 349.161| 373.939| 367.320| 387.109| 390.690| 427.581| 354.588|  371.068| 0.80261|02MAY19:09:49:49 |   NA|

</div>



- PISA verisinde anne eğitim düzeyi **ve** baba eğitim düzeyi lisansüstü olan öğrencilerin seçilmesi


```r
PISA_STU_2018 %>% filter(MISCED==6 & FISCED==6)  %>% head(4)
```

<div class="kable-table">

| CNTRYID|CNT | CNTSCHID| CNTSTUID|CYC  |NatCen |STRATUM |SUBNATIO | OECD| ADMINMODE| LANGTEST_QQQ| LANGTEST_COG| LANGTEST_PAQ| BOOKID| ST001D01T| ST003D02T| ST003D03T| ST004D01T| ST005Q01TA| ST006Q01TA| ST006Q02TA| ST006Q03TA| ST006Q04TA| ST007Q01TA| ST008Q01TA| ST008Q02TA| ST008Q03TA| ST008Q04TA| ST011Q01TA| ST011Q02TA| ST011Q03TA| ST011Q04TA| ST011Q05TA| ST011Q06TA| ST011Q07TA| ST011Q08TA| ST011Q09TA| ST011Q10TA| ST011Q11TA| ST011Q12TA| ST011Q16NA|ST011D17TA |ST011D18TA |ST011D19TA | ST012Q01TA| ST012Q02TA| ST012Q03TA| ST012Q05NA| ST012Q06NA| ST012Q07NA| ST012Q08NA| ST012Q09NA| ST013Q01TA| ST019AQ01T| ST019BQ01T| ST019CQ01T| ST021Q01TA| ST125Q01NA| ST126Q01TA| ST127Q01TA| ST127Q02TA| ST127Q03TA| ST022Q01TA| ST023Q01TA| ST023Q02TA| ST023Q03TA| ST023Q04TA| ST023Q05TA| ST097Q01TA| ST097Q02TA| ST097Q03TA| ST097Q04TA| ST097Q05TA| ST100Q01TA| ST100Q02TA| ST100Q03TA| ST100Q04TA| ST102Q01TA| ST102Q02TA| ST102Q03TA| ST102Q04TA| ST211Q01HA| ST211Q02HA| ST211Q03HA| ST212Q01HA| ST212Q02HA| ST212Q03HA| ST104Q02NA| ST104Q03NA| ST104Q04NA| ST213Q01HA| ST213Q02HA| ST213Q03HA| ST213Q04HA| ST150Q01IA| ST150Q02IA| ST150Q03IA| ST150Q04HA| ST152Q05IA| ST152Q06IA| ST152Q07IA| ST152Q08IA| ST154Q01HA| ST153Q01HA| ST153Q02HA| ST153Q03HA| ST153Q04HA| ST153Q05HA| ST153Q06HA| ST153Q08HA| ST153Q09HA| ST153Q10HA| ST158Q01HA| ST158Q02HA| ST158Q03HA| ST158Q04HA| ST158Q05HA| ST158Q06HA| ST158Q07HA| ST160Q01IA| ST160Q02IA| ST160Q03IA| ST160Q04IA| ST160Q05IA| ST167Q01IA| ST167Q02IA| ST167Q03IA| ST167Q04IA| ST167Q05IA| ST168Q01HA| ST175Q01IA| ST176Q01IA| ST176Q02IA| ST176Q03IA| ST176Q05IA| ST176Q06IA| ST176Q07IA| ST161Q01HA| ST161Q02HA| ST161Q03HA| ST161Q06HA| ST161Q07HA| ST161Q08HA| ST163Q02HA| ST163Q03HA| ST163Q04HA| ST164Q01IA| ST164Q02IA| ST164Q03IA| ST164Q04IA| ST164Q05IA| ST164Q06IA| ST165Q01IA| ST165Q02IA| ST165Q03IA| ST165Q04IA| ST165Q05IA| ST166Q01HA| ST166Q02HA| ST166Q03HA| ST166Q04HA| ST166Q05HA| ST016Q01NA| ST036Q05TA| ST036Q06TA| ST036Q08TA| ST225Q01HA| ST225Q02HA| ST225Q03HA| ST225Q04HA| ST225Q05HA| ST225Q06HA| ST181Q02HA| ST181Q03HA| ST181Q04HA| ST182Q03HA| ST182Q04HA| ST182Q05HA| ST182Q06HA| ST183Q01HA| ST183Q02HA| ST183Q03HA| ST184Q01HA| ST185Q01HA| ST185Q02HA| ST185Q03HA| ST186Q05HA| ST186Q06HA| ST186Q07HA| ST186Q10HA| ST186Q09HA| ST186Q02HA| ST186Q01HA| ST186Q08HA| ST186Q03HA| ST208Q01HA| ST208Q02HA| ST208Q04HA| ST188Q01HA| ST188Q02HA| ST188Q03HA| ST188Q06HA| ST188Q07HA| ST034Q01TA| ST034Q02TA| ST034Q03TA| ST034Q04TA| ST034Q05TA| ST034Q06TA| ST196Q02HA| ST196Q03HA| ST196Q04HA| ST196Q05HA| ST196Q06HA| ST196Q07HA| ST197Q01HA| ST197Q02HA| ST197Q04HA| ST197Q07HA| ST197Q08HA| ST197Q09HA| ST197Q12HA| ST215Q01HA| ST215Q02HA| ST215Q03HA| ST215Q04HA| ST215Q05HA| ST216Q01HA| ST216Q02HA| ST216Q03HA| ST216Q04HA| ST216Q05HA| ST216Q06HA| ST218Q01HA| ST218Q02HA| ST218Q03HA| ST218Q04HA| ST218Q05HA| ST218Q06HA| ST218Q07HA| ST222Q01HA| ST222Q03HA| ST222Q04HA| ST222Q05HA| ST222Q06HA| ST222Q08HA| ST222Q09HA| ST222Q10HA| ST214Q01HA| ST214Q02HA| ST214Q03HA| ST214Q06HA| ST220Q01HA| ST220Q02HA| ST220Q03HA| ST220Q04HA| ST217Q01HA| ST217Q02HA| ST217Q03HA| ST217Q04HA| ST217Q05HA| ST219Q01HA| ST219Q02HA| ST219Q03HA| ST219Q04HA| ST219Q05HA| ST219Q06HA| ST204Q02HA| ST204Q03HA| ST204Q04HA| ST204Q05HA| ST177Q01HA| ST177Q02HA| ST177Q03HA| ST189Q01HA| ST221Q01HA| ST221Q02HA| ST221Q03HA| ST221Q04HA| ST221Q05HA| ST221Q06HA| ST221Q07HA| ST221Q08HA| ST221Q09HA| ST221Q11HA| ST223Q02HA| ST223Q04HA| ST223Q05HA| ST223Q08HA| ST123Q02NA| ST123Q03NA| ST123Q04NA| ST205Q01HA| ST205Q02HA| ST205Q03HA| ST205Q04HA| ST059Q01TA| ST059Q02TA| ST059Q03TA| ST059Q04HA| ST060Q01NA| ST061Q01NA| ST062Q01TA| ST062Q02TA| ST062Q03TA| ST038Q03NA| ST038Q04NA| ST038Q05NA| ST038Q06NA| ST038Q07NA| ST038Q08NA| ST207Q01HA| ST207Q02HA| ST207Q03HA| ST207Q04HA| ST207Q05HA| ST206Q01HA| ST206Q02HA| ST206Q03HA| ST206Q04HA| IC001Q01TA| IC001Q02TA| IC001Q03TA| IC001Q04TA| IC001Q05TA| IC001Q06TA| IC001Q07TA| IC001Q08TA| IC001Q09TA| IC001Q10TA| IC001Q11TA| IC009Q01TA| IC009Q02TA| IC009Q03TA| IC009Q05NA| IC009Q06NA| IC009Q07NA| IC009Q08TA| IC009Q09TA| IC009Q10NA| IC009Q11NA| IC002Q01HA| IC004Q01HA| IC005Q01TA| IC006Q01TA| IC007Q01TA| IC150Q01HA| IC150Q02HA| IC150Q03HA| IC150Q04HA| IC150Q05HA| IC150Q06HA| IC150Q07HA| IC150Q08HA| IC150Q09HA| IC151Q01HA| IC151Q02HA| IC151Q03HA| IC151Q04HA| IC151Q05HA| IC151Q06HA| IC151Q07HA| IC151Q08HA| IC151Q09HA| IC152Q01HA| IC152Q02HA| IC152Q03HA| IC152Q04HA| IC152Q05HA| IC152Q06HA| IC152Q07HA| IC152Q08HA| IC152Q09HA| IC008Q01TA| IC008Q02TA| IC008Q03TA| IC008Q04TA| IC008Q05TA| IC008Q07NA| IC008Q08TA| IC008Q09TA| IC008Q10TA| IC008Q11TA| IC008Q12TA| IC008Q13NA| IC010Q01TA| IC010Q02NA| IC010Q03TA| IC010Q04TA| IC010Q05NA| IC010Q06NA| IC010Q07TA| IC010Q08TA| IC010Q09NA| IC010Q10NA| IC010Q11HA| IC010Q12HA| IC011Q01TA| IC011Q02TA| IC011Q03TA| IC011Q04TA| IC011Q05TA| IC011Q06TA| IC011Q07TA| IC011Q08TA| IC011Q09TA| IC011Q10HA| IC013Q01NA| IC013Q04NA| IC013Q05NA| IC013Q11NA| IC013Q12NA| IC013Q13NA| IC014Q03NA| IC014Q04NA| IC014Q06NA| IC014Q08NA| IC014Q09NA| IC015Q02NA| IC015Q03NA| IC015Q05NA| IC015Q07NA| IC015Q09NA| IC016Q01NA| IC016Q02NA| IC016Q04NA| IC016Q05NA| IC016Q07NA| IC169Q01HA| EC031Q01TA| EC032Q01TA| EC033Q01NA| EC150Q01WA| EC150Q02WA| EC150Q03WA| EC150Q04WA| EC150Q05WA| EC150Q06WA| EC150Q07WA| EC150Q08WA| EC150Q09WA| EC150Q10WA| EC151Q01WA| EC151Q01WB| EC151Q01WC| EC151Q02WA| EC151Q02WB| EC151Q02WC| EC151Q03WA| EC151Q03WB| EC151Q03WC| EC151Q04WA| EC151Q04WB| EC151Q04WC| EC151Q05WA| EC151Q05WB| EC151Q05WC| EC152Q01HA| EC153Q01HA| EC153Q02HA| EC153Q03HA| EC153Q04HA| EC153Q05HA| EC153Q06HA| EC153Q07HA| EC153Q08HA| EC153Q09HA| EC153Q10HA| EC153Q11HA| EC160Q01HA| EC158Q01HA| EC158Q02HA| EC159Q01HA| EC159Q02HA| EC163Q01HA| EC163Q02HA| EC163Q03HA| EC163Q04HA| EC163Q05HA| EC163Q06HA| EC163Q07HA| EC162Q01HA| EC162Q02HA| EC162Q03HA| EC162Q04HA| EC162Q05HA| EC162Q06HA| EC162Q07HA| EC162Q08HA| EC154Q01IA| EC154Q02IA| EC154Q03IA| EC154Q04HA| EC154Q05IA| EC154Q06IA| EC154Q07IA| EC154Q08HA| EC154Q09IA| EC012Q01NA| EC012Q02NA| EC012Q04NA| EC012Q06NA| EC012Q07NA| EC012Q08NA| EC012Q13HA| EC012Q12NA| EC155Q01DA| EC155Q02DA| EC155Q03DA| EC155Q04HA| EC155Q05HA| WB150Q01HA| WB151Q01HA| WB152Q01HA| WB153Q01HA| WB153Q02HA| WB153Q03HA| WB153Q04HA| WB153Q05HA| WB154Q01HA| WB154Q02HA| WB154Q03HA| WB154Q04HA| WB154Q05HA| WB154Q06HA| WB154Q07HA| WB154Q08HA| WB154Q09HA| WB155Q01HA| WB155Q02HA| WB155Q03HA| WB155Q04HA| WB155Q05HA| WB155Q06HA| WB155Q07HA| WB155Q08HA| WB155Q09HA| WB155Q10HA| WB156Q01HA| WB158Q01HA| WB160Q01HA| WB161Q01HA| WB162Q01HA| WB162Q02HA| WB162Q03HA| WB162Q04HA| WB162Q05HA| WB162Q06HA| WB162Q07HA| WB162Q08HA| WB162Q09HA| WB163Q01HA| WB163Q02HA| WB163Q03HA| WB163Q04HA| WB163Q05HA| WB163Q06HA| WB163Q07HA| WB163Q08HA| WB164Q01HA| WB165Q01HA| WB166Q01HA| WB166Q02HA| WB166Q03HA| WB166Q04HA| WB167Q01HA| WB168Q01HA| WB168Q02HA| WB168Q03HA| WB168Q04HA| WB171Q01HA| WB171Q02HA| WB171Q03HA| WB171Q04HA| WB172Q01HA| WB173Q01HA| WB173Q02HA| WB173Q03HA| WB173Q04HA| WB176Q01HA| WB177Q01HA| WB177Q02HA| WB177Q03HA| WB177Q04HA| WB032Q01NA| WB032Q02NA| WB031Q01NA| WB178Q01HA| WB178Q02HA| WB178Q03HA| WB178Q04HA| WB178Q05HA| WB178Q06HA| WB178Q07HA| FL150Q01TA| FL150Q02TA| FL150Q03TA| FL151Q01HA| FL151Q02HA| FL164Q01HA| FL164Q02HA| FL164Q03HA| FL164Q04HA| FL164Q05HA| FL164Q06HA| FL164Q07HA| FL164Q08HA| FL164Q09HA| FL164Q10HA| FL164Q11HA| FL164Q12HA| FL164Q13HA| FL164Q14HA| FL164Q15HA| FL164Q16HA| FL164Q17HA| FL164Q18HA| FL165Q01HA| FL165Q02HA| FL165Q03HA| FL165Q04HA| FL166Q01HA| FL166Q02HA| FL166Q03HA| FL166Q05HA| FL166Q06HA| FL166Q07HA| FL153Q01HA| FL153Q02HA| FL153Q03HA| FL153Q04HA| FL153Q05HA| FL153Q06HA| FL167Q01HA| FL167Q02HA| FL167Q03HA| FL167Q04HA| FL167Q05HA| FL156Q01TA| FL156Q02TA| FL156Q03TA| FL156Q04TA| FL156Q05TA| FL156Q06TA| FL156Q07HA| FL159Q01HA| FL159Q02HA| FL159Q03HA| FL159Q04HA| FL160Q01HA| FL160Q02HA| FL160Q03HA| FL160Q04HA| FL161Q01HA| FL161Q02HA| FL161Q03HA| FL162Q01HA| FL162Q02HA| FL162Q03HA| FL162Q04HA| FL162Q05HA| FL162Q06HA| FL163Q01HA| FL163Q02HA| FL163Q03HA| FL163Q04HA| FL163Q05HA| FL168Q01HA| FL168Q02HA| FL168Q03HA| FL168Q04HA| FL168Q05HA| FL168Q06HA| FL168Q07HA| FL168Q08HA| FL169Q01HA| FL169Q02HA| FL169Q03HA| FL169Q04HA| PA001Q01TA| PA001Q02TA| PA001Q03TA| PA003Q01TA| PA003Q02TA| PA003Q03TA| PA003Q04HA| PA003Q05IA| PA003Q06IA| PA003Q07IA| PA154Q01IA| PA154Q02IA| PA154Q03IA| PA154Q04IA| PA154Q05IA| PA154Q06IA| PA154Q07IA| PA154Q08IA| PA154Q09IA| PA154Q10HA| PA155Q01IA| PA156Q01HA| PA156Q02HA| PA156Q03HA| PA156Q04HA| PA004Q02NA| PA004Q03NA| PA004Q04NA| PA008Q01TA| PA008Q02TA| PA008Q03TA| PA008Q04TA| PA008Q05TA| PA008Q06NA| PA008Q07NA| PA008Q08NA| PA008Q09NA| PA008Q10NA| PA009Q01NA| PA009Q02NA| PA009Q03NA| PA009Q04NA| PA009Q05NA| PA009Q06NA| PA009Q07NA| PA009Q08NA| PA009Q09NA| PA009Q10NA| PA009Q11NA| PA007Q01TA| PA007Q02TA| PA007Q03TA| PA007Q04TA| PA007Q05TA| PA007Q06TA| PA007Q07TA| PA007Q09NA| PA007Q11NA| PA007Q12NA| PA007Q13NA| PA007Q14NA| PA007Q15NA| PA005Q01TA| PA006Q01TA| PA006Q02TA| PA006Q03TA| PA006Q04TA| PA006Q05TA| PA006Q06TA| PA006Q07TA| PA006Q08TA| PA006Q09TA| PA006Q10TA| PA006Q11TA| PA006Q12HA| PA006Q13HA| PA006Q14HA| PA158Q01HA| PA158Q02IA| PA158Q03HA| PA158Q04IA| PA158Q05HA| PA159Q01HA| PA160Q01HA| PA160Q02HA| PA160Q03HA| PA160Q04HA| PA160Q05HA| PA161Q01HA| PA161Q02HA| PA161Q03HA| PA161Q05HA| PA161Q06HA| PA161Q07HA| PA162Q01HA| PA163Q01HA| PA166Q01HA| PA167Q02HA| PA167Q03HA| PA167Q04HA| PA167Q05HA| PA168Q01HA| PA168Q02HA| PA168Q03HA| PA168Q06HA| PA169Q01HA| PA169Q02HA| PA169Q03HA| PA169Q04HA| PA169Q05HA| PA169Q06HA| PA170Q01HA| PA170Q02HA| PA170Q04HA| PA170Q07HA| PA170Q08HA| PA170Q09HA| PA170Q12HA| PA171Q01HA| PA171Q03HA| PA171Q04HA| PA171Q05HA| PA171Q06HA| PA171Q08HA| PA171Q09HA| PA171Q10HA| PA172Q01WA| PA172Q02WA| PA172Q03WA| PA172Q04WA| PA172Q05WA| PA172Q06WA| PA018Q01NA| PA018Q02NA| PA018Q03NA| PA177Q01HA| PA177Q02HA| PA177Q03HA| PA177Q04HA| PA177Q05HA| PA177Q06HA| PA177Q07HA| PA177Q08HA| PA180Q01HA| PA182Q01HA| PA175Q01HA| PA175Q02HA| PA041Q01TA| PA042Q01TA| EFFORT1| EFFORT2|OCOD1 |OCOD2 |OCOD3 | GRADE|   AGE|PROGN    |COBN_S |COBN_M |COBN_F | LANGN| ISCEDL| ISCEDD| ISCEDO| MISCED| FISCED| HISCED| PARED| MISCED_D| FISCED_D| HISCED_D| PAREDINT| BMMJ1| BFMJ2| HISEI| LANGMOTHER| LANGFATHER| LANGSIBLINGS| LANGFRIEND| LANGSCHMATES| IMMIG| DURECEC| REPEAT|  BSMJ| MMINS| LMINS| SMINS| TMINS| FCFMLRTY| SCCHANGE| CHANGE| STUBMI|    ESCS| UNDREM| METASUM| METASPAM| ICTHOME| ICTSCH| HOMEPOS| CULTPOSS|  HEDRES|  WEALTH|  ICTRES| DISCLIMA| TEACHSUP|  DIRINS| PERFEED| EMOSUPS| STIMREAD| ADAPTIVITY| TEACHINT| JOYREAD| SCREADCOMP| SCREADDIFF| PISADIFF| PERCOMP| PERCOOP| ATTLNACT| COMPETE| WORKMAST| GFOFAIL|   EUDMO|    SWBP| RESILIENCE| MASTGOAL| GCSELFEFF| GCAWARE|  ATTIMM| INTCULT| PERSPECT| COGFLEX| RESPECT|  AWACOM| GLOBMIND| DISCRIM|  BELONG| BEINGBULLIED|  ENTUSE| HOMESCH|  USESCH|  INTICT| COMPICT|  AUTICT| SOIAICT| ICTCLASS| ICTOUTSIDE| INFOCAR| INFOJOB1| INFOJOB2| FLCONFIN| FLCONICT| FLSCHOOL| FLFAMILY| CURSUPP| EMOSUPP| PQSCHOOL| PASCHPOL| PRESUPP| JOYREADP| ATTIMMP| INTCULTP| GCAWAREP| BODYIMA| SOCONPA| W_FSTUWT| W_FSTURWT1| W_FSTURWT2| W_FSTURWT3| W_FSTURWT4| W_FSTURWT5| W_FSTURWT6| W_FSTURWT7| W_FSTURWT8| W_FSTURWT9| W_FSTURWT10| W_FSTURWT11| W_FSTURWT12| W_FSTURWT13| W_FSTURWT14| W_FSTURWT15| W_FSTURWT16| W_FSTURWT17| W_FSTURWT18| W_FSTURWT19| W_FSTURWT20| W_FSTURWT21| W_FSTURWT22| W_FSTURWT23| W_FSTURWT24| W_FSTURWT25| W_FSTURWT26| W_FSTURWT27| W_FSTURWT28| W_FSTURWT29| W_FSTURWT30| W_FSTURWT31| W_FSTURWT32| W_FSTURWT33| W_FSTURWT34| W_FSTURWT35| W_FSTURWT36| W_FSTURWT37| W_FSTURWT38| W_FSTURWT39| W_FSTURWT40| W_FSTURWT41| W_FSTURWT42| W_FSTURWT43| W_FSTURWT44| W_FSTURWT45| W_FSTURWT46| W_FSTURWT47| W_FSTURWT48| W_FSTURWT49| W_FSTURWT50| W_FSTURWT51| W_FSTURWT52| W_FSTURWT53| W_FSTURWT54| W_FSTURWT55| W_FSTURWT56| W_FSTURWT57| W_FSTURWT58| W_FSTURWT59| W_FSTURWT60| W_FSTURWT61| W_FSTURWT62| W_FSTURWT63| W_FSTURWT64| W_FSTURWT65| W_FSTURWT66| W_FSTURWT67| W_FSTURWT68| W_FSTURWT69| W_FSTURWT70| W_FSTURWT71| W_FSTURWT72| W_FSTURWT73| W_FSTURWT74| W_FSTURWT75| W_FSTURWT76| W_FSTURWT77| W_FSTURWT78| W_FSTURWT79| W_FSTURWT80| UNIT| WVARSTRR| PV1MATH| PV2MATH| PV3MATH| PV4MATH| PV5MATH| PV6MATH| PV7MATH| PV8MATH| PV9MATH| PV10MATH| PV1READ| PV2READ| PV3READ| PV4READ| PV5READ| PV6READ| PV7READ| PV8READ| PV9READ| PV10READ| PV1SCIE| PV2SCIE| PV3SCIE| PV4SCIE| PV5SCIE| PV6SCIE| PV7SCIE| PV8SCIE| PV9SCIE| PV10SCIE| PV1GLCM| PV2GLCM| PV3GLCM| PV4GLCM| PV5GLCM| PV6GLCM| PV7GLCM| PV8GLCM| PV9GLCM| PV10GLCM| PV1RCLI| PV2RCLI| PV3RCLI| PV4RCLI| PV5RCLI| PV6RCLI| PV7RCLI| PV8RCLI| PV9RCLI| PV10RCLI| PV1RCUN| PV2RCUN| PV3RCUN| PV4RCUN| PV5RCUN| PV6RCUN| PV7RCUN| PV8RCUN| PV9RCUN| PV10RCUN| PV1RCER| PV2RCER| PV3RCER| PV4RCER| PV5RCER| PV6RCER| PV7RCER| PV8RCER| PV9RCER| PV10RCER| PV1RTSN| PV2RTSN| PV3RTSN| PV4RTSN| PV5RTSN| PV6RTSN| PV7RTSN| PV8RTSN| PV9RTSN| PV10RTSN| PV1RTML| PV2RTML| PV3RTML| PV4RTML| PV5RTML| PV6RTML| PV7RTML| PV8RTML| PV9RTML| PV10RTML|   SENWT|VER_DAT          | test|
|-------:|:---|--------:|--------:|:----|:------|:-------|:--------|----:|---------:|------------:|------------:|------------:|------:|---------:|---------:|---------:|---------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|:----------|:----------|:----------|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|-------:|-------:|:-----|:-----|:-----|-----:|-----:|:--------|:------|:------|:------|-----:|------:|------:|------:|------:|------:|------:|-----:|--------:|--------:|--------:|--------:|-----:|-----:|-----:|----------:|----------:|------------:|----------:|------------:|-----:|-------:|------:|-----:|-----:|-----:|-----:|-----:|--------:|--------:|------:|------:|-------:|------:|-------:|--------:|-------:|------:|-------:|--------:|-------:|-------:|-------:|--------:|--------:|-------:|-------:|-------:|--------:|----------:|--------:|-------:|----------:|----------:|--------:|-------:|-------:|--------:|-------:|--------:|-------:|-------:|-------:|----------:|--------:|---------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|--------:|-------:|-------:|------------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|----------:|-------:|--------:|--------:|--------:|--------:|--------:|--------:|-------:|-------:|--------:|--------:|-------:|--------:|-------:|--------:|--------:|-------:|-------:|--------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|----:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|:----------------|----:|
|     792|TUR | 79200001| 79201275|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|     21|         9|         9|      2002|         2|          1|         NA|          1|         NA|         NA|          1|         NA|          1|         NA|         NA|          1|          1|          1|          1|          2|          1|          2|          2|          2|          1|          2|          1|          2|0792001    |0792002    |0792002    |          3|          1|          1|          2|          2|          1|          1|          1|          1|          1|          1|          1|         NA|          6|          5|          1|          1|          1|          1|          4|          4|          4|          4|          4|          2|          2|          3|          1|          1|          3|          2|          1|          4|          2|          3|          4|          3|          3|          2|          2|          2|          2|          2|          3|          2|          3|          2|          2|          2|          2|          4|          4|          4|          4|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          3|          1|          1|          3|          3|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          2|          2|          2|          1|          1|          1|          6|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|          2|          2|          2|          0|          0|          0|         NA|          0|          1|          4|          3|          4|          1|          1|          1|          1|          1|          1|          1|          3|          1|          1|          1|          4|          2|          1|          1|          4|          1|          2|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|          2|          3|          2|          2|          3|          1|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          3|          3|          1|          2|          1|          3|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|          1|          3|          2|          2|          1|          2|          1|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          2|          2|          2|          2|          1|          1|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|         NA|          3|          2|          2|          2|          2|          5|          6|          6|          4|         40|         40|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          2|          2|          3|          2|          2|          2|          2|          1|          1|          1|          1|          1|          3|          1|          2|          1|          2|          3|          1|          1|          1|          1|          2|          2|          2|          3|          2|          1|          1|          2|          1|          5|          5|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          3|          4|          4|          1|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|      10|      10|2330  |2330  |2211  |    -1| 15.58|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      6|      6|      6|    16|        6|        6|        6|       16| 82.41| 82.41| 82.41|         NA|         NA|           NA|         NA|           NA|     1|       1|      0| 88.70|   240|   200|   240|  1600|       NA|       NA|     NA|     NA|  0.0324|  -0.60|   -1.72|    -1.41|       9|      9| -2.1008|  -2.7469| -0.6853| -2.1121| -1.7005|  -1.1699|  -0.4060| -1.0499|  0.2682|      NA|  -0.6200|    -0.5786|  -1.0615| -1.1538|    -0.8250|     1.2421|   0.2705| -0.6142| -0.9391|  -0.6583|  1.1811|  -2.7365| -1.8939| -2.1464| -1.2568|    -1.4832|  -1.3162|   -2.7142| -0.0549| -1.2083| -0.2157|  -0.3405|  1.3823| -1.2781| -1.3933|   0.2910| -1.1549| -0.4217|       1.1625| -2.7049| -0.5991| -1.0707| -2.9336| -2.6033| -2.5144|  0.2639|   1.0418|    -1.3048|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|   71.02860|   71.02860|    71.0286|   71.02860|  213.08579|    213.0858|     71.0286|   213.08579|   213.08579|    71.02860|    71.02860|    213.0858|   213.08579|    213.0858|   213.08579|     71.0286|   213.08579|    71.02860|   213.08579|    71.02860|    213.0858|    213.0858|   213.08579|    213.0858|     71.0286|    71.02860|   213.08579|     71.0286|     71.0286|    213.0858|    213.0858|    71.02860|     71.0286|    71.02860|     71.0286|   213.08579|    71.02860|   213.08579|    71.02860|   213.08579|     71.0286|     71.0286|    71.02860|     71.0286|    213.0858|   213.08579|    71.02860|    213.0858|    213.0858|     71.0286|     71.0286|   213.08579|    213.0858|   213.08579|    213.0858|    71.02860|    213.0858|     71.0286|    213.0858|     71.0286|   213.08579|   213.08579|    213.0858|   213.08579|    71.02860|     71.0286|    213.0858|    71.02860|    71.02860|   213.08579|   213.08579|     71.0286|    71.02860|     71.0286|    71.02860|    213.0858|    2|        3| 417.314| 486.246| 419.767| 413.368| 508.158| 475.248| 527.383| 482.872| 477.418|  476.539| 393.006| 428.757| 364.850| 382.522| 378.563| 416.048| 395.846| 383.782| 374.509|  381.877| 402.112| 431.478| 384.063| 472.941| 420.800| 472.894| 460.407| 465.356| 439.954|  442.546|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 377.648| 346.106| 347.468| 351.544| 464.958| 406.800| 305.063| 415.645| 451.572|  332.146| 418.336| 387.692| 376.644| 348.832| 469.856| 438.034| 377.209| 433.141| 463.976|  390.554| 370.646| 356.020| 346.501| 346.212| 425.656| 396.229| 416.122| 421.807| 457.353|  390.627| 419.099| 390.744| 410.400| 377.828| 443.815| 406.021| 393.957| 420.428| 398.023|  462.478| 400.889| 416.115| 426.449| 396.449| 425.235| 391.150| 373.368| 416.023| 417.897|  416.855| 0.80261|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200001| 79202343|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|     22|        11|         3|      2002|         2|          1|          1|          1|          1|         NA|          1|         NA|          1|         NA|         NA|          1|          1|          1|          1|          2|          1|          2|          2|          2|          2|          2|          1|          1|0792001    |0792001    |0792001    |          3|          4|          3|          4|          3|          3|          1|          3|          1|          1|          1|          1|         NA|          6|          6|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          2|          2|          4|          3|          3|          4|          3|          2|          3|          2|          3|          3|          4|          1|          1|          2|          3|          3|          4|          1|          1|          1|          1|          2|          2|          2|          2|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          1|          2|         NA|          5|         NA|          1|          5|          5|          1|          4|          4|          4|          2|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          0|          4|          2|          3|          0|          0|          1|         NA|          0|          0|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          3|          4|          3|          4|          3|          2|          4|          1|          3|          1|          4|          2|          4|          1|          2|          2|          4|          3|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|         NA|          1|         NA|         NA|         NA|         NA|         NA|         NA|         NA|          1|          2|          3|          4|          5|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          5|          1|          1|          1|          1|          5|          5|          5|          5|          5|          3|         NA|         NA|         NA|         NA|         NA|          3|          3|          2|          3|          2|          1|          1|          3|          2|          2|          1|          2|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          0|          2|          0|         20|         30|          4|          4|          2|          1|          1|          1|          1|          1|          1|          4|          1|          1|          1|          1|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          5|          7|          7|          2|          1|          2|          1|          3|          4|          4|          4|          1|          4|          1|          2|          2|          5|          4|          4|          4|          5|          5|          5|          5|          5|          5|         NA|         NA|         NA|         NA|          5|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|          3|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          4|          4|          4|          4|          4|          4|          3|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          3|          3|          4|         NA|          3|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|       7|       9|9701  |6111  |2330  |     1| 16.08|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      6|      6|      6|    16|        6|        6|        6|       16| 17.00| 11.56| 17.00|         NA|         NA|           NA|         NA|           NA|     1|       2|      0| 82.41|     0|    60|    60|   600|       NA|       NA|     NA|     NA| -0.4280|  -1.64|   -1.72|    -1.41|      11|     10| -0.2441|  -1.2687| -1.0118|  0.6090| -0.1120|  -1.4882|  -1.5550| -0.5066|  1.1225| -2.4468|  -2.3003|    -1.6010|  -2.2177| -0.1119|    -0.3140|     0.2426|   0.2705| -1.9892| -1.6237|  -1.6038|  2.0054|  -2.7365| -1.8939|  1.1963|  0.6502|     1.5900|  -1.4972|   -2.6739|      NA| -0.6155| -0.0180|  -0.2098| -0.8312| -3.1739| -2.7948|       NA| -1.1549| -1.2605|      -0.7823|      NA|  2.3702|  3.3041|  2.6186|  1.4987|  2.0258|  1.4359|   0.2764|     0.5477|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|   71.02860|   71.02860|    71.0286|   71.02860|  213.08579|    213.0858|     71.0286|   213.08579|   213.08579|    71.02860|    71.02860|    213.0858|   213.08579|    213.0858|   213.08579|     71.0286|   213.08579|    71.02860|   213.08579|    71.02860|    213.0858|    213.0858|   213.08579|    213.0858|     71.0286|    71.02860|   213.08579|     71.0286|     71.0286|    213.0858|    213.0858|    71.02860|     71.0286|    71.02860|     71.0286|   213.08579|    71.02860|   213.08579|    71.02860|   213.08579|     71.0286|     71.0286|    71.02860|     71.0286|    213.0858|   213.08579|    71.02860|    213.0858|    213.0858|     71.0286|     71.0286|   213.08579|    213.0858|   213.08579|    213.0858|    71.02860|    213.0858|     71.0286|    213.0858|     71.0286|   213.08579|   213.08579|    213.0858|   213.08579|    71.02860|     71.0286|    213.0858|    71.02860|    71.02860|   213.08579|   213.08579|     71.0286|    71.02860|     71.0286|    71.02860|    213.0858|    2|        3| 319.885| 325.236| 298.124| 347.893| 344.137| 332.804| 309.840| 414.770| 310.236|  393.137| 319.453| 333.203| 345.495| 339.966| 346.631| 336.530| 325.728| 322.760| 315.270|  302.398| 366.331| 434.453| 385.126| 406.671| 436.551| 410.509| 382.595| 415.349| 392.922|  369.015|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 283.543| 366.617| 279.752| 300.736| 324.928| 291.124| 291.853| 289.940| 254.055|  227.516| 358.106| 363.373| 337.079| 305.745| 345.937| 316.643| 330.522| 345.601| 305.511|  333.845| 357.716| 390.257| 312.117| 343.106| 459.546| 320.759| 363.881| 368.221| 351.077|  367.712| 349.881| 326.972| 361.684| 320.697| 356.205| 366.312| 364.327| 303.503| 310.790|  355.886| 392.458| 301.654| 400.555| 347.418| 370.830| 351.170| 382.755| 390.538| 411.888|  355.742| 0.80261|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200002| 79201796|07MS |079200 |TUR0231 |7920000  |    1|         2|          344|          344|           NA|     14|        10|        12|      2002|         2|          2|          1|          2|          2|         NA|          1|          1|          2|          2|         NA|          1|          1|          1|          1|          2|          1|          2|          2|          2|          1|          1|          1|          1|0792001    |0792001    |0792001    |          4|          2|          1|          4|          2|          2|          1|          3|          3|          1|          1|          1|         NA|          7|          5|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          3|          3|          4|          3|          1|          1|          1|          1|          1|          2|          1|          1|          2|          3|          4|          4|          2|          4|          2|          3|          3|          3|          4|          3|          3|          2|          1|          1|          3|          2|          4|          4|          4|          3|          2|          2|          1|          1|          1|          1|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          3|          3|          2|          2|          1|          1|          5|          4|          3|          3|          3|          5|          5|          4|          5|          5|          5|          3|          3|          3|          1|          2|          1|          2|          2|          2|          6|          3|          3|          4|          4|          4|          3|          3|          4|          4|          3|          6|          6|          1|          1|          4|          4|          1|          1|          1|          0|          0|          0|         NA|          0|          1|          4|          4|          4|          3|          4|          4|          3|          3|          3|          3|          3|          4|          4|          4|          3|          2|          4|          2|          4|          2|          3|          2|          3|          5|          4|          5|          4|          4|          4|          4|          4|          4|          1|          1|          4|          1|          4|          3|          3|          3|          3|          3|          3|          3|          2|          3|          4|          2|          3|          3|          2|          2|          1|          3|          4|          1|          1|          1|          3|          2|          1|          4|         NA|          4|          4|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          3|          4|          4|          4|          4|          4|          4|          4|          4|          1|          1|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          7|         12|          6|          4|         45|         40|          2|          3|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|         NA|          1|         NA|         NA|         NA|          1|          1|          1|          2|          3|          5|          6|          7|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|         NA|          5|          5|          5|          5|          5|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          2|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|       9|      10|9701  |7313  |0210  |     0| 15.33|07920003 |079200 |079200 |079200 |   344|      3|      2|      3|      6|      6|      6|    16|        6|        6|        6|       16| 17.00| 28.12| 28.12|         NA|         NA|           NA|         NA|           NA|     1|      NA|      0| 51.63|   480|   280|   240|  1800|       NA|       NA|     NA|     NA| -0.3629|  -0.94|   -0.57|    -0.50|      11|      6| -0.5908|  -1.2687| -0.1357| -0.5757| -0.8794|   0.5156|   1.3140|  0.8667|  0.5121|  1.0346|   1.2234|     0.7339|   0.5665|  0.8418|     0.1222|    -1.1260|   0.2705|  2.0378|  1.6762|   1.0844|  2.0054|   0.9982|  0.4637|  1.7411| -0.5928|     2.3693|   1.1969|    0.1904| -0.3908|  1.4992|  1.6052|   0.2828|  1.3651|  0.9289|  1.9924|   1.0637|  3.1825|  2.7249|      -0.7823|  4.2444|  3.2502| -1.7161|  2.6186|  1.9637|  2.0258|  2.3635|   0.3701|     0.2858|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 141.0072|   240.7143|   240.7143|   240.7143|   240.7143|   41.30004|   41.30004|   240.7143|   41.30004|   41.30004|    240.7143|    240.7143|    41.30004|    41.30004|    41.30004|    41.30004|    240.7143|    41.30004|    240.7143|    41.30004|    240.7143|    41.30004|    41.30004|    41.30004|    41.30004|    240.7143|    240.7143|    41.30004|    240.7143|    240.7143|    41.30004|    41.30004|    240.7143|    240.7143|    240.7143|    240.7143|    41.30004|    240.7143|    41.30004|    240.7143|    41.30004|    41.30004|    41.30004|    41.30004|    41.30004|    240.7143|    240.7143|    41.30004|    240.7143|    240.7143|    41.30004|    41.30004|    240.7143|    240.7143|    240.7143|    240.7143|    41.30004|    240.7143|    41.30004|    240.7143|    41.30004|    240.7143|    240.7143|    240.7143|    240.7143|    41.30004|    41.30004|    240.7143|    41.30004|    41.30004|    240.7143|    240.7143|    41.30004|    41.30004|    41.30004|    41.30004|    240.7143|    41.30004|    240.7143|    41.30004|    240.7143|    1|       57| 443.870| 396.780| 427.970| 443.445| 418.659| 449.843| 516.755| 481.983| 366.538|  478.075| 426.008| 435.133| 453.348| 422.474| 455.716| 439.651| 405.524| 467.967| 394.096|  434.098| 401.136| 409.881| 413.004| 393.396| 433.268| 424.349| 406.283| 400.307| 383.053|  432.332|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 443.836| 412.311| 456.017| 414.868| 463.390| 396.421| 414.492| 463.735| 372.784|  416.948| 450.159| 372.321| 419.331| 415.684| 454.373| 396.183| 416.833| 462.638| 422.924|  405.198| 419.637| 369.663| 406.003| 443.158| 402.653| 439.935| 449.029| 474.734| 400.518|  448.606| 426.647| 414.058| 453.267| 427.081| 434.707| 418.490| 468.946| 424.650| 426.481|  414.536| 364.013| 385.907| 405.188| 416.708| 446.551| 358.091| 426.772| 370.101| 405.751|  397.489| 0.79668|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200002| 79202928|07MS |079200 |TUR0231 |7920000  |    1|         2|          344|          344|           NA|      6|        10|         4|      2002|         2|          2|          2|          1|          1|         NA|          2|          2|          1|          1|         NA|          1|          1|          1|          1|          2|          1|          1|          1|          2|          1|          1|          1|          2|0792001    |0792001    |0792001    |          3|          3|          2|          4|          3|          2|          1|          2|          3|          1|          1|          1|         NA|          5|          4|          1|          1|          1|          1|          3|          3|          3|          3|          3|          4|          4|          4|          4|          4|          1|          1|          3|          1|          3|          3|          3|          3|          4|          1|          4|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          6|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          3|          2|          2|          3|          2|          2|          1|          4|          4|          4|          4|          4|          1|          1|          1|          3|          3|          3|          3|          3|          3|          6|          6|          6|          6|          6|          6|          1|          1|          1|          1|          1|          1|          3|          5|          3|          4|          8|          1|          1|          1|          0|          0|          0|         NA|          0|          1|          4|          4|          4|          4|          4|          4|          4|          1|          1|          1|          3|          4|          4|          4|          3|          1|          3|          2|          4|          2|          3|          2|          3|          5|          5|          5|          4|          4|          4|          4|          4|          3|          1|          1|          4|          1|          4|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          4|          4|          1|          1|          1|          3|          2|          1|          1|          1|          1|          1|          1|          1|          2|          3|          3|          4|          4|          4|          2|          1|          2|          2|          1|          1|          1|          1|          1|          2|          3|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          3|          3|          4|          4|          4|          1|          4|          4|          1|          1|          1|          0|          1|          1|          1|          2|          2|          1|          2|          1|          2|          1|          1|          1|          1|          1|          2|          2|          2|          1|          1|          1|          1|          4|          4|          4|          0|         46|         40|          2|          2|          1|          1|          1|          1|          1|          1|          2|          4|          4|          4|          4|          4|          1|          2|          4|          3|          1|          2|          3|          1|          1|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          5|          5|          5|          4|          4|          5|          5|          5|          5|          5|          5|          5|          5|          5|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|         NA|          2|          2|          2|          1|          2|          1|          1|          1|          1|          3|          3|          3|          3|          3|          4|          4|          4|          4|          4|          3|          3|          2|          2|          2|          1|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|      10|      10|9701  |9329  |2149  |     0| 16.00|07920003 |079200 |079200 |079200 |   344|      3|      2|      3|      6|      6|      6|    16|        6|        6|        6|       16| 17.00| 16.36| 17.00|         NA|         NA|           NA|         NA|           NA|     1|       1|      0| 78.69|   160|   160|   160|  1840|       NA|       NA|     NA|     NA| -0.3786|  -1.64|   -1.72|    -0.04|       9|     10| -0.1272|  -0.8167| -0.1357| -0.0745| -0.3490|   2.0345|   0.0483| -1.0988| -0.3253| -1.5824|  -2.3003|    -0.5786|  -2.2177| -0.1119|    -2.4403|     1.2421|   1.6524| -1.9892| -0.4866|   1.0844|  2.0054|   1.8164| -1.8939|  1.7411| -0.5928|     2.3693|   1.8524|   -2.7142| -0.6916|  0.3014| -0.3066|   1.0349|  2.1449|  0.9289| -0.0263|   0.1369| -1.1549|  0.8801|      -0.7823|  2.5249| -2.2971|  0.2701| -2.1534|  0.0537|  2.0258| -0.3310|  -1.2188|    -1.3048|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 141.0072|   240.7143|   240.7143|   240.7143|   240.7143|   41.30004|   41.30004|   240.7143|   41.30004|   41.30004|    240.7143|    240.7143|    41.30004|    41.30004|    41.30004|    41.30004|    240.7143|    41.30004|    240.7143|    41.30004|    240.7143|    41.30004|    41.30004|    41.30004|    41.30004|    240.7143|    240.7143|    41.30004|    240.7143|    240.7143|    41.30004|    41.30004|    240.7143|    240.7143|    240.7143|    240.7143|    41.30004|    240.7143|    41.30004|    240.7143|    41.30004|    41.30004|    41.30004|    41.30004|    41.30004|    240.7143|    240.7143|    41.30004|    240.7143|    240.7143|    41.30004|    41.30004|    240.7143|    240.7143|    240.7143|    240.7143|    41.30004|    240.7143|    41.30004|    240.7143|    41.30004|    240.7143|    240.7143|    240.7143|    240.7143|    41.30004|    41.30004|    240.7143|    41.30004|    41.30004|    240.7143|    240.7143|    41.30004|    41.30004|    41.30004|    41.30004|    240.7143|    41.30004|    240.7143|    41.30004|    240.7143|    1|       57| 418.139| 361.718| 393.269| 393.235| 404.487| 389.460| 394.586| 417.914| 413.546|  390.016| 337.750| 374.678| 343.616| 319.301| 318.048| 357.921| 295.277| 332.347| 362.002|  361.905| 379.086| 432.544| 380.733| 364.132| 306.397| 347.663| 364.507| 346.814| 338.728|  324.971|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 409.927| 394.010| 389.691| 371.200| 366.854| 402.885| 427.311| 331.686| 307.682|  359.950| 416.622| 382.470| 413.758| 371.716| 364.574| 378.854| 386.800| 344.209| 341.800|  361.578| 409.945| 388.802| 410.297| 365.353| 357.619| 392.400| 397.926| 367.740| 356.009|  385.793| 359.043| 363.541| 417.164| 419.127| 382.980| 390.273| 357.180| 398.057| 345.840|  379.761| 398.593| 372.166| 385.107| 406.064| 383.030| 345.005| 361.854| 384.186| 332.480|  369.736| 0.79668|02MAY19:09:49:49 |   NA|

</div>


- PISA verisinde anne eğitim düzeyi **ve ya** baba eğitim düzeyi lisansüstü olan öğrencilerin seçilmesi


```r
PISA_STU_2018 %>% filter(MISCED==6 | FISCED==6) %>% head(4)
```

<div class="kable-table">

| CNTRYID|CNT | CNTSCHID| CNTSTUID|CYC  |NatCen |STRATUM |SUBNATIO | OECD| ADMINMODE| LANGTEST_QQQ| LANGTEST_COG| LANGTEST_PAQ| BOOKID| ST001D01T| ST003D02T| ST003D03T| ST004D01T| ST005Q01TA| ST006Q01TA| ST006Q02TA| ST006Q03TA| ST006Q04TA| ST007Q01TA| ST008Q01TA| ST008Q02TA| ST008Q03TA| ST008Q04TA| ST011Q01TA| ST011Q02TA| ST011Q03TA| ST011Q04TA| ST011Q05TA| ST011Q06TA| ST011Q07TA| ST011Q08TA| ST011Q09TA| ST011Q10TA| ST011Q11TA| ST011Q12TA| ST011Q16NA|ST011D17TA |ST011D18TA |ST011D19TA | ST012Q01TA| ST012Q02TA| ST012Q03TA| ST012Q05NA| ST012Q06NA| ST012Q07NA| ST012Q08NA| ST012Q09NA| ST013Q01TA| ST019AQ01T| ST019BQ01T| ST019CQ01T| ST021Q01TA| ST125Q01NA| ST126Q01TA| ST127Q01TA| ST127Q02TA| ST127Q03TA| ST022Q01TA| ST023Q01TA| ST023Q02TA| ST023Q03TA| ST023Q04TA| ST023Q05TA| ST097Q01TA| ST097Q02TA| ST097Q03TA| ST097Q04TA| ST097Q05TA| ST100Q01TA| ST100Q02TA| ST100Q03TA| ST100Q04TA| ST102Q01TA| ST102Q02TA| ST102Q03TA| ST102Q04TA| ST211Q01HA| ST211Q02HA| ST211Q03HA| ST212Q01HA| ST212Q02HA| ST212Q03HA| ST104Q02NA| ST104Q03NA| ST104Q04NA| ST213Q01HA| ST213Q02HA| ST213Q03HA| ST213Q04HA| ST150Q01IA| ST150Q02IA| ST150Q03IA| ST150Q04HA| ST152Q05IA| ST152Q06IA| ST152Q07IA| ST152Q08IA| ST154Q01HA| ST153Q01HA| ST153Q02HA| ST153Q03HA| ST153Q04HA| ST153Q05HA| ST153Q06HA| ST153Q08HA| ST153Q09HA| ST153Q10HA| ST158Q01HA| ST158Q02HA| ST158Q03HA| ST158Q04HA| ST158Q05HA| ST158Q06HA| ST158Q07HA| ST160Q01IA| ST160Q02IA| ST160Q03IA| ST160Q04IA| ST160Q05IA| ST167Q01IA| ST167Q02IA| ST167Q03IA| ST167Q04IA| ST167Q05IA| ST168Q01HA| ST175Q01IA| ST176Q01IA| ST176Q02IA| ST176Q03IA| ST176Q05IA| ST176Q06IA| ST176Q07IA| ST161Q01HA| ST161Q02HA| ST161Q03HA| ST161Q06HA| ST161Q07HA| ST161Q08HA| ST163Q02HA| ST163Q03HA| ST163Q04HA| ST164Q01IA| ST164Q02IA| ST164Q03IA| ST164Q04IA| ST164Q05IA| ST164Q06IA| ST165Q01IA| ST165Q02IA| ST165Q03IA| ST165Q04IA| ST165Q05IA| ST166Q01HA| ST166Q02HA| ST166Q03HA| ST166Q04HA| ST166Q05HA| ST016Q01NA| ST036Q05TA| ST036Q06TA| ST036Q08TA| ST225Q01HA| ST225Q02HA| ST225Q03HA| ST225Q04HA| ST225Q05HA| ST225Q06HA| ST181Q02HA| ST181Q03HA| ST181Q04HA| ST182Q03HA| ST182Q04HA| ST182Q05HA| ST182Q06HA| ST183Q01HA| ST183Q02HA| ST183Q03HA| ST184Q01HA| ST185Q01HA| ST185Q02HA| ST185Q03HA| ST186Q05HA| ST186Q06HA| ST186Q07HA| ST186Q10HA| ST186Q09HA| ST186Q02HA| ST186Q01HA| ST186Q08HA| ST186Q03HA| ST208Q01HA| ST208Q02HA| ST208Q04HA| ST188Q01HA| ST188Q02HA| ST188Q03HA| ST188Q06HA| ST188Q07HA| ST034Q01TA| ST034Q02TA| ST034Q03TA| ST034Q04TA| ST034Q05TA| ST034Q06TA| ST196Q02HA| ST196Q03HA| ST196Q04HA| ST196Q05HA| ST196Q06HA| ST196Q07HA| ST197Q01HA| ST197Q02HA| ST197Q04HA| ST197Q07HA| ST197Q08HA| ST197Q09HA| ST197Q12HA| ST215Q01HA| ST215Q02HA| ST215Q03HA| ST215Q04HA| ST215Q05HA| ST216Q01HA| ST216Q02HA| ST216Q03HA| ST216Q04HA| ST216Q05HA| ST216Q06HA| ST218Q01HA| ST218Q02HA| ST218Q03HA| ST218Q04HA| ST218Q05HA| ST218Q06HA| ST218Q07HA| ST222Q01HA| ST222Q03HA| ST222Q04HA| ST222Q05HA| ST222Q06HA| ST222Q08HA| ST222Q09HA| ST222Q10HA| ST214Q01HA| ST214Q02HA| ST214Q03HA| ST214Q06HA| ST220Q01HA| ST220Q02HA| ST220Q03HA| ST220Q04HA| ST217Q01HA| ST217Q02HA| ST217Q03HA| ST217Q04HA| ST217Q05HA| ST219Q01HA| ST219Q02HA| ST219Q03HA| ST219Q04HA| ST219Q05HA| ST219Q06HA| ST204Q02HA| ST204Q03HA| ST204Q04HA| ST204Q05HA| ST177Q01HA| ST177Q02HA| ST177Q03HA| ST189Q01HA| ST221Q01HA| ST221Q02HA| ST221Q03HA| ST221Q04HA| ST221Q05HA| ST221Q06HA| ST221Q07HA| ST221Q08HA| ST221Q09HA| ST221Q11HA| ST223Q02HA| ST223Q04HA| ST223Q05HA| ST223Q08HA| ST123Q02NA| ST123Q03NA| ST123Q04NA| ST205Q01HA| ST205Q02HA| ST205Q03HA| ST205Q04HA| ST059Q01TA| ST059Q02TA| ST059Q03TA| ST059Q04HA| ST060Q01NA| ST061Q01NA| ST062Q01TA| ST062Q02TA| ST062Q03TA| ST038Q03NA| ST038Q04NA| ST038Q05NA| ST038Q06NA| ST038Q07NA| ST038Q08NA| ST207Q01HA| ST207Q02HA| ST207Q03HA| ST207Q04HA| ST207Q05HA| ST206Q01HA| ST206Q02HA| ST206Q03HA| ST206Q04HA| IC001Q01TA| IC001Q02TA| IC001Q03TA| IC001Q04TA| IC001Q05TA| IC001Q06TA| IC001Q07TA| IC001Q08TA| IC001Q09TA| IC001Q10TA| IC001Q11TA| IC009Q01TA| IC009Q02TA| IC009Q03TA| IC009Q05NA| IC009Q06NA| IC009Q07NA| IC009Q08TA| IC009Q09TA| IC009Q10NA| IC009Q11NA| IC002Q01HA| IC004Q01HA| IC005Q01TA| IC006Q01TA| IC007Q01TA| IC150Q01HA| IC150Q02HA| IC150Q03HA| IC150Q04HA| IC150Q05HA| IC150Q06HA| IC150Q07HA| IC150Q08HA| IC150Q09HA| IC151Q01HA| IC151Q02HA| IC151Q03HA| IC151Q04HA| IC151Q05HA| IC151Q06HA| IC151Q07HA| IC151Q08HA| IC151Q09HA| IC152Q01HA| IC152Q02HA| IC152Q03HA| IC152Q04HA| IC152Q05HA| IC152Q06HA| IC152Q07HA| IC152Q08HA| IC152Q09HA| IC008Q01TA| IC008Q02TA| IC008Q03TA| IC008Q04TA| IC008Q05TA| IC008Q07NA| IC008Q08TA| IC008Q09TA| IC008Q10TA| IC008Q11TA| IC008Q12TA| IC008Q13NA| IC010Q01TA| IC010Q02NA| IC010Q03TA| IC010Q04TA| IC010Q05NA| IC010Q06NA| IC010Q07TA| IC010Q08TA| IC010Q09NA| IC010Q10NA| IC010Q11HA| IC010Q12HA| IC011Q01TA| IC011Q02TA| IC011Q03TA| IC011Q04TA| IC011Q05TA| IC011Q06TA| IC011Q07TA| IC011Q08TA| IC011Q09TA| IC011Q10HA| IC013Q01NA| IC013Q04NA| IC013Q05NA| IC013Q11NA| IC013Q12NA| IC013Q13NA| IC014Q03NA| IC014Q04NA| IC014Q06NA| IC014Q08NA| IC014Q09NA| IC015Q02NA| IC015Q03NA| IC015Q05NA| IC015Q07NA| IC015Q09NA| IC016Q01NA| IC016Q02NA| IC016Q04NA| IC016Q05NA| IC016Q07NA| IC169Q01HA| EC031Q01TA| EC032Q01TA| EC033Q01NA| EC150Q01WA| EC150Q02WA| EC150Q03WA| EC150Q04WA| EC150Q05WA| EC150Q06WA| EC150Q07WA| EC150Q08WA| EC150Q09WA| EC150Q10WA| EC151Q01WA| EC151Q01WB| EC151Q01WC| EC151Q02WA| EC151Q02WB| EC151Q02WC| EC151Q03WA| EC151Q03WB| EC151Q03WC| EC151Q04WA| EC151Q04WB| EC151Q04WC| EC151Q05WA| EC151Q05WB| EC151Q05WC| EC152Q01HA| EC153Q01HA| EC153Q02HA| EC153Q03HA| EC153Q04HA| EC153Q05HA| EC153Q06HA| EC153Q07HA| EC153Q08HA| EC153Q09HA| EC153Q10HA| EC153Q11HA| EC160Q01HA| EC158Q01HA| EC158Q02HA| EC159Q01HA| EC159Q02HA| EC163Q01HA| EC163Q02HA| EC163Q03HA| EC163Q04HA| EC163Q05HA| EC163Q06HA| EC163Q07HA| EC162Q01HA| EC162Q02HA| EC162Q03HA| EC162Q04HA| EC162Q05HA| EC162Q06HA| EC162Q07HA| EC162Q08HA| EC154Q01IA| EC154Q02IA| EC154Q03IA| EC154Q04HA| EC154Q05IA| EC154Q06IA| EC154Q07IA| EC154Q08HA| EC154Q09IA| EC012Q01NA| EC012Q02NA| EC012Q04NA| EC012Q06NA| EC012Q07NA| EC012Q08NA| EC012Q13HA| EC012Q12NA| EC155Q01DA| EC155Q02DA| EC155Q03DA| EC155Q04HA| EC155Q05HA| WB150Q01HA| WB151Q01HA| WB152Q01HA| WB153Q01HA| WB153Q02HA| WB153Q03HA| WB153Q04HA| WB153Q05HA| WB154Q01HA| WB154Q02HA| WB154Q03HA| WB154Q04HA| WB154Q05HA| WB154Q06HA| WB154Q07HA| WB154Q08HA| WB154Q09HA| WB155Q01HA| WB155Q02HA| WB155Q03HA| WB155Q04HA| WB155Q05HA| WB155Q06HA| WB155Q07HA| WB155Q08HA| WB155Q09HA| WB155Q10HA| WB156Q01HA| WB158Q01HA| WB160Q01HA| WB161Q01HA| WB162Q01HA| WB162Q02HA| WB162Q03HA| WB162Q04HA| WB162Q05HA| WB162Q06HA| WB162Q07HA| WB162Q08HA| WB162Q09HA| WB163Q01HA| WB163Q02HA| WB163Q03HA| WB163Q04HA| WB163Q05HA| WB163Q06HA| WB163Q07HA| WB163Q08HA| WB164Q01HA| WB165Q01HA| WB166Q01HA| WB166Q02HA| WB166Q03HA| WB166Q04HA| WB167Q01HA| WB168Q01HA| WB168Q02HA| WB168Q03HA| WB168Q04HA| WB171Q01HA| WB171Q02HA| WB171Q03HA| WB171Q04HA| WB172Q01HA| WB173Q01HA| WB173Q02HA| WB173Q03HA| WB173Q04HA| WB176Q01HA| WB177Q01HA| WB177Q02HA| WB177Q03HA| WB177Q04HA| WB032Q01NA| WB032Q02NA| WB031Q01NA| WB178Q01HA| WB178Q02HA| WB178Q03HA| WB178Q04HA| WB178Q05HA| WB178Q06HA| WB178Q07HA| FL150Q01TA| FL150Q02TA| FL150Q03TA| FL151Q01HA| FL151Q02HA| FL164Q01HA| FL164Q02HA| FL164Q03HA| FL164Q04HA| FL164Q05HA| FL164Q06HA| FL164Q07HA| FL164Q08HA| FL164Q09HA| FL164Q10HA| FL164Q11HA| FL164Q12HA| FL164Q13HA| FL164Q14HA| FL164Q15HA| FL164Q16HA| FL164Q17HA| FL164Q18HA| FL165Q01HA| FL165Q02HA| FL165Q03HA| FL165Q04HA| FL166Q01HA| FL166Q02HA| FL166Q03HA| FL166Q05HA| FL166Q06HA| FL166Q07HA| FL153Q01HA| FL153Q02HA| FL153Q03HA| FL153Q04HA| FL153Q05HA| FL153Q06HA| FL167Q01HA| FL167Q02HA| FL167Q03HA| FL167Q04HA| FL167Q05HA| FL156Q01TA| FL156Q02TA| FL156Q03TA| FL156Q04TA| FL156Q05TA| FL156Q06TA| FL156Q07HA| FL159Q01HA| FL159Q02HA| FL159Q03HA| FL159Q04HA| FL160Q01HA| FL160Q02HA| FL160Q03HA| FL160Q04HA| FL161Q01HA| FL161Q02HA| FL161Q03HA| FL162Q01HA| FL162Q02HA| FL162Q03HA| FL162Q04HA| FL162Q05HA| FL162Q06HA| FL163Q01HA| FL163Q02HA| FL163Q03HA| FL163Q04HA| FL163Q05HA| FL168Q01HA| FL168Q02HA| FL168Q03HA| FL168Q04HA| FL168Q05HA| FL168Q06HA| FL168Q07HA| FL168Q08HA| FL169Q01HA| FL169Q02HA| FL169Q03HA| FL169Q04HA| PA001Q01TA| PA001Q02TA| PA001Q03TA| PA003Q01TA| PA003Q02TA| PA003Q03TA| PA003Q04HA| PA003Q05IA| PA003Q06IA| PA003Q07IA| PA154Q01IA| PA154Q02IA| PA154Q03IA| PA154Q04IA| PA154Q05IA| PA154Q06IA| PA154Q07IA| PA154Q08IA| PA154Q09IA| PA154Q10HA| PA155Q01IA| PA156Q01HA| PA156Q02HA| PA156Q03HA| PA156Q04HA| PA004Q02NA| PA004Q03NA| PA004Q04NA| PA008Q01TA| PA008Q02TA| PA008Q03TA| PA008Q04TA| PA008Q05TA| PA008Q06NA| PA008Q07NA| PA008Q08NA| PA008Q09NA| PA008Q10NA| PA009Q01NA| PA009Q02NA| PA009Q03NA| PA009Q04NA| PA009Q05NA| PA009Q06NA| PA009Q07NA| PA009Q08NA| PA009Q09NA| PA009Q10NA| PA009Q11NA| PA007Q01TA| PA007Q02TA| PA007Q03TA| PA007Q04TA| PA007Q05TA| PA007Q06TA| PA007Q07TA| PA007Q09NA| PA007Q11NA| PA007Q12NA| PA007Q13NA| PA007Q14NA| PA007Q15NA| PA005Q01TA| PA006Q01TA| PA006Q02TA| PA006Q03TA| PA006Q04TA| PA006Q05TA| PA006Q06TA| PA006Q07TA| PA006Q08TA| PA006Q09TA| PA006Q10TA| PA006Q11TA| PA006Q12HA| PA006Q13HA| PA006Q14HA| PA158Q01HA| PA158Q02IA| PA158Q03HA| PA158Q04IA| PA158Q05HA| PA159Q01HA| PA160Q01HA| PA160Q02HA| PA160Q03HA| PA160Q04HA| PA160Q05HA| PA161Q01HA| PA161Q02HA| PA161Q03HA| PA161Q05HA| PA161Q06HA| PA161Q07HA| PA162Q01HA| PA163Q01HA| PA166Q01HA| PA167Q02HA| PA167Q03HA| PA167Q04HA| PA167Q05HA| PA168Q01HA| PA168Q02HA| PA168Q03HA| PA168Q06HA| PA169Q01HA| PA169Q02HA| PA169Q03HA| PA169Q04HA| PA169Q05HA| PA169Q06HA| PA170Q01HA| PA170Q02HA| PA170Q04HA| PA170Q07HA| PA170Q08HA| PA170Q09HA| PA170Q12HA| PA171Q01HA| PA171Q03HA| PA171Q04HA| PA171Q05HA| PA171Q06HA| PA171Q08HA| PA171Q09HA| PA171Q10HA| PA172Q01WA| PA172Q02WA| PA172Q03WA| PA172Q04WA| PA172Q05WA| PA172Q06WA| PA018Q01NA| PA018Q02NA| PA018Q03NA| PA177Q01HA| PA177Q02HA| PA177Q03HA| PA177Q04HA| PA177Q05HA| PA177Q06HA| PA177Q07HA| PA177Q08HA| PA180Q01HA| PA182Q01HA| PA175Q01HA| PA175Q02HA| PA041Q01TA| PA042Q01TA| EFFORT1| EFFORT2|OCOD1 |OCOD2 |OCOD3 | GRADE|   AGE|PROGN    |COBN_S |COBN_M |COBN_F | LANGN| ISCEDL| ISCEDD| ISCEDO| MISCED| FISCED| HISCED| PARED| MISCED_D| FISCED_D| HISCED_D| PAREDINT| BMMJ1| BFMJ2| HISEI| LANGMOTHER| LANGFATHER| LANGSIBLINGS| LANGFRIEND| LANGSCHMATES| IMMIG| DURECEC| REPEAT|  BSMJ| MMINS| LMINS| SMINS| TMINS| FCFMLRTY| SCCHANGE| CHANGE| STUBMI|    ESCS| UNDREM| METASUM| METASPAM| ICTHOME| ICTSCH| HOMEPOS| CULTPOSS|  HEDRES|  WEALTH|  ICTRES| DISCLIMA| TEACHSUP|  DIRINS| PERFEED| EMOSUPS| STIMREAD| ADAPTIVITY| TEACHINT| JOYREAD| SCREADCOMP| SCREADDIFF| PISADIFF| PERCOMP| PERCOOP| ATTLNACT| COMPETE| WORKMAST| GFOFAIL|   EUDMO|    SWBP| RESILIENCE| MASTGOAL| GCSELFEFF| GCAWARE|  ATTIMM| INTCULT| PERSPECT| COGFLEX| RESPECT|  AWACOM| GLOBMIND| DISCRIM|  BELONG| BEINGBULLIED|  ENTUSE| HOMESCH|  USESCH|  INTICT| COMPICT|  AUTICT| SOIAICT| ICTCLASS| ICTOUTSIDE| INFOCAR| INFOJOB1| INFOJOB2| FLCONFIN| FLCONICT| FLSCHOOL| FLFAMILY| CURSUPP| EMOSUPP| PQSCHOOL| PASCHPOL| PRESUPP| JOYREADP| ATTIMMP| INTCULTP| GCAWAREP| BODYIMA| SOCONPA| W_FSTUWT| W_FSTURWT1| W_FSTURWT2| W_FSTURWT3| W_FSTURWT4| W_FSTURWT5| W_FSTURWT6| W_FSTURWT7| W_FSTURWT8| W_FSTURWT9| W_FSTURWT10| W_FSTURWT11| W_FSTURWT12| W_FSTURWT13| W_FSTURWT14| W_FSTURWT15| W_FSTURWT16| W_FSTURWT17| W_FSTURWT18| W_FSTURWT19| W_FSTURWT20| W_FSTURWT21| W_FSTURWT22| W_FSTURWT23| W_FSTURWT24| W_FSTURWT25| W_FSTURWT26| W_FSTURWT27| W_FSTURWT28| W_FSTURWT29| W_FSTURWT30| W_FSTURWT31| W_FSTURWT32| W_FSTURWT33| W_FSTURWT34| W_FSTURWT35| W_FSTURWT36| W_FSTURWT37| W_FSTURWT38| W_FSTURWT39| W_FSTURWT40| W_FSTURWT41| W_FSTURWT42| W_FSTURWT43| W_FSTURWT44| W_FSTURWT45| W_FSTURWT46| W_FSTURWT47| W_FSTURWT48| W_FSTURWT49| W_FSTURWT50| W_FSTURWT51| W_FSTURWT52| W_FSTURWT53| W_FSTURWT54| W_FSTURWT55| W_FSTURWT56| W_FSTURWT57| W_FSTURWT58| W_FSTURWT59| W_FSTURWT60| W_FSTURWT61| W_FSTURWT62| W_FSTURWT63| W_FSTURWT64| W_FSTURWT65| W_FSTURWT66| W_FSTURWT67| W_FSTURWT68| W_FSTURWT69| W_FSTURWT70| W_FSTURWT71| W_FSTURWT72| W_FSTURWT73| W_FSTURWT74| W_FSTURWT75| W_FSTURWT76| W_FSTURWT77| W_FSTURWT78| W_FSTURWT79| W_FSTURWT80| UNIT| WVARSTRR| PV1MATH| PV2MATH| PV3MATH| PV4MATH| PV5MATH| PV6MATH| PV7MATH| PV8MATH| PV9MATH| PV10MATH| PV1READ| PV2READ| PV3READ| PV4READ| PV5READ| PV6READ| PV7READ| PV8READ| PV9READ| PV10READ| PV1SCIE| PV2SCIE| PV3SCIE| PV4SCIE| PV5SCIE| PV6SCIE| PV7SCIE| PV8SCIE| PV9SCIE| PV10SCIE| PV1GLCM| PV2GLCM| PV3GLCM| PV4GLCM| PV5GLCM| PV6GLCM| PV7GLCM| PV8GLCM| PV9GLCM| PV10GLCM| PV1RCLI| PV2RCLI| PV3RCLI| PV4RCLI| PV5RCLI| PV6RCLI| PV7RCLI| PV8RCLI| PV9RCLI| PV10RCLI| PV1RCUN| PV2RCUN| PV3RCUN| PV4RCUN| PV5RCUN| PV6RCUN| PV7RCUN| PV8RCUN| PV9RCUN| PV10RCUN| PV1RCER| PV2RCER| PV3RCER| PV4RCER| PV5RCER| PV6RCER| PV7RCER| PV8RCER| PV9RCER| PV10RCER| PV1RTSN| PV2RTSN| PV3RTSN| PV4RTSN| PV5RTSN| PV6RTSN| PV7RTSN| PV8RTSN| PV9RTSN| PV10RTSN| PV1RTML| PV2RTML| PV3RTML| PV4RTML| PV5RTML| PV6RTML| PV7RTML| PV8RTML| PV9RTML| PV10RTML|   SENWT|VER_DAT          | test|
|-------:|:---|--------:|--------:|:----|:------|:-------|:--------|----:|---------:|------------:|------------:|------------:|------:|---------:|---------:|---------:|---------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|:----------|:----------|:----------|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|-------:|-------:|:-----|:-----|:-----|-----:|-----:|:--------|:------|:------|:------|-----:|------:|------:|------:|------:|------:|------:|-----:|--------:|--------:|--------:|--------:|-----:|-----:|-----:|----------:|----------:|------------:|----------:|------------:|-----:|-------:|------:|-----:|-----:|-----:|-----:|-----:|--------:|--------:|------:|------:|-------:|------:|-------:|--------:|-------:|------:|-------:|--------:|-------:|-------:|-------:|--------:|--------:|-------:|-------:|-------:|--------:|----------:|--------:|-------:|----------:|----------:|--------:|-------:|-------:|--------:|-------:|--------:|-------:|-------:|-------:|----------:|--------:|---------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|--------:|-------:|-------:|------------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|----------:|-------:|--------:|--------:|--------:|--------:|--------:|--------:|-------:|-------:|--------:|--------:|-------:|--------:|-------:|--------:|--------:|-------:|-------:|--------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|----:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|:----------------|----:|
|     792|TUR | 79200001| 79201275|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|     21|         9|         9|      2002|         2|          1|         NA|          1|         NA|         NA|          1|         NA|          1|         NA|         NA|          1|          1|          1|          1|          2|          1|          2|          2|          2|          1|          2|          1|          2|0792001    |0792002    |0792002    |          3|          1|          1|          2|          2|          1|          1|          1|          1|          1|          1|          1|         NA|          6|          5|          1|          1|          1|          1|          4|          4|          4|          4|          4|          2|          2|          3|          1|          1|          3|          2|          1|          4|          2|          3|          4|          3|          3|          2|          2|          2|          2|          2|          3|          2|          3|          2|          2|          2|          2|          4|          4|          4|          4|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          3|          1|          1|          3|          3|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          2|          2|          2|          1|          1|          1|          6|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|          2|          2|          2|          0|          0|          0|         NA|          0|          1|          4|          3|          4|          1|          1|          1|          1|          1|          1|          1|          3|          1|          1|          1|          4|          2|          1|          1|          4|          1|          2|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|          2|          3|          2|          2|          3|          1|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          3|          3|          1|          2|          1|          3|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|          1|          3|          2|          2|          1|          2|          1|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          2|          2|          2|          2|          1|          1|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|         NA|          3|          2|          2|          2|          2|          5|          6|          6|          4|         40|         40|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          2|          2|          3|          2|          2|          2|          2|          1|          1|          1|          1|          1|          3|          1|          2|          1|          2|          3|          1|          1|          1|          1|          2|          2|          2|          3|          2|          1|          1|          2|          1|          5|          5|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          3|          4|          4|          1|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|      10|      10|2330  |2330  |2211  |    -1| 15.58|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      6|      6|      6|    16|        6|        6|        6|       16| 82.41| 82.41| 82.41|         NA|         NA|           NA|         NA|           NA|     1|       1|      0| 88.70|   240|   200|   240|  1600|       NA|       NA|     NA|     NA|  0.0324|  -0.60|   -1.72|    -1.41|       9|      9| -2.1008|  -2.7469| -0.6853| -2.1121| -1.7005|  -1.1699|  -0.4060| -1.0499|  0.2682|      NA|  -0.6200|    -0.5786|  -1.0615| -1.1538|    -0.8250|     1.2421|   0.2705| -0.6142| -0.9391|  -0.6583|  1.1811|  -2.7365| -1.8939| -2.1464| -1.2568|    -1.4832|  -1.3162|   -2.7142| -0.0549| -1.2083| -0.2157|  -0.3405|  1.3823| -1.2781| -1.3933|    0.291| -1.1549| -0.4217|       1.1625| -2.7049| -0.5991| -1.0707| -2.9336| -2.6033| -2.5144|  0.2639|   1.0418|    -1.3048|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 417.314| 486.246| 419.767| 413.368| 508.158| 475.248| 527.383| 482.872| 477.418|  476.539| 393.006| 428.757| 364.850| 382.522| 378.563| 416.048| 395.846| 383.782| 374.509|  381.877| 402.112| 431.478| 384.063| 472.941| 420.800| 472.894| 460.407| 465.356| 439.954|  442.546|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 377.648| 346.106| 347.468| 351.544| 464.958| 406.800| 305.063| 415.645| 451.572|  332.146| 418.336| 387.692| 376.644| 348.832| 469.856| 438.034| 377.209| 433.141| 463.976|  390.554| 370.646| 356.020| 346.501| 346.212| 425.656| 396.229| 416.122| 421.807| 457.353|  390.627| 419.099| 390.744| 410.400| 377.828| 443.815| 406.021| 393.957| 420.428| 398.023|  462.478| 400.889| 416.115| 426.449| 396.449| 425.235| 391.150| 373.368| 416.023| 417.897|  416.855| 0.80261|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200001| 79201556|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|     17|        10|         8|      2002|         2|          1|          2|          2|          2|         NA|          1|          2|          1|          2|         NA|          1|          1|          1|          1|          2|          1|          1|          2|          2|          1|          1|          1|          2|0792001    |0792002    |0792001    |          2|          3|          2|          4|          2|          1|          1|          1|          2|          1|          1|          1|         NA|          7|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|          3|          2|          2|          3|          4|          3|          3|          3|          3|          3|          3|          3|          2|          3|          3|          1|          2|          1|          3|          2|          3|          2|          2|          3|          3|          2|          2|          3|          3|          2|          2|          2|          2|          4|          2|          1|          2|          1|          2|          2|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          3|          2|          2|          2|          2|          3|          3|          3|          5|          2|          4|          3|          5|          5|          5|          5|          4|          3|          3|          3|          3|          3|          3|          2|          2|          2|          4|          2|          6|          5|          6|          6|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          2|          2|          2|          1|          1|          1|         NA|          0|          1|          3|          3|          3|          2|          3|          4|          3|          3|          2|          3|          4|          4|          2|          3|          3|          1|          3|          2|          3|          2|          3|          2|          3|          2|          3|          2|          4|          4|          4|          4|          4|          4|          2|          2|          4|          2|          3|          1|          1|          1|          1|          1|          1|          1|          1|         NA|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          1|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          2|          1|          2|          1|          2|          2|          2|          1|          2|          2|          2|          2|          2|          2|          3|          3|          3|          2|          2|          2|          2|          4|          5|          2|          2|         30|         20|          2|          2|          2|          1|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          2|          2|          2|          2|          1|          1|          3|          1|          3|          1|          1|          1|          3|          3|          3|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          5|          5|          6|          1|          1|          3|          3|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          3|          3|          4|          4|          4|          4|          4|          4|          4|          4|          4|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          2|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|       8|      10|9701  |2149  |2611  |     0| 15.67|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      4|      6|      6|    16|        4|        6|        6|       16| 17.00| 78.69| 78.69|         NA|         NA|           NA|         NA|           NA|     1|      NA|      0| 86.72|   100|    80|    40|   600|       NA|       NA|     NA|     NA|  0.3978|   0.45|   -1.72|    -1.41|       6|     10| -1.0700|  -1.7393| -0.1357| -1.0005| -1.2275|  -0.5396|  -1.3345| -1.0988|  0.2682| -0.6576|  -0.6200|    -1.4494|  -0.6079|  0.3568|     0.1222|     1.2421|   0.2705| -0.6142| -0.9391|  -0.6583|  0.1956|  -0.1982| -0.2006| -0.0193| -0.5928|     2.3693|  -0.9149|   -2.7142| -3.4472| -0.2014|  0.2865|   0.1686|  0.2165| -1.4721| -0.1577|    0.291|  0.5881|  0.2243|      -0.7823| -0.9501| -0.0861|  0.7849| -1.2900|  0.0537|  0.0979|  0.5149|   0.2080|     1.1397|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 450.910| 448.120| 394.473| 460.198| 454.828| 449.245| 489.145| 476.646| 505.314|  507.013| 441.286| 415.682| 406.586| 437.001| 473.036| 416.363| 427.909| 471.902| 419.949|  439.851| 453.525| 440.738| 459.294| 471.902| 465.314| 488.763| 465.500| 487.284| 474.574|  457.588|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 481.527| 376.670| 396.524| 524.728| 438.520| 429.856| 416.504| 430.541| 467.738|  431.698| 491.194| 457.365| 446.866| 529.190| 447.829| 494.859| 471.574| 475.993| 477.110|  488.957| 510.438| 444.392| 428.712| 530.462| 448.440| 449.362| 469.799| 465.111| 468.271|  484.944| 502.328| 434.123| 528.107| 424.583| 467.751| 437.751| 488.107| 442.279| 452.980|  491.581| 453.225| 486.874| 502.363| 457.223| 505.248| 487.735| 469.526| 474.984| 448.720|  541.895| 0.80261|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200001| 79202343|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|     22|        11|         3|      2002|         2|          1|          1|          1|          1|         NA|          1|         NA|          1|         NA|         NA|          1|          1|          1|          1|          2|          1|          2|          2|          2|          2|          2|          1|          1|0792001    |0792001    |0792001    |          3|          4|          3|          4|          3|          3|          1|          3|          1|          1|          1|          1|         NA|          6|          6|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          2|          2|          4|          3|          3|          4|          3|          2|          3|          2|          3|          3|          4|          1|          1|          2|          3|          3|          4|          1|          1|          1|          1|          2|          2|          2|          2|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          1|          2|         NA|          5|         NA|          1|          5|          5|          1|          4|          4|          4|          2|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          0|          4|          2|          3|          0|          0|          1|         NA|          0|          0|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          3|          4|          3|          4|          3|          2|          4|          1|          3|          1|          4|          2|          4|          1|          2|          2|          4|          3|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|         NA|          1|         NA|         NA|         NA|         NA|         NA|         NA|         NA|          1|          2|          3|          4|          5|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          5|          1|          1|          1|          1|          5|          5|          5|          5|          5|          3|         NA|         NA|         NA|         NA|         NA|          3|          3|          2|          3|          2|          1|          1|          3|          2|          2|          1|          2|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          0|          2|          0|         20|         30|          4|          4|          2|          1|          1|          1|          1|          1|          1|          4|          1|          1|          1|          1|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          5|          7|          7|          2|          1|          2|          1|          3|          4|          4|          4|          1|          4|          1|          2|          2|          5|          4|          4|          4|          5|          5|          5|          5|          5|          5|         NA|         NA|         NA|         NA|          5|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|          3|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          4|          4|          4|          4|          4|          4|          3|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          3|          3|          4|         NA|          3|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|       7|       9|9701  |6111  |2330  |     1| 16.08|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      6|      6|      6|    16|        6|        6|        6|       16| 17.00| 11.56| 17.00|         NA|         NA|           NA|         NA|           NA|     1|       2|      0| 82.41|     0|    60|    60|   600|       NA|       NA|     NA|     NA| -0.4280|  -1.64|   -1.72|    -1.41|      11|     10| -0.2441|  -1.2687| -1.0118|  0.6090| -0.1120|  -1.4882|  -1.5550| -0.5066|  1.1225| -2.4468|  -2.3003|    -1.6010|  -2.2177| -0.1119|    -0.3140|     0.2426|   0.2705| -1.9892| -1.6237|  -1.6038|  2.0054|  -2.7365| -1.8939|  1.1963|  0.6502|     1.5900|  -1.4972|   -2.6739|      NA| -0.6155| -0.0180|  -0.2098| -0.8312| -3.1739| -2.7948|       NA| -1.1549| -1.2605|      -0.7823|      NA|  2.3702|  3.3041|  2.6186|  1.4987|  2.0258|  1.4359|   0.2764|     0.5477|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 319.885| 325.236| 298.124| 347.893| 344.137| 332.804| 309.840| 414.770| 310.236|  393.137| 319.453| 333.203| 345.495| 339.966| 346.631| 336.530| 325.728| 322.760| 315.270|  302.398| 366.331| 434.453| 385.126| 406.671| 436.551| 410.509| 382.595| 415.349| 392.922|  369.015|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 283.543| 366.617| 279.752| 300.736| 324.928| 291.124| 291.853| 289.940| 254.055|  227.516| 358.106| 363.373| 337.079| 305.745| 345.937| 316.643| 330.522| 345.601| 305.511|  333.845| 357.716| 390.257| 312.117| 343.106| 459.546| 320.759| 363.881| 368.221| 351.077|  367.712| 349.881| 326.972| 361.684| 320.697| 356.205| 366.312| 364.327| 303.503| 310.790|  355.886| 392.458| 301.654| 400.555| 347.418| 370.830| 351.170| 382.755| 390.538| 411.888|  355.742| 0.80261|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200001| 79203553|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|     15|        10|         1|      2002|         1|          2|         NA|          1|          1|         NA|          2|         NA|         NA|          1|         NA|          1|          1|          1|          1|         NA|          1|          1|          1|          1|          1|          2|          1|          1|0792001    |0792002    |0792001    |          3|          2|          1|          4|          3|          3|          1|          2|          5|          1|          1|          1|         NA|          2|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          3|          2|          2|          2|          1|          1|          1|          3|          1|          2|          2|          3|          3|          2|          1|          2|          2|          2|          2|          2|          2|          2|          3|          2|          1|          1|          1|          1|          2|          2|          2|          2|          4|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          3|          4|          1|          2|          1|          3|          4|          4|          1|          2|          3|          2|          5|          4|          4|          2|          3|          2|          3|          2|          2|          3|          2|          2|          3|          1|          5|          5|          4|          6|          6|          2|          2|          3|          4|          5|          6|          4|          4|          4|          4|          4|          1|          2|          2|          2|          0|          0|          0|         NA|          0|          1|          3|          4|          4|          3|          3|          3|          3|          1|          2|          4|          3|          3|          2|          3|          3|          4|          2|          2|          2|          4|          3|          3|          2|          2|          2|          3|          3|          4|          3|          2|          3|          2|          4|          4|          3|          4|          2|          4|          4|          3|          3|          3|          3|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          2|          1|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          4|          4|          4|          1|          1|          1|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          3|          3|          3|          3|          2|          2|          3|          5|          6|          7|          6|         40|         40|          2|          1|          1|          2|          2|          4|          1|          1|          4|          4|          4|          4|          4|          4|          3|          3|          3|          3|          2|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          3|          3|          3|          3|          2|          2|          2|          2|          2|          2|          3|          4|          2|          6|          7|          1|          1|          4|          4|          1|          1|          1|          1|          2|          2|          2|          2|          4|          2|          4|          2|          2|          2|          4|          4|          1|          1|          4|          5|          4|          5|          3|          1|          1|          2|          4|          1|          1|          4|          3|          1|          4|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          3|          2|          4|          3|          4|          2|          3|          3|          3|          2|          2|          3|          3|          2|          3|          3|          3|          3|          3|          2|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|       8|      10|2221  |9703  |5111  |     0| 16.25|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      6|      5|      6|    16|        6|        5|        6|       16| 68.70| 17.00| 68.70|         NA|         NA|           NA|         NA|           NA|     1|       4|      0| 46.76|   240|   200|   280|  1600|       NA|       NA|     NA|     NA|  0.6187|   0.80|    0.98|    -1.41|      11|      6| -0.0982|   0.6014| -0.5089| -0.6098|  0.0154|   0.1625|   0.7628|  0.0351| -0.3253| -0.6576|  -0.6200|    -1.0467|  -0.8687|  1.1914|    -0.8490|     0.4090|   0.7323| -0.2309|  0.6012|  -0.6583|  1.2643|  -0.1015| -0.3288| -0.3121| -1.1176|    -0.0960|  -1.0266|    0.5471|  2.3015|  0.9840|  0.2865|  -1.7137| -1.6677|  0.9289| -0.1577|    0.291|  0.5881| -1.2487|       1.7757| -0.6642| -0.0861|  0.3558| -0.1436| -0.1996| -0.7462|  0.5149|   0.5207|     0.5761|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 415.225| 440.810| 484.132| 443.869| 465.435| 439.322| 541.338| 560.146| 499.883|  442.704| 518.787| 519.112| 502.570| 460.873| 493.765| 487.487| 545.821| 533.014| 560.481|  512.165| 497.778| 498.176| 496.351| 481.535| 446.003| 471.244| 488.351| 485.299| 488.595|  487.027|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 473.410| 503.853| 410.128| 449.512| 456.477| 465.956| 490.658| 481.180| 502.043|  510.345| 479.546| 544.253| 451.091| 449.859| 515.263| 495.030| 507.116| 502.315| 500.315|  511.370| 533.638| 567.418| 490.035| 544.260| 518.100| 541.488| 551.262| 545.764| 505.330|  547.064| 476.441| 511.302| 466.972| 513.422| 511.897| 507.532| 495.385| 513.871| 537.022|  463.353| 503.396| 524.080| 483.114| 521.571| 534.724| 546.075| 496.663| 530.087| 597.237|  532.370| 0.80261|02MAY19:09:49:49 |   NA|

</div>




<!--chapter:end:09-veri_duzenlemeI.Rmd-->

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


<!--chapter:end:11-veri_duzenlemeII.Rmd-->

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

<div class="kable-table">

|   OKULID| OGRENCIID| CINSIYET|     SES|
|--------:|---------:|--------:|-------:|
| 79200001|  79200768|        2| -2.4521|
| 79200001|  79201064|        2| -2.1042|
| 79200001|  79201118|        1| -2.2700|
| 79200001|  79201275|        2|  0.0324|
| 79200001|  79201481|        2| -0.0674|
| 79200001|  79201556|        2|  0.3978|

</div>

Aynı işlem `c()` fonksiyonu içinde de yapılabilir.


```r
select(PISA_OGR_2018, c(OKULID, OGRENCIID, CINSIYET ,SES))
```

- **select()** fonksiyonu ile sütun bazında seçim yapılabilir.


```r
PISA_OGR_2018 %>% select(OKULID, OGRENCIID, CINSIYET ,SES) %>% head(6)
```

<div class="kable-table">

|   OKULID| OGRENCIID| CINSIYET|     SES|
|--------:|---------:|--------:|-------:|
| 79200001|  79200768|        2| -2.4521|
| 79200001|  79201064|        2| -2.1042|
| 79200001|  79201118|        1| -2.2700|
| 79200001|  79201275|        2|  0.0324|
| 79200001|  79201481|        2| -0.0674|
| 79200001|  79201556|        2|  0.3978|

</div>


- **select()** fonksiyonu belirli bir aralıktaki değişkenler iki nokta `:` opertorü ile seçilebilir.

- örneğin okumadan alınan zevke ilişkin maddeler aşağıdaki şekilde seçilebilir.


```r
PISA_OGR_2018 %>% select(ST097Q01TA:ST097Q05TA) %>% head(6)
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
PISA_OGR_2018 %>% select(OKULID:SINIF,-KITAPCIK) %>% head(6)
```

<div class="kable-table">

|   OKULID| OGRENCIID|OKUL_TUR | SINIF|
|--------:|---------:|:--------|-----:|
| 79200001|  79200768|TUR0112  |    10|
| 79200001|  79201064|TUR0112  |    10|
| 79200001|  79201118|TUR0112  |    10|
| 79200001|  79201275|TUR0112  |     9|
| 79200001|  79201481|TUR0112  |     9|
| 79200001|  79201556|TUR0112  |    10|

</div>


### **starts_with()**

- Sadece **select()** fonksiyonu içinde çalışan birtakım fonksiyonlar değişken seçim işini kolaylaştırır.

- **ST097** ile başlayan degişkenlerin seçilmesi


```r
select(PISA_OGR_2018, starts_with("ST097")) %>% head(6)
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

- **NA** ile **biten** degişkenlerin seçilmesi


```r
select(PISA_OGR_2018, ends_with("NA")) %>% head(6)
```

<div class="kable-table">

| ST104Q02NA| ST104Q03NA| ST104Q04NA| ST016Q01NA| ST123Q02NA| ST123Q03NA| ST123Q04NA| ST060Q01NA| ST061Q01NA| ST038Q03NA| ST038Q04NA| ST038Q05NA| ST038Q06NA| ST038Q07NA| ST038Q08NA| IC009Q05NA| IC009Q06NA| IC009Q07NA| IC009Q10NA| IC009Q11NA| IC008Q07NA| IC008Q13NA| IC010Q02NA| IC010Q05NA| IC010Q06NA| IC010Q09NA| IC010Q10NA| IC013Q01NA| IC013Q04NA| IC013Q05NA| IC013Q11NA| IC013Q12NA| IC013Q13NA| IC014Q03NA| IC014Q04NA| IC014Q06NA| IC014Q08NA| IC014Q09NA| IC015Q02NA| IC015Q03NA| IC015Q05NA| IC015Q07NA| IC015Q09NA| IC016Q01NA| IC016Q02NA| IC016Q04NA| IC016Q05NA| IC016Q07NA|
|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|
|          2|          2|          2|         NA|          4|          4|          4|         NA|         NA|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          1|          1|          2|          1|          2|          1|          1|          5|          4|          4|          4|          2|          4|          4|          3|          3|          3|          3|          3|          4|          4|          4|          4|          4|          3|          3|          3|          3|          3|
|          2|          2|          3|          7|          4|          3|          1|         60|         35|          4|          4|          2|          1|          2|          3|          3|          3|          3|          3|          1|          1|          2|          3|          4|          4|          2|          5|          4|          3|          4|          4|          4|          4|          3|          4|          4|          4|          4|          4|          4|          4|          4|          3|          4|          4|          4|          4|          4|
|          2|          2|          2|          4|          3|          3|          3|         41|         70|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|
|          3|          2|          3|          3|          3|         NA|          3|         40|         40|          2|          2|          2|          2|          2|          2|          1|          2|          2|          2|          1|          1|          1|          1|          1|          1|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          3|          4|          4|
|          3|          2|          4|          1|          1|          1|          1|         44|         40|          2|          2|          1|          1|          1|          1|          1|          1|          1|          3|          1|          5|          5|          5|          5|          5|          5|          5|          4|          3|          4|          4|          4|          4|          2|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|
|          3|          2|          3|          4|          3|          3|          3|         30|         20|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|

</div>


### **contains()**

- **OKUMA** geçen değişkenlerin seçilmesi


```r
select(PISA_OGR_2018,contains("OKUMA")) %>% head(6)
```

<div class="kable-table">

| OKUMA_BAGLILIGI| OKUMA_ZEVK| ODOKUMA1| ODOKUMA2| ODOKUMA3| ODOKUMA4| ODOKUMA5| ODOKUMA6| ODOKUMA7| ODOKUMA8| ODOKUMA9| ODOKUMA10|
|---------------:|----------:|--------:|--------:|--------:|--------:|--------:|--------:|--------:|--------:|--------:|---------:|
|         -0.9225|    -0.2891|  376.022|  417.746|  420.630|  413.837|  434.434|  424.054|  470.450|  446.634|  440.164|   443.152|
|          1.0741|     0.6040|  512.316|  473.229|  563.902|  485.396|  500.394|  495.048|  477.050|  526.291|  523.062|   481.411|
|         -0.6200|     0.6380|  396.383|  413.859|  423.121|  452.124|  392.434|  433.205|  387.037|  406.997|  402.509|   438.667|
|         -0.6200|    -1.1538|  393.006|  428.757|  364.850|  382.522|  378.563|  416.048|  395.846|  383.782|  374.509|   381.877|
|          0.3780|     0.6669|  552.457|  570.109|  562.955|  530.835|  532.487|  521.763|  481.840|  540.839|  471.671|   519.829|
|         -0.6200|     0.3568|  441.286|  415.682|  406.586|  437.001|  473.036|  416.363|  427.909|  471.902|  419.949|   439.851|

</div>


###  **matches()**

- içinde **02** geçen değişkenlerin seçilmesi


```r
select(PISA_OGR_2018,matches("02")) %>% head(6)
```

<div class="kable-table">

| ST097Q02TA| ST100Q02TA| ST102Q01TA| ST102Q02TA| ST102Q03TA| ST102Q04TA| ST211Q02HA| ST212Q02HA| ST104Q02NA| ST213Q02HA| ST150Q02IA| ST153Q02HA| ST158Q02HA| ST160Q02IA| ST167Q02IA| ST176Q02IA| ST161Q02HA| ST163Q02HA| ST164Q02IA| ST165Q02IA| ST166Q02HA| ST225Q02HA| ST181Q02HA| ST183Q02HA| ST185Q02HA| ST186Q02HA| ST208Q02HA| ST188Q02HA| ST034Q02TA| ST196Q02HA| ST197Q02HA| ST215Q02HA| ST216Q02HA| ST218Q02HA| ST214Q02HA| ST220Q02HA| ST217Q02HA| ST219Q02HA| ST204Q02HA| ST177Q02HA| ST221Q02HA| ST223Q02HA| ST123Q02NA| ST205Q02HA| ST059Q02TA| ST062Q02TA| ST207Q02HA| ST206Q02HA| IC001Q02TA| IC009Q02TA| IC002Q01HA| IC150Q02HA| IC151Q02HA| IC152Q02HA| IC008Q02TA| IC010Q02NA| IC011Q02TA| IC015Q02NA| IC016Q02NA|
|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|
|          2|          2|          2|          2|          3|          2|          3|          2|          2|          2|          3|          2|          2|          1|          1|          4|          4|          2|          2|          2|          5|          0|          4|          1|          1|          3|          5|          4|          3|          3|          2|          3|          2|          3|          1|          2|          1|          1|          4|          1|          1|          2|          4|          4|          6|          2|          4|          4|          3|          3|          5|          1|          1|          1|          1|          1|          1|          4|          3|
|          2|          3|          2|          3|          2|          2|          2|          2|          2|          1|          1|          1|          1|          4|          4|          5|          3|          3|          5|          6|          6|          0|          4|          4|          2|          4|          5|          3|          4|          3|          3|          1|          2|          4|          4|          2|          1|          3|          3|          1|          1|          2|          4|          3|          6|          1|          3|          3|          3|          3|          3|          4|          4|          1|          5|          3|          1|          4|          4|
|          3|          2|          2|          2|          3|          3|          2|          2|          2|          3|          1|          2|          2|          3|          1|          2|          2|          1|          6|          5|          6|          0|          3|          3|          3|          2|          3|          2|          2|          1|          3|          3|          3|          3|          3|          2|          2|          3|          3|          1|          1|          2|          3|          3|          5|          1|          3|          2|          3|          3|          5|          2|          2|          4|          1|          1|          1|          2|          2|
|          2|          2|          2|          3|          4|          3|          2|          2|          3|          2|          4|          1|          2|          1|          1|          2|          2|          2|          1|          1|          1|          0|          4|          1|          1|          1|          2|          2|          2|          1|          3|          3|          2|          2|          1|          1|          3|          3|          2|          1|          1|          1|          3|          2|          6|          2|          1|          2|          1|          1|          1|          3|          1|          4|          1|          1|          2|          1|          2|
|          3|          3|          3|          1|          2|          2|          2|          1|          3|          1|          1|          2|          2|          4|          1|          5|          4|          1|          6|          6|          5|          0|          4|          4|          3|          1|          2|          3|          1|          1|          3|          3|          3|          4|          1|          2|          3|          2|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          1|          3|          5|          1|          1|          4|          5|          5|          3|          4|          4|
|          3|          3|          3|          3|          3|          3|          3|          2|          3|          2|          2|          1|          2|          3|          3|          5|          3|          2|          2|          4|          4|          1|          3|          2|          2|          2|          3|          4|          2|          1|          1|          2|          2|          3|          2|          2|          3|          3|          3|          1|          1|          2|          3|          2|          5|          2|          3|          2|          1|          2|          3|          1|          3|          4|          2|          2|          3|          3|          3|

</div>


### **num_range()**

-  ardışık ilerleyen değişkenlerin seçilmesi


```r
select(PISA_OGR_2018,num_range("AGIRLIKLANDIRMA",1:5)) %>% head(6)
```

<div class="kable-table">

| AGIRLIKLANDIRMA1| AGIRLIKLANDIRMA2| AGIRLIKLANDIRMA3| AGIRLIKLANDIRMA4| AGIRLIKLANDIRMA5|
|----------------:|----------------:|----------------:|----------------:|----------------:|
|          71.0286|         213.0858|          71.0286|         213.0858|          71.0286|
|          71.0286|         213.0858|          71.0286|         213.0858|          71.0286|
|          71.0286|         213.0858|          71.0286|         213.0858|          71.0286|
|          71.0286|         213.0858|          71.0286|         213.0858|          71.0286|
|          71.0286|         213.0858|          71.0286|         213.0858|          71.0286|
|          71.0286|         213.0858|          71.0286|         213.0858|          71.0286|

</div>


###  Matıksal operatorler ile seçim

- farklı fonksiyonları aynı anda mantıksal operatörlerle kullanarak da seçim yapabilirsiniz.

- veya **|** operatorünün kullanılması


```r
select(PISA_OGR_2018,contains("OKUMA") | matches("2")) %>% head(6)
```

<div class="kable-table">

| OKUMA_BAGLILIGI| OKUMA_ZEVK| ODOKUMA1| ODOKUMA2| ODOKUMA3| ODOKUMA4| ODOKUMA5| ODOKUMA6| ODOKUMA7| ODOKUMA8| ODOKUMA9| ODOKUMA10| ST097Q02TA| ST100Q02TA| ST102Q01TA| ST102Q02TA| ST102Q03TA| ST102Q04TA| ST211Q01HA| ST211Q02HA| ST211Q03HA| ST212Q01HA| ST212Q02HA| ST212Q03HA| ST104Q02NA| ST213Q01HA| ST213Q02HA| ST213Q03HA| ST213Q04HA| ST150Q02IA| ST152Q05IA| ST152Q06IA| ST152Q07IA| ST152Q08IA| ST153Q02HA| ST158Q02HA| ST160Q02IA| ST167Q02IA| ST176Q02IA| ST161Q02HA| ST163Q02HA| ST164Q02IA| ST165Q02IA| ST166Q02HA| ST225Q01HA| ST225Q02HA| ST225Q03HA| ST225Q05HA| ST225Q06HA| ST181Q02HA| ST182Q03HA| ST182Q04HA| ST182Q05HA| ST182Q06HA| ST183Q02HA| ST185Q02HA| ST186Q02HA| ST208Q01HA| ST208Q02HA| ST208Q04HA| ST188Q02HA| ST034Q02TA| ST196Q02HA| ST197Q02HA| ST197Q12HA| ST215Q01HA| ST215Q02HA| ST215Q03HA| ST215Q04HA| ST215Q05HA| ST216Q01HA| ST216Q02HA| ST216Q03HA| ST216Q04HA| ST216Q05HA| ST216Q06HA| ST218Q01HA| ST218Q02HA| ST218Q03HA| ST218Q04HA| ST218Q05HA| ST218Q06HA| ST218Q07HA| ST222Q01HA| ST222Q03HA| ST222Q04HA| ST222Q05HA| ST222Q06HA| ST222Q08HA| ST222Q09HA| ST222Q10HA| ST214Q01HA| ST214Q02HA| ST214Q03HA| ST214Q06HA| ST220Q01HA| ST220Q02HA| ST220Q03HA| ST220Q04HA| ST217Q01HA| ST217Q02HA| ST217Q03HA| ST217Q04HA| ST217Q05HA| ST219Q01HA| ST219Q02HA| ST219Q03HA| ST219Q04HA| ST219Q05HA| ST219Q06HA| ST204Q02HA| ST204Q03HA| ST204Q04HA| ST204Q05HA| ST177Q02HA| ST221Q01HA| ST221Q02HA| ST221Q03HA| ST221Q04HA| ST221Q05HA| ST221Q06HA| ST221Q07HA| ST221Q08HA| ST221Q09HA| ST221Q11HA| ST223Q02HA| ST223Q04HA| ST223Q05HA| ST223Q08HA| ST123Q02NA| ST123Q03NA| ST123Q04NA| ST205Q01HA| ST205Q02HA| ST205Q03HA| ST205Q04HA| ST059Q02TA| ST062Q01TA| ST062Q02TA| ST062Q03TA| ST207Q01HA| ST207Q02HA| ST207Q03HA| ST207Q04HA| ST207Q05HA| ST206Q01HA| ST206Q02HA| ST206Q03HA| ST206Q04HA| IC001Q02TA| IC009Q02TA| IC002Q01HA| IC150Q02HA| IC151Q02HA| IC152Q01HA| IC152Q02HA| IC152Q03HA| IC152Q04HA| IC152Q05HA| IC152Q06HA| IC152Q07HA| IC152Q08HA| IC152Q09HA| IC008Q02TA| IC008Q12TA| IC010Q02NA| IC010Q12HA| IC011Q02TA| IC013Q12NA| IC015Q02NA| IC016Q02NA| EFFORT2|OCOD2 | BFMJ2| AGIRLIKLANDIRMA2| AGIRLIKLANDIRMA12| AGIRLIKLANDIRMA20| AGIRLIKLANDIRMA21| AGIRLIKLANDIRMA22| AGIRLIKLANDIRMA23| AGIRLIKLANDIRMA24| AGIRLIKLANDIRMA25| AGIRLIKLANDIRMA26| AGIRLIKLANDIRMA27| AGIRLIKLANDIRMA28| AGIRLIKLANDIRMA29| AGIRLIKLANDIRMA32| AGIRLIKLANDIRMA42| AGIRLIKLANDIRMA52| AGIRLIKLANDIRMA62| AGIRLIKLANDIRMA72|  ODMAT2|  ODFEN2| PV2RCLI| PV2RCUN| PV2RCER| PV2RTSN| PV2RTML|
|---------------:|----------:|--------:|--------:|--------:|--------:|--------:|--------:|--------:|--------:|--------:|---------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|-------:|:-----|-----:|----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|
|         -0.9225|    -0.2891|  376.022|  417.746|  420.630|  413.837|  434.434|  424.054|  470.450|  446.634|  440.164|   443.152|          2|          2|          2|          2|          3|          2|          2|          3|          3|          3|          2|          2|          2|          2|          2|          2|          2|          3|          2|          1|          2|          2|          2|          2|          1|          1|          4|          4|          2|          2|          2|          5|          0|          0|          0|          0|          1|          4|          4|          4|          4|          3|          1|          1|          3|         NA|          5|          5|          4|          3|          3|          2|          3|          4|          3|          3|          4|          5|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|         NA|          3|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|         NA|          1|          1|          1|          2|          2|          2|          2|          4|          4|          4|          4|          4|          4|          4|          6|          2|          2|          3|          4|          4|          4|          4|          4|          4|          4|          4|          4|          3|          3|          5|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          4|          4|          3|      10|6111  | 11.56|         213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286| 477.281| 427.972| 436.019| 469.127| 465.273| 443.435| 440.472|
|          1.0741|     0.6040|  512.316|  473.229|  563.902|  485.396|  500.394|  495.048|  477.050|  526.291|  523.062|   481.411|          2|          3|          2|          3|          2|          2|          3|          2|          1|          4|          2|          2|          2|          1|          1|          2|          2|          1|          3|          4|          3|          4|          1|          1|          4|          4|          5|          3|          3|          5|          6|          6|          0|          0|          0|          0|          1|          4|          3|          4|          3|          3|          4|          2|          4|          4|          5|          4|          3|          4|          3|          3|          2|          1|          1|          1|          3|          4|          2|          2|          1|          4|          2|          3|          3|          4|          3|          4|          2|          3|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          3|          2|          2|          2|          2|          1|          1|          1|          1|          1|          2|          4|          3|          4|          4|          3|          4|          3|          1|          3|          2|          1|          1|          1|          2|          2|          2|          1|          1|          2|          1|          1|          2|          3|          3|          3|          4|          3|          1|          3|          3|          3|          4|          6|          1|          1|          3|          2|          3|          3|          3|          3|          2|          3|          2|          1|          3|          3|          3|          4|          4|          1|          1|          1|          1|          4|          5|          3|          5|          1|          5|          1|          3|          4|          1|          4|          4|          4|      10|7531  | 23.47|         213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286| 529.618| 555.509| 502.597| 536.260| 532.476| 521.353| 528.225|
|         -0.6200|     0.6380|  396.383|  413.859|  423.121|  452.124|  392.434|  433.205|  387.037|  406.997|  402.509|   438.667|          3|          2|          2|          2|          3|          3|          3|          2|          2|          2|          2|          1|          2|          2|          3|          3|          3|          1|          2|          2|          2|          2|          2|          2|          3|          1|          2|          2|          1|          6|          5|          6|          0|          0|          0|          0|          1|          3|          3|          3|          3|          3|          3|          3|          2|          3|          3|          3|          2|          2|          1|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          3|          3|          3|          3|          2|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          1|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          5|          1|          1|          1|          3|          3|          3|          3|          3|          2|          2|          2|          2|          3|          3|          5|          2|          2|          4|          4|          4|          4|          4|          4|          4|          4|          4|          1|          1|          1|          1|          1|          2|          2|          2|       9|6111  | 11.56|         213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286| 410.058| 399.453| 390.350| 485.928| 435.867| 460.715| 427.410|
|         -0.6200|    -1.1538|  393.006|  428.757|  364.850|  382.522|  378.563|  416.048|  395.846|  383.782|  374.509|   381.877|          2|          2|          2|          3|          4|          3|          3|          2|          2|          2|          2|          2|          3|          2|          2|          2|          2|          4|          2|          2|          2|          2|          1|          2|          1|          1|          2|          2|          2|          1|          1|          1|          0|          0|          0|          0|          1|          4|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          1|          3|          3|          3|          3|          1|          3|          3|          1|          2|          1|          3|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|          1|          3|          2|          2|          1|          2|          1|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|         NA|          3|          2|          2|          2|          2|          6|          2|          2|          2|          1|          1|          2|          2|          3|          2|          2|          2|          2|          1|          1|          1|          3|          1|          4|          4|          4|          4|          4|          4|          4|          4|          4|          1|          2|          1|          2|          2|          1|          1|          2|      10|2330  | 82.41|         213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286| 486.246| 431.478| 346.106| 387.692| 356.020| 390.744| 416.115|
|          0.3780|     0.6669|  552.457|  570.109|  562.955|  530.835|  532.487|  521.763|  481.840|  540.839|  471.671|   519.829|          3|          3|          3|          1|          2|          2|          3|          2|          2|          1|          1|          3|          3|          1|          1|          1|          1|          1|          4|          3|          2|          3|          2|          2|          4|          1|          5|          4|          1|          6|          6|          5|          0|          0|          1|          0|          1|          4|          3|          2|          4|          3|          4|          3|          1|          2|          2|          2|          3|          1|          1|          3|          3|          4|          3|          3|          1|          2|          1|          3|          4|          1|          1|          1|          1|          4|          3|          2|          2|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          1|          3|          3|          3|          3|          3|          2|          2|          2|          3|          4|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          2|          2|          1|          2|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          1|          3|          5|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          4|          5|          5|          5|          5|          3|          4|          4|          4|       8|3359  | 64.40|         213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286| 551.896| 539.614| 468.250| 473.691| 506.400| 506.118| 517.907|
|         -0.6200|     0.3568|  441.286|  415.682|  406.586|  437.001|  473.036|  416.363|  427.909|  471.902|  419.949|   439.851|          3|          3|          3|          3|          3|          3|          2|          3|          3|          1|          2|          1|          3|          2|          2|          3|          3|          2|          2|          2|          2|          2|          1|          2|          3|          3|          5|          3|          2|          2|          4|          4|          1|          1|          1|          0|          1|          3|          2|          3|          4|          3|          2|          2|          2|          2|          3|          2|          4|          2|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          1|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          2|          1|          2|          1|          2|          2|          2|          1|          2|          2|          2|          2|          2|          2|          3|          3|          3|          2|          2|          2|          2|          5|          2|          2|          2|          3|          3|          3|          3|          3|          2|          2|          2|          2|          1|          2|          3|          1|          3|          4|          4|          4|          4|          4|          4|          4|          4|          4|          2|          2|          2|          2|          3|          2|          3|          3|      10|2149  | 78.69|         213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286| 448.120| 440.738| 376.670| 457.365| 444.392| 434.123| 486.874|

</div>


- ve **&** operatorunun kullanılması


```r
select(PISA_OGR_2018,contains("OKUMA") & matches("2")) %>% head(6)
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
select(PISA_OGR_2018,-contains("OKUMA"),-matches("02"))  %>% head(5)
```

<div class="kable-table">

|   OKULID| OGRENCIID|OKUL_TUR | KITAPCIK| SINIF| DOGUMAY| CINSIYET| ANNE_OKUL| ANNE_LISANSUSTU| ANNE_LISANS| ANNE_ONLISANS| BABA_OKUL| BABA_LISANSUSTU| BABA_LISANS| BABA_ONLISANS| OLANAK_MASA| OLANAK_ODA| OLANAK_SESSIZYER| OLANAK_BILGISAYAR| OLANAK_YAZILIM| OLANAK_INTERNET| OLANAK_KLASIKKITAP| OLANAK_SIIRKITAP| OLANAK_SANATESER| OLANAK_KAYNAKKITAP| OLANAK_TEKNIKKITAP| OLANAK_SOZLUK| OLANAK_SANATKITAP|OLANAK_KLIMA |OLANAK_TVABONE |OLANAK_TATIL | MIKTAR_TV| MIKTAR_ARABA| MIKTAR_BANYO| MIKTAR_AKILLITEL| MIKTAR_BILGISAYAR| MIKTAR_TABLET| MIKTAR_EKITAPOKUYUCU| MIKTAR_MUZIKALET| KITAPSAYISI| DOGUMULKE_OGR| DOGUMULKE_ANNE| DOGUMULKE_BABA| TR_GELIS_YAS| BASLAMA_YAS_OKULONCESI| BASLAMA_YAS_ILKOKUL| SINIFTEKRARI_ILKOKUL| SINIFTEKRARI_ORTAOKUL| SINIFTEKRARI_LISE| EV_KONUSULAN_DIL| ANNE_KONUSULAN_DIL| BABA_KONUSULAN_DIL| KARDES_KONUSULAN_DIL| YARKADAS_KONUSULAN_DIL| OARKADAS_KONUSULAN_DIL| ST097Q01TA| ST097Q03TA| ST097Q04TA| ST097Q05TA| ST100Q01TA| ST100Q03TA| ST100Q04TA| ST211Q01HA| ST211Q03HA| ST212Q01HA| ST212Q03HA| ST104Q03NA| ST104Q04NA| ST213Q01HA| ST213Q03HA| ST213Q04HA| ST150Q01IA| ST150Q03IA| ST150Q04HA| ST152Q05IA| ST152Q06IA| ST152Q07IA| ST152Q08IA| ST154Q01HA| ST153Q01HA| ST153Q03HA| ST153Q04HA| ST153Q05HA| ST153Q06HA| ST153Q08HA| ST153Q09HA| ST153Q10HA| ST158Q01HA| ST158Q03HA| ST158Q04HA| ST158Q05HA| ST158Q06HA| ST158Q07HA| ST160Q01IA| ST160Q03IA| ST160Q04IA| ST160Q05IA| ST167Q01IA| ST167Q03IA| ST167Q04IA| ST167Q05IA| ST168Q01HA| ST175Q01IA| ST176Q01IA| ST176Q03IA| ST176Q05IA| ST176Q06IA| ST176Q07IA| ST161Q01HA| ST161Q03HA| ST161Q06HA| ST161Q07HA| ST161Q08HA| ST163Q03HA| ST163Q04HA| ST164Q01IA| ST164Q03IA| ST164Q04IA| ST164Q05IA| ST164Q06IA| ST165Q01IA| ST165Q03IA| ST165Q04IA| ST165Q05IA| ST166Q01HA| ST166Q03HA| ST166Q04HA| ST166Q05HA| ST016Q01NA| ST036Q05TA| ST036Q06TA| ST036Q08TA| ST225Q01HA| ST225Q03HA| ST225Q05HA| ST225Q06HA| ST181Q03HA| ST181Q04HA| ST182Q03HA| ST182Q04HA| ST182Q05HA| ST182Q06HA| ST183Q01HA| ST183Q03HA| ST184Q01HA| ST185Q01HA| ST185Q03HA| ST186Q05HA| ST186Q06HA| ST186Q07HA| ST186Q10HA| ST186Q09HA| ST186Q01HA| ST186Q08HA| ST186Q03HA| ST208Q01HA| ST208Q04HA| ST188Q01HA| ST188Q03HA| ST188Q06HA| ST188Q07HA| ST034Q01TA| ST034Q03TA| ST034Q04TA| ST034Q05TA| ST034Q06TA| ST196Q03HA| ST196Q04HA| ST196Q05HA| ST196Q06HA| ST196Q07HA| ST197Q01HA| ST197Q04HA| ST197Q07HA| ST197Q08HA| ST197Q09HA| ST197Q12HA| ST215Q01HA| ST215Q03HA| ST215Q04HA| ST215Q05HA| ST216Q01HA| ST216Q03HA| ST216Q04HA| ST216Q05HA| ST216Q06HA| ST218Q01HA| ST218Q03HA| ST218Q04HA| ST218Q05HA| ST218Q06HA| ST218Q07HA| ST222Q01HA| ST222Q03HA| ST222Q04HA| ST222Q05HA| ST222Q06HA| ST222Q08HA| ST222Q09HA| ST222Q10HA| ST214Q01HA| ST214Q03HA| ST214Q06HA| ST220Q01HA| ST220Q03HA| ST220Q04HA| ST217Q01HA| ST217Q03HA| ST217Q04HA| ST217Q05HA| ST219Q01HA| ST219Q03HA| ST219Q04HA| ST219Q05HA| ST219Q06HA| ST204Q03HA| ST204Q04HA| ST204Q05HA| ST177Q01HA| ST177Q03HA| ST189Q01HA| ST221Q01HA| ST221Q03HA| ST221Q04HA| ST221Q05HA| ST221Q06HA| ST221Q07HA| ST221Q08HA| ST221Q09HA| ST221Q11HA| ST223Q04HA| ST223Q05HA| ST223Q08HA| ST123Q03NA| ST123Q04NA| ST205Q01HA| ST205Q03HA| ST205Q04HA| ST059Q01TA| ST059Q03TA| ST059Q04HA| ST060Q01NA| ST061Q01NA| ST062Q01TA| ST062Q03TA| ST038Q03NA| ST038Q04NA| ST038Q05NA| ST038Q06NA| ST038Q07NA| ST038Q08NA| ST207Q01HA| ST207Q03HA| ST207Q04HA| ST207Q05HA| ST206Q01HA| ST206Q03HA| ST206Q04HA| IC001Q01TA| IC001Q03TA| IC001Q04TA| IC001Q05TA| IC001Q06TA| IC001Q07TA| IC001Q08TA| IC001Q09TA| IC001Q10TA| IC001Q11TA| IC009Q01TA| IC009Q03TA| IC009Q05NA| IC009Q06NA| IC009Q07NA| IC009Q08TA| IC009Q09TA| IC009Q10NA| IC009Q11NA| IC004Q01HA| IC005Q01TA| IC006Q01TA| IC007Q01TA| IC150Q01HA| IC150Q03HA| IC150Q04HA| IC150Q05HA| IC150Q06HA| IC150Q07HA| IC150Q08HA| IC150Q09HA| IC151Q01HA| IC151Q03HA| IC151Q04HA| IC151Q05HA| IC151Q06HA| IC151Q07HA| IC151Q08HA| IC151Q09HA| IC152Q01HA| IC152Q03HA| IC152Q04HA| IC152Q05HA| IC152Q06HA| IC152Q07HA| IC152Q08HA| IC152Q09HA| IC008Q01TA| IC008Q03TA| IC008Q04TA| IC008Q05TA| IC008Q07NA| IC008Q08TA| IC008Q09TA| IC008Q10TA| IC008Q11TA| IC008Q12TA| IC008Q13NA| IC010Q01TA| IC010Q03TA| IC010Q04TA| IC010Q05NA| IC010Q06NA| IC010Q07TA| IC010Q08TA| IC010Q09NA| IC010Q10NA| IC010Q11HA| IC010Q12HA| IC011Q01TA| IC011Q03TA| IC011Q04TA| IC011Q05TA| IC011Q06TA| IC011Q07TA| IC011Q08TA| IC011Q09TA| IC011Q10HA| IC013Q01NA| IC013Q04NA| IC013Q05NA| IC013Q11NA| IC013Q12NA| IC013Q13NA| IC014Q03NA| IC014Q04NA| IC014Q06NA| IC014Q08NA| IC014Q09NA| IC015Q03NA| IC015Q05NA| IC015Q07NA| IC015Q09NA| IC016Q01NA| IC016Q04NA| IC016Q05NA| IC016Q07NA| IC169Q01HA| caba| EFFORT2|OCOD1 |OCOD2 |OCOD3 | Sinif_Duzey|   Yas|Program  |COBN_S |COBN_M |COBN_F | LANGN| ISCEDL| ISCEDD| ISCEDO| Anne_Egitim| Baba_Egitim| Ebeveyn_egitimi| PARED| Anne_Egitim_D| Baba_Egitim_D| Ebeveyn_egitimi_D| PAREDINT| BMMJ1| BFMJ2| HISEI| Anne_DIL| Baba_DIL| Kardes_DIL| Arkadas_DIL| O_Arkadas_DIL| Gocmenlik| Okuloncesi_yil| Sinif_tekrari| Beklenen_Mesleki_Statu| Ogrenme_zamani_mat| Ogrenme_zamani_turkce| Ogrenme_zamani_fen| Ogrenme_zamani_toplam|     SES| MC_Anlama_Hatirlama| MC_Ozetleme| MC_Degerlendirme| BIT_EV| BIT_OKL| EVSEL_ESYA| KULTUREL_KAYNAK| EGITIMSEL_KAYNAK| ZENGINLIK| BIT_KAYNAK| DISIPLIN| OGR_DESTEK| OGR_YONLENDIRME| GERI_BILDIRIM| DUYGUSAL_DESTEK| TALIMAT_UYAR| OGR_ILGISI| OK_YETERLIK| OK_ZORLUK| ALGILANAN_PISA_ZORLUK| ALGILANAN_REKABET| ALGILANAN_ISBIRLIGI| OKUL_TUTUM| REKABET| USTALIK| BASARISIZLIK_KORKUSU|   EUDMO| IYI_OLUS| DAYANIKLIK| MASTGOAL| KURSOR_OZYET| KURSOR_FARKINDALIK| GOCMENLIK_TUTUM| KULTURLERE_ILGI| BAKIS_ACISI| BILISSEL_ESNEKLIK| KULTURLERE_SAYGI| ILETISIM_FARKINDALIK| KURESEL_FIKIR| AYRIMCI_IKLIM| AIDIYET| ZORBALIK| BIT_BOSZAMAN| BIT_OKULDISI| BIT_OKUL| BIT_ILGI| BIT_YET| BIT_OZERK| BIT_SOSYAL| BIT_DERS| BIT_DERSDISI| W_FSTUWT| AGIRLIKLANDIRMA1| AGIRLIKLANDIRMA2| AGIRLIKLANDIRMA3| AGIRLIKLANDIRMA4| AGIRLIKLANDIRMA5| AGIRLIKLANDIRMA6| AGIRLIKLANDIRMA7| AGIRLIKLANDIRMA8| AGIRLIKLANDIRMA9| AGIRLIKLANDIRMA10| AGIRLIKLANDIRMA11| AGIRLIKLANDIRMA12| AGIRLIKLANDIRMA13| AGIRLIKLANDIRMA14| AGIRLIKLANDIRMA15| AGIRLIKLANDIRMA16| AGIRLIKLANDIRMA17| AGIRLIKLANDIRMA18| AGIRLIKLANDIRMA19| AGIRLIKLANDIRMA20| AGIRLIKLANDIRMA21| AGIRLIKLANDIRMA22| AGIRLIKLANDIRMA23| AGIRLIKLANDIRMA24| AGIRLIKLANDIRMA25| AGIRLIKLANDIRMA26| AGIRLIKLANDIRMA27| AGIRLIKLANDIRMA28| AGIRLIKLANDIRMA29| AGIRLIKLANDIRMA30| AGIRLIKLANDIRMA31| AGIRLIKLANDIRMA32| AGIRLIKLANDIRMA33| AGIRLIKLANDIRMA34| AGIRLIKLANDIRMA35| AGIRLIKLANDIRMA36| AGIRLIKLANDIRMA37| AGIRLIKLANDIRMA38| AGIRLIKLANDIRMA39| AGIRLIKLANDIRMA40| AGIRLIKLANDIRMA41| AGIRLIKLANDIRMA42| AGIRLIKLANDIRMA43| AGIRLIKLANDIRMA44| AGIRLIKLANDIRMA45| AGIRLIKLANDIRMA46| AGIRLIKLANDIRMA47| AGIRLIKLANDIRMA48| AGIRLIKLANDIRMA49| AGIRLIKLANDIRMA50| AGIRLIKLANDIRMA51| AGIRLIKLANDIRMA52| AGIRLIKLANDIRMA53| AGIRLIKLANDIRMA54| AGIRLIKLANDIRMA55| AGIRLIKLANDIRMA56| AGIRLIKLANDIRMA57| AGIRLIKLANDIRMA58| AGIRLIKLANDIRMA59| AGIRLIKLANDIRMA60| AGIRLIKLANDIRMA61| AGIRLIKLANDIRMA62| AGIRLIKLANDIRMA63| AGIRLIKLANDIRMA64| AGIRLIKLANDIRMA65| AGIRLIKLANDIRMA66| AGIRLIKLANDIRMA67| AGIRLIKLANDIRMA68| AGIRLIKLANDIRMA69| AGIRLIKLANDIRMA70| AGIRLIKLANDIRMA71| AGIRLIKLANDIRMA72| AGIRLIKLANDIRMA73| AGIRLIKLANDIRMA74| AGIRLIKLANDIRMA75| AGIRLIKLANDIRMA76| AGIRLIKLANDIRMA77| AGIRLIKLANDIRMA78| AGIRLIKLANDIRMA79| AGIRLIKLANDIRMA80| UNIT| WVARSTRR|  ODMAT1|  ODMAT2|  ODMAT3|  ODMAT4|  ODMAT5|  ODMAT6|  ODMAT7|  ODMAT8|  ODMAT9| ODMAT10|  ODFEN1|  ODFEN2|  ODFEN3|  ODFEN4|  ODFEN5|  ODFEN6|  ODFEN7|  ODFEN8|  ODFEN9| ODFEN10| PV1RCLI| PV2RCLI| PV3RCLI| PV4RCLI| PV5RCLI| PV6RCLI| PV7RCLI| PV8RCLI| PV9RCLI| PV10RCLI| PV1RCUN| PV2RCUN| PV3RCUN| PV4RCUN| PV5RCUN| PV6RCUN| PV7RCUN| PV8RCUN| PV9RCUN| PV10RCUN| PV1RCER| PV2RCER| PV3RCER| PV4RCER| PV5RCER| PV6RCER| PV7RCER| PV8RCER| PV9RCER| PV10RCER| PV1RTSN| PV2RTSN| PV3RTSN| PV4RTSN| PV5RTSN| PV6RTSN| PV7RTSN| PV8RTSN| PV9RTSN| PV10RTSN| PV1RTML| PV2RTML| PV3RTML| PV4RTML| PV5RTML| PV6RTML| PV7RTML| PV8RTML| PV9RTML| PV10RTML|   SENWT|VER_DAT          |
|--------:|---------:|:--------|--------:|-----:|-------:|--------:|---------:|---------------:|-----------:|-------------:|---------:|---------------:|-----------:|-------------:|-----------:|----------:|----------------:|-----------------:|--------------:|---------------:|------------------:|----------------:|----------------:|------------------:|------------------:|-------------:|-----------------:|:------------|:--------------|:------------|---------:|------------:|------------:|----------------:|-----------------:|-------------:|--------------------:|----------------:|-----------:|-------------:|--------------:|--------------:|------------:|----------------------:|-------------------:|--------------------:|---------------------:|-----------------:|----------------:|------------------:|------------------:|--------------------:|----------------------:|----------------------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----:|-------:|:-----|:-----|:-----|-----------:|-----:|:--------|:------|:------|:------|-----:|------:|------:|------:|-----------:|-----------:|---------------:|-----:|-------------:|-------------:|-----------------:|--------:|-----:|-----:|-----:|--------:|--------:|----------:|-----------:|-------------:|---------:|--------------:|-------------:|----------------------:|------------------:|---------------------:|------------------:|---------------------:|-------:|-------------------:|-----------:|----------------:|------:|-------:|----------:|---------------:|----------------:|---------:|----------:|--------:|----------:|---------------:|-------------:|---------------:|------------:|----------:|-----------:|---------:|---------------------:|-----------------:|-------------------:|----------:|-------:|-------:|--------------------:|-------:|--------:|----------:|--------:|------------:|------------------:|---------------:|---------------:|-----------:|-----------------:|----------------:|--------------------:|-------------:|-------------:|-------:|--------:|------------:|------------:|--------:|--------:|-------:|---------:|----------:|--------:|------------:|--------:|----------------:|----------------:|----------------:|----------------:|----------------:|----------------:|----------------:|----------------:|----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|-----------------:|----:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|:----------------|
| 79200001|  79200768|TUR0112  |       20|    10|      10|        2|         3|               2|           2|             2|         3|               2|           2|             2|           1|          1|                1|                 2|              2|               2|                  1|                1|                2|                  1|                  2|             1|                 2|0792002      |0792002        |0792002      |         2|            1|            2|                2|                 1|             2|                    1|                3|           2|             1|              1|              1|           NA|                      6|                   5|                    1|                     1|                 1|                1|                  4|                  4|                    4|                      4|                      4|          1|          1|          1|          1|          2|          2|          3|          2|          3|          3|          2|          2|          2|          2|          2|          2|          3|          3|          4|          2|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          2|          1|          2|          1|          1|          2|          2|          4|          3|          2|          1|          1|          2|          1|          1|          1|         NA|          3|          4|          5|          2|          4|          1|          3|          2|          2|          2|          2|          2|          3|          1|          1|          3|          1|          1|          1|          1|          1|          5|          3|          1|          6|         NA|          1|          1|          2|          0|          0|          0|          1|          4|          4|          4|          4|          4|          3|          4|          1|          1|          4|          2|          2|          1|          2|          1|          3|          3|          3|          3|         NA|          5|          4|          4|          4|          4|          3|          3|          3|          3|          3|          3|          4|          4|          3|          4|          3|          3|          3|          3|          3|          3|          4|          3|          4|          5|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          2|         NA|          3|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          1|          1|          2|          1|          1|          1|          1|          1|         NA|          1|          1|          1|          2|          2|          2|          4|          4|          4|          4|          4|          5|          7|          6|         NA|         NA|          2|          3|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          3|          2|          3|          3|          1|          1|          2|          3|          3|          3|          2|          3|          2|          2|          2|          2|          2|          2|          1|          4|          1|          5|          7|          1|          3|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          3|          4|          1|          4|          3|          4|          2|          1|          2|          1|          1|          1|          2|          1|          1|          1|          1|          5|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          2|          4|          4|          3|          3|          3|          3|          3|          4|          4|          4|          4|          3|          3|          3|          3|          2|   10|      10|9701  |6111  |9704  |           0| 15.50|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|           2|           2|               2|     8|             2|             2|                 2|        9| 17.00| 11.56| 17.00|       NA|       NA|         NA|          NA|            NA|         1|              1|             0|                     NA|                 NA|                    NA|                 NA|                    NA| -2.4521|               -0.94|       -1.72|            -0.04|      4|       8|    -2.3750|         -0.5921|          -1.3835|   -2.8866|    -2.4931|  -1.9119|    -0.3971|         -0.2546|       -0.3253|          1.0346|      -0.1716|    -1.0615|     -0.6712|   -0.0697|                0.2705|            2.0378|              1.6762|     0.4626|  2.0054|  1.8164|              -1.1090| -0.8382|  -1.1889|     2.3693|       NA|       0.9683|            -0.2736|          1.4992|          0.1208|     -1.2292|            0.2165|           0.9289|              -0.1577|       -2.8778|        0.5881| -0.6659|  -0.7823|      -0.5131|      -0.3817|  -1.7161|   1.0435|  0.0537|    2.0258|     0.5149|   0.0390|      -1.3048| 142.0572|          71.0286|         213.0858|          71.0286|         213.0858|          71.0286|          71.0286|          71.0286|          71.0286|         213.0858|          213.0858|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|    2|        3| 483.048| 477.281| 480.638| 494.293| 507.554| 522.458| 538.795| 402.822| 485.275| 540.275| 462.325| 427.972| 456.810| 434.988| 444.467| 457.415| 453.608| 447.165| 463.464| 463.425| 424.897| 436.019| 444.568| 449.735| 403.609| 458.672| 457.902| 452.226| 411.985|  451.702| 439.127| 469.127| 474.409| 484.051| 459.989| 492.256| 496.422| 483.753| 461.741|  436.576| 448.889| 465.273| 467.666| 513.751| 437.552| 546.952| 468.595| 465.507| 503.251|  469.400| 473.404| 443.435| 455.826| 487.585| 514.687| 468.640| 462.800| 473.295| 487.510|  460.414| 475.910| 440.472| 437.323| 465.047| 466.901| 418.813| 483.735| 445.559| 475.808|  462.321| 0.80261|02MAY19:09:49:49 |
| 79200001|  79201064|TUR0112  |        5|    10|       2|        2|         3|               2|           2|             2|         3|               2|           2|             2|           1|          2|                1|                 2|              2|               2|                  1|                1|                1|                  1|                  2|             1|                 2|0792001      |0792002        |0792002      |         2|            2|            2|                4|                 1|             1|                    1|                4|           3|             1|              1|              1|           NA|                      6|                   5|                    1|                     1|                 1|                1|                  4|                  4|                    4|                      4|                      4|          3|          3|          3|          3|          4|          3|          2|          3|          1|          4|          2|          2|          3|          1|          2|          2|          1|          1|          4|          3|          4|          3|          4|          5|          1|          2|          1|          1|          1|          1|          2|          2|          2|          2|          2|          1|          1|          1|          2|          3|          4|          2|          2|          5|          2|          5|          4|          3|          2|          5|          5|          5|          5|          4|          4|          2|          3|          1|          3|          4|          5|          2|          6|          2|          3|          6|          5|          6|          6|          2|          4|          1|          6|          7|          1|          1|          1|          0|          0|          0|          1|          4|          4|          3|          4|          3|          3|          4|          4|          2|          3|          1|          3|          1|          2|          2|          3|          3|          3|          2|          4|          4|          3|          1|          4|          4|          3|          2|          3|          3|          4|          3|          4|          4|          3|          2|          3|          4|          3|          4|          4|          2|          1|          1|          3|          4|          2|          1|          4|          2|          3|          3|          3|          4|          2|          3|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|          2|          2|          2|          1|          1|          1|          1|          2|          4|          4|          4|          3|          4|          1|          3|          2|          3|          1|          2|          1|          2|          2|          2|          1|          1|          2|          1|          1|          3|          3|          3|          3|          1|          3|          3|          4|          6|          6|          6|         60|         35|          1|          3|          4|          4|          2|          1|          2|          3|          2|          3|          3|          3|          2|          2|          1|          2|          3|          3|          3|          2|          1|          1|          3|          1|          3|          2|          3|          3|          3|          3|          1|          3|          3|          1|          4|          3|          4|          4|          4|          4|          4|          1|          5|          2|          5|          1|          1|          4|          1|          3|          5|          1|          5|          1|          1|          1|          1|          4|          5|          3|          5|          1|          5|          2|          5|          5|          1|          3|          4|          5|          4|          1|          2|          2|          1|          1|          4|          4|          2|          2|          2|          5|          5|          4|          4|          4|          2|          1|          1|          3|          2|          2|          4|          4|          3|          4|          4|          4|          4|          3|          4|          4|          4|          4|          4|          4|          4|          3|          4|          4|          4|          4|          3|    7|      10|9701  |7531  |2611  |           0| 16.17|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|           2|           2|               2|     8|             2|             2|                 2|        9| 17.00| 23.47| 23.47|       NA|       NA|         NA|          NA|            NA|         1|              1|             0|                  86.72|                210|                   210|                210|                  2100| -2.1042|               -0.60|       -0.95|             0.42|      5|       3|    -1.8443|          0.3624|          -1.3835|   -2.3397|    -2.3112|  -0.4003|    -1.1176|         -0.3733|        0.0728|         -1.0624|       0.1888|    -1.4401|      1.2374|   -0.1817|                1.9717|            0.6912|             -0.4213|     1.0844|  2.0054|  0.4870|               1.8905| -1.0946|  -1.1176|     0.1123|   1.1101|       0.4153|             0.6013|         -1.0478|         -0.1149|      1.0349|            0.3024|           0.9289|               0.4748|        1.3556|        1.5785| -0.3540|   2.4122|       0.2570|       0.5014|   0.4012|   1.3541|  1.4987|    1.3545|     2.3635|   1.2850|       0.9409| 142.0572|          71.0286|         213.0858|          71.0286|         213.0858|          71.0286|          71.0286|          71.0286|          71.0286|         213.0858|          213.0858|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|    2|        3| 541.139| 529.618| 516.712| 509.319| 543.800| 544.083| 537.209| 476.977| 519.471| 532.874| 536.046| 555.509| 553.832| 531.649| 528.851| 533.099| 499.113| 537.615| 549.746| 452.920| 480.514| 502.597| 479.291| 535.308| 429.311| 471.008| 458.337| 476.741| 506.172|  450.403| 519.885| 536.260| 506.943| 532.521| 462.051| 487.408| 497.342| 548.166| 530.531|  474.572| 559.394| 532.476| 545.079| 589.216| 482.084| 524.097| 498.018| 567.929| 499.327|  490.810| 447.791| 521.353| 502.951| 467.590| 451.939| 471.438| 480.654| 548.421| 496.817|  438.275| 500.916| 528.225| 517.816| 505.885| 477.363| 526.670| 521.478| 523.722| 494.396|  467.632| 0.80261|02MAY19:09:49:49 |
| 79200001|  79201118|TUR0112  |       16|    10|       1|        1|         4|               2|           2|             2|         3|               2|           2|             2|           2|          2|                2|                 2|              1|               2|                  1|                1|                1|                  1|                  1|             1|                 1|0792002      |0792001        |0792002      |         2|            3|            2|                4|                 1|             1|                    1|                1|           1|             1|              1|              1|           NA|                      6|                   5|                    1|                     1|                 1|                1|                  1|                  1|                    1|                      1|                      1|          2|          3|          3|          3|          2|          2|          3|          3|          2|          2|          1|          2|          2|          2|          3|          3|          2|          1|          2|          2|          2|          2|          2|          4|          1|          2|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          3|          2|          2|          1|          4|          4|          4|         NA|          5|          2|          2|          4|          2|          4|          3|          3|          2|          3|          3|          4|          1|          1|          2|          6|          6|          3|          6|          6|          6|          6|          1|          6|          6|          6|          4|          2|          2|          2|          0|          0|          0|          1|          3|          3|          3|          3|          3|          3|          3|          3|          1|          3|          3|          3|          3|          3|          1|          2|          3|          3|          3|          3|          3|          2|          2|          2|          2|          3|          2|          3|          2|          3|          2|          3|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          3|          3|          3|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          1|          2|          2|          2|          3|          3|          3|          3|          3|          4|          2|          2|         41|         70|          1|          1|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          2|          2|          2|          3|          3|          3|          3|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          5|          1|          3|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|          4|          4|          4|          4|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|    8|       9|9701  |6111  |2330  |           0| 16.25|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|           1|           2|               2|     8|             1|             2|                 2|        9| 17.00| 11.56| 17.00|       NA|       NA|         NA|          NA|            NA|         1|              1|             0|                  82.41|                350|                   280|                140|                  2870| -2.2700|                0.10|       -0.18|            -0.04|      3|       0|    -1.9449|          0.2154|          -1.5164|   -1.9453|    -2.0867|  -0.3031|    -0.3971|         -0.5072|       -0.3253|         -0.6576|      -0.9282|    -0.3689|     -0.4089|    0.9065|                0.8876|            0.6912|             -0.9391|    -0.6583|  0.1956| -0.1015|               0.4637|  0.2621|  -0.5928|    -1.4832|  -0.4347|      -0.9111|            -0.0549|         -0.2014|         -0.4982|     -0.8702|           -0.8312|          -0.4401|              -0.1577|        0.2910|        0.5881| -0.3184|   2.0700|      -3.5940|      -2.2971|  -1.7161|  -1.7210| -1.1888|   -1.1563|    -0.7345|   0.3701|       0.2858| 142.0572|          71.0286|         213.0858|          71.0286|         213.0858|          71.0286|          71.0286|          71.0286|          71.0286|         213.0858|          213.0858|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|    2|        3| 438.872| 410.058| 448.972| 509.320| 438.305| 437.978| 374.374| 394.238| 389.679| 406.201| 416.271| 399.453| 467.897| 481.931| 414.718| 412.110| 397.644| 408.578| 422.486| 431.633| 405.191| 390.350| 424.945| 452.030| 344.114| 440.066| 468.701| 486.608| 424.487|  446.807| 445.660| 485.928| 402.752| 495.788| 425.782| 475.268| 500.588| 487.242| 456.602|  468.181| 441.278| 435.867| 423.106| 449.796| 408.176| 468.193| 461.418| 481.248| 479.042|  447.929| 482.026| 460.715| 453.753| 475.813| 475.101| 429.407| 503.751| 457.465| 445.960|  461.785| 435.054| 427.410| 463.953| 450.673| 483.763| 435.906| 462.534| 464.111| 433.016|  474.589| 0.80261|02MAY19:09:49:49 |
| 79200001|  79201275|TUR0112  |       21|     9|       9|        2|         1|              NA|           1|            NA|         1|              NA|           1|            NA|           1|          1|                1|                 1|              2|               1|                  2|                2|                2|                  1|                  2|             1|                 2|0792001      |0792002        |0792002      |         3|            1|            1|                2|                 2|             1|                    1|                1|           1|             1|              1|              1|           NA|                      6|                   5|                    1|                     1|                 1|                1|                  4|                  4|                    4|                      4|                      4|          2|          3|          1|          1|          3|          1|          4|          3|          2|          2|          2|          2|          3|          2|          2|          2|          4|          4|          4|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          3|          1|          3|          3|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          2|          2|          1|          1|          6|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|          2|          2|          2|          0|          0|          0|          1|          3|          4|          1|          1|          1|          1|          1|          1|          3|          1|          1|          4|          2|          1|          1|          4|          2|          1|          2|          2|          2|          2|          2|          2|          2|          4|          3|          2|          2|          3|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          1|          3|          3|          1|          1|          3|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|          3|          2|          2|          2|          1|          2|          3|          3|          3|          3|          3|          3|          3|          3|          2|          2|          2|          1|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|         NA|          3|          2|          2|          2|          5|          6|          4|         40|         40|          2|          2|          2|          2|          2|          2|          2|          2|          1|          2|          2|          3|          2|          2|          2|          1|          1|          1|          1|          3|          1|          2|          1|          2|          3|          1|          1|          1|          2|          2|          2|          3|          2|          1|          2|          1|          5|          5|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|          4|          4|          1|   10|      10|2330  |2330  |2211  |          -1| 15.58|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|           6|           6|               6|    16|             6|             6|                 6|       16| 82.41| 82.41| 82.41|       NA|       NA|         NA|          NA|            NA|         1|              1|             0|                  88.70|                240|                   200|                240|                  1600|  0.0324|               -0.60|       -1.72|            -1.41|      9|       9|    -2.1008|         -2.7469|          -0.6853|   -2.1121|    -1.7005|  -1.1699|    -0.4060|         -1.0499|        0.2682|              NA|      -0.5786|    -1.0615|     -0.8250|    1.2421|                0.2705|           -0.6142|             -0.9391|    -0.6583|  1.1811| -2.7365|              -1.8939| -2.1464|  -1.2568|    -1.4832|  -1.3162|      -2.7142|            -0.0549|         -1.2083|         -0.2157|     -0.3405|            1.3823|          -1.2781|              -1.3933|        0.2910|       -1.1549| -0.4217|   1.1625|      -2.7049|      -0.5991|  -1.0707|  -2.9336| -2.6033|   -2.5144|     0.2639|   1.0418|      -1.3048| 142.0572|          71.0286|         213.0858|          71.0286|         213.0858|          71.0286|          71.0286|          71.0286|          71.0286|         213.0858|          213.0858|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|    2|        3| 417.314| 486.246| 419.767| 413.368| 508.158| 475.248| 527.383| 482.872| 477.418| 476.539| 402.112| 431.478| 384.063| 472.941| 420.800| 472.894| 460.407| 465.356| 439.954| 442.546| 377.648| 346.106| 347.468| 351.544| 464.958| 406.800| 305.063| 415.645| 451.572|  332.146| 418.336| 387.692| 376.644| 348.832| 469.856| 438.034| 377.209| 433.141| 463.976|  390.554| 370.646| 356.020| 346.501| 346.212| 425.656| 396.229| 416.122| 421.807| 457.353|  390.627| 419.099| 390.744| 410.400| 377.828| 443.815| 406.021| 393.957| 420.428| 398.023|  462.478| 400.889| 416.115| 426.449| 396.449| 425.235| 391.150| 373.368| 416.023| 417.897|  416.855| 0.80261|02MAY19:09:49:49 |
| 79200001|  79201481|TUR0112  |        1|     9|       9|        2|         1|              NA|          NA|            NA|         1|               2|           2|             2|           1|          1|                1|                 1|              1|               1|                  1|                2|                2|                  1|                  1|             1|                 2|0792001      |0792001        |0792001      |         3|            2|            3|                4|                 3|             3|                    1|                3|           2|             1|              1|              1|           NA|                      8|                   4|                    1|                     1|                 1|                1|                  4|                  4|                    4|                      4|                      4|          3|          4|          3|          1|          2|          1|          4|          3|          2|          1|          3|          2|          4|          1|          1|          1|          1|          4|          1|          4|          3|          2|          3|          5|          2|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          4|          4|          2|          4|          1|          5|          5|          5|          4|          3|          4|          5|          5|          5|          3|          4|          4|          2|          2|          2|          1|          1|          6|          6|          6|          6|          6|          6|          6|          6|          6|          5|          6|          1|          6|          1|          4|          1|          1|          0|          1|          0|          1|          4|          4|          3|          2|          4|          3|          4|          4|          3|          3|          3|          4|          4|          4|          4|          4|          1|          2|          3|          2|          2|          2|          2|          3|          2|          2|          1|          4|          1|          3|          4|          4|          1|          4|          4|          3|          4|          4|          3|          3|          3|          4|          3|          1|          2|          1|          4|          1|          1|          1|          1|          3|          2|          2|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|          3|          3|          3|          2|          2|          3|          4|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          2|          2|          2|          3|          3|          1|          1|          1|          1|          1|          3|          5|          2|         44|         40|          4|          4|          2|          2|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          1|          1|          1|          1|          3|          1|          3|          3|          1|          3|          1|          3|          1|          1|          1|         NA|          3|          3|          1|          4|          5|          5|          5|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          3|          3|          3|          3|          3|          3|          3|          3|          3|          4|          3|          4|          4|          4|          4|          2|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          2|    7|       8|4211  |3359  |0210  |          -1| 15.58|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|           4|           4|               4|    12|             4|             4|                 4|       12| 48.10| 64.40| 64.40|       NA|       NA|         NA|          NA|            NA|         1|             NA|             0|                  51.63|                 40|                   120|                200|                  1760| -0.0674|               -1.64|       -1.72|            -0.96|      7|       5|    -0.0107|         -1.2613|           1.1793|    0.0426|     0.0895|  -0.1926|    -0.4760|          0.0351|        0.5984|         -2.4468|      -1.1725|    -2.2177|      1.8839|   -0.0697|               -1.2720|           -1.9892|              1.6762|    -0.6036|  2.0054|  0.0273|               1.8905|  0.2621|  -1.4371|    -1.0586|  -1.3162|       0.2632|             0.4100|         -2.2640|          1.6052|     -0.7822|            0.0712|          -1.4721|              -0.8225|       -0.2500|        1.1000|  0.0399|   0.7703|       4.2444|       3.3070|   0.7849|   1.3541|  1.2754|    2.0258|     2.3635|  -1.2188|      -1.3048| 142.0572|          71.0286|         213.0858|          71.0286|         213.0858|          71.0286|          71.0286|          71.0286|          71.0286|         213.0858|          213.0858|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|           71.0286|          213.0858|          213.0858|          213.0858|          213.0858|           71.0286|           71.0286|          213.0858|           71.0286|           71.0286|          213.0858|          213.0858|           71.0286|           71.0286|           71.0286|           71.0286|          213.0858|    2|        3| 485.833| 551.896| 544.535| 546.151| 546.013| 535.842| 517.757| 509.575| 534.352| 566.853| 519.906| 539.614| 547.041| 554.625| 531.748| 541.801| 510.916| 568.291| 475.206| 497.850| 451.323| 468.250| 510.586| 531.433| 561.364| 540.507| 511.999| 558.558| 535.366|  413.639| 465.915| 473.691| 499.391| 470.539| 546.244| 527.365| 495.834| 537.913| 554.605|  458.782| 487.449| 506.400| 506.931| 516.703| 569.719| 519.064| 558.043| 578.880| 539.894|  480.368| 537.477| 506.118| 531.372| 500.348| 541.544| 550.238| 554.259| 472.640| 492.549|  512.635| 479.120| 517.907| 527.877| 481.168| 502.008| 494.766| 535.814| 487.814| 484.203|  523.968| 0.80261|02MAY19:09:49:49 |

</div>


### **rename()** fonksiyonu

- **select()** fonksiyonu icinde değişken seçimi sırasında değişken adı değişimi yapılabilir.

- Örnekte **ODOKUMA1** degişkeninin adını **okumapuan** olarak değiştirip seçebilirsiniz.


```r
PISA_OGR_2018 %>%
select(OGRENCIID,OKUL_TUR,CINSIYET,SES,okumapuan = ODOKUMA1) %>%
head(2)
```

<div class="kable-table">

| OGRENCIID|OKUL_TUR | CINSIYET|     SES| okumapuan|
|---------:|:--------|--------:|-------:|---------:|
|  79200768|TUR0112  |        2| -2.4521|   376.022|
|  79201064|TUR0112  |        2| -2.1042|   512.316|

</div>


- Örnekte ise **ODOKUMA1** degişkeninin adı okumapuan olarak **rename()** fonksiyonu ile de değiştirilebilir.


```r
PISA_OGR_2018 %>%
select(OGRENCIID,OKUL_TUR,CINSIYET,SES,ODOKUMA1) %>%
rename(okumapuan=ODOKUMA1)%>%
head(2)
```

<div class="kable-table">

| OGRENCIID|OKUL_TUR | CINSIYET|     SES| okumapuan|
|---------:|:--------|--------:|-------:|---------:|
|  79200768|TUR0112  |        2| -2.4521|   376.022|
|  79201064|TUR0112  |        2| -2.1042|   512.316|

</div>


### mutate fonksiyonu

- **mutate()** fonksiyonu ile veri setine yeni değişken ekleyebilirsiniz.

- **transmute()** fonksiyonu ile veri setine yeni değişken eklenirken, eski değişken/ler veri setiden çıkarılır.

- Okumadan zevk alma maddelerinden bir veri seti oluşturup, bu veri setine toplam puan ekleme


```r
zevk  <- select(PISA_OGR_2018, starts_with("ST097"))
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
mutate(toplam=rowSums(select(., ST097Q01TA:ST097Q05TA)),.before= ST097Q01TA)%>% head(2)
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

- Ilk olarak özyeterliği ölçen maddelerden yeni bir veri oluşturulmuş, daha sonra bu puanların önce toplam puanları daha sonra toplam puanların kareleri alınmıştır.


```r
ozyeterlik <- PISA_OGR_2018 %>%
  expss::drop_var_labs() %>%
  select(ST196Q02HA:ST196Q07HA)

ozyeterlik%>%
  rowwise() %>%
  mutate(toplam = sum(across()))%>%
  mutate(toplam_kare=toplam*toplam) %>% head(2)
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
table(PISA_OGR_2018$SINIF)
```

```
## 
##    7    8    9   10   11   12 
##    3   19 1295 5360  207    6
```

- **SINIF** değişkenini kullanarak ortaokul ve lise olmak üzere iki düzeyli **OKUL** adlı bir değişken oluşturalım.




```r
PISA_OGR_2018 %>%
  select(1:5) %>%
  mutate(okul = ifelse(SINIF == 7 | SINIF == 8,
                       "Ortaokul", "Lise")) %>%
    head(3)
```

<div class="kable-table">

|   OKULID| OGRENCIID|OKUL_TUR | KITAPCIK| SINIF|okul |
|--------:|---------:|:--------|--------:|-----:|:----|
| 79200001|  79200768|TUR0112  |       20|    10|Lise |
| 79200001|  79201064|TUR0112  |        5|    10|Lise |
| 79200001|  79201118|TUR0112  |       16|    10|Lise |

</div>


## case_when()

- **case_when()** fonksiyonu çoklu **ifelse() ** kullanımı ile benzer işlevi sağlar.

- **case_when()** birden fazla koşula dayalı karşılaştırmalarda yeni bir değişken oluşturmak amacıyla kullanılır.

- Sosyoekomik düzeye ilişikin betimsel istatistikler

```r
summary(PISA_OGR_2018$SES)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max.    NA's 
## -4.7546 -2.0633 -1.3002 -1.1712 -0.3228  2.7617      35
```


- SES değişkeninin kategorik hale getirilmesi


```r
v1 <- PISA_OGR_2018 %>%
  mutate(SES_kategorik =
    case_when(
      SES <=  -2 ~ "dusuk",
      SES > -2 & SES <  0 ~ "orta",
      SES >=0 ~ "yuksek" )) %>%
      select(SES,SES_kategorik)
```


- Olusturulan yeni SES_kategorik degişkeninin veri setinde nasıl dağıldığını inceleme



```r
v1 %>% group_by(SES_kategorik) %>% summarize(f=n())
```

<div class="kable-table">

|SES_kategorik |    f|
|:-------------|----:|
|dusuk         | 1856|
|orta          | 3676|
|yuksek        | 1323|
|NA            |   35|

</div>


teşekkürler !


- [Siz de yapın](https://learnr-examples.shinyapps.io/ex-data-filter/#section-welcome>)

- [Siz de yapın](https://learnr-examples.shinyapps.io/ex-data-summarise/)
--



<!--chapter:end:12-veri_duzenlemeIII.Rmd-->

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

<img src="images/left_join.PNG" width="60%" style="display: block; margin: auto;" />

- **A %>% right_join(B)**

`B` den tüm satırları, mümkün olduğunda `A` ile eşleştir (olmadığında "NA" verir), hem `A` hem de `B` den gelen sütunları alır.

<img src="images/right_join.PNG" width="60%" style="display: block; margin: auto;" />

-  Pratikte genellike **left_join()** kullanılır.




- **A %>% inner_join(B)**
<br>
yanlızca `A` ve `B` nin eşleşen satırlarını birleştirir. Hem `A` hem de `B` den gelen sütunları alır.

<img src="images/inner_join.PNG" width="75%" style="display: block; margin: auto;" />





- **A %>% full_join(B)** 

`A` ve `B` den tüm satırları birleştirir. Hem `A` hem de `B` den gelen sütunları alır.

<img src="images/full_join.PNG" width="75%" style="display: block; margin: auto;" />







- **A %>% semi_join(B)**

`A` nın `B` ile eşleşen satırlarını alır.  Sadece `A` dan gelen sütunları alır.

<img src="images/semi_join.PNG" width="75%" style="display: block; margin: auto;" />






-  **A %>% anti_join(B)**
<br>
`A` nın `B` ile eşleşemeyen satırlarını alır. Sadece `A` dan gelen sütunları alır.

<img src="images/anti_join.PNG" width="75%" style="display: block; margin: auto;" />



- Aynı değerleri içeren satırların olduğu sütunların *eşleşmesi* gerektiğini söylüyoruz.

- Bunları birleştirme için bir **by =** argümanını kullanıyoruz.

- Eğer birleştirme yapmak istediğimiz sütun/ların isimleri aynı ise **by =** argümanını kullanmaya gerek yoktur. 



cinsiyet1



```r
cinsiyet1
```

<div class="kable-table">

|ogrenci      |cinsiyet |
|:------------|:--------|
|Mert Kaya    |Erkek    |
|Zeynep Turan |Kiz      |
|Zeynep Inal  |Kiz      |

</div>

kangrubu1



```r
kangrubu1
```

<div class="kable-table">

|ogrenci      |kangrubu |
|:------------|:--------|
|Zeynep Turan |A Rh(-)  |
|Zeynep Inal  |0 Rh (+) |
|Can Eser     |ARh(+)   |

</div>


```r
left_join(cinsiyet1,kangrubu1)
```

```
## Joining with `by = join_by(ogrenci)`
```

<div class="kable-table">

|ogrenci      |cinsiyet |kangrubu |
|:------------|:--------|:--------|
|Mert Kaya    |Erkek    |NA       |
|Zeynep Turan |Kiz      |A Rh(-)  |
|Zeynep Inal  |Kiz      |0 Rh (+) |

</div>


```r
right_join(cinsiyet1,kangrubu1)
```

```
## Joining with `by = join_by(ogrenci)`
```

<div class="kable-table">

|ogrenci      |cinsiyet |kangrubu |
|:------------|:--------|:--------|
|Zeynep Turan |Kiz      |A Rh(-)  |
|Zeynep Inal  |Kiz      |0 Rh (+) |
|Can Eser     |NA       |ARh(+)   |

</div>



cinsiyet1

```r
cinsiyet1
```

<div class="kable-table">

|ogrenci      |cinsiyet |
|:------------|:--------|
|Mert Kaya    |Erkek    |
|Zeynep Turan |Kiz      |
|Zeynep Inal  |Kiz      |

</div>

kangrubu1

```r
kangrubu1
```

<div class="kable-table">

|ogrenci      |kangrubu |
|:------------|:--------|
|Zeynep Turan |A Rh(-)  |
|Zeynep Inal  |0 Rh (+) |
|Can Eser     |ARh(+)   |

</div>



```r
inner_join(cinsiyet1,kangrubu1)
```

```
## Joining with `by = join_by(ogrenci)`
```

<div class="kable-table">

|ogrenci      |cinsiyet |kangrubu |
|:------------|:--------|:--------|
|Zeynep Turan |Kiz      |A Rh(-)  |
|Zeynep Inal  |Kiz      |0 Rh (+) |

</div>



```r
full_join(cinsiyet1,kangrubu1)
```

```
## Joining with `by = join_by(ogrenci)`
```

<div class="kable-table">

|ogrenci      |cinsiyet |kangrubu |
|:------------|:--------|:--------|
|Mert Kaya    |Erkek    |NA       |
|Zeynep Turan |Kiz      |A Rh(-)  |
|Zeynep Inal  |Kiz      |0 Rh (+) |
|Can Eser     |NA       |ARh(+)   |

</div>



cinsiyet1

```r
cinsiyet1
```

<div class="kable-table">

|ogrenci      |cinsiyet |
|:------------|:--------|
|Mert Kaya    |Erkek    |
|Zeynep Turan |Kiz      |
|Zeynep Inal  |Kiz      |

</div>

kangrubu1

```r
kangrubu1
```

<div class="kable-table">

|ogrenci      |kangrubu |
|:------------|:--------|
|Zeynep Turan |A Rh(-)  |
|Zeynep Inal  |0 Rh (+) |
|Can Eser     |ARh(+)   |

</div>



```r
semi_join(cinsiyet1,kangrubu1)
```

```
## Joining with `by = join_by(ogrenci)`
```

<div class="kable-table">

|ogrenci      |cinsiyet |
|:------------|:--------|
|Zeynep Turan |Kiz      |
|Zeynep Inal  |Kiz      |

</div>



```r
anti_join(cinsiyet1,kangrubu1)
```

```
## Joining with `by = join_by(ogrenci)`
```

<div class="kable-table">

|ogrenci   |cinsiyet |
|:---------|:--------|
|Mert Kaya |Erkek    |

</div>




cinsiyet1

```r
cinsiyet2
```

<div class="kable-table">

|ogrenci      |cinsiyet |
|:------------|:--------|
|Mert Kaya    |Erkek    |
|Zeynep Turan |Kiz      |
|Zeynep Inal  |Kiz      |

</div>

kangrubu1

```r
kangrubu2
```

<div class="kable-table">

|ad           |kangrubu |
|:------------|:--------|
|Zeynep Turan |A Rh(-)  |
|Zeynep Inal  |0 Rh (+) |
|Can Eser     |ARh(+)   |

</div>



```r
cinsiyet2 %>% 
left_join(kangrubu2,by=c("ogrenci"="ad"))
```

<div class="kable-table">

|ogrenci      |cinsiyet |kangrubu |
|:------------|:--------|:--------|
|Mert Kaya    |Erkek    |NA       |
|Zeynep Turan |Kiz      |A Rh(-)  |
|Zeynep Inal  |Kiz      |0 Rh (+) |

</div>



```r
kangrubu2 %>% 
left_join(cinsiyet2,by=c("ad"="ogrenci"))
```

<div class="kable-table">

|ad           |kangrubu |cinsiyet |
|:------------|:--------|:--------|
|Zeynep Turan |A Rh(-)  |Kiz      |
|Zeynep Inal  |0 Rh (+) |Kiz      |
|Can Eser     |ARh(+)   |NA       |

</div>


<img src="images/kumeislemleri.png" width="70%" style="display: block; margin: auto;" />


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

<div class="kable-table">

|   OKULID| OGRENCIID| CINSIYET| KITAPSAYISI| ST196Q02HA| ST196Q03HA| ST196Q04HA| ST196Q05HA| ST196Q06HA| ST196Q07HA|
|--------:|---------:|--------:|-----------:|----------:|----------:|----------:|----------:|----------:|----------:|
| 79200001|  79200768|        2|           2|          3|          3|          4|          4|          3|          4|
| 79200001|  79201064|        2|           3|          3|          3|          4|          4|          3|          2|

</div>


```r
miniSCH <- PISA_SCH_2018 %>% select(CNTSCHID,okulbuyukluk = SCHSIZE,sinifbuyuk= CLSIZE)
miniSCH %>% head(2)
```

<div class="kable-table">

| CNTSCHID| okulbuyukluk| sinifbuyuk|
|--------:|------------:|----------:|
| 79200001|          775|         33|
| 79200002|         1178|         53|

</div>



- veri setinde eşleştirme yapılması istenilen değişkenin farklı adları olduğunda 

```r
left_join(miniOGR,miniSCH,by=c("OKULID"="CNTSCHID")) %>% head(6)
```

<div class="kable-table">

|   OKULID| OGRENCIID| CINSIYET| KITAPSAYISI| ST196Q02HA| ST196Q03HA| ST196Q04HA| ST196Q05HA| ST196Q06HA| ST196Q07HA| okulbuyukluk| sinifbuyuk|
|--------:|---------:|--------:|-----------:|----------:|----------:|----------:|----------:|----------:|----------:|------------:|----------:|
| 79200001|  79200768|        2|           2|          3|          3|          4|          4|          3|          4|          775|         33|
| 79200001|  79201064|        2|           3|          3|          3|          4|          4|          3|          2|          775|         33|
| 79200001|  79201118|        1|           1|          1|          2|          3|          2|          2|          2|          775|         33|
| 79200001|  79201275|        2|           1|          1|          1|          1|          1|          1|          1|          775|         33|
| 79200001|  79201481|        2|           2|          1|          4|          4|          1|          4|          4|          775|         33|
| 79200001|  79201556|        2|           2|          1|          1|          1|          1|          1|          1|          775|         33|

</div>



- konu ile ilgili daha fazla alıştırma için [adresini](https://rpubs.com/williamsurles/293454) inceleyebilirsiniz.

teşekkürler !






<!--chapter:end:13-veri_duzenlemeIV.Rmd-->

# Veri duzenleme  - V




- **tiydr** paketi
- **gather()** fonksiyonu
- **separete()** fonksiyonu
- **spread()** fonksiyonu
- **unite()** fonksiyonu 



## Veriyi İnceleme

- Bir veriyi R ortamamına aktardıktan sonra

  - Veri setinizde yer alan tüm satırlar/sütunlar doğru bir şekilde aktarılmış mı?
  
  - Sütun isimleri düzgün mü? 
  
  - Özellikle sütun adlarında boşluk olması ya da farklı      karakterler bulunması sıkıntı yaratabilir.



- Aktarılan boş satır ve sütunlar var mı?

  - **filter()** ve **select()** gibi fonksiyonlarla            incelebilir. 
   
- Eksik veriler nasıl temsil ediliyor?

  - **NA**,**" "** (bosluk), **.**, **999** ,  **9999**
  
  - eksik veriler **mutate()** ve **ifelse()** ile             düzenlebilir.
  
- character ve factor değişkenler düzgün tanımlanımış mı?
  
## Dağınık Veri

.pull-left-narrow[
  
    
| **Program**     | **Kadın** | **Erkek**|
|-----------------|----------:|---------:|
| Olcme           |      6    |    6     |
| Program         |      5    |    5     |
| Yonetim         |      7    |    8     |
| PDR             |      5    |    3     |


- Gözlem nedir?
  - Her bir programda yer alan öğrencilerin cinsiyeti
- Değişkenler nelerdir?
  - Program, Cinsiyet, Frekans
- Değerler nelerdir?
    + Program: Olcme, Program, Yonetim, PDR
    + Cinsiyet: Kadın, Erkek 
- Bunların degisken değeri olması gerekiyor, sutun baslığı değil!
    + Frekans: ***Frekanslar iki sütuna dağılmış !!!**


## Düzgün Veri


| **Program**     | **Cinsiyet** | **Frekans** |
|-----------------|-------------:|------------:|
| Olcme           |     Kadın    |    6        |
| Olcme           |     Erkek    |    6        |
| Program         |     Kadın    |    5        |
| Program         |     Erkek    |    5        |
| Yonetim         |     Kadın    |    7        |
| Yonetim         |     Erkek    |    8        |
| PDR             |     Kadın    |    5        |
| PDR             |     Erkek    |    3        |


- Değişkenler sütunda



- Gözlemler Satırlarda olmalıdır !


- Çok sayıda **satırı** anlamlandırmak, çok sayıda **sütunu** anlamlandırmaktan daha kolaydır.

- **ggplot2**,**plotly**,**lattice** gibi paketleri rahat kullanabilmek için düzenli veri gereklidir.

- hiyerarşik ve karma modeller için de verinin düzgün olması önemlidir.

- Değişken adları mümkün olduğunca anlamlı olmalıdır.

- Eksik değerler ve **dengesiz** tekrarlanan ölçüm verileriyle ilgili daha az sorun sağlar.



- **tidyr** paketi **reshape** paketi gibi veri düzenlemede kullanılabilir.

- **gather()**: bir dizi sütun alır ve onları iki yeni sütuna (kendi adını verebileceğin) dönüştürür.

  - A key:  Orijinal sütun adlarını saklayan bir anahtar
  - A value: Bu orijinal sütunlardaki değerlere sahip bir değer.

## **gather()** fonksiyonu

- Fonksiyonun kullanım şekli

```r
gather(data, key, value, ..., na.rm = FALSE, 
       convert = FALSE, factor_key = FALSE)
```

- Fonksiyonun kullanımı göstermek için veri seti oluşturma


```r
n=20
genisveri <- data.frame(
  ID = paste("ID",101:120,sep=""),
  Sure_1 = sample(50:60,20,replace=TRUE),
  Sure_2 = sample(40:55,20,replace=TRUE),
  Sure_3 = sample(35:50,20,replace=TRUE)
)
```




```r
genisveri %>% head(6)
```

<div class="kable-table">

|ID    | Sure_1| Sure_2| Sure_3|
|:-----|------:|------:|------:|
|ID101 |     57|     47|     44|
|ID102 |     57|     50|     36|
|ID103 |     52|     41|     47|
|ID104 |     56|     49|     43|
|ID105 |     59|     52|     49|
|ID106 |     57|     52|     43|

</div>


- gather() fonksiyonu geniş veriyi, uzun veri haline getirir.


```r
uzun <- genisveri %>% gather(Sure, Zaman, Sure_1:Sure_3)
```

- Olusan veride Sure_1,Sure_2 ve Sure_3, Sure değişkenin değerleri haline geldi.



```r
uzun %>% head(3)
```

<div class="kable-table">

|ID    |Sure   | Zaman|
|:-----|:------|-----:|
|ID101 |Sure_1 |    57|
|ID102 |Sure_1 |    57|
|ID103 |Sure_1 |    52|

</div>


```r
uzun %>% tail(3)
```

<div class="kable-table">

|   |ID    |Sure   | Zaman|
|:--|:-----|:------|-----:|
|58 |ID118 |Sure_3 |    50|
|59 |ID119 |Sure_3 |    38|
|60 |ID120 |Sure_3 |    47|

</div>

- Gördüğünüz gibi, şimdi iki sütunumuz var: Biri *Sure* için, diğeri **Zaman** için. Her katılımcı icin üc farkli süre degeri olduğu için her bir ID değeri üç kere tekrarlamaktadır.


## **separate()**

- **separate()** bir sütunu birden çok sütuna ayırır.

- değerlerin sütun adlarına gömüldüğü toplanmış verilerde ortaktır.

- Olusan veride Sure_1,Sure_2 ve Sure_3 değerlerinin karakter ve sayısal değerlerini ayırmak için **separate():** fonkisyonu kullanabilirsiniz.



```r
uzun_ayrı <- uzun %>% 
            separate(Sure, c("Sure","Sayı"),"_") 

uzun_ayrı %>% head(3)
```

<div class="kable-table">

|ID    |Sure |Sayı | Zaman|
|:-----|:----|:----|-----:|
|ID101 |Sure |1    |    57|
|ID102 |Sure |1    |    57|
|ID103 |Sure |1    |    52|

</div>


## **unite()** fonksiyonu

- **gather*()** fonksiyonun tam tersi olarak iki sütunu alıp
tek sutunda birlestirir.


```r
uzun_birles <- uzun_ayrı %>% unite(SURE, Sure, Sayı, sep = ".")
uzun_birles %>% head(3)
```

<div class="kable-table">

|ID    |SURE   | Zaman|
|:-----|:------|-----:|
|ID101 |Sure.1 |    57|
|ID102 |Sure.1 |    57|
|ID103 |Sure.1 |    52|

</div>


## **spread()** fonksiyonu

- **spread():**  **gather*()** fonksiyonun tam tersini yaparak uzun veriden genis veri olusturmaya yarar.


```r
tekrar_genis <- uzun_birles %>% spread(SURE, Zaman)
tekrar_genis %>% head(6)
```

<div class="kable-table">

|ID    | Sure.1| Sure.2| Sure.3|
|:-----|------:|------:|------:|
|ID101 |     57|     47|     44|
|ID102 |     57|     50|     36|
|ID103 |     52|     41|     47|
|ID104 |     56|     49|     43|
|ID105 |     59|     52|     49|
|ID106 |     57|     52|     43|

</div>








<!--chapter:end:14-veri_duzenlemeV.Rmd-->

# Betimleyici İstatistik 

<!-- https://statsandr.com/blog/descriptive-statistics-in-r/ -->

<!-- https://rpubs.com/williamsurles/298945 -->

 <!-- https://rpubs.com/odenipinedo/introduction-to-data-visualization-with-ggplot2 -->

## Veri Yükleme


- `PISA_STU_2018` ve PISA_STU_2018` veri setlerini kullanacağız. 

- veri seti R'de varsayılan olarak içe aktarılır, yalnızca PISA_STU_2018 çalıştırarak yüklemeniz gerekir:


```r
load("import/PISA_STU_2018.rda") # ogrenci verisi
head(PISA_STU_2018)
```

<div class="kable-table">

| CNTRYID|CNT | CNTSCHID| CNTSTUID|CYC  |NatCen |STRATUM |SUBNATIO | OECD| ADMINMODE| LANGTEST_QQQ| LANGTEST_COG| LANGTEST_PAQ| BOOKID| ST001D01T| ST003D02T| ST003D03T| ST004D01T| ST005Q01TA| ST006Q01TA| ST006Q02TA| ST006Q03TA| ST006Q04TA| ST007Q01TA| ST008Q01TA| ST008Q02TA| ST008Q03TA| ST008Q04TA| ST011Q01TA| ST011Q02TA| ST011Q03TA| ST011Q04TA| ST011Q05TA| ST011Q06TA| ST011Q07TA| ST011Q08TA| ST011Q09TA| ST011Q10TA| ST011Q11TA| ST011Q12TA| ST011Q16NA|ST011D17TA |ST011D18TA |ST011D19TA | ST012Q01TA| ST012Q02TA| ST012Q03TA| ST012Q05NA| ST012Q06NA| ST012Q07NA| ST012Q08NA| ST012Q09NA| ST013Q01TA| ST019AQ01T| ST019BQ01T| ST019CQ01T| ST021Q01TA| ST125Q01NA| ST126Q01TA| ST127Q01TA| ST127Q02TA| ST127Q03TA| ST022Q01TA| ST023Q01TA| ST023Q02TA| ST023Q03TA| ST023Q04TA| ST023Q05TA| ST097Q01TA| ST097Q02TA| ST097Q03TA| ST097Q04TA| ST097Q05TA| ST100Q01TA| ST100Q02TA| ST100Q03TA| ST100Q04TA| ST102Q01TA| ST102Q02TA| ST102Q03TA| ST102Q04TA| ST211Q01HA| ST211Q02HA| ST211Q03HA| ST212Q01HA| ST212Q02HA| ST212Q03HA| ST104Q02NA| ST104Q03NA| ST104Q04NA| ST213Q01HA| ST213Q02HA| ST213Q03HA| ST213Q04HA| ST150Q01IA| ST150Q02IA| ST150Q03IA| ST150Q04HA| ST152Q05IA| ST152Q06IA| ST152Q07IA| ST152Q08IA| ST154Q01HA| ST153Q01HA| ST153Q02HA| ST153Q03HA| ST153Q04HA| ST153Q05HA| ST153Q06HA| ST153Q08HA| ST153Q09HA| ST153Q10HA| ST158Q01HA| ST158Q02HA| ST158Q03HA| ST158Q04HA| ST158Q05HA| ST158Q06HA| ST158Q07HA| ST160Q01IA| ST160Q02IA| ST160Q03IA| ST160Q04IA| ST160Q05IA| ST167Q01IA| ST167Q02IA| ST167Q03IA| ST167Q04IA| ST167Q05IA| ST168Q01HA| ST175Q01IA| ST176Q01IA| ST176Q02IA| ST176Q03IA| ST176Q05IA| ST176Q06IA| ST176Q07IA| ST161Q01HA| ST161Q02HA| ST161Q03HA| ST161Q06HA| ST161Q07HA| ST161Q08HA| ST163Q02HA| ST163Q03HA| ST163Q04HA| ST164Q01IA| ST164Q02IA| ST164Q03IA| ST164Q04IA| ST164Q05IA| ST164Q06IA| ST165Q01IA| ST165Q02IA| ST165Q03IA| ST165Q04IA| ST165Q05IA| ST166Q01HA| ST166Q02HA| ST166Q03HA| ST166Q04HA| ST166Q05HA| ST016Q01NA| ST036Q05TA| ST036Q06TA| ST036Q08TA| ST225Q01HA| ST225Q02HA| ST225Q03HA| ST225Q04HA| ST225Q05HA| ST225Q06HA| ST181Q02HA| ST181Q03HA| ST181Q04HA| ST182Q03HA| ST182Q04HA| ST182Q05HA| ST182Q06HA| ST183Q01HA| ST183Q02HA| ST183Q03HA| ST184Q01HA| ST185Q01HA| ST185Q02HA| ST185Q03HA| ST186Q05HA| ST186Q06HA| ST186Q07HA| ST186Q10HA| ST186Q09HA| ST186Q02HA| ST186Q01HA| ST186Q08HA| ST186Q03HA| ST208Q01HA| ST208Q02HA| ST208Q04HA| ST188Q01HA| ST188Q02HA| ST188Q03HA| ST188Q06HA| ST188Q07HA| ST034Q01TA| ST034Q02TA| ST034Q03TA| ST034Q04TA| ST034Q05TA| ST034Q06TA| ST196Q02HA| ST196Q03HA| ST196Q04HA| ST196Q05HA| ST196Q06HA| ST196Q07HA| ST197Q01HA| ST197Q02HA| ST197Q04HA| ST197Q07HA| ST197Q08HA| ST197Q09HA| ST197Q12HA| ST215Q01HA| ST215Q02HA| ST215Q03HA| ST215Q04HA| ST215Q05HA| ST216Q01HA| ST216Q02HA| ST216Q03HA| ST216Q04HA| ST216Q05HA| ST216Q06HA| ST218Q01HA| ST218Q02HA| ST218Q03HA| ST218Q04HA| ST218Q05HA| ST218Q06HA| ST218Q07HA| ST222Q01HA| ST222Q03HA| ST222Q04HA| ST222Q05HA| ST222Q06HA| ST222Q08HA| ST222Q09HA| ST222Q10HA| ST214Q01HA| ST214Q02HA| ST214Q03HA| ST214Q06HA| ST220Q01HA| ST220Q02HA| ST220Q03HA| ST220Q04HA| ST217Q01HA| ST217Q02HA| ST217Q03HA| ST217Q04HA| ST217Q05HA| ST219Q01HA| ST219Q02HA| ST219Q03HA| ST219Q04HA| ST219Q05HA| ST219Q06HA| ST204Q02HA| ST204Q03HA| ST204Q04HA| ST204Q05HA| ST177Q01HA| ST177Q02HA| ST177Q03HA| ST189Q01HA| ST221Q01HA| ST221Q02HA| ST221Q03HA| ST221Q04HA| ST221Q05HA| ST221Q06HA| ST221Q07HA| ST221Q08HA| ST221Q09HA| ST221Q11HA| ST223Q02HA| ST223Q04HA| ST223Q05HA| ST223Q08HA| ST123Q02NA| ST123Q03NA| ST123Q04NA| ST205Q01HA| ST205Q02HA| ST205Q03HA| ST205Q04HA| ST059Q01TA| ST059Q02TA| ST059Q03TA| ST059Q04HA| ST060Q01NA| ST061Q01NA| ST062Q01TA| ST062Q02TA| ST062Q03TA| ST038Q03NA| ST038Q04NA| ST038Q05NA| ST038Q06NA| ST038Q07NA| ST038Q08NA| ST207Q01HA| ST207Q02HA| ST207Q03HA| ST207Q04HA| ST207Q05HA| ST206Q01HA| ST206Q02HA| ST206Q03HA| ST206Q04HA| IC001Q01TA| IC001Q02TA| IC001Q03TA| IC001Q04TA| IC001Q05TA| IC001Q06TA| IC001Q07TA| IC001Q08TA| IC001Q09TA| IC001Q10TA| IC001Q11TA| IC009Q01TA| IC009Q02TA| IC009Q03TA| IC009Q05NA| IC009Q06NA| IC009Q07NA| IC009Q08TA| IC009Q09TA| IC009Q10NA| IC009Q11NA| IC002Q01HA| IC004Q01HA| IC005Q01TA| IC006Q01TA| IC007Q01TA| IC150Q01HA| IC150Q02HA| IC150Q03HA| IC150Q04HA| IC150Q05HA| IC150Q06HA| IC150Q07HA| IC150Q08HA| IC150Q09HA| IC151Q01HA| IC151Q02HA| IC151Q03HA| IC151Q04HA| IC151Q05HA| IC151Q06HA| IC151Q07HA| IC151Q08HA| IC151Q09HA| IC152Q01HA| IC152Q02HA| IC152Q03HA| IC152Q04HA| IC152Q05HA| IC152Q06HA| IC152Q07HA| IC152Q08HA| IC152Q09HA| IC008Q01TA| IC008Q02TA| IC008Q03TA| IC008Q04TA| IC008Q05TA| IC008Q07NA| IC008Q08TA| IC008Q09TA| IC008Q10TA| IC008Q11TA| IC008Q12TA| IC008Q13NA| IC010Q01TA| IC010Q02NA| IC010Q03TA| IC010Q04TA| IC010Q05NA| IC010Q06NA| IC010Q07TA| IC010Q08TA| IC010Q09NA| IC010Q10NA| IC010Q11HA| IC010Q12HA| IC011Q01TA| IC011Q02TA| IC011Q03TA| IC011Q04TA| IC011Q05TA| IC011Q06TA| IC011Q07TA| IC011Q08TA| IC011Q09TA| IC011Q10HA| IC013Q01NA| IC013Q04NA| IC013Q05NA| IC013Q11NA| IC013Q12NA| IC013Q13NA| IC014Q03NA| IC014Q04NA| IC014Q06NA| IC014Q08NA| IC014Q09NA| IC015Q02NA| IC015Q03NA| IC015Q05NA| IC015Q07NA| IC015Q09NA| IC016Q01NA| IC016Q02NA| IC016Q04NA| IC016Q05NA| IC016Q07NA| IC169Q01HA| EC031Q01TA| EC032Q01TA| EC033Q01NA| EC150Q01WA| EC150Q02WA| EC150Q03WA| EC150Q04WA| EC150Q05WA| EC150Q06WA| EC150Q07WA| EC150Q08WA| EC150Q09WA| EC150Q10WA| EC151Q01WA| EC151Q01WB| EC151Q01WC| EC151Q02WA| EC151Q02WB| EC151Q02WC| EC151Q03WA| EC151Q03WB| EC151Q03WC| EC151Q04WA| EC151Q04WB| EC151Q04WC| EC151Q05WA| EC151Q05WB| EC151Q05WC| EC152Q01HA| EC153Q01HA| EC153Q02HA| EC153Q03HA| EC153Q04HA| EC153Q05HA| EC153Q06HA| EC153Q07HA| EC153Q08HA| EC153Q09HA| EC153Q10HA| EC153Q11HA| EC160Q01HA| EC158Q01HA| EC158Q02HA| EC159Q01HA| EC159Q02HA| EC163Q01HA| EC163Q02HA| EC163Q03HA| EC163Q04HA| EC163Q05HA| EC163Q06HA| EC163Q07HA| EC162Q01HA| EC162Q02HA| EC162Q03HA| EC162Q04HA| EC162Q05HA| EC162Q06HA| EC162Q07HA| EC162Q08HA| EC154Q01IA| EC154Q02IA| EC154Q03IA| EC154Q04HA| EC154Q05IA| EC154Q06IA| EC154Q07IA| EC154Q08HA| EC154Q09IA| EC012Q01NA| EC012Q02NA| EC012Q04NA| EC012Q06NA| EC012Q07NA| EC012Q08NA| EC012Q13HA| EC012Q12NA| EC155Q01DA| EC155Q02DA| EC155Q03DA| EC155Q04HA| EC155Q05HA| WB150Q01HA| WB151Q01HA| WB152Q01HA| WB153Q01HA| WB153Q02HA| WB153Q03HA| WB153Q04HA| WB153Q05HA| WB154Q01HA| WB154Q02HA| WB154Q03HA| WB154Q04HA| WB154Q05HA| WB154Q06HA| WB154Q07HA| WB154Q08HA| WB154Q09HA| WB155Q01HA| WB155Q02HA| WB155Q03HA| WB155Q04HA| WB155Q05HA| WB155Q06HA| WB155Q07HA| WB155Q08HA| WB155Q09HA| WB155Q10HA| WB156Q01HA| WB158Q01HA| WB160Q01HA| WB161Q01HA| WB162Q01HA| WB162Q02HA| WB162Q03HA| WB162Q04HA| WB162Q05HA| WB162Q06HA| WB162Q07HA| WB162Q08HA| WB162Q09HA| WB163Q01HA| WB163Q02HA| WB163Q03HA| WB163Q04HA| WB163Q05HA| WB163Q06HA| WB163Q07HA| WB163Q08HA| WB164Q01HA| WB165Q01HA| WB166Q01HA| WB166Q02HA| WB166Q03HA| WB166Q04HA| WB167Q01HA| WB168Q01HA| WB168Q02HA| WB168Q03HA| WB168Q04HA| WB171Q01HA| WB171Q02HA| WB171Q03HA| WB171Q04HA| WB172Q01HA| WB173Q01HA| WB173Q02HA| WB173Q03HA| WB173Q04HA| WB176Q01HA| WB177Q01HA| WB177Q02HA| WB177Q03HA| WB177Q04HA| WB032Q01NA| WB032Q02NA| WB031Q01NA| WB178Q01HA| WB178Q02HA| WB178Q03HA| WB178Q04HA| WB178Q05HA| WB178Q06HA| WB178Q07HA| FL150Q01TA| FL150Q02TA| FL150Q03TA| FL151Q01HA| FL151Q02HA| FL164Q01HA| FL164Q02HA| FL164Q03HA| FL164Q04HA| FL164Q05HA| FL164Q06HA| FL164Q07HA| FL164Q08HA| FL164Q09HA| FL164Q10HA| FL164Q11HA| FL164Q12HA| FL164Q13HA| FL164Q14HA| FL164Q15HA| FL164Q16HA| FL164Q17HA| FL164Q18HA| FL165Q01HA| FL165Q02HA| FL165Q03HA| FL165Q04HA| FL166Q01HA| FL166Q02HA| FL166Q03HA| FL166Q05HA| FL166Q06HA| FL166Q07HA| FL153Q01HA| FL153Q02HA| FL153Q03HA| FL153Q04HA| FL153Q05HA| FL153Q06HA| FL167Q01HA| FL167Q02HA| FL167Q03HA| FL167Q04HA| FL167Q05HA| FL156Q01TA| FL156Q02TA| FL156Q03TA| FL156Q04TA| FL156Q05TA| FL156Q06TA| FL156Q07HA| FL159Q01HA| FL159Q02HA| FL159Q03HA| FL159Q04HA| FL160Q01HA| FL160Q02HA| FL160Q03HA| FL160Q04HA| FL161Q01HA| FL161Q02HA| FL161Q03HA| FL162Q01HA| FL162Q02HA| FL162Q03HA| FL162Q04HA| FL162Q05HA| FL162Q06HA| FL163Q01HA| FL163Q02HA| FL163Q03HA| FL163Q04HA| FL163Q05HA| FL168Q01HA| FL168Q02HA| FL168Q03HA| FL168Q04HA| FL168Q05HA| FL168Q06HA| FL168Q07HA| FL168Q08HA| FL169Q01HA| FL169Q02HA| FL169Q03HA| FL169Q04HA| PA001Q01TA| PA001Q02TA| PA001Q03TA| PA003Q01TA| PA003Q02TA| PA003Q03TA| PA003Q04HA| PA003Q05IA| PA003Q06IA| PA003Q07IA| PA154Q01IA| PA154Q02IA| PA154Q03IA| PA154Q04IA| PA154Q05IA| PA154Q06IA| PA154Q07IA| PA154Q08IA| PA154Q09IA| PA154Q10HA| PA155Q01IA| PA156Q01HA| PA156Q02HA| PA156Q03HA| PA156Q04HA| PA004Q02NA| PA004Q03NA| PA004Q04NA| PA008Q01TA| PA008Q02TA| PA008Q03TA| PA008Q04TA| PA008Q05TA| PA008Q06NA| PA008Q07NA| PA008Q08NA| PA008Q09NA| PA008Q10NA| PA009Q01NA| PA009Q02NA| PA009Q03NA| PA009Q04NA| PA009Q05NA| PA009Q06NA| PA009Q07NA| PA009Q08NA| PA009Q09NA| PA009Q10NA| PA009Q11NA| PA007Q01TA| PA007Q02TA| PA007Q03TA| PA007Q04TA| PA007Q05TA| PA007Q06TA| PA007Q07TA| PA007Q09NA| PA007Q11NA| PA007Q12NA| PA007Q13NA| PA007Q14NA| PA007Q15NA| PA005Q01TA| PA006Q01TA| PA006Q02TA| PA006Q03TA| PA006Q04TA| PA006Q05TA| PA006Q06TA| PA006Q07TA| PA006Q08TA| PA006Q09TA| PA006Q10TA| PA006Q11TA| PA006Q12HA| PA006Q13HA| PA006Q14HA| PA158Q01HA| PA158Q02IA| PA158Q03HA| PA158Q04IA| PA158Q05HA| PA159Q01HA| PA160Q01HA| PA160Q02HA| PA160Q03HA| PA160Q04HA| PA160Q05HA| PA161Q01HA| PA161Q02HA| PA161Q03HA| PA161Q05HA| PA161Q06HA| PA161Q07HA| PA162Q01HA| PA163Q01HA| PA166Q01HA| PA167Q02HA| PA167Q03HA| PA167Q04HA| PA167Q05HA| PA168Q01HA| PA168Q02HA| PA168Q03HA| PA168Q06HA| PA169Q01HA| PA169Q02HA| PA169Q03HA| PA169Q04HA| PA169Q05HA| PA169Q06HA| PA170Q01HA| PA170Q02HA| PA170Q04HA| PA170Q07HA| PA170Q08HA| PA170Q09HA| PA170Q12HA| PA171Q01HA| PA171Q03HA| PA171Q04HA| PA171Q05HA| PA171Q06HA| PA171Q08HA| PA171Q09HA| PA171Q10HA| PA172Q01WA| PA172Q02WA| PA172Q03WA| PA172Q04WA| PA172Q05WA| PA172Q06WA| PA018Q01NA| PA018Q02NA| PA018Q03NA| PA177Q01HA| PA177Q02HA| PA177Q03HA| PA177Q04HA| PA177Q05HA| PA177Q06HA| PA177Q07HA| PA177Q08HA| PA180Q01HA| PA182Q01HA| PA175Q01HA| PA175Q02HA| PA041Q01TA| PA042Q01TA| EFFORT1| EFFORT2|OCOD1 |OCOD2 |OCOD3 | GRADE|   AGE|PROGN    |COBN_S |COBN_M |COBN_F | LANGN| ISCEDL| ISCEDD| ISCEDO| MISCED| FISCED| HISCED| PARED| MISCED_D| FISCED_D| HISCED_D| PAREDINT| BMMJ1| BFMJ2| HISEI| LANGMOTHER| LANGFATHER| LANGSIBLINGS| LANGFRIEND| LANGSCHMATES| IMMIG| DURECEC| REPEAT|  BSMJ| MMINS| LMINS| SMINS| TMINS| FCFMLRTY| SCCHANGE| CHANGE| STUBMI|    ESCS| UNDREM| METASUM| METASPAM| ICTHOME| ICTSCH| HOMEPOS| CULTPOSS|  HEDRES|  WEALTH|  ICTRES| DISCLIMA| TEACHSUP|  DIRINS| PERFEED| EMOSUPS| STIMREAD| ADAPTIVITY| TEACHINT| JOYREAD| SCREADCOMP| SCREADDIFF| PISADIFF| PERCOMP| PERCOOP| ATTLNACT| COMPETE| WORKMAST| GFOFAIL|   EUDMO|    SWBP| RESILIENCE| MASTGOAL| GCSELFEFF| GCAWARE|  ATTIMM| INTCULT| PERSPECT| COGFLEX| RESPECT|  AWACOM| GLOBMIND| DISCRIM|  BELONG| BEINGBULLIED|  ENTUSE| HOMESCH|  USESCH|  INTICT| COMPICT|  AUTICT| SOIAICT| ICTCLASS| ICTOUTSIDE| INFOCAR| INFOJOB1| INFOJOB2| FLCONFIN| FLCONICT| FLSCHOOL| FLFAMILY| CURSUPP| EMOSUPP| PQSCHOOL| PASCHPOL| PRESUPP| JOYREADP| ATTIMMP| INTCULTP| GCAWAREP| BODYIMA| SOCONPA| W_FSTUWT| W_FSTURWT1| W_FSTURWT2| W_FSTURWT3| W_FSTURWT4| W_FSTURWT5| W_FSTURWT6| W_FSTURWT7| W_FSTURWT8| W_FSTURWT9| W_FSTURWT10| W_FSTURWT11| W_FSTURWT12| W_FSTURWT13| W_FSTURWT14| W_FSTURWT15| W_FSTURWT16| W_FSTURWT17| W_FSTURWT18| W_FSTURWT19| W_FSTURWT20| W_FSTURWT21| W_FSTURWT22| W_FSTURWT23| W_FSTURWT24| W_FSTURWT25| W_FSTURWT26| W_FSTURWT27| W_FSTURWT28| W_FSTURWT29| W_FSTURWT30| W_FSTURWT31| W_FSTURWT32| W_FSTURWT33| W_FSTURWT34| W_FSTURWT35| W_FSTURWT36| W_FSTURWT37| W_FSTURWT38| W_FSTURWT39| W_FSTURWT40| W_FSTURWT41| W_FSTURWT42| W_FSTURWT43| W_FSTURWT44| W_FSTURWT45| W_FSTURWT46| W_FSTURWT47| W_FSTURWT48| W_FSTURWT49| W_FSTURWT50| W_FSTURWT51| W_FSTURWT52| W_FSTURWT53| W_FSTURWT54| W_FSTURWT55| W_FSTURWT56| W_FSTURWT57| W_FSTURWT58| W_FSTURWT59| W_FSTURWT60| W_FSTURWT61| W_FSTURWT62| W_FSTURWT63| W_FSTURWT64| W_FSTURWT65| W_FSTURWT66| W_FSTURWT67| W_FSTURWT68| W_FSTURWT69| W_FSTURWT70| W_FSTURWT71| W_FSTURWT72| W_FSTURWT73| W_FSTURWT74| W_FSTURWT75| W_FSTURWT76| W_FSTURWT77| W_FSTURWT78| W_FSTURWT79| W_FSTURWT80| UNIT| WVARSTRR| PV1MATH| PV2MATH| PV3MATH| PV4MATH| PV5MATH| PV6MATH| PV7MATH| PV8MATH| PV9MATH| PV10MATH| PV1READ| PV2READ| PV3READ| PV4READ| PV5READ| PV6READ| PV7READ| PV8READ| PV9READ| PV10READ| PV1SCIE| PV2SCIE| PV3SCIE| PV4SCIE| PV5SCIE| PV6SCIE| PV7SCIE| PV8SCIE| PV9SCIE| PV10SCIE| PV1GLCM| PV2GLCM| PV3GLCM| PV4GLCM| PV5GLCM| PV6GLCM| PV7GLCM| PV8GLCM| PV9GLCM| PV10GLCM| PV1RCLI| PV2RCLI| PV3RCLI| PV4RCLI| PV5RCLI| PV6RCLI| PV7RCLI| PV8RCLI| PV9RCLI| PV10RCLI| PV1RCUN| PV2RCUN| PV3RCUN| PV4RCUN| PV5RCUN| PV6RCUN| PV7RCUN| PV8RCUN| PV9RCUN| PV10RCUN| PV1RCER| PV2RCER| PV3RCER| PV4RCER| PV5RCER| PV6RCER| PV7RCER| PV8RCER| PV9RCER| PV10RCER| PV1RTSN| PV2RTSN| PV3RTSN| PV4RTSN| PV5RTSN| PV6RTSN| PV7RTSN| PV8RTSN| PV9RTSN| PV10RTSN| PV1RTML| PV2RTML| PV3RTML| PV4RTML| PV5RTML| PV6RTML| PV7RTML| PV8RTML| PV9RTML| PV10RTML|   SENWT|VER_DAT          | test|
|-------:|:---|--------:|--------:|:----|:------|:-------|:--------|----:|---------:|------------:|------------:|------------:|------:|---------:|---------:|---------:|---------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|:----------|:----------|:----------|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|-------:|-------:|:-----|:-----|:-----|-----:|-----:|:--------|:------|:------|:------|-----:|------:|------:|------:|------:|------:|------:|-----:|--------:|--------:|--------:|--------:|-----:|-----:|-----:|----------:|----------:|------------:|----------:|------------:|-----:|-------:|------:|-----:|-----:|-----:|-----:|-----:|--------:|--------:|------:|------:|-------:|------:|-------:|--------:|-------:|------:|-------:|--------:|-------:|-------:|-------:|--------:|--------:|-------:|-------:|-------:|--------:|----------:|--------:|-------:|----------:|----------:|--------:|-------:|-------:|--------:|-------:|--------:|-------:|-------:|-------:|----------:|--------:|---------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|--------:|-------:|-------:|------------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|----------:|-------:|--------:|--------:|--------:|--------:|--------:|--------:|-------:|-------:|--------:|--------:|-------:|--------:|-------:|--------:|--------:|-------:|-------:|--------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|-----------:|----:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|-------:|--------:|-------:|:----------------|----:|
|     792|TUR | 79200001| 79200768|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|     20|        10|        10|      2002|         2|          3|          2|          2|          2|         NA|          3|          2|          2|          2|         NA|          1|          1|          1|          2|          2|          2|          1|          1|          2|          1|          2|          1|          2|0792002    |0792002    |0792002    |          2|          1|          2|          2|          1|          2|          1|          3|          2|          1|          1|          1|         NA|          6|          5|          1|          1|          1|          1|          4|          4|          4|          4|          4|          1|          2|          1|          1|          1|          2|          2|          2|          3|          2|          2|          3|          2|          2|          3|          3|          3|          2|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          4|          2|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          2|          1|          2|          2|          1|          1|          2|          2|          4|          1|          3|          2|          1|          1|          1|          2|          1|          1|          1|         NA|          3|          4|          4|          5|          2|          4|          1|          4|          3|          2|          2|          2|          2|          2|          2|          3|          2|          1|          1|          3|          1|          1|          2|          1|          1|          1|          5|          5|          3|          1|          6|         NA|          1|          1|          2|          0|          0|          0|         NA|          0|          1|          4|          4|          4|          4|          4|          4|          3|          4|          1|          1|          1|          4|          1|          2|          2|          1|          2|          1|          3|          3|          3|          3|          3|         NA|          5|          5|          4|          4|          4|          4|          4|          3|          3|          3|          3|          3|          3|          3|          3|          4|          4|          3|          4|          3|          2|          3|          3|          3|          3|          3|          4|          3|          3|          4|          5|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|         NA|          3|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          1|          1|          1|          2|          1|          1|          1|          1|          1|          1|         NA|          1|          1|          1|          2|          2|          2|          2|          4|          4|          4|          4|          4|          4|          4|          5|          6|          7|          6|         NA|         NA|          2|          2|          3|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          4|          3|          3|          2|          3|          3|          1|          1|          2|          3|          3|          3|          2|          3|          3|          2|          2|          2|          2|          2|          2|          1|          5|          4|          1|          5|          7|          1|          1|          3|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          3|          4|          1|          4|          3|          4|          2|          1|          2|          1|          1|          1|          1|          2|          1|          1|          1|          1|          5|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          2|          4|          4|          3|          3|          3|          3|          3|          4|          4|          4|          4|          4|          3|          3|          3|          3|          3|          2|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|      10|      10|9701  |6111  |9704  |     0| 15.50|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      2|      2|      2|     8|        2|        2|        2|        9| 17.00| 11.56| 17.00|         NA|         NA|           NA|         NA|           NA|     1|       1|      0|    NA|    NA|    NA|    NA|    NA|       NA|       NA|     NA|     NA| -2.4521|  -0.94|   -1.72|    -0.04|       4|      8| -2.3750|  -0.5921| -1.3835| -2.8866| -2.4931|  -1.9119|  -0.3971| -0.2546| -0.3253|  1.0346|  -0.9225|    -0.1716|  -1.0615| -0.2891|    -0.6712|    -0.0697|   0.2705|  2.0378|  1.6762|   0.4626|  2.0054|   1.8164| -1.1090| -0.8382| -1.1889|     2.3693|       NA|    0.9683| -0.2736|  1.4992|  0.1208|  -1.2292|  0.2165|  0.9289| -0.1577|  -2.8778|  0.5881| -0.6659|      -0.7823| -0.5131| -0.3817| -1.7161|  1.0435|  0.0537|  2.0258|  0.5149|   0.0390|    -1.3048|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 483.048| 477.281| 480.638| 494.293| 507.554| 522.458| 538.795| 402.822| 485.275|  540.275| 376.022| 417.746| 420.630| 413.837| 434.434| 424.054| 470.450| 446.634| 440.164|  443.152| 462.325| 427.972| 456.810| 434.988| 444.467| 457.415| 453.608| 447.165| 463.464|  463.425|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 424.897| 436.019| 444.568| 449.735| 403.609| 458.672| 457.902| 452.226| 411.985|  451.702| 439.127| 469.127| 474.409| 484.051| 459.989| 492.256| 496.422| 483.753| 461.741|  436.576| 448.889| 465.273| 467.666| 513.751| 437.552| 546.952| 468.595| 465.507| 503.251|  469.400| 473.404| 443.435| 455.826| 487.585| 514.687| 468.640| 462.800| 473.295| 487.510|  460.414| 475.910| 440.472| 437.323| 465.047| 466.901| 418.813| 483.735| 445.559| 475.808|  462.321| 0.80261|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200001| 79201064|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|      5|        10|         2|      2002|         2|          3|          2|          2|          2|         NA|          3|          2|          2|          2|         NA|          1|          2|          1|          2|          2|          2|          1|          1|          1|          1|          2|          1|          2|0792001    |0792002    |0792002    |          2|          2|          2|          4|          1|          1|          1|          4|          3|          1|          1|          1|         NA|          6|          5|          1|          1|          1|          1|          4|          4|          4|          4|          4|          3|          2|          3|          3|          3|          4|          3|          3|          2|          2|          3|          2|          2|          3|          2|          1|          4|          2|          2|          2|          2|          3|          1|          1|          2|          2|          1|          1|          1|          4|          3|          4|          3|          4|          5|          1|          1|          2|          1|          1|          1|          1|          2|          2|          2|          1|          2|          2|          1|          1|          1|          2|          4|          3|          4|          2|          2|          4|          5|          2|          5|          4|          3|          2|          5|          5|          5|          5|          5|          4|          3|          4|          2|          3|          1|          3|          3|          4|          5|          5|          2|          6|          2|          3|          6|          6|          5|          6|          6|          2|          6|          4|          1|          6|          7|          1|          1|          1|          0|          0|          0|         NA|          0|          1|          4|          4|          4|          3|          4|          3|          3|          4|          4|          4|          2|          3|          2|          1|          3|          1|          2|          2|          3|          4|          3|          3|          2|          4|          5|          4|          3|          3|          1|          4|          4|          3|          4|          2|          3|          3|          4|          3|          3|          4|          4|          3|          2|          3|          3|          4|          3|          4|          4|          2|          1|          1|          1|          3|          4|          2|          2|          1|          4|          2|          3|          3|          4|          3|          4|          2|          3|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          3|          2|          2|          2|          2|          1|          1|          1|          1|          1|          2|          4|          3|          4|          4|          3|          4|          3|          1|          3|          2|          3|          1|          1|          2|          1|          1|          2|          2|          2|          1|          1|          2|          1|          1|          2|          3|          3|          3|          4|          3|          1|          3|          3|          3|          4|          6|          6|          6|          6|         60|         35|          1|          1|          3|          4|          4|          2|          1|          2|          3|          2|          3|          3|          3|          3|          2|          3|          2|          1|          2|          3|          3|          3|          3|          2|          1|          1|          3|          1|          3|          2|          3|          3|          3|          3|          3|          1|          3|          3|          1|          3|          4|          3|          4|          4|          4|          4|          4|          4|          1|          5|          2|          5|          1|          1|          4|          4|          1|          3|          5|          1|          5|          1|          1|          1|          1|          1|          4|          5|          3|          5|          1|          5|          5|          2|          5|          5|          1|          3|          4|          5|          4|          1|          2|          2|          3|          1|          1|          4|          4|          2|          2|          2|          5|          5|          4|          4|          1|          4|          2|          1|          1|          3|          2|          2|          4|          4|          3|          4|          4|          4|          4|          3|          4|          4|          4|          4|          4|          4|          4|          4|          3|          4|          4|          4|          4|          4|          3|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|       7|      10|9701  |7531  |2611  |     0| 16.17|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      2|      2|      2|     8|        2|        2|        2|        9| 17.00| 23.47| 23.47|         NA|         NA|           NA|         NA|           NA|     1|       1|      0| 86.72|   210|   210|   210|  2100|       NA|       NA|     NA|     NA| -2.1042|  -0.60|   -0.95|     0.42|       5|      3| -1.8443|   0.3624| -1.3835| -2.3397| -2.3112|  -0.4003|  -1.1176| -0.3733|  0.0728| -1.0624|   1.0741|     0.1888|  -1.4401|  0.6040|     1.2374|    -0.1817|   1.9717|  0.6912| -0.4213|   1.0844|  2.0054|   0.4870|  1.8905| -1.0946| -1.1176|     0.1123|   1.1101|    0.4153|  0.6013| -1.0478| -0.1149|   1.0349|  0.3024|  0.9289|  0.4748|   1.3556|  1.5785| -0.3540|       2.4122|  0.2570|  0.5014|  0.4012|  1.3541|  1.4987|  1.3545|  2.3635|   1.2850|     0.9409|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 541.139| 529.618| 516.712| 509.319| 543.800| 544.083| 537.209| 476.977| 519.471|  532.874| 512.316| 473.229| 563.902| 485.396| 500.394| 495.048| 477.050| 526.291| 523.062|  481.411| 536.046| 555.509| 553.832| 531.649| 528.851| 533.099| 499.113| 537.615| 549.746|  452.920|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 480.514| 502.597| 479.291| 535.308| 429.311| 471.008| 458.337| 476.741| 506.172|  450.403| 519.885| 536.260| 506.943| 532.521| 462.051| 487.408| 497.342| 548.166| 530.531|  474.572| 559.394| 532.476| 545.079| 589.216| 482.084| 524.097| 498.018| 567.929| 499.327|  490.810| 447.791| 521.353| 502.951| 467.590| 451.939| 471.438| 480.654| 548.421| 496.817|  438.275| 500.916| 528.225| 517.816| 505.885| 477.363| 526.670| 521.478| 523.722| 494.396|  467.632| 0.80261|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200001| 79201118|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|     16|        10|         1|      2002|         1|          4|          2|          2|          2|         NA|          3|          2|          2|          2|         NA|          2|          2|          2|          2|          1|          2|          1|          1|          1|          1|          1|          1|          1|0792002    |0792001    |0792002    |          2|          3|          2|          4|          1|          1|          1|          1|          1|          1|          1|          1|         NA|          6|          5|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          3|          3|          3|          3|          2|          2|          2|          3|          2|          2|          3|          3|          3|          2|          2|          2|          2|          1|          2|          2|          2|          2|          3|          3|          3|          2|          1|          1|          2|          2|          2|          2|          2|          4|          1|          2|          2|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          2|          2|          1|          1|          4|          4|          4|         NA|          5|          2|          2|          2|          4|          2|          4|          3|          2|          3|          2|          3|          3|          1|          4|          1|          1|          6|          2|          6|          6|          3|          6|          5|          6|          6|          6|          1|          6|          6|          6|          6|          4|          2|          2|          2|          0|          0|          0|         NA|          0|          1|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          3|          3|          3|          3|          3|          3|          1|          2|          2|          3|          3|          3|          3|          3|          3|          2|          2|          2|          2|          2|          3|          2|          2|          3|          2|          3|          1|          2|          3|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          3|          3|          3|          3|          2|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          1|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          4|          5|          2|          2|         41|         70|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          2|          2|          2|          2|          3|          3|          3|          3|          3|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          5|          5|          1|          3|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|          4|          4|          4|          4|          4|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|       8|       9|9701  |6111  |2330  |     0| 16.25|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      1|      2|      2|     8|        1|        2|        2|        9| 17.00| 11.56| 17.00|         NA|         NA|           NA|         NA|           NA|     1|       1|      0| 82.41|   350|   280|   140|  2870|       NA|       NA|     NA|     NA| -2.2700|   0.10|   -0.18|    -0.04|       3|      0| -1.9449|   0.2154| -1.5164| -1.9453| -2.0867|  -0.3031|  -0.3971| -0.5072| -0.3253| -0.6576|  -0.6200|    -0.9282|  -0.3689|  0.6380|    -0.4089|     0.9065|   0.8876|  0.6912| -0.9391|  -0.6583|  0.1956|  -0.1015|  0.4637|  0.2621| -0.5928|    -1.4832|  -0.4347|   -0.9111| -0.0549| -0.2014| -0.4982|  -0.8702| -0.8312| -0.4401| -0.1577|   0.2910|  0.5881| -0.3184|       2.0700| -3.5940| -2.2971| -1.7161| -1.7210| -1.1888| -1.1563| -0.7345|   0.3701|     0.2858|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 438.872| 410.058| 448.972| 509.320| 438.305| 437.978| 374.374| 394.238| 389.679|  406.201| 396.383| 413.859| 423.121| 452.124| 392.434| 433.205| 387.037| 406.997| 402.509|  438.667| 416.271| 399.453| 467.897| 481.931| 414.718| 412.110| 397.644| 408.578| 422.486|  431.633|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 405.191| 390.350| 424.945| 452.030| 344.114| 440.066| 468.701| 486.608| 424.487|  446.807| 445.660| 485.928| 402.752| 495.788| 425.782| 475.268| 500.588| 487.242| 456.602|  468.181| 441.278| 435.867| 423.106| 449.796| 408.176| 468.193| 461.418| 481.248| 479.042|  447.929| 482.026| 460.715| 453.753| 475.813| 475.101| 429.407| 503.751| 457.465| 445.960|  461.785| 435.054| 427.410| 463.953| 450.673| 483.763| 435.906| 462.534| 464.111| 433.016|  474.589| 0.80261|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200001| 79201275|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|     21|         9|         9|      2002|         2|          1|         NA|          1|         NA|         NA|          1|         NA|          1|         NA|         NA|          1|          1|          1|          1|          2|          1|          2|          2|          2|          1|          2|          1|          2|0792001    |0792002    |0792002    |          3|          1|          1|          2|          2|          1|          1|          1|          1|          1|          1|          1|         NA|          6|          5|          1|          1|          1|          1|          4|          4|          4|          4|          4|          2|          2|          3|          1|          1|          3|          2|          1|          4|          2|          3|          4|          3|          3|          2|          2|          2|          2|          2|          3|          2|          3|          2|          2|          2|          2|          4|          4|          4|          4|          2|          2|          2|          2|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          3|          1|          1|          3|          3|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          2|          2|          2|          1|          1|          1|          6|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|          2|          2|          2|          0|          0|          0|         NA|          0|          1|          4|          3|          4|          1|          1|          1|          1|          1|          1|          1|          3|          1|          1|          1|          4|          2|          1|          1|          4|          1|          2|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|          2|          3|          2|          2|          3|          1|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          3|          3|          1|          2|          1|          3|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|          1|          3|          2|          2|          1|          2|          1|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          2|          2|          2|          2|          1|          1|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|         NA|          3|          2|          2|          2|          2|          5|          6|          6|          4|         40|         40|          2|          2|          2|          2|          2|          2|          2|          2|          2|          1|          1|          2|          2|          3|          2|          2|          2|          2|          1|          1|          1|          1|          1|          3|          1|          2|          1|          2|          3|          1|          1|          1|          1|          2|          2|          2|          3|          2|          1|          1|          2|          1|          5|          5|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          1|          2|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          3|          4|          4|          1|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|      10|      10|2330  |2330  |2211  |    -1| 15.58|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      6|      6|      6|    16|        6|        6|        6|       16| 82.41| 82.41| 82.41|         NA|         NA|           NA|         NA|           NA|     1|       1|      0| 88.70|   240|   200|   240|  1600|       NA|       NA|     NA|     NA|  0.0324|  -0.60|   -1.72|    -1.41|       9|      9| -2.1008|  -2.7469| -0.6853| -2.1121| -1.7005|  -1.1699|  -0.4060| -1.0499|  0.2682|      NA|  -0.6200|    -0.5786|  -1.0615| -1.1538|    -0.8250|     1.2421|   0.2705| -0.6142| -0.9391|  -0.6583|  1.1811|  -2.7365| -1.8939| -2.1464| -1.2568|    -1.4832|  -1.3162|   -2.7142| -0.0549| -1.2083| -0.2157|  -0.3405|  1.3823| -1.2781| -1.3933|   0.2910| -1.1549| -0.4217|       1.1625| -2.7049| -0.5991| -1.0707| -2.9336| -2.6033| -2.5144|  0.2639|   1.0418|    -1.3048|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 417.314| 486.246| 419.767| 413.368| 508.158| 475.248| 527.383| 482.872| 477.418|  476.539| 393.006| 428.757| 364.850| 382.522| 378.563| 416.048| 395.846| 383.782| 374.509|  381.877| 402.112| 431.478| 384.063| 472.941| 420.800| 472.894| 460.407| 465.356| 439.954|  442.546|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 377.648| 346.106| 347.468| 351.544| 464.958| 406.800| 305.063| 415.645| 451.572|  332.146| 418.336| 387.692| 376.644| 348.832| 469.856| 438.034| 377.209| 433.141| 463.976|  390.554| 370.646| 356.020| 346.501| 346.212| 425.656| 396.229| 416.122| 421.807| 457.353|  390.627| 419.099| 390.744| 410.400| 377.828| 443.815| 406.021| 393.957| 420.428| 398.023|  462.478| 400.889| 416.115| 426.449| 396.449| 425.235| 391.150| 373.368| 416.023| 417.897|  416.855| 0.80261|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200001| 79201481|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|      1|         9|         9|      2002|         2|          1|         NA|         NA|         NA|         NA|          1|          2|          2|          2|         NA|          1|          1|          1|          1|          1|          1|          1|          2|          2|          1|          1|          1|          2|0792001    |0792001    |0792001    |          3|          2|          3|          4|          3|          3|          1|          3|          2|          1|          1|          1|         NA|          8|          4|          1|          1|          1|          1|          4|          4|          4|          4|          4|          3|          3|          4|          3|          1|          2|          3|          1|          4|          3|          1|          2|          2|          3|          2|          2|          1|          1|          3|          3|          2|          4|          1|          1|          1|          1|          1|          1|          4|          1|          4|          3|          2|          3|          5|          2|          2|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          4|          4|          4|          2|          4|          1|          1|          5|          5|          5|          4|          3|          4|          5|          5|          5|          5|          3|          4|          4|          4|          2|          2|          2|          1|          1|          1|          6|          6|          6|          6|          6|          6|          6|          6|          6|          6|          6|          5|          5|          6|          1|          6|          1|          4|          1|          1|          0|          0|          1|         NA|          0|          1|          4|          4|          4|          3|          2|          4|          3|          4|          4|          4|          3|          3|          3|          3|          4|          4|          4|          4|          4|          1|          1|          2|          3|          2|          2|          2|          2|          3|          2|          3|          2|          2|          1|          1|          4|          1|          3|          1|          4|          4|          1|          4|          4|          3|          3|          4|          4|          3|          3|          3|          4|          3|          3|          1|          2|          1|          3|          4|          1|          1|          1|          1|          4|          3|          2|          2|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          1|          3|          3|          3|          3|          3|          2|          2|          2|          3|          4|          3|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          2|          1|          2|          2|          1|          2|          3|          3|          1|          1|          1|          1|          1|          1|          1|          3|          1|          5|          2|         44|         40|          4|          4|          4|          2|          2|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          4|          1|          1|          1|          1|          1|          3|          1|          3|          3|          1|          3|          1|          3|          3|          1|          1|          1|         NA|          3|          3|          1|          5|          4|          5|          5|          5|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          1|          4|          4|          4|          4|          4|          4|          4|          4|          4|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          5|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          4|          3|          4|          4|          4|          4|          2|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          2|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|       7|       8|4211  |3359  |0210  |    -1| 15.58|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      4|      4|      4|    12|        4|        4|        4|       12| 48.10| 64.40| 64.40|         NA|         NA|           NA|         NA|           NA|     1|      NA|      0| 51.63|    40|   120|   200|  1760|       NA|       NA|     NA|     NA| -0.0674|  -1.64|   -1.72|    -0.96|       7|      5| -0.0107|  -1.2613|  1.1793|  0.0426|  0.0895|  -0.1926|  -0.4760|  0.0351|  0.5984| -2.4468|   0.3780|    -1.1725|  -2.2177|  0.6669|     1.8839|    -0.0697|  -1.2720| -1.9892|  1.6762|  -0.6036|  2.0054|   0.0273|  1.8905|  0.2621| -1.4371|    -1.0586|  -1.3162|    0.2632|  0.4100| -2.2640|  1.6052|  -0.7822|  0.0712| -1.4721| -0.8225|  -0.2500|  1.1000|  0.0399|       0.7703|  4.2444|  3.3070|  0.7849|  1.3541|  1.2754|  2.0258|  2.3635|  -1.2188|    -1.3048|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 485.833| 551.896| 544.535| 546.151| 546.013| 535.842| 517.757| 509.575| 534.352|  566.853| 552.457| 570.109| 562.955| 530.835| 532.487| 521.763| 481.840| 540.839| 471.671|  519.829| 519.906| 539.614| 547.041| 554.625| 531.748| 541.801| 510.916| 568.291| 475.206|  497.850|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 451.323| 468.250| 510.586| 531.433| 561.364| 540.507| 511.999| 558.558| 535.366|  413.639| 465.915| 473.691| 499.391| 470.539| 546.244| 527.365| 495.834| 537.913| 554.605|  458.782| 487.449| 506.400| 506.931| 516.703| 569.719| 519.064| 558.043| 578.880| 539.894|  480.368| 537.477| 506.118| 531.372| 500.348| 541.544| 550.238| 554.259| 472.640| 492.549|  512.635| 479.120| 517.907| 527.877| 481.168| 502.008| 494.766| 535.814| 487.814| 484.203|  523.968| 0.80261|02MAY19:09:49:49 |   NA|
|     792|TUR | 79200001| 79201556|07MS |079200 |TUR0112 |7920000  |    1|         2|          344|          344|           NA|     17|        10|         8|      2002|         2|          1|          2|          2|          2|         NA|          1|          2|          1|          2|         NA|          1|          1|          1|          1|          2|          1|          1|          2|          2|          1|          1|          1|          2|0792001    |0792002    |0792001    |          2|          3|          2|          4|          2|          1|          1|          1|          2|          1|          1|          1|         NA|          7|          4|          1|          1|          1|          1|          1|          1|          1|          1|          1|          3|          3|          2|          2|          3|          4|          3|          3|          3|          3|          3|          3|          3|          2|          3|          3|          1|          2|          1|          3|          2|          3|          2|          2|          3|          3|          2|          2|          3|          3|          2|          2|          2|          2|          4|          2|          1|          2|          1|          2|          2|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          3|          2|          2|          2|          2|          3|          3|          3|          5|          2|          4|          3|          5|          5|          5|          5|          4|          3|          3|          3|          3|          3|          3|          2|          2|          2|          4|          2|          6|          5|          6|          6|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          4|          2|          2|          2|          1|          1|          1|         NA|          0|          1|          3|          3|          3|          2|          3|          4|          3|          3|          2|          3|          4|          4|          2|          3|          3|          1|          3|          2|          3|          2|          3|          2|          3|          2|          3|          2|          4|          4|          4|          4|          4|          4|          2|          2|          4|          2|          3|          1|          1|          1|          1|          1|          1|          1|          1|         NA|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          1|          1|          1|          1|          2|          2|          2|          2|          2|          2|          2|          1|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          1|          1|          1|          1|          2|          1|          2|          1|          2|          2|          2|          1|          2|          2|          2|          2|          2|          2|          3|          3|          3|          2|          2|          2|          2|          4|          5|          2|          2|         30|         20|          2|          2|          2|          1|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          2|          2|          2|          2|          1|          1|          3|          1|          3|          1|          1|          1|          3|          3|          3|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          5|          5|          6|          1|          1|          3|          3|          1|          1|          1|          1|          1|          3|          3|          3|          3|          3|          3|          3|          3|          3|          4|          4|          4|          4|          4|          4|          4|          4|          4|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          2|          2|          2|          2|          2|          2|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          3|          2|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|         NA|       8|      10|9701  |2149  |2611  |     0| 15.67|07920002 |079200 |079200 |079200 |   344|      3|      1|      1|      4|      6|      6|    16|        4|        6|        6|       16| 17.00| 78.69| 78.69|         NA|         NA|           NA|         NA|           NA|     1|      NA|      0| 86.72|   100|    80|    40|   600|       NA|       NA|     NA|     NA|  0.3978|   0.45|   -1.72|    -1.41|       6|     10| -1.0700|  -1.7393| -0.1357| -1.0005| -1.2275|  -0.5396|  -1.3345| -1.0988|  0.2682| -0.6576|  -0.6200|    -1.4494|  -0.6079|  0.3568|     0.1222|     1.2421|   0.2705| -0.6142| -0.9391|  -0.6583|  0.1956|  -0.1982| -0.2006| -0.0193| -0.5928|     2.3693|  -0.9149|   -2.7142| -3.4472| -0.2014|  0.2865|   0.1686|  0.2165| -1.4721| -0.1577|   0.2910|  0.5881|  0.2243|      -0.7823| -0.9501| -0.0861|  0.7849| -1.2900|  0.0537|  0.0979|  0.5149|   0.2080|     1.1397|      NA|       NA|       NA|       NA|       NA|       NA|       NA|      NA|      NA|       NA|       NA|      NA|       NA|      NA|       NA|       NA|      NA|      NA| 142.0572|    71.0286|   213.0858|    71.0286|   213.0858|    71.0286|    71.0286|    71.0286|    71.0286|   213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|     71.0286|    213.0858|    213.0858|    213.0858|    213.0858|     71.0286|     71.0286|    213.0858|     71.0286|     71.0286|    213.0858|    213.0858|     71.0286|     71.0286|     71.0286|     71.0286|    213.0858|    2|        3| 450.910| 448.120| 394.473| 460.198| 454.828| 449.245| 489.145| 476.646| 505.314|  507.013| 441.286| 415.682| 406.586| 437.001| 473.036| 416.363| 427.909| 471.902| 419.949|  439.851| 453.525| 440.738| 459.294| 471.902| 465.314| 488.763| 465.500| 487.284| 474.574|  457.588|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|      NA|       NA| 481.527| 376.670| 396.524| 524.728| 438.520| 429.856| 416.504| 430.541| 467.738|  431.698| 491.194| 457.365| 446.866| 529.190| 447.829| 494.859| 471.574| 475.993| 477.110|  488.957| 510.438| 444.392| 428.712| 530.462| 448.440| 449.362| 469.799| 465.111| 468.271|  484.944| 502.328| 434.123| 528.107| 424.583| 467.751| 437.751| 488.107| 442.279| 452.980|  491.581| 453.225| 486.874| 502.363| 457.223| 505.248| 487.735| 469.526| 474.984| 448.720|  541.895| 0.80261|02MAY19:09:49:49 |   NA|

</div>
- Veri seti 6890 gözlem ve 1119 değişken içermektedir. 

- Grafiklerle iyi bilinen **ggplot2** paketi grafikleri üzerinden işleyeceğiz.

- **ggplot2** paketindeki grafikler genellikle daha iyi bir görünüme sahiptir ancak daha gelişmiş kodlama becerileri gerektirir (daha fazla bilgi edinmek için "Graphics in R with ggplot2" makalesine bakın). 

- Grafiklerinizi yayınlamanız veya paylaşmanız gerekiyorsa, mümkünse **ggplot2** kullanmanızı öneririm, aksi takdirde varsayılan grafikler işinizi görecektir.

:::{.info data-latex=""}
İpucu: Yakın zamanda **esquisse** eklentilerinden ggplot2 oluşturucusunu keşfettim. Kendiniz kodlamak zorunda kalmadan **ggplot2** paketinden nasıl kolayca grafik çizebileceğinizi görün.
:::

- Bu sayfa görüntülenen tüm grafikler özelleştirilebilir. Örneğin, başlığı, x ve y ekseni etiketlerini, rengi vb. düzenlemek mümkündür. 


```r
library(ggplot2)
ggplot(PISA_STU_2018,aes(x=PV1READ)) + geom_histogram()
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-2-1.png" width="100%" style="display: block; margin: auto;" />

### Minimum and maximum

- `min()` ve `max()` fonksiyonları sayesinde minimum ve maksimum bulunabilir:


```r
min(PISA_STU_2018$PV1READ)
```

```
## [1] 175.608
```



```r
max(PISA_STU_2018$PV1READ)
```

```
## [1] 771.508
```

- Alternatif olarak `range()` fonksiyonu: size doğrudan minimum ve maksimum değerleri verir. `range()` fonksiyonunun çıktısının aslında minimum ve maksimum değerleri (bu sırayla) içeren bir nesne olduğuna dikkat edin. Bu, aslında minimuma şu şekilde erişebileceğiniz anlamına gelir:


```r
range(PISA_STU_2018$PV1READ)[1]
```

```
## [1] 175.608
```

### Ortalama

Ortalama, `mean()` fonksiyonu ile hesaplanabilir:


```r
mean(PISA_STU_2018$PV1READ)
```

```
## [1] 464.2299
```

:::{.info data-latex=""}
İpuçları:

- Veri setinizde en az bir eksik değer varsa, ortalamayı NA hariç tutarak hesaplamak için `mean(PISA_STU_2018$PV1READ, na.rm = TRUE)` kullanın. Bu argüman sadece ortalama için değil, R'da sunulan çoğu fonksiyon için kullanılabilir.
- Kırpılmış  bir ortalama için `mean(PISA_STU_2018$PV1READ, trim = 0.10)` kullanın ve trim bağımsız değişkenini ihtiyaçlarınıza göre değiştirin.:::


### Medyan

- Medyan, `median()` fonksiyonu sayesinde hesaplanabilir:


```r
median(PISA_STU_2018$PV1READ)
```

```
## [1] 463.403
```

- veya quantile() fonksiyonu ile:


```r
quantile(PISA_STU_2018$PV1READ, 0.5)
```

```
##     50% 
## 463.403
```

## I. ve III. Çeyrek

- Medyan gibi, birinci ve üçüncü çeyrekler de `quantile()` işlevi sayesinde ve ikinci bağımsız değişkenin 0.25 veya 0.75 olarak ayarlanmasıyla hesaplanabilir:


```r
quantile(PISA_STU_2018$PV1READ, 0.25) # birinci çeyrek
```

```
##      25% 
## 402.5635
```


```r
quantile(PISA_STU_2018$PV1READ, 0.75) # ücüncü çeyrek
```

```
##      75% 
## 525.7188
```

### Standart sapma ve varyans

- Standart sapma ve varyans `sd()` ve `var()` fonksiyonları ile hesaplanır:


```r
sd(PISA_STU_2018$PV1READ) # standard deviation
```

```
## [1] 87.78006
```


```r
var(PISA_STU_2018$PV1READ) # standard deviation
```

```
## [1] 7705.339
```

- İstatistik dersinden, standart sapma ve varyansın bir örneklem veya popülasyon için hesaplanmasının farklı olduğunu hatırlayın (örneklem ve popülasyon arasındaki farka bakın). R'de standart sapma ve varyans, veriler bir örneklem temsil ediyormuş gibi hesaplanır. 



:::{.info data-latex=""}
İpucu: Birden fazla değişkenin standart sapmasını (veya varyansını) aynı anda hesaplamak için, ikinci bağımsız değişken olarak uygun istatistiklerle birlikte lapply() fonksiyonu ile kullanın
:::


```r
library(dplyr)
PISA_STU_2018 %>% 
  select(starts_with("PV") & ends_with("READ")) %>%
  lapply(.,sd)
```

```
## $PV1READ
## [1] 87.78006
## 
## $PV2READ
## [1] 87.696
## 
## $PV3READ
## [1] 87.07692
## 
## $PV4READ
## [1] 87.40305
## 
## $PV5READ
## [1] 87.21323
## 
## $PV6READ
## [1] 88.08828
## 
## $PV7READ
## [1] 87.45377
## 
## $PV8READ
## [1] 86.65004
## 
## $PV9READ
## [1] 87.56395
## 
## $PV10READ
## [1] 87.37984
```

### Tüm özet istatistikler


```r
summary(PISA_STU_2018$PV1READ)
```

```
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   175.6   402.6   463.4   464.2   525.7   771.5
```

:::{.info data-latex=""}
İpucu: Bu tanımlayıcı istatistikleri gruba göre hesaplamak istiyorsanız `by()` fonksiyonunu kullanın:
:::



```r
by(PISA_STU_2018$PV1READ, PISA_STU_2018$IMMIG, summary)
```

```
## PISA_STU_2018$IMMIG: 1
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   175.6   404.7   465.4   465.8   526.9   771.5 
## ------------------------------------------------------------ 
## PISA_STU_2018$IMMIG: 2
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   310.7   425.5   462.7   473.4   529.5   645.1 
## ------------------------------------------------------------ 
## PISA_STU_2018$IMMIG: 3
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   353.9   401.8   417.5   438.1   458.2   597.6
```

```r
by(PISA_STU_2018$PV1READ, PISA_STU_2018$ST004D01T, summary)
```

```
## PISA_STU_2018$ST004D01T: 1
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   236.4   418.2   477.6   478.1   536.9   771.5 
## ------------------------------------------------------------ 
## PISA_STU_2018$ST004D01T: 2
##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##   175.6   387.5   448.0   450.7   512.2   747.5
```

- `lapply()` kullanımında bağımsız değişkenler veri setinin adı, gruplama değişkeni ve özet fonksiyonudur. Bu sırayı takip edin veya bu sırayı takip etmiyorsanız argümanların adını belirtin.

- Daha açıklayıcı istatistiklere ihtiyacınız varsa, **psych** paketindeki `describe()` fonksiyonunu kullanın:


```r
library(psych)
describe(PISA_STU_2018 %>% 
  select(ESCS,JOYREAD))
```

<div class="kable-table">

|        | vars|    n|       mean|        sd|  median|    trimmed|       mad|     min|    max|  range|      skew|   kurtosis|        se|
|:-------|----:|----:|----------:|---------:|-------:|----------:|---------:|-------:|------:|------:|---------:|----------:|---------:|
|ESCS    |    1| 6855| -1.1712529| 1.1780688| -1.3002| -1.2071859| 1.2613961| -4.7546| 2.7617| 7.5163| 0.2536074| -0.6420796| 0.0142288|
|JOYREAD |    2| 6821|  0.6831396| 0.9756913|  0.6380|  0.6509309| 0.8800714| -2.7316| 2.6574| 5.3890| 0.1236214|  0.2237748| 0.0118138|

</div>
### Değişkenlik katsayısı

- Değişkenlik katsayısı `stat.desc()` ile veya manuel olarak hesaplanarak bulunabilir (Değişkenlik katsayısının standart sapmanın ortalamaya bölünmesi olduğunu unutmayın):



```r
library(pastecs)
round(stat.desc(PISA_STU_2018 %>% 
  select(ESCS,JOYREAD)),2)
```

<div class="kable-table">

|             |     ESCS| JOYREAD|
|:------------|--------:|-------:|
|nbr.val      |  6855.00| 6821.00|
|nbr.null     |     0.00|    0.00|
|nbr.na       |    35.00|   69.00|
|min          |    -4.75|   -2.73|
|max          |     2.76|    2.66|
|range        |     7.52|    5.39|
|sum          | -8028.94| 4659.70|
|median       |    -1.30|    0.64|
|mean         |    -1.17|    0.68|
|SE.mean      |     0.01|    0.01|
|CI.mean.0.95 |     0.03|    0.02|
|var          |     1.39|    0.95|
|std.dev      |     1.18|    0.98|
|coef.var     |    -1.01|    1.43|

</div>


### Mod

- Bildiğim kadarıyla bir değişkenin modunu bulmak için bir fonksiyon yok. Ancak `table()` ve `sort()` fonksiyonları sayesinde bunu kolayca bulabiliriz:


```r
tab <- table(PISA_STU_2018$MISCED) # her benzersiz değer için oluşum sayısı
```


```r
sort(tab, decreasing = TRUE) # en yüksekten en düşüğe doğru sırala
```

```
## 
##    1    2    6    5    0    4    3 
## 1882 1362  887  759  695  675  575
```

- `table()` her bir benzersiz değer için oluşum sayısını verir, ardından `sort() decreasing  = TRUE` argümanı ile oluşum sayısını en yüksekten en düşüğe doğru görüntüler. 

```r
sort(table(PISA_STU_2018$MISCED), decreasing = TRUE)
```

```
## 
##    1    2    6    5    0    4    3 
## 1882 1362  887  759  695  675  575
```

## Frekans tablosu oluşturma

- Herhangi bir ek işlem (yani veri işleme) yapmadan içe aktarılan veri setini kullanarak örneklemimizin demografik özellikleri hakkında bazı temel tanımlayıcı bilgileri hesaplayabilir ve çizebilirsiniz. Aşağıdaki kod, boru olarak da bilinen %>% operatörünü kullanır ve "ve sonra" olarak çevrilebilir. Örneğin, aşağıdaki kod şu şekilde okunabilir:

    - Veri kümesi PISA_STU_2018 ile başlayın ve ardından;
    
    - Değişken MISCED (anne eğitim) göre gruplayın ve ardından;
    
    - Her gruptaki gözlemlerin sayısını sayın ve ardından;
    
    - Gruplandırmayı kaldırın

```r
PISA_STU_2018 %>%
  group_by(MISCED) %>%
  count() %>%
  ungroup()
```

<div class="kable-table">

| MISCED|    n|
|------:|----:|
|      0|  695|
|      1| 1882|
|      2| 1362|
|      3|  575|
|      4|  675|
|      5|  759|
|      6|  887|
|     NA|   55|

</div>

- `group_by()` fonkisyonu veri setinin yüzey düzeyinde değişikliklere neden olmaz, bunun yerine temel yapıyı değiştirir, böylece gruplar belirtilirse, daha sonra çağrılan fonkisyonlar gruplama değişkeninin her düzeyinde ayrı ayrı gerçekleştirilir. Bu gruplama oluşturulan nesnede kalır, bu nedenle nesne üzerinde gelecekte yapılacak işlemlerin gruplar tarafından bilinmeden gerçekleştirilmesini önlemek için `ungroup()` ile kaldırılması önemlidir.

- Bu nedenle yukarıdaki kod, MISCED değişkeninin her bir grubundaki gözlem sayısını sayar. Eğer sadece toplam gözlem sayısına ihtiyacınız varsa, group_by() ve ungroup() satırlarını kaldırabilirsiniz, böylece işlemi gruplar yerine tüm veri seti üzerinde gerçekleştirebilirsiniz:

- Benzer şekilde, örneklemin ortalama başarısını (ve SD'sini) hesaplamak isteyebiliriz ve bunu dplyr/tidyverse paketindeki `summarise()` fonkisyonu kullanarak yapabiliriz.


```r
PISA_STU_2018 %>%
  summarise(ort = mean(PV1READ),
            sd = sd(PV1READ),
            n = n())
```

<div class="kable-table">

|      ort|       sd|    n|
|--------:|--------:|----:|
| 464.2299| 87.78006| 6890|

</div>

- Bu kod, başarı ortalamasının hesaplanmasının sonucunu içeren ort adlı bir sütun biçiminde özet veriler üretir. Daha sonra aynı işlemi standart sapma için yapan sd sütununu oluşturur. Son olarak, istatistiği hesaplamak için kullanılan değerlerin sayısını n adlı bir sütuna eklemek için `n()` fonksiyonu kullanır.

- Yukarıdaki kodun bu işlemin sonucunu kaydetmeyeceğini, sadece konsolda çıktısını vereceğini unutmayın. İleride kullanmak üzere kaydetmek isterseniz, <- notasyonunu kullanarak bir nesnede saklayabilir ve daha sonra nesne adını yazarak yazdırabilirsiniz.

- Son olarak, `group_by()` fonksiyonu özet istatistikleri hesaplarken aynı şekilde çalışacaktır 

- `group_by()` fonksiyonundan  sonra çağrılan işlevin çıktısı gruplama değişkeninin her düzeyi için üretilecektir.


## Görselleştirme

![](images\v1.PNG)


![](images\v2.PNG)

- Grafikler bir **veri kümesini anlamamıza yardımcı olur ve örüntüyü yorumlayabilmek** önemli bir araçtır.

- Grafikler veriyi betimlemek amacıyla kullanılır. 


- Garfiklerin olabildiğince ayrıntı içermesine bunu yaparken de ayrıntıların ne kadarına yorumlayabileceğinize odaklanın.

- Grafikleri sunarken editoryal kararlar gereklidir. Vurgulamak istediğiniz temel özellikleri vurgulayın. Gereksiz ayrıntıları ortadan kaldırın.

- Grafik sistemleri

    - **Base:** öğrenmesi en kolay olan
    
    - **Grid:** diğer araçları geliştirmek için güçlü moduller
    
    - **lattice:** gridler üzerine kurulu genel amaçlı grafikler
    
    - **ggplot2:** grafiklerin grammeri

- `tidyverse` paketi veri düzenlemeleri, görselleştirmeleri, modellemeleri kolay bir şekilde yapabilmemizi sağlayan, R'ın birçok paketini içinde bulunduran pakettir. Bu paketin içeriğinde veri görselleştirme amacıyla `ggplot2` paketi de yer almaktadır.


```r
# install.packages("tidyverse", repos="https://cran.rstudio.com")
library("tidyverse")
library(expss)
```

- Grafikler oluşturulurken, genellikle birden fazla değişkene ilişkin gözlemlerin yer aldığı veri setleri kullanılır.

- Grafiklerin kolay okunması adına `PISA_OGR_2018`  veri setinden veri sayısının azaltılması amacıyla sınıf düzeylerine ilişkin değişkenin her düzeyinden 15'şer kişilik örneklem seçilip toplam 60 gözlemle "df1" nesnesi oluşturulmuştur. 

- Grafik çizimlerinde grup değişkenlerine ihtiyaç duyulduğu için sınıf düzeylerine ve cinsiyete ilişkin değişkenler `as.factor()`fonksiyonuyla kategorik hale getirilmiştir.



```r
load("import/PISA_OGR_2018.rda")
df1 <- PISA_OGR_2018 %>%
dplyr::select(SINIF,CINSIYET,OK_YETERLIK,ODOKUMA1,starts_with("ST097"))  %>%   na.omit()%>%
 expss::drop_var_labs() 

head(df1)
```

<div class="kable-table">

| SINIF| CINSIYET| OK_YETERLIK| ODOKUMA1| ST097Q01TA| ST097Q02TA| ST097Q03TA| ST097Q04TA| ST097Q05TA|
|-----:|--------:|-----------:|--------:|----------:|----------:|----------:|----------:|----------:|
|    10|        2|     -0.6712|  376.022|          1|          2|          1|          1|          1|
|    10|        2|      1.2374|  512.316|          3|          2|          3|          3|          3|
|    10|        1|     -0.4089|  396.383|          2|          3|          3|          3|          3|
|     9|        2|     -0.8250|  393.006|          2|          2|          3|          1|          1|
|     9|        2|      1.8839|  552.457|          3|          3|          4|          3|          1|
|    10|        2|      0.1222|  441.286|          3|          3|          2|          2|          3|

</div>


```r
df2 <- df1 %>% 
  drop_var_labs() %>% 
  filter(SINIF %in%c(8,9,10,11))%>% 
  group_by(SINIF)%>%
  sample_n(15, replace=TRUE) %>%
    ungroup()%>%  
  mutate(SINIF=as.factor(SINIF), CINSIYET=as.factor(CINSIYET)) 
```






## ggplot

-   **ggplot2** paketi, **lattice** paketi gibi verilerdeki birden çok değişkeni aynı grafik üzerinde göstermek ve veriler arasındaki çok düzeyli ilişkileri özetlemek amacıyla geliştirilmiştir.

-   Açılımı grafiğin grameri (grammer of graphics) şeklindedir.

-   **lattice** grafiklerindeki gibi grafikler nesneler olarak kaydedilmekte ve birden çok grafiği tek bir grafiğin üzerinde gösterebilmektedir.

-   **lattice** paketine göre en önemli farkı **katman** mantığıyla çalışmasıdır.
      -   Metin ekleme,
      -   renklendirme,
      -   açıklama kutucukları vb... özelleştirmeler toplama **(+)** işareti ile kodlara eklenebilmektedir.


- **ggplot2** paketnde  Temel Fonksiyonların Kullanımı aşağıdaki şekildedir.
      
      -   **qplot()** ve **ggplot()** fonksiyonları
      -   **qplot()**, hızlı grafik (quick plot) çizimi anlamına gelmektedir.
      
        -   **qplot(x, y, data, geom)** veya
      
        -   **ggplot(x, y, data, geom)** veya
      
        -   **ggplot( data, aes(x, y)) + geom.grafikismi()**

-   **aes()** her bir değişkenin alacağı rolü belirlemede kullanılır.

-   **geom()** argümanı çizilecek grafiği türünü belirlemek için kullanılmaktadır. Geometrik nesneler (geometric objects) olarak adlandırılmaktadır.

- Örneğin **yoğunluk grafiği** çizilmek istendiğinde; 

  - **ggplot(x, y, data, geom="density")** veya  
  
  - **ggplot( data, aes(x, y)) + geom.density()**


- ggplot2 paketinde yer alan tüm grafikler aşağıda listelenmiştir.


```r
library(ggplot2)
ls(pattern = '^geom_', env = as.environment('package:ggplot2'))
```

```
##  [1] "geom_abline"            "geom_area"              "geom_bar"              
##  [4] "geom_bin_2d"            "geom_bin2d"             "geom_blank"            
##  [7] "geom_boxplot"           "geom_col"               "geom_contour"          
## [10] "geom_contour_filled"    "geom_count"             "geom_crossbar"         
## [13] "geom_curve"             "geom_density"           "geom_density_2d"       
## [16] "geom_density_2d_filled" "geom_density2d"         "geom_density2d_filled" 
## [19] "geom_dotplot"           "geom_errorbar"          "geom_errorbarh"        
## [22] "geom_freqpoly"          "geom_function"          "geom_hex"              
## [25] "geom_histogram"         "geom_hline"             "geom_jitter"           
## [28] "geom_label"             "geom_line"              "geom_linerange"        
## [31] "geom_map"               "geom_path"              "geom_point"            
## [34] "geom_pointrange"        "geom_polygon"           "geom_qq"               
## [37] "geom_qq_line"           "geom_quantile"          "geom_raster"           
## [40] "geom_rect"              "geom_ribbon"            "geom_rug"              
## [43] "geom_segment"           "geom_sf"                "geom_sf_label"         
## [46] "geom_sf_text"           "geom_smooth"            "geom_spoke"            
## [49] "geom_step"              "geom_text"              "geom_tile"             
## [52] "geom_violin"            "geom_vline"
```


## Saçılım Grafiği

- Aşağıdaki kod sadece ilk katmanı oluşturur.


```r
grafik_1 <- ggplot(df1, aes(x=ODOKUMA1))
grafik_1 
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-26-1.png" width="80%" style="display: block; margin: auto;" />

### Katman eklenmesi


```r
grafik_1 + geom_histogram()
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-27-1.png" width="50%" style="display: block; margin: auto;" />

###  Yüzey eklenmesi




```r
grafik_1 +
  geom_histogram()  +
  facet_wrap(~CINSIYET, nrow=2)
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-28-1.png" width="50%" style="display: block; margin: auto;" />



```r
grafik_1 + 
  geom_histogram() +
   facet_wrap(~SINIF, nrow=2)
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-29-1.png" width="50%" style="display: block; margin: auto;" />

- **facet_grid** fonksiyonu ise hem tek hem de iki değişkenin panellerde gösterimi için 

  - **facet_grid(satırdeğişkeni~sütundeğişkeni)** 
  
  - **facet_grid(satırdeğişkeni~.)** veya     
  
  - **facet_grid(.~sütundeğişkeni)**



- Yüzeyde kategorik değişkenlerin düzeylerini görebilmek için **factor** değişken olarak tanımlamak gerekir.


```r
library(haven)
PISA_OGR_2018 <- 
  PISA_OGR_2018 %>% 
  mutate_if(is.labelled, funs(as_factor(.)))
```


```r
 ggplot(PISA_OGR_2018, aes(x=ODOKUMA1)) +
  geom_histogram()+
  facet_grid(SINIF~CINSIYET)
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-31-1.png" width="80%" style="display: block; margin: auto;" />


- Yüzeylerin sütunda oluşturulması


```r
ggplot(PISA_OGR_2018,aes(x=ODOKUMA1))+
  geom_histogram()+
  facet_grid(.~CINSIYET)
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-32-1.png" width="40%" style="display: block; margin: auto;" />

- Yüzeylerin satırlarda oluşturulması

```r
ggplot(PISA_OGR_2018,aes(x=ODOKUMA1))+
  geom_histogram()+
  facet_grid(CINSIYET~.)
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-33-1.png" width="40%" style="display: block; margin: auto;" />



```r
ggplot(PISA_OGR_2018,aes(x=ODOKUMA1))+
  geom_histogram()+
  facet_grid(.~SINIF)
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-34-1.png" width="100%" style="display: block; margin: auto;" />





```r
ggplot(PISA_OGR_2018,aes(x=ODOKUMA1))+
  geom_histogram()+
  facet_grid(SINIF~.)
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-35-1.png" width="100%" style="display: block; margin: auto;" />


###  gruplama değişkenleri

- Renklendirme, sembol şekli, sembol büyüklüğü ve çizgi türü belirleyen fonksiyonlar yardımıyla gruplama yapılmaktadır.


#### color ile gruplandırma

- Açıklama kutucukları otomatik çıkar!


```r
p1 <- ggplot(
      PISA_OGR_2018 %>% 
      group_by(SINIF,CINSIYET) %>%
      mutate(ort=mean(ODOKUMA1)) %>% ungroup(),
     aes(x=SINIF, y=ort, color=CINSIYET )) +
  geom_point() +  
  xlab("Sınıf Düzeyi")+
  ylab("Ortalama Puan") 

p1
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-36-1.png" width="100%" style="display: block; margin: auto;" />

- Yüzey eklenmiş garfiklerde de gruplama değişkeni kullanılabilir.



```r
ggplot(PISA_OGR_2018,aes(x=ODOKUMA1,y=OK_YETERLIK,color=CINSIYET)) +
  geom_point()+
  facet_grid(.~SINIF)	
```

```
## Warning: Removed 199 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-37-1.png" width="100%" style="display: block; margin: auto;" />


## Grafik nesnesi

- Oluşturulan grafik **p** nesnesine atanmıştır. **p** nesnesine **+** ile katmanlar eklenebilir.
- Kategorik degişkenler eksen değerlerini belirler.



```r
p <- ggplot(mtcars, aes(cyl, mpg)) +
  geom_point()
p
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-38-1.png" width="100%" style="display: block; margin: auto;" />


- cyl değişkenin sadece 4,6 ve 8 değerlerini eksende belirtmek için factor olarak tanımlamak gerekir.


```r
ggplot(mtcars, aes(factor(cyl), mpg)) +
  geom_point()
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-39-1.png" width="100%" style="display: block; margin: auto;" />

- Grafikler üç bölümden oluşur

![](images/v3.PNG)

## **AESTHETICS** 

    -   fill
    -   color
    -   size
    -   shape
    -   alpha
    -   linetype
    -   labels



### **color** parametresi


```r
ggplot(PISA_OGR_2018, aes(CINSIYET, OK_YETERLIK)) +
  geom_point(color = "blue")
```

```
## Warning: Removed 199 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-40-1.png" width="100%" style="display: block; margin: auto;" />

### **size** ve **shape** parametresi

- her iki parametrenin de olağan değeri 1 dir. 

```r
ggplot(PISA_OGR_2018, aes(CINSIYET, OK_YETERLIK)) +
  geom_point(color = "blue",size=5,shape="a")
```

```
## Warning: Removed 199 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-41-1.png" width="100%" style="display: block; margin: auto;" />


- Veri seti her bir okul türünden 5 kişi alınarak veri seti boyutu küçültülmüştür.


```r
df <- PISA_OGR_2018 %>% group_by(OKUL_TUR)%>% sample_n(5) %>% ungroup()

ggplot(df, aes(CINSIYET, OK_YETERLIK, color = SINIF)) +
  geom_point()
```

```
## Warning: Removed 7 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-42-1.png" width="100%" style="display: block; margin: auto;" />


- Üstüse gelen noktalar için **position**

-   identity
-   dodge
-   stack
-   fill
-   jitter
-   jitterdodge
-   nudge



```r
ggplot(df, aes(CINSIYET, OK_YETERLIK, color = SINIF)) +
  geom_point()
```

```
## Warning: Removed 7 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-43-1.png" width="100%" style="display: block; margin: auto;" />



```r
ggplot(df, aes(CINSIYET, OK_YETERLIK, color = SINIF)) +
  geom_point(position = "jitter")
```

```
## Warning: Removed 7 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-44-1.png" width="100%" style="display: block; margin: auto;" />

### **size** parametresi

- parametreler için veri setinden bir değişken değeri seçilebilir.


```r
ggplot(df, aes(CINSIYET, OK_YETERLIK, size = SINIF)) +
  geom_point()
```

```
## Warning: Using size for a discrete variable is not advised.
```

```
## Warning: Removed 7 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-45-1.png" width="100%" style="display: block; margin: auto;" />

- **size** parametresi  üst üste binen noktaları kaydırarak ayırma


```r
ggplot(df, aes(CINSIYET, OK_YETERLIK, size = SINIF)) +
  geom_point(position = "jitter")
```

```
## Warning: Using size for a discrete variable is not advised.
```

```
## Warning: Removed 7 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-46-1.png" width="100%" style="display: block; margin: auto;" />


## Katmanlar

![](images/v4.PNG)

### alpha

- Şeffaflık düzeyi için **alpa**

```r
ggplot(df, aes(ODOKUMA1, OK_YETERLIK, color = SINIF)) +
  geom_point(alpha = 0.4)
```

```
## Warning: Removed 7 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-47-1.png" width="100%" style="display: block; margin: auto;" />

- Katmanları nesneye ekleme
**grafik1** adlı nesneye istenilen katmanlar eklenebilir.


```r
grafik1 <- ggplot(df, aes(ODOKUMA1, OK_YETERLIK, color = SINIF))
grafik1 +geom_point(alpha = 1.2)
```

```
## Warning: Removed 7 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-48-1.png" width="100%" style="display: block; margin: auto;" />


**grafik1** adlı nesneye CINSIYET değişkenine göre şekil ekleme

```r
grafik1 +geom_point(aes(shape=CINSIYET))
```

```
## Warning: Removed 7 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-49-1.png" width="100%" style="display: block; margin: auto;" />


### **text**

Değişken adları **text** komutu ile veri sembolu olarak eklenebilir. Gösterim amacıyla **df** veri setinin sadece ilk 10 satırı kullanılmıştır.


```r
ggplot(df[1:10,], aes(ODOKUMA1, OK_YETERLIK))+
         geom_text(aes(label = CINSIYET))
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-50-1.png" width="100%" style="display: block; margin: auto;" />

### Scale

Scale fonksiyonları
  -   scale_x() 
  -   scale_y() 
  -   scale_color() 
  -   scale_fill() 
  -   scale_shape() 
  -   scale_linetype() 
  -   scale_size() 
  -   scale_x_continuous() 
  -   scale_y() 
  -   scale_color_discrete() 
  -   scale_fill() 
  -   scale_shape() 
  -   scale_linetype() 
  -   scale_size() 



```r
ggplot(df, aes(x = ODOKUMA1,y = OK_YETERLIK, color = CINSIYET)) +
geom_point(position = "jitter") +
scale_x_continuous("Okuma Puanları") +
scale_color_discrete("Cinsiyet")
```

```
## Warning: Removed 7 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-51-1.png" width="100%" style="display: block; margin: auto;" />

### *limits**


```r
ggplot(df, aes(x = ODOKUMA1,
y = OK_YETERLIK,
color = CINSIYET)) +
geom_point(position = "jitter") +
scale_x_continuous("Okuma Puanları",limits = c(100,900)) +
scale_color_discrete("Cinsiyet")
```

```
## Warning: Removed 7 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-52-1.png" width="100%" style="display: block; margin: auto;" />

### *breaks


```r
ggplot(df, aes(x = ODOKUMA1,
y = OK_YETERLIK,
color = CINSIYET)) +
geom_point(position = "jitter") +
scale_x_continuous("Okuma Puanları",limits = c(100,900),
         breaks=seq(100,900,100)) +
scale_color_discrete("Cinsiyet")
```

```
## Warning: Removed 7 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-53-1.png" width="100%" style="display: block; margin: auto;" />


###  expand


```r
ggplot(df, aes(x = ODOKUMA1,
y = OK_YETERLIK,
color = CINSIYET)) +
geom_point(position = "jitter") +
scale_x_continuous("Okuma Puanları",limits = c(100,900),
                   breaks=seq(100,900,100),
                   expand=c(0,0)) +
scale_color_discrete("Cinsiyet")
```

```
## Warning: Removed 7 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-54-1.png" width="100%" style="display: block; margin: auto;" />

### labs


```r
ggplot(df, aes(x = ODOKUMA1,
y = OK_YETERLIK,
color = CINSIYET)) +
geom_point(position = "jitter") +
  labs(x = "\nBasari Puanları",
       y = "\nYeterlik Puanları",
       color = "Grup")
```

```
## Warning: Removed 7 rows containing missing values (`geom_point()`).
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-55-1.png" width="100%" style="display: block; margin: auto;" />

## Bar Grafiği


```r
ggplot(df, aes(CINSIYET, fill = SINIF)) +   geom_bar() +
  labs(x = "Cinsiyet",
       y = "Frekans")
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-56-1.png" width="100%" style="display: block; margin: auto;" />

## scale_fill


```r
ggplot(df, aes(CINSIYET, fill = SINIF)) +
  geom_bar() +
   labs(x = "Cinsiyet",
       y = "Frekans") +
  scale_fill_manual("CINSIYET", values = c("red","blue","orange","green","darkblue"))
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-57-1.png" width="100%" style="display: block; margin: auto;" />



## Bar Grafikleri

```r
dat <- PISA_STU_2018 %>%
  group_by(ST004D01T) %>%
  summarise(ort = mean(PV1READ),
            sd = sd(PV1READ),
            n = n()) %>%
  ungroup()

ggplot(data = PISA_STU_2018, mapping = aes(x = ST004D01T)) +
  geom_bar()
```

```
## Don't know how to automatically pick scale for object of type
## <haven_labelled/vctrs_vctr/double>. Defaulting to continuous.
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-58-1.png" width="100%" style="display: block; margin: auto;" />

```r
dat <- mutate(PISA_STU_2018, Cinsiyet = factor(
  ST004D01T,
  c(1, 2),
  c("kiz", "erkek")
))

ggplot(data = dat, mapping = aes(x = Cinsiyet)) +
  geom_bar()
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-59-1.png" width="100%" style="display: block; margin: auto;" />


```r
ggplot(data = dat, mapping = aes(x = Cinsiyet)) + 
  geom_bar(aes(y = (..count..)/sum(..count..))) + 
  scale_y_continuous(name = "Yüzde", labels=scales::percent) 
```

```
## Warning: The dot-dot notation (`..count..`) was deprecated in ggplot2 3.4.0.
## ℹ Please use `after_stat(count)` instead.
## This warning is displayed once every 8 hours.
## Call `lifecycle::last_lifecycle_warnings()` to see where this warning was
## generated.
```

<img src="15-betimleyici-istatistik_files/figure-html/unnamed-chunk-60-1.png" width="100%" style="display: block; margin: auto;" />








- teşekkürler !

--


- 😕

- 🙋






<!--chapter:end:15-betimleyici-istatistik.Rmd-->

# (APPENDIX) Appendices {-} 

<!--chapter:end:appendix-0.Rmd-->

# Installing `R` {#installing-r}

Installing R and RStudio is usually straightforward. The sections below explain how and [there is a helpful YouTube video here](https://www.youtube.com/watch?v=lVKMsaWju8w){target="_blank"}.

## Installing Base R

[Install base R](https://cran.rstudio.com/){target="_blank"}. Choose the download link for your operating system (Linux, Mac OS X, or Windows).

If you have a Mac, install the latest release from the newest `R-x.x.x.pkg` link (or a legacy version if you have an older operating system). After you install R, you should also install [XQuartz](http://xquartz.macosforge.org/){target="_blank"} to be able to use some visualisation packages.

If you are installing the Windows version, choose the "[base](https://cran.rstudio.com/bin/windows/base/)" subdirectory and click on the download link at the top of the page. After you install R, you should also install [RTools](https://cran.rstudio.com/bin/windows/Rtools/){target="_blank"}; use the "recommended" version highlighted near the top of the list.

If you are using Linux, choose your specific operating system and follow the installation instructions.

## Installing RStudio

Go to [rstudio.com](https://www.rstudio.com/products/rstudio/download/#download){target="_blank"} and download the RStudio Desktop (Open Source License) version for your operating system under the list titled **Installers for Supported Platforms**.

## RStudio Settings

There are a few settings you should fix immediately after updating RStudio. Go to **`Global Options...`** under the **`Tools`** menu (&#8984;,), and in the General tab, uncheck the box that says **`Restore .RData into workspace at startup`**.  If you keep things around in your workspace, things will get messy, and unexpected things will happen. You should always start with a clear workspace. This also means that you never want to save your workspace when you exit, so set this to **`Never`**. The only thing you want to save are your scripts.

You may also want to change the appearance of your code. Different fonts and themes can sometimes help with visual difficulties or [dyslexia](https://datacarpentry.org/blog/2017/09/coding-and-dyslexia){target="_blank"}. 

<div class="figure" style="text-align: center">
<img src="images/rstudio_settings_general_appearance.png" alt="RStudio General and Appearance settings" width="100%" />
<p class="caption">(\#fig:settings-general)RStudio General and Appearance settings</p>
</div>

You may also want to change the settings in the Code tab. Foe example, Lisa prefers two spaces instead of tabs for my code and likes to be able to see the <a class='glossary'>whitespace<span class='def'></span></a> characters. But these are all a matter of personal preference.

<div class="figure" style="text-align: center">
<img src="images/rstudio_settings_code.png" alt="RStudio Code settings" width="100%" />
<p class="caption">(\#fig:settings-code)RStudio Code settings</p>
</div>


## Installing LaTeX

You can install the LaTeX typesetting system to produce PDF reports from RStudio. Without this additional installation, you will be able to produce reports in HTML but not PDF. This course will not require you to make PDFs. To generate PDF reports, you will additionally need to install <code class='package'>tinytex</code> [@R-tinytex] and run the following code:


```r
tinytex::install_tinytex()
```

<!--chapter:end:appendix-a-installing-r.Rmd-->

# Updating R, RStudio, and packages {#appendix-updating-r}

From time-to-time, updated version of R, RStudio, and the packages you use (e.g., ggplot) will become available. Remember that each of these are separate, so they each have a different process and come with different considerations. We recommend updating to the latest version of all three at the start of each academic year.

## Updating RStudio

RStudio is the easiest component to update. Typically, updates to RStudio won't affect your code, instead they add in new features, like spell-check or upgrades to what RStudio can do. There's usually very little downside to updating RStudio and it's easy to do.

Click `Help - Check for updates`

<div class="figure" style="text-align: center">
<img src="images/update_rstudio.jpg" alt="Updating RStudio" width="100%" />
<p class="caption">(\#fig:img-updaterstudio)Updating RStudio</p>
</div>

If an update is available, it will prompt you to download it and you can install it as usual.

## Updating R

Finally, you may also wish to update R itself. The key thing to be aware of is that when you update R, if you just download the latest version from the website, you will lose all your packages. 

### Windows

The easiest way to update R on Windows and not cause yourself a huge headache is to use the `installr` package. When you use the `updateR()` function, a series of dialogue boxes will appear. These should be fairly self-explanatory but there is a [full step-by-step guide available](https://www.r-statistics.com/2015/06/a-step-by-step-screenshots-tutorial-for-upgrading-r-on-windows/) for how to use `installr`, the important bit is to select "Yes" when it asked if you would like to copy your packages from the older version of R.


```r
# Install the installr package
install.packages("installr")

# Run the update function
installR::updateR()
```

### Mac

For a Mac, you can use the <code class='package'><a href='https://github.com/AndreaCirilloAC/updateR' target='_blank'>updateR</a></code> package. You'll need to install this from GitHub. You will be asked to type your system password (that you use to log into your computer) in the console pane. If relevant, it will ask you if you want to restore your packages for a new major version.


```r
# install from github
devtools::install_github("AndreaCirilloAC/updateR")

# update your R version, you will need your system password
updateR::updateR()
```



## Updating packages

Package developers will occasionally release updates to their packages. This is typically to add in new functions to the package, or to fix or amend existing functions. **Be aware that some package updates may cause your previous code to stop working**. This does not tend to happen with minor updates to packages, but occasionally with major updates, you can have serious issues if the developer has made fundamental changes to how the code works. For this reason, we recommend updating all your packages once at the beginning of each academic year (or semester) - don't do it before an assessment or deadline just in case!

To update an individual package, the easiest way is to use the `install.packages()` function, as this always installs the most recent version of the package.


```r
install.packages("tidyverse")
```

To update multiple packages, or indeed all packages, RStudio provides helpful tools. Click `Tools - Check for Package Updates`. A dialogue box will appear and you can select the packages you wish to update. Be aware that if you select all packages, this may take some time and you will be unable to use R whilst the process completes.

<div class="figure" style="text-align: center">
<img src="images/update_packages.jpg" alt="Updating packages with RStudio" width="100%" />
<p class="caption">(\#fig:img-updateall)Updating packages with RStudio</p>
</div>


## Troubleshooting {#package-install-troubleshooting}

Occasionally, you might have a few problem packages that seemingly refuse to update. For me, `rlang` and `vctrs` cause me no end of trouble. These aren't packages that you will likely every explicitly load, but they're required beneath the surface for R to do things like knit your Markdown files etc.

### Non-zero exit status

If you try to update a package and get an error message that says something like `Warning in install.packages : installation of package ‘vctrs’ had non-zero exit status` or perhaps `Error in loadNamespace(i, c(lib.loc, .libPaths()), versionCheck = vI[[i]]) :  namespace 'rlang' 0.4.9 is being loaded, but >= 0.4.10 is required` one solution I have found is to manually uninstall the package, restart R, and then install the package new, rather than trying to update an existing version. The `installr` package also has a useful function for uninstalling packages.


```r
# Load installr
library(installr)

# Uninstall the problem package
uninstall.packages("package_name")

# Then restart R using session - restart R
# Then install the package fresh

install.packages("package")
```

### Cannot open file

You may get the following error after trying to install any packages at all:

> Error in install packages : Cannot open file 'C:/.....': Permission denied

This usually indicates a permissions problem with writing to the default library (the folder that packages are kept in). Sometimes this means that you need to install R and RStudio as administrator or run it as administrator. 

One other fix may be to change the library location using the following code (check in "C:/Program Files/R" for what version you should have instead of "R-3.5.2"):


```r
# change the library path
.libPaths(c("C:/Program Files/R/R-3.5.2/library"))
```

If that works and you can install packages, set this library path permanently:

1. Install the <code class='package'>usethis</code> package
2. Run `usethis::edit_r_profile()` in the console; it will open up a blank file
3. Paste into the file (your version of): `.libPaths(c("C:/Program Files/R/R-3.5.2/library"))`
4. Save and close the file
5. Restart R for changes to take effect

The code in your .Rprofile will now run every time you start up R. 

As always, if you're having issues, please ask on Teams or come to office hours.

<!--chapter:end:appendix-b-updating-r.Rmd-->

# Conventions

This book will use the following conventions:

* Generic code: `list(number = 1, letter = "A")`
* Highlighted code: <code><span><span class='fu'>dplyr</span><span class='fu'>::</span><span class='fu'><a target='_blank' href='https://rdrr.io/pkg/dplyr/man/slice.html'>slice_max</a></span><span class='op'>(</span><span class='op'>)</span></span></code>
* File paths: <code class='path'>data/sales.csv</code>
* R Packages: <code class='package'>tidyverse</code>
* Functions: <code><span><span class='fu'><a target='_blank' href='https://rdrr.io/r/base/paste.html'>paste</a></span><span class='op'>(</span><span class='op'>)</span></span></code>
* Strings: <code><span><span class='st'>"psyTeachR"</span></span></code>
* Numbers: <code><span><span class='fl'>100</span></span></code>, <code><span><span class='fl'>3.14</span></span></code>
* Logical values: <code><span><span class='cn'>TRUE</span></span></code>, <code><span><span class='cn'>FALSE</span></span></code>
* Glossary items: <a class='glossary'>ordinal<span class='def'></span></a>
* Citations: @R-tidyverse
* Internal links: Chapter\ \@ref(inclusion)
* External links: [R for Data Science](https://r4ds.had.co.nz/){target="_blank"}
* Menu/interface options: **`New File...`**

## Webexercises

See [webexercises](https://psyteachr.github.io/webexercises/) for more details about how to use this in your materials.

* Type an integer: <input class='webex-solveme nospaces regex' size='1' data-answer='["^[0-9]{1}$"]'/>
* I am going to learn a lot: <select class='webex-select'><option value='blank'></option><option value='answer'>TRUE</option><option value='x'>FALSE</option></select>
* What is a p-value? <div class='webex-radiogroup' id='radio_WIPBHUUONL'><label><input type="radio" autocomplete="off" name="radio_WIPBHUUONL" value="x"></input> <span>the probability that the null hypothesis is true</span></label><label><input type="radio" autocomplete="off" name="radio_WIPBHUUONL" value="answer"></input> <span>the probability of the observed (or more extreme) data, under the assumption that the null-hypothesis is true</span></label><label><input type="radio" autocomplete="off" name="radio_WIPBHUUONL" value="x"></input> <span>the probability of making an error in your conclusion</span></label></div>


<div class='webex-solution'><button>Hidden Text</button>
You found some hidden text!
</div>


<div class='webex-solution'><button>Hidden Code</button>

```r
print("You found some hidden code!")
```

```
## [1] "You found some hidden code!"
```


</div>

## Alert boxes

::: {.info data-latex=""}
Informational asides.
:::

::: {.warning data-latex=""}
Notes to warn you about something.
:::

::: {.dangerous data-latex=""}
Notes about things that could cause serious errors.
:::

::: {.try data-latex=""}
Try it yourself.
:::

## Code Chunks


```r
# code chunks
paste("Applied", "Data", "Skills", 1, sep = " ")
```

```
## [1] "Applied Data Skills 1"
```


<div class='verbatim'><pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;{r setup, message = FALSE}</code></pre>

```r
# code chunks with visible r headers
library(tidyverse)
```

<pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;</code></pre></div>

## Glossary

<table class="table" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> term </th>
   <th style="text-align:left;"> definition </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> ordinal </td>
   <td style="text-align:left;">  </td>
  </tr>
</tbody>
</table>



<!--chapter:end:appendix-c-conventions.Rmd-->

# Glossary

You can use the `glossary()` function to automatically link to a term in the [psyTeachR glossary](https://psyteachr.github.io/glossary/) or make your own project-specific glossary.

This will create a link to the glossary and include a tooltip with a short definition when you hover over the term. Use the following syntax in inline r: `glossary("word")`. For example, common <a class='glossary'>data types<span class='def'></span></a> are <a class='glossary'>integer<span class='def'></span></a>, <a class='glossary'>double<span class='def'></span></a>, and <a class='glossary'>character<span class='def'></span></a>.

If you need to link to a definition, but are using a different form of the word, add the display version as the second argument (`display`). You can also override the automatic short definition by providing your own in the third argument (`def`). Add the argument `link = FALSE` if you just want the hover definition and not a link to the psyTeachR glossary.


```r
# glossary("data type", 
#          display = "Data Types", 
#          def = "My custom definition of data types", 
#          link = FALSE)
```

You can add a glossary table to the end of a chapter with the following code. It creates a table of all terms used in that chapter previous to the `glossary_table()` function. It uses `kableExtra()`, so if you use it in a code chunk, set `results='asis'`.

<div class='verbatim'><pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;{r, echo=FALSE, results='asis'}</code></pre>

```r
glossary_table()
```

<pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;</code></pre></div>

<table class="table" style="margin-left: auto; margin-right: auto;">
 <thead>
  <tr>
   <th style="text-align:left;"> term </th>
   <th style="text-align:left;"> definition </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> character </td>
   <td style="text-align:left;">  </td>
  </tr>
  <tr>
   <td style="text-align:left;"> data type </td>
   <td style="text-align:left;">  </td>
  </tr>
  <tr>
   <td style="text-align:left;"> double </td>
   <td style="text-align:left;">  </td>
  </tr>
  <tr>
   <td style="text-align:left;"> integer </td>
   <td style="text-align:left;">  </td>
  </tr>
</tbody>
</table>



If you want to contribute to the glossary, fork the [github project](https://github.com/PsyTeachR/glossary), add your terms and submit a pull request, or suggest a new term at the [issues page](https://github.com/PsyTeachR/glossary/issues).

<!--chapter:end:appendix-d-glossary.Rmd-->

# License {-}

This book is licensed under Creative Commons Attribution-ShareAlike 4.0 International License [(CC-BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/){target="_blank"}. You are free to share and adapt this book. You must give appropriate credit [@psyteachr-template], provide a link to the license, and indicate if changes were made. If you adapt the material, you must distribute your contributions under the same license as the original. 





<!--chapter:end:appendix-y-license.Rmd-->

# References {-}

<!--chapter:end:appendix-z-refs.Rmd-->

