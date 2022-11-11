~목록까지 진행.. 압축1파일 접속) localhost/board/ - 제목2 클릭.. 기능추가)
상세보기에서 조회수 나오게 하기... -> 순서는 조회수를 증가시키고 가져오기; ->
하루에 한번만 허용하고 / 두번은 허용하지 않음.. - DB하나 추가해야함.. - cookie /
session을 활용해야함.. - 세션에 아이디가 살아있는동안은 카운터 X 기능추가)
줄바꿈처리해주기 - 데이터에는 줄바꿈도 들어가 있으나 출력에는 가로로 옆으로
붙여져서 보여짐 (html특징.. 띄어쓰기 하나로 인식..) => nl2br 함수로 처리
cf) nl2br$['content']...
write.php : 유효성 체크 -> 클라이언트에서 체크를 해주게 되면 서버에서 부담이 줄어듬.. => php에서 한번 더 유효성 체크를 해주면 더블체크..
실무에서는 일케함..

방법:
1. 순수 자바스크립트 - 함수 생성
2. 제이쿼리 - 실무에서는 제이쿼리를 사용할 수 없는 경우도 있을 수 있음. ** 함수명 틀리지 않도록 주의!!(함수 만들때 alert('함수 호출')을 사용해서 함수를 실행해보기.)
## let subject = doucument.querySeletor('#subject')?.value; ?. 이문법 찾아보기
doucument.querySeletor('아이디 값') write.php:
<form onsubmit="return chkForm();">
  - return값을 return - turn / false값을 리턴하고, false값을 리턴할 경우
  ** nsubmit='return chkForm(); 사용자가 오래된 브라우저 / 크롬을 사용하지 않으면 사용하지 못할 수도 있음.. ** 중복되는 코드는 함수로 구현 ** javaScript도 재사용가능. *** isFocus && ele.focus(); 앞이 false면 뒤에 문은 실행안함. ***
  isFocus || ele.focus(); // 최상위 폴더에 join.php 파일생성 _inc_page_gnb에서 join 버튼 생성 // 회원가입 - 데이터베이스에 등록하기 전 이메일 중복체크하기 (쿼리문을 들고와야함..->게시물 가져오기 들고 와서 수정)
  
  ** 중요한 것!!중복체크!! // 클라이언트 / php단에서도 확인 해줘야함.. - 부트스트랩에서 폼>입력그룹>버튼 애드온 2번째 복붙
```html
  <div class="input-group mb-3">
    <input
      type="text"
      class="form-control"
      placeholder="Recipient's username"
      aria-label="Recipient's username"
      aria-describedby="button-addon2"
    />
    <button class="btn btn-outline-secondary" type="button" id="button-addon2">
      Button
    </button>
  </div>
```
  - jquery 사용 할 예정 -> 코드의 양을 줄이는 역할 //
  https://releases.jquery.com/ // 다운로드 > Other CDNs 위에 줄에서
```html
  <script>
    function chkDualEmail() {
      //          let email = doucument.querySeletor('#email').vlaue;
      //          let email = doucument.querySeletorAll('#email')[0].vlaue;
      let email = $('#email').val();
      if (
        /^[a-zA-Z0-9._-]{1,}@[0-9a_zA-Z-]{3,}([.][a-zA-Z]${2,3}){1,2}/.test(
          email
        )
      ) {
        alert('이메일을 바르게 입력하세요.');
        return false;
      }
    }
  </script>
  <script
    src="https://code.jquery.com/jquery-3.6.0.min.js"
    integrity="sha256-/xUj+3OJU5yExlq6GSYGSHk7tPXikynS7ogEvDej/m4="
    crossorigin="anonymous"
  ></script>
</form>
```

// 중복체크 여부를 확인하기 위해
```html
<submit onsubmit=""></submit>
<input type="hidden" id="checkDualEmail" value="false" ></input> 추가하기
```
++ 값이 바뀌면 다시 중복확인을 해야하는 코드를 작성해줘야함!!!! -> onchange();
  1) 자가 체크
  2) 자동 체크 (구글의 경우)
    - 화면 이동 없이!!! 실시간으로!! 값을 체크해서 input태그 아래 결과값을 적어줌..
  => 쇼핑몰 -> 주문량이 재고량을 초과했습니다. / 주변의 상가를 보여줄 수 있음.. / 주식 차트 / 활용도가 많다!
  => 글을 이미지 / 차트 등 모두 바꿀 수 있음!!!
++ onkeyup(이메일 값이 변경되었다는 함수)
이메일 값이 

### php의 경우 빈칸이 전부 출력되기 때문에 빈칸을 모두 지우거나 / .trim()을 해줘야함..

## 함수 속의 내장함수가 많은 편일때 바꾸어서 사용할 수 있도록 ex) join -> 더이상 사용할 수 없을 때를 대비할 수 있음
=> 잘하는 사람은 함수를 만들어서 내장함수를 바꿀 수 있도록 작성.. 비슷한 함수는 많으므로 함수를 수정해야할 때 편리하게 사용할 수 있음
=> 유지 보수 관리까지 생각하면서 코드를 작성해야한다!!

## 항상 단순하게 생각해서는 안되고, 모든 상황을 고려해서 작성해야한다... => 해커가 공격함..
=> 개발자가 생각하지 못할 경로는 항상 열여있음.. => 경험에서 나옴..