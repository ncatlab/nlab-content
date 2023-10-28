
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Bialgebra
* table of contents
{: toc}


## Idea

A _bialgebra_ (or bi[[gebra]]) is both an [[algebra]] and a [[coalgebra]], where the operations of either one are [[homomorphisms]] for the other. A bialgebra structure on an [[associative algebra]] is precisely such as to make its [[category of modules]] into a [[monoidal category]] equipped with a [[fiber functor]].


A bialgebra is one of the ingredients in the concept of [[Hopf algebra]].


## Definition

A **bialgebra** is a [[monoid]] [[internalization|in]] the category of [[coalgebra|coalgebras]].  Equivalently, it is a [[comonoid]] [[internalization|in]] the category of [[algebra|algebras]].  Equivalently, it is a monoid in the category of comonoids in [[Vect]] --- or equivalently, a comonoid in the category of monoids in [[Vect]].

More generally, a **[[bimonoid]]** in a monoidal category $M$ is a monoid in the category of comonoids in $M$ --- or equivalently, a comonoid in the category of monoids in $M$.  So, a bialgebra is a bimonoid in $Vect$.

## Properties

### Relation to sesquialgebras

Bialgebras are precisely those [[sesquialgebras]] $A$ whose product $A \otimes A$-$A$-[[bimodule]] is induced from an algebra [[homomorphism]] $A \to A \otimes A$ and whose unit $k$-$A$ bimodule is induced from an algebra homomorphism $A \to k$.

### Tannaka duality and categories of modules
 {#TannakDuality}

The structure of a bialgebra on an [[associative algebra]] equips its [[category of modules]] with the structure of a [[monoidal category]] and a monoidal [[fiber functor]]. In fact that construction is an equivalence. This is the statement of [[Tannaka duality]] for bialgebras. For instance ([Bakke](#Bakke))

[[!include structure on algebras and their module categories - table]]


## Examples

Notions of bialgebra with further structure notably include _[[Hopf algebras]]_ and their variants.

## Related concepts

* [[bimonoid]]

* [[Gerstenhaber-Schack cohomology]], [[bialgebra cocycle]], [[weak bialgebra]], [[bialgebroid]]

* [[Hopf algebra]]

* [[quasitriangular bialgebra]]

* [[sesquialgebra]]

* [[algebra]], [[module]]

* **bialgebra**,  [[2-module]]

* [[trialgebra]], [[3-module]]

## References

[[Tannaka duality]] for bialgebras

* {#Bakke} T&#248;rris Kol&#248;en Bakke, _Hopf algebras and monoidal categories_ (2007) ([pdf](http://munin.uit.no/bitstream/handle/10037/1084/finalthesis.pdf;jsessionid=C0D15EADBDC35E93D95D2DD090411004?sequence=1))
 

On [[bialgebras]] in [[locally presentable categories]]:

* [[Friedrich Ulmer]]. *Bialgebras in locally presentable categories*, University of Wuppertal preprint (1977) &lbrack;[pdf](/nlab/files/Bialgebras_in_locally_presentable_categories.pdf)&rbrack;



[[!redirects bialgebra]]
[[!redirects bialgebras]]
[[!redirects bigebra]]
[[!redirects bigebras]]
