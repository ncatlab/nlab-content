
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _model topos_ is a [[model category]] that [[presentable (∞,1)-category|presents]] an [[(∞,1)-topos]].

+-- {: .num_defn}
###### Definition

A [[model category]] $\mathcal{C}$ is a **model topos** if there is a [[simplicial site]] $K$ and a [[Quillen equivalence]] $\mathcal{C} \simeq sPSh(K)_{loc}$ to the local [[model structure on sSet-presheaves]] over $K$.

=--

This appears as [Rezk, 6.1](#Rezk).

## Related concepts


* [[model site]], [[model structure on simplicial presheaves]]

* [[Ho(CombModCat)]]

[[!include flavors of higher toposes -- list]]


[[!include locally presentable categories - table]]



## References

The terminology "model topos" is due to:

* {#Rezk} [[Charles Rezk]], _Toposes and homotopy toposes_, 2010 ([pdf](https://rezk.web.illinois.edu/homotopy-topos-sketch.pdf), [[Rezk_HomotopyToposes.pdf:file]])

Essentially this idea appears earlier in:

* {#Simpson99} [[Carlos Simpson]],  *A Giraud-type characterization of the simplicial categories associated to closed model categories as $\infty$-pretopoi* ([arXiv:math/9903167](http://arxiv.org/abs/math/9903167))

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry I: Topos theory_, Advances in Mathematics **193** 2 (2005)  257-372  &lbrack;[arXiv:math.AG/0207028](http://arxiv.org/abs/math.AG/0207028), [doi:10.1016/j.aim.2004.05.004](https://doi.org/10.1016/j.aim.2004.05.004)&rbrack;

In the context of [[categorical semantics]] for [[univalence|univalent]] [[homotopy type theory]], the combination of terminology "model topos" with *[[type-theoretic model category]]* to *type-theoretic model topos*:

* {#Shulman19} [[Michael Shulman]], §1.3 in: _All $(\infty,1)$-toposes have strict univalent universes_ ([arXiv:1904.07004](https://arxiv.org/abs/1904.07004))

reviewed in


* {#Riehl22} [[Emily Riehl]], §6.1 of: *On the $\infty$-topos semantics of homotopy type theory*, lecture at *[Logic and higher structures](https://conferences.cirm-math.fr/2689.html)* CIRM (Feb. 2022) &lbrack;[pdf](https://emilyriehl.github.io/files/semantics.pdf), [[Riehl-InfinityToposSemantics.pdf:file]]&rbrack;



[[!redirects model toposes]]
[[!redirects model topoi]]

[[!redirects type-theoretic model topos]]
[[!redirects type-theoretic model topoi]]
[[!redirects type-theoretic model toposes]]

[[!redirects type theoretic model topos]]
[[!redirects type theoretic model topoi]]
[[!redirects type theoretic model toposes]]

