# 멀티스레드

# 프로세스
- 운영체제에서는 실행 중인 하나의 애플리케이션을 프로세스라고 부릅니다.
- 사용자가 애플리케이션을 실행하면 운영체제로부터 실행에 필요한 메모리를 할당받아 애플리케이션의 코드를 실행하는데 이것이 프로세스입니다.

# 멀티 프로세스
- 하나의 애플리케이션은 멀티 프로세스를 만들기도 합니다. 예를 들어 메모장 애플리케이션을 2개 실행했다면 2개의 메모장 프로세스가 생성된 것입니다.

# 스레드
- 운영체제는 두 가지 이상의 작업을 동시에 처리하는 멀티 태스킹을 할 수 있도록 CPU 및 메모리 자원을 프로세스마다 적절히 할당, 병렬로 실행
- 예를 들어, 워드로 문서 작업을 하면서 동시에 윈도우 미디어 플레이어로 음악을 들을 수 있습니다.
- 사전적 의미로 한 가닥의 실, 한 가지 작업을 실행하기 위해 순차적으로 실행할 코드를 실처럼 이어놓아서 유래된 이름.
- 하나의 스레드는 하나의 코드의 실행 흐름이기 떼문에 한 프로세스 내에 스레드가 2개라면 2개의 코드 실행 흐름이 생긴다는 뜻

# 스레드의 개념
- 프로세스는 두 가지 특성인 자원과 제어로 구분할 수 있다.
- 이 중 제어만 분리한 실해 단위를 스레드라고 하는데, 프로세스 하나는 스레드 한 개 이상으로 나눌 수 있다.

# 멀티 프로세스와 멀티 스레드의 차이
멀티 프로세스
- 운영체제에서 할당받은 자신의 메모리를 가지고 실행하기 때문에 각 프로세스는 서로 독립적입니다.
- 따라서 하나의 프로세스에서 오류가 발생해도 다른 프로세스에 영향을 미치지 않습니다.
멀티 스레드
- 하나의 프로세스 내부에 생성되기 때문에 하나의 스레드가 예외를 발생시키면 프로세스 자체가 종료될 수 있어 다른 스레드에 영향을 미치게 됩니다.

ex)
- 멀티 프로세스인 워드와 엑셀을 동시에 사용하던 도중, 워드에 오류가 생겨 먹통이 되더라도 엑셀은 여전히 사용 가능합니다.
- 멀티 스레드로 동작하는 메신저의 경우 파일을 전송하는 스레드에서 예외가 발생하면 메신저 프로세스 자체가 종료되므로 채팅 스레드도 같이 종료됩니다.
- 그렇기 때문에 멀티 스레드에서는 예외 처리에 만전을 기해야 합니다.
