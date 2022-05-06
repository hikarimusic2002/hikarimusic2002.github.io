---
layout: splash
title: "Mathematical Methods for Physicists"
permalink: /solutions/math_physics_ch1
author_profile: false
redirect_from:
  - /resume
---

# Chapter 1: Mathematical Preliminaries

## 1.1 Infinite Series

### 1.1.1

(a) If $A>0$, since $\lim_{n\to \infty}n^p u_n=A$, we have $\vert n^p u_n-A\vert < \frac{A}{2}$ when $n\geq N$ for some $N$. Then $0<\frac{A}{2}\frac{1}{n^p}<u_n<\frac{3A}{2}\frac{1}{n^p}$. Since $\sum_{n=1}^{\infty}\frac{3A}{2}\frac{1}{n^p}$ converges when $p>1$ by Cauchy integral test, $\sum_{n=1}^{\infty}u_n$ converges by comparison test.

If $A<0$, then $\lim_{n\to \infty}n^p(-u_n)=-A$ where $-A>0$. From above $\sum_1^\infty(-u_n)$ converges, so $\sum_1^\infty u_n$ converges.

If $A=0$, we have $\vert n^p u_n\vert < 1$ when $n\geq N$ for some N. Then $-\frac{1}{n^p}<u_n<\frac{1}{n^p}$, so $\vert u_n\vert <\frac{1}{n^p}$ for sufficiently large n. $\sum_{n=1}^\infty \frac{1}{n^p}$ converges by Cauchy integral test, so $\sum_{n=1}^{\infty}u_n$ converges by comparison test.

(b) $\lim_{n\to\infty}nu_n=A$, so $A-\frac{A}{2}<nu_n<A+\frac{A}{2}$ when $n\geq N$ for some N. So $u_n>\frac{A}{2}\frac{1}{n}$ for sufficiently large $n$. The harmonic series $\sum_{n=1}^\infty\frac{1}{n}$ diverges, so $\sum_{n=1}^\infty u_n$ diverges.

--------------

### 1.1.2

