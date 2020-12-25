# PIL.Image.new(mod, boyut, renk)
Verilen mod ve boyutta yeni bir görüntü oluşturur. 3 parametre almaktadır. 
## Parametreler
### 1- mod
Bir görüntünün modu, görüntüdeki bir pikselin türünü ve derinliğini tanımlayan bir dizedir. En çok kullanan mod türleri:
* RGB: RGB red(kırmızı), Green(yeşil), Blue(mavi) Renklerin kısaltılması ile oluşturulmuş bir kelimedir. RGB televizyon-bilgisayar gibi elektronik 
ortamlar da kullanılmaktadır. Bu üç rengin birleşimi ile birçok renk ortaya çıkar.  RGB sayısal gösterimi şu şekildedir: (0-255, 0-255, 0-255) 
Bu üç bölümden her biri 0 ile 255 sayıları arasında bir değer alabilir. Yani eğer şu şekilde yaparsak: (0, 0, 0) siyah renk oluşacaktır. <br>
Kullanım: PIL.Image.new("RGB", boyut, renk)
<img src="https://user-images.githubusercontent.com/25556230/103139483-b141b900-46ed-11eb-9955-9f60e0bfa27d.jpg" width="600" height="300">

* RGBA: Görüldüğü gibi RGB den farkı sounda ki A yani alfa kelimesidir. Sondaki alfa görüntünün saydamlığını (opak) ayarlamaktadır. RGBA'nın sayısal gösterimi ise
şöyledir: (255, 0, 0, 0.3)
(255, 0, 0) ile rengimizi kırmızı yaptık ve 0.3 ile saydamlığını ayarladık. 
Kullanım: PIL.Image.new("RGBA", boyut, renk)
<img src="https://user-images.githubusercontent.com/25556230/103139641-472a1380-46ef-11eb-825a-6b0529a03279.png">

* CMYK: mürekkep ve boya kullanan baskı makinelerine ulaşması gereken tasarımların formatıdır. 
Mmürekkep ve boya gibi kimyasal renklendiriciler bu 4 temel renk kartelasından oluşmaktadır ve baskılar bu 4 rengin fiziksel karışımıyla oluşmaktadır.
CMYK‘da temel 4 renk şu şekildedir;<br>
“C = Cyan” “M = Magenta” “Y = Yellow” “K = Key (Siyah)” (kaynak: https://pazarlamailetisimi.com/rgb-ve-cmyk-nedir/)
<img src="https://user-images.githubusercontent.com/25556230/103139724-2dd59700-46f0-11eb-86a5-f4945a485ab3.jpg" width=500 height=400>

* YCbCr: Y ile luminance (parlaklık) sinyalini, Cb ve Cr  ile ise chrominance (renk) bilgilerini saklayan bir renk uzayıdır. 
YCbCr renk uzayı, dünya çapında sayısal video standardı oluşturma çabaları sırasında ortaya çıkmıştır. Y, 8 bitliklik 16-235 aralığında tanımlanmaktadır. 
Cb ve Cr ise de 16-240 arasında tanımlanmaktadır. (kaynak: http://matlabgoruntuisleme.blogspot.com/2012/09/rgbhsvycbcr-renk-uzaylar-md2.html)<br>
<img src="https://user-images.githubusercontent.com/25556230/103140140-1ef0e380-46f4-11eb-91ce-fff74209d7fc.jpg" width=500 height=300>

### 2- boyut
2. parametre olan boyut, resmimizin kaç pixel genişliğinde ve yüksekliğinde olması gerektiğini söyler. 
Kullanımı şöyledir: Image.new('RGB', (500, 300), 'red')
Görüldüğü gibi 500x300 diye bir sayısal değer yazdık. Bu şunu ifade ediyor: Görüntünün genişliği 500 pixel olsun, yüksekliği ise 300.
<img src="https://user-images.githubusercontent.com/25556230/103140274-b1de4d80-46f5-11eb-95d1-c4d50513bf50.png" width=600 height=400>

### 3- renk
Bu parametre, resmimizi oluşturduğumuzda ilk pixel renklerinin ne olacağını ayarlar. Eğer boş bırakırsak (Örnek olarak: Image.new('RGB', (500, 300)) ) default
olarak siyah rengi verir. Aşşağıdaki resimlerde bütün örnekler verilmiştir. 
Sondaki renk bütün kullanımlara uygundur. 
- Image.new('RGB', (500,100), "hsl( 0, 67%, 46% )")
- Image.new('RGB', (500,100), "#B13A3A")
![rb](https://user-images.githubusercontent.com/25556230/103140348-99bafe00-46f6-11eb-895a-529ecc8b2eb0.png)
![rd](https://user-images.githubusercontent.com/25556230/103140349-9b84c180-46f6-11eb-8fa9-b0df4ddd1552.png)
![Ekran Resmi 2020-12-25 21 19 20](https://user-images.githubusercontent.com/25556230/103140377-e0105d00-46f6-11eb-9661-2503dccbe083.png)
