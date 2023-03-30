# 황영준

## 3/9

Git의 설치
구글 검색 후 설치.

VS code에서 Git 사용
1. 구글에서 Github 검색 후 회원가입
2. Git bash에서 사용자 정보 설정.
-git config --global user.name "HYJ"
-git config --global user.email "99rjsdn@naver.com"
2-1. 정보 확인은 -git config --global
3. 프로젝트 폴더 초기화
-프로젝트 좌측 소스 제어 탭에서  Initialize Repository 버튼 .git 숨긴 폴더 생성됨.
4. commit시 원하는 파일 stage올리고 Message 박스 안에 설명. 그뒤에 commit 버튼.
4-1. 제목은 50자. 엔터키 두번 누르고 자세한 설명.

VS code에서 Github로 push
1. 일부만 commit 후 push할때 케밥메뉴 클릭 후 push
1-1. Github에 Repository없을 때 명령창에 Repository 안내창.
2. 모든 파일 commit 후 push
2-1. 더이상 커밋할 파일 없으면 commit-> publish branch 변경됨
Remote에 Repository없을때 저장소 만들어줌. private public만 선택.(비공개, 공개)

Github 연동.
1. VS code 좌측 하단부 구름 아이콘 혹은 push 진행하며 연동해야함.



## 3/16

R 언어

R설치
https://www.r-project.org/ 방문 후 cran 후 진행.

R.studio 설치
rstudio.com 방문 후 진행.

R studio
1. 소스, 콘솔, 환경, 파일 탭 등으로 구성.


R 언어 이해하기
1. 단순 연산 가능.
2. 변수에 값을 대입하면 환경 창에서 확인 가능.
3. A <- 51:80 이라고 입력하면 A 변수 51~80 설정 함. A 출력시 51, 52.....80
4. 세미콜론 이용해 한줄에 여러 명령문 사용가능
5. 명령문 실행 도중 esc 누르면 작업 취소
6. 인터프리터 방식의 언어, 스크립트 언어 (대본식 진행이라는 뜻)
7. r언어에서의 결과값에서의[1]의 의미
[1]은 해당 객체의 첫 번째 요소(element)를 나타냅니다. 예를 들어, c(1, 2, 3)을 입력하고 실행하면, 다음과 같은 결과가 출력됩니다.

[1] 1 2 3
이 경우, [1]은 첫 번째 요소인 1을 나타냅니다. 만약 결과물이 여러 줄로 출력되는 경우에는, 각 줄마다 해당하는 요소의 인덱스가 출력됩니다.

따라서, [1]은 R에서 출력되는 결과물의 첫 번째 요소를 나타내는 것이며, 해당 객체가 하나의 요소를 가지고 있을 때는 출력되지 않습니다.

R 언어 연산
1. 제곱 ^, 나눗셈나머지 %%, 나머지는 쓰던거 그대로.
2. 함수 사용 가능 log 로그함수, sqrt 제곱근, max 최댓값



## 3/23

변수 벡터 함수


변수
1. 변수 <- 값 하여 변수할당
2. 변수명 작명
2-1. 첫글자는 영문자 혹은 마침표 . 로 시작/일반적으로 영문자
2-2. 두번째 글자부터 영문자, 숫자, 마침표, 밑줄 _ 사용가능
2-3. 변수명 대문자, 소문자 구분함.
2-4. 변수명 중간 공백 사용불가
3. 자료형 : 변수에 저장할 수 있는 값의 종류
3-1. 숫자형 실수 정수
3-2. 문자형 따옴표로 묶어 표현
3-3. 논리형 FALSE, TRUE (F,T 줄여 표현가능)
3-4. 특수형 NULL(정의되지않음), NA(결측값 missing value), NaN(수학적으로 정의 불가능값), Inf(양의 무한대), -Inf(음의 무한대)

벡터
1. 값들의 집합.
2. 같은 데이터 타입.
3. 값 할당시 q < - c(8,18,28) 처럼 c 사용
4. 연속적 숫자 -> A <- 50:90 50부터 90까지 할당됨
5. 일정한 간격의 숫자로 이루어진 벡터 : seq(시작,종료,간격) 함수활용 
6. 벡터 여러 값 이용가능
7. rm() 함수로 변수 초기화 가능

함수
1. 프로그래밍에서 함수의 입력값을 받는 변수를 매개변수라 함
1-1. 함수의 정의에 맞추어 매개변수를 입력하면 정의된 결과값을 얻을 수 있음
1-2. sum() : 총합, mean() : 평균 , length() : 벡터에는 element 개수 ,
     sort() :정렬, sort(,decreasing = TRUE)이용하여 내림차순 가능


##3/30

벡터2
1. 벡터들의 연산이 가능함.
1-1. a <- c(1,3,5)
     b <- c(2,4,6) ##한뒤
     z <- c(x+y) ##하면 z출력시
     3 7 11 ##출력함
1-2. 벡터 연산시 문자열 있으면 숫자 또한 문자열로 변환해 값 할당함.
1-3. 벡터에서 부등호 사용가능 1부터 9값 할당된 벡터d를 이용한 설명
1-3-1. d >= 5 입력하게 되면
FALSE FALSE FALSE FALSE TRUE TRUE TRUE TRUE TRUE
1-3-2. d [2<=d & d<7] 이런 식으로 & 연산자 사용해서 부등호 사용가능.
       결과는 당연하게도 2 3 4 5 6
1-3-3. sum() 함수 등에 사용가능 예를 들어 sum(d>5) TRUE 값 개수 반환함.
1-3-4. length(d>5) 하게 되면 TRUE FALSE로 나뉘는 논리벡터가 됨. 그리고 그 갯수를 출력함.

팩터와 리스트
1. 팩터 : 범주형 데이터 처리용 ex) gender =factor(c("male","female"))
2. 리스트 : 여러가지 자료형 처리용
    my_list <- list(
        name = "John boar",
        age = "30",
        hobby = c('ski','run','ball'),
        address = list(city="SEOUL",street="GEORI"
        )
    )
    print(my_list$name) 하면 John boar
    print(my_list$hobby[2]) 하면 run
    print(my_list$address$city) 하면 SEOUL
