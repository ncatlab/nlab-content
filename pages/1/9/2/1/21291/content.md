## X-Ray Transform

The X-ray transform is the operator
$$
Xf(l) := \int_l f\,d\lambda(l),
$$
where $l\subset\mathbb{R}^n$ is a line, and $\lambda$ the Lebesgue measure on the line. The manifold $M_n$ can be represented as
$$
M_n = \{(\sigma, x)\in S^{n-1}\times\mathbb{R}^n \mid \langle x,\omega\rangle = 0\},
$$
where $(\sigma,x)$ represents a line that passes through $x$ with direction $\omega$. We endow $M_n$ with a measure $\mu$ invariant under rigid motions. It is an open problem to determine the exponents $1\le p,q,r\le\infty$ for which the following inequality holds:
$$
\left\Vert Xf\right\Vert_{L^q(\omega\mapsto L^r_x(\mathbb{R}^{n-1}))} \le C\left\Vert f\right\Vert_{L^p(\mathbb{R}^n)}.
$$
For brevity we will write $L^q_\omega L^r_x := L^q(\omega\mapsto L^r_x(\mathbb{R}^{n-1}))$.

Drury proved the following Theorem.

#### Theorem 

If $E\subset \mathbb{R}^n$ is a measurable set, and $1_E$ is the characteristic function of $E$, then
$$\left\Vert Xf\right\Vert_{L^{n+1,\infty}(M_n)} \le C\left\vert E\right\vert^\frac{2}{n+1},$$
where $L^{p,\infty}$ is the weak-$L^n$ space.

This inequality corresponds to the restricted weak version of the point $(p,q,r) = (\frac{n+1}{2}, n+1, n+1)$.

##### Proof

The dual operator $X^*$ is defined by duality as $\int gXf\,d\mu(l) = \int fX^*g\,dx$, where $f$ and $g$ are smooth functions. Therefore,
$$
X^*g = \int g\delta_x(l)\,d\mu,
$$
where $\delta_l(x) = \lim_{\varepsilon\to 0}\varepsilon^{-n+1}1_{\{l\mid l\cap B(x,\varepsilon)\neq\emptyset\}}$.
 
Set $f = 1_E$ and define the set $F := \{l\in M_n\mid Xf(l)\ge\lambda\}$, then 
$$
\lambda\vert F\vert \le \int_F Xf\,d\mu = \int fX^*1_F \,dx \le \left\Vert X^*1_F\right\Vert_\infty\left\Vert f\right\Vert_1.
$$
Now choose a point $x_0$ such that $X^*1_F(x_0)\ge \frac{1}{2}\left\Vert X^*1_F\right\Vert_\infty$ ---$x$ is _the Bourgain's bush_. By translation symmetry we can assume that $x_0 = 0$. If $\delta_0$ denotes the Dirac delta at the origin, then
$$
\int 1_F Xf\,X\delta_0\,d\mu(l) \ge \lambda\int_F X\delta_0\,d\mu(l)\ge \frac{\lambda}{2}\left\Vert X^*1_F\right\Vert_\infty.
$$
On the other hand
$$
\int 1_F Xf\,X\delta_0\,d\mu(l) \le \int fX^*(1_F X\delta_0)\,dx \le  \left\Vert f\right\Vert_{L^{n,1}} \left\Vert X^*(1_F X\delta_0)\right\Vert_{L^{\frac{n}{n-1},\infty}},
$$
where $L^{p,q}(\mathbb{R}^n)$ refers to the Lorentz spaces. The function $X^*(1_F X\delta_0)$ can be explicitly computed
$$
X^*(1_F X\delta_0)(x) = \frac{1}{\vert x\vert^{n-1}}1_F(l(0,x)),
$$
where $l(0,x)$ is the line that passes through $0$ and $x$. Then, we can estimate the norm as
$$
\left\Vert X^*(1_F X\delta_0)\right\Vert_{L^{\frac{n}{n-1},\infty}} = c_n\vert X^*1_F(0)\vert^\frac{n-1}{n}\le c_n\left\Vert X^*1_F\right\Vert_\infty^\frac{n-1}{n}.
$$
Hence, we get the upper bound
$$
\int 1_F Xf\,X\delta_0\,d\mu(l) \le c_n \left\Vert f\right\Vert_{L^{n,1}}\left\Vert X^*1_F\right\Vert_\infty^\frac{n-1}{n}.
$$
Hence, we have that
$$
\left\Vert f\right\Vert_{L^{n,1}}\ge c_n\lambda \left\Vert X^*1_F\right\Vert_\infty^\frac{1}{n}.
$$
Therefore, we conclude that
$$
c_n\vert F\vert\lambda^{n+1} \le \left\Vert f\right\Vert_1\left\Vert f\right\Vert_{L^{n,1}}^n,
$$
which implies the restricted weak inequality.