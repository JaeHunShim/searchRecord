[스프링의 특징과 개념](http://12bme.tistory.com/157)
======

* ## POJO 기반의 구성
* ## 의존성 주입(DI)을 통한 객체간의 구성
* ## AOP (Aspect -Oriented-Programming)
---
### 1. POJO 기반의 구성
* 일반적인 Java코드를 이용해서 객체를 구성하는 방식을 그대로 스프링에서 사용할수 있다. 즉, 개발자가 특정한 라이브러리나 컨테이너의 기술에 종속이지 않다는 것을 의미.
이것은 일반적인 형태로 코드를 작성하고, 실행할수 있어서 생산성이 유리하고 테스트도 유연하게 할수 있는 장점이 있다
---

### 2. 의존성 주입을 통한 객체간의 구성 관계
* 의존성은 제어의 역행(IOC:Inversion Of Control)은 서로 밀접한 관계가 있다. 의존성이라는 말은 어떠한 객체가 어떠한 일을 혼자서 처리 할수 없다는 것을 의미한다.
만일 A가 다른 객체 B의 도움을 받아야만 어떤일을 할수 있을때 **A는 B에 의존적이다**라고 표현하는데  Java에서는 Interface를 이용해서 이런 의존적인 관계를 유연하게 처리한다.  이러한 의존적인 객체를 직접 연결하는 것이 아니라 **SrpingFrameWork가 제어권을 가지고 유연하게 연결시켜 주는것을 제어의 역행 이라고 한다**  즉, 개발자는 객체나 클래스를 만드는 것 외에는 신경쓰지 않고 코드를 작성 할수 있다.(생성자,set메소드를 이용해서 의존주입하고 간단한 어노테이션 만으로 알아서 처리할수 있다. ex: @Repository, @Service , @Controller...)
---
### 3. AOP 지원(Aspect Oriented Programming)
* 쉽게 말하면 반복적인 코드를 제거해서 개발자가 핵심 비지니스 로직에서 집중할수 있게 하는 방법이다. 대부분 로그, 트랜잭션이나 보안(Intercepter) 등을 모듈로 따로 분리하는 프로그래밍의 패러다임이라고 할수 있다. 실제 프로그램개발에서 **비지니스로직은 아니지만 반드시 해야하는 작업** 정도로 해석하면 될것같다.