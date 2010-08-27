
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
* automatic table of contents goes here
{:toc}




## Idea

$Pr(\infty,1)Cat$ is the [[(∞,1)-category]] of [[locally presentable (∞,1)-categories]] and colimit-preserving [[(∞,1)-functor]]s between them.


Recall that a [[presentable (∞,1)-category]] is a [[localization of an (∞,1)-category|localization]] of a [[(∞,1)-category of (∞,1)-presheaves]]. In particular it has all small [[colimit]]s. An [[(∞,1)-functor]] $C \times D \to E$ from the cartesian product of two presentable $(\infty,1)$-categories is _bilinear_ if it respects colimits in both variables.

It turns out that there is a _universal_ such bilinear functor

$$
  C \times D \to C \otimes D
  \,,
$$

which thereby defines a [[tensor product of presentable (∞,1)-categories]]. This defines a [[monoidal (infinity,1)-category|monoidal structure]] on presentable $(\infty,1)$-categories, which is in fact [[symmetric monoidal (infinity,1)-category|symmetric]]. 

The collection $Pr(\infvty,1)Cat$ of presentable $(\infty,1)$-cateories with colimit-preserving [[(∞,1)-functor]]s between them (i.e. with "*linear*" functors between them!), is an $(\infty,1)$-generalization of the category $Set Mod$ of ordinary categories and [[bimodule]]s or [[profunctor]]s, or [[distributor]]s between them. See [[distributor]] and in particular the discussion there about the equivalent reformulation in terms of colimit-preserving functors.

Using $Pr(\infty,1)Cat$ with its notion of "linearity" one obtains a very general notion of $\infty$-linear algebra. This is described at [[geometric ∞-function theory]].

## Definition

Write $Pr(\infty,1)Cat_1$ for the sub-$(\infty,1)$-category of the [[(∞,1)-category of (∞,1)-categories]] whose

* objects are [[presentable (∞,1)-category|presentable (∞,1)-categories]];

* morphisms are [[limit in a quasi-category|colimit]]-preserving [[(∞,1)-functor]]s.

With $C \times D \to C \otimes D$ the tensor product obtainmed as the universal colimit-preserving functor, $Pr(\infty,1)Cat_1^L$ becomes a [[symmetric monoidal (∞,1)-category]].


### Stable version

The symmetric monoidal structure on presentable $(\infty,1)$-categories restricts to one on presentable [[stable (∞,1)-category|stable (∞,1)-categories]].

The tensor unit of stable presentable $(\infty,1)$-categories is the [[stable (∞,1)-category of spectra]].


## Properties

+-- {: .un_prop}
###### Proposition

All small [[limit in a quasi-category|limits and colimits]] exists in $Pr(\infty,1)Cat$ and are preserved by the embedding $Pr(\infty,1)Cat \hookrightarrow (\infty,1)Cat$.

=--

This is [[Higher Topos Theory|HTT, prop. 5.5.3.13]] together with [[Higher Topos Theory|HTT, theorem 5.5.3.18]].



## As $\infty$-vector spaces

In some context -- such as for instance in the context of [[geometric ∞-function theory]] -- it makes good sense to think of $Pr(\infty,1)Cat$ as a model for an $(\infty,1)$-category of "$\infty$-vector spaces":

Here a small $(\infty,1)$-category $S$ is to be thought of as a _basis_ and the locally presentable $(\infty,1)$-category $C \hookrightarrow PSh_{(\infty,1)}(C)$ as the $\infty$-vector space spanned by this basis. The colimits in $C$ play the role of addition of vectors and the fact that morphisms in $Pr(\infty,1)Cat$ are colimit-presserving means that they play  the role of _linear_ maps between vector spaces.

The monoidal product $\otimes : Pr(\infty,1)Cat \times Pr(\infty,1)Cat \to Pr(\infty,1)Cat$ plays the role of the [[tensor product]] of vector spaces, with a morphism out of $C \otimes D$ being a bilinear morphism out of $C \times D$, and the fact that $Pr(\infty,1)Cat$ is closed monoidal reflects the fact that [[Vect]] is closed monoidal. 


Combined with the fact that the embedding $Pr(\infty,1)Cat \hookrightarrow (\infty,1)Cat$ preserves limits and colimits, this yields some useful statements.

For instance with $Pr(\infty,1)Cat$ regarded as $\infty Vect$, for any [[∞-group]] $G$ with [[delooping]] [[∞-groupoid]] $\mathbf{B}G$, we may think of an [[(∞,1)-functor]] $\rho : \mathbf{B}G \to Pr(\infty,1)Cat$ as a linear [[representation]] of $G$: the single object of $\mathbf{B}G$ is sent to a presentable $(\infty,1)$-category $V$ and the morphisms in $\mathbf{B}G$ then define an [[action]] of $G$ on that.

The corresponding [[action groupoid]] $V//G$ (see there for more) is then the [[limit in a quasi-category|colimit]] over the action, in $Pr(\infty,1)Cat$ 

$$
  \array{
    V//G &\to& Z
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}G &\stackrel{\rho}{\to}& Pr(\infty,1)Cat
  }
  \,.
$$


## References

The $(\infty,1)$-category $Pr(\infty,1)Cat$ is introduced in section 5.5.3 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 

The monoidal structure on $Pr(\infty,1)Cat$ is described in section 4.1 of

* [[Jacob Lurie]], _[[higher algebra|Noncommutative algebra]]_

That this is in fact a symmetric monoidal structure is discussed in section 6 of

* [[Jacob Lurie]], _[[higher algebra|Commutative algebra]]_

see proposition 6.14 and remark 6.18.

[[!redirects symmetric monoidal (infinity,1)-category of presentable (infinity,1)-categories]]


[[!redirects symmetric monoidal (∞,1)-category of presentable (∞,1)-categories]]
[[!redirects symmetric monoidal (infinity,1)-category of presentable (inf]]
[[!redirects Pr(∞,1)Cat]]

[[!redirects presentable (infinity,1)-category]]


category: categories

