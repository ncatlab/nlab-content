
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

Given a [[category]] $C$ and an object $B:C$, let $\mathrm{Mono}(B)$ be the [[category]] whose [[objects]] are [[subobjects]] of $B$ and whose [[morphisms]] are [[monomorphisms]]. A ascending chain of subobjects of $B$ is a [[direct sequence]] in $\mathrm{Mono}(B)$, a [[sequence]] of subobjects $A:\mathbb{N} \to \mathrm{Mono}(B)$ with the following [[dependent type|dependent sequence]] of monomorphisms: for [[natural number]] $n \in \mathbb{N}$, a dependent monomorphism $i_n:A_{n} \hookrightarrow A_{n+1}$. 

Given categories $C$ and $D$ with [[forgetful functor]] $F:C \to D$, an object $B$ is said to satisfy the **ascending chain condition** on subobjects of $F(B)$ if for every ascending chain of subobjects $(A, i_n)$ of $F(B)$, there exists a natural number $m \in \mathbb{N}$ such that for all natural numbers $n \geq m$, the monomorphism $i_n:A_{n} \hookrightarrow A_{n+1}$ is an [[isomorphism]]. 

## Examples

There is a [[forgetful functor]] $F:Ring \to BMod$ from the category [[Ring]] of [[rings]] to the category $BMod$ of [[bimodules]], which forgets the multiplicative structure on the bimodule, that the canonical [[left action]] and [[right action]] of each ring $R$ have [[domain]] $R^2$ and are equal to each other and to the multiplicative binary operation of $R$, and that the canonical [[biaction]] of each ring $R$ has domain $R^3$. 

Given a ring $R$, a two-sided ideal is a subobject of $F(R)$, a sub-$R$-$R$-bimodule. A [[ring]] $R$ is said to satisfy the ascending chain condition on two-sided ideals if for every ascending chain of two-sided ideals $(A, i_n)$ of $F(B)$, there exists a natural number $m \in \mathbb{N}$ such that for all natural numbers $n \geq m$, the monomorphism $i_n:A_{n} \hookrightarrow A_{n+1}$ is an [[isomorphism]]. 

Similarly, there are forgetful functors $G:Ring \to LeftMod$ from $Ring$ to the category $LeftMod$ of [[left modules]] and $H:Ring \to RightMod$ from $Ring$ to the category $RightMod$ of [[right modules]], and one could similarly define the ascending chain condition on [[left ideals]] and [[right ideals]] for rings. 

## See also

* [[descending chain condition]]

* [[Noetherian bimodule]]

* [[Noetherian ring]]

[[!redirects ascending chain conditions]]