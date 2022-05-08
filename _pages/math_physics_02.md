---
layout: splash
title: "Mathematical Methods for Physicists Ch2"
permalink: /solutions/math_physics_02
author_profile: false

---

# Chapter 1: Determinants and Matrices

## 2.1 Determinants

### 2.1.1

(a) $1\times(-1\times1)=-1$

(b) $1\times(1\times1-2\times3)-2\times(3\times1-2\times0)=-11$

(c) $\frac{1}{\sqrt{2}}(-\sqrt{3})\times\sqrt{3}\times(-\sqrt{3}\times\sqrt{3})=\frac{9}{\sqrt{2}}$

-----

### 2.1.2

$$
\begin{vmatrix}
1&3&3\\
1&-1&1\\
2&1&3
\end{vmatrix}
=2
$$
, so the homogeneous linear independent equations have no nontrivial solutions.

-----

### 2.1.3

(a)
$$
\begin{vmatrix}
1&2\\
2&4
\end{vmatrix}
=0
$$

(b)
$$
\begin{vmatrix}
3&2\\
6&4
\end{vmatrix}
=0
$$

(c) $(1,1)$, $(2,2)$

-----

### 2.1.4

(a)
$|A|=\sum_{ij\cdots}\varepsilon_{ij\cdots}a_{1i}a_{2j}\cdots$, which is the sum of all products formed by choosing one entry in each row that they are all in different columns (call it a valid combination), multiplying them together, and multiplying $+1$ or $-1$ depending on the parity of permutation $c_1c_2\cdots$, where $c_i$ is the column of the entry chosen in row i. $a_{ji}C_{ji}=a_{ji}M_{ji}(-1)^{j+i}$, is the sum of all products of valid combinations in $M_{ji}$, multiplying $a_{j+i}$, multiplying $(-1)^{j+i}$. If it takes n steps for a permutation in $M_{ji}$ to return to reference order, then it will take $n+|j-i|$ steps for the permutation appended $a_{ji}$ to return to reference order, so $a_{ij}M_{ij}(-1)^{|j-i|}=a_{ij}M_{ij}(-1)^{j+i}$ will contribute to the sum of products of valid combinations in A that contains $a_{ji}$, so $\sum_{i}a_{ji}C_{ji}$ contains all products of valid combinations, and is therefore equal to $|A|$.

Example:

$$
\begin{vmatrix}
 &o& & \\
 o& & & \\
 & & &o\\
 & &o&
\end{vmatrix}
\xrightarrow{2\,steps}
\begin{vmatrix}
 o&& & \\
 &o& & \\
 & &o&\\
 & &&o
\end{vmatrix}
$$

$$
\begin{vmatrix}
 &o&&&\\
 &&&a_{24}&\\
 o&&&&\\
 &&&&o\\
 &&o&&
\end{vmatrix}
\xrightarrow{2\,steps}
\begin{vmatrix}
 o&&&&\\
 &&&a_{24}&\\
 &o&&&\\
 &&o&&\\
 &&&&o
\end{vmatrix}
\xrightarrow{|4-2|\,steps}
\begin{vmatrix}
 o&&&&\\
 &a_{24}&&&\\
 &&o&&\\
 &&&o&\\
 &&&&o
\end{vmatrix}
$$

(b) If $A'$ is the matrix whose $k^{th}$ column is the $j^{th}$ column of $A$ and all the other columns is the same with $A$,  then $\sum_ia_{ij}C_{ik}=\sum_{i}a'\_{ik}C'\_{ik}$ is the determinant of $A'$, but $A'$ has two equal rows ($j^{th}$ and $k^{th}$ rows), so it equals to zero.

-----

### 2.1.5

(a) $\det(H_1)=1$, $\det(H_2)=8.3333\times10^{-2}$, $\det(H_3)=4.62963\times10^{-4}$

(b)
For $\det(H_4)$: 

Subtract the last row from each row above it:

$$
\renewcommand{\arraystretch}{1.5}
\begin{vmatrix}
\frac{1}{1}&\frac{1}{2}&\frac{1}{3}&\frac{1}{4}\\
\frac{1}{2}&\frac{1}{3}&\frac{1}{4}&\frac{1}{5}\\ 
\frac{1}{3}&\frac{1}{4}&\frac{1}{5}&\frac{1}{6}\\
\frac{1}{4}&\frac{1}{5}&\frac{1}{6}&\frac{1}{7}\\
\end{vmatrix}
=
\begin{vmatrix}
\frac{3}{(1)(4)}&\frac{3}{(2)(5)}&\frac{3}{(3)(6)}&\frac{3}{(4)(7)}\\
\frac{2}{(2)(4)}&\frac{2}{(3)(5)}&\frac{2}{(4)(6)}&\frac{2}{(5)(7)}\\ 
\frac{1}{(3)(4)}&\frac{1}{(4)(5)}&\frac{1}{(5)(6)}&\frac{1}{(6)(7)}\\
\frac{1}{4}&\frac{1}{5}&\frac{1}{6}&\frac{1}{7}\\
\end{vmatrix}
=
\frac{(1)(2)(3)}{(4)(5)(6)(7)}
\begin{vmatrix}
\frac{1}{1}&\frac{1}{2}&\frac{1}{3}&\frac{1}{4}\\
\frac{1}{2}&\frac{1}{3}&\frac{1}{4}&\frac{1}{5}\\ 
\frac{1}{3}&\frac{1}{4}&\frac{1}{5}&\frac{1}{6}\\
1&1&1&1\\
\end{vmatrix}
=
\frac{(3!)^2}{7!}
\begin{vmatrix}
\frac{1}{1}&\frac{1}{2}&\frac{1}{3}&\frac{1}{4}\\
\frac{1}{2}&\frac{1}{3}&\frac{1}{4}&\frac{1}{5}\\ 
\frac{1}{3}&\frac{1}{4}&\frac{1}{5}&\frac{1}{6}\\
1&1&1&1\\
\end{vmatrix}
$$

