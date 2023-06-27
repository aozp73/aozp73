# Comorize 포토그램
<div align="center">
        <img width="80%" src="https://github.com/aozp73/aozp73/assets/122352251/bb8182bc-b6f9-4db3-bbe3-9d52af2050a7"/>
</div>

<br>

&nbsp; - 개인 프로젝트 <br>
&nbsp; - 언어, 프레임워크 및 프로젝트 진행 감 유지 목적 (상세 기능은 아래에서 설명)

<br>

## 수행기능
### 전체요약
<div align="center">
    <img width="60%" src="https://github.com/aozp73/aozp73/assets/122352251/4d350b57-4bc9-4bc2-81b7-78dd02a37fb3"/>
</div>

<br>

### 상세설명 - 기술 블로그
- [회원가입](https://blog.naver.com/aozp73/223139278202), &nbsp; [로그인](https://blog.naver.com/aozp73/223139280833), &nbsp; [회원정보 수정](https://blog.naver.com/aozp73/223139281973)
- [구독하기](https://blog.naver.com/aozp73/223139282846), &nbsp; [좋아요](https://blog.naver.com/aozp73/223139292120), &nbsp; [댓글 기능](https://blog.naver.com/aozp73/223139295036)
- [프로필 페이지](https://blog.naver.com/aozp73/223139284380), &nbsp; [메인 사진 페이지](https://blog.naver.com/aozp73/223139290533), &nbsp; [인기 페이지](https://blog.naver.com/aozp73/223139292832)
- [Securit](https://blog.naver.com/aozp73/223139297871), &nbsp; [AOP](https://blog.naver.com/aozp73/223139298401), &nbsp; [OAuth](https://blog.naver.com/aozp73/223139299149), &nbsp; [공통응답 DTO](https://blog.naver.com/aozp73/223139279475)

### 개념 정리
- [OAuth, AOP, JPA, SpringBoot 등](https://blog.naver.com/aozp73/223139304730)
<br>

## 프로젝트 후기
### 느낀점
#### 1. JPA 

  ① JPA 개념 정리 

    - 학원 수강 당시 (22.11.21 ~ 23.05.16) 1차 프로젝트 Mybatis, 3차 프로젝트 JPA를 적용하였음

    - JPA는 학원 수업 내용에 없었기 때문에 인프런 강의를 신청하여 공부와 병행하며 진행하였는데, 
      당시 협업에 있어 기능 구현에 우선 순위를 둬 여유롭게 정리할 시간이 부족했고, 추가 개념정리가 필요했음  

    - 해당 프로젝트를 통해 영속성 컨텍스트, Dirty Checking, OPEN IN VIEW, 양방향 매핑 (무한 참조)
      등에 대한 개념을 다시 한 번 정리할 수 있었음

  ② OPEN IN VIEW 

    - 해당 프로젝트에선 OPEN IN VIEW를 열어서 Entity로 직접 렌더링, 이전 3차 프로젝트에선 응답마다 별도의 DTO를 만들어 렌더링 

    - 코드 진행을 완벽히 체계적으로 정립하고, 실수하지 않을 자신이 있다면 Entity를 응답하는 것도 좋겠지만, 
      웬만해선 화면마다 필요한 DTO를 직접 만드는 것이 안전하다고 생각함 

    - 실무에선 큰 돈이 오가는 사업 내에서 프로젝트를 진행하고, 웬만해선 실수할 여지를 만들지 않는 것이 좋다고 
      생각하는데, DTO를 만들어 toEntity, toDTO 등 메서드를 통해 로직을 진행하는 것도 불편하지 않았음 

  ③ StackOverFlow 양방향 매핑 
  
    - Controller Return문에서 Object를 리턴할 때 Jackson에 의한 직렬화 과정에서 문제가 있었음 
    - Entity를 Return하면서 필드에 있는 연관관계에 의해 내부적으로 상대를 계속 호출함 
    
    - 양방향 매핑으로 List를 더 편리하게 렌더링 또는 로직에 활용할 수 있었지만, 해당 문제로 Server가 다운된다면, 
      서비스 제공 입장에서 많은 손실이 발생할 것임 
      
    - 따라서, 해당 직렬화 과정 뿐만 아니라 디버깅에 사용한 Systout + .toString 메서드 등도 신경 써서 관리해야 한다는 것을 배움  
    - 특히, JPA Entity를 관리함에 있어 @Data 어노테이션이나 직접 명시한 toString 메서드는 위험할 수 있다는 것을 배움

​

#### 2. AOP 횡단관심사 분리 

  ① 개념 재정리 
  
    - 리플랙션, AOP, 인터셉터, Filter 등을 이전에 진행한 프로젝트 및 학습내용에서 경험할 수 있었음 
    - 학원 완강 후 여러 개념들을 한번씩 더 정리하는 시간을 가지고 싶었는데, 해당 프로젝트에 AOP를 적용하면서
      개념적인 부분을 한번 더 살펴볼 수 있었음 
      
  ② 정리된 코드 진행 

    - 해당 프로젝트에선 @Vaild 에서의 유효성 체크 결과를 BindingResult에 담고, 이 후 응답 로직을 AOP에 적용하였음 
    - 여러 메서드에서 중복되는 코드를 줄이고, 각 메서드에선 요청에 따른 핵심 로직에 집중할 수 있다는 것을 다시 한번 느낄 수 있었음 
    
  ③ 가독성, 협업

    - 중복되는 횡단관심사를 분리함으로써 각각의 요청에 따른 로직만 남아 코드가 간결해졌고, 가독성이 굉장히 높아짐 
    - 협업에 있어 핵심 로직의 직관성이 높아졌고, 코드를 확인하는데 좀 더 수월할 것 같다고 느꼈음 

​

#### 3. OAuth 

  ① 사용자 측면  
  
    - 이전엔 카카오톡 OAuth를 공부하였고, 해당 프로젝트에선 페이스북 OAuth를 연결하여 공부할 수 있었음 
      (사용자 정보에 접근할 수 있는 권한을 사이트에 위임)

    - 각 사이트마다 비밀번호가 다를 수 있어, 따로 관리 해야하는 귀찮음이 발생할 수 있음. 
    - 신뢰성이 높은 대형 사이트의 로그인 시스템을 빌려와 보안적인 부분을 조금 더 고려할 수 있었음 
    - 추가 정보를 입력해야 될 여지는 있지만,  버튼 몇번으로 사이트 진입을 간편하게 할 수 있음

​

#### 4. Query문 

  ① 효울성 
  
    - SQL과 Query에 대한 관심도 많아 수강 당시 SQLD 시험에 응시하였음 

    - SQLD 시험에서 정규화 개념 및 기본 Query, 계층 쿼리, 그룹 함수에 대한 개념을 배울 수 있었음 

    - 해당 프로젝트에선 같은 결과라도 진행 과정에 따라 연산을 더 적게 할수 있고, 그런 과정이 많아지면 
      프로그램이 거대해 질 때 비용절감에 이어질 수 있다는 생각을 가졌음 

    - Query문 작성에 있어 단순히 결과 도출만 하기보단, 부하를 줄이는 것이 중요하다는 것을 느낄 수 있었음 

<br>

## 시연 영상 (클릭 시 확대)
|||
| :------------: | :-------------: |
| 회원가입 / 로그인 / 정보수정 | OAuth 로그인 |
| ![회원가입_로그인_정보수정](https://github.com/aozp73/aozp73/assets/122352251/ccf7870e-b503-406c-90be-9e9127c8b8e0) | ![Oauth 로그인](https://github.com/aozp73/aozp73/assets/122352251/17a8ef21-4e1c-4003-ab2e-7aea1ac99acd) |

|||
| :------------: | :-------------: |
| 프로필 변경 / 게시글 등록 | 구독하기 |
| ![프로필변경_게시글등록](https://github.com/aozp73/aozp73/assets/122352251/a0fbc483-fcb3-4474-ae6a-731863351503) | ![구독하기](https://github.com/aozp73/aozp73/assets/122352251/9de28bf4-48f4-40cf-af50-9fcd6fb9a737) |

|||
| :------------: | :-------------: |
| 댓글 / 좋아요 | |
| ![댓글_좋아요](https://github.com/aozp73/aozp73/assets/122352251/570ef671-e43b-4b2b-ac64-95cffafe0bd2) | ![빈-화면](https://github.com/aozp73/SideProject-Comorize/assets/122352251/296bdadb-528a-4d32-9a59-c3cc93ee03d5) |


<br>

## 기술 스택
### Back-End
|<img src = "https://blog.kakaocdn.net/dn/cKtAuQ/btrAIO5fzCU/NVWnU8UlhL93kq81Ve87uK/img.png" width="150" height="150" />|<img src = "https://user-images.githubusercontent.com/122352251/237043703-20b79833-64fb-45f3-a8fa-5c89c116f2b9.png" width="150" height="150" />|<img src = "https://user-images.githubusercontent.com/122352251/237041368-3cf21fef-807d-467c-9d64-659c5ef5a509.png" width="150" height="150" />|<img src = "https://user-images.githubusercontent.com/122352251/237040483-72812c2e-ce53-4d09-8295-4e31c63bb139.png" width="150" height="150" />|<img src = "https://github.com/aozp73/aozp73/assets/122352251/3c69115f-7a02-4bb4-a0de-5d79f743e454" width="150" height="150" />|
|:--:|:--:|:--:|:--:|:--:| 
|SpringBoot|Java|SpringBootSecurity|Jpa|MariaDB|

<br>

## 사용 라이브러리 
- spring-boot-starter-web
- spring-boot-starter-validation
- spring-boot-starter-security
- spring-boot-starter-data-jpa
- spring-boot-starter-oauth2-client
- spring-boot-starter-aop
- spring-security-taglibs
- spring-boot-devtools
- mariadb-java-client
- qlrm
- lombok
<br>

## 테이블 설계
<div align="center">
        <img width="75%" src="https://github.com/aozp73/aozp73/assets/122352251/fb885369-9e33-42b5-a69c-cc5456b66860"/>
</div>
<br>
