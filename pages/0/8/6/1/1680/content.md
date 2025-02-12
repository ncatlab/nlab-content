+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $A$ an [[abelian group]], the _Eilenberg-Mac Lane spectrum_ $H A$ is the [[spectrum]] that [[Brown representability theorem|represents]] the [[ordinary cohomology|ordinary]] [[cohomology theory]]/[[ordinary homology]]  with [[coefficients]] in $A$.

By default $A$ is taken to be the [[integers]] and hence "the Eilenberg-MacLane spectrum" is $H \mathbb{Z}$, representing [[integral cohomology]].

## Definition


## Incarnations


### As symmetric/orthogonal spectra
 {#AsSymmetricSpectra}

We discuss the model of Eilenberg-MacLane spectra as [[symmetric spectra]] and [[orthogonal spectra]]. To that end, notice the following model for [[Eilenberg-MacLane spaces]].

+-- {: .num_defn #ReducedALinearizationOfnSphere}
###### Definition

For $A$ an [[abelian group]] and $n \in \mathbb{N}$, the **reduced $A$-linearization** $A[S^n]_\ast$ of the [[n-sphere]] $S^n$ is the [[topological space]], whose underlying set is the [[quotient]] 

$$
  \underset{k \in \mathbb{N}}{\sqcup}
   A^k \times (S^n)^k
  \longrightarrow
  A[S^n]_\ast
$$

of the [[tensor product]]  with $A$ of the [[free abelian group]] on the underlying set of $S^n$, by the relation that identifies every [[formal linear combination]] of the (any fixed) basepoint of $S^n$ with 0. The [[topological space|topology]] is the induced [[quotient topology]] (of the [[disjoint union]] of [[product topological spaces]], where $A$ is equipped with the [[discrete topology]]).

=--

([Aguilar-Gitler-Prieto 02, def. 6.4.20](Eilenberg-MacLane+space#AguilarGitlerPrieto02))


+-- {: .num_prop #ReducedALinearizationOfnSphereIsEMSpace}
###### Proposition

For $A$ a [[countable set|countable]] [[abelian group]], then the reduced $A$-linearization $A[S^n]_\ast$ (def. \ref{ReducedALinearizationOfnSphere}) is an [[Eilenberg-MacLane space]], in that its [[homotopy groups]] are

$$
  \pi_q(A[S^n]_\ast)
   \simeq
   \left\{
     \array{
       A & if \; q = n
       \\
       \ast & otherwise
     }
   \right.
$$

(in particular for $n \geq 1$ then there is a unique connected component and hence we need not specify a basepoint for the homotopy group).


=--

([Aguilar-Gitler-Prieto 02, corollary 6.4.23](Eilenberg-MacLane+space#AguilarGitlerPrieto02))

+-- {: .num_defn}
###### Definition

For $A$ a [[countable set|countable]] [[abelian group]], then the [[orthogonal spectrum]] incarnation of the **[[Eilenberg-MacLane spectrum]]** $H A$ is the [[orthogonal spectrum]] with

* components spaces

  $$
    (H A)_V \coloneqq A[S^V]_\ast
  $$

  being the reduced $A$-linearization (def. \ref{ReducedALinearizationOfnSphere}) of the [[representation sphere]] $S^V$;

  hence for $V = \mathbb{R}^n$ then

  $$
    (H A)_n = A[S^n]_\ast
  $$

* $O(V)$-[[action]] on $A[S^V]_\ast$ induced from the canonical $O(V)$-action on $S^V$ ([[representation sphere]]);

* structure maps 

  $$
    \sigma_{V,W}
      \;\colon\;
    (H A)_V \wedge S^W 
      \longrightarrow
    (H A)_{V\oplus W}
  $$

  hence

  $$
    A[S^V] \wedge S^W
      \longrightarrow
    A[S^{V \oplus W}]
  $$    

  given by

  $$
    \left(
    \left(
       \underset{i}{\sum} a_i x_i
    \right),
    y
    \right)
      \mapsto
    \underset{i}{\sum} a_i (x_i, y)
    \,.
  $$

The incarnation of $H A$ as a [[symmetric spectrum]] is the same, with the group action of $O(n)$ replaced by the [[subgroup]] action of the [[symmetric group]] $\Sigma(n) \hookrightarrow O(n)$.

If $R$ is a [[commutative ring]], then the Eilenberg-MacLane spectrum $H R$ becomes a commutative [[orthogonal ring spectrum]] (or [[symmetric ring spectrum]], respectively) by 

1. taking the multiplication

   $$
     (H R)_{V_1} \wedge (H R)_{V_2}
       =
     R[S^{V_1}]_\ast \wedge R[S^{V_2}]_\ast 
       \longrightarrow
     R[S^{V_1 \oplus V_2}]
      =
     (H R)_{V_1 \oplus V_2}
   $$

   to be given by

   $$
     \left(
     \left(
        \underset{i}{\sum} a_i x_i
     \right)
     ,
     \left(
       \underset{j}{\sum} b_j y_j
     \right)
     \right)
      \;\mapsto\;
     \underset{i,j}{\sum}
      (a_i \cdot b_j)(x_i, y_j)
   $$ 

1. taking the unit maps

   $$
     S^V 
       \longrightarrow
     A[S^V]_\ast = (H R)_V 
   $$

   to be given by the canonical inclusion of generators

   $$
     x \mapsto 1 x
     \,.
   $$

=--

([Schwede 12, example I.1.14](#Schwede12), [Schwede 15, V, costruction 3.21](#Schwede15))

### As symmetric monoidal $\infty$-groupoids

Under the identification of [[connective spectra]] with "[[abelian infinity-groups]]" the Eilenberg-MacLane spectrum $H A$ simply _is_ the group $A$.

Here the set $A$ is regarded as a [[discrete category|discrete groupoid]] (one object per integer, no nontrivial morphisms) whose symmetric monoidal structure is that given by the additive group structure on the integers.

Accordingly, the infinite tower of [[suspensions]] induced by this is the sequence of [[∞-groupoids]]

$$
  A, \mathbf{B} A, \mathbf{B}^2 A, \mathbf{B}^3 A, \cdots
$$

that in this case happen to be [[strict omega-groupoids]]. The [[strict omega-groupoid]] $\mathbf{B}^n A$ has only [[identity]] $k$-morphisms for all $k$, except for $k = n$, where $\mathrm{Mor}_n(\mathbf{B}^n A) = A$ are the endomorphisms of the unique identity $(n-1)$-morphism. 

The [[strict ∞-groupoid]] $\mathbf{B}^n A$ is the one given under the [[Dold-Kan correspondence]] by the [[crossed complex]] of groupoids that is trivial everywhere and has the group $\mathbb{Z}$ in degree $n$.

$$
  \begin{aligned}
    [\mathbf{B}^n A] &=
     (  \cdots \to [\mathbf{B}^n A]_{n+1} \to [\mathbf{B}^n A]_{n} \to 
     [\mathbf{B}^n A]_{n-1} \cdots \to [\mathbf{B}^n A]_{1} \stackrel{\to}{\to} [\mathbf{B}^n A]_{0})
      \\ &=
    (  \cdots \to {*} \to A \to 
    {*} \cdots \to {*} \stackrel{\to}{\to} {*})
  \end{aligned}
  \,.
$$

Under the  [[Quillen equivalence]]

$$
  |-| : \infty Grpds \to Top
$$

between [[infinity-groupoids]] and [[topological spaces]] (see _[[homotopy hypothesis]]_) this sequence of suspensions of $A$ maps to the sequence of [[Eilenberg–Mac Lane spaces]]

$$
  |\mathbf{B}^n A|
  \simeq
  K(A, n)
  \,.
$$


## Properties


### Chromatic filtration

[[!include chromatic tower examples - table]]


### Ordinary homology spectra split

**[[ordinary homology spectra split]]**:
For $S$ any [[spectrum]] and $H A$ an Eilenberg-MacLane spectrum,
then the [[smash product]] $S\wedge H A$ (the $A$-[[ordinary homology]] spectrum)
is non-canonically equivalent to a product of EM-spectra (hence a [[wedge sum]] of EM-spectra in the finite case).

### Fibrant-cofibrant models

[MO comment](http://mathoverflow.net/a/218069/381)

 
## Related concepts

* [[generalized Eilenberg-MacLane spectrum]]

* [[Moore spectrum]]

* [[cohomology theory]], [[ordinary cohomology]]


## References

Textbook accounts include

* {#Adams74} [[Frank Adams]], part III, section 2 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Kochmann96} [[Stanley Kochmann]], section 3.5 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

Lecture notes include

* {#May} [[Peter May]], chapter 22 of _A concise course in algebraic topology_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/maybook.pdf))

* {#Rognes12} [[John Rognes]], section 3.2 3.4 of _The Adams spectral sequence_, 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

As [[symmetric spectra]]

* {#Schwede12} [[Stefan Schwede]], Example I.1.14 in _Symmetric spectra_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec.pdf))

* [[John Greenlees]], example 3.6, example 4.16 in _Spectra for commutative algebraists_ ([pdf](http://www.math.uic.edu/~bshipley/greenlees.SpectraMSRI.pdf))

as [[orthogonal spectra]]:

* {#Schwede15} [[Stefan Schwede]], construction V 3.21 in _[[Global homotopy theory]]_, 2015


[[!redirects Eilenberg-MacLane spectrum]]
[[!redirects Eilenberg--MacLane spectrum]]
[[!redirects Eilenberg--Mac Lane spectrum]]
[[!redirects Eilenberg–MacLane spectrum]]
[[!redirects Eilenberg–Mac Lane spectrum]]
[[!redirects Eilenberg-MacLane spectra]]
[[!redirects Eilenberg-Mac Lane spectra]]
[[!redirects Eilenberg--MacLane spectra]]
[[!redirects Eilenberg--Mac Lane spectra]]
[[!redirects Eilenberg–MacLane spectra]]
[[!redirects Eilenberg–Mac Lane spectra]]

[[!redirects HR]]

[[!redirects HA]]
[[!redirects HC]]
[[!redirects HZ]]
