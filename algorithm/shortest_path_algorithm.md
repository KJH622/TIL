# 최단 경로 알고리즘

## 최단 경로 문제

- 최단 경로 알고리즘은 **가장 짧은 경로를 찾는 알고리즘**을 의미한다.

- **다양한 문제 상황**

    - 한 지점에서 다른 한 지점까지의 최단 경로

    - 한 지점에서 다른 모든 지점까지의 최단 경로

    - 모든 지점에서 다른 모든 지점까지의 최단 경로

- 각 지점은 그래프에서 **노드**로 표현

- 지점 간 연결된 도로는 그래프에서 **간선**으로 표현

    ![최단 경로 알고리즘](/algorithm/img/shortest_path_algorithm/shortest_path_1.png)

## 다익스트라 최단 경로 알고리즘       

- **특정한 노드**에서 출발하여 **다른 모든 노드**로 가는 최단 경로를 계산한다.

- 다익스트라 최단 경로 알고리즘은 음의 간선이 없을 때 정상적으로 동작한다.

    - 현실 세계의 도로(간선)은 음의 간선으로 표현되지 않는다.

    - 즉, 현실 세계의 길 찾기 문제에서 사용될 수 있는 알고리즘이다.

- 다익스트라 최단 경로 알고리즘은 그리디 알고리즘으로 분류된다.

    - **매 상황에서 가장 비용이 적은 노드를 선택**해 임의의 과정을 반복한다.

### 다익스트라 최단 경로 알고리즘 동작 과정

- 알고리즘의 **동작 과정**은 다음과 같다.

    1. 출발 노드를 설정한다.

    2. 최단 거리 테이블을 초기화한다.

        - 모든 노드까지 가기 위한 비용을 무한으로 설정한다.
        
        - 자기 자신에 대한 노드는 0으로 설정한다. 왜냐하면 자기 자신에서 자기 자신으로 가는 비용은 0이라고 볼 수 있기 때문이다.

    3. 방문하지 않은 노드 중에서 최단 거리가 가장 짧은 노드를 선택한다.

    4. 해당 노드를 거쳐 다른 노드로 가는 비용을 계산하여 최단 거리 테이블을 갱신한다.

    5. 위 과정에서 3번과 4번을 반복한다.

    - 최단 경로까지 알기 위해서는 별도의 로직이 사용되어야 한다. 그러나 일반적인 코딩테스트에서는 출제되지 않는다.

- 알고리즘 동작 과정에서 최단 거리 테이블은 각 노드에 대한 현재까지의 최단 거리 정보를 가지고 있다.

- 처리 과정에서 더 짧은 경로를 찾으면 '이제부터는 이 경로가 제일 짧은 경로야'라고 갱신한다.

    ![최단 경로 알고리즘](/algorithm/img/shortest_path_algorithm/shortest_path_2.png)

    ![최단 경로 알고리즘](/algorithm/img/shortest_path_algorithm/shortest_path_3.png)

### 동작 과정 살펴보기

- **[초기 상태]** 그래프를 준비하고 출발 노드를 설정한다.

    ![최단 경로 알고리즘](/algorithm/img/shortest_path_algorithm/shortest_path_4.png)

- **[Step 1]** 방문하지 않은 노드 중에서 최단 거리가 가장 짧은 노드인 **1번 노드**를 처리한다.

    - 현재 값인 무한보다 거쳐갈 때의 값이 더 작기 때문에 갱신한다.

    ![최단 경로 알고리즘](/algorithm/img/shortest_path_algorithm/shortest_path_5.png)

- **[Step 2]** 방문하지 않은 노드 중에서 최단 거리가 가장 짧은 노드인 **4번 노드**를 처리한다.

    - 현재 값보다 거쳐갈 때의 값이 더 작은 경우 갱신한다.

    ![최단 경로 알고리즘](/algorithm/img/shortest_path_algorithm/shortest_path_6.png)