Subtract the last column from each column precedes it:

$$
\frac{(3!)^2}{7!}
\begin{vmatrix}
\frac{1}{1}&\frac{1}{2}&\frac{1}{3}&\frac{1}{4}\\
\frac{1}{2}&\frac{1}{3}&\frac{1}{4}&\frac{1}{5}\\ 
\frac{1}{3}&\frac{1}{4}&\frac{1}{5}&\frac{1}{6}\\
1&1&1&1\\
\end{vmatrix}
=
\frac{(3!)^2}{7!}
\begin{vmatrix}
\frac{3}{(1)(4)}&\frac{2}{(2)(4)}&\frac{1}{(3)(4)}&\frac{1}{4}\\
\frac{3}{(2)(5)}&\frac{2}{(3)(5)}&\frac{1}{(4)(5)}&\frac{1}{5}\\ 
\frac{3}{(3)(6)}&\frac{2}{(4)(6)}&\frac{1}{(5)(6)}&\frac{1}{6}\\
0&0&0&1\\
\end{vmatrix}
=
\frac{(3!)^2}{7!}\frac{(3!)^2}{6!}
\begin{vmatrix}
\frac{1}{1}&\frac{1}{2}&\frac{1}{3}&\frac{1}{4}\\
\frac{1}{2}&\frac{1}{3}&\frac{1}{4}&\frac{1}{5}\\ 
\frac{1}{3}&\frac{1}{4}&\frac{1}{5}&\frac{1}{6}\\
0&0&0&1\\
\end{vmatrix}
=
\frac{(3!)^4}{(7!)(6!)}\det(H_3)
$$

By this procedure, we found that

$$
\det(H_n)=\frac{(n-1)!^4}{(2n-1)!(2n-1)!}\det(H_{n-1})
$$

So $\det(H_4)=\frac{3!^4}{7!6!}\det(H_3)=1.65344\times10^{-7}$, $\det(H_5)=\frac{4!^4}{9!8!}\det(H_4)=3.74930\times10^{-12}$, $\det(H_6)=\frac{5!^4}{11!10!}=5.36730\times10^{-18}$

-----

### 2.1.6

Linear dependence implies one row (or column) can be expressed by linear combination of other rows (columns), so $A_{ni}=a_1A_{1i}+a_2A_{2i}+\cdots$. Add $-a_j$ times the $j^{th}$ row to the $n^{th}$  row, then the determinant remains the same, but all entries in the $n^{th}$ row becomes $0$, so the determinant equals to zero.

-----

### 2.1.7

By Gauss's elimination, $x_1=1.88282$, $x_2=-0.36179$, $-0.96889$, $0.44221$, $0.41022$, $0.39219$

-----

### 2.1.8

(a) $\sum_{i}\delta_{ii}=\delta_{11}+\delta_{22}+\delta_{33}=3$

(b) $\sum_{ij}\delta_{ij}\varepsilon_{ijk}=\sum_{i}\delta_{ii}\varepsilon_{iik}=0$

(c) If $i\neq j$, then at least two of $1,j,p,q$ is the same, and $\varepsilon_{ipq}\varepsilon_{jpq}=0$. If  $i=j=1$, then 
$\sum_{pq}\varepsilon_{ipq}\varepsilon_{jpq}=\varepsilon_{123}\varepsilon_{123}+\varepsilon_{132}\varepsilon_{132}=2$, and the case is similar when $i=j=2$ and $i=j=3$. Therefore, $\sum_{pq}\varepsilon_{ipq}\varepsilon_{jpq}=2\delta_{ij}$ 

(d) $\sum_{ijk}\varepsilon_{ijk}\varepsilon_{ijk}=(-1)^2\times6=6$

-----

### 2.1.9

The only case that $\varepsilon_{ijk}\varepsilon_{pqk}\neq0$ is : k is one of $(1,2,3)$ and $(i,j),(p,q)$ are the other two of $(1,2,3)$, respectively. So $i=p,j=q$ or $i=q,j=p$. For the former case, $\varepsilon_{ijk}\varepsilon_{pqk}=(\pm1)^2=1=\delta_{ip}\delta_{jq}$, and for the latter case, $\varepsilon_{ijk}\varepsilon_{pqk}=(1)(-1)=-1=-\delta_{iq}\delta_{jp}$. Therefore, $\sum_{k}\varepsilon_{ijk}\varepsilon_{pqk}=\delta_{ip}\delta_{jq}-\delta_{iq}\delta_{jp}$

## 2.2 Matrices

-----

### 2.2.1

$$
((AB)C)_{il}=\sum_m(AB)_{im}C_{ml}=\sum_m\sum_k A_{ik}B_{km}C_{ml}=\sum_k\sum_m A_{ik}B_{km}C_{ml}=\sum_k A_{ik}(BC)_{kl}=(A(BC))_{il}
$$

-----

### 2.2.2

If $(A+B)(A-B)=A^2-B^2$, than $A^2+BA-AB-B^2=A^2-B^2$, so $AB-BA=[A,B]=0$. If $[A,B]=0$, then $(A+B)(A-B)=A^2-B^2-(AB-BA)=A^2-B^2$

-----

### 2.2.3

(a)

$$
\renewcommand{\arraystretch}{1}
(a+ib)+(c+id)\longleftrightarrow
\begin{pmatrix}
a&b\\-b&a
\end{pmatrix}+
\begin{pmatrix}
c&d\\-d&c
\end{pmatrix}=
\begin{pmatrix}
a+c&b+d\\-(b+d)&a+c
\end{pmatrix}\longleftrightarrow
(a+c)+i(b+d)
$$

