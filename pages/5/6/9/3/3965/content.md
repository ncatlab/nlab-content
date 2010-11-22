
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The purpose of this page is to explain - using appropriate mathematical terminology - Dirac's theory of coupling particles with spin to a [[Yang-Mills field|Yang-Mills]] [[gauge field]]. 

We proceed in three steps: first we recall relevant facts about the gauge field itself, then we discuss charged particles in gauge fields, and finally we add spin. 


## Yang-Mills Theory 

(see: the main article about [[Yang-Mills theory]])

Under a _[[spacetime]]_ we understand a [[smooth manifold|smooth]], oriented, [[pseudo-Riemannian manifold]]. 

+-- {: .un_def}
###### Definition

A **[[Yang-Mills theory]]** over a [[spacetime]] $M$ is:

* A [[Lie group]] $G$, called the _gauge group_, together with an $\mathrm{Ad}$-invariant scalar product $\kappa: \mathfrak{g} \times \mathfrak{g} \to \R$ on its [[Lie algebra]] $\mathfrak{g}$.

* A $G$-[[principal bundle]] $P$ over $M$.

A _gauge field_ is a [[connection on a bundle|connection]] $\omega \in \Omega^1(P,\mathfrak{g})$ on $P$. The [[action functional]] is 

$$
S_{YM}(\omega) := \frac{1}{2} \int_M \| F_{\omega} \|_\kappa^2.
$$

=--



+-- {: .un_remark}
###### Remark

Above we have used the following notation:

* $F_{\omega} \in \Omega^2(M,\mathrm{Ad}(P))$ is the curvature of $\omega$.

* $\mathrm{Ad}(P) := P \times_{\mathrm{Ad}} \mathfrak{g}$ is the 
  [[adjoint bundle]].

* $\| \psi \|_{\kappa}^2 := \psi \wedge_{\kappa} \star \psi   \in \Omega^n(M)$. In general, if $U,V,W$ are vector spaces, $\varphi \in \Omega^p(M,V)$, $\psi\in\Omega^q(M,W)$ and $f: V \times W \to U$ is a linear map, we have $\varphi \wedge_{f} \psi \in \Omega^{p+q}(M,U)$. 

* $\star$ is the [[Hodge-star operator]] determined by the [[metric]] on $M$.

=--


+-- {: .un_remark}
###### Remark

The [[Euler-Lagrange equation]]s determined by the above action together with the [[Bianchi identity]] are called _[[Yang-Mills equations]]_:

$$
\mathrm{D}^{\omega}\star F_{\omega} = 0
\quad\text{ and }\quad
\mathrm{D}^{\omega}F_{\omega}=0,
$$

where $\mathrm{D}^\omega$ denotes the [[exterior covariant derivative|covariant derivative]].

=--


+-- {: .un_definition}
###### Definition

A _gauge transformation_ is a smooth [[bundle]] morphism $g: P \to P$.

=--


+-- {: .un_remark}
###### Remark

Let $g: P \to P$ be a gauge transformation.

* If $\omega$ is a connection on $P$, then $g^{*}\omega$ is another connection on $P$. 

* One can identify $g$ with a smooth map $\tilde g: P \to G$, namely by $g=r_{\tilde g}$, i.e. $g(p) = p \cdot \tilde g(p)$ for all $p\in P$. 

* The pullback along a gauge transformation restricts to an [[automorphism]] of $\Omega^k_{\rho}(P,V)$. In terms of the associated map $\tilde g$, we have
$$
g^{*}\psi = \rho(\tilde g^{-1},\psi)\text{.}
$$

=--


+-- {: .un_theorem}
###### Theorem

The Yang-Mills action functional $S_{YM}$ is gauge-invariant, i.e. 
$$
S_{YM}(g^{*}\omega) = S_{YM}(\omega)
$$
for all gauge transformations $g:P \to P$.


=--

+-- {: .proof}
###### Proof

We have $g^{*}\omega  = \mathrm{Ad}_{\tilde g}^{-1}(\omega) - \tilde g^{*}\bar\theta$ and $g^{*}\Omega = \mathrm{Ad}_{\tilde g}^{-1}(\Omega)$.
Under the isomorphism $\Omega^k(P,\mathrm{Ad}) \cong \Omega^2(M,\mathrm{Ad}(P))$ this corresponds to $F_{g^{*}\omega} = \mathrm{Ad}_{g} (F_{\omega})$. Since the bilinear form $\kappa$ is $\mathrm{Ad}$-invariant by assumption, 
$$
\| F_{g^{*}\omega} \| 
= \mathrm{Ad}_{g} (F_{\omega}) \wedge_{\kappa} \mathrm{Ad}_{g} (F_{\omega}) 
= F_{\omega} \wedge_{\kappa} F_{\omega} 
= \| F_{\omega}\|. 
$$

