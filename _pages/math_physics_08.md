---
layout: splash
title: "Mathematical Methods for Physicists Ch8"
permalink: /solutions/math_physics_08
author_profile: false

---

# Chapter 8 Sturm-Liouville Theory

{% raw %}

## 8.2 Hermitian Operators

### 8.2.1

When multiplied by $e^{-x}$, the Laguerre’s ODE becomes

$$
\newcommand{\pdv}[2]{\frac{\partial#1}{\partial#2}}
\newcommand{\V}{\mathbf}
\newcommand{\M}{\mathrm}
\newcommand{\VE}{\hat{\V{e}}}
\newcommand{\br}[2]{\langle#1|#2\rangle}
\begin{aligned}
e^{-x}xy''+e^{-x}(1-x)y'+e^{-x}ay=0
\end{aligned}
$$

Then $\frac{d}{dx}(e^{-x}x)=e^{-x}(1-x)$, so the ODE is self-adjoint if the boundary term $e^{-x}x\big[v^*u'-(v^*)'u\big]_a^b$ vanishes. 
The inner product becomes

$$
\begin{aligned}
\br{v}{u}=\int_a^bv^*(x)e^{-x}\mathcal{L}(x)u(x)dx=\int_a^b\big[v^*(x)\mathcal{L}(x)u(x)\big]e^{-x}dx
\end{aligned}
$$

which means the ODE will be self-adjoint if we let $e^{-x}$ be the weighting function.

-----

### 8.2.2

When multiplied by $e^{-x^2}$, the Hermite ODE becomes

$$
\begin{aligned}
e^{-x^2}y''-2xe^{-x^2}y'+2\alpha e^{-x^2}y=0
\end{aligned}
$$

Then $\frac{d}{dx}(e^{-x^2})=-2xe^{-x^2}$, so the ODE is self-adjoint if the boundary term $e^{-x^2}\big[v^*u'-(v^*)'u\big]_a^b$ vanishes. 
The inner product becomes

$$
\begin{aligned}
\br{v}{u}=\int_a^bv^*(x)e^{-x^2}\mathcal{L}(x)u(x)dx=\int_a^b\big[v^*(x)\mathcal{L}(x)u(x)\big]e^{-x^2}dx
\end{aligned}
$$

which means the ODE will be self-adjoint if we let $e^{-x^2}$ be the weighting function.

-----

### 8.2.3

When multiplied by $\frac{1}{\sqrt{1-x^2}}$, the Chebyshev ODE becomes

$$
\begin{aligned}
\sqrt{1-x^2}\,y''-\frac{x}{\sqrt{1-x^2}}y'+\frac{n^2}{\sqrt{1-x^2}}y=0
\end{aligned}
$$

Then $\frac{d}{dx}(\sqrt{1-x^2})=-\frac{x}{\sqrt{1-x^2}}$, so the ODE is self-adjoint if the boundary term $\sqrt{1-x^2}\big[v^*u'-(v^*)'u\big]_a^b$ vanishes. 
The inner product becomes 

$$
\begin{aligned}
\br{v}{u}=\int_a^bv^*(x)\frac{1}{\sqrt{1-x^2}}\mathcal{L}(x)u(x)dx=\int_a^b\big[v^*(x)\mathcal{L}(x)u(x)\big]\frac{1}{\sqrt{1-x^2}}dx
\end{aligned}
$$

which means the ODE will be self-adjoint if we let $\frac{1}{\sqrt{1-x^2}}$ be the weighting function.

-----

### 8.2.4

The boundary condition for $p_0(x)y''+p_1(x)y'+p_2(x)=0$ to be self-adjoint is

$$
\begin{aligned}
w(x)p_0(x)\big[v^*u'-(v^*)'u\big]_a^b=0
\end{aligned}
$$

for every $u,v$, with $w(x)$ being the weighting function.

$$
\begin{aligned}
    & \textit{Legendre:}\qquad &&  (1-x^2)\big[v^*u'-(v^*)'u\big]_{-1}^{1}=0 && \qquad \textit{because $1-x^2=0$ at $x=-1,1$}\\
    & \textit{Chebyshev:}\qquad &&  \sqrt{1-x^2}\big[v^*u'-(v^*)'u\big]_{-1}^{1}=0 && \qquad \textit{because $\sqrt{1-x^2}=0$ at $x=-1,1$}\\
    & \textit{Hermite:}\qquad &&  e^{-x^2}\big[v^*u'-(v^*)'u\big]_{-\infty}^{\infty}=0 && \qquad \textit{because $e^{-x^2}$ approach to zero faster than}\\
    & && &&\qquad \textit{polynomial $v^*u'-(v^*)'u$ at $-\infty,\infty$}\\
    & \textit{Laguerre:}\qquad &&  e^{-x}x\big[v^*u'-(v^*)'u\big]_{0}^{\infty}=0 && \qquad \textit{because $x=0$, and $e^{-x}$ approach to zero}\\
    & && &&\qquad \textit{faster than polynomial $x\big[v^*u'-(v^*)'u\big]$ at $\infty$}
\end{aligned}
$$

-----

### 8.2.5

The eigenvectors of an Hermitian operator with different eigenvalues are orthogonal (chapter 6) and therefore linearly independent (because if $au_1+bu_2=0$, then $\br{au_1+bu_2}{au_1+bu_2}=|a|^2\br{u_1}{u_1}+|b|^2\br{u_2}{u_2}=0$, which means $a=b=0$).

-----

### 8.2.6

(a) 
Let $u=\frac{1+x}{1-x}$, so $x=\frac{u-1}{u+1}$, $dx=\frac{2}{(u+1)^2}du$, and $u=0,\infty$ when $x=-1,1$. The integral becomes

$$
\begin{aligned}
\int_0^\infty\frac{1}{2}\frac{u-1}{u+1}(\ln u)\frac{2}{(u+1)^2}du
&=\int_0^\infty\frac{u-1}{(u+1)^3}\ln u\,du\\
&=\frac{-u}{(u+1)^2}\ln u\Big|_0^\infty-\int_0^\infty\frac{-u}{(u+1)^2}\frac{1}{u}du\\
&=\frac{-u}{(u+1)^2}\ln u\Big|_0^\infty-\frac{1}{u+1}\Big|_0^\infty\\
&=(0-0)-(0-1)=1
\end{aligned}
$$

(b) 
The boundary term

$$
\begin{aligned}
(1-x^2)\left[x\frac{1}{1-x^2}-\frac{1}{2}\ln\left(\frac{1+x}{1-x} \right) \right]_{-1}^1
\end{aligned}
$$

does not vanish (diverges), so the proof of the ODE being self-adjoint failed, and therefore the eigenfunctions are not necessarily orthogonal.

-----

### 8.2.7

The boundary term

$$
\begin{aligned}
\sqrt{1-x^2}\left[\frac{-x}{\sqrt{1-x^2}}-0 \right]_{-1}^1=-2
\end{aligned}
$$

does not vanish, so the proof of the ODE being self-adjoint failed, and therefore the eigenfunctions are not necessarily orthogonal.

-----

### 8.2.8

(We prove the case when $w(x)=1$ (or similarly a constant), while I'm not sure the correctness when $w(x)$ is a function of $x$. But if $w(x)$ is the weighting function, which means $\br{u_m}{u_n}=\int_a^bu_m^*u_nw\,dx$, then there is no problem in the following proof.)

We have $(pu_n')'=-\lambda_nwu_n$ from the equation, and $\br{u_m}{u_n}=\int_a^bu_m^*u_ndx=\delta_{mn}$ by the orthogonality.
Integrating $\br{u_m'}{u_n'}$ by parts:

$$
\begin{aligned}
\br{u_m'}{u_n'}&=\int_a^b(u_m')^*pu_n'dx\\
&=u_m^*pu_n'\big|_a^b-\int_a^bu_m^*(pu_n')'dx\\
&=u_m^*pu_n'\big|_a^b+\int_a^bu_m^*\lambda_nwu_ndx\\
&=u_m^*pu_n'\big|_a^b+\lambda_n\br{u_m}{u_n}=\lambda_n\delta_{mn}
\end{aligned}
$$

which means $u_m',u_n'$ are orthogonal, as long as the boundary condition $u_m^*pu_n'\big|_a^b=0$ is satisfied. \\(Or equivalently $(u_m^*)'pu_n\big|_a^b=0$, because we have $\big[u_m^*pu_n'-(u_m^*)'pu_n \big]_a^b=0$ from the boundary conditions making  $u_m,u_n$ orthogonal.)

-----

### 8.2.9

Assume linear dependence, so $\varphi_n=\sum_{i=1}^{n-1}a_i\varphi_i$, then

$$
\begin{aligned}
A\varphi_n=\lambda_n\varphi_n=\sum_{i=1}^{n-1}\lambda_na_i\varphi_i
\end{aligned}
$$

and also

$$
\begin{aligned}
A\varphi_n=A(\sum_{i=1}^{n-1}a_i\varphi_i)=\sum_{i=1}^{n-1}a_i\lambda_i\varphi_i
\end{aligned}
$$

so

$$
\begin{aligned}
\sum_{i=1}^{n-1}a_i(\lambda_n-\lambda_i)\varphi_i=0
\end{aligned}
$$

Note that $\lambda_n-\lambda_1\neq0$, so the equation implies $\varphi_1,\cdots,\varphi_{n-1}$ are linearly dependent. Therefore, the linear dependence between $\varphi_1,\cdots,\varphi_n$ implies the linear dependence between $\varphi_1,\cdots,\varphi_{n-1}$, and by repeating the process, we will find $\varphi_1,\varphi_2$ being linearly dependent, which is impossible because it implies $\lambda_1=\lambda_2$ ($\lambda_2\varphi_2=A\varphi_2=Ak\varphi_1=\lambda_1k\varphi_1=\lambda_1\varphi_2$). So $\varphi_1,\cdots,\varphi_n$ must be linearly independent.

-----

### 8.2.10

(a)
Using Eq 8.15, the ODE will be self-adjoint if multiplied by

$$
\begin{aligned}
\frac{1}{1-x^2}e^{\int\frac{-(2\alpha
+1)x}{1-x^2}dx}=\frac{1}{1-x^2}e^{(\alpha+\frac{1}{2})\ln(1-x^2)}=(1-x^2)^{\alpha-\frac{1}{2}}
\end{aligned}
$$

so the ODE becomes

$$
\begin{aligned}
\left\{(1-x^2)^{\alpha+\frac{1}{2}}\frac{d^2}{dx^2}-(2\alpha+1)x(1-x^2)^{\alpha-\frac{1}{2}}\frac{d}{dx}+n(n+2\alpha)(1-x^2)^{\alpha-\frac{1}{2}} \right\}C_n^{(\alpha)}(x)=0
\end{aligned}
$$

which is self-adjoint because 

$$
\begin{aligned}
\frac{d}{dx}(1-x^2)^{\alpha+\frac{1}{2}}=-(2\alpha+1)x(1-x^2)^{\alpha-\frac{1}{2}}
\end{aligned}
$$

(b)
The boundary conditions will be satisfied if we choose the interval to be $[-1,1]$:

$$
\begin{aligned}
(1-x^2)^{\alpha+\frac{1}{2}}\big[v^*u'-(v^*)'u \big]_{-1}^1=0
\end{aligned}
$$

so the eigenfunctions of different eigenvalues will be orthogonal if the inner product is defined as

$$
\begin{aligned}
\br{C_m}{C_n}=\int_{-1}^1C_m^*C_n(1-x^2)^{\alpha-\frac{1}{2}}\,dx
\end{aligned}
$$

## 8.3 ODE Eigenvalue Problems

### 8.3.1

Let $y=\sum_{j=0}^\infty a_jx^{s+j}$ and substitute:

$$
\begin{aligned}
(1-x^2)\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}-2x\sum_{j=0}^\infty a_j(s+j)x^{s+j-1}+n(n+1)\sum_{j=0}^\infty a_j x^{s+j}=0
\end{aligned}
$$

The coefficients of each order must be zero, so

$$
\begin{aligned}
    & x^{s-2}:\qquad && a_0s(s-1)=0\\
    & x^{s-1}:\qquad && a_1(s+1)s=0\\
    & x^{s+j}:\qquad && a_{j+2}(s+j+2)(s+j+1)-a_j(s+j)(s+j-1)-2a_j(s+j)+n(n+1)a_j=0\\
    & && a_{j+2}=\frac{(s+j)(s+j+1)-n(n+1)}{(s+j+1)(s+j+2)}a_j
\end{aligned}
$$

(a)
$a_0\neq0$, so $s(s-1)=0$.

(b)
Let $s=0$ and $a_1=0$ (so $a_3,a_5,\cdots$ vanish), then

$$
\begin{aligned}
a_{j+2}&=\frac{j(j+1)-n(n+1)}{(j+1)(j+2)}a_j=\frac{(j-n)(j+n+1)}{(j+1)(j+2)}a_j\\
y_{even}&=\sum_{j\; even}a_jx^j=a_0\left[1-\frac{n(n+1)}{2!}x^2+\frac{(n-2)n(n+1)(n+3)}{4!}x^4-\cdots \right]
\end{aligned}
$$

(c) 
Let $s=1$, then $a_1(s+1)s=0$ implies $a_1=0$, and

$$
\begin{aligned}
a_{j+2}&=\frac{(j+1)(j+2)-n(n+1)}{(j+2)(j+3)}a_j=\frac{(j+1-n)(j+2+n)}{(j+2)(j+3)}a_j\\
y_{odd}&=\sum_{j\;even}a_jx^{1+j}=a_0\left[x-\frac{(n-1)(n+2)}{3!}x^3+\frac{(n-3)(n-1)(n+2)(n+4)}{5!}x^5-\cdots \right]
\end{aligned}
$$

(d)
For $y_{even}$, let $u_k=a_{2k}$, so

$$
\begin{aligned}
u_{k+1}=\frac{2k(2k+1)-n(n+1)}{(2k+1)(2k+2)}u_k
\end{aligned}
$$

then the series at $x=\pm 1$ becomes

$$
\begin{aligned}
y_{even}=\sum_{j\;even}a_jx^j=\sum_{k=0}^\infty u_k(x^2)^k=\sum_{k=0}^\infty u_k
\end{aligned}
$$

and

$$
\begin{aligned}
\frac{u_k}{u_{k+1}}=\frac{(2k+1)(2k+2)}{2k(2k+1)-n(n+1)}=1+\frac{1}{k}+\frac{B(k)}{k^2}
\end{aligned}
$$

where $B(k)$ is bounded for large $k$, so by Gauss' test the series diverge.

Similarly, for $y_{odd}$, let $u_k=a_{2k}$, so

$$
\begin{aligned}
u_{k+1}=\frac{(2k+1)(2k+2)-n(n+1)}{(2k+2)(2k+3)}u_k
\end{aligned}
$$

then the series at $x=\pm 1$ becomes

$$
\begin{aligned}
y_{odd}=\sum_{j\;even}a_jx^{1+j}=\sum_{k=0}^\infty xu_k(x^2)^k=\pm\sum_{k=0}^\infty u_k
\end{aligned}
$$

and

$$
\begin{aligned}
\frac{u_k}{u_{k+1}}=\frac{(2k+2)(2k+3)}{(2k+1)(2k+2)-n(n+1)}=1+\frac{1}{k}+\frac{B(k)}{k^2}
\end{aligned}
$$

where $B(k)$ is bounded for large $k$, so by Gauss' test the series diverge.

(e)
From the recurrence relations of $y_{even}$ and $y_{odd}$, if $n$ is a non-negative even integer, then $y_{even}$ will terminate at $a_nx^n$; if $n$ is a non-negative odd integer, then $y_{odd}$ will terminate at $a_{n-1}x^n$. So the series are converted into finite polynomials.

-----

### 8.3.2

When multiplied by $e^{-x^2}$, the equation becomes

$$
\begin{aligned}
e^{-x^2}y''-2xe^{-x^2}y'+2\alpha e^{-x^2}y=0
\end{aligned}
$$

so

$$
\begin{aligned}
\frac{d}{dx}\big[e^{-x^2}\big]=-2xe^{-x^2}
\end{aligned}
$$

and 

$$
\begin{aligned}
e^{-x^2}\big[v^*u'-(v^*)'u \big]_{-\infty}^\infty=0
\end{aligned}
$$

which means the ODE is self-adjoint (Hermitian).

-----

### 8.3.3

Let $y=\sum_{j=0}^\infty a_jx^{s+j}$ and substitute:

$$
\begin{aligned}
\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}-2x\sum_{j=0}^\infty a_j(s+j)x^{s+j-1}+2\alpha\sum_{j=0}^\infty a_j x^{s+j}=0
\end{aligned}
$$

The coefficients of each order must be zero, so

$$
\begin{aligned}
    & x^{s-2}:\qquad && a_0s(s-1)=0\\
    & x^{s-1}:\qquad && a_1(s+1)s=0\\
    & x^{s+j}:\qquad && a_{j+2}(s+j+2)(s+j+1)-2a_j(s+j)+2\alpha a_j=0 \\
    & && a_{j+2}=a_j\frac{2(s+j-\alpha)}{(s+j+1)(s+j+2)}
\end{aligned}
$$

(a)
$s=0$:

$$
\begin{aligned}
a_{j+2}&=a_j\frac{2(j-\alpha)}{(j+1)(j+2)}\\
y_{even}&=\sum_{j\;even}a_jx^j=a_0\left[1+\frac{2(-\alpha)}{2!}x^2+\frac{2^2(-\alpha)(2-\alpha)}{4!}x^4+\cdots \right]
\end{aligned}
$$

$s=1$:

$$
\begin{aligned}
a_{j+2}&=a_j\frac{2(j+1-\alpha)}{(j+2)(j+3)}\\
y_{odd}&=\sum_{j\;even}a_jx^{1+j}=a_0\left[x+\frac{2(1-\alpha)}{3!}x^3+\frac{2^2(1-\alpha)(3-\alpha)}{5!}x^5+\cdots \right]
\end{aligned}
$$

(b)
For $y_{even}$, let $u_k=a_{2k}$, then

$$
\begin{aligned}
u_{k+1}&=u_k\frac{2(2k-\alpha)}{(2k+1)(2k+2)}\\
\lim_{k\to\infty}\frac{a_{2k+2}x^{2k+2}}{a_{2k}x^{2k}}&=\lim_{k\to\infty}\frac{u_{k+1}}{u_k}x^2=\lim_{k\to\infty}\frac{4x^2k-2x^2\alpha}{4k^2+6k+2}=\lim_{k\to\infty}\frac{x^2}{k}=0
\end{aligned}
$$

so by ratio test the series converge.

Similarly, for $y_{odd}$, let $u_k=a_{2k}$, then

$$
\begin{aligned}
u_{k+1}&=u_k\frac{2(2k+1-\alpha)}{(2k+2)(2k+3)}\\
\lim_{k\to\infty}\frac{a_{2k+2}x^{2k+3}}{a_{2k}x^{2k+1}}&=\lim_{k\to\infty}\frac{u_{k+1}}{u_k}x^2=\lim_{k\to\infty}\frac{4x^2k+2x^2(1-\alpha)}{4k^2+10k+6}=\lim_{k\to\infty}\frac{x^2}{k}=0
\end{aligned}
$$

so by ratio test the series converge.

$e^{x^2}=\sum_{k=0}^\infty\frac{x^{2k}}{k!}$, so the ratio of seccessive terms is

$$
\begin{aligned}
\lim_{k\to\infty}\frac{x^{2(k+1)}}{(k+1)!}\frac{k!}{x^{2k}}=\lim_{k\to\infty}\frac{x^2}{k+1}=\lim_{k\to\infty}\frac{x^2}{k}
\end{aligned}
$$

which is the same as the ratios of seccessive terms of $y_{even}$ and $y_{odd}$.

(c)
From the recurrence relations of $y_{even}$ and $y_{odd}$, if $\alpha$ is a non-negative even integer, then $y_{even}$ will terminate at $a_{\alpha}x^{\alpha}$; if $n$ is a non-negative odd integer, then $y_{odd}$ will terminate at $a_{\alpha-1}x^{\alpha}$. So the series are converted into finite polynomials.

-----

### 8.3.4

Let $L_n(x)=\sum_{j=0}^\infty a_jx^{s+j}$ and substitute:

$$
\begin{aligned}
x\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}+(1-x)\sum_{j=0}^\infty a_j(s+j)x^{s+j-1}+n\sum_{j=0}^\infty a_jx^{s+j}=0
\end{aligned}
$$

The coefficients of each order must be zero, so

$$
\begin{aligned}
    & x^{s-1}:\qquad && a_0s(s-1)+a_0s=a_0s^2=0\qquad && s=0\\
    & x^{s+j}:\qquad && a_{j+1}(j+1)j+a_{j+1}(j+1)-a_jj+na_j=0\qquad\qquad && a_{j+1}=a_j\frac{j-n}{(j+1)^2}
\end{aligned}
$$

so

$$
\begin{aligned}
y=\sum_{j=0}^\infty a_jx^j=a_0\left[1+\frac{(-n)}{1^2}x+\frac{(-n)(1-n)}{1^2\cdot2^2}x^2+\cdots \right]
\end{aligned}
$$

From the recurrence relation of $y$, if $n$ is a non-negative integer, then $y$ will terminate at $a_{n}x^{n}$, and the series will be converted into a finite polynomial.

-----

### 8.3.5

Let $T_n=\sum_{j=0}^\infty a_jx^{s+j}$ and substitute:

$$
\begin{aligned}
(1-x^2)\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}-x\sum_{j=0}^\infty a_j(s+j)x^{s+j-1}+n^2\sum_{j=0}^\infty a_jx^{s+j}=0
\end{aligned}
$$

