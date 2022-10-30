
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

String field theory is supposed to be something like a  [[quantum field theory]] which is the [[second quantization]] of the [[string]] in [[string theory]].

Recall that [[string theory|perturbative string theory]] is a higher dimensional version of the Feynman perturbation series in [[quantum field theory]]. This Feynman perturbation series may be understood as computing the path integral over the Lagrangian of the given quantum field theory. _String field theory_ is the attempt to identify this Lagrangian description corresponding to the string perturbation series.

So string field theory is the attempt to complete the following analogy:

Feynman perturbation series : QFT Lagrangian  :: String perturbation theory : String field theory .

### Motivation

The original hope was that string field theory would be a way to embed the string perturbation series prescription into a more coherent non-perturbative framework. 

### Achievements

The most detailed insight that has come out of the study of string field theory is the full understanding of the role of the "tachyon" field in bosonic perturbative string theory. In the bosonic version of the theory one of the excitations of the string is a quantum that appears to have imaginary mass. Such "tachyonic" quanta appear in ordinary field theory when the perturbation series is developed around an extremum of the QFT action functional that is not a local minimum, but a local maximum: it indicates that the  classical configuration around which the perturbation series computes the quantum corrections is dynamically unstable and time evolution will tend to evolve it to the next local minimum. In the perturbative quantum description the movement to the next local minimum manifests itself in the _condensation_ (as in [[Bose-Einstein condensation]]) of the tachyon field. This is called _tachyon condensation_.

Shortly after its conception it was suspected that the tachyon that appears in the perturbation theory of the bosonic string is similarly an indication that the bosonic string's perturbation series has to be understood as being a perturbation about a local maximum of some action functional. String field theory aimed to provide that notion of action functional. And indeed, in bosonic string field theory one has a kind of higher action functional and may compute the "tachyon potential" that it implies. It indeed has a local maximum at the point about which the ordinary bosonic string perturbation series is a perturbative expansion, while a local minimum is foun nearby. 

