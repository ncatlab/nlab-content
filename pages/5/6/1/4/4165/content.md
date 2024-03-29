
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Discrete and concrete objects
+-- {: .hide}
[[!include discrete and concrete objects - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## In set theory

A __[[family]] of [[sets]]__ consists of an __index set__ $I$ and, for each [[element]] $k$ of $I$, a [[set]] $S_k$.

Given $I$, a [[set]] $F$ and a [[function]] $p\colon F \to I$, we get a family of sets by defining $S_k$ to be the [[preimage]] $p^*(k)$.

Conversely, given a family of sets, let $F$ be the [[disjoint union]]
$$ \biguplus_k S_k = \{ (k,x) | k \in I, x \in S_k \} $$
and let $f(k,x)$ be $k$.

(We should talk about ways to formalise this concept in various forms of [[set theory]] and when the latter construction above requires the [[axiom of collection]].)

## In category theory

A __[[family]] of [[sets]]__ consists of an [[discrete groupoid]] $I$ called the __index set__, and a [[functor]] $F:I \to Set$, where [[Set]] is the large [[category of sets]]. 

## In dependent type theory

A **[[family]] of [[sets]]** consists of a type $I$ called the **index type**, and a [[type family]] $S(x)$ indexed by elements $x:I$, such that every dependent type $S(x)$ is an [[h-set]] by the typal [[axiom K]] definition or the typal [[uniqueness of identity proofs]] definition. 

Equivalently, it is a type family $(I, S)$ which satisfies the familial [[axiom K]]. 

## Inconsistency of the universal family of sets

A **universal family of sets** is a set $U$ with a set $I$ and a function $E:U \to I$ such that for all sets $A$, there is a unique element $i_A \in I$ and a [[bijection]] $\delta_A:A \cong E^*(i_A)$ from $A$ to the [[fiber]] of $E$ at $i_A$. This is inconsistent in any [[set theory]], due to the [[set-theoretic Girard's paradox]]. 

## See also

* [[family]]
* [[family of subsets]]

[[!redirects family of sets]]
[[!redirects families of sets]]

[[!redirects universal family of sets]]
[[!redirects universal families of sets]]