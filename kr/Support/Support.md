# Support

이 사용자 가이드는 QGroundControl이 지원하는 기능을 소개합니다. 만약 중요한 정보를 빼먹었거나 정확하지 않은 정보가 있다면 [Issue](https://github.com/mavlink/qgc-user-guide/issues)로 보내주세요.

QGroundControl 관련 질문 및 문제 리포팅은 [QGroundControl Google Group](http://groups.google.com/group/qgroundcontrol)을 이용해 주세요.

## Console Logging

![](../../images/support/Console.jpg)

콘솔은 QGroundControl 문제를 진단하는 유용한 도구로 Settings View에 있습니다. QGroundControl에서 유효한 logging 옵션을 켜고/끄기가 가능합니다. "Set Logging" 버튼을 클릭해서 logging 옵션을 선택합니다.

### 일반적인 logging 옵션

* LinkManagerLog, MultiVehicleManagerLog - 연결 문제를 디버깅
* LinkManagerVerboseLog - 매우 복잡한 연결 문제 디버깅. 사용 가능한 시리얼 포트 연속 출력.
* FirmwareUpgradeLog - 펌웨어 flash 이슈 디버깅
* ParameterLoaderLog - 파라미터 로드 문제 디버깅
* ParameterLoaderVerboseLog - 시스템에 대해서 입력/출력되는 파라미터 전체를 추적하여 로드 문제를 디버깅
* MissionManagerLog - 미션 컨트롤 이슈 디버깅
* RadioComponentControllerLog - 라디오 칼리브레이션 이슈 디버깅

### command line으로 logging

로깅에 대한 다른 대안은 --logging command line 옵션입니다. QGroundControl이 crash되는 상황에서 로그를 얻고자할 때 유용합니다.

실행 방법과 trace가 출력하는 부분은 OS에 따라 달라진다 :

  * Windows
    * 커맨드 프롬프트를 열고 qgroundcontrol.exe가 있는 위치로 디렉토리를 변경합니다. 그리고 실행합니다.:
    * <code>cd "\Program Files (x86)\qgroundcontrol"
qgroundcontrol --logging:full</code>
  * QGC가 시작되면 별도의 콘솔 윈도우가 열리고 log가 출력되는 것을 보게 됩니다.
  * OSX
    * QGC를 터미널에서 실행합니다. Terminal app은 Applications/Utilities에 위치하고 있습니다. 일단 Terminal이 열리면 다음을 복사해서 붙여넣기합니다.:
    * <code>cd /Applications/qgroundcontrol.app/Contents/MacOS/
./qgroundcontrol --logging:full</code>
    * Log traces는 Terminal 윈도우에 출력합니다.
  * Linux
    * <code>./qgroundcontrol-start.sh --logging:full</code>
    * 현재 실행하고 있는 shell에 Log traces가 출력됩니다.

## Developer Chat

다양한 QGroundControl 사용자와 QGroundControl 개발자를 QGroundControl [Gitter](https://gitter.im/mavlink/qgroundcontrol)에서 만날 수 있습니다. 만약 QGroundControl에 관련된 최신 정보를 얻고자 한다면 이 채널을 주의깊게 지켜보는 것을 추천합니다.

## QGroundControl 사용자 돕기

QGroundControl와 같이 사용자 가이드도 오픈소스입니다. [Pull Requests](https://github.com/mavlink/qgc-user-guide/pulls)를 통해 가이드를 수정하고 업데이트하는 것을 환영합니다.
