---
layout: splash
title: "Mathematical Methods for Physicists Ch7"
permalink: /solutions/math_physics_07
author_profile: false

---

# Chapter 7 Ordinary Differential Equations

{% raw %}

## 7.2 First-Order Equations

### 7.2.1

(a) 

$$
\newcommand{\pdv}[2]{\frac{\partial#1}{\partial#2}}
\newcommand{\V}{\mathbf}
\newcommand{\M}{\mathrm}
\newcommand{\VE}{\hat{\V{e}}}
\begin{aligned}
\frac{1}{I}dI&=-\frac{1}{RC}dt\\
ln\frac{I}{I_0}&=-\frac{t}{RC} \\
I&=I_0e^{-\frac{t}{RC}}
\end{aligned}
$$

(b)

$$
\begin{aligned}
I_0&=\frac{V_0}{R}=0.1\,mA\\
I(100)&=0.1e^{-\frac{10^2}{10^4}}=0.099\,mA
\end{aligned}
$$

----- 

### 7.2.2

$$
\begin{aligned}
\frac{1}{f}df&=-\frac{s}{s^2+1}ds\\
\ln f&=-\frac{1}{2}\ln(s^2+1)+C'\\
f&=\frac{C}{\sqrt{s^2+1}}
\end{aligned}
$$

----- 

### 7.2.3

$$
\begin{aligned}
&-\frac{1}{N^2}dN=kdt\\
&\frac{1}{N}-\frac{1}{N_0}=kt\\
&N=N_0(1+N_0kt)^{-1}=(1+\frac{t}{\tau_0})^{-1}
\end{aligned}
$$

----- 

### 7.2.4

(a)

$$
\begin{aligned}
&\frac{1}{(A_0-C)(B_0-C)}dC=\alpha dt\\
&\frac{1}{A_0-B_0}(-\frac{1}{A_0-C}+\frac{1}{B_0-C})dC=\alpha dt\\
&\frac{1}{A_0-B_0}(\ln\frac{A_0-C}{A_0}-\ln\frac{B_0-C}{B_0})=\alpha t\\
&\frac{A_0-C}{B_0-C}\frac{B_0}{A_0}=e^{(A_0-B_0)\alpha t}\\
&C=\frac{A_0B_0(e^{(A_0-B_0)\alpha t}-1)}{A_0e^{(A_0-B_0)\alpha t}-B_0}
\end{aligned}
$$

(b)

$$
\begin{aligned}
&\frac{1}{(A_0-C)^2}dC=\alpha dt\\
&\frac{1}{A_0-C}-\frac{1}{A_0}=\alpha t\\
&C=\frac{A_0^2\,\alpha t}{1+A_0\alpha t}
\end{aligned}
$$

----- 

### 7.2.5

$$
\begin{aligned}
&-v^{-n}dv=\frac{k}{m}dt\\
&\frac{1}{n-1}(v^{-n+1}-v_0^{-n+1})=\frac{k}{m}t\\
&v=v_0\left(1+(n-1)\frac{k}{m}v_0^{n-1}t\right)^{1/(1-n)}
\end{aligned}
$$

because $\frac{dv}{dt}=\frac{dv}{dx}\frac{dx}{dt}=\frac{dv}{dx}v$, so

$$
\begin{aligned}
&-v^{1-n}dv=\frac{k}{m}dx\\
&\frac{1}{n-2}(v^{2-n}-v_0^{2-n})=\frac{k}{m}x\\
&v=v_0\left(1+(n-2)\frac{k}{m}v_0^{n-2}x\right)^{1/(2-n)}
\end{aligned}
$$

----- 

### 7.2.6

$y=ux$, $dy=udx+xdu$. Substituting,

$$
\begin{aligned}
&\frac{udx+xdu}{dx}=g(u)\\
&xdu=(g(u)-u)dx
\end{aligned}
$$

which is a separable equation in $u$ and $x$.

----- 

### 7.2.7

The equation being exact means that we can find a $\varphi$ such that

$$
\begin{aligned}
d\varphi=\pdv{\varphi}{x}dx+\pdv{\varphi}{y}dy=P(x,y)dx+Q(x,y)dy
\end{aligned}
$$

So

$$
\begin{aligned}
\pdv{\varphi}{x}&=P(x,y),\qquad \varphi=\int_{x_0}^xP(x,y)dx+A(y)\\
\pdv{\varphi}{y}&=Q(x,y),\qquad \varphi=\int_{y_0}^yQ(x,y)dy+B(x)
\end{aligned}
$$

for $x=x_0$,

$$
\begin{aligned}
\varphi=A(y)=\int_{y_0}^yQ(x_0,y)dy+B(x_0)
\end{aligned}
$$

so

$$
\begin{aligned}
\varphi=\int_{x_0}^xP(x,y)dx+\int_{y_0}^yQ(x_0,y)dy+B(x_0)
\end{aligned}
$$

because $d\varphi$ will not change when adding a constant, so we can omit $B(x_0)$, and $\varphi$ becomes

$$
\begin{aligned}
\varphi=\int_{x_0}^xP(x,y)dx+\int_{y_0}^yQ(x_0,y)dy=constant
\end{aligned}
$$

----- 

### 7.2.8

The equation being exact implies $\pdv{P(x,y)}{y}=\pdv{Q(x,y)}{x}$. So

$$
\begin{aligned}
\pdv{\varphi}{x}&=P(x,y)+\int_{y_0}^y\pdv{Q(x_0,y)}{x}dy=P(x,y)\\
\pdv{\varphi}{y}&=\int_{x_0}^x\pdv{P(x,y)}{y}dx+Q(x_0,y)\\
&=\int_{x_0}^x\pdv{Q(x,y)}{x}dx+Q(x_0,y)\\
&=[Q(x,y)-Q(x_0,y)]+Q(x_0,y)=Q(x,y)
\end{aligned}
$$

----- 

### 7.2.9

Eq. 7.12 can be rearranged to

$$
\begin{aligned}
[\alpha(x)p(x)y-\alpha(x)q(x)]dx+\alpha(x)dy&=0=P(x,y)dx+Q(x,y)dy\\
\pdv{P(x,y)}{y}&=\pdv{[\alpha(x)p(x)y-\alpha(x)q(x)]}{y}=\alpha(x)p(x)\\
\pdv{Q(x,y)}{x}&=\pdv{\alpha(x)}{x}=\alpha(x)p(x)
\end{aligned}
$$

so $\pdv{P(x,y)}{y}=\pdv{Q(x,y)}{x}$, which means the equation is exact.

----- 

### 7.2.10

The necessary and
sufficient condition for the equation to be exact is $\pdv{f(x)}{y}=\pdv{(g(x)h(y))}{x}$. But $\pdv{f(x)}{y}=0$, so $\pdv{(g(x)h(y))}{x}=\pdv{g(x)}{x}h(y)=0$. Because $h(y)\neq0$, so it must be $\pdv{g(x)}{x}=0$, which means $g(x)=constant$.

----- 

### 7.2.11

$$
\begin{aligned}
\frac{dy}{dx}&=e^{-\int^xp(t)dt}\left(-p(x)\right)\left(\int^xe^{\int^sp(t)dt}q(s)ds+c \right)+e^{-\int^xp(t)dt}\left(e^{\int^xp(t)dt}q(x)\right)\\
&=-p(x)y+q(x)
\end{aligned}
$$

so

$$
\begin{aligned}
\frac{dy}{dx}+p(x)y=q(x)
\end{aligned}
$$

----- 

### 7.2.12

$$
\begin{aligned}
&\frac{m}{mg-bv}dv=dt\\
&-\frac{m}{b}\ln\frac{mg-bv}{mg-bv_0}=t\\
&mg-bv=(mg-bv_0)e^{-\frac{b}{m}t}\\
&v=\frac{mg}{b}-(\frac{mg}{b}-v_0)e^{-\frac{b}{m}t}
\end{aligned}
$$

If $v_0=0$, the equation become

$$
\begin{aligned}
v=\frac{mg}{b}(1-e^{-\frac{b}{m}t})
\end{aligned}
$$

----- 

### 7.2.13

$$
\begin{aligned}
\frac{1}{N_1}dN_1&=\lambda_1dt\\
\ln\frac{N_1}{N_0}&=-\lambda_1t\\
N_1&=N_0e^{-\lambda_1t}
\end{aligned}
$$

so

$$
\begin{aligned}
\frac{dN_2}{dt}&=\lambda_1N_0e^{-\lambda_1t}-\lambda_2N_2\\
\frac{dN_2}{dt}+\lambda_2N_2&=\lambda_1N_0e^{-\lambda_1t}
\end{aligned}
$$

Let the integrating factor $\alpha$ be

$$
\begin{aligned}
\alpha=e^{\int\lambda_2dt}=e^{\lambda_2t}
\end{aligned}
$$

Multiplying, the equation becomes

$$
\begin{aligned}
\frac{d}{dt}(e^{\lambda_2t}N_2)&=\lambda_1N_0e^{(\lambda_2-\lambda_1)t}\\
e^{\lambda_2t}(N_2-0)&=\frac{\lambda_1}{\lambda_2-\lambda_1}N_0\left(e^{(\lambda_2-\lambda_1)t}-1 \right)
\end{aligned}
$$

So $N_2(t)$ is

$$
\begin{aligned}
N_2=\frac{\lambda_1}{\lambda_2-\lambda_1}N_0(e^{-\lambda_1t}-e^{-\lambda_2t})
\end{aligned}
$$

----- 

### 7.2.14

Let $V$ be the volume, and $r$ be the radius of the drop.
$V\propto r^3$, so $\frac{dV}{dr}\propto r^2$, and $\frac{dV}{dt}=\frac{dV}{dr}\frac{dr}{dt}\propto r^2\frac{dr}{dt}$. Also $\frac{dV}{dt}\propto -r^2$ by the model, so $r^2\frac{dr}{dt}=-kr^2$,
$\frac{dr}{dt}=-k$,
$r=r_0-kt$.

----- 

### 7.2.15

(a) 
$\frac{1}{v}dv=-adt$, $\ln\frac{v}{v_0}=-at$, $v=v_0e^{-at}$.

(b) $\frac{1}{v}dv+adt=0$, $\varphi=\int\frac{1}{v}dv+\int adt=constant$, $\ln v+at=\ln v_0$, $v=v_0\,e^{-at}$.

(c) $v(t)=\frac{C}{\alpha(t)}$, $\alpha(t)=e^{\int adt}=e^{at}$, $v=Ce^{-at}$, $v=v_0e^{-at}$.

----- 

### 7.2.16

(a)
$m\dot{v}=mg-bv^2$. 
Let $v_0=\sqrt{\frac{mg}{b}}$ and rearrange:

$$
\begin{aligned}
\frac{1}{v_0^2-v^2}dv&=\frac{b}{m}dt\\
\frac{1}{2v_0}(\frac{1}{v+v_0}-\frac{1}{v-v_0})dv&=\frac{b}{m}dt\\
\frac{1}{2v_0}\ln\frac{v+v_0}{v_i+v_0}\frac{v_i-v_0}{v-v_0}&=\frac{b}{m}t
\end{aligned}
$$

Let $T=\sqrt{\frac{m}{gb}}$,

$$
\begin{aligned}
&\frac{v+v_0}{v_i+v_0}\frac{v_i-v_0}{v-v_0}=e^{\frac{2t}{T}}\\
&(v_i-v_0)e^{-\frac{t}{T}}v+(v_i-v_0)e^{-\frac{t}{T}}v_0=(v_i+v_0)e^{\frac{t}{T}}v-(v_i+v_0)e^{\frac{t}{T}}v_0\\
&(v_i\sinh{\frac{t}{T}}+v_0\cosh{\frac{t}{T}})v=
(v_i\cosh{\frac{t}{T}}+v_0\sinh{\frac{t}{T}})v_0\\
&v=v_0\frac{v_i+v_0\tanh{\frac{t}{T}}}{v_i\tanh{\frac{t}{T}}+v_0}
\end{aligned}
$$

(b)

$$
\begin{aligned}
v_0=\sqrt{\frac{mg}{b}}=52\;m/s
\end{aligned}
$$

----- 

### 7.2.17

Let $u=xy$, $du=ydx+xdy=ydx+\frac{u}{y}dy$. Substitute $u$ for $x$,

$$
\begin{aligned}
(uy-y)\frac{du-\frac{u}{y}dy}{y}+\frac{u}{y}dy&=0\\
\frac{u-1}{u^2-2u}du&=\frac{1}{y}dy\\
\frac{1}{2}(\frac{1}{u}+\frac{1}{u-2})du&=\frac{1}{y}dy\\
\frac{1}{2}\ln u(u-2)&=\ln y+C'\\
u(u-2)&=Cy^2\\
\frac{x^2y-2x}{y}&=C
\end{aligned}
$$

----- 

### 7.2.18

Let $y=ux$, $dy=udx+xdu$ and substitute $u$ for $y$:

$$
\begin{aligned}
&(x^2-u^2x^2e^u)dx+(x^2+ux^2)e^u(udx+xdu)=0\\
&\frac{1}{x}dx=-\frac{(1+u)e^u}{1+ue^u}du\\
&\ln x=-\ln(1+ue^u)+C'\\
&x(1+ue^u)=C\\
&x+ye^\frac{y}{x}=C
\end{aligned}
$$

## 7.3 ODEs with Constant Coefficients

### 7.3.1

Let $y=e^{mx}$ and substitute:

$$
\begin{aligned}
&m^3-2m^2-m+2=0\\
&(m-2)(m-1)(m+1)=0\\
&y=C_1e^{2x}+C_2e^x+C_3e^{-x}
\end{aligned}
$$

-----

### 7.3.2

Let $y=e^{mx}$ and substitute:

$$
\begin{aligned}
&m^3-2m^2+m-2=0\\
&(m-2)(m-i)(m+i)=0\\
y&=C_1e^{2x}+C_2'e^{ix}+C_3'e^{-ix}\\
&=C_1e^{2x}+C_2\cos x+C_3\sin x
\end{aligned}
$$

-----

### 7.3.3

Let $y=e^{mx}$ and substitute:

$$
\begin{aligned}
&m^3-3m+2=0\\
&(m-1)^2(m+2)=0\\
&y=C_1e^x+C_2xe^x+C_3e^{-2x}
\end{aligned}
$$

-----

### 7.3.4

Let $y=e^{mx}$ and substitute:

$$
\begin{aligned}
&m^2+2m+2=0\\
m&=-1+i,\;-1-i\\
y&=C_1'e^{(-1+i)x}+C_2'e^{(-1-i)x}\\
&=e^{-x}(C_1'e^{ix}+C_2'e^{-ix})\\
&=e^{-x}(C_1\cos x+C_2\sin x)
\end{aligned}
$$

## 7.4 Second-Order Linear ODEs

### 7.4.1

$$
\begin{aligned}
y''+\frac{-2x}{1-x^2}y'+\frac{l(l+1)}{1-x^2}y=0
\end{aligned}
$$

so $P(x)=\frac{-2x}{1-x^2}$, $Q(x)=\frac{l(l+1)}{1-x^2}$.

$$
\begin{aligned}
\lim_{x\to -1}P(x)=\infty,\qquad\lim_{x\to -1}(x+1)P(x)=1,\qquad\lim_{x\to -1}(x+1)^2Q(x)=0
\end{aligned}
$$

so $x=-1$ is a regular singularity.

$$
\begin{aligned}
\lim_{x\to 1}P(x)=\infty,\qquad\lim_{x\to 1}(x-1)P(x)=1,\qquad\lim_{x\to 1}(x-1)^2Q(x)=0
\end{aligned}
$$

so $x=1$ is a regular singularity.

$$
\begin{aligned}
\frac{2z-P(z^{-1})}{z^2}&=\frac{2z}{z^2-1},\qquad\frac{Q(z^{-1})}{z^4}=\frac{l(l+1)}{z^2(z^2-1)}\\
\lim_{z\to0}\frac{Q(z^{-1})}{z^4}&=\infty,\qquad\lim_{z\to0}z\cdot\frac{2z-P(z^{-1})}{z^2}=0\qquad\lim_{z\to0}z^2\cdot\frac{Q(z^{-1})}{z^4}=-l(l+1)
\end{aligned}
$$

so $x=\infty$ is a regular singularity.

-----

### 7.4.2

$$
\begin{aligned}
y''+\frac{1-x}{x}y'+\frac{a}{x}y=0
\end{aligned}
$$

so $P(x)=\frac{1-x}{x}$, $Q(x)=\frac{a}{x}$.

$$
\begin{aligned}
\lim_{x\to0}P(x)=\infty,\qquad\lim_{x\to0}xP(x)=1,\qquad\lim_{x\to0}x^2Q(x)=0
\end{aligned}
$$

so $x=0$ is a regular singularity.

$$
\begin{aligned}
\frac{2z-P(z^{-1})}{z^2}&=\frac{z+1}{z^2},\qquad\frac{Q(z^{-1})}{z^4}=\frac{a}{z^3}\\
\lim_{z\to0}\frac{2z-P(z^{-1})}{z^2}&=\infty,\qquad\lim_{z\to0}z\cdot\frac{2z-P(z^{-1})}{z^2}=\infty
\end{aligned}
$$

so $x=\infty$ is an irregular singularity.

-----

### 7.4.3

$$
\begin{aligned}
y''+\frac{-x}{1-x^2}y'+\frac{n^2}{1-x^2}y=0
\end{aligned}
$$

so $P(x)=\frac{-x}{1-x^2}$, $Q(x)=\frac{n^2}{1-x^2}$.

$$
\begin{aligned}
\lim_{x\to -1}P(x)=\infty,\qquad\lim_{x\to -1}(x+1)P(x)=\frac{1}{2},\qquad\lim_{x\to -1}(x+1)^2Q(x)=0
\end{aligned}
$$

so $x=-1$ is a regular singularity.

$$
\begin{aligned}
\lim_{x\to 1}P(x)=\infty,\qquad\lim_{x\to 1}(x-1)P(x)=\frac{1}{2},\qquad\lim_{x\to 1}(x-1)^2Q(x)=0
\end{aligned}
$$

so $x=1$ is a regular singularity.

$$
\begin{aligned}
\frac{2z-P(z^{-1})}{z^2}&=\frac{2z^2-1}{z(z^2-1)},\qquad\frac{Q(z^{-1})}{z^4}=\frac{n^2}{z^2(z^2-1)}\\
\lim_{z\to0}\frac{2z-P(z^{-1})}{z^2}&=\infty,\qquad\lim_{z\to0}z\cdot\frac{2z-P(z^{-1})}{z^2}=1\qquad\lim_{z\to0}z^2\cdot\frac{Q(z^{-1})}{z^4}=-n^2
\end{aligned}
$$

so $x=\infty$ is a regular singularity.

-----

### 7.4.4

$$
\begin{aligned}
y''-2xy'+2\alpha y=0
\end{aligned}
$$

so $P(x)=-2x$, $Q(x)=2\alpha$. $P(x)$ and $Q(x)$ will not diverge at any finite $x$, so the only possible singularity is at $x=\infty$.

$$
\begin{aligned}
\frac{2z-P(z^{-1})}{z^2}&=\frac{2z^2+2}{z^3},\qquad\frac{Q(z^{-1})}{z^4}=\frac{2\alpha}{z^4}\\
\lim_{z\to0}\frac{2z-P(z^{-1})}{z^2}&=\infty,\qquad\lim_{z\to0}z\cdot\frac{2z-P(z^{-1})}{z^2}=\infty
\end{aligned}
$$

so $x=\infty$ is an irregular singularity.

-----

### 7.4.5

(The $+c$ in the hypergeometric function in Table 7.1 should be $-c$.)

Note that $y''=\frac{d^2y}{dx^2}$, so $y''$ should be transformed to $\frac{1}{(-\frac{1}{2})^2}y'' =4y''$. Similarly $y'$ should be transformed to $\frac{1}{-\frac{1}{2}}y'=-2y'$.  Substitute $x,y'' ,y',a,b,c$ into the hypergeometric function:

$$
\begin{aligned}
\frac{1-x}{2}(\frac{1-x}{2}-1)4y''+\big[(1-l+l+1)\frac{1-x}{2}-1\big](-2y')-l(l+1)y=0
\end{aligned}
$$

Rearrange and multiply by $-1$, we get

$$
\begin{aligned}
(1-x^2)y''-2xy'+l(l+1)=0
\end{aligned}
$$

which is the Legendre's equation.

## 7.5 Series Solutions—Frobenius’ Method

## 7.5.1

(Let the equation be $y'' +P(x)y'+Q(x)y=\mathcal{L}y=0$. There should be more conditions for theorem to hold, for example, $P(x)$ and $Q(x)$ being continuous or analytic at $x=x_0$, or $x_0$ is a regular singular point. We prove for the "analytic" case, while I don't know the correctness or the proof for other cases. $P(x)$ being analytic at $x_0$ means that it is infinitely differentiable at $x_0$, that is, $P^{(n)}(x_0)$ is finite for every $n$.)

If $y_1$ and $y_2$ are two functions satisfying $\mathcal{L}y=0$ and $y(x_0)=y_0$, $y'(x_0)=y'_0$, then $\varphi=y_1-y_2$ satisfies $\mathcal{L}\varphi=0$ and $\varphi(x_0)=0$, $\varphi'(x_0)=0$. Let $x=x_0$, we have 

$$
\begin{aligned}
\varphi''(x_0)+P(x_0)\varphi'(x_0)+Q(x_0)\varphi(x_0)=0
\end{aligned}
$$

The second and third terms vanish, so $\varphi'' (x_0)=0$. Differentiate the equation and let $x=x_0$, we have 

$$
\begin{aligned}
\varphi'''(x_0)+P(x_0)\varphi''(x_0)+\big[P'(x_0)+Q(x_0)\big]\varphi'(x_0)+Q'(x_0)\varphi(x_0)=0
\end{aligned}
$$

All except the first term vanish, so $\varphi''' (x_0)=0$. Continue the process by differentiate the equation $n$ times and let $x=x_0$, we will get the equation of the form 

$$
\begin{aligned}
\varphi^{(n)}(x_0)+\sum_{j=1}^{n-1}a_j\varphi^{(j)}(x_0)=0
\end{aligned}
$$

Because $\varphi(x_0)=\varphi'(x_0)=\cdots=\varphi^{(n-1)}(x_0)=0$, so $\sum_{j=1}^{n-1}a_j\varphi^{(j)}(x_0)=0$, which means $\varphi^{(n)}(x_0)=0$.
So we know that $\varphi^{(n)}(x_0)=0$ for every $n$, while $\varphi(x)=\sum_{n=0}^\infty\frac{(x-x_0)^n}{n!}\varphi^{(n)}(x_0)$, so $\varphi(x)=0$, which means $y_1-y_2=0$, $y_1$ is unique. 

-----

### 7.5.2

Let $y(x)=\sum_{j=0}^\infty a_j(x-x_0)^{s+j}$ and substitute into the equation:

$$
\begin{aligned}
\sum_{j=0}^\infty a_j(s+j)(s+j-1)(x-x_0)^{s+j-2}+\sum_{j=0}^\infty P(x)a_j(s+j)(x-x_0)^{s+j-1}+\sum_{j=0}^\infty Q(x)a_j(x-x_0)^{s+j}=0
\end{aligned}
$$

Because $x_0$ is an ordinary point, which means $P(x_0)$ and $Q(x_0)$ are finite, so we can expand $P(x)$ and $Q(x)$ at $x_0$, that is, $P(x)=\sum_{n=0}^\infty p_n(x-x_0)^n$, $Q(x)=\sum_{m=0}^\infty q_m(x-x_0)^m$. Substitute $P(x)$ and $Q(x)$ into the above equation,

$$
\begin{aligned}
\sum_{j=0}^\infty a_j(s+j)(s+j-1)(x-x_0)^{s+j-2}+\sum_{j=0}^\infty \sum_{n=0}^\infty p_na_j(s+j)(x-x_0)^{s+j-1+n}+\sum_{j=0}^\infty\sum_{m=0}^\infty q_ma_j(x-x_0)^{s+j+m}=0
\end{aligned}
$$

We found that term of the lowest order is $a_0s(s-1)(x-x_0)^{s-2}$, whose coefficient must equal zero, so

$$
\begin{aligned}
s(s-1)=0,\qquad s=0,1
\end{aligned}
$$

-----

### 7.5.3

Substitute $y=\sum_{j=0}^\infty a_jx^{s+j}$ into $y''+\omega^2y=0$, we get

$$
\begin{aligned}
\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}+\sum_{j=0}^\infty\omega^2a_jx^{s+j}=0
\end{aligned}
$$

The coefficient of $x^{s-1}$ is $a_1(s+1)s$, which should equal zero, so when

$$
\begin{aligned}
    &s=0:\qquad && (s+1)s=0,\qquad && a_1=arbitrary\\
    &s=1:\qquad && (s+1)s=2\neq0,\qquad && a_1=0
\end{aligned}
$$

-----

### 7.5.4

Substitute $y=\sum_{j=0}^\infty a_jx^{s+j}$ into the equations:

$$
\begin{aligned}
    &Legendre:\quad && (1-x^2)\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}-2x\sum_{j=0}^\infty a_j(s+j)x^{s+j-1}+l(l+1)\sum_{j=0}^\infty a_jx^{s+j}=0\\
    &Chebyshev:\quad && (1-x^2)\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}-x\sum_{j=0}^\infty a_j(s+j)x^{s+j-1}+n^2\sum_{j=0}^\infty a_jx^{s+j}=0\\
    &Hermite:\quad && \sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}-2x\sum_{j=0}^\infty a_j(s+j)x^{s+j-1}+2\alpha\sum_{j=0}^\infty a_jx^{s+j}=0\\
