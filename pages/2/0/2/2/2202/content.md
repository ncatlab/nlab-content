A [[monoidal category]] is **semicartesian** if the unit for the tensor product is terminal.  This a weakening of the concept of [[cartesian monoidal category]], which would seem like pointless [[centipede mathematics]] were it not for the existence of many interesting examples.  

Some examples of semicartesian monoidal categories that are not cartesian include:

* the category of Poisson manifolds with the usual product of Poisson manifolds as its tensor product, 

* the opposite of the category of associative algebras over a field $k$ with its usual tensor product $A \otimes B$, 

* the category of affine spaces made into a monoidal category where the corresponding internal hom has $hom(x,y)$ being the set of affine maps from $x$ to $y$, made into an affine space via pointwise operations,

* the category of convex sets, made into a monoidal category where the corresponding internal hom has $hom(x,y)$ being the set of convex maps from $x$ to $y$, made into an convex space via pointwise operations.

In a semicartesian monoidal category, any tensor product of objects $x \otimes y$ comes equipped with morphisms 
$$ p_x : x \otimes y  \to x $$
$$ p_y : x \otimes y \to y$$
given by
$$ x \otimes y \stackrel{1 \otimes e_y}{\longrightarrow} x \otimes I \stackrel{r_x}{\longrightarrow} x $$
and
$$ x \otimes y \stackrel{e_x \otimes 1}{\longrightarrow} I \otimes y \stackrel{\ell_y}{\longrightarrow} y $$
respectively, where $e$ stands for the unique morphism to the terminal object and $r$, $\ell$ are the right and left unitors.  We can thus ask whether $p_x$ and $p_y$ make $x \otimes y$ into the [[product]] of $x$ and $y$.  If so, it is a theorem that $C$ is a cartesian monoidal category.  (This theorem is probably in Eilenberg and Kelly's paper on closed categories, but they may not have been the first to note it.)