- **[Step 3]** 방문하지 않은 노드 중에서 최단 거리가 가장 짧은 노드인 **2번 노드**를 처리한다.

    - 방문하지 않은 노드 중에서 가장 최단 거리 비용이 작은 것은 노드 번호 2와 노드 번호 5이다.

    - 이러한 경우 둘 중 어떤 노드 먼저 선택해도 상관 없지만 일반적으로 노드 번호가 낮은 것부터 처리한다.

    - 현재 값보다 거쳐갈 때의 값이 더 크면 갱신하지 않는다.

    ![최단 경로 알고리즘](/algorithm/img/shortest_path_algorithm/shortest_path_7.png)

- **[Step 4]** 방문하지 않은 노드 중에서 최단 거리가 가장 짧은 노드인 **5번 노드**를 처리한다.

    ![최단 경로 알고리즘](/algorithm/img/shortest_path_algorithm/shortest_path_8.png)

- **[Step 5]** 방문하지 않은 노드 중에서 최단 거리가 가장 짧은 노드인 **3번 노드**를 처리한다.

    ![최단 경로 알고리즘](/algorithm/img/shortest_path_algorithm/shortest_path_9.png)

- **[Step 6]** 방문하지 않은 노드 중에서 최단 거리가 가장 짧은 노드인 **6번 노드**를 처리한다.

    - 다익스트라 알고리즘을 수행할 때 마지막 노드에 대한 정보는 처리하지 않아도 결과를 얻을 수 있다.

    ![최단 경로 알고리즘](/algorithm/img/shortest_path_algorithm/shortest_path_10.png)

### 다익스트라 알고리즘의 특징

- 그리디 알고리즘: **매 상황에서 방문하지 않은 가장 비용이 적은 노드를 선택**해 임의의 과정을 반복한다.

- 단계를 거치며 **한 번 처리된 노드의 최단 거리는 고정**되어 더 이상 바뀌지 않는다.

    - **한 단계당 하나의 노드에 대한 최단 거리를 확실히 찾는 것으로 이해**할 수 있다.

- 다익스트라 알고리즘을 수행한 뒤에 **테이블에 각 노드까지의 최단 거리 정보가 저장**된다.

    - 완벽한 형태의 최단 경로를 구하려면 소스코드에 추가적인 기능을 더 넣어야 한다.

### 다익스트라 알고리즘: 간단한 구현 방법

- 단계마다 방문하지 않은 노드 중에서 최단 거리가 가장 짧은 노드를 선택하기 위해 **매 단계마다 1차원 테이블의 모든 원소를 확인(순차 탐색)** 한다.

### 다익스트라 알고리즘: 간단한 구현 방법 (Python)

```
import sys
input = sys.stdin.readline
INF = int(1e9) # 무한을 의미하는 값으로 10억을 설정

# 노드의 개수, 간선의 개수를 입력받기
n, m = map(int, input().split())
# 시작 노드 번호를 입력받기
start = int(input())
# 각 노드에 연결되어 있는 노드에 대한 정보를 담는 리스트를 만들기
graph = [[] for i in range(n + 1)]
# 방문한 적이 있는지 체크하는 목적의 리스트를 만들기
visited = [False] * (n + 1) # False: 방문 처리가 되지 않음
# 최단 거리 테이블을 모두 무한으로 초기화
distance = [INF] * (n + 1)

# 모든 간선 정보를 입력 받기
for _ in range(m):
    a, b, c = map(int, input().split())
    # a번 노드에서 b번 노드로 가는 비용이 c라는 의미
    graph[a].append((b, c))

# 방문하지 않은 노드 중에서, 가장 최단 거리가 짧은 노드의 번호를 반환
def get_smallest_node():
    min_value = INF
    index = 0 # 가장 최단 거리가 짧은 노드 (인덱스)
    for i in range(1, n + 1):
        if distance[i] < min_value and not visited[i]: # 방문하지 않은 노드 중에서 min_value보다 작으면
            min_vlaue = distance[i]
            index = i
    return index

def dijkstra(start):
    # 시작 노드에 대해서 초기화
    distance[start] = 0
    visited[start] = True
    for j in graph[start]:
        distance[j[0]] = j[1]
    # 시작 노드를 제외한 전체 n - 1개의 노드에 대해 반복
    for i in range(n - 1):
        # 현재 최단 거리가 가장 짧은 노드를 꺼내서, 방문 처리
        now = get_smallest_node()
        visited[now] = True
        # 현재 노드와 연결된 다른 노드를 확인
        for j in graph[now]:
            cost = distance[now] + j[1]
            # 현재 노드를 거쳐서 다른 노드로 이동하는 거리가 더 짧은 경우
            if cost < distance[j[0]]:
                distance[j[0]] = cost

# 다익스트라 알고리즘을 수행
dijkstra(start)

# 모든 노드로 가기 위한 최단 거리를 출력
for i in range(1, n + 1):
    # 도달할 수 없는 경우, 무한(INFINITY)이라고 출력
    if distance[i] == INF:
        print("INFINITY")
    # 도달할 수 있는 경우 거리를 출력
    else:
        print(distance[i])
```

