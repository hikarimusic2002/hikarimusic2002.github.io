---
layout: splash
title: "Principles of Mathematical Analysis Ch3"
permalink: /solutions/real_analysis_03
author_profile: false

---

# Chapter 3: Numerical Sequences and Series

{% raw %}

### 1.

Let $\newcommand{\V}{\mathbf} \{s_n\}$ converges to $s$, so for every $\varepsilon>0$, there is an integer $N$ such that $n\geq N$ implies $\vert s_n-s\vert <\varepsilon$. By Problem 1.13, $\big\vert \vert s_n\vert -\vert s\vert  \big\vert <\vert s_n-s\vert <\varepsilon$, so for every $\varepsilon>0$, there is an integer $N$ such that $n\geq N$ implies $\big\vert \vert s_n\vert -\vert s\vert  \big\vert <\varepsilon$, which means $\{\vert s_n\vert \}$ converges to $\vert s\vert $.

The converse is not true. Let $s_n=(-1)^n$, then $\{\vert s_n\vert \}$ converges to $1$, but $\{s_n\}$ diverges.

-----

### 2.

$$
\begin{aligned}
\lim_{n\to\infty}(\sqrt{n^2+n}-n)=\lim_{n\to\infty}\frac{n}{\sqrt{n^2+n}+n}=\lim_{n\to\infty}\frac{1}{\sqrt{1+\frac{1}{n}}+1}=\frac{1}{2}
\end{aligned}
$$


-----

### 3.

$s_1<2$. If $s_k<2$, then $s_{k+1}=\sqrt{2+\sqrt{s_k}}<\sqrt{2+\sqrt{2}}<2$, so $s_n<2$ for every $n$ by induction. $s_2>s_1$. If $s_k>s_{k-1}$, then $\sqrt{2+\sqrt{s_k}}>\sqrt{2+\sqrt{s_{k-1}}}$, which means $s_{k+1}>s_k$. s o $\{s_n\}$ is monotonically increasing by induction. By Theorem 3.14, $\{s_n\}$ being monotonic and bounded implies convergence.

-----

### 4.

$s_{2m+1}=1-\frac{1}{2^m}$ holds for $m=0$. If it holds for $m=k$, so $s_{2k+1}=1-\frac{1}{2^k}$, then $s_{2(k+1)+1}=\frac{1}{2}+s_{2k+2}=\frac{1}{2}+\frac{s_{2k+1}}{2}=1-\frac{1}{2^{k+1}}$, which means it also holds for $m=k+1$. So $s_{2m+1}=1-\frac{1}{2^m}$ holds for every $m$ by induction.

$s_{2m}=\frac{1}{2}-\frac{1}{2^m}$ holds for $m=1$. If it holds for $m=k$, so $s_{2k}=\frac{1}{2}-\frac{1}{2^k}$, then $s_{2(k+1)}=\frac{s_{2k+1}}{2}=\frac{1}{4}+\frac{s_{2k}}{2}=\frac{1}{2}-\frac{1}{2^{k+1}}$, which means it also holds for $m=k+1$. So $s_{2m}=\frac{1}{2}-\frac{1}{2^m}$ holds for every $m$ by induction. 

$\{s_{2m+1}\}=\{1-\frac{1}{2^m}\}$ converges to $1$, so $1$ is a subsequential limit of $\{s_n\}$. If $x>1$, then for every $n$ we have $s_n<1<x$. By Theorem 3.17, $1$ is the upper limit of $\{s_n\}$.

$\{s_{2m}\}=\{\frac{1}{2}-\frac{1}{2^m}\}$ converges to $\frac{1}{2}$, so $\frac{1}{2}$ is a subsequential limit of $\{s_n\}$. If $x<\frac{1}{2}$, let $x=\frac{1}{2}-\varepsilon$ where $\varepsilon>0$, and let $N$ be an integer such that $N>-\log_2\varepsilon$, then $s_n\geq\frac{1}{2}-\frac{1}{2^n}>\frac{1}{2}-\varepsilon=x$ for all $n\geq N$. By Theorem 3.17, $\frac{1}{2}$ is the lower limit of $\{s_n\}$.

-----

### 5.

If at least one of  $\limsup_{n\to\infty}a_n$ and $\limsup_{n\to\infty}b_n$ equals to $+\infty$, and the other does not equal to $-\infty$, then 

$$
\begin{aligned}
\limsup_{n\to\infty}(a_n+b_n)=\infty=\limsup_{n\to\infty}a_n+\limsup_{n\to\infty}b_n
\end{aligned}
$$

the inequality holds.

For the rest of the case, we have $\limsup_{n\to\infty}a_n<+\infty$ and $\limsup_{n\to\infty}<+\infty$. By Theorem 3.17, $\limsup_{n\to\infty}(a_n+b_n)$ is also a subsequential limit of $\{a_n+b_n\}$, so there is a subsequence $\{a_{n_k}+b_{n_k}\}$ such that 

$$
\begin{aligned}
    \limsup_{n\to\infty}(a_n+b_n)=\lim_{k\to\infty}(a_{n_k}+b_{n_k}) \tag{1}
\end{aligned}
$$

$\limsup_{k\to\infty}a_{n_k}$, the upper limit of $\{a_{n_k}\}$, is also a subsequential limit of $\{a_{n_k}\}$, so there is a subsequence $\{a_{n_{k_j}}\}$ such that

$$
\begin{aligned}
\lim_{j\to\infty}a_{n_{k_{j}}}=\limsup_{k\to\infty}a_{n_k}
\end{aligned}
$$

$\{a_{n_k}+b_{n_k}\}$ converges, so every subsequential limit equals to $\lim_{k\to\infty}(a_{n_k}+b_{n_k})$, which means

$$
\begin{aligned}
    \lim_{k\to\infty}(a_{n_k}+b_{n_k})=\lim_{j\to\infty}(a_{n_{k_j}}+b_{n_{k_j}}) \tag{2}
\end{aligned}
$$


Both $\{a_{n_{k_j}}+b_{n_{k_j}}\}$ and $\{a_{n_{k_j}}\}$ converge, so $\{b_{n_{k_j}}\}$ also converges, and we have

$$
\begin{aligned}
    \lim_{j\to\infty}(a_{n_{k_j}}+b_{n_{k_j}})=\lim_{j\to\infty}a_{n_{k_j}}+\lim_{j\to\infty}b_{n_{k_j}} \tag{3}
\end{aligned}
$$

$\lim_{j\to\infty}b_{n_{k_j}}$ is a subsequential limit of $\{b_{n_k}\}$, so we have

