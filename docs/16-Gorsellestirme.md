# Görselleştirme

<!-- https://statsandr.com/blog/descriptive-statistics-in-r/ -->

<!-- https://rpubs.com/williamsurles/298945 -->

 <!-- https://rpubs.com/odenipinedo/introduction-to-data-visualization-with-ggplot2 -->




![](images\v1.PNG){width=50%}


![](images\v2.PNG){width=50%}

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

- Grafiklerin kolay okunması adına `PISA_OGR_2018`  veri setinden veri sayısının azaltılması amacıyla sınıf (9. ve 10.) düzeylerine ilişkin değişkenin her düzeyinden 100'şer kişilik örneklem seçilip toplam 200 gözlemle "df1" nesnesi oluşturulmuştur. 




```r
load("import/PISA_OGR_2018.rda")
library(dplyr)
df1 <- PISA_OGR_2018 %>%
select(SINIF,CINSIYET,OK_YETERLIK,ODOKUMA1,starts_with("ST097"))  %>%   
  na.omit()

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


- Grafik çizimlerinde grup değişkenlerine ihtiyaç duyulduğu için sınıf düzeylerine ve cinsiyete ilişkin değişkenler `as.factor()` fonksiyonuyla kategorik hale getirilmiştir.



```r
library(expss)
df2 <- df1 %>% 
  drop_var_labs() %>% 
  filter(SINIF %in%c(9,10))%>% 
  group_by(SINIF)%>%
  sample_n(100, replace=TRUE) %>%
    ungroup()%>%  
  mutate(SINIF=as.factor(SINIF), CINSIYET=as.factor(CINSIYET)) 
```


## ggplot

- Grafikleri iyi bilinen **ggplot2** paketi grafikleri üzerinden işleyeceğiz.

- **ggplot2** paketindeki grafikler genellikle daha iyi bir görünüme sahiptir ancak daha gelişmiş kodlama becerileri gerektirir (daha fazla bilgi edinmek için "Graphics in R with ggplot2" makalesine bakın). 

- Grafiklerinizi yayınlamanız veya paylaşmanız gerekiyorsa, mümkünse **ggplot2** kullanmanızı öneririm, aksi takdirde varsayılan grafikler işinizi görecektir.

:::{.info data-latex=""}
İpucu: Yakın zamanda [**esquisse**](https://dreamrs.github.io/esquisse/index.html) eklentilerinden ggplot2 oluşturucusunu keşfettim. Kendiniz kodlamak zorunda kalmadan **ggplot2** paketinden nasıl kolayca grafik çizebileceğinizi görün.
:::

- Bu sayfa görüntülenen tüm grafikler özelleştirilebilir. Örneğin, başlığı, x ve y ekseni etiketlerini, rengi vb. düzenlemek mümkündür. 


```r
library(ggplot2)
ggplot(df2,aes(x=ODOKUMA1)) + geom_histogram()
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-2-1.png" width="100%" style="display: block; margin: auto;" />

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


## Histogram 

- Aşağıdaki kod sadece ilk katmanı oluşturur.


```r
grafik_1 <- ggplot(df2, aes(x=ODOKUMA1))
grafik_1 
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-4-1.png" width="80%" style="display: block; margin: auto;" />

### Katman eklenmesi


```r
grafik_1 + geom_histogram()
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-5-1.png" width="50%" style="display: block; margin: auto;" />

###  Yüzey eklenmesi




```r
grafik_1 +
  geom_histogram()  +
  facet_wrap(~CINSIYET, nrow=2)
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-6-1.png" width="50%" style="display: block; margin: auto;" />



```r
grafik_1 + 
  geom_histogram() +
   facet_wrap(~SINIF, nrow=2)
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-7-1.png" width="50%" style="display: block; margin: auto;" />

- **facet_grid** fonksiyonu ise hem tek hem de iki değişkenin panellerde gösterimi için 

  - **facet_grid(satırdeğişkeni~sütundeğişkeni)** 
  
  - **facet_grid(satırdeğişkeni~.)** veya     
  
  - **facet_grid(.~sütundeğişkeni)**



- Yüzeyde kategorik değişkenlerin düzeylerini görebilmek için **factor** değişken olarak tanımlamak gerekir.


```r
library(haven)
df2 <- 
  df2 %>% 
  mutate_if(is.labelled, funs(as_factor(.)))
```


```r
 ggplot(df2, aes(x=ODOKUMA1)) +
  geom_histogram()+
  facet_grid(SINIF~CINSIYET)
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-9-1.png" width="80%" style="display: block; margin: auto;" />


- Yüzeylerin sütunda oluşturulması


```r
ggplot(df2,aes(x=ODOKUMA1))+
  geom_histogram()+
  facet_grid(.~CINSIYET)
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-10-1.png" width="40%" style="display: block; margin: auto;" />