### 다익스트라 알고리즘: 간단한 구현 방법 성능 분석

- 총 **O(V)** 번에 걸쳐서 최단 거리가 가장 짧은 노드를 매번 선형 탐색해야 한다.

- 따라서 전체 시간 복잡도는 **O(V<sup>2</sup>)** 이다.

- 일반적으로 코딩 테스트의 최단 경로 문제에서 전체 노드의 개수가 5,000개 이하라면 이 코드로 문제를 해결할 수 있다.

    - 하지만 노드의 개수가 10,000개를 넘어가는 문제라면 어떻게 해야 할까?

## 우선순위 큐(Priority Queue)

- **우선순위가 가장 높은 데이터를 가장 먼저 삭제**하는 자료구조이다.

- 예를 들어 여러 개의 물건 데이터를 자료구조에 넣었다가 가치가 높은 물건 데이터부터 꺼내서 확인해야 하는 경우에 우선순위 큐에 이용할 수 있다.

- Python, C++, Java를 포함한 대부분의 프로그래밍 언어에서 **표준 라이브러리 형태로 지원**한다.

    ![우선순위 큐](/algorithm/img/shortest_path_algorithm/queue_1.png)

### 힙 (Heap)

- **우선순위 큐(Priority Queue)를 구현하기 위해 사용하는 자료구조 중 하나**이다.

    - 힙은 내부적으로 트리 구조를 이용한다.

- **최소 힙(Min Heap)** 과 **최대 힙(Max Heap)** 이 있다.

    - 최소 힙: 값이 낮은 데이터부터 꺼내는 방식

    - 최대 힙: 값이 높은 데이터부터 꺼내는 방식

- 다익스트라 최단 경로 알고리즘을 포함한 다양한 알고리즘에서 사용된다.

    ![우선순위 큐](/algorithm/img/shortest_path_algorithm/queue_2.png)

### 힙 라이브러리 사용 예제: 최소 힙

```
import heapq

# 오름차순 힙 정렬 (Heap Sort)
def heapsort(iterable):
    h = []
    result = []
    # 모든 원소를 차례대로 힙에 삽입
    for value in iterable:
        heapq.heappush(h, value)  # h 리스트에 value 값을 넣음
    # 힙에 삽입된 모든 원소를 차례대로 꺼내어 담기
    for i in range(len(h)):
        result.append(heapq.heappop(h))
    return result

result = heapsort([1, 3, 5, 7, 9, 2, 4, 6, 8, 0])
print(result)

# [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

### 힙 라이브러리 사용 예제: 최대 힙

- 파이썬에서는 최대 힙을 제공하지는 않는다.

- 부호를 바꾸어서 push하고 부호를 바꾸어서 pop한다.

```
import heapq

# 내림차순 힙 정렬 (Heap Sort)
def heapsort(iterable):
    h = []
    result = []
    # 모든 원소르 차례대로 힙에 삽입
    for value in iterable:
        heapq.heappush(h, -value)
    # 힙에 삽입된 모든 원소를 차례대로 꺼내어 담기
    for i in range(len(h)):
        result.append(-heapq.heappop(h))
    return result

