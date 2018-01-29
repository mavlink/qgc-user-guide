# Plan - Structure Scan

A structure scan allows you to create a grid flight pattern which captures images over vertical surfaces. These are tpypically used for the visual inspection or creation of 3d models of structures.

Structure Scan is available to insert into a mission from the Pattern tool.

![](../../images/plan/StructureScan.jpg)

In green you can see the polygon show which represent the structure. In white you can see the flight path for the vehicle. You can also fly circular structure scans by change the polygon to a circle using the center tool.

## Camera based scan
The settings for the scan can be based off of the specifications of the camera on the vehicle. By using the option you can also specify the resolution of the images for the structure surface. You do this by selecting a camera from the list or selecting Custom Camera to provide you own camera specs.

For camera based scans the camera is always pointed directly at the right angles to the surface which it is capturing images for.

<img src="../../images/plan/StructureScanCamera.jpg" style="width: 150px;"/>

### Structure information

* Base layer alt - This is used to specify the bottom of the lowest layer of the scan.
* Structure height - This id used to specify the height of the structure.

Using these two values, the vehicle will fly a pattern such images fully cover the structure starting from "Base layer alt" and then going up "Structure height" amount.

## Manual scan
A manual scan allows you to specify the various distances and heights associated with a structure scan yourself. You select Manual from the list for a manual scan.

<img src="../../images/plan/StructureScanManual.jpg" style="width: 150px;"/>

* Scan Distance - The amount of distance to fly away from the structure.
* Bottom Layer Alt - The bottom altitude of the first layer.
* Layer Height - The height of each subsequent layer.
* Layers - The number of layers to generate.
* Trigger Distance - The distance between each camera trigger.
* Gimbal - Gimbal angles you want to use for the scan.