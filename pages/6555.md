
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Ricci flow_ is the [[gradient flow]] of the [[action functional]] of [[dilaton gravity]]: the [[Einstein-Hilbert action]] coupled to a [[dilaton field]]. 

Equivalently it is the [[renormalization group flow]] of the [[bosonic string]] [[sigma-model]] for [[background gauge field|background fields]] containing [[gravity]] and [[dilaton]] (reviewed e.g. in [Woolgra 07](#Woolgra07), [Carfora 10](#Carfora10), see also the introduction of [Tseytlin 06](#Tseytlin06)).

In ([Perelman 02](#Perelman02)) Ricci flow for dilaton gravity in 3d was shown to enjoy sufficient monotonicity properties such as to complete [[Richard Hamilton]]'s proof of the [[Poincaré conjecture]].
Hamilton's strategy was to equip a compact simply connected 3d manifold with a [[Riemannian metric]], argue that its Ricci flow will, after many "pinchings" (points where the metric degenerates) produce a collection of 3-[[spheres]] and conclude that therefor the original manifold must have been a 3-sphere, too. The technical problem is to control the number of pinchings, which may occur rapidly. Adding also the [[dilaton field]] turns out not to change the qualitative nature of the flow but make it "monotone enough" to control the pinching.

In [Rubinstein-Sinclair](#RubinsteinSinclair) a typical such Ricci flow with pinchings is visualized as follows:

<img src="http://i.stack.imgur.com/FmUuW.png" alt="" />


## References

### General

A quick survey is in the slides

* Annibale Magni, _Perelman's dilaton_ ([pdf](http://www.sissa.it/fa/difftop2010/dwnld/Magni.pdf)).

and a detailed survey is in 

* [[Terry Tao]], _Ricci flow as a gradient flow, log-Sobolev inequalities, and Perelman entropy_ ([blog post](http://terrytao.wordpress.com/2008/04/24/285a-lecture-8-ricci-flow-as-a-gradient-flow-log-sobolev-inequalities-and-perelman-entropy/))

Visualization is in 

* {#RubinsteinSinclair} J. Hyam Rubinstein and Robert Sinclair. "Visualizing Ricci Flow of Manifolds of Revolution", Experimental Mathematics v. 14 n. 3, pp. 257&#8211;384.

The monotonicity of the Ricci flow for the [[string]] [[sigma-model]] in [[dilaton gravity]] background was established in 

* {#Perelman02} [[Grigori Perelman]], _The entropy formula for the Ricci flow and its geometric applications_ ([arXiv:math/0211159](http://arxiv.org/abs/math/0211159))

This was a key step in his completion of Hamilton's program for how to prove the [[Poincare conjecture]].

### As sigma-model renormalization group flow
 {#ReferencesAsSigmaModelRenormalizationGroupFlow}

The identification of Ricci flow with the [[renormalization group flow]] of the [[bosonic string]] [[sigma-model]] is reviewed for instance in 

* Kasper Olsen, _[From Polyakov to Perelman](http://kasperolsen.wordpress.com/2010/03/19/from-polyakov-to-perelman-history-of-the-ricci-flow-and-a-millennium-prize/)_

* {#Woolgra07} E. Woolgar, _Some Applications of Ricci Flow in Physics_, Can.J.Phys.86:645,2008 ([arXiv:0708.2144](http://arxiv.org/abs/0708.2144))

* {#Carfora10} Mauro Carfora, _Renormalization Group and the Ricci flow_ ([arXiv:1001.3595](http://arxiv.org/abs/1001.3595))

and discussed in more detail for instance in 

* T Oliynyk, V Suneeta, E Woolgar, _Irreversibility of World-sheet Renormalization Group Flow_, Phys.Lett. B610 (2005) 115-121 ([arXiv:hep-th/0410001](http://arxiv.org/abs/hep-th/0410001))

* T Oliynyk, V Suneeta, E Woolgar, _A Gradient Flow for Worldsheet Nonlinear Sigma Models_, Nucl.Phys. B739 (2006) 441-458 ([arXiv:hep-th/0510239](http://arxiv.org/abs/hep-th/0510239))

* {#Tseytlin06} [[Arkady Tseytlin]], _On sigma model RG flow, "central charge" action and Perelman's entropy_, Phys.Rev.D75:064024,2007 ([arXiv:hep-th/0612296](http://arxiv.org/abs/hep-th/0612296))

See also at _[string theory -- References -- Fields medal work related to string theory](string+theory#FieldMedalWork)_.

See also

* Alexander Frenkel, Petr Horava, Stephen Randall, _Topological Quantum Gravity of the Ricci Flow_ ([arXiv:2010.15369](https://arxiv.org/abs/2010.15369))

 