- Yüzeylerin satırlarda oluşturulması

```r
ggplot(df2,aes(x=ODOKUMA1))+
  geom_histogram()+
  facet_grid(CINSIYET~.)
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-11-1.png" width="40%" style="display: block; margin: auto;" />



```r
ggplot(df2,aes(x=ODOKUMA1))+
  geom_histogram()+
  facet_grid(.~SINIF)
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-12-1.png" width="100%" style="display: block; margin: auto;" />





```r
ggplot(df2,aes(x=ODOKUMA1))+
  geom_histogram()+
  facet_grid(SINIF~.)
```

```
## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-13-1.png" width="100%" style="display: block; margin: auto;" />


###  gruplama değişkenleri

- Renklendirme, sembol şekli, sembol büyüklüğü ve çizgi türü belirleyen fonksiyonlar yardımıyla gruplama yapılmaktadır.


#### color ile gruplandırma

- Açıklama kutucukları otomatik çıkar!


```r
p1 <- ggplot(
      df2 %>% 
      group_by(SINIF,CINSIYET) %>%
      mutate(ort=mean(ODOKUMA1)) %>% ungroup(),
     aes(x=SINIF, y=ort, color=CINSIYET )) +
  geom_point() +  
  xlab("Sınıf Düzeyi")+
  ylab("Ortalama Puan") 

p1
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-14-1.png" width="100%" style="display: block; margin: auto;" />

- Yüzey eklenmiş garfiklerde de gruplama değişkeni kullanılabilir.



```r
ggplot(df2,aes(x=ODOKUMA1,y=OK_YETERLIK,color=CINSIYET)) +
  geom_point()+
  facet_grid(.~SINIF)	
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-15-1.png" width="100%" style="display: block; margin: auto;" />


## Grafik nesnesi

- Oluşturulan grafik **p** nesnesine atanmıştır. **p** nesnesine **+** ile katmanlar eklenebilir.
- Kategorik degişkenler eksen değerlerini belirler.



```r
p <- ggplot(mtcars, aes(cyl, mpg)) +
  geom_point()
p
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-16-1.png" width="100%" style="display: block; margin: auto;" />


- cyl değişkenin sadece 4,6 ve 8 değerlerini eksende belirtmek için factor olarak tanımlamak gerekir.


```r
ggplot(mtcars, aes(factor(cyl), mpg)) +
  geom_point()
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-17-1.png" width="100%" style="display: block; margin: auto;" />

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
ggplot(df2, aes(CINSIYET, OK_YETERLIK)) +
  geom_point(color = "blue")
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-18-1.png" width="100%" style="display: block; margin: auto;" />

### **size** ve **shape** parametresi

- her iki parametrenin de olağan değeri 1 dir. 

```r
ggplot(df2, aes(CINSIYET, OK_YETERLIK)) +
  geom_point(color = "blue",size=5,shape="a")
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-19-1.png" width="100%" style="display: block; margin: auto;" />


- color argümanı ile renklendirme


```r
ggplot(df2, aes(CINSIYET, OK_YETERLIK, color = SINIF)) +
  geom_point()
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-20-1.png" width="100%" style="display: block; margin: auto;" />


- Üstüse gelen noktalar için **position**

-   identity
-   dodge
-   stack
-   fill
-   jitter
-   jitterdodge
-   nudge



```r
ggplot(df2, aes(CINSIYET, OK_YETERLIK, color = SINIF)) +
  geom_point()
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-21-1.png" width="100%" style="display: block; margin: auto;" />



```r
ggplot(df2, aes(CINSIYET, OK_YETERLIK, color = SINIF)) +
  geom_point(position = "jitter")
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-22-1.png" width="100%" style="display: block; margin: auto;" />

### **size** parametresi

- parametreler için veri setinden bir değişken değeri seçilebilir.


```r
ggplot(df2, aes(CINSIYET, OK_YETERLIK, size = SINIF)) +
  geom_point()
```

```
## Warning: Using size for a discrete variable is not advised.
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-23-1.png" width="100%" style="display: block; margin: auto;" />

- **size** parametresi  üst üste binen noktaları kaydırarak ayırma


```r
ggplot(df2, aes(CINSIYET, OK_YETERLIK, size = SINIF)) +
  geom_point(position = "jitter")
```

