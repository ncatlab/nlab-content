[[!redirects twistor]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Twistor space_ in the orginal sense of ([Penrose 67](#Penrose67)) is a [[complex manifold]] whose [[complex geometry]] is usefully related to the [[conformal geometry]] of ([[one-point compactification|compactified]] [[complexification|complexified]]) 4-dimensional [[Minkowski spacetime]]. The _Penrose transform_ from twistor space to this [[spacetime]] yields powerful computational tools for studying certain [[quantum field theories]], in particular 4d [[Yang-Mills theory]] (e.g. [Ward-Wells 90](#WardWells90), [Witten 03](#Witten03)).

This _Penrose transform_ is exhibited by a [[correspondence]] of [[coset spaces]]/[[flag varieties]]/[[Grassmannians]] which is a special case of general such [[correspondences]] as they are studied in [[Schubert calculus]], [[geometric representation theory]], [[parabolic geometry]]. Therefore one can consider "generalized twistors" to be elements of certain [[flag varieties]] and "generalized Penrose transforms" to be those induced by the relevant [[correspondences]]. ([Baston-Eastwood 89](#BastonEastwood89), [Cap 01](#Cap01)). 

In this generality given a [[semisimple Lie group]] $G$ and two [[parabolic subgroups]] $P_1$ and $P_2$ with [[intersection]] $B \coloneqq$ (typically a [[Borel subgroup]], see at [Schubert calculus -- Correspondences](http://ncatlab.org/nlab/show/Schubert+calculus#Correspondences)), then the _twistor correspondence_ is the [[correspondence]]

$$
  \array{
      && G/B
      \\
      & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
     \\
     G/P_1 && && G/P_2
  }
$$

given by the [[projections]] onto the two [[coset spaces]]/[[flag varieties]] and a _Penrose transform_ is an [[integral transform]]/pull-[[fiber integration|push]] $(p_1)_! \circ (p_1)^\ast$ through this correspondence.

In particular there are higher twistor spaces corresponding to higher dimensional [[Minkowski spacetimes]] which are useful for disucssion higher dimensional [[quantum field theory]], notably there are twistor spaces for 6-dimensional spacetime useful for the study of the [[6d (2,0)-superconformal QFT]] on the [[worldvolume]] of the [[M5-brane]]. ([MREIC 11](#MREIC11))

The original _twistor correspondence_ ([Penrose 67](#Penrose67)) is the [[correspondence]] for $G = SL(4,\mathbb{C})$


$$
  \array{
    && Gr_{1,2}(\mathbb{C}^4)
    \\
    & \swarrow && \searrow
    \\
    \mathbb{C}P^3 && && Gr_2(\mathbb{C}^4)
  }
  \,,
$$

where 

* the [[Grassmannian]] $G_2(\mathbb{C}^4)$ of [[planes]] in complexified 4d [[Minkowski spacetime]];

* the **twistor space** is the [[complex projective space]] $\mathbb{C}P^3 = Gr_1(\mathbb{C}^4)$;

* the correspondence space is the space of lines in planes in $\mathbb{C}^4$.


(e.g. [Ward-Wells 90](#WardWells90))

## Related concepts

+ [[spinor]]

* [[twistor string theory]]

* [[MHV amplitude]]

## References

The notion originates in 

* [[Roger Penrose]], _Twistor algebra_,  Journal of Mathematical Physics 8 (2): 345&#8211;366, (1967) 
 {#Penrose67}

* [[Roger Penrose]], _The twistor programme, Reports on Mathematical Physics 12 (1): 65&#8211;76 (1977)

Introductions and surveys include

* Paul Bair, _Introduction to twistors_ ([pdf](http://www.math.jussieu.fr/~helein/encyclopaedia/baird-twistors.pdf))

* S. A. Huggett, K. P. Tod, _An introduction to twistor theory_, Cambridge University Press (1985)

* Liana David, _The Penrose transform and its applications_, 2001 ([pdf](http://www.maths.ed.ac.uk/pg/thesis/david.pdf))

A discussion in the general context of [[geometric representation theory]] is in

* R. J. Baston, M. G. Eastwood, _The Penrose Transform Its Interaction with Representation Theory_ Oxford Science Publications, Clarendon Press, 1989 
 {#BastonEastwood89}

and the further generalization to [[Cartan geometry]]/[[parabolic geometry]] is discussed in

* [[Andreas Cap]], _Correspondence spaces and twistor spaces for parabolic geometries_, J. Reine Angew. Math. 582 (2005) 143-172 ([arXiv:math/0102097](http://arxiv.org/abs/math/0102097))
  {#Cap01}

More on applications to [[quantum field theory]] is in 

* R.S. Ward, R.O. Wells, _Twistor geometry and field theory_, Cambridge Univ. Press 1990.
  {#WardWells90}

The relation of twistor geometry to [[MHV amplitudes]] in 4d [[Yang-Mills theory]] and [[twistor string theory]] is due to 

* [[Edward Witten]], _Perturbative Gauge Theory As A String Theory In Twistor Space_, Commun. Math. Phys. 252:189-258, 2004 ([arXiv:hep-th/0312171](http://arxiv.org/abs/hep-th/0312171))
  {#Witten03}

The application of twistor methods to the [[6d (2,0)-superconformal QFT]] is discussed for instance in 

* L. J. Mason, R. A. Reid-Edwards, A. Taghavi-Chabert, _Conformal Field Theories in Six-Dimensional Twistor Space_, J. Geom. Phys. 62 (2012), no. 12, 2353-2375 ([arXiv:1111.2585](http://arxiv.org/abs/1111.2585))
 {#MREIC11}


See also 

* Wikipedia, _[Twistor theory](http://en.wikipedia.org/wiki/Twistor_theory)_

[[!redirects twistor theory]]

[[!redirects twistor space]]
[[!redirects twistor spaces]]

[[!redirects twistor correspondence]]
[[!redirects twistor correspondences]]