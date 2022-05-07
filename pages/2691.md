
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

A [[model category]] structure on a category of [[differential graded algebras]] or more specifically on a [[category of differential graded-commutative algebras]] tends to present an [[(∞,1)-category]] of [[∞-algebra over an (∞,1)-algebraic theory|∞-algebras]]. 

For dg-algebras bounded in negative or positive degrees, the [[monoidal Dold-Kan correspondence]] asserts that their model category structures are [[Quillen equivalence|Quillen equivalent]] to the corresponding [[model structure on simplicial algebras|model structure on (co)simplicial algebras]]. This case plays a central role in [[rational homotopy theory]].

The case of model structures on unbounded dg-algebras may be thought of as induced from this by passage to the [[derived geometry]] modeled on formal duals of the bounded dg-algebras. This is described at [[dg-geometry]].


## General

The category of [[dg-algebra]]s is that of [[monoid]]s in a [[category of chain complexes]]. Accordingly general results on a [[model structure on monoids in a monoidal model category]] apply.  

Below we spell out special cases, such as restricting to [[commutative monoids]] when working over a [[ground field]] of [[characteristic zero]], or restricting to non-negatively graded cochain dg-algebras.




## On connective dgc-algebras

We discuss the projective model structure on 
[[differential graded-commutative algebras|differential non-negatively graded-commutative algebras]]. This was originally introduced in [Bousfield-Gugenheim 76](#BousfieldGugenheim76) as a [[model category]] for [[Dennis Sullivan]]'s approach to [[rational homotopy theory]].

### Definition 

+-- {: .num_defn #dgcCochainAlgebrasInNonNegativeDegrees}
###### Definition


For $k$ a [[field]] of [[characteristic zero]], write 

\[
  \label{CategoryOfdgcAlgebras}
  dgcAlg^{\geq 0}_{k}
  \;\in\;
  Categories
\]

for the [[category]] of [[associative unital algebra|unital]] [[differential graded-commutative algebras]] over $k$ in non-negative degrees, equivalently the category of [[commutative monoids]] in the [[symmetric monoidal category]] $Ch^{\geq 0}(k)$ of [[cochain complexes]] in non-negative degrees, equipped with the [[tensor product of chain complexes]].

=--

([Gelfand-Manin 96, V.3.1](#GelfandManin96))

+-- {: .num_example}
###### Example
**([[initial object|initial]] and [[terminal object]])**

In $dgcAlg^{\geq 0}_{k}$ (eq:CategoryOfdgcAlgebras):

1. the [[initial object]] is the ground field algebra $k$;

1. the [[terminal object]] is the zero algebra $0$ (which is indeed a unital algebra).

=--

(Beware that this is incorrectly stated in [Gelfand-Manin 96, p. 335](#GelfandManin96))

More generally:

+-- {: .num_example}
###### Example
**([[coproducts]] and [[products]])**

In $dgcAlg^{\geq 0}_{k}$ (eq:CategoryOfdgcAlgebras):

1. the [[coproduct]] is given by the [[tensor product of algebras]];

   (see at _[pushouts of commutative monoids](category+of+monoids#PushoutOfCommutativeMonoids)_)

1. the [[product]] is given by [[direct sum]] on underlying [[graded vector spaces]]

   (since the [[forgetful functor]] is a [[right adjoint]]).

=--


+-- {: .num_defn #dgcCochainAlgebraInNonNegDegreeOfFiniteType}
###### Definition
**(finite type)**

Say that a [[dgc-algebra]] $A \in dgcAlg^{\geq 0}_k$ (def. \ref{dgcCochainAlgebrasInNonNegativeDegrees}) is of _[[finite type]]_ if its [[forgetful functor|underlying]] [[chain complex]] is in each degree of [[finite number|finite]] [[dimension]] as a $k$-[[vector space]].

=--

+-- {: .num_defn #ProjectiveModelStructureOnCdgAlg}
###### Definition
**(projective model structure on rational connective dgc-algebras)**

Write $(dgcAlg^{\geq 0}_k)_{proj}$ for the catgory of [[dgc-algebras]] from def. \ref{dgcCochainAlgebrasInNonNegativeDegrees} equipped with the following [[classes]] of morphisms:

* _[[weak equivalences]]_ are the [[quasi-isomorphism]];

* _[[fibrations]]_ are the degreewise [[surjections]];

=--


([Bousfield-Gugenheim 76, Def. 4.2](#BousfieldGugenheim76), [Gelfand-Manin 96, Def. V.3.3](#GelfandManin96))


+-- {: .num_prop #IndeedProjectiveModelStructureOnCdgAlg}
###### Proposition

The category $(dgcAlg^{\geq 0}_k)_{proj}$ from def. \ref{ProjectiveModelStructureOnCdgAlg} is a [[model category]], to be called the _projective model structure_.


=--

([Bousfield-Gugenheim 76, Theorem 4.3](#BousfieldGugenheim76), [Gelfand-Manin 96, Theorem V.3.4](#GelfandManin96))


+-- {: .num_remark }
###### Remark
**([[category of fibrant objects]])**

Evidently every [[object]] in $(dgcAlg^{\geq 0}_k)_{proj}$ (Def. \ref{ProjectiveModelStructureOnCdgAlg}, prop. \ref{IndeedProjectiveModelStructureOnCdgAlg}) is a [[fibrant object]]. Therefore these model categories structures are in particular also structures of a [[category of fibrant objects]].

=--

The nature of the cofibrations is discussed [below](#SullivanAlgebras).


### Properties

#### Cofibrations and Sullivan algebras
 {#SullivanAlgebras}

+-- {: .num_defn }
###### Definition
**(sphere and disk algebras)**

Write $k[n]$ for the graded vector space which is the ground field $k$ in degree $n$ and 0 in all other degrees. For $n \in \mathbb{N}$, consider the [[semifree dgc-algebras]]

$$
  S(n) \coloneqq (\wedge^\bullet k[n], 0)
$$ 

and for $n \geq 1$ the [[semifree dgc-algebras]]

$$
  D(n) 
   \coloneqq
   \left\lbrace
     \array{
         0 & (n = 0)
         \\
        (\wedge^\bullet (k[n] \oplus k[n-1]), 0) & (n \gt 0)
     }
   \right.
$$ 

for which the differential sends the generator of $k[n-1]$ to that of $k[n]$

Write

$$
  i_n \colon S(n) \to D(n)
$$

for the obvious morphism that takes the generator in degree $n$ to the generator in degree $n$ (and for $n = 0$ it is the unique morphism from the [[initial object]] $(0,0)$).

For $n \gt 0$ write

$$
  j_n \colon k[0] \to D(n)
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition
**(generating cofibrations)**

The sets

$$
  I = \{i_n \}_{n \geq 1} \cup \{k[0] \to S(0), S(0) \to k[0]\}
$$

and 

$$
  J = \{j_n \}_{n \gt 1} 
$$

are sets of generating cofibrations and acyclic cofibrations, respectively, exhibiting the model category $(dgcAlg^{\geq 0}_k)_{proj}$ from prop. \ref{IndeedProjectiveModelStructureOnCdgAlg} as a [[cofibrantly generated model category]].


=--

review includes ([Hess 06, p. 6](#Hess06))


In this section we describe the cofibrations in the model structure on $(dgcalg^{\geq 0}_k)_{proj}$ (def. \ref{ProjectiveModelStructureOnCdgAlg}, prop. \ref{IndeedProjectiveModelStructureOnCdgAlg}). Notice that it is these that are in the image of the dual [[monoidal Dold-Kan correspondence]].

Before we characterize the cofibrations, first some notation.

For $V$ a $\mathbb{Z}$-[[graded vector space]] write 
$\wedge^\bullet V$ for the [[Grassmann algebra]] over it. Equipped with the trivial differential $d = 0$ this is a [[semifree dga]] $(\wedge^\bullet V, d=0)$.

With $k$ our ground field we write $(k,0)$ for the corresponding dg-algebra, the tensor unit for the standard [[monoidal category|monoidal structure]] on $dgAlg$. This is the [[Grassmann algebra]] on the 0-vector space
$(k,0) = (\wedge^\bullet 0, 0)$.


+-- {: .num_defn }
###### Definition
**(Sullivan algebras)**

A **[[relative Sullivan algebra]]** is a [[morphism]] of dg-algebras that is an inclusion

$$
  (A,d) \to (A \otimes_k \wedge^\bullet V, d')
$$

for $(A,d)$ some dg-algebra and for $V$ some graded vector space, such that 

* there is a [[well ordered set]] $J$

* indexing a basis $\{v_\alpha \in V| \alpha \in J\}$ of $V$;

* such that with $V_{\lt \beta} = span(v_\alpha | \alpha \lt \beta)$ for all basis elements $v_\beta$ we have that 

  $$
    d' v_\beta \in A \otimes \wedge^\bullet V_{\lt \beta}
    \,.
  $$

This is called a **minimal** [[relative Sullivan algebra]] if in addition the condition

$$
  (\alpha \lt \beta) \Rightarrow (deg v_\alpha  \leq deg v_\beta)
$$

holds. For a Sullivan algebra $(k,0) \to (\wedge^\bullet V, d)$ relative to the tensor unit we call the [[semifree dga]] $(\wedge^\bullet V,d)$ simply a **Sullivan algebra**.  And a **minimal Sullivan algebra** if $(k,0) \to (\wedge^\bullet V, d)$ is a minimal relative Sullivan algebra.

=--

+-- {: .num_remark }
###### Remark

Sullivan algebras were introduced by [[Dennis Sullivan]] in his development of [[rational homotopy theory]]. This is one of the key application areas of the model structure on dg-algebras.

=--

+-- {: .num_remark }
###### Remark
**($L_\infty$-algebras)**

Because they are [[semifree dgas]], Sullivan dg-algebras $(\wedge^\bullet V,d)$ are (at least for degreewise finite dimensional $V$) [[Chevalley-Eilenberg algebra]]s of [[L-∞-algebra]]s.

The co-commutative differential co-algebra encoding the corresponding [[L-∞-algebra]] is the free cocommutative algebra $\vee^\bullet V^*$ on the degreewise dual of $V$ with differential $D = d^*$, i.e. the one given by the formula

$$
  \omega(D(v_1 \vee v_2 \vee \cdots v_n)) =
  - (d \omega) (v_1, v_2, \cdots,  v_n)
$$

for all $\omega \in V$ and all $v_i \in V^*$.

=--


+-- {: .num_prop }
###### Proposition
**(cofibrations are relative Sullivan algebras)**

The cofibrations in $(dgcAlg^{\geq 0}_{k})_{proj}$ are precisely the [[retracts]] of [[relative  Sullivan algebras]] $(A,d) \to (A\otimes_k \wedge^\bullet V, d')$.

Accordingly, the cofibrant objects in $(dgcAlg^{\geq 0}_{k})_{proj}$ are precisely the Sullivan algebras $(\wedge^\bullet V, d)$

=--

([Bousfield-Gugenheim 76, Prop. 7.11](#BousfieldGugenheim76)[Gelfand-Manin 96., Prop. V.5.4](#GelfandManin96))


#### Simplicial hom-complexes
 {#HomComplexes}

We discuss [[simplicial set|simplicial]] [[mapping spaces]] between [[dgc-algebras]]. These _almost_ make the projective model structure $(dgcAlg^{\geq 0}_k)_{proj}$ from prop. \ref{IndeedProjectiveModelStructureOnCdgAlg} into a [[simplicial model category]], except that the [[tensoring]]/[[powering]] [[isomorphism]] holds only for [[finite set|finite]] [[simplicial sets]] or else on [[dgc-algebras]] of [[finite type]]. Still, this has useful implications, for instance it implies that the [[reduced suspension]] and [[loop space]] [[adjunction]] on [augmented algebras|augmented]] [[dg-algebras]] is a [[Quillen adjunction]].


+-- {: .num_defn #MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees}
###### Definition
**(simplicial mapping spaces)**

For $A,B \in dgcAlg^{\geq 0}_k$ (def. \ref{dgcCochainAlgebrasInNonNegativeDegrees}), let 

$$
  Maps(A,B)
  \in 
  sSet
$$

be the [[simplicial set]] whose [[n-simplices]] are the dg-algebra [[homomorphisms]] from $A$ into the [[tensor product]] of $B$ with the de Rham complex of [[polynomial differential forms on the n-simplex]] $\Omega_{poly}^\bullet(\Delta^n)$.

$$
  Maps(A,B)_n
   \;\coloneqq\;
  Hom_{dgcAlg^{\geq 0}_k}
  \left(
    A, \; \Omega^\bullet_{poly}(\Delta^n) \otimes_k B 
  \right)
$$

and whose face and degeneracy maps are the obvious ones induced from the fact that $\Omega_{poly}^\bullet \colon \Delta^{op} \to dgcAlg^{\geq 0}_k$ is canonically a [[simplicial object]] in dgc-algebras.

We also call this the _simplicial [[mapping space]]_ from $A$ to $B$. This construction naturally extends to a [[functor]]

$$
  Maps(-,-)
  \;\colon\;
  (dgcAlg^{\geq 0}_k)^{op}
  \times
  dgcAlg^{\geq 0}_k
    \longrightarrow
   dgcAlg^{\geq 0}_k
$$

from the [[product category]] of the [[opposite category]] of [[dgc-algebras]] with the category itself.

Observe that 

$$
  Hom_{dgcAlg^{\geq 0}_k}
  \left(
    A, \; \Omega^\bullet_{poly}(\Delta^n) \otimes_k B 
  \right)
  \;\simeq\;
  {}_{\Omega^\bullet_{poly}}Hom_{dgcAlg^{\geq 0}_k}
  \left(
     \Omega^\bullet_{poly}(\Delta^n) \otimes_k A
     \,,\,
     \Omega^\bullet_{poly}(\Delta^n) \otimes_k B
  \right)  
  \,,
$$

where on the right we have those dg-algebra homomorphism which in addition preserves the left [[dg-module]] structure over $\Omega^\bullet_{poly}(\Delta^n)$. This induces for any three $A,B,C \in dgcAlg^{\geq 0}_k$ a [[composition]] homomorphism of [[simplicial sets]] out of the [[Cartesian product]] of mapping spaces

$$
  \circ^{sSet}_{A,B,C}
  \;\colon\;
  Maps(A,B) \times Maps(B,C)
    \longrightarrow
  Maps(A,C)
  \,.
$$


=--

([Bousfield-Gugenheim 76, 5.1](#BousfieldGugenheim76))

+-- {: .num_remark}
###### Remark

The set of 0-simplices of of the [[mapping space]] $Maps(A,B)$ in def. \ref{MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees} is [[natural isomorphism|naturally isomorphic]] to the ordinary [[hom-set]] of dg-algebras:


$$
  Maps(A,B)_0 \simeq Hom_{dgcAlg^{\geq 0}_k}(A,B)
$$

and under this identification the two notions of [[composition]] agree.

=--

Definition \ref{MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees} makes $dgcAlg^{\geq 0}_k$ an [[sSet]]-[[enriched category]] ("[[simplicial category]]"). The follows says that it is also [[powering|powered]], not over all of $sSet$, but over finite simplicial sets: 

+-- {: .num_prop #PoweringOfdgcCchainAlgebrasInNonNegativeDegreeOverFiniteSimplicialSets}
###### Proposition
**(powering over finite simplicial sets)**

For $A, B \in dgcAlg^{\geq 0}_k$ and $S \in $ [[sSet]], there is a [[natural transformation]]

$$
  Hom_{dgcAlg^{\geq}_k}(A, \Omega^\bullet_{poly}(S) \otimes_k B)
   \longrightarrow
  Hom_{sSet}( S, Maps(A,B) )
$$

from the [[hom-set]] of [[dgc-algebras]] into the [[tensor product]] with the [[polynomial differential forms on n-simplices]] from def. \ref{MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees} to the [[hom-set]] in [[simplicial sets]] into the simplicial [[mapping space]] from def. \ref{MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees}. 

Moreover, this morphism is an [[isomorphism]] if one of the following conditions holds:

* $S$ is a [[finite set|finite]] [[simplicial set]];

* $B$ is of [[finite type]] (def. \ref{dgcCochainAlgebraInNonNegDegreeOfFiniteType}).

=--

([Bousfield-Gugenheim 76, lemma 5.2](#BousfieldGugenheim76))

+-- {: .num_prop}
###### Proposition
**(pullback powering axiom)**

Let $i \colon V \to W$ and $p \colon X \to Y$ be two [[morphisms]] in $dgcAlg^{\geq 0}_k$. Then their [[pullback power]] with respect to the simplicial [[mapping space]] functor (def. \ref{MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees})

$$
  p^i
  \;\colon\;
  Maps(W,X)
   \longrightarrow
  Maps(V,X)
   \underset{Maps(V,Y)}{\times}
  Maps(W,Y)
$$

is 

1. a [[Kan fibration]] if $i$ is a cofibration and $p$ a fibration in the projective [[model category]] structure from prop. \ref{IndeedProjectiveModelStructureOnCdgAlg};

1. in addition a [[weak homotopy equivalence]] (i.e. a weak equivalence in the [[classical model structure on simplicial sets]]) if at least one of $i$ or $p$ is a weak equivalence in the projective model structure from prop. \ref{IndeedProjectiveModelStructureOnCdgAlg}.

=--

([Bousfield-Gugenheim 76, prop. 5.3](#BousfieldGugenheim76))

+-- {: .num_remark}
###### Remark

Prop. \ref{PoweringOfdgcCchainAlgebrasInNonNegativeDegreeOverFiniteSimplicialSets} _would_ say that $(dgcAlg^{\geq 0}_k)_{proj}$ is a [[simplicial model category]] with respect to the simplicial enrichment from def. \ref{MappingSpaceSimOndgcCochainAlgebrasInNonNegDegrees} were it not for the fact that prop. \ref{PoweringOfdgcCchainAlgebrasInNonNegativeDegreeOverFiniteSimplicialSets} gives the [[powering]] only over finite simplicial sets.

=--

#### Relation to simplicial sets

+-- {: .num_prop} 
###### Proposition
**([[Quillen adjunction between simplicial sets and connective dgc-algebras]])**

The [[PL de Rham complex]]-construction is the [[left adjoint]] in a [[Quillen adjunction]] between

* the [[opposite model structure|opposite]] of the [[projective model structure on connective dgc-algebras]]

* the [[classical model structure on simplicial sets]]

$$
  \big(
    DiffGradedCommAlgebras^{\geq 0}_{k}
  \big)^{op}_{proj}
  \underoverset
    {
      \underset
        {\;\;\; exp \;\;\;}
        {\longrightarrow}
    }
    {
      \overset
        {\;\;\;\Omega^\bullet_{PLdR}\;\;\;}
        {\longleftarrow}
    }
    {\bot_{\mathrlap{Qu}}}
  SimplicialSets_{Qu}
$$

=--



#### Relation to cosimplicial commutative algbras

The [[monoidal Dold-Kan correspondence]] gives a [[Quillen equivalence]] to the [[model structure on cosimplicial algebras|projective model structure on cosimplicial commutative algebras]] $(cAlg_k^{\Delta})_{proj}$.


#### Preservation of weak equivalences under pushout
 {#PreservationOfWeakEquivalencesUnderPushout}

+-- {: .num_prop #PushoutAlongRelativeSullivanModelsPreservesQuasiIsos}
###### Proposition
**([[pushout]] along [[relative Sullivan models]] preserves [[quasi-isomorphisms]])**

In the projective model structure on connective dgc-algebras (Def. \ref{ProjectiveModelStructureOnCdgAlg}), the operation of [[pushout]] along a [[relative Sullivan model]] preserves weak equivalences (quasi-isomorphisms).

=--

This is [Felix-Halperin-Thomas 00, Lemma 14.2, using Prop. 6.7 (ii)](#FelixHalperinThomas00). 

The same statement for augmented dgc-algebras is in [Baues 88, Section I.8, Lemma 8.16](#Baues88).

+-- {: .num_remark}
###### Remark

Lemma 14.2 in [Felix-Halperin-Thomas 00](#FelixHalperinThomas00) is stated under the additional assumption that the dgc-algebras being pushed put have $H^0(-) = k$. But this is only used to find the stronger statement that the pushout is itself a Sullivan model. The argument via Prop. 6.7 that the pushout is a quasi-iso does not use this assumption.

=--

+-- {: .num_remark}
###### Remark

Prop. \ref{PushoutAlongRelativeSullivanModelsPreservesQuasiIsos} comes close to saying that the projective model structure on connective dgc-algebras is a [[left proper model category]], but not quite: The class of all [[cofibrations]] is larger than that of [[relative Sullivan algebras]], it includes also their [[retracts]] (see e.g [Hess 06](#Hess06)).

=--

#### Change of scalars

\begin{proposition}\label{ExtensionOfScalarsQuillenAdjunction}
  Let $k$ be a [[field]] of [[characteristic zero]], with 
  $\mathbb{Q} \xhookrightarrow{i} k$ the corresponding inclusion of the [[rational numbers]]. Then the iduced [[extension of scalars]]$\;\dashv\;$[[restriction of scalars]]-[[adjunction]]

$$
  \big(
    dgcAlg^{\geq 0}_k
  \big)_{proj}
    \underoverset
      {\underset{res_{\mathbb{Q}}}{\longrightarrow}}
      {\overset{ (-) \otimes_{\mathbb{Q}} \mathbb{R} }{\longleftarrow}}
      {\bot_{\mathrlap{Qu}}}
  \big(
    dgcAlg^{\geq 0}_{\mathbb{Q}}  
  \big)_{proj}
$$

is a [[Quillen adjunction]] between the respective projective model categories (Def. \ref{ProjectiveModelStructureOnCdgAlg}).

\end{proposition}
([Bousfield & Gugenheim 1976, Lemma 11.6](#BousfieldGugenheim76))
\begin{proof}
  It is immediate that [[restriction of scalars]] is a [[right Quillen functor]]: 

1. It preserves [[fibrations]], since these are the [[surjections]] of underlying sets, and restriction of scalars does not change the underlying sets.

1. It preserves [[weak equivalences]], since these are the [[isomorphisms]] on [[cochain cohomology]] [[cohomology groups|groups]] of underlying [[cochain complexes]], and, again, restriction of scalars does not change the underlying sets of the underlying cochain complexes.

\end{proof}

#### Commutative vs. non-commutative dg-algebras 
 {#CommVsNoncomm}

> this needs harmonization

+-- {: .num_prop }
###### Proposition


The [[forgetful functor]]

$$
  F dgcAlg_k \to dgAlg_k
$$

from (graded-)commutative [[dg-algebra]]s to dg-algebras is the [[right adjoint]] part of a [[Quillen adjunction]]

$$
  Ab
  \colon
  dgAlg 
   \stackrel{\leftarrow}{\to}
  CdgAlg
  :
  F
$$

=--

> boundedness?

+-- {: .proof}
###### Proof

The forgetful functor clearly preserves fibrations and cofibrations. It has a [[left adjoint]], the free abelianization functor $Ab$, which sends a [[dg-algebra]] $A$ to its quotient $A/[A,A]$.

=--


+-- {: .num_theorem }
###### Theorem

Let the ground [[ring]] $k$ be a [[field]] of [[characteristic zero]]. Then every [[dg-algebra]] $A$ which has the structure of an [[algebra over an operad|algebra over]] the [[E-k-operad|E-∞ operad]] has a [[dg-algebra]] morphism $A \to A_c$ to a commutative dg-algebra $A_c$  which is

* a morphism of [[E-k-operad|E-∞ algebras]] (where $A_c$ has the obvious [[E-k-operad|E-∞ algebras]] structure)

* a weak weak equivalence in the model structure on dg-algebras (i.e. a [[quasi-isomorphism]] of the underlying cochain complexes).

=--

This is in ([Kriz-May 95, II.1.5](#KrizMay95)).

So this says that the weak equivalence classes of the commutative dg-algebras in the model category of all dg-algebras already exhaust the most general non-commutative but  homotopy-commutative dg-algebras.

+-- {: .num_remark #HomotopyFaithfulnessOfforgettingCommutativity}
###### Remark

Discussion of a restricted kind of homotopy-faithfulness of the forgetful functor from the homotopy theory of commutative to not-necessarily commutative dg-algebras is in ([Amrani 14](#Amrani14)).

=--







## Unbounded dg-algebras {#Unbounded}

We discuss now the case of unbounded dg-algebras. For these there is no longer the [[monoidal Dold-Kan correspondence]] available. Instead, these can be understood as arising naturally as function $\infty$-algebras in the [[derived geometry|derived]] [[dg-geometry]] over formal duals of bounded dg-algebras, see [[function algebras on ∞-stacks]].

### Gradings and conventions {#GradingsAndConventions}

In [[derived geometry]] two categorical gradings interact: a [[cohesive (∞,1)-topos|cohesive]] $\infty$-groupoid $X$ has a space of [[k-morphism]]s $X_k$ for all non-negative $k$, and each such has itself a _[[simplicial T-algebra]]_ of functions with a component in each non-positive degree. But the directions of the face maps are opposite. We recall the grading situation from [[function algebras on ∞-stacks]].

Functions on a bare $\infty$-groupoid $K$, modeled as a [[simplicial set]], form a [[cosimplicial algebra]] $\mathcal{O}(K)$, which under the [[monoidal Dold-Kan correspondence]] identifies with a cochain [[dg-algebra]] (meaning: with positively graded differential) in non-negative degree

$$
  \left(
    \array{
        \vdots
       \\
       \downarrow \downarrow \downarrow \downarrow      
        \\
        K_2
       \\
       \downarrow^{\partial_0} \downarrow^{\partial_1} \downarrow^{\partial_2}
       \\
       K_1
       \\
       \downarrow^{\partial_0} \downarrow^{\partial_1}
       \\
       K_0
     }
  \right)
   \;\;\;\;\;
   \stackrel{\mathcal{O}}{\mapsto}
   \;\;\;\;\;
  \left(
  \array{
    \vdots
    \\
    \uparrow \uparrow \uparrow \uparrow   
    \\
    \mathcal{O}(K_2)
    \\
    \uparrow^{\partial_0^*} \uparrow^{\partial_1^*} \uparrow^{\partial_2^*}
    \\
    \mathcal{O}(K_1)
    \\
    \uparrow^{\partial_0^*} \uparrow^{\partial_1^*}
    \\
    \mathcal{O}(K_0)
  }
  \right)
   \;\;\;\;\;
  \stackrel{\sim}{\leftrightarrow}
   \;\;\;\;\;
  \left(
    \array{
     \cdots
     \\
     \uparrow^{\mathrlap{\sum_i (-1)^i \partial_i^*}}
     \\
     A_2
     \\
     \uparrow^{\mathrlap{\sum_i (-1)^i \partial_i^*}}
     \\
     A_1
     \\
     \uparrow^{\mathrlap{\sum_i (-1)^i \partial_i^*}}
     \\
     A_0
     \\
     \uparrow
     \\
     0
     \\
     \uparrow
     \\
     0
     \\
     \uparrow
     \\
     \vdots
   }
  \right)
  \,.
$$

On the other hand, a representable $X$ has itself a _[[simplicial T-algebra]]_ of functions, which under the monoidal Dold-Kan correspondence also identifies with a cochain dg-algebra, but then necessarily in non-positive degree to match with the above convention. So we write

$$
  \mathcal{O}(X)
   \;\;\;\;\;
  =
   \;\;\;\;\;
  \left(
   \array{
     \mathcal{O}(X)_0
     \\
     \uparrow \uparrow
     \\
     \mathcal{O}(X)_{-1}
     \\
     \uparrow \uparrow \uparrow
     \\
     \mathcal{O}(X)_{-2}
     \\
     \uparrow \uparrow \uparrow \uparrow
     \\
     \vdots
   }
  \right)
   \;\;\;\;\;
  \stackrel{\sim}{\leftrightarrow}
   \;\;\;\;\;
  \left(
    \array{
        \vdots
        \\
        \uparrow
        \\
        0
        \\
        \uparrow
        \\
        0
        \\
        \uparrow
        \\
       \mathcal{O}(X)_0
       \\
       \uparrow
       \\
       \mathcal{O}(X)_{-1}
       \\
       \uparrow
       \\
       \mathcal{O}(X)_{-2}
       \\
       \uparrow
       \\
       \vdots
    }
  \right)
  \,.
$$

Taking this together, for $X_\bullet$ a general [[∞-stack]], its function algebra is generally an _unbounded_ cochain dg-algebra with mixed contributions as above, the simplicial degrees contributing in the positive direction, and the homological resolution degrees in the negative direction:

$$
  \mathcal{O}(X_\bullet)
   \;\;\;\;\;
   =
   \;\;\;\;\;
  \left(
     \array{
        \vdots
        \\
        \uparrow
        \\
        \bigoplus_{k-p = q} \mathcal{O}(X_k)_{-p}
        \\
        \uparrow
        \\
        \vdots
        \\
        \uparrow^d
        \\
        \mathcal{O}(X_1)_0 \oplus \mathcal{O}(X_2)_{-1} \oplus 
          \mathcal{O}(X_3)_{-2} \oplus \cdots
        \\
        \uparrow^{d}
        \\
        \mathcal{O}(X_0)_0 \oplus \mathcal{O}(X_1)_{-1} \oplus 
          \mathcal{O}(X_2)_{-2} \oplus \cdots
        \\
        \uparrow^{d}
        \\
        \mathcal{O}(X_0)_{-1} \oplus \mathcal{O}(X_1)_{-2} \oplus 
          \mathcal{O}(X_2)_{-3}\oplus \cdots       
        \\
        \uparrow^{d}
        \\
        \vdots
     }
  \right)
  \,.
$$ 



### Definition


+-- {: .num_theorem }
###### Theorem

For $k$ a [[field]] of [[characteristic]] 0 let 

$$
  cdgAlg = CMon(Ch_\bullet(k))
$$ 

be the category of undounded commutative dg-algebras. With fibrations the degreewise surjections and weak equivalences the [[quasi-isomorphism]]s this is a 

* [[model category]]

which is

* [[proper model category|proper]];

* [[combinatorial model category|combinatorial]].

=--

The existence of the model structure follows from the general discussion at [[model structure on dg-algebras over an operad]]. 

Properness and combinatoriality is discussed in ([To&#235;nVezzosi](#ToenVezzosi)):

* in lemma 2.3.1.1 they state that $cdgAlg_+$ constitutes the first two items in a triple which they call an _HA context_ .

* this implies their assumption 1.1.0.4 which asserts properness and
  combinatoriality

Discussion of cofibrations in $dgAlg_{proj}$ is in ([Keller](#Keller)).

### Properties

#### Properness

Let $cdgAg_k$ be the projective model structure on commutative unbounded dg-algebras from above.

This is a [[proper model category]]. See MO discussion [here](http://mathoverflow.net/q/204414/381).


#### Derived tensor product

Let $cdgAg_k$ be the projective model structure on commutative unbounded dg-algebras from above

+-- {: .num_prop }
###### Proposition

For cofibrant $A \in cdgAlg_k$, the functor

$$
  A\otimes_k (-) : k Mod \to A Mod
$$

preserves [[quasi-isomorphism]]s.

For $A,B \in cdgAlg_k$, their [[derived functor|derived]] [[coproduct]] in $k Mod$ coincides in the [[homotopy category]] with the derived [[tensor product]] in $k Mod$: the morphism

$$
  A \coprod_k^{L} B \stackrel{}{\to} A \otimes_k^L B
$$

is an isomorphism in $Ho(k Mod)$.

=--

This follows by the above with ([To&#235;nVezzosi, assumption 1.1.0.4, and page 8](#ToenVezzosi)).


#### Derived hom-functor {#SimplicialHomObjects}

The model structure on unbounded dg-algebras is _almost_ a [[simplicial model category]]. See the section _[simplicial enrichment](model+structure+on+dg-algebras+over+an+operad#SimplicialEnrichment)_ at _[[model structure on dg-algebras over an operad]]_ for details.


+-- {: .num_defn }
###### Definition

Let $k$ be a [[field]] of [[characteristic]] 0. Let 
$\Omega^\bullet_{poly} : sSet \to (cdgAlg_k)^{op}$ be the functor that assigns polynomial [[differential forms on simplices]].

For $A,B \in dgcAlg_k$ define the [[simplicial set]]

$$
cdgAlg_k(A,B) : ([n] \mapsto Hom_{cdgAlg_k}(A, B \otimes_k \Omega^\bullet_{poly}(\Delta[n]))
  \,.
$$

This extends to a functor

$$
  cdgAlg_k(-,-) : cdgAlg_k^{op} \times cdgAlg_k \to sSet
  \,.
$$

=--

+-- {: .num_prop }
###### Proposition

The functor $cdgAlg_k(-,-)$ satisfies the dual of the [[pushout-product axiom]]: for $i : A \to B$ any cofibration in $cdgAlg_k$ and $p : X \to Y$ any fibration, the canonical morphism

$$
  (i^*, p_*) : cdgalg_k(A,B) \to 
    cdgAlg_k(A,X)
      \times_{cdgAlg_k(A,Y)} cdgAlg_k(B,Y)
$$

is a [[Kan fibration]], which is acyclic if $i$ or $p$ is.

=--

This implies in particular that for $A$ cofibrant, $cdgAlg_k(A,B)$ is a [[Kan complex]].


The proof works along the lines of ([Bousfield-Gugenheim 76, prop. 5.3](#BousfieldGugenheim76)). See also the discussion at [[model structure on dg-algebras over an operad]].


+-- {: .proof}
###### Proof

We give the proof for a special case. The general case is analogous.

We show that for $A$ cofibrant, and for any $B$ (automatically fibrant), $cdgAlg_k(A,B)$ is a [[Kan complex]].


By a standard fact in [[rational homotopy theory]] (due to [Bousfield-Gugenheim 76](#BousfieldGugenheim76), discussed at [[differential forms on simplices]]) we have that $\Omega^\bullet_{poly} : sSet \to (cdgAlg^+_k)^{op}$ is a left [[Quillen adjunction|Quillen functor]], hence in particular sends acyclic cofibrations to acyclic cofibrations, hence acyclic [[monomorphism]]s of [[simplicial set]]s to acyclic fibrations of [[dg-algebra]]s. 

Specifically for each [[horn]] inclusion $\Lambda[n]_k \hookrightarrow \Delta[n]$ we have that the restriction map $\Omega^\bullet_{poly}(\Delta[n]) \to \Omega^\bullet_{poly}(\Lambda[n]_k)$ is an acyclic fibration in $cdgAlg_k^*$, hence in $cdgAlg_k$.

A $k$-horn in $cdgAlg_k(A,B)$ is a morphism $A \to B \otimes \Omega^\bullet_{poly}(\Lambda[n]_k)$. A filler for this horn is a lift $\sigma$ in 

$$
  \array{
    && B \otimes \Omega^\bullet_{poly}(\Delta[n])
    \\
    & {}^{\mathllap{\sigma}}\nearrow & \downarrow
    \\
    A &\to& B \otimes \Omega^\bullet_{poly}(\Lambda[n]_k)
  }
  \,.
$$

If $A$ is cofibrant, then such a lift does always exist.

=--

+-- {: .num_prop }
###### Proposition

For $A \in cdgAlg$ cofibrant, $cdgAlg_k(A,B)$ is the correct [[derived hom-space]]


$$
  cdgAlg_k(A,B)
  \simeq
  \mathbb{R}Hom(A,B)   
  \,.
$$

=--


+-- {: .proof}
###### Proof

By the assumption that $A$ is cofibrant and according to the facts discussed at [[derived hom-space]], we need to show that

$$
  s B : [n] \mapsto B\otimes_k \Omega^\bullet_{poly}(\Delta[n])
$$

is a [[simplicial resolution|resolution]], or _simplicial frame_ for $B$. (Notice that every object is fibrant in $cdgAlg_k$).

Since polynomial differential forms are acyclic on simplices (discussed [here](http://nlab.mathforge.org/nlab/show/differential+forms+on+simplices)) it follows that 

$$
  const B \to s B
$$

is degreewise a weak equivalence. It remains to show that $s A$ is fibrant in the [[Reedy model structure]] $[\Delta^{op}, cdgAlg_k]_{Reedy}$. 

One finds that the matching object is given by

$$
  (match s B)_k = B \otimes \Omega^\bullet_{poly}(\partial \Delta[k])
  \,.
$$

Therefore $s B$ is Reedy fibrant if in each degree the morphism 

$$
  (s B_k \to (match s B)_k ) = (\Omega^\bullet_{poly}(\partial \Delta[k] \hookrightarrow \Delta[k]))
$$

is a fibration. But this follows from the fact that $\Omega^\bullet_{poly} : sSet \to cdgAlg_k^{op}$ is a left [[Quillen adjunction|Quillen functor]] (as discussed at [[differential forms on simplices]]).
=--

#### Derived copowering over $sSet$ {#DerivedCopowering}

We discuss a concrete model for the $(\infty,1)$-copowering of 
$(cdgAlg_k)^\circ$ over [[∞Grpd]] in terms of an operation of $cdgAlg_k$ over [[sSet]].

First notice a basic fact about ordinary commutative algebras.

+-- {: .num_prop}
###### Proposition

In $CAlg_k$ the [[coproduct]] is given by the [[tensor product]] over $k$:

$$
  \left(
  \array{
    A 
      &\stackrel{i_A}{\to}& 
    A \coprod B 
      &\stackrel{i_B}{\leftarrow}& 
    B
   }
  \right)
  \simeq
  \left(
    \array{
      A 
        &\stackrel{Id_A \otimes_k e_B}{\to}& 
      A \otimes_k B 
        & \stackrel{e_A \otimes Id_B}{\leftarrow}&
      B
   }
  \right)
$$

=--

+-- {: .proof}
###### Proof

We check the [[universal property]] of the coproduct: for $C \in CAlg_k$ and $f,g : A,B \to C$ two morphisms, we need to show that there is a unique morphism $(f,g) : A \otimes_k B \to C$  such that the diagram

$$
  \array{
    A 
     &\stackrel{Id_A \otimes e_B}{\to}&
    A \otimes_k B
     &\stackrel{e_A \otimes Id_B}{\leftarrow}&
    B
    \\
    & {}_{\mathllap{f}}\searrow & \downarrow^{\mathrlap{(f,g)}} & \swarrow_{\mathrlap{g}} 
    \\
    && C
  }
$$

commutes.
For the left triangle to commute we need that $(f,g)$ sends elements of the form $(a,e_B)$ to $f(a)$. For the right triangle to commute we need that $(f,g)$ sends elements of the form $(e_A, b)$ to $g(b)$. Since every element of $A \otimes_k B$ is a product of two elements of this form

$$
  (a,b) = (a,e_B) \cdot (e_A, b)
$$

this already uniquely determines $(f,g)$ to be given on elements by the map

$$
  (a,b) \mapsto f(a) \cdot g(b)
  \,.
$$

That this is indeed an $k$-algebra homomorphism follows from the fact that $f$ and $g$ are

=--

+-- {: .num_remark}
###### Remark

For these derivations it is crucial that we are working with commutative algebras.

=--

+-- {: .num_cor}
###### Corollary

We have that the [[copower]]ing of $A$ with the map of sets from two points to the single point

$$
  (* \coprod * \to *) \cdot A
  \simeq
  (
    A \otimes_k A
     \stackrel{\mu}{\to}
    A
  )
$$

is the product morphism on $A$. And that the tensoring with the map from the empty set to the point 

$$
  (\emptyset \to *)\cdot A
  \simeq
  (k \stackrel{e_A}{\to} A)
$$

is the unit morphism on $A$. Generally, for $f : S \to T$ any map of sets we have that the tensoring

$$
  (S \stackrel{f}{\to} T) \cdot A
  =
  A^{\otimes_k |S|}
  \to
  A^{\otimes_k |T|}
$$

is the morphism between [[tensor power]]s of $A$ of the cardinalities of $S$ and $T$, respectively, whose component over a copy of $A$ on the right corresponding to $t \in T$ is the iterated product $A^{\otimes_k |f^{-1}\{t\}|} \to A$ on as many tensor powers of $A$ as there are elements in the preimage of $t$ under $f$.

=--

The analogous statements hold true with $CAlg_k$ replaced by $cdgAlg_k$: for $S \in sSet$ and $ A \in cdgAlg_k$ we obtain a simplicial cdg-algebra 

$$
  S \cdot A \in cdgAlg_k^{\Delta^{op}}
$$ 

by the ordinary degreewise [[copower]]ing over [[Set]], using that $cdgAlg_k$ has coproducts (equal to the tensor product over $k$).

This is equivalently a commutative monoid in simplicial unbounded chain complexes

$$
  cdgAlg_k^{\Delta^{op}} \simeq CMon(Ch^\bullet(k)^{\Delta^{op}})
  \,.
$$

By the logic of the [[monoidal Dold-Kan correspondence]] the symmetric [[lax monoidal functor|lax monoidal]] [[Moore complex]] functor (via the [[Eilenberg-Zilber map]]) sends this to a commutative [[monoid]] in non-positively graded cochain complexes in unbounded cochain complexes

$$
  C^\bullet(S \cdot A) \in CMon(Ch^\bullet_-(Ch^\bullet(k)))
  \,.
$$

Since the [[total complex]] functor $Tot : Ch^\bullet(Ch^\bullet(k)) \to Ch^\bullet(k)$ is itself symmetric lax monoidal (...), this finally yields

$$
  Tot C^\bullet(S \cdot A) \in CMon(Ch^\bullet(k)) \simeq
    cdgAlg_k
$$


+-- {: .num_defn}
###### Definition

Define the functor

$$  
  CC : sSet \times cdgAlg \to cdgAlg
$$

by 

$$
  CC(S,A) := Tot C^\bullet(S \cdot A) 
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

We have 

$$
  CC(Y,A)^n := \bigoplus_{k \geq 0} (A^{\otimes_k |Y_k| })_{n+k}
$$

=--

This appears essentially (...) as ([GinotTradlerZeinalian, def 3.1.1](#GinotTradlerZeinalian)).


+-- {: .num_prop}
###### Proposition

The [[(∞,1)-limit|(∞,1)-copowering]] of $(dgcAlg_k)^\circ$ over [[∞Grpd]] is modeled by the [[derived functor]] of $CC$.

=--


This follows from ([GinotTradlerZeinalian, theorem 4.2.7](#GinotTradlerZeinalian)), which asserts that the [[derived functor]] of this tensoring is the unique [[(∞,1)-functor]], up to equivalence, satisfying the axioms of $(\infty,1)$-copowering.




+-- {: .num_prop}
###### Proposition

The functor

$$
  CC : sSet \times cdgAlg_k \to cdgAlg_k
$$

preserves weak equivalences in both arguments.

=--

This is essentially due to ([Pirashvili](#Pirashvili)). The full statement is ([GinotTradlerZeinalian, prop. 4.2.1](#GinotTradlerZeinalian)).


+-- {: .num_remark}
###### Remark

This means that the assumption for the copowering models of higher order [[Hochschild cohomology]] are satsified in $cdgAlg_k$ which are described in the section <a href="http://nlab.mathforge.org/nlab/show/Hochschild+cohomology#PirashviliHigherOrder">Pirashvili's higher Hochschild homology</a> is satisfied:

this means that for $A \in cdgAlg$ and $S \in sSet$, $CC(S,A)$ is a model for the function $\infty$-algebra on the [[free loop space object]] of $Spec A$. See the section <a href="http://nlab.mathforge.org/nlab/show/Hochschild+cohomology#OvercdgAlgs">Higher order Hochschild homology modeled on cdg-algebras</a> for more details.


=--


#### Derived powering over $sSet$ {#DerivedPowering}


+-- {: .num_prop}
###### Claim

Let $S \in \infty Grpd$ be presented by a degreewise finite [[simplicial set]] (which we denote by the same symbol).

Then the [[homotopy limit]] in $cdgAlg_k$ over the $S$-shaped diagram constant on $k$ is given by $\Omega^\bullet_{poly}(S)$.

$$
  \mathbb{R}{\lim_{\leftarrow}}_S const k \simeq \Omega^\bullet_{poly}(S) 
  \,.
$$

=--

+-- {: .proof}
###### Proof

We show dually that for degreewise finite $S$ the assignment $(S, Spec A) \mapsto Spec (\Omega^\bullet_{poly}(S) \otimes A)$ models the $\infty$-copowering in $cdgAlg_k^{op}$.

By the discussion at <a href="http://nlab.mathforge.org/nlab/show/limit+in+a+quasi-category#Tensoring">(∞,1)-copowering</a> it is sufficient to to establish an equivalence

$$
  (dgcAlg_{k}^{op})^\circ(Spec (\Omega^\bullet_{poly}(S) \otimes A), Spec B)
  \simeq
   \infty Grpd(S, (dgcAlg_{k}^{op})^\circ(Spec A, Spec B))
$$

natural in $B$. Consider a cofibrant model of $B$, which we denote by the same symbol. The we compute with 1-categorical [[end]]/[[coend]] calculus
 
$$
  \begin{aligned}
    sSet(S, cdgAlg_k^{op}(Spec A,Spec B))
    & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot Hom_{sSet}(S \times \Delta[r], 
        cdgAlg_k^{op}(Spec A, Spec B))
   \\
   & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
      \int_{[k] \in \Delta}
       Hom_{Set}(S_k \times \Delta[k,r], 
        Hom_{cdgAlg_k^{op}}(Spec \Omega^\bullet_{poly}(\Delta^k) \times Spec A, Spec B))   
   \\
   & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
      \int_{[k] \in \Delta} 
        Hom_{cdgAlg_k^{op}}((S_k \times \Delta[k,r]) \cdot Spec \Omega^\bullet_{poly}(\Delta^k) \times Spec A, Spec B))   
    \\
    & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
        Hom_{cdgAlg_k^{op}}(\int^{[k] \in \Delta} 
 (S_k \times \Delta[k,r]) \cdot Spec \Omega^\bullet_{poly}(\Delta^k) \times Spec A, Spec B))       
    \\
    & \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
        Hom_{cdgAlg_k^{op}}(Spec \Omega^\bullet_{poly}(S \times \Delta[r]) \times Spec A, Spec B))       
  \end{aligned}
  \,,
$$

where all steps are [[isomorphism]]s and the dot denotes the ordinary 1-categorical [[copower]]ing of the 1-category $cdgAlg^{op}$ over [[Set]]. In the last step we are using that the [[tensor product]] commutes with finite limits of dg-algebras. (This is where the finiteness assumption is needed). 

Now we use that $\Omega^\bullet_{poly}$ preserves [[product]]s up to [[quasi-isomorphism]] (as discussed <a href="http://nlab.mathforge.org/nlab/show/differential+forms+on+simplices#Properties">here</a>)

$$
  \Omega^\bullet_{poly}(S \times \Delta[r])
  \simeq
  \Omega^\bullet_{poly}(S) \otimes \Omega_{poly}^\bullet(\Delta[r])
  \,.
$$

This being a weak equivalence between fibrant objects and since $B$ is assumed cofibrant, we have by the [above discussion](#SimplicialHomObjects) of the derived hom-functor (and using the [[factorization lemma]]) a weak equivalence

$$
  \cdots \simeq
    \int^{[r] \in\Delta}
      \Delta[r] \cdot 
        Hom_{cdgAlg_k^{op}}(Spec \Omega^\bullet_{poly}(S) \times Spec \Omega^\bullet_{poly}\Delta[r]) \times Spec A, Spec B))       
  \,.
$$

Since all this is [[natural transformation|natural]] in $B$, this proves the claim. 

=--

#### Path objects
 {#PathObjectsForUnboundedCommutative}
+-- {: .num_prop}
###### Proposition

For $A \in cdgAlg_k$, a [[path object]]

$$
  A \stackrel{\simeq}{\to} P(A) \stackrel{fib}{\to} A \times A
$$

for $A$ is given by

$$
  P(A) := A \otimes_k \Omega^\bullet_{poly}(\Delta[1])
$$

=--

This follows along the above lines. The statement appears for instance as
([Behrend, lemma 1.19](#Behrend)).

#### Relation to $H \mathbb{Z}$-algebra spectra
 {#RelationToAInfinityAlgebras}

For every [[ring spectrum]] $R$ there is the notion of [[algebra spectra]] over $R$. Let $R := H \mathbb{Z}$ be the [[Eilenberg-MacLane spectrum]] for the [[integer]]s. Then unbounded dg-algebras (over $\mathbb{Z}$) are one model for $H \mathbb{Z}$-algebra spectra.


+-- {: .num_prop}
###### Proposition

There is a [[Quillen equivalence]] between the standard [[model category]] structure for $H \mathbb{Z}$-[[algebra spectra]] and the model structure on unbounded differential graded algebras.

=--

See [[algebra spectrum]] for details.

#### Relation to $\mathbb{E}_\infty$-algebras
 {#RelationToEInfinityAlgebras}

Commutative dg-algebras 
over a field $k$ of characteristic 0 constitute a presentation of 
[[E-infinity algebras]] over $k$ ([Lurie, prop. A.7.1.4.11]).

## Related concepts

* [[model structure on equivariant dgc-algebras]]

* [[model structure on differential graded-commutative superalgebras]]

* [[model structure on chain complexes]]

* [[model structure on dg-modules]]

* [[model structure on dg-operads]]

* [[model structure on dg-algebras over an operad]]

  * **model structure on dg-algebras**

  * [[model structure on dg-categories]]

* [[model structure on dg-coalgebras]]

## References

### On connective dgc-algebras

The cofibrantly generated model structure on [[differential graded-commutative algebras]] is originally due to 

* {#BousfieldGugenheim76} [[Aldridge Bousfield]], [[Victor Gugenheim]], _[[On PL deRham theory and rational homotopy type]]_, Memoirs of the AMS 179 (1976) ([ams:memo-8-179](https://bookstore.ams.org/memo-8-179))

Textbook account:

* {#GelfandManin96} [[Sergei Gelfand]], [[Yuri Manin]], Chapter V of: _[[Methods of homological algebra]]_,  transl. from the 1988 Russian (Nauka Publ.) original, Springer 1996. xviii+372 pp. 2nd corrected ed. 2002 ([doi:10.1007/978-3-662-12492-5](https://doi.org/10.1007/978-3-662-12492-5))

Review:

* {#Hess06} [[Kathryn Hess]], p. 6 of: _Rational homotopy theory: a brief introduction_, contribution to _[Summer School on Interactions between Homotopy Theory and Algebra](https://jdc.math.uwo.ca/summerschool/)_, University of Chicago, July 26-August 6, 2004, Chicago ([arXiv:math.AT/0604626](http://arxiv.org/abs/math.AT/0604626)), chapter in Luchezar Lavramov, [[Dan Christensen]], [[William Dwyer]], [[Michael Mandell]], [[Brooke Shipley]] (eds.), _Interactions between Homotopy Theory and Algebra_, Contemporary Mathematics 436, AMS 2007 ([doi:10.1090/conm/436](http://dx.doi.org/10.1090/conm/436))

* {#Moerman15} [[Joshua Moerman]], Section II of: _Rational Homotopy Theory_, 2015 ([pdf](https://www.ru.nl/publish/pages/813282/rational_homotopy_theory.pdf), [[MoermanRationalHomotopyTheory.pdf:file]])


The approach in [Hess 06](#Hess06) makes use of the general discussion in section 3 of 

* [[Paul Goerss]], [[Kirsten Schemmerhorn]], _Model categories and simplicial methods_, Notes from lectures given at the University of Chicago, August 2004, in: _Interactions between Homotopy Theory and Algebra_, Contemporary Mathematics 436, AMS 2007([arXiv:math.AT/0609537](http://arxiv.org/abs/math.AT/0609537), [doi:10.1090/conm/436](http://dx.doi.org/10.1090/conm/436))

that obtains the model structure from the [[model structure on chain complexes]].

See also 



* {#Baues88} Baues, Chapter I.8 of: _Algebraic Homotopy_ ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/baues4.pdf)

* {#FelixHalperinThomas00} [[Yves Félix]], [[Stephen Halperin]], [[Jean-Claude Thomas]], _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000 ([doi:10.1007/978-1-4613-0105-9](https://link.springer.com/book/10.1007/978-1-4613-0105-9))

Generalization to [[equivariant rational homotopy theory]]:

* [[Laura Scull]], _A model category structure for equivariant algebraic models_, Transactions of the American Mathematical Society 360 (5), 2505-2525, 2008 ([doi:10.1090/S0002-9947-07-04421-2](https://doi.org/10.1090/S0002-9947-07-04421-2))


### On non-commutative dg-algebras


For general **non-commutative** (or rather: not necessarily graded-commutative) dg-algebras a model structure is given in

* {#Jardine97} [[J. F. Jardine]], _[[JardineModelDG.pdf:file]]_, Cyclic Cohomology and Noncommutative Geometry, Fields Institute Communications, Vol. 17, AMS (1997), 55-58. 

This is also the structure used in 

* J.L. Castiglioni G. Corti&#241;as, _Cosimplicial versus DG-rings: a version of the Dold-Kan correspondence_ ([arXiv](http://arxiv.org/abs/math/0306289v2))

where aspects of its relation to the [[model structure on cosimplicial rings]] is discussed. (See [[monoidal Dold-Kan correspondence]] for
more on this).

### On unbounded dg-algebras

Discussion of the model structure on unbounded dg-algebras over a field of characteristic 0 is in 

* {#ToenVezzosi} [[Bertrand Toën]], [[Gabriele Vezzosi]], _HAG II, geometric stacks and applicatons_ ([arXiv:math/0404373v4](http://arxiv.org/abs/math/0404373v4))


A general discussion of algebras over an operad in unbounded chain complexes is in

* {#Hinich} [[Vladimir Hinich]],  _Homological algebra of homotopy algebras_ Communications in algebra, 25(10). 3291-3323 (1997)([arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), _Erratum_ ([arXiv:math/0309453](http://arxiv.org/abs/math/0309453)))


A survey of some useful facts with an eye towards [[dg-geometry]] is in

* {#Behrend} [[Kai Behrend]], _Differential graded schemes I: prefect resolving algebras_ ([arXiv:0212225](http://arxiv.org/abs/math/0212225))


Discussion of cofibrations in unbounded dg-algebras are in 

* {#Keller} [[Bernhard Keller]], _$A_\infty$-algebras, modules and functor categories_ ([pdf](http://www.math.jussieu.fr/~keller/publ/ainffun.pdf))


### More

The derived copowering of unbounded commutative dg-algebras over $sSet$ is discussed (somewhat implicitly) in

* {#GinotTradlerZeinalian} [[Grégory Ginot]], Thomas Tradler, Mahmoud Zeinalian, _Derived higher Hochschild homology, topological chiral homology and factorization algebras_, ([arxiv/1011.6483](http://arxiv.org/abs/1011.6483))


The _commutative_ product on the dg-algebra of the higher order Hochschild complex is discussed in

* [[Grégory Ginot]], Thomas Tradler, Mahmoud Zeinalian, _A Chen model for mapping spaces and the surface product_ ([pdf](http://arxiv.org/PS_cache/arxiv/pdf/0905/0905.2231v1.pdf))
{#GinotTradlerZeinalianChenModel}

The relation to [[E-infinity algebras]] is discussed in  

* {#KrizMay95} [[Igor Kriz]] and [[Peter May]], _Operads, algebras, modules and motives_ , Ast&eacute;risque No 233 (1995)

* {#Lurie} [[Jacob Lurie]], section 7.1 of _Higher algebra_ ([pdf](http://www.math.harvard.edu/~lurie/papers/higheralgebra.pdf))
 

The relation between commutative and non-commutative dgas is further discussed in 

* {#Amrani14} [[Ilias Amrani]], _Comparing commutative and associative unbounded differential graded algebras over Q from homotopical point of view_ ([arXiv:1401.7285](http://arxiv.org/abs/1401.7285))

* {#Amrani14b} [[Ilias Amrani]], _Rational homotopy theory of function spaces and Hochschild cohomology_ ([arXiv:1406.6269](http://arxiv.org/abs/1406.6269))

For more see also at _[[model structure on dg-algebras over an operad]]_.

Discussion of [[homotopy limits]] and [[homotopy colimits]] of dg-algebras is in 

* {#Walter06} [[Ben Walter]], _Rational Homotopy Calculus of Functors_ ([arXiv:math/0603336](http://arxiv.org/abs/math/0603336))


[[!redirects model structure on dg-rings]]
[[!redirects model structure on dg-algebra]]
[[!redirects Sullival algebra]]
[[!redirects model structures on dg-algebras]]

[[!redirects model structure on differential graded-commutative algebras]]
[[!redirects model structures on differential graded-commutative algebras]]

[[!redirects projective model structure on differential graded-commutative algebras]]
[[!redirects projective model structures on differential graded-commutative algebras]]

[[!redirects model structure on dgc-algebras]]
[[!redirects model structures on dgc-algebras]]

[[!redirects model structure on connective dgc-algebras]]
[[!redirects model structures on connective dgc-algebras]]


[[!redirects projective model structure on dgc-algebras]]
[[!redirects projective model structures on dgc-algebras]]

[[!redirects projective model structure on connective dgc-algebras]]
[[!redirects projective model structures on connective dgc-algebras]]




