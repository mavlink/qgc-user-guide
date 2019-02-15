# Resume Mission failures

The process of resuming a mission after a battery swap is a fairly complex process within QGC. There tend to be to area which go wrong:

* The Resume Mission dialog doesn't display when it should and you are just left with a Start Mission slider.
* The new mission generated from Resume Mission is not quite correct with respect to recration of waypoints and/or camera commands.

In order for the QGroundControl development team to debug these issues a specific set of information is needed in any Issue entered against Resume Mission.

## Required Information for Resume Mission Dialog problems
* Restart QGC
* Turn on logging for GuidedActionsControllerLog.
* Make sure you have telemetry logging turned on.
* Start the mission.
* Fly till you need a battery swap or possibly manually RTL from the middle of the middle of the mission. In some cases a manual RTL will not reproduce the problem though.
* Once the vehicle lands and disarms you should get the Resume Mission dialog.
* At this point the Resume Mission dialog should display. If not there is a possible bug in QGC.
* Save the Console Log to a file.
* Place the Console Log, Telemetry Log and Plan file someplace which you can link to in the Issue.
* Create the Issue with details and links to all three files.

## Required Information for Resume Mission Generation problems
* Restart QGC
* Turn on logging for GuidedActionsControllerLog.
* Make sure you have telemetry logging turned on.
* Start the mission.
* Fly till you need a battery swap or possibly manually RTL from the middle of the middle of the mission. In some cases a manual RTL will not reproduce the problem though.
* Once the vehicle lands and disarms you should get the Resume Mission dialog.
* Click Resume Mission
* The new mission should be generated.
* Go to Plan
* Select Download from the Sync menu.
* Save the Modified Plan to a file.
* Save the Console Log to a file.
* Place the Console Log, Telemetry Log, Original Plan file and Modified Plan file someplace which you can link to in the Issue.
* Create the Issue with details and links to all four files.