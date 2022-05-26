
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### Artinian rings

Every [[ring]] $R$ has a canonical $R$-$R$-[[bimodule]] structure, with [[left action]] $\alpha_L:R \times R \to R$ and [[right action]] $\alpha_R:R \times R \to R$ defined as the multiplicative binary operation on $R$ and [[biaction]] $\alpha:R \times R \times R \to R$ defined as the ternary product on $R$:
$$\alpha_L(a, b) \coloneqq a \cdot b$$
$$\alpha_R(a, b) \coloneqq a \cdot b$$
$$\alpha(a, b, c) \coloneqq a \cdot b \cdot c$$

Let $\mathrm{TwoSidedIdeals}(R)$ be the [[category of two-sided ideals]] in $R$, whose objects are [[two-sided ideals]] $I$ in $R$, [[subbimodules|sub-$R$-$R$-bimodules]] of $R$ with respect to the canonical bimodule structure on $R$, and whose [[morphisms]] are $R$-$R$-[[bimodule monomorphisms]]. 

A descending chain of two-sided ideals in $R$ is an [[inverse sequence]] of two-sided ideals in $R$, a [[sequence]] of two-sided ideals $A:\mathbb{N} \to \mathrm{TwoSidedIdeals}(R)$ with the following [[dependent type|dependent sequence]] of $R$-$R$-bimodule monomorphisms: for natural number $n \in \mathbb{N}$, a dependent $R$-$R$-bimodule monomorphism $i_n:A_{n+1} \hookrightarrow A_{n}$. 

A [[ring]] $R$ is **Artinian** if it satisfies the [[descending chain condition]] on its two-sided ideals: for every descending chain of two-sided ideals $(A, i_n)$ in $R$, there exists a natural number $m \in \mathbb{N}$ such that for all natural numbers $n \geq m$, the $R$-$R$-bimodule monomorphism $i_n:A_{n+1} \hookrightarrow A_{n}$ is an $R$-$R$-[[bimodule isomorphism]]. 

### Left Artinian rings

Let $\mathrm{LeftIdeals}(R)$ be the category of [[left ideals]] in $R$, whose objects are [[left ideals]] $I$ in $R$, sub-left-$R$-modules of $R$ with respect to the canonical [[left module]] structure $(-)\cdot(-):R \times R \to R$ on $R$, and whose [[morphisms]] are left $R$-module monomorphisms. 

A descending chain of left ideals in $R$ is an [[inverse sequence]] of left ideals in $R$, a [[sequence]] of left ideals $A:\mathbb{N} \to \mathrm{LeftIdeals}(R)$ with the following [[dependent type|dependent sequence]] of left $R$-module monomorphisms: for natural number $n \in \mathbb{N}$, a dependent left $R$-module monomorphism $i_n:A_{n+1} \hookrightarrow A_{n}$. 

A [[ring]] $R$ is **left Artinian** if it satisfies the [[descending chain condition]] on its left ideals: for every descending chain of left ideals $(A, i_n)$ in $R$, there exists a natural number $m \in \mathbb{N}$ such that for all natural numbers $n \geq m$, the left $R$-module monomorphism $i_n:A_{n+1} \hookrightarrow A_{n}$ is an left $R$-module isomorphism. 

### Right Artinian rings

Let $\mathrm{RightIdeals}(R)$ be the category of [[right ideals]] in $R$, whose objects are [[right ideals]] $I$ in $R$, sub-right-$R$-modules of $R$ with respect to the canonical [[right module]] structure $(-)\cdot(-):R \times R \to R$ on $R$, and whose [[morphisms]] are right $R$-module monomorphisms. 

A descending chain of right ideals in $R$ is an [[inverse sequence]] of right ideals in $R$, a [[sequence]] of right ideals $A:\mathbb{N} \to \mathrm{RightIdeals}(R)$ with the following [[dependent type|dependent sequence]] of right $R$-module monomorphisms: for natural number $n \in \mathbb{N}$, a dependent right $R$-module monomorphism $i_n:A_{n+1} \hookrightarrow A_{n}$. 

A [[ring]] $R$ is **right Artinian** if it satisfies the [[descending chain condition]] on its right ideals: for every descending chain of right ideals $(A, i_n)$ in $R$, there exists a natural number $m \in \mathbb{N}$ such that for all natural numbers $n \geq m$, the right $R$-module monomorphism $i_n:A_{n+1} \hookrightarrow A_{n}$ is an right $R$-module isomorphism. 

## Properties

In an artinian ring $R$ the [[Jacobson radical]] $J(R)$ is [[nilpotent ideal|nilpotent]]. A left artinian ring is semiprimitive if and only if the zero ideal is the unique nilpotent ideal.

## Artinian and Noetherian rings

A dual condition is noetherian: a __[[noetherian ring]]__ is a ring satisfying the ascending chain condition on ideals. The symmetry is severely broken if one considers unital rings: for example every unital artinian ring is noetherian. For a converse there is a strong condition: a left (unital) ring $R$ is left artinian iff $R/J(R)$ is semisimple in $_R Mod$ and the Jacobson radical $J(R)$ is nilpotent. Artinian rings are intuitively much smaller than generic noetherian rings. 

## See also

* [[Artinian bimodule]]

* [[artinian object]]

[[!redirects artinian rings]]
[[!redirects Artinian ring]]
[[!redirects Artinian rings]]