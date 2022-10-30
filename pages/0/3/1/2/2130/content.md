
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

A **symplectic manifold** is 

* a [[smooth manifold]] $X$ of even [[dimension]] $dim X = 2 n$;

* equipped with a **symplectic form**: 

  * a closed smooth [[differential form|2-form]] $\omega \in \Omega^2_{cl}(X)$;

  * such that $\omega$ is **non-degenerate**, which means equivalently that

    * $\omega^{\wedge n}=\omega\wedge\omega\wedge\cdots\wedge\omega$ has the maximal [[rank]] at every point $p\in X$;

    * $(\wedge^2 T^*_p X,\omega_p)$ is a [[symplectic vector space]] for every point $p\in X$.  

=--


+-- {: .num_defn}
###### Definition


A $2n$-dimensional [[topological manifold]] $X$ is 

* a real __symplectic manifold__ 

* equipped with  a **symplectic atlas**: 

  * an [[atlas]] consisting of smooth [[chart]]s $\phi_i:U_i\to X$ as usual, 

  * such that the transition functions $\phi_j^{-1}\circ\phi_i:\phi_i^{-1}(\phi_i(U_i)\cap\phi_j(U_j))\to \phi_j^{-1}(\phi_i(U_i)\cap\phi_j(U_j))$ preserve the standard symplectic form $\omega_0=\sum_{i=1}^n dx_i\wedge dp_i$ on $\mathbb{R}^{2n}$ with the basis $(x_1,\ldots,x_n,p_1,\ldots,p_n)$.

=--


