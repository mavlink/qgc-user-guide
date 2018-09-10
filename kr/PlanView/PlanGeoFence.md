# Plan View - GeoFence
GeoFence로 비행할려는 지역에 가상의 울타리를 만들 수 있습니다. 만약 선택한 지역을 벗어나서 비행하는 경우 지정한 동작을 수행하게 됩니다.

모든 비행 펌웨어가 GeoFence를 지원하는 것은 아니며, 지원하는 GeoFence기능도 다를 수 있습니다.

## 예제 화면
ArduCopter 화면:
![](../../assets/plan/GeoFence.APM.Copter.jpg)

ArduPlane 화면:
![](../../assets/plan/GeoFence.APM.Plane.jpg)

PX4 Pro 화면:
![](../../assets/plan/GeoFence.PX4.jpg)

## GeoFence Setup
GeoFence를 생성하는 단계 :

1. Plan View로 변경
2. GeoFence 라디오 버튼 선택 (오른쪽 위)
3. editor 패널에서 fence 셋팅 지정
4. fence 다각형 추가 (지원하는 경우)
5. GeoFence 정보를 비행체로 전송 (아니면 파일로 저장)

### GeoFence 다각형 그리기
다각형 fence를 지원하는 경우, editor 패널의 밑부분에 "Fence Polygon" 섹션이 보입니다. 지도상에 다각형을 그리기 위해서 Draw 버튼을 클릭하여 포인트를 추가할 수 있습니다.

일단 fence 다각형을 그리고나면, 다각형 모퉁이를 움직이기 위해 Adjust 버튼을 클릭합니다. 새로운 fence 다각형을 그릴려면 Draw 버튼을 다시 누릅니다.

### GeoFence Tools
화면의 왼쪽 모퉁이에 Plan Tools가 있습니다. 이 툴의 위에서 부터 아래로 :

* Sync
* Center map
* Map Type
* Zoom In/Out

#### Sync
Sync 툴로 GeoFence를 비행체나 파일로 보낼 수 있습니다. *비행전에 GeoFence를 비행체로 전송했는지 확인하세요.* 툴이 "!"로 표시되는 것은 GeoFence를 변경한 후에 비행체로 전송하지 않았다는 것을 뜻합니다.

Sync 툴은 다음과 같은 기능을 제공합니다 :

* 비행체로 전송 (Send to Vehicle)
* 비행체로부터 로드 (Load from Vehicle)
* 파일에 저장 (Save to File)
* 파일로부터 로드 (Load from File)
* 전체 삭제 (Remove All)

GeoFence를 파일로 저장하는 경우 fence 다각형뿐만 아니라 모든 셋팅이 저장됩니다.

#### 그 이외 도구들
다른 도구들은 미션을 수정하는 동안 문구대로 동작합니다.
