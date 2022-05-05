
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
In fact, these examples come close to to exhausting the sets than can be *proven* to have decidable equality in intuitionistic logic; by [BauerSwan18](#BauerSwan18) there is a [[topos]] (the [[function realizability]] topos, which moreover satisfies [[countable choice]], [[Markov's principle]], and other axioms) [[internal logic|in which]] all sets with decidable equality are [[countable set|countable]] (admit a surjection from a [[decidable subset]] of $\mathbb{N}$).  More precisely, although the statement "all sets with decidable equality are countable" is not true [[stack stemantics|in]] that topos, every global object with decidable equality in that topos is countable.
=--


## Applications
 {#Applications}

Working with decidable subsets of sets with decidable equality makes [[constructive mathematics]] very much like [[classical mathematics]].  This is why constructivism has few consequences for basic [[combinatorics]] and [[algebra]] (although it does have important consequences for more advanced topics in those fields).  In [[analysis]], in contrast, [[constructivism]] matters right away, because constructively the set of [[real numbers]] may not have decidable equality. 

## In type theory

In [[type theory|type-theoretic]] foundations, the notion of decidable equality is slightly different depending on whether "or" is interpreted using [[propositions as types]] or [[propositions as some types]].  That is, decidable equality for $A$ could be either of the two types
$$
\begin{aligned}
  Decidable1(A) &\coloneqq \prod_{x,y\colon A} (x=y) + \neg (x=y)\\
  Decidable2(A) &\coloneqq \prod_{x,y\colon A} [(x=y) + \neg (x=y)]
\end{aligned}
$$
where $[-]$ denotes a [[bracket type]].  Since every type maps to its bracket, $Decidable1(A)$ implies $Decidable2(A)$.

On the other hand, if $Decidable2(A)$ holds and $A$ is an [[h-set]], i.e. it satisfies [[uniqueness of identity proofs]], then $(x=y)$ and $\neg (x=y)$ represent disjoint subobjects of $A\times A$.  Thus $(x=y) + \neg (x=y)$ is already a subobject of $A\times A$, so it is equivalent to its bracket, and $Decidable1(A)$ also holds.

The converse of this is also true: if $Decidable1(A)$ holds, then not only does $Decidable2(A)$ also hold, but in fact $A$ is an h-set.  This was first proven by Michael Hedberg; a proof can be found at [[h-set]] and in the references below.  This fact is useful in [[homotopy type theory]] to show that many familiar types, such as the [[natural numbers]], are h-sets.

For non-h-sets, the difference between $Decidable1$ and $Decidable2$ can be dramatic.  For instance, if we model homotopy type theory in a [[Boolean topos|Boolean]] $(\infty,1)$-topos (such as $\infty Gpd$ constructed classically), then *every* type satisfies $Decidable2$ (which is what it means for the logic to be boolean), but only the h-sets satisfy $Decidable1$ (in accordance with Hedberg\'s theorem).

## Related concepts

* [[decidability]]
* [[stable equality]]

## References

* Michael Hedberg, *A coherence theorem for Martin-L&#246;f's type theory*, J. Functional Programming, 1998

* Nicolai Kraus, *A direct proof of Hedberg's theorem*, [blog post](http://homotopytypetheory.org/2012/03/30/a-direct-proof-of-hedbergs-theorem/)

* {#BauerSwan18} [[Andrej Bauer]] and [[Andrew Swan]], *Every metric space is separable in function realizability*, 2018, [arxiv](https://arxiv.org/abs/1804.00427)


[[!redirects decidable equality]]
[[!redirects Hedberg's theorem]]
