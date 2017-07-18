## Stable Version 3.2 (Current)

This topic contains a high level and *non-exhaustive* list of new features added to *QGroundControl* in version 3.2. More detailed release notes can be found [here](../releases/stable_v3.2_long.md).

* **Settings**
	* **File Save path** - Specify a save path for all files used by QGC.
	* **Telemetry log auto-save** - Telemetry logs are now automatically saved without prompting.
	* **AutoLoad Plans** - Used to automatically load a Plan onto a vehicle when it first connects.
	* **RTK GPS** - Specify the Survey in accuracy and Minimum observation duration.

* **Setup**
	* ArduPilot only
		* **Pre-Flight Barometer and Airspeed calibration** - Now supported
		* **Copy RC Trims** - Now supported

* **Plan View**
	* **Plan files** - Missions are now saved as .plan files which include the mission, geo-fence and rally points.
	* **Plan Toolbar** - New toolbar which shows you mission statistics and Upload button.
	* **Mission Start** - Allows you to specify values such as flight speed and camera settings to start the mission with.
	* **New Waypoint features** - Adjust heading and flight speed for each waypoint as well as camera settings.
	* **Visual Gimbal direction** - Gimbal direction is shown on waypoint indicators.
	* **Pattern tool** - Allows you to add complex patterns to a mission.
		* Fixed Wing Landing (new)
		* Survey (many new features)
	* **Fixed Wing Landing Pattern** - Adds a landing pattern for fixed wings to your mission.
	* **Survey** - New features
		* **Take Images in Turnarounds** - Specify whether to take images through entire survey or just within each transect segment.
		* **Hover and Capture** - Stop vehicle at each image location and take photo.
		* **Refly at 90 degree offset** - Add additional pattern at 90 degree offset to original so get better image coverage.
		* **Entry location** - Specify entry point for survey.
		* **Polygon editing** - Simple on screen mechanism to drag, resize, add/remove points. Much better touch support.

* **Fly View**
	* **Arm/Disarm** - Available from toolbar.
	* **Guided Actions** - New action toolbar on the left. Supports:
		* Takeoff
		* Land
		* RTL
		* Pause
		* Start Mission
		* Resume Mission - after battery change
		* Change Altitude
		* Land Abort
		* Set Waypoint
		* Goto Location	
	* **Remove mission after vehicle lands** - Prompt to remove mission from vehicle after landing.
	* **Flight Time** - Flight time is shown in instrument panel.
	* **Multi-Vehicle View** - Better control of multiple vehicles.

* **Analyze View** - New
	* **Log Download**  - Moved to Analyze view from menu
	* **Mavlink Console** - NSH shell access

* **Support for third-party customized QGroundControl**
	* Standard QGC supports multiple firmware types and multiple vehicle types. There is now support in QGC which allows a third-party to create their own custom version of QGC which is targeted specifically to their custom vehicle. They can then release their own version of QGC with their vehicle.
