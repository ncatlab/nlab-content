

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

An _archimedean group_ is a [[linear order|linearly]] [[ordered group]] in which every element is bounded above by a [[natural number]].

So an archimedean group has no infinite elements (and thus no non-zero [[infinitesimal object|infinitesimal]] elements).

## Definition

Let $(\mathbb{N}^+,1:\mathbb{N}^+,s:\mathbb{N}^+\to \mathbb{N}^+)$ be the set of positive integers.  

Let $(A,\lt)$ be a [[linear order|linearly]] [[ordered group]]. The positive integers are embedded into the [[function algebra|function group]] $A \to A$; there is an injection $inj:\mathbb{N}^+\to (A \to A)$ such that $inj(1) = id_A$ and $inj(s(n)) = inj(n) + id_A$ for all $n:\mathbb{N}^+$.

The __archimedean property__ states that for every $a,b:A$ such that $0 \lt a$ and $0 \lt b$, then there exist $n:\mathbb{N}^+$ such that $a \lt inj(n)(b)$. 

By [[uncurrying]] $inj$ one gets an [[action]] $act: (\mathbb{N}^+\times A) \to A$ such that $act(1,a) = a$ and $act(s(n),a) = act(n,a) + a$ for all $n:\mathbb{N}^+$ and $a:A$. The archimedean property then states that for all $a,b:A$ such that $0 \lt a$ and $0 \lt b$, there exist $n:\mathbb{N}^+$ such that $a \lt act(n,b)$. 

An __archimedean group__ is a linearly ordered group satisfying the archimedean property.

An archimedean group that is also a linearly ordered [[ring]] is called an __archimedean ring__. If an archimedean ring is a $R$-[[associative unital algebra|algebra]], then it is called an __archimedean $R$-algebra__, and if it is a [[field]], then it is called an __[[archimedean field]]__.

## Properties

Every archimedean group is an [[abelian group]] and has no bounded [[cyclic group|cyclic]] [[subgroups]]. The group of [[real numbers]] is the [[terminal object|terminal]] archimedean group. 

## Examples

Archimedean groups include

* [[integers]]

* [[half integers]]

* [[rational numbers]]

* [[dyadic rationals]]

* [[decimal rationals]]

* [[real numbers]]

Non-archimedean groups include

* [[p-adic integers]]

* [[p-adic numbers]]

## See also 

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Archimedean_group">Archimedean group</a>_

[[!redirects archimedean group]]
[[!redirects archimedean groups]]
[[!redirects non-archimedean group]]
[[!redirects non-archimedean groups]]
[[!redirects nonarchimedean group]]
[[!redirects nonarchimedean groups]]

[[!redirects Archimedean group]]
[[!redirects Archimedean groups]]
[[!redirects non-Archimedean group]]
[[!redirects non-Archimedean groups]]

[[!redirects archimedean property]]
[[!redirects Archimedean property]]
