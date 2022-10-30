
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a ([[presymplectic form|pre]])[[symplectic manifold]] $(X,\omega)$, its _quantomorphism group_ is the [[Lie group]] that [[Lie integration|integrates]] the [[Lie algebra|Lie bracket]] inside the [[Poisson algebra]] of $(X, \omega)$.
This is a [[circle group]]-[[central extension]] of the group of [[Hamiltonian symplectomorphisms]]. It extends and generalizes the [[Heisenberg group]] of a [[symplectic vector space]].

(Warning on terminology: A more evident name for the quantomorphism group might seem to be "Poisson group". But this already means something different, see _[[Poisson Lie group]]_.)

### Traditional construction

Over a [[symplectic manifold]] $(X, \omega)$ an explicit construction of the corresponding quantomorphism group is obtained by choosing $(P \to X, \nabla)$ a [[prequantum circle bundle]], regarded with an [[Ehresmann connection]] 1-form $A$ on $P$, and then defining

$$
  QuantomorphismGroup \hookrightarrow Diff(P)
$$

to be the [[subgroup]] of the [[diffeomorphism group]] $P \stackrel{\simeq}{\to} P$ on those [[diffeomorphisms]] that preserve $A$. In other words, the quantomorphism group is the group of equivalences of [[connection on a bundle|bundles with connection]] that need not cover the identity [[diffeomorphism]] on the base manifold $X$.

Notice that the tuple $(P,A)$ is a [[regular contact manifold]] (see the discussion there), and so the quantomorphism group is equivalently that of contactomorphisms $(P,A) \to (P,A)$ of weight 0.

### In higher geometry

This perspective lends itself to a more abstract description: we may regard the [[prequantum circle bundle]] as being modulated by a morphism

$$
  \nabla : X \to \mathbf{B} U(1)_{conn}
$$

in the [[cohesive (∞,1)-topos]] $\mathbf{H} = $ [[Smooth∞Grpd]], with [[domain]] the given symplectic manifold and [[codomain]] the smooth [[moduli stack]] for [[circle n-bundle with connection|circle bundles with connection]]. This in turn may be regarded as an object $\nabla \in \mathbf{H}_{/\mathbf{B}U(1)_{conn}}$ in the [[slice (∞,1)-topos]]. Then the quantomorphism group is the [[automorphism group]]

$$
  QuantomorphismGroup = Aut(\nabla)
$$

formed in $\mathbf{H}_{/\mathbf{B}U(1)_{conn}}$ ([Sch](#Sch)).

From this it is clear what the quantomorphism [[∞-group]] of an [[n-plectic ∞-groupoid]] should be: for

$$
  \nabla : X \to \mathbf{B}^n U(1)_{conn}
$$

the morphism modulating a [[prequantum circle n-bundle]], the corresponding quantomorphism $n$-group is again $Aut(\nabla)$, now formed in $\mathbf{H}_{/\mathbf{B}^n U(1)_{conn}}$

## Properties

### Smooth structure

The quantomorphism group for a [[symplectic manifold]] may naturally be equipped with the structure of a [[group object]] in [[ILH manifolds]] ([Omori](Omori), [Ratiu-Schmid](RatiuSchmid)), as well as in [[convenient manifolds]] ([Vizman, prop. ](#Vizman)). 

### Group extension

[[!include geometric quantization extensions - table]]


## References
 {#References}

### General

Original accounts are

* [[Jean-Marie Souriau]], _Structure des systemes dynamiques_ Dunod, Paris (1970)

  Translated and reprinted as (see section V.18 for the quantomorphism group):

  [[Jean-Marie Souriau]], _Structure of dynamical systems - A symplectic view of physics_, Brikh&#228;user (1997)

* [[Bertram Kostant]], _Quantization and unitary representations_, in _Lectures in modern analysis and applications III_. Lecture Notes in Math. 170 (1970), Springer Verlag, 87&#8212;208

A textbook account is in section II.4 of 

* [[Jean-Luc Brylinski]], _Loop spaces, characteristic classes and geometric quantization_, Birkh&#228;user (1993)

and in 

* Rudolf Schmid, _Infinite-dimensional Lie groups with applications to mathematical physics_

The description in terms of automorphism in the slice $\infty$-topos over the moduli stack of (higher) connections is in section 4.4.17 of

* _[[schreiber:differential cohomology in a cohesive topos]]_
 {#Sch}

and at _[[schreiber:∞-geometric prequantization]]_.




### Smooth manifold structure

The [[ILH manifold|ILH group]] structure on the quantomorphism group is discussed in 

* H. Omori, _Infinite dimensional Lie transformation groups_, Springer lecture notes in mathematics 427 (1974)
 {#Omori}

* T. Ratiu, R. Schmid, _The differentiable structure of three remarkable diffeomorphism groups_, Math. Z.  177 (1981)
 {#RatiuSchmid}

The [[convenient manifold|regular convenient Lie group]] structure is discussed in

* Cornelia Vizman, _Some remarks on the quantomorphism group_ ([[VizmanQuantomorphism.pdf:file]])
 {#Vizman}

A [[metric]]-structure on quantomorphisms groups is discussed in 

* Y. Eliashberg,; L. Polterovich, _Partially ordered groups and geometry of contact transformations_. Geom.Funct.Anal.10(2000),no.6, 1448-1476.




[[!redirects quantomorphism]]
[[!redirects quantomorphisms]]


[[!redirects quantomorphism groups]]

[[!redirects quantomorphism ∞-group]]
[[!redirects quantomorphism ∞-groups]]
[[!redirects quantomorphism infinity-group]]
[[!redirects quantomorphism infinity-groups]]

[[!redirects quantomorphism n-group]]
[[!redirects quantomorphism n-groups]]