\end{aligned}
$$

All the three equations have indicial roots $s=0,1$, and the coefficient of $x^{s-1}$ are all $a_1(s+1)s$, which should be zero. So for $s=0$, $a_1$ may be any finite value; for $s=1$, $a_1$ must be set equal to zero.

$$
\begin{aligned}
Bessel:\qquad x^2\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}+x\sum_{j=0}^\infty a_j(s+j)x^{s+j-1}+(x^2-n^2)\sum_{j=0}^\infty a_jx^{s+j}=0\\
\end{aligned}
$$

The indicial roots are $s=\pm n$, and the coefficient of $x^{s+1}$ term is $a_1(s+1+n)(s+1-n)$, which should be zero. $(s+1+n)(s+1-n)=\pm2n+1\neq0$ when $n\neq\pm\frac{1}{2}$, so $a_1$ must be set equal to zero.

-----

### 7.5.5

Substitute $y=\sum_{j=0}^\infty a_jx^{s+j}$ into the equation:

$$
\begin{aligned}
x(x-1)\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}+\big[(1+a+b)x-c \big]\sum_{j=0}^\infty a_j(s+j)x^{s+j-1}+ab\sum_{j=0}^\infty a_jx^{s+j}=0
\end{aligned}
$$

The coefficient of $x^{s-1}$ is $s(s-1+c)=0$, which means $s=0,1-c$. The coefficient of $x^{s+j}$ with $j\geq0$ is 

