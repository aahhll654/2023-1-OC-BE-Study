# 1. 컨트롤러, 서비스, 리포지토리의 역할

## 1.1 컨트롤러

Controller는 Model과 View 사이를 이어주는 역할을 한다.  
View로부터 사용자의 action을 받아 Model에 전달하고 그렇게 바뀐 Model 데이터를 다시 View에 전달하여 업데이트하는 등 사용자가 애플리케이션을 조작하여 발생하는 이벤트들을 처리한다.

## 1.2 서비스

서비스는 컨트롤러와 리포지토리의 중간에서 비즈니스 로직을 수행하는 역할을 한다. 컨트롤러가 외부에서 온 요청을 서비스로 넘기면 서비스는 핵심 비즈니스 로직을 수행한다. 이때, DB정보가 필요하면 리포지토리에게 요청을 하게 된다.

## 1.3 리포지토리

리포지토리는 데이터베이스와 직접적인 상호작용을 하며, 데이터의 CRUD(생성, 조회, 수정, 삭제)등의 작업을 수행한다.

# 2. TDD란? 왜 하는가?

TDD란 Test-Driven Development의 약자로 '테스트 주도 개발'이라고 한다. TDD는 소프트웨어 개발 방법론 중 하나로 작은 단위의 테스트를 먼저 작성하고 이를 통과하는 코드를 추가하는 것을 반복하여 구현하는 것을 말한다.
TDD는 기본적으로  
테스트 케이스 작성 -> 테스트 케이스를 통과하는 코드 작성 -> 코드 리팩토링  
위와 같이 3단계의 반복으로 진행한다.

TDD의 장점은 다음과 같다.

### 1. 유지 보수성 향상

기본적으로 단위 테스트 기반의 테스트 코드를 작성하기 때문에 유지 보수를 하기 용이하다.

### 2. 높은 코드 품질

테스트 코드를 먼저 작성하기 때문에 무엇을 해야하는지 정의하고 생각할 수 있어 완성도 높은 설계로 이어진다.

### 3. 디버깅 시간의 단축

자동화된 단위 테스트를 통해 특정 버그를 쉽게 찾을 수 있다.

위와 같은 장점들이 TDD를 하는 이유이다.