$$
(a+ib)(c+id)\longleftrightarrow
\begin{pmatrix}
a&b\\-b&a
\end{pmatrix}
\begin{pmatrix}
c&d\\-d&c
\end{pmatrix}=
\begin{pmatrix}
ac-bd&ad+bc\\-(ad+bc)&ac-bd
\end{pmatrix}\longleftrightarrow
(ac-bd)+i(ad+bc)
$$

(b)

$$
(a+ib)^{-1}=\frac{1}{a^2+b^2}(a-ib)\longleftrightarrow\frac{1}{a^2+b^2}
\begin{pmatrix}
a&-b\\b&a
\end{pmatrix}
$$

-----

### 2.2.4

Multiply each row of $A$ by $-1$ will turn $A$ into $-A$, so $\det(-A)=(-1)^n\det(A)$.

-----

### 2.2.5

(a) If $A^2=0$ and $$A=\begin{pmatrix}
x&y\\z&t
\end{pmatrix}$$

$$
A^2=
\begin{pmatrix}
x&y\\z&t
\end{pmatrix}
\begin{pmatrix}
x&y\\z&t
\end{pmatrix}=0
$$

Then $x^2+yz=0$, $t^2+yz=0$, $y(x+t)=0$, $z(x+t)=0$. Let $y=b^2$, $z=-a^2$, then $x=\pm ab$, $t=\pm ab$. Without less of generality let $x=ab$ because the sign of $a$ and $b$ is arbitrary. If $y\neq0$, then $t=-x=-ab$; if $y=0$, then $t=x=ab=0$ so $t=-ab$. Therefore, in all cases we can find $a,b$ such that $$\begin{pmatrix}
x&y\\z&t
\end{pmatrix}=\begin{pmatrix}
ab&b^2\\-a^2&-ab
\end{pmatrix}$$

(b)
Let $$A=\begin{pmatrix}
1&0\\0&1
\end{pmatrix}$$, $$B=\begin{pmatrix}
-1&0\\0&-1
\end{pmatrix}$$, then $$\det{C}=\det\begin{pmatrix}
0&0\\0&0
\end{pmatrix}=0$$ but $\det{A}+\det{B}=1+1=2$

-----

### 2.2.6

$$K=
\begin{pmatrix}
0&0&i\\
-i&0&0\\
0&-1&0
\end{pmatrix}
$$, 
$$K^2=
\begin{pmatrix}
0&-i&0\\
0&0&1\\
i&0&0
\end{pmatrix}
$$, 
$$K^3=
\begin{pmatrix}
-1&0&0\\
0&-1&0\\
0&0&-1
\end{pmatrix}=-I
$$, 
$K^4=-K$, $K^5=-K^2$, $K^6=I$. So if $n=6k$, k is positive integer, then $K^n=I$

\paragraph{2.2.7}
\[[A,[B,C]]=[A,BC-CB]=(ABC-ACB)-(BCA-CBA)=ABC-ACB-BCA+CBA\]
\[[B,[A,C]]-[C,[B,A]]=[B,AC-CA]-[C,AB-BA]\]
\[=(BAC-BCA)-(ACB-CAB)-[(CAB-CBA)-(ABC-BAC)]=ABC-ACB-BCA+CBA\]
So $[A,[B,C]]=[B,[A,C]]-[C,[B,A]]$

\paragraph{2.2.8}
Use the definition of commutator and carry out the corresponding matrix multiplication, then all the three relations are trivially satisfied.

\paragraph{2.2.9}
Carry out the corresponding matrix multiplication, then all the relations are trivially satisfied.

\paragraph{2.2.10}
If $A$ and $B$ are upper right triangular matrices, then $A_{ij}=0$ when $j<i$, $B_{ij}=0$ when $j<i$. $(AB)_{ij}=\sum_k A_{ik}B_{kj}$, when $j<i$: if $k>j$, then $B_{kj}=0$, if $k\leq j$, then $k<i$ and $A_{ik}=0$. So in all case $(AB)_{ij}=\sum_k A_{ik}B_{kj}=0$ when $j<i$, so $AB$ is also an upper right triangular matrix.

\paragraph{2.2.11}
(a)(b) By matrix multiplication the relations hold trivially.

(c) When $i=j$, $\sigma_i\sigma_j+\sigma_j\sigma_i=2(\sigma_i)^2=2I_2=2\delta_{ij}I_2$. When $i\neq j$: by (a) we know the inverse matrix of $\sigma_i$ is itself, and by (b) we have $\sigma_i\sigma_j=i\sigma_k$, so $(\sigma_i\sigma_j)^{-1}=\sigma_j^{-1}\sigma_i^{-1}=\sigma_j\sigma_i=(i\sigma_k)^{-1}=-i\sigma_k$, so $\sigma_i\sigma_j+\sigma_j\sigma_i=i\sigma_k-i\sigma_k=0=2\delta_{ij}I_2$. So $\sigma_i\sigma_j+\sigma_j\sigma_i=2\delta_{ij}I_2$ holds for all cases.

\paragraph{2.2.12}
(a)(b) By definition of commutator and matrix multiplication, the relations can be easily verified.

(c) $[M^2,M_i]=2IM_i-M_i2I=0$; $[M_z,L^+]=[M_z,M_x]+i[M_z,M_y]=iM_y+i(-i)M_x=M_x+iM_y$; $[L^+,L^-]=[M_x+iM_y,M_x-iM_y]=i[M_y.M_x]-i[M_x,M_y]=2M_z$

\paragraph{2.2.13}
It is similar with Exercise 2.2.12.

\paragraph{2.2.14}
If the $i^{th}$ diagonal entries of $A$ is $a_i$, then $(AB)_{ij}=a_iB_{ij}$, and $(BA)_{ij}=B_{ij}a_j$. So if $i\neq j$, then by $a_iB_{ij}=a_jB_{ij}$ and $a_i\neq a_j$, we have $B_{ij}=0$, which means $B$ is a diagonal matrix.

