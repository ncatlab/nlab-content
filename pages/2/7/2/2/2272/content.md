
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

## Idea

Poisson manifolds are a mathematical setup for [[classical mechanics]] with finitely many degrees of freedom. 

## Definition

A __[[Poisson algebra]]__ is a commutative unital [[associative algebra]] $A$, in this case over the field of [[real number|real]] or [[complex numbers]], equipped with a Lie bracket $\{,\}:A\otimes A\to A$ such that, for any $f\in A$, $\{ f,-\}:A\to A$ is a [[derivation]] of $A$ as an associative algebra.

A __Poisson manifold__ is a real [[smooth manifold]] $M$ equipped with a __Poisson structure__. A Poisson structure is a Lie algebra bracket $\{,\}:C^\infty(M)\times C^\infty(M)\to C^\infty(M)$ on the vector space of smooth functions on $M$ which together with the pointwise multiplication of functions makes it a Poisson algebra. As derivations of $C^\infty(M)$ correspond to smooth [[tangent vector fields]], for each $f\in C^\infty(M)$ there is a vector $X_f$ given by $X_f(g)=\{f,g\}$ and called the __Hamiltonian vector field__ corresponding to the function $f$, which is viewed as a classical hamiltonian function.  

Alternatively a Poisson structure on a manifold is given by a choice of smooth antisymmetric bivector called a __Poisson bivector__ $P\in\Lambda^2 T M$; then $\{f,g\}:=\langle df\otimes dg, P\rangle$. 

This induces and is equivalently encoded by the structure of a [[Poisson Lie algebroid]].


A morphism $h:M\to N$ of Poisson manifolds is a morphism of smooth manifolds such that, for all $f,g\in C^\infty(N)$, $\{f\circ h, g\circ h\}_M = \{f,g\}_N$. 


## Examples

+-- {: .num_example}
###### Example

Every [[symplectic manifold]] carries a natural Poisson structure; however, such Poisson manifolds are very special. It is a basic theorem that Poisson structures on a manifold are equivalent to the smooth [[foliation]]s of the underlying manifold such that each leaf is a symplectic manifold.

=--

+-- {: .num_example}
###### Example


The dual to a finite-dimensional [[Lie algebra]] has a natural structure of a Poisson manifold, the _[[Lie-Poisson structure]]_. Its leaves are called [[coadjoint orbits]].

=--

+-- {: .num_example}
###### Example

Given a [[symplectic manifold]] $(X,\omega)$ and given a [[Hamiltonian]] [[function]] $H \colon X \longrightarrow \mathbb{R}$, there is a Poisson bracket on the functions on the [[smooth space|smooth]] [[path space]] $[I,X]$ (the "space of histories" or "space of [[trajectories]]"), for $I = [0,1]$ the closed [[interval]], which is such that its [[symplectic leaves]] are each a copy of $X$, but regarded as the space of initial conditions for evolution with respect to $H$ with a [[source]] term added. For more on this see at _[[off-shell Poisson bracket]]_.

=--

+-- {: .num_example}
###### Example

Every [[local action functional]] which admits a [[Green's function]] for its [[equations of motion]] defines the [[Peierls bracket]] on [[covariant phase space]] (where in fact it is symplectic) and also "[[off-shell Poisson bracket|off-shell]]" on all of configuration space, where it is a genuine Poisson bracket, the canonocal Poisson bracket of the corresponding [[prequantum field theory]].

=--

## Properties

### Deformation quantization

[[Kontsevich formality]] implies that every Poisson manifold has a family of [[deformation quantizations]], parameterized by the [[Grothendieck-Teichmüller group]].


## Related concepts

* [[Poisson tensor]]

* [[Poisson geometry]]

* [[Poisson cohomology]]

* [[isotropic submanifold]], [[coisotropic submanifold]]

* [[symplectic leaf]]

* [[symplectic realization]]

* [[symplectic dual pair]]

* [[Poisson Lie algebroid]]

* [[Poisson bracket Lie n-algebra]]

* [[deformation quantization]]

  * [[Moyal quantization]]

[[!include Isbell duality - table]]

[[!include infinitesimal and local - table]]


[[!redirects Poisson Lie algebra]]

[[!redirects Poisson manifolds]]

[[!redirects Poisson bracket]]


[[!redirects Poisson structure]]
[[!redirects Poisson structures]]

[[!redirects Poisson Lie algebra]]
[[!redirects Poisson Lie algebras]]

[[!redirects Poisson bracket Lie algebra]]
[[!redirects Poisson bracket Lie algebras]]

