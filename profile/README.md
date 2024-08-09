# 현대인의 멘탈 케어 다이어리 SODA🍀
![1](https://github.com/user-attachments/assets/7fda93f0-f2d7-4fd3-8b6b-48bc0f75d953)

* 배포 URL :
* Test ID :
* Test PW :

## 프로젝트 소개

- SODA(소다)는 삶이 지치고 힘든 사람들의 스트레스를 해소하고 소소하지만 확실한 행복을 기록하는 현대인의 멘탈케어 다이어리입니다.
- 사용자는 오늘의 일기를 작성하면 AI가 사용자 맞춤형 코멘트를 달아줍니다.
- '오늘의 기분전환' 탭을 통해 작성한 일기를 바탕으로 기분전환을 할 수 있는 활동들을 추천받을 수 있습니다.
- 일기를 쓰거나 자신이 쓴 댓글이 채택되면 포인트가 쌓이며, 쌓인 포인트로 기부도 가능합니다.


## 팀원 구성

<div align="center">

| **김정주** | **이예림** | **오승민** | **오현우** | **곽현민** | **류동현** |
| :------: |  :------: | :------: | :------: | :------: | :------: |
| [<img src="https://github.com/user-attachments/assets/103798ae-f186-4604-b473-76ce83f76f92" height=200 > <br/> @KimJJRoSY](https://github.com/KimJJRoSY) |  [<img src="https://github.com/user-attachments/assets/35da7876-58b2-4a1a-b5e7-76ab64fa61ca" height=200> <br/> @yerimi00](https://github.com/yerimi00) | [<img src="https://github.com/user-attachments/assets/68677def-b098-49e5-95aa-37c95739ff34" height=200> <br/> @seung876](https://github.com/seung876) | [<img src="https://github.com/user-attachments/assets/71bef990-264e-4fd9-a206-efe83ccd14de" height=200 > <br/> @HyunWoo9930](https://github.com/HyunWoo9930) | [<img src="https://github.com/user-attachments/assets/51367291-260d-4402-9f87-27da589d5290" height=200> <br/> @sadew1112](https://github.com/sadew1112) | [<img src="https://github.com/user-attachments/assets/beb0c141-ec20-40d1-9840-3ba50ce15bcb" height=200> <br/> @wayne4918](https://github.com/wayne4918) | 


<div align="left">
  
## 1. 개발 환경

- Front : HTML, React, styled-components, Recoil
- Back-end : 
- 버전 및 이슈관리 : Github, Github Issues, Github Project
- 협업 툴 : Discord, Notion, Gather
- 서비스 배포 환경 : 
- 디자인 : [Figma](https://www.figma.com/design/cVcFM9sAudq5GgkZmKy9cP/2024-%EC%A4%91%EC%95%99%ED%95%B4%EC%BB%A4%ED%86%A4%5B%EC%86%8C%EB%8B%A4%5D?node-id=42-3&t=n99vWUJC0qUFUwLS-1)
  
<br>

## 2. 채택한 개발 기술과 브랜치 전략

### React, styled-component

- React
    - 컴포넌트화를 통해 추후 유지보수와 재사용성을 고려했습니다.
    - 유저 배너, 상단과 하단 배너 등 중복되어 사용되는 부분이 많아 컴포넌트화를 통해 리소스 절약이 가능했습니다.
- styled-component
    - props를 이용한 조건부 스타일링을 활용하여 상황에 알맞은 스타일을 적용시킬 수 있었습니다.
    - 빌드될 때 고유한 클래스 이름이 부여되어 네이밍 컨벤션을 정하는 비용을 절약할 수 있었습니다.
    - S dot naming을 통해 일반 컴포넌트와 스타일드 컴포넌트를 쉽게 구별하도록 했습니다.
    
### Recoil

- 최상위 컴포넌트를 만들어 props로 유저 정보를 내려주는 방식의 경우 불필요한 props 전달이 발생합니다. 따라서, 필요한 컴포넌트 내부에서만 상태 값을 가져다 사용하기 위해 상태 관리 라이브러리를 사용하기로 했습니다.
- Redux가 아닌 Recoil을 채택한 이유
    - Recoil은 React만을 위한 라이브러리로, 사용법도 기존의 useState 훅을 사용하는 방식과 유사해 학습비용을 낮출 수 있었습니다.
    - 또한 Redux보다 훨씬 적은 코드라인으로 작동 가능하다는 장점이 있었습니다.
- 로그인과 최초 프로필 설정 시 유저 정보를 atom에 저장하여 필요한 컴포넌트에서 구독하는 방식으로 사용했습니다.

### eslint, prettier

- 정해진 규칙에 따라 자동적으로 코드 스타일을 정리해 코드의 일관성을 유지하고자 했습니다.
- 코드 품질 관리는 eslint에, 코드 포맷팅은 prettier에 일임해 사용했습니다.
- airbnb의 코딩 컨벤션을 참고해 사용했고, 예외 규칙은 팀원들과 협의했습니다.
- 협업 시 매번 컨벤션을 신경 쓸 필요 없이 빠르게 개발하는 데에 목적을 두었습니다.

### 브랜치 전략

- Git-flow 전략을 기반으로 main, develop 브랜치와 feature 보조 브랜치를 운용했습니다.
- main, develop, Feat 브랜치로 나누어 개발을 하였습니다.
    - **main** 브랜치는 배포 단계에서만 사용하는 브랜치입니다.
    - **develop** 브랜치는 개발 단계에서 git-flow의 master 역할을 하는 브랜치입니다.
    - **Feat** 브랜치는 기능 단위로 독립적인 개발 환경을 위하여 사용하고 merge 후 각 브랜치를 삭제해주었습니다.

<br>

## 3. 프로젝트 구조

```
//프로젝트 구조를 작성해주세요
```

<br>

## 4. 역할 분담

### 👑FE 팀장 : 김정주

- **UI**
    - 페이지 : 
    - 공통 컴포넌트 : 
- **기능**
    - 기능 : 

<br>
    
### 👑BE 팀장 : 오현우

- **기능**
    - 기능 : 

<br>

### ✨FE : 이예림

- **UI**
    - 페이지 : 
    - 공통 컴포넌트 : 
- **기능**
    - 기능 : 

<br>

### FE : 오승민

- **UI**
    - 페이지 : 
    - 공통 컴포넌트 : 
- **기능**
    - 기능 : 
    
<br>

### BE : 류동현

- **기능**
    - 기능 : 

<br>

### BE : 곽현민

- **기능**
    - 기능 : 

<br>

## 5. 개발 기간 및 작업 관리

### 개발 기간

- 전체 개발 기간 : 
- UI 구현 : 
- 기능 구현 : 

<br>

### 작업 관리

- GitHub Projects와 Issues를 사용하여 진행 상황을 공유했습니다.
- 주간회의를 진행하며 작업 순서와 방향성에 대한 고민을 나누고 Notion에 회의 내용을 기록했습니다.

<br>

## 6. 신경 쓴 부분


  
<br>

## 7. 페이지별 기능



<br>

## 8. 개선목표


  
<br>

## 8. 프로젝트 소감

<br>

### 김정주
- 소감 3줄 부탁드려요~!

 ### 이예림
- 소감 3줄 부탁드려요~!
  
 ### 오승민
- 소감 3줄 부탁드려요~!

### 오현우
- 소감 3줄 부탁드려요~!

### 류동현
- 소감 3줄 부탁드려요~!

### 곽현민
- 소감 3줄 부탁드려요~!



  
<br>
