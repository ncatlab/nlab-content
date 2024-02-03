
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Countable sets
* table of contents
{: toc}

## Idea

Let $S$ be any [[set]], and let $\mathbf{N}$ be the [[set]] of [[natural number]]s.  Let $|S|$ be the [[cardinality]] of $S$, and let $\aleph_0$ be the cardinality of $\mathbf{N}$.

Then $S$ is:

*  __denumerable__ if ${|S|} = \aleph_0$,
*  __countable__ if ${|S|} \leq \aleph_0$, and
*  __uncountable__ if ${|S|} \gt \aleph_0$.

Note that the first two terms are not entirely standardised; some authors use them interchangeably for one or the other concept.


## Definitions

If you accept the [[axiom of choice]], then there is really nothing more to say than what was above.  In weaker [[foundations]], more care may be needed.  The following definitions should be more than enough for practical use in [[constructive mathematics]]:

* A [[set]] $S$ is __denumerable__ if there exists a [[bijection]] between $S$ and $\mathbf{N}$; or in other words if $S$ is the same as $\mathbf{N}$ [[up to isomorphism]] in [[Set]].
* $S$ is __denumerably indexed__ if there exists a [[surjection]] to $S$ from $\mathbf{N}$ (or equivalently any denumerable set); or in other words if $S$ a [[quotient set]] of a $\mathbf{N}$, up to isomorphism. 
* $S$ is __split denumerably indexed__ if there exists a [[split surjection]] to $S$ from $\mathbf{N}$. 
* $S$ is __countable__ if there exists a bijection between $S$ and a [[detachable subset|detachable]] [[lower subset]] of $\mathbf{N}$. 
* $S$ is __countably indexed__ if there exists a [[surjection]] to $S$ from a countable set. 
* $S$ is __split countably indexed__ if there exists a [[split surjection]] to $S$ from a countable set. 
* $S$ is __subcountable__ (or _subdenumerable_) if there exists an [[injection]] from $S$ to a countable set, or equivalently to a denumerable set; or in other words if $S$ is a [[subset]] of $\mathbf{N}$, up to isomorphism.
* $S$ is __subcountably indexed__ (or _subdenumerably indexed_) if $S$ is a [[subquotient]] of $\mathbf{N}$, up to isomorphism. 
* $S$ is __split subcountably indexed__ (or _split subdenumerably indexed_) if there exists a [[split surjection]] to $S$ from a subcountable set, or equivalently if there exists an [[injection]] from $S$ to a split countably indexed set or equivalently to a split denumerably indexed set. 
* $S$ is __uncountable__ if, given any [[function]] $f$ from a detachable subset of $\mathbf{N}$ to $S$, the function is strongly non-surjective in the sense that there exists an element of $S$ that is not in the [[image]] of $f$.

Of course, the terms are even less standardised here.  Certainly it is common for 'countable' to mean countably indexed, and yet it may also (as in classical mathematics) mean denumerable.  In at least some contexts, 'enumerable' (without the initial 'd') means denumerably indexed. 

Not only does the difference between 'denumerable' and 'countable' disappear when we add the prefix 'sub' (for obvious reasons), but it almost disappears when we add the suffix 'ly indexed'!  Specifically, a set is denumerably indexed if and only if it is both [[inhabited set|inhabited]] and countably indexed; and a set is countably indexed if and only if it is either [[empty set|empty]] or denumerably indexed.  That countability involves *lower* subsets of $\mathbb{N}$ is also almost irrelevant here; any *inhabited* detachable subset of $\mathbb{N}$ is denumerably indexed regardless of its closure under order.

On the other hand, it is key that countability involves *detachable* subsets of $\mathbb{N}$, so that not every subcountable set is necessarily countable (or even countably indexed).  Indeed, the set of [[computable numbers]] is subcountably indexed, while the set of [[real numbers]] is uncountable (and thus not countably indexed); yet in [[Russian constructivism]], these are the same set!  One reason to focus on countably indexed sets is that this is about the most general concept that definitely does *not* hold of the set of real numbers.