$$
\begin{aligned}
\lim_{j\to\infty}b_{n_{k_j}}\leq\limsup_{k\to\infty}b_{n_k}
\end{aligned}
$$

Therefore, we have

$$
\begin{aligned}
    \lim_{j\to\infty}a_{n_{k_j}}+\lim_{j\to\infty}b_{n_{k_j}}\leq\limsup_{k\to\infty}a_{n_k}+\limsup_{k\to\infty}b_{n_k} \tag{4}
\end{aligned}
$$

It is obvious that 

$$
\begin{aligned}
\limsup_{k\to\infty}a_{n_k}\leq \limsup_{n\to\infty}a_n
\end{aligned}
$$

and also

$$
\begin{aligned}
\limsup_{k\to\infty}b_{n_k}\leq \limsup_{n\to\infty}b_n
\end{aligned}
$$

so we have

$$
\begin{aligned}
    \limsup_{k\to\infty}a_{n_k}+\limsup_{k\to\infty}b_{n_k}\leq\limsup_{n\to\infty}a_n+\limsup_{n\to\infty}b_n \tag{5}
\end{aligned}
$$

Combining equation (1) to (5), we have

$$
\begin{aligned}
\limsup_{n\to\infty}(a_n+b_n)\leq\limsup_{n\to\infty}a_n+\limsup_{n\to\infty}b_n
\end{aligned}
$$

-----

### 6.

(a)

$$
\begin{aligned}
a_n=\sqrt{n+1}-\sqrt{n}=\frac{1}{\sqrt{n+1}+\sqrt{n}}>\frac{1}{2\sqrt{n+1}}
\end{aligned}
$$

$\sum\frac{1}{2(n+1)^{1/2}}$ diverges by Theorem 3.28, so $\sum a_n$ diverges by comparison test.

(b)

$$
\begin{aligned}
a_n=\frac{\sqrt{n+1}-\sqrt{n}}{n}=\frac{1}{n(\sqrt{n+1}+\sqrt{n})}<\frac{1}{n\cdot2\sqrt{n}}
\end{aligned}
$$

$\sum\frac{1}{2n^{3/2}}$ converges by Theorem $3.28$, so $\sum a_n$ converges by comparison test.


(c)

$$
\begin{aligned}
\limsup_{n\to\infty}\sqrt[n]{\vert a_n\vert }=\lim_{n\to\infty}(\sqrt[n]{n}-1)=0
\end{aligned}
$$

so $\sum a_n$ converges by root test.

(d)
For $\vert z\vert \leq1$, 

$$
\begin{aligned}
\lim_{n\to\infty}\vert a_n\vert =\lim_{n\to\infty}\frac{1}{\vert 1+z^n\vert }\geq\lim_{n\to\infty}\frac{1}{1+\vert z\vert ^n}=
\begin{cases}
1,\quad & \vert z\vert <1\\
\frac{1}{2},\quad & \vert z\vert =1
\end{cases}
\end{aligned}
$$

which is not zero, so $\sum a_n$ diverges by Theorem 3.23.

For $\vert z\vert >1$, 

$$
\begin{aligned}
\limsup_{n\to\infty}\left\vert \frac{a_{n+1}}{a_n} \right\vert =\limsup_{n\to\infty}\frac{\vert 1+z^n\vert }{\vert 1+z^{n+1}\vert }\leq\limsup_{n\to\infty}\frac{\vert z\vert ^n+1}{\vert z\vert ^{n+1}-1}=\frac{1}{\vert z\vert }<1
\end{aligned}
$$

so $\sum a_n$ converges by ratio test

-----

### 7.

$$
\begin{aligned}
(\sqrt{a_n}-\frac{1}{n})^2&=a_n+\frac{1}{n^2}-\frac{2\sqrt{a_n}}{n}\geq0\\
\frac{\sqrt{a_n}}{n}&\leq\frac{a_n}{2}+\frac{1}{2n^2}
\end{aligned}
$$

$\sum\frac{a_n}{2}$ and $\sum\frac{1}{2n^2}$ converges, so $\sum\frac{\sqrt{a_n}}{2}$ converges by comparison test.

-----

### 8.

Being monotonic and bounded implies convergence, so let $\lim_{n\to\infty}b_n=b$. If $\{b_n\}$ is increasing, let $d_n=b-b_n$, then $d_0\geq d_1\geq d_2\geq\cdots$, and $\lim_{n\to\infty}d_n=0$.

$$
\begin{aligned}
\sum a_nb_n=\sum a_nb-\sum a_nd_n
\end{aligned}
$$

$\sum a_nb$ converges because $\sum a_n$ converges. $\sum a_nd_n$ converges by Theorem $3.42$ because $\sum a_n$ is bounded and $d_n$ satisfy the conditions. Therefore, $\sum a_nb_n$ converges.

If $\{b_n\}$ is decreasing, let $d_n=b_n-b$, then the convergence can be proved similarly.

-----

### 9.

(a)
The series converges when 

$$
\begin{aligned}
\limsup_{n\to\infty}\left\vert \frac{(n+1)^3z^{n+1}}{n^3z^n} \right\vert =\vert z\vert \limsup_{n\to\infty}\left\vert \frac{(n+1)^3}{n^3} \right\vert =\vert z\vert <1
\end{aligned}
$$

so the radius of convergence $R=1$.


(b)
The series converges when 

$$
\begin{aligned}
\limsup_{n\to\infty}\left\vert \frac{\frac{2^{n+1}}{(n+1)!}z^{n+1}}{\frac{2^n}{n!}z^n} \right\vert =\vert z\vert \limsup_{n\to\infty}\left\vert \frac{2}{n+1} \right\vert =0<1
\end{aligned}
$$


so the radius of convergence $R=\infty$.


(c)
The series converges when 

$$
\begin{aligned}
\limsup_{n\to\infty}\left\vert \frac{\frac{2^{n+1}}{(n+1)^2}z^{n+1}}{\frac{2^n}{n^2}z^n} \right\vert =\vert z\vert \limsup_{n\to\infty}\left\vert \frac{2n^2}{(n+1)^2} \right\vert =2\vert z\vert <1
\end{aligned}
$$

so the radius of convergence $R=\frac{1}{2}$.


(d)
The series converges when 

$$
\begin{aligned}
\limsup_{n\to\infty}\left\vert \frac{\frac{(n+1)^3}{3^{n+1}}z^{n+1}}{\frac{n^3}{3^n}z^n} \right\vert =\vert z\vert \limsup_{n\to\infty}\left\vert \frac{(n+1)^3}{3n^3} \right\vert =\frac{\vert z\vert }{3}<1
\end{aligned}
$$

