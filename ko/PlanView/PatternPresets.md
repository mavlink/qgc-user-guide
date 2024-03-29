# 계획 보기 - 패턴 사전 설정

일반적인 설정을 명명된 사전 설정으로 저장할 수 있습니다.

> **Note** 현재는 탐색 패턴에서만 지원됩니다. 다른 패턴에 대한 지원은 개발 중입니다.

## 사전설정 관리

![사전 설정 콤보](../../assets/plan/pattern/PatternPresetCombo.jpg)

패턴 항목의 상단에는 사전 설정을 관리할 수 있는 새로운 선택 항목이 있습니다.

* **사용자 지정(모든 설정 지정)** 사전 설정을 사용하지 *않고* 모든 설정을 수동으로 지정 가능합니다.
* **사전 설정 저장** 현재 설정을 명명된 사전 설정으로 저장합니다.
* **사전 설정 삭제** 현재 선택된 사전 설정을 삭제합니다.
* **사전 설정:** 이 항목 아래에는 이 패턴에 사용할 수 있는 사전 설정이 나열됩니다.

## 사전 설정 생성/업데이트

![사전 설정 저장](../../assets/plan/pattern/PatternPresetSave.jpg)

**설정을 사전 설정으로 저장**을 선택하면 사전 설정 이름을 입력하라는 메시지가 표시됩니다. 기존 사전 설정에 대한 새 설정을 저장하려면 사전 설정이 현재 선택된 상태에서 **설정을 사전 설정으로 저장**을 선택합니다.

현재 선택한 카메라를 사전 설정에 저장할지 여부를 지정할 수 있습니다. 카메라를 사전 설정과 함께 저장하지 않도록 선택하면 사전 설정을 로드할 때 현재 카메라가 사용됩니다. 프리셋을 사용할 때 다른 카메라로 변경할 수 있습니다. 동일한 사전 설정으로 다른 시간에 다른 카메라로 차량을 비행하지 않는 한, 사전 설정에 카메라를 저장하도록 선택하여야 합니다.

## 사전 설정 조회

사전 설정의 정확한 설정을 보려면, 모든 설정을 표시하는 **사용자 지정(모든 설정 지정)**으로 다시 전환합니다. 그런 다음 완료후, 명명된 사전 설정을 사용하도록 다시 전환할 수 있습니다.

## 계획 파일의 사전 설정

현재 선택된 사전설정을 플랜 파일에 저장되어 플랜을 다시 로드할 때 사전설정이 다시 선택됩니다. 사전 설정은 QGroundControl 버전에 따라 다릅니다. 다른 사용자와 사전 설정이 있는 계획 파일을 공유하는 경우 해당 사용자도 이름은 같지만 설정이 다른 사전 설정이 있는 경우 잘못된 동작이 발생할 수 있습니다.