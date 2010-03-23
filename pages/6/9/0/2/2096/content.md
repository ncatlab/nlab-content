#Idea#

Two maps $f : X \to Z$ and $g : Y \to Z$ of [[manifold]]s are _transversal_ roughly if the images of $X$ and $Y$ in $Z$ do not "touch tangentially".

# Definition #

Two maps $f : X \to Z$ and $g : Y \to Z$ of [[manifold]]s are _transversal_ if for all point $x \in X$ and $y \in Y$ with $f(x) = z = g(y)$ the differentials of $f$ and $g$ in these points span the entire tangent space at $z$ in that

$$
  im(d f) \oplus im(d g) \simeq T_z Z
  \,.
$$

# Remarks #

Various constructions involving [[pullback]]s of [[manifold]]s work as expected only for pullbacks involving transversal maps. 

This is to be regarded as the dual of the possibly more familiar statement that various constructions involving [[quotient object|quotient]]s only work as expected for _free_ [[action]]s.

Both of these "problems" are solved by passing from the ordinary $1$-[[1-category|category]] of manifolds to a suitable [[higher category theory|higher category]] of [[generalized smooth spaces]].

More precisely: 

* the problem with the [[pushout]]s (quotients) is resolved by passing to [[stack]]s and [[smooth infinity-stack]]s.

* the problem with the [[pullback]]s is resolved by passing to [[derived stack]]s. Concretely for the case of manifolds this is discussed at [[derived smooth manifold]].


[[!redirects transversal map]]