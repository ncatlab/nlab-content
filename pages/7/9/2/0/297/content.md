<div class="rightHandSide toc">
[[!include physicscontents]]
</div>


_Functorial quantum field theory_, one of the two approaches of axiomatizing [[quantum field theory]]. The other is [[AQFT]]. FQFT formalizes the _Schr&ouml;dinger picture_ of quantum mechanics, while AQFT formalizes the _Heisenberg picture_.

#Idea#

Much work in quantum field theory is based on arguments using the [[path integral]]. While in the physics literature this is usually not a well defined object, it is generally assumed to satisfy a handful of properties, notably the _sewing laws_. These say, roughly, that the path integral over a domain $\Sigma$ which decomposes into subdomains $\Sigma_1$ and $\Sigma_2$ is the same as the path integral over $\Sigma_1$ composed with that over $\Sigma_2$.

##Formalization of sewing and locality in terms of functoriality##

It was in

* Michael Atiyah, _Topological quantum field theory_, Publications Math&eacute;matique de l'IH&Eacute;S, 68  (1988), p. 175-186

that it was realized that 

* this means that this property can be taken as the <em>defining</em> property of the path integral, thereby circumventing the problem of constructing it as an actual integral;

* this property can be conveniently axiomatized by saying that the path integral is a [[functor]] from a suitable category whose morphisms are [[cobordism]]s to a category of vector spaces.

