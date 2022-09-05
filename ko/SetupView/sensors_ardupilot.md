# 센서 설정 (ArduPilot)

*센서 설정* 섹션에서는 차량의 나침반, 자이로스코프, 가속도계 및 기타 센서를 구성하고 보정할 수 있습니다(사용 가능한 센서는 차량 유형에 따라 다름).

사용 가능한 센서는 사이드바 옆에 버튼 목록으로 표시됩니다. 녹색으로 표시된 센서는 이미 보정된 반면 빨간색으로 표시된 센서는 비행 전에 보정이 필요합니다. 조명이 없는 센서는 보정하지 않도록 선택할 수 있는 기본값이 있는 간단한 설정입니다.

각 센서의 버튼을 클릭하여 보정 시퀀스를 시작합니다.

![Sensors Setup screen Copter](../../assets/setup/sensor/sensor_setup_overview_ardupilot.jpg)

## 가속도계  {#accelerometer}

To calibrate the flight controller accelerometers you will be asked to place and hold your vehicle a number of orientations (you will be prompted when to move between positions).

The calibration steps are:

1. Click the **Accelerometer** sensor button. ![Accelerometer calibration](../../assets/setup/sensor/accelerometer_ardupilot.jpg) > **Note** You should already have set the [Flight Controller Orientation](#flight_controller_orientation) above. If not, you can also set it here. 
2. Click **OK** to start the calibration. 
3. Position the vehicle based on text instructions in the center display. Click the **Next** button to capture each position. ![Accelerometer calibration](../../assets/setup/sensor/accelerometer_positions_ardupilot.jpg)

## Compass {#compass}

ArduPilot uses onboard calibration support that allows for more accurate calibration.

> **Note** Older ArduPilot firmware can be calibrated using the [same process as PX4](../SetupView/sensors_px4.md#compass).

You need to rotate the vehicle randomly around all axes until the progress bar fills all the way to the right and the calibration completes. When the calibration completes you will get the following results:

![ArduPilot Compass Calibration Onboard Result](../../assets/setup/sensor_compass_ardupilot_onboard_calibration_result.jpg)

This shows you the quality of the calibration for each compass. Using these values you can determine whether you may want to turn off usage of poorly performing compasses.

## Level Horizon {#level_horizon}

If the horizon (as shown in the HUD) is not level after completing accelerometer calibration you can calibrate the level horizon for your vehicle. You will be asked to place the vehicle in a level orientation while it captures the information.

1. Click the **Level Horizon** sensor button. ![Level Horizon calibration](../../assets/setup/sensor_level_horizon.jpg) > **Note** You should already have set the [Flight Controller Orientation](#flight_controller_orientation) above. If not, you can also set it here. 
2. Place the vehicle in its level flight orientation on a level surface: 
    - For planes this is the position during level flight (planes tend to have their wings slightly pitched up!)
    - For copters this is the hover position.
3. Click **OK** to start the calibration.

## Pressure/Barometer {#pressure}

This calibration set's the altitude to zero at the current pressure.

To perform **Pressure** calibration:

1. Click the **Calibrate Pressure** button and then **Ok**.
    
    ![Calibrate Pressure](../../assets/setup/sensor/calibrate_pressure_ardupilot.jpg)
    
    The calibration result is immediately displayed:
    
    ![Calibrate Pressure Result](../../assets/setup/sensor/calibrate_pressure_result_ardupilot.jpg)

## CompassMot (Optional)

CompassMot calibration is optional! It is recommended for vehicles that only have an internal compass and when there is significant interference on the compass from the motors, power wires, etc. CompassMot only works well if you have a battery current monitor because the magnetic interference is linear with current drawn.

To perform **CompassMot** calibration:

1. Click the **CompassMot** sensor button.
    
    <img src="../../assets/setup/sensor_compass_mot_menu.jpg" style="width: 250px;" />

2. Follow the onscreen prompts.
    
    ![CompassMot calibration](../../assets/setup/sensor_compass_mot.jpg)

## Sensor Settings {#sensor_settings}

The *Sensor Settings* section allows you to specify the compass orientation and which compasses are enabled.

> **Tip** You can skip this section if the flight controller and compass are mounted upright on the vehicle and facing the front (this is the default orientation - `ROTATION_NONE`).

If the autopilot/compass are mounted in any other way you will need to specify their orientations as YAW, PITCH and/or ROLL offsets relative to the forward-facing-upright orientation (clock-wise rotation around the Z, Y and X axis, respectively).

![Flight Controller Orientation](../../assets/setup/flight_controller_orientation.png)

For example, the image below are at orientations: `ROTATION_NONE`, `ROTATION_YAW_90`,`ROTATION_YAW_180`,`ROTATION_YAW_270`.

![Flight controller yaw rotation](../../assets/setup/flight_controller_yaw_rotation.png)

To set the orientation(s) and compasses used:

1. Select the **Sensor Settings** button.
    
    ![Sensor Settings](../../assets/setup/sensor/sensor_settings_ardupilot.jpg)

2. Select the **AutoPilot Orientation**.

3. Select the *orientation* from **Compass 1 (primary/external) > Orientation** (or check **Compass2 (secondary, external) > Use Compass** to instead use the internal compass).
4. Press **OK**.