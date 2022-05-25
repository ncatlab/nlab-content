
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

## Idea

An *Artinian bimodule* is a bimodule which satisfies the descending chain condition on its subbimodules. 

## Definition

Given [[rings]] $R$ and $S$ and an $R$-$S$-[[bimodule]] $B$, let $\mathrm{Mono}(B)$ be the [[category]] whose [[objects]] are $R$-$S$-[[subbimodules]] of $B$ and whose [[morphisms]] are $R$-$S$-[[bimodule monomorphisms]]. A descending chain of $R$-$S$-subbimodules is a [[sequence]] of $R$-$S$-subbimodules $A:\mathbb{N} \to \mathrm{Mono}(B)$ with the following [[dependent type|dependent sequence]] of $R$-$S$-bimodule monomorphisms: for natural number $n \in \mathbb{N}$, a dependent $R$-$S$-bimodule monomorphism $i_n:A_{n+1} \hookrightarrow A_{n}$. 

An $R$-$S$-[[bimodule]] $B$ is **Artinian** if it satisfies the **descending chain condition** on its subbimodules: for any descending chain of $R$-$S$-subbimodules $(A, i_n)$ of $B$, there exists a natural number $m \in \mathbb{N}$ such that for all natural numbers $n \geq m$, the $R$-$S$-bimodule monomorphism $i_n:A_{n+1} \hookrightarrow A_{n}$ is an $R$-$S$-[[bimodule isomorphism]]. 

## Examples

A [[ring]] $R$ is [[Artinian ring|Artinian]] if it is Artinian as a $R$-$R$-[[bimodule]] with respect to its canonical bimodule structure, with its [[left action]] and [[right action]] defined as its multiplicative binary operation and its [[biaction]] defined as its ternary product:
$$\alpha_L(a, b) \coloneqq a \cdot b$$
$$\alpha_R(a, b) \coloneqq a \cdot b$$
$$\alpha(a, b, c) \coloneqq a \cdot b \cdot c$$

## See also

* [[bimodule]]

* [[Noetherian bimodule]]

* [[Artinian ring]]

[[!redirects Artinian bimodules]]