
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The **torsion subgroup** of a [[group]] is the [[subgroup]] of all those elements $g$, which have finite [[order]], i.e. those for which $g^n = e$ for some $n \in \mathbb{N}$.

A group is **torsion-free** if there is no such element apart from the neutral element $e$ itself, i.e. when the torsion subgroup is trivial.

Given a [[ring]] $R$, an element $m$ in an $R$-[[module]] $M$ is **torsion element** if there is a nonzero element $r$ in $R$ such that $r m=0$. A **[[torsion module]]** is a module whose elements are all torsion. A [[torsion-free module]] is a module whose elements are not torsion, other than $0$. 

Torsion and torsion-free classes of objects in an [[abelian category]] were introduced axiomatically as a [[torsion theory]] (or torsion pair) in ([Dickson](#Dickson)).

Notice that there are other, completely independent, concepts referred to as _[[torsion]]_. See there for more.

## Properties

### Relation to the $Tor$-functor

+-- {: .num_prop}
###### Proposition

For $A$ an [[abelian group]], its torsion subgroup is isomorphic to the value of the degree-1 [[Tor|Tor functor]] $Tor^\mathbb{Z}_1(\mathbb{Q}/\mathbb{Z}, A)$. 

=--

See at _[Tor - relation to torsion subgroups](Tor#RelationToTorsionGroups)_ for more.

### Relation to flatness

+-- {: .num_prop}
###### Proposition

An [[abelian group]] is torsion-free precisely if regarded as a $\mathbb{Z}$-[[module]] it is a [[flat module]].

=--

This is a special case of a [more general result](http://ncatlab.org/nlab/show/principal+ideal+domain#flat) for modules over a principal ideal domain. See also _[flat module - Examples](flat+module#Examles)_ for more.


## Examples and applications 

* In [[rational homotopy theory]] one considers the [[homotopy group]]s $\pi_n(X)$ of [[topological space]]s $X$ tensored over $\mathbb{Q}$: the resulting groups $\pi_n(X) \otimes_{\mathbb{Z}} \mathbb{Q}$ are then necessarily torsion-free -- in this sense [[rational homotopy theory]] studies spaces "up to torsion".

* The torsion elements of an [[elliptic curve]] as a group are important in number theory and arithmetic geometry. See [[torsion points of an elliptic curve]].

## Related concepts

* [[torsion-free module]]

* [[p-torsion]]

* [[torsion approximation]]

* [[Pontryagin duality for torsion abelian groups]]

* [[Bockstein homomorphism]]

## References

* {#Dickson} S. E. Dickson, _Torsion theories for abelian categories_,
Thesis, New Mexico State University (1963).
 


[[!redirects torsion subgroup]]
[[!redirects torsion subgroups]]

[[!redirects torsion group]]
[[!redirects torsion groups]]
[[!redirects torsion element]]
[[!redirects torsion elements]]


[[!redirects torsion-free group]]
[[!redirects torsion-free abelian group]]
[[!redirects torsion-free groups]]
[[!redirects torsion-free abelian groups]]