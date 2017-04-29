# Flight Modes Setup

This page allows you to configure the flight mode switch on your rc transmitter. Flight modes allow for different levels of flight stablization as well as features such as Return to Launch (RTL).

## ArduPilot Flight Mode Setup
![](../../images/setup/ArduCopterFlightMode.jpg)
*Note: Image is from an ArduCopter vehicle.*

You can assign up to 6 different flight modes to a single channel of your transmitter. The flight mode will be selected when the output from the channel is whithin the specified PWM range as shown in the image above. To change a flight mode selection simply select it from the dropdown.

You can test your switch setup by turning on your transmitter. The page will highlight the currently selected flight mode in yellow. In the above image Flight Mode 4 is currently active. This also works for testing Channel Options settings.

The example image above shows a typical setup for a three position flight mode switch with an additional option of RTL being on a channel 7 switch. You can also setup 6 flight modes using two switches plus mixing on your transmitter. Scroll down to the center section of this [page](http://ardupilot.org/copter/docs/common-rc-transmitter-flight-mode-configuration.html#common-rc-transmitter-flight-mode-configuration) for tutorials on how to do that.

### ArduCopter only
* The flight mode channel is fixed to channel 5. 
* You can also set additional Channel Options for channels 7-12. This allows you to assign functions to these switches.

### ArduPlane only
* The flight mode channel can be selected from the drop down. (Not shown in image)
* ArduPlane does not support additional Channel Options.

[ArduCopter detailed flight mode descriptions](http://ardupilot.org/copter/docs/flight-modes.html)

[ArduCopter detailed channel option descriptions](http://ardupilot.org/copter/docs/channel-7-and-8-options.html#configuration)

[ArduPlane detailed flight mode descriptions](http://ardupilot.org/plane/docs/flight-modes.html)

## PX4 Pro Flight Mode Setup
![](../../images/setup/PX4SingleChannelFlightMode.jpg)
