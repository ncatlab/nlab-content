#Definition#

Recall that a [[point of a topos|point]] $x$ of a [[topos]] $E$ is a geometric morphism 

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
  \end{aligned}
  \,.
$$

So for sheaves on (open subsets of) topological spaces the stalk at a given point is the colimit over all values of the sheaf on open subsets containing this point.

By the general definition of colimits in [[Set]] described at [[limits and colimits by example]], the elements in this colimit can in turn be described as equivalence classes represented pairs $(z, V)$ with $x \in V$ $z \in F(V)$, where the equivalence relation says that two such pairs $(z_1, V_1)$ and $(z_2, V_2)$ coincide if there is a third pair $(z,U)$ with $U \subset V_1$ and $U \subset V_2$ such that $z = z_1|_U = z_2|_U$.

for $F = C(-)$ a sheaf of functions on $X$, such an equivalence class, hence such an element in a stalk of $F$ is called a function **germ**.

### testing sheaf morphisms on stalks ###

For $E = Sh(X)$ a topos of sheaves on a topological space (or generally if the topos $E$ has "[[point of a topos|enough points]]"), the bahaviour of morphisms $f : A \to B$ in $E$ can be tested on stalks

+-- {: .un_theorem}
###### Theorem

A morphism $f : A \to B$ of sheaves on $X$ is a

* [[monomorphism]]

* resp. [[epimorphism]]

* resp. [[isomorphism]]

if and only every induced map of stalk sets $stalk_x(f) : stalk_x(A) \to stalk_x(B)$ is, for all $x \in X$
=--

+-- {: .proof}
###### Proof

The statement for isomorphisms follows from the identification of sheaves with [[etale space]]s (e.g. section II, 6, corollary 3 in MacLane-Moerdijk, [[Sheaves in Geometry and Logic]]). The statement for epimorphisms/monomorphisms is proposition 6 there. 

=--

### Example ###

Let $X$ be a smooth manifold and let $\Omega^n(X)$ and $Z^{n+1}(X)$ be the sheaves of differential $n$-forms and that of _closed_ differential $(n+1)$-forms on $X$, respectively, for some $n \in \mathbb{N}$. Let

$$
  d : \Omega^n(X) \to Z^{n+1}
$$

be the morphism of sheaves that is given on each open subset by the deRham differential.

Then:

* for $U \subset X$ the map $d_U : \Omega^n(U) \to Z^{n+1}(U)$ need not be [[epimorphism|epi]], since not every closed form is exact;

* but by the [[Poincare lemma]] every closed form is _locally_ exact, so that for each $x \in X$ the map of stalks $d_x : stalk_x(\Omega^n(X)) \to stalk_x(Z^{n+1}(X))$ is an epimorphism.

Accordingly, the morphism $d : \Omega^n(X) \to Z^{n+1}(X)$ is an [[epimorphism]] of sheaves.

This kind of example plays a crucial role in the computation of [[abelian sheaf cohomology]], see the examples listed there.
