# java-racingcar

자동차 경주 미션 저장소

## 우아한테크코스 코드리뷰

- [온라인 코드 리뷰 과정](https://github.com/woowacourse/woowacourse-docs/blob/master/maincourse/README.md)

## 목표

- TDD 방식으로 개발해보기
- 포키 : Driver와 Navigator 역할을 분명하게 해보기
- 쿤 : Navigator 역할을 할 때, 더 넓은 관점에서 바라보기

## 기능 목록

- [X] 경주할 자동차의 이름을 입력받는다
    - [X] 입력받은 이름을 쉼표 단위로 구분한다
    - [X] [예외] 이름이 5자 이상일 경우
    - [X] [예외] 이름이 공백인 경우
    - [X] [예외] 이름이 중복인 경우

```markdown
경주할 자동차 이름을 입력하세요(이름은 쉼표(,)를 기준으로 구분).
pobi,crong,honux
```

- [X] 시도할 횟수를 입력받는다
    - [ ] [예외] 숫자가 아닌 값
    - [ ] [예외] 음수인 값

```markdown
시도할 회수는 몇회인가요?
5
```

- [X] 각 자동차에 난수를 부여한다
- [X] 난수가 4 이상일 경우 전진한다
- [X] 모든 자동차가 전진이 끝나면 결과를 출력한다

```markdown
실행 결과
pobi : -
crong : -
honux : -
```

- [X] 위 과정을 시도횟수만큼 반복한다
- [X] 경주가 끝나면 우승자를 도출한다
    - [X] 가장 많이 전진한 차가 우승한다
    - [X] 우승자는 2명 이상일 수 있다
- [X] 우승자를 출력한다

```markdown
pobi, honux가 최종 우승했습니다.
```

## 도메인 설계

### Car

- 전진하기
- 현재 상태 toString() 오버라이딩

### Game

- 입력받은 횟수에 맞게 게임 진행
- Car 객체에 랜덤값 부여

### Referee

- Car의 전진여부 판단
- 우승자 판정