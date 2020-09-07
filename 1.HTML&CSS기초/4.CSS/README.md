# CSS

- CSS : Cascading Style Sheets

  - HTML(마크업 언어)을 꾸며주는 언어
  - HTML은 웹 페이지의 <b>정보</b>를 표현하고,  CSS는 웹 페이지의 <b>디자인</b>을 담당

  - 대다수의 웹 페이지는 10여 개의 HTML 태그를 이용하여 만들어졌지만, CSS로 인해 매우 다양함



### CSS 문법

- HTML과 비슷하게 속성과 값의 집합으로 나타낼 수 있음

- 꾸밀 대상인 요소와 그에 대한 스타일 내용으로 이루어짐

  ```css
  h1 { color:yellow; font-size:2em;}
  ```

  - 선택자(selector)  : h1
  - 속성(property) : color
  - 값(value) : yellow
  - 선언(declaration) : color:yellow, font-size:2em
  - 선언부(declaration block) : {color:yellow, font-size:2em;}
  - 규칙(rule set) : h1{color:yellow;font-size:2em;}

- 주석

  ```css
  /* 주석 내용 */
  ```

- CSS의 적용

  - Inline

    - 해당 요소에 직접 스타일 속성을 이용해서 규칙을 선언

    - 선택자는 필요하지 않고, 선언부의 내용에 스타일 속성의 값으로 원하는 스타일을 표기

      ```html
      <div style="color:red;">내용</div>
      ```

  - Internal

    - \<head> 태그 내의 \<style> 태그에 스타일 규칙을 선언

      ```html
      <style> div {color : red;} </style>
      ```

  - External

    - 외부 스타일 시트 파일을 이용하여, 별도의 외부 파일을 삽입
    - 확장자는 .css이며, css 파일이라고 부름

    - \<link> 태그를 이용하여 CSS 파일을 연결

      ```html
      <link rel="stylesheet" href="css/style.css">
      ```

      - rel 속성 : 연결되는 파일과 문서와의 관계를 정의, CSS 파일의 경우 <i>stylesheet</i>로 지정

    - 여러 많은 페이지에서도 \<link> 태그를 이용하며 모든 페이지에 같은 스타일 적용 가능

    - 파일 관리가 편하며, 용량이 작기 때문에 주로 사용

  - Import

    - 스타일 시트 내에서 다른 스타일 시트 파일을 부르는 방식

    ```css
    @import url("css/style.css");
    ```

    

### 선택자

- SELECTOR

- 요소 선택자(태그 선택자)

  - 선택자 부분에 태그의 이름이 들어감
  - 해당 선택자의 요소에 스타일 규칙이 적용됨

  ```css
  h1{color:yellow;}
  h2{color:yellow;}
  ```

  - 쉼표를 이용해 그룹화가 가능

  ```css
  h1, h2{color:yellow;}
  ```

  - 별표(asterisk)를 이용하면 모든 요소를 선택 가능

  ```css
  *{color:yellow;}
  ```

  

- CLASS 선택자

  - 가장 일반적으로 스타일 규칙을 적용할 수 있음
  - 태그의 class 속성 값을 이용

  ```css
  .foo {font-size:30px;}
  ```

  ```html
  <p class="foo">Hi</p>
  ```

  - CLASS 선택자의 제일 앞 부분엔 .을 넣어야 함

  - 다중 CLASS

    ```css
    .foo{font-size:30px;}
    .bar{color:yellow;}
    ```

    ```html
    <p class="foo bar">Hi</p>
    ```

    - 공백으로 구분하여 여러 class 값을 적용 가능

    

- ID 선택자

  - CLASS 선택자와 비슷하지만, .대신 #을 사용
  - 속성 값으로 id 값을 사용

  ```css
  #foo {background-color:red;}
  ```

  ```html
  <p id="foo">Hi</p>
  ```

  - 문서 내의 유일한 요소에 사용해야 하기 때문에, 하나의 태그에서만 사용이 가능함

  

- 선택자의 조합

  - 요소와 클래스의 조합

    ```css
    p.bar {...}
    ```

  - 다중 클래스

    ```css
    .foo.bar{...}
    ```

    - class 속성에 foo와 bar가 모두 있어야 함

  - id와 class의 조합

    ```css
    #foo.bar{...}
    ```

    - foo라는 id에서 bar라는 클래스인 요소ㅋ



- 속성 선택자

  - 단순 속성으로 선택

    ```css
    p[class] {color:yellow;}
    p[class][id] {text-decoration:underline;}
    ```

    ```html
    <p class="foo">Hello</p>
    <p class="bar">Hi</p>
    <p class="cla" id="title">Bye</p>
    ```

    - 해당 속성을 가지고 있다면, 속성 값과는 관계 없이 style 적용 가능

  - 정확한 속성값으로 선택

    ```css
    p[class="foo"] {color:silver;}
    p[id="title"] {text-decoration:underline;}
    ```

    - 정확한 속성값을 가진 요소에만 스타일을 적용

  - 부분 속성값으로 선택

    - 속성의 이름과 속성 값 사이에 있는 기호에 따라 다른 동작
    - \[class~="bar"] : "bar"라는 단어가 있는 경우
    - \[class^="bar"] : "bar"라는 단어로 시작하는 경우
    - \[class$="bar"] : "bar"라는 단어로 끝나는 경우
    - \[class*="bar"] : "bar"라는 문자가 포함될 경우

    

