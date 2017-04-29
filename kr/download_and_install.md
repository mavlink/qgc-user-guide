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

릴리즈 관련 정보는 [여기](ReleaseNotes.md)를 참고하세요.

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

QGroundControl의 데일리 빌드도 사용이 가능합니다. 아래 빌드들은 안정 빌드보다 많은 테스트를 진행하지는 못했지만 최신 [새로운 기능들](DailyBuildChanges/DailyBuildNewFeatures.md)을 가지고 있습니다. 사용시 위험할 수 있다는 것을 명심하세요!

* [Windows](https://s3-us-west-2.amazonaws.com/qgroundcontrol/builds/master/QGroundControl-installer.exe)
* [OS X](https://s3-us-west-2.amazonaws.com/qgroundcontrol/builds/master/QGroundControl.dmg)
* Linux
  * [AppImage](https://s3-us-west-2.amazonaws.com/qgroundcontrol/builds/master/QGroundControl.AppImage)
  * [Compressed Archive](https://s3-us-west-2.amazonaws.com/qgroundcontrol/builds/master/QGroundControl.tar.bz2)
* [Android](https://play.google.com/store/apps/details?id=org.mavlink.qgroundcontrolbeta&rdid=org.mavlink.qgroundcontrolbeta)

### Android daily builds

구글 플레이 스토어에 안드로이드 데일리 빌드 버전을 받을 수 있습니다. 기존 베타 테스트는 더 이상 지원하지 않습니다. 만약 기존에 멤버였다면 [멤버 탈퇴](https://play.google.com/apps/testing/org.mavlink.qgroundcontrol)를 하도록 합니다.


### Test Flight 사용해서 iOS Beta 설치

QGroundControl의 iOS 버전은 현재 오픈 베타입니다. 여러분의 이메일 주소를 [여기](https://github.com/mavlink/qgroundcontrol/issues/3509)에 추가하면 베타 버전을 받을 수 있습니다. WiFi 연결을 지원하는 iOS 장치에서만 가능하다는 점을 명심하세요. 일단 설치되면 Test Flight app을 통해서 새로운 버전의 알림을 받을 수 있습니다. iOS 베타 빌드의 릴리즈 주기는 매주 혹은 격주라기 보다는 그때그때 일어납니다.
