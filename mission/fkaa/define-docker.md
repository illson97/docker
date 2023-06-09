### 사전미션 1. Docker?

#### 1. 컨테이너 기술이란 무엇입니까?
- 컨테이너란?
  - 소프트웨어 서비스를 환경에 독립적으로 실행할 수 있도록 실행에 종속되는 요소를 패키징하는 소프트웨어의 표준 단위이다.

#### 2. 도커란 무엇입니까?
- 도커란?
  - 도커는 컨테이너 기술을 활용한 서비스의 하나로, 애플리케이션 개발, 배송 및 실행을 위한 개방형 프르랫폼으로, 애플리케이션을 인프라에서 분리하여 ㅅ소프트웨어를 신속하게 제공할 수 있다는 이점이 있다.
  - ref. https://docs.docker.com/get-started/overview/

#### 3. 도커 파일, 도커 이미지, 도커 컨테이너의 개념은 무엇이고, 서로 어떤 관계입니까?
- 도커 파일이란?
  - Docker File은 Docker에서 이미지를 생성하기 위해 작성하는 파일로 별도의 확장자를 가지지 않으며, `docker build` 명령을 통해 Dockerfile에 기술된 정보를 바탕으로 Docker 이미지를 작성한다.
  - Docker File의 명령어

|명령| 설명                   |
|:---|:---------------------|
|FROM| 베이스 이미지를 지정          |
|RUN| 명령 실행(이미지를 생성할 때 실행) |
|CMD|컨테이너 실행 명령(생성된 컨테이너 안에서 명령을 실행)|
|LABEL|라벨 설정|
|EXPOSE|포트 익스포트|
|ENV|환경변수|
|ADD|파일 / 디렉토리 추가|
|COPY|파일 복사|
|ENTRYPOINT|컨테이너 실행 명령|
|VOLUME|볼륨 마운트|
|USER|사용자지정|
|WORKDIR|작업 디렉토리|
|ARG|Dockerfile 안의 변수|
|ONBUILD|빌드 완료 후 실행되는 명령|
|STOPSIGNAL|시스템 콜 시그널 설정|
|HEALTHCHECK|컨테이너의 헬스 체크|
|SEHLL|기본 쉘 설정|

- 도커 이미지란?
  - 소스코드, 라이브러리, 종속성, 도구 및 응용 프로그램 등 애플리케이션의 실행에 종속되는 기타 파일을 포함하는 불변 파일이다.
  - 이미지는 읽기 전용이므로 스냅샷이라고도 하고, 특정 시점의 애플리케이션과 가상 환경을 나타낸다.
  - 위의 특성으로 개발자가 안정적이고 균일한 조건에서 소프트웨어를 테스트하고 실험할 수 있는 환경을 제공한다.

- 도커 컨테이너란?
  - 사용자가 기본 시스템에서 애플리케이션을 분리할 수 있는 가사오하된 런타임 환경이다.

- 도커 파일, 도커 이미지, 도커 컨테이너간의 관계는?
  - 도커 파일을 실행하여 도커 이미지를 생성한다.
  - 도커 컨테이너는 이미지에 의해 실행되는 구조이다. 즉, 컨테이너는 이미지에 종속되어 런타임 환경을 구성하고 애플리케이션을 실행하는 데 사용된다.
  - Dockerfile >> (build) >> Dockerimage >> (Create) >> Container

#### 4. [실전미션] 도커 설치하기

