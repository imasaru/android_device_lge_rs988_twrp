## TWRP device tree for LG G5 (US Carrier-Unlocked RS988)

Add to `.repo/local_manifests/rs988.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/lge/rs988" name="android_device_lge_rs988" remote="TeamWin" revision="android-8.1" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_rs988-eng
make -j5 recoveryimage
```

Kernel sources are available at: https://github.com/LineageOS/android_kernel_lge_msm8996

