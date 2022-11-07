> 💡 npm과 yarn은 둘 다 지속적으로 관리가 되고 있고 추가적인 업데이트로 인하여 패키지 관리자로써 모두 훌륭하다. 따라서 무엇을 고를 지는 정말 본인의 취향 차이일 듯..

<br>

# npm과 yarn

- npm과 yarn은 `Node.js의 패키지 관리자`이다.
- 개발자 누구나 [npm 레지스트리(온라인 플랫폼)](https://www.npmjs.com/)에 패키지를 만들어 게시하거나 공유하면 npm, yarn과 같은 명령어를 통해 패키지 설치 및 삭제가 가능하다. (패키지들은 오픈소스)
- CLI(Command-Line Interface), `명령 줄 인터페이스`를 통하여 패키지 설치, 삭제 및 패키지 버전 관리와 의존성 관리를 편리하게 할 수 있다.

<br>

# npm

- npm, Node Package Manager
- Node.js의 `디폴트 패키지 관리자`이다. 노드를 설치하면 자동으로 설치가 된다.
- [npm 레지스트리(온라인 플랫폼)](https://www.npmjs.com/)을 제공하여 준다.
  - npm 레지스트리에는 사람들 누구나 Node.js 오픈소스 패키지를 만들고, 게시하고 공유할 수 있다.
  - npm 레지스트리(온라인 플랫폼)에 출시된 패키지들은 모든 사람들이 검색하고 사용할 수 있다.
- `명령 줄 인터페이스`이다.
  - npm 레지스트리를 통하여 툴을 설치할 수 있고 삭제할 수도 있다.

<br>

# yarn

- yarn, Yet Another Resource Negotiator
- 페이스북에서 만든 `JavaScript 패키지 관리자`이다.
- Node.js와 사용하기 위해서는 따로 설치를 진행해주어야 한다. (npm intall yarn --global)
- npm과 비슷한 기능을 지원한다. NPM 레지스트리나 GitHub 저장소에 등록된 툴 설치, 삭제를 진행할 수 있고 패키지 dependencies 또한 관리할 수 있다.
- npm 레지스트리와 호환하면서 `속도나 안정성 측면에서 npm보다 향상`되었다.

<br>

# npm과 yarn의 차이점

### 1. 속도

- npm은 한 번에 하나씩 패키지를 설치하지만 `yarn은 여러 패키지들을 동시에 가져오고 설치할 수 있도록 최적화`되어 있어 npm보다 속도가 훨씬 빠르다.

### 2. 보안

- npm은 자동으로 패키지에 포함된 다른 패키지 코드를 실행하지만 `yarn은 yarn.lock이나 package.json에 있는 파일들만 설치`한다.
- 보안은 yarn의 핵심 기능 중 하나이지만 최근 npm의 업데이트에서 npm의 보안 업데이트도 크게 향상되었다.

### 3. 명령어

- 아래와 같이 각 패키지 관리자에 따라 명령어가 다른 것을 확인할 수 있다.
<p align="center">
<img src="https://user-images.githubusercontent.com/99185757/200278789-806d4ed1-889f-49cd-92b0-bc2e60b89160.jpeg">
</p>
