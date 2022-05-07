---
layout: splash
title: "Principles of Mathematical Analysis"
permalink: /solutions/real_analysis_ch1
author_profile: false
redirect_from:
  - /resume
---

# Chapter 1: Mathematical Preliminaries

### 1.

If $r+x$ is rational, than $x=(r+x)-r$ is rational, a contradiction, so $r+x$ is irrational.

If $rx$ is rational, than $x=(rx)\frac{1}{r}$ is rational, a contradiction, so $rx$ is irrational.
$\newcommand{\V}{\mathbf}$

---------

### 2.

If there is a rational number $\frac{p}{q}$ (p,q are intergers and $gcd(p,q)=1$), whose square is 12. Then $p^2=12q^2$. $3|12$, so $3|p^2$, $3|p$. So $9|p^2$, $9|12q^2$, $3|4q^2$, $3|q$. So $3|p$ and $3|q$, contrary to $gcd(p,q)=1$.

---------

### 3.

(a) $x\neq0$, so $\frac{1}{x}$ exists. $y=y\cdot x\cdot \frac{1}{x}=z\cdot x\cdot \frac{1}{x}=z$

(b) Take $z=1$ in (a).

(c) Take $z=\frac{1}{x}$ in (a).

(d) $\frac{1}{x}\cdot x=1$, so $x=\frac{1}{\frac{1}{x}}$ from (c).

---------

### 4.

For an element x of E, $\alpha\leq x $ and $x\leq \beta$, so $\alpha \leq\beta$.

---------

### 5.

For every $x\in A$, $x\geq \inf A$, so $-x\leq -\inf A$, so $-\inf A$ is an upper bound of -A. If $\gamma<-\inf A$, $-\gamma >\inf A$, so $-\gamma$ is not a lower bound of A, then there is a element $x<-\gamma$ in A. Then there is an element $-x>\gamma$ in -A, which means $\gamma$ is not an upper bound of -A. So $-\inf A=\sup (-A)$, and $\inf A=-\sup (-A)$.


---------

### 6.

(a) $((b^m)^{\frac{1}{n}})^{nq}=b^{mq}=b^{np}=((b^p)^{\frac{1}{q}})^{nq}=k$. By Theorem 1.21, $k^{\frac{1}{nq}}$ is unique, so $(b^m)^{\frac{1}{n}}=(b^p)^{\frac{1}{q}}$. 
\medskip

(b) Let $r=\frac{m}{n}$, $s=\frac{p}{q}$. $(b^{r+s})^{nq}=(b^{\frac{mq+np}{nq}})^{nq}=b^{mq+np}=((b^m)^{\frac{1}{n}}(b^p)^{\frac{1}{q}})^{nq}=(b^rb^s)^{nq}$. By \\Theorem 1.21, $b^{r+s}=b^rb^s$.
\medskip

(c) If $t<r$, then $r-t>0$, so $b^{r-t}>1$, $b^r>b^t$. So $b^r\geq b^t$ for all $b^t\in B(r)$, so $b^r$ is an upper bound of $B(r)$. But $b^r\in B(r)$, so every $\gamma<b^r$ is not an upper bound of $B(r)$, so $b^r=\sup B(r)$.
\medskip

(d) If $b^{x+y}<b^xb^y$, then $\frac{b^{x+y}}{b^y}<b^x$, and there is an rational $t\leq x$ that $\frac{b^{x+y}}{b^y}<b^t$. Then $\frac{b^{x+y}}{b^t}<b^y$, and there is an rational $s\leq y$ that $\frac{b^{x+y}}{b^t}<b^s$. So $b^{s+t}>b^{x+y}$, but $s+t\leq x+y$, contradicting to the definition of $b^{x+y}$.

If $b^{x+y}>b^xb^y$, then there is a rational $r<x+y$ that $b^r>b^xb^y$ $\,^*$, which means $b^r>b^pb^q$ for all rational $p\leq x$ and $q\leq y$. Let $\varepsilon$ be an positive real number such that $r<x+y-\varepsilon$. By Theorem 1.20(b), there are rational $p$ and $q$ such that $x-\frac{\varepsilon}{2}<p<x$ and $y-\frac{\varepsilon}{2}<q<y$. So $r<x+y-\varepsilon<p+q$, and $b^r<b^{p+q}=b^pb^q$, contradicting with $b^r>b^pb^q$.

Therefore, only $b^{x+y}=b^xb^y$ can be the case.

---------

### 7.

