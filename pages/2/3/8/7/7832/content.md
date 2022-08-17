
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


#Contents#
* table of contents
{:toc}

## Idea

Generally, given a [[covering space]] $E \to X$, a *deck transformation* is a [[bundle]]-[[automorphism]], hence a [[continuous map]] $\delta \,\colon\, E \xrightarrow{\;\sim\;} E$ fixing the base $X$.

Assuming without real restriction that $X$ is [[connected topological space|connected]], then $E \to X$ is a [[principal bundle]] with [[discrete space|discrete]] [[fibers]] and the deck transformation determines and is determined by the element $\delta_x \,\colon\, E_x \xrightarrow{\;\sim\;} E_x$ of the [[permutation group]] $Aut(E_x)$ of its [[fiber]] $E_x$ over any fixed [[basepoint]] $x \in X$.

When the [[fundamental theorem of covering spaces]] applies (i.e. when $X$ is [[locally path-connected topological space|locally path-connected]] and [[semi-locally simply-connected topological space]]) then the [[fundamental group]] $\pi_1(X,x)$ has a canonical [[group action|action]] on this fiber, by a [[group homomorphism]] $\pi_1(X,x) \xrightarrow{\;} Aut(E_x)$, and often it is specifically this $\pi_1$-action which is referred to as being *by deck transformations*.

In particular, in the case that $E \to X$ is the [[universal cover]], then $E_x \,\simeq\, \pi_1(X)$ and $E \to X$ is a $\pi_1(X)$-[[principal bundle]] with the [[fundamental group]] $\pi_1(X)$ being identified with the group of deck transformations.



## Definition

+-- {: .num_defn}
###### Definition
A *deck transformation* or *cover automorphism* is an [[automorphism]] of a [[covering space]] relative to the base space.

i.e. if $p\colon E\to X$ is a cover then a cover automorphism $f\in deck(p)=\{f|f\in Aut(E), p\circ f=p\}\subseteq Aut(E)$ is an automorphism of $E$ such that $p$ is invariant under composition with $f$.
=--

## Related concepts

* [[branched cover]]

* [[twisted de Rham cohomology]]

* [[Borel-equivariant rational homotopy theory]]


## References

Any of the references at *[[covering space]]*. 

See also:

* Wikipedia, *[Deck transformation](https://en.wikipedia.org/wiki/Covering_space#Deck_transformation)*

* MathWorld, *[Deck transformation](https://mathworld.wolfram.com/DeckTransformation.html)*



[[!redirects deck transformations]]

[[!redirects cover automorphism]]
[[!redirects cover automorphisms]]