\paragraph{2.2.15}
$(AB)_{ij}=\sum_k A_{ik}B_{kj}=\sum_k a_i\delta_{ik}b_j\delta_{kj}=a_ib_j\delta_{ij}=a_ib_i\delta_{ij}$. $(BA)_{ij}=\sum_k B_{ik}A_{kj}=\sum_k b_i\delta_{ik}a_j\delta_{kj}=a_jb_i\delta_{ij}=a_ib_i\delta_{ij}$. So $(AB)_{ij}=(BA)_{ij}$, and $A$ and $B$ commute.

\newcommand{\trace}{\mathrm{trace}}

\paragraph{2.2.16}
For any two matrices $X,Y$ we have $\trace(XY)=\trace(YX)$. If $A,B$ commute, $\trace(ABC)=\trace(BAC)=\trace(CBA)$; if $B,C$ commute, $\trace(ABC)=\trace(ACB)=\trace(CBA)$; if $A,C$ commute, $\trace(ABC)=\trace(CAB)=\trace(ACB)=\trace(CBA)$.

\paragraph{2.2.17}
$\trace([M_j,M_k])=\trace(M_jM_k-M_kM_j)=\trace(M_jM_k)-\trace(M_kM_j)=0=\trace(iM_l)=i\trace(M_l)$, so $\trace(M_l)=0$, ans so as $M_j$ and $M_k$ because the commutation relation is cyclic.

\paragraph{2.2.18}
$\trace(A)=\trace(ABB)=\trace(BAB)=\trace(-ABB)=\trace(-A)=-\trace(A)$, so $\trace(A)=0$. The same is for $\trace(B)$.

\paragraph{2.2.19}
(a) If $AB=-BA$ and both are non-singular (so the matrix inverses exist): $\trace(A)=\trace(ABB^{-1})=\trace(B^{-1}AB)=\trace(-B^{-1}BA)=\trace(-A)=-\trace(A)$, so $\trace(A)=0$. The same is for $\trace(B)$.

(b) $A,B$ being non-singular means $\det(A),\det(B)\neq0$. Suppose they are anti-commuting and n is odd, then $\det(A)\det(B)=\det(AB)=\det(-BA)=\det(-B)\det(A)=(-1)^n\det(B)\det(A)=-\det(A)\det(B)$, so $\det(A)\det(B)=0$. So either  $\det(A)$ or $\det(B)$ equals to zero, contradicting to $\det(A),\det(B)\neq0$. 

\paragraph{2.2.20}
$(A^{-1}A)_{ik}=\sum_j(A^{-1})_{ij}A_{jk}=\sum_j\frac{(-1)^{i+j}M_{ji}}{\det(A)}A_jk=\frac{1}{\det(A)}\sum_j(-1)^{i+j}M_{ji}A_{jk}$. If $i=k$, notice that $\det(A)=\det(A^T)=\sum_{j}(-1)^{i+j}M_{ji}A_{ji}$, so $(A^{-1}A)_{ik}=\frac{\det(A)}{\det(A)}=1$; if $i\neq k$, then $(A^{-1}A)_{ik}=\frac{1}{\det(A)}\sum_{j}(-1)^{i+j}M_{ji}A_{jk}=\frac{1}{\det(A)}A_{jk}C_{ji}=0$ by Exercise 2.1.4(b) (it is obvious by noticing that $\sum_{j}(-1)^{i+j}M_{ji}A_{jk}$ is the determinant of A whose $k^{th}$ column is replaced by $j^{th}$ column, and the determinant of matrix with two same column is zero). Therefore, $(A^{-1}A)_{ik}=\delta_{ik}$, so $A^{-1}A=I$.

\paragraph{2.2.21}
(a) The unit matrix with $M_{ii}$ replaced by $k$.

(b) The unit matrix with $M_{im}$ replaced by $-K$.

(c) The unit matrix with $M_{ii},M_{mm}$ replaced by 0 and $M_{im},M_{mi}$ replaced by 1.

\paragraph{2.2.22}
(a) The unit matrix with $M_{ii}$ replaced by $k$.

(b) The unit matrix with $M_{mi}$ replaced by $-k$.

(c) The unit matrix with $M_{ii},M_{mm}$ replaced by 0 and $M_{im},M_{mi}$ replaced by 1.

\paragraph{2.2.23}
By Gauss-Jordan matrix inversion, $A^{-1}=
\begin{pmatrix}
1&-1&0\\
-1&\frac{11}{7}&-\frac{1}{7}\\
0&-\frac{1}{7}&\frac{2}{7}
\end{pmatrix}
$

\paragraph{2.2.24}
(a) $\sum_{i=1}^nT_{ij}$ is the sum of fraction of population of $j$th area having moved to other(including $j$) areas, so the sum add up to 1.

(b) $\sum_{i=1}^nQ_i=\sum_{i=1}^n(TP)_i=\sum_{i=1}^n\sum_{j=1}^n T_{ij}P_j=\sum_{j=1}^n\left(\sum_{i=1}^nT_{ij} \right)P_j=\sum_{j=1}^nP_j=1$

