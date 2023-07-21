# Sporting 어플리케이션
<div align="center">
        <img width="26%" src="https://user-images.githubusercontent.com/118786401/235388216-78fb76d0-b9ec-4dad-ab40-c12c2a86176b.png"/>
</div>

<br>

&nbsp; - Back-End 3명, Front-End 2명 (Back-End 팀장으로 참가) <br>
&nbsp; - 경기장 대여기업, 일반인, 관리자 3개의 Role을 두어, 각각의 UX/UI를 고려하여 기능구현 <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(상세 기능은 아래에서 설명)

<br>

## 개인 수행기능
### 전체요약
<div align="center">
    <img width="60%" src="https://github.com/aozp73/aozp73/assets/122352251/2455dd69-4c7d-4f08-96b5-090c8dd5f62f"/>
</div>

<br>

### 상세설명 (기술 블로그 포함)
- 테스트 - JPA Repository Test : DB 설계 후, Test 진행 ([JPA Repository Test - 기술 블로그](https://blog.naver.com/aozp73/223107831358))

<br>

- 경기장 - 등록 기능 : &nbsp;경기장 등록시 사전 S3에 넣어놓은 경기장 Default 사진을 함께 DB에 저장 (카테고리별로 상이)<br>
([등록 기능 - 기술 블로그 1](https://blog.naver.com/aozp73/223077210498)), ([등록 기능 - 기술 블로그 2](https://blog.naver.com/aozp73/223077219273))
- 경기장 - 리스트 조회 기능 : &nbsp;QueryString으로 넘어온 KeyWord값에 따라 카테고리에 맞는 경기장 리스트 응답<br>
([리스트 조회 - 기술 블로그 1](https://blog.naver.com/aozp73/223077309184)), ([리스트 조회 기능 - 기술 블로그 2](https://blog.naver.com/aozp73/223078084488))
- 경기장 - 기업 본인이 등록한 리스트 조회 기능 : &nbsp;이전 토픽과 동일하게 진행, JPA-QueryDSL활용<br>
([등록 리스트 조회 - 기술 블로그 1](https://blog.naver.com/aozp73/223078241849)), ([등록 리스트 조회 - 기술 블로그 2](https://blog.naver.com/aozp73/223078243514))
- 경기장 - 수정 페이지 요청 : &nbsp;수정 페이지 요청시, 미리 값이 입력될 수 있게 DB 조회 후 응답<br>
([수정 페이지 요청 - 기술 블로그 1](https://blog.naver.com/aozp73/223078516338)), ([수정 페이지 요청 - 기술 블로그 2](https://blog.naver.com/aozp73/223079160319))
- 경기장 - 수정 : 경기장 수정 페이지엔 코트 수정이 포함되어 있음. Java의 Map, Stream 문법 활용하여 진행 
([수정 - 기술 블로그](https://blog.naver.com/aozp73/223084822080))

<br>

- 예약&결제 - 경기장 예약 및 결제 기능 : &nbsp;BootPay를 통해 App이 넘겨준 데이터 검증 후 DB 저장 ([예약/결제 - 기술 블로그](https://blog.naver.com/aozp73/223093098448))
- 예약&결제 - 나의 경기장 예약 리스트 조회 : &nbsp;QueryDSL의 goe()를 활용해 유효한 리스트만 응답 ([예약 리스트 - 기술 블로그](https://blog.naver.com/aozp73/223093110031))
- 테스트 - SpringBoot 통합 테스트 : &nbsp;Topic 진행 완료 후, 통합 테스트 진행 ([통합 테스트 - 기술 블로그](https://blog.naver.com/aozp73/223096085205))
- API문서 - RestDoc 연동 (API 자동 문서화) : &nbsp;통합 테스트와 연계해 자동 API 문서화 활용 ([RestDoc - 기술 블로그](https://blog.naver.com/aozp73/223096094596))

<br>

- 관리자 - 이메일 전송 기능 구현 : &nbsp;간단한 구글 API를 활용하여 원하는 사용자에게 이메일 전송 ([이메일 API - 기술 블로그](https://blog.naver.com/aozp73/223089211518))
- 관리자 - 경기장 등록승인/비활성화/재활성화 기능 구현 : &nbsp;Status를 활용해 각 기능 구현 ([등록승인/비활성/재활성 - 기술 블로그](https://blog.naver.com/aozp73/223107834823))
- 관리자 - 통계 차트 구현 : &nbsp;관리자가 App을 운영함에 있어 관련 데이터를 통계로 보여주고 싶다는 취지로 진행<br>
([접속률 통계 - 기술 블로그](https://blog.naver.com/aozp73/223092115322)), ([게시글 조회수 - 기술 블로그](https://blog.naver.com/aozp73/223092170027))

<br>

### 팀원 공유 목적의 샘플 코드
#### S3
 - Github : https://github.com/aozp73/S3_Sample
 - Blog : https://blog.naver.com/aozp73/223107841108 

#### QueryDSL
 - Github : https://github.com/aozp73/querydsl
 - Blog : https://blog.naver.com/aozp73/223079188235

#### Admin (View, JPA - 페이징, 검색)
 - Github : https://github.com/aozp73/JPA-AdministratorSample_layout-paging-searching
 - Blog : https://blog.naver.com/aozp73/223107843272  

<br>

## 프로젝트 후기
### 느낀점
  ※ 1차 프로젝트에서 Mybatis를 활용하여 백엔드/프런트엔드 진행<br>
 &nbsp;&nbsp;&nbsp;&nbsp;2차 프로젝트에서 Mybatis를 활용하여 Restful 서버 구현 및 응답 DTO 입체적으로 진행
 <br> <br>
 &nbsp;&nbsp;JPA 학습 블로깅 : https://blog.naver.com/aozp73/223107860479 <br> <br>
 &nbsp; <b>1. JPA</b>
  - 인프런 강의 2~3개 듣고, 학원에서 기본 개념을 배운 상태에서 프로젝트에 도입
  - 프로젝트 중 QueryDSL, 영속성 컨텍스트, Dirty Checking, 스냅샵, Proxy 개념 등을 찾아보면서 진행
  - JPA를 쓰면서 가장 크게 느낀 부분은 Fetch-join, Eager&Lazy 전략 등 기본 개념에 대해 이해하고 있어야, 날라가는 Query에 대한 부하를 줄일 수 있다는 것이었음
  - 쓸데없는 조회 Query가 날라가지 않아야 누적되거나 큰 프로젝트 진행 시 깔끔한 처리가 될 것 같음 

<br>

  - Mybatis를 기반으로 진행된 프로젝트가 많고, 보수할 일이 많겠지만 새로운 기술을 배우는 부분도 즐거웠음
  - Mybatis와 비교하면, JPA를 사용하면서 Query에 대해 조금 덜 신경 쓰며 Service단의 비지니스 로직에 좀 더 집중할 수 있었음

<br> <br>
 &nbsp; <b>2. 새로운 기술 활용</b>
  - 1~2차 프로젝트와는 다르게 새로운 기술을 많이 찾아보고, 도입하였음 
  - AmazonS3, RestDocs, Security, Jira, ChartJS 등 활용 

<br>

  - 기술을 도입할 때마다 느꼈던 것은 처음에 세팅하는 부분에서 찾아볼 문서나 내용이 조금 있고, 기본적으로는 활용하기 쉽게 제공해주었음 
  - 기술을 쓰는 것 자체가 대단하다거나 어려운 것이라는 느낌보단, 해당 기술을 진행하는 프로젝트에 어떻게 활용하여 UX를 향상시키고, 유저를 늘리는지가 포인트 같음 
  - 이전보다 다양한 기술을 활용하면서 편리하다는 것을 느꼈고, 나중에 경력이 된다면 해당 기술들을 커스텀마이징 할 수 있는 개발자가 되면 좋겠다고 생각하였음

<br> <br>
  &nbsp; <b>3. 백엔드 팀원간 샘플코드 공유</b> 
  - 몇 개월동안 공부하고 프로젝트에서 활용했던 Mybatis가 아닌 JPA 및 새로운 기술을 도입하는 상황이었음 
  - 백엔드 협업을 진행하면서 한 사람만 기술에 대해 이해하고 있거나, 진행할 수 있는 것은 세분화된 업무 분담이 아니고서야 별로 좋지 않아 보였음 
  - 따라서, 분담하여 공부해온 내용이나 특정 팀원이 코드 이해도가 더 높은 상황이라면 해당 코드에 대한 샘플 코드를 만들어서 팀원과 공유하는 방식을 활용하였음 

<br>

  - 처음에 조간회의에서 자신의 진행 방식을 팀원에게 공유하며 동료검토를 하는 식으로 해보고 싶었지만, 프로젝트와 공부를 병행하면서 정신 없는 상황이어서 진행하지는 못함 
  - 서로간에 샘플 코드를 공유하고 리뷰함으로써 같은 속도로 프로젝트를 진행하고, 팀적인 협업이 되는 느낌이 들었음

<br> <br>
  &nbsp; <b>4. 프런트 팀원과 협업 소통</b>
  - 백단, 프런트단을 동시에 진행하면서 화면설계와 API문서 공유에서 협업할 부분이 많았음
  - 화면설계의 경우 원래 디자인팀이 따로 있는 경우도 있다고 하는데, 해당 프로젝트의 경우 같이 화면설계를 한 이 후 백엔드, 프런트엔드 개발을 진행함 

<br>

  - API문서의 경우 Test를 하고 RestDocs로 만들기 전에 수기로 작성하여 줘야하는 상황이었는데 수기로 작성한 API문서의 경우 한번씩 Update된 부분이 누락되거나, 오타가 발생하는 일이 생겼음 
  - 해당 문제를 겪으면서, 통합 테스트 진행 후 RestDocs로 문서를 뽑는 것이 편리할 뿐만 아니라 문서에 대한 신뢰성을 상당히 높여준다는 것을 알 수 있었음 

<br>

  - 기본적으로 화면에서 데이터를 뿌릴 때는 로직을 최소화하고, 최대한 View 역할인 그림 그리는 부분에 집중해야 한다고 배웠음 
  - 따라서, 로직은 최대한 백엔드단에서 처리할려고 하였으며 해당 부분에서는 큰 문제가 없었음

<br>

## 시연 영상
[![파이널_시연영상](http://img.youtube.com/vi/IId4x-dPgvY/0.jpg)](https://youtu.be/IId4x-dPgvY?t=0s)

<br>

## 발표 PPT
[3차_미니프로젝트_발표PPT](파이널_프로젝트_PPT_PDF판.pdf)

<br>

## 프로젝트 2조
- 김태훈(팀장)
- 전국일(Front-End)
- 이상현(Back-End 총괄)
- 임원빈(Back-End)
- 박지연(Back-End)

<br>

## 기술 스택
### Back-End
|<img src = "https://blog.kakaocdn.net/dn/cKtAuQ/btrAIO5fzCU/NVWnU8UlhL93kq81Ve87uK/img.png" width="150" height="150" />|<img src = "https://user-images.githubusercontent.com/122352251/237043703-20b79833-64fb-45f3-a8fa-5c89c116f2b9.png" width="150" height="150" />|<img src = "https://user-images.githubusercontent.com/122352251/237041368-3cf21fef-807d-467c-9d64-659c5ef5a509.png" width="150" height="150" />|<img src = "https://user-images.githubusercontent.com/122352251/237040483-72812c2e-ce53-4d09-8295-4e31c63bb139.png" width="150" height="150" />|<img src = "https://user-images.githubusercontent.com/122352251/237043987-1054dae4-6586-4973-9bb5-22569fc2e6ef.png" width="150" height="150" />|
|:--:|:--:|:--:|:--:|:--:| 
|SpringBoot|Java|SpringBootSecurity|Jpa|Jwt|

|<img src = "https://user-images.githubusercontent.com/122352251/237037161-4974e0aa-3c05-4b90-9960-a02ab2d7c100.png" width="150" height="150" />|<img src = "https://user-images.githubusercontent.com/122352251/237044332-af860ac9-2e18-4599-8d7c-b0114e3000af.png" width="150" height="150" />|<img src = "https://user-images.githubusercontent.com/122352251/237044459-985f38e5-1fff-420b-8779-2d0c7abd19e0.png" width="150" height="150" />|<img src = "https://user-images.githubusercontent.com/122352251/237044745-76511b18-0673-4d70-a90b-ef3219a6b665.png" width="150" height="150" />|<img src = "https://user-images.githubusercontent.com/122352251/237044893-dadef4f7-a166-4680-a0a4-8b5a56b016d2.png" width="150" height="150" />|
|:--:|:--:|:--:|:--:|:--:|
|VScode|Base64|AmazonS3|Jnuit5|Restdocs|

### Front-End
|<img src = "https://user-images.githubusercontent.com/118786401/235388856-a9918dac-e5ed-4cb3-86cc-6bf65ba00e85.png" width="150" height="150" />|<img src = "https://blog.kakaocdn.net/dn/cj5mLL/btrAJSMQt43/yfpTni01hZgrvKHmUdVjk1/img.png" width="150" height="150" />|<img src = "https://blog.kakaocdn.net/dn/eG2w1k/btrAD5NJ1dy/YwmkEkygLgmKevkYNgWiPk/img.png" width="150" height="150" />|<img src = "https://blog.kakaocdn.net/dn/dJtW2R/btrAIfhLlRL/cTJDpEZlRWh9m9QczAkGqK/img.png" width="150" height="150" />|<img src = "https://blog.kakaocdn.net/dn/biJtm8/btrAGfWUCEm/wLv8P9GuJP55PI0AWxOyS1/img.png" width="150" height="150" />|<img src = "https://blog.kakaocdn.net/dn/m3Phc/btrAGgBsKbm/FNYpkhIrVweUUEH4h5tsWK/img.png" width="150" height="150" />|
|:--:|:--:|:--:|:--:|:--:|:--:|
|Flutter|HTML5|CSS|jQuery|Bootstrap|JavaScript|

<br>

### 협업툴
|<img src = "https://blog.kakaocdn.net/dn/eyjfrN/btrAKvXV0RA/zkyytdkZy7ESd85knYRDq1/img.png" width="150" height="150" />|<img src = "https://blog.kakaocdn.net/dn/mEK9t/btrAHjxWZX3/iEGILm2rWSrOKsfilmPUA1/img.png" width="150" height="150" />|<img src = "https://user-images.githubusercontent.com/118786401/235388614-9304e93a-be4c-43ee-a203-22ff64ddd1da.png" width="150" height="150" />|
|:--:|:--:|:--:|
|Git|Github|Jira|

<br>

### DataBase
|<img src = "https://user-images.githubusercontent.com/118786401/235388737-3027032d-547f-433d-aaad-703e83c86397.svg" width="150" height="150" />|<img src = "https://blog.kakaocdn.net/dn/ccYmmf/btrAGfJoswn/gVqLJkEUq6WgY1MwOEopD1/img.png" width="150" height="150" />|
|:--:|:--:|
|H2|MySQL|

<br>

## 사용한 라이브러리 (Back-End)
-  boot:spring-boot-starter-mail
-  boot:spring-boot-starter-validation
-  boot:spring-boot-starter-security
-  boot:spring-boot-starter-data-jpa
-  boot:spring-boot-starter-web
-  boot:spring-boot-starter-test

-  security:spring-security-test
-  servlet:jstl
-  embed:tomcat-embed-jasper
-  codec:commons-codec:1.15
-  cloud:spring-cloud-starter-aws:2.2.6.RELEASE
-  projectlombok:lombok
-  boot:spring-boot-devtools
-  h2database:h2
-  projectlombok:lombok

-  querydsl:querydsl-jpa:5.0.0
-  querydsl:querydsl-core:5.0.0
-  querydsl:querydsl-apt:5.0.0:jpa
-  persistence:hibernate-jpa-2.1-api:1.0.2.Final
-  annotation:javax.annotation-api:1.3.2

<br>

## 기능 설명
**스포르팅**은 전국의 경기장을 예약 및 결제할 수 있고, 업주로서 경기장을 등록하는 기능을 제공하는 어플리케이션입니다.

### 일반 회원 관련 기능
- 이메일 회원가입 기능
- 이메일 로그인 기능
- 내 정보 수정 기능
- OAuoth 로그인 기능

|||
| :------------: | :-------------: |
| 회원가입 | 로그인 |
| ![회원가입 (1)](https://user-images.githubusercontent.com/118786401/235410401-2dc8e4aa-6044-478d-9c48-f94326645663.gif) | ![로그인 (1)](https://user-images.githubusercontent.com/118786401/235410412-9ee2a68d-bba0-4b51-9fb0-f3dedb265d13.gif) |
| 회원 정보 수정 | OAuth 로그인 |
| ![일반회원-수정하기](https://user-images.githubusercontent.com/118786401/235585788-17d8ad9c-6fe1-4996-b010-aba88ec7ecfd.gif) | ![내카카오오오스](https://user-images.githubusercontent.com/118786401/236964986-294caa6d-97c8-4815-8527-ad45cd99ca51.gif) |

### 기업 회원 관련 기능
- 이메일 회원가입 기능
- 이메일 로그인 기능
- 내 정보 수정 기능

|||
| :------------: | :-------------: |
| 회원가입 | 로그인 |
| ![회원가입 (1)](https://user-images.githubusercontent.com/118786401/235410401-2dc8e4aa-6044-478d-9c48-f94326645663.gif) | ![로그인 (1)](https://user-images.githubusercontent.com/118786401/235410412-9ee2a68d-bba0-4b51-9fb0-f3dedb265d13.gif) |
| 회원 정보 수정 | OAuth 로그인 |
| ![기업회원정보수정](https://user-images.githubusercontent.com/118786401/236104041-2efc5932-054a-4239-8b17-ad2ae2fd0da1.gif) | ![내카카오오오스](https://user-images.githubusercontent.com/118786401/236964986-294caa6d-97c8-4815-8527-ad45cd99ca51.gif) |

### 경기장 관련 기능
- 경기장 목록보기
- 경기장 상세보기
- 경기장 예약 결제 기능
- 경기장 등록하기 기능
- 내가 등록한 경기장 목록보기
- 내가 등록한 경기장 상세보기
- 내가 등록한 경기장 수정하기
- 지도 API를 사용하여서 주변 경기장 찾기 기능
- 지역별 경기장 찾기 기능

|||
| :------------: | :-------------: |
| 경기장 목록보기 | 경기장 상세보기 |
| ![경기장-리스트](https://user-images.githubusercontent.com/118786401/235410807-0d7a5bbd-2841-409e-bd3e-bfeeb35ef20a.gif) | ![경기장-상세-페이지](https://user-images.githubusercontent.com/118786401/235840487-f0380533-5ea4-4696-9c86-d3240b4d95d2.gif) |
| 경기장 예약 결제 | 경기장 등록하기 |
| <img src = "https://user-images.githubusercontent.com/118786401/235840568-b767bd79-0192-44d4-8281-3f6e5e9e2207.gif" width="360" height="694" /> | ![경기장-등록하기](https://user-images.githubusercontent.com/118786401/236105517-da445b1f-afda-4151-9eba-3e15c9c497ca.gif) |
| 내가 등록한 경기장 목록보기 | 주변 경기장 찾기 기능 |
| ![내-경기장-리스트](https://user-images.githubusercontent.com/118786401/235842177-51ae4197-a42e-457e-a521-29089e38a52c.gif) | ![지도](https://user-images.githubusercontent.com/118786401/236969658-236cf7e0-2a05-4769-8955-cb3884456a46.gif) |
| 지역별 경기장 | 
| ![지역별-검색](https://user-images.githubusercontent.com/118786401/237002905-09e0ec29-1902-429a-8e0a-312090f4340e.gif) |
### 관리자 관련 기능
- 경기장 및 코트 등록 승인, 비활성화 등 상태 변경 기능
- 기업/일반 회원 비활성화 등 상태 변경 기능
- 회원 접속률 및 경기장 조회수 통계 기능
- 등록된 회원에게 관리자가 이메일을 보내는 기능

|||
| :------------: | :-------------: |
| 경기장 등록 승인 | 경기장 비활성화 |
| ![경기장-등록-승인](https://user-images.githubusercontent.com/118786401/236108145-d67696c8-2b88-4515-9bcf-7d505183577a.gif) | ![경기장-삭제](https://user-images.githubusercontent.com/118786401/236108156-8d625ffa-ceb5-4cf5-97b8-d7d7f3a56351.gif) |
| 비활성화된 경기장 상태 변경 | 기업 회원 가입 승인 |
| ![비활성경기장상태변경](https://user-images.githubusercontent.com/118786401/236108344-c537462c-41f2-47c3-ab23-3fcde0264ade.gif) | ![KakaoTalk_20230504_125252112](https://user-images.githubusercontent.com/118786401/236116149-cf70a15c-2591-475c-a489-b0a9d58a93ef.gif) |
| 기업 회원 삭제 | 메일링 기능 |
| ![KakaoTalk_20230504_125252112_01](https://user-images.githubusercontent.com/118786401/236116199-63566051-04d9-45b0-9a92-70e77cc1217d.gif) | ![KakaoTalk_20230504_140206107](https://user-images.githubusercontent.com/118786401/236116970-d4045d3b-4952-4cda-a021-a7ccf9673cf0.gif) |
| 통계 |
| ![KakaoTalk_20230504_125252112_02](https://user-images.githubusercontent.com/118786401/236117333-a5411b7e-62a5-40de-a446-89a9e66436e3.gif) |

### 기타 기능
- 이달의 선수 보기 기능
- 이달의 경기장 보기 기능
- 회사 소개 기능
- 공지 사항 기능

|||
| :------------: | :-------------: |
| 이달의 선수 보기 기능 | 이달의 경기장 보기 기능 |
| ![명예의선수](https://user-images.githubusercontent.com/118786401/235411237-b8f0940c-3990-4f4f-9cb5-050116f2930f.gif) | ![이달의구장](https://user-images.githubusercontent.com/118786401/235411254-7c8348f2-a02e-4fd0-8c73-4d7176604ec1.gif) |
| 회사 소개 | 이달의 플레이 |
| ![회사소개](https://user-images.githubusercontent.com/118786401/236106104-3de05c82-4c84-4754-b382-98037757bda5.gif) | ![어플_유튜브](https://user-images.githubusercontent.com/118786401/236968469-aa2b14ba-812f-4606-a564-39db9c9efb66.gif) |
| 공지 사항 |
| ![공지사항](https://user-images.githubusercontent.com/118786401/237002807-6b321e3c-3a18-4388-9e34-af048c93839e.gif) |

<br>

## 테이블 설계
![DB설계](https://user-images.githubusercontent.com/118786401/235402286-40c1a4a8-8624-4600-b9d9-5d12499ea795.png)

<br>

## Jira
https://nomadhuns.atlassian.net/jira/software/projects/GFP/boards/1/roadmap   
역할분담, 계획수립 등 지라를 유용하게 사용하였다.

<br>

## 보완할 점
- OAuth를 통한 회원가입 및 로그인
- 일반 회원 및 기업 회원 통계
- 지도 API를 사용하여서 주변 경기장 찾기 기능
- 리뷰 관련 기능
- 고객센터 문의 기능
- 포인트 기능

<br>

## 프로젝트 진행하면서 느낀점 (팀원 전체)
- AWS S3에 사진파일을 저장하여 활용하였다. 기존 DB와의 통신과 더불어 외부 통신 코드가 추가되어 부하가 커지지 않을까에 대한 고민이 있었다.
  평소 최대한 클린코드 및 간결한 코드를 작성하여 전체적인 부하에 대해 신경써야겠다는 생각이 들었다.
- 1~2차 프로젝트에선 Mybatis를 활용하였고, 3차 프로젝트에선 JPA를 공부하며 사용하였다. 
  JpaRepository 상속에 따른 기본 CRUD 간결화 및 네이밍 쿼리 사용으로 Repository 진행보다 비지니스 로직에 조금 더 집중할 수 있었다.
- Test 코드에 대해 많은 관심을 가지고 프로젝트를 시작하였지만, 진행한 Test 코드가 실질적으로 많은 상황을 보완해줄 수 있을까라는 생각이 들었다.
  Repository 테스트, 단위 테스트 및 통합 테스트를 진행한 결과 아쉬운 부분이 존재하였고, 기회가 된다면 Test코드에 대해 전문적으로 배우고 싶다는 
  생각이 들었다.
  
- 이번 프로젝트를 하며 인증과 권한부여를 시큐리티를 이용해서 사용하였다. 
  시큐리티를 사용하여 복잡한 코드작성을 피할 수 있었고 jwt를 이용한 사용자 관리를 단순화 할 수 있었다. 
  강력한 보안 체계를 구축하기 위해서는 많은 구성 요소와 개념을 이해하고 그들 간의 상호 작용을 적절한 학습과 경험을 통해 배웠다.
- 수기로 작성하던 RESTfulApi 문서를 Restdoc이라는 라이브러리를 이용하여  API 문서를 문서화해서 사용하여 팀원들간의 소통을 편하고 원활하게 할 수 있었다.
  테스트 코드에서 생성된 결과를 기반으로 api문서를 작성을하는데 통합테스트 코드에 대한 충분한 이해가 없어서 어려움을겪었었다.