Let $b_n'=\frac{b_n}{2K}$, then $\lim_{n\to\infty}\frac{b_n'}{a_n}=\frac{1}{2}$, so for sufficiently large $n$, we have $\frac{1}{2}-\frac{1}{2}=0<\frac{b_n'}{a_n}<1=\frac{1}{2}+\frac{1}{2}$. Then $0<b_n'<a_n$ or $0>b_n'>a_n$, so $\sum a_n$ converging implies $\sum b_n'$ converging by comparison test, and therefore $\sum b_n$ converges.

Let $b_n''=\frac{2b_n}{K}$, then $\lim_{n\to\infty}\frac{b_n''}{a_n}=2$, so for sufficiently large $n$, we have $2+1=3>\frac{b_n''}{a_n}>1=2-1$.Then $3a_n>b_n'' >a_n$ or $3a_n<b_n'' <a_n$,  so $\sum a_n$ diverging implies $\sum b_n''$ divergeing by comparison test, and therefore $\sum b_n$ diverges.

--------------

### 1.1.3

$$
\begin{aligned}
\int_2^\infty\frac{1}{x(\ln x)^2}dx=-\left[\frac{1}{\ln x}\right]_2^\infty=\frac{1}{\ln 2}
\end{aligned}
$$

so by Cauchy integral test $\sum_{n=2}^\infty \frac{1}{n(\ln n)^2}$ converges.

--------------

### 1.1.4

$$
\begin{aligned}
\frac{u_n}{u_{n+1}}=1+\frac{(a_1-b_1)n+(a_0-b_0)}{n^2+b_1n+b_0}=1+\frac{a_1-b_1}{n}+\frac{B(n)}{n^2}
\end{aligned}
$$

where $B(n)$ is bounded for large n (it can be verified by binomial theorem, that each term in $B(n)$ has negative or zero power of n). By Gauss' test, $\sum_{n=1}^\infty u_n$ converges if $a_1-b_1>1$ and diverges if $a_1-b_1\leq 1$. 

--------------

### 1.1.5

(a) $\ln n<n$, so $\frac{1}{\ln n}>\frac{1}{n}>0$ for all positive integers $n$, and the harmonic series $\sum_{n=1}^\infty \frac{1}{n}$ diverging implies $\sum_{n=2}^\infty \frac{1}{\ln n}$ diverging.

(b) $\frac{(n+1)!}{10^{n+1}}/\frac{n!}{10^n}=\frac{n+1}{10}\geq 1$ for $n\geq 9$, so $\sum_{n=1}^\infty \frac{n!}{10^n}$ diverges by ratio test.

(c) $2n(2n+1)>(2n)^2$, so $0<\frac{1}{2n(2n+1)}<\frac{1}{(2n)^2}$. 
$\sum_{n=1}^\infty \frac{1}{4n^2}$ converges by integral test, so $\sum_{n=1}^\infty \frac{1}{2n(2n+1)}$ converges by comparison test.

(d) $\frac{1}{\sqrt{n(n+1)}}>\frac{1}{\sqrt{(n+1)^2}}=\frac{1}{n+1}>0$. Since $\sum_{n=1}^\infty \frac{1}{n+1}$ diverges by integral test, $\sum_{n=1}^\infty\[n(n+1)\]^{-\frac{1}{2}}$ diverges.

(e) $\int_0^\infty \frac{1}{2x+1}=\frac{1}{2}\ln(2n+1)\bigr\vert_0^\infty$ is infinite, so $\sum_{n=0}^\infty\frac{1}{2n+1}$ diverges by integral test.

--------------

### 1.1.6
(a) $0<\frac{1}{n(n+1)}<\frac{1}{n^2}$. Since $\sum_{n=1}^\infty\frac{1}{n^2}$ converges by integral test, $\sum_{n=1}^\infty \frac{1}{n(n+1)}$ converges by comparison test. 

(b) $\int_2^\infty \frac{1}{n\ln n}\,dx=\ln \ln n\vert_2^\infty$ is infinite, so $\sum_{n=2}^{\infty} \frac{1}{n\ln n}$ converges by integral test.

(c) $\frac{1}{(n+1)2^{n+1}}/\frac{1}{n2^n}=\frac{n}{n+1}\frac{1}{2}\leq \frac{1}{2}$ for all $n$, so $\sum_{n=1}^\infty \frac{1}{n\,2^n}$ converges by retio test.

(d) $\ln \frac{n+1}{n}=\ln (n+1)-\ln n$, so 

$$
\begin{aligned}
\sum_{n=1}^\infty \ln (1+\frac{1}{n})=(\ln2-\ln1)+(\ln3-\ln2)+\cdots=\lim_{n\to\infty} \ln n
\end{aligned}
$$

is infinite, which means $\sum_{n=1}^\infty \ln (1+\frac{1}{n})$ diverges.

(e) $n^{\frac{1}{n}}>1$. Let $x_n=n^{\frac{1}{n}}-1$, then $(1+x_n)^n=n$, and $\frac{n(n+1)}{2}x_n^2\leq n$ by binomial theorem. Therefore, $0\leq x_n \leq \sqrt{\frac{2}{n-1}}$, so $\lim_{n\to\infty}\sqrt{\frac{2}{n-1}}=0$ implies $\lim_{n\to\infty}x_n=0$, and $\lim_{n\to\infty}n^{\frac{1}{n}}=1$.

$\lim_{n\to\infty}n^{\frac{1}{n}}=1$ implies for sufficiently large $n$, $0=1-1<n^{\frac{1}{n}}<1+1=2$, so $\frac{1}{n^{\frac{1}{n}}}>\frac{1}{2}$, and $\frac{1}{n\cdot n^{\frac{1}{n}}}>\frac{1}{2n}$. Since $\sum_{n=1}^\infty \frac{1}{2n}$ diverges by integral test, $\sum_{n=1}^\infty \frac{1}{n\cdot n^{\frac{1}{n}}}$ diverges by comparison test.

--------------

### 1.1.7

If $a_1\geq a_2\geq a_3 \geq \cdots \geq 0$, then $\sum_{n=1}^\infty a_n$ converges if and only if $\sum_{k=1}^\infty2^ka_{2k}$ converges.

$$
\begin{aligned}
\sum_{k=1}^\infty 2^k \frac{1}{(2^k)^p(\ln 2^k)^q}=2^{(1-p)k}\frac{1}{k^q}\frac{1}{(\ln2)^q}
\end{aligned}
$$ 

If $p>1$, then $\sum_{k=1}^\infty \frac{1}{(2^{p-1})^k}\frac{1}{(\ln 2)^q}$ converges by ratio test, so $\sum_{k=1}^\infty 2^k \frac{1}{(2^k)^p(\ln 2^k)^q}$ converges, and $\sum_{n=2}^\infty \frac{1}{n^p(\ln n)^q}$ converges. 

If $p=1$, then $\sum_{k=1}^\infty 2^k \frac{1}{(2^k)^p(\ln 2^k)^q}=\frac{1}{k^q}\frac{1}{(\ln2)^q}$, which converges if $q>1$.

Therefore, if $p>1$, or $p=1$ and $q>1$, wh have $\sum_{n=2}^\infty \frac{1}{n^p(\ln n)^q}$ converges.

--------------

### 1.1.8

$$
\begin{aligned}
\gamma &= \lim_{n\to\infty}(\sum_{m=1}^n\frac{1}{m}-\ln n)=\sum_{m=1}^{1000}\frac{1}{m}+\lim_{n\to\infty}(\sum_{m=1001}^n\frac{1}{m}-\ln n)\\
\lim_{n\to\infty}n &= \sum_{m=1001}^\infty\ln \frac{m}{m-1}-\ln 1000\\
\gamma &= \sum_{m=1}^{1000}\frac{1}{m}-\ln{1000}+\sum_{m=1001}^\infty(\frac{1}{m}-\ln\frac{m}{m-1})\\
\int_{1001}^\infty(\frac{1}{x}-\ln\frac{x}{x-1})\,dx &\geq \sum_{m=1001}^\infty(\frac{1}{m}-\ln\frac{m}{m-1})\geq \int_{1001}^\infty(\frac{1}{x}-\ln\frac{x}{x-1})\,dx+(\frac{1}{1001}-\ln\frac{1001}{1000})\\
\int_{1001}^\infty(\frac{1}{x}-\ln\frac{x}{x-1})\,dx &= \left[\ln\frac{x}{x-1}+x\ln\frac{x-1}{x}\right]_{1001}^\infty=-0.000\,499\,667\\
\frac{1}{1001}-\ln\frac{1001}{1000} &= -0.000\,000\,499\\
\sum_{m=1}^{1000}\frac{1}{m}-\ln1000 &= 0.577\,714\,7\\
0.577\,715-0.000\,499 &> \gamma>0.577\,714-0.000\,500-0.000\,001\\
0.577\,213 &< \gamma<0.577\,216
\end{aligned}
$$ 

--------------

### 1.1.9

The number in each shell is proportional to $r^2$, but the solid angle of each shell is proportional to $\frac{1}{r^2}$, so the total solid angle occupied by stars in each shell is the same. Let it be $\omega_0$.

If the solid angle occupied by stars from shell 1 to n is $a_n$, then $a_{n+1}=a_n+a-a_n\cdot \frac{a}{4\pi}$, where $a_n\cdot \frac{a}{4\pi}$ is the solid angle of stars in shell $n+1$ that is blocked by stars in shell 1 to n. So $a_{n+1}-4\pi=(a_n-4\pi)(1-\frac{a}{4\pi})$, and $a_n=(a-4\pi)(1-\frac{a}{4\pi})^{n-1}+4\pi$. Therefore, $1-\frac{a}{4\pi}<1$, which means $\lim_{n\to\infty}a_n=4\pi$.

--------------

### 1.1.10

$$
\begin{aligned}
\frac{u_n}{u_{n+1}}=\left (\frac{2n+2}{2n+1} \right)^2=1+\frac{4n+3}{4n^2+4n+1}=1+\frac{1}{n}+\frac{B(n)}{n^2}
\end{aligned}
$$

where B(n) is bound for large n. By Gauss' test, 

$$
\begin{aligned}\sum_{n=1}^\infty\left[\frac{1\cdot3\cdot5\cdots(2n-1)}{2\cdot4\cdot6\cdots(2n)}\right]^2
\end{aligned}
$$ 

converges.

--------------

### 1.1.11

(a) $\frac{\ln n}{n}$ is monotonically decreasing, and $\lim_{n\to\infty}\frac{\ln n}{n}=0$, so the series converges by  Leibniz criterion. $\frac{\ln n}{n}\geq \frac{1}{n}$ when $n\geq 3$, and $\sum_{n=1}^\infty\frac{1}{n}$ diverges by integral test, so $\sum_{n=1}^\infty\frac{\ln n}{n}$ diverges by comparison test, so the series is not absolutely convergent.

(b)  The series $\frac{1}{1}-\frac{1}{3}+\frac{1}{5}-\cdots$ converges by Leibniz criterion, and so does the series  $\frac{1}{2}-\frac{1}{4}+\frac{1}{6}-\cdots$. So the series  $\frac{1}{1}+\frac{1}{2}-\frac{1}{3}-\frac{1}{4}+\frac{1}{5}+\frac{1}{6}\cdots$ is the sum of two convergent series, and is therefore convergent.
$\sum_{n=1}^\infty\frac{1}{n}$ diverges by integral test, so the series is not absolutely convergent.

(c) 
Combine adjacent terms with same sign to form a new series 

$$
\begin{aligned}
sum_{n=1}^\infty a_n=(1)-(\frac{1}{2}+\frac{1}{3})+(\frac{1}{4}+\frac{1}{5}+\frac{1}{6})-(\frac{1}{7}+\frac{1}{8}+\frac{1}{9}+\frac{1}{10})+\cdots
\end{aligned}
$$

where 

$$
\begin{aligned}
a_n &= \frac{1}{\frac{n^2-n}{2}+1}+\frac{1}{\frac{n^2-n}{2}+2}+\cdots+\frac{1}{\frac{n^2-n}{2}+n}\\
a_{n+1} &= \frac{1}{\frac{n^2+n}{2}+1}+\frac{1}{\frac{n^2+n}{2}+2}+\cdots+\frac{1}{\frac{n^2+n}{2}+n}+\frac{1}{\frac{n^2+n}{2}+n+1}
\begin{aligned}
$$

so $a_n$ has n terms and $a_{n+1}$ has $n+1$ terms.

$$
\begin{aligned}a_{n}-a_{n+1}=(\frac{1}{\frac{n^2-n}{2}+1}-\frac{1}{\frac{n^2+n}{2}+1})+(\frac{1}{\frac{n^2-n}{2}+2}-\frac{1}{\frac{n^2+n}{2}+2})+\cdots+(\frac{1}{\frac{n^2-n}{2}+n}-\frac{1}{\frac{n^2+n}{2}+n})-\frac{2}{n^2+3n+2}
\end{aligned}
$$

The $k^{st}$ term (except for the last term) of $a_{n}-a_{n+1}$ is

$$
\begin{aligned}
\frac{1}{\frac{n^2-n}{2}+k}-\frac{1}{\frac{n^2+n}{2}+k}\geq\frac{1}{\frac{n^2-n}{2}+n}-\frac{1}{\frac{n^2+n}{2}+n}=\frac{4}{n^3+4n^2+3n}
\end{aligned}
$$

so 

$$
\begin{aligned}
a_{n}-a_{n+1}\geq\frac{4}{n^3+4n^2+3n}\cdot n-\frac{2}{n^2+3n+2}=\frac{4}{n^2+4n+3}\cdot n-\frac{2}{n^2+3n+2}\geq0
\end{aligned}
$$

which means the sequence $a_n$ is monotonically decreasing.

$$
\begin{aligned}
0\leq a_n\leq\frac{1}{\frac{n^2-n}{2}}\cdot n=\frac{2}{n-1}
\end{aligned}
$$

so $\lim_{n\to\infty}a_n=0$ because $\lim_{n\to\infty}\frac{2}{n-1}=0$. Therefore, the series converges by Leibniz criterion.
$\sum_{n=1}^\infty\frac{1}{n}$ diverges by integral test, so the series is not absolutely convergent.

--------------

### 1.1.12

$$
\begin{aligned}
\beta(2) &= 1-\sum_{k=1}^\infty\frac{16k}{(16k^2-1)^2}=1-\sum_{k=1}^{40}\frac{16k}{(16k^2-1)^2}-\sum_{k=41}^\infty\frac{16k}{(16k^2-1)^2}\\
\int_{41}^\infty\frac{16x}{(16x^2-1)^2}\,dx &\leq \sum_{k=41}^\infty\frac{16k}{(16k^2-1)^2}\leq\int_{41}^\infty\frac{16x}{(16x^2-1)^2}\,dx\,+\frac{16\cdot 41}{(16\cdot 41^2-1)^2}\\
1-\sum_{k=1}^{40}\frac{16k}{(16k^2-1)^2} &= 0.915\,984\,644\\
\int_{41}^\infty\frac{16x}{(16x^2-1)^2}\,dx &= \frac{-1}{2(16x^2-1)}\Big|_{41}^\infty=0.000\,018\,591\\
\frac{16\cdot 41}{(16\cdot 41^2-1)^2} &= 0.000\,000\,907\\
0.915965146 &\leq \beta(2)\leq0.915966053
\end{aligned}
$$

So $\beta(2)=0.915966$ (to six-digit accuracy).

--------------

### 1.1.13

$$
\begin{aligned}
\zeta(2)+a\alpha_1+b\alpha_2 &= \sum_{n=1}^\infty(\frac{1}{n^2}+\frac{a}{n(n+1)}+\frac{b}{n(n+1)(n+2)})=\frac{(1+a)n^2+(3+2a+b)n+2}{n^2(n+1)(n+2)}\\
\zeta(2)-\alpha_1-\alpha_2 &= \frac{2}{n^2(n+1)(n+2)}
\end{aligned}
$$

--------------

### 1.1.14

$$
\begin{aligned}
\sum_{n=0}^\infty \frac{1}{(2n+1)^3}+\sum_{n=1}^\infty\frac{1}{(2n)^3}=\sum_{n=1}^\infty\frac{1}{n^3}\\
\lambda(3) &= \sum_{n=1}^\infty\frac{1}{n^3}-\sum_{n=1}^\infty\frac{1}{(2n)^3}=\frac{7}{8}\sum_{n=1}^\infty\frac{1}{n^3}=\frac{7}{8}\zeta(3)\\
\lambda(3) &= 1.051800
\end{aligned}
$$

to six decimal place.

--------------

### 1.1.15

(a) 

$$
\begin{aligned}
\sum_{n=2}^\infty[\zeta(n)-1]=\sum_{n=2}^\infty(\sum_{k=1}^\infty\frac{1}{k^n}-1)=\sum_{n=2}^\infty\sum_{k=2}^\infty\frac{1}{k^n}=\sum_{k=2}^\infty\sum_{n=2}^\infty\frac{1}{k^n}=\sum_{k=2}^\infty\frac{\frac{1}{k^2}}{1-\frac{1}{k}}=\sum_{k=2}^\infty(\frac{1}{k-1}-\frac{1}{k})=1
\end{aligned}
$$

(b) 

$$
\begin{aligned}
\sum_{n=2}^\infty(-1)^n[\zeta(n)-1]=\sum_{n=2}^\infty(-1)^n(\sum_{k=1}^\infty\frac{1}{k^n}-1)=\sum_{n=2}^\infty(-1)^n\sum_{k=2}^\infty\frac{1}{k^n}=\sum_{k=2}^\infty\sum_{n=2}^\infty(-1)^n\frac{1}{k^n}
\end{aligned}
$$

$$
\begin{aligned}
=\sum_{k=2}^\infty\frac{\frac{1}{k^2}}{1-(-\frac{1}{k})}=\sum_{k=2}^\infty(\frac{1}{k}-\frac{1}{k+1})=\frac{1}{2}
\end{aligned}
$$

--------------

### 1.1.16

(a) 

$$
\begin{aligned}
\zeta(3)-\alpha_2' &= 1+\sum_{n=1}^\infty(\frac{1}{n^3}-\frac{1}{(n-1)n(n+1)})=1+\sum_{n=2}^\infty\frac{-1}{(n-1)n^3(n+1)}\\
\zeta(3) &= \frac{5}{4}-\sum_{n=2}^\infty\frac{1}{n^3(n^2-1)}
\end{aligned}
$$

(b) 

$$
\begin{aligned}
\zeta(3)+\alpha_4' &= \frac{5}{4}-\sum_{n=2}^\infty\frac{1}{(n-1)n^3(n+1)}+\sum_{n=3}^\infty\frac{1}{(n-2)(n-1)n(n+1)(n+2)}\\
&= \frac{29}{24}+\sum_{n=3}^\infty\frac{4}{(n-2)(n-1)n^3(n+1)(n+2)}\\
\zeta(3) &= \frac{115}{96}+\sum_{n=3}^\infty\frac{4}{(n-2)(n-1)n^3(n+1)(n+2)}
\end{aligned}
$$

(c) 

$$
\begin{aligned}
\int_{N}^\infty\frac{1}{x^3}\,dx\leq\sum_{n=N}^\infty\frac{1}{n^3}\leq\int_{N}^\infty\frac{1}{x^3}\,dx+\frac{1}{N^3}
\end{aligned}
$$

$\frac{1}{126^3}=4.999\times10^{-7}<5\times10^{-7}$, so 125 terms are required.

$$
\begin{aligned}
\int_{N}^\infty\frac{1}{x^3(x^2-1)}\,dx\leq\sum_{n=N}^\infty\frac{1}{n^3(n^2-1)}\leq\int_{N}^\infty\frac{1}{x^3(x^2-1)}\,dx+\frac{1}{N^3(N^2-1)}
\end{aligned}
$$

$\frac{1}{19^3(19^2-1)}=4\times10^{-7}<5\times10^{-7}$, so 17 terms ($n=2$ to $n=18$) are required.

$$
\begin{aligned}
\int_{N}^\infty\frac{4}{x^3(x^2-1)(x^2-4)}\,dx\leq\sum_{n=N}^\infty\frac{1}{n^3(n^2-1)(n^2-4)}\leq\int_{N}^\infty\frac{4}{x^3(x^2-1)(x^2-4)}\,dx+\frac{4}{N^3(N^2-1)(N^2-4)}
\end{aligned}
$$

$\frac{4}{10^3(10^2-1)(10^2-4)}=4.2\times10^{-7}<5\times10^{-7}$, so 7 terms ($n=3$ to $n=9$) are required.


## 1.2 Series of Functions

## 1.2.1

(a) When $x>0$, $\lim_{n\to\infty}\frac{(-1)^{n-1}}{n^x}=0$, and the sequence $\frac{1}{n^x}$ is monotonically decreasing, so by Leibniz criterion, $\sum_{n=1}^\infty\frac{(-1)^{n-1}}{n^x}$ converges. 
When $x\leq0$, $\lim_{n\to\infty}\frac{(-1)^{n-1}}{n^x}\neq0$, so $\sum_{n=1}^\infty\frac{(-1)^{n-1}}{n^x}$ diverges. 
Therefore, the series converges for $x>0$, and if the series uniformly converges in the interval $[a,b]$, then $0<a<b$.

For $x\in[a,b]$, $0<a<b$,

$$
\begin{aligned}
|S(x)-s_n(x)|=|\sum_{k=n+1}^\infty\frac{(-1)^{k-1}}{k^x}|\leq\frac{1}{(n+1)^x}<\frac{1}{n^x}<\frac{1}{n^a}
\end{aligned}
$$

For any $\epsilon>0$, let $N=(\frac{1}{\epsilon})^{\frac{1}{a}}+1$, then 

$$
\begin{aligned}
|S(x)-s_n(x)|<\frac{1}{n^a}<\frac{1}{N^a}=\epsilon
\end{aligned}
$$

for all $n\geq N$, so the series is uniformly convergent in the range $[a,b]$ if $0<a<b$.

(b) The series converges when $x>1$ and diverges when $x\leq 1$ by integral test, so if it uniformly converges in interval $[a,b]$, then $1<a<b$.
For $x\in[a,b]$ and $1<a<b$,
$|\frac{1}{n^x}|\leq\frac{1}{n^a}$. $\sum_n \frac{1}{n^a}$ is a convergent series, so by Weierstrass M test,  $\sum_{n=1}^\infty\frac{1}{n^x}$ is uniformly convergent in the range $[a,b]$ if $1<a<b$.

--------------

## 1.2.2

The series converges when $\vert x\vert <1$ and diverges when $\vert x\vert \geq1$. If it uniformly converges in the interval $[a,b]$, then $-1<a<b<1$. For $x\in [a,b]$ and $-1<a<b<1$, let $c=\max(\vert a\vert ,\vert b\vert )$, then $vert x^n\vert \leq x^c$. Because $c<1$, so $\sum_{n=0}^\infty x^c$ converges, so by Weietress M test, $\sum_{n=0}^\infty x^n$ uniformly converges in the range $[a,b]$ if $-1<a<b<1$. 

--------------

## 1.2.3

(a) When $0<x\leq1$, $\lim_{n\to\infty}\frac{1}{1+x^n}\neq0$, so the series diverges. When $x>1$, $0<\frac{1}{1+x^n}<\frac{1}{x^n}$. The geometry series $\frac{1}{x^n}$ converges, so $\sum_{n=0}^\infty\frac{1}{1+x^n}$ converges by comparison test.

(b) If the series is uniformly convergent in the interval $[a,b]$, then $1<a<b$. For $x\in [a,b]$ and $1<a<b$, $\frac{1}{1+x^n}<\frac{1}{x^n}\leq\frac{1}{a^n}$. The geometry series $\sum_{n=0}^\infty\frac{1}{a^n}$ converges, so by Weierstrass M test, $\sum_{n=0}^\infty\frac{1}{1+x^n}$ is uniformly convergent in the range $[a,b]$ if $1<a<b$.

--------------

## 1.2.4

For $x\in[a,b]$, $\vert a_n\cos nx+b_n\sin nx\vert \leq|a_n|+|b_n|$. $\sum\vert a_n\vert $ and $\sum\vert b_n\vert$ converges, so $\sum(\vert a_n\vert +\vert b_n\vert )$ converges, so $\sum(a_n\cos nx+b_n\sin nx)$ is uniformly convergent by Weierstrass M test in the range $[a,b]$ for any $a<b$.

--------------

## 1.2.5

Let $j=2n$, $a_n(x)=u_{2n}(x)$, then $a_{n+1}(x)=\frac{(2n+1)(2n+2)-l(l+1)}{(2n+2)(2n+3)}x^2a_n(x)$. Since
$\lim_{n\to\infty}\frac{a_{n+1}(x)}{a_n(x)}=x^2>1$ when $|x|>1$ and $\lim_{n\to\infty}\frac{a_{n+1}(x)}{a_n(x)}<1$ when $|x|<1$, by ratio test the series diverges when $|x|>1$ and converges when $|x|<1$. When $x=1$,

$$
\begin{aligned}
\frac{a_n}{a_{n+1}}=\frac{4n^2+10n+6}{4n^2+6n+2-l(l+1)}=1+\frac{4n+4+l(l+1)}{4n^2+6n+2-l(l+1)}=1+\frac{1}{n}+\frac{B(n)}{n^2}
\end{aligned}
$$

where $B(n)$ is bound for large n. By Gauss' test, the series diverges when $x=1$, so the range of convergence is $-1<x<1$.

--------------

## 1.2.6

Let $j=2m$, $a_m(x)=u_{2m}(x)$. When $x=\pm1$, we have $\frac{a_m(x)}{a_{m+1}(x)}=1+\frac{3}{2m}+\frac{B(m)}{m^2}$, where $B(m)$ is bound for large m. By Gauss' test, the series converges at $x=\pm1$.

--------------

## 1.2.7

Let $j=2m$, $u_m=a_{2m}$, then 

$$
\begin{aligned}
\frac{u_m}{u_{m+1}}=\frac{4m^2+(4k+6)m+(k+1)(k+2)}{4m^2+(4k+4\alpha)m+k(k+2\alpha)-n(n+2\alpha)}=1+\frac{6-4\alpha}{4m}+\frac{B(m)}{m^2}
\end{aligned}
$$

where $B(m)$ is bound for large m. By Gauss' test, the series converges $\alpha<\frac{1}{2}$ and diverges when $\alpha\geq\frac{1}{2}$.

--------------

## 1.2.8

$$
\begin{aligned}
\sin x &= \sum_{n=0}^\infty\frac{x^n}{n!}\left(\frac{d^n\sin{x}}{dx^n}\Big|_{x=0}\right)=\sum_{k=0}^\infty\frac{x^{2k}}{(2k)!}(-1)^k\sin{0}+\sum_{k=0}^\infty\frac{x^{2k+1}}{(2k+1)!}(-1)^k\cos{0}=\sum_{n=0}^\infty(-1)^n\frac{x^{2n+1}}{(2n+1)!}\\
\cos x &= \sum_{n=0}^\infty\frac{x^n}{n!}\left(\frac{d^n\cos{x}}{dx^n}\Big|_{x=0}\right)=\sum_{k=0}^\infty\frac{x^{2k}}{(2k)!}(-1)^k\cos{0}+\sum_{k=0}^\infty\frac{x^{2k+1}}{(2k+1)!}(-1)^{k+1}\sin{0}=\sum_{n=0}^\infty(-1)^n\frac{x^{2n}}{(2n)!}
\end{aligned}
$$

--------------

## 1.2.9

Expand $\sin{x}$ and $\cos{x}$ for 4 terms, and perform long division.

![image tooltip here](/files/math_physics_ch1_pic1.png)

So $\cot{x}=\frac{1}{x}-\frac{x}{3}-\frac{x^3}{45}-\frac{2x^5}{945}+\cdots$.

--------------

## 1.2.10

$$\frac{d}{dx}\coth^{-1}x=\frac{1}{1-x^2}=\frac{d}{dx}\left(\frac{1}{2}\ln\frac{x+1}{x-1}\right)=\frac{1}{1-x^2}$$

So 

$$\frac{d^n}{dx^n}\coth^{-1}x=\frac{d^n}{dx^n}\left(\frac{1}{2}\ln\frac{x+1}{x-1}\right)$$

and 

$$\sum_{n=0}^\infty\frac{x^n}{n!}\frac{d^n}{dx^n}\coth^{-1}x=\sum_{n=0}^\infty\frac{x^n}{n!}\frac{d^n}{dx^n}\left(\frac{1}{2}\ln\frac{x+1}{x-1}\right)$$

Therefore, $\coth^{-1}x=\frac{1}{2}\ln\frac{x+1}{x-1}$.

--------------

## 1.2.11

(a) $\frac{d}{dx}x^{\frac{1}{2}}=\frac{1}{2}x^{-\frac{1}{2}}$ is undefined at $x=0$, so Maclaurin expansion does not exist.

(b) 

$$x^{\frac{1}{2}}=\sum_{n=0}^\infty\frac{(x-x_0)^n}{n!}\frac{d^n}{dx^n}x^{\frac{1}{2}}=\sum_{n=0}^\infty u_n(x)$$

$$\lim_{n\to\infty}\frac{u_{n+1}(x)}{u_n(x)}= \lim_{n\to\infty}\left|\frac{(x-x_0)^{n+1}}{(n+1)!}\frac{d^{n+1}}{dx^{n+1}}x^{\frac{1}{2}}\Big/\frac{(x-x_0)^n}{n!}\frac{d^n}{dx^n}x^{\frac{1}{2}}\right|=\lim_{n\to\infty}\left|\frac{x-x_0}{x_0}\frac{2n-1}{2n+2} \right|<1$$ 

when $|x-x_0|<x_0$, so the series converges when $|x-x_0|<x_0$. When $x=0$, all the terms are less than 0, and

$$\frac{u_{n}(x)}{u_{n+1}(x)}=\frac{2n+2}{2n-1}=1+\frac{2}{2n-1}=1+\frac{1}{n}+\frac{B(n)}{n^2}$$ 

where B(n) is bound for large n, so the series diverges by Gauss' test.
When $x=2x_0$, $\sum_{n=0}^\infty u_n(x)$ is an alternating series, and $\lim_{n\to\infty}u_n(x)=0$, so the series converges by Leibniz criterion.
Therefore, the range of convergence is $0<x\leq 2x_0$.

--------------

## 1.2.12

$$\lim_{x\to x_0}\frac{f(x)}{g(x)}=\lim_{x\to x_0}\frac{f(x_0)+(x-x_0)f'(x_0)+\sum_{n=2}^{\infty}a_n(x-x_0)^n}{g(x_0)+(x-x_0)g'(x_0)+\sum_{n=2}^{\infty}b_n(x-x_0)^n}$$

When $f(x_0)=g(x_0)=0$, 

$$\lim_{x\to x_0}\frac{f(x)}{g(x)}=\lim_{x\to x_0}\frac{(x-x_0)f'(x_0)+\sum_{n=2}^{\infty}a_n(x-x_0)^n}{(x-x_0)g'(x_0)+\sum_{n=2}^{\infty}b_n(x-x_0)^n}=\lim_{x\to x_0}\frac{f'(x_0)+\sum_{n=1}^\infty c_n(x-x_0)^n}{g'(x_0)}=\lim_{x\to x_0}\frac{f'(x)}{g'(x)}$$

by binomial theorem.

--------------

## 1.2.13

(a) 

$$\frac{1}{n}-\ln{\frac{n}{n-1}}=\frac{1}{n}+\ln{\frac{n-1}{n}}=\frac{1}{n}+
\ln{(1-\frac{1}{n})}=\frac{1}{n}-\sum_{k=1}^\infty(\frac{1}{n})^k=-\sum_{k=2}^\infty(\frac{1}{n})^k<0$$

(b) 

$$\frac{1}{n}-\ln{\frac{n+1}{n}}=\frac{1}{n}-\ln{(1+\frac{1}{n})}=\frac{1}{n}-\sum_{k=1}^\infty(-1)^{k+1}(\frac{1}{n})^k=\sum_{k=2}^\infty(-1)^k(\frac{1}{n})^k>0$$

Euler-Mascheroni constant:

$$\gamma=\lim_{n\to\infty}\left(\sum_{k=1}^n\frac{1}{k}-\ln{n}\right)=1+\sum_{n=2}^\infty(\frac{1}{n}-\ln{\frac{n}{n-1}})<1$$

$$\gamma=1+\sum_{n=2}^\infty(\frac{1}{n}-\ln{\frac{n}{n-1}})=1+\sum_{n=1}^\infty(\frac{1}{n+1}-\ln{\frac{n+1}{n}})=1-1+\sum_{n=1}^\infty(\frac{1}{n}-\ln{\frac{n+1}{n}})+\lim_{n\to\infty}\frac{1}{n+1}>0$$

So the Euler-Mascheroni constant $\gamma$ is bound by 0 and 1, and is therefore finite.

--------------

## 1.2.14

$$\psi(x\pm h)=\psi(x)\pm h\psi'(x)+\frac{h^2}{2}\psi''(x)\pm \frac{h^3}{6}\psi^{(3)}(x)+\frac{h^4}{24}\psi^{(4)}(x)+\cdots$$

$$\frac{1}{h^2}\left[\psi(x+h)-2\psi(x)+\psi(x-h)\right]=\psi''(x)+\frac{h^2}{12}\psi^{(4)}(x)+\cdots$$

So the error is $\frac{h^2}{12}\psi^{(4)}(x)$.

--------------

## 1.2.15

$\sin{x}=x-\frac{x^3}{6}+\frac{x^5}{120}-\frac{x^7}{5040}+\cdots$, and $\tan{x}=x+\frac{x^3}{3}+\frac{2x^5}{15}+\frac{7x^7}{315}+\cdots$ (expansion of $\tan{x}$ can be obtained by long division of expansions of $\sin{x}$ and $\cos{x}$).
The term of highest order in $(\sin{(\tan{x})}-\tan{(\sin{x})})$ is $x^7$, the coefficient is 

$$\left\{\left[\frac{7}{315}-\frac{1}{6}\left(3\times\frac{2}{15}+3\times\frac{1}{3^2}\right)+\frac{1}{120}\left(5\times\frac{1}{3}\right)-\frac{1}{5040}\right]-\left[-\frac{1}{5040}+\frac{1}{3}\left(3\times\frac{1}{120}+3\times\frac{1}{36}\right)+\frac{2}{15}\left(5\times\frac{-1}{6}+\frac{7}{315} \right)\right]\right\}x^7$$

$$\lim_{x\to\infty}\left[\frac{\sin{(\tan{x})}-\tan{(\sin{x})}}{x^7} \right]=-\frac{1}{30}$$

--------------

## 1.2.16

If the convergence ranges of the series $\sum_{n=0}^\infty a_n x^n$ is $-R<x<R$, then $\lim_{n\to\infty}\left|\frac{a_n+1}{a_n}R\right|=1$. The differentiated series is $\sum_{n=1}^\infty na_nx^{n-1}$, $\lim_{n\to\infty}\left|\frac{n+1}{n}\frac{a_n+1}{a_n}x\right|=\lim_{n\to\infty}\left|\frac{a_n+1}{a_n}x\right|<1$ when $-R<x<R$ (ignoring the end points). The integrated series is $\sum_{n=0}^\infty\frac{a_n}{n+1}x^{n+1}$, $\lim_{n\to\infty}\left|\frac{n+1}{n+2}\frac{a_n+1}{a_n}x\right|=\lim_{n\to\infty}\left|\frac{a_n+1}{a_n}x\right|<1$ when $-R<x<R$ (ignoring the end points). So all the series have the same converging range (ignoring the end points).

## 1.3 Binomial Theorem

### 1.3.1

$$P(x)=c\left(\frac{\cosh{x}}{\sinh(x)}-\frac{1}{x} \right)=c\frac{(1+\frac{x^2}{2}+\frac{x^4}{24}+\cdots)-(1+\frac{x^3}{6}+\frac{x^4}{120})}{x+\frac{x^3}{6}+\frac{x^5}{120}+\cdots}=c\frac{\frac{x}{3}+\frac{x^3}{30}+\cdots}{1+\frac{x^2}{6}+\cdots}$$

$$=c(\frac{x}{3}+\frac{x^3}{30}+\cdots)(1-\frac{x^2}{6}+\cdots)=c\left(\frac{x}{3}-\frac{x^3}{45}+\cdots\right)$$

--------------

### 1.3.2

By binomial theorem, $\frac{1}{1-x^2}=\sum_{n=0}^\infty(-1)^n x^{2n}$, so $\int_0^1\frac{1}{1+x^2}dx=\sum_{n=0}^\infty(-1)^n\frac{x^{2n+1}}{2n+1}$. At $x=1$, $\lim_{n\to\infty}(-1)^n x^{2n}\neq 0$, so the series diverges; $\lim_{n\to\infty}\frac{x^{2n+1}}{2n+1}=0$ and the sequence $\frac{x^{2n+1}}{2n+1}$ is monotonically decreasing, so by Leibniz criterion the series converges. 

--------------

### 1.3.3

$e^{-t}t^n=\sum_{p=0}^\infty\frac{(-t)^p}{p!}t^n$. When $-a\leq t\leq a$ \,($a>0$), we have $\left|\frac{(-t)^p}{p!}t^n\right|\leq\frac{a^{p+n}}{p!}$ and $\sum_{p=0}^\infty\frac{a^{p+n}}{p!}$ is convergent, so by Weierstrass M test $\sum_{p=0}^\infty\frac{(-t)^p}{p!}t^n$ is uniformly convergent in $-a\leq t\leq a$ for every $a>0$, and the series can be integrated by terms.

\[\int_0^x e^{-t}t^n dt=\int_0^x\sum_{p=0}^\infty\frac{(-t)^p}{p!}t^n=\sum_{p=0}^\infty\int_0^x(-1)^p\frac{t^{n+p}}{p!}dt=\sum_{p=0}^\infty(-1)^p\frac{x^{n+p+1}}{p!(n+p+1)}\]
For $-a\leq x\leq a$\,($a>0$), the integrated series converges by Leibniz criterion, so the range of convergence is $-a\leq t\leq a$ for every $a>0$. 

--------------

### 1.3.4

(a) $x=\sinh{y}=\frac{e^y-e^{-y}}{2}=y+\frac{y^3}{6}+\frac{y^5}{120}+\cdots$. Because x in terms of y has only terms of odd orders, y in terms of x can only has terms of odd orders too. Let $y=a_1x+a_3x^3+a_5x^5+\cdots$, substituting into $x=y+\frac{y^3}{6}+\frac{y^5}{120}+\cdots$, obtaining $x=a_1x+(a_3+\frac{a_1^3}{6})x^3+(a_5+\frac{a_1^2a_3}{2}+\frac{a_1^5}{120})x^5+\cdots$, so $a_1=1$, $a_3=-\frac{1}{6}$, $a_5=\frac{3}{40}$. Therefore  $\sinh^{-1}x=x-\frac{x^3}{6}+\frac{3x^5}{40}+\cdots$.
\medskip

(b) $\frac{d}{dx}\sinh^{-1}x=(x^2+1)^{-1/2}$, $\frac{d^2}{dx^2}\sinh^{-1}x=-x(x^2+1)^{-3/2}$, $\frac{d^3}{dx^3}\sinh^{-1}x=-(x^2+1)^{-3/2}+3x^2(x^2+1)^{-5/2}$, $\frac{d^4}{dx^4}\sinh^{-1}x=9x(x^2+1)^{-5/2}-15x^3(x^2+1)^{-7/2}$, $\frac{d^5}{dx^5}\sinh^{-1}x=9(x^2+1)^{-5/2}-90x^2(x^2+1)^{-7/2}+105x^4(x^2+1)^{-9/2}$. So $\sinh^{-1}x=\sum_{n=0}^\infty\frac{x^n}{n!}\frac{d^n}{dx^n}\sinh^{-1}x=x-\frac{x^3}{6}+\frac{3x^5}{40}+\cdots$.

--------------

### 1.3.5

$$\frac{1}{(1-x)^{n+1}}=\sum_{m=0}^\infty\binom{-(n+1)}{m}(-x)^m=\sum_{m=0}^\infty\frac{(n+m)!}{m!n!}x^m=\sum_{m'=n}^\infty\frac{m'!}{(m'-n)!n!}x^{m'-n}=\sum_{m=n}^\infty\binom{m}{n}x^{m-n}$$

In the third equal sign we use a substitution $m'=m+n$.

--------------

### 1.3.6

$$(1+x)^{-\frac{m}{2}}=\sum_{n=0}^\infty\binom{-\frac{m}{2}}{n}x^n=\sum_{n=0}^\infty\frac{(-1)^n\frac{(m+2n-2)!!}{2^n (m-2)!!}}{n!}=\sum_{n=0}^\infty(-1)^n\frac{(m+2n-2)!!}{2^n n!(m-2)!!}$$

--------------

### 1.3.7

(a) $\nu'=\nu(1\pm \frac{v}{c}+(\frac{v}{c})^2+\cdots) $

(b) $\nu'=\nu(1\pm \frac{v}{c})$

(c) $\nu'=\nu(1\pm\frac{v}{c}+\frac{1}{2}(\frac{v}{c})^2)+\cdots$

--------------

### 1.3.8

(a) $v_1=c(\delta+\frac{1}{2}\delta^2)$

(b) $v_2=c\delta(1+\frac{1}{2}\delta)(1-2\delta+\cdots)=c(\delta-\frac{3}{2}\delta^2+\cdots)$

(c) Solve for $v_3$, obtaining $v_3=c\frac{\delta^2+2\delta}{2+2\delta+\delta^2}=c\delta(1+\frac{\delta}{2})(1-\delta\cdots)=c(\delta-\frac{1}{2}\delta^2+\cdots)$

--------------

### 1.3.9

$$\frac{w}{c}=\frac{2(1-\alpha)}{1+(1-\alpha^2)}\frac{1-\alpha}{1-\alpha+\frac{\alpha^2}{2}}=(1-\alpha)\left[1-(-\alpha+\frac{\alpha^2}{2})+(-\alpha+\frac{\alpha^2}{2})^2-(-\alpha+\frac{\alpha^2}{2})^3+\cdots\right]$$

$$=(1-\alpha)(1+\alpha+\frac{\alpha^2}{2}+\cdots)=1-\frac{\alpha^2}{2}-\frac{\alpha^3}{2}+\cdots$$

--------------

### 1.3.10

$$x=\frac{c^2}{g}\left\{ 1+\frac{1}{2}\left(g\frac{t}{c}\right)-\frac{1}{8}\left(g\frac{t}{c}\right)^4+\frac{1}{16}\left(g\frac{t}{c}\right)^6-\cdots \right\}=\frac{1}{2}gt^2-\frac{1}{8}\frac{g^3t^4}{c^2}+\frac{1}{16}\frac{g^5t^6}{c^4}-\cdots$$

--------------

### 1.3.11

$$\frac{\gamma^2}{(s+n-|k|^2)^2}=\frac{\gamma^2}{\left(n+|k|(1-\frac{1}{2}\frac{\gamma^2}{|k|^2}+\cdots-1)\right)^2}=\frac{\gamma^2}{n^2(1-\frac{\gamma^2}{2n|k|})^2+\cdots}=\frac{\gamma^2}{n^2}(1+\frac{\gamma^2}{n|k|}+\cdots)=\frac{\gamma^2}{n^2}+\frac{\gamma^4}{n^3|k|}+\cdots$$

$$
\begin{aligned}
E &= mc^2\left[1-\frac{1}{2}\left(\frac{\gamma^2}{n^2}+\frac{\gamma^4}{n^3|k|}+\cdots\right)+\frac{3}{8}\left(\frac{\gamma^2}{n^2}+\frac{\gamma^4}{n^3|k|}+\cdots\right)^2 +\cdots\right]\\
 &= mc^2\left[1-\frac{1}{2}\frac{\gamma^2}{n^2}+(\frac{3}{8}-\frac{n}{2|k|})\frac{\gamma^4}{n^4}+\cdots \right]
\end{aligned}
$$

--------------

### 1.3.12

(a)

$$R=\frac{2mc^2(1+\frac{E_k}{2mc^2})^{1/2}-2mc^2}{E_k}=\frac{\frac{1}{2}E_k+\cdots}{E_k}\approx \frac{1}{2}$$

(b)

$$R=\sqrt{\frac{2mc^2(E_k+2mc^2)}{E_k^2}}-\frac{2mc^2}{E_k}\approx0$$

--------------

### 1.3.13

The first series converges for $|x|<1$, and the second series converges for $|x^{-1}|<1$, that is, $|x|>1$. The ranges of convergence of the two series do not overlap, so when adding together to get $\sum_{n=-\infty}^\infty x^n$, nowhere can the series converge.
--------------

### 1.3.14

(a) By binomial theorem, when $|x|<1$,
$$\frac{1}{1-x}=\sum_{n=0}^\infty\binom{-1}{n}(-x)^n=\sum_{n=0}^\infty x^n$$

$$\frac{x}{(1-x)^2}=x\sum_{n=0}^\infty\binom{-2}{n}(-x)^n=x\sum_{n=0}^\infty(n+1)x^n=\sum_{n=1}^\infty nx^n$$

$$\langle \varepsilon \rangle=\frac{\varepsilon_0 e^{\frac{-\varepsilon_0}{kT}}}{(1-\frac{-\varepsilon_0}{kT})^2}\Big/ \frac{1}{1-\frac{-\varepsilon_0}{kT}}==\frac{\varepsilon_0}{e^{\frac{\varepsilon_0}{kT}}-1}$$

(b)

$$\langle \varepsilon \rangle=\frac{\varepsilon_0}{1+\frac{\varepsilon_0}{kT}+\cdots-1}\approx kT$$

--------------

### 1.3.15

$$\tan^{-1}x=\int_{0}^x\frac{dt}{1+t^2}=\int_0^\infty\sum_{n=0}^\infty(-1)^n t^{2n}=\sum_{n=0}^\infty(-1)^n\frac{x^{2n+1}}{2n+1}$$

When $-a<t<a$ and $0<a<1$, the series $\sum_{n=0}^\infty (-1)^n t^{2n}$ is uniformly convergent by Weierstrass M test, so the series can be integrated by term. 

--------------

### 1.3.16

$$\frac{2+2\varepsilon}{1+2\varepsilon}=2(1+\varepsilon)(1-2\varepsilon+4\varepsilon^2-\cdots)=2-2\varepsilon+4\varepsilon^2-\cdots$$

$$\frac{\ln(1+2\varepsilon)}{\varepsilon}=\frac{2\varepsilon-\frac{4\varepsilon^2}{2}+\frac{8\varepsilon^3}{3}-\cdots}{\varepsilon}=2-2\varepsilon+\frac{8}{3}\varepsilon^2-\cdots$$

$$\lim_{n\to\infty}f(\varepsilon)=\lim_{n\to\infty}\frac{(1+\varepsilon)}{\varepsilon^2}\left(\frac{4}{3}\varepsilon^2+\cdots\right)=\frac{4}{3}$$

--------------

### 1.3.17

$$
\begin{aligned}
\xi_1 &= 1+\frac{A^2(1-2A^{-1}+A^{-2})}{2A}\left[-(A^{-1}+\frac{A^{-2}}{2}+\frac{A^{-3}}{3}+\frac{A^{-4}}{4}+\cdots )-(A^{-1}-\frac{A^{-2}}{2}+\frac{A^{-3}}{3}-\frac{A^{-4}}{4}+\cdots ) \right]\\
 &= 1+\frac{A}{2}(1-2A^{-1}+A^{-2})(-2A^{-1}-\frac{2}{3}A^{-3}-\cdots)=2A^{-1}-\frac{4}{3}A^{-2}+\frac{2}{3}A^{-3}+\cdots\\
\xi_2 &= \frac{2}{A}(1+\frac{2}{3}A^{-1})^{-1}=2A^{-1}(1-\frac{2}{3}A^{-1}+\frac{4}{9}A^{-2}-\cdots)=2A^{-1}-\frac{4}{3}A^{-2}+\frac{8}{9}A^{-3}+\cdots 
\end{aligned}

--------------

### 1.3.18

(a) 

$$\arctan{x}=\int_0^\infty\frac{1}{1+t^2}dt=\int_0^\infty\sum_{k=0}^\infty(-1)^k t^{2k}dt=\sum_{k=0}^\infty\frac{x^{2k+1}}{2k+1}$$

(In exercise 1.3.15 we have verified that this series expansion is valid in $-a\leq x\leq a$ for $0<a<1$).

$$\int_{0}^1\arctan{t}\frac{dt}{t}=\int_0^1\sum_{n=0}^\infty\frac{t^{2k}}{2k+1}dt=\sum_{k=0}^\infty(-1)^k\frac{1}{(2k+1)^2}$$

which is the Catalan's constant.

(b) Integrating by parts, 

$$-\int_0^1\ln{x}\frac{dx}{1+x^2}=-\left[(\ln{x})\arctan{x}\Big|_0^1-\int_0^1\frac{1}{x}\arctan{x}dx \right]=\int_0^1\arctan{x}\frac{dx}{x}$$

which is the same with (a).

## 1.4 Mathematical Induction

### 1.4.1

If the equation holds for $n=k-1$, then  $\sum_{j=1}^{k-1}j^4=\frac{k-1}{30}(2k-1)(k)(3k^2-3k-1)=\frac{k^5}{5}-\frac{k^4}{2}+\frac{k^3}{3}-\frac{k}{30}$, and $\sum_{j=1}^{k}j^4=\sum_{j=1}^{k-1}j^4+k^4=\frac{k^5}{5}+\frac{k^4}{2}+\frac{k^3}{3}-\frac{k}{30}=\frac{k}{30}(2k+1)(k+1)(3k^2+3k-1)$. $\sum_{j=1}^1j^4=1=\frac{1}{30}(2+1)(1+1)(3+3-1)$. The equation holds for $n=1$, and if it holds for $n=k-1$ then it will holds for $n=k$, so the equation holds for all positive integers by mathematical induction.

--------------

### 1.4.2

If $(\frac{d}{dx})^n[f(x)g(x)]=\sum_{j=0}^n\binom{n}{j}\left[(\frac{d}{dx})^jf(x) \right]\left[(\frac{d}{dx})^{n-j}g(x) \right]$, then

$$
\begin{aligned}
\left(\frac{d}{dx} \right)^{n+1}\left[f(x)g(x) \right] &= \sum_{j=0}^n\binom{n}{j}\left[\left(\frac{d}{dx} \right)^{j+1}f(x) \right]\left[\left(\frac{d}{dx} \right)^{n-j}g(x) \right]
+\sum_{j=0}^n\binom{n}{j}\left[\left(\frac{d}{dx} \right)^{j}f(x) \right]\left[\left(\frac{d}{dx} \right)^{n-j+1}g(x) \right]\\
 &= \sum_{j=1}^{n+1}\binom{n}{j-1}\left[\left(\frac{d}{dx} \right)^{j}f(x) \right]\left[\left(\frac{d}{dx} \right)^{n+1-j}g(x) \right]
+\sum_{j=0}^n\binom{n}{j}\left[\left(\frac{d}{dx} \right)^{j}f(x) \right]\left[\left(\frac{d}{dx} \right)^{n+1-j}g(x) \right]\\
 &=\sum_{j=1}^n\binom{n+1}{j}\left[\left(\frac{d}{dx} \right)^{j}f(x) \right]\left[\left(\frac{d}{dx} \right)^{n+1-j}g(x) \right]
+\left[\left(\frac{d}{dx} \right)^{n+1}f(x) \right]\left[\left(\frac{d}{dx} \right)g(x) \right]+\left[\left(\frac{d}{dx} \right)f(x) \right]\left[\left(\frac{d}{dx} \right)^{n+1}g(x) \right]\\
 &=\sum_{j=0}^{n+1}\binom{n+1}{j}\left[\left(\frac{d}{dx} \right)^{j}f(x) \right]\left[\left(\frac{d}{dx} \right)^{n+1-j}g(x) \right]
\end{aligned}
$$

so the equation holds for all positive integers by mathematical induction.

## 1.5 Operations On Series Expansions Of Functions

### 1.5.1

$$\int_{-x}^x\frac{dt}{1-t~^2}=\frac{1}{2}\int_{-x}^x\left(\frac{1}{1-t}+\frac{1}{1+t}\right)dt=\frac{1}{2}\left[-\ln{\frac{1-x}{1+x}} +\ln{\frac{1+x}{1-x}}\right]=\ln{\frac{1+x}{1-x}}$$

--------------

### 1.5.2

If the equation holds for p,

$$
\begin{aligned}
\frac{1}{n(n+1)\cdots(n+p)} &= \frac{1}{p!}\sum_{j=0}^p (-1)^j \binom{p}{j}\frac{1}{n+j}\\
\frac{1}{n(n+1)\cdots(n+p)(n+p+1)} &= \frac{1}{p!}\sum_{j=0}^p (-1)^j \binom{p}{j}\frac{1}{n+j}\frac{1}{n+p+1}\\
&=\frac{1}{p!}\sum_{j=0}^p (-1)^j \binom{p}{j}\left(\frac{1}{n+j}-\frac{1}{n+p+1}\right)\frac{1}{p+1-j}\\
&=\frac{1}{(p+1)!}\sum_{j=0}^p (-1)^j\frac{p+1}{p+1-j} \binom{p}{j}\left(\frac{1}{n+j}-\frac{1}{n+p+1}\right)\\
&=\frac{1}{(p+1)!}\sum_{j=0}^p(-1)^j\binom{p+1}{j}\frac{1}{n+j}-\frac{1}{(p+1)!}\frac{1}{n+p+1}\sum_{j=0}^p(-1)^j\binom{p+1}{j}\\
&=\frac{1}{(p+1)!}\sum_{j=0}^p(-1)^j\binom{p+1}{j}\frac{1}{n+j}-\frac{1}{(p+1)!}\frac{1}{n+p+1}(-1)^{p+1}\sum_{j=1}^{p+1}(-1)^{j}\binom{p+1}{j}\\
&=\frac{1}{(p+1)!}\sum_{j=0}^p(-1)^j\binom{p+1}{j}\frac{1}{n+j}+\frac{1}{(p+1)!}\frac{1}{n+p+1}(-1)^{p+1}\sum_{j=1}^{p+1}(-1)^{j-1}\binom{p+1}{j}\\
&=\frac{1}{(p+1)!}\sum_{j=0}^p(-1)^j\binom{p+1}{j}\frac{1}{n+j}+\frac{1}{(p+1)!}\frac{1}{n+p+1}(-1)^{p+1}\\
&=\frac{1}{(p+1)!}\sum_{j=0}^{p+1}(-1)^j\binom{p+1}{j}\frac{1}{n+j}
\end{aligned}
$$

So the equation holds for p+1. The equation hold for 1. Therefore, it holds for all positive integers by mathematical induction.

--------------

### 1.5.3

$$
\begin{aligned}
u_n(p) &= \frac{1}{(n+1)\cdots(n+p-1)}\frac{1}{p}\left[\frac{1}{n}-\frac{1}{n+p} \right]=\frac{1}{p}\left[u_n(p-1)-u_{n+1}(p-1) \right]\\
\sum_{n=1}^\infty u_n(p) &= \frac{u_1(p-1)}{p}=\frac{1}{p\cdot p!}
\end{aligned}
$$

--------------

### 1.5.4

Substituting Eq. (1.88) into Eq. (1.87):

$$f(x)=\sum_{n=0}^\infty\sum_{j=0}^n(-1)^{n+j}\binom{n}{j}\frac{x^n}{(1+x)^{n+1}}c_{n-j}$$

Rearrange the series by $n'=n-j$:

$$
\begin{aligned}
f(x) &= \sum_{n'=0}^\infty\sum_{j=0}^\infty(-1)^{n'}\binom{n'+j}{j}\frac{x^{n'+j}}{(1+x)^{n'+1+j}}c_{n'}
=\sum_{n'=0}^\infty(-1)^{n'}c_{n'}\frac{x^{n'}}{(1+x)^{n'+1}}\sum_{j=0}^\infty\binom{n'+j}{j}\left(\frac{x}{1+x} \right)^j\\
&=\sum_{n'=0}^\infty(-1)^{n'}c_{n'}\frac{x^{n'}}{(1+x)^{n'+1}}\sum_{j=0}^\infty\binom{-n'-1}{j}\left(-\frac{x}{1+x} \right)^j =\sum_{n'=0}^\infty(-1)^{n'}c_{n'}\frac{x^{n'}}{(1+x)^{n'+1}}\left(1-\frac{x}{1+x} \right)^{-n'-1}\\
&=\sum_{n'=0}^\infty(-1)^{n'}c_{n'}\frac{x^{n'}}{(1+x)^{n'+1}}(1+x)^{n'+1}=\sum_{n'=0}^\infty(-1)^{n'}c_{n'}x^{n'}=\sum_{n=0}^\infty(-1)^{n}c_{n}x^{n}
\end{aligned}
$$

--------------

### 1.5.5

Let $\arctan{x}=\sum_{n=0}^\infty(-1)^n c_n x^n$, then from $n=0$, $c_n=0, -\frac{1}{1}, 0, \frac{1}{3}, 0, -\frac{1}{5}, \cdots$, which means there are only odd terms. $a_n=\sum_{j=0}^n(-1)^j\binom{n}{j}c_{n-j}$, when n is odd, $a_n=\sum_{j=0,2,4,\cdots,n-1}\binom{n}{j}c_{n-j}=\sum_{k=1,3,5,\cdots,n}\binom{n}{k}c_k=-\binom{n}{1}\frac{1}{1}+\binom{n}{3}\frac{1}{3}-\binom{n}{5}\frac{1}{5}+\cdots$; when n is even, $a_n=\sum_{j=1,3,5,\cdots,n-1}(-1)\binom{n}{j}c_{n-j}=\sum_{k=1,3,5,\cdots,n-1}(-1)\binom{n}{k}c_k=\binom{n}{1}\frac{1}{1}-\binom{n}{3}\frac{1}{3}+\binom{n}{5}\frac{1}{5}-\cdots$. The numerical verification of $\arctan{(1)}$ and $\arctan{(3^{-1/2})}$ is straightforward by using Eq. (1.87).

## 1.6 Some Important Series

### 1.6.1

$$\ln{(1+x)}=x-\frac{x^2}{2}+\frac{x^3}{3}-\frac{x^4}{4}+\frac{x^5}{5}-\cdots$$

$$\ln{(1-x)}=-x-\frac{x^2}{2}-\frac{x^3}{3}-\frac{x^4}{4}-\frac{x^5}{5}-\cdots$$

so

$$\ln{\left(\frac{1+x}{1-x} \right)}=\ln{(1+x)}-\ln{(1-x)}=2\left(x+\frac{x^3}{3}+\frac{x^5}{5}+\cdots \right)$$

## 1.7 Vectors

### 1.7.1

$3(A_x)^2=1.732^2$, so $A_x=A_y=A_z\approx1.000$

--------------

### 1.7.2

$(\textbf{B}-\textbf{A})+(\textbf{C}-\textbf{B})+(\textbf{A}-\textbf{C})=0$

--------------

### 1.7.3

(a) $(x-x_1)^2+(y-y_1)^2+(z-z_1)^2=0$

(b) $\mathbf{r}=\mathbf{r}+\mathbf{a}$

--------------

### 1.7.4

Let $\mathbf{v}_i'$ and $\mathbf{r}_i'$ be the velocity and position of the $i$th galaxy viewed from $\mathbf{r}_1$. Then 

$$\mathbf{v}_i'=\mathbf{v}_i-\mathbf{v}_1=H_0\mathbf{r}_i-H_0\mathbf{r}_1=H_0\mathbf{r}_i'$$

--------------

### 1.7.5

Diagonals: $\pm(1,1,1), \pm(-1,1,1), \pm(1,-1,1), \pm(1,1,-1)$

Diagonals of faces: $\pm(1,-1,0),\pm(1,0,-1),\pm(0,1,-1)$

--------------

### 1.7.6

(a) $(x-a_x)a_x+(y-a_y)a_y+(z-a_z)a_z=0$. It is the surface containing the tip of $\mathbf{a}$ and perpendicular to $\mathbf{a}$.

(b)$(x-a_x)x+(y-a_y)a_y+(z-a_z)a_z=0$, so $(x-\frac{a_x}{2})^2+(y-\frac{a_y}{2})^2+(z-\frac{a_z}{2})^2=\frac{a_x^2+a_y^2+a_z^2}{4}$. It is a sphere cantered at the tip of $\frac{1}{2}\mathbf{a}$ with radius  $\frac{1}{2}|\mathbf{a}|$.

--------------

### 1.7.7

$(1,0,1)\cdot(0,1,-1)/(\sqrt{2}\cdot\sqrt{2})=-1/2=\cos{\theta}$, so $\theta=120^\circ$

--------------

### 1.7.8

$(1+t-2,1+2t-1,1+3t-3)\cdot(1,2,3)=0$, so $t=\frac{1}{2}$, and the nearest point is $(\frac{3}{2},2,\frac{5}{2})$. So the nearest distance with $(2,1,3)$ is $\sqrt{\frac{3}{2}}$.

--------------

### 1.7.9

Let the position vector of three vertices of the triangle be $\mathbf{A}, \mathbf{B}, \mathbf{C}$. Let the median from \textbf{C} and the median from \textbf{B} intersect at point \textbf{X}. Then $\mathbf{X}-\mathbf{B}=m(\frac{\mathbf{A}}{2}+\frac{\mathbf{C}}{2}-\mathbf{B})$,  $\mathbf{X}-\mathbf{C}=m(\frac{\mathbf{A}}{2}+\frac{\mathbf{B}}{2}-\mathbf{C})$. Solve for $m,n$ obtaining $m=n=\frac{2}{3}$, and $\mathbf{X}=\frac{\mathbf{A}}{3}+\frac{\mathbf{B}}{3}+\frac{\mathbf{C}}{3}$. $\mathbf{X}-\mathbf{A}=\frac{-2\mathbf{A}}{3}+\frac{\mathbf{B}}{3}+\frac{\mathbf{C}}{3}=\frac{2}{3}(-\mathbf{A}+\frac{\mathbf{B}}{2}+\frac{\mathbf{C}}{2})$. Therefore, the three medians intersect at one point, and the distances from this point to three vertices are $2/3$ of the median's length.

--------------

### 1.7.10

$|\mathbf{A}|^2=|\mathbf{B}|^2+|\mathbf{C}|^2-2\mathbf{B}\cdot\mathbf{C}=|\mathbf{B}|^2+|\mathbf{C}|^2-2|\mathbf{B}||\mathbf{C}|$

--------------

### 1.7.11

$\mathbf{Q}=-2\mathbf{P}$, so \textbf{Q} and \textbf{P} are anti-parallel. $\mathbf{P}\cdot\mathbf{R}=0$ and $\mathbf{Q}\cdot\mathbf{R}=0$, so \textbf{R} is perpendicular to \textbf{P} and \textbf{Q}.

## 1.8 Complex Numbers And Functions

### 1.8.1

$x+iy=re^{i\theta}$ where $r=\sqrt{x^2+y^2}$ and  $\theta=\tan^{-1}\frac{y}{x}$. $(x+iy)^{-1}=r^{-1}e^{-i\theta}=\frac{1}{\sqrt{x^2+y^2}}(\cos{(-\theta)}+i\sin{(-\theta}))=\frac{x}{x^2+y^2}-i\frac{y}{x^2+y^2}$

--------------

### 1.8.2

$(re^{i\theta})^{1/2}=r^{1/2}e^{i\theta/2}$ is a complex number. $i^{1/2}=(e^{i\pi/2})^{1/2}=e^{i\pi/4}=\frac{\sqrt{2}}{2}+\frac{\sqrt{2}}{2}i$

--------------

### 1.8.3

(a)

$$
\begin{aligned}
\cos{n\theta} &= \Re{\left[e^{in\theta}\right]}=\Re{\left[(e^{i\theta})^n\right]}=\Re{\left[\sum_{k=0}^n\binom{n}{k}\cos^{n-k}\theta\sin^k\theta(i)^k\right]}\\
&= \sum_{k=0,2,4,\cdots}\binom{n}{k}\cos^{n-k}\theta\sin^k\theta(-1)^{k/2}
=\cos^n\theta-\binom{n}{2}\cos^{n-2}\theta\sin^2\theta+\binom{n}{4}\cos^{n-4}\theta\sin^{n}\theta-\cdots
\end{aligned}
$$

(b)

$$
\begin{aligned}
\sin{n\theta} &= \Im{\left[e^{in\theta}\right]}=\Im{\left[(e^{i\theta})^n\right]}=\Im{\left[\sum_{k=0}^n\binom{n}{k}\cos^{n-k}\theta\sin^k\theta(i)^k\right]}\\
&= \sum_{k=1,3,5,\cdots}\binom{n}{k}\cos^{n-k}\theta\sin^k\theta(-1)^{(k-1)/2}
=\binom{n}{1}\cos^{n-1}\theta\sin\theta-\binom{n}{3}\cos^{n-3}\theta\sin^3\theta+\cdots
\end{aligned}
$$

--------------

### 1.8.4

(a)

$$\sum_{n=0}^{N-1}\cos{nx}=\Re{\left[\sum_{n=0}^{N-1}e^{inx} \right]}=\Re{\left[\frac{1-e^{iNx}}{1-e^{ix}} \right]}=\Re{\left[\frac{e^{iNx/2}}{e^{ix/2}}\left(\frac{e^{iNx/2}-e^{-iNx/2}}{e^{ix/2}-e^{-ix/2}} \right) \right]}=\left(\cos{\frac{(N-1)x}{2}}\right)\frac{\sin{(Nx/2)}}{\sin{(x/2)}}$$

(b)

$$\sum_{n=0}^{N-1}\sin{nx}=\Im{\left[\sum_{n=0}^{N-1}e^{inx} \right]}=\Im{\left[\frac{1-e^{iNx}}{1-e^{ix}} \right]}=\Im{\left[\frac{e^{iNx/2}}{e^{ix/2}}\left(\frac{e^{iNx/2}-e^{-iNx/2}}{e^{ix/2}-e^{-ix/2}} \right) \right]}=\left(\sin{\frac{(N-1)x}{2}}\right)\frac{\sin{(Nx/2)}}{\sin{(x/2)}}$$

--------------

### 1.8.5

$$\sin{z}=z-\frac{z^3}{3!}+\frac{z^5}{5!}-\cdots$$

$$\cos{z}=1-\frac{z^2}{2!}+\frac{z^4}{4!}-\cdots$$

$$\sinh{z}=\frac{e^z-e^{-z}}{2}=z+\frac{z^3}{3!}+\frac{z^5}{5!}+\cdots$$

$$\cosh{z}=\frac{e^x+e^{-x}}{2}=1+\frac{z^2}{2!}+\frac{z^4}{4!}+\cdots$$

Substituting $iz$ for $z$, then we obtain all the four equations. 

--------------

### 1.8.6

(a)

$$
\begin{aligned}
\sin{(x+iy)} &= \frac{e^{-y+ix}-e^{y-ix}}{2i}=\frac{e^{-y}\cos{x}-e^y\cos{x}}{2i}+\frac{ie^{-y}\sin{x}+ie^y\sin{x}}{2i}=\sin{x}\cosh{y}+i\cos{x}\sinh{y}\\
\cos{(x+iy)} &= \frac{e^{-y+ix}+e^{y-ix}}{2}=\frac{e^{-y}\cos{x}+e^y\cos{x}}{2}+\frac{ie^{-y}\sin{x}-ie^y\sin{x}}{2}=\cos{x}\cosh{y}-i\sin{x}\sinh{y}
\end{aligned}
$$

(b)

$$
\begin{aligned}
|\sin{z}|^2 &= \sin^2x(1+\sinh^2y)+(1-\sin^2x)\sinh^2y=\sin^2x+\sinh^2y\\
|\cos{z}|^2 &= \cos^2x(1+\sinh^2y)+(1-\cos^2x)\sinh^2y=\cos^2x+\sinh^2y
\end{aligned}
$$

--------------

### 1.8.7

(a)

$$
\begin{aligned}
\sinh{(x+iy)} &= i\sin{(y-ix)}=i(\sin{y}\cosh{x}-i\cos{y}\sinh{x})=\sinh{x}\cos{y}+i\cosh{x}\sin{y}\\
\cosh{(x+iy)} &= \cos{(y-ix)}=\cos{y}\cosh{x}+i\sin{y}\sinh{x}=\cosh{x}\cos{y}+i\sinh{x}\sin{y}
\end{aligned}
$$

(b)

$$
\begin{aligned}
|\sinh{(x+iy)}|^2 &= |\sin{(y-ix)}|^2=\sin^2{y}+\sinh^2{(-x)}=\sinh^2{x}+\sin^2{y}\\
|\cosh{(x+iy)}|^2 &= |\cos{(y-ix)}|^2=\cos^2{y}+\sinh^2{(-x)}=1-\sin^2{y}+\cosh^2{x}-1=\cosh^2{x}-\sin^2{y}
\end{aligned}
$$

--------------

### 1.8.8

(a) 

$$
\begin{aligned}
\frac{\sinh{(\frac{z}{2})}}{\cosh{(\frac{z}{2}})} &= \frac{\sinh{(\frac{x}{2})}\cos{(\frac{y}{2})}+i\cosh{(\frac{x}{2})}\sin{(\frac{y}{2})}}{\cosh{(\frac{x}{2})}\cos{(\frac{y}{2})}+i\sinh{(\frac{x}{2})}\sin{(\frac{y}{2})}}=\frac{\cosh(\frac{x}{2})\sinh(\frac{x}{2})+i\cos(\frac{y}{2})\sin(\frac{y}{2})}{\cosh^2(\frac{x}{2})\cos^2(\frac{y}{2})+\sinh^2(\frac{x}{2})\sin^2(\frac{y}{2})}\\
&= \frac{\frac{1}{2}\sinh{x}+i\frac{1}{2}\sin{y}}{\frac{\cosh{x}+1}{2}\frac{1+\cos{y}}{2}+\frac{\cosh{x}-1}{2}\frac{1-\cos{y}}{2}}=\frac{\sinh{x}+i\sin{y}}{\cosh{x}+\cos{y}}
\end{aligned}
$$

(b)

$$
\begin{aligned}
\coth(\frac{z}{2}) &= \frac{1}{\tanh(\frac{z}{2})}=\frac{\cosh{x}+\cos{y}}{\sinh{x}+i\sin{y}}=\frac{(\cosh{x}+\cos{y})(\sinh{x}-i\sin{y})}{\sinh^2{x}+\sin^2{y}}\\
&= \frac{(\cosh{x}+\cos{y})(\sinh{x}-i\sin{y})}{\cosh^2{x}-\cos^2{y}}=\frac{\sinh{x}-i\sin{y}}{\cosh{x}-\cos{y}}
\end{aligned}
$$

--------------

### 1.8.9

$$
\begin{aligned}
\tan^{-1}x &= \int_0^x\frac{1}{1+x^2}dx=\int_0^x(1-x^2+x^4-\cdots)dx=x-\frac{x^3}{3}+\frac{x^5}{5}-\cdots\\
\ln(1-ix) &= -{ix}-\frac{(ix)^2}{2}-\frac{(ix)^3}{3}-\frac{(ix)^4}{4}-\frac{(ix)^5}{5}-\cdots\\
\ln(1+ix) &= {ix}-\frac{(ix)^2}{2}+\frac{(ix)^3}{3}-\frac{(ix)^4}{4}+\frac{(ix)^5}{5}-\cdots\\
\frac{i}{2}\ln\left(\frac{1-ix}{1+ix} \right) &= \frac{i}{2}\left(\ln(1-ix)-\ln(1+ix) \right)=\frac{i}{2}(-2)\left((ix)+\frac{(ix)^3}{3}+\frac{(ix)^5}{5}+\cdots \right)=x-\frac{x^3}{3}+\frac{x^5}{5}-\cdots
\end{aligned}
$$

--------------

### 1.8.10

(a) 

$$(-8)^{1/3}=\left(8e^{i(1+2n)\pi} \right)^{1/3}=2e^{i\frac{\pi}{3}}, 2e^{i\pi},2e^{-i\frac{\pi}{3}}=1+\sqrt{3}i,-2,1-\sqrt{3}i$$

$$\[i^{1/4}=(e^{i(\frac{1}{2}+2n)\pi})^{1/4}=e^{i\frac{\pi}{8}},e^{i\frac{5\pi}{8}},e^{i\frac{9\pi}{8}},e^{i\frac{13\pi}{8}}$$

$$\[\frac{1}{\sqrt{2}}+\frac{1}{\sqrt{2}}i$$

--------------

### 1.8.11

(a) 

$$(1+i)^3=\left(\sqrt{2}e^{i\frac{\pi}{4}} \right)^3=2^{3/2}e^{i3\pi/4}$$

(b) 

$$\left(e^{i(-1+2n)\pi} \right)^{1/5}=e^{ik\pi/5}$$

where $k=1,3,5,7,9$.

## 1.9 Derivatives and Extrema

### 1.9.1

$$f(x,y)=\sum_{n=0}^\infty\frac{x^n}{n!}\frac{\partial^nf}{\partial x^n}\Big|_{0,y}=
\sum_{n=0}^\infty\frac{x^n}{n!}\sum_{m=0}^\infty\frac{y^m}{m!}\frac{\partial^{m+n}f}{\partial y^m\partial x^n}\Big|_{0,0}$$

Rearrange the double series by $p=m+n$ and $q=n$,

$$f(x,y)=\sum_{p=0}^\infty\sum_{q=0}^p\frac{x^{p-q}}{(p-q)!}\frac{y^q}{q!}\frac{\partial^{m+n}f}{\partial y^m\partial x^n}\Big|_{0,0}
=\sum_{p=0}^\infty\sum_{q=0}^p\frac{1}{p!}\binom{p}{q}x^{p-q}y^q\frac{\partial^{m+n}f}{\partial y^m\partial x^n}\Big|_{0,0}$$

--------------

### 1.9.2

Expand the function in every variable as in Exercise 1.9.1, then

$$f(x_1,\cdots,x_m)=\sum_{n_1=0}^\infty\cdots\sum_{n_m=0}^\infty\frac{x_1^{n_1}}{n_1!}\cdots\frac{x_m^{n_m}}{n_m!}\frac{\partial^{n_1+\cdots+n_m}}{\partial x_1^{n_1}\cdots\partial x_m^{n_m}}f(0,\cdots,0)$$

Let $n=n_1+\cdots+n_m$, substitute $\alpha_i t$ for $x_i$, and apply the generalized form of binomial theorem (Eq 1.80),

$$
\begin{aligned}
f(x_1,\cdots,x_m) &= \sum_{n_1=0}^\infty\cdots\sum_{n_m=0}^\infty\frac{1}{n!}\frac{n!}{n_1!\cdots n_m!}t^{n_1\cdots+n_m}\left(\alpha_1\frac{\partial}{\partial x_1} \right)^{n_1}\cdots\left(\alpha_m\frac{\partial}{\partial x_m} \right)^{n_m}f(0,\cdots,0)\\
&= \sum_{n=0}^\infty\frac{t^n}{n!}\left(\alpha_1\frac{\partial}{\partial x_1}+\cdots+\alpha_m\frac{\partial}{\partial x_m} \right)^nf(0,\cdots,0)
=\sum_{n=0}^\infty\frac{t^n}{n!}\left(\sum_{i=1}^m\alpha_i\frac{\partial}{\partial x_i} \right)^n f(0,\cdots,0)\\
\end{aligned}
$$

## 1.10 Evaluation of Integrals


### 1.10.1

$$\Gamma(n)=\int_0^\infty t^{n-1}e^{-t}dt=-t^{n-1}e^{-t}\Big|_0^\infty+\int_0^\infty(n-1)t^{n-2}e^{-t}dt=(n-1)\Gamma(n-1)$$

We have integrated by parts and applied the definition of $\Gamma(n-1)$. Keep reducing n by this method until $n=1$, and note that $\Gamma(1)=1$, we  obtain

$$\Gamma(n)=(n-1)!$$

--------------

### 1.10.2

Let $J(a)=\int_o^\infty e^{-ax}\frac{\sin{x}}{x}dx$, then $\int_0^\infty \frac{\sin x}{x}dx=J(0)$.

$$
\begin{aligned}
\frac{dJ(a)}{da} &= -\int_0^\infty e^{-ax}\sin{x}dx=-\Im{\left[ \int_0^\infty e^{(-a+i)x} \right] dx}=-\Im{\left
[\frac{e^{(-a+i)x}}{-a+i}\bigg|_0^\infty \right]}=\frac{-1}{a^2+1}\\
J(a) &= \int\frac{-1}{a^2+1}da=-\tan^{-1}a+c=-\tan^{-1}a+\frac{\pi}{2}
\end{aligned}
$$

where $c$ is determined by $J(\infty)=0$.

$$\int_0^\infty \frac{\sin x}{x}dx=J(0)=\frac{\pi}{2}$$

--------------

### 1.10.3

$$\int_0^\infty\frac{dx}{\cosh{x}}=\int_0^\infty\frac{2}{e^x+e^{-x}}dx=\int_0^\infty\frac{2e^{-x}}{1+e^{-2x}}=\int_0^\infty2e^{-x}(1-e^{-2x}+e^{4x}-\cdots)dx=2(\frac{1}{1}-\frac{1}{3}+\frac{1}{5}-\cdots)$$

where the expansion is valid for all positive x because $e^{-2x}<1$ for all positive x. $\tan^{-1}1=\frac{\pi}{4}=\int_0^1\frac{1}{1+x^2}dx=\int_0^1(1-x^2+x^4-\cdots) dx=1-\frac{1}{3}+\frac{1}{5}-\cdots$, so 

$$\int_0^\infty\frac{dx}{\cosh{x}}=2\tan^{-1}1=\frac{\pi}{2}$$

--------------

### 1.10.4

$$\int_0^\infty\frac{dx}{e^{ax}+1}=\int_0^\infty\frac{e^{-ax}}{1+e^{-ax}}=\int_0^\infty e^{-ax}(1-e^{-ax}+e^{-2ax}-\cdots)dx=\frac{1}{a}(\frac{1}{1}-\frac{1}{2}+\frac{1}{3}-\cdots)=\frac{1}{a}\ln{(1+1)}=\frac{\ln{2}}{a}$$

--------------

### 1.10.5

Integrating by parts

$$\int_\pi^\infty\frac{\sin{x}}{x^2}dx=\frac{-1}{x}\sin{x}\Big|_\pi^\infty-\int_\pi^\infty-\frac{\cos{x}}{x}dx=-\mathrm{Ci}(\pi)$$

where $\mathrm{Ci}(x)$ is the cosine integral (see Table 1.2)

--------------

### 1.10.6

Let $J(a)=\int_0^\infty e^{-ax}\frac{\sin{x}}{x}dx$, which is the same as Exercise 1.10.2, then $\int_0^\infty e^{-x}\frac{\sin{x}}{x}dx=J(1)$.

$$\int_0^\infty e^{-x}\frac{\sin{x}}{x}dx=-\tan^{-1}{1}+\frac{\pi}{2}=\frac{\pi}{4}$$

--------------

### 1.10.7

Integrating by parts

$$\int_0^x \mathrm{erf}(t)dt=\mathrm{erf}(t)\cdot t\Big|_0^x-\int_0^x d\,\mathrm{erf}(t)\cdot t=x\,\mathrm{erf}(x)-\int_0^x\frac{2}{\sqrt{\pi}}e^{-t^2}dt\cdot t=x\,\mathrm{erf}(x)+\frac{e^{-x^2}-1}{\sqrt{\pi}}$$

--------------

### 1.10.8

Integrating by parts

$$
\begin{aligned}
\int_1^x\mathrm{E_1}(t)\,dt &= \mathrm{E_1}(t)\,t\Big|_1^x-\int_1^x d\,\mathrm{E_1}(t)\cdot t=\mathrm{E_1}(t)\,t\Big|_1^x-\int_1^x -t^{-1}e^{-t}\,dt\cdot t=\mathrm{E_1}(t)\,t\Big|_1^x-e^{-t}\Big|_1^x\\
&=x\,\mathrm{E_1}(x)-\mathrm{E_1}(1)+e^{-1}-e^{-x}
\end{aligned}
$$

--------------

### 1.10.9

Let $y=x+1$

$$\int_0^\infty\frac{e^{-x}}{x+1}dx=\int_1^\infty\frac{e^{-y+1}}{y}dy=e\,\mathrm{E_1}(1)$$

--------------

### 1.10.10

Integrating by parts

$$I=\int_0^\infty(\tan^{-1}x)^2\frac{1}{x^2}dx=-(\tan^{-1}x)^2\frac{1}{x}\Big|_0^\infty-\int_0^\infty2\tan^{-1}x\frac{1}{1+x^2}\frac{-1}{x}dx=\int_0^\infty\frac{2\tan^{-1}x}{(1+x^2)x}dx$$

Let $J(a)=\int_0^\infty\frac{2\tan^{-1}ax}{(1+x^2)x}dx$, then $I=J(1)$

$$
\begin{aligned}
\frac{dJ(a)}{da} &= \int_0^\infty\frac{2}{(1+x^2)x}\frac{x}{1+a^2x^2}=\frac{2}{1-a^2}\int_0^\infty\left(\frac{1}{1+x^2}-\frac{a^2}{1+a^2x^2} \right)dx\\
&= \frac{2}{1-a^2}\left[\tan^{-1}x\Big|_0^\infty-a\tan^{-1}ax\Big|_0^\infty \right]=\frac{2}{1-a^2}\left[(1-a)\frac{\pi}{2} \right] =\frac{\pi}{1+a}\]
\[J(a)=\int\frac{\pi}{1+a}da=\pi\ln|1+a|+c=\pi\ln|1+a|
\end{aligned}
$$

where $c=0$ is determined by $J(0)=0$. So 

$$\int_0^\infty\left(\frac{\tan^{-1}x}{x} \right)^2dx=J(1)=\pi\ln2$$

--------------

### 1.10.11

$$A=4\int_0^a dx\int_0^{b\sqrt{1-\frac{x^2}{a^2}}}dy=4\int_0^ab\sqrt{1-\frac{x^2}{a^2}}dx$$

Let $\frac{x}{a}=\sin{\theta}$, then$\sqrt{1-\frac{x^2}{a^2}}=\cos{\theta}$, $dx=a\cos{\theta}d\theta$, and the range of integration becomes $0$ to $\frac{\pi}{2}$

$$A=4\int_0^\frac{\pi}{2}ab\cos^2\theta d\theta=4ab\left(\frac{\theta}{2}+\frac{\sin{2\theta}}{4} \right)\Big|_0^{\frac{\pi}{2}}=\pi ab$$

--------------

### 1.10.12

$$A=\int_{-\frac{\pi}{3}}^\frac{\pi}{3}d\theta\int_{\frac{1}{2}\sec{\theta}}^1 r\,dr=\int_{-\frac{\pi}{3}}^\frac{\pi}{3}\frac{1}{2}\left(1-\frac{\sec^2\theta}{4} \right)d\theta=\left(\frac{\theta}{2}-\frac{\tan{\theta}}{8} \right)\Big|_{-\frac{\pi}{3}}^{\frac{\pi}{3}}=\frac{\pi}{3}-\frac{\sqrt{3}}{4}$$

Which is the area of the circular sector minus the area of triangle.

## 1.11 Dirac Delta Function

### 1.11.1

$$\lim_{n\to\infty}\int_{-\infty}^\infty f(x)\delta_n(x)dx=\lim_{n\to\infty}\int_{-\frac{1}{2n}}^{\frac{1}{2n}}f(x)n\,dx=\lim_{n\to\infty}f(\xi_n)\frac{1}{n}n=f(0)$$

where $-\frac{1}{2n}\leq\xi_n\leq\frac{1}{2n}$ (by mean value theorem).

--------------

### 1.11.2

Let $nx=\tan\theta$, then $1+n^2x^2=\sec^2\theta$, and $ndx=\sec^2\theta d\theta$. The range of integration becomes $-\frac{\pi}{2}$ to $\frac{\pi}{2}$

$$\int_{-\infty}^\infty\frac{n}{\pi}\frac{1}{1+n^2x^2}dx==\int_{-\frac{\pi}{2}}^\frac{\pi}{2}\frac{n}{\pi}\frac{1}{\sec^2\theta}\frac{1}{n}\sec^2\theta\,d\theta=\frac{\theta}{\pi}\Big|_{-\frac{\pi}{2}}^\frac{\pi}{2} =1$$

--------------

### 1.11.3

The proof probably requires contour integral of complex analysis, while I have no idea whether there is any elementary proof.

--------------

### 1.11.4

Let $a(x-x_1)=y$, then $x=\frac{y}{a}+x_1$, $adx=dy$,

$$\int_{-\infty}^\infty f(x)\delta[a(x-x_1)]dx=\frac{1}{a}\int_{-\infty}^\infty f(\frac{y}{a}+x_1)\delta(y)dy=\frac{1}{a}f(\frac{0}{a}+x_1)=\frac{1}{a}f(x_1)=\int_{-\infty}^\infty f(x)\frac{1}{a}\delta(x-x_1)dx$$

so $\delta[a(x-x_1)]=\frac{1}{a}\delta(x-x_1)$.

--------------

### 1.11.5

When $(x-x_1)(x-x_2)\neq0$, $\delta[(x-x_1)(x-x_2)]=0$, so

$$\int_{-\infty}^\infty f(x)\delta[(x-x_1)(x-x_2)]dx=\int_{x_1-\varepsilon}^{x_1+\varepsilon}f(x)\delta[(x-x_1)(x-x_2)]dx+\int_{x_2-\varepsilon}^{x_2+\varepsilon}f(x)\delta[(x-x_1)(x-x_2)]dx$$

for arbitrarily small positive $\varepsilon$. Then

$$
\begin{aligned}
&\lim_{\varepsilon\to0}\int_{x_1-\varepsilon}^{x_1+\varepsilon}f(x)\delta[(x-x_1)(x-x_2)]dx+\int_{x_2-\varepsilon}^{x_2+\varepsilon}f(x)\delta[(x-x_1)(x-x_2)]dx\\
=& \int_{x_1-\varepsilon}^{x_1+\varepsilon}f(x)\delta[(x-x_1)(x_1-x_2)]dx+\int_{x_2-\varepsilon}^{x_2+\varepsilon}f(x)\delta[(x_2-x_1)(x-x_2)]dx\\
=& \int_{x_1-\varepsilon}^{x_1+\varepsilon}f(x)\frac{1}{|x_1-x_2|}\delta(x-x_1)dx+\int_{x_2-\varepsilon}^{x_2+\varepsilon}f(x)\frac{1}{|x_1-x_2|}\delta(x-x_2)dx\\
=& \int_{-\infty}^\infty f(x)\frac{\delta(x-x_1)+\delta(x-x_2)}{|x_1-x_2|}dx
\end{aligned}
$$

Therefore,

$$\delta[(x-x_1)(x-x_2)]=\frac{\delta(x-x_1)+\delta(x-x_2)}{|x_1-x_2|}$$

--------------

### 1.11.6

Integrating by parts

$$\int_{-\infty}^\infty f(x)x\frac{d\delta(x)}{dx}dx=f(x)x\delta(x)\Big|_{-\infty}^\infty-\int_{-\infty}^\infty[f'(x)x+f(x)]\delta(x)dx=0-f(0)=-\int_{-\infty}^\infty f(x)\delta(x)dx$$

Therefore,

$$x\frac{d\delta(x)}{dx}=-\delta(x)$$

--------------

### 1.11.7

Integrating by parts

$$\int_{-\infty}^\infty\frac{d\delta(x)}{dx}f(x)dx=\delta(x)f(x)\Big|_{-\infty}^\infty-\int_{-\infty}^\infty\delta(x)f'(x)dx=-f'(0)$$

--------------

### 1.11.8

(The equation holds only when $f(x)$ has only one zero point.) When $f(x)\neq0$, $\delta\left(f(x)\right)=0$, so

$$\int_{-\infty}^\infty h(x)\delta(f(x))dx=\int_{x_0-\varepsilon}^{x_0+\varepsilon}h(x)\delta\left((x-x_0)f'(x_0)+\frac{(x-x_0)^2}{2}f''(x_0)+\cdots \right)dx$$

for arbitrary small positive $\varepsilon$. Then

$$\lim_{\varepsilon\to 0}\int_{x_0-\varepsilon}^{x_0+\varepsilon} h(x)\delta(f(x))dx
=\lim_{\varepsilon\to 0}\int_{x_0-\varepsilon}^{x_0+\varepsilon} h(x)\delta\left((x-x_0)f'(x_0)\right)dx
=\int_{-\infty}^{\infty} h(x)\frac{1}{|f'(x_0)|}\delta(x-x_0) dx$$4

by Exercise 1.11.4. Therefore

$$\delta\left(f(x) \right)=\frac{1}{|f'(x_0)|}\delta(x-x_0)$$

--------------

### 1.11.9

(a)

$$\int_{-\infty}^\infty\frac{n}{2\cosh^2{nx}}dx=\frac{1}{2}\tanh{nx}\Big|_{-\infty}^\infty=1$$

(b)

$$\int_{-\infty}^x\frac{n}{2\cosh^2{nx}}dx=\frac{1}{2}\left(\tanh{nx}+1 \right)=u_n(x)$$

When $n\to\infty$ and $x<0$, $u_n(x)=\frac{1}{2}(-1+1)=0$; when $n\to\infty$ and $x>0$, $u_n(x)=\frac{1}{2}(1+1)=1$.
