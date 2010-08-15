[[!redirects Exterior Covariant Derivative]]
We require:

* A smooth manifold $M$.

* A Lie group $G$ with Lie algebra $\mathfrak{g}$.

* A principal $G$-bundle $P$ over $M$.

* A finite-dimensional representation $\rho: G \to V \times V$. 

**Definition 1.**
A form $\psi \in \Omega^k(P,V)$ is called:

* _horizontal_, if $\psi_q(v_1,...,v_k)=0$ whenever one of the vectors $v_i$ is vertical. 

* _equivariant_, if $r_g^{*}\psi = \rho(g^{-1},\psi)$ for all $g\in G$, where $r_g: P \to P$ denotes the right action of $G$ on $P$.


We denote by $\Omega^k_{\rho}(P,V)$ the space of horizontal and equivariant forms. Note that $\Omega_{\rho}^k(P,V)$ is in general not closed under the ordinary exterior derivative. There is a canonical isomorphism
$$
\Omega^k_{\rho}(P,V) \cong \Omega^k(M,P \times_{\rho}V),
$$
where $P \times_{\rho}V$ is the vector bundle associated to $P$ via the representation $\rho$.

**Definition 2.**
Let $\omega \in \Omega^1(P,\mathfrak{g})$ be a connection on $P$. The _exterior covariant derivative for forms on $P$_
$$
\mathrm{d}^{\omega}: \Omega^k(P,V) \to \Omega^{k+1}(P,V)
$$
is defined by
$$
(\mathrm{d}^{\omega}\psi)_q(v_1,...,v_k) := (\mathrm{d}\varphi)_q(Hv_1,...,Hv_k)\text{,}
$$
where $H: TP \to TP$ denotes the projection to the horizontal subspace defined by $\omega$. 

Some facts are:

* Every form in the image of $\mathrm{d}^{\omega}$ is horizontal. If a form $\psi$ is equivariant, $\mathrm{d}^{\omega}$ is also equivariant. 

* The restriction of $\mathrm{d}^{\omega}$ to $\Omega^k_{\rho}(P,V)$ can be described in terms of the connection 1-form $\omega\in \Omega^1(P,\mathfrak{g})$ and the derivative $\mathrm{d}\rho: \mathfrak{g} \times V \to V$ of the representation $\rho$:
$$
\mathrm{d}^{\omega}(\psi) = \mathrm{d}\psi + \omega \wedge_{\mathrm{d}\rho} \psi\text{.}
$$
Here we have used the following general notation: if $U,V,W$ are vector spaces, $\varphi \in \Omega^p(M,V)$, $\psi\in\Omega^q(M,W)$ and $f: V \times W \to U$ is a linear map, we have $\varphi \wedge_{f} \psi \in \Omega^{p+q}(M,U)$. 


* The previous fact can be used to show
$$
\mathrm{d}^{\omega}(\mathrm{d}^{\omega}(\psi)) = \Omega \wedge_{\mathrm{d}\rho} \psi\text{,}
$$
in particular, $\mathrm{d}^{\omega} \circ \mathrm{d}^{\omega} = 0$ if $\omega$ is flat. 


**Definition 3.**
The _exterior covariant derivative for forms on $M$_ 
$$
\mathrm{D}^{\omega}: \Omega^k(M,P \times_{\rho} V) \to \Omega^{k+1}(M,P \times_{\rho}V)
$$
is the map induced from $\mathrm{d}^\omega$ under the isomorphism
$\Omega^k_{\rho}(P,V) \cong \Omega^k(M,P \times_{\rho}V)$.


**Examples.**

* The connection $\omega$ itself is not in $\Omega_{\mathrm{Ad}}^1(P,\mathfrak{g})$: it is not horizontal.

* The curvature of $\omega$ is $\Omega := \mathrm{d}^\omega(\omega)\in \Omega^2_{\mathrm{Ad}}(P,\mathfrak{g})$. Since $\mathrm{d}(\mathrm{Ad})=[-,-]$, we have
$$
\Omega = \mathrm{d}\omega + [\omega \wedge \omega]\text{.}
$$
The Bianchi identity is $\mathrm{d}^{\omega}\Omega=0$. 

Under the isomorphism $\Omega^k_{\rho}(P,V) \cong \Omega^k(M,P \times_{\rho}V)$, the curvature $\Omega$ corresponds to a 2-form $F_{\omega} \in \Omega^2(M,\mathrm{Ad}(P))$, and the Bianchi-identity corresponds to $\mathrm{D}^{\omega}F_{\omega} = 0$. 


[[!redirects exterior covariant derivative]]
