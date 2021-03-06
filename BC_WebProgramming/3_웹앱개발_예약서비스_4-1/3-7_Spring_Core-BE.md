# 웹 프로그래밍 - 3. 웹 앱 개발:예약서비스 1/4

## 7. Spring Core - BE

### Spring Framework
- Framework: 반제품
- 모듈화
- IoC(Inversion of Control) 컨테이너
- 선언적으로 트렌젝션 관리 가능
- 완전한 기능을 가진 MVC Framework 제공
- AOP(Aspect Oriented Programming)지원: 핵심 기능과 공통 기능을 분리하여 사용 가능
- 도메인 논리코드와 쉽게 분리될 수 있는 구조

### [Spring Modules](https://docs.spring.io/spring/docs/4.3.14.RELEASE/spring-framework-reference/htmlsingle/#overview)
#### AOP & Instrumentation
- spring-AOP
- spring-aspects
- spring-instrument

#### Messaging
- spring-messaging

#### Data Access / Integration
- spring-jdbc
- spring-tx
- spring-orm
- spring-oxm
- spring-jms

#### Web
- spring-web
- spring-webmvc
- spring-websorket
- spring-webmvc-portlet

### 컨테이너(Container)
- 인스턴스의 생명주기 관리
- 생성된 인스턴스에게 추가적인 기능 제공
- (예. Tomcat이 Servlet Container를 가지고 있어 생명주기를 관리해 줌)

### IoC(Inversion of Control)
- 제어의 역전
- 개발자가 아닌 다른 프로그램이 프로그램의 흐름을 제어하는 것

### DI(Dependency Injection)
- 의존성 주입
- 클래스 사이의 의존 관계를 Bean설정 정보를 바탕으로 컨테이너가 자동으로 연결해주는 것

### Spring에서 제공하는 IoC/DI
- BeanFactory
   + IoC/DI에 대한 기본 기능을 가짐
- ApplicationContext
   + BeanFactory의 모든 기능을 포함
   + 트렌젝션처리와 AOP등에 개한 처리 가능
   + BeanPostProcessor, BeanFactoryPostProcessor 등을 자동으로 등록
   + 국제화 처리
   + 어플리케이션 이벤트 처리

### Bean
- Spring컨테이너가 관리하는 객체
1. 기본 생성자를 가진다
2. 필드는 private하게 선언한다
3. getter, setter 메소드를 가진다. getName(), setName()을 name 프로퍼티(property)라고 한다

### Java Config를 이용한 설정
- annotation은 jdk 5부터 지원
- @Configuration: 스프링 설정 클래스를 선언
- @Bean: bean을 정의
- @ComponentScan: @Controller, @Service, @Repository, @Component이 붙은 클래스를 찾아 컨테이너에 등록
- @Component: 컴포넌트 스캔의 대상이 되는 어노테이션 중 하나로 주로 유틸, 기타 지원 클래스에 사용
- @Autowired: 주입 대상이 되는 bean을 컨테이너에 찾아 주입



<br>



---
[HOME](https://github.com/tunaep5/Boostcourse/blob/master/README.md)
