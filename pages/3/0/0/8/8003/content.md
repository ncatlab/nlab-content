
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

To a [[permutative category]]  $C$ is naturally associated a [[Gamma-space]], hence a [[symmetric spectrum]]. The [[generalized (Eilenberg-Steenrod) cohomology]] theory [[Brown representability theorem|represented]] by this is called the 
_([[algebraic K-theory|algebraic]]) [[K-theory]]_ of (or represented by) $C$.

If the category is is even a [[bipermutative category]] then the corresponding [[K-theory of a bipermutative category]] in addition has [[E-infinity ring]] structure, hence is a [[multiplicative cohomology theory]].

## Definition
 {#Definition}

### Via topological group completion

For $C$ a [[permutative category]] its [[nerve]]/[[geometric realization]] $\vert C \vert$ (often denoted $B C$, but we avoid this here not to confuse with [[delooping]]) is naturally a [[topological monoid]] ([Quillen 70](#Quillen70) see e.g. [May, theorem 4.10](#May)). Its [[group completion]] $\Omega B {\vert C\vert}$ is the _algebraic K-theory [[spectrum]]_ of $C$ (see e.g. [May, def 4.11](#May))

In particular for $R$ a [[topological ring]] one considers $C$ a [[skeletal category|skeleton]] of the [[groupoid]] of (finitely generated) [[projective modules]] over $R$. Then the K-theory of $C$ is the [[algebraic K-theory]] of $R$ (e.g. [May, p. 25](#May))

By ([Dwyer-Kan 80](#DwyerKan80)) the operation $\Omega B (-)$ is the [[derived functor]] of [[group completion]], so that this construction ought to be a model for the [[K-theory of a symmetric monoidal (infinity,1)-category]].

### Via Gamma spaces

Write $FinSet^{*/}$ for the [[category]] of [[pointed objects]] [[finite sets]].

For $C$ a [[permutative category]], there is naturally a [[functor]]

$$
  \widebar {C}_{(-)} : FinSet^{*/} \to Cat
$$

$$
  A \mapsto \widebar C_A
$$

such that (...).

([Elmendorf-Mandell, theorem 4.2](#ElmendorfMandell06))

Accordingly, postcomposition with the [[nerve]] $N : Cat \to sSet$ produces from $C$ a [[Gamma-space]] $N \widebar C$. To this corresponds a [[spectrum]] 

$$
  K^{Seg} C \coloneqq \{N \widebar C_{S_\bullet^n}\}
  \,.
$$ 

This is the _K-theory spectrum of $C$_.

([Elmendorf-Mandell, def. 4.3](#ElmendorfMandell06))


## Related concepts

* [[K-theory of a bipermutative category]]

* [[algebraic K-theory of a symmetric monoidal (∞,1)-category]]

## References

* {#Quillen70} [[Daniel Quillen]], _Cohomology of groups_, Proceedings of the international congress of mathematics 1970

* {#Quillen} [[Daniel Quillen]], _On the group completion of a simplicial monoid_

* {#Segal} [[Graeme Segal]], _Catgeories and cohomology theories_, Topology vol 13 (1974)  ([pdf](http://ncatlab.org/nlab/files/SegalCategoriesAndCohomologyTheories.pdf))
 

* [[Peter May]], _The spectra associated to permutative categories_, Topology 17 (1978) ([pdf](http://www.math.uchicago.edu/~may/PAPERS/23.pdf))

* {#May} [[Peter May]], _$E_\infty$-Spaces, group completions, and permutative categories_ ([pdf](http://www.math.uchicago.edu/~may/PAPERS/13.pdf))


* {#DwyerKan80} [[William Dwyer]], [[Daniel Kan]], _Simplicial localization of categories_, Journal of pure and applied algebra 17 (1980) 267-284

* [[Anthony Elmendorf]], [[Michael Mandell]], _Permutative categories as a model of connective stable homotopy_, in: [[Birgit Richter]] (ed.) _Structured Ring spectra_, Cambridge University Press (2004)

* {#ElmendorfMandell06} [[Anthony Elmendorf]], [[Michael Mandell]], _Rings, modules and algebras in infinite loop space theory_, K-Theory 0680 ([web](http://www.math.uiuc.edu/K-theory/0680/), [pdf](http://www.math.uiuc.edu/K-theory/0680/RMAsubmit.pdf))
 
* [[Anthony Elmendorf]], [[Michael Mandell]], _Permutative categories, multicategories, and algebraic K-theory_, Algebraic & Geometric Topology 9 (2009) 2391-2441 ([arXiv:0710.0082v2](http://arxiv.org/abs/0710.0082))


