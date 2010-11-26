__$Bool Alg$__ is the [[category]] whose [[objects]] are [[boolean algebras]] and whose [[morphisms]] are lattice [[homomorphisms]], that is [[functions]] which preserve finitary [[meets]] and [[joins]] (equivalently, binary meets and joins and the [[top]] and [[bottom]] elements); it follows that the homomorphisms preserve [[negation]].  $Bool Alg$ is a [[subcategory]] of [[Pos]], in fact a [[replete subcategory]] of both [[DistLat]] and [[HeytAlg]].

$Bool Alg$ is given by a finitary [[variety of algebras]], or equivalently by a [[Lawvere theory]], so it has all the usual properties of such categories.  The __[[free object|free]] boolean algebra__ on a [[set]] $X$ is the __double [[power set]]__ $\mathcal{P}\mathcal{P}X$ of $X$[^1]; an element $a$ of $X$ is interpreted as the set of all those [[subsets]] of $X$ to which $a$ belongs, and the boolean algebra operations on the [[intersection]] and [[union]] as usual.

In [[constructive mathematics]], we do not use the entire power set but instead use (both times) only the [[decidable subsets]] of $X$.  Thus, the free boolean algebra on $X$ is $\mathcal{P}_{dec}\mathcal{P}_{dec}X$, which may more simply be written as $2^{2^X}$ (which is also a good notation classically).  In [[predicative mathematics]], the same argument shows that the free boolean algebra exists if we allow [[function sets]], although even this is not allowed in strongly predicative foundations.

[^1]: Adding this as a footnote because I am a complete newbie in editing n-Lab pages; anyway, is this assertion correct? For a finite set $X$, the free Boolean algebra is indeed the double power set, but I have my doubts that this is true for a general set. My (informal) reasoning is as follows: Boolean algebras are Boolean commutative rings, so by general arguments, to construct the free Boolean algebra, you construct first the free commutative ring and then quotient it to make it Boolean. Now the free commutative ring is just the ring of polynomials with integer coefficients. If you quotient by the idempotent relation, then you get polynomials with coefficients in the (unique) Boolean field and with all exponents $1$. But a straight comparison via the singleton inclusion, shows that this set is much smaller than the double power set. Can anyone correct, either me or the page?

category: category

[[!redirects BoolLat]]
[[!redirects Bool Lat]]
[[!redirects BoolAlg]]
[[!redirects Bool Alg]]
[[!redirects BoolRing]]
[[!redirects Bool Ring]]

[[!redirects free boolean algebra]]
[[!redirects free Boolean algebra]]
[[!redirects free boolean lattice]]
[[!redirects free Boolean lattice]]
[[!redirects free boolean ring]]
[[!redirects free Boolean ring]]

[[!redirects double powerset]]
[[!redirects double power set]]