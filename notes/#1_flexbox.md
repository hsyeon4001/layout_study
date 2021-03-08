####1.0 Life Before Flexbox

- 웹 사용기기가 다양해지면서 스크린 크기도 다양해짐
- 다양한 스크린 크기에 맞는 디자인이 필요해짐
- flexbox 등장

####1.1 First Rule of Flexbox

- flexbox는 children과 상호작용 X, 대신 container가 필요함
- container: box들의 바로 상위인 부모 box. 자식 box들의 위치를 조정할 수 있음.
- container로 만들려면 container에 해당하는 box의 스타일에 `display: flex` 적용

####1.2 Main Axis and Cross Axis

- flex container의 flex-direction 기본값은 row.
- justify-content: main axis 방향으로 flex children 위치 변경
- align-items: corss axis 방향으로 flex children 위치 변경
- main axis: flex 방향과 수평한 축
- cross axis: flex 방향과 수직인 축

####1.3 Column and Row

- `flex-direction: column` 적용 시 main axis, cross axis가 row일 때와 반대로 적용. 적용되는 box를 90도 회전해서 세운다고 생각하기
