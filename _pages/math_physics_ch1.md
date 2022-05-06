---
layout: splash
title: "Mathematical Methods for Physicists"
permalink: /solutions/math_physics_ch1
author_profile: false
redirect_from:
  - /resume
---

## Chapter 1: Mathematical Preliminaries

### 1.1 Infinite Series

#### 1.1.1
(a) If $A>0$, $\lim_{n\to \infty}n^p u_n=A$, so $|n^p u_n-A|< \frac{A}{2}$ when $n\geq N$ for some N. Then $0<\frac{A}{2}\frac{1}{n^p}<u_n<\frac{3A}{2}\frac{1}{n^p}$. $\sum_{n=1}^{\infty}\frac{3A}{2}\frac{1}{n^p}$ converges when $p>1$ by Cauchy integral test, so $\sum_{n=1}^{\infty}u_n$ converges by comparison test.

If $A<0$, then $\lim_{n\to \infty}n^p(-u_n)=-A$, $-A>0$. From above $\sum_1^\infty(-u_n)$ converges, so $\sum_1^\infty(u_n)$ converges.

If $A=0$, $|n^p u_n|< 1$ when $n\geq N$ for some N. Then $-\frac{1}{n^p}<u_n<\frac{1}{n^p}$, so $|u_n|<\frac{1}{n^p}$ for sufficiently large n. $\sum_{n=1}^\infty \frac{1}{n^p}$ converges by Cauchy integral test, so $\sum_{n=1}^{\infty}u_n$ converges by comparison test.
\medskip

(b) $\lim_{n\to\infty}nu_n=A$, so $A-\frac{A}{2}<nu_n<A+\frac{A}{2}$ when $n\geq N$ for some N. So $u_n>\frac{A}{2}\frac{1}{n}$ for sufficiently large n. The harmonic series $\sum_{n=1}^\infty\frac{1}{n}$ diverges, so $\sum_{n=1}^\infty u_n$ diverges.

