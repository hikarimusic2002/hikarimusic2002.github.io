---
layout: splash
title: "Principles of Mathematical Analysis Ch2"
permalink: /solutions/real_analysis_02
author_profile: false

---

# Chapter 2: Basic Topology

{% raw %}

### 1.

"$\newcommand{\V}{\mathbf} x\in\phi $" is always false, so "$x\in\phi \Rightarrow x\in S$" in always true, by mathematical logic.

-----

### 2.

Let $S$ be the set of equations of the form $a_0z^n+a_1z^{n-1}+\cdots+a_{n-1}z+a_n=0$ with $a_0,\cdots,a_n$ being integers. Let $A_N$ be the set of equations in $S$ such that $n+\vert a_0\vert +\vert a_1\vert +\cdots+\vert a_n\vert =N$ with $N$ being positive integer. By \textit{Hint}, $A_N$ is finite (it has less than $\frac{(N+n+1)!}{N!(n+1)!}2^{n+1}$ elements). It is obvious that

$$
\begin{aligned}
S=\bigcup_{N=1}^\infty A_N
\end{aligned}
$$

Because $A_N$ is finite, $S$ is countable by Theorem 2.12. Let $\alpha$ be an equation is $S$, and let $B_\alpha$ be the set of complex numbers satisfying $\alpha$. By fundamental theorem of algebra, the roots of $\alpha$ are countable, so $B_\alpha$ is countable. So the set

$$
\begin{aligned}
T=\bigcup_{\alpha\in S}B_\alpha
\end{aligned}
$$

is countable by Corollary of Theorem 2.12, and the set of algebraic numbers is a subset of $T$, so the set of algebraic numbers is countable.

-----

### 3.

If every real number is algebraic, then the set of real numbers is a subset of the set of algebraic numbers and is therefore at most countable by Exercise 2, which contradicts the fact that the set of real numbers is uncountable (Corollary of Theorem 2.43).

-----

### 4.

Not countable. If the set of irrational numbers is countable, then because the set of rational numbers is also countable, the set of real numbers, which is the union of rational and irrational numbers, will be countable, contradicting to the fact that the set of real numbers is uncountable.

-----

### 5.

Let $A=\{\frac{1}{n}\vert n\in\mathbb{N}\}$, $B=\{1+\frac{1}{n}\vert n\in\mathbb{N}\}$, $C=\{2+\frac{1}{n}\vert n\in\mathbb{N}\}$. Then the set $A\cup B\cup C$ is bounded and has only three limit points: $0,1,2$. 

-----

### 6.

Let $p$ be a limit point of $E'$, then every neighborhood of $p$, $\{x\vert d(x,p)<r_1\}$ contains a $q\in E'$, which means $q$ is a limit point of $E$, so every neighborhood of $q$, $\{x\vert d(x,q)<r_2\}$ contains a $s\in E$. 

Let $r_2=r_1-d(q,p)$, then 

$$
\begin{aligned}
d(s,p)\leq d(s,q)+d(q,p)<r_2+d(q,p)=r_1
\end{aligned}
$$

which means $s$ is in the neighboorhood of $p$. So every neighborhood of $p$ contains a point of $E$, which means $p$ is a limit point of $E$, so $p\in E'$. So every limit point of $E'$ belongs to $E'$, which means $E'$ is closed.

If $a$ is a limit point of $\bar{E}$, then every neighborhood of $a$ contains a point of $E$ or $E'$, and from above we know that the later also implies the neighborhood contains a point of $E$, so $a$ is a limit point of $E$. So every limit point of $\bar{E}$ is a limit point of $E$.

If $b$ is a limit point of $E$, so every neighborhood of $b$ contains a point of $E$, then because $E\subset\bar{E}$, the neighborhood contains a point of $\bar{E}$, which means $b$ is a limit point of $\bar{E}$. So every limit point of $E$ is a limit point of $\bar{E}$.

From the above two statements we know $E$ and $\bar{E}$ have the same limit points.

$E$ and $E'$ do not necessary have the same limit points. Let $E$ be $\{\frac{1}{n}\vert n\in\mathbb{N}\}$, then $0$ is a limit point of $E$, but that also means $E'$ has only $0$ as its element, so $E'$ has no limit point.

-----

### 7.

(a) $B_n\supset A_i$, so $\bar{B}_n\supset A_i$. By Theorem 2.27(a) we know $\bar{B}_n$ is closed, so by Theorem 2.27(c) we have $\bar{B}_n\supset\bar{A}_i$. Therefore $\bar{B}_n\supset\bigcup_{i=1}^n\bar{A}_i$.

$B_n\subset\bigcup_{i=1}^n\bar{A}_i$. Because $\bar{A}_i$ is closed, by Theorem 2.24(d) we know $\bigcup_{i=1}^n\bar{A}_i$ is closed. So by Theorem 2.27(c) we have $\bar{B}_n\subset\bigcup_{i=1}^n\bar{A}_i$.

The above two statements implies $\bar{B}_n=\bigcup_{i=1}^n\bar{A}_i$.


(b) The first result in (a) still holds, but the second does not because when $n$ becomes infinity, Theorem 2.24(d) no longer applies. So we have only $\bar{B}_n\supset\bigcup_{i=1}^\infty\bar{A}_i$. 

