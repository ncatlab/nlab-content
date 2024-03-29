
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

The right [[adjoint functor]] of a [[functor]], if it exists, is one of two best approximations to a [[weak inverse]] of that functor.  (The other best approximation is the functor\'s [[left adjoint]], if it exists.)  Note that a weak inverse itself, if it exists, must be a right adjoint, forming an [[adjoint equivalence]].

A right adjoint to a [[forgetful functor]] is called a [[cofree functor]]; in general, right adjoints may be thought of as being defined cofreely, consisting of anything that works in an inverse, regardless of whether it's needed.

The concept generalises immediately to [[enriched category|enriched categories]] and in [[2-category|2-categories]].


## Definitions 

Given [[partial order|posets]] (or [[preorder|prosets]]) $C$ and $D$ and a monotone function $U: C \to D$, a __right adjoint__ of $U$ is a monotone function $G: D \to C$ such that
$$ U(x) \leq y \;\Leftrightarrow\; x \leq G(y) $$
for all $x$ in $C$ and $y$ in $D$.

Given [[locally small categories]] $C$ and $D$ and a [[functor]] $U: C \to D$, a __right adjoint__ of $U$ is a functor $G: D \to C$ with a [[natural isomorphism]] between the [[hom-set]] functors
$$ Hom_D(U(-),-), Hom_C(-,G(-)): C^op \times D \to Set .$$

Given $V$-enriched categories $C$ and $D$ and a $V$-[[enriched functor]] $U: C \to D$, a __left adjoint__ of $U$ is a $V$-enriched functor $F: D \to C$ with a $V$-[[enriched natural transformation|enriched natural isomorphism]] between the [[hom-object]] functors
$$ Hom_C(F(-),-), Hom_D(-,U(-)): D^op \times C \to Set .$$

Given categories $C$ and $D$ and a functor $U: C \to D$, a __right adjoint__ of $U$ is a functor $G: D \to C$ with [[natural transformations]]
$$ \iota: id_C \to U ; G,\; \epsilon: G ; U \to id_D $$
satisfying certain [[triangle identities]].

Given a [[2-category]] $\mathcal{B}$, objects $C$ and $D$ of $\mathcal{B}$, and a morphism $U: C \to D$ in $\mathcal{B}$, a __right adjoint__ of $U$ is a morphism $G: D \to C$ with $2$-morphisms
$$ \iota: id_C \to U ; G,\; \epsilon: G ; U \to id_D $$
satisfying the triangle identities.

Although it may not be immediately obvious, these definitions are all compatible.

Whenever $G$ is a right adjoint of $U$, we have that $U$ is a [[left adjoint]] of $G$.

## Properties

* [[right adjoints preserve limits]]

* right adjoints preserve [[monomorphisms]].


## Related concepts

*  See [[Galois connection]] for right adjoints of monotone functions.
*  See [[adjoint functor]] for right adjoints of functors.
*  See [[adjunction]] for right adjoints in $2$-categories.
*  See [[examples of adjoint functors]] for examples.

* [[parametric right adjoint]]

[[!redirects right adjoints]]

[[!redirects right adjoint functor]]
[[!redirects right adjoint functors]]

