---
layout: splash
title: "Mathematical Methods for Physicists Ch4"
permalink: /solutions/math_physics_04
author_profile: false

---

# Chapter 4 Tensors and Differential Forms

## 4.1 Tensor Analysis

### 4.1.1

{% raw %}

$$
\newcommand{\T}{\mathrm}
\newcommand{\V}{\mathbf}
\newcommand{\pdv}[2]{\frac{\partial#1}{\partial#2}}
\newcommand{\del}{\boldsymbol{\nabla}}
\newcommand{\VE}{\mathbf{\hat{e}}}
\newcommand{\EE}{\pmb{\varepsilon}}
$$
Let all the components of a tensor $\T{A}$ vanish in a coordinate system $K$. For any coordinate system $K'$, the components of $\T{A}$ in $K'$ are linear combinations of components of $\T{A}$ in $K$ according to the transformation laws of tensors, and is therefore zero. So in every coordinate systems, all the components of $\T{A}$ vanish.

-----

### 4.1.2

$$
\begin{aligned}
A_{ij}=\sum_k\sum_l\pdv{(x^0)^k}{x^i}\pdv{(x^0)^l}{x^j}A^0_{kl}=\sum_k\sum_l\pdv{(x^0)^k}{x^i}\pdv{(x^0)^l}{x^j}B^0_{kl}=B_{ij}
\end{aligned}
$$

-----

### 4.1.3

Let the vector be $\V{A}$, and its components be $A^i$ and $(A')^i$ in the two reference frames. For $i=1,2,3$, $A^i=0$ and $(A')^i=0$. Applying the transformation law,

$$
\begin{aligned}
(A')^i=\sum_j\pdv{(x')^i}{x^j}A^j=\pdv{(x')^i}{x^0}A^0
\end{aligned}
$$

For $i=1,2,3$, $(A')^i=0$, but at least one of $\pdv{(x')^i}{x^0}\neq0$, so $A^0$ must be zero. So all the components of $\V{A}$ in the first reference frame vanish, and by exercise 4.1.1, all the components of $\V{A}$ vanish in every reference frame. In particular, the zeroth component of $\V{A}$ vanish in every reference frame.

-----

### 4.1.4

Let $\T{A}$ be an isotropic second-rank tensor in 3-D space. Consider the $90^\circ$ rotation about $x_3$ axis. Then $(x')^1=x^2$, $(x')^2=-x^1$, $(x')^3=x^3$. So 

$$
\begin{aligned}
A^{11}=(A')^{11}=\sum_i\sum_j\pdv{(x')^1}{x^i}\pdv{(x')^1}{x^j}A^{ij}=\pdv{(x')^1}{x^2}\pdv{(x')^1}{x^2}A^{22}=A^{22}
\end{aligned}
$$

Similarly, we can prove $A^{22}=A^{33}$, so $A^{11}=A^{22}=A^{33}=k$, $k$ is a constant.

Consider the $180^\circ$ rotation about $x_3$ axis. Then $(x'')^1=-x^1$, $(x'')^2=-x^2$, $(x'')^3=x^3$. So

$$
\begin{aligned}
A^{13}=(A'')^{13}=\sum_i\sum_j\pdv{(x'')^1}{x^i}\pdv{(x'')^3}{x^j}A^{ij}=\pdv{(x')^1}{x^1}\pdv{(x')^1}{x^3}A^{13}=(-1)(1)A^{13}=-A^{13}
\end{aligned}
$$

so $A^{13}=0$. Similarly, we can prove $A^{31}=A^{12}=A^{21}=A^{23}=A^{32}=0$. Therefore, 

$$
\begin{aligned}
A^{ij}=
\begin{cases}
k,\quad i=j\\
0,\quad i\neq j
\end{cases}
\end{aligned}
$$

which is $k\delta^i_j$.

-----

### 4.1.5

[First raletion]
If $i=k$, then $R_{iklm}=-R_{kilm}=-R_{iklm}$, so $R_{iklm}=0$. The same is for $l=m$, so $R_{iklm}\neq0$ only if $i\neq k$ and $l\neq m$. $R_{ik\textit{__}}$ will determine $R_{ki\_\_}$, and $R_{\_\_lm}$ will determine $R_{\_\_ml}$, so if we let $(i,k),(l,m)\in\{(1,2),(1,3),(1,4),(2,3),(2,4),(3,4)\}$, then all the other components are determined. So the number of independent components is $6\times6=36$.

[Second relation]
If $(i,k)\neq(l,m)$, then $R_{iklm}$ determines $R_{lmik}$. So the number of components reduced is $C^6_2=15$, and the number of independent components becomes $36-15=21$.

[Third relation]
If one of $k,l,m$ equals $i$, let it be $k$, then the relation becomes $R_{iilm}+R_{ilmi}+R_{imil}=0$. Using the first two relations, it becomes $R_{imil}+R_{miil}=0$, which is the first relation, so no new information are obtained. If two of $k,l,m$ are equal, let it be $k=l$, then the relation become $R_{ikkm}+R_{ikmk}+R_{imkk}=0$. Using the first  relation, it becomes $R_{ikkm}+R_{ikmk}=0$, which is the first relation, so no new information are obtained. So the relation furnishes new information only if all four indices are different. 
Using the first relation, $R_{iklm}+R_{ilmk}+R_{imkl}=0$ becomes $R_{ikml}+R_{ilkm}+R_{imlk}=0$, so the parity of the permutation of $k,l,m$ does not matter. 
Using the first two relation, $R_{iklm}+R_{ilmk}+R_{imkl}=0$ becomes $R_{klmi}+R_{kmil}+R_{kilm}=0$, so whether the first index is $1,2,3$ or $4$ does not matter. Therefore, let $=1$, and $(k,l,m)=(2,3,4)$, then we get a new equation, so the number of independent components becomes $21-1=20$.

-----

### 4.1.6

If two of $i,k,l,m$ are equal, that it be $i=k$, then $T_{iklm}=-T_{kilm}=-T_{iklm}$, so $T_{iklm}=0$. So $T_{iklm}\neq0$ only if all the indices are different. But there are only three possible values (3-D space) for the four indices, so at least two of $i,k,l,m$ are equal, so $T_{iklm}=0$. Therefore, there are no independent components.

-----

### 4.1.7

By the transformation law, 

$$
\begin{aligned}
(T')_{\cdots i}=\sum\cdots\sum_k\cdots\pdv{x^k}{(x')^i}T_{\cdots k}
\end{aligned}
$$

Defining $\left(\pdv{T}{x} \right)_{\cdots ij}=\pdv{T_{\cdots i}}{x_j}$. If the transformation is linear, then $\pdv{^2x^\mu}{(x')^j(x')^i}=0$ for all $\mu$. So

$$
\begin{aligned}
\left(\pdv{T}{x} \right)'_{\cdots ij}&=\pdv{(T')_{\cdots i}}{(x')^j}=\sum\cdots\sum_k\cdots\pdv{x^k}{(x')^i}\sum_l\pdv{x^l}{(x')^j}\pdv{T_{\cdots k}}{x^l}\\
&=\sum\cdots\sum_k\sum_l\cdots\pdv{x^k}{(x')^i}\pdv{x^l}{(x')^j}\pdv{T_{\cdots k}}{x^l}\\
&=\sum\cdots\sum_k\sum_l\cdots\pdv{x^k}{(x')^i}\pdv{x^l}{(x')^j}\left(\pdv{T}{x}\right)_{\cdots kl}
\end{aligned}
$$

which is the transformation law for tensors of rank $n+1$, so $\left(\pdv{T}{x} \right)_{\cdots ij}=\pdv{T_{\cdots i}}{x_j}$ is a tensor of rank $n+1$.

-----

### 4.1.8

By the transformation law, 

$$
\begin{aligned}
(T')_{ijk\cdots}=\sum_l\sum_m\sum_n\cdots\sum\pdv{x^l}{(x')^i}\pdv{x^m}{(x')^j}\pdv{x^n}{(x')^k}\cdots T_{lmn\cdots}
\end{aligned}
$$

Note that in Cartesian coordinates, $\pdv{x^m}{(x')^j}=\pdv{(x')^j}{x^m}$. So

$$
\begin{aligned}
\sum_j\pdv{(T')_{ijk\cdots}}{(x')^j}&=\sum_j\sum_l\sum_m\sum_n\cdots\sum\pdv{x^l}{(x')^i}\pdv{x^m}{(x')^j}\pdv{x^n}{(x')^k}\cdots\pdv{T_{lmn\cdots}}{(x')^j}\\
&=\sum_l\sum_m\sum_n\cdots\sum\pdv{x^l}{(x')^i}\pdv{x^n}{(x')^k}\cdots\sum_j\pdv{(x')^j}{x^m}\pdv{T_{lmn\cdots}}{(x')^j}\\
&=\sum_l\sum_m\sum_n\cdots\sum\pdv{x^l}{(x')^i}\pdv{x^n}{(x')^k}\cdots\pdv{T_{lmn\cdots}}{x^m}\\
&=\sum_l\sum_n\cdots\sum\pdv{x^l}{(x')^i}\pdv{x^n}{(x')^k}\cdots\sum_m\pdv{T_{lmn\cdots}}{x^m}
\end{aligned}
$$

which is the transformation law for tensors of rank $n-1$, so $\sum_j\pdv{T_{ijk\cdots}}{x^j}$ is a tensor of rank $n-1$.

-----

### 4.1.9

When defining $x_4=ict$, the Lorentz transformations take the form

$$
\begin{aligned}
\begin{pmatrix}
x'_1\\x'_2\\x'_3\\x'_4
\end{pmatrix}=
\begin{pmatrix}
\gamma&0&0&i\gamma\beta\\
0&1&0&0\\
0&0&1&0\\
-i\gamma\beta&0&0&\gamma
\end{pmatrix}
\begin{pmatrix}
x_1\\x_2\\x_3\\x_4
\end{pmatrix}
\end{aligned}
$$

or $\V{x'}=\T{U}\V{x}$, where $\gamma=\frac{1}{\sqrt{1-\frac{v^2}{c^2}}}$, $\beta=\frac{v}{c}$. It can be verified that $\T{U}$ is orthogonal, so $\T{U}^{-1}=\T{U}^T$, and $\V{x}=\T{U}^T\V{x'}$.\quad $\pdv{x'_i}{x_j}=\T{U}_{ij}$, and $\pdv{x_j}{x'_i}=\T{U}^T_{ji}=\T{U}_{ij}$, so $\pdv{x'_i}{x_j}=\pdv{x_j}{x'_i}$. (Therefore, as long as the transformation is orthogonal, this relation holds.)

$$
\begin{aligned}
({\square}^2)'&=\sum_i\pdv{^2}{(x'_i)^2}=\sum_i\pdv{}{x'_i}(\pdv{}{x'_i})=\sum_i\sum_j\pdv{x_j}{x'_i}\pdv{}{x_j}(\pdv{}{x'_i})=\sum_i\sum_j\pdv{x_j}{x'_i}\pdv{^2}{x_j\partial x'_i}\\
&=\sum_j\sum_i\pdv{x'_i}{x_j}\pdv{^2}{x'_i\partial x_j}=\sum_j\sum_i\pdv{x'_i}{x_j}\pdv{}{x'_i}(\pdv{}{x_j})=\sum_j\pdv{}{x_j}(\pdv{}{x_j})=\sum_j\pdv{^2}{{x_j}^2}={\square}^2
\end{aligned}
$$

