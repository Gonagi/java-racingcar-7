# java-racingcar-precourse

# 기능 요구 사항

- 주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.
- 각 자동차에 이름을 부여할 수 있다. 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- 자동차 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하만 가능하다.
- 사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
- 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.
- 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.
- 우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다.
- 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시킨 후 애플리케이션은 종료되어야 한다.

---

# 기능 목록 및 요구 분석

- [ ] 경주할 자동차 이름 입력하는 기능

  - 이름은 영어로만 이루어져 있다.
    - 대문자, 소문자 입력이 가능하다.

- [ ] 각 이름을 ","로 구분하는 기능

  - 각 이름은 중복되지 않는다.
  - 각 이름은 5자 이하이다.

- [ ] 차수별 실행 결과 출력하는 기능
  - 입력한 자동차 이름에 따라 "${이름} : ${전진결과}\n" 형식의 문자열을 반복 출력한다.
  - 실행 결과 출력 후, 개행을 통해 한 문장을 띄워야 한다.
- [ ] 단독 우승자 안내 문구 출력하는 기능
  - "최종 우승자 : " + ${우승자 이름}
- [ ] 공동 우승자 안내 문구 출력하는 기능
  - "최종 우승자 : " + ${우승자 이름} + ", " + ...
  - 우승자가 여려명일 때는 입력한 순서대로 출력한다.
- [ ] 자동차 전진하는 기능
  - 무작위 값이 4 이상인 경우에만 전진한다.
  - 무작위 값이 4 미만인 경우에는 정지한다.
- [ ] 우승자 선정하는 기능
  - 최대 전진 값을 구한다.
  - 최대 전진 값과 동일한 자동차를 구한다.

---

# 에러 상황

- [ ] 경주할 자동차 이름 입력하는 기능
  - 이름으로 영어가 아닌 숫자, 특수 문자가 입력된 경우
  - 쉼표가 먼저 입력된 상황
  - 쉼표가 마지막으로 입력된 상황
  - 쉼표 사이 자동차 이름이 없는 상황
  - null
  - 빈 문자열을 입력한 경우
  - 이름이 5자 초과인 경우
  - 이름이 중복된 경우
- [ ] 시도할 횟수 입력하는 기능

  - 숫자가 아닌 경우
  - 소수, 문자, ...
  - int 타입의 최대값인인 2,147483647을 초과한 숫자를 입력한 경우
  - 음수 입력한 상황
  - null
  - 빈 입력

  ***

  # 핵심 기능만 구현

  - [x] 경주할 자동차 이름 입력하는 기능
  - [x] 시도할 횟수 입력하는 기능
  - [x] 각 이름을 ","로 구분하는 기능
  - [x] Car(자동차)
    - 이름 가져 오는 기능
    - 위치 가져 오는 기능
  - [ ] 차수별 실행 결과 출력하는 기능
