# 탐사 (패턴 계획)

탐사 기능으로 다각형 영역에 그리드 비행 패턴을 생성할 수 있습니다. 임의의 다각형, 그리드의 각도 및 기타 속성, 지오태깅된 이미지 생성에 적합한 카메라 설정을 지정할 수 있습니다.

> **Warning** 조사 지역에 고도 변화가 심한 경우 [지형 추적](#terrain)을 활성화하는 것이 좋습니다.
> 
> 카메라 사양을 사용하여 측량을 계획할 때 측량 영역 아래의 지면은 평평한 것으로 가정합니다. 즉, 이륙 홈 위치와 동일한 고도에 있습니다. 측량 아래의 지면 고도가 홈 위치보다 높거나 낮으면, 이미지의 효과적인 중첩이 계산된 것보다 (각각) 더 적거나 많을 것입니다. 조사 지역 아래의 지상 고도가 홈 위치보다 *상당히* 높으면 차량이 지상 장애물로 날아가도록 하는 잘못된 임무 경로를 계획할 수 있습니다.
> 
> 지형 추적을 사용하면 측량이 지형 위의 원하는 고도와 더 가깝게 일치하도록 하고 지면 수준에 너무 가까운 임무를 계획할 가능성을 줄입니다.

![Survey](../../assets/plan/survey/survey.jpg)

## 탐사 생성

탐사를 생성하려면:

1. [계획 뷰](../PlanView/PlanView.md)에서 *계획 도구*를 엽니다.
2. *계획 도구*에서 *패턴 도구*를 선택한 다음 *탐사*를 선택합니다.
  
  ![Survey Menu](../../assets/plan/survey/survey_menu.jpg)
  
  그러면 지도에 설문조사 그리드가 추가되고 임무 목록(오른쪽)에 *설문조사* 항목이 추가됩니다.

3. 지도에서 정점을 끌어 다각형의 모양을 변경합니다.

4. 기존 정점 사이의 `(+)` 기호를 클릭하여 새 정점을 만듭니다. 그런 다음 새 정점을 새 위치로 끌어서 수정할 수 있습니다.

탐사에 관련된 설정은 다음 섹션에서 설명합니다.

## 설정

설문조사는 연결된 미션 항목(*플랜 보기*의 오른쪽에 있는 미션 항목 목록)에서 추가하여 설정할 수 있습니다.

### 카메라

카메라 트리거 동작은 카메라/카메라 설정에 따라 차이가 납니다. 기존 카메라, 사용자 지정 카메라를 선택하거나 수동으로 설정을 입력할 수 있습니다. 사용 가능한 카메라(QGC 3.4) 목록은 아래와 같습니다.

![Survey - Camera Select](../../assets/plan/survey/survey_camera_select.jpg)

#### 알려진 카메라 {#known_camera}

Selecting a known camera from the option dropdown generates a grid pattern based on the camera capabilities.

![Survey - Camera Sony](../../assets/plan/survey/survey_camera_sony.jpg)

The default settings can be tuned for your survey using the configuration options:

- **Landscape/Portrait** - Camera orientation relative to the "normal" orientation of the vehicle.
- **Overlap** - Overlap between each image capture. This can be configured separately for when flying along grid lines or across them.
- Select one of: 
  - **Altitude** - Survey altitude (ground resolution will be calculated/displayed for this altitude).
  - **Ground resolution** - Ground resolution for each image (altitude required to achieve this resolution calculated and shown).

#### Custom Camera {#custom_camera}

Selecting the custom camera option allows you to specify the settings for a new camera in a similar way to a known camera.

![Survey - Custom Camera](../../assets/plan/survey/survey_camera_custom.jpg)

The camera-specific settings are:

- **Sensor width/height** - The size of the image sensor of the camera.
- **Image width/height** - The resolution of the image captured by the camera.
- **Focal Length** - The focal length of the camera lens.

The remaining settings are the same as for a [known camera](#known_camera).

#### Manual Camera

The manual camera option allows you to specify desired survey height, trigger interval and appropriate grid spacing for your camera.

![Survey - Manual Camera Settings](../../assets/plan/survey/survey_camera_manual.jpg)

The configurable options are:

- **Altitude** - Survey altitude to fly the whole grid.
- **Trigger Distance** - The distance over ground between each camera shot.
- **Spacing** - Distance between adjacent grid (flight path) lines across the corridor.

### Transects

The *Transects* section is used for grid settings that are independent of the camera used.

![Survey - Transects](../../assets/plan/survey/survey_transects.jpg)

The configurable options are:

- **Angle** - The angle of the grid lines, relative to North. ![Survey - Angle](../../assets/plan/survey/survey_transects_angle.jpg)
- **Turnaround dist** - Amount of additional distance to add outside the survey area for vehicle turn around.
- **Rotate Entry Point** - Press button to swap the start and end point of the survey.
- **Hover and capture image** - Hover to capture images (multicopter only).
- **Refly at 90 degree offset** - Check to refly the whole mission at a 90 degree offset. ![Survey - Fly Offset](../../assets/plan/survey/survey_transects_offset.jpg)
- **Images in turnarounds** - Check to take images when turning
- **Relative altitude** - Check to make specified altitudes relative to home (if unchecked they are AMSL).

### Terrain

By default, a flying vehicle will follow the survey path at a fixed altitude. Enabling *Terrain Following* makes the vehicle maintain a constant height relative to ground.

![Survey - Terrain Following Settings](../../assets/plan/survey/survey_terrain.jpg)

> **Note** Terrain following uses terrain heights queried from *AirMap* servers.

The configurable options are:

- **Vehicle follows terrain** - Check to enable terrain following (and display the following options). 
  - **Tolerance** - The accepted deviation in altitude from the target altitude.
  - **Max Climb Rate** - Maximum climb rate when following terrain.
  - **Max Descent Rate** - Maximum descent rate when following terrain.

### Statistics

The *Statistics* section shows the calculated survey area, photo interval, photo spacing and planned photo count.

![Survey - Statistics](../../assets/plan/survey/survey_statistics.jpg)