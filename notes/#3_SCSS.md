#### 3.0 CSS Preprocessors and Set Up

- SCSS: CSS의 전처리기로 고유 문법을 통해 쉽게 CSS 작성 가능. variables, function, extend 등 프로그래밍 언어의 기능을 가짐

#### 3.1 Variables and Nesting

- \_파일명.scss: 파일명 앞에 언더바 사용 시 css로 컴파일하지 않음
- $: 변수 생성 키워드. 사용은 scss파일에서 css처럼 @import "파일명"
- nesting: 같은 부모 아래 자식 element들에 스타일이 적용될 경우 이를 하나로 묶어서 작성함. nesting 안에 nesting도 가능.
- &: nesting 안에서 :hover, :active 등 가상 클래스를 위해 부모 이름을 적어야 할 경우 &로 대체 가능

#### 3.2 Mixins

- mixins: scss functionality를 재사용할 수 있게 하는 기능
- `@mixin name() {}`
- 매개변수로 일정한 스타일링에 색상 등 종류가 바뀔 경우 매개변수를 사용하면 재사용에 용이함. 상황에 따라 다른 스타일 적용을 원할 경우.
- `@if 조건문 {} @else {}`: 인자로 전달된 값에 따라 조건문 적용 가능

#### 3.3 Extends

- 다른 코드를 확장해 재사용하고 싶을 경우. 중복되는 스타일링을 분리할 수 있음
- %: extend 사용 키워드
