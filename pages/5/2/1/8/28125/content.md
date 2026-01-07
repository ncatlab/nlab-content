
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



\tableofcontents

## Idea

*Relative operads* are the [[operad|operadic]] generalization of *[[relative categories]]*. In generalization of how the latter model [[(infinity,1)-category|$(\infty,1)$-categories]], so relative operads model [[(infinity,1)-operad|$(\infty,1)$-operads]].

## Definition

A *[[relative operad]]* is a pair $(O,W)$, where $O$ is a [[colored operad]] and $W$ is a [[replete subcategory]] of the category of unary operations of $O$. 


## Properties

### Relation to $(\infty,1)$-operads

 
Given a relative operad $O$, one can formally invert the maps in $W$ to obtain an $(\infty,1)$-operad $O[W^{-1}]$, called its *localization*. This process defines a functor
$$
  L 
   \;\colon\; 
  \mathsf{RelOp}
    \longrightarrow 
  \mathsf{Op}_{(\infty,1)}
$$
from the category of relative operads to the [[(∞,1)-category]] of $(\infty,1)$-operads. The main theorem of [ACP25](#ACP25) asserts that $L$ is in fact a [[localization of an (infinity,1)-category|localization]] of [[(∞,1)-categories]]. Therefore, relative operads model $(\infty,1)$-operads.

## References


* {#ACP25} [[Kensuke Arakawa]], [[Victor Carmona]], [[Francesca Pratali]]: *Relative operads model $\infty$-operads* &lbrack;[arXiv:2512.16374](https://arxiv.org/abs/2512.16374)&rbrack;

[[!redirects relative operads]]