=--


+-- {: .un_example}
###### Example

Let $M$ be a [[spacetime]]. A classical [[electromagnetic field]] theory over $M$ is a Yang-Mills Theory over $M$ with gauge group $G=U(1)$. In more detail: 

* for an electromagnetic field theory given by a $U(1)$-bundle $P$ over $M$, we have $\mathrm{Ad}(P) \cong P \times \R$, so that $\Omega^k(M,\mathrm{Ad}(P)) \cong \Omega^k(M)$ and $\Omega^k_{\mathrm{Ad}}(P,\mathfrak{g})\cong \Omega^k_{\mathrm{Ad}}(P)$. In particular, $F_{\omega} \in \Omega^2(M)$. 

* Since $U(1)$ is [[abelian group|abelian]], $\mathrm{d}(\mathrm{Ad}) = 0$ and so $\mathrm{D}^{\omega}=\mathrm{d}$ on $\Omega^{k}_{\mathrm{Ad}}(P)$.
  
* Thus, the Yang-Mills equations reduce to  Maxwell's equations for an electromagnetic field on $M$:
$$
\mathrm{d}\star F_{\omega} = 0
\quad\text{ and }\quad
\mathrm{d}F_{\omega}=0
\text{.}
$$

=--


## General Matter Fields 

+-- {: .un_def}
###### Definition

Let $G$ be a gauge group. A _matter type for  $G$_ is a tuple $(V,h,\rho,f)$ consisting of:

* a finite-dimensional real [[vector space]] $V$ called the _internal state space_.

* a [[scalar product]] $h: V \times V \to \R$.

* a [[representation]] $\rho: G \times V \to V$ that is [[isometry|isometric]] with respect to $h$ i.e. $h(\rho(g)(v),\rho(g)(w)) = h(v,w)$.

* a [[smooth function]] $f: V \to \R$ that is $\rho$-invariant, i.e. $f(\rho(g)(v))=f(v)$.

=--


+-- {: .un_def}
###### Definition

Let $P$ be a principal $G$-bundle over $M$, and let $\mathcal{T} =(V,h,\rho,f)$ be a matter type for $G$. A _field for $P$ of type $\mathcal{T}$_ is a smooth [[section]] $\phi: M \to P \times_{\rho} V$. Its  [[action functional]] is

$$
S_{\mathcal{T}}(\omega,\phi) := \int_M  \;\|\, \mathrm{D}^{\omega}(\phi)\, \|^2_{h}  +  \star (f \circ \phi) \text{.}
$$

=--


+-- {: .un_theorem}
###### Theorem

The action functional $S_{\mathcal{T}}$ is gauge invariant, i.e. 
$$
S_{\mathcal{T}}(g^{*}\omega,g^{*}\phi) = S_{\mathcal{T}}(\omega,\phi)
$$
for all gauge transformations $g:P \to P$.

=--

+-- {: .proof}
###### Proof

One calculates that $g^{*}\omega = \mathrm{Ad}_{\tilde g}^{-1}(\omega) - \tilde g^{*}\bar\theta$, where $\tilde g:P \to G$ is the smooth map associated to $g$ via $g(p) = p\cdot  \tilde g(p)$. Further, $g^{*}\psi = \rho(\tilde g^{-1})(\psi)$. A computation shows
$$
\mathrm{d}(\rho(\tilde g^{-1})(\psi)) = \rho(\tilde g^{-1})(\mathrm{d}\psi) + \tilde g^{*}\bar\theta\wedge_{\mathrm{d}\rho} \rho(\tilde g^{-1})(\psi)\text{,}
$$
where $\mathrm{d}\rho: \mathfrak{g} \otimes V \to V$. 
Now we compute

$\quad\quad\mathrm{d}^{g^{*}\omega}(g^{*}\psi)$

$\quad\quad\quad\quad= \mathrm{d}\rho(\tilde g^{-1},\psi) + g^{*}\omega \wedge_{\mathrm{d}\rho} \rho(\tilde g^{-1},\psi)$


