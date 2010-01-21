# Canonical transformations
* table of contents
{: toc}


## Idea

[[Jim Dolan]] has made the term 'canonical' precise in a way analogous to the way in which the concept of [[natural transformation]] has made the term 'natural' precise.

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


## Warnings

This formalisation is far from accepted, even the regulars on this wiki.  There is nothing wrong with the definition itself; the question is whether anything like this really captures the meaning of 'canonical'.

Furthermore, I may not have properly defined what Dolan has in mind.  In particular, it may be that the functors $C,D$ above should by default be defined only on the core of $C$.  In that case, a canonical transformation is the general non-[[evil]] notion of an operation from an object of $C$ to a morphism of $D$.


## References

* [old newsgroup thread](http://groups.google.com/group/sci.math/browse_frm/thread/9f5ca96dc1a95ada/47a1bb21f6566547) introducing the contrast between 'natural' and 'canonical' (note that 'Robert Scott' is really [[Jim Dolan]])

The notion for higher functors makes a prominent appearance in [[Chris Schommer-Pries]]'s work on [[FQFT]] with defects/[[bi-brane]]s. See _slide 81_ (the penultimate page) here:

* [[Chris Schommer-Pries]], _Topological defects and classifying local topological field theories in low dimension_ ([pdf](http://sites.google.com/site/chrisschommerpriesmath/Home/Slides-MFO-6-11-09.pdf?attredirects=0))


[[!redirects canonical transformations]]