Let $A_n=\{x\vert x>\frac{1}{n}\}$. Then $B=\{x\vert x>0\}$, $\bar{B}=\{x\vert x\geq0\}$, $\bar{A}_n=\{x\vert x\geq\frac{1}{n}\}$, $\bigcup_{n=1}^\infty\bar{A}_n=\{x\vert x>0\}$. So $0$ is a element of $\bar{B}_n$ but not $\bigcup_{i=1}^\infty\bar{A}_i$.

-----

### 8.

Every point $p$ of an open set $E$ is an interior point of $E$, which means there is a neighborhood $\{x:\vert \V{x}-\V{p}\vert <r_1\}\subset E$. For every neighborhood of $p$, $N_r(p)=\{x:\vert \V{x}-\V{p}\vert <r_2\}$, let $y$ be a point such that $0<\vert \V{y}-\V{p}\vert <\min(r_1,r_2)$, then $y\neq p$ and $y$ is in both $E$ and $N_r(p)$. So every neighborhood of $p$ contains a point of $E$ , which means $p$ is a limit point of $E$.

The statement does not hold for closed set when the closed set contains isolated points, for example $E=\{(0,0)\}$.

-----

### 9.

(a) Let $p\in E^\circ$, which means $p$ is an interior point of $E$, so there is a neighborhood $N_p$ such that $N_p\subset E$. $N_p$ is an open set, so for every $q\in N_p$, there is a neighborhood $N_q$ such that $N_q\subset N_p$, and therefore $N_q\subset E$. The fact that $q$ has a neighborhood $N_q\subset E$ implies $q$ is an interior point of $E$, or $q\in E^\circ$. The statement "$q\in N_p\Rightarrow q\in E^\circ$" implies $N_p\subset E^\circ$, so for every $p\in E^\circ$ there is a neighborhood $N_p\subset E^\circ$, which means $E^\circ$ is open.

(b) If $E$ is open, then every point in $E$ is an interior point of $E$ and therefore belongs to $E^\circ$, so $E\subset E^\circ$. It is obvious that $E^\circ\subset E$, so $E=E^\circ$.

If $E^\circ=E$, then because $E^\circ$ is open, $E$ is open.


(c) If $G$ is open, then for every $p\in G$ there is a neighborhood $N_p\subset G$, and therefore $N_p\subset E$. So $p$ is an interior point of $E$, which means $p\in E^\circ$. The statement "$ p\in G\Rightarrow p\in E^\circ$" implies $G\subset E^\circ$.


(d)
For every $p\in(E^\circ)^c$, $p\not\in E^\circ$, so $p$ is not an interior point of $E$, which means every neighborhood of $p$ contains an element not in $E$, which means in $E^c$. Then $p$ is either an element of $E^c$, or a limit point of $E^c$, in either cases $p\in\overline{(E^c)}$. So $(E^\circ)^c\subset\overline{(E^c)}$.
 
For every $p\in\overline{(E^c)}$, either $p\in E^c$, or $p$ is a limit point of $E^c$. For the former case, because $E^\circ\subset E$, $(E^\circ)^c\supset E^c$, so $q\in E^c\subset (E^\circ)^c$. For the later case, every neighborhood of $p$ contains an element of $E^c$, so $p$ cannot be an interior point of $E$, $p\not\in E^\circ$, $p\in(E^\circ)^c$. In either cases $p\in(E^\circ)^c$, so $\overline{(E^c)}\subset(E^\circ)^c$.

Combining the above two statements we have $(E^\circ)^c=\overline{(E^c)}$.


(e) No. Let $E=(-1,0)\cup(0,1)$. Then $\bar{E}=[-1,1]$, $E^\circ=(-1,0)\cup(0,1)$, $(\bar{E})^\circ=(-1,1)$, so $E^\circ\neq(\bar{E})^\circ.$


(f) No. Let $E$ contains only a single point, then $\bar{E}$ also contains that point. But $E^\circ$ is empty, and therefore $\overline{(E^\circ)}$ is empty. So $\overline{E}\neq\overline{(E^\circ)}$.

-----

### 10.

We verify the three definitions of metric. 

(a) $d(p,q)=1>0$ if $p\neq q$; $d(p,p)=0$

(b) $d(p,q)=d(q,p)=1$ when $p\neq q$; $d(p,q)=d(q,p)=0$ when $p=q$.

(c) If $p=q$, then $d(p,q)=0\leq d(p,r)+d(r,q)$.

If $p\neq q$, then either $r\neq p$ or $r\neq q$ or both, so $d(p,r)+d(r,q)\geq1=d(p,q)$.

For every subset $E$ in $X$, let $p$ be any point of $E$, then the neighborhood $N_p$ of $p$ with radius $r<1$ will contain only $p$, so $N_p\subset E$, and therefore $p$ is an interior point of $E$, which means $E$ is open. So every subset in $X$ is open.

For every subset of $E$ in $X$, because there is no limit point in $X$ (the neighborhood of $p$ with radius $r<1$ contains only $p$), the statement "every limit point of $E$ is a point of $E$ " is always true, so $E$ is closed. So every subset in $X$ is closed.

For every finite subset $E$ in $X$, let $\{G_\alpha\}$ be an open cover of $E$. Choose one $G_\alpha$ for each element that contains that element, then the resulting subcover is finite and contains E, so $E$ is compact. For every infinite subset $E'$ in $X$, let $G_\alpha$ contains only $\alpha$, $\alpha\in E'$, then $\bigcup_\alpha G_\alpha$ is an open cover of $E'$, while any finite subcover contains only finite elements of $E'$ and therefore cannot contains $E'$, so $E'$ is not compact. In conclusion, a subset in $X$ is compact if and only if it is finite.