$\quad\quad\quad\quad= \rho(\tilde g^{-1},\mathrm{d}\psi) + \tilde g^{*}\bar\theta\wedge_{\mathrm{d}\rho} \rho(\tilde g^{-1},\psi) + (\mathrm{Ad}_{\tilde g}^{-1}(\omega) - \tilde g^{*}\bar\theta) \wedge_{\mathrm{d}\rho} \rho(\tilde g^{-1},\psi)$


$\quad\quad\quad\quad= \rho(\tilde g^{-1},\mathrm{d}\psi)  + \rho(\tilde g^{-1},\omega\wedge_{\mathrm{d}\rho} \psi)$


$\quad\quad\quad\quad= \rho(\tilde g^{-1},\mathrm{d}^{\omega}\psi)\text{.}$


Since $h$ is invariant, the invariance of the first term follows. The invariance of the second term is clear.

=--



+-- {: .un_remark}
###### Remark


One can either keep a connection $\omega$ fixed and consider

$$
S_{\omega}(\phi) := S_{\mathcal{T}}(\omega,\phi)
$$

as a matter field in an "external gauge field", or consider the combined action functional

$$
S(\omega,\phi) := S_{Y\!M}(\omega) + S_{\mathcal{T}}(\omega,\phi)\text{.}
$$


=--


+-- {: .un_example}
###### Example
**(Scalar particle in an external, trivial gauge field)**

We consider $G=\left \lbrace e \right \rbrace$, $P=M$, so that necessarily $\omega=0$. A _scalar field_ is field for $M$ of matter type $(\R,h,\id,f)$ where $f(x) := -\frac{1}{2}m^2x^2$ and $h(x,y) = x y$. The action functional is
$$
S(0,\phi) =\frac{1}{2} \int_M  \| \mathrm{d}\phi \|_h^2 +\star m^{2}\phi^2\text{.}
$$
The Euler-Lagrange equation is the _[[Klein-Gordon equation]]_
$$
(\triangle + m^2)\phi = 0\text{,}
$$
where $\triangle := \delta \circ \mathrm{d}: \Omega^k(M) \to \Omega^{k}(M)$ is the Laplace operator and $\delta := \star \mathrm{d} \star$ is the exterior coderivative. 

=--

+-- {: .un_example}
###### Example
**(Charged particle in an  electromagnetic field, e.g. a $\pi^{-}$-meson)**

