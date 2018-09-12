# Corridor Scan (Plan Pattern)

A corridor scan allows you to create a flight pattern that follows a poly-line. 
This can be used to, for example, survey a road.

![Corridor Scan](../../assets/Plan/corridor_scan.jpg)

You can specify the path as well as the specifications for the width of the corridor and camera settings appropriate for creating geotagged images.

## Creating a Scan

To create a corridor scan:
1. Open [PlanView](../PlanView/PlanView.md) *Plan Tools*).
1. Choose the *Pattern Tool* from the *Plan Tools* and then select *Corridor Scan*.

   ![Corridor Scan](../../assets/Plan/corridor_scan_menu.jpg)
   
   This will add a corridor to the map, and a *Corridor Scan* item to the mission list (on the right).
1. On the map drag the ends of the corridor to the start and end positions of the scan, respectively.
1. Click the `(+)` symbol at the centre of a line to create a new vertix.
   The new vertix can then be dragged into position to follow the path of the desired corridor.

The corridor scan settings are covered in the next section.

## Settings

The corridor scan can be further configured in the associated mission item (in the mission item list on the right hand side of the Plan View). 

### Camera

Camera triggering behaviour depends on the camera/camera settings.
You can select an existing camera or manually enter the settings.
The list of available cameras (QGC 3.4) is given below.

![Corridor Scan - Select Camera](../../assets/Plan/corridor_scan_settings_camera_select.jpg)

#### Known Camera 
Selecting a known camera from the option dropdown allows you to generate a grid pattern based on the camera's specifications.

![Corridor Scan - Camera Settings Canon SX260](../../assets/Plan/corridor_scan_settings_camera_canon_sx260.jpg)

The configurable options are:

- **Landscape/Portrait** - Camera orientation relative to the "normal" orientation of the vehicle.
- **Image Overap** - Overlap between each image.
- **Altitude** - Survey altitude. 
  The ground resolution will be calculated and shown for the specified altitude.
- **Ground resolution** - Ground resolution you want for each image. 
  The altitude required to achieve this resolution is calculated and shown.

#### Manual Camera 

The manual camera option allows you to specify desired survey height triggering for your camera.

![Corridor Scan - Manual Camera Settings](../../assets/Plan/corridor_scan_settings_camera_manual.jpg)

The configurable options are:

- **Altitude** - Survey altitude.
- **Trigger Distance** - The distance over ground for each camera shot.
- **Spacing** - TBD.


### Corridor

![Corridor Scan - Corridor Settings](../../assets/Plan/corridor_scan_settings_corridor.jpg)

The configurable options are:

- **Width** - Set the width of the scan around the polyline that defines the path.
- **Turnaround dist** - TBD.
- **Take images in turnarounds** - Check to enable image capture a turnaround points.
- **Relative altitude** - Check to TBD.
- **Rotate entry point** - Press button to swap the start and end point of the corridor scan.


### Terrain Following

By default a flying vehicle will follow the corridor path at a fixed altitude. 
Enabling *Terrain Following* makes the vehicle maintain a constant height relative to ground.

![Corridor Scan - Terrain Following Settings](../../assets/Plan/corridor_scan_settings_terrain.jpg)

The configurable options are:

- **Vehicle follows terrain** - Check to enable terrain following (and display the following options).
- **Tolerance** - The accepted deviation in altitude from the target altitude.
- **Max Climb Rate** - Maximum climb rate when following terrain.
- **Max Descent Rate** - Maximum descent rate when following terrain.

### Statistics

The *Statistics* section shows the calculated survey area, photo interval, photo spacing and planned photo count.

![Corridor Scan - Statistics](../../assets/Plan/corridor_scan_settings_statistics.jpg)

