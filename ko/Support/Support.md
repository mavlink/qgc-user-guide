# Support

This user guide is meant to be the main provider of support for *QGroundControl*. If you find incorrect or missing information please report an [Issue](https://github.com/mavlink/qgc-user-guide/issues).

*Questions* about how to use *QGroundControl* should be raised in the discussion server for the associated flight stack:

- [PX4 Flight Stack](http://discuss.px4.io/c/qgroundcontrol/qgroundcontrol-usage) (discuss.px4.io).
- [ArduPilot Flight Stack](http://discuss.ardupilot.org/c/ground-control-software/qgroundcontrol) (discuss.ardupilot.org).

## Developer Chat {#developer_chat}

*QGroundControl* developers (and many regular/deeply-involved users) can be found on the [#QGroundControl Slack channel](https://px4.slack.com/).

> **Tip** This channel is a good place to keep up to date with the latest and greatest changes in *QGroundControl*.

<span></span>

> **Note** The *QGroundControl* Gitter channel will be discontinued in March 2020.

## GitHub Issues

Issues are used to track bugs against *QGroundControl* as well as feature requests for later versions. The current list of issues can be found on [GitHub here](https://github.com/mavlink/qgroundcontrol/issues).

> **Note** Please contact our developers using the [IM](#developer_chat) channels **before** creating GitHub issues!

### Feature Requests

Feature Requests should first be discussed on a [developer IM](#developer_chat) channel. The developer team will direct you to create a feature request on Github if necessary (or refer you to the appropriate existing feature).

### Reporting Bugs

Bug reports should first be discussed on a [developer IM](#developer_chat) channel (there are many cases where something that seems like a bug is actually a vehicle setup problem). The developer team will direct you to create an issue if necessary.

If you are directed to create an issue, please provide all information needed to reproduce the problem (OS, *QGroundControl* version/build, Autopilot version/release etc). The sections below explain how to get additional information that can help with debugging issues.

#### Console Logging

*Console Logs* can be helpful when diagnosing *QGroundControl* problems. For more information see: [Console Logging](../SettingsView/console_logging.md).

#### Reporting Crashes from Windows Builds

When QGC crashes a crash dump file will be place in the Users LocalAppData directory. To navigate to that directory use the Start/Run command. You can bring this up window WinKey+R. Type into that ```%localappdata%``` for Open and click Ok. Crash dumps will be in a ```QGCCrashDumps``` folder in that directory. You should find a new **.dmp** file there. Add a link to that file in a GitHub Issue when reporting you problem.

#### Reporting Hangs from Windows Builds

If Windows is telling you the *QGroundControl program is unresponsive* use the following steps to report the hang:

1. Open *Task Manager* (right-click TaskBar, select **Task Manager**)
2. Switch to the Processes tab and local **qgroundcontrol.exe**
3. Right-click on **groundcontrol.exe** and select **Create Dump File**
4. Place the dump file in a public location
5. Add a link to the **.dmp** file and above details in the GitHub issue.

## Troubleshooting

Troubleshooting information is provided in two topics:

- [QGC Installation/Configuration Problems](../Support/troubleshooting_qgc.md) - problems/solutions related to **running** *QGroundControl* on the host computer.
- [QGC/Vehicle Interaction Problems](../Support/CommonProblems.md) - problems/solutions related to **using** *QGroundControl* to interact with a vehicle.

## Help Improve these Docs!

Just like *QGroundControl* itself, the user guide is an open source, user created and supported GitBook. We welcome [Pull Requests](https://github.com/mavlink/qgc-user-guide/pulls) against the guide for fixes and/or updates.