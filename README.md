<h1>GLC<h1>
<h2>가천대학교 안드로이드수업 기말 프로젝트<h2>

기능

1.회원관리 ( 회원가입 , 로그인 )
    -Firebase Authentication 기능과 연동
    -이메일 형식으로 회원 가입 하고 파이어 베이스 서버에 데이터 전송
    -로그인 시 파이어 베이스의 정보와 비교하여 로그인 작업을 시행함
    -정보가 일치 할 경우 Main Activity 로 이동한다.
    (이 때 회원 정보 세션을 파이어 베이스 라이브러리에서 관리해줌)

2.SNS
    1.Recycler View 를 사용해서 UI를 구성
    2.파이어 베이스의 저장소,데이터 베이스와 연동하여
       SNS 기능에 필요한 push , pull , update , delete 구현
    3. 글 작성시 기기 내부 갤러리에 접근해서 사진을 가져오고
       글내용과 사진URL 등은 DB에 업로드 하고 사진 파일은
       Stroage 에 업로드
    4. DB에 저장된 정보들을 클래스 형식으로 가져와  SNS
       ITEM개개인을 UI에 매칭시키고 사진은 DB에 저장된
       사진 URL 정보를 이용해 Stroage 에서 다운로드해서 매칭
    5.댓글은 글 item의 자식 노드로 글 레코드에 종식시킨다.
       댓글에는 댓글 내용과 댓글을 작성한 ID를 저장한다.
    6. Feed Item 생성시 DB에 댓글 노드가 존재할 경우 가져와서
        입력한 댓글을  생성시킨다.

3.지하철
    -가천대역의 수원 , 서울 행 지하철 도착정보
    -서울시 공공데이터 지하철 도착정보 API 를 이용
    -Retrofit 라이브러리를 사용해서 비동기 방식으로 API에서 데이터를 가져옴
    -Api에서 가져온 정보를 사용해서 xml 을 안드로이드에 파싱
    -현재 실시간 도착정보를 UI에 매칭


4.학식정보
    -Jsoup 라이브러리(HTML크롤링)를 사용
    -Retrofit 라이브러리를 사용해 비동기 방식으로 정보를  www.gachon.ac.kr/food.jsp 의 정보를 HTML 파싱
    -비전타워 , 교육대학교 , 예술대학교 학생식당의    정보를 가져옴
    -월,화,수,목,금요일의 학식정보를 각각 UI에 매칭

5.가천대학교 컴퓨터 공학과 공지사항
    1. Jsoup 라이브러리를 사용해서 컴퓨터 공학과 공지사항의 제목,작성일,선택 시 URL정보를 파싱
    2. ListView 를 이용해서 제목 과 작성일을 게시판 형식으로  UI구성
    3. ListView 의 Item 클릭 시 WebView 를    이용해서 해당 글의 url 을 이용해서 공지사항 확인


6.가천대학교 지역 날씨
    1. MyWeatherMap API 를 사용해서 복정동의 좌표를 입력
    2. Json형식의 날씨 데이터를  비동식 방식     으로 파싱해서 가져옴
    3. 현재 온도 , 날씨 상태, 최저/최고기온 , 습도 ,바람세기 , 대기압 데이터 를 UI에 매칭
    4. 각 날씨 상황에 맞춰서  날씨  Icon 매칭

201739425 유민상
