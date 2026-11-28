# Changelog / Değişiklik Günlüğü

## 1.4 — 2026-11-28

### English
**What's new**
- **In-app Settings with sliding sub-pages & streamlined tray menu:** Moved all preferences, Preferred DNS, Hotkey, Exempt sites, Selected apps, Backup/Restore and Connection X-Ray into a single-surface in-app **Settings** view, leaving a clean 5-item notification area menu. Added inline update checking with a `v1.4` badge and a **What's new** modal.
- **Encrypted DNS (DoH) & Cloudflare DNS:** Added **Cloudflare (1.1.1.1)** to Preferred DNS and an optional **Encrypted DNS (DoH)** toggle (RFC 8484 direct-IP HTTPS, Keep-Alive pool, TTL cache, automatic provider failover and LAN/Captive Portal exemption).
- **Visual Selected Apps picker & 8-site Quick Test:** Pick running apps with icons and live search under **Settings → Selected apps**, and run a parallel 4-stage **8-site Quick Test** inside Connection X-Ray with one-click copy.
- **Driverless System Proxy Mode (Windows ARM64 & non-admin PCs):** Added an optional local loopback proxy mode requiring no WinDivert driver or administrator rights (enabled automatically on Windows ARM64).
- **New languages (RU, FA, ES) & live blocked counter:** Added **Russian (RU)**, **Persian (FA, RTL)** and **Spanish (ES)** alongside existing English and Turkish (5 languages total, English default), live blocked-trackers counter on Home, and status-badged taskbar/tray icons.
- **Standalone Android release (`DevronDPI.apk`, rootless Android 10+):** Shipped a signed Material 3 Android app with local on-device `VpnService` + DPI proxy, IPv6 `AAAA` leak prevention on 4G/5G, visual per-app picker, cached Preferred DNS, Tracker & ad shield, parallel 4-stage X-Ray & 8-site benchmark, Quick Settings tile, auto-start on boot, 5 languages, Dark/Light themes and shared RSA-2048 signed rules.

**Fixes**
- Fixed Windows 11 double drop-shadow halo, Light/Dark theme transition frame skips and card edge bleed, warning banner clipping over the power orb, and live settings hot-reload without false drop notifications or timer resets.
- Fixed Android 14/15 foreground service startup edge cases, fragmented TLS ClientHello reassembly, socket relay half-close handling, Turkish-locale hostname normalization, and log viewer clear/copy behavior.

