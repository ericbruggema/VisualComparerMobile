# Installation

[← Back to the overview](../README.md)

Visual Comparer Mobile is installed from an APK file that you download from this repository's [Releases](https://github.com/ericbruggema/VisualComparerMobile/releases) page. It is not published in the Play Store.

## Requirements

* **Android 11 (API 30) or newer.** A tablet is best; phones work too.
* About 50 MB for the app, plus some space for its cache (the fingerprints of your photos and videos).
* Photos and videos on the device or on an SD card. Cloud-only files that are not stored on the device cannot be analysed.

## Install the APK

1. **Download** `VisualComparerMobile-<version>.apk` from the [latest release](https://github.com/ericbruggema/VisualComparerMobile/releases/latest) on your device (open this page there), or download it on a computer and copy it over.
2. **Open the file.** Android asks you to allow installing apps from this source (your browser or file manager). Allow it for now; you can turn it off again afterwards (*Settings → Apps → Special app access → Install unknown apps*).
3. **Google Play Protect** may say it does not know the app, because it is not published in the Play Store. If you downloaded it from this page and the fingerprint matches (see below), choose to install anyway. If you are not sure, do not install it.
4. **Start the app.** Read and accept the terms. Allow access to photos and videos, and to notifications, so a long scan can show its progress.
5. Pick folders and scan. See [Getting started](getting-started.md).

## Permissions

| Permission | Why |
|---|---|
| **Photos and videos** (`READ_MEDIA_IMAGES`, `READ_MEDIA_VIDEO`; on Android 12 and older: storage) | To find and read your photos and videos so they can be compared. Nothing is uploaded. |
| **Notifications** | To show the progress of a long scan and to tell you when it is done. |
| **Foreground service (data sync), wake lock** | A long scan runs as a foreground service with a progress notification, so Android does not stop it when the screen turns off. |

The app has **no internet permission** at all: it cannot send anything anywhere. When you trash or delete files, Android itself asks for your permission each time. For folders on an SD card or in other storage, the app uses Android's folder picker; it only gets access to the folders you pick.

## Check your download

Every release has a file `SHA256SUMS.txt` with the SHA-256 fingerprint of the APK. If the fingerprint of your file is different, the file was damaged or changed: delete it and download again. On a computer, in PowerShell:

```powershell
Get-FileHash .\VisualComparerMobile-1.0.0.apk -Algorithm SHA256
```

### Check the signing certificate

The APK is signed with the author's own release key. The SHA-256 fingerprint of the signing certificate is:

```
ca54f2efd74c3ec3af7d14fb668d671f2b478c0b67490c305af83c255e352358
```

You can check it with `apksigner` from the Android SDK build tools:

```
apksigner verify --print-certs VisualComparerMobile-1.0.0.apk
```

Look at `Signer #1 certificate SHA-256 digest`. It has to be the value above, and it stays the same for every future version: Android refuses to install an update that is signed with a different key.

## Update

Download the new APK from the Releases page and open it; Android installs it over the old version and keeps your libraries, results and cache. The app never checks for updates by itself and never contacts any server.

## Remove

*Settings → Apps → Visual Comparer → Uninstall.* This also removes the app's data (libraries, saved results and the cache). Files in a quarantine folder that you placed outside the app (on the SD card, for example) stay where they are until you delete them; the **quarantine inside the app's own storage** is removed with the app, so empty or restore it first.

## Which version do I have?

Open the menu (⋮) → **About**. It shows the version and the limits of the free edition.
