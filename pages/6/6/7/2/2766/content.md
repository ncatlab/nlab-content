**WARNING: Tentative**

## Definition 

Let $F:J\to C$ be a [[diagram]] in a category $C$.

For any objects $c,c'\in C$, let $T:\Delta c\to F$ and $T':\Delta c'\to F$ denote [[cones]] over $F$. A **cone morpmism** is a $C$-morphism $\phi\colon c \to c'$ such that all component diagrams

$$\array{
c &{}&\stackrel{\phi}{\longrightarrow} &{}& c' \\
{}& \mathllap{\scriptsize{T_j}}\searrow &{}& \swarrow\mathrlap{\scriptsize{T'_j}} &{}  \\
{}&{}&F(j)&{}&{}
}
$$

commute.

+--{.query}
[[Eric]]: What is the "component free" way to say that?

[[Finn Lawler]]:  I think the category of cones over $F$ is the comma category $\Delta / F$, so that a morphism $\alpha : T \to T'$ should be just a natural transformation $\alpha : \Delta c \Rightarrow \Delta c'$ such that $T' \alpha = T$.  That gives your condition in components, I think.
=--

**The following material is very tentative**

Note that given any cone $T':\Delta c'\to F$ and any morphism $\phi:c\to c'$ we can obtain a new cone $T:\Delta c\to F$ whose components are given by

$$T_j = \phi^* T'_j =  T'_j\circ \phi,$$

which can be thought of as "pulling back" the cone $T'$ along $\phi$.

[[!redirects cone morphisms]]
[[!redirects cone function]]
[[!redirects cone functions]]