\paragraph{2.2.25}
\renewcommand{\arraystretch}{1.5}
\[
\begin{pmatrix}
1&\frac{1}{2}&\frac{1}{4}&\frac{1}{8}&\frac{1}{16}&\frac{1}{32}\\
\frac{1}{2}&1&\frac{1}{2}&\frac{1}{4}&\frac{1}{8}&\frac{1}{16
}\\
\frac{1}{4}&\frac{1}{2}&1&\frac{1}{2}&\frac{1}{4}&\frac{1}{8}\\
\frac{1}{8}&\frac{1}{4}&\frac{1}{2}&1&\frac{1}{2}&\frac{1}{4}\\
\frac{1}{16}&\frac{1}{8}&\frac{1}{4}&\frac{1}{2}&1&\frac{1}{2}\\
\frac{1}{32}&\frac{1}{16}&\frac{1}{8}&\frac{1}{4}&\frac{1}{2}&1\\
\end{pmatrix}
\begin{pmatrix}
1&0&0&0&0&0\\
0&1&0&0&0&0\\
0&0&1&0&0&0\\
0&0&0&1&0&0\\
0&0&0&0&1&0\\
0&0&0&0&0&1\\
\end{pmatrix}
\xrightarrow{R_i-\frac{1}{2}R_{i-1}\rightarrow R_i \,i=6\sim2}
\]
\[
\begin{pmatrix}
1&\frac{1}{2}&\frac{1}{4}&\frac{1}{8}&\frac{1}{16}&\frac{1}{32}\\
0&\frac{3}{4}&\frac{3}{8}&\frac{3}{16}&\frac{3}{32}&\frac{3}{64}\\
0&0&\frac{3}{4}&\frac{3}{8}&\frac{3}{16}&\frac{3}{32}\\
0&0&0&\frac{3}{4}&\frac{3}{8}&\frac{3}{16}\\
0&0&0&0&\frac{3}{4}&\frac{3}{8}\\
0&0&0&0&0&\frac{3}{4}\\
\end{pmatrix}
\begin{pmatrix}
1&0&0&0&0&0\\
-\frac{1}{2}&1&0&0&0&0\\
0&-\frac{1}{2}&1&0&0&0\\
0&0&-\frac{1}{2}&1&0&0\\
0&0&0&-\frac{1}{2}&1&0\\
0&0&0&0&-\frac{1}{2}&1\\
\end{pmatrix}
\xrightarrow[R_i-\frac{1}{2}R_{i+1}\rightarrow R_i \,i=1\sim5]{\frac{3}{4}R_1\rightarrow R_1}
\]
\[
\begin{pmatrix}
\frac{3}{4}&0&0&0&0&0\\
0&\frac{3}{4}&0&0&0&0\\
0&0&\frac{3}{4}&0&0&0\\
0&0&0&\frac{3}{4}&0&0\\
0&0&0&0&\frac{3}{4}&0\\
0&0&0&0&0&\frac{3}{4}\\
\end{pmatrix}
\begin{pmatrix}
1&-\frac{1}{2}&0&0&0&0\\
-\frac{1}{2}&\frac{5}{4}&-\frac{1}{2}&0&0&0\\
0&-\frac{1}{2}&\frac{5}{4}&-\frac{1}{2}&0&0\\
0&0&-\frac{1}{2}&\frac{5}{4}&-\frac{1}{2}&0\\
0&0&0&-\frac{1}{2}&\frac{5}{4}&-\frac{1}{2}\\
0&0&0&0&-\frac{1}{2}&1\\
\end{pmatrix}
\xrightarrow{\frac{4}{3}R_i\rightarrow R_i\,i=1\sim 6}
\]
\[
\begin{pmatrix}
1&0&0&0&0&0\\
0&1&0&0&0&0\\
0&0&1&0&0&0\\
0&0&0&1&0&0\\
0&0&0&0&1&0\\
0&0&0&0&0&1\\
\end{pmatrix}
\begin{pmatrix}
\frac{4}{3}&-\frac{2}{3}&0&0&0&0\\
-\frac{2}{3}&\frac{5}{3}&-\frac{2}{3}&0&0&0\\
0&-\frac{2}{3}&\frac{5}{3}&-\frac{2}{3}&0&0\\
0&0&-\frac{2}{3}&\frac{5}{3}&-\frac{2}{3}&0\\
0&0&0&-\frac{2}{3}&\frac{5}{3}&-\frac{2}{3}\\
0&0&0&0&-\frac{2}{3}&\frac{4}{3}\\
\end{pmatrix}
\]

\paragraph{2.2.26}
If $A,B$ are orthogonal, $AA^T=I$ and $BB^T=I$, then $(AB)(AB)^T=ABB^TA^T=AA^T=I$, so $AB$ is also orthogonal.

\paragraph{2.2.27}
$\det(AA^T)=\det(A)\det(A^T)=(\det(A))^2=\det(I)=1$, so $\det(A)=\pm1$

\paragraph{2.2.28}
If $A=A^T$ and $B=-B^T$, then $\trace(AB)=\trace(BA)=\trace(-B^TA^T)=\trace(-(AB)^T)=-\trace(AB)$, so $\trace(AB)=0$.

\paragraph{2.2.29}
\renewcommand{\arraystretch}{1}
$AA^T=\begin{pmatrix}a&b\\c&d\end{pmatrix}\begin{pmatrix}a&c\\b&d\end{pmatrix}=\begin{pmatrix}1&0\\0&1\end{pmatrix}$, so $a^2+b^2=1$, $c^2+d^2=1$, $ac+bd=0$. Let $\theta=\tan^{-1}\frac{b}{a}$, then $a=\cos\theta$, $b=\sin\theta$, $\frac{c}{d}=-\tan{\theta}$, $c=-\sin\theta$, $d=\cos\theta$. So the most general form is $\begin{pmatrix}\cos\theta&\sin\theta\\-\sin\theta&\cos\theta\end{pmatrix}$.

\paragraph{2.2.30}
$\det(A^*)=\sum_{ij\cdots}\varepsilon_{ij\cdots}a_{1i}^*a_{2j}^*\cdots=(\sum_{ij\cdots}\varepsilon_{ij\cdots}a_{1i}a_{2j}\cdots)^*=(\det A)^*$

$\det(A^*)=\det((A^*)^T)=A^\dagger$

\paragraph{2.2.31}
If two of the matrices are real, then their commutator is real, so $i$ multiply the third matrix must be real, so the third matrix must be  pure imaginary.

\paragraph{2.2.32}
$(AB)^\dagger=((AB)^T)^*=(B^TA^T)^*=((B)^T)^*((A)^T)^*=B^\dagger A^\dagger$

