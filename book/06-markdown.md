# Markdown

Bu bölümde kullanacağımız paketler şunlardır.


```r
knitr::opts_chunk$set(message = FALSE, warning = FALSE)
# bu bölüm için gerekli paketler
library(tidyverse) # çeşitli veri manipülasyon fonksiyonları
library(knitr) # tablo ve görüntü gösterimi için
library(kableExtra) # tabloları şekillendirmek için
library(papaja) # APA tarzı tablolar için
library(gt) # süslü tablolar için
library(DT) # etkileşimli tablolar için
```

🔗İndir [R Markdown Cheat Sheet](https://www.rstudio.org/links/r_markdown_cheat_sheet).

🔗İndir [R Markdown Cheat Sheet TURKCE](https://www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf)

::: {.try data-latex=""}
🔗[R markdon sunusu](https://atalay-k.github.io/OLC750/sunu/T_Dokumantasyon.html#1)
:::

::: {.try data-latex=""}
🔗[markdown hatırlatıcı notlar](https://www.markdownguide.org/cheat-sheet/)
:::

## Neden tekrarlanabilir raporlar kullanılmalı?

Bir rapor hazırladığınızı düşünün

-   içinde analiz sonuçları olan tablolar

-   grafikler ve görsel olsun

-   bu raporu güncellemeniz gerektiğinde veri seti, grafikler, analizler başka dizinlerde olabilir.

-   Tekrarlanabilir raporlar, tüm analizleri gerçekleştirmek ve tabloları oluşturmak için gereken kodla birlikte rapor metnini tek bir belgede bir araya getirmektir.

-   Bu, başlangıçta biraz fazladan çaba gerektirse de, herhangi bir değişiklik olduğunda tek bir düğmeye basarak tüm raporunuzu güncellemenizi sağlayarak size fazlasıyla geri ödeme yapacaktır.

-   Araştırmalar ayrıca, bilimsel literatürdeki makalelerin çoğunda olmasa bile birçoğunda raporlama hataları olduğunu göstermektedir. Tekrarlanabilir raporlar, transkripsiyon ve yuvarlama hatalarını önlemeye yardımcı olur.

-   Rapor daha sonra orijinal formattan HTML, word ve ya PDF gibi daha taşınabilir başka bir formata "derlenir". Bu, örneğin Microsoft Excel'de veya SPSS gibi bir istatistik programında bir grafik oluşturup ardından bunu Microsoft Word'e yapıştırdığınız geleneksel kesme ve yapıştırma yaklaşımlarından farklıdır.

## Bir proje düzenlemek

-   İlk olarak, organize olmamız gerekiyor. RStudio'daki projeler, bir proje için ihtiyaç duyduğunuz tüm dosyaları gruplandırmanın bir yoludur. Çoğu proje komut dosyalarını, veri dosyalarını ve komut dosyası veya görüntüler tarafından oluşturulan PDF raporu gibi çıktı dosyalarını içerir.

### Dosya Sistemi

-   Bilgisayarınızın dosya sistemi, hem dosyaları hem de "alt dizinleri" içeren büyük dizin gibidir. Bir dosyanın konumunu adıyla ve içinde bulunduğu tüm dizinlerin adlarıyla belirtebilirsiniz.

-   Örneğin, Kubra Masaüstünde report.Rmd adında bir dosya arıyorsa, tam dosya yolunu şu şekilde belirtebilir: **/Users/Kubra/Desktop/report.Rmd** , çünkü Masaüstü dizini, tüm dosya sisteminin tabanında bulunan Kullanıcılar/Users dizininin içindeki Kubra dizininin içindedir. Bu dosya masaüstünüzde olsaydı, kullanıcı dizininizin adı da Kubra değilse muhtemelen farklı bir yola sahip olurdunuz. Şu anda oturum açmış olan kişinin kullanıcı dizinini temsil etmek için \~ kısayolunu da kullanabilirsiniz: **\~/Desktop/report.Rmd.**

### Çalışma Dizini

-   Tüm dosyalarınızı nereye koymalısınız? Genellikle tek bir proje için tüm komut dosyalarınızın ve veri dosyalarınızın bilgisayarınızdaki tek bir klasörde, o projenin çalışma dizininde olmasını istersiniz. Dosyaları bu ana proje dizini içindeki alt dizinlerde düzenleyebilirsiniz, örneğin tüm ham veri dosyalarını **data/import** adlı bir dizine koyabilir ve tüm görüntü dosyalarını **images** adlı bir dizine kaydedebilirsiniz.

-   Kodunuz, uygun biçimi kullanarak yalnızca üç tür konumdaki dosyalar kullanılmalıdır.

| Yer              | Örnek                                                  |
|--------------------------------|----------------------------------------|
| web              | "<https://atalay-k.github.io/OLC731/import/veri1.txt>" |
| dizin içinde     | "veri1.txt"                                            |
| alt dizin içinde | "import/veri1.txt"                                     |

::: {.warning data-latex=""}
Bir komut dosyasında asla çalışma dizininizi ayarlamayın veya değiştirmeyin.
:::

-   R Markdown dosyaları otomatik olarak **.Rmd** dosyasının bulunduğu dizini çalışma dizini olarak kullanacaktır.

-   Kodunuz çalışma dizininizin bir alt dizinindeki bir dosyaya ihtiyaç duyuyorsa (örneğin, import/veri1.txt), çalışma dizinini başka bir konuma veya bilgisayara taşıdığınızda erişilebilir olması için dosyayı göreli bir yol kullanarak yükleyin:


```r
dat <- read.table("import/veri1.txt")  # dogru
```

Bu dosyayı aşağıdaki gibi mutlak yol/adres ile yüklemeyin:


```r
dat <- read.table("c:/Users/Kubra/Desktop/OLC731/import/veri1.txt")  # yanlıs
```

-   Örnek veriyi düzgün aktarmak aşağıdaki kodla sağlanır.


```r
(veri1 <- read.table("import/veri1.txt",
                    header= TRUE,
                    sep= ";",
                    dec= ","))
```

<div class="kable-table">

<table>
 <thead>
  <tr>
   <th style="text-align:right;"> no </th>
   <th style="text-align:right;"> m_1 </th>
   <th style="text-align:right;"> m_2 </th>
   <th style="text-align:right;"> m_3 </th>
   <th style="text-align:right;"> m_4 </th>
   <th style="text-align:right;"> m_5 </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 522 </td>
   <td style="text-align:right;"> 12 </td>
   <td style="text-align:right;"> 14.0 </td>
   <td style="text-align:right;"> 16 </td>
   <td style="text-align:right;"> 20.0 </td>
   <td style="text-align:right;"> 10 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 222 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> NA </td>
   <td style="text-align:right;"> 20 </td>
   <td style="text-align:right;"> 10.0 </td>
   <td style="text-align:right;"> 10 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 454 </td>
   <td style="text-align:right;"> 5 </td>
   <td style="text-align:right;"> 10.2 </td>
   <td style="text-align:right;"> 6 </td>
   <td style="text-align:right;"> 4.0 </td>
   <td style="text-align:right;"> 10 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 567 </td>
   <td style="text-align:right;"> 10 </td>
   <td style="text-align:right;"> 20.0 </td>
   <td style="text-align:right;"> NA </td>
   <td style="text-align:right;"> 12.2 </td>
   <td style="text-align:right;"> 20 </td>
  </tr>
</tbody>
</table>

</div>

::: {.info data-latex=""}
Ayrıca, Windows'a özgü geriye doğru eğik çizgi kullanma kuralının aksine, ileriye doğru eğik çizgi kullanma kuralına dikkat edin. Bu, dosyalara yapılan referansların işletim sistemlerinden bağımsız olarak herkes için çalışmasını sağlamak içindir.
:::

### Nesneleri Adlandırma

Dosyaları, hem insanların hem de bilgisayarların kolayca bulabileceği şekilde adlandırın. İşte bazı önemli ilkeler:

-   dosya ve dizin adları yalnızca harf, rakam, tire ve alt çizgi içermeli, dosya adı ve uzantısı arasında nokta (.) olmalıdır (bu boşluk olmadığı anlamına gelir!)
-   Büyük harf kullanımı konusunda tutarlı olun (hatırlamayı kolaylaştırmak için bir kural belirleyin, örneğin her zaman küçük harf kullanın)
-   dosya adının bölümlerini ayırmak için alt çizgi (\_) ve bir bölümdeki sözcükleri ayırmak için tire (-) kullanın
-   dosyaları mantıklı bir sırayla alfabetik hale getiren ve aradığınız dosyayı bulmanızı kolaylaştıran bir kalıpla adlandırın
-   bir dosya adını listenin en üstüne taşımak için önüne alt çizgi ekleyin veya sıralarını kontrol etmek için tüm dosyaların önüne sayı ekleyin
-   tarihler için YYYY-MM-DD biçimini kullanın, böylece kronolojik sıraya göre sıralanırlar

Örneğin, bu dosya adları tam bir karmaşa:

-   <code class='path'>Veri (Katilimci) 04-15.xls</code>
-   <code class='path'>final raporu2.doc</code>
-   <code class='path'>Katilimci Veri Nisan 12.xls</code>
-   <code class='path'>proje notlari</code>
-   <code class='path'>Anket Veri Kasim 15.xls</code>
-   <code class='path'>rapor.doc</code>
-   <code class='path'>rapor son.doc</code>

Benzer dosyaların aynı yapıya sahip olması ve dosyaları taramanın veya ilgili dosyaları bulmak için kod kullanmasının kolay olması için dosyaları yapılandırabilirsiniz.

-   <code class='path'>proje-notlari</code>
-   <code class='path'>veri_katilimci_2021-04-12.xls</code>
-   <code class='path'>veri_katilimci_2021-04-15.xls</code>
-   <code class='path'>veri_anket_2021-04-15.xls</code>
-   <code class='path'>rapor_v1.doc</code>
-   <code class='path'>rapor_v2.doc</code>
-   <code class='path'>rapor_v3.doc</code>

::: {.try data-latex=""}
Yukarıdaki dosyaları adlandırmak için başka yollar düşünün. Kendi proje dosyalarınızdan bazılarına bakın ve neleri geliştirebileceğinizi görün.
:::

### Yeni bir projeye başlamak

-   Artık dosya sisteminin nasıl çalıştığını ve komut dosyalarının bunlara erişmesini kolaylaştırmak için nesneleri nasıl adlandıracağımızı anladığımıza göre, projemizi yapmaya hazırız.

-   Öncelikle, bu sınıf için tüm materyallerinizi tutacağınız yeni bir dizin oluşturun (benimki Ranaliz adınında). Bu dizini Global Options'ın general bölümü altında varsayılan çalışma dizini olarak ayarlayabilirsiniz. Bu, bir projede çalışmıyorsanız dosyaların varsayılan olarak buraya kaydedileceği anlamına gelir.

::: {.warning data-latex=""}
Bu dizin OneDrive'daysa veya tam dosya yolu özel karakterler içeriyorsa ya da bazı Windows makinelerinde 260 karakterden fazlaysa bazen sorunlara neden olabilir.
:::

-   Ardından, OLC731_2023 adında yeni bir proje oluşturmak için **`File`** menüsü altında **`New Project...`** öğesini seçin. Yeni oluşturduğunuz dizinin içine kaydettiğinizden emin olun. RStudio kendini yeniden başlatacak ve çalışma dizini olarak bu yeni proje dizini ile açılacaktır.

Proje dizininin içeriğini görmek için sağ alt bölmedeki Files sekmesine tıklayın. Tüm proje bilgilerini içeren Ranaliz.Rproj adlı bir dosya göreceksiniz, projeyi açmak için üzerine çift tıklayabilirsiniz.

::: {.info data-latex=""}
Ayarlarınıza bağlı olarak, özel kullanıcı ayarlarınızı içeren .Rproj.user adlı bir dizin de görebilirsiniz. Bu ve nokta ile başlayan diğer "görünmez" dosyaları yok sayabilirsiniz.
:::

## R Markdown

-   Bu derste, bir içindekiler tablosu, uygun başlıklar, kod parçaları, tablolar, resimler, satır içi R ve bir kaynakça içeren bir R Markdown belgesi oluşturmayı öğreneceğiz.

::: {.info data-latex=""}
R Markdown'a çok benzeyen quarto adında yeni bir tür tekrarlanabilir rapor formatı var. Bu derste [quarto](https://quarto.org/){target="_blank"} kullanmayacağız çünkü aynı anda hem quarto hem de R Markdown öğreniyorsanız kafa karıştırıcı olabilecek birkaç küçük farkı var, ancak R Markdown'ı öğrendikten sonra quarto'yu çok kolay bir şekilde öğrenebilirsiniz.
:::

-   Tekrar üretilebilir raporlar oluşturmak için metin ve kodun karıştırılmasını sağlayan R Markdown kullanacağız. Yeniden üretilebilir bir komut dosyası, kod bloklarında kod bölümleri içerecektir. Bir kod bloğu arka arkaya üç backtick sembolü ile başlar ve biter, küme parantezleri arasında kod hakkında bazı bilgiler bulunur, örneğin {r chunk-name, echo=FALSE} (bu kodu çalıştırır, ancak derlenen belgede kod bloğunun metnini göstermez). Kod bloklarının dışındaki metin, başlıklar, paragraflar, listeler, kalınlaştırma ve bağlantılar gibi biçimlendirmeyi belirtmenin bir yolu olan markdown ile yazılır. [Örnek Dosyayı beraber inceleyelim.](https://raw.githubusercontent.com/atalay-k/OLC731/main/docs/repro.Rmd)

-   Bir şablondan yeni bir R Markdown dosyası açarsanız, içinde birkaç kod bloğu bulunan örnek bir belge görürsünüz. Bir R Markdown (Rmd) belgesinden HTML veya PDF raporu oluşturmak için belgeyi derlersiniz. Bir belgeyi derlemeye RStudio'da örme denir. Dosyanızı bir rapora derlemek için üzerine tıkladığınız, içinden iğneler geçen bir iplik yumağına benzeyen bir düğme vardır.

::: {.try data-latex=""}
**`File > New File > R Markdown...`** menüsünden yeni bir R Markdown dosyası oluşturun. Başlığı ve yazarı değiştirin, dosyayı Ornek1.Rmd olarak kaydedin, ardından bir html dosyası oluşturmak için ör düğmesine tıklayın.
:::

### YAML Header {#yaml}

-   🔗 [YAML başlığı çeşitli seçenekleri ayarlayabileceğiniz bölümdür.](https://bookdown.org/yihui/rmarkdown/html-document.html)

```         
---
title: "Demo"
author: "Kubra"
output:
  html_document:
    toc: true
    toc_float:
      collapsed: false
      smooth_scroll: false
      number_sections: false
---
```

::: {.info data-latex=""}
Seçeneklerin ne işe yaradığını görmek için değerleri `false` tan `true` ya değiştirmeyi deneyin.
:::

-   Varsayılan temalar şunlardır: default, cerulean, cosmo, darkly, flatly, journal, lumen, paper, readable, sandstone, simplex, spacelab, united ve yeti. Linkten 🔗[daha fazla temayı inceleyebilirsiniz.](https://rpubs.com/ranydc/rmarkdown_themes).

### Kurulum

-   Varsayılan şablonu kullanarak RStudio'da yeni bir R Markdown dosyası oluşturduğunuzda, otomatik olarak bir kurulum blogu oluşturulur.

<div class='verbatim'><pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;{r setup, include=FALSE}</code></pre>

```r
knitr::opts_chunk$set(echo = TRUE)
```

<pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;</code></pre></div>

-   Kod parçaları için daha fazla varsayılan seçeneği buradan ayarlayabilirsiniz. Olası seçeneklerin açıklamaları için knitr seçenekleri belgelerine bakın. [knitr dokumanı](https://yihui.name/knitr/options/){target="_blank"}

<div class='verbatim'><pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;{r setup, include=FALSE}</code></pre>

```r
knitr::opts_chunk$set(
  fig.width  = 8,
  fig.height = 5,
  fig.path   = 'images/',
  echo       = FALSE,
  warning    = TRUE,
  message    = FALSE,
  cache      = FALSE
)
```

<pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;</code></pre></div>

Yukarıdaki kod aşağıdaki seçenekleri ayarlar:

-   fig.width = 8 : varsayılan şekil genişliği 8 inçtir (bunu tek tek şekiller için değiştirebilirsiniz)

-   fig.height = 5 : varsayılan şekil yüksekliği 5 inçtir

-   fig.path = 'images/' : şekiller "images" dizinine kaydedilir

-   echo = FALSE : işlenen belgede kod parçalarını gösterme

-   warning = FALSE : herhangi bir işlev uyarısı gösterme

-   message = FALSE : herhangi bir işlev mesajı gösterme

-   cache = FALSE : her örgü ördüğünüzde tüm görüntüleri ve nesneleri oluşturmak için tüm kodu çalıştırın (zaman alıcı kodunuz varsa TRUE olarak ayarlayın) Konsola <code><span><span class='fu'><a target='_blank' href='https://rdrr.io/r/utils/str.html'>str</a></span><span class='op'>(</span><span class='fu'>knitr</span><span class='fu'>::</span><span class='va'><a target='_blank' href='https://rdrr.io/pkg/knitr/man/opts_chunk.html'>opts_chunk</a></span><span class='op'>$</span><span class='fu'>get</span><span class='op'>(</span><span class='op'>)</span><span class='op'>)</span></span></code> yazarak geçerli kod bloğu seçeneklerinin bir listesini bulun.

İhtiyacınız olan paketleri <code><span><span class='kw'><a target='_blank' href='https://rdrr.io/r/base/library.html'>library</a></span><span class='op'>(</span><span class='op'>)</span></span></code>kullanarak da bu bloğunuza ekleyebilirsiniz. Genellikle bir komut dosyası üzerinde çalışırken, başka bir eklenti paketi yüklemeniz gerektiğini fark edersiniz. `library(...)` çağrısını kodun en altına gömmeyin. En üste koyun, böylece kullanıcı hangi paketlerin gerekli olduğuna dair genel bir fikir elde edilir.

::: {.try data-latex=""}
tidyverse paketinden fonksiyon kullanacağız, bu yüzden kurulum bloğunuza yükleyin.
:::

### Yapı

-   Bir içindekiler tablosu (`toc`) eklerseniz, bu tablo belge başlıklarınızdan oluşturulur. Markdown'daki başlıklar, başlık başlığının önüne bir veya daha fazla hash (\#) eklenerek oluşturulur.

-   Kendi analiz komut dosyalarınızı geliştirirken aşağıdaki yapıyı kullanın:

-   Kullanmanız gereken tüm eklenti paketlerini yükleyin

-   herhangi bir özel fonksiyon tanımlayın

-   birlikte çalışacağınız verileri yükleyin veya simüle edin

-   kaydetmeniz gereken her şeyi kaydedin

::: {.try data-latex=""}
Varsayılan metni silin ve başlıklar ve alt başlıklar oluşturarak belgenize biraz yapı ekleyin. Bazı verileri yükleyeceğiz, bir özet tablo oluşturacağız, verileri çizeceğiz ve analiz edeceğiz.
:::

### Kod Blokları

-   Metninize eklemek için görüntüler, tablolar veya hesaplamalar oluşturan ve görüntüleyen kod parçaları ekleyebilirsiniz. Bazı verileri yükleyerek başlayalım.

-   İlk olarak, belgenizde bir kod bloğu oluşturun. Bu kod iris veri setini yükler.


```r
library(datasets)
data(iris)
```

### Yorumlar

-   Kod blokları içine hash sembolü (\#) ile yorum ekleyebilirsiniz. R yorumlayıcısı, hash'ten satır sonuna kadar olan karakterleri yoksayacaktır.


```r
n <- nrow(iris) # toplam satır sayısı
mu <- mean(iris$Petal.Length)  # taç yaprak uzunluğu ortalaması
sd <- sd(iris$Petal.Length) # taç yaprak uzunluğu standart sapması


simule_deger <- rnorm(n, mu, sd)
```

-   Bir kod parçasını, özellikle kod rapor metninde açıklanmamışsa, orada ne yaptığınızı açıklayan bir yorumla başlatmak genellikle iyi bir uygulamadır.

-   Nesnelerinizi açık bir şekilde adlandırırsanız, genellikle açıklayıcı yorumlar eklemeniz gerekmez. Örneğin, yukarıdaki üç nesneyi n_iris, ort_petal ve sd_petal olarak adlandırmış olsaydım, yorumları atlardım.

-   Yorumların bir başka kullanımı da çalıştırmak istemediğiniz ancak silmek de istemediğiniz bir kod bölümünü "yorumlamaktır". Örneğin, bir paketi yüklemek için kullanılan kodu kodunuza dahil edebilirsiniz, ancak kodun her çalıştırıldığında uzun bir yüklemeye zorlamaması için her zaman yorumlamanız gerekir.


```r
# install.packages("dplyr")
# install.packages("tidyr")
# install.packages("ggplot2")
```

::: {.info data-latex=""}
Satırları seçip Cmd-shift-C (Mac) veya Ctrl-shift-C (Windows) yazarak aynı anda birden fazla satıra yorum yazabilir veya yorumu kaldırabilirsiniz.
:::

-   Kodunuzu iyi bir şekilde yorumlamak biraz sanattır. Bu beceriyi geliştirmenin en iyi yolu, başkalarının kodlarını okumak ve başkalarının kodunuzu incelemesini sağlamaktır.

### Satır İçi kodlar {#inline-r}

-   Şimdi setosa ve virginica çiçek türlerinde yaprak uzunluklarını analiz edelim. Önce analiz kodunu çalıştıracağız. Daha sonra makalemizde kullanmak isteyebileceğimiz sayıları değişkenlere kaydedeceğiz ve uygun şekilde yuvarlayacağız. Son olarak, bir sonuçları biçimlendirmek için glue::glue() kullanacağız.


```r
# analiz
library(dplyr)
setosa_petal <- filter(iris, Species == "setosa") %>% pull(Petal.Length)
virginica_petal <- filter(iris, Species == "virginica") %>% pull(Petal.Length)
petal_test <- t.test(setosa_petal, virginica_petal)

# rapor edilecek degerleri yorumlama
t <- petal_test$statistic %>% round(2)
df <- petal_test$parameter %>% round(1)
p <- petal_test$p.value %>% round(3)
# handle p-values < .001
p_symbol <- ifelse(p < .001, "<", "=")
if (p < .001) p <- .001

# sonucları birleştirme
petal_result <- glue::glue("t = {t}, df = {df}, p {p_symbol} {p}")
```

-   Sonuçları, aşağıdaki gibi görünen satır içi R kodu ile bir paragrafa ekleyebilirsiniz:

```{=html}
<pre><code> virginica çiçeklerinin yaprakları setosa çiçeklerinin yapraklarından uzundur(&#96;r petal_result&#96;).</code></pre>
```
virginica çiçeklerinin yaprakları setosa çiçeklerinin yapraklarından uzundur (t = -49.99, df = 58.6, p < 0.001).

### Tablolar {#repro-tables}

-   Çalışmaların yöntem bölümüne betimsel bilgiler eklemek istediğimizde


```r
ozet_tablo <- iris %>%
  group_by(Species) %>%
  summarise(
    n = n(),
    ortalama = mean(Petal.Length),
    sd = sd(Petal.Length)
  )
ozet_tablo
```

<div class="kable-table">

<table>
 <thead>
  <tr>
   <th style="text-align:left;"> Species </th>
   <th style="text-align:right;"> n </th>
   <th style="text-align:right;"> ortalama </th>
   <th style="text-align:right;"> sd </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> setosa </td>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:right;"> 1.462 </td>
   <td style="text-align:right;"> 0.1736640 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> versicolor </td>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:right;"> 4.260 </td>
   <td style="text-align:right;"> 0.4699110 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> virginica </td>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:right;"> 5.552 </td>
   <td style="text-align:right;"> 0.5518947 </td>
  </tr>
</tbody>
</table>

</div>

::: {.warning data-latex=""}
Yukarıdaki tablo etkileşimli görünümde tibble biçiminde yazdırılacak, ancak ördüğünüzde YAML başlığındaki df_print ayarındaki biçimi kullanacaktır.
:::

-   Yukarıdaki tabloda, sütun etiketlerini değiştirerek, ortalamaları yuvarlayarak ve bir başlık ekleyerek daha okuyucu dostu hale getirlebilir. Bunun için <code><span><span class='fu'>knitr</span><span class='fu'>::</span><span class='fu'><a target='_blank' href='https://rdrr.io/pkg/knitr/man/kable.html'>kable</a></span><span class='op'>(</span><span class='op'>)</span></span></code> işlevini veya tablolarınızı biçimlendirmek için diğer paketlerdeki daha özel işlevleri kullanabilirsiniz.

::: tab
<button class="tablinks" onclick="openCity(event, &#39;knitr&#39;)">

knitr

</button>

<button class="tablinks" onclick="openCity(event, &#39;kableExtra&#39;)">

kableExtra

</button>

<button class="tablinks" onclick="openCity(event, &#39;papaja&#39;)">

papaja

</button>

<button class="tablinks" onclick="openCity(event, &#39;gt&#39;)">

gt

</button>

::: {#knitr .tabcontent}

```r
yeni_ad <- c("Çiçek Türü", "Frekans", "Ortalama", "Sd")

knitr::kable(ozet_tablo,
             digits = 2,
             col.names = yeni_ad,
             caption = "Petal Uzulukları için Özet Tablo")
```

<table>
<caption>(\#tab:kable-demo)Petal Uzulukları için Özet Tablo</caption>
 <thead>
  <tr>
   <th style="text-align:left;"> Çiçek Türü </th>
   <th style="text-align:right;"> Frekans </th>
   <th style="text-align:right;"> Ortalama </th>
   <th style="text-align:right;"> Sd </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> setosa </td>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:right;"> 1.46 </td>
   <td style="text-align:right;"> 0.17 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> versicolor </td>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:right;"> 4.26 </td>
   <td style="text-align:right;"> 0.47 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> virginica </td>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:right;"> 5.55 </td>
   <td style="text-align:right;"> 0.55 </td>
  </tr>
</tbody>
</table>
:::

::: {#kableExtra .tabcontent}
[**kableExtra**](https://haozhu233.github.io/kableExtra/awesome_table_in_html.html) **paketi çok sayıda seçenek sunar.**


```r
library(kableExtra)

kable(ozet_tablo,
      digits = 2,
      col.names = c("Çiçek Türü", "Frekans", "Ortalama", "Sd"),
      caption = "Petal Uzulukları için Özet Tablo") |>
  kable_classic() |>
  kable_styling(full_width = FALSE, font_size = 20) |>
  add_header_above(c(" " = 2, "Degerler" = 2)) |>
  kableExtra::row_spec(2, bold = TRUE, background = "lightgrey")
```

<table class=" lightable-classic table" style='font-family: "Arial Narrow", "Source Sans Pro", sans-serif; margin-left: auto; margin-right: auto; font-size: 20px; width: auto !important; margin-left: auto; margin-right: auto;'>
<caption style="font-size: initial !important;">(\#tab:kableExtra-demo)Petal Uzulukları için Özet Tablo</caption>
 <thead>
<tr>
<th style="empty-cells: hide;" colspan="2"></th>
<th style="padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; " colspan="2"><div style="border-bottom: 1px solid #111111; margin-bottom: -1px; ">Degerler</div></th>
</tr>
  <tr>
   <th style="text-align:left;"> Çiçek Türü </th>
   <th style="text-align:right;"> Frekans </th>
   <th style="text-align:right;"> Ortalama </th>
   <th style="text-align:right;"> Sd </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> setosa </td>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:right;"> 1.46 </td>
   <td style="text-align:right;"> 0.17 </td>
  </tr>
  <tr>
   <td style="text-align:left;font-weight: bold;background-color: lightgrey !important;"> versicolor </td>
   <td style="text-align:right;font-weight: bold;background-color: lightgrey !important;"> 50 </td>
   <td style="text-align:right;font-weight: bold;background-color: lightgrey !important;"> 4.26 </td>
   <td style="text-align:right;font-weight: bold;background-color: lightgrey !important;"> 0.47 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> virginica </td>
   <td style="text-align:right;"> 50 </td>
   <td style="text-align:right;"> 5.55 </td>
   <td style="text-align:right;"> 0.55 </td>
  </tr>
</tbody>
</table>
:::

::: {#papaja .tabcontent}
[**papaja**](https://crsh.github.io/papaja_man/reporting.html#tables) **paketi ile APA formatında tablolar elde edebilirsiniz.**


```r
papaja::apa_table(ozet_tablo,
                  col.names = c("Çiçek Türü", "Frekans", "Ortalama", "Sd"),
                  caption = "Petal Uzulukları için Özet Tablo",
                  col_spanners = list("Means" = c(3, 4)))
```

Table: (\#tab:papaja-demo) Petal Uzulukları için Özet Tablo


Çiçek Türü   Frekans   Ortalama   Sd   
-----------  --------  ---------  -----
setosa       50        1.46       0.17 
versicolor   50        4.26       0.47 
virginica    50        5.55       0.55 
:::

::: {#gt .tabcontent}
[**gt**](https://gt.rstudio.com/index.html) **paketinde de çok sayıda seçenek bulunmaktadır.**


```r
library(gt)

gt(ozet_tablo, caption = "Petal Uzulukları için Özet Tablo") |>
  fmt_number(columns = c(ortalama, sd),
             decimals = 2) |>
  cols_label(Species = "Çiçek Türü",
             n = "Frekans",
             ortalama = "ortalama",
             sd = "sd") |>
  tab_spanner(label = "Degerler",
              columns = c(ortalama, sd)) |>
  opt_stylize(style = 6, color = "blue")
```

```{=html}
<div id="xxmmfpcfga" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#xxmmfpcfga table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#xxmmfpcfga thead, #xxmmfpcfga tbody, #xxmmfpcfga tfoot, #xxmmfpcfga tr, #xxmmfpcfga td, #xxmmfpcfga th {
  border-style: none;
}

#xxmmfpcfga p {
  margin: 0;
  padding: 0;
}

#xxmmfpcfga .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 16px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #5F5F5F;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #5F5F5F;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#xxmmfpcfga .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#xxmmfpcfga .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#xxmmfpcfga .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#xxmmfpcfga .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#xxmmfpcfga .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #5F5F5F;
}

#xxmmfpcfga .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #5F5F5F;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #5F5F5F;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#xxmmfpcfga .gt_col_heading {
  color: #FFFFFF;
  background-color: #0076BA;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#xxmmfpcfga .gt_column_spanner_outer {
  color: #FFFFFF;
  background-color: #0076BA;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#xxmmfpcfga .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#xxmmfpcfga .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#xxmmfpcfga .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #5F5F5F;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#xxmmfpcfga .gt_spanner_row {
  border-bottom-style: hidden;
}

#xxmmfpcfga .gt_group_heading {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #5F5F5F;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #5F5F5F;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#xxmmfpcfga .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #5F5F5F;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #5F5F5F;
  vertical-align: middle;
}

#xxmmfpcfga .gt_from_md > :first-child {
  margin-top: 0;
}

#xxmmfpcfga .gt_from_md > :last-child {
  margin-bottom: 0;
}

#xxmmfpcfga .gt_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: none;
  border-top-width: 1px;
  border-top-color: #D5D5D5;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D5D5D5;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D5D5D5;
  vertical-align: middle;
  overflow-x: hidden;
}

#xxmmfpcfga .gt_stub {
  color: #333333;
  background-color: #89D3FE;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D5D5D5;
  padding-left: 5px;
  padding-right: 5px;
}

#xxmmfpcfga .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#xxmmfpcfga .gt_row_group_first td {
  border-top-width: 2px;
}

#xxmmfpcfga .gt_row_group_first th {
  border-top-width: 2px;
}

#xxmmfpcfga .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#xxmmfpcfga .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #5F5F5F;
}

#xxmmfpcfga .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#xxmmfpcfga .gt_last_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #5F5F5F;
}

#xxmmfpcfga .gt_grand_summary_row {
  color: #333333;
  background-color: #D5D5D5;
  text-transform: inherit;
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
}

#xxmmfpcfga .gt_first_grand_summary_row {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #5F5F5F;
}

#xxmmfpcfga .gt_last_grand_summary_row_top {
  padding-top: 8px;
  padding-bottom: 8px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #5F5F5F;
}

#xxmmfpcfga .gt_striped {
  background-color: #EDF7FC;
}

#xxmmfpcfga .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #5F5F5F;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #5F5F5F;
}

#xxmmfpcfga .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#xxmmfpcfga .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
}

#xxmmfpcfga .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#xxmmfpcfga .gt_sourcenote {
  font-size: 90%;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
}

#xxmmfpcfga .gt_left {
  text-align: left;
}

#xxmmfpcfga .gt_center {
  text-align: center;
}

#xxmmfpcfga .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#xxmmfpcfga .gt_font_normal {
  font-weight: normal;
}

#xxmmfpcfga .gt_font_bold {
  font-weight: bold;
}

#xxmmfpcfga .gt_font_italic {
  font-style: italic;
}

#xxmmfpcfga .gt_super {
  font-size: 65%;
}

#xxmmfpcfga .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#xxmmfpcfga .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#xxmmfpcfga .gt_indent_1 {
  text-indent: 5px;
}

#xxmmfpcfga .gt_indent_2 {
  text-indent: 10px;
}

#xxmmfpcfga .gt_indent_3 {
  text-indent: 15px;
}

#xxmmfpcfga .gt_indent_4 {
  text-indent: 20px;
}

#xxmmfpcfga .gt_indent_5 {
  text-indent: 25px;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <caption>(#tab:gt-demo)Petal Uzulukları için Özet Tablo</caption>
  <thead>
    
    <tr class="gt_col_headings gt_spanner_row">
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="2" colspan="1" scope="col" id="Çiçek Türü">Çiçek Türü</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="2" colspan="1" scope="col" id="Frekans">Frekans</th>
      <th class="gt_center gt_columns_top_border gt_column_spanner_outer" rowspan="1" colspan="2" scope="colgroup" id="Degerler">
        <span class="gt_column_spanner">Degerler</span>
      </th>
    </tr>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col" id="ortalama">ortalama</th>
      <th class="gt_col_heading gt_columns_bottom_border gt_right" rowspan="1" colspan="1" scope="col" id="sd">sd</th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="Species" class="gt_row gt_center">setosa</td>
<td headers="n" class="gt_row gt_right">50</td>
<td headers="ortalama" class="gt_row gt_right">1.46</td>
<td headers="sd" class="gt_row gt_right">0.17</td></tr>
    <tr><td headers="Species" class="gt_row gt_center gt_striped">versicolor</td>
<td headers="n" class="gt_row gt_right gt_striped">50</td>
<td headers="ortalama" class="gt_row gt_right gt_striped">4.26</td>
<td headers="sd" class="gt_row gt_right gt_striped">0.47</td></tr>
    <tr><td headers="Species" class="gt_row gt_center">virginica</td>
<td headers="n" class="gt_row gt_right">50</td>
<td headers="ortalama" class="gt_row gt_right">5.55</td>
<td headers="sd" class="gt_row gt_right">0.55</td></tr>
  </tbody>
  
  
</table>
</div>
```
:::
:::

#### Manuel tablo

Tablo eklemek için diğer bir yol ise elle tablo oluşturmaktadır. Tablo oluşturulmak istendiğinde aşağıdaki şekilde eklenebilir.


```r
| col1   |col2    |  
|:------:|:------:|
|içerik1 |içerik2 |
```

Yukarıdaki içerik örüldüğünde aşağıdaki tablo oluşmaktadır.

| col1   |col2    |  
|:------:|:------:|
|içerik1 |içerik2 |

Tablo eklemek için Rstudio yer alan Visual özelliğini kullanmakta pratiktir. Hazırladığınız markdown dosyasını Visual modunda açtığınızda Table menüsünde tablo oluşturma, satır sütun ekleme, hizalama gibi işlemler menü aracılığı ile yapılabilimektedir.

### Görseller {#repro-figures}

-   Şekil başlığının kod bloğında nasıl biçimlendirildiğine dikkat edin.

<div class='verbatim'><pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;{r boxplot}</code></pre>

```r
dat <- subset(iris, Species != "versicolor")
dat$Species <- factor(dat$Species)

ggplot(dat, aes(Species, Petal.Length)) +
  geom_boxplot(width = 0.25,
               show.legend = FALSE)  +
  labs(x = "", y = "Petal Uzunluğu") +
  theme(text = element_text(size = 20, family = "Times"))
```

<div class="figure" style="text-align: center">
<img src="06-markdown_files/figure-html/unnamed-chunk-11-1.png" alt="Petal Uzunlukları ve Türler" width="100%" />
<p class="caption">(\#fig:unnamed-chunk-11)Petal Uzunlukları ve Türler</p>
</div><pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;</code></pre></div>

<div class="figure" style="text-align: center">
<img src="06-markdown_files/figure-html/pet-plot-out-1.png" alt=" Petal Uzunlukları ve Türler" width="100%" />
<p class="caption">(\#fig:pet-plot-out) Petal Uzunlukları ve Türler</p>
</div>

::: {.info data-latex=""}
Son satır varsayılan metin boyutunu ve yazı tipini değiştirir, bu da bir derginin gereksinimlerini karşılayan şekiller oluşturmak için yararlı olabilir.
:::

-   Kodlarla oluşturamadığınız şekilleri de resim dosyaları ile dökümana ekleyebilirsiniz:

``` md
![neden R](https://miro.medium.com/v2/resize:fit:720/format:webp/1*TX77o_zJ4zbpJ3vN4BkLsg.jpeg){style="width: 50%"}
```

![neden R](https://miro.medium.com/v2/resize:fit:720/format:webp/1*TX77o_zJ4zbpJ3vN4BkLsg.jpeg){style="width: 50%"}

### Bağlantılı Dökümanlar

-   Markdown bölümler arasında bağlantılar içeren daha uzun raporlar oluşturmanıza yardımcı olur.

-   Başlığı olan tüm şekillere veya tablolara otomatik olarak şekil ve tablo numaraları ekler ve bunlara referansla bağlantı vermenize olanak sağlar.

-   Tablolara ve şekillere bağlantılar oluşturmak için, şekillerinizi veya tablolarınızı oluşturan kod bloklarınız adlandırmanız ve ardından satır içi kodlamanızda bu adları çağırmanız gerekir:

<div class='verbatim'><pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;{r tablo1}</code></pre>

```r
# kodlar
```

<pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;</code></pre></div>

<div class='verbatim'><pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;{r sekil1}</code></pre>

```r
# kodlar
```

<pre class='sourceCode r'><code class='sourceCode R'>&#96;&#96;&#96;</code></pre></div>

```         
Bakınız Tablo\ \@ref(tab:tablo1) or Sekil\ \@ref(fig:sekil1).
```

::: {.warning data-latex=""}
Kod blok adları yalnızca harf, rakam ve tire içerebilir. Boşluk veya alt çizgi gibi başka karakterler içeriyorlarsa, referanslama çalışmayacaktır.
:::

Başlıklarınızı {#} ile adlandırarak da raporunuzun farklı bölümlerine bağlantı verebilirsiniz:

```         
# Baslık 1 {#baslık-1}

## Baslık 2 {#baslık-2}

Bakınız Bolum\ \@ref(baslık-1) and Bolum\ \@ref(baslık-2)
```

-   Aşağıdaki kod, ggplot2 paketindeki `diamonds` veri seti kullanarak tam bir raporda metnin şekillere veya tablolara nasıl bağlanacağını göstermektedir - bu belgeyi şimdi oluşturmak için aşağıdaki kodları kullanın.


<div class='webex-solution'><button>Dokuman burada</button>



````md
---
title: 
output: 
  bookdown::html_document2:
    number_sections: true
---

# ORNEK DOSYA

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = FALSE,
                      message = FALSE,
                      warning = FALSE)
library(tidyverse)
library(kableExtra)
theme_set(theme_minimal())
```

Pırlanta ücretleri çeşitli faktörlere bağlıdır

- cut (Bakınız Tablo\ \@ref(tab:kesim))
- colour (Bakınız Tablo\ \@ref(tab:renk))
- clarity (Bakınız Şekil\ \@ref(fig:parlaklik))
- carats (Bakınız Şekil\ \@ref(fig:karat))
- Bakınız Bolum\ \@ref(sonuclar) sonuclar icin

## Tablolar

### Kesim

```{r kesim}
diamonds %>%
  group_by(cut) %>%
  summarise(avg = mean(price),
            .groups = "drop") %>%
  kable(digits = 0, 
        col.names = c("Cut", "Average Price"),
        caption = "Kesime göre ortalama pırlanta fiyatı.") %>%
  kable_material()
```

### Renk

```{r renk}
diamonds %>%
  group_by(color) %>%
  summarise(avg = mean(price),
            .groups = "drop") %>%
  kable(digits = 0, 
        col.names = c("Cut", "Average Price"),
        caption = "Renge göre ortalama pırlanta fiyatı.") %>%
  kable_material()
```

## Grafikler

### Parlaklık

```{r parlaklik, fig.cap = "Parlaklığa göre pırlanta fiyatı"}
ggplot(diamonds, aes(x = clarity, y = price)) +
  geom_boxplot() 
```

### Karat

```{r karat, fig.cap = "Karata göre pırlanta fiyatı"}
ggplot(diamonds, aes(x = carat, y = price)) +
  stat_smooth()
```

### Sonuclar {#sonuclar}

"Kodlar haricinde pırlantalarla ilgilenmiyorum :) "
````


</div>


Bu format varsayılan olarak numaralandırılmış bölümler bulunuyor, numaralandırma bunu istemiyorsanız `YAML` bölümünde `number_sections: false` ayarını yapın. Numaralandırılmış bölümleri kaldırırsanız, `\@ref(sonuclar)` gibi bağlantılar "??" gösterecektir, bu nedenle bunun yerine aşağıdaki gibi URL bağlantı adresi kullanmanız gerekir:

```         
Son açıklamalar için [son bölüme](#sonuclar) bakınız.
```

## Kaynakça

R Markdown'da metin içi referanslar yapmanın ve otomatik olarak bir kaynakça oluşturmanın birkaç yolu vardır. Markdown dosyalarının, atıfta bulunmanız gereken referansları içeren bir BibTex veya JSON dosyasına (referansları belirli bir formatta içeren düz bir metin dosyası) bağlanması gerekir. Bu dosyanın adını bibliography: refs.bib gibi YAML başlığında belirtirsiniz ve [@tidyverse] gibi bir \@ sembolü ve kısa ad kullanarak metin içinde referanslara atıfta bulunursunuz. Referanslarınızı örneğin APA stilinde biçimlendirmek için bir [Citation Style Language (.csl) dosyası da ekleyebilirsiniz.](https://github.com/citation-style-language/styles/blob/master/apa.csl)

a [bibliography](https://bookdown.org/yihui/rmarkdown-cookbook/bibliography.html){target="_blank"}

```         
---
title: "My Paper"
author: "Me"
output:
  html_document:
    toc: true
bibliography: refs.bib
csl: apa.csl
---
```

### Referans yazılımdan dönüştürme

EndNote veya Zotero gibi çoğu referans yazılımı BibTeX formatına aktarabilen dışa aktarma seçeneklerine sahiptir. Ortaya çıkan dosyadaki kısa adları kontrol etmeniz yeterlidir.

::: {.warning data-latex=""}
Bir referans programı kullanmak hayatınızı çok daha kolaylaştıracaktır. Zotero muhtemelen en iyisidir.
:::

Dışa aktarılan dosya şu şekilde görünmelidir:


```bib

@article{kathawalla_easing_2021,
	title = {Easing {Into} {Open} {Science}: {A} {Guide} for {Graduate} {Students} and {Their} {Advisors}},
	volume = {7},
	issn = {2474-7394},
	shorttitle = {Easing {Into} {Open} {Science}},
	url = {https://doi.org/10.1525/collabra.18684},
	doi = {10.1525/collabra.18684},
	abstract = {This article provides a roadmap to assist graduate students and their advisors to engage in open science practices. We suggest eight open science practices that novice graduate students could begin adopting today. The topics we cover include journal clubs, project workflow, preprints, reproducible code, data sharing, transparent writing, preregistration, and registered reports. To address concerns about not knowing how to engage in open science practices, we provide a difficulty rating of each behavior (easy, medium, difficult), present them in order of suggested adoption, and follow the format of what, why, how, and worries. We give graduate students ideas on how to approach conversations with their advisors/collaborators, ideas on how to integrate open science practices within the graduate school framework, and specific resources on how to engage with each behavior. We emphasize that engaging in open science behaviors need not be an all or nothing approach, but rather graduate students can engage with any number of the behaviors outlined.},
	number = {1},
	urldate = {2022-09-07},
	journal = {Collabra: Psychology},
	author = {Kathawalla, Ummul-Kiram and Silverstein, Priya and Syed, Moin},
	month = jan,
	year = {2021},
	pages = {18684},
}
```

### BibTeX Dosyası Oluşturma

Referansları manuel olarak da ekleyebilirsiniz. RStudio'da **`File`** \> **`New File...`** \> **`Text File`** seçeneğine gidin. \> Metin Dosyası'na gidin ve dosyayı "refs.bib" olarak kaydedin.

Ardından, YAML başlığınıza `bibliography: refs.bib` satırını ekleyin.

### Referans ekleme

Bir dergi makalesine aşağıdaki formatta referanslar ekleyebilirsiniz:

```         
@article{shortname,
  author = {Author One and Author Two and Author Three},
  title = {Paper Title},
  journal = {Journal Title},
  volume = {vol},
  number = {issue},
  pages = {startpage--endpage},
  year = {year},
  doi = {doi}
}
```

Kitaplara, teknik raporlara ve daha fazlasına atıfta bulunma talimatları için BibTeX formatına ilişkin eksiksiz bir kılavuza bakın.

citation() ve toBibtex() fonksiyonlarını kullanarak bir R paketi için referans alabilirsiniz. Bibtex girişini bibliography.bib dosyanıza yapıştırabilirsiniz. Referansa atıfta bulunmak için ilk virgülden önce kısa bir ad (örneğin, "ggplot2") eklediğinizden emin olun.

See [A complete guide to the BibTeX format](https://www.bibtex.com/g/bibtex-format/){target="_blank"} kitaplara, teknik raporlara ve daha fazlasına atıfta bulunma talimatları için.

Bir R paketinin referansını `citation()` ve `toBibtex()` fonksiyonlarını kullanarak alabilirsiniz. Bibtex girişini bibliography.bib dosyanıza yapıştırabilirsiniz. Referansa atıfta bulunmak için ilk virgülden önce kısa bir ad (örneğin, "ggplot2") eklediğinizden emin olun.


```r
citation(package="ggplot2") %>% toBibtex()
```

```
## @Book{,
##   author = {Hadley Wickham},
##   title = {ggplot2: Elegant Graphics for Data Analysis},
##   publisher = {Springer-Verlag New York},
##   year = {2016},
##   isbn = {978-3-319-24277-4},
##   url = {https://ggplot2.tidyverse.org},
## }
```

[Google Scholar](https://scholar.google.com/) girişlerinde BibTeX atıf seçeneği vardır. DOI'yi kendiniz eklemeniz gerekse de, Zotero tarayıcı bağlayıcısı aracılığıyla bir atıf ekleyemiyorsanız, ilgili değerleri almanın en kolay yolu genellikle budur. Önerilen kısa adı koruyabilir veya sizin için daha anlamlı olan bir adla değiştirebilirsiniz.

<div class="figure" style="text-align: center">
<img src="images/google-scholar.png" alt="Get BibTex citations from Google Scholar." width="100%" />
<p class="caption">(\#fig:google-scholar)Get BibTex citations from Google Scholar.</p>
</div>

### Referanslara atıfta bulunma

Metin içinde referansları bu şekilde gösterebilirsiniz:

```         
This tutorial uses several R packages [@tidyverse;@rmarkdown].
```

Bu eğitimde çeşitli R paketleri kullanılmaktadır (Allaire vd., 2018; Wickham, 2017).

### Atıf yapılmayan referanslar

Bir öğeyi kaynak göstermeden referans bölümüne eklemek istiyorsanız, bunu YAML başlığına şu şekilde ekleyin:

```         
nocite: |
  @kathawalla_easing_2021, @broman2018data, @nordmann2022data
```

Ya da .bib dosyasındaki tüm öğeleri şu şekilde ekleyin:

```         
nocite: '@*'
```

### Atıf Stilleri

Çeşitli dergiler için [stil dosyalarının](https://www.zotero.org/styles){target="_blank"} bir listesini arayabilir ve kaynakçanızı belirli bir derginin stiline göre biçimlendirecek bir dosya indirebilirsiniz. YAML başlığınıza `csl: filename.csl` satırını eklemeniz gerekir.

::: {.try data-latex=""}
refs.bib dosyanıza bazı alıntılar ekleyin, metninizde bunlara atıfta bulunun ve otomatik olarak oluşturulan referans bölümünü görmek için makalenizi işleyin. Birkaç farklı atıf stili dosyası deneyin.
:::

### Referens Bölümü

Varsayılan olarak, referans bölümü belgenin sonuna eklenir. Konumu değiştirmek istiyorsanız (örneğin, referanslardan sonra şekil ve tablo eklemek için), referansları istediğiniz yere `<div id="refs"></div>` ekleyin.

::: {.try data-latex=""}
Raporunuza metin içi alıntılar ve bir referans listesi ekleyin.
:::

## Özel Şablonlar

Bazı paketler özel R Markdown şablonları sağlar. reprores, YAML başlığındaki tüm olası seçenekleri gösteren, kaynakça ve stil dosyalarına sahip olan ve bağlantılı şekil ve tabloların nasıl ayarlanacağını açıklayan bir Rapor şablonuna sahiptir. Birden fazla dosya içerdiğinden, RStudio sizden tüm dosyaları tutmak için yeni bir klasör oluşturmanızı isteyecektir.

Ödevinizi yapmak için aşağdaki kodla reproses pakeini yükleyebilirsiniz.


```r
# devtools::install_github("psyteachr/reprores-v3")
```
Daha sonra aşağıdaki gibi taslağı (template) açabilirsiniz. Örnek dosyayı inceledikten sonra kendi içerieğinizi oluşturabilirsiniz.

<div class="figure" style="text-align: center">
<img src="images/custom-rmd.png" alt="Şablonlar" width="75%" />
<p class="caption">(\#fig:img-custom-rmd)Şablonlar</p>
</div>

::: {.try data-latex=""}
Rapor şablonu ile bir rapor başlatın ve örün. Seçenekleri değiştirmeyi veya silmeyi deneyin.
:::

## Ödev

- rpubs sayfalarını oluşturup, bu bilgiyi bana ulaştırınız.

- rpubs sayfasında ilk dört haftada öğrendiklerinizin kısa bir özetini paylaşınız.

- Ayrıca [linkte](REGRESYONODEVI.html) yer alan çoklu regresyon ile ilgili dökümanı repores paketinin Report şablonu ile oluşturmanızı bekliyorum. Bu dökümana eklenmiş ayrıca bir adet görsel bulunmaktadır. Görsele buradan [ulaşabilirsiniz](images/LS.png). Bu ödeviniz gönderdiğim dosyaya benzerliğine göre puanlanacaktır.

- not:   şanlonda (templatede)  alan YMAL header  css: extras/style.css # path to css file kısmını siliniz. 

## Diğer Kaynaklar

-   [Chapter 27: R Markdown](http://r4ds.had.co.nz/r-markdown.html) in *R for Data Science*
-   [R Markdown Cheat Sheet](https://github.com/rstudio/cheatsheets/raw/master/rmarkdown.pdf)
-   [R Markdown reference Guide](https://www.rstudio.com/wp-content/uploads/2015/03/rmarkdown-reference.pdf)
-   [R Markdown Tutorial](https://rmarkdown.rstudio.com/lesson-1.html)
-   [R Markdown: The Definitive Guide](https://bookdown.org/yihui/rmarkdown/) by Yihui Xie, J. J. Allaire, & Garrett Grolemund
-   [Project Structure](https://slides.djnavarro.net/project-structure/) by Danielle Navarro
-   [How to name files](https://speakerdeck.com/jennybc/how-to-name-files) by Jenny Bryan
-   [Papaja](https://crsh.github.io/papaja_man/) Reproducible APA Manuscripts
-   [The Turing Way](https://the-turing-way.netlify.app/)
