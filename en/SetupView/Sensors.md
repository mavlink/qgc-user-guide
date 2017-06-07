# Sensors

The *Sensor Setup* section allows you to configure and calibrate the vehicle's compass, gyroscope, accelerometer and other sensors (if present).

Available sensors are displayed as a list of buttons beside the sidebar. Sensors marked with green are already calibrated. Sensors marked with red require calibration prior to flight. 

![Sensors Setup screen for VTOL vehicle](../../images/setup/sensors_px4_vtol.jpg)

> **Note** The image shown is from a VTOL vehicle running PX4 firmware. Other autopilot firmware and vehicles will offer slightly different options.

Click on the button for each sensor to start its calibration sequence.

<span id="flight_controller_orientation"></span>
## Flight Controller Orientation (Sensor Settings / Set Orientations)

> **Tip** You can skip this section if the flight controller and compass are mounted in the default orientation (upright on the vehicle and facing the front - `ROTATION_NONE`).

If the autopilot/compass are mounted in any other way you will need to specify the orientations using either the **Sensor Settings** or **Set Orientation** buttons. In either case, choose the orientation for your autopilot/sensors from the selection list(s) and then press **OK**.

<img src="../../images/setup/sensor_orientation_sensor_settings.jpg" style="width: 600px;"/>

<img src="../../images/setup/sensor_orientation_set_orientations.jpg" style="width: 600px;"/>

> **Note** The orientation is specified as YAW, PITCH and/or ROLL offsets relative to the forward-facing-upright orientation (clock-wise rotation around the Z, Y and X axis, respectively).
>
> <img src="../../images/setup/flight_controller_orientation.png" style="width: 600px;"/>
>
> For example, the image below shows some `ROTATION_YAW_XX` orientations:
> <img src="../../images/setup/flight_controller_yaw_rotation.png" style="width: 600px;"/>



## Compass

### PX4 Compass Calibration

For PX4 you will be guided to position the vehicle in a number of set orientations and rotate the vehicle about the specified axis. 

> **Note** This process is also used for calibrating the compass on older ArduPilot firmware.

The calibration steps are:

1. Click the **Compass** sensor button

1. Click **OK** to start the calibration. 

   <img src="../../images/setup/sensor_compass_orientation_prompt.jpg" width="250px" title="Start calibration prompt" />

   > **Note** You should already have set the [Flight Controller Orientation](#flight_controller_orientation) in the previous section. If not, you can also set it here.

1. Place the vehicle in any of the orientations shown in red (incomplete) and hold it still. Once prompted (the orientation-image turns yellow) rotate the vehicle around the specified axis in either/both directions. Once the calibration is complete in that orientation the associated image on the screen will turn green.
 
   ![](../../images/setup/sensors_px4_compass.jpg)
   
1. Repeat the calibration process for all vehicle orientations.
   
Once you've rotated the vehicle in all the positions *QGroundControl* will display *Calibration complete* (all orientation images will be displayed in green and the progress bar will fill completely). You can then proceed to the next sensor. 


### ArduPilot Compass Calibration

ArduPilot uses onboard calibration support that allows for more accurate calibration. 

> **Note** Older ArduPilot firmware can be calibrated using the same process as PX4. 

You need to rotate the vehicle randomly around all axes until the progress bar fills all the way to the right and the calibration completes. When the calibration completes you will get the following results:

![ArduPilot Compass Calibration Onboard Result](../../images/setup/sensor_compass_ardupilot_onboard_calibration_result.jpg)

This shows you the quality of the calibration for each compass. Using these values you can determine whether you may want to turn off usage of poorly performing compasses.



## Accelerometer

To calibrate the flight controller accelerometers you will be asked to place and hold your vehicle a number of orientations (you will be prompted when to move between positions).

The screens are different for PX4 and ArduPilot:

* **PX4:** Position the vehicle as guided by the *images* on the screen. This is very similar to compass calibration.
  
  ![Accelerometer calibration](../../images/setup/sensor_accelerometer_positions_px4.jpg)
  
* **ArduPilot:** Position the vehicle based on text instructions in the center display. Click the **Next** button to capture each position.


## Level Horizon

If the horizon (as shown in the HUD) is not level after completing Accelerometer calibration you can calibrate the level horizon for your vehicle. You will be asked to place the vehicle in a level orientation while it captures the information.

1. Place the vehicle in its level flight orientation on a level surface:

  * For planes this is the position during level flight (planes tend to have their wings slightly pitched up!)
  * For copters this is the hover position.

1. Click the **Level Horizon** button.


## Airspeed

For Airspeed calibration you will need to keep your airspeed sensor out of any wind and then blow across the sensor. 

To calibrate the airspeed sensor:

1. Click the **Airspeed** sensor button
1. Click **OK** to start the calibration. 

![Airspeed calibration](../../images/setup/sensors_airspeed.jpg)


## CompassMot (Optional - ArduPilot only)

CompassMot calibration is optional! It is recommended for vehicles that only have an internal compass and where there is significant interference on the compass from the motors, power wires, etc. CompassMot only works well if you have a battery current monitor because the magnetic interference is linear with current drawn.

To perform **CompassMot** calibration:

1. Click the **CompassMot** button.
1. Follow the onscreen prompts.