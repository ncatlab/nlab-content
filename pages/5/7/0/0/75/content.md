
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Idea
 {#Idea}

In the context of _foundations of mathematics_ or _[[mathematical logic]]_ one studies formal systems -- [[theories]] -- that allow us to formalize much if not all of [[mathematics]] (and hence, by extension, at least aspects of mathematical fields such as fundamental [[physics]]).

There are two different attitudes to what a desirable or interesting foundation should achieve:

1. In **[[proof theory|proof-theoretic]] foundations** the emphasis is on seeing which formal systems, however convoluted they may be conceptually, allow us to formalize and prove which [[theorems]]. 

   The archetypical such system is [[ZFC]] [[set theory]]. Other formal systems of interest here are [[elementary function arithmetic]] and [[second order arithmetic]], because they are [[proof theory|proof-theoretically]] weak, and still can derive "almost all of undergraduate mathematics" ([Harrington](#Harrington)).

1. In **[[practical foundations]]** (following a term introduced in ([Taylor](#Taylor))) the emphasis is on conceptually natural formalizations that _concentrate the essence of practice and in turn use the result to guide practice_ ([Lawvere](#Lawvere)), as in ([Eilenberg-Steenrod](#EilenbergSteenrod), [Harper](#Harper)).

   Formal systems of interest here are [[ETCS]] or flavors of [[type theory]], which allow natural expressions for central concepts in mathematics (notably via their [[categorical semantics]] and the conceptual strength of [[category theory]]).

For a philosophical treatment of foundations see [[foundations and philosophy]]. 

## Deductive systems

Almost all [[foundations of mathematics]] are expressed in some foundational [[deductive system]]. 

One versatile deductive system [[natural deduction]], which could be used to define certain foundation of mathematics using [[logic over type theory]], such as all [[set theories]], including [[categorical set theories]] like [[ETCS]], as well as the foundations of mathematics using only [[type theory]], including [[set-level type theories]] as well as [[higher foundations]] such as [[homotopy type theory]]. 

Dependent type theories could also act as a [[predicate logic]] in and of itself, using [[propositional truncations]] and the usual type formers. Then one could define inside the dependent type theory a model of [[ZFC]] or [[ETCS]] or a ([[univalent]]) [[Tarski universe]] satisfying suitable axioms and work entirely inside of that model. 

Alternatives include [[sequent calculus]] for logic over untyped theories, such as [[unsorted set theory]], as well as [[lambda-calculus]] for [[type theories]]. 

(Not sure where [[higher-order logic]] would fit)

## Basic notions

### Objects and collections

In most foundations of mathematics, there are basic notions of objects and collections of objects. 

Note that in certain foundations, the objects, collections, and membership are derived notions from some other notion. Collections are referred to a number of names, such as [[set]], [[class]], [[type]], et cetera. Objects could be referred to as [[element]] or [[term]]. 

For example, in [[pure set]] theories like [[ZFC]] and [[Mostowski set theory]], elements and sets are the same notion, and thus elements could be considered to be a derived notion from set, or sets could be considered to be a derived notion from element. In [[material set theory]] with [[urelements]], such as [[ZFA]], elements are the basic notion and sets are derived from elements. In [[ETCS]], while sets are basic, elements are derived from a basic notion of [[function]], and in [[fully formal ETCS]], both sets and elements are derived notions from a basic notion of [[function]]. In [[SEAR]] and [[structural ZFC]], sets and elements are both basic distinct notions. 

Something similar occurs with [[class theories]], such as [[Morse-Kelley class theory]] and the framework of [[algebraic set theory]], where classes play the role of sets. 

In type theory, there are also a distinction to be made. In most type theories, both terms and types are basic foundational notions. However, in [[book HoTT]], terms are the basic notion, and [[types]] are derived from terms. 

In [[higher-order logic]], the [[domain of discourse]] and higher-order [[predicates]] play the role of collections, while the objects in the [[domain of discourse]] play the role of the elements. 

### Membership and typing

In most foundations, there is a basic notion of membership, of an "object being in a collection". 

Foundations could be contrasted between those foundations where membership is a [[membership relation]], and those foundations where membership is a [[typing judgment]]. This distinction is largely the same distinction as the distinction between [[unsorted set theories]] and [[simply sorted set theories]] on one hand, and [[dependently sorted set theories]] and [[dependent type theories]] on the other hand. 

For theories with a membership relation, one could further distinguish between [[homogeneous membership relations]] (for relations on the same sort) and [[heterogeneous membership relations]] (for relations between two different sorts), as well as membership relations which are primitive to the theory, and membership relations which are derived from some other existing structure in the theory. 

For theories with a typing judgment, one simply judges the object, element, or term $a$ to be in the collection, set, or type $A$, () or $a:A$. This is in contrast to membership relations, where () is a proposition with some truth value, and thus one could say whether the proposition that the object, element, or term $a$ is in collection, set, or type $A$ is true or not. 

Formally, there are also a difference in the contexts. When () or $a:A$ is a judgment, then it lies in the type layer, but when () is a true proposition, then it lies in the proposition layer $\Phi$ while the typing judgment $a:$Set lies in the type layer. 

### Equality and equivalence

In most foundations such as [[dependent type theory]] and [[logic over type theory]], one distinguishes various different notions of _[[equality]]_ or _[[equivalence]]_ of the terms of the language.

There are broadly three different notions of equality which could be distinguished: **[[judgmental equality]]**, **[[propositional equality]]**, and **[[typal equality]]**, each of which applies for both objects (elements, terms) and collections (sets, classes, types). Judgmental equality is defined as a basic judgment in the foundations. Propositional equality is defined as a proposition in any [[typed predicate logic]]. Typal equality is defined as a type in type theory, and is also called the [[identity type]] or [[path type]] for elements, and the [[type of equivalences]] for types. 

The equality of elements used in most [[set theories]] and [[class theories]] are [[propositional equalities]]. The equality of elements used in [[dependent type theories]] are [[typal equality]]. If the dependent type theory is not an [[objective type theory]], most likely it also either has one of [[judgmental equality]] or [[propositional equality]] to use for [[definitions]]. 

The equality of collections differs from theory to theory. There are [[set theories]] and [[class theories]] where [[propositional equality]] is used as the notion of [[equality]] between sets and classes, while for other set theories and class theories, the notion of equality between sets and classes is rather [[bijection]] of sets and classes, rather than equality of sets and classes. Something similar happens in dependent type theory, depending on whether one uses a separate type judgment, or [[Russell universes]] without a separate type judgment: for Russell universes, the [[identity type]] is used for the equality of types in the universe, since types are terms of Russell universes. On the other hand, the dependent type theories with a separate type judgment, there is no identity type between two types, and one has to use the [[type of equivalences]] instead. 

A mathematical foundation is said to respect the [[principle of equivalence]] if there is no strict [[propositional equality]] between sets. Thus, any [[unsorted set theory]] like [[fully formal ETCS]] violates the [[principle of equivalence]]. 

### Size issues, universes, and classes

In most foundations of mathematics, there is no way to talk about the collection of all collections; this is known as [[size issues]] in [[mathematics]]. However, there is a way around it, by the usage of [[universes]]. Essentially, instead of trying to talk about the collection of all sets, one instead talks about the collection $U$, whose elements are called **$U$-[[small sets]]** or **$U$-small types**, and whose [[subsets]] or [[subtypes]] are called **$U$-[[classes]]**. 
The objects not in $U$ are called **$U$-[[large sets]]** or **$U$-large types**, and the [[subsets]] or [[subtypes]] which are not [[singleton subsets]] or subtypes are called **$U$-[[proper classes]]**. Each foundations of mathematics has their own approach to [[universes]]:

* In [[set theory]], one usually either uses [[Grothendieck universes]], or some internal model of [[set theory]] or [[class theory]], whether [[well-pointed category|well-pointed]] [[Heyting categories]], [[well-pointed category|well-pointed]] [[division allegories]], [[sets]] with [[extensional relation|extensional]] [[well-founded relation|well-founded]] [[transitive relation|transitive]] relations, [[categories with class structure]], et cetera. 

* In [[class theory]], the notion of universe is already in the theory via the [[universal class]], which is by definition a [[class]] [[universe]]. The basic primitive in class theory are [[classes]], and the $U$-small classes are called [[sets]]. 

* In [[dependent type theory]], one uses [[univalent universe|univalent]] [[Russell universes]] or [[Tarski universes]], which are basically internal models of [[dependent type theory]]. 

## Effect of foundations on concrete problems
{#Concrete}

It may seem on first sight that foundational questions in mathematics are remote from "real mathematics". This is not quite so. For a list of "real world" problems that do depend on foundations see

* [[effects of foundations on "real" mathematics]]

## Related concepts

* [[New Foundations]]

* [[univalent foundations for mathematics]]

* [[synthetic mathematics]]

* [[category theory and foundations]]

\section{Philosophical musings}

* [[Gravity and grace]], Simone Weil.

## References

* [[Bertrand Russell]], _[[Principia Mathematica]]_, 1910 

* {#Lawvere} [[William Lawvere]], _Foundations and applications: axiomatization and education_, Bulletin of Symbolic Logic 9 (2003), 213-224 ([ps](http://www.math.ucla.edu/~asl/bsl/0902/0902-006.ps), [Euclid](http://projecteuclid.org/euclid.bsl/1052669290))
 
* {#Harrington} L. A. Harrington (ed.), _Harvey Friedman's Research on the Foundations of Mathematics_, Studies in Logic and the Foundations of Mathematics (2012)

* [[Stefania Centrone]], [[Deborah Kant]], [[Deniz Sarikaya]] (editors), *[[Reflections on the Foundations of Mathematics]]*, Synthese Library **407** Springer (2019)  &lbrack;[doi:10.1007/978-3-030-15655-8](https://doi.org/10.1007/978-3-030-15655-8)&rbrack;

[[practical foundations|Practical foundations]] in terms of [[type theory]] language are laid out in

* [[Paul Taylor]], _[[Practical Foundations of Mathematics]]_, Cambridge University Press ([web](http://www.paultaylor.eu/~pt/prafm/index.html))
{#Taylor}

Under [[computational trinitarianism]] this corresponds to a practical foundation in [[program|programming]], laid out in

*  [[Robert Harper]], _[[Practical Foundations for Programming Languages]]_ ([web](https://www.cs.cmu.edu/~rwh/pfpl/))
{#Harper}

A classification of [[material set theories]] and [[structural set theories]] is in

* [[Michael Shulman]] (2018). Comparing material and structural set theories. [arXiv:1808.05204](https://arxiv.org/abs/1808.05204).
{#Shulman2018}

A foundation for [[algebraic topology]] in this practical spirit is laid out in 

* [[Samuel Eilenberg]], [[Norman Steenrod]], _[[Foundations of Algebraic Topology]]_
  {#EilenbergSteenrod}

A big picture intro to the comparison between set theory, type theory and topos/category theory as approaches to foundations is in

* [[Steve Awodey]], _From Sets to Types to Categories to Sets_ [pdf](http://www.andrew.cmu.edu/user/awodey/preprints/stcsFinal.pdf)

A comparative discussion of complexities of different foundations is in 

* [[Freek Wiedijk]], _Is ZF a hack? Comparing the complexity of some (formalist interpretations of) foundational systems for mathematics_ ([pdf](http://www.cs.ru.nl/~freek/zfc-etc/zfc-etc.pdf))

  **Abstract** This paper presents [[Automath]] encodings (which also are
valid in LF/P) of various kinds of foundations of mathematics. Then it compares these encodings according to their size, to find out which foundation is the simplest.

   The systems analyzed in this way are two kinds of [[set theory]] (ZFC and NF), two systems based on Church's [[higher order logic]] ([[Isabelle]]/Pure and [[HOL]]), three kinds of [[type theory]] (the [[calculus of constructions]], Luo's extended calculus of constructions, and Martin-L&#246;f predicative type theory) and one [[ETCS|foundation based on category theory]]. The conclusions of this paper are that the simplest system is type theory (the calculus of constructions) but that type theories that know about serious mathematics are not simple at all. Set theory is one of the simpler systems too. Higher order logic is the simplest if one looks at the number of concepts (twenty-five) needed to explain the system. On the other side of the scale, category theory is relatively complex, as is Martin-L&#246;f's type theory.

* [[Colin McLarty]], _Set theory for Grothendieck's number theory_, [pdf](http://www.cwru.edu/artsci/phil/Groth%20found.pdf)

[[!redirects mathematical foundation]]
[[!redirects mathematical foundations]]


[[!redirects foundation]]
[[!redirects foundations]]
[[!redirects Foundation]]
[[!redirects Foundations]]
[[!redirects foundation of mathematics]]
[[!redirects foundations of mathematics]]