A [[monoidal category]] is **semicartesian** if the unit for the tensor product is a [[terminal object]].  This a weakening of the concept of [[cartesian monoidal category]], which might seem like pointless [[centipede mathematics]] were it not for the existence of many interesting examples.  

Some examples of semicartesian monoidal categories that are not cartesian include the following.

* The category of [[Poisson manifold]]s with the usual product of Poisson manifolds as its tensor product.

* The opposite of the category of [[associative algebra]]s over a given [[base field]] $k$ with its usual tensor product $A \otimes B$.

* The category of [[strict 2-categories]] with the [[Gray tensor product]], and the category of [[strict omega-categories]] with the [[Crans-Gray tensor product]].

* The category of [[affine space|affine spaces]] made into a [[closed monoidal category]] where the [[internal hom]] has $hom(x,y)$ being the set of affine linear maps from $x$ to $y$, made into an affine space via pointwise operations.

* The category of [[convex space|convex spaces]], also known as 'barycentric algebras', made into a closed monoidal category where the internal hom has $hom(x,y)$ being the set of convex linear maps from $x$ to $y$, made into an barycentric algebra via pointwise operations.

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
