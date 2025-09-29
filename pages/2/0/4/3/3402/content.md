
# Complete boolean algebras
* table of contents
{: toc}

## Definition

A __complete Boolean algebra__ is a [[complete lattice]] that is also a [[Boolean algebra]].  Since lattice homomorphisms of Boolean algebras automatically preserves the Boolean structure, the complete Boolean algebras form a [[full subcategory]] [[CompBoolAlg]] of [[CompLat]].


## Category of complete Boolean algebras

A natural notion of [[morphism]] for complete Boolean algebras is that of a continuous homomorphism of Boolean algebras, also known as complete Boolean homomorphisms.
These can be defined as homomorphisms of Boolean algebras that preserve [[suprema]], or, equivalently, [[infima]].
It suffices to require preservation of [[suprema]] of [[directed subsets]].

With this notion of morphisms, complete Boolean algebras form a category.


## Relation to Stonean locales and Boolean locales

The category of complete Boolean algebras is equivalent
to the category of [[Boolean locales]]
and [[Stonean locales]].
The latter fact is also known as the (localic) __Stonean duality__.

In the presence of the [[axiom of choice]],
the category of [[Stonean locales]] is equivalent
to the category of [[Stonean spaces]],
so the latter is contravariantly equivalent to the category
of complete Boolean algebras.
The latter fact is also known as the (traditional) __Stonean duality__.


## Stonean duality

The [[Stone duality]] establishes a [[contravariant equivalence]]
of [[categories]] between the category of [[Boolean algebras]]
and the category of [[Stone spaces]].
The latter is a [[full subcategory]] of the category [[Top]]
of [[topological spaces]] and [[continuous maps]]
on [[compact]] [[totally disconnected]] [[Hausdorff]] [[topological spaces]].

Recall that a [[Stonean space]] is a [[compact]] [[extremally disconnected]]
[[Hausdorff]] [[topological space]].
[[Morphisms]] of [[Stonean spaces]] are defined to be [[open]] [[continuous maps]].
Restricting the [[Stone duality]] produces a [[contravariant equivalence]]
between the category of complete Boolean algebras
and the category of [[Stonean spaces]].
See Corollary 6.10(2) in [Bezhanishvili](#SDGC).


## CABAs

Assuming [[excluded middle]], complete *[[atomic Boolean algebra|atomic]]* Boolean algebras are (up to [[isomorphism]]) precisely [[power sets]].  In fact, taking power sets defines a [[fully faithful functor]] from the [[opposite category]] of [[Set]] to [[Comp Bool Alg]] whose [[essential image]] consists of the complete atomic boolean algebras.  See at _[Set -- Properties -- Opposite category](Set#OppositeCategory)_. These abstract representations of power sets are important enough to have their own abbreviation: 'CABA'.

This property of CABAs is not applicable in [[constructive mathematics]], where power sets are rarely boolean algebras.  However, we can use [[discrete space|discrete]] [[locales]] instead (or rather, their corresponding [[frames]]).  That is, define a __CABA__ to be (not a complete atomic boolean algebra but) a frame $X$ such that the locale maps $X \to 1$ and $X \to X \times X$ (which in the category of frames are maps $0 \to X$ and $X + X \to X$) are [[open map|open]] (as locale maps).  (Of course, that $X \to 1$ is open is the condition that $X$ is [[overt locale|overt]].)  Then it should be (I will check) a classical theorem that CABAs and complete atomic boolean algebras are the same, and a constructive theorem that CABAs and power sets are the same (in the same functorial manner as above). 

Relatedly, CABAs are the same as [[completely distributive lattice|completely distributive complete Boolean algebras]]. 

Another approach is via [[overlap algebra|overlap algebras]].  An overlap algebra is a [[frame]] with two extra conditions (one of which is [[overt locale|overtness]] of the corresponding [[locale]]).  Classically, overlap algebras are the same thing as complete Boolean algebras; constructively, atomic overlap algebras are the same thing as powersets.  See [Ciraulo 2010](#Ciraulo2010).


## Algebraicity 

Complete Boolean algebras are the models of an [[algebraic theory]] (in which the operations, notably $j$-indexed [[suprema]] and infima, have arities $j$ unbounded by any cardinal). It follows from general principles that the underlying-set functor $U: CompBoolAlg \to Set$ preserves and reflects limits and isomorphisms. 

However, this functor $U$ is _not_ [[monadic functor|monadic]]; in fact, it does not even possess a left adjoint. Indeed, while the free complete Boolean algebra on a _finite_ set $X$ exists and coincides with the free Boolean algebra on $X$ (it is finite, being isomorphic to the double power set $P(P X)$), we have 

+-- {: .un_theorem}
###### Theorem (Gaifman-Hales; Solovay) 
There is no free complete Boolean algebra on countably many generators. 
=-- 

As a consequence, $CompBoolAlg$ is not cocomplete (otherwise there would exist a countable coproduct of copies of $P(P 1)$, which is ruled out by the previous theorem). 


## Related concepts

* [[Boolean locale]]
* [[Stonean locale]]
* [[completely distributive lattice]] 
* [[sigma-complete Boolean algebra|$\sigma$-complete Boolean algebra]]

## References

For instance around theorem 2.4 of 

* [[Jaap van Oosten]], _Basic category theory_ ([pdf](http://www.staff.science.uu.nl/~ooste110/syllabi/catsmoeder.pdf))

and

* PlanetMath, _[representing a complete atomic Boolean algebra by power set](https://planetmath.org/representingacompleteatomicbooleanalgebrabypowerset)_

The [[Stone duality]] for complete Boolean algebras is explained in

*  [[Guram Bezhanishvili]],
_Stone duality and Gleason covers through de Vries duality_.
Topology and its Applications 157 (2010), 1064--1080.    
{#SDGC}

For overlap algebras, see

*  [[Francesco Ciraulo]], 2010.  _The Role of the Overlap Relation in Constructive Mathematics_.  [Slides](https://www.math.unipd.it/~ciraulo/documents/Ciraulo%20Chiemsee%202010.pdf).
{#Ciraulo2010} 


[[!redirects complete Boolean algebra]]
[[!redirects complete boolean algebra]]
[[!redirects complete Boolean algebras]]
[[!redirects complete boolean algebras]]
[[!redirects complete Boolean lattice]]
[[!redirects complete boolean lattice]]
[[!redirects complete Boolean lattices]]
[[!redirects complete boolean lattices]]
[[!redirects complete Boolean ring]]
[[!redirects complete boolean ring]]
[[!redirects complete Boolean rings]]
[[!redirects complete boolean rings]]

[[!redirects complete atomic Boolean algebra]]
[[!redirects complete atomic boolean algebra]]
[[!redirects complete atomic Boolean algebras]]
[[!redirects complete atomic boolean algebras]]
[[!redirects complete atomic Boolean lattice]]
[[!redirects complete atomic boolean lattice]]
[[!redirects complete atomic Boolean lattices]]
[[!redirects complete atomic boolean lattices]]
[[!redirects complete atomic Boolean ring]]
[[!redirects complete atomic boolean ring]]
[[!redirects complete atomic Boolean rings]]
[[!redirects complete atomic boolean rings]]
[[!redirects caba]]
[[!redirects CABA]]
[[!redirects cabas]]
[[!redirects CABAs]]
[[!redirects caba's]]
[[!redirects CABA's]]
[[!redirects caba’s]]
[[!redirects CABA’s]]
[[!redirects caba\'s]]
[[!redirects CABA\'s]]
