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

#### 2.5 Shortcuts

- `grid-column: start line / end line`
- 끝 위치는 -1로 대체 가능 => line 수에 상관 없이 끝부터 -1, -2 -3... 적용
- `grid-column: 2 / span 4`: 시작(끝) 위치 대신 box의 크기를 지정
- 같은 행(열)의 시작 위치 전부 지정 안할 경우 요소 순서대로 자리잡음

#### 2.6 Line Naming

- container의 column/row 개수 선언 시 `grid-template-columns: [first-line] 100px [second-line] 200px`처럼 naming 가능.

#### 2.7 Grid Template

- fr: fraction. grid container 크기를 기준으로 나눔 => pixel 처럼 크기 계산 필요하지 않음.
- `grid-template-columns: 1fr 2fr 1fr`: 1대 2대 1 비율로 container column을 나눔
- row의 경우 명시적 height 선언 후 fr 적용 가능
- grid-template: "naming" + 높이 / 각 column의 width 한 번에 선언 가능. repeat는 사용 불가능.

#### 2.8 Place Items

- justify-items, align-items: default는 stretch. 부모 container에 속하는 property로 grid의 크기를 조절해 grid 범위를 채움
- `place-items: align justify`
