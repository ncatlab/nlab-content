# Anafunctions

* table of contents
{: toc}

## Idea

An *anafunction* is a [[relation]] between two [[sets]] $A,B$ such that to each [[element]] of $A$ there corresponds exactly one element of $B$.  It can (usually) equivalently be defined as a [[span]] $A \leftarrow F \to B$ of functions whose first leg $F\to A$ is both [[injective function|injective]] and [[surjective function|surjective]].

Every [[function]] yields an anafunction, namely its [[graph of a function|graph]], and this embeds the set of functions from $A$ to $B$ into the set of anafunctions.  Conversely, in ordinary mathematics every anafunction is the graph of some function, so these two sets are isomorphic (and indeed, in some foundations such as [[material set theory]], *equal*).  Thus in such cases the notion of anafunction is unneeded.

However, in more exotic contexts where the [[function comprehension|function comprehension principle]] (a.k.a. the "axiom of unique choice") fails, such as the [[internal logic]] of a [[quasitopos]] or a [[tripos]], it may be necessary to distinguish anafunctions from functions.  Indeed, the fact that every anafunction is a function, or equivalently that every injective and surjective function is an [[isomorphism]], is essentially the definition of the function comprehension principle.

Anafunctions are a [[decategorification]] of the notion of [[anafunctor]], and take their name from the latter.  Traditionally they would be called "total functional relations".

## In dependent type theory

In [[dependent type theory]], an anafunction is a type family $R$ indexed by types $A$ and $B$ such that for each element $a:A$, the [[dependent sum type]] $\sum_{b:B} R(a, b)$ is a [[contractible type]]: 
$$\mathrm{isAnafunction}(R) \coloneqq \prod_{a:A} \mathrm{isContr}\left(\sum_{b:B} R(a, b) \right)$$

The [[principle of unique choice]] holds in dependent type theory, which means that given any anafunction $a:A, b:B \vdash R(a, b) \; \mathrm{type}$, there is a function $a:A \vdash f(a):B$. 

The categorical semantics of an anafunction in dependent type theory is an [[infinity-anafunctor]], since the [[identity types]] between two elements of a type are not required to be [[mere propositions]]. 

Given any type family $R$ indexed by types $A$ and $B$, there is a type family $R^\op$ indexed by $B$ and $A$, defined by $R^\op(b, a) \coloneqq R(a, b)$ for all $a:A$ and $b:B$. An anafunction $R$ is an [[equivalence of types]] if both $R$ and $R^\op$ are anafunctions. 

## See also

* [[anafunctor]]
* [[infinity-anafunctor]]
* [[equivalence of types]]
* [[dependent anafunction]]

## References

For anafunctions in [[foundations of mathematics]] without the [[principle of unique choice]] see:

* [[Mike Shulman]], *Mathematics without the principle of unique choice*. [[MathOverflow]]. June 5, 2018. [Web](https://mathoverflow.net/questions/302037/mathematics-without-the-principle-of-unique-choice).

[[!redirects anafunctions]]
