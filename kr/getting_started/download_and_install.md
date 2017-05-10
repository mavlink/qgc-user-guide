# 다운로드와 설치

## 다운로드

아래 링크에서 현재 QGroundControl의 안정버전을 다운받습니다.

* [Windows](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl-installer.exe)
* [OS X](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.dmg)
* Linux
  * [AppImage](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.AppImage)
  * [Compressed Archive](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.tar.bz2)
* [Android](https://play.google.com/store/apps/details?id=org.mavlink.qgroundcontrol)

기존 출시한 안정버전은 <a href="https://github.com/mavlink/qgroundcontrol/releases/" target="_blank">GitHub</a>에서 찾을 수 있습니다.

릴리즈 관련 정보는 [여기](../releases/release_notes.md)를 참고하세요.

## OS 요구사항

* 윈도우 비스타 이상
* Mac OSX 10.8 이상
* Ubuntu 14.04 이상
* Android 5.1 이상
* iOS 8.0 이상 (Beta)


## 설치

* 윈도우 : 인스톨러를 실행시키기 위해서 실행파일을 더블 클릭합니다.
* Mac : .dmg 파일을 더블 클릭하고 QGroundControl 어플리케이션을 Application 폴더로 끌어다 넣습니다.

## Linux에서 설치와 실행

### AppImage

```sh
chmod +x ./QGroundControl.AppImage
./QGroundControl.AppImage (or double click)
```

### Compressed Archive

github에 있는 <a class="urlextern" title="https://github.com/mavlink/qgroundcontrol" href="https://github.com/mavlink/qgroundcontrol" rel="nofollow">README</a>에 따라 추가 패키지가 필요할 수 있습니다. Qt를 설치할 필요는 없습니다.

```sh
tar jxf QGroundControl.tar.bz2
cd qgroundcontrol
./qgroundcontrol-start.sh
```

## Daily Builds

The daily build can be [downloaded from here](../releases/daily_builds.md).