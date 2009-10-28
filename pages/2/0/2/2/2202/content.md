A [[monoidal category]] is **semicartesian** if the unit for the tensor product is a [[terminal object]].  This a weakening of the concept of [[cartesian monoidal category]], which might seem like pointless [[centipede mathematics]] were it not for the existence of many interesting examples.  

Some examples of semicartesian monoidal categories that are not cartesian include the following.

* The category of [[Poisson manifold]]s with the usual product of Poisson manifolds as its tensor product.

* The opposite of the category of [[associative algebra]]s over a given [[base field]] $k$ with its usual tensor product $A \otimes B$.

* The category of [[strict 2-categories]] with the [[Gray tensor product]], and the category of [[strict omega-categories]] with the [[Crans-Gray tensor product]].

* The category of [[affine space]]s made into a [[closed monoidal category]] where the [[internal hom]] has $hom(x,y)$ being the set of affine linear maps from $x$ to $y$, made into an affine space via pointwise operations.

* The category of [[barycentric algebra]]s, made into a closed monoidal category where the internal hom has $hom(x,y)$ being the set of convex linear maps from $x$ to $y$, made into an barycentric algebra via pointwise operations.

+-- {: .query}
Which meaning of 'convex set' are you using here?

[[John Baez]]: roughly speaking: a set equipped with $n$-ary 'convex linear combination' operations, one for every $n$-tuple of real numbers in $[0,1]$ that add to 1, obeying some obvious axioms.  There is a Lawvere theory for convex sets and it's a <i>lot</i> like the algebraic theory for real [[affine space|affine spaces]] (described already on the $n$Lab): I think you just throw in one extra condition, namely that we only allow affine linear combinations where the coefficients lie in [0,1].

_Toby_:  Yeah, I like that theory.  But note that some people limit 'convex set' to mean a convex subset of a (real) affine space, and your convex sets are more general.  See Section 12.7 of _[[HAF]]_ or page 1 of [this paper](http://staff.science.uva.nl/~gfontain/tacl09-abstracts/tacl2009_submission_48.pdf), which suggest the term 'barycentric algebra' (which I have used above).

[[Mike Shulman]]: What about "convex space" or "abstract convex space"?

_Toby_:  But &lsaquo;convex subset of an affine space&rsaquo; also has a perfectly good abstract definition, and people do use 'convex set' in this sense.  AFAIK, you\'re free to distinguish this from 'convex space', but that\'s liable to be confusing.  (I will shortly write a bit at [[barycentric algebra]] to explain the facts that I\'m merely alluding to here.)
=--

In a semicartesian monoidal category, any tensor product of objects $x \otimes y$ comes equipped with morphisms 
$$ p_x : x \otimes y  \to x $$
$$ p_y : x \otimes y \to y$$
given by
$$ x \otimes y \stackrel{1 \otimes e_y}{\longrightarrow} x \otimes I \stackrel{r_x}{\longrightarrow} x $$
and
$$ x \otimes y \stackrel{e_x \otimes 1}{\longrightarrow} I \otimes y \stackrel{\ell_y}{\longrightarrow} y $$
respectively, where $e$ stands for the unique morphism to the terminal object and $r$, $\ell$ are the right and left unitors.  We can thus ask whether $p_x$ and $p_y$ make $x \otimes y$ into the [[product]] of $x$ and $y$.  If so, it is a theorem that $C$ is a cartesian monoidal category.  (This theorem is probably in Eilenberg and Kelly's paper on closed categories, but they may not have been the first to note it.)  This also follows if we posit the existence of a natural [[diagonal morphism]] $x \to x \otimes x$.


[[!redirects semicartesian category]]
[[!redirects semi-cartesian category]]
[[!redirects semi-Cartesian category]]
[[!redirects semicartesian monoidal categories]]
[[!redirects semi-cartesian monoidal category]]
[[!redirects semi-cartesian monoidal categories]]
[[!redirects semicartesian categories]]
[[!redirects semi-cartesian categories]]
[[!redirects semi-Cartesian categories]]