$$
\begin{aligned}
a_j(s+j)(s+j-1)-a_{j+1}(s+j+1)(s+j)+(1+a+b)a_j(s+j)-c\,a_{j+1}(s+j+1)+ab\,a_j=0
\end{aligned}
$$

Choose $s=0$ for simplicity and rearrange,

$$
\begin{aligned}
a_{j+1}=a_j\frac{(j+a)(j+b)}{(j+1)(j+c)}
\end{aligned}
$$

So

$$
\begin{aligned}
a_j=a_0\frac{a(a+1)\cdots(a+j-1)b(b+1)\cdots(b+j-1)}{j!\,c(c+1)\cdots(c+j-1)}=a_0\frac{(a)_j(b)_j}{j!(c)_j}
\end{aligned}
$$

where we define $(a)_j=a(a+1)\cdots(a+j-1)$, and so do $(b)_j$ and $(c)_j$.
Let $a_0=1$, then the solution is 

$$
\begin{aligned}
y=\sum_{j=0}^\infty\frac{(a)_j(b)_j}{j!(c)_j}x^j=1+\frac{ab}{1!\,c}x+\frac{a(a+1)b(b+1)}{2!\,c(c+1)}x^2+\cdots
\end{aligned}
$$

The inverse of radius of convergence is

$$
\begin{aligned}
R^{-1}=\lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right|=\lim_{n\to\infty}\frac{(n+a)(n+b)}{(n+1)(n+c)}=1 
\end{aligned}
$$

so the series converges for $-1<x<1$. 

At $x=1$, we use the Gauss' test:

$$
\begin{aligned}
\frac{a_n}{a_{n+1}}=\frac{n^2+(1+c)n+c}{n^2+(a+b)n+ab}=1+\frac{1+c-a-b}{n}+\frac{B(n)}{n^2}
\end{aligned}
$$

so the series converges for $1+c-a-b>1$, which is $c>a+b$, and diverges for $1+c-a-b\leq1$, which is $c\leq a+b$.

At $x=-1$, the series is an alternating series, so the series converges if the coefficient monotonically decreases to $0$ for $n\to\infty$. The condition is probably satisfied if $a+b<1+c$, while I don't know how to prove it.

