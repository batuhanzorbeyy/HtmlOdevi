# Git branch ve merge conflict ödevi

Repo: https://github.com/batuhanzorbeyy/HtmlOdevi

## Hazırlanan dallar

- `feature/login-turkce`: Giriş formundaki başlığı `Giriş Yap` olarak değiştirir.
- `feature/login-karsilama`: Aynı başlığı `Hoş Geldiniz` olarak değiştirir.

İki dal aynı main commit'inden ayrıldı. Çakışacak dosya: `htmldersleri/LoginForm/page.html`.

## GitHub Desktop ve VS Code ile tamamla

1. GitHub Desktop'ta bu repoyu klonla veya Fetch origin yap. Bekleyen yerel değişiklik varsa önce kaydet ve commit et.
2. Current Branch menüsünden `feature/login-turkce` dalına geç. Yerel dalın gerideyse Pull origin yap.
3. Branch → Merge into current branch menüsünden `feature/login-karsilama` dalını seç ve birleştirmeyi başlat.
4. Çakışan `htmldersleri/LoginForm/page.html` dosyasını VS Code'da aç. Çakışmanın ekran görüntüsünü al.
5. İşaretlerle çevrelenen çakışmalı başlık bloğunun tamamını şu iki satırla değiştir; dosyanın diğer satırlarını koru:

```html
    <h1>Hoş Geldiniz</h1>
    <p>Devam etmek için giriş yapın.</p>
```

6. `<<<<<<<`, `=======` ve `>>>>>>>` işaretlerini kaldırdığından emin ol ve dosyayı kaydet. Üç panelli Merge Editor kullanıyorsan Result bölümünü düzenle ve Complete Merge ile dosyayı hazırla.
7. GitHub Desktop'a dön, Continue merge ile birleştirmeyi commit et, ardından Push origin yap.
8. Çözülmüş kodu ve GitHub Desktop History sekmesindeki birleştirme kaydını ekran görüntüsü olarak kaydet. Windows + Shift + S ile ekran görüntüsü alabilirsin.

## Teslim

- Repo bağlantısını ve gerçek çakışma/çözüm ekran görüntülerini LMS'ye yükle.
- İki feature dalını değerlendirme bitene kadar silme.
- Bu rehber, GitHub Desktop ve VS Code adımlarının tamamlandığına dair kanıt değildir. Ekran görüntülerini işlemi kendi bilgisayarında yaparken al.

Birleştirme burada `feature/login-turkce` üzerinde tamamlanır; ödev maddeleri main'e birleştirmeyi zorunlu tutmuyor.
