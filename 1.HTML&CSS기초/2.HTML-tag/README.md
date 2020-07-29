## HTML 태그

- HTML의 버전에 따라 새로운 태그가 생기기도 하고 없어지기도 함



1. 제목과 단락 요소

   - HEADING 태그

     ```html
     <h1>Hello</h1>
     ```

     - 문서 내에 제목을 표현하기 위해서 사용
     - 제목의 레벨에 따라 h1 ~ h6 까지 존재
     - 숫자가 낮을 수록 큰 제목을 의미

   - Paragraph 태그, Linebreak 태그

     ```html
     <p>
     	첫번째 단락
     </p>
     <p>
         두번째 단락 <br>
         두번째 단락
     </p>
     ```

     - \<p> : 단락을 나타내는 태그

     - \<br> : 줄바꿈을 나타내는 태그로, html에서는 공백을 무시하기 때문에 줄바꿈을 위해 사용, 닫기 태그와 내용이 존재하지 않는 빈 태그

       

2. 텍스트를 꾸며주는 요소

   ```html
   <p>
     <b> Bold </b>
     <i> Italic </i>
     <u> Underline </u>
     <s> Strike </s>
   </p>
   ```

   - \<b> : 글자를 굵게 표시
   - \<i> : 글자를 이탤릭체로 표시
   - \<u> : 글자에 밑줄을 표시
   - \<s> : 글자에 중간선을 표시



3. 앵커 요소

   ```html
   <a href="http://www.naver.com">네이버</a>
   ```

   - 링크를 생성하는 태그

   - a태그, 앵커 태그, 링크 태그 등 다양하게 불림
   - href(hypertext reference) 속성
     - 링크를 생성하기 위하여 반드시 가지고 있어야 함
     - href의 값은 링크의 목적지 url
   - target 속성
     - _self : 현재 화면에 표시하며, default 값
     - _blank : 새로운 창에 표시
     - _parent, _top : 프레임이라는 특정 조건에서만 동작하며, 요즘은 잘 쓰이지 않음
   - 기타 속성
     - [LINK](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)

   - 내부 링크
     - \<a> 를 통한 링크는 페이지 내부의 특정 요소로도 이동이 가능
     - href 속성 값에 #을 쓰고 이동하고자 하는 내부 페이지의 id 속성 값을 적으면 이동 가능
     - 웹 페이지 하단의 'top' 또는 '맨 위로 이동하기' 버튼이 해당



4. 의미 없는 요소를 묶기 위한 태그

   ```html
   <div>
       <span>Hello,</span> HTML
   </div>
   ```

   - 태그 자체에는 의미가 없으며, 요소들을 묶기 위한 용도로 사용
   - 스타일을 적용하거나, 서버에 전송할 데이터를 담기 위한 용도
   - HTML은 문서를 웹에 나타내기 위해 제작되었으나, 현재의 웹은 문서 형태에서 많이 벗어났기 때문에 자주 사용
   - \<div>
     - division의 줄임말, 블록 레벨 태그
     - 한 줄을 생성해서 내용을 표현
   - \<span>
     - 인라인 레벨 태그
     - 블록 레벨의 한 줄 안에서 나눠서 사용



5. 리스트 요소

   - 여러 내용을 나열하기 위해 사용
   - 리스트는 중첩도 가능
   - \<ul>, \<ol>의 자식으로는 \<li> 태그만 사용 가능

   - ul(unordered list)

     ```html
     <ul>
         <li>사과</li>
         <li>오렌지</li>
         <li>바나나</li>
     </ul>
     ```

     - 순서가 없는 리스트를 표현하기 위해 사용
     - 나오는 순서가 바뀌더라도 상관이 없는 경우

     > <ul>
     >     <li>사과</li>
     >     <li>오렌지</li>
     >     <li>바나나</li>
     > </ul>

     

   - ol(ordered list)

     ```html
     <ol>
         <li>물을 붓는다.</li>
         <li>물을 끓인다.</li>
         <li>라면을 넣는다.</li>
     </ol>
     ```

     - 순서가 있는 리스트를 표현하기 위해 사용
     - 나오는 순서가 바뀌면 안 될 경우

     > <ol>
     >     <li>물을 붓는다.</li>
     >     <li>물을 끓인다.</li>
     >     <li>라면을 넣는다.</li>
     > </ol>

   

   - dl(definition/description list)

     ```html
     <dl>
         <dt>사과</dt>
         <dd>빨간색</dd>
         <dt>오렌지</dt>
         <dd>주황색</dd>
         <dt>바나나</dt>
         <dd>노란색</dd>
     </dl>
     ```

     - 용어와 그에 대한 정의를 표현하기 위해 사용
     - \<ul>, \<ol>은 항목을 단순하게 나열하지만, \<dl>은 용어와 설명이 세트를 이룸
     - \<dt> : 용어를 나타내는 태그
     - \<dd> : 용어에 대한 정의 또는 설명을 나타내는 태그, 여러 개를 쓸 수 있음

     > <dl>
     >     <dt>사과</dt>
     >     <dd>빨간색</dd>
     >     <dt>오렌지</dt>
     >     <dd>주황색</dd>
     >     <dt>바나나</dt>
     >     <dd>노란색</dd>
     > </dl>



