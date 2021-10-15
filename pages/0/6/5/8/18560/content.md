
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of content
{:toc}

## Idea

The concept of _$(\infty, 1)$-profunctor_ is the [[categorification]] of that of[[profunctors]] from [[category theory]] to [[(∞,1)-category theory]].

## Definition ##

If $C$ and $D$ are [[(∞,1)-categories]], then a **profunctor** from $C$ to $D$ is a [[(∞,1)-functor]] of the form

$$
  F \colon D^{op}\times C \to \infty Grpd
  \,.
$$

Such a  profunctor is usually written as $F \,\colon\,  C &#8696; D$. Composition of (∞,1)-profunctors in [[(∞,1)Prof]] is by the "tensor product of (∞,1)-functors" [[homotopy coend]] construction: if $H\colon A &#8696;  B$ and $K\colon B &#8696;  C$, their composite is given as a functor $C^{op}\times A \to \infty Grpd$ by
$$(c,a)\mapsto \int^{b\in B} H(b,a)\times K(c,b).$$

Every [[(∞,1)-functor]] $f\colon C\to D$ induces two (∞,1)-profunctors $D(1,f)\colon C &#8696; D$ and $D(f,1)\colon D &#8696; C$, defined by $D(1,f)(d,c) = D(d,f(c))$ and $D(f,1)(c,d) = D(f(c),d)$. (Here $D(-,-)$ denotes the [[hom functor]] of $D$ and $1$ denotes the identity (∞,1)-functor on the respective category.) 

Since a profunctor is also known as a (bi)module or a distributor or a correspondence, we should expect other names to be used for $(\infty, 1)$-profunctor. In [[Higher Topos Theory]] (Definition 2.3.1.3), Lurie speaks of a **correspondence**.

## Properties 

### Relation to presentable $\infty$-categories
 {#RelationToPresentableInfinityCategories}

In analogy to the situation for [[profunctors]] between [[1-categories]] (see [there](profunctor#FuncsOnPresheaves)), $\infty$-profunctors 

$$
  \mathcal{C} &#8696; \mathcal{D}
$$ 

are equivalently plain but [[(infinity,1)-colimit|$\infty$-colimit]]-[[preserved limit|preserving]] [[(infinity,1)-functors|$\infty$-functors]] 

$$
  PSh_\infty(\mathcal{C})
  \xrightarrow{\;}
  PSh_\infty(\mathcal{D})
$$

between the corresponding [[(infinity,1)-categories of (infinity,1)-presheaves|$\infty$-categories of $\infty$-presheaves]].

In this way [[small (infinity,1)-categories|small $\infty$-categories]] with $\infty$-profunctors between them is a [[full sub-(infinity,1)-category|full sub-$\infty$-category]] of of the $\infty$-category [[Pr(∞,1)Cat]] that of [[presentable (infinity,1)-categories|presentable $\infty$-categories]] with [[cocontinuous functor|cocontinuous]] [[(infinity,1)-functor|$\infty$-functors]] between them.


## Related pages

* [cograph of an (∞,1)-profunctor](cograph+of+a+profunctor#in_category_theory_2)

* [[(∞,1)Prof]]

## References

* [[Emily Riehl]], [[Dominic Verity]], _Kan extensions and the calculus of modules for ∞-categories_, ([arXiv:1507.01460](https://arxiv.org/abs/1507.01460))

* [[Rune Haugseng]], _Bimodules and natural transformations for enriched ∞-categories_, ([arXiv:1506.07341](https://arxiv.org/abs/1506.07341))

[[!redirects (infinity,1)-profunctors]]

[[!redirects (∞,1)-profunctor]]
[[!redirects (∞,1)-profunctors]]

[[!redirects (infinity, 1)-profunctor]]
[[!redirects (infinity, 1)-profunctor]]
[[!redirects (\infty, 1)-profunctor]]

[[!redirects infinity1-profunctor]]

