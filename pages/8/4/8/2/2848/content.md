
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

In [[logic]], a __proposition__ is intended to be interpreted [[semantics|semantically]] as having a [[truth value]].  In modern logic, it's cleanest to start by specifying a [[context]] and considering the propositions *in* that context.


## Predicates

If (in a given context $\Gamma$) we have a [[type]] $A$, then we may extend $\Gamma$ to a context $\Delta \coloneqq \Gamma, x\colon A$ (assuming that the [[variable]] $x$ is not otherwise in use).  We may then think of any proposition in $\Delta$ as a __predicate__ $P$ in $\Gamma$ with the __free variable__ $x$ of type $A$; this generalises to more complicated extensions of contexts (say by several variables).

If $P$ is a predicate with free variable $x$ of type $A$ and $t$ is a [[term]] of type $A$, then we get a proposition $P[t/x]$ by substituting $t$ for every instance of $x$ in $P$.  Conversely, any proposition $Q$ may be interpreted as a predicate $Q[\hat{x}]$ in which the free variable $x$ simply doesn't appear.  (We have $Q[\hat{x}][t/x] = Q$ for every term $t$.)

There is a more traditional approach of viewing a predicate as a [[function]] from terms to propositions, a __propositional function__.  Then $P[t/x]$ is written $P(t)$, while $P$ itself from above is written $P(x)$ (since a variable is a term).  In this approach, less care is usually taken with the context, so that $Q[\hat{x}]$ may be conflated with $Q$ (since $Q[\hat{x}](x) = Q$, or this would be so if $x$ were a term in $\Gamma$ instead of only in $\Delta$). 

From a higher-categorical point of view, predicates could be viewed as an [[indexed family]] of propositions with index object $I$ and function $P:I \rightarrow Prop$, the [[(-1)-groupoid]] version of the indexed family of [[set|sets]] found in [[set theory]] with index object $I$ and [[functor]] $S:I \rightarrow Set$ and the indexed family of [[groupoid|groupoids]] found in [[groupoid theory]] with index object $I$ and [[2-functor]] $G:I \rightarrow Grpd$.

## In category-theoretic logic

In [[category-theoretic logic|categorial logic]]/[[categorical semantics]], we have a [[category]] $\mathcal{C}$ and a [[class of monomorphisms]] (often all [[monomorphisms]]) $\mathcal{M}$ in $\mathcal{C}$.  Then a __context__ is an [[object]] of $\mathcal{C}$ and a __proposition__ in the context $\Gamma$ is an $\mathcal{M}$-[[subobject]] of $\Gamma$.  We also have a class of [[display maps]] (often all [[morphisms]] in $\mathcal{C}$) such that $\mathcal{M}$ is closed under [[pullbacks]] both along display maps and along [[sections]] of display maps.  These two ways of pulling back propositions in one context to propositions in another context correspond (respectively) to forming $Q[\hat{x}]$ and $P[t/x]$.

More specifically, if $\mathcal{C}$ is a [[finitely complete category]], then the objects of $\mathcal{C}$ may equivalently be viewed as contexts and as types in the [[internal language]] of $\mathcal{C}$; a morphism from $\Gamma$ to $A$ is a term of type $A$ in context $\Gamma$.  The extension of $\Gamma$ by a variable $x$ of type $A$ is the [[product]] $\Gamma \times A$, and the display map to $\Gamma$ is simply the projection.  Every term $t\colon \Gamma \to A$ defines a section of this display map, and we may literally construct $Q[\hat{x}]$ and $P[t/x]$ as pullbacks.

If $\mathcal{C}$ is even a [[topos]], then a proposition $Q$ in $\Gamma$ may be identified with a term whose type is the [[subobject classifier]] $\Omega$, and the predicate $Q[\hat{x}]$ is the [[composite]] $\Gamma \times A \to \Gamma \to \Omega$.  Given a term $t\colon \Gamma \to A$ and a predicate $P\colon \Gamma \times A \to \Omega$, the proposition $P[t/x]$ is the composite $\Gamma \to \Gamma \times A \to \Omega$.  Internalising a bit (by [[currying]]), we may view $Q$ as a [[global element]] $1 \to \Omega^\Gamma$ and $P$ as a [[morphism]] $A \to \Omega^\Gamma$, recovering the view that predicates are proposition-valued 'functions' (morphisms).

In general, we may intuitively think of an object $A$ in the [[slice category]] $\mathcal{C}/\Gamma$ as the 'set' (object) of possible values of terms $t$ of type $A$ in context $\Gamma$, and think of a predicate $P$ with a free variable of type $A$ (in the same context) as being the 'subset' (subobject) on those $t$ for which the statement $P(t)$ is [[true]].

## In type theory
 {#InTypeTheory}

In [[type theory]] under the _[[propositions as types]]_ paradigm, every [[type]] represents the proposition that it is [[inhabited type|inhabited]]. Hence the types which have at most one term may be identified with propositions ("propositions as some types"). In [[homotopy type theory]] these are the [[(-1)-types]]. The [[reflective subuniverse|reflection]] that sends types to their underlying proposition qua [[(-1)-truncation]] is the [[n-truncation modality]] for $n = (-1)$, also called [[bracket type]]-formation.


## Propositional and predicate logic

In [[propositional logic]], we fix a single context (considered the [[empty context]]) and consider the logic of propositions in that context.  In [[predicate logic]], we fix the empty context but work also in extensions of that context by free variables.  Predicate logic uses [[quantifiers]] as a way to move between contexts, more specifically to move from a predicate $P$ in a given context $\Gamma$ (which is a proposition in some extension of $\Gamma$) to a proposition in $\Gamma$.  The free variables in the predicate still appear in the written form of the proposition, but they are now *bound* variables and are not free in the proposition\'s context; some logicians prefer to systematically replace bound variables with numbered placeholders (especially when defining [[Gödel number]]s and the like).

## Related concepts

* [[property]]

* [[mere proposition]]

* [[type of propositions]], [[bracket type]], [[h-proposition]]

* [[propositional extensionality]]

* [[theory]]

* **proposition**/[[type]] ([[propositions as types]]) 

* [[definition]]/[[proof]]/[[program]] ([[proofs as programs]])

* [[theorem]], [[axiom]]

* [[conjecture]], [[folklore]]

[[!redirects proposition]]
[[!redirects propositions]]

[[!redirects predicate]]
[[!redirects predicates]]
[[!redirects propositional function]]
[[!redirects propositional functions]]
