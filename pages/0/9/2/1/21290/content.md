## X-Ray Transform

The X-ray transform is the operator
$$Xf(l) := \int_l f\,d\lambda(x),$$
where $l\subset\mathbb{R}^n$ is a line, and $\lambda$ the Lebesgue measure on the line. The manifold $M_n$ can be represented as
$$
M_n = \{(\sigma, x)\in \mathbb{P}^{n-1}\times\mathbb{R}^n \mid \langle x,\sigma\rangle = 0\};
$$
here $\mathbb{P} := S^{n-1}/\{\pm\}$ is the space of lines in $\mathbb{R}^n$ that pass through the origin, and $(\sigma,x)$ represents a line that passes through $x$ with direction $\sigma$. We endow $M_n$ with a measure $\mu$ invariant under rigid motions. It is an open problem to determine the exponents $1\le p,q,r\le\infty$ for which the following inequality holds:
$$
\left\Vert Xf\right\Vert_{L^q(\sigma\mapsto L^r_x(\mathbb{R}^{n-1}))} \le C\left\Vert f\right\Vert_{L^p(\mathbb{R}^n)}.
$$
For brevity we will write $L^q_\sigma L^r_x := L^q(\sigma\mapsto L^r_x(\mathbb{R}^{n-1}))$.

We can write the X-ray transform of a function $f\in C_c^\infty(\mathbb{R}^n)$ as
$$
Xf(l) = \int f\delta_{l}(x)\,dx
$$
where $\delta_{l} := \lim_{\varepsilon\to 0}\varepsilon^{-n+1}1_{\{x\in\mathbb{R}^n\mid \;l\cap B_\varepsilon(x)\neq\emptyset\}}$. If $(\sigma,x)$ is a line $l\in M_n$, and $P_\sigma$ the projection to the plane $\{y\mid \langle y,\sigma\rangle = 0\}$, then $\delta_l$ is the pull-back $P_\sigma^*\delta_x = \delta_x\circ P_\sigma$, where $\delta_x$ is the Dirac delta centered at $x\in\mathbb{R}^{n-1}$.

The operator dual to $X$, _i.e._ $\int Xh\,f\,d\mu = \int h\,X^*f\,dx$, acts on functions $f$ in $M_n$ as
$$
X^*f = \int f\delta_{\{x\}}(l)\,d\mu(l);
$$
here $\delta_{\{x\}} := \lim_{\varepsilon\to 0}\varepsilon^{-n+1}1_{\{l\in M_n\mid \;l\cap B_\varepsilon(x)\neq\emptyset\}}$  ---this is a distribution in $M_n$, do not confuse with the typical Dirac delta $\delta_x$ centered at $x$. The distribution $\delta_{\{x\}}$ is the restriction of the measure $\mu$ in $M_n$ to the set of lines passing through $x\in\mathbb{R}^n$.

The first bound we can get for the X-ray transform is
$$
\int \vert Xf\vert\,d\mu(l) \le \int X\vert f\vert\,1\,d\mu(l) = \int \vert f\vert\,X^*1\,dx = \int \vert f\vert\,dx,
$$
since $X^*1$ is constant. Alternatively, we can use the fact that the integral of $X\vert f\vert$ along all the lines with the same direction equals $\left\Vert f\right\Vert_1$, which also implies the inclusion $X:L^1(\mathbb{R}^n)\to L^1(M_n)$. Any other bound of the X-ray transform can be interpolated with this bound to get further inequalities.

