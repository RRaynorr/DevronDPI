# Değişiklik Günlüğü / Changelog

## 1.2 — 2026-11-26

### Türkçe
**Yenilikler**
- **Anycast erişim köprüsü:** Ağınızda `1.1.1.1`, `9.9.9.9`, `208.67.222.222`, `8.8.8.8` veya `94.140.14.14` gibi bilinen sağlayıcı IP adresleri doğrudan engelliyse bağlantı, aynı sağlayıcıya ait sertifika doğrulamalı alternatif Anycast IP adresine yönlendirilir. Böylece hem bu siteler hem de tarayıcı içi şifreli DNS (DoH) çalışmaya devam eder.
- **Özel adres tanılama ve akış kontrolü:** Bildirim alanı menüsündeki **Bağlantıyı tanıla** penceresinden artık istediğiniz bir alan adını veya IP adresini tek başına test edebilirsiniz. Tanılama, TLS bağlantısı kurulduktan hemen sonra veri akışını donduran derin DPI engellerini de tespit eder.
- **Güçlendirilmiş paket motoru:** Çoklu TLS bölme ve TCP MD5 kullanan yeni yedek yöntem, her bağlantıda rastgele üretilen sahte `ClientHello` paketleri, `TTL=255` ağ donanımları için Auto-TTL desteği, büyük yanıtlar için doğrulanan `TCP 53` DNS yedeği ve tüm Discord ses portlarını kapsayan genişletilmiş ses düzeltmesi eklendi.
- **Küresel kamu ve akademik alan adı muafiyeti:** `.gov`, `.edu`, `.mil`, `.int`, `.europa.eu` ve ülke bazlı kamu/üniversite uzantılarının (`.gov.tr`, `.edu.tr`, `.gov.uk`, `.ac.uk`, `.gouv.fr`, `.gob.es` vb.) paketleri bölünmeden doğrudan geçirilir.
- **Daha eksiksiz kayıtlar ve sadeleştirilen arayüz metinleri:** **Kayıtları kopyala** çıktısına etkin yöntem özeti, canlı paket sayaçları ve varsa `devron-engine.log` dosyasının son satırları eklendi; Bilgi ve Gizlilik ekranı ile bildirim metinleri yeniden düzenlendi.
- **LGPLv3 harici sürücü desteği:** Kendi uyumlu 64-bit `WinDivert.dll` ve `WinDivert64.sys` sürücüsünü kullanmak isteyenler için yönetici korumalı `C:\Program Files\DevronDPI\WinDivert\` klasörü desteği eklendi.

**Düzeltmeler**
- İlk DNS sunucusu sahte veya erişilemeyen bir IP adresi döndürdüğünde analizin yedek DNS yöntemlerine (`OpenDNS`, `AdGuard`, `Quad9`) geçmeden erken durması düzeltildi; sahte yerel DNS yanıtları artık IP engeli yerine DNS müdahalesi olarak algılanıyor.
- Bilgisayar uykudan uyandığında veya kablosuz ağlar arasında geçiş yapılırken internet birkaç saniye gecikirse korumanın kendi kendini kalıcı olarak kapatması giderildi.
- Bağlantı testlerinin yalnızca `TLS 1.2` yerine işletim sisteminin güncel `TLS 1.3 / 1.2` ayarını kullanması sağlandı.
- Kayıtlar ekranındaki üst filtre sekmelerinde (*Tümü / Uyarılar / Hatalar / Ayrıntılar*) iki seçeneğin aynı anda seçili kalması, kısayol atama penceresindeki değer kutusu (ve kullanımda olan kısayol uyarısı) ile bildirim alanı menü genişliği düzeltildi.
- Otomatik güncelleme ve başlangıç kontrollerinde antivirüs yazılımlarının yanlış alarm vermesine yol açabilen yardımcı komut satırı çağrıları kaldırıldı.

### English
**What's new**
- **Anycast access bridge:** when well-known provider IPs such as `1.1.1.1`, `9.9.9.9`, `208.67.222.222`, `8.8.8.8` or `94.140.14.14` are directly blocked on your network, traffic is routed to a certificate-verified alternative Anycast IP of the same provider so both their sites and browser DoH keep working.
- **Single-address diagnostics and stream check:** **Diagnose connection** in the notification area menu now lets you test any specific domain or IP address, and detects deep-DPI blocks that freeze data transfer right after TLS connection setup.
- **Stronger packet engine:** added a multi-split + TCP MD5 fallback method, per-connection randomized fake `ClientHello` packets, Auto-TTL support for `TTL=255` network gear, verified `TCP 53` DNS fallback for large responses, and broader port coverage for Discord voice.
- **Global public & academic domain exemption:** government and university domains worldwide (`.gov`, `.edu`, `.mil`, `.int`, `.europa.eu`, `.gov.tr`, `.edu.tr`, `.gov.uk`, `.ac.uk`, `.gouv.fr`, `.gob.es`, etc.) are passed through without splitting packets.
- **More complete logs and clearer UI copy:** **Copy logs** now includes the active method summary, live packet counters and recent lines from `devron-engine.log`; rewrote the Info & Privacy screen and notification texts in clearer language.
- **LGPLv3 external driver override:** added support for placing a custom compatible 64-bit `WinDivert.dll` and `WinDivert64.sys` pair in the admin-protected `C:\Program Files\DevronDPI\WinDivert\` folder.

**Fixes**
- Fixed automatic analysis stopping early before trying `OpenDNS`, `AdGuard` and `Quad9` when the first DNS server returned an unreachable address; bogus local DNS answers are now reported as DNS tampering rather than an IP block.
- Fixed protection staying off after waking from sleep or switching Wi-Fi when the adapter takes a few extra seconds to come online.
- Connection probes now negotiate the OS default `TLS 1.3 / 1.2` instead of forcing `TLS 1.2`.
- Fixed the filter tabs on the Logs screen (*All / Warnings / Errors / Details*), the shortcut preview box (plus in-use conflict warning) in the hotkey dialog and notification area menu width in English.
- Removed background helper command calls during updates and startup checks that could trigger heuristic antivirus false positives.

## 1.1 — 2026-11-26

### Türkçe
**Yenilikler**
- Quad9 yedek DNS yöntemi: Yandex, OpenDNS ve AdGuard yanıt vermezse otomatik analiz Quad9 (`9.9.9.9`) sunucusuna geçer.
- Farklı ekran ölçeklerinde düzgün görünüm: dizüstü bilgisayar ekranı (%125) ile harici 2K ekran (%100) gibi kurulumlarda pencere bozulmuyor; monitörler arası sürüklemede düzen yeni ölçeğe göre yeniden kuruluyor.
- "Başlangıçta çalıştır" açıkken **BAĞLAN** düğmesine basıldığında yönetici izni sorulmaz.
- Daha sağlam hata kaydı: yönetici motor işleminin çökmesi `devron-engine.log` dosyasına yazılır; arayüzde beklenmedik hata olursa uyarı şeridi çıkar.

**Düzeltmeler**
- "Bağlı değil" yazısında `ğ` harfinin kuyruğunun kesilmesi giderildi.
- %100 ölçekte "Kayıtları kopyala" düğmesindeki metnin kesilmesi giderildi.
- Bozuk paket akışında kayıt dosyasının şişmesi önlendi; kayıtlar artık arka planda yazılıyor.
- Sürüm numarası iki haneli yapıldı.

### English
**What's new**
- Quad9 fallback DNS profile: if Yandex, OpenDNS and AdGuard do not answer, the automatic analysis moves on to Quad9 (9.9.9.9).
- Correct layout on different display scales: the window no longer breaks on setups such as a 125% laptop panel next to a 100% 2K monitor; dragging it between monitors rebuilds the layout for the new scale.
- With "Run at startup" on, pressing CONNECT no longer asks for administrator permission.
- More robust error logging: a crash of the elevated engine process is written to `devron-engine.log`; an unexpected error in the window shows a warning banner.

**Fixes**
- The tail of the `ğ` in "Bağlı değil" was cut off.
- The "Copy logs" button caption was cut off at 100% scale.
- A faulty packet stream could flood the log file; logs are now written in the background.
- The version number now has two parts.

## 1.0 — 2026-11-26

İlk yayın. / Initial release.
