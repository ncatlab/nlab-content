

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

A closed _Jacobi diagram_ is a connected undirected [[graph]] with oriented trivalent vertices and with an embedded oriented [[circle]], regarded modulo cyclic identifications, if any.

Here is a picture of a typical Jacobi diagram:

<center>
<img src="https://ncatlab.org/nlab/files/JacobiDiagram.jpg" width="300">
</center>

Here the internal lines need not form a [[tree]]; the following is also a Jacobi diagram:

<center>
<img src="https://ncatlab.org/nlab/files/OneLoopJacobiDiagram.jpg" width="200">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

If all the [[vertices]] sit on the circle, Jacobi diagrams specialize to [[chord diagrams]].

Half the number of vertices of a Jacobi diagram is called its _order_

$$
  order(\Gamma) \;\coloneqq\; \#Vertices(\Gamma)/2
$$

For example, these are the two closed Jacobi diagrams with 2 vertices (order 1):

<center>
<img src="https://ncatlab.org/nlab/files/JacobiDiagramsOfOrder1.jpg" width="200">
</center>

and these are are the 10 closed Jacobi diagrams with 4 vertices (order 2):

<center>
<img src="https://ncatlab.org/nlab/files/JacobiDiagramsOfOrder2.jpg" width="700">
</center>