The coefficients of each order must be zero, so

$$
\begin{aligned}
    & x^{s-2}:\qquad && a_0s(s-1)=0\\
    & x^{s-1}:\qquad && a_1(s+1)s=0\\
    & x^{s+j}:\qquad && a_{j+2}(s+j+2)(s+j+1)-a_j(s+j)(s+j-1)-a_j(s+j)+n^2a_j=0\\
    & && a_{j+2}=a_j\frac{(s+j-n)(s+j+n)}{(s+j+1)(s+j+2)}
\end{aligned}
$$

For $s=0$, let $a_1=0$, then

$$
\begin{aligned}
a_{j+2}&=a_j\frac{(j-n)(j+n)}{(j+1)(j+2)}\\
y_{even}&=\sum_{j\;even}a_jx^j=a_0\left[1+\frac{(-n)n}{2!}x^2+\frac{(2-n)(-n)n(2+n)}{4!}x^4+\cdots \right]
\end{aligned}
$$

For $s=1$, $a_1=0$, and

$$
\begin{aligned}
a_{j+2}=a_j\frac{(j+1-n)(j+1+n)}{(j+2)(j+3)}\\
y_{odd}=\sum_{j\;even}a_jx^{1+j}=a_0\left[x+\frac{(1-n)(1+n)}{3!}x^3+\frac{(3-n)(1-n)(1+n)(3+n)}{5!}x^5+\cdots \right]
\end{aligned}
$$

