#Definition#

Recall that a [[point of a topos|point x of a topos E]] is a geometric morphism 

$$
  x : Set \to E
  \,.
$$ 

The **stalk** at $x$ of an object $e \in E$ is the image of $e$ under the corresponding [[inverse image]] morphism

$$
  x^* : E \to set
$$

i.e.

$$
  stalk_x(e) := x^*(e)
  \,.
$$

## Special case of sheaf topoi ##

If $E$ is the [[category of sheaves]] on the [[category of open subsets]] $Op(X)$ of a [[topological space]] $X$

$$
  E = Sh(X)
  \,,
$$

then the [[point of a topos|topos points]] of $E$ come precisely from the ordinmary points 

$$
  (x : {*} \to X)   in  Top
  \,,
$$

of the space $X$, where the [[direct image]] morphism

$$
  x_* : Set \to Sh(X)
$$

sends every set to the sheaf which is the constant functor on that set. By the general [[Kan extension]] formula for the [[inverse image]] (see there) one finds in this case for any [[sheaf]] $F \in Sh(X)$ the stalk 

$$
  \begin{aligned}
    stalk_x(F)
    & =
    colim_{({*} \to x^{-1}(V)) \in (const_{*}, x^{-1}) } F(V)
    \\
    &=
    colim_{V \subset X | x \in V} F(V)
  \,.
$$

So for sheaves on (open subsets of) topological spaces the stalk at a given point is the colimit over all values of the sheaf on open subsets containing this point.

By the general definition of colimits in [[Set]] described at [[limits and colimits by example]], the elements in this colimit can in turn be described as equivalence classes represented pairs $(z, V)$ with $x \in V$ $z \in F(V)$, where the equivalence relation says that two such pairs $(z_1, V_1)$ and $(z_2, V_2)$ coincide if there is a third pair $(z,U)$ with $U \subset V_1$ and $U \subset V_2$ such that $z = z_1|_U = z_2|_U$.

for $F = C(-)$ a sheaf of functions on $X$, such an equivalence class, hence such an element in a stalk of $F$ is called a function **germ**.

  