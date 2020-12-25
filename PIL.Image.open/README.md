# PIL.Image.open(dosyaAdı, mod)
Verilen görüntü dosyasını açar ve tanımlar.

### Parametreler
* dosyaAdı: Dosya adı yazan yere açmak istediğimiz görüntünün adını yazıyoruz.<br>
Örnek: PIL.Image.open("resim.jpg")

* mod: Bu parametreyi vermemize gerek yoktur fakat verildiği zaman "r" yazılmalıdır. r=read <br>
Örnek: PIL.Image.open("resim.jpg", "r")
<img src="https://user-images.githubusercontent.com/25556230/103140847-b9edbb80-46fc-11eb-851b-c01a258c5cd3.png" width=500 height=100>

Kaynak koduna baktığımız zaman fark olmadığını görürüz. İf mode r'ye eşit değilse hata mesajı yolluyor.

<img src="https://user-images.githubusercontent.com/25556230/103140844-b8bc8e80-46fc-11eb-9ce4-b960d6a7a55e.png" width=500 height=100>

### Hata mesajları ve anlamları

* FileNotFoundError – Dosya bulunamazsa bu hatayı döndürür.
* PIL.UnidentifiedImageError – Görüntü açılamıyorsa ve tanımlanamıyorsa bu hatayı döndürür.
* ValueError – Mod "r" değilse veya dosyaAdı için bir StringIO örneği kullanılıyorsa bu hatayı döndürür.
