# Support

This user guide is meant to be the main provider of support for *QGroundControl*. If you find incorrect or missing information please report an [Issue](https://github.com/mavlink/qgc-user-guide/issues).

Questions about *QGroundControl* should be raised in the associated flight stack's discussion server at the links below:
* [PX4 Flight Stack](http://discuss.px4.io/c/qgroundcontrol/qgroundcontrol-usage) (discuss.px4.io).
* [ArduPilot Flight Stack](http://discuss.ardupilot.org/c/ground-control-software/qgroundcontrol) (discuss.ardupilot.org).


## Console Logging

![Console logging](../../images/support/Console.jpg)

The Console can be helpful tool for diagnosing *QGroundControl* problems. It can be found in the [SettingsView](../SettingsView/SettingsView.md). It allows you turn turn on/off the logging options available in *QGroundControl*. Click the "Set Logging" button to select logging options.

### Commonly used logging options

* `LinkManagerLog`, `MultiVehicleManagerLog` - Debug connection problems.
* `LinkManagerVerboseLog` - Very noisy connection problem debugging. Continuous output of available serial ports.
* `FirmwareUpgradeLog` - Debug firmware flash issues.
* `ParameterLoaderLog` - Debug parameter load problems.
* `ParameterLoaderVerboseLog` - Debug parameter load problems with full trace of parameters coming/going/in system.
* `MissionManagerLog` - Debug mission protocol issues.
* `RadioComponentControllerLog` - Debug Radio calibration issues.

### Logging from the command line

An alternate mechanism for logging is using the --logging command line option. This is handy if you are trying to get logs from a situation where *QGroundControl* crashes.

How you do this and where the traces are output vary by OS:

  * Windows
    * You must open a command prompt, change directory to the **qgroundcontrol.exe** location, and run it from there:
      ```bash
      cd "\Program Files (x86)\qgroundcontrol"
      qgroundcontrol --logging:full</code>
      ```
    * When *QGroundControl* starts you should see a separate console window open which will have the log output
  * OSX
    * You must run *QGroundControl* from Terminal. The Terminal app is located in Applications/Utilities. Once Terminal is open paste the following into it:
      ```bash
      cd /Applications/qgroundcontrol.app/Contents/MacOS/
      ./qgroundcontrol --logging:full
      ```
    * Log traces will output to the Terminal window.
  * Linux
    * 
    ```bash
    ./qgroundcontrol-start.sh --logging:full
    ```
    * Log traces will output to the shell you are running from.


## Developer Chat

The *QGroundControl* developers as well as many *QGroundControl* users can be found on the *QGroundControl* [Gitter](https://gitter.im/mavlink/qgroundcontrol) channel. If you are a heavy user of *QGroundControl* and want to keep up to date on the latest information or help with *QGroundControl* we suggest monitoring that channel.



## GitHub Issues

Issues are used to track bugs against *QGroundControl* as well as feature requests for later versions. The current list of issues can be found on [GitHub here](https://github.com/mavlink/qgroundcontrol/issues).

Please don't enter Issues directly into GitHub without first contacting developers using the [Gitter](https://gitter.im/mavlink/qgroundcontrol) channel as described below.

### Reporting Bugs

It is best to first ask any question around a bug on the Gitter channel. There are many cases where something that seems like a bug is actually a vehicle setup problem. After that if directed to you can enter a GitHub Issue for the bug using the link above.

### Feature Requests

Feature Requests should also first go through the Gitter channel to determine whether the feature is actually missing. That way you may be directed to a feature you haven't found which covers what you were looking for. If the feature is truly not available, then you can enter a GitHub Issue for the request using the link above.


## Help out your fellow QGroundControl users

Just like *QGroundControl* itself, the user guide is an open source, user created and supported GitBook. We welcome [Pull Requests](https://github.com/mavlink/qgc-user-guide/pulls) against the guide for fixes and/or updates.
