
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

## Definition ##

In [[constructive mathematics]], a [[set]] $X$ has __stable equality__ if any two [[elements]] of $X$ are [[equality|equal]] if (hence iff) they are [[double negation|not not]] equal.  

## Examples ##

* Every [[set]] with [[decidable equality]] has stable equality, but not conversely.

* Every [[set]] $S$ with a [[tight apartness relation]] $\#$ has stable equality, because even in [[constructive mathematics]], given elements $x \in S$ and $y \in S$, $\neg \neg \neg (x \# y) \iff \neg (x \# y)$, and because $\neg (x \# y) \iff x = y$, $\neg \neg (x = y) \iff x = y$, and thus $S$ is stable. 

* In particular, the [[Dedekind real numbers]] have stable equality, and any Heyting [[subfield]] of the [[Dedekind real numbers]] has stable equality. 

## See also ##

* [[stable relation]]
* [[decidable equality]]
* [[stable equivalence relation]]

## References

* {#BauerSwan18} [[Andrej Bauer]] and [[Andrew Swan]], *Every metric space is separable in function realizability*, 2018, [arxiv](https://arxiv.org/abs/1804.00427)

[[!redirects stable equalities]]
