### 문자열 덧셈 계산 기능
1. 문자열이 숫자로 시작한다면, <br>쉼표(,) 또는 콜론(:)을 구분자로 가지는 문자열을 받아 구분자를 기준으로 분할한 각 숫자의 합을 반환한다.
    - 문자열에 대해 구분자를 기준으로 분할해 문자열 배열에 담는다.
    - 이후 반복문을 돌며 각 문자열을 정수로 변환해 각 숫자의 합을 구한 뒤 출력한다.
      - 만약 정수로 변환 할 수 없는 문자열이 있다면 `IllegalArgumentException`을 발생시키고 종료한다.
2. 문자열이 '\\\\'로 시작한다면, <br>'\\\\' 뒤부터 '\\n' 앞의 문자열을 분할한 뒤, 구분자 목록에 추가한다. 이후 나머지 문자열을 구분자를 기준으로 분할한 각 숫자의 합을 반환한다.
    - 만약 '\\\\' ~ '\\n' 사이의 문자열에 정수가 있다면  `IllegalArgumentException`을 발생시키고 종료한다.
    - '\\n' 뒤의 문자열에 대해 1번의 과정을 수행하되, 갱신된 구분자를 분할 기준으로 삼는다.
3. 문자열이 숫자로 시작하지도 않고, '\\\\'로 시작하지도 않는다면,<br>`IllegalArgumentException`을 발생시키고 종료한다.
