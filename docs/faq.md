# FAQ and troubleshooting

[← Back to the overview](../README.md)

Short answers to the questions people ask most. Nothing here replaces looking at your files yourself before you delete them.

* [Using the app](#using-the-app)
* [The free edition](#the-free-edition)
* [Privacy and permissions](#privacy-and-permissions)
* [Problems](#problems)

## Using the app

**Where do I start?**
Open the app, accept the terms, tap **Start scan** (all photos and videos on the device are the default), then read the groups. [Getting started](getting-started.md) shows every step; the menu ⋮ → **Guide** opens a short introduction.

**Which files can it compare?**
What your own device can decode. Open **About → Check supported formats on this device** to see it. Many phones cannot open AVI, WMV, FLV, OGV or MPEG program streams. See [Supported formats](formats.md). For those, use the [Windows version](https://github.com/ericbruggema/VisualComparer).

**Why was a copy not found?**
Matching is based on the picture. Heavily edited, strongly cropped or very short copies can be missed, and the *Fast* video profile skips speed changes and short clips. Try a looser setting or the *Thorough* profile, or use *Compare again* on the results screen with another sensitivity (it does not scan again). See [Photos and videos](photos-and-videos.md#what-is-not-found-and-why).

**Why were two different files grouped?**
Look-alikes happen, especially with burst shots, screenshots of the same screen or loose settings. The match strength is shown for each copy. Look before you delete and use a stricter setting.

**The first scan takes long. Is that normal?**
Yes. Every photo and video is analysed once. Plug in your device and let it run; later scans only analyse new or changed files. You can set the app to scan only while charging.

**Can I leave the app during a scan?**
Yes. The scan runs as a foreground service with a progress notification that has a *Cancel* button. Android limits background work: on Android 15 such a service may run about six hours per day; the app then stops cleanly and asks you to open it again.

**How do I undo a clean-up?**
For quarantine: menu ⋮ → **Log** → *Undo*. Files in the system trash can be restored from the trash in the Files app or your gallery, as long as Android keeps them.

**Does it compare sound?**
No, only the picture.

**Can I scan my SD card or a cloud folder?**
The SD card is included by default (*Settings → What to scan → Include SD card*). Other storage can be added through Android's folder picker (**Add…**). Files that are only in the cloud and not on the device cannot be analysed.

## The free edition

**What are the limits?**
A scan processes up to **500 videos** and **2,500 photos**; each has its own limit. Everything else works without restrictions.

**What happens when I have more files?**
The scan runs on the first files in the order of your folders and the app tells you how many files were skipped. Scan fewer folders at once, or run the scan again on the remaining folders.

## Privacy and permissions

**What does the app send?**
Nothing. The app has no internet permission, so it cannot send anything. Your photos, videos, folder names and scan results stay on the device.

**Why does it ask for access to photos and videos?**
To find and read them so they can be compared. It only reads; trashing or deleting always goes through an Android confirmation dialog.

**Why notifications?**
To show the progress of a long scan, and to tell you when it is done.

## Problems

**Google Play Protect or Android warns about the app.**
The app is installed from a file instead of the Play Store, so Android does not know it. Check the fingerprint and the signing certificate as described in [Installation](installation.md#check-your-download); if they match, you can install anyway. If you are not sure, do not install it.

**"App not installed" or an update does not install.**
An update must be signed with the same key as the installed version. The certificate fingerprint of every release is the one in [Installation](installation.md#check-the-signing-certificate). If you installed a different build of the app before (for example a debug build), uninstall it first; your libraries and cache of that build are removed with it.

**The scan stops when I turn off the screen.**
Allow notifications (the scan runs as a foreground service) and, on some devices, exclude the app from battery optimisation (*Settings → Apps → Visual Comparer → Battery → Unrestricted*).

**A file type shows "Not on this device".**
See [Supported formats](formats.md#if-a-type-shows-not-on-this-device).

**Some files are listed as broken.**
They could not be read (damaged, empty, or a type your device cannot decode). Open **Broken videos** from the results screen to quarantine or trash them.

**The app is slow on my device.**
Speed depends on the device and the number of files. Videos are the slow part. Lower *Number of files analysed at the same time* for a cooler phone, scan while charging, and use *Fast* for a first rough check. Later scans are much faster because of the cache.

**Where can I report a bug or ask something?**
Use the [issue tracker](https://github.com/ericbruggema/VisualComparerMobile/issues) or the contact options on ericbruggema.nl. Please mention the version (About), your device and Android version, and what you did. There is no guaranteed support or response time.

---

Always keep a backup of photos and videos you cannot lose. You are responsible for what you delete.
