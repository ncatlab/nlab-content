
# Essentially bounded functions
* table of contents
{: toc}

## Definition

Let $X$ be a [[measure space]], or at least a [[measurable space]] equipped with a $\delta$-[[delta-filter|filter]] of [[full sets]] (or a $\sigma$-[[sigma-ideal|ideal]] of [[null sets]]).  Let $Y$ be a [[bornological set]].

A [[function]] from $X$ (or from a full subset of $X$) to $Y$ is __essentially bounded__ if it is [[almost equal]] to a [[bounded function]] from $X$ to $Y$.  That is, for some full subset $E$ of $X$, the [[direct image]] $f(E)$ is a [[bounded subset]] of $Y$.  (Here we equip $X$, and indeed equip every full subset of $X$, with the [[final structure|trivial bornology]] according to which every set is bounded.)

If $Y$ also has the structure of a measurable space, then we typically require an essentially bounded function to be [[measurable function|measurable]], although technically this is an independent property.  (We can always equip $Y$ with the [[final structure|trivial measurable structure]] according to which only the [[empty subset]] and the [[improper subset]] are measurable; then every function to $Y$ is measurable.)

The [[quotient set]] of essentially bounded measurable functions from $X$ to $Y$ modulo [[almost equality]] is denoted $L^\infty(X,Y)$.  With $L^\infty(X)$, we typically take $Y$ to be the [[real line]] equipped with the [[Borel-measurable sets]], or occasionally the [[complex plane]].  With $L^\infty$, we typically take $X$ to be the real line equipped with the [[Lebesgue-measurable sets]].


## Properties

Given any measure space $X$, $L^\infty(X,\mathbb{R})$ and $L^\infty(X,\mathbb{C})$ are (real and complex) [[Lebesgue spaces]] with $p = \infty$, hence [[Banach spaces]].  In fact, they are [[Banach algebras]], indeed $C^*$-[[C-star-algebras|algebras]].  At least when $X$ is [[localizable measure space|localizable]], they are in fact $W^*$-[[W-star-algebra|algebras]].  (Note that the [[involution]] $*$ is trivial when the target is $\mathbb{R}$.)  Of course, they are [[commutative algebra|commutative]]; $L^\infty(X,\mathbb{R})$ may also be viewed as an associative [[JB-algebra]] (thus a [[JBW-algebra]] if $X$ is localizable).

Conversely, every commutative complex $W^*$-algebra is, up to [[isomorphism]] of $W^*$-algebras, of the form $L^\infty(X,\mathbb{C})$ for some localizable measure space $X$; the same goes for $L^\infty(X,\mathbb{R})$ and commutative real $W^*$-algebras with trivial involution.  In fact, we have more: a [[dual equivalence]] between the [[category]] of localizable measure spaces (or rather, [[localizable measurable spaces]], as the [[morphisms]] ---taken up to almost equality, of course--- need not respect the measure, except for the full and null sets) and the category of commutative complex $W^*$-algebras (or the category of commutative real $W^*$-algebras with trivial involution, or the category of associative real $JBW$-algebras).


## Uselessness

Arguably, we do not need the concept of essentially bounded function; it is sufficient to consider bounded [[partial functions]] with full domains, that is [[almost functions]].  Traditionally, [[measure theory]] uses [[total functions]], but it cares about them only up to [[almost equality]], so almost functions are a natural concept.  In [[constructive analysis]], one must use almost functions, since then not every partial function can necessarily be extended to a total function.

Nevertheless, essentially bounded functions are traditional.


[[!redirects essentially bounded function]]
[[!redirects essentially bounded functions]]
[[!redirects essentially-bounded function]]
[[!redirects essentially-bounded functions]]
