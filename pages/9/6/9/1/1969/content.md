#Contents#
* automatic table of contents goes here
{:toc}


## Idea ##

A [[model category]] $C$ models an [[(∞,1)-category]] $\mathbf{C}$. The latter may be conceived as a [[simplicially enriched category]] with the same objects as $C$.

For $X,Y \in Obj(C)$ objects of $C$ the [[SSet]]-[[hom object]] $\mathbf{C}(X,Y)$ is the _$(\infty,1)$-categorical hom space_ between $X$ and $Y$ defined by $C$.

There are various equivalent explicit expressions for this objects. These are described and compared in the following.

+-- {: .query}
I don\'t like this term, (for reasons other than using the word 'categorical' ^_^).  Is there any hom-space that is *not* $(\infty,1)$-categorial?  It seems to me that if your hom-objects are spaces, then you\'re an $(\infty,1)$-category; and if you\'re an $(\infty,1)$-category, then your hom-objects could be any spaces.  So how about [[hom-space]]?  ---Toby

[[Urs Schreiber]]: I see your point. On the other hand probably few readers will expect behind a title "hom-space" more than a remark about the definition of a Top-enriched category. Here the point is the construction of these from 1-categorical data.

How can we say this better?

_Toby_:  Well, I also thought of 'hom-$\infty$-groupoid' and 'hom-simplicial set' (at which point the hyphen in 'hom-object' looks worse and worse), but these struck me as too specific, although they match what you\'re saying here.

=--


## Details ##

Let $C$ be a [[model category]]. Recall the [[simplicial localization|hammock localization]] procedure on $C$:

For $X,Y \in Obj(C)$ and for $n \in \mathbb{N}$ define a category $w Mor_C^n(X,Y)$ 

* whose objects are zig-zags of morphisms in $C$ of length $n$

  $$
    X = X_0 \leftarrow X_1 \to X_2 \leftarrow \cdots \to X_{n-1} \leftarrow X_n = Y
  $$
  such that each morphism going to the left, $X_{2k}\leftarrow X_{2k +1}$, is a [[weak equivalence]].

* morphisms between such objects $(X,X_i,Y) \to (X',X'_i,Y')$ are collections of weak equivalences $(X_i \to X'_i)$ for all $0 \lt i \lt n $ such that all triangles and squares commute.

Write $N(wMor_C^n(X,Y))$ for the [[nerve]] of this category, a [[simplicial set]].

Then the [[simplicial localization|hammock localization]] $L^H C$ of $C$ is the [[simplicially enriched category]] with objects those of $C$ and [[hom-object]]s given by the [[colimit]] over the length of these hammock hom-categories

$$
  L^H C(X,Y) = colim_n N(wMor_C^n(X,Y))
  \,.
$$

Suppose now that $Q : C \to C$ is a [[cofibrant replacement functor]] and $R : C \to C$ a [[fibrant replacement functor]], $\Gamma^\bullet : C \to (cC)_c$ a [[cosimplicial resolution functor]] and $\Lambda_\bullet : C \to (sC)_f$ a [[simplicial resolution functor]] in the [[model category]] $C$.


+-- {: .un_theorem }
###### Theorem (Dwyer--Kan)

There are natural weak equivalences between the following equivalent realizations of this [[SSet]] [[hom-object]]:

$$
  \array{
    Mor_C(\Gamma^\bullet X, R Y)
    &&&&
    Mor_C(Q X, \Lambda_\bullet Y)
    \\
    & \searrow^\simeq && {}^\simeq \swarrow
    \\
    &&
    diag Mor_C(\Gamma^\bullet X, \Lambda_\bullet Y)
    \\
    &&
    \uparrow^\simeq
    \\
    &&
    hocolim_{p,q \in \Delta^{op} \times \Delta^{op}}
    Mor_C(\Gamma^p X, \Lambda_q Y)
    \\
    &&\downarrow^\simeq
    \\
    &&N wMor_C^3(X,Y)
    \\
    &&\downarrow^\simeq
    \\
    &&Mor_{L^H C}(X,Y)
  }
  \,.
$$

=--


## References ##

A useful quick review is page 14, 15 of

* Clark Barwick, _On (enriched) left Bousfield localization of model categories_ ([arXiv](http://arxiv.org/abs/0708.2067))

The definition in terms of simplicial and fibrant/cofibrant resolutions is described in detail in sections 16, 17 of

* Hirschhorn, _Model categories and their localization_ .


[[!redirects (∞,1)-categorical hom-space]]
[[!redirects (infinity,1)-categorical hom space]]
[[!redirects (∞,1)-categorical hom space]]
[[!redirects (infinity,1)-categorial hom-space]]
[[!redirects (∞,1)-categorial hom-space]]
[[!redirects (infinity,1)-categorial hom space]]
[[!redirects (∞,1)-categorial hom space]]