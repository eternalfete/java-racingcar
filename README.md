# 프리코스 2주차 - 자동차 경주 게임

> 사용자가 입력한 횟수 만큼 자동차 경주를 하여 우승자를 가리는 게임

## 1. 기능 요구 사항

### 1. 룰
- 주어진 횟수 동안 n대의 자동차는 전진 혹은 정지
- 사용자가 각 차에 이름을 부여하고, 출력시 자동차 이름도 함께 출력
- 자동차 이름은 쉼표(,)로 구분, 이름은 5자 이하
- 몇 번 이동할지 사용자가 입력
- 전진 조건은 0~9 사이의 random 값을 구해 4 이상 전진, 3 이하 정지
- 자동차 경주 게임 완료 후 우승자 출력. 우승자는 1명 이상일 수 있음

### 2. 구현 기능 목록

#### 2.1 자동차 이름 입력 받고, 이름의 길이를 검증한 후 자동차 객체 생성

1-1. 사용자로부터 자동차의 이름을 입력받는다.
1-2. 쉼표 단위로 끊어서 자동차의 이름이 5자 이하인지 검증한다.
1-3. 검증된 자동차 이름으로 자동차 객체를 생성한다.

#### 2.2 사용자에게 몇 번 이동할 것인지 입력 받기

사용자로부터 몇 회 이동할 것인지 입력 받는다.

#### 2.3 0~9 사이의 random 값을 만들고, 4 이상이면 전진, 3 이하이면 정지하는 기능 추가

random 값을 만들고, 4 이상이면 전진, 3 이하면 정지하는 기능을 가진 메소드를 추가한다.
해당 메소드는 자동차 객체를 받아 해당 기능을 1회 실행한다.

#### 2.4 실행 결과 출력 기능 추가

자동차 객체를 받아 현재 위치를 출력하는 기능을 추가한다.
해당 기능을 이용해 모든 자동차의 실행 결과를 1회 출력하는 기능을 추가한다.

#### 2.5 사용자가 입력한 횟수만큼 2.5 기능과 2.6 기능 반복 수행하는 기능 추가

사용자의 입력 횟수만큼 2.5 및 2.6 기능을 반복 수행하는 기능을 추가한다.

#### 2.6 최종 우승자 가리기

각 자동차의 위치를 받아 최종 우승자를 가리는 기능을 추가한다.

#### 2.7 최종 우승자 출력

2.8에서 구한 최종 우승자를 출력한다.


### 3. 주요 변수

- `cars` - `ArrayList<Car>`, 사용자가 입력한 이름을 가진 자동차 객체를 담는다.
- 

### 4. 주요 메서드

- `setCarNames` - `void`, 사용자에게 자동차 이름을 입력받고, 검증한 후 해당 이름을 가진 자동차 객체 리스트를 만든다.
    - `getInputCarNames` - `String`, 사용자에게 자동차의 이름을 입력 받아 리턴한다.
    - `validateUserInput` - `ArrayList<String>`, 사용자의 입력이 유효한지(자동차 이름의 길이가 5 이하 인지) 확인 한 후 콤마(",")로 분리된 입력값을 `ArrayList<String>`의 형태로 리턴한다.
    - `parseInputString` - `ArrayList<String>`, 사용자의 입력 값을 콤마(",")로 분리한 후 `ArrayList<String>`으로 리턴한다.
 - 