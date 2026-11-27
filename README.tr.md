# DevronDPI

**Windows için tek tıkla DPI aşma aracı.** İnternet servis sağlayıcınızın derin paket denetimiyle (DPI) engellediği web sitelerine, uygulamalara, çevrim içi oyunlara ve sesli sohbet platformlarına VPN kullanmadan, hız ve gecikme (ping) kaybı olmadan erişin.

🇬🇧 [English](README.md) &nbsp;|&nbsp; 🇹🇷 **Türkçe**

[![Sürüm](https://img.shields.io/github/v/release/RRaynorr/DevronDPI?style=for-the-badge&logo=github&label=S%C3%9CR%C3%9CM&color=10B981)](../../releases/latest) [![İndirme](https://img.shields.io/github/downloads/RRaynorr/DevronDPI/total?style=for-the-badge&label=%C4%B0ND%C4%B0RME&color=E11D48)](../../releases) [![VirusTotal v1.3](https://img.shields.io/badge/VirusTotal_v1.3-2%2F67-yellow?style=for-the-badge&logo=virustotal&logoColor=white)](https://www.virustotal.com/gui/file/22a83858f4a1fcaa1af30e55f3fac2c775c0b1d24d7e880dd62afd7c677313b8)

**[⬇ Son sürümü indir](../../releases/latest)** · Kurulum gerektirmez. `DevronDPI.exe` dosyasını çalıştırın ve **BAĞLAN** düğmesine basın.

## Neler yapar?

- **Ayar istemez.** Ağınızı test eder, çalışan yöntemi bulur ve her ağ için ayrı kaydeder (ev ağı, telefonun mobil erişim noktası vb.). Sonraki bağlantılar daha hızlı kurulur.
- **VPN değildir.** Trafik başka bir sunucudan geçmez; gecikme süresi (ping) ve hız değişmez.
- **"Bağlı" gerçekten bağlı demektir.** Engelli test siteleriyle güvenli bağlantı doğrulanmadan yeşil yanmaz.
- **4 aşamalı Engel Röntgeni ve site bazlı kurallar.** Bildirim alanı menüsündeki **Bağlantıyı tanıla** penceresi `1. DNS → 2. TCP → 3. TLS SNI → 4. 24 KB Akış` aşamalarını canlı sürelerle gösterir. Belirli bir site açılmıyorsa arka planda alternatifleri test eder; yalnızca 4/4 geçtiği kanıtlandığında **Çalışan Kuralı Uygula** (siteye özel kaydedilir, sıfırlanabilir) veya **Muafiyet Listesine Ekle** düğmesini sunar.
- **Şifreli DNS (DoH) ve Anycast köprüsü.** Ağınızda `1.1.1.1` veya `9.9.9.9` gibi bilinen sağlayıcı IP adresleri doğrudan engelliyse bağlantıyı aynı sağlayıcıya ait sertifika doğrulamalı alternatif Anycast IP adresine yönlendirir.
- **Oyun, anti-cheat, kamu ve özel muafiyet listesi.** Kamu/akademik alan adları (`.gov`, `.edu`, `.gov.tr`, `.edu.tr`, `.gov.uk`, `.ac.uk` vb.) ile hassas oyun/anti-cheat servislerini (`Riot Vanguard`, `Steam`, `Battle.net`, `EasyAntiCheat`, `BattlEye` vb.) otomatik olarak doğrudan geçirir; bildirim alanı menüsündeki **Muafiyet listesi** üzerinden kendi alan adlarınızı (banka, kurumsal portal vb.) da ekleyebilirsiniz.
- **Discord sesli sohbet.** "RTC Bağlanıyor" aşamasında takılma sorununa yardımcı olur.
- **Ağ değişimi, uyku ve kilit ekranında otomatik toparlanma.** Kablosuz ağ değiştiğinde, bilgisayar uykudan uyandığında veya kilit ekranından dönüldüğünde bağlantıyı otomatik kontrol edip doğrular.
- **İzleyici & reklam koruması (isteğe bağlı, 0 ms).** Bildirim alanı menüsünden açıldığında bilinen reklam, izleme ve telemetri alan adlarını HTTPS şifresini kırmadan ve sertifika kurmadan yerel olarak engeller; tarayıcıda DoH açıkken bile çalışır.
- **Dijital imzalı kural güncellemeleri (`rules.json`).** GitHub üzerinden RSA-2048 imzasıyla doğrulanan hafif güncellemeler; yeni sürüm kurmaya gerek kalmadan muafiyet, izleyici ve site kurallarını güncel tutar, çevrim dışı durumda yerleşik kurallarla kesintisiz çalışır.
- **Akıcı arayüz ve canlı Windows tema takibi.** Ekran, sekme, tema, dil, menü ve kaydırmada yumuşak geçişler, boşta %0 işlemci kullanımı ve Windows Koyu/Açık tema değişimine canlı uyum.
- **Taşınabilir (USB) kip ve ayar yedekleme.** Bildirim alanı menüsünden ayarlarınızı tek tıkla dışa/içe aktarın veya `DevronDPI.exe` yanına boş bir `portable.flag` dosyası koyarak tüm ayar ve kayıtları `%AppData%` yerine doğrudan uygulama klasöründe tutun.

Ayrıca başlangıçta çalıştırma, açılışta otomatik bağlanma, arka planda çalışma, kısayol tuşu, İngilizce/Türkçe arayüz, açık/koyu tema ve desteklenmeyen sistemlerde (ARM64 / 32-bit) açılışta net uyumluluk bilgilendirmesi bulunur. 64-bit Windows 10/11 içindir.

## Ekran görüntüleri

| Bağlı | Kayıtlar |
|:---:|:---:|
| <img src="docs/baglandi.png" width="300" alt="Bağlı ekranı"> | <img src="docs/kayitlar.png" width="300" alt="Kayıtlar ekranı"> |
| **Bildirim alanı menüsü** | **Açık tema** |
| <img src="docs/bildirim-menusu.png" width="300" alt="Bildirim alanı menüsü"> | <img src="docs/acik-tema.png" width="300" alt="Açık tema"> |

## Kullanım

1. `DevronDPI.exe` dosyasını çalıştırın.
2. **BAĞLAN** düğmesine basın. İlk bağlantıda Windows yönetici izni ister; **Evet** diyerek onaylayın.

Analiz birkaç saniye sürer. Bağlanırken düğmeye tekrar basarsanız işlem iptal edilir.

<details>
<summary><b>Pencere, bildirim alanı ve kayıtlar</b></summary>

- **X** düğmesi uygulamayı kapatır ve bağlantıyı keser. Üst çubuktan **Arka planda çalış** seçeneğini açarsanız X ve küçült düğmeleri pencereyi bildirim alanına gizler.
- Pencere açık değilken bağlantı koparsa ya da yeniden kurulursa Windows bildirimi gösterilir.
- **Bildirim alanı simgesi:** Sol tıklama pencereyi açar. Sağ tıklama ile açılan bildirim alanı menüsünde bağlan/kes, **Başlangıçta çalıştır**, **Açılışta otomatik bağlan** (varsayılan olarak kapalıdır), **İzleyici & reklam koruması** (varsayılan olarak kapalıdır), **Arka planda çalış**, kısayol tuşu, **Muafiyet listesi**, **Ayarları yedekle / geri yükle**, **Bağlantıyı tanıla** (4 aşamalı Engel Röntgeni), güncelleme kontrolü ve **Çıkış** yer alır.
- **Kayıtlar:** Tek parça kapsül sekmeler (*Tümü / Uyarı / Hata / Ayrıntı*), 3 canlı gösterge (*Korunan Akış*, *Önlenen Kesinti*, *DNS & Köprü*), kart içi anlık arama ve tek tıkla **Kayıtları kopyala** / **Kaydet** / **Temizle** düğmelerini içerir.

</details>

<details>
<summary><b>Yönetici izni ve "Başlangıçta çalıştır"</b></summary>

WinDivert ile paket yakalamak yönetici yetkisi gerektirir. Pencere normal kullanıcı yetkisiyle çalışır; yalnızca paket motoru ayrı bir süreçte yönetici olarak başlar. Bu sayede ekran görüntüsü araçları ve kısayollar kesintiye uğramaz. Pencere kapanınca motor da durur.

**Başlangıçta çalıştır** seçeneğini açarken yönetici iznini bir kez verirsiniz. Sonrasında ne Windows açılışında ne de **BAĞLAN** düğmesine basıldığında yeniden onay istenir (yalnızca güncelleme sonrasındaki ilk bağlantıda bir kez daha sorulabilir). Bu seçenek `DevronDPI.exe` dosyasının bir kopyasını, yalnızca yöneticilerin değiştirebildiği `C:\Program Files\DevronDPI\` klasörüne yerleştirir ve zamanlanmış bir görev oluşturur. Seçeneği kapattığınızda ikisi de kaldırılır. Dosyayı başka bir klasöre taşırsanız bu seçeneği bir kez kapatıp yeniden açın.

</details>

## Bilmeniz gerekenler

- **Genel IP engelini aşamaz.** Bir site doğrudan IP adresi düzeyinde engelliyse (desteklenen Anycast sağlayıcıları dışında) hiçbir DPI aracı bu engeli aşamaz, VPN gerekir. DevronDPI bu durumu tespit eder ve açıklar.
- **"Bağlı" durumu her sitenin açılacağı anlamına gelmez;** ağınızda engelli görünen test sitelerine erişilebildiğini gösterir.
- **Sistem DNS sorguları şifrelenmez.** Alan adı sorguları seçilen DNS sunucusuna şifresiz iletilir. Tarayıcınızın kendi şifreli DNS (DoH) ayarı ise etkilenmez; Anycast köprüsü sayesinde engelli ağlarda da çalışmayı sürdürür.
- **Şirket ve okul ağlarında** DNS yönlendirmesi nedeniyle yerel ağdaki iç alan adları çözülemeyebilir.
- **QUIC engeli** nedeniyle UDP 443 portunu kullanan bazı VPN uygulamaları etkilenebilir.
- DNS yönlendirmesi arayüzden kapatılamaz. Yönlendirme yapmayan tek yöntem Global seçeneğidir ve en son sırada denenir.

## Gizlilik

- Veri toplanmaz, telemetri bulunmaz. Ayarlar ve kayıtlar (`devron.conf`, `devron.log`, `devron-engine.log`, `rules.cache.json`) yalnızca `%AppData%\DevronDPI` klasöründe tutulur.
- Bağlantı ve tanılama kontrollerinde test edilen adreslerle yalnızca TLS bağlantı kurulumu ve kısa veri akışı doğrulaması yapılır; kişisel bir veri gönderilmez. Bağlanılan her sitede olduğu gibi karşı sunucu IP adresinizi görür.
- Üçüncü taraflara yalnızca iki bilgi gider: **DNS sorguları** seçilen sunucuya (Yandex, OpenDNS, AdGuard veya Quad9), **güncelleme ve imzalı kural kontrolleri** ise GitHub sunucularına. Bu hizmetlerin kendi gizlilik politikaları geçerlidir.

## Güvenlik

- **Güncellemeler** GitHub üzerinden alınır, onayınız olmadan kurulmaz ve SHA-256 özeti eşleşmezse reddedilir. Sürüm geçmişi için [CHANGELOG.md](CHANGELOG.md) dosyasına bakabilirsiniz.
- **İmzalı kural güncellemeleri (`rules.json`)** hem indirilirken hem de yerel önbellekten okunurken gömülü RSA-2048 açık anahtarıyla doğrulanır; imzasız, kurcalanmış veya sınır dışı hiçbir kural kabul edilmez ve kod/komut çalıştırılamaz.
- **Uygulama dosyası henüz dijital imzalı değildir.** Bu nedenle Windows SmartScreen ya da "Yayıncı bilinmiyor" uyarısı görünebilir. Uygulamayı yalnızca [sürümler](../../releases) sayfasından indirin ve SHA-256 özetini sürüm notlarıyla karşılaştırın.
- **Antivirüs uyarıları** (`RiskTool.WinDivert` vb.), paket yakalama sürücüsünden (WinDivert) kaynaklanan yanlış alarmlardır. WinDivert, GoodbyeDPI uygulamasının da kullandığı Microsoft imzalı resmî bir sürücüdür. Gerekirse `DevronDPI.exe` dosyasını antivirüs istisnalarına ekleyebilirsiniz.

Güvenlik açığı bildirmek için [SECURITY.md](SECURITY.md) dosyasını inceleyin.

<details>
<summary><b>Nasıl çalışır?</b></summary>

DPI sistemleri bağlandığınız siteyi genellikle TLS `ClientHello` paketindeki SNI alanından tanır. DevronDPI, WinDivert aracılığıyla giden paketleri yakalar ve gönderilmeden önce bilgisayarınızda yeniden düzenler:

- **SNI bölme:** `ClientHello` paketi birkaç TCP parçasına bölünür; böylece DPI sistemi alan adını tek parça hâlinde göremez.
- **Sahte paketler:** Düşük TTL değerli ya da geçersiz TCP Seq, Checksum veya TCP MD5 seçeneği taşıyan sahte paketler DPI sistemini yanıltır. Uygun TTL değeri, paket DPI cihazına ulaşıp hedef sunucuya varmadan düşecek biçimde, sunucunun `SYN-ACK` yanıtından ölçülen ağ yönlendirici (hop) mesafesine göre otomatik hesaplanır (Auto-TTL).
- **DNS yönlendirme:** UDP 53 sorguları Yandex DNS sunucusuna (`77.88.8.8`) standart olmayan 1253 portundan iletilir. Yanıt alınamazsa sırasıyla OpenDNS, AdGuard ve Quad9 denenir; büyük yanıtlarda doğrulanan TCP DNS yedeği devreye girer.
- **Anycast köprüsü:** `1.1.1.1`, `9.9.9.9`, `208.67.222.222`, `8.8.8.8` veya `94.140.14.14` doğrudan engelliyse bağlantı, işletim sisteminin sertifika deposuyla doğrulanan alternatif Anycast IP adresine yönlendirilir.
- **QUIC engeli:** Giden UDP 443 paketleri düşürülür; böylece tarayıcılar ve Discord HTTP/3 yerine TCP üzerinden TLS kullanır.
- **Discord sesli sohbet:** Ses sunucusuna giden ilk 74 baytlık keşif paketinin hemen önüne zararsız bir sahte paket eklenir. Ses akışına dokunulmaz.

Analiz önce bu ağda daha önce çalışan yöntemi dener; ardından sırasıyla standart, alternatif, hafif, yedek DNS ve global yöntemlere, en son da farklı bölme noktalarına geçer.

443 numaralı portta yalnızca ilk bağlantı paketleri kullanıcı moduna alınır. İndirme, video ve oyun trafiği işletim sistemi çekirdeğinde kalır; işlemci kullanımı sıfıra yakındır.

</details>

## Sıkça sorulan sorular

<details>
<summary><b>"Bağlı" yazıyor ama bir site açılmıyor.</b></summary>

Bildirim alanı menüsünden **Bağlantıyı tanıla** penceresini açıp o sitenin adresini yazın; 4 aşamalı Engel Röntgeni (`DNS → TCP → TLS SNI → 24 KB Akış`) sorunun tam kaynağını gösterir. Alternatif yöntem veya muafiyet işe yarıyorsa doğrulanıp tek tıkla uygulanabilir. Doğrudan IP engellerinde VPN gerekir.
</details>

<details>
<summary><b>Discord "RTC Bağlanıyor" aşamasında takılı kalıyor.</b></summary>

DevronDPI bağlıyken bu sorun genellikle düzelir. Ses sunucusunun IP adresi doğrudan engelliyse açılamaz. Bağlı olduğunuzdan ve **Kayıtlar** ekranında hata bulunmadığından emin olun.
</details>

<details>
<summary><b>Tarayıcım şifreli DNS (DoH) kullanıyor, sorun olur mu?</b></summary>

Hayır. Tarayıcınız kendi şifreli DNS ayarını kullanmaya devam eder; üstelik Cloudflare (`1.1.1.1`) veya Quad9 (`9.9.9.9`) ağınızda engelliyse Anycast köprüsü sayesinde DoH bağlantısı da çalışır.
</details>

<details>
<summary><b>Uygulamayı nasıl kaldırırım?</b></summary>

Önce bildirim alanı menüsünden **Başlangıçta çalıştır** seçeneğini kapatın (zamanlanmış görevi ve `Program Files` kopyasını siler). Ardından `DevronDPI.exe` dosyasını silin. İsterseniz `%AppData%\DevronDPI` (ayarlar ve kayıtlar) ile `C:\ProgramData\DevronDPI` (sürücü dosyaları) klasörlerini de silebilirsiniz.
</details>

## Sorun bildirme

[Sorunlar (Issues)](../../issues) sayfasından yeni kayıt açıp şunları ekleyin:

- **Kayıtlar** ekranındaki **Kayıtları kopyala** çıktısı (uygulama sürümü, yöntem özeti, sayaçlar ve motor kayıtları içindedir).
- Ne yaptığınız ve neyle karşılaştığınız, mümkünse ekran görüntüsü.

Kayıtlarda test edilen sitelerin adları yer alabilir; paylaşmadan önce gözden geçirin.

## Lisans

Ücretsiz ve kapalı kaynaklıdır; [LICENSE](LICENSE) koşullarıyla dağıtılır. © 2026 RRaynorr

WinDivert bileşeni LGPLv3 lisanslıdır. Ayrıntılar ve kendi WinDivert sürümünüzü kullanma bilgisi için [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) dosyasına bakın.
