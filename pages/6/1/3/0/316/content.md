
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

### As a contracted cylinder

The **cone** over an [[object]] $X$ in a [[category]] with [[pushout]]s, [[terminal object]]  and with [[cylinder object]] $X \times I$ is the [[pushout]] $cone(X) := X\times I \coprod_X *$

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


[[!redirects cones]]