result = heapsort([1, 3, 5, 7, 9, 2, 4, 6, 8, 0])
print(result)

# [9, 8, 7, 6, 5, 4, 3, 2, 1, 0]
```

### 다익스트라 알고리즘: 개선된 구현 방법

- 단계마다 **방문하지 않은 노드 중에서 최단 거리가 가장 짧은 노드를 선택**하기 위해 **힙 (Heap)** 자료구조를 이용한다.

- 다익스트라 알고리즘이 동작하는 **기본 원리는 동일**하다.

    - 현재 가장 가까운 노드를 저장해 놓기 위해서 힙 자료구조를 추가적으로 이용한다는 점이 다르다.

    - 현재의 최단 거리가 가장 짧은 노드를 선택해야 하므로 최소 힙을 사용한다.

### 다익스트라 알고리즘: 동작 과정 살펴보기 (우선순위 큐)

- **[초기 상태]** 그래프를 준비하고 출발 노드를 설정하여 우선순위 큐에 삽입한다.

    - 큐에 데이터를 넣을 때 튜플 형태로 묶는 과정에서 첫 번째 원소를 기준으로 작은 원소부터 나온다.

    ![우선순위 큐](/algorithm/img/shortest_path_algorithm/queue_3.png)

- **[Step 1]** 우선순위 큐에서 원소를 꺼낸다. **1번 노드**는 아직 방문하지 않았으므로 이를 처리한다.

    - 큐에 데이터를 넣어줄 때는 거리 값이 갱신된 노드의 정보를 기준으로 넣어준다.
    
    - 거리가 짧은 원소를 우선적으로 pop할 수 있도록 넣어준다.

    ![우선순위 큐](/algorithm/img/shortest_path_algorithm/queue_4.png)

- **[Step 2]** 우선순위 큐에서 원소를 꺼낸다. **4번 노드**는 아직 방문하지 않았으므로 이를 처리한다.

    - 만일 거리가 같은 경우, 노드가 더 작은 것을 우선적으로 pop할 수 있게 넣는다.

    - 3번 노드와 같이 우선순위 큐에 존재하는 값이 갱신될 경우 기존 값은 우선순위 큐에서 아래쪽으로 밀려난다.

    ![우선순위 큐](/algorithm/img/shortest_path_algorithm/queue_5.png)

- **[Step 3]** 우선순위 큐에서 원소를 꺼낸다. **2번 노드**는 아직 방문하지 않았으므로 이를 처리한다.

    ![우선순위 큐](/algorithm/img/shortest_path_algorithm/queue_6.png)

- **[Step 4]** 우선순위 큐에서 원소를 꺼낸다. **5번 노드**는 아직 방문하지 않았으므로 이를 처리한다.

    ![우선순위 큐](/algorithm/img/shortest_path_algorithm/queue_7.png)

- **[Step 5]** 우선순위 큐에서 원소를 꺼낸다. **3번 노드**는 아직 방문하지 않았으므로 이를 처리한다.

    ![우선순위 큐](/algorithm/img/shortest_path_algorithm/queue_8.png)

- **[Step 6]** 우선순위 큐에서 원소를 꺼낸다. **3번 노드**는 이미 방문했으므로 무시한다.

    ![우선순위 큐](/algorithm/img/shortest_path_algorithm/queue_9.png)

- **[Step 7]** 우선순위 큐에서 원소를 꺼낸다. **6번 노드**는 아직 방문하지 않았으므로 이를 처리한다.

    ![우선순위 큐](/algorithm/img/shortest_path_algorithm/queue_10.png)

- **[Step 8]** 우선순위 큐에서 원소를 꺼낸다. **3번 노드**는 이미 방문했으므로 무시한다.

    ![우선순위 큐](/algorithm/img/shortest_path_algorithm/queue_11.png)

### 다익스트라 알고리즘: 개선된 구현 방법 (Python)

```
import heapq
import sys
input = sys.stdin.readline
INF = int(1e9) # 무한을 의미하는 값으로 10억을 설정

