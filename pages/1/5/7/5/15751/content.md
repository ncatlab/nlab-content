+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **nuclear object** is a categorical generalization of the concept of a finite-dimensional vector space, or more generally, a finite-dimensional object.

## Definition

### In a symmetric monoidal closed category

A _nuclear object_in a [[symmetric monoidal closed category]] $\mathcal{M}$ with unit $k$ is an object $A$ such that the canonical morphism $\phi _A:A\otimes A^*\to [ A, A]$ with $A^*:=[A,k]$ is an isomorphism.

A _morphism_ $f:A\to B$ is called _nuclear_ if there exists a morphism $p:k\to B\otimes A^*$ such that

$$\array{k & \overset{p}{\to} & B\otimes A^*\\
  n(f)\searrow && \swarrow\phi\\
  & [A,B] & }$$

is commutative, where $n(f)$, the name of $f$, obtains via adjointness from $k\otimes A\simeq A\overset{f}{\to} B$.

### In a linearly distributive category

In [CS'99](#CockettSeely99), Cockett and Seely generalize the above notion to [[linearly distributive categories]].

## Properties

* $A$ is nuclear precisely if $id_A$ is nuclear.

* If $A$ is nuclear then the canonical map to the double dual $\theta _A: A\to A^{**}$ is an isomorphism.

* The full subcategory $nuc(\mathcal{M})$ of nuclear objects is symmetric monoidal closed.

* $A$ is nuclear precisely if $A^*$ is nuclear.

* In a cartesian monoidal $\mathcal{M}$ only $1$ is nuclear.

* If $A$ is nuclear there exists a natural [[trace]] morphism $t_A:[A,A]\simeq A\otimes A^*\simeq A^*\otimes A \to k$.

## Examples

* Nuclear objects in the category of complete semilattices are precisely the [[completely distributive lattices]], or in absence of the [[axiom of choice]], more generally, the _constructively completely distributive lattices_ (Higgs&Rowe 1989, Rosebrugh&Wood 1994).

* Nuclear objects in the category of pointed sets are precisely the pointed sets with cardinality $\leq 2$.

* Nuclear objects in the category of [[Banach spaces]] with morphisms the bounded maps are the [[nuclear spaces]] (Rowe 1988).


## Related concepts

* [[nucleus of a profunctor]]

* [[completely distributive lattice]]

* [[nuclear space]]

* [[self-dual object]]

* [[dualizable object]]

* [[trace]]

## References

* D. A. Higgs, K. A. Rowe, _Nuclearity in the category of complete semilattices_ , JPAA **57** no.1 (1989) pp.67-78.

* R. Rosebrugh, R. J. Wood, _Constructive complete distributivity IV_ , App. Cat. Struc. **2** (1994) pp.119-144. ([preprint](http://www.mta.ca/~rrosebru/articles/ccd4.pdf))

* K. A. Rowe, _Nuclearity_ , Canad.Math.Bull. **31**  no.2 (1988) pp.227-235. ([pdf](http://cms.math.ca/cmb/v31/cmb1988v31.0227-0235.pdf))

* G. N. Raney, _Tight Galois Connections and Complete Distributivity_ , Trans.Amer.Math.Soc **97** (1960) pp.418-426. ([pdf](http://www.ams.org/journals/tran/1960-097-03/S0002-9947-1960-0120171-3/S0002-9947-1960-0120171-3.pdf))

For the generalization to [[linearly distributive categories]]:

* {#CockettSeely99} [[J. R. B. Cockett]] and [[R. A. G. Seely]], _Linearly distributive functors_, Journal of Pure and Applied Algebra 143 (1999) 155–203, [doi:10.1016/S0022-4049(98)00110-8](https://doi.org/10.1016/S0022-4049%2898%2900110-8)

[[!redirects nuclear objects]]