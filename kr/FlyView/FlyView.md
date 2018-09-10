# Fly View

![](../../assets/quickstart/ConnectedVehicle.jpg)

Fly View는 비행체가 비행하는 동안 사용하는 메인 뷰입니다. map뷰와 video뷰 사이를 스위칭 가능합니다.(가능한 경우에)

## Map

map은 연결된 모든 비행체의 위치를 보여줍니다. 또한 현재 비행체에 대한 미션을 보여줍니다.

## Fly Tools
화면 왼쪽 모퉁이에 Fly Tools을 볼 수 있습니다. 위에서 아래로 Tools의 순서는 :

* Center map
* Map Type
* Zoom In/Out

### Center Map
Center Map tool은 home position, 비행체 등과 같은 여러 포인트 주변을 지도 중앙에 위치시킵니다.

### Map Type
현재 지도 타입을 거리(Street), 위성(Satellite), 하이브리드(Street+Satellite) 중에 선택할 수 있습니다. 기본 제공 지도(map provider)는 Bing이며 하이브리드 지도를 보다 잘 나타냅니다. Settings -> General 에서 제공 지도를 변경할 수 있습니다.

## Video
왼쪽 아래에서 비디오 출력을 볼 수 있습니다. QGroundControl은 UDP 연결을 이용해서 RTP와 RTSP 비디오 스트리밍을 제공합니다. 직접 연결된 UVC 장치도 지원합니다. QGC 비디오 지원에 관한 보드 자세한 내용은 [Video README](https://github.com/mavlink/qgroundcontrol/blob/master/src/VideoStreaming/README.md)을 참고하세요.

비디오 부분을 클릭하면 Fly view의 메인 화면으로 변경시킬 수 있습니다.

## Instrument Panel
오른쪽에 instrument panel은 현재 비행체에 대한 정보를 보여줍니다. 패널의 중앙 섹션은 여러 페이지로 구성됩니다. 중앙 섹션을 클릭해서 페이지간 이동이 가능합니다.

### Telemetry page

<img src="../../assets/fly/InstrumentTelemetryPage.jpg" style="width: 100px;"/>

텔레메트리 페이지 내에서 볼 수 있는 값은 작은 기어 아이콘을 클릭해서 설정이 가능합니다.

### Vehicle Health page

<img src="../../assets/fly/InstrumentHealthPage.jpg" style="width: 100px;"/>

이 페이지에서는 비행체 내부 시스템의 정상상태를 보여줍니다. 어떤 시스템이 정상에서 이상상태로 변경되면 이 페이지는 자동으로 변경됩니다.

### Vibration Clipping page

<img src="../../assets/fly/InstrumentClipPage.jpg" style="width: 100px;"/>

이 페이지는 현재 진동 값과 clip 카운트를 보여줍니다.

## Guided Bar
화면의 밑부분에 Guided Bar가 있습니다. 비행체와 QGroundControl application과 직접 상호작용하는데 사용합니다. 비행체나 현재 Vehicle 상태에 따라 선택가능한 옵션이 바뀝니다.

가능한 옵션들 :

* Arm, Disarm, Emergency Stop
* Takeoff
* Change altitiude
* Go to location
* RTL
* Pause