-----

### 11.

$d_1$: $d(0,2)=2^2>1^2+1^2=d(0,1)+d(1,2)$, so Definition 2.15(c) is not satisfied and $d_1$ is not a metric.

$d_2$: Definition (a) and (b) can be easily verified. For Definition (c),

$$
\begin{aligned}
\vert p-q\vert &\leq\vert p-r\vert +\vert r-q\vert \leq\vert p-r\vert +\vert r-q\vert +2\sqrt{\vert p-r\vert \vert r-q\vert }=(\sqrt{\vert p-r\vert }+\sqrt{\vert r-q\vert })^2\\
d(p,q)&=\sqrt{\vert p-q\vert }\leq\sqrt{\vert p-q\vert }+\sqrt{\vert r-q\vert }=d(p,r)+d(r,q)
\end{aligned}
$$

so Definition (c) is satisfied, and $d_2$ is a metric.

$d_3$: $d(-1,1)=\vert (-1)^2-1^2\vert =0$ while $-1\neq1$, so Definition  (a) is not satisfied and $d_3$ is not a metric.

$d_4$: $d(1,1)=\vert 1-2\vert =1\neq0$, so Definition (a) is not satisfied and $d_4$ is not a metric.

$d_5$: Definition (a) and (b) can be easily verified. For Definition (c), $\vert p-q\vert \leq\vert p-r\vert +\vert r-q\vert $, so

$$
\begin{aligned}
d(p,q)=
\frac{\vert p-q\vert }{1+\vert p-q\vert }\leq\frac{(\vert p-r\vert +\vert r-q\vert )}{1+(\vert p-r\vert +\vert r-q\vert )}\leq\frac{\vert p-r\vert }{1+\vert p-r\vert }+\frac{\vert r-q\vert }{1+\vert r-q\vert }=d(p,r)+d(r,q)
\end{aligned}
$$

so Definition (c) is satisfied, and $d_5$ is a metric.

-----

### 12.

If an open cover $\bigcup_\alpha G_\alpha$ contains $K$, then there is an open set $G_0$ contains $0$, which means $0$ is an interior point of $G_0$, so there is a neighborhood $N_r(0)=\{x\vert -r<x<r\}$ be included in $G_0$. According to the archimedean property of $R$, there is a $N$ such that $Nr>1$, and if $n>N$, $\frac{1}{n}$ is included in $N_r(0)$ and therefore included in $G_0$ beacause $\frac{1}{n}<\frac{1}{N}<r$. So take the union of $G_0$ and the other $N$ open sets that contain $1,\frac{1}{2},\cdots,\frac{1}{N}$, then we formed a finite subcover of $K$, so $K$ is compact.

-----

### 13.

Let $K_i$ consists of $\frac{1}{2^i}$ and $\frac{1}{2^i}+\frac{1}{n}$, $n=2^{i+1},2^{i+1}+1,\cdots$, so all the elements are in the range $[\frac{1}{2^i},\frac{1}{2^i}+\frac{1}{2^{i+1}}]$, and the only limit point is $\frac{1}{2^i}$. Note that the range of different $K_i$ do not overlap.

Let $K$ be the union of $0$ and all the $K_i$, for $i=1,2,\cdots$. Note that all the elements are in the range $[0,1]$, so $K$ is bounded. We want to find all the limit points of $K$ to prove that it is closed.


For $x<0$, $x$ is not a limit point because the neighborhood with radius $r<\vert x\vert $ does not contain an element of $K$.

$x=0$ is a limit point of $K$ because for every neighborhood with radius $r$, let $N>\log_2\frac{1}{r}$, then $\frac{1}{2^N}<r$, so every neighborhood contains an element of $K$.

For $0<x<1$, either $x$ is in the range of $K_i$, $[\frac{1}{2^i},\frac{1}{2^i}+\frac{1}{2^{i+1}}]$, or in the interval between $K_i$ and $K_{i-1}$, which is $(\frac{1}{2^i}+\frac{1}{2^{i+1}},\frac{1}{2^{i-1}})$. For the former, $x$ is a limit point of $K$ if and only if it is a limit point of $K_i$, so the only possible limit point is $\frac{1}{2^i}$. For the later, $x$ is not a limit point of $K$ because the neighborhood with radius $r<\min\left(\vert x-\frac{1}{2^i}-\frac{1}{2^{i+1}}\vert ,\vert x-\frac{1}{2^{i-1}}\vert \right)$ does not contain an element of $K$.

For $x\geq1$, $x$ is not a limit point because the neighborhood with radius $r<\frac{1}{4}$ does not contain an element of $K$.

So the limit points of $K$ are $0$ and $\frac{1}{2^i}$, $i=1,2,\cdots$, which are all in $K$, so $K$ is closed. 


By Theorem 2.41, $K$ being closed and bounded implies $K$ is compact, and the limit points $0,\frac{1}{2^1},\frac{1}{2^2},\cdots$ form a countable set, so the $K$ we constructed satisfy the condition.

-----

### 14.

Let $G_n=(\frac{1}{n},1)$, then $\bigcup_{n=1}^\infty G_n$ is a open cover of $(0,1)$ because for every $0<x<1$, $x$ is included in $G_N$ if $Nx>1$. Let $\bigcup_{i=1}^kG_{n_i}\;(n_1<n_2\cdots<n_k)$ be a finite subcover of the open cover, then the element $0<x<\frac{1}{n_k}$ is not included in this subcover, a contradiction. So $\bigcup_{n=1}^\infty G_n$ is an open cover of $(0,1)$ but has no finite subcover.