In addition, in the presence of [[countable choice]], the difference between *denumerably indexed* and *split denumerably indexed*, *countably indexed* and *split countably indexed*, and *subcountably indexed* and *split subcountably indexed* disappear, since every surjection out of $\mathbb{N}$ and every subset of $\mathbb{N}$ has a [[section]] by [[countable choice]]. 

Under the [[BHK interpretation]] of constructive mathematics, one only has the split versions of denumerably indexed, countably indexed, subcountably indexed. 

There is a lot of freedom in defining uncountability.  You can start with countable or countably indexed sets and require that any function from them to $S$ be non-surjective (in the strong sense used in the definition above).  Or you can start with denumerable or denumerably indexed sets and require that any function from them to $S$ be non-surjective, then add the additional clause that $S$ must be [[inhabited set|inhabited]].  Or you can compromise, and start with a detachable subset of $\mathbb{N}$ without requiring it to be a lower subset, since this is enough to prove $S$ inhabited and make the order-closure irrelevant.  All of these definitions are equivalent!

Arguably, uncountability is really a property of a set [[equipped with]] an [[inequality relation]] $\#$.  Then $S$ is __$\#$-uncountable__, or the pair $(S,\#)$ is __strongly uncountable__ (or just _uncountable_ if context is clear) if, given any [[function]] $f$ from a detachable subset of $\mathbf{N}$ to $S$ (or equivalently any variation as in the previous paragraph), the function is $\#$-strongly non-surjective in the sense that there exists an element of $S$ that is $\#$-distinct from every element in the [[image]] of $f$.  Then the mere set $S$ is uncountable if and only if it is uncountable when equipped with the [[denial inequality]].


## Examples and Properties

