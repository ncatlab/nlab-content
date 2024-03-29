
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

The notion of [[module]] over an [[associative algebra]] has a generalization to a notion of modules over an algebra that is an [[algebra over an operad]].

Note that sometimes an algebra over an operad is called a module over the operad, so here we have a module over a module.  (Whether algebras/modules over operads are more like algebras or more like modules depends on your point of view, so both terms are used.)


## Definition

Let $\mathcal{E}$ be a [[closed monoidal category|closed]] [[symmetric monoidal category]], $P$ an [[operad]] in $\mathcal{E}$ and $A$ a $P$-[[algebra over an operad]].

A **module** over $A$ consists of

* an [[object]] $N \in \mathcal{E}$;

* for all $1 \leq k \leq n \in \mathbb{N}$ a [[morphism]]

  $$
    \mu_{n,k} : P(n) \otimes A^{\otimes^{k-1}} \otimes N \otimes
      A^{\otimes^{n-k}} \to N
  $$

  in $\mathcal{E}$ (the [[action]] morphims)

* such that this data satisfies

  * [[unitality]] (...)

  * [[associativity]] (...)

  * equivariance (...)


## Properties

Under suitable conditions there is a [[model structure on modules over an algebra over an operad]].


## Examples

$A_\infty$-modules, etc.

(...)

## Related concepts

* [[model structure on modules over an algebra over an operad]]


## References

A review of modules over algebras over operads is at the beginning of

* [[Clemens Berger]], [[Ieke Moerdijk]], _On the derived category of an algebra over an operad_ ([arXiv](http://arxiv.org/abs/0801.2664))


[[!redirects module over an algebra over an operad]]
[[!redirects modules over an algebra over an operad]]
[[!redirects modules over algebras over an operad]]
[[!redirects modules over algebras over operads]]