so the radius of convergence $R=3$.

-----

### 10.

For every positive integer $N$, there is an integer $n$ such that $a_n\neq0$. Because $\vert a_n\vert \geq1$, we have $\sqrt[n]{\vert a_n\vert }\geq1$. Therefore, 

$$
\begin{aligned}
\alpha&=\limsup_{n\to\infty}\sqrt[n]{\vert a_n\vert }\geq1\\
R&=\frac{1}{\alpha}\leq1
\end{aligned}
$$

-----

### 11.

(a) If $\{a_n\}$ is not bounded, then $\lim_{n\to\infty}a_n=\infty\;or\,-\infty$, so

$$
\begin{aligned}
\lim_{n\to\infty}\frac{a_n}{1+a_n}=1\neq0
\end{aligned}
$$

which means $\sum\frac{a_n}{1+a_n}$ diverges by Theorem 3.23.

If $\{a_n\}$ is bounded, so there is a $M$ such that $\vert a_n\vert <M$ for every $n$, then

$$
\begin{aligned}
\frac{a_n}{1+a_n}\geq\frac{a_n}{1+M}
\end{aligned}
$$

$\sum\frac{a_n}{1+M}$ diverges because $\sum a_n$ diverges, so $\sum\frac{a_n}{1+a_n}$ diverges by comparison test.


(b)
$a_n>0$, so $s_n$ is monotonically increasing, and $s_{N+1},s_{N+2},\cdots\leq s_{N+k}$. Therefore, 

$$
\begin{aligned}
\frac{a_{N+1}}{s_{N+1}}+\cdots+\frac{a_{N+k}}{s_{N+k}}\geq\frac{a_{N+1}}{s_{N+k}}+\cdots+\frac{a_{N+k}}{s_{N+k}}=1-\frac{s_N}{s_{N+k}}
\end{aligned}
$$

$s_n$ is monotonically increasing but diverges, which implies that it is not bounded, so $\lim_{n\to\infty}s_n=\infty\,or-\infty$. For every integer $N$,

$$
\begin{aligned}
\lim_{k\to\infty}\left\vert \sum_{n=N+1}^{N+k}\frac{a_n}{s_n} \right\vert \geq\lim_{k\to\infty}\left\vert 1-\frac{s_N}{s_{N+k}} \right\vert =1
\end{aligned}
$$

so for $\varepsilon<1$, the Cauchy criterion (Theorem 3.11) is not satisfied, which means $\sum\frac{a_n}{s_n}$ diverges.


(c)

$$
\begin{aligned}
\frac{a_n}{s_n^2}=\frac{s_{n}-s_{n-1}}{s_n^2}\leq\frac{s_n-s_{n-1}}{s_n\cdot s_{n-1}}=\frac{1}{s_{n-1}}-\frac{1}{s_n}
\end{aligned}
$$

Because $\lim_{n\to\infty}s_n=\infty\,or-\infty$, so

$$
\begin{aligned}
\sum_{n=2}^\infty\left(\frac{1}{s_{n-1}}-\frac{1}{s_n} \right)=\frac{1}{s_1}-\lim_{n\to\infty}\frac{1}{s_n}=\frac{1}{s_1}
\end{aligned}
$$

which is convergent, so $\frac{a_n}{s_n^2}$ converges by comparison test.


(d)
$\sum\frac{a_n}{1+a_n}$ may be convergent or divergent. For example, let $a_n=1$ for every $n$, then

$$
\begin{aligned}
\sum\frac{a_n}{1+na_n}=\sum\frac{1}{n+1}
\end{aligned}
$$

which is divergent. On the other hand, let

$$
\begin{aligned}
a_n=
\begin{cases}
1,\quad & n=m^2,\quad m\in\mathbb{N}\\
\frac{1}{n^2},\quad & otherwise
\end{cases}
\end{aligned}
$$

Then

$$
\begin{aligned}
\sum_{n=1}^N\frac{a_n}{1+na_n}=\sum_{m=1}^\infty\frac{1}{1+m^2}+\sum_{\substack{n=1\\n\neq m^2}}^\infty\frac{\frac{1}{n^2}}{1+n\cdot\frac{1}{n^2}}
\end{aligned}
$$

The first series converges because 

$$
\begin{aligned}
\frac{1}{1+m^2}<\frac{1}{m^2}
\end{aligned}
$$

and $\sum\frac{1}{m^2}$ converges. The second series converges because 

$$
\begin{aligned}
\frac{\frac{1}{n^2}}{1+n\cdot\frac{1}{n^2}}=\frac{1}{n(n+1)}<\frac{1}{n^2}
\end{aligned}
$$

and $\sum\frac{1}{n^2}$ converges. Therefore, $\sum\frac{a_n}{1+na_n}$ converges.

-----

### 12.

(a)
$a_n>0$, so $s_n=\sum_{m=1}^n a_m$ is monotonically increasing, and $r_n=\sum_{m=n}^\infty a_m$ is monotonically decreasing, which means $r_m>r_{m+1},\cdots,r_{n}$. Therefore,

$$
\begin{aligned}
\frac{a_m}{r_m}+\cdots+\frac{a_n}{r_n}>\frac{a_m}{r_m}+\cdots+\frac{a_n}{r_m}=1-\frac{r_{n+1}}{r_m}>1-\frac{r_n}{r_m}
\end{aligned}
$$

By Cauchy criterion, $\lim_{n\to\infty}r_n=0$. For every positive integer $N$,

$$
\begin{aligned}
\lim_{k\to\infty}\left\vert \sum_{n=N}^k\frac{a_n}{r_n} \right\vert >\lim_{k\to\infty}\left\vert 1-\frac{r_k}{r_N} \right\vert =1
\end{aligned}
$$

so the Cauchy criterion (Theorem 3.22) cannot be satisfied, which means $\sum\frac{a_n}{r_n}$ diverges.


(b)
$r_n\neq r_{n+1}$, so 

$$
\begin{aligned}
(\sqrt{r_n}-\sqrt{r_{n+1}})^2&>0\\
r_n-2\sqrt{r_n}\sqrt{r_{n+1}}+r_{n+1}&>0\\
2r_n-2\sqrt{r_n}\sqrt{r_{n+1}}&>r_n-r_{n+1}\\
2(\sqrt{r_n}-\sqrt{r_{n+1}})&>\frac{r_n-r_{n+1}}{\sqrt{r_n}}=\frac{a_n}{\sqrt{r_n}}
\end{aligned}
$$