# 노드의 개수, 간선의 개수를 입력 받기
n, m = map(int, input().split())
# 시작 노드 번호를 입력 받기
start = int(input())
# 각 노드에 연결되어 있는 노드에 대한 정보를 담는 리스트를 만들기
graph = [[] for i in range(n + 1)]
# 최단 거리 테이블을 모두 무한으로 초기화
distance = [INF] * (n + 1)

# 모든 간선 정보를 입력 받기
for _ in range(m):
    a, b, c = map(int, input().split())
    # a번 노드에서 b번 노드로 가는 비용이 c라는 의미
    graph[a].append((b, c))

def dijkstra(start):
    q = []
    # 시작 노드로 가기 위한 최단 경로는 0으로 설정하여, 큐에 삽입
    heapq.heappush(q, (0, start)) # 출발 노드까지의 거리가 0
    distance[start] = 0
    while q: # 큐가 비어있지 않다면
        # 가장 최단 거리가 짧은 노드에 대한 정보 꺼내기
        dist, now = heapq.heappop(q)
        # 현재 노드가 이미 처리된 적이 있는 노드라면 무시
        if distance[now] < dist:
            continue
        # 현재 노드와 연결된 다른 인접한 노드들을 확인
        for i in graph[now]:
            cost = dist + i[1]
            # 현재 노드를 거쳐서, 다른 노드로 이동하는 거리가 더 짧은 경우
            if cost < distance[i[0]]:
                distance[i[0]] = cost
                heapq.heappush(q, (cost, i[0]))

# 다익스트라 알고리즘을 수행
dijkstra(start)

# 모든 노드로 가기 위한 최단 거리를 출력
for i in range(1, n + 1):
    # 도달할 수 없는 경우, 무한(INFINITY)이라고 출력
    if distance[i] == INF:
        print("INFINITY")
    # 도달할 수 있는 경우 결과를 출력
    else:
        print(distance[i])
