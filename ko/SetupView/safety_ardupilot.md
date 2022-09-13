# 안전 설정 (ArduPilot)

*안전 설정*에서는 (기체별) 비상 안전 설정을 설정합니다.

> **Tip** 설정 페이지에서는 가장 중요한 안전 옵션을 설정합니다. 다른 안전 장치 설정은 각 차량 유형에 대한 안전 장치 설명서에 설명된 [매개변수](../SetupView/Parameters.md)를 통하여 설정할 수 있습니다.

<span></span>

> **Note** *QGroundControl*은 ArduPilot에서 폴리곤 펜스 또는 랠리 포인트를 지원하지 않습니다.

## 콥터

콥터의 안전 페이지는 아래와 같습니다.

![Safety Setup - Copter (Ardupilot)](../../assets/setup/safety/safety_arducopter.jpg)

> **Note** 추가 안전 설정 및 정보는 [안전장치](http://ardupilot.org/copter/docs/failsafe-landing-page.html)를 참고하십시오.

### 배터리 안전장치 {#battery_failsafe_copter}

이 패널은 [배터리 안전장치](http://ardupilot.org/copter/docs/failsafe-battery.html) 매개변수를 설정합니다. 전압 및 남은 용량에 대해 낮거나 중요한 임계값을 설정하고 안전 장치 값이 위반되는 경우 조치를 정의할 수 있습니다. 임계값을 0으로 설정하여 비활성화할 수 있습니다.

> **Tip** 두 번째 배터리가 있는 경우([전원 설정](../SetupView/Power.md)에서 활성화됨) 두 번째 패널이 동일한 설정으로 표시됩니다.

![Safety Setup - Battery1 Failsafe Triggers (Copter)](../../assets/setup/safety/safety_arducopter_battery1_failsafe_triggers.jpg)

설정 옵션은 다음과 같습니다:

- **Low action**([BATT_FS_LOW_ACT](http://ardupilot.org/copter/docs/parameters.html#batt-fs-low-act-low-battery-failsafe-action)) - 없음, Land, RTL, SmartRTL, SmartRTL 또는 Land, Terminate 중 하나를 선택합니다.
- **Critical action**([BATT_FS_CRT_ACT](http://ardupilot.org/copter/docs/parameters.html#batt-fs-crt-act-critical-battery-failsafe-action)) - 없음, Land, RTL, SmartRTL, SmartRTL 또는 Land, Terminate 중 하나를 선택합니다.
- **Low voltage threshold**([BATT_LOW_VOLT](http://ardupilot.org/copter/docs/parameters.html#batt-low-volt-low-battery-voltage)) - *낮은 동작*을 트리거하는 배터리 전압입니다. 
- **Critical voltage threshold<**([BATT_CRT_VOLT](http://ardupilot.org/copter/docs/parameters.html#batt-crt-volt-critical-battery-voltage))- *중요 작업*을 트리거하는 배터리 전압입니다. 
- **Low mAh threshold**([BATT_LOW_MAH](http://ardupilot.org/copter/docs/parameters.html#batt-low-mah-low-battery-capacity)) - *낮은 작업*을 트리거하는 배터리 용량입니다. 
- **Critical mAh threshold**([BATT_CRT_MAH](http://ardupilot.org/copter/docs/parameters.html#batt-crt-mah-battery-critical-capacity)) - *중요한 작업*을 트리거하는 배터리 용량입니다. 

### 일반적인 안전장치 트리거 {#failsafe_triggers_copter}

이 패널은 [GCS 안전장치](http://ardupilot.org/copter/docs/gcs-failsafe.html)를 활성화하고 스로틀 안전장치를 설정합니다.

![Safety Setup - General Failsafe Triggers (Copter)](../../assets/setup/safety/safety_arducopter_general_failsafe_triggers.jpg)

설정 옵션은 다음과 같습니다:

- **Ground Station failsafe** - 비활성화, 항상 RTL 활성화, 자동 모드에서 미션 계속 활성화, 항상 SmartRTL 또는 RTL 활성화, 항상 SmartRTL 또는 Land 활성화.
- **Throttle failsafe** - 비활성화됨, 항상 RTL, 자동 모드에서 미션 계속, 항상 착륙.
- **PWM Threshold**([FS_THR_VALUE](http://ardupilot.org/copter/docs/parameters.html#fs-thr-value-throttle-failsafe-value)) - 스로틀 페일세이프가 트리거되는 PWM 값입니다.

### 지오펜스 {#geofence_copter}

이 패널은 원통형 [Simple Geofence](http://ardupilot.org/copter/docs/ac2_simple_geofence.html)에 대한 매개변수를 설정합니다. 울타리 반경 또는 높이 활성화 여부, 위반 최대값 및 위반 시 조치를 설정할 수 있습니다.

![Safety Setup - Geofence (Copter)](../../assets/setup/safety/safety_arducopter_geofence.jpg)

설정 옵션은 다음과 같습니다:

- **Circle GeoFence enabled**([FENCE_TYPE](http://ardupilot.org/copter/docs/parameters.html#fence-type-fence-type), [FENCE_ENABLE](http://ardupilot.org/copter/docs/parameters.html#fence-enable-fence-enable-disable)) - 원형 지오펜스를 활성화합니다.
- **Altitude GeoFence enabled**([FENCE_TYPE](http://ardupilot.org/copter/docs/parameters.html#fence-type-fence-type), [FENCE_ENABLE](http://ardupilot.org/copter/docs/parameters.html#fence-enable-fence-enable-disable)) - 고도 지오펜스를 활성화합니다.
- 울타리 작업([FENCE_ACTION](http://ardupilot.org/copter/docs/parameters.html#fence-action-fence-action)) 다음 중 하나: 
  - **보고만** - 울타리 위반을 보고합니다.
  - **RTL 또는 Land** - 출발지 복귀 또는 펜스 경계 착륙
- **최대 반경**([FENCE_RADIUS](http://ardupilot.org/copter/docs/parameters.html#fence-radius-circular-fence-radius)) - 부서졌을 때 RTL을 유발하는 원형 울타리 반경.
- **최대 고도**([FENCE_ALT_MAX](http://ardupilot.org/copter/docs/parameters.html#fence-alt-max-fence-maximum-altitude))- 고도 지오펜스를 트리거하는 최대 고도를 표시합니다.

### 출발지 복귀 {#rtl_copter}

This panel sets the [RTL Mode](http://ardupilot.org/copter/docs/rtl-mode.html) behaviour.

![Safety Setup - RTL (Copter)](../../assets/setup/safety/safety_arducopter_return_to_launch.jpg)

The configuration options are:

- Select RTL return altitude ([RTL_ALT](http://ardupilot.org/copter/docs/parameters.html#rtl-alt-rtl-altitude)): 
  - **Return at current altitude** - Return at current altitude.
  - **Return at specified altitude** - Ascend to specified altitude to return if below current altitude.
- **Loiter above home for** ([RTL_LOIT_TIME](http://ardupilot.org/copter/docs/parameters.html#rtl-loit-time-rtl-loiter-time)) - Check to set a loiter time before landing.
- One of 
  - **Land with descent speed** ([LAND_SPEED](http://ardupilot.org/copter/docs/parameters.html#land-speed-land-speed)) - Select final descent speed.
  - **Final loiter altitude** ([RTL_ALT_FINAL](http://ardupilot.org/copter/docs/parameters.html#rtl-alt-final-rtl-final-altitude)) - Select and set final altitude for landing after RTL or mission (set to 0 to land).

### Arming Checks {#arming_checks_copter}

This panel sets which [Pre-ARM Safety Checks](http://ardupilot.org/copter/docs/prearm_safety_check.html) are enabled.

![Safety Setup - Arming Checks (Copter)](../../assets/setup/safety/safety_arducopter_arming_checks.jpg)

The configuration options are:

- **Arming Checks to perform** ([ARMING_CHECK](http://ardupilot.org/copter/docs/parameters.html#arming-check-arm-checks-to-peform-bitmask)) - Check all appropriate: Barometer, Compass, GPS lock, INS, Parameters, RC Channels, Board voltage, Battery Level, Airspeed, Logging Available, Hardware safety switch, GPS Configuration, System.

## Plane

The Plane safety page is shown below.

![Safety Setup - Plane (Ardupilot)](../../assets/setup/safety/safety_arduplane.jpg)

> **Note** For additional safety settings and information see: [Plane Failsafe Function](http://ardupilot.org/plane/docs/apms-failsafe-function.html) and [Advanced Failsafe Configuration](http://ardupilot.org/plane/docs/advanced-failsafe-configuration.html).

### Battery Failsafe {#battery_failsafe_plane}

The plane battery failsafe is the same as for copter except there are different options for the [Low](http://ardupilot.org/plane/docs/parameters.html#batt-fs-low-act-low-battery-failsafe-action) and [Critical](http://ardupilot.org/plane/docs/parameters.html#batt-fs-crt-act-critical-battery-failsafe-action) actions: None, RTL, Land, Terminate.

For more information see: [battery failsafe](#battery_failsafe_copter) (copter).

### Failsafe Triggers {#failsafe_triggers_plane}

This panel enables the [GCS Failsafe](http://ardupilot.org/plane/docs/advanced-failsafe-configuration.html#ground-station-communications-loss) and enables/configures the throttle failsafe.

![Safety Setup - Failsafe Triggers (Plane)](../../assets/setup/safety/safety_arduplane_failsafe_triggers.jpg)

The configuration options are:

- **Throttle PWM threshold** ([THR_FS_VALUE](http://ardupilot.org/plane/docs/parameters.html#thr-fs-value-throttle-failsafe-value)) - PWM value below which throttle failsafe triggers.
- **GCS failsafe** ([FS_GCS_ENABL](http://ardupilot.org/plane/docs/parameters.html#fs-gcs-enabl-gcs-failsafe-enable)) - Check to enable GCS failsafe.

### Return to Launch {#rtl_plane}

This panel sets the [RTL Mode](http://ardupilot.org/copter/docs/rtl-mode.html) behaviour.

![Safety Setup - RTL (Plane)](../../assets/setup/safety/safety_arduplane_return_to_launch.jpg)

The configuration options are:

- Select RTL return altitude ([RTL_ALT](http://ardupilot.org/copter/docs/parameters.html#rtl-alt-rtl-altitude)): 
  - **Return at current altitude** - Return at current altitude.
  - **Return at specified altitude** - Ascend to specified altitude to return if below current altitude.

### Arming Checks {#arming_checks_plane}

[Arming Checks](#arming_checks_copter) are the same as for copter.

## Rover

The Rover safety page is shown below.

![Safety Setup - Rover (Ardupilot)](../../assets/setup/safety/safety_ardurover.jpg)

> **Note** For additional safety settings and information see: [Failsafes](http://ardupilot.org/rover/docs/rover-failsafes.html).

### Battery Failsafe {#battery_failsafe_rover}

The rover battery failsafe is the same as for [copter](#battery_failsafe_copter).

### Failsafe Triggers {#failsafe_triggers_rover}

This panel enables the rover [Failsafes](http://ardupilot.org/rover/docs/rover-failsafes.html).

![Safety Setup - Failsafe Triggers (Rover)](../../assets/setup/safety/safety_ardurover_failsafe_triggers.jpg)

The configuration options are:

- **Ground Station failsafe** ([FS_GCS_ENABL](http://ardupilot.org/rover/docs/parameters.html#fs-gcs-enable-gcs-failsafe-enable)) - Check to enable GCS failsafe.
- **Throttle failsafe** ([FS_THR_ENABLE](http://ardupilot.org/rover/docs/parameters.html#fs-thr-enable-throttle-failsafe-enable)) - Enable/disable throttle failsafe (value is *PWM threshold* below).
- **PWM threshold** ([FS_THR_VALUE](http://ardupilot.org/rover/docs/parameters.html#fs-thr-value-throttle-failsafe-value)) - PWM value below which throttle failsafe triggers.
- **Failsafe Crash Check** ([FS_CRASH_CHECK](http://ardupilot.org/rover/docs/parameters.html#fs-crash-check-crash-check-action)) - What to do in the event of a crash: Disabled, Hold, HoldAndDisarm

### Arming Checks {#arming_checks_rover}

[Arming Checks](#arming_checks_copter) are the same as for copter.

## Sub

The Sub safety page is shown below.

![Safety Setup - Sub (Ardupilot)](../../assets/setup/safety/safety_ardusub.jpg)

> **Note** For additional safety settings and information see: [Failsafes](https://www.ardusub.com/operators-manual/failsafes.html).

### Failsafe Actions {#failsafe_actions_sub}

The configuration options are:

- **GCS Heartbeat** - Select one of: Disabled, Warn only, Disarm, Enter depth hold mode, Enter surface mode.
- **Leak** - Select one of: Disabled, Warn only, Enter surface mode. 
  - **Detector Pin** - Select one of: Disabled, Pixhawk Aux (1-6), Pixhawk 3.3ADC(1-2), Pixhawk 6.6ADC.
  - **Logic when Dry** - Select one of: Low, High.
- **Battery** - ?.
- **EKF** - Select one of: Disabled, Warn only, Disarm.
- **Pilot Input** - Select one of: Disabled, Warn only, Disarm.
- **Internal Temperature** - Select one of: Disabled, Warn only.
- **Internal Pressure** - Select one of: Disabled, Warn only.

### Arming Checks {#arming_checks_sub}

[Arming Checks](#arming_checks_copter) are the same as for copter.