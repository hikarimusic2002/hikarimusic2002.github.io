---
layout: splash
title: "Mathematical Methods for Physicists"
permalink: /solutions/math_physics_ch1
author_profile: false
redirect_from:
  - /resume
---

## Chapter 1: Mathematical Preliminaries

### 1.1.1
(a) 

  If $A>0$, $\lim_{n\to \infty}n^p u_n=A$, so $$\vert n^p u_n-A\vert < \frac{A}{2}$$ when $$n\geq N$$ for some $$N$$. Then $$0<\frac{A}{2}\frac{1}{n^p}<u_n<\frac{3A}{2}\frac{1}{n^p}$$. $$\sum_{n=1}^{\infty}\frac{3A}{2}\frac{1}{n^p}$$ converges when $$p>1$$ by Cauchy integral test, so $$\sum_{n=1}^{\infty}u_n$$ converges by comparison test.

  If $$A<0$$, then $$\lim_{n\to \infty}n^p(-u_n)=-A$$, $$-A>0$$. From above $$\sum_1^\infty(-u_n)$$ converges, so $$\sum_1^\infty(u_n)$$ converges.

  If $$A=0$$, $$\vert n^p u_n\vert < 1$$ when $$n\geq N$$ for some N. Then $$-\frac{1}{n^p}<u_n<\frac{1}{n^p}$$, so $$\vert u_n \vert <\frac{1}{n^p}$$ for sufficiently large $$n$$. $$\sum_{n=1}^\infty \frac{1}{n^p}$$ converges by Cauchy integral test, so $$\sum_{n=1}^{\infty}u_n$$ converges by comparison test.
  
### 1.1.2
Let $b_n'=\frac{b_n}{2K}$, then $\lim_{n\to\infty}\frac{b_n'}{a_n}=\frac{1}{2}$, so for sufficiently large n, $\frac{1}{2}-\frac{1}{2}=0<\frac{b_n'}{a_n}<1=\frac{1}{2}+\frac{1}{2}$. Then $0<b_n'<a_n$ or $0>b_n'>a_n$, so $\sum a_n$ converges implies $\sum b_n'$ converges by comparison test, and therefore $\sum b_n$ converges.

Let $b_n''=\frac{2b_n}{KK}$, then $\lim_{n\to\infty}\frac{b_n''}{a_n}=2$, so for sufficiently large n $2+1=3>\frac{b_n''}{a_n}>1=2-1$.Then $3a_n>b_n''>a_n$ or $3a_n<b_n''<a_n$,  so $\sum a_n$ diverges implies $\sum b_n''$ diverges by comparison test, and therefore $\sum b_n$ diverges.

