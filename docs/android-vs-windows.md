# Android compared with Windows

[← Back to the overview](../README.md)

Visual Comparer exists for two platforms. The matching engine is the same (the Android version is a port of the Windows one), so a photo or video that is found on one is found on the other. They differ in what the platform offers.

* 🖥️ **[Visual Comparer for Windows](https://github.com/ericbruggema/VisualComparer)**: installer or portable zip, ffmpeg for every format.
* 📱 **Visual Comparer Mobile** (this repository): an APK for Android 11 and newer.

| Feature | Windows | Android |
|---|:---:|:---:|
| Duplicate photos and videos in one scan | ✓ | ✓ |
| Photo strictness levels (5), rotated/mirrored and cropped matching | ✓ | ✓ |
| Video accuracy profiles (fast, normal, thorough) | ✓ | ✓ |
| Scan modes: all vs all, A vs B, new vs library | ✓ | ✓ |
| Libraries with saved results, `.vcslib` export/import | ✓ | ✓ |
| Match bars on a shared timeline | ✓ | ✓ |
| Side by side, wipe slider, flicker, difference view | ✓ | ✓ |
| PSNR and SSIM | ✓ | ✓ |
| VMAF score | ✓ | not on Android |
| NVIDIA CUDA decoding and GPU alignment | ✓ optional | not on Android |
| Quarantine and undo log | ✓ | ✓ |
| Delete | Recycle Bin or permanent | Trash, with system consent each time |
| Export CSV / JSON / HTML | ✓ | ✓ |
| Supported formats | everything the bundled ffmpeg reads | what your device can decode, tested in the app |
| Keyboard shortcuts | ✓ | touch gestures |
| Languages | English, Dutch, German | English, Dutch, German |
| Installation | installer or portable zip | APK from the Releases page |
| Free edition limit per scan | 500 videos, 2,500 photos | 500 videos, 2,500 photos |
| Internet access | none | none (no internet permission) |

## Which one should I use?

* **Photos and videos on your phone or tablet**, and you want to clean up without a computer: the Android app.
* **Large archives, rare formats (AVI, WMV, FLV, MPEG), a NAS or backup drives**: the Windows version. It has a bigger screen, more memory and ffmpeg.
* **Both**: scan the phone backup on your PC and keep the phone itself light. Settings and libraries are not shared between the two; they are separate programs with separate data.
