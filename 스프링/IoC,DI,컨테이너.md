# 제어의 역전 IoC
Inversion of Control
프로그램의 제어 흐름을 내부에서 관리하는게 아닌 외부에서 관리해주고 연결 시켜 주는 것을 말한다 

# 프레임 워크 VS 라이브러리 
내가 만든 코드를 대신 실행시켜주고 제어해주면 프레임워크가 맞다
반면에 내가 작성한 코드가 직접 제어의 흐름을 담당한다면 라이브러리다

# 의존 관계 주입 - DI
Dependency Injection

의존관계는 정적인 클래스 의존관계와 동적인 객체의 의존관계 두 개를 분리해서 생각해야 한다

애플리케이션 실행 시점에 외부에서 실제 구현 객체를 생성해 클라이언트에게 전달해서 클라이언트와 서버의 실제 의존 관게를 연결시켜주는 것을 말한다 

- 객체 인스턴스를 생성해서 그 참조값을 전달한다
- 클라이언트 코드를 변경하지 않고 클라이언트가 호출하는 객체 인스턴스 타입을 쉽게 바꿀 수 있다
- 정적인 클래스 의존 관계를 변경하지 않고 동적인 객체 인스턴스의 의존 관계를 쉽게 바꿀 수 있다

# IoC 컨테이너 , DI컨테이너
Appconfig처럼 외부에서 객체를 생성하고 관리해 주는 것을 IoC컨테이너 또는 DI컨테이너라 한다

