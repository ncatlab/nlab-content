
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A graded monoid is like a monoid but where elements of the monoid possess some degree and such that when you multiply, you sum the degrees. It can be defined in any monoidal category.

## Definition and properties

Let $M$ be a [[commutative monoid]] (in the category $\mathbf{Sets}$). A **$M$-graded monoid** $\Phi$ in a [[monoidal category]] $\mathcal{V}$ with [[unit object]] $I$ is the data of

* for each $m \in M$, an [[object]] $\Phi_m$,
* for each $m,n \in M$, a [[morphism]]
  $$\nabla_{m,n}: \Phi_m \otimes \Phi_n \to \Phi_{m+n} $$
* a morphism
  $$ \eta: I \to \Phi_0 $$

such that the obvious [[associativity]] and [[unit]] [[axioms]] hold.

Thus, a $M$-graded monoid is in particular a $M$-[[graded object]]. In fact, a $M$-graded monoid is just a [[monoid in a monoidal category|monoid]] in the monoidal category of $M$-graded objects of $\mathcal{V}$, hence a [[lax monoidal functor]] $M \to \mathcal{V}$ by [[Day convolution#DayMonoidsAreLaxMonoidalFunctorsOnTheSite|this proposition]] (where $M$ is viewed as a [[discrete category|discrete]] monoidal category).

We say that a $M$-graded monoid is **connected** if $\eta$ is an isomorphism.


If $\Phi$ is a $M$-graded monoid in $\mathcal{V}$, then $(\Phi_{0},\nabla_{0,0},\eta)$ is a (non-graded) monoid in $\mathcal{V}$.

## Examples

The following are all examples of connected $\mathbb{N}$-graded monoids.

* In the [[symmetric monoidal category]] of [[groups]] with the [[cartesian product]], an example of $\mathbb{N}$-graded monoid is the trivial one $1 = (1)_n$

* In the same category, another example is the **graded monoid of symmetric groups** $\Sigma = (\Sigma_n)_n$.

* In any monoidal category, defining $\Phi_n := A^{\otimes n}$, $\nabla_{m,n}:A^{\otimes m} \otimes A^{\otimes n} \rightarrow A^{\otimes (m+n)}$ given by [[associators]] and $\eta = 1_{I}$, we obtain the connected $\mathbb{N}$-graded monoid of tensor powers.

* In any symmetric monoidal category, defining $S^n(A)$ equal to the [[coequalizer]] of the $n!$ permutations $A^{\otimes n} \rightarrow A^{\otimes n}$ and defining the multiplication $S^n(A) \otimes S^p(A) \rightarrow S^{n+p}(A)$ by using the universal property of the coequalizer, we obtain the connected commutative $\mathbb{N}$-graded monoid of [[symmetric powers]].

* In any symmetric monoidal category, defining $\Gamma^n(A)$ equal to the [[equalizer]] of the $n!$ permutations $A^{\otimes n} \rightarrow A^{\otimes n}$ and defining the multiplication $\Gamma^n(A) \otimes \Gamma^p(A) \rightarrow \Gamma^{n+p}(A)$ by using the universal property of the equalizer, we obtain the connected commutative $\mathbb{N}$-graded monoid of [[divided powers]].

* In any symmetric monoidal category enriched over the category of abelian groups, defining $\Lambda^n(A)$ equal to the coequalizer of the $n!$ signed permutations $sgn(\sigma).\sigma:A^{\otimes n} \rightarrow A^{\otimes}$ where $sgn(\sigma)$ is the [[signature]] of the permutation $\sigma$ and defining the multiplication $\Lambda^n(A) \otimes \Lambda^p(A) \rightarrow \Lambda^{n+p}(A)$ by using the universal property of the equalizer, we obtain the connected graded-commutative  (ie. such that $\sigma;\nabla_{p,n} = sgn(\sigma).\sigma:\Phi_{n} \otimes \Phi_{p} \rightarrow \Phi_{n+p}$) $\mathbb{N}$-graded monoid of [[exterior powers]]. Replacing the coequalizer by an equalizer always provides an isomorphic $\mathbb{N}$-graded monoid.

The  connected commutative $\mathbb{N}$-graded monoid of symmetric powers and of divided powers are not isomorphic in general, but they are if the symmetric monoidal category is enriched over $\mathbb{Q}^{+}$-modules, for instance in the category of [[vector spaces]] over a [[field]] of [[characteristic]] $0$ or in the category of sets and [[relations]] (where $S^{n}(X) \cong \Gamma^{n}(X)$ is equal to the set of all multisets of $n$ elements of $X$).

## See also

* [[monoid object]]
* [[graded object]]
* [[graded comonoid]]
* [[graded bimonoid]]

[[!redirects graded unitary monoid]]
[[!redirects graded unital monoid]]