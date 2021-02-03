
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A [[function]] which is [[differentiable function]] to arbitrary order is called a _smooth function_.


### Between Cartesian spaces

A [[function]] on (some open subset of) a [[cartesian space]] $\mathbb{R}^n$ with values in the [[real line]] $\mathbb{R}$ is **smooth**, or __infinitely differentiable__, if all its [[derivative]]s exist at all points. More generally, if $A \subseteq \mathbb{R}^n$ is any subset, a function $f: A \to \mathbb{R}$ is defined to be _smooth_ if it has a smooth extension to an open subset containing $A$. 

By [[coinduction]]: A [[function]] $f : \mathbb{R} \to \mathbb{R}$ is _smooth_ if (1) its [[derivative]] exists and (2) the derivative is itself a smooth function. 

For $A \subseteq \mathbb{R}^n$, a **smooth map** $\phi: A \to \mathbb{R}^m$ is a function such that $\pi \circ \phi$ is a smooth function for every linear functional $\pi: \mathbb{R}^m \to \mathbb{R}$. (In the case of finite-dimensional codomains as here, it suffices to take the $\pi$ to range over the $m$ coordinate projections.) 

The concept can be generalised from cartesian spaces to [[Banach spaces]] and some other infinite-dimensional spaces.  There is a [[locale]]-based analogue suitable for [[constructive mathematics]] which is not described as a function of points but as a special case of a [[continuous map]] (in the localic sense).

### Between smooth manifolds

A [[topological manifold]] whose transition functions are smooth maps is a [[smooth manifold]]. A smooth function between smooth manifolds is a function that (co-)restricts to a smooth function between subsets of Cartesian spaces, as above, with respect to any choice of [[atlases]], hence which is a $k$-fold [[differentiable function]] (see there for more details), for all $k$ The [[category]] [[Diff]] is the category whose objects are smooth manifolds and whose morphisms are smooth maps betweeen them.

### Between generalized smooth spaces

There are various [[categories]] of [[generalised smooth spaces]] whose [[morphisms]] are generalized [[smooth functions]].

For details see for example at _[[smooth set]]_.


## Properties

Basic facts about smooth functions are

* the [[Hadamard lemma]]

* [[Borel's theorem]]

* the [[Tietze extension theorem]]

* the [[Steenrod-Wockel approximation theorem]]

* [[embedding of smooth manifolds into formal duals of R-algebras]]

* [[derivations of smooth functions are vector fields]]


## Examples

Every [[analytic functions]] (for instance a [[holomorphic function]]) is also a smooth function.

A crucial property of smooth functions, however, is that they contain also [[bump functions]].


## Related concepts

* [[differentiable function]]

* [[smooth function with rapidly decreasing derivatives]]

* [[smooth homotopy]], [[smooth isotopy]]

* [[nonlinear functional]], [[linear functional]]


[[!include infinitesimal and local - table]]

## References

An early account, in the context of [[Cohomotopy]], [[cobordism theory]] and the [[Pontryagin-Thom construction]]:

* {#Pontrjagin55} [[Lev Pontrjagin]], Chapter I of: _Smooth manifolds and their applications in Homotopy theory_, Trudy Mat. Inst. im Steklov, No 45, Izdat. Akad. Nauk. USSR, Moscow, 1955 (AMS Translation Series 2, Vol. 11, 1959) ([doi:10.1142/9789812772107_0001](https://www.worldscientific.com/doi/abs/10.1142/9789812772107_0001), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/pont001.pdf))



[[!redirects smooth function]]
[[!redirects smooth functions]]
[[!redirects smooth map]]
[[!redirects smooth maps]]
[[!redirects infinitely differentiable function]]
[[!redirects infinitely differentiable functions]]
[[!redirects infinitely differentiable map]]
[[!redirects infinitely differentiable maps]]
