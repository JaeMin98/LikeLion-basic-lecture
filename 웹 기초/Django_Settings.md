## Django_OT
- 강의 목적 : Django 프레임워크를 이용한 웹 서비스 개발
- 강의 대상 : 웹서비스를 처음 만들어보는 사람
- 필수 지식 : HTML/CSS 기초지식, Python 기초지식
- 강의 진행 방식 : 개념과 실습을 번갈아가며 진행

## Django_환경설정

### 🔸Window OS 환경
- 필수 설치 1 : 크롬(Chrome)
- 필수 설치 2 : 파이썬(Python)
- 필수 설치 3 : git
- 필수 설치 4 : VScode(Visual Studio Code)

## Django_터미널사용법

### 🔸CLI, GUI과 터미널
- CLI(Command Line Interface) : 그래픽 없이 명령어로 컴퓨터를 조정하는 인터페이스

- GUI(Graphic User Interface) : 마우스를 이용해 컴퓨터를 조정하는 인터페이스
- GUI 장점 : 진입장벽이 낮고 사용하기 편리하다
- GUI 단점 : 처음 지정된 기능 밖에 사용 불가, 조작 속도가 CLI에 비해 늦은 경우가 있음

- 터미널 : CLI를 GUI 환경에서 사용할 수 있게해줌

### 🔸터미널의 디렉터리
- Home(~) : 터미널 구동 시 처음 위치하는 디렉토리
- Working directory(.) : 현재 위치를 나타낸다, 작업중인 현재 위치
- Root directory(/) : 루트 구조에서 최상단을 의미함, 모든 디렉터리의 시작점
- 상위 디렉터리(..), 하위 디렉터리 : 디렉터리의 상대적인 위치를 표현함  (하위 디레터리는 동시에 여러개가 존재할 수 있으므로 하위 디렉터리 명령어는 따로 존재하지 않음)

### 🔸터미널의 디렉터리 명령어
명령어 조합 : 명령어 [옵션] [인자..]
옵션 : 명령어의 기능을 보완하는 것, 명령어에 따라 존재하지 않을 수 있음
인자 : 파일명이나 디렉터리 명

- pwd(print working directory) : 현재위치를 알려준다

- man(manual) : 명령어 설명서  ex) man [명령어] -> man pwd
```
name : 명령어에 대한 간단한 설명
synopsis : 명령어 사용 방법을 간단하게 요약하여 알려줌
description : 명령어 사용 방법을 상세하게 알려줌
```

- ls(list) : 디렉터리의 목록을 보여준다
ls의 옵션 : a(숨김파일까지 보여줌) , l(상세하게 보여줌) ,F(파일인지 디렉터리인지 보여줌)


- cd(change directory) : 현재 위치를 이동해줌, cd [위치]


- clear : 터미널 청소기, 기존에 입력했던 명령어들이 지워짐

## Django_시작하기
- Django는 Python을 사용하는 프레임워크이다

- 가상환경만들기
```
python -m venv [이름]
(에러가 날경우 python3 -m venv [이름])
```

- source를 이용하여 activate 실행하기
```
source [이름]/[상위디렉토리]/activate
```

- 터미널을 이용해 Django 다운받기
```
pip(Python Install Program)
pip install django
```

- Django로 프로젝트 만들기
```
Django-admin startproject [이름]
-> 서버를 구동시키는 manage.py가 생성됨
```

- manage.py 실행 시키기 (장고 서버 실행시키기)
```
python manage.py runserver
```