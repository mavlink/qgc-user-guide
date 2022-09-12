# 전원 설정

*전원 설정*은 배터리 매개변수를 설정과 프로펠러 고급 설정을 제공합니다.

![Battery Calibration](../../assets/setup/PX4Power.jpg)

## 배터리 전압 및 전류 보정

데이터 시트에서 배터리 전력 모듈에 대한 다음의 데이터를 입력합니다: 셀 수, 셀당 최대 전압, 셀당 빈 전압. 전압 분배기 및 볼트당 암페어 정보도 입력하면 더욱 좋습니다.

*QGroundControl*을 사용하여 측정에서 적절한 전압 분배기 및 볼트당 암페어 값을 계산할 수 있습니다.

1. 멀티미터를 사용하여 배터리의 전압을 측정합니다.
2. *전압 분배기* 필드 옆에 있는 **계산**을 클릭합니다. 표시된 프롬프트에서: 
    1. 측정 전압을 입력합니다.
    2. 새 전압 분배기 값을 생성하려면 **계산**을 클릭합니다.
    3. **닫기**를 클릭하여 값을 기본 양식에 저장합니다. 
3. 배터리의 전류를 측정합니다.
4. *볼트당 암페어* 필드 옆에 있는 **계산**을 클릭합니다. 표시된 프롬프트에서: 
    1. 측정한 전류를 입력합니다.
    2. Click **Calculate** to generate a new *amps per volt* value.
    3. Click **Close** to save the value into the main form. 

## Advanced Power Settings

Click the **Show Advanced Settings** checkbox to specify advanced power settings.

### Voltage Drop on Full Load

Batteries show less voltage at high throttle. Enter the difference in Volts between idle throttle and full throttle, divided by the number of battery cells. The default value should be used if unsure!

> **Warning** If the value is too high the battery may be deep-discharged and damaged.

## ESC PWM Minimum and Maximum Calibration

To calibrate the ESC max/min PWM values:

1. Remove the propellers. 
2. Connect the vehicle to QGC via USB (only). 
3. Click the **Calibrate** button.

> **Warning** Never attempt ESC calibration with props on.
> 
> Motors should not spin during ESC calibration. However if an ESC doesn't properly support/detect the calibration sequence then it will respond to the PWM input by running the motor at maximum speed.

## Other Settings

Select the **Show UAVCAN Settings** checkbox to access additional settings for UAVCAN Bus Configuration and motor index and direction assignment.