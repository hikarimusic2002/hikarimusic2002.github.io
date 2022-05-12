---
layout: splash
title: "Mathematical Methods for Physicists Ch13"
permalink: /solutions/math_physics_13
author_profile: false

---

# Chapter 13: Gamma Function

{% raw %}

## 13.1 Definitions, Properties

### 13.1.1

$$
\newcommand{\pdv}[2]{\frac{\partial#1}{\partial#2}}
\newcommand{\V}{\mathbf}
\newcommand{\abs}[1]{\left\vert #1\right\vert}
\newcommand{\lfpr}[1]{\left(#1\right)}
\newcommand{\lfbr}[1]{\left[#1\right]}
\newcommand{\lfab}[1]{\left|#1\right|}
\newcommand{\brke}[1]{\langle#1\rangle}
\begin{aligned}
\Gamma(z+1)=\int\limits_0^\infty e^{-t}t^zdt=-\lfbr{e^{-t}t^z }_0^\infty-\int\limits_0^\infty-e^{-t}\cdot z\,t^{z-1}dt=z\int\limits_0^\infty e^{-t}t^{z-1}dt=z\Gamma(z)
\end{aligned}
$$

-----

### 13.1.2

(a)
The expression is equal to

$$
\begin{aligned}
\frac{\frac{(n+2s)!}{n!}}{(2s)!!\cdot\frac{(2n+2s+1)!!}{(2n+1)!!}}=\frac{\frac{(n+2s)!}{n!}}{2^s\cdot s!\cdot\frac{(2n+2s+1)!}{2^{n+s}(n+s)!}\frac{2^n\cdot n!}{(2n+1)!}}=\frac{(n+s)!(n+2s)!(2n+1)!}{s!n!n!(2n+2s+1)!}
\end{aligned}
$$

(b)

$$
\begin{aligned}
\frac{(n+s)!(n+2s)!(2n+1)!}{s!n!n!(2n+2s+1)!}=\frac{(s+n)!}{s!}\frac{(n+2s)!}{n!}\frac{(2n+1)!}{(2n+2s+1)!}\frac{1}{n!}=\frac{(s+1)_n(n+1)_{2s}}{(2n+2)_{2s}(1)_n}
\end{aligned}
$$

-----

### 13.1.3

$$
\begin{aligned}
\Gamma(z)=\int\limits_0^\infty e^{-s}s^{z-1}ds
\end{aligned}
$$

Use the substitution $s=t^2$, $ds=2t\,dt$, we have

$$
\begin{aligned}
\Gamma(z)=\int\limits_0^\infty e^{-t^2}t^{2(z-1)}\cdot2t\,dt=2\int\limits_0^\infty e^{-t^2}t^{2z-1}dt
\end{aligned}
$$

Use the substitution $e^{-s}=t$, $-e^{-s}ds=dt$, we have

$$
\begin{aligned}
\Gamma(z)=\int\limits_1^0 t\lfbr{\ln\lfpr{\frac{1}{t}} }^{z-1}\lfpr{-\frac{dt}{t} }=\int\limits_0^1\lfbr{\ln\lfpr{\frac{1}{t}} }^{z-1}dt
\end{aligned}
$$

-----

### 13.1.4

Using the substitution $t=\frac{mv^2}{2kT}$, so $v=\lfpr{\frac{2kT}{m}}^{\frac{1}{2}}t^{\frac{1}{2}}$, $dv=\frac{1}{2}\lfpr{\frac{2kT}{m}}^{\frac{1}{2}}t^{-\frac{1}{2}}dt$, then

$$
\begin{aligned}
        \langle v^n\rangle & =\frac{\int_0^\infty v^ndN}{N}\\
        & =\int_0^\infty4\pi\lfpr{\frac{m}{2\pi kT}}^{\frac{3}{2}}e^{-\frac{mv^2}{2kT}}v^{n+2}dv\\
        & =\int_0^\infty4\pi^{-\frac{1}{2}}\lfpr{\frac{2kT}{m}}^{-\frac{3}{2}}e^{-t}\lfpr{\frac{2kT}{m}}^{\frac{n+2}{2}}t^{\frac{n+2}{2}}\cdot\frac{1}{2}\lfpr{\frac{2kT}{m}}^{\frac{1}{2}}t^{-\frac{1}{2}}dt\\
        & =\lfpr{\frac{2kT}{m}}^{\frac{n}{2}}\frac{1}{\sqrt{\pi}\cdot\frac{1}{2}}\int_0^\infty e^{-t}t^{\frac{n+1}{2}}dt\\
        & =\lfpr{\frac{2kT}{m}}^{\frac{n}{2}}\frac{\Gamma\lfpr{\frac{n+3}{2}}}{\Gamma\lfpr{\frac{3}{2}}}
\end{aligned}
$$

-----

### 13.1.5

$$
\begin{aligned}
-\int\limits_0^1 x^k\ln x\,dx=-\int\limits_{\infty}^0e^{-kt}(-t)(-e^{-t}dt)=\int\limits_0^\infty e^{-(k+1)t}t\,dt=\frac{1}{(k+1)^2}\int\limits_0^\infty e^{-s}s\,ds=\frac{\Gamma(2)}{(k+1)^2}=\frac{1}{(k+1)^2}
\end{aligned}
$$

where we use the substitution $x=e^{-t}$ and $(k+1)t=s$.

-----

### 13.1.6

$$
\begin{aligned}
\int\limits_0^\infty e^{-x^4}dx=\int\limits_0^\infty e^{-t}\cdot\frac{1}{4}t^{-\frac{3}{4}}dt=\frac{1}{4}\Gamma\lfpr{\frac{1}{4}}=\Gamma\lfpr{\frac{5}{4}}
\end{aligned}
$$

where we use the substitution $x=t^{\frac{1}{4}}$.

-----

### 13.1.7

$$
\begin{aligned}
\lim_{x\to0}\frac{\Gamma(ax)}{\Gamma(x)}=\lim_{x\to0}\frac{\frac{1}{ax}\Gamma(ax+1)}{\frac{1}{x}\Gamma(x+1)}=\frac{1}{a}
\end{aligned}
$$

-----

### 13.1.8

From Equation 13.1, $\Gamma(z)$ has simple poles at every non-negative integer $z=-N$. Note that $\Gamma(z+N)=(z+N-1)\cdots(z)\Gamma(z)$, so the residue at $z=-N$ is

$$
\begin{aligned}
residue=\lim_{z\to-N}(z+N)\cdot\Gamma(z)=\lim_{z\to-N}(z+N)\cdot\frac{\Gamma(z+N)}{(z+N-1)\cdots(z)}=\lim_{z\to-N}\frac{\Gamma(z+N+1)}{(-1)\cdots(-N)}=\frac{(-1)^N}{N!}
\end{aligned}
$$

-----

### 13.1.9

As is Figure 13.1, $\Gamma(x)$ is a continuous function on the segment $x\in(-N,-N+1)$ where $N\in\mathbb{N}$. For even $N$,\; $\Gamma(x)$ ranges from $\Gamma(-N+\frac{1}{2})$ to $+\infty$, and for odd $N$, $\Gamma(x)$ ranges from $-\infty$ to $\Gamma(-N+\frac{1}{2})$. Therefore, if we prove that $\Gamma(-N+\frac{1}{2})\to0$ as $N\to\infty$, then for every $k\neq0$, there are infinite many segments $(-N,-N+1)$ in which $y=\Gamma(x)$ intersects with $y=k$.

From Equation 13.23, we have

$$
\begin{aligned}
\Gamma\lfpr{-N+\frac{1}{2}}\Gamma\lfpr{N+\frac{1}{2}}=\frac{\pi}{\sin\lfpr{-N+\frac{1}{2}}}=(-1)^N\pi
\end{aligned}
$$

Note that 

$$
\begin{aligned}
\lim_{N\to\infty}\left|\Gamma\lfpr{N+\frac{1}{2}} \right|=\infty
\end{aligned}
$$

so 

$$
\begin{aligned}
\lim_{N\to\infty}\Gamma\lfpr{-N+\frac{1}{2}}=0
\end{aligned}
$$

from which we proved the problem.

-----

### 13.1.10

(a)
Use the substitution $x=\sqrt{\frac{t}{a}}$,

$$
\begin{aligned}
\int\limits_0^\infty x^{2s+1}e^{-ax^2}dx=\int\limits_0^\infty \lfpr{\frac{t}{a}}^{\frac{2s+1}{2}}e^{-t}\frac{dt}{2\sqrt{at}}=\frac{\int_0^\infty e^{-t}t^sdt}{2a^{s+1}}=\frac{s!}{2a^{s+1}}
\end{aligned}
$$

(b)
Use the substitution $x=\sqrt{\frac{t}{a}}$,

$$
\begin{aligned}
\int\limits_0^\infty x^{2s}e^{-ax^2}dx=\int\limits_0^\infty \lfpr{\frac{t}{a}}^se^{-t}\frac{dt}{2\sqrt{at}}=\frac{\int_0^\infty e^{-t}t^{s-\frac{1}{2}}dt}{2a^{s+\frac{1}{2}}}=\frac{\Gamma(s+\frac{1}{2})}{2a^{s+\frac{1}{2}}}=\frac{\frac{(2s-1)!!}{2^s}\Gamma(\frac{1}{2})}{2a^{s+\frac{1}{2}}}=\frac{(2s-1)!!}{2^{s+1}a^s}\sqrt{\frac{\pi}{a}}
\end{aligned}
$$

-----

### 13.1.11

By the binomial theorem:

$$
\begin{aligned}
(1+x)^{\frac{1}{2}}=\sum_{n=0}^\infty\binom{\frac{1}{2}}{n}x^n=\sum_{n=0}^\infty a_nx^n
\end{aligned}
$$

(b)

$$
\begin{aligned}
a_n=\binom{\frac{1}{2}}{n}=\frac{(\frac{1}{2})(-\frac{1}{2})\cdots(-\frac{2n-3}{2})}{n(n-1)\cdots1}=(-1)^{n+1}\frac{(2n-3)!!}{2^nn!}=(-1)^{n+1}\frac{(2n-3)!!}{(2n)!!}
\end{aligned}
$$

(a)

$$
\begin{aligned}
a_n=(-1)^{n+1}\frac{(2n-3)!!}{2^nn!}=(-1)^{n+1}\frac{\frac{(2n-3)!}{(2n-4)!!}}{2^nn!}=(-1)^{n+1}\frac{\frac{(2n-3)!}{2^{n-2}(n-2)!}}{2^nn!}=(-1)^{n+1}\frac{(2n-3)!}{2^{2n-2}n!(n-2)!}
\end{aligned}
$$

-----

### 13.1.12

By the binomial theorem:

$$
\begin{aligned}
(1+x)^{-\frac{1}{2}}=\sum_{n=0}^\infty\binom{-\frac{1}{2}}{n}x^n=\sum_{n=0}^\infty a_nx^n
\end{aligned}
$$

(b)

$$
\begin{aligned}
a_n=\binom{-\frac{1}{2}}{n}=\frac{(-\frac{1}{2})(-\frac{3}{2})\cdots(-\frac{2n-1}{2})}{n(n-1)\cdots1}=(-1)^n\frac{(2n-1)!!}{2^nn!}=(-1)^n\frac{(2n-1)!!}{(2n)!!}
\end{aligned}
$$

(a)

$$
\begin{aligned}
a_n=(-1)^n\frac{(2n-1)!!}{2^nn!}=(-1)^n\frac{\frac{(2n)!}{(2n)!!}}{2^nn!}=(-1)^n\frac{\frac{(2n)!}{2^nn!}}{2^nn!}=(-1)^n\frac{(2n)!}{2^{2n}(n!)^2}
\end{aligned}
$$

-----

### 13.1.13

The $(p+1)^{th}$ term counted from the front is

$$
\begin{aligned}
        & \quad\;2\frac{(2n-1)!!}{(2n)!!}\frac{1\cdot3\cdots(2p-1)}{1\cdot2\cdots p}\frac{n(n-1)\cdots(n-p+1)}{(2n-1)(2n-3)\cdots(2n-2p+1)}\cos(n-2p)\theta\\
        & =2\frac{(2n-1)!!}{(2n)!!}\frac{(2p-1)!!}{p!}\frac{\frac{n!}{(n-p)!}}{\frac{(2n-1)!!}{(2n-2p-1)!!}}\cos(n-2p)\theta\\
        & =\frac{(2p-1)!!(2n-2p-1)!!}{2^{n-1}p!(n-p)!}\cos(n-2p)\theta
\end{aligned}
$$

Use the substitution $n=2s+1$ and $p=s-m$, we have

$$
\begin{aligned}
a_m\cos(2m+1)\theta=\frac{(2s-2m-1)!!(2s+2m+1)!!}{2^{2s}(s-m)!(s+m+1)!}\cos(2m+1)\theta
\end{aligned}
$$

-----

### 13.1.14

(a)
From Equation 13.23,

$$
\begin{aligned}
\Gamma\lfpr{\frac{1}{2}-n}\Gamma\lfpr{\frac{1}{2}+n}=\frac{\pi}{\sin\pi(\frac{1}{2}-n)}=(-1)^n\pi
\end{aligned}
$$

(b)

$$
\begin{aligned}
\Gamma\lfpr{\frac{1}{2}+n}&=\lfpr{\frac{2n-1}{2}}\lfpr{\frac{2n-3}{2}}\cdots\lfpr{\frac{1}{2}}\Gamma\lfpr{\frac{1}{2}}=\frac{(2n-1)!!}{2^n}\pi^{\frac{1}{2}}\\
\Gamma\lfpr{\frac{1}{2}}&=\lfpr{-\frac{1}{2}}\lfpr{-\frac{3}{2}}\cdots\lfpr{-\frac{2n-1}{2}}\Gamma\lfpr{\frac{1}{2}-n}=(-1)^n\frac{(2n-1)!!}{2^n}\Gamma\lfpr{\frac{1}{2}-n}
\end{aligned}
$$

so

$$
\begin{aligned}
\Gamma\lfpr{\frac{1}{2}-n}=(-1)^n\frac{2^n}{(2n-1)!!}\pi^{\frac{1}{2}}
\end{aligned}
$$

It can be verified that $\Gamma(\frac{1}{2}+n)\Gamma(\frac{1}{2}-n)=(-1)^n\pi$.

-----

### 13.1.15

$$
\begin{aligned}
\Gamma(z^*)=\int\limits_0^\infty e^{-t}t^{z^*-1}dt=\int\limits_0^\infty e^{-t}t^{[z-1]^*}dt =\lfbr{\int\limits_0^\infty e^{-t}t^{z-1}dt }^*=\lfbr{\Gamma(z) }^*
\end{aligned}
$$

-----

### 13.1.16

From Equation 13.15,

$$
\begin{aligned}
        \frac{1}{\lfab{\Gamma(\alpha+i\beta)}} & =\lfab{\alpha+i\beta}\cdot\lfab{e^{\gamma(\alpha+i\beta)}}\cdot\prod_{n=1}^\infty\lfab{1+\frac{\alpha+i\beta}{n}}\cdot\lfab{e^{-\frac{\alpha+i\beta}{n}}}\\
        & =\sqrt{\alpha^2+\beta^2}e^{\gamma\alpha}\prod_{n=1}^\infty\sqrt{(1+\frac{\alpha}{n})^2+(\frac{\beta}{n})^2}\cdot e^{-\frac{\alpha}{n}}\\
        & =\lfbr{\sqrt{1+\frac{\beta^2}{\alpha^2}}\prod_{n=1}^\infty\sqrt{1+\frac{\beta^2}{(\alpha+n)^2}}}\lfbr{\alpha e^{\gamma\alpha}\prod_{n=1}^\infty\lfpr{1+\frac{\alpha}{n}}e^{-\frac{\alpha}{n}}}\\
        & =\lfbr{\prod_{n=0}^\infty\sqrt{1+\frac{\beta^2}{(\alpha+n)^2}}\, }\frac{1}{\lfab{\Gamma(\alpha)}}
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
\lfab{\Gamma(\alpha+i\beta)}=\lfab{\Gamma(\alpha)}\prod_{n=0}^\infty\lfbr{1+\frac{\beta^2}{(\alpha+n)^2}}^{-\frac{1}{2}}
\end{aligned}
$$

-----

### 13.1.17

$$
\begin{aligned}
\Gamma(n+ib+1)=(n+ib)(n-1+ib)\cdots(1+ib)\Gamma(1+ib)
\end{aligned}
$$

From Exercise 13.1.16,

$$
\begin{aligned}
\lfab{\Gamma(1+ib)}=\lfab{\Gamma(1)}\prod_{n=0}^\infty\lfbr{1+\frac{b^2}{(1+n)^2} }^{-\frac{1}{2}}
\end{aligned}
$$

From Equation 11.89, let $z=i\pi b$, then

$$
\begin{aligned}
\sin(i\pi b)=i\pi b\prod_{n=1}^\infty\lfpr{1+\frac{b^2}{n^2}}
\end{aligned}
$$

so

$$
\begin{aligned}
\prod_{n=0}^\infty\lfbr{1+\frac{b^2}{(1+n)^2} }^{-\frac{1}{2}}=\lfpr{\frac{i\pi b}{\sin(i\pi b)}}^{\frac{1}{2}}=\lfpr{\frac{\pi b}{\sinh\pi b}}^{\frac{1}{2}}
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
\lfab{\Gamma(n+ib+1)}=\lfab{\Gamma(1+ib)}\prod_{s=1}^n\lfab{s+ib}=\lfpr{\frac{\pi b}{\sinh\pi b}}^{\frac{1}{2}}\prod_{s=1}^n(s^2+b^2)^{\frac{1}{2}}
\end{aligned}
$$

-----

### 13.1.18

From Exercise 13.1.16, 

$$
\begin{aligned}
\frac{|\Gamma(x)|}{|\Gamma(x+iy)|}=\prod_{n=0}^\infty\lfbr{1+\frac{y^2}{(x+n)^2}}^{\frac{1}{2}}\geq1
\end{aligned}
$$

so $\abs{\Gamma(x)}\geq\abs{\Gamma(x+iy)}$.

-----

### 13.1.19

From Exercise 13.1.16,

$$
\begin{aligned}
|\Gamma(\frac{1}{2}+iy)|^2=|\Gamma(\frac{1}{2})|^2\prod_{n=0}^\infty\lfbr{1+\frac{y^2}{(\frac{1}{2}+n)^2}}^{-1}=\frac{\pi}{\prod_{n=0}^\infty\lfbr{1+\frac{y^2}{(\frac{1}{2}+n)^2}}}
\end{aligned}
$$

By Equation 11.90,

$$
\begin{aligned}
\cosh \pi y=\cos i\pi y=\prod_{n=1}^\infty\lfpr{1-\frac{(i\pi y)^2}{(n-\frac{1}{2})^2\pi^2}}=\prod_{n=0}^\infty\lfpr{1+\frac{y^2}{(n+\frac{1}{2})^2}}
\end{aligned}
$$

so

$$
\begin{aligned}
|\Gamma(\frac{1}{2}+iy)|^2=\frac{\pi}{\cosh\pi y}
\end{aligned}
$$

-----

### 13.1.20

(a)
Using the results from 13.1.10, and substituting $x-\mu=y$:

$$
\begin{aligned}
\int\limits_{-\infty}^\infty f(x)dx&=\int\limits_{-\infty}^\infty\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{y^2}{2\sigma^2}}dy=\frac{2}{\sigma\sqrt{2\pi}}\frac{\Gamma(\frac{1}{2})}{2\cdot2^{-\frac{1}{2}}\sigma^{-1}}=1\\
\langle x\rangle=\int\limits_{-\infty}^\infty xf(x)dx&=\int\limits_{-\infty}^\infty(y+\mu)\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{y^2}{2\sigma^2}}dy=0+\mu\cdot1=\mu
\end{aligned}
$$

Note that the integral containing $y$ vanishes since the integrand is an odd function.

(b)

$$
\begin{aligned}
        \langle x^2\rangle & =\int\limits_{-\infty}^\infty x^2f(x)dx=\int\limits_{-\infty}^\infty(y^2+2\mu y+\mu^2)\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{y^2}{2\sigma^2}}dy\\
        & =\frac{2}{\sigma\sqrt{2\pi}}\frac{\Gamma(\frac{3}{2})}{2\cdot2^{-\frac{3}{2}}\sigma^{-3}}+0+\mu^2\cdot1=\sigma^2+\mu^2\\
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
(\langle x^2\rangle-\langle x\rangle^2)^{\frac{1}{2}}=(\sigma^2+\mu^2-\mu^2)=\sigma
\end{aligned}
$$

-----

### 13.1.21

(a)

$$
\begin{aligned}
\brke{x}=\int\limits_{0}^\infty xf(x)dx=\frac{1}{\beta^\alpha\Gamma(\alpha)}\int\limits_{0}^\infty x^\alpha e^{-\frac{x}{\beta}}dx=\frac{\beta^\alpha\cdot\beta}{\beta^\alpha\Gamma(\alpha)}\int\limits_{0}^\infty y^\alpha e^{-y}dy=\frac{\beta\Gamma(\alpha+1)}{\Gamma(\alpha)}=\alpha\beta
\end{aligned}
$$

(b)

$$
\begin{aligned}
\brke{x^2}&=\int\limits_{0}^\infty x^2f(x)dx=\frac{1}{\beta^\alpha\Gamma(\alpha)}\int\limits_{0}^\infty x^{\alpha+1} e^{-\frac{x}{\beta}}dx=\frac{\beta^{\alpha+1}\cdot\beta}{\beta^\alpha\Gamma(\alpha)}\int\limits_{0}^\infty y^{\alpha+1} e^{-y}dy=\frac{\beta^2\Gamma(\alpha+2)}{\Gamma(\alpha)}=\alpha^2\beta^2+\alpha\beta^2\\
\sigma^2&=\brke{x^2}-\brke{x}^2=\alpha\beta^2
\end{aligned}
$$

-----

### 13.1.22

From Exercise 13.1.16,

$$
\begin{aligned}
\lfab{\Gamma(1+i\gamma)}^2=\lfab{\Gamma(1)}^2\prod_{n=0}^\infty\lfbr{1+\frac{\gamma^2}{(1+n)^2}}^{-1}=\prod_{n=1}^\infty\lfbr{1+\frac{\gamma^2}{n^2}}^{-1}
\end{aligned}
$$

By Equation 11.89, we have

$$
\begin{aligned}
\frac{\sin(i\pi\gamma)}{i\pi\gamma}=\prod_{n=1}^\infty\lfbr{1+\frac{\gamma^2}{n^2}}
\end{aligned}
$$

so

$$
\begin{aligned}
\lfbr{\Gamma(1+i\gamma)}^2=\frac{i\pi\gamma}{\sin(i\pi\gamma)}=\frac{2\pi\gamma}{e^{\pi\gamma}-e^{-\pi\gamma}}
\end{aligned}
$$

and therefore

$$
\begin{aligned}
\lfbr{\psi(0)}^2=e^{-\pi\gamma}\lfab{\Gamma(1+i\gamma)}^2=\frac{2\pi\gamma}{e^{2\pi\gamma}-1}
\end{aligned}
$$

-----

### 13.1.23

$$
\begin{aligned}
\int\limits_C e^{-t}(-t)^\nu dt=e^{-i\pi\nu}\int\limits_C e^{-t}t^{\nu}dt=e^{-i\pi\nu}\lfpr{e^{2i\pi\nu}-1}\Gamma(\nu+1)=2i\sin\pi\nu\Gamma(\nu+1)
\end{aligned}
$$

## 13.2 Digamma and Polygamma Functions

### 13.2.1

The ratio of successive terms is 

$$
\begin{aligned}
\lim_{n\to\infty}\lfab{\frac{a_{n+1}}{a_n}}=\lfab{\frac{\zeta(n+1)}{\zeta(n)}\frac{n}{n+1}\cdot x }=\lfab{\frac{1}{1}\cdot x }=\lfab{x }
\end{aligned}
$$

so by ratio test, the series converges when $\abs{x}<1$ and diverges at $\abs{x}>1$. At $x=1$, the series is an alternative series and converges since $\lim_{n\to\infty}\frac{\zeta(n)}{n}=0$. At $x=-1$, 

$$
\begin{aligned}
\frac{u_n}{u_{n+1}}=\frac{\zeta(n)}{\zeta(n+1)}\frac{n+1}{n}=1+\frac{1}{n}+\frac{B(n^2)}{n^2}
\end{aligned}
$$

where $B(n)$ is bounded for large $n$, so the series diverges by Gauss test.

Therefore, the range of convergence is $-1<x\leq 1$.

-----

### 13.2.2

(a)
Separate the odd and even terms, we have

$$
\begin{aligned}
\ln\Gamma(x+1)=-\gamma x +\sum_{n=1}^{\infty}\frac{\zeta(2n)}{2n}x^{2n}-\sum_{n=1}^\infty\frac{\zeta(2n+1)}{2n+1}x^{2n+1}
\end{aligned}
$$

Using Equation 12.38 to relate the zeta functions with Bernoulli numbers in the series of even terms, we have

$$
\begin{aligned}
\sum_{n=1}^\infty\frac{\zeta(2n)}{2n}x^{2n}=-\frac{1}{2}\sum_{n=1}^\infty(-1)^nB_{2n}\frac{(2\pi x)^{2n}}{(2n)!2n}
\end{aligned}
$$

From Equation 12.35, we have

$$
\begin{aligned}
\cot t =\frac{1}{t}+2\sum_{n=1}^\infty(-1)^n B_{2n}\frac{(2t)^{2n-1}}{(2n)!}
\end{aligned}
$$

Integrating both sides:

$$
\begin{aligned}
\ln\sin t=\ln t+\sum_{n=1}^\infty(-1)^nB_{2n}\frac{(2t)^{2n}}{(2n)!(2n)}
\end{aligned}
$$

Substituting, we have

$$
\begin{aligned}
\sum_{n=1}^\infty\frac{\zeta(2n)}{2n}x^{2n}=-\frac{1}{2}\lfbr{\ln\sin\pi x -\ln\pi x }=\frac{1}{2}\ln\lfpr{\frac{\pi x}{\sin\pi x}}
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
\ln\Gamma(x+1)=\frac{1}{2}\ln\lfpr{\frac{\pi x}{\sin\pi x}}-\gamma x-\sum_{n=1}^\infty\frac{\zeta(2n+1)}{2n+1}x^{2n+1}
\end{aligned}
$$

The range of convergence is $-1<x<1$ by ratio test.

(b) 
The last term in (a) is

$$
\begin{aligned}
-\sum_{n=1}^\infty\frac{\zeta(2n+1)}{2n+1}x^{2n+1}=-\sum_{n=1}^\infty\lfbr{\zeta(2n+1)-1 }\frac{x^{2n+1}}{2n+1}-\sum_{n=1}^\infty\frac{x^{2n+1}}{2n+1}
\end{aligned}
$$

Using the expansion

$$
\begin{aligned}
-\frac{1}{2}\ln\lfpr{\frac{1+x}{1-x}}=-\frac{1}{2}\lfbr{\sum_{n=1}^\infty(-1)^{n-1}\frac{x^n}{n}+\sum_{n=1}^\infty\frac{x^n}{n} }=-\frac{1}{2}\lfbr{2x+2\sum_{n=1}^\infty\frac{x^{2n+1}}{2n+1} }=-x-\sum_{n=1}^\infty\frac{x^{2n+1}}{2n+1}
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
        \ln\Gamma(x+1) & =\frac{1}{2}\ln\lfpr{\frac{\pi x}{\sin\pi x} }-\gamma x-\sum_{n=1}^\infty\lfbr{\zeta(2n+1)-1 }\frac{x^{2n+1}}{2n+1}+x-\frac{1}{2}\ln\lfpr{\frac{1+x}{1-x} }\\
        & =\frac{1}{2}\ln\lfpr{\frac{\pi x}{\sin\pi x} }-\frac{1}{2}\ln\lfpr{\frac{1+x}{1-x} }+(1-\gamma)x-\sum_{n=1}^\infty\lfbr{\zeta(2n+1)-1 }\frac{x^{2n+1}}{2n+1}
\end{aligned}
$$

The range of convergence is the same as (a), which is $-1<x<1$.

-----

### 13.2.3

$$
\begin{aligned}
\sum_{j=1}^\infty\frac{n}{j(n+j)}=\sum_{j=1}^\infty\lfpr{\frac{1}{j}-\frac{1}{n+j} }=\sum_{j=1}^n\frac{1}{j}+\sum_{j=1}^\infty\frac{1}{n+j}-\sum_{j=1}^\infty\frac{1}{n+j}=\sum_{j=1}^n\frac{1}{j}
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
\psi(n+1)=\sum_{j=1}^n\frac{1}{j}-\gamma=\sum_{j=1}^n\frac{n}{j(n+j)}-\gamma
\end{aligned}
$$

-----

### 13.2.4

From Equation 13.40,

$$
\begin{aligned}
        \psi(z+1) &= -\gamma +\sum_{m=1}^\infty\lfpr{\frac{1}{m}-\frac{1}{m+z} }\\
        & =-\gamma+\sum_{m=1}^\infty\lfbr{\frac{1}{m}-\frac{1}{m}\sum_{n=0}^\infty(-1)^n\frac{z^n}{m^n} }\\
        & =-\gamma+\sum_{m=1}^\infty\sum_{n=1}^\infty(-1)^{n+1}\frac{z^n}{m^{n+1}}\\
        & =-\gamma+\sum_{n=2}^\infty(-1)^n\sum_{m=1}^\infty\frac{z^{n-1}}{m^n}\\
        & =-\gamma+\sum_{n=2}^\infty(-1)^n\zeta(n)z^{n-1}
\end{aligned}
$$

-----

### 13.2.5

(a)
From Equation 13.44,

$$
\begin{aligned}
        \ln\Gamma(z+1) & =-\gamma z+\sum_{n=2}^\infty(-1)^n\frac{z^n}{n}\zeta(n)\\
        & =-\gamma z+\sum_{n=2}^\infty(-1)^n\lfbr{\zeta(n)-1 }\frac{z^n}{n}+\sum_{n=2}^\infty(-1)^n\frac{z^n}{n}\\
        & =-\gamma z+\sum_{n=2}^\infty(-1)^n\lfbr{\zeta(n)-1 }\frac{z^n}{n}+\sum_{n=1}^\infty(-1)^n\frac{z^n}{n}+z\\
        & =-\ln(1+z)+z(1-\gamma)+\sum_{n=2}^\infty(-1)^n\lfbr{\zeta(n)-1 }\frac{z^n}{n}
\end{aligned}
$$

where we use the series $-\ln(1+z)=\sum_{n=1}^\infty(-1)^n\frac{z^n}{n}$.

(b)
The last summation in (a) has a radius of convergence $R=2$ since $\zeta(n)-1=\frac{1}{2^n}+\frac{1}{3^n}+\cdots\approx \frac{1}{2^n}$ for large $n$, but the summation $-\ln(1+z)=\sum_{n=1}^\infty(-1)^n\frac{z^n}{n}$ has a radius of convergence $R=1$, so the range of convergence is the same as that in Exercise 13.2.1, which is $-1<x\leq 1$.

-----

### 13.2.6

(It is a part of Exercise 13.2.2) 
Using Equation 12.38 to relate the zeta functions with Bernoulli numbers, we have

$$
\begin{aligned}
\sum_{n=1}^\infty\frac{\zeta(2n)}{2n}z^{2n}=-\frac{1}{2}\sum_{n=1}^\infty(-1)^nB_{2n}\frac{(2\pi z)^{2n}}{(2n)!2n}
\end{aligned}
$$

From Equation 12.35, we have

$$
\begin{aligned}
\cot t =\frac{1}{t}+2\sum_{n=1}^\infty(-1)^n B_{2n}\frac{(2t)^{2n-1}}{(2n)!}
\end{aligned}
$$

Integrating both sides:

$$
\begin{aligned}
\ln\sin t=\ln t+\sum_{n=1}^\infty(-1)^nB_{2n}\frac{(2t)^{2n}}{(2n)!(2n)}
\end{aligned}
$$

Substituting, we have

$$
\begin{aligned}
\frac{1}{2}\ln\lfpr{\frac{\pi z}{\sin\pi z}}=-\frac{1}{2}\lfbr{\ln\sin\pi z -\ln\pi z }=\sum_{n=1}^\infty\frac{\zeta(2n)}{2n}z^{2n}
\end{aligned}
$$

The range of convergence is $-1<z<1$ by ratio test.

-----

### 13.2.7

From Equation 13.15,

$$
\begin{aligned}
    \ln\Gamma(z+1) & =\ln z+\ln\Gamma(z)\\
    & =\ln z-\ln z-\gamma z-\sum_{m=1}^\infty\ln\lfpr{1+\frac{z}{m} }+\sum_{m=1}^\infty\frac{z}{m}\\
    & =-\gamma z+\sum_{m=1}^\infty\lfbr{\frac{z}{m}+\sum_{n=1}^\infty(-1)^n\frac{1}{n}\cdot\frac{z^n}{m^n} }\\
    & =-\gamma z+\sum_{m=1}^\infty\sum_{n=2}^\infty(-1)^n\frac{z^n}{n}\cdot\frac{1}{m^n}\\
    & =-\gamma z+\sum_{n=2}^\infty(-1)^n\frac{z^n}{n}\zeta(n)
\end{aligned}
$$

-----

### 13.2.8

From Equation 13.41,

$$
\begin{aligned}
        \psi^{(m)}(z+2) & =(-1)^{m+1}m!\sum_{n=1}^\infty\frac{1}{(z+1+n)^{m+1}}\\
        & =(-1)^{m+1}m!\sum_{n=1}^\infty\frac{1}{(z+n)^{m+1}}-(-1)^{m+1}m!\frac{1}{(z+1)^{m+1}}\\
        & =\psi^{(m)}(z+1)+(-1)^m\frac{m!}{(z+1)^{m+1}}
\end{aligned}
$$

-----

### 13.2.9

(a)

$$
\begin{aligned}
(a)_n=\frac{(a+n-1)!}{(n-1)!}=\frac{\Gamma(a+n)}{\Gamma(n)}
\end{aligned}
$$

(b)

$$
\begin{aligned}
    \frac{d}{da}(a_n) & =\frac{da}{da}(a+1)\cdots(a+n-1)+a\frac{d(a+1)}{da}\cdots(a+n-1)+a(a+1)\cdots\frac{d(a+n-1)}{da}\\
    & =(a)_n\lfbr{\frac{1}{a}+\frac{1}{a+1}+\cdots+\frac{1}{a+n-1} }\\
    & =(a)_n\lfbr{\lfpr{-\gamma+\sum_{m=1}^{a+n-1}\frac{1}{m} }-\lfpr{-\gamma+\sum_{m=1}^{a-1}\frac{1}{m} } }\\
    & =(a)_n\lfbr{\psi(a+n)-\psi(a) }
\end{aligned}
$$

where we use Equation 13.40.

(c)

$$
\begin{aligned}
(a)_{n+k}=\lfbr{a(a+1)\cdots(a+n-1) }\lfbr{(a+n)(a+n+1)\cdots(a+n+k-1) }=(a)_n\cdot(a+n)_k 
\end{aligned}
$$

-----

### 13.2.10

From Equation 13.36,

$$
\begin{aligned}
\psi(1)&=\lim_{n\to\infty}\lfpr{\ln n-\frac{1}{1}-\frac{1}{2}-\cdots-\frac{1}{n} }=-\gamma\\
\psi^{(1)}(1)&=\lim_{n\to\infty}\lfpr{\frac{1}{n}+\frac{1}{1^2}+\frac{1}{2^2}+\cdots+\frac{1}{n^2} }=\zeta(2)\\
\psi^{(2)}(1)&=\lim_{n\to\infty}\lfpr{-\frac{1}{n^2}-\frac{2}{1^3}-\frac{2}{2^3}-\cdots-\frac{2}{n^3} }=-2\zeta(3)
\end{aligned}
$$

-----

### 13.2.11

(a)
Differentiating the integral definition of $\Gamma(z+1)$ using Leibniz integral rule, we have

$$
\begin{aligned}
\Gamma(z+1)&=\int\limits_0^\infty e^{-r}r^zdr\\
\frac{d\Gamma(z+1)}{dz}&=\int\limits_0^\infty\pdv{}{z}\lfbr{e^{-r}r^z }dr=\int\limits_0^\infty e^{-r}r^z\ln r\,dr
\end{aligned}
$$

Making $z=0$, and using Equation 13.37 and 13.39, we have

$$
\begin{aligned}
\int\limits_0^\infty e^{-r}\ln r\,dr=\Gamma'(1)=\Gamma(1)\psi(1)=-\gamma
\end{aligned}
$$

(b)
Integrating by parts:

$$
\begin{aligned}
        \int\limits_0^\infty e^{-r} r\ln r\,dr & =\lfbr{-e^{-r}r\ln r }_0^\infty +\int\limits_0^\infty e^{-r}\lfbr{r\cdot\frac{1}{r}+\ln r }dr\\
        & =0+\int\limits_0^\infty e^{-r}dr+\int\limits_0^\infty e^{-r}\ln r\,dr\\
        & =1-\gamma
\end{aligned}
$$

(c)
Similar with (b),

$$
\begin{aligned}
        \int\limits_0^\infty e^{-r}r^n\ln r\,dr & =\lfbr{-e^{-r}r^n\ln r }_0^\infty+\int\limits_0^\infty e^{-r}\lfbr{r^{n-1}+nr^{n-1}\ln r }dr\\
        & =0+\int\limits_0^\infty e^{-r}r^{n-1}dr+n\int\limits_0^\infty e^{-r}r^{n-1}\ln r\,dr\\
        & =(n-1)!+n\int\limits_0^\infty e^{-r}r^{n-1}\ln r\,dr
\end{aligned}
$$

-----

### 13.2.12

Making the substitution $x=\alpha^2Z^2$ and $z=2(1-x)^{\frac{1}{2}}$, and expanding about $x=0$, we have

$$
\begin{aligned}
\Gamma\lfbr{2(1-\alpha^2Z^2)^{\frac{1}{2}}+1 }=\lfbr{\Gamma(z+1) }_{x=0}+\lfbr{\frac{d\Gamma(z+1)}{dx} }_{x=0}x+\frac{1}{2!}\lfbr{\frac{d^2\Gamma(z+1)}{dx^2} }_{x=0}x^2+\cdots
\end{aligned}
$$

Differentiating, we have

$$
\begin{aligned}
\frac{d\Gamma(z+1)}{dx} &=\Gamma'(z+1)\frac{dz}{dx} \\
\frac{d^2\Gamma(z+1)}{dx^2} &=\Gamma''(z+1)\lfpr{\frac{dz}{dx} }^2+\Gamma'(z+1)\frac{d^2z}{dx^2}
\end{aligned}
$$

Using Equation 13.37, 13.40, 13.41 to evaluate the terms at $x=0$ (or $z+1=3$), we have

$$
\begin{aligned}
\Gamma'(3) & =\Gamma(3)\psi(3)=2(-\gamma+\frac{3}{2})=-2\gamma+3\\
\Gamma''(3) & =\Gamma(3)\lfbr{\psi^2(3)+\psi'(3) }=2\lfbr{(-\gamma+\frac{3}{2})^2+\zeta(2)-\frac{5}{4} }=2\gamma^2-6\gamma+2\zeta(2)+2\\
\frac{dz(0)}{dx} & =\lfbr{-(1-x)^{-\frac{1}{2}} }_{x=0}=-1\\
\frac{d^2z(0)}{dx^2} & =\lfbr{-\frac{1}{2}(1-x)^{-\frac{3}{2}} }_{x=0}=-\frac{1}{2}
\end{aligned}
$$

Substituting, we have

$$
\begin{aligned}
\Gamma\lfbr{2(1-\alpha^2Z^2)^{\frac{1}{2}}+1 }=2+(2\gamma-3)\alpha^2Z^2+\lfpr{\gamma^2-\frac{5}{2}\gamma+\zeta(2)+\frac{1}{4} }\alpha^4Z^4+\cdots 
\end{aligned}
$$

-----

### 13.2.13

The argument of $\Gamma(1+ib)$ is the imaginary part of $\ln\Gamma(1+ib)$. From Equation 13.44,

$$
\begin{aligned}
\ln\Gamma(1+ib)=-\gamma ib+\sum_{n=2}^\infty(-1)^n\frac{(ib)^n}{n}\zeta(n)=\lfbr{\sum_{n=1}^\infty(-1)^n\frac{b^{2n}}{2n}\zeta(2n)}+\lfbr{-\gamma b-\sum_{n=1}^\infty(-1)^n\frac{b^{2n+1}}{2n+1}\zeta(2n+1) }i
\end{aligned}
$$

Therefore, the argument of $\Gamma(1+ib)$ is approximately $-\gamma b$ for small $b$. 

-----

### 13.2.14

(a)
From Equation 13.38,

$$
\begin{aligned}
&\psi(1+1)=-\gamma+\sum_{n=1}^\infty\frac{1}{n(n+1)}\\
&\sum_{n=1}^\infty\frac{1}{n(n+1)}=\psi(2)+\gamma=1
\end{aligned}
$$

(b)

$$
\begin{aligned}
\psi(2+1)&=-\gamma+\sum_{n=1}^\infty\frac{2}{n(n+2)}\\
\sum_{n=2}^\infty\frac{1}{n^2-1}&=\sum_{n=1}^\infty\frac{1}{n(n+2)}=\frac{1}{2}\lfpr{\psi(3)+\gamma }=\frac{3}{4}
\end{aligned}
$$

-----

### 13.2.15

From Equation 13.38,

$$
\begin{aligned}
\psi(1+b)&=-\gamma+\sum_{n=1}^\infty\frac{b}{n(n+b)}\\
\psi(1+a)&=-\gamma+\sum_{n=1}^\infty\frac{a}{n(n+a)}\\
\frac{1}{(b-a)}\lfbr{\psi(1+b)-\psi(1+a) }&=\frac{1}{(b-a)}\sum_{n=1}^\infty\frac{b(n+a)-a(n+b)}{n(n+a)(n+b)}=\sum_{n=1}^\infty\frac{1}{(n+a)(n+b)}
\end{aligned}
$$

## 13.3 The Beta Function

### 13.3.1

(a)

$$
\begin{aligned}
B(a+1,b)+B(a,b+1)=\frac{\Gamma(a+1)\Gamma(b)}{\Gamma(a+b+1)}+\frac{\Gamma(a)\Gamma(b+1)}{\Gamma(a+b+1)}=\frac{a\Gamma(a)\Gamma(b)+b\Gamma(a)\Gamma(b)}{(a+b)\Gamma(a+b)}=\frac{\Gamma(a)\Gamma(b)}{\Gamma(a+b)}=B(a,b)
\end{aligned}
$$

(b)

$$
\begin{aligned}
\frac{a+b}{b}B(a,b+1)=\frac{a+b}{b}\frac{\Gamma(a)\Gamma(b+1)}{\Gamma(a+b+1)}=\frac{a+b}{b}\frac{\Gamma(a)b\Gamma(b)}{(a+b)\Gamma(a+b)}=\frac{\Gamma(a)\Gamma(b)}{\Gamma(a+b)}=B(a,b)
\end{aligned}
$$

(c)

$$
\begin{aligned}
\frac{b-1}{a}B(a+1,b-1)=\frac{b-1}{a}\frac{\Gamma(a+1)\Gamma(b-1)}{\Gamma(a+b)}=\frac{b-1}{a}\frac{a\Gamma(a)\frac{1}{b-1}\Gamma(b)}{\Gamma(a+b)}=\frac{\Gamma(a)\Gamma(b)}{\Gamma(a+b)}=B(a,b)
\end{aligned}
$$

(d)

$$
\begin{aligned}
B(a,b)B(a+b,c)&=\frac{\Gamma(a)\Gamma(b)}{\Gamma(a+b)}\frac{\Gamma(a+b)\Gamma(c)}{\Gamma(a+b+c)}=\frac{\Gamma(a)\Gamma(b)\Gamma(c)}{\Gamma(a+b+c)}\\
B(b,c)B(a,b+c)&=\frac{\Gamma(b)\Gamma(c)}{\Gamma(b+c)}\frac{\Gamma(a)\Gamma(b+c)}{\Gamma(a+b+c)}=\frac{\Gamma(a)\Gamma(b)\Gamma(c)}{\Gamma(a+b+c)}
\end{aligned}
$$

-----

### 13.3.2

(a)
From Equation 13.50,

$$
\begin{aligned}
\int\limits_{-1}^1(1-x^2)^{\frac{1}{2}}x^{2n}dx=2\int\limits_0^1(1-x^2)^{\frac{1}{2}}x^{2(n-\frac{1}{2})+1}dx=B(n-\frac{1}{2}+1,\frac{1}{2}+1)=B(n+\frac{1}{2},\frac{3}{2})
\end{aligned}
$$

For $n=0$,

$$
\begin{aligned}
B(\frac{1}{2},\frac{3}{2})=\frac{\Gamma(\frac{1}{2})\Gamma(\frac{3}{2})}{\Gamma(2)}=\frac{\sqrt{\pi}\frac{1}{2}\sqrt{\pi}}{1}=\frac{\pi}{2}
\end{aligned}
$$

For $n=1,2,3,\cdots$,

$$
\begin{aligned}
B(n+\frac{1}{2},\frac{3}{2})=\frac{\Gamma(n+\frac{1}{2})\Gamma(\frac{3}{2})}{\Gamma(n+2)}=\frac{\sqrt{\pi}\frac{(2n-1)!!}{2^n}\frac{1}{2}\sqrt{\pi}}{(n+1)!}=\pi\frac{(2n-1)!!}{(2n+2)!!}
\end{aligned}
$$

(b)

$$
\begin{aligned}
\int\limits_{-1}^1(1-x^2)^{-\frac{1}{2}}x^{2n}dx=2\int\limits_0^1(1-x^2)^{-\frac{1}{2}}x^{2(n-\frac{1}{2})+1}dx=B(n-\frac{1}{2}+1,-\frac{1}{2}+1)=B(n+\frac{1}{2},\frac{1}{2})
\end{aligned}
$$

For $n=0$,

$$
\begin{aligned}
B(\frac{1}{2},\frac{1}{2})=\frac{\Gamma(\frac{1}{2})\Gamma(\frac{1}{2})}{\Gamma(1)}=\frac{\sqrt{\pi}\sqrt{\pi}}{1}=\pi
\end{aligned}
$$

For $n=1,2,3,\cdots$,

$$
\begin{aligned}
B(n+\frac{1}{2},\frac{1}{2})=\frac{\Gamma(n+\frac{1}{2})\Gamma(\frac{1}{2})}{\Gamma(n+1)}=\frac{\sqrt{\pi}\frac{(2n-1)!!}{2^n}\sqrt{\pi}}{n!}=\pi\frac{(2n-1)!!}{(2n)!!}
\end{aligned}
$$

-----

### 13.3.3

From Equation 13.50,

$$
\begin{aligned}
\int\limits_{-1}^1(1-x^2)^ndx=B(\frac{1}{2},n+1)=\frac{\Gamma(\frac{1}{2})\Gamma(n+1)}{\Gamma(n+\frac{3}{2})}=\frac{\sqrt{\pi}\cdot n!}{\sqrt{\pi}\frac{(2n+1)!!}{2^{n+1}}}=\frac{2(2n)!!}{(2n+1)!!}
\end{aligned}
$$

-----

### 13.3.4

Using the substitution $x=\cos2\theta$, so $1+x=2\cos^2\theta$, $1-x=2\sin^2\theta$, and $dx=-4\sin\theta\cos\theta d\theta$, we have

$$
\begin{aligned}
        & \int\limits_{-1}^1(1+x)^a(1-x)^bdx\\
        = & \int\limits_{\frac{\pi}{2}}^0 2^a\cos^{2a}\theta\cdot2^b\sin^{2b}\theta(-4\sin\theta\cos\theta d\theta)\\
        = & 2^{a+b+2}\int\limits_0^{\frac{\pi}{2}}\cos^{2a+1}\theta\sin^{2b+1}\theta d\theta\\
        = & 2^{a+b+1}B(a+1,b+1)
\end{aligned}
$$

where we used Equation 13.47.

-----

### 13.3.5

To make the range of integral becomes from $0$ to $1$, use the substitution $u=\frac{x-t}{z-t}$, so $du=\frac{dx}{z-t}$, $x-t=(z-t)u$, $z-x=(z-t)(1-u)$. Substituting, 

$$
\begin{aligned}
\int\limits_t^z\frac{dx}{(z-x)^{1-\alpha}(x-t)^\alpha}=\int\limits_0^1\frac{(z-t)du}{(z-t)^{1-\alpha+\alpha}(1-u)^{1-\alpha}u^{\alpha}}=B(1-\alpha,\alpha)=\frac{\Gamma(1-\alpha)\Gamma(\alpha)}{\Gamma(1)}=\frac{\pi}{\sin\alpha}
\end{aligned}
$$

where we use Equation 13.49 and 13.23.

-----

### 13.3.6

$$
\begin{aligned}
\int\int x^py^qdx\,dy&=\int\limits_0^1 y^qdy\int\limits_0^{1-y}x^pdx=\int\limits_0^1y^q\cdot\frac{(1-y)^{p+1}}{p+1}dy=\frac{B(p+2,q+1)}{p+1}\\
\frac{B(p+2,q+1)}{p+1}&=\frac{\Gamma(p+2)\Gamma(q+1)}{(p+1)\Gamma(p+q+2)}=\frac{\Gamma(p+1)\Gamma(q+1)}{\Gamma(p+q+2)}=\frac{B(p+1,q+1)}{p+q+2}
\end{aligned}
$$

-----

### 13.3.7

Use the substitutions $u=x+y\cos\theta$ and $v=y\sin\theta$, which is a transformation from the oblique coordinates _x-y_ to the orthogonal coordinates _u-v_. We have

$$
\renewcommand\arraystretch{1.5}
\begin{aligned}
du\,dv&=
\begin{vmatrix}
\pdv{u}{x} & \pdv{u}{y}\\
\pdv{v}{x} & \pdv{v}{y}
\end{vmatrix}dx\,dy=
\begin{vmatrix}
1 & \cos\theta\\
0 & \sin\theta
\end{vmatrix}dx\,dy=\sin\theta\,dx\,dy\\
u^2+v^2&=x^2+y^2\cos^2\theta+2xy\cos\theta+y^2\sin^2\theta=x^2+y^2+2xy\cos\theta
\end{aligned}
$$

Substituting, we have

$$
\begin{aligned}
\int\limits_0^\infty\int\limits_0^\infty e^{-(x^2+y^2+2xy\cos\theta)}dx\,dy=\int\limits_{v=0}^\infty\int\limits_{u=\cot\theta}^\infty e^{-(x^2+y^2)}\frac{du\,dv}{\sin\theta}=\int\limits_{r=0}^\infty\int\limits_{\phi=0}^\theta e^{-r^2}\frac{r\,dr\,d\phi}{\sin\theta}=\frac{1}{\sin\theta}\lfbr{\frac{e^{-r^2}}{-2}}_0^\infty\theta=\frac{\theta}{\sin\theta}
\end{aligned}
$$

where we transforms to the polar coordinates for integration. The area of integration is between $v=0$ and $v=u\tan\theta$, so the angle $\theta$ is restriced to $-\pi<\theta<\pi$.

-----

### 13.3.8

From Equation 13.47,

$$
\begin{aligned}
\int\limits_0^{\frac{\pi}{2}}\cos^{\frac{1}{2}}\theta\,d\theta=\frac{B(\frac{3}{4},\frac{1}{2})}{2}=\frac{\Gamma(\frac{3}{4})\Gamma(\frac{1}{2})}{2\Gamma(\frac{5}{4})}=\frac{\pi}{2\sqrt{2}\Gamma(\frac{5}{4})}\times\frac{\sqrt{\pi}}{2\Gamma(\frac{5}{4})}=\frac{(2\pi)^{\frac{3}{2}}}{16\lfbr{\Gamma(\frac{5}{4})}^2}
\end{aligned}
$$

where we use Equation 13.23 to relate $\Gamma(\frac{3}{4})$ and $\Gamma(\frac{5}{4})$:

$$
\begin{aligned}
\Gamma(\frac{3}{4})=\frac{1}{\Gamma(\frac{1}{4})}\frac{\pi}{\sin\frac{\pi}{4}}=\frac{\pi}{2\sqrt{2}\Gamma(\frac{5}{4})}
\end{aligned}
$$

-----

### 13.3.9

From Equation 13.49:

$$
\begin{aligned}
\int\limits_0^1(1-x^4)^{-\frac{1}{2}}dx=\frac{1}{4}B(\frac{1}{4},\frac{1}{2})=\frac{1}{4}\frac{\Gamma(\frac{1}{4})\Gamma(\frac{1}{2})}{\Gamma(\frac{3}{4})}=\frac{1}{4}\frac{\Gamma(\frac{1}{4})\sqrt{\pi}}{\frac{1}{\Gamma(\frac{1}{4})}\frac{\pi}{\sin\frac{\pi}{4}}}=\frac{\lfbr{\Gamma(\frac{1}{4})}^2}{4\sqrt{2\pi}}=\frac{4\lfbr{\Gamma(\frac{5}{4})}^2}{\sqrt{2\pi}}
\end{aligned}
$$

-----

### 13.3.10

Expand the term $\cos(z\cos\theta)$:

$$
\begin{aligned}
\cos(z\cos\theta)=\sum_{s=0}^\infty\frac{(-1)^s}{(2s)!}z^{2s}\cos^{2s}\theta
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
\int\limits_0^{\frac{\pi}{2}}\sin^{2\nu}\theta\cos(z\cos\theta)d\theta=\sum_{s=0}^\infty\frac{(-1)^s}{(2s)!}z^{2s}\int\limits_0^{\frac{\pi}{2}}\sin^{2\nu}\theta\cos^{2s}\theta\,d\theta=\sum_{s=0}^\infty\frac{(-1)^s}{(2s)!}z^{2s}\frac{B(\nu+\frac{1}{2},s+\frac{1}{2})}{2}
\end{aligned}
$$

Substituting,

$$
\begin{aligned}
        J_\nu & =\frac{2}{\sqrt{\pi}\Gamma(\nu+\frac{1}{2})}\lfpr{\frac{z}{2}}^{\nu}\sum_{s=0}^\infty\frac{(-1)^s}{(2s)!}z^{2s}\frac{\Gamma(\nu+\frac{1}{2})\Gamma(s+\frac{1}{2})}{2\Gamma(s+\nu+1)}\\
        & =\sum_{s=0}^\infty(-1)^s\lfpr{\frac{z}{2}}^{\nu}\frac{z^{2s}}{\Gamma(s+\nu+1)}\frac{\Gamma(s+\frac{1}{2})}{\sqrt{\pi}(2s)!}\\
        & =\sum_{s=0}^\infty(-1)^s\lfpr{\frac{z}{2}}^{\nu}\frac{z^{2s}}{\Gamma(s+\nu+1)}\frac{\sqrt{\pi}\frac{(2s-1)!!}{2^s}}{\sqrt{\pi}(2s)!!(2s-1)!!}\\
        & =\sum_{s=0}^\infty(-1)^s\frac{1}{s!\Gamma(s+\nu+1)}\lfpr{\frac{z}{2}}^{2s+\nu}
\end{aligned}
$$

-----

### 13.3.11

(a)

$$
\begin{aligned}
&\int\limits_{-1}^1\lfbr{P_m^m(x)}^2dx=2\int\limits_0^1\lfbr{(2m-1)!!}^2(1-x^2)^mdx=\lfbr{(2m-1)!!}^2B(\frac{1}{2},m+1)\\
&\lfbr{(2m-1)!!}^2\frac{\Gamma(\frac{1}{2})\Gamma(m+1)}{\Gamma(m+\frac{3}{2})}=\lfbr{(2m-1)!!}^2\frac{\sqrt{\pi}\cdot m!}{\sqrt{\pi}\frac{(2m+1)!!}{2^{m+1}}}=\frac{2}{2m+1}(2m)!
\end{aligned}
$$

(b)

$$
\begin{aligned}
&\int\limits_{-1}^1\lfbr{P_m^m(x)}^2\frac{dx}{1-x^2}=2\int\limits_0^1\lfbr{(2m-1)!!}^2(1-x^2)^{m-1}dx=\lfbr{(2m-1)!!}^2B(\frac{1}{2},m)\\
&\lfbr{(2m-1)!!}^2\frac{\Gamma(\frac{1}{2})\Gamma(m)}{\Gamma(m+\frac{1}{2})}=\lfbr{(2m-1)!!}^2\frac{\sqrt{\pi}\cdot(m-1)!}{\sqrt{\pi}\cdot\frac{(2m-1)!!}{2^m}}=2\cdot(2m-1)!
\end{aligned}
$$

-----

### 13.3.12

(a)

$$
\begin{aligned}
\int\limits_0^1 x^{2p+1}(1-x^2)^{-\frac{1}{2}}dx=\frac{B(p+1,\frac{1}{2})}{2}=\frac{\Gamma(p+1)\Gamma(\frac{1}{2})}{2\Gamma(p+\frac{3}{2})}=\frac{p!\cdot\sqrt{\pi}}{2\sqrt{\pi}\cdot\frac{(2p+1)!!}{2^{p+1}}}=\frac{(2p)!!}{(2p+1)!!}
\end{aligned}
$$

(b)

$$
\begin{aligned}
\int\limits_0^1 x^{2p}(1-x^2)^qdx=\frac{B(p+\frac{1}{2},q+1)}{2}=\frac{\Gamma(p+\frac{1}{2})\Gamma(q+1)}{2\Gamma(p+q+\frac{3}{2})}=\frac{\sqrt{\pi}\cdot\frac{(2p-1)!!}{2}\cdot q!}{2\sqrt{\pi}\cdot\frac{(2p+2q+1)!!}{2^{p+q+1}}}=\frac{(2p-1)!!(2q)!!}{(2p+2q+1)!!}
\end{aligned}
$$

-----

### 13.3.13

Use the substitution $t=\frac{Ax^n}{E}$, so $dt=\frac{nAx^{n-1}}{E}dx$, or $dx=\frac{1}{n}t^{\frac{1}{n}-1}(\frac{E}{A})^{\frac{1}{n}}dt$:

$$
\begin{aligned}
\tau&=2\sqrt{2m}\int\limits_0^1\frac{\frac{1}{n}t^{\frac{1}{n}-1}\lfpr{\frac{E}{A}}^{\frac{1}{n}}dt}{\sqrt{E}(1-t)^{\frac{1}{2}}}=\frac{2}{n}\sqrt{\frac{2m}{E}}\lfpr{\frac{E}{A}}^{\frac{1}{n}}\int\limits_0^1 t^{\frac{1}{n}-1}(1-t)^{-\frac{1}{2}}dt=\frac{2}{n}\sqrt{\frac{2m}{E}}\lfpr{\frac{E}{A}}^{\frac{1}{n}}B(\frac{1}{n},\frac{1}{2})\\
\tau&=\frac{2}{n}\sqrt{\frac{2m}{E}}\lfpr{\frac{E}{A}}^{\frac{1}{n}}\frac{\Gamma(\frac{1}{n})\Gamma(\frac{1}{2})}{\Gamma(\frac{1}{n}+\frac{1}{2})}=\frac{2}{n}\sqrt{\frac{2\pi m}{E}}\lfpr{\frac{E}{A}}^{\frac{1}{n}}\frac{\Gamma(\frac{1}{n})}{\Gamma(\frac{1}{n}+\frac{1}{2})}
\end{aligned}
$$

{% endraw %}