We have

$$
\begin{aligned}
\sum_{n=1}^\infty2(\sqrt{r_n}-\sqrt{r_{n+1}})=2\sqrt{r_1}-\lim_{n\to\infty}2\sqrt{r_{n}}=2\sqrt{r_1}
\end{aligned}
$$

which is convergent, so $\sum\frac{a_n}{\sqrt{r_n}}$ converges by comparison test.

-----

### 13.

Let $\sum a_n$ and $\sum  b_n$ be two absolutely convergent series, and let $c_n=\sum_{k=0}^n a_kb_{n-k}$. Let $d_n$ be the Cauchy product of $\sum\vert a_n\vert $ and $\sum\vert b_n\vert $, which is

$$
\begin{aligned}
d_n=\sum_{k=0}^n\vert a_k\vert \vert b_{n-k}\vert =\sum_{k=0}^n\vert a_k b_{n-k}\vert 
\end{aligned}
$$

Both $\sum\vert a_n\vert $ and $\sum\vert b_n\vert $ converges absolutely, so $\sum d_n$ converges by Theorem 3.50.

$$
\begin{aligned}
\vert c_n\vert =\left\vert \sum_{k=0}^n a_kb_{n-k} \right\vert \leq\sum_{k=0}^n\vert a_k b_{n-k}\vert =d_n
\end{aligned}
$$

$\sum d_n$ converges, so $\sum\vert c_n\vert $ converges by comparison test, which means $\sum c_n$ converges absolutely.

-----

### 14.

(a)
For every $\varepsilon>0$, let $N$ be a positive integer such that $\vert s_n-s\vert <\frac{\varepsilon}{2}$ for $n>N$. Let $M$ be a positive integer such that $\frac{(s_0-s)+\cdots+(s_N-s)}{M}<\frac{\varepsilon}{2}$. Then for $n>\max(N,M)$, we have

$$
\begin{aligned}
\sigma_n-s=\frac{(s_0-s)+\cdots+(s_n-s)}{n+1}<\frac{(s_0-s)+\cdots+(s_N-s)}{M}+\frac{(s_{N+1}-s)+\cdots+(s_n-s)}{n-N}<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon
\end{aligned}
$$
$$\begin{aligned}

\end{aligned}$$
which means $\lim\sigma_n=s$.


(b)
Let $s_n=(-1)^n$, then $\{s_n\}$ diverges, but $\lim\sigma_n=0$ because $(s_0+\cdots+s_n)\leq1$ and $\lim\frac{1}{n+1}=0$.


(c)
Let $s_n$ be 

$$
\begin{aligned}
s_n=\begin{cases}
m,\quad & n=m^3,\;m\in\mathbb{N}\\
\frac{1}{2^n},\quad & otherwise
\end{cases}
\end{aligned}
$$

then $\limsup s_n=\infty$ because it is not bounded.

$$
\begin{aligned}
\sigma_n\leq\frac{\frac{1}{2^0}+\cdots+\frac{1}{2^n}}{n+1}+\frac{1+\cdots+M}{n+1}\leq\frac{2}{n+1}+\frac{M^2}{n+1}\leq\frac{2}{n+1}+n^{-\frac{1}{3}}
\end{aligned}
$$

where $M$ is the largest positive integer such that $M^3\leq n$. We have $\lim\frac{2}{n+1}=\lim n^{-\frac{1}{3}}=0$, and $\sigma_n\geq0$, so $\lim\sigma_n=0$.


(d)

$$
\begin{aligned}
s_n-\sigma_n=\frac{ns_n-\sum_{k=0}^{n-1}s_k}{n+1}=\frac{\sum_{k=1}^n ks_k-\sum_{k=0}^{n-1}(k+1)s_k}{n+1}=\frac{\sum_{k=1}^n(ks_k-ks_{k-1})}{n+1}=\frac{\sum_{k=1}^n ka_k}{n+1}
\end{aligned}
$$

Note that $\frac{\sum_{k=0}^n ka_k}{n+1}$ is the arithmetic means of the sequence $\{na_n\}$, so by (a), $\lim(na_n)=0$ implies $\lim(s_n-\sigma_n)=0$, which is $\lim s_n=\lim\sigma_n$.


(e)
For $m<n$,

$$
\begin{aligned}
        & \quad\;\frac{m+1}{n-m}(\sigma_n-\sigma_m)+\frac{\sum_{i=m+1}^n(s_n-s_i)}{n-m}\\
        & =\frac{m+1}{n-m}\sigma_n-\frac{\sum_{i=0}^m s_i}{n-m}+\frac{(n-m)s_n}{n-m}-\frac{\sum_{i=m+1}^n s_i}{n-m}\\
        & =\frac{(n-m)s_n}{n-m}+\frac{m+1}{n-m}\sigma_n-\frac{\sum_{i=0}^n s_i}{n-m}\\
        & =s_n+\frac{m+1}{n-m}\sigma_n-\frac{n+1}{n-m}\sigma_n\\
        & =s_n-\sigma_n
\end{aligned}
$$

For $i\geq m+1$,

$$
\begin{aligned}
\vert s_n-s_i\vert &=\left\vert \sum_{k=i+1}^n(s_k-s_{k-1}) \right\vert \leq\sum_{k=i+1}^n\vert s_k-s_{k-1}\vert =\sum_{k=i+1}^n\vert a_k\vert\\
\sum_{k=i+1}^n\vert a_k\vert &\leq\sum_{k=i+1}^n\frac{M}{k}\leq\sum_{k=i+1}^n\frac{M}{i+1}=\frac{(n-i)M}{i+1}\leq\frac{(n-m-1)M}{m+2}
\end{aligned}
$$

For $\varepsilon>0$, let $m$ be the integer such that 

$$
\begin{aligned}
m\leq\frac{n-\varepsilon}{1+\varepsilon}<m+1
\end{aligned}
$$

form which we have

$$
\begin{aligned}
\frac{m+1}{n-m}\leq\frac{1}{\varepsilon}\qquad\frac{n-m-1}{m+2}<\varepsilon
\end{aligned}
$$

We have $\lim_{n\to\infty}\frac{m+1}{n-m}(\sigma_n-\sigma_m)=0$, and

$$
\begin{aligned}
\frac{1}{n-m}\sum_{i=m+1}^n(s_n-s_i)\leq\frac{(n-m-1)M}{m+2}<M\varepsilon
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
\limsup_{n\to\infty}\vert s_n-\sigma\vert <M\varepsilon
\end{aligned}
$$

