# Supported formats

[← Back to the overview](../README.md)

Android has no ffmpeg. Visual Comparer Mobile therefore uses the **decoders of your own device**, and these differ per phone, per tablet and per Android version. That is why the app tests it for you.

## Check what your device can read

Open the menu ⋮ → **About** and tap **Check supported formats on this device**. The app:

1. tries a small sample file of **every file type** it looks for (a tiny real video or photo of that type that ships with the app),
2. asks the system which **video codecs** the device decodes, and whether it does so in **hardware**,
3. shows the result: *Works* or *Not on this device* for every type.

<p align="center"><img src="images/android-formats.png" alt="The format check on a device" width="280"></p>

The screenshot shows an emulator; a real phone or tablet gives its own answer.

## What the app looks for

* **Video file types**: MP4, M4V, MOV, 3GP, MKV, WebM, TS, M2TS, MTS, MPG, MPEG, VOB, AVI, DIVX, WMV, FLV and OGV
* **Video codecs**: H.264, H.265 (HEVC), VP9, VP8, AV1, MPEG-4, H.263 and MPEG-2
* **Photo types**: JPEG, PNG, WebP, GIF, BMP, TIFF, HEIC, HEIF and AVIF

You can change the list of extensions per scan in *Settings → What to scan*.

## What this means in practice

* **MP4, M4V, MOV, 3GP, MKV, WebM and TS** with H.264, H.265, VP9 or AV1 are read on most modern devices (AV1 and HEVC depend on the device).
* **Many phones and tablets cannot open AVI, WMV, FLV, OGV or MPEG program streams** (MPG, MPEG, VOB). Files of those types cannot be compared on the device; use the **[Windows version](https://github.com/ericbruggema/VisualComparer)** for them, which reads them with ffmpeg.
* **HEIC, HEIF and AVIF** photos depend on the Android version and the device.
* **RAW camera files** are not supported.
* A file that cannot be decoded is listed under **Broken videos** instead of failing the scan.
* Animated GIFs are compared by their first frame; the EXIF orientation of photos is applied.

## If a type shows "Not on this device"

* Update Android and the system apps (some codecs arrive through system updates).
* Convert the files to a common type (for example MP4 with H.264) on a computer.
* Or scan that folder with the Windows version.

Both versions compare the same way; only the list of readable formats differs.
