
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

On manifolds with rational [[string structure]] the [[Witten genus]] takes values in [[modular forms]]. On manifolds with actual [[string structure]] this refines further to a ring of "topological modular forms". This ring is at the same time the ring of [[homotopy groups]] of an [[E-∞ ring]] spectrum, called _[[tmf]]_.

## Properties

### Relation to modular forms

Write $\overline{\mathcal{M}}$ for the [[Deligne-Mumford compactification]] of the [[moduli stack of elliptic curves]] regarded as a [[derived scheme]], such that [[tmf]] is defined as the [[global sections]] of the derived [[structure sheaf]]

$$
  tmf = \mathcal{O}(\overline{\mathcal{M}})
  \,.
$$

Write $\omega$ for the standard [[line bundle]] on $\overline{\mathcal{M}}$ such that the [[sections]] of $\omega^{\otimes k}$ are the ordinary [[modular forms]] of weight $k$ (as discussed there).

Then there is the [[descent spectral sequence]]

$$
  H^s(\overline{M}, \omega^{\otimes t}) \Rightarrow tmf_{2t-s}
$$

and since the ordinary modular forms embed on the left as

$$
  H^0(\overline{\mathcal{M}}, \omega^{\otimes t}) \hookrightarrow
   H^s(\overline{M}, \omega^{\otimes t})
$$

this induces an [[edge morphism]]



$$
  tmf_{2 \bullet} \longrightarrow MF_\bullet
$$

from topological modular forms to ordinary [[modular forms]].

The [[kernel]] and [[cokernel]] of this map are 2-[[torsion]] and 3-[[torsion]] and hence "away from 6" this map is an [[isomorphism]].


## Related concepts

* [[modular form]]

* [[Jacobi form]]

##  References 

See also the references at _[[tmf]]_. 

An introductory exposition is in 

* {#MazelGee13} [[Aaron Mazel-Gee]], _You could've invented $tmf$_, April 2013 ([pdf slides](http://math.berkeley.edu/~aaron/writing/ustars-tmf-beamer.pdf))

A collection of resources is in

* [[Nora Ganter]], _[Topological modular forms literature list](http://www.ms.unimelb.edu.au/~nganter/talbot/index.html)_


The original identification of topological modular forms as the coefficient ring of the [[tmf]] [[E-∞ ring]] and the refinement of the [[Witten genus]] to a morphism of [[E-∞ rings]], hence to the [[string orientation of tmf]] is due to 

* [[Michael Hopkins]], _Topological modular forms, the Witten Genus, and the theorem of the cube_, Proceedings of the International Congress of Mathematics, Z&#252;rich 1994 ([pdf](http://www.mathunion.org/ICM/ICM1994.1/Main/icm1994.1.0554.0565.ocr.pdf))

* [[Michael Hopkins]], _Algebraic topology and modular forms_, Proceedings of the ICM, Beijing 2002, vol. 1, 283--309 ([arXiv:math/0212397](http://arxiv.org/abs/math/0212397))

* [[Matthew Ando]], [[Michael Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))
  {#AndoHopkinsRezk}

see also remark 1.4 of

* [[Paul Goerss]], _Topological modular forms (after Hopkins, Miller and Lurie)_ ([pdf](http://arxiv.org/PS_cache/arxiv/pdf/0910/0910.5130v1.pdf)).

and for more on the [[sigma-orientation]] see

* [[Matthew Ando]], _The sigma orientation for analytic circle-equivariant elliptic cohomology_, Geom. Topol. 7 (2003) 91-153 ([arXiv:math/0201092](http://arxiv.org/abs/math/0201092))

Equivariant topological modular forms are discussed in 

* [[David Gepner]], [[Lennart Meier]], _On equivariant topological modular forms_, ([arXiv:2004.10254](https://arxiv.org/abs/2004.10254))




[[!redirects topological modular forms]]