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
since $X^*1$ is constant. Alternatively, we can use the fact that the integral of $X\vert f\vert$ along all the lines with the same direction equals $\left\Vert f\right\Vert_1$, which also implies that $X:L^1(\mathbb{R}^n)\to L^1(M_n)$. Any other bound of the X-ray transform can be interpolated with this bound to get further inequalities.

 +-- {: .num_defn #SobolevSlobodeckij}
###### Definition
**([[Sobolev space]])

Let $\varphi$ be a smooth function with Fourier transform supported in $\vert\xi\vert\sim 1$, and let $\tilde{\varphi}$ be a smooth function with Fourier transform supported in $\vert\xi\vert\lesssim 1$. Suppose that 
$$
1 = \sum_{k\ge 0}\varphi_k,
$$
where $\varphi_0 := \tilde{\varphi}$ and $\varphi_k(x) := \varphi(x/2^k)$, for $k\ge 1$. Let $P_k$ be the projection $(P_k f)^\wedge := \varphi_k \hat{f}$. 

The Sobolev-Slobodeckij spaces $W^{s,p}(\mathbb{R}^n)$ are, for $1\lt p\lt \infty$ and $-\infty\lt s\lt \infty$, defined as
$$
\Vert f\Vert_{W^{s,p}(\mathbb{R}^n)} := \Big[\sum_{k\ge 0}(2^{sk}\Vert P_kf\Vert_{L^p(\mathbb{R}^n)})^p\Big]^\frac{1}{p}\quad if s \neq integer,
$$
and
$$
\Vert f\Vert_{W^{s,p}(\mathbb{R}^n)} := \Big[\sum_{\vert\alpha\vert\le s}\Vert D^\alpha f\Vert_{L^p(\mathbb{R}^n)}^p\Big]^\frac{1}{p} \quad if s = integer.
$$
See ([Triebel 1978, Sec. 2.3.1](#triebel1978)).

=--

The relation between that X-ray transform and the Kakeya set conjecture is the content of the following Theorem

+-- {: .num_theorem}
###### Theorem

Let $n-sp\gt 0$. If for every function $f$ with compact support $K$ it holds that
$$
\label{eqThmXRayKakeya}
\Vert Xf\Vert_{L^1_\sigma L^\infty_x(M_n)}\le C_K\Vert f\Vert_{W^{s,p}(\mathbb{R}^n)},
$$
then the Hausdorff dimension of a Kakeya set is at least $n-sp$.

=--

+-- {: .proof}
###### Proof

To compute the Hausdorff dimension we can use both balls $B_r(x)$ and dyadic cubes $Q_k := [l2^k,(l+1)2^k]^n$, for $k$ integer. In fact, we can cover a cube $Q_k$ with a ball of radius $\sqrt{n}2^{k-1}$, and conversely we can cover a ball of radius $r$ with a few cubes $Q_k$, for $2^{k-1}\lt r\le 2^k$. 

Let $E\subset\mathbb{R}^n$ be a Kakeya set. Give any covering $\mathcal{C} = \{Q_k\}$ of $E$ at scale $0\lt\delta\le 1$, i.e. a covering such that for every cube $Q_k\in\mathcal{C}$ its side-length is $2^k\le\delta$, the goal is to show that if $0\le d\lt n-sp$ then
$$
\sum_{Q_k\in\mathcal{C}}l(Q_k)^d \to \infty \quad as\;\delta\to 0,
$$
where $l(Q_k) = 2^k$ is the side-length of the cube.

Let $\mathcal{C}$ be a covering of $E$ at scale $\delta$. We denote by $\mathcal{C}_k$ the collection of all the cubes in $\mathcal{C}$ with side-length $2^k$, and we denote by $A_k$ the union of all the cubes in $\mathcal{C}_k$; therefore,
$$
1_E \le \sum_k 1_{A_k} := \sum_k \Big(\sum_{Q_k\in\mathcal{C}_k}1_{Q_k}\Big).
$$ 
Since our hypotheses involve the spaces $W^{s,p}$, we should mollify $1_{A_k}$. We take a suitable smooth function $\varphi$ with compact support,  define the dilations $\varphi_k(x) := 2^{-nk}\varphi(x/2^k)$, and replace $1_{A_k}$ by $\varphi_k*1_{A_k}$. 

Since $E$ contains a unit line segment in every direction $\sigma$, then for every $\sigma\in \mathbb{P}^{n-1}$ it holds that $\Vert X1_E(\cdot,\sigma)\Vert_{L^\infty} \ge 1$, and then that
$$
1\le \Vert X1_E\Vert_{L^1_\sigma L^\infty_x}\le C\sum_{2^k\le\delta}\Vert X\big(\varphi_k*1_{A_k}\big)\Vert_{L^1_\sigma L^\infty_x}.
$$
By (eq:eqThmXRayKakeya) we have that
$$
1\le C\sum_{2^k\le\delta} \Vert \varphi_k*1_{A_k}\Vert_{W^{s,p}}.
$$
In general, the $W^{s,p}$-norm of $\varphi_k*f$ is
$$
\Vert f\Vert_{W^{s,p}}\le C2^{-ks}\Vert f\Vert_p;
$$
see Lemma below. Hence,
$$
1\le C\sum_{2^k\le\delta} \Vert \varphi_k*1_{A_k}\Vert_{W^{s,p}} \le C\sum_{2^k\le\delta}2^{-ks+\frac{nk}{p}}\vert \mathcal{C}_k\vert^\frac{1}{p}
$$
where $\vert \mathcal{C}_k\vert$ denotes the number of cubes in $\mathcal{C}_k$.

By hypothesis $n-sp\gt 0$, then for every $0\le d \lt n-sp$ we can apply Hölder inequality to get
$$
1 \le \Big(\sum_{2^k\le\delta} 2^{p'k(\frac{n-d}{p}-s)}\Big)^\frac{1}{p'}\Big(\sum_k 2^{kd}\vert\mathcal{C}_k\vert\Big)^\frac{1}{p} \le C\delta^\alpha\Big(\sum_{Q_k\in\mathcal{C}}l(Q_k)^d\Big)^\frac{1}{p},
$$
where $\alpha = \frac{n-d}{p}-s\gt 0$. The statement of the Theorem follows. 

=--

For a fixed direction $\sigma$, the X-ray transform maps $f$ to a function $x\mapsto Xf(x,\sigma)$ in $\mathbb{R}^{n-1}$. The function $Xf(\cdot,\sigma)$ turns out to be more regular than $f$. 

+-- {: .num_theorem}
###### Theorem

If $f\in L^2(\mathbb{R}^n)$ then
$$
\label{eqThmL2Bound}
\left\Vert \vert D\vert^\frac{1}{2}Xf\right\Vert_{L^2(M_n)} \le C\left\Vert f\right\Vert_{L^2(\mathbb{R}^n)}.
$$

=--

The Sobolev embedding Theorem $\Vert f\Vert_{L^\infty(\mathbb{R}^{n-1})}\le C\Vert f\Vert_{W^{s,2}(\mathbb{R}^{n-1})}$, for $s\gt \frac{n-1}{2}$, and the inequality (eq:eqThmL2Bound) allow us to conclude that
$$
\Vert f\Vert_{L^2_\sigma L^\infty_x}\le C \Vert f\Vert_{W^{s,2}(\mathbb{R}^n)}
$$
for $s\gt \frac{n}{2}-1$. Hence, the Hausdorff dimension of a Kakeya set $E\subset\mathbb{R}^n$ is at least 2. This result is the best possible in $\mathbb{R}^2$, but  far away from the expected dimension for $n\ge 3$.

+-- {: .num_theorem}
###### Theorem
**(Drury, 1983)

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

* [[Bourgain, J.]], Besicovitch type maximal function operators and applications to Fourier Analysis, Geom. Funct. Anal., 1, 1991

* [[Christ, M.]], Estimates for the $k$-plane transform, Indiana Univ. Math. J., 33, 1984

* [[Drury, S. W.]], $L^p$ estimates for the X-ray transform, Illinois J. Math., 27, 1983

* {#triebel1978} [[Triebel, H]], Interpolation Theory, Function Spaces, Differential Operators, North-Holland publishing company, 1978