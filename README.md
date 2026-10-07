# Seslerin İzinde — web sitesi

Görme engelli bir çiftin içerik markası **Seslerin İzinde**'nin tanıtım sitesi.
Adres: https://seslerinizinde.com ve www.seslerinizinde.com (Cloudflare Registrar, 7 Ekim 2026, 1 yıl, 10,46 USD, otomatik yenileme kapalı).

Durum: taslak. İçerik ve görünüm sahiplerinden ayrıca gelecek. Yayın, push ve alan adı bağlama yalnız açık onayla. Forali sitesine ve ayarlarına dokunulmaz.

## Yapı

- `docs/index.html` — Türkçe ana sayfa; `docs/en/index.html` — İngilizce. `hreflang` ile birbirine bağlı.
- `docs/site.css`, `docs/404.html` (iki dilli), `docs/favicon.svg`, `docs/CNAME` (seslerinizinde.com), `docs/.nojekyll`.
- Derleme yok: düz HTML/CSS. Çerez, analitik, dış yazı tipi, dış betik ve gömülü video yok.

## İçerik kuralları

- Doğrulanmış bağlantılar: YouTube @seslerinizinde, TikTok @seslerin.izinde (7 Ekim'de sayfa kimliği eşleşti).
- Instagram: doğrulanamadı (giriş duvarı); sahipleri onaylayınca eklenir.
- X (Twitter) yok. E-posta adresi şimdilik yazılmaz.
- İletişim formu: statik sitede üçüncü taraf form hizmeti gerekir; hizmet seçilmeden eklenmez.
- Takipçi sayısı, şirket, ödül gibi doğrulanmamış veya izin verilmemiş bilgi yazılmaz.
- Tek `h1`, sıralı başlıklar, doğru `lang`, "İçeriğe atla", görünür odak. "Erişilebilirlik doğrulandı" yalnız gerçek VoiceOver turundan sonra.

## Yayın: GitHub Pages (ayrı depo)

Bu depo kendi özel alan adını taşır; bu yüzden Forali'nin kullanıcı sitesine bağlı alan adından etkilenmez.

1. GitHub'da `seslerinizinde` deposu oluşturulur ve gönderilir (onayla). Ücretsiz hesapta Pages için depo herkese açık olmalı.
2. Depo → Settings → Pages → Source: Deploy from a branch, `main`, klasör `/docs`.
3. Alan adı doğrulaması: GitHub profil → Settings → Pages → Add a domain → `seslerinizinde.com`; verilen TXT kaydı (`_github-pages-challenge-recepgur07-bot`) Cloudflare'a birebir eklenir, Verify.
4. Cloudflare DNS (hepsi "DNS only", gri bulut):
   - A `@` 185.199.108.153 / 185.199.109.153 / 185.199.110.153 / 185.199.111.153
   - AAAA `@` 2606:50c0:8000::153 / 2606:50c0:8001::153 / 2606:50c0:8002::153 / 2606:50c0:8003::153
   - CNAME `www` → `recepgur07-bot.github.io`
5. Depo → Settings → Pages → Custom domain `seslerinizinde.com` (CNAME dosyasıyla aynı), DNS check başarılı → sertifika gelince "Enforce HTTPS".
6. Kontrol: `https://seslerinizinde.com`, `https://www.seslerinizinde.com` (apex'e yönlenmeli), `/en/`.