(a) 
$b^n-1=(b-1)(b^{n-1}+b^{n-2}+\cdots +1)\geq (b-1)(1+1+\cdots +1)=(b-1)n$
\medskip

(b)
$b^{\frac{1}{n}}>1$, so substitute $b$ with $b^{\frac{1}{n}}$ in (a) we obtain (b).
\medskip

(c)
$b-1\geq n(b^{\frac{1}{n}}-1)>\frac{b-1}{t-1}(b^{\frac{1}{n}}-1)$, so $(b^{\frac{1}{n}}-1)<(t-1)$ since $b-1>0$ and $t-1>0$. So $b^{\frac{1}{n}}<t$.
\medskip

(d)
$b^w<y$, so $y\cdot b^{-w}>1$. So from (c), $b^{\frac{1}{n}}<y\cdot b^{-w}$ when $n>\frac{b-1}{y\cdot b^{-w}-1}$. So $b^{w+\frac{1}{n}}<y$ for sufficiently large n.
\medskip

(e)
$b^w>y$, so $\frac{b^w}{y}>1$. So from (c), $b^{\frac{1}{n}}<\frac{b^w}{y}$ when $n>\frac{b-1}{\frac{b^w}{y}-1}$. Since $b^{\frac{1}{n}},y>0$, $b^{w-\frac{1}{n}}>y$ for sufficiently large n.
\medskip

(f)
If $b^x<y$, from (d) $b^{x+\frac{1}{n}}<y$ for some n. Then $x+\frac{1}{n}\in A$, but $x+\frac{1}{n}>x$, contrary to the fact that x in an upper bound of A.

If $b^x>y$, form (e) $b^{x-\frac{1}{n}}>y$ for some n. So $b^{x-\frac{1}{n}}>b^w$, and $x-\frac{1}{n}>w$ for all w in A since $b>1$. So $x-\frac{1}{n}$ is an upper bound of A, but $x-\frac{1}{n}<x$, contrary to $x=\sup A$.

Therefore, only $b^x=y$ can be the case.
\medskip

