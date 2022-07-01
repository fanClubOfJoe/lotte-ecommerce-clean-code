# lotte-ecommerce-clean-code


# 롯데 이커머스 스터디 3rd

**공지사항**

---

- 미션 내용을 외부에 유출하지 말아주세요.
- 페어끼리 각자 미션을 구현해주세요. (절대로 구글링도 안돼요)
- 코드리뷰 전엔 본인 팀꺼 구현하기 전까진 다른사람 PR 을 훔쳐보지 맙시다 ! ! !
- 혹시라도 훔쳐보게 됐다면 마음 속으로 자책합시다.
- 결국 학습의 핵심은 수동적으로 편하게 정해진 지식만 쌓아가느냐, 능동적으로 본인이 주체가 되어 갈증과 궁금증을 느끼는 지식을 쌓아가느냐에서 차이가 벌어지는듯 합니다.
- 이번 스터디가 능동적으로 본인이 주체가되어 공부할 수 있는 스터디가 된다면 좋겠습니다.
- 우리가 나누는 지식들이 모두 공유되는걸 지향합시다.
- 각자 올리는 정보 공유나 질의 응답 같은 것들을 의무적으로 다들 한번씩 살펴보면 좋겠습니다 (카톡의 경우엔 이모지 체크, 코드 리뷰 코멘트는 타 페어것이라도 꼭  읽고 이모지 때립시다).

**도서**

---

[Clean Code(클린 코드) - 교보문고](http://www.kyobobook.co.kr/product/detailViewKor.laf?mallGb=KOR&ejkGb=KOR&barcode=9788966260959)

로버트 C 마틴 - 클린코드 스터디

**슬기로운 코드리뷰생활**

---

[11번가 백명석 코드리뷰 세미나.md](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e6c5d73b-81b8-428b-9e0b-db3e1f24ac6c/11번가_백명석_코드리뷰_세미나.md)

11번가의 msa를 성공적으로 도입한 백명석님의 코드리뷰 세미나 내용 정리

**텍스트와 이미지로 살펴보는 온라인 코드리뷰 과정**

---

[wwh-docs/README.md at master · wwh-techcamp-2018/wwh-docs](https://github.com/wwh-techcamp-2018/wwh-docs/blob/master/README.md)

**동영상으로 보고 싶다면**

---

[github을 기반으로한 온라인 코드 리뷰 방법](https://www.youtube.com/watch?v=a5c9ku-_fok)

**깃허브 커밋 컨벤션**

---

[AngularJS Git Commit Message Conventions](https://gist.github.com/stephenparish/9941e89d80e2bc58a153)

# 🚗**자동차 경주 게임 미션**

---

## **기능 요구사항**

- 각 자동차에 이름을 부여할 수 있다. **자동차 이름은 5자를 초과**할 수 없다.
- 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- 자동차 이름은 쉼표(,)를 기준으로 구분한다.
- 전진하는 조건은 0에서 9 사이에서 random 값을 구한 후 random 값이 4이상일 경우이다.
- **자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한명 이상일 수 있다.**

### **실행 결과**

- 위 요구사항에 따라 3대의 자동차가 5번 움직였을 경우 프로그램을 실행한 결과는 다음과 같다.

```
경주할 자동차 이름을 입력하세요(이름은 쉼표(,)를 기준으로 구분).
pobi,crong,honux
시도할 회수는 몇회인가요?
5

실행 결과
pobi : -
crong : -
honux : -

pobi : --
crong : -
honux : --

pobi : ---
crong : --
honux : ---

pobi : ----
crong : ---
honux : ----

pobi : -----
crong : ----
honux : -----

pobi : -----
crong : ----
honux : -----

pobi, honux가 최종 우승했습니다.

```

### **힌트**

- 자동차는 자동차 이름과 위치 정보를 가지는 Car 객체를 추가해 구현한다.

## **프로그래밍 요구사항**

- 자바 코드 컨벤션을 지키면서 프로그래밍한다.
    - 기본적으로 [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html)을 원칙으로 한다.
    - 단, 들여쓰기는 '2 spaces'가 아닌 '4 spaces'로 한다.
- indent(인덴트, 들여쓰기) depth를 3이 넘지 않도록 구현한다. 2까지만 허용한다.
    - 예를 들어 while문 안에 if문이 있으면 들여쓰기는 2이다.
    - 힌트: indent(인덴트, 들여쓰기) depth를 줄이는 좋은 방법은 함수(또는 메소드)를 분리하면 된다.
- else 예약어를 쓰지 않는다.
    - 힌트: if 조건절에서 값을 return하는 방식으로 구현하면 else를 사용하지 않아도 된다.
    - else를 쓰지 말라고 하니 switch/case로 구현하는 경우가 있는데 switch/case도 허용하지 않는다.
- 3항 연산자를 쓰지 않는다.
- 함수(또는 메소드)가 한 가지 일만 하도록 최대한 작게 만들어라.
- **모든 기능을 TDD로 구현해 단위 테스트가 존재해야 한다.** 단, UI(System.out, System.in) 로직은 제외 (TDD를 처음 접하거나 모르신다면, 공부후에 공유해 보는 기회를 갖는건 어떨까요 ?)
    - 핵심 로직을 구현하는 코드와 UI를 담당하는 로직을 구분한다.
    - UI 로직을 InputView, ResultView와 같은 클래스를 추가해 분리한다.
- **모든 원시 값과 문자열을 포장한다.**
- **일급 컬렉션을 쓴다.**
- **(원시 값 문자열 포장, 일급 컬렉션 등도 정리하여 같이 공부해봐요 !)**

## **기능 목록 및 commit 로그 요구사항**

- 기능을 구현하기 전에 README.md 파일에 구현할 기능 목록을 정리해 추가한다.
- git의 commit 단위는 앞 단계에서 README.md 파일에 정리한 기능 목록 단위로 추가한다.
    - 참고문서: [AngularJS Commit Message Conventions](https://gist.github.com/stephenparish/9941e89d80e2bc58a153)

### **AngularJS Commit Message Conventions 중**

- commit message 종류를 다음과 같이 구분
- 위 북마크에 첨부하였으니 참고하시길 바랍니다.
