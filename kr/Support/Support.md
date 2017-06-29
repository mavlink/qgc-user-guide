# Support

이 사용자 가이드는 QGroundControl이 지원하는 기능을 소개합니다. 만약 중요한 정보를 빼먹었거나 정확하지 않은 정보가 있다면 [Issue](https://github.com/mavlink/qgc-user-guide/issues)로 보내주세요.

QGroundControl 관련 질문 및 문제 리포팅은 [QGroundControl Usage Category here](http://discuss.px4.io/c/qgroundcontrol/qgroundcontrol-usage)을 이용해 주세요.

## Console Logging

![Console logging](../../images/support/Console.jpg)

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



## GitHub Issues
추후 버전에 대한 기능 요청뿐만 아니라 QGroundControl의 버그를 추적하는데 Issues를 사용합니다.
현재 Issues 목록은 https://github.com/mavlink/qgroundcontrol/issues 에서 찾을 수 있습니다.

아래에서 설명하는 Gitter 채널을 사용해서 먼저 개발자와 연락하고 Issues를 넣도록 하세요.

### 버그 리포팅
먼저 Gitter 채널에서 버그에 관한 질문을 하는 것이 가장 좋습니다. 가끔은 버그처럼 보이지만 실제로는 비행체 셋업과 관련된 문제인 경우가 많이 있습니다. 이렇게 해도 계속 된다면 위에 링크에 들어가서 Github Issue를 넣어도 됩니다.

### 기능 요청
기능 요청도 우선 Gitter 채널을 통해 해당 기능이 정말 없는지를 확인하도록 합니다. 이런 방식으로 실제로 있는데 여러분이 찾이 못한 기능을 찾도록 도움을 얻을 수 있습니다. 만약 해당 기능이 정말 없다면 위 링크의 Github Issue에 들어가서 요청을 하면 됩니다.


## QGroundControl 사용자 돕기

QGroundControl와 같이 사용자 가이드도 오픈소스입니다. [Pull Requests](https://github.com/mavlink/qgc-user-guide/pulls)를 통해 가이드를 수정하고 업데이트하는 것을 환영합니다.