-----

### 15.

For the "closed" case, let $K_n=\{x\vert x\geq n\}$, then $K_n$ is closed and every finite subcollection of $\{K_n\}$ is nonempty, but $\bigcap_1^\infty K_n$ is empty because for every $x$, let $N>x$, then $x$ is not included in $K_N$.


For the "bounded" case, let $K_n=\{x\vert 0<x<\frac{1}{n}\}$, then $K_n$ is bounded and every finite subcollection of $\{K_n\}$ is nonempty, but $\bigcap_1^\infty K_n$ is empty because for every $x$, let $Nx>1$, then $x$ is not included in $K_N$.

-----

### 16.

$E^c=\{p\,\vert \,p^2\leq2\;or\;p^2\geq3\}=\{p\,\vert \,p^2<2\;or\;p^2>3\}$ because there is no rational number whose square is $2$ or $3$. Let $x\in E^c$, if $x^2<2$, by Theorem 1.20(b) there is rational number $y$ such that $x<y<\sqrt{2}$, so the neighborhood $N_r(x)$ with $r=y-x$ is included in $E^c$, which means $x$ is an interior point of $E^c$. Similarly, if $x^2>3$, there is a rational number $y$ such that $\sqrt{3}<y<x$, so the neighborhood $N_r(x)$ with $r=x-y$ is included in $E^c$, which means $x$ is an interior point of $E^c$. So every $x\in E^c$ is an interior point of $E^c$, which means $E^c$ is an open set, and therefore $E$ is an closed set. 

It is obvious that $E$ is bounded.

Let $G_n=\{p\,\vert \,2+\frac{1}{n}<p^2<3\}$, then $\bigcup_{n=1}^\infty G_n$ is an open cover of $E$ because $G_n$ is open (as $E$), and for every $x\in E$, which means $x^2>2$, there is a positive real number $\delta$ such that $x^2>2+\delta$; let $N\delta>1$, then $x^2>2+\delta>2+\frac{1}{N}$, so $x$ is included in $G_N$. For every finite subcover $\bigcup_{i=1}^kG_{n_i}\;(n_1<n_2<\cdots<n_k)$, the rational $x$ in $E$ that satisfy $\sqrt{2}<x<\sqrt{2+\frac{1}{n_k}}$ will not be included in any $G_{n_i}$, so $\bigcup_{i=1}^kG_{n_i}$ cannot be a finite subcover of $E$. Therefore, $E$ is not compact.

For $x\in E$, $2<x^2<3$. There exists $y_1,y_2$ such that $\sqrt{2}<y_1<x<y_2<\sqrt{3}$, so the neighborhood $N_r(x)$ with $r=\min(\vert x-y_1\vert ,\vert x-y_2\vert )$ is included in $E$, which means $x$ is an interior point of $E$, so $E$ is open.

-----

### 17.

_countable_: If $E$ is countable, let its elements be enumerated as $s_1,s_2,\cdots$. Construct a sequence $s$ by making the $n^{th}$ digit of $s$ be $4$ if the $n^{th}$ digit of $s_n$ is $7$, and the $n^{th}$ digit of $s$ be $7$ if the $n^{th}$ digit of $s_n$ is $4$. Then $s$ is different with every $s_i$, but $s$ is a element of $E$, a contradiction. So $E$ is uncountable.

_dense_: $E$ is not dense in $[0,1]$ because there are many points in $[0,1]$ that are neither a point or a limit point of $E$, for example, $0.5$\,.

_compact_: It is obvious that $E$ is bounded. If there is a limit point of $E$ that is not an element of $E$, whose $n^{th}$ digit is neither $4$ nor $7$, consider the neighborhood with radius $r=10^{-(n+1)}$, then the neighborhood cannot contain any element of $E$ because the $n^{th}$ and $(n+1)^{th}$ digit cannot be $44,47,74$ or $77$, a contradiction. So every limit point of $E$ belongs to $E$, which means $E$ is closed. Being bounded and closed implies being compact in $R^1$ (Theorem 2.41).

_perfect_: We have proved that $E$ is closed. If there is a element $x$ of $E$ that is not a limit point of $E$, which means there is a neighborhood $N_r(x)$ contains no element of $E$, let $N$ be large enough so $10^{-N}<r$, and let $y$ be an element of $E$ that is the same with $x$ at the first $N$ digit but different at the $(N+1)^{th}$ digit, then $\vert y-x\vert <10^{-N}<r$, so $y\in E$ is in $N_r(x)$, a contradiction. So every element of $E$ is a limit point of $E$. Together with the fact that $E$ is closed, we proved that $E$ is perfect.

-----

### 18.

Let $E_0=[a_0,b_0]$, $a_0,b_0$ are irrational. Enumerate all the rational number in $[a_0,b_0]$ as $r_1,r_2,\cdots$. For $a_0<r_1<b_0$, found irrational number $a_1,b_1$ that such that $a_0<b_1<r_1<a_1<b_0$, and remove $(b_1,a_1)$ to get $E_1=[a_0,b_1]\cup[a_1,b_0]$. Continue in this way to construct $E_2,E_3,\cdots$ by removing segments around $r_2,r_3,\cdots$ with irrational numbers being the end points, then $E_1\supset E_2\supset E_3\supset\cdots$. Let $P=\bigcap_{n=1}^\infty E_n$. It is obvious that $E_n$ is compact, so by Theorem 2.36, $P$ is not empty. From the construction, $P$ contains no rational number. 

