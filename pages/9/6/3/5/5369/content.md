
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

The general notion [[model structure on enriched categories]] gives in particular a model structure on [[dg-categories]], called the _Dwyer-Kan model structure_, and analogous to the usual [[model structure on sSet-categories]] which models [[(infinity,1)-categories]].

There are interesting [[left Bousfield localizations]] of this model structure, called the _quasi-equiconic_ and _Morita_ model structures.  Here the [[fibrant objects]] are the [[pretriangulated dg-categories]], resp. [[idempotent complete category|idempotent complete]] [[pretriangulated dg-categories]].  In characteristic zero, the Morita model structure is known to present the [[(infinity,1)-category]] of linear [[stable (infinity,1)-categories]] ([Cohn 13](#Cohn13)).

## Statement

### With Dwyer-Kan equivalences

+-- {: .num_theorem}
###### Theorem

Let $k$ be a [[commutative ring]]. Write $dgCat_k$ for the [[category]] of [[small category|small]] [[dg-categories]] over $k$.

There is the structure of a [[cofibrantly generated model category]] on $dgCat_k$ where a dg-functor $F : A \to B$ is

* a weak equivalence if

  1. for all objects $x,y \in A$ the component $F_{x,y} : A(x,y) \to B(F(x), F(y))$ is a [[quasi-isomorphism]] of [[chain complexes]];

  1. the induced functor on [[homotopy categories]] $H^0(F)$ (obtained by taking degree 0 [[chain homology]] in each hom-object)  is an [[equivalence of categories]].

* a fibration if

  1. for all objects  $x,y \in A$ the component $F_{x,y}$ is a degreewise surjection of chain complexes;

  1. for each [[isomorphism]] $F(x) \to Z$ in $H^0(B)$ there is a lift to an isomorphism in $H^0(A)$.

=--

This is due to ([Tabuada](#Tabuada)).



+-- {: .num_remark}
###### Remark

The definition is entirely analogous to the [[model structure on sSet-categories]].   Both are special cases of the [[model structure on enriched categories]].

=--



### With Morita equivalences
  {#WithMoritaEquivalences}

There is another model category structure with more weak equivalences, the _Morita equivalences_ ([Tabuada 05](#Tabuada05)).  This is in fact the [[left Bousfield localization]] of the above model structure with respect to the Morita equivalences, i.e. functors $F: C \to D$ whose induced [[restriction of scalars]] functor $\mathbf Lf^* : \mathbf D(D) \to \mathbf D(C)$ is an [[equivalence of categories]].

The [[fibrant objects]] with respect to this model structure are the [[dg-categories]] A for which the canonical inclusion $H^0(A) \hookrightarrow \mathbf D(A)$ has its [[essential image]] stable under [[cones]], [[suspensions]], and [[direct sums]].  Hence the [[homotopy category]] with respect to this model structure is identified with the [[full subcategory]] of Ho(DGCat), the homotopy category of the Dwyer-Kan model structure, spanned by dg-categories of this form.

This model structure is a presentation of the [[(∞,1)-category]] of [[stable (∞,1)-categories]] ([Cohn 13](#Cohn13)).

The [[pretriangulated dg-category|pretriangulated envelope]] of [[Bondal]]-[[Kapranov]] is a [[fibrant replacement]] functor for the Morita model structure.  The [[DG quotient]] of [[Drinfeld]] is a model for the [[homotopy cofibre]] with respect to the Morita model structure.

### Quasi-equiconic model structure

Here the [[fibrant objects]] are the [[pretriangulated dg-categories]]. (...)


## Related concepts

* [[model structure on dg-operads]]

* [[model structure on dg-algebras over an operad]]

  * [[model structure on dg-algebras]]

  * **model structure on dg-categories**

## References
 {#References}


The model structure on dg-categories is due to

* [[Gonçalo Tabuada]], _Une structure de cat&#233;gorie de mod&#232;les de Quillen sur la cat&#233;gorie des dg-cat&#233;gories_ C. R. Acad. Sci. Paris S&#233;r. I Math. 340 (1) (2005), 15&#8211;19.
{#Tabuada}

It is reproduced as theorem 4.1 in 

* [[Bernhard Keller]], _On differential graded categories_ ([pdf](http://atlas.mat.ub.es/grgta/articles/Keller.pdf))


A summary of the various model structures on dg-categories:

* {#CisinskiTabuada11} [[Denis-Charles Cisinski]], [[Goncalo Tabuada]], Section 2 of: _Non-connective K-theory via universal invariants_, Compositio Math. **147** (2011) 1281-1320 &lbrack;[arXiv:0903.3717](http://arxiv.org/abs/0903.3717), [pdf](http://www.math.univ-toulouse.fr/~dcisinsk/Non-connective-K-theory.pdf)&rbrack;


Discussion of [[internal homs]] of dg-categories in terms of refined [[Fourier-Mukai transforms]] is in

* [[Bertrand Toën]], _The homotopy theory of dg-categories and derived Morita theory_, Invent. Math. 167 (2007), 615&#8211;667

Discussion of [[internal homs]] of dg-categories using (just) the structure of a [[category of fibrant objects]] is in 

* Alberto Canonaco, Paolo Stellari, _Internal Homs via extensions of dg functors_ ([arXiv:1312.5619](http://arxiv.org/abs/1312.5619))

The derived internal Hom in the homotopy category of DG-categories is equivalent to the dg-category of A_infty-functors.

* [[Giovanni Faonte]], _A-infinity functors and homotopy theory of DG-categories_, [arXiv](http://arxiv.org/abs/1412.1255).

A proof that the [[internal hom]] of Ho(DGCat) constructed by To&#235;n is in fact the right [[derived functor]] of the internal hom of DGCat is in

* Beatriz Rodriguez Gonzalez, _A derivability criterion based on the existence of adjunctions_, 2012, [arXiv:1202.3359](http://arxiv.org/abs/1202.3359).

There is also 

* David Rosoff, _Mapping spaces of $A_\infty$-algebras_ ([pdf](http://www.math.washington.edu/~rosoff/ainfs.pdf))

The model structure with Morita equivalences as weak equivalences is discussed in

* {#Tabuada05} [[Goncalo Tabuada]], _Invariants additifs de dg-catgories_. Internat. Math. Res. Notices 53 (2005), 33093339.

That the Morita model structure on dg-categories presents the homotopy theory of $k$-linear [[stable (infinity,1)-categories]] was shown in

* {#Cohn13} [[Lee Cohn]], _Differential Graded Categories are k-linear Stable Infinity Categories_ ([arXiv:1308.2587](http://arxiv.org/abs/1308.2587))

See also 

* Piergiorgio Panero, Boris Shoikhet, _A Quillen model structure on the category of Kontsevich-Soibelman weakly unital dg categories_ ([arXiv:1907.07970](https://arxiv.org/abs/1907.07970))


* Piergiorgio Panero, Boris Shoikhet, _A closed model structure on the category of weakly unital dg categories, II_ ([https://arxiv.org/abs/2007.12716](https://arxiv.org/abs/2007.12716))

[[!redirects model structures on dg-categories]]

[[!redirects Dwyer-Kan model structure on dg-categories]]
[[!redirects canonical model structure on dg-categories]]
[[!redirects quasi-equiconic model structure on dg-categories]]
[[!redirects Morita model structure on dg-categories]]

[[!redirects (infinity,1)-category of dg-categories]]
[[!redirects infinity-category of dg-categories]]


