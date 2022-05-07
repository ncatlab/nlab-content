
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

All [[maximal torus|maximal tori]] of a compact Lie group are conjugate by [[inner automorphisms]]. The [[dimension]] of a maximal torus $T$ of a compact Lie group is called the _[[rank of a Lie group|rank]]_ of $G$. 

The [[normalizer]] $N(T)$ of a maximal torus $T$ determines $G$. 

The [[Weyl group]] $W(G)=W(G,T)$ of $G$ with respect to a choice of a maximal torus $T$ is the [[group of automorphisms]] of $T$ which are restrictions of [[inner automorphisms]] of $G$. 

The maximal torus is of [[finite number|finite]] [[index of a subgroup|index]] in its normalizer; the [[quotient group|quotient]] $N(T)/T$ is [[isomorphism|isomorphic]] to $W(G)$. 

The [[cardinality]] of $W(G)$ for a compact [[connected topological space|connected]] $G$, equals the [[Euler characteristic]] of the [[homogeneous space]] $G/T$ ("[[flag variety]]"). 

See also at _[[relation between compact Lie groups and reductive algebraic groups]]_

### Abelian compact Lie groups

\begin{proposition}
\label{MaximalToriOfConnectedCompactLieGroupsAreMaximalAbelianSubgroups}
  The [[maximal torus]] of a [[connected topological space|connected]] [[compact Lie group]] is also the maximal [[abelian group|abelian]] [[subgroup]]. 
\end{proposition}
(e.g. [Salamon 2021, Lem. 6.5](#Salamon21))

In particular:
\begin{proposition}
All connected compact abelian Lie groups are [[tori]], up to [[isomorphism]].
\end{proposition}
([Adams 1982, Thm. 2.19, Cor. 2.20](#Adams82))

\begin{proposition}
  Every [[abelian group|abelian]] [[compact Lie group]] is [[isomorphism|isomorphic]] to the [[direct product group]] of an [[n-torus]] with a [[finite group|finite]] [[abelian group]].
\end{proposition}
  The [[quotient]] of the Lie group $G$ by the [[subgroup]] $G_e$ which is the [[connected component]] of the [[neutral element]] is a [[finite group]] $G/G_0$ and by the assumption that $G$ is compact, this is a finite group. Hence the resulting [[group extension]]
$$
  G_0
  \xhookrightarrow{\;\;}
  G
  \twoheadrightarrow
  G/G_0
$$
is classified by ...
\begin{proof}
  
\end{proof}

### Invariant metric
 {#InvariantMetric}

\begin{prop}\label{CompactLieGroupsAdmitBiinvariantMetrics}
**([[compact Lie groups]] admit [[bi-invariant Riemannian metrics]])**\linebreak
  Every compact Lie group admits a [[bi-invariant Riemannian metric]].
\end{prop}

([Milnor 76, Cor. 1.4](invariant+metric#Milnor76))

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

### Spaces of homomorphisms

* [[nearby homomorphisms from compact Lie groups are conjugate]]


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

Textbook accounts:

* {#Bredon72} [[Glen Bredon]], Section 0.6 of: _[[Introduction to compact transformation groups]]_, Academic Press  1972 ([ISBN 9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1), [pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf))

* {#Adams82} [[Frank Adams]], *Lectures on Lie groups*, University of Chicago Press, 1982 ([ISBN:9780226005300](https://press.uchicago.edu/ucp/books/book/chicago/L/bo3614673.html), [gbooks](https://www.google.com/books/edition/Lectures_on_Lie_Groups/TC7d3ZcqjfsC?hl=en))

In the broader context of [[smooth manifolds]]:

* {#Lee12} [[John Lee]], _Introduction to Smooth Manifolds_, Springer 2012 ([doi:10.1007/978-1-4419-9982-5](https://doi.org/10.1007/978-1-4419-9982-5), [Draft pdf of the 1st edition](https://lost-contact.mit.edu/afs/adrake.org/usr/rkh/Books/books/Introduction%20to%20Smooth%20Manifolds%20-%20J.%20Lee.pdf)) 

Dedicated lecture notes:

* {#Salamon21} [[Dietmar Salamon]], *Notes on compact Lie groups*, 2021 ([pdf](https://people.math.ethz.ch/~salamon/PREPRINTS/liegroup.pdf), [[Salamon_CompactLieGroups.pdf:file]])

Discussion in the context of [[representation theory]]:

* [[Tammo tom Dieck]], [[Theodor Bröcker]], *Representations of compact Lie groups*, Springer 1985 ([doi:10.1007/978-3-662-12918-0](https://link.springer.com/book/10.1007/978-3-662-12918-0))

For more see also the references at *[[equivariant homotopy theory]]*.

[[!redirects compact Lie groups]]
