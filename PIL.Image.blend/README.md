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
img1:
<img src="https://user-images.githubusercontent.com/25556230/103141973-d80fe780-470d-11eb-960e-ecb20c7bfa9d.jpg" width=200 height=200>

img2:
<img src="https://user-images.githubusercontent.com/25556230/103141975-da724180-470d-11eb-8f9f-ccf46697134b.jpg" width=200 height=200>


* İki resmi Image.blend() ile birleştirerek alpha değerini değiştirelim.
```
image_alpha = Image.blend(img1, img2, 0.0)
image_alpha.show()
```
