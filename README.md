# ToDo List Clone Coding

올해 다짐한 것이 안드로이드 개발자가 되겠다고 다짐했습니다. 가장 재밌었다고 느낀 개발 분야이기에 더 열심히 공부해보려 합니다. 그래서 ToDo List Clone 코딩을 진행할까 합니다. 역시 모든 코드의 흐름을 알기 위해서 하나하나 모두 기록할 예정입니다. 화이팅!!

이 프로젝트를 하면서 꼭 알아야 할 것

1. MVP, MVVM, 구글 아키텍처에 대해 꼭 알아보기
2. DI 소개 및 Koin 사용하기
3. 시나리오를 기반으로 TDD코드 작성하기
4. ToDo 리스트, 상세 화면 구현하기

### 1. MVP, MVVM, 구글 아키텍처 | 아키테처를 사용하면 좋은 이유

- 일관적인 코드작성(유지보수 👍, 협업 👍)
- 생산성 향상
- 테스트의 용이성(👍)
- 어플리케이션 개발의 방향성을 잡아줌
  - 비즈니스 로직을 기반으로한 Unit Test 코드를 작성하기 매우 용이함
- 등등등...
- 디자인 패턴의 예시
  - MVC: Model + View + Controller
  - MVP: Model + View(ViewController) + Presenter
  - MVVM: Model + View(ViewController) + ViewModel
  - MVVM + DataBinding
  - MVI: Model + View + Intent
  - MvRx, Flux, Ribs, etc...

#### Design Pattern MVVM

![MVVm](/Users/junku/Desktop/Android Clone Coding/ToDo List Clone Coding/img/MVVm.png)

#### Design Pattern MVVM + DataBinding

![MVVMDATABINDING](/Users/junku/Desktop/Android Clone Coding/ToDo List Clone Coding/img/MVVMDATABINDING.png)



👏🏻 TDD

**TDD**: Test Driven Development의 약자, 테스트가 개발을 이끌어 간다는 것을 의미한다.

테스트를 먼저 만들고 테스트를 통과하기 위한 과정을 짜는 것

결정과 피드백 사이의 Gap 간극을 조절할 수 있는 테크닉 중 하나

🤔 **TDD가 필요한 이유**

1. 에자일 같이 매우 빠르고 많이 프로덕트 개선이 일어나는 과정에서는 어쩔 수 없는 불확실성이 따른다.
2. 이러한 이유로 빠른 커뮤니케이션 핑퐁, 피드백과 협력이 필요할 수 있다.
3. TDD도 마찬가지로 잦은 피드백과 협력을 증진시킬 수 있는 방법이기에, 1번과 같은 상황에서 충분히 도움된다.
4. 예시
   - 결과가 너무 뻔하다면, 안해도 됨
   - 자신감 지수가 낮은 경우 (처음 해보는 개발이라던가 불확실성이 높은 경우)
   - 요구사항이 빈번히 바뀌는 경우
   - 테크니컬한 스펙, 비즈니스 로직이 자주 바뀌는 경우
   - 개발하고 난 뒤에 다른 개발자에게 해당 스펙에 대해 인수인계가 필요한 경우
5. 그럼에도 불구하고 TDD가 어려운 이유
   - 개발시간 증가 →  필요성을 못느끼는 실무진이 있을 수 있다.
     - 일반적인 회사는 프로젝트의 단기적인 성과에 집중한다.
     - 전체적인 개발 시간을 줄이기 보다는 오늘 해야할 업무를 쳐내기 바쁘다.
   - TDD 자체가 어렵다.
     - 일반적인 개발 방식과 반대로 감 from ( 개발 → 테스트 ) to ( 테스트 → 개발 )
     - 체득한 것을 내려놓기 어려움 (Unlearning: 이미 배운 것을 잊어가야함)
   - TDD를 사용하기 위해서는 `프레임워크, 툴을 사용해야한다는`강박관념이 있어 진입장벽을 만든다.
     - 반드시 툴 (단위 테스트 프레임워크)을 써서 이렇게 해야 한다고 생각한다.
     - 이런 규칙에 얽메이면 민접한 방식으로 개발을 주도하기가 어려워진다.
     - 도구 / 규칙에 집착하게 되면 오히려 TDD가 어렵다.
6. TDD를 잘하는 방법
   - 피드벡을 자주 받을 수 있는 환경을 만든다.
     - Test Case 작성
     - 주기적인 프로세스 검증
   - 내가 하는 작업에 협력을 할 수 있는 방법을 유도한다.
     - 함께 비즈니스 로직을 고민한다.
     - 프로덕트 스펙을 잘게 쪼갠다.
     - 민첩하게 비즈니스 로직을 구현한다. → 빠르게 검증