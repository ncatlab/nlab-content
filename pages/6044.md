
# Cross products
* table of contents
{: toc}

## Idea

In general, the term 'cross product' is used for any operation denoted by the symbol '$\times$', such as [[cartesian product]], [[direct product]], [[Tychonoff product]], or (subsuming all of these) [[product|product in a category]].

However, there is another completely different context, used in the elementary analysis of [[vector spaces]], and that is what we discuss here.  Originally isolated from the multiplication operation in [[quaternions]] as a binary operation on $\mathbb{R}^3 \simeq Im(\mathbb{H})$, the cross product now has generalisations to other arities, other dimensions, and other ground fields.


## Definitions

### Classical

The **classical cross product** on the [[Cartesian space]] $\mathbb{R}^3$ is the [[bilinear function]]

$$
  (-) \times (-)\colon \mathbb{R}^3 \times \mathbb{R}^3 \to \mathbb{R}^3
$$

given by

$$ (a,b,c) \times (d,e,f) = (b e - c f, c d - a f, a e - b d) .$$

This operation is invariant under [[orthogonal group|orthogonal transformations]] and there is nothing special here about the [[real numbers]], so given any $3$-dimensional [[orientation|oriented]] [[inner product space]] $V$ over any [[field]], we have a bilinear cross product

$$
  (-) \times (-)\colon V \times V \to V
$$

given, upon choosing any oriented orthonormal basis for $V$, by the formula above.  We can even do this over any [[free module]] of rank $3$ over any [[commutative ring]] (or arguably a non-commutative [[ring]], but not a [[rig]]) equipped (as may always be done) with an inner product that admits an orthonormal basis.


### Binary {#binary}

We have already, trivially, generalized the cross product to other ground fields.  One way to generalise it to other dimensions is to identify characteristic features as a bilinear operation and see what operations in other dimensions have these.

In this vein, a **binary cross product** on any [[inner product space]] $V$ is a [[bilinear function]]

$$
  (-) \times (-)\colon V \times V \to V
$$

such that for all $x, y\in V$ we have

1. Alternation: $x \times x = 0$.

2. Orthgonality: $x \times y$ is orthogonal to both $x$ and $y$; that is, $x \cdot (x \times y) = (x \times y) \cdot y = 0$.

3. Area: ${\|x \times y\|} = {\|x\|} {\|y\|}$ if $x, y$ are orthogonal.

From these, we can prove a more general formula for ${\|x \times y\|}$:

$$ {\|x \times y\|}^2 = {\|x\|}^2 {\|y\|}^2 - (x \cdot y)^2 ,$$

or equivalently

$$ {\|x \times y\|} = {\|x\|} {\|y\|} {|\sin\angle(x,y)|} .$$

