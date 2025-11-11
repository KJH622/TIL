# 집합 자료형

## 집합 자료형의 특징

- 중복을 허용하지 않는다.

- 순서가 없다.

즉, set의 특징은 **자료형의 중복을 제거하기 위한 필터의 역할**로서 사용된다.

```
# 나머지가 다른 것이 몇 개인가?

result = []

for _ in range(n):
    n = int(input())
    rest = n % 42
    result.append(rest)

result_set = set(result)
print(len(result_set))
```