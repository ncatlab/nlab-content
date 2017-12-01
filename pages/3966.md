


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The combination of an [[exterior derivative]] with a [[covariant derivative]].

## Definition

### Definition on vector bundles
Let $p: E \to M$ be a [[vector bundle]] with a linear [[connection on a bundle|connection]] given by the [[covariant derivative]] $\nabla: \Gamma(T M) \times \Gamma(E) \to \Gamma(E)$. We let $\Omega(M, E)$ be the space of all [[differential form#twisted|differential forms with values in]] $E$. To define the exterior covariant derivative, we take the explicit formula of the [[exterior derivative]], and replace the usual [[derivative]] with the convariant derivative.

+-- {: .num_defn #DerivVect}
###### Definition
The **exterior covariant derivative** $d_\nabla: \Omega^p (M, E) \to \Omega^{p + 1}(M, E)$ is defined by the following formula: given a $p$-form $\Phi \in \Omega^p (M, E)$, its exterior covariant derivative is given by
$$
\begin{aligned}
(\mathrm{d}_\nabla \Phi)(X_0, \dots, X_p) =& \displaystyle\sum_{i = 0}^p (-1)^i \nabla_{X_i}\Phi (X_0, \dots, \hat{X_i}, \dots, X_p) \\
&+ \displaystyle\sum_{i \lt j} (-1)^{i + j} \Phi([X_i, X_j], X_0, \dots, \hat{X_i}, \dots, \hat{X_j}, \dots, X_p),
\end{aligned}
$$
where each $X_i$ is a [[vector field]] on $M$, and $\hat{X}$ means omission of $X$.
=--

In the case of the trivial bundle with the trivial connection, this gives the usual exterior derivative of a vector-valued differential form.

### Definition on principal $G$-bundles

Let $p: P \to M$ be a [[principal bundle|principal]] $G$-[[bundle]]. Let $\omega \in \Omega^1(P,\mathfrak{g})$ be a [[principal connection|connection]] on $P$. Let $H: T P \to T P$ be the horizontal projection given by $\omega$.

We let $V$ be a vector space, and $\rho: G \to \GL(V)$ be a [[representation]] of $G$ on $V$.

+-- {: .num_defn}
###### Definition
A [[differential form]] $\psi \in \Omega^k(P,V)$ is called:

* **horizontal**, if $\psi_q(v_1,\dots,v_k)=0$ whenever one of the vectors $v_i$ is [[vertical vector field|vertical]]. 

* **equivariant**, if $r_g^{*}\psi = \rho(g^{-1},\psi)$ for all $g\in G$, where $r_g: P \to P$ denotes the right action of $G$ on $P$.
=--

We denote by $\Omega^k_{\rho}(P,V)$ the space of horizontal and equivariant forms. Note that $\Omega_{\rho}(P,V)$ is in general not closed under the ordinary [[exterior derivative]]. There is a canonical isomorphism
$$
\Omega^k_{\rho}(P,V) \cong \Omega^k(M,P \times_{\rho}V),
$$
where $P \times_{\rho}V$ is the vector bundle [[associated bundle|associated]] to $P$ via the representation $\rho$.

+-- {: .num_defn}
###### Definition
 The **exterior covariant derivative** for forms on $P$
$$
\mathrm{d}_{\omega}: \Omega^k(P,V) \to \Omega^{k+1}(P,V)
$$
is defined by
$$
(\mathrm{d}_{\omega}\psi)_q(v_1,\dots,v_k) := (\mathrm{d}\varphi)_q(H v_1,\dots,H v_k).
$$
=--

+-- {: .num_prop}
###### Proposition
Every form in the image of $\mathrm{d}_{\omega}$ is horizontal. If a form $\psi$ is equivariant, $\mathrm{d}_{\omega} \psi$ is also equivariant.
=--

+-- {: .num_prop}
###### Proposition
The [[restriction]] of $\mathrm{d}_{\omega}$ to $\Omega^k_{\rho}(P,V)$ can be described in terms of the connection 1-form $\omega\in \Omega^1(P,\mathfrak{g})$ and the derivative $\mathrm{d}\rho: \mathfrak{g} \times V \to V$ of the representation $\rho$:
$$
\mathrm{d}_{\omega}(\psi) = \mathrm{d}\psi + \omega \wedge_{\mathrm{d}\rho} \psi\text{.}
$$
Here we have used the following general notation: if $U,V,W$ are vector spaces, $\varphi \in \Omega^p(M,V)$, $\psi\in\Omega^q(M,W)$ and $f: V \times W \to U$ is a linear map, we have $\varphi \wedge_{f} \psi \in \Omega^{p+q}(M,U)$. 
=--

+-- {: .num_prop}
###### Proposition
Unlike the usual [[exterior derivative]], the exterior covariant derivative need not be [[nilpotent]] in general. Instead, we have
$$
\mathrm{d}_{\omega}(\mathrm{d}_{\omega}(\psi)) = \Omega \wedge_{\mathrm{d}\rho} \psi.
$$
In particular, $\mathrm{d}_{\omega} \circ \mathrm{d}_{\omega} = 0$ if $\omega$ is flat. 
=--

+-- {: .num_defn}
###### Definition
The **exterior covariant derivative for forms on $M$**
$$
\mathrm{D}_{\omega}: \Omega^k(M,P \times_{\rho} V) \to \Omega^{k+1}(M,P \times_{\rho}V)
$$
is the map induced from $\mathrm{d}_\omega$ under the isomorphism
$\Omega^k_{\rho}(P,V) \cong \Omega^k(M,P \times_{\rho}V)$.
=--
Note that a connection on the principal bundle $p: P \to M$ [[induced connection|induces]] a connection on the [[associated bundle|associated vector bundle]] $P \times_\rho V$. Then the exterior covariant derivative in the sense of Definition \ref{DerivVect} coincides with this exterior covariant derivative.

+-- {: .num_example}
###### Example
$ $

* The [[connection on a bundle|connection]] $\omega$ itself is not in $\Omega_{\mathrm{Ad}}^1(P,\mathfrak{g})$: it is not horizontal.

* The [[curvature#curvature_of_a_connection|curvature]] of $\omega$ is $\Omega := \mathrm{d}_\omega(\omega)\in \Omega^2_{\mathrm{Ad}}(P,\mathfrak{g})$. Since $\mathrm{d}(\mathrm{Ad})=[-,-]$, we have
$$
\Omega = \mathrm{d}\omega + [\omega \wedge \omega]\text{.}
$$
The [[Bianchi identity]] is $\mathrm{d}_{\omega}\Omega=0$. 

Under the isomorphism $\Omega^k_{\rho}(P,V) \cong \Omega^k(M,P \times_{\rho}V)$, the curvature $\Omega$ corresponds to a 2-form $F_{\omega} \in \Omega^2(M,\mathrm{Ad}(P))$, and the [[Bianchi identity]] corresponds to $\mathrm{D}_{\omega}F_{\omega} = 0$. 
=--

## Applications

* In [[Yang-Mills theory]]...

## Related Concepts

* [[differential form]]

* [[connection on a bundle]]

* [[covariant derivative]]

* [[Yang-Mills theory]]

[[!redirects covariant exterior derivative]]
[[!redirects exterior covariant derivative]]
[[!redirects Exterior covariant derivative]]
[[!redirects Exterior Covariant Derivative]]