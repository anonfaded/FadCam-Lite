<div align="center">

<img src="https://raw.githubusercontent.com/anonfaded/FadCam/master/design-assets/PSDs/fadcam_lite.png" alt="FadCam Lite logo" width="140">

# `>_` FadCam Lite

**Record video on Android, even with the screen off.**

FadCam’s recording engine in a **~14 MB download**.

Android 7.0+ · Ad-free · Open source

<a href="https://github.com/anonfaded/FadCam-Lite/releases">
    <img src="https://raw.githubusercontent.com/vadret/android/master/assets/get-github.png" alt="Get it on GitHub" height="70"></a>

<br>

[![GitHub all releases](https://img.shields.io/github/downloads/anonfaded/FadCam-Lite/total?label=Downloads&logo=github)](https://github.com/anonfaded/FadCam-Lite/releases/)

<sub>Scan to visit the Patreon shop</sub><br>
<img src="https://raw.githubusercontent.com/anonfaded/FadCam/master/app/src/main/assets/QRCodes/QRCode_patreon_shop.png" alt="Scan to visit the Patreon shop" width="150">

</div>

> [!Tip]
> This project is part of the [FadSec Lab suite](https://github.com/fadsec-lab), ad-free and privacy-first.

> [!Note]
> FadCam Lite Pro (three disguised apps, lifetime access) is being added to the [Shop](https://www.patreon.com/cw/Fadedx/shop) in the next few days, before 2027. Until then the shop lists the current FadCam Pro bundle.

---

<details>
<summary>Table of contents</summary>

- [Screenshots](#_-screenshots)
- [What is FadCam Lite?](#_-what-is-fadcam-lite)
- [What you get](#_-what-you-get)
- [Lite vs. full FadCam](#_-which-one-should-you-install)
- [Download](#_-download)
- [Privacy](#_-privacy)
- [Building from source](#_-building-from-source)
- [Support and shop](#_-support--shop)
- [Community](#_-community)

</details>

---

## `>_` Screenshots

| Home | Records | Settings |
| :---: | :---: | :---: |
| <img src="https://raw.githubusercontent.com/anonfaded/FadCam/master/src/lite/fastlane/metadata/android/en-US/images/phoneScreenshots/01-home.png" alt="FadCam Lite Home tab" width="240"> | <img src="https://raw.githubusercontent.com/anonfaded/FadCam/master/src/lite/fastlane/metadata/android/en-US/images/phoneScreenshots/02-records.png" alt="FadCam Lite Records tab" width="240"> | <img src="https://raw.githubusercontent.com/anonfaded/FadCam/master/src/lite/fastlane/metadata/android/en-US/images/phoneScreenshots/03-settings.png" alt="FadCam Lite Settings tab" width="240"> |

## `>_` What is FadCam Lite?

FadCam Lite is the **little brother of [FadCam](https://github.com/anonfaded/FadCam)**.

FadCam grew into a full multimedia suite: video editor, screen recorder, live streaming, remote control, on-device AI. That is a lot of app when all you want is to press record and know the file will survive.

Lite keeps the recorder and drops the suite. Same engine, same crash-safe files, same privacy, **~14 MB instead of ~186 MB**.

**Smaller app. Simpler interface. Less storage. Nothing to configure if you don't want to.**

> [!TIP]
> **Time to uninstall a few apps.**
>
> FadCam Lite does their jobs too. Yes, all of these. Without any trackers or dark patterns.
>
> - **Background recording:** Record even with the screen off, powered by crash-resistant Hybrid MP4 technology.
> - **Bodycam:** Wear it for personal security and hands-free recording.
> - **Dashcam:** Record the road or motovlogs smoothly with video stabilization.
>
> **3 Jobs. One FadCam.** Time to say goodbye to those extra apps. The full [FadCam](https://github.com/anonfaded/FadCam) replaces 10 apps.

## `>_` What you get

- **Hybrid MP4**: powered by FadCam's Hybrid MP4 pipeline. Designed to preserve recorded footage through crashes, power loss, and sudden shutdowns.
- **Front / back / dual camera** where your device supports it
- **Watermarks**: timestamp, location, logo or your own text
- **Video splitting by file size**
- **10 shortcuts** ready for your home screen or automation workflows. For example, use an automation app to bind a recording shortcut to a volume button.
- **Tab Lock** for Home, Records, and Settings, with PIN, password, or biometric unlock
- **Clock widget**

## `>_` What is not included

These live in the full app only:

| Feature | Why it is Full-only |
|---|---|
| Video editor (Faditor Mini) | Ships FFmpeg, ~45 MB of native libraries |
| Screen recording (FadRec) | Separate capture pipeline and overlay system |
| Remote streaming | Bundled web UI and network stack (~2 MB) |
| Motion detection | Ships OpenCV, ~51 MB |
| Forensic intelligence | LiteRT runtime (~15 MB) and on-device AI model (~54 MB) |
| Mini apps (torch, QR) | Outside the recorder's scope |

Together that is **~166 MB of libraries and assets**, the difference between a ~186 MB suite and a ~14 MB recorder.

## `>_` Which one should you install?

**Choose FadCam Lite** if you want a dependable background recorder that stays out of the way and out of your storage.

**Choose [FadCam](https://github.com/anonfaded/FadCam)** if you want the editor, screen recording, streaming, motion detection and forensic intelligence.

They are separate apps with separate package names, so you can install both side by side.

## `>_` Download

<a href="https://github.com/anonfaded/FadCam-Lite/releases">
    <img src="https://raw.githubusercontent.com/vadret/android/master/assets/get-github.png" alt="Download FadCam Lite on GitHub" height="70"></a>

## `>_` Privacy

- No ads, no analytics, no trackers, no accounts
- Your recordings never leave your device
- At launch, Lite can check GitHub Releases for updates. You can turn off update checks in Settings.

## `>_` Source code and issues

This repository hosts FadCam Lite releases and tracks Lite issues separately from the full app. [Report a FadCam Lite issue](https://github.com/anonfaded/FadCam-Lite/issues)

FadCam Lite is open source under GPL-3.0. Its `lite` build flavor lives in the shared FadCam codebase. [Browse the source or contribute](https://github.com/anonfaded/FadCam)

## `>_` Building from source

<details>
<summary>Expand source build instructions</summary>

The release package is `com.fadcam.lite`. Clone the main repository and build the `lite` flavor. For a specific branch or tag, add `--branch` with its name to the clone command.

```bash
git clone --depth 1 https://github.com/anonfaded/FadCam.git
cd FadCam
```

**Debug build** (installs alongside the stable app as `com.fadcam.lite.beta`):

```bash
./gradlew assembleLiteDebug     # build the APK
./gradlew installLiteDebug      # build + install on a connected device
```

**Release build** (`com.fadcam.lite`):

```bash
./gradlew assembleLiteRelease
```

**Where the APK lands**

```
app/build/outputs/apk/lite/debug/     FadCam_lite_v<version>-universal.apk
app/build/outputs/apk/lite/release/   FadCam_lite_v<version>-universal.apk
```

**Two things you need before a build succeeds**

1. **`local.properties` with a signing keystore.** Both build types are signed with the same key, and the build fails on purpose if it is missing, because a debug-signed APK could not replace an installed release:

   ```properties
   sdk.dir=/path/to/Android/sdk
   KEYSTORE_FILE=/path/to/keystore.jks
   KEYSTORE_PASSWORD=…
   KEY_ALIAS=…
   KEY_PASSWORD=…
   ```

   For a fork, generate your own with `keytool`. You do not need the upstream key.

2. **The patched Media3 composite build.** FadCam records through a custom Media3 fork (the Hybrid MP4 pipeline). Clone it next to this repo and point to it:

   ```bash
   git clone --depth 1 https://github.com/anonfaded/media3-patched.git /tmp/media3-patched
   ```

   or set `media3.patched.path=/your/path` in `local.properties`.

Builds target **JDK 17**.

</details>

## `>_` Support & Shop

**FadCam Lite Pro** (Notes, Calculator, Weather: three disguised apps with lifetime access) is being added to the shop in the next few days, before 2027. In the meantime, the shop carries the current FadCam Pro bundle.

Your purchases help fund development and maintenance.

[![Support me on Patreon](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Fshieldsio-patreon.vercel.app%2Fapi%3Fusername%3DFadedx%26type%3Dpatrons%26suffix%3Dpatrons%2520%257C%2520Shop&style=for-the-badge)](https://www.patreon.com/cw/Fadedx/shop)

## `>_` Community

You’re welcome to share feedback, suggest ideas, talk through issues, or drop in and say hi.

[![Discord](https://img.shields.io/discord/1263384048194027520?label=Join%20Us%20on%20Discord&logo=discord)](https://discord.gg/kvAZvdkuuN)

## `>_` Credits

- Recording engine, design and code shared with [FadCam](https://github.com/anonfaded/FadCam)
- Icons by [Icons8](https://icons8.com) and [Flaticon](https://www.flaticon.com/)
- Elapsed timer font: Doto by The Doto Project Authors
- Location reverse geocoding by [Nominatim](https://nominatim.org/) / [OpenStreetMap](https://www.openstreetmap.org/)

## `>_` License

GNU General Public License v3.0
