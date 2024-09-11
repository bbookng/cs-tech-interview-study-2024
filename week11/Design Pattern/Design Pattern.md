# Design Pattern 

- 일종의 설계 기법이며, 설계 방법이다. 

> 디자인 패턴은 개발하면서 발생하는 **반복적인 문제**들을 어떻게 해결할 것인지에 대한 **해결 방안**으로 실제 현업에서 비즈니스 요구 사항을 프로그래밍으로 처리하면서 만들어진 다양한 해결책 중에서 많은 사람들이 인정한 **모범 사례(Best Practice)** 다.
> 이러한 디자인 패턴은 **객체 지향 4대 특성** (캡슐화, 상속, 추상화, 다형성) 과 **설계 원칙** (SOLID)을 기반으로 구현되어 있다. 

### 💡 목적
- SW **재사용성, 호환성, 유지보수성**을 보장.

### 💡 장점

1. **재사용성** : 반복적인 문제에 대한 일반적인 해결책을 제공하므로, 이를 재사용하여 유사한 상황에서 코드를 더 쉽게 작성할 수 있다. 
2. **가독성** : 일정한 구조로 정리하고 명확하게 작성하여 개발자가 코드를 이해하고 유지보수하기 쉽게 만든다. 
3. **유지보수성** : 코드를 쉽게 모듈화 할 수 있으며, 변경이 필요한 경우 해당 모듈만 수정하여 유지보수가 쉬워진다. 
4. **확장성** : 새로운 기능을 추가하거나 변경할 때 디자인 패턴을 활용하여 기존 코드를 변경하지 않고도 새로운 기능을 통합할 수 있다. 
5. **안정성과 신뢰성** : 수많은 사람들이 인정한 모범 사례로 검증된 솔루션을 제공한다. 

### 💡 특징
- **디자인 패턴은 아이디어**임, 특정한 구현이 아님.
- 프로젝트에 항상 적용해야 하는 것은 아니지만, 추후 재사용, 호환, 유지 보수시 발생하는 **문제 해결을 예방하기 위해 패턴을 만들어 둔 것**임. 

### 💡 원칙 - SOLID (객체지향 설계 원칙)
(간략한 설명)
1. **Single Responsibility Principle**
	- 하나의 클래스는 하나의 역할만 해야 함. 
2. **Open - Close Principle**
	- 확장 (상속) 에는 열려있고, 수정에는 닫혀 있어야 함. 
3. **Liskov Substitution Principle**
	- 자식이 부모의 자리에 항상 교체될 수 있어야 함. 
4. **Interface Segregation Principle**
	- 인터페이스가 잘 분리되어서, 클래스가 꼭 필요한 인터페이스만 구현하도록 해야 함. 
5. **Dependency Inversion Property**
	- 상위 모듈이 하위 모듈에 의존하면 안됨. 
	- 둘 다 추상화에 의존하며, 추상화는 세부 사항에 의존하면 안됨.

### 💡 분류 (중요)
![[Pasted image 20240902165322.png]]
##### 📌 3가지 패턴의 목적을 이해하기 ! 
#### 1. 생성 패턴 (Creational) : 객체의 생성 방식 결정
- Class-creational patterns, Object-creational patterns.
- 예) DBConnection을 관리하는 Instance를 하나만 만들 수 있도록 제한하여, 불필요한 연결을 막음.
  ##### 1. Singleton (싱글톤 패턴)
  : 하나의 클래스 인스턴스를 전역에서 접근 가능하게 하면서 해당 인스턴스가 한 번만 생성되도록 보장하는 패턴.
  ##### 2. Factory Method (팩토리 메서드 패턴)
  : 객체를 생성하기 위한 인터페이스를 정의하고, 서브 클래스에서 어떤 클래스의 인스턴스를 생성할지 결정하는 패턴.
  ##### 3. Abstract Factory (추상 팩토리 패턴)
  : 관련된 객체들의 집합을 생성하는 인터페이스를 제공하며, 구체적인 팩토리 클래스를 통해 객체 생성을 추상화하는 패턴. 
  ##### 4. Builder (빌더 패턴)
  : 복잡한 객체의 생성 과정을 단순화하고, 객체를 단계적으로 생성하며 구성하는 패턴.
  ##### 5. Prototype (프로토타입 패턴)
  : 객체를 복제하여 새로운 객체를 생성하는 패턴으로, 기존 객체를 템플릿으로 사용하는 패턴. 
