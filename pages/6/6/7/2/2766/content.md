**WARNING: Tentative**

## Definition 

Let $F:J\to C$ be a [[diagram]] in a category $C$. Also, for any objects $c,c'\in C$, let $T:\Delta(c)\to F$ and $T':\Delta(c')\to F$ denote [[cones]] over $F$. 

A **cone morphism** is a [[natural transformation]] $\Delta(\phi)\colon \Delta(c)\to\Delta(c')$ such that the diagram
$$\array{
\Delta(c) &{}&\stackrel{\Delta(\phi)}{\longrightarrow} &{}& \Delta(c') \\
{}& \mathllap{\scriptsize{T}}\searrow &{}& \swarrow\mathrlap{\scriptsize{T'}} &{}  \\
{}&{}&F&{}&{}
}
$$
commutes.

Note, in particular, this means that all component diagrams

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

[[Eric]]: Thanks Finn! I'm still learning all this, so it'll take me some time to absorb what you said. It sounds good though :) Either way, it sounds like some potentially good additional content.

[[Finn Lawler]]:  I should point out that a natural transformation $\alpha: \Delta c \Rightarrow \Delta c'$ is very nearly exactly the same thing as a morphism $\phi: c \to c'$ (it's $\phi$ in each component, which you'll see if you draw $\alpha$'s naturality square, so it's $\Delta \phi$ for some $\phi$).  Now look at the triangle above, write $\Delta \phi : \Delta c \to \Delta c'$ instead of $\phi$ and erase the $j$s and you have the morphism in the comma category.

I hope this helps.  If it's done the opposite, apologies.  I've a habit of trying the one and accomplishing the other.
=--

**The following material is very tentative**

Note that given any cone $T':\Delta c'\to F$ and any morphism $\phi:c\to c'$ we can obtain a new cone $T:\Delta c\to F$ whose components are given by

$$T_j = \phi^* T'_j =  T'_j\circ \phi,$$

which can be thought of as "pulling back" the cone $T'$ along $\phi$.

+--{.query}
[[Finn Lawler]]: I think this is just composition with $\Delta \phi$.
=--

[[!redirects cone morphisms]]
[[!redirects cone function]]
[[!redirects cone functions]]