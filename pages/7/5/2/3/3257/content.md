# Canonical transformations
* table of contents
{: toc}


## Idea

[[Jim Dolan]] (or if not him, then somebody in [[John Baez]]\'s circle) has tried to make the term 'canonical' precise in a way analogous to the way in which the concept of [[natural transformation]] has made the term 'natural' precise.

A canonical transformation is like a natural transformation except that it is only required to be natural with respect to [[isomorphisms]].  Every natural transformation is canonical, but not every canonical transformation is natural.


## Definition

Given [[categories]] $C$ and $D$ and [[functors]] $F\colon C \to D$ and $G\colon C \to D$, a __canonical transformation__ $\eta\colon F \to G$ consists of a family of [[morphisms]] of $D$ indexed by the [[objects]] of $C$:

$$ \eta(x)\colon F(x) \to G(x) ,\;\;\; x\colon C ,$$

such that the following diagram commutes for every [[isomorphism] in $C$:

$$ \array {
   F(x)            & \overset{\eta(x)}\to  & G(x) \\
   F(u) \downarrow &                       & \downarrow G(u) \\
   F(y)            & \underset{\eta(y)}\to & G(y)
},\;\;\; u\colon x \overset{\sim}\to y\colon C .$$

Note that, while $u$ must be an isomorphism, $\eta(x)$ need not be.


## Reduction to natural transformations

A canonical transformation can be understood as a special kind of natural transformation.  Given $F, G\colon C \to D$ as in the definition, we can restrict $F$ and $G$ to the [[core]] (underlying groupoid) $\tilde{C}$ of $C$ to produce $\tilde{F}, \tilde{G}\colon \tilde{C} \to D$.  Then a canonical transformation from $F$ to $G$ is precisely a natural transformation from $\tilde{F}$ to $\tilde{G}$.

In particular, if $C$ is already a [[groupoid]], then every canonical transformation between functors out of $C$ is natural.


[[!redirects canonical transformations]]