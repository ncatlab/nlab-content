__$Comp Lat$__ is the [[category]] whose [[objects]] are [[complete lattices]] and whose [[morphisms]] are complete lattice [[homomorphisms]], that is [[functions]] which preserve all [[joins]] and [[meets]] (including the [[bottom]] and [[top]] elements).  $Comp Lat$ is a [[subcategory]] of [[Pos]].

$Comp Lat$ is given by a [[variety of algebras]], or equivalently by an [[algebraic theory]], so it is an [[equationally presented category]]; however, it requires operations of arbitrarily large arity.  In fact, it is *not* a [[monadic category]] (over [[Set]]), because it lacks some [[free objects]].  Specifically, the __free complete lattice__ on a [[set]] $X$, while it exists (by general abstract nonsense) as a [[class]], is small only if $X$ has at most $2$ elements (in which case it is finite and equals the [[free lattice]] on $X$).


## In weak foundations

For all practical purposes, $Comp Lat$ is not available in [[predicative mathematics]].  The definition goes through, but we cannot prove that $Comp Lat$ has any [[infinite set|infinite]] objects.  (More precisely, the [[power class]] of a nontrivial small complete boolean algebra must also be small.)  Generally speaking, predicative mathematics treats infinite complete lattices only as [[proper class|large]] objects.

In impredicative [[constructive mathematics]], it no longer holds that the free complete lattice on a set with at most $2$ elements equals the free lattice on that set.  In particular, the free complete lattice on the [[empty set]] is the set of [[truth values]], while the free lattice on the empty set is the set $\{\bot, \top\}$ of decidable truth values.  (I\'m not sure whether the free complete lattice on $1$ or $2$ elements is even small.)

In predicative constructive mathematics, even the free complete lattice on the empty set is a proper class.


category: category

[[!redirects CompLat]]
[[!redirects Comp Lat]]

[[!redirects free complete lattice]]