To test the convergence at $x=\pm1$, let $u_k=a_{2k}$:

$y_{even}:$

$$
\begin{aligned}
u_{k+1}&=u_k\frac{(2k-n)(2k+n)}{(2k+1)(2k+2)}\\
y_{even}&=\sum_{j\;even}a_jx^j=\sum_{k=0}^\infty u_k(x^2)^k=\sum_{k=0}^\infty u_k\\
\frac{u_k}{u_{k+1}}&=\frac{4k^2+6k+2}{4k^2-n^2}=1+\frac{3}{2k}+\frac{B(k)}{k^2}
\end{aligned}
$$

so $y_{even}$ converges at $x=\pm1$ by Gauss' test.

$y_{odd}:$

$$
\begin{aligned}
u_{k+1}&=u_k\frac{(2k+1-n)(2k+1+n)}{(2k+2)(2k+3)}\\
y_{odd}&=\sum_{j\;even}a_jx^{1+j}=\sum_{k=0}^\infty xu_k(x^2)^k=\pm\sum_{k=0}^\infty u_k\\
\frac{u_k}{u_{k+1}}&=\frac{4k^2+10k+6}{4k^2+4k+1-n^2}=1+\frac{3}{2k}+\frac{B(k)}{k^2}
\end{aligned}
$$