Since $\varepsilon$ is arbitrary, $\lim s_n=\sigma$.

-----

### 15.

* _Theorem 3.22_ :
From Theorem 3.11, in $R^k$, a sequence converges if and only if it is a Cauchy sequence. Therefore, $s_n=\sum a_n$ converges if and only if for every $\varepsilon>0$, there is an integer $N=N'+1$ such that
$$\begin{aligned}
\vert s_m-s_{n-1}\vert =\left\vert \sum_{k=n}^m a_k \right\vert \leq \varepsilon
\end{aligned}$$
if $m\geq n\geq N'+1=N$.

* _Theorem 3.23_ :
By taking $m=n$, we have

$$
\begin{aligned}
\vert a_n\vert \leq\varepsilon\qquad(n\geq N)
\end{aligned}
$$

which means $\lim\vert a_n\vert =\lim a_n=0$.

* _Theorem 3.25_ :
The proof is identical with that in the text because $\left\vert \sum_{k=n}^m a_k \right\vert \leq\sum_{k=m}^n\vert a_k\vert$ holds in every $R^k$.

* _Theorem 3.33_ :
The proof is identical with that in the text because the comparison text (Theorem 3.25) and Theorem 3.23 holds in every $R^k$.

* _Theorem 3.34_ :
The proof is identical with that in the text as Theorem 3.33.

* _Theorem 3.42_ :
The proof is identical with that in the text because the Cauchy criterion (Theorem 3.22) holds in every $R^k$.

* _Theorem 3.45_ :
The proof is identical with that in the text because the equality and Cauchy criterion hold in every $R^k$.

* _Theorem 3.47_ :
The proof is identical with that in the text because the proof of the limit rules (Theorem 3.3) holds in every $R^k$.

* _Theorem 3.55_ :
The proof is identical with that in the text because the Cauchy criterion holds in every $R^k$.

-----

### 16.

(a)
$x_1>\sqrt{\alpha}$. If $x_n>\sqrt{\alpha}$, then $x_{n+1}>\sqrt{\alpha}$ because

$$
\begin{aligned}
(x_n-\sqrt{\alpha})^2&>0\\
\frac{x_n^2+\alpha}{2x_n}&>\frac{2x_n\sqrt{\alpha}}{2x_n}\\
x_{n+1}&>\sqrt{\alpha}
\end{aligned}
$$

So by induction, $x_n>\sqrt{\alpha}$ for every $n$. From $x_n^2>\alpha$, we have

$$
\begin{aligned}
x_{n+1}=\frac{1}{2}\left(x_n+\frac{\alpha}{x_n}\right)<\frac{1}{2}\left(x_n+x_n\right)=x_n
\end{aligned}
$$

So $\{x_n\}$ decreases monotonically. Along with the fact that $\{x_n\}$ is bounded below, $\{x_n\}$ converges. Let $\lim x_n=x$, then

$$
\begin{aligned}
\lim_{n\to\infty} x_{n+1}=\lim_{n\to\infty}\frac{1}{2}\left(x_n+\frac{\alpha}{x_n}\right)=\frac{x}{2}+\frac{\alpha}{2x}=\lim_{n\to\infty} x_n=x
\end{aligned}
$$

Solving for $x$, we have

$$
\begin{aligned}
\lim_{n\to\infty }x_n=\sqrt{\alpha}
\end{aligned}
$$

(b)

$$
\begin{aligned}
\varepsilon_{n+1}=\frac{1}{2}\left(x_n+\frac{\alpha}{x_n} \right)-\sqrt{\alpha}=\frac{x_n^2-2x_n\sqrt{\alpha}+\alpha}{2x_n}=\frac{(x_n-\sqrt{\alpha})^2}{2x_n}=\frac{\varepsilon_n^2}{2x_n}<\frac{\varepsilon_n^2}{2\sqrt{\alpha}}
\end{aligned}
$$

Setting $\beta=2\sqrt{\alpha}$, then $\varepsilon_{n+1}<\frac{\varepsilon_n^2}{\beta}$ for every $n$. Consider the inequality 

$$
\begin{aligned}
\varepsilon_{n+1}<\beta\left(\frac{\varepsilon_1}{\beta} \right)^{2^n}
\end{aligned}
$$

It holds for $n=1$:

$$
\begin{aligned}
\varepsilon_2<\frac{\varepsilon_1^2}{\beta}=\beta\left(\frac{\varepsilon_1}{\beta} \right)^2
\end{aligned}
$$

If it holds for $n=k$:

$$
\begin{aligned}
\varepsilon_{k+1}<\beta\left(\frac{\varepsilon_1}{\beta} \right)^{2^k}
\end{aligned}
$$

then it also holds for $n=k+1$:

$$
\begin{aligned}
\varepsilon_{k+2}<\frac{\varepsilon_{k+1}^2}{\beta}<\frac{1}{\beta}\left[\beta\left(\frac{\varepsilon_1}{\beta} \right)^{2^k} \right]^2=\beta\left(\frac{\varepsilon_1}{\beta} \right)^{2^{k+1}}
\end{aligned}
$$

So the inequality holds for every $n$ by induction.


(c)
From $25<27,\;5<3\sqrt{3},\;20<12\sqrt{3},\;10(2-\sqrt{3})<2\sqrt{3}$, we have

$$
\begin{aligned}
\frac{\varepsilon_1}{\beta}=\frac{
2-\sqrt{3}}{2\sqrt{3}}<\frac{1}{10}
\end{aligned}
$$

From $2\sqrt{3}=\sqrt{12}<\sqrt{16}=4$, we have

$$
\begin{aligned}
\beta=2\sqrt{3}<4
\end{aligned}
$$

Therefore, from the inequality in (b), we have

$$
\begin{aligned}
\varepsilon_5&<4\left(\frac{1}{10} \right)^{2^4}=4\cdot10^{-16}\\
\varepsilon_6&<4\left(\frac{1}{10} \right)^{2^5}=4\cdot10^{-32}
\end{aligned}
$$

-----

### 17.

(a)(b)
$$
\begin{aligned}
x_{n+1}-\sqrt{\alpha}=\frac{\alpha+x_n}{1+x_n}-\sqrt{\alpha}=-\frac{(\sqrt{\alpha}-1)(x_n-\sqrt{\alpha})}{1+x_n}
\end{aligned}
$$

