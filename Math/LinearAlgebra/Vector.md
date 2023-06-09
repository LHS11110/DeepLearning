# 물리적 벡터
## n차원 벡터
- n차원상의 벡터 $V=(v_1, v_2, \cdots, v_n)$
- 영벡터 $\vec 0 = 0 = (0, 0, \cdots, 0)$
- 두 벡터 $v=(v_1, v_2, \cdots, v_n), w=(w_1, w_2, \cdots, w_n)$가 같다. $\Leftrightarrow v_1=w_1, \cdots, v_n=w_n$
## 벡터 연산
- 노름(norm): 벡터의 크기 (또는 길이), $||v||=\sqrt (v_1^2 + v_2^2 + \cdots + v_n^2)$
- 단위벡터: 노름이 1인 벡터, 정규화: $\frac{v}{||v||}$
- 표준단위벡터: $e_1=(1, 0, \cdots, 0), e_2=(0, 1, \cdots, 0)$
### 벡터의 덧셈과 뺄셈
- $v \pm w = (v_1 \pm w_1, \cdots, v_n \pm w_n)$
### 벡터의 실수배
- $kv=(kv_1, kv_2, \cdots, kv_n)$
### 선형(일차)결합
- 벡터를 나타내는 또 다른 방법을 말한다. $n$개의 벡터에 실수배를 하고 모두 더해 얻어지는 벡터가 $w$와 같다면, $w$는 벡터 $n$개의 선형(일차)결합이라 한다.
- $w=k_1v_1 + k_2v_2 + \cdots + k_nv_n$, 이때 $v$는 벡터이고 $k$는 임의의 실수값이다.
## 스칼라 곱(내적)
- Dot Product라고도 하며, 두 벡터로부터 실수 스칼라를 얻는 연산

$$
\begin{aligned}
v \cdot w &= |v||w|cos\theta \\
&= v_1 w_1 + v_2 w_2 + \cdots + v_n w_n
\end{aligned}
$$

## 벡터 연산 성질
1. $u + v = v + u$
2. $(u + v) + w = u + (v + w)$
3. $u + 0 = u$
4. $u + (-u) = 0$
5. $k(u + v) = ku + kv$
6. $k(mu) = (km)u$
7. $r(u + v) = ru + rv$
8. $1u = u, 0u = 0$
## 벡터 곱
- 가위 곱(cross product) 또는 외적이라고도 한다.
- 연산 결과로 벡터가 나오며 방향은 주어진 두 벡터의 수직이고, 크기는 두 벡터로 만들어진 평행사변형의 면적이다.

$$
\begin{aligned}
v \times w = (det \begin{pmatrix} v_2 & v_3 \\
w_2 & w_3\end{pmatrix}, -det \begin{pmatrix} v_1 & v_3 \\
w_1 & w_3\end{pmatrix}, det \begin{pmatrix} v_1 & v_2 \\
w_1 & w_2 \end{pmatrix})
\end{aligned}
$$

## 벡터 곱 연산 성질
1. $u \times v = -(v \times u)$
2. $u \times (v + w) = (u \times v) + (u \times w)$
3. $k(u \times v) = (ku) \times v = u \times (kv)$
4. $u \times 0 = 0$
5. $u \times u = 0$
# 수학적 벡터
## 대수구조
- 대수구조란 원소들에 대해 일련의 연산들이 주어진 집합을 말한다.
- 대수학은 이러한 대수구조를 연구하는 학문이다.
- 반군: 결합법칙을 따르는 하나의 이항 연산을 갖는 대수구조
- 모노이드: 항등원을 가지면서 반군을 따르는 대수구조
- 군: 역원을 가지면서 모노이드를 따르는 대수구조
- 아벨군(가환군): 교환 법칙이 성립하면서 군을 따르는 대수구조
- 환: 덧셈에 대하여 아벨군, 곱셈에 대하여 반군을 따르며 분배법칙이 성립하는 대수구조
- 가군: 어떤 환의 원소에 대한 곱셈이 주어지며, 분배법칙이 성립하는 아벨군
- 가환환: 곱셈이 교환법칙을 만족하는 환
- 나눗셈환: 0이 아닌 모든 원소가 역원을 가지며, 원소가 둘 이상인 환
체: 가환환인 나눗셈환. 즉, 사칙연산이 자유로이 시행 될 수 있고 산술의 잘 알려진 규칙들을 만족하는 대수구조
## 벡터공간
- 체 $F$에 대한 가군($V, +, \cdot$)을 벡터공간, $V$의 원소를 벡터라 한다.
- 이때 $+$는 벡터의 덧셈이고, $\cdot$은 벡터의 스칼라배이다.
- $(V, +)$는 아벨군이다. $(u, v, w \in V)$
- $(V, +, \cdot)$는 $F$의 가군이다. $(k, m \in F)$
## 선형생성
### 부분벡터공간
- 벡터공간 $V$상에서 정의된 덧셈과 스칼라배에 대하여 그 자체로서 벡터공간이 되는 $V$의 부분집합 $W$를 $V$의 부분벡터공간 또는 부분공간이라 한다.
### 선형생성
- 벡터공간 $V$의 공집합이 아닌 부분집합 $S={v_1, v_2, \cdots, v_n}$내의 벡터들의 가능한 모든 선형결합으로 이루어진, $V$의 부분벡터공간을 $S$의 (선형)생성 $span(S)$라 한다.

$$
\begin{aligned}
\end{aligned}
$$