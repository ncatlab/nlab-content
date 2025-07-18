
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

There are various different paradigms for the interpretation of 
[[predicate logic]] in [[type theory]].  In "logic-enriched type theory", there is a separate class of "[[propositions]]" from the class of "[[types]]".  But we can also identify propositions with particular types.  In the _[[propositions as types]]_-paradigm, every proposition is a type, and also every type is identified with a proposition (the proposition that it is an [[inhabited type]]).

By contrast, in the paradigm that may be called [[propositions as some types]], every proposition is a type, but not every type is a proposition.  The types which are propositions are generally those which "have at most one inhabitant" --- in [[homotopy type theory]] this is called being of [[h-level 1]] or being a [[homotopy n-type|(-1)-type]].  This paradigm is often used in the [[categorical semantics]] of type theory, such as the [[internal logic]] of various kinds of categories.

Under "propositions as types", all type-theoretic operations represent corresponding logical operations ([[dependent sum]] is the [[existential quantifier]], [[dependent product]] the [[universal quantifier]], and so on).  However, under "propositions as some types", not every such operation preserves the class of propositions; this is particularly the case for [[dependent sum]] and [[disjunction]]([[or]]).  Thus, in order to obtain the correct logical operations, we need to reflect these constructions back into propositions somehow, finding the "underlying proposition", corresponding to the [[truncated|(-1)-truncation]]/[[h-level 1|h-level 1-projection]].  This operation in type theory is called the **bracket type** (when denoted $[A]$); in [[homotopy type theory]] it can be identified with the [[higher inductive type]] $isInhab$.

## Definition
 
### As a higher inductive type
{#AsHigherInductiveType}

In any [[dependent type theory]] with [[identity types]], given type $A$, the **support**  of $A$ denoted $supp(A)$ or $isInhab(A)$ or $\tau_{-1} A$ or $\| A \|_{-1}$ or $\| A \|$ or, lastly, $[A]$, is the [[higher inductive type]] defined by the two constructors

$$
  a \colon A \;\vdash \; isinhab(a) \colon supp(A)
$$

$$
  x \colon supp(A) \;,\; y \colon supp(A)
  \;\vdash \;
  inpath(x,y) \colon (x = y)
 \,,
$$

where in the last [[sequent]] on the right we have the [[identity type]]. ([Voevodsky](#Voevodsky), [1Lab](#1Lab))

This says that $supp(A)$ is the type which is [[universal property|universal]] with the property that the [[terms]] of $A$ map to it and that any two term of $A$ become [[equivalence in homotopy type theory|equivalent]] in $supp(A)$.

In [[Agda]] [[syntax]] this is

    data isinhab {i : Level} (A : Set i) : Set i where
      inhab : A → isinhab A
      inhab-path : (x y : isinhab A) → x ≡ y

The [[recursion principle]] for $supp(A)$ says that if $B$ is a [[mere proposition]] and we have $f: A \to B$, then there is an induced $g : supp(A) \to B$ such that $g(isinhab(a)) \equiv f(a)$ for all $a:A$. In other words, any mere proposition which follows from (the inhabitedness of) $A$ already follows from $supp(A)$. Thus, $supp(A)$, as a mere proposition, contains no more information than the inhabitedness of $A$.

The [[induction principle]] states that if we have a family of mere propositions $B(x)$ indexed by $x:A$ and we have $f:\prod_{x:A} B(isinhab(x))$, then there is an induced $g:\prod_{z:supp(A)} B(z)$ such that $g(isinhab(a)) \equiv f(a)$ for all $a:A$. 

#### Inference rules

The inference rules for bracket types are as follows:

* Formation rules for bracket types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash [A] \; \mathrm{type}}$$

* Introduction rules for bracket types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:A \vdash [x]:[A] \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, x:[A], y:[A] \vdash \mathrm{trunc}_A(x, y):x =_{[A]} y \; \mathrm{type}}$$

* Elimination rules for bracket types:

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash p:\prod_{x:A} \prod_{y:B(x)} \prod_{z:B(x)} y =_{B(x)} z \quad \Gamma \vdash f:\prod_{x:A} B([x])}{\Gamma, x:[A] \vdash \mathrm{ind}_{[A]}^{B(-)}(p, f, x):B(x)}$$