\paragraph{2.2.33}
$S^\dagger_{ij}=S^*_{ji}$, so 
$\trace(S^\dagger S)=\sum_i(S^\dagger S)_{ii}=\sum_i\sum_j S^\dagger_{ij}S_{ji}=\sum_i\sum_j|S_{ji}|^2>0$ when $S$ is not null matrix.

\paragraph{2.2.34}
$A^\dagger=A$, $B^\dagger=B$. $(AB+BA)^\dagger=B^\dagger A^\dagger+A^\dagger B^\dagger=BA+AB=AB+BA$; $[i(AB-BA)]^\dagger=-i(B^\dagger A^\dagger-A^\dagger B^\dagger)=-i(BA-AB)=i(AB-BA)$. So both $(AB-BA)$ and $i(AB-BA)$ are Hermitian.

\paragraph{2.2.35}
$(C+C^\dagger)^\dagger=C^\dagger+C=C+C^\dagger$; $[i(C-C^\dagger)]^\dagger=-i(C^\dagger-C)=i(C-C^\dagger)$. So both matrices are Hermitian,

\paragraph{2.2.36}
$C=-i(AB-BA)$, $C^\dagger=i(B^\dagger A^\dagger-A^\dagger B^\dagger)=i(BA-AB)=-i(AB-BA)=C$ so $C$ is Hermitian.

\paragraph{2.2.37}
If $AB=BA$, then $(AB)^\dagger=B^\dagger A^\dagger=BA=AB$ so $AB$ is Hermitian; if $AB$ is Hermitian, then $AB=(AB)^\dagger=B^\dagger A^\dagger=BA$. Therefore, $AB=BA$ is a necessary and sufficient condition for $AB$ to be Hermitian.

\paragraph{2.2.38}
$UU^\dagger=I$, $U^\dagger=U^{-1}$, $U=(U^{-1})^\dagger$, $U^{-1}U=I=U^{-1}(U^{-1})^\dagger$, so $U^{-1}$ is unitary.

\paragraph{2.2.39}
It is obvious that $(A\otimes B)^T=A^T\otimes B^T$, so $(A\otimes B)^\dagger=A^\dagger\otimes B^\dagger$. If $A$ and $B$ are unitary, then $(A\otimes B)(A\otimes B)^\dagger =(A\otimes B)(A^\dagger\otimes B^\dagger)=(AA^\dagger\otimes BB^\dagger)=I_1\otimes I_2=I$

\paragraph{2.2.40}
$\boldsymbol{\sigma}\cdot\mathbf{p}=\sigma_1p_1+\sigma_2p_2+\sigma_3p_3=
\begin{pmatrix}
0&p_1\\p_1&0
\end{pmatrix}+
\begin{pmatrix}
0&-ip_2\\ip_2&0
\end{pmatrix}+
\begin{pmatrix}
p_3&0\\0&-p_3
\end{pmatrix}=
\begin{pmatrix}
p_3&p_1-ip_2\\p_1+ip_2&-p_3
\end{pmatrix}
$,
so $(\boldsymbol{\sigma}\cdot\mathbf{p})^2=\begin{pmatrix}
p_3&p_1-ip_2\\p_1+ip_2&-p_3
\end{pmatrix}\begin{pmatrix}
p_3&p_1-ip_2\\p_1+ip_2&-p_3
\end{pmatrix}=
\begin{pmatrix}
\mathbf{p}^2&0\\0&\mathbf{p}^2
\end{pmatrix}=\mathbf{p}^2\mathbf{1}_2
$

\paragraph{2.2.41}
$(\gamma^0)^2=(\sigma_3)^2\otimes(1_2)^2=1_2\otimes1_2=1_4$. $(\gamma^i)^2=\gamma^2\otimes(\sigma_i)^2=(-1_2)\otimes1_2=-1_4$. When $\mu\neq0$, $\gamma^\mu\gamma^i+\gamma^i\gamma^\mu=\gamma^2\otimes(\sigma_\mu\sigma_i)+\gamma^2\otimes(\sigma_i\sigma_\mu)=\gamma^2\otimes(\sigma_\mu\sigma_i+\sigma_i\sigma_\mu)=\gamma^2\otimes0=0$; when $\mu=0$, $\gamma^0\gamma^i+\gamma^i\gamma^0=(\sigma_3\gamma)\otimes(\sigma_i)+(\gamma\sigma_3)\otimes(\sigma_i)=
\begin{pmatrix}0&1\\1&0\end{pmatrix}\otimes(\sigma_i)+
\begin{pmatrix}0&-1\\-1&0\end{pmatrix}\otimes(\sigma_i)=0
$

\paragraph{2.2.42}
$\gamma^5\gamma^\mu=i\gamma^0\gamma^1\gamma^2\gamma^3\gamma^\mu$. Switch $\gamma^\mu$ with $\gamma^i$ left to it: if $i=\mu$, it won't cange; if $i\neq\mu$, it will be multiplied $(-1)$ by the anti-commuting properties. So after switching four times to move $\gamma^\mu$ to the left-most side, three $(-1)$ have been multiplied, so $\gamma^5\gamma^\mu=-i\gamma^\mu\gamma^0\gamma^1\gamma^2\gamma^3=-\gamma^\mu\gamma^5$, so $\gamma^5$ anti-commutes with all four $\gamma^\mu$.

\paragraph{2.2.43}
($\gamma_\mu=\sum g_{\nu\mu}\gamma^\mu=$ should be $\gamma_\nu=\sum g_{\nu\mu}\gamma^\mu$) $\gamma_0=\gamma^0$ and $\gamma_i=-\gamma ^i,\,i=1,2,3$. Along with $(\gamma^0)^2=1$ and $(\gamma^i)^2=-1$, we have $\gamma_\mu\gamma^\mu=1,\,\mu=0,1,2,3$.
\medskip

