# PIL.Image.blend(img1, img2, alpha)

Bir alfa değeri kullanarak iki görüntü arasında bir enterpolasyon yapar. Enterpolasyon, belli sınırlar arasında varolan bir fonksiyonda sabit 
aralıklarla alınan verilerin daha küçük aralıklarda hesaplanması (Ekşi sözlük yorumu). Kısacası iki resmi birleştirerek yeni bir görüntü yaratıyoruz. Bu görüntünün
şeffaflık oranını ise biz belirliyoruz.
Unutulmaması gereken önemli bir nokta, her iki görüntünün de aynı boyutta ve aynı modda olması, yani genişlik ve yüksekliğin benzer olması 
ve RGB, RGBA, CMYK gibi modların aynı olması gerektiğidir (Kaynak: https://www.codespeedy.com/python-pil-image-blend-method/). <br>

### Parametreler
* img1, img2 açıklamaya gerek duymuyorum. Bunlar boyutları ve türleri aynı olan iki adet resmimiz.
