## Bootstrap  
Bootstrap : CSS/JavaScript 기반의 오픈소스 웹 프레임워크 



### 🔸Bootstrap의 속성
 - 반응형 웹 지원(자동화면조정)  
 - 브라우저 호환성이 좋음  
 - 타 프레임 워크에 비해 성능이 다소 떨어짐  



### 🔸Bootstrap 사용전 준비 과정
head 태그 안에 <strong>부트스트랩과 jQuery</strong>를 사용하기 위한 코드를 head에 작성 후 Bootstrap을 사용할 수 있다.  
- <strong>Bootstrap 코드</strong> : <http://bootstrapk.com/getting-started/>  
```
    <!-- 합쳐지고 최소화된 최신 CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap.min.css">

    <!-- 부가적인 테마 -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap-theme.min.css">

    <!-- 합쳐지고 최소화된 최신 자바스크립트 -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/js/bootstrap.min.js"></script>

```    
- <strong>jQuery 코드</strong> : <https://code.jquery.com/>  
```
<script src="https://code.jquery.com/jquery-3.6.0.js"
        integrity="sha256-H+K7U5CnXl1h5ywQfKtSj8PCmoN9aaq30gDh27Xc0jk=" crossorigin="anonymous"></script>  
```



### 🔸Bootstrap이 제공하는 태그들
부트스트랩에는 다양한 태그들이 있다
콘테이너, 버튼, 폼 형식 등.. <http://bootstrapk.com/css/>에 마련된 형식을 붙여넣으면 간편하게 사용이 가능하다.



#### 🔹Bootstrap 태그 예시
- 콘테이너(container) : 사이트의 콘텐츠를 감싸 정렬해주는 콘테이너를 생성  
```
<div class="container">
...
</div>
```

- 입력 폼
```
<form>
  <div class="form-group">
    <label for="exampleInputEmail1">이메일 주소</label>
    <input type="email" class="form-control" id="exampleInputEmail1" placeholder="이메일을 입력하세요">
  </div>
  <div class="form-group">
    <label for="exampleInputPassword1">암호</label>
    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="암호">
  </div>
  <div class="form-group">
    <label for="exampleInputFile">파일 업로드</label>
    <input type="file" id="exampleInputFile">
    <p class="help-block">여기에 블록레벨 도움말 예제</p>
  </div>
  <div class="checkbox">
    <label>
      <input type="checkbox"> 입력을 기억합니다
    </label>
  </div>
  <button type="submit" class="btn btn-default">제출</button>
</form>
```

- 버튼
```
<!-- Provides extra visual weight and identifies the primary action in a set of buttons -->
<button type="button" class="btn btn-primary">Primary</button>
```