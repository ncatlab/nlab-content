
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
 {#InHigherGeometry}

This perspective lends itself to a more abstract description in [[higher differential geometry]]: we may regard the [[prequantum circle bundle]] as being modulated by a morphism

$$
  \nabla : X \to \mathbf{B} U(1)_{conn}
$$

in the [[cohesive (∞,1)-topos]] $\mathbf{H} = $ [[Smooth∞Grpd]], with [[domain]] the given symplectic manifold and [[codomain]] the smooth [[moduli stack]] for [[circle n-bundle with connection|circle bundles with connection]]. This in turn may be regarded as an object $\nabla \in \mathbf{H}_{/\mathbf{B}U(1)_{conn}}$ in the [[slice (∞,1)-topos]]. Then the quantomorphism group is the [[automorphism group]]

$$
  \mathbf{QuantMorph}(X.\nabla) \coloneqq 
  \underset{\mathbf{B}U(1)_{conn}}{\prod} \mathbf{Aut}(\nabla)
$$

in $\mathbf{H}$, or rather its [[differential concretification]] ([FRS 13](#FRS13)).

From this it is clear what the quantomorphism [[∞-group]] of an [[n-plectic ∞-groupoid]] should be: for

$$
  \nabla : X \to \mathbf{B}^n U(1)_{conn}
$$

the morphism modulating a [[prequantum circle n-bundle]], the corresponding quantomorphism $n$-group is again $Aut(\nabla)$, now formed in $\mathbf{H}_{/\mathbf{B}^n U(1)_{conn}}$

## Properties

### Smooth structure

The quantomorphism group for a [[symplectic manifold]] may naturally be equipped with the structure of a [[group object]] in [[ILH manifolds]] ([Omori](Omori), [Ratiu-Schmid](RatiuSchmid)), as well as in [[convenient manifolds]] ([Vizman, prop. ](#Vizman)). 

### Group extension

+-- {: .num_prop}
###### Proposition

For $(X,\omega)$ a [[connected topological space|connected]] [[symplectic manifold]] there is a [[central extension of groups]]

$$
  1 \to U(1) \to QuantomorphismGroup(X,\omega) \to HamiltonianSymplectomorphisms(X,\omega) \to 1
  \,.
$$

=--

This is due to ([Kostant](#Kostant)). It appears also ([Brylinski, prop. 2.4.5](#Brylinski)). 

[[!include geometric quantization extensions - table]]

## Examples

### Covering an affine symplectic group
 {#CoveringAnAffineSymplecticGroup}

Given a [[symplectic vector space]] $(V,\omega)$ one may consider the restriction of its [[quantomorphism group]] to the [[affine symplectic group]] $ASp(V,\omega)$ ([Robbin-Salamon 93, corollary 9.3](#RobbinSalamon93))

$$
  \array{
     ESp(V,\omega) &\hookrightarrow& QuantMorph(V,\omega)
     \\
     \downarrow && \downarrow
     \\
     ASp(V,\omega)
     &\hookrightarrow&
     HamSympl(V,\omega)
  }
$$

Sometimes (e.g. [Robbin-Salamon 93, p. 30](#RobbinSalamon93)) this $ESp(V,\omega)$ is called the _extended symplectic group_, but maybe to be more specific one should at the very least say "[[extended affine symplectic group]]" or "extended inhomogeneous symplectic group" ([ARZ 06, prop. V.1](#ARZ06)). 

Notice that the further restriction to $V$ regarded as the [[translation group]] over itself is the [[Heisenberg group]] $Heis(V,\omega)$

$$
  \array{
     Heis(V,\omega)
     &\hookrightarrow&
     ESp(V,\omega) &\hookrightarrow& QuantMorph(V,\omega)
     \\
     \downarrow && \downarrow && \downarrow
     \\
     V
     &\hookrightarrow&
     ASp(V,\omega)
     &\hookrightarrow&
     HamSympl(V,\omega)
  }
$$

The group $ESp(V,\omega)$ is that of those [[quantomorphisms]] which come from [[Hamiltonians]] that are [[polynomials]] of degree-2 in canonical [[coordinates]] on $V$. Those elements covering elements in the [[symplectic group]] instead of the [[affine symplectic group]] come from homogeneous quadratic Hamiltonians. (e.g. [Robbin-Salamon 93, prop. 10.1](#RobbinSalamon93)). In fact $ESp$ is the [[semidirect product]] of the [[metaplectic group]] $Mp(V,\omega)$ with the [[Heisenberg group]] ([ARZ 06, prop. V.1](#ARZ06))

$$
  ESp(V,\omega) \simeq Heis(V,\omega) \rtimes Mp(V,\omega)
  \,.
$$



## Related concepts

* [[conserved current]]

* [[Hamiltonian action]], [[classical anomaly]]

[[!include slice automorphism groups in higher prequantum geometry - table]]


[[!include higher Atiyah groupoid - table]]




## References
 {#References}

### General

Original accounts are

* [[Jean-Marie Souriau]], _Structure des systemes dynamiques_ Dunod, Paris (1970)

  Translated and reprinted as (see section V.18 for the quantomorphism group):

  [[Jean-Marie Souriau]], _Structure of dynamical systems - A symplectic view of physics_, Brikh&#228;user (1997)

* {#Kostant} [[Bertram Kostant]], _Quantization and unitary representations_, in _Lectures in modern analysis and applications III_. Lecture Notes in Math. 170 (1970), Springer Verlag, 87&#8212;208
 

A textbook account is in section II.4 of 

* [[Jean-Luc Brylinski]], _Loop spaces, characteristic classes and geometric quantization_, Birkh&#228;user (1993)

and in 

* Rudolf Schmid, _Infinite-dimensional Lie groups with applications to mathematical physics_

The description in terms of automorphism in the slice $\infty$-topos over the moduli stack of (higher) connections is in

* {#FRS13} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_ ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))

and in section 4.4.17 of

* {#Sch} _[[schreiber:differential cohomology in a cohesive topos]]_
 



### Smooth manifold structure

The [[ILH manifold|ILH group]] structure on the quantomorphism group is discussed in 

* {#Omori} H. Omori, _Infinite dimensional Lie transformation groups_, Springer lecture notes in mathematics 427 (1974)
 

* {#RatiuSchmid} T. Ratiu, R. Schmid, _The differentiable structure of three remarkable diffeomorphism groups_, Math. Z.  177 (1981)
 

The [[convenient manifold|regular convenient Lie group]] structure is discussed in

* {#Vizman} Cornelia Vizman, _Some remarks on the quantomorphism group_ ([[VizmanQuantomorphism.pdf:file]])
 

A [[metric]]-structure on quantomorphisms groups is discussed in 

* Y. Eliashberg,; L. Polterovich, _Partially ordered groups and geometry of contact transformations_. Geom.Funct.Anal.10(2000),no.6, 1448-1476.

### Examples

The quantomorphisms over elements of the [[symplectic group]] of a [[symplectic vector space]] are discussed in 

* {#Segal63} [[Irving Segal]], _Transforms for operators and symplectic automorphisms over a locally compact abelian group_, Math. Scand. 13 (1963) 31-43 www.mscand.dk/article/download/10686/8707


* {#RobbinSalamon93} [[Joel Robbin]],  [[Dietmar Salamon]], _Feynman path integrals on phase space and the metaplectic representation_ in [[Dietmar Salamon]] (ed.), _Symplectic Geometry_, LMS Lecture Note series 192 (1993) ([[RobbinSalamonMetaplectic.pdf:file]])

* {#ARZ06} [[Sergio Albeverio]], J. Rezende and J.-C. Zambrini, _Probability and Quantum Symmetries. II. The Theorem of Noether in quantum mechanics_, Journal of Mathematical Physics 47, 062107 (2006) ([pdf](http://gfm.cii.fc.ul.pt/people/jczambrini/JMathPhys-47-062107.pdf))


[[!redirects quantomorphism]]
[[!redirects quantomorphisms]]


[[!redirects quantomorphism groups]]

[[!redirects quantomorphism ∞-group]]
[[!redirects quantomorphism ∞-groups]]
[[!redirects quantomorphism infinity-group]]
[[!redirects quantomorphism infinity-groups]]

[[!redirects quantomorphism n-group]]
[[!redirects quantomorphism n-groups]]