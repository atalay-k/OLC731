# Betimleyici İstatistik 

<!-- https://statsandr.com/blog/descriptive-statistics-in-r/ -->

<!-- https://rpubs.com/williamsurles/298945 -->

 <!-- https://rpubs.com/odenipinedo/introduction-to-data-visualization-with-ggplot2 -->


## Görselleştirme

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

- Grafiklerin kolay okunması adına `PISA_OGR_2018`  veri setinden veri sayısının azaltılması amacıyla sınıf düzeylerine ilişkin değişkenin her düzeyinden 15'şer kişilik örneklem seçilip toplam 60 gözlemle "df1" nesnesi oluşturulmuştur. 

- Grafik çizimlerinde grup değişkenlerine ihtiyaç duyulduğu için sınıf düzeylerine ve cinsiyete ilişkin değişkenler `as.factor()`fonksiyonuyla kategorik hale getirilmiştir.



```r
load("import/PISA_OGR_2018.rda")
df1 <- PISA_OGR_2018 %>%
dplyr::select(SINIF,CINSIYET,OK_YETERLIK,ODOKUMA1,starts_with("ST097"))  %>%   
  na.omit()%>%
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

- Grafikleri iyi bilinen **ggplot2** paketi grafikleri üzerinden işleyeceğiz.

- **ggplot2** paketindeki grafikler genellikle daha iyi bir görünüme sahiptir ancak daha gelişmiş kodlama becerileri gerektirir (daha fazla bilgi edinmek için "Graphics in R with ggplot2" makalesine bakın). 

- Grafiklerinizi yayınlamanız veya paylaşmanız gerekiyorsa, mümkünse **ggplot2** kullanmanızı öneririm, aksi takdirde varsayılan grafikler işinizi görecektir.

:::{.info data-latex=""}
İpucu: Yakın zamanda [**esquisse**](https://dreamrs.github.io/esquisse/index.html) eklentilerinden ggplot2 oluşturucusunu keşfettim. Kendiniz kodlamak zorunda kalmadan **ggplot2** paketinden nasıl kolayca grafik çizebileceğinizi görün.
:::

- Bu sayfa görüntülenen tüm grafikler özelleştirilebilir. Örneğin, başlığı, x ve y ekseni etiketlerini, rengi vb. düzenlemek mümkündür. 










































































