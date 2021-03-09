#### 1.0 Life Before Flexbox

- 웹 사용기기가 다양해지면서 스크린 크기도 다양해짐
- 다양한 스크린 크기에 맞는 디자인이 필요해짐
- flexbox 등장

#### 1.1 First Rule of Flexbox

- flexbox는 children과 상호작용 X, 대신 container가 필요함
- container: box들의 바로 상위인 부모 box. 자식 box들의 위치를 조정할 수 있음.
- container로 만들려면 container에 해당하는 box의 스타일에 `display: flex` 적용

#### 1.2 Main Axis and Cross Axis

- flex container의 flex-direction 기본값은 row.
- justify-content: main axis 방향으로 flex children 위치 변경
- align-items: corss axis 방향으로 flex children 위치 변경
- main axis: flex 방향과 수평한 축
- cross axis: flex 방향과 수직인 축

#### 1.3 Column and Row

- `flex-direction: column` 적용 시 main axis, cross axis가 row일 때와 반대로 적용. 적용되는 box를 90도 회전해서 세운다고 생각하기
- 세로 방향으로의 위치 변경은 부모 box의 height에 비례해서 변경됨 -> height 값이 없으면 위치 변화 없음

#### 1.4 align-self and order

- align-self: align-items와 같은 효과지만 해당 box 하나만 적용
- order: 같은 위치 내의 box 순서를 변경. HTML 변화 없이 순서를 변경하고 싶을 경우 사용. child에 적용 가능한 property. 모든 box의 defalut order는 0 => 0보다 큰 값을 줄수록 순서가 뒤로 밀림

#### 1.5 wrap, nowrap, reverse, align-content

- flexbox는 item들을 같은 줄에 있도록 유지 -> flex 상태일 경우 width를 지정해도 그보다 작아질 수 있음
- flex-wrap: 기본값은 nowrap. child의 크기를 결정하는 property로 wrap시 child의 크기를 유지 -> 한 줄 이상 넘어갈 수 있음
- `flex-direction: row-reverse`: 정렬 순서 역순화
- reverse화는 `flex-wrap: wrap-reverse` 등 다른 property에서 복합 적용 가능
- align-content: 줄나눔. wrap으로 한 줄 이상 flexbox가 넘어갈 경우의 line 간 거리를 수정

#### 1.6 flex-grow, flex-shrink

- flex-shrink: 공간이 부족할 때의 element의 행동을 정의함. 기본값은 1, 그 이상은 다른 child보다 지정 값만큼 더 줄어듦
- flex-grow: 공간이 남을 때의 element의 행동을 정의함. flex-shrink와 반대로 동작함

#### 1.7 flex-basis

- child에 적용되는 property element의 최초 width를 정의. width의 변화가 발생하지 않을 경우 width와 동일하므로 굳이 사용하진 않음
