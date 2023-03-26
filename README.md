# DeepLearning
- 딥러닝은 인공신경망(Artificial Neural Networks)을 기반으로 하는 머신러닝 기술 중 하나이다.
- 대규모 데이터셋을 사용하여 패턴을 인식하고 학습한다.
- 인공신경망은 생물학적 뉴런의 동작에서 영감을 받아 설계된 수학적 모델로, 입력층, 은닉층, 출력층 등으로 구성된다.
- 딥러닝은 이러한 인공신경망의 구조를 여러 층으로 구성해 보다 복잡한 문제를 해결할 수 있도록 하였다.
- 딥러닝은 다양한 분야에서 활용되며 이미지 인식, 음성 인식, 자연어 처리 등 다양한 분야에서 높은 성능을 보이고 있다.
- 대부분 전결합 계층(Fully Connected Layer) 구조로 구현되며 FC Layer는 행렬 연산으로 표현 가능하다.
## 딥러닝 수학적 모델
$$
\begin{aligned}
x&: 입력 행렬 \\
b&: 편향 행렬 \\
w&: 가중치 행렬 \\
y&: 출력 행렬 \\
a&: 활성화 함수 \\
x_{1, M}&=\begin{pmatrix}x_0 & x_1 & x_2 & \cdots & x_{M - 1} \end{pmatrix} \\
b_{1, N}&=\begin{pmatrix}b_0 & b_1 & b_2 & \cdots & b_{N - 1} \end{pmatrix} \\
w_{M, N}&=\begin{pmatrix}w_{0, 0} & w_{0, 1} & \cdots & w_{0, N - 1} \\
w_{1, 0} & w_{1, 1} & \cdots & w_{1, N - 1} \\
\vdots & \vdots & \ddots & \vdots \\
w_{M - 1, 0} & w_{M - 1, 1} & \cdots & w_{M - 1, N - 1} \\
\end{pmatrix} \\
\\
y_{1, N}&=a(wx + b)
\end{aligned}
$$
# Perceptron
- 퍼셉트론은 인공신경망의 한 종류로, 이진 분류(Binary Classification) 문제를 해결하는 데에 사용된 간단한 모델이다.
- 딥러닝의 기반이 되는 모델로 입력값(Input)과 가중치(Weight)를 곱한 합을 임계치(Threshold)와 비교하여 출력값(Output)을 결정한다.
- 입력값으로 출력값을 도출하는 과정에서 활성화 함수(Activation Function)를 사용하여 입력값과 가중치의 합을 변환한다.
- 초기 퍼셉트론에서는 계단 함수(Step Function)를 활성화 함수로 사용했다.
- 퍼셉트론은 여러 입력값을 받아서 하나의 출력값을 만들어 내는 구조이며 단층 퍼셉트론(Single-Layer Perceptron)과 다층 퍼셉트론(Multi-Layer Perceptron)으로 나뉜다.
- 단층 퍼셉트론은 하나의 선형 분리(Linear Separability) 가능한 문제를 해결할 수 있다.
- 다층 퍼셉트론은 여러 층의 노드로 이루어진 인공신경망으로, 다양한 비선형 문제를 해결할 수 있다.
## 퍼셉트론 수학적 모델
- f는 활성화 함수, x는 입력, w는 가중치, b는 편향(Bias)이다.
$$f\big((\displaystyle\sum_{i=0}^{n} w_i x_i) + b\big)$$
# 기본적인 딥러닝 구성 요소와 의미
## 입력층
- 모델의 입력값을 받는 층이다. 입력에는 정수값 또는 실수값을 사용하며 여러 입력이 주어질 수 있다.
## 은닉층
- 입력층과 출력층 사이에 존재한다. 여러 개의 층을 사용할수록 더 복잡한 문제를 학습할 수 있다.
## 출력층
- 모델의 출력값을 생성하는 층이다.
## 가중치
- 입력값과 노드들 간의 연결 강도를 조절하는 매개변수이다. 가중치는 모델이 학습되는 과정에서 업데이트된다.
## 편향
- 모델의 각 노드에 더해지는 상수값이다. 입력값이 없는 노드를 활성화시키기 위한 용도이다.
## 활성화 함수
- 입력값과 가중치의 합을 변환하는 함수이다. 활성화 함수는 비선형 함수이며 모델의 복잡도를 올려 비선형 패턴을 학습할 수 있게 한다.
- 활성화 함수를 사용하지 않거나 활성화 함수가 선형 함수라면 은닉층을 쌓는 의미가 없다. 이는 비선형 분류기를 구현할 수 없다는 뜻이 된다.
## 손실 함수
- 모델의 출력값과 실제값의 차이를 측정하는 함수이다. 손실 함수는 틀린 정답일수록 차이가 크므로 손실 함수를 최소화하는 방향으로 모델을 학습시킨다.
## 옵티마이저
- 손실 함수를 최소화하는 가중치와 편향을 찾는 최적화 알고리즘이다. SGD(Stochastic Gradient Descent) 등이 대표적인 옵티마이저이다.