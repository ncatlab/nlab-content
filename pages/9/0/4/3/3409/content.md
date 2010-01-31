__$Comp Bool Alg$__ is the [[category]] whose [[objects]] are [[complete boolean algebras]] and whose [[morphisms]] are complete lattice [[homomorphisms]], that is [[functions]] which preserve all [[joins]] and [[meets]] (including the [[bottom]] and [[top]] elements); it follows that they preserve the boolean [[negation]] operation.  $Comp Bool Alg$ is a [[subcategory]] of [[Pos]].


## Properties

$Comp Bool Alg$ is given by a [[variety of algebras]], or equivalently by an [[algebraic theory]], so it is an [[equationally presented category]]; however, it requires operations of arbitrarily large arity.  In fact, it is *not* a [[monadic category]] (over [[Set]]), because it lacks some [[free objects]].  Specifically, the __free boolean algebra__ on a [[set]] $X$, while it exists (by general abstract nonsense) as a [[class]], is small only if $X$ is [[finite set|finite]] (in which case it is finite and equals the [[free boolean algebra]] $2^{2^X}$ on $X$).


## In weak foundations

For all practical purposes, $Comp Bool Alg$ is not available in [[predicative mathematics]].  The definitions go through, but we cannot prove that it has any [[infinite set|infinite]] objects.  (More precisely, the [[power class]] of a nontrivial small complete boolean algebra must also be small.)  Generally speaking, predicative mathematics treats infinite complete boolean algebras only as [[proper class|large]] objects.

In impredicative [[constructive mathematics]], it no longer holds that the free complete boolean algebra on a finite set equals the free boolean algebra on that set.  In particular, the free complete boolean algebra on the [[empty set]] is the set of [[truth values]], while the free boolean algebra on the empty set is the set $\{\bot, \top\}$ of decidable truth values.  (I\'m not sure whether the free complete boolean algebra a positive finite number of elements is even small.)

In predicative constructive mathematics, even the free complete boolean algebra on the empty set is a proper class.


category: category

[[!redirects CompBoolAlg]]
[[!redirects Comp Bool Alg]]
[[!redirects CompBoolLat]]
[[!redirects Comp Bool Lat]]
[[!redirects CompBoolRing]]
[[!redirects Comp Bool Ring]]

[[!redirects free complete boolean algebra]]
[[!redirects free complete Boolean algebra]]
[[!redirects free complete boolean lattice]]
[[!redirects free complete Boolean lattice]]
[[!redirects free complete boolean ring]]
[[!redirects free complete Boolean ring]]