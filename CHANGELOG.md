# Changelog

All notable changes to Visual Comparer Mobile (Android). Downloads are on the [Releases](https://github.com/ericbruggema/VisualComparerMobile/releases) page.

## 1.0.0 (free edition), first public release

**Finding duplicates**
* Photos and videos in one scan and one result list, in separate groups.
* Photos: five strictness levels (byte-identical, identical, same picture, similar, loose), optional matching of rotated, mirrored and cropped copies, EXIF orientation applied.
* Videos: three accuracy profiles (fast, normal, thorough); finds re-encodes, other resolution or container, crops, black bars, rotation, mirroring, clips from a longer video, time shifts, speed changes, watermarks and burned-in subtitles.
* Scan modes: all vs all, A vs B, new vs library. Libraries with saved results and `.vcslib` import/export.
* Candidate index and fingerprint cache; later scans only analyse new or changed files.
* Uses the decoders of the device (no ffmpeg). **Check supported formats on this device** shows what can really be read.

**Results and comparing**
* The reason for every match, and for videos a bar on a shared timeline.
* Two-pane results and three-column review on tablets, one pane at a time on phones.
* Comparer: side by side, wipe slider, A/B flicker, difference heat map, linked zoom and pan, frame stepping, PSNR and SSIM.
* Compare again with another sensitivity without scanning.
* Export to CSV, JSON and HTML.

**Cleaning up safely**
* Quarantine (private storage or a folder you choose) and system trash, always with Android's own confirmation; undo log; protected reference folders; quick check before removing; never a whole group at once.

**Running scans**
* Foreground service with a progress notification and a cancel button; optional "only while charging".

**Privacy**
* No internet permission, no account, no telemetry.

**Free edition**
* Up to 500 videos and 2,500 photos per scan.
* Android 11 (API 30) or newer.
