# Settings

[← Back to the overview](../README.md)

Open **Settings** from the menu ⋮ on the start or results screen. On a tablet the settings are shown in two columns. Changes apply immediately.

<p align="center"><img src="images/android-settings.png" alt="Settings" width="260"></p>

## Libraries

A **library** keeps a set of folders together with its mode, accuracy, sensitivity and saved results. Use one per purpose, for example *Family photos* or *Download folder*. The active library is shown at the top of the start screen; the menu ⋮ → **Libraries** manages them:

* create, rename, duplicate and delete libraries,
* **export and import** a library as a `.vcslib` file (through Android's file picker),
* compare two libraries with each other,
* see the last scan and the space you could free per library.

Results are saved per library and come back when you reopen the app.

## Appearance

* **Theme**: automatic (follows the device), light or dark.
* **Language**: automatic (device language), English, Dutch or German. The language changes immediately.

## What to scan

| Setting | What it does |
|---|---|
| **Include subfolders** | Search folders recursively (on by default). |
| **Include SD card** | Also search the SD card (on by default). |
| **Number of files analysed at the same time** | *Automatic* adapts to your device. Fewer at a time means a cooler phone and a longer scan. |
| **Ignore files smaller than … MB and shorter than … seconds** | Filters for **videos**. Photos are always searched. |
| **File types / Photo file types** | The extensions that are searched, separated by commas. |
| **Exclusion patterns** | One per line; `*` and `?` are wildcards, for example `*/.thumbnails/*`, `*.part`, `*.tmp`, `*/.trash*/*`. |

## What to keep?

The criteria that choose the best file of a group, applied from top to bottom; tick what counts and move them with the arrows: highest resolution, longest duration, highest bitrate, preferred folder wins, newest file, oldest file, preferred codec. You also set your **preferred folders** (the first wins) and **preferred codecs** (for example `h264, hevc, av1, vp9`).

## Safety

| Setting | What it does |
|---|---|
| **Protected reference folders** | Files in them are never removed and count as the original. |
| **Quarantine folder** | *App storage (private)* by default. Choose a folder on the SD card or in cloud storage to keep quarantined files outside the app (so they survive uninstalling it). Only quarantined files can be restored by the app's undo. |
| **Extended check before deleting** | Reads and compares both files again just before they are removed (slow). The quick check (the files still exist and are unchanged) is always done. |

## Accuracy

Videos are always read over their full length. When two videos are aligned, the number of points compared per video is limited to keep memory in check. **Automatic** adapts to the memory and processor of your device; you can set the **compare resolution** yourself, with a note about the memory your device has available. A warning appears if the number may exceed the memory available to the app; lower it or use fewer parallel files.

## Thumbnails

The **size of the thumbnails** in the timeline and the **number of thumbnails per video**.

## Battery

* **Only scan while charging**: a scan waits until the charger is connected.
* A first scan of many files takes a while and uses a lot of power. Plug in the device and let it run; the next scan reuses everything already analysed.

## Cache

Fingerprints of previously scanned files are reused, so the next scan of the same files is much faster. This card shows how much is stored and has **Clear cache**, which erases all stored fingerprints and posters (files are analysed again on the next scan).

## About

Shows the version, the limits of the free edition, the **Terms of use**, the third-party components, and **Check supported formats on this device** (see [Supported formats](formats.md)).
