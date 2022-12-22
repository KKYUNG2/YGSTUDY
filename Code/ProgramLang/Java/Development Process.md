# 자바프로그램 개발 Process

1. 자바 프로그램을 개발하기 위해서는 우선 파일 확장명이 .java인 텍스트 파일을 생성 

2. 자바 소스 파일을 컴파일러인 javac 명령어로 컴파일

3. 컴파일이 성공하면 확장명이 .class인 바이트 코드 파일이 생성됨


.java -> (javac 컴파일러) -> .class



# 바이트 코드 파일과 자바 가상 기계
- 자바 프로그램은 완전히 기계어가 아닌, 바이트 코드파일(.class)로 구성됩니다.
- 바이트 코드 파일은 운영체제에서 바로 실행할 수 없고, 자바 가상 기계(JVM)라는 번역기가 필요합니다.


# 자바가 JVM을 사용하는 이유
- 바이트 코드 파일을 다양한 운영체제에서 수정하지 않고 사용할 수 있도록 위함입니다.
- 이 특징이 자바 언어를 성공으로 이끌었다고 볼 수 있습니다.
ex) 개발자는 윈도우 운영체제에서 편하게 프로그램(바이트 코드 파일)을 개발하고, 개발 완료된 프로그램은
리눅스로 옮겨 바로 실행할 수 있습니다.
- javac 명령어로 컴파일된 바이트 코드 파일은 JDK가 설치된 어떠한 운영체제에서도 java 명령어로 동일하게 실행할 수 있습니다.
- 각 운영체제의 JVM은 바이트 코드 파일을 해당 운영체제에서 실행 가능한 기계어로 번역해서 실행

