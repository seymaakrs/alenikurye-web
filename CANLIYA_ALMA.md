# 🚀 Aleni Kurye — Canlıya Alma (Turhost Domain + GitHub Pages)

Domain: **alenikurye.com** (Turhost)
Hosting: **GitHub Pages** (ücretsiz, HTTPS otomatik, sınırsız trafik)

> Not: Netlify ücretsiz limiti dolduğu için artık GitHub Pages kullanıyoruz.
> `main` branch'e her push, `.github/workflows/deploy.yml` ile otomatik canlıya çıkar.
> DNS ayarları için aşağıdaki "GitHub Pages DNS" bölümüne bak.

## GitHub Pages DNS (Turhost paneli)

Turhost DNS yönetiminde A kayıtları:
```
A  @  185.199.108.153
A  @  185.199.109.153
A  @  185.199.110.153
A  @  185.199.111.153
CNAME  www  seymaakrs.github.io
```
GitHub repo → Settings → Pages → Custom domain: `alenikurye.com` → "Enforce HTTPS" aç.

---

## Eski Netlify rehberi (referans)



## ADIM 1 — Netlify Hesabı Aç (2 dakika)

1. https://app.netlify.com/signup adresine git
2. "GitHub ile giriş yap" veya "Email ile kayıt ol" — hangisi kolay geliyorsa
3. Email doğrulamasını yap

---

## ADIM 2 — Siteyi Netlify'a Yükle (30 saniye)

### En kolay yol: Drag & Drop
1. https://app.netlify.com/drop adresine git
2. Bilgisayarından **`alenikurye-web`** klasörünü (tüm içeriğiyle) siteye sürükle-bırak
3. Netlify anında deploy eder, sana rastgele bir URL verir:
   `https://rastgele-isim-123.netlify.app`
4. Bu URL'i aç — site canlıda ✅

### Alternatif: Site Settings'ten isim değiştir
- Netlify paneli → Site settings → Change site name → `alenikurye` yaz
- Yeni URL: `https://alenikurye.netlify.app` (geçici, asıl domain bağlanınca gerek kalmayacak)

---

## ADIM 3 — alenikurye.com Domain'ini Netlify'a Bağla

### Netlify Tarafı
1. Site paneli → **Domain settings** → **Add custom domain**
2. `alenikurye.com` yaz → Verify → Yes, add domain
3. `www.alenikurye.com` de ekle (redirect olacak)
4. Netlify sana 2 şey gösterir:
   - **DNS records** (A ve CNAME değerleri)
   - **Nameservers** (eğer DNS'i Netlify'da yönetmek istersen)

### YÖNTEM A — Sadece DNS Kaydı (KOLAY, önerilen)

Turhost'ta domaini aldın → https://panel.turhost.com/domain/manage/567473

1. Panel → **DNS Yönetimi** / **DNS Records** sekmesine gir
2. Mevcut kayıtları sil (varsa, A ve CNAME hariç dikkat et)
3. Şu kayıtları ekle:

```
Tür    | İsim | Değer                      | TTL
-------|------|----------------------------|-----
A      | @    | 75.2.60.5                  | 3600
CNAME  | www  | [site-isminiz].netlify.app | 3600
```

> Not: Netlify sana kendi IP'sini verecek, yukarıdaki IP Netlify'ın load balancer'ı. Panelde Netlify'ın gösterdiği IP ile değiştir (genelde `75.2.60.5` veya `99.83.190.102` olur).

4. Kaydet → **24 saat içinde** (genelde 15 dakika-2 saat) domain açılır
5. Netlify otomatik **Let's Encrypt SSL** kuracak → `https://alenikurye.com` çalışır

### YÖNTEM B — Netlify DNS (tüm yönetim Netlify'da)

1. Netlify → Domain settings → "Set up Netlify DNS" tıkla
2. Netlify sana 4 nameserver verir, örnek:
   ```
   dns1.p01.nsone.net
   dns2.p01.nsone.net
   dns3.p01.nsone.net
   dns4.p01.nsone.net
   ```
3. Turhost panelinden → **Nameserver Değişikliği** (Name Servers)
4. Mevcut nameserverları sil, Netlify'ınkileri yaz
5. Kaydet → 2-24 saat içinde aktif

> Hangisini seçmeli? Başlangıç için **Yöntem A daha hızlı**. İleride email (alenikurye.com'a mail kurmak) istersen yöntem B daha esnek.

---

## ADIM 4 — SSL Sertifikası (Otomatik)

Domain bağlandıktan 1-24 saat sonra:
- Netlify → Domain settings → HTTPS → **Verify DNS configuration** → tıkla
- "Provision certificate" → Let's Encrypt SSL otomatik kurulur
- Artık `https://alenikurye.com` yeşil kilit ile açılır

---

## ADIM 5 — Google Search Console (SEO'ya başla)

1. https://search.google.com/search-console adresine git
2. **"URL prefix"** seçeneği → `https://alenikurye.com` yaz
3. Doğrulama: **HTML tag** yöntemi seç → kodu kopyala
4. Netlify → Site settings → Build & deploy → Post processing → **Snippet injection**
   - Ya da `index.html`'in `<head>`'ine ekleyip tekrar yükle
5. Verify → ✅
6. Sol menüden **Sitemaps** → `sitemap.xml` yaz → Submit
7. 2-5 gün içinde Google sayfayı indekslemeye başlar

---

## ADIM 6 — Google Business Profile (YEREL ARAMA İÇİN ŞART)

"sapanca kurye" araması yapıldığında harita ve üstte çıkmak için:

1. https://business.google.com
2. "Businessimi yönet" → **Create**
3. İşletme adı: **Aleni Kurye**
4. Kategori: **Kurye hizmeti** (Courier service)
5. Servis bölgesi: Sapanca, Maşukiye, Kartepe, Sakarya, Adapazarı ekle
6. Telefon: **0552 716 29 68**
7. Web: `https://alenikurye.com`
8. Saatler: 7/24 açık
9. Açıklama: "Sapanca, Maşukiye ve Kartepe bölgesinde 7/24 eve servis kurye. Tekel, yemek, market, eczane, mangal ve özel premium hizmetler. 5 dakikaya kapınızda."
10. Doğrulama: Kartpostal (5-14 gün) / telefon / email ile gelir
11. Onaylanınca **fotoğraflar yükle** (motor, ekip, logo) → arama sonuçlarında çok etkili

---

## ADIM 7 — Ek Kayıtlar (opsiyonel ama faydalı)

- **Bing Webmaster:** https://www.bing.com/webmasters → site + sitemap ekle
- **Yandex Webmaster:** https://webmaster.yandex.com (Türkiye'de kullanan kesim var)
- **Sosyal medya:** Instagram + TikTok hesabı aç (@alenikurye), siteye linkle

---

## 🟢 Kontrol Listesi

- [ ] Netlify hesabı açıldı
- [ ] `alenikurye-web` klasörü yüklendi
- [ ] Geçici `.netlify.app` URL'i çalışıyor
- [ ] Turhost DNS kayıtları girildi
- [ ] `https://alenikurye.com` açılıyor
- [ ] SSL sertifikası aktif (yeşil kilit)
- [ ] Google Search Console doğrulandı + sitemap gönderildi
- [ ] Google Business Profile oluşturuldu
- [ ] WhatsApp butonları test edildi (telefondan)
- [ ] Mobil test edildi

---

## 🆘 Takıldığın Yerde

Netlify bir şey sorarsa ya da Turhost paneli farklı görünüyorsa:
- Netlify ekranının screenshot'ını at
- Turhost DNS ekranının screenshot'ını at
- Birlikte çözelim
