
#Contents#
* table of contents
{:toc}

## Idea

"Transcendental syntax" ([Girard 13](#Girard13)) is the name of a proposal (or maybe a pamphlete) by [[Jean-Yves Girard]] which means to rethink fundamental aspects of [[formal logic]], of [[syntax]]/[[semantics]]. According to Girard, _[[linear logic]]_ and _[[Geometry of Interaction]]_ are but exercises in transcendental syntax ([Girard 13b](#Girard13b)).

While Girard's prose is notoriously demanding, exegesis may be found in ([Abrusci-Pistone 12](#AbrusciPistone12), [Rouleau 13](#Rouleau13)). 

> Girard describes four levels of [[semantics]]: alethic, functional, interactive, and deontic. They descend into the depths of meaning, and thus are numbered from -1 to -4. The negatively first, alethic, is the layer of truth or models. The negatively second, functional, is the layer of functions or categories. The negatively third, interaction, is the layer of games or game semantics. The negatively fourth, deontic, is the layer of normativity or formatting. ([Equivalent eXchange](http://equivalentexchange.wordpress.com/2012/03/07/j-y-girards-transcendental-syntax/))

### Philosophical interpretation

The Transcendental Syntax starts from the strong claim that [[formal logic]] makes a lot of arbitrary choices such as the *rules of logic* (see [[deductive systems]]) and that it should be possible to study the mechanisms of reasoning without these assumptions (to which Girard refers to as "prejudices" hiding the "blind spots" of logic).

The solution presented by the Transcendental Syntax can be understood as an update of [[Kant]]'s epistemology by taking *computation* into account through recent works in [[linear logic]] and the [[Curry-Howard correspondence]]. It suggests the division of the whole logical activity into four concepts ([Girard 16](#Girard13b)):

|                             | Analytic / Answers | Synthetic / Questions |
|-----------------------------|--------------------|-----------------------|
| **A posteriori / Explicit** | Constat            | Usine                 |
| **A priori / Implicit**     | Performance        | Usage                 |

The point of view of the Transcendental Syntax is that logic studies the relationship between questions (formulas) and their answers (proofs) by means of finite objects. In order to do so with as less assumptions about logic as possible, we should start by defining the *answers*, seen as neutral and objective. Then we study the sufficient conditions making the logical concepts (proofs, formulas, logical correctness) emerge from the meaningless. In reference to [[Kant]], Girard talks about the *conditions of possibility of language*.

The **answers** corresponds to a space of computational objects called *epistates* which can be evaluated (performance) into a [[normal form]] (constat). This is the space where proofs are formulated but not yet considered logically correct.

The space of **questions** considers two alternative definitions of *meaning* corresponding to [[formula | formulas]] or [[type | types]] called *dichology*:

- the use (usage): it corresponds to [[Ludwig Wittgenstein]] meaning-as-use. The computational behaviour of epistates and their potential interaction with other ones induces a classification into dichologies.

- the factory (usine): we want our computational objets to pass a specific set of *tests* in order to accept them in the corresponding type.

This is related to the distinction between existentialism and essentialism in philosophy. The **logical certainty** corresponds to the adequacy between usine and usage: we would like the usine to be finite and sufficient to ensure what we consider a right use of epistates.

### Technical interpretation

Technically speaking, the Transcendental Syntax is basically a finitary version of the [[Geometry of Interaction]]. Some preliminary works include *flows* ([Girard 95](#Girard95), [Bagnol 14](#Bagnol14)) or *interaction graphs* ([Seiller 16](#Seiller16)). The Transcendental Syntax generalises and extends both by taking into account [[proof net | proof nets']] logical correctness in a more general setting.

The elementary objects are *constellations* defined as multisets of clauses containing first-order terms. Two constellations can interact by using the dynamics of Robinson's resolution ([Robinson 65](#Robinson65)). We use constellations to encode [[proof net | proof structures]], their [[cut rule | cut elimination]] but also the correction graphs asserting logical correctness. 

We can obtain two alternative notions of typing:

- By using [[realizability]] techniques for linear logic as in [[ludics]] or Seiller's interaction graphs, we can define [[formula | formulas]] called *behaviours*. This corresponds to types "à la Curry" where untyped computational objects are typed.

- Inspired by the logical correctness of [[proof net | proof nets]], we can define a type as a finite set of tests (encoded as constellations). If a constellation passes all tests, it is considered as part of the corresponding type. This corresponds to types "à la Church" where types exist before the computational objects being typed. In the context of [[proof net | proof nets]], it corresponds to testing proof structures against correction graphs.

### The blind spots of logic made computationally explicit

An important ambition of the Transcendental Syntax is to make assumptions computationally explicit, to "put everything on the table". In the Transcendental Syntax, it is no more possible to write a proof as usual. A proof comes as a hybrid objects $(\Phi, \mathcal{T})$ where $\Phi$ is a constellation (elementary computational object) and $\mathcal{T}$ is a set of constellations corresponding to tests asserting the logical correctness of $\Phi$. The constellation $\Phi$ has to satisfy a given criterion of orthogonality when interacting with $\Phi' \in \mathcal{T}$, written $\Phi \bot \Phi'$. Logical objects only exist as computationally justified constructions.

Following this approach and by choosing a right notion of orthogonality, it is possible to construct axiom-free systems. In Transcendental Syntax's fourth paper ([Girard 20](#Girard20)), Girard sketches a reconstruction of [[Peano arithmetic]].

This might be compared with other approaches in [[type theory]] such as [[computational type theory]] or [[cubical type theory]] where some logical constructions are not primitive anymore but reconstructed. A major difference seems to be the starting point and the primitives considered. It is also very similar to approaches in [[realizability | classical realizability]].

All these approaches, including Girard Transcendental Syntax start from the assumption that computation can fully explain logic and are thus extensions of the [[computational trinitarianism | Curry-Howard-Lambek correspondence]].

## Related entries

* [[realizability]]

* [[proof net]]

* [[geometry of interaction]]

* [[transcendental grammar]]

* [[Critique of Pure Reason]]

* [[computational type theory]]

* [[cubical type theory]]

* [[type theory]]

* [[computational trinitarianism]]

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

The beginnings of an attempt to formalize Transcendental Syntax is given in

* [[Boris Eng]], [[Thomas Seiller]], _Multiplicative Linear Logic from Logic Programs and Tilings_ ([hal-02895111](https://hal.archives-ouvertes.fr/hal-02895111))

* [[Boris Eng]], _Stellar Resolution: Multiplicatives - for the linear logician, through examples_ ([hal-02977750](https://hal.archives-ouvertes.fr/hal-02977750))

[[!redirects Transcendental Syntax]]
[[!redirects Transcendental syntax]]