# The idea

In [[category theory]], a concept is (half-jokingly) said to be _evil_ if it involves equations between [[object|objects]].  More precisely:

* A property of categories is _non-evil_ if it when it holds for a [[category]] $C$, it also holds for any category $C'$ that is [[equivalence|equivalent]] to $C$.

* A property of functors is _non-evil_ if when holds for a [[functor]] $F$, it also holds for any functor $F'$ that is [[natural isomorphism|naturally isomorphic]] to $F$.

By rigorously avoiding equations between objects, we can ensure that the properties we define are non-evil.  (This should be made more precise, to become a theorem.)

The ideas here generalize in many directions.  For example not only properties, but also constructions involving categories and functors, can be evil or non-evil.  The idea also generalizes to $n$-categories and to objects, morphisms etc. [[internalization|internal]] to $n$-categories.

# General definition

If $X$ is an $\infty$-[[infinity-groupoid|groupoid]], then a property $P$ of objects of $X$ is __non-evil__ if, whenever $P(a)$ holds for an object $a$ of $X$ and $b$ is equivalent (as an object of $X$) to $a$, then $P(b)$ holds. Alternatively, an operation $f$ from objects of $X$ to objects of (another $\infty$-groupoid) $Y$ is __non-evil__ if, whenever $a$ and $b$ are equivalent objects of $X$, $f(a)$ and $f(b)$ are equivalent (as objects of $Y$).

(Note that everything is an object of some $\infty$-groupoid. For example, a $2$-morphism in some random $5$-category is an object of a hom-$3$-category, which has an underlying $3$-groupoid, which is a special kind of $\infty$-groupoid. For some purposes, this $2$-morphism may instead need to be seen as an object in a $2$-arrow $5$-category, which has an underlying $\infty$-groupoid as well; exactly which $\infty$-groupoid is relevant depends on the [[context]]. Also note that we really do need $\infty$-groupoids here, rather than $\infty$-categories, since dualities are not evil.)

The operation-version of evil gives the property-version if you think of a property as an operation taking values in the $\infty$-groupoid (in fact a $0$-groupoid, or [[set]]) of [[(-1)-category|truth values]]. (The property-version also gives the operation-version, although that is a little more involved.) An operation will be non-evil if it is given (as the object-operation) by a [[functor]] ('$\infty$-functor', if you prefer). A property is non-evil precisely iff it\'s a functor to the $\infty$-groupoid of truth values.

This definition should be the conclusion of a theorem that using certain language (including avoiding equations between objects of a category) makes it impossible to say anything evil. [[Michael Makkai]] works on such a language, [[FOLDS]] ('first-order logic with dependent sorts').  To learn more, see his paper _[First Order Logic with Dependent Sorts, with Applications to Category Theory](http://www.math.mcgill.ca/makkai/)_.

#Discussion

There's been a lot of discussion of this on the $n$-Category Caf&#233; --- someone find it and cite it!