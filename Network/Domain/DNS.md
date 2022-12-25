#Created By KYG

# DNS

DNS의 정의
- 인터넷을 구성하고 있는 IP 주소는 IPv4의 경우 192.168.0.1 같이 숫자로 구성된다.
- 이런 숫자는 아무런 의미도 없기 때문에 외우기 힘들어 따라서 naver.com 같은 문자열로 서버 주소를 표현한다.
- 다만 실제 컴퓨터 통신에서는 문자열 주소를 IPv4 주소로 변환해주는 서비스가 필요하다.
- 이런 서비스를 DNS 서비스라고 한다.

DNS(Domain Name System)
- 문자열 주소를 IP 주소로 해석해주는 네트워크 서비스를 말한다.
- DNS 서버에는 도메인 주소와 IP 주소의 쌍(Pair)이 저장된다.


# A Record & CNAME
- 어느날 팀장님께서 A Record와 CNAME에 대해 질문하셨고, 그 해답을 명확하게 말씀드리지 못했다.
- 따라서 언제 어디서든 어떤 질문이


# A 레코드 (A Record)
- A 레코드(A Record)는 DNS에 저장되는 정보의 타입으로 도메인 주소와 서버의 IP 주소가 직접 매핑시키는 방법이다.
- 위 테이블에 적혀있는 것처럼 첫 번째 컬럼값이 naver.com 같은 도메인 주소고, 두 번째 컬럼 값이 192.168.0.1 같은 IP 주소인 형태를 말한다.
- 위에서 말했던 것처럼 사용자가 A 레코드에 해당하는 도메인 주소에 대한 해석을 요청하면 DNS 서버는 IP 주소를 리턴해준다.


# CNAME
- CNAME은 Canonical Name의 약자로 도메인 주소를 또 다른 도메인 주소로 매핑 시키는 형태의 DNS 레코드 타입이다.

naver.com	192.168.0.68
dev.naver.com	192.168.0.15
develop.naver.com   dev.naver.com


- 위와 같은 정보가 DNS 서버에 저장되어 있다고하자.
- 사용자가 dev.naver.com 주소를 요청하면 서버는 192.168.0.15 를 응답한다.

- 만약 develop.naver.com을 요청하면 DNS 서버는 dev.naver.com을 리턴하고,
- 사용자는 다시 dev.naver.com 정보를 DNS 서버에 요청한다.
- DNS 서버는 이제 192.168.0.15 을 리턴하고 사용자는 IP 주소를 사용하게 된다.



# A 레코드 vs. CNAME
- A 레코드 타입과 CNAME 타입의 장단점은 명확하다.


# A 레코드

장점
- 한번의 요청으로 찾아갈 서버의 IP 주소를 한번에 알 수 있다는 점이다.

단점
- IP 주소가 자주 바뀌는 환경에서는 조금 번거로울 수 있다는 점이다.
- 예를 들어,

192.168.0.15 www.naver.com
192.168.0.15 dev.naver.com
192.168.0.15 develop.naver.com


- 이렇게 구성되어있다면, 192.168.0.15를 가지고 있는 모든 www.naver.com, dev.naver.com, develop.naver.com을 모두 바꿔주어야 합니다.


# CNAME 레코드

장점
- IP 주소가 자주 변경되는 환경에서 유연하게 대응할 수 있다는 점이다.
- 예를 들어, dev.naver.com, develop.naver.com 도메인 정보를 www.naver.com이라는 주소로 매핑시키는 CNAME 레코드로 저장하고,
- www.naver.com이라는 주소를 192.168.0.15 라는 IP 주소로 매핑시키는 A 레코드로 저장해 놨다면,
- 서버의 IP 주소가 바뀌었을 때 www.naver.com의 A 레코드 정보만 변경시키면 된다.

단점
- 레코드의 단점은 실제 IP 주소를 얻을 때까지 여러번 DNS 정보를 요청해야 한다는 점이다.
- DNS 정보를 해석하는데 여러번 요청이 필요하다는 점은 경우에 따라서 성능저하를 유발할 수 있다.