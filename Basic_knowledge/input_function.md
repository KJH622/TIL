# 입력함수

## input()

- **input()** 은 기본적으로 문자열을 입력받는 것으로 처리된다.

## sys.stdin.readline()

- **sys.stdin.readline()** 은 한 줄에 여러 입력 값을 받을 수 있다.

- 입력 함수를 사용하기 위해서는 **import sys**를 사용해야 한다.

```
import sys

a = sys.stdin.readline()

print(a)
```

### 옵션

- **readline()** 은 개행문자를 포함하고 있다. 그래서 문자열 마지막에 개행문자가 포함되어 출력되는데 이러한 공백 없이 출력할 수 있게 하는 함수이다.

    - **rstrip()** : 오른쪽 공백을 삭제

    - **lstrip()** : 왼쪽 공백을 삭제

    - **strip()** : 왼쪽, 오른쪽 공백을 삭제