So if $x_{n}-\sqrt{\alpha}<0$,\; $x_{n+1}-\sqrt{\alpha}>0$, and if $x_n-\sqrt{\alpha}>0$,\; $x_{n+1}-\sqrt{\alpha}<0$. Because $x_1>\sqrt{\alpha}$, we have $x_1,x_3,x_5,\cdots>\sqrt{\alpha}$, and $x_2,x_4,x_6,\cdots<\sqrt{\alpha}$.

$$
\begin{aligned}
x_{n+2}=\frac{\alpha+x_{n+1}}{1+x_{n+1}}=\frac{\alpha+\frac{\alpha+x_n}{1+x_n}}{1+\frac{\alpha+x_n}{1+x_n}}=\frac{(\alpha+1)x_n+2\alpha}{2x_n+\alpha+1}=x_n+\frac{-2(x_n^2-\alpha)}{2x_n+\alpha+1}
\end{aligned}
$$

For the odd terms, $x_n^2-\alpha>0$, so $x_{n+2}<x_n$, which is $x_1>x_3>x_5>\cdots$.

For the even terms, $x_n^2-\alpha<0$, so $x_{n+2}>x_n$, which is $x_2<x_4<x_6<\cdots$.

(c)
The sequence of odd terms is monotonically decreasing and bounded below by $\sqrt{\alpha}$, so it converges. Let the limit be $x$:

$$
\begin{aligned}
\lim_{n\to\infty}x_{n+2}=\frac{(\alpha+1)x+2\alpha}{2x+\alpha+1}=\lim_{n\to\infty}x_n=x
\end{aligned}
$$

Solving for $x$, we have $x=\sqrt{\alpha}$. Similarly, the sequence of even terms being monotonically increasing and bounded above by $\sqrt{\alpha}$ implies convergence, and the limit is also $\sqrt{\alpha}$. Therefore, both the sequences of odd and even terms converging to $\sqrt{\alpha}$ implies that 

$$
\begin{aligned}
\lim_{n\to\infty}x_n=\sqrt{\alpha}
\end{aligned}
$$

(d)
Let $\delta_n=\vert x_n-\sqrt{\alpha}\vert $, then 

$$
\begin{aligned}
\delta_{n+1}=\frac{(\sqrt{\alpha}-1)\delta_n}{1+x_n}>\frac{(\sqrt{\alpha}-1)\delta_n}{1+x_1}=\gamma\delta_n
\end{aligned}
$$

where $\gamma<1$. By induction we have

$$
\begin{aligned}
\delta_{n+1}>\gamma^n\delta_1
\end{aligned}
$$

Compared with the sequence in Exercise 16:

$$
\begin{aligned}
\varepsilon_{n+1}<\beta\left(\frac{\varepsilon_1}{\beta} \right)^{2^n}
\end{aligned}
$$

The sequence $a^{2^n}$ for $a<1$ converges faster than $b^n$ for $b<1$, so for $n>N$ where $N$ is large enough, we have

$$
\begin{aligned}
\varepsilon_{n+1}<\beta\left(\frac{\varepsilon_1}{\beta} \right)^{2^n}<\gamma^n\delta_1<\delta_{n+1}
\end{aligned}
$$

which means the sequence in Exercise 16 converges faster than that in Exercise 17.

-----

### 18.
For $0<a<1$, we have

$$
\begin{aligned}
1-a^p=(1-a)(1+a+\cdots+a^{p-1})<(1-a)(1+1+\cdots+1)=p(1-a)
\end{aligned}
$$

$x_1>\sqrt[p]{\alpha}$. If $x_n>\sqrt[p]{\alpha}$, so $0<\frac{\sqrt[p]{\alpha}}{x_n}<1$, then 

$$
\begin{aligned}
1-\left(\frac{\sqrt[p]{\alpha}}{x_n} \right)^p &<p\left(1-\frac{\sqrt[p]{\alpha}}{x_n} \right)\\
\frac{x_n}{p}-\frac{\alpha}{p}x_n^{-p+1} &<x_n-\sqrt[p]{\alpha}\\
x_{n+1} &=\frac{p-1}{p}x_n+\frac{\alpha}{p}x_{n}^{-p+1} >\sqrt[p]{\alpha}
\end{aligned}
$$

So by induction, $x_n>\sqrt[p]{\alpha}$ for every $n$. From $x_n^p>\alpha$, or $x_n>\alpha x_n^{-p+1}$, we have

$$
\begin{aligned}
x_{n+1}=\frac{p-1}{p}x_n+\frac{\alpha}{p}x_n^{-p+1}<\frac{p-1}{p}x_n+\frac{1}{p}x_n=x_n
\end{aligned}
$$

So $\{x_n\}$ decreases monotonically. Along with the fact that $\{x_n\}$ is bounded below, $\{x_n\}$ converges. Let $\lim x_n=x$, then 

$$
\begin{aligned}
\lim_{n\to\infty}x_{n+1}=\lim_{n\to\infty}\left(\frac{p-1}{p}x_n+\frac{\alpha}{p}x_n^{-p+1} \right)=\frac{p-1}{p}x+\frac{\alpha}{p}x^{-p+1}=\lim_{n\to\infty}x_n=x
\end{aligned}
$$

solving for $x$, we have

$$
\begin{aligned}
\lim_{n\to\infty}x_n=\sqrt[p]{\alpha}
\end{aligned}
$$

-----

### 19.
Let the Cantor set be denoted as $P$.

If $x\in P$, then $0\leq x\leq1$, and $3x$ satisfies either the two inequalities:

$$
\begin{aligned}
0&\leq 3x\leq 1\\
2&\leq 3x\leq 3
\end{aligned}
$$

Let $\alpha_1$ be $0$ or $2$, respectively, and let $\beta_1=3x-\alpha_1$. Then $0\leq\beta_1\leq1$, and $3\beta_1$ satisfies either the two inequalities:

$$
\begin{aligned}
0&\leq3\beta_1\leq1\\
2&\leq3\beta_1\leq3
\end{aligned}
$$

Let $\alpha_2$ be $0$ or $2$, respectively, and let $\beta_2=3\beta_1-\alpha_2$. Continue the process to obtain the sequences $\{\alpha_n\}$ and $\{\beta_n\}$, where $\alpha_n$ is $0$ or $2$, and $0\leq\beta_n\leq1$ for every $n$. Then we have

$$
\begin{aligned}
x=\sum_{n=1}^N\frac{\alpha_n}{3}+\frac{\beta_N}{3}
\end{aligned}
$$

Since $\frac{\beta_N}{3^N}$ can be arbitrarily small for large enough $N$, we have

$$
\begin{aligned}
x=\lim_{N\to\infty}\sum_{n=1}^N\frac{\alpha_n}{3^n}=\sum_{n=1}^\infty\frac{\alpha_n}{3^n}
\end{aligned}
$$

