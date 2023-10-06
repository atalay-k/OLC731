# R Dökümantasyon 


- **Mark up** düzeltme veya açıklama amacıyla bir kağıdın üzerine not düşme anlamına gelmektedir.


  -   Latex
  -   HTML (hypertext Markup Language)
  -   markdown
  - R Markdown ile

        -   Rapor, makale ve yazı yazma amacıyla kullanabilirsiniz.
        -   Web sitesi oluşturabilirsiniz.
        -   Sunum hazırlyabilirsiniz.

- Neden Markdown 
    
    -   hata olasılığını azaltır.
    -   analiz + programla + biçimlendirme + rapor
    
    -   R + markdown = R markdown

![markdown](images/rmd.png){width=50%}



|    Türü   | Uzantısı|
|:---------:|:------:|
|     R     |   .R   |
| markdown  |  .md   |
| Rmarkdown |  .Rmd  |




- R  üç ana bölümden oluşur
  - metadata (yaml header)
  - metin  
  - kod blokları  



## Başlıklar


<div class="info">
<h1 id="başlık-..-başlık">Başlık …..# Başlık</h1>
<h2 id="alt-başlık-alt-başlık">Alt Başlık ……## Alt Başlık</h2>
<h3 id="alt-alt-başlık-alt-alt-başlık">Alt-Alt Başlık ……### Alt-Alt
Başlık</h3>
<h4 id="alt-alt-alt-başlık-alt-alt-alt-başlık">Alt-Alt-Alt Başlık ……###
Alt-Alt-Alt Başlık</h4>
</div>

## Alt Başlık
### Alt-Alt Başlık
#### Alt-Alt-Alt Başlık

### Vurygulama

<div class="info">
<p><em>Merhaba Dünya</em> ##<em>Merhaba Dünya</em></p>
<p><strong>Merhaba Dünya</strong> ##<strong>Merhaba Dünya</strong></p>
<p><del>Merhaba Dünya</del> ##_<del>Merhaba Dünya</del></p>
</div>





## Matematiksel İşlemler


<div class="info">
<p><span class="math inline">\(\frac{3}{5}\)</span> ##<span
class="math inline">\(\frac{3}{5}\)</span></p>
</div>

::: {.try data-latex=""}
$\frac{3}{5}$   ##$\frac{3}{5}$
:::

<div class="info">
<p><span class="math inline">\(\sqrt{\frac{X}{Y}}\)</span> ##<span
class="math inline">\(\sqrt{\frac{X}{Y}}\)</span></p>
</div>


$\sqrt{\frac{X}{Y}}$


