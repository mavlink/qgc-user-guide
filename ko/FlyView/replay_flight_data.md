# 비행 데이터 재생

> **Warning** 이 기능은 주로 **자동 조종 장치 개발자**와 **자동차 제작자**를 위한 것입니다. 데스크톱 빌드(Windows, Linux, Mac OS)에서만 지원됩니다.

*비행 데이터 재생* 기능을 사용하면 사용자가 원격 측정 로그를 재생하여 과거 또는 문제가 있는 비행을 검토할 수 있습니다. 비행을 시작, 일시 중지, 중지, 다시 시작할 수 있습니다.

> **Note** *QGroundControl*은 비행 재생을 활성 연결처럼 취급합니다. 재생을 일시 중지/중지하면 지상국에서 "통신 끊김"을 보고하고 연결이 끊기거나 추가 메시지가 표시될 때까지 기다립니다.

비행을 재생하려면:
1. 활성화된 연결을 모두 끊습니다.
1. **애플리케이션 설정 > 일반 > 플라이 뷰**
1. **텔레메트리 로그 재생 상태 표시줄 표시**를 선택하여 화면 하단의 비행 재생 표시줄을 토글합니다.

   ![Toggle Flight Replay](../../assets/fly/flight_replay/flight_replay_toggle.jpg)
1. Select the **Load Telemetry Log** button in the bar to display a *file selection* dialog.
   - Choose a log file to replay from the available telemetry logs.
   - *QGroundControl* will immediately start playing the log.
1. When a log is loaded you can use the:
   - **Pause/Play** button to pause and restart playing.
   - *Slider* to drag to a new position in the log.
   - *Rate* selector to choose the playback speed.
1. To stop replay (i.e. to load a new file to replay), first pause the flight, and then select **Disconnect** (when it appears). After disconnecting, the **Load Telemetry Log** button will be displayed.

> **Tip** You can inspect the running replay in more detail using the [MAVLink Inspector](../analyze_view/mavlink_inspector.md).
