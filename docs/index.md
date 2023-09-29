---
title: "OLC731" # edit
subtitle: "R YAZILIMI ILE VERI ANALIZI" 
author: "Kubra Atalay Kabasakal" # edit
date: "2023-09-29"
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

(İzlence) [**İzlence**](https://akts.hacettepe.edu.tr/ders_detay.php?ders_ref=DRSTNM_0000000000000000000018497&ders_kod=OLC731&zs_link=2&prg_kod=21134&submenuheader=2).

## Eğitmen {.unnumbered}

`<svg aria-hidden="true" role="img" viewBox="0 0 448 512" style="height:1em;width:0.88em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:black;overflow:visible;position:relative;"><path d="M224 0c70.7 0 128 57.3 128 128s-57.3 128-128 128s-128-57.3-128-128S153.3 0 224 0zM209.1 359.2l-18.6-31c-6.4-10.7 1.3-24.2 13.7-24.2H224h19.7c12.4 0 20.1 13.6 13.7 24.2l-18.6 31 33.4 123.9 39.5-161.2c77.2 12 136.3 78.8 136.3 159.4c0 17-13.8 30.7-30.7 30.7H265.1 182.9 30.7C13.8 512 0 498.2 0 481.3c0-80.6 59.1-147.4 136.3-159.4l39.5 161.2 33.4-123.9z"/></svg>`{=html} [Dr. Kübra Atalay Kabasakal](https://avesis.hacettepe.edu.tr/katalay)

`<svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:1em;width:1em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:black;overflow:visible;position:relative;"><path d="M64 112c-8.8 0-16 7.2-16 16v22.1L220.5 291.7c20.7 17 50.4 17 71.1 0L464 150.1V128c0-8.8-7.2-16-16-16H64zM48 212.2V384c0 8.8 7.2 16 16 16H448c8.8 0 16-7.2 16-16V212.2L322 328.8c-38.4 31.5-93.7 31.5-132 0L48 212.2zM0 128C0 92.7 28.7 64 64 64H448c35.3 0 64 28.7 64 64V384c0 35.3-28.7 64-64 64H64c-35.3 0-64-28.7-64-64V128z"/></svg>`{=html} [kkatalay\@gmail.com](mailto:kkatalay@gmail.com){.email}

`<svg aria-hidden="true" role="img" viewBox="0 0 512 512" style="height:1em;width:1em;vertical-align:-0.125em;margin-left:auto;margin-right:auto;font-size:inherit;fill:black;overflow:visible;position:relative;"><path d="M64 112c-8.8 0-16 7.2-16 16v22.1L220.5 291.7c20.7 17 50.4 17 71.1 0L464 150.1V128c0-8.8-7.2-16-16-16H64zM48 212.2V384c0 8.8 7.2 16 16 16H448c8.8 0 16-7.2 16-16V212.2L322 328.8c-38.4 31.5-93.7 31.5-132 0L48 212.2zM0 128C0 92.7 28.7 64 64 64H448c35.3 0 64 28.7 64 64V384c0 35.3-28.7 64-64 64H64c-35.3 0-64-28.7-64-64V128z"/></svg>`{=html} [katalay\@hacettepe.edu.tr](mailto:katalay@hacettepe.edu.tr){.email}

## Kitaplar {.unnumbered}

-   Atar, B., Atalay Kabasakal, K, Unsal Ozberk, E. B., Ozberk, E. H. & Kibrislioglu Uysal, N. (2020). R ile Veri Analizi ve Psikometri Uygulamaları, Pegem Akademi, Ankara.

-   Desjardins, C. D., & Bulut, O. (2018). [Handbook of educational measurement and psychometrics using R](https://www.routledge.com/Handbook-of-Educational-Measurement-and-Psychometrics-Using-R/Desjardins-Bulut/p/book/9780367734671). Boca Raton, FL: CRC Press.

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




