+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]

=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Similar to how equality is stable if its [[double negation]] implies equality, an *equivalence relation* ought is **stable** if its [[double negation]] [[implication|implies]] equality. 

## Definition 

In [[set theory]], an [[equivalence relation]] $\equiv$ on a set $S$ is **stable** if for all $a \in S$ and $b \in S$, if $\neg\neg(a \equiv b)$ then $a \equiv b$. 

In [[type theory]], a ([[proposition]]-valued) [[equivalence relation]] $\equiv$ on a type $T$ is **stable** if for all $a:T$ and $b:T$, there is a function $p(a, b):\neg\neg(a \equiv b) \to (a \equiv b)$. 

## Properties

* The negation of every stable equivalence relation is an [[apartness relation]]. 

## See also 

* [[equivalence relation]]
* [[stable equality]]
* [[tight apartness relation]]
* [[univalent equivalence relation]]

[[!redirects stable equivalence relations]]