> graphics grabbed from [Chmutov-Duzhin-Mostovoy 11](#ChmutovDuzhinMostovoy11)

In applications to [[Vassiliev invariants]] in [[knot theory]], Jacobi diagrams play the role of connected [[Feynman diagrams]] for [[Chern-Simons theory]] in the presence of one [[Wilson line]] (the circle is then the knot/Wilson line).

**Terminology.** Jacobi diagrams have originally been called "chinese character diagrams" ([Bar-Natan 95, Def. 1.8](#BarNatan95)) 
or "[[Feynman diagrams]] for [[Chern-Simons theory]]" ([Kricker-Spence-Aitchison 97](#KrickerSpenceAitchison97))
or "circle diagrams" ([Kneissler 97](#Kneissler97))
or "round diagrams" ([Willerton 99](#Willerton99)).
The term "Jacobi diagram" ([Chmutov-Duzhin-Mostovoy 11, Chapter 5](#ChmutovDuzhinMostovoy11), [Jackson-Moffat 19, Section 13](#JacksonMoffat19)) alludes to the [[Jacobi identity]] -- here also called the [[STU relation]] -- via the fact that these diagrams are naturally labelled by a [[Lie algebra]] equipped with a [[Lie algebra representation]] (which is really just the [[interaction]]-aspect of their interpretation as [[Chern-Simons theory]] [[Feynman diagrams]]...).

## Definition

### Jacobi diagrams

(...)

### STU-relations and weight systems
 {#STURelationsAndWeightSystems}

For $R \in $ [[CRing]] a [[commutative ring]], let $R\langle \mathcal{D}^t \rangle$ denote the $R$-[[linear span]] of the [[set]] $\mathcal{D}^t$ of [[Jacobi diagrams]]. 

Then one traditionally writes

\[
  \label{QuotientSpaceBySTU}
  \mathcal{A}^t 
    \;\coloneqq\;
  R\langle \mathcal{D}^c \rangle/STU 
\]

for the [[quotient spaces]] of the [[linear span]] of [[Jacobi diagrams]] by the [[STU relations]]:

<center>
<img src="https://ncatlab.org/nlab/files/STU-relation.jpg" width="400">
</center>

Hence:

<center>
<img src="https://ncatlab.org/nlab/files/JacobiDiagramsModuloSTURelationsII.jpg" width="700">
</center>

A [[linear function]]

$$
  w \;\colon\; \mathcal{A}^t \longrightarrow R
  \,,
$$

-- hence a plain $R$-valued [[function]] on the [[set]] $\mathcal{D}^t$ of [[Jacobi diagrams]] which is [[invariant]] under the [[STU relations]] --

is called a _[[framed weight system]]_. See there for more.


> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

## Properties

### Relation to chord diagrams

[[chord diagrams modulo 4T are Jacobi diagrams modulo STU]]:


<center>
<img src="https://ncatlab.org/nlab/files/ChordDiagModulo4TAreJAcobiDiagModuloSTU.jpg" width="840">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

### Relation to Adams operations

On the [[vector space]] $\mathcal{A}$ of [[Jacobi diagrams]] [[quotient vector space|modulo]] [[STU-relations]] ([[chord diagrams modulo 4T are Jacobi diagrams modulo STU|equivalently]] [[chord diagrams]] [[quotient vector space|modulo]] [[4T relations]])  there is a system of [[linear maps]] (for $q \in \mathbb{Z}$, $q \neq 0$)

$$
  \psi^q
  \;\colon\;
  \mathcal{A}
  \longrightarrow
  \mathcal{A}
$$

which respect the [[coalgebra]] [[mathematical structure|structure]] and satisfy

$$
  \psi^{q_2} \circ \psi^q_1
  \;=\;
  \psi^{q_1 \cdot q_2}
$$

and as such are (dually) analogous to the [[Adams operations]] on [[topological K-theory]].

([Bar-Natan 95, Def. 3.11 & Theorem 7](#BarNatan95))

In fact, when evaluated in [[Lie algebra weight systems]] $w_{\mathbf{N}}$ and under the identification (see [here](equivariant+K-theory#RelationToRepresentationTheory)) of the [[representation ring]] of a [[compact Lie group]] $G$ with the $G$-[[equivariant K-theory]] of the point, these Adams operations on [[Jacobi diagrams]] correspond to the [[Adams operations]] on [[equivariant K-theory]]:


$$
  w_{\mathbf{N}}(\psi^q D)
  \;=\;
  w_{\psi^q \mathbf{N}}(D)
  \,.
$$

([Bar-Natan 95, Exc. 6.24](#BarNatan95)
)

For more see at _[[Adams operation on Jacobi diagrams]]_.

## Related concepts

[[!include chord diagrams and weight systems -- table]]


## References

### General

Original articles

* {#BarNatan95} [[Dror Bar-Natan]], _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

* {#KrickerSpenceAitchison97} A. Kricker, B. Spence and I. Aitchison, _Cabling the Vassiliev invariants_, J. Knot Theory Ramifications 6 (1997) 327–358

* {#Kneissler97} [[Jan Kneissler]], _The number of primitive Vassiliev invariants up to degree 12_ ([arXiv:q-alg/9706022](https://arxiv.org/abs/q-alg/9706022))

* {#Willerton99} [[Simon Willerton]], _The Kontsevich integral and algebraic structures on the space of diagrams_ in: Knots in Hellas ’98. Series on Knots and Everything, vol. 24, World Scientific, 2000, 530–546 ([arXiv:math/9909151](https://arxiv.org/abs/math/9909151))


Lecture notes:

* {#BarNatanStoimenow97} [[Dror Bar-Natan]], [[Alexander Stoimenow]]: _The Fundamental Theorem of Vassiliev Invariants_, in: *Geometry and Physics*, Lecture Notes in Pure and Applied Mathematics **184** Marcel Dekker Inc. (1996) &lbrack;[arXiv:q-alg/9702009](https://arxiv.org/abs/q-alg/9702009), [ISBN:0-8247-9791-4](https://users-math.au.dk/swann/Aarhus-proceedings-1995/index.html)&rbrack;


Textbook accounts

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], Section 5 of:  _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))

* {#JacksonMoffat19} [[David Jackson]], [[Iain Moffat]], Section 13 of: _An Introduction to Quantum and Vassiliev Knot Invariants_, Springer 2019 ([doi:10.1007/978-3-030-05213-3](https://link.springer.com/book/10.1007/978-3-030-05213-3))


[[!include weight systems on chord diagrams in physics]]

[[!redirects Jacobi diagrams]]