It is obvious that $P$ is closed. If $x\in P$, let $S$ be a neighborhood of $x$. Let $I_n$ be that interval of $E_n$ which contains x. Choose $n$ large enough so that $I_n\subset S$ (It is possible because the length of $I_n$ can be arbitrary small, due to the fact that rational numbers are dense). Let $x_n$ be an endpoint of $I_n$, such that $x_n\neq x$. It follows from the construction of $P$ that $x_n\in P$. Hence $x$ is a limit point of $P$, and $P$ is perfect. Therefore, $P$ is not empty, perfect and contains no rational number, which satisfies the conditions.

-----

### 19.

(a) $A$ and $B$ being disjoint implies $A\cap B=\phi$. From Theorem 2.27, because $A$ and $B$ are closed, $A=\bar{A}$ and $B=\bar{B}$. So $A\cap\bar{B}=\bar{A}\cap B=A\cap B=\phi$,         which means $A$ and $B$ are separated.


(b) If $A\cap B=\phi$ but $A\cap\bar{B}\neq\phi$, then there is a limit point $x$ of $B$ being included in $A$. Because $A$ is open, there is a neighborhood $N_r(x)\subset A$. But because $x$ is also a limit point of $B$, there is an element of $B$ contained in $N_r(x)$, and therefore contained in $A$. So $A$ and $B$ have a common element, a contradiction. So $A\cap\bar{B}=\phi$, similarly $\bar{A}\cap B=\phi$, so $A$ and $B$ are separated.


(c) It is obvious that $A$ and $B$ are disjoint open sets, so by (b), $A$ and $B$ are separated.


(d) Let $E$ be a connected metric space with at least two points. Assume $E$ is countable. Find two points $a$ and $b$. The set of real number between $0$ and $d(a,b)$ is uncountable, but the set of distances between $a$ and other elements are countable, so there exist a $\delta$ such that $0<\delta<d(a,b)$ and $\delta$ is not equal to any distance between $a$ and other elements. So $E=\{x\vert d(a,x)<\delta\}\cup\{x\vert d(a,x)>\delta\}$, which means $E$ is not connected by (c), a contradiction. So $E$ must be uncountable.

-----

### 20.

Let $\bar{E}$ be a closure of a connected set $E$. Assume $\bar{E}$ is not connected, so there are two nonempty sets $A$ and $B$ such that $\bar{E}=A\cup B$ and $\bar{A}\cap B=A\cap\bar{B}=\phi$. Note that

$$
\begin{aligned}
E=\bar{E}\cap E=(A\cup B)\cap E=(A\cap E)\cup(B\cap E)
\end{aligned}
$$

If $A\cap E=\phi$, then $A\subset E'$ and $E\subset B$, so $A\subset E'\subset\bar{E}\subset\bar{B}$, which means $A\cap\bar{B}\neq\phi$, a contradiction. So $A\cap E\neq\phi$, and similarly $B\cap E\neq\phi$. 

$A\cap E\subset A$,\; $\overline{(A\cap E)}\subset\overline{A}$,\; $B\cap E\subset B$,\; $\overline{(B\cap E)}\subset\overline{B}$. So $\overline{(A\cap E)}\cap(B\cap E)\subset\overline{A}\cap B=\phi$, and $(A\cap E)\cap\overline{(B\cap E)}\subset A\cap\overline{B}=\phi$, which means $A\cap E$ and $B\cap E$ are two nonempty separated sets, so $E$, being the union of them, is not connected, a contradiction. So $\bar{E}$ must be connected.

The interior of a connected set can be not connected. Consider a set $E$ in $R^2:$

$$
\begin{aligned}
E=\{\V{x}:\vert \V{x}-(-2,0)\vert <1\}\cup\{\V{x}:\vert \V{x}-(2,0)\vert <1\}\cup\{\V{x}:\V{x}=(k,0),-2<k<2\}
\end{aligned}
$$

which means $E$ consists of two balls and a line connecting them. It is obvious that $E$ is connected, but its interior, being $\{\V{x}:\vert \V{x}-(-2,0)\vert <1\}\cup\{\V{x}:\vert \V{x}-(2,0)\vert <1\}$, is not connected.

-----

### 21.

(a) If $x\in A_0'$, so $x$ is a limit point of $A_0$, then every neighborhood $N_{r_0}(x)$ contains a point $y\neq x$ such that $y\in A_0$. Consider a neighborhood of $\V{p}(x)$ with radius $r$. Let $r_0=\frac{r}{\vert \V{a}\vert +\vert \V{b}\vert }$, then there is a $y\in A_0$ such that $\vert y-x\vert <r_0=\frac{r}{\vert \V{a}\vert +\vert \V{b}\vert }$. Then $\vert \V{p}(y)-\V{p}(x)\vert =\vert -(y-x)\V{a}+(y-x)\V{b}\vert \leq\vert y-x\vert (\vert \V{a}\vert +\vert \V{b}\vert )<r$, so $\V{p}(y)\in A$ is in the neighborhood of $P(x)$, which means $\V{p}(x)$ is a limit point of $A$. Therefore, if $x\in A_0'$, then $\V{p}(x)\in A'$. It implies that if $x\in\bar{A}_0$, then $\V{p}(x)\in\bar{A}$. Similarly, if $x\in\bar{B}_0$, then $\V{p}(x)\in\bar{B}$.

