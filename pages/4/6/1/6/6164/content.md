
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _generalized homology theory_ is a certain [[functor]] from suitable [[topological spaces]] to [[graded abelian groups]] which satisfies most, but not all, of the abstract properties of [[ordinary homology]] functors (e.g. [[singular homology]]). 

By the [[Brown representability theorem]], under certain conditions every [[spectrum]] $K$ is the coefficient object of a [[generalized (Eilenberg-Steenrod) cohomology|generalized]] [[cohomology theory]] and [[Spanier-Whitehead duality|S-dually]] of a generalized homology theory. For $K = H R$ an [[Eilenberg-MacLane spectrum]] this reduces to [[homology|ordinary homology]].

See at _[[generalized (Eilenberg-Steenrod) cohomology]]_ for more.

## Definition

### Reduced homology

Throughout, write [[Top]]${}_{CW}$ for the category of [[topological spaces]] [[homeomorphism|homeomorphic]] to [[CW-complexes]]. Write $Top^{\ast/}_{CW}$ for the corresponding category of [[pointed topological spaces]]. 

Recall that [[colimits]] in $Top^{\ast/}$ are computed as colimits in $Top$ after adjoining the base point and its inclusion maps to the given diagram

+-- {: .num_example #WedgeSumAsCoproduct}
###### Example

The [[coproduct]] in [[pointed topological spaces]] is the _[[wedge sum]]_, denoted $\vee_{i \in I} X_i$.

=--


Write

$$
  \Sigma \coloneqq S^1 \wedge (-)
  \;\colon\;
  Top^{\ast/}_{CW} \longrightarrow Top^{\ast/}_{CW}
$$

for the [[reduced suspension]] functor.

Write $Ab^{\mathbb{Z}}$ for the category of [[integer]]-[[graded abelian groups]].

+-- {: .num_defn #ReducedGeneralizedHomology}
###### Definition

A **reduced homology theory** is a [[functor]]

$$
  \tilde E_\bullet 
   \;\colon\; 
  (Top^{\ast/}_{CW}) \longrightarrow Ab^{\mathbb{Z}}
$$

from the category of [[pointed topological spaces]] ([[CW-complexes]]) to $\mathbb{Z}$-[[graded abelian groups]] ("[[homology groups]]"), in components

$$
  \tilde E _\bullet
    \;\colon\; 
  (X \stackrel{f}{\longrightarrow} Y)
    \mapsto
  (\tilde E_\bullet(X) 
    \stackrel{f_\ast}{\longrightarrow}
  \tilde E_\bullet(Y))
  \,,
$$

and equipped with a [[natural isomorphism]] of degree +1, to be called the **[[suspension isomorphism]]**, of the form

$$
  \sigma
    \;\colon\;
  \tilde E_\bullet(-) 
    \overset{\simeq}{\longrightarrow} 
  \tilde E_{\bullet +1}(\Sigma -) 
$$

such that:

1. **([[homotopy invariance]])** If $f_1,f_2 \colon X \longrightarrow Y$ are two morphisms of pointed topological spaces such that there is a (base point preserving) [[homotopy]] $f_1 \simeq f_2$ between them, then the induced [[homomorphisms]] of abelian groups are [[equality|equal]] 

   $$
     f_1_\ast = f_2_\ast
     \,.
   $$

1. {#ReducedExactnessAxiom} **(exactness)** For $i \colon A \hookrightarrow X$ an inclusion of pointed topological spaces, with $j \colon X \longrightarrow Cone(i)$ the induced [[mapping cone]], then this gives an [[exact sequence]] of graded abelian groups

   $$
     \tilde E_\bullet(A)
      \overset{i_\ast}{\longrightarrow} 
     \tilde E_\bullet(X)
       \overset{j_\ast}{\longrightarrow}
     \tilde E_\bullet(Cone(i)) 
     \,.
   $$

We say $\tilde E_\bullet$ is **additive** if in addition

* **([[wedge axiom]])** For $\{X_i\}_{i \in I} $ any set of pointed CW-complexes, then the canonical morphism

  $$
    \oplus_{i \in I} \tilde E_\bullet(X_i)
      \longrightarrow
    \tilde E^\bullet(\vee_{i \in I} X_i) 
  $$

  from the [[direct sum]] of the value on the summands to the value on the [[wedge sum]], example \ref{WedgeSumAsCoproduct}, is an [[isomorphism]].

We say $\tilde E_\bullet$ is **ordinary** if its value on the [[0-sphere]] $S^0$ is concentrated in degree 0:

* **(Dimension)**  $\tilde E_{\bullet\neq 0}(\mathbb{S}^0) \simeq 0$.

A [[homomorphism]] of reduced cohomology theories

$$
  \eta \;\colon\; \tilde E_\bullet \longrightarrow \tilde F_\bullet
$$

is a [[natural transformation]] between the underlying functors which is compatible with the suspension isomorphisms in that all the following [[commuting square|squares commute]]

$$
  \array{
    \tilde E_\bullet(X) &\overset{\eta_X}{\longrightarrow}&  \tilde F_\bullet(X)
    \\
    {}^{\mathllap{\sigma_E}}\downarrow && \downarrow^{\mathrlap{\sigma_F}}
    \\
    \tilde E_{\bullet + 1}(\Sigma X) 
    &\overset{\eta_{\Sigma X}}{\longrightarrow}&
    \tilde F_{\bullet + 1}(\Sigma X)
  }
  \,.
$$

=--

### Unreduced homology

In the following a _pair_ $(X,A)$ refers to a [[subspace]] inclusion of [[topological spaces]] ([[CW-complexes]])  $A \hookrightarrow X$.  Whenever only one space is mentioned, the subspace is assumed to be the [[empty set]] $(X, \emptyset)$. Write $Top_{CW}^{\hookrightarrow}$ for the category of such pairs (the [[full subcategory]] of the [[arrow category]] of $Top_{CW}$ on the inclusions). We identify $Top_{CW} \hookrightarrow Top_{CW}^{\hookrightarrow}$ by $X \mapsto (X,\emptyset)$.


+-- {: .num_defn #GeneralizedHomologyTheory}
###### Definition

A **homology theory** (unreduced, [[relative cohomology|relative]]) is a [[functor]]

$$
  E_\bullet : (Top_{CW}^{\hookrightarrow}) \longrightarrow Ab^{\mathbb{Z}}
$$

to the category of $\mathbb{Z}$-[[graded abelian groups]], as well as a [[natural transformation]] of degree +1, to be called the **[[connecting homomorphism]]**, of the form

$$
  \delta_{(X,A)} 
    \;\colon\;  
  E_{\bullet + 1}(X, A)
    \longrightarrow
  E_\bullet(A, \emptyset)  
  \,.
$$ 

such that:

1. **(homotopy invariance)** For $f \colon (X_1,A_1) \to (X_2,A_2)$ a [[homotopy equivalence]] of pairs, then 

   $$
     E_\bullet(f) 
      \;\colon\; 
     E_\bullet(X_1,A_1) \stackrel{\simeq}{\longrightarrow} E_\bullet(X_2,A_2)
   $$

   is an [[isomorphism]];

1. {#ExactnessUnreduced} **(exactness)** For $A \hookrightarrow X$ the induced sequence

   $$ 
     \cdots 
       \to 
     E_{n+1}(X, A) 
       \stackrel{\delta}{\longrightarrow} 
     E_n(A) 
       \longrightarrow
     E_n(X) 
       \longrightarrow 
     E_n(X, A) 
       \to 
     \cdots 
   $$

   is a [[long exact sequence]] of [[abelian groups]].

1. {#excision} **([[excision]])** For $U \hookrightarrow A \hookrightarrow X$ such that $\overline{U} \subset Int(A)$, then the natural inclusion of the pair $i \colon (X-U, A-U) \hookrightarrow (X, A)$ induces an isomorphism 

   $$
     E_\bullet(i) 
      \;\colon\; 
     E_n(X-U, A-U)  
      \overset{\simeq}{\longrightarrow}
     E_n(X, A)
   $$

We say $E_\bullet$ is **additive** if it takes [[coproducts]] to [[direct sums]]:

* **(additivity)** If $(X, A) = \coprod_i (X_i, A_i)$ is a [[coproduct]], then the canonical comparison morphism 

  $$
    \oplus_i E_n(X_i, A_i) \overset{\simeq}{\longrightarrow} E_n(X, A)
  $$

  is an [[isomorphism]]from the [[direct sum]] of the value on the summands, to the value on the total pair.

We say $E_\bullet$ is **ordinary** if its value on the point is concentrated in degree 0

* **(Dimension)**: $E_{\bullet \neq 0}(\ast,\emptyset) = 0$.

A [[homomorphism]] of unreduced homology theories 

$$
  \eta \;\colon\; E_\bullet \longrightarrow F_\bullet
$$

is a [[natural transformation]] of the underlying functors that is compatible with the connecting homomorphisms, hence such that all these [[commuting square|squares commute]]:

$$
  \array{
     E_{\bullet +1}(X,A) 
       &\overset{\eta_{(X,A)}}{\longrightarrow}&
     F_{\bullet +1}(X,A)
     \\
     {}^{\mathllap{\delta_E}}\downarrow && \downarrow^{\mathrlap{\delta_F}}
     \\
     E_\bullet(A,\emptyset) &\overset{\eta_{(A,\emptyset)}}{\longrightarrow}& F_\bullet(A,\emptyset)
  }
  \,.
$$

=--

+-- {: .num_defn #AlternativeFormulationOfExcisionAxiom}
###### Lemma

The excision axiom in def. \ref{GeneralizedHomologyTheory} is equivalent to the following statement:

For all $A,B \hookrightarrow X$ with $X = A \cup B$, then the inclusion

$$
  i \colon (A, A \cap B) \longrightarrow (X,B) 
$$

induces an isomorphism,

$$
  i_\ast
    \;\colon\;
  E_\bullet(A, A \cap B)
    \overset{\simeq}{\longrightarrow}
  E_\bullet(X, B)
  \,.
$$

=--

(e.g [Switzer 75, 7.2, 7.5](#Switzer75))

+-- {: .proof}
###### Proof

First consider the statement under the condition that $X = Int(A) \cup Int(B)$.

In one direction, suppose that $E^\bullet$ satisfies the original excision axiom. Given $A,B$ with $X = \Int(A) \cup Int(B)$, set $U \coloneqq X-A$ and observe that 

$$
  \begin{aligned}
     \overline{U} 
        & = \overline{X-A} 
     \\ & = X- Int(A)
     \\ & \subset Int(B)
  \end{aligned}
$$

and that

$$
  (X-U, B-U) = (A, A \cap B)
  \,.
$$

Hence the excision axiom implies $  E^\bullet(X, B) \overset{\simeq}{\longrightarrow} E^\bullet(A, A \cap B)$. 

Conversely, suppose $E^\bullet$ satisfies the alternative condition. Given $U \hookrightarrow A \hookrightarrow X$ with $\overline{U} \subset Int(A)$, observe that we have a cover

$$
  \begin{aligned}
          Int(X-U) \cup Int(A) 
      & = (X - \overline{U}) \cap \Int(A)
   \\ & \supset (X - Int(A)) \cap Int(A)
   \\ & = X   
  \end{aligned}
$$

and that

$$
  (X-U, (X-U) \cap A) = (X-U, A - U)
  \,.
$$

Hence

$$
  E^\bullet(X-U,A-U)
  \simeq
  E^\bullet(X-U, (X-U)\cap A)
  \simeq
  E^\bullet(X,A)
  \,.
$$

This shows the statement for the special case that $X = Int(A)\cup Int(U)$.  The general statement reduces to this by finding a suitable homotopy equivalence to a slightly larger covering pair (e.g [Switzer 75, 7.5](#Switzer75)).

=--

+-- {: .num_prop #ExactSequenceOfATriple}
###### Proposition
**(exact sequence of a triple)**

For $E_\bullet$ an unreduced generalized cohomology theory, def. \ref{GeneralizedHomologyTheory}, then every inclusion of two consecutive subspaces

$$
  Z \hookrightarrow Y \hookrightarrow X
$$

induces a [[long exact sequence]] of homology groups of the form

$$
  \cdots
   \to
  E_q(Y,Z)
    \stackrel{}{\longrightarrow}
  E_q(X,Z)
    \stackrel{}{\longrightarrow}
  E_q(X,Y)
    \stackrel{\bar \delta}{\longrightarrow}
  E_{q-1}(Y,Z) 
    \to
  \cdots
$$

where 

$$
  \bar \delta 
    \;\colon \;
  E_{q}(X,Y)
   \stackrel{\delta}{\longrightarrow}
  E_{q-1}(Y)
   \longrightarrow
  E_{q-1}(Y,Z) 
  \,.
$$

=--

+-- {: .proof}
###### Proof

Apply the [[braid lemma]] to the interlocking long exact sequences of the three pairs $(X,Y)$, $(X,Z)$, $(Y,Z)$:

<img src="http://www.ncatlab.org/nlab/files/BraidDiagramForHomologyOnTripled.jpg" width="500">

(graphics from [this Maths.SE comment](http://math.stackexchange.com/a/1180681/58526))

See [here](braid+lemma#ExactSequenceForTripleInGeneralizedHomology) for details.


=--



## Properties


### Expression by ordinary homology via Atiyah-Hirzebruch spectral sequence

The [[Atiyah-Hirzebruch spectral sequence]] serves to express generalized homology $E_\bullet$ in terms of ordinary homology with coefficients in $E_\bullet(\ast)$.

### Whitehead theorem
 {#WhiteheadTheorem}

+-- {: .num_prop}
###### Proposition

Let $\phi \colon E \longrightarrow F$ be a morphism of reduced generalized (co-)homology functors, def. \ref{ReducedGeneralizedHomology} (a [[natural transformation]]) such that its component

$$
  \phi(S^0) \colon E(S^0) \longrightarrow F(S^0)
$$

on the [[0-sphere]] is an [[isomorphism]]. Then $\phi(X)\colon E(X)\to F(X)$ is an [[isomorphism]] for $X$ any [[CW-complex]] with a [[finite number]] of cells. If both $E$ and $F$ satisfy the [[wedge axiom]], then $\phi(X)$ is an isomorphism for $X$ any [[CW-complex]], not necessarily finite.

=--


For $E$ and $F$ [[ordinary cohomology]]/[[ordinary homology]] functors a proof of this is in ([Eilenberg-Steenrod 52, section III.10](#EilenbergSteenrod52)). From this the general statement follows (e.g. [Kochman 96, theorem 3.4.3, corollary 4.2.8](#Kochman96)) via the [[natural transformation|naturality]] of the [[Atiyah-Hirzebruch spectral sequence]] (the classical result gives that $\phi$ induces an isomorphism between the second pages of the AHSSs for $E$ and $F$). A complete proof of the general result is also given as ([Switzer 75, theorem 7.55, theorem 7.67](#Switzer75))


## Examples

* [[stable homotopy homology theory]] is the homology theory represented by the [[sphere spectrum]]

* [[ordinary homology]] is the homology theory represented by an [[Eilenberg-MacLane spectrum]]

* [[bordism homology theory]] is the homology theory represented by a [[Thom spectrum]];



## Related concepts

* [[generalized cohomology]]

* [[Kronecker pairing]]

* [[Atiyah-Hirzebruch spectral sequence]]

* [[Steenrod algebra]]

* [[phantom map]]

* [[bivariant cohomology]]

* [[Bousfield equivalence]]

* [[Hurewicz homomorphism]], [[Boardman homomorphism]]

## References

(For more see the references at  _[[generalized (Eilenberg-Steenrod) cohomology]]_.)

Original articles include

* [[George Whitehead]], _Generalized homology theories_  (1961) ([pdf](http://www.maths.ed.ac.uk/~aar/papers/gww9.pdf))

Textbook accounts include

* {#Kochmann96} [[Stanley Kochmann]], section 3.4 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Switzer75} [[Robert Switzer]], chapter 7 (and 8-12) of _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 


* [[Stefan Schwede]], chapter II, section 6 of  _[[Symmetric spectra]]_, 2012  ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

See also

* [[Friedrich Bauer]], _Classifying spectra for generalized homology theories_ Annali di Maternatica pura ed applicata
(IV), Vol. CLXIV (1993), pp. 365-399 

* [[Friedrich Bauer]], _Remarks on universal coefficient theorems for generalized homology theories_ Quaestiones Mathematicae
Volume 9, Issue 1 & 4, 1986, Pages 29 - 54 

A general construction of homologies by "geometric cycles" similar to the [[Baum-Douglas geometric cycles]] for [[K-homology]] is discussed in 

* S. Buoncristiano, C. P. Rourke and B. J. Sanderson, _A geometric approach to homology theory_, Cambridge Univ. Press, Cambridge, Mass. (1976)

Further generalization of this to [[bivariant cohomology theories]] is in 

* Martin Jakob, _Bivariant theories for smooth manifolds_, Applied Categorical Structures 10 no. 3 (2002)


[[!redirects generalized homology theory]]
[[!redirects generalized homology theories]]

[[!redirects Whitehead-generalized homology theory]]
[[!redirects Whitehead-generalized homology theories]]


[[!redirects homology theory]]
[[!redirects homology theories]]

[[!redirects generalized homologies]]

[[!redirects generalised homology]]
[[!redirects generalised homologies]]

