# 그대로 출력하기

- 표준 입력으로 들어오는 **모든 문자**를 **그대로** 출력한다.

- 공백/빈 줄/탭 등도 그대로 유지해야 하고, 임의의 가공을 하면 안된다.

- 입력은 EOF(파일 끝)까지 주어진다.

- `input()` 은 마지막 줄 추러나 공백 보존에 신경써야 해서 불편하다.

## 파이썬 풀이

### 풀이 1

```
import sys

def main():
    data = sys.stdin.read() # EOF까지 전부 읽기
    sys.stdout.write(data) # 가공 없이 그대로 출력

if __name__ = "__main__":
    main()
```
### 풀이 2

```
import sys

for line in sys.stdin: # 한 줄씩 읽되
    sys.stdout.write(line) # end =''로 그대로 출력
```