+-- {: .num_note #TangentCotangentIsomorphism}
###### Remark

The non-degenracy of the symplectic form implies that it defines an [[isomorphism]]

$$
  \omega(-,-) : \Gamma(T X) \to \Gamma(T^* X)
$$

between [[section]]s of the [[tangent bundle]] -- [[vector field]]s --  and [[section]]s of the [[cotangent bundle]] -- [[differential form|differential 1-form]]s -- on $X$ by the map

$$
  (v \in T_x X) \mapsto (\omega(v,-) \in T^*_x X)
  \,.
$$

=--

+-- {: .num_defn}
###### Definition

The vector fields in the image of the exact 1-forms under the isomorphism, remark \ref{TangentCotangentIsomorphism}, are called **[[Hamiltonian vector fields]]**.

=--

This means that for $H \in C^\infty(X)$ a [[smooth function]] and $d H$ its differential 1-form, the corresponding [[Hamiltonian vector field]] $v_H \in \Gamma(T X)$ is the unique vector field such that

$$
  d H = \omega(v_H, -)
  \,
$$

Equivalently, for $\phi \mathbb{R}^{2n} \to X$ a [[coordinate chart]] of $X$ and $\phi^*\omega = \omega_{i j} d x^i \wedge d x^j$ the symplectic form on this patch, the [[Hamiltonian vector field]] $v_H$ is

$$
  v_H =  \frac{\partial H}{\partial x^i} (\omega^{-1})^{i j} \partial_j
  \,.
$$

## Properties

### Darboux coordinates

By [[Darboux's theorem]] every symplectic manifold has an [[atlas]] by [[coordinate charts]] $\mathbb{R}^{2n} \simeq U \hookrightarrow X$ on which the [[symplectic form]] takes the canonical form $\omega|_U = \sum_{k = 1}^n d x^{2k} \wedge d x^{2 k+1}$.


### Relation to almost symplectic structure
 {#SymplecticStructure}

The existence of a 2-form $\omega \in \Omega^2(X)$ which is non-degenerate (but not necessarily closed) is equivalent to the existence of a [[G-structure|Sp-structure]] on $X$, a [[reduction of the structure group]] of the [[tangent bundle]] along the inclusion of the [[symplectic group]] into the [[general linear group]]

$$
  Sp(2n) \hookrightarrow GL(2n)
  \,.
$$

Such an _Sp(2n)-structure_ is also called an _almost symplectic structure_ on $X$. Adding the extra condition that $d \omega = 0$ -- the condition for [[integrability of G-structures]] -- makes it a genuine symplectic structure. See at _[integrability of G-structures -- Examples -- Symplectic structure](integrability+of+G-structures#ExampleSymplecticStructure)_.

A _[[metaplectic structure]]_ on a symplectic or almost symplectic manifold is in turn [[lift of the structure group]] to the [[metaplectic group]]. 

### Relation to almost Hermitian and K&#228;hler structure

By the [above](#SymplecticStructure), a symplectic manifold structure is an
[[integrable G-structure|integrable]] $Sp(2n,\mathbb{R}) \hookrightarrow GL(2n,\mathbb{R})$-structure. Further [[reduction of the structure group]] along the [[maximal compact subgroup]] inclusion of the [[unitary group]] $U(n) \hookrightarrow Sp(2n,\mathbb{R})$ yields is an [[almost Hermitian structure]]. If that is again [[integrable G-structure|first order integrable]] then it is _[[Kähler structure]]_. 

Such  a refinement from symplectic to K&#228;hler structure is also called a choice of _[[Kähler polarization]]_.

### Symplectomorphisms

+-- {: .num_prop}
###### Proposition

For $(X, \omega)$ a symplectic manifold, the [[vector field]]s
$v \in \Gamma(T X)$ that generate [[diffeomorphism]]s that preserve the symplectic structure are precisely the locally [[Hamiltonian vector fields]].

=--

+-- {: .proof}
###### Proof

The condition in question is that the [[Lie derivative]]

$$
  L_v \omega = 0
$$

vanishes. By [[Cartan's magic formula]] and using that $d \omega = 0$ this is equivalently

$$
  d \iota_v \omega = 0
  \,.
$$

By the [[Poincare lemma]] it follows that there is locally a function $H$ with $d H = \iota_v \omega$.

=--


### Poisson structure

+-- {: .num_defn}
###### Definition

For $(X,\omega)$ a symplectic manifold, 
define a bilinear skew-symmetric map

$$
  \{-,-\} : C^\infty(X) \otimes C^\infty(X) \to C^\infty(X)
$$

by

$$
  \{F,H\} := \iota_{v_F} \iota_{v_H} \omega
  \,.
$$

=--

In a [[coordinate chart]] this says that

$$
  \{F,H\} = (\frac{\partial F}{\partial x^i}) (\omega^{-1})^{i j}
    (\frac{\partial H}{\partial x^j})
  \,.
$$


+-- {: .num_prop}
###### Proposition

The bracket $\{-,-\}$ makes $C^\infty(X)$ a [[Poisson algebra]].

=--


## Examples

* every [[Kähler manifold]] is canonically also a symplectic manifold;

* the [[critical locus]] over any [[local action functional]] becomes a symplectic manifold after dividing out symmetries: the reduced [[phase space]].

## Related concepts

* [[bilinear form]], [[quadratic form]], [[sesquilinear form]]

* [[Kähler form]], [[Hermitian form]]

* [[MSp]]

The notion of symplectic manifold is equivalent to that of [[symplectic Lie n-algebroid]] for $n = 0$. (See there.) 

* [[isotropic submanifold]], [[coisotropic submanifold]]

* [[symplectic singularity]], [[symplectic resolution]]

* [[symplectic reduction]]

* [[symplectic connection]]

* [[geometric quantization]], [[canonical momentum]]

* [[contact manifold]]

* [[G2-manifold]]

[[!include (co)isotropic subspaces - table]]

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]



## References

See the references at [[symplectic geometry]].

Discussion of the [[torsion of a G-structure|torsion-invariants]] of almost symplectic structures includes

* {#AlbuquerquePicken11} Rui Albuquerque, Roger Picken, _On invariants of almost symplectic connections_ ([arXiv:1107.1860](http://arxiv.org/abs/1107.1860))

The generalization of the notion of symplectic manifolds to [[dg-manifolds]] is sometimes known as _[[NQ-supermanifolds|PQ-supermanifolds]]_ , due to

* M. Alexandrov, [[Maxim Kontsevich|M. Kontsevich]], [[Albert Schwarz|A. Schwarz]], O. Zaboronsky, _The geometry of the master equation and topological quantum field theory_, Int. J. Modern Phys. A 12(7):1405--1429, 1997 ([arXiv:hep-th/9502010](http://arxiv.org/abs/hep-th/9502010))


[[!redirects symplectic manifolds]]
[[!redirects symplectic form]]
[[!redirects symplectic forms]]

[[!redirects symplectic structure]]
[[!redirects almost symplectic structure]]

[[!redirects symplectic structures]]
[[!redirects almost symplectic structures]]