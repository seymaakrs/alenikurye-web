# 🚀 Aleni Kurye — Canlıya Alma (Turhost Domain + GitHub Pages)

Domain: **alenikurye.com** (Turhost)
Hosting: **GitHub Pages** (ücretsiz, HTTPS otomatik, sınırsız trafik)
Telefon: **0552 716 19 68**

> `main` branch'e her push, `.github/workflows/deploy.yml` ile otomatik canlıya çıkar.

---

## 1. DNS — Turhost paneli

Turhost DNS yönetiminde A kayıtları:

```
A      @    185.199.108.153
A      @    185.199.109.153
A      @    185.199.110.153
A      @    185.199.111.153
CNAME  www  seymaakrs.github.io
```

Doğrulama: terminalde `getent hosts alenikurye.com` çalıştırınca yukarıdaki 4 IP'den birini dönmeli.

## 2. GitHub Pages ayarı

GitHub repo → **Settings** → **Pages**:
- Source: **GitHub Actions**
- Custom domain: `alenikurye.com`
- ✅ **Enforce HTTPS** açık olmalı

## 3. Sertifika

Domain bağlandıktan ~10-30 dakika sonra GitHub otomatik Let's Encrypt SSL alır. Sayfa adres çubuğunda 🔒 yeşil kilit görünür.

---

## 4. Google Search Console (SEO)

1. https://search.google.com/search-console
2. **URL prefix** → `https://alenikurye.com`
3. Doğrulama: **HTML tag** → çıkan `<meta>` etiketini kopyala → `index.html` `<head>` içine yapıştır → commit + push (otomatik deploy olur) → Verify
4. Sol menü → **Sitemaps** → `sitemap.xml` yaz → Submit
5. 2-5 gün içinde Google indekslemeye başlar

## 5. Google Business Profile (yerel arama için kritik)

1. https://business.google.com → **Create**
2. İşletme adı: **Aleni Kurye**
3. Kategori: **Kurye hizmeti** (Courier service)
4. Servis bölgesi: Sapanca, Maşukiye, Kartepe, Sakarya, Adapazarı
5. Telefon: **0552 716 19 68**
6. Web: `https://alenikurye.com`
7. Saatler: 7/24 açık
8. Açıklama: *"Sapanca, Maşukiye ve Kartepe bölgesinde 7/24 eve servis kurye. Tekel, yemek, market, eczane, mangal ve özel premium hizmetler. 5 dakikaya kapınızda."*
9. Doğrulama: kartpostal (5-14 gün) / telefon / email
10. Onaylanınca fotoğraf yükle (motor, ekip, logo) → arama sonuçlarında çok etkili

## 6. Ek kayıtlar (opsiyonel)

- **Bing Webmaster:** https://www.bing.com/webmasters
- **Yandex Webmaster:** https://webmaster.yandex.com
- **Sosyal medya:** Instagram + TikTok (@alenikurye), siteye linkle

---

## ✅ Kontrol listesi

- [ ] Turhost DNS kayıtları girildi (4 A + 1 CNAME)
- [ ] GitHub Settings → Pages → Custom domain set, HTTPS açık
- [ ] `https://alenikurye.com` açılıyor (yeşil kilit)
- [ ] WhatsApp butonu test edildi (telefondan tıklayınca 0552 716 19 68 sohbeti açılıyor mu?)
- [ ] Telefon linki test edildi
- [ ] Mobilde test edildi
- [ ] Google Search Console doğrulandı + sitemap gönderildi
- [ ] Google Business Profile oluşturuldu

---

## 🆘 Sorun çıkarsa

- DNS ekranının screenshot'ı + tarayıcı hata ekranı → birlikte çözeriz
- GitHub Actions sekmesinde son deploy yeşil mi? Kırmızıysa log'a bak.
