

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}


## Idea

In [[category theory]], a _cone_ over a [[diagram]] $F\colon J \to C$ is an [[object]] $c$ in $C$ equipped with a [[morphism]] from $C$ to each vertex of $F$, such that every *new* triangle arising in this way [[commutative triangle|commutes]].

A cone which is [[universal property|universal]] is a [[limit]].

The dual notion is _[[cocone]]_, where $c$ is equipped with a morphism *to* $c$ *from* each vertex of $F$ (but $c$ itself still belongs to $C$).

This definition generalizes to [[higher category theory]]. In particular in [[(∞,1)-category theory]] a cone over an [[∞-groupoid]] is essentially a cone in the sense of [[homotopy theory]].


## Definition

### As a contracted cylinder

The **cone** over an [[object]] $X$ in a [[category]] with [[pushout]]s, [[terminal object]]  and with [[cylinder object]] $X \times I$ is the [[pushout]] $cone(X) := X\times I \amalg_X *$

$$
  \array{
    X &\stackrel{d_1}{\to} & X \times I
    \\
    \downarrow && \downarrow
    \\
    * &\to& cone(X)
  }
  \,.
$$

See also [[mapping cone]].




### Over a diagram in a category

Let $F: J \to C$ be a [[diagram]] in a [[category]] $C$. 

If $c$ is an object of $C$, a **cone** from $c$ to $F$ is a [[natural transformation]] 
$$T: \Delta(c) \to F$$ 
where $\Delta(c):J\to C$ denotes the [[constant functor]].

In other words, a cone consists of morphisms (called the **components** of the cone) 

$$T_j: c \to F(j),$$

one for each object $j$ of $J$, which are compatible with all the morphisms $F(f): F(j) \to F(k)$ of the diagram, in the sense that each diagram 
$$\array{
{}&{}&c&{}&{} \\
{}& \mathllap{\scriptsize{T_j}}\swarrow &{}& \searrow\mathrlap{\scriptsize{T_k}} &{}  \\
F(j) &{}&\stackrel{F(f)}{\longrightarrow} &{}& F(k) \\
}
$$
commutes.

It's called a cone because one pictures $c$ as sitting at the vertex, and the diagram itself as forming the base of the cone. 

A [[cocone]] in $C$ is precisely a cone in the [[opposite category]] $C^op$.


### Over a diagram in an $(\infty,1)$-category

For $F : D \to C$ a [[diagram]] of [[(∞,1)-categories]], i.e. an [[(∞,1)-functor]], the $(\infty,1)$-category of $(\infty,1)$-cones over $F$ is the [[over quasi-category]] denoted $C_{/F}$. Its objects are cones over $F$. Its [[k-morphism]]s are $k$-homotopies between cones. The [[limit in a quasi-category|(∞,1)-categorical limit]] over $F$ is, if it exists, the [[initial object]] in $C_{/F}$.


[[!redirects cone]]
[[!redirects cones]]
