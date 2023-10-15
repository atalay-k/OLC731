---
title: "Uretilebilir Rapor 1"
author: "Kubra"
output:
  html_document:
    theme: journal
    toc: true
    toc_float:
      collapsed: false
      smooth_scroll: false
      number_sections: false
---



## Veri Üretim

Burada iki koşullu bir çalışmadan elde edilen verileri simüle edeceğiz. 
A koşulundaki ortalama 0 ve B koşulundaki ortalama 1'dir.


```r
n <- 100

data <- data.frame(
  id = 1:n,
  condition = c("A", "B") |> rep(each = n/2),
  dv = c(rnorm(n/2, 0), rnorm(n/2, 1))
)
```

## Grafik

<img src="repro_files/figure-html/condition-plot-1.png" width="100%" style="display: block; margin: auto;" />
