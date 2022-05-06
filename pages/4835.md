

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[quantum field theory]] the term _operator product expansion_ (OPE) refers to [[Taylor expansion]] of products in the [[algebra of quantum observables]] of [[field observables]] $\mathbf{\Phi}^a(x)$ in the form

$$
  \label{SchematicOPE}
  \mathbf{\Phi}^a(x) \mathbf{\Phi}^b(y)
  \;\sim\;
  C^{a b}{}_c(x) \mathbf{\Phi}^c(y)
  \,.
$$

Here "$\sim$" means something like "as $x$ gets close to $y$ the [[expectation values]] in the given [[vacuum state]] of [[observables]] proportional to the left hand side approach those of observables proportional to the right hand side", schematically:

$$
  \left\langle
    \mathbf{\Phi}^a(x) \mathbf{\Phi}^b(y)
    A
  \right\rangle
  \underset{x \to y}{\longrightarrow}
  C^{a b}{}_c(x)
  \left\langle
    \mathbf{\Phi}^c(y)
    A
  \right\rangle
$$

If the [[algebra of observables]] is [[representation|represented]] via [[operator-valued distributions]] [[action|acting]] on some [[Hilbert space]], as commonly assumed, then this becomes an expansion of ([[product of distributions|distributional]]) [[operator products]], whence the name _operator product expansion_ ([Wilson 69](#Wilson69), [Wilson-Zimmermann 72](#WilsonZimmermann72)).

For [[conformal field theory]] and specifically for [[2d CFT]] the operator product expansion is well understood, is neatly captured by the concept of [[vertex operator algebras]]. Via the _[[conformal bootstrap]]_ the equation (eq:SchematicOPE) defines or at least constrains the conformal field theory ([Ferrara-Grillo-Gatto 73](#FerraraGrilloGatto73), [Polyakov 74](#Polyakov74), [Belavin-Polyakov-Zamolodchikov 84](#BelavinPolyakovZamolodchikov84)).

Attempts to similarly use the concept of the operator product expansion to _define_ more general [[perturbative quantum field theory]] (and possibly [[non-perturbative quantum field theory]]) are discussed in ([Hollands-Olbermann 09](#HollandsOlbermann09), [Holland-Hollands 13](#HollandHollands13)). The concept of [[factorization algebras]], rooted as it is in that of [[vertex operator algebras]], may be thought of as meaning to axiomatize operator product expansions in the generality of Euclidean ([[Wick rotation|Wick rotated]]) field theory.

Apparently [Kontsevich 10](#Kontsevich10) suggested that [[perturbative QFT]] should be thought of as the [[deformation theory]] controlled by a certain [[L-infinity algebra]] which is constructed from OPEs.

## See also

* [[Vertex operator algebra]]

## References

The general concept is due to 
 
* {#Wilson69} [[Kenneth Wilson]], _Nonlagrangian models of current algebra_, Phys. Rev., 179:1499–1512, 1969.

* {#WilsonZimmermann72} [[Kenneth Wilson]], [[Wolfhart Zimmermann]], _Operator product expansions and composite field operators in the general framework of quantum field theory_, Commun. Math. Phys., 24:87–106, 1972

and is further developed in

* {#HollandsOlbermann09} [[Stefan Hollands]], Heiner Olbermann, _Perturbative Quantum Field Theory via Vertex Algebras_, J. Math. Phys. 50:112304, 2009 ([arXiv:0906.5313](https://arxiv.org/abs/0906.5313))

* {#HollandHollands13} Jan Holland, [[Stefan Hollands]], _Operator product expansion algebra_,  	J. Math. Phys. 54, 072302 (2013) ([arXiv:1205.4904](https://arxiv.org/abs/1205.4904))

Development for [[AQFT on curved spacetime|QFT on curved spacetimes]]:

* [[Stefan Hollands]], [[Robert Wald]], _Axiomatic quantum field theory in curved spacetime_, Commun. Math. Phys. 293:85-125, 2010 ([arXiv:0803.2003](https://arxiv.org/abs/0803.2003))


Brief survey:

* _[Operator Product Expansion](http://home.uni-leipzig.de/tet/?page_id=288)_

The relevance of the concept of OPEs to [[conformal field theory]] ([[conformal bootstrap]]) was noticed in

* {#FerraraGrilloGatto73} S. Ferrara, A. F. Grillo, and R. Gatto, _Tensor representations of conformal algebra and conformally covariant operator product expansion_, Annals Phys. 76 (1973) 161–188

* {#Polyakov74} [[Alexander Polyakov]], _Nonhamiltonian approach to conformal quantum field theory_, Zh. Eksp. Teor. Fiz. 66 (1974) 23–42

* {#BelavinPolyakovZamolodchikov84} [[Alexander Belavin]], [[Alexander Polyakov]], and [[Alexander Zamolodchikov]], _Infinite conformal symmetry in two-dimensional quantum field theory_, Nucl. Phys. B241 (1984) 333–380


There was also a talk

* {#Kontsevich10} [[Maxim Kontsevich]], talk at _[Renormalization: algebraic, geometric and probabilistic aspects](http://math.univ-lyon1.fr/~calaque/Colloque-schedule.htm)_,  Institut Camille Jordan (Lyon) June 16 - 18, 2010

[[!redirects OPE]]
[[!redirects OPEs]]
[[!redirects operator product expansions]]