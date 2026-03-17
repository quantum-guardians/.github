# Small World Approach

- 방향 그래프에서 모든 edge에서 edge 간의 거리를 최소화 하는 접근 방법
- QUBO를 문제로 바꾸기 위해서 Heuristic하게 접근
  - 모든 edge에 1차 이웃(1-hop Neighbor)과 2차 이웃(2-hop Neighbor)의 수를 최대화 하는 문제로 바꿈

## QUBO
> 제약 조건 없는 이진 변수 이차 최적화

### Binary variable

binary variable: $e_{ij}$

$$
\text{Let } \forall i, j \in V \text{ such that } i < j:
$$
$$
\text{Direction}(i, j) = 
\begin{cases} 
i \to j & \text{if } e_{ij} = 0 \newline
j \to i & \text{if } e_{ij} = 1
\end{cases}
$$

### Objective Function
$$
\text{min } \sum_{\forall e_{ij} \in E} (-I_{i\rightarrow j}) + \sum_{\forall e_{ik}, e_{kj}}( - I_{i\rightarrow k} \cdot I_{k\rightarrow j})
$$
$$
I_{i\rightarrow j} = 
\begin{cases} 
1-e_{ij} & \text{if } i < j \\
e_{ij} & \text{if } i > j
\end{cases}
$$

- $\sum_{\forall e_{ij} \in E} (-I_{i\rightarrow j})$
  - 모든 Edge의 1차 이웃의 수
- $\sum_{\forall e_{ik}, e_{kj}}( - I_{i\rightarrow k} \cdot I_{k\rightarrow j})$
  - 모든 Edge의 2차 이웃의 수
