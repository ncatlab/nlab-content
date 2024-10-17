
#Contents#
* table of contents
{:toc}

## Idea

"Transcendental syntax" ([Girard 13](#Girard13)) is the name of a proposal (or maybe a pamphlete) by [[Jean-Yves Girard]] which means to rethink fundamental aspects of [[formal logic]], of [[syntax]]/[[semantics]] in the light of computer science (and more especially through the so-called [[Curry-Howard correspondence | Curry-Howard-Lambek correspondence]]. According to Girard, _[[linear logic]]_ and _[[Geometry of Interaction]]_ are but exercises in transcendental syntax ([Girard 13b](#Girard13b)).

While Girard's prose is notoriously demanding, exegesis may be found in ([Abrusci-Pistone 12](#AbrusciPistone12)) for the philosophical side, ([Rouleau 13](#Rouleau13)) which was written before the more modern developements of transcendental syntax by means of stars and constellations ([Girard 13b](#Girard13b)) or ([Eng 23](#Eng23)) for an attempt to formalize and contextualize Girard's last works from the point of view of computer science.

### Getting rid of semantics

Usually, [[semantics]] dictates what logic is. It allows and forbids manipulations of symbols by following what we consider logic to be, in a dualism between symbol (interpreted) and its meaning (interpreter). An ambition of the transcendental syntax is to _get rid of semantics_ (which is actually a distinguished form of syntax) by redirecting the computational power of semantics and its dialogue with syntax and putting it at the same level as syntax: the barrier is broken and everything becomes synctatic objects of same nature interacting in a same space from which logical meaning emerges. This approach is meant to make more explicit the mechanisms underlying logical reasoning (which appears in types, formulas, specifications, computer programs, mathematical proofs, computational constraints, computational complexity, ...).

## Philosophical interpretation

The transcendental syntax starts from the claim that [[formal logic]] makes a lot of rather arbitrary choices such as the so-called *rules of logic* (see [[deductive systems]]) and that it should be possible to study the mechanisms of reasoning without these assumptions (that Girard calls "prejudices").

His point of view can be seen as an update of [[Kant]]'s epistemology taking *computation* into account through recent works in [[linear logic]] and the [[Curry-Howard correspondence | Curry-Howard-Lambek correspondence]]. The whole logical activity is divided into four concepts ([Girard 16](#Girard13b)):

|                             | Analytic / Answers | Synthetic / Questions |
|-----------------------------|--------------------|-----------------------|
| **A posteriori / Explicit** | Constat            | Usine                 |
| **A priori / Implicit**     | Performance        | Usage                 |

The idea is that logic studies the relationship between questions (formulas being a special case) which are subjective and their answers (proofs being a special case) which are objective, by means of finite objects (because reasoning should be finite and verifiable, otherwise it would not even be possible). In order to be freed from those "prejudices", one should start by defining the *answers*, seen as neutral and meaningless. Then, the point would be to study the sufficient conditions making the logical concepts (proofs, formulas, logical correctness) emerge from the meaningless. In reference to [[Kant]], Girard uses the expression ``conditions of possibility of language".

The **answers** correspond to the space of computation (generalizing proofs) which can be evaluated (**performance**) into a [[normal form]] (**constat**). This is the space where proofs are constructed but not yet considered logically meaningful or correct. It is the material on which logic is constructed.

The space of **questions** considers two alternative definitions of *meaning* corresponding to [[formula | formulas]] or [[type | types]]:

- the use (usage): it corresponds to [[Ludwig Wittgenstein]]'s meaning-as-use. The meaning of computational objects is defined by their potential interactions.

- the factory (usine): the meaning of computational objects is defined by a set of (well-chosen) *tests* they have to pass (exactly as for tests in programming).

This is related to the distinction between existentialism and essentialism in philosophy. **Logical certainty** corresponds to the _adequacy_ between usine and usage: we would like factory's tests to be finite and sufficient in a way to guarantee an associated computational behavior (in a same way tests in a factory should be relevant and guarantee a correct use of objets which are made, or in the case of programming, that the tests corresponding to some program specification guarantee some property like the absence of bugs).

According to Girard [Girard 16](#Girard16), the separation between constat and performance comes from undecidability (as in the halting problem) because the potential of programs cannot always be reduced to their result (which is not always defined). As for the separation between usine and usage, it would come from Gödel's [[incompleteness theorem]] which intuitively implies that the possible uses of a logical object may go beyond what we expect from their definition (our formatting of the concept of logic).

The transcendental syntax has a _monist_ approach (opposed to a _dualist_) to logic and start from the assumption that computation can fully explain logic and it therefore extends the [[computational trinitarianism | Curry-Howard-Lambek correspondence]].

## Technical interpretation

Technically speaking, the transcendental syntax is a finitary improvement of Girard's [[Geometry of Interaction]] (in its original form and with its initial motivation). Some preliminary works include *flows* ([Girard 95](#Girard95), [Bagnol 14](#Bagnol14)) or *interaction graphs* ([Seiller 16](#Seiller16)). The transcendental syntax generalizes and extends both by taking into account [[proof net | proof nets']] logical correctness in a more general framework.

The elementary objects (analytic) considered by Girard are called *constellations*. They are defined as multisets of clauses containing first-order terms (with no logical meaning associated). Two constellations can interact by using Robinson's resolution ([Robinson 65](#Robinson65)). We use constellations to encode [[proof net | proof structures]], their [[cut rule | cut elimination]] but also the correction graphs asserting logical correctness. Constellations were initially found by analyzing the behavior of proof-nets and their correctness but other basis of computation can be chosen.

Answers are constellations and questions correspond to two notions of types:

- by using [[realizability]] techniques for linear logic as in ludics or Seiller's interaction graphs, we can define [[formula | formulas]] called *behaviors*. This corresponds to types "à la Curry" where untyped computational objects are typed a posteriori.

- Inspired by the logical correctness of [[proof net | proof nets]], we can define types as a finite sets of tests (encoded as constellations). If a constellation passes all tests, it can be labelled by the corresponding type label. This is close to types "à la Church" where types exist before the computational objects being typed. In the context of [[proof net | proof nets]], it corresponds to testing proof structures against correction graphs.

Although never explicitly mentioned by Girard, the transcendental syntax is very close to [[realizability | realizability theory]]. In realizability theory, types are designed from a model of computation (for instance, natural numbers and recursive functions or lambda-terms with beta-reduction). However, the transcendental syntax is able to speak about logical correctness (through linear logic). Note that other alternative approaches for the reconstruction of linear logic exist such as Beffara's concurrent realizability ([Beffara 06](#Beffara06)).

## Intuitive illustrations

### Car factory

This is an example given by Girard in his book ([_Le fantôme de la transparence_](#Girard16c)).

A car (analytics) can be certified by a factory (usine) and receive a label (type) which can guarantees that it will work as expected (adequacy). However, it would be absurd to drive 20000km with a car only to show that it can do it (actual use cannot serve as effective testing). Those factory tests are effective, finite, partial but sufficient. They are well-chosen and can be more laxist or strict.

### Automata theory

An finite automata is a machine receiving a finite word as input and which either accepts or rejects it. Hence, there are two kind of objects (analytic): machines and words and machines can only interact with words.

Only by interaction, a way to tell whether a machine recognizes some language is to feed it with all the words of that language (Girard's use). However, in the case the language is infinite (e.g. all binary words ending with 00), you would never be able to conclude. However, we are still able to reason on automata and words by an external logical reasoning and analysis.

The idea of the transcendental syntax would be to reify this external reasoning by extending the computational space such that it can express automata, words and their interaction but also such that it is "large" enough in order to introduce "exotic objects" which can serve as finite tests against automata, thus internalizing our external logical reasoning into the syntax observed.

Those exotic objects are what Girard calls the "hidden files" of logic, in reference to hidden files in Unix systems which are often essential but invisible.

This is reminiscent of how the space of real numbers is extended to complex numbers in order to solve some equations.

### Lambda-calculus

Lambda-term is a syntactic theory of functions. In order to check whether some term is a function from some type **A** to some type **B**, the "use" approach would be to test it against all terms of type **A** and check whether it produces a term of type **B**. Since there can be infinitely many terms of type **A**, testing would never finish.

However, we are still able to say that a term is a function by using type rules for simply typed lambda-calculus (STLC). Those typing rules provide tests (Girard's factory) and we have guarantees that if the term has the same of a function (it is a lambda abstraction) and that it is well-typed, then it will behave well as a function.

## Axiom-free systems

Following this approach, it is theoretically possible (but non-trivial) to construct axiom-free systems. In ([Girard 20](#Girard20)), Girard roughly sketches a reconstruction of [[Peano arithmetic]].

## Transcendental syntax and computer science

The transcendental syntax generalizes, extends or is simply related to several important aspects of computer science (although no direct link has been studied yet, thus making this section speculative):

- in [[descriptive complexity]], we are interested in capturing classes with fragments of logic. In Girard's third paper on transcendental syntax ([Girard 18](#Girard18)), a reconstruction of predicate and second order logic is sketched. They are both essential in descriptive complexity.

- In [[certified programming | model checking and program specification]], we are interested in designing types as specifications or capturing properties of a model of computation with formulas in order to reason about a system. Girard's constellations used in the transcendental syntax actually generalizes state machines and types can be constructed with realizability techniques.

- In *software testing*, we are interested in testing a program against a finite number of tests in order to assert that the program has a specific behavior. By generalizing the idea of correctness criterion coming from the theory of proof-nets, it is possible encode tests and programs as objects of the same kind.

- Girard's constellations are independent agents communicating with local interactions. This is reminiscent of the _actor model_ in programming or of process calculi (such as the pi-calculus) and we can imagine applications to logic for concurrent, distributed or parallel systems. Links to [[Yves Lafont]]'s interaction nets/combinators could be made as well since they both are alternative to proof-nets.

Although no link have been properly studied, Girard's constellations are reminiscent of biological or chemical computation. However, links between tile systems (Wang tiles and abstract tile assembly models) and Girard's constellation have been mentionned in ([Eng 23](#Eng23)). Morever, it also has been remarked that constellations generalize a model called _flexible tiles_ ([JonoskaMcColm 05](#JonoskaMcColm05)) which is used for DNA-based computation.

The transcendental syntax may also serve as a way to develop new ideas and concepts:

- in the same way as assembly languages are low-level languages close to machine operations, Girard's constellations can be seen as a low-level language which would be closer to the elementary mechanisms of reasoning (since it decomposes lambda-terms) and be used as a compilation target.

- Since logical concepts emerge from objets without any logical meaning, the transcendental syntax may be used to design "logic-agnostic" proof-assistants or tools which are not bound to primitive definitions hard-coded into a compiler or an interpreter. Logical concepts would then be defined by the programmer (as programming libraries for instance).

## Related entries

* [[realizability]]

* [[proof net]]

* [[geometry of interaction]]

* [[transcendental grammar]]

* [[Critique of Pure Reason]]

* [[computational type theory]]

* [[type theory]]

* [[computational trinitarianism]]

* [[certified programming]]

## References

* {#Robinson65} [[JA Robinson]], _A machine-oriented logic based on the resolution principle_, 1965.

* {#Girard95} [[Jean-Yves Girard]], _Geometry of interaction III: accommodating the additives_, 1995 ([pdf](https://girard.perso.math.cnrs.fr/GOI3.pdf)).

* {#Bagnol14} [[Marc Bagnol]], _On the Resolution Semiring_, PhD Thesis 2014 ([pdf](https://www.normalesup.org/~bagnol/phd/these_screen.pdf))

* {#Seiller16} [[Thomas Seiller]], _Interaction Graphs: Full Linear Logic_, 2016 ([pdf](https://www.seiller.org/documents/articles/IG-Full.pdf))

* {#Girard13b} [[Jean-Yves Girard]], _Geometry of Interaction VI: a Blueprint for Transcendental Syntax_, 2013 ([CiteSeer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.303.7141))

* {#Girard13} [[Jean-Yves Girard]], _Transcendental syntax 2.0_, 2013 ([pdf](https://pdfs.semanticscholar.org/8548/a157279b27de84d1effd772b683c7b9d7701.pdf))

* {#Girard16} [[Jean-Yves Girard]], _Transcendental syntax I: deterministic case_, 2016 ([pdf](http://girard.perso.math.cnrs.fr/trsy1.pdf))

* {#Girard16b} [[Jean-Yves Girard]], _Transcendental syntax II: non-deterministic case_, 2016 ([pdf](http://girard.perso.math.cnrs.fr/trsy2.pdf))

* {#Girard16c} [[Jean-Yves Girard]], _Le fantôme de la transparence_, 2016

* {#Girard18} [[Jean-Yves Girard]], _Transcendental syntax III: equality_, 2018 ([pdf](http://girard.perso.math.cnrs.fr/trsy3.pdf))

* {#Girard20} [[Jean-Yves Girard]], _Transcendental syntax IV: logic without systems_, 2020 ([pdf](http://girard.perso.math.cnrs.fr/trsy4.pdf))

* {#AbrusciPistone12} [Vito Michele Abrusci, Paolo Pistone](http://www.uniroma3.it/persona.php?persona=v9rdc8l%2Fv34h57mDvlwB1jjlJFqAH%2B3Or9wKcvkvgtI%3D&tab=2), _On Transcendental syntax: a Kantian program for logic?_, 2012 ([pdf](https://www.academia.edu/10495057/On_Trascendental_syntax_a_Kantian_program_for_logic))

* {#Rouleau13} [[Vincent Laurence Rouleau]], _Towards an understanding of Girard's transcendental syntax: Syntax by testing_, PhD thesis 2013  ([pdf](https://ruor.uottawa.ca/bitstream/10393/23680/3/Laurence_Rouleau_Vincent_2013_thesis.pdf))

* {#Beffara06} [[Emmanuel Beffara]], _A Concurrent Model for Linear Logic_, PhD thesis 2013  ([pdf](https://www.sciencedirect.com/science/article/pii/S1571066106001927))

* {#JonoskaMcColm05} [[Nataša Jonoska, Gregory L. McColm]], _A computational model for self-assembling flexible tiles_, 2005

* [[Boris Eng]], _A gentle introduction to Girard's Transcendental Syntax for the linear logician_ ([hal-02977750](https://hal.archives-ouvertes.fr/hal-02977750))

* {#Eng23} [[Boris Eng]], _An exegesis of transcendental syntax_, PhD thesis 2023 ([tel-04179276v1](https://hal.science/tel-04179276v1))

[[!redirects Transcendental Syntax]]