(a) If $\mu=\alpha$, $\gamma_\mu\gamma^\alpha\gamma^\mu=\gamma_\mu\gamma^\mu\gamma^\alpha=\gamma^\alpha$; if $\mu\neq\alpha$, $\gamma_\mu\gamma^\alpha\gamma^\mu=-\gamma_\mu\gamma^\mu\gamma^\alpha=-\gamma^\alpha$. So $\sum\gamma_\mu\gamma^\alpha\gamma^\mu=(1-3)\gamma^\alpha=-2\gamma^\alpha$
\medskip

(b) If $\alpha=\beta$, $\gamma_\mu\gamma^\alpha\gamma^\beta\gamma^\mu=\gamma^\alpha\gamma^\beta=(\gamma^\alpha)^2=g^{\alpha\alpha}=g^{\alpha\beta}$ for all $\mu=0,1,2,3$, so $\sum\gamma_\mu\gamma^\alpha\gamma^\beta\gamma^\mu=4g^{\alpha\beta}$. If $\alpha\neq\beta$, for $\mu=\alpha$ or $\mu=\beta$, $\gamma_\mu\gamma^\alpha\gamma^\beta\gamma^\mu=-\gamma^\alpha\gamma^\beta$, and for $\mu\neq\alpha$ and $\mu\neq\beta$, $\gamma_\mu\gamma^\alpha\gamma^\beta\gamma^\mu=\gamma^\alpha\gamma^\beta$, so $\sum\gamma_\mu\gamma^\alpha\gamma^\beta\gamma^\mu=(-2+2)\gamma^\alpha\gamma^\beta=0=g^{\alpha\beta}$. So $\sum\gamma_\mu\gamma^\alpha\gamma^\beta\gamma^\mu=4g^{\alpha\beta}$.
\medskip

(c)
If $\alpha,\beta,\nu$ are different with each other, then $\sum\gamma_\mu\gamma^\alpha\gamma^\beta\gamma^\nu\gamma^\mu=(3-1)\gamma^\alpha\gamma^\beta\gamma^\nu=2(-1)^3\gamma^\nu\gamma^\beta\gamma^\alpha=-2\gamma^\nu\gamma^\beta\gamma^\alpha$. If only two of  $\alpha,\beta,\nu$ are the same, then $\sum\gamma_\mu\gamma^\alpha\gamma^\beta\gamma^\nu\gamma^\mu=(-3+1)\gamma^\alpha\gamma^\beta\gamma^\nu=-2(1)(-1)^2\gamma^\nu\gamma^\beta\gamma^\alpha\\=-2\gamma^\nu\gamma^\beta\gamma^\alpha$. If $\alpha,\beta,\nu$ are all the same, then $\sum\gamma_\mu\gamma^\alpha\gamma^\beta\gamma^\nu\gamma^\mu=(-3+1)\gamma^\alpha\gamma^\beta\gamma^\nu=-2\gamma^\nu\gamma^\beta\gamma^\alpha$. Therefore, in all cases, $\sum\gamma_\mu\gamma^\alpha\gamma^\beta\gamma^\nu\gamma^\mu=-2\gamma^\nu\gamma^\beta\gamma^\alpha$.



\paragraph{2.2.44}
$(\gamma^5)^2=-\gamma^0\gamma^1\gamma^2\gamma^3\gamma^0\gamma^1\gamma^2\gamma^3=-(-1)^{3+2+1}(\gamma^0)^2(\gamma^1)^2(\gamma^2)^2(\gamma^3)^2=1$, so\\ $M^2=\frac{1}{4}(1+2\gamma^5+(\gamma^5)^2)=\frac{1}{4}(2+2\gamma^5)=\frac{1}{2}(1+\gamma^5)=M$.

\paragraph{2.2.45}
By evaluation, we can found that the 16 Dirac matrices is equal to $(i)^n\sigma_i\otimes\sigma_j,\,i,j=0,1,2,3$ with each Dirac matrix having different $(i,j)$, if we let $\sigma_0=1_2$, $n$ depend on $i,j$. Then the problem is equivalent to prove that the 16 $\sigma_i\otimes\sigma_j$ form a linearly independent set. If $a,b\neq0$ and $(i.j)\neq(k,l)$, then  $a\sigma_i\otimes\sigma_j+b\sigma_k\otimes\sigma_l\neq0$ because the four $\sigma_\mu$ form a linearly independent set. So the 16 $\sigma_i\otimes\sigma_j$ form a linearly independent set, and the 16 Dirac matrices form a linearly independent set

\paragraph{2.2.46}
(The 16 Dirac matrices is defined as $E_{ij}=\sigma_i\otimes\sigma_j$, $i,j=0,1,2,3$, where $\sigma_0=I_2$) \\For $(i,j)\neq(0,0)$, $\trace(E_{ij})=\trace(\sigma_i)(\sigma_j)=0$ because $\trace(\sigma_k)=0$ when $k=1,2,3$. So $\trace(E_{ij}E_{mn})\neq0$ only when $(\sigma_i\otimes\sigma_j)(\sigma_m\otimes\sigma_n)=\sigma_0\otimes\sigma_0$, that is, $i=m$ and $j=n$. Let $c_i=c_{mn}$, $\Gamma_i=E_{mn}$,  $\sum_{i=1}^{16}c_i\Gamma_i=\sum_{i,j=0}^3c_{ij}E_{ij}$, then $\trace(A\Gamma_i)=\trace(\sum_{i,j=0}^3c_{ij}E_{ij}E_{mn})=c_{mn}\trace(E_{mn}E_{mn})=c_{mn}\trace(I_4)=4c_{mn}=4c_i$, so $c_i=\frac{1}{4}\trace(A\Gamma_i)$.

