# What I learned_Day 1
2022.03.18
<br>

## 1. Semantic Markup
div 태그만 사용하던 시대는 지나갔다. HTML의 발전에 따라 아래의 태그로 스크린 리더의 접근성도 확장하고 직관적으로 보일 수 있다.
- Instead of divs
  - header
  - nav
  - article
  - section
  - aside
  - footer

## 2. HTML Emmet
VS code 에서 사용되는 emmet 을 이용하여 더욱 편하게 코드를 짤 수 있다.<br>
- nav>ul>li 입력후 Tab 을 누르면 아래의 코드가 자동으로 입력된다
  ```html
  <nav>
    <ul>
      <li>
      </li>
    <ul>
  </nav>
  ```
- ul>li*5
  ```html
  <ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
  </ul>
  ```
Emmet doc cheat_sheet : https://docs.emmet.io/cheat-sheet/

## 3. Table
- td, tr, th
  - td: table data 의 줄임 말로 표의 한칸인 cell 을 뜻한다
  - tr: table row 의 줄임 말로 표의 행(row)을 뜻한다
  - th: table head(thead 태그는 후술)의 줄임 말로 표의 제일 위의 행을 말하고 중복으로 만들 수 있으며 기본값은 bold로 처리된다

- thead, tbody, tfoot
  - thead: 표의 제일 위에 있는 헤드라인을 말하며 여러개의 th가 있다면 1개의 thead 아래에 속한다
  - tbody: 표의 전체적인 내용을 담은 부분
  - tfoot: 표의 가장 아래쪽에 위치하는 부분(예를 들어 합계, 평균 등에 쓰인다)

- colspan, rowspan Attribute
  - colspan: columnspan의 줄임 말로 열 범위를 뜻하며 attribute로 사용 하여 열의 크기를 지정할 수 있다
  - rowspan: 행 범위를 뜻하며 attribute로 사용하여 행의 크기를 지정할 수 있다 

## 4. Form
form은 일종의 컨테이너로 그룹화된 모든 입력을 담는 상자 라고 볼 수 있다 이 폼을 한데모아 어디로 보낼지(action)정할 수 있다.
- input elements
  - type
    -  text: text 를 입력할 수 있는 입력칸이 나온다
    -  password: 입력할 수 있는 입력칸이지만 입력을 하면 text 그대로가 아닌 ⦁ 으로 보여진다
    -  placeholder: text나 password 같은 입력칸에 입력하면 사라지는 문자를 보여준다(사용자에게 무엇을 입력하면 되는지 알려줄 수 있다)
    -  radio: 중복선택할 수 없는 여러가지 버튼을 제공 하며 name을 다른 버튼들과 하나로 통일해야 중복값에 체크되지 않는다 value(전달해야 될 값)도 넣어주자<br>
  - id: 해당 페이지 내에서 중복된 이름이 있어서는 안된다
  - name: id와 name은 통상적으로 같은 문자를 사용하며 name은 같은 이름을 여러곳에서 사용이 가능하다 radio 같이 중복되게 체크되지 않으려면 name의 이름을 같은걸로 바꿔주면 1개의 object로 취급된다
    
- label elements<br>
아주 중요한 요소로 사용자 혹은 관련자들의 접근성을 높이려면 꼭 써주는게 좋다

- required Attribute<br>
유효성 검사를 할 때 필요한 속성이며 사용자가 값을 넣지 않았다면 값을 넣지 않았다고 알려주며 그 다음 상황으로 진행되지 않는다

- select elements<br>
select 와 option은 짝이므로 꼭 같이 써주자 select 는 option의 목록을 선택 할 수 있는 창을 제공한다