```

### 다익스트라 알고리즘: 개선된 구현 방법 성능 분석

- 힙 자료구조를 이용하는 다익스트라 알고리즘의 시간 복잡도는 **O(ElogV)** 이다.

- 노드를 하나씩 꺼내 검사하는 반복문(while문)은 노드의 개수 V 이상의 횟수로는 처리되지 않는다.

    - 결과적으로 현재 우선순위 큐에서 꺼낸 노드와 연결된 다른 노드들을 확인하는 총횟수는 최대 간선의 개수(E)만큼 연산이 수행될 수 있다.

- 직관적으로 **전체 과정은 E개의 원소를 우선순위 큐에 넣었다가 모두 빼내는 연산과 매우 유사**하다.

    - 시간 복잡도를 O(ElogE)로 판단할 수 있다.

    - 중간 간선을 포함하지 않는 경우에 이를 O(ElogV)로 정리할 수 있다.

        - **O(ElogE) -> O(ElogV<sup>2</sup>) -> O(2ElogV) -> O(ElogV)**

## 플로이드 워셜 알고리즘

### 개요

- **모든 노드에서 다른 모든 노드까지의 최단 경로를 모두 계산**한다.

- 플로이드 워셜(Floyd-Warshall) 알고리즘은 다익스트라 알고리즘과 마찬가지로 단계별로 **거쳐 가는 노드를 기준으로 알고리즘을 수행**한다.

    - 다만 매 단계마다 방문하지 않은 노드 중에서 최단 거리를 찾는 노드를 찾는 과정이 필요하지 않다.

- 플로이드 워셜은 2차원 테이블에 최단 거리 정보를 저장한다.

- 플로이드 워셜 알고리즘은 다이나믹 프로그래밍 유형에 속한다.

### 플로이드 워셜 알고리즘

- 각 단계마다 **특정한 노드 k를 거쳐 가는 경우를 확인**한다.

    - a에서 b로 가는 최단 거리보다 a에서 k를 거쳐 b로 가는 거리가 더 짧은지 검사한다.

- 점화식은 다음과 같다.

    ![플로이드 워셜 알고리즘](/algorithm/img/shortest_path_algorithm/floyd_warshall_1.png)

### 플로이드 워셜 알고리즘: 동작 과정 살펴보기

- **[초기 단계]** 그래프를 준비하고 최단 거리 테이블 을 초기화한다.

    ![플로이드 워셜 알고리즘](/algorithm/img/shortest_path_algorithm/floyd_warshall_2.png)

- **[Step 1]** **1번 노드**를 거쳐 가는 경우를 고려하여 테이블을 갱신한다.

    - 즉, 1번 행과 1번 열에 대한 정보는 갱신되지 않으며 자기 자신에서 자기 자신으로 가는 경우는 갱신되지 않는다.

    ![플로이드 워셜 알고리즘](/algorithm/img/shortest_path_algorithm/floyd_warshall_3.png)

- **[Step 2]** **2번 노드**를 거쳐 가는 경우를 고려하여 테이블을 갱신한다.

    - 즉, 2번 행과 2번 열에 대한 정보는 갱신되지 않으며 자기 자신에서 자기 자신으로 가는 경우는 갱신되지 않는다.

    ![플로이드 워셜 알고리즘](/algorithm/img/shortest_path_algorithm/floyd_warshall_4.png)

- **[Step 3]** **3번 노드**를 거쳐 가는 경우를 고려하여 테이블을 갱신한다.

    - 즉, 3번 행과 3번 열에 대한 정보는 갱신되지 않으며 자기 자신에서 자기 자신으로 가는 경우는 갱신되지 않는다.

    ![플로이드 워셜 알고리즘](/algorithm/img/shortest_path_algorithm/floyd_warshall_5.png)

- **[Step 4]** **4번 노드**를 거쳐 가는 경우를 고려하여 테이블을 갱신한다.

    - 즉, 4번 행과 4번 열에 대한 정보는 갱신되지 않으며 자기 자신에서 자기 자신으로 가는 경우는 갱신되지 않는다.

    ![플로이드 워셜 알고리즘](/algorithm/img/shortest_path_algorithm/floyd_warshall_6.png)

### 플로이드 워셜 알고리즘 (Python)

```
INF = int(1e9) # 무한을 의미하는 값으로 10억을 설정

# 노드의 개수 및 간선의 개수를 입력 받기
n = int(input())
m = int(input())
# 2차원 리스트(그래프 표현)를 만들고, 무한으로 초기화
graph = [[INF] * (n + 1) for _ in range(n + 1)]

# 자기 자신에서 자기 자신으로 가는 비용은 0으로 초기화
for a in range(1, n + 1):
    for b in range(1, n + 1):
        if a == b:
            graph[a][b] = 0

# 각 간선에 대한 정보를 입력 받아, 그 값으로 초기화
for _ in range(m):
    # A에서 B로 가는 비용은 C라고 설정
    a, b, c = map(int, input().split()) 
    # 2차원 배열을 이용해서 그래프에 대한 정보를 표현하기 때문에 'a행 b열의 값이 c이다' == 'a에서 b로 이동하는 최단 거리 비용이 c이다'
    graph[a][b] = c

# 점화식에 따라 플로이드 워셜 알고리즘을 수행
for k in range(1, n + 1): # k는 거쳐가는 노드
    for a in range(1, n + 1): # a는 출발 노드
        for b in range(1, n + 1): # b는 도착 노드
            graph[a][b] = min(graph[a][b], graph[a][k] + graph[k][b])

# 수행된 결과를 출력
for a in range(1, n + 1):
    for b in range(1, n + 1):
        # 도달할 수 없는 경우, 무한(INFINITY)이라고 출력
        if graph[a][b] == INF:
            print("INFINITY", end=" ")
        # 도달할 수 있는 경우 거리를 출력
        else:
            print(graph[a][b], end=" ")
    print()
