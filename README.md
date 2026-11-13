# PureClean Releases

Bu depo yalnızca **yayın artefaktlarını** barındırır:

- `PureClean_<sürüm>_x64-setup.exe` — NSIS installer
- `...exe.sig` — Tauri updater minisign imzası
- `latest.json` — güncelleme manifesti

Kaynak kod özel depoda tutulur. Güncelleme uç noktası:

`https://github.com/Fastrree/PureClean-Releases/releases/latest/download/latest.json`

## Doğrulama

```powershell
Invoke-WebRequest "https://github.com/Fastrree/PureClean-Releases/releases/latest/download/latest.json"
```

İmza `tauri signer` tarafından üretilir; uygulama güncellemeyi kurmadan önce doğrular.
