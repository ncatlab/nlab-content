
#Contents#
* table of contents
{:toc}

## Idea

"Transcendental syntax" ([Girard 13](#Girard13)) is the name of a proposal (or maybe a pamphlete) by [[Jean-Yves Girard]] which means to rethink fundamental aspects of [[formal logic]], of [[syntax]]/[[semantics]]. According to Girard, _[[linear logic]]_ and _[[Geometry of Interaction]]_ are but exercises in transcendental syntax ([Girard 13b](#Girard13b)).

While Girard's prose is notoriously demanding, exegesis may be found in ([Abrusci-Pistone 12](#AbrusciPistone12)) for the philosophical side and ([Rouleau 13](#Rouleau13)) which was written before the more modern developements of transcendental syntax by means of stars and constellations ([Girard 13b](#Girard13b)). 

The positionning of transcendental syntax in logic is summarised by Girard's four levels of understanding of proofs, in which the last level corresponds to the transcendental syntax:

> Girard describes four levels of [[semantics]]: alethic, functional, interactive, and deontic. They descend into the depths of meaning, and thus are numbered from -1 to -4. The negatively first, alethic, is the layer of truth or models. The negatively second, functional, is the layer of functions or categories. The negatively third, interaction, is the layer of games or game semantics. The negatively fourth, deontic, is the layer of normativity or formatting. ([Equivalent eXchange](http://equivalentexchange.wordpress.com/2012/03/07/j-y-girards-transcendental-syntax/))

### Philosophical interpretation

The transcendental syntax starts from the strong claim that [[formal logic]] makes a lot of rather arbitrary choices such as the so-called *rules of logic* (see [[deductive systems]]) and that it should be possible to study the mechanisms of reasoning without these assumptions (to which Girard refers to as being the "prejudices" of logic).

The solution presented by the transcendental syntax can be understood as an update of [[Kant]]'s epistemology by taking *computation* into account through recent works in [[linear logic]] and the [[Curry-Howard correspondence | Curry-Howard-Lambek correspondence]]. It suggests the division of the whole logical activity into four concepts ([Girard 16](#Girard13b)):

|                             | Analytic / Answers | Synthetic / Questions |
|-----------------------------|--------------------|-----------------------|
| **A posteriori / Explicit** | Constat            | Usine                 |
| **A priori / Implicit**     | Performance        | Usage                 |

The point of view of the transcendental syntax is that logic studies the relationship between questions (formulas) which are subjective and their answers (proofs) which are objective, by means of finite objects (because of the intuition that reasoning should be finite and verifiable). In order to do so with as less assumptions about logic as possible, we should start by defining the *answers*, seen as neutral and objective. Then we study the sufficient conditions making the logical concepts (proofs, formulas, logical correctness) emerge from the meaningless. In reference to [[Kant]], Girard uses the expression ``conditions of possibility of language".

The **answers** corresponds to a space of general computational objects called *epistates* which can be evaluated (performance) into a [[normal form]] (constat). This is the space where proofs are formulated but not yet considered logically meaningful or correct.

The space of **questions** considers two alternative definitions of *meaning* corresponding to [[formula | formulas]] or [[type | types]] called *dichology*:

- the use (usage): it corresponds to [[Ludwig Wittgenstein]] meaning-as-use. The computational behavior of epistates and their potential interaction with other ones induces a classification into dichologies.

- the factory (usine): we want our computational objects to pass a specific set of *tests* in order to accept them in the corresponding type.

This is related to the distinction between existentialism and essentialism in philosophy. The **logical certainty** corresponds to the adequacy between usine and usage: we would like the usine to be finite and sufficient to ensure what we consider a right use of epistates. According to Girard [Girard 16](#Girard16), the separation between constat and performance comes from undecidability (as in the halting problem) because the potential of programs cannot always be reduced to their result (which is not always defined). As for the separation between usine and usage, it would come from Gödel's [[incompleteness theorem]] which intuitively means that the possible uses of a logical object may go beyond what we expect from our definition (our formatting of the concept of logic).

### Technical interpretation

Technically speaking, the transcendental syntax is basically a finitary improvement of the [[Geometry of Interaction]]. Some preliminary works include *flows* ([Girard 95](#Girard95), [Bagnol 14](#Bagnol14)) or *interaction graphs* ([Seiller 16](#Seiller16)). The transcendental syntax generalizes and extends both by taking into account [[proof net | proof nets']] logical correctness in a more general form.

The elementary objects we consider are *constellations*, defined as multisets of clauses containing first-order terms. Two constellations can interact by using the dynamics of Robinson's resolution ([Robinson 65](#Robinson65)). We use constellations to encode [[proof net | proof structures]], their [[cut rule | cut elimination]] but also the correction graphs asserting logical correctness.

We can obtain two alternative notions of typing:

- By using [[realizability]] techniques for linear logic as in [[ludics]] or Seiller's interaction graphs, we can define [[formula | formulas]] called *behaviors*. This corresponds to types "à la Curry" where untyped computational objects are typed. In this case, types are *designed* and not defined as primitive objects.

- Inspired by the logical correctness of [[proof net | proof nets]], we can define types as a finite sets of tests (encoded as constellations). If a constellation passes all tests, it is considered as part of the corresponding type. This corresponds to types "à la Church" where types exist before the computational objects being typed. In the context of [[proof net | proof nets]], it corresponds to testing proof structures against correction graphs.

### Getting rid of semantics

An important ambition of the transcendental syntax is to make assumptions computationally explicit, and to "put everything on the table". In the transcendental syntax, it is no more possible to write a proof as usual. A proof necessarily comes as a hybrid object $(\Phi, \mathcal{T})$ where $\Phi$ is a constellation (elementary computational object) and $\mathcal{T}$ is a set of constellations corresponding to tests asserting the logical correctness of $\Phi$. The constellation $\Phi$ has to satisfy a given criterion of orthogonality when interacting with $\Phi' \in \mathcal{T}$, written $\Phi \bot \Phi'$. Logical objects only exist as computationally justified constructions.

Following this approach and by choosing a right notion of orthogonality, it is possible to construct axiom-free systems. In transcendental syntax's fourth paper ([Girard 20](#Girard20)), Girard sketches a reconstruction of [[Peano arithmetic]]. An essential point which allows us to actually get rid of semantic explanations is that both tests and tested are of the same kind, have the same role and interact in a symmetric way. The "boundaries" of logic then rely on a given notion of orthogonality and not on a semantic system deciding what is logical or not.

This might be compared with other approaches in [[type theory]] such as [[computational type theory]] or [[cubical type theory]] where some logical constructions are not primitive anymore but reconstructed. A major difference seems to be the starting point and the primitives considered.

All these approaches, including Girard transcendental syntax start from the assumption that computation can fully explain logic and are thus extensions of the [[computational trinitarianism | Curry-Howard-Lambek correspondence]].

### Transcendental syntax as an instance of realizability

Although never explicitly mentioned by Girard, at the technical level, the transcendental syntax is indeed very close to [[realizability | realizability theory]]. In realizability theory, types are designed from a model of computation (for instance, natural numbers and recursive functions or lambda-terms with beta-reduction). But while realizability theory is more focussed on speaking about logic with computation, the transcendental syntax describes computation with logic instead. Moreover, the transcendental syntax can speak about logical correctness and is able to reconstruct linear logic in a convenient way. Note that other alternative approaches for the reconstruction of linear logic exist such as Beffara's concurrent realizability ([Beffara 06](#Beffara06)).

### Transcendental syntax as a toolbox for computer science

The transcendental syntax generalizes, extends or is simply related to several important aspects of computer science (although no direct link has been studied yet):

- in [[descriptive complexity]], we are interested in capturing classes with fragments of logic. This is something which can be considered in the transcendental syntax. Moreover, Girard's third paper on transcendental syntax ([Girard 18](#Girard18)), a reconstruction of predicate and second order logic are sketched, which are essential in descriptive complexity.

- In [[certified programming | model checking and program specification]], we are interested in designing types as specifications or capturing properties of a model of computation with formulas in order to reason about a system. Girard's stars and constellations used in the transcendental syntax actually generalizes state machines and types can be constructed with realizability techniques. A logical system can then be extracted from these techniques.

- In *unit testing*, we are interested in testing a program against a finite number of values in order to assert that the program has a specific behavior and that it is sound. By generalizing the idea of correctness criterion coming from the theory of proof-nets, in the transcendental syntax, it is possible encode tests and programs as objects of the same kind. Both can be typed and testing extends to any model of computation.

## Related entries

* [[realizability]]

* [[proof net]]

* [[geometry of interaction]]

* [[transcendental grammar]]

* [[Critique of Pure Reason]]

* [[computational type theory]]

* [[cubical type theory]]

* [[type theory]]

* [[ludics]]

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

* {#Girard18} [[Jean-Yves Girard]], _Transcendental syntax III: equality_, 2018 ([pdf](http://girard.perso.math.cnrs.fr/trsy3.pdf))

* {#Girard20} [[Jean-Yves Girard]], _Transcendental syntax IV: logic without systems_, 2020 ([pdf](http://girard.perso.math.cnrs.fr/trsy4.pdf))

* {#AbrusciPistone12} [Vito Michele Abrusci](http://www.uniroma3.it/persona.php?persona=v9rdc8l%2Fv34h57mDvlwB1jjlJFqAH%2B3Or9wKcvkvgtI%3D&tab=2), Paolo Pistone, _On Transcendental syntax: a Kantian program for logic?_, 2012 ([pdf](https://www.academia.edu/10495057/On_Trascendental_syntax_a_Kantian_program_for_logic))

* {#Rouleau13} [[Vincent Laurence Rouleau]], _Towards an understanding of Girard's transcendental syntax: Syntax by testing_, PhD thesis 2013  ([pdf](https://ruor.uottawa.ca/bitstream/10393/23680/3/Laurence_Rouleau_Vincent_2013_thesis.pdf))

* {#Beffara06} [[Emmanuel Beffara]], _A Concurrent Model for Linear Logic_, PhD thesis 2013  ([pdf](https://www.sciencedirect.com/science/article/pii/S1571066106001927))

The beginnings of an attempt to formalize Transcendental Syntax is given in

* [[Boris Eng]], [[Thomas Seiller]], _Multiplicative Linear Logic from Logic Programs and Tilings_ ([hal-02895111](https://hal.archives-ouvertes.fr/hal-02895111))

* [[Boris Eng]], _A gentle introduction to Girard's Transcendental Syntax for the linear logician_ ([hal-02977750](https://hal.archives-ouvertes.fr/hal-02977750))

[[!redirects Transcendental Syntax]]