The __Godement product__ of two [[natural transformation]]s between appropriate [[functor]]s is their [[horizontal composition]] as 2-cells in the [[2-category]] [[Cat]] of categories, functors and natural transformations.

For categories $A,B,C$, if $\alpha: F_1\to G_1 : A\to B$ and $\beta: F_2\to G_2 : B\to C$ are natural transformations of functors, the components $(\alpha * \beta)_M$ of the Godement product $\alpha * \beta: F_2\circ F_1\to G_2\circ G_1$ are defined by any of the two equivalent formulas:
$$
(\beta * \alpha)_M = \beta_{F_2 M}\circ G_1(\alpha_M) 
$$
$$
(\beta * \alpha)_M = G_2(\alpha_M)\circ\beta_{F_1 M} 
$$

The Godement product is strictly associative (so that $Cat$ is a [[strict 2-category]]).

The [[interchange law]] in (general) 2-categories (which in the case of $Cat$ boils down to assertion that the two formulas above are equivalent) is also sometimes called _Godement interchange law_.