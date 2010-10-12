#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **convex space** (also called **barycentric algebra** and other terms, invented independently many times) is a set equipped with a notion of taking weighted averages, or convex-linear combinations, of its elements.  Do not confuse this with an (abstract) _[[convex set]]_ , which a special kind of convex space, also defined below.

Convex spaces may be important in the foundations of [[probability theory]].  The [[category]] of convex spaces is [[semicartesian monoidal category|semicartesian monoidal]] but not [[cartesian monoidal category|cartesian monoidal]].

The [[monad]] assigning to any set the free convex space on that set is a [[finitary monad|finitary]] [[commutative monad]].  We can thus follow Durov in thinking of it as a [[generalized ring]].  This allows us to think of convex spaces as 'modules' of a generalized ring, very much as [[vector spaces]] are modules of a field.  This is also true of the relatives of convex spaces: [[affine space|affine spaces]] and [[conical space|conical spaces]].  For example, an **affine space** may be defined just as a convex space is defined below, but dropping the condition $0 \leq p \leq 1$.

## Definition

A __convex space__ is a [[set]] $X$ equipped with:

*  for each [[real number]] $p$ such that $0 \leq p \leq 1$, an operation $c_p: X \times X \to X$,

such that the following identities always hold:

*  $c_0(a,b) = b$,
*  $c_1(a,b) = a$ (this one is redundant),
*  $c_p(a,a) = a$,
*  $c_p(a,b) = c_{1-p}(b,a)$,
*  $c_p(c_q(a,b),c) = c_{p q}(a,c_r(b,c))$ for $(1 - p q)r = (1 - q)p$.

This defines convex spaces as a [[variety of algebras]], with one binary operation for each $p$.

The intended interpretation is that $c_p(a,b)$ is the average of $a$ and $b$, with $a$ given the weight $p$ and $b$ given the weight $1 - p$; this is called the __$p$-weighted average__ of $a$ and $b$.  It is also possible to give an '[[bias|unbiased]]' definition, in which the most general operation is an $n$-ary operation parametrised by a list $(p_1,\ldots,p_n)$ such that $0 \leq p_i \leq 1$ for each $i$ and $\sum_{i = 1}^n p_i = 1$.  Such an operation is called a __convex-linear combination__.

A [[homomorphism]] of convex spaces may be called a __convex-linear map__ or an __affine linear map__ (since an [[affine space]] is a convex space with extra properties, as in the examples below).  It should probably *not* be called a 'convex map', which (between affine spaces) is something more general.


## Examples

Any real [[vector space]] is a convex space, with $c_p(a,b) = p a + (1 - p) b$.  In the unbiased version, any convex-linear combination is a linear combination.  Note that a convex-linear map between vector spaces may not be a linear map, since it may not preserve the identity; thus, a vector space is a convex space with [[extra structure]].

More generally, any real [[affine space]] is a convex space; since $p + (1 - p) = 1$, the expression for $c_p$ in a vector space is valid in an affine space.  In the unbiased version, any convex-linear combination is an affine linear combination.  Now any convex-linear map between affine spaces is an affine linear map (and conversely); an affine space is a convex space with [[extra properties]].

Still more generally, any [[convex subset]] (that is, one containing the entire line segment between two given points) of a real [[affine space]] is a convex space (again with extra properties, which are described algebraically below).

The [[Boolean field]] $\{0,1\}$ is a convex space with $c_p(a,b) = a \vee b = a + b - a b$ whenever $0 \lt p \lt 1$ (with $c_0(a,b) = b$ and $c_1(a,b) = a$ as always); this cannot be realised as a subset of a vector space.  This can be generalised to any (possibly unbounded) [[semilattice]].  (It would be nice to find an example like this that can be defined constructively; this one relies on [[excluded middle]].)


## Abstract convex sets

There is a nice abstract converse to the example of a [[convex subset]] of an affine space.  A convex space is __cancellative__ if $a = b$ whenever $c_p(a,c) = c_p(b,c)$ for some $c$ and $p \gt 0$.  We may call a cancellative convex space an __abstract convex set__.  The justification for this terminology is this
+-- {: .un_theorem}
###### Theorem (Thm 2 in the paper by Stone)

A convex space is cancellative if and only if it is isomorphic (as a convex space) to a convex subset of some real affine space.
=--

Compare this with the theorem that a [[monoid]] is cancellative if and only if it is isomorphic to a submonoid of some [[group]].

+--{: .query}
[[Mike Shulman]]: What are some examples of non-cancellative convex spaces?

_Toby_:  The last example in the list above: $\{0,1\}$ with $c_p(a,b) = a \vee b$ whenever $0 \lt p \lt 1$; this generalises to any nontrivial semilattice.  I don\'t know any better examples.

[[John Baez]]: Could someone provide a proof or reference to the above theorem?

_Toby_:  _HAF_ cites Romanowska & Smith (added to the references below, but I haven\'t read it).

[[Tobias Fritz]]: reference added.
=--


## References

Convex spaces have been rediscovered many times under many different names.  References tend to define $c_p$ only for $0 \lt p \lt 1$, but it seems obvious that it\'s best to include the edge cases as well.  Classically, it makes no difference, but the definition above is probably better in [[constructive mathematics]].

*  _[[Handbook of Analysis and its Foundations]]_, Section 12.7 (short and to the point).

*  Romanowska, Smith, Or&#322;owska; Abstract barycentric algebras; [pdf](http://staff.science.uva.nl/~gfontain/tacl09-abstracts/tacl2009_submission_48.pdf).  This generalises from $[0,1]$ to an arbitrary $L \Pi$-algebra ($L$ for '&#321;ukasiewicz', $\Pi$ for 'product', so think of $[0,1]$ as a space of fuzzy truth values).

*  Romanowska & Smith (1985); Modal Theory: An Algebraic Approach to Order, Geometry, and Convexity; Res. Exp. Math. 9; Heldermann-Verlag, Berlin, 1985.

* Marshall Harvey Stone, Postulates for the barycentric calculus. Ann. Mat. Pura. Appl. (4), 29:25&#8211;30, 1949.

* Tobias Fritz, Convex spaces I: definition and examples. 
[[arXiv](http://arxiv.org/abs/0903.5522)]

* Bart Jacobs, Duality for convexity. [[arXiv](http://arxiv.org/abs/0911.3834)]

* Joe Flood, Semiconvex geometry, _J. Austral. Math. Soc. Ser. A_ **30** (1980/81), 496-&#8211;510. 

* T. Swirszcz, _Monadic functors and categories of convex sets_ , Preprint No. **70**, _Proc. Inst. Math. Pol. Acad. Sci._, Warsaw.

* T. Swirszcz, Monadic functors and convexity, _Bull. Acad. Polon. Sci. Ser. Sci. Math. Astronom. Phys._ **22** (1974), 39--42. 

* Stanley P. Gudder, Convexity and mixtures, _SIAM Review_ **19** (1977), 221--240.

* Stanley P. Gudder, A general theory of convexity, 
_Milan Journal of Mathematics_, **49** (1979), 89--96.

Many other references, and a discussion of how convex spaces have been repeatedly rediscovered, can be found at the $n$-Category Caf&#233; post [Convex Spaces](http://golem.ph.utexas.edu/category/2009/04/convex_spaces.html).


[[!redirects barycentric algebra]]
[[!redirects convex combination]]
[[!redirects convex linear combination]]
[[!redirects convex-linear combination]]
[[!redirects convex-linear map]]
[[!redirects convex linear map]]
[[!redirects convex-linear function]]
[[!redirects convex linear function]]