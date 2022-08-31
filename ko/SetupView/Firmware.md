# 펌웨어 로딩

*QGroundControl* **데스크탑** 버전을 이용하여 Pixhawk 비행 컨트롤러에 [PX4 Pro](http://px4.io/) 또는 [ArduPilot](http://ardupilot.com) 펌웨어를 설치할 수 있습니다. QGroundControl은 선택한 자동조종장치의 최신 안정적인 버전을 기본적으로 설치하며, 베타 버전, 일일 빌드 버전 또는 사용자 지정 버전의 펌웨어를 설치할 수 있습니다.

*QGroundControl*은 SiK 라디오 및 PX4 Flow 기기용 펌웨어도 설치할 수 있습니다.

> **Caution** 펌웨어 업로드는 현재 *QGroundControl*의 태블릿이나 스마트폰 버전에서는 사용할 수 없습니다.

## 펌웨어 업데이트를 위한 장치 연결

> **Caution** </strong>펌웨어를 설치 전에 기체에 모든 USB (직접 또는 원격 측정 라디오) 연결은 *해제*하여야 합니다. 기체에 배터리를 연결하지 *않아야* 합니다.

1. First select the **Gear** icon (*Vehicle Setup*) in the top toolbar and then **Firmware** in the sidebar.
    
    ![Firmware disconnected](../../assets/setup/firmware/firmware_disconnected.jpg)

2. Connect your device (Pixhawk, SiK Radio, PX4 Flow) directly to your computer via USB.
    
    > **Note** Connect directly to a powered USB port on your machine (do not connect through a USB hub).

## Select Firmware to Load

Once the device is connected you can choose which firmware to load (*QGroundControl* presents sensible options based on the connected hardware).

1. For a Pixhawk-compatible board choose either **PX4 Flight Stack vX.X.X Stable Release** or **ArduPilot Flight Stack** radio buttons to download the *current stable release*.
    
    ![Select PX4](../../assets/setup/firmware/firmware_select_default_px4.jpg)
    
    If you select *ArduPilot* you will also have to choose the specific firmware and the type of vehicle (as shown below).
    
    ![Select ArduPilot](../../assets/setup/firmware/firmware_selection_ardupilot.jpg)

2. Check **Advanced settings** to select specific developer releases or install firmware from your local file system.
    
    ![ArduPilot - Advanced Settings](../../assets/setup/firmware/firmware_selection_advanced_settings.jpg)

## Update the firmware

1. Click the **OK** button to start the update.
    
    The firmware will then proceed through a number of upgrade steps (downloading new firmware, erasing old firmware etc.). Each step is printed to the screen and overall progress is displayed on a progress bar.
    
    ![Firmware Upgrade Complete](../../assets/setup/firmware/firmware_upgrade_complete.jpg)

Once the firmware has finished loading the device/vehicle will reboot and reconnect. Next you will need to configure the [airframe](../SetupView/Airframe.md) (and then sensors, radio, etc.)