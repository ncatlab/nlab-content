
{:bluebox: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



This page on aspects of [[homotopy type theory]] is meant for readers who are interested in [[homotopy theory]] but not (necessarily) in [[formal logic]] and [[formal proof]]. This page is meant to help answer the question:

> I am a homotopy theorist; what can homotopy type theory do for me?

See also at _[[homotopy type theory FAQ]]_ the section _[Why should I care? -- For homotopy theorists](homotopy+type+theory+FAQ#WhyShouldICareForHomotopyTheorists)_.

Since homotopy theory takes place in [[model categories]] and similar categorical structures, the input from homotopy type theory is via its [[categorical semantics]]. In this sense the question which this page is meant to help to answer is

> I am a homotopy theorist; which methods can I learn from the [[categorical semantics of homotopy type theory]]?

For the moment this page will mostly list pointers with brief comments to other entries where details are given. You should maybe read it like an instructional exercise list and follow the pointers for help.

#Contents#
* table of contents
{:toc}



## Basic dictionary for the internal language
 {#BasicDictionary}

Starting from ([[(infinity,1)-category theory|homotopy]]) [[category theory]], 
the corresponding ([[homotopy type theory|homotopy]]) [[type theory]] is simply a formal language for denoting familiar constructions, as indicated in the following table.


|  ([[(infinity,1)-category theory|homotopy]]) [[category theory]] | ([[homotopy type theory|homotopy]]) [[type theory]] |
|----------------------|------------------|
|  [[semantics]]       | [[syntax]] |
| [[object]] $X$ | [[type]] $x : X$ |
| [[fibration]]([[display map]]) $\array{A \\ \downarrow^{\mathrlap{p}} \\ X}$  | [[dependent type]]  $x : X \vdash A(x) : Type$ |
| [[section]] $\array{ X &&\stackrel{t}{\to}&& A \\ & {}_{\mathllap{id}}\searrow && \swarrow_{p} \\ && X}$ | [[term]] $x : X \vdash t(x) : A(x)$ |
|  [[pullback]] $\array{ f^* A &\to& A \\ \downarrow && \downarrow^{\mathrlap{p}} \\ Y &\stackrel{f}{\to} & X }$ | [[substitution]] $y : Y \vdash A(f(y)) : Type$ |
| [[direct image]] $\array{ A && f_* A \\ {}^{\mathllap{p}}\downarrow && \downarrow ^{f_* p}\\ X &\stackrel{f}{\to}& Y}$ | [[dependent product]] $ y : Y \vdash \underset{x : X(y)}{\prod } A(x) : Type$ |
| [internal hom in slice](locally%20cartesian%20closed%20category#EquivalentCharacterizations) $\array{ X \times f^* A && f_* f^* A & = [X,A]_Y \\ {}^{\mathllap{}}\downarrow && \downarrow \\ X &\stackrel{f}{\to}& Y}$ | [[function type]] $ y : Y \vdash X(y) \to A(y) : Type$ |
| postcomposition $\array{ A &=& f_! A \\ \downarrow && \downarrow \\ X &\stackrel{f}{\to}& Y}$ | [[dependent sum]] $y : Y \vdash \underset{x : X(y)}{\sum} A(x) : Type$ |
| [[fiber product|fiber]][[product]] $\array{ X \times f^* A &=& f_! f^* A & = X \times_Y A\\ \downarrow && \downarrow \\ X &\stackrel{f}{\to}& Y}$ | [[product type]] $y : Y \vdash X(y) \times A(y) : Type$ |
| [[Beck-Chevalley condition]] of [[codomain fibration]] | [[substitution]] commutes with [[dependent sum]] |
| [[path space object]] $\array{A^I \\ \downarrow^{\mathrlap{(d_1,d_0)}} \\ A \times A}$ | [[identity type]] $a,b : A \vdash (a = b)$ |
| [[truncated object in an (infinity,1)-category|(-2)-truncated morphism]]/[[equivalence in an (infinity,1)-category|equivalence]] $\array{Y \\ \downarrow^{\mathrlap{\simeq}} \\ X}$ | [[true]]/[[unit type]] $x : X \vdash 1 : Type$ |
| [[truncated object in an (infinity,1)-category|(-1)-truncated morphism]]/[[monomorphism in an (infinity,1)-category|monomorphism]] $\array{\phi \\ \downarrow \\ X}$ | [[proposition]] $x : X \vdash \phi(x) : Type$ |
| [[direct image]] of [[truncated object in an (infinity,1)-category|(-1)-truncated morphism]] | [[universal quantifier]] $y : Y \vdash \underset{x \in X(y)}{\forall} \phi(x) : Type$ |
| [[truncated object of an (infinity,1)-category|(-1)-truncation]] of postcomposition of [[truncated object in an (infinity,1)-category|(-1)-truncated morphism]] | [[existential quantifier]] $y : Y \vdash \underset{x \in X(y)}{\exists} \phi(x) : Type$ |

The symbols in the right column may be formally manipulated according to the rules of _[[type theory]]_.
For the case of ordinary categories, this table defines a [[functor]] 

$$
  Lang : LocallyCartesianClosedCategories \to DependentTypeTheories
$$

from _[[locally cartesian closed categories]]_ to _[[dependent type theories]]_ that sends each category to its _[[internal language]]_. 

The important fact is that

+-- {: .num_theorem }
###### Theorem

The functor $Lang$ is an [[equivalence of categories]].

=--

This is discussed at _[[relation between type theory and category theory]]_. So the (dependent) type theory is just an equivalent way of talking about a (locally cartesian closed category).  

For the case of [[(∞,1)-categories]]/[[homotopy theories]] that we are interested in here, there remain some things to be fully worked out, but it is clear that we get an analogous construction

$$
  Lang : LocallyCartesianClosed(\infty,1)Categories \to HomotopyTypeTheory
$$

from [[locally cartesian closed (∞,1)-categories]] to [[homotopy type theory]] which is expected to be an [[equivalence of (∞,1)-categories]].

As the above table shows, from the perspective of [[dependent type theory]] [[categories]] $\mathcal{C}$ are regarded systematically via the collection of their [[slice categories]] (their associated "[[hyperdoctrines]]"). If $\mathcal{C}$ is a [[locally cartesian closed category]] then every [[morphism]] $f : X \to Y$ in $\mathcal{C}$ induces an [[adjoint triple]] of functors between the corresponding slice categories

+-- {: bluebox}
###### 

([[dependent sum]] $\dashv$ [[base change]] $\dashv$ [[dependent product]]) = $(\sum_f \dashv f^* \dashv \prod_f) : \mathcal{C}_{/X} \to \mathcal{C}_{/Y}$.

=--

Many familiar constructions are usefully expressed entirely in terms of these [[adjoint triples]]. For instance the [[internal hom]] in a slice category. 

While this is in principle clear/well known, the systematic use of the base change adjoint triple enforced by type theory turns out to lead to various elegant constructions that have not found much attention before, and which can be useful in applications.

## Homotopy pullbacks

The yoga of [[homotopy pullbacks]], [[homotopy fibers]], [[loop space objects]], [[fiber sequences]] etc. is basic to [[homotopy theory]], and of course is also fairly elementary. Homotopy type theory can hardly add a previously unknown fact here. Nevertheless, it is noteworthy that many of these constructions, elementary as they are, look _even simpler_ when formulated in homotopy type theory. 


|  [[category theory]] | [[type theory]] |
|---|---|
| [[homotopy pullback]] $\array{A \times_C^h B &\to& B \\ \downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{g}} \\ A &\stackrel{f}{\to}& X}$ | $\underset{a : A, b : B}{\sum} (f(a) = g(b))$ /  $\{ a : A, b : B ; (f(a) = g(b)) \}$  |
| [[homotopy fiber]] $\array{hfib(f) &\to& * \\ \downarrow &\swArrow_{\simeq}& \downarrow^{\mathrlap{}} \\ A &\stackrel{f}{\to}& X}$ | $\sum_{a : A} (f(a) = *)$ / $\{ a : A ; (f(a) = *) \}$  |
| [[mapping cocylinder]] $\array{ CoCyl(f) &\to& X \\ \downarrow && \downarrow^{\mathrlap{f}} \\ Y^I &\stackrel{d_0}{\to} & Y \\ \downarrow^{\mathrlap{d_1}} \\ Y } $ | $y : Y \vdash \underset{x : X}{\sum} (f(x) = y)$ |
| [[free loop space object]] $\array{\mathcal{L}X &\to& X \\ \downarrow &\swArrow_{\simeq}& \downarrow \\ X &\to& X \times X}$ | $\underset{x,y : X}{\sum} (x = y) and (x = y)$ |

* [[pasting law]] (...)


## Detecting $n$-truncation

The central insight (due to [[Vladimir Voevodsky]]) that boosts dependent type theory with identity types to genuine homotopy type theory is that in terms of [[identity types]] there are simple natural expressions for [[n-truncated|n-truncation]] and detection of $n$-truncation of objects and morphisms. Translated via [[categorical semantics]] to [[homotopy theory]], these formulas turn out to refomulate some basic yoga of model category computation in a new way that hasn't received attention before in homotopy theory, emphasizing the base change adjoint triple. 

| [[category theory]] | [[type theory]] |
|----|----|
| object $X$ is [[(-2)-truncated]]/[[contractible]] | [[isContr]]$(X) = \sum_{x : X} \prod_{y : X} (x = y)$ |
| morphism $X$ is [[(-2)-truncated]]/[[equivalence in an (infinity,1)-category|equivalence]] | [[isEquiv]]$(f) \coloneqq \prod_{x : {X}} isContr(hfiber(f,x) $ |
 
+-- {: .num_remark }
###### Remark

In the [[(∞,1)-category]] [[∞Grpd]] it is true that a morphism $f : X \to Y$ is an equivalence precisely if for all global points $y : * \to Y$ the corresponding homotopy fiber of $f$ is contractible. The same simple statement is not available _in the "external" logic_ for a general [[(∞,1)-category]], simply because there an object $Y$ may not even have enough global points (it may be non-trivial and have no global point). 

The above is useful in that it says that _in the [[internal logic]]_ of the $(\infty,1)$-category, the simple statement familiar form [[∞Grpd]] is true generally, after all. 

=--



## Homotopy algebras over homotopy monads
 {#Induction}

We have seen that homtopy type theory naturally describes 
[[homotopy pullbacks]] and some other finite [[(∞,1)-limits]] in terms of [[identity types]] and the [[base change]] [[adjoint triple]]. The [[duality|dual]] notion, _[[homotopy colimits]]_, is conceived of in homotopy type theory as a (vast) generalization of the basic notion of _[[induction]]_ and _[[recursion]]_, subsumed type-theoretically in the notion of _[[inductive type]]_, roughly a kind of [[type]] that is given by [[generators and relations]].

Traditionally inductive types are in category theory [[categorical semantics|interpreted]] as _[[algebras over an endofunctor]]_. While useful, this is a concept somewhat alien to usual constructions in category theory or homotopy theory. The natural notion is instead that of an [[algebra over a monad]]. While an [[algebra over an endofunctor]] may be thought of as a monad-algebra over a [[free monad]], from the point of view of homotopy theory it still seems unnatural to restrict attention to free monads.

However, after generalization to _[[homotopy type theory]]_ this is rectified: here the homotopy-theoretic notion of [[induction]] turns out to be about [[∞-algebras over an (∞,1)-monad]], as one would hope, and a _[[higher inductive type]]_ is an [[initial algebras of a presentable (∞,1)-monad]].

(...)
  


## Detecting $n$-connectedness

| [[category theory]] | [[type theory]] |
|--|--|
| [[n-connected object of an (infinity,1)-topos|(-1)-connected object]]/ [[inhabited object]] $X$ | $isInhab(X) \coloneqq ...$ |
| [[n-connected object of an (infinity,1)-topos|(-1)-connected morphism]]/ [[effective epimorphism in an (infinity,1)-category|effective epimorphism]] $f : X \to Y$ | $\prod_{y : Y} isInhab(\sum_{x : X} (f(x) = y))$ |

## Homotopy pushouts

| [[category theory]] | [[type theory]] |
|---|---|
| [[homotopy pushout]] $\array{ C &\stackrel{g}{\to}& B \\ {}^{\mathllap{f}}\downarrow &\swArrow_{\simeq}& \downarrow \\ A &\to&  A \coprod_C^h B}$ | $hpushout (A\,B\,C : Type) (f : C \to A) (g : C \to B) : Type \coloneqq \left\{ \array{inl : B \to hpushout(f,g) \\ inr : A \to hpushout(f,g) \\ glue \prod_{c : C} (inl(f(c)) = inr(g(c)))} \right.$  |

(...)

## Constructing $n$-truncation

| [[category theory]] | [[type theory]] |
|---|---|
| [[truncated object in an (infinity,1)-category|(-1)-truncation]] $\tau_{-1}(-)$ | $supp(X : Type) : Type \coloneqq \left\{ \array{ proj : X \to supp X \\ \underset{x, y : supp X}{\prod} (x = y) }\right.  $ |

## Specific HoTT proofs in homotopy theory

We list in the following theorems in homotopy theory together with such proofs of them in terms of homotopy type theory language that are either new (to the best of our knowledge), or else that are at least considerably simpler than earlier proofs with traditional homotopy theory tools.

### Blakers-Massey theorem

see at _[[Blakers-Massey theorem]]_

### Essential uniqueness of group units

(...)

### Equivalence of notions of stabilizer $\infty$-groups

(...) [...](http://nforum.mathforge.org/discussion/3454/stabilizer-subgroup/?Focus=28287#Comment_28287)

(...)