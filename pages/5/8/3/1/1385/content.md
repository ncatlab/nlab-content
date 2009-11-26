#Contents
* automatic table of contents goes here
{:toc}


## Idea

Recall that a [[presentable (∞,1)-category]] is a [[localization of an (∞,1)-category|localization]] of a [[(∞,1)-category of (∞,1)-presheaves]]. In particular it has all small [[colimit]]s. An [[(∞,1)-functor]] $C \times D \to E$ from the cartesian product of two presentable $(\infty,1)$-categories is _bilinear_ if it respects colimits in both variables.

It turns out that there is a _universal_ such bilinear functor

$$
  C \times D \to C \otimes D
  \,,
$$

which thereby defines a [[tensor product of presentable (∞,1)-categories]]. This defines a [[monoidal (infinity,1)-category|monoidal structure]] on presentable $(\infty,1)$-categories, which is in fact [[symmetric monoidal (infinity,1)-category|symmetric]]. 

The collection of presentable $(\infty,1)$-cateories with colimit-preserving [[(∞,1)-functor]]s between them (i.e. with "*linear*" functors between them!), called

$$
  Pr^L
  \,,
$$

is an $(\infty,1)$-generalization of the category $Set Mod$ of ordinary categories and [[bimodule]]s or [[profunctor]]s, or [[distributor]]s between them. See [[distributor]] and in particular the discussion there about the equivalent reformulation in terms of colimit-preserving functors.

Using $Pr^L$ with its notion of "linearity" one obtains a very general notion of $\infty$-linear algebra. This is described at [[geometric ∞-function theory]].

## Definition

Write $Pr(\infty,1)Cat_1^L$ for the sub-$(\infty,1)$-category of the [[(∞,1)-category of (∞,1)-categories]] whose

* objects are [[presentable (∞,1)-category|presentable (∞,1)-categories]];

* morphisms are colimit-preserving [[(∞,1)-functor]]s.

With $C \times D \to C \otimes D$ the tensor product obtainmed as the universal colimit-preserving functor, $Pr(\infty,1)Cat_1^L$ becomes a [[symmetric monoidal (∞,1)-category]].


## Stable version

The symmetric monoidal structure on presentable $(\infty,1)$-categories restricts to one on presentable [[stable (∞,1)-category|stable (∞,1)-categories]].

The tensor unit of stable presentable $(\infty,1)$-categories is the [[stable (∞,1)-category of spectra]].


##References

The monoidal structure on $Pr(\infty,1)Cat_1^L$ is described in section 4.1 of

* [[Jacob Lurie]], [[higher algebra|Noncommutative algebra]].

That this is in fact a symmetric monoidal structure is discussed in section 6 of

* [[Jacob Lurie]], [[higher algebra|Commutative algebra]].

see proposition 6.14 and remark 6.18.


[[!redirects symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]]
[[!redirects symmetric monoidal (infinity,1)-category of presentable (inf]]