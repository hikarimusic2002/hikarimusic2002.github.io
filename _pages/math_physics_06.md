---
layout: splash
title: "Mathematical Methods for Physicists Ch6"
permalink: /solutions/math_physics_06
author_profile: false

---

# Chapter 6 Eigenvalue Problems

{% raw %}

## 6.2 Matrix Eigenvalue Problems

### 6.2.1

$$
\newcommand{\br}[2]{\langle#1|#2\rangle}
\newcommand{\brr}[2]{\left\langle#1|#2\right\rangle}
\newcommand{\pdv}[2]{\frac{\partial#1}{\partial#2}}
\newcommand{\M}{\mathrm}
\newcommand{\V}{\mathbf}
\newcommand{\VE}{\mathbf{\hat{e}}}
\newcommand{\ket}[1]{|#1\rangle}
\newcommand{\bra}[1]{\langle#1|}
\newcommand{\n}{\lambda}
\begin{aligned}
\begin{vmatrix}
1-\n&0&1\\
0&1-\n&0\\
1&0&1-\n
\end{vmatrix}=
(1-\n)(2-\n)(-\n)=0
\end{aligned}
$$

$$
\begin{aligned}
& \n_1=0,\qquad && x_1+x_3=0,\qquad && x_2=0,\qquad && \V{c}_1=\frac{1}{\sqrt{2}}(1,0,-1)\\
& \n_2=1,\qquad && x_3=0,\qquad && x_1=0,\qquad && \V{c}_2=(0,1,0)\\
& \n_3=2,\qquad && -x_1+x_3=0,\qquad && -x_2=0,\qquad && \V{c}_3=\frac{1}{\sqrt{2}}(1,0,1)\\
\end{aligned}
$$

-----

### 6.2.2

$$
\begin{aligned}
\begin{vmatrix}
1-\n&\sqrt{2}&0\\
\sqrt{2}&-\n&0\\
0&0&-\n
\end{vmatrix}=
-\n(\n-2)(\n+1)=0
\end{aligned}
$$

$$
\begin{aligned}
& \n_1=-1,\qquad && 2x_1+\sqrt{2}x_2=0,\qquad && x_3=0,\qquad && \V{c}_1=\frac{1}{\sqrt{3}}(1,-\sqrt{2},0)\\
& \n_2=0,\qquad && x_1+\sqrt{2}x_2=0,\qquad && \sqrt{2}x_1=0,\qquad && \V{c}_2=(0,0,1)\\
& \n_3=2,\qquad && -x_1+\sqrt{2}x_2=0,\qquad && -2x_3=0,\qquad && \V{c}_3=\frac{1}{\sqrt{3}}(\sqrt{2},1,0)\\
\end{aligned}
$$

-----

### 6.2.3

$$
\begin{aligned}
\begin{vmatrix}
1-\n&1&0\\
1&-\n&1\\
0&1&1-\n
\end{vmatrix}=
(1-\n)(\n-2)(\n+1)=0
\end{aligned}
$$

$$
\begin{aligned}
& \n_1=-1,\qquad && 2x_1+x_2=0,\qquad && x_1+x_2+x_3=0,\qquad && \V{c}_1=\frac{1}{\sqrt{6}}(1,-2,1)\\
& \n_2=1,\qquad && x_2=0,\qquad && x_1-x_2+x_3=0,\qquad && \V{c}_2=\frac{1}{\sqrt{2}}(1,0,-1)\\
& \n_3=2,\qquad && -x_1+x_2=0,\qquad && x_1-2 x_2+x_3=0,\qquad && \V{c}_3=\frac{1}{\sqrt{3}}(1,1,1)\\
\end{aligned}
$$

-----

### 6.2.4

$$
\begin{aligned}
\begin{vmatrix}
 1-\n&\sqrt{8} &0 \\
 \sqrt{8}& 1-\n&\sqrt{8} \\
0 &\sqrt{8} & 1-\n
\end{vmatrix}=
(1-\n)(5-\n)(-3-\n)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1=-3 ,\qquad && 4x_1+\sqrt{8}x_2=0,\qquad && \sqrt{8}x_2+4x_3=0,\qquad && \V{c}_1=\frac{1}{2}(1,-\sqrt{2},1)\\
    & \n_2=1 ,\qquad && \sqrt{8}x_2=0,\qquad && \sqrt{8}x_1+\sqrt{8}x_3=0,\qquad && \V{c}_2=\frac{1}{\sqrt{2}}(1,0,-1)\\
    & \n_3=5 ,\qquad && -4x_1+\sqrt{8}x_2=0,\qquad && \sqrt{8}x_2-4x_3=0,\qquad && \V{c}_3=\frac{1}{2}(1,\sqrt{2},1)\\
\end{aligned}
$$

-----

### 6.2.5

$$
\begin{aligned}
\begin{vmatrix}
 1-\n& 0& 0\\
 0& 1-\n&1 \\
 0& 1& 1-\n
\end{vmatrix}=
(1-\n)(2-\n)(-\n)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1=0 ,\qquad && x_1=0,\qquad && x_2+x_3=0,\qquad && \V{c}_1=\frac{1}{\sqrt{2}}(0,1,-1)\\
    & \n_2=1 ,\qquad && x_3=0,\qquad && x_2=0,\qquad && \V{c}_2=(1,0,0)\\
    & \n_3=2 ,\qquad && -x_1=0,\qquad && -x_2+x_3=0,\qquad && \V{c}_3=\frac{1}{\sqrt{2}}(0,1,1)\\
\end{aligned}
$$

-----

### 6.2.6

$$
\begin{aligned}
\begin{vmatrix}
 1-\n& 0& 0\\
 0& 1-\n& \sqrt{2}\\
 0&\sqrt{2} & -\n
\end{vmatrix}=
(1-\n)(\n-2)(\n+1)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1=-1 ,\qquad && 2x_1=0,\qquad && 2x_2+\sqrt{2}x_3=0,\qquad && \V{c}_1=\frac{1}{\sqrt{3}}(0,-1,\sqrt{2})\\
    & \n_2=1 ,\qquad && \sqrt{2}x_3=0,\qquad && \sqrt{2}x_2-x_3=0,\qquad && \V{c}_2=(1,0,0)\\
    & \n_3=2 ,\qquad && -x_1=0,\qquad && -x_2+\sqrt{2}x_3=0,\qquad && \V{c}_3=\frac{1}{\sqrt{3}}(0,\sqrt{2},1)\\
\end{aligned}
$$

-----

### 6.2.7

$$
\begin{aligned}
\begin{vmatrix}
 -\n&1 &0 \\
 1& -\n&1 \\
 0& 1& -\n
\end{vmatrix}=
(-\n)(\n+\sqrt{2})(\n-\sqrt{2})=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1=-\sqrt{2} ,\qquad && \sqrt{2}x_1+x_2=0,\qquad && x_2+\sqrt{2}x_3=0,\qquad && \V{c}_1=\frac{1}{2}(1,-\sqrt{2},1)\\
    & \n_2=0 ,\qquad && x_2=0,\qquad && x_1+x_3=0,\qquad && \V{c}_2=\frac{1}{\sqrt{2}}(1,0,-1)\\
    & \n_3=\sqrt{2} ,\qquad && -\sqrt{2}x_1+x_2=0,\qquad && x_2-\sqrt{2}x_3=0,\qquad && \V{c}_3=\frac{1}{2}(1,\sqrt{2},1)\\
\end{aligned}
$$

-----

### 6.2.8

$$
\begin{aligned}
\begin{vmatrix}
 2-\n&0 &0 \\
 0& 1-\n&1 \\
 0&1 & 1-\n
\end{vmatrix}=
(2-\n)(2-\n)(-\n)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1=0 ,\qquad && 2x_1=0,\qquad && x_2+x_3=0,\qquad && \V{c}_1=\frac{1}{\sqrt{2}}(0,1,-1)\\
    & \n_{2,3}=2 ,\qquad && -x_2+x_3=0,\qquad && \qquad && \V{c}_2=(1,0,0)\qquad&&\textit{(not unique)}\\
    &\qquad && \qquad && \qquad && \V{c}_3=\frac{1}{\sqrt{2}}(0,1,1)\qquad&&\textit{(not unique)}\\
\end{aligned}
$$

-----

### 6.2.9

$$
\begin{aligned}
\begin{vmatrix}
 -\n&1&1 \\
1 & -\n& 1\\
1 & 1& -\n
\end{vmatrix}=
-(\n+1)(\n-2)(\n+1)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_{1,2}=-1 ,\qquad && x_1+x_2+x_3=0,\qquad && \qquad && \V{c}_1=\frac{1}{\sqrt{2}}(1,-1,0)\quad &&\textit{(not unique)}\\
    & \qquad && \qquad && \qquad && \V{c}_2=\frac{1}{\sqrt{6}}(1,1,-2)\qquad &&\textit{(not unique)}\\
    & \n_3=2 ,\qquad && -2x_1+x_2+x_3=0,\qquad && x_1+x_2-2x_3=0,\qquad && \V{c}_3=\frac{1}{\sqrt{3}}(1,1,1) \\
\end{aligned}
$$

-----

### 6.2.10

$$
\begin{aligned}
\begin{vmatrix}
 1-\n&-1 &-1 \\
 -1& 1-\n& -1\\
 -1&-1 & 1-\n
\end{vmatrix}=
-(\n-2)(\n-2)(\n+1)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1=-1 ,\qquad && 2x_1-x_2-x_3=0,\qquad && -x_1-x_2+2x_3=0,\qquad && \V{c}_1=\frac{1}{\sqrt{3}}(1,1,1)\\
    & \n_{2,3}=2 ,\qquad && -x_1-x_2-x_3=0,\qquad && \qquad && \V{c}_2=\frac{1}{\sqrt{2}}(1,-1,0)  \quad &&\textit{(not unique)}\\
    &  \qquad && \qquad && \qquad && \V{c}_3=  \frac{1}{\sqrt{6}}(1,1,-2)\quad &&\textit{(not unique)}\\
\end{aligned}
$$

-----

### 6.2.11

$$
\begin{aligned}
\begin{vmatrix}
 1-\n&1 &1 \\
 1& 1-\n&1 \\
 1& 1& 1-\n
\end{vmatrix}=
-\n^2(\n-3)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_{1,2}=0 ,\qquad && x_1+x_2+x_3=0,\qquad && \qquad && \V{c}_1=\frac{1}{\sqrt{2}}(1,-1,0)  \quad &&\textit{(not unique)}\\
    &  \qquad && \qquad && \qquad && \V{c}_2=\frac{1}{\sqrt{6}}(1,1,-2)  \quad &&\textit{(not unique)}\\
    & \n_3=3 ,\qquad && -2x_1+x_2+x_3=0,\qquad && x_1+x_2-2x_3=0,\qquad && \V{c}_3=\frac{1}{\sqrt{3}}(1,1,1)\\
\end{aligned}
$$

-----

### 6.2.12

$$
\begin{aligned}
\begin{vmatrix}
 5-\n&0 &2 \\
 0& 1-\n&0 \\
 2& 0& 2-\n
\end{vmatrix}=
-(\n-1)(\n-6)(\n-1)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_{1,2}=1 ,\qquad && 2x_1+x_3=0,\qquad && \qquad && \V{c}_1=(0,1,0)  \quad &&\textit{(not unique)}\\
    & \qquad && \qquad && \qquad && \V{c}_2=\frac{1}{\sqrt{5}}(1,0,-2)  \quad &&\textit{(not unique)}\\
    & \n_3=6 ,\qquad && -x_1+2x_3=0,\qquad && -5x_2=0,\qquad && \V{c}_3=\frac{1}{\sqrt{5}}(2,0,1)  \\
\end{aligned}
$$

-----

### 6.2.13

$$
\begin{aligned}
\begin{vmatrix}
 1-\n& 1&0 \\
 1& 1-\n&0 \\
 0& 0& -\n
\end{vmatrix}=
-\n^2(\n-2)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_{1,2}=0 ,\qquad && x_1+x_2=0,\qquad && \qquad && \V{c}_1=(0,0,1)  \quad &&\textit{(not unique)}\\
    & \qquad && \qquad && \qquad && \V{c}_2=\frac{1}{\sqrt{2}}(1,-1,0)  \quad &&\textit{(not unique)}\\
    & \n_3=2 ,\qquad && -x_1+x_2=0,\qquad && -2x_3=0,\qquad && \V{c}_3=\frac{1}{\sqrt{2}}(1,1,0)  \\
\end{aligned}
$$

-----

### 6.2.14

$$
\begin{aligned}
\begin{vmatrix}
 5-\n&0 &\sqrt{3} \\
 0& 3-\n&0 \\
 \sqrt{3}&0 & 3-\n
\end{vmatrix}=
-(\n-3)(\n-6)(\n-2)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1=2 ,\qquad && \sqrt{3}x_1+x_3=0,\qquad && x_2=0,\qquad && \V{c}_1=\frac{1}{2}(1,0,-\sqrt{3})\\
    & \n_2=3 ,\qquad && 2x_1+\sqrt{3}x_3=0,\qquad && \sqrt{3}x_1=0,\qquad && \V{c}_2=(0,1,0)\\
    & \n_3=6 ,\qquad && -x_1+\sqrt{3}x_3=0,\qquad && -3x_2=0,\qquad && \V{c}_3=\frac{1}{2}(\sqrt{3},0,1)\\
\end{aligned}
$$

-----

### 6.2.15



For every real coefficient homogeneous quadratic function (equation) in three variables 

$$
\begin{aligned}
\renewcommand{\arraystretch}{1.5}
a_{11}x^2+a_{22}y^2+a_{33}z^2+a_{12}xy+a_{13}xz+a_{23}yz=1
\end{aligned}
$$

it can be verified that it is equivalent to the matrix equation 

$$
\begin{aligned}
\begin{pmatrix}
x,y,z
\end{pmatrix}
\begin{pmatrix}
a_{11}&\frac{a_{12}}{2}&\frac{a_{13}}{2}\\
\frac{a_{12}}{2}&a_{22}&\frac{a_{23}}{2}\\
\frac{a_{13}}{2}&\frac{a_{23}}{2}&a_{33}
\end{pmatrix}
\begin{pmatrix}
x\\y\\z
\end{pmatrix}=1
\end{aligned}
$$

Note that the middle matrix is Hermitian, so it can be diagonalized by a unitary transformation, which will transform the equation to 

$$
\begin{aligned}
\begin{pmatrix}
x',y',z'
\end{pmatrix}
\begin{pmatrix}
\n_1&0&0\\
0&\n_2&0\\
0&0&\n_3
\end{pmatrix}
\begin{pmatrix}
x'\\y'\\z'
\end{pmatrix}=1
\end{aligned}
$$

or $\n_1(x')^2+\n_2(y')^2+\n_3(z')^2=1$, which can be an ellipsoid, hyperboloid, elliptic cylinder, hyperbolic cylinder, or two parallel planes, depends on the sign of $\n_1,\n_2,\n_3$.


$x^2+2xy+2y^2+2yz+z^2=1$ is equivalent to 

$$
\renewcommand{\arraystretch}{1}
\begin{aligned}
\begin{pmatrix}
x,y,z
\end{pmatrix}
\begin{pmatrix}
1&1&0\\
1&2&1\\
0&1&1
\end{pmatrix}
\begin{pmatrix}
x\\y\\z
\end{pmatrix}=1
\end{aligned}
$$

Find the eigenvectors to diagonalize it:

$$
\begin{aligned}
\begin{vmatrix}
1-\n&1&0\\
1&2-\n&1\\
0&1&1-\n
\end{vmatrix}=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1=0 ,\qquad && x_1+x_2=0,\qquad && x_2+x_3=0,\qquad && \V{c}_1=\frac{1}{\sqrt{3}}(1,-1,1)\\
    & \n_2=1 ,\qquad && x_2=0,\qquad && x_1+x_2+x_3=0,\qquad && \V{c}_2=\frac{1}{\sqrt{2}}(1,0,-1)\\
    & \n_3=3 ,\qquad && -2x_1+x_2=0,\qquad && x_2-2x_3=0,\qquad && \V{c}_3=\frac{1}{\sqrt{6}}(1,2,1)\\
\end{aligned}
$$

Transform into the $\V{c}_1,\V{c}_2,\V{c}_3$ basis, the equation becomes

$$
\begin{aligned}
\begin{pmatrix}
x',y',z'
\end{pmatrix}
\begin{pmatrix}
0&0&0\\
0&1&0\\
0&0&3
\end{pmatrix}
\begin{pmatrix}
x'\\y'\\z'
\end{pmatrix}=1
\end{aligned}
$$

or

$$
\begin{aligned}
(y')^2+3(z')^2=1
\end{aligned}
$$

which is an elliptic cylinder.
The axis of cylinder is in the $x'$ direction, which is the $\V{c}_1$ direction, $(1,-1,1)$.
The major axis of ellipse is in the $y'$ direction,  which is the $\V{c}_2$ direction, $(1,0,-1)$, with the length of semi-major axis being $1$.
The minor axis of ellipse is in the $z'$ direction,  which is the $\V{c}_3$ direction, $(1,2,1)$, with the length of semi-minor axis being $\frac{1}{\sqrt{3}}$.

## 6.4 Hermitian Matrix Diagonalization

### 6.4.1

$$
\begin{aligned}
\M{A}\V{x}&=\n\V{x}\\
\M{G}\M{A}\M{G}^{-1}\M{G}\V{x}&=\n\M{G}\V{x}\\
\M{A}'\V{x}'&=\n\V{x}'
\end{aligned}
$$

the same is for the transformation from $\M{A}'$ to $\M{A}$. So if $\n$ is an eigenvalue of $\M{A}$, it is an eigenvalue of $\M{A}'$, and vice versa. So $\M{A}'$ and $\M{A}$ have the same eigenvalues (though the eigenvectors may be different.)

The invariance of trace and determinant under similarity transformation can be shown by the invariance of eigenvalues along with the fact that sum of eigenvalues equals trace (compare the coefficient of $\n^{n-1}$ in $\det(\M{A}-\n \M{I})=(-1)^n(\n^n-(\mathrm{tr} \M{A})\n^{n-1}+\cdots)=(-1)^n(\n-\n_1)\cdots(\n-\n_n)$\;) and product of eigenvalues equals determinant (let $\n=0$ in $\det(\M{A}-\n \M{I})=(\n_1-\n)\cdots(\n_n-\n)$). However, they can be proved more simply by

$$
\newcommand{\tr}{\mathrm{tr}}
\begin{aligned}
\tr(\M{G}\M{A}\M{G}^{-1})&=\tr(\M{A}\M{G}^{-1}\M{G})=\tr(\M{A})\\
\det(\M{G}\M{A}\M{G}^{-1})&=\det(\M{G})\det(\M{A})\det(\M{G}^{-1})=\det(\M{A})
\end{aligned}
$$

-----

### 6.4.2

(The theorem is correct only when the eigenvectors form a complete set, which means the number of independent eigenvectors is equal to the dimension of the matrix.)

If matrix $\M{A}$ has real eigenvalues and orthonormal eigenvectors, then by transforming into the basis of the eigenvectors , it will be diagonalized, with the diagonal components being the real eigenvalues:

$$
\begin{aligned}
\M{A}=\M{U}\M{A'}\M{U}^{-1}
\end{aligned}
$$

($\M{U}$ is unitary, $\M{A'}$ is diagonal and real, and therefore Hermitian)

$$
\begin{aligned}
\M{A}^\dagger=(\M{U}\M{A'}\M{U}^{-1})^\dagger=(U^{-1})^\dagger(A')^\dagger(U)^\dagger=\M{U}\M{A'}\M{U}^{-1}=\M{A}
\end{aligned}
$$

so $\M{A}$ is Hermitian.

-----

### 6.4.3

(A non-symmetric real matrix cannot be diagonalized by an orthogonal transformation, but may be diagonalized by an unitary transformation)

If $\M{A}$ is real and non-symmetric, but can be diagonalized by an orthogonal transformation, then

$$
\begin{aligned}
\M{A}=\M{S}\M{A'}\M{S}^{-1}
\end{aligned}
$$

$\M{S}$ is orthogonal, and $\M{A'}$ is diagonal. Then

$$
\begin{aligned}
\M{A}^T=(\M{S}^{-1})^T(\M{A'})^T\M{S}^T=\M{S}\M{A'}\M{S}^{-1}=\M{A}
\end{aligned}
$$

so $A$ is symmetric, contradict.

To show a non-symmetric real matrix may be diagonalized by an unitary transformation, we give a counterexample:

$$
\begin{aligned}
\M{A}=
\begin{pmatrix}
1&1\\
-1&1
\end{pmatrix}\qquad \M{U}=\frac{1}{\sqrt{2}}
\begin{pmatrix}
1&-i\\
1&i
\end{pmatrix}
\end{aligned}
$$

it can be checked that $\M{U}$ is unitary:

$$
\begin{aligned}
\M{U}\M{U}^\dagger=
\frac{1}{\sqrt{2}}\frac{1}{\sqrt{2}}
\begin{pmatrix}
1&-i\\1&i
\end{pmatrix}
\begin{pmatrix}
1&1\\
i&-i
\end{pmatrix}=
\begin{pmatrix}
1&0\\0&1
\end{pmatrix}=\M{I}
\end{aligned}
$$

and

$$
\begin{aligned}
\M{U}\M{A}\M{U}^{-1}=
\frac{1}{\sqrt{2}}\frac{1}{\sqrt{2}}
\begin{pmatrix}
1&-i\\1&i
\end{pmatrix}
\begin{pmatrix}
1&1\\
-1&1
\end{pmatrix}
\begin{pmatrix}
1&1\\
i&-i
\end{pmatrix}=
\begin{pmatrix}
1+i&0\\
0&1-i
\end{pmatrix}
\end{aligned}
$$

so an non-symmetric real matrix may be diagonalized by an unitary transformation.

-----

### 6.4.4

$L_x,L_y,L_z$ are Hermitain, so

$$
\begin{aligned}
(\V{L}^2)^\dagger=(L_x^2)^\dagger+(L_y^2)^\dagger+(L_z^2)^\dagger=L_x^2+L_y^2+L_z^2=\V{L}^2
\end{aligned}
$$

so $\V{L}^2$ is Hermitian, and therefore its eigenvalues are real.

Let $\V{x}$ be an eigenvector of $\V{L}^2$, so $\V{L}^2\V{x}=\n\V{x}$. Then

$$
\begin{aligned}
\br{\V{x}|\V{L}^2}{\V{x}}=\br{\V{x}|L_x^2}{\V{x}}+\br{\V{x}|L_y^2}{\V{x}}+\br{\V{x}|L_z^2}{\V{x}}=\br{L_x\V{x}}{L_x\V{x}}+\br{L_y\V{x}}{L_y\V{x}}+\br{L_z\V{x}}{L_z\V{x}}\geq0
\end{aligned}
$$

but also

$$
\begin{aligned}
\br{\V{x}|\V{L}^2}{\V{x}}=\n\br{\V{x}}{\V{x}}
\end{aligned}
$$

so $\n\br{\V{x}}{\V{x}}\geq0$, and therefore $\n\geq0$.

-----

### 6.4.5

$$
\begin{aligned}
\M{A}\V{x_i}&=\n_i\V{x_i}\\
\V{x_i}&=\M{A}^{-1}\M{A}\V{x_i}=\n_i\V{A}^{-1}\V{x_i}
\end{aligned}
$$

so

$$
\begin{aligned}
\M{A}^{-1}\V{x_i}=\frac{1}{\n_i}\V{x_i}
\end{aligned}
$$

-----

### 6.4.6

(a) By making $\n=0$ in $\det(\M{A}-\n\M{I})=(\n_1-\n)\cdots(\n_n-\n)$, we know that $\det(\M{A})$ equals to the product of its eigenvalues. So $\det(\M{A})=0$ means that at least one of its eigenvalue is zero, then let $\V{x}$ be the eigenvector corresponding to the eigenvalue, we have

$$
\begin{aligned}
\M{A}\V{x}=0\V{x}=0
\end{aligned}
$$

(
It is a circular reasoning because the existence of eigenvector corresponding to an eigenvalue depends on the fact that $\V{x}$ exists when

$$
\begin{aligned}
(\M{A}-\n\M{I})\V{x}=0
\end{aligned}
$$

and $\det(\M{A}-\n\M{I})=0$, while this is exactly what we want to prove in this problem. However, a formal proof probably requires knowledge of linear algebra such as rank, Gaussian elimination, etc, which are beyond the scope of the book and probably not intended by the author.
)

(b) If $\M{A}\vert\V{v}\rangle=0$, then $\vert\V{v}\rangle$ is an eigenvector of $\M{A}$ with zero eigenvalue. So

$$
\begin{aligned}
\det(\M{A})=\n_1\n_2\cdots\n_n=0
\end{aligned}
$$

and therefore $\M{A}$ is singular.

-----

### 6.4.7

Transform $\M{A}$ and $\M{B}$ into their orthonormal eigenvector basis (which is unitary because $\M{A}$ and $\M{B}$ are Hermitian), we have

$$
\renewcommand{\arraystretch}{1.0}
\begin{aligned}
\M{U}_1\M{A}\M{U}_1^{-1}=
\begin{pmatrix}
\n_1&&\\
 &\ddots& \\
  & &\n_n
\end{pmatrix}=
\M{U}_2\M{B}\M{U}_2^{-1}
\end{aligned}
$$

so

$$
\begin{aligned}
\M{A}=\M{U}_1^{-1}\M{U}_2\M{B}\M{U}_2^{-1}\M{U}_1
=(\M{U}_1^{-1}\M{U}_2)\M{B}(\M{U}_1^{-1}\M{U}_2)^{-1}=\M{U}\M{B}\M{U}^{-1}
\end{aligned}
$$

-----

### 6.4.8

$$
\renewcommand{\arraystretch}{1.5}
\begin{aligned}
\M{M}_x:\quad
\begin{vmatrix}
 -\n&\frac{1}{\sqrt{2}} &0 \\
 \frac{1}{\sqrt{2}} & -\n&\frac{1}{\sqrt{2}} \\
 0 &\frac{1}{\sqrt{2}} &-\n
\end{vmatrix}=
-\n(\n-1)(\n+1)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1=-1 ,\qquad && x_1+\frac{1}{\sqrt{2}}x_2=0,\qquad && \frac{1}{\sqrt{2}}x_2+x_3=0,\qquad && \V{c}_1=\frac{1}{2}(1,-\sqrt{2},1) \\
    & \n_2=0 ,\qquad && x_2=0,\qquad && \frac{1}{\sqrt{2}}x_1+\frac{1}{\sqrt{2}}x_3=0,\qquad && \V{c}_2=\frac{1}{\sqrt{2}}(1,0,-1)\\
    & \n_3=1 ,\qquad && -x_1+\frac{1}{\sqrt{2}}x_2=0,\qquad && \frac{1}{\sqrt{2}}x_2-x_3=0,\qquad && \V{c}_3=\frac{1}{2}(1,\sqrt{2},1) \\
\end{aligned}
$$

$$
\begin{aligned}
\M{M}_y:\quad
\begin{vmatrix}
 -\n&\frac{-i}{\sqrt{2}} &0 \\
 \frac{i}{\sqrt{2}} & -\n&\frac{-i}{\sqrt{2}} \\
 0 &\frac{i}{\sqrt{2}} &-\n
\end{vmatrix}=
-\n(\n-1)(\n+1)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1=-1 ,\qquad && x_1-\frac{i}{\sqrt{2}}x_2=0,\qquad && \frac{i}{\sqrt{2}}x_2+x_3=0,\qquad && \V{c}_1=\frac{1}{2}(1,-\sqrt{2}i,-1) \\
    & \n_2=0 ,\qquad && \frac{-i}{\sqrt{2}}x_2=0,\qquad && \frac{i}{\sqrt{2}}x_1-\frac{i}{\sqrt{2}}x_3=0,\qquad && \V{c}_2=\frac{1}{\sqrt{2}}(1,0,1)\\
    & \n_3=1 ,\qquad && -x_1-\frac{i}{\sqrt{2}}x_2=0,\qquad && \frac{i}{\sqrt{2}}x_2-x_3=0,\qquad && \V{c}_3=\frac{1}{2}(1,\sqrt{2}i,-1) \\
\end{aligned}
$$

$$
\begin{aligned}
\M{M}_z:\quad
\begin{vmatrix}
 1-\n&0 &0 \\
 0 & -\n&0 \\
 0 &0 &-1-\n
\end{vmatrix}=
\n(1-\n)(1+\n)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1=-1 ,\qquad && 2x_1=0,\qquad && x_2=0,\qquad && \V{c}_1=(0,0,1) \\
    & \n_2=0 ,\qquad && x_1=0,\qquad && -x_3=0,\qquad && \V{c}_2=(0,1,0)\\
    & \n_3=1 ,\qquad && -x_2=0,\qquad && -2x_3=0,\qquad && \V{c}_3=(1,0,0) \\
\end{aligned}
$$

-----

### 6.4.9

(a)

$$
\begin{aligned}
a'_{ij}&=\br{\varphi'_i|\M{A}}{\varphi'_j}=\br{\varphi_i\cos\theta-\varphi_j\sin\theta|\M{A}}{\varphi_i\sin\theta+\varphi_j\cos\theta}\\
&=\br{\varphi_i|\M{A}}{\varphi_i}\sin\theta\cos\theta+\br{\varphi_i|\M{A}}{\varphi_j}\cos^2\theta-\br{\varphi_j|\M{A}}{\varphi_i}\sin^2\theta-\br{\varphi_j|\M{A}}{\varphi_j}\sin\theta\cos\theta\\
&=a_{ii}\sin\theta\cos\theta+a_{ij}\cos^2\theta-a_{ji}\sin^2\theta-a_{jj}\sin\theta\cos\theta\\
&=a_{ij}\cos2\theta-(a_{jj}-a_{ii})\frac{1}{2}\sin2\theta=0
\end{aligned}
$$

when $\frac{2a_{ij}}{a_{jj}-a_{ii}}=\frac{\sin2\theta}{\cos2\theta}=\tan2\theta$

(b)

$$
\begin{aligned}
a'_{\mu\nu}=\br{\varphi'_\mu|\M{A}}{\varphi'_\nu}=\br{\varphi_\mu|\M{A}}{\varphi_\nu}=a_{\mu\nu}
\end{aligned}
$$

(c)

$$
\begin{aligned}
a'_{ii}&=\br{\varphi'_i|\M{A}}{\varphi'_i}=\br{\varphi_i\cos\theta-\varphi_j\sin\theta|\M{A}}{\varphi_i\cos\theta-\varphi_j\sin\theta}\\
&=\br{\varphi_i|\M{A}}{\varphi_i}\cos^2\theta-\br{\varphi_i|\M{A}}{\varphi_j}\sin\theta\cos\theta-\br{\varphi_j|\M{A}}{\varphi_i}\sin\theta\cos\theta+\br{\varphi_j|\M{A}}{\varphi_j}\sin^2\theta\\
&=a_{ii}\cos^2\theta+a_{jj}\sin^2\theta-2a_{ij}\sin\theta\cos\theta\\
a'_{jj}&=\br{\varphi'_j|\M{A}}{\varphi'_j}=\br{\varphi_i\sin\theta+\varphi_j\cos\theta|\M{A}}{\varphi_i\sin\theta+\varphi_j\cos\theta}\\
&=\br{\varphi_i|\M{A}}{\varphi_i}\sin^2\theta+\br{\varphi_i|\M{A}}{\varphi_j}\sin\theta\cos\theta+\br{\varphi_j|\M{A}}{\varphi_i}\sin\theta\cos\theta+\br{\varphi_j|\M{A}}{\varphi_j}\cos^2\theta\\
&=a_{ii}\sin^2\theta+a_{jj}\cos^2\theta+2a_{ij}\sin\theta\cos\theta\\
\tr(\M{A'})-\tr(\M{A})&=a'_{ii}+a'_{jj}-a_{ii}-a_{jj}=0
\end{aligned}
$$

(d)

$$
\begin{aligned}
a'_{i\mu}&=\br{\varphi'_i|\M{A}}{\varphi'_\mu}=\br{\varphi_i\cos\theta-\varphi_j\sin\theta|\M{A}}{\varphi_\mu}=a_{i\mu}\cos\theta-a_{j\mu}\sin\theta\\
a'_{j\mu}&=\br{\varphi'_j|\M{A}}{\varphi'_\mu}=\br{\varphi_i\sin\theta+\varphi_j\cos\theta|\M{A}}{\varphi_\mu}=a_{i\mu}\sin\theta+a_{j\mu}\cos\theta
\end{aligned}
$$

Note that $a_{i\mu}'^2+a_{j\mu}'^2-a_{i\mu}^2-a_{j\mu}^2=0$. Let $S$ be the sum of the squares
of the off-diagonal elements of $\M{A}$, and let $\mu,\nu\neq i,j$, \,$\mu\neq\nu$, then

$$
\begin{aligned}
S'-S&=\sum_\mu\sum_\nu(a_{\mu\nu}'^2-a_{\mu\nu}^2)+\sum_\mu(a_{i\mu}'^2+a_{j\mu}'^2-a_{i\mu}^2-a_{j\mu}^2)-\sum_\mu(a_{\mu i}'^2+a_{\mu j}'^2-a_{\mu i}^2-a_{\mu j}^2)\,+(a_{ij}'^2+a_{ji}'^2-a_{ij}^2-a_{ji}^2)\\
&=-2a_{ij}^2
\end{aligned}
$$

because the first three summations are zero.

## 6.5 Normal Matrices

### 6.5.1

$$
\begin{aligned}
\begin{vmatrix}
 2-\n&4 \\
 1 & 2-\n 
\end{vmatrix}=
\n(\n-4)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1=0 ,\qquad && x_1+2x_2=0,\qquad && \V{c}_1=\frac{1}{\sqrt{5}}(2,-1) \\
    & \n_2=4 ,\qquad && x_1-2x_2=0,\qquad && \V{c}_2=\frac{1}{\sqrt{5}}(2,1)\\
\end{aligned}
$$

-----

### 6.5.2

Let 

$$
\begin{aligned}
\renewcommand{\arraystretch}{1.0}
\M{A}=\begin{pmatrix}
a&b\\c&d
\end{pmatrix}
\end{aligned}
$$

then its eigenvalue $\n$ satisfies

$$
\begin{aligned}
\begin{vmatrix}
a-\n&b\\c&d-\n
\end{vmatrix}=\n^2-\n(a+d)+(ad-bc)=\n^2-\n\,\mathrm{trace}(\M{A})+\det(\M{A})=0
\end{aligned}
$$

-----

### 6.5.3

$$
\begin{aligned}
\M{U}\V{c}&=\n\V{c}\\
\V{c}^\dagger\M{U}^\dagger&=\n^*\V{c}^\dagger\\
(\n^*\V{c}^\dagger)(\n\V{c})&=|\n|^2\V{c}^\dagger\V{c}=\V{c}^\dagger\M{U}^\dagger\M{U}\V{c}=\V{c}^\dagger\V{c}
\end{aligned}
$$

so 

$$
\begin{aligned}
|\n|^2=1
\end{aligned}
$$

-----

### 6.5.4

(The results hold only when the orthogonal matrix is a rotation, not a reflection, which means the determinant is $1$, not $-1$.)

(a)
Transform the matrix to the coordinate system where the axis of rotation coincides with the new $x$-axis, then it becomes

$$
\begin{aligned}
\begin{pmatrix}
1&0&0\\
0&\cos\varphi&\sin\varphi\\
0&-\sin\varphi&\cos\varphi
\end{pmatrix}
\end{aligned}
$$

By exercise 6.4.1, the trace (sum of eigenvalues) of a matrix is invariant under a similarity transformation, so the sum of the three eigenvalues of the original matrix equals the trace of the new matrix, which is 

$$
\begin{aligned}
1+2\cos\varphi
\end{aligned}
$$

(b) By exercise 6.4.1, the determinant (product of eigenvalues) of a matrix is invariant under a similarity transformation, so the product of the three eigenvalues of the original matrix equals the determinant of the new matrix, which is $\cos^2\varphi+\sin^2\varphi=1$. Let the other two eigenvalues be $a$ and $b$, then 

$$
\begin{aligned}
a+b=2\cos\varphi,\qquad ab=1
\end{aligned}
$$

so

$$
\begin{aligned}
a+\frac{1}{a}=2\cos\varphi
\end{aligned}
$$

solving for $a$, we have 

$$
\begin{aligned}
a=\frac{2\cos\varphi\pm\sqrt{4\cos^\varphi-4}}{2}=\cos\varphi\pm i\sin\varphi=e^{i\varphi}, e^{-i\varphi}
\end{aligned}
$$

So one of $a,b$ must be $e^{i\varphi}$, and the other must be $e^{-i\varphi}$.

-----

### 6.5.5

Expand $\V{y}$ in the orthonormal basis of $\V{x}_i$, we have

$$
\begin{aligned}
\br{\V{y}|\M{A}}{\V{y}}&=\sum_i\sum_j\br{\V{y}}{\V{x}_j}\br{\V{x}_i|\M{A}}{\V{x}_j}\br{\V{x}_j}{\V{y}}\\
&=\sum_i\sum_j\br{\V{y}}{\V{x}_j}\delta_{ij}\n_i\br{\V{x}_j}{\V{y}}\\
&=\sum_i|y_i|^2\n_i
\end{aligned}
$$

Note that $\br{\V{y}}{\V{y}}=\sum_i\vert y_i\vert^2=1$, and $\vert y_i\vert^2\geq0$, so

$$
\begin{aligned}
\n_1=(\sum_i|y_i|^2)\n_1\leq\sum_i|y_i|^2\n_i\leq(\sum_i|y_i|^2)\n_n=\n_n
\end{aligned}
$$

so

$$
\begin{aligned}
\n_1\leq\br{\V{y}|\M{A}}{\V{y}}\leq\n_n
\end{aligned}
$$

-----

### 6.5.6

The eigenvalues of a Hermitian matrix is real, and the eigenvalues of a unitary matrix have unit magnitude (from exercise 6.5.3), so the eigenvalues can only be $\pm1$.

-----

### 6.5.7

To prove the statement, we only need the anti-commuting condition and the fact that the metrics are non-singular (because they are unitary). If $\gamma_i\gamma_j=-\gamma_j\gamma_i$, then 

$$
\begin{aligned}
\det(\gamma_i)\det(\gamma_j)=(-1)^n\det(\gamma_j)\det(\gamma_i)
\end{aligned}
$$

Because $\det(\gamma_i),\det(\gamma_i)\neq0$, so $(-1)^n=1$, which means $n$ is even.

To show that $2\times2$ matrices are inadequate to form a set of four anticommuting, Hermitian,
unitary matrices, let the matrix satisfying the conditions be 

$$
\begin{aligned}
\begin{pmatrix}
a&b\\c&d
\end{pmatrix}
\end{aligned}
$$

It is Hermitian, so $c=b^*$, and $a,d$ are real:

$$
\begin{aligned}
\begin{pmatrix}
a&b\\b^*&d
\end{pmatrix}
\end{aligned}
$$

It is unitary, so

$$
\begin{aligned}
\begin{pmatrix}
a&b\\b^*&d
\end{pmatrix}
\begin{pmatrix}
a&b\\b^*&d
\end{pmatrix}=\begin{pmatrix}
a^2+|b|^2&b(a+d)\\
b^*(a+d)&d^2+|b|^2
\end{pmatrix}=
\begin{pmatrix}
1&0\\0&1
\end{pmatrix}
\end{aligned}
$$

so $b=0$ or $a+d=0$. 

If $a+d=0$, then $a^2+\vert b\vert^2=1$, which means we can find $0\leq\theta\leq\frac{\pi}{2}$ such that $a^2=\cos^2\theta$, $\vert b\vert^2=\sin^2\theta$. So the matrix has the form

$$
\begin{aligned}
\pm
\begin{pmatrix}
\cos\theta&\sin\theta e^{i\varphi}\\
\sin\theta e^{-i\varphi}& -\cos\theta
\end{pmatrix}
\end{aligned}
$$

If $b=0$, then $a,d=\pm1$. If $a,d$ have same sign, then the matrix is $\pm\M{I}$, and it will contradict with the anti-commuting property because $\M{A}\M{I}+\M{I}\M{A}=0$ implies $\M{A}=0$. Therefore, it must be $a=1,d=-1$ or $a=-1,d=1$, which is of the form of above equation by making $\theta=0$. 

Now using the anti-commuting property,

$$
\begin{aligned}
&\begin{pmatrix}
\cos\theta_1&\sin\theta_1 e^{i\varphi_1}\\
\sin\theta_1 e^{-i\varphi_1}& -\cos\theta_1
\end{pmatrix}
\begin{pmatrix}
\cos\theta_2&\sin\theta_2 e^{i\varphi_2}\\
\sin\theta_2 e^{-i\varphi_2}& -\cos\theta_2
\end{pmatrix}+
\begin{pmatrix}
\cos\theta_2&\sin\theta_2 e^{i\varphi_2}\\
\sin\theta_2 e^{-i\varphi_2}& -\cos\theta_2
\end{pmatrix}
\begin{pmatrix}
\cos\theta_1&\sin\theta_1 e^{i\varphi_1}\\
\sin\theta_1 e^{-i\varphi_1}& -\cos\theta_1
\end{pmatrix}\\
=\begin{pmatrix}
2\cos\theta_1\cos\theta_2+2\sin\theta_1\sin\theta_2\cos(\varphi_1-\varphi_2)& 0\\
0& 2\cos\theta_1\cos\theta_2+2\sin\theta_1\sin\theta_2\cos(\varphi_1-\varphi_2)
\end{pmatrix}
\end{aligned}
$$

so

$$
\begin{aligned}
2\cos\theta_1\cos\theta_2+2\sin\theta_1\sin\theta_2\cos(\varphi_1-\varphi_2)=0
\end{aligned}
$$

Because both the terms are non-negative ($0\leq\theta\leq\frac{\pi}{2}$), we must have 

$$
\begin{aligned}
\cos\theta_1\cos\theta_2=0
\end{aligned}
$$

and 

$$
\begin{aligned}
\sin\theta_1\sin\theta_2\cos(\varphi_1-\varphi_2)=0
\end{aligned}
$$

From $\cos\theta_1\cos\theta_2=0$ we know at most one of the matrix can have non-zero $\cos\theta$, which means except this matrix, all the other matrices have $\theta=\frac{\pi}{2}$.

From $\sin\theta_1\sin\theta_2\cos(\varphi_1-\varphi_2)=0$, we know when $\theta_1,\theta_2=\frac{\pi}{2}$, we must have $\varphi_1-\varphi_2=\pm\frac{\pi}{2}$, which means there are at most two matrices with $\theta=\frac{\pi}{2}$.

In conclusion, we can have at most two matrices with $\theta=\frac{\pi}{2}$ and one matrix with $\theta\neq\frac{\pi}{2}$, so it is inadequate for $2\times2$ matrices to form four anticommuting, Hermitian,
unitary matrices.

(The three Pauli matrices are:

$$
\begin{aligned}
    & \theta=0 ,\qquad&& && \sigma_1=\begin{pmatrix}0&1\\1&0\end{pmatrix}\\
    & \theta=\frac{\pi}{2},\qquad&& \varphi=-\frac{\pi}{2},\qquad&&\sigma_2=\begin{pmatrix}0&-i\\i&0\end{pmatrix}\\
    & \theta=\frac{\pi}{2},\qquad && \varphi=0 ,\qquad&& \sigma_3=
\begin{pmatrix}
1&0\\0&-1
\end{pmatrix}\\
\end{aligned}
$$

which are anticommuting, Hermitian and
unitary.
)

-----

### 6.5.8

$$
\begin{aligned}
|\V{y}\rangle=\sum_n|\V{x}_n\rangle\br{\V{x}_n}{\V{y}}
\end{aligned}
$$

so

$$
\begin{aligned}
\M{A}|\V{y}\rangle&=\sum_n\M{A}|\V{x}_n\rangle\br{\V{x}_n}{\V{y}}=\sum_n\n_n|\V{x}_n\rangle\br{\V{x}_n}{\V{y}}=\left(\sum_n\n_n|\V{x_n}\rangle\langle\V{x}_n|\right)|\V{y}\rangle\\
\M{A}&=\sum_n\n_n|\V{x_n}\rangle\langle\V{x}_n|
\end{aligned}
$$

-----

### 6.5.9

$$
\begin{aligned}
\begin{pmatrix}
1&0\\0&1
\end{pmatrix}
\M{A}
\begin{pmatrix}
1&0\\0&1
\end{pmatrix}=
\begin{pmatrix}
1&0\\0&-1
\end{pmatrix}
\end{aligned}
$$

so

$$
\begin{aligned}
\M{A}=\begin{pmatrix}
1&0\\0&-1
\end{pmatrix}
\end{aligned}
$$

-----

### 6.5.10

$$
\begin{aligned}
\M{A}\ket{\V{u}_j}&=\n_j\ket{\V{u}_j}\\
\M{A}^\dagger\ket{\V{v}_i}&=\n_i\ket{\V{v}_i}
\end{aligned}
$$

so

$$
\begin{aligned}
\br{\V{v}_i|\M{A}}{\V{u}_j}=\n_j\br{\V{v}_i}{\V{u}_j}=\n_i^*\br{\V{v}_i}{\V{u}_j}
\end{aligned}
$$

if $\n_j\neq\n_i^*$, we must have $\br{\V{v}_i}{\V{u}_j}=0$.

-----

### 6.5.11

(a) 

$$
\begin{aligned}
(\tilde{\M{A}}\M{A})\ket{\V{f}_n}=\n_n\tilde{\M{A}}\ket{\V{g}_n}=\n_n^2\ket{\V{f}_n}
\end{aligned}
$$

(b)

$$
\begin{aligned}
(\M{A}\tilde{\M{A}})\ket{\V{g}_n}=\n_n\M{A}\ket{\V{f}_n}=\n_n^2\ket{\V{g}_n}
\end{aligned}
$$

(c)

$$
\begin{aligned}
(\tilde{\M{A}}\M{A})^\dagger&=\M{A}^\dagger(\tilde{\M{A}})^\dagger=\tilde{\M{A}}\M{A}\\
(\M{A}\tilde{\M{A}})^\dagger&=(\tilde{\M{A}})^\dagger\M{A}^\dagger=\M{A}\tilde{\M{A}}
\end{aligned}
$$

so $(\tilde{\M{A}}\M{A})$ and $(\M{A}\tilde{\M{A}})$ are Hermitian, which means their eigenvectors $\ket{\V{f}_n}$ and $\ket{\V{g}_n}$ form an orthogonal set, and their eigenvalue $\n_n^2$ is real.

-----

### 6.5.12

$$
\begin{aligned}
\ket{\V{y}}&=\sum_n\ket{\V{f}_n}\br{\V{f}_n}{\V{y}}\\
\M{A}\ket{\V{y}}&=\sum_n\M{A}\ket{\V{f}_n}\br{\V{f}_n}{\V{y}}=\sum_n\n_n\ket{\V{g}_n}\br{\V{f}_n}{\V{y}}=\left(\sum_n\n_n\ket{\V{g}_n}\bra{\V{f}_n} \right)\ket{\V{y}}
\end{aligned}
$$

so

$$
\begin{aligned}
\M{A}=\sum_n\n_n\ket{\V{g}_n}\bra{\V{f}_n}
\end{aligned}
$$

-----

### 6.5.13

(a)

$$
\begin{aligned}
\tilde{\M{A}}=\frac{1}{\sqrt{5}}
\begin{pmatrix}
2&1\\2&-4
\end{pmatrix}\qquad
\tilde{\M{A}}\M{A}=
\begin{pmatrix}
1&0\\0&4
\end{pmatrix}\qquad
\M{A}\tilde{\M{A}}=\frac{1}{5}
\begin{pmatrix}
8&-6\\-6&17
\end{pmatrix}
\end{aligned}
$$

(b)

$$
\begin{aligned}
\renewcommand{\arraystretch}{1.5}
\begin{vmatrix}
 \frac{8}{5}-\n_n^2&\frac{-6}{5} \\
 \frac{-6}{5} & \frac{17}{5}-\n_n^2 
\end{vmatrix}=
(\n_n^2-1)(\n_n^2-4)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1^2=1 ,\qquad && x_1-2x_2=0,\qquad && \V{g}_1=\frac{1}{\sqrt{5}}(2,1) \\
    & \n_2^2=4 ,\qquad && 2x_1+x_2=0,\qquad && \V{g}_2=\frac{1}{\sqrt{5}}(1,-2)\\
\end{aligned}
$$

(c)

$$
\begin{aligned}
\begin{vmatrix}
 1-\n_n^2&0 \\
0& 4-\n_n^2 
\end{vmatrix}=
(\n_n^2-1)(\n_n^2-4)=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1^2=1 ,\qquad && 3x_2=0,\qquad && \V{f}_1=(1,0) \\
    & \n_2^2=4 ,\qquad && -3x_1=0,\qquad && \V{f}_2=(0,1)\\
\end{aligned}
$$

(d) 
$\n_1^2=1$ ($\n_1=1$) :

$$
\begin{aligned}
&\frac{1}{\sqrt{5}}
\begin{pmatrix}
2&2\\1&-4
\end{pmatrix}
\begin{pmatrix}
1\\0
\end{pmatrix}=1\cdot\frac{1}{\sqrt{5}}
\begin{pmatrix}
2\\1
\end{pmatrix}\\
&\frac{1}{\sqrt{5}}
\begin{pmatrix}
2&1\\2&-4
\end{pmatrix}\frac{1}{\sqrt{5}}
\begin{pmatrix}
2\\1
\end{pmatrix}=1\cdot\begin{pmatrix}
1\\0
\end{pmatrix}
\end{aligned}
$$

$\n_2^2=4$ ($\n_2=2$) :

$$
\begin{aligned}
&\frac{1}{\sqrt{5}}
\begin{pmatrix}
2&2\\1&-4
\end{pmatrix}
\begin{pmatrix}
0\\1
\end{pmatrix}=2\cdot\frac{1}{\sqrt{5}}
\begin{pmatrix}
1\\-2
\end{pmatrix}\\
&\frac{1}{\sqrt{5}}
\begin{pmatrix}
2&1\\2&-4
\end{pmatrix}\frac{1}{\sqrt{5}}
\begin{pmatrix}
1\\-2
\end{pmatrix}=2\cdot\begin{pmatrix}
0\\1
\end{pmatrix}
\end{aligned}
$$

(e)

$$
\begin{aligned}
\sum_n\n_n\ket{\V{g}_n}\bra{\V{f}_n}=1\cdot
\begin{pmatrix}
\frac{2}{\sqrt{5}}\\\frac{1}{\sqrt{5}}
\end{pmatrix}
\begin{pmatrix}
1&0
\end{pmatrix}+2\cdot
\begin{pmatrix}
\frac{1}{\sqrt{5}}\\\frac{-2}{\sqrt{5}}
\end{pmatrix}
\begin{pmatrix}
0&1
\end{pmatrix}=
\frac{1}{\sqrt{5}}
\begin{pmatrix}
2&2\\1&-4
\end{pmatrix}=\M{A}
\end{aligned}
$$

-----

### 6.5.14

(a)

$$
\begin{aligned}
\M{A}=\sum_n\n_n\ket{\V{g}_n}\bra{\V{f}_n}=1\cdot
\begin{pmatrix}
\frac{1}{\sqrt{2}}\\\frac{1}{\sqrt{2}}
\end{pmatrix}
\begin{pmatrix}
1&0
\end{pmatrix}-1\cdot
\begin{pmatrix}
\frac{1}{\sqrt{2}}\\\frac{-1}{\sqrt{2}}
\end{pmatrix}
\begin{pmatrix}
0&1
\end{pmatrix}=
\begin{pmatrix}
\frac{1}{\sqrt{2}}&\frac{-1}{\sqrt{2}}\\
\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}
\end{pmatrix}=
\frac{1}{\sqrt{2}}
\begin{pmatrix}
1&-1\\1&1
\end{pmatrix}
\end{aligned}
$$

(b)

$$
\begin{aligned}
&\frac{1}{\sqrt{2}}\begin{pmatrix}
1&-1\\1&1
\end{pmatrix}
\begin{pmatrix}
1\\0
\end{pmatrix}=1\cdot\frac{1}{\sqrt{2}}
\begin{pmatrix}
1\\1
\end{pmatrix}\\
&\frac{1}{\sqrt{2}}\begin{pmatrix}
1&-1\\1&1
\end{pmatrix}
\begin{pmatrix}
0\\1
\end{pmatrix}=-1\cdot\frac{1}{\sqrt{2}}
\begin{pmatrix}
1\\-1
\end{pmatrix}
\end{aligned}
$$

(c)

$$
\begin{aligned}
&\frac{1}{\sqrt{2}}\begin{pmatrix}
1&1\\-1&1
\end{pmatrix}\frac{1}{\sqrt{2}}
\begin{pmatrix}
1\\1
\end{pmatrix}=1\cdot
\begin{pmatrix}
1\\0
\end{pmatrix}\\
&\frac{1}{\sqrt{2}}\begin{pmatrix}
1&1\\-1&1
\end{pmatrix}\frac{1}{\sqrt{2}}
\begin{pmatrix}
1\\-1
\end{pmatrix}=-1\cdot
\begin{pmatrix}
0\\1
\end{pmatrix}
\end{aligned}
$$

-----

### 6.5.15

(a)

$$
\begin{aligned}
\M{U}^\dagger=e^{-ia\M{H}^\dagger}=e^{-ia\M{H}}=\M{U}^{-1}
\end{aligned}
$$

so $\M{U}$ is unitary.

(b)

$$
\begin{aligned}
\M{U}^\dagger\M{U}=e^{-ia\M{H}^\dagger}e^{ia\M{H}}=e^{ia(\M{H-\M{H}^\dagger})}=\M{I}=e^{i2n\pi\M{I}}
\end{aligned}
$$

so $a(\M{H}-\M{H}^\dagger)=2n\pi\M{I}$. Because $\M{H}-\M{H}^\dagger$ is independent of $a$, so it must be $n=0$, and therefore $\M{H}-\M{H}^\dagger=0$, $\M{H}=\M{H}^\dagger$, which means $\M{H}$ is Hermitian.

(c) It can be verified that $u_j=e^{iah_j}$, with $u_j$ and $h_j$ being eigenvalues of $\M{U}$ and $\M{H}$. Transform into the eigenvector basis, and note that determinant and trace of a matrix is invariant under unitary transformation, we have

$$
\begin{aligned}
\det\M{U}=\prod_j u_j=\prod_j e^{iah_j}=e^{ia\sum_j h_j}=e^{ia\,\mathrm{trace}\M{H}}
\end{aligned}
$$

so when $\mathrm{trace}\,\M{H}=0$, $\det\M{U}=1$.

(d) When $\det\M{U}=1=e^{i2n\pi}$, $a\,\mathrm{trace}\,\M{H}=2n\pi$, and because $\M{H}$ is independent of $a$, it must be $n=
0$, so $\mathrm{trace}\,\M{H}=0$.

-----

### 6.5.16

$\M{B}$ is defined as 

$$
\begin{aligned}
\M{B}=\sum_{j=0}^\infty\frac{1}{j!}\M{A}^j
\end{aligned}
$$

If $\V{x}_i$ is an eigenvector of $\M{A}$, so $\M{A}\V{x}_i=A_i\V{x}_i$, then 

$$
\begin{aligned}
\M{B}\V{x}_i=\sum_{j=o}^\infty\frac{1}{j!}\M{A}^j
\V{x}_i=\sum_{j=0}^\infty\frac{1}{j!}(A_i)^j\V{x}_i=e^{A_i}\V{x}_i
\end{aligned}
$$

which means $\V{x}_i$ is also an eigenvector of $\M{B}$ with eigenvalue being $e^{A_i}$.

-----

### 6.5.17

Let $\V{x}$ be an eigenvector of $\M{P}$ so $\M{P}\V{x}=\rho_\lambda\V{x}$. Then

$$
\begin{aligned}
\M{P}^2\V{x}=\M{P}(\M{P}\V{x})=\M{P}(\rho_\lambda\V{x})=(\rho_\lambda)^2\V{x}
\end{aligned}
$$

But also

$$
\begin{aligned}
\M{P}^2\V{x}=\M{P}\V{x}=\rho_\lambda\V{x}
\end{aligned}
$$

so $(\rho_\lambda)^2=\rho_\lambda$, which means $\rho_\lambda=0,1$.

-----

### 6.5.18

$\br{\V{x}\_i\vert \M{A}}{\V{x}\_j}=\lambda_j\br{\V{x}\_i}{\V{x}\_j}=\lambda_j\delta_{ij}$. So

$$
\begin{aligned}
\br{\V{x}|\M{A}}{\V{x}}&=\left( \bra{\V{x}_1}+\sum_{i=2}^n\delta_i\bra{\V{x}_i} \right)\M{A}\left( \ket{\V{x}_1}+\sum_{j=2}^n\delta_j\ket{\V{x}_i} \right)\\
&=\br{\V{x}_1|\M{A}}{\V{x}_1}+\sum_{j=2}^n\delta_j\br{\V{x}_1|\M{A}}{\V{x}_j}+\sum_{i=2}^n\delta_i^*\br{\V{x}_i|\M{A}}{\V{x}_1}+\sum_{i=2}^n\sum_{j=2}^n\delta_i^*\delta_j\br{\V{x}_i|\M{A}}{\V{x}_j}\\
&=\lambda_1\br{\V{x}_1}{\V{x}_1}+\sum_{i=2}^n|\delta_i|^2\lambda_i\br{\V{x}_i}{\V{x}_i}
\end{aligned}
$$

and

$$
\begin{aligned}
\br{\V{x}}{\V{x}}&=\left( \bra{\V{x}_1}+\sum_{i=2}^n\delta_i\bra{\V{x}_i} \right)\left( \ket{\V{x}_1}+\sum_{j=2}^n\delta_j\ket{\V{x}_i} \right)\\
&=\br{\V{x}_1}{\V{x}_1}+\sum_{j=2}^n\delta_j\br{\V{x}_1}{\V{x}_j}+\sum_{i=2}^n\delta_i^*\br{\V{x}_i}{\V{x}_1}+\sum_{i=2}^n\sum_{j=2}^n\delta_i^*\delta_j\br{\V{x}_i}{\V{x}_j}\\
&=\br{\V{x}_1}{\V{x}_1}+\sum_{i=2}^n|\delta_i|^2\br{\V{x}_i}{\V{x}_i}
\end{aligned}
$$

so

$$
\begin{aligned}
\frac{\br{\V{x}|\M{A}}{\V{x}}}{\br{\V{x}}{\V{x}}}=\frac{\lambda_1\br{\V{x}_1}{\V{x}_1}+\sum_{i=2}^n|\delta_i|^2\lambda_i\br{\V{x}_i}{\V{x}_i}}{\br{\V{x}_1}{\V{x}_1}+\sum_{i=2}^n|\delta_i|^2\br{\V{x}_i}{\V{x}_i}}\leq
\frac{\lambda_1\br{\V{x}_1}{\V{x}_1}+\sum_{i=2}^n|\delta_i|^2\lambda_1\br{\V{x}_i}{\V{x}_i}}{\br{\V{x}_1}{\V{x}_1}+\sum_{i=2}^n|\delta_i|^2\br{\V{x}_i}{\V{x}_i}}=\lambda_1
\end{aligned}
$$

and the error in $\lambda_1$ is 

$$
\begin{aligned}
\lambda_1-\frac{\br{\V{x}|\M{A}}{\V{x}}}{\br{\V{x}}{\V{x}}}=\frac{\sum_{i=2}^n|\delta_i|^2(\lambda_1-\lambda_i)\br{\V{x}_i}{\V{x}_i}}{\br{\V{x}_1}{\V{x}_1}+\sum_{i=2}^n|\delta_i|^2\br{\V{x}_i}{\V{x}_i}}\simeq
\frac{\sum_{i=2 }^n|\delta_i|^2(\lambda_1-\lambda_i)\br{\V{x}_i}{\V{x}_i}}{\br{\V{x}_1}{\V{x}_1}}
\end{aligned}
$$

so the error is of the order of $\vert\delta_i\vert^2$.

-----

### 6.5.19

(a)

$$
\begin{aligned}
    m\ddot{x_1}&=-kx_1+k(x_2-x_1)=-2kx_1+kx_2\\
    m\ddot{x_2}&=k(x_1-x_2)-kx_2=kx_1-2kx_2
\end{aligned}
$$

(b)
To find the normal mode, let $x_1(t)=x_1\sin\omega t$, $x_2(t)=x_2\sin\omega t$. Substitute and cancel
out $\sin\omega t$, we have

$$
\begin{aligned}
\begin{pmatrix}
\frac{2k}{m}&\frac{-k}{m}\\
\frac{-k}{m}&\frac{2k}{m}
\end{pmatrix}
\begin{pmatrix}
x_1\\x_2
\end{pmatrix}=\omega^2
\begin{pmatrix}
x_1\\x_2
\end{pmatrix}
\end{aligned}
$$

so the secular equation is 

$$
\begin{aligned}
\begin{vmatrix}
\frac{2k}{m}-\omega^2&\frac{-k}{m}\\
\frac{-k}{m}&\frac{2k}{m}-\omega^2
\end{vmatrix}=
(\omega^2-\frac{k}{m})(\omega^2-\frac{3k}{m})=0
\end{aligned}
$$

$$
\begin{aligned}
    & \omega^2=\frac{k}{m} ,\qquad && x_1-x_2=0,\qquad && \V{c}_1=\frac{1}{\sqrt{2}}(1,1) \\
    & \omega^2=\frac{3k}{m} ,\qquad && -x_1-x_2=0,\qquad && \V{c}_2=\frac{1}{\sqrt{2}}(1,-1) \\
\end{aligned}
$$

(c) For $\omega^2=\frac{k}{m}$, $x_1=x_2$, so the two masses vibrate in phase (move together). For $\omega^2=\frac{3k}{m}$, $x_1=-x_2$, so the two masses vibrate in anti-symmetry movement.

-----

### 6.5.20

Follow the proof in Section 6.5 (p.319), we know if $\M{A}\V{x}\_j=\lambda_j\V{x}\_j$, or $(\M{A}-\lambda_j\M{I})\ket{\V{x}\_j}=0$, then we have $(\M{A}^\dagger-\lambda_j^\star\M{I})\ket{\V{x}\_j}=0$, or $\M{A}^\dagger\V{x}\_j=\lambda_j^\star\V{x}\_j$, so $\ket{\V{x}\_j}$ is also an eigenvector of $\M{A}^\dagger$ with eigenvalue $\lambda_j^\star$.

$$
\begin{aligned}
\frac{\M{A}+\M{A}^\dagger}{2}\V{x}_j=\frac{\n_j+\n_j^*}{2}\V{x}_j=\mathfrak{Re}(\n_j)\,\V{x}_j
\end{aligned}
$$

so $\V{x}_j$ is an eigenvector of $\frac{\M{A}+\M{A}^\dagger}{2}$ with $\mathfrak{Re}(\n_j)$ as eigenvalue.

$$
\begin{aligned}
\frac{\M{A}-\M{A}^\dagger}{2i}\V{x}_j=\frac{\n_j-\n_j^*}{2i}\V{x}_j=\mathfrak{Im}(\n_j)\,\V{x}_j
\end{aligned}
$$


so $\V{x}_j$ is an eigenvector of $\frac{\M{A}-\M{A}^\dagger}{2i}$ with $\mathfrak{Im}(\n_j)$ as eigenvalue.

-----

### 6.5.21

(a) Substituting into Eq. 3.37, we have

$$
\begin{aligned}
\M{U}=
\begin{pmatrix}
\frac{1}{2}&\frac{-1}{2}&\frac{1}{\sqrt{2}}\\
\frac{1}{2}&\frac{-1}{2}&\frac{-1}{\sqrt{2}}\\
\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}&0
\end{pmatrix}
\end{aligned}
$$

(b)

$$
\begin{aligned}
\begin{vmatrix}
\frac{1}{2}-\n&\frac{-1}{2}&\frac{1}{\sqrt{2}}\\
\frac{1}{2}&\frac{-1}{2}-\n&\frac{-1}{\sqrt{2}}\\
\frac{1}{\sqrt{2}}&\frac{1}{\sqrt{2}}&-\n
\end{vmatrix}=-(\n-1)(\n-\frac{-1+\sqrt{3}i}{2})(\n-\frac{-1-\sqrt{3}i}{2})=0
\end{aligned}
$$

$$
\begin{aligned}
    & \n_1=1,\qquad && -x_1-x_2+\sqrt{2}x_3=0,\qquad && x_1-3x_2-\sqrt{2}x_3=0,\qquad && \V{c}_1=\frac{1}{\sqrt{3}}(\sqrt{2},0,1)\\
    & \n_2=\frac{-1+\sqrt{3}i}{2},\qquad && (2-\sqrt{3}i)x_1-x_2+\sqrt{2}x_3=0,\qquad && x_1-\sqrt{3}ix_2-\sqrt{2}x_3=0,\qquad && \V{c}_2=\frac{1}{\sqrt{6}}(1,-\sqrt{3}i,-\sqrt{2})\\
    & \n_3=\frac{-1-\sqrt{3}i}{2},\qquad && (2+\sqrt{3}i)x_1-x_2+\sqrt{2}x_3=0,\qquad && x_1+\sqrt{3}ix_2-\sqrt{2}x_3=0,\qquad && \V{c}_3=\frac{1}{\sqrt{6}}(1,\sqrt{3}i,-\sqrt{2})\\
\end{aligned}
$$


The eigenvector with $\n=1$ is in the direction of rotation axis, which is $\V{c}_1=\frac{1}{\sqrt{3}}(\sqrt{2},0,1)$.
From Exercise 6.5.4, we know the other two eigenvalues of a rotation are $e^{i\varphi}$ and $e^{-i\varphi}$. Compared with $\n_2=e^{i\frac{2\pi}{3}}$, $\n_3=e^{-i\frac{2\pi}{3}}$, we know the rotation angle is $\frac{2\pi}{3}$.

{% endraw %}
