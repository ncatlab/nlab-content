[[!redirects Dirac electron]]
The purpose of this page is to explain - using appropriate mathematical terminology - Dirac's theory of coupling particles with spin to a gauge field. 

Useful literature on this topic is:

* D. Bleecker, _Gauge Theory and Variational Principles_, Addison-Weasley, 1981.

* H. Blaine Lawson Jr. , Marie-Louise Michelson, _Spin geometry_, Princeton Univ. Press, 1989.

* G. L. Naber, _Topology, Geometry and Gauge Dields_, Springer, 1999.

We proceed in three steps: first we recall relevant facts about the gauge field itself, then we discuss charged particles in gauge fields, and finally we add spin. 

### Yang-Mills Theory ###

(see: the main article about [Yang-Mills Theory](http://ncatlab.org/nlab/show/Yang-Mills+theory))

Under a _spacetime_ we understand a smooth, oriented, Pseudo-Riemannian manifold. 

**Definition. **
A _Yang-Mills Theory_ over a space time $M$ is:

* A Lie group $G$, called the _gauge group_, together with an $\mathrm{Ad}$-invariant scalar product $\kappa: \mathfrak{g} \times \mathfrak{g} \to \R$ on its Lie algebra $\mathfrak{g}$.

* A principal $G$-bundle $P$ over $M$.

A _gauge field_ is a connection $\omega \in \Omega^1(P,\mathfrak{g})$ on $P$. The action functional is 

$$
S_{YM}(\omega) := \frac{1}{2} \int_M \| F_{\omega} \|_\kappa^2.
$$


**Remark. **
Above we have used the following notation:

* $F_{\omega} \in \Omega^2(M,\mathrm{Ad}(P))$ is the curvature of $\omega$.

* $\mathrm{Ad}(P) := P \times_{\mathrm{Ad}} \mathfrak{g}$ is the adjoint bundle.

* $\| \psi \|_{\kappa}^2 := \psi \wedge_{\kappa} \star \psi   \in \Omega^n(M)$. In general, if $U,V,W$ are vector spaces, $\varphi \in \Omega^p(M,V)$, $\psi\in\Omega^q(M,W)$ and $f: V \times W \to U$ is a linear map, we have $\varphi \wedge_{f} \psi \in \Omega^{p+q}(M,U)$. 


**Remark. **
The Euler-Lagrange equations determined by the above action together with the Bianchi identity are called _Yang-Mills equations_:
$$
\mathrm{D}^{\omega}\star F_{\omega} = 0
\quad\text{ and }\quad
\mathrm{D}^{\omega}F_{\omega}=0,
$$
where $\mathrm{D}^\omega$ denotes the [covariant derivative](http://ncatlab.org/nlab/show/exterior+covariant+derivative).


**Definition.**
A _gauge transformation_ is a smooth bundle morphism $g: P \to P$.


**Remark.**
Let $g: P \to P$ be a gauge transformation.

* If $\omega$ is a connection on $P$, then $g^{*}\omega$ is another connection on $P$. 

* One can identify $g$ with a smooth map $\tilde g: P \to G$, namely by $g=r_{\tilde g}$, i.e. $g(p) = p \cdot \tilde g(p)$ for all $p\in P$. 

* The pullback along a gauge transformation restricts to an automorphism of $\Omega^k_{\rho}(P,V)$. In terms of the associated map $\tilde g$, we have
$$
g^{*}\psi = \rho(\tilde g^{-1},\psi)\text{.}
$$

**Theorem. **
The Yang-Mills action functional $S_{YM}$ is gauge-invariant, i.e. 
$$
S_{YM}(g^{*}\omega) = S_{YM}(\omega)
$$
for all gauge transformations $g:P \to P$.


Proof. 
We have $g^{*}\omega  = \mathrm{Ad}_{\tilde g}^{-1}(\omega) - \tilde g^{*}\bar\theta$ and $g^{*}\Omega = \mathrm{Ad}_{\tilde g}^{-1}(\Omega)$.
Under the isomorphism $\Omega^k(P,\mathrm{Ad}) \cong \Omega^2(M,\mathrm{Ad}(P))$ this corresponds to $F_{g^{*}\omega} = \mathrm{Ad}_{g} (F_{\omega})$. Since the bilinear form $\kappa$ is $\mathrm{Ad}$-invariant by assumption, 
$$
\| F_{g^{*}\omega} \| 
= \mathrm{Ad}_{g} (F_{\omega}) \wedge_{\kappa} \mathrm{Ad}_{g} (F_{\omega}) 
= F_{\omega} \wedge_{\kappa} F_{\omega} 
= \| F_{\omega}\|. 
$$

**Example. **
Let $M$ be a spacetime. A classical electromagnetic field theory over $M$ is a Yang-Mills Theory over $M$ with gauge group $G=U(1)$. Also see the main article about [electromagnetic fields](http://ncatlab.org/nlab/show/electromagnetic+field). In more detail: 

* for an electromagnetic field theory given by a $U(1)$-bundle $P$ over $M$, we have $\mathrm{Ad}(P) \cong P \times \R$, so that $\Omega^k(M,\mathrm{Ad}(P)) \cong \Omega^k(M)$ and $\Omega^k_{\mathrm{Ad}}(P,\mathfrak{g})\cong \Omega^k_{\mathrm{Ad}}(P)$. In particular, $F_{\omega} \in \Omega^2(M)$. 

* Since $U(1)$ is abelian, $\mathrm{d}(\mathrm{Ad}) = 0$ and so $\mathrm{D}^{\omega}=\mathrm{d}$ on $\Omega^{k}_{\mathrm{Ad}}(P)$.
  
* Thus, the Yang-Mills equations reduce to  Maxwell's equations for an electromagnetic field on $M$:
$$
\mathrm{d}\star F_{\omega} = 0
\quad\text{ and }\quad
\mathrm{d}F_{\omega}=0
\text{.}
$$


### General Matter Fields ###

**Definition. **
Let $G$ be a gauge group. A _matter type for  $G$_ is a tuple $(V,h,\rho,f)$ consisting of:

* a finite-dimensional real vector space $V$ called the _internal state space_.

* a scalar product $h: V \times V \to \R$.

* a representation $\rho: G \times V \to V$ that is isometric with respect to $h$ i.e. $h(\rho(g)(v),\rho(g)(w)) = h(v,w)$.

* a smooth function $f: V \to \R$ that is $\rho$-invariant, i.e. $f(\rho(g)(v))=f(v)$.


**Definition. **
Let $P$ be a principal $G$-bundle over $M$, and let $\mathcal{T} =(V,h,\rho,f)$ be a matter type for $G$. A _field for $P$ of type $\mathcal{T}$_ is a smooth section $\phi: M \to P \times_{\rho} V$. Its  action functional is
$$
S_{\mathcal{T}}(\omega,\phi) := \int_M  \;\|\, \mathrm{D}^{\omega}(\phi)\, \|^2_{h}  +  \star (f \circ \phi) \text{.}
$$

**Theorem. **
The action functional $S_{\mathcal{T}}$ is gauge invariant, i.e. 
$$
S_{\mathcal{T}}(g^{*}\omega,g^{*}\phi) = S_{\mathcal{T}}(\omega,\phi)
$$
for all gauge transformations $g:P \to P$.


Proof. One calculates that $g^{*}\omega = \mathrm{Ad}_{\tilde g}^{-1}(\omega) - \tilde g^{*}\bar\theta$, where $\tilde g:P \to G$ is the smooth map associated to $g$ via $g(p) = p\cdot  \tilde g(p)$. Further, $g^{*}\psi = \rho(\tilde g^{-1})(\psi)$. A computation shows
$$
\mathrm{d}(\rho(\tilde g^{-1})(\psi)) = \rho(\tilde g^{-1})(\mathrm{d}\psi) + \tilde g^{*}\bar\theta\wedge_{\mathrm{d}\rho} \rho(\tilde g^{-1})(\psi)\text{,}
$$
where $\mathrm{d}\rho: \mathfrak{g} \otimes V \to V$. 
Now we compute
$$
\mathrm{d}^{g^{*}\omega}(g^{*}\psi) 
= \mathrm{d}\rho(\tilde g^{-1})(\psi) + g^{*}\omega \wedge_{\mathrm{d}\rho} \rho(\tilde g^{-1})(\psi)
$$
$$
= \rho(\tilde g^{-1})(\mathrm{d}\psi) + \tilde g^{*}\bar\theta\wedge_{\mathrm{d}\rho} \rho(\tilde g^{-1})(\psi) + (\mathrm{Ad}_{\tilde g}^{-1}(\omega) - \tilde g^{*}\bar\theta) \wedge_{\mathrm{d}\rho} \rho(\tilde g^{-1})(\psi)
$$
= \rho(\tilde g^{-1})(\mathrm{d}\psi)  + \rho(\tilde g^{-1})(\omega\wedge_{\mathrm{d}\rho} \psi) 
$$
= \rho(\tilde g^{-1})(\mathrm{d}^{\omega}\psi)\text{.}
$$
Since $h$ is invariant, the invariance of the first term follows. The invariance of the second term is clear.

**Remark. **
One can either keep a connection $\omega$ fixed and consider
$$
S_{\omega}(\phi) := S_{\mathcal{T}}(\omega,\phi)
$$
as a matter field in an "external gauge field", or consider the combined action functional
$$
S(\omega,\phi) := S_{Y\!M}(\omega) + S_{\mathcal{T}}(\omega,\phi)\text{.}
$$


**Example ** (Scalar particle in an external, trivial gauge field)
We consider $G=\left \lbrace e \right \rbrace$, $P=M$, so that necessarily $\omega=0$. A _scalar field_ is field for $M$ of matter type $(\R,h,\id,f)$ where $f(x) := -\frac{1}{2}m^2x^2$ and $h(x,y) = x y$. The action functional is
$$
S(0,\phi) =\frac{1}{2} \int_M  \| \mathrm{d}\phi \|_h^2 +\star m^{2}\phi^2\text{.}
$$
The Euler-Lagrange equation is the _Klein-Gordon equation_
$$
(\triangle + m^2)\phi = 0\text{,}
$$
where $\triangle := \delta \circ \mathrm{d}: \Omega^k(M) \to \Omega^{k}(M)$ is the Laplace operator and  and $\delta := \star \mathrm{d} \star$ is the exterior coderivative. 


**Example ** (Charged particle in an  electromagnetic field, e.g. a $\pi^{-}$-meson)
Let $P$ be a $U(1)$-principal bundle over $M$. A _field of charge $n \in \Z$_ is a field for $P$ of matter type $(\C,h,\rho_n,f)$, where $\rho_n: U(1) \times \C \to \C$ is defined by $\rho_n(z,z') := z^nz'$  and $f(z) := -\frac{1}{2}m^2|z|^2$. The action functional is
$$
S(\omega,\phi) =\frac{1}{2} \int_M  \| \mathrm{D}^{\omega}\phi \|^2 +\star m^{2} \| \phi \| ^2\text{.}
$$
The Euler-Lagrange equation is
$$
(\triangle^{\omega} +m^2) \phi = 0\text{,}
$$
where $\triangle^{\omega} :=\delta^{\omega}\circ \mathrm{D}^{\omega}$ is the _covariant Laplace operator_ and $\delta^{\omega} := \star \mathrm{D}^{\omega} \star$ is the _exterior covariant coderivative_. 


### Matter Fields with Spin ###

The Klein-Gordon equations found above are -- unlike the Schr&#246;dinger equation -- of second order on time. Dirac's motivation was to find a first order equation which upon iteration yields the Klein-Gordon equation. 
We first discuss free spinors (where free means that there are not coupled to an electromagntic field, but still feel the "gravity" of the manifold), and then add the coupling.

#### Free Spinors ####

**Remark.** We recall some facts about Clifford algebras and the spin group. Also see the main article about [clifford algebras](http://ncatlab.org/nlab/show/Clifford+algebra). 

* We denote by $C(p,q)$ the Clifford algebra on $\R^{p,q}$, i.e. the quotient of the tensor algebra of $\R^{p+q}$ by the ideal generated by $v \otimes w + w \otimes v + 2 \left \langle v,w  \right \rangle\cdot 1$, where $\left \langle -,-  \right \rangle$ is the Minkowski scalar product of signature $(p,q)$. 

* The map $v \mapsto -v$ extends to an anti-automorphism $\alpha: C(p,q) \to C(p,q)$, whose eigenspace decomposition yields the usual $\Z_2$-grading on $C(p,q)$. 

* We have $\dim C(p,q) = 2^{p+q}$.

* The Clifford algebra inherits a bilinear form $H(v,w) := (v^{tr}w)_0$, where $()^{tr}$ is the anti-automorphism of the tensor algebra that reverts the order of tensor products, and $()_0$ denotes the degree 0 part.

* We denote by $SO(p,q)$ the group of linear maps $\R^{p+q}\to \R^{p+q}$ that preserve the product $\left \langle -,-  \right \rangle$. 
We define
$$
Spin(p,q) := \left \lbrace v_{1}\cdot ... \cdot v_{2r}\in C(p,q)\mid v_i \in \R^{p+q}, \| v_i \|=1,r \in \N \right \rbrace \text{.}
$$
Then, we define a group homomorphism
$\Lambda: Spin(p,q) \to SO(p,q)$
by $\Lambda(\varphi)v = \alpha(\varphi) v \varphi^{-1}$. This gives a central extension
$$
1 \to \Z_2 \to Spin(p,q) \to SO(p,q) \to 1\text{.}
$$

* We denote by $\C(p,q) := C(p,q) \otimes_{\R} \C$ the complexification of the Clifford  algebra. The bilinear form $H$ on $C(p,q)$ extends to a sesquilinear form $H$ on $\C(p,q)$ defined by $H(v,w)=(v^{tr}\bar w)_0$. 

* Multiplication in $\C(p,q)$ restricts to an action of $\spin{p,q}$ on $\C(p,q)$. One can decompose $\C(p,q)$ into $k$ copies of a subrepresentation $\Sigma$:
$$
\C(p,q) = \Sigma \oplus ... \oplus  \Sigma \text{.}
$$

* The representation $\Sigma$ is isometric with respect to $H$. 
If $p+q$ is odd, $k=2^{(p+q-1)/2}$, and $\Sigma$ is irreducible. If $p+q$ is even, $k=2^{(p+q)/2}$, and $\Sigma = \Sigma^{+} \oplus \Sigma^{-}$ with $\Sigma^{\pm}$ irreducible and  $\dim_{\C}\Sigma^{\pm}=2^{(p+q-2)/2}$. 

**Remark. ** We also need some facts about spin structures. Also see the main article about [spin structures](http://ncatlab.org/nlab/show/spin+structure).

* Let $M$ be a spacetime with pseudo-Riemannian metric of signature $(p,q)$. We denote by $FM$ be the principal $SO(p,q)$-bundle over $M$ of orthonormal frames, the _frame bundle_. 

* A _spin structure_ on $M$ is a principal $Spin(p,q)$-bundle $SM$ over $M$ together with a bundle morphism $\lambda: SM \to FM$ such that $\lambda(X\cdot\varphi) = \lambda(X)\cdot\Lambda(\varphi)$ for all $X\in SM$ and all $\varphi\in Spin(p,q)$. 

* Let $\theta \in \Omega^1(FM,\mathfrak{so}(p,q))$ be the Levi-Cevita connection on $FM$. Then, 
$$
\Theta := \mathrm{d}\Lambda^{-1}(\lambda^{*}\theta) \in \Omega^1(SM,\mathfrak{spin}(p,q))
$$
is a connection on $SM$. 


**Remark. ** 
Finally, we recall the definition of the Dirac operator. 

* Let $\rho: C(p,q) \times V \to V$ be a representation, with $V \subset \C(p,q)$. Note that in the above realization of the group $Spin(p,q)$, the representation $\rho$ restricts to a representation of $Spin(p,q)$.
The _spinor bundle_ is the vector bundle $V M := SM \times_{\rho} V$. 

* _Clifford multiplication_ is a map
$$
TM \otimes V M \to V M: u \otimes s \mapsto u \cdot s\text{.}
$$
It is defined as follows. We write $s=(X,v)$ with $X\in SM$ and $v\in V$. We consider the orthonormal frame $\alpha_X := \lambda(X): TM \to \R^n$. Then, $\alpha_X(u) \in \C(p,q)$ and 
$$
u \cdot s := (X,\alpha_X(u)\cdot v)\text{.}
$$
One can show using above-listed properties of the Clifford algebra that this definition does not depend on the choice of the representative $(X,v)$.

* The _Dirac operator_ is
$$
D: \Gamma(M,V M) \to \Gamma(M,V M) : \psi \mapsto \sum_{i} e_i \cdot  \mathrm{D}^{\Theta}\psi (e_i)
$$
where $e_i\in TM$ runs over a local orthonormal basis.




I'll continue tomorrow...