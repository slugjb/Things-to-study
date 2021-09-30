#### Spring
***
## RequestMapping

특정 url로 요청하면 controller에서 어떠한 방식으로 처리할지 정의하는데,

이때 들어온 요청을 특정 method와 mapping하기 위해 사용

함과 동시에 다른 origin에서 내 resources에 함수로 접근하지 못하게 하기 위해 사용된다.

* GET
  * 캐시 가능
  * 브라우저 히스토리에 기록 저장
  * 북마크 가능
  * 길이 제한 O
  * 데이터 요청에만 사용
  * 보안 매우 취약
  * http 메시지에 body 없음
  * 멱등(idempotent)이다
  
  get을 통한 요청은 url 주소 끝에 파라미터로 포함되어 전송되며, 이를 query string라고 부른다.
  
  ex) www.ex.com/sample?name=value?name2=value2

* POST
  * 캐시 불가
  * 브라우저 히스토리 저장 안됨
  * 북마크 불가
  * 길이 제한 X
  * http 메시지에 body 있음
  * 멱등(idempotent)이 아니다

  post는 전송할 데이터를 http 메시지 body 부분에 담아서 서버로 보낸다.
  
  body의 타입은 Content-Type 헤더에 따라 결정 된다.

## PathVariables
## @RequestBody 와 @RequestParam
## Spring Boot Application
## Autowired
## RequiredArgsConstructor
## POM -> Gradle
***
#### React JS
***
## 클래스형 컴포넌트
  * 특징
      1) render()메소드와 Component 상속 필수
      
  * 단점
      1) state, props 사용 불편
      2) 많은 메모리 사용

## 함수형 컴포넌트
   * 특징
       1) 간편한 컴포넌트 선언 및 프로그래밍 가능
       2) Reack Hook 사용
   
   * ~~단점~~
       1) ~~state와 생명주기(Life Cycle) 사용을 위해서는 클래스형으로 구현해야 함~~
            => useState, useEffect 사용(React Hook)
      
      

## package.json
 1) 정의
   * 프로젝트의 정보를 정의하고, 의존하는 패키지 버전 정보를 명시하는 파일이다.
   * 프로젝트의 정보 - name, verson 영역
   * 패키지 버전 정보 - dependencies 또는 devDependencies 영역
   
 2) 프로젝트 정보
   * package.json 파일은 반드시 name과 version 항목을 포함해야 한다.
   * name -> 소문자 한 단어로 이루어져야한다. 하이픈( - )과 언더스코어( _ )가 포함 될 수 있다.
   * version -> x.x.x 형식을 따라야 하며, 작성 큐칙을 ```시맨틱 버저닝``` 이라고 한다.

 3) 패키지 정보
   * "dependencies": 프로덕션 환경에서 응용 프로그램에 필요한 패키지
   * "devDependencies" 로컬 개발 및 테스트에만 필요한 패키지

## 시맨틱 버저닝
   dot을 기준으로 3영역 Major, Minor, Patch로 나뉜다.
![image](https://user-images.githubusercontent.com/64000158/135395088-9fcbfd11-2440-429f-a1a5-f237233e76b2.png)

  >작성 규칙

  ![image](https://user-images.githubusercontent.com/64000158/135395178-5041b73e-e3c2-4ba5-9cb1-b725bf6869df.png)
  
## 틸드(~)와 캐럿(^)
 1) 틸드(tilde)
``` 
   "devDependencies": {
      "@vue/cli-service": "~4.3.0",
   },
```
   해당 패키지의 패치 레벨 변경을 허용하겠다는 의미이다.
    4.3.0 이상, 4.4.0 미만과 같은 의미이다.

2) 캐럿(caret)
```
  "dependencies": {
     "vue": "^2.6.11"
   }
```
   해당 패키지의 마이너, 패치 변경을 허용하겠다는 의미이다.
   2.6.11 이상, 3.0.0 미만과 같은 의미이다.
   
   
## State와 Props(Properties)
 1) State
      컴포넌트의 상태를 나타내며, 컴포넌트 내부에 선언되기 때문에 변할 수 있으며,      
      이러한 state는 외부에 공개하지 않고, 컴포넌트가 스스로 관리한다.      
      state로 사용되는 주된 값으로는 리스트에서 선택된 값, 체크박스 체크값, 텍스트 박스의 값 등등.
      
      * 상태에 따라 변하는 것
      * 직접 변경 가능
      * state가 변경되면 컴포넌트를 다시 렌더링 해야함
      * 외부에는 비공개, 컴포넌트 스스로 관리

