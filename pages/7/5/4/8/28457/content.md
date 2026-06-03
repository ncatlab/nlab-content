
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
#### Higher algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Idea

Given a [[monoidal category]] $V$, we can form the [[category of monoids]] $Mon(V)$ in $V$.

- If $V$ is a [[braided monoidal category]], then $Mon(V)$ admits a tensor product, making it a monoidal category. (The category of monoids in $Mon(V)$ is the [[category of commutative monoids]] $CMon(V)$ in $V$.)
- If $V$ is a [[symmetric monoidal category]], then $Mon(V)$ is furthermore a braided monoidal category (moreover a symmetric monoidal category).

One dimension higher, given a [[monoidal bicategory]] $V$, we can form the [[bicategory]] of [[pseudomonoids]] $PsMon(V)$ in $V$.

- If $V$ is a [[braided monoidal bicategory]], then $Mon(V)$ is a monoidal bicategory.
- If $V$ is a [[sylleptic monoidal bicategory]], then $Mon(V)$ is furthermore a braided monoidal bicategory.
- If $V$ is a [[symmetric monoidal bicategory]], then $Mon(V)$ is furthermore a sylleptic monoidal bicategory (moreover a symmetric monoidal bicategory).

This phenomenon extends to higher dimensions and is dubbed **symmetry shifting** in [Stenzel 2026](#Stenzel26). The following is Corollary 2.10 ibid.

\begin{theorem}
  Let $0 \leq k \leq \infty$ and let $V$ be an [[En-algebra|$E_k$-monoidal $(\infty, 1)$-category]]. For all $0 \leq m \leq k$, the $(\infty, 1)$-category of $E_m$-monoids in $V$ is an $E_{k - m}$-monoidal $(\infty, 1)$-category.
\end{theorem}

## Related concepts

* [[k-tuply monoidal n-category]]
* [[microcosm principle]]
* [[Fox's theorem]]

## References

* [[Raffael Stenzel]], _Symmetry shifting for monoidal bicategories_, [arXiv:2602.15358](https://arxiv.org/abs/2602.15358)