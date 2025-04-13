
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

On the other hand, if type theory contains a [[universe]] [[Type]], so that types can be considered as *points* of $Type$, then between two types we also have an [[identity type]] $Paths_{Type}(X,Y)$.  The _univalence axiom_ says that these two notions of "sameness" for types are the same.  

Extensionality principles like [[function extensionality]], [[propositional extensionality]] (where $X$ and $Y$ are [[h-propositions]], and univalence ("typal extensionality") are naturally regarded as a stronger form of _[[identity of indiscernibles]]_. In particular, the [[consistency]] of univalence means that in [[Martin-Löf type theory]] without univalence, one cannot define any [[predicate]] that provably distinguishes isomorphic [[types]]; thus isomorphic types are "externally indiscernible", and univalence incarnates that principle internally by making them identical.

The name *univalence* (due to Voevodsky) comes from the following reasoning.  A fibration or bundle $p\colon E\to B$ of some sort is commonly said to be *universal* if every other bundle of the same sort is a pullback of $p$ in a unique way (up to homotopy).  Less commonly, a bundle is said to be *versal* if every other bundle is a pullback of it in *some* way, not necessarily unique.  By contrast, a bundle is said to be *univalent* if every other bundle is a pullback of it in *at most one* way (up to homotopy).  In the language of [[(∞,1)-category]] theory, a univalent bundle is an [[object classifier]].

The univalence axiom does not *literally* say that anything is univalent in this sense.  However, it is *equivalent* to saying that the canonical fibration over $Type$ is univalent: every fibration with _small_ fibers is an essentially unique pullback of this one (while those with large fibers are not, they are pullbacks of the next higher $Type_1$).  For a description of this equivalence, see section 4.8 of the [[HoTT Book]] (syntactically) and [Gepner-Kock](#GepnerKock12) (semantically).

Univalence is a commonly assumed [[axiom]] in [[homotopy type theory]], and is central to the proposal ([Voevodsky](#Voevodsky)) that this provides a natively [[homotopy theory|homotopy theoretic]] [[foundation]] of [[mathematics]] (see at _[[univalent foundations for mathematics]]_).

## Definition

We work in a [[dependent type theory]] with [[identity types]], [[function types]], [[dependent product types]], [[product types]], and [[dependent sum types]]. 

There are multiple notions of [[equivalence types]] in [[dependent type theory]], which can be used for a definition of univalence for a [[type universe]] $U$; these include

* [[definitional isomorphism types]]
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

Traditional [[homotopy type theory]] uses the type of functions with contractible fibers for both $\simeq$ and $R$, while [[Mike Shulman]]'s model of [[higher observational type theory]] uses the type of $U$-small one-to-one correspondences for $R$ and the type of [[definitional isomorphisms]] for $\simeq$. 

### Stricter versions of univalence

There are stricter versions of univalence, where we replace the [[equivalence of types]] between the identity type $A =_U B$ and the type of equivalences of the universe $A \simeq B$ in the univalence axioms with some notion of [[equality]], such as [[judgmental equality]], [[propositional equality]], and [[typal equality]]. 

1. In any [[dependent type theory]] with [[judgmental equality]], given a [[type universe]] $U$, one could replace the equivalence of types in the definition of univalence with a [[judgmental equality]] of types. This results in **judgmental univalence**, which states that for all small types $A:U$ and $B:U$, one could judge that $(A =_U B) \equiv (A \simeq B) \; \mathrm{type}$.

2. Similarly, in the context of any [[logic over type theory]] with [[propositional equality]], given a [[type universe]] $U$, one could replace the equivalence of types in the definition of univalence with a [[propositional equality]] of types. This results in **propositional univalence**, which states that for all small types $A:U$ and $B:U$, $(A =_U B) \equiv (A \simeq B) \; \mathrm{true}$.

3. Finally, if we are working inside a [[Tarski universe]] $(\mathcal{V}, \mathcal{T})$, then given an internal [[Tarski universe]] $U:\mathcal{V}$ with $T:\mathcal{T}(U) \to \mathcal{V}$, one could replace the equivalence of types in the definition of univalence with a [[typal equality]] of types. This results in **typal univalence**, which states that for all small types $A:\mathcal{T}(U)$ and $B:\mathcal{T}(U)$, there is an [[identification]] $\mathrm{ua}(A, B):(T(A) =_U T(B)) =_{\mathcal{V}} (T(A) \simeq_{\mathcal{V}} T(B))$.

Each of these imply the usual versions of univalence either through the structural rules for [[judgmental equality]] and [[propositional equality]], or through [[identification elimination]], [[transport]], and [[action on identifications]] for [[typal equality]]. 

### Rules for judgmentally univalent universes

With judgmentally univalent Tarski universes $(U, T)$, identities $p:A =_U B$ are [[equivalences of types]] $A$ and $B$. Namely, given [[function types]] and the [[isEquiv]] type family, one could add rules to the type theory which says that $A =_U B$ behaves as an [[equivalence type]]:

Introduction rules:
$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma, x:T[A/X] \vdash f:T[B/X] \quad \Gamma \vdash y:\mathrm{isEquiv}(f)}{\Gamma \vdash \mathrm{equiv}(f, y):A =_U B}$$

Elimination rules:
$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma, x:T[A/X] \vdash f:T[B/X] \quad \Gamma, z:A =_U B \vdash C \; \mathrm{type} \quad \Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash c:C[\mathrm{equiv}(f, y)/z]}{\Gamma, z:A =_U B \vdash \mathrm{ind}_{A =_U B}^C(c):C}$$

Computation rules:
$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma, x:T[A/X] \vdash f:T[B/X] \quad \Gamma, z:A =_U B \vdash C \; \mathrm{type} \quad \Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash c:C[\mathrm{equiv}(f, y)/z]}{\Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash \beta_{A =_U B}^C(c):\mathrm{ind}_{A =_U B}^C(c)[\mathrm{equiv}(f, y)/z] =_{C[\mathrm{equiv}(f, y)/z]} c}$$

Uniqueness rules:
$$\frac{\Gamma \vdash A:U \quad \Gamma \vdash B:U \quad \Gamma, x:T[A/X] \vdash f:T[B/X] \quad \Gamma, z:A =_U B \vdash C \; \mathrm{type} \quad \Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash c:C[\mathrm{equiv}(f, y)/z] \quad \Gamma, z:A =_U B \vdash u:C \quad \Gamma, x:T[A/X], f:T[B/X], y:\mathrm{isEquiv}(f) \vdash i_\mathrm{in}(u):u[\mathrm{equiv}(f, y)/z] =_{C[\mathrm{in}(x, y)/z]} c}{\Gamma, e:A =_U B \vdash \eta_{A =_U B}^C(c):u[e/z] =_{C[e/z]} \mathrm{ind}_{A =_U B}^C(c)[e/z]}$$

### Weaker versions of univalence

In the context of [[function extensionality]], Ian Orton and Andrew Pitts showed [here](http://types2017.elte.hu/proc.pdf#page=93) that the univalence axiom can be simplified to the following special cases:

   * $unit : A = \sum_{a:A} 1$
   * $flip : (\sum_{a:A} \sum_{b:B} C(a,b)) = (\sum_{b:B} \sum_{a:A} C(a,b))$
   * $contract: IsContr(A) \to (A=1)$
   * $unit_\beta : coe(unit(a)) = (a,\star)$
   * $flip_\beta : coe(flip(a,b,c)) = (b,a,c)$.

   The proof constructs $ua(f): A=B$ (for $f:A\simeq B$) as the composite
   $$ A \overset{unit}{=} \sum_{a:A} 1 \overset{contract}{=} \sum_{a:A} \sum_{b:B} f a=b \overset{flip}{=} \sum_{b:B} \sum_{a:A} f a = b \overset{contract}{=} \sum_{b:B} 1 \overset{unit}{=} B $$
   and uses $unit_\beta$ and $flip_\beta$ to compute that $coe(ua(f))(a) = f(a)$, hence by function extensionality $coe(ua(f)) = f$.

This is weaker than univalence because in the absense of [[function extensionality]], it is no longer possible to prove univalence from this set of axioms. 

In addition, unlike the definitions above, this definition of univalence cannot be generalized to [[reflexive graphs]]. 

### Internal univalence

Suppose the [[Tarski universe]] $U$ has 

* internal identity types 
$$\mathrm{Id}^U:\prod_{A:U} T(A) \times T(A) \to U$$
* internal dependent product types 
$$\Pi_U (x:(-)).(-)(x):\left(U \times \prod_{A:U} T(A) \to U\right) \to U$$ 
* internal dependent sum types 
$$\Sigma_U (x:(-)).(-)(x):\left(U \times \prod_{A:U} T(A) \to U\right) \to U$$ 

We assume the weakest notion of Tarski universe, where the type reflection $T(A)$ of each $A:U$ is only equivalent to the external type, since (judgmentally, propositionally, typally) strict Tarski universes are weakly Tarski universes, because the [[judgmental equality]] and [[propositional equality]] imply equivalence of types by the structural rules for judgmental and propostional equality, and [[typal equality]] in a [[type universe]] of types imply equivalence of types by [[identification elimination]], [[transport]], and [[action on identifications]]. 

This allows us to define the internal type of equivalences $A \simeq_U^\mathrm{in} B$, internal to the universe $U$, which comes with a canonical equivalence of types
$$\mathrm{canonical}_\simeq(A, B):T(A \simeq_U^\mathrm{in} B) \simeq (T(A) \simeq T(B))$$ 
This implies that the equivalence $T(A) \simeq T(B)$ is $U$-small, and [[transport]] being an [[equivalence]] then implies that in any universe $U$ which is closed under [[function types]], [[dependent product types]], and [[dependent sum types]], for all $A:U$ and $B:U$, the [[identity type]] $A =_U B$ is $U$-small. 

The internal univalence axiom states that the canonical function 
$$\mathrm{idtointernalequiv}(A, B):(A =_U B) \to T(A \simeq_U^\mathrm{in} B)$$
is an equivalence of types
$$\mathrm{idtoequiv}(A, B):(A =_U B) \simeq T(A \simeq_U^\mathrm{in} B)$$

This is not definable for [[strongly predicative]] [[type universes]], since [[strongly predicative]] [[type universes]] are by definition not closed under [[dependent product types]]. 

In addition, the internal and external versions of univalence imply each other. In order to show that the two axioms imply each other, we need to show that there is an [[identification]] 
$$i(p):\mathrm{canonical}_\simeq(A, B)(\mathrm{idtoequiv}(A, B)(p)) =_{T(A) \simeq T(B)}  \mathrm{trans}^{T}(A, B)(p)$$
for all identifications $p:A =_U B$. By the [[J rule]] it is enough to show that $\mathrm{canonical}_\simeq(A, A)$ maps the identity equivalence of $T(A \simeq_U^\mathrm{in} A)$ to the identity equivalence in $T(A) \simeq T(A)$. Since the identity equivalence in $T(A \simeq_U^\mathrm{in} A)$ is just the [[identity function]] $\mathrm{canonical}_\simeq^{-1}(A, A)(\lambda x.x)$ the above statement is always true. Thus, if the universe is closed under [[identity types]], [[dependent product types]], and [[dependent sum types]] the two univalence axioms imply each other and both define the same notion of univalent universe. 

## In categorical semantics
 {#InCategoricalSemantics}

Let $\mathcal{C}$ be a [[locally cartesian closed model category]] in which all objects are cofibrant. 

By the [[categorical semantics]] of [[homotopy type theory]], a [[dependent type]]

$$
  b : B \vdash E(b) : Type
$$

corresponds to a [[morphism]] $E \to B$ in $\mathcal{C}$ that is a [[fibration]] between fibrant objects.

Then the [[dependent type|dependent]] [[function type]]

$$
  b_1, b_2 : B \vdash ( E(b_1) \to E(b_2)) : Type
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

The fibration $E \to B$ is univalent, precisely when this morphism is  a weak equivalence.

This appears originally as [Voevodsky, def. 3.4](#UnivalentFoundationsProject)

### In simplicial presheaves
  {#InSimplicialPresheaves}

(...)

See ([Shulman 12](#Shulman12), [UF 13](UF13))

(...)

## Properties

### Relation to function extensionality

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
The semantics of dependent type theory with excluded middle and universes satisfying the univalence axiom are [[boolean topos|boolean]] [[(infinity,1)-topos|$(\infty, 1)$-toposes]]. 

However, there is a global choice axiom which is inconsistent with univalence:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{gc}_A:A + (A \to \emptyset)}$$
This is sometimes called "excluded middle" in the [[propositions as types]] interpretation of type theory, where the principle of excluded middle is reinterpreted so that types are used instead of [[mere propositions]]. But this choice principle is a much stronger axiom than excluded middle, being of comparable strength to a [[choice operator]] and implying that every type is an [[h-set]]; hence inconsistent with the univalence axiom. 

### Canonicity and homotopy canonicity
 {#Canonicity}

It is currently open whether the univalence axiom enjoys [[canonicity]] in general, but for the special case of [[1-truncated]] homotopy types ([[groupoids]]) (and two nested univalent [[universes]] and [[function extensionality]]), [[homotopy canonicity]] has been shown in ([Shulman 12, section 13](#Shulman12).  Thus, in univalent homotopy 1-type theory with two universes, every [[term]] of [[type]] of the [[natural numbers]] is [[propositional equality|propositionally equal]] to a [[numeral]].

The construction in ([Shulman 12, section 13](#Shulman12)) uses [[Artin gluing]] of a suitable [[type-theoretic model category|type-theoretic fibration category]] with the [[category]] [[Set]] and [[Grpd]], respectively, effectively inducing canonicity from these categories. By ([Shulman 12, remark 13.13](#Shulman12)) for this construction to generalize to untruncated univalent type theory, one seems to need a sufficiently strict [[global sections]] functor with values in some model for [[infinity-groupoids]]. A proof of the full result has been announced by [[Christian Sattler]] and [[Krzysztof Kapulkin]] ([Sattler 19](#Sattler19)).

Notice that this sort of [[canonicity]] does not yet imply [[computational effectiveness]], which would require also an [[algorithm]] to extract that [[numeral]] from the given [[term]].  There may be such an algorithm, but so far attempts to extract one from the proof (or to give a [[constructive mathematics|constructive]] version of the [[proof]], which would imply the existence of an algorithm) have not succeeded.

It is also a *[[propositional equality|propositional]]* canonicity, as opposed to the [[judgmental equality|judgmental]] canonicity which many traditional [[type theories]] enjoy.  Another approach to canonicity for 1-truncated univalence can be found in ([Harper-Licata](#HarperLicata)), which involves modifying the type theory by adding more [[judgmental equalities]], resulting in a judgmental canonicity.  However, no [[algorithm]] for computing canonical forms has yet been given for this approach either.

Canonicity has been proved for [[cubical type theory]].

One might also try to construct the Hoffman-Streicher groupoid model in a constructive framework; Awodey and Bauer have done some work in this direction with an [[predicative mathematics|impredicative]] [[universe]] of [[h-sets]].

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

## Related concepts

* [[univalent foundations]]

* [[univalent type theory]]

* [[extensionality]]

  * Univalence is closely related to the "completeness" condition in the theory of [[Segal spaces]]/[[semi-Segal spaces]]. See _[[complete Segal space]]_/_[[complete semi-Segal space]]_.

  * [[propositional extensionality]]

* contrary to univalence is the [[axiom UIP]]

* [[directed univalence axiom]]

* [[identity type#IdentityTypesBetweenTypes|identity type between types]]

## References
 {#References}

> For more references see also at _[[homotopy type theory]]_.

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


Later in:

* [[Vladimir Voevodsky]],  *[The Origins and Motivations of Univalent Foundations](https://www.ias.edu/ideas/2014/voevodsky-origins)*, IAS Institute Letter Summer 2014

appears the claim that:

> have been working on the ideas that led to the discovery of univalent models since 2005 and gave the first public presentation on this subject at Ludwig-Maximilians-Universität München in November 2009.



A comprehensive discussion finally appears in the textbook:

* [[UF-IAS-2012|Univalent Foundations Project]], p. 4 & Sec. 2.10 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013)  &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

Voevodsky's ([Bousfield's](#Bousfield06)) original idea for the [[universal Kan fibration]] as a model for a univalent universe in [[simplicial sets]]/[[infinity-groupoids|$\infty$-groupoids]] was eventually published as:

* {#KapulkinLumsdaine21} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], *The Simplicial Model of Univalent Foundations (after Voevodsky)*, Journal of the European Mathematical Society **23** (2021) 2071–2126  $[$[arXiv:1211.2851](https://arxiv.org/abs/1211.2851), [doi:10.4171/jems/1050](https://doi.org/10.4171/jems/1050)$]$

Exposition and survey

* [[Peter Aczel]], *On Voevodsky’s Univalence Axiom*, talk at Third European Set Theory Conference (2011) &lbrack;[pdf](http://www.cs.man.ac.uk/~petera/Recent-Slides/Edinburgh-2011-slides_pap.pdf), [[Aczel-Univalence.pdf:file]]&rbrack;

  > (in view of the [[structure identity principle]])

* [[Mike Shulman]], _Homotopy type theory, IV_ ([blog post](http://golem.ph.utexas.edu/category/2011/04/homotopy_type_theory_iv.html))

Additional definition of univalent universes appeared in section 17.1 of 

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

as well as in this Google Groups thread:

* {#Licata16} [[Dan Licata]], *weak univalence with "beta" implies full univalence* ([web](https://groups.google.com/forum/#!msg/homotopytypetheory/j2KBIvDw53s/YTDK4D0NFQAJ))

An accessible account of Voevodsky's proof (following [Bousfield 06](#Bousfield06)) that the universal [[Kan fibration]] in [[simplicial sets]] is univalent:

* {#KapulkinLumsdaineVoevodsky12} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], [[Vladimir Voevodsky]], _Univalence in simplicial sets_ &lbrack;[arXiv:1203.2553](http://arxiv.org/abs/1203.2553)&rbrack;

A quick elegant proof of the [[object classifier]]/universal [[associated infinity-bundle]] in simplicial sets/$\infty$-groupoids is in 

* {#Moerdijk} [[Ieke Moerdijk]] (notes by Chris Kapulkin), _Fiber bundles and univalence_ ([pdf](http://www-home.math.uwo.ca/~kkapulki/notes/fiber_bundles_univalence.pdf))
 
See also 

* [[Colin McLarty]], _A univalent universe in finite order arithmetic_ ([arXiv:1412.6714](http://arxiv.org/abs/1412.6714))

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
 

Some details regarding the univalence axiom for [[weakly Tarski universes]] appeared on MathOverflow in:

* Madeleine Birchfield, Valery Isaev, *Univalence for weakly Tarski universes*, MathOverflow, ([web](https://mathoverflow.net/q/431723))

A discussion of univalence in categories of [[diagrams]] over an [[inverse category]] with values in a category for which univalence is already established is discussed in 

* [[Michael Shulman]], _Univalence for inverse diagrams, oplax limits, and gluing, and homotopy canonicity_ ([arXiv:1203.3253](http://arxiv.org/abs/1203.3253))
 {#Shulman12}

This discusses [[canonicity]] of univalence in its section 13. Another approach to showing canonicity is (via [[cubical sets]]) in 

* [[Thierry Coquand]], Simon Huber, _A model of type theory in cubical sets_, 2013  ([pdf](http://www.cse.chalmers.se/~coquand/mod1.pdf), [Haskell code](https://github.com/simhu/cubical), [discussion](https://groups.google.com/forum/#!topic/homotopytypetheory/GmXKEArD3HY))
  {#CoquandHuber13}

A proof of canonicity is presented in the talk

* {#Sattler19} [[Christian Sattler]], _Homotopy Canonicity_, ([abstract](http://www.ii.uib.no/~bezem/abstracts/TYPES_2019_paper_110))


On the issue of strict pullback of the univalent universe see

* Univalent Foundations Mailing List, _[Quotients](https://groups.google.com/d/msg/univalent-foundations/Glo7NgNvhJA/4j9SewiFvQ0J)_, March 2013
  {#UF13}

The computational interpretation of univalence / [[canonicity]] is discussed in 

* [[Dan Licata]], [[Robert Harper]], _Computing with Univalence_  (2012) ([pdf](http://4wft.fmf.uni-lj.si/wp-content/uploads/2012/04/Licata.pdf))

* [[Robert Harper]], [[Daniel Licata]], _Canonicity for 2-dimensional type theory_ (2011) ([pdf](http://www.cs.cmu.edu/~rwh/papers/2dtt-can/paper.pdf))
 {#HarperLicata}

* [[Daniel Licata]] _The computational interpretation of HoTT (in 2D)_, talk at [[UF-IAS-2012]]  ([video](http://video.ias.edu/stream&ref=1674))

* Simon Huber (with [[Thierry Coquand]]), _Towards a computational justification of the Axiom of Univalence_ , talk at _TYPES 2011_ ([pdf](http://www.cse.chalmers.se/~simonhu/slides/types11.pdf))

* Bruno Barras, [[Thierry Coquand]], Simon Huber, _A Generalization of Takeuti-Gandy Interpretation_ ([pdf](http://uf-ias-2012.wikispaces.com/file/view/semi.pdf))

and realized in [[cubical type theory]] in

* {#Coquand13} [[Thierry Coquand]] (with [[Marc Bezem]] and [[Simon Huber]]), _Computational content of the Axiom of Univalence_, September 2013 ([pdf](http://www.humboldt-kolleg.iam.unibe.ch/talks/Coquand.pdf))
 
* [[Cyril Cohen]], [[Thierry Coquand]], [[Simon Huber]], [[Anders Mörtberg]], _Cubical Type Theory: a constructive interpretation of the univalence axiom_ ([pdf](https://hal.inria.fr/hal-01378906/document))

* {#BezemCoquandHuber17} [[Marc Bezem]], [[Thierry Coquand]], [[Simon Huber]], _The univalence axiom in cubical sets_ ([arXiv:1710.10941](https://arxiv.org/abs/1710.10941))

A study of the [[semantics|semantic]] side of univalence in [[(infinity,1)-toposes]], as well as further cases of [[locally cartesian closed (infinity,1)-categories]] is in

* {#GepnerKock12} [[David Gepner]], [[Joachim Kock]], _Univalence in locally cartesian closed infinity-categories_ ([arXiv:1208.1749](http://arxiv.org/abs/1208.1749))

This does not yet show that the univalence axiom in its usual form holds in the internal type theory of [[(infinity,1)-toposes]], however, due to the lack of a (known) sufficiently strict model for the object classifier.  (But it works with [[Tarski universes]], see there and [[type universes]]). Constructions of such a model in some very special cases are in [Shulman12](#Shulman12) above, and also in

* [[Michael Shulman]], _The univalence axiom for elegant Reedy presheaves_, [arXiv:1307.6248](http://arxiv.org/abs/1203.3253).

* {#Cisinski14} [[Denis-Charles Cisinski]], _Univalent universes for elegant models of homotopy types_ ([arXiv:1406.0058](http://arxiv.org/abs/1406.0058))

Finally, full proof that all [[∞-stack]] [[(∞,1)-topos]] have [[presentable (∞,1)-category|presentations]] by [[model categories]] which interpret (provide [[categorical semantics]]) for [[homotopy type theory]] with [[univalence|univalent]] [[type universes]]:

* {#Shulman19} [[Michael Shulman]], _All $(\infty,1)$-toposes have strict univalent universes_ ([arXiv:1904.07004](https://arxiv.org/abs/1904.07004)).

Application of univalence to [[proof]] transfer:

* Cyril Cohen, Enzo Crance, Assia Mahboubi, *Trocq: Proof Transfer for Free, With or Without Univalence*, in: *Programming Languages and Systems. ESOP 2024*, Lecture Notes in Computer Science **14576**, Springer (2024) &lbrack;[arXiv:2310.14022](https://arxiv.org/abs/2310.14022), [doi:10.1007/978-3-031-57262-3_10](https://doi.org/10.1007/978-3-031-57262-3_10)&rbrack;

Some discussion about the univalence axiom in [[dependent type theory with type variables]] occurs in:

* {#CTZulip} *Dependent Type Theory vs Polymorphic Type Theory*, Category Theory Zulip ([web](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Dependent.20Type.20Theory.20vs.20Polymorphic.20Type.20Theory))


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


