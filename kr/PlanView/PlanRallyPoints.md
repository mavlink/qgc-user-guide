# Plan View - Rally Points

Rally 포인트는 착륙 혹은 로이터링 위치를 대신합니다.

RETURN TO LAUNCH(RTL)모드에서 home position보다 안전하고 편리한 목적지를 제공하는데 일반적으로 사용됩니다.

![](../../assets/plan/RallyPoints.jpg)

> **Note** 모든 비행 펌웨어가 렐리 포인트를 지원하는 것은 아니며, 지원하더라도 Rally Point 기능은 다를 수 있습니다. ArduPilot와 관련한 문서는 [여기](http://ardupilot.org/copter/docs/common-rally-points.html)에서 찾을 수 있습니다. PX4는 현재(4월 2017) 지원하지 않습니다.

## Rally Point Setup
GeoFence를 생성하는 단계 :

1. Plan View로 변경
2. Rally 버튼을 선택 (화면의 오른쪽 상단)
3. 지도에 클릭해서 렐리 포인트 추가

### Rally Points Tools
화면의 왼쪽 모퉁이에 Plan Tools가 있습니다. 이 도구들은 위에서 아래로 순서로 :

* Sync
* Center map
* Map Type
* Zoom In/Out

#### Sync
Sync는 Rally Points를 비행체나 파일로 보낼 수 있습니다. *비행전에 Rally Points를 비행체로 전송했는지 확인하세요.* "!"로 표시되는 것은 GeoFence를 변경한 후에 비행체로 전송하지 않았다는 것을 뜻합니다.

Sync 도구는 다음과 같은 기능을 제공합니다 :

* 비행체로 전송
* 비행체로부터 로드
* 파일에 저장
* 파일로부터 로드
* 전체 삭제

#### 그 이외 도구들
다른 도구들은 미션을 수정하는 동안 문구대로 동작합니다.