+-- {: .num_theorem}
###### Theorem
**(Drury's $L^{\frac{n+1}{2},1}\to L^{n+1,\infty}$ Inclusion)

If $E\subset \mathbb{R}^n$ is a measurable set, and $1_E$ is the characteristic function of $E$, then
\[
\label{eqThmDrury}
\left\Vert X(1_E)\right\Vert_{L^{n+1,\infty}(M_n)} \le C\left\vert E\right\vert^\frac{2}{n+1}.
\]

=--

###### Remark 

This inequality corresponds to the restricted weak version of the point $(p,q,r) = (\frac{n+1}{2}, n+1, n+1)$. The quasinorm of the space $L^{p,q}(\nu)$, for $1\le p\lt\infty$ and $1\le q \lt\infty$, is
$$
\left\Vert f\right\Vert_{p,q} := \Big(p\int_0^\infty s^q\nu\{\vert f\vert\ge s\}^\frac{q}{p}\frac{ds}{s}\Big)^\frac{1}{q},
$$
and, for $1\le p\lt\infty$ and $q=\infty$, is
$$
\left\Vert f\right\Vert_{p,\infty} := \sup_{s\gt 0} (s\nu\{\vert f\vert\ge s\}^\frac{1}{p})
$$

+-- {: .proof}
###### Proof
 
Let $f = 1_E$ and define the set $F := \{l\in M_n\mid Xf(l)\ge\lambda\}$, then 
$$
\label{eqProofDruryLowerBush}
\lambda\vert F\vert \le \int_F Xf\,d\mu = \int fX^*1_F \,dx \le \left\Vert X^*1_F\right\Vert_\infty\left\Vert f\right\Vert_1.
$$
This establishes a lower bound for $\left\Vert X^*1_F\right\Vert_\infty$, and we will get now an upper bound.

Choose a point $x_0$ such that $X^*1_F(x_0)\ge \frac{1}{2}\left\Vert X^*1_F\right\Vert_\infty$ ---$x_0$ is the center of the _Bourgain's bush_. By translation symmetry we can assume that $x_0 = 0$. If $\delta_0$ is the Dirac delta centered at the origin, then
$$
\label{eqProofDruryLower}
\int 1_F Xf\,X\delta_0\,d\mu(l) \ge \lambda\int_F X\delta_0\,d\mu(l)\ge \frac{\lambda}{2}\left\Vert X^*1_F\right\Vert_\infty.
$$
Here we can think of $X\delta_0$ as the distribution we defined earlier $\delta_{\{0\}} := \lim_{\varepsilon\to 0}\varepsilon^{-n+1}1_{\{l\in M_n\mid \;l\cap B_\varepsilon(0)\neq\emptyset\}}$ supported over the lines passing through the point $0$. We can also justify the notation $X\delta_0$ by a limiting process since $\delta_0 := \lim_{\varepsilon\to 0}\varepsilon^{-n}1_{B_\varepsilon(0)}$.

On the other hand, we can also estimate the left side of (eq:eqProofDruryLower) as
$$
\int 1_F Xf\,X\delta_0\,d\mu(l) \le \int fX^*(1_F X\delta_0)\,dx \le  \left\Vert f\right\Vert_{L^{n,1}} \left\Vert X^*(1_F X\delta_0)\right\Vert_{L^{\frac{n}{n-1},\infty}},
$$
The function $X^*(1_F X\delta_0)$ can be computed explicitly
$$
X^*(1_F X\delta_0)(x) = \frac{1}{\vert x\vert^{n-1}}1_F(l(\tilde{x}, 0)),
$$
where $\tilde{x} := x/\vert x\vert$ and $l(\tilde{x}, 0)$ is the line that passes through $0$ and $x$. Then, we can estimate the norm of $X^*(1_F X\delta_0)$ as
$$
\left\Vert X^*(1_F X\delta_0)\right\Vert_{L^{\frac{n}{n-1},\infty}} = c_n\vert X^*1_F(0)\vert^\frac{n-1}{n}\le c_n\left\Vert X^*1_F\right\Vert_\infty^\frac{n-1}{n}.
$$
Then we get the bound
$$
\label{eqProofDruryUpper}
\int 1_F Xf\,X\delta_0\,d\mu(l) \le c_n \left\Vert f\right\Vert_{L^{n,1}}\left\Vert X^*1_F\right\Vert_\infty^\frac{n-1}{n}.
$$
By (eq:eqProofDruryLower) and (eq:eqProofDruryUpper) we get the desired upper bound for $\left\Vert X^*1_F\right\Vert_\infty$:
$$
c_n\lambda \left\Vert X^*1_F\right\Vert_\infty^\frac{1}{n} \lesssim \left\Vert f\right\Vert_{L^{n,1}}.
$$
This and (eq:eqProofDruryLowerBush) allow us to conclude that
$$
\vert F\vert \lesssim \frac{1}{\lambda^{n+1}}\left\Vert f\right\Vert_1\left\Vert f\right\Vert_{L^{n,1}}^n = \frac{1}{\lambda^{n+1}}\vert E\vert^2,
$$
which implies the restricted weak inequality (eq:eqThmDrury).

=--

## References

* [[Drury, S. W.]], $L^p$ estimates for the X-ray transform, Illinois J. Math., 27, 1983

* [[Christ, M.]], Estimates for the $k$-plane transform, Indiana Univ. Math. J., 33, 1984

* [[Bourgain, J.]], Besicovitch type maximal function operators and applications to Fourier Analysis, Geom. Funct. Anal., 1, 1991