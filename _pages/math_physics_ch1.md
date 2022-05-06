---
layout: archive
title: "Chapter 1: Mathematical Preliminaries"
permalink: /solutions/math_physics_ch1
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

(a) If $A>0$, $\lim_{n\to \infty}n^p u_n=A$, so $|n^p u_n-A|< \frac{A}{2}$ when $n\geq N$ for some N. Then $0<\frac{A}{2}\frac{1}{n^p}<u_n<\frac{3A}{2}\frac{1}{n^p}$. $\sum_{n=1}^{\infty}\frac{3A}{2}\frac{1}{n^p}$ converges when $p>1$ by Cauchy integral test, so $\sum_{n=1}^{\infty}u_n$ converges by comparison test.
