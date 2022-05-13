---
layout: splash
title: "Mathematical Methods for Physicists Ch5"
permalink: /solutions/math_physics_05
author_profile: false

---

# Chapter 5: Vector Spaces

## 5.1 Vectors in Function Spaces

### 5.1.1

{% raw %}

If there are two expansions of $f(x)$, so

$$
\newcommand{\br}[2]{\langle#1|#2\rangle}
\newcommand{\brr}[2]{\left\langle#1|#2\right\rangle}
\newcommand{\pdv}[2]{\frac{\partial#1}{\partial#2}}
\newcommand{\M}{\mathrm}
\newcommand{\V}{\mathbf}
\newcommand{\VE}{\mathbf{\hat{e}}}
\newcommand{\PP}[1]{\mathcal{P}_{#1}}
\newcommand{\FF}[1]{\mathcal{F}_{#1}}
\newcommand{\II}[1]{\int_{-1}^1#1\,dx}
\begin{aligned}
f(x)=\sum_{n=0}^\infty a_n\varphi_n(x)=\sum_{n=0}^\infty b_n\varphi_n(x)
\end{aligned}
$$

then

$$
\begin{aligned}
g(x)&=\sum_{n=0}^\infty(a_n-b_n)\varphi_n(x)=0\\
\br{g(x)}{g(x)}&=\sum_{n=0}^\infty(a_n-b_n)^2=0
\end{aligned}
$$

so $a_n=b_n$, and the expansion is unique.

-----

### 5.1.2

If 

$$
\begin{aligned}
f(x)=\sum_{i=1}^Nc_i\varphi_i(x)=\sum_{i=1}^Nc'_i\varphi_i(x)
\end{aligned}
$$

so 

$$
\begin{aligned}
\sum_{i=1}^N(c_i-c'_i)\varphi_i(x)
\end{aligned}
$$

By definition of linear independence, the linear combination of a linear independent set equals zero only if all the coefficient is zero. The set of $\varphi_i$ is linear independent, so $c_i-c'_i$ must be zero, which means $c_i=c'_i$, the components are unique.

-----

### 5.1.3

The mean square error $M$ is

$$
\begin{aligned}
M&=\int_0^1(f(x)-\sum_jc_jx^j)^2dx\\
=&\int_0^1\left[f(x)^2+(\sum_jc_jx^j)(\sum_jc_jx^j)-2f(x)(\sum_jc_jx^j) \right]dx
\end{aligned}
$$

When $M$ is minimized, $\pdv{M}{c_i}=0$ for every $i$, so

$$
\begin{aligned}
\pdv{M}{c_i}=\int_0^1\left[2x^i(\sum_jc_jx^j)-2f(x)x^i \right]dx=0
\end{aligned}
$$

so

$$
\begin{aligned}
\sum_j\int_0^1x^{i+j}dx\cdot c_j=\int_0^1x^if(x)dx
\end{aligned}
$$

Let $\int_0^1x^{i+j}dx=A_{ij}$, $\int_0^1x^if(x)dx=b_i$, then the equation becomes

$$
\begin{aligned}
\sum_jA_{ij}c_j=b_i
\end{aligned}
$$

or $\M{A}\V{c}=\V{b}$ in matrix form.

-----

### 5.1.4

Let $F(x)=\varphi_i(x)$, then

$$
\begin{aligned}
a_j=\delta_{ij}=\int_a^b\varphi_i(x)\varphi_{j}(x)w(x)dx
\end{aligned}
$$

so the basis are orthonormal. 

When the mean square error is minimized, 

$$
\begin{aligned}
\pdv{}{c_n}\left(\int_a^b[F(x)-\sum_{k=o}^mc_k\varphi_k(x)]^2w(x)dx \right)=0
\end{aligned}
$$

so

$$
\begin{aligned}
\int_a^b 2[F(x)-\sum_{k=o}^mc_k\varphi_k(x)](-\varphi_n(x))w(x)dx=0\\
-\int_a^bF(x)\varphi_n(x)w(x)dx+\sum_{k=0}^mc_k\delta_{kn}=0
\end{aligned}
$$

Note that the first term is $-a_n$, and the second term is $c_n$, so

$$
\begin{aligned}
c_n=a_n
\end{aligned}
$$

-----

### 5.1.5

(a)

$$
\begin{aligned}
&\int_{-\pi}^\pi\frac{\sin(2n+1)x}{2n+1}\frac{\sin(2m+1)x}{2m+1}dx\\
=&\int_{-\pi}^\pi\frac{\cos(2(n-m)x)-\cos(2(n+m+1)x)}{2(2n+1)(2m+1)}\\
=&\begin{cases}
0,\quad\quad\quad\;\;\textit{when $n\neq m$}\\
\frac{\pi}{(2n+1)^2},\quad\textit{when $n=m$}
\end{cases}
\end{aligned}
$$

so

$$
\begin{aligned}
\int_{-\pi}^\pi\left[f(x)\right]^2dx&=\int_{-\pi}^\pi\frac{4h^2}{\pi^2}(\sum_{n=0}^\infty\frac{\sin(2n+1)x}{2n+1})(\sum_{m=0}^\infty\frac{\sin(2m+1)x}{2m+1})dx\\
&=\frac{4h^2}{\pi^2}\sum_{n=0}^\infty\frac{\pi}{(2n+1)^2}=\frac{4h^2}{\pi}\sum_{n=0}^\infty\frac{1}{(2n+1)^2}
\end{aligned}
$$

(b)

$$
\begin{aligned}
\sum_{n=0}^\infty\frac{1}{(2n+1)^2}&=\frac{1}{1^2}+\frac{1}{3^2}+\frac{1}{5^2}+\frac{1}{7^2}+\cdots\\
&=(\frac{1}{1^2}+\frac{1}{2^2}+\frac{1}{3^2}+\frac{1}{4^2}+\frac{1}{5^2}+\frac{1}{6^2}+\frac{1}{7^2}+\cdots)-\frac{1}{2^2}(\frac{1}{1^2}+\frac{1}{2^2}+\frac{1}{3^2}+\cdots)\\
&=\frac{3}{4}\zeta(2)=\frac{\pi^2}{8}
\end{aligned}
$$

so

$$
\begin{aligned}
\frac{4h^2}{\pi}\sum_{n=0}^\infty\frac{1}{(2n+1)^2}=\frac{4h^2}{\pi}\frac{\pi^2}{8}=\frac{\pi}{2}h^2
\end{aligned}
$$


-----

### 5.1.6

$$
\begin{aligned}
\left[\int_a^bf(x)g(x)dx \right]^2+\frac{1}{2}\int_a^bdx\int_a^bdy\left[f(x)g(y)-f(y)g(x) \right]^2=\int_a^b\left[f(x) \right]^2dx\int_a^b\left[g(x) \right]^2dx
\end{aligned}
$$

and note that $\frac{1}{2}\int_a^bdx\int_a^bdy\left[f(x)g(y)-f(y)g(x) \right]^2\geq0$, so

$$
\begin{aligned}
\left[\int_a^bf(x)g(x)dx \right]^2\leq\int_a^b\left[f(x) \right]^2dx\int_a^b\left[g(x) \right]^2dx
\end{aligned}
$$

To prove the identity, note that

$$
\begin{aligned}
&\frac{1}{2}\int_a^bdx\int_a^bdy\left[f(x)g(y)-f(y)g(x) \right]^2\\
=&\frac{1}{2}\int_a^bdx\int_a^bdy\left[f(x)^2g(y)^2+f(y)^2g(x)^2-2f(x)g(x)f(y)g(y) \right]\\
=&\frac{1}{2}\int_a^bdx\left[f(x)^2\int_a^b[g(y)]^2dy+(\int_a^b[f(y)]^2dy)\;g(x)^2-2f(x)g(x)\int_a^bf(y)g(y)dy \right]\\
=&\frac{1}{2}\left[\int_a^b[f(x)]^2dx\int_a^b[g(y)]^2dy+\int_a^b[f(y)]^2dy\int_a^b[g(x)]^2dx-2\int_a^bf(x)g(x)dx\int_a^bf(y)g(y)dy \right]\\
=&\int_a^b[f(x)]^2dx\int_a^b[g(x)]^2dx-\left[\int_a^bf(x)g(x)dx\right]^2
\end{aligned}
$$

Rearranging the terms we get the identity.

-----

### 5.1.7

The basis are orthonormal, so $\langle a_i\varphi_i\vert a_j\varphi_j \rangle$ is zero when $i\neq j$ and is $\vert a_i\vert^2$ when $i=j$. Let $f=\sum_ka_k\varphi_k$, $k$ can be infinite, and let $\sum_na_n\varphi_n$ be an incomplete expansion of $f$, then 

$$
\begin{aligned}
I&=\left\langle f-\sum_na_n\varphi_n\Big|f-\sum_na_n\varphi_n \right\rangle\\
&=\langle f|f \rangle-\left\langle \sum_na_n\varphi_n\Big|f \right\rangle-\left\langle f\Big|\sum_na_n\varphi_n \right\rangle+\left\langle \sum_na_n\varphi_n\Big|\sum_na_n\varphi_n \right\rangle\\
&=\langle f|f \rangle-\left\langle \sum_na_n\varphi_n\Big|\sum_ka_k\varphi_k \right\rangle-\left\langle \sum_ka_k\varphi_k\Big|\sum_na_n\varphi_n \right\rangle+\left\langle \sum_na_n\varphi_n\Big|\sum_na_n\varphi_n \right\rangle\\
&=\langle f|f \rangle-\sum_n|a_n|^2-\sum_n|a_n|^2+\sum_n|a_n|^2\\
&=\langle f|f \rangle-\sum_n|a_n|^2\geq0
\end{aligned}
$$


so

$$
\begin{aligned}
\langle f|f \rangle\geq\sum_n|a_n|^2
\end{aligned}
$$

-----

### 5.1.8

By integrating by parts, we have

$$
\begin{aligned}
\int_0^1\sin\pi x\,dx&=\frac{\pi}{2}\\
\int_0^1x\sin\pi x\,dx&=\frac{1}{\pi}-\frac{1}{\pi}\int_0^1\cos\pi x\,dx=\frac{1}{\pi}\\
\int_0^1x^2\sin\pi x\,dx&=\frac{1}{\pi}-\frac{2}{\pi^2}\int_0^1\sin\pi x\,dx=\frac{1}{\pi}-\frac{4}{\pi^3}\\
\int_0^1x^3\sin\pi x\,dx&=\frac{1}{\pi}-\frac{6}{\pi^2}\int_0^1x\sin\pi x\,dx=\frac{1}{\pi}-\frac{6}{\pi^3}
\end{aligned}
$$

Let $\sin\pi x=\sum a_n\varphi_n$, then 

$$
\begin{aligned}
a_0&=\frac{\langle\varphi_0|\sin\pi x\rangle}{\langle\varphi_0|\varphi_0\langle}=\frac{I_0}{1}=\frac{2}{\pi}\\
a_1&=\frac{\langle\varphi_1|\sin\pi x\rangle}{\langle\varphi_1|\varphi_1\rangle}=\frac{2I_1-I_0}{\frac{1}{3}}=0\\
a_2&=\frac{\langle\varphi_2|\sin\pi x\rangle}{\langle\varphi_2|\varphi_2\rangle}=\frac{6I_2-6I_1+I_0}{\frac{1}{5}}=\frac{10}{\pi}-\frac{120}{\pi^3}\\
a_3&=\frac{\langle\varphi_3|\sin\pi x\rangle}{\langle\varphi_3|\varphi_3\rangle}=\frac{20I_3-30I_2+12I_1-I_0}{\frac{1}{7}}=0
\end{aligned}
$$

so

$$
\begin{aligned}
\sin\pi x=\frac{2}{\pi}\varphi_0+(\frac{10}{\pi}-\frac{120}{\pi^3})\varphi_2+\cdots
\end{aligned}
$$

-----

### 5.1.9

Integrating by parts for $n$ times, we have

$$
\begin{aligned}
\int_0^\infty x^ne^{-2x}dx=\frac{n!}{2^{n+1}}
\end{aligned}
$$

Let $e^{-x}=\sum a_nL_n(x)$, then

$$
\begin{aligned}
a_0&=\langle L_0|e^{-x}\rangle=\int_0^\infty e^{-2x}dx=\frac{1}{2}\\
a_1&=\langle L_1|e^{-x}\rangle=\int_0^\infty e^{-2x}dx-\int_0^\infty xe^{-2x}dx=\frac{1}{4}\\
a_2&=\langle L_2|e^{-x}\rangle=\int_0^\infty e^{-2x}dx-2\int_0^\infty xe^{-2x}dx+\frac{1}{2}\int_0^\infty x^2e^{-2x}dx=\frac{1}{8}\\
a_3&=\langle L_3|e^{-x}\rangle=\int_0^\infty e^{-2x}dx-3\int_0^\infty xe^{-2x}dx+\frac{3}{2}\int_0^\infty x^2e^{-2x}dx-\frac{1}{6}\int_0^\infty x^3e^{-2x}dx=\frac{1}{16}
\end{aligned}
$$

so

$$
\begin{aligned}
e^{-x}=\frac{1}{2}L_0+\frac{1}{4}L_1+\frac{1}{8}L_2+\frac{1}{16}L_3+\cdots
\end{aligned}
$$

-----

### 5.1.10

Expand $\varphi_n$ in the $\chi_n$ basis, we have

$$
\begin{aligned}
\varphi_n=\sum_m\chi_m\langle\chi_m|\varphi_n\rangle
\end{aligned}
$$

so

$$
\begin{aligned}
f=\sum_n\varphi_na_n=\sum_n\sum_m\chi_m\langle\chi_m|\varphi_n\rangle a_n
\end{aligned}
$$

-----

### 5.1.11

$$
\begin{aligned}
\sum_j|\VE_j\rangle\br{\VE_j}{\V{a}}=\sum_j\VE_j(\VE_j\cdot\V{a})=\V{a}
\end{aligned}
$$

-----

### 5.1.12

$$
\begin{aligned}
\br{\V{a}}{\V{a}}=a_1^2-2a_1a_2+ka_2^2=(a_1-a_2)^2+(k-1)a_2^2>0\quad\textit{(when $\V{a}\neq0$)}
\end{aligned}
$$

so $k-1>0$, $k>1$.

$$
\begin{aligned}
\br{\V{a}}{\V{b}}^*&=a_1b_1-a_1b_2-a_2b_1+ka_2b_2=b_1a_1-b_1a_2-b_2a_1+kb_2a_2=\br{\V{b}}{\V{a}}\\
\br{\V{a}}{\V{b}+\V{b'}}&=a_1(b_1+b'_1)-a_1(b_2+b'_2)-a_2(b_1+b'_1)+ka_2(b_2+b'_2)\\
\br{\V{a}}{\V{b}+\V{b'}}&=a_1(b_1+b'_1)-a_1(b_2+b'_2)-a_2(b_1+b'_1)+ka_2(b_2+b'_2)\\
&=(a_1b_1-a_1b_2-a_2b_1+ka_2b_2)+(a_1b'_1-a_1b'_2-a_2b'_1+ka_2b'_2)=\br{\V{a}}{\V{b}}+\br{\V{a}}{\V{b'}}\\
\br{\V{a}}{x\V{b}}&=a_1xb_1-a_1xb_2-a_2xb_1+ka_2xb_2=x(a_1b_1-a_1b_2-a_2b_1+ka_2b_2)=x\br{\V{a}}{\V{b}}
\end{aligned}
$$

so the condition for the scalar product to be valid is $k>1$.

## 5.2 Gram-Schmidt Orthogonalization

### 5.2.1

$$
\begin{aligned}
P_0^*(x)&=1\\
\psi_1(x)&=x-1\frac{\br{1}{x}}{\br{1}{1}}=x-\frac{\int_0^1xdx}{\int_0^1dx}=x-\frac{1}{2}\\
P_1^*(x)&=\frac{\psi_1(x)}{\psi_1(1)}=2x-1\\
\psi_2(x)&=x^2-1\frac{\br{1}{x^2}}{\br{1}{1}}-(2x-1)\frac{\br{2x-1}{x^2}}{\br{2x-1}{2x-1}}=x^2-\frac{\int_0^1x^2dx}{\int_0^1dx}-(2x-1)\frac{\int_0^1(2x^3-x^2)dx}{\int_0^1(2x-1)^2dx}=x^2-x+\frac{1}{6}\\
P_2^*(x)&=\frac{\psi_2(x)}{\psi_2(1)}=6x^2-6x+1\\
\psi_3(x)&=x^3-1\frac{\br{1}{x^3}}{\br{1}{1}}-(2x-1)\frac{\br{2x-1}{x^3}}{\br{2x-1}{2x-1}}-(6x^2-6x+1)\frac{\br{6x^2-6x+1}{x^3}}{\br{6x^2-6x+1}{6x^2-6x+1}}=x^3-\frac{3}{2}x^2+\frac{3}{5}x-\frac{1}{20}\\
P_3^*(x)&=\frac{\psi_3(x)}{\psi_3(1)}=20x^3-30x^2+12x-1
\end{aligned}
$$

-----

### 5.2.2

$$
\begin{aligned}
\varphi_0&=1\\
L_0&=\frac{\varphi_0}{{\br{\varphi_0}{\varphi_0}}^{1/2}}=\frac{1}{(\int_0^\infty e^{-x}dx)^{1/2}}=\pm1\quad\textit{(choose $1$)}\\
\varphi_1&=x-1\int_0^\infty1 xe^{-x}dx=x-1\\
L_1&=\frac{\varphi_1}{{\br{\varphi_1}{\varphi_1}}^{1/2}}=\frac{x-1}{(\int_0^\infty(x-1)^2e^{-x}dx)^{1/2}}=\pm(x-1)\quad\textit{(choose $-x+1$)}\\
\varphi_2&=x^2-1\int_0^\infty1x^2e^{-x}dx-(1-x)\int_0^\infty(1-x)x^2e^{-x}dx=x^2-4x+2\\
L_2&=\frac{\varphi_2}{{\br{\varphi_2}{\varphi_2}}^{1/2}}=\frac{x^2-4x+2}{(\int_0^\infty (x^2-4x+2)^2e^{-x}dx)^{1/2}}=\pm\frac{x^2-4x+2}{2}\quad\textit{(choose $\frac{x^2-4x+2}{2}$)}
\end{aligned}
$$

(The choice of sign in the normalization is arbitrary and is so chosen to match the answer given in the text.)

-----

### 5.2.3

$$
\begin{aligned}
\psi_0(x)&=1\\
\varphi_0(x)&=\frac{\psi_0}{\br{\psi_0}{\psi_0}^{1/2}}=\frac{1}{(\int_0^\infty xe^{-x}dx)^{1/2}}=1\\
\psi_1(x)&=x-1\int_0^\infty1x\cdot xe^{-x}dx=x-2\\
\varphi_1(x)&=\frac{\psi_1}{\br{\psi_1}{\psi_1}^{1/2}}=\frac{x-2}{(\int_0^\infty(x^2-4x+4)xe^{-x}dx)^{1/2}}=\frac{x-2}{\sqrt{2}}\\
\psi_2(x)&=x^2-1\int_0^\infty1x^2\cdot xe^{-x}dx-\frac{x-1}{\sqrt{2}}\int_0^\infty\frac{x-2}{\sqrt{2}}x^2\cdot xe^{-x}dx=x^2-6x+6\\
\varphi_2(x)&=\frac{\psi_2}{\br{\psi_2}{\psi_2}^{1/2}}=\frac{x^2-6x+6}{(\int_0^\infty(x^4-12x^3+48x^2-72x+36)xe^{-x}dx)^{1/2}}=\frac{x^2-6x+6}{2\sqrt{3}}
\end{aligned}
$$

(using the formula $\int_0^\infty x^ne^{-x}dx=n!$ can facilate the calculation.)

-----

### 5.2.4

To calculate the scalar product, we need the Gaussian integral $\int_{-\infty}^\infty x^ne^{-x^2}dx$. When $n$ is odd, $\int_{-\infty}^\infty x^ne^{-x^2}dx=0$ because $x^ne^{-x^2}$ is odd function. When $n$ is even, from Example 1.10.7 we have $\int_{-\infty}^\infty e^{-x^2}dx=\sqrt{\pi}$, and by substitution we have

$$
\begin{aligned}
\int_{-\infty}^\infty e^{-ax^2}dx=\frac{\sqrt{\pi}}{\sqrt{a}}
\end{aligned}
$$

differentiate both sides regarding $a$, 

$$
\begin{aligned}
\frac{d}{da}\int_{-\infty}^\infty e^{-ax^2}dx=\int_{-\infty}^\infty (-x^2)e^{-ax^2}dx=-\frac{1}{2}\frac{\sqrt{\pi}}{a^{-\frac{3}{2}}}
\end{aligned}
$$

so

$$
\begin{aligned}
\int_{-\infty}^\infty x^2e^{-ax^2}dx=\frac{\sqrt{\pi}}{2a^{-\frac{3}{2}}}
\end{aligned}
$$

differentiate again,

$$
\begin{aligned}
\frac{d}{da}\int_{-\infty}^\infty x^2e^{-ax^2}dx=\int_{-\infty}^\infty (-x^4)e^{-ax^2}dx=-\frac{3}{4}\frac{\pi}{a^{-\frac{5}{2}}}
\end{aligned}
$$

so

$$
\begin{aligned}
\int_{-\infty}^\infty x^4e^{-ax^2}dx=\frac{3\sqrt{\pi}}{4a^{-\frac{3}{2}}}
\end{aligned}
$$

Let $\varphi_n$ be the non-scaled function, and $H_n=a_n\varphi_n$, so $\br{H_n}{H_n}=\int_{-\infty}^\infty a_n^2\varphi_n^2e^{-x^2}dx=2^nn!\sqrt{\pi}$. Then

$$
\begin{aligned}
\varphi_0&=1\\
\br{H_0}{H_0}&=\int_{-\infty}^\infty a_0^21^2e^{-x^2}dx=a_0^2\sqrt{\pi}=\sqrt{\pi}
\end{aligned}
$$

so $a_0=1$, and $H_0=1$.

$$
\begin{aligned}
\varphi_1&=x-1\frac{\int_{-\infty}^\infty1\cdot xe^{-x^2}dx}{\int_{-\infty}^\infty1\cdot1e^{-x^2}dx}=x\\
\br{H_1}{H_1}&=\int_{-\infty}^\infty a_1^2x^2e^{-x^2}dx=a_1^2\frac{\sqrt{\pi}}{2}=2\sqrt{\pi}
\end{aligned}
$$

so $a_1=2$, and $H_1=2x$.

$$
\begin{aligned}
\varphi_2&=x^2-1\frac{\int_{-\infty}^\infty1\cdot x^2e^{-x^2}dx}{\int_{-\infty}^\infty1\cdot1e^{-x^2}dx}-2x\frac{\int_{-\infty}^\infty2x\cdot x^2e^{-x^2}dx}{\int_{-\infty}^\infty2x\cdot2xe^{-x^2}dx}=x^2-\frac{1}{2}\\
\br{H_2}{H_2}&=\int_{-\infty}^\infty a_2^2(x^2-\frac{1}{2})^2e^{-x^2}dx=a_2^2\frac{\sqrt{\pi}}{2}=8\sqrt{\pi}
\end{aligned}
$$

so $a_2=4$, and $H_2=4x^2-2$.

-----

### 5.2.5

$$
\begin{aligned}
\int_{-1}^1\frac{x^{2n}}{\sqrt{1-x^2}}dx=
\begin{cases}
\pi,\quad &n=0\\
\pi\frac{(2n-1)!!}{(2n)!!},\quad &n=1,2,3\cdots
\end{cases}
\end{aligned}
$$

from Exercise 13.3.2, and $\int_{-1}^1\frac{x^{2n+1}}{\sqrt{1-x^2}}dx=0$ because $\frac{x^{2n+1}}{\sqrt{1-x^2}}$ is an odd function.

Let $\varphi_n$ be the non-scaled function, and
$T_n=a_n\varphi_n$, so $\br{T_n}{T_n}=\int_{-1}^1a_n^2\varphi_n^2\frac{1}{\sqrt{1-x^2}}dx$. Then

$$
\begin{aligned}
\varphi_0&=1\\
\br{T_0}{T_0}&=\int_{-1}^1a_0^2\frac{1}{\sqrt{1-x^2}}dx=a_0^2\pi=\pi
\end{aligned}
$$

so $a_0=1$, and $T_0=1$.

$$
\begin{aligned}
\varphi_1&=x-1\frac{\int_{-1}^11\cdot x\frac{1}{\sqrt{1-x^2}}dx}{\int_{-1}^11\cdot1\frac{1}{\sqrt{1-x^2}}dx}=x\\
\br{T_1}{T_1}&=\int_{-1}^1a_1^2x^2\frac{1}{\sqrt{1-x^2}}dx=a_1^2\frac{\pi}{2}=\frac{\pi}{2}
\end{aligned}
$$

so $a_1=1$, and $T_1=x$.

$$
\begin{aligned}
\varphi_2&=x^2-1\frac{\int_{-1}^11\cdot x^2\frac{1}{\sqrt{1-x^2}}dx}{\int_{-1}^11\cdot1\frac{1}{\sqrt{1-x^2}}dx}-x\frac{\int_{-1}^1x\cdot x^2\frac{1}{\sqrt{1-x^2}}dx}{\int_{-1}^1x\cdot x\frac{1}{\sqrt{1-x^2}}dx}=x^2-\frac{1}{2}\\
\br{T_2}{T_2}&=\int_{-1}^1a_2^2(x^2-\frac{1}{2})^2\frac{1}{\sqrt{1-x^2}}dx=a_2^2\frac{\pi}{8}=\frac{\pi}{2}
\end{aligned}
$$

so $a_2=2$, and $T_2=2x^2-1$.

$$
\begin{aligned}
\varphi_3&=x^3-1\frac{\int_{-1}^11\cdot x^3\frac{1}{\sqrt{1-x^2}}dx}{\int_{-1}^11\cdot1\frac{1}{\sqrt{1-x^2}}dx}-x\frac{\int_{-1}^1x\cdot x^3\frac{1}{\sqrt{1-x^2}}dx}{\int_{-1}^1x\cdot x\frac{1}{\sqrt{1-x^2}}dx}-(2x^2-1)\frac{\int_{-1}^1(2x^2-1)x^3\frac{1}{\sqrt{1-x^2}}dx}{\int_{-1}^1(2x^2-1)^2\frac{1}{\sqrt{1-x^2}}dx}=x^3-\frac{3}{4}x\\
\br{T_3}{T_3}&=\int_{-1}^1a_3^2(x^3-\frac{3}{4}x)^2\frac{1}{\sqrt{1-x^2}}dx=a_3^2\frac{\pi}{32}=\frac{\pi}{2}
\end{aligned}
$$

so $a_3=4$, and $T_3=4x^3-3x$.

-----

### 5.2.6

Note that 

$$
\begin{aligned}
\int_{-1}^1x^{2n+1}\sqrt{1-x^2}dx=0
\end{aligned}
$$

because $x^{2n+1}\sqrt{1-x^2}$ is an odd function.

Let $\varphi_n$ be the non-scaled function, and $U_n=a_n\varphi_n$, so $\br{U_n}{U_n}=\int_{-1}^1a_n^2\varphi_n^2\sqrt{1-x^2}dx$. Then

$$
\begin{aligned}
\varphi_0&=1\\
\br{U_0}{U_0}&=\int_{-1}^1a_0^2\sqrt{1-x^2}dx=a_0^2\frac{\pi}{2}=\frac{\pi}{2}
\end{aligned}
$$

so $a_0=1$, and $U_0=1$.

$$
\begin{aligned}
\varphi_1&=x-1\frac{\int_{-1}^11\cdot x\sqrt{1-x^2}dx}{\int_{-1}^11\cdot1\sqrt{1-x^2}dx}=x\\
\br{U_1}{U_1}&=\int_{-1}^1a_1^2x^2\sqrt{1-x^2}dx=a_1^2\frac{\pi}{8}=\frac{\pi}{2}
\end{aligned}
$$

so $a_1=2$, and $U_1=2x$.

$$
\begin{aligned}
\varphi_2&=x^2-1\frac{\int_{-1}^11\cdot x^2\sqrt{1-x^2}dx}{\int_{-1}^11\cdot1\sqrt{1-x^2}dx}-2x\frac{\int_{-1}^12x\cdot x^2\sqrt{1-x^2}dx}{\int_{-1}^12x\cdot 2x\sqrt{1-x^2}dx}=x^2-\frac{1}{4}\\
\br{U_2}{U_2}&=\int_{-1}^1a_2^2(x^2-\frac{1}{4})^2\sqrt{1-x^2}dx=a_2^2\frac{\pi}{32}=\frac{\pi}{2}
\end{aligned}
$$

so $a_2=4$, and $U_2=4x^2-1$.

-----

### 5.2.7

$$
\begin{aligned}
\psi_0&=1\\
\varphi_0&=1\\
\psi_1&=x-1\frac{\int_0^\infty1\cdot xe^{-x^2}dx}{\int_0^\infty1\cdot1e^{-x^2}dx}=x-\frac{1}{\sqrt{\pi}}\\
\varphi_1&=x-\frac{1}{\sqrt{\pi}}
\end{aligned}
$$

-----

### 5.2.8

$$
\begin{aligned}
\V{a_1'}&=\begin{pmatrix}1\\1\\1\end{pmatrix}\\
\V{a_1}&=\frac{\V{a_1'}}{(\V{a_1'}\cdot\V{a_1'})^{1/2}}=\frac{1}{\sqrt{3}}\begin{pmatrix}1\\1\\1\end{pmatrix}\\
\V{a_2'}&=\V{c_2}-\V{a_1}(\V{a_1}\cdot\V{c_2})=\frac{1}{3}\begin{pmatrix}-1\\-1\\2\end{pmatrix}\\
\V{a_2}&=\frac{\V{a_2'}}{(\V{a_2'}\cdot\V{a_2'})^{1/2}}=\frac{1}{\sqrt{6}}\begin{pmatrix}-1\\-1\\2\end{pmatrix}\\
\V{a_3'}&=\V{c_3}-\V{a_1}(\V{a_1}\cdot\V{c_3})-\V{a_2}(\V{a_2}\cdot\V{c_3})=\frac{1}{2}\begin{pmatrix}1\\-1\\0\end{pmatrix}\\
\V{a_3}&=\frac{\V{a_3'}}{(\V{a_3'}\cdot\V{a_3'})^{1/2}}=\frac{1}{\sqrt{2}}\begin{pmatrix}1\\-1\\0\end{pmatrix}
\end{aligned}
$$

## 5.3 Operators

-----

### 5.3.1

$$
\begin{aligned}
\br{f}{Ag}=\br{A^{\dagger}f}{g}=\br{g}{A^\dagger f}^*=\br{(A^\dagger)^\dagger g}{f}^*=\br{f}{(A^\dagger)^\dagger g}
\end{aligned}
$$

so 

$$
\begin{aligned}
\br{f}{(A-(A^\dagger)^\dagger)g}=0
\end{aligned}
$$

for any $f$ and $g$. If $A-(A^\dagger)^\dagger\neq0$, which means there are some $g$ such that $(A-(A^\dagger)^\dagger) g=\varphi\neq0$, then let $f=\varphi$, and $\br{f}{(A-(A^\dagger)^\dagger)g}=\br{\varphi}{\varphi}>0$, contradict. So $A-(A^\dagger)^\dagger$ must be zero, which means 

$$
\begin{aligned}
(A^\dagger)^\dagger=A
\end{aligned}
$$

-----

### 5.3.2

$$
\begin{aligned}
\br{f}{UVg}=\br{U^\dagger f}{Vg}=\br{V^\dagger U^\dagger f}{g}
\end{aligned}
$$

also

$$
\begin{aligned}
\br{f}{UVg}=\br{(UV)^\dagger f}{g}
\end{aligned}
$$

so 

$$
\begin{aligned}
\br{((UV)^\dagger-V^\dagger U^\dagger)f}{g}=0
\end{aligned}
$$

for any $f$ and $g$, so $(UV)^\dagger-V^\dagger U^\dagger$ must be zero, which means

$$
\begin{aligned}
(UV)^\dagger=V^\dagger U^\dagger
\end{aligned}
$$

-----

### 5.3.3

(a) 

$$
\begin{aligned}
(A_1)_{ij}&=\br{\varphi_i|A_1}{\varphi_j}=\br{x_i|\sum_{k=1}^3x_k(\pdv{}{x_k})}{x_j}=\br{x_i}{x_j}=\delta_{ij}\\
(A_2)_{ij}&=\br{\varphi_i|A_2}{\varphi_j}=\br{x_i|x_1(\pdv{}{x_2})-x_2(\pdv{}{x_1})}{x_j}=\br{x_i}{x_1\delta_{2j}-x_2\delta_{1j}}=\delta_{i1}\delta_{2j}-\delta_{i2}\delta_{1j}
\end{aligned}
$$

In matrix forms,

$$
\begin{aligned}
\M{A_1}=
\begin{pmatrix}
1&0&0\\
0&1&0\\
0&0&1
\end{pmatrix}
\quad\quad \M{A_2}
\begin{pmatrix}
0&1&0\\
-1&0&0\\
0&0&0
\end{pmatrix}
\end{aligned}
$$

(b) 

$$
\begin{aligned}
\psi_i=\br{\varphi_i}{\psi}=\br{x_i}{x_1-2x_2+3x_3}=\delta_{i1}-2\delta_{i2}+3\delta_{i3}
\end{aligned}
$$

In matrix form, 

$$
\begin{aligned}
\boldsymbol{\psi}=
\begin{pmatrix}
1\\-2\\3
\end{pmatrix}
\end{aligned}
$$

(c) From matrix equation, 

$$
\begin{aligned}
\boldsymbol{\chi}=\left[
\begin{pmatrix}
1&0&0\\
0&1&0\\
0&0&1
\end{pmatrix}
-
\begin{pmatrix}
0&1&0\\
-1&0&0\\
0&0&0
\end{pmatrix}
\right]
\begin{pmatrix}
1\\-2\\3
\end{pmatrix}=
\begin{pmatrix}
3\\-1\\3
\end{pmatrix}
\end{aligned}
$$

which is $3x_1-x_2+3x_3$.

By direct application,

$$
\begin{aligned}
\chi&=(A_1-A_2)\psi=\sum_{i=1}^3x_i(\pdv{}{x_i})(x_1-2x_2+3x_3)-\left[x_1(\pdv{}{x_2})-x_2(\pdv{}{x_1}) \right](x_1-2x_2+3x_3)\\
&=x_1-2x_2+3x_3-(-2x_1-x_2)=3x_1-x_2+3x_3
\end{aligned}
$$

which is the same with the results from matrix multiplication.

-----

### 5.3.4

(a)

$$
\begin{aligned}
AP_0&=x\frac{d}{dx}(\frac{1}{\sqrt{2}})=0\\
AP_1&=x\frac{d}{dx}(\sqrt{\frac{3}{2}}x)=\sqrt{\frac{3}{2}}x=P_1\\
AP_2&=x\frac{d}{dx}\left(\sqrt{\frac{5}{2}}(\frac{3}{2}x^2-\frac{1}{2})\right)=\sqrt{\frac{5}{2}}\,3x^2=2P_2+\sqrt{5}P_0\\
AP_3&=x\frac{d}{dx}\left(\sqrt{\frac{7}{2}}(\frac{5}{2}x^3-\frac{3}{2}x)\right)=\sqrt{\frac{7}{2}}\frac{15}{2}x^3-\sqrt{\frac{7}{2}}\frac{3}{2}x=3P_3+\sqrt{21}P_1
\end{aligned}
$$

We can evaluate $A_{ij}$ by $A_{ij}=\br{P_i}{AP_j}$, and $\br{P_i}{P_j}=\delta_{ij}$. In matrix form,

$$
\begin{aligned}
\M{A}=
\begin{pmatrix}
0&0&\sqrt{5}&0\\
0&1&0&\sqrt{21}\\
0&0&2&0\\
0&0&0&3
\end{pmatrix}
\end{aligned}
$$

(b)

$$
\begin{aligned}
x^3&=P_0\int_{-1}^1\frac{1}{\sqrt{2}}\,x^3dx+P_1\int_{-1}^1\sqrt{\frac{3}{2}}x\cdot x^3dx+P_2\int_{-1}^1\sqrt{\frac{5}{2}}(\frac{3}{2}x^2-\frac{1}{2})\cdot x^3dx+P_3\int_{-1}^1\sqrt{\frac{7}{2}}(\frac{5}{2}x^3-\frac{3}{2}x)x^3dx\\
&=\frac{\sqrt{6}}{5}P_1+\frac{2\sqrt{14}}{35}P_3
\end{aligned}
$$

(c)

$$
\begin{aligned}
\renewcommand{\arraystretch}{1.5}
\begin{pmatrix}
0&0&\sqrt{5}&0\\
0&1&0&\sqrt{21}\\
0&0&2&0\\
0&0&0&3
\end{pmatrix}
\begin{pmatrix}
0\\\frac{\sqrt{6}}{5}\\0\\\frac{2 \sqrt{14}}{35}
\end{pmatrix}=
\begin{pmatrix}
0\\\frac{3\sqrt{6}}{5}\\0\\\frac{6\sqrt{14}}{35}
\end{pmatrix}
\end{aligned}
$$

which is 

$$
\begin{aligned}
\frac{3\sqrt{6}}{5}(\sqrt{\frac{3}{2}}x)+\frac{6\sqrt{14}}{35}\sqrt{\frac{7}{2}}(\frac{5}{2}x^3-\frac{3}{2}x)=3x^3
\end{aligned}
$$

which is the same as $Ax^3=x\frac{d}{dx}(x^3)=3x^3$.

## 5.4 Self-Adjoint Operators

### 5.4.1

(a)

$$
\begin{aligned}
\br{f}{(A+A^\dagger)g}&=\br{(A+A^\dagger)^\dagger f}{g}=\br{(A^\dagger+A)f}{g}=\br{(A+A^\dagger)f}{g}\\
\br{f}{i(A-A^\dagger)g}&=\br{-i(A-A^\dagger)^\dagger f}{g}=\br{-i(A^\dagger-A)f}{g}=\br{i(A-A^\dagger)f}{g}
\end{aligned}
$$

(b)
For every operator $A$,

$$
\begin{aligned}
A=\frac{1}{2}(A+A^\dagger)-\frac{i}{2}i(A-A^\dagger)
\end{aligned}
$$

where both $A+A^\dagger$ and $i(A-A^\dagger)$ are Hermitian.

-----

### 5.4.2

Let $A,B$ be Hermitian. 

If $AB$ is Hermitian, then $\br{f}{ABg}=\br{ABf}{g}$, but also

$$
\begin{aligned}
\br{f}{ABg}=\br{Af}{Bg}=\br{BAf}{g}
\end{aligned}
$$

so $\br{(AB-BA)f}{g}=0$ for any $f,g$, which means $(AB-BA)$ must be zero, and therefore $AB=BA$, 

If $AB=BA$, then 

$$
\begin{aligned}
\br{f}{ABg}=\br{Af}{Bg}=\br{BAf}{g}=\br{ABf}{g}
\end{aligned}
$$

so $AB$ is Hermitian.

-----

### 5.4.3

$A,B$ are Hermitian because they are quantum mechanical operators. $C=-i(AB-BA)$, so

$$
\begin{aligned}
\br{f}{Cg}=\br{C^\dagger d}{g}=\br{i(B^\dagger A^\dagger-A^\dagger B^\dagger)f}{g}=\br{i(BA-AB)f}{g}=\br{-i(AB-BA)f}{g}=\br{Cf}{g}
\end{aligned}
$$

so $C$ is Hermitian.

-----

### 5.4.4

$\mathcal{L}$ is Hermitian, so

$$
\begin{aligned}
\br{\psi|\mathcal{L}^2}{\psi}=\br{\psi|\mathcal{L}\mathcal{L}}{\psi}=\br{\mathcal{L}\psi}{\mathcal{L}\psi}\geq0
\end{aligned}
$$

by the definition of scalar product.

-----

### 5.4.5

(a) In spherical polar coordinate, $\varphi_1=C\sin\theta\cos\varphi$, $\varphi_2=C\sin\theta\sin\varphi$, $\varphi_3=C\cos\theta$. So

$$
\begin{aligned}
\br{\varphi_1}{\varphi_1}&=\int_0^\pi\int_0^{2\pi}(|C|^2\sin^2\theta\cos^2\varphi)\sin\theta\, d\theta\,d\varphi\\
&=|C|^2\int_0^\pi\sin^3\theta\,d\theta\int_0^{2\pi}\cos^2\varphi\,d\varphi=|C|^2\frac{4\pi}{3}=1
\end{aligned}
$$

so

$$
\begin{aligned}
C=\sqrt{\frac{3}{4\pi}}e^{i\theta}
\end{aligned}
$$

By symmetry this $C$ also made $\varphi_2$ and $\varphi_3$ normalized.

$$
\begin{aligned}
\br{\varphi_1}{\varphi_2}&=\int_0^\pi\int_0^{2\pi}|C|^2\sin^2\theta\cos^2\varphi\sin\theta\,d\theta\,d\varphi\\
&=|C|^2\int_0^\pi\sin^3\theta\,d\theta\int_0^{2\pi}\sin\varphi\cos\varphi\,d\varphi=0
\end{aligned}
$$

By symmetry $\br{\varphi_2}{\varphi_3}$ and $\br{\varphi_3}{\varphi_1}$ are also zero.

(b) Let $i,j,k$ be a cyclic permutation of $x,y,z$, then all the three operators have the form

$$
\begin{aligned}
L_i=-i(x_j\pdv{}{x_k}-x_k\pdv{}{x_j})
\end{aligned}
$$

Note that $\pdv{}{x_k}(\frac{1}{r})=-\frac{x_k}{r^3}$, so

$$
\begin{aligned}
L_i\varphi_b&=-i\left[x_j\pdv{}{x_k}(\frac{Cx_b}{r})-x_k\pdv{}{x_j}(\frac{Cx_b}{r}) \right]\\
&=-iC\left[x_j\pdv{x_b}{x_k}\frac{1}{r}-x_jx_b\frac{x_k}{r^3}-x_k\pdv{x_b}{x_j}\frac{1}{r}+x_kx_b\frac{x_j}{r^3} \right]\\
&=-i\frac{C}{r}\left[x_j\delta_{kb}-x_k\delta_{jb} \right]=-i\left[\varphi_j\delta_{kb}-\varphi_k\delta_{jb} \right]
\end{aligned}
$$

so

$$
\begin{aligned}
\br{\varphi_a|L_i}{\varphi_b}&=-i\left[\br{\varphi_a}{\varphi_j}\delta_{kb}-\br{\varphi_a}{\varphi_k}\delta_{jb} \right]=-i\left(\delta_{aj}\delta_{kb}-\delta_{ak}\delta_{jb} \right)\\
&=\begin{cases}
-i & \textit{when $a=j,\;b=k$}\\
i & \textit{when $a=k,\;b=j$}
\end{cases}
\end{aligned}
$$

The components of $L_i$ are $(L_i)\_{ab}=\br{\varphi_a\vert L_i}{\varphi_b}$, so in matrix form,

$$
\begin{aligned}
L_x=
\begin{pmatrix}
0&0&0\\
0&0&-i\\
0&i&0
\end{pmatrix}\quad
L_y=
\begin{pmatrix}
0&0&i\\
0&0&0\\
-i&0&0
\end{pmatrix}\quad
L_z=
\begin{pmatrix}
0&-i&0\\
i&0&0\\
0&0&0
\end{pmatrix}\quad
\end{aligned}
$$

(c)

$$
\begin{aligned}
L_xL_y-L_yL_x=
\begin{pmatrix}
0&0&0\\
0&0&-i\\
0&i&0
\end{pmatrix}
\begin{pmatrix}
0&0&i\\
0&0&0\\
-i&0&0
\end{pmatrix}-
\begin{pmatrix}
0&0&i\\
0&0&0\\
-i&0&0
\end{pmatrix}
\begin{pmatrix}
0&0&0\\
0&0&-i\\
0&i&0
\end{pmatrix}=
\begin{pmatrix}
0&1&0\\
-1&0&0\\
0&0&0
\end{pmatrix}=iL_z
\end{aligned}
$$

(we can prove $[L_x,L_y]=iL_z$, $[L_y,L_z]=iL_x$, $[L_z,L_x]=iL_y$ together:
Note that 

$$
\begin{aligned}
\br{\varphi_a|L_i}{\varphi_b}=\begin{cases}
-i & \textit{when $a=j,\;b=k$}\\
i & \textit{when $a=k,\;b=j$}
\end{cases}
\end{aligned}
$$

is equivalent with $(L_i)\_{ab}=-i\varepsilon_{iab}$.
Let $i,j,k$ be a cyclic permutation of $x,y,z$, then

$$
\begin{aligned}
(L_iL_j)_{ab}=\sum_c(L_i)_{ac}(L_j)_{cb}=\sum_c-\varepsilon_{iac}\varepsilon_{jcb}=-\varepsilon_{iak}\varepsilon_{jkb}=\varepsilon_{iak}\varepsilon_{jbk}=\delta_{ij}\delta_{ab}-\delta_{ib}\delta_{aj}=-\delta_{ib}\delta_{aj}
\end{aligned}
$$

by Exercise 2.1.9. So

$$
\begin{aligned}
(L_iL_j-L_jL_i)_{ab}=-\delta_{ib}\delta_{aj}+\delta_{jb}\delta_{ai}=\sum_l\varepsilon_{ijl}\varepsilon_{abl}=\varepsilon_{ijk}\varphi_{abk}=\varepsilon_{abk}=i(-i\varepsilon_{kab})=i(L_k)_{ab}
\end{aligned}
$$

which means $[L_i,L_j]=iL_k$ )

## 5.5 Unitary Operators

### 5.5.1

(There are mistakes in the matrix $\M{U}$ given in the text: $\M{U}\_{33}$ should be $\frac{-i}{\sqrt{2}}$ and $\M{U}\_{43}$ should be $\frac{i}{\sqrt{2}}$. It can be verified by checking $\chi_3=U_{33}\chi_3'+U_{43}\chi_4'$. The author probably forget to take the complex conjugate of $\chi_3'$ when calculating $\br{\chi_3'}{\chi_3}=\int_0^\pi\int_0^{2\pi}\sin\theta\,d\theta d\varphi(\chi_3')^\star\chi_3$, as well as $\br{\chi_4'}{\chi_3}$. )

(a) 

$$
\begin{aligned}
f(\theta,\varphi)&=\V{c}=
\begin{pmatrix}
3\\2i\\-1\\0\\1
\end{pmatrix}\\
\V{c'}&=\M{U}\V{c}=
\begin{pmatrix}
\frac{-1}{\sqrt{2}}&\frac{-i}{\sqrt{2}}&0&0&0\\
\frac{1}{\sqrt{2}}&\frac{-i}{\sqrt{2}}&0&0&0\\
0&0&\frac{-i}{\sqrt{2}}&\frac{1}{\sqrt{2}}&0\\
0&0&\frac{i}{\sqrt{2}}&\frac{1}{\sqrt{2}}&0\\
0&0&0&0&1
\end{pmatrix}
\begin{pmatrix}
3\\2i\\-1\\0\\1
\end{pmatrix}=
\begin{pmatrix}
\frac{-1}{\sqrt{2}}\\\frac{5}{\sqrt{2}}\\\frac{i}{\sqrt{2}}\\\frac{-i}{\sqrt{2}}\\1
\end{pmatrix}\\
\sum_ic_i'\chi_i'&=\sqrt{\frac{15}{8\pi}}\sin\theta\cos\theta(\frac{1}{\sqrt{2}}e^{i\varphi}+\frac{5}{\sqrt{2}}e^{-i\varphi})+\sqrt{\frac{15}{32\pi}}\sin^2\theta(\frac{i}{\sqrt{2}}e^{2i\varphi}-\frac{i}{\sqrt{2}}e^{-2i\varphi})+\chi_5'\\
&=3\sqrt{\frac{15}{4\pi}}\sin\theta\cos\theta\cos\varphi-2i\sqrt{\frac{15}{4\pi}}\sin\theta\cos\theta\sin\varphi-\sqrt{\frac{15}{4\pi}}\sin^2\theta\sin\varphi\cos\varphi+\chi_5\\
&=3\chi_1-2i\chi_2-\chi_3+\chi_5=\sum_ic_i\chi_i=f(\theta,\varphi)
\end{aligned}
$$


(b)

$$
\begin{aligned}
\M{U}^{-1}\M{U}=
\begin{pmatrix}
\frac{-1}{\sqrt{2}}&\frac{1}{\sqrt{2}}&0&0&0\\
\frac{-i}{\sqrt{2}}&\frac{-i}{\sqrt{2}}&0&0&0\\
0&0&\frac{-i}{\sqrt{2}}&\frac{i}{\sqrt{2}}&0\\
0&0&\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}&0\\
0&0&0&0&1
\end{pmatrix}
\begin{pmatrix}
\frac{-1}{\sqrt{2}}&\frac{-i}{\sqrt{2}}&0&0&0\\
\frac{1}{\sqrt{2}}&\frac{-i}{\sqrt{2}}&0&0&0\\
0&0&\frac{-i}{\sqrt{2}}&\frac{1}{\sqrt{2}}&0\\
0&0&\frac{i}{\sqrt{2}}&\frac{1}{\sqrt{2}}&0\\
0&0&0&0&1
\end{pmatrix}=
\begin{pmatrix}
1&0&0&0&0\\
0&1&0&0&0\\
0&0&1&0&0\\
0&0&0&1 &0\\
0&0&0&0&1
\end{pmatrix}
\end{aligned}
$$

-----

### 5.5.2

(a) The transformation is $x=z'$, $y=y'$, $z=-x'$. The new basis is defined as $\varphi_1'=x'$, $\varphi_2'=y'$, $\varphi_3'=z'$, so $\varphi_1=\varphi_3'$, $\varphi_2=\varphi_2'$, $\varphi_3=-\varphi_1'$, which in matrix representation becomes

$$
\begin{aligned}
\renewcommand{\arraystretch}{1.0}
\begin{pmatrix}
0&0&-1\\
0&1&0\\
1&0&0\\
\end{pmatrix}
\end{aligned}
$$

(b) The transformation corresponds to rotating $\frac{\pi}{2}$ counterclockwise about $y$-axis, so the Euler angles are $\alpha=0$, $\beta=\frac{\pi}{2}$, $\gamma=0$. By Eq. 3.37, 

$$
\begin{aligned}
S(\alpha,\beta,\gamma)=
\begin{pmatrix}
0&0&-1\\
0&1&0\\
1&0&0\\
\end{pmatrix}
\end{aligned}
$$

which is the same as (a).

(c)

$$
\begin{aligned}
\begin{pmatrix}
0&0&-1\\
0&1&0\\
1&0&0\\
\end{pmatrix}
\begin{pmatrix}
2\\-3\\1
\end{pmatrix}=
\begin{pmatrix}
-1\\-3\\2
\end{pmatrix}
\end{aligned}
$$

so $f'=-x'-3y'+2z'=z-3y+2x=f$, consistent.

-----

### 5.5.3

$\varphi_1'=-\varphi_3$, $\varphi_2'=\varphi_2$, $\varphi_3'=\varphi_1$, so the inverse transformation matrix is 

$$
\begin{aligned}
\M{U'}&=\begin{pmatrix}
0&0&1\\
0&1&0\\
-1&0&0\\
\end{pmatrix}\\
\M{U'}\M{U}&=\begin{pmatrix}
0&0&1\\
0&1&0\\
-1&0&0\\
\end{pmatrix}
\begin{pmatrix}
0&0&-1\\
0&1&0\\
1&0&0\\
\end{pmatrix}
=\begin{pmatrix}
1&0&0\\
0&1&0\\
0&0&1\\
\end{pmatrix}
\end{aligned}
$$

so the two matrix are matrix inverses of each other.

-----

### 5.5.4

(
The transformation matrix $V$ given is not unitary. A possible unitary $V$ is

$$
\begin{aligned}
\begin{pmatrix}
1&0&0\\
0&\cos\theta&i\sin\theta\\
0&\sin\theta&-i\cos\theta
\end{pmatrix}
\end{aligned}
$$

which will be used to solve the problem.)

(a)

$$
\begin{aligned}
&\begin{pmatrix}
i\sin\theta&\cos\theta&0\\
-\cos\theta&i\sin\theta&0\\
0&0&1
\end{pmatrix}
\begin{pmatrix}
3\\-1\\-2
\end{pmatrix}=
\begin{pmatrix}
-\cos\theta+3i\sin\theta\\
-3\cos\theta-i\sin\theta\\
-2
\end{pmatrix}\\
&\begin{pmatrix}
1&0&0\\
0&\cos\theta&i\sin\theta\\
0&\sin\theta&-i\cos\theta
\end{pmatrix}
\begin{pmatrix}
-\cos\theta+3i\sin\theta\\
-3\cos\theta-i\sin\theta\\
-2
\end{pmatrix}=
\begin{pmatrix}
-\cos\theta+3i\sin\theta\\
-3\cos^2\theta-i\sin\theta(\cos\theta+2)\\
-3\sin\theta\cos\theta+i(2\cos\theta-\sin^2\theta)
\end{pmatrix}
\end{aligned}
$$

so

$$
\begin{aligned}
f(x)=(-\cos\theta+3i\sin\theta)\chi_1+(-3\cos^2\theta-i\sin\theta(\cos\theta+2))\chi_2+(-3\sin\theta\cos\theta+i(2\cos\theta-\sin^2\theta))\chi_3
\end{aligned}
$$

(b)

$$
\begin{aligned}
(UV)=&\begin{pmatrix}
i\sin\theta&\cos\theta&0\\
-\cos\theta&i\sin\theta&0\\
0&0&1
\end{pmatrix}
\begin{pmatrix}
1&0&0\\
0&\cos\theta&i\sin\theta\\
0&\sin\theta&-i\cos\theta
\end{pmatrix}=
\begin{pmatrix}
i\sin\theta&\cos^2\theta&i\sin\theta\cos\theta\\
-\cos\theta&i\sin\theta\cos\theta&-\sin^2\theta\\
0&\sin\theta&-i\cos\theta\\
\end{pmatrix}\\
&\begin{pmatrix}
i\sin\theta&\cos^2\theta&i\sin\theta\cos\theta\\
-\cos\theta&i\sin\theta\cos\theta&-\sin^2\theta\\
0&\sin\theta&-i\cos\theta\\
\end{pmatrix}
\begin{pmatrix}
3\\-1\\-2
\end{pmatrix}=
\begin{pmatrix}
-\cos^2\theta+i\sin\theta(3-2\cos\theta)\\
-3\cos\theta+2\sin^2\theta-i\sin\theta\cos\theta\\
-\sin\theta+2i\cos\theta
\end{pmatrix}\\
(VU)=
&\begin{pmatrix}
1&0&0\\
0&\cos\theta&i\sin\theta\\
0&\sin\theta&-i\cos\theta
\end{pmatrix}
\begin{pmatrix}
i\sin\theta&\cos\theta&0\\
-\cos\theta&i\sin\theta&0\\
0&0&1
\end{pmatrix}=
\begin{pmatrix}
i\sin\theta&\cos\theta&0\\
-\cos^2\theta&i\sin\theta\cos\theta&i\sin\theta\\
-\sin\theta\cos\theta&i\sin^2\theta&-i\cos\theta
\end{pmatrix}\\
&\begin{pmatrix}
i\sin\theta&\cos\theta&0\\
-\cos^2\theta&i\sin\theta\cos\theta&i\sin\theta\\
-\sin\theta\cos\theta&i\sin^2\theta&-i\cos\theta
\end{pmatrix}
\begin{pmatrix}
3\\-1\\-2
\end{pmatrix}=
\begin{pmatrix}
-\cos\theta+3i\sin\theta\\
-3\cos^2\theta-i\sin\theta(\cos\theta+2)\\
-3\sin\theta\cos\theta+i(2\cos\theta-\sin^2\theta)
\end{pmatrix}
\end{aligned}
$$

So only applying $VU$ gives the same answer as (a), which is quite obvious because $U$ is applied first.

-----

### 5.5.5.


(a) Let the normalized $\PP{n}=a_nP_n$ and $\FF{n}=b_nP_n$. Let the factors $a_n$ and $b_n$ be positive real numbers (every $a_ne^{i\theta}$ can also normalize the functions, as well as $b_ne^{i\theta}$)

$$
\begin{aligned}
\II{|a_0|^2P_0^2}&=|a_0|^22=1,\quad a_0=\frac{1}{\sqrt{2}},\quad\PP{0}=\frac{1}{\sqrt{2}}\\
\II{|a_1|^2P_1^2}&=|a_1|^2\frac{2}{3}=1,\quad a_1=\sqrt{\frac{3}{2}},\quad\PP{1}=\sqrt{\frac{3}{2}}x\\
\II{|a_2|^2P_2^2}&=|a_2|^2\frac{2}{5}=1,\quad a_2=\sqrt{\frac{5}{2}},\quad\PP{2}=\sqrt{\frac{5}{2}}(\frac{3}{2}x^2-\frac{1}{2})\\
\II{|b_0|^2F_0^2}&=|b_0|^2\frac{2}{5}=1,\quad b_0=\sqrt{\frac{5}{2}},\quad\FF{1}=\sqrt{\frac{5}{2}}x^2\\
\II{|b_1|^2F_1^2}&=|b_1|^2\frac{2}{3}=1,\quad b_1=\sqrt{\frac{3}{2}},\quad\FF{1}=\sqrt{\frac{3}{2}}x\\
\II{|b_2|^2F_2^2}&=|b_2|^28=1,\quad b_2=\frac{1}{\sqrt{8}},\quad\FF{2}=\frac{1}{\sqrt{8}}(5x^2-3)
\end{aligned}
$$

(b) $U_{ij}=\II{F_i^\star P_j}$. Note that except $U_{00},U_{02},U_{11},U_{20},U_{22}$, all the other $U_{ij}$ vanish because $F_i^\star P_j$ are odd functions for these $i,j$.

$$
\begin{aligned}
U_{00}&=\II{\frac{\sqrt{5}}{2}x^2}=\frac{\sqrt{5}}{3}\\
U_{02}&=\II{\frac{5}{2}(\frac{3}{2}x^4-\frac{1}{2}x^2)}=\frac{2}{3}\\
U_{11}&=\II{\frac{3}{2}x^2}=1\\
U_{20}&=\II{\frac{1}{4}(5x^2-3)}=-\frac{2}{3}\\
U_{22}&=\II{\frac{\sqrt{5}}{4}(\frac{15}{2}x^4-7x^2+\frac{3}{2})}=\frac{\sqrt{5}}{3}
\end{aligned}
$$

so

$$
\begin{aligned}
\M{U}=
\begin{pmatrix}
\frac{\sqrt{5}}{3}&0&\frac{2}{3}\\
0&1&0\\
-\frac{2}{3}&0&\frac{\sqrt{5}}{3}
\end{pmatrix}
\end{aligned}
$$

(c)$V_{ij}=\II{P_i^\star F_j}$. Note that except $V_{00},V_{02},V_{11},V_{20},V_{22}$, all the other $V_{ij}$ vanish because $P_i^\star F_j$ are odd functions for these $i,j$.

$$
\begin{aligned}
V_{00}&=\II{\frac{\sqrt{5}}{2}x^2}=\frac{\sqrt{5}}{3}\\
V_{02}&=\II{\frac{1}{4}(5x^2-3)}=-\frac{2}{3}\\
V_{11}&=\II{\frac{3}{2}x^2}=1\\
V_{20}&=\II{\frac{5}{2}(\frac{3}{2}x^4-\frac{1}{2}x^2)}=\frac{2}{3}\\
V_{22}&=\II{\frac{\sqrt{5}}{4}(\frac{15}{2}x^4-7x^2+\frac{3}{2})}=\frac{\sqrt{5}}{3}
\end{aligned}
$$

so

$$
\begin{aligned}
\M{V}=
\begin{pmatrix}
\frac{\sqrt{5}}{3}&0&-\frac{2}{3}\\
0&1&0\\
\frac{2}{3}&0&\frac{\sqrt{5}}{3}
\end{pmatrix}
\end{aligned}
$$

(d)

$$
\begin{aligned}
\M{U}^{-1}&=\begin{pmatrix}
\frac{\sqrt{5}}{3}&0&-\frac{2}{3}\\
0&1&0\\
\frac{2}{3}&0&\frac{\sqrt{5}}{3}
\end{pmatrix}=\M{V}\\
\M{V}^{-1}&=\begin{pmatrix}
\frac{\sqrt{5}}{3}&0&\frac{2}{3}\\
0&1&0\\
-\frac{2}{3}&0&\frac{\sqrt{5}}{3}
\end{pmatrix}=\M{U}\\
\M{U}\M{U}^{-1}&=\begin{pmatrix}
\frac{\sqrt{5}}{3}&0&\frac{2}{3}\\
0&1&0\\
-\frac{2}{3}&0&\frac{\sqrt{5}}{3}
\end{pmatrix}
\begin{pmatrix}
\frac{\sqrt{5}}{3}&0&-\frac{2}{3}\\
0&1&0\\
\frac{2}{3}&0&\frac{\sqrt{5}}{3}
\end{pmatrix}=
\begin{pmatrix}
1&0&0\\
0&1&0\\
0&0&1
\end{pmatrix}\\
\M{V}\M{V}^{-1}&=\begin{pmatrix}
\frac{\sqrt{5}}{3}&0&-\frac{2}{3}\\
0&1&0\\
\frac{2}{3}&0&\frac{\sqrt{5}}{3}
\end{pmatrix}
\begin{pmatrix}
\frac{\sqrt{5}}{3}&0&\frac{2}{3}\\
0&1&0\\
-\frac{2}{3}&0&\frac{\sqrt{5}}{3}
\end{pmatrix}=
\begin{pmatrix}
1&0&0\\
0&1&0\\
0&0&1
\end{pmatrix}
\end{aligned}
$$

(e)

$$
\renewcommand{\arraystretch}{2}
\begin{aligned}
\V{f}_{P}&=
\begin{pmatrix}
\II{(\frac{1}{\sqrt{2}})(5x^2-3x+1)}\\
\II{(\sqrt{\frac{3}{2}}x)(5x^2-3x+1)}\\
\II{\sqrt{\frac{5}{2}}(\frac{3}{2}x^2-\frac{1}{2})(5x^2-3x+1)}\\
\end{pmatrix}=
\begin{pmatrix}
\frac{8\sqrt{2}}{3}\\-\sqrt{6}\\\frac{2\sqrt{10}}{3}
\end{pmatrix}\\
\V{f}_{F}&=
\begin{pmatrix}
\II{(\sqrt{\frac{5}{2}}x^2)(5x^2-3x+1)}\\
\II{(\sqrt{\frac{3}{2}}x)(5x^2-3x+1)}\\
\II{\frac{1}{\sqrt{8}}(5x^2-3)(5x^2-3x+1)}\\
\end{pmatrix}=
\begin{pmatrix}
\frac{4\sqrt{10}}{3}\\-\sqrt{6}\\-\frac{2\sqrt{2}}{3}
\end{pmatrix}\\
\M{U}\V{f}_{P}&=\begin{pmatrix}
\frac{\sqrt{5}}{3}&0&\frac{2}{3}\\
0&1&0\\
-\frac{2}{3}&0&\frac{\sqrt{5}}{3}
\end{pmatrix}
\begin{pmatrix}
\frac{8\sqrt{2}}{3}\\-\sqrt{6}\\\frac{2\sqrt{10}}{3}
\end{pmatrix}=
\begin{pmatrix}
\frac{4\sqrt{10}}{3}\\-\sqrt{6}\\-\frac{2\sqrt{2}}{3}
\end{pmatrix}=\V{f}_F
\end{aligned}
$$



## 5.6 Transformations of Operators

### 5.6.1

(a) 

$$
\renewcommand{\arraystretch}{1.2}
\begin{aligned}
S_x=
\begin{pmatrix}
0&\frac{1}{2}\\
\frac{1}{2}&0
\end{pmatrix},\quad
S_y=
\begin{pmatrix}
0&\frac{-i}{2}\\
\frac{i}{2}&0
\end{pmatrix}
S_z=
\begin{pmatrix}
\frac{1}{2}&0\\
0&\frac{-1}{2}
\end{pmatrix}
\end{aligned}
$$

(b)

$$
\begin{aligned}
\br{\varphi_1'}{\varphi_2'}&=\br{C(\alpha+\beta)}{C(\alpha-\beta)}=|C|^2(\br{\alpha}{\alpha}-\br{\alpha}{\beta}+\br{\beta}{\alpha}-\br{\beta}{\beta})=|C|^2(1-1)=0\\
\br{\varphi_1'}{\varphi_1'}&=\br{C(\alpha+\beta)}{C(\alpha+\beta)}=|C|^2(\br{\alpha}{\alpha}+\br{\alpha}{\beta}+\br{\beta}{\alpha}+\br{\beta}{\beta})=|C|^22=1
\end{aligned}
$$

so $C=\frac{1}{\sqrt{2}}$ can normalize $\varphi_1'$ and $\varphi_2'$. The transformation matrix $\M{U}$ is

$$
\begin{aligned}
\M{U}=
\begin{pmatrix}
\br{\varphi_1'}{\varphi_1}&\br{\varphi_1'}{\varphi_2}\\
\br{\varphi_2'}{\varphi_1}&\br{\varphi_2'}{\varphi_2}
\end{pmatrix}=
\begin{pmatrix}
\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\\
\frac{1}{\sqrt{2}}&\frac{-1}{\sqrt{2}}
\end{pmatrix}
\end{aligned}
$$

(c)

$$
\begin{aligned}
S_x'&=\M{U}S_x\M{U}^{-1}=
\begin{pmatrix}
\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\\
\frac{1}{\sqrt{2}}&\frac{-1}{\sqrt{2}}
\end{pmatrix}
\begin{pmatrix}
0&\frac{1}{2}\\
\frac{1}{2}&0
\end{pmatrix}
\begin{pmatrix}
\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\\
\frac{1}{\sqrt{2}}&\frac{-1}{\sqrt{2}}
\end{pmatrix}=\begin{pmatrix}
\frac{1}{2}&0\\
0&\frac{-1}{2}
\end{pmatrix}\\
S_y'&=\M{U}S_y\M{U}^{-1}=
\begin{pmatrix}
\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\\
\frac{1}{\sqrt{2}}&\frac{-1}{\sqrt{2}}
\end{pmatrix}
\begin{pmatrix}
0&\frac{-i}{2}\\
\frac{i}{2}&0
\end{pmatrix}
\begin{pmatrix}
\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\\
\frac{1}{\sqrt{2}}&\frac{-1}{\sqrt{2}}
\end{pmatrix}=\begin{pmatrix}
0&\frac{i}{2}\\
\frac{-i}{2}&0
\end{pmatrix}\\
S_z'&=\M{U}S_z\M{U}^{-1}=
\begin{pmatrix}
\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\\
\frac{1}{\sqrt{2}}&\frac{-1}{\sqrt{2}}
\end{pmatrix}
\begin{pmatrix}
\frac{1}{2}&0\\
0&\frac{-1}{2}
\end{pmatrix}
\begin{pmatrix}
\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\\
\frac{1}{\sqrt{2}}&\frac{-1}{\sqrt{2}}
\end{pmatrix}=\begin{pmatrix}
0&\frac{1}{2}\\
\frac{1}{2}&0
\end{pmatrix}
\end{aligned}
$$

-----

### 5.6.2

(a) Note that $y\pdv{}{z}(e^{-r^2})-z\pdv{}{y}(e^{-r^2})=e^{-r^2}(-2r)(y\frac{z}{r}-z\frac{y}{r})=0$, so

$$
\begin{aligned}
L_x\varphi_1&=0\\
L_x\varphi_2&=-iC(-ze^{-r^2})=i\varphi_3\\
L_x\varphi_3&=-iC(ye^{-r^2})=-i\varphi_2
\end{aligned}
$$

so in matrix form,

$$
\begin{aligned}
L_x=
\begin{pmatrix}
0&0&0\\
0&0&-i\\
0&i&0
\end{pmatrix}
\end{aligned}
$$

(b)

$$
\begin{aligned}
L_x'=\M{U}L_x\M{U}^{-1}=
\begin{pmatrix}
1&0&0\\
0&\frac{1}{\sqrt{2}}&\frac{-i}{\sqrt{2}}\\
0&\frac{1}{\sqrt{2}}&\frac{i}{\sqrt{2}}\\
\end{pmatrix}
\begin{pmatrix}
0&0&0\\
0&0&-i\\
0&i&0
\end{pmatrix}
\begin{pmatrix}
1&0&0\\
0&\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}\\
0&\frac{i}{\sqrt{2}}&\frac{-i}{\sqrt{2}}\\
\end{pmatrix}=
\begin{pmatrix}
0&0&0\\
0&1&0\\
0&0&-1
\end{pmatrix}
\end{aligned}
$$

(c) $\varphi_i'$ is the $i^{th}$ column of $\M{U}^{-1}$ in $\varphi_i$ basis, so

$$
\begin{aligned}
\varphi_1'=Cxe^{-r^2}\quad\varphi_2'=C\frac{y+iz}{\sqrt{2}}e^{-r^2}\quad\varphi_3'=C\frac{y-iz}{\sqrt{2}}e^{-r^2}
\end{aligned}
$$

$L_x\varphi_i'$ is the $i^{th}$ column of $L_x'$ in $\varphi_i'$ basis, so

$$
\begin{aligned}
L_x\varphi_1'=0\quad L_x\varphi_2'=\varphi_2'=C\frac{y+iz}{\sqrt{2}}e^{-r^2}\quad L_x\varphi_3'=-\varphi_3'=-C\frac{y-iz}{\sqrt{2}}e^{-r^2} 
\end{aligned}
$$

-----

### 5.6.3

Definition:

$$
\begin{aligned}
\varphi_1&=T_{11}\chi_1\\
\varphi_2&=T_{12}\chi_1+T_{22}\chi_2\\
\varphi_3&=T_{13}\chi_1+T_{23}\chi_2+T_{33}\chi_3\\
\M{T}&=
\begin{pmatrix}
T_{11}&T_{12}&T_{13}\\
0&T_{22}&T_{23}\\
0&0&T_{33}
\end{pmatrix}
\end{aligned}
$$

Let $\psi_i$ be the orthogonalized but yet normalized functions, so

$$
\begin{aligned}
\psi_1&=\chi_1\\
\psi_2&=\chi_2-\psi_1\frac{\br{\psi_1}{\chi_2}}{\br{\psi_1}{\psi_1}}\\
\psi_3&=\chi_3-\psi_2\frac{\br{\psi_2}{\chi_3}}{\br{\psi_2}{\psi_2}}-\psi_1\frac{\br{\psi_1}{\chi_3}}{\br{\psi_1}{\psi_1}}
\end{aligned}
$$

By comparing the coefficients of $\chi_n$ in $\varphi_n$ and $\psi_n$, we have

$$
\begin{aligned}
\varphi_n=T_{nn}\psi_n
\end{aligned}
$$

Let

$$
\begin{aligned}
S_{ij}&=\br{\chi_i}{\chi_j}\\
\M{S}&=
\begin{pmatrix}
\br{\chi_1}{\chi_1}&\br{\chi_1}{\chi_2}&\br{\chi_1}{\chi_3}\\
\br{\chi_2}{\chi_1}&\br{\chi_2}{\chi_2}&\br{\chi_2}{\chi_3}\\
\br{\chi_3}{\chi_1}&\br{\chi_3}{\chi_2}&\br{\chi_3}{\chi_3}\\
\end{pmatrix}\\
D_1&=\br{\chi_1}{\chi_1}\\
D_2&=
\begin{vmatrix}
\br{\chi_1}{\chi_1}&\br{\chi_1}{\chi_2}\\
\br{\chi_2}{\chi_1}&\br{\chi_2}{\chi_2}\\
\end{vmatrix}\\
D_3&=
\begin{vmatrix}
\br{\chi_1}{\chi_1}&\br{\chi_1}{\chi_2}&\br{\chi_1}{\chi_3}\\
\br{\chi_2}{\chi_1}&\br{\chi_2}{\chi_2}&\br{\chi_2}{\chi_3}\\
\br{\chi_3}{\chi_1}&\br{\chi_3}{\chi_2}&\br{\chi_3}{\chi_3}\\
\end{vmatrix}
\end{aligned}
$$

Note that $S_{ij}^\star =\br{\chi_j}{\chi_1}$, $D_n^\star =D_n$. In this problem when $\vert A\vert^2=k$, let $A=\sqrt{k}$, without the phase factor.

From Eq. 5.79 we have

$$
\begin{aligned}
\M{T}^\dagger\M{S}\M{T}=\M{I}
\end{aligned}
$$

note that from the derivation, the equation will hold for any dimension, so

$$
\begin{aligned}
&T_{11}^*\br{\chi_1}{\chi_1}T_{11}=1\\
&T_{11}=\frac{1}{\sqrt{D_1}}\\
&\begin{pmatrix}
T_{11}^*&0\\
T_{12}^*&T_{22}^*\\
\end{pmatrix}
\begin{pmatrix}
\br{\chi_1}{\chi_1}&\br{\chi_1}{\chi_2}\\
\br{\chi_2}{\chi_1}&\br{\chi_2}{\chi_2}\\
\end{pmatrix}
\begin{pmatrix}
T_{11}&T_{12}\\
0&T_{22}\\
\end{pmatrix}=
\begin{pmatrix}
1&0\\
0&1\\
\end{pmatrix}
\end{aligned}
$$

Take the determinant of both sides:

$$
\begin{aligned}
&T_{11}^*T_{22}^*D_2T_{11}T_{22}=1\\
&|T_{22}|^2=\frac{1}{|T_{11}|^2D_2}=\frac{D_1}{D_2},\quad T_{22}=\sqrt{\frac{D_1}{D_2}}\\
&\begin{pmatrix}
T_{11}^*&0&0\\
T_{12}^*&T_{22}^*&0\\
T_{13}^*&T_{23}^*&T_{33}^*
\end{pmatrix}
\begin{pmatrix}
\br{\chi_1}{\chi_1}&\br{\chi_1}{\chi_2}&\br{\chi_1}{\chi_3}\\
\br{\chi_2}{\chi_1}&\br{\chi_2}{\chi_2}&\br{\chi_2}{\chi_3}\\
\br{\chi_3}{\chi_1}&\br{\chi_3}{\chi_2}&\br{\chi_3}{\chi_3}\\
\end{pmatrix}
\begin{pmatrix}
T_{11}&T_{12}&T_{13}\\
0&T_{22}&T_{23}\\
0&0&T_{33}
\end{pmatrix}=
\begin{pmatrix}
1&0&0\\
0&1&0\\
0&0&1
\end{pmatrix}\\
&T_{11}^*T_{22}^*T_{33}^*D_2T_{11}T_{22}T_{33}=1\\
|T_{33}|^2&=\frac{1}{|T_{22}|^2|T_{11}|^2D_3}=\frac{D_2}{D_3},\quad T_{33}=\sqrt{\frac{D_2}{D_3}}\\
\psi_1&=\chi_1\\
\varphi_1&=T_{11}\chi_1=\frac{\chi_1}{\sqrt{D_1}}\\
\psi_2&=\chi_2-\psi_1\frac{\br{\psi_1}{\chi_2}}{\br{\psi_1}{\psi_1}}=\chi_2-\chi_1\frac{S_{12}}{S_{11}}\\
\varphi_2&=T_{22}\psi_2=\sqrt{\frac{D_1}{D_2}}(\chi_1\frac{-S_{12}}{S_{11}}+\chi_2)=\chi_1\frac{-S_{12}}{\sqrt{D_1D_2}}+\chi_2\sqrt{\frac{D_1}{D_2}}\\
\psi_3&=\chi_3-\psi_2\frac{\br{\psi_2}{\chi_3}}{\br{\psi_2}{\psi_2}}-\psi_1\frac{\br{\psi_1}{\chi_3}}{\br{\psi_1}{\psi_1}}\\
&=\chi_3-(\chi_2-\chi_1\frac{S_{12}}{S_{11}})\frac{S_{23}-S_{13}\frac{S_{21}}{S_{11}}}{S_{22}-\frac{S_{12}S_{21}}{S_{11}}}-\chi_1\frac{S_{13}}{S_{11}}\\
&=\chi_3+\chi_2\frac{S_{13}S_{21}-S_{11}S_{23}}{S_{11}S_{22}-S_{12}S_{21}}+\chi_1\frac{S_{11}S_{12}S_{13}-S_{12}S_{21}S_{13}-S_{11}S_{22}S_{13}+S_{12}S_{21}S_{13}}{(S_{11}S_{22}-S_{12}S_{21})S_{11}}\\
&=\chi_3+\chi_2\frac{S_{13}S_{21}-S_{11}S_{23}}{D_2}+\chi_1\frac{S_{11}S_{12}S_{13}-S_{12}S_{21}S_{13}-S_{11}S_{22}S_{13}+S_{12}S_{21}S_{13}}{D_2D_1}\\
\varphi_3&=T_{33}\psi_3=\chi_3\sqrt{\frac{D_2}{D_3}}+\chi_2\frac{S_{13}S_{21}-S_{11}S_{23}}{\sqrt{D_2D_3}}+\chi_1\frac{S_{11}S_{12}S_{13}-S_{12}S_{21}S_{13}-S_{11}S_{22}S_{13}+S_{12}S_{21}S_{13}}{D_1\sqrt{D_2D_3}}
\end{aligned}
$$

so

$$
\begin{aligned}
\M{T}&=\begin{pmatrix}
T_{11}&T_{12}&T_{13}\\
0&T_{22}&T_{23}\\
0&0&T_{33}
\end{pmatrix}\\
T_{11}&=\frac{1}{\sqrt{D_1}}\\
T_{12}&=\frac{-S_{12}}{\sqrt{D_1D_2}}\\
T_{22}&=\sqrt{\frac{D_1}{D_2}}\\
T_{13}&=\frac{S_{11}S_{12}S_{13}-S_{12}S_{21}S_{13}-S_{11}S_{22}S_{13}+S_{12}S_{21}S_{13}}{D_1\sqrt{D_2D_3}}\\
T_{23}&=\frac{S_{13}S_{21}-S_{11}S_{23}}{\sqrt{D_2D_3}}\\
T_{33}&=\sqrt{\frac{D_2}{D_3}}
\end{aligned}
$$

## 5.7 Invariants

### 5.7.1

In matrix representation,

$$
\begin{aligned}
&\M{X}\M{P}-\M{P}\M{X}=i\M{I}\\
&\M{U}\M{X}\M{P}\M{U}^{-1}-\M{U}\M{P}\M{X}\M{U}^{-1}=i\M{U}\M{I}\M{U}^{-1}=i\M{I}\\
&\M{U}\M{X}\M{U}^{-1}\M{U}\M{P}\M{U}^{-1}-\M{U}\M{P}\M{U}^{-1}\M{U}\M{X}\M{U}^{-1}=i\M{I}\\
&\M{X}'\M{P}'-\M{P}'\M{X}'=i\M{I}
\end{aligned}
$$

so $[x,p]=i$ is invariant under unitary transformation.

-----

### 5.7.2

$$
\begin{aligned}
\boldsymbol{\sigma}_1'&=
\begin{pmatrix}
\cos\theta&\sin\theta\\
-\sin\theta&\cos\theta
\end{pmatrix}
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix}
\begin{pmatrix}
\cos\theta&-\sin\theta\\
\sin\theta&\cos\theta
\end{pmatrix}=
\begin{pmatrix}
\sin2\theta&\cos2\theta\\
\cos2\theta&-\sin2\theta
\end{pmatrix}\\
\boldsymbol{\sigma}_2'&=
\begin{pmatrix}
\cos\theta&\sin\theta\\
-\sin\theta&\cos\theta
\end{pmatrix}
\begin{pmatrix}
0&-i\\
i&0
\end{pmatrix}
\begin{pmatrix}
\cos\theta&-\sin\theta\\
\sin\theta&\cos\theta
\end{pmatrix}=
\begin{pmatrix}
0&-i\\
i&0
\end{pmatrix}\\
\boldsymbol{\sigma}_3'&=
\begin{pmatrix}
\cos\theta&\sin\theta\\
-\sin\theta&\cos\theta
\end{pmatrix}
\begin{pmatrix}
1&0\\
0&-1
\end{pmatrix}
\begin{pmatrix}
\cos\theta&-\sin\theta\\
\sin\theta&\cos\theta
\end{pmatrix}=
\begin{pmatrix}
\cos2\theta&-\sin2\theta\\
-\sin2\theta&-\cos2\theta
\end{pmatrix}\\
\boldsymbol{\sigma}_1'\boldsymbol{\sigma}_2'-\boldsymbol{\sigma}_2'\boldsymbol{\sigma}_1'&=
\begin{pmatrix}
i\cos2\theta&-i\sin2\theta\\
-i\sin2\theta&-i\cos2\theta
\end{pmatrix}-
\begin{pmatrix}
-i\cos2\theta&i\sin2\theta\\
i\sin2\theta&i\cos2\theta
\end{pmatrix}
=\begin{pmatrix}
2i\cos2\theta&-2i\sin2\theta\\
-2i\sin2\theta&-2i\cos2\theta
\end{pmatrix}=2i\boldsymbol{\sigma}_3'
\end{aligned}
$$

so $[\boldsymbol{\sigma}_1',\boldsymbol{\sigma}_2']=2i\boldsymbol{\sigma}_3'$ is still valid under transformation.

-----

### 5.7.3

(a) From Exercise 5.6.2(a), 

$$
\begin{aligned}
L_x\varphi_1&=0\\
L_x\varphi_2&=-iC(-ze^{-r^2})=i\varphi_3\\
L_x\varphi_3&=-iC(ye^{-r^2})=-i\varphi_2
\end{aligned}
$$

so in matrix form,

$$
\begin{aligned}
L_x=
\begin{pmatrix}
0&0&0\\
0&0&-i\\
0&i&0
\end{pmatrix}
\end{aligned}
$$

(b)

$$
\begin{aligned}
L_x\left[(x+iy)e^{-r^2} \right]=L_x\frac{\varphi_1+i\varphi_2}{C}=\frac{i(i\varphi_3)}{C}=-\frac{\varphi_3}{C}=-ze^{-r^2}
\end{aligned}
$$

(c) 
In matrix form, the above equation becomes

$$
\begin{aligned}
\begin{pmatrix}
0\\0\\-1
\end{pmatrix}=
\begin{pmatrix}
0&0&0\\
0&0&-i\\
0&i&0
\end{pmatrix}
\begin{pmatrix}
1\\i\\0
\end{pmatrix}
\end{aligned}
$$

after transformation,

$$
\begin{aligned}
\begin{pmatrix}
0\\\frac{i}{\sqrt{2}}\\\frac{-i}{\sqrt{2}}
\end{pmatrix}=
\begin{pmatrix}
0&0&0\\
0&1&0\\
0&0&-1
\end{pmatrix}
\begin{pmatrix}
1\\\frac{i}{\sqrt{2}}\\\frac{i}{\sqrt{2}}
\end{pmatrix}
\end{aligned}
$$

where the transformed $L_x$ has been obtained in Exercise 5.6.2(b).

(d) From Exercise 5.6.2(c),

$$
\begin{aligned}
\varphi_1'=Cxe^{-r^2}\quad\varphi_2'=C\frac{y+iz}{\sqrt{2}}e^{-r^2}\quad\varphi_3'=C\frac{y-iz}{\sqrt{2}}e^{-r^2}
\end{aligned}
$$

(e)

$$
\begin{aligned}
\varphi_2'\frac{i}{\sqrt{2}}+\varphi_3'\frac{-i}{\sqrt{2}}&=-Cze^{-r^2}\\
\varphi_1'+\varphi_2'\frac{i}{\sqrt{2}}+\varphi_3'\frac{i}{\sqrt{2}}&=C(x+iy)e^{-r^2}\\
L_x\varphi_1'&=L_x(Cxe^{-r^2})=0\\
L_x\varphi_2'&=L_x(C\frac{y+iz}{\sqrt{2}}e^{-r^2})=C\frac{y+iz}{\sqrt{2}}e^{-r^2}=\varphi_2'\\
L_x\varphi_3'&=L_x(C\frac{y-iz}{\sqrt{2}}e^{-r^2})
=-C\frac{y-iz}{\sqrt{2}}e^{-r^2}=-\varphi_3'
\end{aligned}
$$

so the vectors and operators transform correctly by $\M{U}$.

{% endraw %}
