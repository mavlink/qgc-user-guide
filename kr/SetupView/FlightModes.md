# Flight Modes Setup

이 페이지에서는 rc 트랜스미터에서 비행모드(flight mode) 스위치를 설정하는 방법에 대해서 알아봅니다. 비행모드는 RTL(Return to Launch)과 같은 기능뿐만 아니라 다양한 비행 안정성 단계를 지정합니다.

## ArduPilot 비행모드 셋업
![](../../assets/setup/ArduCopterFlightMode.jpg)
*Note: ArduCopter 비행체 이미지*


여러분이 가지고 있는 트랜스미터에서 하나의 채널에 6가지 서로 다른 비행모드를 할당할 수 있습니다. 비행모드를 설정하는 방법은 채널의 출력이 특정 PWM 값의 범위에 있을 때 설정됩니다. 위에 이미지를 참고하세요. 비행모드를 변경할려면 간단하게 드롭다운에서 선택합니다.

트랜스미터를 켜서 여러분의 스위치 셋업을 테스트할 수 있습니다. 현재 선택된 비행모드를 노란색으로 하이라이트로 표시합니다. 위에 이미지에서 비행모드 4가 활성화되어 있습니다. 이렇게 하면 채널 옵션 셋팅도 테스트합니다.

위 예제 이미지는 3개 위치 비행모드 스위치와 채널 7 스위치로 RTL을 추가 옵션으로 설정하였습니다. 트랜스미터에서 2개 스위치와 믹싱을 사용해서 6개 비행모드를 설정할 수 있습니다. 어떻게 하는지 알려면 이[페이지](http://ardupilot.org/copter/docs/common-rc-transmitter-flight-mode-configuration.html#common-rc-transmitter-flight-mode-configuration)의 가운데 섹션으로 스크롤다운하세요.

### ArduCopter만 해당
* 비행모드 채널은 채널 5로 고정되어 있음
* 채널 7-12에 대해서 추가로 채널 옵션을 설정할 수 있음. 이들 스위치에 기능을 할당할 수 있음.

### ArduPlane만 해당
* 비행모드 채널은 드롭다운으로 선택가능. (이미지 없음)
* ArduPlane은 추가 채널 옵션을 지원하지 않음.

[ArduCopter 상세 비행모드 설명](http://ardupilot.org/copter/docs/flight-modes.html)

[ArduCopter 상세 비행모드 설명](http://ardupilot.org/copter/docs/channel-7-and-8-options.html#configuration)

[ArduPlane 상세 비행모드 설명](http://ardupilot.org/plane/docs/flight-modes.html)

## PX4 Pro 비행모드 셋업
![](../../assets/setup/PX4SingleChannelFlightMode.jpg)