```

### 플로이드 워셜 알고리즘 성능 분석

- 노드의 개수가 N개일 때 알고리즘 상으로 N번의 단계를 수행한다.

    - 각 단계마다 **O(N<sup>2</sup>)** 의 연산을 통해 현재 노드를 거쳐 가는 모든 경로를 고려한다.

- 따라서 플로이드 워셜 알고리즘의 총 시간 복잡도는 **O(N<sup>3</sup>)** 이다.

- **플로이드 워셜 알고리즘이 사용되어야 하는 문제에서는 노드의 개수가 500개 이하로 구성되는 경우가 많다.**

## <문제> 전보

### 문제 설명

- 어떤 나라에는 **N개의 도시**가 있다. 그리고 각 도시는 보내고자 하는 메시지가 있는 경우, 다른 도시로 전보를 보내서 다른 도시로 해당 메시지를 전송할 수 있다.

- 하지만 X라는 도시에서 Y라는 도시로 전보를 보내고자 한다면, 도시 X에서 도시 Y로 향하는 통로가 설치되어 있어야 한다. 예를 들어 X에서 Y로 향하는 통로는 있지만, Y에서 X로 향하는 통로가 없다면 Y는 X로 메시지를 보낼 수 없다. 또한 통로를 거쳐 메시지를 보낼 때는 일정 시간이 소요된다.

- 어느 날 C라는 도시에서 위급 상황이 발생했다. 그래서 최대한 많은 도시로 메시지를 보내고자 한다. 메시지는 **도시 C에서 출발하여 각 도시 사이에 설치된 통로를 거쳐, 최대한 많이 퍼져나갈 것**이다.

- 각 도시의 번호와 통로가 설치되어 있는 정보가 주어졌을 때, 도시 C에서 보낸 메시지를 받게 되는 도시의 개수는 총 몇 개이며 도시들이 모두 메시지를 받는 데까지 걸리는 시간은 얼마인지 계산하는 프로그램을 작성하시오.

### 문제 조건

![전보](/algorithm/img/shortest_path_algorithm/wire_1.png)

### 문제 해결 아이디어

- **핵심 아이디어** : 한 도시에서 다른 도시까지의 **최단 거리 문제**로 치환할 수 있다.

- N과 M의 범위가 충분히 크기 때문에 우선순위 큐를 활용한 다익스트라 알고리즘을 구현한다.

### 답안 예시 (Python)

```
import heapq
import sys
input = sys.stdin.readline
INF = int(1e9) # 무한을 의미하는 값으로 10억을 설정

def dijkstra(start):
    q = []
    # 시작 노드로 가기 위한 최단 경로는 0으로 설정하여, 큐에 삽입
    heapq.append(q, (0, start))
    distance[start] = 0
    while q: # 큐가 비어있지 않다면
        # 가장 최단 거리가 짧은 노드에 대한 정보를 꺼내기
        dist, now = heapq.heappop(q)
        if distance[now] < dist:
            continue
        # 현재 노드와 연결된 다른 인접한 노드들을 확인
        for i in graph[now]:
            cost = dist + i[1]
            # 현재 노드를 거쳐서, 다른 노드로 이동하는 거리가 더 짧은 경우
            if cost < distance[i[0]]
                distance[i[0]] = cost
                heapq.heappush(q, (cost, i[0]))

# 노드의 개수, 간선의 개수, 시작 노드를 입력 받기
n, m, start = map(int, input().split())
# 각 노드에 연결되어 있는 노드에 대한 정보를 담는 리스트를 만들기
graph = [[] for i in range(n + 1)]
# 최단 거리 테이블을 모두 무한으로 초기화
distance = [INF] * (n + 1)

# 모든 간선 정보를 입력 받기
for _ in range(m):
    x, y, z = map(int, input().split())
    # x번 노드에서 y번 노드로 가는 비용이 z라는 의미
    graph[x].append((y, z))

# 다익스트라 알고리즘을 수행
dijkstra(start)

