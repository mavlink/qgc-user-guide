# Download and Install

## Downloading

The links below will download the current Stable releases of QGroundControl.

* [Windows](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl-installer.exe)
* [OS X](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.dmg)
* Linux
  * [AppImage](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.AppImage)
  * [Compressed Archive](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.tar.bz2)
* [Android](https://play.google.com/store/apps/details?id=org.mavlink.qgroundcontrol)

Previous stable releases can be found on <a href="https://github.com/mavlink/qgroundcontrol/releases/" target="_blank">GitHub</a>. 

Release notes are [here](../releases/release_notes.md).

## OS Requirements

* Windows Vista or above
* Mac OSX 10.8 or above
* Ubuntu 14.04 LTS or above
* Android 5.1 or above
* iOS 8.0 or above (Beta)


## Installing

* Windows: Double click the executable to launch the installer.
* Mac: Double click the .dmg file to mount it, then drag the QGroundControl application to your Application folder.

## Installing and Running on Linux

### AppImage

```sh
chmod +x ./QGroundControl.AppImage
./QGroundControl.AppImage (or double click)
```

### Compressed Archive

You will also need to install additional packages as specified in the github <a class="urlextern" title="https://github.com/mavlink/qgroundcontrol" href="https://github.com/mavlink/qgroundcontrol" rel="nofollow">README</a>. You do not need to install Qt.

```sh
tar jxf QGroundControl.tar.bz2
cd qgroundcontrol
./qgroundcontrol-start.sh
```

## Daily Builds

The daily build can be [downloaded from here](../releases/daily_builds.md).