### Türkçe
**Yenilikler**
- **Uygulama içi Ayarlar, kayan alt sayfalar ve sadeleştirilmiş bildirim alanı menüsü:** Tüm ayarlar, Tercih Edilen DNS, Kısayol, Muafiyet Listesi, Seçili Uygulamalar, Yedekleme ve Bağlantı Röntgeni tek yüzeyli **Ayarlar** ekranına taşındı; bildirim alanı menüsü 5 satırla sadeleştirildi. Satır içi güncelleme kontrolü (`v1.4` rozetli) ve **Yenilikler** penceresi eklendi.
- **Şifreli DNS (DoH) ve Cloudflare DNS:** Tercih Edilen DNS listesine **Cloudflare (1.1.1.1)** ve isteğe bağlı **Şifreli DNS (DoH)** anahtarı eklendi (doğrudan IP üzerinden RFC 8484 HTTPS, Keep-Alive havuzu, TTL önbelleği, otomatik sağlayıcı yedeklemesi ve yerel ağ/Captive Portal muafiyeti).
- **Görsel Seçili Uygulamalar ve 8 sitelik Hızlı Test:** **Ayarlar → Seçili uygulamalar** ekranında açık uygulamaları simgeleri ve anlık aramayla seçebilir, Bağlantı Röntgeni içinde paralel 4 aşamalı **8 sitelik Hızlı Test** çalıştırıp raporu tek tıkla kopyalayabilirsiniz.
- **Sürücüsüz Sistem Proxy Modu (Windows ARM64 ve yönetici izinsiz PC'ler):** WinDivert sürücüsü ve yönetici izni gerektirmeyen isteğe bağlı Sistem Proxy Modu eklendi (Windows ARM64 cihazlarda otomatik etkinleşir).
- **Yeni diller (RU, FA, ES) ve canlı sayaç:** Mevcut İngilizce ve Türkçenin yanına **Rusça (RU)**, **Farsça (FA, RTL)** ve **İspanyolca (ES)** eklendi (toplam 5 dil, varsayılan İngilizce); ana ekrana canlı engellenen izleyici sayacı ve görev çubuğu/bildirim alanına durum rozetli simgeler eklendi.
- **Bağımsız Android sürümü (`DevronDPI.apk`, root'suz Android 10+):** Cihaz içi yerel `VpnService` + DPI proxy, 4G/5G IPv6 `AAAA` sızıntı engeli, görsel uygulama seçici, önbellekli Tercih Edilen DNS, İzleyici & reklam koruması, paralel 4 aşamalı Röntgen ve 8 sitelik toplu test, Hızlı Ayarlar kutucuğu, açılışta başlatma, 5 dil, Koyu/Açık Material 3 tema ve ortak RSA-2048 imzalı kurallarla imzalı Android sürümü yayınlandı.

**Düzeltmeler**
- Windows 11 çift gölge kenarlığı, Koyu/Açık tema geçişindeki kare atlaması ve kart kenarı taşması, uyarı şeridinin bağlantı düğmesini örtmesi ve ayar değiştirirken yanlış kopma bildirimi/sayaç sıfırlanması giderildi.
- Android 14/15 ön plan servisi başlangıç kenar durumları, parçalı TLS ClientHello birleştirme, soket yarım kapatma, Türkçe dil ayarında büyük `I` alan adı bozulması ve kayıt temizleme/kopyalama sorunları düzeltildi.

## 1.3 — 2026-11-27

### English
**What's new**
- **Visual 4-stage Connection X-Ray & per-site rules:** **Diagnose connection** now shows live timings for `DNS → TCP → TLS SNI → 24 KB Flow`. When a specific site fails to load, DevronDPI tests alternatives in the background and offers **Apply Working Rule** or **Add to Exempt List** only after verifying that all 4 stages succeed.
- **Game & anti-cheat exemptions + Custom exempt list:** Popular game launchers and anti-cheat services (Riot/Vanguard, Steam, Battle.net, EasyAntiCheat, BattlEye, FACEIT, Epic, EA, Ubisoft, Rockstar) are automatically passed through untouched. You can also add your own domains (banking, corporate portals) via **Exempt sites** in the notification area menu.
- **Tracker & ad shield (optional, 0 ms):** Enable **Tracker & ad shield** from the notification area menu to block known advertising, tracking and telemetry domains locally with zero latency — works in browsers even with DoH enabled, without decrypting HTTPS or installing certificates.
- **Digitally signed rule updates (`rules.json`):** Optional RSA-2048 verified updates from GitHub keep exemptions, tracker lists and site rules up to date without needing a new app release, with seamless offline fallback.
- **Redesigned Logs & smoother UI:** Sliding filter tabs (*All / Warn / Error / Details*), 3 live counters (*Protected Flows*, *Blocked Resets*, *DNS & Bridge*), instant search filtering, a cleaner *Details* view, and fluid transitions across views, themes, language, menus and scrolling.
- **Windows integration & stability:** Live Windows Dark/Light theme sync, automatic connection re-check after unlocking Windows, one-click settings backup/restore, USB portable mode (`portable.flag`), connection stability improvements, and clear startup notices on unsupported architectures (ARM64 / 32-bit).

### Türkçe
**Yenilikler**
- **4 aşamalı görsel Engel Röntgeni ve site bazlı kurallar:** **Bağlantıyı tanıla** penceresi artık `DNS → TCP → TLS SNI → 24 KB Akış` aşamalarını canlı sürelerle gösterir. Belirli bir site açılmadığında alternatifleri arka planda dener ve yalnızca tüm aşamalar başarıyla geçildiğinde **Çalışan Kuralı Uygula** veya **Muafiyet Listesine Ekle** seçeneğini sunar.
- **Oyun ve anti-cheat muafiyeti + Özel muafiyet listesi:** Popüler oyun başlatıcıları ve anti-cheat servisleri (Riot/Vanguard, Steam, Battle.net, EasyAntiCheat, BattlEye, FACEIT, Epic, EA, Ubisoft, Rockstar) otomatik olarak doğrudan geçirilir. Bildirim alanı menüsündeki **Muafiyet listesi** ile banka veya kurumsal portallarınızı da ekleyebilirsiniz.
- **İzleyici & reklam koruması (isteğe bağlı, 0 ms):** Bildirim alanı menüsünden açılabilen bu özellik, bilinen reklam, izleme ve telemetri alan adlarını HTTPS şifresini kırmadan ve sertifika kurmadan yerel olarak engeller; tarayıcıda DoH açıkken bile çalışır.
- **Dijital imzalı kural güncellemeleri (`rules.json`):** GitHub üzerinden RSA-2048 imzasıyla doğrulanan hafif güncellemeler; yeni sürüm kurmaya gerek kalmadan muafiyet, izleyici ve site kurallarını güncel tutar, çevrim dışı durumda yerleşik kurallarla kesintisiz çalışır.
- **Yenilenen Kayıtlar ekranı ve akıcı arayüz:** Kayan filtre sekmeleri (*Tümü / Uyarı / Hata / Ayrıntı*), 3 canlı sayaç (*Korunan Akış*, *Önlenen Kesinti*, *DNS & Köprü*), anlık arama, daha sade *Ayrıntı* görünümü ve ekran, tema, dil, menü ile kaydırmada akıcı geçişler eklendi.
- **Windows uyumu ve kararlılık:** Canlı Windows Koyu/Açık tema takibi, kilit ekranından dönüşte otomatik bağlantı kontrolü, tek tıkla ayar yedekleme/geri yükleme, taşınabilir USB kipi (`portable.flag`), bağlantı kararlılığı iyileştirmeleri ve desteklenmeyen sistemlerde (ARM64 / 32-bit) açılış bilgilendirmesi eklendi.

## 1.2 — 2026-11-26

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
- Kayıtlar ekranındaki üst filtre sekmelerinde (*Tümü / Uyarılar / Hatalar / Ayrıntılar*), kısayol atama penceresindeki değer kutusu (ve kullanımda olan kısayol uyarısı) ile bildirim alanı menü genişliği düzeltildi.
- Otomatik güncelleme ve başlangıç kontrollerinde antivirüs yazılımlarının yanlış alarm vermesine yol açabilen yardımcı komut satırı çağrıları kaldırıldı.

## 1.1 — 2026-11-26

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

## 1.0 — 2026-11-26

Initial release. / İlk yayın.
