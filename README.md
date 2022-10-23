# Java를 이용한 회원관리 프로그램

 - IDE : Eclipse
 - DB : H2 사용
 - DBMS : JDBC 사용
 - 콘솔을 통해 아이디(MEMBER_ID), 이름(NAME), 전화번호(PHONE_NUMBER)를 받아 회원가입 절차를 진행
 - 콘솔을 통해 DB 조회, 등록, 수정, 삭제가 가능

## 프로그램 구현

### 1) 테이블 설계

 - H2 데이터베이스에 회원(MEMBER) 테이블을 생성
 - MEMBER 테이블에 저장할 정보는 회원의 아이디(MEMBER_ID), 회원 이름(NAME), 전화번호(PHONE_NUMBER)

### 2) Member 클래스 구현

 - 사용자가 입력한 회원 정보를 저장할 수 있도록 private 맴버변수(필드) 선언
 - private 멤버 필드에 접근하기 위한 Getter 메소드와 Setter 메소드를 선언하고, Member 객체의 상태를 문자열로 리턴하는 toString() 메소드를 재정의(Overriding)

### 3) MemberDAO 클래스 구현

 - Connection 객체를 획득하고, 사용한 Connection 객체를 종료하는 Utility 클래스를 작성
 - 회원 등록, 수정, 삭제, 상세 조회, 목록 조회 기능의 메소드 구현

### 4) MemberManager 클래스 구현

 - MemberDAO와 사용자가 키보드를 통해 입력한 데이터를 읽어들이는 입력 스트림을 맴버변수로 선언하고, 맴버변수를 초기화하는 생성자를 작성
 - 무한루프를 돌면서 사용자가 입력한 메뉴 정보를 읽어들이는 readMenu() 메소드를 구현

 <img src = "https://user-images.githubusercontent.com/102512612/197381338-ecbe3459-cd42-4690-b02b-e12aaa1491e6.png"/>

## 프로그램 실행 과정

### 1) 프로그램 시작

 - 프로그램을 실행하면 다음과 같은 메뉴가 출력된다

 <img src = "https://user-images.githubusercontent.com/102512612/197381873-8a423793-258d-45f5-b9f4-1828edb80a8a.png"/>

### 2) 회원 목록 출력

 - 사용자가 1번 메뉴를 입력하면 회원 목록을 출력한다.
 - 하지만, 등록된 회원이 없다면 다음과 같이 등록된 회원이 없다는 메시지를 출력한다

 <img src = "https://user-images.githubusercontent.com/102512612/197382077-ecb65ef9-7bf5-4e36-9350-636535961c9d.png"/>

 - 만약 등록된 회원 목록이 있다면 정상적으로 회원 목록을 출력한다

 <img src = "https://user-images.githubusercontent.com/102512612/197382331-1890ab88-c14a-4ba9-b26e-db77a6c1ca0f.png"/>

### 3) 회원 가입

 - 사용자가 2번 메뉴를 입력하면 회원 가입 기능을 실행한다

 <img src = "https://user-images.githubusercontent.com/102512612/197382535-b15f8bf1-34e0-43b5-9dd5-e34ef9c2423a.png"/>

 - 회원 가입 후 회원 목록을 출력해보면 회원이 정상적으로 가입되었음을 알 수 있다

 <img src = "https://user-images.githubusercontent.com/102512612/197382614-b49de71c-1aba-4ef0-80ce-6153dcdf7cd7.png"/>

### 4) 회원 수정

 - 사용자가 3번 메뉴를 입력하면 회원 수정(전화번호 수정) 기능을 실행한다
 - 수정 후 회원 목록을 출력해보면 정상적으로 회원의 전화번호가 수정되었음을 알 수 있다

 <img src = "https://user-images.githubusercontent.com/102512612/197382741-5020531c-9c2d-434a-8c70-b3d7e53673f1.png"/>

### 5) 회원 삭제

 - 사용자가 4번 메뉴를 입력하면 회원 삭제 기능을 실행한다
 - 삭제 후 회원 목록을 출력해보면 정상적으로 회원이 삭제되었음을 알 수 있다

 <img src = "https://user-images.githubusercontent.com/102512612/197382834-57c8370f-cd56-4d50-baae-b63d98a8b3a4.png"/>

### 6) 프로그램 종료

 - 사용자가 0번 메뉴를 입력하면 다음 메시지를 출력하고 프로그램을 종료한다

 <img src = "https://user-images.githubusercontent.com/102512612/197382902-401bda63-b6bd-4214-a78e-a3e917edadb3.png"/>

