# Security Policy / Güvenlik Politikası

🇬🇧 English · 🇹🇷 [Türkçe aşağıda](#türkçe)

## English

### Supported versions
Security fixes are made only for the [latest release](../../releases/latest). Please make sure you are on the current version first.

### Reporting a vulnerability
**Please do not report security issues on the public Issues page.** Instead:

1. Open the **Security** tab of this repository.
2. Use **Report a vulnerability** to open a private report. Only you and the developer can see it.

Please include:
- The affected DevronDPI and Windows versions.
- What the problem is and how to reproduce it.
- Its possible impact (for example privilege escalation, or a malicious update/rules file being accepted).

After reviewing a report I will keep the details private until a fix is released. If you wish, you will be credited in the release notes once it is fixed.

### Scope
In scope:
- A normal-rights program gaining administrator rights through DevronDPI.
- The elevated engine process accepting commands from another program.
- A bypass of the update verification (SHA-256, GitHub address check) or `rules.json` RSA-2048 signature verification.
- Code execution through the settings, rules, or log files, or leakage of user data.

Out of scope:
- A site blocked at the IP address level (no DPI tool can open it).
- Windows' "Unknown publisher" / SmartScreen warning because the exe is not digitally signed.
- Antivirus false alarms caused by WinDivert (explained in the README).
- DPI bypass not working on a particular network (that is a bug report: use the [Issues](../../issues) page).

---

## Türkçe

### Desteklenen sürümler
Güvenlik düzeltmeleri yalnızca [son sürüm](../../releases/latest) için yayınlanır. Bildirim göndermeden önce güncel sürümü kullandığınızdan emin olun.

### Güvenlik açığı bildirme
**Güvenlik açıklarını herkese açık Sorunlar (Issues) sayfasından bildirmeyin.** Bunun yerine:

1. Bu deponun **Security** sekmesine gidin.
2. **Report a vulnerability** düğmesiyle özel bildirim açın. Bildirimi yalnızca siz ve geliştirici görebilir.

Bildirime şu bilgileri ekleyin:
- Etkilenen DevronDPI ve Windows sürümü.
- Sorunun ne olduğu ve nasıl yeniden üretileceği.
- Olası etkisi (ör. yetki yükseltme, sahte bir güncelleme veya kural dosyasının kabul edilmesi).

Bildirimi inceledikten sonra düzeltme yayınlanana kadar ayrıntıları gizli tutarım. Düzeltme yayınlandığında isterseniz adınız sürüm notlarında teşekkür olarak belirtilir.

### Kapsam
Şu durumlar güvenlik sorunu kapsamındadır:
- Normal kullanıcı yetkili bir programın DevronDPI aracılığıyla yönetici yetkisi kazanması.
- Yönetici motor işleminin başka bir programdan komut kabul etmesi.
- Güncelleme doğrulamasının (SHA-256 özeti, GitHub adres kontrolü) veya `rules.json` RSA-2048 imza doğrulamasının aşılabilmesi.
- Ayar, kural veya kayıt dosyaları üzerinden kod çalıştırılabilmesi ya da kullanıcı verilerinin sızması.

Şu durumlar kapsam dışıdır:
- Bir sitenin doğrudan IP adresi düzeyinde engellenmiş olması (DPI aracı bunu aşamaz).
- Dijital kod imzası bulunmadığı için Windows SmartScreen tarafından gösterilen "Yayıncı bilinmiyor" uyarısı.
- Antivirüs yazılımlarının WinDivert sürücüsü nedeniyle verdiği yanlış alarmlar (`README.md` içinde açıklanmıştır).
- DPI aşma yöntemlerinin belirli bir ağda çalışmaması (bu bir hata bildirimidir; [Sorunlar (Issues)](../../issues) sayfasından iletebilirsiniz).
