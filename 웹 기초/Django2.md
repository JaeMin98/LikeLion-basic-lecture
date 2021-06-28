
### 🔸Templete 상속
각종 html파일에서 겹치는 부분을 base.html을 사용해 상속시켜 중복되는 코드를 방지하는 것
<br>
- 1.home.html 코드
```
{% extends 'base.html '%}

{% block content %}
...
...
...
{% endblock %}
```
- 2.(ex)lionproject>tamplates>base.html 코드
```
{% block content %}
{% endblock %}
```

- 3.settings.py 파일 수정
```
settings.py파일 > TEMPLATES 의 DIRS > ['(ex)lionproject/templates'],
```
<br>
<br>

### 🔸Static과 Media
#### 정적파일과 동적파일
- 정적 파일 : 미리 서버에 저장되어 있는 파일, 서버에 저장된 그대로를 서비스해주는 파일
- 동적 파일 : 서버의 데이터들이 어느정도 가공된다음 보여지는 파일
<br>
#### 정적파일 종류
- Static : 개발자가 서버를 개발할 때 미리 넣어놓은 정적파일(img,js,css)
- Media : 사용자가 업로드 할 수있는 파일
<br>
#### 사진을 보여줄 때 클라이언트와 서버간 대화
- 1.클라이언트 > 서버에 사진을 요청
- 2.서버 > 사진의 url 제공
따라서 media라는 폴더를 만들어 사용자가 업로드한 파일들을 모아놓아야 함
<br>
<br>
### 🔸Form(입력공간)
#### 기존의 form 방법과 비교하여 forms.py를 이용했을 때의 장점
- 데이터베이스의 model이 변할 때마다 바꿀 필요가 없음
- 유효성 검사 가능 : 데이터베이스가 받을 수 있는 파일인지 검사하는 것

### 🔸User, 장고에서 제공해주는 User table
#### Authentication 과정
- 1.클라이언트가 서버에 회원가입 요청
- 2.서버에서 유저테이블에 회원정보를 저장
- 3.클라이언트가 서버에 로그인 요청
- 4.유저테이블에서 정보를 찾아서 응답

### 🔸Paginator
#### Paginator란?
paginator : 이용자가 많아짐에 따라 글이 많아지면 블로그 객체를 잘라서 보내주는 것
ex) page/1/ -> 10개의 글 보여주기
```
blogs = Blogs.objects.all('-pub_date')
...
blogs =paginator.set_page(page)
```
<br>
####QuerySet Method
order_by : 최신글을 보여주고싶을 때는()
blogs = Blogs.objects.order_by('-pub_date')