(g)
If $x<x'$, let $q$ be a rational that $x<q<x'$(Theorem 1.20(b)). By definition of real power in Exercise 6, $b^x<b^q\leq b^{x'}$, so $b^x<b^{x'}$. Similarly, $x>x'$ implies $b^x>b^{x'}$. Therefore, if $b^x=b^{x'}$, then $x=x'$ and $x$ is unique

---------

### 8.

If complex field is an ordered field, then $1>0$ from proposition 1.18(d), $-1<0$ from proposition 1.18(a). But $-1=i^2>0$ from proposition 1.18(d), a contradiction, so complex field cannot be an ordered field.

---------

### 9.

When $a<c$, $z<w$. When $a>c$, $z>w$. When $a=c$ and $b<d$, $z<w$. When $a=c$ and $b>d$, $z>w$. When $a=c$ and $b=d$, $z=w$. So definition 1.5(i) is satisfied.

If $z<w$ and $w<r$ ($r=e+fi$), then $a<c$ or $a=c$, $c<e$ or $c=e$. If $a<c$, then $a<e$, so $z<r$. If $a=c$ and $c<e$, then $a<e$, so $z<r$. If $a=c$ and $c=e$, then $b<d$ and $d<f$, so $b<f$, so $z<r$. Therefore, for all cases $z<r$ when $z<w$ and $w<r$, satisfying definition 1.5(ii).
\medskip

Assume that complex number under this definition has least-upper-bound property. Consider the set $S=\{xi|x\in\mathbb{R}\}$. $1$ is greater than all the $0+xi$, so $S$ is bound above. Let $a+bi=\sup S$, $a\geq0$. If $a>0$, then $\frac{a}{2}>0$ is also an upper bound, a contradiction. So $a=0$, but then $(b+1)i>a+bi$ and $(b+1)i\in S$, a contradiction. Therefore, complex number under this definition cannot have least-upper-bound property.

---------

### 10.

$z^2=(a^2-b^2)+2abi$, $a^2-b^2=u$, $2ab=(|w|^2-u^2)^{\frac{1}{2}}=|v|$, so when $v\geq 0$, $z^2=w$, when $v\leq 0$, $\overline{z}^2=u-2abi=u+vi=w$. When $w\neq 0$, either $a$ or $b\neq 0$, and $z\neq -z$, so $\pm z^2=w$ when $v\geq 0$ and $\pm \overline{z}^2=w$ when $v\leq 0$.

---------

### 11.

If $z=0$, then $r=0$ and $w$ can be any complex number that $|w|=1$. $w$ and $r$ are not uniquely determined by $z$.
\medskip

If $z\neq 0$, let $z=a+bi$. Let $r=\sqrt{a^2+b^2}$ and $w=\frac{a}{\sqrt{a^2+b^2}}+\frac{b}{\sqrt{a^2+b^2}}i$. Then $|w|=\frac{a^2+b^2}{a^2+b^2}=1$, and $z=rw$.
If $z=rw$, then $|z|=|r||w|=|r|=r$, and $w=\frac{z}{r}$, so $r$ and $w$ are uniquely determined by $z$.

---------

### 12.

If $|z_1+z_2+\cdots+z_{n-1}|\leq |z_1|+|z_2|+\cdots+|z_{n-1}|$, then by Theorem 1.33(e), $|z_1+z_2+\cdots+z_n|\leq |z_1+z_2+\cdots+z_{n-1}|+|z_n|\leq|z_1|+|z_2|+\cdots+|z_{n-1}|+|z_n|$. $|z_1|\leq|z_1|$, so the proof completes by induction.

---------

### 13.

$|x|=|x-y+y|\leq|x-y|+|y|$, so $|x|-|y|\leq|x-y|$; $|y|=|y-x+x|\leq|y-x|+|x|$, so $|y|-|x|\leq|y-x|=|x-y|$. So $\left||x|-|y| \right|\leq|x-y|$.

---------

### 14.

$|1+z|^2+|1-z|^2=(1+z)(1+\bar{z})+(1-z)(1-\bar{z})=1+z+\bar{z}+1+1-z-\bar{z}+1=4$.

---------

### 15.

According to the proof of Theorem 1.35, when the equality holds, $\sum|Ba_j-Cb_j|^2=0$, so $Ba_j-Cb_j=0$ for all $j$, and $a_j=\frac{C}{B}b_j=kb_j$ where $k$ is a constant independent of $j$. If $a_j=kb_j$ for all $j$, $C=\sum kb_j\bar{b_j}=kB$, and $Ba_j-Cb_j=Bkb_j-kBb_j=0$, the equality holds. So $a_j=kb_j$ with $k$ being a constant independent of $j$ is a sufficient and necessary condition for the equality to hold. 

---------

### 16.

(a) If $\V{z}=\frac{\V{x}+\V{y}}{2}+\V{w}$, $\V{w}\cdot(\V{x}-\V{y})=0$, and $|\V{w}|=\sqrt{r^2-\frac{d^2}{4}}$, then $|\V{z}-\V{x}|=|-\frac{\V{x}-\V{y}}{2}+\V{w}|=\sqrt{|\V{w}|^2+|\frac{\V{x}-\V{y}}{2}|^2-2\V{w}\cdot\frac{\V{x}-\V{y}}{2}}=\sqrt{r^2-\frac{d^2}{4}+\frac{d^2}{4}}=r$, and similarly $|\V{z}-\V{y}|=r$. So we want to prove that there are infinitely many $\V{w}$ that satisfy $\V{w}\cdot(\V{x}-\V{y})=0$ and $|\V{w}|=\sqrt{r^2-\frac{d^2}{4}}$. Let $\V{x}-\V{y}=\V{u}\neq0$, $\sqrt{r^2-\frac{d^2}{4}}=s>0$. Let $u_i$ be the coordinate that $u_i\neq0$, and choose other two coordinates $u_j, u_k$(they exist because the dimension $k\geq3$). Let $w_i=au_j+bu_k$, $w_j=-au_i$, $w_k=-bu_i$, and all the other coordinates $=0$. Then $\V{w}\cdot\V{u}=0$, and we want to prove that there are infinitely many $a,b$ that satisfy $|\V{w}|=s$. Substituting, we get \[(au_j+bu_k)^2+(-au_i)^2+(-bu_i)^2=s^2\]
\[(u_i^2+u_k^2)b^2+2u_ju_ka\cdot b+a^2(u_i^2+u_j^2)-s^2=0\]
To solve the quadratic equation for $b$, the discriminant  $\Delta=4u_j^2u_k^2a^2-4(u_i^2+u_k^2)\left[a^2(u_i^2+u_j^2)-k^2 \right]$. When $a^2<\frac{k^2}{u_i^2+u_j^2}$, $\Delta>0$, the solution of $b$ exists, so there are infinitely many $a$ and $b$ satisfying $|\V{w}|=s$. So there are infinitely many $\V{w}$ satisfying $\V{w}\cdot(\V{x}-\V{y})=0$ and $|\V{w}|=\sqrt{r^2-\frac{d^2}{4}}$, so there are infinitely many $\V{z}$ satisfying $|\V{z}-\V{x}|=r$ and $|\V{z}-\V{y}|=r$.
\medskip

(b) Let $\V{z}=\frac{\V{x}+\V{y}}{2}$, then $|\V{z}-\V{x}|=|\V{z}-\V{y}|=|\frac{\V{x}-\V{y}}{2}|=\frac{d}{2}=r$. If $\V{z}'\neq \V{z}$, then $|\V{z}'-\V{z}|=\varepsilon>0$, and $|\V{z}'-\V{x}|\geq|\V{z}'-\V{z}|+|\V{z}-\V{x}|=\varepsilon+r>r$, so $\V{z}'$ cannot satisfy the condition, and $\V{z}$ is unique.
\medskip

(c) If such $\V{z}$ exists, then $2r=|\V{x}-\V{z}|+|\V{z}-\V{y}|\geq|\V{x}-\V{y}|=d$, contradicting with $2r<d$, so the $\V{z}$ cannot exist.

---------

### 17.

$|\V{x}+\V{y}|^2+|\V{x}-\V{y}|^2=\sum(x_i+y_i)^2+\sum(x_i-y_i)^2=2\sum x_i^2+2\sum y_i^2+\sum 2x_iy_i+\sum(-2)x_iy_i=2|\V{x}|^2+2|\V{y}|^2$. It can be geometrically interpreted as the sum of squares of two diagonals of parallelograms being equal to the sum of squares of four sides of parallelograms.

---------

### 18.

If $x_1=x_2=0$, let $y_1=y_2=1$, $y_k=0$ for $k>2$, then $\V{y}\neq0$ and $\V{x}\cdot\V{y}=0$. If one of $x_1,x_2\neq0$, let $y_1=x_2, y_2=-x_1$, $y_k=0$ for $k>2$, then $\V{y}\neq0$ and $\V{x}\cdot\V{y}=0$.

When $k=1$, if $\V{x}\neq0$ and $\V{y}\neq0$, then $\V{x}\cdot\V{y}=x_1y_1\neq0$, so the $\V{y}$ satisfying the condition does not necessary exist.

---------

### 19.

$$
\begin{aligned}
\sum(x_i-a_i)^2 &=4\sum(x_i-b_i)^2\\
\sum3x_i^2-(8b_i-2a_i)x_i+(4b_i^2-a_i^2) &=0\\
\sum3(x_i-\frac{4b_i-a_i}{3})^2+(4b_i^2-a_i^2)-\frac{(4b_i-a_i)^2}{3} &=0\\
\sum3(x_i-\frac{4b_i-a_i}{3})^2 &=\sum\frac{4a_i^2-8a_ib_i+4b_i}{3}\\
\sum(x_i-\frac{4b_i-a_i}{3})^2 &=\sum\frac{4}{9}(b_i-a_i)^2=\sum(\frac{2}{3}(b_i-a_i))^2
\end{aligned}
$$

So if $\V{c}=\frac{4\V{b}-\V{a}}{3}$ and $r=\frac{2}{3}|\V{b}-\V{a}|$, then the two equations are sufficient and necessary conditions for each other.

---------

### 20.

The proof of least-upper-bound property and axioms (A1) to (A3) did not use property (III) and therefore still hold. Let $0^*$ be $\{x|x\in\mathbb{Q},x\leq0 \}$. For every $r\in\alpha$ and $s\in0^*$, $r+s\leq r$, hence $r+s\in\alpha$, so $\alpha+0^*\subset\alpha$. For every $r\in\alpha$, $r=r+0\in\alpha+0^*$, so $\alpha\subset\alpha+0^*$. So $\alpha+0^*=\alpha$, and (A4) holds. If (A5) holds, let $\alpha=\{x|x\in\mathbb{Q},x<1\}$, then there is an $\alpha'$ such that $\alpha+\alpha'=0^*$. So there are $r\in\alpha$ and $s\in\alpha'$ that $r+s=0$, and because $r<1$, $s>-1$. Let $s=-1+\varepsilon$, $\varepsilon>0$, and let $t=1-\frac{\varepsilon}{2}$, then $t\in\alpha$. $s+t\in\alpha'+\alpha=0^*$, so $s+t\leq0$, but $s+t=-1+\varepsilon+1-\frac{\varepsilon}{2}=\frac{\varepsilon}{2}>0$, a contradiction, so (A5) cannot hold.