so $y_{odd}$ converges at $x=\pm1$ by Gauss' test.

-----

### 8.3.6

Let $U_n=\sum_{j=0}^\infty a_jx^{s+j}$ and substitute:

$$
\begin{aligned}
(1-x^2)\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}-3x\sum_{j=0}^\infty a_j(s+j)x^{s+j-1}+n(n+2)\sum_{j=0}^\infty a_jx^{s+j}=0
\end{aligned}
$$

The coefficients of each order must be zero, so

$$
\begin{aligned}
    & x^{s-2}:\qquad && a_0s(s-1)=0\\
    & x^{s-1}:\qquad && a_1(s+1)s=0\\
    & x^{s+j}:\qquad && a_{j+2}(s+j+2)(s+j+1)-a_j(s+j)(s+j-1)-3a_j(s+j)+n(n+2)a_j=0\\
    & && a_{j+2}=a_j\frac{(s+j)(s+j+2)-n(n+2)}{(s+j+1)(s+j+2)}=a_j\frac{(s+j-n)(s+j+n+2)}{(s+j+1)(s+j+2)}
\end{aligned}
$$

Choose $s=1$, then $a_1=0$, and

$$
\begin{aligned}
y_{odd}=\sum_{j\;even}a_jx^{1+j}=a_0\left[x+\frac{(1-n)(3+n)}{3!}x^3+\frac{(3-n)(1-n)(3+n)(5+n)}{5!}x^5+\cdots \right]
\end{aligned}
$$