# 도달할 수 있는 노드의 개수
count = 0
# 도달할 수 있는 노드 중에서, 가장 멀리 있는 노드와의 최단 거리
max_distance = 0
for d in distance:
    # 도달할 수 있는 노드인 경우
    if d != 1e9:
        count += 1
        max_distance = max(max_distance, d)

# 시작 노드는 제외해야 하므로 count - 1을 출력
print(count - 1, max_distance)
```

## <문제> 미래 도시

### 문제 설명

- 미래 도시에는 1번부터 N번까지의 회사가 있는데 특정 회사끼리는 서로 도로를 통해 연결되어 있다. 방문 판매원 A는 현재 1번 회사에 위치해 있으며, X번 회사에 방문해 물건을 판매하고자 한다.

- 미래 도시에서 특정 회사에 도착하기 위한 방법은 회사끼리 연결되어 있는 도로를 이용하는 방법이 유일하다. 또한 연결된 2개의 회사는 **양방향**으로 이동할 수 있다. 공중 미래 도시에서 특정 회사와 다른 회사가 도로로 연결되어 있다면, 정확히 1만큼의 시간이 이동할 수 있다.

- 또한 오늘 방문 판매원 A는 기대하던 소개팅에도 참석하고자 한다. 소개팅의 상대는 K번 회사에 존재한다. 방문 판매원 A는 X번 회사에 가서 물건을 판매하기 전에 먼저 소개팅 상대의 회사에 찾아가서 함께 커피를 마실 예정이다. 따라서 방문 판매원 A는 **1번 회사에서 출발하여 K번 회사를 방문한 뒤에 X번 회사로 가는 것이 목표**이다. 이때 방문 판매원 A는 가능한 한 빠르게 이동하고자 한다.

- 방문 판매원이 회사 사이를 이동하게 되는 **최소 시간**을 계산하는 프로그램을 작성하시오.

### 문제 조건

![미래 도시](/algorithm/img/shortest_path_algorithm/city_1.png)

### 문제 해결 아이디어

- **핵심 아이디어** : 전형적인 최단 거리 문제이므로 **최단 거리 알고리즘을 이용해 해결**한다.

- N의 크기가 최대 100이므로 플로이드 워셜 알고리즘을 이용해도 효율적으로 해결할 수 있다.

- 플로이드 워셜 알고리즘을 수행한 뒤에 **(1번 노드에서 X까지의 최단 거리 + X에서 K까지의 최단 거리)** 를 계산하여 출력하면 정답 판정을 받을 수 있다.

### 답안 예시 (Python)

```
INF = int(1e9) # 무한을 의미하는 값으로 10억을 설정

# 노드의 개수 및 간선의 개수를 입력 받기
n, m = map(int, input().split()) # 회사의 개수, 경로의 개수
# 2차원 리스트(그래프 표현)를 만들고, 모든 값을 무한으로 초기화
graph = [[INF] * (n + 1) for _ in range(n + 1)]

# 자기 자신에서 자기 자신으로 가는 비용은 0으로 초기화
for a in range(1, n + 1):
    for b in range(1, n + 1):
        if a == b:
            graph[a][b] = 0

# 각 간선에 대한 정보를 입력 받아, 그 값으로 초기화
for _ in range(m):
    # A와 B가 서로에게 가는 비용은 1이라고 설정
    a, b = map(int, input().split())
    graph[a][b] = 1
    graph[b][a] = 1

# 거쳐 갈 노드 k와 최종 목적지 노드 x를 입력받기
k, x = map(int, input().split())

# 점화식에 따라 플로이드 워셜 알고리즘을 수행
for k in range(1, n + 1):
    for a in range(1, n + 1):
        for b in range(1, n + 1):
            graph[a][b] = min(graph[a][b], graph[a][k] + graph[k][b])

# 수행된 결과를 출력
distance = graph[1][k] + graph[k][x]

# 도달할 수 없는 경우, -1을 출력
if distance >= INF:
    print("-1")
# 도달할 수 있다면, 최단 거리를 출력
else:
    print(distance)
```