## 🎯 기능 구현 목록
**1. 자동차의 이름을 입력받는 기능**
- [ ] 사용자는 자동차 이름을 input에 입력하고, 엔터 혹은 확인버튼을 클릭한다. 
  - 자동차 이름은 ,를 기준으로 구분하여 입력하며, 이름은 5자 이하만 가능하다. 
- [ ] 입력받은 자동차 이름이 유효한지 검사한다. 
  - [예외처리] 5자를 초과한 것이 있으면 alert를 이용해 메시지를 보여주고, 다시 입력할 수 있게 한다. 
  - [예외처리] 문자가 아닌 것이 있으면, alert를 이용해 메시지를 보여주고, 다시 입력할 수 있게 한다.
- [ ] 입력받은 것이 유효하다면, 입력받은 string을 `,` 기준으로 배열화한다. (`split(')`) 

**2. 시도 횟수를 입력받는 기능**
- [ ] 사용자는 시도할 횟수를 입력하고, 엔터 혹은 확인버튼을 클릭한다. 
- [ ] 입력받은 값이 유효한지 검사한다. 
  - [예외처리] 숫자가 아닌 경우, alert를 이용해 메시지를 보여주고, 다시 입력할 수 있게 한다. 

**3. 자동차를 전진 또는 정지할지 결정하는 기능** 
- [ ] 0~9 사이의 무작위 값을 구한다 
  - [ ] 무작위 값이 4 이상일 경우, 전진한다.
  - [ ] 무작이 값이 3 이하인 경우, 멈춘다. 

**4. 게임 과정을 출력하는 기능** 
- [ ] 게임 과정을 출력한다. 

**5. 우승자를 알려주는 기능** 
- [ ] `-` 의 갯수가 가장 많은 자동차를 우승으로 출력한다. 
  - 우승자는 한명 이상일 수 있다. 
- [ ] 우승자가 여러명일 경우, 쉼표(,)를 이용하여 구분한다. 


## ✅ 요구 사항
- [ ] 주어진 index.html에 html 엘리먼트를 직접 추가하거나 기존의 html 엘리먼트를 임의로 삭제하지 않는다. id와 같은 선택자를 추가하는 작업만 가능하다.
- [ ] 다음과 같이 Car 객체를 만들고, new 를 이용해 인스턴스를 만들어 사용한다.
  ```javascript
  function Car(name) {
  this.name = name;
  }
  ```
- [ ] dom 선택자를 잘 지정한다. 
  - 자동차의 이름을 입력하는 input 태그는 `car-names-input` id값을 가진다.
  - 자동차의 이름을 제출하는 button 태그는 `car-names-submit` id값을 가진다.
  - 레이싱 횟수를 입력하는 input 태그는 `racing-count-input` id값을 가진다.
  - 레이싱 횟수을 제출하는 button 태그는 `racing-count-submit` id값을 가진다.
  - 최종 우승자를 출력하는 span 태그는 `racing-winners` id값을 가진다.
    - 예) <span id="racing-winners">poco,park,jun</span>
- [ ] 전진하는 조건을 판단하기 위한 랜덤 값은 MissionUtils 라이브러리의 Random.pickNumberInRange를 사용해 구한다. MissionUtils 라이브러리 스크립트는 index.html에 이미 포함되어 전역 객체에 추가되어 있으므로, 따로 import 하지 않아도 구현 코드 어디에서든 사용할 수 있다.
- [ ] 외부 라이브러리(jQuery, Lodash 등)를 사용하지 않고, 순수 Vanilla JS로만 구현한다.
- [ ] 자바스크립트 코드 컨벤션을 지키면서 프로그래밍 한다. 정답이 없으므로, 다양한 컨벤션을 비교해보며 스스로 더 적절해보이는 컨벤션을 자율적으로 선택한다.
- [ ] indent(인덴트, 들여쓰기) depth를 3이 넘지 않도록 구현한다. 2까지만 허용한다. 예를 들어 while문 안에 if문이 있으면 들여쓰기는 2이다.
- [ ] 함수(또는 메소드)가 한 가지 일만 하도록 최대한 작게 만들어라.
- [ ] 변수 선언시 var 를 사용하지 않는다. const 와 let 을 사용한다.
- [ ] import 문을 이용해 스크립트를 모듈화하고 불러올 수 있게 만든다.
- [ ] 함수(또는 메소드)의 길이가 15라인을 넘어가지 않도록 구현한다.
- [ ] 함수(또는 메소드)가 한 가지 일만 잘 하도록 구현한다.
- [ ] 테스트에서 all pass를 한다. (`npm run test`)

