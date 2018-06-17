본 소프트웨어는 딥러닝를 활용하여 수화인식을 지원하는 소프트웨어이다.
mp4파일 형식으로 리눅스 서버 (URL 주소)에 업로드 하며, 리턴 값을 받는 구조를
지니고 있다.

1. 어플리케이션
본 어플리케이션의 파일 구조는, 기본적으로 안드로이드에서 제공되는
파일을 제외하고, 패럴 팀이 개발한 자료들만 본 파일에 기재하였다.


Paral\app\src\main\java\com\example\dyllis\streamtest

\MainActivity 

VideoStart() : 액티비티에 촬영 후 전송된 mp4 파일을 즉시 보여주는 함수임.

ExpressTxt() : 서브 쓰레드로써, 파일 전송 후에 텍스트 값과, 음성출력을 하는 함수임.

PreExpressTxt() : 시작과 동시에 서버의 초기 prediction(인식 값을 저장하는 .txt) 값을 불러와서
inputCheck에 저장하기 위한 함수임.

inputCheck는 ExpressTxt가 실행될 때, 인식처리가 되고나서 값을 한번만 표현하기 위함.

ViewDeepResult() : prediction 값을 불러와서 inputLine에 저장하기 위한 함수임.

uploadFile() : 파일저장과 동시에 서버에 업로드함.



\SplashActivty : 초기 액티비티 실행시 로고화면을 보여주는 액티비티임.




C:\Users\Dyllis\Documents\Comprehensive-LHS\Paral\app\src\main\res\drawable

=> 액티비티에 사용된 이미지 파일 목록임.

C:\Users\Dyllis\Documents\Comprehensive-LHS\Paral\app\src\main\res\layout
activity_main

=> 메인화면을 보여주는 .xml 파일

