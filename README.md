# java-ladder
사다리타기 미션 저장소

## 우아한테크코스 코드리뷰
* [온라인 코드 리뷰 과정](https://github.com/woowacourse/woowacourse-docs/blob/master/maincourse/README.md)

# 문자열 덧셈 계산기

## 요구사항

- 쉼표(,) 또는 콜론(:)을 구분자로 가지는 문자열을 전달하는 경우 구분자를 기준으로 분리한 각 숫자의 합을 반환 (예: “” => 0, "1,2" => 3, "1,2,3" => 6, “1,2:3” => 6)
- 앞의 기본 구분자(쉼표, 콜론)외에 커스텀 구분자를 지정할 수 있다. 커스텀 구분자는 문자열 앞부분의 “//”와 “\n” 사이에 위치하는 문자를 커스텀 구분자로 사용한다. 예를 들어 “//;\n1;2;3”과 같이 값을 입력할 경우 커스텀 구분자는 세미콜론(;)이며, 결과 값은 6이 반환되어야 한다.
- 문자열 계산기에 숫자 이외의 값 또는 음수를 전달하는 경우 RuntimeException 예외를 throw한다.

## 기능

- 구분자를 기준으로 숫자를 분리한다.
- 커스텀 구분자를 기준으로 숫자를 분리한다.
- 분리된 숫자들을 더해준다.
- 숫자 이외의 값 또는 음수가 있을 경우 RuntimeException을 throw한다.

# 사다리 게임 - 1단계

## 요구사항

- 사다리 게임에 참여하는 사람에 이름을 최대5글자까지 부여할 수 있다. 사다리를 출력할 때 사람 이름도 같이 출력한다.
- 사람 이름은 쉼표(,)를 기준으로 구분한다.
- 사람 이름을 5자 기준으로 출력하기 때문에 사다리 폭도 넓어져야 한다.
- 사다리 타기가 정상적으로 동작하려면 라인이 겹치지 않도록 해야 한다.
  - `|-----|-----|` 모양과 같이 가로 라인이 겹치는 경우 어느 방향으로 이동할지 결정할 수 없다

## 필요한 기능

- 문자열을 입력받아 객체를 생성
  - 문자열을 입력받는다.
  - 입력받은 문자열을 쉼표(',')를 기준으로 구분한다.
  - 객체를 생성한다.
  - 일급 컬렉션에 담아준다.
- 사다리 높이를 입력받아 사다리를 만든다.
  - 사다리 높이를 입력받는다.
  - 사다리 높이 만큼 세로 라인 길이를 설정한다.
  - 사람의 수 만큼 가로 라인을 설정한다.
  - 겹치지 않게 가로 라인을 만든다.
- 사다리를 출력해준다.

## 가능한 예외

문자열을 입력받아 객체를 생성

- 문자열을 입력받아 객체를 생성
  - 쉼표로 구분하지 않는 경우
  - 구분된 문자열의 길이가 5를 초과하는 경우
  - 문자열이 공백인 경우
  - 문자열이 NULL인 경우
- 사다리 높이를 입력받아 사다리를 만든다.
  - 높이가 음수인 경우
  - 가로라인이 연속되는 경우



1. 사람의 이름을 입력받는다.
2. 입력 받은 이름을 컴마(,) 기준으로 나눠준다.
3. 사람 객체를 생성한다.
4. 사람 컨테이너 객체를 만든다. 
5. 사다리의 높이를 입력 받는다.
6. 사다리 객체를 사람수와 사다리 높이를 인자로 받아서 생성하다.
7. 사다리 높이만큼 Line 클래스 리스트를 만들어준다.
  1. Line은 가로라인을 boolean List로 가지고 있는다 (사람 수 - 1)
  2. 가로 라인을 그어준다. 이 때 연속되면 안된다
8. 사다리를 출력해준다.