--------------
#### 1.1.2
Let $b_n'=\frac{b_n}{2K}$, then $\lim_{n\to\infty}\frac{b_n'}{a_n}=\frac{1}{2}$, so for sufficiently large n, $\frac{1}{2}-\frac{1}{2}=0<\frac{b_n'}{a_n}<1=\frac{1}{2}+\frac{1}{2}$. Then $0<b_n'<a_n$ or $0>b_n'>a_n$, so $\sum a_n$ converges implies $\sum b_n'$ converges by comparison test, and therefore $\sum b_n$ converges.

Let $b_n''=\frac{2b_n}{KK}$, then $\lim_{n\to\infty}\frac{b_n''}{a_n}=2$, so for sufficiently large n $2+1=3>\frac{b_n''}{a_n}>1=2-1$.Then $3a_n>b_n'' >a_n$ or $3a_n<b_n'' <a_n$,  so $\sum a_n$ diverges implies $\sum b_n''$ diverges by comparison test, and therefore $\sum b_n$ diverges.

--------------
#### 1.1.3
$\int_2^\infty \frac{1}{x(\ln x)^2}dx=-\frac{1}{\ln x}\bigr |_2^\infty=\frac{1}{\ln 2}$, so by Cauchy integral test $\sum_{n=2}^\infty \frac{1}{n(\ln n)^2}$ converges.

--------------
#### 1.1.4
$$\frac{u_n}{u_{n+1}}=1+\frac{(a_1-b_1)n+(a_0-b_0))}{n^2+b_1n+b_0}=1+\frac{a_1-b_1}{n}+\frac{B(n)}{n^2}$$
where $B(n)$ is bounded for large n (It can be verified by binomial theorem, that each term in $B(n)$ has negative or zero power of n. By Gauss' test, $\sum_{n=1}^\infty u_n$ converges if $a_1-b_1>1$ and diverges if $a_1-b_1\leq 1$. 

\paragraph{1.1.5}
(a) $\ln n<n$, so $\frac{1}{\ln n}>\frac{1}{n}>0$ for all positive integers n, and the harmonic series $\sum_{n=1}^\infty \frac{1}{n}$ diverges implies $\sum_{n=2}^\infty \frac{1}{\ln n}$ diverges.
\medskip

(b) $\frac{(n+1)!}{10^{n+1}}/\frac{n!}{10^n}=\frac{n+1}{10}\geq 1$ for $n\geq 9$, so $\sum_{n=1}^\infty \frac{n!}{10^n}$ diverges by ratio test.
\medskip

(c) $2n(2n+1)>(2n)^2$, so $0<\frac{1}{2n(2n+1)}<\frac{1}{(2n)^2}$. 
$\sum_{n=1}^\infty \frac{1}{4n^2}$ converges by integral test, so $\sum_{n=1}^\infty \frac{1}{2n(2n+1)}$ converges by comparison test.
\medskip

(d) $\frac{1}{\sqrt{n(n+1)}}>\frac{1}{\sqrt{(n+1)^2}}=\frac{1}{n+1}>0$. $\sum_{n=1}^\infty \frac{1}{n+1}$ diverges by integral test, so $\sum_{n=1}^\infty[n(n+1)]^{-\frac{1}{2}}$ diverges.
\medskip

(e) $\int_0^\infty \frac{1}{2x+1}=\frac{1}{2}\ln (2n+1)\bigr |_0^\infty$ is infinite, so $\sum_{n=0}^\infty \frac{1}{2n+1}$ diverges by integral test.

\paragraph{1.1.6}
(a) $0<\frac{1}{n(n+1)}<\frac{1}{n^2}$. $\sum_{n=1}^\infty\frac{1}{n^2}$ converges by integral test, so $\sum_{n=1}^\infty \frac{1}{n(n+1)}$ converges by comparison test. 
\medskip

(b) $\int_2^\infty \frac{1}{n\ln n}\,dx=\ln \ln n\bigr |_2^\infty$ is infinite, so $\sum_{n=2}^{\infty} \frac{1}{n\ln n}$ converges by integral test.
\medskip

(c) $\frac{1}{(n+1)2^{n+1}}/\frac{1}{n2^n}=\frac{n}{n+1}\frac{1}{2}\leq \frac{1}{2}$ for all n, so $\sum_{n=1}^\infty \frac{1}{n2^n}$ converges by retio test.
\medskip

(d) $\ln \frac{n+1}{n}=\ln (n+1)-\ln n$, so $\sum_{n=1}^\infty \ln (1+\frac{1}{n})=(\ln2-\ln1)+(\ln3-\ln2)+\cdots=\lim_{n\to\infty} \ln n$ is infinite, so $\sum_{n=1}^\infty \ln (1+\frac{1}{n})$ diverges.
\medskip

(e) $n^{\frac{1}{n}}>1$. Let $x_n=n^{\frac{1}{n}}-1$, then $(1+x_n)^n=n$, and $\frac{n(n+1)}{2}x_n^2\leq n$ by binomial theorem, so $0\leq x_n \leq \sqrt{\frac{2}{n-1}}$, and $\lim_{n\to\infty}\sqrt{\frac{2}{n-1}}=0$ implies $\lim_{n\to\infty}x_n=0$, so $\lim_{n\to\infty}n^{\frac{1}{n}}=1$.

$\lim_{n\to\infty}n^{\frac{1}{n}}=1$ implies for sufficiently large n, $0=1-1<n^{\frac{1}{n}}<1+1=2$, so $\frac{1}{n^{\frac{1}{n}}}>\frac{1}{2}$, and $\frac{1}{n\cdot n^{\frac{1}{n}}}>\frac{1}{2n}$. $\sum_{n=1}^\infty \frac{1}{2n}$ diverges by integral test, so $\sum_{n=1}^\infty \frac{1}{n\cdot n^{\frac{1}{n}}}$ diverges by comparison test.

\paragraph{1.1.7}
If $a_1\geq a_2\geq a_3 \geq \cdots \geq 0$, then $\sum_{n=1}^\infty a_n$ converges if and only if $\sum_{k=1}^\infty2^ka_{2k}$ converges\footnote{See Walter Rudin, \textit{Principles of Mathmatical Analysis}, Chapter 3, theorem 3.27}. 

$\sum_{k=1}^\infty 2^k \frac{1}{(2^k)^p(\ln 2^k)^q}=2^{(1-p)k}\frac{1}{k^q}\frac{1}{(\ln2)^q}$. If $p>1$, then $\sum_{k=1}^\infty \frac{1}{(2^{p-1})^k}\frac{1}{(\ln 2)^q}$ converges by ratio test, so $\sum_{k=1}^\infty 2^k \frac{1}{(2^k)^p(\ln 2^k)^q}$ converges, and $\sum_{n=2}^\infty \frac{1}{n^p(\ln n)^q}$ converges. 

If $p=1$, $\sum_{k=1}^\infty 2^k \frac{1}{(2^k)^p(\ln 2^k)^q}=\frac{1}{k^q}\frac{1}{(\ln2)^q}$, converges if $q>1$.

Therefore, if $p>1$, or $p=1$ and $q>1$, then $\sum_{n=2}^\infty \frac{1}{n^p(\ln n)^q}$ converges.

\paragraph{1.1.8}
\[\gamma=\lim_{n\to\infty}(\sum_{m=1}^n\frac{1}{m}-\ln n)=\sum_{m=1}^{1000}\frac{1}{m}+\lim_{n\to\infty}(\sum_{m=1001}^n\frac{1}{m}-\ln n)\]

\[\lim_{n\to\infty}n=\sum_{m=1001}^\infty\ln \frac{m}{m-1}-\ln 1000\]

\[\gamma=\sum_{m=1}^{1000}\frac{1}{m}-\ln{1000}+\sum_{m=1001}^\infty(\frac{1}{m}-\ln\frac{m}{m-1})\]

\[\int_{1001}^\infty(\frac{1}{x}-\ln\frac{x}{x-1})\,dx\geq\sum_{m=1001}^\infty(\frac{1}{m}-\ln\frac{m}{m-1})\geq \int_{1001}^\infty(\frac{1}{x}-\ln\frac{x}{x-1})\,dx+(\frac{1}{1001}-\ln\frac{1001}{1000})\]

\[\int_{1001}^\infty(\frac{1}{x}-\ln\frac{x}{x-1})\,dx=\ln\frac{x}{x-1}+x\ln\frac{x-1}{x}\Big |_{1001}^\infty=-0.000\,499\,667\]

\[\frac{1}{1001}-\ln\frac{1001}{1000}=-0.000\,000\,499\]

\[\sum_{m=1}^{1000}\frac{1}{m}-\ln1000=0.577\,714\,7\]

\[0.577\,715-0.000\,499>\gamma>0.577\,714-0.000\,500-0.000\,001\]

\[0.577\,213<\gamma<0.577\,216\]

\paragraph{1.1.9}
The number in each shell is proportional to $r^2$, but the solid angle of each shell is proportional to $\frac{1}{r^2}$, so the total solid angle occupied by stars in each shell is the same. Let it be $\omega_0$.

If the solid angle occupied by stars from shell 1 to n is $a_n$, then $a_{n+1}=a_n+a-a_n\cdot \frac{a}{4\pi}$, where $a_n\cdot \frac{a}{4\pi}$ is the solid angle of stars in shell $n+1$ that is blocked by stars in shell 1 to n. So $a_{n+1}-4\pi=(a_n-4\pi)(1-\frac{a}{4\pi})$, and $a_n=(a-4\pi)(1-\frac{a}{4\pi})^{n-1}+4\pi$. $1-\frac{a}{4\pi}<1$, so $\lim_{n\to\infty}a_n=4\pi$.

\paragraph{1.1.10}
\[\frac{u_n}{u_{n+1}}=\left (\frac{2n+2}{2n+1} \right)^2=1+\frac{4n+3}{4n^2+4n+1}=1+\frac{1}{n}+\frac{B(n)}{n^2}\] 

where B(n) is bound for large n. By Gauss' test, \[\sum_{n=1}^\infty\left[ \frac{1\cdot3\cdot5\cdots(2n-1)}{2\cdot4\cdot6\cdots(2n)} \right]^2\] 

converges.

\paragraph{1.1.11}
(a) $\frac{\ln n}{n}$ is monotonically decreasing, and $\lim_{n\to\infty}\frac{\ln n}{n}=0$, so the series converges by  Leibniz criterion. $\frac{\ln n}{n}\geq \frac{1}{n}$ when $n\geq 3$, and $\sum_{n=1}^\infty\frac{1}{n}$ diverges by integral test, so $\sum_{n=1}^\infty\frac{\ln n}{n}$ diverges by comparison test, so the series is not absolutely convergent.
\medskip

(b)  The series $\frac{1}{1}-\frac{1}{3}+\frac{1}{5}-\cdots$ converges by Leibniz criterion, and so does the series  $\frac{1}{2}-\frac{1}{4}+\frac{1}{6}-\cdots$. So the series  $\frac{1}{1}+\frac{1}{2}-\frac{1}{3}-\frac{1}{4}+\frac{1}{5}+\frac{1}{6}\cdots$ is the sum of two convergent series, and is therefore convergent.
$\sum_{n=1}^\infty\frac{1}{n}$ diverges by integral test, so the series is not absolutely convergent.
\medskip

(c) 
Combine adjacent terms with same sign to form a new series $\sum_{n=1}^\infty a_n$
\[(1)-(\frac{1}{2}+\frac{1}{3})+(\frac{1}{4}+\frac{1}{5}+\frac{1}{6})-(\frac{1}{7}+\frac{1}{8}+\frac{1}{9}+\frac{1}{10})+\cdots\]

where \[a_n=\frac{1}{\frac{n^2-n}{2}+1}+\frac{1}{\frac{n^2-n}{2}+2}+\cdots+\frac{1}{\frac{n^2-n}{2}+n}\]
\[a_{n+1}=\frac{1}{\frac{n^2+n}{2}+1}+\frac{1}{\frac{n^2+n}{2}+2}+\cdots+\frac{1}{\frac{n^2+n}{2}+n}+\frac{1}{\frac{n^2+n}{2}+n+1}\]

so $a_n$ has n terms and $a_{n+1}$ has $n+1$ terms.

\[a_{n}-a_{n+1}=(\frac{1}{\frac{n^2-n}{2}+1}-\frac{1}{\frac{n^2+n}{2}+1})+(\frac{1}{\frac{n^2-n}{2}+2}-\frac{1}{\frac{n^2+n}{2}+2})+\cdots+(\frac{1}{\frac{n^2-n}{2}+n}-\frac{1}{\frac{n^2+n}{2}+n})-\frac{2}{n^2+3n+2}\]

The $k^{st}$ term (except for the last term) of $a_{n}-a_{n+1}$ is
\[\frac{1}{\frac{n^2-n}{2}+k}-\frac{1}{\frac{n^2+n}{2}+k}\geq\frac{1}{\frac{n^2-n}{2}+n}-\frac{1}{\frac{n^2+n}{2}+n}=\frac{4}{n^3+4n^2+3n}\]

so \[a_{n}-a_{n+1}\geq\frac{4}{n^3+4n^2+3n}\cdot n-\frac{2}{n^2+3n+2}=\frac{4}{n^2+4n+3}\cdot n-\frac{2}{n^2+3n+2}\geq0\]

which means the sequence $a_n$ is monotonically decreasing.
\[0\leq a_n\leq\frac{1}{\frac{n^2-n}{2}}\cdot n=\frac{2}{n-1}\]

so $\lim_{n\to\infty}a_n=0$ because $\lim_{n\to\infty}\frac{2}{n-1}=0$. Therefore the series converges by Leibniz criterion.
$\sum_{n=1}^\infty\frac{1}{n}$ diverges by integral test, so the series is not absolutely convergent.





\paragraph{1.1.12}
\[\beta(2)=1-\sum_{k=1}^\infty\frac{16k}{(16k^2-1)^2}=1-\sum_{k=1}^{40}\frac{16k}{(16k^2-1)^2}-\sum_{k=41}^\infty\frac{16k}{(16k^2-1)^2}\]

\[\int_{41}^\infty\frac{16x}{(16x^2-1)^2}\,dx\leq\sum_{k=41}^\infty\frac{16k}{(16k^2-1)^2}\leq\int_{41}^\infty\frac{16x}{(16x^2-1)^2}\,dx\,+\frac{16\cdot 41}{(16\cdot 41^2-1)^2}\]

\[1-\sum_{k=1}^{40}\frac{16k}{(16k^2-1)^2}=0.915\,984\,644\]
\[\int_{41}^\infty\frac{16x}{(16x^2-1)^2}\,dx=\frac{-1}{2(16x^2-1)}\Big|_{41}^\infty=0.000\,018\,591\]
\[\frac{16\cdot 41}{(16\cdot 41^2-1)^2}=0.000\,000\,907\]
\[0.915965146\leq\beta(2)\leq0.915966053\]

So $\beta(2)=0.915966$ (to six-digit accuracy).

\paragraph{1.1.13}
\[\zeta(2)+a\alpha_1+b\alpha_2=\sum_{n=1}^\infty(\frac{1}{n^2}+\frac{a}{n(n+1)}+\frac{b}{n(n+1)(n+2)})=\frac{(1+a)n^2+(3+2a+b)n+2}{n^2(n+1)(n+2)}\]

\[\zeta(2)-\alpha_1-\alpha_2=\frac{2}{n^2(n+1)(n+2)}\]

\paragraph{1.1.14}
\[\sum_{n=0}^\infty \frac{1}{(2n+1)^3}+\sum_{n=1}^\infty\frac{1}{(2n)^3}=\sum_{n=1}^\infty\frac{1}{n^3}\]

\[\lambda(3)=\sum_{n=1}^\infty\frac{1}{n^3}-\sum_{n=1}^\infty\frac{1}{(2n)^3}=\frac{7}{8}\sum_{n=1}^\infty\frac{1}{n^3}=\frac{7}{8}\zeta(3)\]
\[\lambda(3)=1.051800\]

to six decimal place.

\paragraph{1.1.15}
(a) \[\sum_{n=2}^\infty[\zeta(n)-1]=\sum_{n=2}^\infty(\sum_{k=1}^\infty\frac{1}{k^n}-1)=\sum_{n=2}^\infty\sum_{k=2}^\infty\frac{1}{k^n}=\sum_{k=2}^\infty\sum_{n=2}^\infty\frac{1}{k^n}=\sum_{k=2}^\infty\frac{\frac{1}{k^2}}{1-\frac{1}{k}}=\sum_{k=2}^\infty(\frac{1}{k-1}-\frac{1}{k})=1\]

(b) \[\sum_{n=2}^\infty(-1)^n[\zeta(n)-1]=\sum_{n=2}^\infty(-1)^n(\sum_{k=1}^\infty\frac{1}{k^n}-1)=\sum_{n=2}^\infty(-1)^n\sum_{k=2}^\infty\frac{1}{k^n}=\sum_{k=2}^\infty\sum_{n=2}^\infty(-1)^n\frac{1}{k^n}\]

\[=\sum_{k=2}^\infty\frac{\frac{1}{k^2}}{1-(-\frac{1}{k})}=\sum_{k=2}^\infty(\frac{1}{k}-\frac{1}{k+1})=\frac{1}{2}\]

\paragraph{1.1.16}
(a) \[\zeta(3)-\alpha_2'=1+\sum_{n=1}^\infty(\frac{1}{n^3}-\frac{1}{(n-1)n(n+1)})=1+\sum_{n=2}^\infty\frac{-1}{(n-1)n^3(n+1)}\]
\[\zeta(3)=\frac{5}{4}-\sum_{n=2}^\infty\frac{1}{n^3(n^2-1)}\]

(b) \[\zeta(3)+\alpha_4'=\frac{5}{4}-\sum_{n=2}^\infty\frac{1}{(n-1)n^3(n+1)}+\sum_{n=3}^\infty\frac{1}{(n-2)(n-1)n(n+1)(n+2)}\]
\[=\frac{29}{24}+\sum_{n=3}^\infty\frac{4}{(n-2)(n-1)n^3(n+1)(n+2)}\]
\[\zeta(3)=\frac{115}{96}+\sum_{n=3}^\infty\frac{4}{(n-2)(n-1)n^3(n+1)(n+2)}\]

(c) 
\[\int_{N}^\infty\frac{1}{x^3}\,dx\leq\sum_{n=N}^\infty\frac{1}{n^3}\leq\int_{N}^\infty\frac{1}{x^3}\,dx+\frac{1}{N^3}\]

$\frac{1}{126^3}=4.999\times10^{-7}<5\times10^{-7}$, so 125 terms are required.

\[\int_{N}^\infty\frac{1}{x^3(x^2-1)}\,dx\leq\sum_{n=N}^\infty\frac{1}{n^3(n^2-1)}\leq\int_{N}^\infty\frac{1}{x^3(x^2-1)}\,dx+\frac{1}{N^3(N^2-1)}\]

$\frac{1}{19^3(19^2-1)}=4\times10^{-7}<5\times10^{-7}$, so 17 terms ($n=2$ to $n=18$) are required.

\[\int_{N}^\infty\frac{4}{x^3(x^2-1)(x^2-4)}\,dx\leq\sum_{n=N}^\infty\frac{1}{n^3(n^2-1)(n^2-4)}\leq\int_{N}^\infty\frac{4}{x^3(x^2-1)(x^2-4)}\,dx+\frac{4}{N^3(N^2-1)(N^2-4)}\]

$\frac{4}{10^3(10^2-1)(10^2-4)}=4.2\times10^{-7}<5\times10^{-7}$, so 7 terms ($n=3$ to $n=9$) are required.

