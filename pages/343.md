A __cartesian monoidal category__ is a [[monoidal category]] whose monoidal structure is given by the category-theoretic [[product]] (and so whose unit is a [[terminal object]]).  Any category with finite products can be considered as a cartesian monoidal category (as long as we have either (1) a specified product for each pair of objects, (2) a global [[axiom of choice]], or (3) we allow the monoidal product to be an [[anafunctor]]).  Note that the term __cartesian category__ usually means a category with finite products but can also mean a [[finitely complete category]].

Cartesian monoidal categories have a number of special and important properties, such as the existence of a diagonal maps $A \to A\otimes A$ and augmentations $A\to I$ for any object $A$.  These maps make any object into a [[comonoid]] in a unique way.  Moreover, one can show that any monoidal category equipped with suitably well-behaved diagonals and augmentations _must_ in fact be cartesian monoidal.

More precisely, we may define a monoidal category $C$ to be [[semicartesian monoidal category]] if the unit for the tensor product is the [[terminal object]], say $1$.   If this is true, any tensor product of objects $x \otimes y$ comes equipped with morphisms to $x$ and $y$, given by
$$ x \otimes y \stackrel{1 \otimes !}{\to} x \otimes 1 \stackrel{r_x}{\to} x $$
and
$$ x \otimes y \stackrel{! \otimes 1}{\to} 1 \otimes y \stackrel{\ell_y}{\to} y $$
where $!$ is the unique morphism to the terminal object and $r$, $\ell$ are the right and left unitors.  We can thus ask whether these morphisms 
$$ x \otimes y  \to x $$
$$  x \otimes y \to y$$
satisfy the universal property of a [[product]].  If so, it is a theorem, perhaps due to Eilenberg and Kelly, that $C$ is a cartesian monoidal category.  (This theorem is probably in Eilenberg and Kelly's paper on closed categories, but they may not have been the first to note it.)

Some examples of semicartesian monoidal categories that are not cartesian include:

* the category of Poisson manifolds with the usual product of Poisson manifolds as its tensor product, 

* the opposite of the category of associative algebras over a field $k$ with its usual tensor product $A \otimes B$, 

* the category of affine spaces made into a monoidal category where the corresponding internal hom has $hom(x,y)$ being the set of affine maps from $x$ to $y$, made into an affine space via pointwise operations,

* the category of convex sets, made into a monoidal category in a way analogous to the affine space example above.

A cartesian monoidal category which is also [[closed monoidal category|closed]] is called a [[cartesian closed category]].


[[!redirects cartesian categories]]
[[!redirects cartesian category]]
[[!redirects cartesian monoidal categories]]