
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Topologically complete spaces
* table of contents
{: toc}

## Idea

A [[topological space]] is topologically complete if and only if it is [[complete space|completely]] [[metrizable space|metrizable]].  However, the term 'topologically complete' may be applied to other [[spaces]] as well, and in this case it means that the [[underlying topological space]] is completely metrizable.

One can vary this by considering some other kind of underlying space (besides the underlying topological one) and other kinds of completability (besides complete metrizability).


## Definitions

### General

Let $C$, $M$, $S$, and $T$ be [[categories]], and suppose that we have [[functors]] $U\colon C \to M$, $V\colon M \to S$, and $W\colon S \to T$.  We will think of the [[objects]] of these categories as [[spaces]], and we\'ll think of these functors and their [[composites]] as [[forgetful functors]].  Also, we\'ll think of $C$ as a [[subcategory]] of $M$, and we\'ll think of the objects of $C$ as the _complete_ spaces in $M$.

The basic example to keep in mind is the case where $T$ is the category [[Top]] of [[topological spaces]] and [[continuous functions]], $M$ is the category [[Met]] of [[metric spaces]] and [[short functions]], and $C$ is the [[full subcategory]] of $Met$ consisting of the [[complete metric spaces]].  In the motivating example, $S$ is also $Met$, but this can remain flexible.  In any case, $U, V, W$ should all be standard forgetful functors.

Even in other situations, it should be that once you specify $M, S, T$, then $C, U, V, W$ should all be obvious.  Typically, $C, M, S, T$ will be [[concrete categories]], $U, V, W$ will be [[faithful functor|faithful]] [[isofibrations]], and $U$ will additionally be [[full functor|full]], but this doesn\'t really affect anything.

An object $X$ of $S$ is __$M$-izable__ if there is an object $Y$ of $M$ and an [[isomorphism]] in $S$ between $X$ and $V(Y)$.  $X$ is __completely $M$-izable__ if there is an object $Z$ of $C$ and an isomorphism in $S$ between $X$ and $V(U(Z)$.  $X$ is __$T$-ly $M$-izable__ if there is an object $Y$ of $M$ and an isomorphism in $T$ between $W(X)$ and $W(V(Y))$.  Finally, $X$ is __$T$-ly completely $M$-izable__ if there is an object $Z$ of $C$ and an isomorphism in $T$ between $W(X)$ and $W(V(U(Z)))$.  (If all functors are isofibrations, then we may without loss of generality require these $T$-isomorphisms to be [[equalities]], which is typically what is done in topology books.)

The actual terminology used will be based on terms for the objects of $M$ and $T$ rather than terms for $M$ and $T$ themselves; for example, in the standard example where $M$ is $Met$ and $T$ is $Top$, then we say that $X$ is __topologically completely metrizable__ (to mean that $X$ is $Top$-ly completely $Met$-izable).  $C, U, V, W$ are suppressed in the terminology because they are supposed to be obvious; $S$ is suppressed because you are supposed to know what it is when you first mention $X$.


### Special cases

A space $X$ (an object of $S$) is $M$-izable if and only if $X$ is $S$-ly $M$-izable; $X$ is completely $M$-izable iff $X$ is $S$-ly completely $M$-izable.  $X$ is [[complete space|complete]] iff $X$ is $S$-ly completely $S$-izable; $X$ is always $S$-ly $S$-izable.  Finally, $X$ is $T$-ly completely $M$-izable iff $X$ is $T$-ly $C$-izable.

A space is __topologically complete__ if it is topologically completely metrizable; this is the standard example above.  At least one reference ([Schechter 1997](#Schechter1997)) uses this term for a space that is topologically completely *pseudometrizable* (that is, $M$ is the category of [[pseudometric spaces]]).  According to Wikipedia, at least one reference ([Kelley 1955](#Kelley1955)) uses this term for a space that is topologically completely *uniformizable* (that is, $M$ is the category of [[uniform spaces]]).

A space is __Dieudonn&#233;-complete__ if it is topologically completely uniformizable.  At least one reference ([Arkhangel&#8242;skii 1977](#Ark1977)) uses this term for a space that is topologically completely *Hausdorff*-uniformizable (that is, $M$ is the category of of [[Hausdorff space|Hausdorff]] uniform spaces).


## Categories of complete spaces

If we consider the entire category of complete spaces in some sense, then $S$ must be specified explicitly; that is, we speak of the category of $T$-ly $M$-izable $S$-spaces or the category of $T$-ly completely $M$-izable $S$-spaces.  However, if $S$ is not specified, then we take it to be $T$ by default, so the $T$-ly [completely] $M$-izable spaces are the same as the [completely] $M$-izable $T$-spaces.  We consider these categories to be [[full subcategories]] of $S$.

Up to [[equivalence of categories|equivalence]] of categories, the category of $M$-izable $T$-spaces (aka the $T$-ly $M$-izable spaces, that is the $T$-ly $M$-izable $T$-spaces) is the category whose [[objects]] are taken from $M$ and whose [[morphisms]] are taken from $T$; similarly, the category of completely $M$-izable $T$-spaces has objects taken from $C$ and morphisms taken from $T$.

In particular, following our standard example, the category of topologically complete spaces (that is the category of completely metrizable toplogical spaces) may be taken to have complete metric spaces as objects and continuous functions as morphisms.


## References

*  A.V. Arkhangel&#8242;skii (1977).  _Complete space_.  Matematicheskaya entsiklopediya.  [Updated English version](https://www.encyclopediaofmath.org/index.php/Complete_space). 
   {#Ark1977}

*  [[John Kelley]] (1955).  _General Topology_, 1975.
   {#Kelley1955}

*  Eric Schechter (1997).  _[[Handbook of Analysis and its Foundations]]_, Section 20.12.
   {#Schechter1997}


[[!redirects topologically complete space]]
[[!redirects topologically complete spaces]]

[[!redirects Dieudonne complete space]]
[[!redirects Dieudonne complete spaces]]
[[!redirects Dieudonné complete space]]
[[!redirects Dieudonné complete spaces]]
[[!redirects Dieudonne-complete space]]
[[!redirects Dieudonne-complete spaces]]
[[!redirects Dieudonné-complete space]]
[[!redirects Dieudonné-complete spaces]]

[[!redirects complete topological space]]
[[!redirects complete topological spaces]]
