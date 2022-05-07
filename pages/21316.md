# Eilenberg-Zilber categories

* table of contents
{: toc}

## Idea

An Eilenberg-Zilber category is a special sort of [[generalized Reedy category]] for which degeneracies behave particularly well.

## Definition

An **Eilenberg-Zilber category** (or **EZ-category**) is a small category $R$ equipped with a function $d:ob(R) \to \mathbb{N}$ such that

1. For $f:x\to y$,
   1. If $f$ is an isomorphism, then $deg(x)=deg(y)$.
   2. If $f$ is a noninvertible monomorphism, then $deg(x)\lt deg(y)$.
   3. If $f$ is a noninvertible split epimorphism, then $deg(x) \gt deg(y)$.
2. Every morphism factors as a split epimorphism followed by a monomorphism.
3. Any pair of split epimorphisms in $R$ has an [[absolute colimit|absolute]] [[pushout]].

Since a morphism is a split epimorphism if and only if its image in the [[presheaf category]] $[R^{op},Set]$ is an epimorphism, condition (2) says that the (epi, mono) [[factorization system]] of $[R^{op},Set]$ restricts to $R$ via the [[Yoneda embedding]], while condition (3) says that the representables are closed in $[R^{op},Set]$ under pushouts of pairs of epimorphisms.

## Properties

Any EZ-category is a [[generalized Reedy category]] where $R^+$ and $R^-$ are the monomorphisms and the split epimorphisms, respectively.  Moreover, $R^{op}$ is also a generalized Reedy category where the definitions of $R^+$ and $R^-$ are reversed.  However, the generalized Reedy model structures on contravariant functors (corresponding to the generalized Reedy strurcture on $R^{op}$) are generally better-behaved.

Any element of a presheaf on an EZ-category $R$ is a degeneracy of a unique nondegenerate element.

If an EZ-category is also a strict [[Reedy category]] (i.e. contains no nonidentity isomorphisms), then it is an [[elegant Reedy category]].

## References

* {#BergerMoerdijk2011} [[Clemens Berger]], [[Ieke Moerdijk]], _On an extension of the notion of Reedy category_, Mathematische Zeitschrift, 269, 2011 ([arXiv:0809.3341](https://arxiv.org/abs/0809.3341), [doi:10.1007/s00209-010-0770-x]( https://doi.org/10.1007/s00209-010-0770-x))
* {#Isaacson2010} [[Samuel Isaacson]], _Symmetric cubical sets_, Journal of Pure and Applied Algebra, 215, 2011 ([arXiv:0910.4948](https://arxiv.org/abs/0910.4948), [doi:10.1016/j.jpaa.2010.08.001](http://dx.doi.org/10.1016/j.jpaa.2010.08.001))
* {#BergnerRezk2013} [[Julia Bergner]], [[Charles Rezk]], _Reedy categories and the Θ-construction_, Mathematische Zeitschrift, 274, 2013 ([arXiv:1110.1066](https://arxiv.org/abs/1110.1066), [doi:10.1007/s00209-012-1082-0](http://dx.doi.org/10.1007/s00209-012-1082-0))
* {#Cisinski2019} [[Denis-Charles Cisinski]], _Higher Categories and homotopical algebra_, Cambridge University Press, 2019, [doi:10.1017/9781108588737](http://dx.doi.org/10.1017/9781108588737))


 

[[!redirects Eilenberg-Zilber categories]]
[[!redirects EZ-category]]
[[!redirects EZ-categories]]
[[!redirects EZ-Reedy category]]
[[!redirects EZ-Reedy categories]]