2) Props
      State와의 간단한 차이로는, 변할 수 없다는 것이다. 컴포넌트는 상속하는 부모 컴포넌트로부터,
      props를 받고, 이 props는 상속받은 컴포넌트 내에서 수정이 불가능하다.
      react에서는 부모 -> 자식 일방향성 상속이기 때문이다.
      
      * 읽기 전용
      * 부모 요소에서 설정
      * 초깃값과 자료형의 유요성 검사가 가능

![image](https://user-images.githubusercontent.com/64000158/135398430-be860b15-b3c6-434f-9fd2-4055a8bb30e8.png)



## Entity code
 * 마크업 언어와 충돌하는 것을 방지하기 위해 HEML에서 규정한 문자열의 코드 

     특정 문자열을 코드로 표기한 집합이다.
     
## JSX
 * Javascript 와 XML를 합쳐서 탄생한 기존 자바스크립트의 확장 문법
 * 스크립트 내부에 마크업 코드 작성 가능
 * 변수나 프로퍼티의 바인딩 가능


ex) 코드 작성 예시
```
 ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```
↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓↓
```
const element = <h1>Hello, world!</h1>;
 
ReactDOM.render(
  element,
  document.getElementById('root')
);
```

## 바벨(Babel) - 6to5
 ES6(ECMAScript 6)를 ES5(ECMAScript 5)로 변환해준다.
 
 JSX를 브라우저가 읽기 쉬운 ES5 코드로 변환해주고, 이를 바탕으로 개발자가 
 
 최신 문법을 사용하면서도 여러 브라우저에서 작동될 수 있는 환경 제공
 
## Fragments -  ``` <Fragment> </Fragment> ``` or ```<> </> ```

 React의 일반적인 패턴은 component가 여러개의 요소를 반환하는 것이다.
 
 React의 규칙 중 하나로, Virtual DOM에서 컴포넌트 변화를 감지해 낼 때 효율적으로 
 
 비교 할 수 있도록 컴포넌트 내부는 하나의 DOM트리 구조로 이루어져야 하기 때문이다.
 
 Fragments를 사용하면 DOM에 별도 노드를 추가하지 않고 자식 목록을 그룹화 할 수 있다.
 
 ## 펼침 연산자(spread operator)
  * 배열에 포함된 항목을 목록으로 바꿔주는 연산자이다.
  * ...  으로 표시한다.
  * 단독으로 쓰일 수 없다.
  * 목록으로 바꿨다면 이를 배열이나 객체 등에 담아주어야 한다.
       ※ 변수에 담게 되면 에러 발생
  ```
  const class1 = [1, 2, 3];
  const a = ...class2; // X
  const a = [...class2]; // O
  ```
  가장 큰 장점은 조작(mutation)이나 부수 효과(side effect)로 인한 문제를 피할 수 있다.
  또한, push(), splice(), concat()등의 배열 메소드를 외울 필요 없이 간결하게 코드 작성이 가능하다.
  위 메소드들은 원본 배열 값을 변경하는데, 펼침 연산자는 원본 배열을 변경하지 않는다.
 ```
  const class1 = [1, 2, 3];
  const class2 = [4, 5, 6];
  
  // concat()
  const class3 = [...class1, ...class2]; 
  console.log(class3); // [ 1, 2, 3, 4, 5, 6 ] 
  
  // push() 
  const class4 = [...class1, 7];
  onsole.log(class4); // [ 1, 2, 3, 7 ] 
  
  // splice() 
  const class5 = [...class1.slice(0, 2)]; 
  console.log(class5); // [ 1, 2 ]
```
 이 외에도 함수의 매개변수에 값을 전달할 때도 코드를 편하게 관리 할 수 있다.
 ```
 const student = ['John', 19, 'A+'];
 
 function introduce(name, age, grade) {
   console.log(`${name}(${age}) - ${grade}`);
 } 
 
 introduce(student[0], student[1], student[2]); // John(19) - A+
 
 introduce(...student); // John(19) - A+
```

## VDOM
## DOM(Document Object Model)
## BOM(Browser Object Model)
 