\paragraph{2.2.47}
Note that $(\gamma^0)^T=\gamma^0$, $(\gamma^1)^T=-\gamma^1$, $(\gamma^2)^T=\gamma^2$, $(\gamma^3)^T=-\gamma^3$. $C^{-1}=-i(\gamma^0)^{-1}(\gamma^2)^{-1}=i\gamma^0\gamma^2$, so $C\gamma^\mu C^{-1}=-\gamma^2\gamma^0\gamma^\mu\gamma^0\gamma^2$. If $\mu=0$ or $2$, $-\gamma^2\gamma^0\gamma^\mu\gamma^0\gamma^2=-(-1)(1)(-1)\gamma^\mu=-\gamma^\mu=-(\gamma^\mu)^T$; If $\mu=1$ or $3$, $-\gamma^2\gamma^0\gamma^\mu\gamma^0\gamma^2=-(-1)^2(1)(-1)\gamma^\mu=\gamma^\mu=-(\gamma^\mu)^T$. So in all cases $C\gamma^\mu C^{-1}=-(\gamma^\mu)^T$.

\paragraph{2.2.48}
(a) \[\gamma^0mc^2=mc^2\sigma_3\otimes I_2=
\begin{pmatrix}mc^2&0\\0&-mc^2\end{pmatrix}\] \[c(\alpha_1p_1+\alpha_2p_2+\alpha_3p_3)=c\gamma^0(\gamma^1p_1+\gamma^2p_2+\gamma^3p_3)=c(\sigma_3\otimes I_2)(\gamma\otimes\sigma_1p_1+\gamma\otimes\sigma_2p_2+\gamma\otimes\sigma_3p_3)\]
\[=c\sigma_1\otimes(\sigma_1p_1+\sigma_2p_2+\sigma_3p_3)=
\begin{pmatrix}
0&c(\sigma_1p_1+\sigma_2p_2+\sigma_3p_3)\\\sigma_1p_1+\sigma_2p_2+\sigma_3p_3&0\end{pmatrix}\]
\[-EI_4=-EI_2\otimes I_2=
\begin{pmatrix}
-E&0\\0&-E
\end{pmatrix}
\]
\[\psi=
\begin{pmatrix}
\psi_L\\\psi_S
\end{pmatrix}
\]
So $\left[\gamma^0mc^2+c(\alpha_1p_1+\alpha_2p_2+\alpha_3p_3)-E\right]\psi=0$ becomes
\[
\begin{pmatrix}
mc^2-E&c(\sigma_1p_1+\sigma_2p_2+\sigma_3p_3)\\
c(\sigma_1p_1+\sigma_2p_2+\sigma_3p_3)&-mc^2-E
\end{pmatrix}
\begin{pmatrix}
\psi_L\\\psi_S
\end{pmatrix}=0
\]

(b) By the indicated approximation, the equation becomes
\[
\begin{pmatrix}
-\varepsilon&c(\sigma_1p_1+\sigma_2p_2+\sigma_3p_3)\\
c(\sigma_1p_1+\sigma_2p_2+\sigma_3p_3)&-2mc^2
\end{pmatrix}
\begin{pmatrix}
\psi_L\\\psi_S
\end{pmatrix}=0
\]
It can be separated to $\varepsilon\psi_L=c(\alpha_1p_1+\alpha_2p_2+\alpha_3p_3)\psi_S$ and $c(\alpha_1p_1+\alpha_2p_2+\alpha_3p_3)\psi_L=2mc^2\psi_S$. Eliminating $\psi_S$ and we obtain $\frac{1}{2m}\left(p_1^2+p_2^2+p_3^2\right)\psi_L=\varepsilon\psi_L$

(c) From the two separated equations, we can get $(\frac{\psi_S}{\psi_L})^2=\frac{\varepsilon}{2mc^2}\ll1$ in the non-relativistic approximation.

\paragraph{2.2.49}
\[(\gamma^0)^2=
\begin{pmatrix}
I_2&0\\0&I_2
\end{pmatrix}=I_4
\]
\[
(\gamma^i)^2=
\begin{pmatrix}
-\sigma_i^2&0\\0&-\sigma_i^2
\end{pmatrix}=
\begin{pmatrix}
-I_2&0\\0&-I_2
\end{pmatrix}=-I_4 ,\, i=1,2,3
\]
\[
\gamma^\mu\gamma^i+\gamma^i\gamma^\mu=
\begin{pmatrix}
-\sigma_\mu\sigma_i&0\\
0&-\sigma_\mu\sigma_i
\end{pmatrix}+
\begin{pmatrix}
-\sigma_i\sigma_\mu&0\\
0&-\sigma_i\sigma_\mu
\end{pmatrix}=
0,\,\mu\neq i
\]

\paragraph{2.2.50}
As in Exercise 2.2.48 but with $\gamma^0$ and $\gamma^i$ defined in Exercise 2.2.49, the Dirac equation becomes
\[
\begin{pmatrix}
-c(\sigma_1p_1+\sigma_2p_2+\sigma_3p_3)-E&mc^2\\
mc^2&c(\sigma_1p_1+\sigma_2p_2+\sigma_3p_3)-E
\end{pmatrix}
\begin{pmatrix}
\psi_L\\\psi_S
\end{pmatrix}=0
\]
In the limit that m approaches zero, the equation becomes
\[
\begin{pmatrix}
-c(\sigma_1p_1+\sigma_2p_2+\sigma_3p_3)-E&0\\
0&c(\sigma_1p_1+\sigma_2p_2+\sigma_3p_3)-E
\end{pmatrix}
\begin{pmatrix}
\psi_L\\\psi_S
\end{pmatrix}=0
\]
which separates into independent $2\times2$ blocks.

\paragraph{2.2.51}
(a) $|r'|^2=r'^\dagger r'=r^\dagger U^\dagger Ur=r^\dagger r=|r|^2$

(b) $r^\dagger r=r'^\dagger r'=r^\dagger U^\dagger Ur$ for any $r$, so $U^\dagger U=I$.
