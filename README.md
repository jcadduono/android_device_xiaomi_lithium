## TWRP device tree for Xiaomi Mi MIX (lithium)

Add to `.repo/local_manifests/lithium.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/xiaomi/lithium" name="android_device_xiaomi_lithium" remote="TeamWin" revision="android-6.0" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_lithium-eng
make -j5 recoveryimage
```

Kernel sources are available at: https://github.com/jcadduono/android_kernel_xiaomi_msm8996/tree/twrp-6.0