which means that $x\in X(a)$. Therefore, $P\subset X(a)$.


If $x\not\in P$, then for some $N$ we have $1<3\beta_n<2$, so

$$
\begin{aligned}
x&=\sum_{n=1}^N\frac{\alpha_n}{3^n}+\frac{\beta_N}{3^N}\\
\sum_{n=1}^N\frac{\alpha_n}{3^n}+\frac{1}{3^{N+1}}<x&<\sum_{n=1}^N\frac{\alpha_n}{3^n}+\frac{2}{3^{N+1}}
\end{aligned}
$$

so if $x=\sum_{n=1}^\infty\frac{\alpha_n}{3^n}$, then $\alpha_{N+1}$ cannot be $0$ or $2$, which means $x\not\in X(a)$. Therefore, $X(a)\subset P$.


From $P\subset X(a)$ and $X(a)\subset P$, we have $X(a)=P$.

-----

### 20.
For every $\varepsilon>0$, let $N_1$ be the positive integer such that for $n,m\geq N_1$,

$$
\begin{aligned}
d(p_n,p_m)<\frac{\varepsilon}{2}
\end{aligned}
$$

Let $N_2$ be the positive integer such that for $n_i\geq N_2$,

$$
\begin{aligned}
d(p_{n_i},p)<\frac{\varepsilon}{2}
\end{aligned}
$$

Let $N=\max(N_1,N_2)$. Then for $n\geq N$, choose $n_i\geq N$, and we have

$$
\begin{aligned}
d(p_n,p)\leq d(p_n,p_{n_i})+d(p_{n_i},p)<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon
\end{aligned}
$$

which implies $\{p_n\}$ converges to $p$.

-----

### 21.
Construct a sequence $\{x_n\}$ such that $x_n\in E_n$ for each $n$. Because $E_n\supset E_{n+1}$,\;\;$E_n$ contains the points $x_n,x_{n+1},x_{n+2},\cdots$, and therefore $\lim\mathrm{diam}\,E_n=0$ implies that $\{x_n\}$ is a Cauchy sequence. Since the metric space is complete, $\{x_n\}$ converges to a point $x$. Since $x$ is a limit point of the set of $\{x_n\}$, it is a limit point of every $E_n$, and since $E_n$ is closed, $x\in E_n$ for every $n$. Therefore,

$$
\begin{aligned}
x\in\bigcap_{n=1}^\infty E_n
\end{aligned}
$$

If $E=\bigcap_1^\infty E_n$ consists of more that one point, then $\mathrm{diam}\,E>0$. But for each $n$,\; $\mathrm{diam}\,E_n\geq\mathrm{diam}\,E$. This contradicts the assumption that $\mathrm{diam}\,E_n\to0$. Therefore, $\bigcap_1^\infty E_n$ consists of exactly one point.

-----

### 22.
Find a neighborhood $E_1$ with diameter less than $1$ such that $\overline{E_1}\subset G_1$ (it exists because $G_1$ is open). Since $G_2$ is dense, every neighborhood centered at any point contains a point of $G_2$, so $E_1\cap G_2$ is nonempty, and because both $E_1$ and $G_2$ are open, $E_1\cap G_2$ is open. Find a neighborhood $E_2$ with diameter less than $\frac{1}{2}$ such that $\overline{E_2}\subset E_1\cap G_2$. Continue the process to construct a sequence of sets $\{\overline{E_n}\}$, where $\overline{E_n}\supset\overline{E_{n+1}}$, and $\overline{E_n}\subset G_n$. Every $\overline{E_n}$ is closed, and because $0\leq\mathrm{diam}\,\overline{E_n}\leq\frac{1}{n}$,

$$
\begin{aligned}
\lim_{n\to\infty}\mathrm{diam}\,\overline{E_n}=0
\end{aligned}
$$

so by Exercise 21, there is a point $x$ contained in every $\overline{E_n}$, so $x$ is contained in every $G_n$, which means $\bigcap_1^\infty G_n$ is not empty.

-----

### 23.
$\{p_n\}$ and $\{q_n\}$ are Cauchy sequences, so for every $\varepsilon>0$, there is a positive integer $N_1$ such that $d(p_n,p_m)<\frac{\varepsilon}{2}$ for $n,m\geq N_1$, and a positive integer $N_2$ such that $d(q_n,q_m)<\frac{\varepsilon}{2}$ for $n,m\geq N_2$. Let $N=\max(N_1,N_2)$. For $n,m\geq N$, we have

$$
\begin{aligned}
\left\vert d(p_n,q_n)-d(p_m,q_m) \right\vert \leq d(p_n,p_m)+d(q_n,q_m)<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon
\end{aligned}
$$

which implies $\{d(p_n,q_n)\}$ is a Cauchy sequence. Since every Cauchy sequence in $R$ converges, $\{d(p_n,q_n)\}$ converges.

-----

### 24.
(a)
*  _reflexive_ :

$$
\begin{aligned}
\lim_{n\to\infty}d(p_n,p_n)=0
\end{aligned}
$$

so $\{p_n\}\sim\{p_n\}$.

*  _symmetric_ : If $\{p_n\}\sim\{q_n\}$, so $\lim d(p_n,q_n)=0$, then

$$
\begin{aligned}
\lim_{n\to\infty}d(q_n,p_n)=\lim_{n\to\infty}d(p_n,q_n)=0
\end{aligned}
$$

so $\{q_n\}\sim\{p_n\}$.

*  _transitive_ : If $\{p_n\}\sim\{q_n\}$ and $\{q_n\}\sim\{r_n\}$, so $\lim d(p_n,q_n)=\lim d(q_n,r_n)=0$, then

$$
\begin{aligned}
d(p_n,r_n)&\leq d(p_n,q_n)+d(q_n,r_n)\\
\lim_{n\to\infty}d(p_n,r_n)&=0
\end{aligned}
$$

so $\{p_n\}\sim\{r_n\}$.
 

(b)
If $\{p_n\},\{p_n'\}\in P$, and $\{q_n\},\{q_n'\}\in Q$
, then

$$
\begin{aligned}
&d(p_n',q_n')\leq d(p_n',p_n)+d(p_n,q_n)+d(q_n,q_n')\\
&\vert d(p_n',q_n')-d(p_n,q_n) \vert \leq d(p_n',p_n)+d(q_n,q_n')
\end{aligned}
$$

Since $\lim d(p_n',p_n)=\lim d(q_n,q_n')=0$, we have

