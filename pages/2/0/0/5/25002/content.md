
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Idea

A definition of [[field]] in [[constructive mathematics]] which uses [[denial inequality]]. It is primarily used in [[synthetic differential geometry]]. 

## Definition

A **field in the sense of Kock**, or **Kock field** for short, is a [[commutative ring]] $R$ such that [[Anders Kock]]'s Postulate K is satisfied: 

1. $R$ is nontrivial ($0 \neq 1$)

2. For all [[natural numbers]] $n \in \mathrm{N}$ and [[functions]] $x \colon \mathrm{Fin}(n) \to R$, if $x(i) \neq 0$ for all elements $i \in \mathrm{Fin}(n)$, then there exists an element $j \in \mathrm{Fin}(n)$ such that $x(j)$ is invertible. 

> (Here $Fin(n) \simeq \{1, \cdots, n\}$ denotes any [[finite set]] with $n$ elements.)

## Properties

Every Kock field is a [[local ring]] where the [[denial inequality]] $\neq$ is the [[apartness relation]] defined by $a \neq b$ if and only if $b - a$ is [[invertible]]. Thus, it is a [[weak local ring]] with an [[equivalence relation]] $a \approx b$ defined by the [[double negation]] of [[equality]]. 

However, unlike a [[Heyting field]], a Kock field cannot in general be proven to have [[stable equality]], since its [[apartness relation]] is not tight.  

Every Kock field with [[decidable equality]] is a [[discrete field]]. 

## See also

* [[local ring]]
* [[ordered local ring]]
* [[discrete field]]
* [[Heyting field]]
* [[weak Heyting field]]

## References

* [[David Jaz Myers]], Axiom 3 in Sec. 4.1 of: *Orbifolds as microlinear types in synthetic differential cohesive homotopy type theory* &lbrack;[arXiv:2205.15887](https://arxiv.org/abs/2205.15887)&rbrack;

[[!redirects Postulate K]]
[[!redirects field in the sense of Kock]]