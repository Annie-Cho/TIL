# TypeScript
> JavaScript에 타입을 강제시키는 언어이다.

- 기존 JavaScript는 타입에 상관없이 값들이 변수에 들어갈 수 있으므로 매우 위험하다.
- ex) 경매 서비스에서 1인당 글쓰기 권한을 최대 5개로 지정해놓았다. 어느날 보니 누군가가 게시글을 5개 이상쓰며 게시판을 동일한 글로 도배를 해놓았다. 로직은 분명 다 짜여졌는데 기능이 작동하지를 않았다. 코드를 열어보니 작성한 게시글 갯수를 표현해주는 변수에 "01111111"이라는 값이 들어가 있었다. => JavaScript에서는 타입을 지정해주지 않기 때문에 문자열로 선언된 후 +1을 해주면 정수 1의 값이 되는 것이 아니라 문자열 "01"이 되는 것이다.
- TypeScript에서는 타입 지정을 해주기 때문에 위와 같은 문제가 발생하지 않는다.

## JavaScript와 TypsScript 표현의 차이점
```javascript
/* JavaScript에서는 가능 */
let hello = "안녕하세요"
hello = 123     //처음 선언할 때는 String타입이었으나 123과 같은 정수를 대입해도 전혀 문제가 되지 않는다.

/* TypeScript에서는 불가 */
let hello: string = "안녕하세요"
hello = 123     //ERROR!!! 선언할 때 이미 string타입으로 지정되어있으므로 정수인 123을 대입할 수 없다.
```

## TypeScript에서는 꼭 타입을 붙여줘야할까?
- 타입은 꼭 붙여주어야 한다. 만약 선언할 때 타입 선언을 안하고 값을 대입하였을 경우 TypeScript는 해당 값을 통해 타입을 추론하여 개발자가 알려주지 않더라도 변수의 타입을 명시해놓는다.
- 만약 변수가 가질 수 있는 타입이 2개 이상이라면? 아래와 같이 선언하여 사용할 수 있다.
```javascript
let money: number | string = 1000     //number타입 또는 string타입이 가능하다.
money = "5000원"
```

## VSCode사용 시 설치 방법
- Nestjs로 new하여 새로운 개발용 폴더를 만든다면 굳이 아래와 같은 커맨드를 이용하여 설치할 필요 없다.
```text
yarn init
yarn add typescript --dev
yarn add ts-node
```
