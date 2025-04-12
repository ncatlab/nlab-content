
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[type theory]], a _type universe_ -- usually written $\mathcal{U}$ or $Type$ -- is a [[type]] whose [[terms]] are either themselves [[type|types]] ([[Russell universes]]), or representations of types in an internal model of the type theory ([[Tarski universes]]). Either way, it is a [[universe]] of (small) [[type|types]], a _universe in type theory_, and sometimes called a _type of types_.

{#TypeUniverseAsReflection} One also speaks of $\mathcal{U}$ as being a _reflection_ of the type system in itself (e.g. [MartinL&#246;f 74, p. 6](#MartinLoef74), [Palmgren, pp. 2-3](#Palmgren), [Rathjen, p. 1](#Rathjen), [Luo 11, section 2.5](#Luo11), [Luo 12, p. 2](#Luo12), [Stanf. Enc. Phil.](#SEP)), following the _[[reflection principle]]_ in [[set theory]].

In [[homotopy type theory]] a type of (small) types is what in [[(∞,1)-category theory|higher]] [[categorical semantics]] is interpreted as a (small) _[[object classifier]]_.  Thus, the type of types is a refinement of the [[type of propositions]] which only contains the [[(-1)-truncated]]/[[h-level]]-1 types (and is semantically a [[subobject classifier]]).

In the presence of a type universe a [[judgement]] of the form

$$
  \vdash A : \mathcal{U}
$$

says that $A$ is a [[term]] of [[type]] $\mathcal{U}$, hence is either a (small) [[type]] itself (for Russell universes), or a representation of types in an internal model of the type theory (for Tarski universes). 

More generally, in Russell universes a [[hypothetical judgement]] of the form

$$
  x : X \vdash A(x) : \mathcal{U}
$$

says that $A$ is an $X$-[[dependent type]].

In Tarski universes the corresponding hypothetical judgment would be of the form

$$
  x : X \vdash El(A)(x)\; type
$$

Type universes are important in [[dependent type theory]] for numerous reasons:

1. Dependent type theory with a separate [[type]] [[judgment]] serves as a background for a variety of [[foundations of mathematics]] via the [[propositions as some types]] interpretation of dependent type theory: One can add a [[von Neumann universe]] to the dependent type theory and work entirely in the von Neumann universe for [[material set theory]]; one can add a [[category of sets]] to the dependent type theory and work entirely in the category of sets for [[structural set theory]]; and one can add a [[type of all propositions]] and a [[natural numbers type]] and work in the dependent type theory itself for [[higher-order logic]]. For [[univalent type theory]] and [[univalent foundations]], on the other hand, one needs to add a type universe satisfying certain [[axioms]] and [[axiom schemata]], such as [[universe extensionality]], closure under identity types, closure under dependent sum types, closure under dependent product types, [[propositional resizing]], [[axiom of replacement|replacement]], [[axiom of infinity|infinity]], and [[axiom of choice|choice]], to the dependent type theory. 

1. In [[set theory]], one could usually quantify over sets using the [[universal quantifier]] and the [[existential quantifier]]. However, in [[dependent type theory]], one could only quantify over elements of types. Without type universes, types are not elements of type universes, but rather [[judgment|judged]] separately as a type, and thus it is impossible to quantify over types. Quantification over types is necessary for proving [[universal properties]] of various [[mathematical structures]], such as that the [[integers]] are the [[initial object|initial]] [[commutative ring]]. 

1. Having a [[hierarchy of universes]] where every type is an element of the hierarchy, instead of a single separate type judgment has its own benefits. These includes the lack of annotations in defining types, since all types are elements of universes $A:U_i$ and all family of types are elements of function types $B:A \to U_i$; the lack of additional rules for judgmental equality in type theories with judgmental equality, since they are all admissible; the ease of definitions of types in [[objective type theory]] which does not have [[judgmental equality]]; and the lack of separate type judgments for modes in [[split context]] [[modal type theory]]. However, this comes at the cost of having to formalize the theory of universe levels of the hierarchy of universes before formalizing the type theory. 

In [[homotopy type theory]] the type universe $\mathcal{U}$ is often assumed to satisfy the [[univalence]] [[axiom]]. This is a reflection of the fact that in its [[categorical semantics]] as an [[object classifier]] is part of an [[internal (∞,1)-category]] in the ambient [[(∞,1)-topos]]: the one that as an [[indexed category]] is the small [[codomain fibration]].

[[Per Martin-Lof]]'s original type theory contained a Russell universe which contained *all* types, which therefore in particular contained itself, i.e. one had $Type : Type$. But it was pointed out by [[Jean-Yves Girard]] that this was inconsistent; see [[Girard's paradox]]. Thus, modern type theories generally contain a [[hierarchy of universes]]. 

