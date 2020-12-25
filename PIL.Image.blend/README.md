# PIL.Image.blend(img1, img2, alpha)

Bir alfa değeri kullanarak iki görüntü arasında bir enterpolasyon yapar. Enterpolasyon, belli sınırlar arasında varolan bir fonksiyonda sabit 
aralıklarla alınan verilerin daha küçük aralıklarda hesaplanması (Ekşi sözlük yorumu). Kısacası iki resmi birleştirerek yeni bir görüntü yaratıyoruz. Bu görüntünün
şeffaflık oranını ise biz belirliyoruz.
Unutulmaması gereken önemli bir nokta, her iki görüntünün de aynı boyutta ve aynı modda olması, yani genişlik ve yüksekliğin benzer olması 
ve RGB, RGBA, CMYK gibi modların aynı olması gerektiğidir (Kaynak: https://www.codespeedy.com/python-pil-image-blend-method/). <br>

Blend yönteminde kullanılan matematiksel denklem.

```
out = image1 * (1.0 - alpha) + image2 * alpha
```

## Parametreler
* img1 ve img2 parametrelerini açıklamaya gerek duymuyorum. Bunlar boyutları ve türleri aynı olan iki adet resmimiz.

* alpha: resimlerin karışım oranını belirler. Örneklerle daha iyi anlaşılacaktır.


## Örnekler
* İlk önce 2 adet resmi Image.open ile açarak img1 ve img2 değişkenlerine atıyoruz.
```
img1 = Image.open("face.jpg")
img2 = Image.open("face2.jpg")
```
img1:<br>
<img src="https://user-images.githubusercontent.com/25556230/103141973-d80fe780-470d-11eb-960e-ecb20c7bfa9d.jpg" width=200 height=200>

img2:<br>
<img src="https://user-images.githubusercontent.com/25556230/103141975-da724180-470d-11eb-8f9f-ccf46697134b.jpg" width=200 height=200>


* İki resmi Image.blend() ile birleştirerek alpha değerini değiştirelim.
```
image_alpha = Image.blend(img1, img2, 0.0)
image_alpha.show()
```
Görüldüğü gibi alpha değerine 0.0 verdik. Bu bize img1 resmini döndürecek. Eğer 1.0 yaparsak img2 resmini döndürür. 0.0 ve 1.0 da aslında görünen hiçbir değişiklik olmayacaktır. Ama eğer bu sayıda daha spesifik bir değişiklik yaparsak fark anlaşılacaktır.

* Şimdi alpha değerini 0.3, 0.5 ve 0.7 yaparak birleştirmeyi görelim.
```
image_alpha = Image.blend(img1, img2, 0.5)
image_alpha.show()
```
Çıktı: 0.5 ile her iki resmi ortak şekilde birleştirdi. <br>
![Ekran Resmi 2020-12-26 00 09 41](https://user-images.githubusercontent.com/25556230/103142093-f4f8ea80-470e-11eb-9fc8-093929f4a22c.png)
```
image_alpha = Image.blend(img1, img2, 0.3)
image_alpha.show()
```
Çıktı: 0.0 nasıl bize img1 veriyorsa 0.3 te bize img1 ağırlıklı alarak onun üstüne img2'yi koyar. Bu sayıyı arttırdıkça img2 resim üzerinde daha da belirecektir.
Görüldüğü gibi img1 daha baskındır. <br>
![Ekran Resmi 2020-12-26 00 10 43](https://user-images.githubusercontent.com/25556230/103142095-faeecb80-470e-11eb-8582-01814af03b4e.png)
```
image_alpha = Image.blend(img1, img2, 0.7)
image_alpha.show()
```
Çıktı: 0.7 yaparsak bu sefer img2 ağırlı olarak alıp, img1'i onun üstüne yerleştirecek. Görüldüğü gibi img2 daha baskındır. <br>
![Ekran Resmi 2020-12-26 00 10 20](https://user-images.githubusercontent.com/25556230/103142094-f9bd9e80-470e-11eb-8137-2dfc017ef75a.png)
