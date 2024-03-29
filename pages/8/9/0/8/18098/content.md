
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

The definition of a **Gorenstein** [[ring spectrum]] is motivated by the [[Gorenstein ring|Gorenstein condition]] for [[rings]]. A Gorenstein ring, $R$, is a commutative [[Noetherian ring|Noetherian]] [[local ring]] such that the [[Ext]]-group $Ext^{\ast}_R(k, R)$ is one [[dimension|dimensional]] as a $k$-[[vector space]], where $k$ is the [[residue field]] of $R$. This last condition may be restated as the property that the [[homology]] of the ([[derived functor|right derived]]) Hom complex $Hom_R(k, R)$ is equivalent to a [[suspension]] of $k$.

Thus, a [[ring spectrum]] $\mathbf{R} \to \mathbf{k}$ is said to be Gorenstein if there is an [[equivalence in an (infinity,1)-category|equivalence]] of $\mathbf{R}$-[[module spectra]] $Hom_{\mathbf{R}}(\mathbf{k}, \mathbf{R}) \simeq \Sigma^a\mathbf{k}$ for some [[integer]] $a$.

A ring, $R \to k$, is [[Gorenstein ring|Gorenstein]] if and only if the ring spectrum $H R \to H k$ is Gorenstein. 

## Examples

Examples from [[representation theory]], from [[chromatic stable homotopy theory]] and from [[rational homotopy theory]] are given in ([Greenlees16, Sec. 23](#Greenlees16)).

## References

* [[William Dwyer]], [[John Greenlees]], [[Srikanth Iyengar]], _Duality in algebra and topology_, Advances in Maths
200 (2006) 357-402, ([ arXiv:math/0510247](https://arxiv.org/abs/math/0510247))

* {#Greenlees16} [[John Greenlees]], _Homotopy Invariant Commutative Algebra over fields_, ([arXiv:1601.02473](https://arxiv.org/abs/1601.02473))

[[!redirects Gorenstein ring spectra]]