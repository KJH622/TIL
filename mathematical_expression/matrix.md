# 행렬

1. 기본 파이썬 문법(리스트, for문)

2. 라이브러리 사용(numpy, pandas 등)

## for문을 이용한 행렬 생성 (기본 파이썬)

**1. 고정값으로 초기화**

```
rows, cols = 3, 4
matrix = [[0 for _ in range(cols)] for _ in range(rows)]

print(matrix)
# [[0, 0, 0, 0],
#  [0, 0, 0, 0],
#  [0, 0, 0, 0]]
```

- `[[0]*cols]*rows` 형태로 만들면 모든 행이 같은 객체를 참조하므로 사용 X

**2. 1부터 순서대로 채우기**

```
rows, cols = 3, 3
num = 1
matrix = []

for i in range(rows):
    rows = []
    for j in range(cols):
        row.append(num)
        num += 1
    matrix.append(row)
    
print(matrix)
# [[1, 2, 3],
# [4, 5, 6],
# [7, 8, 9]]
```

**3. 사용자 입력으로 행렬 만들기**

```
rows, cols = map(int, input().split())

matrix = []
for _ in range(rows):
    row = list(map(int, input().split()))
    matrix.append(row)

print(matrix)
```

## 라이브러리 사용 (numpy)

**1. 기본 행렬 생성**

```
import numpy as np

# 직접 정의
matrix = np.array([1, 2], [3, 4])

# 0으로 채우기
zeros = np.zeros((3, 3))

# 1로 채우기
ones = np.ones((2, 4))

# 단위 행렬 (identity matrix)
eye = np.eye(3)

print(matrix)
print(zeros)
print(eye)
```

**2. numpy로 입력받기**

```
import numpy as np

rows, cols = map(int, input().split())
data = [list(map(int, input().split())) for _ in range(rows)]
matrix = np.array(data)

print(matrix)

# 입력
# 2 3
# 1 2 3
# 4 5 6

# 출력
# [[1 2 3]
#  [4 5 6]]
```

**3. 난수(random) 행렬**

```
import numpy as np

# 0 ~ 1 사이 난수
rand_matrix = np.random.rand(3, 3)

# 1 ~ 10 사이 정수 난수
rand_int_matrix = np.random.randint(1, 11, (3, 3))

print(rand_matrix)
print(rand_int_matrix)
```

![행렬](/mathematical_expression/img/matrix_img.png)