
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

_Dependent type theory_ is the flavor of [[type theory]] that admits _[[dependent types]]_.

Its [[categorical semantics]] is in [[locally cartesian closed categories]] $C$, where a [[dependent type]]

$$
  x : X \vdash E(x) \; \mathrm{type}
$$

is interpreted as a [[morphism]]  $E \to X$, hence an [[object]] in the [[slice category]] $C_{/X}$.

Then change of [[context]] corresponds to [[base change]] in $C$. See also _[[dependent sum]]_ and _[[dependent product]]_.

Dependent type systems are heavily used for _[[certified programming|software certification]]_. 

## In the foundations of mathematics

Dependent type theory itself support various [[foundations of mathematics]] via the [[propositions as some types]] interpretation of [[dependent type theory]], where propositions are the types where every two elements are equal 

$$\mathrm{isProp}(A) \coloneqq \prod_{x:A} \prod_{y:A} x =_A y$$

Suppose that a dependent type theory has a separate [[type]] [[judgment]] as well as [[dependent product types]], [[dependent sum types]], [[identity types]], [[weak function extensionality]], [[propositional truncations]], [[empty type]], [[unit type]], [[sum types]]. All the operations in [[predicate logic]] are derivable from said type formers: 

* [[universal quantification]] is the dependent product type of families of propositions due to weak function extensionality

* similarly, [[implication]] is the function type of two propositions due to weak function extensionality, and function types are just dependent product types of a constant family of types

* [[logical conjunction]] is the product type of two propositions, and product types are just dependent sum types of a constant family of types

* [[existential quantification]] is the propositional truncation of dependent sum types

* [[logical disjunction]] is the propositional truncation of sum types

* [[falsehood]] is the empty type

* [[truth]] is the unit type

* [[excluded middle]] and the [[law of double negation]] is stated as an [[inference rule]] about propositions

Then 

* One can add a [[cumulative hierarchy]] to the dependent type theory and work entirely in the cumulative hierarchy for [[material set theory]]

* One can add a [[category of sets]] to the dependent type theory and work entirely in the category of sets for [[structural set theory]]

* One can add a [[type universe]] satisfying certain [[axioms]] and [[axiom schemata]], such as [[universe extensionality]], closure under identity types, closure under dependent sum types, closure under dependent product types, [[propositional resizing]], [[axiom of replacement|replacement]], [[axiom of infinity|infinity]], and [[axiom of choice|choice]], to the dependent type theory and work entirely in the universe for [[univalent type theory]] or [[univalent foundations]]. Adding internal universe types as [[small]] [[object classifiers]] as well as all [[higher inductive types|higher inductive]] and [[coinductive types]] to the universe results in [[homotopy type theory]]. 

* One can add a [[Russell type of all propositions]] and a [[natural numbers type]] and work in the dependent type theory itself for [[higher-order logic]].

## Description

### Judgments for types and terms

[[!include judgements for types and terms - table]]

## Properties

+-- {: .num_theorem}
###### Theorem

The [[functors]] 

* $Cont$, that form a [[category of contexts]] of a [[dependent type theory]];

* $Lang$ that forms the [[internal language]] of a [[locally cartesian closed category]]

constitute an [[equivalence of categories]]

$$
  DependentTypeTheories
    \stackrel{\overset{Lang}{\leftarrow}}{\underset{Cont}{\to}}
  LocallyCartesianClosedCategories
  \,.
$$

=--

