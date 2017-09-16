

#Idea#

Recall that a [[presentable (infinity,1)-category]] in particular has all small colimits. An [[(infinity,1)-functor]] $C \times D \to E$ from the cartesian product of two presentable $(\infty,1)$-categories is _bilinear_ if it respects colimits in both variables.

It turns out that there is a _universal_ such bilinear functor

$$
  C \times D \to C \otimes D
  \,,
$$

which thereby defines a [[tensor product]] of presentable $(\infty,1)$-categories. This defines a [[monoidal (infinity,1)-category|monoidal structure]] on presentable $(\infty,1)$-categories, which is in fact [[symmetric monoidal (infinity,1)-category|symmetric]]. 

#Definition#

Write $Pr(\infty,1)Cat_1^L$ for the sub-$(\infty,1)$-category of the [[(infinity,1)-category of (infinity,1)-categories]] whose

* objects are [[presentable (infinity,1)-category|presentable (infinity,1)-categories]];

* morphisms are colimit preserving [[(infinity,1)-functor]]s.

With $C \times D \to C \otimes D$ the tensor product obtainmed as the universal colimit preserving functor, $Pr(\infty,1)Cat_1^L$ becomes a [[symmetric monoidal (infinity,1)-category]].


#Stable version#

The symmetric monoidal structure on presentable $(\infty,1)$-categories restricts to one on presentable [[stable (infinity,1)-category|stable (infinity,1)-categories]].

The tensor unit of stable presentable $(\infty,1)$-categories is the [[stable (infinity,1)-category of spectra]].


#References#

The monoidal structure on $Pr(\infty,1)Cat_1^L$ is described in section 4.1 of

* [[Jacob Lurie]], [[higher algebra|Noncommutative algebra]].

That this is in fact a symmetric monoidal structure is discussed in section 6 of

* [[Jacob Lurie]], [[higher algebra|Commutative algebra]].

see proposition 6.14 and remark 6.18.
