
{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

***

$\,$

$\,$


+-- {: .standout}

[S4D2 -- Graduate Seminar on Topology](https://basis.uni-bonn.de/qisserver/rds?state=verpublish&status=init&vmfile=no&publishid=107560&moduleCall=webInfo&publishConfFile=webInfo&publishSubDir=veranstaltung)

$\;\;\;\;\;\;\;\;\;\;\;$ **Complex oriented cohomology**

$\;\;\;\;\;\;\;\;\;\;\;$ Dr. [[Urs Schreiber]]

$\;\;\;\;\;\;\;\;\;\;\;$ 

=---

$\,$

**Abstract.** _The [[category]] of those [[generalized cohomology theories]] that are equipped with a universal "[[complex oriented cohomology theory|complex]] [[orientation in generalized cohomology|orientation]]" happens to unify within it the abstract structure theory of [[stable homotopy theory]] with the concrete richness of the [[differential topology]] of [[cobordism theory]] and of the [[arithmetic geometry]] of [[formal group laws]] (of [[higher Jacobians]]), such as [[elliptic curves]]. In the seminar we work through classical results in [[algebraic topology]], organized such as to give in the end a first glimpse of the modern picture of [[chromatic homotopy theory]]._



$\,$

***

Accompanying notes.

Main page: _[[Introduction to Stable homotopy theory]]_.

***

#Contents#
* table of contents
{:toc}

## Seminar) Complex oriented cohomology


**Outline.** We start with two classical topics of [[algebraic topology]] that first run independently in parallel:

* [S.1) Generalized cohomology](#S1GeneralizedCohomology)

* [S.2) Cobordism theory](#S2CobordismTheory)

The development of either of these happens to give rise to the concept of _[[spectra]]_ and via this concept it turns out that both topics are intimately related. The unification of both is our third topic

* [S.3) Complex oriented cohomology](#ComplexOrientedCohomologyTheory)

$\,$

**Literature.** ([Kochman 96](#Kochman96)).


### **S.1)** Generalized cohomology
 {#S1GeneralizedCohomology}

**Idea.** The concept that makes [[algebraic topology]] be about methods of [[homological algebra]] applied to [[topology]] is that of [[generalized homology]] and [[generalized cohomology]]: these are [[covariant functors]] or [[contravariant functors]], respectively,

$$
  Spaces \longrightarrow Ab^{\mathbb{Z}}
$$

from (sufficiently nice) [[topological spaces]] to $\mathbb{Z}$-[[graded abelian groups]], such that a few key properties of the [[homotopy types]] of topological spaces is preserved as one passes them from [[Ho(Top)]] to the much more tractable [[abelian category]] [[Ab]].

**Literature.** ([Aguilar-Gitler-Prieto 02, chapters 7,8 and 12](#AguilarGitlerPrieto02), [Kochman 96, 3.4, 4.2](#Kochman96), [Schwede 12, II.6](#Schwede12)) 


#### Generalized cohomology functors
 {#GeneralizedHomologyAndCohomologyFunctors}

**Idea.** A [[generalized (Eilenberg-Steenrod) cohomology]] theory is such a contravariant functor which satisfies the key properties exhibited by [[ordinary cohomology]] (as computed for instance by [[singular cohomology]]), notably [[homotopy invariance]] and [[excision]], _except_ that its value on the point is not required to be concentrated in degree 0. Dually for [[generalized homology]]. There are two versions of the axioms, one for [[reduced cohomology]], and they are equivalent if properly set up.

An important example of a generalised cohomology theory other than [[ordinary cohomology]] is [[topological K-theory]]. The other two examples of key relevance below are [[cobordism cohomology]] and [[stable cohomotopy]].

**Literature.** ([Switzer 75, section 7](#Switzer75), [Aguilar-Gitler-Prieto 02, section 12 and section 9](#AguilarGitlerPrieto02), [Kochman 96, 3.4](#Kochman96)).


$\,$

##### Reduced cohomology


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

By the existence of the [[classical model structure on topological spaces]] ([thm.](Introduction+to+Stable+homotopy+theory+--+P#TopQuillenModelStructure)), its [[Quillen adjunction]] to the [[classical model structure on simplicial sets]] ([rmk.](Introduction+to+Stable+homotopy+theory+--+P#EveryTopologicalSpaceWeaklyEquivalentToACWComplex)) and the characterization of its [[homotopy category of a model category|homotopy category]] ([cor.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyCategoryOfSubcategoriesOfModelCategoriesOnGoodObjects)), the homotopy invariance axiom in def. \ref{ReducedGeneralizedCohomology} is equivalent to the functor passing to the classical pointed homotopy category. In view of this and since on CW-complexes the standard topological mapping cone construction is a model for the [[homotopy cofiber]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#StandardTopologicalMappingConeIsHomotopyCofiber)), this gives the equivalence of the two versions of the exactness axiom.

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

Prop. \ref{HomotopyTheoreticVersionOfCohomologyFunctorDefIsEquivalent} naturally suggests (e.g. [Lurie, section 1.4](#LurieHigherAlgebra)) that the concept of generalized cohomology be formulated in the generality of any abstract homotopy theory ([[model category]]), not necessarily that of (pointed) topological spaces:

+-- {: .num_defn #GeneralizedCohomologyOnGeneralInfinityCategory}
###### Definition

Let $\mathcal{C}$ be a [[model category]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#ModelCategory)) with $\mathcal{C}^{\ast/}$ its [[slice model structure|pointed model category]] ([prop.](Introduction+to+Stable+homotopy+theory+--+P#ModelStructureOnSliceCategory)). 

A **reduced additive [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology theory]] ** on $\mathcal{C}$ is 

1. a [[functor]]

   $$
     \tilde E^\bullet \;\colon \; Ho(\mathcal{C})^{op} \longrightarrow Ab^{\mathbb{Z}}
   $$

1. a [[natural isomorphism]] ("[[suspension isomorphisms]]") of degree +1

   $$
     \sigma \; \colon \; \tilde E^\bullet \longrightarrow \tilde E^{\bullet+1} \circ \Sigma
   $$

such that 

* **(exactness)** $\tilde E^\bullet$ takes [[homotopy cofiber sequences]] to [[exact sequences]].

=--

Finally we need the following terminology:

+-- {: .num_defn }
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



##### Unreduced cohomology

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




##### Relation between unreduced and reduced cohomology
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

##### Generalized homology functors

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



#### Brown representability theorem
 {#BrownRepresentabilityTheorem}


**Idea.** Given any [[functor]] such as the generalized (co)homology functor [above](#GeneralizedHomologyAndCohomologyFunctors), an important question to ask is whether it is a _[[representable functor]]_. Due to the $\mathbb{Z}$-grading and the [[suspension isomorphisms]], if a generalized (co)homology functor is representable at all, it must be represented by a $\mathbb{Z}$-indexed sequence of [[pointed topological spaces]] such that the [[reduced suspension]] of one is comparable to the next one in the list. This is a _[[spectrum]]_ or more specifically: a _[[sequential spectrum]]_ .

Whitehead observed that indeed every [[spectrum]] represents a generalized (co)homology theory.  The _[[Brown representability theorem]]_ states that, conversely, every generalized (co)homology theory is represented by a spectrum, subject to conditions of additivity.

As a first application, [[Eilenberg-MacLane spectra]] representing [[ordinary cohomology]] may be characterized via Brown representability.

**Literature.** ([Switzer 75, section 9](#Switzer75), [Aguilar-Gitler-Prieto 02, section 12](#AguilarGitlerPrieto02), [Kochman 96, 3.4](#Kochman96))


##### Traditional discussion
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

An **[[Omega-spectrum]]** $X$ ([def.](Introduction+to+Stable+homotopy+theory+--+1#OmegaSpectrum)) is 

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

+-- {: .num_prop}
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

##### Homotopy-theoretic discussion

Using abstract [[homotopy theory]] in the guise of [[model category]] theory (see the _[[Introduction to Stable homotopy theory -- P|lecture notes on classical homotopy theory]]), the traditional proof and further discussion of the [[Brown representability theorem]] [above](#BrownRepresentabilityTraditional) becomes more transparent ([Lurie, section 1.4.1](#LurieHigherAlgebra), for exposition see also [Mathew 11](Brown+representability+theorem#Mathew11)). 

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


See also ([Lurie, example 1.4.1.4](#LurieHigherAlgebra))

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

([Lurie, p. 114, Lemma star](#LurieHigherAlgebra))

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

([Lurie, theorem 1.4.1.2](#LurieHigherAlgebra))

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


#### Milnor exact sequence
 {#S2MilnorExactSequence}


**Idea.** One tool for computing [[generalized cohomology]] [[cohomology groups|groups]] via "[[inverse limits]]" are _[[Milnor exact sequences]]_. For instance the generalized cohomology of the [[classifying space]] $B U(1)$ plays a key role in the [[complex oriented cohomology]]-theory discussed [below](#ComplexOrientedCohomologyTheory), and via the equivalence $B U(1) \simeq \mathbb{C}P^\infty$ to the [[homotopy type]] of the infinite [[complex projective space]], which is the [[direct limit]] of finite dimensional projective spaces $\mathbb{C}P^n$, this is an [[inverse limit]] of the generalized cohomology groups of the $\mathbb{C}P^n$s. But what really matters here is the [[derived functor]] of the [[limit]]-operation -- the  [[homotopy limit]] -- and the [[Milnor exact sequence]] expresses how the naive limits receive corrections from higher "[[lim^1]]-terms". In practice one mostly proceeds by verifying conditions under which these corrections happen to disappear, these are the _[[Mittag-Leffler conditions]]_.

We need this for instance for the computation of [[Conner-Floyd Chern classes]] [below](#ConnerFloydChernClasses).

**Literature.** ([Switzer 75, section 7 from def. 7.57 on](#Switzer75), [Kochman 96, section 4.2](#Kochman96), [Goerss-Jardine 99, section VI.2](#GoerssJardine99), )

##### $Lim^1$ and Mittag-Leffler condition
 {#Lim1}

+-- {: .num_defn #TheBoundaryMapDefiningLim1}
###### Definition

Given a [[tower]] $A_\bullet$ of [[abelian groups]]

$$
  \cdots \to A_3 \stackrel{f_2}{\to} A_2 \stackrel{f_1}{\to} A_1 \stackrel{f_0}{\to} A_0
$$

write

$$
  \partial
    \;\colon\;
  \underset{n}{\prod} A_n
    \longrightarrow
  \underset{n}{\prod} A_n
$$

for the homomorphism given by 

$$
  \partial \;\colon\; 
    (a_n)_{n \in \mathbb{N}} 
  \mapsto  
    (a_n - f_n(a_{n+1}))_{n \in \mathbb{N}}.

=--

+-- {: .num_defn #LimitAsKernelAnalogousToLim1}
###### Remark

The [[limit]] of a sequence as in def. \ref{TheBoundaryMapDefiningLim1} -- hence the group $\underset{\longleftarrow}{\lim}_n A_n$ universally equipped with morphisms $\underset{\longleftarrow}{\lim}_n A_n \overset{p_n}{\to} A_n$ such that all

$$
  \array{
     && \underset{\longleftarrow}{\lim}_n A_n
     \\
     & {}^{\mathllap{p_{n+1}}}\swarrow && \searrow^{\mathrlap{p_n}}
     \\
     A_{n+1} && \overset{f_n}{\longrightarrow} && A_n
  }
$$

[[commuting diagram|commute]] -- is equivalently the [[kernel]] of the morphism $\partial$ in def. \ref{TheBoundaryMapDefiningLim1}.

=--

+-- {: .num_defn #Lim1ViaCokernel}
###### Definition

Given a [[tower]] $A_\bullet$ of [[abelian groups]]

$$
  \cdots \to A_3 \stackrel{f_2}{\to} A_2 \stackrel{f_1}{\to} A_1 \stackrel{f_0}{\to} A_0
$$

then its "[[lim^1]]" $\underset{\longleftarrow}{\lim}^1 A_\bullet$ is the [[cokernel]] of the map $\partial$ in def. \ref{TheBoundaryMapDefiningLim1}, hence the group that makes a [[long exact sequence]] of the form

$$
  0 \to 
  \underset{\longleftarrow}{\lim}_n A_n
  \longrightarrow
  \underset{n}{\prod} A_n
   \stackrel{\partial}{\longrightarrow}
  \underset{n}{\prod} A_n
    \longrightarrow
  \underset{\longleftarrow}{\lim}^1_n A_n
  \to 0
  \,,
$$


=--

+-- {: .num_defn #MittagLefflerCondition}
###### Definition

A tower $A_\bullet$ of [[abelian groups]]

$$
  \cdots \to A_3 \to A_2 \to A_1 \to A_0
$$

is said to satify the **[[Mittag-Leffler condition]]** if for all $k$ there exists $i \geq k$ such that for all $j \geq i \geq k$ the [[image]] of the [[homomorphism]] $A_i \to A_k$ equals that of $A_j \to A_k$
 
$$
  im(A_i \to A_k) \simeq im(A_j \to A_k)
  \,.
$$

=--

+-- {: .num_example}
###### Example

The Mittag-Leffler condition, def. \ref{MittagLefflerCondition}, is satisfied in particular when all morphisms $A_{i+1}\to A_i$ are [[epimorphisms]] (hence [[surjections]] of the underlying [[sets]]).

=--

+-- {: .num_prop #Lim1VanihesUnderMittagLeffler}
###### Proposition

If a tower $A_\bullet$ satisfies the [[Mittag-Leffler condition]], def. \ref{MittagLefflerCondition}, then its $\underset{\leftarrow}{\lim}^1$ vanishes:

$$
  \underset{\longleftarrow}{\lim}^1 A_\bullet = 0
  \,.
$$

=--

([Switzer 75, theorem 7.75](#Switzer75), [Kochmann 96, prop. 4.2.3](#Kochmann96))


##### Mapping telescopes

Given a sequence 

$$
  X_\bullet
  =
  \left(
  X_0 
   \overset{f_0}{\longrightarrow}
  X_1
   \overset{f_1}{\longrightarrow}
  X_2
   \overset{f_2}{\longrightarrow}
  \cdots
  \right)
$$

of ([[pointed topological space|pointed]]) [[topological spaces]], then its _mapping telescope_ is the result of forming the (reduced) [[mapping cylinder]] $Cyl(f_n)$ for each $n$ and then attaching all these cylinders to each other in the canonical way


+-- {: .num_defn #MappingTelescope}
###### Definition

For

$$
  X_\bullet
  =
  \left(
  X_0 
   \overset{f_0}{\longrightarrow}
  X_1
   \overset{f_1}{\longrightarrow}
  X_2
   \overset{f_2}{\longrightarrow}
  \cdots
  \right)
$$

a sequence  in [[Top]], its **mapping telescope** is the [[quotient topological space]] of the [[disjoint union]] of [[product topological spaces]]

$$
  Tel(X_\bullet)
  \coloneqq
  \left(
  \underset{n \in \mathbb{N}}{\sqcup}  
  \left(
    X_n \times [n,n+1]
  \right)
  \right)/_\sim
$$

where the [[equivalence relation]] quotiented out is

$$
  (x_n, n) \sim (f(x_n), n+1)
$$

for all $n\in \mathbb{N}$ and $x_n \in X_n$.

Analogously for $X_\bullet$ a sequence of [[pointed topological spaces]] then use [[reduced cylinders]] ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#StandardReducedCyclinderInTop)) to set

$$
  Tel(X_\bullet)
  \coloneqq
  \left(
  \underset{n \in \mathbb{N}}{\sqcup}  
  \left(
    X_n \wedge [n,n+1]_+
  \right)
  \right)/_\sim
  \,.
$$

=--

+-- {: .num_defn #TelescopeOfCWComplexEquivalentToTheOriginal}
###### Definition

For $X_\bullet$ the sequence of stages of a ([[pointed topological space|pointed]]) [[CW-complex]] $X = \underset{\longleftarrow}{\lim}_n X_n$, then the canonical map

$$
  Tel(X_\bullet)
  \longrightarrow
  X
$$

from the [[mapping telescope]], def. \ref{MappingTelescope}, is a [[weak homotopy equivalence]].

=--


+-- {: .proof}
###### Proof

Write in the following $Tel(X)$ for $Tel(X_\bullet)$ and write $Tel(X_n)$ for the mapping telescop of the substages of the finite stage $X_n$ of $X$. It is intuitively clear that each of the projections at finite stage

$$
  Tel(X_n) \longrightarrow X_n
$$

is a [[homotopy equivalence]], hence ([prop.](Introduction+to+Stable+homotopy+theory+--+P#TopologicalHomotopyEquivalencesAreWeakHomotopyEquivalences)) a weak homotopy equivalence. A concrete construction of a homotopy inverse is given for instance in ([Switzer 75, proof of prop. 7.53](#Switzer75)).

Moreover, since spheres are [[compact object|compact]], so that elements of [[homotopy groups]] $\pi_q(Tel(X))$ are represented at some finite stage $\pi_q(Tel(X_n))$ it follows that 

$$
  \underset{\longrightarrow}{\lim}_n \pi_q(Tel(X_n)) 
    \overset{\simeq}{\longrightarrow} 
  \pi_q(Tel(X))
$$

are [[isomorphisms]] for all $q\in \mathbb{N}$ and all choices of basepoints (not shown). 

Together these two facts imply that in the following commuting square, three morphisms are isomorphisms, as shown.

$$
  \array{
    \underset{\longleftarrow}{\lim}_n \pi_q(Tel(X_n))
    &\overset{\simeq}{\longrightarrow}&
    \pi_q(Tel(X))
    \\
    {}^{\mathllap{\simeq}}\downarrow && \downarrow
    \\
    \underset{\longleftarrow}{\lim}_n \pi_q(X_n)
    &\underset{\simeq}{\longrightarrow}&
    \pi_q(X)    
  }
  \,.
$$

Therefore also the remaining morphism is an isomorphism ([[two-out-of-three]]). Since this holds for all $q$ and all basepoints, it is a weak homotopy equivalence.

=--

##### Milnor sequences

+-- {: .num_prop #MilorSequenceForReducedCohomologyOnCWComplex}
###### Proposition

Let $X$ be a [[pointed topological space|pointed]] [[CW-complex]], $X = \underset{\longleftarrow}{\lim}_n X_n$ and let $\tilde E^\bullet$ an [additive](#WedgeAxiom) [[reduced cohomology theory]], def. \ref{ReducedGeneralizedCohomology}.

Then the canonical morphisms make a [[short exact sequence]]

   $$
     0 
      \to 
     \underset{\longleftarrow}{\lim}^1_n \tilde E^{\bullet-1}(X_n)
      \longrightarrow
     \tilde E^{\bullet}(X)
      \longrightarrow
     \underset{\longleftarrow}{\lim}_n \tilde E^{\bullet}(X_n)
     \to 
     0
     \,,
   $$

saying that 

1. the failure of the canonical comparison map $\tilde E^\bullet(X) \to \underset{\longleftarrow}{\lim} \tilde E^\bullet(X_n)$ to the [[limit]] of the [[cohomology groups]] on the finite stages to be an [[isomorphism]] is at most in a non-vanishing [[kernel]];

1. this kernel is precisely the $\lim^1$ (def. \ref{Lim1ViaCokernel}) of the cohomology groups at the finite stages in one degree lower.

=--

e.g. ([Switzer 75, prop. 7.66](#Switzer75), [Kochmann 96, prop. 4.2.2](#Kochmann96))


+-- {: .proof}
###### Proof


For 

$$
  X_\bullet
  = 
  \left(
    X_0 
      \overset{i_0}{\hookrightarrow}
    X_1 
      \overset{i_1}{\hookrightarrow}
    X_2 
      \overset{i_1}{\hookrightarrow}
    \cdots
  \right)
$$ 

the sequence of stages of the ([[pointed topological space|pointed]]) [[CW-complex]] $X = \underset{\longleftarrow}{\lim}_n X_n$, write

$$
  \begin{aligned}
    A_X 
    &\coloneqq 
    \underset{n \in \mathbb{N}}{\sqcup} X_{2n} \times [2n,{2n}+1];
  \\
    B_X 
    &\coloneqq 
    \underset{n \in \mathbb{N}}{\sqcup} X_{(2n+1)} \times [2n+1,{2n}+2].
  \end{aligned}
$$

for the [[disjoint unions]] of the [[cylinders]] over all the stages in even and all those in odd degree, respectively.

These come with canonical inclusion maps into the [[mapping telescope]] $Tel(X_\bullet)$ ([def.](mapping+telescope#MappingTelescope)), which we denote by

$$
  \array{
    A_X && && B_X
    \\
    & {}_{\mathllap{\iota_{A_x}}}\searrow && \swarrow_{\mathrlap{\iota_{B_x}}}
    \\
    && Tel(X_\bullet)
  }
  \,.
$$

Observe that 

1. $A_X \cup B_X \simeq Tel(X_\bullet)$;

1. $A_X \cap B_X \simeq \underset{n \in \mathbb{N}}{\sqcup} X_n$;

and that there are [[homotopy equivalences]]

1. $A_X \simeq \underset{n \in \mathbb{N}}{\sqcup} X_{2n+1}$

1. $B_X \simeq \underset{n \in \mathbb{N}}{\sqcup} X_{2n}$

1. $Tel(X_\bullet) \simeq X$.

The first two are obvious, the third is [this proposition](mapping+telescope#TelescopeOfCWComplexEquivalentToTheOriginal). 

This implies that the [[Mayer-Vietoris sequence]] ([prop.](generalized+cohomology#MayerVietorisSequenceInGeneralizedCohomology)) for $\tilde E^\bullet$ on the cover $A \sqcup B \to X$ is isomorphic to the bottom horizontal sequence in the following diagram:

$$
  \array{
     \tilde E^{\bullet-1}(A_X)\oplus \tilde E^{\bullet-1}(B_X)
      &\longrightarrow&
    \tilde E^{\bullet-1}(A_X \cap B_X)
      &\longrightarrow& 
    \tilde E^\bullet(X)
      &\overset{(\iota_{A_x})^\ast - (\iota_{B_x})^\ast}{\longrightarrow}&
    \tilde E^\bullet(A_X)\oplus \tilde E^\bullet(B_X)
      &\overset{}{\longrightarrow}&
    \tilde E^\bullet(A_X \cap B_X)
    \\
    \downarrow^{\mathrlap{\simeq}}
     &&
    \downarrow^{\mathrlap{\simeq}} 
      && 
    \downarrow^{\mathrlap{=}}
      &&
    {}^{\mathllap{(id, -id)}}\downarrow^{\mathrlap{\simeq}}
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    \underset{n}{\prod}\tilde E^{\bullet-1}(X_n)
      &\underset{\partial}{\longrightarrow}&
    \underset{n}{\prod}\tilde E^{\bullet-1}(X_n) 
      &\longrightarrow& 
    \tilde E^\bullet(X)
      &\overset{(i_n^\ast)_{n}}{\longrightarrow}&
    \underset{n}{\prod}\tilde E^\bullet(X_n)
      &\underset{\partial}{\longrightarrow}&
    \underset{n}{\prod}\tilde E^\bullet(X_n)
  }
  \,,
$$

hence that the bottom sequence is also a [[long exact sequence]].

To identify the morphism $\partial$, notice that it comes from pulling back $E$-cohomology classes along the inclusions $A \cap B \to A$ and $A\cap B \to B$. Comonentwise these are the inclusions of each $X_n$ into the left and the right end of its cylinder inside the [[mapping telescope]], respectively. By the construction of the [[mapping telescope]], one of these ends is embedded via $i_n \colon X_n \hookrightarrow X_{n+1}$ into the cylinder over $X_{n+1}$. In conclusion, $\partial$ acts by

$$
  \partial
    \;\colon\;
  (a_n)_{n \in \mathbb{N}}
    \mapsto
  ( a_n - i_n^\ast(a_{n+1}) )
  \,.
$$

(The relative sign is the one in $(\iota_{A_x})^\ast - (\iota_{B_x})^\ast$ originating in the definition of the [[Mayer-Vietoris sequence]] and properly propagated to the bottom sequence while ensuring that $\tilde E^\bullet(X)\to \prod_n \tilde E^\bullet(X_n)$ is really $(i_n^\ast)_n$ and not $(-1)^n(i_n^\ast)_n$, as needed for the statement to be proven.)

This is the morphism from def. \ref{TheBoundaryMapDefiningLim1} for the sequence

$$
   \cdots
    \to 
  \tilde E^\bullet(X_{n+1}) 
    \overset{i_n^\ast}{\longrightarrow}
  \tilde E^\bullet(X_n)
    \overset{i_n^\ast}{\longrightarrow}
  \tilde E^{\bullet}(X_{n-1})
   \to
   \cdots
 \,.
$$

Hence truncating the above long exact sequence by forming kernel and cokernel of $\partial$, the result follows via remark \ref{LimitAsKernelAnalogousToLim1} and definition \ref{Lim1ViaCokernel}.

=--

In contrast:

+-- {: .num_prop}
###### Proposition

Let $X$ be a [[pointed topological space|pointed]] [[CW-complex]], $X = \underset{\longleftarrow}{\lim}_n X_n$.

For $\tilde E_\bullet$ an additive reduced [[generalized homology theory]], then

   $$
     \underset{\longrightarrow}{\lim}_n \tilde E_\bullet(X_n)
     \overset{\simeq}{\longrightarrow}
     \tilde E_\bullet(X)
   $$

   is an [[isomorphism]].

=--

([Switzer 75, prop. 7.53](#Switzer75))





#### Serre-Atiyah-Hirzebruch spectral sequence
 {#SerreAtiyahHirzebruchSpectralSequence}

**Idea.** Another important tool for computing [[generalized cohomology]] is to reduce it to the computation of [[ordinary cohomology]] with [[coefficients]]. Given a [[generalized cohomology theory]] $E$, there is a [[spectral sequence]] known as the _[[Atiyah-Hirzebruch spectral sequence]]_ (AHSS) which serves to compute $E$-cohomology of $F$-[[fiber bundles]] over a [[simplicial complex]] $X$ in terms of [[ordinary cohomology]] with [[coefficients]] in the generalized cohomology $E^\bullet(F)$ of the fiber. For $E = $ [[HA]] this is known as the _[[Serre spectral sequence]]_.

The [[Atiyah-Hirzebruch spectral sequence]] in turn is a consequence of the "[[Cartan-Eilenberg spectral sequence]]" which arises from the [[exact couple]] of [[relative cohomology]] groups of the skeleta of the CW-complex, and whose first page is the relative cohomology groups for codimension-1 skeleta.

We need the AHSS for instance for the computation of [[Conner-Floyd Chern classes]] [below](#ConnerFloydChernClasses).


**Literature.** ([Kochman 96, section 2.2 and 4.2](#Kochman96)) 

See also the accompanying  _[[Introduction to Stable homotopy theory -- I|lecture notes on spectral sequences]]_. 

##### Converging spectral sequences

+-- {: .num_defn #CohomologySpectralSequence}
###### Definition

A **cohomology [[spectral sequence]]** $\{E_r^{p,q}, d_r\}$ is

1. a sequence $\{E_r^{\bullet,\bullet}\}$ (for $r \in \mathbb{N}$, $r \geq 2$) of [[bigraded object|bigraded]] [[abelian groups]];

1. a sequence of [[linear maps]] ("[[differentials]]") 

   $$
     \{d_r \colon E_r^{\bullet,\bullet} \longrightarrow E_r^{\bullet+r, \bullet-r+1}\}
   $$

such that 

* $H_{r+1}^{\bullet,\bullet}$ is the [[cochain cohomology]] of $d_r$, i.e. $E_{r+1}^{\bullet, \bullet} = H(E_r^{\bullet,\bullet},d_r)$, for all $r \in \mathbb{N}$, $r \geq 1$.

Given a $\mathbb{Z}$-[[graded abelian group]]_ $C^\bullet$ equipped with a decreasing [[filtration]]

$$
  C^\bullet \supset \cdots \supset F^s C^\bullet \supset F^{s+1} C^\bullet \supset \cdots \supset 0$$

such that

$$
  C^\bullet = \underset{s}{\cup} F^s C^\bullet \;\;\;\; and \;\;\;\; 0 = \underset{s}{\cap} F^s C^\bullet
$$

then the spectral sequence is said to **converge** to  $C^\bullet$, denoted, 

$$
  E_2^{\bullet,\bullet} \Rightarrow C^\bullet
$$

if

1.  in each bidegree $(s,t)$ the sequence $\{E_r^{s,t}\}_r$ eventually becomes constant on a group 

    $E_\infty^{s,t} \coloneqq E_{\gg 1}^{s,t}$;

1. $E_\infty^{\bullet,\bullet}$ is the [[associated graded]] of the filtered $C^\bullet$ in that

   $E_\infty^{s,t} \simeq F^s C^{s+t} / F^{s+1}C^{s+t}$.


{#MultiplicativeSpectralSequence} The converging spectral sequence is called a **[[multiplicative spectral sequence]]** if 

1. $\{E_2^{\bullet,\bullet}\}$ is equipped with the structure of a [[bigraded object|bigraded]] [[associative algebra|algebra]];

1. $F^\bullet C^\bullet$ is equipped with the structure of a filtered [[graded algebra]] ($F^p C^k \cdot F^q C^l \subset F^{p+q} C^{k+l}$);

such that

1. each $d_{r}$ is a [[derivation]] with respect to the (induced) algebra structure on ${E_r^{\bullet,\bullet}}$, graded of degree 1 with respect to total degree;

1. the multiplication on $E_\infty^{\bullet,\bullet}$ is compatible with that on $C^\bullet$.

=--

A useful way to generate spectral sequences is via [[exact couples]]:

+-- {: .num_defn #ExactCoupleAndDerivedExactCouple}
###### Definition

An **[[exact couple]]** is three [[homomorphisms]] of [[abelian groups]] of the form

$$
  \array{
    D && \stackrel{g}{\longrightarrow} && D
    \\
    & {}_{\mathllap{f}}\nwarrow && \swarrow_{\mathrlap{h}}
    \\
    && E
  }
$$

such that the [[image]] of one is the [[kernel]] of the next.

$$
  im(h) = ker(f)\,,\;\;\; im(f) = ker(g)\,, \;\;\; im(g) = ker(f)
  \,.
$$

Given an exact couple, then its **derived exact couple** is

$$
  \array{
    im(g) && \stackrel{g}{\longrightarrow} && im(g)
    \\
    & {}_{\mathllap{f}}\nwarrow && \swarrow_{\mathrlap{h \circ g^{-1}}}
    \\
    && H(E, h \circ f)
  }
  \,.
$$

=--

+-- {: .num_prop #CohomologicalSpectralSequenceOfAnExactCouple}
###### Proposition
**(cohomological spectral sequence of an exact couple)**

Given an exact couple, def. \ref{ExactCoupleAndDerivedExactCouple}, of the form

$$
  \array{
    D_1 && \stackrel{g_1}{\longrightarrow} && D_1
    \\
    & {}_{\mathllap{f_1}}\nwarrow && \swarrow_{\mathrlap{h_1}}
    \\
    && E_1
  }
$$

then its derived exact couple 

$$
  \array{
    D_2 && \stackrel{g_2}{\longrightarrow} && D_2
    \\
    & {}_{\mathllap{f_2}}\nwarrow && \swarrow_{\mathrlap{h_2}}
    \\
    && E_2
  }
$$

is itself an exact couple. Accordingly there is induced a sequence of exact couples 

$$
  \array{
    D_r && \stackrel{g_r}{\longrightarrow} && D_r
    \\
    & {}_{\mathllap{f_r}}\nwarrow && \swarrow_{\mathrlap{h_r}}
    \\
    && E_r
  }
  \;\;\;\;\;\;
  for \; r \in \mathbb{N}
  \,.
$$

If the abelian groups $D$ and $E$ are equipped with [[bigraded object|bigrading]] such that

$$
  deg(f) = (0,0)\,,\;\;\;\; deg(g) = (-1,1)\,,\;\;\; deg(h) = (1,0)
$$

then $\{E_r^{\bullet,\bullet}, d_r\}$ with

$$
  \begin{aligned}
    d_r & \coloneqq h_r \circ f_r
     \\
     & = h \circ g^{-r+1} \circ f
  \end{aligned}
$$

is a cohomological [[spectral sequence]], def. \ref{CohomologySpectralSequence}.

If for each bidegree $(s,t)$ there exists $R \gg 1$ such that for all $r \geq R$ 

1. $g \colon D^{s+R,t-R} \stackrel {\simeq}{\longrightarrow} D^{s+R -1, t-R-1}$;

1. $g\colon D^{s-R+1, t+R-1} \stackrel{0}{\longrightarrow} D^{s-R,t+R-1}$ 

then this spectral sequence converges to the [[inverse limit]] group

$$
  G^\bullet 
    \coloneqq 
  \underset{\longleftarrow}{\lim}
  \left(
    \cdots \stackrel{g}{\to} D^{s,\bullet-s} \stackrel{g}{\longrightarrow} D^{s-1, \bullet - s + 1}
   \stackrel{g}{\to}
   \cdots
  \right)
$$

filtered by 

$$
  F^p G^\bullet \coloneqq ker(G^\bullet \to D^{p-1, \bullet - p+1})
  \,.
$$

=--

+-- {: .proof}
###### Proof

By exactness of the exact couple, the [[kernel]]

$$
  ker(d_{r-1}) \coloneqq ker(h \circ g^{-r+2} \circ f)
$$

consists of those elements $x$ such that $g^{-r+2} (f(x)) = g(y)$, for some $y$, hence 

$$
  ker(d_{r-1}) = f^{-1}(g^{r-1}(D^{s+r-1,t-r+1}))
  \,.
$$

By assumption there is for each $(s,t)$ an $R$ such that for all $r \geq R$ then $ker(d_{r-1})$ is independent of $r$. 

Moreover, $im(d_{r-1})$ consists of the image under $h$ of those $x$ such that $g^{r-2}(x)$ is in the image of $f$, hence (by exactness of the exact couple) such that $g^{r-2}(x)$ is in the kernel of $g$, hence such that $x$ is in the kernel of $g^{r-1}$. If $r \gt R$ then by assumption $g^{r-1} = 0$ and so then $im(d_{r-1}) = im(h)$.

It follows that

$$
  \begin{aligned}
    E_\infty^{p,n-p}
    & =
    ker(d_R)/im(d_R)
    \\
    &
    \simeq
    f^{-1}(im(g^R))/im(h)
    \\
    &
    \simeq
    im(g^R) \cap im(f)
    \\
    & 
    \simeq
    im(g^R) \cap ker(g)
  \end{aligned}
$$

where in last two steps we used once more the exactness of the exact couple.

The last group is that of elements $x \in G^n$ which map to zero in $D^{p-1,n-p+1}$ and where two such are identified if they agree in $D^{p,n-p}$, hence indeed 

$$
  E_\infty^{p,n-p} \simeq F^p G^n / F^{p+1} G^n
  \,.
$$


=--

##### The AHSS

The following proposition requires, in general, to evaluate cohomology functors not just on [[CW-complexes]], but on all topological spaces. Hence we invoke prop. \ref{HomotopyTheoreticVersionOfCohomologyFunctorDefIsEquivalent} to regard a [[reduced cohomology theory]] as a contravariant functor on all pointed topological spaces, which sends [[weak homotopy equivalences]] to isomorphisms (def. \ref{ReducedGeneralizedCohomologyHomotopyHomotopicalFunctor}).


+-- {: .num_prop #AHSSExistence}
###### Proposition
**(Serre-Cartan-Eilenberg-Whitehead-Atiyah-Hirzebruch spectral sequence)**

Let $A^\bullet$ be a an [additive](#UnreducedAdditivity)  unreduced  [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology functor]]  (def. \ref{ReducedGeneralizedCohomologyHomotopyHomotopicalFunctor}). Let $B$ be a [[simply connected topological space|simply connected]] [[CW-complex]] and let $X \stackrel{\pi}{\to} B$ be a [[Serre fibration]] with [[fibers]] $F$. 

$$
  \array{
    F &\longrightarrow& X
    \\
    && \downarrow^{\mathrlap{\in Fib_{cl}}}
    \\
    && B
  }
  \,.
$$

If at least one of the following two conditions is met

* $B$ is [[finite number|finite]]-dimensional as a [[CW-complex]];

* $A^\bullet(F)$ is bounded below in degree and the sequences $\cdots to A^p(X_{n+1}) \to A^p(X_n) \to \cdots$ satisfy the [[Mittag-Leffler condition]] (def. \ref{MittagLefflerCondition}) for all $p$;

then there is a cohomology [[spectral sequence]], def. \ref{CohomologySpectralSequence}, whose $E_2$-page is the [[ordinary cohomology]] $H^\bullet(B,A^\bullet(F))$ of $B$ with [[coefficients]] in the $A$-[[cohomology groups]] $A^\bullet(F)$ of the fiber, and which converges to the $A$-cohomology groups of the total space

$$
  E_2^{p,q} 
    = 
  H^p(B, A^q(F)) 
   \;
    \Rightarrow 
   \;
  A^\bullet(X)
$$ 

with respect to the filtering given by

$$
  F^p A^\bullet(X) 
   \coloneqq 
  ker\left(
    A^\bullet(X) 
      \to 
    A^\bullet(X_{p-1})
  \right)
  \,,
$$

where $X_{p} \coloneqq \pi^{-1}(B_{p})$ is the fiber over the $p$th stage of the [[CW-complex]] $B = \underset{\longleftarrow}{\lim}_n B_n$.


=--

+-- {: .proof #ProofOfTheAHSS}
###### Proof

The [exactness axiom](#ExactnessUnreduced) for $A$ gives an [[exact couple]], def. \ref{ExactCoupleAndDerivedExactCouple}, of the form

$$
  \array{
    \underset{s,t}{\prod} A^{s+t}(X_{s})
    &&
      \stackrel{}{\longrightarrow} 
    &&
    \underset{s,t}{\prod} A^{s+t}(X_{s})
    \\
    & \nwarrow && \swarrow
    \\
    && \underset{s,t}{\prod} A^{s+t}(X_{s}, X_{s-1})
  }
  \;\;\;\;\;\;\;
  \left(
      \array{
        A^{s+t}(X_s) & \longrightarrow & A^{s+t}(X_{s-1})
        \\
        \uparrow && \downarrow_{\mathrlap{\delta}}
        \\
        A^{s+t}(X_s, X_{s-1}) && A^{s+t+1}(X_{s}, X_{s-1})
      }
  \right)
  \,,
$$

where we take $X_{\gg 1} = X$ and $X_{\lt 0} = \emptyset$. 

In order to determine the $E_2$-page, we analyze the $E_1$-page: By definition

$$
  E_1^{s,t}
   =
  A^{s+t}(X_s, X_{s-1})
$$


Let $C(s)$ be the set of $s$-dimensional cells of $B$, and notice that for $\sigma \in C(s)$ then 

$$
  (\pi^{-1}(\sigma), \pi^{-1}(\partial \sigma)) \simeq (D^n, S^{n-1}) \times F_\sigma
  \,,
$$

where $F_\sigma$ is [[weak homotopy equivalence|weakly homotopy equivalent]] to $F$ ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#FibersOfSerreFibrations)).
 
This implies that 

$$
  \begin{aligned}
    E_1^{s,t}
    & \coloneqq
    A^{s+t}(X_s, X_{s-1})
    \\
    & \simeq \tilde A^{s+t}(X_s/X_{s-1})
    \\
    & \simeq \tilde A^{s+t}(\underset{\sigma \in C(n)}{\vee} S^s \wedge F_+)
    \\
    & \simeq \underset{\sigma \in C(s)}{\prod} \tilde A^{s+t}(S^s \wedge F_+)
    \\
    & \simeq \underset{\sigma \in C(s)}{\prod} \tilde A^t(F_+)
    \\
    & \simeq \underset{\sigma \in C(s)}{\prod} A^t(F)
    \\
    & \simeq C^s_{cell}(B,A^t(F))
  \end{aligned}
  \,,
$$

where we used the relation to [[reduced cohomology]] $\tilde A$, prop. \ref{ReducedToUnreducedGeneralizedCohomology} together with lemma \ref{EvaluationOfCohomologyTheoryOnGoodPairIsEvaluationOnQuotient}, 
then the [wedge axiom](#WedgeAxiom) and the [suspension isomorphism](#SuspensionIsomorphismForReducedGeneralizedCohomology) of the latter. 

The last group $C^s_{cell}(B,A^t(F))$ appearing in this sequence of isomorphisms is that of [[cellular cohomology|cellular cochains]] ([def.](Introduction+to+Stable+homotopy+theory+--+I#CellularChainComplex)) of degree $s$ on $B$ with [[coefficients]] in the group $A^t(F)$. 

Since [[cellular cohomology]] of a [[CW-complex]] agrees with its [[singular cohomology]] ([thm.](Introduction+to+Stable+homotopy+theory+--+I#CelluarEquivalentToSingularFromSpectralSequence)), hence with its [[ordinary cohomology]], to conclude that the $E_2$-page is as claimed, it is now sufficient to show that the differential $d_1$ coincides with the differential in the [[cellular cochain complex]] ([def.](Introduction+to+Stable+homotopy+theory+--+I#CellularChainComplex)). 

We discuss this now for $\pi = id$, hence $X = B$ and $F = \ast$. The general case works the same, just with various factors of $F$ appearing in the following: 

Consider the following diagram, which [[commuting diagram|commutes]] due to the [[natural transformation|naturality]] of the [connecting homomorphism](#ConnectingHomomorphismOfUnreducedCohomology) $\delta$ of $A^\bullet$:

$$
  \array{
    \partial^\ast
     \colon
    & C^{s-1}_{cell}(X,A^t(\ast))
      & =&  \underset{i \in I_{s-1}}{\prod} A^t(\ast)
      && \longrightarrow &&
    \underset{i \in I_s}{\prod} A^t(\ast)
    & = & 
    C_{cell}^{s}(X,A^t(\ast))
    \\
    && & {}^{\mathllap{\simeq}}\downarrow && && \downarrow^{\mathrlap{\simeq}}
    \\
    && & \underset{i \in I_{s-1}}{\prod} \tilde A^{s+t-1}(S^{s-1}) 
      && &&
    \underset{i \in I_s}{\prod} \tilde A^{s+t}(S^{s}) 
    \\
    && & {}^{\mathllap{\simeq}}\downarrow && && \downarrow^{\mathrlap{\simeq}}
    \\
    && d_1 \colon &
    A^{s+t-1}(X_{s-1}, X_{s-2})
      &\overset{}{\longrightarrow}&
    A^{s+t-1}(X_{s-1})
      &\overset{\delta}{\longrightarrow}&
    A^{s+t}(X_s, X_{s-1})
    \\
    && & 
    \downarrow && \downarrow && \downarrow
    \\
    && & 
    A^{s+t-1}(S^{s-1}, \emptyset)
      &\overset{}{\longrightarrow}&
    A^{s+t-1}(S^{s-1})
      &\overset{\delta}{\longrightarrow}&
    A^{s+t}(D^s , S^{s-1})
  }
  \,.
$$

Here the bottom vertical morphisms are those induced from any chosen cell inclusion $(D^s , S^{s-1}) \hookrightarrow (X_s, X_{s-1})$.

The differential $d_1$ in the spectral sequence is the middle horizontal composite. From this the vertical isomorphisms give the top horizontal map. But the bottom horizontal map identifies this top horizontal morphism componentwise with the restriction to the boundary of cells. Hence the top horizontal morphism is indeed the coboundary operator $\partial^\ast$ for the [[cellular cohomology]] of $X$ with coefficients in $A^\bullet(\ast)$ ([def.](Introduction+to+Stable+homotopy+theory+--+I#CellularChainComplex)). This cellular cohomology coincides with [[singular cohomology]] of the [[CW-complex]] $X$ ([thm.](https://ncatlab.org/nlab/show/Introduction+to+Stable+homotopy+theory+--+I#CelluarEquivalentToSingularFromSpectralSequence)), hence computes the [[ordinary cohomology]] of $X$.

Now to see the convergence. If $B$ is finite dimensional then the convergence condition as stated in prop. \ref{CohomologicalSpectralSequenceOfAnExactCouple} is met.  Alternatively, if $A^\bullet(F)$ is bounded below in degree, then by the above analysis the $E_1$-page has a horizontal line below which it vanishes. Accordingly the same is then true for all higher pages, by each of them being the cohomology of the previous page. Since the differentials go right and down, eventually they pass beneath this vanishing line and become 0. This is again the condition needed in the proof of prop. \ref{CohomologicalSpectralSequenceOfAnExactCouple} to obtain convergence. 

By that proposition the convergence is to the [[inverse limit]]

$$
  \underset{\longleftarrow}{\lim}
  \left(
    \cdots \stackrel{}{\to} A^\bullet(X_{s+1}) \longrightarrow A^\bullet(X_{s})
    \to \cdots
  \right)
  \,.
$$

If $X$ is finite dimensional or more generally if the sequences that this limit is over satisfy the [[Mittag-Leffler condition]] (def. \ref{MittagLefflerCondition}), then this limit is $A^\bullet(X)$, by prop. \ref{Lim1VanihesUnderMittagLeffler}.

 
=--

##### Multiplicative structure

+-- {: .num_prop #AHSSForMultiplicativeCohomologyIsMultiplicative}
###### Proposition

For $E^\bullet$ a [[multiplicative cohomology theory]] ([[Brown representability theorem|Brown represented]] by a [[ring spectrum]]), then the Atiyah-Hirzebruch spectral sequences (prop. \ref{AHSSExistence}) for $E^\bullet(X)$ are [[multiplicative spectral sequences]].

=--

A decent proof is spelled out in ([Kochman 96, prop. 4.2.9](#Kochman96)). Use the [graded commutativity of smash products of spheres](smash+product+of+spectra#GradedCommutativity) to get the sign in the graded derivation law for the differentials. See also the proof via [[Cartan-Eilenberg systems]] at _[multiplicative spectral sequence -- Examples -- AHSS for multiplicative cohomology](multiplicative+spectral+sequence#AHSSForMultiplicativeCohomology)_.


+-- {: .num_prop #AHSSPairing}
###### Proposition

For $E$ a [[ring spectrum]] and $X$ a finite [[CW-complex]], then the [[Kronecker pairing]]

$$
  \langle-,-\rangle_X 
    \;\colon\; 
   E^{\bullet_1}(X) \otimes E_{\bullet_2}(X) \longrightarrow \pi_{\bullet_2-\bullet_1}(E)
$$ 

extends to a compatible pairing of [[Atiyah-Hirzebruch spectral sequences]].

=--

([Kochman 96, prop. 4.2.10](#Kochman96))



### **S.2)** Cobordism theory
 {#S2CobordismTheory}

**Idea.** As one passes from [[abelian groups]] to [[spectra]], a miracle happens: even though the latter are just the proper embodiment of [[linear algebra]] in the context of [[homotopy theory]] ("[[higher algebra]]") their inspection reveals that spectra natively know about deep phenomena of [[differential topology]], [[index theory]] and in fact [[string theory]] (for instance via a close relation between _[[genera and partition functions - table|genera and partition functions]]_). 

A strong manifestation of this phenomenon comes about in [[complex oriented cohomology theory]]/[[chromatic homotopy theory]] that we eventually come to [below](#ComplexOrientedCohomologyTheory). It turns out to be higher algebra over the complex Thom spectrum [[MU]]. 

Here we first concentrate on its real avatar, the [[Thom spectrum]] [[MO]]. The seminal result of [[Thom's theorem]] says that the [[stable homotopy groups]] of [[MO]] form the [[cobordism ring]] of [[cobordism]]-[[equivalence classes]] of [[manifolds]]. In the course of discussing this _[[cobordism theory]]_ one encounters various phenomena whose complex version also governs the complex oriented cohomology theory that we are interested in [below](#ComplexOrientedCohomologyTheory).

**Literature.** ([Kochman 96, chapter I and sections II.2, II6](Kochman96)). A quick efficient account is in ([Malkiewich 11](#Malkiewich11)). See also ([Aguilar-Gitler-Prieto 02, section 11](#AguilarGitlerPrieto02)).


#### Classifying spaces, $G$-Structure and Bordism
 {#ClassifyingSpaces}

**Idea.** Every [[manifold]] $X$ of [[dimension]] $n$ carries a canonical [[vector bundle]] of [[rank]] $n$: its [[tangent bundle]]. There is a [[universal vector bundle]] of rank $n$, of which all others arise by [[pullback]], up to [[isomorphism]]. The base space of this universal bundle is hence called the [[classifying space]] and denoted $B GL(n) \simeq B O(n)$ (for $O(n)$ the [[orthogonal group]]). This may be realized as the [[homotopy type]] of a [[direct limit]] of [[Grassmannian manifolds]]. In particular the tangent bundle of a manifold $X$ is classified by a map $X \longrightarrow B O(n)$, unique up to homotopy. For $G$ a [[subgroup]] of $O(n)$, then a lift of this map through the canonical map $B G \longrightarrow B O(n)$ of classifying spaces is a _[[G-structure]]_ on $X$

$$
  \array{
    && B G
    \\
    &\nearrow& \downarrow
    \\
    X &\longrightarrow& B O(n)
  }
$$ 

for instance an [[orientation]] for the inclusion $SO(n) \hookrightarrow O(n)$ of the [[special orthogonal group]], or an [[almost complex structure]] for the inclusion $U(n) \hookrightarrow O(2n)$ of the [[unitary group]].

All this generalizes, for instance from tangent bundles to [[normal bundles]] with respect to any [[embedding]]. It also behaves well with respect to passing to the [[boundary]] of manifolds, hence to [[bordism]]-classes of manifolds. This is what appears in [[Thom's theorem]] [below](#ThomTheorem).

**Literature.** ([Kochman 96, 1.3-1.4](#Kochman96))


#### Thom spectra
 {#ThomSpectra}
 
**Idea**. Given a [[vector bundle]] $V$ of rank $n$ over a [[compact topological space]], then its [[one-point compactification]] is equivalently the result of forming the bundle $D(V) \hookrightarrow V$ of unit [[n-balls]], and identifying with one single point all the boundary unit [[n-spheres]] $S(V)\hookrightarrow V$. Generally, this construction $Th(C) \coloneqq D(V)/S(V)$ is called the _[[Thom space]]_ of $V$. 

Thom spaces occur notably as codomains for would-be [[left inverses]] of [[embeddings]] of [[manifolds]] $X \hookrightarrow Y$. The _[[Pontrjagin-Thom collapse map]]_ $Y \to Th(N X)$ of such an embedding is a continuous function going the other way around, but landing not quite in $X$ but in the [[Thom space]] of the [[normal bundle]] of $X$ in $Y$. Composing this further with the classifying map of the [[normal bundle]] lands in the Thom space of the [[universal vector bundle]] over the [[classifying space]] $B O(k)$, denoted $M O(k)$. In particular in the case that $Y = S^n$ is an [[n-sphere]] (and every manifold embeds into a large enough $n$-sphere, see also at [[Whitney embedding theorem]]), the [[Pontryagin-Thom collapse map]] hence associates with every manifold an element of a [[homotopy group]] of a universal Thom space $M O(k)$.

This curious construction turns out to have excellent formal properties: as the dimension ranges, the universal Thom spaces arrange into a [[spectrum]], called the _[[Thom spectrum]]_, and the homotopy groups defined by the Pontryagin-Thom collapse pass along to the [[stable homotopy groups]] of this spectrum. 

Moreover, via [[Whitney sum]] of [[vector bundle]] the [[Thom spectrum]] naturally is a [[ring spectrum]], and under the Pontryagin-Thom collapse the [[Cartesian product]] of manifolds is compatible with this ring structure.

**Literature.** ([Kochman 96, 1.5](#Kochman96), [Schwede 12, chapter I exaple 1.16](#Schwede12))


#### Thom's theorem
 {#ThomTheorem}

**Idea.** By the [[Pontryagin-Thom collapse]] construction [above](#ThomSpectra), there is an assignment

$$
  n Manifolds \longrightarrow \pi_n(M O)
$$

which sends [[disjoint union]] and [[Cartesian product]] of manifolds to sum and product in the [[ring]] of [[stable homotopy groups]] of the [[Thom spectrum]]. One finds then that two manifolds map to the same element in $\pi_\bullet(M O)$ precisely if they are connected by a [[bordism]] as [above](#ClassifyingSpaces). The [[bordism]]-classes $\Omega_\bullet^O$ of manifolds  form a [[commutative ring]] under [[disjoint union]] and [[Cartesian product]], called the _[[bordism ring]]_, and hence Pontrjagin-Thom collapse produces a ring [[homomorphism]]

$$
  \Omega_\bullet^O \longrightarrow \pi_\bullet(M O)
  \,.
$$

[[Thom's theorem]] states that this homomorphism is an [[isomorphism]].

**Literature.** ([Kochman 96, 1.5](#Kochman96))


#### Thom isomorphism
 {#ThomIsomorphism}


**Idea.** If a [[vector bundle]] $E \stackrel{p}{\longrightarrow} X$ of [[rank]] $n$ carries a cohomology class $\omega \in H^n(Th(E),R)$  that looks fiberwise like a [[volume form]] -- a [[Thom class]] -- then the operation of pulling back from base space and then forming the [[cup product]] with this [[Thom class]] is an [[isomorphism]] on (reduced) cohomology

$$
  ( (-) \cup \omega) \circ p^\ast 
  \;\colon\;
  H^\bullet(X,R) \stackrel{\simeq}{\longrightarrow} \tilde H^{\bullet+n}(Th(E),R)
  \,.
$$

This is the _[[Thom isomorphism]]_. It follow from the [[Serre spectral sequence]] (or else from the [[Leray-Hirsch theorem]]).

We need this below to compute (co)homology of universal Thom spectra $M U$ in terms of that of the [[classifying spaces]] $B U$.

Composed with pullback along the [[Pontryagin-Thom collapse map]], the Thom isomorphism produces maps in cohomology that covariantly follow the underlying maps of spaces. These "[[Umkehr maps]]" have the interpretation of [[fiber integration]] against the Thom class.


**Literature.** ([Kochman 96, 2.6](#Kochman96))



#### Orientation in generalized cohomology
 {#OrientationAndFiberIntegration}


**Idea.** From the way the [[Thom isomorphism]] via a [[Thom class]] works in [[ordinary cohomology]] (as [above](#ThomIsomorphism)), one sees what the general concept of [[orientation in generalized cohomology]] and of [[fiber integration in generalized cohomology]] is to be.

An important application is given by taking $E = $ [[KU]] to be [[topological K-theory]]. Then [[orientation in generalized cohomology|orientation]] is [[spin structure]] and fiber integration with coefficients in $E$ is [[fiber integration in K-theory]]. This is classical _[[index theory]]_.

**Literature.** ([Kochman 96, section 4.3](#Kochman96), [Adams 74, part III, section 10](#Adams74), [Lurie 10, lecture 5](#Lurie10))


$\,$

### **S.3)** Complex oriented cohomology
 {#ComplexOrientedCohomologyTheory}



**Idea.** Given the concept of [[orientation in generalized cohomology]] as [above](#OrientationAndFiberIntegration), it is clearly of interest to consider [[cohomology theories]] $E$ such that there exists an [[orientation in generalized cohomology|orientation]]/[[Thom class]] on the [[universal vector bundle]] over any [[classifying space]] $B G$ (or rather: on its induced [[spherical fibration]]), because then _all_ $G$-[[associated bundle|associated]] [[vector bundles]] inherit an orientation.

Considering this for $G = U(n)$ the [[unitary groups]] yields the concept of _[[complex oriented cohomology theory]]_. 

It turns out that a complex orientation on a generalized cohomology theory $E$ in this sense is already given by demanding that there is a suitable generalization of the [[first Chern class]] of [[complex line bundles]] in $E$-cohomology. By the [[splitting principle]], this already implies the existence of [[generalized Chern classes]] ([[Conner-Floyd Chern classes]]) of all degrees, and these are the required universal generalized [[Thom classes]].

Where the ordinary [[first Chern class]] in [[ordinary cohomology]] is simply additive under [[tensor product]] of [[complex line bundles]], one finds that the composite of generalized first Chern classes is instead governed by more general commutative [[formal group laws]]. This phenomenon governs much of the theory to follow.

**Literature.** ([Kochman 96, section 4.3](#Kochman96), [Lurie 10, lectures 1-10](#Lurie10), [Adams 74, Part I, Part II](#Adams74)).


#### Chern classes
 {#ChernClasses}

**Idea**. In particular [[ordinary cohomology]] [[HR]] is canonically a [[complex oriented cohomology theory]]. The behaviour of general [[Conner-Floyd Chern classes]] to be discussed [below](#ConnerFloydChernClasses) follows closely the behaviour of the ordinary [[Chern classes]]. 

An ordinary [[Chern class]] is a [[characteristic class]] of [[complex vector bundles]], and since there is the [[classifying space]] $B U$ of complex vector bundles, the _universal_ Chern classes are those of the [[universal complex vector bundle]] over the [[classifying space]] $B U$, which in turn are just the [[ordinary cohomology]] classes in $H^\bullet(B U)$

These may be computed inductively by iteratively applying to the [[spherical fibrations]]

$$
  S^{2n-1} \longrightarrow B U(n-1) \longrightarrow B U(n)
$$

the [[Thom-Gysin exact sequence]], a special case of the [[Serre spectral sequence]]. 

Pullback of Chern classes along the canonical map $(B U(1))^n \longrightarrow B U(n)$ identifies them with the [[symmetric polynomials]] in the [[first Chern class]] in $H^2(B U(1))$. This is the _[[splitting principle]]_.

**Literature.** ([Kochman 96, section 2.2 and 2.3](#Kochman96), [Switzer 75, section 15.3](#Switzer75) [Lurie 10, lecture 5, prop. 6](#Lurie10))

$\,$

Let $R$ be a [[commutative ring]] and let

$$
  \array{
    S^n &\longrightarrow& E
    \\
    && \downarrow^{\mathrlap{\pi}}
    \\
    && B
  }
$$

be a [[fiber bundle]] of [[n-spheres]] over a [[simply connected topological space|simply connected]] [[simplicial complex]]. 

+-- {: .num_prop }
###### Proposition

There exists a [[Thom class]]  $c \in H^{n+1}(E; R)$ (in the [[ordinary cohomology]] of the total space with [[coefficients]] in $R$) such that the [[cup product]] operation $c \cup (-)$ sits in a [[long exact sequence]] of [[cohomology groups]] of the form

$$
  \cdots 
   \to 
   H^k(B; R) 
     \stackrel{\pi^\ast}{\longrightarrow}
   H^k(E; R)
    \stackrel{}{\longrightarrow}
   H^{k-n}(B;R)
   \stackrel{c \cup (-)}{\longrightarrow}
   H^{k+1}(B; R)
   \to
   \cdots
  \,.
$$

=--

(e.g. [Switzer 75, section 15.30](#Switzer75), [Kochman 96, corollary 2.2.6](#Kochman96))

+-- {: .proof}
###### Proof

There is the corresponding [[Serre spectral sequence]] 

$$
  E_2^{s,t}
  =
  H^s(B; H^t(S^n;R))
  \;\Rightarrow\;
  H^{s+t}(E; R)
  \,.
$$

Since the [[ordinary cohomology]] of the [[n-sphere]] [[fiber]] is concentrated in just two degees

$$
  H^t(S^n; R)
  =
  \left\{
    \array{
      R & for \; t= 0 \; and \; t = n
      \\
      0 & otherwise
    }
  \right.
$$

most terms on the $E_2$ page of this spectral sequence, and hence on all the further pages, vanish. As a consequence, the only possible non-vanishing differentials $d_r$ are those on the $(n+1)$-page, of the form

$$
  \array{
     E_{n+1}^{s,n} & \simeq & H^s(B;R)
     \\
     {}^{\mathllap{d_{n+1}}}\downarrow
     \\
     E_{n+1}^{s+n+1,0} & \simeq &  H^{s+n+1}(B;R)
  }
  \,.
$$

Now since the [[coefficients]] $R$ is a [[ring]], then by prop. \ref{AHSSForMultiplicativeCohomologyIsMultiplicative} the [[Serre spectral sequence]] is [[multiplicative spectral sequence|multiplicative]] under [[cup product]] and the [[differential]] is a [[derivation]] (of total degree 1) with respect to this product.

To make use of this, write

$$
  \iota = 1 \in H^0(B;R) \stackrel{\simeq}{\longrightarrow} E_{n+1}^{0,n} 
$$

for the unit in the cup product ring $H^\bullet(X;R)$, regarded as an element in the $(n+1)$-page of the spectral sequence. Notice that as such $\iota$ is not in degree 0, but in bidegree $(0,n)$, in particular $\iota$ is _not_ in $E_{n+1}^{0,0}$ and in particular is not the unit in there, and hence $d_{n+1}(\iota)$ need not vanish. Write

$$
  c \coloneqq d_{n+1}(\iota) \in E_{n+1}^{n+1,0} \stackrel{\simeq}{\longrightarrow} H^{n+1}(B; R)
$$

for this element. This is the Thom class in question.

Because, notice that every element in $E_{n+1}^{\bullet,n}$ is of the form $\iota \cdot b$ for $b\in E_{n+1}^{\bullet,0} \simeq H^\bullet(B;R)$, and since $d_{n+1}$ is a [[derivation]] and vanishes on $E_{n+1}^{\bullet,0}$, it follows that its action is fixed by 

$$
  \begin{aligned}
    d_{n+1}(\iota \cdot b)
    & =
    d_{n+1}(\iota) \cdot b + (-1)^{n} \iota \cdot \underset{= 0}{\underbrace{d_{n+1}(b)}}
    \\
    & = c \cdot b
  \end{aligned}
  \,.
$$

This shows that 

$$
  \array{
     E_{n+1}^{s,n} & \simeq & H^s(B;R)
     \\
     {}^{\mathllap{d_{n+1}}}\downarrow && \downarrow^{\mathrlap{c \cup (-)}}
     \\
     E_{n+1}^{s+n+1, 0} & \simeq & H^{s+n+1}(B;R)
  }
  \,.
$$

Hence the non-vanishing entries of the $E_\infty$-page of the spectral sequence sit in [[exact sequences]] like so

$$
  \array{
     0
     \\
     \downarrow
     \\
     E_\infty^{s,n}
     \\
     {}^{\mathllap{ker(d_{n+1})}}\downarrow
     \\
     E_{n+1}^{s,n} & \simeq & H^s(B;R)
     \\
     {}^{\mathllap{d_{n+1}}}\downarrow && \downarrow^{\mathrlap{c \cup (-)}}
     \\
     E_{n+1}^{s+n+1, 0} & \simeq & H^{s+n+1}(B;R)
     \\
     {}^{\mathllap{coker}(d_{n+1})}\downarrow
     \\
     E_\infty^{s+n+1,0}
     \\
     \downarrow
     \\
     0
  }  
  \,.
$$

Finally observe (lemma \ref{lemma}) that due to the sparseness of the $E_\infty$-page, there are also [[short exact sequences]] of the form

$$
  0 \to E_\infty^{s,0} \longrightarrow H^s(E; R) \longrightarrow  E_\infty^{s-n,n} \to 0
  \,.
$$

Concatenating these with the above exact sequences yields the desired [[long exact sequence]].

=--

+-- {: .num_lemma #lemma}
###### Lemma

For a cohomology [[spectral sequence]] converging to some $C^\bullet$ with the property that $E_\infty^{s,t} = 0$ unless $t = 0$ or $t = n$, then there are [[short exact sequences]] of the form

$$
  0 \to E_\infty^{s,0} \longrightarrow C^s \longrightarrow  E_\infty^{s-n,n} \to 0
  \,.
$$

=--

(e.g. [Switzer 75, p. 356](#Switzer75))

+-- {: .proof}
###### Proof

By definition of convergence the $E_{\infty}^{s,t}$ sit in [[short exact sequences]] of the form

$$
  0 \to F^{s+1}C^{s+t} \longrightarrow F^s C^{s+t} \longrightarrow E_\infty^{s,t} \to 0
  \,.
$$

So when $E_\infty^{s,t} = 0$ the left morphism here is an [[isomorphism]].

We may use this to either shift away the filtering degree

* if $t \geq n$ then $F^s C^{s+t} = F^{s}C^{s-1+t+1} \simeq F^0 C^{s-1+t+1} = F^0 C^{s+t} \simeq C^{s+t}$.

or to shift away the offset of the filtering to the total degree:

* if $0 \leq t-1 \leq n-1$ then $F^{s+1}C^{s+t} = F^{s+1}C^{s+1+t-1} = F^{s+t}C^{s+1+t-1} = F^{s+t}C^{s+t}$

* if $t \lt 0$ then $F^{s}C^{s+t} = 0$.

In particular $F^{s}C^{s} \simeq E_\infty^{s,0}$.

Hence the defining exact sequence

$$
  0 \to F^{s+1}C^{s+n} \longrightarrow F^{s}C^{s+n} \longrightarrow E_\infty^{s,n} \to 0
$$

becomes

$$
  0 \to E_\infty^{s+n,0} \longrightarrow C^{s+n} \longrightarrow E_\infty^{s,n}
 \to 0
  \,.
$$

=--



#### Conner-Floyd Chern classes
 {#ConnerFloydChernClasses}

**Idea.** For $E$ a [[complex oriented cohomology theory]], then the generators of the $E$-[[cohomology groups]] of the [[classifying space]] $B U$ are called the _[[Conner-Floyd Chern classes]]_, in $E^\bullet(B U)$. 

Using basic properties of the classifying space $B U(1)$ via its incarnation as the infinite [[complex projective space]] $\mathbb{C}P^\infty$, one finds that the [[Atiyah-Hirzebruch spectral sequences]]

$$
  H^p(\mathbb{C}P^n, \pi_q(E)) \Rightarrow H^\bullet(\mathbb{C}P^n)
$$

collapse right away, and that the [[inverse system]] which they form satisfies the [[Mittag-Leffler condition]]. Accordinly the [[Milnor exact sequence]] gives that the ordinary [[first Chern class]] $c_1$ generates,  over $\pi_\bullet(E)$, all Conner-Floyd classes over $B U(1)$:

$$
  E^\bullet(B U(1)) \simeq \pi_\bullet(E) [ [ c_1 ] ]
  \,.
$$

This is the key input for the discussion of [[formal group laws]] [below](#FormalGroupLaws).

Combining the [[Atiyah-Hirzebruch spectral sequence]] with the [[splitting principle]] as for ordinary Chern classes [above](#ChernClasses) yields, similarly, that in general Conner-Floyd classes are generated, over $\pi_\bullet(E)$, from the ordinary Chern classes.

Finally one checks that Conner-Floyd classes canonically serve as [[Thom classes]] for $E$-cohomology of the [[universal complex vector bundle]], therby showing that [[complex oriented cohomology theories]] are indeed canonically [[orientation in generalized cohomology|oriented]] on ([[spherical fibrations]] of) [[complex vector bundles]]. 
 
**Literature.** ([Kochman 96, section 4.3](#Kochman96) [Adams 74, part I.4, part II.2 II.4, part III.10](#Adams74), [Lurie 10, lecture 5](#Lurie10))


#### Formal group laws of first CF-Chern classes
 {#FormalGroupLaws}

**Idea.** The [[classifying space]] $B U(1)$ for [[complex line bundles]] is a [[homotopy type]] canonically equipped with commutative group structure ([[infinity-group]]-structure), corresponding to the [[tensor product]] of complex line bundles. By the above, the [[first Chern class]] of these complex line bundles generates the $E$-cohomology of $B U(1)$, it follows that the [[cohomology ring]] $E^\bullet(B U(1)) \simeq \pi_\bullet(E)[ [ c_1 ] ]$ behaves like the ring of $\pi_\bullet(E)$-valued functions on a 1-dimensional commutative [[formal group]] equipped with a canonical [[coordinate]] function $c_1$. This is called a _[[formal group law]]_ over the [[graded ring]] $\pi_\bullet(E)$. 

On abstract grounds it follows that there exists a commutative ring $L$ and a universal (1-dimensional commutative) formal group law $\ell$ over $L$. This is called the _[[Lazard ring]]_. [[Lazard's theorem]] identifies this ring concretely: it turns out to simply be the [[polynomial ring]] on generators in every even degree.

Further below this has profound implications on the structure theory for complex oriented cohomology. The [[Milnor-Quillen theorem on MU]] identifies the Lazard ring as the cohomology ring of the [[Thom spectrum]] [[MU]], and then the [[Landweber exact functor theorem]], implies that there are lots of complex oriented cohomology theories.

**Literature.** ([Kochman 96, section 4.4](#Kochman96), [Lurie 10, lectures 1 and 2](#Lurie10))


#### Complex cobordism
 {#ComplexCobordismCohomology}

**Idea.** There is a [[weak homotopy equivalence]] $\phi \colon B U(1)\stackrel{\simeq}{\longrightarrow} M U(1)$ between the [[classifying space]] for [[complex line bundles]] and the  [[Thom space]] of the [[universal vector bundle|universal complex line bundle]]. This gives an element $\pi_\ast(c_1) \in M U^2(B U(1))$ in the [[complex cobordism cohomology]] of $B U(1)$ which makes the universal complex [[Thom spectrum]] [[MU]] become a [[complex oriented cohomology theory]].

This turns out to be a [[universal complex orientation on MU]]: for every other [[ring spectrum]] $E$ there is an equivalence between complex orientations on $E$ and ring spectrum homomorphisms

$$
  \{M U \longrightarrow E\} \;\simeq\; \{complex\;orientations\;on\;E\}
  \,.
$$

Hence [[complex oriented cohomology theory]] is just [[higher algebra]] over [[MU]]. Equivalently: affine [[spectral geometry]] over $Spec(MU)$.

**Literature.** ([Schwede 12, example 1.18](#Schwede12), [Kochman 96, section 1.4, 1.5, 4.4](#Kochman96), [Lurie 10, lectures 5 and 6](#Lurie10))


#### Homology of $M U$
 {#HomologyOfMU}

**Idea.** Since, by the above, every [[complex oriented cohomology theory]] $E$ is indeed [[orientation in generalized cohomology|oriented]] over [[complex vector bundles]], there is a [[Thom isomorphism]] which reduces the computation of the $E$-[[homology of MU]], $E_\bullet(M U)$ to that of the [[classifying space]] $B U$. The homology of $B U$, in turn, may be determined by the duality with its cohomology ([[universal coefficient theorem]]) via [[Kronecker pairing]] and the induced duality of the corresponding [[Atiyah-Hirzebruch spectral sequences]] (prop. \ref{AHSSPairing}) from the Conner-Floyed classes [above](#ConnerFloydChernClasses). Finally, via the [[Hurewicz homomorphism]]/[[Boardman homomorphism]] the homology of $M U$ gives a first approximation to the [[homotopy groups]] of [[MU]].

**Literature.** ([Kochman 96, section 2.4, 4.3](#Kochman96), [Lurie 10, lecture 7](#Lurie10))


#### Milnor-Quillen theorem on $M U$
 {#QuillenTheoremOnMU}

**Idea.** From the computation of the [[homology of MU]] [above](#HomologyOfMU) and applying the [[Boardman homomorphism]], one deduces that the [[stable homotopy groups]] $\pi_\bullet(MU)$ of [[MU]] are finitely generated. This implies that it is suffient to compute them over the [[p-adic integers]] for all primes $p$. Using the [[change of rings theorem]], this finally is obtained from inspection of the filtration in the $H\mathbb{F}_p$-[[Adams spectral sequence]] for $MU$. This is Milnor's theorem wich together with [[Lazard's theorem]] shows that there is an isomorphism of rings $L \simeq \pi_\bullet(M U)$ with the [[Lazard ring]]. Finally [[Quillen's theorem on MU]] says that this isomorphism is exhibited by the universal ring homomorphism $L \longrightarrow \pi_\bullet(M U)$ which classifies the universal complex orientation on $M U$.

**Literature.** ([Kochman 96, section 4.4](#Kochman96), [Lurie, lecture 10](#Lurie10))


#### Landweber exact functor theorem

**Idea.** By the above, every [[complex oriented cohomology theory]] induces a [[formal group law]] from its first [[Conner-Floyd Chern class]]. Moreover, [[Quillen's theorem on MU]] together with [[Lazard's theorem]] say that the [[cohomology ring]] $\pi_\bullet(M U)$ of [[complex cobordism cohomology]] [[MU]] is the classifying ring for formal group laws. 

The _[[Landweber exact functor theorem]]_ says that, conversely, forming the [[tensor product]] of [[complex cobordism cohomology theory]] ([[MU]]) with a [[Landweber exactness|Landweber exact]] [[ring]] via some [[formal group law]] yields a [[cohomology theory]], hence a [[complex oriented cohomology theory]]. 

**Literature.** ([Lurie 10, lectures 15,16](#Lurie10))

### Outlook: Geometry of $Spec(MU)$

The grand conclusion of [[Quillen's theorem on MU]] ([above](#QuillenTheoremOnMU)): [[complex oriented cohomology theory]] is essentially the [[spectral geometry]] over $Spec(M U)$, and the latter is a kind of derived version of the [[moduli stack of formal groups]] (1-dimensional commutative).


* [[Landweber-Novikov theorem]]

* [[Adams-Quillen theorem]]

* [[Adams-Novikov spectral sequence]]

(...)

**Literature.** ([Kochman 96, sections 4.5-4.7 and section 5](#Kochman96), [Lurie 10, lectures 12-14](#Lurie10))



$\,$

***

$\,$

## References
 {#References}

### Basic reading

For **Prelude) Classical homotopy theory** 

A concise and yet comprehensive and self-contained re-write of the proof ([Quillen 67](#Quillen67)) of the [[classical model structure on topological spaces]] is in

* {#Hirschhorn15} [[Philip Hirschhorn]], _The Quillen model category of topological spaces_ ([arXiv:1508.01942](http://arxiv.org/abs/1508.01942)).

For relevant background on [[algebraic topology]] see also ([Aguilar-Gitler-Prieto 02, chapters 1-6](#AguilarGitlerPrieto02)) below. 

For general [[model category]] theory a decent concise account is in

* {#DwyerSpalinski95} [[William Dwyer]], J. Spalinski, _[[Homotopy theories and model categories]]_ ([pdf](http://folk.uio.no/paularne/SUPh05/DS.pdf)) in [[Ioan Mackenzie James]] (ed.), _[[Handbook of Algebraic Topology]]_ 1995

For the [[classical model structure on simplicial sets]] and its [[Quillen equivalence]] to that on topological spaces, good sources are

* {#GoerssJardine99} [[Paul Goerss]], [[Rick Jardine]], chapter I of_[[Simplicial homotopy theory]]_, Birkh&#228;user, Progress in Mathematics (1999), reprinted as Modern Classics (2009)

* {#JoyalTierney05} [[André Joyal]], [[Myles Tierney]], _An introduction to simplicial homotopy theory_, 2005  ([chapter I](http://hopf.math.purdue.edu/cgi-bin/generate?/Joyal-Tierney/JT-chap-01), more notes [pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern47.pdf))

For the restriction to the [[convenient category of topological spaces|convenient category]] of [[compactly generated topological spaces]] a good source is still

* {#Lewis78} [[Gaunce Lewis]], _Compactly generated spaces_ ([pdf](http://www.math.uchicago.edu/~may/MISC/GaunceApp.pdf)), appendix A of _The Stable Category and Generalized Thom Spectra_ PhD thesis Chicago, 1978


For section **1) Stable homotopy theory** we follow the modern picture of the stable homotopy category in the style of the exposition

* {#Malkiewich14} [[Cary Malkiewich]], _The stable homotopy category_, 2014 ([pdf](http://math.uiuc.edu/~cmalkiew/stable.pdf)).

but we also take some clues from the [[Bousfield-Friedlander model structure]]. The classical account in ([Adams 74, part III sections 2, 4-7](#Adams74)) is still a good read (but ignore the "[[Adams category]]"-construction of the [[stable homotopy category]] in sections III.2 and III.3).

For the discussion of [[ring spectra]] we pass to [[symmetric spectra]]. A comprehensive and account is in

* {#Schwede12} [[Stefan Schwede]], _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

In order to construct and understand the [[model structure on symmetric spectra]] via the [[model structure on orthogonal spectra]] we develop the approach of 

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], _[[Model categories of diagram spectra]]_, Proceedings of the London Mathematical Society, 82 (2001), 441-512 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf))

For **Interlude: Spectral sequences** a discussion streamlined for our purposes is in ([Rognes 12, section 2](#Rognes12)).

In **2) Adams spectral sequence** for the general theory we follow ([Hopkins 99, section 5](#Hopkins99)) as worked out in

* {#Aramian} [[Nersés Aramian]], _The Adams spectral sequence_ ([[AramianANSS.pdf:file]])

and we take some further clues from ([Adams 74, III.15](#Adams74)).

For the special case of the classical Adams spectral sequence a comprehensive survey is in 

* {#Bruner09} [[Robert Bruner]], _An Adams spectral sequence primer_, 2009 ([pdf](http://www.math.wayne.edu/~rrb/papers/adams.pdf))

For the **Seminar on Complex oriented cohomology** an excellent textbook to hold on to is

* {#Kochman96} [[Stanley Kochman]], chapters I - IV of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

While this gives detailed proofs, some standard steps used are made more explicit for instance in 

* {#Switzer75} [[Robert Switzer]], _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 


Specifically for **S.1) Generalized cohomology** a neat account is in:

* {#AguilarGitlerPrieto02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 12 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))


For **S.2) Cobordism theory** an efficient collection of the highlights is in

* {#Malkiewich11} [[Cary Malkiewich]], _Unoriented cobordism and $M O$_, 2011 ([pdf](http://math.uiuc.edu/~cmalkiew/cobordism.pdf))

except that it omits proof of the [[Leray-Hirsch theorem]]/[[Serre spectral sequence]] and that of the [[Thom isomorphism]], but see the references there and see ([Kochman 96](#Kochman96), [Aguilar-Gitler-Prieto 02, section 11.7](#AguilarGitlerPrieto02)) for details.
 
For **S.3) Complex oriented cohomology** besides ([Kochman 96, chapter 4](#Kochman96)) have a look at part II of 

* {#Adams74} [[Frank Adams]], _[[Stable homotopy and generalized homology]]_, Chicago Lectures in mathematics, 1974

and

* {#Lurie10} [[Jacob Lurie]], lectures 1-10 of _[[Chromatic Homotopy Theory]]_, 2010

(These overlap, pick the one that seems more inviting on first reading.)

### Further reading

The two originals

* {#Quillen67} [[Daniel Quillen]], _Axiomatic homotopy theory_ in  _Homotopical algebra_, Lecture Notes in Mathematics, No. 43 43, Berlin (1967)

* {#Brown73} [[Kenneth Brown]], _[[Abstract Homotopy Theory and Generalized Sheaf Cohomology]]_, Transactions of the American Mathematical Society, Vol. 186 (1973), 419-458  ([JSTOR](http://www.jstor.org/stable/1996573))

are still an excellent source. For further reading on homotopy theory and stable homotopy theory a useful collection is

* {#James95} [[Ioan Mackenzie James]], _[[Handbook of Algebraic Topology]]_ 1995

The modern chromatic picture originates around

* {#Hopkins99} [[Mike Hopkins]], _[[Complex oriented cohomology theories and the language of stacks]]_, 1999 

a useful survey is in

* {#Wilson13} [[Dylan Wilson]] section 1.2 of _Spectral Sequences from Sequences of Spectra: Towards the Spectrum of the Category of Spectra_ lecture at _[2013 Pre-Talbot Seminar](http://math.harvard.edu/~hirolee/pretalbot2013/)_, March 2013 ([[DylanWilsonOnANSS.pdf:file]])

a wealth of details is in

* {#Ravenel86} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, 1987/2003 ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenelA1.pdf))

and new foundations have been laid in

* {#LurieHigherAlgebra} [[Jacob Lurie]], _[[Higher Algebra]]_

Further useful lecture notes pointed to above include the following:

* {#Hatcher04} [[Alan Hatcher]], _[Spectral sequences in algebraic topology](http://www.math.cornell.edu/~hatcher/SSAT/SSATpage.html)_ _II: The Adams spectral sequence_, 2004 ([pdf](http://www.math.cornell.edu/~hatcher/SSAT/SSch2.pdf))

* {#Rognes12} [[John Rognes]], _The Adams spectral sequence_ (following [Bruner](#Bruner)), 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