* Computation rules for bracket types

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma \vdash p:\prod_{x:A} \prod_{y:B(x)} \prod_{z:B(x)} y =_{B(x)} z \quad \Gamma \vdash f:\prod_{x:A} B([x]) \quad \Gamma \vdash a:A}{\Gamma \vdash \mathrm{ind}_{[A]}^{B(-)}(p, f, [a]) \equiv f(a):B([a])}$$

### With a type of all propositions

Suppose the [[dependent type theory]] has a [[univalent]] [[type of all propositions]] $(\mathrm{Prop}, \mathrm{El})$. Then the bracket type of $A$ could be defined as the type

$$[A] \coloneqq \prod_{P:\mathrm{Prop}} (A \to \mathrm{El}(P)) \to \mathrm{El}(P)$$

### As localization

Let $\mathbb{1}$ be the [[unit type]] and let $\mathbb{2}$ be the [[type of booleans]]. The bracket type of a type $A$ is the [[localization of a type at a family of functions|localization]] of $A$ at the unique function $\mathbb{2} \to \mathbb{1}$. 

$$\left[A\right] \coloneqq L_\mathbb{2}(A)$$

By definition, the type of functions $(\mathbb{1} \to \left[A\right]) \to (\mathbb{2} \to \left[A\right])$ is an [[equivalence of types]]. 

This is the special case of the [[n-truncation modality]] as the [[n-truncation modality]] is localization at the unique map from the $(n + 1)$-dimensional sphere type to the unit type, and $\mathbb{2}$ is the zero-dimensional [[sphere type]]. 

For more see at _[[n-truncation modality]]_.

### As a sequential colimit

Let $A * B$ denote the [[join type]] of $A$ and $B$, and let $A^{*(n)}$ be the iterated join type, inductively defined on the natural numbers by $A^{*(0)} \coloneqq \emptyset$ and $A^{*(n + 1)} \coloneqq A^{*(n)} * A$. 

Then the propositional truncation of $A$ is the [[sequential colimit]] of the sequence of functions 

$$A^{*(0)} \overset{\mathrm{inr}}\to A^{*(1)} \overset{\mathrm{inr}}\to A^{*(2)} \overset{\mathrm{inr}}\to \ldots$$

### As a quotient set

Let $A$ be a type and $R(x, y)$ be a binary family of [[contractible types]] indexed by $x:A$ and $y:A$, so that the product projection function for the dependent sum type

$$p_1:\left(\sum_{z:A \times A} R(\pi_1(z), \pi_2(z))\right) \to (A \times A)$$

is an [[equivalence of types]]. Then the propositional truncation of $A$ is the [[quotient set]] $A / R$. (The quotient set in [[dependent type theory]] can be defined using inference rules without propositional truncations.)

### Using hubs and spokes

