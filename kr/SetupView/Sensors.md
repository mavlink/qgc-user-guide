# Sensors
Sensor 셋업을 통해 비행체의 센서를 설정하고 칼리브레이션할 수 있습니다.

![](../../assets/setup/sensors_px4_vtol.jpg)
*Note: PX4 펌웨어를 실행하는 비행체인 경우의 이미지. PX4 펌웨어 옵션은 조금 다를 수 있습니다.*

개별 칼리브레이션 단계를 시작하려면 sensor 버튼을 클릭합니다. 빨간색으로 표시된 sensor의 경우 비행하기 전에 칼리브레이션이 필요합니다. 녹색으로 표시된 sensor는 칼리브레이션이 정상적으로 되었다는 뜻입니다.

## Accelerometer
비행체에 가속도센서를 칼리브레이션하기 위해서는 특정 방향으로 비행체를 위치시키라는 지시를 따르며, 다음 단계로 이동하라는 지시가 나올때까지 유지합니다.

ArduPilot의 경우 화면 중앙에 문자로된 지시를 따르며 Next 버튼을 클릭합니다.

PX4의 경우 위치를 이미지로 가이드합니다.

## Compass

### ArduPilot (새로운 펌웨어)
새로운 ArduPilot 펌웨어의 경우 컴파스 칼리브레이션은 보다 정확한 칼리브레이션을 위해서 Onboard 칼리브레이션을 제공합니다. 비행체를 랜덤하게 모든 축에 대해서 회전시켜서 프로그레스바가 오른쪽으로 다차면 칼리브레이션이 완료됩니다. 칼리브레이션이 완료되면 다음과 같은 결과가 나옵니다. :

![](../../assets/setup/sensor_compass_ardupilot_onboard_calibration_result.jpg)

여기서 각 컴파스에 대해서 칼리브레이션의 품질을 보여줍니다. 이 값을 이용하면 성능이 좋지 않은 컴파스의 경우 사용할지 여부를 결정하는데 도움이 됩니다.

### ArduPilot (이전 펌웨어)와 PX4

PX4와 이전 ArduPilot의 경우 가이드에 따라서 비행체를 각 축에 대해서 여러 방향으로 회전시킵니다. 아직 설정이 완료되지 않은 방향으로 비행체를 둬서 칼리브레이션이 되게 합니다. 회전하라는 지시가 나오면 지정한 축으로 비행체를 회전시킵니다.

![](../../assets/setup/sensor_compass_select_px4.jpg)

## Level Horizon
Accelerometer 칼리브레이션을 마치고 나면 HUD에 수평선이 보이는데 이것은 비행체에 대한 level horizon을 칼리브레이션할 수 있는 level을 뜻하는 것이 아닙니다. 정보를 얻는 동안 비행체를 level orientation으로 위치시키라는 지시가 나올 것입니다.

## CompassMot (ArduPilot만 해당)
CompassMot 칼리브레이션은 내부 컴파스를 가지는 비행체로서 모터, 전선 등으로부터 컴파스에 큰 간섭이 생기는 경우에 추천합니다. CompassMot는 배터리 전류 모니터링을 가지고 있는 경우 잘 동작합니다. 왜냐하면 자기 간섭은 전류가 떨어지는 것에 선형관계를 가지기 때문입니다.

CompassMot 칼리브레이션을 수행할려면 버튼을 클릭하고 onscreen 프롬프트를 따라합니다.

## Sensor Settings
방향 설정 및 센서 사용법

<img src="../../assets/setup/sensor_orientation_sensor_settings.jpg" style="width: 200px;"/>
