
### 🔸Django setting 복습
- 1.가상환경 만들기 : python -m venv myvenv
- 2.가상환경 실행 : source myvenv/Scripts/activate
- 3.django 다운 : pip install django
- 4.프로젝트 생성 : django-admin startproject[프로젝트 이름]
- 5.서버 가동 : python manage.py runserver

## MTV패턴
### 🔸장고의 디자인 패턴
#### MTV(Model Template View)
Model : DataBase(DB)
Template : frontend 사용자가 보이는 영역, HTMl, CSS, 템플릿 언어
View : 데이터를 처리하는 곳, MTV중에서 핵심

## Django 실습 순서
본 강의는 이론보다는 실습을 위주로 학습해야함
App생성 -> Template 제작 -> View 제작 -> URL 연결

## 웹사이트 구동 순서
- 1.사용자가 서버에 요청
- 2.서버의 view는 model에게 요청에 필요한 데이터를 받음
- 3.view는 받은 데이터를 적절하게 처리해서 template으로 넘김
- 4.template는 받은 정보를 사용자에게 보여줌


## 템플릿 언어 html에서 파이썬 변수와 문법을 사용하게 해주는 언어
```
{% for word in wordDict %}
...
{% endfor %}
```
변수를 입력할 때는 {{변수명}}을 사용


## Django와 데이터베이스
### 🔸휘발성 데이터인 wordcount를 데이터베이스를 사용해 저장함
- 1. home.html을 보기위해 요청함 : 클라이언트 -> 서버
- 2. 클라이언트 요청에 대한 응답  : home.html <- Views.py
- 3. home.html의 정보를 제출 : home.html -> (result url + data) -> Views.py

### 🔸ORM(Object Relation Mapping)
객체지향적 방법으로 데이터베이스의 데이터를 생성,삭제,수정 등을 할 수 있음

### 🔸python으로 DB(DataBase) 나타내기
class와 객체를 사용해각 테이블을 나타냄
ex)
```
class Blog:
    id = 숫자
    제목 = 문자
    본문 = 문자
    생성날짜 = 날짜
    글쓴이 = 문자
```

### 🔸models.py
#### makemigration
앱 내의 migration 폴더를 만들어서 models.py의 변경사항을 저장
#### migrate
migration폴더를 실행시켜 데이터베이스에 적용
#### ※모델의 변경사항이 생기면 makemigration를 먼저 하고 migrate를 해야함

### 🔸CRUD
#### Create : 데이터베이스에 데이터들을 저장함
GET : 데이터를 얻기 위한 요청, url에 데이터가 보임
POST : 데이터를 생성하기 위한 요청, Csrf공격 방지 가능

#### Read : 데이터를 웹페이지 상에서 보일 수 있도록 읽음
path-converter : 데이터베이스의 데이터 개수만큼 웹 페이지가 필요하지만 path-converter를 사용하면 id값을 통해 단축할 수 있음

#### Update : 수정내역을 데이터베이스에 적용시켜 업데이트함, 수정할 데이터의 id값을 받아야함

#### Delete : 데이터베이스에 저장된 데이터를 삭제함
