# Third-Party Notices / Üçüncü Taraf Bildirimleri

🇬🇧 English · 🇹🇷 [Türkçe aşağıda](#türkçe)

## English

DevronDPI is closed-source freeware (see `LICENSE`). It uses the following third-party components:

### WinDivert 2.2 (Windows) — LGPLv3

- **Files:** `WinDivert.dll`, `WinDivert64.sys`
- **Copyright:** © Basil (basil00 / Reqrypt), 2011–2022
- **License:** GNU Lesser General Public License, version 3 (LGPLv3)
  - LGPLv3 text: https://www.gnu.org/licenses/lgpl-3.0.txt
  - GPLv3 text, which the LGPLv3 builds on: https://www.gnu.org/licenses/gpl-3.0.txt
  - Copies of both texts are in the `LICENSES` folder of this repository (`LICENSES/LGPL-3.0.txt`, `LICENSES/GPL-3.0.txt`).
- **Source code:** https://github.com/basil00/WinDivert (release v2.2.2 is the version DevronDPI uses: https://github.com/basil00/WinDivert/releases/tag/v2.2.2)
- DevronDPI embeds the original, **unmodified** official WinDivert binaries and loads them as a separate dynamic library (`WinDivert.dll`) and driver (`WinDivert64.sys`). The LGPLv3 applies to WinDivert only, not to DevronDPI. DevronDPI's own license does not restrict your rights under the LGPLv3 (see `LICENSE`, sections 2 and 3).
- The files embedded in `DevronDPI.exe` (SHA-256), so you can compare them with the official release:
  - `WinDivert.dll` (47,616 bytes): `c1e060ee19444a259b2162f8af0f3fe8c4428a1c6f694dce20de194ac8d7d9a2`
  - `WinDivert64.sys` (94,144 bytes): `8da085332782708d8767bcace5327a6ec7283c17cfb85e40b03cd2323a90ddc2`
- On first connect DevronDPI writes these two files to `C:\ProgramData\DevronDPI\WinDivert-<id>\` and loads them from there. If you wish to use your own compatible 64-bit `WinDivert.dll` and `WinDivert64.sys` build under the LGPLv3, place both files in `C:\Program Files\DevronDPI\WinDivert\`.

### Hev SOCKS5 Tunnel Library (`com.zaneschepke:hevtunnel` 1.0.1, Android) — Apache-2.0 / MIT / BSD-3-Clause

- **Component:** `com.zaneschepke:hevtunnel:1.0.1` (Android wrapper around `hev-socks5-tunnel` and `lwIP`)
- **Copyright:** © Zane Schepke (Android library), © Heiher (`hev-socks5-tunnel`), © Swedish Institute of Computer Science (`lwIP`)
- **Licenses:**
  - `hevtunnel`: Apache License, Version 2.0 (https://www.apache.org/licenses/LICENSE-2.0.txt)
  - `hev-socks5-tunnel`: MIT License (https://github.com/heiher/hev-socks5-tunnel)
  - `lwIP`: BSD 3-Clause License
- **Source code:** https://github.com/zaneschepke/amneziawg-android · https://github.com/heiher/hev-socks5-tunnel

### AndroidX & Material Components for Android — Apache-2.0

- **Components:** `androidx.core:core-ktx`, `androidx.appcompat:appcompat`, `com.google.android.material:material`
- **License:** Apache License, Version 2.0 (https://www.apache.org/licenses/LICENSE-2.0.txt)

---

## Türkçe

DevronDPI kapalı kaynaklı ücretsiz bir yazılımdır (bkz. `LICENSE`). Uygulama aşağıdaki üçüncü taraf bileşenlerini kullanır:

### WinDivert 2.2 (Windows) — LGPLv3

- **Dosyalar:** `WinDivert.dll`, `WinDivert64.sys`
- **Telif hakkı:** © Basil (basil00 / Reqrypt), 2011–2022
- **Lisans:** GNU Kısıtlı Genel Kamu Lisansı, sürüm 3 (LGPLv3)
  - LGPLv3 metni: https://www.gnu.org/licenses/lgpl-3.0.txt
  - LGPLv3'ün temel aldığı GPLv3 metni: https://www.gnu.org/licenses/gpl-3.0.txt
  - Her iki metnin kopyası bu deponun `LICENSES` klasöründe (`LICENSES/LGPL-3.0.txt`, `LICENSES/GPL-3.0.txt`) yer alır.
- **Kaynak kodu:** https://github.com/basil00/WinDivert (DevronDPI tarafından kullanılan sürüm v2.2.2: https://github.com/basil00/WinDivert/releases/tag/v2.2.2)
- DevronDPI; resmî ve **değiştirilmemiş** WinDivert dosyalarını barındırır, bunları ayrı bir dinamik kütüphane (`WinDivert.dll`) ve sürücü (`WinDivert64.sys`) olarak yükler. LGPLv3 yalnızca WinDivert bileşeni için geçerlidir, DevronDPI için geçerli değildir. DevronDPI lisansı, LGPLv3 kapsamındaki haklarınızı kısıtlamaz (bkz. `LICENSE`, madde 2 ve 3).
- `DevronDPI.exe` içindeki gömülü dosyaların SHA-256 özetleri (resmî sürümle karşılaştırabilirsiniz):
  - `WinDivert.dll` (47.616 bayt): `c1e060ee19444a259b2162f8af0f3fe8c4428a1c6f694dce20de194ac8d7d9a2`
  - `WinDivert64.sys` (94.144 bayt): `8da085332782708d8767bcace5327a6ec7283c17cfb85e40b03cd2323a90ddc2`
- İlk bağlantıda bu iki dosya `C:\ProgramData\DevronDPI\WinDivert-<kimlik>\` klasörüne çıkarılır ve oradan yüklenir. LGPLv3 kapsamında kendi uyumlu 64-bit `WinDivert.dll` ve `WinDivert64.sys` dosyalarınızı kullanmak isterseniz her iki dosyayı `C:\Program Files\DevronDPI\WinDivert\` klasörüne koyabilirsiniz.

### Hev SOCKS5 Tunnel Library (`com.zaneschepke:hevtunnel` 1.0.1, Android) — Apache-2.0 / MIT / BSD-3-Clause

- **Bileşen:** `com.zaneschepke:hevtunnel:1.0.1` (`hev-socks5-tunnel` ve `lwIP` için Android sarmalayıcısı)
- **Telif hakkı:** © Zane Schepke (Android kütüphanesi), © Heiher (`hev-socks5-tunnel`), © Swedish Institute of Computer Science (`lwIP`)
- **Lisanslar:**
  - `hevtunnel`: Apache License, Version 2.0 (https://www.apache.org/licenses/LICENSE-2.0.txt)
  - `hev-socks5-tunnel`: MIT Lisansı (https://github.com/heiher/hev-socks5-tunnel)
  - `lwIP`: BSD 3-Clause Lisansı
- **Kaynak kodu:** https://github.com/zaneschepke/amneziawg-android · https://github.com/heiher/hev-socks5-tunnel

### AndroidX & Material Components (Android) — Apache-2.0

- **Bileşenler:** `androidx.core:core-ktx`, `androidx.appcompat:appcompat`, `com.google.android.material:material`
- **Lisans:** Apache License, Version 2.0 (https://www.apache.org/licenses/LICENSE-2.0.txt)
