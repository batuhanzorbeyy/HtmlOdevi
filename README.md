# HtmlOdevi — Git Merge Conflict Çalışması

HTML ve CSS ile hazırlanmış giriş, arama, iletişim ve hakkımızda sayfalarını içeren web projesi.

## İki feature dalı

| Dal | Giriş sayfasındaki değişiklik |
| --- | --- |
| `feature/login-turkce` | `<h1>Login</h1>` → `<h1>Giriş Yap</h1>` |
| `feature/login-karsilama` | `<h1>Login</h1>` → `<h1>Hoş Geldiniz</h1>` |

İki dal `a4ef09a45e3b6d77602b37f6f1ab18292bca4e77` ortak commit'inden oluşturuldu. Aynı dosyanın aynı satırına farklı içerikler yazıldığı için birleştirme gerçek bir içerik çakışması oluşturdu.

## Çakışan dosya

`htmldersleri/LoginForm/page.html`

Git tarafından üretilen çakışmalı bölüm:

```html
<<<<<<< HEAD
    <h1>Giriş Yap</h1>
=======
    <h1>Hoş Geldiniz</h1>
>>>>>>> origin/feature/login-karsilama
```

## Uygulanan çözüm

Karşılama başlığı korundu, giriş yapma yönlendirmesi ayrı bir paragraf olarak eklendi:

```html
    <h1>Hoş Geldiniz</h1>
    <p>Devam etmek için giriş yapın.</p>
```

Çakışma işaretleri kaldırıldı; iki dalın geçmişini koruyan iki ebeveynli bir merge commit ile sonuç `homework/merge-cozumu` dalında kaydedildi. Formun diğer alanları korunmuştur.

## Doğrulama ve teslim durumu

- İki feature dalı GitHub'da bulunuyor.
- Gerçek Git birleştirmesinde `CONFLICT (content)` gözlendi.
- Çözüm yerel Git ortamında commit edilerek doğrulandı; `git diff --cached --check` başarılı oldu.
- Çözülmüş dosya ve iki ebeveynli birleştirme kaydı GitHub'da yayımlandı.
- Bu uygulama Codex'in Git ortamı ve GitHub bağlantısı ile yapıldı. GitHub Desktop veya VS Code kullanıldığına dair bir iddia değildir.
- Ödevin GitHub Desktop + VS Code ekran görüntüsü şartı ayrıca tamamlanmalıdır. GitHub ekran görüntüsü bu uygulama şartının yerine geçmez.
- LMS teslimi henüz yapılmadı.

## Desktop ve VS Code'da yeniden uygulama

Feature dallarının uçları korunmuştur. `feature/login-turkce` dalına geçip `feature/login-karsilama` dalını birleştirerek çakışmayı yeniden oluşturabilirsiniz; `main` dalına geçmeniz gerekmez. Ayrıntılı adımlar: [MERGE-ODEVI.md](MERGE-ODEVI.md).
