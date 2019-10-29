# Motors Setup

This section is used to setup and test individual motors/servos, and applies to both ArduPilot and PX4:

1. Remove all propellers before running the test.
   > **Warning** You must do this before activating the motors (next step)
1. Slide the switch to enable motor sliders (labeled "Propellers are removed - Enable motor sliders").
1. Adjust the individual sliders to spin the motors and confirm they spin in the correct direction.
   > **Note** The motors only spin after you release the slider and will automatically stop spinning after 3 seconds.

<!-- PX4 Firmware specific:
- If a safety button is used, it must be pressed before motor testing is allowed.
- The kill-switch still works to stop motors immediately.
- The parameter `COM_MOT_TEST_EN` can be used to completely disable motor testing.
- On boards with an IO, only the MAIN pins can be tested.
- On the shell, `motor_test` can be used as well, which has additional options.
-->

![Motors Test](../../assets/setup/Motors.png)

Vehicle specific instructions are provided in the following topics:
* [Motors Setup (ArduSub)](../SetupView/Motors_ardusub.md)