[[Ashoke Sen]] conjectured the statement -- now known as _[[Sen's conjecture]]_ -- that the depth of this tachyon potential, i.e. the energy density difference between this local maximum and this local minimum corresponds precisely to the energy density of the space-filling D25-[[brane]] that is seen in [[perturbative string theory]]. This would mean that the condensation of the bosonic string's tachyon corresponds to the decay of the unstable space-filling D25 brane. 

The detailed quantitative confirmation of Sen's conjecture has been one of the main successes of string field theory. In the course of this a detailed algebraic description of the "true bosonic string vacuum", i.e. of the theory at that local tachyon potential minimum has been found. However, the algebraic expressions involved tend to be hard to handle in their complexity.

### Shortcomings

The shortcoming of the current development of string field theory can probably be summarized as follows:

* it has been studied as a theory of a _classical_ action functional. Little is known about the true quantum effects of the string field theory action functional.

* the best understanding exists for bosonic open string field theory, while closed and supersymmetric string field theory has remained much less accessible.

### In terms of higher category theory

Closed string field theory is governed by an [[L-infinity algebra]] of interactions, open string field theory by an [[A-infinity algebra]] and open-closed string field theory by a mixture of both: an [[open-closed homotopy algebra]].


## Definition

So far string field theory is defined in terms of an [[action functional]]. So, strictly speaking, it is defined as a [[classical field theory]]. The corresponding [[BV-BRST formalism|quantum master action]] is known, but apart from that not much detail about the [[quantization]] of this action has been considered in the literature.


### The interaction terms

The unrestricted [[configuration space]] of string field theory is the subcomplex of the [[BRST complex]] of the closed ([[superstring|super]]-)[[string]], regarded as a $\mathbb{N}$-[[graded vector space]] with respect to the ghost number grading, on those elements $\Psi$ that satisfy

1. $(b_0 - \bar b_0) \Psi = 0$;

1. $(L_0 - \bar L_0) \Psi = 0$ ("level matching condition"),


We shall write $\mathfrak{g}$ for this graded vector space. See ([Markl, section 1](#Markl))

This is equipped for each $k \in \mathbb{N}$ with a $k$-ary operation

$$
  [-,\cdots,-]_k : \mathfrak{g}^{\otimes k} \to \mathfrak{g}
$$

given by the [[correlator|(k+1)-point function]] of the string (the amplitude for $k$ closed strings coming in and merging into a single outgoing string). For $k = 1$ this is the [[BRST complex|BRST operator]]

$$
  [-]_1 = d_{BRST}
  \,.
$$

These operations are graded-symmetric: for all $\{\Psi_j\}$ of homogeneous degree $deg \Psi_j$ and for all $0 \leq i \lt k$ we have

\[
  \label{GradedSymmetrykBracket}
  [\Psi_1 , \cdots, \Psi_i, \Psi_{i+1}, \cdots, \Psi_k]_k
  =
  (-1)^{(deg \Psi_i)(deg \Psi_{i+1})}
  [\Psi_1 , \cdots, \Psi_{i+1}, \Psi_{i}, \cdots, \Psi_k]_k .
\]

([Zwiebach, (4.4)](#Zwiebach)).

Moreover, there is a bilinear [[inner product]]

$$
  \langle -,- \rangle : \mathfrak{g} \otimes \mathfrak{g} \to \mathbb{C}
$$

coming from the [[Hilbert space]] inner product of string states ([Zwiebach (2.60)](#Zwiebach)). This is non-degenerate on elements $\Psi$ which are annihilated by the [[BRST complex|ghost]] operator 

$$
  b_0^- := b_0 - \bar b_0
$$

in that for all $A \in \mathfrak{g}$ with  $b_0^- A = 0$ we have

\[
  \label{NonDegeneracyOfInnerProduct}
  (\forall B \in \mathfrak{g} \,:\,
  \langle A,B\rangle = 0)
  \Rightarrow
  A = 0  
  \,.
\]

This is ([Zwiebach, (2.61)](#Zwiebach)).


The inner product satisfies for all $\Psi_1, \Psi_2$ of homogeneous degree the relation

\[
  \label{GradedSymmetryBilinearPairing}
  \langle \Psi_1 , \psi_2 \rangle
  = 
  (-1)^{(deg \Psi_1 + 1) (deg \Psi_2 + 1)}
  \langle \Psi_2, \Psi_1 \rangle
\]

([Zwiebach, (2.50)](#Zwiebach)).


Moreover, it is non-vanishing only on pairs of elements of total degree 5. ([Zwiebach, (2.31)(2.44)](#Zwiebach)).

From this one constructs the $(n+1)$-point functions

\[
  \label{CorrelationFunctions}
  \{ \Psi_0, \Psi_1, \cdots, \Psi_k \}
  :=
  \langle \Psi_0, [\Psi_1, \cdots, \Psi_k]_k \rangle
  \,.
\]

These are still graded-symmetric in all arguments: for all $\{\Psi_j\}$ of homogeneous degree $deg \Psi_j$ and all $0 \leq i \lt k$ we have

\[
  \label{GradedSymmetrykPointFunction}
  \{\Psi_0, \cdots, \Psi_i, \Psi_{i+1}, \cdots, \Psi_k\}
  = 
  (-1)^{(deg \Psi_i)(deg \Psi_{i+1})}
  \{\Psi_0, \cdots, \Psi_{i+1}, \Psi_{i}, \cdots, \Psi_k\}
  \,.
\]

([Zwiebach, (4.36)](#Zwiebach)).


### The action functional

+-- {: .num_defn #LabelConfigurationSpace}
###### Definition

The proper [[configuration space]] of string field theory is the sub-complex of the [[BRST complex]] of the closed ([[superstring|super]]-)[[string]] on those elements $\Psi$ for which

1. $(b_0 - \bar b_0) \vert\Psi\rangle = 0$;

1. $(L_0 - \bar L_0) \vert \Psi \rangle = 0$ ("level matching condition");

1. $\vert \Psi \rangle^\dagger = - (\langle \Psi \vert)$ ("reality");

1. $\vert \Psi\rangle$ is Grassmann even (...define...)

1. $ghostnumber \vert \Psi \rangle = 2$ (...define...)

=--

This is ([Zwiebach, (3.9)](#Zwiebach))


The _[[action functional]]_ of closed string field theory is 

$$
  S : \Psi 
   \mapsto 
   \sum_{k = 1}^\infty
   \frac{1}{(k+1)!}
   \langle \Psi, [\Psi, \cdots, \Psi]_k\rangle
  \,.
$$

([Zwiebach, (4.41)](#Zwiebach))


Since $[-]_1 = d_{BRST}$ is the [[BRST complex|BRST operator]] this starts out as

$$
  S : \Psi 
  = 
  \frac{1}{2}\langle \Psi , d_{BRST} \Psi \rangle
  + 
  \frac{1}{3} \langle \Psi, [\Psi, \Psi]_2\rangle
  + 
  \cdots
  \,.
$$

### As an $\infty$-Chern-Simons theory

The above action functional for closed string field theory turns out to have a general abstract meaning in [[higher category theory]]/[[homotopy theory]].

+-- {: .num_prop}
###### Proposition

The string [[BRST complex]] equipped with its $k$-ary interaction genus-0 interaction vertices  

$$
  (\mathfrak{g}, \{[-,\cdots,-]_k\})
$$ 

is an [[L-∞ algebra]].

=--

This is ([Zwiebach, (4.12)](#Zwiebach)). For more details on the $L_\infty$-structure see _[References -- Relation to L-∞- and A-∞-algebra](ReferencesHomotopyAlgebra))_ .

+-- {: .num_prop}
###### Proposition

The inner product $\langle -,-\rangle$ satisfies the definition of a non-degenerate [[invariant polynomial]] on this $L_\infty$-algebra when restricted to fields of even degree as in def. \ref{LabelConfigurationSpace}.

=--

+-- {: .proof}
###### Proof

For simplicity of notation we discuss this as if $\mathfrak{g}$ were finite-dimensional. The argument for the infinite-dimensional case follows analogously.

Let $\{t_a\}$ be a [[basis]] of $\mathfrak{g}$ with dual basis $\{t^a\}$. Then the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$ is generated from the $\{t^a\}$ with [[differential]] given by

$$
  d_{CE(\mathfrak{g})} 
   : 
  t^a
  \mapsto
  -
  \sum_{k = 1}^\infty
  \frac{1}{k!} [t_{a_1}, \cdots, t_{a_k}]_k \,\,
  t^{a_1} \wedge \cdots \wedge t^{a_k}
  \,.
$$

The [[Weil algebra]] $W(\mathfrak{g})$ is similarly generated from $\{t^a, r^a\}$ with differential

$$
  d_{W(\mathfrak{g})} 
   : 
  t^a
  \mapsto
  -
  \sum_{k = 1}^\infty
  \frac{1}{k!} [t_{a_1}, \cdots, t_{a_k}] \,\,
  t^{a_1} \wedge \cdots \wedge t^{a_k}
  + r^a
$$

and

$$
  d_{W(\mathfrak{g})} 
  : 
  r^a 
    \mapsto
  \sum_{k = 1}^\infty
  \frac{1}{k!}
  [t_{a_0}, t_{a_1}, \cdots, t_{a_k}]_{k+1}
  \,
  r^{a_0} \wedge t^{a_1} \wedge \cdots \wedge t^{a_k}
  \,.
$$

Write

$$
  P_{a b} := \langle t_a, t_b\rangle
$$

for the components of the bilinear pairing in this basis. By (eq:GradedSymmetryBilinearPairing) it follows that we can indeed regard

$$
  P_{a b} r^a \wedge r^b
  \in W(\mathfrak{g})
$$

as an element in the [[Weil algebra]] (since $deg r^a = deg t^a + 1$).

Therefore to see that this is an [[invariant polynomial]] it remains to check that it is $d_W$-closed. To see this, first introduce the notation

$$
  C_{a_0, \cdots, a_k} :=
  \{t_{a_0}, \cdots, t_{a_k}\}
$$

for the components of the $(k+1)$-point function (eq:CorrelationFunctions). Then compute

$$
  \begin{aligned}
     d_{W(\mathfrak{g})} P_{a b } r^a \wedge r^b
     & = 
     2 P_{a b} r^a \wedge 
     \left(
        \sum_{k = 1}^\infty
        [t_{a_1}, \cdots, t_{a_k}]_k
        \,
        r^{a_1} \wedge t^{a_2}\wedge \cdots \wedge t^{a_k}
     \right)
     \\
     & = 
     2 \sum_{k = 1}^\infty
     C_{a_0, a_1, \cdots, a_k}
     \,
     r^{a_0} \wedge r^{a_1} \wedge t^{a_2} \wedge \cdots \wedge t^{a_k}
  \end{aligned}
  \,.
$$

This expression vanishes term-by-term by the symmetry properties (eq:GradedSymmetrykPointFunction) when restricted to fields of even degree: by first switching the factors in the wedge product and then relabelling the indices we obtain

$$
  \begin{aligned}
  C_{a_0,  a_1, \cdots, a_k} r^{a_0} \wedge r^{a_1}
  &= 
  (-1)^{(deg t_{a_0} + 1)(deg t_{a_1} + 1) + (deg t_{a_0})(deg t_{a_1})}
  C_{a_0,  a_1, \cdots, a_k} r^{a_0} \wedge r^{a_1}
  \\
  & = 
  (-1)^{deg t_{a_0}  + deg t_{a_1} + 1}
  C_{a_0,  a_1, \cdots, a_k} r^{a_0} \wedge r^{a_1}
  \\
  & =
  (-1)
  C_{a_0,  a_1, \cdots, a_k} r^{a_0} \wedge r^{a_1}
  \end{aligned}
  \,,
$$

where in the last step we used the constraints on degrees given by def. \ref{LabelConfigurationSpace}.

This shows that $\langle-,-\rangle$ satisfies the defining equation of an invariant polynomial on the proper configuration space. The non-degeneracy is due to (eq:NonDegeneracyOfInnerProduct).

=--

From the discussion at [[Chern-Simons element]] in the section [Canonical Chern-Simons element](http://ncatlab.org/nlab/show/Chern-Simons+element#CanonicalChernSimonsElement) we have that the [[Lagrangian]] of the [[schreiber:infinity-Chern-Simons theory]] defined by the data $(\mathfrak{g}, \langle -,-\rangle)$ is

$$
  L : A \mapsto 
  \langle A,  d A\rangle
  + 
  \sum_{k = 1}^\infty
  \frac{2}{(k+1)!}
  \langle A , [A, \cdots , A]_k\rangle
$$

for $A$ a $\mathfrak{g}$-[[infinity-Lie algebroid valued differential form|valued differential form]] on some $\Sigma$. So the closed string field theory action looks like that of $\infty$-Chern-Simons theory over an odd-graded $\Sigma$.


## References

### Bosonic string field theory

Original articles are

* [[Edward Witten]], _Noncommutative Geometry and String Field Theory_ , Nucl. Phys B268 , 253, (1986)

* [[Edward Witten]], _On background independent open string field theory_,  Phys.Rev. D46 (1992) 5467. ([arXiv:hep-th/9208027](http://arxiv.org/abs/hep-th/9208027))

* [[Barton Zwiebach]], _Closed string field theory: Quantum action and the B-V master equation_ , Nucl.Phys. B390 (1993) 33 ([arXiv:hep-th/9206084](http://arxiv.org/abs/hep-th/9206084))
  {#Zwiebach}

Brief reviews include

* [[Barton Zwiebach]], _Closed String Field Theory: An Introduction_ ([arXiv:hep-th/9305026](http://arxiv.org/abs/hep-th/9305026))

* Leonardo Rastelli, _String Field Theory_ in _Encyclopedia of Mathematical Physics_ ([arXiv:hep-th/0509129](http://arxiv.org/abs/hep-th/0509129))

A textbook-like account is in

* W. Siegel, _Introduction to string field theory_ ([arXiv:hep-th/0107094](http://arxiv.org/abs/hep-th/0107094))

Further developments are in

* [[Ashoke Sen]], [[Barton Zwiebach]], _Quantum Background Independence of Closed String Field Theory_ ([arXiv:hep-th/9311009](http://arxiv.org/abs/hep-th/9311009))

### Superstring field theory

Original articles include

* R. Saroja, [[Ashoke Sen]], _Picture Changing Operators in Closed Fermionic String Field Theory_ ([arXiv:hep-th/9202087](http://arxiv.org/abs/hep-th/9202087))

* Yuji Okawa, [[Barton Zwiebach]], _Heterotic String Field Theory_ ([arXiv:hep-th/0406212](http://arxiv.org/abs/hep-th/0406212))

Reviews include

* [[Nathan Berkovits]], _Review of open superstring field theory_ , ([arXiv:hep-th/0105230](http://arxiv.org/abs/hep-th/0105230))

### Relation to $A_\infty$- and $L_\infty$-algebras
 {#ReferencesHomotopyAlgebra}

The [[L-infinity algebra]] structure in closed string field theory was first noticed in 

* [[Barton Zwiebach]], _Closed string field theory: Quantum action and the B-V master equation_ , Nucl.Phys. B390 (1993) 33 ([arXiv:hep-th/9206084](http://arxiv.org/abs/hep-th/9206084))


The [[A-infinity algebra]] structure of open string field theory in 

* [[Matthias Gaberdiel]], [[Barton Zwiebach]], _Tensor Constructions of Open String Theories I: Foundations_ ([arXiv:hep-th/9705038](http://arxiv.org/abs/hep-th/9705038))

For the topological string see

* [[Manfred Herbst]], _Quantum A-infinity Structures for Open-Closed Topological Strings_ ([arXiv:hep-th/0602018](http://arxiv.org/abs/hep-th/0602018))

Discussion of the mathematical aspects is in 

* [[Jim Stasheff]], _Closed string field theory, strong homotopy Lie algebras and the operad actions of moduli space_ Talk given at the _Conference on Topics in Geometry and Physics_ (1992) ([arXiv:hep-th/9304061](http://arxiv.org/abs/hep-th/9304061))

* [[Martin Markl]], _Loop Homotopy Algebras in Closed String Field Theory_ (1997) ([arXiv:hep-th/9711045](http://arxiv.org/abs/hep-th/9711045))
 {#Markl}

* [[Alessandro Tomasiello]], _A-infinity structure and superpotentials_ ([arXiv:hep-th/0107195](http://arxiv.org/abs/hep-th/0107195))


* [[Hiroshige Kajiura]], _Homotopy Algebra Morphism and Geometry of Classical String Field Theory_ (2001) ([arXiv:hep-th/0112228](http://arxiv.org/abs/hep-th/0112228))

* [[Hiroshige Kajiura]], [[Jim Stasheff]], _Homotopy algebras inspired by classical open-closed string field theory_ (2004) ([arXiv:math/0410291](http://arxiv.org/abs/math/0410291))


Discussion of the CSFT-action as of the form of [[schreiber:infinity-Chern-Simons theory]] is in section 4.4 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

Surveys are in 



* [[Jim Stasheff]], _[[A Survey of Cohomological Physics]]_ 

* [[Hiroshige Kajiura]], [[Jim Stasheff]], _Homotopy algebra of open&#8211;closed strings_ Geometry & Topology Monographs 13 (2008) 229&#8211;259 ([pdf](http://msp.warwick.ac.uk/gtm/2008/13/gtm-2008-13-010s.pdf)) ([arXiv:hep-th/0606283](http://arxiv.org/abs/hep-th/0606283))

See also _[[higher category theory and physics]]_ .

#### For Yang-Mills theory

Discussion of the [[L-infinity algebra]] structure in the [[Yang-Mills theory]] that appears to lowest order in open string field theory is for instance in

* [[Anton Zeitlin]], 

  _Homotopy Lie Superalgebra in Yang-Mills Theory_ ([arXiv:0708.1773](http://arxiv.org/abs/0708.1773))

  _BV Yang-Mills as a Homotopy Chern-Simons via SFT_ ([arXiv:0709.1411](http://arxiv.org/abs/0709.1411))

  _SFT-inspired Algebraic Structures in Gauge Theories_ ([arXiv:0711.3843](http://arxiv.org/abs/0711.3843))

  _Conformal Field Theory and Algebraic Structure of Gauge Theory_ ([arXiv:0812.1840](http://arxiv.org/abs/0812.1840))

[[!redirects String field theory]]

[[!redirects closed string field theory]]