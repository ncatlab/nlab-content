

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

\tableofcontents

## Idea

A *Kakeya Set* is a [[subset]] of a [[Euclidean space]] that contains a unit line segment for every [[direction]]. For example, a [[ball]] is a Kakeya set.

The *Kakeya Set Conjecture* asserts that every [[compact topological space|compact]] Kakeya set $E\subset\mathbb{R}^n$ has [[Hausdorff dimension]] $n$.

## X-Ray Transform

The *X-ray transform* is the operator
$$\operatorname{X} f(l) \coloneqq \int_l f\,d\lambda(x),$$
where $l\subset\mathbb{R}^n$ is a line, and $\lambda$ the [[Lebesgue measure]] on the line. 

Define a [[manifold]] $M_n$ by
$$
M_n = \big\{(\sigma, x)\in \mathbb{P}^{n-1}\times\mathbb{R}^n \mid \langle x,\sigma\rangle = 0\big\};
$$
where $\mathbb{P}^{n-1} \coloneqq S^{n-1}/\{\pm\}$ is the [[projective space]] of lines in $\mathbb{R}^n$ that pass through the origin, and $(\sigma,x)$ represents a line that passes through $x$ with direction $\sigma$. 


We endow $M_n$ with a [[measure]] $\mu$ invariant under rigid motions. 

It is an open problem to determine the exponents $1\le p,q,r\le\infty$ for which the following [[inequality]] holds:
$$
  \left\Vert \operatorname{X}f\right\Vert
   _{L^q\big(\sigma\mapsto L^r_x(\mathbb{R}^{n-1})\big)} 
  \;\le\; 
  C\left\Vert f\right\Vert_{L^p(\mathbb{R}^n)}.
$$

For brevity we will write $L^q_\sigma L^r_x \coloneqq L^q\big(\sigma\mapsto L^r_x(\mathbb{R}^{n-1})\big)$.

We can write the X-ray transform of a function $f\in C_c^\infty(\mathbb{R}^n)$ as
$$

  \operatorname{X} f(l) 
   = 
  \int f\delta_{l}(x)\,d
 \,,x
$$
where $\delta_{l} \coloneqq \lim_{\varepsilon\to 0}\varepsilon^{-n+1}1_{\{x\in\mathbb{R}^n\mid \;l\cap B_\varepsilon(x)\neq\emptyset\}}$. 

If $(\sigma,x)$ is a line $l\in M_n$, and $P_\sigma$ the projection to the plane $\{y\mid \langle y,\sigma\rangle = 0\}$ then $\delta_l$ is the [[pullback of a distribution|pullback]] $P_\sigma^*\delta_x = \delta_x\circ P_\sigma$, where $\delta_x$ is the [[Dirac delta distribution]] centered at $x\in\mathbb{R}^{n-1}$.

The operator dual to $\operatorname{X}$, _i.e._ $\int \operatorname{X}h\,f\,d\mu = \int h\,\operatorname{X}^*f\,dx$, acts on functions $f$ in $M_n$ as
$$
\operatorname{X}^*f(x) = \int f\delta_{\{x\}}(l)\,d\mu(l);
$$
here $\delta_{\{x\}} \coloneqq \lim_{\varepsilon\to 0}\varepsilon^{-n+1}1_{\{l\in M_n\mid \;l\cap B_\varepsilon(x)\neq\emptyset\}}$  --- this is a distribution in $M_n$, not to be confused with the usual [[Dirac delta distribution]] $\delta_x$ centered at $x$: The distribution $\delta_{\{x\}}$ is the restriction of the measure $\mu$ in $M_n$ to the set of lines passing through $x\in\mathbb{R}^n$.

The first bound we can get for the X-ray transform is
$$
\int \vert \operatorname{X} f\vert\,d\mu(l) \le \int \operatorname{X}\vert f\vert\,1\,d\mu(l) = \int \vert f\vert\,\operatorname{X}^*1\,dx = \int \vert f\vert\,dx,
$$
since $\operatorname{X}^*1$ is constant. Alternatively, we can use the fact that the integral of $\operatorname{X}\vert f\vert$ along all the lines with the same direction equals $\left\Vert f\right\Vert_1$, which also implies that $\operatorname{X}:L^1(\mathbb{R}^n)\to L^1(M_n)$. Any other bound of the X-ray transform can be interpolated with this bound to get further inequalities.