## 📖 1주차 피드백 
- [ ] 2주 차 미션에서는 1주 차에서 학습한 것에 더해 클래스를 분리하며 개발하는 것을 목표로 할 것.
- [ ] 이름을 통해 의도를 드러내기. 이를 통해 변수, 함수, 클래스의 역할에 대한 의도를 드러내자. (숫자 및 불용어는 제외하기)
- [ ] 축약하지 마라. 의도를 드러낼 수 있다면 이름이 길어져도 괜찮다. 
   - 클래스 및 메서드 이름을 한 두단어로 유지하려고 노력하라 
   - 문맥을 중복하는 이름을 자제하라 (ex. 클래스 이름이 Order라면, shipOrder라고 메서드 이름을 짓지 말자. ship()으로 하면 order.ship()으로 간결한 호출이 가능하다.)
- [ ] 공백도 코딩 컨벤션이다. if, for, while문 사이의 공백도 코딩 컨벤션이니까 신경쓰자. 
- [ ] 공백 라인을 의미있게 사용해라. 공백라인을 문백을 분리하는 부분에 사용하면 좋다. 다만, 과도한 공백은 지양하자. 
- [ ] 반복하지 마라. 중복은 소프트웨어에서 모든 악의 근원이다. 
- [ ] space vs tab의 혼용을 하지마라. 둘 중 하나만 사용하라. 확신이 서지 않으면 pr을 보낸 후 들여쓰기가 잘 되어있는지 확인하는 습관을 들이자. 
- [ ] 의미없는 주석을 달지 말자. 이름을 통해 어떤 의도인지 드러난다면 주석을 달지 않는다. 가능하면 주석이 아닌 이름을 통해 의도를 드러내고, 불가능한 경우 주석을 단다. 
- [ ] 커밋 메시지를 의미 있게 작성하라. 커밋 메시지에 해당 커밋에서 작업한 내용에 대한 이해가 가능하도록 작성한다. 
- [ ] 기능 목록을 업데이트하라. README.md 파일에 작성하는 기능 목록은 기능 구현을 하면서 바뀔 수 있다. 시작부터 완벽히 정리해야한다고 생각하지말고, 구현하면서 계속 업데이트하자. 죽은 문서가 아닌 살아있는 문서를 만들기 위해 노력한다. 
- [ ] 기능 목록을 재검토하라. 기능 목록은 클래스 설계와 구현, 함수(메서드) 설계와 구현과 같이 너무 상세히 작성하지 않는다. 이름과 반환값은 언제든지 변경될 수 있기 때문이다. 너무 세세한 부분까지 정리하기 보다, 구현해야 할 기능 목록을 정리하는데 집중하자. 정상적인 경우도 중요하지만, 예외적 상황도 기능목록에 정리한다. 특히 예외 상황은 시작 단계에서 모두 찾기 힘들기 때문에, 기능을 구현하면서 계속해서 추가해나간다. 
- [ ] README.md를 상세히 작성하라. 해당 프로젝트가 어떤 프로젝트이며, 어떤 기능을 담고 있는지 기술하기 위해 적절한 마크다운을 사용하라. 
- [ ] linter, code formater의 기능을 활용해라. 이를 통해 더 생산적으로 코드를 작성할 수 있다. 
- [ ] 최종 제출 코드에서 EOL(End Of Line) 설정을 확인하라. 환경에 따라 의도한 바와 다르게 개행 문자가 처리되지 않도록 EOL 설정을 확인한다. 
- [ ] 최종 제출 코드에서 불필요한 console.log를 남기지 않는다. 
- [ ] var 대신 const, let을 사용하라. 

