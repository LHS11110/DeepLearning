# 행렬
- 성분: 행렬안에 배열된 구성원 (항=원소=성분)
- 행(row): 행렬의 가로줄
- 열(column): 행렬의 세로줄
- $A_{m, n}$: $m$개의 행과 $n$개의 열로 이루어진 행렬 $A$
## 표기
$$
\begin{aligned}
A_{M, N}&=\begin{pmatrix}a_{1, 1} & a_{1, 2} & \cdots & a_{1, N} \\
a_{2, 1} & a_{2, 2} & \cdots & a_{2, N} \\
\vdots & \vdots & \ddots & \vdots \\
a_{M, 1} & a_{M, 2} & \cdots & a_{M, N} \\
\end{pmatrix} \\
a_{i, j}&: 2행 1열 성분이라고 읽는다.
\end{aligned}
$$
## 용어 정리
- 주대각선: 행렬의 왼쪽 위에서 오른쪽 아래를 가르는 선
- 주대각성분: 주대각선에 걸치는 i행 i열 성분
- 영행렬: 모든 성분이 0인 행렬
- 전치행렬: $a_{i, j}$에 대하여 $a_{j, i}$, 행렬에 표기할 때는 $A^T$
- 대칭행렬: $A=A^T$인 A
- 정사각행렬: 행, 열의 개수가 같은 행렬
- 단위행렬: 주대각성분들이 1이고, 그 외의 성분은 0인 정사각행렬
## 행렬의 연산
- 행렬 $A_{mn}=(a_{i, j}), B_{mn}=(b_{i, j})$에 대해
### 덧셈과 뺄셈
- $A \pm B = (a_{i, j} \pm b_{i, j})$
### 상수배
- 상수 c에 대해 $cA = (ca_{i, j})$
### 곱셈
- $A_{mn}=(a_{i, j})$와 행렬 $B_{nr}=(b_{j, k})$에 대해
- $AB=(c_{i, k})$, $C_{mr}$ 행렬이 나온다.
- 단, $c_{i, k}=\displaystyle\sum_{j=0}^{n} a_{i, j}b_{j, k}$
- 행렬곱셈은 교환법칙이 성립되지 않는다.
### 아다마르 곱
- 두 벡터 또는 행렬을 곱하는 또 다른 방법으로 각 성분을 곱한다.
- $A_{mn} \times B_{mn} = (a_{i, j}b_{i, j})$
# 행렬식
- 정사각행렬 $A$를 하나의 수로써 대응시키는 특별한 함수. $detA=|A|$
- 이때, $A$가
1. $0 \times 0$ $\rightarrow$ $det() = 0$
2. $1 \times 1$ $\rightarrow$ $det(a) = a$
3. $2 \times 2$

$$
\begin{aligned}
det\begin{pmatrix} a_{1, 1} & a_{1, 2} \\
a_{2, 1} & a_{2, 2} \end{pmatrix} = a_{1, 1}a_{2, 2} - a_{1, 2}a_{2, 1}
\end{aligned}
$$

- 소행렬: 행렬 $A_{M, N}$의 i행과 j열을 제거하여 만든 행렬 $B_{M - 1, N - 1}$
- 소행렬식(minor determinant): 소행렬의 행렬식, 표현식은 다음과 같다. $M_{i, j}$
- 여인수(cofactor): $C_{i, j} = (-1)^{i + j}M_{i, j}$
- 라플라스 전개(Laplace expansion, 여인수 전개라고도 한다.)로 정의한 행렬식

$$
\begin{aligned}
det(A)=\displaystyle\sum_{j=1}^{n} a_{i, j}C_{i, j}
\end{aligned}
$$

# 역행렬
- 역행렬은 행렬 $A$와 곱하여 단위행렬 $I$가 나오게 하는 행렬을 말한다.
- 행렬식이 0이면 역행렬이 존재하지 않는다. 즉, 행렬식이 0이 아닌 정사각행렬 $A$의 역행렬 $A^{-1}$은
- 여인수행렬: 행렬 $A=(a_{i, j})$에 대해 모든 원소에 여인수를 취하는 행렬
- 수반행렬(adjoint matrix): $A=(a_{i, j})$에 대해 $A$의 여인수행렬의 전치행렬

$$
\begin{aligned}
A^{-1}&=\frac{1}{detA}\begin{pmatrix} C_{1, 1} & C_{2, 1} & \cdots \\
C_{1, 2} & C_{2, 2} & \cdots \\
\vdots & \vdots & \ddots
\end{pmatrix} \\
\\
A^{-1}&=\frac{adjA}{detA}
\end{aligned}
$$