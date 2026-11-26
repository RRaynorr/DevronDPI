# Third-party notices

DevronDPI is closed-source freeware (see `LICENSE`).
It uses the following third-party components.

## WinDivert 2.2 — LGPLv3

- Files: `WinDivert.dll`, `WinDivert64.sys`
- Copyright (c) basil00 (Reqrypt)
- License: GNU Lesser General Public License v3.0
- Unmodified source code and full license text: https://github.com/basil00/WinDivert
- DevronDPI embeds the original, unmodified WinDivert binaries and loads them as a separate
  dynamic library and driver. The LGPLv3 applies only to WinDivert, not to DevronDPI.

## ConfuserEx, dnlib (build-time tools only)

- License: MIT (https://github.com/mkaring/ConfuserEx, https://github.com/0xd4d/dnlib)
- Used only to protect the build output; not part of the running application.
