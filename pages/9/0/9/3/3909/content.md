[[!redirects twistor]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Twistor space_ in the orginal sense of ([Penrose 67](#Penrose67)) is a [[complex manifold]] whose [[complex geometry]] is usefully related to the [[conformal geometry]] of ([[one-point compactification|compactified]] [[complexification|complexified]]) 4-dimensional [[Minkowski spacetime]]. The _Penrose transform_ from twistor space to this [[spacetime]] yields powerful computational tools for studying certain [[quantum field theories]], in particular 4d [[Yang-Mills theory]]. Notably it sends [[ordinary cohomology]] classes on twistor space to [[self-dual Yang-Mills theory|self-dual Yang-Mills fields]] on spacetime ([Ward 77](#Ward77), [Ward-Wells 90](#WardWells90)). Morever, when twistor space is taken as a [[target space]] for [[twistor string theory]], then it serves to compute the [[MHV amplitudes]] in [[super Yang-Mills theory]] ([Witten 03](#Witten03)).

This _Penrose transform_ is exhibited by a [[correspondence]] of [[coset spaces]]/[[flag varieties]]/[[Grassmannians]] which is a special case of general such [[correspondences]] as they are studied in [[Schubert calculus]], [[geometric representation theory]], [[parabolic geometry]]. Therefore one can consider "generalized twistors" to be elements of certain [[flag varieties]] and "generalized Penrose transforms" to be those induced by the relevant [[correspondences]]. ([Baston-Eastwood 89](#BastonEastwood89), [Cap 01](#Cap01)). 

In this generality given a [[semisimple Lie group]] $G$ and two [[parabolic subgroups]] $P_1$ and $P_2$ with [[intersection]] $P_1 \cap P_2$, then the _twistor correspondence_ is the [[correspondence]] (see at [Schubert calculus -- Correspondences](http://ncatlab.org/nlab/show/Schubert+calculus#Correspondences)) of the form

$$
  \array{
      && G/(P_1 \cap P_2)
      \\
      & {}^{\mathllap{p_1}}\swarrow && \searrow^{\mathrlap{p_2}}
     \\
     G/P_1 && && G/P_2
  }
$$

given by the [[projections]] onto the two [[coset spaces]]/[[flag varieties]] and a _Penrose transform_ is an [[integral transform]]/pull-[[fiber integration|push]] $(p_1)_! \circ (p_1)^\ast$ through this correspondence.

In particular there are higher twistor spaces corresponding to higher dimensional [[Minkowski spacetimes]] which are useful for disucssion higher dimensional [[quantum field theory]], notably there are twistor spaces for 6-dimensional spacetime useful for the study of the [[6d (2,0)-superconformal QFT]] on the [[worldvolume]] of the [[M5-brane]] ([MREIC 11](#MREIC11)) with its [[self-dual higher gauge field]], the [[B-field]] .

The original _twistor correspondence_ ([Penrose 67](#Penrose67)) is the [[correspondence]]


$$
  \left(
  \array{
    && Gr_{1,2}(\mathbb{C}^4)
    \\
    & \swarrow && \searrow
    \\
    \mathbb{C}P^3 && && Gr_2(\mathbb{C}^4)
  }
  \right)
  \;\;\;\;\; 
    \simeq
  \;\;\;\;\; 
  \left(
  \array{
    && SL_\mathbb{C}(4)/SL_{\mathbb{C}}(2)
    \\
    & \swarrow && \searrow
    \\
    SL_{\mathbb{C}}(4)/SL_{\mathbb{C}}(3) 
     && && 
    SL_{\mathbb{C}}(4)/(SL_{\mathbb{C}}(2)\times SL_{\mathbb{C}}(2))
  }  
  \right)
  \,,
$$

where 

* the [[Grassmannian]] $G_2(\mathbb{C}^4)$ of [[planes]] in complexified 4d [[Minkowski spacetime]];

* the **twistor space** is the [[complex projective space]] $\mathbb{C}P^3 = Gr_1(\mathbb{C}^4)$;

* the correspondence space $Gr_{1, 2}(\mathbb{C}^4)$ is the space of lines in planes in $\mathbb{C}^4$.


(e.g. [Ward-Wells 90](#WardWells90))

## Related concepts

* A real analog of this is the _[[Radon transform]]_.

* [[spinor]]

* [[twistor string theory]]

* [[MHV amplitude]]

* [[Radon transform]]

* [[Schubert calculus]]

* [[celestial sphere]], [[quadric]], [[Klein quadric]]

## References

### General

The notion originates in 

* [[Roger Penrose]], _Twistor algebra_,  Journal of Mathematical Physics 8 (2): 345&#8211;366, (1967) 
 {#Penrose67}

* [[Roger Penrose]], _The twistor programme, Reports on Mathematical Physics 12 (1): 65&#8211;76 (1977)

The relation to [[self-dual Yang-Mills theory]] is due to 

* R. S. Ward, _On Selfdual gauge fields_, Phys. Lett. A61 (1977) 81-82.
 {#Ward77}

Introductions and surveys include

* Fedja Hadrovich, _Twistor primer_ ([html](http://users.ox.ac.uk/~tweb/00004/), [pdf](http://henry.pha.jhu.edu/twistors.pdf))

* Paul Bair, _Introduction to twistors_ ([pdf](http://www.math.jussieu.fr/~helein/encyclopaedia/baird-twistors.pdf))

* S. A. Huggett, K. P. Tod, _An introduction to twistor theory_, Cambridge University Press (1985)

* Liana David, _The Penrose transform and its applications_, 2001 ([pdf](http://www.maths.ed.ac.uk/pg/thesis/david.pdf))

See also 

* Wikipedia, _[Twistor theory](http://en.wikipedia.org/wiki/Twistor_theory)_


### Relation to geometric representation theory and parabolic geometry

A discussion in the general context of [[geometric representation theory]] is in

* R. J. Baston, M. G. Eastwood, _The Penrose Transform Its Interaction with Representation Theory_ Oxford Science Publications, Clarendon Press, 1989 
 {#BastonEastwood89}

and the further generalization to [[Cartan geometry]]/[[parabolic geometry]] is discussed in

* [[Andreas Cap]], _Correspondence spaces and twistor spaces for parabolic geometries_, J. Reine Angew. Math. 582 (2005) 143-172 ([arXiv:math/0102097](http://arxiv.org/abs/math/0102097))
  {#Cap01}

### Application to quantum field theory

More on traditional applications to [[quantum field theory]] is in 

* R.S. Ward, R.O. Wells, _Twistor geometry and field theory_, Cambridge Univ. Press 1990.
  {#WardWells90}

The relation of twistor geometry to [[MHV amplitudes]] in 4d [[Yang-Mills theory]] and [[twistor string theory]] is due to 

* [[Edward Witten]], _Perturbative Gauge Theory As A String Theory In Twistor Space_, Commun. Math. Phys. 252:189-258, 2004 ([arXiv:hep-th/0312171](http://arxiv.org/abs/hep-th/0312171))
  {#Witten03}

Surveys of the resulting modern application of twistors in field theory include

* David Skinner, _The geometry of scattering amplitudes_, talk notes, November 2009 ([pdf](http://research.physics.unc.edu/string/transparencies/trans_20091112.pdf))

### Application to the 6d self-dual 2-form field

A general discussion of the Penrose-Ward-type transform applied to [[circle 2-bundles]] on twistor space is in 

* [[David Chatterjee]], sections 4 and 8 of _On Gerbs_, 1998 ([pdf](http://people.maths.ox.ac.uk/hitchin/hitchinstudents/chatterjee.pdf))

The application of twistor methods to the [[6d (2,0)-superconformal QFT]] is discussed for instance in 

* L. J. Mason, R. A. Reid-Edwards, A. Taghavi-Chabert, _Conformal Field Theories in Six-Dimensional Twistor Space_, J. Geom. Phys. 62 (2012), no. 12, 2353-2375 ([arXiv:1111.2585](http://arxiv.org/abs/1111.2585))
 {#MREIC11}



[[!redirects twistor theory]]

[[!redirects twistor space]]
[[!redirects twistor spaces]]

[[!redirects twistor correspondence]]
[[!redirects twistor correspondences]]

[[!redirects Penrose transform]]
[[!redirects Penrose transforms]]

[[!redirects Penrose transformation]]
[[!redirects Penrose transformations]]

[[!redirects Penrose twistor transform]]
[[!redirects Penrose twistor transforms]]

[[!redirects Penrose twistor transformation]]
[[!redirects Penrose twistor transformations]]

[[!redirects Penrose-Ward transform]]
[[!redirects Penrose-Ward transforms]]

[[!redirects Penrose-Ward transformation]]
[[!redirects Penrose-ward transformations]]

[[!redirects Penrose-Ward twistor transform]]
[[!redirects Penrose-Ward twistor transforms]]

[[!redirects Penrose-Ward twistor transformation]]
[[!redirects Penrose-Ward twistor transformations]]