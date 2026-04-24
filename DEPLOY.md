# Aleni Kurye — Canlıya Alma Rehberi

## 1. Domain: alenikurye.com
- **Nereden:** GoDaddy, Natro, İsimTescil veya Cloudflare Registrar (en ucuz).
- **Öneri:** Cloudflare Registrar (~10-12 USD/yıl, Türkçe kart destekli).

## 2. Hosting (ÜCRETSİZ seçenekler)

### Seçenek A — Netlify (en kolay, önerilen)
1. https://app.netlify.com → **Add new site → Deploy manually**
2. Tüm `alenikurye-web/` klasörünü sürükle-bırak.
3. Rastgele URL verecek (örn. `aleni-kurye.netlify.app`) — site anında canlı.
4. **Domain bağlama:** Site settings → Domain management → Add custom domain → `alenikurye.com`
5. Netlify'ın verdiği DNS sunucularını domain sağlayıcına gir. Otomatik HTTPS.

### Seçenek B — Vercel
1. https://vercel.com → Import → klasörü yükle → Deploy.

### Seçenek C — Cloudflare Pages
1. https://pages.cloudflare.com → Upload assets → klasörü bırak.

## 3. Canlıya Alırken Kontrol Listesi
- [ ] Domain alındı
- [ ] Hosting'e yüklendi
- [ ] DNS yönlendirildi (A/CNAME kaydı)
- [ ] HTTPS aktif (otomatik)
- [ ] `https://alenikurye.com` açılıyor
- [ ] WhatsApp butonları çalışıyor (test et)
- [ ] Telefon numarası doğru: 0552 716 29 68
- [ ] Mobil test edildi

## 4. Google'a Bildirim (SEO)
1. **Google Search Console:** https://search.google.com/search-console
   - Property ekle → `https://alenikurye.com`
   - Doğrulama: DNS veya HTML etiket
   - Sitemap gönder: `https://alenikurye.com/sitemap.xml`
2. **Google Business Profile:** https://business.google.com
   - İşletme oluştur → "Aleni Kurye" → Sakarya/Sapanca bölge → hizmetler
   - Bu adım yerel aramada ("sapanca kurye", "sapanca tekel servis") çıkmak için kritik.
3. **Bing Webmaster:** https://www.bing.com/webmasters

## 5. SEO Anahtar Kelimeler (hedeflenen)
- sapanca kurye
- sakarya eve servis
- sapanca bungalov kurye
- sapanca 7/24 tekel servis
- sapanca market servisi
- sakarya mangal malzeme servisi

## Dosya Yapısı
```
alenikurye-web/
├── index.html          ← ana sayfa (SEO meta, structured data)
├── robots.txt          ← arama motorları için
├── sitemap.xml         ← site haritası
├── manifest.webmanifest← PWA
├── favicon.svg         ← sekme ikonu
├── netlify.toml        ← netlify config + güvenlik header'ları
└── DEPLOY.md           ← bu dosya
```