-----

### 7.5.6

Substitute $y=\sum_{j=0}^\infty a_jx^{s+j}$ into the equation:

$$
\begin{aligned}
x\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}+(c-x)\sum_{j=0}^\infty a_j(s+j)x^{s+j-1}-a\sum_{j=0}^\infty a_jx^{s+j}=0
\end{aligned}
$$

The coefficient of $x^{s-1}$ is $s(s-1+c)=0$, which means $s=0,1-c$. The coefficient of $x^{s+j}$ with $j\geq0$ is 

$$
\begin{aligned}
a_{j+1}(s+j+1)(s+j)+c\,a_{j+1}(s+j+1)-a_j(s+j)-a\,a_j=0
\end{aligned}
$$

Choose $s=0$ for simplicity and rearrange,

$$
\begin{aligned}
a_{j+1}=a_j\frac{(j+a)}{(j+1)(j+c)}
\end{aligned}
$$

So

$$
\begin{aligned}
a_j=a_0\frac{a(a+1)\cdots(a+j-1)}{j!\,c(c+1)\cdots(c+j-1)}=a_0\frac{(a)_j}{j!(c)_j}
\end{aligned}
$$

Let $a_0=1$, then the solution is 

$$
\begin{aligned}
y=\sum_{j=0}^\infty\frac{(a)_j}{j!(c)_j}x^j=1+\frac{a}{1!\,c}x+\frac{a(a+1)}{2!\,c(c+1)}x^2+\cdots
\end{aligned}
$$

The inverse of radius of convergence is

$$
\begin{aligned}
R^{-1}=\lim_{n\to\infty}\left|\frac{a_{n+1}}{a_n}\right|=\lim_{n\to\infty}\frac{(n+a)}{(n+1)(n+c)}=0 
\end{aligned}
$$

so $R=\infty$, which means the series converges for every $x$.

-----

### 7.5.7

Let $u=\sum_{j=0}^\infty a_j\xi^{s+j}$ and substitute:

$$
\begin{aligned}
\sum_{j=0}^\infty a_j(s+j)^2\xi^{s+j-1}+(\frac{1}{2}E\xi+\alpha-\frac{m^2}{4\xi}-\frac{1}{4}F\xi^2)\sum_{j=0}^\infty a_j\xi^{s+j}=0
\end{aligned}
$$

The coefficients of each order should be zero, so

$$
\begin{aligned}
    &\xi^{s-1}:\quad && a_0s^2-\frac{m^2}{4}a_0=0 && s=\pm\frac{m}{2}=\frac{m}{2}\\
    & \xi^s:\quad && a_1(\frac{m}{2}+1)^2+\alpha a_0-\frac{m^2}{4}a_1=0\quad && a_1=a_0\frac{-\alpha}{1+m}\\
    & \xi^{s+1}:\qquad && a_2(\frac{m}{2}+2)^2+\frac{E}{2}a_0+\alpha a_1-\frac{m^2}{4}a_2=0\qquad && a_2=a_o\left[\frac{\alpha^2}{2(m+1)(m+2)}-\frac{E}{4(m+2)} \right]\\
\end{aligned}
$$

so

$$
\begin{aligned}
y=a_0\xi^{\frac{m}{2}}\left\{1-\frac{\alpha}{m+1}\xi+\left[\frac{\alpha^2}{2(m+1)(m+2)}-\frac{E}{4(m+2)} \right]+\cdots \right\}
\end{aligned}
$$

-----

### 7.5.8

Let $u=\sum_{j=0}^\infty a_j\eta^{s+j}$ and substitute:

$$
\begin{aligned}
\sum_{j=0}^\infty a_j(s+j)(s+j-1)\eta^{s+j-2}-\sum_{j=0}^\infty a_j(s+j)(s+j+1)\eta^{s+j}+\alpha\sum_{j=0}^\infty a_j\eta^{s+j}+\beta\eta^2\sum_{j=0}^\infty a_j\eta^{s+j}=0
\end{aligned}
$$

The coefficients of each order should be zero, so

$$
\begin{aligned}
    & \eta^{s-2}:\qquad && a_0s(s-1)=0,\qquad && s=0,1\quad\textit{(choose $s=1$)}\\
    & \eta^{s-1}:\qquad && a_1(s+1)s=0,\qquad && a_1=0\\
    & \eta^{s}:\qquad && a_2(s+2)(s+1)-a_0s(s+1)+\alpha a_0=0,\qquad && a_2=a_0\frac{2-\alpha}{6}\\
    & \eta^{s+1}:\qquad && a_3(s+3)(s+2)-a_1(s+1)(s+2)+\alpha a_1=0,\qquad && a_3=0\\
    & \eta^{s+2}:\qquad && a_4(s+4)(s+3)-a_2(s+2)(s+3)+\alpha a_2+\beta a_0=0,\qquad && a_4=a_0\left[\frac{(12-\alpha)(2-\alpha)}{120}-\frac{\beta}{20}\right]\\
\end{aligned}
$$

so

$$
\begin{aligned}
y=a_0\eta\left\{1+\frac{2-\alpha}{6}\eta^2+\left[\frac{(12-\alpha)(2-\alpha)}{120}-\frac{\beta}{20} \right]\eta^4+\cdots \right\}
\end{aligned}
$$

-----

### 7.5.9

Let $\varphi=\sum_{j=0}^\infty a_jx^{s+j}$ and substitute (expand $e^{-ax}$ for small $x$):

$$
\begin{aligned}
\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}+E'\sum_{j=0}^\infty a_jx^{s+j}-\frac{A'(1-ax+\frac{a^2x^2}{2}-\cdots)}{x}\sum_{j=0}^\infty a_jx^{s+j}
\end{aligned}
$$

The coefficients of each order should be zero, so

$$
\begin{aligned}
    & x^{s-2}:\qquad && a_0s(s-1)=0,\qquad && s=0,1\quad\textit{(choose $s=1$)}\\
    & x^{s-1}:\qquad && a_1(s+1)s-A'a_0-0,\qquad && a_1=a_0\frac{A'}{2}\\
    & x^{s}:\qquad && a_2(s+2)(s+1)+E'a_0-A'a_1+A'a\,a_0=0 ,\qquad && a_2=\frac{a_0}{6}(\frac{A'^2}{2}-E'-aA') \\
\end{aligned}
$$

so

$$
\begin{aligned}
\varphi=a_0\left\{x+\frac{A'}{2}x^2+\frac{1}{6}(\frac{A'^2}{2}-E'-aA')x^3+\cdots \right\}
\end{aligned}
$$

-----

### 7.5.10

Substitute $y=\sum_{j=0}^\infty a_jx^{s+j}$ into the equation:

$$
\begin{aligned}
\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}+\frac{1}{x^2}\sum_{j=0}^\infty a_j(s+j)x^{s+j-1}-\frac{2}{x^2}\sum_{j=0}^\infty a_jx^{s+j}=0
\end{aligned}
$$

The coefficient of $x^{s-3}$ is $a_0s=0$, which means $s=0$. The coefficient of $x^{s+j-2}$ with $j\geq0$ is 

$$
\begin{aligned}
&a_j(s+j)(s+j-1)+a_{j+1}(s+j+1)-2a_j=0\\
&a_{j+1}=a_j\frac{2-j(j-1)}{j+1}
\end{aligned}
$$

So $a_1=a_0\frac{2}{1}=2a_0,\;a_2=a_1\frac{2}{2}=2a_0,\;a_3=a_2\frac{2-2}{3}=0,\;a_j=0$ for $j\geq4$. Therefore, $y=a_0(1+2x+2x^2)$, substitute into the equation,

$$
\begin{aligned}
4+\frac{1}{x^2}(4x+2)-\frac{2}{x^2}(1+2x+2x^2)=0
\end{aligned}
$$

so it is indeed a solution.

-----

### 7.5.11

Let $I_0(x)=\frac{e^x}{\sqrt{2\pi x}}f(x)$, then

