
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The collection of [[functors]] from ([[pointed topological space|pointed]]) [[topological spaces]] to [[abelian groups]] which assign [[cohomology groups]] of [[ordinary cohomology]] (e.g. [[singular cohomology]]) may be [[axiom|axiomatized]] by a small set of natural conditions, called the _Eilenberg-Steenrod axioms_ ([Eilenberg-Steenrod 52, I.3](#EilenbergSteenrod52)), see [below](#TheEilenbergSteenrodAxioms). One of these conditions, the "dimension axiom" ([Eilenberg-Steenrod 52, I.3 Axiom 7](#EilenbergSteenrod52)) says that the (co)homology groups assigned to the point are concentrated in degree 0. The class of functors obtained by discarding this "dimension axiom" came to be known as _generalized (co)homology theories_ ([Whitehead 62](#Whitehead62)) or _extraordinary (co)homology theories_. 

Examples include [[topological K-theory]] ([Atiyah-Hirzebruch 61, 1.8](https://ncatlab.org/nlab/show/topological+K-theory#AtiyahHirzebruch61)), [[elliptic cohomology]] and [[cobordism cohomology theory]]. Dually one speaks of _[[generalized homology]]_.

Notice that, while the terminology "generalized cohomology" is standard in [[algebraic topology]] with an eye towards [[stable homotopy theory]], it is somewhat unfortunate in that there are various _other_ and _further_ generalizations of the axioms that all still deserve to be and are called "[[cohomology]]". For instance dropping the [[suspension isomorphism|suspension]] axiom leads to [[nonabelian cohomology]] and dropping the "homotopy axiom" (and taking the domain spaces to be [[smooth manifolds]]) leads to the further generality of [[differential cohomology]]. 
This entry here is concerned with the generalization obtained from the Eilenberg-Steenrod axioms by _just_ discarding the dimension axiom. For lack of a better term, we say "generalized (Eilenberg-Steenrod) cohomology" here.

In ([Whitehead 62](#Whitehead62)) it was observed that every [[spectrum]] induces a generalized homology theory.  The _[[Brown representability theorem]]_ ([Brown 62](#Brown62)) asserts that every generalized (co)homology arises this way, being [[representable functor|represented]] by [[mapping spectra]] into/[[smash product]] with a [[spectrum]].  But beware that the cohomology theory represented by a spectrum in general contains strictly less information than the spectrum, due to the existence of "[[phantom maps]]".

On the other hand, if one refines the concept of a generalized homology theory from taking values in [[graded abelian]] groups to taking values in [[homotopy types]] then it does become equivalent to the concept of _spectrum_, this is the statement at _[excisive functor -- Examples -- Spectrum objects](excisive+%28%E2%88%9E%2C1%29-functor#SpectrumObjects)_.

This means that from a perspective of [[higher category theory]], generalized Eilenberg-Steenrod cohomology is the intrinsic [[cohomology]] of the [[(∞,1)-category of spectra]], or better: [[twisted cohomology|twisted]] generalized Eilenberg-Steenrod cohomology is the intrinsic cohomology of the [[tangent (∞,1)-topos]] of [[parameterized spectra]].


+-- {: .standout}

Generalized Eilenberg-Steenrod cohomology is 
[[cohomology]] $E(X)= H(X,E)$ with [[coefficients]] $E$ a [[spectrum object]].

=--

## Definition
 {#TheEilenbergSteenrodAxioms}

This sections states the classical formulation of the Eilenberg-Steenrod axioms due to ([Eilenberg-Steenrod 52, I.3](#EilenbergSteenrod52)) in terms of concepts from classical [[algebraic topology]], such as [[CW-pairs]] and [[mapping cones]]. 

More abstractly, via the [[classical model structure on topological spaces]], these structures are seen to serve as presentations for certain [[homotopy pushouts]]. In terms of "abstract homotopy theory" ([[(infinity,1)-category theory]]) one obtains a more streamlined formulation, which we turn to [below](#AbstractFormulation).

$\,$

There are two versions of the statement of the axioms:

* _[Reduced cohomology](#ReducedCohomology)_;

* _[Unreduced cohomology](#UnreducedCohomology)_.

There are functors taking any reduced cohomology theory to an unreduced one, and vice versa. When some fine detail in the axioms is suitably set up, then this establishes an [[equivalence of categories|equivalence]] between reduced and unreduced generalized cohomology:

* _[Relation between reduced and unreduced cohomology](#RelationBetweenReducedAndUnreduced)_

The fine detail in the axioms that makes this work is such as to ensure that a cohomology theory is a functor on the [[opposite category|opposite]] of the (pointed/pairwise) [[classical homotopy category]]. Since this has different presentations, there are corresponding different versions of suitable axioms:

1. On the one hand, $Ho(Top_{Quillen})$ may be presented by topological spaces homeomorphic to [[CW-complexes]] and with [[homotopy equivalence]]-classes of continuous functions between them, and accordingly a generalized cohomology theory may be taken to be a funtor on (pointed/pairs of) CW-complexes invariant under [[homotopy equivalence]].

1. On the other hand, $Ho(Top_{Quillen})$ may be presented by all topological spaces with [[weak homotopy equivalences]] [[localization|inverted]], and accordingly a generalized cohomology theory may be taken to be a functor on all (pointed/pairs of) topological spaces that sends weak homotopy equivalences to isomorphisms.

Notice however that "[[classical homotopy category]]" is already ambiguous. Pre Quillen this was the category of _all_ topological spaces with homotopy equivalence classes of maps between them, and often generalized cohomology functors are defined on this larger category and only restricted to CW-complexes or required to preserve weak homotopy equivalences when need be (e.g. [Switzer 75, p.117](#Switzer75)), such as for establishing the equivalence between reduced and unreduced theories.

Moreover, historically, these conditions have been decomposed in several numbers of ways. Notably ([Eilenberg-Steenrod 52](#EilenbergSteenrod52)) originally listed 7 axioms for unreduced cohomology, more than typically counted today, but their axioms 1 and 2 jointly just said that we have a functor on topological spaces, axiom 3 was the condition for the connecting homomorphism to be a [[natural transformation]], conditions which later ([Switzer 75, p. 99,100](#Switzer75)) were absorbed in the underlying structure. 

Finally, following the historical development it is common to state the exactness properties of cohomology functors in terms of [[mapping cone]] constructions. These are models for [[homotopy cofibers]], but in general only when some technical conditions are met, such that the underlying topological spaces are CW-complexes. 

For these reasons, in the following we stick to two points of views: where we discuss cohomology theories as functors on topological spaces we restrict attention to those homeomorphic to CW-complexes. In a second description we speak fully abstractly about functors on the homotopy category of a given model category of $\infty$-category.

### Reduced cohomology
 {#ReducedCohomology}

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

Write $Ab^{\mathbb{Z}}$ for the category of integer-[[graded abelian groups]].

+-- {: .num_defn #ReducedGeneralizedCohomology}
###### Definition

A **reduced [[cohomology theory]]** is a [[functor]]

$$
  \tilde E^\bullet 
   \;\colon\; 
  (Top^{\ast/}_{CW})^{op} \longrightarrow Ab^{\mathbb{Z}}
$$

from the [[opposite category|opposite]] of [[pointed topological spaces]] ([[CW-complexes]]) to $\mathbb{Z}$-[[graded abelian groups]] ("[[cohomology groups]]"), in components

$$
  \tilde E 
    \;\colon\; 
  (X \stackrel{f}{\longrightarrow} Y)
    \mapsto
  (\tilde E^\bullet(Y) 
    \stackrel{f^\ast}{\longrightarrow}
  \tilde E^\bullet(X))
  \,,
$$

and equipped with a [[natural isomorphism]] of degree +1, to be called the **[[suspension isomorphism]]**, of the form

$$
  \sigma
    \;\colon\;
  \tilde E^{\bullet +1}(\Sigma -) 
    \overset{\simeq}{\longrightarrow} 
  \tilde E^\bullet(-) 
$$

such that:

1. **([[homotopy invariance]])** If $f_1,f_2 \colon X \longrightarrow Y$ are two morphisms of pointed topological spaces such that there is a (base point preserving) [[homotopy]] $f_1 \simeq f_2$ between them, then the induced [[homomorphisms]] of abelian groups are [[equality|equal]] 

   $$
     f_1^\ast = f_2^\ast
     \,.
   $$

1. {#ReducedExactnessAxiom} **(exactness)** For $i \colon A \hookrightarrow X$ an inclusion of [[pointed topological spaces]], with $j \colon X \longrightarrow Cone(i)$ the induced [[mapping cone]], then this gives an [[exact sequence]] of [[graded abelian groups]]

   $$
     \tilde E^\bullet(Cone(i)) 
      \overset{j^\ast}{\longrightarrow} 
     \tilde E^\bullet(X)
       \overset{i^\ast}{\longrightarrow}
     \tilde E^\bullet(A)
     \,.
   $$

We say $\tilde E^\bullet$ is **additive** if in addition

* {#WedgeAxiom} **([[wedge axiom]])** For $\{X_i\}_{i \in I} $ any set of pointed CW-complexes, then the canonical comparison morphism

  $$
    \tilde E^\bullet(\vee_{i \in I} X_i) 
     \longrightarrow
    \prod_{i \in I} \tilde E^\bullet(X_i)
  $$

  is an [[isomorphism]], from the functor applied to their [[wedge sum]], example \ref{WedgeSumAsCoproduct}, to the [[product]] of its values on the wedge summands, .

We say $\tilde E^\bullet$ is **ordinary** if its value on the [[0-sphere]] $S^0$ is concentrated in degree 0:

* **(Dimension)**  $\tilde E^{\bullet\neq 0}(\mathbb{S}^0) \simeq 0$.

A [[homomorphism]] of reduced cohomology theories

$$
  \eta \;\colon\; \tilde E^\bullet \longrightarrow \tilde F^\bullet
$$

is a [[natural transformation]] between the underlying functors which is compatible with the suspension isomorphisms in that all the following [[commuting square|squares commute]]

$$
  \array{
    \tilde E^\bullet(X) &\overset{\eta_X}{\longrightarrow}&  \tilde F^\bullet(X)
    \\
    {}^{\mathllap{\sigma_E}}\downarrow && \downarrow^{\mathrlap{\sigma_F}}
    \\
    \tilde E^{\bullet + 1}(\Sigma X) 
    &\overset{\eta_{\Sigma X}}{\longrightarrow}&
    \tilde F^{\bullet + 1}(\Sigma X)
  }
  \,.
$$

=--

(e.g. [AGP 02, def. 12.1.4](#AguilarGitlerPrieto02))

We may rephrase this more intrinsically and more generally:

+-- {: .num_defn #GeneralizedCohomologyOnGeneralInfinityCategory}
###### Definition

Let $\mathcal{C}$ be an [[(∞,1)-category]] with [[(∞,1)-pushouts]], and with a [[zero object]] $0 \in \mathcal{C}$. Write $\Sigma \colon \mathcal{C} \to \mathcal{C}\colon X\mapsto 0 \underset{X}{\sqcup} 0$ for the corresponding [[suspension]] [[(∞,1)-functor]].

A **reduced generalized cohomology theory** on $\mathcal{C}$ is 

1. a [[functor]]

   $$
     E^\bullet \;\colon \; Ho(\mathcal{C})^{op} \longrightarrow Ab^{\mathbb{Z}}
   $$

   (from the [[opposite category|opposite]] of the [[homotopy category of an (infinity,1)-category|homotopy category]] of $\mathcal{C}$ into $\mathbb{Z}$-[[graded abelian groups]]);

1. a [[natural isomorphisms]] ("[[suspension isomorphisms]]") of degree +1

   $$
     \sigma \; \colon \; H^\bullet \longrightarrow H^{\bullet+1} \circ \Sigma
   $$

such that $H^\bullet$

1. takes small [[coproducts]] to [[products]];

1. takes [[homotopy cofiber sequences]] to [[exact sequences]].

=--

+-- {: .num_defn #ConnectinHomomorphismForCohomologyTheoryOnInfinityCategory}
###### Definition

Given a generalized cohomology theory $(H^\bullet,\sigma)$ on some $\mathcal{C}$ as in def. \ref{GeneralizedCohomologyOnGeneralInfinityCategory}, and given a [[homotopy cofiber sequence]] in $\mathcal{C}$

$$
  X \stackrel{f}{\longrightarrow} Y \stackrel{g}{\longrightarrow} Z
  \stackrel{coker(g)}{\longrightarrow}
  \Sigma X
  \,,
$$

then the corresponding **[[connecting homomorphism]]** is the composite

$$
  \partial 
    \;\colon\; 
  E^\bullet(X)
   \stackrel{\sigma}{\longrightarrow}
  E^{\bullet+1}(\Sigma X)
   \stackrel{coker(g)^\ast}{\longrightarrow}
  E^{\bullet+1}(Z)
  \,.
$$

=--

+-- {: .num_prop #LongExactSequenceOfACohomologyTheoryOnAnInfinityCategory}
###### Proposition

The [[connecting homomorphisms]] of def. \ref{ConnectinHomomorphismForCohomologyTheoryOnInfinityCategory} are parts of [[long exact sequences]]

$$
  \cdots
   \stackrel{\partial}{\longrightarrow}
  E^{\bullet}(Z) 
    \longrightarrow 
  E^\bullet(Y) 
    \longrightarrow 
  E^\bullet(X)
    \stackrel{\partial}{\longrightarrow}
  E^{\bullet+1}(Z)
   \to \cdots
  \,.
$$

=--


+-- {: .proof}
###### Proof

By the defining exactness of $E^\bullet$, def. \ref{GeneralizedCohomologyOnGeneralInfinityCategory}, and the way this appears in def. \ref{ConnectinHomomorphismForCohomologyTheoryOnInfinityCategory}, using that $\sigma$ is by definition an isomorphism.

=--



### Unreduced cohomology
 {#UnreducedCohomology}

In the following a _pair_ $(X,A)$ refers to a [[subspace]] inclusion of [[topological spaces]] ([[CW-complexes]])  $A \hookrightarrow X$.  Whenever only one space is mentioned, the subspace is assumed to be the [[empty set]] $(X, \emptyset)$. Write $Top_{CW}^{\hookrightarrow}$ for the category of such pairs (the [[full subcategory]] of the [[arrow category]] of $Top_{CW}$ on the inclusions). We identify $Top_{CW} \hookrightarrow Top_{CW}^{\hookrightarrow}$ by $X \mapsto (X,\emptyset)$.


+-- {: .num_defn #GeneralizedCohomologyTheory}
###### Definition

A _[[cohomology theory]]_ (unreduced, [[relative cohomology|relative]]) is a [[functor]]

$$
  E^\bullet : (Top_{CW}^{\hookrightarrow})^{op} \to Ab^{\mathbb{Z}}
$$

to the category of $\mathbb{Z}$-[[graded abelian groups]], as well as a [[natural transformation]] of degree +1, to be called the **[[connecting homomorphism]]**, of the form

$$
  \delta_{(X,A)} 
    \;\colon\;  
  E^\bullet(A, \emptyset) \to E^{\bullet + 1}(X, A)
  \,.
$$ 

such that:

1. **(homotopy invariance)** For $f \colon (X_1,A_1) \to (X_2,A_2)$ a [[homotopy equivalence]] of pairs, then 

   $$
     E^\bullet(f) 
      \;\colon\; 
     E^\bullet(X_2,A_2) \stackrel{\simeq}{\longrightarrow} E^\bullet(X_1,A_1)
   $$

   is an [[isomorphism]];

1. {#ExactnessUnreduced} **(exactness)** For $A \hookrightarrow X$ the induced sequence

   $$ 
     \cdots 
       \to 
     E^n(X, A) 
       \longrightarrow 
     E^n(X) 
       \longrightarrow
     E^n(A) 
       \stackrel{\delta}{\longrightarrow} 
     E^{n+1}(X, A) 
       \to 
     \cdots 
   $$

   is a [[long exact sequence]] of [[abelian groups]].

1. {#excision} **([[excision]])** For $U \hookrightarrow A \hookrightarrow X$ such that $\overline{U} \subset Int(A)$, then the natural inclusion of the pair $i \colon (X-U, A-U) \hookrightarrow (X, A)$ induces an isomorphism 

   $$
     E^\bullet(i) 
      \;\colon\; 
     E^n(X, A)
      \overset{\simeq}{\longrightarrow}
     E^n(X-U, A-U)  
   $$

We say $E^\bullet$ is **additive** if it takes [[coproducts]] to [[products]]:

* **(additivity)** If $(X, A) = \coprod_i (X_i, A_i)$ is a [[coproduct]], then the canonical comparison morphism 

  $$
    E^n(X, A) \overset{\simeq}{\longrightarrow} \prod_i E^n(X_i, A_i)
  $$

  is an [[isomorphism]] from the value on $(X,A)$ to the [[product]] of values on the summands.

We say $E^\bullet$ is **ordinary** if its value on the point is concentrated in degree 0

* **(Dimension)**: $E^{\bullet \neq 0}(\ast,\emptyset) = 0$.

A [[homomorphism]] of unreduced cohomology theories 

$$
  \eta \;\colon\; E^\bullet \longrightarrow F^\bullet
$$

is a [[natural transformation]] of the underlying functors that is compatible with the connecting homomorphisms, hence such that all these [[commuting square|squares commute]]:

$$
  \array{
     E^\bullet(A,\emptyset) &\overset{\eta_{(A,\emptyset)}}{\longrightarrow}& F^\bullet(A,\emptyset)
     \\
     {}^{\mathllap{\delta_E}}\downarrow && \downarrow^{\mathrlap{\delta_F}}
     \\
     E^{\bullet +1}(X,A) 
       &\overset{\eta_{(X,A)}}{\longrightarrow}&
     F^{\bullet +1}(X,A)
  }
  \,.
$$

=--

e.g. ([AGP 02, def. 12.1.1 ](#AguilarGitlerPrieto02)). 


+-- {: .num_defn #AlternativeFormulationOfExcisionAxiom}
###### Lemma

The excision axiom in def. \ref{GeneralizedCohomologyTheory} is equivalent to the following statement:

For all $A,B \hookrightarrow X$ with $X = Int(A) \cup Int(B)$, then the inclusion

$$
  i \colon (A, A \cap B) \longrightarrow (X,B) 
$$

induces an isomorphism,

$$
  i^\ast 
    \;\colon\;
  E^\bullet(X, B)
    \overset{\simeq}{\longrightarrow}
  E^\bullet(A, A \cap B)
$$

=--

(e.g [Switzer 75, 7.2](#Switzer75))

+-- {: .proof}
###### Proof

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
      & = (X - \overline{U}) \cup \Int(A)
   \\ & \supset (X - Int(A)) \cup Int(A)
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

=--

The following lemma shows that the dependence in pairs of spaces in a generalized cohomology theory is really a stand-in for evaluation on [[homotopy cofibers]] of inclusions.

+-- {: .num_lemma #EvaluationOfCohomologyTheoryOnGoodPairIsEvaluationOnQuotient}
###### Lemma

Let $E^\bullet$ be an cohomology theory, def. \ref{GeneralizedCohomologyTheory}, and let $A \hookrightarrow X$. Then there is an isomorphism 

$$
  E^\bullet(X,A)
    \stackrel{\simeq}{\longrightarrow}
  E^\bullet(X \cup Cone(A), \ast)
$$

between the value of $E^\bullet$ on the pair $(X,A)$ and its value on the [[mapping cone]] of the inclusion, relative to a basepoint.

If moreover $A \hookrightarrow X$ is (the [[retract]] of) a [[relative cell complex]] inclusion, then also the morphism in cohomology induced from the [[quotient]] map $p \;\colon\; (X,A)\longrightarrow (X/A, \ast)$ is an [[isomorphism]]:

$$
  E^\bullet(p)
    \;\colon\; 
  E^\bullet(X/A,\ast)
    \longrightarrow
  E^\bullet(X,A)
  \,.
$$

=--

(e.g [AGP 02, corollary 12.1.10](#AguilarGitlerPrieto02))


+-- {: .proof}
###### Proof

Consider $U \coloneqq (Cone(A)-A \times \{0\}) \hookrightarrow Cone(A)$, the cone on $A$ minus the base $A$. We have

$$
  ( X\cup Cone(A)-U, Cone(A)-U) \simeq (X,A)
$$

and hence the first isomorphism in the statement is given by the excision axiom followed by homotopy invariance (along the contraction of the cone to the point).

Next consider the quotient of the [[mapping cone]] of the inclusion:

$$
  ( X\cup Cone(A), Cone(A) ) \longrightarrow (X/A,\ast)
  \,.
$$

If $A \hookrightarrow X$ is a cofibration, then this is a [[homotopy equivalence]] since $Cone(A)$ is contractible and since by the dual [[factorization lemma]] $X \cup Cone(A)\to X/A$ is a weak homotopy equivalence, hence a homotopy equivalence on CW-complexes.

Hence now we get a composite isomorphism

$$
  E^\bullet(X/A,\ast)
    \overset{\simeq}{\longrightarrow}
  E^\bullet( X\cup Cone(A), Cone(A) )
    \overset{\simeq}{\longrightarrow}
  E^\bullet(X,A)
  \,.
$$


=--

+-- {: .num_example #GeneralizedCohomologyOnHomotopyQuotientMaps}
###### Example

As an important special case of : Let $(X,x)$ be a [[pointed topological space|pointed]] [[CW-complex]]. For $p\colon (Cone(X), X) \to (\Sigma X,\{x\})$ the quotient map from the reduced cone on $X$ to the [[reduced suspension]], then 

$$
  E^\bullet(p)
  \;\colon\;
  E^\bullet(Cone(X),X)
   \overset{\simeq}{\longrightarrow}
  E^\bullet(\Sigma X, \{x\})
$$ 

is an isomorphism.

=--

+-- {: .num_prop #ExactSequenceOfATriple}
###### Proposition
**(exact sequence of a triple)**

For $E^\bullet$ an unreduced generalized cohomology theory, def. \ref{GeneralizedCohomologyTheory}, then every inclusion of two consecutive subspaces

$$
  Z \hookrightarrow Y \hookrightarrow X
$$

induces a [[long exact sequence]] of cohomology groups of the form

$$
  \cdots
   \to
  E^{q-1}(Y,Z) 
    \stackrel{\bar \delta}{\longrightarrow}
  E^q(X,Y)
    \stackrel{}{\longrightarrow}
  E^q(X,Z)
    \stackrel{}{\longrightarrow}
  E^q(Y,Z)
    \to
  \cdots
$$

where 

$$
  \bar \delta 
    \;\colon \;
  E^{q-1}(Y,Z) 
   \longrightarrow
  E^{q-1}(Y)
   \stackrel{\delta}{\longrightarrow}
  E^{q}(X,Y)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Apply the [[braid lemma]] to the interlocking long exact sequences of the three pairs $(X,Y)$, $(X,Z)$, $(Y,Z)$. See [here](braid+lemma#ExactSequenceForTripleInGeneralizedHomology) for details.

The dual braid diagram for [[generalized homology]] is this:

<img src="http://www.ncatlab.org/nlab/files/BraidDiagramForHomologyOnTripled.jpg" width="500">

(graphics from [this Maths.SE comment](http://math.stackexchange.com/a/1180681/58526))

=---

+-- {: .num_remark}
###### Remark

The exact sequence of a triple in prop. \ref{ExactSequenceOfATriple} is what gives rise to the [[Cartan-Eilenberg spectral sequence]] for $E$-cohomology of a [[CW-complex]] $X$.

=--

+-- {: .num_example #ExtractingSuspensionIsomorphismFromUnreducedCohomology}
###### Example

For $(X,x)$ a [[pointed topological space]] and $Cone(X) = (X \wedge (I_+))/X$ its reduced [[cone]], the long exact sequence of the triple $(\{x\}, X, Cone(X))$, prop. \ref{ExactSequenceOfATriple},

$$
   0
   \simeq
   E^q(Cone(X), \{x\})
     \longrightarrow
   E^q(X,\{x\})
     \overset{\bar \delta}{\longrightarrow}
   E^{q+1}(Cone(X),X)
     \longrightarrow
   E^{q+1}(Cone(X), \{x\})
   \simeq 0
$$

exhibits the [[connecting homomorphism]] $\bar \delta$ here as an [[isomorphism]]

$$
   \bar \delta
     \;\colon\;
   E^q(X,\{x\})
     \overset{\simeq}{\longrightarrow}
   E^{q+1}(Cone(X),X)
  \,.
$$

This is the _[[suspension isomorphism]]_ extracted from the unreduced cohomology theory, see def. \ref{FromUnreducedToReducedCohomology} below.

=--

+-- {: .num_prop #MayerVietorisSequenceInGeneralizedCohomology}
###### Proposition
**([[Mayer-Vietoris sequence]])**

Given $E^\bullet$ an unreduced cohomology theory, def. \ref{GeneralizedCohomologyTheory}. Given a topological space covered by the [[interior]] of two spaces as $X = Int(A) \cup Int(B)$, then for each $C \subset A \cap B$ there is a [[long exact sequence]] of cohomology groups of the form

$$
  \cdots
  \to 
  E^{n-1}(A \cap B , C)
  \overset{\bar \delta}{\longrightarrow}
  E^n(X,C)
  \longrightarrow
  E^n(A,C) \oplus E^n(B,C)
  \longrightarrow
  E^n(A \cap B, C)
  \to
  \cdots
  \,.
$$

=--

e.g. ([Switzer 75, theorem 7.19](#Switzer75), [Aguilar-Gitler-Prieto 02, theorem 12.1.22](#AguilarGitlerPrieto02))


## Relation between reduced and unreduced cohomology
 {#RelationBetweenReducedAndUnreduced}

+-- {: .num_defn #FromUnreducedToReducedCohomology}
###### Definition
**(unreduced to reduced cohomology)**

Let $E^\bullet$ be an unreduced cohomology theory, def. \ref{GeneralizedCohomologyTheory}. Define a reduced cohomology theory, def. \ref{ReducedGeneralizedCohomology} $(\tilde E^\bullet, \sigma)$ as follows.

For $x \colon \ast \to X$ a [[pointed topological space]], set

$$
  \tilde E^\bullet(X,x) \coloneqq E^\bullet(X,\{x\})
  \,.
$$

This is clearly [[functor|functorial]]. Take the [[suspension isomorphism]] to be the composite

$$
  \sigma 
   \;\colon\;
  \tilde E^{\bullet+1}(\Sigma X)
   =
  E^{\bullet+1}(\Sigma X, \{x\})
   \overset{E^\bullet(p)}{\longrightarrow}
  E^{\bullet+1}(Cone(X),X)
    \overset{\bar \delta^{-1}}{\longrightarrow}
  E^\bullet(X,\{x\})
   =
  \tilde E^{\bullet}(X)
$$

of the isomorphism $E^\bullet(p)$ from example \ref{GeneralizedCohomologyOnHomotopyQuotientMaps} and the [[inverse]] of the isomorphism $\bar \delta$ from example \ref{ExtractingSuspensionIsomorphismFromUnreducedCohomology}.

=--

+-- {: .num_prop}
###### Proposition

The construction in def. \ref{FromUnreducedToReducedCohomology} indeed gives a reduced cohomology theory.

=--

(e.g. [Switzer 75, 7.34](#Switzer75))

+-- {: .proof}
###### Proof

We need to check the exactness axiom given any $A\hookrightarrow X$. By lemma \ref{EvaluationOfCohomologyTheoryOnGoodPairIsEvaluationOnQuotient} we have an isomorphism

$$
  \tilde E^\bullet(X \cup Cone(A))
  =
  E^\bullet(X \cup Cone(A), \{\ast\})
    \overset{\simeq}{\longrightarrow}
  E^\bullet(X,A)
  \,.
$$

Unwinding the constructions shows that this makes the following [[commuting diagram|diagram commute]]:

$$
  \array{
     \tilde E^\bullet(X\cup Cone(A)) 
        &\overset{\simeq}{\longrightarrow}&
     E^\bullet(X,A)
     \\
     \downarrow && \downarrow
     \\
     \tilde E^\bullet(X) &=& E^\bullet(X,\{x\})
     \\
     \downarrow && \downarrow
     \\
     \tilde E^\bullet(A) &=& E^\bullet(A,\{a\})
  }
  \,,
$$

where the vertical sequence on the right is exact by prop. \ref{ExactSequenceOfATriple}. Hence the left vertical sequence is exact.

=--


+-- {: .num_defn #ReducedToUnreducedGeneralizedCohomology}
###### Definition
**(reduced to unreduced cohomology)**

Let $(\tilde E^\bullet, \sigma)$ be a reduced cohomology theory, def. \ref{ReducedGeneralizedCohomology}. Define an unreduced cohomolog theory $E^\bullet$, def. \ref{GeneralizedCohomologyTheory}, by 

$$
  E^\bullet(X,A)
  \coloneqq
  \tilde E^\bullet( X_+ \cup Cone(A_+))
$$

and let the connecting homomorphism be as in def. \ref{ConnectinHomomorphismForCohomologyTheoryOnInfinityCategory}.

=--
+-- {: .num_prop}
###### Proposition

The construction in def. \ref{ReducedToUnreducedGeneralizedCohomology} indeed yields an unreduced cohomology theory.

=--

e.g. ([Switzer 75, 7.35](#Switzer75))

+-- {: .proof}
###### Proof

Exactness holds by prop. \ref{LongExactSequenceOfACohomologyTheoryOnAnInfinityCategory}. For excision, it is sufficient to consider the alternative formulation of lemma \ref{AlternativeFormulationOfExcisionAxiom}.  For CW-inclusions, this follows immediately with lemma \ref{EvaluationOfCohomologyTheoryOnGoodPairIsEvaluationOnQuotient}.

=--

+-- {: .num_theorem}
###### Theorem

The constructions of def. \ref{ReducedToUnreducedGeneralizedCohomology} and def. \ref{FromUnreducedToReducedCohomology} constitute a pair of [[functors]] between then [[categories]] of reduced cohomology theories, def. \ref{ReducedGeneralizedCohomology} and unreduced cohomology theories, def. \ref{GeneralizedCohomologyTheory} which exhbit an [[equivalence of categories]].

=--

+-- {: .proof}
###### Proof

(...careful with checking the respect for suspension iso and connecting homomorphism..)

To see that there are [[natural isomorphisms]] relating the two composites of these two functors to the identity:

One composite is

$$
  \begin{aligned}
    E^\bullet 
    & \mapsto
    (\tilde E^\bullet \colon (X,x) \mapsto E^\bullet(X,\{x\})) 
    \\
    & \mapsto
    ((E')^\bullet \colon (X,A) \mapsto E^\bullet( X_+ \cup Cone(A_+) ), \ast)
  \end{aligned}
  \,,
$$

where on the right we have, from the construction, the reduced mapping cone of the original inclusion $A \hookrightarrow X$ with a base point adjoined. That however is isomorphic to the unreduced mapping cone of the original inclusion. With this the natural isomorphism is given by lemma \ref{EvaluationOfCohomologyTheoryOnGoodPairIsEvaluationOnQuotient}.

The other composite is

$$
  \begin{aligned}
    \tilde E^\bullet
     & \mapsto
    (E^\bullet \colon (X,A) \mapsto \tilde E^\bullet(X_+ \cup Cone(A_+)))
    \\
    & \mapsto 
    ((\tilde E')^\bullet \colon X \mapsto \tilde E^\bullet(X_+ \cup Cone(*_+)))
  \end{aligned}
$$

where on the right we have the reduced mapping cone of the point inclusion with a point adoined. As before, this is isomorphic to the unreduced mapping cone of the point inclusion. That finally is clearly homotopy equivalent to $X$, and so now the natural isomorphism follows with homotopy invariance.
 
=--

Finally we record the following basic relation between reduced and unreduced cohomology:

+-- {: .num_prop #UnreducedCohomologyIsReducedPlusPointValue}
###### Proposition

Let $E^\bullet$ be an unreduced cohomology theory, and $\tilde E^\bullet$ its reduced cohomology theory from def. \ref{FromUnreducedToReducedCohomology}. For $(X,\ast)$ a pointed topological space, then there is an identification

$$
  E^\bullet(X) \simeq \tilde E^\bullet(X) \oplus E^\bullet(\ast)
$$

of the unreduced cohomology of $X$ with the [[direct sum]] of the reduced cohomology of $X$ and the unreduced cohomology of the base point.

=--

+-- {: .proof}
###### Proof

The pair $\ast \hookrightarrow X$ induces the sequence

$$
  \cdots
   \to 
  E^{\bullet-1}(\ast)
    \stackrel{\delta}{\longrightarrow}
  \tilde E^\bullet(X)
    \stackrel{}{\longrightarrow}
  E^\bullet(X) 
    \stackrel{}{\longrightarrow}
  E^\bullet(\ast)
    \stackrel{\delta}{\longrightarrow}
  \tilde E^{\bullet+1}(X)
    \to
  \cdots
$$

which by the exactness clause in def. \ref{GeneralizedCohomologyTheory} is [[exact sequence|exact]]. 

Now since the composite $\ast \to X \to \ast$ is the identity, the morphism 
$E^\bullet(X) \to E^\bullet(\ast)$ has a [[section]] and so is in particular an [[epimorphism]]. Therefore, by exactness, the [[connecting homomorphism]] vanishes, $\delta = 0$ and we have a [[short exact sequence]]

$$
  0 
    \to 
  \tilde E^\bullet(X)
    \stackrel{}{\longrightarrow}
  E^\bullet(X) 
    \stackrel{}{\longrightarrow}
  E^\bullet(\ast)
    \to
  0
$$

with the right map an epimorphism. Hence this is a [[split exact sequence]] and the statement follows.


=--







## Brown functoriality

+-- {: .num_prop }
###### Proposition

Given a generalized cohomology functor $E^\bullet \colon Ho(\mathcal{C})^{op}\to Ab^{\mathbb{Z}}$, def. \ref{GeneralizedCohomologyOnGeneralInfinityCategory}, its underlying [[Set]]-valued functors $H^n \colon Ho(\mathcal{C})^{op}\to Ab\to Set$ are [[Brown functors]], def. \ref{BrownFunctorOnInfinityCategory}.

=--

+-- {: .proof}
###### Proof


The first condition on a [[Brown functor]] holds by definition of $H^\bullet$. For the second condition, given a homotopy pushout square


$$
  \array{
    X_1 &\stackrel{f_1}{\longrightarrow}& Y_1
    \\
    \downarrow^{} && \downarrow
    \\
    X_2 &\stackrel{f_2}{\longrightarrow}& Y_2
  }
$$

in $\mathcal{C}$, consider the induced morphism of the [[long exact sequences]] given by prop. \ref{LongExactSequenceOfACohomologyTheoryOnAnInfinityCategory}

$$
  \array{
    H^\bullet(coker(f_2))
      &\longrightarrow&
    H^\bullet(Y_2) 
      &\stackrel{f^\ast_2}{\longrightarrow}& 
    H^\bullet(X_2)
      &\stackrel{}{\longrightarrow}&
    H^{\bullet+1}(\Sigma coker(f_2))
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow && \downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    H^\bullet(coker(f_1))
      &\longrightarrow&
    H^\bullet(Y_1) 
      &\stackrel{f^\ast_1}{\longrightarrow}& 
    H^\bullet(X_1)
      &\stackrel{}{\longrightarrow}&
    H^{\bullet+1}(\Sigma coker(f_1))
  }
$$

Here the outer vertical morphisms are [[isomorphisms]], as shown, due to the [[pasting law]] (see also at _[fiberwise recognition of stable homotopy pushouts](homotopy+pullback#FiberwiseRecognitionInStableCase)_). 

This means that the [[four lemma]] applies to this diagram. Inspection shows that this implies the claim.

=--

## Examples 


* [[ordinary cohomology]]: [[Eilenberg-Mac Lane spectrum]]

* [[K-theory]]: [[K-theory spectrum]]
* [[tmf]]

* [[cobordism cohomology theory]]

* [[Morava K-theory]], [[integral Morava K-theory]]

* [[Morava E-theory]]

* [[stable cohomotopy]]



## Properties



### Expression by ordinary cohomology via Atiyah-Hirzebruch spectral sequence

The [[Atiyah-Hirzebruch spectral sequence]] serves to express generalized cohomology $E^\bullet$ in terms of ordinary cohomology with coefficients in $E^\bullet(\ast)$.

### Whitehead theorem
 {#WhiteheadTheorem}

+-- {: .num_prop}
###### Proposition

Let $\phi \colon E \longrightarrow F$ be a morphism of reduced generalized (co-)homology functors, def. \ref{ReducedGeneralizedCohomology} (a [[natural transformation]]) such that its component

$$
  \phi(S^0) \colon E(S^0) \longrightarrow F(S^0)
$$

on the [[0-sphere]] is an [[isomorphism]]. Then $\phi(X)\colon E(X)\to F(X)$ is an [[isomorphism]] for $X$ any [[CW-complex]] with a [[finite number]] of cells. If both $E$ and $F$ satisfy the [[wedge axiom]], then $\phi(X)$ is an isomorphism for $X$ any [[CW-complex]], not necessarily finite.

=--


For $E$ and $F$ [[ordinary cohomology]]/[[ordinary homology]] functors a proof of this is in ([Eilenberg-Steenrod 52, section III.10](#EilenbergSteenrod52)). From this the general statement follows (e.g. [Kochman 96, theorem 3.4.3, corollary 4.2.8](#Kochman96)) via the [[natural transformation|naturality]] of the [[Atiyah-Hirzebruch spectral sequence]] (the classical result gives that $\phi$ induces an isomorphism between the second pages of the AHSSs for $E$ and $F$). A complete proof of the general result is also given as ([Switzer 75, theorem 7.55, theorem 7.67](#Switzer75))


## Related concepts

* [[Brown representability theorem]]

* [[generalized homology theory]]

* [[Kronecker pairing]]

* [[bivariant cohomology theory]]

* [[multiplicative cohomology theory]]

[[!include twisted generalized cohomology in linear homotopy type theory -- table]]



## References 

The axioms including the dimension axiom are due to 

* {#EilenbergSteenrod52} [[Samuel Eilenberg]], [[Norman Steenrod]], _Foundations of algebraic topology_, Princeton 1952 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/eilestee.pdf))

The concept of generalized homology obtained by discarding the dimension axiom and the observation that every [[spectrum]] induces an example is due to

* {#Whitehead62} [[George Whitehead]], _Generalized homology theories_, Transactions of the American Mathematical Society, 102 (1962) 227-283 ([pdf](http://www.ams.org/journals/tran/1962-102-02/S0002-9947-1962-0137117-6/S0002-9947-1962-0137117-6.pdf), [jstor:1993676](https://www.jstor.org/stable/1993676))


The proof that every generalized (co)homology theory arises this way ([[Brown representability theorem]]) is due to

* {#Brown62} [[Edgar Brown]], _Cohomology theories_, Annals of Mathematics, Second Series 75: 467&#8211;484 (1962)

* {#Brown65} [[Edgar Brown]], _Abstract homotopy theory_, Trans. AMS 119 no. 1 (1965)

An early lecture note account is in

* {#Adams74} [[Frank Adams]], part III, sections 2 and 6 of _[[Stable homotopy and generalised homology]]_, 1974

Textbook accounts include

* {#Switzer75} [[Robert Switzer]], chapter 7 (and 8-12) of _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 


* {#Kochman96} [[Stanley Kochman]], section 3.4 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#May99} [[Peter May]] chapter 18 of _A Concise Course on Algebraic Topology_, Chicago Lecture Notes  1999 ([pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))


* {#AguilarGitlerPrieto02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 12.1 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

* {#KonoTamaki02} [[Akira Kono]], [[Dai Tamaki]], _Generalized cohomology_, AMS 2002, esp. chapter 2 ([[GeneralizedCohomology.pdf:file]])

* [[Stefan Schwede]], chapter II, section 6 of  _[[Symmetric spectra]]_, 2012  ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

Discussion in the further generality of [[equivariant cohomology]] is in

* {#tomDieck79} [[Tammo tom Dieck]], section 7 of _[[Transformation Groups and Representation Theory]]_, Lecture Notes in Mathematics 766, Springer 1979


A pedagogical introduction to [[spectrum|spectra]] and generalized (Eilenberg-Steenrod) cohomology is in

* [[John Baez]], [TWF 149](http://math.ucr.edu/home/baez/twf_ascii/week149) 

Formulation in [[(infinity,1)-category theory]] is in

* {#LurieHigherAlgebra} [[Jacob Lurie]], section 1.4.1 of _[[Higher Algebra]]_

More references relating to the [[nPOV]] on cohomology include:

* [[Mike Hopkins]], _[[Complex oriented cohomology theories and the language of stacks]]_ course notes ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/coctalos.pdf))

* [[Jacob Lurie]],  _[[A Survey of Elliptic Cohomology - cohomology theories]]_

Formulation in [[homotopy type theory]]:

* [[Evan Cavallo]], _Synthetic Cohomology in Homotopy Type Theory_ MSc Thesis 2015 ([pdf](https://www.cs.cmu.edu/~rwh/theses/cavallo-msc.pdf))


[[!redirects generalized Eilenberg-Steenrod cohomology]]
[[!redirects generalized Eilenberg?Steenrod cohomology]]
[[!redirects generalized (Eilenberg?Steenrod) cohomology]]
[[!redirects generalized (Eilenberg--Steenrod) cohomology]]
[[!redirects generalized (Eilenberg-Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg?Steenrod) cohomology theory]]

[[!redirects generalized (Eilenberg--Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg--Steenrod) cohomology theories]]
[[!redirects generalized (Eilenberg-Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg-Steenrod) cohomology theories]]

[[!redirects generalised (Eilenberg-Steenrod) cohomology]]
[[!redirects generalised (Eilenberg?Steenrod) cohomology]]
[[!redirects generalised (Eilenberg--Steenrod) cohomology]]
[[!redirects generalised (Eilenberg-Steenrod) cohomology theory]]
[[!redirects generalised (Eilenberg?Steenrod) cohomology theory]]
[[!redirects generalised (Eilenberg--Steenrod) cohomology theory]]
[[!redirects Eilenberg-Steenrod cohomology]]
[[!redirects Eilenberg?Steenrod cohomology]]
[[!redirects Eilenberg--Steenrod cohomology]]
[[!redirects Eilenberg-Steenrod cohomology theory]]
[[!redirects Eilenberg?Steenrod cohomology theory]]
[[!redirects Eilenberg--Steenrod cohomology theory]]

[[!redirects Eilenberg-Steenrod axioms]]

[[!redirects generalized (Eilenberg-Steenrod) cohomology theory]]
[[!redirects generalized (Eilenberg-Steenrod) cohomology theories]]

[[!redirects generalized (Eilenberg-Steenrod) cohomlogy theory]]
[[!redirects generalized (Eilenberg-Steenrod) cohomlogy theories]]

[[!redirects extraordinary cohomology theory]]
[[!redirects extraordinary cohomology theories]]

[[!redirects Eilenberg–Steenrod cohomology theory]]
[[!redirects Eilenberg–Steenrod cohomology theories]]
