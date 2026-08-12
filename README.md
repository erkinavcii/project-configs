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

İleride başka projeler eklenirse aynı desen: `<ProjeAdı>/` altında o
projenin okuduğu dosyalar.
