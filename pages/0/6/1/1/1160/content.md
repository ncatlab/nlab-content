
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definitions

In [[constructive mathematics]], a [[set]] $X$ has __decidable equality__ if any two elements of $X$ are either [[equality|equal]] or [[negation|not]] equal.  Equivalently, $X$ has decidable equality if its [[equality]] [[relation]] is a [[decidable subset]] of $X \times X$.  Sometimes one says that such a set $X$ is _discrete_, although of course this term has many meanings.  Of course, in [[classical mathematics]], every set has decidable equality.  But the concept generalises in [[sheaf and topos theory|topos theory]] to the notion of [[decidable object]].

## Examples

* Every [[finite set]] has decidable equality (though the same is not true for finitely-indexed or subfinite sets).

* The [[natural numbers]] have decidable equality.

+--{: .un_remark}
###### Remark
In fact, these examples come close to exhausting the sets that can be *proven* to have decidable equality in intuitionistic logic; by [BauerSwan18](#BauerSwan18) there is a [[topos]] (the [[function realizability]] topos, which moreover satisfies [[countable choice]], [[Markov's principle]], and other axioms) [[internal logic|in which]] all sets with decidable equality are [[countable set|countable]] (admit a surjection from a [[decidable subset]] of $\mathbb{N}$).  More precisely, although the statement "all sets with decidable equality are countable" is not true [[stack semantics|in]] that topos, every global object with decidable equality in that topos is countable.
=--


## Applications
 {#Applications}

Working with decidable subsets of sets with decidable equality makes [[constructive mathematics]] very much like [[classical mathematics]].  This is why constructivism has few consequences for basic [[combinatorics]] and [[algebra]] (although it does have important consequences for more advanced topics in those fields).  In [[analysis]], in contrast, [[constructivism]] matters right away, because constructively the set of [[real numbers]] may not have decidable equality. 

## In type theory

In [[type theory|type-theoretic]] foundations, there are two different notions of decidable equality, depending on whether "or" is interpreted using [[sum types]] $\prod_{x,y\colon A} (x=y) + \neg (x=y)$ or [[disjunctions]] $\prod_{x,y\colon A} (x=y) \vee \neg (x=y)$, i.e. the [[bracket type]] of [[sum types]]. The former notion of decidable equality is called **untruncated decidable equality**, while the latter notion is called **truncated decidable equality**. Since every type maps to its bracket, untruncated decidable equality implies truncated decidable equality.

On the other hand, if truncated decidable equality holds and $A$ is an [[h-set]], i.e. it satisfies [[uniqueness of identity proofs]], then $(x=y)$ and $\neg (x=y)$ represent disjoint subobjects of $A\times A$.  Thus $(x=y) + \neg (x=y)$ is already a subobject of $A\times A$, so it is equivalent to its bracket, and untruncated decidable equality also holds.

The converse of this is also true: if untruncated decidable equality holds, then not only does truncated decidable equality also hold, but in fact $A$ is an h-set. This was first proven by Michael Hedberg; a proof can be found at [[Hedberg's theorem]] and in the references below. This fact is useful in [[homotopy type theory]] to show that many familiar types, such as the [[natural numbers]], are h-sets.

For non-h-sets, the difference between untruncated decidable equality and truncated decidable equality can be dramatic. For instance, if we model homotopy type theory in a [[Boolean topos|Boolean]] $(\infty,1)$-topos (such as $\infty Gpd$ constructed classically), then *every* type satisfies truncated decidable equality (which is what it means for the logic to be boolean), but only the h-sets satisfy untruncated decidable equality (in accordance with Hedberg\'s theorem).

### Using the boolean domain

There is also a few definitions of decidable equality in [[dependent type theory]], which rely on the [[boolean domain]] with its extensionality principle and the fact that that the decidable equality is always valued in the [[boolean domain]]. 

The first definition states that decidable equality on a type $A$ is a [[binary function]] $\mathrm{Eq}_A:A \times A \to \mathrm{Bit}$ which comes with a family of equivalences
$$x:A, y:A \vdash \delta(x, y):\mathrm{Id}_A(x, y) \simeq \mathrm{Id}_\mathbb{2}(\mathrm{Eq}_A(x, y), 1)$$

The second also relies on the fact that the [[boolean domain]] forms a [[univalent Tarski universe]] $(\mathrm{Bit}, \mathrm{El}_\mathrm{Bit})$. Here, decidable equality on a type $A$ is a [[binary function]] $\mathrm{Eq}_A:A \times A \to \mathrm{Bit}$ which comes with a family of equivalences 
$$x:A, y:A \vdash \delta(x, y):\mathrm{El}_\mathrm{Bit}(\mathrm{Eq}_A(x, y)) \simeq (x =_A y)$$

Either way, this is typically how the [[natural numbers type]] is proven to have decidable equality, by defining a binary function into the boolean domain called [[observational equality]] and using the extensionality principle of the natural numbers. 

### Properties

Every set with decidable equality is [[locally finite type|locally finite]]. 

## Related concepts

* [[decidability]]
* [[stable equality]]
* [[locally finite type]]
* [[classical set]]

## References

* Michael Hedberg, *A coherence theorem for Martin-L&#246;f's type theory*, J. Functional Programming, 1998

* Nicolai Kraus, *A direct proof of Hedberg's theorem*, [blog post](http://homotopytypetheory.org/2012/03/30/a-direct-proof-of-hedbergs-theorem/)

* {#BauerSwan18} [[Andrej Bauer]] and [[Andrew Swan]], *Every metric space is separable in function realizability*, 2018, [arxiv](https://arxiv.org/abs/1804.00427)

[[!redirects decidable set]]
[[!redirects decidable sets]]

[[!redirects decidable equality]]
[[!redirects truncated decidable equality]]
[[!redirects untruncated decidable equality]]