From the recurrence relation, if $n$ is a positive odd integer, then $y_{odd}$ will terminate at $a_{n-1}x^{n}$, and the series will be converted into a finite polynomial.

## 8.4 Variation Method

### 8.4.1

(a)

$$
\begin{aligned}
\br{\varphi}{\varphi}=\int_0^\infty4\alpha^3x^2e^{-2\alpha x}dx=4\alpha^3\left[2\frac{e^{-2\alpha x}}{(-2\alpha)^3} \right]_0^\infty=1
\end{aligned}
$$

(b)

$$
\begin{aligned}
\langle x^{-1}\rangle=\int_0^\infty 4\alpha^3xe^{-2\alpha x}dx=4\alpha^3\left[-\frac{e^{-2\alpha x}}{(-2\alpha)^2} \right]_0^\infty=\alpha
\end{aligned}
$$

(c)

$$
\begin{aligned}
\langle\frac{d^2}{dx^2}\rangle&=\int_0^\infty4\alpha^3xe^{-\alpha x}\frac{d^2}{dx^2}(xe^{-\alpha x})dx\\
&=4\alpha^5\int_0^\infty x^2e^{-2\alpha x}dx-8\alpha^4\int_0^\infty xe^{-2\alpha x}dx\\
&=4\alpha^5\left[2\frac{e^{-2\alpha x}}{(-2\alpha)^3} \right]_0^\infty-8\alpha^4\left[-\frac{e^{-2\alpha x}}{(-2\alpha)^2} \right]_0^\infty\\
&=\alpha^2-2\alpha^2=-\alpha^2
\end{aligned}
$$

(d)

$$
\begin{aligned}
\left\langle\varphi\left|-\frac{1}{2}\frac{d^2}{dx^2}-\frac{1}{x} \right|\varphi \right\rangle&=\frac{\alpha^2}{2}-\alpha\\
\frac{d}{d\alpha}\left[\frac{\alpha^2}{2}-\alpha\right]&=\alpha-1=0
\end{aligned}
$$

so

$$
\begin{aligned}
\alpha=1
\end{aligned}
$$

and the minimum value of the expectation value is

$$
\begin{aligned}
\left[\frac{\alpha^2}{2}-\alpha\right]_{\alpha=1}=-\frac{1}{2}
\end{aligned}
$$

{% endraw %}
