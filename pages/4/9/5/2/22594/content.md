

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

An _archimedean group_ is a [[linear order|linearly ordered]] [[abelian group]] in which every element is bounded above by a [[natural number]].

So an archimedean group has no infinite elements (and thus no non-zero [[infinitesimal object|infinitesimal]] elements).

## Definition

Let $(\mathbb{N}^+,1:\mathbb{N}^+,s:\mathbb{N}^+\to \mathbb{N}^+)$ be the set of positive integers and let $(\mathbb{Z},0,+,-,1)$ be the [[free abelian group]] on the set ${1}$.  

Let $(A,\lt)$ be a [[linear order|linearly ordered]] [[abelian group]] containing $\mathbb{Z}$ as a linearly ordered abelian subgroup, where $0 \lt 1$. The positive integers are embedded into $A \to A$; there is an injection $inj:\mathbb{N}^+\to (A \to A)$ such that $inj(1)(a) = a$ and $inj(s(n))(a) = inj(n)(a) + a$ for all $n:\mathbb{N}^+$ and $a:A$.

The __archimedean property__ states that if $0 \lt a$, then there exist $m,n:\mathbb{N}^+$ such that $inj(n)(1) \lt inj(m)(a)$ for all $a:A$. 

An __archimedean group__ is a linearly ordered abelian group with subgroup $\mathbb{Z}$ satisfying the archimedean property.  

By [[uncurrying]] $inj$ one gets an [[action]] $act: (\mathbb{N}^+\times A) \to A$ such that $act(1,a) = a$ and $act(s(n),a) = act(n,a) + a$ for all $n:\mathbb{N}^+$ and $a:A$. The archimedean property then states that if $0 \lt a$, then there exist $m,n:\mathbb{N}^+$ such that $act(n,1) \lt act(m,a)$ for all $a:A$. 

## Properties

The abelian group of [[integers]] is the [[initial object|initial]] archimedean group, and the abelian group of [[real numbers]] is the [[terminal object|terminal]] archimedean group. 

## See also

* [[archimedean field]]

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
