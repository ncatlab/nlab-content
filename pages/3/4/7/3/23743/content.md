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

# Setoids
* table of contents
{: toc}

## Idea

Similar to how an [[inequality space]] has an [[apartness relation]] whose [[negation]] implies [[equality]], a *stable setoid* ought to have a [[equivalence relation]] (i.e. setoid) whose [[double negation]] [[implication|implies]] equality. 

## Definition 

In [[type theory]], a [[setoid]] $(T, \equiv)$ is **stable** if for all $a:T$ and $b:T$, $p(a, b):\neg\neg(a \equiv b) \to (a = b)$. 

## Properties 

* Every stable setoid is a [[univalent setoid]], and thus a [[set]]. 

* Every stable setoid is a [[inequality space]]. 

## See also 

* [[setoid]]
* [[stable equality]]
* [[inequality space]]
* [[univalent setoid]]

[[!redirects stable setoids]]
