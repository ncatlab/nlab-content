
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
* automatic table of contents goes here
{:toc}

## Idea

The _model structure on strict $\omega$-categories_ is a [[model category]] structure that presentes the [[(∞,1)-category]] of [[strict ∞-categories]].

It resticts to the [[model structure on strict ∞-groupoids]].

These structures also go by the name [[canonical model structure]] or [[folk model structure]].



## Properties

+-- {: .un_lemma}
###### Observation

Every object is fibrant. The acyclic fibrations are precisely the functors that are [[k-surjective functor]]s for all $k \in \mathbb{N}$.

=--

+-- {: .un_theorem}
###### Theorem


The [[transferred model structure]] on [[Str∞Grpd]] along the [[forgetful functor]]

$$
  U : Str \omega Grpd \to Str \omega Cat
$$

exists and coincides with the [[model structure on strict ∞-groupoids]] defined in ([BrownGolasinski](#BrownGolasinski)).

=--

This is proven in ([AraMetayer](#AraMetayer)).

## References

The [[model structure on strict ∞-groupoids]] was introduced in

* [[Ronnie Brown]], Marek Golasinski; _A model structure for the homotopy theory of crossed complexes_ ([numdam](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1989__30_1_61_0))
{#BrownGolasinski}

The model structure on strict $\omega$-categories was discussed in

* [[Yves Lafont]], [[Francois Métayer]], [[Krzysztof Worytkiewicz]], _A folk model structure on omega-cat_ ([arXiv](http://arxiv.org/abs/0712.0617))


Dicussion of cofibrant [[resolution]] in this model structure by [[polygraph]]s/[[computad]] is in

* [[Francois Métayer]], _Cofibrant complexes are free_ ([arXiv](http://arxiv.org/abs/math.CT/0701746))

* [[Francois Métayer]], _Resolutions by polygraphs_ ([tac](http://www.tac.mta.ca/tac/volumes/11/7/11-07.pdf))

The relation betwee then model structure on strict $\omega$-categories and that on strict $\omega$-groupoids is established in

* Dimitri Ara, [[Francois Metayer]], _The Brown-Golasinski model structure on $\infty$-groupoids revisited_ ([pdf](http://hal.archives-ouvertes.fr/docs/00/52/58/42/PDF/folkgr.pdf))
{#AraMetayer}

[[!redirects model structure on strict ∞-categories]]