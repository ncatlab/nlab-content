
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _idempotent monoid_ is a [[monoid]], which is [[idempotent]] in that “squares to itself” in the evident [[category theory|category-theoretic]] sense.

## Definition

An **idempotent monoid** $(A,\mu,\eta)$ in a [[monoidal category]] $\mathcal{C}$ is a [[monoid in a monoidal category|monoid in]] $\mathcal{C}$ whose multiplication morphism $\mu\colon A\otimes_{\mathcal{C}}A\to A$ is an [[isomorphism]].

Similarly, an **idempotent semigroup in $\mathcal{C}$** (also called a _non-unital idempotent monoid in $\mathcal{C}$_) is a semigroup $(A,\mu)$ in $\mathcal{C}$ with $\mu$ an isomorphism.

We write $\mathsf{IdemMon}(\mathcal{C})$ for the [[full subcategory]] of $\mathsf{Mon}(\mathcal{C})$ spanned by the idempotent monoids in $\mathcal{C}$.

### Strict idempotency

An idempotent monoid $(A,\mu,\eta)$ or semigroup $(A,\mu)$ is **strict** if $\mu\colon A\otimes_{\mathcal{C}}A\to A$ is not only an [[isomorphism]], but in fact the [[identity morphism]] of $A$.

## Properties

### Preservation by strong monoidal functors

A [[strong monoidal functor]] (resp. [[strict monoidal functor]]) $F\colon\mathcal{C}\to\mathcal{D}$ induces a functor
\[\mathsf{IdemMon}(F)\colon\mathsf{IdemMon}(\mathcal{C})\to\mathsf{IdemMon}(\mathcal{D}),\]
and hence “preserves” idempotent monoids (resp. strict idempotent monoids).

Similarly, strong (strict) semigroupal functors ("non-unital strong monoidal functors") “preserve” (strict) idempotent semigroups.

### As strong monoidal functors from the punctual category

(Strict) idempotent monoids in $\mathcal{C}$ are the same as (strict) strong monoidal functors from the punctual monoidal category $\mathsf{pt}$.

Similarly, (strict) idempotent semigroups in $\mathcal{C}$ may be identified with (strict) strong semigroupal functors functors $(F,F^\otimes)\colon\pt\to\mathcal{C}$.

### As strictly unitary strong monoidal functors from the Boolean monoid

(Strict) idempotent semigroups in $\mathcal{C}$ are also the same as _strictly unitary_ strong monoidal functors (resp. strict monoidal functors) from $\mathbb{B}_\mathsf{disc}$ to $\mathcal{C}$, where $\mathbb{B}=(\{0,1\},\vee,1)$ is the “Boolean monoid”, the initial monoid with an idempotent element.

## Examples

* An idempotent semigroup in $\left(A_{\mathsf{disc}},\cdot_A,1_A\right)$ for $A$ an ordinary [[monoid]] (in [[Set|$\mathsf{Set}$]]) is an [[idempotent]] [[element]] of $A$, i.e. an element $a\in A$ such that $a^2=a$.

* An idempotent semigroup in $\left(\mathrm{End}_{\mathcal{C}}(X)_{\mathsf{disc}},\circ^{\mathcal{C}}_{X,X,X},\mathrm{id}_X\right)$ with $\mathrm{End}_{\mathcal{C}}(X)$ the monoid of [[endomorphisms]] of $\mathcal{C}$ at $X$ is an idempotent morphism $f\colon X\to X$ of $\mathcal{C}$, satisfying $f\circ f=f$.

* An idempotent monoid in [[abelian groups]] $\left(\mathsf{Ab},\otimes_{\mathbb{Z}},\mathbb{Z}\right)$ is a [[solid ring]].

* An idempotent monoid in an [[endomorphism]] [[functor category]] $\left(\mathsf{Fun}(\mathcal{C},\mathcal{C}),\circ,\mathrm{id}_\mathcal{C}\right)$ is an [[idempotent monad]].

* An idempotent monoid in the monoidal category $\mathsf{End}_{\mathcal{C}}(X)$  of endomorphisms of a bicategory $\mathcal{C}$ at $X\in\mathrm{Obj}(\mathcal{C})$ is an idempotent $1$-morphism $f\colon X\to X$ of $\mathcal{C}$, satisfying $f\circ f\simeq f$ up to a coherent $2$-isomorphism.

* An idempotent monoid in [[Spectra]] $\left(\mathsf{Sp},\otimes_{\mathbb{S}},\mathbb{S}\right)$ is a "solid ring spectrum" as in [Gutierrez 2013, Section 4](#Gutierrez13). See also [MO #298435](https://mathoverflow.net/questions/298435).

* An idempotent monoid in the category $\mathsf{Fun}(\mathcal{C},\mathsf{Sets})$ equipped with the Day convolution monoidal structure is a [[strong monoidal functor]]. Similarly, strict idempotent monoids in $\mathsf{Fun}(\mathcal{C},\mathsf{Sets})$ recover [[strict monoidal functors]].

## Related concepts

* [[monoid]]

* [[commutative monoid in a symmetric monoidal category]]

* [[idempotent monad]]

## References

* Peter Hines, _The categorical theory of self-similarity_, 1999. [[Theory and Applications of Categories]]. ([abstract](http://www.tac.mta.ca/tac/volumes/6/n3/6-03abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/6/n3/n3.pdf), [dvi](http://www.tac.mta.ca/tac/volumes/6/n3/n3.dvi), [ps](http://www.tac.mta.ca/tac/volumes/6/n3/n3.ps).)

* {#Gutierrez13} [[Javier J. Gutiérrez]], *On solid and rigid monoids in monoidal categories*, Applied Categorical Structures 23, no. 2 (2015), 575-589 ([arXiv:1303.5265](https://arxiv.org/abs/1303.5265))