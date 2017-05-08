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

Daily Builds of QGroundControl are also available for use. These builds have less testing than Stable builds but will have the absolute latest set of [new features](../releases/daily_build_new_features.md) available. Use at your own risk!

* [Windows](https://s3-us-west-2.amazonaws.com/qgroundcontrol/builds/master/QGroundControl-installer.exe)
* [OS X](https://s3-us-west-2.amazonaws.com/qgroundcontrol/builds/master/QGroundControl.dmg)
* Linux
  * [AppImage](https://s3-us-west-2.amazonaws.com/qgroundcontrol/builds/master/QGroundControl.AppImage)
  * [Compressed Archive](https://s3-us-west-2.amazonaws.com/qgroundcontrol/builds/master/QGroundControl.tar.bz2)
* [Android](https://play.google.com/store/apps/details?id=org.mavlink.qgroundcontrolbeta&rdid=org.mavlink.qgroundcontrolbeta)

### Android daily builds

Daily builds for Android now have there own Google Play store entry. The old opt-in beta test is no longer valid. If you were a member of that you should [opt-out](https://play.google.com/apps/testing/org.mavlink.qgroundcontrol).


### Installing iOS Beta using Test Flight

The iOS version of QGroundControl is currently in open Beta. You can opt-in to the Beta by adding your email address [here](https://github.com/mavlink/qgroundcontrol/issues/3509). Keep in mind that due to device restrictions on iOS only WiFi connections are supported. Once installed you will be notified of new versions through the Test Flight app. The release frequency of iOS beta builds is on an ad-hoc basis more on the order of a new build every week or two.

