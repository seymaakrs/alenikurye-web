# Aleni Kurye — alenikurye.com

Sapanca, Maşukiye, Kartepe ve Sakarya bölgesinde 7/24 eve servis kurye sitesinin kaynak kodu. Tek sayfa statik site, GitHub Pages ile yayında.

- **Yayın:** https://alenikurye.com
- **Telefon:** 0552 716 19 68
- **Hosting:** GitHub Pages (`main` branch → `.github/workflows/deploy.yml`)

## Yapı

```
index.html              # Tüm site (HTML + CSS + JS tek dosya)
404.html                # Yanlış URL'de marka uyumlu 404 + anasayfaya yönlendirme
favicon.svg             # Sekme ikonu
manifest.webmanifest    # PWA / "Ana ekrana ekle"
sitemap.xml             # Google için site haritası
robots.txt              # Arama motoru kuralları
CNAME                   # alenikurye.com bağlantısı (GitHub Pages için)
.nojekyll               # GitHub Pages'a "olduğu gibi yayınla" der
.github/workflows/      # Otomatik deploy robotu
fonts/                  # Yedek lokal yazı tipleri (şu an Google Fonts kullanılıyor)
images/                 # Boş — gelecekteki hero/servis fotoğrafları için
CANLIYA_ALMA.md         # DNS + Google Search Console + Business Profile rehberi
```

## Geliştirme

Statik site — özel build adımı yok. `index.html`'i tarayıcıda aç, çalışıyor.

## Yayına gönderme

`main` branch'e push → GitHub Actions otomatik deploy → ~2 dakikada `alenikurye.com` güncel.

Detaylı domain/DNS/SEO rehberi için: [`CANLIYA_ALMA.md`](./CANLIYA_ALMA.md)