Besides $L^p$-spaces, we need to consider spaces of regular functions.

+-- {: .num_defn #SobolevSlobodeckij}
###### Definition
**([[Sobolev space]])

Let $\varphi$ be a [[smooth function]] with [[Fourier transform]] [[support of a function|supported]] in $\vert\xi\vert\sim 1$, and let $\tilde{\varphi}$ be a smooth function with [[Fourier transform]] supported in $\vert\xi\vert\lesssim 1$. Suppose that 
$$
1 = \sum_{k\ge 0}\varphi_k,
$$
where $\varphi_0 \coloneqq \tilde{\varphi}$ and $\varphi_k(\xi) \coloneqq \varphi(\xi/2^k)$, for $k\ge 1$. Let $P_k$ be the projection $(P_k f)^\wedge \coloneqq \varphi_k \hat{f}$. 

The Sobolev-Slobodeckij spaces $W^{s,p}(\mathbb{R}^n)$ are, for $1\lt p\lt \infty$ and $-\infty\lt s\lt \infty$, defined as
$$
\Vert f\Vert_{W^{s,p}(\mathbb{R}^n)} := \Big[\sum_{k\ge 0}(2^{sk}\Vert P_k f\Vert_{L^p(\mathbb{R}^n)})^p\Big]^\frac{1}{p}\quad \text{if}\phantom{.} s \notin \mathbb{N},
$$
and
$$
\Vert f\Vert_{W^{s,p}(\mathbb{R}^n)} \coloneqq \Big[\sum_{\vert\alpha\vert\le s}\Vert \partial^\alpha f\Vert_{L^p(\mathbb{R}^n)}^p\Big]^\frac{1}{p} \quad \text{if}\phantom{.} s \in \mathbb{N}.
$$
See ([Triebel 1978, Sec. 2.3.1](#triebel1978)).

=--

The relation between that X-ray transform and the Kakeya set conjecture is the content of the following Theorem:

+-- {: .num_theorem #ThmXRayKakeya}
###### Theorem
**([Bourgain 1991, Lemma 2.15](#bourgain1991))

Let $n - s p\gt 0$. If for every function $f$ such that $supp\,f\subset K$, for $K$ compact, it holds that
$$
\label{eqThmXRayKakeya}
\Vert \operatorname{X} f\Vert_{L^1_\sigma L^\infty_x(M_n)}\le C_K\Vert f\Vert_{W^{s,p}(\mathbb{R}^n)},
$$
then the Hausdorff dimension of a Kakeya set is at least $n- s p$.

=--

+-- {: .proof}
###### Proof

To compute the Hausdorff dimension we can use either balls $B_r(x)$ or dyadic cubes $Q_k :l\coloneqq [l2^k,(l+1)2^k]^n$, for $k$ integer. In fact, we can cover a cube $Q_k$ with a ball of radius $\sqrt{n}2^{k-1}$, and conversely we can cover a ball of radius $r$ with a few cubes $Q_k$, for $2^{k-1}\lt r\le 2^k$. 

Let $E\subset\mathbb{R}^n$ be a Kakeya set. Give any covering $\mathcal{C} = \{Q_k\}$ of $E$ at scale $0\lt\delta\le 1$, i.e. a covering such that for every cube $Q_k\in\mathcal{C}$ its side-length is $2^k\le\delta$, the goal is to show that if $0\le d\lt n - s p$ then
$$
\sum_{Q_k\in\mathcal{C}}l(Q_k)^d \to \infty \quad \text{as}\phantom{.}\delta\to 0,
$$
where $l(Q_k) = 2^k$ is the side-length of the cube.

Let $\mathcal{C}$ be a covering of $E$ at scale $\delta$. We denote by $\mathcal{C}_k$ the collection of all the cubes in $\mathcal{C}$ with side-length $2^k$, and we denote by $A_k$ the union of all the cubes in $\mathcal{C}_k$; therefore,
$$
1_E \le \sum_k 1_{A_k} \coloneqq \sum_k \Big(\sum_{Q_k\in\mathcal{C}_k}1_{Q_k}\Big).
$$ 
Since our hypotheses involve the spaces $W^{s,p}$, we should mollify $1_{A_k}$. We take a suitable smooth function $\varphi$ with compact support,  define the dilations $\varphi_k(x) \colon l\coloneqq 2^{-nk}\varphi(x/2^k)$, and replace $1_{A_k}$ by $\varphi_k*1_{A_k}$. 

Since $E$ contains a unit line segment in every direction $\sigma$, then for every $\sigma\in \mathbb{P}^{n-1}$ it holds that $\Vert \operatorname{X}1_E(\cdot,\sigma)\Vert_{L^\infty} \ge 1$, and then that
$$
1\le \Vert \operatorname{X}1_E\Vert_{L^1_\sigma L^\infty_x}\le C\sum_{2^k\le\delta}\Vert \operatorname{X}\big(\varphi_k*1_{A_k}\big)\Vert_{L^1_\sigma L^\infty_x}.
$$
By (eq:eqThmXRayKakeya) we have that
$$
1
  \;\le\; C\sum_{2^k\le\delta} \Vert \varphi_k*1_{A_k}\Vert_{W^{s,p}}.
$$
In general, the $W^{s,p}$-norm of $\varphi_k*f$ is
$$
\Vert \varphi_k*f\Vert_{W^{s,p}}\le C2^{-ks}\Vert f\Vert_p;
$$
see Lemma \ref{LemmSobolevConv} below. Hence,
$$
1\le C\sum_{2^k\le\delta} \Vert \varphi_k*1_{A_k}\Vert_{W^{s,p}} \le C\sum_{2^k\le\delta}2^{-ks+\frac{nk}{p}}\vert \mathcal{C}_k\vert^\frac{1}{p}
$$
where $\vert \mathcal{C}_k\vert$ denotes the number of cubes in $\mathcal{C}_k$.

By hypothesis $n-s p\gt 0$, then for every $0\le d \lt n-sp$ we can apply Hölder inequality to get
$$
1 \le \Big(\sum_{2^k\le\delta} 2^{p'k(\frac{n-d}{p}-s)}\Big)^\frac{1}{p'}\Big(\sum_k 2^{kd}\vert\mathcal{C}_k\vert\Big)^\frac{1}{p} \le C\delta^\alpha\Big(\sum_{Q_k\in\mathcal{C}}l(Q_k)^d\Big)^\frac{1}{p},
$$
where $\alpha = \frac{n-d}{p}-s\gt 0$. The statement of the Theorem follows. 
=--

+-- {: .num_lemma #LemmSobolevConv}
###### Lemma

If $\psi$ is a smooth function and $\psi_l(x) :l\coloneqq 2^{nl}\psi(2^l x)$, for $l\ge 0$, then
$$
\label{LemmSobolevConv}
\Vert \psi_l*f\Vert_{W^{s,p}(\mathbb{R}^n)}\le C2^{ls}\Vert f\Vert_p,
$$
where $C$ depends on $\psi$.
=--

+-- {: .proof}
###### Proof

If $s$ is an [[integer]], then (eq:LemmSobolevConv) follows from $\partial^\alpha(\psi_l*f) = (\partial^\alpha \psi_l)*f$ and from the [[Young inequality for convolutions]]. 

If $s\neq$ integer, then we have to estimate the norm of $P_k f$; recall that $(P_k f)^\wedge \coloneqq \varphi_k \hat{f}$, where $\varphi_k(\xi) \coloneqq \varphi(\xi/2^k)$. If $k\le l$ then by the [[Young inequality for convolutions]]
$$
\Vert P_k(\psi_l*f)\Vert_p \le \Vert \check{\varphi}_k\Vert_1\Vert \psi_l\Vert_1\Vert f\Vert_p \le C\Vert f\Vert_p.
$$
If $k\gt l$ then fix a number $2N\gt s$. We estimate the norm of $P_k f$ as
$$
\Vert P_k(\psi_l*f)\Vert_p \le \Vert (\vert \xi\vert^{-2N}\varphi_k)^\vee\Vert_1 \Vert \Delta^N(\psi_l*f)\Vert_p.
$$ 
As before we get $\Vert \Delta^N (\psi_l*f)\Vert_p\le C 2^{2 N l}\Vert f\Vert_p$. For the other term, since $(\vert \xi\vert^{-2N}\varphi_k)^\vee(x) = 2^{(n-2 N)k}(\vert \xi\vert^{-2N}\varphi)^\vee(2^k x)$ then we get
$$
\Vert (\vert \xi\vert^{-2N}\varphi_k)^\vee\Vert_1 = 2^{-k2N}\Vert (\vert \xi\vert^{-2N}\varphi)^\vee\Vert_1;
$$
we conclude so that $\Vert P_k(\psi_l*f)\Vert_p \le C2^{2N(l-k)}\Vert f\Vert_p$. Therefore, the $W^{s,p}$-norm of $\psi_l*f$ is 
$$
\begin{aligned}
\Vert \psi_l*f\Vert_{W^{s,p}(\mathbb{R}^n)}^p &\le \sum_{0\le k\le l}2^{p k s}\Vert P_k(\psi_l*f)\Vert_p^p + \sum_{k\gt l}2^{p k s}\Vert P_k(\psi_l*f)\Vert_p^p \\
&\le C\Big(\sum_{0\le k \le l}2^{pks} + 2^{p 2 N l}\sum_{k \gt l}2^{p(s-2N)k}\Big)\Vert f\Vert_p^p \\
&= C2^{p s l}\Vert f\Vert_p^p,
\end{aligned}
$$
which concludes the proof.
=--

For a fixed direction $\sigma$, the X-ray transform maps $f$ to a function $x\mapsto \operatorname{X} f(x,\sigma)$ in $\mathbb{R}^{n-1}$. The function $\operatorname{X} f(\cdot,\sigma)$ turns out to be more regular than $f$. 

+-- {: .num_theorem}
###### Theorem

If $f\in L^2(\mathbb{R}^n)$ has support $supp f\subset K$, for $K$ compact, then
$$
\label{eqThmL2Bound}
\left\Vert \vert \langle D\rangle^\frac{1}{2}\operatorname{X} f\right\Vert_{L^2(M_n)} \le C_K\left\Vert f\right\Vert_{L^2(\mathbb{R}^n)}.
$$

=--

\begin{remark}
The Japanese bracket $\langle\cdot\rangle$ is defined as $\langle \xi\rangle \coloneqq (1+\vert \xi\vert^2)^\frac{1}{2}$, and then $\langle D\rangle^2 = I-\Delta$.
\end{remark}

+-- {: .proof}
###### Proof

We set $g \coloneqq \langle D\rangle^\frac{1}{2} f$, and for a fixed direction $\sigma\in \mathbb{P}^{n-1}$ we compute the Fourier transform of the function $x\in\mathbb{R}^{n-1}\mapsto \operatorname{X}g(x,\sigma)$. By rotational symmetry we can assume that $\sigma = e_n$, so
$$
\operatorname{X}g(x,e_n) = \int g(x,t)\,dt.
$$
The [[Fourier transform]] is $(\operatorname{X}g(\cdot,e_n))^\wedge(\eta) = \hat{g}(\eta,0)$. If $\delta_{\perp\sigma} = \lim_{\varepsilon\to 0}\varepsilon^{-1}1_{\{\xi\mid \vert\langle \xi,\sigma\rangle\vert\le\varepsilon\}}$ is the [[Dirac delta distribution]] of the plane normal to $\sigma$, then we may write
$$
\Vert \operatorname{X}g(\cdot,\sigma)\Vert_{L^2(\mathbb{R}^{n-1})}^2 = \int \vert \hat{g}\vert^2\delta_{\perp\sigma}\,d\xi.
$$
Hence,
$$
\Vert \operatorname{X}g(\cdot,\sigma)\Vert_{L^2(M_n)}^2 = \int\vert \hat{g}\vert^2\Big(\int_{S^{n-1}}\delta_{\perp\sigma}(\xi)\,dS(\sigma)\Big)\,d\xi = \int \langle \xi\rangle\vert\hat{f}\vert^2\frac{d\xi}{\vert \xi\vert}.
$$
For high frequencies we have that
$$
\int_{\vert\xi\vert\ge 1} \langle \xi\rangle\vert\hat{f}\vert^2\frac{d\xi}{\vert \xi\vert} \le C\Vert f\Vert_2^2.
$$
For low frequencies we have that
$$
\int_{\vert\xi\vert\le 1} \langle \xi\rangle\vert\hat{f}\vert^2\frac{d\xi}{\vert \xi\vert} \le C\Vert f\Vert_1^2 \le C_K\Vert f\Vert_2^2.
$$
The statement of the Theorem follows.
=--

The Sobolev embedding Theorem $\Vert h\Vert_{L^\infty(\mathbb{R}^{n-1})}\le C\Vert h\Vert_{W^{s,2}(\mathbb{R}^{n-1})}$, for $s\gt \frac{n-1}{2}$, and the inequality (eq:eqThmL2Bound) allow us to conclude that for every $f$ such that $supp\,f\subset K$, for $K$ compact, it holds that
$$
\Vert \operatorname{X} f\Vert_{L^2_\sigma L^\infty_x}\le C_K \Vert f\Vert_{W^{s,2}(\mathbb{R}^n)},
$$
for $s\gt \frac{n}{2}-1$. Hence, by Theorem \ref{ThmXRayKakeya} the Hausdorff dimension of a Kakeya set $E\subset\mathbb{R}^n$ is at least 2. This result is the best possible in $\mathbb{R}^2$ ([Córdoba 1977](#cordoba1977)), but  far away from the expected dimension for $n\ge 3$.

+-- {: .num_defn #LorentzSpace}
###### Definition
**(Lorentz Spaces)

Let $(X,\nu)$ be a [[measure space]]. The quasinorm of the space $L^{p,q}(\nu)$, for $1\le p\lt\infty$ and $1\le q \lt\infty$, is
$$
\left\Vert f\right\Vert_{p,q} := \Big(p\int_0^\infty s^q\nu\{\vert f\vert\ge s\}^\frac{q}{p}\frac{ds}{s}\Big)^\frac{1}{q},
$$
and, for $1\le p\lt\infty$ and $q=\infty$, is
$$
\left\Vert f\right\Vert_{p,\infty} \coloneqq \sup_{s\gt 0} (s\nu\{\vert f\vert\ge s\}^\frac{1}{p})
$$
=--

+-- {: .num_theorem}
###### Theorem
**([Drury 1983](#drury1983))

If $E\subset \mathbb{R}^n$ is a measurable set, and $1_E$ is the characteristic function of $E$, then
\[
\label{eqThmDrury}
\left\Vert \operatorname{X}(1_E)\right\Vert_{L^{n+1,\infty}(M_n)} \le C\left\vert E\right\vert^\frac{2}{n+1}.
\]

=--

\begin{remark}

This inequality corresponds to the restricted weak version of the point $(p,q,r) = (\frac{n+1}{2}, n+1, n+1)$.
\end{remark}

+-- {: .proof}
###### Proof
 
Let $f = 1_E$ and define the set $F \coloneqq \{l\in M_n\mid \operatorname{X} f(l)\ge\lambda\}$, then 
$$
\label{eqProofDruryLowerBush}
\lambda\vert F\vert \le \int_F \operatorname{X} f\,d\mu = \int f\operatorname{X}^*1_F \,dx \le \left\Vert \operatorname{X}^*1_F\right\Vert_\infty\left\Vert f\right\Vert_1.
$$
This establishes a lower bound for $\left\Vert \operatorname{X}^*1_F\right\Vert_\infty$, and we will get now an upper bound.

Choose a point $x_0$ such that $\operatorname{X}^*1_F(x_0)\ge \frac{1}{2}\left\Vert \operatorname{X}^*1_F\right\Vert_\infty$ ---$x_0$ is the center of _Bourgain's bush_. By translation symmetry we can assume that $x_0 = 0$. If $\delta_0$ is the Dirac delta centered at the origin, then
$$
\label{eqProofDruryLower}
\int 1_F \operatorname{X} f\,\operatorname{X}\delta_0\,d\mu(l) \ge \lambda\int_F \operatorname{X}\delta_0\,d\mu(l)\ge \frac{\lambda}{2}\left\Vert \operatorname{X}^*1_F\right\Vert_\infty.
$$
Here we can think of $\operatorname{X}\delta_0$ as the distribution we defined earlier $\delta_{\{0\}} \coloneqq \lim_{\varepsilon\to 0}\varepsilon^{-n+1}1_{\{l\in M_n\mid \;l\cap B_\varepsilon(0)\neq\emptyset\}}$ supported over the lines passing through the point $0$. We can also justify the notation $\operatorname{X}\delta_0$ by a limiting process since $\delta_0 \coloneqq \lim_{\varepsilon\to 0}\varepsilon^{-n}1_{B_\varepsilon(0)}$.

On the other hand, we can also estimate the left side of (eq:eqProofDruryLower) as
$$
\int 1_F \operatorname{X} f\,\operatorname{X}\delta_0\,d\mu(l) = \int f\operatorname{X}^*(1_F \operatorname{X}\delta_0)\,dx \le  \left\Vert f\right\Vert_{L^{n,1}} \left\Vert \operatorname{X}^*(1_F \operatorname{X}\delta_0)\right\Vert_{L^{\frac{n}{n-1},\infty}},
$$
The function $\operatorname{X}^*(1_F \operatorname{X}\delta_0)$ can be computed explicitly
$$
\operatorname{X}^*(1_F \operatorname{X}\delta_0)(x) = \frac{1}{\vert x\vert^{n-1}}1_F(l(\tilde{x}, 0)),
$$
where $\tilde{x} \coloneqq x/\vert x\vert$ and $l(\tilde{x}, 0)$ is the line that passes through $0$ and $x$. Then, we can estimate the norm of $\operatorname{X}^*(1_F \operatorname{X}\delta_0)$ as
$$
\left\Vert \operatorname{X}^*(1_F \operatorname{X}\delta_0)\right\Vert_{L^{\frac{n}{n-1},\infty}} = c_n\vert \operatorname{X}^*1_F(0)\vert^\frac{n-1}{n}\le c_n\left\Vert \operatorname{X}^*1_F\right\Vert_\infty^\frac{n-1}{n}.
$$
Then we get the bound
$$
\label{eqProofDruryUpper}
\int 1_F \operatorname{X} f\,\operatorname{X}\delta_0\,d\mu(l) \le c_n \left\Vert f\right\Vert_{L^{n,1}}\left\Vert \operatorname{X}^*1_F\right\Vert_\infty^\frac{n-1}{n}.
$$
By (eq:eqProofDruryLower) and (eq:eqProofDruryUpper) we get the desired upper bound for $\left\Vert \operatorname{X}^*1_F\right\Vert_\infty$:
$$
c_n\lambda \left\Vert \operatorname{X}^*1_F\right\Vert_\infty^\frac{1}{n} \lesssim \left\Vert f\right\Vert_{L^{n,1}}.
$$
This and (eq:eqProofDruryLowerBush) allow us to conclude that
$$
\vert F\vert \lesssim \frac{1}{\lambda^{n+1}}\left\Vert f\right\Vert_1\left\Vert f\right\Vert_{L^{n,1}}^n = \frac{1}{\lambda^{n+1}}\vert E\vert^2,
$$
which implies the restricted weak inequality (eq:eqThmDrury).

=--

Drury's Theorem and the bound $L^1\to L^1$ imply that
$$
\Vert \operatorname{X} f\Vert_{L^q(M_n)}\le C\Vert f\Vert_{L^p(\mathbb{R}^n)},
$$
for $1\le p\lt \frac{n+1}{2}$ and $\frac{n-1}{q}+1 = \frac{n}{p}$. By Sobolev embedding Theorem $\Vert h\Vert_{L^\infty(\mathbb{R}^{n-1})} \le \Vert h\Vert_{W^{s,q}(\mathbb{R}^{n-1})}$, for $s\gt \frac{n-1}{q}$, we get further 
$$
\Vert \operatorname{X} f\Vert_{L^q_\sigma L^\infty_x(M_n)}\le C\Vert f\Vert_{W^{s,p}(\mathbb{R}^n)},
$$
for $1\le p\lt \frac{n+1}{2}$, $\frac{n-1}{q}+1 = \frac{n}{p}$ and $s\gt \frac{n}{p}-1$. Hence, by Theorem \ref{ThmXRayKakeya} the Hausdorff dimension of a Kakeya set $E\subset\mathbb{R}^n$ is at least $\frac{n+1}{2}$.



## References

* {#cordoba1977} A. Córdoba: *The Kakeya Maximal Function and the Spherical Summation Multipliers*, Amer. J. Math. **99** (1977)

* M. Christ: *Estimates for the $k$-plane transform*, Indiana Univ. Math. J. **33** (1984)

* {#drury1983} S. W. Drury,l: *$L^p$ estimates for the X-ray transform*, Illinois J. Math. **27** (1983)

* {#triebel1978} H. Triebel: *Interpolation Theory, Function Spaces, Differential Operators*, North-Holland (1978)

* {#bourgain1991} J. Bourgain: *Besicovitch type maximal function operators and applications to Fourier Analysis*, Geom. Funct. Anal. **1** (1991)

See also:

* Wikipedia: *[Kakeya set](https://en.m.wikipedia.org/wiki/Kakeya_set)

* [[Victor Porton]]: [proof](https://www.researchgate.net/publication/389600840_Proof_of_Kakeya's_Conjecture) in arbitrary dimensions