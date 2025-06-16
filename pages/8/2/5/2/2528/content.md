
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+-- {: .hide}
[[!include quasi-category theory contents]]
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

# Presets
* table of contents
{: toc}

## Idea

A _preset_ is a [[set]] without an [[equality relation]].  Conversely, a set may be defined as a preset $X$ equipped with an equality relation, an [[equivalence relation|equivalence]] _prerelation_ on $X$ which satisfies the [[principle of substitution]] and the [[identity of indiscernibles]]. 

In his seminal work _The Foundations of Constructive Analysis_ (1967), [[Errett Bishop]] explained what you must do to define a _set_ (see also [[Bishop set]]) in three steps:

1. You must state what one must do to construct an element of the set;
2. Given two elements constructed as in (1), you must state what one must do to prove that the elements are equal;
3. You must prove that the relation defined in (2) is reflexive, symmetric, and transitive (which can be phrased in similar 'what one must do' terms, but that\'s kind of wordy).

If you only do (1), then you don\'t have a set, according to Bishop; you only have a __preset__.

## Prefunctions and prerelations

As [[functions]] go between sets, so __prefunctions__ go between presets. (Bishop used the term 'operation' instead of 'prefunction', but 'operation' has many other meanings.) Even if $X$ and $Y$ are sets, a prefunction from $X$ to $Y$ is not the same as a function from $X$ to $Y$, because a prefunction need not preserve equality; that is, we may have $a = b$ without $f(a) = f(b)$.  Conversely, we may define a function as a prefunction (between sets) that preserves equality; such a prefunction is said to be __extensional__.

For example, consider the identity prefunction on the underlying preset of both $Q^+$ and $Z^+ \times Z^+$, as defined above.  From $Z^+ \times Z^+$ to $Q^+$, this is a function, since $a/b = c/d$ if $(a,b) = (c,d)$.  But from $Q^+$ to $Z^+ \times Z^+$, it is not a function, since (for example) $2/4 = 3/6$ but $(2,4) \neq (3,6)$.  A related example is the operation of taking the numerator of a (positive) rational number; from $Q^+$ to $Z^+$, we may view this as a prefunction but not as a function, although it is a function on $Z^+ \times Z^+$.

In general, the prefunctions from $X$ to $Y$ form a preset, since there is no way to compare them for equality.  (Of course, it is still [[predicative mathematics|impredicative]], at least in the classical sense, to form this preset.)  However, if $Y$ is a set, then these prefunctions do form a set, with $f = g$ defined to mean that $f(a) = g(a)$ for every $a$ in $X$.  If $X$ is also a set, then the [[function set]] from $X$ to $Y$ is a [[subset]] of this set of prefunctions.

Composition of prefunctions is also possible, but likewise does not preserve equality. 

A (say binary) __prerelation__ between $X$ and $Y$ may be thought of as a prefunction from $X \times Y$ to [[truth values]].  Even if one is too predicative to allow a (pre)set of truth values, still one may have a notion of prerelation, by fiat if nothing else.  Note that one *can* compare prerelations for equality; $R = S$ means that $a \sim_R b$ if and only if $a \sim_S b$.  (In other words, a preset of truth values becomes a set under the biconditional, so we can compare functions to it.) In particular, the [[principle of substitution]] and [[identity of indiscernibles]] together imply that any two equality relations on a preset are equal to each other, so equality is unique if it exists. 

We define a [[relation]] between sets to be a prerelation that respects equality; such a prefunction is said to be __extensional__.

Many properties of relations can also be predicated of prerelations, but not all. In particular, prerelations may be [[reflexive relation|reflexive]], [[symmetric relation|symmetric]], and [[transitive relation|transitive]], so we have a notion of equivalence prerelation, which completes the definition of sets in terms of presets. A prerelation may also be [[entire relation|entire]], but it makes no sense to ask if it is [[functional relation|functional]] unless $Y$ is a set.  In that case, there is a correspondence between prefunctions and functional entire prerelations as usual.  In general, however, there is no way to define the prerelation corresponding to a given prefunction (which would be a sort of pre-[[graph of a function|graph]]).  In other words, the idea that functions are certain relations (namely the functional entire ones) does not extended to prefunctions and prerelations unless $Y$ is a set.

In general, prerelations are 

## Presets, types, sets, and setoids

Presets do not have equality. However, the types in many type theories come equipped with some kind of [[identity type]], where the only difference from equality is that they are not predicates. Thus, strictly speaking, the types in the type theories are not presets. 

The sets defined by Bishop do not have [[quotient sets]], so there is still a distinction between Bishop sets and the quotient set of an object with an equivalence relation: this is the difference between a [[set]] and a [[setoid]]. Some people call a set with no quotient sets a "preset", however, this use of "preset" is at odds with preset as something that does not have equality. 

While there is at most one [[equality]] on a preset due to the [[principle of substitution]] and the [[identity of indiscernibles]], a given preset may have many different equivalence relations, giving rise to setoids. For example, the setoid $Q^+$ of positive rational numbers may be defined using the same underlying set as the setoid $Z^+ \times Z^+$ of ordered pairs of positive integers, but the equivalence relation is different; two pairs $(a,b)$ and $(c,d)$ of positive integers are equivalent iff $a = c$ and $b = d$, while two positive rational numbers $a/b$ and $c/d$ are equivalent iff $a d = b c$. (Of course, these definitions require that one already has the set $Z^+$ of positive integers with its equality relation, and the operation of multiplication on it. Additionally, the [[cartesian product]] of two [[sets]] is itself a [[set]].)

## Formalisation

### In category theory

One may hope to formalise the category of presets and prefunctions between presets, but unfortunately, presets and prefunctions do not form a category. Instead, they only form a [[magmoid]]. 

### In type theory

It is possible to develop type-theoretic foundations in which presets are *not* equipped with identity relations (only metamathematical identity or interconvertibilty *judgements*); see [[tobybartels:preset]] for some discussion. Unlike the case for types with identity relations, the [[presentation axiom]] is not provable in the base theory, although it is provable in the impredicative version (where identity relations can be defined, following [[Gottfried Leibniz|Leibniz]]\'s definition of equality). 

However, there is a way to formalize [[presets]] and [[prefunctions]] in [[dependent type theory]] even with [[identity types]]: by instead defining [[propositional equality]] as the [[predicate]] that the [[identity type]] is [[contractible]] 

$$x = y \coloneqq \mathrm{isContr}(\mathrm{Id}_A(x, y))$$

Expanding out the definition of a [[contractible type]], a witness of propositional equality consists of an [[identification]] and a [[contraction]] showing that the identification is the [[center of contraction]] of the [[identity type]]. 

By this definition of equality, propositional equality is always a [[binary relation]], because [[isContr]] is always a [[proposition]] in [[dependent type theory]]. In fact, if all identifications in an [[identity type]] are unique (i.e. there is a function $\mathrm{Id}_A(x, y) \to x = y$), then the identity type is an [[h-proposition]], and if the identity type is an [[h-proposition]], then all identifications in the identity type are unique; hence the name *[[propositional equality]]* for unique identifications and the relation $x = y$ for the type $\mathrm{isContr}(\mathrm{Id}_A(x, y))$. 

A **[[set]]** is then precisely a type where all identifications are unique. The [[uniqueness of identity proofs]] states that all identity types are propositions and all identifications are unique. 

Propositional equality satisfies the [[principle of substitution]] by [[transport]] of the unique identification across [[predicates]], and satisifes the [[identity of indiscernibles]] because propositional equality is always a proposition, and so we have:

$$\prod_{x:A} \prod_{y:A} \mathrm{isContr}(\mathrm{Id}_A(x, y)) \simeq \prod_{x:A \to \mathrm{Prop}} P(x) \simeq P(y)$$

However, propositional equality is not an [[equivalence relation]] because it is not [[reflexive]]: for any [[loop space type]] which is not a [[contractible type]], the proposition $\mathrm{isContr}(\mathrm{Id}_A(x, x))$ is an [[empty type]]. The only such types with a reflexive propositional equality are thus those that satisfy [[axiom K]]: the [[h-sets]], thus making non-set types [[presets]]. 

Furthermore, every function can still be interpreted as a **prefunction** in the following sense: while functions do preserve identifications, they do not preserve propositional equality in the sense of the uniqueness of identifications. *Any* [[identification]] is given by a function out of the [[interval type]] $\mathbb{I}$, and the inductively generated identification $p:\mathrm{Id}_\mathbb{I}(0, 1)$ in the interval type is unique in $\mathrm{Id}_\mathbb{I}(0, 1)$, but not all identifications are unique in the absence of [[uniqueness of identity proofs]]. One can define an [[extensional function]] as one that does preserve the uniqueness of identifications, and prove that functions between [[h-sets]] preserve the uniqueness of identifications, and that h-sets are precisely the types between which all functions preserve uniqueness of identifications. To say that all functions are extensional along the lines of the [[preset]] approach to [[set theory]] is equivalent to the [[uniqueness of identity proofs]] that implies that all types are [[h-sets]].  

### In logic

If an untyped [[first-order logic]] does not have equality of propositions or equality of predicates, then the [[domain of discourse]] is a preset instead of a set. This remains true for typed first-order logic with multiple types, which are presets if each type does not have local equality. 

The sorts in [[Michael Makkai]]\'s [[FOLDS]] are presets.  FOLDS is very different from the other foundations considered above, since it is based strictly on prerelations and has no notion of prefunction.  As far as I can tell, it therefore does not prove the [[presentation axiom]].

## Applications

To make the [[principle of equivalence]] hold automatically, a [[category]] should have only a preset of [[objects]] and only its [[hom-sets]] as sets.  Then a category whose set of objects *is* a set may be called a [[strict category]], which is really a special case of a [[strict ∞-category]].  Alternatively, one may keep sets as sets but adopt pre[[class]]es; then a [[small category]] is strict but a large category is not.

## Related concepts

* [[setoid]]

* [[type theory]]

* [[Bishop set]], [[predicative topos]]

* [[prefunction]]

* [[propositional equality]]

[[!redirects preset]]
[[!redirects presets]]
[[!redirects pre-set]]
[[!redirects pre-sets]]

[[!redirects prerelation]]
[[!redirects prerelations]]
[[!redirects pre-relation]]
[[!redirects pre-relations]]

[[!redirects preset theory]]

[[!include types and logic - table]]