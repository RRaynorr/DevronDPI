# Değişiklik günlüğü / Changelog

## 1.1 — 2026-11-26

### Türkçe
**Yenilikler**
- Quad9 yedek DNS profili: Yandex, OpenDNS ve AdGuard yanıt vermezse otomatik analiz Quad9'a (9.9.9.9) geçer.
- Farklı ekran ölçeklerinde düzgün görünüm: laptop ekranı (%125) ile harici 2K ekran (%100) gibi kurulumlarda pencere bozulmuyor; monitörler arası sürüklemede düzen yeni ölçeğe göre yeniden kuruluyor.
- "Başlangıçta çalıştır" açıkken BAĞLAN'a basarken yönetici izni sorulmaz.
- Daha sağlam hata kaydı: yönetici motor işleminin çökmesi `devron-engine.log` dosyasına yazılır; arayüzde beklenmedik hata olursa uyarı şeridi çıkar.

**Düzeltmeler**
- "Bağlı değil" yazısında `ğ` harfinin kuyruğunun kesilmesi.
- %100 ölçekte "Kayıtları kopyala" butonunun metninin kesilmesi.
- Bozuk paket akışında kayıt dosyasının şişmesi; kayıtlar artık arka planda yazılıyor.
- Sürüm numarası iki haneli oldu.

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
