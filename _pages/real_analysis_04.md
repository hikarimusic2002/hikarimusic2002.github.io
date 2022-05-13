---
layout: splash
title: "Principles of Mathematical Analysis Ch4"
permalink: /solutions/real_analysis_04
author_profile: false

---

# Chapter 4: Continuity

{% raw %}

### 1.
$f$ satisfying the condition is not necessary continuous. Consider the function

$$
\newcommand{\V}{\mathbf}
\newcommand{\diam}[1]{\mathrm{diam}\,#1}\begin{aligned}
f(x)=
\begin{cases}
1,\quad \textit{if x=0}\\
0,\quad otherwise
\end{cases}
\end{aligned}
$$

then $\lim_{h\to 0}[f(x+h)-f(x-h)]=0$ for every $x$, while $f$ is not continuous at $x=0$.

-----

### 2

Let $q\in f(\overline{E})$, so there is a $p\in\overline{E}$ such that $f(p)=q$. Consider the neighborhood of $q$: $$\begin{aligned}N_\varepsilon=\{y\in Y\vert \,d_Y(y,q)<\varepsilon \}\end{aligned}$$
Since $f$ is continuous, there is a $\delta>0$ such that 

$$
\begin{aligned}
x\in N_{\delta}=\{x\in X\vert \,d_X(x,p)<\delta\}
\end{aligned}
$$

 implies $f(x)\in N_\varepsilon$. Since $p$ is a point or a limit point of $E$, there is a point of $E$ contained in $N_\delta$, and therefore there is a point of $f(E)$ contained in $N_\varepsilon$. So every neighborhood of $q$ contains a point of $f(E)$, which means $q\in\overline{f(E)}$. Therefore, $f(\overline{E})\subset\overline{f(E)}$.

Let $f$ be a mapping from $X=(0,1)$ to $Y=R$, such that 

$$
\begin{aligned}
f(x)=x
\end{aligned}
$$

Let $E=X$. Since $\overline{E}=E$ in $X$, we have

$$
\begin{aligned}
f(\overline{E})&=f(E)=(0,1)\\
\overline{f(E)}&=\overline{(0,1)}=[0,1]
\end{aligned}
$$

so $f(\overline{E})$ is a proper subset of $\overline{f(E)}$.

-----

### 3.

$\{0\}$ is closed in $R$, so by Corollary of Theorem 4.8, $Z(f)=f^{-1}(\{0\})$ is closed in $X$, since $f$ is continuous.

-----

### 4.

$E$ is dense in $X$, so $\overline{E}=X$. From Exercise 2, $f(X)=f(\overline{E})\subset\overline{f(E)}$, so every point of $f(X)$ is a point or a limit point of $f(E)$, which means $f(E)$ is dense in $f(X)$.

Let $p\in X$. Since $E$ is dense in $X$, there is a sequence $\{p_n\}\to p$ where $p_n\in E$ for each $n$, so $g(p_n)=f(p_n)$. Since $g$ and $f$ are continuous,

$$
\begin{aligned}
g(p)=\lim_{n\to\infty}g(p_n)=\lim_{n\to\infty}f(p_n)=f(p)
\end{aligned}
$$

so $g(p)=f(p)$ for all $p\in X$.

-----

### 5.

The complement of $E$ is open, so by Exercise 2.29, it is the union of an at most countable collection of disjoint segments. Let $E^c=\bigcup_i(a_i,b_i)$. Let $g_i$ be a real function on $(a_i,b_i)$. If $a_i=\infty$ or $-\infty$, let $g_i(x)=f(b_i)$. If $b_i=\infty$ or $-\infty$, let $g_i(x)=f(a_i)$. If both $a_i$ and $b_i$ are finite, let $g_i$ be that

$$
\begin{aligned}
g_i(x)=\frac{f(b_i)-f(a_i)}{b_i-a_i}(x-a_i)+f(a_i)
\end{aligned}
$$

so $g_i(x)$ is a linear function $g_i(x)=m_ix+k_i$ where $g_i(a_i)=f(a_i)$ and $g_i(b_i)=f(b_i)$. Let $g$ be a real function on $R^1$ such that

$$
\begin{aligned}
g(x)=\begin{cases}
f(x),\quad & \textit{if $x\in E$}\\
g_i(x),\quad & \textit{if $x\in(a_i,b_i)\in E^c$}
\end{cases}
\end{aligned}
$$

$g$ is continuous at every point except those $a_i$ and $b_i$ since $f(x)$ and $g_i(x)$ are continuous. At $a_i$, for every $\varepsilon>0$, there is a $\delta_1>0$ such that $\vert x-a_i\vert <\delta_1$ implies $\vert f(x_i)-f(a_i)\vert <\varepsilon$. Let $\delta_2=0$ if $g_i(x)=f(a_i)$, or $\delta_2=\frac{\varepsilon}{\vert m\vert }$ otherwise. Let $\delta=\max(\delta_1,\delta_2)$. For $\vert x-a_i\vert <\delta$, 

$$
\begin{aligned}
\vert g(x)-g(a_i)\vert <\varepsilon
\end{aligned}
$$

so $g$ is continuous at $a_i$. Similarly $g$ is continuous at $b_i$. So $g$ is a continuous real function on $R^1$ such that $g(x)=f(x)$ for all $x\in E$.


Let $f$ be a real continuous function defined on $E=(0,1)$ such that $f(x)=\frac{1}{x}$. Note that $E$ is open. The extension $g$ of $f$ cannot be continuous at $0$ whatever value $g(0)$ is assigned since $\lim_{x\to0}f(x)=\infty\neq g(0)$.


Let $\mathbf{f}=(f_1,f_2,\cdot,f_n)$ be a vector-valued continuous function defined on a closed set $E\subset R^1$. By Theorem 4.10, each $f_k$ is continuous, so there exist continuous function $g_k$ on $R^1$ such that $g_k(x)=f_k(x)$ for all $x\in E$. Let $\mathbf{g}=(g_1,g_2,\cdot,g_n)$, then by Theorem 4.10, $\mathbf{g}$ is a continuous function on $R^1$ such that $\mathbf{g}(x)=\mathbf{f}(x)$ for all $x\in E$.

-----

### 6.

If $f$ is continuous on $E$, let $\phi$ be a function from $E\in R^1$ to $R^2$ such that 

$$
\begin{aligned}
\phi(x)=(x,f(x))
\end{aligned}
$$

then the graph of $f$ is $\phi(E)$. Since both the functions  $\phi_1(x)=x$ and $\phi_2(x)=f(x)$ are continuous, $\phi$ is continuous by Theorem 4.10. Since $E$ is compact, $\phi(E)$ is compact by Theorem 4.14.


If $f$ is not continuous at some point $p$, then there is a sequence $\{p_n\}$ in $E$ such that $\{p_n\}$ converges to $p$, but $\{f(p_n)\}$ does not converge to $f(p)$. Consider the sequence $\{q_n\}$ in $\phi(E)$ such that $q_n=(p_n,f(p_n))$. If a subsequence $\{q_{n_k}\}$ converges to $(a,b)$, then $\{p_{n_k}\}\to a$ and $\{f(p_{n_k})\}\to b$. Since $\{p_n\}$ converges to $p$, $a=p$, but since $\{f(p_n)\}$ does not converge to $f(p)$, $b\neq f(p)$,* so $(a,b)\not\in \phi(E)$. Therefore, there is no subsequence of $\{q_n\}$ in $\phi(E)$ converges to a point of $\phi(E)$, which means $\phi(E)$ is not compact by Theorem 3.6. 

-----

### 7.

$(\vert x\vert -y^2)^2\geq0$, so $x^2+y^4\geq2\vert x\vert y^2$, and

$$
\begin{aligned}
\vert f(x,y)\vert =\frac{\vert xy^2\vert }{\vert x^2+y^4\vert }\leq\frac{\vert xy^2\vert }{2\vert xy^2\vert }=\frac{1}{2}
\end{aligned}
$$

so $f(x,y)$ is bounded by $\frac{1}{2}$.


Let $x=y^3$, then

$$
\begin{aligned}
g(x,y)=\frac{y^3\cdot y^2}{y^6+y^6}=\frac{1}{2y}
\end{aligned}
$$

since $\frac{1}{2y}\to\infty$ as $y\to0$, $g(x,y)$ is unbounded in every neighborhood of $(0,0)$.


Let $x=y^2$, then

$$
\begin{aligned}
f(x,y)=\frac{y^2\cdot y^2}{y^4+y^4}=\frac{1}{2}
\end{aligned}
$$

For $\varepsilon<\frac{1}{2}$, in every neighborhood $\vert (x,y)-(0,0)\vert <\delta$ there is a point $(a^2,a)$ such that $\vert f(a^2,a)-f(0,0)\vert =\frac{1}{2}>\varepsilon$, so $f$ is not continuous at $(0,0)$.


If $f(x,y)$ and $g(x,y)$ are restricted to a straight line not passing $(0,0)$, then the denominators of $f(x,y)$ and $g(x,y)$ are not zero, which implies that they are continuous by Theorem 4.9. If $f(x,y)$ and $g(x,y)$ are restricted to a straight line $y=mx$ passing $(0,0)$, then

$$
\begin{aligned}
f(x,y)&=\frac{x\cdot m^2x^2}{x^2+m^4x^4}=\frac{m^2x}{1+m^4x^2}\\
g(x,y)&=\frac{x\cdot m^2x^2}{x^2+m^6x^6}=\frac{m^2x}{1+m^6x^4}
\end{aligned}
$$

both the denominators of which are not zero, so they are continuous by Theorem 4.9.

-----

### 8.

Let $x$ be a limit point of $E$, so there is a sequence $\{x_n\}$ in $E$ such that $\{x_n\}\to x$. For $\varepsilon>0$, there is a $\delta>0$ such that $\vert p-q\vert <\delta$ implies $\vert f(p)-f(q)\vert <\varepsilon$, since $f$ is uniformly continuous; for $\delta>0$, there is a positive integer $N$ such that $m,n\geq N$ implies $\vert x_n-x_m\vert <\delta$, since $\{x_n\}$ converges and is therefore a Cauchy sequence. Therefore, for $\varepsilon>0$ there is a positive integer $N$ such that $m,n\geq N$ implies $\vert f(x_n)-f(x_m)\vert <\varepsilon$, which means $\{f(x_n)\}$ is a Cauchy sequence. Since every Cauchy sequence in $R^1$ converges, $\{f(x_n)\}$ converges to a point $y$, where $y=y(x)$ depends on $x$. Let $F$ be a function on $\overline{E}$ to $R^1$ such that

$$
\begin{aligned}
F(x)=\begin{cases}
f(x),\quad & \textit{if $x\in E$}\\
y(x),\quad & \textit{if $x\in \overline{E}\setminus E$}
\end{cases}
\end{aligned}
$$

By the construction of $y$, $F$ is continuous. Since $\overline{E}$ is closed and bounded, it is compact, so $F(\overline{E})$ is compact and therefore bounded by Theorem 4.14. Note that $f(E)=F(E)\subset F(\overline{E})$, so $f(E)$ is bounded.


Let $f(x)=x$ be a function from $E=R^1$ to $R^1$. It is uniformly continuous if we let $\delta=\varepsilon$, since $\vert f(x)-f(y)\vert =\vert x-y\vert <\delta=\varepsilon$. But $E$ is not bounded. $f(E)=f(R^1)=R^1$ is not bounded.

-----

### 9.

If $f$ is a uniformly continuous function from $X$ to $Y$, then for every $\varepsilon>0$, there is a $\delta>0$ such that $d_X(p,q)<\delta$ implies $d_Y(f(p),f(q))<\varepsilon$. If $E\subset X$ and $\mathrm{diam}\,E<\delta$, then for $p,q\in E$, we have $d_X(p,q)\leq\mathrm{diam}\,E<\delta$, and therefore $d_Y(f(p),f(q))<\varepsilon$. Since $\mathrm{diam}\,f(E)=\sup d_Y(f(p),f(q))$ for $f(p),f(q)\in E$, we have $\mathrm{diam}\,f(E)<\varepsilon$.


If for every $\varepsilon>0$ there exists a $\delta>0$ such that $\mathrm{diam}\,E<\delta$ implies $\mathrm{diam}\,f(E)<\varepsilon$, then for every $d_X(p,q)<\delta$, let $E=\{p,q\}$, then $\mathrm{diam}\,E=d_X(p,q)<\delta$, and therefore $d_Y(f(p),f(q))=\mathrm{diam}\,f(E)<\varepsilon$, which means $f$ is uniformly continuous.

-----

### 10.

Let $f$ be a continuous mapping of a compact metric space $X$ into a metric space $Y$. Suppose $f$ is not uniformly continuous, then for some $\varepsilon>0$ there are sequences $\{p_n\},\{q_n\}$ in $X$ such that $d_X(p_n,q_n)\to0$ but $d_Y(f(p_n),f(q_n))>\varepsilon$ for every $n$. By Theorem 3.6, a subsequence $\{p_{n_i}\}$ of $\{p_n\}$ converges to a point $p\in X$, and a subsequence $\{q_{n_{i_j}}\}=\{q_{n_k}\}$ of $\{q_{n_i}\}$ converges to a point $q\in X$. So $\{p_{n_k}\}\to p$ and $\{q_{n_k}\}\to q$, but note that $d_X(p_n,q_n)\to0$, so $p=  q$. Since $f$ is continuous, we have $\{f(p_{n_k})\}\to f(p)$ and $\{f(q_{n_k})\}\to f(q)$, while $f(p)=f(q)$, so $d_Y(f(p_{n_k}),f(q_{n_k}))\to0$, contradicting with $d_Y(f(p_n),f(q_n))>\varepsilon$. So $f$ is uniformly continuous. 

-----

### 11.

Suppose $f$ is a uniformly continuous mapping from $X$ to $Y$, and $\{x_n\}$ is a Cauchy sequence in $X$. For every $\varepsilon>0$, there is a $\delta>0$ such that $d_X(p,q)<\delta$ implies $d_Y(f(p),f(q))<\varepsilon$; for $\delta>0$, there is a positive integer $N$ such that $m,n\geq N$ implies $d_X(x_m,x_n)<\delta$, and therefore $d_Y(f(x_m),f(x_n))<\varepsilon$. So $\{f(x_n)\}$ is a Cauchy sequence in $Y$.


(Exercise 13) For each $x\in X$, let $\{x_n\}$ be a sequence in $E$ such that $\{x_n\}\to x$ (the sequence exists since $E$ is dense in $X$). Since $\{x_n\}$ is a Cauchy sequence, $\{f(x_n)\}$ is also a Cauchy sequence and therefore converges, since $\{f(x_n)\}$ is in $R^1$. Let the limit be $F(x)$.

$F$ is a function defined on $X$, and $F(x)=f(x)$ for $x\in E$ since $f$ is continuous on $E$. So $F$ is an extension of $f$ from $E$ to $X$. For every $\varepsilon>0$, there is a $\delta>0$ such that $p,q\in E$ and $d(p,q)<\delta$ implies $d(f(p),f(q))<\frac{\varepsilon}{3}$. For $x,y\in X$ and $d(x,y)<\delta$, let $N$ be a positive integer such that $d(f(x_N),F(x))<\frac{\varepsilon}{3}$ and $d(x_N,x)<\frac{\delta-d(x,y)}{2}$; let $M$ be a positive integer such that $d(f(y_M),F(y))<\frac{\varepsilon}{3}$ and $d(y_N,y)<\frac{\delta-d(x,y)}{2}$. Let $p=x_N$ and $q=y_M$. Then we have

$$
\begin{aligned}
d(p,q)\leq d(p,x)+d(x,y)+d(y,q)<\frac{\delta-d(x,y)}{2}+d(x,y)+\frac{\delta-d(x,y)}{2}=\delta
\end{aligned}
$$

and therefore

$$
\begin{aligned}
d(F(x),F(y))\leq d(F(x),F(p))+d(F(p),F(q))+d(F(q),F(y))<\frac{\varepsilon}{3}+\frac{\varepsilon}{3}+\frac{\varepsilon}{3}=\varepsilon
\end{aligned}
$$

Therefore, for every $\varepsilon>0$ there is a $\delta>0$ such that $x,y\in X$ and $d(x,y)<\delta$ implies $d(F(x),F(y))<\varepsilon$, which means $F$ is a uniformly continuous extension of $f$ from $E$ to $X$.

-----

### 12.

_restate:_  If $f$ is a uniformly continuous function from $X$ to $Y$, and $g$ is a uniformly function form $f(X)\subset Y$ to $Z$, then the composition $h=g\circ f$ is a uniformly continuous function from $X$ to $Z$.


_proof:_ For $\varepsilon>0$, there is a $\eta>0$ such that $d_Y(x,y)<\eta$ implies $d_Z(g(x),g(y))<\varepsilon$; for $\eta>0$, there is a $\delta>0$ such that $d_X(p,q)<\delta$ implies $d_Y(f(p),f(q))<\eta$. Therefore, for $\varepsilon>0$, there is a $\delta>0$ such that $d_X(p,q)<\delta$ implies $d_Z(g(f(p)),g(f(q)))<\varepsilon$, which means $g\circ f$ is uniformly continuous. 

-----

### 13.

For each $p\in X$ and each positive integer $n$, let $V_n(p)$ be the set of all $q\in E$ with $d(p,q)<\frac{1}{n}$. For every $n$, $V_n(p)$ is nonempty since $E$ is dense in $X$, so $f(V_n(p))$ is nonepmty for every $n$. For $\varepsilon>0$, there is a $\delta>0$ such that $E\subset X$ with $\diam{E}<\delta$ implies $\diam{f(E)}<\varepsilon$; for $\delta>0$, let $N$ be the positive integer such that $\frac{1}{N}<\delta$, then $\diam{V_n(p)}<\delta$ for $n\geq N$. Therefore, for $\varepsilon>0$ there is a positive integer $N$ such that $n\geq N$ implies $\diam{f(V_n(p))}<\varepsilon$, which means $\diam{f(V_n(p))}\to0$. Let $M$ be the positive integer such that $\diam{f(V_n(p))}<1$ for $n\geq M$. Then $\overline{f(V_M(p))},\overline{f(V_{M+1}(p))},\overline{f(V_{M+2}(p))},\cdots$ are closed and bounded, so they are compact. From Theorem 3.10, $\overline{f(V_M(p))}\supset\overline{f(V_{M+1}(p))}\supset\cdots$ and $\diam{\overline{f(V_n(p))}}\to0$ implies there is exactly one point contained in every $\overline{f(V_n(p))}$, let it be $g(p)$.


$g$ is a function defined on $X$, and for $x\in E$, $g(x)=f(x)$, so $g$ is an extension of $f$ from $E$ to $X$. For every $\varepsilon>0$, there is a $\delta>0$ such that $p,q\in E$ and $d(p,q)<\delta$ implies $d(f(p),f(q))<\frac{\varepsilon}{3}$. For $x,y\in X$ such that $d(x,y)<\delta$, let $N,M$ be positive integers such that $\overline{f(V_N(x))}<\frac{\varepsilon}{3}$ and $\overline{f(V_M(y))}<\frac{\varepsilon}{3}$. Let $p$ be an element of $E$ such that $d(p,x)<\min(\frac{1}{N},\frac{\delta-d(x,y)}{2})$, and let $q$ be an element of $E$ such that $d(p,y)<\min(\frac{1}{M},\frac{\delta-d(x,y)}{2})$ ($p,q$ exist because $E$ is dense in $X$). Then we have

$$
\begin{aligned}
d(p,q)\leq d(p,x)+d(x,y)+d(y,q)<\frac{\delta-d(x,y)}{2}+d(x,y)+\frac{\delta-d(x,y)}{2}=\delta
\end{aligned}
$$

and therefore

$$
\begin{aligned}
d(g(x),g(y))\leq d(g(x),g(p))+d(g(p),g(q))+d(g(q),g(y))<\frac{\varepsilon}{3}+\frac{\varepsilon}{3}+\frac{\varepsilon}{3}=\varepsilon
\end{aligned}
$$

Therefore, for every $\varepsilon>0$ there is a $\delta>0$ such that $x,y\in X$ and $d(x,y)<\delta$ implies $d(g(x),g(y))<\varepsilon$, so $g$ is a uniformly continuous extension of $f$ from $E$ to $X$.


The range space can be replaced by $R^k$, compact spaces or complete metric spaces, since by Exercise 3.21, the existence and uniqueness of $g(p)$ so constructed does not change, and the rest of the proof holds in every metric space.

The consequence may not hold if the range space is incomplete. For example, let $E=Q$, the rational numbers which is dense in $R$, and let $f(x)=x$ be a function from $Q$ to $Q$, which is uniformly continuous. If $f$ has a continuous extension from $Q$ to $R$, then the extension $F_1$ is a function from $R$ to $Q$ such that $F_1(x)=x$ for $x\in Q$. Let $F_2$ be the identity function $F_2(x)=x$ from $R$ to $R$. We have $F_1(p)=F_2(p)$ for $p\in Q$, while if $q\in R\setminus Q$, then $F_1(q)\in Q$ but $F_2(q)\in R\setminus Q$, so $F_1(q)\neq F_2(q)$, a contradiction to Exercise 4. Therefore, $f$ does not have a continuous extension from $Q$ to $R$.

-----

### 14.

If $f(0)=0$ or $f(1)=1$, then we are done, so supposed $f(0)>0$ and $f(1)< 1$. Let $g(x)=f(x)-x$, which is continuous since $f(x)$ is continuous. $g(0)=f(0)-0>0$, and $g(1)=f(1)-1<0$, so by Theorem 4.23, there is a point $p\in(0,1)$ such that $g(p)=0$. Then $f(p)=p$.

-----

### 15.

Let $f$ be a continuous mapping of $R^1$ into $R^1$. If it is not monotonic, then there are $a<b<c$ such that $f(a)<f(b)$ and $f(b)>f(c)$, or $f(a)>f(b)$ and $f(b)<f(c)$. Consider the first case only, since the second case can be proved similarly. The interval $I=[a,c]$ is compact, so $f(I)$ is compact, and therefore $\sup f(I)$ exists and $\sup f(I)\in f(I)$. Let $u$ be the point in $[a,c]$ such that $f(u)=\sup f(I)$. Since $f(a),f(c)<f(b)\leq f(u)$, $u\neq a,b$, so $u\in (a,b)$. Consider the segment $S=(a,b)$ which is open. $f(u)\in f(S)$ while it is not an interior point of $f(S)$, since every neighborhood $N_\varepsilon(f(u))$ contains a point $p$ such that $f(u)<p<f(u)+\varepsilon$, which is not in $f(S)$. So $f(S)$ is not open, which means $f$ is not an open mapping. Therefore, every continuous open mapping of $R^1$ into $R^1$ is monotonic.

-----

### 16.

Let $f(x)=[x]$ and $g(x)=(x)$. Both the functions are continuous on segments $(n,n+1)$, where $n$ is an integer. At $x=n$, $f(n-)=n-1$, $f(n+)=n$, $g(n-)=1$, $g(n+)=0$, so both the functions have simple discontinuity at integer points.

-----

### 17.

For $f(x-)<f(x+)$, a rational number $p$ such that $f(x-)<p<f(x+)$ exists by Theorem 1.20. If for every $\delta>0$, there is a $t$ such that $x-\delta<t<x$ and $f(t)\geq p$, let $t_n$ be that $t$ when $\delta=\frac{1}{n}$, then $\{t_n\}\to x$, but $\{f(t_n)\}$ either diverges or converges to $q\geq p$, a contradiction to the definition of $f(x-)<p$. Therefore, there is a $\delta>0$ such that $x-\delta<t<x$ implies $f(t)<p$. Let $q$ be a rational number in $(a,b)$ such that $x-\delta<q<x$, then $q<t<x$ implies $f(t)<p$. Similarly, we can find a rational number $r$ in $(a,b)$ such that $x<t<r$ implies $f(t)>p$.

If there are two points $x_1<x_2$ of $E$ associated to the same $(p,q,r)$, let $t$ be a point such that $x_1<t<x_2$, then $x_1<t<r$ so $f(t)>p$, but $q<t<x_2$ so $f(t)<p$, a contradiction, which means at most one point of $E$ is associated with each triple $(p,q,r)$. So the set of simple discontinuity such that $f(x-)<f(x+)$ is countable. Similar is for the case of $f(x-)>f(x+)$.

Let $p$ be the set of points on which $f(x-)=f(x+)<f(x)$. With each point $x$ of $E$, associate a triple $(p,q,r)$ of rational numbers such that $f(x-)=f(x+)<p<f(x)$, and $a<q<t<x$ or $x<t<r<b$ implies $f(t)<p$. If there are two points $x_1<x_2$ of $P$ associated to the same $(p,q,r)$, then $q<x_1<x_2$ implies $f(x_1)<p$, but $f(x_1)>p$, a contradiction, which means at most one point of $P$ is associated with each triple $(p,q,r)$. So the set of simple discontinuity such that $f(x-)=f(x+)<f(x)$ is countable. Similar is for the case of $f(x-)=f(x+)>f(x)$.

Therefore, the set of points at which $f$ has a simple discontinuity is at most countable.

-----

### 18.

Let $x$ be a point in $R^1$. For every $\varepsilon>0$, let $N$ be the positive integer such that $N\leq\frac{1}{\varepsilon}<N+1$. For $1\leq n\leq N$, let $M_n$ be the integer such that $\frac{M_n}{n}\leq x\leq \frac{M_n+1}{n}$. If $x=\frac{M_n}{n}$, let $\delta_n=\frac{1}{n}$, otherwise let $\delta_n=\min(x-\frac{M_n}{n},\frac{M_n+1}{n}-x)$. Let $\delta=\min(\delta_1,\delta_2,\cdots,\delta_N)$, so there is no rational number $\frac{m}{n}$ other than $x$ with $n\leq N$ be contained the neighborhood of $x$ with radius $\delta$. For every $t$ such that $0<\vert t-x\vert <\delta$, if $t$ is irrational, then $\vert f(t)-0\vert =\vert 0-0\vert <\varepsilon$; if $t$ is rational so $t=\frac{m}{n}$, then by the construction of $\delta$ we have $n>N$, so $\vert f(t)-0\vert =\vert \frac{1}{n}-0\vert \leq\frac{1}{N+1}<\varepsilon$. Therefore, for each $\varepsilon>0$ there is a $\delta>0$ such that $0<\vert t-x\vert <\delta$ implies $\vert f(t)-0\vert <\varepsilon$, which means $\lim_{t\to x}f(t)=0$. If $x$ is irrational, then $\lim_{t\to x}f(t)=f(x)=0$, so $f$ is continuous at $x$; if $x$ is rational, then $f(x+)=f(x-)=\lim_{t\to x}f(t)=0\neq f(x)$, so $f$ has a simple discontinuity at $x$.

-----

### 19.

Suppose $f$ is a real function with domain $R^1$ which has the intermediate value property. If $f$ is not continuous at a point $x_0$, then there is a sequence $\{p_n\}$ such that $\{p_n\}\to x_0$ but $\{f(p_n)\}$ does not converge to $f(x_0)$. Either the set of $p_n$ such that $f(p_n)>f(x_0)$ or the set of $p_n$ such that $f(p_n)<f(x_0)$ are infinite. Consider the first case only since the second case can be proved similarly. Let $\{x_n\}$ be the subsequence of $\{p_n\}$ such that $f(x_n)>f(x_0)$ for every $n$. $\{f(x_n)\}$ does not converge to $f(x_0)$, so there is a $r'$ such that $f(x_n)>r'>f(x_0)$ for every $n$. Let $r$ be a rational number such that $r'>r>f(x_0)$. Let $t_n$ be the point such that $x_0<t_n<x_n$ and $f(t_n)=r$. $x_0$ is a limit point of the set of $t_n$, which is a subset of $E=\{x\,\vert \,f(x)=r\}$, so $x_0$ is a limit point of $E$. But $f(x_0)\neq r$, so $x_0\not\in E$, which means $E$ is not closed. Therefore, if $f$ is a real function with domain $R^1$ which has the intermediate value property, and for every rational $r$, the set of all $x$ with $f(x)=r$ is closed, then $f$ is continuous.

-----

### 20.

(a) $\rho_E(x)=\inf_{z\in E}d(x,z)=0$ if and only if for every $\varepsilon>0$ there is a $z\in E$ such that $d(x,z)<E$, which is equivalent to $x\in\overline{E}$.

(b) $\rho_E(x)\leq d(x,z)\leq d(x,y)+d(y,z)$ for all $z$, so $\rho_E(x)-d(x,y)\leq d(y,z)$ for all $z$, which means $\rho_E(x)-d(x,y)\leq\rho_E(y)$. Interchanging $x$ and $y$, we have $\vert \rho_E(x)-\rho_E(y)\vert \leq d(x,y)$. For every $\varepsilon>0$, let $\delta=\varepsilon$, then $d(x,y)<\delta$ implies $\vert \rho_E(x)-\rho_E(y)\vert <\varepsilon$, which means $\rho_E$ is a uniformly continuous function.

-----

### 21.

$K$ is compact and $\rho_F$ is continuous, so $\rho_F(K)$ is compact by Theorem 4.14. So $\inf\rho_F(K)\in\rho_F(K)$, which means there is a $u\in K$ such that $\rho_F(u)=\inf \rho_F(K)$. If $\rho_F(u)=0$, then by Exercise 20, $u\in\overline{F}$ and therefore $u\in F$ since $F$ is closed, a contradiction to $K$ and $F$ being disjoint. So $\inf\rho_F(K)=\rho_F(u)>0$. Let $\delta$ be a number such that $0<\delta<\inf\rho_F(K)$. For a point $p\in K$ and all points $q\in F$, $d(p,q)\geq \rho_F(p)$, and for all $p\in K$, $\rho_F(p)\geq \inf\rho_F(K)>\delta$, so $d(p,q)>\delta$ for all $p\in K$ and $q\in F$.


Let $A=\{n\,\vert \,n\in \mathbb{N}\}$ and $B=\{n+\frac{1}{n+1}\vert n\in \mathbb{N}\}$. $A$ and $B$ are disjoint, and both of which are closed but not compact. For every $\varepsilon>0$, let $N$ be the positive integer such that $N+1>\frac{1}{\delta}$, then $p=N\in A$ and $q=N+\frac{1}{N+1}\in B$ satisfy $d(p,q)=\frac{1}{N+1}<\delta$.

-----

### 22.

If $\rho_A(p)=\rho_B(p)=0$, then $p\in\overline{A}=A$ and $p\in\overline{B}=B$, a contradiction to $A$ and $B$ being disjoint, so $\rho_A(p)+\rho_B(p)\neq0$ for all $p\in X$. By Theorem 4.9, $f$ is continuous. $\rho_A(p)\geq0$ and $\rho_B(p)\geq0$, so

$$
\begin{aligned}
0=\frac{0}{\rho_A(p)+\rho_B(p)}\leq\frac{\rho_A(p)}{\rho_A(p)+\rho_B(p)}\leq\frac{\rho_A(p)}{\rho_A(p)}=1
\end{aligned}
$$

for all $p\in X$, so the range of $f$ lies in $[0,1]$. $f(p)=0$ if and only if $\rho_A(p)=0$, if and only if $p\in\overline{A}=A$. $f(p)=1$ if and only if $\rho_B(p)=0$, if and only if $p\in\overline{B}=B$.

$f$ is a continuous function from $X$ to $Y=[0,1]$. $[0,\frac{1}{2})$ is open in $Y$, so $V=f^{-1}([0,\frac{1}{2}))$ is open in $X$ by Theorem 4.8. Similarly, $W=f^{-1}((\frac{1}{2},1])$ is open in $X$. $f(p)=0\in[0,\frac{1}{2})$ for all $p\in A$, so $A\subset V$. Similarly, $B\subset W$.

-----

### 23.

Let $x$ be a point in $(a,b)$. Find $p,q$ and $\eta$ such that $a<p<p+\eta<x<q-\eta<q<b$. Let $M_1=\max(f(p),f(q))$. For every $t$ such that $p<t<q$, let $\lambda=\frac{q-t}{q-p}$, then 

$$
\begin{aligned}
t&=\lambda p+(1-\lambda)q\\
f(t)&\leq \lambda f(p)+(1-\lambda)f(q)\leq \lambda M_1+(1-\lambda)M_1=M_1
\end{aligned}
$$

So $f(t)\leq M_1$ for all $t$ in $(p,q)$.

For every $t$ such that $\frac{p+q}{2}<t<q$, let $\lambda=\frac{2t-p-q}{2(t-p)}$, then

$$
\begin{aligned}
\frac{p+q}{2}&=\lambda p+(1-\lambda)t\\
f(\frac{p+q}{2})&\leq \lambda f(p)+(1-\lambda)f(t)
\end{aligned}$$

$$
\begin{aligned}
        f(t) & \geq \frac{1}{1-\lambda}f(\frac{p+q}{2})-\frac{\lambda}{1-\lambda}f(p)\\
        & =\frac{2(t-p)}{q-p}f(\frac{p+q}{2})-\frac{2t-p-q}{q-p}f(p)\\
        & \geq -2\left\vert f(\frac{p+q}{2}) \right\vert -\vert f(p)\vert 
\end{aligned}$$

Let $M_2=-2\left\vert f(\frac{p+q}{2}) \right\vert -\vert f(p)\vert$, then $f(t)\geq M_2$ for all $t$ in $(\frac{p+q}{2},q)$. Similarly, we can find $M_3$ such that $f(t)\geq M_3$ for all $t$ in $(p,\frac{p+q}{2})$. Let $M=\max(\vert M_1\vert ,\vert M_2\vert ,\vert M_3\vert ,\vert f(p)\vert ,\vert f(q)\vert ,\vert f(\frac{p+q}{2})\vert )$, then $\vert f(t)\vert <M$ for all $t$ in $[p,q]$.

For every $\varepsilon>0$, let $\delta=\frac{\eta}{2M}\varepsilon$. For every $y$ in $(x,x+\delta)$, let $\lambda=\frac{y-x}{y-p}$, then

$$
\begin{aligned}
x&=\lambda p+(1-\lambda)y\\
f(x)&\leq \lambda f(p)+(1-\lambda)f(y)\\
f(x)-f(y)&\leq\lambda\left(f(p)-f(y) \right)=\frac{y-x}{y-p}\left(f(p)-f(y) \right)<\frac{\delta}{\eta}\cdot 2M=\varepsilon
\end{aligned}
$$

Let $\lambda=\frac{q-y}{q-x}$, then

$$
\begin{aligned}
y&=\lambda x+(1-\lambda)q\\
f(y)&\leq \lambda f(x)+(1-\lambda)f(q)\\
f(y)-f(x)&\leq(1-\lambda)(f(q)-f(x))=\frac{y-x}{q-x}(f(q)-f(x))<\frac{\delta}{\eta}\cdot 2M=\varepsilon
\end{aligned}
$$

So $\vert f(y)-f(x)\vert <\varepsilon$ for all $y$ in $(x,x+\delta)$. Similarly, $\vert f(y)-f(x)\vert <\varepsilon$ for all $y$ in $(x-\delta,x)$. Therefore, for every $\varepsilon>0$ there is a $\delta>0$ such that $\vert y-x\vert <\delta$ implies $\vert f(y)-f(x)\vert <\varepsilon$, so $f$ is continuous at $x$. Since $x$ is arbitrary, $f$ is continuous.

If $g$ is an increasing convex function, and $f$ is convex, then

$$
\begin{aligned}
g(f(\lambda x+(1-\lambda)y))\leq g(\lambda f(x)+(1-\lambda)f(y))\leq \lambda g(f(x))+(1-\lambda)g(f(y))
\end{aligned}
$$

so $g\circ f$ is convex.

If $f$ is convex in $(a,b)$ and $a<s<t<u<b$, let $\lambda=\frac{u-t}{u-s}$, then

$$
\begin{aligned}
&t=\lambda s+(1-\lambda)u\\
&f(t)\leq \lambda f(s)+(1-\lambda)f(u)=\frac{u-t}{u-s}f(s)+\frac{t-s}{u-s}f(u)
\end{aligned}
$$

Rearranging we can obtain

$$
\begin{aligned}
\frac{f(t)-f(s)}{t-s}&\leq\frac{f(u)-f(s)}{u-s}\\
\frac{f(u)-f(s)}{u-s}&\leq\frac{f(u)-f(t)}{u-t}
\end{aligned}
$$

-----

### 24.

Consider the inequality $f(\lambda x+(1-\lambda)y)\leq \lambda f(x)+(1-\lambda)f(y)$ for all $x,y\in (a,b)$. If $\lambda=0$ or $1$, the inequality holds. If $\lambda=\frac{1}{2}$,

$$
\begin{aligned}
f(\lambda x+(1-\lambda)y)=f(\frac{x+y}{2})\leq\frac{f(x)+f(y)}{2}=\lambda f(x)+(1-\lambda)f(y)
\end{aligned}
$$

so the inequality holds. Suppose the inequality holds for $\lambda=\frac{k}{2^n}$ where $n$ is a positive integer and $k=0,1,\cdots,2^n$. Consider $\lambda=\frac{r}{2^{n+1}}$ where $r=0,1,\cdots,2^{n+1}$. If $r$ is even, then the inequality holds since $\lambda=\frac{r}{2^{n+1}}=\frac{2r'}{2^{n+1}}=\frac{r'}{2^n}$ where $r'$ is an integer. If $r$ is odd, then $\lambda=\frac{r}{2^{n+1}}=\frac{1}{2}\left(\frac{t}{2^n}+\frac{t+1}{2^n} \right)$ for some integer $t$, so

$$
\begin{aligned}
        & \quad\,\, f\left[\frac{r}{2^{n+1}}x+\left(1-\frac{r}{2^{n+1}} \right)y \right]\\
        & =f\left[\frac{\frac{t}{2^n}x+(1-\frac{t}{2^n})y+\frac{t+1}{2^n}x+(1-\frac{t+1}{2^n})y}{2} \right]\\
        & \leq\frac{f\left[\frac{t}{2^n}x+(1-\frac{t}{2^n})y \right]+f\left[\frac{t+1}{2^n}x+(1-\frac{t+1}{2^n})y \right]}{2}\\
        & \leq \frac{\frac{t}{2^n}f(x)+(1-\frac{t}{2^n})f(y)+\frac{t+1}{2^n}f(x)+(1-\frac{t+1}{2^n})f(y)}{2}\\
        & =\frac{r}{2^{n+1}}f(x)+\left(1-\frac{r}{2^{n+1}} \right)f(y)
\end{aligned}
$$

so the inequality holds for $\lambda=\frac{r}{2^{n+1}}$. Therefore, by induction, the inequality holds for all $\lambda\in A$ where $A=\{\frac{k}{2^n}\,\vert \,n,k\in\mathbb{N},\,0\leq k\leq 2^n\}$. For $x,y\in(a,b)$, consider the function $g$ from $[0,1]$ to $R^1$ that maps $\lambda$ to $\lambda f(x)+(1-\lambda)f(y)-f(\lambda x+(1-\lambda)y)$. For all $\lambda \in A$, $\lambda f(x)+(1-\lambda)f(y)-f(\lambda x+(1-\lambda)y)\geq0$, so $g(\lambda)\geq0$, which means $A\subset g^{-1}([0,\infty))$. Since $f$ is continuous, $g$ is continuous, and since $[0,\infty)$ is closed in $R^1$, $g^{-1}([0,\infty))$ is closed in $[0,1]$ by Theorem 4.8. For $\lambda\in[0,1]$, every neighborhood of $\lambda$ contains a point of $A$ and therefore a point of  $g^{-1}([0,\infty))$, so $\lambda$ is a point or a limit point of $g^{-1}([0,\infty))$, and since $g^{-1}([0,\infty))$ is closed, $\lambda\in g^{-1}([0,\infty))$, which is $g(\lambda)\geq0$. Therefore, for every $x,y\in(a,b)$ and $\lambda\in[0,1]$, the inequality $f(\lambda x+(1-\lambda)y)\leq\lambda f(x)+(1-\lambda)f(y)$ holds, so $f$ is convex.

-----

### 25.

(a) Take $\V{z}\not\in K+C$, put $F=\V{z}-C$, the set of all $\V{z}-\V{y}$ with $\V{y}\in C$. If $\V{t}\in K$ and $\V{t}\in F$, then $\V{t}=\V{x}=\V{z}-\V{y}$ for some $\V{x}\in K$ and $\V{y}\in C$, a contradiction to $\V{z}\not\in K+C$, so $K$ and $F$ are disjoint. $K$ is compact and $F$ is closed since $C$ is closed, so by Exercise 21, there exists $\delta>0$ such that $\vert \V{p}-\V{q}\vert >\delta$ if $\V{p}\in K,\,\V{q}\in F$, so $\vert \V{p}-\V{q}\vert =\vert \V{p}-(\V{z}-\V{r})\vert =\vert \V{p}+\V{r}-\V{z}\vert >\delta$ for $\V{p}\in K,\,\V{r}\in C$, which means the open ball with center $\V{z}$ and radius $\delta$ contains no element of $K+C$. So if $\V{z}\not\in K+C$, then $\V{z}$ is not a limit point of $K+C$, which means $K+C$ is closed.


(b)
$C_1$ and $C_2$ have no limit points and therefore closed. Let $\beta_k=k\alpha-[k\alpha]$, where $k$ is a positive integer, and $[k\alpha]$ denotes the largest integer less than or equal to $k\alpha$. If $i\neq j$ but $\beta_i=\beta_j$, then $i\alpha-[i\alpha]=j\alpha-[j\alpha]$, so

$$
\begin{aligned}
\alpha=\frac{[i\alpha]-[j\alpha]}{i-j}
\end{aligned}
$$

which means $\alpha$ is rational, a contradiction. Therefore, $\beta_i\neq\beta_j$ for $i\neq j$, so there are infinitely many different elements of $\{\beta_k\}$ in $(0,1)$. For every integer $N$, consider the disjoint sets $(\frac{0}{N},\frac{1}{N}),\,[\frac{1}{N},\frac{2}{N}),\cdots,[\frac{N-1}{N},\frac{N}{N})$ whose union is $(0,1)$. There are only $N$ sets but infinitely many elements of $\{\beta_k\}$ in $(0,1)$, which means there are at least two elements $\beta_i,\beta_j$ in the same set, so $0<\beta_i-\beta_j<\frac{1}{N}$. Note that $\beta_i-\beta_j=(i+j)\alpha-([i\alpha]+[j\alpha])$ is an element of $C_1+C_2$, so for every positive integer $N$ there is an element $y$ of $C_1+C_2$ such that $0<y<\frac{1}{N}$. For every $x\in R^1$ and $\varepsilon>0$, let $N$ be a positive integer such that $N>\frac{1}{\varepsilon}$, then the segment $(\frac{k}{N},\frac{k+1}{N})$ for some integer $k$ is in the neighborhood of $x$ with radius $\varepsilon$. Let $n$ be the integer such that $n\leq\frac{k}{N}<n+1$, and let $y$ be an element of $C_1+C_2$ such that $0<y<\frac{1}{N}$, then there is an integer $m$ such that $\frac{k}{N}<n+my<\frac{k+1}{N}$, while $n+my\in C_1+C_2$, so $(\frac{k}{N},\frac{k+1}{N})$ contains a point of $C_1+C_2$. Therefore, every neighborhood of $x\in R^1$ contains a point of $C_1+C_2$, which means $C_1+C_2$ is dense in $R^1$. $C_1+C_2$ is countable but $R^1$ is uncountable, so there exists $x\in R^1$ but $x\not\in C_1+C_2$, which means $x$ is a limit point of $C_1+C_2$ while not in $C_1+C_2$, so $C_1+C_2$ is not closed.

-----

### 26.

$g$ is a continuous one-to-one mapping of the compact metric space $Y$ onto $g(Y)$, so $g^{-1}$ is a continuous mapping of $g(Y)$ onto $Y$ by Theorem 4.17. Since $Y$ is compact and $g$ is continuous, $g(Y)$ is compact by Theorem 4.14, and since $g^{-1}$ is continuous, $g^{-1}$ is uniformly continuous by Theorem 4.19. Therefore, if $h$ is uniformly continuous, then $f=g^{-1}\circ h$ is uniformly continuous by Exercise 12. If $h$ is continuous, then $f=g^{-1}\circ h$ is continuous by Theorem 4.7.

Let $X=Z=\{\V{x}\in R^2\,\vert \; \vert \V{x}\vert =1\}$ and $Y=\{x\in R^1\,\vert \,0\leq x<2\pi\}$. Let $g$ be the function from $Y$ onto $Z$ such that $g(t)=(\cos t,\sin t)$. Since $g$ is a one-to-one mapping onto $Z$, $g^{-1}$ is a well-defined function from $Z$ to $Y$. Let $f$ be the same as $g^{-1}$ with the domain replaced by $X$. $h=g\circ f$ is the identity function and therefore uniformly continuous, but $f$ is not continuous at $\V{x}=(0,1)$. Note that $Y$ is not compact while $X$ and $Z$ are compact.

{% endraw %}
