# Aleni Kurye — Yarın Devam Listesi

## ✅ Tamamlananlar
- Full site (`index.html`) — kırmızı/bordo palette, emoji yok, SVG ikonlar
- Fontlar: PT Sans (body) + Bangers (display, ticari serbest)
- Hizmet slider (5 slayt, otomatik dönüyor)
- Hakkımızda bölümü (samimi ton)
- Lokasyonlar: Sapanca, Maşukiye, Kartepe, Kırkpınar, Kurtköy, Mahmudiye, Şükriye, Sakarya, Adapazarı
- Premium/özel hizmetler bloğu (evrak, nişan, düğün, parti)
- SSS (7 soru, accordion)
- SEO: LocalBusiness + FAQPage schema, geo meta, keywords, sitemap, robots
- favicon.svg, manifest.webmanifest, netlify.toml

## 🟡 Yarın Senden Bekleyenler
1. **Domain:** alenikurye.com — Cloudflare Registrar önerisi (~$10/yıl)
2. **Logo dosyası** — tiger logolu PNG/SVG göndereceksin
3. **Stok görseller** — Pexels/Unsplash'tan aranacaklar:
   - Sapanca göl manzarası (hero arka planı için)
   - Kurye motoru / teslimat
   - Bungalov / villa dış çekim
   - Servis görselleri (tekel, yemek, mangal, çiçek)
   - → `images/` klasörüne bırak

## 🟡 Yarın Bende Bekleyen İşler
1. Logo geldiğinde: nav + favicon + footer'a entegre
2. Görseller geldiğinde: hero'ya parallax arka plan, slider'a fotoğraf, hakkımızda görsel kutusu
3. Domain alındığında:
   - Netlify'a deploy (drag & drop)
   - DNS ayarları (A/CNAME)
   - SSL aktivasyonu
   - Google Search Console → sitemap gönderim
   - Google Business Profile → Sapanca yerel arama kaydı
   - Bing Webmaster kaydı
4. Bouncy ticari lisansı alınırsa → fontu geri tak (tek satır değişiklik)

## 📁 Dosya Yapısı
```
alenikurye-web/
├── index.html              ← ana sayfa (tam SEO + structured data)
├── robots.txt
├── sitemap.xml
├── manifest.webmanifest
├── favicon.svg
├── netlify.toml            ← deploy config + güvenlik header'ları
├── DEPLOY.md               ← deploy rehberi
├── YARIN_DEVAM.md          ← bu dosya
├── fonts/
│   ├── fonts.css
│   ├── pt-sans/            ← ticari serbest
│   └── bouncy/             ← PERSONAL USE — lisans alınmalı
│       └── READ_BEFORE_ANY_USE.txt
└── images/
    └── README.txt          ← eklenecek görsellerin listesi
```

## 🚀 Dev Server (yarın tekrar çalıştırmak için)
Preview panelinden `alenikurye` sunucusunu başlat — http://localhost:3000

## 📞 Telefon
0552 716 29 68 (tüm butonlarda ve schema'da bu numara)
