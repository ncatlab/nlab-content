


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A **convex space** (also called **barycentric algebra** and other terms, invented independently many times) is a [[set]] [[extra structure|equipped]] with a notion of taking weighted averages, or convex-[[linear combinations]], of its elements.  Do not confuse this with an (abstract) _[[convex set]]_, which a special kind of convex space, also defined below.

The [[category]] of convex spaces is an algebraic theory, being the affine part of the theory of $K$-(semi)modules with only the idempotent operations.  This definition is used by [Meng (1989)](#Meng), and many basic properties of the category are detailed therein.  The category is complete, cocomplete, symmetric monoidal closed under the (usual) tensor product construction, and has a cogenerator [B&ouml;rger and Kemper (1994)](#Borger).   The subcategory consisting of the single object, the unit interval, is dense (left-adequate) in the category.  This follows from Isbell's theorem on left adequate subcategories for algebraic theories, using the fact that the free convex space on 2 elements is the unit interval. 

Axiomatically, a convex space can be characterized as a [[set]] $X$ equipped with a family of [[functions]] $c_p : X \times X \to X$ satisfying some natural [[axioms]] (described below). 

For examples all [[nonunital ring|nonunital]] [[commutative rings]] are convex spaces, with the map $c_p(x,y) = x + p(y-x)$. 


The [[monad]] assigning to any set the free convex space on that set is a [[finitary monad|finitary]] [[commutative monad]].  We can thus follow Durov in thinking of it as a [[generalized ring]].  This allows us to think of convex spaces as 'modules' of a generalized ring, very much as [[vector spaces]] are modules of a field.  This is also true of the relatives of convex spaces: [[affine space|affine spaces]] and [[conical space|conical spaces]].  For example, all **affine spaces** are convex spaces as defined below.

Of particular importance are convex spaces parametrized by the interval $P = [0,1]$ or the Boolean algebra $P = \{0,1\}$. These two algebras are dual, in a certain sense described by [Jacobs (2009)](#Jacobs). This duality is functorial, and therefore is present for convex spaces for general $P$. This leads to the notion of a [[dual convex space]].

## Definition

A __convex space__ is a [[set]] $X$ equipped with:

* a multiplicatively closed [[subset]] $Q$ of a [[semiring|(semi)]][[ring]] $P$, so that for each element $p\in Q$ there exists an element $q\in Q$ such that $p+q=1$, and

* an operation $c_p: X \times X \to X$ defined for all $p\in Q$,

such that the following identities always hold:

*  $c_0(x,y) = x$,
*  $c_p(x,x) = x$ for all $p \in P$,
*  $c_p(x,y) = c_{1-p}(y,x)$ for all $p \in P$ (in semiring case replace $1-p$ by $q$ and require that $p+q = 1$),
* $c_p(x, c_q(y,z)) = c_{p q}(c_r(x,y),z)$ for all $p,q,r \in P$ satisfying $p(1 - q) = (1 - p q)r$.

As a consequence of the first and third axioms, $c_1(x,y) = c_0(y,x) = y$.

This defines convex spaces as a [[variety of algebras]], with one binary operation for each $p$. 

The intended interpretation is that $c_p(x,y) = x + p(y-x) = (1-p)x + p y$. i.e., $c_p(x,y)$ is the $p$-weighted average of $x$ and $y$, where $x$ gets weight $1-p$ and $y$ gets weight $p$. By thinking of $p$ as a continuous parameter, this interpretation has the advantage of "starting" at $x$, then moving toward $y$ at "rate" $p$.

This interpretation is '[[bias|biased]]', in the sense that the centered choice $p=0$ favors $x$. It is also possible to give an '[[bias|unbiased]]' definition, which characterizes to convex-linear combinations of many points. This is an $n$-ary operation parametrised by a list $p := (p_1,\ldots,p_n)$ satisfying $\sum_{i = 1}^n p_i = 1$. If $x := (x^1,\ldots, x^n)$, then $c_p(x) := \sum_i p_i x^i$.

A [[homomorphism]] of convex spaces may be called a __convex-linear map__ or an __affine linear map__ (since an [[affine space]] is a convex space with extra properties, as in the examples below).  It should probably *not* be called a 'convex map', which (between affine spaces) is something more general.


## Examples

Any real [[vector space]] is a convex space, with $c_p(x,y) = x + p(y-x)$.  In the unbiased version, any convex-linear combination is a [[linear combination]].  Note that a convex-linear map between vector spaces may not be a linear map, since it may not preserve the identity; thus, a vector space is a convex space with [[extra structure]].

More generally, any real [[affine space]] is a convex space; since $p + (1 - p) = 1$, the expression for $c_p$ in a vector space is valid in an affine space.  In the unbiased version, any convex-linear combination is an [[affine linear combination]].  Now any convex-linear map between affine spaces is an affine linear map (and conversely); an affine space is a convex space with [[extra properties]].

Still more generally, any [[convex subset]] (that is, one containing the entire line segment between two given points) of a real [[affine space]] is a convex space (again with extra properties, which are described algebraically below).

The [[Boolean field]] $\{0,1\}$ is a convex space with $c_p(x,y) = x \vee y = x + y - x y$ whenever $0 \lt p \lt 1$ (with $c_0(x,y) = x$ and $c_1(x,y) = y$ as always); this cannot be realised as a subset of a vector space.  This can be generalised to any (possibly unbounded) [[semilattice]].  (It would be nice to find an example like this that can be defined constructively; this one relies on [[excluded middle]].)


## Abstract convex sets

There is a nice abstract converse to the example of a [[convex subset]] of an affine space.  A convex space is __cancellative__ if $y = z$ whenever $c_p(x,y) = c_p(x,z)$ for some $c$ and $p \ne 0$.  We may call a cancellative convex space an __abstract convex set__.  The justification for this terminology is this

+-- {: .un_theorem}
**Theorem** (Thm. 2 in the paper by Stone)

A convex space is cancellative if and only if it is isomorphic (as a convex space) to a convex subset of some real affine space.
=--

Compare this with the theorem that a [[monoid]] is [[cancellative monoid|cancellative]] if and only if it is isomorphic to a submonoid of some [[group]].

Of course, most of the examples given above are cancellative, being manifestly given as convex subsets of real affine space.  However, the last example --- a semilattice with $c_p(x,y) = x \vee y$ whenever $0 \lt p \lt 1$ --- is non-cancellative.

## Related concepts

* [[convex function]]
* [[distribution monad]]
* [[monads of probability, measures, and valuations]]
* [[vector space]], [[affine space]], [[conical space]]

## References

Convex spaces have been rediscovered many times under many different names.  References tend to define $c_p$ only for $0 \lt p \lt 1$, but it seems obvious that it\'s best to include the edge cases as well.  Classically, it makes no difference, but the definition above is probably better in [[constructive mathematics]].

*  _[[Handbook of Analysis and its Foundations]]_, Section 12.7 (short and to the point).

* {#Borger} B&ouml;rger & Kemper, Cogenerators for convex spaces, Applied Categorical Structures, Vol. 2 (1994), 1-11.
 
*  Romanowska, Smith, Or&#322;owska; Abstract barycentric algebras; [pdf](http://staff.science.uva.nl/~gfontain/tacl09-abstracts/tacl2009_submission_48.pdf).  This generalises from $[0,1]$ to an arbitrary $L \Pi$-algebra ($L$ for '&#321;ukasiewicz', $\Pi$ for 'product', so think of $[0,1]$ as a space of fuzzy truth values).

*  Romanowska & Smith (1985); Modal Theory: An Algebraic Approach to Order, Geometry, and Convexity; Res. Exp. Math. 9; Heldermann-Verlag, Berlin, 1985.

* Marshall Harvey Stone, _Postulates for the barycentric calculus_, Ann. Mat. Pura. Appl. (4), 29:25&#8211;30, 1949.

* [[Tobias Fritz]], Convex spaces I: definition and examples. 
[arXiv/0903.5522](http://arxiv.org/abs/0903.5522)

* [[John Baez]], [[Tobias Fritz]], [[Tom Leinster]], [[johnbaez:Convex spaces and an operadic approach to entropy]], $n$Lab draft

* {#Jacobs} [[Bart Jacobs]], _Duality for convexity_ [arXiv/0911.3834](http://arxiv.org/abs/0911.3834)

* J.R. Isbell, Adequate subcategories, Illinois Journal of Math, 4, 541-552  (1960).

* Shiri Artstein-Avidan, Vitali Milman, _The concept of duality in convex analysis, and the characterization of the Legendre transform_, Annals of Math. __169__, n.2, 661-674 (2009) 

* Joe Flood, _Semiconvex geometry_, J. Austral. Math. Soc. Ser. A **30** (1980/81), 496-&#8211;510. 

* T. Swirszcz, _Monadic functors and categories of convex sets_ , Preprint No. **70**, _Proc. Inst. Math. Pol. Acad. Sci._, Warsaw; _Monadic functors and convexity_, _Bull. Acad. Polon. Sci. Ser. Sci. Math. Astronom. Phys._ **22** (1974), 39--42. 

* Stanley P. Gudder, _Convexity and mixtures_, SIAM Review **19** (1977), 221--240; _A general theory of convexity_, Milan Journal of Mathematics, **49** (1979), 89--96.

* {#Meng} Xiao-qing Meng, _Categories of convex sets and of metric spaces with applications to stochastic programming and related areas_, PhD thesis ([[Meng.djvu|djvu:file]]) 

Many other references, and a discussion of how convex spaces have been repeatedly rediscovered, can be found at the $n$-Category Caf&#233; post [Convex Spaces](http://golem.ph.utexas.edu/category/2009/04/convex_spaces.html).


[[!redirects convex space]]
[[!redirects convex spaces]]
[[!redirects barycentric algebra]]
[[!redirects barycentric algebras]]

[[!redirects convex combination]]
[[!redirects convex combinations]]
[[!redirects convex linear combination]]
[[!redirects convex linear combinations]]
[[!redirects convex-linear combination]]
[[!redirects convex-linear combinations]]

[[!redirects convex linear function]]
[[!redirects convex linear functions]]
[[!redirects convex-linear function]]
[[!redirects convex-linear functions]]
[[!redirects convex linear map]]
[[!redirects convex linear maps]]
[[!redirects convex-linear map]]
[[!redirects convex-linear maps]]