$$
\begin{aligned}
    & \frac{d}{dx}I_0(x)=\frac{e^x}{\sqrt{2\pi x}}\left[(1-\frac{1}{2}x^{-1})f(x)+f'(x)\right]\\
    & \frac{d^2}{dx^2}I_0(x)=\frac{e^x}{\sqrt{2\pi x}}\left[(1-x^{-1}+\frac{3}{4}x^{-2})f(x)+(2-x^{-1})f'(x)+f''(x) \right]\\
\end{aligned}
$$

Substitute into the equation and eliminate $\frac{e^x}{\sqrt{2\pi x}}$, we get

$$
\begin{aligned}
x^2f''(x)+2x^2f'(x)+\frac{1}{4}f(x)=0
\end{aligned}
$$

Let $f(x)=\sum_j b_jx^{-j}$ and substitute, we get

$$
\begin{aligned}
x^2\sum_j b_j j(j+1)x^{-j-2}+2x^2\sum_j b_j(-j)x^{-j-1}+\frac{1}{4}\sum_j b_jx^{-j}=0
\end{aligned}
$$

The coefficient of $x^{-j}$ must vanish, so

$$
\begin{aligned}
&b_jj(j+1)-2b_{j+1}(j+1)+\frac{1}{4}b_j=0\\
&b_{j+1}=b_j\frac{j(j+1)+\frac{1}{4}}{2(j+1)}
\end{aligned}
$$

Let $b_0=1$, then $b_1=\frac{1}{8}b_0=\frac{1}{8}$, $b_2=\frac{9}{16}b_1=\frac{9}{128}$.

-----

### 7.5.12

Use the recursive relation in Exercise 8.3.1 and write a program for calculation, we have

$$
\begin{aligned}
    & \textit{sum to } x^k\qquad && x=0.95\qquad && x=0.99\qquad && x=1.00
    \\
    & x^{200}\qquad && 0.21543\qquad && -0.255451\qquad && -0.650013 \\
    & x^{400}\qquad && 0.215429\qquad && -0.268429\qquad && -0.85409 \\
    & x^{600}\qquad && 0.215429\qquad && -0.269403\qquad && -0.973583 \\
    & x^{800}\qquad && 0.215429\qquad && -0.269494\qquad && -1.0584 \\
    & x^{1000}\qquad && 0.215429\qquad && -0.269504\qquad && -1.1242 \\
    & x^{1200}\qquad && 0.215429\qquad && -0.269505\qquad && -1.17797 \\
    & x^{1400}\qquad && 0.215429\qquad && -0.269505\qquad && -1.22343 \\
    & x^{1600}\qquad && 0.215429\qquad && -0.269505\qquad && -1.26282 \\
    & x^{1800}\qquad && 0.215429\qquad && -0.269505\qquad && -1.29756 \\
    & x^{2000}\qquad && 0.215429\qquad && -0.269505\qquad && -1.32864 \\
\end{aligned}
$$

-----

### 7.5.13

(a)
Use the recursive relation in Exercise 8.3.3

$$
\begin{aligned}
a_{j+2}=2a_j\frac{j-\alpha}{(j+1)(j+2)}\qquad\textit{($j$ odd)}
\end{aligned}
$$

Let $\alpha=0$ and $a_1=1$, write a program to calculate $\sum_{j\;odd}a_jx^j$ (for simplicity, we cut the calculation when the last term is less than $10^{-6}$, which is a stricter condition than that in the problem). Note that

$$
\begin{aligned}
\frac{a_{j+2}\,x^{j+2}}{a_j\,x^j}=\frac{2jx^2}{(j+1)(j+2)}<\frac{2x^2}{j}
\end{aligned}
$$

so if $a_k$ is the first term after truncation, then the sum of remaining terms is less than the infinite geometric series with $a_k$ as the first term and $\frac{2x^2}{j}$ as the ratio, which is

$$
\begin{aligned}
\frac{a_k}{1-\frac{2x^2}{j}}
\end{aligned}
$$

This can set the upper bound of the error of the summation.

$$
\begin{aligned}
    & x && \textit{partial sum}\qquad && \textit{truncate at}\qquad && \textit{error} && \textit{upper bound}\\
    & 1\qquad && 1.4626516\qquad && a_{19}x^{19}=1.45\times10^{-7}\qquad && 2\times10^{-7}\qquad && 1.4626518\\
    & 2\qquad && 16.4526271\qquad && a_{37}x^{37}=5.80\times10^{-7}\qquad && 8\times10^{-7}\qquad && 16.4526279\\
    & 3\qquad && 1444.5451221\qquad && a_{65}x^{65}=6.02\times10^{-7}\qquad && 9\times10^{-7}\qquad && 1444.5451230
\end{aligned}
$$

(b)
Expand $e^{x^2}$ and integrate:

$$
\begin{aligned}
e^{x^2}&=\sum_{n=0}^\infty \frac{x^{2n}}{n!}\\
\int_0^x e^{x^2}dx&=\sum_{n=0}^\infty\frac{x^{2n+1}}{n!(2n+1)}=\sum_{j\;odd}a_jx^j
\end{aligned}
$$

where $j=2n+1$, so $a_j=\frac{1}{(\frac{j-1}{2})!j}$. Therefore, $a_1=1$, and

$$
\begin{aligned}
\frac{a_{j+2}}{a_j}=\frac{(\frac{j-1}{2})!j}{(\frac{j+1}{2})!(j+2)}=\frac{2j}{(j+1)(j+2)}
\end{aligned}
$$

which is the recursive relation of Hermite series $y_{odd}(\alpha=0)$, so the series is equal to $\int_0^x e^{x^2}dx$.

(c)

$$
\begin{aligned}
\int_0^1 e^{x^2}dx&=1.46265175\\
\int_0^2 e^{x^2}dx&=16.45262777\\
\int_0^3 e^{x^2}dx&=1444.54512289
\end{aligned}
$$

## 7.6 Other Solutions

### 7.6.1

If $\V{A}=a\VE_x+b\VE_y+c\VE_z=0$, then $\V{A}\cdot\V{A}=a^2+b^2+c^2=0$, so $a=b=c=0$, which means $\VE_x,\VE_y,\VE_z$ are linearly independent.

-----

### 7.6.2

$$
\begin{aligned}
a\V{A}+b\V{B}+c\V{C}=
\begin{pmatrix}
aA_1+bB_1+cC_1\\
aA_1+bB_1+cC_1\\
aA_3+bB_3+cC_3
\end{pmatrix}=
\begin{pmatrix}
0\\0\\0
\end{pmatrix}
\end{aligned}
$$

so

$$
\begin{aligned}
\begin{pmatrix}
A_1&B_1&C_1\\
A_2&B_2&C_2\\
A_3&B_3&C_3\\
\end{pmatrix}
\begin{pmatrix}
a\\b\\c
\end{pmatrix}=
\begin{pmatrix}
0\\0\\0
\end{pmatrix}
\end{aligned}
$$

Let the square matrix be $\M{M}$. $a,b,c$ have non-trivial solution if and only if $\det(\M{M})=0$, so the sufficient and necessary condition for the vectors to be linearly independent is $\det(\M{M})\neq0$. Note that $\det(\M{M})=\V{A}\cdot\V{B}\times\V{C}$, so the two criterions is equivalent.

-----

### 7.6.3

$\frac{d}{dx}(\frac{x^n}{n!})=\frac{x^{n-1}}{(n-1)!}$, so the Wronskian is 

$$
\renewcommand{\arraystretch}{1.5}
\begin{aligned}
W=
\begin{vmatrix}
1&\frac{x^1}{1!}&\frac{x^2}{2!}& &\frac{x^N}{N!}\\
0&1&\frac{x^1}{1!}&\cdots&\frac{x^{N-1}}{(N-1)!}\\
0&0&1& &\frac{x^{N-2}}{(N-2)!}\\
 &\vdots& &\ddots&\vdots\\
0&0&0&\cdots&1\\
\end{vmatrix}=1\neq0
\end{aligned}
$$

which means the functions are linearly independent.

-----

### 7.6.4

$$
\begin{aligned}
\begin{vmatrix}
y_1&y_2\\
y'_1&y'_2\\
\end{vmatrix}=
y_1y_2'-y_1'y_2=0
\end{aligned}
$$

so $\frac{y_1'}{y_1}=\frac{y_2'}{y_2}$, $\ln y_1=\ln y_2+\ln c$, $y_1=cy_2$.

-----

### 7.6.5

$W(x_0)=W(x_0+\varepsilon)=0$, so

$$
\begin{aligned}
    & W'(x_0)=\lim_{\varepsilon\to0}\frac{W(x_0+\varepsilon)-W(x_0)}{\varepsilon}=0\\
    & W(x_0)=constant=0
\end{aligned}
$$

so the Wronskian is zero for all $x$, and the functions are linearly dependent.

-----

### 7.6.6

$$
\begin{aligned}
W=\begin{vmatrix}
\sin x & e^x & e^{-x}\\
\cos x & e^x & -e^{-x}\\
-\sin x & e^x & e^{-x}
\end{vmatrix}
=4\sin x=0\qquad
\textit{for $x=\pm n\pi,\;n=0,1,2,\cdots$}
\end{aligned}
$$

-----

### 7.6.7

The functions must be differentiable for the Wronskian to be valid, but $\vert x\vert$ is not differentiable at $x=0$.

-----

### 7.6.8

$\cosh x=\frac{e^x+e^{-x}}{2}=\frac{1}{2}(e^x+\frac{1}{e^x})$, so between $\cosh x$ and $e^x$ there is a dependence which is not linear.

-----

### 7.6.9

Let $W=P_n(x)Q'_n(x)-P'_n(x)Q_n(x)=0$, then by Eq. 7.60 we have 

$$
\begin{aligned}
W'&=-\frac{-2x}{1-x^2}W\\
\frac{1}{W}dW&=\frac{2x}{1-x^2}dx\\
\ln W&=-\ln(1-x^2)+\ln A_n\\
W&=\frac{A_n}{1-x^2}
\end{aligned}
$$

-----

### 7.6.10

Let $y_1,y_2,y_3$ be three solutions of the equation, so $y''_i+P(x)y'_i+Q(x)y_i=0$, $i=1,2,3$. The wronskian is

$$
\begin{aligned}
W&=\begin{vmatrix}
y_1 & y_2 & y_3 \\
y'_1 & y'_2 & y'_3 \\
y''_1 & y''_2 & y''_3 
\end{vmatrix}\\
&=\begin{vmatrix}
y_1 & y_2 & y_3 \\
y'_1 & y'_2 & y'_3 \\
-P(x)y'_1-Q(x)y_1 & -P(x)y'_2-Q(x)y_2 & -P(x)y'_3-Q(x)y_3 
\end{vmatrix}\\
&=-P(x)\begin{vmatrix}
y_1 & y_2 & y_3 \\
y'_1 & y'_2 & y'_3 \\
y'_1 & y'_2 & y'_3 
\end{vmatrix}-Q(x)
\begin{vmatrix}
y_1 & y_2 & y_3 \\
y'_1 & y'_2 & y'_3 \\
y_1 & y_2 & y_3 
\end{vmatrix}=0
\end{aligned}
$$

so the Wronskian is zero for all $x$ and the three solutions are linearly dependent.

-----

### 7.6.11

(a)
The equation is self-adjoint, so $p'(x)=q(x)$ (Eq. 8.9). Therefore,

$$
\begin{aligned}
W'(x)&=-\frac{q(x)}{p(x)}W(x)=-\frac{p'(x)}{p(x)}W(x)\\
\frac{W'(x)}{W(x)}&=-\frac{p'(x)}{p(x)}\\
\ln W(x)&=-\ln p(x)+\ln C\\
W(x)&=\frac{C}{p(x)}
\end{aligned}
$$

(b)

$$
\begin{aligned}
y_1^2\frac{d}{dx}(\frac{y_2}{y_1})&=y_1y'_2-y'_1y_2=W(x)=\frac{C}{p(x)}\\
\frac{d}{dx}(\frac{y_2}{y_1})&=\frac{C}{p(x)[y_1(x)]^2}\\
y_2(x)&=Cy_1(x)\int^x\frac{dt}{p(t)[y_1(t)]^2}
\end{aligned}
$$

-----

### 7.6.12

$$
\begin{aligned}
y&=e^{-\frac{1}{2}\int^xP(t)dt}z\\
y'&=e^{-\frac{1}{2}\int^xP(t)dt}\Big(z'-\frac{1}{2}zP(x)\Big)\\
y''&=e^{-\frac{1}{2}\int^xP(t)dt}\left[z''-P(x)z'+\Big(\frac{1}{4}P^2(x)-\frac{1}{2}P'(x)\Big)z \right]
\end{aligned}
$$

