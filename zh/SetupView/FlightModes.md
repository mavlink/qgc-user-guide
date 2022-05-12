# Flight Modes Setup

The *Flight Modes* section allows you to map flight modes to radio channel(s), and hence to the switches on your radio control transmitter. Both flight mode setup and the available flight modes are different in PX4 and ArduPilot (and there are some differences between ArduCopter and ArduPlane).

To access this section, select the **Gear** icon (Vehicle Setup) in the top toolbar and then **Flight Modes** in the sidebar.

> **Note** You must already have [configured your radio](../SetupView/Radio.md) in order to set flight modes.

<span></span>

> **Tip** Flight modes provide different levels of *autopilot-assisted flight*, and *fully autonomous flight* via missions or offboard (API-based) control. Different flight modes allow new users to learn flying with a more forgiving platform than provided by basic RC control alone. They also enable automation of common tasks like taking off, landing and returning to the original launch position.

<div>
</div>

> For more information about the flight modes on each platform see: * [PX4 Flight Modes](https://docs.px4.io/en/flight_modes/) * [ArduCopter Flight Modes](http://ardupilot.org/copter/docs/flight-modes.html) * [ArduPlane Flight Modes](http://ardupilot.org/plane/docs/flight-modes.html)

## ArduPilot Flight Mode Setup

On ArduPilot you can assign up to 6 different flight modes to a single channel of your transmitter (the channel is selectable on Plane, but fixed to channel 5 on Copter).

ArduCopter (only) also allows you to specify additional *Channel Options* for channels 7-12. These allow you to assign functions to these switches (for example, to turn on a camera, or return to launch). There is additional information about channel configuration in the ArduCopter docs: [Auxiliary Function Switches](https://ardupilot.org/copter/docs/channel-7-and-8-options.html#channel-7-and-8-options)

To set the flight modes:

1. Turn on your RC transmitter.
2. Select the **Gear** icon (Vehicle Setup) in the top toolbar and then **Flight Modes** in the sidebar.
    
    ![Flight modes setup - ArduCopter](../../assets/setup/flight_modes_copter_ardupilot.jpg)
    
    > **Note** The above image is a screenshot of the flight mode setup for ArduCopter.

3. Select up to 6 flight modes in the drop downs.

4. **ArduCopter only:** Select additional *Channel Options* for channels 7-12.
5. **ArduPlane only:** Select the mode channel from the dropdown.
    
    ![Flight modes setup - ArduPlane](../../assets/setup/flight_modes_plane_ardupilot.jpg)

6. Test that the modes are mapped to the right transmitter switches by selecting each mode switch on your transmitter in turn, and check that the desired flight mode is activated (the text turns yellow on *QGroundControl* for the active mode).

All values are automatically saved as they are changed.

> **Note** The ArduCopter screenshot above shows a typical setup for a three position flight mode switch with an additional option of RTL being on a channel 7 switch. You can also setup 6 flight modes using two switches plus mixing on your transmitter. Scroll down to the center section of this [page](http://ardupilot.org/copter/docs/common-rc-transmitter-flight-mode-configuration.html#common-rc-transmitter-flight-mode-configuration) for tutorials on how to do that.

## PX4 Autopilot Flight Mode Setup

*PX4* (*QGroundControl*) supports assigning up to 6 flight modes to switch positions encoded in a single channel.

### Single-Channel Mode {#single_channel}

The single-channel selection mode allows you to specify a "mode" channel and select up to 6 flight modes that will be activated based on the PWM value of the channel. You can also separately specify channels for mapping a kill switch, return to launch mode, and offboard mode.

> **Note** In order to use approach you will first need to configure your *transmitter* to encode the physical positions of your mode switch(es) into a single channel. There is a video guide of how this is done for the popular *Taranis* transmitter [below](#taranis_setup) (check your documentation if you use a different transmitter).

To configure single-channel flight mode selection:

1. Turn on your RC transmitter.
2. Select the **Gear** icon (Vehicle Setup) in the top toolbar and then **Flight Modes** in the sidebar.
    
    ![Flight modes multi-channel](../../assets/setup/flight_modes_single_channel_px4.jpg)

3. Specify *Flight Mode Settings*:
    
    - Select the **Mode channel** (above this shown as Channel 5, but this will depend on your transmitter configuration). 
    - Select up to six **Flight Modes**.
4. Specify *Switch Settings*: 
    - Select the channels that you want to map to specific actions - e.g. *Return* mode, *Kill switch*, *offboard* mode, etc. (if you have spare switches and channels on your transmitter).
5. Test that the modes are mapped to the right transmitter switches: 
    - Check the *Channel Monitor* to confirm that the expected channel is changed by each switch.
    - Select each mode switch on your transmitter in turn, and check that the desired flight mode is activated (the text turns yellow on *QGroundControl* for the active mode).

All values are automatically saved as they are changed.

#### Video Example (including Transmitter Setup)

It is common to use the positions of a 2- and a 3-position switch on the transmitter to represent the 6 flight modes, and encode each combination of switches as a particular PWM value for the mode that will be sent on a single channel.

The video below shows how this is done with the *FrSky Taranis* transmitter (a very popular and highly recommended RC transmitter). The process involves assigning a "logical switch" to each combination of positions of the two real switches. Each logical switch is then assigned to a different PWM value on the same channel.

<a id="taranis_setup"></a>
The video then shows how to use *QGroundControl* to specify the mode channel and map modes to each of the 6 "slots". {% youtube %} http://www.youtube.com/watch?v=scqO7vbH2jo {% endyoutube %}