6. 이미지 요소

   ```html
   <img src="./image/apple.jpg" alt="사과">
   ```

   - 문서에 이미지를 삽입하는 태그로, 닫는 태그가 없는 빈 태그
   - src 속성 : \<img>의 필수 속성으로, 이미지의 경로를 나타냄
   - alt 속성 : 이미지의 대체 텍스트를 나타내며, src와 더불어 필수 속성
   - width, height 속성 : 이미지의 가로/세로 크기를 나타내는 속성
     - 값의 단위는 기본적으로 픽셀
     - 속성을 표기 하지 않으면 원본 크기대로 나타남
     - 둘 중 하나만 선언하면, 선언된 속성의 크기에 맞춰 비율이 변환됨

   - 상대 경로와 절대 경로

     ```html
     <!-- 상대 경로 -->
     <img src="./image/apple.jpg" alt="사과">
     
     <!-- 절대 경로 -->
     <img src="C:/users/document/image/apple.jpg" alt="사과">
     <img src="http://www.naver.com/apple.jpg" alt="사과">
     ```

     - 상대 경로는 현재 웹 페이지를 기준으로 이미지의 위치를 나타냄
       - "./"는 현재 페이지가 위치한 폴더
     - 절대 경로는 실제 이미지가 위치한 곳의 전체 경로를 나타냄

   - 이미지 파일 형식 : gif, jpg, png 등



7. 테이블 요소

   - 표를 나타내는 태그
   - 내용이 들어가는 칸인 셀(Cell)로 구성
   - 표의 가로 방향을 행(row), 세로 방향을 열(column)이라 부름
   - 표를 구성할 때는 위에서 밑으로, 좌측에서 우측으로 작성

   - 표의 구성 요소

     ```html
     <table>
         <tr>
             <th>1단</th>
             <th>2단</th>
         </tr>
         <tr>
             <td>1*1=1</td>
             <td>2*1=2</td>
         </tr>
         <tr>
             <td>1*2=2</td>
             <td>2*2=4</td>
         </tr>
     </table>
     ```

     - \<table> : 표를 나타내는 태그
       - \<table> 태그는 하나 이상의 \<tr> 태그를 가짐
     - \<tr> : 행을 나타내는 태그
       - 셀을 나타내는 \<th>, \<td>를 자식으로 가짐
     - \<th> : 제목 셀을 나타내는 태그
     - \<td> : 셀을 나타내는 태그

     <table>
         <tr>
             <th>1단</th>
             <th>2단</th>
         </tr>
         <tr>
             <td>1*1=1</td>
             <td>2*1=2</td>
         </tr>
         <tr>
             <td>1*2=2</td>
             <td>2*2=4</td>
         </tr>
     </table>
     

   - 표의 구조와 관련된 태그

     ```html
     <table>
         <caption>Summary</caption>
         <thead>
             <tr>
                 <th>Fruit</th>
                 <th>Price</th>
             </tr>
         </thead>
         <tbody>
             <tr>
                 <td>Apple</td>
                 <td>$1000</td>
             </tr>
             <tr>
                 <td>Orange</td>
                 <td>$500</td>
             </tr>
         </tbody>
     	<tfoot>
             <tr>
                 <td>Sum</td>
                 <td>$1500</td>
             </tr>
         </tfoot>
     </table>
     ```

     - \<caption> : 표의 제목

     - \<thead> : 제목 행을 그룹화

     - \<tfoot> : 바닥 행을 그룹화

     - \<tbody> : 본문 행을 그룹화

       <table>
           <caption>Summary</caption>
           <thead>
               <tr>
                   <th>Fruit</th>
                   <th>Price</th>
               </tr>
           </thead>
           <tbody>
               <tr>
                   <td>Apple</td>
                   <td>$1000</td>
               </tr>
               <tr>
                   <td>Orange</td>
                   <td>$500</td>
               </tr>
           </tbody>
       	<tfoot>
               <tr>
                   <td>Sum</td>
                   <td>$1500</td>
               </tr>
           </tfoot>
       </table>

   - 표의 병합
     - 속성이며 값으로 병합할 셀의 개수를 사용
     - rowspan : 셀을 세로방향으로 병합
     - colspan : 셀을 가로방향으로 병합
     
     

