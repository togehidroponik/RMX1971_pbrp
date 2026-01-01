# android_device_realme_RMX1971
For building Pitchblack Recovery for Realme 5 Pro

Pitchblack tree for Realme 5 Pro

## Features

Works:

- Everything

## Compile

First checkout manifest :

```
repo init --depth=1 -u https://gitlab.com/Pitchblack/Manifest.git -b pbrp_9.0
repo sync
```

Then add these projects to .repo/manifest.xml:

```xml
<project path="device/realme/RMX1971" name="device/RMX1971" remote="gitlab" revision="master" />
```

Finally execute these:

```
. build/envsetup.sh
lunch omni_RMX1971-eng
mka recoveryimage ALLOW_MISSING_DEPENDENCIES=true
```

To test it:

```
fastboot flash /path/to/recovery.img
and then
Flash the zip through the recovery for addon support.
```


## Thanks

- Thanks to @mauronfrio and @MadhavSaladi