This ([Seely, theorem 6.3](#Seely)).  It is somewhat more complicated than this, because we need to strictify the category theory to match the category theory; see [[categorical model of dependent types]].  For a more detailed discussion see at
_[[relation between type theory and category theory]]_.

## Extensional vs Intensional
 {#ExtensionalIntensional}

There is an important distinction between *[[extensional type theory|extensional]]* type theories and *[[intensional type theory|intensional]]* ones. The meanings of these words is probably clearest when dealing with function types, such as an exponential $Y^X$, but also arises in respect to quotient types and identity types.

### Extensional and intensional function types

A [[function type]] $Y^X$ is said to be **extensional** if whenever $f,g\colon X\to Y$ are functions such that $f(x)=g(x)$ for all $x\in X$, then in fact $f=g$ as elements of $Y^X$.  This clearly corresponds to the modeling of function types by [[function sets]] in the set-theoretic semantics, or more generally by [[exponential objects]] in the categorical semantics discussed above.  The uniqueness clause of the defining assertion of an exponential object, i.e. that any map $Z\times X\to Y$ factors through a *unique* map $Z\to Y^X$, precisely models this "extensionality" property.  Thus, the standard categorical semantics is most closely allied to type theories which have such an "extensionality" axiom.

By contrast, suppose that $X$ and $Y$ are interpreted by [[data types]] in some [[programming language]], and $Y^X$ is interpreted by some type of computable functions from $Y^X$.  Of course, many differently coded functions can have the same "extensional behavior," i.e. the same output for any given input, but we may still want to distinguish between these functions because they may not share other properties (such as running time or complexity).  Thus, this type $Y^X$ is not extensional---equality of functions, as elements of $Y^X$, is "implementation-sensitive," a finer measure than mere equality on all inputs.  We say instead that these function types are **intensional**.

In type theory, extensional function-types generally come with both a "$\beta$-rule," which specifies the computational behavior of a $\lambda$-abstraction (i.e. $(\lambda x. t)(y) = t[y/x]$), and an "$\eta$-rule," which specifies that a $\lambda$-abstraction is determined by its behavior (i.e. $f = (\lambda x. f(x))$).  In the categorical semantics, the first specifies the existence of factorizations, while the second requires them to be unique.  In intensional type theory, we generally keep the $\beta$-rule (it is certainly natural from a computational standpoint) but discard the $\eta$-rule.  Thus, one natural sort of semantics for intensional type theory is valued in a category with "weak exponentials," i.e. objects which satisfy the existence but not uniqueness property of an exponential (and similarly for dependent type theory with $\Pi$-types and weak [[dependent product]]s).

### Quotient types and exact completion

[[intensional type theory|Intensional type theory]] is also popular among adherents of [[constructive mathematics]] and especially [[predicative mathematics]], because of its computational content.  [[Per Martin-Lof|Per Martin-Löf]]'s original [[Martin-Löf dependent type theory|dependent type theory]] is often presented from this perspective.

When viewing intensional type theory as a foundation for mathematics (rather than, say, a syntax for reasoning about computer programs), it is natural to view the types as representing [[presets]], rather than sets.  This is in line with the classical constructivist viewpoint that "a set is defined by a collection of things together with an equality relation."  Note that in intensional type theory, the "equality" between terms is free to be the "syntactic" equality, which is entirely computable and preserved by everything in sight.  In particular, if we adopt the viewpoint of [[propositions as types]], then "the axiom of choice is trivially valid" for functions between types (i.e. presets) since to assert that something exists is to give an element of a sum type, which is exactly to give a witness and thereby a way to choose such a thing.

If we then define "sets" to be types equipped with equality relations (sometimes called [[setoids]]), then the sets will have more familiar properties, such as existence of extensional exponentials (obtained by equipping the intensional exponentials with an extensional equality relation), as well as the existence of [[quotient sets]].  (The existence of quotient types is often assumed in extensional type theory, but not in intensional type theory.)  In categorical terms, the [[syntactic category]] of an intensional type theory has only weak exponentials (resp. dependent products), but that is sufficient to ensure that its [[free exact completion]] has actual exponentials (resp. dependent products).  Note also that free exact completions always also validate [[COSHEP]], since every object of the starting category (here the category of types) is projective.  This matches the above observations about the axiom of choice.

### Identity types

(to be written...)

Relation between [[identity types]] and [[path space objects]] in a [[category with weak equivalences]]. 

### Higher-categorical semantics

* [[homotopy type theory]]

(to be written...)

## Examples

* [[objective type theory]]
* [[weak type theory]]
* [[book HoTT]]
* [[Martin-Löf type theory]]
* [[cubical type theory]]
* [[higher observational type theory]]
* [[univalent type theory]]
* [[propositional logic as a dependent type theory]]
* [[higher order logic as a dependent type theory]]
* [[impredicative dependent type theory]]
* [[dependent type theory with type variables]]
* [[strongly predicative dependent type theory]]

## Related concepts

* [[type theory]]

  * [[simple type theory]]

  * [[polymorphic type theory]]

  * **dependent type theory**

  * [[polymorphic dependent type theory]]

* [[categorical semantics of dependent types]]

  [[relation between category theory and type theory]]

* [[linear dependent type theory]]

* [[set theory and dependent type theory]]

* [[dependent type theoretic methods in natural language semantics]]

* [[spartan type theory]]

## References

For original references see at *[[Martin-Löf dependent type theory]]*, such as:

* {#Hofmann95} [[Martin Hofmann]], *Syntax and semantics of dependent types*, Chapter 2 in: _Extensional concepts in intensional type theory_, Ph.D. thesis, University of Edinburgh (1995), Distinguished Dissertations, Springer (1997) &lbrack;[ECS-LFCS-95-327](http://www.lfcs.inf.ed.ac.uk/reports/95/ECS-LFCS-95-327/), [[HofmannExtensionalIntensionalTypeTheory.pdf:file]], [doi:10.1007/978-1-4471-0963-1](https://doi.org/10.1007/978-1-4471-0963-1)&rbrack;

also published as:

* [[Martin Hofmann]], *Syntax and semantics of dependent types*, in *Semantics and logics of computation*, Publ. Newton Inst. **14**, Cambridge Univ. Press (1997) 79-130 &lbrack;[doi:10.1017/CBO9780511526619.004](https://doi.org/10.1017/CBO9780511526619.004)&rbrack;

Gentle exposition of the basic principles:

* [[Thomas Kehrenberg]], *Introduction to dependent type theory* (2022-23) &lbrack;[blog series](https://tm.kehrenberg.net/series/introduction-to-dependent-type-theory/)&rbrack;


Introductory accounts:

* {#Thompson91} [[Simon Thompson]], §6.3 in: *[[Type Theory and Functional Programming]]*, Addison-Wesley (1991) &lbrack;ISBN:0-201-41667-0, [webpage](http://www.cs.kent.ac.uk/people/staff/sjt/TTFP), [pdf](http://www.cs.kent.ac.uk/people/staff/sjt/TTFP/ttfp.pdf)&rbrack;

* {#Jacobs98} [[Bart Jacobs]], Chapter 10 in: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf), [webpage](http://www.cs.ru.nl/B.Jacobs/CLT/bookinfo.html)&rbrack;

  > (emphasis on the [[categorical model of dependent types]])


Introduction with parallel details on using [[proof assistants]]:

for [[Coq]]:

* [[Adam Chlipala]], _Certified programming with dependent types_, MIT Press 2013 &lbrack;[ISBN:9780262026659 ](https://mitpress.mit.edu/books/certified-programming-dependent-types), [pdf](http://adam.chlipala.net/cpdt/cpdt.pdf),  [book webpage](http://adam.chlipala.net/cpdt/)&rbrack;

* [[Théo Winterhalter]], *Formalisation and Meta-Theory of Type Theory*, Nantes (2020) &lbrack;[pdf](https://github.com/TheoWinterhalter/phd-thesis/releases/download/v1.2.1/TheoWinterhalter-PhD-v1.2.1.pdf), [github](https://github.com/TheoWinterhalter/phd-thesis)&rbrack;


for [[Agda]]:

* {#Norell08} [[Ulf Norell]], *Dependently Typed Programming in Agda*, p. 230-266 in: *Advanced Functional Programming* AFP 2008. Lecture Notes in Computer Science **5832** (2009) &lbrack;[doi:10.1007/978-3-642-04652-0_5](https://doi.org/10.1007/978-3-642-04652-0_5), [pdf](https://www.cse.chalmers.se/~ulfn/papers/afp08/tutorial.pdf)&rbrack;

* [[Agda]] Tutorial: _Introduction to dependent type theory_ ([webpage](http://ocvs.cfv.jp/Agda/tutorial/node128.html))

Original  discussion of dependent type theory as the [[internal language]] of [[locally cartesian closed categories]] is in 

* {#Seely} [[R. A. G. Seely]], _Locally cartesian closed categories and type theory_, Math. Proc. Camb. Phil. Soc. (1984) 95 ([pdf](http://www.math.mcgill.ca/rags/LCCC/LCCC.pdf))

A formal definition of dependent type theories beyond [[Martin-Löf dependent type theory]]:

* {#BauerHaselwarterLumsdaine20} [[Andrej Bauer]], [[Philipp G. Haselwarter]], [[Peter LeFanu Lumsdaine]], *A general definition of dependent type theories* &lbrack;[arXiv:2009.05539](https://arxiv.org/abs/2009.05539)&rbrack;

{#CSystemsReferences} On ([[essentially algebraic theory|essentially algebraic]])  formulations of dependent type theory (see [here](categorical+model+of+dependent+types#ContextualCategoriesOrCSystems) at *[[categorical models of dependent type theory]]*):

* [[Egbert Rijke]], _An algebraic formulation of dependent type theory_, ([mailing list discussion](https://groups.google.com/forum/#!topic/homotopytypetheory/OraMqbnCYy8/discussion))
* Vladimir Voevodsky, _B-systems_, ([arXiv:1410.5389](http://arxiv.org/abs/1410.5389))
* Vladimir Voevodsky, _A C-system defined by a universe in a category_, ([arXiv:1406.7413](http://arxiv.org/abs/1409.7925))
* Vladimir Voevodsky, _C-system of a module over a monad on sets_, ([arXiv:1406.7413](http://arxiv.org/abs/1407.3394))
* Vladimir Voevodsky, _Subsystems and regular quotients of C-systems_, ([arXiv:1406.7413](http://arxiv.org/abs/1406.7413))

For more see the references at _[[Martin-Löf dependent type theory]]_.

[[!redirects dependent type theories]]
[[!redirects Dependent type theories]]
[[!redirects Dependent type theory]]