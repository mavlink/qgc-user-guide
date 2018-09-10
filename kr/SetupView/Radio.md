# 라디오 셋업

라디오 셋업은 주요 트랜스미터 자세 제어 스틱(roll, pitch, yaw, throttle)을 채널로 매핑 설정하며 다른 모든 트랜스미터 제어/RC 채널에 대해서 최대, 최소, 트림, 반전 셋팅을 칼리브레이션합니다.

주요 칼리브레이션 절차는 PX4와 Ardupilot이 동일합니다. (추가적으로 다양한 비행제어기에 특화된 셋팅/도구는 [아래](#additional-radio-setup)를 참고하세요.)

> **Note** 라디오 시스템을 칼리브레이션하기 전에 리시버와 트랜스미터는 반드시 연결된 상태여야 합니다. 트랜스미터와 리시버 쌍의 바인딩 절차는 하드웨에에 따라 다릅니다. (메뉴얼의 지시를 따릅니다.)



## 칼리브레이션 수행

칼리브레이션 절차는 어렵지 않습니다. - 화면의 오른쪽 위에 트랜스미터 그림이 보이고 특정 패턴으로 스틱을 움직이라는 지시가 나옵니다. 단순히 지시를 따르면 칼리브레이션을 성공적으로 완료할 수 있습니다.

라디오를 칼리브레이션 하기 위해서 :

1. 상단 툴바에서 **Gear** 아이콘을(Vehicle Setup) 선택합니다. 그리고 사이드바에 있는 **Radio** 을 선택합니다.
1. RC 트랜스미터를 켭니다.
1. **OK** 를 누르면 칼리브레이션이 시작됩니다.

   ![라디오 셋업 - 시작하기 전](../../assets/setup/radio_start_setup.jpg)

   > **Note** 위 이미지는 PX4 Pro인 경우입니다. 칼리브레이션/위 섹션은 두개 펌웨어에 대해서 동일하지만 *추가 라디오 셋업* 섹션은 다릅니다.

1. *transmitter mode* 라디오 버튼을 설정하면 트랜스미터 설정과 매치시킵니다. (이렇게 하면 *QGroundControl* 는 칼리브레이션 동안 여러분이 따라야 할 올바른 스틱 위치를 표시합니다.)

   ![라디오 셋업 - 스틱 움직이기](../../assets/setup/radio_sticks_throttle.jpg)

1. 텍스트와 트랜스미터 이미지에서 지시하는 위치로 스틱을 이동시킵니다. 스틱이 위치에 있을때 **Next** 를 누릅니다. 모든 위치에 대해서 반복합니다.
1. 프롬프트가 나오면 다른 모든 스위치와 다이얼을 최대 허용범위까지 움직입니다.(*Channel Monitor* 를 통해 움직이는 것을 관찰할 수 있음)

1. **Next** 를 눌러서 설정을 저장합니다.

라디오 칼리브레이션은 [PX4 셋업 비디오](https://youtu.be/91VGmdSlbo4?t=4m30s) (youtube)를 참고하세요.



## 추가 라디오 셋업 {#additional-radio-setup}

*라디오 셋업* 화면의 아래 부분에 사용하는 펌웨어에 따라 *추가 라디오 셋업* 섹션이 달라집니다. 각 autopilot마다의 옵션은 아래와 같습니다.

PX4 | ArduPilot
---|---
<img src="../../assets/setup/radio_additional_radio_setup_px4.jpg" title="Radio setup - PX4 additional settings" width="300px" /> | <img src="../../assets/setup/radio_additional_radio_setup_ardupilot.jpg" title="Radio setup - ArduPilot additional settings" width="300px" />


### Spectrum 바인드 (ArduPilot/PX4)

라디오 시스템을 칼리브레이션하기 전에, 리시버와 트랜스미터는 연결된 상태여야 합니다. 만약 *Spektrum* 리시버를 가지고 있다면, *QGroundControl* 를 사용하면 아래와 같이 *bind mode* 로 할 수 있습니다. (비행체의 리시버에 물리적으로 쉽게 접근하기 어려운 경우 특히 유용합니다.)

Spektrum 트랜스미터/리시버 바인드 :

1. **Spektrum Bind** 버튼 선택
1. 리시버에 대한 라디오 버튼 선택
1. **OK** 누르기

   ![Spektrum 바인드](../../assets/setup/radio_additional_setup_spectrum_bind_select_channels.jpg)

1. 바인드 버튼을 누르고 있으면서 Spektrum 트랜스미터 켜기


### Trims 복사하기 (PX4)

이 셋팅은 수동으로 라디오 트랜스미터로부터 trim 셋팅을 복사합니다. 따라서 autopilot 내에 자동으로 적용될 수 있습니다. 완료되고 나면 수동으로 설정한 trim들을 제거해야 합니다.

trim을 복사:

1. **Copy Trims** 선택
1. 스틱을 가운데에 두고 throttle을 완전히 아래로 내림
1. **Ok** 누르기

   ![Trim 복사하기](../../assets/setup/radio_additional_radio_setup_copy_trims_px4.jpg)

1. 트랜스미터를 0으로 두면 trim이 리셋



### AUX 사용 채널 (PX4)

AUX 사용 채널을 이용하면 트랜스미터로 임의의 하드웨어 제어가 가능합니다. (예로 잡는 장치)

AUX 채널을 사용하는 방법 :

1. 2개 트랜스미터 제어까지 별로 채널로 매핑이 가능
1. 이 채널들을 AUX1과 AUX2로 각각 매핑하며 설정하자마자 비행체에 값이 저장

   ![AUX1 and AUX2 RC passthrough channels](../../assets/setup/radio_additional_setup_aux_passthrough_channels_px4.jpg)

flight controller는 AUX1/AUX2의 지정한 채널로부터 수정하지 않은 값을 연결된 서버/릴레이로 전달하여 하드웨어를 조정


### Param 튜닝 채널 (PX4)

튜닝 채널을 이용해서 트랜스미터의 튜닝 노브를(knob) 파라미터로 매핑이 가능합니다. (트랜스미터로 동적으로 파라미터를 수정할 수 있습니다.)

> **Tip** 이 기능은 수동 비행중 튜닝이 가능하도록 제공합니다.

파라미터 채널을 위해 사용하는 채널들은 *Radio* 셋업에서 할당됩니다.(여기서!) 각 튜닝 채널을 관련 파라미터로 매핑하는 것은 *Parameter editor* 에서 정의합니다.

튜닝 채널 셋업하기 :

1. 최대 3개 트랜스미터 제어를 별도의 채널로 매핑
1. 선택 목록을 사용해서 *PARAM Tuning Id* 를 라디오 채널로 매핑을 선택. 설정하자마자 비행체에 값이 저장.

   ![라디오 채널을 튜닝 채널로 매핑](../../assets/setup/radio_additional_radio_setup_param_tuning_px4.jpg)

PARAM 튜닝 채널을 파라미터로 매핑 :

1. **Parameters** 사이드바를 열기
1. 트랜스미터로 매핑하기 위한 파라미터를 선택 (*Parameter Editor* 를 열기)
1. **Advanced Settings** 체크박스를 체크
1. **Set RC to Param...** 버튼을 클릭 (아래와 같이 대화창이 나타남)

   ![Map tuning channels to parameters](../../assets/setup/parameters_radio_channel_mapping_px4.jpg)
1. *Parameter Tuning ID* 선택 목록에서 매핑하기 위해서 튜닝 채널을 선택
1. **OK** 를 누르면 대화창이 닫힘
1. **Save** 를 누르면 모든 변경 내용이 저장되고 *Parameter Editor* 가 닫힘


> **Tip** *Parameters* 화면의 오른쪽 위에 있는 **Tools > Clear RC to Param** 메뉴를 선택하면 명시적으로 모든 파라미터/튜닝 채널 매핑이 가능합니다.
