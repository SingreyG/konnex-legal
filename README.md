# konnex-legal

Konnex mobil oyununun yasal metinleri (Gizlilik Politikası, Kullanım Şartları) ve destek sayfası.

## Yayın

GitHub Pages aracılığıyla yayımlanır. Aşağıdaki adımlar:

1. GitHub'da yeni **public** repo aç: `konnex-legal`
2. Bu klasörün içeriğini repo'ya push et:
   ```bash
   cd konnex-legal
   git init
   git add .
   git commit -m "init: privacy + terms + landing"
   git branch -M main
   git remote add origin https://github.com/<github-username>/konnex-legal.git
   git push -u origin main
   ```
3. GitHub repo ayarları → **Settings → Pages** → Source: `Deploy from a branch`, Branch: `main` / `(root)` → Save
4. ~30 saniye sonra şu adresler aktif olur:
   - `https://<github-username>.github.io/konnex-legal/`
   - `https://<github-username>.github.io/konnex-legal/privacy.html`
   - `https://<github-username>.github.io/konnex-legal/terms.html`
5. Konnex'in `app.json` → `extra.legalUrls` içindeki `singrey` placeholder'ını gerçek GitHub kullanıcı adınla değiştir.

## Dosya yapısı

```
konnex-legal/
├── index.html            # Landing — privacy/terms linkleri + iletişim
├── privacy.html          # Gizlilik Politikası (TR + EN)
├── terms.html            # Kullanım Şartları (TR + EN)
├── README.md             # Bu dosya
└── assets/
    └── style.css         # paper bg + JetBrains Mono — Konnex temasıyla uyumlu
```

## Güncelleme

İçeriği değiştirdiğinde commit + push yeterli; GitHub Pages dakikalar içinde yeniden yayımlar.

## Kullanım yerleri

- **App Store Connect** → Privacy Policy URL alanına: `https://<github-username>.github.io/konnex-legal/privacy.html`
- **Google Play Console** → Privacy Policy alanına: aynı URL
- **App içinde** (Settings ekranı) → Gizlilik / Kullanım Şartları satırları doğrudan bu URL'leri açar.
