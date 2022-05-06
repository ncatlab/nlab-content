
{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

***

$\,$

This page collects introductory seminar notes to the concepts of [[generalized (Eilenberg-Steenrod) cohomology theory]], basics of [[cobordism theory]] and [[complex oriented cohomology]].


$\,$

_The [[category]] of those [[generalized cohomology theories]] that are equipped with a universal "[[complex oriented cohomology theory|complex]] [[orientation in generalized cohomology|orientation]]" happens to unify within it the abstract structure theory of [[stable homotopy theory]] with the concrete richness of the [[differential topology]] of [[cobordism theory]] and of the [[arithmetic geometry]] of [[formal group laws]], such as [[elliptic curves]]. In the seminar we work through classical results in [[algebraic topology]], organized such as to give in the end a first glimpse of the modern picture of [[chromatic homotopy theory]]._



$\,$

For background on [[stable homotopy theory]] see _[[Introduction to Stable homotopy theory]]_.

For application to/of the [[Adams spectral sequence]] see _[[Introduction to the Adams Spectral Sequence]]_

$\,$

***

$\,$


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


$\,$

**Outline.** We start with two classical topics of [[algebraic topology]] that first run independently in parallel:

* [1) Generalized cohomology](#S1GeneralizedCohomology)

* [2) Cobordism theory](#S2CobordismTheory)

The development of either of these happens to give rise to the concept of _[[spectra]]_ and via this concept it turns out that both topics are intimately related. The unification of both is our third topic

* [3) Complex oriented cohomology](#ComplexOrientedCohomologyTheory)

$\,$

**Literature.** ([Kochman 96](#Kochman96)).


##  Generalized cohomology
 {#S1GeneralizedCohomology}

**Idea.** The concept that makes [[algebraic topology]] be about methods of [[homological algebra]] applied to [[topology]] is that of [[generalized homology]] and [[generalized cohomology]]: these are [[covariant functors]] or [[contravariant functors]], respectively,

$$
  Spaces \longrightarrow Ab^{\mathbb{Z}}
$$

from (sufficiently nice) [[topological spaces]] to $\mathbb{Z}$-[[graded abelian groups]], such that a few key properties of the [[homotopy types]] of topological spaces is preserved as one passes them from [[Ho(Top)]] to the much more tractable [[abelian category]] [[Ab]].

**Literature.** ([Aguilar-Gitler-Prieto 02, chapters 7,8 and 12](#AguilarGitlerPrieto02), [Kochman 96, 3.4, 4.2](#Kochman96), [Schwede 12, II.6](#Schwede12))



### Generalized cohomology functors
 {#GeneralizedHomologyAndCohomologyFunctors}

**Idea.** A [[generalized (Eilenberg-Steenrod) cohomology]] theory is such a contravariant functor which satisfies the key properties exhibited by [[ordinary cohomology]] (as computed for instance by [[singular cohomology]]), notably [[homotopy invariance]] and [[excision]], _except_ that its value on the point is not required to be concentrated in degree 0. Dually for [[generalized homology]]. There are two versions of the axioms, one for [[reduced cohomology]], and they are equivalent if properly set up.

An important example of a generalised cohomology theory other than [[ordinary cohomology]] is [[topological K-theory]]. The other two examples of key relevance below are [[cobordism cohomology]] and [[stable cohomotopy]].

**Literature.** ([Switzer 75, section 7](#Switzer75), [Aguilar-Gitler-Prieto 02, section 12 and section 9](#AguilarGitlerPrieto02), [Kochman 96, 3.4](#Kochman96)).


$\,$

#### Reduced cohomology


The traditional formulation of reduced generalized cohomology in terms of point-set topology is this:

+-- {: .num_defn #ReducedGeneralizedCohomology}
###### Definition

A **[[reduced cohomology theory]]** is

1. a [[functor]]

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

1. {#SuspensionIsomorphismForReducedGeneralizedCohomology} equipped with a [[natural isomorphism]] of degree +1, to be called the **[[suspension isomorphism]]**, of the form

   $$
     \sigma_E
       \;\colon\;
     \tilde E^\bullet(-)
       \overset{\simeq}{\longrightarrow}
     \tilde E^{\bullet +1}(\Sigma -)
   $$

such that:

1. **([[homotopy invariance]])** If $f_1,f_2 \colon X \longrightarrow Y$ are two morphisms of pointed topological spaces such that there is a (base point preserving) [[homotopy]] $f_1 \simeq f_2$ between them, then the induced [[homomorphisms]] of abelian groups are [[equality|equal]]

   $$
     f_1^\ast = f_2^\ast
     \,.
   $$

1. {#ReducedExactnessAxiom} **(exactness)** For $i \colon A \hookrightarrow X$ an inclusion of pointed topological spaces, with $j \colon X \longrightarrow Cone(i)$ the induced [[mapping cone]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#ConeAndMappingCylinder)), then this gives an [[exact sequence]] of graded abelian groups

   $$
     \tilde E^\bullet(Cone(i))
      \overset{j^\ast}{\longrightarrow}
     \tilde E^\bullet(X)
       \overset{i^\ast}{\longrightarrow}
     \tilde E^\bullet(A)
     \,.
   $$

=--

(e.g. [AGP 02, def. 12.1.4](#AguilarGitlerPrieto02))


This is equivalent (prop. \ref{HomotopyTheoreticVersionOfCohomologyFunctorDefIsEquivalent} below) to the following more succinct homotopy-theoretic definition:

+-- {: .num_defn #ReducedGeneralizedCohomologyHomotopyTheoretically}
###### Definition

A **reduced [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology theory]]** is a [[functor]]

$$
  \tilde E^\bullet
   \;\colon\;
  Ho(Top^{\ast/})^{op} \longrightarrow Ab^{\mathbb{Z}}
$$

from the [[opposite category|opposite]] of the pointed [[classical homotopy category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalHomotopyCategory), [def.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalPointedHomotopyCategory)), to $\mathbb{Z}$-[[graded abelian groups]], and equipped with [[natural isomorphisms]], to be called the **[[suspension isomorphism]]** of the form

$$
  \sigma
    \;\colon\;
  \tilde E^{\bullet +1}(\Sigma -)
    \overset{\simeq}{\longrightarrow}
  \tilde E^\bullet(-)
$$

such that:

* **(exactness)** it takes [[homotopy cofiber]] sequences in $Ho(Top^{\ast/})$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyFiber)) to [[exact sequence|exact sequences]].


=--

As a consequence (prop. \ref{HomotopyTheoreticVersionOfCohomologyFunctorDefIsEquivalent} below), we find yet another equivalent definition:

+-- {: .num_defn #ReducedGeneralizedCohomologyHomotopyHomotopicalFunctor}
###### Definition

A **reduced [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology theory]]** is a [[functor]]

$$
  \tilde E^\bullet
   \;\colon\;
  (Top^{\ast/})^{op} \longrightarrow Ab^{\mathbb{Z}}
$$

from the [[opposite category|opposite]] of the category of [[pointed topological spaces]] to $\mathbb{Z}$-[[graded abelian groups]], such that

* **(WHE)** it takes [[weak homotopy equivalences]] to isomorphisms

and equipped with [[natural isomorphism]], to be called the **[[suspension isomorphism]]** of the form

$$
  \sigma
    \;\colon\;
  \tilde E^{\bullet +1}(\Sigma -)
    \overset{\simeq}{\longrightarrow}
  \tilde E^\bullet(-)
$$

such that

* **(exactness)** it takes [[homotopy cofiber]] sequences in $Ho(Top^{\ast/})$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyFiber)), to [[exact sequence|exact sequences]].

=--

+-- {: .num_prop #HomotopyTheoreticVersionOfCohomologyFunctorDefIsEquivalent}
###### Proposition

The three definitions

* def. \ref{ReducedGeneralizedCohomology}

* def. \ref{ReducedGeneralizedCohomologyHomotopyTheoretically}

* def. \ref{ReducedGeneralizedCohomologyHomotopyHomotopicalFunctor}

are indeed equivalent.

=--

+-- {: .proof}
###### Proof

Regarding the equivalence of def. \ref{ReducedGeneralizedCohomology} with def. \ref{ReducedGeneralizedCohomologyHomotopyTheoretically}:

By the existence of the [[classical model structure on topological spaces]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#TopQuillenModelStructure)), the characterization of its [[homotopy category of a model category|homotopy category]] ([cor.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects)) and the existence of [[CW-approximations]], the homotopy invariance axiom in def. \ref{ReducedGeneralizedCohomology} is equivalent to the functor passing to the classical pointed homotopy category. In view of this and since on CW-complexes the standard topological mapping cone construction is a model for the [[homotopy cofiber]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#StandardTopologicalMappingConeIsHomotopyCofiber)), this gives the equivalence of the two versions of the exactness axiom.

Regarding the equivalence of def. \ref{ReducedGeneralizedCohomologyHomotopyTheoretically} with def. \ref{ReducedGeneralizedCohomologyHomotopyHomotopicalFunctor}:

This is the [[universal property]] of the [[classical homotopy category]]  ([thm.](Introduction+to+Stable+homotopy+theory+--+P#UniversalPropertyOfHomotopyCategoryOfAModelCategory)) which identifies it  with the [[localization]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfACategoryWithWeakEquivalences)) of $Top^{\ast/}$ at the weak homotopy equivalences ([thm.](Introduction+to+Stable+homotopy+theory+--+P#TopQuillenModelStructure)), together with the existence of [[CW approximations]] ([rmk.](Introduction+to+Stable+homotopy+theory+--+P#EveryTopologicalSpaceWeaklyEquivalentToACWComplex)): jointly this says that, up to [[natural isomorphism]], there is a bijection between functors $F$ and $\tilde F$ in the following diagram (which is filled by a natural isomorphism itself):

$$
  \array{
    Top^{op} &\overset{F}{\longrightarrow}& Ab^{\mathbb{Z}}
    \\
    {}^{\mathllap{\gamma_{Top}}}\downarrow & \nearrow_{\mathrlap{\tilde F}}
    \\
    Ho(Top)^{op}\simeq (Top_{CW})/_\sim
  }
$$

where $F$ sends weak homotopy equivalences to isomorphisms and where $(-)_\sim$ means identifying homotopic maps.


=--

Prop. \ref{HomotopyTheoreticVersionOfCohomologyFunctorDefIsEquivalent} naturally suggests (e.g. [Lurie 10, section 1.4](#LurieHigherAlgebra)) that the concept of generalized cohomology be formulated in the generality of any abstract homotopy theory ([[model category]]), not necessarily that of (pointed) topological spaces:

+-- {: .num_defn #GeneralizedCohomologyOnGeneralInfinityCategory}
###### Definition

Let $\mathcal{C}$ be a [[model category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#ModelCategory)) with $\mathcal{C}^{\ast/}$ its [[slice model structure|pointed model category]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#ModelStructureOnSliceCategory)).

A **reduced additive [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology theory]] ** on $\mathcal{C}$ is

1. a [[functor]]

   $$
     \tilde E^\bullet \;\colon \; Ho(\mathcal{C}^{\ast/})^{op} \longrightarrow Ab^{\mathbb{Z}}
   $$

1. a [[natural isomorphism]] ("[[suspension isomorphisms]]") of degree +1

   $$
     \sigma \; \colon \; \tilde E^\bullet \longrightarrow \tilde E^{\bullet+1} \circ \Sigma
   $$

such that

* **(exactness)** $\tilde E^\bullet$ takes [[homotopy cofiber sequences]] to [[exact sequences]].

=--

Finally we need the following terminology:

+-- {: .num_defn #AdditiveOrdinary}
###### Definition

Let $\tilde E^\bullet$ be a [[reduced cohomology theory]] according to either of def. \ref{ReducedGeneralizedCohomology}, def. \ref{ReducedGeneralizedCohomologyHomotopyTheoretically}, def. \ref{ReducedGeneralizedCohomologyHomotopyHomotopicalFunctor} or def. \ref{GeneralizedCohomologyOnGeneralInfinityCategory}.

We say $\tilde E^\bullet$ is **additive** if in addition

* {#WedgeAxiom} **([[wedge axiom]])** For $\{X_i\}_{i \in I} $ any set of pointed CW-complexes, then the canonical morphism

  $$
    \tilde E^\bullet(\vee_{i \in I} X_i)
    \longrightarrow
    \prod_{i \in I} \tilde E^\bullet(X_i)
  $$

  from the functor applied to their [[wedge sum]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#WedgeSumAsCoproduct)), to the [[product]] of its values on the wedge summands, is an [[isomorphism]].

We say $\tilde E^\bullet$ is **ordinary** if its value on the [[0-sphere]] $S^0$ is concentrated in degree 0:

* **(Dimension)**  $\tilde E^{\bullet\neq 0}(\mathbb{S}^0) \simeq 0$.

If $\tilde E^\bullet$ is not ordinary, one also says that it is **generalized** or **extraordinary**.

A **[[homomorphism]] of reduced cohomology theories**

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

We now discuss some constructions and consequences implied by the concept of reduced cohomology theories:

+-- {: .num_defn #ConnectinHomomorphismForCohomologyTheoryOnInfinityCategory}
###### Definition

Given a generalized cohomology theory $(E^\bullet,\delta)$ on some $\mathcal{C}$ as in def. \ref{GeneralizedCohomologyOnGeneralInfinityCategory}, and given a [[homotopy cofiber sequence]] in $\mathcal{C}$ ([prop.](Introduction+to+Stable+homotopy+theory+--+P#LongFiberSequence)),

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




#### Unreduced cohomology

Given a reduced [[generalized cohomology theory]] as in def. \ref{ReducedGeneralizedCohomology}, we may "un-reduce" it and evaluate it on unpointed topological spaces $X$ simply by evaluating it on $X_+$ ([def.](Introduction+to+Stable+homotopy+theory+--+P#BasePointAdjoined)). It is conventional to further generalize to [[relative cohomology]] and evaluate on unpointed subspace inclusions $i \colon A \hookrightarrow X$, taken as placeholders for their [[mapping cones]] $Cone(i_+)$ ([prop.](Introduction+to+Stable+homotopy+theory+--+P#UnreducedMappingConeAsReducedConeOfBasedPointAdjoined)).

In the following a _pair_ $(X,U)$ refers to a [[subspace]] inclusion of [[topological spaces]]  $U \hookrightarrow X$.  Whenever only one space is mentioned, the subspace is assumed to be the [[empty set]] $(X, \emptyset)$. Write $Top_{CW}^{\hookrightarrow}$ for the category of such pairs (the [[full subcategory]] of the [[arrow category]] of $Top_{CW}$ on the inclusions). We identify $Top_{CW} \hookrightarrow Top_{CW}^{\hookrightarrow}$ by $X \mapsto (X,\emptyset)$.

+-- {: .num_defn #GeneralizedCohomologyTheory}
###### Definition

A _[[cohomology theory]]_ (unreduced, [[relative cohomology|relative]]) is

1. a [[functor]]

   $$
     E^\bullet : (Top_{CW}^{\hookrightarrow})^{op} \to Ab^{\mathbb{Z}}
   $$

   to the category of $\mathbb{Z}$-[[graded abelian groups]],

1. {#ConnectingHomomorphismOfUnreducedCohomology} a [[natural transformation]] of degree +1, to be called the **[[connecting homomorphism]]**, of the form

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

1. **([[excision]])** For $U \hookrightarrow A \hookrightarrow X$ such that $\overline{U} \subset Int(A)$, then the natural inclusion of the pair $i \colon (X-U, A-U) \hookrightarrow (X, A)$ induces an isomorphism

   $$
     E^\bullet(i)
      \;\colon\;
     E^n(X, A)
      \overset{\simeq}{\longrightarrow}
     E^n(X-U, A-U)
   $$

We say $E^\bullet$ is **additive** if it takes [[coproducts]] to [[products]]:

* {#UnreducedAdditivity} **(additivity)** If $(X, A) = \coprod_i (X_i, A_i)$ is a [[coproduct]], then the canonical comparison morphism

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

between the value of $E^\bullet$ on the pair $(X,A)$ and its value on the unreduced [[mapping cone]] of the inclusion ([rmk.](Introduction+to+Stable+homotopy+theory+--+P#UnreducedCone)), relative to a basepoint.

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

If $A \hookrightarrow X$ is a cofibration, then this is a [[homotopy equivalence]] since $Cone(A)$ is contractible and since by the dual [[factorization lemma]] ([lem.](Introduction+to+Stable+homotopy+theory+--+P#FactorizationLemma)) and by the invariance of homotopy fibers under weak equivalences ([lem.](Introduction+to+Stable+homotopy+theory+--+P#FiberOfFibrationIsCompatibleWithWeakEquivalences)), $X \cup Cone(A)\to X/A$ is a weak homotopy equivalence, hence, by the universal property of the [[classical homotopy category]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#UniversalPropertyOfHomotopyCategoryOfAModelCategory)) a homotopy equivalence on CW-complexes.

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

Apply the [[braid lemma]] to the interlocking long exact sequences of the three pairs $(X,Y)$, $(X,Z)$, $(Y,Z)$:

<img src="http://www.ncatlab.org/nlab/files/BraidDiagramForHomologyOnTripled.jpg" width="500">

(graphics from [this Maths.SE comment](http://math.stackexchange.com/a/1180681/58526), showing the dual situation for homology)

See [here](braid+lemma#ExactSequenceForTripleInGeneralizedHomology) for details.


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





#### Relation between unreduced and reduced cohomology
 {#RelationBetweenUnreducedAndReducedCohomology}

+-- {: .num_defn #FromUnreducedToReducedCohomology}
###### Definition
**(unreduced to reduced cohomology)**

Let $E^\bullet$ be an [[generalized (Eilenberg-Steenrod) cohomology|unreduced cohomology theory]], def. \ref{GeneralizedCohomologyTheory}. Define a reduced cohomology theory, def. \ref{ReducedGeneralizedCohomology} $(\tilde E^\bullet, \sigma)$ as follows.

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

(e.g [Switzer 75, 7.34](#Switzer75))

+-- {: .proof}
###### Proof

We need to check the [exactness axiom](#ExactnessUnreduced) given any $A\hookrightarrow X$. By lemma \ref{EvaluationOfCohomologyTheoryOnGoodPairIsEvaluationOnQuotient} we have an isomorphism

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

Let $(\tilde E^\bullet, \sigma)$ be a [[reduced cohomology theory]], def. \ref{ReducedGeneralizedCohomology}. Define an unreduced cohomolog theory $E^\bullet$, def. \ref{GeneralizedCohomologyTheory}, by

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

where on the right we have, from the construction, the reduced mapping cone of the original inclusion $A \hookrightarrow X$ with a base point adjoined. That however is isomorphic to the unreduced mapping cone of the original inclusion ([prop. ](Introduction+to+Stable+homotopy+theory -- P#UnreducedMappingConeAsReducedConeOfBasedPointAdjoined)). With this the natural isomorphism is given by lemma \ref{EvaluationOfCohomologyTheoryOnGoodPairIsEvaluationOnQuotient}.

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




#### Generalized homology functors

All of the above has a dual version with [[generalized cohomology]] replaced by [[generalized homology]]. For ease of reference, we record these dual definitions:

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

  from the [[direct sum]] of the value on the summands to the value on the [[wedge sum]] ([prop.](Introduction+to+Stable+homotopy+theory -- P#WedgeSumAsCoproduct)), is an [[isomorphism]].

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
  E^\bullet(A, \emptyset)
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

1. **([[excision]])** For $U \hookrightarrow A \hookrightarrow X$ such that $\overline{U} \subset Int(A)$, then the natural inclusion of the pair $i \colon (X-U, A-U) \hookrightarrow (X, A)$ induces an isomorphism

   $$
     E_\bullet(i)
      \;\colon\;
     E_n(X-U, A-U)
      \overset{\simeq}{\longrightarrow}
     E_n(X, A)
   $$

We say $E^\bullet$ is **additive** if it takes [[coproducts]] to [[direct sums]]:

* **(additivity)** If $(X, A) = \coprod_i (X_i, A_i)$ is a [[coproduct]], then the canonical comparison morphism

  $$
    \oplus_i E^n(X_i, A_i) \overset{\simeq}{\longrightarrow} E^n(X, A)
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
     E_\bullet(A,\emptyset) &\overset{\eta_{(A,\emptyset)}}{\longrightarrow}& F^\bullet(A,\emptyset)
  }
  \,.
$$

=--



#### Multiplicative cohomology theories

The [[generalized cohomology theories]] considered above assign _[[cohomology groups]]_. It is familiar from [[ordinary cohomology]] with [[coefficients]] not just in a group but in a [[ring]], that also the cohomology groups inherit compatible ring structure. The generalization of this phenomenon to generalized cohomology theories is captured by the concept of [[multiplicative cohomology theories]]:

+-- {: .num_defn #PairingOfUnreducedCohomologyTheories}
###### Definition

Let $E_1, E_2, E_3$ be three unreduced [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology theories]] ([def.](generalized+cohomology+theory#GeneralizedCohomologyTheory)). A **pairing of cohomology theories**

$$
  \mu \;\colon\; E_1 \Box E_2 \longrightarrow E_3
$$

is a [[natural transformation]] (of functors on $(Top_{CW}^{\hookrightarrow}\times Top_{CW}^{\hookrightarrow})^{op} $) of the form

$$
  \mu_{n_1,n_2}
   \;\colon\;
  E_1^{n_1}(X,A)
    \otimes
  E_2^{n_2}(Y,B)
    \longrightarrow
  E_3^{n_1 + n_2}(X\times Y \;,\; A\times Y \cup X \times B)
$$

such that this is compatible with the connecting homomorphisms $\delta_i$ of $E_i$, in that the following are [[commuting squares]]

$$
  \array{
    E_1^{n_1}(A)
      \otimes
    E_2^{n_2}(Y,B)
      &\overset{\delta_1 \otimes id_2}{\longrightarrow}&
    E_1^{n_1+1}(X,A) \otimes E_2^{n_2}(Y,B)
    \\
    {}^{\mathllap{\mu_{n_1,n_2}}}\downarrow && \downarrow^{\mathrlap{\mu_{n_1+1, n_2}}}
    \\
   \underoverset
     {E_3^{n_1 + n_2}(A \times Y  \cup  X \times B , X \times B)}
     {E_3^{n_1 + n_2}(A \times Y, A \times B)}
     {\simeq}
     &\overset{\delta_3}{\longrightarrow}&
     E_3^{n_1 + n_2+ 1}(X \times Y, A \times B)
  }
$$

and

$$
  \array{
    E_1^{n_1}(X,A)
      \otimes
    E_2^{n_2}(B)
      &\overset{(-1)^{n_1} id_1 \otimes \delta_2}{\longrightarrow}&
    E_1^{n_1+1}(X,A) \otimes E_2^{n_2}(Y,B)
    \\
    {}^{\mathllap{\mu_{n_1,n_2}}}\downarrow
      &&
    \downarrow^{\mathrlap{\mu_{n_1, n_2 + 1}}}
    \\
   \underoverset
     {E_3^{n_1 + n_2}(A \times Y \cup X \times B , A \times Y)}
     {E_3^{n_1 + n_2}(X \times B, A \times B)}
     {\simeq}
     &\overset{\delta_3}{\longrightarrow}&
     E_3^{n_1 + n_2+ 1}(X \times Y, A \times B)
  }
  \,,
$$

where the isomorphisms in the bottom left are the [excision isomorphisms](generalized+cohomology+theory##excision).

=--

+-- {: .num_defn #MultiplicativeCohomologyTheory}
###### Definition

An (unreduced) **multiplicative cohomology theory** is an unreduced [[generalized cohomology theory]] theory $E$ (def. \ref{GeneralizedCohomologyTheory}) equipped with

1. (external multiplication) a pairing (def. \ref{PairingOfUnreducedCohomologyTheories}) of the form $\mu \;\colon\; E \Box E  \longrightarrow E$;

1. (unit) an element $1 \in E^0(\ast)$

such that

1. ([[associativity]]) $\mu \circ (id \otimes \mu) = \mu \circ (\mu \otimes id)$;

2. ([[unitality]]) $\mu(1\otimes x) = \mu(x \otimes 1) = x$ for all $x \in E^n(X,A)$.

The mulitplicative cohomology theory is called **commutative** (often considered by default) if in addition

* **(graded commutativity)**

  $$
    \array{
      E^{n_1}(X,A) \otimes E^{n_2}(Y,B)
      &\overset{(u \otimes v) \mapsto (-1)^{n_1 n_2} (v \otimes u) }{\longrightarrow}&
      E^{n_2}(Y,B) \otimes E^{n_1}_{X,A}
      \\
      {}^{\mathllap{\mu_{n_1,n_2}}}\downarrow && \downarrow^{\mathrlap{\mu_{n_2,n_1}}}
      \\
      E^{n_1 + n_2}( X \times Y , A \times Y \cup X \times B)
      &\underset{(switch_{(X,A), (Y,B)})^\ast}{\longrightarrow}&
      E^{n_1 + n_2}( Y \times X , B \times X \cup Y \times A)
    }
    \,.
  $$

{#InternalMultiplicationOfMultiplicativeCohomologyTheory} Given a multiplicative cohomology theory $(E, \mu, 1)$, its **[[cup product]]** is the composite of the above external multiplication with pullback along the [[diagonal]] maps $\Delta_{(X,A)} \colon (X,A) \longrightarrow (X\times X, A \times X \cup X \times A)$;

$$
  (-) \cup (-)
   \;\colon\;
  E^{n_1}(X,A)
   \otimes
  E^{n_2}(X,A)
    \overset{\mu_{n_1,n_2}}{\longrightarrow}
  E^{n_1 + n_2}( X \times X, \; A \times X \cup X \times A)
    \overset{\Delta^\ast_{(X,A)}}{\longrightarrow}
  E^{n_1 + n_2}(X, \; A \cup B)
  \,.
$$

=--

e.g. ([Tamaki-Kono 06, II.6](multiplicative+cohomology+theory#TamakiKono06))

+-- {: .num_prop #RingAndModuleStructureOnCohomologyGroupsOfMultiplicativeCohomplogyTheory}
###### Proposition

Let $(E,\mu,1)$ be a multiplicative cohomology theory, def. \ref{MultiplicativeCohomologyTheory}. Then

1. For every space $X$ the [cup product](#InternalMultiplicationOfMultiplicativeCohomologyTheory) gives $E^\bullet(X)$ the structure of a $\mathbb{Z}$-[[graded ring]], which is graded-commutative if $(E,\mu,1)$ is commutative.

1. For every pair $(X,A)$ the external multiplication $\mu$ gives $E^\bullet(X,A)$ the structure of a left and right [[module]] over the graded ring $E^\bullet(\ast)$.

1. All pullback morphisms respect the left and right action of $E^\bullet(\ast)$ and the connecting homomorphisms respect the right action and the left action up to multiplication by $(-1)^{n_1}$

=--

+-- {: .proof}
###### Proof

Regarding the third point:

For pullback maps this is the [[natural transformation|naturality]] of the external product: let $f \colon (X,A) \longrightarrow (Y,B)$ be a morphism in $Top_{CW}^{\hookrightarrow}$ then naturality says that the following square commutes:

$$
  \array{
    E^{n_1}(\ast) \otimes E^{n_2}(Y,B)
    &\overset{\mu_{n_1,n_2}}{\longrightarrow}&
    E^{n_1 + n_2}(Y, B)
    \\
    {}^{\mathllap{(id,f^\ast)}}\downarrow && \downarrow^{\mathrlap{f^\ast}}
    \\
    E^{n_1}(\ast) \otimes E^{n_2}(X,A)
    &\overset{\mu_{n_1,n_2}}{\longrightarrow}&
    E^{n_1 + n_2}(Y,B)
  }
  \,.
$$

For connecting homomorphisms this is the (graded) commutativity of the squares in def. \ref{MultiplicativeCohomologyTheory}:

$$
  \array{
    E^{n_1}(\ast)\otimes E^{n_2}(A)
      &\overset{(-1)^{n_1} (id, \delta)}{\longrightarrow}&
    E^{n_1}(\ast) \otimes E^{n_2 + 2}(X)
    \\
    {}^{\mathllap{\mu_{n_1,n_2}}}\downarrow && \downarrow^{\mathrlap{\mu_{n_1,n_2}}}
    \\
    E^{n_1 + n_2}(A)
      &\overset{\delta}{\longrightarrow}&
     E_3^{n_1 + n_2+ 1}(X,B)
  }
  \,.
$$

=--




### Brown representability theorem
 {#BrownRepresentabilityTheorem}


**Idea.** Given any [[functor]] such as the generalized (co)homology functor [above](#GeneralizedHomologyAndCohomologyFunctors), an important question to ask is whether it is a _[[representable functor]]_. Due to the $\mathbb{Z}$-grading and the [[suspension isomorphisms]], if a generalized (co)homology functor is representable at all, it must be represented by a $\mathbb{Z}$-indexed sequence of [[pointed topological spaces]] such that the [[reduced suspension]] of one is comparable to the next one in the list. This is a _[[spectrum]]_ or more specifically: a _[[sequential spectrum]]_ .

Whitehead observed that indeed every [[spectrum]] represents a generalized (co)homology theory.  The _[[Brown representability theorem]]_ states that, conversely, every generalized (co)homology theory is represented by a spectrum, subject to conditions of additivity.

As a first application, [[Eilenberg-MacLane spectra]] representing [[ordinary cohomology]] may be characterized via Brown representability.

**Literature.** ([Switzer 75, section 9](#Switzer75), [Aguilar-Gitler-Prieto 02, section 12](#AguilarGitlerPrieto02), [Kochman 96, 3.4](#Kochman96))




#### Traditional discussion
 {#BrownRepresentabilityTraditional}


Write $Top_{{\geq 1}}^{\ast/} \hookrightarrow Top^{\ast/}$ for the [[full subcategory]] of _[[connected topological space|connected]]_ [[pointed topological spaces]]. Write $Set^{\ast/}$ for the category of [[pointed sets]].

+-- {: .num_defn #BrownFunctorTraditional}
###### Definition

A **[[Brown functor]]** is a functor

$$
  F\;\colon \; Ho(Top_{\geq 1}^{\ast/})^{op} \longrightarrow Set^{\ast/}
$$

(from the [[opposite category|opposite]] of the [[classical homotopy category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalHomotopyCategory), [def.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalPointedHomotopyCategory)) of [[connected topological space|connected]] [[pointed topological space|pointed]] [[topological spaces]]) such that

1. **(additivity)** $F$ takes small coproducts ([[wedge sums]]) to [[products]];

1. **(Mayer-Vietoris)** If $X = Int(A) \cup Int(B)$ then for all $x_A \in F(A)$ and $x_B \in F(B)$ such that $(x_A)|_{A \cap B} = (x_B)|_{A \cap B}$ then there exists $x_X \in F(X)$ such that $x_A = (x_X)|_A$ and $x_B = (x_X)|_B$.

=--

+-- {: .num_prop #EveryComponentOfAdditiveReducedCohomologyIsBrownFunctor}
###### Proposition

For every [additive](#WedgeAxiom) [[reduced cohomology theory]] $\tilde E^\bullet(-) \colon Ho(Top^{\ast/})^{op}\to Set^{\ast/}$ (def. \ref{ReducedGeneralizedCohomologyHomotopyTheoretically}) and for each degree $n \in \mathbb{N}$, the restriction of $\tilde E^n(-)$ to connected spaces is a [[Brown functor]] (def. \ref{BrownFunctorTraditional}).

=--

+-- {: .proof}
###### Proof

Under the relation between reduced and unreduced cohomology [above](#RelationBetweenUnreducedAndReducedCohomology), this follows from the [[exact sequence|exactness]] of the [[Mayer-Vietoris sequence]] of prop. \ref{MayerVietorisSequenceInGeneralizedCohomology}.

=--

+-- {: .num_theorem #BrownRepresentabilityForTraditionalBrownFunctors}
###### Theorem
**(Brown representability)**

Every [[Brown functor]] $F$ (def. \ref{BrownFunctorTraditional}) is [[representable functor|representable]], hence there exists $X \in Top_{\geq 1}^{\ast/}$ and a [[natural isomorphism]]

$$
  [-,X]_{\ast} \overset{\simeq}{\longrightarrow} F(-)
$$

(where $[-,-]_\ast$ denotes the [[hom-functor]] of $Ho(Top_{\geq 1}^{\ast/})$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfPointedModelStructureIsEnrichedInPointedSets))).

=--

(e.g. [AGP 02, theorem 12.2.22](#AguilarGitlerPrieto02))

+-- {: .num_remark #ConnectivityInTraditionalBrownRepresentability}
###### Remark

A key subtlety in theorem \ref{BrownRepresentabilityForTraditionalBrownFunctors} is the restriction to _connected_ pointed topological spaces in def. \ref{BrownFunctorTraditional}. This comes about since the proof of the theorem requires that continuous functions $f \colon X \longrightarrow Y$ that induce isomorphisms on pointed homotopy classes

$$
  [S^n,X]_\ast \longrightarrow [S^n,Y]_\ast
$$

for all $n$ are [[weak homotopy equivalences]] (For instance in [AGP 02](#AguilarGitlerPrieto02) this is used in the proof of theorem 12.2.19 there). But $[S^n,X]_\ast = \pi_n(X,x)$ gives the $n$th [[homotopy group]] of $X$ _only_ for the canonical basepoint, while for a weak homotopy equivalence in general one needs to consider the homotopy groups at all possible basepoints, at least one for each connected component. But so if one does assume that all spaces involved are connected, hence only have one connected component, then indeed weak homotopy equivalences are equivalently those maps  $X\to Y$ making all the $[S^n,X]_\ast \longrightarrow [S^n,Y]_\ast$ into isomorphisms.

See also example \ref{TheClassicalPointedConnectedHomotopyCategoryAsDomainForTheAbstractBrownRepresentabilityTheorem} below.

=--

The representability result applied degreewise to an additive reduced cohomology theory will yield (prop. \ref{AdditiveReducedCohomologyTheoryRepresentedByOmegaSpectrum} below) the following concept.

+-- {: .num_defn #OmegaSpectrum}
###### Definition

An **[[Omega-spectrum]]** $X$ ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#OmegaSpectrum)) is

1. a sequence $\{X_n\}_{n \in \mathbb{N}}$ of [[pointed topological spaces]] $X_n \in Top^{\ast/}$

1. [[weak homotopy equivalences]]

   $$
     \tilde \sigma_n
     \;\colon\;
     X_n \underoverset{\in W_{cl}}{\tilde \sigma_n}{\longrightarrow} \Omega X_{n+1}
   $$

   for each $n \in \mathbb{N}$, form each space to the [[loop space]] of the following space.

=--

+-- {: .num_prop #AdditiveReducedCohomologyTheoryRepresentedByOmegaSpectrum}
###### Proposition

Every [additive](#WedgeAxiom) [[reduced cohomology theory]] $\tilde E^\bullet(-) \colon (Top_{CW}^\ast)^{op} \longrightarrow Ab^{\mathbb{Z}}$ according to def. \ref{ReducedGeneralizedCohomologyHomotopyTheoretically}, is [[representable functor|represented]] by an [[Omega-spectrum]] $E$ (def. \ref{OmegaSpectrum}) in that in each degree $n \in \mathbb{N}$

1. $\tilde E^n(-)$ is represented by some $E_n \in Ho(Top^{\ast/})$;

1. the [suspension isomorphism](#SuspensionIsomorphismForReducedGeneralizedCohomology) $\sigma_n$ of $\tilde E^\bullet$ is represented by the structure map $\tilde \sigma_n$ of the Omega-spectrum in that for all $X \in Top^{\ast/}$ the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       \tilde E^{n}(X)
         &\overset{\sigma_n(X)}{\longrightarrow}&
         &\longrightarrow&
       \tilde E^{n+1}(\Sigma X)
       \\
       {}^{\mathllap{\simeq}}\downarrow
         && &&
       \downarrow^{\mathrlap{\simeq}}
       \\
       [X,E_n]_\ast
         &\overset{[X,\tilde \sigma_n]_\ast}{\longrightarrow}&
       [X, \Omega E_{n+1}]_\ast
         &\simeq&
       [\Sigma X, E_{n+1}]_\ast
     }
     \,,
   $$

   where $[-,-]_\ast \coloneqq Hom_{Ho(Top_{\geq 1}^{\ast/})}$ denotes the [[hom-sets]] in the [[classical pointed homotopy category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#ClassicalModelStructureOnPointedTopologicalSpaces)) and where in the bottom right we have the $(\Sigma\dashv \Omega)$-[[adjunction]] isomorphism ([prop.](Introduction+to+Stable+homotopy+theory+--+P#SuspensionAndLoopAreAdjointOnHomotopyCategory)).

=--

+-- {: .proof}
###### Proof

If it were not for the connectedness clause in def. \ref{BrownFunctorTraditional} (remark \ref{ConnectivityInTraditionalBrownRepresentability}), then theorem \ref{BrownRepresentabilityForTraditionalBrownFunctors} with prop. \ref{EveryComponentOfAdditiveReducedCohomologyIsBrownFunctor} would immediately give the existence of the $\{E_n\}_{n \in \mathbb{N}}$ and the remaining statement would follow immediately with the [[Yoneda lemma]], which says in particular that morphisms between [[representable functors]] are in [[natural bijection]] with the morphisms of objects that represent them.

The argument with the connectivity condition in Brown representability taken into account is essentially the same, just with a little bit more care:

For $X$ a [[pointed topological space]], write $X^{(0)}$ for the connected component of its basepoint. Observe that the [[loop space]] of a pointed topological space only depends on this connected component:

$$
  \Omega X \simeq \Omega (X^{(0)})
  \,.
$$

Now for $n \in \mathbb{N}$, to show that $\tilde E^n(-)$ is representable by some $E_n \in Ho(Top^{\ast/})$, use first that the restriction of $\tilde E^{n+1}$ to connected spaces is represented by some $E_{n+1}^{(0)}$. Observe that the [[reduced suspension]] of any $X \in Top^{\ast/}$ lands in $Top_{\geq 1}^{\ast/}$. Therefore the $(\Sigma\dashv \Omega)$-[[adjunction]] isomorphism ([prop.](Introduction+to+Stable+homotopy+theory+--+P#SuspensionAndLoopAreAdjointOnHomotopyCategory)) implies that $\tilde E^{n+1}(\Sigma(-))$ is represented on _all_ of $Top^{\ast/}$ by $\Omega E_{n+1}^{(0)}$:

$$
  \tilde E^{n+1}(\Sigma X)
    \simeq
  [\Sigma X, E_{n+1}^{(0)}]_\ast
    \simeq
  [X, \Omega E_{n+1}^{(0)}]_\ast
    \simeq
  [X, \Omega E_{n+1}]_\ast
  \,,
$$

where $E_{n+1}$ is any pointed topological space with the given connected component $E_{n+1}^{(0)}$.

Now the [suspension isomorphism](#SuspensionIsomorphismForReducedGeneralizedCohomology) of $\tilde E$ says that $E_n \in Ho(Top^{\ast/})$ representing $\tilde E^n$ exists and is given by $\Omega E_{n+1}^{(0)}$:

$$
  \tilde E^n(X) \simeq \tilde E^{n+1}(\Sigma, X)\simeq [X,\Omega E_{n+1}]
$$

for any $E_{n+1}$ with connected component $E_{n+1}^{(0)}$.

This completes the proof. Notice that running the same argument next for $(n+1)$ gives a representing space $E_{n+1}$ such that its connected component of the base point is $E_{n+1}^{(0)}$ found before. And so on.

=--

Conversely:

+-- {: .num_prop #SpectrumRepresentsCohomologyTheoryDegreewise}
###### Proposition

Every [[Omega-spectrum]] $E$, def. \ref{OmegaSpectrum}, represents an [additive](#WedgeAxiom) [[reduced cohomology theory]] def. \ref{ReducedGeneralizedCohomology} $\tilde E^\bullet$ by

$$
  \tilde E^n(X)
    \coloneqq
  [X,E_n]_\ast
$$

with [suspension isomorphism](#SuspensionIsomorphismForReducedGeneralizedCohomology) given by

$$
  \sigma_n
    \;\colon\;
  \tilde E^n(X)
    =
  [X,E_n]_\ast
    \overset{[X,\tilde \sigma_n]}{\longrightarrow}
  [X, \Omega E_{n+1}]_\ast
    \overset{\simeq}{\to}
  [\Sigma X, E_{n+1}]
    =
  \tilde E^{n+1}(\Sigma X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The [additivity](#WedgeAxiom) is immediate from the construction.
The [exactnes](#ReducedExactnessAxiom) follows from the [[long exact sequences]] of [[homotopy cofiber sequences]] given by [this prop.](Introduction+to+Stable+homotopy+theory+--+P#LongFiberSequence).

=--

+-- {: .num_remark}
###### Remark

If we consider the [[stable homotopy category]] $Ho(Spectra)$ of [[spectra]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#TheStableHomotopyCategory)) and consider any [[topological space]] $X$ in terms of its [[suspension spectrum]] $\Sigma^\infty X \in Ho(Spectra)$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+1-1#SuspensionSpectrum)), then the statement of prop. \ref{SpectrumRepresentsCohomologyTheoryDegreewise} is more succinctly summarized by saying that the [[graded abelian group|graded]] reduced cohomology groups of a topological space $X$ represented by an [[Omega-spectrum]] $E$ are the hom-groups

$$
  \tilde E^\bullet(X)
   \;\simeq\;
  [\Sigma^\infty X, \Sigma^\bullet E]
$$

in the [[stable homotopy category]], into all the [[suspensions]] ([thm.](Introduction+to+Stable+homotopy+theory+--+1-1#StableModelStructureOnSequentiaSpectraIsStableModelCategory)) of $E$.

This means that more generally, for $X \in Ho(Spectra)$ any spectrum, it makes sense to consider

$$
  \tilde E^\bullet(X)
    \;\coloneqq\;
  [X,\Sigma^\bullet E]
$$

to be the graded reduced generalized $E$-cohomology groups of the spectrum $X$.

See also in  _[[Introduction to Stable homotopy theory -- 1|part 1]]_ [this example](Introduction+to+Stable+homotopy+theory+--+1-1#ForASpectrumXGeneralizedECohomology).

=--



#### Application to ordinary cohomology
 {#BrownRepresentabilityAppliedToOrdinaryCohomology}

+-- {: .num_example #EilenbergMacLaneSpectrum}
###### Example

Let $A$ be an [[abelian group]]. Consider [[singular cohomology]] $H^n(-,A)$ with [[coefficients]] in $A$.  The corresponding [[reduced cohomology]] evaluated on [[n-spheres]] satisfies

$$
  \tilde H^n(S^q,A)
  \simeq
  \left\{
    \array{
      A & if \; q = n
      \\
      0 & otherwise
    }
  \right.
$$

Hence singular cohomology is a [generalized cohomology theory](#S1GeneralizedCohomology) which is "[[ordinary cohomology]]" in the sense of def. \ref{AdditiveOrdinary}.

Applying the [[Brown representability theorem]] as in prop. \ref{AdditiveReducedCohomologyTheoryRepresentedByOmegaSpectrum} hence produces an [[Omega-spectrum]] (def. \ref{OmegaSpectrum}) whose $n$th component space is characterized as having [[homotopy groups]] concentrated in degree $n$ on $A$. These are called _[[Eilenberg-MacLane spaces]]_  $K(A,n)$

$$
  \pi_q(K(A,n))
    \simeq
  \left\{
    \array{
      A & if \; q = n
      \\
      0 & otherwise
    }
  \right.
  \,.
$$

Here for $n \gt 0$ then $K(A,n)$ is connected, therefore with an essentially unique basepoint, while $K(A,0)$ is (homotopy equivalent to) the underlying set of the group $A$.

Such spectra are called **[[Eilenberg-MacLane spectra]]** $H A$:

$$
  (H A)_n \simeq K(A,n)
  \,.
$$

=--

As a consequence of example \ref{EilenbergMacLaneSpectrum} one obtains the uniqueness result of Eilenberg-Steenrod:

+-- {: .num_prop}
###### Proposition

Let $\tilde E_1$ and $\tilde E_2$ be ordinary (def. \ref{AdditiveOrdinary}) [[generalized (Eilenberg-Steenrod) cohomology theories]]. If there is an isomorphism

$$
  \tilde E_1(S^0) \simeq \tilde E_2(S^0)
$$

of [[cohomology groups]] of the [[0-sphere]], then there is an [[isomorphism]] of cohomology theories

$$
  \tilde E_1 \overset{\simeq}{\longrightarrow} \tilde E_2
  \,.
$$

=--

(e.g. [Aguilar-Gitler-Prieto 02, theorem 12.3.6](#AguilarGitlerPrieto02))




#### Homotopy-theoretic discussion

Using abstract [[homotopy theory]] in the guise of [[model category]] theory (see the _[[Introduction to Stable homotopy theory -- P|lecture notes on classical homotopy theory]]), the traditional proof and further discussion of the [[Brown representability theorem]] [above](#BrownRepresentabilityTraditional) becomes more transparent ([Lurie 10, section 1.4.1](#LurieHigherAlgebra), for exposition see also [Mathew 11](Brown+representability+theorem#Mathew11)).

This abstract homotopy-theoretic proof uses the general concept of [[homotopy colimits]] in [[model categories]] as well as the concept of [[derived hom-spaces]] ("[[(∞,1)-category|∞-categories]]"). Even though in the accompanying [[Introduction to Stable homotopy theory -- P|Lecture notes on classical homotopy theory]] these concepts are only briefly indicated, the following is included for the interested reader.



+-- {: .num_defn #BrownFunctorOnInfinityCategory}
###### Definition

Let $\mathcal{C}$ be a [[model category]]. A [[functor]]

$$
  F \;\colon\; Ho(\mathcal{C})^{op} \longrightarrow Set
$$

(from the [[opposite category|opposite]] of the [[homotopy category of a model category|homotopy category]] of $\mathcal{C}$ to [[Set]])

is called a **[[Brown functor]]** if

1. it sends small [[coproducts]] to [[products]];

1. it sends [[homotopy pushouts]] in $\mathcal{C}\to Ho(\mathcal{C})$ to [[weak pullbacks]] in [[Set]] (see remark \ref{WeakPullbacks}).

=--

+-- {: .num_remark #WeakPullbacks}
###### Remark

A _[[weak pullback]]_ is a diagram that satisfies the existence clause of a [[pullback]], but not necessarily the uniqueness condition. Hence the second clause in def. \ref{BrownFunctorOnInfinityCategory} says that for a [[homotopy pushout]] square

$$
  \array{
    Z &\longrightarrow& X
    \\
    \downarrow &\swArrow& \downarrow
    \\
    Y &\longrightarrow& X \underset{Z}{\sqcup}Y
  }
$$

in $\mathcal{C}$, then the induced universal morphism


$$
  F\left(X \underset{Z}{\sqcup}Y\right)
  \stackrel{epi}{\longrightarrow}
  F(X) \underset{F(Z)}{\times} F(Y)
$$

into the actual [[pullback]] is an [[epimorphism]].

=--

+-- {: .num_defn #CompactGenerationByCogroupObjects}
###### Definition

Say that  a [[model category]] $\mathcal{C}$
is **compactly generated by cogroup objects closed under suspensions** if


1. $\mathcal{C}$ is [[compactly generated (∞,1)-category|generated]] by a set

   $$
    \{S_i \in \mathcal{C}\}_{i \in I}
   $$

   of [[compact object in an (infinity,1)-category|compact objects]] (i.e. every object of $\mathcal{C}$ is a [[homotopy colimit]] of the objects $S_i$.)

1. each $S_i$ admits the structure of a [[cogroup]] object in the [[homotopy category of a model category|homotopy category]] $Ho(\mathcal{C})$;

1. the set $\{S_i\}$ is closed under forming [[reduced suspensions]].

=--

+-- {: .num_example #SuspensionsAreHCogroupObjects}
###### Example
**([[suspensions are H-cogroup objects]])**

Let $\mathcal{C}$ be a [[model category]] and $\mathcal{C}^{\ast/}$ its pointed model category ([prop.](Introduction+to+Stable+homotopy+theory+--+P#ModelStructureOnSliceCategory)) with [[zero object]] ([rmk.](Introduction+to+Stable+homotopy+theory+--+P#PointedObjectsHaveZeroObject)). Write $\Sigma \colon X \mapsto 0 \underset{X}{\coprod} 0$ for the [[reduced suspension]] functor.

Then the [[fold map]]

$$
  \Sigma X \coprod \Sigma X
    \simeq
  0 \underset{X}{\sqcup} 0 \underset{X}{\sqcup} 0
    \longrightarrow
  0 \underset{X}{\sqcup} X \underset{X}{\sqcup} 0
  \simeq
  0 \underset{X}{\sqcup} 0
  \simeq
  \Sigma X
$$

exhibits [[cogroup]] structure on the image of any [[suspension object]] $\Sigma X$ in the [[homotopy category of an (∞,1)-category|homotopy category]].

This is equivalently the [[group]]-structure of the first ([[fundamental group|fundamental]]) [[homotopy group]] of the values of [[representable functor|functor co-represented]] by $\Sigma X$:

$$
  Ho(\mathcal{C})(\Sigma X, -)
   \;\colon\;
  Y
   \mapsto
  Ho(\mathcal{C})(\Sigma X, Y)
   \simeq
  Ho(\mathcal{C})(X, \Omega Y)
   \simeq
  \pi_1 Ho(\mathcal{C})(X, Y)
  \,.
$$

=--

+-- {: .num_example #TheClassicalPointedConnectedHomotopyCategoryAsDomainForTheAbstractBrownRepresentabilityTheorem}
###### Example

In bare [[pointed homotopy types]] $\mathcal{C} = Top^{\ast/}_{Quillen}$, the ([[homotopy types]] of) [[n-spheres]] $S^n$ are [[cogroup]] objects for $n \geq 1$, but not for $n = 0$, by example \ref{SuspensionsAreHCogroupObjects}. And of course they are [[compact object in an (∞,1)-category|compact objects]].

So while $\{S^n\}_{n \in \mathbb{N}}$ generates all of the homotopy theory of $Top^{\ast/}$, the latter is _not_ an example of def. \ref{CompactGenerationByCogroupObjects} due to the failure of $S^0$ to have [[cogroup]] structure.

Removing that generator, the homotopy theory generated by $\{S^n\}_{{n \in \mathbb{N}} \atop {n \geq 1}}$ is $Top^{\ast/}_{\geq 1}$, that of _[[connected object|connected]]_ [[pointed homotopy types]]. This is one way to see how the connectedness condition in the classical version of Brown representability theorem arises. See also remark \ref{ConnectivityInTraditionalBrownRepresentability} above.

=--


See also ([Lurie 10, example 1.4.1.4](#LurieHigherAlgebra))

In homotopy theories compactly generated by cogroup objects closed under forming suspensions, the following strenghtening of the [[Whitehead theorem]] holds.

+-- {: .num_prop #WhiteheadTheoremForCompactGenerationByCogroupObjects}
###### Proposition

In a  homotopy theory compactly generated by cogroup objects $\{S_i\}_{i \in I}$ closed under forming suspensions, according to def. \ref{CompactGenerationByCogroupObjects}, a morphism $f\colon X \longrightarrow Y$ is an [[equivalence in an (infinity,1)-category|equivalence]] precisely if for each $i \in I$ the induced function of maps in the [[homotopy category of a model category|homotopy category]]

$$
  Ho(\mathcal{C})(S_i,f)
   \;\colon\;
  Ho(\mathcal{C})(S_i,X)
   \longrightarrow
  Ho(\mathcal{C})(S_i,Y)
$$

is an [[isomorphism]] (a [[bijection]]).

=--

([Lurie 10, p. 114, Lemma star](#LurieHigherAlgebra))

+-- {: .proof }
###### Proof

By the [[(∞,1)-Yoneda lemma|∞-Yoneda lemma]], the morphism $f$ is a weak equivalence precisely if for all objects $A \in \mathcal{C}$  the induced morphism of [[derived hom-spaces]]

$$
  \mathcal{C}(A,f)
  \;\colon\;
  \mathcal{C}(A,X)
   \longrightarrow
  \mathcal{C}(A,Y)
$$

is an equivalence in $Top_{Quillen}$. By assumption of compact generation and since the hom-functor $\mathcal{C}(-,-)$ sends [[homotopy colimits]] in the first argument to [[homotopy limits]], this is the case precisely already if it is the case for $A \in \{S_i\}_{i \in I}$.

Now the maps

$$
  \mathcal{C}(S_i,f)
  \;\colon\;
  \mathcal{C}(S_i,X)
   \longrightarrow
  \mathcal{C}(S_i,Y)
$$

are weak equivalences in $Top_{Quillen}$ if they are [[weak homotopy equivalences]], hence if they induce [[isomorphisms]] on all [[homotopy groups]] $\pi_n$ for **all basepoints**.

It is this last condition of testing on all basepoints that the assumed [[cogroup]] structure on the $S_i$ allows to do away with: this cogroup structure implies that $\mathcal{C}(S_i,-)$ has the structure of an $H$-group, and this implies (by group multiplication), that all [[connected components]] have the same homotopy groups, hence that all homotopy groups are independent of the choice of basepoint, up to isomorphism.

Therefore the above morphisms are equivalences precisely if they are so under applying $\pi_n$ based on the connected component of the [[zero morphism]]

$$
  \pi_n\mathcal{C}(S_i,f)
    \;\colon\;
  \pi_n \mathcal{C}(S_i,X)
     \longrightarrow
  \pi_n\mathcal{C}(S_i,Y)
  \,.
$$

Now in this pointed situation we may use that

$$
  \begin{aligned}
    \pi_n \mathcal{C}(-,-) & \simeq \pi_0 \mathcal{C}(-,\Omega^n(-))
    \\
    & \simeq \pi_0\mathcal{C}(\Sigma^n(-),-)
    \\
    & \simeq Ho(\mathcal{C})(\Sigma^n(-),-)
  \end{aligned}
$$

to find that $f$ is an equivalence in $\mathcal{C}$ precisely if the induced morphisms

$$
  Ho(\mathcal{C})(\Sigma^n S_i, f)
    \;\colon\;
  Ho(\mathcal{C})(\Sigma^n S_i,X)
    \longrightarrow
  Ho(\mathcal{C})(\Sigma^n S_i,Y)
$$

are isomorphisms for all $i \in I$ and $n \in \mathbb{N}$.

Finally by the assumption that each suspension $\Sigma^n S_i$ of a generator is itself among the set of generators, the claim follows.

=--

+-- {: .num_theorem #BrownRepresentabilityOnPresentableInfinityCategories}
###### Theorem
**(Brown representability)**

Let $\mathcal{C}$ be a [[model category]] compactly generated by cogroup objects closed under forming suspensions, according to def. \ref{CompactGenerationByCogroupObjects}. Then a [[functor]]

$$
  F \;\colon\; Ho(\mathcal{C})^{op} \longrightarrow Set
$$

(from the [[opposite category|opposite]] of the [[homotopy category of a model category|homotopy category]] of $\mathcal{C}$ to [[Set]])
is [[representable functor|representable]] precisely if it is a [[Brown functor]], def. \ref{BrownFunctorOnInfinityCategory}.

=--

([Lurie 10, theorem 1.4.1.2](#LurieHigherAlgebra))

+-- {: .proof #ProofFollowingLurie}
###### Proof


Due to the version of the Whitehead theorem of prop. \ref{WhiteheadTheoremForCompactGenerationByCogroupObjects} we are essentially reduced to showing that [[Brown functors]] $F$ are representable on the $S_i$. To that end consider the following lemma.
(In the following we notationally identify, via the [[Yoneda lemma]], objects of $\mathcal{C}$, hence of $Ho(\mathcal{C})$, with the functors they [[representable functor|represent]].)

Lemma ($\star$): _Given $X \in \mathcal{C}$ and $\eta \in F(X)$, hence $\eta \colon X \to F$, then there exists a morphism $f \colon X \to X'$ and an [[extension]] $\eta' \colon X' \to F$ of $\eta$ which induces for each $S_i$ a [[bijection]] $\eta'\circ (-) \colon PSh(Ho(\mathcal{C}))(S_i,X') \stackrel{\simeq}{\longrightarrow} Ho(\mathcal{C})(S_i,F) \simeq F(S_i)$._

To see this, first notice that we may directly find an extension $\eta_0$ along a map $X\to X_o$ such as to make a [[surjection]]: simply take $X_0$ to be the [[coproduct]] of **all** possible elements in the codomain and take

$$
  \eta_0
  \;\colon\;
   X
     \sqcup
   \left(
     \underset{{i \in I,} \atop {\gamma \colon S_i \stackrel{}{\to} F}}{\coprod}
     S_i
   \right)
   \longrightarrow
   F
$$

to be the canonical map. (Using that $F$, by assumption, turns coproducts into products, we may indeed treat the coproduct in $\mathcal{C}$ on the left as the coproduct of the corresponding functors.)

To turn the surjection thus constructed into a bijection, we now successively form quotients of $X_0$. To that end proceed by [[induction]] and suppose that $\eta_n \colon X_n \to F$ has been constructed. Then for $i \in I$ let

$$
  K_i
    \coloneqq
  ker
  \left(
     Ho(\mathcal{C})(S_i, X_n)
        \stackrel{\eta_n \circ (-)}{\longrightarrow}
     F(S_i)
   \right)
$$

be the [[kernel]] of  $\eta_n$ evaluated on $S_i$. These $K_i$ are the pieces that need to go away in order to make a bijection. Hence define $X_{n+1}$ to be their joint [[homotopy cofiber]]

$$
  X_{n+1}
     \coloneqq
   coker\left(
     \left(
        \underset{{i \in I,} \atop {\gamma \in K_i}}{\sqcup} S_i
     \right)
     \overset{(\gamma)_{{i \in I} \atop {\gamma\in K_i}}}{\longrightarrow}
     X_n
  \right)
  \,.
$$

Then by the assumption that $F$ takes this homotopy cokernel to a [[weak limit|weak]] [[fiber]] (as in remark \ref{WeakPullbacks}), there exists an extension $\eta_{n+1}$ of $\eta_n$ along $X_n \to X_{n+1}$:

Then by the assumption that $F$ takes this homotopy cokernel to a [[weak limit|weak]] [[fiber]] (as in remark \ref{WeakPullbacks}), there exists an extension $\eta_{n+1}$ of $\eta_n$ along $X_n \to X_{n+1}$:

$$
  \array{
    \left(
      \underset{{i \in I}\atop {\gamma \in K_i}}{\sqcup} S_i
    \right)
    &\overset{(\gamma)_{{i \in I}\atop \gamma \in K_i}}{\longrightarrow}&
    X_n
    &\overset{\eta_n}{\longrightarrow}& F
    \\
    \downarrow &(po^{h})& \downarrow & \nearrow_{\mathrlap{\exists \eta_{n+1}}}
    \\
    \ast &\longrightarrow& X_{n+1}
  }
  \;\;\;\;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;\;\;\;
  \array{
    && F(X_{n+1}) &\longrightarrow& \ast
    \\
    &{}^{\mathllap{\exists \eta_{n+1}}}\nearrow& \downarrow^{\mathrlap{epi}} && \downarrow
    \\
    \ast &\overset{\eta_n}{\longrightarrow}& ker\left((\gamma^\ast\right)_{{i \in I} \atop {\gamma \in K_i}}) &\longrightarrow& \ast
    \\
    &{}_{\mathllap{\eta_n}}\searrow& \downarrow &(pb)& \downarrow
    \\
    && F(X_n)
    &\underset{(\gamma^\ast)_{{i \in I} \atop {\gamma \in K_i}} }{\longrightarrow}&
    \underset{{i \in I}\atop {\gamma\in K_i}}{\prod}F(S_i)
  }
  \,.
$$

It is now clear that we want to take

$$
  X' \coloneqq \underset{\rightarrow}{\lim}_n X_n
$$

and extend all the $\eta_n$ to that colimit. Since we have no condition for evaluating $F$ on colimits other than pushouts, observe that this [[sequential colimit]] is equivalent to the following pushout:

$$
  \array{
    \underset{n}{\sqcup} X_n
    &\longrightarrow& \underset{n}{\sqcup} X_{2n}
    \\
    \downarrow && \downarrow
    \\
    \underset{n}{\sqcup} X_{2n+1} &\longrightarrow& X'
  }
  \,,
$$

where the components of the top and left map alternate between the identity on $X_n$ and the above successor maps $X_n \to X_{n+1}$.
Now the excision property of $F$ applies to this pushout, and we conclude the desired  extension $\eta' \colon X' \to F$:

$$
  \array{
    && \underset{n}{\sqcup} X_n
    \\
    & \swarrow && \searrow
    \\
    \underset{n}{\sqcup} X_{2n+1} &\longrightarrow& X' &\longleftarrow& \underset{n}{\sqcup} X_{2n}
    \\
    & {}_{\mathllap{(\eta_{2n+1})_{n}}}\searrow& \downarrow^{\mathrlap{\exists \eta}} & \swarrow_{\mathrlap{(\eta_{2n})_n}}
    \\
    && F
  }
  \;\;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;\;
  \array{
    && F(X')
    \\
    &{}^{\mathllap{\exists \eta}}\nearrow& \downarrow^{\mathrlap{epi}}
    \\
    &\ast \overset{(\eta_n)_n}{\longrightarrow}& \underset{\longleftarrow}{\lim}_n F(X_n)
    \\
    & \swarrow && \searrow
    \\
    \underset{n}{\prod}F(X_{2n+1})
    && &&
    \underset{n}{\prod}(X_{2n})
    \\
    & \searrow && \swarrow
    \\
    && \underset{n}{\prod}F(X_n)
  }
  \,,
$$



It remains to confirm that this indeed  gives the desired bijection. Surjectivity is clear. For injectivity use that all the $S_i$ are, by assumption, [[compact object|compact]], hence they may be taken inside the [[sequential colimit]]:

$$
  \array{
    && X_{n(\gamma)}
    \\
    &{}^{\mathllap{ \exists \hat \gamma}}\nearrow& \downarrow
    \\
    S_i
      &\overset{\gamma}{\longrightarrow}&
    X'
      =
    \underset{\longrightarrow}{\lim}_n X_n
  }
  \,.
$$

With this, injectivity follows because by construction we quotiented out the kernel at each stage. Because suppose that $\gamma$ is taken to zero in $F(S_i)$, then by the definition of $X_{n+1}$ above there is a factorization of $\gamma$ through the point:

$$
  \array{
    0 \colon & S_i
    &\overset{\hat \gamma}{\longrightarrow}&
    X_{n(\gamma)}
    &\overset{\eta_n}{\longrightarrow}& F
    \\
    & \downarrow && \downarrow &
    \\
    & \ast &\longrightarrow& X_{n(\gamma)+1}
    \\
    & && \downarrow
    \\
    & && X'
  }
$$

This concludes the proof of Lemma ($\star$).

Now apply the construction given by this lemma to the case
$X_0 \coloneqq 0$ and the unique $\eta_0 \colon 0 \stackrel{\exists !}{\to} F$. Lemma $(\star)$ then produces an object $X'$ which represents $F$ on all the $S_i$, and we want to show that this $X'$ actually represents $F$ generally, hence that for every $Y \in \mathcal{C}$ the function

$$
  \theta \coloneqq \eta'\circ (-)
  \;\colon\;
  Ho(\mathcal{C})(Y,X')
   \stackrel{}{\longrightarrow}
  F(Y)
$$

is a [[bijection]].

First, to see that $\theta$ is surjective, we need to find a preimage of any $\rho \colon Y \to F$. Applying Lemma $(\star)$ to $(\eta',\rho)\colon X'\sqcup Y \longrightarrow F$ we get an extension $\kappa$ of this through some $X' \sqcup Y \longrightarrow Z$ and the morphism on the right of the following commuting diagram:

$$
  \array{
    Ho(\mathcal{C})(-,X') && \longrightarrow && Ho(\mathcal{C})(-, Z)
    \\
    & {}_{\mathllap{\eta'\circ(-)}}\searrow && \swarrow_{\mathrlap{\kappa \circ (-)}}
    \\
    && F(-)
  }
  \,.
$$

Moreover, Lemma $(\star)$ gives that evaluated on all $S_i$, the two diagonal morphisms here become isomorphisms. But then prop. \ref{WhiteheadTheoremForCompactGenerationByCogroupObjects} implies that $X' \longrightarrow Z$ is in fact an equivalence. Hence the component map $Y \to Z \simeq Z$ is a lift of $\kappa$ through $\theta$.

Second, to see that $\theta$ is injective, suppose $f,g \colon Y \to X'$ have the same image under $\theta$. Then consider their [[homotopy pushout]]

$$
  \array{
    Y \sqcup Y &\stackrel{(f,g)}{\longrightarrow}& X'
    \\
    \downarrow && \downarrow
    \\
    Y &\longrightarrow& Z
  }
$$

along the [[codiagonal]] of $Y$. Using that $F$ sends this to a [[weak pullback]] by assumption, we obtain an extension $\bar \eta$ of $\eta'$ along $X' \to Z$. Applying Lemma $(\star)$ to this gives a further extension $\bar \eta' \colon Z' \to Z$ which now makes the following diagram

$$
  \array{
    Ho(\mathcal{C})(-,X') && \longrightarrow && Ho(\mathcal{C})(-, Z)
    \\
    & {}_{\mathllap{\eta'\circ(-)}}\searrow && \swarrow_{\mathrlap{\bar \eta' \circ (-)}}
    \\
    && F(-)
  }
$$

such that the diagonal maps become isomorphisms when evaluated on the $S_i$. As before, it follows via prop. \ref{WhiteheadTheoremForCompactGenerationByCogroupObjects} that the morphism
$h \colon X' \longrightarrow Z'$ is an equivalence.

Since by this construction $h\circ f$ and $h\circ g$ are homotopic

$$
  \array{
    Y \sqcup Y &\stackrel{(f,g)}{\longrightarrow}& X'
    \\
    \downarrow && \downarrow & \searrow^{\mathrlap{\stackrel{h}{\simeq}}}
    \\
    Y &\longrightarrow& Z &\longrightarrow& Z'
  }
$$

it follows with $h$ being an equivalence that already $f$ and $g$ were homotopic, hence that they represented the same element.


=--




+-- {: .num_prop #CohomologyFunctorOnInfinityCategoryIsBrownFunctor}
###### Proposition

Given a reduced additive cohomology functor $H^\bullet \colon Ho(\mathcal{C})^{op}\to Ab^{\mathbb{Z}}$, def. \ref{GeneralizedCohomologyOnGeneralInfinityCategory}, its underlying [[Set]]-valued functors $H^n \colon Ho(\mathcal{C})^{op}\to Ab\to Set$ are [[Brown functors]], def. \ref{BrownFunctorOnInfinityCategory}.

=--

+-- {: .proof}
###### Proof

The first condition on a [[Brown functor]] holds by definition of $H^\bullet$. For the second condition, given a [[homotopy pushout]] square

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

+-- {: .num_cor }
###### Corollary

Let $\mathcal{C}$ be a [[model category]] which satisfies the conditions of theorem \ref{BrownRepresentabilityOnPresentableInfinityCategories}, and let $(H^\bullet, \delta)$ be a reduced additive [[generalized cohomology]] functor on $\mathcal{C}$, def. \ref{GeneralizedCohomologyOnGeneralInfinityCategory}. Then there exists a [[spectrum object]] $E \in Stab(\mathcal{C})$ such that

1. $H\bullet$ is degreewise [[representable functor|represented]] by $E$:

   $$
     H^\bullet \simeq Ho(\mathcal{C})(-,E_\bullet)
     \,,
   $$

1. the [[suspension isomorphism]] $\delta$ is given by the structure morphisms $\tilde \sigma_n \colon E_n \to \Omega E_{n+1}$ of the spectrum, in that

   $$
     \delta
       \colon
     H^n(-)
      \simeq
     Ho(\mathcal{C})(-,E_n)
      \stackrel{Ho(\mathcal{C})(-,\tilde\sigma_n) }{\longrightarrow}
     Ho(\mathcal{C})(-,\Omega E_{n+1})
       \simeq
     Ho(\mathcal{C})(\Sigma (-), E_{n+1})
       \simeq
     H^{n+1}(\Sigma(-))
     \,.
   $$

=--

+-- {: .proof}
###### Proof

Via prop. \ref{CohomologyFunctorOnInfinityCategoryIsBrownFunctor}, theorem \ref{BrownRepresentabilityOnPresentableInfinityCategories} gives the first clause. With this, the second clause follows by the [[Yoneda lemma]].

=--




### Milnor exact sequence
 {#S2MilnorExactSequence}


**Idea.** One tool for computing [[generalized cohomology]] [[cohomology groups|groups]] via "[[inverse limits]]" are _[[Milnor exact sequences]]_. For instance the generalized cohomology of the [[classifying space]] $B U(1)$ plays a key role in the [[complex oriented cohomology]]-theory discussed [below](#ComplexOrientedCohomologyTheory), and via the equivalence $B U(1) \simeq \mathbb{C}P^\infty$ to the [[homotopy type]] of the infinite [[complex projective space]] (def. \ref{ComplexProjectiveSpace}), which is the [[direct limit]] of finite dimensional projective spaces $\mathbb{C}P^n$, this is an [[inverse limit]] of the generalized cohomology groups of the $\mathbb{C}P^n$s. But what really matters here is the [[derived functor]] of the [[limit]]-operation -- the  [[homotopy limit]] -- and the [[Milnor exact sequence]] expresses how the naive limits receive corrections from higher "[[lim^1]]-terms". In practice one mostly proceeds by verifying conditions under which these corrections happen to disappear, these are the _[[Mittag-Leffler conditions]]_.

We need this for instance for the computation of [[Conner-Floyd Chern classes]] [below](#ConnerFloydChernClasses).

**Literature.** ([Switzer 75, section 7 from def. 7.57 on](#Switzer75), [Kochman 96, section 4.2](#Kochman96), [Goerss-Jardine 99, section VI.2](#GoerssJardine99), )




***

$\,$

## References
 {#References}

We follow in outline the textbook

* {#Kochman96} [[Stanley Kochman]], chapters I - IV of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

For some basics in [[algebraic topology]] see also

* {#Switzer75} [[Robert Switzer]], _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975.

Specifically for **S.1) Generalized cohomology** a neat account is in:

* {#AguilarGitlerPrieto02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 12 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))


For **S.2) Cobordism theory** an efficient collection of the highlights is in

* {#Malkiewich11} [[Cary Malkiewich]], _Unoriented cobordism and $M O$_, 2011 ([pdf](http://math.uiuc.edu/~cmalkiew/cobordism.pdf))

except that it omits proof of the [[Leray-Hirsch theorem]]/[[Serre spectral sequence]] and that of the [[Thom isomorphism]], but see the references there and see ([Kochman 96](#Kochman96), [Aguilar-Gitler-Prieto 02, section 11.7](#AguilarGitlerPrieto02)) for details.

For **S.3) Complex oriented cohomology** besides ([Kochman 96, chapter 4](#Kochman96)) have a look at

* {#Adams74} [[Frank Adams]], _[[Stable homotopy and generalized homology]]_, Chicago Lectures in mathematics, 1974

and

* {#Lurie10} [[Jacob Lurie]], lectures 1-10 of _[[Chromatic Homotopy Theory]]_, 2010

See also

* {#Schwede12} [[Stefan Schwede]], _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))



[[!redirects Introduction to Stable homotopy theory -- S]]
