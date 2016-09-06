
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

# Localizable measures
* table of contents
{: toc}

## Idea

Many of the important theorems of [[measure theory]] fail to hold in full generality.  (See below under Theorems for which theorems we\'re talking about.)  Often these theorems are stated for $\sigma$-[[sigma-finite measures|finite measures]], but they do hold a bit more generally than that.  In fact, they hold for _localizable_ measures, and this fact *characterizes* the localizable measures.


## Definition

The following definition is in elementary terms; but we will see that there are many other characterizations.

Let $\mu$ be a [[positive measure]] on an [[abstract set]] $X$.  (That is, certain [[subsets]] of $X$, forming a $\sigma$-[[sigma-algebra|algebra]], are [[measurable set|measurable]] by $\mu$, and $\mu$ maps these sets to the space $[0,\infty]$ of [[lower real numbers]] in a [[monotone function|monotone]] and [[countably additive measure|countably additive]] way.)

Given two measurable subsets $E$ and $F$, $E$ __essentially contains__ $F$ if the set
$$ \{ x\colon X \;|\; x \in F \;\Rightarrow\; x \in E \} $$
is [[full set|full]]; or equivalently (using [[excluded middle]]) if $F \setminus E$ is [[null set|null]].  (This is a [[preorder]] on the measurable sets.)

Then $\mu$ is __localizable__ if the following conditions both apply:

*  Semifiniteness:  Every measurable set $E$ with positive measure essentially contains a measurable set with finite positive measure.  (We may strengthen 'essentially contains' to 'contains' in this clause.)

*  Essential suprema:  Given any collection $\mathcal{C}$ of measurable sets, there is a measurable set $E$ such that:

   *  $E$ essentially contains each element of $\mathcal{C}$; and
   *  Given any measurable set $F$ that essentially contains every element of $\mathcal{C}$, $F$ essentially contains $E$.

   (This set $E$ is essentially unique, in that it essentially contains and is essentially contained in any other set with the same property; we call $E$ [[the]] __essential union__ $\ess \bigcup \mathcal{C}$ of $\mathcal{C}$.)

We generalize to [[measures]] taking place in some space other than $[0,\infty]$: a $\mu$ is __localizable__ if ${|\mu|}$ is, as long as $\mu$ has an [[absolute value]] (or [[total variation]]) ${|\mu|}$ that takes values in $[0,\infty]$.

Of course, a set equipped with a localizable measure is a __localizable measure space__.


## Examples

Every $\sigma$-[[sigma-finite measure|finite]] measure is localizable.  (Since this includes so many examples, the theorems below are often stated for $\sigma$-finite measures.)

Any [[counting measure]] is localizable (but $\sigma$-finite only on a [[countable set]]).


## Properties

The following [[sheaf]] condition is fundamental:  Given any [[cover]] $\mathcal{U}$ of $X$ (a localizable measure space) by [[measurable sets]] and a $\mathcal{U}$-indexed [[family]] $f$ of [[partial function|partial]] [[measurable functions]] (with $\dom f_A = A$), if always $f_A = f_B$ almost everywhere on $A \cap B$ (meaning that there is a [[full subset]] $E$ of $X$ such that $f_A = f_B$ on $A \cap B \cap E$), then there exists a (necessarily unique up to [[almost equality]]) measurable (and total) function $\ess \bigcup f$ such that always $\ess \bigcup f = f_A$ almost everywhere on $A$.  (This is Theorem 213N in [Fremlin](#Fremlin).  I don\'t know if it characterizes localizable measures.)

Slightly more generally, start with *any* family of partial measurable functions on $X$ and treat it as a cover of (any representative of) the essential union of its domains.

... other results such as the [[Radon–Nikodym theorem]] ...

These ideas are elaborated at [[measurable space]] [[Boolean toposes]] and [[Boolean valued model]]s and [[forcing]].

## Other localizable structures

Whether a semifinite measure $\mu$ is localizable depends only on which measurable sets are [[full set|full]] (or [[null set|null]]).  Sometimes it is convenient to equip a [[measurable space]] with a $\delta$-[[delta-filter|filter]] of full sets (or a $\sigma$-[[sigma-ideal|ideal]] of null sets), without equipping it with the measure of any other set.  A __localizable measurable space__ is a measurable space so equipped, such that every collection of measurable sets has an essential union.  (It is a theorem, I believe, that every localizable measurable space is capable of supporting a semifinite, hence localizable, measure with the same full/null sets.)

Knowing the full/null sets is also sufficient to define [[almost equality]] of [[measurable functions]] between measurable spaces; this gives us a [[category]] $Loc Meas$ of localizable measurable spaces.  This category is [[dual category|dual]] to the category of [[commutative ring|commutative]] [[von Neumann algebras]]; hence an arbitrary von Neumann algebra may be viewed as a _noncommutative_ localizable measurable space (in the sense of [[noncommutative geometry]]).

If $\mathcal{M}$ is the $\sigma$-[[sigma-algebra|algebra]] of measurable sets and $\mathcal{F}$ is the $\delta$-filter of full sets (or $\mathcal{N}$ is the $\sigma$-ideal of null sets), then we may form the [[quotient ring|quotient]] [[boolean algebra]] $\mathcal{M}/\mathcal{F}$ (or $\mathcal{M}/\mathcal{N}$) by identifying each full set with the [[improper subset|entire space]] (or identifying each null set with the [[empty subset|empty set]]).  Then a measurable space is localizable iff this quotient is [[complete boolean algebra|complete]]; this is the real point of the notion of localizability.

This boolean algebra is all the structure needed to specify a measure on the original space (at least one that is [[absolutely continuous measure|absolutely continuous]] in that it has at least the requisite full/null sets).  We can now abstract away the [[underlying set]] and simply look at the complete boolean algebra.  However, it is *not* true that every complete boolean algebra is capable of arising in this way from a measurable space.  Those which do so arise may be called __[[measurable locales]]__, since a complete boolean algebra is a [[frame]] and measurable functions (up to almost equality) between the measurable spaces correspond to [[continuous maps]] between the frames, thought of as [[locales]].  (That is, $Loc Meas$ is [[equivalence of categories|equivalent]] to $Meas Loc$, a sort of pun.)

Without requiring localizability, the boolean algebra $\mathcal{M}/\mathcal{F}$ (or $\mathcal{M}/\mathcal{N}$) is called a [[measurable algebra]]; equipped with a measure, we have a [[measure algebra]].  Thus a measurable locale is the same thing as a __localizable measurable algebra__, and one may also speak of __localizable measure algebras__ (with the category of these equivalent to the category localizable measure spaces, so long as morphisms in the latter are again only defined up to almost equality).


## In weak foundations

The [[axiom of choice]] is indispensable for the development above, as stated.  (The reason is that one constantly makes choices among essentially equivalent measurable sets, or among almost equal measurable functions.)  However, the [[category]] of localizable measurable spaces (and [[measurable functions]] up to [[almost equality]]) is (assuming choice) [[equivalence of categories|equivalent to]] the category of [[measurable locales]], which may prove to be more tractable without choice, even in [[constructive mathematics]].  That said, nobody has worked out a constructive development of this yet.  (In particular, identifying which boolean algebras we want is more difficult; perhaps surprisingly, they are still boolean, but they are no longer necessarily complete!)


## References

This giant treatise on all of [[measure theory]] is free (in both senses) online:

*  D.H. Fremlin, _Measure Theory_, [web](http://www.essex.ac.uk/maths/people/fremlin/mt.htm)
   {#Fremlin}


[[!redirects localizable measure]]
[[!redirects localizable measures]]
[[!redirects localisable measure]]
[[!redirects localizable measures]]

[[!redirects localizable measure space]]
[[!redirects localizable measure spaces]]
[[!redirects localisable measure space]]
[[!redirects localizable measure spaces]]

[[!redirects localizable measurable space]]
[[!redirects localizable measurable spaces]]
[[!redirects localisable measurable space]]
[[!redirects localisable measurable spaces]]

[[!redirects localizable measure algebra]]
[[!redirects localizable measure algebras]]
[[!redirects localisable measure algebra]]
[[!redirects localisable measure algebras]]
