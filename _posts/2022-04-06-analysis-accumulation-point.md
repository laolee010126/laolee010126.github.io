---
title: 해석학 유클리드 공간 - Accumulation point(聚点，极限点)
date: 2022-04-06
categories: [해석학]
tags: [해석학, 유클리드 공간] # TAG names should always be lowercase
math: true
img_path:
---

# 유클리드 공간 $R_n$

---

## 1. Euclide space(유클리드 공간)

---

### 1-1 Vector space(선형 공간)

벡터 공간을 얘기기전 벡터의 합과 벡터의 스칼라곱을 정의해야한다.
<br/>

> $\alpha \in R$ > <br/> > $\vec{x} \ = \ (x_1, x_2, ..., x_n) \in R^n$ > $\vec{y} \ = \ (y_1, y_2, ..., y_n) \in R^n$

임의의 $\alpha, \vec{x},\vec{y} \ 에 \ 대하여$ 벡터 합과 벡터와 스칼라 곱을 아래와 같이 정의한다.

\begin{gather}
\vec{x} \ 와 \ \vec{y} \ 의 \ 합 \ 정의
\\\\\vec{x} + \vec{y} \ = \ (x_1 + y_1, x_2 + y_2, ..., x_n + y_n)
\end{gather}

<br/>

\begin{gather}
a 와 \ \vec{x} \ 의 \ 곱 \ 정의
\\\\a\vec{x} \ = \ (ax_1, ax_2, ..., ax_n)
\end{gather}

<br/>
또한 zero element(零元) 이랑 unit element(单位元)은 아래와 같이 정의한다.
<br/>
<br/>
$\exists \vec{0} \in R^n \ s.t \ \forall \vec{x} \in R^n$
\begin{gather}
\vec{x} \ + \ \vec{0}  \ = \ \vec{x} \ ;
\end{gather}

$\exists 1 \in R \ s.t \ \forall \vec{x} \in R^n$
\begin{gather}
1\vec{x} \ = \ \vec{x} \ ;
\end{gather}

<br/>

> 정의: 위에 나오는 선형 연산들을 부여한 $R^n$ 을 n demendion vector space 라고 한다.
> {: .prompt-info }

---

### 1-2 Definition of Euclide space(유클리드 공간 정의)

위에서 정의한 선형공간에 내적(dot product) 이라는 연선을 추가해 유클리드 공간을 정의한다.

#### Dot product(내적)

\begin{gather}
\vec{x}\vec{y} \ = \ \sum\_{i=-1}^{n} x_iy_i
\end{gather}

<br/>

벡터공간에 내적 연산을 추가함으로써 유클리드 공간이 정의된다.

---

## 2. Limit of dot sequence(점 수열 극한)

점 수열의 극한 이해: 점들이 마지막에 한 점으로 모인다.

### 정리 13.1.1 (点列 극한 <=> 벡터의 한 원소 의 극한 = 극한 벡터의 대응 원소)

$\lim\_{k\to\infty} \\{\vec{x}\_k\\} \ = \ \vec{x}\_0 $

$\Leftrightarrow $

$\forall i \ \lim_{k\to\infty} x_i^k = x_i^0$

### 点列极限性质

1. $\\{x_k\\}$ 극한이 존재할때, 극한값은 유일하다.
2. $\\{x_k\\}$ 극한이 존재할때, $\\{x_k\\}$ 는 유계이다.
3. 벡터극한의 내적, 벡터극한과 스칼라의 곱, 벡터극한끼리 더하기 가능.

---

## 3. Accumulation point

### 3-1 Definition of accumulation point

정의:
$E$ 는 $E \subset{R^n}$ 를 만족하는 주어진 집합이라고 설정한다. 만약 $x \in R^n$ 의 임의의 $\delta$ 구역 $U(\vec{x}, \delta), (\delta > 0)$ 에 $E$ 중 $\vec{x}$ 와 다른 점 이 존재한다면, $\vec{x}$ 는 accumulation point(聚点) 혹은 극한점(极限点)이라고 한다.
<br/>

> 聚点의 존재 의의는 어떤 점이 聚点이면 그 점에서 극한을 취할 수 있다.
> {: .prompt-tip }

<br/>

### 3-2 isolated point

정의:
$\vec{x} \in E$ 에대하여, $\exists \ \delta_0  \ s.t \ \vec{x} \notin U_0(\vec{x}, \delta_0)$ 이러한 점을 isolated point(孤立点)라고 한다.

> E에 포함되지만, 聚点은 아닌 点을 isolated point(孤立点)라고 이해하면 된다.
> {: .prompt-tip }

---

## 开集，闭集

### 중요한 세가지 점들

1. 内点($E^\circ$): 孤立点이 아닌 범위 내의 점
2. 外点($(E^c)^\circ$): 범위의 테두리가 아닌 바깥점
3. 边界点$(\partial E)$: 범위의 테두리 + 孤立点

![img-description](/assets/img/myimg/analysis-dots.jpeg)

> 总结: 聚点은 内点 + 테두리점들；孤立点은 혼자 떨어져있는 점들
> {: .prompt-tip }

### 开集，闭集

1. 开集: $E = E^\circ$
2. 闭集: $E^c = (E^c)^\circ$

### 开集，闭集성질

1. 开集的性质
   1. $R^n$ 与 $\empty$ is open set
   2. 任意个开集的并是开集
