
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

A real [[Lie group]] is **compact** if its underlying [[topological group]] is a [[compact topological group]].

## Properties

### Maximal tori

All [[maximal torus|maximal tori]] of a compact Lie group are conjugate by [[inner automorphism]]s. The [[dimension]] of a maximal torus $T$ of a compact Lie group is called the _[[rank of a Lie group|rank]]_ of $G$. 

The [[normalizer]] $N(T)$ of a maximal torus $T$ determines $G$. 

The [[Weyl group]] $W(G)=W(G,T)$ of $G$ with respect to a choice of a maximal torus $T$ is the [[group of automorphisms]] of $T$ which are restrictions of [[inner automorphisms]] of $G$. 

The maximal torus is of [[finite number|finite]] [[index of a subgroup|index]] in its normalizer; the [[quotient group|quotient]] $N(T)/T$ is [[isomorphism|isomorphic]] to $W(G)$. 

The [[cardinality]] of $W(G)$ for a compact [[connected topological space|connected]] $G$, equals the [[Euler characteristic]] of the [[homogeneous space]] $G/T$ ("[[flag variety]]"). 

See also at _[[relation between compact Lie groups and reductive algebraic groups]]_

### Smooth actions

+-- {: .num_prop #SmoothActionOfCompactLieGroupOnSmoothManifoldIsProper} 
###### Proposition

Let $X$ be a [[smooth manifold]] and let $G$ be a [[compact Lie group]].
Then every [[smooth function|smooth]] [[action]] of $G$ on $X$ is [[proper action|proper]].

=--

(e.g. [Lee 12, Corollary 21.6](#Lee12))

### Equivariant triangulation theorem
 {#EquivariantTriangulationTheorem}

The _[[equivariant triangulation theorem]]_ ([Illman 78](equivariant+triangulation+theorem#Illman78), [Illman 83](equivariant+triangulation+theorem#Illman83)) says that for $G$ a compact Lie group and $X$ a [[compact topological space|compact]] [[smooth manifold]] equipped with a [[smooth function|smooth]] $G$-[[action]], there exists a $G$-[[equivariant triangulation]] of $X$.

## Examples

* A [[discrete group]] is a compact Lie group iff it is a [[finite group]].

* The [[classical Lie groups]] for *definite* [[inner product space|inner products]] are compact, such as the [[orthogonal groups]], the [[unitary groups]], the [[quaternionic unitary groups]], etc., but not the [[Lorentz group]] etc.


## Applications

### In equivariant homotopy theory
 {#InEquivariantHomotopyTheory}

Compact Lie groups make a somewhat unexpected appearance as [[equivariance groups]] in [[equivariant homotopy theory]], where the compact Lie condition on the [[equivariance group]] is needed in order for (the available proofs of) the [[equivariant Whitehead theorem]] to hold. 

(Namely, the [[equivariant triangulation theorem]] [above](#EquivariantTriangulationTheorem) is used in these proofs to guaratee that [[Cartesian products]] of [[coset spaces]] $G/H$ are themselves [[G-CW-complexes]].)

### In gauge theory

In [[gauge theory]] ([[Yang-Mills theory]]/[[Chern-Simons theory]], ...) ...


## Related concepts

* [[locally compact topological group]]

* [[compact topological group]]

* [[maximal compact subgroup]]

* [[closed subgroup]]

* [[proper Lie groupoid]]

* [[p-compact group]]

* [[twisted ad-equivariant K-theory]]

## References

* {#Lee12} [[John Lee]], _Introduction to Smooth Manifolds_, Springer 2012 ([doi:10.1007/978-1-4419-9982-5](https://doi.org/10.1007/978-1-4419-9982-5), [Draft pdf of the 1st edition](https://lost-contact.mit.edu/afs/adrake.org/usr/rkh/Books/books/Introduction%20to%20Smooth%20Manifolds%20-%20J.%20Lee.pdf)) (Corollary 7.2 on page 147 of the draft).

[[!redirects compact Lie groups]]