In section 7.3 of the [[HoTT Book]] [UFP13](#UFP13), the authors give another definition of the propositional truncation using the hubs and spokes construction developed in section 6.7. Since the [[type of booleans]] is the zero-[[dimensional]] [[sphere]], the propositional truncation of $A$ is a [[higher inductive type]] generated by 

* A function $[-]:A \to [A]$

* For each function $r:\mathrm{bool} \to A$, a hub point $h(r):A$

* For each function $r:\mathrm{bool} \to A$ and each boolean $x:\mathrm{bool}$, a spoke path $s_r(x):r(x) =_A h(r)$

## Semantics

One presentation of the [[internal logic|internal]] [[type theory]] of 
[[regular categories]] consists of [[dependent type theory]] with the [[unit type]], 
[[strong extensional equality types]], strong [[dependent sums]], and bracket types.  (The internal logic of a regular category can alternatively be presented as a [[logic-enriched type theory]].)

The [[semantics]] of bracket types in a [[regular category]] $C$ is as follows.

A [[dependent type]] (a type in [[context]] $X$)

$$x\colon X \vdash A(x) \colon Type$$

is interpreted in $C$ as an arbitrary [[morphism]]


$$
  \array{
    A
    \\  
    \downarrow
    \\
    X
  }
  \,.
$$

The corresponding bracket type

$$ x\colon X \vdash [A(x)] \colon Type $$

is interpreted then as the [[image]]-[[(epi, mono) factorization system|factorization]] 

$$
  \array{
     A &&\to&& [A] & := im(A \to X)
     \\
     & \searrow && \swarrow
     \\
     && X
    \,.
  }
$$

Therefore $[A] \to X$ is a [[monomorphism]], and hence the interpretation of a [[proposition]] about the elements of $X$.


## Related concepts

* [[image]], [[inhabited type]]

* [[cone type]], [[bracket type]], [[set truncation]]

* [[n-truncation modality]]

* [[weakly constant function]]

* [[propositional truncation object]]

[[!include homotopy n-types - table]]

## References

The original articles are

* M.E. Maietti, _The Type Theory of Categorical Universes_ PhD thesis, Universit&#224; Degli Studi di Padova, 1998

(which speaks of "mono types") and

* [[Frank Pfenning]], _Intensionality, extensionality, and proof irrelevance in modal type theory_, In Proceedings of the 16th Annual Symposium on Logic in Computer Science (LICS'01), June 2001. 

* [[Steve Awodey]], [[Andrej Bauer]], *Propositions as $[$Types$]$*, Journal of Logic and Computation, **14**  (2004) 447-471 &lbrack;[doi:10.1093/logcom/14.4.447](https://doi.org/10.1093/logcom/14.4.447), [pdf](http://andrej.com/papers/brackets_letter.pdf)&rbrack;

Discussion in the context of [[homotopy type theory]]:

* {#UFP13} [[Univalent Foundations Project]], §3.7 *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;


Exposition:

* {#Shulman} [[Mike Shulman]], _Minicourse on homotopy type theory_ (2012) ([web](http://www.sandiego.edu/~shulman/hottminicourse2012/))

Formalization:

* {#Voevodsky} [[Vladimir Voevodsky]], _The hProp version of the "inhabited" construction._ ([web](http://www.math.ias.edu/~vladimir/Foundations_library/hProp.html#lab140))

* {#1Lab} [[1lab]], *[Propositional truncation](https://1lab.dev/1Lab.HIT.Truncation.html)*

Discussion in the more general context of [[n-truncation modality|$n$-truncations]]:

* [[Guillaume Brunerie]], _Truncations and truncated higher inductive types_ ([web](http://homotopytypetheory.org/2012/09/16/truncations-and-truncated-higher-inductive-types/))

More on the [[universal property]] of propositional truncation:

* [[Nicolai Kraus]], *The General Universal Property of the Propositional Truncation*, in *TYPES 2014* Leibniz International Proceedings in Informatics (LIPIcs) **39** (2015) &lbrack;[arXiv:1411.2682](https://arxiv.org/abs/1411.2682), [doi:10.4230/LIPIcs.TYPES.2014.111](https://doi.org/10.4230/LIPIcs.TYPES.2014.111)&rbrack;

For propositional truncations as sequential colimits, see section 26.5 of

* {#RijkeDraft22} [[Egbert Rijke]] (2022), *[[Introduction to Homotopy Type Theory]]*, draft. ([pdf](https://raw.githubusercontent.com/martinescardo/HoTTEST-Summer-School/main/HoTT/hott-intro.pdf))

as well as section 16.2 of the lecture notes:

* [[Egbert Rijke]], *The homotopy image of a map*, Lecture 16 in: *[[Introduction to Homotopy Type Theory]]*, lecture notes, CMU (2018) &lbrack;[pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]], [webpage](https://www.andrew.cmu.edu/user/erijke/hott/)&rbrack;

For [[n-truncations]] as [[localizations]] at [[sphere types]], see:

* [[David Jaz Myers]], Orbifolds as microlinear types in synthetic differential cohesive homotopy type theory ([arXiv:2205.15887](https://arxiv.org/abs/2205.15887))

That propositional truncations with judgmental computation rules along with the [[type of booleans]] imply function extensionality:

* [[Nicolai Kraus]], [[Martín Escardó]], [[Thierry Coquand]], [[Thorsten Altenkirch]], *Notions of Anonymous Existence in Martin-Löf Type Theory*,  Logical Methods in Computer Science **13** 1 &lbrack;<a href="https://doi.org/10.23638/LMCS-13(1:15)2017">doi:10.23638/LMCS-13(1:15)2017</a>, [arXiv:1610.03346](https://arxiv.org/abs/1610.03346)&rbrack;

[[!redirects bracket type]]
[[!redirects bracket types]]

[[!redirects propositional truncation]]
[[!redirects propositional truncations]]
[[!redirects propositionally truncated]]
[[!redirects isInhab]]