$A$ and $B$ are separated, so $\bar{A}\cap B=A\cap\bar{B}=\phi$. If $x\in B_0$, $\V{p}(x)\in B$, then $\V{p}(x)\not\in \bar{A}$, so $x\not\in \bar{A}_0$. It implies $\bar{A}_0\cap B_0=\phi$. Similarly, $A_0\cap\bar{B}_0=\phi$. So $A_0$ and $B_0$ are separated. 


(b)
Let $(0,1)=I$. $(A_0\cup B_0)\cap I=(A_0\cap I)\cup(B_0\cap I)\subset I$. Because $A_0$ and $B_0$ are separated, so $A_0\cap I$ and $B_0\cap I$ are separated, but $I=(0,1)$ is connected, so $(A_0\cup B_0)\cap I$ is a proper subset of $I$. So there must exist a $t_0\in(0,1)$ but $t_0\not\in A_0\cup B_0$ , which means $\V{p}(t_0)\not\in A\cup B$.


(c) If a subset $E$ of $R^k$ is not connected, then $E$ is the union of two nonempty separated sets $A$ and $B$. Let $\V{a}\in A\in E$, $\V{b}\in B\in E$, then by (b) there is a $t_0\in(0,1)$ such that $(1-t)\V{a}+t\V{b}\not\in A\cup B=E$. However, if $E$ is convex, then whenever $\V{a}\in E$, $\V{b}\in E$ and $0<t<1$, we must have $(1-t)\V{a}+t\V{b}\in E$, which means that $E$ is connected.

-----

### 22.

Consider the set of points which have only rational coordinates, $Q^k$. Because the set of rational numbers is countable, so by Theorem 2.13 we knows $Q^k$ is countable. Consider any point $\V{x}=(x_1,x_2,\cdots,x_k)\in R^k$, and consider a neighborhood of $\V{x}$ with radius $r$. Find rational numbers $a_i$ such that $x_i-\frac{r}{\sqrt{k}}<a_i<x_i+\frac{r}{\sqrt{k}},\;i=1,2,\cdots,k$ (They exist by Theorem 1.20(b)). Then $\vert \V{a}-\V{x}\vert =\sqrt{\sum_k(a_i -x_i)^2}<r$, so $\V{a}\in Q^k$ is in the neighborhood of $\V{x}$, which means $\V{x}$ is a limit point of $Q^k$, so $Q^k$ is dense in $R^k$. Therefore, $Q^k$ is a countable dense subset of $R^k$, which means $R^k$ is separable.

-----

### 23.

Let $X$ be a separable metric space, and let $C$ be a countable dense subset of $X$. Let $\mathcal{B}$ be the collection of all neighborhoods centered at some point of $C$ with rational radius, which means

$$
\begin{aligned}
\mathcal{B}=\{N_r(x):r\in Q,\;x\in C \}
\end{aligned}
$$

$Q$ and $C$ are countable, so $\mathcal{B}$ is countable by Corollary of Theorem 2.12.

If $G$ is an open set in $X$ and $x\in G$, then there is a neighborhood $N_{\varepsilon}(x)\subset G$. Let $h$ be a rational number such that $0<h<\frac{\varepsilon}{2}$ (it exists by Theorem 1.20 (b)). $C$ is dense in $X$, so $x\in C$ or $x$ is a limit point of $C$, in either cases there is a $q\in C$ such that $q\in N_h(x)$. So $x\in N_h(q)$ (because $d(x,q)<h$), and $N_h(q)\subset N_\varepsilon(x)\subset G$ (because if $y\in N_h(q)$, then $d(y,x)\leq d(y,q)+d(q,x)<h+h=2h<\varepsilon$). Also note that $N_h(q)\in\mathcal{B}$ (because $h\in Q$ and $q\in C$).

Therefore, for every $x\in X$ and every open set $G\subset X$ such that $x\in G$, we have $N_h(q)\in\mathcal{B}$ such that $x\in N_h(q)\subset G$, so $\mathcal{B}$ is a countable base of $X$. So every separable metric space has a countable base.

-----

### 24.

If the process of choosing $x_{j+1}$ from $x_1,\cdots,x_j$ does not stop after a finite number of steps, then $x_1,x_2,\cdots$ form an infinite subset of $X$, and therefore has a limit point $p$ in $X$. Then the neighborhood $N_{\frac{\delta}{2}}(p)$ contains infinite many points of $x_1,x_2,\cdots$ (Theorem 2.20), in specific, two points $x_i$ and $x_j$, so $d(x_i,x_j)=d(x_i,p)+d(p,x_j)<\frac{\delta}{2}+\frac{\delta}{2}=\delta$, a contradiction. So the process must stop after a finite number of steps. 

Therefore, $X$ can be covered by finitely many neighborhoods of radius $\delta$, which means we can find $E_\delta=\{x_{\delta1},x_{\delta2},\cdots,x_{\delta k} \}$ such that 

$$
\begin{aligned}
X\subset\bigcup_{j=1}^kN_\delta(x_{\delta j})
\end{aligned}
$$

for every $\delta>0$. Let

$$
\begin{aligned}
E=\bigcup_{n=1}^\infty E_{\frac{1}{n}}
\end{aligned}
$$

Because $E_{\frac{1}{n}}$ is finite, $E$ is countable by Theorem 2.12. 

