# 배포 요약

*QGroundControl*의 지금까지의 배포판들의 정보들을 설명합니다.

> **Note** 안정적인 빌드 메이저 및 마이너 번호는 다음과 같습니다. *패치* 배포 번호는 표시되어 있지 않으나, [Github 배포 페이지](https://github.com/mavlink/qgroundcontrol/releases)에서 나와 있습니다.

## 안정 버전 4.0(현재)

> **Note** QGroundControl의 설정 형식은 이번 배포판에서 변경되었습니다. 즉, 모든 QGroundControl의 설정이 기본값으로 재설정됩니다.

* 설정 
  * 언어: 언어 선택 허용
  * 접근성 향상을 위한 원격 측정 데이터의 선택적 [CSV 로깅](../SettingsView/csv.md).
  * ArduPilot 
    * Mavlink: 가능한 스트리밍 속도 설정
* 설정 
  * 조이스틱 
    * 새로운 조이스틱 설정 UI
    * 보류 버튼을 단일 또는 반복 작업으로 설정하는 기능
  * ArduPilot 
    * 모터 테스트
    * ArduSub 
      * 자동 모터 방향 감지
* 계획 
  * 전체 계획을 완료 마법사를 사용하여 템플릿에서 계획을 생성.
  * 설문조사: 자주 사용하는 설정을 사전 설정으로 저장
  * 다각형 편집 
    * 새로운 편집 도구 UI
    * 지도 위치에서 폴리곤 추적 지원
  * ArduPilot 
    * 최신 펌웨어 및 mavlink v2를 사용하여 GeoFence 및 Rally Points 지원
* 비행 
  * 클릭하여 ROI 지원
  * ADSB SBS 서버에 연결하기 위한 지원이 추가되었습니다. 예를 들어 'dump1090 --net'을 실행하는 USB SDR 동글의 ADSB 데이터에 대한 지원을 추가합니다.
  * 나침반에서 집으로 향하는 방향, COG 및 다음 웨이포인트 방향 표시기를 켤 수 있는 기능.
  * 비디오 
    * h.265 비디오 스트림 지원 추가
    * 비행 데이터가 포함된 [동영상 오버레이](../FlyView/VideoOverlay.md)를 현지에서 녹화된 동영상의 자막으로 자동 추가
  * 차량 유형별 비행 전 체크리스트. 설정에서 켜기
* 분석 
  * 차트 지원을 포함하는 새로운 Mavlink 탐색기. Android 및 iOS를 포함한 모든 빌드에서 지원됩니다.
* 일반 
  * 릴리스된 Windows 빌드는 이제 64비트 전용입니다.
  * 로그 재생: 재생 속도 지정 기능
  * ArduPilot 
    * 플래싱 및 자동 연결과 관련하여 chibios 펌웨어 및 ArduPilot 부트로더에 대한 지원이 향상되었습니다.

일부 기능들에 대한 자세한 내용은 [v4.0](../releases/stable_v4.0_additional.md)을 참고하십시오.

## 안정 버전 3.5

이 섹션에는 버전 3.5에서 *QGroundControl*에 추가된 새 기능의 상위 수준 및 *전체* 목록이 포함되어 있습니다.

* **전체** 
  * QGC에 Airmap 통합을 추가하였습니다. OSX 빌드 전용.
  * 범프 설정 버전(현재 8). 이렇게 하면 모든 설정들이 기본값으로 재설정됩니다.
  * 중국어, 터키어 및 부분적인 독일어 번역이 추가되었습니다. 
  * Taisync 2.4GHz ViUlinx 디지털 HD 무선 네트웍 지원이 추가되었습니다.
  * 여러 구성 요소에서 매개변수 로드를 수정합니다. 이것은 특히 WiFi 연결에 큰 변화가 일어났습니다.
  * **ArduPilot** ChibiOS 펌웨어 연결 및 플래시 지원.
* **설정** 
  * **RTK** 설정/일반에서 고정 RTK 기반 스테이션 위치 지정에 대한 지원을 추가합니다.
  * **GCS 위치** 
    * NMEA GPS 장치용 UDP 포트 옵션이 추가되었습니다.
    * 사용 가능한 경우 GCS 방향 표시
* **계획** 
  * **폴리곤** SHP 파일에서 폴리곤 불러오기를 지원합니다.
  * **고정익 착륙 패턴** 정지 사진 및 동영상 지원이 추가되었습니다. RTL을 수행하면 카메라가 중지되도록 기본값은 켜짐입니다.
  * **위치 편집 대화상자** 폴리곤 정점에서 사용할 수 있습니다.
* **비행** 
  * **카메라 페이지** 새로운 MAVLink 카메라 메시지에 대한 지원이 업데이트되었습니다. 카메라 선택, 카메라 모드, 사진/동영상 시작/중지, 스토리지 관리 등등 
  * **궤도** 회전 방향 변경 지원.
  * **계기판** 
    * 새로운 estimatorStatus Vehicle FactGroup에 ESTIMATOR_STATUS 값을 추가하였습니다. 이제 계기판에 표시할 수 있습니다.
    * 계기판에서 표시할 수 있도록 GCS까지의 거리를 설정합니다.
    * 기준점 방향을 계기판에서 표시할 수 있도록 합니다.

## 안정 버전 3.4

이 섹션에는 버전 3.4에서 *QGroundControl*에 추가된 새 기능의 상위 수준 및 *전체* 목록이 포함되어 있습니다. 각 안정적인 릴리스에서 다수의 버그들이 수정되었습니다.

* **설정** 
  * **오프라인 지도** 
    * Center Tool을 사용하면 위도/경도 또는 UTM 좌표로 지도 위치를 지정할 수 있습니다. 생성하는 오프라인 지도 영역을 편리하게 수정할 수 있습니다.
    * 오프라인 사용을 위해 지형 높이를 미리 다운로드합니다.
  * **Help** QGC 사용자 가이드 및 포럼에 대한 링크를 제공합니다.
* **설정** 
  * **펌웨어** PX4 또는 ArduPilot Flow 펌웨어를 플래시하는 기능. 
  * PX4 프로 펌웨어 
    * **비행 모드** 사용 가능한 모든 송신기 스위치에 대한 채널을 지정합니다.
    * **튜닝: 고급** 차량 PID 튜닝 지원의 초기 구현. 이것은 3.5 일일 빌드에서 수정중인 개선 사항입니다.
  * ArduPilot 펌웨어 
    * **전원/안전** 새로운 다중 배터리 설정을 지원합니다.
    * **Trad Heli** 새로운 설정 페이지.
* **계획** 
  * **파일 로드/저장** 표준 파일 로드/저장/다른 이름으로 저장 사용자 모델과 일치하는 계획 파일 로드를 위한 새 모델입니다.
  * **KML 로드** 동기화 메뉴에서 직접 KML 파일을 로드하는 기능. 필요한 경우 KML에서 생성하려는 패턴 유형을 묻는 메시지가 표시됩니다.
  * **탐사** 불규칙한 모양의 다각형에 대한 지원이 개선되었습니다.
  * **[복도 스캔](../PlanView/pattern_corridor_scan.md)** - 폴리라인 형태의 비행 패턴을 생성합니다. 예를 들어, 도로 조사에 사용할 수 있습니다.
  * **[고정익 착륙 패턴](../PlanView/pattern_fixed_wing_landing.md)** 
    * 평면도에 시각적으로 표시되는 착륙 영역.
    * 착륙 위치/방향은 차량 위치/방향에서 복사할 수 있습니다.
  * **지형** 
    * 미션 아이템의 높이는 지형 위의 높이로 지정할 수 있습니다.
    * 측량 및 복도 스캔은 지형을 따라 비행 계획을 생성할 수 있습니다. **Note** 이 기능은 [ArduPilot 지형 추적](http://ardupilot.org/copter/docs/common-terrain-following.html) 기능을 지원하지 않습니다. 
  * **위치 편집** 차량 위치에서 항목 위치를 설정합니다. 
* **비행** 
  * **비행 전 체크리스트** 설정에서 이 기능을 켤 수 있습니다. 비행 전에 따라야 할 일반적인 체크리스트를 제공합니다. 3.5 일일 빌드에서 더 많은 기능이 제공할 예정입니다.
  * **계기판** 
    * 많은 새로운 값을 표시할 수 있습니다.
    * 많은 새로운 값을 표시할 수 있습니다. 새로운 MavLink 카메라 사양을 지원하는 카메라가 필요합니다.
  * **ArduPlane** QuadPlane 지원을 포함하여 안내 명령에 대한 지원이 향상되었습니다.
  * **높은 대기 시간 링크** 위성 연결과 같은 대기 시간이 긴 링크를 지원합니다. 비용을 줄이기 위하여 이러한 링크에서 QGroundControl에서 기체 트래픽을 제한합니다. HIGH_LATENCY MavLink 메시지를 지원합니다. 듀얼 링크 설정으로, 높은 대기 시간에서 일반 링크로의 장애 복구를 지원합니다.

## 안정 버전 3.3

> **Tip** 버전 3.3에 대한 자세한 출시 정보는 [여기](../releases/stable_v3.3_long.md)에서 확인할 수 있습니다.

이 섹션에는 버전 3.3에서 *QGroundControl*에 추가된 새 기능의 상위 수준 및 *전체* 목록이 포함되어 있습니다. 각 안정적인 릴리스에서 다수의 버그들이 수정되었습니다.

* **설정** 
  * 로컬 NMEA GPS 장치 지원.
  * 비디오 녹화 설정을 저장합니다.
* **설정** 
  * **Parameter Editor** - Searching updates as you type characters for near immediate response to searches.
  * **Joystick** - Android joystick support.
* **계획** 
  * **새로운 기능 - 구조 스캔 패턴** - 수직 표면(다각형 또는 원형) 위의 이미지를 캡처하는 다층 비행 패턴을 생성합니다. 3D 모델 생성 또는 수직 표면 검사에 사용됩니다.
  * **고정익 착륙 패턴** - 거리 또는 활공 경사 낙하율로 배회지에서 착륙 지점까지의 거리를 조정할 수 있습니다.
  * PX4 GeoFence 및 Rally Point 지원.
  * 낮은 임무 항목 고도 표시의 지형 고도 표시
* **비행** 
  * 비디오 녹화를 시작/중지합니다.
  * 여러 기체에 연결된 경우 기체 아이콘이 더 잘 표시됩니다.
  * 다중 기체 보기는 모든 기체에 적용되는 명령을 지원합니다.
  * ADS-B 센서에서 보고된 기체를 표시합니다.
* **분석** 
  * **Mavlink 콘솔** - Mavlink 콘솔과의 통신을 위한 새로운 지원.
  * **로그 다운로드** - 메뉴에서 분석 보기로 이동하였습니다.

## 안정 버전 3.2

> **Tip** 버전 3.2에 대한 자세한 출시 정보는 [여기](../releases/stable_v3.2_long.md)에서 확인할 수 있습니다.

이 섹션에는 버전 3.2에서 *QGroundControl*에 추가된 새 기능의 상위 수준 및 *전체* 목록이 포함되어 있습니다.

* **설정**
  
  * **파일 저장 경로** - QGroundControl에서 사용하는 모든 파일의 저장 경로를 지정합니다.
  * **원격 측정 로그 자동 저장** - 이제 원격 측정 로그를 묻지 않고, 자동으로 저장합니다.
  * **계획 자동 로드** - 기체 최조 연실시 미션을 자동으로 로드합니다.
  * **RTK GPS** - 정확도와 최소 관찰 기간으로 측량을 지정합니다.

* **설정**
  
  * ArduPilot 전용 
    * **비행 전 기압계 및 속도 보정** - 이제 지원됨
    * **Copy RC Trims** - Now supported

* **Plan View**
  
  * **Plan files** - Missions are now saved as .plan files which include the mission, geo-fence and rally points.
  * **Plan Toolbar** - New toolbar which shows you mission statistics and Upload button.
  * **Mission Start** - Allows you to specify values such as flight speed and camera settings to start the mission with.
  * **New Waypoint features** - Adjust heading and flight speed for each waypoint as well as camera settings.
  * **Visual Gimbal direction** - Gimbal direction is shown on waypoint indicators.
  * **Pattern tool** - Allows you to add complex patterns to a mission. 
    * Fixed Wing Landing (new)
    * Survey (many new features)
  * **Fixed Wing Landing Pattern** - Adds a landing pattern for fixed wings to your mission.
  * **Survey** - New features 
    * **Take Images in Turnarounds** - Specify whether to take images through entire survey or just within each transect segment.
    * **Hover and Capture** - Stop vehicle at each image location and take photo.
    * **Refly at 90 degree offset** - Add additional pattern at 90 degree offset to original so get better image coverage.
    * **Entry location** - Specify entry point for survey.
    * **Polygon editing** - Simple on screen mechanism to drag, resize, add/remove points. Much better touch support.

* **Fly View**
  
  * **Arm/Disarm** - Available from toolbar.
  * **Guided Actions** - New action toolbar on the left. Supports: 
    * Takeoff
    * Land
    * RTL
    * Pause
    * Start Mission
    * Resume Mission - after battery change
    * Change Altitude
    * Land Abort
    * Set Waypoint
    * Goto Location
  * **Remove mission after vehicle lands** - Prompt to remove mission from vehicle after landing.
  * **Flight Time** - Flight time is shown in instrument panel.
  * **Multi-Vehicle View** - Better control of multiple vehicles.

* **Analyze View** - New
  
  * **Log Download** - Moved to Analyze view from menu
  * **Mavlink Console** - NSH shell access

* **Support for third-party customized QGroundControl**
  
  * Standard QGC supports multiple firmware types and multiple vehicle types. There is now support in QGC which allows a third-party to create their own custom version of QGC which is targeted specifically to their custom vehicle. They can then release their own version of QGC with their vehicle.

## Stable Version 3.1

New Features

* [Survey](../PlanView/pattern_survey.md) mission support
* [GeoFence](../PlanView/PlanGeoFence.md) support in Plan View
* [Rally Point](../PlanView/PlanRallyPoints.md) support in Plan View (ArduPilot only)
* ArduPilot onboard compass calibration
* Parameter editor search will now search as you type for quicker access
* Parameter display now supports unit conversion
* GeoTag images from log files (PX4 only)
* System health in instrument panel
* MAVLink 2.0 support (no signing yet)

Major Bug Fixes

* Fixed crash after disconnect from Vehicle
* Fixed android crash when using SiK Radios
* Many multi-vehicle fixes
* Bluetooth fixes