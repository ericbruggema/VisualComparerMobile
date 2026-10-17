# Getting started

[← Back to the overview](../README.md)

Your first scan on a phone or tablet. Four steps: **pick folders, scan, read the results, clean up.**

## Before you begin

* Install the app, see [Installation](installation.md).
* The first time you start it you read and accept the terms of use. A short guide follows (you can open it again from the menu ⋮ → **Guide**).
* Try it on a small folder first. The free edition handles up to 500 videos and 2,500 photos per scan.

## 1 · Start: pick what to scan

<p align="center"><img src="images/android-start.png" alt="The start screen" width="260"></p>

At the top you see the active **library** (a set of folders with its own settings and results; see [Settings](settings.md#libraries)). The ⋮ menu holds *Settings, Libraries, Log, Guide* and *About*.

1. **What to compare**
   * **All vs all**: find duplicates within all chosen folders.
   * **A vs B**: only copies between two sets (handy to check an old backup against a new one).
   * **New vs library**: check new files against everything you scanned before.
2. **Folders**: *All videos and photos on this device* is the default. Tap **Add…** to pick specific folders (your camera folder, *Download*, WhatsApp, an SD card, a cloud folder through Android's folder picker). Remove one with ✕.
3. **What to look for**: *Videos and photos*, *Videos only* or *Photos only*.
4. **How strict for photos**: five levels, from *Identical* to *Loose*, plus *Also rotated or mirrored* and *Also cropped*. *Same picture* is a good start. See [Photos and videos](photos-and-videos.md).
5. **How accurate for videos**: *Fast*, *Normal* or *Thorough*. Under **More options** you find the sensitivity.

Tap **Start scan**. The app asks for access to photos and videos (and for notifications) the first time.

## 2 · Scan: watch it work

You see each phase live: **Find › Analyse › Candidates › Compare › Group**, with the number of files found, how many come from the cache, how many are new, the speed and the time left. You can leave the app: a scan runs as a foreground service with a progress notification that has a *Cancel* button. What is analysed stays in the cache, so cancelling is never a waste.

* A first scan of many files takes a while and uses a lot of power. **Plug in your device** and let it run; the next scan reuses everything already analysed. You can set the app to scan only while charging (*Settings → Battery*).
* Android limits how long a background scan may run (on Android 15, about six hours per day for this kind of service). If the limit is reached the app stops cleanly and tells you to open it again to continue.

## 3 · Results: read the groups

On a **phone** you see the list of groups; tap a group to open it. On a **tablet** the list is on the left and the selected group on the right.

<p align="center">
  <img src="images/android-photo-group.png" alt="A photo group" width="260">
  <img src="images/android-results-landscape.png" alt="Two-pane results on a tablet" width="560">
</p>

* Each group is one photo or video in several versions. Each copy has **Keep / Remove** buttons, its properties and the reason it matched ("smaller", "other format", "rotated 270°", "same picture"…). The best version is marked and kept by default.
* **Photo groups** show the photos large next to each other; **video groups** have a **bar on a shared timeline** that shows which part of each copy matches the best version. **Tap or drag a bar** and every copy jumps to the same scene.
* Above the list: a search box, a filter *All / Photos / Videos* and a sort (largest first, name).
* **Check duplicates** marks everything except the best in every group; **Uncheck all** clears the marks.

### Look closer

* Tap two copies to **compare** them: side by side, wipe slider, A/B flicker, difference heat map, with linked zoom and pan; for videos also frame stepping and PSNR/SSIM. Photos have their own comparer with rotate and mirror for B.
* Use **Full screen review** to walk through the groups one by one: swipe or tap to keep or remove.

<p align="center">
  <img src="images/android-review.png" alt="Review" width="260">
  <img src="images/android-video-compare.png" alt="Video comparer" width="260">
  <img src="images/android-photo-compare.png" alt="Photo comparer" width="260">
</p>

More in [Results and clean-up](results-and-cleanup.md).

## 4 · Clean up safely

1. Mark what you want to remove (**Check duplicates**, or tap *Remove* per copy).
2. Tap **Quarantine** (recommended first) or **Move to trash**.
3. Android shows its own confirmation dialog; confirm it. The app never deletes anything without the system asking you.
4. Afterwards you see how many files were moved and how much space you freed. The **Log** (menu ⋮) lets you undo.

A whole group is never removed at once, and protected folders are never touched.

> ⚠️ You decide what is removed and you are responsible for it. Look at a group before you delete. Keep a backup of everything you cannot afford to lose.

## What next?

* Check what your device can read: **About → Check supported formats on this device** ([Supported formats](formats.md)).
* Change the sensitivity afterwards without scanning again: on the results screen choose *Compare again* ([Results and clean-up](results-and-cleanup.md#compare-again-with-another-sensitivity)).
* Not sure why something was or was not found? See [Photos and videos](photos-and-videos.md) and the [FAQ](faq.md).
