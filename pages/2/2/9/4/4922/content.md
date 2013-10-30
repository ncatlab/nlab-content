+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

### Internal to a general category

In a category $C$, for $G$ a [[group object]] and $H \hookrightarrow G$ a [[subgroup|subgroup object]], the left/right _object of cosets_ is the [[orbit|object of orbits]] of $G$ under left/right multiplication by $H$.

Explicitly, the left coset space $G/H$ [[coequalizes]] the parallel morphisms
$$
  H \times G \underoverset{\mu}{proj_G}\rightrightarrows G 
$$ 
where $\mu$ is (the inclusion $H\times G \hookrightarrow G\times G$ composed with) the group multiplication.  

Simiarly, the right coset space $H\backslash G$ [[coequalizes]] the parallel morphisms
$$
  G \times H \underoverset{proj_G}{\mu}\rightrightarrows G 
$$ 

### Internal to Set

Specializing the above definition to the case where $C$ is the well-pointed topos $Set$, given an element $g$ of $G$, its orbit $gH$ is an element of $G/H$ and is called a _left coset_.

Using comprehension, we can write
$$
  G/H = \{g H | g \in G\}
$$

Similar situation on the right.

## Properties 

The coset inherits the structure of a group if $H$ is a [[normal subgroup]].

Unless $G$ is abelian, considering both left and right coset spaces provide different information. 

The natural projection $G\to G/H$, mapping the element $g$ to the element $g H$, realizes $G$ as an $H$-[[principal bundle]] over $G/H$. We therefore have a [[homotopy pullback]]
$$
  \array{
   G & \to&* 
   \\
    \downarrow && \downarrow
   \\
   G/H &\to& \mathbf{B}H
  }
$$
where $\mathbf{B}H$ is the [[delooping|delooping groupoid]] of $H$.
By the [[pasting law]] for [[homotopy pullbacks]] then we get the [[homotopy pullback]]

$$
  \array{
   G/H & \to&\mathbf{B}H 
   \\
    \downarrow && \downarrow
   \\
   * &\to& \mathbf{B}G
  }
$$

## Related concepts

* [[coset space]]

* [[coadjoint orbit]]

* [[index of a subgroup]]

[[!redirects coset]]
[[!redirects cosets]]
[[!redirects left coset]]
[[!redirects right coset]]
[[!redirects left cosets]]
[[!redirects right cosets]]