Substitute into $y''+P(x)y'+Q(x)y=0$ and eliminate $e^{-\frac{1}{2}\int^xP(t)dt}$, we get

$$
\begin{aligned}
z''+\left[Q(x)-\frac{1}{2}P'(x)-\frac{1}{4}P^2(x) \right]z=0
\end{aligned}
$$

-----

### 7.6.13

The Laplacian in spherical polar coordinates of $\varphi(r)$ is $\frac{1}{r^2}\frac{d}{dr}\left[r^2\frac{d\varphi(r)}{dr}\right]=\varphi''(r)+\frac{2}{r}\varphi'(r)$. 
Use the substitution in Exercise 7.6.12:

$$
\begin{aligned}
\varphi(r)=ze^{-\frac{1}{2}\int^r\frac{2}{t}dt}=ze^{-\ln r}=\frac{z}{r}
\end{aligned}
$$

So $z=r\varphi(r)$, and the Laplacian becomes 

$$
\begin{aligned}
\frac{1}{r}\left[z''+\Big(0-\frac{1}{2}(-\frac{2}{r^2})-\frac{1}{4}\frac{4}{r^2}\Big)z \right]=\frac{1}{r}z''=\frac{1}{r}\frac{d^2}{dr^2}[r\varphi(r)]
\end{aligned}
$$

which corresponds to the results from Exercise 3.10.34.

-----

### 7.6.14

$$
\begin{aligned}
y_2(x)&=y_1(x)\int^x\frac{e^{-\int^sP(t)dt}}{[y_1(s)]^2}ds\\
y_2'(x)&=y_1'(x)\int^x\frac{e^{-\int^sP(t)dt}}{[y_1(s)]^2}ds+y_1(x)\frac{e^{-\int^xP(t)dt}}{[y_1(x)]^2}\\
y_2''(x)&=y_1''(x)\int^x\frac{e^{-\int^sP(t)dt}}{[y_1(s)]^2}ds+2y_1'(x)\frac{e^{-\int^xP(t)dt}}{[y_1(x)]^2}+y_1(x)\frac{e^{-\int^xP(t)dt}\big[-P(x)[y_1(x)]^2-2y_1(x)y_1'(x)\big]}{[y_1(x)]^4}\\
&=y_1''(x)\int^x\frac{e^{-\int^sP(t)dt}}{[y_1(s)]^2}ds-\frac{e^{-\int^xP(t)dt}P(x)}{y_1(x)}
\end{aligned}
$$

so