For every $x\in X$, let $N_r(x)$ be any neighborhood of $x$, and let $N$ be a positive integer such that $\frac{1}{N}<r$, then $x\in N_{\frac{1}{N}}(y)$ for some $y\in E_{\frac{1}{N}}\subset E$ (because $X$ is covered by neighborhoods of radius $\frac{1}{N}$), and therefore $y\in N_r(x)$ (because $d(y,x)<\frac{1}{N}<r$). So for every $x\in X$, every neighborhood of $x$ contains a point $y\in E$, which means  $x\in E$ or $x$ is a limit point of $E$, and that means $E$ is dense in $X$. So $X$ contains a countable dense subset $E$, which means $X$ is separable.

-----

### 25.

For every compact metric space $K$, the collection of neighborhoods centered at every $x\in K$ with radius $\frac{1}{n}$ forms a open cover of $K$, so it has a finite subcover covering $K$. Let $E_{\frac{1}{n}}$ be the finite subcover, and let 

$$
\begin{aligned}
E=\bigcup_{n=1}^\infty E_{\frac{1}{n}}
\end{aligned}
$$

$E$ is countable by Theorem 2.12. If $G$ is an open set in $K$ and $x\in G$, then there is a neighborhood $N_\varepsilon(x)\subset G$. Let $N$ be an integer such that $0<\frac{1}{N}<\frac{\varepsilon}{2}$. Because $E_{\frac{1}{N}}$ covers $K$, there is an open set $V\in E$ with center $q$ such that $x\in V$. And $V\subset N_{\varepsilon}(x)\subset G$ (because if $y\in V$, then $d(y,x)<d(y,q)+d(q,x)<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon$). Therefore, for every $x\in K$ and every open set $G\subset K$ such that $x\in G$, we have $V\subset E$ such that $x\in V\subset G$, which means $E$ is a countable base of $K$.

Let $C$ be the set of centers of neighborhoods in $E$. $C$ is countable because $E$ is countable. For every $x\in K$ and every neighborhood $N_r(x)$, we can find $x\in V\subset N_r(x)$ where $V\in E$, so the center of $V$, which is an element of $C$, is in $N_r(x)$. So every neighborhood of $x$ contains a point of $C$, which means $x$ is a point or a limit point of $C$, so $C$ is dense in $K$. Therefore, $C$ is a countable dense subset of $K$, which means $K$ is separable.


(Or alternatively, note that every infinite subset of $K$ has a limit point in $K$ (Theorem 2.37), so $K$ is separable (Exercise 24), and therefore has a countable base (Exercise 23).)

-----

### 26.

Every infinite subset of $X$ has a limit point, so $X$ is separable (Exercise 24), and therefore has a countable base (Exercise 23). It follows that every open cover of $X$ has a countable subcover $\{G_n\},\,n=1,2,3,\cdots$ (because every open set is in the union of a subcollection of the countable base). If no finite subcollection of $\{G_n\}$ covers $X$, then the complement $F_n$ of $G_1\cup\cdots\cup G_n$ is nonempty for each $n$, but $\bigcap F_n$ is empty. Let $E$ be a set contains a point from each $F_n$, which means $E=\{x_1,x_2,\cdots\}$ with $x_n\in F_n$, then $E$ is obviously infinite (otherwise there will be an element of $E$ belongs to infinitely many $F_n$, which implies $\bigcap F_n$ being non-empty). So $E$ being infinite implies there is a limit point $p$ of $E$, let $p\in G_k$, and there is a neighborhood $N_r(p)\in G_k\subset G_1\cup\cdots\cup G_k$. For $i\geq k$, $x_i\in F_i$ so $x_i\not\in G_1\cup\cdots\cup G_k$, which means there are at most $k$ elements of $E$ belongs to $G_1\cup\cdots\cup G_k$ and therefore possibly belongs to $N_r(p)$, contradicts to the fact that $p$ is a limit point of $E$ (Theorem 2.20).  So there must be a finite subcollection of $\{G_n\}$ covers $X$, which means $X$ is compact.

-----

### 27.

Let $\{V_n\}$ be a countable base of $R^k$, and let $W$ be the union of those $V_n$ for which $E\cap V_n$ is at most countable.

If $x\in P^c$, then there is a neighborhood $N_r(x)$ containing at most countably many points of $E$. By the definition of countable base,  there is a $V_n\in\{V_n\}$ such that $x\in V_n\subset N_r(x)$. $E\cap V_n\subset E\cap N_r(x)$ is at most countable, so $V_n\subset W$, and therefore $x\in W$. This implies $P^c\subset W$.

If $x\in W$, then there is a $V_n$ such that $x\in V_n$ and $E\cap V_n$ is at most countable. Let $N_r(x)$ be a neighborhood such that $N_r(x)\subset V_n$, then $N_r(x)\cap E\subset V_n\cap E$ is at most countable, which means $N_r(x)$ contains at most countably many points of $E$, so $x\not\in P$. This implies $W\subset P^c$.

From the above two statements, we have $P^c=W$. So

$$
\begin{aligned}
P^c\cap E=W\cap E=\bigcup_{n=1}^\infty V_n\cap E
\end{aligned}
$$

Every $V_n\cap E$ is at most countable, so $P^c\cap E$ is at most countable, which means at most countably many points of $E$ are not in $P$.

Let $x$ be a limit point of $P$, then in every neighborhood $N_r(x)$, there is a $y\in P$ in $N_r(x)$. Let $r'=r-d(x,y)$, then the neighborhood $N_{r'}(y)\subset N_r(x)$, and it contains uncountably many points of E because $y\in P$, so $N_r(x)$ also contains uncountably many points of $E$. So $x\in P$, which means $P$ is closed.

