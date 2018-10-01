## Part 2. 스위프트(Swift)
### 면접에서 최다 빈출되는 꼭 알아야 할 중요한 Swift 개념들을 모아봤습니다.  <br> 주니어 개발자라면 이 정도는 꼭 알고 계셔야 해요 :)

<br>

#### Swift 

* 클로저(Closure)
  * 일회용 함수를 작성할 수 있는 구문. 익명(Anonymous) 함수라고도 불린다. Objective-C 에서는 블록(Block) 이 클로저의 역할을 했었다. 스위프트는 함수형 프로그래밍을 채택하고 있으므로, 클로저는 중요한 역할을 담당한다. Closure 는 변수나 상수가 선언된 위치에서 참조(Reference)를 획득(capture)하고 저장할 수 있다. 

  * "변수에 함수를 선언합니다. 그리고 마찬가지로 이 변수는 함수처럼 호출도 가능합니다. 따라서 코드를 간결하고 직관적으로 작성하는데 많은 도움을 주는 기능입니다. 물론 프로그래머가 재사용할일이 많다면, 
따로 함수를 만들어주는게 맞겠지만 그게 아니라면 일일히 어떤 함수를 찾아갈 필요없이 클로저를 사용해서 바로 내용을 확인할 수 있겠습니다. 클로저가 직관적이고 간결한 코드 작성에 크게 기여하는 부분은 
축약형이 따로 존재한다는 것인데요. 기본문법 형태인 기본클로저에서부터 후행클로저, 타입유추, 단축인자생략, return 키워드 삭제, 연산자 함수까지 간결하게 축약할 수가 있습니다. 다만, 지나치게 축약하게
되면 해당 코드를 처음보는 사람은 내용을 인지하지 못하는 경우도 있습니다."

  * "클로저의 또다른 아주 중요한 특성 중에 하나가 Escaping Closure입니다. 클로저가 함수로부터 Escape한다는 것은 클로저가 인자로 전달되지만 함수가 반환된 후 실행된다는 것을 의미합니다. 
이 개념은 기존에 알고 있던 Scope 개념을 무시하는 개념입니다. 함수 안에서 선언된 변수가 로컬 변수의 영역을 뛰어넘는다는 말이 되기 때문입니다. 이것의 중요한 점은 Escaping Closure을 이용하면
A함수가 마무리된 상태에서만 B 함수가 실행되도록 코드를 작성할 수 있고, 그것은 곧 비동기 함수에도 같은 맥락으로 적용할 수 있다는 뜻이 됩니다. 예를 하나 들어 보겠습니다. 만약 서버에서 JSON형식의
데이터를 가져와 화면에 보여주는 앱을 만든다고 생각해보면 HTTP통신을 위해 Alamofire 라이브러리를 사용합니다. Alamofire의 메소드는 서버로 Request를 전송하고 GET방식으로 JSON형식의 데이터를 
받아와서 Response객체에 할당됩니다. 일반적으로 서버에 Request를 전송하고 Response를 받아오는 함수들은 비동기로 작동하여 Request를 보낸 직후 반환되어 버리는데, 바로 이 부분에서 responseJSON 
메서드가 Escaping Closure의 형태로 작성되어 있기 때문에 값이 전부 들어온 이후에야 Data타입이 JSON 형식으로 변경될 수 있는 것입니다. 아래 completionHandler 부분을 보면 responseJSON 메서드가 
Escaping Closure 형태로 작성되어 있는 것을 볼 수 있습니다."

<br>

* AutoLayout

* IBDesignable & IBInspectable

* Swift vs Objective-C 

* Cocoapods

  * Xcode 내 Cocoa 환경에서 작업하는 프로젝트에서 오픈 소스 라이브러리(Open source library) 를 사용할 수 있게 해주는 역할 및 관리해주는 툴로서, 디펜던시 매니저(Dependency Manager) 라고도 불린다. 

<br>

* ARC vs non-ARC / (ARC 관련) Strong, Weak, Unowned 의 개념

* Apple 공식 문서 번역 : ARC [Part. 1](http://atelier-chez-moi.tistory.com/37) / [Part. 2](http://atelier-chez-moi.tistory.com/40)

<br>

* ARC와 Block, GCD 와 연관해서 설명해보세요

* Static 키워드

* Overloading vs Overriding

* Access Control 의 종류와 특징

* Delegate 와 Protocol 의 차이는 무엇일까요 ?

* Rxswift 란 무엇일까요 ?

* HIG(Human Interface Guideline) 을 알고 있나요 ?

* 옵셔널(Optional) 의 개념에 대해 설명할 수 있나요 ?
  * 옵셔널은 스위프트에서 새롭게 등장한 개념으로, 프로그램의 안정성을 높이기 위해서 마련되었다고 볼 수 있다. 값을 처리하는 과정에서 잠재적으로 값이 없는 문제가 발생할 수 있다. 이럴 경우 오류를 발생시키는 것이 아니라, 값이 없다는 뜻으로서 'nil'을 반환한다. 결국 옵셔널 타입이 가질 수 있는 값은 nil 인 경우와 nil 이 아닌 경우가 있다.

  * 그렇다면 옵셔널 값은 어떻게 사용해야 할까 ? 대표적인 방법으로 옵셔널 바인딩을 사용한다. 이 방법은 옵셔널 값이 nil 이 아닌 경우 안전한 방법으로 그 값을 받아내는 것을 뜻한다. if 문을 이용하여 nil 여부를 확인하고 nil 이 아닐 경우 값을 할당함으로서 옵셔널을 해제할 수 있다. 

  * 물론, 스위프트는 옵셔널과 옵셔널이 아닌 값은 철저히 다른 타입으로 인식한다. 쉬운 예로 Int 와 Optional Int 는 철저히 다른 타입이 된다. Optional Int 를 옵셔널 바인딩 혹은 강제 해제로 옵셔널을 해제시켜주어야 비로소 같은 타입이 된다. 

<br>

#### (Additional) Objective-C

* Block vs Non-block ?

* Block 코드가 무엇이며 사용 방법과 장점, 단점은 ?

* assign / retain 의 설명과 차이점은 ? 

* delegate 프로퍼티를 assign 속성을 주는 이유?

* Auto release pool을 동작 설명?

* NSString *b = @"test";
NSString *a = [b copy]; 
에서 a와 b는 같은가? (주소값 포함)
