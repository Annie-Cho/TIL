## 📌 Nestjs

- 효율적이고 확장 가능한 Node.js 서버 측 애플리케이션을 구축하기 위한 프레임워크

### Nestjs의 특징

- 확장이 가능하고 유지 관리가 쉬운 서버 애플리케이션을 쉽게 개발할 수 있다.
- TypeScript를 적극적으로 도입함으로서 서버 개발 시 발생할 수 있는 오류들을 사전에 방지할 수 있도록 하였다.
- module을 통해 확장이 용이하도록 설계되어있다.
- Nest는 typescript를 사용하며 DI(Dependency Injection), IoC(Inversion of Control), 모듈을 통한 구조화 등의 기술을 통해 생산성이 높다.
- Nestjs 프로젝트가 생성된 후 디렉토리 구조는 아래와 같다.

<p align="center">
<img width="627" alt="스크린샷 2022-11-23 오후 11 43 26" src="https://user-images.githubusercontent.com/99185757/203575249-387626c4-9f02-4d44-ba47-21acf70da4c3.png">
</p>
  
- 사실,, 개인적으로 docs 또한 상세하게 잘 만들어져있는 게 마음에 든다.(사용자의 편리성?)

<br>

## 📌 Express

- 웹 및 모바일 애플리케이션을 위한 일련의 강력한 기능을 제공하는 간결하고 유연한 Node.js 웹 애플리케이션 프레임워크
- Node.js(서버에서 JavaScript가 작동되도록 해주는 런타임 환경)의 원칙과 방법을 이용하여 웹 애플리케이션을 만들기 위한 프레임워크이다.

### Express 특징

- 가장 많이 사용하는 node.js 프레임워크로 많은 개발자들에게 코드와 구조의 통일성을 향상시킬 수 있다.
- Typescript를 express에서 사용할 수 있지만, tsconfig.json, lint.json 등등의 json파일을 만들고 세팅하는 과정이 복잡하다.

<br>

## 📌 Nestjs와 Express의 차이점

- Nestjs는 아키텍처의 정의도 프레임워크에서 제공하기 때문에 각 개발자들의 아키텍처가 통일되고 서로 작성한 코드의 구조를 쉽게 파악할 수 있다.
- 라우팅의 차이 : Express는 라우팅을할 때 app.use처럼 등록해서 사용한다. 하지만 Nestjs는 모듈 별로 나누어서 라우팅을 한다.
>💡 라우팅 : 네트워크에서 경로를 선택하는 프로세스
    
- 컨트롤러의 차이 : Nestjs는 클래스 별로 컨트롤러에서 method에 데코레이터를 사용한다. Auth에서도 데코레이터를 사용한다.
    - 데코레이터는 클래스, 메타데이터를 참고해서 Nest가 라우팅 맵을 만들 수 있도록한다. 컨트롤러 내용에 맞게끔 요청을 묶어주는 용도?

<p align="center">
 <img width="630" alt="스크린샷 2022-11-23 오후 11 46 20" src="https://user-images.githubusercontent.com/99185757/203575872-3154c8cf-cb47-44c0-b36c-f1c65008e481.png">
</p>
    
- 서비스의 차이 : Nestjs의 경우 함수 인자로 인터페이스로 정한 값들이 들어온다.

<p align="center">
<img width="621" alt="스크린샷 2022-11-23 오후 11 47 32" src="https://user-images.githubusercontent.com/99185757/203576102-c9cb5b8a-6cde-4b89-920b-ba48b4e151ef.png">
</p>
