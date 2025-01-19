
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

### In the real numbers

#### Epsilon-delta definition

Let $\mathbb{R}$ be the [[real numbers]]. A function $f:\mathbb{R} \to \mathbb{R}$ is **smooth** if it comes with a [[sequence]] of functions $D^{(-)}f:\mathbb{N} \to (\mathbb{R} \to \mathbb{R})$ and a sequence of functions $M^{(-)}f:\mathbb{N} \to (\mathbb{Q}_+ \to \mathbb{Q}_+)$ in the positive rational numbers, such that 

* for every real number $x \in \mathbb{R}$, $(D^{0}f)(x) = f(x)$

* for every natural number $n \in \mathbb{N}$, for every positive rational number $\epsilon \in \mathbb{Q}_+$, for every real number $h \in \mathbb{R}$ such that $0 \lt | h | \lt M^{n}f(\epsilon)$, and for every real number $x \in \mathbb{R}$, 
$$|(D^{n}f)(x + h) - (D^{n}f)(x) - h (D^{n + 1}f)(x)| \lt \epsilon |h|$$

Unwrapping the recursive definition above, a function $f:\mathbb{R} \to \mathbb{R}$ is **smooth** if it comes with a [[sequence]] of functions $D^{(-)}f:\mathbb{N} \to (\mathbb{R} \to \mathbb{R})$ and a sequence of functions $M^{(-)}f:\mathbb{N} \to (\mathbb{Q}_+ \to \mathbb{Q}_+)$ in the positive rational numbers, such that 

* for every real number $x \in \mathbb{R}$, $(D^{0}f)(x) = f(x)$

* for every natural number $n \in \mathbb{N}$, for every positive rational number $\epsilon \in \mathbb{Q}_+$, for every real number $h \in \mathbb{R}$ such that $0 \lt | h | \lt M^{n}f(\epsilon)$, and for every real number $x \in \mathbb{R}$, 
$$\left|f(x + h) - \sum_{i=0}^n \frac{h^i (D^{i}f)(x)}{i!}\right| \lt \epsilon |h^n|$$

#### Infinitesimal definition

Given a predicate $P$ on the real numbers $\mathbb{R}$, let $I$ denote the set of all elements in $\mathbb{R}$ for which $P$ holds. A [[partial function]] $f:\mathbb{R} \to \mathbb{R}$ is equivalently a function $f:I \to \mathbb{R}$ for any such predicate $P$ and set $I$. 

A function $f:I \to \mathbb{R}$ is **smooth at a subset** $S \subseteq I$ with injection $j:S \hookrightarrow \mathbb{R}$ if it has a function $\frac{d^{-} f}{d x^{-}}:\mathbb{N} \times S \to \mathbb{R}$ with $\frac{d^0 f}{d x^0}\left(a\right) = a$ for all $a \in S$, such that for all Archimedean ordered Artinian local $\mathbb{R}$-algebras $A$ with ring homomorphism $h_A:\mathbb{R} \to A$ and [[nilradical]] $D$, natural numbers $n \in \mathbb{N}$, and purely infinitesimal elements $\epsilon \in D$ such that $\epsilon^{n + 1} = 0$
$$f_A(h_A(j(a)) + \epsilon) = \sum_{i = 0}^{n} \frac{1}{i!} h_A\left(\frac{d^i f}{d x^i}\left(a\right)\right) \epsilon^i$$ 

Equivalently, let $\mathbb{R}[[\epsilon]]$ denote the ring of univariate [[formal power series]] on $\mathbb{R}$. $\mathbb{R}[[\epsilon]]$ is a [[Artinian local ring|Artinian local]] $\mathbb{R}$-algebra with homomorphism $h:\mathbb{R} \to \mathbb{R}[[\epsilon]]$. A function $f:I \to \mathbb{R}$ is **smooth at a subset** $S \subseteq I$ with injection $j:S \hookrightarrow \mathbb{R}$ if it has a function $\frac{d^{-} f}{d x^{-}}:\mathbb{N} \times S \to \mathbb{R}$ with $\frac{d^0 f}{d x^0}\left(a\right) = a$ for all $a \in S$, such that for all natural numbers $n \in \mathbb{N}$
$$f_A(h(j(a)) + \epsilon) = \sum_{i = 0}^{\infty} \frac{1}{i!} h\left(\frac{d^i f}{d x^i}\left(a\right)\right) \epsilon^i$$ 

A function $f:I \to \mathbb{R}$ is **smooth at an element** $a \in I$ if it is smooth at the [[singleton subset]] $\{a\}$, and a function $f:I \to \mathbb{R}$ is **smooth** if it is smooth at the [[improper subset]] of $I$. 

### Between Cartesian spaces

A [[function]] on (some open subset of) a [[cartesian space]] $\mathbb{R}^n$ with values in the [[real line]] $\mathbb{R}$ is **smooth**, or __infinitely differentiable__, if all its [[derivative]]s exist at all points. More generally, if $A \subseteq \mathbb{R}^n$ is any subset, a function $f: A \to \mathbb{R}$ is defined to be _smooth_ if it has a smooth extension to an open subset containing $A$. 

By [[coinduction]]: A [[function]] $f : \mathbb{R} \to \mathbb{R}$ is _smooth_ if (1) its [[derivative]] exists and (2) the derivative is itself a smooth function. 

For $A \subseteq \mathbb{R}^n$, a **smooth map** $\phi: A \to \mathbb{R}^m$ is a function such that $\pi \circ \phi$ is a smooth function for every linear functional $\pi: \mathbb{R}^m \to \mathbb{R}$. (In the case of finite-dimensional codomains as here, it suffices to take the $\pi$ to range over the $m$ coordinate projections.) 

The concept can be generalised from cartesian spaces to [[Banach spaces]] and some other infinite-dimensional spaces.  There is a [[locale]]-based analogue suitable for [[constructive mathematics]] which is not described as a function of points but as a special case of a [[continuous map]] (in the localic sense).

### Between smooth manifolds

A [[topological manifold]] whose transition functions are smooth maps is a [[smooth manifold]]. A smooth function between smooth manifolds is a function that (co-)restricts to a smooth function between subsets of Cartesian spaces, as above, with respect to any choice of [[atlases]], hence which is a $k$-fold [[differentiable function]] (see there for more details), for all $k$ The [[category]] [[Diff]] is the category whose objects are smooth manifolds and whose morphisms are smooth maps between them.

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

* [[Fabius function]]

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
