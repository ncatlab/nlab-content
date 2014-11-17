
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _Calabi-Yau algebra_ is an algebraic incarnation of the notion of _[[Calabi-Yau manifold]]_  and [[higher algebra]]-version of the notion of [[Frobenius algebra]].

## Definition


+-- {: .num_defn }
###### Definition

For $A$ a [[dg-algebra]] and $N$ a [[dg-module|dg-bimodule]] over $A$, write

$$
  N^! := RHom_{A Bimod}(N, A \otimes A)
$$

for the dual $A$-[[bimodule]], where $RHom$ denotes the [[derived functor|right derived]] [[hom-functor]] with respect to the [[model structure on dg-modules]].

=--

+-- {: .num_defn }
###### Definition

A homologically smooth [[dg-algebra]] $A$ is a **Calabi-Yau algebra** of [[dimension]] $d$ if there is a [[quasi-isomorphism]] of $A$-[[bimodule]]s

$$
 f :  A \stackrel{\simeq}{\to} A^![d]
$$

such that

$$
  f \simeq f^![d]
  \,.
$$ 

=--

This is ([Ginzburg, def. 3.2.3](#Ginzburg)).

## Properties

Let $X$ be a [[smooth scheme|smooth]] [[quasi-projective variety]]. Write $D^b(Coh X)$ for the [[derived category]] of bounded [[chain complex]]es of [[coherent sheaves]] over $X$.

+-- {: .num_defn #TiltingGenerator}
###### Definition

An [[object]] $\mathcal{E} \in D^b(Coh X)$ is called a **tilting generator** if the [[Ext]]-functor satisfies

1. $Ext^i(\mathcal{E}, \mathcal{E}) = 0$ for all $i \gt 0$;

1. $Ext^\bullet(\mathcal{E},\mathcal{F}) = 0$ implies $\mathcal{F} = 0$;

1. the [[endomorphism]] algebra $End(\mathcal{E}) = Hom(\mathcal{E},\mathcal{E})$ has finite [[Hochschild cohomology|Hochschild]] [[dimension]].

=--

This appears as ([Ginzburg, def. 7.1.1](#Ginzburg)). 

+-- {: .num_remark}
###### Remark

For $\mathcal{E}$ a tilting generator there is an [[equivalence of categories|equivalence]] of [[triangulated categories]]

$$
  D^b(Coh X) \stackrel{\simeq}{\to}  D^b(End(\mathcal{E})Mod)
$$

to the [[derived category]] of [[module]]s over $End(\mathcal{E})$.

=--

+-- {: .num_prop}
###### Proposition

For $X$ smooth connected variety which is projective over an affine variety, let $\mathcal{E} in D^b(Coh X)$ be a tilting generator, def. \ref{TiltingGenerator}. 

Then $End \mathcal{E}$ is a Calabi-Yau algebra of dimension $d$ precisely if $X$ is a [[Calabi-Yau manifold]] of dimension $d$.

=--

This appears as ([Ginzburg, prop. 3.3.1](#Ginzburg)).

## Related concepts

* [[Calabi-Yau object]]

  * **Calabi-Yau algebra**, [[Calabi-Yau manifold]]

  * [[Calabi-Yau category]]

## References

* {#Ginzburg} [[Victor Ginzburg]], _Calabi-Yau algebras_ ([arXiv:0612139](http://arxiv.org/abs/math/0612139))
 

[[!redirects Calabi-Yau algebras]]

[[!redirects Calabi-Yau A-∞ algebra]]
[[!redirects Calabi-Yau A-∞ algebras]]
