## Tools
- [Emulator](https://developer.android.com/studio)
- [Root Devices](https://github.com/newbit1/rootAVD)
- [Trust User Certs](https://github.com/NVISOsecurity/MagiskTrustUserCerts)
- [X-Plore](https://www.apkmirror.com/apk/lonely-cat-games/x-plore-file-manager/x-plore-file-manager-4-32-00-release/x-plore-file-manager-4-32-00-android-apk-download/)

## Root `Device`
```bash
./rootAVD.sh ListAllAVDs
```

## Install `margisk`
```shell
./rootAVD.sh InstallApps
```

## Approve Terminal as `root`
```shell
adb shell su
```

## Verify files system editor install `X-Plore.apk` version 4.32.00

```shell
adb install "com.lonelycatgames.Xplore_4.32.00-43200_minAPI23(arm64-v8a,armeabi-v7a,x86,x86_64)(nodpi)_apkmirror.com.apk"
```