(Using the [[polarization identity]] to express $x \cdot y$ in terms of $\|x\|$, $\|y\|$, and either $\|x + y\|$ or $\|x - y\|$, this is the double of Hero's Formula for the area of a triangle.)

Conversely, using this more general area formula, we can prove both the restricted area formula and alternation, so that only orthogonality is needed as a separate axiom.

We then have over the [[real numbers]]:

* In [[dimension]] $0$ or $1$, there is one binary cross product: $x \times y \coloneqq 0$.

* In dimension $3$, there are two binary cross products, one for each orientation, matching the classical cross product.

* In dimension $7$, there are uncountably many binary cross products.  Even fixing an orthonormal basis and requiring compatibility with this (in that the cross product of any two distinct basis vectors must be another basis vector or its opposite), there are still 480 distinct cross products.

* In any other finite dimension, there are no binary cross products at all.

These cross products exist over any base field, but as far as I know there may be additional cross products over some fields in dimensions greater than $1$.  (The claim that there are uncountably many cross products in $7$ dimensions becomes the claim that the [[algebraic variety]] of these inner products has dimension greater than $0$; even in the real case, it would be worthwhile to describe this variety in more detail.)  If we pick an orthonormal basis and demand compatibility with it, then the classification above is complete over any field (as the problem becomes essentially combinatorial), except that some of these cross products will be identified in characteristic $2$.

Binary cross products are closely related to [[normed division algebras]] (NDAs).  Given a normed division algebra $A$, the imaginary hyperplane $Im(A)$ inherits an inner product from $A$ and gains a cross product as
$$ x \times y \coloneqq Im(x y) = \frac{1}{2}[x,y] = x y + x \cdot y .$$
Conversely, given an inner product space $V$ with a binary cross product, the orthogonal [[direct sum]] $K \oplus V$ becomes a NDA as
$$ (a,x) (b,y) = (a b - x \cdot y, a y + b x + x \times y) ,$$
where $K$ is the ground field.  (Compare the relationship between complex $*$-algebras and [[Jordan--Lie algebras]], where $A$ is $V \oplus V$ instead of $K \oplus V$, which we again think of as consisting of real and imaginary parts and where we again have two multiplication operations on $V$.)

By [[Hurwitz theorem|Hurwitz's theorem]], the only finite-dimensional NDAs over $\mathbb{R}$ are $\mathbb{R}$ itself (the [[real numbers]]), $\mathbb{C}$ (the [[complex numbers]]), $\mathbb{H}$ (the [[quaternions]]), and $\mathbb{O}$ (the [[octonions]]).  Thus the limited possibilities for binary cross products are determined by the limited possibilities for NDA structures.

By one of the deeper strands of mathematics, this classification of something as innocent-looking as cross-products is closely related not just to the existence of [[normed division algebras]] over the [[real numbers]], but also to all of the following: [[parallelizable manifold|parallelizable]] [[n-spheres]], the existence of [[real spin representations]] (see also at _[[supersymmetry and division algebras]]_), and the [[homotopy groups of spheres]] of [[Hopf invariant one]]; see [there](Hopf+invariant+one#RelationToHSpaceStructureAndNormedDivisionAlgebras).


### $(n-1)$-ary {#counary}

Given an [[orientation|oriented]] [[inner product space]] $V$ of finite [[dimension]] $n$, we can define the signed [[volume]] of an $n$-[[tuple]] of vectors.  (See also [[volume form]].)  This allows us to characterise a __co-unary cross product__ of $n - 1$ vectors as a multilinear operation
$$ &#10761;\colon V^{n - 1} \to V $$
such that
$$ v_0 \cdot &#10761;(v_1,\ldots,v_{n-1}) = vol(v_0,v_1,\ldots,v_{n-1}) $$
always.  There is exactly one such cross product on any such $V$ (so two if we start with an unoriented inner product space).

In $3$ dimensions, this also recovers the classical cross product.  In $2$ dimensions, this produces a __unary cross product__ given by ${\times}(a,b) = (b,-a)$; in a counterclockwise-oriented plane, it rotates a vector clockwise through a right angle.  In $1$ dimension, this is a nullary operation (a constant) whose value is the positive basis vector.


### Vector-valued {#vectorvalued}

Generalizing all of the above, let a __vector-valued cross product__ on any [[inner product space]] $V$ be a multilinear function
$$ &#10761;\colon V^k \to V $$
for some [[natural number]] $k$ (called the [[arity]]) such that:

1. Alternation: $&#10761;(v_1,\ldots,v_k) = 0$ if $v_i = v_j$ for some $i \ne j$.

2. Orthgonality: $&#10761;(v_1,\ldots,v_k)$ is orthogonal to each $v_i$.

3. Area: ${\|&#10761;(v_1,\ldots,v_k)\|} = \prod_i {\|v_i\|}$ if the $v_i$ are mutually orthogonal.

We can again extend (3) to get the magnitude of the cross product of any $k$ vectors; its square is the [[determinant]] of the matrix whose $(i,j)$th entry is $v_i \cdot v_j$ (the [[Gram determinant]]), and then (1) again follows.

Then for an inner product space $V$ over $\mathbb{R}$ of finite dimension $n$, we have:

* If $k = 0$, then there is one cross product for each [[unit vector]] of $V$: none when $n = 0$, two (one for each orientation) when $n = 1$, and uncountably many when $n \geq 2$ (of which $2n$ are compatible with a given basis).

* If $k = 1$, then there is one cross product for each way of writing $\mathbb{R}^n$ as as $n/2$-fold [[internal direct sum]] of $2$-dimensional subspaces and orienting each subspace: one (always $0$) when $n = 0$, two (one for each orientation) when $n = 2$, uncountably many when $n \geq 4$ is even (of which $2^{n/2}(n-1)!!$ are compatible with a given basis), and none when $n$ is odd.

* If $k = 2$, then the possibilities are as listed [above](#binary) for binary cross products: one (always $0$) when $n = 0, 1$, two (one for each orientation) when $n = 3$, uncountably many (related to the octonions, and of which $480$ are compatible with a given basis) when $n = 7$, and none when $n \ne 0, 1, 3, 7$.

* If $k = 3$, then there is one cross product (always $0$) when $n = 0, 1, 2$, two cross products (one for each orientation) when $n = 4$, uncountably many cross products (related to the octonions) when $n = 8$, and none when $n \ne 0, 1, 2, 4, 8$.

* If $4 \leq k \lt n - 1$, then there are no cross products.

* If $k = n - 1$, then there are two cross products, one for each orientation, as described [above](#counary) for $(n-1)$-ary cross products.

* If $k = n$, then there are no cross products.

* If $k \geq n + 1$, then there is one cross product (always $0$).

Or organized by dimension ($n$) rather than arity ($k$):

* If $n = 0$, then there is no cross product when $k = 0$ and one cross product (always zero) when $k \geq 1$.

* If $n = 1$, then there are two cross products (one for each unit vector, or equivalently for each orientation) when $k = 0$, none when $k = 1$, and one (always zero) when $k \geq 2$.

* If $n = 2$, then there are uncountably many cross products (one for each unit vector, of which four are compatible with a given basis) when $k = 0$, two (one for each orientation) when $k = 1$, none when $k = 2$, and one (always zero) when $k \geq 3$.

* If $n = 3$, then there are uncountably many cross products (one for each unit vector, of which six are compatible with a given basis) when $k = 0$, none when $k = 1$, two (one for each orientation) when $k = 2$, none when $k = 3$, and one (always zero) when $k \geq 4$.

* If $n = 4$, then there are uncountably many cross products (one for each unit vector, of which eight are compatible with a given basis) when $k = 0$, uncountably many (four for each $2$-dimensional subspace, and of which twelve are compatible with a given basis) when $k = 1$, none when $k = 2$, two (one for each orientation) when $k = 3$, none when $k = 4$, and one (always zero) when $k \geq 5$.

* If $n = 5$, then there are uncountably many cross products (one for each unit vector, of which ten are compatible with a given basis) when $k = 0$, none when $k = 1, 2, 3$, two (one for each orientation) when $k = 4$, none when $k = 5$, and one (always zero) when $k \geq 6$.

* If $n = 6$, then there are uncountably many cross products (one for each unit vector, of which twelve are compatible with a given basis) when $k = 0$, uncountably many (related to the $2$-dimensional decompositions, and of which $120$ are compatible with a given basis) when $k = 1$, none when $k = 2, 3, 4$, two (one for each orientation) when $k = 5$, none when $k = 6$, and one (always zero) when $k \geq 7$.

* If $n = 7$, then there are uncountably many cross products (one for each unit vector, of which $14$ are compatible with a given basis) when $k = 0$, none when $k = 1$, uncountably many (related to the octonions, and of which $480$ are compatible with a given basis) when $k = 2$, none when $k = 3, 4, 5$, two (one for each orientation) when $k = 6$, none when $k = 7$, and one (always zero) when $k \geq 8$.

* If $n = 8$, then there are uncountably many cross products (one for each unit vector, of which $16$ are compatible with a given basis) when $k = 0$, uncountably many (related to the $2$-dimensional decompositions, and of which $1680$ are compatible with a given basis) when $k = 1$, none when $k = 2, 3$, uncountably many (related to the octonions) when $k = 4$, none when $k = 5, 6$, two (one for each orientation) when $k = 7$, none when $k = 8$, and one (always zero) when $k \geq 9$.

* If $n \geq 9$ is odd, then there are uncountably many cross products (one for each unit vector, of which $2n$ are compatible with a given basis) when $k = 0$, none when $1 \leq k \lt n - 1$, two (one for each orientation) when $k = n - 1$, none when $k = n$, and one (always zero) when $k \geq n + 1$.

* If $n \geq 10$ is even, then there are uncountably many cross products (one for each unit vector, of which $2n$ are compatible with a given basis) when $k = 0$, uncountably many (related to the $2$-dimensional decompositions, and of which $2^{n/2}(n-1)!!$ are compatible with a given orientation) when $k = 1$, none when $2 \leq k \lt n - 1$, two (one for each orientation) when $k = n - 1$, none when $k = n$, and one (always zero) when $k \geq n + 1$.


### Tensor-valued {#tensorvalued}

Fixing a field $K$, let [[Vect]] be $Vect_K$, the [[symmetric monoidal category]] of vector spaces over $K$ (with the usual [[tensor product]]), and let $T$ be any [[symmetric monoidal functor]] from $Vect$ to itself.  Note that any inner product $g\colon V \otimes V \to K$ extends to a (possibly degenerate) inner product $T(g)\colon T(V) \otimes T(V) \to K$; similarly, any element $x$ of $V$, thought of as a linear map $x\colon K \to V$, gives rise to an element $T(x)$ of $T(V)$.  The vector-valued cross products [above](#vectorvalued) use the [[identity functor]] for $T$, but other possible choices for $T$ are $V \mapsto V \otimes V$, $V \mapsto \Lambda^2 V$, and the constant functor $V \mapsto K$.  We could also take $Vect$ to be a [[full subcategory]] of $Vect_K$ closed under the tensor product, such as $Fin Vect_K$; this may allow more possibilities for $T$ in exchange for fewer possibilities for $V$.

Given an inner-product space $V$ and a symmetric monoidal functor $T$, a __$T$-valued cross product__ on $V$ is a multilinear function
$$ &#10761;\colon V^k \to T(V) $$
for some natural arity $k$ such that:

1. Alternation: $&#10761;(v_1,\ldots,v_k) = 0$ if $v_i = v_j$ for some $i \ne j$.

2. Orthogonality: $&#10761;(v_1,\ldots,v_k)$ is orthogonal (in $T(V)$) to each $T(v_i)$.

3. Area: ${\|&#10761;(v_1,\ldots,v_k)\|} = \prod_i {\|v_i\|}$ if the $v_i$ are mutually orthogonal (in $V$).

Again it follows that in any case ${\|&#10761;(v_1,\ldots,v_k)\|}$ is a square root of the Gram determinant, and again this implies both (1) and (3).

I do not know a full list of these, but one important example is the __scalar-valued binary cross product__ in $2$ dimensions:
$$ (a, b) \times (c, d) = a d - b c .$$
Actually, this scalar-valued cross product $x \times y$ is simply the dot product $x \cdot {\times}y$, where ${\times}y$ is the [unary](#counary) cross product in $2$ dimensions.

More generally, in any number $n \geq 2$ of dimensions, there is a __multivector-valued binary cross product__ (actually one for each orientation) whose values are $(n-2)$-[[multivector|vectors]]; this includes the scalar-valued cross product when $n = 2$ and the classical cross product when $n = 3$, but gets more complicated for larger values of $n$.  In particular, for $n = 4$, we have a [[bivector]]-valued cross product, which is the [[Hodge duals]] of the [[exterior product]].

Or generalizing the scalar-valued binary cross product in a different way, the [[volume]] form on an $n$-dimensional inner-product space is a __scalar-valued $n$-ary cross product__.  Notice that there are two of these, one for each orientation, and each of these is the dot product with one of the vector-valued $(n-1)$-ary cross products.  There are no other scalar-valued cross products, except for the identically zero products of arity $k \gt n$ and the two nullary products given by the unit-norm scalars (so just $1$ and $-1$ over the real numbers) for arbitrary $n$.


## Relationships

### Exterior products

The cross product is also called 'outer product', and both of these terms are sometimes also used for the [[exterior product]].  In its most basic form, the exterior product of two vectors $u,v$ is a [[bivector]] $u \wedge v$.  But note that this is *not* a bivector-valued cross product by the definition [above](#tensorvalued), since it lacks orthogonality (and indeed has nothing to do with the inner product).

In $3$ dimensions, given an inner product and an orientation, we can use the [[Hodge dual]] to turn the exterior product into a vector, and this is the classical cross product once more.  In $2$ dimensions, using the same structure, we can turn the bivector into a [[scalar]]; this recovers the scalar-valued binary cross product [above](#tensorvalued).  In general, this produces the binary $(n-2)$-vector-valued cross product.

Using only the inner product but not the orientation, we get (respectively) a [[pseudovector]] (sometimes called an axial vector) or more generally a [[pseudoscalar]] or other [[pseudotensor]]; this perspective is common in [[geometric algebra]].  In general in dimension $n$, a bivector becomes an $(n-2)$-pseudovector, but this is not usually an simplification.

In classical applications of the cross product, often not all of the structure is needed, and the exterior product is really the fundamental concept.


### Curls

If $M$ is a [[Riemannian manifold]], then the [[tangent space]] at each point is an [[inner product space]], so it may be possible to smoothly assign a $k$-ary cross product to these spaces.  If this is done, then we can take the [[curl]] of a $(k-1)$-[[multivector|vector]] [[vector field|field]] as follows:

*  Use the metric to turn the $(k-1)$-vector field into a $(k-1)$-[[differential form|form]].
*  Take the [[exterior differential]] to get a $k$-form.
*  Use the metric again to get a $k$-vector field.
*  Apply the cross product to get a [[vector field]] (or more generally a [[tensor field]] for a tensor-valued cross product).

This vector field is the __curl__ of the original $(k-1)$-vector field.  This justifies the notation $\Del \times X$ for the curl.

(It\'s important that the cross product is [[alternating form|alternating]] and [[multilinear map|multilinear]], so that it makes sense to apply it to a $k$-vector rather than to $k$ individual vectors.)

When $k = 2$ and $n = 3$, there is one smooth choice of cross product for each [[orientation]] of $M$, and we recover the classical notion of curl.

When $k = 1$ and $n = 2$, we may also consider the scalar-valued curl, using the scalar-valued binary cross product described [above](#tensorvalued).  The scalar-valued curl of a vector field $X$ is the same as the [[divergence]] of the rotated vector field ${\times}X$ (using the [unary](#counary) cross product in $2$ dimensions); that is, $\Del \times X = \Del \cdot {\times}X$.

In modern mathematics, of course, we usually think of the exterior differential of differential forms as the fundamental concept, and only turn these forms into vector fields and the like under certain circumstances.


## Related concepts

* [[associative 3-form]]


## References

* The English Wikipedia article _[Seven-dimensional cross product](https://en.wikipedia.org/wiki/Seven-dimensional_cross_product)_ actually covers all non-zero vector-valued cross products in finite dimensions over the real numbers.


[[!redirects cross product]]
[[!redirects cross products]]
[[!redirects vector product]]
[[!redirects vector products]]
[[!redirects vector cross product]]
[[!redirects vector cross products]]

[[!redirects scalar cross product]]
[[!redirects scalar cross products]]
