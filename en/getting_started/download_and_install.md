# Download and Install

The sections below can be used download the [current stable release](../releases/release_notes.md) of *QGroundControl* for each platform.

## Windows

Install *QGroundControl* for Windows Vista or later:

1. Download [QGroundControl-installer.exe](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl-installer.exe).
1. Double click the executable to launch the installer.


## Mac OS X

Install *QGroundControl* for Mac OS X 10.8 or later: 

1. Download [QGroundControl.dmg](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.dmg).
1. Double-click the .dmg file to mount it, then drag the QGroundControl application to your Application folder.

  
## Ubuntu Linux

Install *QGroundControl* for Ubuntu Linux 14.04 LTS or later. You can either install the AppImage **or** the compressed archive.

### AppImage

1. Download [QGroundControl.AppImage](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.AppImage).
1. Install using the terminal commands:
   ```sh
   chmod +x ./QGroundControl.AppImage
   ./QGroundControl.AppImage  (or double click)
   ```

### Compressed Archive

1. Download [QGroundControl.tar.bz2](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.tar.bz2).
1. Extract the archive using the terminal command:
   ```sh
   tar jxf QGroundControl.tar.bz2
   cd qgroundcontrol
   ./qgroundcontrol-start.sh
   ```
1. Install additional packages as specified in the github <a class="urlextern" title="https://github.com/mavlink/qgroundcontrol" href="https://github.com/mavlink/qgroundcontrol" rel="nofollow">README</a>. You do not need to install Qt.

  
## Android

Install *QGroundControl* for Android 5.1 or later:

1. Open the Google Play Store [QGroundControl link](https://play.google.com/store/apps/details?id=org.mavlink.qgroundcontrol).
1. Follow the installation instructions.


## iOS

> **Note** *QGroundControl* for iOS is in beta. It can only be installed as a [daily build](../releases/daily_builds.md#installing-ios-beta-using-test-flight).

Install *QGroundControl* for iOS 8.0 or later:  

1. Follow the instructions for [Installing iOS Daily Beta using Test Flight](../releases/daily_builds.md#installing-ios-beta-using-test-flight).


## Old Stable Releases

Old stable releases can be found on <a href="https://github.com/mavlink/qgroundcontrol/releases/" target="_blank">GitHub</a>. 

## Daily Builds

Daily builds can be [downloaded from here](../releases/daily_builds.md).
