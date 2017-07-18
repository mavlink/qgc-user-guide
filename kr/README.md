# QGroundControl User Guide

[![Releases](https://img.shields.io/github/release/mavlink/QGroundControl.svg)](https://github.com/mavlink/QGroundControl/releases) [![Discuss](https://img.shields.io/badge/discuss-px4-ff69b4.svg)](http://discuss.px4.io/c/qgroundcontrol/qgroundcontrol-usage) [![Discuss](https://img.shields.io/badge/discuss-ardupilot-ff69b4.svg)](http://discuss.ardupilot.org/c/ground-control-software/qgroundcontrol) [![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/mavlink/qgroundcontrol?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) [![Slack](https://px4-slack.herokuapp.com/badge.svg)](http://slack.px4.io) 

QGroundControl를 이용하면 ArduPilot나 PX4기반 비행체에 대해서 완전한 비행 제어와 셋업이 가능합니다. QGroundControl의 목표는 유경험자들은 하이엔드 기능을 그리고 새로운 사용자는 쉽게 사용할 수 있도록 하는 것입니다.

**핵심 기능:**

* ArduPilot와 PX4 Pro 기반 비행체에 대한 완전한 셋업/설정 지원
* PX4와 ArduPilot을 실행하는 비행체에 대한 비행 지원(혹은 MAVLink 프로토콜을 사용해서 통신하는 다른 오토파일롯)
* 미션 플래닝으로 자동 비행
* 비행체 위치, 비행 경로, waypoint와 비행체 장치를 보여주는 비행 지도
* 디스플레이 오버레이로 비디오 스트리밍
* 여러 비행체 관리 지원
* QGC는 Windows, OS X, Linux 플랫폼, iOS, Android 장치에서 실행

![](../../images/quickstart/ConnectedVehicle.jpg)

> **노트** QGroundControl 사용자 가이드는 계속 작업 중입니다. 따라서 제공된 정보 중에 놓치거나 완료하지 않은 자료들이 있을 수 있습니다.

<span></span>
> **Tip** QGroundControl의 아키텍쳐와 개발 관련 정보는 [개발자 가이드](https://dev.qgroundcontrol.com/en/)를 참고하세요.
