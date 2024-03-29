# 모터 설정 (ArduSub)

ArduSub가 제대로 작동하려면 모터가 올바르게 설정되어야 합니다.

ROV를 방금 조립했다면 먼저 **수동 테스트** 섹션에서 추진기가 올바른 출력에 연결되었는 지 확인하십시오. 각 슬라이더를 드래그하여 표시된 프레임에 따라 *올바른 모터*가 회전하는 지 확인합니다.

추진기가 적절한 출력에 연결되면, [자동 방향 감지](#automatic)(ArduSub 4.0에서 권장) 또는 [수동 테스트](#manual)로 *정확한 방향*(정방향/역방향)을 확인할 수 있습니다.

> **Note** [수동 테스트](#manual)는 ArduSub 3.5까지 지원되며, ArduSub 4.0은 [수동 테스트](#manual)와 [자동 방향 감지](#automatic)를 모두 지원합니다.

## 수동 테스트 {#manual}

ArduSub 모터 설정에서 각각의 모터를 테스트할 수 있습니다. 슬라이더를 사용하면 각 모터를 정방향 또는 역방향 모드로 회전할 수 있으며, 슬라이더 아래의 확인란을 사용하면 개별 추진기의 작동을 반대로 할 수 있습니다.

오른쪽 이미지는 각 추진기의 위치, 방향 및 현재 사용 중인 프레임을 보여줍니다. 프레임 선택이 차량과 일치하지 않으면, 먼저 [프레임](../SetupView/airframe_ardupilot.md#ardusub) 탭에서 올바른 프레임을 선택하십시오.

모터를 수동으로 설정하고 테스트하려면 페이지의 지침을 읽고 따르십시오.

> **Warning** 스위치를 밀어 차량을 무장시키고 테스트를 활성화하기 전에 모터와 프로펠러에 장애물이 없는 지 확인하십시오!

![Ardusub 모터 테스트](../../assets/setup/motors-sub.jpg)

## 자동 방향 감지 {#automatic}

Ardusub 4.0 이상 버전에서는 모터 방향의 자동 감지를 지원합니다. 이것은 각 모터에 펄스를 적용하고 프레임이 예상대로 반응하는 지 확인하고 필요한 경우 모터를 반대로 하여 작동합니다. 이 과정은 약 1분 정도 걸립니다.

자동 모터 방향 감지를 수행하려면 **차량 설정->모터** 탭으로 이동하여 **자동 감지 방향** 버튼을 클릭하고 기다립니다. 프로세스에 대한 추가 출력은 실행될 때 버튼 옆에 표시됩니다.

> **Warning** 이 절차를 수행하려면 프레임 보기에 표시된 대로 모터가 *올바른 출력*에 연결되어 있어야 합니다!

![Ardusub 모터 자동 설정](../../assets/setup/motors-sub-auto.jpg)
