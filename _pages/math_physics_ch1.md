---
layout: archive
title: "Mathematical Methods for Physicists"
permalink: /solutions/math_physics_ch1
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

## Chapter 1: Mathematical Preliminaries

### 1.1.1
(a) 

If $A>0$, $\lim_{n\to \infty}n^p u_n=A$, so $$|n^p u_n-A|< \frac{A}{2}$$ when $$n\geq N$$ for some $$N$$. Then $$0<\frac{A}{2}\frac{1}{n^p}<u_n<\frac{3A}{2}\frac{1}{n^p}$$. $$\sum_{n=1}^{\infty}\frac{3A}{2}\frac{1}{n^p}$$ converges when $$p>1$$ by Cauchy integral test, so $$\sum_{n=1}^{\infty}u_n$$ converges by comparison test.

If $$A<0$$, then $$\lim_{n\to \infty}n^p(-u_n)=-A$$, $$-A>0$$. From above $$\sum_1^\infty(-u_n)$$ converges, so $$\sum_1^\infty(u_n)$$ converges.

If $$A=0$$, $$|n^p u_n|< 1$$ when $$n\geq N$$ for some N. Then $$-\frac{1}{n^p}<u_n<\frac{1}{n^p}$$, so $$|u_n|<\frac{1}{n^p}$$ for sufficiently large $$n$$. $$\sum_{n=1}^\infty \frac{1}{n^p}$$ converges by Cauchy integral test, so $$\sum_{n=1}^{\infty}u_n$$ converges by comparison test.