8. 폼 요소

   - 폼 요소는 서버에 데이터를 전달하기 위한 요소

   - \<input>

     - 내용이 없는 빈 요소로 type 속성을 통해 여러 종류의 값을 입력 받음

     - text 속성

       ```html
       <input type="text" placeholder="o o o">
       ```

       - 아이디, 이름, 주소, 전화번호 등 단순한 텍스트를 입력하기 위해 사용
       - placeholder 속성을 통해 사용자의 입력 전, 텍스트 박스에 값을 표시

       

     - password 속성

       ```html
  <input type="password">
       ```
     
       - 암호와 같이 공개를 하면 안 되는 내용을 입력할 때 사용
  - 텍스트 박스의 모양은 text 타입과 같지만, 실제로 값을 입력할 때는 값이 표시되지 않음
     
       

     - radio 속성

       ```html
  <input type="radio" name="gender">남자
       <input type="radio" name="gender">여자
  ```
     
       - 라디오 버튼을 만들 때 사용
       - 라디오 버튼은 중복 선택이 불가능
       - checked 속성 사용 가능

       
       
     - checkbox 속성

       ```php+HTML
       <input type="checkbox" name="fruit">사과
  <input type="checkbox" name="fruit">오렌지
       <input type="checkbox" name="fruit">바나나
  ```
     
  - 체크 박스를 만들 때 사용
       - 체크 박스는 중복 선택이 가능
       - checked 속성 사용 가능
     
       
       
- file 속성
     
       ```html
       <input type="file">
  ```
     
       - 파일을 서버에 올릴 때 사용
     
  
     
- submit, reset, image, button 속성
     
  ```html
       <input type="submit">
       <input type="reset">
       <input type="image" src="http://placehold.it/50x50?text=click" alt="click" width="50" height="50">
  <input type="button">
       ```

       - 클릭 가능한 버튼을 생성
  - submit : 값을 전송
       - reset : 값을 초기화
  - image : 이미지를 삽입할 수 있는 버튼
         - src, alt 속성이 반드시 필요함
  - button : 아무 기능이 없는 버튼 생성
     - 
       
     
   - \<select>
   
     ```html
  <select>
         <option>사과</option>
         <option>오렌지</option>
         <option>바나나</option>
     </select>
     ```
   
  - 선택 목록을 표시
     - multiple 속성을 사용하면 다중 선택 가능
     - \<select> 내부의 \<option>으로 각 항목을 나타낼 수 있음
       - \<option>의 속성으로 selected가 있으며, 선택된 항목을 의미
   
  
     
- \<textarea>
   
  ```html
     <textarea rows="5" cols="30">
     </textarea>
     ```
   
     - \<input type="text">는 한 줄만 입력이 가능하나, \<textarea>는 여러 줄의 텍스트를 입력받을 수 있음
     - 텍스트 상자의 크기를 조절하기 위한 rows, cols 속성이 존재
   
  
     
   - \<button>
   
     ```html
  <button type="submit|reset|button">버튼</button>
     ```
   
     - 버튼을 만들기 위해 사용
     - submit, reset, button의 세 가지 타입이 존재
     - 내용을 버튼 안에 직접 넣을 수 있음

     
   
- \<label>
   
     ```html
     <label for="name">이름</label><input type="text" id="name">
     ```

     - form 요소의 이름과 form 요소를 연결하기 위해 사용, 모든 form 요소에 사용 가능
     - label의 for 속성과 input의 id 속성값을 동일하게 생성
  - label을 클릭하면 연결된 form을 클릭한 것과 동일한 효과 발생
     - 각 form마다 label을 할당
     - 사용성, 접근성에서 중요한 역할을 하기 때문에 반드시 명시

     

   - \<fieldset>, \<legend>

     ```html
     <fieldset>
         <legend>
          정보
         </legend>
         ... 폼 ...
     </fieldset>
  ```
   
  - \<fieldset> : 여러 폼 요소를 그룹화하여 구조적으로 만들기 위해 사용
   
  - \<legend> : 폼 요소의 제목으로, \<fieldset> 내부에 가장 먼저 작성
   
    
   
   - \<form>
   
  ```html
     <form action="" method"">
         <fieldset>
             <legend>
                 정보
             </legend>
          ... 폼...
         </fieldset>
  </form>
     ```

     - action : 데이터를 처리하기 위한 서버의 주소
  - method : 데이터 전송 방식
       - get : 주소창에 파라미터 형태로 추가되어 데이터가 노출됨
       - post : 데이터가 노출되지 않음