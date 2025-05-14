+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Mere Propositions
* table of contents
{: toc}

## Idea

In [[homotopy type theory]], the notion of **mere proposition** is an internalization of the notion of [[proposition]] / [[(-1)-truncated]] object.  Mere propositions are also called **h-propositions**, types of [[h-level]] $1$, $(-1)$-[[truncated types]], or even just **propositions** if no ambiguity will result.  Semantically, mere propositions correspond to [[(-1)-groupoids]] or more generally [[(-1)-truncated objects]].

Mere propositions are one way to embed [[logic]] into homotopy type theory, via the [[propositions as some types]] / [[bracket types]] approach.  For many purposes, this is the "correct" way to embed logic (as opposed to the [[propositions as types]] approach --- for instance, the PAT version of [[excluded middle]] contradicts the [[univalence axiom]], whereas the mere-propositional version does not).

## Definition

Consider [[intensional type theory|intensional]] [[type theory]] with [[dependent sums]], [[dependent products]], and [[identity types]].  

There are many equivalent definitions of a [[type]] being an _h-proposition_.  Perhaps the simplest is as follows. 

+-- {: .num_defn}
###### Definition

For $A$ a type, let $isProp(A)$ denote the [[dependent product]] of the [[identity types]] for all pairs of [[terms]] of $A$:

$$ isProp(A) \coloneqq \prod_{x\colon A} \prod_{y\colon A} (x=y) $$

We say that $A$ is an h-proposition if $isProp(A)$ is an [[inhabited type]].

=--

In [[propositions as types]] language, this can be pronounced as "every two elements of $A$ are equal".


+-- {: .num_prop}
###### Proposition

The following are provably [[equivalence in homotopy type theory|equivalent]] definitions of $isProp(A)$:

* $isProp(A) \coloneqq \prod_{x\colon A} \prod_{y\colon A} isContr(x=y) $
* $ isProp(A) \coloneqq (A \to isContr(A)) $
* $isProp(A) \coloneqq \mathrm{isEquiv}(\mathrm{const}_{\mathbb{2}, A})$
* $isProp(A) \coloneqq \prod_{f:\mathbb{2} \to A} f(0) = f(1)$
* $isProp(A) \coloneqq \prod_{f:\mathbb{2} \to A} isContr(f(0) = f(1))$
* $isProp(A) \coloneqq \prod_{f:\mathbb{2} \to A} \prod_{x:\mathbb{2}} \prod_{y:\mathbb{2}} f(x) = f(y)$
* $isProp(A) \coloneqq \prod_{f:\mathbb{2} \to A} \sum_{p:\mathbb{I} \to A} \prod_{x:\mathbb{2}} p(\mathrm{rec}_\mathbb{2}^\mathbb{I}(0_\mathbb{I}, 1_\mathbb{I})(x)) = f(x)$

=--

The first fits into the general [[inductive definition]] of [[n-groupoid]]: an $\infty$-groupoid is an $n$-groupoid if all its hom-groupoids are $(n-1)$-groupoids. 

The second says that being a proposition is equivalent to being "[[contractible]] if [[inhabited]]", and when [[isContr]] is expanded out to $\sum_{x:A} \prod_{y:A} x =_A y$, the resulting type $A \to \sum_{x:A} \prod_{y:A} x =_A y$ is just the type of the [[graph of a dependent function|graphs of dependent functions]] of $\prod_{x:A} \prod_{y:A} x =_A y$. 

The third states that being a proposition is the same as being a $\mathrm{bool}$-[[localization of a type|local type]]: the function 
$$\mathrm{const}_{\mathbb{2}, A} \equiv \lambda x:A.\lambda b:v.x:A \to (\mathrm{bool} \to A)$$ 
which takes elements $x:A$ to [[constant functions]] from the [[type of booleans]] with value $x$ is an [[equivalence of types]]. 

The fourth states that being a proposition is equivalent to the condition that for every function from the [[type of booleans]], $f(0) = f(1)$, and is interderivable from the usual definition of isProp via the recursion principle of the type of booleans. 

