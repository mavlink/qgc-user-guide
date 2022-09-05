# 라디오 설정

무선 조종기 설정은 주요 송신기 자세 제어 스틱(롤, 피치, 요, 스로틀)의 매핑 채널을 설정하고, 다른 모든 송신기 제어/RC 채널에 대한 최소, 최대, 트림 및 역방향 설정을 보정합니다.

주요 보정 프로세스는 PX4 및 ArduPilot에서 동일합니다(여러 추가 비행 컨트롤러 관련 설정/도구는 [아래에 자세히 설명되어 있음](#additional-radio-setup)).

> **Note** 무선 조종기를 보정하려면, 수신기와 송신기를 먼저 바인딩하여야 합니다. 송신기와 수신기를 바인딩 프로세스는 하드웨어에 따라 조금씩 차이가 날 수 있습니다 (자세한 지침은 설명서 참조).

## 보정 절차

보정 프로세스는 간단합니다. 화면 오른쪽 상단의 트랜스미터 다이어그램에 표시된 특정 패턴으로 스틱을 움직여야 합니다. 지침에 따라 보정을 완료합니다.

무선 조종기 보정 절차

1. 상단 도구 모음에서 **톱니 바퀴** 아이콘(기체 설정)을 선택한 다음 가장자리 표시줄에서 **무선 조종기**를 선택하십시오.
2. RC 송신기를 켭니다.
3. **확인**을 눌러 보정작업을 시작합니다.
    
    ![Radio setup - before starting](../../assets/setup/radio_start_setup.jpg)
    
    > **Note** 위 이미지는 PX4 Pro용입니다. 보정/상단 섹션은 두 펌웨어 모두 동일하지만 *추가 라디오 설정* 섹션은 다릅니다.

4. 트랜스미터와 일치하는 *송신기 모드* 라디오 버튼을 설정합니다 (이렇게하면 *QGroundControl*이 교정 중에 따라야 할 올바른 스틱 위치를 표시함).
    
    ![Radio setup - move sticks](../../assets/setup/radio_sticks_throttle.jpg)

5. 스틱을 텍스트(및 송신기 이미지)에 표시된 위치로 이동합니다. 스틱이 제자리에 있으면 **다음**을 누르십시오. 모든 위치에 대하여 반복하십시오.

6. 메시지가 표시되면 다른 모든 스위치와 다이얼을 전체 범위로 이동합니다 (*채널 모니터*에서 움직이는 것을 관찰 할 수 있습니다).

7. **Next(다음)**를 클릭하여 설정을 시작합니다.

Radio calibration is demonstrated in the [PX4 setup video here](https://youtu.be/91VGmdSlbo4?t=4m30s) (youtube).

## Additional Radio Setup

At the lower part of the *Radio Setup* screen is firmware-specific *Additional Radio setup* section. The options for each autopilot are shown below.

| PX4                                                                                                                               | ArduPilot                                                                                                                                     |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| <img src="../../assets/setup/radio_additional_radio_setup_px4.jpg" title="Radio setup - PX4 additional settings" width="300px" /> | <img src="../../assets/setup/radio_additional_radio_setup_ardupilot.jpg" title="Radio setup - ArduPilot additional settings" width="300px" /> |

### Spectrum Bind (ArduPilot/PX4)

Before you can calibrate the radio system the receiver and transmitter must be connected/bound. If you have a *Spektrum* receiver you can put it in *bind mode* using *QGroundControl* as shown below (this can be particularly useful if you don't have easy physical access to the receiver on your vehicle).

To bind a Spektrum transmitter/receiver:

1. Select the **Spektrum Bind** button
2. Select the radio button for your receiver
3. Press **OK**
    
    ![Spektrum Bind](../../assets/setup/radio_additional_setup_spectrum_bind_select_channels.jpg)

4. Power on your Spektrum transmitter while holding down the bind button.

### Copy Trims (PX4)

This setting is used to copy the manual trim settings from your radio transmitter so that they can be applied automatically within the autopilot. After this is done you will need to remove the manually set trims.

To copy the trims:

1. Select **Copy Trims**.
2. Center your sticks and move throttle all the way down. 
3. Press **Ok**.
    
    ![Copy Trims](../../assets/setup/radio_additional_radio_setup_copy_trims_px4.jpg)

4. Reset the trims on your transmitter back to zero.

### AUX Passthrough Channels (PX4)

AUX passthrough channels allow you to control arbitrary optional hardware from your transmitter (for example, a gripper).

To use the AUX passthrough channels:

1. Map up to 2 transmitter controls to separate channels. 
2. Specify these channels to map to the AUX1 and AUX2 ports respectively, as shown below. Values are saved to the vehicle as soon as they are set.
    
    ![AUX1 and AUX2 RC passthrough channels](../../assets/setup/radio_additional_setup_aux_passthrough_channels_px4.jpg)

The flight controller will pass through the unmodified values from the specified channels out of AUX1/AUX2 to the connected servos/relays that drive your hardware.

### Param Tuning Channels (PX4)

Tuning channels allow you to map a transmitter tuning knob to a parameter (so that you can dynamically modify a parameter from your transmitter).

> **Tip** This feature is provided to enable manual in-flight tuning.

The channels used for parameter tuning are assigned in the *Radio* setup (here!), while the mapping from each tuning channel to its associated parameter is defined in the *Parameter editor*.

To set up tuning channels:

1. Map up to 3 transmitter controls (dials or sliders) to separate channels.
2. Select the mapping of *PARAM Tuning Id* to radio channels, using the selection lists. Values are saved to the vehicle as soon as they are set.
    
    ![Map radio channels to tuning channels](../../assets/setup/radio_additional_radio_setup_param_tuning_px4.jpg)

To map a PARAM tuning channel to a parameter:

1. Open the **Parameters** sidebar. 
2. Select the parameter to map to your transmitter (this will open the *Parameter Editor*).
3. Check the **Advanced Settings** checkbox.
4. Click the **Set RC to Param...** button (this will pop-up the foreground dialog displayed below)
    
    ![Map tuning channels to parameters](../../assets/setup/parameters_radio_channel_mapping_px4.jpg)

5. Select the tuning channel to map (1, 2 or 3) from the *Parameter Tuning ID* selection list.

6. Press **OK** to close the dialog.
7. Press **Save** to save all changes and close the *Parameter Editor*.

> **Tip** You can clear all parameter/tuning channel mappings by selecting menu **Tools > Clear RC to Param** at the top right of the *Parameters* screen.