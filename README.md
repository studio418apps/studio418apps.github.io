# studio418apps.github.io

Studio 418 web sitesi: stüdyo ana sayfası ve uygulamaların gizlilik/destek sayfaları. GitHub Pages ile yayınlanır.

## Yapı

```
index.html                 Stüdyo ana sayfası
assets/style.css           Ortak stil (açık/koyu tema)
assets/teapot.svg          Logo (renk CSS'teki --mark değişkeninden gelir)
assets/favicon.svg         Sadeleştirilmiş favicon (açık/koyu tema)
bookfrog/index.html        BookFrog tanıtım sayfası
bookfrog/privacy.html      Gizlilik politikası (TR + EN) → App Store "Privacy Policy URL"
bookfrog/support.html      Destek + SSS (TR + EN)      → App Store "Support URL"
.nojekyll                  .well-known klasörünün yayınlanması için gerekli
```

## Yayınlamadan önce doldurulacaklar

`bookfrog/privacy.html` içinde:
- `[AD SOYAD]` / `[FULL NAME]` — veri sorumlusunun adı
- `[GG.AA.YYYY]` / `[DD.MM.YYYY]` — yürürlük ve güncelleme tarihleri
- `[BÖLGE]` / `[REGION]` — Supabase projesinin sunucu bölgesi
- `[30]` — hesap silindikten sonra verilerin silinme süresi (uygulamadaki gerçek davranışla aynı olmalı)

E-posta adresi farklıysa tüm dosyalarda `studio418apps@gmail.com` ifadesini değiştir.

Gizlilik metni bir başlangıç taslağıdır, hukuki danışmanlık yerine geçmez. Uygulamanın gerçek veri akışı netleşince (özellikle hata kaydı aracı, Supabase bölgesi ve silme süresi) güncelle ve lansmandan önce bir hukukçuya göz attır.

## Universal Links (Faz 1'de eklenecek)

Ebeveyn davet linkleri için `.well-known/apple-app-site-association` dosyası eklenecek. Team ID ve bundle ID belli olunca oluşturulacak, örnek içerik:

```json
{
  "applinks": {
    "details": [
      { "appIDs": ["TEAMID.com.studio418.bookfrog"], "components": [{ "/": "/bookfrog/invite/*" }] }
    ]
  }
}
```

Dosya uzantısız olmalı. `.nojekyll` sayesinde GitHub Pages `.well-known` klasörünü yayınlar.