- [Mathematics in R Markdown](https://rpruim.github.io/s341/S19/from-class/MathinRmd.html)


## Bağlantı Verme

.pull-left[


```r
[rpubs](https://rpubs.com)
```
]

.pull-right[

[rpubs](https://rpubs.com)
]


## Figure (Şekil)

.pull-left[

```r
ggplot(mpg) + geom_bar(aes(y = class))
```
]
.pull-right[

<img src="04-Dokumantasyon_files/figure-html/unnamed-chunk-7-1.png" width="100%" style="display: block; margin: auto;" />
]


##  Yeni Dosya

- Yeni bir R Markdown dosyası başlatmak için **File > New File > R Markdown** kullanılabilir.


- Kayıtlı R Markdown dosyasını işlemek için **Knit** tuşu veya **Ctrl/Command + Shift + K** kısa yolu kullanılabilir.



##  Kod bloğu eklemek

- Kod bloğu eklemek için **Insert R** tuşu veya **Ctrl + Alt + I / Cmd + Option + I** kısa yolu kullanılabilir.

- ya da chunck ekle butonu kullanılabilir.





## Kod Bölümü Nasıl Oluşturulur

- Kod olarak belirtmek istenilen bloğun başına ve sonuna üç tane ters tırnak işaretini `´´´` eklemek gerekir. Yazılacak olan kodların ne kodu olduğunu küme parentezi içinde belirtebilirsiniz. 

- r codu icin ornek: `{r}`

``` {.r}
´´´´{r}
kodu buraya ekleyin
´´´´
```

- Bu bölümler metin icinde farklı renkte görünür.


```r
x <- 2
```


## Kod Bölümü İsmi

Kod bölümlerine aşağıdaki gibi isimlendirilebilir.

``` {.r}
´´´´{r isim}
kodu buraya ekleyin
´´´´
```

Isim vermenin üç temel avantaji bulunmaktadir.

1.  Komut dosyası düzenleyicisinin sol alt kısmındaki açılır kod gezginini kullanarak kod bloklarına daha kolay erişebilirsiniz.

2.  İsimli kod bölümleri, bu kodların başka yerlerde kullanımını kolaylaştırır.

3.  Çalışması uzun süren kod bölümlerini belleğe alarak, sonrasında kullanımı kolaylaştırır.



## Kod Bölümü Ayarlamaları

**knitr** paketi kod bölümlerinizi özelleştirebilecek çok sayıda seçenek sunar. Bu seçeneklere bağlantıdan ulaşabilirsiniz.[buradan](https://yihui.org/knitr/options/)


## Kod Bölümü Ayarlamaları

| Argümanlar                       |  anlamı                                                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| include = TRUE                   | çalıştırdıktan sonra kod bloğunu belgeye ekleme                                                                                     |
| eval = FALSE                      | kodu çalıştırmadan dosyanın işlenmesini sağlar.                                                                                     |
| echo = FALSE                      | kodun gizlenmesini sağlar.                                                                                                          |
| message = FALSE                   | mesajın gizlenmesini sağlar.                                                                                                        |
| warning = FALSE                   | uyarıların gizlenmesini sağlar.                                                                                                     |




| Argümanlar            | anlamı                                                                                                                              |
|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| error = FALSE         | hatalara rağmen dosyanın işlenmesini sağlar.                                                                                        |
| cache = TRUE          | kodun çalışmadan en son önbellekteki halini almaya yarar.                                                                           |
| cache.path            | önbelleğe atılan sonuçların dizini (default = "cache/")                                                                             |
| child                 | oluşturulacak ve eklenecek belge (default = NULL)                                                                                   |
| collapse              | bütün çıktıları tek bir sonuca yığar (default = FALSE)                                                                              |
| comment               | sonuç satırları için örnek (default = '\#\#')                                                                                       |



## Kod Bölümü Ayarlamaları  


| Argümanlar            | anlamı                                                                                                                              |
|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| dependson             | önbellek için blok destek dosyaları (default = NULL)                                                                                |
| fig.align             | 'left', 'right', ya da 'center' (default = 'default')                                                                               |
| fig.cap               | resim altyazısı koyma (default = NULL)                                                                                               |
| fig.height, fig.width | inç cinsinden grafik boyutları                                                                                                      |
| highlight             | kaynak kodu vurgulama (default = TRUE)                                                                                              |
| tidy                  | düzenli (tidy) kodu gösterir (default = FALSE)                                                                                      |




### include

`include = TRUE` kod bloğunu çalıştırdıktan sonra kod bloğunu belgeye ekler.

``` {.r}
{r include=TRUE}
library(airports)
table(usairports$region)
```

`include = TRUE ile calisan blok`


```r
library(airports)
table(usairports$region)
```

```
## 
##  AAL  ACE  AEA  AGL  ANE  ANM  ASO  ASW  AWP 
##  759 1393 2473 3878  843 2267 3210 3428 1364
```




### include

`include = FALSE` kod bloğunu çalıştırdıktan sonra kod bloğunu belgeye eklemez.



`include = FALSE ile calisan blok`




### eval

`eval = TRUE` kodu çalıştırarak dosyanın işlenmesini sağlar.

``` {.r}
{r eval=TRUE}
# atama operatoru kullanimi
x <-3
x
```


```r
x <-3
x
```

```
## [1] 3
```


### eval

`eval = FALSE` kodu çalıştırılmadan dosyanın işlenmesini sağlar.

``` {.r}
{r eval=FALSE}
# atama operatoru kullanimi
x <-3
x
```


```r
x <-3
x
```


### eval & include


- **eval = TRUE** include =FALSE beraber kullanıldığnda kod çalışır ancak çıktı yansıtılmaz. 

- Bu kod blogunda oluşan nesneler ise hem metin içinde hem de kod bloklarinda kullanılabilir.

``` {.r}
{r, eval=TRUE, include = FALSE}
y <-"kod ozellikleri"
y
```




## Çıktılara metin içine aktarma

- Bir r oturumunda oluşan nensneler metin için aşağıdaki şeklinde yazıldığında
metine nesne değeri aktarılır.


```r
`r nrow(usairports)`
```


```r
usairports data setinin  `r nrow(usairports)` satır ve `r ncol(usairports)` sütundan oluşmaktadır.
```

- markdown

- usairports data seti 19615 satır ve 14 sütundan oluşmaktadır.





### Sayısal işlemlerde

- **set.seed()** fonksiyonunun 41 değeri ile kullanarak **rnorm()** fonksiyonu ile ortalaması 50, standart sapması 10 olan bir vektor oluşturulması örneği


```r
set.seed(41)
veri <- rnorm(n=100, mean=50 , sd=10)
```


Metin içinde kullanımı


```r
Olusturulan veri setinin ortalamasi `r mean(veri)`, standart sapması ise `r sd(veri)` dir.
```

Olusturulan veri setinin ortalamasi 51.9031344, standart sapması ise 10.2822903 dir.


## markdown kaynak


- [markdown hatırlatıcı notlar](https://www.markdownguide.org/cheat-sheet/)

- [markdown tablo oluşturucu](https://www.tablesgenerator.com/markdown_tables).







## YAML

YAML - Yet Another Mark up Language - Bir Başka Biçimleme Dili


- themes: cerulean, journal, flatly, darkly, readable, spacelab, united, cosmo, lumen, paper, sandstone, simplex, ve yeti

- styles: tango, pygments, kate, monochrome, espresso, zenburn, haddock, breezedark, ve textmate



## Kaynaklar

- [R Markdown Kitabı](https://bookdown.org/yihui/rmarkdown/) 

- [R Markdown Kitabı](https://r4ds.had.co.nz/r-markdown.html)


- [RStudio R Markdown dersi](https://rmarkdown.rstudio.com/lesson-1.html)

- [RStudio Hatırlatma Notları](https://rstudio.com/resources/cheatsheets/) Türkçe R Markdown cheatsheet var.

- [W3 schools HTML & CSS](https://www.w3schools.com/html/default.asp)






## blogdown

**Amaç:** Web sitesi oluşturmak  
**Kaynak:** [blogdown kitabı](https://bookdown.org/yihui/blogdown/)  
**Örnek:** [https://amber.rbind.io/](https://amber.rbind.io/)  
**Kaynak kodu:** https://github.com/ProQuestionAsker/websiteSource  






## bookdown

**Amaç:** Kitap yazmak  
**Kaynak:** [bookdown kitabı](https://bookdown.org/yihui/bookdown/)  
**Örnek ve kaynak kodu:** [Bookdown örnekleri](https://bookdown.org/)  


## xaringan

**Amaç:** Daha farklı sunumlar yapma  
**Kaynak:** [R Markdown kitabı 7.   bölüm](https://bookdown.org/yihui/rmarkdown/xaringan.html)  




## Öneri

- R Ladies Ankara için Dr. Mine Dogucu'nın yaptığı [minedogucu.com](minedogucu.com) workshopun [örneklerini](https://github.com/mdogucu/rmd-tr/tree/master/ornekler) ve [sunumunu](https://mdogucu.github.io/rmd-tr/sunum/sunum.html#1) bulabilirsiniz.

Sunumu [YouTube](https://www.youtube.com/watch?v=ykmoy3AO_qI&feature=youtu.be)'dan izleyebilirsiniz.



## Şablon

- [ödevlerinizi örnekteki gibi yapabilirsiniz](Kaynaklar/AD_SOYAD_ODEVADI.Rmd)

- [Örnekte kullanılan veri seti](Kaynaklar/dataWBT.csv)
---

## Ödev

- datacamp tan üzerinize atanan ödevi bir sonraki derse gelmeden tamamlayınız.

.large[.hand[Teşekkürler..]]



☕ 
