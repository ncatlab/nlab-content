
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[intensional type theory]], [[identity types]] behave like [[path space objects]]; this viewpoint is called [[homotopy type theory]].  This induces furthermore a notion of [[homotopy fibers]], hence of [[homotopy equivalence]]s between [[types]].

On the other hand, if type theory contains a [[type universe]] $U$, so that types can be considered as *points* of $U$, then between two types we also have an [[identity type]] $X =_U Y$.  The _univalence axiom_ says that these two notions of "sameness" for types are the same.  

Extensionality principles like [[function extensionality]], [[propositional extensionality]] (where $X$ and $Y$ are [[h-propositions]]), and univalence ("typal extensionality") are naturally regarded as a stronger form of _[[identity of indiscernibles]]_. In particular, the [[consistency]] of univalence means that in [[Martin-Löf type theory]] without univalence, one cannot define any [[predicate]] that provably distinguishes isomorphic [[types]]; thus isomorphic types are "externally indiscernible", and univalence incarnates that principle internally by making them identical.

The name *univalence* (due to Voevodsky, see [Voevodsky 14](#Voevodsky14) for etymology) comes from the following reasoning.  A fibration or bundle $p\colon E\to B$ of some sort is commonly said to be *universal* if every other bundle of the same sort is a pullback of $p$ in a unique way (up to homotopy).  Less commonly, a bundle is said to be *versal* if every other bundle is a pullback of it in *some* way, not necessarily unique.  By contrast, a bundle is said to be *univalent* if every other bundle is a pullback of it in *at most one* way (up to homotopy).  In the language of [[(∞,1)-category]] theory, a univalent bundle is an [[object classifier]].

The univalence axiom does not *literally* say that anything is univalent in this sense.  However, it is *equivalent* to saying that the canonical fibration over $U$ is univalent: every fibration with $U$-_small_ fibers is an essentially unique pullback of this one.  For a description of this equivalence, see section 4.8 of the [[HoTT Book]] (syntactically) and [Gepner-Kock](#GepnerKock12) (semantically).

Univalence is a commonly assumed [[axiom]] in [[homotopy type theory]], and is central to the proposal ([Voevodsky](#Voevodsky)) that this provides a natively [[homotopy theory|homotopy theoretic]] [[foundation]] of [[mathematics]] (see at _[[univalent foundations for mathematics]]_).

## Definition

We work in a [[dependent type theory]] with [[identity types]], [[function types]], [[dependent product types]], [[product types]], and [[dependent sum types]]. 

There are multiple notions of [[equivalence types]] in [[dependent type theory]], which can be used for a definition of univalence for a [[type universe]] $U$; these include

* various notions of (weak) [[equivalence types]]
  * the type of [[functions]] with [[contractible type|contractible]] [[fiber type|fibers]]
  * the type of [[spans]] with contractible fibers
  * the type of [[multivalued partial functions]] which are single-valued and [[total function|total]] and have contractible fibers
  * the type of [[one-to-one correspondences]]
* type of $U$-small equivalences, given a type universe $U$ and a definition of equivalence above

Let us assume an arbitrary notion of equivalence type $\simeq_0$. Every [[Russell universe]] $U$ is a [[reflexive graph]] with the graph type family $R(A, B)$ defined as $R(A, B) \coloneqq A \simeq_0 B$ and the function $\mathrm{idtofam}(A, B)$ is defined as 

$$\mathrm{idtofam}(A, B) \coloneqq \mathrm{idtoequiv}(A, B)$$

Similarly, every [[Tarski universe]] $U$ with universal type family $T$ is a [[reflexive graph]] with the graph type family $R(A, B)$ defined as $R(A, B) \coloneqq T(A) \simeq_0 T(B)$ and the function $\mathrm{idtofam}(A, B)$ is defined as 

$$\mathrm{idtofam}(A, B) \coloneqq \mathrm{transport}^T(A, B)$$

And finally, every [[Tarski universe]] $U$ with type of terms $T$ and function $\mathrm{typeof}:T \to U$ is a reflexive graph with the graph type family $R(A, B)$ defined as 

$$R(A, B) \coloneqq \left(\sum_{t:T} \mathrm{typeOf}(t) =_U A\right) \simeq \left(\sum_{t:T} \mathrm{typeOf}(t) =_U B\right)$$

and the function $\mathrm{idtofam}(A, B)$ is defined as 

$$\mathrm{idtofam}(A, B) \coloneqq \mathrm{transport}^{\sum_{t:T} \mathrm{typeOf}(t) =_U (-)}(A, B)$$

Now, let us assume an arbitrary notion of equivalence type $\simeq$. A Russell or Tarski universe is **univalent** if it is [[univalent reflexive graph|univalent]] as a [[reflexive graph]], or equivalently, if one of the following equivalent conditions by the [[fundamental theorem of identity types]] hold:

1. That for each $x:A$ the type of elements $y:A$ such that $R(x, y)$ is a [[contractible type]]. 
$$x:A \vdash \mathrm{ua}(x):\mathrm{isContr}\left(\sum_{y:A} R(x, y)\right)$$

1. That there is a family of equivalences 
$$x:A, y:A \vdash \mathrm{ua}(x, y):(x =_A y) \simeq R(x, y)$$

1. That $R(x, y)$ is an [[identity system]]. 

1. That for each $x:A$ and $y:A$, the function $\mathrm{idtofam}(x, y)$ is an [[equivalence of types]]
$$x:A, y:A, \vdash \mathrm{ua}(x, y):\mathrm{isEquiv}(\mathrm{idtofam}(x, y))$$

1. That $\mathrm{idtofam}(x, y)$ is a [[retraction]] (This is due to [[Daniel Licata]] in [Licata 16](#Licata16))
$$x:A, y:A \vdash \mathrm{ua}(x, y):R(x, y) \to (x =_A y)$$
$$x:A, y:A, r:R(x, y) \vdash G(x, y):\mathrm{idtofam}(x, y, \mathrm{ua}(x, y, r)) =_{R(x, y)} r$$

1. That $R(x, y)$ with the function $\mathrm{idtofam}(x, y)$ satisfies the [[universal property]] of the [[unary sum]] of $x =_A y$. 

See [[fundamental theorem of identity types]] for proofs that these definitions are the same. 

### Decomposition
 {#Decomposition}

Assuming [[function extensionality]], [[Ian Orton]] and [[Andrew Pitts]] showed in [Orton and Pitts 19](#OrtonPitts19) that the univalence axiom can be simplified to the following special cases:

   * $unit : A = \sum_{a:A} 1$
   * $flip : (\sum_{a:A} \sum_{b:B} C(a,b)) = (\sum_{b:B} \sum_{a:A} C(a,b))$
   * $contract: IsContr(A) \to (A=1)$
   * $unit_\beta : coe(unit(a)) = (a,\star)$
   * $flip_\beta : coe(flip(a,b,c)) = (b,a,c)$.

The proof constructs $ua(f): A=B$ (for $f:A\simeq B$) as the composite
$$ A \overset{unit}{=} \sum_{a:A} 1 \overset{contract}{=} \sum_{a:A} \sum_{b:B} f a=b \overset{flip}{=} \sum_{b:B} \sum_{a:A} f a = b \overset{contract}{=} \sum_{b:B} 1 \overset{unit}{=} B $$
and uses $unit_\beta$ and $flip_\beta$ to compute that $coe(ua(f))(a) = f(a)$, hence by function extensionality $coe(ua(f)) = f$.

In the absence of [[function extensionality]], this set of axioms is [conjectured to be weaker than univalence](#WeakerVariants).
In addition, unlike the definitions above, this definition of univalence cannot be generalized to [[reflexive graphs]]. 

### Resizing the identity types

Due to the usual [[univalence axiom]], we know that it is consistent to [[resize]] the [[identity types]] of a universe $U$ to be $U$-[[small type|small]]. 

Resizing the identity types allows for one more version of univalence, where we replace the [[equivalence of types]] between the identity type $A =_U B$ and the type of equivalences of the universe $A \simeq B$ in the univalence axioms with the [[identity type]] of the universe $U$, resulting in the statement that for all small types $A:U$ and $B:U$, there is an [[identification]] 
$$\mathrm{ua}(A, B):(T(A) =_U T(B)) =_{U} (T(A) \simeq T(B))$$

This implies the usual version of univalence either through [[identification elimination]], [[transport]], and [[action on identifications]] for the [[identity type]]. On the other hand, the usual version of univalence implies this version of univalence by repeated applications of univalence. 

## Stricter variants of univalence

There are a few variants of univalence that are stricter than the usual axiom of univalence in that they use [[judgmental equalities]] and thus have to be expressed as (possibly multiple) [[inference rules]] instead of an [[axiom]].

### Using definitional isomorphism

There is a variant of univalence called **definitional univalence** or **judgmental univalence**, which says that for $x:A$ and $y:A$, the function $\mathrm{idtofam}(x, y)$  inductively defined in the previous section is a [[definitional isomorphism]] instead of an [[equivalence of types]]. 

Unlike the case for the usual typal variant of univalence, where one can use an element of an [[equivalence type]], we cannot use definitional isomorphisms as elements of [[definitional isomorphism types]] to express definitional univalence, because the large recursion principle of the [[interval type]] together with [[definitional isomorphism types]] implies [[equality reflection]], which contradicts univalence. 

[[Mike Shulman]]\'s model of [[higher observational type theory]] uses the type of $U$-small one-to-one correspondences for $R$ in definitional univalence. 

### Using judgmental equality of types

There is another variant of univalence where we replace the [[equivalence of types]] between the identity type $A =_U B$ and the type of equivalences of the universe $A \simeq B$ in the univalence axioms with [[judgmental equality of types]], resulting in the statement that for all small types $A:U$ and $B:U$, one could judge that $(A =_U B) \equiv (A \simeq B) \; \mathrm{type}$. This implies the usual version of univalence through the structural rules for [[judgmental equality]]. The interpretation of such a univalent universe is that [[identifications]] of universes *are* [[equivalences of types]]. 

Such univalent Tarski universes $(U, T)$ can be defined directly using inference rules instead of a judgmental equality, which say that identities $p:A =_U B$ are [[equivalences of types]] $A$ and $B$. Namely, given [[function types]] and the [[isEquiv]] type family, one could add rules to the type theory which says that $A =_U B$ behaves as an [[equivalence type]]:

Introduction rules:
$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma, x:T[A/X] \vdash f:T[B/X] \quad \Gamma \vdash y:\mathrm{isEquiv}(f)}{\Gamma \vdash \mathrm{equiv}(f, y):A =_U B}$$

Elimination rules:
$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma, x:T[A/X] \vdash f:T[B/X] \quad \Gamma, z:A =_U B \vdash C \; \mathrm{type} \quad \Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash c:C[\mathrm{equiv}(f, y)/z]}{\Gamma, z:A =_U B \vdash \mathrm{ind}_{A =_U B}^C(c):C}$$

Computation rules:
$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma, x:T[A/X] \vdash f:T[B/X] \quad \Gamma, z:A =_U B \vdash C \; \mathrm{type} \quad \Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash c:C[\mathrm{equiv}(f, y)/z]}{\Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash \beta_{A =_U B}^C(c):\mathrm{ind}_{A =_U B}^C(c)[\mathrm{equiv}(f, y)/z] =_{C[\mathrm{equiv}(f, y)/z]} c}$$

Uniqueness rules:
$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma, x:T[A/X] \vdash f:T[B/X] \quad \Gamma, z:A =_U B \vdash C \; \mathrm{type} \quad \Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash c:C[\mathrm{equiv}(f, y)/z] \quad \Gamma, z:A =_U B \vdash u:C \quad \Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash i_\mathrm{in}(u):u[\mathrm{equiv}(f, y)/z] =_{C[\mathrm{in}(x, y)/z]} c}{\Gamma, e:A =_U B \vdash \eta_{A =_U B}^C(c):u[e/z] =_{C[e/z]} \mathrm{ind}_{A =_U B}^C(c)[e/z]}$$

## Weaker variants of univalence
 {#WeakerVariants}

Van den Berg ([Van den Berg 20, Definition 2.13](#VanDenBerg20)) gives a definition of univalent fibration in a [[category with path objects|path category]] which can be translated into type theory as follows:

$$A:U, B:U \vdash \mathrm{ua}(A, B): (A \simeq B) \to (A =_U B)$$
$$A:U, B:U, e : (A\simeq B), a: A \vdash G(A,B,e,a) : \mathrm{coe}(\mathrm{ua}(A,B))(a) =_{B} e(a)$$

Notably, this variant of the univalence axiom can be unfolded and presented as a pair of inference rules in a type theory with only [[identity types]], [[dependent sum types]], and $U$.
All uses of [[dependent product types]] can be replaced with hypothetical judgements.

Assuming [[dependent product types]] with [[function extensionality]], this is equivalent to the univalence axiom ([Licata 16](#Licata16)).
If [[function extensionality]] is not explicitly assumed, it is an open question whether it is equivalent to the univalence axiom (or equivalently, [that it implies function extensionality](#UnivalenceFunctionExtensionality)).
This is observed in Remark 4.6 of [Swan 24](#Swan24).
It is, however, equivalent to [Orton and Pitts' set of axioms](#Decomposition).

## In categorical semantics
 {#InCategoricalSemantics}

Let $\mathcal{C}$ be a [[locally cartesian closed model category]] in which all objects are cofibrant. 

By the [[categorical semantics]] of [[homotopy type theory]], a [[dependent type]]

$$
  b : B \vdash E(b) \; \mathrm{type}
$$

corresponds to a [[morphism]] $E \to B$ in $\mathcal{C}$ that is a [[fibration]] between fibrant objects.

Then the [[dependent type|dependent]] [[function type]]

$$
  b_1, b_2 : B \vdash ( E(b_1) \to E(b_2)) \; \mathrm{type}
$$

is interpreted as the [[internal hom]] $[-,-]_{\mathcal{C}/_{B \times B}}$ in the [[slice category]] $\mathcal{C}/_{B \times B}$ after extending $E$ to the [[context]] $B \times B$ by pulling back along the two projections $p_1, p_2 : B \times B \to B$, respectively. Hence this is interpreted as

$$
  [p_1^* E \, , \, p_2^* E]_{\mathcal{C}/_{B \times B}}
  \simeq
  [E \times B \, , \, B \times E]_{\mathcal{C}/_{B \times B}}
  \in 
  \mathcal{C}/_{B \times B}
  \,.
$$

Consider then the [[diagonal]] morphism $\Delta_B : B \to B \times B$  in $\mathcal{C}$ as an object of $\mathcal{C}/_{B \times B}$.  We would like to define a morphism 
$$ q \colon \Delta_B \to [E \times B , B \times E]_{\mathcal{C}/_{B \times B}} \,.$$
in $\mathcal{C}/_{B \times B}$.  By the defining ([[product]] $\dashv$ [[internal hom]])-[[adjunction]], it suffices to define a morphism
$$ \Delta_B \times_{\mathcal{C}/_{B \times B}} E \times B \to B \times E $$
in $\mathcal{C}/_{B \times B}$.  But now by the 
[[universal property]] of [[pullback]], it suffices to define just in $\mathcal{C}_{/B}$ a morphism
$$ \Delta_B \times_{\mathcal{C}/_{B \times B}} E \times B \to \Delta_B \times_{\mathcal{C}/_{B \times B}} B \times E\,. $$  
And since the composite pullback along either composite
$$ B \xrightarrow{\Delta_B} B\times B \xrightarrow{\pi_1} B$$
$$ B \xrightarrow{\Delta_B} B\times B \xrightarrow{\pi_2} B$$
is the identity, both $\Delta_B \times_{\mathcal{C}/_{B \times B}} E \times B$ and $\Delta_B \times_{\mathcal{C}/_{B \times B}} B \times E$ are isomorphic to $E$; thus here we can take the [[identity]] morphism.

Now, using the [[path object]] factorization in $\mathcal{C}$

$$
  \array{
     B &&\stackrel{\simeq}{\hookrightarrow}&& B^I
     \\
     & {}_{\mathllap{\Delta_B}}\searrow
     && \swarrow_{\mathrlap{}}
     \\
     && B \times B
  }
$$

by an acyclic cofibration followed by a fibration, we obtain a fibrant replacement of $\Delta_B$ in the [[slice model category]] $\mathcal{C}_{B \times B}$.

Since also $[E \times B, B \times E]_{\mathcal{C}/_{B \times B}}$ is fibrant by the axioms on the [[locally cartesian closed model category]] $\mathcal{C}$, we have a 
lift $\hat q$ in the [[diagram]] in $\mathcal{C}/_{B \times B}$

$$
  \array{
    B &\stackrel{q}{\to}& [E \times B, B \times E]_{\mathcal{C}/_{B \times B}}
   \\
   \downarrow &{}^{\mathllap{\hat q}}\nearrow& \downarrow
   \\
   B^I &\to& B \times B = *_{\mathcal{C}/_{B \times B}}
  } 
  \,.
$$

This lift is the interpretation of the [[identity type|path induction]] that deduces a map on all paths $\gamma \in B^I$ from one on just the identity paths $id_b \in B \hookrightarrow B^I$.


Finally, let $Eq(E) \hookrightarrow [E \times B , B \times E]_{\mathcal{C}/_{B \times B}}$ be the [[subobject]]  on the weak equivalences (...), and observe that $q$ and $\hat q$ factor through this to give a morphism

$$
  \hat q : B^I \to Eq(E)
  \,.
$$

The fibration $E \to B$ is **univalent** in $\mathcal{C}$ if this morphism is a weak equivalence.  By the [[2-out-of-3 property]], of course, it is equivalent to ask that $q\colon B\to Eq(E)$ be a weak equivalence.

(...)

### In simplicial sets
 {#InSimplicialSets}

We specialize the [general discussion](#InCategoricalSemantics) above to the realization in $\mathcal{C} = $ [[sSet]], equipped with the 
standard [[model structure on simplicial sets]].

For $E \to B$ any fibration ([[Kan fibration]])
between fibrant objects ([[Kan complexes]]),
consider first the simplicial set

$$
  [E \times B , B \times E]_{B \times B}
  \in 
  sSet/_{B \times B} 
$$

defined as the [[internal hom]] in the [[slice category]] $sSet/_{B \times B}$.

Notice that the vertices of this simplicial set over 
a fixed pair $(b_1, b_2) : * \to B \times B$ of vertices in $B$ form the set of morphisms $E_{b_1} \to E_{b_2}$ between the [[fibers]] in $sSet$.

This is because -- by the defining property of the [[internal hom]] in the [[slice category|slice]] and using that [[products]] in $sSet/_{B \times B}$ are [[pullbacks]] in $sSet$ -- the horizontal morphisms of simplcial sets in

$$
  \array{
    * &&\to&& [E \times B, B \times E]_{B \times B}
    \\
    & {}_{\mathllap{(b_1,b_2)}}\searrow && \swarrow
    \\
    && B \times B
  }
$$

correspond bijectively to the horizontal morphisms in

$$
  \array{
    E_{b_1} \times \{b_2\} &&\to&& \{b_1\} \times E_{b_2}
    \\
    & \searrow && \swarrow
    \\
    && B \times B
  }
$$

in $sSet$, which are precisely morphisms $E_{b_1} \to E_{b_2}$.

Let then 

$$
  Eq(E) \hookrightarrow [E \times B, B \times E]_{B \times B}
  \in sSet/_{B \times B}
$$

be the full sub-simplicial set on those vertices that correspond to 
[[weak equivalences]]
(([[weak homotopy equivalence|weak]]) [[homotopy equivalences]]).

By a similar consideration, one sees that the [[diagonal]] morphism
$\Delta_B : B \to B \times B$ in $sSet$, regarded as an object  $B \in sSet/_{B \times B}$, comes with a canonical morphism

$$
  B \to Eq(E)
  \,.
$$

The fibration $E \to B$ is univalent, precisely when this morphism is a weak equivalence.

This appears originally as [Voevodsky, def. 3.4](#UnivalentFoundationsProject)

### In simplicial presheaves
  {#InSimplicialPresheaves}

(...)

See ([Shulman 15](#Shulman12), [UF 13](UF13))

(...)

## Properties

### Relation to function extensionality
  {#UnivalenceFunctionExtensionality}

The univalence axiom implies [[function extensionality]].

A commented version of a formal proof of this fact can be found in ([Bauer-Lumsdaine](#BauerLumsdaine)).

### Univalence and axiom K

In this section we assume that the universe is a Tarski universe. [[Axiom K]] states that for all $A:U$ the type $T(A)$ is a set. This means the type reflection of the internal equivalences $T(A \simeq_U B)$ is an [[h-set]], and the univalence axiom then implies that $U$ is an [[h-groupoid]]. 

It is frequently stated that the univalence axiom and axiom K are inconsistent with each other. However, this is only true if the Tarski universe $U$ has internal univalent Tarski universes $V:U$ where the type $T(V)$ has terms $A:T(V)$ such that $T_V(A)$ is an [[h-set]] which is not an [[h-proposition]], such as the [[booleans type]]. As a result, $T(V)$ can be proven to not be a set, causing axiom K for $U$ to be inconsistent with the existence of $V:U$ and univalence. 

### Univalence and excluded middle
 {#UnivalenceLEM}
 {#UnivalenceExcludedMiddle}

The [[univalence axiom]] is consistent with [[excluded middle]]. This is because the principle of excluded middle as traditionally defined in mathematics is about [[propositions]] or [[(-1)-truncated]] types. 
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{lem}_A:\mathrm{isProp}(A) \to (A \vee (A \to \emptyset))}$$
Dependent type theory with excluded middle and universes satisfying the univalence axiom has semantics in [[boolean topos|boolean]] [[(infinity,1)-topos|$(\infty, 1)$-toposes]].
A short proof of the excluded middle for the [simplicial model](#InSimplicialSets) can be found in [Kapulkin--Lumsdaine 20](#KapulkinLumsdaine20).

However, there is a global choice axiom which is inconsistent with univalence:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{gc}_A:A + (A \to \emptyset)}$$
This is sometimes called "excluded middle" in the [[propositions as types]] interpretation of type theory, where the principle of excluded middle is reinterpreted so that types are used instead of [[mere propositions]]. But this choice principle is a much stronger axiom than excluded middle, being of comparable strength to a [[choice operator]] and implying that every type is an [[h-set]]; hence inconsistent with the univalence axiom. 

### Canonicity and homotopy canonicity
 {#Canonicity}

If we extend [[Martin-Löf type theory]] with an axiom stating that a universe $U$ is univalent, we get a type theory which does not satisfy [[canonicity]]: there exist [[terms]] $\cdot \vdash N : \mathbb{N}$ in the [[empty context]] which are not [[judgmentally equal]] to any [[numeral]].
For example, if $\cdot \vdash e : \mathbb{N} \simeq \mathbb{N}$ is some [[equivalence type|equivalence]] (such as the identity equivalence), then $coe(ua(e))(0) : \mathbb{N}$ is such a term: although there is a [[typal equality]] $coe(ua(e))(0) = e(0)$, there is no [[judgmental equality]].
This can be shown using [[normalization]] for MLTT to compare the [[normal forms]] of $coe(ua(e))(0)$ and $e(0)$, treating [[judgments]] of the extended theory as judgments of MLTT with an extra hypothesis in the [[context]] stating that $U$ is univalent.

Despite this, it is possible to extend [[Martin-Löf type theory]] with univalent universes _further_ to create a theory that does enjoy [[canonicity]].
[[cubical type theories|Cubical type theories]] are examples of such theories which can support an infinite [[universe hierarchy|hierarchy]] of univalent universes; see [[cubical type theory]] for more details.
An earlier canonicity result for a type theory with one univalent universe where every type is an [[h-groupoid]] was proven by Harper and Licata ([Harper and Licata 12](#HarperLicata)).

A separate question is whether [[Martin-Löf type theory]] extended with one or more univalent universes satisfies the weaker [[homotopy canonicity]] property.
In 2019, [[Christian Sattler]] and [[Krzysztof Kapulkin]] announced a proof of this result; the proof has been described in talks ([Sattler 19](#Sattler19)) but has not appeared publicly.
[[Rafaël Bocquet]] gives a second proof of homotopy canonicity in a preprint ([Bocquet 23](#Bocquet23)).
Earlier homotopy canonicity results for truncated versions of univalent type theory were shown by Shulman ([Shulman 15, Section 13](#Shulman12)).
[Shulman 15, Theorem 13.7](#Shulman12) shows that [[Martin-Löf type theory]] with

* one univalent universe $U_0$,
* a "strong homotopy" [[natural number type]] (not contained in $U_0$),
* [[function extensionality]], and
* an axiom asserting that every type is an [[h-set]]

has homotopy canonicity.
[Shulman 15, Theorem 13.12](#Shulman12) shows that [[Martin-Löf type theory]] with

* two nested univalent universes $U_0 : U_1$,
* a "strong homotopy" [[natural number type]] contained in $U_1$,
* [[function extensionality]],
* an axiom asserting that every type is a [[h-groupoid]]

has homotopy canonicity.
The proofs use [[Artin gluing]] of a suitable [[type-theoretic model category|type-theoretic fibration category]] with the [[categories]] [[Set]] and [[Grpd]], respectively, effectively inducing canonicity from these categories.
By ([Shulman 15, remark 13.13](#Shulman12)), for this construction to generalize to a univalent type theory without a global [[truncation]] axiom, one seems to need a sufficiently strict [[global sections]] functor with values in some model for [[infinity-groupoids]].
The proofs in [Sattler 19](#Sattler19) and [Bocquet 23](#Bocquet23) address this problem in different ways.

### A univalent universe inside a non-univalent universe

In a post to the [Homotopy Type Theory Google Group](https://groups.google.com/forum/#!forum/homotopytypetheory), Peter LeFanu Lumsdaine [wrote](https://groups.google.com/d/msg/homotopytypetheory/3wp32xV7OX0/2HfAnBt44XoJ):

> Let $(x_0:X)$ be any [[pointed type]], and $(\mathcal{U}, El)$ be a universe (with rules as I set out a couple of emails ago). Then $X \times \mathcal{U}$ is again a universe, admitting all the same constructors as $\mathcal{U}$: take

> $El(x,A) = El(A)$,  
> $(x,A) +_\mathcal{U} (y,B) = (x_0, A +_\mathcal{U} B)$,

> and so on; that is, constructor operations on $(X \times \mathcal{U})$ are constantly $x_0$ on the first component, and mirror those of $\mathcal{U}$ on the second component.

> Now if $\mathcal{U}$ is univalent, and $X$ has non-trivial $\pi_0$ (e.g. $X=S^1$), then $\mathcal{U} \rightarrow (X \times \mathcal{U}$) gives a univalent universe sitting inside a non-univalent one (again, with the rules as I set out earlier).

> Slightly more generally, given any cumulative pair of universes $\mathcal{U}_0 \rightarrow \mathcal{U}_1$, we can consider $\mathcal{U}_0 \rightarrow A \times \mathcal{U}_1$; this shows we can additionally have the smaller universe represented by an element of the larger one.

[[Mike Shulman]] [added](https://groups.google.com/d/msg/homotopytypetheory/3wp32xV7OX0/kIapR0lo1UEJ):

> [N]ot only is $X \times \mathcal{U}$ not univalent, it's not even "univalent on the image of $\mathcal{U}$", as was the case for the example in the groupoid model that I mentioned.

## Univalence axiom without universes

In [[dependent type theory with type variables]], presented using a single type judgment and with [[identity type#IdentityTypesBetweenTypes|identity types between types]], it is possible to state the univalence axiom without any [[type universes]]. 

The **univalence axiom** states that the function 

$$\mathrm{idtoequiv}(A, B):(A = B) \to (A \simeq B)$$

inductively defined by 

$$\mathrm{idtoequiv}(A, A, \mathrm{refl}(A)) \coloneqq \mathrm{id}_A$$

is an [[equivalence of types]] for all types $A$ and $B$, 

$$\mathrm{isEquiv}(\mathrm{idtoequiv}(A, B))$$

where $\mathrm{id}_A \coloneqq \lambda x:A.x$ is the [[identity function]] on the type $A$. This is given by the following axiom:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma, A \; \mathrm{type}, B \; \mathrm{type} \vdash \mathrm{ua}(A, B):\mathrm{isEquiv}(\lambda p:A = B.\mathrm{idtoequiv}(A, B, p))}$$

In [[impredicative polymorphism]], this is also given by the following axiom:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{ua}:\Pi A.\Pi B.\mathrm{isEquiv}(\lambda p:A = B.\mathrm{idtoequiv}(A, B, p))}$$

Unlike the other presentation of dependent type theory in terms of universes, in this presentation of dependent type theory with a type judgment and type variables, it *is consistent* to assume both the [[univalence axiom]] and an [[axiom of set truncation]] like [[UIP]] or [[axiom K]], since here there is no universe, provided one doesn’t have any higher types, such as the circle type. 

There is one other version of univalence, where we replace the [[equivalence of types]] between the identity type $A = B$ and the type of equivalences of the universe $A \simeq B$ in the univalence axioms with the [[identity type]], resulting in the statement that for all small types $A$ and $B$, there is an [[identification]] $\mathrm{ua}(A, B):(A = B) = (A \simeq B)$.

This implies the usual version of univalence either through [[identification elimination]], [[transport]], and [[action on identifications]] for the [[identity type]]. 

## Related concepts

* [[resizing axiom]]

* [[univalent foundations]]

* [[univalent type theory]]

* [[extensionality]]

  * Univalence is closely related to the "completeness" condition in the theory of [[Segal spaces]]/[[semi-Segal spaces]]. See _[[complete Segal space]]_/_[[complete semi-Segal space]]_.

  * [[propositional extensionality]]

* contrary to univalence is the [[axiom UIP]]

* [[directed univalence axiom]]

* [[axiom of relativity]]

* [[identity type#IdentityTypesBetweenTypes|identity type between types]]

## References
 {#References}

> For more references see also at _[[homotopy type theory]]_.

### History

Arguably, the earliest occurrence of a version of the univalence axiom is due -- under the name "universe extensionality" -- to:

* {#HofmannStreicher98} [[Martin Hofmann]], [[Thomas Streicher]], Section 5.4 of:  _The groupoid interpretation of type theory_, in: [[Giovanni Sambin]] et al. (eds.), *Twenty-five years of constructive type theory*, Proceedings of a congress, Venice, Italy, October 19-21, 1995. Oxford: Clarendon Press. Oxf. Logic Guides. **36** (1998) 83-111   &lbrack;[ISBN:9780198501275](https://global.oup.com/academic/product/twenty-five-years-of-constructive-type-theory-9780198501275), [ps](http://www.mathematik.tu-darmstadt.de/~streicher/venedig.ps.gz), [[HofmannStreicherGroupoidInterpretation.pdf:file]]&rbrack;

Strictly speaking, univalence for *propositions* has a much longer pedigree, this that can and does hold even in [[set-level foundations]], but this is the earliest version of univalence that goes beyond what is possible there.  However, their universe extensionality axiom is stated only for [[h-sets]], and would be incorrect if naively generalized to higher types.  The correct statement that works for higher types requires a better definition of [[equivalences in homotopy type theory]] (see [there](equivalence+in+type+theory#TheIssueWithQuasiInverses) for details), which Voevodsky was the first to give.

For comments on the early history see also:

* {#Altenkirch21} [[Thorsten Altenkirch]], *Martin Hofmann’s contributions to type theory: Groupoids and univalence*, Mathematical Structures in Computer Science **31** 9 (2021) 953-957 &lbrack;[doi:10.1017/S0960129520000316](https://doi.org/10.1017/S0960129520000316)&rbrack;

It is this notion of [[equivalence in homotopy type theory]] which was fixed in 

* {#Voevodsky10} [[Vladimir Voevodsky]], p. 8, 10-11 of: *Univalent Foundations Project* (2010) &lbrack;[pdf](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/univalent_foundations_project.pdf), [[Voevodsky-UFP2010.pdf:file]]&rbrack;

ever since the univalence axiom is widely attributed to Voevodsky. Earlier documentation of the univalence axiom in modern form is hard to come by:

The first technical understanding of (the semantics of) univalence in simplicial sets seems to be due to:

* {#Bousfield06} [[Aldridge Bousfield]], [email to VV from 01 May 2006 10:10:30 CDT](https://groups.google.com/g/homotopytypetheory/c/K_4bAZEDRvE/m/YSQz-jJ_AAAJ) $[$[[BousfieldOnUnivalence.jpg:file]]$]$

(which 6 years later came to be written up as [Kapulkin, Lumsdaine & Voevodsky12](#KapulkinLumsdaineVoevodsky12) and another 10 years later was published as [Kapulkin & Lumsdaine 2021](#KapulkinLumsdaine21)).

The first mentioning by Voevodsky of the term "univalence" by email is 3.5 years later, from [Dec. 30 2009](https://groups.google.com/g/homotopytypetheory/c/K_4bAZEDRvE/m/3N2xxxfSAAAJ) (according to [Grayson, Oct. 2017](https://groups.google.com/g/homotopytypetheory/c/K_4bAZEDRvE/m/-Lp5dxTTAAAJ)).

The earliest recorded statement of the univalence axiom by Voevodsky's hand date may be [Voevodsky (2010), p. 11](#Voevodsky10)

see also:

* [[Vladimir Voevodsky]], *The equivalence axiom and univalent models of type theory* (Talk at CMU on February 4, 2010) ([arXiv:1402.5556](https://arxiv.org/abs/1402.5556))

* {#Voevodsky14} [[Vladimir Voevodsky]], _Univalent foundations – new type-theoretic foundations of mathematics_, talk at IHP 2014 ([pdf](https://www.math.ias.edu/vladimir/sites/math.ias.edu.vladimir/files/2014_04_22_slides.pdf))

Later in:

* [[Vladimir Voevodsky]],  *[The Origins and Motivations of Univalent Foundations](https://www.ias.edu/ideas/2014/voevodsky-origins)*, IAS Institute Letter Summer 2014

appears the claim that:

> have been working on the ideas that led to the discovery of univalent models since 2005 and gave the first public presentation on this subject at Ludwig-Maximilians-Universität München in November 2009.

A comprehensive discussion finally appears in the textbook:

* [[UF-IAS-2012|Univalent Foundations Project]], p. 4 & Sec. 2.10 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013)  &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

Voevodsky's ([Bousfield's](#Bousfield06)) original idea for the [[universal Kan fibration]] as a model for a univalent universe in [[simplicial sets]]/[[infinity-groupoids|$\infty$-groupoids]] was eventually published as:

* {#KapulkinLumsdaine21} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], *The Simplicial Model of Univalent Foundations (after Voevodsky)*, Journal of the European Mathematical Society **23** (2021) 2071–2126  $[$[arXiv:1211.2851](https://arxiv.org/abs/1211.2851), [doi:10.4171/jems/1050](https://doi.org/10.4171/jems/1050)$]$

### Exposition and survey

* [[Peter Aczel]], *On Voevodsky’s Univalence Axiom*, talk at Third European Set Theory Conference (2011) &lbrack;[pdf](http://www.cs.man.ac.uk/~petera/Recent-Slides/Edinburgh-2011-slides_pap.pdf), [[Aczel-Univalence.pdf:file]]&rbrack;

  > (in view of the [[structure identity principle]])

* [[Mike Shulman]], _Homotopy type theory, IV_ &lbrack;[blog post](http://golem.ph.utexas.edu/category/2011/04/homotopy_type_theory_iv.html)&rbrack;

Additional definition of univalent universes appeared in section 17.1 of 

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press &lbrack;[arXiv:2212.11082](https://arxiv.org/abs/2212.11082)&rbrack;

### Variants

A superficially weaker but equivalent statement of univalence:

* {#Licata16} [[Dan Licata]], *weak univalence with "beta" implies full univalence* &lbrack;[web](https://groups.google.com/forum/#!msg/homotopytypetheory/j2KBIvDw53s/YTDK4D0NFQAJ)&rbrack;


A reduction of the univalence axiom to special cases:

* {#OrtonPittsTYPES17} [[Ian Orton]], [[Andrew M. Pitts]], _Decomposing the Univalence Axiom_, in 23rd International Conference on Types for Proofs and Programs (TYPES 2017), Leibniz International Proceedings in Informatics (LIPIcs) **104** (2019) 6:1--6:19 &lbrack;[arXiv:1712.04890](https://arxiv.org/abs/1712.04890), [doi:10.4230/LIPIcs.TYPES.2017.6](https://doi.org/10.4230/LIPIcs.TYPES.2017.6)&rbrack;

On a possibly-weaker variant of univalence:

* {#VanDenBerg20} [[Benno van den Berg]], Section 2.3 in _Univalent polymorphism_, Annals of Pure and Applied Logic **171** (2020) 102793 &lbrack;[arXiv:1803.10113](https://arxiv.org/abs/1803.10113), [doi:10.1016/j.apal.2020.102793](http://doi.org/10.1016/j.apal.2020.102793)&rbrack;

* {#Swan24} [[Andrew Swan]], Section 4 in _A categorical formulation of Kraus' paradox_ (2024) &lbrack;[arXiv:2403.17961](https://arxiv.org/abs/2403.17961)&rbrack;

Some details regarding the univalence axiom for [[weakly Tarski universes]] appeared on MathOverflow in:

* [[Madeleine Birchfield]], [[Valery Isaev]], *Univalence for weakly Tarski universes*, MathOverflow, &lbrack;[web](https://mathoverflow.net/q/431723)&rbrack;

Some discussion about the univalence axiom in [[dependent type theory with type variables]] occurs in:

* {#CTZulip} *Dependent Type Theory vs Polymorphic Type Theory*, Category Theory Zulip &lbrack;[web](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Dependent.20Type.20Theory.20vs.20Polymorphic.20Type.20Theory)&rbrack;

### Semantics

An accessible account of Voevodsky's proof (following [Bousfield 06](#Bousfield06)) that the universal [[Kan fibration]] in [[simplicial sets]] is univalent:

* {#KapulkinLumsdaineVoevodsky12} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], [[Vladimir Voevodsky]], _Univalence in simplicial sets_ &lbrack;[arXiv:1203.2553](http://arxiv.org/abs/1203.2553)&rbrack;

A quick elegant proof of the [[object classifier]]/universal [[associated infinity-bundle]] in simplicial sets/$\infty$-groupoids is in 

* {#Moerdijk} [[Ieke Moerdijk]] (notes by Chris Kapulkin), _Fiber bundles and univalence_ &lbrack;[pdf](http://www-home.math.uwo.ca/~kkapulki/notes/fiber_bundles_univalence.pdf)&rbrack;

A study of the [[semantics|semantic]] side of univalence in [[(infinity,1)-toposes]], as well as further cases of [[locally cartesian closed (infinity,1)-categories]] is in

* {#GepnerKock12} [[David Gepner]], [[Joachim Kock]], _Univalence in locally cartesian closed infinity-categories_, Forum Mathematicum **29** 3 (2016) 617--652 &lbrack;[arXiv:1208.1749](http://arxiv.org/abs/1208.1749), [doi:10.1515/forum-2015-0228](https://doi.org/10.1515/forum-2015-0228)&rbrack;

This does not yet show that the univalence axiom in its usual form holds in the internal type theory of [[(infinity,1)-toposes]], however, due to the lack of a (known) sufficiently strict model for the object classifier.  (But it works with [[Tarski universes]], see there and [[type universes]]). Constructions of such a model in some very special cases are in [Shulman12](#Shulman12) below, and also in

* [[Michael Shulman]], _The univalence axiom for elegant Reedy presheaves_, Homology, Homotopy and Applications **17** 2 (2015) 81--106 &lbrack;[arXiv:1307.6248](http://arxiv.org/abs/1203.3253), [doi:10.4310/HHA.2015.v17.n2.a6](https://doi.org/10.4310/HHA.2015.v17.n2.a6)&rbrack;

* {#Cisinski14} [[Denis-Charles Cisinski]], _Univalent universes for elegant models of homotopy types_ &lbrack;[arXiv:1406.0058](http://arxiv.org/abs/1406.0058)&rbrack;

Finally, full proof that all [[∞-stack]] [[(∞,1)-topos]] have [[presentable (∞,1)-category|presentations]] by [[model categories]] which interpret (provide [[categorical semantics]]) for [[homotopy type theory]] with [[univalence|univalent]] [[type universes]]:

* {#Shulman19} [[Michael Shulman]], _All $(\infty,1)$-toposes have strict univalent universes_ &lbrack;[arXiv:1904.07004](https://arxiv.org/abs/1904.07004))&rbrack;

On the issue of strict pullback of the univalent universe see

* Univalent Foundations Mailing List, _[Quotients](https://groups.google.com/d/msg/univalent-foundations/Glo7NgNvhJA/4j9SewiFvQ0J)_, March 2013
  {#UF13}

On an interpretation of a univalent universe at the strength of finite order arithmetic:

* [[Colin McLarty]], _A univalent universe in finite order arithmetic_ &lbrack;[arXiv:1412.6714](http://arxiv.org/abs/1412.6714)&rbrack;

Coexistence of univalence with the [[excluded middle]]:

* {#KapulkinLumsdaine20} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], _The Law of Excluded Middle in the Simplicial Model of Type Theory_, Theory and Applications of Categories **35** 40 (2020) 1546--1548 &lbrack;[arXiv:2006.13694](https://arxiv.org/abs/2006.13694), [doi:10.70930/tac/ykx24t1x](https://doi.org/10.70930/tac/ykx24t1x)&rbrack;

### Proof assistants

Implementation of univalence in [[proof assistants]]:

in [[Agda]]:

* [[Martín Escardó]], *[Voevodsky’s univalence axiom](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html#univalence)*, §3.11 in: *Introduction to Univalent Foundations of Mathematics with Agda* &lbrack;[arXiv:1911.00580](https://arxiv.org/abs/1911.00580),  [webpage](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html)&rbrack;

[[cubical Agda]]:

* [[1lab]], *[Univalence](https://1lab.dev/1Lab.Univalence.html)*

in [[Coq]]:

* _[HoTT/HoTT theories/Types/Universe.v](https://github.com/HoTT/HoTT/blob/master/theories/Types/Universe.v)_

* _[HoTT/HoTT theories/UnivalenceAxiom.v](https://github.com/HoTT/HoTT/blob/master/theories/UnivalenceAxiom.v)_


A guided walk through the formal proof that univalence implies [[functional extensionality]] is at

* {#BauerLumsdaine} [[Andrej Bauer]], [[Peter LeFanu Lumsdaine]], _[[Oberwolfach HoTT-Coq tutorial]]_

Application of univalence to [[proof]] transfer:

* [[Cyril Cohen]], Enzo Crance, [[Assia Mahboubi]], *Trocq: Proof Transfer for Free, With or Without Univalence*, in: *Programming Languages and Systems. ESOP 2024*, Lecture Notes in Computer Science **14576**, Springer (2024) &lbrack;[arXiv:2310.14022](https://arxiv.org/abs/2310.14022), [doi:10.1007/978-3-031-57262-3_10](https://doi.org/10.1007/978-3-031-57262-3_10)&rbrack;

### Canonicity and computational interpretations

A discussion of univalence in categories of [[diagrams]] over an [[inverse category]] with values in a category for which univalence is already established is discussed in 

* [[Michael Shulman]], _Univalence for inverse diagrams and homotopy canonicity_, Mathematical Structures in Computer Science **25** (2015) 1203--1277 &lbrack;[arXiv:1203.3253](http://arxiv.org/abs/1203.3253), [doi:10.1017/S0960129514000565](https://doi.org/10.1017/S0960129514000565)&rbrack;

This discusses [[homotopy canonicity]] of univalence in its section 13. 
A proof of [[homotopy canonicity]] was presented in

* {#Sattler19} [[Christian Sattler]], _Homotopy Canonicity_, Talk at HoTT-UF (2019) &lbrack;[abstract](https://eutypes.cs.ru.nl/pmwiki/uploads/Main/books-of-abstracts-TYPES2019.pdf), [program](https://sites.google.com/view/hott-uf-2019/speakers)&rbrack;

Another proof of [[homotopy]] canonicity is the subject of

* {#Bocquet23} [[Rafaël Bocquet]], _Strict Rezk completions of models of HoTT and homotopy canonicity_ (2023) &lbrack;[arXiv:2311.05849](https://arxiv.org/abs/2311.05849)&rbrack;

Another approach to showing canonicity is (via [[cubical sets]]) in 

* [[Marc Bezem]], [[Thierry Coquand]], [[Simon Huber]], _A model of type theory in cubical sets_, in 19th International Conference on Types for Proofs and Programs (TYPES 2013), Leibniz International Proceedings in Informatics (LIPIcs) **26** (2014) 107--128 &lbrack;[doi:10.4230/LIPIcs.TYPES.2013.107](https://doi.org/10.4230/LIPIcs.TYPES.2013.107), [pdf](http://www.cse.chalmers.se/~coquand/mod1.pdf), [Haskell code](https://github.com/simhu/cubical), [discussion](https://groups.google.com/forum/#!topic/homotopytypetheory/GmXKEArD3HY)&rbrack;
  {#CoquandHuber13}

* {#BezemCoquandHuber17} [[Marc Bezem]], [[Thierry Coquand]], [[Simon Huber]], _The univalence axiom in cubical sets_, Journal of Automated Reasoning **63** (2019) 159--171 &lbrack;[arXiv:1710.10941](https://arxiv.org/abs/1710.10941), [doi:10.1007/s10817-018-9472-6](https://doi.org/10.1007/s10817-018-9472-6)&rbrack;

The computational interpretation of univalence / [[canonicity]] is discussed in 

* [[Dan Licata]], [[Robert Harper]], _Computing with Univalence_  (2012) &lbrack;[pdf](http://4wft.fmf.uni-lj.si/wp-content/uploads/2012/04/Licata.pdf)&rbrack;

* [[Robert Harper]], [[Daniel Licata]], _Canonicity for 2-dimensional type theory_, in Proceedings of the 39th annual ACM SIGPLAN-SIGACT symposium on Principles of Programming Languages (POPL) (2012) 337--348 &lbrack;[doi:10.1145/2103656.2103697](https://doi.org/10.1145/2103656.2103697), [pdf](http://www.cs.cmu.edu/~rwh/papers/2dtt-can/paper.pdf)&rbrack;
 {#HarperLicata}

* [[Daniel Licata]], _The computational interpretation of HoTT (in 2D)_, talk at [[UF-IAS-2012]]  &lbrack;[video](http://video.ias.edu/stream&ref=1674)&rbrack;

* [[Simon Huber]] (with [[Thierry Coquand]]), _Towards a computational justification of the Axiom of Univalence_ , talk at _TYPES 2011_ &lbrack;[pdf](http://www.cse.chalmers.se/~simonhu/slides/types11.pdf)&rbrack;

* [[Bruno Barras]], [[Thierry Coquand]], [[Simon Huber]], _A Generalization of the Takeuti-Gandy Interpretation_, Mathematical Structures in Computer Science **25** Special Issue 5 (2015) 1071--1099 &lbrack;[pdf](https://simhu.github.io/papers/v5.pdf), [doi:10.1017/S0960129514000504](https://doi.org/10.1017/S0960129514000504)&rbrack;

and realized in [[cubical type theory]] in

* {#Coquand13} [[Thierry Coquand]] (with [[Marc Bezem]] and [[Simon Huber]]), _Computational content of the Axiom of Univalence_, September 2013 &lbrack;[pdf](http://www.humboldt-kolleg.iam.unibe.ch/talks/Coquand.pdf)&rbrack;
 
* [[Cyril Cohen]], [[Thierry Coquand]], [[Simon Huber]], [[Anders Mörtberg]], _Cubical Type Theory: a constructive interpretation of the univalence axiom_, in 21st International Conference on Types for Proofs and Programs (TYPES 2015), Leibniz International Proceedings in Informatics (LIPIcs) **69** (2018) 5:1--5:34 &lbrack;[arxiv:1611.02108](https://arxiv.org/abs/1611.02108), [hal-01378906](https://hal.inria.fr/hal-01378906), [doi:10.4230/LIPIcs.TYPES.2015.5](https://doi.org/10.4230/LIPIcs.TYPES.2015.5)&rbrack;

[[!redirects univalence]]
[[!redirects univalent]]

[[!redirects univalent type family]]
[[!redirects univalent type families]]

[[!redirects univalent universe]]
[[!redirects univalent universes]]
[[!redirects universe extensionality]]

[[!redirects judgmental univalence]]
[[!redirects judgmentally univalent]]
[[!redirects judgmentally univalent universe]]
[[!redirects judgmentally univalent universes]]
[[!redirects judgmental universe extensionality]]

[[!redirects propositional univalence]]
[[!redirects propositionally univalent]]
[[!redirects propositionally univalent universe]]
[[!redirects propositionally univalent universes]]
[[!redirects propositional universe extensionality]]

[[!redirects typal univalence]]
[[!redirects typally univalent]]
[[!redirects typally univalent universe]]
[[!redirects typally univalent universes]]
[[!redirects typal universe extensionality]]

[[!redirects definitional univalence]]
[[!redirects definitionally univalent]]
[[!redirects definitionally univalent universe]]
[[!redirects definitionally univalent universes]]
[[!redirects definitional universe extensionality]]

