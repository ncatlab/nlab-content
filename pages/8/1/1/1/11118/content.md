
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


## Definition

Let $M$ be a [[commutative monoid]] (in the category $\mathbf{Sets}$). A **$M$-graded monoid** $\Phi$ in a [[symmetric monoidal category]] $\mathcal{V}$ with [[unit object]] $I$ is the data of

* for each $m \in M$, an [[object]] $\Phi_m$,
* for each $m,n \in M$, a [[morphism]]
  $$\nabla_{n,m}: \Phi_m \otimes \Phi_n \to \Phi_{m+n} $$
* a morphism
  $$ \eta: I \to \Phi_0 $$
such that the obvious [[associativity]] and [[unit]] [[axioms]] hold.

Thus, a $M$-graded monoid is in particular a $M$-[[graded object]]. In fact, a $M$-graded monoid is just a [[monoid in a monoidal category|monoid]] in the monoidal category of $M$-graded objects of $\mathcal{V}$, hence a [[lax monoidal functor]] $M \to \mathcal{V}$ by [[Day convolution#DayMonoidsAreLaxMonoidalFunctorsOnTheSite|this proposition]] (where $M$ is viewed as a [[discrete category|discrete]] monoidal category).

We say that a $M$-graded monoid is **connected** if

* $\eta$ is an isomorphism,
* $\eta \otimes \nabla_{0,p}$ and $\nabla_{n,0} \otimes \eta$ are equal to the identity. 

## Properties

* If $\Phi$ is a $M$-graded monoid in $\mathcal{V}$, then $(\Phi_{0},\nabla_{0,0},\eta)$ is a monoid in $\mathcal{V}$.
* If $\mathcal{V}$ is a symmetric monoidal category which is also a [[zero morphism|enriched over pointed sets]], and if $(A,\nabla,\eta)$ is a monoid in $\mathcal{V}$, then we get a $\mathbb{N}$-graded monoid $\Phi$ by defining:

  * $\Phi_{m} := A$ for every $m$
  * $\nabla_{0,0} := \nabla$
  * $\nabla_{m,n} := 0$ if $m \neq 0$ or $n \neq 0$

## Examples

* In the [[symmetric monoidal category]] of [[groups]] with the [[cartesian product]], two examples of $\mathbb{N}$-graded monoids are the trivial one $1 = (1)_n$ and the **graded monoid of symmetric groups** $\Sigma = (\Sigma_n)_n$.

The two examples above in the category of groups are connected (by considering that $\Sigma_{0} = 1$).

## See also

* [[monoid object]]
* [[graded object]]
* [[graded comonoid]]
* [[graded bimonoid]]

[[!redirects graded unitary monoid]]
[[!redirects graded unital monoid]]