## Formalizations 

### Russell universe
  {#RussellStyle}

A **[[Russell universe]]** or **universe &#224; la Russell** is a [[type]] whose terms *are* types. In the presence of a separate [[judgment]] "$A \;type$", this can be formulated as a [[natural deduction|deduction rule]] of the form

$$\frac{A:\mathcal{U}}{A \;type}$$

Thus, the [type formers](natural+deduction#IntroductionAndElimination) have rules saying which universe they belong to, such as:

$$\frac{A:\mathcal{U}\quad B:A\to \mathcal{U}}{\Pi\, A\, B : \mathcal{U}}$$

With Russell universes, we can also omit the judgment "$A\; type$" and replace it everywhere by a judgment that A is a term of some universe. This is the approach taken in [UFP13](#UFP13).

### Tarski universes
 {#TarskiStyle}

A **[[Tarski universe]]** or a **universe &#224; la Tarski** ([Hofmann, section 2.1.6](#Hofmann), [Luo 12](#Luo12), [Gallozzi 14, p. 40](#Gallozzi14)) is a type $U$ together with an "interpretation" operation allowing us to regard its [[terms]] as _codes_ or _names_ for actual types. Thus we have a rule such as

$$\frac{A:\mathcal{U}}{El(A)\;type}$$

saying that for each term $A$ of the type universe $U$ there is an actual type $El(A)$. This is the approach taken by [[Egbert Rijke]]'s [[Introduction to Homotopy Type Theory]]. 

Conversely, with notation as used at _[[object classifier in an (infinity,1)-topos]]_, one might write $A = 'El(A)'$ to indicate that $A$ is the _name_ of the type $El(A)$ in the type universe.

We usually also have operations on the universe corresponding to (but not identical to) type formers, such as

$$\frac{A:\mathcal{U}\quad B:A\to \mathcal{U}}{\pi(A, B) : \mathcal{U}}$$

with an [[equality]] $El(\pi(A,B))=\Pi \, El(A)\, El(B)$. Usually this latter equality (and those for other type formers) is a [[judgmental equality]]. If it is only an [[equivalence in homotopy type theory|equivalence]] (i.e. we have a rule which gives us a canonical term of the equivalence type), we may speak of a **[[weakly Tarski universe]]** ([Gallozzi 14, p. 49-50](#Gallozzi14)).

We can give a slightly different definition of weakly Tarski universe using [[typal equality]] in either a larger universe or a [[dependent type theory with type variables]] and [[identity type#IdentityTypesBetweenTypes|identity types between types]]. More precisely, 

* in a larger universe $U'$ we can consider a universe $\mathcal{U}$ and with the usual rules for the relative reflection $el(a):\mathcal{U}'$ for any $a:\mathcal{U}$, a choice of weakly or strongly Tarski [[computation rules]] for the reflections $El$ and $El'$, and a computation rule for the relative reflection el of $\mathcal{U}$ inside $\mathcal{U}'$ based on typal equality, which gives us canonical elements of the identity types $Id_{\mathcal{U}'}(\pi'(el(a),el(b)),el(\pi(a,b)))$ and similarly for the other type formers. 

* in [[dependent type theory with type variables]] and [[identity type#IdentityTypesBetweenTypes|identity types between types]] we can similarly consider a universe $\mathcal{U}$ and with the usual rules for the relative reflection $el(a) \; \mathrm{type}$ for any $a:\mathcal{U}$, a choice of weakly or strongly Tarski [[computation rules]] for the reflections $El$ and $El'$, and a computation rule for the relative reflection el of $\mathcal{U}$ based on typal equality, which gives us canonical elements of the identity types between types $\mathrm{Id}(\pi'(el(a),el(b)),el(\pi(a,b)))$ and similarly for the other type formers. 

If the containing universe or dependent type theory with type variables is univalent, the two definitions of a weak Tarski universe turn out to coincide.

The three notions of Tarski universe can be ordered by generality: Every Tarski universe is weakly Tarski by equivalences, because both definitional equality of types $A \equiv B$ and the identity types between two types $A = B$ imply that the two types of equivalent $A \simeq B$. Similarly, every strict Tarski universe is weakly Tarski by the identity type, because definitional equality of types $A \equiv B$ implies that two types are identified $A = B$. 

Since each type former is independent of each other, one could also have mixed versions of Tarski universes, where some of the type formers are strictly Tarski and some are weakly Tarski. This leads to $2^n$ possible Tarski universes, where $n$ is the number of type formers in a type theory, and the $2^n$ type theories are only [[partially ordered]] by generality. Internally in an ambient universe, that number becomes $3^n$. 

Universes defined internally via [[induction-recursion]] are stricty Tarski. Weakly Tarski universes are easier to obtain in [[semantics]] (see [below](#CategoricalSemantics)): they are somewhat more annoying to use, but probably suffice for most purposes. In [[objective type theory]], there is no [[definitional equality]], so every Tarski universe is weakly Tarski. 

### Other universes

There are other universes which one could use. For example, any model of [[material set theory]] $V$ or [[structural set theory]] $\mathcal{E}$ would suffice. Material set theories become Tarski universes by the type family 

$$x:V \vdash \mathrm{El}(x) \coloneqq \sum_{y:V} y \in x$$

and structural set theories become Tarski universes by the type family 

$$x:V \vdash \mathrm{El}(x) \coloneqq \mathrm{hom}(1, x)$$

where $1:\mathcal{E}$ is the [[terminal object|terminal]] [[separator]]. 

Thus, in a [[dependent type theory]] with a separate [[type]] [[judgment]], one could simply include inference rules for [[ZFC]] or [[ETCS]]. 

## Properties

### Universe enlargement
 {#UniverseEnlargement}

Both [[Coq]] and [[Agda]] support [[universe polymorphism]] to deal with the issue of universe enlargement. Moreover, Coq supports [[typical ambiguity]].

### Extensionality principle of type universes

The extensionality principle of type universes is given by the [[univalence axiom]], which for [[Tarski universes]] $(U, T)$ states that [[transport]] across the universal type family $T$ is an equivalence of types for all small types $A:U$ and $B:U$; and for [[Russell universes]] $U$ states that the recursively defined function $\mathrm{idToEquiv}$, which takes identifications between small types $A:U$ and $B:U$ to equivalences between $A$ and $B$, is an equivalence of types for all small types $A:U$ and $B:U$. 

### Cumulativity

A tower of universes is **cumulative** if $A:\mathcal{U}_i$ implies $A:\mathcal{U}_{i+1}$ (rather than, say, $Lift(A):\mathcal{U}_{i+1}$).

Cumulative Russell universes have some issues; see for instance [Luo 12](#Luo12).

* [[Coq]] uses Russell style universes. For practical purposes, it also has cumulativity, although there is some question (perhaps mainly semantic) of whether this is true internally or whether it uses casts that are simply hidden from the user.

* [[Agda]] uses non-cumulative Russell style universes.

* [UFP13](#UFP13) (first edition) uses cumulative Russell style universes.

### Categorical semantics
 {#CategoricalSemantics}

[[univalence|Univalent]] [Russell universes](#RussellStyle) have been shown to be interpreted in [[type-theoretic model categories]] presenting the base [[(∞,1)-topos]] [[∞Grpd]] ([Kapulkin-Lumsdaine-Voevodsky 12](#KapulkinLumsdaineVoevodsky12))
and more generally presenting [[(∞,1)-toposes]] of [[(∞,1)-presheaves]] over [[elegant Reedy categories]] ([Shulman 13](#Shulman13)).

Discussion for general [[(∞,1)-toposes]] (of [[(∞,1)-sheaves]]) that should have implementation [weakly Tarski](#TarskiStyle) ([Gallozzi 14, p. 49-50](#Gallozzi14)) is in ([Gepner-Kock 12](#GepnerKock12)).

For more on this see the respective sections at _[[relation between type theory and category theory]]_.

## Other types of types

There is other notions of type of types. Suppose we have a Russell universe $U$ or a Tarski universe $(U, T)$ and a function $P:U \to \mathrm{Prop}_U$. Then the type of $U$-small types which satisfy $P$ is given by the [[dependent sum type]] $\sum_{A:U} P(A)$ for Russell universes and $\sum_{A:U} T(P(A))$ for Tarski universes. 

Since universes are internal models of type theory, in a dependent type theory with a separate [[type]] [[judgment]], one could generalize the above notion of "type of $U$-small types which satisfy $P$" to the notion of "type of all types which satisfy $P$". Types $A$, previously elements of the universe $A:U$, are now judged to be types $A \; \mathrm{type}$. The function $P:U \to \mathrm{Prop}_U$ which takes types to propositons is now an operator on types, which is defined using [[inference rules]]:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash P(A) \; \mathrm{type}} \quad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{proptrunc}_{P(A)}:\mathrm{isProp}(P(A)) \; \mathrm{type}}$$

Examples of such $P$ definable from the existing type formers in [[dependent type theory]] include 

* $\mathrm{isProp}$, which results in the [[type of all propositions]], 
* $\mathrm{isFinite}$, which results in the [[type of all finite types]], 
* given a type $T$, $[(-) \simeq T]$, which results in the type of all types merely [[equivalence of types|equivalent]] to $T$. 
* given a type $T$, $[(-) \hookrightarrow T]$, which results in the [[subobject preorder|subtype preorder]] of $T$, the type of all types which merely [[embedding of types|embed into]] $T$. 

The resulting **type of types which satisfy $P$** is denoted by $\mathrm{Type}_P$. 

Care must be taken for which $P$ one could use to define the type of all types which satisfy $P$. For example, given [[unit type]] $\mathbb{1}$, for $P(A) \equiv A \to \mathbb{1}$ and $P(A) \equiv \mathrm{isSet}(A)$, the resulting $\mathrm{Type}_P$ always contains itself or its [[set truncation]] in addition to the [[empty type]], resulting in [[Girard's paradox]]; thus, one cannot form such types of types in the type theory. Similarly, for 
$$P(A) \equiv \prod_{x:A} \prod_{y:A} (x =_A y) \vee \neg (x =_A y)$$ 
the resulting $\mathrm{Type}_P$ contains its set truncation in addition to the empty type if the [[principle of excluded middle]] holds for all propositions, resulting in [[Girard's paradox]]; thus, one could only form $\mathrm{Type}_P$ for 
$$P(A) \equiv \prod_{x:A} \prod_{y:A} (x =_A y) \vee \neg (x =_A y)$$ 
if one doesn't have excluded middle in the type theory. 

Now, supposing that the [[dependent type theory]] has the above rules for $P(A)$, $\mathrm{Type}_P$ could be presented either as a [[Russell universe]] or a [[Tarski universe]] in a [[dependent type theory]]. The difference between the two is that in the former, every type which satisfies $P$ in the type theory is literally an element of the type of types which satisfy $P$, while in the latter, elements of $\mathrm{Type}_P$ are only indices of a type family $\mathrm{El}$; every [[finite type]] in the type theory is only [[essentially small type|essentially $\mathrm{Type}_P$-small]] for [[weak Tarski universes]] or [[judgmentally equal]] to an $P(A)$ for $A:\mathrm{Type}_P$ for [[strict Tarski universes]]. 

For weak Tarski type of types with satisfy $P$, one also needs the typal congruence rules for forming $P(A)$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B}{\Gamma \vdash \mathrm{congform}_P(e):P(A) \simeq P(B) \; \mathrm{type}}$$

#### As a strict Tarski universe

As a [[strict Tarski universe]], the type of all types which satisfy $P$ is given by the following [[natural deduction]] [[inference rules]]:

Formation rules for the type of all types which satisfy $P$:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Type}_P \; \mathrm{type}}$$

Introduction rules for the type of all types which satisfy $P$:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{toElem}_A:P(A) \to \mathrm{Type}_P}$$

Elimination rules for the type of all types which satisfy $P$:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{El}(A) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{witn}_P(A):P(\mathrm{El}(A))}$$

Computation rules for the type of all types which satisfy $P$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \mathrm{El}(\mathrm{toElem}_A(p)) \equiv A \; \mathrm{type}}$$

* Judgmental computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \mathrm{witn}_P(\mathrm{toElem}_A(p)) \equiv p:P(A)}$$

* Typal computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \beta_{\mathrm{Type}_P}^{\mathrm{Witn}_P,A}(p):\mathrm{witn}_P(\mathrm{toElem}_A(p)) =_{P(A)} p}$$

Uniqueness rules for the type of all types which satisfy $P$:

* Judgmental computation rules:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{toElem}_{\mathrm{El}(A)}(\mathrm{witn}_P(A)) \equiv A:\mathrm{Type}_P}$$

* Typal computation rules:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \eta_{\mathrm{Type}_P}(A):\mathrm{toElem}_{\mathrm{El}(A)}(\mathrm{witn}_P(A)) =_{\mathrm{Type}_P} A}$$

[[univalence axiom|Extensionality principle]] of the type of all types which satisfy $P$:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P \quad \Gamma \vdash B:\mathrm{Type}_P} {\Gamma \vdash \mathrm{ext}_{\mathrm{Type}_P}(A, B):\mathrm{isEquiv}(\mathrm{transport}^\mathrm{El}(A, B))}$$

#### As a weak Tarski universe

As a [[weak Tarski universe]], the type of all types which satisfy $P$ is given by the following [[natural deduction]] [[inference rules]]:

Formation rules for the type of all types which satisfy $P$:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Type}_P \; \mathrm{type}}$$

Introduction rules for the type of all types which satisfy $P$:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{toElem}_A:P(A) \to \mathrm{Type}_P}$$

Elimination rules for the type of all types which satisfy $P$:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{El}(A) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{witn}_P(A):P(\mathrm{El}(A))}$$

Computation rules for the type of all types which satisfy $P$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \beta_{\mathrm{Type}_P}^{\mathrm{El}, A}(p):\mathrm{El}(\mathrm{toElem}_A(p)) \simeq A \; \mathrm{type}}$$

* Judgmental computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \mathrm{congform}_P(\beta_{\mathrm{Type}_P}^{\mathrm{El}, A}(p))(\mathrm{witn}_P(\mathrm{toElem}_A(p))) \equiv p:P(A)}$$

* Typal computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \beta_{\mathrm{Type}_P}^{\mathrm{witn}_P,A}(p):\mathrm{congform}_P(\beta_{\mathrm{Type}_P}^{\mathrm{El}, A}(p))(\mathrm{witn}_P(\mathrm{toElem}_A(p))) =_{P(A)} p}$$

where the equivalence
$$\mathrm{congform}_P(\beta_{\mathrm{Type}_P}^{\mathrm{El}, A}(p)):P(\mathrm{El}(\mathrm{toElem}_A(p))) \simeq P(A)$$
is provided from the typal computation rules for $P(A)$. 

Uniqueness rules for the type of all types which satisfy $P$:

* Judgmental computation rules:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash A \equiv \mathrm{toElem}_{\mathrm{El}(A)}(\mathrm{witn}_P(A)):\mathrm{Type}_P}$$

* Typal computation rules:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \eta_{\mathrm{Type}_P}(A):A =_{\mathrm{Type}_P} \mathrm{toElem}_{\mathrm{El}(A)}(\mathrm{witn}_P(A))}$$

[[univalence axiom|Extensionality principle]] of the type of all types which satisfy $P$:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P \quad \Gamma \vdash B:\mathrm{Type}_P} {\Gamma \vdash \mathrm{ext}_{\mathrm{Type}_P}(A, B):\mathrm{isEquiv}(\mathrm{transport}^\mathrm{El}(A, B))}$$

#### As a Russell universe

As a [[Russell universe]], the type of all types which satisfy $P$ is given by the following [[natural deduction]] [[inference rules]]:

Formation rules for the type of all types which satisfy $P$:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{Type}_P \; \mathrm{type}}$$

