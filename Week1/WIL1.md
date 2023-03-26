# 1. MVC 패턴이란?

MVC 패턴이란 model-view-controller 패턴을 의미한다.  
애플리케이션을 세 가지의 구성요소로 나누어 각각 고유한 역할을 수행하도록 하는 개발 방식이다.
MVC 패턴을 사용하면 애플리케이션의 시각적인 요소와 비즈니스 로직을 분리하여 서로 영향 없이 쉽게 고칠 수 있는 애플리케이션을 만들 수 있다.

## 1.1 Model

Model은 데이터를 처리하는 영역이다.  
데이터 추출, 저장, 삭제, 업데이트 등과 같은 데이터와 관련된 비즈니스 로직을 처리한다.

## 1.2 View

View는 데이터를 받아와 사용자에게 화면을 보여주는 영역이다. 즉, UI 담당이다.  
Controller로 부터 보여줄 값(Model)을 받아와 사용자에게 보여준다.

## 1.3 Controller

Controller는 Model과 View 사이를 이어주는 역할을 한다.  
View로부터 사용자의 action을 받아 Model에 전달하고 그렇게 바뀐 Model 데이터를 다시 View에 전달하여 업데이트하는 등 사용자가 애플리케이션을 조작하여 발생하는 이벤트들을 처리한다.

# 2. API와 서버?

API란 Application Programming Interface의 약자로, 프로그램들이 서로 통신할 수 있게 하는 매커니즘이다.  
예를 들어, 기상청의 소프트웨어 시스템에는 기상 데이터가 저장되어 있다. 휴대폰의 날씨 앱은 API를 통해 이 시스템과 통신하여 휴대폰에 기상 정보를 표시한다.  
서버란 클라이언트의 요청을 받으면 서비스, 데이터를 제공하는 컴퓨터 혹은 프로그램을 의미한다.  
즉, 요청을 보내는 애플리케이션을 클라이언트라고 하고 응답을 보내는 애플리케이션을 서버라고 한다.
기상청의 날씨 데이터베이스가 서버이고 모바일 앱은 클라이언트인 것이다.

# 3. RESTful 이란?

RESTful이란 일반적으로 REST라는 아키텍쳐를 구현하는 웹 서비스를 나타내기 위한 용어이다.  
즉, REST API를 제공하는 웹 서비스를 RESTful하다고 할 수 있다.  
REST란, Representational State Transfer의 약자로, 자원을 이름으로 구분하여 해당 자원의 상태(정보)를 주고 받는 모든 것을 의미한다.  
REST의 구성요소로는 자원(Resource), 행위(Verb), 표현(Representation)이 있다.  
자원이란, 웹서버가 관리하는 모든 것들이다. 자원은 URI라는 통합 자원 식별자(Uniform Resource Identifier)를 통해 고유한 주소로 지정해서 식별할 수 있다.
REST에서 하나의 자원은 JSON, XML, TEXT, RSS 등 여러 형태의 표현(Representation)으로 나타내어 질 수 있다.
웹 서버에서 행위는 HTTP 프로토콜의 Method를 이용한다. GET, POST, PUT, DELETE 와 같은 메서드를 통해 해당 자원에 대한 CRUD Operation을 적용한다.

CRUD Operation이란,  
Create: 생성(POST)  
Read: 조회(GET)  
Update: 수정(PUT)  
Delete: 삭제(DELETE) 를 말한다.

즉, 이러한 REST를 기반으로 서비스 API를 구현한 것을 REST API라고 하고, 이 REST API를 제공하는 웹 서비스를 RESTful하다고 할 수 있는 것이다.
