# @Configuration이 싱글톤을 보장하는 방법
만약 AppConfig라는 클래스에 @Configuration이 있다면

스프링은 CGLIB이라는 바이트 코드 조작 라이브러리를 사용해서 AppConfig 클래스를 상속받은 임의의 클래스를 만들고
그 클래스를 스프링 빈으로 등록한다

이 임의의 클래스가 싱글톤이 보장되도록 만들어준다

# CGLIB을 사용한 로직 예상
- @Bena이 붙어있는 매서드마다 스프링 빈이 존재하는지 확인, 존재하면 이미 있는 빈을 반환하고
- 없으면 생성해서 스프링 빈으로 등록하고 반환한다
  -> 코드가 동적으로 만들어진다
- 이러한 로직으로 싱글톤을 보장

# @Configuration을 적용하지 않고 @Bean만 적용하면 어떻게 될까?
@Bean만 사용해도 스프링 빈으로 등록되는 건 맞지만, 싱글톤을 보장하지 않는다

스프링 설정 정보는 항상 @Configuration을 사용하도록 하자
