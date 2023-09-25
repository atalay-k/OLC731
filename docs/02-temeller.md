# R Temel Özellikler






- R konsolda gorunen **>** isareti, R yaziliminin sizden komut bekledigini belirtir. R'in hesap makinesi olarak kullanim ornekleri sunulmustur.


```r
2+2
```

```
[1] 4
```
- R boşluklara duyarlı değildir.

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

* Atama operatörü olarak "küçüktür" simgesi ile "kısa çizgi" simgesi **`<- `** simgeleri kullanılabilir.

* **`<- `** yerine "eşittir" **`=`** simgesi de atama operatörü olarak kullanılabilir.

* Ancak **`=`** operatörü programlama yaparken matematiksel eşitlikle karışabilmektedir.


* Atama yapılacak nesne isimlendirilirken harflerle (A* Z veya a* z) başlamalıdır.

* İsimlendirmeye harfle başlandıktan sonra rakamlar (0* 9), nokta (.) ve alt cizgi (\_) ile devam edilebilmektedir.

* R harflerin küçük ve ya büyük olmasına karşı duyarlıdır.

* R fonksiyonlarına benzer isimlerde nesne ismi kullanmamaya **dikkat edilmelidir.**

* Ayrıca **c,C,D,F,I,q,t,T** gibi tek harfli nesne ismi kullanmaktan kaçınılmalıdır; bunların R'da özel anlamları bulunmaktadır.


*  R yazılımında **#** işareti ile başlayan satir, yorum satırıdır.

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

* çıkarma işlemi için **-**,

* çarpma işlemi için  **\***,

* bölme işlemi için **/**,

* üs alma işlemi için  **^** veya *

* mod alma icin ise **%%** operatorleri kullanılmaktadır.

- Kodlamanızın büyük bir kısmı nesne oluşturmayı ve nesneleri manipüle etmeyi içerecektir. Nesneler bir şeyler içerir. Bu şeyler sayılar, kelimeler veya işlemlerin ve analizlerin sonucu olabilir

**Alıştırma Nesneler oluşturma**

* Aşağıdaki kodu kopyalayıp konsola yapıştırın, kodu kendi adınızı ve yaşınızı kullanacak şekilde değiştirin ve çalıştırın. Enviroment bölmesinde `ad`, `yas`, `gun`, `yeniyil` ve `veri` nesnelerinin göründüğünü göreceksiniz.  


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

- Bu örneklerde, `ad`, `yas` ve `yeniyil` her zaman `ada`, `36` değerlerini ve 2024 Yeni Yıl Günü tarihini içerecektir, ancak `gun` tarihi işletim sisteminden alacaktır ve `veri` rastgele oluşturulmuş bir veri kümesi olacaktır, bu nedenle bu nesnelerin değerleri statik olmayacaktır.

- Daha da önemlisi, nesneler hesaplamalara dahil olabilir ve birbirleriyle etkileşime girebilir. Örneğin:


```r
yas + 10
yeniyil - gun
mean(veri)
```

```
[1] 46
Time difference of 116 days
[1] 16.63326
```

- Son olarak, bu işlemlerin sonucunu yeni bir nesnede saklayabilirsiniz:


```r
n1 <- yas + 10
```

<div class="try">
<p>&lt;-<code>ifadesini</code>içerir<code>şeklinde okumak faydalı olabilir, örneğin</code>ad<code>ifadesi</code>ada`
metnini içerir.</p>
</div>

- Bu ders boyunca sürekli olarak nesneler yaratacaksınız ve ilerledikçe onlar ve nasıl davrandıkları hakkında daha fazla bilgi edineceksiniz, ancak şimdilik bunların değerleri kaydetmenin bir yolu olduğunu, bu değerlerin sayı, metin veya işlemlerin sonucu olabileceğini ve yeni değişkenler oluşturmak için başka işlemlerde kullanılabileceğini anlamak yeterlidir.

<div class="info">
<p>Nesnelerin ‘değişkenler’ olarak adlandırıldığını da görebilirsiniz.
Programlama terimlerinde ikisi arasında fark vardır, ancak çok sık
eşanlamlı olarak kullanılırlar.</p>
</div>

**Alıştırma Nesneler oluşturma**

* Aşağıdaki kodu kopyalayıp konsola yapıştırın.
- Eni 4 cm, boyu 10 cm bir dikdörtgenin alanı hesaplayınız.


```r
# en nesnesi tanimlama

# boy nesnesi tanimlama

# alan nesnesi tanimlama

# alan nesnesini yazdirma
```


```
[1] 40
```

- Eni 4 cm, boyu 10 cm bir dikdörtgenin köşegen uzunluğunu hesaplayınız.


```r
# en nesnesi tanimlama

# boy nesnesi tanimlama

# kosegen nesnesi tanimlama

# kosegen nesnesini yazdirma
```



```
[1] 10.77033
```

