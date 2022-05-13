---
layout: splash
title: "Principles of Mathematical Analysis Ch6"
permalink: /solutions/real_analysis_06
author_profile: false

---

# Chapter 6: The Riemenn-Stieltjes Integral

{% raw %}

### 1.

For every partition $P$, since there are points $
\newcommand{\lfpr}[1]{\left(#1\right)}
\newcommand{\lfbr}[1]{\left[#1\right]}
\def\upint{\int\limits^{-}\kern-11.9pt\int}
\def\upintt{\int\limits^{-}\kern-8.6pt\int}
\def\lowint{\int\limits_{-}\kern-11.1pt\int}
\def\lowintt{\int\limits_{-}\kern-7.8pt\int}
x_i\neq x_0$ in every interval of the partition, we have $L(P,f,\alpha)=\sum f(x_i)\Delta\alpha_i=0$, and therefore $\lowintt_a^bfd\alpha=0$.

For every $\varepsilon>0$, since $\alpha$ is continuous at $x_0$, there is a $\delta>0$ such that $\vert \alpha(x)-\alpha(x_0)\vert <\frac{\varepsilon}{2}$ for $\vert x-x_0\vert <\delta$. Let $I$ be the intersection of $[x_0-\delta,x_0-\delta]$ and $[a,b]$, and let its end points be $x_1,x_2$. Consider the partition $P=\{a,x_1,x_2,b\}$, then 

$$
\begin{aligned} 
U(P,f,\alpha)=f(x_0)\cdot[\alpha(x_2)-\alpha(x_1)]< 1\cdot\varepsilon=\varepsilon
\end{aligned}
$$

since $\varepsilon$ can be arbitrarily small, we have $\upintt_a^bfd\alpha=0$.

Therefore, $\lowintt_a^bfd\alpha=\upintt_a^bfd\alpha=\int_a^bfd\alpha=0$, and $f\in \mathscr R(\alpha)$.

-----

### 2.

Suppose $f\geq0$ and $f$ is continuous on $[a,b]$. If there is a $x_0\in[a,b]$ such that $f(x_0)>0$, then since $f$ is continuous, there is a $\delta>0$ such that for $\vert x-x_0\vert <\delta$, we have $\vert f(x)-f(x_0)\vert <\frac{f(x_0)}{2}$, which means $f(x)>\frac{f(x_0)}{2}$. Let $\eta=\min(\delta,\frac{b-a}{2})>0$. If $x_0\leq\frac{a+b}{2}$, then $f(x)>\frac{f(x_0)}{2}$ in the interval $[x_0,x_0+\eta]$; if $x_0>\frac{a+b}{2}$, then $f(x)>\frac{f(x_0)}{2}$ in the interval $[x_0-\eta,x_0]$. In both cases, for every partition $P$, we have $U(P,f)>\frac{f(x_0)}{2}\cdot\eta$, and therefore

$$
\begin{aligned} 
\int_a^bf(x)dx=\upint_a^bf(x)dx\geq\frac{f(x_0)}{2}\cdot\eta>0
\end{aligned}
$$

which is a contradiction. Therefore, $\int_a^bf(x)dx=0$ implies $f(x)=0$ for all $x\in[a,b]$.

-----

### 3.

If $f(0+)=f(0)$, then for every $\varepsilon>0$ there is a $\delta>0$ such that $\vert f(x)-f(0)\vert <\frac{\varepsilon}{2}$ for $x-0<\delta$. Consider the partition $P=\{-1,0,\delta,1\}$, then we have

$$
\begin{aligned} 
U(P,f,\beta_1)-L(P,f,\beta_1)<\lfbr{\frac{\varepsilon}{2}-\lfpr{-\frac{\varepsilon}{2}}}\cdot\lfbr{\beta_1(\delta)-\beta_1(0)}=\varepsilon
\end{aligned}
$$

which means $f\in\mathscr{\beta}_1$ from Theorem 6.6.

If $f\in\mathscr{\beta}_1$, then for every $\varepsilon>0$, there is a partition $P$ such that $U(P,f,\beta_1)-L(P,f,\beta_1)<\varepsilon$. Let $P^\star =P\cup\{0\}$ and $[0,\delta]$ be the corresponding interval of $P^\star $, and let $M$ and $m$ be the maximum and minimum of $f$ in $[0,\delta]$, then 

$$
\begin{aligned} 
U(P^\star ,f,\beta_1)-L(P^\star ,f,\beta_1)=M-m\leq U(P,f,\beta_1)-L(P,f,\beta_1)<\varepsilon
\end{aligned}
$$

Therefore, for $x\in[0,\delta]$ we have $\vert f(x)-f(0)\vert \leq M-m<\varepsilon$, which means $f(0+)=f(0)$.

When $\delta\to0$, we have $M\to f(0)$ and $m\to f(0)$, so $\lowintt f\,d\beta_1=\upintt f\,d\beta_1=\int f\,d\beta=f(0)$.


(b) _statement:_ $f\in\mathscr{R}(\beta_2)$ if and only if $f(0-)=f(0)$.

\textit{proof:} The proof is similar with (a) if we instead consider the interval $[-\delta,0]$.


(c) If $f$ is continuous at $0$, then for every $\varepsilon>0$ there is a $\delta>0$ such that $\vert f(x)-f(0)\vert <\frac{\varepsilon}{2}$ for $\vert x-0\vert <\delta$. Consider the partition $P=\{-1,-\delta,\delta,1\}$, then we have

$$
\begin{aligned} 
U(P,f,\beta_3)-L(P,f,\beta_3)<\lfbr{\frac{\varepsilon}{2}-\lfpr{\frac{\varepsilon}{2}}}\cdot\lfbr{\beta_3(\delta)-\beta_3(-\delta)}=\varepsilon
\end{aligned}
$$

which means $P\in\mathscr{R}(\beta_3)$ from Theorem 6.6.

If $f\in\mathscr{R}(\beta_3)$, then for every $\varepsilon>0$ there is a partition $P$ such that $U(P,f,\beta_3)-L(P,f,\beta_3)<\frac{\varepsilon}{2}$. Let $P^\star =P\cup\{0\}$, and let $[-\delta_1,0]$ and $[0,\delta_2]$ be the corresponding intervals of $P^\star $. Let $(M_1,m_1)$ and $(M_2,m_2)$ be the maximum and minimum of the two intervals, respectively, then we have

$$
\begin{aligned} 
U(P^\star ,f,\beta_3)-L(P^\star ,f,\beta_3)=(M_1-m_1)\frac{1}{2}+(M_2-m_2)\frac{1}{2}\leq U(P,f,\beta_3)-L(P,f,\beta_3)
<\frac{\varepsilon}{2}\end{aligned}
$$

Let $\delta=\min(\delta_1,\delta_2)$, then for $x\in[-\delta,0]$ we have $\vert f(x)-f(0)\vert \leq M_1-m_1<\varepsilon$, and for $x\in[0,\delta]$ we have $\vert f(x)-f(0)\vert \leq M_2-m_2<\varepsilon$. Therefore, $\vert f(x)-f(0)\vert <\varepsilon$ for all $\vert x-0\vert <\delta$, which means $f$ is continuous at $0$.


(d) If $f$ is continuous at $0$, which means $f(0-)=f(0+)=f(0)$, then from (a) $\sim$ (c) we have 

$$
\begin{aligned} 
\int f\,d\beta_1=\int f\,d\beta_2=\int f\,d\beta_3=f(0)
\end{aligned}
$$

-----

### 4.

In every interval of every partition there are rational and irrational numbers, so 

$$
\begin{aligned} 
U(P,f)-L(P,f)=1\cdot(b-a)-0\cdot(b-a)=b-a>0
\end{aligned}
$$

which means $f\not\in\mathscr{R}$ by Theorem 6.6.

-----

### 5.

_$f^2\in\mathscr{R}$ does not imply $f\in\mathscr{R}$._ Let $f(x)=1$ if $x$ is rational and $f(x)=-1$ if $x$ is irrational, then $f^2\in\mathscr{R}$ on $[a,b]$ while $f\not\in\mathscr{R}$.

_$f^3\in\mathscr{R}$ implies $f\in\mathscr{R}$._ Let $h(x)=\sqrt[3]{x}$, then $f^3\in\mathscr{R}$ on $[a,b]$ and $h\in\mathscr{R}$ on $[-\infty,\infty]$ imply $f=h\circ f^3\in\mathscr{R}$ by Theorem 6.11.

-----

### 6.

For every $\varepsilon>0$, we can cover the Cantor set by finitely many disjoint intervals $[u_j,v_j]$ such that the total length is less than $\frac{\varepsilon}{1+2M}$, where $M=\sup\vert f(x)\vert $, and in such a way that every point of $P$ lies in the interior of some $[u_j,v_j]$. Removing the segments $(u_j,v_j)$ from $[0,1]$, then the remaining set $K$ is compact, and therefore $f$ is uniformly continuous on $K$ by Theorem 4.19, so there exists $\delta>0$ such that $\vert f(s)-f(t)\vert <\frac{\varepsilon}{1+2M}$ for $s\in K$, $t\in K$, $\vert s-t\vert <\delta$. Form a partition $\mathcal{P}$ as follows: each $u_j$ and $v_j$ occur in $\mathcal{P}$. No point of any segment $(u_j,v_j)$ occurs in $\mathcal{P}$. If $x_{i-1}$ is not one of the $u_j$, then $\Delta x_i<\delta$. So every interval of $\mathcal{P}$ is either $[u_j,v_j]$ or having a length less than $\delta$. Therefore,

$$
\begin{aligned} 
U(\mathcal{P},f)-L(\mathcal{P},f)\leq 2M\cdot\frac{\varepsilon}{1+2M}+1\cdot\frac{\varepsilon}{1+2M}=\varepsilon
\end{aligned}
$$

which means $f\in\mathscr{R}$.


{% endraw %}
