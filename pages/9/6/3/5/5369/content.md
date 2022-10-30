
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

A [[model category]] structure on the category of [[dg-categories]] that exhibits them as a presentation for [[stable (infinity,1)-categories]].

## Statement

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


> this model structure should be a presentation of the [[(∞,1)-category]] of [[stable (∞,1)-categories]] over the ring $k$.

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

Discussion of [[internal homs]] of dg-categories in terms of refined [[Fourier-Mukai transforms]] is in

* [[Bertrand Toën]], _The homotopy theory of dg-categories and derived Morita theory_, Invent. Math. 167 (2007), 615&#8211;667

Discussion of [[internal homs]] of dg-categories using (just) the structure of a [[category of fibrant objects]] is in 

* Alberto Canonaco, Paolo Stellari, _Internal Homs via extensions of dg functors_ ([arXiv:1312.5619](http://arxiv.org/abs/1312.5619))

There is also 

* David Rosoff, _Mapping spaces of $A_\infty$-algebras_ ([pdf](http://www.math.washington.edu/~rosoff/ainfs.pdf))


