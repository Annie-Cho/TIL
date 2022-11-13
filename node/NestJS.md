# NestJS
- 서버 측 애플리케이션 개발에 있어 아키텍처의 문제를 해결하기 위해 등장하였다.
- Express는 사용하기도 쉽고 성능도 뛰어나지만 아키텍처에 관한 정의나 기능을 제공해주고 있지는 않다.
- NestJS를 활용하여 아래와 같이 다양한 아키텍처를 정의할 수 있다. 따라서 다른 개발자가 작성한 코드를 쉽게 이해할 수 있다.
<p align="center">
<img width="700" alt="스크린샷 2022-11-13 오후 11 32 53" src="https://user-images.githubusercontent.com/99185757/201527201-e30b7a10-b55a-496d-aa12-4cf5bade2c39.png">
</p>
<br>

## NestJS의 구성

NestJS 홈페이지의 샘플 코드를 통하여 어떻게 세분화가 되어 나뉘어져있는지 알 수 있다. 크게 Module, Resolver(=Controller), Service로 나눌 수 있고 models에는 저장할 data 객체를, dto에는 argument로 입력받아올 input data객체를 명시해줄 수 있다.
<p align="center">
<img width="796" alt="스크린샷 2022-11-13 오후 11 35 51" src="https://user-images.githubusercontent.com/99185757/201527329-02da7666-2a46-4439-ba92-2ca2ab8b55b1.png">
</p>

### Module
- Resolver와 Service를 이어주는 부분이라고 볼 수 있다. 이렇게 생성된 Module은 recipe 기능 밖의 app.module.ts에 import되어 사용된다.
<p align="center">
<img width="799" alt="스크린샷 2022-11-13 오후 11 36 20" src="https://user-images.githubusercontent.com/99185757/201527348-5ae957d2-ad3c-434a-80cd-e8d07c85ec48.png">
</p>
  
### Resolver(=Controller)
Resolver에서는 Request를 연결된 service로 넘겨준다. 이 때, 입력받은 Argument(Args)를 넘겨줄 수 있다. Resolver를 통하여 service에 있는 기능들을 이용하면서 DI(의존성주입)이 가능해졌다.
<p align="center">
<img width="813" alt="스크린샷 2022-11-13 오후 11 38 21" src="https://user-images.githubusercontent.com/99185757/201527449-9f0ee404-27a4-4839-af3c-232d46ca39d2.png">
</p>
  
### Service
Service는 아래와 같이 CRUD가 실질적으로 일어나는 곳이라고 생각하면 된다.
<p align="center">
<img width="791" alt="스크린샷 2022-11-13 오후 11 39 15" src="https://user-images.githubusercontent.com/99185757/201527484-f9d123b6-8cce-44a8-ae46-ba6fb307cc21.png">
</p>

### Models
Models에는 저장할 data를 아래와 같은 객체 형태로 선언할 수 있다.
<p align="center">
<img width="794" alt="스크린샷 2022-11-13 오후 11 39 48" src="https://user-images.githubusercontent.com/99185757/201527515-d5803f3b-d3e0-4fa2-bff9-3950edebf7f9.png">
</p>

### DTO
DTO에는 입력받은 값을 argument로 넘겨줄 때의 input data를 아래와 같은 객체 형태로 선언해야한다.
<p align="center">
<img width="797" alt="스크린샷 2022-11-13 오후 11 40 26" src="https://user-images.githubusercontent.com/99185757/201527546-1bc2d97c-14b3-41fd-bef0-e5a00f9349e4.png">
</p>
