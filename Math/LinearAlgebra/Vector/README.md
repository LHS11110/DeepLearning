# 벡터
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
- n차원의 벡터 $w$가 임의의 실수 $k1, k2, \cdots, k_r$에 대하여 $w=k_{1}v_{1}+k_{2}v_{2}+\cdots+k_{r}v_{r}$
- $w$를 $v_1, v_2, \cdots, v_r$의 선형(일차)결합이라 한다.
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