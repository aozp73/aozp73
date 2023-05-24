# RestAPI Server 구축
### 프로젝트 소개
<br>

<div align="center">
  <img width="80%" src="https://github.com/aozp73/aozp73/assets/122352251/5da48b1a-9cd1-4736-a2aa-96acae3b014d"/>
</div> <br>

&nbsp; - 기존 1차 프로젝트를 RESTful하게 변경 후 배포까지 진행 <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(상세 진행 과정은 아래에서 설명)

<br>
<hr>

### 개인 수행기능
#### 전체요약
<div align="center">
    <img width="60%" src="https://github.com/aozp73/aozp73/assets/122352251/c4e841d9-76e1-4877-9462-d7b8ad99b031"/>
</div>

#### 상세설명 (기술 블로그 포함)
##### SpringBoot 통합 테스트
- Controller, Service, Repository 등 코드 진행 후 최종적으로 Test하기 위해 진행 ([통합 테스트 - 기술 블로그](https://blog.naver.com/aozp73/223055990816))
##### Controller Junit 단위 테스트
- 통합 테스트에 비해 상당히 가볍게 진행 가능, 모듈화 하여 layer 진행마다 테스트 가능 ([단위 테스트 - 기술 블로그](https://blog.naver.com/aozp73/223057284808))
##### AWS 배포
- MobaXterm, AWS, EC2 환경에서 배포 진행, 배포 후 요청 성공 여부 확인 ([AWS 배포 - 기술 블로그](https://blog.naver.com/aozp73/223055991744))
##### @Vaild, 유효성체크
- @Vaild 어노테이션과 BindingResult를 활용하여 간편한 유효성 체크 진행 ([@Vaild, update - 기술 블로그](https://blog.naver.com/aozp73/223053532912)), ([@Vaild, save - 기술 블로그](https://blog.naver.com/aozp73/223053554098))
##### Board, Love Topic 주석추가
- 협업 간 부재 시 또는 퇴사 시 활용 목적. 상세한 주석 추가 ([board 주석추가 - 기술 블로그](https://blog.naver.com/aozp73/223054465094)), ([love 주석추가 - 기술 블로그](https://blog.naver.com/aozp73/223054507737))

##### Board-Topic RestAPI 
 ① Mybatis로 진행함에 있어 ResultMap을 활용하여 DTO안을 입체적으로 변환하여 응답 <br>
 ② 전체적으로 입체적인 DTO 생성 (내부 클래스 활용), XML파일의 ResultMap을 공통적으로 사용 <br>
 ③ 따라서, 해당 프로젝트에선 과정을 정리한 기술 블로그만 기입 
 ([]())
- MyBoardList :  ([해당 Topic - 기술 블로그](https://blog.naver.com/aozp73/223053078486))
- MyScrapBoardList : ([해당 Topic - 기술 블로그](https://blog.naver.com/aozp73/223053083854))
- MyBoardDelete : ([해당 Topic - 기술 블로그](https://blog.naver.com/aozp73/223053135850))
- updateForm : ([해당 Topic - 기술 블로그](https://blog.naver.com/aozp73/223053182531))
- saveForm : ([해당 Topic - 기술 블로그](https://blog.naver.com/aozp73/223053183458))
- update : ([해당 Topic - 기술 블로그](https://blog.naver.com/aozp73/223052709296))
- save : ([해당 Topic - 기술 블로그](https://blog.naver.com/aozp73/223052732533))
- boardList : ([해당 Topic - 기술 블로그](https://blog.naver.com/aozp73/223053185644))
- detail : ([해당 Topic - 기술 블로그](https://blog.naver.com/aozp73/223053187899))

##### Love-Topic RestAPI
- Insert/Delete : ([해당 Topic - 기술 블로그](https://blog.naver.com/aozp73/223053160874))

<br>
<hr>

### 프로젝트 후기
#### 느낀점
 1. API문서 
  - 백엔드와 프런트 협업간에 API문서가 필요함
  - 프런트는 서버의 어떤 주소에 어떤 방식으로 데이터를 요청해야 되는지, 어떤 데이터를 응답하는지 알아야 하는데, API 문서가 없다면 계속해서 불필요한 질문과 소통을 계속 해야할 것이다.
  - API 문서를 통해 불필요한 소통을 없애고, 프런트와 백엔드의 각 작업에 집중할 수 있음 
  - 프로젝트 문서와 API문서, 주석 등 특정 프로젝트에 대한 정보를 최대한 잘 유지, 관리하는 것이 중요하다는 생각이 들었음
 2. 프로젝트 내 컨밴션 
  - Filter를 사용하면서 각 팀원이 진행하는 topic과 관리하는 Controller가 다르더라도 주소 컨밴션을 잘 지키는 것이 중요하다는 것을 알 수 있었음
  - 각 토픽은 다른 개발자가 진행하지만, Filter는 한 파일로 진행하였음 
  - 해당 Filter에서 정한 path에 맞게 각 topic에 주소 컨밴션을 맞추어 적용할 수 있었음

#### 어려웠던 점
  1. DTO 구조화 
   - 2차 프로젝트에서는 1차 프로젝트 결과를 RESTful Server로 만드는 거 였음
   - JPA를 사용한 ORM을 활용하지 않고, Mybatis 사용 그대로 DTO를 입체화하여 응답하는 과정 학습
   - 해당 과정에서 I/O 부하 관련하여 각각의 service에서 select문 호출을 최대한 1번으로 만들기 위해 기본 쿼리를 합치는 과정이 다소 어려웠음
  2. API 문서화 
   - 이번에 JWT 토큰 활용, base64 json으로 받는 과정 등 다른 과정등을 진행하면서 API 문서 자동화에 부분을 따로 공부하지 못했다
   - API문서를 하나하나 수기로 작성하면서, 조원끼리 서로 오타가 있는 것을 발견하기도 했고 상황에 따라 시간이 많이 걸릴수도 있겠다는 생각이 들었다
   - 위 사항 때문에 수기로 작성하는 것이 큰 프로젝트에서 신뢰성이 있을까라는 생각도 들었다
   - 찾아보니 API 문서를 자동화하는 방법에 swagger, Rest Docs 등이 있었고, 각각의 장단점이 있었다
   - swagger는 코드 내에 swagger 관련 어노테이션 및 코드를 진행하는 방식이여서, 다음 프로젝트에선 test 코드에 적용할 수 있는 Rest Docs를 적용해보고 싶다는 생각이 들었다
<br>
<hr>

### 시연 영상
https://github.com/aozp73/aozp73/assets/122352251/17e8b7cd-54d8-4033-9cf6-6abdfd8f928f

<br>
<hr>

### 발표 자료
[2차_미니프로젝트_발표PPT](2차_프로젝트_PPT_PDF판.pdf)

<br>
<hr>

### 팀 소개
- 김태훈 (팀장)
- 이상현
- 강민호
- 김지윤 (개인공부)

<br>
<hr>

### 기술스택
<div align="center">
  <img width="80%" src="https://github.com/aozp73/aozp73/assets/122352251/048b1f32-eb2d-4ab2-ace2-61287753f30f"/>
</div>
<br>
<hr>

### 아키텍쳐
<div align="center">
    <img width="80%" src="https://github.com/aozp73/aozp73/assets/122352251/f8c7699b-f81d-4f46-b33c-2fa6297290e0"/>
</div>
<br>
<hr>

### 기능 

#### 공통 기능
- 회원가입 : 유저네임 중복 체크 및 비밀번호 확인 체크
- 회원정보 수정 시 하나의 버튼으로 사진 포함하여 수정 (사진 등록 전 미리 보기)
- 레디스로 구현하여 브라우저가 닫혀도(JSessionID가 없어도) 로그인 유지
- 구직자/공고 페이징

#### 기업 관련 기능
- 이력서 등록한 원하는 기술을 보유한 유저 추천받기
- 구직자 목록 정렬 조건 기능 (등록일순/마감일순/매칭공고)
- 공고 등록 기능
- 등록한 공고 목록 수정 및 삭제
- 지원한 구직자 합/불합격 선택

#### 구직자 관련 기능
- 채용 합/불합격시 등록된 이메일로 메일링
- 여러개의 자소서 쓰기 및 수정
- 공고 지원
- 보유 기술을 등록하여 기업 추천받기
- 관심 있는 기업 북마크 

<br>
<hr>

### 테이블 설계
![테이블](https://user-images.githubusercontent.com/118786401/233412160-0d63fe4b-acb1-4d0e-b077-1d38cb985bfe.png)  

<br>
<hr>
