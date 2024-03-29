
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The category of [[dg-modules]] over a [[dg-algebra]], or more generally a [[dg-category]], admits [[dg-model structures]] which present the [[derived dg-category]].

In the case of [[dg-algebras]] in an [[abelian category]] $\mathcal{A}$, [[dg-modules]] are the same as [[module over an algebra over an operad|modules]] over [[algebra over an operad|algebras]] over the [[associative operad]] in $Ch(\mathcal{A})$. These admit model structures as described in [[model structure on modules over an algebra over an operad]], [[transferred model structure|transferred]] from the [[model structures on chain complexes]] in $\mathcal{A}$.

More generally there are [[model structures]] on [[dg-modules]] over a [[dg-category]], analogous to [[model structures on simplicial presheaves]].

## Definitions
 {#Definitions}

+-- {: .num_theorem #ProjectiveModelStructure}
###### Theorem
**(projective model structure)**

There is a [[cofibrantly generated model structure]] on the category of [[dg-modules]], called the **projective model structure**, where 

1. the [[weak equivalences]] are object-wise [[quasi-isomorphisms]] of [[chain complexes]], 

1. the [[fibrations]] are object-wise [[epimorphisms]]. 

Moreover, this is a [[dg-model structure]].

=--

+-- {: .num_theorem #InjectveModelStructure}
###### Theorem
**(injective model structure)

There is a [[model structure]] on the category of [[dg-modules]], called the **injective model structure**, where 

1. the [[weak equivalences]] are object-wise [[quasi-isomorphisms]] of [[chain complexes]], 

1. and the [[cofibrations]] are object-wise [[monomorphisms]].

=--

See ([To&#235;n 04](#Toen), section 3) and ([Keller 06](#Keller06), theorem 3.2). 

These model structures present the [[derived dg-category]].


## Related concepts

* [[model structure on chain complexes]]

* [[module structure on modules in a monoidal model category]]

* [[model structure on dg-algebras]]

* [[model structure on dg-comodules]]

## References

Section 3 of

* {#Toen2004} [[Bertrand Toën]], _The homotopy theory of dg-categories and derived Morita theory_, [arXiv:math/0408337](http://arxiv.org/abs/math/0408337).

Paragraph 3.2 of

* {#Keller06} [[Bernhard Keller]], _On differential graded categories_, [arXiv:math/0601185](http://arxiv.org/abs/math/0601185).

### For dg-algebras

For the case of [[dg-algebras]], see the references below.

A general account is around section 11.2.5 of 

* [[Benoit Fresse]], _Modules over operads and functors_ Springer Lecture Notes in Mathematics, (2009) ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.159.5833&rep=rep1&type=pdf))
{#Fresse}

and in section 3 of

* {#Hinich}[[Vladimir Hinich]],  _Homological algebra of homotopy algebras_ Communications in algebra, 25(10). 3291-3323 (1997)([arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), _Erratum_ ([arXiv:math/0309453](http://arxiv.org/abs/math/0309453)))


The [[homotopy category]] and [[triangulated category]] of dg-modules is discussed for instance also in

* {#Bernstein} Joseph Bernstein, _DG-modules and equivariant cohomology_ ([pdf](http://www.math.tau.ac.il/~bernstei/Publication_list/publication_texts/luntz_ESF/4-dg-modules-and-equivariant-cohomology.pdf)).


See also

* {#BarthelMayRiehl14} [[Tobias Barthel]], [[Peter May]], [[Emily Riehl]], _Six model structures for DG-modules over DGAs: model category theory in homological action_, New York J. Math. 20 (2014) 1077&#8211;1159 ([pdf](http://www.math.harvard.edu/~eriehl/six.pdf))

Discussion as a model for [[rational parameterized stable homotopy theory]] is due to

* [[Vincent Braunack-Mayer]], _[[schreiber:thesis Braunack-Mayer|Rational parameterized stable homotopy theory]]_, Zurich 2018

[[!redirects model structures on dg-modules]]

[[!redirects dg-model structure on dg-modules]]
[[!redirects dg-model structures on dg-modules]]

[[!redirects category of dg-modules]]
[[!redirects categories of dg-modules]]