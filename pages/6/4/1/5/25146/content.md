

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Set theory
+-- {: .hide}
[[!include set theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

\tableofcontents

## Definition

### In set theory

In [[set theory]], there are many ways to say that given the [[relation]] or [[correspondence]] $R$, $R(x, y)$ holds of elements $x \in A$ and $y \in B$. In [[allegorical set theories]] like [[SEAR]], it is a foundational concept. In [[categorical set theories]] like [[ETCS with elements]], we say that $R(x, y)$ holds of elements $x \in A$ and $y \in B$ if the ordered pair $(x, y)$ is in the [[image]] of the function $(p_1, p_2):R \to A \times B$. In [[material set theories]] like [[ZFC]], we say that $R(x, y)$ holds of elements $x \in A$ and $y \in B$ if the ordered pair $(x, y)$ is in $R$. 

In [[set theory]], a **one-to-one correspondence** or **bitotal correspondence** is a [[relation]] or [[correspondence]] $R$ between sets $A$ and $B$ for which for every element $x \in A$, there is a unique element $y \in B$ such that $R(x, y)$ holds, and for every element $y \in B$, there is a unique element $x \in A$ such that $R(x, y)$ holds. Equivalently, it is an [[anafunction]] $R$ between sets $A$ and $B$ such that for every element $y \in B$, there is a unique element $x \in A$ such that $R(x, y)$ holds. 

### In type theory

In [[type theory]], given types $A$ and $B$, a **one-to-one correspondence** or **bitotal correspondence** is a [[correspondence]] $x:A, y:B \vdash R(x, y)$ for which for every element $x:A$, [[uniqueness quantifier|there exists a unique]] element $y:B$ such that $R(x, y)$, and for every element $y:B$, there exists a unique element $x:A$ such that $R(x, y)$. Equivalently, it is an [[anafunction]] $x:A, y:B \vdash R(x, y)$ such that for every element $y:B$, the dependent type $\sum_{x:A} R(x, y)$ is a [[contractible type]]. 

Given a [[Tarski universe]] $(U, T)$, the type of all $U$-small one-to-one correspondences between $A$ and $B$ is given by the type 

$$\mathrm{BitotalCorr}_U(A, B) \coloneqq \sum_{R:A \times B \to U} \left(\prod_{x:A} \exists!y:B.T(R(x, y)\right) \times \left(\prod_{y:B} \exists!x:A.T(R(x, y))\right)$$

The univalence axiom for $U$ is given by the [[equivalence of types]]

$$\mathrm{ua}_U:\prod_{A:U} \prod_{B:U} (A =_U B) \simeq \mathrm{BitotalCorr}_U(T(A), T(B))$$

## Properties

By the [[principle of unique choice]], given every one-to-one correspondence, there is a [[bijection]] $f:A \cong B$. However, in the absence of the principle of unique choice, bijections and one-to-one correspondences are not necessarily the same; this is the same phenomena as the phenomena between [[functions]] and [[anafunctions]]. However, frequently in [[material set theories]], functions are defined to be anafunctions, and so bijections are similarly defined to be one-to-one correspondences. 

Something similar occurs in [[dependent type theory]], where by the [[principle of unique choice]], given every one-to-one correspondence, there is a function with contractible fibers $x:A \vdash f(x):B$, which becomes a bijection in the context of [[axiom K]] or [[uniqueness of identity proofs]]. However, in contrast to [[material set theory]], in dependent type theory, there is always a distinction between a function $x:A \vdash f(x):B$ and an anafunction $x:A, y:B \vdash R(x, y)$, and so there is always a distinction between a function with contractible fibers and a one-to-one correspondence. 

## See also

* [[bijection]], [[equivalence of types]]

* [[anafunction]]

## References

* [[Mike Shulman]], *Towards Third-Generation HOTT -- Part 1* ([slides](https://www.cmu.edu/dietrich/philosophy/hott/slides/shulman-2022-04-28.pdf), [video](https://www.youtube.com/watch?v=FrxkVzItMzA))

* [[Mike Shulman]], *Higher Observational Type Theory: An autonomous foundation for univalent mathematics* ([slides](https://home.sandiego.edu/~shulman/papers/chapman-fall2022.pdf))

[[!redirects one-to-one correspondence]]
[[!redirects one-to-one correspondences]]
[[!redirects one to one correspondence]]
[[!redirects one to one correspondences]]
[[!redirects 1-to-1 correspondence]]
[[!redirects 1-to-1 correspondences]]
[[!redirects 1 to 1 correspondence]]
[[!redirects 1 to 1 correspondences]]
[[!redirects 1-1 correspondence]]
[[!redirects 1-1 correspondences]]
[[!redirects 1–1 correspondence]]
[[!redirects 1–1 correspondences]]

[[!redirects bitotal correspondence]]
[[!redirects bitotal correspondences]]