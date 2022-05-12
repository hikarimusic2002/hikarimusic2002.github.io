---
layout: splash
title: "Mathematical Methods for Physicists Ch12"
permalink: /solutions/math_physics_12
author_profile: false

---

# Chapter 12: Further Topics in Analysis

{% raw %}

## 12.1 Orthogonal Polynomials

### 12.1.1

$$
\begin{aligned}
\newcommand{\pdv}[2]{\frac{\partial#1}{\partial#2}}
\newcommand{\V}{\mathbf}
\newcommand{\del}{\boldsymbol{\nabla}}
\newcommand{\abs}[1]{\left\vert #1\right\vert}
\newcommand{\lfpr}[1]{\left(#1\right)}
\newcommand{\lfbr}[1]{\left[#1\right]}
\def\dashint{{\int\limits_{-\infty}^\infty}\kern-10.0pt{-}\;}
g(x,t)&=\sum_{n=0}^\infty\frac{1}{n!}H_n(x)t^n\\
&=\sum_{n=0}^\infty\frac{(-1)^n}{n!}t^ne^{x^2}\left(\frac{d}{dx}\right)^ne^{-x^2}\\
&=\sum_{n=0}^\infty\frac{(-1)^n}{n!}t^ne^{x^2}\frac{n!}{2\pi i}\oint\limits_{c}\frac{e^{-z^2}}{(z-x)^{n+1}}dz\\
&=\oint\limits_c\left(\sum_{n=0}^\infty\left(\frac{-t}{z-x}\right)^n\frac{e^{x^2-z^2}}{2\pi i(z-x)} \right)dz\\
&=\oint\limits_c\frac{1}{1-\frac{-t}{z-x}}\frac{e^{x^2-z^2}}{2\pi i(z-x)}\\
&=\oint\limits_c\frac{e^{x^2-z^2}}{2\pi i(z-x+t)}dz
\end{aligned}
$$

The function has a simple pole at $z=x-t$ with residue

$$
\begin{aligned}
\lim_{z\to x-t}(z-x+t)\cdot\frac{e^{x^2-z^2}}{2\pi i(z-x+t)}=\frac{e^{-t^2+2xt}}{2\pi i}
\end{aligned}
$$

so we have

$$
\begin{aligned}
g(x,t)=2\pi i\cdot\frac{e^{-t^2+2xt}}{2\pi i}=e^{-t^2+2xt}
\end{aligned}
$$

### 12.1.2

(a)

$$
\begin{aligned}
w(x)=\frac{1}{x}\cdot e^{\int\frac{1-x}{x}dx}=\frac{1}{x}\cdot e^{\ln x-x}=e^{-x}
\end{aligned}
$$

Using the Rodrigues formula,

$$
\begin{aligned}
y_n(x)=e^x\left(\frac{d}{dx}\right)^n\left[e^{-x}x^n\right]
\end{aligned}
$$

(b)
(Using the rescaled polynomials with a factor $\frac{1}{n!}$ from the table)

$$
\begin{aligned}
g(x,t)&=\sum_{n=0}^\infty L_n(x)t^n\\
&=\sum_{n=0}^\infty\frac{e^xt^n}{n!}\left(\frac{d}{dx}\right)^n\left[x^ne^{-x} \right]\\
&=\sum_{n=0}^\infty\frac{e^xt^n}{n!}\frac{n!}{2\pi i}\oint\limits_c\frac{z^ne^{-z}}{(z-x)^{n+1}}dz\\
&=\oint\limits_c\left(\sum_{n=0}^\infty\left(\frac{tz}{z-x}\right)^n\frac{e^{x-z}}{2\pi i(z-x)} \right)dz\\
&=\oint\limits_c\frac{1}{1-\frac{tz}{z-x}}\frac{e^{x-z}}{2\pi i(z-x)}dz\\
&=\oint\limits_c\frac{e^{x-z}}{2\pi i(1-t)(z-\frac{x}{1-t})}dz
\end{aligned}
$$

The function has a simple pole at $z=\frac{x}{1-t}$ with residue 

$$
\begin{aligned}
\lim_{z\to\frac{x}{1-t}}(z-\frac{x}{1-t})\cdot\frac{e^{x-z}}{2\pi i(1-t)(z-\frac{x}{1-t})}=\frac{e^{\frac{-xt}{1-t}}}{2\pi i(1-t)}
\end{aligned}
$$

so we have

$$
\begin{aligned}
g(x,t)=2\pi i\cdot\frac{e^{\frac{-xt}{1-t}}}{2\pi i(1-t)}=\frac{e^{\frac{-xt}{1-t}}}{1-t}
\end{aligned}
$$

-----

### 12.1.3

From Equation 12.10:

$$
\begin{aligned}
p\left[wp^n\right]'=wp^n\left[(n-1)p'+q\right]
\end{aligned}
$$

Note that $\frac{d^kp}{dx^k}=0$ for $k>2$, so we have

$$
\begin{aligned}
\left(\frac{d}{dx} \right)^{n+1}\left(p\left[wp^n\right]' \right)&=\sum_{k=0}^{n+1}\binom{n+1}{k}\frac{d^kp}{dx^k}\frac{d^{n+1-k}\left[wp^n\right]'}{dx^{n+1-k}}\\
&=p\lfpr{\frac{d}{dx}}^{n+2}\lfbr{wp^n}+(n+1)p'\lfpr{\frac{d}{dx}}^{n+1}\lfbr{wp^n}+\frac{(n+1)n}{2}p''\lfpr{\frac{d}{dx}}^n\lfbr{wp^n}
\end{aligned}
$$

Also note that $\frac{d^k[(n-1)p'+q]}{dx^k}=0$ for $k>1$, so we have

$$
\begin{aligned}
&\lfpr{\frac{d}{dx}}^{n+1}\lfbr{(n-1)p'+q}wp^n\\
=&\sum_{k=0}^{n+1}\binom{n+1}{k}\frac{d^k\lfbr{(n-1)p'+q}}{dx^k}\frac{d^{n+1-k}\lfbr{wp^n}}{dx^{n+1-k}}\\
=&\lfbr{(n-1)p'+q}\lfpr{\frac{d}{dx}}^{n+1}\lfbr{wp^n}\;+\;(n+1)\lfbr{(n+1)p''+q'}\lfpr{\frac{d}{dx}}^n\lfbr{wp^n}
\end{aligned}
$$

Equating the two sides of the equation, dividing by $w$, rearranging, and using $y_n=\frac{1}{w}\lfpr{\frac{d}{dx}}^n\lfbr{wp^n}$, we have

$$
\begin{aligned}
\frac{p}{w}\lfpr{\frac{d}{dx}}^{n+2}\lfbr{wp^n}+\frac{2p'-q}{w}\lfpr{\frac{d}{dx}}^{n+1}\lfbr{wp^n}-\lfbr{\frac{n^2-n-2}{2}p''+(n+1)q'}y_n=0
\end{aligned}
$$

-----

### 12.1.4

From Equation 12.12:

$$
\begin{aligned}
\frac{p}{w}\lfpr{\frac{d}{dx}}^{n+2}\lfbr{wp^n}+\frac{2p'-q}{w}\lfpr{\frac{d}{dx}}^{n+1}\lfbr{wp^n}=\lfbr{\frac{n^2-n-2}{2}p''+(n+1)q'}y_n
\end{aligned}
$$

Calculate $py_n''$ and $qy_n'$:

$$
\begin{aligned}
    & p\,y_n''=p\lfbr{\frac{1}{w}\lfpr{\frac{d}{dx}}^n\lfbr{wp^n}}''=\frac{p}{w}\lfpr{\frac{d}{dx}}^{n+2}\lfbr{wp^n}+2p\frac{dw^{-1}}{dx}\lfpr{\frac{d}{dx}}^{n+1}\lfbr{wp^n}+p\frac{d^2w^{-1}}{dx^2}\lfpr{\frac{d}{dx}}^n\lfbr{wp^n}\\
    & q\,y_n'=q\lfbr{\frac{1}{w}\lfpr{\frac{d}{dx}}^n\lfbr{wp^n}}'=\frac{q}{w}\lfpr{\frac{d}{dx}}^{n+1}\lfbr{wp^n}+q\frac{dw^{-1}}{dx}\lfpr{\frac{d}{dx}}^n\lfbr{wp^n}
\end{aligned}
$$

Note that by definition we have

$$
\begin{aligned}
    & \frac{dw^{-1}}{dx}=-\frac{w'}{w^2}=\frac{p'-q}{wp}\\
    & \frac{d^2w^{-1}}{dx^2}=\frac{p''-q'}{wp}-\frac{p'-q}{(wp)^2}(wp)'=\frac{1}{wp}\lfbr{p''-q'-\frac{q(p'-q)}{p}}
\end{aligned}
$$

Substituting, summing together and using Equation 12.12, we have

$$
\begin{aligned}
p\,y_n''+q\,y_n'&=\frac{p}{w}\lfpr{\frac{d}{dx}}^{n+2}\lfbr{wp^n}+\frac{2p'-q}{w}\lfpr{\frac{d}{dx}}^{n+1}\lfbr{wp^n}+\frac{p''-q'}{w}\lfpr{\frac{d}{dx}}^n\lfbr{wp^n}\\
&=\lfbr{\frac{n^2-n-2}{2}p''+(n+1)q'}y_n+\lfbr{p''-q'}y_n=\lfbr{\frac{n^2-n}{2}p''+nq'}y_n
\end{aligned}
$$

which is Equation 12.16:

$$
\begin{aligned}
p\,y_n''+q\,y_n'-\lfbr{\frac{n^2-n}{2}p''+nq'}y_n=0
\end{aligned}
$$

-----

### 12.1.5

(a)

$$
\begin{aligned}
g(x,t)&=\sum_{n=0}^\infty J_n(x)t^n\\
&=\sum_{n=0}^\infty\frac{t^n}{2\pi i}\oint\limits_c e^{\frac{x}{2}(z-\frac{1}{z})}z^{-n-1}dz\\
&=\oint\limits_c\lfpr{\sum_{n=0}^\infty\frac{e^{\frac{x}{2}{(z-\frac{1}{z})}}}{2\pi iz}\lfpr{\frac{t}{z}}^n }dz\\
&=\oint\limits_c\frac{e^{\frac{x}{2}{(x-\frac{1}{z})}}}{2\pi iz}\frac{1}{1-\frac{t}{z}}dz\\
&=\oint\limits_c\frac{e^{\frac{x}{2}{(z-\frac{1}{z})}}}{2\pi i(z-t)}dz
\end{aligned}
$$

The function has a simple pole at $z=t$ with residue

$$
\begin{aligned}
\lim_{z\to t}(z-t)\cdot\frac{e^{\frac{x}{2}{(z-\frac{1}{z})}}}{2\pi i(z-t)}=\frac{e^{\frac{x}{2}{(t-\frac{1}{t})}}}{2\pi i}
\end{aligned}
$$

So the generating function of Bessel functions is

$$
\begin{aligned}
g(x,t)=e^{\frac{x}{2}{(t-\frac{1}{t})}}
\end{aligned}
$$

(b)
With similar process, the generating function of modified Bessel functions is

$$
\begin{aligned}
g(x,t)=e^{\frac{x}{2}{(t+\frac{1}{t})}}
\end{aligned}
$$

-----

### 12.1.6

$$
\begin{aligned}
\lfbr{1+(t^2-2tz)}^{-\frac{1}{2}}=1-\frac{1}{2}\lfpr{t^2-2tz}+\frac{3}{8}\lfpr{t^2-2tz}^2+\cdots=1+zt+\frac{3z^2-1}{2}t^2+\cdots
\end{aligned}
$$

so the coefficient is

$$
\begin{aligned}
    & a_0=P_0(z)=1\\
    & a_1=P_1(z)=z\\
    & a_2=P_2(z)=\frac{1}{2}\lfpr{3z^2-1}
\end{aligned}
$$

-----

### 12.1.7

$$
\begin{aligned}
    & \pdv{}{t}\lfpr{\frac{1}{1-2xt+t^2}}=\frac{2x-2t}{(1-2xt+t^2)^2}=\frac{2x-2t}{1-2xt+t^2}\sum_{n=0}^\infty U_n(x)t^n\\
    & \pdv{}{t}\lfpr{\sum_{n=0}^\infty U_n(x)t^n}=\sum_{n=1}^\infty nU_n(x)t^{n-1}
\end{aligned}
$$

Equating the two sides, we have

$$
\begin{aligned}
\sum_{n=0}^\infty 2xU_nt^n-\sum_{n=0}^\infty2U_nt^{n+1}=\sum_{n=1}^\infty nU_nt^{n-1}-\sum_{n=1}^\infty 2xnU_nt^n+\sum_{n=1}^\infty nU_nt^{n+1}
\end{aligned}
$$

Collect the terms of $t^n$, we have

$$
\begin{aligned}
2xU_n-2U_{n-1}=(n+1)U_{n+1}-2xnU_n+(n-1)U_{n-1}
\end{aligned}
$$

so the recurrence relation is (for $n\geq1$):

$$
\begin{aligned}
U_{n+1}(x)-2xU_n(x)+U_{n-1}(x)=0
\end{aligned}
$$

## 12.2 Bernoulli Numbers

### 12.2.1

$$
\begin{aligned}
\frac{t}{e^t-1}&=\frac{-te^{-t}}{e^{-t}-1}=\frac{-t(e^{-t}-1)-t}{e^{-t}-1}=\frac{-t}{e^{-t}-1}-t\\
\frac{te^{t}}{e^t-1}&=\frac{t}{1-e^{-t}}=\frac{-t}{e^{-t}-1}
\end{aligned}
$$

-----

### 12.2.2

$$
\begin{aligned}
        \frac{te^{ts}}{e^t-1} & =\frac{t(1+ts+\frac{t^2s^2}{2}+\cdots)}{1+t+\frac{t^2}{2}+\frac{t^3}{6}+\cdots-1}\\
        & =\frac{1+ts+\frac{t^2s^2}{2}+\cdots}{1+\frac{t}{2}+\frac{t^2}{6}+\cdots}\\
        & =(1+ts+\frac{t^2s^2}{2}+\cdots)(1-\frac{t}{2}-\frac{t^2}{6}+\frac{t^2}{4}+\cdots)\\
        & =1+(s-\frac{1}{2})t+(\frac{s^2}{2}-\frac{s}{2}+\frac{1}{12})t^2+\cdots\\
        & =B_0+B_1t+\frac{B_2}{2}t^2
\end{aligned}
$$

so we have

$$
\begin{aligned}
        B_0(s) & =1\\
        B_1(s) & =s-\frac{1}{2}\\
        B_2(s) & =s^2-s+\frac{1}{6}
\end{aligned}
$$

-----

### 12.2.3

$$
\begin{aligned}
\cot 2x=\frac{\cos 2x}{\sin 2x}=\frac{\cos^2x-\sin^2x}{2\sin x\cos x}=\frac{\cot x}{2}-\frac{\tan x}{2}
\end{aligned}
$$

so

$$
\begin{aligned}
\tan x=\cot x-2\cot2x
\end{aligned}
$$

From Equation 12.35, we have

$$
\begin{aligned}
        \cot x & =\sum_{n=0}^\infty(-1)^nB_{2n}\frac{2^{2n}x^{2n-1}}{(2n)!}\\
        2\cot2x & =\sum_{n=0}^\infty(-1)^nB_{2n}\frac{2^{2n+1}(2x)^{2n-1}}{(2n)!}=\sum_{n=0}^\infty(-1)^nB_{2n}\frac{2^{4n}x^{2n-1}}{(2n)!}
\end{aligned}
$$

so

$$
\begin{aligned}
\tan x & =\cot x-2\cot 2x\\
&=\sum_{n=0}^\infty\frac{(-1)^n2^{2n}(1-2^{2n})B_{2n}}{(2n)!}x^{2n-1}\\
&=\sum_{n=0}^\infty\frac{(-1)^{n-1}2^{2n}(2^{2n}-1)B_{2n}}{(2n)!}x^{2n-1}
\end{aligned}
$$

## 12.3 Euler-Maclaurin Integration Formula

### 12.3.1

$$
\begin{aligned}
        \sum_{m=1}^n m &= \int_1^n xdx+\frac{1}{2}+\frac{n}{2}+\frac{B_2}{2!}[1-1]\\
        & =\frac{n^2-1}{2}+\frac{n+1}{2}=\frac{1}{2}n(n+1)\\
        \sum_{m=1}^n m^2 & =\int_1^n x^2 dx+\frac{1}{2}+\frac{n^2}{2}+\frac{B_2}{2!}[2n-2]\\
        & =\frac{n^3-1}{3}+\frac{n^2+1}{2}+\frac{n-1}{6}=\frac{1}{6}n(n+1)(2n+1)\\
        \sum_{m=1}^n m^3 & =\int_1^n x^3dx+\frac{1}{2}+\frac{n^3}{2}+\frac{B_2}{2!}[3n^2-3]+\frac{B_4}{4!}[6-6]\\
        & =\frac{n^4-1}{4}+\frac{n^3+1}{2}+\frac{n^2-1}{4}=\frac{1}{4}n^2(n+1)^2\\
        \sum_{m=1}^n m^4 & =\int_1^n x^4 dx+\frac{1}{2}+\frac{n^4}{2}+\frac{B_2}{2!}[4n^3-4]+\frac{B_4}{4!}[24n-24]\\
        & =\frac{n^5-1}{5}+\frac{n^4+1}{2}+\frac{n^3-1}{3}-\frac{n-1}{30}\\
        & =\frac{1}{30}n(n+1)(2n+1)(3n^2+3n-1)
\end{aligned}
$$

-----

## 12.3.2

$$
\begin{aligned}
\gamma=\lim_{n\to\infty}\lfpr{\sum_{s=1}^n\frac{1}{s}-\ln n}=\sum_{s=1}^n\frac{1}{s}-\ln n+\lim_{n'\to\infty}\lfpr{\sum_{s=n+1}^{n'}\frac{1}{s}-\ln\frac{n'}{n}}
\end{aligned}
$$

The last term can be evaluated by Euler-Maclaurin formula:

$$
\begin{aligned}
        \lim_{n'\to\infty}\lfpr{\sum_{s=n+1}^{n'}\frac{1}{s}-\int\limits_{n}^{n'}\frac{1}{s}ds} & =\lim_{n'\to\infty}\lfbr{\frac{\frac{1}{n'}-\frac{1}{n}}{2}+\sum_{k=1}^N\frac{B_{2k}}{(2k)!}\lfpr{f^{(2k-1)}(n')-f^{2k-1}(n) } }+remainder\\
        & =\lim_{n'\to\infty}\lfbr{\frac{1}{2n'}-\frac{1}{2n}-\sum_{k=1}^N\frac{B_{2k}}{2k}\lfpr{\frac{1}{(n')^{2k}}-\frac{1}{n^{2k}} } }+remainder\\
        & =-\frac{1}{2n}+\sum_{k=1}^N\frac{B_{2k}}{(2k)n^{2k}}+remainder
\end{aligned}
$$

where we have evaluated 

$$
\begin{aligned}
f^{(2k-1)}(n)=-(2k-1)!\frac{1}{n^{2k}}
\end{aligned}
$$

So by ignoring the remainder term, we have

$$
\begin{aligned}
\gamma=\sum_{s=1}^n\frac{1}{s}-\ln n-\frac{1}{2n}+\sum_{k=1}^N\frac{B_{2k}}{(2k)n^{2k}}
\end{aligned}
$$

Let $n=1000$ and $N=2$ (evaluate the term of $B_2$ and $B4$), we have

$$
\begin{aligned}
\gamma=0.577215664902
\end{aligned}
$$

## 12.4 Dirichlet Series

### 12.4.1

Use $N-1=\sum_{n=1}^{N-1}\binom{2N}{2n}B_{2n}$ to obtain $B_{2n}$, and use $B_{2n}=(-1)^{n+1}\frac{2(2n)!}{(2\pi)^{2n}}\zeta(2n)$ to obtain $\zeta(2n)$:

$$
\begin{aligned}
    & n=1: \qquad && B_{2}=\frac{1}{6}\qquad && \zeta(2)=\frac{\pi^2}{6}\\
    & n=2: \qquad && B_4=-\frac{1}{30}\qquad && \zeta(4)=\frac{\pi^4}{90}\\
    & n=3: \qquad && B_6=\frac{1}{42}\qquad && \zeta(6)=\frac{\pi^6}{945}\\
    & n=4: \qquad && B_8=-\frac{1}{30}\qquad && \zeta(8)=\frac{\pi^8}{9450}\\
    & n=5: \qquad && B_{10}=\frac{5}{66}\qquad && \zeta(10)=\frac{\pi^{10}}{93555}
\end{aligned}
$$

-----

### 12.4.2

Using the substitution $1-x=e^{-t}$, we have

$$
\begin{aligned}
    \int_0^1\lfbr{\ln(1-x)}^2\frac{dx}{x} & =\int_0^\infty\frac{t^2e^{-t}}{1-e^{-t}}dt\\
    & =\int_0^\infty\lfpr{t^2e^{-t}\sum_{n=0}^\infty e^{-nt} }dt\\
    & =\sum_{n=0}^\infty\int_0^\infty t^2e^{-(1+n)t}dt\\
    & =\sum_{n=0}^\infty\frac{2}{(1+n)^3}\\
    & =\sum_{n=1}^\infty\frac{2}{n^3}\\
    & =2\zeta(3)
\end{aligned}
$$

where we expanded $(1-e^{-t})^{-1}$, and integrated by parts.

### 12.4.3

(This is essentially Exercise 11.8.18)

(a)

$$
\begin{aligned}
\int\limits_0^\infty\frac{(\ln z)^2}{1+z^2}dz=\int\limits_0^1\frac{(\ln z)^2}{1+z^2}dz+\int\limits_1^\infty\frac{(\ln z)^2}{1+z^2}dz
\end{aligned}
$$

By the substitution $z=\frac{1}{t}$, the first integral becomes

$$
\begin{aligned}
\int\limits_0^1\frac{(\ln z)^2}{1+z^2}dz=\int\limits_{\infty}^1\frac{(-\ln t)^2}{1+t^{-2}}(-t^{-2}dt)=\int\limits_1^\infty\frac{(\ln t)^2}{1+t^2}dt
\end{aligned}
$$

which is the same with the second integral. By another substitution $z=e^t$, we have

$$
\begin{aligned}
\int\limits_1^\infty\frac{(\ln z)^2}{1+z^2}dz
&=\int\limits_0^\infty\frac{t^2e^t}{1+e^{2t}}dt=\int\limits_0^\infty\frac{t^2e^{-t}}{1+e^{-2t}}dt\\
&=\int\limits_0^\infty\left(\sum_{n=0}^\infty(-1)^n\,t^2\, e^{-(2n+1)t} \right)dt\\
&=\sum_{n=0}^\infty(-1)^n\int\limits_0^\infty t^2\,e^{-(2n+1)t}dt\\
&=\sum_{n=0}^\infty(-1)^n\left[\frac{2e^{-(2n+1)t}}{-(2n+1)^3} \right]_0^\infty\\
&=2\sum_{n=0}^\infty(-1)^n(2n+1)^{-3}
\end{aligned}
$$

so

$$
\begin{aligned}
\int\limits_0^\infty\frac{(\ln z)^2}{1+z^2}dz&=2\int\limits_1^\infty\frac{(\ln z)^2}{1+z^2}dz\\
&=4\sum_{n=0}^\infty(-1)^n(2n+1)^{-3}\\
&=4\lfpr{1-\frac{1}{3^3}+\frac{1}{5^3}-\frac{1}{7^3}+\cdots}
\end{aligned}
$$

(b)
By the substitution $z=e^t$, we have

$$
\begin{aligned}
I=\int\limits_0^\infty\frac{(\ln z)^2}{1+z^2}dz=\int\limits_{-\infty}^\infty\frac{t^2}{1+e^{2t}}\cdot e^t dt=\int\limits_{-\infty}^\infty\frac{t^2}{e^t+e^{-t}}dt
\end{aligned}
$$

The function has poles at $z=(n+\frac{1}{2})i\pi$, and the pole at $z=\frac{i\pi}{2}$ is

$$
\begin{aligned}
\lim_{z\to\frac{i\pi}{2}}(z-\frac{i\pi}{2})\cdot\frac{z^2e^z}{1+e^{2z}}=\lim_{z\to\frac{i\pi}{2}}\frac{z^2e^z}{2e^{2z}}=\frac{\pi^2i}{8}
\end{aligned}
$$

Take the contour to be that in Figure 11.29. Integral on the two vertical segments vanish as $R\to\infty$, and integral on the segment at $x+i\pi$ is

$$
\begin{aligned}
\int\limits_{\infty}^{-\infty}\frac{(t+i\pi)^2}{e^{t+i\pi}+e^{-t-i\pi}}dt&=\int\limits_{-\infty}^\infty\frac{(t+i\pi)^2}{e^t+e^{-t}}\\
&=\int\limits_{-\infty}^\infty\frac{t^2}{e^t+e^{-t}}dt+\int\limits_{-\infty}^\infty\frac{2i\pi t}{e^t+e^{-t}}dt+\int\limits_{-\infty}^\infty\frac{-\pi^2}{e^t+e^{-t}}dt
\end{aligned}
$$

The first integral is $I$, the second integral vanishes as it is an odd function, and the third integral is

$$
\begin{aligned}
\int\limits_{-\infty}^\infty\frac{-\pi^2}{e^t+e^{-t}}dt=\int\limits_0^\infty\frac{-\pi^2}{x^2+1}dx=-\pi^2\Big[\tan^{-1}x\Big]_0^\infty=-\frac{\pi^3}{2}
\end{aligned}
$$

Using the residue theorem, we have

$$
\begin{aligned}
I+I-\frac{\pi^3}{2}&=2\pi i\cdot\frac{\pi^2i}{8}\\
I&=\frac{\pi^3}{8}
\end{aligned}
$$

-----

### 12.4.4

$$
\begin{aligned}{4}
    & \beta(2)=1 && -\frac{1}{3^2} && +\frac{1}{5^2} && -\frac{1}{7^2}+\cdots \\
    & \zeta(2)=1+\frac{1}{2^2} && +\frac{1}{3^2}+\frac{1}{4^2} && +\frac{1}{5^2}+\frac{1}{6^2} && +\frac{1}{7^2}+\cdots
\end{aligned}
$$

so

$$
\begin{aligned}
\zeta(2)+\beta(2)&=2\lfpr{1+\frac{1}{5^2}+\frac{1}{9^2}+\cdots}+\lfpr{\frac{1}{2^2}+\frac{1}{4^2}+\frac{1}{6^2}+\cdots}\\
&=2\sum_{k=1}^\infty(4k-3)^{-2}+\frac{1}{4}\zeta(2)
\end{aligned}
$$

Therefore

$$
\begin{aligned}
\beta(2)&=2\sum_{k=1}^\infty(4k-3)^{-2}-\frac{3}{4}\zeta(2)\\
&=2\sum_{k=1}^\infty(4k-3)^{-2}-\frac{\pi^2}{8}
\end{aligned}
$$

-----

### 12.4.5

(a)

$$
\begin{aligned}
        \int_0^1\frac{\ln(1+x)}{x}dx & =\int_0^1\frac{1}{x}\left(x-\frac{x^2}{2}+\frac{x^3}{3}-\frac{x^4}{4}+\cdots\right)dx\\
        & =\int_0^1\left(1-\frac{x}{2}+\frac{x^2}{3}-\frac{x^3}{4}+\cdots \right)dx\\
        & =\left[x-\frac{x^2}{2^2}+\frac{x^3}{3^2}-\frac{x^4}{4^2}+\cdots \right]_0^1\\
        & =\frac{1}{1^2}-\frac{1}{2^2}+\frac{1}{3^2}-\frac{1}{4^2}+\cdots
\end{aligned}
$$

Let the integral be $S$, and note that

$$
\begin{aligned}
\zeta(2)=\frac{1}{1^2}+\frac{1}{2^2}+\frac{1}{3^2}+\frac{1}{4^2}+\cdots
\end{aligned}
$$

so

$$
\begin{aligned}
\zeta(2)-S&=2\left(\frac{1}{2^2}+\frac{1}{4^2}+\frac{1}{6^2}+\cdots \right)\\
&=\frac{1}{2}\left(\frac{1}{1^2}+\frac{1}{2^2}+\frac{1}{3^2}+\cdots \right)=\frac{1}{2}\zeta(2)
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
S=\frac{1}{2}\zeta(2)
\end{aligned}
$$

(b)

$$
\begin{aligned}
        \lim_{a\to1}\int_0^a\frac{\ln(1-x)}{x}dx & =\lim_{a\to1}\int_0^a\frac{-1}{x}\left(x+\frac{x^2}{2}+\frac{x^3}{3}+\frac{x^4}{4}+\cdots \right)dx \\
        & =-\lim_{a\to1}\int_0^a\left(1+\frac{x}{2}+\frac{x^2}{3}+\frac{x^3}{4}+\cdots \right)dx\\
        & =-\lim_{a\to1}\left[x+\frac{x^2}{2^2}+\frac{x^3}{3^2}+\frac{x^4}{4^2}+\cdots \right]_0^a\\
        & =-\left(\frac{1}{1^2}+\frac{1}{2^2}+\frac{1}{3^2}+\frac{1}{4^2}+\cdots \right)\\
        & =-\zeta(2)
\end{aligned}
$$

-----

### 12.4.6

(a)

$$
\begin{aligned}
&\sum_{s=2}^n 2^{-s}\zeta(s)=\sum_{s=2}^n 2^{-s}\sum_{p=1}^\infty\frac{1}{p^s}=\sum_{s=2}^n\sum_{p=1}^\infty\frac{1}{(2p)^s}\\
&\sum_{p=1}^\infty(2p)^{-n-1}\left[1-\frac{1}{2p} \right]^{-1}=\sum_{p=1}^\infty\sum_{s=n+1}^\infty\frac{1}{(2p)^s}
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
         & \quad\,\sum_{s=2}^n 2^{-s}\zeta(2)+\sum_{p=1}^\infty(2p)^{-n-1}\left[1-\frac{1}{2p} \right]^{-1}\\
        & =  \sum_{p=1}^\infty\left(\sum_{s=2}^n\frac{1}{(2p)^s}+\sum_{n+1}^\infty\frac{1}{(2p)^s} \right)\\
        & =  \sum_{p=1}^\infty\sum_{s=2}^\infty\frac{1}{(2p)^s}=\sum_{p=1}^\infty\frac{\frac{1}{(2p)^2}}{1-\frac{1}{2p}}\\
        & =  \sum_{p=1}^\infty\frac{1}{2p(2p-1)}=\sum_{p=1}^\infty\lfpr{\frac{1}{2p-1}-\frac{1}{2p} }\\
        & =  1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\cdots\\
        & =  \ln 2
\end{aligned}
$$

(b)

$$
\begin{aligned}
\sum_{p=1}^\infty(2p)^{-n-1}\lfbr{1-\frac{1}{2p} }^{-1}<\sum_{p=1}^\infty(2p)^{-n-1}\cdot2=\frac{1}{2^n}\zeta(n+1)<1\times10^{-6},\qquad n\geq20
\end{aligned}
$$

So by taking $n=20$, we can obtain $\ln 2$ from the first summation of the precision to the sixth decimal place:

$$
\begin{aligned}
\sum_{s=2}^{20}2^{-s}\zeta(s)=0.693146
\end{aligned}
$$

-----

### 12.4.7

(a)

$$
\begin{aligned}
&\sum_{s=1}^n 4^{-2s}\zeta(2s)=\sum_{s=1}^n 4^{-2s}\sum_{p=1}^\infty\frac{1}{p^{2s}}=\sum_{s=1}^n\sum_{p=1}^\infty\frac{1}{(4p)^{2s}}\\
&\sum_{p=1}^\infty(4p)^{-2n-2}\lfbr{1-\frac{1}{(4p)^2}}^{-1}=\sum_{p=1}^\infty\sum_{s=n+1}^\infty\frac{1}{(4p)^{2s}}
\end{aligned}
$$

Therefore, 

$$
\begin{aligned}
        & \quad\,\, 1-2\sum_{s=1}^n 4^{-2s}\zeta(2s)-2\sum_{p=1}^\infty(4p)^{-2n-2}\lfbr{1-\frac{1}{(4p)^2} }^{-1}\\
        & =1-2\sum_{p=1}^\infty\lfpr{\sum_{s=1}^n\frac{1}{(4p)^{2s}}+\sum_{s=n+1}^\infty\frac{1}{(4p)^{2s}} }\\
        & =1-2\sum_{p=1}^\infty\sum_{s=1}^\infty\frac{1}{(4p)^{2s}}=1-2\sum_{p=1}^\infty\frac{\frac{1}{(4p)^2}}{1-\frac{1}{(4p)^2}}\\
        & =1-2\sum_{p=1}^\infty\frac{1}{(4p+1)(4p-1)}=1-\sum_{p=1}^\infty\lfpr{\frac{1}{4p-1}-\frac{1}{4p+1} }\\
        & =1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\frac{1}{9}-\cdots\\
        & =\frac{\pi}{4}
\end{aligned}
$$

(b)

$$
\begin{aligned}
2\sum_{p=1}^\infty(4p)^{-2n-2}\lfbr{1-\frac{1}{(4p)^2} }^{-1}<2\sum_{p=1}^\infty(4p)^{-2n-2}\cdot2=\frac{1}{4^{2n+1}}\zeta(2n+2)<1\times10^{-6},\qquad n\geq5
\end{aligned}
$$

So by taking $n=5$, we can obtain $\frac{\pi}{4}$ from the equation of the precision to the sixth decimal place:

$$
\begin{aligned}
1-2\sum_{s=1}^5 4^{-2s}\zeta(2s)=0.785398
\end{aligned}
$$

## 12.5 Infinite Products

### 12.5.1

(There should be a condition that $0\leq a_n<1$)

For the $1+a_n$ case, if $\sum a_n$ converges,

$$
\begin{aligned}
1+a_n\leq e^{a_n}\\
|\ln(1+a_n)|\leq a_n
\end{aligned}
$$

$\sum a_n$ converges, so $\sum\ln(1+a_n)$ converges by comparison test. Therefore, $\ln\prod(1+a_n)$ converges, which implies $\prod(1+a_n)$ converges.

For the $1+a_n$ case, if $\sum a_n$ diverges, 

$$
\begin{aligned}
p_n=\prod_{n=1}^N(1+a_n)\geq\sum_{n=1}^N a_n=s_n
\end{aligned}
$$

$s_n$ is monotonically increasing but diverges, which implies it is infinite, so $p_n$ is infinite and diverges.

For $1-a_n$ case, note that for $a_n<\frac{1}{2}$, we have $(1-a_n)\geq(1+2a_n)^{-1}$ and $(1-a_n)\leq(1+a_n)^{-1}$:

$$
\begin{aligned}
|\ln(1-a_n)|\leq|\ln(1+2a_n)|\leq 2a_n
\end{aligned}
$$

So if $\sum a_n$ converges, then $\sum\ln(1-a_n)$ converges, and therefore $\prod(1-a_n)$ converges.

$$
\begin{aligned}
-\ln(1-a_n)\geq\ln(1+a_n)
\end{aligned}
$$

So if $\sum a_n$ diverges, $\sum\ln(1+a_n)$ diverges, $\sum\ln(1-a_n)$ diverges, and therefore $\prod(1-a_n)$ diverges.

-----

### 12.5.2

$$
\begin{aligned}
\prod_{n=1}^\infty\lfpr{\frac{1+\frac{a}{n}}{1+\frac{b}{n}} }=\prod_{n=1}^\infty\lfpr{1+\frac{a-b}{n+b} }
\end{aligned}
$$

$\sum\frac{a-b}{n+b}=(a-b)\sum\frac{1}{n+b}$ diverges when $a\neq b$, so $\prod\lfpr{\frac{1+\frac{a}{n}}{1+\frac{b}{n}} }$ diverges by Theorem in Exercise 12.5.1.

-----

### 12.5.3

From Equation 11.89 and 11.90:

$$
\begin{aligned}
\sin z&=z\prod_{n=1}^\infty\lfpr{1-\frac{z^2}{n^2\pi^2} } =z\prod_{n=1}^\infty\lfpr{1-\frac{(2z)^2}{(2n)^2\pi^2} } =z\prod_{n\;even}\lfpr{1-\frac{(2z)^2}{n^2\pi^2} }\\
\cos z&=\prod_{n=1}^\infty\lfpr{1-\frac{z^2}{(n-\frac{1}{2})^2\pi^2} }=\prod_{n=1}^\infty\lfpr{1-\frac{(2z)^2}{(2n-1)^2\pi^2} } =\prod_{n\;odd}\lfpr{1-\frac{(2z)^2}{n^2\pi^2} }
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
2\sin z\cos z=2z\prod_{n=1}^\infty\lfpr{1-\frac{(2z)^2}{n^2\pi^2} }=\sin2z
\end{aligned}
$$

-----

### 12.5.4

$$
\begin{aligned}
\prod_{n=2}^\infty\lfpr{1+\frac{(-1)^n}{n} }=\prod_{n\;even}\lfpr{1+\frac{1}{n} }\lfpr{1+\frac{-1}{n+1} }=\prod_{n\;even}\frac{n+1}{n}\frac{n}{n+1}=1
\end{aligned}
$$

-----

### 12.5.5.

$$
\begin{aligned}
\prod_{n=2}^\infty\lfbr{1-\frac{2}{n(n+1)} }=\prod_{n=2}^\infty\frac{(n-1)(n+2)}{n(n+1)}=\prod_{n=2}^\infty\frac{n-1}{n}\prod_{n=4}^\infty\frac{n}{n-1}=\frac{1}{2}\cdot\frac{2}{3}=\frac{1}{3}
\end{aligned}
$$

-----

### 12.5.6

$$
\begin{aligned}
\prod_{n=2}^\infty\lfpr{1-\frac{1}{n^2} }=\prod_{n=2}^\infty\frac{(n-1)(n+1)}{n\cdot n}=\prod_{n=2}^\infty\frac{n-1}{n}\prod_{n=3}^\infty\frac{n}{n-1}=\frac{1}{2}
\end{aligned}
$$

-----

### 12.5.7

$$
\begin{aligned}
\prod_{p=1}^\infty(1+z^p)=\prod_{p=1}^\infty\frac{1-z^{2p}}{1-z^p}=\frac{\prod_{q=1}^\infty(1-z^{2q})}{\prod_{p=1}^\infty(1-z^p)}=\frac{1}{\prod_{q=1}^\infty(1-z^{2q-1})}=\prod_{q=1}^\infty(1-z^{2q-1})^{-1}
\end{aligned}
$$

The convergence of the infinite product requires the condition $\abs{z}<1$ because $\sum z^n$ converges when $\abs{z}<1$.

-----

### 12.5.8

$$
\begin{aligned}
\prod_{r=1}^\infty\lfpr{1+\frac{x}{r}}e^{-\frac{x}{r}}=\prod_{r=1}^\infty\lfpr{1+\frac{x}{r}}\lfpr{1-\frac{x}{r}+\sum_{n=2}^\infty a_n\left(\frac{x}{r}\right)^n}=\prod_{r=1}^\infty\lfpr{1+\sum_{n=2}^\infty b_n\left(\frac{x}{r}\right)^n }
\end{aligned}
$$

To verify the convergence, evaluate the sum:

$$
\begin{aligned}
\sum_{r=1}^\infty\sum_{n=2}^\infty b_n\lfpr{\frac{x}{r}}^n=\sum_{n=2}^\infty\sum_{r=1}^\infty b_n\lfpr{\frac{x}{r}}^n=\sum_{n=2}^\infty b_nx^n\zeta(n)
\end{aligned}
$$

which converges for finite $x$, so the infinte products converges.

-----

### 12.5.9

From Equation 12.35,

$$
\begin{aligned}
\cot x=\frac{1}{x}+\sum_{n=1}^\infty(-1)^n B_{2n}\frac{(2x)^{2n-1}}{(2n)!}
\end{aligned}
$$

so by integrating $\frac{d(\ln\sin x)}{dx}=\cot x$, we have

$$
\begin{aligned}
\ln\sin x=\ln x+\sum_{n=1}^\infty(-1)^nB_{2n}\frac{(2x)^{2n}}{(2n)\cdot(2n)!}=\ln x+\sum_{n=1}^\infty\frac{(-1)^n 2^{2n}B_{2n}}{(2n)\cdot(2n)!}x^{2n}
\end{aligned}
$$

so we have

$$
\begin{aligned}
a_0=0,\qquad a_{2n-1}=0,\qquad a_{2n}=\frac{(-1)^n2^{2n}B_{2n}}{(2n)\cdot(2n)!}
\end{aligned}
$$

for $n\in\mathbb{N}$.

-----

### 12.5.10

From Equation 11.89,

$$
\begin{aligned}
\ln\sin z=\ln z+\sum_{n=1}^\infty\ln\lfpr{1-\left(\frac{z}{n\pi}\right)^2 }=\ln z-\sum_{n=1}^\infty\sum_{m=1}^\infty\frac{1}{m}\lfpr{\frac{z}{n\pi} }^{2m}
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
z\cot z=z\frac{d(\ln\sin z)}{dz}=z\cdot\frac{1}{z}-z\sum_{n=1}^\infty\sum_{m=1}^\infty2\frac{z^{2m-1}}{(n\pi)^{2m}}=1-2\sum_{m,n=1}^\infty\lfpr{\frac{z}{n\pi} }^{2m}=1-2\sum_{m=1}^\infty\frac{\zeta(2m)}{\pi^{2m}}z^{2m}
\end{aligned}
$$

From Equation 12.35, we have

$$
\begin{aligned}
z\cot z=1+\sum_{n=1}^\infty\frac{(-1)^n2^{2n}B_{2n}}{(2n)!}z^{2n}
\end{aligned}
$$

So by equating each term in the summation of the two expression of $z\cot z$, we have

$$
\begin{aligned}
\frac{(-1)^n2^{2n}B_{2n}}{(2n)!}&=-\frac{2\zeta(2n)}{\pi^{2n}}\\
B_{2n}&=(-1)^{n-1}\frac{2(2n)!}{(2\pi)^{2n}}\zeta(2n)
\end{aligned}
$$

## 12.6 Asymptotic Series

### 12.6.1

From Exercise 11.8.26, we have

$$
\begin{aligned}
\int_0^\infty\cos\frac{\pi u^2}{2}du=\int_0^\infty\sin\frac{\pi u^2}{2}du=\frac{1}{2}
\end{aligned}
$$

so

$$
\begin{aligned}
C(x)&=\frac{1}{2}-\int_x^\infty\cos\frac{\pi u^2}{2}du\\
s(x)&=\frac{1}{2}-\int_x^\infty\sin\frac{\pi u^2}{2}du
\end{aligned}
$$

(a)
Substitute $\frac{\pi u^2}{2}=t$ and integrate by parts continuously, we have

$$
\begin{aligned}
        C(x) & =\frac{1}{2}-\int_{\frac{\pi x^2}{2}}^\infty\frac{\cos t}{\sqrt{2\pi t}}\,dt\\
        & \approx\frac{1}{2}-\left[\frac{\sin t}{(2\pi t)^{\frac{1}{2}}}-(-\pi)\frac{-\cos t}{(2\pi t)^{\frac{3}{2}}}+(-\pi)(-3\pi)\frac{-\sin t}{(2\pi t)^{\frac{5}{2}}}-(-\pi)(-3\pi)(-5\pi)\frac{\cos t}{(2\pi t)^{\frac{7}{2}}}+\cdots \right]_{\frac{\pi x^2}{2}}^\infty\\
        &  \approx\frac{1}{2}+\frac{1}{\pi x}\sin\frac{\pi x^2}{2}-\frac{\pi}{(\pi x)^3}\cos\frac{\pi x^2}{2}-\frac{1\cdot3\cdot\pi^2}{(\pi x)^5}\sin\frac{\pi x^2}{2}+\frac{1\cdot3\cdot5\cdot\pi^3}{(\pi x)^7}\cos\frac{\pi x^2}{2}+\cdots
\end{aligned}
$$

Note that the sign changes every two terms.

(b)
Substitute $\frac{\pi u^2}{2}=t$ and integrate by parts continuously, we have

$$
\begin{aligned}
        s(x) & =\frac{1}{2}-\int_{\frac{\pi x^2}{2}}^\infty\frac{\sin t}{\sqrt{2\pi t}}\,dt\\
        & \approx\frac{1}{2}-\left[\frac{-\cos t}{(2\pi t)^{\frac{1}{2}}}-(-\pi)\frac{-\sin t}{(2\pi t)^{\frac{3}{2}}}+(-\pi)(-3\pi)\frac{\cos t}{(2\pi t)^{\frac{5}{2}}}-(-\pi)(-3\pi)(-5\pi)\frac{\sin t}{(2\pi t)^{\frac{7}{2}}}+\cdots \right]_{\frac{\pi x^2}{2}}^\infty\\
        &  \approx\frac{1}{2}-\frac{1}{\pi x}\cos\frac{\pi x^2}{2}-\frac{\pi}{(\pi x)^3}\sin\frac{\pi x^2}{2}+\frac{1\cdot3\cdot\pi^2}{(\pi x)^5}\cos\frac{\pi x^2}{2}+\frac{1\cdot3\cdot5\cdot\pi^3}{(\pi x)^7}\cos\frac{\pi x^2}{2}-\cdots
\end{aligned}
$$

Note that the sign changes every two terms.

-----

### 12.6.2

Integrate by parts continuously:

$$
\begin{aligned}
        & \quad Ci(x)+i\,si(x) \\ 
        & =-\int_x^\infty\frac{e^{it}}{t}dt\\
        & \approx -\left[\frac{e^{it}}{i}\frac{1}{t}-\frac{e^{it}}{i^2}\frac{(-1)}{t^2}+\frac{e^{it}}{i^3}\frac{(-1)(-2)}{t^3}-\frac{e^{it}}{i^4}\frac{(-1)(-2)(-3)}{t^4}+\frac{e^{it}}{i^5}\frac{(-1)(-2)(-3)(-4)}{t^5}-\cdots \right]_x^\infty\\
        & \approx -\frac{i\,e^{it}}{t}\left[1-i\lfpr{\frac{1!}{t}}-\lfpr{\frac{2!}{t^2}}+i\lfpr{\frac{3!}{t^3}}+\lfpr{\frac{4!}{t^4}}-\cdots \right]
\end{aligned}
$$

which is Equation 12.92, so the asymptotic expansions of $Ci(x)$ and $si(x)$ are the same with that given in the text.

-----

### 12.6.3

$$
\begin{aligned}
        \mathrm{erf}(x) & =1-\frac{2}{\sqrt{\pi}}\int_x^\infty e^{-t^2}dt\\
        & =1-\frac{1}{\sqrt{\pi}}\int_{x^2}^\infty\frac{e^{-u}}{\sqrt{u}}\,du\\
        & \approx 1-\frac{1}{\sqrt{\pi}}\lfbr{\frac{-e^{-u}}{u^{\frac{1}{2}}}-\lfpr{-\frac{1}{2}}\frac{e^{-u}}{u^{\frac{3}{2}}}+\lfpr{-\frac{1}{2}}\lfpr{-\frac{3}{2}}\frac{-e^{-u}}{u^{\frac{5}{2}}}-\lfpr{-\frac{1}{2}}\lfpr{-\frac{3}{2}}\lfpr{-\frac{5}{2}}\frac{e^{-u}}{u^{\frac{7}{2}}}+\cdots }_{x^2}^\infty\\
        & \approx 1+\frac{1}{\sqrt{\pi}}\lfbr{-\frac{e^{-x^2}}{x}+\frac{1}{2}\frac{e^{-x^2}}{x^3}-\frac{1\cdot3}{2^2}\frac{e^{-x^2}}{x^5}+\frac{1\cdot3\cdot5}{2^3}\frac{e^{-x^2}}{x^7}-\cdots }\\
        & \approx 1-\frac{e^{-x^2}}{\sqrt{\pi}x}\lfbr{1-\frac{1}{2x^2}+\frac{1\cdot3}{2^2x^4}-\frac{1\cdot3\cdot5}{2^3x^6}+\cdots+(-1)^n\frac{(2n-1)!!}{2^nx^{2n}} }
\end{aligned}
$$

-----

### 12.6.4

Let $P_\nu(z)=1+\sum_{n=1}^\infty a_n$, then

$$
\begin{aligned}
\lim_{n\to\infty}\left|\frac{a_n}{a_{n-1}} \right|=\frac{(4n)^2(4n)^2}{(2n)(2n)(8z)^2}=\frac{n^2}{z^2}\to\infty
\end{aligned}
$$

as $n\to\infty$ for finite $z$, so $P_\nu(z)$ diverges and can only be an asymptotic series. Similarly is $Q_\nu(z)$.

-----

### 12.6.5

$\sum_{n=0}^\infty(-1)^n\frac{1}{x^{n+1}}$ is an alternating series and $\lim_{n\to\infty}\frac{1}{x^{n+1}}=0$, so it converges and is therefore not an asymptotic series.

-----

### 12.6.6

By the definition,

$$
\begin{aligned}
\gamma=\lim_{N\to\infty}\left(\sum_{s=1}^Ns^{-1}-\ln N \right)=\left(\sum_{s=1}^ns^{-1}-\ln n \right)+\lim_{N\to\infty}\left(\sum_{s=n+1}^N s^{-1}-\ln\frac{N}{n} \right)
\end{aligned}
$$

Let $f(x)=x^{-1}$, then $f^{(2k-1)}(x)=-(2k-1)!\,x^{-2k}$. By Euler-Maclaurin integration formula, we have

$$
\begin{aligned}
\sum_{s=n+1}^\infty s^{-1}=\int_n^Ns^{-1}ds+\frac{\frac{1}{N}-\frac{1}{n}}{2}+\sum_{k=1}^p\frac{B_{2k}}{(2k)!}\left(-\frac{(2k-1)!}{N^{2k}}+\frac{(2k-1)!}{n^{2k}} \right)+R_p
\end{aligned}
$$

so

$$
\begin{aligned}
\lim_{N\to\infty}\lfpr{\sum_{s=n+1}^Ns^{-1}-\ln\frac{N}{n} }=-\frac{1}{2n}+\sum_{k=1}^p\frac{B_{2k}}{(2k)n^{2k}}+R_p
\end{aligned}
$$

where $R_p$ can be arbitrarily small when $p$ is large enough. Therfore,

$$
\begin{aligned}
\gamma\approx\sum_{s=1}^ns^{-1}-\ln n-\frac{1}{2n}+\sum_{k=1}^\infty\frac{B_{2k}}{(2k)n^{2k}}
\end{aligned}
$$

-----

### 12.6.7

_(The answer given is incorrect. It is the asymptotic series for $\int_0^\infty\frac{e^{-xv}}{(1+v^2)}dv$)_

Substitute $u=xv$ and use the binomial expansion, we have

$$
\begin{aligned}
    & \quad\int_0^\infty\frac{e^{-xv}}{(1+v^2)^2}dv \\
    & =\int_0^\infty e^{-u}\lfpr{1+\frac{u^2}{x^2} }^{-2}\frac{du}{x}\\
    & =\int_0^\infty e^{-u}\sum_{n=0}^\infty\binom{-2}{n}\frac{u^{2n}}{x^{2n+1}}du\\
    & =\sum_{n=0}^\infty\binom{-2}{n}\frac{1}{x^{2n+1}}\int_0^\infty e^{-u}u^{2n}du\\
    & =\sum_{n=0}^\infty\frac{(-1)^n(n+1)\cdot(2n)!}{x^{2n+1}}\\
    & \approx\frac{1}{x}-\frac{2\cdot2!}{x^{3}}+\frac{3\cdot4!}{x^5}-\cdots+\frac{(-1)^n(n+1)\cdot(2n)!}{x^{2n+1}}
\end{aligned}
$$

where we have used $\binom{-2}{n}=(-1)^n(n+1)$ and $\int_0^\infty e^{-u}u^ndu=n!$.

## 12.7 Method of Steepest Descents

### 12.7.1

_The statement that "$\abs{F(z)}^2$ can have no extremum in the interior of a region in which $F$ is analytic" is incorrect. Let $F(z)=z$, then $\abs{F(z)}^2$ has a minimum at $z=0$. However, the fact used in the text is that "$\ln\abs{F}$" has no extremum in the interior where $F$ is analytic (Equation 12.100), and it is a true statement which we are going to prove._

We first prove that $\ln\abs{F(z)}$ is harmonic (satisfies the Laplace equation) if $F(z)$ is analytic. Let $F(z)=u(z)+iv(z)$, then

$$
\begin{aligned}
    \ln|F| & = \ln|\sqrt{u^2+v^2}|=\frac{1}{2}\ln(u^2+v^2)\\
    \pdv{\ln|F|}{x} & =\frac{u\pdv{u}{x}+v\pdv{v}{x}}{u^2+v^2}\\
    \pdv{^2\ln|F|}{x^2}&=\frac{\lfpr{\pdv{u}{x}}^2+\lfpr{\pdv{v}{x}}^2+u\pdv{^2u}{x^2}+v\pdv{^2v}{x^2}}{u^2+v^2}-\frac{2\lfpr{u\pdv{u}{x}+v\pdv{v}{x} }^2}{(u^2+v^2)^2}\\
    &=\frac{-(u^2-v^2)\lfbr{\lfpr{\pdv{u}{x}}^2-\lfpr{\pdv{v}{x}}^2 }-4uv\pdv{u}{x}\pdv{v}{x}+u\pdv{^2u}{x^2}+v\pdv{^2v}{x^2} }{(u^2+v^2)^2}\\
    \pdv{^2\ln|F|}{y^2}&=\frac{-(u^2-v^2)\lfbr{\lfpr{\pdv{u}{y}}^2-\lfpr{\pdv{v}{y}}^2 }-4uv\pdv{u}{y}\pdv{v}{y}+u\pdv{^2u}{y^2}+v\pdv{^2v}{y^2} }{(u^2+v^2)^2}
\end{aligned}
$$

Summing the two equations, and noting that by  Cauchy-Riemann conditions $\pdv{u}{x}=\pdv{v}{y}$, $\pdv{u}{y}=-\pdv{v}{x}$, we have

$$
\begin{aligned}
&\lfpr{\pdv{u}{x}}^2-\lfpr{\pdv{v}{x}}^2+\lfpr{\pdv{u}{y}}^2-\lfpr{\pdv{v}{y}}^2\\
=&\lfpr{\pdv{u}{x}}^2-\lfpr{\pdv{v}{x}}^2+\lfpr{\pdv{v}{x}}^2-\lfpr{\pdv{u}{x}}^2=0\\
&\pdv{u}{x}\pdv{v}{x}+\pdv{u}{y}\pdv{v}{y}=\pdv{u}{x}\pdv{v}{x}-\pdv{v}{x}\pdv{u}{x}=0\\
&\pdv{^2u}{x^2}+\pdv{^2u}{y^2}=0\qquad \pdv{^2v}{x^2}+\pdv{^2v}{y^2}=0
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
\pdv{^2\ln|F|}{x^2}+\pdv{^2\ln|F|}{y^2}=0
\end{aligned}
$$

which means $\ln\abs{F}$ is harmonic. By the mean value property of harmonic function (the 3D version of which has been proved in Exercise 3.9.9), we have

$$
\begin{aligned}
\ln|F(z_0)|=\frac{1}{2\pi r}\int_0^{2\pi}\ln|F(z_0+re^{i\theta})|\,rd\theta
\end{aligned}
$$

so the mean value of $\ln\abs{F}$ on a circle about any point $z_0$ is equal to $\ln\abs{F}$. Therefore, there cannot be an extremum of $\ln\abs{F}$ at $z_0$, otherwise the mean value on an circle around $z_0$ will be less than or greater than $\ln\abs{F(z_0)}$ (For the case $z_0$ being an maximum or minimum, respectively.)

-----

### 12.7.2

$$
\begin{aligned}
\int_0^s\cos x^2\,dx+i\int_0^s\sin x^2\,dx=\int_0^s e^{ix^2}dx=s\int_0^1 e^{is^2z^2}dz=\sqrt{t}\int_0^1 e^{itz^2}dz
\end{aligned}
$$

Let $w(z)=itz^2$, then $w'(z)=2itz$, $w''(z)=2it$. So the saddle point is $z=0$, and the direction of steepest descent is

$$
\begin{aligned}
\theta=-\frac{\arg w''}{2}+\frac{\pi}{2}=\frac{\pi}{4}
\end{aligned}
$$

Which means the original path moving from $(0,0)$ to $(1,0)$, is deformed to the path that starts from $(0,0)$, moving in the $\frac{\pi}{4}$ direction, and ends at $(1,0)$. To use Equation 12.108, note that in Equation 12.104 which is derived from , there is a factor "$2$" since both the ascending and descending parts are included, while in this problem since the saddle point happens to be the start point, only the descending part is involved in the integration. Therefore, use Equation 12.108 with an additional factor $\frac{1}{2}$, we have

$$
\begin{aligned}
f(t)\approx\frac{1}{2}\sqrt{t}e^0e^{i\frac{\pi}{4}}\sqrt{\frac{2\pi}{|2it|}}=\sqrt{\frac{\pi}{8}}+\sqrt{\frac{\pi}{8}}i
\end{aligned}
$$

so

$$
\begin{aligned}
&\int_0^s\cos x^2\,dx\approx\sqrt{\frac{\pi}{8}}\\
&\int_0^s\sin x^2\,dx\approx\sqrt{\frac{\pi}{8}}
\end{aligned}
$$

-----

### 12.7.3

Let $s=\abs{s}e^{i\alpha}$, then

$$
\begin{aligned}
\Gamma(s+1)=\int_0^\infty \rho^s e^{-\rho}d\rho=s^{s+1}\int_0^\infty e^{s(\ln z-z)}dz
\end{aligned}
$$

Proceeding as in Example 12.7.1, the saddle point is still $z=1$, and since $w'' (1,s)=-s=-\abs{s}e^{\alpha}$, we have

$$
\begin{aligned}
\theta=-\frac{\arg w''}{2}+(\frac{\pi}{2}\; or\; \frac{3\pi}{2})=-\frac{\alpha}{2}\; or\; \pi-\frac{\alpha}{2}
\end{aligned}
$$

Choose $\theta=-\frac{\alpha}{2}$, and use Equation 12.108,

$$
\begin{aligned}
\Gamma(s+1)\approx s^{s+1}e^{-s}e^{-\frac{i\alpha}{2}}\sqrt{\frac{2\pi}{|s|}}=\sqrt{2\pi s}\,s^se^{-s}\frac{\sqrt{s}}{\sqrt{|s|e^{i\alpha}}}=\sqrt{2\pi s}\,s^se^{-s}
\end{aligned}
$$

Note that at the vicinity of the saddle point $z=1$, $\mathfrak{Im}[s(\ln z-z)]=-\abs{s}\cos\alpha$ is constant.

## 12.8 Dispersion Relations

### 12.8.1

Let $f(z)=u(z)+iv(z)$ be a function meeting the conditions of Schwarz reflection principle. For real number $x$, $f(x)=f^\star(x^\star)=f^\star(x)$, which means $f(z)$ is real when $x$ is real, so $v(x)=0$. By the dispersion relation, $u(x)=0$, so $f(x)=0$. Therefore,

$$
\begin{aligned}
f(z)=\frac{1}{2\pi i}\int_{-\infty}^\infty\frac{f(x)}{x-z}dx=0
\end{aligned}
$$

which means $f(z)$ is identically zero.

-----

### 12.8.2

$$
\begin{aligned}
        f(x_0) & =\frac{1}{2\pi i}\left\{\int\limits_{-\infty}^{x_0-\delta}\frac{f(x)}{x-x_0}dx+\int\limits_{x_0+\delta}^\infty\frac{f(x)}{x-x_0}dx \right\}+\frac{1}{2\pi i}\int\limits_C\frac{f(x)}{x-x_0}dx\\
        & =\frac{1}{2\pi i}\dashint\frac{f(x)}{x-x_0}dx+\frac{f(x_0)}{2}
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
f(x_0)=\frac{1}{\pi i}\dashint\frac{f(x)}{x-x_0}dx
\end{aligned}
$$

-----

### 12.8.3

(a)
Let $f(z)=e^{iz}$, then by Jordan's lemma, since $\lim_{R\to\infty}\frac{1}{z-z_0}=0$,

$$
\begin{aligned}
\lim_{R\to\infty}\int\limits_C\frac{e^{iz}}{z-z_0}dz=0
\end{aligned}
$$

where $C$ is a semicircle of radius $R$ in the upper half-plane with center at the origin. Therefore, using the same contour, Equation 12.116 still holds:

$$
\begin{aligned}
f(z_0)=\frac{1}{2\pi i}\int\limits_{-\infty}^\infty\frac{f(x)}{x-z_0}dx
\end{aligned}
$$

(b)
$e^{ix}=\cos x+i\sin x$, so

$$
\begin{aligned}
\frac{1}{\pi}\dashint\frac{\sin x}{x-x_0}dx=\frac{1}{\pi}\dashint\frac{\sin(x+x_0)}{x}dx=\frac{1}{\pi}\dashint\frac{\sin x\cos x_0}{x}dx+\frac{1}{\pi}\dashint\frac{\cos x\sin x_0}{x}dx
\end{aligned}
$$

$\frac{\sin x}{x}$ is an even function, so by Exercise 1.10.2,

$$
\begin{aligned}
\dashint\frac{\sin x}{x}dx=2\int\limits_0^\infty\frac{\sin x}{x}dx=\pi
\end{aligned}
$$

$\frac{\cos x}{x}$ is an odd function, so

$$
\begin{aligned}
\dashint\frac{\cos x}{x}dx=0
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
\frac{1}{\pi}\dashint\frac{\sin x}{x-x_0}dx=\cos x_0
\end{aligned}
$$

which is the first part of the dispersion relations. The second part can be proved similarly:

$$
\begin{aligned}
\frac{1}{\pi}\dashint\frac{\cos x}{x-x_0}dx
&=\frac{1}{\pi}\dashint\frac{\cos(x+x_0)}{x}dx
=\frac{1}{\pi}\dashint\frac{\cos x\cos x_0}{x}dx-\frac{1}{\pi}\dashint\frac{\sin x\sin x_0}{x}dx\\
\frac{1}{\pi}\dashint\frac{\cos x}{x-x_0}dx&=-\sin x_0
\end{aligned}
$$

-----

### 12.8.4

If $f(x)=u(x)+iv(x)$ and $f(x)=f^*(-x)$, then $u(x)+iv(x)=u(-x)-iv(-x)$, which means $u(x)$ is even and $v(x)$ is odd.

(a)

$$
\begin{aligned}
        u(x_0) & =\frac{1}{\pi}\dashint\frac{v(x)}{x-x_0}dx\\
        & =\frac{1}{\pi}\dashint\frac{v(x)}{-x_0}\left(1+\frac{x}{x_0}+\cdots \right)dx\\
        & \approx -\frac{1}{\pi x_0}\dashint v(x)dx-\frac{1}{\pi x_0^2}\dashint xv(x)dx
\end{aligned}
$$

$v(x)$ is odd, so the first integral vanishes. $xv(x)$ is even, so the second integral becomes $2\int_0^\infty xv(x)dx$. Therefore,

$$
\begin{aligned}
u(x_0)\approx-\frac{2}{\pi x_0^2}\int_0^\infty xv(x)dx
\end{aligned}
$$

(b)

$$
\begin{aligned}
        v(x_0) & =-\frac{1}{\pi}\dashint\frac{u(x)}{x-x_0}dx\\
        & =-\frac{1}{\pi}\dashint\frac{u(x)}{-x_0}\left(1+\frac{x}{x_0}+\cdots \right)dx\\
        & \approx\frac{1}{\pi x_0}\dashint u(x)dx+\frac{1}{\pi x_0^2}\dashint xu(x)dx
\end{aligned}
$$

$u(x)$ is even, so the first integral becomes $2\int_0^\infty u(x)dx$. $xu(x)$ is odd, so the second integral vanishes. Therefore,

$$
\begin{aligned}
v(x_0)\approx\frac{2}{\pi x_0}\int_0^\infty u(x)dx
\end{aligned}
$$

-----

### 12.8.5

(a)
From the dispersion relations, 

$$
\begin{aligned}
        v(x_0)&=-\frac{1}{\pi}\dashint\frac{u(x)}{x-x_0}dx=-\frac{1}{1+x_0^2}\\
        u(x_0) & =\frac{1}{\pi}\dashint \frac{v(x)}{x-x_0}dx\\
        & =-\frac{1}{\pi}\dashint\frac{1}{1+x^2}\frac{1}{x-x_0}dx
\end{aligned}
$$

The function has three simple poles:

$$
\begin{aligned}
    & z=i\qquad && residue=\frac{1}{2i(i-x_0)}\\
    & z=-i\qquad && residue=\frac{1}{2i(i+x_0)}\\
    & z=x_0\qquad && residue=\frac{1}{1+x_0^2}
\end{aligned}
$$

The contour encloses $z=i$, and passes a semi-circle at $z=x_0$, so by the residue theorem,

$$
\begin{aligned}
u(x_0)=-\frac{1}{\pi}\lfbr{2\pi i\cdot\frac{1}{2i(i-x_0)}+\pi i\frac{1}{1+x_0^2} }=\frac{x_0}{1+x_0^2}
\end{aligned}
$$

(b)
Substituting,

$$
\begin{aligned}
\frac{1}{\pi}\dashint\frac{u(x)}{x-x_0}dx=\frac{1}{\pi}\dashint\frac{x}{(1+x^2)(x-x_0)}dx
\end{aligned}
$$

Find the poles with residues and use the residue theorem:

$$
\begin{aligned}
\frac{1}{\pi}\dashint\frac{u(x)}{x-x_0}dx  =\frac{1}{\pi}\lfbr{2\pi i\cdot\frac{i}{2i(i-x_0)}+\pi i\cdot\frac{x_0}{1+x_0^2} }=\frac{1}{1+x_0^2}
\end{aligned}
$$

(c)

$$
\begin{aligned}
f(z)|_{y=0}=u(x)+iv(x)=\frac{x}{1+x^2}-\frac{i}{1+x^2}=(x-i)^{-1}
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
f(z)=(z-i)^{-1}
\end{aligned}
$$

Since $\lim_{R\to\infty}z\cdot\frac{f(z)}{z-z_0}=0$, the semicircular part of the integral vanishes, so the conditions for the Hilbert transforms are satisfied.

(d)
$f(-x)=(-x-i)^{-1}\neq f^*(x)=(x+i)^{-1}$, so the crossing conditions are not satisfied.

-----

### 12.8.6

By the dispersion relations:

$$
\def\dint{{\int_0^\infty}\kern-18.0pt{-}}
\begin{aligned}
        \mathfrak{Re}\lfbr{n^2(\omega_0)-1 }& =k\\
        \mathfrak{Im}\lfbr{n^2(\omega_0)-1 }& =-\frac{2}{\pi}\dint\frac{\omega_0k}{\omega^2-\omega_0^2}d\omega\\
        & =-\frac{k}{\pi}\lim_{\delta\to0}\lfpr{\lfbr{\ln\frac{\omega_0-\omega}{\omega+\omega_0} }_0^{\omega_0-\delta}+\lfbr{\ln\frac{\omega-\omega_0}{\omega+\omega_0}}_{\omega_0+\delta}^\infty}\\
        & =-\frac{k}{\pi}\lim_{\delta\to0}\left(\ln\frac{2\omega_0+\delta}{2\omega_0-\delta}\right)\\
        & =0
\end{aligned}
$$

which means when the real part is constant, the imaginary part is zero.

(b)
It is just the converse of (a).

-----

### 12.8.7

$$
\begin{aligned}
\int\limits_{-\infty}^\infty |v(x)|^2dx=\int\limits_{-\infty}^\infty\frac{1}{(x^2+1)^2}dx
\end{aligned}
$$

The function has a second pole at $z=i$ with residue

$$
\begin{aligned}
residue=\lim_{z\to i}\frac{d}{dz}\lfbr{(z-i)^2\cdot\frac{1}{(z^2+1)^2} }=\frac{1}{4i}
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
\int\limits_{-\infty}^\infty|v(x)|^2dx=2\pi i\cdot\frac{1}{4i}=\frac{\pi}{2}
\end{aligned}
$$

Note that $\abs{u(x)}^2+\abs{v(x)}^2=\frac{1}{x^2+1}$, and

$$
\begin{aligned}
\int\limits_{-\infty}^\infty\frac{1}{x^2+1}dx=2\pi i\cdot\frac{1}{2i}=\pi
\end{aligned}
$$

so 

$$
\begin{aligned}
\int\limits_{-\infty}^\infty|u(x)|^2dx=\pi-\frac{\pi}{2}=\frac{\pi}{2}
\end{aligned}
$$

-----

### 12.8.8

(a)
Using the Hilbert transform:

$$
\begin{aligned}
        v(y)& =-\frac{1}{\pi}\dashint\frac{\delta(x)}{x-y}dx=\frac{1}{\pi y}\\
        \delta(w)& =\frac{1}{\pi}\dashint\frac{v(y)}{y-w}dy=\frac{1}{\pi^2}\dashint\frac{dy}{y(y-w)}
\end{aligned}
$$

(b)
Changing the variables $w=s-t$, $x=y+t$, so $y=x-t$, $y-w=x-s$, then the equation becomes

$$
\begin{aligned}
\delta(s-t)=\frac{1}{\pi^2}\dashint\frac{dx}{(x-t)(x-s)}
\end{aligned}
$$

{% endraw %}
