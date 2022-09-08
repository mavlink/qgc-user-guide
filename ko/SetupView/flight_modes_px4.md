# PX4 비행 모드 설정

*비행 모드* 섹션에서는 RC 송신기의 특정 스위치/스위치 위치에 의해 트리거되는 비행 모드 및 기타 작업을 설정할 수 있습니다.

> **Note** 비행 모드를 설정하려면 비행 모드를 설정하기 위해 [무전기를 구성](../SetupView/Radio.md)해야 합니다. - [RC 송신기 설정](../SetupView/FlightModes.md#transmitter-setup)(비행 모드 & 송신기 설정)

이 섹션에 액세스하려면, 상단 툴바에서 **기어** 아이콘(차량 설정)을 선택한 다음 사이드바에서 **비행 모드**를 선택하세요.

![Flight modes single-channel](../../assets/setup/flight_modes/px4_single_channel.jpg)




## 비행 모드 설정

The screen allows you to specify a "mode" channel and select up to 6 flight modes that will be activated based on the value sent on the channel. You can also assign a small number of channels to trigger particular actions, such as deploying landing gear, or emergency shutdown (kill switch).

The steps are:

1. Turn on your RC transmitter.
1. Select the **Gear** icon (Vehicle Setup) in the top toolbar and then **Flight Modes** in the sidebar.

   ![Flight modes single-channel](../../assets/setup/flight_modes/px4_single_channel.jpg)

1. Specify *Flight Mode Settings*:
   * Select the transmitter **Mode channel** (shown as Channel 5 above).
   * Select up to six **Flight Modes** for switch positions encoded in the channel. > **Note** Position mode, return mode and mission mode [are recommended](https://docs.px4.io/master/en/config/flight_mode.html#what-flight-modes-and-switches-should-i-set).
1. Specify *Switch Settings*:
   * Select the channels that you want to map to specific actions - *Kill switch*, landing gear, etc. (if you have spare switches and channels on your transmitter).
1. Test that the modes are mapped to the right transmitter switches:
   * Check the *Channel Monitor* to confirm that each switch moves the expected channel.
   * Select each mode switch on your transmitter in turn, and check that the desired flight mode is activated (the text turns yellow on *QGroundControl* for the active mode).

All values are automatically saved as they are changed.


## See Also

- [PX4 Flight Modes](https://docs.px4.io/en/flight_modes/)