so the d’Alembertian is invariant under Lorentz transformation.

-----

### 4.1.10

(Using the Einstein convention)

$$
\begin{aligned}
K_{mn}A^mB^n=K_{mn}\pdv{x^m}{(x')^i}\pdv{x^n}{(x')^j}(A')^i(B')^j=(K')_{ij}(A')^i(B')^j
\end{aligned}
$$

so

$$
\begin{aligned}
\left[(K')_{ij}-K_{mn}\pdv{x^m}{(x')^i}\pdv{x^n}{(x')^j} \right](A')^i(B')^j=0
\end{aligned}
$$

Because $\T{A'}$ and $\T{B'}$ are arbitrary, the coefficient must vanish. (For example, to prove $(K')_{12}-K_{mn}\pdv{x^m}{(x')^1}\pdv{x^n}{(x')^2}$=0, set $(A')^1=(B')^2=1$, all the other components of $\T{A'}$ and $\T{B'}=0$.) Therefore,

$$
\begin{aligned}
(K')_{ij}=K_{mn}\pdv{x^m}{(x')^i}\pdv{x^n}{(x')^j}
\end{aligned}
$$

which means that $K_{ij}$ is a second-rank tensor.

-----

### 4.1.12

(Using the Einstein convention)

$$
\begin{aligned}
(B')^k_i&=\pdv{(x')^k}{x^p}\pdv{x^m}{(x')^i}B^p_m
=\pdv{(x')^k}{x^p}\pdv{x^m}{(x')^i}K_{mn}A^{np}\\
&=\pdv{(x')^k}{x^p}\pdv{x^m}{(x')^i}K_{mn}\pdv{x^n}{(x')^j}\pdv{x^p}{(x')^l}(A')^{jl}\\
&=K_{mn}\pdv{x^m}{(x')^i}\pdv{x^n}{(x')^j}\left(\pdv{(x')^k}{x^p}\pdv{x^p}{(x')^l} \right)(A')^{jl}\\
&=K_{mn}\pdv{x^m}{(x')^i}\pdv{x^n}{(x')^j}\delta^k_l(A')^{jl}\\
&=K_{mn}\pdv{x^m}{(x')^i}\pdv{x^n}{(x')^j}(A')^{jk}\\
&=(K')_{ij}(A')^{jk}
\end{aligned}
$$

so

$$
\begin{aligned}
\left[(K')_{ij}-K_{mn}\pdv{x^m}{(x')^i}\pdv{x^n}{(x')^j} \right](A')^{jk}=0
\end{aligned}
$$

Because $\T{A'}$ is arbitrary, the coefficient must vanish. Therefore,

$$
\begin{aligned}
(K')_{ij}=K_{mn}\pdv{x^m}{(x')^i}\pdv{x^n}{(x')^j}
\end{aligned}
$$

which means that $\T{K}$ is a second-rank tensor.

## 4.2 Pseudsotensors, Dual Tensors

### 4.2.1

Let the transformation matrix from $\V{x}$ to $\V{x'}$ be $\T{A}$, then

$$
\begin{aligned}
\renewcommand{\arraystretch}{1.5}
\T{A}=
\begin{pmatrix}
\pdv{(x')^1}{x^1}&\pdv{(x')^1}{x^2}&\pdv{(x')^1}{x^3}\\
\pdv{(x')^2}{x^1}&\pdv{(x')^2}{x^2}&\pdv{(x')^2}{x^3}\\
\pdv{(x')^3}{x^1}&\pdv{(x')^3}{x^2}&\pdv{(x')^3}{x^3}\\
\end{pmatrix}
\end{aligned}
$$

(take $n=3$ for example). Then $\det{(\T{A})}=\varepsilon_{ljk}\pdv{(x')^l}{x^1}\pdv{(x')^j}{x^2}\pdv{(x')^k}{x^3}$ (using Einstein convention)(we use $l$ instead of $i$ for reason that will soon be clear). If we permute $(1,2,3)$, then we must permute $(l,j,k)$ in the same way to retain the formula $\pdv{(x')^l}{x^1}\pdv{(x')^j}{x^2}\pdv{(x')^k}{x^3}$. Therefore, 

$$
\begin{aligned}
    \varepsilon_{ljk}\pdv{(x')^l}{x^m}\pdv{(x')^j}{x^n}\pdv{(x')^k}{x^p}=\varepsilon_{mnp}\varepsilon_{ljk}\pdv{(x')^l}{x^1}\pdv{(x')^j}{x^2}\pdv{(x')^k}{x^3}=\varepsilon_{mnp}\det{(\T{A})}
\end{aligned}
\tag{1}
$$

$C_i$ is a pseudovector, so the transformation law gives

$$
\begin{aligned}
(C')_i&=\det{(\T{A})}\pdv{x^m}{(x')^i}C_m=\det{(\T{A)}}\pdv{x^m}{(x')^i}\frac{1}{2}\varepsilon_{mnp}C^{np}\quad \textit{(combine $\det{(\T{A})}$ and $\varepsilon_{mnp}$)}\\
&=\frac{1}{2}\pdv{x^m}{(x')^i}(\varepsilon_{mnp}\det{(\T{A})})C^{np}\quad\textit{(use equation 1)}\\
&=\frac{1}{2}\pdv{x^m}{(x')^i}\varepsilon_{ljk}\pdv{(x')^l}{x^m}\pdv{(x')^j}{x^n}\pdv{(x')^k}{x^p}C^{np}\quad\textit{(combine $\pdv{x^m}{(x')^i}$ and $\pdv{(x')^l}{x^m}$)}\\
&=\frac{1}{2}\delta^l_i\varepsilon_{ljk}\pdv{(x')^j}{x^n}\pdv{(x')^k}{x^p}C^{np}\\
&=\frac{1}{2}\varepsilon_{ijk}\pdv{(x')^j}{x^n}\pdv{(x')^k}{x^p}C^{np}
=\frac{1}{2}\varepsilon_{ijk}(C')^{jk}
\end{aligned}
$$

the last equality holds because $C_i=\frac{1}{2}\varepsilon_{ijk}C^{jk}$ holds in all coordinate systems, so $(C')_i=\frac{1}{2}\varepsilon_{ijk}(C')^{jk}$.

If $j\neq k$, let $i$ be the remaining value other than $j,k$, then $\varepsilon_{ijk}\neq0$, so we have 

$$
\begin{aligned}
(C')^{jk}=\pdv{(x')^j}{x^n}\pdv{(x')^k}{x^p}C^{np}
\end{aligned}
$$

If $j=k$, then $\pdv{(x')^j}{x^p}\pdv{(x')^k}{x^n}=\pdv{(x')^j}{x^n}\pdv{(x')^k}{x^p}$, and because $\T{C}$ is antisymmetric, so $(C')^{jk}=(C)^{jk}=0$ for $j=k$. Therefore,

$$
\begin{aligned}
&\pdv{(x')^j}{x^n}\pdv{(x')^k}{x^p}C^{np}\\
=&\pdv{(x')^j}{x^1}\pdv{(x')^k}{x^2}(C^{12}+C^{21})+
\pdv{(x')^j}{x^1}\pdv{(x')^k}{x^3}(C^{13}+C^{31})+
\pdv{(x')^j}{x^2}\pdv{(x')^k}{x^3}(C^{23}+C^{32})\\
=&0=(C')^{jk}
\end{aligned}
$$

so $(C')^{jk}=\pdv{(x')^j}{x^n}\pdv{(x')^k}{x^p}C^{np}$ still holds. Therefore, in all cases,

$$
\begin{aligned}
(C')^{jk}=\pdv{(x')^j}{x^n}\pdv{(x')^k}{x^p}C^{np}
\end{aligned}
$$

holds, which implies that $C^{jk}$ is a tensor.

-----

### 4.2.2

If there is a one-to-one correspondence between two sets, then the numbers of elements of the two sets need to be the same. If there is a one-to-one correspondence between the components of a vector $C_i$ and the components of a tensor $(AB)^{jk}$, because the numbers of components of $C_i$ and $(AB)^{jk}$ are different ($n$ and $n^2$), it should mean that the one-to-one correspondence exists between \textit{independent} components of $C_i$ and $(AB)^{jk}$, so the number of _independent_ components of $C_i$ and $(AB)^{jk}$ should be the same.

By the antisymmetry property of ${AB}^{jk}$, ${AB}^{jj}=-{AB}^{jj}$, so ${AB}^{jj}=0$, and ${AB}^{jk}=-{AB}^{kj}$. So the  the number of \textit{independent} components of and $(AB)^{jk}=\frac{n\times n-n}{2}$, should be equal to $n$,  the number of \textit{independent} components of $C_i$. So

$$
\begin{aligned}
\frac{n\times n-n}{2}=n
\end{aligned}
$$

so $n=3$.

-----

### 4.2.3

$$
\begin{aligned}
\del\cdot\del\times\V{A}=\pdv{}{x^i}(\del\times\V{A})_i=\pdv{}{x^i}\varepsilon_{ijk}\pdv{}{x^j}A^k
=(\varepsilon_{ijk}\pdv{}{x^i}\pdv{}{x^j})A^k=0
\end{aligned}
$$

because $\pdv{}{x^i}\pdv{}{x^j}=\pdv{}{x^j}\pdv{}{x^i}$ and $\varepsilon_{ijk}+\varepsilon_{jik}=0$.

$$
\begin{aligned}
(\del\times\del\varphi)_i=\varepsilon_{ijk}\pdv{}{x^j}(\del\varphi)_k=\varepsilon_{ijk}\pdv{}{x^j}\pdv{}{x^k}\varphi=0
\end{aligned}
$$

because $\pdv{}{x^j}\pdv{}{x^k}=\pdv{}{x^k}\pdv{}{x^j}$ and $\varepsilon_{ijk}+\varepsilon_{ikj}=0$.

-----

### 4.2.4

(a)

$$
\begin{aligned}
(A')^{ik}_{jl}&=\pdv{(x')^i}{x^m}\pdv{x^n}{(x')^j}\pdv{(x')^k}{x^p}\pdv{x^q}{(x')^l}\delta^m_n\delta^p_q\\
&=\pdv{(x')^i}{x^m}\pdv{x^m}{(x')^j}\pdv{(x')^k}{x^p}\pdv{x^p}{(x')^l}\\
&=\pdv{(x')^i}{(x')^j}\pdv{(x')^k}{(x')^l}=\delta^i_j\delta^k_l
\end{aligned}
$$


(b) 

$$
\begin{aligned}
(B')^{ij}_{kl}&=\pdv{(x')^i}{x^m}\pdv{x^p}{(x')^k}\pdv{(x')^j}{x^n}\pdv{x^q}{(x')^l}(\delta^m_p\delta^n_q+\delta^m_q\delta^n_p)\\
&=\pdv{(x')^i}{(x')^k}\pdv{(x')^j}{(x')^l}+\pdv{(x')^i}{(x')^l}\pdv{(x')^j}{(x')^k}=
\delta^i_k\delta^j_l+\delta^i_l\delta^j_k
\end{aligned}
$$

(c) 

$$
\begin{aligned}
(C')^{ij}_{kl}&=\pdv{(x')^i}{x^m}\pdv{x^p}{(x')^k}\pdv{(x')^j}{x^n}\pdv{x^q}{(x')^l}(\delta^m_p\delta^n_q-\delta^m_q\delta^n_p)\\
&=\pdv{(x')^i}{(x')^k}\pdv{(x')^j}{(x')^l}-\pdv{(x')^i}{(x')^l}\pdv{(x')^j}{(x')^k}=
\delta^i_k\delta^j_l- \delta^i_l\delta^j_k
\end{aligned}
$$

-----

### 4.2.5

Similar with Exercise 4.2.1, let $\T{A}$ be the transformation matrix from $\V{x}$ to $\V{x'}$, then $\det(\T{A})=\varepsilon_{kl}\pdv{(x')^k}{x^1}\pdv{(x')^l}{x^2}$, and

$$
\begin{equation}
\varepsilon_{kl}\pdv{(x')^k}{x^m}\pdv{(x')^l}{x^n}=
\varepsilon_{mn}\varepsilon_{kl}\pdv{(x')^k}{x^1}\pdv{(x')^l}{x^2}=\varepsilon_{mn}\det(\T{A})
\end{equation}
\tag{1}
$$

$\varepsilon_{ij}$ is defined as $\varepsilon_{11}=\varepsilon_{22}=0$, $\varepsilon_{12}=1$, $\varepsilon_{21}=-1$, regardless of which coordinate system it is in. So it is invariant in all coordinate systms, and $(\varepsilon')_{kl}=\varepsilon_{kl}$. (We will use it later.)

$$
\begin{aligned}
(\varepsilon')_{ij}&=(\varepsilon')_{kl}(\delta')^k_i(\delta')^l_j=\varepsilon_{kl}\pdv{(x')^k}{(x')^i}\pdv{(x')^l}{(x')^j}\\
&=\varepsilon_{kl}\pdv{(x')^k}{x^m}\pdv{x^m}{(x')^i}\pdv{(x')^l}{x^n}\pdv{x^n}{(x')^j}\quad\textit{(combining $\varepsilon_{kl}\pdv{(x')^k}{x^m}\pdv{(x')^l}{x^n}$)}\\
&=\left(\varepsilon_{kl}\pdv{(x')^k}{x^m}\pdv{(x')^l}{x^n}\right)\pdv{x^m}{(x')^i}\pdv{x^n}{(x')^j}\quad\textit{(use equation 1)}\\
&=\varepsilon_{mn}\det(\T{A})\pdv{x^m}{(x')^i}\pdv{x^n}{(x')^j}=\det(\T{A})\pdv{x^m}{(x')^i}\pdv{x^n}{(x')^j}\varepsilon_{mn}
\end{aligned}
$$

which is the transformation equation for a second-rank pseudotensor, Therefore $\varepsilon_{ij}$ is a second-rank pseudotensor. It does not contradict the uniqueness of $\delta^i_j$ because we proved $\delta^i_j$ is the only isotropic second rank \textit{tensor} (with a coefficient), while $\varepsilon_{ij}$ is an isotropic second-rank \textit{pseudotensor} (it fails to keep the transformation law under improper rotation). 

-----

### 4.2.6

$$\varepsilon=
\begin{pmatrix}
0&1\\-1&0
\end{pmatrix}$$ in matrix form, and let the orthogonal transformation be  
$$\T{S}=
\begin{pmatrix}
\cos\varphi&\sin\varphi\\-\sin\varphi&\cos\varphi
\end{pmatrix}$$. Then the similarity transformation is 

$$
\begin{aligned}
\varepsilon'=\T{S}\varepsilon{\T{S}}^T=
\begin{pmatrix}
\cos\varphi&\sin\varphi\\-\sin\varphi&\cos\varphi
\end{pmatrix}
\begin{pmatrix}
0&1\\-1&0
\end{pmatrix}
\begin{pmatrix}
\cos\varphi&-\sin\varphi\\\sin\varphi&\cos\varphi
\end{pmatrix}=
\begin{pmatrix}
0&1\\-1&0
\end{pmatrix}
\end{aligned}
$$

so $\varepsilon_{ij}$ is invariant under orthogonal similarity transformations. It corresponds to the isotropic property of $\varepsilon_{ij}$ under proper rotation.

-----

### 4.2.7

Using the result from Exercise 2.1.9, we have $\varepsilon^{mnk}\varepsilon_{ijk}=\delta^m_i\delta^n_j-\delta^m_j\delta^n_i$, so

$$
\begin{aligned}
\varepsilon^{mnk}A_k
=\varepsilon^{mnk}\frac{1}{2}\varepsilon_{ijk}B^{ij}
=\frac{1}{2}(\delta^m_i\delta^n_j-\delta^m_j\delta^n_i)B^{ij}=\frac{1}{2}(B^{mn}-B^{nm})=B^{mn}
\end{aligned}
$$


## 4.3 Tensors in General Coordinates

### 4.3.1

$q^i,q^j,q^k$ are independent, so $\EE^i,\EE^j,\EE^k$ is linear independent. (If $\EE^i,\EE^j,\EE^k$ is linear dependent, which means $a\EE^i+b\EE^j+c\EE^k=0$, then $\pdv{(aq^i+bq^j+cq^k)}{x}\VE_x+\pdv{(aq^i+bq^j+cq^k)}{y}\VE_y+\pdv{(aq^i+bq^j+cq^k)}{z}\VE_z=0$, so $aq^i+bq^j+cq^k=d$, which means $q^i,q^j,q^k$ are dependent.)

Express $\frac{\EE_j\times\EE_k}{\EE_j\times\EE_k\cdot\EE_i}$ in the bases of $\EE^i,\EE^j,\EE^k$, and note that $\EE^p\cdot\EE_q=\delta^p_q$, no matter whether $\EE^i,\EE^j,\EE^k$ and $\EE_i,\EE_j,\EE_k$ are orthogonal. Then

$$
\begin{aligned}
\frac{\EE_j\times\EE_k}{\EE_j\times\EE_k\cdot\EE_i}&=A_i\EE^i+A_j\EE^j+A_k\EE^k\\
\frac{\EE_j\times\EE_k\cdot\EE_i}{\EE_j\times\EE_k\cdot\EE_i}&=1=A_i\\
\frac{\EE_j\times\EE_k\cdot\EE_j}{\EE_j\times\EE_k\cdot\EE_i}&=0=A_j\\
\frac{\EE_j\times\EE_k\cdot\EE_k}{\EE_j\times\EE_k\cdot\EE_i}&=0=A_k
\end{aligned}
$$


so

$$
\begin{aligned}
\frac{\EE_j\times\EE_k}{\EE_j\times\EE_k\cdot\EE_i}=\EE^i
\end{aligned}
$$

-----

### 4.3.2

(a) If $i\neq j$, then $g_{ij}=\EE_i\cdot\EE_j=0$, so $g_{ij}$ is diagonal.

(b)
$g_{ji}=0$ when $i\neq j$, so

$$
\begin{aligned}
&g^{ii}g_{ii}\quad\textit{(no summation on i)}\\
=&g^{ij}g_{ji}\quad\textit{(summation on $j$)}\\
=&\delta^i_i\quad\textit{(by definition of $g^{ij}$)}\\
=&1
\end{aligned}
$$

so 

$$
\begin{aligned}
g^{ii}=\frac{1}{g_{ii}}
\end{aligned}
$$

(c) $\EE_j\cdot\EE_i=0$, so 

$$
\begin{aligned}
&(\EE^i\cdot\EE^i)(\EE_i\cdot\EE_i)\quad\textit{(no summation on i)}\\
=&(\EE^i\cdot\EE^j)(\EE_j\cdot\EE_i)\quad\textit{(summation on $j$)}\\
=&\delta^i_i=1\quad\textit{(by Eq. $4.46$)}
\end{aligned}
$$

so $|\EE^i|^2|\EE_i|^2=1$, which means

$$
\begin{aligned}
|\EE^i|=\frac{1}{|\EE_i|}
\end{aligned}
$$

-----

### 4.3.3

$$
\begin{aligned}
(\EE^i\cdot\EE^j)\cdot(\EE_j\cdot\EE_k)=(\pdv{q^i}{x}\pdv{q^j}{x}+\pdv{q^i}{y}\pdv{q^j}{y}+\pdv{q^i}{z}\pdv{q^j}{z})(\pdv{x}{q^j}\pdv{x}{q^k}+\pdv{y}{q^j}\pdv{y}{q^k}+\pdv{z}{q^j}\pdv{z}{q^k})
\end{aligned}
$$

Note that $j$ is summed, so $\pdv{q^j}{x}\pdv{x}{q^j}=\pdv{x}{x}=1$, and $\pdv{q^j}{x}\pdv{y}{q^j}=\pdv{y}{x}=0$. Similarly, $\pdv{q^j}{y}\pdv{y}{q^j}=\pdv{q^j}{z}\pdv{z}{q^j}=1$, and  other cross terms are zero. So the equation becomes

$$
\begin{aligned}
\pdv{q^i}{x}\pdv{x}{q^k}+\pdv{q^i}{y}\pdv{y}{q^k}+\pdv{q^i}{z}\pdv{z}{q^k}=\pdv{q^i}{q^k}=\delta^i_k
\end{aligned}
$$

-----

### 4.3.4

$$
\begin{aligned}
\Gamma^m_{jk}\,\EE_m&=\pdv{\EE_k}{q^j}=\pdv{^2x}{q^j\partial q^k}\VE_x+\pdv{^2y}{q^j\partial q^k}\VE_y+\pdv{^2z}{q^j\partial q^k}\VE_z\\
&=\pdv{^2x}{q^k\partial q^j}\VE_x+\pdv{^2y}{q^k\partial q^j}\VE_y+\pdv{^2z}{q^k\partial q^j}\VE_z=
\pdv{\EE_j}{q^k}=\Gamma^m_{kj}\,\EE_m
\end{aligned}
$$

so $(\Gamma^m_{jk}-\Gamma^m_{kj})\EE_m=0$. Because $\EE_m$ are linear independent, $\Gamma^m_{jk}-\Gamma^m_{kj}$ must be zero for every $m$, so

$$
\begin{aligned}
\Gamma^m_{jk}=\Gamma^m_{kj}
\end{aligned}
$$

-----

### 4.3.5

$(q^1,q^2,q^3)=(\rho,\varphi,z)$, and $x=\rho\cos\varphi$, $y=\rho\sin\varphi$, $z=z$. So

$$
\begin{aligned}
\EE_1&=\pdv{x}{\rho}\VE_x+\pdv{y}{\rho}\VE_y+\pdv{z}{\rho}\VE_z=\cos\varphi\,\VE_x+\sin\varphi\,\VE_y\\
\EE_2&=\pdv{x}{\varphi}\VE_x+\pdv{y}{\varphi}\VE_y+\pdv{z}{\varphi}\VE_z=-\rho\sin\varphi\,\VE_x+\rho\cos\varphi\,\VE_y\\
\EE_3&=\pdv{x}{z}\VE_x+\pdv{y}{z}\VE_y+\pdv{z}{z}\VE_z=\VE_z\\
(g_{ij})&=
\begin{pmatrix}
\EE_1\cdot\EE_1&\EE_1\cdot\EE_2&\EE_1\cdot\EE_3\\
\EE_2\cdot\EE_1&\EE_2\cdot\EE_2&\EE_2\cdot\EE_3\\
\EE_3\cdot\EE_1&\EE_3\cdot\EE_2&\EE_3\cdot\EE_3\\
\end{pmatrix}=
\begin{pmatrix}
1&0&0\\
0&{\rho}^2&0\\
0&0&1
\end{pmatrix}
\end{aligned}
$$

Because $g^{ij}g_{jk}=\delta^i_k$, the unit matrix, so $(g^{ij})=(g_{jk})^{-1}$, the matrix inverse. Therefore,  

$$
\begin{aligned}
(g^{ij})=
\begin{pmatrix}
1&0&0\\
0&\frac{1}{{\rho}^2}&0\\
0&0&1
\end{pmatrix}
\end{aligned}
$$

-----

### 4.3.6

Differentiate $\EE^i\cdot\EE_k=\delta^i_k$ by $q^j$, we have

$$
\begin{aligned}
&\pdv{\EE^i}{q^j}\cdot\EE_k+\EE^i\cdot\pdv{\EE_k}{q^j}=0\\
&\pdv{\EE^i}{q^j}\cdot\EE_k=-\EE^i\cdot\pdv{\EE_k}{q^j}=-\EE^i\cdot(\Gamma^\mu_{jk}\EE_\mu)=-\Gamma^i_{jk}
\end{aligned}
$$

so

$$
\begin{aligned}
\pdv{\EE^i}{q^j}=-\Gamma^i_{jk}\EE^k
\end{aligned}
$$

when expanded in the contravariant basis.

$V_{i;j}$ is defined as $\pdv{\V{V}'}{q^j}=V_{i;j}\EE^i$. Expand the vector in contravariant basis $\V{V'}=V_i\EE^i$ and differentiate, we have

$$
\begin{aligned}
\pdv{\V{V'}}{q^j}&=\pdv{V_i}{q^j}\EE^i+V_i\pdv{\EE^i}{q^j}\\
&=\pdv{V_i}{q^j}\EE^i-V_i\Gamma^i_{jk}\EE^k\quad\textit{(interchange $i$ and $k$ in the second term)}\\
&=(\pdv{V_i}{q^j}-V_k\Gamma^k_{ji})\EE^i\quad\textit{( $i$ and $j$ in $\Gamma^k_{ji}$ can be interchanged)}\\
&=(\pdv{V_i}{q^j}-V_k\Gamma^k_{ij})\EE^i=V_{i;j}\EE^i
\end{aligned}
$$


So

$$
\begin{aligned}
V_{i;j}=\pdv{V_i}{q^j}-V_k\Gamma^k_{ij}
\end{aligned}
$$

because the set of $\EE^i$ are linear independent.

-----

### 4.3.7

$$
\begin{aligned}
\pdv{V_i}{q^j}-V_k\Gamma^k_{ij}&=\pdv{(g_{ik}V^k)}{q^j}-V_k\Gamma^k_{ij}\\
&=g_{ik}\pdv{V^k}{q^j}+\pdv{g_{ik}}{q^j}V^k-V_k\Gamma^k_{ij}\\
&=g_{ik}\pdv{V^k}{q^j}+\pdv{(\EE_i\cdot\EE_k)}{q^j}V^k-V_k\Gamma^k_{ij}\\
&=g_{ik}\pdv{V^k}{q^j}+V^k\EE_i\cdot\pdv{\EE_k}{q^j}+V^k\EE_k\cdot\pdv{\EE_i}{q^j}-V_k\Gamma^k_{ij}\\
&
=g_{ik}\pdv{V^k}{q^j}+V^m\EE_i\cdot\pdv{\EE_m}{q^j}+V_k\EE^k\cdot\pdv{\EE_i}{q^j}-V_k\Gamma^k_{ij}\\
&=g_{ik}\pdv{V^k}{q^j}+V^m(g_{ik}\EE^k)\cdot\pdv{\EE_m}{q^j}+V_k\Gamma^k_{ij}-V_k\Gamma^k_{ij}\\
&=g_{ik}\pdv{V^k}{q^j}+g_{ik}V^m\Gamma^k_{mj} \\
&=g_{ik}\left[\pdv{V^k}{q^j}+V^m\Gamma^k_{mj} \right]
\end{aligned}
$$

(Or note that $\V{V'}=V_i\EE^i=V^k\EE_k$, so

$$
\begin{aligned}
\pdv{\V{V'}}{q^j}=\left[\pdv{V_i}{q^j}-V_k\Gamma^k_{ij} \right]\EE^i=\left[\pdv{V^k}{q^j}+V^m\Gamma^k_{mj} \right]\EE_k
\end{aligned}
$$

Take the scalar product of both sides with $\EE_i$, and note that $\EE^i\cdot\EE_i=1$, and $\EE_k\cdot\EE_i=g_{ik}$. Therefore,

$$
\begin{aligned}
\pdv{V_i}{q^j}-V_k\Gamma^k_{ij}=\left[\pdv{V^k}{q^j}+V^m\Gamma^k_{mj} \right]g_{ik}
\end{aligned}
$$

which is another verification.)

-----

### 4.3.8

From Eq. 4.63, $\Gamma^n_{ij}=\frac{1}{2}g^{nk}\left[\pdv{g_{ik}}{q^j}+\pdv{g_{jk}}{q^i}-\pdv{g_{ij}}{q^k} \right]$. Because $g^{ij}$ has only diagonal components, $g^{nk}\neq0$ only when $n=k$, so $\Gamma^n_{ij}=\frac{1}{2}g^{nn}\left[\pdv{g_{in}}{q^j}+\pdv{g_{jn}}{q^i}-\pdv{g_{ij}}{q^n} \right]$ ($n$ is not summed). The only non-constant component of $(g_{ij})$ is $g_{22}=\rho=q^1$, so the only non-zero derivative of $g_{ij}$ is $\pdv{g_{22}}{q^1}=2\rho$. When $n=1$, $\pdv{g_{in}}{q^j}+\pdv{g_{jn}}{q^i}=0$, so $i,j$ must be $2$ to have non-zero $\Gamma^n_{ij}$. When $n=2$, $\pdv{g_{ij}}{q^n}=0$, so one of $i,j$ must be $1$ and the other must be $2$ to make $\pdv{g_{in}}{q^j}+\pdv{g_{jn}}{q^i}\neq0$. When $n=3$, none of the derivatives can be non-zero.
Therefore, there are only three nonzero $\Gamma^n_{ij}$: $\Gamma^1_{22}$, $\Gamma^2_{12}$, $\Gamma^2_{21}$.

$$
\begin{aligned}
\Gamma^1_{22}&=\frac{1}{2}(1)[-2\rho]=-\rho\\
\Gamma^2_{12}&=\Gamma^2_{21}=\frac{1}{2}(\frac{1}{{\rho}^2})[2\rho]=\frac{1}{\rho}
\end{aligned}
$$

-----

### 4.3.9

$V^i_{;j}=\pdv{V^i}{q^j}+V^k\Gamma^i_{kj}$, so 

$$
\begin{aligned}
V^1_{;2}&=\pdv{V^1}{q^2}+V^2\Gamma^1_{22}=\pdv{V^\rho}{\varphi}-V^\varphi\rho=V^\rho_{;\varphi}\\
V^2_{;1}&=\pdv{V^2}{q^1}+V^2\Gamma^2_{21}=\pdv{V^\varphi}{\rho}+V^\varphi\frac{1}{\rho}=V^\varphi_{;\rho}\\
V^2_{;2}&=\pdv{V^2}{q^2}+V^1\Gamma^2_{12}=\pdv{V^\varphi}{\varphi}+V^\rho\frac{1}{\rho}=V^\varphi_{;\varphi}
\end{aligned}
$$

For all the other $i,j$,

$$
\begin{aligned}
V^i_{;j}=\pdv{V^i}{q^j}
\end{aligned}
$$

-----

### 4.3.10

$g_{ij;k}$ and $g^{ij}_{;k}$ are not defined in the text, but I think they are probably defined as \\$\pdv{(g_{ij}\EE^i\cdot\EE^j)}{q^k}=g_{ij;k}\,\EE^i\cdot\EE^j$ and $\pdv{(g^{ij}\EE_i\cdot\EE_j)}{q^k}=g^{ij}_{;k}\,\EE_i\cdot\EE_j$. 

$$
\begin{aligned}
\pdv{(g_{ij}\EE^i\cdot\EE^j)}{q^k}&=\pdv{g_{ij}}{q^k}\EE^i\cdot\EE^j+g_{ij}\pdv{\EE^i}{q^k}\cdot\EE^j+g_{ij}\EE^i\cdot\pdv{\EE^j}{q^k}\\
&=\pdv{g_{ij}}{q^k}\EE^i\cdot\EE^j+g_{ij}(-\Gamma^i_{k\alpha}\EE^\alpha)\cdot\EE^j+g_{ij}\EE^i\cdot(-\Gamma^j_{k\beta}\EE^\beta)
\end{aligned}
$$

(_interchange_ $i$ _and_ $\alpha$ _in the second term, and interchange_ $j$ _and_ $\beta$ _in the last term_)

$$
\begin{aligned}
&=\pdv{g_{ij}}{q^k}\EE^i\cdot\EE^j-g_{\alpha j}\Gamma^\alpha_{ki}\EE^i\cdot\EE^j-g_{i\beta}\Gamma^\beta_{kj}\EE^i\cdot\EE^j\\
&=\left[\pdv{g_{ij}}{q^k}-g_{j\alpha }\Gamma^\alpha_{ik}-g_{i\beta}\Gamma^\beta_{jk}\right]\EE^i\cdot\EE^j
\end{aligned}
$$

so 

$$
\begin{aligned}
g_{ij;k}&=\pdv{g_{ij}}{q^k}-g_{j\alpha }\Gamma^\alpha_{ik}-g_{i\beta}\Gamma^\beta_{jk}\quad\textit{(using Eq. $4.63$)}\\
&=\pdv{g_{ij}}{q^k}-g_{j\alpha}\frac{1}{2}g^{\alpha m}\left[\pdv{g_{im}}{q^k}+\pdv{g_{km}}{q^i}-\pdv{g_{ik}}{q^m} \right]-g_{i\beta}\frac{1}{2}g^{\beta n}\left[\pdv{g_{jn}}{q^k}+\pdv{g_{kn}}{q^j}-\pdv{g_{jk}}{q^n} \right]\\
&=\pdv{g_{ij}}{q^k}-\frac{1}{2}\delta^m_j\left[\pdv{g_{im}}{q^k}+\pdv{g_{km}}{q^i}-\pdv{g_{ik}}{q^m} \right]-\frac{1}{2}\delta^n_i\left[\pdv{g_{jn}}{q^k}+\pdv{g_{kn}}{q^j}-\pdv{g_{jk}}{q^n} \right]\\
&=\pdv{g_{ij}}{q^k}-\frac{1}{2}\left[\pdv{g_{ij}}{q^k}+\pdv{g_{jk}}{q^i}-\pdv{g_{ik}}{q^j} \right]-\frac{1}{2}\left[\pdv{g_{ij}}{q^k}+\pdv{g_{ik}}{q^j}-\pdv{g_{jk}}{q^i} \right]\\
&=\pdv{g_{ij}}{q^k}-\pdv{g_{ij}}{q^k}=0
\end{aligned}
$$

We can prove $g^{ij}_{;k}=0$ in a similar way. Or we can note that \[g^{lj}_{;k}\,\EE_l\cdot\EE_j=\pdv{(g^{lj}\EE_l\cdot\EE_j)}{q^k}=\pdv{(g_{lj}\EE^l\cdot\EE^j)}{q^k}=g_{lj;k}\,\EE^l\cdot\EE^j=0\]
multiply both side with $\EE^j\cdot\EE^i$, and note that $(\EE_l\cdot\EE_j)(\EE^j\cdot\EE^i)=\delta^i_l$, we have

$$
\begin{aligned}
g^{lj}_{;k}(\EE_l\cdot\EE_j)(\EE^j\cdot\EE^i)&=0\\
g^{lj}_{;k}\delta^i_l&=0\\
g^{ij}_{;k}&=0
\end{aligned}
$$

-----

### 4.3.11

From Example 4.3.1, the metric tensor of spherical polar coordinates is

$$
\begin{aligned}
(g_{ij})=
\begin{pmatrix}
1&0&0\\
0&r^2&0\\
0&0&r^2\sin^2\theta
\end{pmatrix}
\end{aligned}
$$

so $[\det(g)]^{1/2}=r^2\sin\theta$. Use Eq. 4.69, we have 

$$
\begin{aligned}
\del\cdot\V{V}&=\frac{1}{[\det(g)]^{1/2}}\pdv{}{q^k}\left([\det(g)]^{1/2}V^k \right)\\
&=\frac{1}{r^2\sin\theta}\left[\pdv{}{r}(r^2\sin\theta V^r)+\pdv{}{\theta}(r^2\sin\theta V^\theta)+\pdv{}{\varphi}(r^2\sin\theta V^\varphi) \right]
\end{aligned}
$$

Compared with the results in Chapter 3, and note that 

$$
\begin{aligned}
    \EE_r&=\pdv{\V{r}}{r}=\VE_r & \EE_r V^r&=\VE_r(V^r)=\VE_r V_r & V^r&=V_r\\
    \EE_\theta&=\pdv{\V{r}}{\theta}=r\VE_\theta & \EE_\theta V^\theta&=\VE_\theta(rV^\theta)=\VE_\theta V_\theta & V^\theta&=\frac{1}{r}V_\theta\\
    \EE_\varphi&=\pdv{\V{r}}{\varphi}=r\sin\theta\VE_\varphi & \EE_\varphi V^\varphi&=\VE_\varphi(r\sin\theta V^\varphi)=\VE_\varphi V_\varphi & V^\varphi&=\frac{1}{r\sin\theta}V_\varphi\\
\end{aligned}
$$

Substitute $V^r,V^\theta,V^\varphi$ into the above equation, we get Eq. 3.157.

-----

### 4.3.12

$A_i=\pdv{\varphi}{q^i}$ bexause it is the gradient of a scalar. From Exercise 4.3.6 we have 

$$
\begin{aligned}
A_{i;j}=\pdv{A_i}{q^j}-A_k\Gamma^k_{ij}&=\pdv{^2\varphi}{q^j\partial q^i}-A_k\Gamma^k_{ij}\\
&=\pdv{^2\varphi}{q^i\partial q^j}-A_k\Gamma^k_{ji}=\pdv{A_j}{q^i}-A_k\Gamma^k_{ji}=A_{j;i}
\end{aligned}
$$


so

$$
\begin{aligned}
A_{i;j}-A_{j;i}=0
\end{aligned}
$$

## 4.4 Jacobians

### 4.4.1

(a) If $f(u,v)=0$, then by differentiating we have

$$
\begin{aligned}
\pdv{f}{x}&=\pdv{f}{u}\pdv{u}{x}+\pdv{f}{v}\pdv{v}{x}=0\\
\pdv{f}{y}&=\pdv{f}{u}\pdv{u}{y}+\pdv{f}{v}\pdv{v}{y}=0\\
\pdv{f}{z}&=\pdv{f}{u}\pdv{u}{z}+\pdv{f}{v}\pdv{v}{z}=0
\end{aligned}
$$

which means $\pdv{u}{x}:\pdv{v}{x}=\pdv{u}{y}:\pdv{v}{y}=\pdv{u}{z}:\pdv{v}{z}=(-\pdv{f}{v}):\pdv{f}{u}$, so $\del u=(\pdv{u}{x},\pdv{u}{y},\pdv{u}{z})$ are parallel to $\del v=(\pdv{v}{x},\pdv{v}{y},\pdv{v}{z})$, and therefore $(\del u)\times(\del v)=0$

If $(\del u)\times(\del v)=0$, then $(\pdv{u}{x},\pdv{u}{y},\pdv{u}{z})=a(\pdv{v}{x},\pdv{v}{y},\pdv{v}{z})$ (or $u$,$v$ being interchanged, and $a$ can be zero for one or both of $\del u$,$\del v$ being zero). So $\pdv{(u-av)}{x}=\pdv{(u-av)}{y}=\pdv{(u-av)}{z}=0$, means that $u-av=b$, \\a constant, so $u-av-b=0$ is the relation for $u$ and $v$.

(b) 

$$
\begin{aligned}
J=
\begin{vmatrix}
\pdv{u}{x}&\pdv{u}{y}\\
\pdv{v}{x}&\pdv{v}{y}
\end{vmatrix}
=\pdv{u}{x}\pdv{v}{y}-\pdv{u}{y}\pdv{v}{x}
=\left[(\pdv{u}{x}\VE_x+ \pdv{u}{y}\VE_y)\times(\pdv{v}{x}\VE_x+\pdv{v}{y}\VE_y)\right]_z=\left[(\del u)\times(\del v)\right]_z=0
\end{aligned}
$$

-----

### 4.4.2

$h_1$,$h_2$ are defined as

$$
\begin{aligned}
\pdv{\V{r}}{q_1}&=h_1\VE_1=\pdv{x}{q_1}\VE_x+\pdv{y}{q_1}\VE_y\\
\pdv{\V{r}}{q_2}&=h_2\VE_2=\pdv{x}{q_2}\VE_x+\pdv{y}{q_2}\VE_y
\end{aligned}
$$

Because $\VE_1$ and $\VE_2$ are orthogonal, the area of the parallelogram formed by $h_1\VE_1$ and $h_2\VE_2$ is $h_1h_2$, and also the area of the parallelogram equals to the determinant of components in Cartesian coordinate, so

$$
\begin{aligned}
Area=h_1h_2=
\begin{vmatrix}
\pdv{x}{q_1}&\pdv{y}{q_1}\\
\pdv{x}{q_2}&\pdv{y}{q_2}\\
\end{vmatrix}=
\pdv{x}{q_1}\pdv{y}{q_2}-\pdv{x}{q_2}\pdv{y}{q_1}
\end{aligned}
$$

-----

### 4.4.23

(a) Solve for $x,y$, we have $x=\frac{vu}{v+1}$, $y=\frac{u}{v+1}$, so

$$
\begin{aligned}
J=
\begin{vmatrix}
\pdv{x}{u}&\pdv{y}{u}\\
\pdv{x}{v}&\pdv{y}{v}\\
\end{vmatrix}=\left(\frac{v}{v+1}\right)\left(\frac{-u}{(v+1)^2}\right)-\left(\frac{1}{v+1}\right)\left(\frac{u}{v+1}-\frac{vu}{(v+1)^2}\right)=\frac{-u}{(v+1)^2}
\end{aligned}
$$

(b) 

$$
\begin{aligned}
J^{-1}=
\begin{vmatrix}
\pdv{u}{x}&\pdv{v}{x}\\
\pdv{u}{y}&\pdv{v}{y}\\
\end{vmatrix}=(1)(\frac{-x}{y^2})-(\frac{1}{y})(1)=\frac{-(x+y)}{y^2}=\frac{(v+1)^2}{-u}
\end{aligned}
$$

so

$$
\begin{aligned}
J=\frac{1}{J^{-1}}=\frac{-u}{(v+1)^2}
\end{aligned}
$$

## 4.5 Differential Forms

### 4.5.1

($i,j,k$ denotes any cyclic permutation of 1,2,3)

$$
\begin{aligned}
&*1=(1)(-1)^0dt\wedge dx_1\wedge dx_2\wedge dx_3=dt\wedge dx_1\wedge dx_2\wedge dx_3\\
&*dx_i=(-1)(-1)^1dt\wedge dx_j\wedge dx_k=dt\wedge dx_j\wedge dx_k\\
&*dt=(1)(-1)^0dx_1\wedge dx_2\wedge dx_3=dx_1\wedge dx_2\wedge dx_3\\
&*(dx_j\wedge dx_k)=(1)(-1)^2dt\wedge dx_i=dt\wedge dx_i\\
&*(dt\wedge dx_i)=(1)(-1)^1dx_j\wedge dx_k=-dx_j\wedge dx_k\\
&*(dx_1\wedge dx_2\wedge dx_3)=(-1)(-1)^3dt=dt\\
&*(dt\wedge dx_i\wedge dx_j)=(1)(-1)^2dx_k=dx_k\\
&*(dt\wedge dx_1\wedge dx_2\wedge dx_3)=(1)(-1)^3=-1
\end{aligned}
$$

------

### 4.5.2

Let the force field be $\V{F}=F_x\VE_x+F_y\VE_y+F_z\VE_z$, so the infinitely small work done is $dw=\V{F}\cdot d\V{r}=F_xdx+F_ydy+F_zdz$, and $w=F_x(x_2-x_1)+F_y(y_2-y_1)+F_z(z_2-z_1)$. Substituting, we get $F_x=\frac{a}{3}$, $F_y=\frac{b}{2}$, $F_z=c$. So

$$
\begin{aligned}
dw=\frac{a}{3}dx+\frac{b}{2}dy+cdz
\end{aligned}
$$

## 4.6 Differentiating Forms

### 4.6.1

(a) $d\omega_1=dx\wedge dy+dy\wedge dx=0$

(b) $d\omega_2=dx\wedge dy-dy\wedge dx=2dx\wedge dy$
 
(c) $d(d\omega_2)=2d(dx)\wedge dy-2dx\wedge d(dy)=0$

------

### 4.6.2

$$
\begin{aligned}
d\omega_3&=(ydx+xdy)\wedge dz+(zdx+xdz)\wedge dy-(zdy+ydz)\wedge dx=2zdx\wedge dy-2ydz\wedge dx\\
d(d\omega_3)&=2dz\wedge dx\wedge dy-2dy\wedge dz\wedge dx=0
\end{aligned}
$$

------

### 4.6.3

(a)

$$
\begin{aligned}
\omega_2\wedge\omega_3&=(x\,dy-y\,dx)\wedge(xy\,dz+xz\,dy-yz\,dx)=x^2y\,dy\wedge dz+xy^2\,dz\wedge dz\\
d(\omega_2\wedge\omega_3)&=2xy\,dx\wedge dy\wedge dz+2xy\,dy\wedge dz\wedge dx=4xy\,dx\wedge dy\wedge dz
\end{aligned}
$$

(b) 

$$
\begin{aligned}
d(\omega_2\wedge\omega_3)=(d\omega_2)\wedge\omega_3-\omega_2\wedge(d\omega_3)=2xy\,dx\wedge dy\wedge dz-(-2xy)\,dy\wedge dz\wedge dx=4xy\,dx\wedge dy\wedge dz
\end{aligned}
$$

## 4.7 Integrating Forms

### 4.7.1

$$
\begin{aligned}
&A(x,y,z)dx\wedge dy\wedge dz\\
=&A(u,v,w)(\pdv{x}{u}du+\pdv{x}{v}dv+\pdv{x}{w}dw)\wedge(\pdv{y}{u}du+\pdv{y}{v}dv+\pdv{y}{w}dw)\wedge(\pdv{z}{u}du+\pdv{z}{v}dv+\pdv{z}{w}dw)\\
=&A(u,v,w)\left[\pdv{x}{u}(\pdv{y}{v}\pdv{z}{w}-\pdv{y}{w}\pdv{z}{v})-\pdv{x}{v}(\pdv{y}{u}\pdv{z}{w}-\pdv{y}{w}\pdv{z}{u})+\pdv{x}{w}(\pdv{y}{u}\pdv{z}{v}-\pdv{y}{v}\pdv{z}{u}) \right]du\wedge dv\wedge dw\\
=&A(u,v,w)
\begin{vmatrix}
\pdv{x}{u}&\pdv{y}{u}&\pdv{z}{u}\\
\pdv{x}{v}&\pdv{y}{v}&\pdv{z}{v}\\
\pdv{x}{w}&\pdv{y}{w}&\pdv{z}{w}\\
\end{vmatrix}
du\wedge dv\wedge dw\\
=&A(u,v,w)\pdv{(x,y,z)}{(u,v,w)}du\wedge dv\wedge dw
\end{aligned}
$$

-----

### 4.7.2

$\int\limits_S\del\times\V{H}\cdot d\V{a}=kI=k\int\limits_S\V{J}\cdot d\V{a}$, where $\V{J}$ is the current density. In the differential form, the equation becomes

$$
\begin{aligned}
\left[\pdv{H_z}{y}-\pdv{H_y}{z}\right]dy\wedge dz+\left[\pdv{H_x}{z}-\pdv{H_z}{x}\right]dz\wedge dx+\left[\pdv{H_y}{x}-\pdv{H_x}{y}\right]dx\wedge dy=kJ_x\,dy\wedge dz+kJ_y\,dz\wedge dx+kJ_z\,dx\wedge dy
\end{aligned}
$$


the corresponding components of the two sides equal, respectively.

-----

### 4.7.3

If $\pdv{f}{x}=A$ and $\pdv{f}{y}=B$, then $\pdv{A}{y}=\pdv{^2f}{y\partial x}=\pdv{^2f}{x\partial y}=\pdv{B}{x}$, so being exact implies being closed.
If $\pdv{A}{y}=\pdv{B}{x}=\varphi(x,y)$, then $A=\int_{y_0}^y\varphi(x,y)dy+h(x)$ and $B=\int_{x_0}^x\varphi(x,y)dx+g(y)$. Let $f=\int_{x_0}^x\int_{y_0}^y\varphi(x,y)dxdy+\int_{x_0}^xh(x)dx+\int_{y_0}^yg(y)dy$, then $\pdv{f}{x}=\int_{y_0}^y\varphi(x,y)dy+h(x)=A$ and $\pdv{f}{y}=\int_{x_0}^x\varphi(x,y)dx+g(y)=B$, so being closed implies being exact. Therefore, being closed and being exact are sufficient and necessary conditions for each other.

To find the function $f$ for exact $Adx+Bdy$, let $f=\int_{x_0}^xA(x,y)dx+\int_{y_0}^yB(x_0,y)dy$, then $\pdv{f}{x}=A(x,y)$, and $\pdv{f}{y}=\int_{x_0}^x\pdv{A(x,y)}{y}dx+B(x_0,y)=\int_{x_0}^x\pdv{B(x,y)}{x}dx+B(x_0,y)=B(x,y)-B(x_0,y)+B(x_0,y)=B(x,y)$. So $f$ satisfy the condition.

(1)$\pdv{y}{y}=\pdv{x}{x}=1$, so $ydx+xdy$ is closed and exact. Let $x_0=y_0=0$, then 

$$
\begin{aligned}
f=\int_{x_0}^xydx+\int_{y_0}^yx_0dy=xy
\end{aligned}
$$

(2) $\pdv{}{y}(\frac{y}{x^2+y^2})\neq\pdv{}{x}(\frac{x}{x^2+y^2})$, so $\frac{ydx+xdy}{x^2+y^2}$ is neither closed nor exact.

(3) $\pdv{}{y}[\ln(xy)+1]=\pdv{}{x}(\frac{x}{y})=\frac{1}{y}$, so $[\ln(xy)+1]dx+\frac{x}{y}dy$ is closed and exact. Let $x_0=0$, then

$$
\begin{aligned}
f=\int_{x_0}^x[\ln(xy)+1]dx+\int_{y_0}^y\frac{x_0}{y}dy=x\ln(xy)
\end{aligned}
$$

(4) $\pdv{}{y}(\frac{-y}{x^2+y^2})=\pdv{}{x}(\frac{x}{x^2+y^2})=\frac{-x^2+y^2}{(x^2+y^2)^2}$, so $\frac{-y}{x^2+y^2}dx+\frac{x}{x^2+y^2}dy$ is closed and exact. Let $x_0=0$, then

$$
\begin{aligned}
f=\int_{x_0}^x\frac{-y}{x^2+y^2}dx+\int_{y_0}^y\frac{x_0}{{x_0}^2+y^2}dy=-\tan^{-1}\frac{x}{y}
\end{aligned}
$$

(5) $f(z)dx=(x+iy)dx+(-y+ix)dy$.\quad$\pdv{(x+iy)}{y}=\pdv{(-y+ix)}{x}=i$, so $(x+iy)dx+(-y+ix)dy$ is closed and exact. Let $x_0=y_0=0$, then

$$
\begin{aligned}
f=\int_{x_0}^x(x+iy)dx+\int_{y_0}^y(-y+ix_0)dy=\frac{x^2-y^2}{2}+ixy
\end{aligned}
$$

{% endraw %}
