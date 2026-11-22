# APK Utils

A small collection of Bash aliases and functions for downloading, inspecting,
and reverse engineering Android APKs.

## Setup

Source the script in your shell profile:

```bash
source /path/to/apk_utils/apk_utils
```

The script expects its tools under `~/.bb/MobSec/Android` and adds one Android
SDK build-tools directory to `PATH`. Edit the paths and versions at the top of
the script if your installation differs.

## Commands

- `apk_download <package> [downloader]` - Download an APK. Downloaders are
  `playstore-arm` (default), `playstore-arm64`, `playstore-x86`, or `gplaycli`.
- `apk_pull <package>` - Pull an APK from a connected device and merge split
  APKs when necessary.
- `apk_rename <file.apk>` - Rename an APK using its package name and version.
- `apk_decompile_one <file.apk>` - Decompile one APK with Apktool and JADX.
- `apk_decompile_all` - Decompile every APK in the current directory.
- `adb_logcat_pkg <package>` - Follow logcat output for one package.
- `playstore_open <package>` - Open an app's Play Store page on a device.
- `adb_open_url <url>` - Open a URL on a connected device.
- `update_apktool` / `update_jadx` - Pull and build the bundled Apktool or
  JADX sources.

Additional aliases provide direct access to Apktool, JADX, Procyon, Enjarify,
APKEditor, Recaf, and Android schemas.