### 문서 구조 관련 선택자

- 조합자(결정자) : 문서의 요소나 구조를 기반으로 선택자를 조합하는 것
- 부모와 자식
  - 해당 요소를 포함하는 가장 가까운 상위 요소, 각 요소의 부모 요소는 하나 뿐
  - 자식 요소는 부모 요소와 반대 개념이며, 여러 개를 가질 수 있음

- 조상과 자손
  - 부모와 자식의 관계와 비슷함
  - 조상 요소는 해당 요소를 포함하는 모든 상위 요소이며, 부모 요소를 포함하여 여러 개의 조상 요소를 가질 수 있음
  - 자손 요소는 해당 요소가 포함한 모든 요소

- 형제
  - 같은 부모를 가지고 있는 요소
  - 바로 뒤에 있는 형제 요소를 인접해 있다고 함

- 문서 구조 관련 선택자

  - 자손 선택자

    ```css
    div span{color:red;}
    ```

    - 선택자 사이에 기호가 없으며, 공백으로 구분

  - 자식 선택자

    ```css
    div > h1{color:red;}
    ```

    - \<div> 의 자식인 \<h1> 을 선택

  - 인접 형제 선택자

    ```CSS
    div + p{color:red;}
    ```

    - 인접 형제의 관계에 있는 것을 선택



### 가상 선택자

- 가상 클래스(pseudo class)

  - 미리 정해놓은 상황에 적용되도록 선언한 클래스

  - 요소 자체에 미리 클래스를 선언하는 것이 아닌, 특정 상황에만 적용하고 싶을 때 사용

  - [LINK](https://developer.mozilla.org/ko/docs/Web/CSS/Pseudo-classes)

    ```css
    :pseudo-class{
    	property:value;
    }
    ```

  - 문서 구조와 관련된 가상 클래스

    - :first-child : 첫 번째 자식 요소

    - :last-child : 마지막 자식 요소

      ```html
      <ul>
          <li>HTML</li>
          <li>CSS</li>
          <li>JS</li>
      </ul>
      ```

      ```css
      li:first-child {color:red;}
      li:last-child {color:blue;}
      ```

      - 이와 같이 사용하면, 직접 스타일을 지정하지 않더라도 HTML은 red, JS는 blue 색상으로 출력됨

  - 앵커 요소와 관련된 가상 클래스

    - :link : 아직 방문하지 않은 앵커

    - :visited : 방문한 하이퍼링크

      ```css
      a:link{color:blue;}
      a:visited{color:gray;}
      ```

  - 사용자 동작과 관련된 가상 클래스
    - :focus : 현재 입력 초점을 가진 요소
    - :hover : 마우스 포인터가 있는 요소
    - :active : 사용자의 입력으로 활성화된 요소, 순간적으로 활성화 됨

- 가상 요소
  - 미리 정의한 위치에 삽입이 되도록 선언한 요소
  - :before : 가장 앞에 삽입
  - :after : 가장 뒤에 삽입
  - <b>before와 after 가상 요소는 내용이 따로 없기 때문에, 반드시 content 속성을 이용하여 내용을 삽입해야 함</b>
  - :first-line : 요소의 첫 번째 줄에 있는 텍스트
  - :first-letter : 블록 레벨 요소의 첫 번째 문자



### 구체성

- 같은 요소를 나타내는 스타일이 여러 개가 존재한다면, 가장 구체적으로 나타낸 스타일이 적용됨

  ```css
  h1{color:red;}
  body h1{color:green;}
  ```

  - 위의 코드에서는 color:green가 적용됨

- 구체성의 순위

  1. id
  2. class
  3. 기타 요소

- important 키워드 : 모든 구체성을 무시하고 우선적으로 적용됨

  ```css
  h1{color:red !important;}
  ```



### 상속

- 부모의 스타일을 자식 클래스에서 상속 받음

  - 박스 모델 속성은 상속되지 않음

- 상속된 속성은 구체성을 가지지 않음

  ```css
  *{color:red;}
  h1#page{color:gray;}
  ```

  ```html
  <h1 id="page">Hello, <em>CSS</em></h1>
  ```

  - 위의 코드에서 CSS는 gray가 아닌 red가 적용됨



### 캐스케이딩

- 구체성이 같은 규칙이 정의될 경우

  ```css
  h1{color:red;}
  h1{color:blue;}
  ```

  - blue 색상이 적용됨

- cascading 규칙

  - 중요도(!important)와 출처

  - 구체성
  - 선언 순서