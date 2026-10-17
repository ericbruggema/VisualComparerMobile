# Photos and videos

[← Back to the overview](../README.md)

How the app decides that two files are "the same": the photo strictness levels, the video accuracy profiles, what is found and what is not. The engine is the same as in [Visual Comparer for Windows](https://github.com/ericbruggema/VisualComparer/blob/main/docs/how-it-works.md); this page covers what matters on Android.

## The idea

A checksum or file size changes the moment a single pixel changes. A photo that was resized by a chat app, or a video that was converted for the phone, is a different **file** but the same **picture**. The app compares what the files *look like*: every photo is turned into a small greyscale picture and a short fingerprint of its light and dark areas (also for the picture turned by 90°, 180°, 270° and mirrored); a video is sampled every few seconds and each sample gets such a fingerprint. Fingerprints are stored in a local database (the cache), so an unchanged file is analysed only once. An index selects the candidate pairs, so the app does not compare every file with every other. Only the **picture** is compared, **not the sound**.

## Photos: how strict?

On the start screen (*How strict for photos*):

| Level | Finds |
|---|---|
| **Byte-identical** | Only files that are byte for byte the same. The fastest option. |
| **Identical** | The exact same photo, even if it is smaller, in another format, re-saved, rotated or mirrored. Not one that is slightly different. |
| **Same picture** *(default)* | Also light edits such as colour and brightness changes. |
| **Similar** | Look-alikes; follows the sensitivity setting. |
| **Loose** | Also burst shots and near-duplicates. Expect photos that are similar but not the same. |

Two switches: **Also rotated or mirrored** (on by default) and **Also cropped** (off by default: also finds a photo of which a piece was cut off, or that has a watermark or subtitles).

The photo's **EXIF orientation** is applied, so a portrait phone photo is compared the way you see it. Each copy shows why it matched: *smaller: 1200×900*, *other format: PNG*, *rotated 270°*, *mirrored*, *same picture*. The best copy is the one with the **highest resolution, then the largest file**.

If two different-looking photos end up in one group, use a stricter level and *Compare again* from the results screen.

## Videos: how accurate?

| Profile | A picture is taken | Use it for |
|---|---|---|
| **Fast** | about every 4 seconds | A first rough check. Can miss speed changes and very short clips. |
| **Normal** *(default)* | every 1 to 4 seconds, depending on the length | Daily use. |
| **Thorough** | every 0.5 to 2 seconds | Short clips and speed differences. The slowest. |

A higher **sensitivity** (*More options*) finds more, looser matches and more false ones; a lower value is stricter.

## What is found

| Change | Photos | Videos |
|---|:---:|:---:|
| Exact copy | ✓ | ✓ |
| Resized, recompressed, other format or container | ✓ | ✓ |
| Rotated or mirrored | ✓ | ✓ |
| Light edits (colour, brightness) | ✓ (*Same picture* or looser) | ✓ |
| Mildly cropped; black bars | ✓ (*Also cropped*) | ✓ |
| A clip from a longer video, another intro | – | ✓ |
| Another speed (for example 24 ↔ 25 fps) | – | ✓ (Normal or Thorough) |
| Watermark or burned-in subtitles | – | ✓ |
| Strongly cropped, heavily edited, collages | usually not | usually not |

A clip appears in the group of the longer video with a shorter bar, so you can see it is only part of it.

## What is not found, and why

* **Very short clips** (a few seconds) can be missed by *Fast*.
* **Heavily edited** pictures are different pictures for the app.
* **Files your device cannot decode** cannot be analysed at all (see [Supported formats](formats.md)).
* **Sound is ignored.**
* **Look-alikes** (burst shots, screenshots of the same screen) can be grouped, especially at *Similar* and *Loose*.
* A match percentage is an **indication**, not proof. Always look before you delete.

## How long does it take?

* The first scan analyses every file once. On a phone this is slower than on a PC and uses power: plug in the device. Photos are decoded at a reduced size and are quick; videos are the slow part.
* Later scans only analyse new or changed files and are much faster.
* The number of files analysed at the same time is *Automatic* and adapts to your device; *Settings → What to scan* lets you lower it for a cooler phone.
* Android has no CUDA/GPU alignment; the comparing runs on the processor. The *Compare resolution* setting limits memory use for long videos.

## The free edition

A scan processes up to **500 videos** and **2,500 photos**, each with its own limit. If more are found, the first files (in the order of your folders) are scanned and the app tells you how many were skipped.
