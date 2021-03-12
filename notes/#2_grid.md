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

#### 2.9 Place Content

- items vs. content: items는 각 cell, content는 전체 grid
- justify-content/align-content: container 범위 내에서 grid 전체의 수평/수직 위치를 조정
- place-items vs. place-content: 각 cell 하나 하나에 적용 vs 전체 grid에 같이 적용

#### 2.10 Auto Columns and Rows

- align-self처럼 self 들어갈 경우 해당 cell만 조작 -> container가 아니라 cell에 적용해야함
- `place-self: justify-self align-self`
- 추가되는 element(grid)에 대해 지정된 스타일이 없다면 css는 자동으로 default인 사이즈 없는 grid를 집어넣음
- grid-auto-rows: 지정하지 않은 개수의 rows에 대해 크기를 미리 정해둠
- grid-auto-flow: default 값은 row. column 설정 시 여분의 div가 column으로 생성됨

#### 2.11 minmax

- minmax: 1fr처럼 container 크기에 따라 유동적인 값의 경우 grid의 원하는 최소, 최대 크기를 설정. ex) `grid-template-columns: repeat(10, minmax(100px, 1fr))`

#### 2.12 auto-fit auto-fill

- auto-fit, auto-fill: repeat()에 사용. 반응형에 유용
- auto-fill: grid에 지정된 column의 개수 범위에서 가능한 많은 column을 만듦. 만들어야 할 column(element) 수보다 범위가 넓으면 빈 공간으로 보임
- auto-fit: container의 수평 범위에 맞게 column 크기를 조정해 화면을 꽉 채움

#### 2.13 min-content max-content

- min-content, max-content: content가 필요한 최대/최소 크기만큼 grid 크기가 조정됨