#### 2. 구조 패턴 (Structural) : 객체간의 관계를 조직
- 예) 2개의 인터페이스가 서로 호환이 되지 않을 때, 둘을 연결해주기 위해서 새로운 클래스를 만들어서 연결시킬 수 있도록 함.
  ##### 1. Adapter (어댑터 패턴)
  : 인터페이스 호환성을 제공하지 않는 클래스를 사용하기 위해 래퍼(Wrapper)를 제공하는 패턴.
  ##### 2. Bridge (브릿지 패턴)
  : 추상화와 구현을 분리하여 두 가지를 독립적으로 확장할 수 있는 패턴.
  ##### 3. Composite (컴포지트 패턴)
  : 개별 객체와 복합 객체를 동일하게 다루어, 트리 구조의 객체를 구성하는 패턴.
  ##### 4. Decorator (데코레이터 패턴)
  : 객체에 동적으로 새로운 기능을 추가하여 객체를 확장할 수 있는 패턴.
  ##### 5. Facade (파사드 패턴)
  : 서브시스템을 더 쉽게 사용할 수 있도록 단순한 인터페이스를 제공하는 패턴.
  ##### 6. Flyweight (플라이웨이트 패턴)
  : 공유 가능한 객체를 통해 메모리 사용을 최적화하는 패턴.
  ##### 7. Proxy (프록시 패턴)
  : 다른 객체에 대한 대리자(Proxy)를 제공하여 접근 제어, 지연 로딩 등을 구현하는 패턴. 
#### 3. 행위 패턴 (Behavioral) : 객체의 행위를 조직, 관리, 연합
- 예) 하위 클래스에서 구현해야 하는 함수 및 알고리즘들을 미리 선언하여, 상속시 이를 필수로 구현하도록 함.
  ##### 1. Observer (옵저버 패턴)
  : 객체 간의 일대다 종속 관계를 정의하여 한 객체의 상태 변경이 다른 객체들에게 알려지도록 한다. 
  ##### 2. Strategy (전략 패턴)
  : 알고리즘을 정의하고, 실행 중에 선택할 수 있게 한다. 
  ##### 3. Command (커맨드 패턴)
  : 요청을 객체로 캡슐화하여 요청을 매개변수화 하고, 요청을 큐에 저장하거나 로깅하고 실행을 지연시킨다. 
  ##### 4. State (상태 패턴)
  : 객체의 상태를 캡슐화하고, 상태 전환을 관리한다. 
  ##### 5. Chain of Responsibility (책임 연쇄 패턴)
  : 요청을 보내는 객체와 이를 처리하는 객체를 분리하여, 다양한 처리자 중 하나가 요청을 처리한다. 
  ##### 6. Visitor (방문자 패턴)
  : 객체 구조를 순회하면서 다양한 연산을 수행할 수 있게 한다. 
  ##### 7. Interpreter (인터프리터 패턴)
  : 언어나 문법에 대한 해석기를 제공하여, 주어진 언어로 표현된 문제를 해결하는 패턴.
  ##### 8. Memento (메멘토 패턴)
  : 객체의 내부 상태를 저장하고 복원할 수 있는 기능을 제공하는 패턴. 
  ##### 9. Mediator (중재자 패턴)
  : 객체 간의 상호 작용을 캡슐화하여, 객체 간의 직접적인 통신을 방지하는 패턴. 
  ##### 10. Template Method (템플릿 메서드 패턴)
  : 알고리즘의 구조를 정의하면서 하위 클래스에서 각 단계의 구현을 제공하는 디자인 패턴. 
  ##### 11. Iterator (이터레이터 패턴)
  : 컬렉션 내의 요소들에 접근하는 방법을 표준화하여 컬렉션의 내부 구조에 독립적으로 접근할 수 있는 패턴. 

---
[Ref](https://gyoogle.dev/blog/design-pattern/Overview.html)