Let $x\in P$ and $N_r(x)$ be a neighborhood of $x$, then $N_r(x)$ contains uncountably many points of $E$. If $N_r(x)$ contains no elements of $P$ other than $x$, then $N_r(x)\subset\{x\}\cup P^c$, and $N_r(x)\cap E\subset \{x\}\cup(P^c\cap E)$ is at most countable, contradicting to the fact that $N_r(x)$ contains uncountably many points of $E$. Therefore, $N_r(x)$ contains an element of $P$ other then $x$, which means $x$ is a limit point of $P$. 

Therefore, $P$ is closed, and every point of $P$ is a limit point of $P$, which means $P$ is perfect.

-----

### 28.

Let $P$ be defined as in Exercise 27. Every point of $P$ is a limit point of $E$, and $E$ is closed, so $P\subset E$, which means $P\cap E=P$.

$$
\begin{aligned}
E=(P\cap E)\cup(P^c\cap E)=P\cup(P^c\cap E)
\end{aligned}
$$

The result in Exercise 27 is not restricted to $R^k$, so $P$ is perfect, and $P^c\cap E$ is at most countable. So $E$ is the union of a perfect set and a set which is at most countable. 

_Corollary_: Let $E$ be a closed set in $R^k$. If it has no isolated point, then it is perfect and is therefore uncountable (Theorem 2.43). So every countable closed set in $R^k$ has isolated point.

-----

### 29.

From Theorem 22 and 23, $R^1$ is separable and has a countable base $\{V_\alpha\}$. For every open set $E$, let $\{V_{\alpha'}\}$ be the collection of all $V_{\alpha'}$ such that $x\in V_{\alpha'}\subset E$ for some $x\in E$. Every $V_{\alpha'}\subset E$, so $\bigcup_{\alpha'}V_{\alpha'}\subset E$. For every $x\in E$, $x\in V_{\alpha'}$ for some $\alpha'$, so $E\subset\bigcup_{\alpha'}V_{\alpha'}$. Therefore $E=\bigcup_{\alpha'}V_{\alpha'}$. $\{V_{\alpha}\}$ is countable, so  $\{V_{\alpha'}\}$ is also countable, and note that $V_{\alpha'}$ is a segment, so $\bigcup_{\alpha'}V_{\alpha'}$ is the union of at most countable collection of disjoint segments.

-----

### 30.

Let $G_n$ be a dense open subset of $R^k$, for $n=1,2,3,\cdots$.
Let $G$ be an nonempty set in $R^k$, and let $N_r(x)\subset G$ be an neighborhood in $G$. $G_1$ is dense in $R^k$, so $N_r(x)$ contains an element of $G_1$, which means $N_r(x)\cap G_1\neq\varnothing$. Both $G_1$ and $N_r(x)$ are open, so $N_r(x)\cap G_1$ is open. Let $N_{r_1}(x_1)$ be a neighborhood such that $\overline{N_{r_1}}\subset N_r(x)\cap G_1$ (It is easy to find it if we first choose a neighborhood with radius $\varepsilon$ in $N_r(x)\cap G_1$, and let $N_{r_1}(x_1)$ be a neighborhood centered at the same point and with radius $\frac{\varepsilon}{2}$). Similarly, $N_{r_1}(x_1)\cap G_2$ is nonempty and open, so we can find $N_{r_2}(x_2)$ such that $\overline{N_{r_2}(x_2)}\subset N_{r_1}(x_1)\cap G_2$. Repeat the process, we have

$$
\begin{aligned}
    \overline{N_{r_1}(x_1)} & \subset N_r(x)\cap G_1\\
    \overline{N_{r_2}(x_2)} & \subset N_{r_1}(x_1)\cap G_2\\
                            & \vdots \\
    \overline{N_{r_n}(x_n)} & \subset N_{r_{n-1}}(x_{n-1})\cap G_n
\end{aligned}
$$

Every $\overline{N_{r_n}(x_n)}$ is closed and bounded and therefore compact. $\overline{N_{r_{n+1}}(x_{n+1})}\subset N_{r_n}(x_n) \subset\overline{N_{r_n}(x_n)}$, so

$$
\begin{aligned}
\overline{N_{r_1}(x_1)}\supset \overline{N_{r_2}(x_2)}\supset\cdots
\end{aligned}
$$

By Theorem 2.36, 

$$
\begin{aligned}
\bigcap_{n=1}^\infty\overline{N_{r_n}(x_n)}\neq\varnothing
\end{aligned}
$$

$\overline{N_{r_n}(x_n)}\subset G_n$, so

$$
\begin{aligned}
\bigcup_{n=1}^\infty G_n\supset\bigcap_{n=1}^\infty\overline{N_{r_n}(x_n)}\neq\varnothing
\end{aligned}
$$

The equivalent statement is proved.

If $R^k=\bigcup_1^\infty F_n$, where every $F_n$ is closed and has empty interior, then $F_n^c$ is open and dense in $R^k$ (Every neighborhood of $x\in F_n$ contains a point not in $F_n$, so $F_n\subset(F_n^c)'$, and $R^k=F\cup F^c\subset(F^c)'\cup F^c$, which means $F^c$ is dense in $R^k$). Then from the equivalent statement, we have 

$$
\begin{aligned}
\bigcap_{n=1}^\infty F_n^c\neq\varnothing
\end{aligned}
$$

which means there is an element not contained in every $F_n$, a contradiction. Therefore, at least one $F_n$ has a nonempty interior.


{% endraw %}