(Strictly speaking, Atiyah's original article mentions this functor slightly indirectly only.)

All this was originally formalized in the context of [[TQFT|topological quantum field theory]] only. This is the easiest case that already exhibits all the functoriality that is implied by "FQFT" but by far not the only case (see below).

A pedagogical exposition of how the physicist's way of thinking about the path integral leads to its definition as a functor is given in

* Kevin Walker, _TQFTs_ ([pdf](http://canyon23.net/math/tc.pdf))

A pedagogical exposition of the notion of quantum field theory as a functor on [[cobordism]]s is in 

* John Baez, _Quantum quandaries: a Category-Theoretic perspective_ ([arXiv](http://arxiv.org/abs/quant-ph/0404040))

and a review of much of the existing material in the literature is in 

* Bruce H. Bartlett, _Categorical Aspects of Topological Quantum Field Theories_ ([arXiv](http://arxiv.org/abs/math/0512103)).

##Non-topological FQFTs (especially conformal)## 

This mostly concentrates on [[TQFT|topological quantum field theories]], those where the path integral depends only on the diffeomorphism class of the domain it is evaluated on. This is the simplest and by far best understood case. But the idea of functorial FQFT is not restricted to this case.

This was realized in

* Graeme Segal, _The definition of conformal field theory_, in: _Topology, Geometry and quantum field theory_, London. Math. Soc. LNS 308, edited by U. Tillmann, Cambridge Univ. Press 2004, 247-343

There the notion of 2-dimensional [[conformal field theory]] is axiomatized as a functor on a category of 2-dimensional cobordisms with conformal structure.

(Apparently a similar definition has been given by Kontsevich, but never published.) The details of the category of conformal cobordisms can get a bit technical and slight variations of Segal's original definition may be necessary. The work by Huang and Kong can be regarded as a further refinement and maybe completion of Segal's program

* Yi-Zhi Huang, _Geometric interpretation of vertex operator algebras_, Proc. Natl. Acad. Sci. USA, Vol 88. (1991) pp. 9964-9968

* Liang Kong, _Open-closed field algebras_ Commun. Math. Physics. 280, 207-261 (2008) ([arXiv](http://arxiv.org/abs/math/0610293)).

A very concrete construction of functorial CFTs (for the special case of _rational_ CFTs) is provided by the 
[[FFRS-formalism]].

##Extended (multi-tiered) FQFT##

But one notices that the formalization of quantum field theory as a [[functor]] on [[cobordism]]s encodes only a small aspect of the full sewing law imagined to be satisfied by the path integral: In a 1-[[category]] of $n$-dimensional [[cobordism]]s these are glued along $(n-1)$-dimensional boundaries. One could imagine more generally a formalization where a given [[cobordism]] is allowed to be chopped into arbitrary parts of arbitrary co-dimension such that the path integral can still consistently be evaluated on each of these parts.

This leads to the notion of _extended quantum field theory_, which is taken to be an $\infty$-functor on an [[higher category theory|infinity category]] of [[extended cobordism]]s. Early ideas about a formalization of this approach were given in

* John Baez and Jim Dolan, _Higher-dimensional algebra and Topological Quantum Field Theory_  ([arXiv](http://arxiv.org/abs/q-alg/9503002)) .

Making this precise involves giving a precise definition of an $\infty$-category of cobordisms. Several approaches exist, such as

* Eugenia Cheng and Nick Gurski, _Towards an $n$-category of cobordisms_,
Theory and Applications of Categories,  Vol. 18, 2007, No. 10, pp 274-302.  ([tac](http://www.tac.mta.ca/tac/volumes/18/10/18-10abs.html))

or

* Marco Grandis, _Collared cospans, cohomotopy and TQFT (Cospans in Algebraic Topology, II)_, Dip. Mat. Univ. Genova, Preprint 555 (2007). ([pdf](http://www.dima.unige.it/~grandis/wCub2.pdf))

There is a long-term project by Stephan Stolz and Peter Teichner which originally tried to refine Segal's 1-functorial formulation of conformal field theory to a 2-functorial extended FQFT, as indicated in

* Stephan Stolz and Peter Teichner, _What is an elliptic object?_ ([pdf](http://math.berkeley.edu/~teichner/Papers/Oxford.pdf)).


More recently, Mike Hopkins and Jacob Lurie claimed 
([Hopkins-Lurie on Baez-Dolan](http://golem.ph.utexas.edu/category/2008/05/hopkinslurie_on_baezdolan.html))
to have found a complete coherent formalization of topological extended FQFT in the context of [[(infinity,1)-category|(infinity,n)-categories]] using an [[(infinity,n)-category of cobordisms]]. This is described in 

* [[Jacob Lurie]], [[On the Classification of Topological Field Theories]] 

A very detailed account of this for the 2-dimensional case is presented in

* Chris Schommer-Pries, _The Classification of Two-Dimensional Extended Topological Field Theories_, PhD thesis, Berkeley, 2009 ([pdf](http://sites.google.com/site/chrisschommerpriesmath/Home/my-web-documents/Schommer-Pries-Thesis-5-12-09.pdf?attredirects=0))

see also 

* [[extended topological quantum field theory]]


## (extended) FQFT from background fields: $\sigma$-models## 


In this context Dan Freed is picking up again his old work on higher algebraic structures in quantum field theory, as described in

* Daniel S. Freed, _Quantum Groups from Path Integrals_ ([arXiv](http://xxx.lanl.gov/abs/q-alg/9501025))

* Daniel S. Freed, _Higher Algebraic Structures and Quantization_ ([arXiv](http://arxiv.org/abs/hep-th/9212115))

where he argued that and how the path integral should assign $n$-categorical objects to domains of codimension $n$, and is re-expressing this in the $\infty$-functorial context.  (Freed speaks of _multi-tiered_ QFT instead of extended QFT.) 

* Daniel S. Freed, _Remarks on Chern-Simons Theory_ ([arXiv](http://arxiv.org/abs/0808.2507)).

Freed's ideas on how an extended or multi-tiered QFT arises from a path integral coming from a given background field were further formalized in the context of "finite" QFTs in

* Simon Willerton, _The twisted Drinfeld double of a finite group via gerbes and finite groupoids_ ([arXiv](http://arxiv.org/abs/math.QA/0503266))

* Bruce Bartlett, _On unitary 2-representations of finite groups and topological quantum field theory_, PhD thesis, Sheffield (2008) ([arXiv] (http://arxiv.org/abs/0901.3975))

There are indications that a complete picture of this involves [[groupoidification]] 

* Jeffrey Morton, _Extended TQFTs and Quantum Gravity_ ([arXiv](http://arxiv.org/abs/0710.0032))

and, more generally [[geometric function theory]]:

a big advancement in the understanding of extended $\sigma$-model QFTs is the discussion in

* David Ben-Zvi, John Francis, David Nadler,
_Integral Transforms and Drinfeld Centers in Derived Geometry_ ([arXiv](http://arxiv.org/abs/0805.0157))

which realizes $\sigma$-models by homming [[cobordism]] [[cospan]]s into the total spaces (realized as [[infinity-stack homotopically|infinity-stack]]) of background fields and regarding the resulting [[span]]s as pull-push operators on suitable [[geometric function theory|geometric functions]].  

A similar approach to bring the old work by Dan Freed mentioned above in contact with the picture of extended functorial QFT and the Baez-Dolan-Lurie structure theorem is

* Daniel S. Freed, Michael J. Hopkins, Jacob Lurie, Constantin Teleman, _Topological Quantum Field Theories from Compact Lie Groups_ ([arXiv](http://arxiv.org/abs/0905.0731)).

A related discussion concerning the construction of an extended FQFT from a higher categorical background field in the context of [[schreiber:Differential Nonabelian Cohomology|differential nonabelian cohomology]] is proposed in 

* [[schreiber:Nonabelian cocycles and their sigma model QFTs]]. 

A discussion of the relation between extended _FQFT_ and [[AQFT]] with further references is in

* Urs Schreiber, _AQFT from $n$-functorial QFT_ ([arXiv](http://arxiv.org/abs/0806.1079)).



## homological FQFT (and TCFT) ##

As usual, the problem of constructing FQFT becomes much more tractable when linear approximations are applied. In homological FQFT and in TCFT the Hom-spaces of the cobordism category (the moduli spaces of cobordisms with given punctures/boundaries) are approximated by complexes  of chains on them. This leads to formalization of $\infty$-functorial QFT in the context of differential graded algebra.

* Getzler

* Kontsevich

* Costello
 
  * [[factorization algebra]]

* etc.


[[!redirects FQFTs]]
[[!redirects Functorial quantum field theory]]
[[!redirects Functorial quantum field theories]]
[[!redirects functorial quantum field theory]]
[[!redirects functorial quantum field theories]]