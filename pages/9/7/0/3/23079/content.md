
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

An _idempotent monoid_ is a monoid that “squares to itself” in the evident [[category theory|category-theoretic]] sense.

## Definition

An **idempotent monoid in $\mathcal{C}$** is a monoid $(A,\mu,\eta)$ in $\mathcal{C}$ whose multiplication morphism $\mu\colon A\otimes_{\mathcal{C}}A\to A$ is an isomorphism.

Similarly, a **non-unital idempotent monoid in $\mathcal{C}$** is a non-unital monoid $(A,\mu)$ in $\mathcal{C}$ with $\mu$ an isomorphism.

We write $\mathsf{IdemMon}(\mathcal{C})$ for the full subcategory of $\mathsf{Mon}(\mathcal{C})$ spanned by the idempotent monoids in $\mathcal{C}$.

## Properties

### Preservation by strong monoidal functors

A [[strong monoidal functor]] $F\colon\mathcal{C}\to\mathcal{D}$ induces a functor
\[\mathsf{IdemMon}(F)\colon\mathsf{IdemMon}(\mathcal{C})\to\mathsf{IdemMon}(\mathcal{D}),\]
and hence “preserves” idempotent monoids.

Similarly, non-unital strong monoidal functors “preserve” non-unital idempotent monoids.

### As strong monoidal functors from the punctual category

(Non-unital) idempotent monoids in $\mathcal{C}$ are the same as (non-unital) strong monoidal functors from the punctual monoidal category $\mathsf{pt}$.

### As strictly unitary strong monoidal functors from the Boolean monoid

Non-unital idempotent monoids in $\mathcal{C}$ are also the same as _strictly unitary_ strong monoidal functors from $\mathbb{B}_\mathsf{disc}$, where $\mathbb{B}=(\{0,1\},\vee,1)$ is the “Boolean monoid”, the initial monoid with an idempotent element.

## Examples

* A non-unital idempotent monoid in $\left(A_{\mathsf{disc}},\cdot_A,1_A\right)$ for $A$ an ordinary monoid (in $\mathsf{Set}$) is an idempotent element of $A$, i.e. an element $a\in A$ such that $a^2=a$.
* A non-unital idempotent monoid in $\left(\mathrm{End}_{\mathcal{C}}(X)_{\mathsf{disc}},\circ^{\mathcal{C}}_{X,X,X},\mathrm{id}_X\right)$ with $\mathrm{End}_{\mathcal{C}}(X)$ the monoid of endomorphisms of $\mathcal{C}$ at $X$ is an idempotent morphism $f\colon X\to X$ of $\mathcal{C}$, satisfying $f\circ f=f$.
* An idempotent monoid in $\left(\mathsf{Ab},\otimes_{\mathbb{Z}},\mathbb{Z}\right)$ is a [[solid ring]].
* An idempotent monoid in $\left(\mathsf{Fun}(\mathcal{C},\mathcal{C}),\circ,\mathrm{id}_\mathcal{C}\right)$ is an [[idempotent monad]].
* An idempotent monoid in the monoidal category $\mathsf{End}_{\mathcal{C}}(X)$  of endomorphisms of a bicategory $\mathcal{C}$ at $X\in\mathrm{Obj}(\mathcal{C})$ is an idempotent $1$-morphism $f\colon X\to X$ of $\mathcal{C}$, satisfying $f\circ f\simeq f$ up to coherent $2$-isomorphism.
* An idempotent monoid in $\left(\mathsf{Sp},\otimes_{\mathbb{S}},\mathbb{S}\right)$ is a "solid ring spectrum" as in [Gutierrez 2013, Section 4](#Gutierrez13). See also [MO #298435](https://mathoverflow.net/questions/298435).

## Related concepts

* [[monoid]]
* [[commutative monoid in a symmetric monoidal category]]
* [[idempotent monad]]

## References

* Peter Hines, _The categorical theory of self-similarity_, 1999. [[Theory and Applications of Categories]]. ([abstract](http://www.tac.mta.ca/tac/volumes/6/n3/6-03abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/6/n3/n3.pdf), [dvi](http://www.tac.mta.ca/tac/volumes/6/n3/n3.dvi), [ps](http://www.tac.mta.ca/tac/volumes/6/n3/n3.ps).)

* {#Gutierrez13} [[Javier J. Gutiérrez]], *On solid and rigid monoids in monoidal categories*, Applied Categorical Structures 23, no. 2 (2015), 575-589 ([arXiv:1303.5265](https://arxiv.org/abs/1303.5265))