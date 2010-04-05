# Commutative diagrams

## Idea

A commutative diagram is a [[diagram]] in which [[composition]] is [[path independence|path-independent]].


## Definitions

### Slick definition

For our purposes, a __[[diagram]]__ $D$ in a [[category]] $C$ consists of a [[quiver]] $J$ and a [[functor]] to $C$ from the [[free category]] on $J$:
$$ J \overset{D}\to C ,\; J\;\text{a quiver}. $$
Then this diagram $D$ __commutes__ if this functor $D$ factors (up to [[natural isomorphism]]) through a [[poset]] $P$:
$$ J \to P \to C \;\cong\; J \to C ,\; P\;\text{a poset} ;$$
or equivalently (treating $C$ as a [[strict category]]) if the functor factors up to [[equality]] through a [[proset]] $Q$:
$$ J \to Q \to C \;\cong\; J \to C ,\; Q\;\text{a proset} .$$
In the above, we are identifying quivers, posets, and prosets with certain categories in the usual ways.


### Elementary definition

Recall that a __[[quiver]]__ $J$ consists of a [[set]] $V$ of _vertices_, a set $E$ of _edges_, and two [[functions]] $s,t\colon E \to V$.  Given a category $C$, a __diagram__ $D$ of shape $J$ in a category $C$ is consists of a map from $V$ to the [[objects]] of $C$ and a map from $E$ to the [[morphisms]] of $C$, both denoted $F$, such that $F(s(e)) = S(F(e))$ and $F(t(e)) = T(F(e))$ for each edge $e$, where $S,T$ are the [[source]] and [[target]] maps in $C$.

Recall that a __[[path]]__ $p$ in $J$ consists of a [[list]] $(v_0,v_1,\ldots,v_n)$ of vertices and a list $(e_1,\ldots,e_n)$ of edges such that $s(e_i) = v_{i-1}$ and $t(e_i) = v_{i}$ for each $i$, where $n$ is any [[natural number]] (possibly zero).  We say that $v_0$ is the __source__ of the path and that $v_n$ is its __target__.  Given a path $p$ and a diagram $D$, the __composite__ of $p$ under $D$ is the [[composite]] $F(e_1);\ldots;F(e_n)\colon F(v_0) \to F(v_n)$ in $C$.

A diagram $D$ __commutes__ if, given any two vertices $x,y$ in $J$ and any two paths $p,p'$ with source $x$ and target $y$, the composites of $p$ and $p'$ under $D$ are equal in $C$.


## Links

* [Wikipedia](http://en.wikipedia.org/wiki/Commutative_diagram)
* [Mathworld](http://mathworld.wolfram.com/CommutativeDiagram.html)
* [[alternative experimental definition of commutative diagram|An Experiment]]


[[!redirects commutative diagram]]
[[!redirects commuting diagram]]
