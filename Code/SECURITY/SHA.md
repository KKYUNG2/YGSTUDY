#First created on December 20, 2022 by KYG

# SHA-1, SHA-256, SHA-384, SHA-512

SHA란?
- 1993년에 미국의 연방정보처리표준 규격(FIPS PUB 180)으로서 발표된 것을 SHA라 부른다.


SHA-1
- 2005년에 암호학적으로 공격에 취학한 것이 밝혀졌다.
- 2010년 이후로는 호환성 유지 이외의 목적으로는 사용을 권장하지 않는다.

SHA-256, SHA-384, SHA-512
- NIST에서 만든 일방향 해시 함수로 각각 256, 384, 512 비트 해시 값을 출력한다.
- 이들 일방향 해시 함수를 모아서 SHA-2라고 하는 경우도 있다.

SHA-512 구조
- SHA-512 알고리즘에서는 최대 길이가 2^128 비트 이하인 메시지를 입력으로 사용하고 길이가 512 비트인 메시지 다이제스트를 출력한다.
- 입력 데이터는 길이가 1,024 비트인 블록으로 나누어서 처리된다.

SHA-512의 안전성
- 2017년 현재까지 SHA-512에 숨어있는 약점을 지적한 연구 보고서는 없다.
- 동일한 메시지 다이제스트를 갖는 두 메시지를 찾아야 하는 난이도는 2^256번의 연산을 수행해야 얻을 수 있는 수준.
- 반면에? 주어진 다이제스트와 같은 다이제스트를 갖는 메시지를 찾아야 하는 난이도는 2^512번 연산을 수행해야 하는 수준





