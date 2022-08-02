Let $M$ be a [[commutative monoid]]. A **$M$-graded monoid** $\Phi$ in a [[symmetric monoidal category]] $\mathcal{V}$ with [[unit object]] $I$ is the data of

* for each $m \in M$, an [[object]] $\Phi_m$,
* for each $m,n \in M$, a [[morphism]]
  $$ \Phi_m \otimes \Phi_n \to \Phi_{m+n} $$
* a morphism
  $$ I \to \Phi_0 $$
such that the obvious [[associativity]] and [[unit]] [[axioms]] hold.

Thus, a graded monoid is in particular a [[graded object]]. In fact, a graded monoid is just a [[monoid in a monoidal category|monoid]] in the monoidal category of graded objects of $\mathcal{V}$.

## Examples

* In the [[symmetric monoidal category]] of [[groups]] with the [[cartesian product]], two examples of $\mathbb{N}$-graded monoids are the trivial one $1 = (1)_n$ and the **graded monoid of symmetric groups** $\Sigma = (\Sigma_n)_n$.

## See also

* [[monoid object]]
* [[graded object]]
* [[graded comonoid]]
* [[graded bimonoid]]

[[!redirects graded unitary monoid]]
[[!redirects graded unital monoid]]