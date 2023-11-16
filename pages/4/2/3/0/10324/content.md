
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Statement

Let $M$ be a [[smooth manifold]]. By an ([[embedding|embedded]]) **[[submanifold]]** we mean a [[immersion of smooth manifolds|smooth immersion]] of [[smooth manifolds]] $i \colon X \to M$ that is a topological embedding of $X$ as a [[closed subspace]] of $M$. 

In that case, we have that for each $x \in X$, the [[tangent space]] $T_x X$ is included in the subspace $T_{i(x)} M$. We define the normal fiber $N_x$ to be the quotient $T_{i(x)} M/T_x X$ and the **[[normal bundle]]** (with respect to the embedding $i$) to be the space $N X$ consisting of pairs $\{(x, v): x \in X, v \in N_x\}$, forming a vector bundle over $X$ in an evident way. We let $i_0 \colon X \to N X$ denote the zero section. An [[open neighborhood]] $V$ of the zero section is **convex** if its intersection with $N_x$ is a [[convex subset]] of the vector space $N_x$. 

+-- {: .num_theorem} 
###### Theorem 
**(Tubular Neighborhood theorem)** 

For any [[submanifold]] $i \colon X \hookrightarrow M$, there is an [[open neighborhood]] $U$ of $i(X)$ in $M$ and a convex open neighborhood $V$ of $i_0(X)$ in $N X$ and a [[diffeomorphism]] $\phi: U \to V$ such that the diagram 

$$
  \array{
    X & & 
    \\ 
    \mathllap{i} \downarrow & \searrow{}^{\mathrlap{i_0}} & 
    \\ 
    U & \underset{\phi}{\longrightarrow} & V
}
$$ 

[[commuting diagram|commutes]]. Such $U$ is called a **[[tubular neighbourhood]]** of $i(X)$.

=-- 

See for instance ([Silva 06, theorem 6.5](#Silva06))

## References 

* {#Silva06} [[Ana Cannas da Silva]], §6.2 in: *Lectures on Symplectic Geometry*, Lecture Notes in Mathematics **1764**, Springer (2008) &lbrack;[doi:10.1007/978-3-540-45330-7](https://doi.org/10.1007/978-3-540-45330-7), [pdf](https://www.math.tecnico.ulisboa.pt/~acannas/Books/lsg.pdf)&rbrack;


[[!redirects tubular neighbourhood theorem]]