```
## Warning: Using size for a discrete variable is not advised.
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-24-1.png" width="100%" style="display: block; margin: auto;" />


## Katmanlar

![](images/v4.PNG)

### alpha

- Şeffaflık düzeyi için **alpa**

```r
ggplot(df2, aes(ODOKUMA1, OK_YETERLIK, color = SINIF)) +
  geom_point(alpha = 0.4)
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-25-1.png" width="100%" style="display: block; margin: auto;" />

- Katmanları nesneye ekleme
**grafik1** adlı nesneye istenilen katmanlar eklenebilir.


```r
grafik1 <- ggplot(df2, aes(ODOKUMA1, OK_YETERLIK, color = SINIF))
grafik1 +geom_point(alpha = 1.2)
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-26-1.png" width="100%" style="display: block; margin: auto;" />


**grafik1** adlı nesneye CINSIYET değişkenine göre şekil ekleme


```r
grafik1 +geom_point(aes(shape=CINSIYET))
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-27-1.png" width="100%" style="display: block; margin: auto;" />


### **text**

Değişken adları **text** komutu ile veri sembolü olarak eklenebilir. Gösterim amacıyla **df** veri setinin sadece ilk 10 satırı kullanılmıştır.


```r
ggplot(df2[1:10,], aes(ODOKUMA1, OK_YETERLIK))+
         geom_text(aes(label = CINSIYET))
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-28-1.png" width="100%" style="display: block; margin: auto;" />

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
ggplot(df2, aes(x = ODOKUMA1,y = OK_YETERLIK, color = CINSIYET)) +
geom_point(position = "jitter") +
scale_x_continuous("Okuma Puanları") +
scale_color_discrete("Cinsiyet")
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-29-1.png" width="100%" style="display: block; margin: auto;" />

### *limits**


```r
ggplot(df2, aes(x = ODOKUMA1,
y = OK_YETERLIK,
color = CINSIYET)) +
geom_point(position = "jitter") +
scale_x_continuous("Okuma Puanları",limits = c(100,900)) +
scale_color_discrete("Cinsiyet")
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-30-1.png" width="100%" style="display: block; margin: auto;" />

### *breaks


```r
ggplot(df2, aes(x = ODOKUMA1,
y = OK_YETERLIK,
color = CINSIYET)) +
geom_point(position = "jitter") +
scale_x_continuous("Okuma Puanları",limits = c(100,900),
         breaks=seq(100,900,100)) +
scale_color_discrete("Cinsiyet")
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-31-1.png" width="100%" style="display: block; margin: auto;" />


###  expand


```r
ggplot(df2, aes(x = ODOKUMA1,
y = OK_YETERLIK,
color = CINSIYET)) +
geom_point(position = "jitter") +
scale_x_continuous("Okuma Puanları",limits = c(100,900),
                   breaks=seq(100,900,100),
                   expand=c(0,0)) +
scale_color_discrete("Cinsiyet")
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-32-1.png" width="100%" style="display: block; margin: auto;" />

### labs


```r
ggplot(df2, aes(x = ODOKUMA1,
y = OK_YETERLIK,
color = CINSIYET)) +
geom_point(position = "jitter") +
  labs(x = "\nBasari Puanları",
       y = "\nYeterlik Puanları",
       color = "Grup")
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-33-1.png" width="100%" style="display: block; margin: auto;" />

## Bar Grafiği


```r
ggplot(df2, aes(CINSIYET, fill = SINIF)) +   geom_bar() +
  labs(x = "Cinsiyet",
       y = "Frekans")
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-34-1.png" width="100%" style="display: block; margin: auto;" />

## scale_fill


```r
ggplot(df2, aes(CINSIYET, fill = SINIF)) +
  geom_bar() +
   labs(x = "Cinsiyet",
       y = "Frekans") +
  scale_fill_manual("CINSIYET", values = c("red","blue","orange","green",
                                           "darkblue","purple"))
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-35-1.png" width="100%" style="display: block; margin: auto;" />



## Bar Grafikleri

```r
ggplot(data = PISA_OGR_2018, mapping = aes(x = CINSIYET)) +
  geom_bar()
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-36-1.png" width="100%" style="display: block; margin: auto;" />



```r
# df2 <- mutate(df2, Cinsiyet = factor(
#   CINSIYET,
#   c(1, 2),
#   c("kiz", "erkek")
# ))

ggplot(data = df2, mapping = aes(x = CINSIYET)) +
  geom_bar()
```

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-37-1.png" width="100%" style="display: block; margin: auto;" />


```r
ggplot(data = df2, mapping = aes(x = CINSIYET)) + 
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

<img src="16-Gorsellestirme_files/figure-html/unnamed-chunk-38-1.png" width="100%" style="display: block; margin: auto;" />








- teşekkürler !

--


- 😕

- 😄





