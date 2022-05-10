---
layout: splash
title: "Mathematical Methods for Physicists Ch9"
permalink: /solutions/math_physics_09
author_profile: false

---

# Chapter 9: Partial Differential Equations



{% raw %}

## 9.2 First-Order Equations

### 9.2.1

Let $s=x+2y$, $t=2x-y$, then

$$
\newcommand{\pdv}[2]{\frac{\partial#1}{\partial#2}}
\newcommand{\V}{\mathbf}
\begin{aligned}
\pdv{\varphi}{x}=\pdv{\varphi}{s}+2\pdv{\varphi}{t}\\
\pdv{\varphi}{y}=2\pdv{\varphi}{s}-\pdv{\varphi}{t}
\end{aligned}
$$

so the equation becomes

$$
\begin{aligned}
5\pdv{\varphi}{s}+t\varphi&=0\\
\frac{1}{\varphi}d\varphi&=-\frac{t}{5}ds\\
\ln\varphi&=-\frac{ts}{5}+C(t)\\
\varphi&=e^{-\frac{1}{5}(2x^2-2y^2+3xy)}f(2x-y)
\end{aligned}
$$

Or note that $s+2t=5x$, so the solution can be transformed into

$$
\begin{aligned}
\varphi&=e^{-\frac{st}{5}}e^{-\frac{2t^2}{5}}e^{\frac{2t^2}{5}}f(t)
=e^{-\frac{5x\cdot t}{5}}g(t)\\
&=e^{-2x^2+xy}g(2x-y)
\end{aligned}
$$

-----

### 9.2.2

Let $s=x-2y$, $t=2x+y$, then

$$
\begin{aligned}
\pdv{\varphi}{x}&=\pdv{\varphi}{s}+2\pdv{\varphi}{t}\\
\pdv{\varphi}{y}&=-2\pdv{\varphi}{s}+\pdv{\varphi}{t}
\end{aligned}
$$

so the equation becomes

$$
\begin{aligned}
5\pdv{\varphi}{s}+\frac{3t-s}{5}&=0\\
\pdv{\varphi}{s}&=\frac{s-3t}{25}\\
\varphi&=\frac{s^2-6st}{50}+f(t)\\
&=\frac{s^2-6st}{50}+\frac{9t^2}{50}-\frac{9t^2}{50}+f(t)\\
&=\frac{(s-3t)^2}{50}+g(t)\\
&=\frac{(x+y)^2}{2}+g(2x+y)
\end{aligned}
$$

-----

### 9.2.3

Let $s=x+y-z,\;t=x-y,\;u=x+y+2z$, then

$$
\begin{aligned}
\pdv{\varphi}{x}&=\pdv{\varphi}{s}+\pdv{\varphi}{t}+\pdv{\varphi}{u}\\
\pdv{\varphi}{y}&=\pdv{\varphi}{s}-\pdv{\varphi}{t}+\pdv{\varphi}{u}\\
\pdv{\varphi}{x}&=-\pdv{\varphi}{s}+2\pdv{\varphi}{u}
\end{aligned}
$$

so the equation becomes

$$
\begin{aligned}
3\pdv{\varphi}{s}&=0\\
\varphi&=f(t,u)=f(x-y,x+y+2z)
\end{aligned}
$$

or note that $t+u=2(x+z)$, so the equation can be transformed into

$$
\begin{aligned}
\varphi=f(t,2(x+z)-t)=g(t,x+z)=g(x-y,x+z)
\end{aligned}
$$

-----

### 9.2.4

Let $s=x+y+z,\;t=x-y,\;u=x+y-2z$, then

$$
\begin{aligned}
\pdv{\varphi}{x}&=\pdv{\varphi}{s}+\pdv{\varphi}{t}+\pdv{\varphi}{u}\\
\pdv{\varphi}{y}&=\pdv{\varphi}{s}-\pdv{\varphi}{t}+\pdv{\varphi}{u}\\
\pdv{\varphi}{z}&=\pdv{\varphi}{s}-2\pdv{\varphi}{u}
\end{aligned}
$$

so the equation becomes

$$
\begin{aligned}
3\pdv{\varphi}{s}&=t\\
\varphi&=\frac{st}{3}+f(t,u)\\
&=\frac{st}{3}-\frac{ut}{3}+\frac{ut}{3}+f(t,u)\\
&=\frac{3z\cdot t}{3}+g(t,u)\\
&=(x-y)z+g(x-y,x+y-2z)
\end{aligned}
$$

-----

### 9.2.5

(a)

$$
\begin{aligned}
\pdv{\varphi}{x}&=\pdv{u}{x}\pdv{\varphi}{u}+\pdv{v}{x}\pdv{\varphi}{v}=y\pdv{\varphi}{u}+2x\pdv{\varphi}{v}\\
\pdv{\varphi}{y}&=\pdv{u}{y}\pdv{\varphi}{u}+\pdv{v}{y}\pdv{\varphi}{v}=x\pdv{\varphi}{u}-2y\pdv{\varphi}{v}
\end{aligned}
$$

so the equation becomes

$$
\begin{aligned}
&(x^2+y^2)\pdv{\varphi}{u}=0\\
&\varphi=f(v)=f(x^2-y^2)
\end{aligned}
$$

(b)
The characteristics are $x^2-y^2=constant$, which are hyperbolas centered at $(0,0)$ and with $x=y,\;x=-y$ as asymptotes. 

-----

### 9.2.6

Let $u=x^2-y^2,\;v=xy$, then

$$
\begin{aligned}
\pdv{\varphi}{x}&=\pdv{u}{x}\pdv{\varphi}{u}+\pdv{v}{x}\pdv{\varphi}{v}=2x\pdv{\varphi}{u}+y\pdv{\varphi}{v}\\
\pdv{\varphi}{y}&=\pdv{u}{y}\pdv{\varphi}{u}+\pdv{v}{y}\pdv{\varphi}{v}=-2y\pdv{\varphi}{u}+x\pdv{\varphi}{v}
\end{aligned}
$$

so the equation beocomes

$$
\begin{aligned}
&2(x^2+y^2)\pdv{\varphi}{u}=0\\
&\varphi=f(v)=f(xy)
\end{aligned}
$$

## 9.3 Second-Order Equations

### 9.3.1

$$
\begin{aligned}
\pdv{\varphi}{x}&=\pdv{\varphi}{\xi}\pdv{\xi}{x}+\pdv{\varphi}{\eta}\pdv{\eta}{x}=c^{\frac{1}{2}}\pdv{\varphi}{\xi}\\
\pdv{^2\varphi}{x^2}&=c^{\frac{1}{2}}\left(\pdv{^2\varphi}{\xi^2}\pdv{\xi}{x}+\pdv{^2\varphi}{\xi\partial\eta}\pdv{\eta}{x}\right)=c\pdv{^2\varphi}{\xi^2}\\
\pdv{^2\varphi}{x\partial y}&=c^{\frac{1}{2}}\left(\pdv{^2\varphi}{\xi^2}\pdv{\xi}{y}+\pdv{^2\varphi}{\xi\partial\eta}\pdv{\eta}{y} \right)=-b\pdv{^2\varphi}{\xi^2}+\pdv{^2\varphi}{\xi\partial\eta}\\
\pdv{\varphi}{y}&=\pdv{\varphi}{\xi}\pdv{\xi}{y}+\pdv{\varphi}{\eta}\pdv{\eta}{y}=-c^{-\frac{1}{2}}b\pdv{\varphi}{\xi}+c^{-\frac{1}{2}}\pdv{\varphi}{\eta}\\
\pdv{^2\varphi}{y^2}&=-c^{-\frac{1}{2}}b\left(\pdv{^2\varphi}{\xi^2}\pdv{\xi}{y}+\pdv{^2\varphi}{\xi\partial\eta}\pdv{\eta}{y} \right)+c^{-\frac{1}{2}}\left(\pdv{^2\varphi}{\xi\partial\eta}\pdv{\xi}{y}+\pdv{^2\varphi}{\eta^2}\pdv{\eta}{y} \right)=c^{-1}b^2\pdv{^2\varphi}{\xi^2}-2c^{-1}b\pdv{^2\varphi}{\xi\partial\eta}+c^{-1}\pdv{^2\varphi}{\eta^2}
\end{aligned}
$$

Substituting, we get

$$
\begin{aligned}
\mathcal{L}&=a\pdv{^2}{x^2}+2b\pdv{^2}{x\partial y}+c\pdv{^2}{y^2}\\
&=(ac-b^2)\pdv{^2}{\xi^2}+\pdv{^2}{\eta^2}
\end{aligned}
$$

## 9.4 Separation of Variables

### 9.4.1

$$
\begin{aligned}
(\nabla^2+k^2)(a_1\varphi_1+a_2\varphi_2)=a_1\nabla^2\varphi_1+a_1k^2\varphi_1+a_2\nabla^2\varphi_2+a_2k^2\varphi_2=a_1(\nabla^2+k^2)\varphi_1+a_2(\nabla^2+k^2)\varphi_2
\end{aligned}
$$

-----

### 9.4.2

Let $\varphi(\rho,\varphi,z)=P(\rho)\Phi(\varphi)Z(z)$ and substitute:

$$
\begin{aligned}
\frac{\Phi Z}{\rho}\frac{d}{d\rho}\left(\rho\frac{dP}{d\rho}\right)+\frac{PZ}{\rho^2}\frac{d^2\Phi}{d\varphi^2}+P\Phi\frac{d^2Z}{dz^2}+\left[k^2+f(\rho)+\frac{1}{\rho^2}g(\varphi)+h(z) \right]P\Phi Z=0
\end{aligned}
$$

The equation can be seperated into

$$
\begin{aligned}
&\frac{1}{Z}\frac{d^2Z}{dz^2}+h(z)=l^2\\
&\frac{1}{\Phi}\frac{d^2\Phi}{d\varphi^2}+g(\varphi)=-m^2\\
&\frac{\rho}{P}\frac{d}{d\rho}\left(\rho\frac{dP}{d\rho} \right)+\left[f(\rho)+l^2+k^2 \right]\rho^2-m^2=0
\end{aligned}
$$

-----

### 9.4.3

Let $\psi(r,\theta,\varphi)=R(r)\Theta(\theta)\Phi(\phi)$ and substitute, we have

$$
\begin{aligned}
\frac{1}{Rr^2}\frac{d}{dr}\left(r^2\frac{dR}{dr}\right)+\frac{1}{\Theta r^2\sin\theta}\frac{d}{d\theta}\left(\sin\theta\frac{d\Theta}{d\theta} \right)+\frac{1}{\Phi r^2\sin^2\theta}\frac{d^2\Phi}{d\varphi^2}=-k^2
\end{aligned}
$$

Ir can be rearranged into

$$
\begin{aligned}
\frac{1}{R}\frac{d}{dr}\left(r^2\frac{dR}{dr} \right)+r^2k^2=-\frac{1}{\Theta\sin\theta}\frac{d}{d\theta}\left(\sin\theta\frac{d\Theta}{d\theta} \right)-\frac{1}{\Phi\sin^2\theta}\frac{d^2\Phi}{d\varphi^2}
\end{aligned}
$$

By equating each side to $\lambda$ we can separate $R$. The rest of the equation can be rearranged into

$$
\begin{aligned}
\frac{1}{\Phi}\frac{d^2\Phi}{d\varphi^2}=-\frac{\sin\theta}{\Theta}\frac{d}{d\theta}\left(\sin\theta\frac{d\Theta}{d\theta} \right)-\lambda\sin^2\theta
\end{aligned}
$$

By equating each side to $-m^2$ we can separate $\Phi$ and $\Theta$. 

So the equation can be separated into

$$
\begin{aligned}
&\frac{1}{R}\frac{d}{dr}\left(r^2\frac{dR}{dr} \right)+r^2k^2=\lambda\\
&\frac{1}{\Phi}\frac{d^2\Phi}{d\varphi^2}=-m^2\\
-&\frac{\sin\theta}{\Theta}\frac{d}{d\theta}\left(\sin\theta\frac{d\Theta}{d\theta} \right)-\lambda\sin^2\theta=-m^2
\end{aligned}
$$

which are the same as equation (9.74), (9.77), and (9.78).

-----

### 9.4.4

Let $\psi(r,\theta,\varphi)=R(r)\Theta(\theta)\Phi(\varphi)$. Substitute and divide by $R\Theta\Phi$, we get

$$
\begin{aligned}
\frac{1}{Rr^2}\frac{d}{dr}\left(r^2\frac{dR}{dr} \right)+f(r)+\frac{1}{r^2}\left[\frac{1}{\Theta\sin\theta}\frac{d}{d\theta}\left(\sin\theta\frac{d\Theta}{d\theta} \right)+g(\theta) \right]+\frac{1}{r^2\sin^2\theta}\left[\frac{1}{\Phi}\frac{d^2\Phi}{d\varphi^2}+h(\varphi) \right]+k^2=0
\end{aligned}
$$

It can be seperated into

$$
\begin{aligned}
&\frac{1}{\Phi}\frac{d^2\Phi}{d\varphi^2}+h(\varphi)=-m^2\\
&\frac{1}{R}\frac{d}{dr}\left(r^2\frac{dR}{dr} \right)+r^2f(r)+r^2k^2=\lambda\\
-&\frac{1}{\Theta\sin\theta}\frac{d}{d\theta}\left(\sin\theta\frac{d\Theta}{d\theta} \right)-g(\theta)+\frac{m^2}{\sin^2\theta}=\lambda
\end{aligned}
$$

-----

### 9.4.5

Let $\psi(x,y,z)=X(x)Y(y)Z(z)$ and substitute, we have

$$
\begin{aligned}
YZ\frac{d^2X}{dx^2}+XZ\frac{d^2Y}{dy^2}+XY\frac{d^2Z}{dz^2}+\frac{2mE}{\hbar^2}XYZ=0
\end{aligned}
$$

It can be separated into

$$
\begin{aligned}
\frac{1}{X}\frac{d^2X}{dx^2}=-l^2\qquad \frac{1}{Y}\frac{d^2Y}{dy^2}=-m^2\qquad \frac{1}{Z}\frac{d^2Z}{dz^2}=-n^2
\end{aligned}
$$

where $l^2+m^2+n^2=\frac{2mE}{\hbar^2}$.

The solution of $X$ is $X=A\sin lx+B\cos lx$. When the boundary conditions $X(0)=X(a)=0$ ia applied, we must require $B=0$ and $la=\lambda\pi$, where $\lambda$ is a positive integer. Similarly $mb=\mu\pi$, $nc=\nu\pi$, where $\mu,\nu$ are positive integers. So

$$
\begin{aligned}
E=\frac{\hbar^2}{2m}(l^2+m^2+n^2)=\frac{\pi^2\hbar^2}{2m}\left(\frac{\lambda^2}{a^2}+\frac{\mu^2}{b^2}+\frac{\nu^2}{c^2}\right)
\end{aligned}
$$

and the minimum of $E$ is

$$
\begin{aligned}
E_{min}=\frac{\pi^2\hbar^2}{2m}\left(\frac{1}{a^2}+\frac{1}{b^2}+\frac{1}{c^2}\right)
\end{aligned}
$$

in which case $\lambda=\mu=\nu=1$.
 
-----

### 9.4.6

From Exercise 3.10.32 (c), we have

$$
\begin{aligned}
\V{L}^2=-\frac{1}{\sin\theta}\pdv{}{\theta}\left(\sin\theta\pdv{}{\theta}\right)-\frac{1}{\sin^2\theta}\pdv{^2}{\varphi^2}
\end{aligned}
$$

Let $\psi(r,\theta,\varphi)=R(r)\Theta(\theta)\Phi(\varphi)$. Substitute into the equation and divide by $R\Theta\Phi$, we have

$$
\begin{aligned}
-\frac{1}{\Theta\sin\theta}\pdv{}{\theta}\left(\sin\theta\pdv{\Theta}{\theta} \right)-\frac{1}{\Phi\sin^2\theta}\pdv{^2\Phi}{\varphi^2}=l(l+1)
\end{aligned}
$$

which can be separated into

$$
\begin{aligned}
\frac{1}{\Phi}\pdv{^2\Phi}{\varphi^2}=-m^2
\end{aligned}
$$

and

$$
\begin{aligned}
\frac{1}{\sin\theta}\pdv{}{\theta}\left(\sin\theta\pdv{\Theta}{\theta} \right)-\frac{m^2}{\sin^2\theta}\Theta+l(l+1)\Theta=0
\end{aligned}
$$

Let $t=\cos\theta$ and $\Theta(\theta)=P(\cos\theta)=P(t)$, the $\Theta$ equation becomes

$$
\begin{aligned}
(1-t^2)P''(t)-2tP'(t)-\frac{m^2}{1-t^2}P(t)+l(l+1)P(t)=0
\end{aligned}
$$

which is the associated Legendre equation. 

-----

### 9.4.7

(a) Multiply the equation by $-\frac{2}{\hbar}\left(\frac{m}{k} \right)^{1/2}$ and use the definitions of $a$ and $\lambda$, we have

$$
\begin{aligned}
\frac{1}{a^2}\frac{d^2\psi}{dx^2}-a^2x^2\psi+\lambda\psi=0
\end{aligned}
$$

Note that $\frac{d^2\psi}{dx^2}=\frac{d^2\psi}{d\xi^2}\left(\frac{d\xi}{dx} \right)^2=a^2\frac{d^2\psi}{d\xi^2}$, and $a^2x^2=\xi^2$, we have

$$
\begin{aligned}
\frac{d^2\psi}{d\xi^2}+(\lambda-\xi^2)\psi=0
\end{aligned}
$$

(b)

$$
\begin{aligned}
\frac{d\psi}{d\xi}&=\left[y'(\xi)-\xi y(\xi) \right]e^{-\frac{\xi^2}{2}}\\
\frac{d^2\psi}{d\xi^2}&=\left[y''(\xi)-2\xi y'(\xi)+(\xi^2-1)y(\xi) \right]e^{-\frac{\xi^2}{2}}
\end{aligned}
$$

Substitute and eliminate $e^{-\frac{\xi^2}{2}}$, we have

$$
\begin{aligned}
y''(\xi)-2\xi y'(\xi)+(\lambda-1)y(\xi)=0
\end{aligned}
$$

which is the Hermite differential equation.

## 9.5 Laplace and Poisson Equations

### 9.5.1

(a) Using Equation (3.158),

$$
\begin{aligned}
\nabla^2\varphi_1=\frac{1}{r^2}\pdv{}{r}\left(r^2\pdv{(\frac{1}{r})}{r} \right)=\frac{1}{r^2}\pdv{}{r}(-1)=0
\end{aligned}
$$

(b)
Substitute $r\cos\theta$ for $z$, then

$$
\begin{aligned}
\varphi_2&=\frac{1}{2r}\ln\frac{1+\cos\theta}{1-\cos\theta}\\
\pdv{\varphi_2}{r}&=-\frac{1}{2r^2}\ln\frac{1+\cos\theta}{1-\cos\theta}\\
\pdv{\varphi_2}{\theta}&=-\frac{1}{r\sin\theta}
\end{aligned}
$$

Using Equation (3.158),

$$
\begin{aligned}
\nabla^2\varphi_2&=\frac{1}{r^2}\pdv{}{r}\left(r^2\pdv{\varphi_2}{r} \right)+\frac{1}{r^2\sin\theta}\pdv{}{\theta}\left(\sin\theta\pdv{\varphi_2}{\theta} \right)\\
&=\frac{1}{r^2}\pdv{}{r}\left(-\frac{1}{2}\ln\frac{1+\cos\theta}{1-\cos\theta} \right)+\frac{1}{r^2\sin\theta}\pdv{}{\theta}\left(-\frac{1}{r} \right)=0
\end{aligned}
$$

-----

### 9.5.2

$$
\begin{aligned}
\nabla^2\Psi=\pdv{^2\Psi}{x^2}+\pdv{^2\Psi}{y^2}+\pdv{^2\Psi}{z^2}=0
\end{aligned}
$$

so

$$
\begin{aligned}
\nabla^2\left(\pdv{\Psi}{z}\right)&=\pdv{^3\Psi}{x^2\partial z}+\pdv{^3\Psi}{y^2\partial z}+\pdv{^3\Psi}{z^3}\\
&=\pdv{}{z}\left(\pdv{^2\Psi}{x^2}+\pdv{^2\Psi}{y^2}+\pdv{^2\Psi}{z^2}\right)=0
\end{aligned}
$$

which means $\pdv{\Psi}{z}$ is also a solution of Laplace's equation.

-----

### 9.5.3

Suppose $\psi_1$ and $\psi_2$ are distinct solutions to the Laplace or Poisson equation for the same Dirichlet boundary conditions, then $\psi=\psi_1-\psi_2$ will also be a solution to the Laplace equation with a zero Dirichlet boundary conditions. From Eq. (9.88),

$$
\begin{aligned}
\int\limits_S\psi\pdv{\psi}{\V{n}}dS=\int\limits_V\psi\nabla^2\psi\,d\tau+\int\limits_V   \nabla\psi\cdot\nabla\psi\,d\tau
\end{aligned}
$$

$\int\limits_S\psi\pdv{\psi}{\V{n}}dS$ vanishes because $\psi$ vanishes on the boundary. $\int\limits_V\psi\nabla^2\psi\,d\tau$ vanishes because $\psi$ is a solution to the Laplace equation. Therefore $\int\limits_V   \nabla\psi\cdot\nabla\psi\,d\tau$ must vanish, which means $\nabla\psi=0$ everywhere, so $\psi=constant=0$ because it is zero on the boundary. So $\psi_1=\psi_2$, which means the solution is unique.

## 9.6 Wave Equation 

### 9.6.1

Using the d’Alembert’s solution:

$$
\begin{aligned}
\psi(x,t)&=\frac{1}{2}\left[\psi(x+ct,0)+\psi(x-ct,0)\right]+\frac{1}{2c}\int_{x-ct}^{x+ct}\pdv{\psi(x,0)}{t}dx\\
&=\frac{1}{2}\left[\sin(x+ct)+\sin(x-ct)\right]+\frac{1}{2c}\int_{x-ct}^{x+ct}\cos x\,dx\\
&=\sin x\cos ct+\frac{1}{c}\cos x\sin ct
\end{aligned}
$$

-----

### 9.6.2

$$
\begin{aligned}
\psi(x,t)&=\frac{1}{2}\left[\psi(x+ct,0)+\psi(x-ct,0)\right]+\frac{1}{2c}\int_{x-ct}^{x+ct}\pdv{\psi(x,0)}{t}dx\\
&=\frac{1}{2}\left[\delta(x+ct)+\delta(x-ct)\right]
\end{aligned}
$$

-----

### 9.6.3

$$
\begin{aligned}
\psi(x,t)&=\frac{1}{2}\left[\psi(x+ct,0)+\psi(x-ct,0)\right]+\frac{1}{2c}\int_{x-ct}^{x+ct}\pdv{\psi(x,0)}{t}dx\\
&=\frac{1}{2}\left[\psi_0(x+ct)+\psi_0(x-ct)\right]
\end{aligned}
$$

where $\psi_0$ is the given square-wave pulse.

-----

### 9.6.4

$$
\begin{aligned}
\psi(x,t)&=\frac{1}{2}\left[\psi(x+ct,0)+\psi(x-ct,0)\right]+\frac{1}{2c}\int_{x-ct}^{x+ct}\pdv{\psi(x,0)}{t}dx\\
&=\frac{1}{2c}\int_{x-ct}^{x+ct}\sin x\,dx
=\frac{1}{2c}\left[\cos(x-ct)-\cos(x+ct) \right]
=\frac{1}{c}\sin x\cos ct
\end{aligned}
$$

## 9.7 Heat-Flow, or Diffusion PDE

### 9.7.1

Substitute $T(r,t)=R(r)T(t)$ into the equation, we have

$$
\begin{aligned}
R\pdv{T}{t}=KT\nabla^2R=KT\frac{1}{r^2}\pdv{}{r}\left(r^2\pdv{R}{r} \right)
\end{aligned}
$$

which can be separated into

$$
\begin{aligned}
\frac{1}{KT}\pdv{T}{t}=\frac{1}{Rr^2}\left(r^2\pdv{^2R}{r^2}+2r\pdv{R}{r} \right)=-\alpha^2
\end{aligned}
$$

so the $R$ equation is

$$
\begin{aligned}
r^2\frac{d^2R}{dr^2}+2r\frac{dR}{dr}+\alpha^2r^2R=0
\end{aligned}
$$

For $R=\frac{\sin\alpha r}{r}$:

$$
\begin{aligned}
&r^2\pdv{^2R}{r^2}+2r\pdv{R}{r}+\alpha^2r^2R\\
=&\frac{d}{dr}\left(r^2\frac{dR}{dr}\right)+\alpha^2r^2R\\
=&\frac{d}{dr}\left(\alpha r\cos\alpha r-\sin\alpha r\right)+\alpha^2r\sin\alpha r\\
=&\alpha\cos\alpha r-\alpha^2r\sin\alpha r-\alpha\cos\alpha r+\alpha^2 r\sin\alpha r=0
\end{aligned}
$$

For $R=\frac{\cos\alpha r}{r}$:

$$
\begin{aligned}
&r^2\pdv{^2R}{r^2}+2r\pdv{R}{r}+\alpha^2r^2R\\
=&\frac{d}{dr}\left(r^2\frac{dR}{dr}\right)+\alpha^2r^2R\\
&\frac{d}{dr}\left(-\alpha r\sin\alpha r-\cos\alpha r\right)+\alpha^2r\cos\alpha r\\
=&-\alpha\sin\alpha r-\alpha^2r\cos\alpha r+\alpha\sin\alpha r+\alpha^2r\cos\alpha r=0
\end{aligned}
$$

so $\frac{\sin\alpha r}{r}$ and $\frac{\cos\alpha r}{r}$ are solutions to the equation.

-----

### 9.7.2

Substitute $T(\rho,t)=P(\rho)T(t)$ into the equation, we have

$$
\begin{aligned}
P\pdv{T}{t}=KT\nabla^2P=KT\frac{1}{\rho}\pdv{}{\rho}\left(\rho\pdv{P}{\rho}\right)
\end{aligned}
$$

which can be separated into

$$
\begin{aligned}
\frac{1}{KT}\pdv{T}{t}=\frac{1}{P\rho}\left(\rho\pdv{^2P}{\rho^2}+\pdv{P}{\rho}\right)=-\alpha^2
\end{aligned}
$$

so

$$
\begin{aligned}
\frac{dT}{dt}+\alpha^2KT&=0\\
\rho\frac{d^2P}{d\rho^2}+\frac{dP}{d\rho}+\alpha^2\rho P&=0
\end{aligned}
$$

-----

### 9.7.3

Use Equation 9.114:

$$
\begin{aligned}
\psi(x,t)&=\frac{1}{\sqrt{\pi}}\int_{-\infty}^\infty A\delta(x-2a\xi\sqrt{t})e^{-\xi^2}d\xi\\
&=\frac{A}{\sqrt{\pi}}\int_{-\infty}^{\infty}\delta(x-y)e^{-\frac{y^2}{4a^2t}}\frac{dy}{2a\sqrt{t}}\\
&=\frac{A}{2a\sqrt{\pi t}}e^{-\frac{x^2}{4a^2t}}
\end{aligned}
$$

-----

### 9.7.4

From Equation 9.101, the solutions have the form

$$
\begin{aligned}
\psi(x,t)=(A\cos\omega x+B\sin\omega x)e^{-\omega^2a^2t}+C_0'x+C_0
\end{aligned}
$$

Using the boundary conditions:

$$
\begin{aligned}
    & \psi(0,\infty)=C_0=1\qquad && C_0=1\\
    & \psi(L,\infty)=C_0'L+C_0=0\qquad && C_0'=-\frac{1}{L}\\
    & \psi(0,t)=Ae^{-\omega^2 a^2t}+1=1\qquad && A=0\\\
    & \psi(L,t)=B\sin(\omega L)\,e^{-\omega^2a^2t}=0\qquad && \omega L=n\pi\qquad\textit{n is a positive integer}
\end{aligned}
$$

So

$$
\begin{aligned}
\psi(x,t)=\sum_{n=1}^\infty a_n\sin\left(\frac{n\pi x}{L}\right)e^{-\frac{n^2\pi^2a^2}{L^2}t}-\frac{x}{L}+1
\end{aligned}
$$

To determine $a_n$, use $\psi(x,0)=0$ and the orthogonality $\int_0^L\sin\left(\frac{n\pi x}{L}\right)\sin\left(\frac{m\pi x}{L}\right)dx=\frac{L}{2}\delta_{nm}$:

$$
\begin{aligned}
\int_0^L\psi(x,0)\sin\left(\frac{n\pi x}{L}\right)dx=\frac{L}{2}a_n+\frac{L}{n\pi}=0
\end{aligned}
$$

so $a_n=-\frac{2}{n\pi}$, and the overall solution is

$$
\begin{aligned}
\psi(x,t)=-\sum_{n=1}^\infty \frac{2}{n\pi}\sin\left(\frac{n\pi x}{L}\right)e^{-\frac{n^2\pi^2a^2}{L^2}t}-\frac{x}{L}+1
\end{aligned}
$$

It can be verified that the solution satisfies the boundary, initial conditions and the PDE.

{% endraw %}
