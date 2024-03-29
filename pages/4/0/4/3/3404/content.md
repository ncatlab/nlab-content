
# $Sup Lat$
* table of contents
{: toc}

## Definitions

__$Sup Lat$__ is the [[category]] whose [[objects]] are [[suplattices]] and whose [[morphisms]] are suplattice [[homomorphisms]], that is [[functions]] which preserve all [[joins]] (including the [[bottom element]]).  Analogously, __$Inf Lat$__ is the category whose objects are [[inflattices]] and whose morphisms are inflattice homomorphisms, which preserve all [[meets]].

Actually, $Sup Lat$ and $Inf Lat$ are [[equivalence of categories|equivalent]]; the difference between the two is merely the notational choice between $\leq$ and $\geq$.  However, this choice corresponds to using either of two [[inclusion functor]]s representing $Sup Lat$ and $Inf Lat$ as [[replete subcategories]] of [[Pos]]; similarly, [[CompLat]] can be viewed as a replete [[wide subcategory]] of $Sup Lat$ and $Inf Lat$ in two different ways.

One can write __$Comp Semi Lat$__ (meaning the category of [[complete semilattices]]) if one wishes to remain ambiguous about the notation.


## Properties

$Sup Lat$ is given by a [[variety of algebras]], or equivalently by an [[algebraic theory]], so it is an [[equationally presented category]]; however, it requires operations of arbitrarily large arity.  Nevertheless, it is a [[monadic category]] (over [[Set]]), because it has [[free objects]].  Specifically, the __free suplattice__ on a [[set]] $X$ is the [[power set]] $\mathcal{P}X$ of $X$ with the operation of [[union]]; an element $a$ of $X$ appears as the [[singleton subset]] $\{a\}$ in $\mathcal{P}X$.

The __free inflattice__ on $X$ is slightly less natural; of course, we can take it to be $\mathcal{P}X$ with the operation of union again, but then the order on the elements is the opposite of the usual order.  However, we can also take it to be $\mathcal{P}X$ with the operation of [[intersection]]; this uses the fact that [[complementation]] is an [[automorphism]] of $\mathcal{P}X$.  Then the generator $a$ appears as $X \setminus \{a\}$ in the lattice.

$Sup Lat$ is a [[monoidal category]]; it admits a [[tensor product]] which represents [[binary morphisms]]: functions which preserve joins separately in each variable.  A [[monoid object|monoid]] in $Sup Lat$ is a __[[quantale]]__, including [[frames]] as a special case.

In fact, $Sup Lat$ is even a [[star-autonomous category]], and *a fortiori* a [[linearly distributive category]].  The dual of a suplattice is its opposite poset, which is also a suplattice since every suplattice is also an inflattice.


## In weak foundations

For all practical purposes, $Sup Lat$ is not available in [[predicative mathematics]].  The definition goes through, but we cannot prove that $Sup Lat$ has any [[infinite set|infinite]] objects.  (More precisely, the [[power set]] of any nontrivial small suplattice must be small.)  Generally speaking, predicative mathematics treats infinite suplattices only as [[proper class|large]] objects.  Although they are of little interest, we can ask which of the facts above hold predicatively; the answer is that $Comp Lat$ is not wide as a subcategory of $Sup Lat$, and $Sup Lat$ is not monadic (since $\mathcal{P}X$ is generally large).

In impredicative [[constructive mathematics]], we cannot intepret $\mathcal{P}X$ with intersection as the free inflattice on $X$, since [[complementation]] is not an automorphism.  Everything else goes through, however, including the interpretation of $\mathcal{P}X$ with reverse inclusion as the free inflattice.  In particular, $Sup Lat$ (and hence $Inf Lat$) is still a monadic category.


category: category

[[!redirects Sup]]
[[!redirects SupLat]]
[[!redirects Sup Lat]]
[[!redirects Inf]]
[[!redirects InfLat]]
[[!redirects Inf Lat]]
[[!redirects CompSemiLat]]
[[!redirects Comp Semi Lat]]

[[!redirects free suplattice]]
[[!redirects free sup-lattice]]
[[!redirects free sup lattice]]
[[!redirects free inflattice]]
[[!redirects free inf-lattice]]
[[!redirects free inf lattice]]
[[!redirects free complete semilattice]]