The fifth states that being a proposition is equivalent to the condition that for every function from the [[type of booleans]], $f(0) = f(1)$ is contractible, and is interderivable from the first via the recursion principle of the type of booleans. 

The sixth states that being a proposition is equivalent to the condition that every function from the [[type of booleans]] is a [[weakly constant function]], and can be proven to be equivalent to the fourth via double induction on the type of booleans and the properties of identity types. 

The seventh states that being a proposition is equivalent to the condition that every function from the [[type of booleans]] to $A$ factors through the [[interval type]] via the function $\mathrm{rec}_\mathbb{2}^\mathbb{I}(0_\mathbb{I}, 1_\mathbb{I}):\mathbb{2} \to \mathbb{I}$ defined by the recursion principle of the type of booleans. 

### Rules for isProp

The usual definition of isProp is given by the following rules:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{isProp}(A) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{isProp}(A) \equiv \prod_{x:A} \prod_{y:A} x =_A y \; \mathrm{type}}$$

If the [[dependent type theory]] doesn't have [[dependent function types]], but still has [[identity types]] one could still define isProp by adding the formation, introduction, elimination, computation, and uniqueness rules for isProp:

Formation rules for isProp types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A, y:A \vdash x =_A y \; \mathrm{type}}{\Gamma \vdash \mathrm{isProp}(A) \; \mathrm{type}}$$

Introduction rules for isProp types:
$$\frac{\Gamma, x:A, y:A \vdash p(x, y):x =_A y}{\Gamma \vdash \lambda(x).\lambda(y).p(x, y):\mathrm{isProp}(A)}$$

Elimination rules for isProp types:
$$\frac{\Gamma \vdash p:\mathrm{isProp}(A) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A}{\Gamma \vdash p(a, b):a =_A b}$$

Computation rules for isProp types:
$$\frac{\Gamma, x:A, y:A \vdash p(x, y):x =_A y \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A}{\Gamma \vdash \beta_\mathrm{isProp}:(\lambda(x).\lambda(y).p(x, y))(a, b) =_{a =_A b} p(a, b)}$$

Uniqueness rules for isProp types:
$$\frac{\Gamma \vdash p:\mathrm{isProp}(A)}{\Gamma \vdash \eta_\mathrm{isProp}:p =_{\mathrm{isProp}(A)} \lambda(x).\lambda(y).p(x, y)}$$

## Properties

* We can prove that for any $A$, the type $isProp(A)$ is an h-proposition, i.e. $isProp(isProp(A))$.  Thus, any two inhabitants of $isProp(A)$ (witnesses that $A$ is an h-proposition) are "equal".

* Every function between h-propositions $A$ and $B$ is an [[embedding of types]]. 

* If $A$ and $B$ are h-props and there exist maps $A\to B$ and $B\to A$, then $A$ and $B$ are [[equivalence of types|equivalent]]. This follows from the fact that if $A$ and $B$ are types and there exists embeddings $A\to B$ and $B\to A$, then $A$ and $B$ are equivalent. 

### Relation to the principles of omniscience

Suppose that $A$ is a mere proposition. Then $A$ is [[equivalence of types|equivalent]] to the [[existential quantifier]] $\exists x:A.(\lambda t.1)(x) = 1$, where $\lambda t.1$ is the [[constant function]] from $A$ to the [[booleans]] which takes elements of $A$ to the boolean $1:\mathrm{bool}$. Then, one can show that various [[principles of omniscience]] are equivalent to weak versions of excluded middle, via the special case of the constant function $\lambda t.1$: 

* That the [[limited principle of omniscience]] holds for all mere propositions is equivalent to [[excluded middle]]:

$$\left(\prod_{A:\mathrm{Prop}} \prod_{f:A \to 2} \exists x:A.f(x) = 1 \vee \neg (\exists x:A.f(x) = 1)\right) \simeq \left(\prod_{A:\mathrm{Prop}} A \vee \neg A\right)$$

* That the [[weak limited principle of omniscience]] holds for all mere propositions is equivalent to [[weak excluded middle]]:

