# REST API

## 📌 REST란?

- REST = REpresentational State Transfer = 브라우저 표현 상태의 변경
- 브라우저와 같은 웹 클라이언트는 URL과 같은 Resource Identifier(자원 식별자)를 통해 resource(자원)에 대해 어떠한 요청을 하고 그 결과를 받게된다. 받은 결과는 브라우저 화면에 새로운 내용이 디스플레이 되는 등의 방식으로 표현된다. 이 과정에서 브라우저 표현 상태의 변경이 일어나게 되는 것이다.

<br>

## 📌 REST의 구성 요소

- 자원(Resource) => URI(Uniform Resource Identifier)
- 행위(Verb) => [HTTP Methods](https://github.com/Annie-Cho/TIL/blob/master/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC/HTTP.md#%EC%9A%94%EC%B2%AD-%EB%A9%94%EC%86%8C%EB%93%9Crequest-method)
- 표현(Representations)

### URI와 URL

- `URI(Uniform Resource Identifier)` : Identifier, 식별자 라는 단어에서 볼 수 있듯이 인터넷에 있는 자원을 나타내는 유일한 주소이다.
- `URL(Uniform Resource Locator)` : Locator, 위치탐지기 라는 단어에서 볼 수 있듯이 네트워크 상에서 자원의 위치를 알려주는 규약이다.
- URI와 URL의 차이점
  - https://en.dict.naver.com/#/search?query=hello&range=all 이와 같은 주소가 있을 때,
  - URL : https://en.dict.naver.com/#/search => 말 그대로 자원의 위치를 알려준다. 참고로 URI이기도 하다.
  - URI : https://en.dict.naver.com/#/search?query=hello&range=all => 자원의 식별자로써 query와 range값을 이용하여 자원을 식별한다. URL은 될 수 없다.

<br>

## 📌 REST API 디자인

- URI는 정보의 자원을 표현해야한다.
- 자원(resource)에 대한 행위는 HTTP Methods로 표현한다. URI에 간접적으로 유추할 수 있는 행위를 표현하면 안됀다.

### REST API 규칙

- URI는 resource를 표현하는데 중점을 두고, 간접적으로 행위를 유추할 수 있는 단어가 들어가면 안됀다.(resource는 명사를 사용하여 작성한다.)

```text
//게시물 가져오는 URI
GET /boards/show/1      //wrong -> show와 같이 유추할 수 있는 단어는 안됀다.
GET /boards/1           //ok

//게시물 추가하는 URI
GET /boards/insert/2    //wrong -> POST를 사용하여 추가하는 행위를 나타내준다. 또한 위와 동일하게 insert와 같이 유추가능한 단어는 안됀다.
POST /boards/2          //ok
```

<br>

### URI설계 시 주의할 점

- 슬래시(/)는 계층 관계를 나타낼 때 사용된다.
- URI 마지막 문자로 '/'를 포함하지 않는다.

```text
https://www.test.com/boards/1
```

- 하이픈(-)을 사용하여 URI의 가독성을 높인다. `밑줄(_)은 사용할 수 없다.`

```text
https://www.test.com/users/validate-phone-number
```

- URI를 구성할 때에는 대문자 보다 소문자로 구성한다. 대소문자에 따라 다른 리소스로 인식할 수 있기 때문이다.
- 파일 확장자는 URI에 포함시키지 않는다. 대신 Accept 헤더를 사용하면 된다.

```text
https://www.test.com/photos/friends/photo-at-caffe.png  => wrong

GET / photos/friends/photo-at-caffe HTTP/1.1 Host: www.test.com Accept: image/png       //Host는 도메인 주소이다.
```

<br>

### 리소스 간의 관계를 표현하는 방법

- REST 리소스 간에는 연관관계가 있을 수 있는데, 이러한 경우에는 아래와 같이 URI를 표현한다.

```text
/리소스명/리소스 ID/관계가 있는 다른 리소스명
GET : /users/{userId}/devices
```

- 관계명이 복잡하다면 서브 리소스를 사용하여 표현할 수 있다.

```text
GET : /users/{userId}/likes/devices
```

## 참고

- https://meetup.toast.com/posts/92
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods
- https://inpa.tistory.com/entry/WEB-%F0%9F%8C%90-URL-URI-%EC%B0%A8%EC%9D%B4
