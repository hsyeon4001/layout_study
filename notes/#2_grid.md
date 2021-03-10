#### 2.1 Life Before Grid

- `justify-content: space-between` 등을 할 경우 빈 공간을 채우기 위해 child 간의 간격이 달라짐. 이를 일일이 조정하지 않고, 일정한 격자(grid) 형태를 만들기 위해 grid가 생겨남

#### 2.2 CSS Grid Basic Concepts

- `display: grid` 후 grid-template-columns와 grid-template-rows로 열과 행의 각 box 크기를 지정. 선언 수보다 box 수가 많을 경우 마지막 지정 값이 적용됨
- column-gap: margin과 유사. 각 column 사이 거리를 지정

#### 2.3 Grid Template Areas

- `grid-template-columns: 200px 200px 200px 200px` => `grid-template-columns: repeat(4, 200px)`
- `grid-area: 영역 이름` 선언 후 `grid-template-area: ""`로 레이아웃 구성. '.'으로 공백 생성

#### 2.4 Rows and Columns

- grid-column-start: column의 시작 위치(line) 지정
- grid-column-end: column의 끝 위치(line) 지정