$$
\begin{aligned}
&y_2''(x)+P(x)y_2'(x)+Q(x)y_2(x)\\
=&y_1''(x)\int^x\frac{e^{-\int^sP(t)dt}}{[y_1(s)]^2}ds+P(x)y_1'(x)\int^x\frac{e^{-\int^sP(t)dt}}{[y_1(s)]^2}ds+Q(x)y_1(x)\int^x\frac{e^{-\int^sP(t)dt}}{[y_1(s)]^2}ds\\
=&\big[y_1''(x)+P(x)y_1'(x)+Q(x)y_1(x)\big]\int^x\frac{e^{-\int^sP(t)dt}}{[y_1(s)]^2}ds=0
\end{aligned}
$$

-----

### 7.6.15

Inclusion of lower limits will introduce a constant to the integral, so the function become

$$
\begin{aligned}
y_3(x)&=y_1(x)\left[\int^x\frac{e^{-\int^sP(t)dt+a}}{[y_1(s)]^2}ds+b\right]\\
&=e^ay_1(x)\int^x\frac{e^{-\int^sP(t)dt}}{[y_1(s)]^2}ds+by_1(x)\\
&=a'y_2(x)+b'y_1(x)
\end{aligned}
$$

which is a linear combination of $y_1$ and $y_2$, so no new independent solution is generated.

-----

### 7.6.16

From Eq. 7.67,

$$
\begin{aligned}
y_2=r^m\int^r\frac{e^{-\int^s\frac{1}{t}dt}}{(s^m)^2}ds=r^m\int^rs^{-1-2m}ds=r^m\frac{r^{-2m}}{-2m}\propto r^{-m}
\end{aligned}
$$

so $r^{-m}$ is the second solution.

-----

### 7.6.17

Use equation 7.67,

$$
\begin{aligned}
y_2(x)&=y_1(x)\int^x\frac{e^{-\int^{x_2}0\cdot dx_1}}{[y_1(x_2)]^2}dx_2\\
&=y_1(x)\int^x(x_2-\frac{x_2^3}{3!}+\frac{x_2^5}{5!}-\cdots)^{-2}dx_2\\
&=y_1(x)\int^xx_2^{-2}(1-\frac{x_2^2}{3!}+\frac{x_2^4}{5!}-\cdots)^{-2}dx_2\\
&=y_1(x)\int^xx_2^{-2}(1+c_2x_2^2+c_4x_2^4+\cdots)dx_2
\end{aligned}
$$

so there is no $x_2^{-1}$ term in the integral, and therefore $c_n=0$.

-----

### 7.6.18

From Eq. 7.49, the first solution of Bessel’s equation is

$$
\begin{aligned}
y_1=\sum_{j=0}^\infty(-1)^j\frac{1}{j!(n+j)!}(\frac{x}{2})^{n+2j}=x^n(b_0+b_2x^2+b_4x^4+\cdots)
\end{aligned}
$$

so by using Eq. 7.67, the second solution is

$$
\begin{aligned}
y_2(x)&=y_1(x)\int^x\frac{e^{-\int^{x_2}\frac{1}{x_1}\cdot dx_1}}{[y_1(x_2)]^2}dx_2\\
&=y_1(x)\int^xx_2^{-1-2n}(b_0+b_2x^2+b_4x^4+\cdots)^{-2}dx_2\\
&=y_1(x)\int^xx_2^{-1-2n}(c_0+c_2x^2+c_4x^4+\cdots)dx_2
\end{aligned}
$$

All the terms in the integral have the form $x_2^{-1-2n+2k}$, where $k$ is an integer, but $n$ is not an integer, so $x_2^{-1-2n+2k}\neq x^{-1}$, which means there is no $x_2^{-1}$ term in the integral, and therefore $y_2$ does not contain a logarithmic term.

-----

### 7.6.19

(a)

$$
\begin{aligned}
y_2(x)&=y_1(x)\int^x\frac{e^{-\int^{x_2}-2x_1dx_1}}{[y_1(x_2)]^2}dx_2
=\int^xe^{x_2^2}dx_2\\
&=\int^x\left(\sum_{n=0}^\infty\frac{x_2^{2n}}{n!}\right)dx_2=\sum_{n=0}^\infty\frac{x^{2n+1}}{(2n+1)n!}\\
&=x\sum_{j\;even}\frac{x^j}{(j+1)(\frac{j}{2})!}=x\sum_{j\;even}a_jx^j
\end{aligned}
$$

where we use the substitution $j=2n$. So

$$
\begin{aligned}
\frac{a_{j+2}}{a_j}=\frac{1}{\frac{(j+3)}{(j+1)}\frac{(j+2)}{2}}=\frac{2(j+1)}{(j+2)(j+3)}
\end{aligned}
$$

which is the recursive relation of $y_{odd}$ (Exercise 8.3.3), so $y_2=y_{odd}$.

(b)

$$
\begin{aligned}
y_2(x)&=y_1(x)\int^x\frac{e^{-\int^{x_2}-2x_1dx_1}}{[y_1(x_2)]^2}dx_2
=x\int^xx_2^{-2}e^{x_2^2}dx_2\\
&=x\int^x\left(\sum_{n=0}^\infty\frac{x_2^{2n-2}}{n!}\right)dx_2=x\sum_{n=0}^\infty\frac{x^{2n-1}}{(2n-1)n!}\\
&=\sum_{j\;even}\frac{x^j}{(j-1)(\frac{j}{2})!}=\sum_{j\;even}a_jx^j
\end{aligned}
$$

where we use the substitution $j=2n$. So

$$
\begin{aligned}
\frac{a_{j+2}}{a_j}=\frac{1}{\frac{(j+1)}{(j-1)}\frac{(j+2)}{2}}=\frac{2(j-1)}{(j+1)(j+2)}
\end{aligned}
$$

which is the recursive relation of $y_{even}$ (Exercise 8.3.3), so $y_2=y_{even}$.

-----

### 7.6.20

$$
\begin{aligned}
y_2(x)&=y_1(x)\int^x\frac{e^{-\int^s\frac{1-t}{t}dt}}{[y_1(s)]^2}ds\\
&=\int^xe^{-(\ln s-s)}ds=\int^x\frac{e^s}{s}ds\\
&=\int^x\left(\sum_{n=0}^\infty\frac{s^{n-1}}{n!}\right)ds=\ln x+\sum_{n=1}^\infty\frac{x^n}{n\cdot n!}
\end{aligned}
$$

-----

### 7.6.21

(a)

$$
\begin{aligned}
y_2(x)=\int^x\left(\sum_{n=0}^\infty\frac{s^{n-1}}{n!}\right)ds=\ln x+\sum_{n=1}^\infty\frac{x^n}{n\cdot n!}
\end{aligned}
$$

(b)

$$
\begin{aligned}
y_2'&=\frac{e^x}{x}\\
y_2''&=\frac{e^x}{x}(1-\frac{1}{x})\\
xy_2''+(1-x)y_2'&=\frac{e^x}{x}(x-1+1-x)=0
\end{aligned}
$$

(c)

$$
\begin{aligned}
y_2'&=\frac{1}{x}+\sum_{n=1}^\infty\frac{x^{n-1}}{n!}\\
y_2''&=-\frac{1}{x^2}+\sum_{n=2}^\infty\frac{(n-1)x^{n-2}}{n!}\\
xy_2''+(1-x)y_2'&=-\frac{1}{x}+\sum_{n=2}^\infty\frac{(n-1)x^{n-1}}{n!}+\frac{1}{x}+\sum_{n=1}^\infty\frac{x^{n-1}}{n!}-1-\sum_{n=1}^\infty\frac{x^n}{n!}\\
&=\sum_{n=1}^\infty\frac{nx^n}{(n+1)!}+\sum_{n=1}^\infty\frac{x^n}{(n+1)!}+1-1-\sum_{n=1}^\infty\frac{x^n}{n!}\\
&=\sum_{n=1}^\infty\left(\frac{n}{(n+1)!}+\frac{1}{(n+1)!}-\frac{1}{n!}\right)x^n=0
\end{aligned}
$$

-----

### 7.6.22

(a)

$$
\begin{aligned}
y_2(x)&=y_1(x)\int^x\frac{e^{-\int^s\frac{-t}{1-t^2}dt}}{[y_1(s)]^2}ds\\
&=\int^xe^{-\frac{1}{2}\ln(1-s^2)}ds=\int^x\frac{1}{\sqrt{1-s^2}}ds=\sin^{-1}x
\end{aligned}
$$

(b)

$$
\begin{aligned}
(1-x^2)\frac{dy'}{dx}&=xy'\\
\frac{1}{y'}dy'&=\frac{x}{1-x^2}dx\\
\ln y'&=-\frac{1}{2}\ln(1-x^2)\\
y'&=\frac{1}{\sqrt{1-x^2}}\\
y&=\int\frac{1}{\sqrt{1-x^2}}dx=\sin^{-1}x
\end{aligned}
$$

-----

### 7.6.23

$$
\begin{aligned}
y_2(x)&=y_1(x)\int^x\frac{e^{-\int^s\frac{-t}{1-t^2}dt}}{[y_1(s)]^2}ds\\
&=x\int^x\frac{e^{-\frac{1}{2}\ln(1-s^2)}}{s^2}ds=x\int^x\frac{1}{s^2\sqrt{1-s^2}}ds=x\frac{-\sqrt{1-x^2}}{x}=-\sqrt{1-x^2}
\end{aligned}
$$

-----

### 7.6.24

(a)
Let $y_1(r)=\sum_{j=0}^\infty a_jr^{s+j}$ and substitute:

$$
\begin{aligned}
-\frac{\hbar^2}{2m}\sum_{j=0}^\infty a_j(s+j)(s+j-1)r^{s+j-2}+l(l+1)\frac{\hbar^2}{2m}r^{-2}\sum_{j=0}^\infty a_jr^{s+j}+(\frac{b_{-1}}{r}+b_0+b_1r+\cdots-E)\sum_{j=0}^\infty a_jr^{s+j}=0
\end{aligned}
$$

The coefficient of $r^{s-2}$ is

$$
\begin{aligned}
&-\frac{\hbar^2}{2m}a_0s(s-1)+l(l+1)\frac{\hbar^2}{2m}a_0=0\\
&s^2-s-l(l+1)=0\\
&s=l+1,-l
\end{aligned}
$$

so

$$
\begin{aligned}
y_1(x)=a_0r^{l+1}+a_1r^{l+2}+\cdots
\end{aligned}
$$

(b)

$$
\begin{aligned}
y_2(x)&=y_1(x)\int^x\frac{e^{-\int^s0dt}}{[y_1(s)]^2}ds\\
&=(a_0r^{l+1}+a_1r^{l+2}+\cdots)\int^x(a_0s^{l+1}+a_1s^{l+2}+\cdots)^{-2}ds\\
&=(a_0r^{l+1}+a_1r^{l+2}+\cdots)\int^xa_0^{-2}s^{-2l-2}(1+c_1s+c_2s^{2}+\cdots)ds\\
&=(a_0r^{l+1}+a_1r^{l+2}+\cdots)(k_0r^{-2l-1}+k_1r^{-2l}+\cdots)\\
&=p_0r^{-l}+p_1r^{-l+1}+\cdots
\end{aligned}
$$

where $p_0=-\frac{1}{a_0(2l+1)}\neq0$, so $y_2(x)$ diverges at the origin as $r^{-l}$.

-----

### 7.6.25

$$
\begin{aligned}
y_2'(x)&=y_1'(x)f(x)+y_1(x)f'(x)\\
y_2''(x)&=y_1''(x)f(x)+2y_1'(x)f'(x)+y_1(x)f''(x)
\end{aligned}
$$

Substitute into $y_2'' +P(x)y_2'+Q(x)y_2=0$ and rearrange:

$$
\begin{aligned}
y_1(x)f''(x)+\big[2y_1'(x)+P(x)y_1(x)\big]f'(x)+\big[y_1''(x)+P(x)y_1'(x)+Q(x)y_1(x)\big]f(x)=0
\end{aligned}
$$

Note that $y_1'' (x)+P(x)y_1'(x)+Q(x)y_1(x)=0$, so the equation becomes

$$
\begin{aligned}
\frac{1}{f'(x)}df'(x)&=-\left(\frac{2y_1'(x)}{y_1(x)}+P(x) \right)dx\\
\ln f'(x)&=-\ln[y_1(x)]^2-\int^xP(t)dt\\
f'(x)&=\frac{e^{-\int^x}P(t)dt}{[y_1(x)]^2}\\
f(x)&=\int^x\frac{e^{-\int^sP(t)dt}}{[y_1(s)]^2}ds
\end{aligned}
$$

-----

### 7.6.26

(a)
Substitute $y_1,y_2$ into the equation:

$$
\begin{aligned}
a_0\frac{1\pm\alpha}{2}\frac{-1\pm\alpha}{2}x^{\frac{-3\pm\alpha}{2}}+\frac{1-\alpha^2}{4}x^{-2}a_0x^{\frac{1\pm\alpha}{2}}=0
\end{aligned}
$$

so $y_1,y_2$ are indeed solutions.

(b)

$$
\begin{aligned}
y_2(x)=y_1(x)\int^x\frac{e^{-\int^s0dt}}{[y_1(s)]^2}ds=a_0x^\frac{1}{2}\int^xa_0^{-2}s^{-1}ds=a_0^{-1}x^{\frac{1}{2}}\ln x\propto x^{\frac{1}{2}}\ln x
\end{aligned}
$$

(c)

$$
\begin{aligned}
\lim_{\alpha\to0}\left(\frac{y_1-y_2}{\alpha}\right)&=\lim_{\alpha\to0}\left(\frac{a_0x^{\frac{1}{2}}(x^{\frac{\alpha}{2}}-x^{-\frac{\alpha}{2}})}{\alpha} \right)=a_0x^{\frac{1}{2}}\lim_{\alpha\to0}\frac{e^{\frac{\alpha}{2}\ln x}-e^{-\frac{\alpha}{2}\ln x}}{\alpha}\\
&=a_0x^{\frac{1}{2}}\lim_{\alpha\to0}\left[e^{\frac{\alpha}{2}\ln x}\frac{\ln x}{2}-e^{-\frac{\alpha}{2}\ln x}(-\frac{\ln x}{2}) \right]=a_0x^{\frac{1}{2}}\ln x\propto x^{\frac{1}{2}}\ln x
\end{aligned}
$$

where we use the L'Hôpital's rule to obtain the limit.

## 7.7 Inhomogeneous Linear ODEs 

### 7.7.1

Let $y_p=u_1y_1+u_2y_2$, then from Eq 7.98 we have

$$
\begin{aligned}
\renewcommand{\arraystretch}{1}
    & y_1u_1'+y_2u_2'=0\\
    & y_1'u_1'+y_2'u_2'=F(x)
\end{aligned}
$$

Using the Cramer's rules and integrating:

$$
\begin{aligned}
u_1'&=\frac{
\begin{vmatrix}
0&y_2\\F&y_2'
\end{vmatrix}
}{
\begin{vmatrix}
y_1&y_2\\
y_1'&y_2'
\end{vmatrix}
}=
\frac{-y_2F}{W[y_1,y_2]}\qquad
u_1=\int^x\frac{-y_2(s)F(s)}{W[y_1(s),y_2(s)]}ds\\
u_2'&=\frac{
\begin{vmatrix}
y_1&0\\y_1'&F
\end{vmatrix}
}{
\begin{vmatrix}
y_1&y_2\\
y_1'&y_2'
\end{vmatrix}
}=
\frac{y_1F}{W[y_1,y_2]}\qquad
u_2=\int^x\frac{y_1(s)F(s)}{W[y_1(s),y_2(s)]}ds
\end{aligned}
$$

so

$$
\begin{aligned}
y_p&=u_1y_1+u_2y_2\\
&=-y_1(x)\int^x\frac{y_2(s)F(s)}{W[y_1(s),y_2(s)]}ds+y_2(x)\int^x\frac{y_1(s)F(s)}{W[y_1(s),y_2(s)]}ds
\end{aligned}
$$

-----

### 7.7.2

For the homogeneous equation, let $y=e^{mx}$ and substitue:

$$
\begin{aligned}
&m^2+1=0\qquad m=\pm i\\
&y=C_1'e^{ix}+C_2'e^{-ix}=C_1\cos x+C_2\sin x
\end{aligned}
$$

For the particular solution, we can found $y_p=1$ by observation, or by Eq 7.98

$$
\begin{aligned}
     \cos x\,u_1'+\sin x\,u_2'&=0\\
     -\sin x\,u_1'+\cos x\,u_2'&=1
\end{aligned}
$$

$$
\begin{aligned}
    & u_1'=-\sin x\qquad && u_1=\cos x\\
    & u_2'=\cos x\qquad && u_2=\sin x
\end{aligned}
$$

$$
\begin{aligned}
y_p=u_1y_1+u_2y_2=\cos^2x+\sin^2x=1
\end{aligned}
$$

so

$$
\begin{aligned}
y=C_1\cos x+C_2\sin x+1
\end{aligned}
$$

-----

### 7.7.3

For the homogeneous equation, let $y=e^{mx}$ and substitue:

$$
\begin{aligned}
&m^2+4=0\qquad m=\pm 2i\\
&y=C_1e^{2ix}+C_2e^{-2ix}
\end{aligned}
$$

For the particular solution, from Eq 7.98,

$$
\begin{aligned}
    e^{2ix}u_1'+e^{-2ix}u_2'&=0\\
    2ie^{2ix}u_1'-2ie^{-2ix}u_2'&=e^x
\end{aligned}
$$

$$
\begin{aligned}
    & u_1'=\frac{e^x}{4ie^{2ix}}=\frac{1}{4i}e^{(1-2i)x}\qquad && u_1=\frac{1}{4i(1-2i)}e^{(1-2i)x}\\
    & u_2'=\frac{-e^x}{4ie^{-2ix}}=\frac{-1}{4i}e^{(1+2i)x}\qquad && u_2=\frac{-1}{4i(1+2i)}e^{(1+2i)x}
\end{aligned}
$$

$$
\begin{aligned}
y_p=u_1y_1+u_2y_2=e^x\left[\frac{1}{4i(1-2i)}-\frac{1}{4i(1+2i)}\right]=\frac{1}{5}e^x
\end{aligned}
$$

so

$$
\begin{aligned}
y=C_1e^{2ix}+C_2e^{-2ix}+\frac{1}{5}e^x
\end{aligned}
$$

-----

### 7.7.4

For the homogeneous equation, let $y=e^{mx}$ and substitue:

$$
\begin{aligned}
&m^2-3m+2=0\qquad m=1,2\\
&y=C_1e^x+C_2e^{2x}
\end{aligned}
$$

For the particular solution, from Eq 7.98,

$$
\begin{aligned}
    e^xu_1'+e^{2x}u_2'&=0\\
    e^xu_1'+2e^{2x}u_2'&=\sin x
\end{aligned}
$$

$$
\begin{aligned}
    & u_1'=-e^{-x}\sin x\qquad && u_1=\frac{1}{2}e^{-x}(\cos x+\sin x)\\
    & u_2'=e^{-2x}\sin x\qquad && u_2=-\frac{1}{5}e^{-2x}(\cos x+2\sin x)
\end{aligned}
$$

$$
\begin{aligned}
y_p=u_1y_1+u_2y_2=\frac{3}{10}\cos x+\frac{1}{10}\sin x
\end{aligned}
$$

so

$$
\begin{aligned}
y=C_1e^x+C_2e^{2x}+\frac{3}{10}\cos x+\frac{1}{10}\sin x
\end{aligned}
$$

-----

### 7.7.5

Let $y=\sum_{j=0}^\infty a_jx^{s+j}$ and substitute:

$$
\begin{aligned}
x\sum_{j=0}^\infty a_j(s+j)(s+j-1)x^{s+j-2}-(1+x)\sum_{j=0}^\infty a_j(s+j)x^{s+j-1}+\sum_{j=0}^\infty a_jx^{s+j}=0
\end{aligned}
$$

The coefficient of $x^{s-1}$ is $a_0s(s-2)=0$, which means $s=0,2$. The coefficient of $x^{s+j}$ with $j\geq0$ is

$$
\begin{aligned}
a_{j+1}(s+j+1)(s+j)-a_{j+1}(s+j+1)-a_j(s+j)+a_j=0
\end{aligned}
$$

Choose $s=0$ and rearrange:

$$
\begin{aligned}
a_{j+1}&=a_j\frac{1}{j+1}\\
a_j&=a_0\frac{1}{j!}
\end{aligned}
$$

so

$$
\begin{aligned}
y_1=\sum_{j=0}^\infty a_jx^{s+j}=\sum_{j=0}^\infty a_0\frac{x^j}{j!}=a_0e^x\propto e^x
\end{aligned}
$$

Using Eq 7.67,

$$
\begin{aligned}
y_2(x)&=y_1(x)\int^x\frac{e^{\int^s(\frac{1}{t}+1)dt}}{[y_1(s)]^2}ds\\
&=e^x\int^xse^se^{-2s}ds=e^x(-xe^{-x}-e^{-x})=-1-x\propto 1+x
\end{aligned}
$$

Let $y_p=u_1y_1+u_2y_2$ and use Eq 7.98,

$$
\begin{aligned}
e^xu_1'+(1+x)u_2'&=0\\
e^xu_1'+u_2'&=x
\end{aligned}
$$

$$
\begin{aligned}
    & u_1'=e^{-x}(1+x)\qquad && u_1=-e^{-x}(x+2)\\
    & u_2'=-1\qquad && u_2=-x
\end{aligned}
$$

$$
\begin{aligned}
y_p=u_1y_1+u_2y_2=-(x+2)-x(1+x)=-x^2-2x-2
\end{aligned}
$$

where $-2x-2=-2(x+1)=-2y_2$ and therefore can be omitted, so $y_p=-x^2$, and

$$
\begin{aligned}
y=C_1e^x+C_2(1+x)-x^2
\end{aligned}
$$

## 7.8 Nonlinear Differential Equations

### 7.8.1

Let $y=2+u$ and substitute into the equation:

$$
\begin{aligned}
u'=(2+u)^2-(2+u)-2=u^2+3u
\end{aligned}
$$

which is a Bernoulli equation, so let $v=u^{1-2}=u^{-1}$ and substitute:

$$
\begin{aligned}
v'&=-u^{-2}u'=-(1+3v)\\
\frac{1}{3v+1}dv&=-dx\\
\frac{1}{3}\ln(3v+1)&=-x+C'\\
v&=\frac{Ce^{-3x}-1}{3}\\
u&=v^{-1}=\frac{3}{Ce^{-3x}-1}
\end{aligned}
$$

so

$$
\begin{aligned}
y=2+\frac{3}{Ce^{-3x}-1}
\end{aligned}
$$

-----

### 7.8.2

Let $y=x^2+u$ and substitute into the equation:

$$
\begin{aligned}
2x+u'&=  \frac{(x^2+u)^2}{x^3}-\frac{(x^2+u)}{x}+2x\\
u'&=\frac{1}{x}u+\frac{1}{x^3}u^2
\end{aligned}
$$

which is a Bernoulli equation, so let $v=u^{1-2}=u^{-1}$ and substitute:

$$
\begin{aligned}
v'&=-u^{-2}u'=-(\frac{1}{x}v+\frac{1}{x^3})\\
v'+\frac{1}{x}v&=-\frac{1}{x^3}
\end{aligned}
$$

which is a linear first-order equation. The integrating factor is

$$
\begin{aligned}
\alpha=e^{\int\frac{1}{x}dx}=x
\end{aligned}
$$

Multiplying,

$$
\begin{aligned}
\frac{d}{dx}(xv)&=xv'+v=-\frac{1}{x^2}\\
xv&=x^{-1}+C\\
v&=\frac{1+Cx}{x^2}\\
u&=v^{-1}=\frac{x^2}{1+Cx}
\end{aligned}
$$

so

$$
\begin{aligned}
y=x^2+\frac{x^2}{1+Cx}
\end{aligned}
$$

-----

### 7.8.3

Let $u=y^{1-3}=y^{-2}$ and substitute:

$$
\begin{aligned}
u'&=-2y^{-3}y'=-2(-xu+x)=2x(u-1)\\
\frac{1}{u-1}du&=2xdx\\
\ln(u-1)&=x^2+C'\\
u&=Ce^{x^2}+1\\
y&=u^{-\frac{1}{2}}=\frac{1}{\sqrt{Ce^{x^2}+1}}
\end{aligned}
$$

-----

### 7.8.4

(a)

$$
\begin{aligned}
y''=0\qquad y'=a\qquad y=ax+b
\end{aligned}
$$

Substitute into the equation:

$$
\begin{aligned}
ax+b=xa+a^2
\end{aligned}
$$

so $b=a^2$, and therefore

$$
\begin{aligned}
y=ax+a^2
\end{aligned}
$$

(b)

$$
\begin{aligned}
f'(y')=2y'=-x\qquad y=-\frac{x^2}{4}+c
\end{aligned}
$$

Substitute into the equation:

$$
\begin{aligned}
-\frac{x^2}{4}+c=-\frac{x^2}{2}+\frac{x^2}{4}
\end{aligned}
$$

so $c=0$, and therefore

$$
\begin{aligned}
y=-\frac{x^2}{4}
\end{aligned}
$$

The envelope of a family of curves $f(x,y,a)$ can be obtained by solving 

$$
\begin{aligned}
\begin{cases}
    f(x,y,a)=0\\
    f_a(x,y,a)=0
\end{cases}
\end{aligned}
$$

where $f_a$ is the derivative of $f$ regarding $a$. So

$$
\begin{aligned}
\begin{cases}
    y=ax+a^2\\
    0=x+2a
\end{cases}
\end{aligned}
$$

which means $a=-\frac{x}{2}$ and $y=-\frac{x^2}{4}$.

{% endraw %}
