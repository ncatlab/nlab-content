
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Finite objects
* autmatic table of contents goes here
{:toc}

## Idea

A [[finite object]] in a [[category]] is a generalisation of the notion of [[finite set]] in [[Set|the category of sets]].

As there are already at least five distinct notions of finite set in [[constructive mathematics]], so there must be at least five distinct notions of finite object internal to a topos.  Additionally, the definitions may also be interpreted in an 'external' sense, giving even further notions.  Only some are mentioned below.

Also beware that the term 'finite object' is also used in a much more general sense to mean a [[compact object]].


## Definitions

The _external_ version of a "finite set" in the strictest sense is usually called a **finite cardinal**.  This is an object $[n]$ which is the pullback of $N_{\lt}\to N$ along some [[global element]] $n:1\to N$.  Here $N$ is a [[natural numbers object]] and $N_{\lt} \hookrightarrow N\times N$ is its strict order relation.  We can then consider [[subobject]]s, [[quotient object]]s, and [[subquotient object]]s of finite cardinals to obtain external versions of subfinite, finitely indexed, and subfinitely indexed sets.

The full subcategory of finite cardinals in any topos is again a topos, and it is [[Boolean topos|Boolean]].  Its [[subobject classifier]] is $2=1\sqcup 1$, which in the ambient topos is the classifier only of [[decidable object|decidable]] subobjects.  This means that classically valid arguments, including all of finitary combinatorics, can generally be applied easily to finite cardinals, as long as we always interpret "subset" to mean "decidable subset."

The _internal_ version of a "finite set" is an object $X$ such that "$X$ is a finite cardinal" is true in the internal logic.  This is equivalent to saying that $X$ is _locally_ isomorphic to a finite cardinal, i.e. there is an epimorphism $U\to 1$ and a [[generalized element]] $n:U\to N$ such that $U\times X \cong n^*(N_\lt)$ over $U$.  Equivalently, there is a $U\to 1$ such that $U\times X$ is a finite cardinal in the slice topos $S/U$.

Likewise, the internal version of "finitely indexed set" is one which is locally a quotient of a finite cardinal, and so on.  An "internally finitely indexed" object is generally called a _$K$-finite object_, and an "internally subfinitely indexed" one is called a _$\tilde{K}$-finite object_.  Since it is still provable in the internal logic that any decidable finitely indexed set is finite, the "internally finite" objects can be characterized as the _decidable $K$-finite objects_.

The decidable $K$-finite objects in any topos also form a Boolean topos whose subobject classifier is $2$; it can be regarded as the "[[stack]] completion" of the topos of finite cardinals.  The category of $K$-finite objects is a topos if and only if every $K$-finite object is decidable, and the category of $\tilde{K}$-finite objects is a topos if (but not only if) the subobject classifier is $K$-finite.


## Examples

* In any Boolean topos, all four internal notions coincide.  In a [[well-pointed topos]], each internal notion coincides with its external notion.  Therefore, in a well-pointed Boolean topos, including the topos [[Set]] as usually conceived, all notions of finiteness coincide.

* In a [[presheaf]] topos $[C^{op},Set]$, the finite cardinals are the finite-set-valued functors which are constant on each connected component.  In particular, if $C$ is a [[group]], then the topos of finite cardinals is equivalent to [[FinSet]].

* Likewise, in the [[Grothendieck topos]] $Sh(X)$ of [[sheaf|sheaves]] on a space $X$, the finite cardinals are the locally constant functions $X\to N$.  So if $X$ is connected, the topos of finite cardinals in $Sh(X)$ is also equivalent to $FinSet$.

* Examples of such are [[tiny object]]s and [[infinitesimal object]]s in sheaf toposes.

* By contrast, the $K$-finite objects in $[C^{op},Set]$ are the finite-set-valued functors each of whose transition functions is surjective, and the _decidable_ K-finite objects are the finite-set-valued functors each of whose transition functions is bijective.

* In particular, if $C$ is a groupoid, the topos of decidable $K$-finite objects is equivalent to $[C^{op},FinSet]$.  Since the topos of presheaves on a groupoid is Boolean, this gives an example of a Boolean topos in which the finite cardinals ("externally finite objects") and the (decidable) $K$-finite objects ("internally finite objects") fail to coincide.

* In $Sh(X)$, the decidable K-finite objects are those that are "locally finite;" i.e. there is an open cover of $X$ such that over each open in the cover, the sheaf is a locally constant function to $N$.  These are essentially the same as [[covering space|covering spaces]] of $X$.

+--{.query}
_Toby_: I think that I\'ll move the internal stuff to [[finite object]], to keep each page relatively short.

By the way, do I understand you correctly that 'finite object' in topos theory by default means 'decidable K-finite object'?

_Mike_: Okay (to the move).  To the question, I'm realizing more and more that I don't really have the background to be able to say what "topos theorists" say.  My only source for this material is the Elephant (and what I've been able to deduce on my own, which of course tells us nothing about terminology).  The Elephant never says "finite object" unqualified; only "finite cardinal" or "K-finite object" or "decidable K-finite object" or "$\tilde{K}$-finite object."  If "projective" means "externally projective," and likewise for "choice" and (maybe) "inhabited," then "finite object" should mean "finite cardinal," but I wouldn't use it that way myself out of fear of ambiguity and since "finite cardinal" means the same thing.  I don't see any objection to "internally finite object" meaning "decidable K-finite object," though.

=--


[[!redirects finite object]]
[[!redirects finite objects]]

[[!redirects finite]]