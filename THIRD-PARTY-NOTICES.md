# Third-party notices / Üçüncü taraf bildirimleri

DevronDPI is closed-source freeware (see `LICENSE`).
It uses the following third-party components.

## WinDivert 2.2 — LGPLv3

- Files: `WinDivert.dll`, `WinDivert64.sys`
- Copyright (c) Basil (basil00 / Reqrypt), 2011-2022
- License: GNU Lesser General Public License, version 3 (LGPLv3).
  - LGPLv3 text: https://www.gnu.org/licenses/lgpl-3.0.txt
  - GPLv3 text, which the LGPLv3 builds on: https://www.gnu.org/licenses/gpl-3.0.txt
  - Copies of both texts are in the `LICENSES` folder of this repository
    (`LICENSES/LGPL-3.0.txt`, `LICENSES/GPL-3.0.txt`).
- Source code: https://github.com/basil00/WinDivert (release v2.2.2 is the version DevronDPI uses:
  https://github.com/basil00/WinDivert/releases/tag/v2.2.2)
- DevronDPI embeds the original, **unmodified** official WinDivert binaries and loads them as a
  separate dynamic library (`WinDivert.dll`) and driver (`WinDivert64.sys`). The LGPLv3 applies to
  WinDivert only, not to DevronDPI. DevronDPI's own license does not restrict your rights under
  the LGPLv3 (see `LICENSE`, sections 2 and 3).
- The files embedded in `DevronDPI.exe` (SHA-256), so you can compare them with the official release:
  - `WinDivert.dll` (47,616 bytes): `c1e060ee19444a259b2162f8af0f3fe8c4428a1c6f694dce20de194ac8d7d9a2`
  - `WinDivert64.sys` (94,144 bytes): `8da085332782708d8767bcace5327a6ec7283c17cfb85e40b03cd2323a90ddc2`
- On first connect DevronDPI writes these two files to `C:\ProgramData\DevronDPI\WinDivert-<id>\`
  and loads them from there.

## ConfuserEx, dnlib (build-time tools only)

- License: MIT (https://github.com/mkaring/ConfuserEx, https://github.com/0xd4d/dnlib)
- Not used for the released build; not part of the running application.

---

## Türkçe özet

DevronDPI kapalı kaynaklı ücretsiz bir yazılımdır (bkz. `LICENSE`).

**WinDivert 2.2 (LGPLv3):** Paket yakalama için resmî, **değiştirilmemiş** WinDivert dosyaları
(`WinDivert.dll`, `WinDivert64.sys`) `DevronDPI.exe`'nin içine gömülüdür ve ayrı bir kütüphane ve
sürücü olarak yüklenir. LGPLv3 yalnızca WinDivert için geçerlidir, DevronDPI için değil.
DevronDPI'ın lisansı, LGPLv3'ten doğan haklarınızı kısıtlamaz. Lisans metinleri `LICENSES` klasöründedir; kaynak kod
yukarıdaki bağlantıdadır. Gömülü dosyaların SHA-256 özetleri yukarıda verilmiştir; resmî
sürümle karşılaştırabilirsiniz.