## React - Hook
   https://ko.reactjs.org/docs/hooks-intro.html 
    분석 필요
    
    React component는 클래스형과 함수형으로 나뉘는데, 기존의 개발방식은 함수형을 주로 사용하되
    state나 life cycle method를 사용해야 할 때만 클래스형을 사용하는 방식.
    
    state나 life cycle method를 사용해야 할 때는 클래스형 사용.
    
    생명주기 먼저 공부
    
  
## React Component 생명주기  // VDOM 개념 필요

  모든 컴포넌트는 
   초기화 -> 업데이트 -> 소멸 단계를 거치게되고,
   각 단계에서 메소드들이 정해진 순서대로 호출되는데,
   이때 호출되는 메소드를 생명 주기 메소드라고 부른다.


  * class형 component 생명주기
  
  * 마운트(생성)
   1) state, context, defaultProps 저장
   2) componentWillMount
   3) render
   4) componentDidMount

      Mount : 컴포넌트가 처음 실행 되는 것
      
      컴포넌트가 시작되면 우선 state, context, defaultProps 저장 하고 후에,
      componentWillMount 메소드를 호출한다. 그리고 render로 컴포넌트를 DOM에
      부착한 후 Mount가 완료된 후에 componentDidMount가 호출된다.
      
      주의할 점은, componentWillMount단계에서는 props나 state를 바꾸면 안 된다.
      Mount 중이기 때문이고, 아직 DOM에 render하지 않았기 때문에 DOM에도 접근할 수 없다.
      componentDidMount에서는 DOM에 접근할 수 있기 때문에, 여기서는 주로 AJAX 요청이나,
      setTimeout, setlnterval같은 행동을 한다.
      
   * 업데이트 - 리액트 컴포넌트가 업데이트 되는것을 말함

      업데이트가 발생하는 경우
        1) props가 바뀔 때
        2) state가 바뀔 때
        3) 부모 컴포넌트가 리렌더링될 때
        4) 강제로 트리거를 발생시킬 때

      호출하는 메소드
        1) static getDerivedStateFromProps
        2) shouldComponentUpdate
              > 컴포넌트가 다시 렌더링을 해야 할지 말아야 할지 결정하는 메소드이다.
                초기 렌더링 혹은 forceUpdate()호출시에는 호출되지 않는다.
                렌더링을 방지하여 성능을 최적화하는 목적으로 사용한다.
        3) render
        4) getSnapshotBeforeUpdate
              > render 메소드 호출 후 DOM 변화를 반영하기 직전에 호출되니ㅡㄴ 메소드
              > 여기서 return된 값을 componentDidUpdate에서 3번째 파라미터로 받아 올 수 있다.
        5) componentDidUpdate
              > 리렌더링을 완료한 후 실행되는 메소드.
              > 최초 렌더링 시에는 호출되지 않음.
              > 컴포넌트가 업데이트 되었을 때, DOM을 조작하기 위해 사용
              >  ※ 주의 : componentDidUpdate에서 setState를 사용하면 무한 렌더링
              >            우려가 있으므로 조건문을 잘 작성해야한다.

   * 마운트 해제(제거)  - 리액트 컴포넌트가 DOM상에서 제거되는 것
        1) componentWillUnmount
              > 컴포넌트가 DOM에서 제거되기 직전에 호출되는 메소드이다.
              > 타이머를 제거하거나 데이터구독해제등의 목적으로 사용된다.
              >   ※ 주의 : componentWillUnmount가 호출된 컴포넌트는 다시
              >             렌더링 하지 않으므로, setState를 호출하면 안된다.
              
      
 ## useEffect - life cycle를 대채하는 Hook    
  

#### 보충 필요, 매우 중요 (정리 및 공부)
***

## CORS(Cross-Origin Resource Sharing)

http header를 사용해서 appcation이 다른 origin의 resources에 접근 할 수 있도록

함과 동시에 다른 origin에서 내 resources에 함수로 접근하지 못하게 하기 위해 사용된다.

## Log4j / Slf4j

  * log4j
      > 자바 기반 로깅 유틸리티, 디버그용 도구로 주로 사용된다.
      > 애플리케이션에 문제 발생 시, 로깅을 활성화하면 문제의 위치를 정확히 파악할 수 있다.
      > 속도 및 성능에 영향을 미치지 않고 편리하게 사용할 수 있다.
    
    참고 : https://cheershennah.tistory.com/80 , https://cofs.tistory.com/354
 
  * slf4j
      > log4j, logback, commons-logging 같은 로깅 프레임워크를 위한 추상화를 제공해준다.

  

