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
- Controller, Service, Repository 등 코드 진행 후 최종적으로 Test하기 위해 진행
(https://blog.naver.com/aozp73/223055990816)
##### Controller Junit 단위 테스트
- 통합 테스트에 비해 상당히 가볍게 진행 가능, 모듈화 하여 layer 진행마다 테스트 가능
(https://blog.naver.com/aozp73/223057284808)
##### AWS 배포
- MobaXterm, AWS, EC2 환경에서 배포 진행, 배포 후 요청 성공 여부 확인
(https://blog.naver.com/aozp73/223055991744)
##### @Vaild, 유효성체크
- @Vaild 어노테이션과 BindingResult를 활용하여 간편한 유효성 체크 진행 <br>
(update - https://blog.naver.com/aozp73/223053532912), (save - https://blog.naver.com/aozp73/223053554098)
##### Board, Love Topic 주석추가
- 협업 간 부재 시 또는 퇴사 시 활용 목적. 상세한 주석 추가 <br>
(board - https://blog.naver.com/aozp73/223054465094), (love - https://blog.naver.com/aozp73/223054507737)

##### Board-Topic RestAPI 
 ① Mybatis로 진행함에 있어 ResultMap을 활용하여 DTO안을 입체적으로 변환하여 응답 <br>
 ② 전체적으로 입체적인 DTO 생성 (내부 클래스 활용), XML파일의 ResultMap을 공통적으로 사용 <br>
 ③ 따라서, 해당 프로젝트에선 과정을 정리한 기술 블로그만 기입 
- update : (https://blog.naver.com/aozp73/223052709296)
- save : (https://blog.naver.com/aozp73/223052732533)
- MyBoardList : (https://blog.naver.com/aozp73/223053078486)
- MyScrapBoardList : (https://blog.naver.com/aozp73/223053083854)
- MyBoardDelete : (https://blog.naver.com/aozp73/223053135850)
- updateForm : (https://blog.naver.com/aozp73/223053182531)
- saveForm : (https://blog.naver.com/aozp73/223053183458)
- boardList : (https://blog.naver.com/aozp73/223053185644)
- detail : (https://blog.naver.com/aozp73/223053187899)

##### Love-Topic RestAPI
- Insert/Delete : (https://blog.naver.com/aozp73/223053160874)

<br>
<hr>

### 프로젝트 후기
#### 느낀점

<br>
<hr>

### 시연 영상
https://github.com/aozp73/aozp73/assets/122352251/17e8b7cd-54d8-4033-9cf6-6abdfd8f928f

<br>
<hr>

### 발표 자료
[2차_미니프로젝트_발표PPT](2차_프로젝트_PPT.pptx)

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