Introduction rules for the type of all types which satisfy $P$:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{toElem}_A:P(A) \to \mathrm{Type}_P}$$

Elimination rules for the type of all types which satisfy $P$:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash A \; \mathrm{type}} \qquad \frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{witn}_P(A):P(A)}$$

Computation rules for the type of all types which satisfy $P$:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \mathrm{toElem}_A(p) \equiv A \; \mathrm{type}}$$

* Judgmental computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \mathrm{witn}_P(\mathrm{toElem}_A(p)) \equiv p:P(A)}$$

* Typal computation rules:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash p:P(A)}{\Gamma \vdash \beta_{\mathrm{Type}_P}^{\mathrm{finWitn},A}(p):\mathrm{witn}_P(\mathrm{toElem}_A(p)) =_{P(A)} p}$$

Uniqueness rules for the type of all types which satisfy $P$:

* Judgmental computation rules:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \mathrm{toElem}_{A}(\mathrm{witn}_P(A)) \equiv A:\mathrm{Type}_P}$$

* Typal computation rules:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P}{\Gamma \vdash \eta_{\mathrm{Type}_P}(A):\mathrm{toElem}_{A}(\mathrm{witn}_P(A)) =_{\mathrm{Type}_P} A}$$

[[univalence axiom|Extensionality principle]] of the type of all types which satisfy $P$:
$$\frac{\Gamma \vdash A:\mathrm{Type}_P \quad \Gamma \vdash B:\mathrm{Type}_P} {\Gamma \vdash \mathrm{ext}_{\mathrm{Type}_P}(A, B):\mathrm{isEquiv}(\mathrm{idToEquiv}(A, B))}$$

