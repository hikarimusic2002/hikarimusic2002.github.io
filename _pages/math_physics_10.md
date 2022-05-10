---
layout: splash
title: "Mathematical Methods for Physicists Ch10"
permalink: /solutions/math_physics_10
author_profile: false

---

# Chapter 10: Green’s Functions

{% raw %}

## 10.1 One-Dimensional Problems

### 10.1.1

The solution given by the Green's function is

$$
\newcommand{\pdv}[2]{\frac{\partial#1}{\partial#2}}
\newcommand{\V}{\mathbf}
\newcommand{\br}[2]{\langle#1|#2\rangle}
\newcommand{\del}{\boldsymbol{\nabla}}
\begin{aligned}
y(x)=\int_0^xt\cdot f(t)\,dt+x\int_x^1f(t)\,dt
\end{aligned}
$$

then

$$
\begin{aligned}
    & y'(x)=xf(x)+\int_x^1f(t)\,dt-xf(x)=\int_x^1f(t)\,dt\\
    & y''(x)=-f(x)\\
    & y(0)=\int_0^0t\cdot f(t)\,dt+0\int_x^1f(t)\,dt=0\\
    & y'(1)=\int_1^1f(t)\,dt=0
\end{aligned}
$$

so the equation $\mathcal{L}y=-y''(x)=f(x)$ is satisfied, and the boundary conditions $y(0)=0$ and $y'(1)=0$ are also satisfied.

-----

### 10.1.2

(a) $\sin x$ satisfies the homogeneous equation and $y(0)=0$, and $\cos(x-1)$ satisfies the homogeneous equation and $y'(1)=0$, so the Green's function has the form

$$
\begin{aligned}
G(x,t)=
\begin{cases}
h_1(t)\sin x,\quad & 0\leq x<t\\
h_2(t)\cos(x-1),\quad & t<x\leq1
\end{cases}
\end{aligned}
$$

Using the general properties of Green's function:

$$
\begin{aligned}
    & G(t_+,t)=G(t_-,t)\quad && \longrightarrow\quad && h_2(t)\cos(t-1)=h_1(t)\sin t\\
    & \pdv{G}{x}(t_+,t)-\pdv{G}{x}(t_-,t)=\frac{1}{p(t)}\quad && \longrightarrow\quad && -h_2(t)\sin(t-1)-h_1(t)\cos t=1
\end{aligned}
$$

so $h_1(t)=-\frac{\cos(t-1)}{\cos(1)}$, and $h_2(t)=-\frac{\sin t}{\cos(1)}$. Therefore the Green's function is

$$
\begin{aligned}
G(x,t)=
\begin{cases}
-\frac{\sin x\cos(t-1)}{\cos(1)},\quad & 0\leq x<t\\[5pt]
-\frac{\cos(x-1)\sin t}{\cos(1)},\quad & t<x\leq1
\end{cases}
\end{aligned}
$$

(b) $e^x$ satisfies the homogeneous equation and $y(-\infty)=0$, and $e^{-x}$ satisfies the homogeneous equation and $y(\infty)=0$, so the Green's function has the form

$$
\begin{aligned}
G(x,t)=
\begin{cases}
e^xh_1(t),\quad & -\infty<x<t\\
e^{-x}h_2(t),\quad & t<x<\infty
\end{cases}
\end{aligned}
$$

Using the general properties of Green's function:

$$
\begin{aligned}
    & G(t_+,t)=G(t_-,t)\quad && \longrightarrow\quad && e^{-t}h_2(t)=e^th_1(t) \\
    & \pdv{G}{x}(t_+,t)-\pdv{G}{x}(t_-,t)=\frac{1}{p(t)}\quad && \longrightarrow\quad && -e^{-t}h_2(t)-e^th_1(t)=1
\end{aligned}
$$

so $h_1(t)=-\frac{e^{-t}}{2}$, and $h_2(t)=-\frac{e^t}{2}$. Therefore the Green's function is

$$
\begin{aligned}
G(x,t)=
\begin{cases}
-\frac{e^{x-t}}{2},\quad & -\infty<x<t\\[5pt]
-\frac{e^{t-x}}{2},\quad & t<x<\infty
\end{cases}
\end{aligned}
$$

-----

### 10.1.3

The solution is

$$
\begin{aligned}
y(x)=\int_0^x\sin(x-t)f(t)dt
\end{aligned}
$$

By Leibniz integral rule,

$$
\begin{aligned}
    & y'(x)=\sin(x-x)f(x)+\int_0^x\pdv{\sin(x-t)}{x}f(t)\,dt=\int_0^x\cos(x-t)f(t)\,dt\\
    & y''(x)=\cos(x-x)f(x)+\int_0^x\pdv{\cos(x-t)}{x}f(t)\,dt=f(x)-y(x)\\
    & y(0)=\int_0^0\sin(x-t)f(t)\,dt=0\\
    & y'(0)=\int_0^0\cos(x-t)f(t)\,dt=0
\end{aligned}
$$

so the equation $y''+y=f(x)$ is satisfied, and the initial conditions $y(0)=y'(0)=0$ are also satisfied.

-----

### 10.1.4

$\sin(\frac{x}{2})$ satisfies the homogeneous equation and $y(0)=0$, and $\cos(\frac{x}{2})$ satisfies the homogeneous equation and $y(\pi)=0$, so the Green's function has the form

$$
\begin{aligned}
G(x,t)=
\begin{cases}
h_1(t)\sin(\frac{x}{2}),\quad & 0\leq x<t\\
h_2(t)\cos(\frac{x}{2}),\quad & t<x\leq\pi
\end{cases}
\end{aligned}
$$

Using the general properties of Green's function:

$$
\begin{aligned}
    & G(t_+,t)=G(t_-,t)\quad && \longrightarrow\quad && h_2(t)\cos(\frac{t}{2})=h_1(t)\sin(\frac{t}{2})\\
    & \pdv{G}{x}(t_+,t)-\pdv{G}{x}(t_-,t)=\frac{1}{p(t)}\quad && \longrightarrow\quad && -\frac{1}{2} h_2(t)\sin(\frac{t}{2})-\frac{1}{2} h_1(t)\cos(\frac{t}{2})=-1
\end{aligned}
$$

so $h_1(t)=2\cos(\frac{t}{2})$, and $h_2(t)=2\sin(\frac{t}{2})$. Therefore the Green's function is

$$
\begin{aligned}
G(x,t)=
\begin{cases}
2\sin(\frac{x}{2})\cos(\frac{t}{2}),\quad & 0\leq x<t\\[5pt]
2\cos(\frac{x}{2})\sin(\frac{t}{2}),\quad & t<x\leq\pi
\end{cases}
\end{aligned}
$$

-----

### 10.1.5

Let $u=kx$, then the equation becomes Bessel's equation with order $n=1$, so the solution is $J_1(kx)$ and $Y_1(kx)$. \;$J_1(kx)$ satisfies $y(0)=0$, and $Y_1(k)J_1(kx)-J_1(k)Y_1(kx)$ satisfies $y(1)=0$. To find the Green's function, we must put it into the self-sdjoint form:

$$
\begin{aligned}
x\frac{d^2y}{dx^2}+\frac{dy}{dx}+(k^2x-\frac{1}{x})y=\frac{f(x)}{x}
\end{aligned}
$$

Then the Green's function has the form (we use $g$ instead of $G$ to remind that it is the Green's function of the self-adjoint equation, not the original equation)

$$
\begin{aligned}
g(x,t)=
\begin{cases}
h_1(t)J_1(kx),\quad & 0\leq x<t\\
h_2(t)\left[Y_1(k)J_1(kx)-J_1(k)Y_1(kx)\right],\quad & t<x\leq1
\end{cases}
\end{aligned}
$$

Using the general properties of Green's function:

$$
\begin{aligned}
    & G(t_+,t)=G(t_-,t)\quad && \longrightarrow\quad && h_2(t)\left[Y_1(k)J_(kt)-J_1(k)Y_1(kt) \right]=h_1(t)J_1(kt) \\
    & \pdv{G}{x}(t_+,t)-\pdv{G}{x}(t_-,t)=\frac{1}{p(t)}\quad && \longrightarrow\quad && h_2(t)\left[Y_1(k)J_1'(kt)-J_1(k)Y_1'(kt) \right]-h_1(t)J_1'(kt)=\frac{1}{t}
\end{aligned}
$$

so $h_1(t)=-\frac{\pi}{2J_1(k)}\left[Y_1(k)J_1(kt)-J_1(k)Y_1(kt) \right]$, and $h_2(t)=-\frac{\pi}{2J_1(k)}J_1(kt)$. Therefore the Green's function is

$$
\begin{aligned}
g(x,t)=
\begin{cases}
-\frac{\pi}{2J_1(k)}J_1(kx)\left[Y_1(k)J_1(kt)-J_1(k)Y_1(kt) \right] ,\quad & 0\leq x<t\\
-\frac{\pi}{2J_1(k)}\left[Y_1(k)J_1(kx)-J_1(k)Y_1(kx)\right]J_1(kt) ,\quad & t<x\leq1
\end{cases}
\end{aligned}
$$

The solution is given by $y(x)=\int_0^1g(x,t)\frac{f(x)}{x}dx$, which means the Green's function of the original equagtion is

$$
\begin{aligned}
G(x,t)=\frac{g(x,t)}{x}=
\begin{cases}
\frac{\pi}{2x}J_1(kx)\left[Y_1(kt)-\frac{Y_1(k)}{J_1(k)}J_1(kt) \right] ,\quad & 0\leq x<t\\[5pt]
\frac{\pi}{2x}\left[Y_1(kx)-\frac{Y_1(k)}{J_1(k)}J_1(kx) \right]J_1(kt) ,\quad & t<x\leq1
\end{cases}
\end{aligned}
$$

-----

### 10.1.6

The equation is Legendre's differential equation of order $n=0$, so the solution is $P_0(x)=1$ and $Q_0(x)=\frac{1}{2}\ln\frac{1+x}{1-x}$. \;$Q_0(x)$ is infinite at $x=\pm1$, so the function for $x<t$ and $x>t$ that satisfies the boundary conditions will both be a multiple of $P_0(x)$, which results in the absence of the discontinuity in $\frac{dG(x,t)}{dx}\big\vert_{x=t}$. So no Green's function can be constructed.

-----

### 10.1.7

The solution of the homogeneous equation has the form $c_1e^{-kt}+c_2$. The only solution that satisfies $\psi(0)=\psi'(0)=0$ is the trivial solution $\psi(t)=0$, while there is no other boundary condition. To find the Green's function, we must  put the equation into self-adjoint form:

$$
\begin{aligned}
e^{kt}\frac{d^2\psi}{dt^2}+ke^{kt}\frac{d\psi}{dt}=e^{kt}f(t)
\end{aligned}
$$

Then the Green's function has the form

$$
\begin{aligned}
g(t,u)=
\begin{cases}
0,\quad & 0\leq t<u\\
h_1(u)e^{-kt}+h_2(u),\quad & u<t
\end{cases}
\end{aligned}
$$

Using the general properties of Green's function:

$$
\begin{aligned}
    & G(u_+,u)=G(u_-,u)\quad && \longrightarrow\quad && h_1(u)e^{-kt}+h_2(u)=0 \\
    & \pdv{G}{t}(u_+,u)-\pdv{G}{t}(u_-,u)=\frac{1}{p(u)}\quad && \longrightarrow\quad && -kh_1(u)e^{-ku}=e^{-ku}
\end{aligned}
$$

so $h_1(u)=-\frac{1}{k}$, and $h_2(u)=\frac{e^{-ku}}{k}$. Therefore the Green's function of the self-adjoint equation is

$$
\begin{aligned}
g(t,u)=
\begin{cases}
0,\quad & 0\leq t<u\\
\frac{1}{k}\left(-e^{-kt}+e^{-ku} \right) ,\quad & u<t
\end{cases}
\end{aligned}
$$

and the Green's function of the original equation is

$$
\begin{aligned}
G(t,u)=g(t,u)e^{ku}=
\begin{cases}
0,\quad & 0\leq t<u\\
\frac{1}{k}\left(1-e^{k(u-t)} \right) ,\quad & u<t
\end{cases}
\end{aligned}
$$

If $f(t)=e^{-t}$, then the solution is given by

$$
\begin{aligned}
y(t)=\int_0^t\frac{1}{k}\left(1-e^{k(u-t)} \right)e^{-u}du=\frac{(k-1)-ke^{-t}+e^{-kt}}{k(k-1)}
\end{aligned}
$$

-----

### 10.1.8

From the Green's function, the solution is given by

$$
\begin{aligned}
\psi(x)=\int_{-\infty}^x-\frac{i}{2k}e^{ik(x-x')}g(x')dx'+\int_x^\infty-\frac{i}{2k}e^{ik(x'-x)}g(x')dx'
\end{aligned}
$$

Using the Leibniz integral rule:

$$
\begin{aligned}
\frac{d\psi(x)}{dx}&=-\frac{i}{2k}e^{ik(x-x)}g(x)+\int_{-\infty}^x-\frac{i}{2k}(ik)e^{ik(x-x')}g(x')dx'+\frac{i}{2k}e^{ik(x-x)}g(x)+\int_x^\infty-\frac{i}{2k}(-ik)e^{ik(x'-x)}g(x')dx'\\
&=\int_{-\infty}^x\frac{1}{2}e^{ik(x-x')}g(x')dx'+\int_x^\infty-
\frac{1}{2}e^{ik(x'-x)}g(x')dx'\\
\frac{d^2\psi(x)}{dx^2}&=\frac{1}{2}e^{ik(x-x)}g(x)+\int_{-\infty}^x\frac{1}{2}(ik)e^{ik(x-x')}g(x')dx'+\frac{1}{2}e^{ik(x-x)}g(x)+\int_x^\infty-\frac{1}{2}(-ik)e^{ik(x'-x)}g(x')dx'\\
&=g(x)-k^2\psi(x)
\end{aligned}
$$

so the solution satisfies the equation $\frac{d^2\psi}{dx^2}+k^2\psi=g(x)$

-----

### 10.1.9

$e^{kx}$ satisfies the homogeneous equation and $y(-\infty)=0$, and $e^{-kx}$ satisfies the homogeneous equation and $y(\infty)=0$, so the Green's function has the form

$$
\begin{aligned}
G(x,t)=
\begin{cases}
h_1(t)e^{kx} ,\quad & -\infty<x<t\\
h_2(t)e^{-kx} ,\quad & t<x<\infty
\end{cases}
\end{aligned}
$$

Using the general properties of Green's function:

$$
\begin{aligned}
    & G(t_+,t)=G(t_-,t)\quad && \longrightarrow\quad && h_2(t)e^{-kt}=h_1(t)e^{kt} \\
    & \pdv{G}{x}(t_+,t)-\pdv{G}{x}(t_-,t)=\frac{1}{p(t)}\quad && \longrightarrow\quad && -kh_2(t)e^{-kt}-kh_1(t)e^{kt}=1
\end{aligned}
$$

so $h_1(t)=-\frac{1}{2k}e^{-kt}$, and $h_2(t)=-\frac{1}{2k}e^{kt}$. Therefore the Green's function is

$$
\begin{aligned}
G(x,t)=
\begin{cases}
-\frac{1}{2k}e^{k(x-t)} ,\quad & -\infty<x<t\\[5pt]
-\frac{1}{2k}e^{k(t-x)} ,\quad & t<x<\infty
\end{cases}
=-\frac{1}{2k}e^{-k|x-t|}
\end{aligned}
$$

-----

### 10.1.10

(a) From Example 10.1.1,

$$
\begin{aligned}
G(x,t)=
\begin{cases}
x(1-t),\quad & 0\leq x<t\\
t(1-x),\quad & t<x\leq1
\end{cases}
\end{aligned}
$$

is the Green's function of the equation $-y''=f(x)$, with boundary conditions $y(0)=y(1)=0$. The operator $\mathcal{L}=-\frac{d^2}{dx^2}$ and boundary conditions $y(0)=y(1)=0$ have the orthonormal eigenfunctions $\varphi_n=\sqrt{2}\sin n\pi x$ with eigenvalues $\lambda_n=n^2\pi^2$, so by Equation 10.14, the Green's function is given by

$$
\begin{aligned}
G(x,t)=\sum_n\frac{\varphi_n^*(t)\varphi_n(x)}{\lambda_n}=\sum_{n=1}^\infty\frac{2\sin n\pi x\,\sin n\pi t}{n^2\pi^2}
\end{aligned}
$$

(b) From Exercise 10.1.1, 

$$
\begin{aligned}
G(x,t)=
\begin{cases}
x,\quad & 0\leq x<t\\
t,\quad & t<x\leq1
\end{cases}
\end{aligned}
$$

is the Green's function of the equation $-y''=f(x)$, with boundary conditions $y(0)=0,\,y'(1)=0$. The operator $\mathcal{L}=-\frac{d^2}{dx^2}$ and boundary conditions $y(0)=0,\,y'(1)=0$ have the orthonormal eigenfunctions $\varphi_n=\sqrt{2}\sin(n+\frac{1}{2})\pi x$ with eigenvalues $\lambda_n=(n+\frac{1}{2})^2\pi^2$, so by Equation 10.14, the Green's function is given by

$$
\begin{aligned}
G(x,t)=\sum_n\frac{\varphi_n^*(t)\varphi_n(x)}{\lambda_n}=\sum_{n=1}^\infty\frac{2\sin(n+\frac{1}{2})\pi x\,\sin (n+\frac{1}{2})\pi t}{(n+\frac{1}{2})^2\pi^2}
\end{aligned}
$$

-----

### 10.1.11

(a)

$$
\begin{aligned}
y''(x)&=y(x)\\
y'(x)-y'(-1)&=\int_{-1}^xy(t)dt\\
y'(x)&=c+\int_{-1}^xy(t)dt\\
y(x)-y(-1)&=c\int_{-1}^xdx+\int_{-1}^xds\int_{-1}^sy(t)dt\\
&=c(x+1)+\int_{-1}^xy(t)dt\int_t^xds\\
&=c(x+1)+\int_{-1}^xy(t)(x-t)dt
\end{aligned}
$$

where we change the order of integration in the last three equation (the area to be integrated is an upper triangle in the \textit{t-s} surface). Substitute $y(1)=1$ and $y(-1)=1$:

$$
\begin{aligned}
y(1)-y(-1)&=2c+\int_{-1}^1y(t)(1-t)dt=0\\
c=&-\frac{1}{2}\int_{-1}^1y(t)(1-t)dt
\end{aligned}
$$

so

$$
\begin{aligned}
y(x)&=y(-1)+c(x+1)+\int_{-1}^xy(t)(x-t)dt\\
&=1-\frac{1}{2}\int_{-1}^1(x+1)y(t)(1-t)dt+\int_{-1}^xy(t)(x-t)dt\\
&=1-\int_{-1}^x\frac{1}{2}(1-x)(t+1)y(t)dt-\int_x^1\frac{1}{2}(1-t)(x+1)y(t)dt\\
&=1-\int_{-1}^1K(x,t)\,y(t)\,dt
\end{aligned}
$$

where

$$
\begin{aligned}
K(x,t)=
\begin{cases}
\frac{1}{2}(1-x)(t+1),\quad & x>t\\
\frac{1}{2}(1-t)(x+1),\quad & x<t
\end{cases}
\end{aligned}
$$

(b) Let $u(x)=y(x)-1$, then the equation becomes $u''(x)=u(x)+1$, and the boundary conditions becomes $u(1)=u(-1)=0$. \;$u(x)=x+1$ satisfies the homogeneous equation and $u(-1)=0$, and $u(x)=x-1$ satisfies the homogeneous equation and $u(1)=0$. So the Green's function has the form

$$
\begin{aligned}
G(x,t)=
\begin{cases}
h_1(t)(x+1),\quad & x<t\\
h_2(t)(x-1),\quad & x>t
\end{cases}
\end{aligned}
$$

Using the general properties of Green's function:

$$
\begin{aligned}
    & G(t_+,t)=G(t_-,t)\quad && \longrightarrow\quad && h_2(t)(t-1)=h_1(t)(t+1) \\
    & \pdv{G}{x}(t_+,t)-\pdv{G}{x}(t_-,t)=\frac{1}{p(t)}\quad && \longrightarrow\quad && h_2(t)-h_1(t)=1
\end{aligned}
$$

so $h_1(t)=\frac{1}{2}(t-1)$, and $h_2(t)=\frac{1}{2}(t+1)$. Therefore the Green's function is

$$
\begin{aligned}
G(x,t)=
\begin{cases}
\frac{1}{2}(x+1)(t-1),\quad & x<t\\[2pt]
\frac{1}{2}(x-1)(t+1),\quad & x>t
\end{cases}
\end{aligned}
$$

To match the notation with the book, define

$$
\begin{aligned}
K(x,t)=-G(x,t)=
\begin{cases}
\frac{1}{2}(1-x)(t+1),\quad & x>t\\[2pt]
\frac{1}{2}(1-t)(x+1),\quad & x<t
\end{cases}
\end{aligned}
$$

then the solution (integral equation) is given by

$$
\begin{aligned}
y(x)=1+u(x)=1+\int_{-1}^1G(x,t)\left[u(t)+1 \right]dt=1-\int_{-1}^1K(x,t)\,y(t)\,dt
\end{aligned}
$$

-----

### 10.1.12

$$
\begin{aligned}
&y'(x)-y'(0)+a_1y(x)-a_1y(0)+a_2\int_0^xy(t)dt=0\\
&y(x)-y(0)-y'(0)(x-0)+a_1\int_0^xy(t)dt-a_1y(0)(x-0)+a_2\int_0^xds\int_0^sy(t)dt=0\\
&y(x)-y'_0x+a_1\int_0^xy(t)dt+a_2\int_0^xy(t)(x-t)dt=0
\end{aligned}
$$

Substitute $y(1)=0$:

$$
\begin{aligned}
-y'_0&+a_1\int_0^1y(t)dt+a_2\int_0^1y(t)(1-t)dt=0\\
y_0'&=a_1\int_0^1y(t)dt+a_2\int_0^1y(t)(1-t)dt\\
y(x)&=y'_0x-a_1\int_0^xy(t)dt-a_2\int_0^xy(t)(x-t)dt\\
&=a_1\int_0^1xy(t)dt+a_2\int_0^1x(1-t)y(t)dt-a_1\int_0^xy(t)dt-a_2\int_0^x(x-t)y(t)dt\\
&=\int_0^x\big[a_2t(1-x)+a_1(x-1)\big]y(t)dt+\int_x^1\big[a_2x(1-t)+a_1x\big]y(t)dt\\
&=\int_0^1K(x,t)y(t)dt
\end{aligned}
$$

where

$$
\begin{aligned}
K(x,t)=
\begin{cases}
a_2t(1-x)+a_1(x-1),\quad & t<x\\
a_2x(1-t)+a_1x,\quad & x<t
\end{cases}
\end{aligned}
$$

If $a_1=0$, then the equation is self-adjoint, so $K(x,t)$ is the Green's function of the equation, and therefore has the properties of Green's function (symmetry, continuity, etc.)

-----

### 10.1.13

Regard $V_0\frac{e^{-r}}{r}y(r)$ as the inhomogeneous term:

$$
\begin{aligned}
\frac{d^2y(r)}{dr^2}-k^2y(r)=-V_0\frac{e^{-r}}{r}y(r)
\end{aligned}
$$

The solution of the homogeneous equation has the form $c_1e^{kr}+c_2e^{-kr}$. \;$\sinh kr=\frac{1}{2}(e^{kr}-e^{-kr})$ satisfies the homogeneous equation and y(0)=0, and $e^{-kr}$ satisfies the homogeneous equation and $y(\infty)=0$. So the Green's function has the form

$$
\begin{aligned}
G(r,t)=
\begin{cases}
h_1(t)\sinh kr,\quad & 0\leq r<t\\
h_2(t)e^{-kr},\quad & t<r<\infty
\end{cases}
\end{aligned}
$$

Using the general properties of Green's function:

$$
\begin{aligned}
    & G(t_+,t)=G(t_-,t)\quad && \longrightarrow\quad && h_2(t)e^{-kt}=h_1(t)\sinh ht \\
    & \pdv{G}{r}(t_+,t)-\pdv{G}{r}(t_-,t)=\frac{1}{p(t)}\quad && \longrightarrow\quad && -kh_2(t)e^{-kt}-kh_1(t)\cosh kt=1
\end{aligned}
$$

so $h_1(t)=-\frac{1}{k}e^{-kt}$, and $h_2(t)=-\frac{1}{k}\sinh kt$. Therefore the Green's function is

$$
\begin{aligned}
G(r,t)=
\begin{cases}
-\frac{1}{k}e^{-kt}\sinh kr,\quad & 0\leq r<t\\[2pt]
-\frac{1}{k}e^{-kr}\sinh kt,\quad & t<r<\infty
\end{cases}
\end{aligned}
$$

and the solution (integral equation) is given by

$$
\begin{aligned}
y(r)=\int_0^\infty G(r,t)f(t)dt=-V_0\int_0^\infty G(r,t)\frac{e^{-t}}{t}y(t)\,dt
\end{aligned}
$$

## 10.2 Problems in Two and Three Dimensions

### 10.2.1

$$
\begin{aligned}
\mathcal{L}\int_a^b\Big[G(x_1,x_2)+\varphi(x_1)\Big]f(x_2)dx_2=\int_a^b\Big[\mathcal{
L}G(x_1,x_2)+\mathcal{L}\varphi(x_1)\Big]f(x_2)dx_2=\mathcal{L}\int_a^bG(x_1,x_2)f(x_2)dx_2
\end{aligned}
$$

if $\mathcal{L}\varphi(x_1)=0$. That means
the Green's function will still give the correct solution if added a solution of the homogeneous equation.
$\frac{1}{2}|x_1-x_2|$ is the Green's function of Laplace equation, and $-\frac{1}{2}x_1-\frac{1}{2}x_2$ is a solution of the homogeneous solution, so

$$
\begin{aligned}
\frac{1}{2}|x_1-x_2|-\frac{1}{2}x_1-\frac{1}{2}x_2=
\begin{cases}
-x_1,\quad & 0\leq x_1<x_2\\
-x_2,\quad & x_2<x_1\leq1
\end{cases}
\end{aligned}
$$

is also a Green's function of Laplace equation, which is consistent with the one found in Example 10.1.1 (negative signs arise because the operator is defined as $\mathcal{L}=-\frac{d^2}{dx^2}$ in Example 10.1.1).

-----

### 10.2.2

$$
\begin{aligned}
\mathcal{L}\psi(\V{r})&=\del\cdot\big[p(\V{r})\del\psi(\V{r}) \big]+q(\V{r})\psi(\V{r})\\
\br{\chi}{\mathcal{L}\psi}&=\int\limits_V\chi^*\mathcal{L}\psi\,d\tau=\int\limits_V\chi^*\del\cdot\big[p\del\psi\big]\,d\tau+\int\limits_V\chi^*q\psi\,d\tau\\
&=\int\limits_V\del\cdot(\chi^*p\del\psi)\,d\tau-\int\limits_V(\del\chi^*)\cdot(p\del\psi)\,d\tau+\int\limits_V\chi^*q\psi\,d\tau\\
&=\oint\limits_A\chi^*p(\del\psi)\cdot d\boldsymbol{\sigma}-\int\limits_V\del\cdot(\psi p\del\chi^*)\,d\tau+\int\limits_V\psi\del\cdot(p\del\chi^*)\,d\tau+\int\limits_V\chi^*q\psi\,d\tau\\
&=\oint\limits_A\chi^*p(\del\psi)\cdot d\boldsymbol{\sigma}-\int\limits_A\psi p(\del\chi^*)\cdot d\boldsymbol{\sigma} +\int\limits_V\psi\big[\del\cdot(p\del\chi^*)+q\chi^*\big]\,d\tau\\
&=\oint\limits_A(\chi^*p\del\psi-\psi p\del\chi^*)\cdot d\boldsymbol{\sigma}+\int\limits_V\psi\mathcal{L}\chi^*\,d\tau\\
&=\br{\mathcal{L}\chi}{\psi}
\end{aligned}
$$

which implies $\mathcal{L}$ is Hermitian. 
                           
(The surface integral vanishes by the Dirichlet boundary conditions.) 
                           
($\del\cdot(f\V{V})=(\del f)\cdot\V{V}+f\del\cdot\V{V}$ and $\int_V\del\cdot\V{V}\,d\tau=\oint_A\V{V}\cdot d\boldsymbol{\sigma}$ have been used several times.)

-----

### 10.2.3

(The space to be integrated given in the book is not quite clear, and the result we get is different from the book.)

$$
\begin{aligned}
&\lim_{|\V{r}_1-\V{r}_2|\to0}\int k^2G(\V{r}_1,\V{r}_2)d^3r_2\\
=&\lim_{a\to0}\int\limits_{|\V{r}_1-\V{r}_2|<a}-k^2\,\frac{e^{ik|\V{r}_1-\V{r}_2|}}{4\pi |\V{r}_1-\V{r}_2|}\,d^3r_2\\
=&-\lim_{a\to0}\int_0^a\int_0^\pi\int_0^{2\pi}k^2\,\frac{e^{ikr}}{4\pi r}\,r^2\sin\theta\,d\theta\,d\varphi\\
=&-\lim_{a\to0}k^2\int_0^a re^{ikr}dr=\lim_{a\to0}(ika\,e^{ika}-e^{ika}+1)=0
\end{aligned}
$$


Substitute $k$ with $ik$, the case becomes modified Helmholtz operator, and the result is the same.

-----

### 10.2.4

For

$$
\begin{aligned}
G(\V{r}_1,\V{r}_2)=-\frac{e^{ik|\V{r}_1-\V{r}_2|}}{4\pi|\V{r}_1-\V{r}_2|}=-\frac{e^{ikr_{12}}}{4\pi r_{12}}
\end{aligned}
$$

We want to show that $(\del^2+k^2)G(\V{r_1},\V{r}_2)=\delta(\V{r}_1-\V{r}_2)$.

For $\V{r}_1\neq\V{r}_2$, 

$$
\begin{aligned}
(\del^2+k^2)G(\V{r_1},\V{r}_2)&=-\del^2\frac{e^{ikr}}{4\pi r}-k^2\frac{e^{ikr}}{4\pi r}\\
&=-\frac{1}{r^2}\frac{d}{dr}\left[r^2\frac{d}{dr}(\frac{e^{ikr}}{4\pi r}) \right]-\frac{k^2e^{ikr}}{4\pi r}\\
&=-\frac{1}{r^2}\frac{d}{dr}\left[\frac{ikr\,e^{ikr}}{4\pi}-\frac{e^{ikr}}{4\pi} \right]-\frac{k^2e^{ikr}}{4\pi r}\\
&=-\frac{ike^{ikr}}{4\pi r^2}+\frac{k^2e^{ikr}}{4\pi r}+\frac{ike^{ikr}}{4\pi r^2}-\frac{k^2e^{ikr}}{4\pi r}=0
\end{aligned}
$$

For $\V{r}_1=\V{r}_2$, the function diverges, but for every $a>0$,

$$
\begin{aligned}
&\int\limits_{r_{12}<a}(\del^2+k^2)G(\V{r}_1,\V{r}_2)d^3r_1\\
=&-\int\limits_{r_{12}<a}\del\cdot\del\frac{e^{ikr_{12}}}{4\pi r_{12}}d^3r_{12}-\int\limits_{r_{12}<a}k^2\frac{e^{ikr_{12}}}{4\pi r_{12}}d^3r_{12}\\
=&-\oint\limits_{r_{12}=a}\del\frac{e^{ikr_{12}}}{4\pi r_{12}}\cdot d\boldsymbol{\sigma}_{12}-\int_0^a\int_0^\pi\int_0^{2\pi}k^2\frac{e^{ikr}}{4\pi r}r^2\sin\theta\,d\theta\,d\varphi\\
=&-\oint\limits_{r_{12}=a}\left(\frac{ike^{ikr_{12}}}{4\pi r_{12}}-\frac{e^{ikr_{12}}}{4\pi r_{12}^2} \right)\hat{\V{r}}\cdot d\boldsymbol{\sigma}_{12}-k^2\int_0^a re^{ikr}dr\\
=&-\left(\frac{ike^{ika}}{4\pi a}-\frac{e^{ika}}{4\pi a^2} \right)4\pi a^2-k^2\left(\frac{ae^{ika}}{ik}+\frac{e^{ika}-1}{k^2} \right)\\
=&-ika\,e^{ika}+e^{ika}+ika\,e^{ika}-e^{ika}+1=1
\end{aligned}
$$

Therefore, it must be

$$
\begin{aligned}
(\del^2+k^2)G(\V{r_1},\V{r}_2)=\delta(\V{r}_1-\V{r}_2)
\end{aligned}
$$

-----

### 10.2.5

$$
\begin{aligned}
-\frac{e^{ik|\V{r}_1-\V{r}_2|}}{4\pi|\V{r}_1-\V{r}_2|}
\end{aligned}
$$

is the fundamental Green's function of the Helmholtz equation, and

$$
\begin{aligned}
\frac{i\sin k|\V{r}_1-\V{r}_2|}{4\pi|\V{r}_1-\V{r}_2|}
\end{aligned}
$$

is a solution of the Helmholtz equation, so

$$
\begin{aligned}
-\frac{e^{ik|\V{r}_1-\V{r}_2|}}{4\pi|\V{r}_1-\V{r}_2|}+\frac{i\sin k|\V{r}_1-\V{r}_2|}{4\pi|\V{r}_1-\V{r}_2|}=\frac{-\cos k|\V{r}_1-\V{r}_2|}{4\pi|\V{r}_1-\V{r}_2|}
\end{aligned}
$$

is also a Green's function of the Helmholtz equation, and the asymptotic $r$ dependence is $\cos kr$, which is a standing wave.

-----

### 10.2.6

In Exercise 10.2.4, substitute $k$ with $ik$, then the Helmholtz equation $(\del^2+k^2)\psi=0$ becomes $(\del^2-k^2)\psi=0$, which is the modified Helmholtz equation, and the Green's function becomes

$$
\begin{aligned}
G(\V{r}_1,\V{r}_2)=-\frac{e^{-k|\V{r}_1-\V{r}_2|}}{4\pi|\V{r}_1-\V{r}_2|}
\end{aligned}
$$

which is the fundamental Green's function of the modified Helmholtz equation, and

$$
\begin{aligned}
\lim_{|\V{r}_1-\V{r}_2|\to\infty}-\frac{e^{-k|\V{r}_1-\V{r}_2|}}{4\pi|\V{r}_1-\V{r}_2|}=0
\end{aligned}
$$

-----

### 10.2.7

Using the Poisson's equation for electrostatics:

$$
\begin{aligned}
\del^2\varphi=-\frac{\rho}{\varepsilon_0}
\end{aligned}
$$

For $\V{r}\neq0$,

$$
\begin{aligned}
\rho(\V{r})&=-\varepsilon_0\del^2\varphi(\V{r})\\
&=-\varepsilon_0\frac{Z}{4\pi\varepsilon_0}\frac{1}{r^2}\frac{d}{dr}\left[r^2\frac{d}{dr}(\frac{e^{-ar}}{r}) \right]\\
&=-\frac{Z}{4\pi}\frac{1}{r^2}\frac{d}{dr}\left[-ar\,e^{-ar}-e^{-ar} \right]\\
&=-\frac{Za^2}{4\pi}\frac{e^{-ar}}{r}
\end{aligned}
$$

For $\V{r}=0$, the function diverges, but for every $R>0$,

$$
\begin{aligned}
&\int\limits_{r<R}\rho(\V{r})d^3r=\int\limits_{r<R}-\varepsilon_0\del^2\varphi(\V{r})d^3r=-\frac{Z}{4\pi}\int\limits_{r<R}\del^2(\frac{e^{-ar}}{r})d^3r=-\frac{Z}{4\pi}\oint\limits_{r=R}\del(\frac{e^{-ar}}{r})\cdot d\boldsymbol{\sigma}=ZaR\,e^{-aR}+Ze^{-aR}
\end{aligned}
$$

Note that

$$
\begin{aligned}
\int\limits_{r<R}\frac{Za^2}{4\pi}\frac{e^{-ar}}{r}d^3r=\int_0^R\frac{Za^2}{4\pi}\frac{e^{-ar}}{r}4\pi r^2\,dr=Za^2\int_0^R re^{-ar}dr=-ZaR\,e^{-aR}-Ze^{-aR}+Z
\end{aligned}
$$

so for every $R$,

$$
\begin{aligned}
\int\limits_{r<R}\left[\rho(\V{r})+\frac{Za^2}{4\pi}\frac{e^{-ar}}{r} \right]d^3r=Z
\end{aligned}
$$

but

$$
\begin{aligned}
\rho(\V{r})+\frac{Za^2}{4\pi}\frac{e^{-ar}}{r}=0, \quad \textit{for $\V{r}\neq0$}
\end{aligned}
$$

which means

$$
\begin{aligned}
\rho(\V{r})+\frac{Za^2}{4\pi}\frac{e^{-ar}}{r}=Z\delta(r)
\end{aligned}
$$

Therefore,

$$
\begin{aligned}
\rho(\V{r})=Z\delta(r)-\frac{Za^2}{4\pi}\frac{e^{-ar}}{r}
\end{aligned}
$$

{% endraw %}
