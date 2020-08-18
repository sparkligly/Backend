##javainstall 
설치과정

###1. java (Java Programing Language)

**자바언어의 특징**
     - 운영체제에 독립적이다.
     - 객체지향언어이다. (OOP : Operation Oriented Programing language)
        : 상속, 캡슐화, 다향성 등
     - 배우기 쉽다. 
     - 자동 메모리 관리(Garbage Collection)
     - 네트워크와 분산처리를 지원한다.
     - 멀티쓰레드를 지원한다.
     - 동적 로딩(Dynamic Loading)을 지원한다.

 ###JVM (Java Virtual Machine)
     - java로 작성된 어플리케이션은 모두 JVM에서만 실행되기 때문에 필요하다.

## 자바개발환경 구축하기
 ** 1) JDK 1.7 (Java Developement Kit)**
     - 주요 실행파일( 예제는 뒤에서 )
        (1) javac.exe
            : 자바 컴파일러, 자바소스코드를 바이트코드로 컴파일한다.
        (2) java.exe
            : 자바 인터프리터, 컴파일러가 생성한 바이트코드를 해석하여 실행한다.
        (3) javap.exe
            : 역어셈블러, 컴파일된 클래스파일을 원래의 소스로 변환한다.

     - 다운로드
        (1) 최신버젼이 아니기 때문에 아래 URL로 접속한다.
            : http://java.sun.com/products/archive/
        (2) Java SE7을 선택한다.
        (3) Java SE Development Kit 7u80를 선택한다.
        (4) Accept License Agreement를 선택을 한다.
        (5) 자신의 운영체제에 적당한 파일을 다운로드 한다.
             : window 32비트 - Windows x86를 선택한다.

     - 환경변수 설정
        (1) 내컴퓨터 > 설정 > 고급 시스템설정 > 환경변수
        (2) 시스템 변수(S)에서 ‘새로만들기’를 클릭한다.
        (3) 변수이름 : JAVA_HOME
           변수 값 : C:\Program Files\Java\jdk1.7.0_79 (jdk설치 위치)
        (4) 아래쪽 시스템 변수(S)에서 Path를 선택한다.
        (5) ‘편집’을 클릭 한다.
        (6) 마지막 부분에 “ ;%JAVA_HOME%\bin; ”을 추가한다.

     - java설치 확인방법
        (1) 윈도우키를 누르고 실행창에 ‘cmd'를 입력한다.
        (2) ‘java –version’을 입력한다.
        (3) ‘javac –version’을 입력한다.
        (4) 버전이 같다면 정상이다.
        (5) ‘java’를 입력 시 화면출력이 정상적으로 이루어진다.
        (6) ‘javac’를 입력 시 화면출력이 정상적으로 이루어진다.


 ** 2) Java API문서**
     - http://www.oracle.com/technetwork/java/javase/documentation/java-se-7-doc-download-435117.html         로 접속한다.
     - JDK Documentation(가장위) zip 파일은 다운로드한다.
     - 다운로드 파일에서 jdk-7u79-docs-all/docs/api/index.html을 실행한다.

 ** 3) 자바로 프로그램 작성하기**
     - JDK를 설치하였다면 자바로 프로그램을 만들어 보자.
     - Hello.java
        (1) 메모장을 켠다. (window키+R > notepad 입력)
        (2) 메모장아래 아래 내용을 입력한다.
           : Class Hello{
                public static void main(String[] args){
			System.out.println(“Hello, world”) //화면의 글자를 출력하는 용도
                 }
              }
        (3) 새로운 이름으로 저장하기를 눌러 “Hello.java” 파일명으로 저장한다.
        (4) 자바파일이 있는 위치에서 명령 프롬프트 창을 켠다.
            : shift+우측마우스 클릭하면 목록이 활성화 되는데 “여기서 명령창 열기” 이용
        (5) javac Hello.java << 명령어를 입력 한다.
            : javac명령어는 자바컴파일러(javac.exe)를 사용하여 소스파일(Hello.java)로부터
             클래스파일(Hello.class)을 생성 한다.
        (6) java Hello << 명령어를 입력 한다.
            : (5)번을 통해 얻어진 클래스파일을 실행한다.


  **3) Eclipse 설치**
     - 다운로드
        (1) http://www.eclipse.org 해당 URL로 접속한다.
        (2) 우측 상단의 “DownLoad” 버튼을 클릭한다.
	   (3) 중단의 왼쪽에 “DOWNLOAD 64BIT” 버튼을 클릭한다.
	   (4) 우측 하단에 “Becomming a mirror site”를 선택한다.
	   (5) 왼쪽위에 “More Packages”를 선택한다.
	   (6) 여기까지가 https://www.eclipse.org/downloads/packages/ 접속한 것이다.
	   (7) 왼쪽 상단에 “Luna Packeages”를 선택한다.
	   (8) 두 번째 있는 “Eclipse IDE for Java EE Develpoers” 에 있는 윈도우 64bit용
           파일을 다운로드 한다.(자신의 윈도우 bit확인 필요)

  **   - 설치**
        (1) 다운로드한 파일의 압축을 풀어준다.
        (2) 압축해제 폴더 > eclipse 폴더에 eclipse.exe 파일을 클릭한다.
        (3) Workspace설정
           : 이클립스를 실행하면 Workspace설정 화면이 활성화 된다.
           : 가상으로 압축해제폴더를 설정하면 “압출해제 폴더 > Workspace 폴더가
             생성된다.

     - 인코딩 UTF-8(한글 인식을 위해)
        (1) Window > Preferences 이동한다.
        (2) type filter text에 “enc”를 입력한다.
        (3) 왼쪽이 대분류이고 오른쪽이 소분류 이다. 대분류에 따른 소분류까지 전체를
           인코딩 설정해 주어야 한다.
        (4) 대분류 Content Types
           : 오른쪽 아래에 Default encoding에 “UTF-8”을 넣은 후 update 버튼을 
            클릭한다.
        (5) 대분류 Workspace
            : Text file encoding을 “UTF-8”로 설정후 Apply 버튼을 클릭한다.
        (6) 대분류 CSS Files
            : Encoding을 “ISO 10646/Unicode(UTF-8)”을 선택후 Apply 버튼을 클릭한다.
        (7) 대분류 HTML Files
            : Encoding을 “ISO 10646/Unicode(UTF-8)”을 선택후 Apply 버튼을 클릭한다.
        (8) 대분류 JSP Files
            : Encoding을 “ISO 10646/Unicode(UTF-8)”을 선택후 Apply 버튼을 클릭한다.

     - JDK 설정하기(JAVA파일을 컴파일위해)
         (1) Window > Preferences > java > Installed JREs 이동한다.
         (2) “Add.... ” 버튼을 클릭한다.
         (3) Standard VM을 선택후 Next 버튼을 클릭한다.
         (4) Directory 버튼을 클릭한다.
         (5) JDK가 설치된 폴더로 이동한다. ex)C:\Program Files\Java\jdk1.7.0_79
         (6) Library가 확인이 되면 Finish 버튼을 클릭한다.
         (7) 기존 설정되어 있던 JRE나 JDK가 있다면 삭제 한다.
         (8) 새로 설정한 JDK를 선택 후 OK 버튼을 클릭한다.


     - project 만들기
         (1) Project Explorer를 선택한다.
         (2) 마우스 오른쪽을 클릭 시 활성화 되는 목록중 new > project...을 클릭한다.
         (3) type filter text에 “project”를 타이핑 한다.
         (4) 가장 상단에 “Java Project”를 선택 후 Next 버튼을 클릭 한다.
         (5) Project name을 적어준다. ex) TestProject
            JRE 영역에 설정한 JDK정상적으로 적용되었는지 확인한다.
         (6) Finish 버튼을 클릭한다.

     - JAVA 파일 만들기 (JAVA파일 위치 확인)
         (1) src(source folder)폴더 선택 후 오른쪽 마우스를 클릭한다.
         (2) type filter text에 “class”를 타이핑한다.
         (3) Next 버튼을 클릭한다.
         (4) Name 영역에 클래스 명을 입력한다. ex)classTest
            : 명명규칙은 변수에서 설명
         (5) Finish버튼을 클릭 한다.

##데이터 용량 단위

1. 비트 : bit (이진법의 최소단위)
2. 바이트 : 1byte = 8bit
3. 킬로바이트 : 1KB = 1024byte
4. 메가바이트 : 1MB = 1024KB
5. 기가바이트 : 1GB = 1024MB
6. 테라바이트 : 1TB = 1024GB
7. 페타바이트 : 1PB = 1024TB
8. 엑사바이트 : 1EB = 1024PB

        
