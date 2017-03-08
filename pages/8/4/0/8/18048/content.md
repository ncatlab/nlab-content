
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[model category]] structure on the category of [[comodules]] in [[chain complexes]] over a [[dg-coalgebra]].


## Details

Let $C$ be a [[differential graded-cocommutative coalgebra]] over a [[field]]. 

**Model structure of the second kind**

There exists a [[model category]] structure on the category $C dgCoMod$ of [[dg-comodules]] over $C$ whose

* weak equivalences are the [[quasi-isomorphisms]];

* fibrations are the [[surjections]] whose [[kernel]] is such that its underlying [[comodule]] over the underlying [[coalgebra]] of $C$ is an [[injective object]].

This is due to ([Positelski 11, 8.2 Theorem (a)](#Positelski11)).

**Model structure of the first kind**

There is another model structure where the fibrations in addition satisfy the condition that their kernel $K$ satisfies that for all acyclic $N$, then $\underline{Hom}_C(N,K)$ is acyclic.

This is due to ([Positelski 11, 8.2 Remark](#Positelski11)), there called the "model category structure of the first kind".  This is also reviewed as ([Pridham 13, prop. 2.2](#Pridham13)).


## Related concepts

* [[model structure on dg-coalgebras]]

* [[model structure on coalgebras over a comonad]]

## References

* {#Positelski11} [[Leonid Positselski]], _Two kinds of derived categories, Koszul duality, and comodule-contramodule correspondence_, Memoirs of the Amer. Math. Soc. 212 (2011), no.996, ([arXiv:0905.2621](https://arxiv.org/abs/0905.2621))

* {#Pridham13} [[Jonathan Pridham]], _Tannaka duality for enhanced triangulated categories_ ([arXiv:1309.0637](https://arxiv.org/abs/1309.0637))
