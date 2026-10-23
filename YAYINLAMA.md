# Siteyi yayına alma

## 1. GitHub Pages (ücretsiz)

1. GitHub'da **`ayse-solmaz.github.io`** adında yeni bir **public** repo aç. İsim tam olarak bu olmalı.
2. Bu klasördeki `index.html` dosyasını repoya yükle ("Add file → Upload files" yeterli).
3. 1–2 dakika sonra site şu adreste açılır: **https://ayse-solmaz.github.io**

Terminalden yapmak istersen:

```bash
cd site
git init
git add index.html
git commit -m "Kişisel site"
git branch -M main
git remote add origin https://github.com/ayse-solmaz/ayse-solmaz.github.io.git
git push -u origin main
```

Siteyi güncellemek için `index.html`'i düzenleyip tekrar push etmen yeterli.

## 2. Domain (isteğe bağlı, yılda yaklaşık 10–15 $)

1. Cloudflare Registrar veya Namecheap'ten bir domain al (ör. `aysesolmaz.com` / `aysesolmaz.dev`).
2. GitHub'da repo → **Settings → Pages → Custom domain** alanına domaini yaz, kaydet.
3. Domain sağlayıcının DNS ayarlarına şunları ekle:
   - `A` kayıtları (`@`): `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` kaydı (`www`): `ayse-solmaz.github.io`
4. DNS oturunca (birkaç dakika ile birkaç saat arası) **Enforce HTTPS** kutusunu işaretle.

## Sonradan düzenlemek isteyebileceğin yerler

- Profil fotoğrafı: `index.html` içinde `avatars.githubusercontent.com` geçen iki satır.
- İletişim bölümüne e-posta eklemek istersen `#iletisim` bölümüne bir `mailto:` linki ekle.
- Yeni proje eklemek için `<article class="card">` bloklarından birini kopyalaman yeterli.
