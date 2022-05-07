[[!redirects generalized Cauchy real numbers]]
[[!redirects generalised Cauchy real number]]
[[!redirects generalised Cauchy real numbers]]

[[!redirects Cauchy complete real number]]
[[!redirects Cauchy complete real numbers]]
[[!redirects Cauchy-complete real number]]
[[!redirects Cauchy-complete real numbers]]

[[!redirects Cauchy net real number]]
[[!redirects Cauchy net real numbers]]
[[!redirects Cauchy-net real number]]
[[!redirects Cauchy-net real numbers]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##

The Cauchy completion of the rational numbers, in the sense that all [[Cauchy nets]] in the rational numbers [[converge]]. 

## Definition ##

Let $\mathbb{Q}$ be the [[rational numbers]] and let 

$$\mathbb{Q}_{+} \coloneqq \{x \in \mathbb{Q} \vert 0 \lt x\}$$ 

be the set of positive rational numbers. Let $I$ be a [[directed set]] and

$$C(I, \mathbb{Q}) \coloneqq \{x \in \mathbb{Q}^I \vert \forall \epsilon \in \mathbb{Q}_{+}. \exists N \in I. \forall i \in I. \forall j \in I. (i \geq N) \wedge (j \geq N) \wedge (\vert x_i - x_j \vert \lt \epsilon)\}$$

is the set of all [[Cauchy nets]] with index set $I$ and values in $\mathbb{Q}$. Let 

$$CauchyNetsIn(\mathbb{Q}) \coloneqq \bigcup_{I \in Ob(DirectedSet_\mathcal{U})} C(I, \mathbb{Q})$$ 

be the (large) set of all Cauchy nets in $\mathbb{Q}$ in a [[universe]] $\mathcal{U}$, where $DirectedSet_\mathcal{U}$ is the [[category]] of all directed sets in $\mathcal{U}$. 

Let the [[relation]] $\equiv_{I, J}$ in the Cartesian product $C(I, \mathbb{Q}) \times C(J, \mathbb{Q})$ for directed sets $I$ and $J$ be defined as 

$$a \equiv_{I, J} b \coloneqq \forall \epsilon \in \mathbb{Q}_{+}, \exists M \in I. \forall i \in I. \exists N \in J. \forall j \in J. (i \geq M) \wedge (j \geq N) \wedge (\vert a_i - b_j \vert \lt \epsilon)$$

Let a *generalized Cauchy algebra* be defined as a [[set]] $A$ with a function $\iota \in {A}^{CauchyNetsIn(\mathbb{Q})}$ such that 

$$\forall I \in Ob(DirectedSet_\mathcal{U}). \forall J \in Ob(DirectedSet_\mathcal{U}). \forall a \in C(I, \mathbb{Q}). \forall b \in C(J, \mathbb{Q}). (a \equiv_{I, J} b) \implies (\iota(a) = \iota(b))$$

A *generalized Cauchy algebra homomorphism* is a function $f:B^A$ between Cauchy algebras $A$ and $B$ such that 

$$\forall a \in C(\mathbb{Q}). f(\iota_A(a)) = \iota_B(a)$$

The *category of generalized Cauchy algebras* is the category $GCAlg$ whose objects $Ob(GCAlg)$ are generalized Cauchy algebras and whose morphisms $Mor(GCAlg)$ are generalized Cauchy algebra homomorphisms. The set of **generalized Cauchy real numbers**, denoted $\mathbb{R}$, is defined as the initial object in the category of Cauchy algebras. 

## See also ##

* [[HoTT book real numbers]]
* [[Cauchy real numbers]]