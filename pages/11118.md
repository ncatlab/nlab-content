
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

Let $M$ be a [[commutative monoid]]. A **$M$-graded monoid** $\Phi$ in a [[symmetric monoidal category]] $\mathcal{V}$ with [[unit object]] $I$ is the data of

* for each $m \in M$, an [[object]] $\Phi_m$,
* for each $m,n \in M$, a [[morphism]]
  $$\nabla_{n,m}: \Phi_m \otimes \Phi_n \to \Phi_{m+n} $$
* a morphism
  $$ \eta: I \to \Phi_0 $$
such that the obvious [[associativity]] and [[unit]] [[axioms]] hold.

Thus, a graded monoid is in particular a [[graded object]]. In fact, a graded monoid is just a [[monoid in a monoidal category|monoid]] in the monoidal category of graded objects of $\mathcal{V}$.

## Properties

* If $\Phi$ is a graded monoid, then $(\Phi_{0},\nabla_{0,0},\eta)$ is a monoid.
* If $\mathcal{V}$ is a symmetric monoidal category which is also a [[zero morphism|enriched over pointed sets]], and if $(A,\nabla,\eta)$ is a monoid in $\mathcal{V}$, then we get a $\mathbb{N}$-graded monoid $\Phi$ by defining:

  * $\Phi_{m} := A$ for every $m$
  * $\nabla_{0,0} := \nabla$
  * $\nabla_{m,n} := 0$ if $m \neq 0$ or $n \neq 0$

## Examples

* In the [[symmetric monoidal category]] of [[groups]] with the [[cartesian product]], two examples of $\mathbb{N}$-graded monoids are the trivial one $1 = (1)_n$ and the **graded monoid of symmetric groups** $\Sigma = (\Sigma_n)_n$.

* We say that a graded monoid has a trivial unit if :
  * $\eta$ is an isomorphism
  * $\nabla_{m,0}$ and $\nabla_{0,n}$ are isomorphisms for every $m,n \in M$. 

The two examples above in the category of groups have trivial units (by considering that $\Sigma_{0} = 1$).

## See also

* [[monoid object]]
* [[graded object]]
* [[graded comonoid]]
* [[graded bimonoid]]

[[!redirects graded unitary monoid]]
[[!redirects graded unital monoid]]