# Support

This user guide is meant to be the main provider of support for *QGroundControl*. If you find incorrect or missing information please report an [Issue](https://github.com/mavlink/qgc-user-guide/issues).

*Questions* about how to use *QGroundControl* should be raised in the discussion forum for the associated flight stack:

- [PX4 Pro Flight Stack](http://discuss.px4.io/c/qgroundcontrol/qgroundcontrol-usage) (discuss.px4.io).
- [ArduPilot Flight Stack](http://discuss.ardupilot.org/c/ground-control-software/qgroundcontrol) (discuss.ardupilot.org).

These forums are also the best place to start discussions on bugs/problems you are having with *QGroundControl* and or feature requests you would like to make. From there you may be directed to entering information in a GitHub Issue for further resolution.

### Developer Chat {#developer_chat}

*QGroundControl* developers (and many regular/deeply-involved users) can be found on the [#QGroundControl Slack channel](https://px4.slack.com/).

## GitHub Issues

Issues are used to track bugs against *QGroundControl* as well as feature requests for later versions. The current list of issues can be found on [GitHub here](https://github.com/mavlink/qgroundcontrol/issues).

> **Note** Please contact our developers using the support forums **before** creating GitHub issues for either bugs or feature requests.

### Reporting Bugs

If you are directed to create an issue, please use the "Bug report" template and provide all information specified in the template.

##### Reporting Crashes from Windows Builds

When QGC crashes a crash dump file will be place in the Users LocalAppData directory. To navigate to that directory use the Start/Run command. You can bring this up window WinKey+R. Type into that ```%localappdata%``` for Open and click Ok. Crash dumps will be in a ```QGCCrashDumps``` folder in that directory. You should find a new **.dmp** file there. Add a link to that file in a GitHub Issue when reporting you problem.

##### Reporting Hangs from Windows Builds

If Windows is telling you the *QGroundControl program is unresponsive* use the following steps to report the hang:

1. Open *Task Manager* (right-click TaskBar, select **Task Manager**)
2. Switch to the Processes tab and local **qgroundcontrol.exe**
3. Right-click on **groundcontrol.exe** and select **Create Dump File**
4. Place the dump file in a public location
5. Add a link to the **.dmp** file and above details in the GitHub issue.

### Feature Requests

If you are directed to create a feature request after discussion on support forums please use the "Feature request" template which has some helpful information on required details.

## Troubleshooting

Troubleshooting information is provided in two topics:

- [QGC Installation/Configuration Problems](../Support/troubleshooting_qgc.md) - problems/solutions related to **running** *QGroundControl* on the host computer.
- [QGC/Vehicle Interaction Problems](../Support/CommonProblems.md) - problems/solutions related to **using** *QGroundControl* to interact with a vehicle.

### Console Logging

*Console Logs* can be helpful when diagnosing *QGroundControl* problems. For more information see: [Console Logging](../SettingsView/console_logging.md).

## Help Improve these Docs!

Just like *QGroundControl* itself, the user guide is an open source, user created and supported GitBook. We welcome [Pull Requests](https://github.com/mavlink/qgc-user-guide/pulls) against the guide for fixes and/or updates.