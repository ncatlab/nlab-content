
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

Given a [[category]] $C$ and an object $B:C$, let $\mathrm{Mono}(B)$ be the [[category]] whose [[objects]] are [[subobjects]] of $B$ and whose [[morphisms]] are [[monomorphisms]]. A descending chain of subobjects of $B$ is an [[inverse sequence]] in $\mathrm{Mono}(B)$, a [[sequence]] of subobjects $A:\mathbb{N} \to \mathrm{Mono}(B)$ with the following [[dependent sequence]] of monomorphisms: for [[natural number]] $n \in \mathbb{N}$, a dependent monomorphism $i_n:A_{n+1} \hookrightarrow A_{n}$. 

Given categories $C$ and $D$ with forgetful functor $F:C \to D$, an object $B$ is said to satisfy the **descending chain condition** on subobjects of $F(B)$ if for every descending chain of subobjects $(A, i_n)$ of $F(B)$, there exists a natural number $m \in \mathbb{N}$ such that for all natural numbers $n \geq m$, the monomorphism $i_n:A_{n+1} \hookrightarrow A_{n}$ is an [[isomorphism]]. 

Subobjects (considered as isomorphism classes) form a possibly large [[partially ordered set]] (poset). A partially ordered set $(X,\geq)$ is satisfying a descending chain condition if any inverse sequence $x_1\geq x_2\geq x_3\geq\ldots$ eventually stabilizes, that is, there exists $n$ such that $x_n = x_{n+1} =x_{n+2}=\ldots$.

## Examples

There is a [[forgetful functor]] $F:Ring \to BMod$ from the category [[Ring]] of [[rings]] to the category $BMod$ of [[bimodules]], which forgets the multiplicative structure on the bimodule, that the canonical [[left action]] and [[right action]] of each ring $R$ have [[domain]] $R^2$ and are equal to each other and to the multiplicative binary operation of $R$, and that the canonical [[biaction]] of each ring $R$ has domain $R^3$. 

Given a ring $R$, a two-sided ideal is a subobject of $F(R)$, a sub-$R$-$R$-bimodule. A [[ring]] $R$ is said to satisfy the descending chain condition on two-sided ideals if for every descending chain of two-sided ideals $(A, i_n)$ of $F(B)$, there exists a natural number $m \in \mathbb{N}$ such that for all natural numbers $n \geq m$, the monomorphism $i_n:A_{n+1} \hookrightarrow A_{n}$ is an [[isomorphism]]. 

Similarly, there are forgetful functors $G:Ring \to LeftMod$ from $Ring$ to the category $LeftMod$ of [[left modules]] and $H:Ring \to RightMod$ from $Ring$ to the category $RightMod$ of [[right modules]], and one could similarly define the descending chain condition on [[left ideals]] and [[right ideals]] for rings. 

## See also

* [[ascending chain condition]]

* [[Artinian bimodule]]

* [[Artinian ring]]

* [[Mittag-Leffler condition]]

[[!redirects descending chain conditions]]
