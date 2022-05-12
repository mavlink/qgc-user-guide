# Flight Modes Setup

The *Flight Modes* section allows you to map flight modes to radio channel(s), and hence to the switches on your radio control transmitter. Both flight mode setup and the available flight modes are different in PX4 and ArduPilot (and there are some differences between ArduCopter and ArduPlane).

> **Note** In order to set up flight modes you must already have already [configured your radio](../SetupView/Radio.md), and [setup the transmitter](#transmitter-setup) (as shown below).

To access this section, select the **Gear** icon (Vehicle Setup) in the top toolbar and then **Flight Modes** in the sidebar.

For more flight stack specific setup see:

- [ArduPilot Flight Modes Setup](../SetupView/flight_modes_ardupilot.md)
- [PX4 Flight Modes Setup](../SetupView/flight_modes_px4.md)

## Transmitter Setup

In order setup flight modes you will first need to configure your *transmitter* to encode the physical positions of your mode switch(es) into a single channel.

On both PX4 and ArduPilot you can assign up to 6 different flight modes to a single channel of your transmitter It is common to use the positions of a 2- and a 3-position switch on the transmitter to represent the 6 flight modes. Each combination of switches is then encoded as a particular PWM value that will be sent on a single channel.

> **Note** The single channel is selectable on PX4 and ArduPlane, but is fixed to channel 5 on Copter.

The process for this varies depending on the transmitter. For the *FrSky Taranis* transmitter (a very popular and highly recommended RC transmitter) the process involves assigning a "logical switch" to each combination of positions of the two real switches. Each logical switch is then assigned to a different PWM value on the same channel.

After configuring the switch positions in a single channel you can then map them to flight modes in QGroundControl.