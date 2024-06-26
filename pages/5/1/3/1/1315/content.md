
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### $\infty$-Lie theory
+-- {: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{: toc}

## Idea

For $X$ a smooth space, there are useful refinements of the [[fundamental groupoid]] $\Pi_1(X)$ which remember more than just the [[homotopy]] class of [[paths]], i.e. whose morphisms are (piecewise, say) smooth paths in $X$ modulo an equivalence relation still strong enough to induce a groupoid structure, but weaker than dividing out homotopies relative to endpoints.


## Definition

Let $X$ be a smooth [[manifold]].

+-- {: .un_defn}
###### Definition
For $\gamma_1, \gamma_2  : [0,1] \to X$ two smooth maps, a **[[thin homotopy]]** $\gamma_1 \Rightarrow \gamma_2$ is a smooth [[homotopy (as an operation)|homotopy]], i.e. a smooth map
$$
  \Sigma : [0,1]^2 \to X
$$
with 

* $\Sigma(0,-) = \gamma_1$
* $\Sigma(1,-) = \gamma_2$
* $\Sigma(-,0) = \gamma_1(0) = \gamma_2(0)$
* $\Sigma(-,1) = \gamma_1(1) = \gamma_2(1)$

which is _thin_ in that it doesn't sweep out any surface: every $2$-form pulled back to it vanishes:

* $\forall B \in \Omega^2(X)\colon \Sigma^* B = 0$.
=--

+-- {: .un_defn}
###### Definition
A path $\gamma\colon [0,1] \to X$ has **[[sitting instants]]** if there is a neighbourhood of the boundary of $[0,1]$ such that $\gamma$ is locally constant restricted to that.
=--

+-- {: .un_defn}
###### Definition
The **path groupoid** $P_1(X)$ is the [[diffeological groupoid]] that has

* $Obj(P_1(X)) = X$
* $P_1(X)(x,y) = \{$thin-homotopy classes of paths $\gamma\colon x \to y $ with sitting instants$\}$.

Composition of paths comes from concatenation and reparameterization of representatives. The quotient by thin-homotopy ensures that this yields an associative composition with inverses for each path.
=--

This definition makes sense for $X$ any [[generalized smooth space]], in particular for $X$ a [[sheaf]] on [[Diff]].

Moreover, $P_1(X)$ is always itself naturally a groupoid [[internal category|internal to]] [[generalized smooth spaces]]: if $X$ is a [[Chen space]] or [[diffeological space]] then $P_1(X)$ is itself internal to that category.  However, even if $X$ is a manifold, $P_1(X)$ will not be a manifold, see [[smooth structure of the path groupoid]] for details.

There are various generalizations of the path groupoid to [[n-groupoids]] and [[∞-groupoids]]. See

* [[path n-groupoid]],

* [[path ∞-groupoid]].


## Remarks

If $G$ is a Lie group, then internal (i.e. smooth) functors from the path groupoid to the one-object Lie groupoid corresponding to $G$ are in bijection to $Lie(G)$-valued differential forms on $X$. With gauge transformations regarded as morphisms between Lie-algebra valued differential forms, this extends naturally to an equivalence of categories
$$
  [P_1(X), \mathbf{B}G] \simeq \Omega^2(X, Lie(G))
$$
where on the left the [[functor category]] is the one of internal (smooth) functors.

More generally, smooth [[anafunctors]] from $P_1(X)$ to $\mathbf{B}G$ are canonically equivalent to smooth $G$-principal bundles on $X$ with [[connection]]:
$$
  Ana(P_1(X), \mathbf{B}G) \simeq G Bund_\nabla(X)
  \,.
$$

See also 

* [[Atiyah Lie groupoid]].


## References

For "path groupoids" in [[simplicial sets]], aka *[[Dwyer-Kan loop groupoids]]* see there, such as:

* [[André Joyal]], [[Myles Tierney]], *On the theory of path groupoids*, Journal of Pure and Applied Algebra **149** 1 (2000) 69-100 &lbrack;<a href="https://doi.org/10.1016/S0022-4049(98)00164-9">doi:10.1016/S0022-4049(98)00164-9</a>&rbrack;


[[!redirects path goupoid]]
[[!redirects path groupoids]]

[[!redirects smooth path groupoid]]
[[!redirects smooth path groupoids]]
