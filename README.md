# project-configs

Birden fazla projenin **statik, uzaktan-güncellenebilir config dosyalarını**
tuttuğu ortak repo. Kaynak kod burada değil — her proje kendi (genelde
private) reposunda yaşıyor, sadece "kendini onaran" mekanizmalarının okuduğu
küçük yapılandırma dosyaları burada, proje adına göre klasörlenmiş.

Neden ayrı repo: kaynak kodu private tutup yalnızca bu dosyaları public
yapabilmek için. Bu repo hiçbir kullanıcı verisi, kimlik bilgisi ya da
telif hakkıyla korunan içerik taşımaz — yalnızca CSS seçici / uç nokta gibi
yapılandırma metinleri.

## Klasörler

- `Eksim/selectors.json` — [Eksim](https://github.com/erkinavcii/Eksim)
  (gayriresmî Ekşi Sözlük istemcisi) için CSS seçici + uç nokta + `baseUrl`
  config'i. Uygulama bunu `raw.githubusercontent.com` üzerinden günde bir
  kez kontrol eder; site HTML'i değiştiğinde ya da erişim adresi
  taşındığında tek bir commit ile kurulu uygulamalar düzelir, yeni sürüm
  yayınlamaya gerek kalmaz.

- `FamilyPulse/` — [FamilyPulse](https://github.com/erkinavcii/FamilyPulse)
  (aile güvenlik/konum takibi uygulaması) için Google Play'in **yayın
  öncesi zorunlu tuttuğu, herkese açık URL'den erişilebilir olması gereken**
  yasal metinler — kaynak kod (private repo) içinde barındırılamayacakları
  için buradalar. Play Console'a Store listing / Data Safety alanlarına
  girilecek gizlilik politikası ve hesap silme URL'leri buradan verilecek.
  Türkçe + İngilizce, karşılıklı dil geçiş linkleriyle:
  - `privacy.html` / `privacy-en.html` — Gizlilik ve Veri Kullanımı
  - `terms-of-service.html` / `terms-of-service-en.html` — Kullanım Şartları
  - `delete-account.html` / `delete-account-en.html` — Hesap ve Veri Silme Talebi

  ⚠️ **Taslak.** Her sayfada bir TASLAK bandı ve köşeli parantezli
  ([AD SOYAD / ŞİRKET UNVANI], [BURAYA_DESTEK_EPOSTASI] vb.) doldurulmamış
  alanlar var; hukuki inceleme yapılmadan gerçek yayın URL'si olarak
  kullanılmamalı. Kaynak, güncellenirken FamilyPulse reposundaki `docs/`
  klasörüdür — değişiklik oradan yapılıp buraya yeniden kopyalanmalı.

İleride başka projeler eklenirse aynı desen: `<ProjeAdı>/` altında o
projenin okuduğu dosyalar.
