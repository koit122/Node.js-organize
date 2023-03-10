# 인용
[https://hanamon.kr/nodejs-%EA%B0%9C%EB%85%90-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0/](https://hanamon.kr/nodejs-%EA%B0%9C%EB%85%90-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0/)
# 시작 전 기초지식
빌드(Build)
```plaintext
소스 코드 파일을 컴퓨터에서 실행할 수 있는 독립적인 형태로 변환하는 과정
exe파일을 생성 작업을 통칭해서 빌드라고 한다.
```
런타임(Runtime)
```plaintext
프로그래밍 언어가 동작하는 환경
```
모듈(module)
```plaintext
프로그램을 구성하는 구성요소로, 관련된 데이터와 함수를 하나로 묶은 단위
```
번들(bundle)
```plaintext
프로젝트 개발에 사용한 여러 모듈을 하나로 묶어내는 작업을 의미한다.
```
패키지
```plaintext
모듈과 동일한 의미로 쓰인다.
```
난독화
```plaintext
작성된 코드를 읽기 어렵게 만드는 작업니다. 빌드된 결과(제품)은 브라우저에 해석되는 용도이기 때문에 용량을 축소하고, 읽기 어렵게 만드는 등 최적화를 하는것이 좋다.
```

# Node.js
## Node.js란
Node.js는 Chrome V8 javaScript엔진으로 빌드된(위에서 동작하는) JavaScript 런타임  
자바스크립트의 문법을 해석하고 그것을 실제로 동작시킬수 있는 엔진  

즉,노드를 통해 **다양한 자바스크립트 애플리케이션을 실행**할 수 있으며,  
서버를 실행하는데 가장 많이 사용된다.

## Node.js가 필요한 이유
웹 브라우저에서는 html, css ,js만 동작을 한다. 앞의 3개만으로도 웹 제작이 가능하지만 상당히 비효율 적이다. 그래서 개발을 도와주는 여러가지 모듈들을 설치해서 사용하게 된다. 해당 모듈들에서 제작한 코드들은 다시 html,css,js로 변환을 해야하는데 이를 컴퓨터에 변환작업을 명령해야한다 그 명령이 돌아가는 환경이 node.js이다. 

JavaScript언어는 웹 브라우저 안에서만 동작을 하는 언어이다.(스크립트 언어는 특정 프로그램 안에서만 동작)이 javaScript를 브라우저에서 독립시키기 위해 나온것이 Node.js이다. Node.js를 통해 터미널 프로그램에서 바로 실행시킬수 있다.(컴퓨터에서 실행할수 있게 만든다) 이로써 브라우저와 무관한 프로그램을 만들고 명령할수 있게된다. 여기서 중요한 것은 Node.js를 이용하여 **서버를 만들 수 있다**는 것이다.

중요한 이유는 이전까지 Server-Client 웹사이트를 만들 때 웹에서 표시되는 부분은 JavaScript 를 사용하여 만들어야만 했으며, 서버는 Reby, Java 등 다른 언어를 써서 만들었어야 했는데 마침내 한 가지 언어로 전체 웹 페이지를 만들 수 있게 된 것이다.

## Node.js 설치
1.[https://nodejs.org/ko/](https://nodejs.org/ko/)사이트 접속  
LTS(Long Term Supported)장기적으로 안정되고 신뢰도가 높은  
지원이 보장되는 버전으로, 유지/보수와 보안(서버 운영 등)에 초점을 맞춰  
대부분 사용자에게 추천되는 버전이다.

최신버전은 최신기능들이 있지만 업데이트가 자주 일어나고 변경사항이 많다.  

개발자로서 일하다보면 최신버전이나 LTS버전이 아닌 다른 버전에서 작업을 해야할 경우가 생기게 된다. 그래서 노드버전메니저를 설치해서 사용하는것이 좋다.(NVM)

## node.js 터미널 명려어
명령어 | 기능 
|--|--|
node --version | 현재 사용되고있는 node의 버전 확인

# nvm
## nvm
node.js의 버전을 관리해주는 프로그램이다.
## nvm가 필요한 이유
개발자로서 일하다 보면 최신 버전이나 LTS버전이 아닌 다른 버전에서 작업을 해야할 경우가 생기게 된다.  
1.프로젝트마다 최적의 버전이 다를 수 있기 때문   
2.팀 단위에서 사용하는 버전이 정해져 있는 경우  
그래서 노드버전메니저를 설치해서 사용하는것이 좋다.(NVM)  
## nvm설치
1.nvm-windows검색  
2.README.md에서 Download Now 클릭  
3.nvm-setup.zip다운로드  
4.압축풀어서 가져오기 
## nvm 터미널 명려어
명령어 | 기능 
|--|--|
nvm --help | nvm의 명령어들을 출력한다.
nvm ls | nvm가 가지고 있는 버전의 리스트를 출력
nvm install verson | node.js의 verson을 설치한다.
nvm uninstall verson | node.js의 verson을 삭제한다.
nvm use verson | 해당 verson으로 변경/사용 하겠다.
## 버전 추천
2022년 기준 10이상의 버전을 추천하며 일반적인 경우 12버전을 추천한다.  


# npm
## npm란
전 세계의 개발자들(개인, 회사 등)이 만든 다양한 기능(패키지, 모듈)을 관리한다.  
여러 개발자들이 업로드하는 곳을 npm(생태계)라고한다.  
그리고 이런 여러 패키지들을 터미널에서 install하여 우리의 프로젝트에 설치하여  
사용할 수 있게 된다.
## npm필요한 이유
link태그와 script태그를 활용하여 외부의 저장소에 연결하여 패키지를  
가져오는 방식은 원시적인 방식이다.    
현재의 방식은 node.js환경에서 npm을 사용하여 각각의 패키지들을 설치하고  
가공처리를 걸쳐서 결과물로써 만든다.  
물론 npm를 이용하여 패키지를 관리할 시 원시적인 방식보다 구성이 복잡해지고,  
학습해야할 양이 늘어나게 되지만  관리 효율이 증가하고 손쉽게 기능을 고도화 시킬 수 있게된다.  
또한 적은 시간으로도 고기능의 패키지를 추가할 수 있게 된다.
## 프로젝트 내부에 버전관리(git)이 필요하지 않는 파일과 폴더
.cache, dist, node_modules파일은 터미널에서 후작업을 통해 만들어진 폴더들이기에 
해당 폴더들은 npm명령어로 언제든 다시 동일한 버전으로 설치가 가능하기 때문에 버전관리를 해주지 않는다. 그 이유는 언제든 명령어로 설치가 가능한 폴더들은 계속해서 버전관리를 해주게 되면 외부 저장소에 파일을 보낼때 마다 시간도 오래걸리고, 용량 등 비효율적이기 때문이다. 그렇기에 특정 조치를 취해 버전관리 목록에서 제외하는것이 좋다.  
버전관리 목록에서 제외하기
```plaintext
프로젝트의 루트경로에 .gitignore를 생성하고 해당 파일 안에 폴더나 파일을 명시해 버전관리를 하지 않겠다는 선언을 해준다.
ex)
.cache/dist/node_modules
>>>.cache, dist, node_modules폴더 3개가 gitignore(무시)처리 되었다.
```
## npm설치
npm(node package manager)
npm은 node.js설치 시 자동으로 설치가 된다.  

프론트엔드 개발자는    
웹 브라우저에서 동작하는 js 이해  
웹페이지를 만드는 컴퓨터 환경을 제어하는 js도 이해해야한다. 

js문법을 배워서 브라우저와 컴퓨터 환경을 제어할 수 있다.  
프론트 엔드 개발에서는 컴퓨터를 많이 제어하지는 않는다.

## npm 터미널 명령어
명령어 | 기능
|--|--|
npm init -y | 프로젝트 생성
npm install "package" | 일반 응용성 package를 설치한다.
npm install "package"@0.0.0 | 0.0.0q버전의 일반 응용성 package를 설치한다. 
npm install "package" -D | 개발용 의존성package를 설치한다. 
npm run "명령어" | npm명령을 통해서 내부(프로젝트)에서 "명령어"를 동작시킨다 
npm info "package" | 설치된 패키지의 버전을 확인한다.
npm update "package" | 패키지를 업데이트 한다.
## npm로 만들어진 패키지 구조
```json
{
  "name": "npm-test",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "parcel-bundler": "^1.12.5"
  },
  "dependencies": {
    "lodash": "^4.17.21"
  }
}
```
객체옵션 | 값
|--|--|
mane | 프로젝트의 이름
version | 프로젝트의 버전
description | 프로젝트에 대한 간단한 설명
main | npm생태계에 업로드할때 필요한 값이다.
scripts | 현재의 프로젝트 내부에서 사용할 수 있는 스크립트 명령들을 명시한다.
keywords | 프로젝트 관련 키워드
author | 작가라는 뜻으로 소유주
license | 라이센스에 대한 언급
devDependencise | 개발용 응존성 패키지 설치 내역 기록
Dependencise | 일반 응용성 패키지 설치 내역 기록
  
## npm 터미널 명령어 추가 정보 & 질문
package 설치 시 설치하지 않은 다른 패키지들이 설치되는 이유설치한 
```plaintext
패키지를 사용할 때 필요한 패키지들도 같이 설치된 것이다.
```
devDependencies와 Dependencies의 필요성
```plaintext
패키지를 손실(실수, 사고 등)이 일어났을때 해당 설치 내역 기록을 통해  
패키지들을 다시 설치할 수 있게된다.
```
패키지 설치시 생성되는 package-lock.json의 필요성
```plaintext
npm을 통해 설치한 패키지들의 내부에서 작동하는 다른 패키지(패키지 개발시 사용된 패키지)들에 대한 정보가 저장된다.
package.json 수동관리
package-lock.json 자동관리
```
개발성 의존성 패키지와 일반 응용성 패키지의 차이
```plaintext  
개발성 의존성 패키지 : 개발 당시에만 필요한 페키지로 웹 브라우저의
                     동작에는 필요하지 않는 패키지
일반 응요성 패키지   : 웹 브라우저에서 동작하는것을 전제하는 패키지  
```

# npm을 사용한 개발서버 실행과 빌드
vs플러그인을 사용해서 개발용 서버를 열고 해당 페이지를 보는것은  
원식적인 방법이다.
## parcel-bundler 명령어
parcel-bundler는 로컬상 오픈서버 개방 + 배포용으로 빌드하기 위한 패키지
명령어 | 기능
|--|--|
parcel index.html | 로컬(컴퓨터)환경에서 개발용 서버 오픈, 브라우저에서 프로젝트 확인
parcel build index.html | 인터넷상에 업로드한는 용으로 index.html을 빌드한다.  dist파일을 생성하고 프로젝트를 난독화 해준다.


## npm을 이용한 개발서버 오픈
1. npm을 이용하여 parcel-bundler를 개발성 의존성 페키지로 설치한다.
1. package.json의 옵션중 scripts 부분에 "dev" : "parcel index.html"을 넣는다.  
선언시 프로젝트 내부에서만 동작하게 된다.
1. 터미널에 npm run dev 를 명령한다.  
npm명령을 통해서 dev(scripts부분)을 동작시키겠다.  
## 일반 응용성 패키지 사용법
1. main.js(패키지가 필요한 모든 파일에서 가능)에 import _ from "ladash(패키지)"입력  
패키지에서(from) 가져와(import) _에 저장한다.  
npm을 통해 미리 설치된 패키지 내부에 있는 package.json내부의 main옵션에 명시되어있는 패키지.js파일을 실제로 가지고와 main.js에 적용한다.
---
## mpm을 사용한 개발서버 실행과 빌드 추가 정보 & 질문
### 추가정보
1. 코드추가후 저장을 안하면 터미널은 변경사항을 인식하지 못한다.  
### 질문
npm을 이용하여 패키지를 설치 후 터미널 명령 불가 이유
```plaintext  
npm를 통해 설치한 패키지는 로컬(컴퓨터)가 아닌 프로젝트에 설치된 것이기 때문에 터미널에서 동작을 명령하면 해당 프로그램은 로컬에 없기때문에 실행되지 않는다.  
```
scripts옵션의 값으로 꼭 dev라는 이름을 써야하는가?
```plaintext  
그렇지 않다.  
원하는 이름을 지정해 주어도 된다.(변한 이름으로 터미널 명령을 해아한다.) 
```
# 유의적 버전
유의적 버전관리란 package.json의 dependencies옵션의 버전값에서 ^를 넣고 뺌 으로써,  버전을 고정시켜 버리거나 major버전을 제외한 버전을 업데이트 하거나 하는등 상황에 맞게 사용할수 있게 해주는 것이다.
## 버전의 구성
^major.minor.patch로 구성이 되어있다.
버전 | 설명
|--|--|
^ | major을 제외한 minor, patch 버전을 언제든 최신화 하겠다.
maior | 이전 버전과 호환되지 않는 새로운 버전으로 바뀔때 +1된다.
minor | 기존 버전과 호환이 가능하며, 기능만 추가된 버전으로 바뀔때 +1된다.
patch | 기존 버전과 호환이 가능하며, 버그 및 오타등 자잘한 수정이 이루어졌을떄 +1된다.
## 버전 확인하기
npm info package
## 패키지의 특정 버전을 지목하여 설치하기
npm install package&0.0.0
## 패키지를 업데이트 하기
npm update package  
패키지를 업데이트 할 수 있는 이유는 package.jsom의 dependencies옵션값인 버전에 ^가 붙어있어 minor, patch 버전의 변경은 업데이트가 가능하다.(major 버전은 불가)  
만약 dependencies옵션값에 ^를 제거하고 명령어를 실행 시 명령이 바로 취소되며 버전을 업데이트 하지 않는다.
## 버전관련 정보 & 질문
### 정보
1. 설치하려고 하는 패키지가 이미 프로젝트에 설치되어 있다면 해당 버전의 패키지 위에 덮어씌어진다.
### 질문
dependencies에 기록된 패키지의 버전이 실제와는 다를수도 있고, 이에따라 이를 확인하는 방법
```plaintext
1.node-modules폴더에 들어가기
2.해당 패키지 폴더에 들어가기
3.package.json 파일로 들어가 version 옵션의 값을 확인하기
```