$$\left(\prod_{A:\mathrm{Prop}} \prod_{f:A \to 2} \neg (\exists x:A.f(x) = 1) \vee \neg \neg (\exists x:A.f(x) = 1)\right) \simeq \left(\prod_{A:\mathrm{Prop}} \neg A \vee \neg \neg A\right)$$

* That the [[lesser limited principle of omniscience]] holds for all mere propositions is equivalent to [[de Morgan's law]]:

$$\left(\prod_{A:\mathrm{Prop}} \prod_{B:\mathrm{Prop}} \prod_{f:A \to 2} \prod_{g:B \to 2} \neg ((\exists x:A.f(x) = 1) \wedge (\exists x:B.g(x) = 1)) \to (\neg (\exists x:A.f(x) = 1) \vee \neg (\exists x:B.g(x) = 1))\right) \simeq \left(\prod_{A:\mathrm{Prop}} \prod_{B:\mathrm{Prop}} \neg (A \wedge B) \to (\neg A) \vee (\neg B)\right)$$

* That [[Markov's principle]] holds for all mere propositions is equivalent to the [[double negation law]]:

$$\left(\prod_{A:\mathrm{Prop}} \prod_{f:A \to 2} \neg \neg (\exists x:A.f(x) = 1) \to \exists x:A.f(x) = 1\right) \simeq \left(\prod_{A:\mathrm{Prop}} \neg \neg A \to A\right)$$

## Categorical semantics

We discuss the [[categorical semantics]] of h-propositions.

Let $\mathcal{C}$ be a [[locally cartesian closed category]] with [[categorical semantics of homotopy type theory|sufficient structure]] to interpret all the above type theory.  This means that $C$ has a [[weak factorization system]] with [[stable path objects]], and that [[trivial cofibrations]] are preserved by pullback along fibrations between fibrant objects.  (We ignore questions of [[coherence]], which are not important for this discussion.)

Then for a fibrant object $A$, the object $isProp(A)$ defined above (with the first definition) is obtained by taking [[dependent product]] of the path-object $A^I \to A\times A$ along the projection $A\times A\to 1$.  By [[adjunction]], a [[global element]] of $isProp(A)$ is therefore equivalent to a [[section]] of the path-object, which exactly means a (right) [[homotopy]] between the two projections $A\times A\;\rightrightarrows\; A$.  The existence of such a homotopy, in turn, is equivalent to saying that *any two maps $X\;\rightrightarrows\; A$ are homotopic*.

More generally, we may apply this locally.  Suppose that $A\to B$ is a fibration, which we can regard as a dependent type
$$x\colon B \vdash A(x)\colon Type.$$
Then we have a dependent type
$$x\colon B \vdash isProp(A(x))\colon Type$$
represented by a fibration $isProp(A)\to B$.  By applying the above argument in the [[slice category]] $\mathcal{C}/B$, we see that $isProp(A)\to B$ has a [[section]] exactly when any two maps in $\mathcal{C}/B$ into $A\to B$ are homotopic over $B$.  We can also construct the type
$$\prod_{x\colon B} isProp(A(x))$$
in global context, which has a global element precisely when $isProp(A)\to B$ has a section.


## Related concepts

* [[subsingleton]], [[subterminal object]]

* [[propositional truncation]]

* [[isEquiv]]

* [[isContr]]

* **isProp**

* [[center of contraction]]

* [[propositional logic as a dependent type theory]]

* [[coinduction]]

* [[strict proposition]]

[[!include homotopy n-types - table]]

## References

* [section 3.3](http://planetmath.org/33merepropositions) of [[Homotopy Type Theory -- Univalent Foundations of Mathematics]]

* [HoTT repository](https://github.com/HoTT/HoTT/blob/master/Coq/HLevel.v)

[[!redirects mere propositions]]
[[!redirects h-proposition]]
[[!redirects h-propositions]]
[[!redirects h-prop]]
[[!redirects h-props]]
[[!redirects hProp]]
[[!redirects hProps]]
[[!redirects h-level 1]]
[[!redirects h-level 1 type]]
[[!redirects h-level 1 types]]
[[!redirects isProp]]
[[!redirects (-1)-truncated type]]
[[!redirects (-1)-truncated types]]

[[!redirects merely]]