$$
\begin{aligned}
\lim_{n\to\infty}d(p_n',q_n')=\lim_{n\to\infty}d(p_n,q_n)
\end{aligned}
$$

So $\Delta(P,Q)$ is unchanged if $\{p_n\}$ and $\{q_n\}$ are replaced by equivalent sequences.

Verify the three definition of distance function:

*  _Definition (a)_

$$
\begin{aligned}
\Delta(P,Q)=\lim_{n\to\infty}d(p_n,q_n)\begin{cases}
>0\quad \textit{if $P\neq Q$}\\
=0\quad \textit{if $P=Q$}
\end{cases}
\end{aligned}
$$

*  _Definition (b)_

$$
\begin{aligned}
\Delta(P,Q)=\lim_{n\to\infty}d(p_n,q_n)=\lim_{n\to\infty}d(q_n,p_n)=\Delta(Q,P)
\end{aligned}
$$

*  _Definition (c)_

$$
\begin{aligned}
\Delta(P,Q)=\lim_{n\to\infty}d(p_n,q_n)\leq\lim_{n\to\infty}d(p_n,r_n)+\lim_{n\to\infty}d(r_n,q_n)=\Delta(P,R)+\Delta(R,Q)
\end{aligned}
$$
    
So $\Delta$ is a distance function in $X^*$.

(c)
Let $\{P_n\}$ be a Cauchy sequence in $X^*$, so every $P_n$ is an equivalence class. Let $p_n=\{p_{n,m}\}$ be an element of $P_n$. so $p_n$ is a Cauchy sequence in $X$. By the definition of Cauchy sequence, there is a positive integer $N_n$ such that for $s,t\geq N_n$,

$$
\begin{aligned}
d(p_{n,s},p_{n,t})<\frac{1}{2^n}
\end{aligned}
$$

Let $q$ be a sequence in $X$ such that $q=\{q_n\}=\{p_{n,N_n}\}$.

For $\varepsilon>0$, there is a positive integer $M_1$ such that for $m,n\geq M_1$,

$$
\begin{aligned}
\Delta(P_m,P_n)<\frac{\varepsilon}{6}
\end{aligned}
$$

There is a positive integer $M_2$ such that

$$
\begin{aligned}
\frac{1}{2^{M_2}}<\frac{\varepsilon}{3}
\end{aligned}
$$

Let $M=\max(M_1,M_2)$. For $m,n\geq M$, since 

$$
\begin{aligned}
\Delta(P_m,P_n)=\lim_{k\to\infty}d(p_{m,k},p_{n,k})
\end{aligned}
$$

there is a positive integer $N_0$ such that for $k\geq N_0$,

$$
\begin{aligned}
&\left\vert d(p_{m,k},p_{n,k})-\Delta(P_m,P_n) \right\vert <\frac{\varepsilon}{6}\\
&d(p_{m,k},p_{n,k})<\frac{\varepsilon}{6}+\Delta(P_m,P_n)<\frac{\varepsilon}{3}
\end{aligned}
$$

Let $N=\max(N_0,N_m,N_n)$. Let $k$ be a positive integer such that $k\geq N$. Then

$$
\begin{aligned}
        d(q_m,q_n) & =d(p_{m,N_m},p_{n,N_n})\\
        & \leq d(p_{m,N_m},p_{m,k})+d(p_{m,k},p_{n,k})+d(p_{n,k},p_{n,N_n})\\
        & < \frac{1}{2^m}+\frac{\varepsilon}{3}+\frac{1}{2^n}\\
        & <\frac{\varepsilon}{3}+\frac{\varepsilon}{3}+\frac{\varepsilon}{3}=\varepsilon
\end{aligned}
$$

Therefore, for $\varepsilon>0$, there is a positive integer $M$ such that for $m,n\geq M$, \;$d(q_m,q_n)<\varepsilon$, which means that $q=\{q_n\}$ is a Cauchy sequence. Let $Q\in X^*$ be the equivalence class containing $q$.

$$
\begin{aligned}
\lim_{n\to\infty}\Delta(P_n,Q)=\lim_{n\to\infty}\lim_{m\to\infty}d(p_{n,m},q_n)
\end{aligned}
$$

For $m\geq N_n$, \;$d(p_{n,m},q_n)<\frac{1}{2^n}$, so

$$
\begin{aligned}
\Delta(P_n,Q)=\lim_{m\to\infty}d(p_{n,m},q_n)<\frac{1}{2^n}
\end{aligned}
$$

Because $\lim_{n\to\infty}\frac{1}{2^n}=0$,

$$
\begin{aligned}
\lim_{n\to\infty}\Delta(P_n,Q)=0
\end{aligned}
$$

which means that $\{P_n\}$ converges to $Q$. So every Cauchy sequence in $X^*$ converges, which means that $X^*$ is complete.


(d)

$$
\begin{aligned}
\Delta(P_p,P_q)=\lim_{n\to\infty}d(p,q)=d(p,q)
\end{aligned}
$$


(e)
Let $P$ be an element of $X^*$, which contains a Cauchy sequence $p=\{p_n\}$. For $\varepsilon>0$, there is a positive integer $N$ such that for $n,m\geq N$,

$$
\begin{aligned}
d(p_n,p_m)<\varepsilon
\end{aligned}
$$

Consider $p_N\in X$, and $\varphi(p_N)\in\varphi(X)$.

$$
\begin{aligned}
\Delta(P,\varphi(p_N))=\lim_{n\to\infty}d(p_n,p_N)<\varepsilon
\end{aligned}
$$

which means $\varphi(p_N)$ is contained in the neighborhood of $P$ with radius $\varepsilon$. Therefore, every neighborhood centered at any point of $X^*$ contains an element of $\varphi(X)$, which means $\varphi(X)$ is dense in $X^*$.

If $X$ is complete, then $\{p_n\}$ converges. Let $\lim_{n\to\infty}p_n=a$, then

$$
\begin{aligned}
\Delta(P,\varphi(a))=\lim_{n\to\infty}d(p_n,a)=0
\end{aligned}
$$

so $P=\varphi(a)\in\varphi(X)$. Therefore, $X^*\subset\varphi(X)$, and obviously $\varphi(X)\subset X^*$, so $\varphi(X)=X^*$.

-----

### 25.
The completion of $X$ must be a complete metric space, and contains a dense subset isometric with $X$. If $X$ is the rational numbers with the metric $d(x,y)=\vert x-y\vert$, then the real numbers with the same metric satisfies the conditions. So the completion of $Q$ is $R$.

{% endraw %}
