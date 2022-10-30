
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [classification](http://ncatlab.org/nlab/show/SCFT#Classification) of [[superconformal field theories]] predicts the existence of such a theory with $(2,0)$-[[supersymmetry]] in [[dimension]] 6, which is such that it contains a [[self-dual higher gauge theory]] whose field configurations are [[connections on a 2-bundle]] (a [[circle n-bundle with connection|circle 2-bundle with connection]] in the abelian case).

It is expected ([Witten](#Witten07)) that such theories arise as the [[worldvolume]] theories of [[M5-brane]]s and that their compactifications are at the heart of the phenomenon that leads to [[S-duality]] and hence [[geometric Langlands duality]] ([Witten](#Witten09)).

Due to the [[self-dual higher gauge theory|self-duality]] a characterization of these theories by an [[action functional]] is at best subtle, maybe impossible. Therefore more direct descriptions are still under investigation (for instance [SSW11](#SSW11)). A review of recent developments is in ([Moore11](#Moore)).

## Properties

### Holographic dual

Under [[AdS-CFT|AdS7/CFT6]] the 6d $(2,0)$-superconformal QFT is supposed to be dual to [[11-dimensional supergravity|M-theory]] on [[anti de Sitter spacetime]] $AdS_7 \times S^4$.  

See [[AdS/CFT correspondence]] for more on this.

### Solitonic 1-branes

The 5d $(2,0)$-[[SCFT]] has tensionless 1-[[brane]] configurations. From the point of view of the ambient [[11-dimensional supergravity]] these are the boundaries of [[M2-branes]] ending on the [[M5-branes]]. ([GGT](#GGT))

### Compactification on a Riemann surface

The [[Kaluza-Klein mechanism|compactification]] of the 5-brane on a [[Riemann surface]] yields as [[worldvolume]] [[theory (physics)|theory]] [[N=2 D=4 super Yang-Mills theory]]. See at _[N=2 D=4 SYM -- Construction by compactification of 5-branes](N%3D2+D%3D4+super+Yang-Mills+theory#ConstructionByCompactificationOf5Branes)_.


The _[[AGT correspondence]]_ relates  the [[partition function]] of $SU(2)^{n+3g-3}$-[[N=2 D=4 super Yang-Mills theory]] obtained by [[Kaluza-Klein mechanism|compactifying]] the $6d$ M5-brane theory on a [[Riemann surface]] $C_{g,n}$ of [[genus]] $g$ with $n$ punctures to 2d [[Liouville theory]] on $C_{g,n}$. 

## Related entries

* [[2d (2,0)-superconformal QFT]]

[[!include gauge theory from AdS-CFT -- table]]


[[!include table of branes]]

## References

### General

The first indication of a 6d theory with a self-dual 2-form field appears in section 1 of 

* [[Edward Witten]], _Some comments on string dynamocs_ ([hepth/9507121](http://arxiv.org/abs/hep-th/9507121))

Surveys include

* [[Greg Moore]], _On the role of six&#8208;dimensional $(2,0)$-theories in recent developments in
Physical Mathematics_ , talk at Strings2011 ([pdf slides](http://www.physics.rutgers.edu/~gmoore/Strings2011FinalPDF.pdf))
  {#Moore}

* [[Greg Moore]], _Applications of the six-dimensional (2,0) theories to Physical Mathematics_, [Felix Klein lectures Bonn (2012)](http://www.hcm.uni-bonn.de/events/eventpages/felix-klein-lectures/applications-of-the-six-dimensional-20-theories-to-physical-mathematics/) ([pdf](http://www.physics.rutgers.edu/~gmoore/FelixKleinLectureNotes.pdf))

See also the references and discussion at _[[M5-brane]]_.

### Compactification to 4d super-Yang-Mills

The conformal structure of the 6d theory and its relation under [[Kaluza-Klein mechanism|compactification]] on a [[Riemann surface]] to [[electric-magnetic duality]]/[[S-duality]] in 4-dimensions is discussed in

* [[Edward Witten]], _[[Conformal field theory in four and six dimensions]]_ in [[Ulrike Tillmann]] (ed.) _Topology, geometry and quantum field theory_ LMS Lecture Note Series (2004) ([arXiv:0712.0157](http://arxiv.org/abs/0712.0157))
 {#Witten07}

and the resulting relation to the [[geometric Langlands correspondence]] is disucssed in 

* [[Edward Witten]], _Geometric Langlands From Six Dimensions_ ([arXiv:0905.2720](http://arxiv.org/abs/0905.2720))
 {#Witten09}.

For more references on this see at _[[N=2 D=4 super Yang-Mills theory]]_ the section _[References - Constructions from 5-branes](N%3D2+D%3D4+super+Yang-Mills+theory#ConstructionByCompactificationOf5Branes)_.


### Models and special properties
 {#ModelsAndSpecialProperties}

A proposal for related higher nonabelian differential form data is made in 

* [[Henning Samtleben]], Ergin Sezgin, Robert Wimmer, _(1,0) superconformal models in six dimensions_ ([arXiv:1108.4060](http://arxiv.org/abs/1108.4060))
 {#SSW11}

Since by [[transgression]] every nonabelian [[principal 2-bundle]]/[[gerbe]] gives rise to some kind of nonabelian 1-bundle on [[loop space]] it is clear that some parts (but not all) of the nonabelian gerbe theory on the 5-brane has an equivalent reformulation in terms of ordinary gauge theory on the [[loop space]] of the 5-brane and possibly for gauge group the [[loop group]] of the original gauge group. 

Comments along these lines have been made in 

* [[Andreas Gustavsson]], _Selfdual strings and loop space Nahm equations_ ([arXiv:0802.3456](http://arxiv.org/abs/0802.3456)).

In fact, via the [[strict 2-group]] version of the [[string 2-group]] there is a local gauge in which the loop group variables appear already before transgression of the 5-brane gerbe to loop space. This is discussed from a [[holographic principle|holographic]] point of view in

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane]]_ 

### On the holographic dual 
 {#ReferencesOnTheHolographicDual}

The basics of the relation of the 6d theory to a 7d theory under [[AdS-CFT]] is reviewed [[holographic principle|holographic duality]]


* [[Juan Maldacena]], _The Large N limit of superconformal field theories and supergravity_, Adv. Theor. Math. Phys. 2:231, 1998, [hep-th/9711200](http://arxiv.org/abs/hep-th/9711200); _Wilson loops in Large N field theories_, Phys. Rev. Lett. __80__ (1998) 4859, [hep-th/9803002](http://arxiv.org/abs/hep-th/9803002)
 {#Maldacena}

The argument that the abelian [[7d Chern-Simons theory]] of a [[circle n-bundle with connection|3-connection]] yields this way the [[conformal blocks]] of the abelian [[self-dual higher gauge theory]] of the 6d theory on a _single_ brane is due to

* [[Edward Witten]], _Five-Brane Effective Action In M-Theory_ J. Geom. Phys.22:103-133,1997 ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))
 {#WittenI}

* [[Edward Witten]], _AdS/CFT Correspondence And Topological Field Theory_ JHEP 9812:012,1998 ([arXiv:hep-th/9812012](http://arxiv.org/abs/hep-th/9812012)) 
 {#Witten98}

The nonabelian generalization of this 7d action functional that follows from taking the quantum corrections ([[Green-Schwarz mechanism]] and flux quantization) of the [[supergravity C-field]] into account is discussed in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane]]_

See also

* [[Eric D'Hoker]], John Estes, Michael Gutperle, Darya Krym, 

  _Exact Half-BPS Flux Solutions in M-theory I
Local Solutions_ ([arXiv:0806.0605](http://arxiv.org/abs/0806.0605))

  _Exact Half-BPS Flux Solutions in M-theory II: Global solutions asymptotic to $AdS_7 \times S^4$ ([arXiv:0810.4647](http://arxiv.org/abs/0810.4647))
  {#HEGK}

### Solitonic 1-brane excitations

* [[Jerome Gauntlett]], [[Joaquim Gomis]], [[Paul Townsend]], _BPS Bounds for Worldvolume Branes_ ([arXiv:hep-th/9711205](http://arxiv.org/abs/hep-th/9711205))
 {#GGT}

* P.S. Howe, [[Neil Lambert]], [[Peter West]], _The Threebrane Soliton of the M-Fivebrane_ ([arXiv:hep-th/9710033](http://arxiv.org/abs/hep-th/9710033))

### Relation to extended TQFT

Relation to [[extended TQFT]] is discussed in

* [[Dan Freed]], _[[4-3-2 8-7-6]]_


[[!redirects 6d (2,0)-susy QFT]]
[[!redirects 6d (2,0)-superconformal QFT]]