## Related concepts

* [[resizing axiom]]

* [[universe polymorphism]]

* [[univalence]]

* [[Prop]], the [[type of propositions]]

  * [[subobject classifier]]

* [[object classifier]]

* [[type of classes]]

* [[parametric polymorphism]]

* [[Girard's paradox]]

* [[Awodey's conjecture]]

* [[univalent type theory]]

* [[hierarchy of universes]]

## References

Type universes in [[Martin-Löf type theory]] originate in un-stratified and hence inconsistent form with

* [[Per Martin-Löf]], §2.7.1 in: *A Theory of Types*, unpublished note (1971) &lbrack;[pdf](https://raw.githubusercontent.com/michaelt/martin-lof/master/pdfs/martin-loef1971%20-%20A%20Theory%20of%20Types.pdf), [[MartinLoef1971-ATheoryOfTypes.pdf:file]]&rbrack;

and then in stratified and consistent form in

* {#MartinLof75} [[Per Martin-Löf]], §1.10 in: _An intuitionistic theory of types: predicative part_, in: H. E. Rose, J. C. Shepherdson (eds.), *Logic Colloquium '73, Proceedings of the Logic Colloquium*, Studies in Logic and the Foundations of Mathematics **80**, Elsevier (1975) 73-118 &lbrack;<a href="https://doi.org/10.1016/S0049-237X(08)71945-1">doi:10.1016/S0049-237X(08)71945-1</a>, [CiteSeer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.131.926)&rbrack;

elaborated on in

* [[Per Martin-Löf]] (notes by [[Giovanni Sambin]]): *Universes*, pp. 47 in: _Intuitionistic type theory_, Lecture notes Padua 1984, Bibliopolis, Napoli (1984) &lbrack;[pdf](https://archive-pml.github.io/martin-lof/pdfs/Bibliopolis-Book-retypeset-1984.pdf), [[MartinLofIntuitionisticTypeTheory.pdf:file]]&rbrack;

which also introduces (p. 48) the distinction into notions of *[[Russell universes]]* and *[[Tarski universes]]*.

Further discussion in

* {#Hofmann95} [[Martin Hofmann]], *Universes*, section 2.3.5 in: *Syntax and semantics of dependent types*, Chapter 2 in: _Extensional concepts in intensional type theory_, Ph.D. thesis, University of Edinburgh (1995), Distinguished Dissertations, Springer (1997) &lbrack;[ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]], [doi:10.1007/978-1-4471-0963-1](https://doi.org/10.1007/978-1-4471-0963-1)&rbrack;

Review and further discussion:

* {#Palmgren} [[Erik Palmgren]], _On Universes in Type Theory_, in *Twenty-Five Years of Constructive Type Theory*, Oxford University Press (1998) 191–204 &lbrack;[pdf](http://www2.math.uu.se/~palmgren/universe.pdf), [doi:10.1093/oso/9780198501275.003.0012](https://doi.org/10.1093/oso/9780198501275.003.0012)&rbrack;

Introduction with an eye towards [[homotopy type theory]]:

* {#UFP13} [[Univalent Foundations Project]], §1.3 in *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;


Definition of weakly Tarski universes:

* {#Hofmann} [[Martin Hofmann]], section 2.1.6 of _Syntax and semantics of dependent types_ ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.8985))

* {#Luo12} [[Zhaohui Luo]], _Notes on Universes in Type Theory_, 2012 ([pdf](http://www.cs.rhul.ac.uk/home/zhaohui/universes.pdf))

* {#Gallozzi14} [[Cesare Gallozzi]], _Constructive Set Theory from a Weak Tarski Universe_, MSc thesis (2014) ([arXiv:1411.5591](https://arxiv.org/abs/1411.5591))


Detailed discussion of the type of types in [[Coq]] is in

* [[Adam Chlipala]], _[Certified programming with dependent types](http://adam.chlipala.net/cpdt/)_ -- _[Library Universes](http://adam.chlipala.net/cpdt/html/Universes.html)_ 

See also around slide 8 of the survey

* Frade, _Calculus of inductive constructions_ (2008/2009) ([pdf](http://www3.di.uminho.pt/~mjf/pub/SFV-CIC-2up.pdf))

A [[formal proof]] in [[homotopy type theory]] that the type of [[homotopy n-types]] is not itself a homotopy $n$-type (it is an $(n+1)$-type) is in 

* [[Nicolai Kraus]], [[Christian Sattler]], _The universe $\mathcal{U}_n$ is not an $n$-type_ May 2013 ([pdf](http://red.cs.nott.ac.uk/~ngk/universes.pdf))

[[(∞,1)-category theory|(∞,1)-Categorical]] semantics for [[univalence|univalent]] type universes is discussed in

* {#KapulkinLumsdaineVoevodsky12} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], [[Vladimir Voevodsky]], _The Simplicial Model of Univalent Foundations_ ([arXiv:1211.2851](http://arxiv.org/abs/1211.2851))

* {#Shulman13} [[Michael Shulman]], _The univalence axiom for elegant Reedy presheaves_ ([arXiv:1307.6248](http://arxiv.org/abs/1307.6248))

* {#GepnerKock12} [[David Gepner]], [[Joachim Kock]], _Univalence in locally cartesian closed ∞-categories_ ([arXiv:1208.1749](http://arxiv.org/abs/1208.1749))

Relation to [[injective types]]:

* {#Escardo19} [[Martín Escardó]], _Injectives types in univalent mathematics_ ([arXiv:1903.01211](https://arxiv.org/abs/1903.01211))


See also

* {#Rathjen} [[Michael Rathjen]], _The strength of Martin-L&#246;f type theory with superuniverse. Part I_ [pdf](https://www1.maths.leeds.ac.uk/~rathjen/Super.pdf)

* {#SEP} Stanford Encyclopedia of Philosophy,  _[Type theory -- Extensions of type systems, Polymorphism, Paradoxes](http://plato.stanford.edu/entries/type-theory/#6)_

* {#Luo11} [[Zhaohui Luo]], _Contextual analysis of word meanings in type-theoretical semantics_, in Pogodalla, Prost (eds.) _Logical Aspects of Computational Linguistics_, 2011 ([pdf](http://www.cs.rhul.ac.uk/home/zhaohui/LACL11.pdf))

[[!redirects type universes]]

[[!redirects type of types]]
[[!redirects types of types]]

[[!redirects universe of types]]
[[!redirects universes of types]]

[[!redirects type of small types]]
[[!redirects types of small types]]

[[!redirects universe of small types]]
[[!redirects universes of small types]]

[[!redirects universe in type theory]]
[[!redirects universes in type theory]]

[[!redirects universe type]]
[[!redirects universe types]]

[[!redirects Type]]