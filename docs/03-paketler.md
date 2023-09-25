# R Paketler

- R'yi yüklediğinizde, veri işleme ve istatistiksel analiz seçenekleri de dahil olmak üzere bir dizi fonksiyona erişebilirsiniz. Varsayılan kurulumda yer alan fonksiyonlar genellikle **Temel R** olarak adlandırılır ve birçok Temel R fonksiyonunu gösteren faydalı bir cheatsheet sayfası vardır [cheatsheet](https://github.com/rstudio/cheatsheets/raw/main/base-r.pdf) 
- Bununla birlikte, R'nin gücü genişletilebilir ve açık kaynak olmasıdır - basitçe söylemek gerekirse, bir fonksiyon mevcut değilse veya çok iyi çalışmıyorsa, herkes yeni görevleri gerçekleştirmenize olanak tanıyan veri ve kod içeren yeni bir **paket** oluşturabilir. Base R'yi telefonunuzda gelen varsayılan uygulamalar, paketleri ise ayrıca indirmeniz gereken ek uygulamalar olarak düşünmek faydalı olabilir.

*  R fonksiyonları ayrı paketler halinde düzenlenmişlerdir. Böylece gerekli paketlerle çalışarak daha az bellek kullanımı ve hızlı işlem gücü sağlanır.

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


![yükle* etkinleştir](images/packagebulb.png)


### Alıştırma :  tidyverse yükleme

- Bir paketi kullanabilmek için önce onu yüklemeniz gerekir. Aşağıdaki kod, bu derste çok sık kullanacağımız bir paket olan `tidyverse` paketini yükler.


```r
install.packages("tidyverse")
```

- Bir paketi yalnızca bir kez yüklemeniz gerekir, ancak R'yi her başlattığınızda kullanmak istediğiniz paketleri yüklemeniz gerekir, benzer şekilde telefonunuza bir uygulamayı bir kez yüklemeniz gerekir, ancak her kullanmak istediğinizde açmanız gerekir.

**UYARI: WARNING: Rtools is required to build R packages" gibi bir hata mesajı alırsanız, [Rtools] (https://cran.r-project.org/bin/windows/Rtools/) adlı ekstra bir yazılım indirmeniz ve yüklemeniz gerekebilir.**



### Alıştırma : tidyverse etkinleştir

* Tidyverse'i etkinleştirmek için aşağıdaki kodu çalıştırın.  


```r
library(tidyverse)
```

Bir hata mesajı gibi görünen bir şey alacaksınız - öyle değil. Bu sadece R'nin size ne yaptığını anlatmasıdır.

Şimdi `tidyverse` paketini etkinleştirdiğimize göre, içerdiği fonksiyonlardan herhangi birini kullanabiliriz, ancak unutmayın, R'yi her başlattığınızda `library()` fonksiyonunu çalıştırmanız gerekir.

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

- R ve R Studio güncellemelerine ek olarak, paketlerin yazarları da bazen kodlarını günceller. Bu, bir pakete işlev eklemek için olabileceği gibi hataları düzeltmek için de olabilir. Kaçınılması gereken bir şey, yüklü bir paketi istemeden güncellemektir. `install.packages()` işlevini çalıştırdığınızda, her zaman paketin en son sürümü yüklenir ve yüklemiş olabileceğiniz eski sürümlerin üzerine yazılır. Bazen bu bir sorun teşkil etmez, ancak bazen paket önemli ölçüde değiştiği için güncellemenin kodunuzun artık çalışmadığı anlamına geldiğini görürsünüz. Bir paketin eski bir sürümüne geri dönmek mümkündür ancak yine de bundan kaçınmaya çalışın.

\begin{danger}
Bir paketin üzerine yanlışlıkla daha sonraki bir sürümün yazılmasını
önlemek için, sizin veya bir başkasının kodu yanlışlıkla çalıştırması
ihtimaline karşı analiz komut dosyalarınıza \texttt{install.packages()}
i \textbf{asla} dahil etmemelisiniz.
\end{danger}


## R ve RStudio'ya nasıl alıntı yapılır

- R'ye atıfta bulunmanız ve referans vermeniz gereken bilimsel bir rapor yazmaktan biraz uzak olabilirsiniz, ancak zamanı geldiğinde bunu onu geliştiren insanlara (çoğu ücretsiz!) kredi vermek için yapmak önemlidir. R, RStudio ve kullandığınız paketler için ayrı alıntılar sağlamalısınız.

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

Kullandığınız herhangi bir paket için atıf oluşturmak için, atıf yapmak istediğiniz paketin adıyla birlikte `citation()` işlevini de kullanabilirsiniz.


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