Let $P$ be a $U(1)$-principal bundle over $M$. A _field of charge $n \in \Z$_ is a field for $P$ of matter type $(\C,h,\rho_n,f)$, where $\rho_n: U(1) \times \C \to \C$ is defined by $\rho_n(z,z') := z^nz'$  and $f(z) := -\frac{1}{2}m^2|z|^2$. The action functional is
$$
S(\omega,\phi) =\frac{1}{2} \int_M  \| \mathrm{D}^{\omega}\phi \|^2 +\star m^{2} \| \phi \| ^2\text{.}
$$
The Euler-Lagrange equation is _covariant Klein-Gordon equation_
$$
(\triangle^{\omega} +m^2) \phi = 0\text{,}
$$
where $\triangle^{\omega} :=\delta^{\omega}\circ \mathrm{D}^{\omega}$ is the _covariant Laplace operator_ and $\delta^{\omega} := \star \mathrm{D}^{\omega} \star$ is the _exterior covariant coderivative_. 

=--



## Matter Fields with Spin 

The [[Klein-Gordon equation]]s found above are -- unlike the [[Schrödinger equation]] -- of second order on time. Dirac's motivation was to find a first order equation which upon iteration yields the Klein-Gordon equation. 
We first discuss free [[spinor]]s (where free means that they are not coupled to an [[electromagnetic field]], but still feel the "[[gravity]]" of the [[spacetime]] [[manifold]]), and then add the coupling.

### Free Spinors 

+-- {: .un_example}
###### Example

We recall some facts about [[Clifford algebra]]s and the [[spin group]]. 

* We denote by $C(p,q)$ the Clifford algebra on $\R^{p,q}$, i.e. the quotient of the tensor algebra of $\R^{p+q}$ by the ideal generated by $v \otimes w + w \otimes v + 2 \left \langle v,w  \right \rangle\cdot 1$, where $\left \langle -,-  \right \rangle$ is the Minkowski scalar product of signature $(p,q)$. 

* The map $v \mapsto -v$ extends to an anti-automorphism $\alpha: C(p,q) \to C(p,q)$, whose eigenspace decomposition yields the usual $\Z_2$-grading on $C(p,q)$. 

* We have $\dim C(p,q) = 2^{p+q}$.

* The Clifford algebra inherits a [[bilinear form]] $H(v,w) := (v^{tr}w)_0$, where $()^{tr}$ is the anti-automorphism of the tensor algebra that reverts the order of [[tensor product]]s, and $()_0$ denotes the degree 0 part.

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

=--


+-- {: .un_remark}
###### Remark

We also need some facts about [[spin structure]]s. 

* Let $M$ be a [[spacetime]] with [[pseudo-Riemannian metric]] of [[signature]] $(p,q)$. We denote by $FM$ be the principal $SO(p,q)$-bundle over $M$ of orthonormal frames, the _[[frame bundle]]_. 

* A _[[spin structure]]_ on $M$ is a principal $Spin(p,q)$-bundle $SM$ over $M$ together with a bundle morphism $\lambda: SM \to FM$ such that $\lambda(X\cdot\varphi) = \lambda(X)\cdot\Lambda(\varphi)$ for all $X\in SM$ and all $\varphi\in Spin(p,q)$. 

* Let $\theta \in \Omega^1(FM,\mathfrak{so}(p,q))$ be the Levi-Cevita connection on $FM$. Then, 
$$
\Theta := \mathrm{d}\Lambda^{-1}(\lambda^{*}\theta) \in \Omega^1(SM,\mathfrak{spin}(p,q))
$$
is a connection on $SM$. 


=--


+-- {: .un_remark}
###### Remark

Finally, we recall the definition of the [[Dirac operator]]. 

* Let $\rho: C(p,q) \times V \to V$ be a [[representation]], with $V \subset \C(p,q)$. Note that in the above realization of the group $Spin(p,q)$, the representation $\rho$ restricts to a representation of $Spin(p,q)$.
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

* The _[[Dirac operator]]_ is
$$
D: \Gamma(M,V M) \to \Gamma(M,V M) : \psi \mapsto \sum_{i} e_i \cdot  \mathrm{D}^{\Theta}\psi (e_i)
$$
where $e_i\in TM$ runs over a local orthonormal basis.

=--



+-- {: .un_def}
###### Definition

Let $M$ be a spacetime with spin structure $SM$, and considered as a  $Spin(p,q)$ as a Yang-Mills theory over $M$. A _free spinor_ is a field for $SM$ of type $(V,h,\rho,f)$, where $V \subset \C(p,q)$, the scalar product $h$ is
$$
h(v,w):=\frac{1}{2}(H(v,w) + H(w,v))\text{,}
$$
and $\rho$ is the restriction of the multiplication in $\C(p,q)$ to $Spin(p,q)$.
The action functional is
$$
S(\psi) := \int_M D \psi \wedge_{h} \star \psi  + \star f \circ \psi\text{.}
$$

=--


+-- {: .un_def}
###### Definition

The Euler-Lagrange equation determined by the action functional $S(\psi)$ is the _Dirac equation_
$$
D\psi + \mathrm{i}m\psi = 0\text{.}
$$

=--


+-- {: .un_def}
###### Definition
**(Weyl spinors)**

We assume spacetime to have even dimension.
_[[Weyl spinor]]s_ have $V=\Sigma^{\pm}$, with the sign corresponding to left/right-handed spinors. Thus, $\dim_{\C}(V)=2$.
Further $f=0$ (they are massless). In the standard model, neutrinos are left-handed Weyl spinors.  

=--


+-- {: .un_def}
###### Definition
**(Dirac spinors)**

We assume spacetime to have signature $(1,3)$. [[Dirac spinor]]s have $V=\Sigma^{+} \oplus \Sigma^{-}$, so that $\dim_{\C}(V)=4$. The function $f$ is taken to be $f(v)=-mh(v,v)$. In the standard model, electrons are Dirac spinors. 

=--


+-- {: .un_remark}
###### Remark

In the physical literature, the picture is slightly different:
The representation space $V$ of a spinor is not a subspace of the Clifford algebra, but rather $\C^n$. One can think about this as a further  association of $\C^n$ to the Clifford bundle $VM$ using a representation of $\C(p,q)$ on $\C^n$. Below we describe this in the case of the electron, i.e. $(p,q)=(1,3)$ and $V= \Sigma^{+} \oplus \Sigma^{-}$. Another difference is here that instead of $Spin(1,3)$, physicists often use the (non-canonically) isomorphic group $SL(2,\C)$.

* One starts with the following representation  $\gamma: \C(1,3) \to \mathrm{Gl}(4,\C)$. Consider the $\R$-linear map 
$$
\gamma: \R^4 \to \mathrm{Gl}(4,\C): v \mapsto \begin{pmatrix} 0 & v' \\
v'' & 0 
\end{pmatrix}\text{,}
$$
where 
$$
v' := \begin{pmatrix} v_0 + v_3 & v_1 - iv_2 \\
v_1 + iv_2 & v_0 - v_3 \\
\end{pmatrix}
\quad\text{ and }\quad
v'' = \begin{pmatrix} v_0-v_3 & -v_1 + iv_2 \\
-v_1-iv_2 & v_0+v_3 \\
\end{pmatrix}\text{.}
$$
It satisfies $\gamma(v) \cdot \gamma(v)= - \left \langle v,v  \right \rangle I_4$. The Clifford algebra has a universal property that implies that $\gamma$ extends uniquely to a representation of $\C(1,3)$. 
The images of the standard basis vectors $e_0,...,e_3$ are often called _$\gamma$-matrices_, $\gamma_k := \gamma(e_k)$.


* The restriction of the representation $\gamma$ to $Spin(1,3)$ is a representation $\rho: Spin(1,3) \times \C^4 \to \C^4$. It splits into a direct sum of two representations equivalent to $\Sigma^+$ and $\Sigma^-$. Using $\rho\circ\alpha = \alpha$, one checks using the above definition of the group homomorphism $\Lambda: Spin(p,q) \to SO(p,q)$ that
$$
\gamma(\Lambda(\varphi)v) = \rho(\varphi)\gamma(v)\rho(\varphi)^{-1}\text{.}
$$

* The above mentioned identification between $Spin(1,3)$ and $SL(2,\C)$ is 
$$
Spin(1,3) \to SL(2,\C) : v_1 \cdot...\cdot v_{2r} \mapsto v_1'v_2''v_3'\cdot...\cdot v_{2r}''\text{.}
$$
Under this isomorphism, $\rho$ becomes
$$
\rho: SL(2,\C) \to \mathrm{Gl}(4,\C) : A \mapsto \begin{pmatrix}A & 0 \\
0 & A^{*-1}
\end{pmatrix}\text{.}
$$
Under this identification, the splitting of $\rho$ into a direct sum yields the defining representation, often called $D^{(1/2,0)}$ and its conjugate, often called $D^{(0,1/2)}$.

* Finally, the bilinear form $H$ becomes 
$$
H(v,w) := v^{\mathrm{tr}}\gamma_0\bar w.
$$ 


=--


+-- {: .un_remark}
###### Remark

If $M=\R^{1,3}$ one can take the trivial spin structure $SM=M \times SL(2,\C)$. It has a canonical global section, so that a spinor $\psi$ can be identified with a map $\psi: M \to \C^4$. The Dirac operator is now
$D \psi = \gamma^{i}\partial_i \psi$, where $\gamma^i := \eta^{ik}\gamma_k$. Now, the Dirac equation is
$$
\gamma^i\partial_i \psi + \mathrm{i} m\psi = 0\text{.}
$$
Let's go back to Dirac's orginial motivation. Dirac was looking for a first order differential equation 
$$
\alpha^k\partial_k\psi +im\psi=0
$$
for functions $\psi: \R^{4} \to \C^n$, whose solutions are automatically solutions of the Klein-Gordon equation
$$
(\triangle + m^2)\psi = 0\text{,}
$$
where $\triangle= \partial^k\partial_k$. If $\psi$ is a solution to the first equation,
$$
\alpha^{j}\partial_j\alpha^k\partial_k \psi = \alpha^{j}\partial_j(-im\psi) = - m^2\psi\text{.}
$$
This is the Klein-Gordon equation, if $\alpha^{i}\alpha^{j}=\eta^{ij}$. This can only be satisfied for matrices, so that better $\alpha^{i}\alpha^{j}=\eta^{ij}I_n$. Since $\eta^{ij}I_n$ is a symmetric matrix, this can be written as
$$
\frac{1}{2}(\alpha^{i}\alpha^j + \alpha^j\alpha^i)= \eta^{ij}\text{.}
$$
The smallest matrices satisfying this relation are the above "gamma matrices". If $m=0$, there is a solution in dimension two, the "Pauli matrices". 

=--




+-- {: .un_remark}
###### Remark

For a general spacetime $M$, and unlike in the previous remark, $D^2 \neq \triangle$. Rather, $D^2$ is given by the _Lichnerowiz formula_ which has in fact been proved first by Schr&#246;dinger. So, Dirac's motivation actually fails for "curved spacetimes". 


=--


### Charged Spinors

+-- {: .un_remark}
###### Remark
**(Bundle Splicing)**

* Consider principal $G_k$-bundles $P_k$ over $M$, for $k=1,2$. The fibre product $P_1 \times_M P_2$ is a principal $(G_1 \times G_2)$-bundle over $M$, denoted $P_1 \circ P_2$.

* If $\omega_1$ and $\omega_2$ are connections on $P_1$ and $P_2$, respectively, then 
$$
\omega_1 \circ \omega_2 := \mathrm{pr}_1^{*}\omega_1 \oplus \mathrm{pr}_2^{*}\omega_2 \in \Omega^1(P_1 \circ P_2,\mathfrak{g}_1 \oplus \mathfrak{g}_2)
$$
is a connection on $P_1 \circ P_2$.

* Suppose $V$ is a vector space and $\rho_k: G_k \to \mathrm{Gl}(V)$ are representations, such that $\rho_1(g_1) \circ \rho_2(g_2) = \rho_2(g_2) \circ \rho_1(g_1)$ for all $g_1\in G_1$ and $g_2 \in G_2$. Then, $\rho_1 \times \rho_2$ is a representation of $G_1 \times G_2$ on $V$. 

=--



+-- {: .un_remark}
###### Remark

Let $M$ be a spacetime with spin structure $SM$ and let $P$ be a Yang-Mills theory over $M$ with gauge group $G$. For $\rho_{SM}: Spin(p,q) \to \mathrm{Gl}(V)$ a representation with $V \subset \C(p,q)$, and $\rho_P: G \to \mathrm{Gl}(V)$ a commuting representation, the associated bundle $VP := (SM \circ P) \times_{(\rho_{SM} \times \rho_P)} V$ still has a Clifford multiplication. 
For $\omega$ a connection on $P$, one can define a Dirac operator 
$$
D^{\omega}: \Gamma(M,\Sigma M \circ P) \to \Gamma(M,\Sigma M \circ P):\psi \mapsto \sum_{i} e_i \cdot \mathrm{D}^{\Theta \circ \omega}(\psi)(e_i)\text{.}
$$


=--


+-- {: .un_def}
###### Definition

Let $M$ be a spacetime with spin structure, let $P$ be a Yang-Mills theory with gauge group $G$ over $M$, and let $\rho_P$ be a representation of $G$ on $V$ commuting with $\rho_{SM}$. A _charged spinor_ is a field for $SM \circ P$ of type $(V,h,\rho_{SM} \times \rho_P,f)$, where $V \subset \C(p,q)$ and $H$ is given as before.
Its action functional is
$$
S(\omega, \psi) := \int_M D^{\omega} \psi \wedge_{h} \star \psi    + \star f \circ \psi\text{.}
$$


=--


+-- {: .un_def}
###### Definition
**(Spinor in an electromagnetic field)**

Here, $\rho_{SM}: Spin(p,q) \to \mathrm{Gl}(V)$ is some representation, and $\rho_P: \ueins \to \mathrm{Gl}(V)$ is given by complex multiplication with $z^{n}$, where $n\in \Z$ is the charge of the spinor. Obviously $\rho_{SM}$ and $\rho_P$ commute. The Euler-Lagrange equation is
$$
D^{\omega}\psi + im\psi = 0\text{.}
$$
If $M=\R^{1,3}$ one can take $SM=M \times SL(2,\C)$. The canonical global section identifies $\psi$ with a smooth function $\psi: \R^{3,1} \to \C^4$ and the connection $\omega$ with a 1-form with components $A_{i}$. Then,
$$
D^{\omega}\psi = \gamma^{i}(\partial_{i} + A_i)\psi\text{.}
$$
This gives the "[[Dirac equation]]" one usually finds in a textbook. 

=--


## References

Useful literature on this topic is:

* [[Christian Bär]], _Introduction to Spin Geometry_, Oberwolfach Reports 53 (2006), p. 3135-3136.

* D. Bleecker, _Gauge Theory and Variational Principles_, Addison-Weasley, 1981.

* H. Blaine Lawson Jr. , Marie-Louise Michelson, _Spin geometry_, Princeton Univ. Press, 1989.

* G. L. Naber, _Topology, Geometry and Gauge Dields_, Springer, 1999.




[[!redirects Dirac electron]]
[[!redirects spinors in Yang-Mills theory]]