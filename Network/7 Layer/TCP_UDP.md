# TCP와 UDP

![](../../../../../../../../var/folders/py/mt1_j5_j7pzb4jcv7tm58bfr0000gn/T/TemporaryItems/NSIRD_screencaptureui_5hI87s/스크린샷 2022-11-09 오전 12.42.39.png)

# TCP의 3-way HandShaking 역할
 
- 양쪽 모두 데이터가 전송 할 준비가 되었다는 것을 보장하고, 데이터 전달이 이루어지기 전 한 쪽이 다른 쪽이 준비가
되었다는 것을 알 수 있다.
- 양쪽 모두 상대편에 대한 초기 순차일련번호를 얻을 수 있도록 한다.

# 소켓 종류

스트림(TCP)

- 양방향으로 바이트 스트림을 전송, 연결 지향성
- 오류 수정, 전송처리, 흐름제어 보장
- 송신된 순서에 따라 중복되지 않게 데이터를 수신 -> 오버헤드가 발생
- 소량의 데이터보다 대량의 데이터 전송에 적합 -> TCP를 사용

데이터그램(UDP)

- 비연결형소켓
- 데이터의 크기에 제한이 있음
- 확실하게 전달이 보장되지 않음, 데이터가 손실되어도 오류가 발생하지 않음
- 실시간 멀티미디어 정보를 처리하기 위해 주로 사용 EX) 전화

# HTTP 통신과 SOCKET 통신의 비교

# HTTP 통신

- Client의 요청(Request)이 있을 때만 서버가 응답(Response)하여 해당 정보를 전송하고 곧바로 연결을 종료하는 방식

# HTTP 통신의 특징

- Client가 요청을 보내는 경우에만 Server가 응답하는 단방향 통신이다.
- Server로부터 응답을 받은 후에는 연결이 바로 종료된다.
- 실시간 연결이 아니고, 필요한 경우에만 Server로 요청을 보내는 상황에 유용하다.
- 요청을 보내 Server의 응답을 기다리는 어플리케이션의 개발에 주로 사용된다.

# SOCKET 통신

- Server와 Client가 특정 Port를 통해 실시간으로 양방향 통신을 하는 방식

# SOCKET 통신의 특징

- Server와 Client가 계속 연결을 유지하는 양방향 통신이다.
- Server와 Client가 실시간으로 데이터를 주고받는 상황이 필요한 경우에 사용한다.
- 실시간 동영상 Streaming이나 온라인 게임 등과 같은 경우에 자주 사용된다.