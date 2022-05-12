+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A [[mathematical structure]] used to define the [[real numbers]] in [[Alfred Tarski]]'s axioms for the [[real numbers]]. 

## Definition ##

A [[Tarski group]] is a [[pointed set|pointed]] [[commutative invertible semigroup]] $(G, +, -, 1)$ with a [[dense linear order]] $\lt$ such that $1 \lt 1 + 1$, $a \lt b + c + a$ implies $a \lt b + a$ or $a \lt c + a$, and $a \lt b$ implies $c + a \lt c + b$. 

As a result, every Tarski group is an [[abelian group]] with [[identity element]] $0 \coloneqq 1 - 1$, and a [[trivial group|nontrivial]] [[ordered group]].

### In Tarski's axioms for the real numbers ###

* Axiom 5 says that $\mathbb{R}$ is a [[commutative semigroup]]. 

* Axiom 6 with axiom 5 together say that $\mathbb{R}$ is a [[commutative invertible semigroup]]. 

* Axiom 8 says that $\mathbb{R}$ is a [[pointed set]], which with axioms 5 and 6 imply that $\mathbb{R}$ is an [[abelian group]]. 

* Axiom 1 says that $\mathbb{R}$ has a [[connected relation]] $\lt$. 

* Axiom 2 says that $\lt$ is an [[asymmetric relation]] and thus an [[irreflexive relation]]. 

* The fragment of Axiom 4 that only refers to [[singleton]] [[subsets]] says that $\lt$ is a [[comparison]], making $\lt$ into a [[linear order]]. 

* Axiom 3 says that $\lt$ is a [[dense linear order]].

* Axiom 7 says that for all $a, b, c, d \in G$, $a + b \lt c + d$ implies that $a \lt c$ or $b \lt d$, which imply that $\mathbb{R}$ is a linearly [[ordered group]]. 

* Axiom 9 says that $1 \lt 1 + 1$, which indicates that $\mathbb{R}$ is not [[trivial group|trivial]]. 

## See also ##

* [[abelian group]]

* [[commutative invertible semigroup]]

* [[pointed set]]

* [[dense linear order]]

* [[ordered group]]

* [[real numbers]]

## References ##

* [[Alfred Tarski]],  *Introduction to Logic and to the Methodology of Deductive Sciences* (4th edition). Oxford University Press. (1994) $[$[doi:10.2307/2180610](https://doi.org/10.2307/2180610), ISBN 978-0-19-504472-0$]$

* Ucsnay, Stefanie (Jan 2008), A Note on Tarski's Note. The American Mathematical Monthly, Vol 115 No. 1, pg 66–68. JSTOR 27642393

