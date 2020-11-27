# Document v0.1
|작성자|작성일자|작성내용|버전|
|------|--------|------|---|
|허재혁|2020.11.27|최초 작성|0.1|

## 요구조건 파악
### 주어진 요건
#### RandomUtils
```
RandomUtils.nextInt(int startInclusive, int endInclusive);
```
- 역할
    - 위 static 메소드는 startInclusive와 endInclusive 사이의 수(들)에서 하나의 수를 랜덤하게 뽑는다.
- 책임
    - startInclusive와 endInclusive의 대소를 비교하고 startInclusive <= endInclusive의 경우에만 랜덤하게 수를 뽑는다. 나머지 경우에는 IllegalArgumentException이 발생한다.
- 관계
    - 문제에 따르면 서로 다른 임의의 수를 뽑아야 하므로 위 메소드로 뽑은 수가 그 전에 뽑은 수에 포함되었는지 검증한 후 없는 경우에만 포함시킨다. 따라서 이를 검증할 객체/메소를 구현해야 한다.

<br>

### 기능 구현 목록
- [x] '숫자를 입력해주세요 : '라는 명령과 함께 플레이어에게 3자리의 수를 입력받는다.
    - [x] **예외** 입력 길이가 3이 아닌 경우
    - [x] **예외** 입력 길이는 3이나 숫자로 치환되지 않는 경우
- [ ] 주어진 RandomUtils를 이용하여 1부터 9까지 임의의 서로 다른 숫자 3개를 생성한다.
- [ ] 입력한 수에 대한 결과를 볼, 스트라이크 갯수, 혹은 낫싱으로 출력한다.
    - [ ] 스트라이크: 숫자와 자리가 모두 일치한다.
    - [ ] 볼: 숫자는 일치하나 자리가 일치하지 않는다.
    - [ ] 낫싱: 스트라이크와 볼이 모두 없다.
- [ ] 3스트라이크일 때, 플레이어에게 게임 재진행 여부를 1(새로 시작), 2(종료)으로 입력받는다.
    - [ ] **예외** 입력이 1이나 2가 아닐 경우
- [ ] 게임 재진행 여부에 따라 게임을 다시 진행하거나 종료한다.