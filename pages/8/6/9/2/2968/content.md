
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In classical [[homotopy theory]], a _homotopy lifting property_ is a condition satisfied by [[continuous map]]s between [[topological space]]s. 
More generally, such a condition may appear in more general context of a [[category]] with [[product]]s and with an [[interval object]] $I$:

The [[Eckmann-Hilton duality|Eckmann–Hilton dual]] of the homotopy lifting property is the [[homotopy extension property]].


## Definition

Let $C$ be a [[category]] with [[product]]s and with [[interval object]] $I$.

A [[morphism]] $E \to B$ has the homotopy lifting property if it has the [[right lifting property]] with respect to all morphisms of the form $(Id,0) :  Y \to Y \times I$.

This means that for all commuting squares

$$
  \array{
    Y &\stackrel{f}\to& E
    \\
    \downarrow &&  \downarrow^p
    \\
    Y\times I &\stackrel{F}{\to}& B
  }
$$

there exists a morphism $\sigma : Y \times I \to E$ such that both triangles in 

$$
  \array{
    Y &\stackrel{f}\to& E
    \\
    \downarrow &{}^\sigma\nearrow&  \downarrow^p
    \\
    Y\times I &\stackrel{F}{\to}& B
  }
$$
commute.


For $Y = *$ a [[generator]] this can be rephrased as saying that the 
universal morphism $E^I \to B^I \times_B E$ induced by the commuting square

$$
  \array{
    E^I &\to& E
    \\
    \downarrow && \downarrow
    \\
    B^I &\to& B
  }
$$

is an [[epimorphism]]. If it is even an [[isomorphism]] then the lift $\sigma$ exists _uniquely_ . 


The homotopy lifting property is an instance of a [[right lifting property]]. 


## Examples

### For topological spaces

Here the ambient category is $C = $ [[Top]] and the [[interval object]] is the [[topological interval]] $I = [0,1]$.

A [[continuous map]] $p:E\to B$ of [[topological spaces]] satisfies the **homotopy lifting property** (or *covering homotopy property*) with respect to a space $Y$ if for every [[commuting square]] in $Top$

$$
  \array{
    Y &\stackrel{f}\to& E
    \\
    \downarrow^{\sigma_0} &{}^{\tilde{F}}\nearrow&  \downarrow^p
    \\
    Y\times I &\stackrel{F}{\to}& B
  }
  \,.
$$

there is a diagonal such that the entire diagram commutes. The map $\sigma_0:Y\to Y\times I$ is given by $y\mapsto (y,0)$ for $y\in Y$.

A map $p$ is a **[[Hurewicz fibration]]** if it satisfies the homotopy lifting property with respect to all spaces $X$. A map $p$ is a **[[Serre fibration]]** if it satisfies the homotopy lifting property with respect to all disks (equivalently, all topological [[cube]]s). 


There are weaker notions than the usual homotopy lifting property. For example, in the notion of [[Dold fibration]] one requires in the above diagram that the lower triangle is commutative while the upper one is commutative only up to a homotopy. Alternatively, one can characterize the Dold fibrations by the delayed homotopy lifting property, where instead the notion of [[delayed homotopy]] is used, but the lift makes the division of the square strictly commutative. 

### For metric spaces

For [[metric spaces]], there is also a weaker notion, the [[approximate homotopy lifting property]]. 

### For quasi-categories

Morphism between [[quasi-categories]] that are left [[fibrations of quasi-categories]] satisfy the homotopy lifting property with respect to $\Delta[0] \hookrightarrow \Delta[1]$

### For smooth bundles

[[!redirects covering homotopy property]]