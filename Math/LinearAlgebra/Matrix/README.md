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
- $mn$ 행렬 $A=(a_{i, j}), B=(b_{i, j})$에 대하여
### 덧셈과 뺄셈
- $A \pm B = (a_{i, j} \pm b_{i, j})$
### 상수배
- 상수 c에 대해 $cA = (ca_{i, j})$
### 곱셈
- $mn$ 행렬 $A=(a_{i, j})$와 $nr$ 행렬 $B=(b_{j, k})$에 대해
- $AB=(c_{i, k})$: $mr$ 행렬
- 단, $c_{i, k}=\displaystyle\sum_{j=0}^{n} a_{i, j}b_{j, k}$
- 행렬곱셈은 교환법칙이 성립되지 않는다.
#### 합성함수와 행렬곱셈의 관계
$$
\begin{aligned}
f(x, y)&=(ax + by, cx + dy) \\
g(x, y)&=(px + qy, rx + sy) \\
f \circ g&=(apx+aqy+brx+bsy, cpx+cqy+drx+dsy) \\
&=((ap+br)x+(aq+bs)y, (cp+dr)x+(cq+ds)y) \\
\\
F&=\begin{pmatrix} a & b \\
c & d \\
\end{pmatrix} \\
G&=\begin{pmatrix} p & q \\
r & s \\
\end{pmatrix} \\
FG&=\begin{pmatrix} ap+br & aq+bs \\
cp+dr & cq+ds \\
\end{pmatrix} \\
\begin{pmatrix} (ap+br)x+(aq+bs)y \\
(cp+dr)x+(cq+ds)y \\
\end{pmatrix}&=\begin{pmatrix} ap+br & aq+bs \\
cp+dr & cq+ds \\
\end{pmatrix} \begin{pmatrix} x \\
y \\
\end{pmatrix}
\end{aligned}
$$
#### 연립일차방정식과 행렬의 관계
- 계수행렬: 연립일차방정식의 계수만 모아놓은 행렬 
- 상수항: 연립일차방정식의 상수를 모아놓은 행렬
- 첨가행렬: 계수와 상수를 모두 모아놓은 행렬
- Leading Entry: 각 행에서 처음으로 0이 아닌 성분
##### 행 사다리꼴 행렬
- 행 사다리꼴 행렬의 3가지 조건
1. 각 행의 Leading Entry는 1이다.
2. 모든 성분이 0인 행은 마지막에 위치한다.
3. 현재 행의 Leading Entry는 위 행의 Leading Entry보다 오른쪽 열에 위치하고, 아래 행의 Leading Entry보다 왼쪽 열에 위치해야 한다.
- 기약 행 사다리꼴: 위 3가지 조건을 지키면서 Leading Entry에 속한 열의 나머지 성분은 모두 0인 사다리꼴
##### 가우스-조던 소거법
- 다음 세 가지의 기본 행 연산을 통해 연립일차방정식의 첨가행렬을 기약 행 사다리꼴로 변환하여 해를 구한다.
1. 한 행을 상수배한다.
2. 한 행을 상수배하여 다른 행에 더한다.
3. 두 행을 맞바꾼다.
##### 역행렬 이용
- $A=$계수행렬, $B=$상수항
- 연립일차방정식 $AX=B$에서 $A$의 역행렬 $A^{-1}$가 존재하면, $X=A^{-1}B$
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

# 크래머 공식
- 연립일차방정식 $AX=B$에서, $A$가 행렬식이 0이 아닌 정사각행렬일 때,

$$
\begin{aligned}
x_j=\frac{detA_j}{detA}
\end{aligned}
$$

- 단, $j=1, \cdots, n$이고 $A_j$는 $A$의 $j$번째 열을 $B$의 $j$번째 열로 바꾼 행렬이다.