In [[classical mathematics]], the set of [[real numbers]] is uncountable. In [[constructive mathematics]], the [[MacNeille real numbers]] are always uncountable, and in the presence of [[countable choice]], the [[Dedekind real numbers]] are uncountable. However, without countable choice, it is consistent that the Dedekind real numbers are countably indexed and thus *not* uncountable (cf [Bauer 2022](#Bauer22)), although it is unknown whether it is consistent that the Dedekind real numbers are countable in the sense of having a *bijection* with a detachable lower subset of the natural numbers. 

Every denumerable set is [[infinite set|infinite]], and hence so is every set with a denumerable subset.  Classically (usng [[dependent choice]] $DC$), we have the converse: a set is infinite if and only if it has a denumerable subset.  If a set has a denumerable subset, then its [[power set]] is uncountable.  Even without $DC$, using [[excluded middle]] instead, the power set of an infinite set is uncountable.

In contrast, the set of [[algebraic numbers]] is denumerable.  Also, the set of [[computable numbers]] is subcountably indexed (and infinite, so denumerable in classical mathematics).  Combined with the uncountability of the real numbers, this gives the existence of transcendental numbers (constructively) and uncomputable numbers (classically).

Classically, every set is countable [[xor]] uncountable.  Even constructively, a countably indexed set cannot be uncountable.  In [[Russian constructivism]], however, there are subcountable sets that are also uncountable.  In particular, the set of computable numbers is subcountably indexed, while the set of real numbers is uncountable, yet in Russian constructivism, these are the same set!  In some formalisms of Russian constructivism, *every* set is subcountably indexed.

The [[empty set]] is countable, although not denumerably indexed.  Conversely, any uncountable set must be [[inhabited set|inhabited]], as must be any denumerably indexed set.  Even constructively, a countable set is empty xor inhabited.

Every [[finite set]] is countable, every finitely indexed set is countably indexed, every subfinite set is subcountable, and every subfinitely indexed set is subcountably indexed.  Conversely, every uncountable set is [[infinite set|infinite]].

Classically, a denumerable set is precisely an [[infinite set|infinite]] countable set; sometimes this is written as a _countably infinite set_.  Thus classically, a countable set is finite xor denumerable.  Even constructively, a countable set is denumerable if and only if it is not finite.

Classically (using [[countable choice]]), [[countable unions of countable sets are countable]].


## History

Arguably, [[set theory]] as such begins with the 1873 correspondence between [[Georg Cantor]] and [[Richard Dedekind]] on countability.  Although they tacitly used [[excluded middle]] throughout, generally speaking, their results were constructive if taken to be about countably indexed sets.  They worked out the countability of the algebraic numbers and the uncountability of the real numbers, including both constructive and nonconstructive proofs of the existence of transcendental numbers.  (This was the same year that [[Charles Hermite]] published a proof that $\mathrm{e}$ is transcendental, although [[Joseph Liouville]] had shown how to artificially construct transcendental numbers as early as 1851.)

In subsequent correspondence with Cantor, [[Karl Weierstrass]] stressed the usefulness of the countability of the algebraic numbers but downplayed the notion of uncountability.  Still, he urged Cantor to publish.  Since Weierstrass and the [[finitism|finitist]] [[Leopold Kronecker]] were senior editors at Krelle\'s Journal, Cantor wrote his 1874 article carefully.  He showed the denumerability of the algebraic numbers explicitly and titled the article as if that were the only subject.  He then added a footnote in the proofreading stages, using an [[interval]]-based argument, showing how a transcendental number could be constructed from this denumeration.

Cantor\'s argument was essentially a constructive proof that the set of real numbers is uncountable, as it could apply to any denumerably indexed subset.  He tacitly used [[LLPO]], but it\'s straightforward to avoid this using binary [[meets]] and [[joins]] of real numbers, which are constructive.  He also used a [[Dedekind cut]] to construct the final transcendental number, and it is this that Kronecker would have most likely objected to, since it is an irreducibly infinite procedure to construct a single number.  However, the argument is acceptable to any non-finitist constructivist.

In the correspondence with Dedekind, it was Cantor who first considered and proved the uncountability of the real numbers but Dedekind who first considered and proved the countability of the algebraic numbers, which was the ostensible subject of Cantor\'s article.  Furthermore, it was Dedekind who first wrote the interval-based proof that Cantor used in his footnote that was the real point of the article.  However, Cantor gave Dedekind no credit.  This strained their relationship for a few years afterward.

The [[diagonal argument]] also shows the uncountability of the real numbers (nonconstructively through [[Cantor's Theorem]] on the cardinality of power sets, constructively through a slight generalization), but Cantor did not publish this until 1891.  Interpreted finitistically as an algorithm to construct, from a sequence of real numbers, an approximation of a hypothetical number not in the sequence, the diagonal argument is more efficient; pedagogically, it is easier to explain.  However, it was not the first.


## Related concepts

* [[countable ordinal]]

* [[countable cover]]


## References

* Wikipedia, _[Cantor's first set theory article](https://en.wikipedia.org/wiki/Cantor%27s_first_set_theory_article)_ 

which discusses both the origin of the 1874 article and the questions of constructivity that arose in its aftermath.

That in the absence of [[countable choice]] it is consistent that the [[Dedekind real numbers]] are countably indexed:

* {#Bauer22} [[Andrej Bauer]], *The countable reals* ([video](https://www.youtube.com/watch?v=4CBFUojXoq4)). 

[[!redirects countable set]]
[[!redirects countable sets]]
[[!redirects countably infinite set]]
[[!redirects countably infinite sets]]
[[!redirects denumerable set]]
[[!redirects denumerable sets]]

[[!redirects uncountable]]
[[!redirects uncountable set]]
[[!redirects uncountable sets]]

[[!redirects countable family]]
[[!redirects countable families]]

[[!redirects numerable]]
[[!redirects numerable set]]
[[!redirects numerable sets]]
