## GraphQL(Graph Query Language)

- 페이스북에서 2015년에 발표한 쿼리이다. Rest를 대체할 수 있다.
- API를 위한 쿼리 언어(Query Language)이며 타입 시스템을 사용하여 쿼리를 실행하는 서버 사이드 런타임이다.
- 클라이언트가 서버로부터 데이터를 가져오는 목적으로 사용한다.

### 쿼리 언어

- 정보를 얻기 위해 보내는 질의문을 만들기 위해 사용되는 컴퓨터 언어이다.

<br>

## GraphQL의 단점

- 파일 업로드
    - 자체적으로는 돌아갈 수 없어서 Graphql-upload를 사용하고 있는데 이런 저런 충돌문제가 자주 발생한다.
- 클라이언트가 직접 필요한 데이터를 스스로 받아와야 하므로 문법 상의 문제가 발생할 경우가 있다.
    
    - 실제로 클라이언트 쪽에서 데이터가 불러지지 않는다고 하여 서버를 확인하였으나 이상이 없어 함께 확인하다보니 클라이언트에서 API를 호출 시 문법이 틀려 데이터를 가지고 오지 못하는 경우가 있었다.

<br>

## Rest-api와 GraphQL-api의 차이점

- 엔드포인트의 차이 : Rest-api의 경우 수많은 엔드포인트로 나누어져 있지만 GraphQL의 경우 한개로 합쳐져 편리하게 사용할 수 있다.
- method의 차이 : Rest-api는 CRUD마다 사용하는 method가 존재하지만 GraphQL의 경우 데이터 조회 시에는 Query를, 데이터를 조작할 시에는 Mutation을 사용한다.
   
<p align="center">
<img width="654" alt="스크린샷 2022-11-20 오후 11 41 02" src="https://user-images.githubusercontent.com/99185757/202908500-3de1596f-7042-42e4-98ed-e63b056b1bb0.png">
</p>
  
- 자체적인 Api-docs의 지원 : Rest-api의 경우 개발 시 직접 API docs를 swagger와 같은 툴을 사용하여 만들어야 한다. 하지만 GraphQL은 Apollo Client / Server를 사용하여 자체적인 API docs를 지원해준다. Rest-api의 경우 Schema-first이고 Graphql의 경우 Code first를  적용하여 자동으로 api 명세를 업데이트시킨 후 플레이그라운드라는 IDE(통합 개발 환경)에서 API를 테스트하거나 세부적인 명세를 확인할 수 있다.
- API호출 시 모든 데이터를 가져오는 Rest-Api와는 달리 GraphQL은 필요한 데이터만 선택하여 가져올 수 있다.

