
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

# Presets
* table of contents
{: toc}

## Idea

A _preset_ is a [[set]] without an [[equality relation]].  Conversely, a set may be defined as a preset $X$ equipped with an equality relation (technically an [[equivalence relation|equivalence]] _prerelation_ on $X$).


In his seminal work _The Foundations of Constructive Analysis_ (1967), [[Errett Bishop]] explained what you must do to define a _set_ (see also [[Bishop set]]) in three steps:

1. You must state what one must do to construct an element of the set;
2. Given two elements constructed as in (1), you must state what one must do to prove that the elements are equal;
3. You must prove that the relation defined in (2) is reflexive, symmetric, and transitive (which can be phrased in similar 'what one must do' terms, but that\'s kind of wordy).

If you only do (1), then you don\'t have a set, according to Bishop; you only have a __preset__.


A given preset may define many different sets, depending on the equality relation.  For example, the set $Q^+$ of positive rational numbers may be defined using the same preset as the set $Z^+ \times Z^+$ of ordered pairs of positive integers, but the equality relation is different; two pairs $(a,b)$ and $(c,d)$ of positive integers are equal iff $a = c$ and $b = d$, while two positive rational numbers $a/b$ and $c/d$ are equal iff $a d = b c$.  (Of course, these definitions require that one already has the set $Z^+$ of positive integers, including its equality relation, and the operation of multiplication on it.)


## Prefunctions and prerelations

As [[functions]] go between sets, so __prefunctions__ go between presets.  (Bishop used the term 'operation' instead of 'prefunction', but 'operation' has many other meanings.)  Even if $X$ and $Y$ are sets, a prefunction from $X$ to $Y$ is not the same as a function from $X$ to $Y$, because a prefunction need not preserve equality; that is, we may have $a = b$ without $f(a) = f(b)$.  Conversely, we may define a function as a prefunction (between sets) that preserves equality; such a prefunction is said to be __extensional__.

For example, consider the identity prefunction on the underlying preset of both $Q^+$ and $Z^+ \times Z^+$, as defined above.  From $Z^+ \times Z^+$ to $Q^+$, this is a function, since $a/b = c/d$ if $(a,b) = (c,d)$.  But from $Q^+$ to $Z^+ \times Z^+$, it is not a function, since (for example) $2/4 = 3/6$ but $(2,4) \neq (3,6)$.  A related example is the operation of taking the numerator of a (positive) rational number; from $Q^+$ to $Z^+$, we may view this as a prefunction but not as a function, although it is a function on $Z^+ \times Z^+$.

In general, the prefunctions from $X$ to $Y$ form a preset, since there is no way to compare them for equality.  (Of course, it is still [[predicative mathematics|impredicative]], at least in the classical sense, to form this preset.)  However, if $Y$ is a set, then these prefunctions do form a set, with $f = g$ defined to mean that $f(a) = g(a)$ for every $a$ in $X$.  If $X$ is also a set, then the [[function set]] from $X$ to $Y$ is a [[subset]] of this set of prefunctions.

Composition of prefunctions is also possible, but likewise does not preserve equality. If $A$ is a preset, then the elements of $A$ could be thought of as prefunctions from the terminal preset $1$ to $A$. 

A (say binary) __prerelation__ between $X$ and $Y$ may be thought of as a prefunction from $X \times Y$ to [[truth values]].  Even if one is too predicative to allow a (pre)set of truth values, still one may have a notion of prerelation, by fiat if nothing else.  Note that one *can* compare prerelations for equality; $R = S$ means that $a \sim_R b$ if and only if $a \sim_S b$.  (In other words, a preset of truth values becomes a set under the biconditional, so we can compare functions to it.)  We define a [[relation]] between sets to be a prerelation that respects equality.

Many properties of relations can also be predicated of prerelations, but not all.  In particular, prerelations may be [[reflexive relation|reflexive]], [[symmetric relation|symmetric]], and [[transitive relation|transitive]], so we have a notion of equivalence prerelation, which completes the definition of sets in terms of presets.  A prerelation may also be [[entire relation|entire]], but it makes no sense to ask if it is [[functional relation|functional]] unless $Y$ is a set.  In that case, there is a correspondence between prefunctions and functional entire prerelations as usual.  In general, however, there is no way to define the prerelation corresponding to a given prefunction (which would be a sort of pre-[[graph of a function|graph]]).  In other words, the idea that functions are certain relations (namely the functional entire ones) does not extended to prefunctions and prerelations unless $Y$ is a set.


## Formalisation

Many [[foundations]] based on [[type theory]], such as those of Per Martin-L&#246;f and Thierry Coquand, use [[type|types]] (sometimes called 'sets', but they don\'t have [[quotient set|quotients]]) which behave something like presets (and are sometimes even called 'presets').  Then a [[set]] (sometimes called '[[setoid]]') is defined as above, as a type with an equality relation.  However, these types usually come equipped with '[[identity type|identity]]' relations, which are equality relations in all but name; this amounts to saying that every preset has a [[free object|free]] set, a __completely presented set__.  (Note that the cofree set on a preset always exists; it is a [[subsingleton]].)  They usually also adopt an [[axiom of choice]] for prefunctions that, together with the identity relations, proves the [[presentation axiom]] (a weak form of the full axiom of choice) for general sets.

It is possible to develop type-theoretic foundations in which presets are *not* equipped with identity relations (only metamathematical identity or interconvertibilty *judgements*); see [[tobybartels:preset]] for some discussion.  The presentation axiom is not provable in the base theory, although it is provable in the impredicative version (where identity relations can be defined, following [[Gottfried Leibniz|Leibniz]]\'s definition of equality).  A similar result holds for [[SEAR plus epsilon|SEAR+$\epsilon$]].

The sorts in [[Michael Makkai]]\'s [[FOLDS]] are presets.  FOLDS is very different from the other foundations considered above, since it is based strictly on prerelations and has no notion of prefunction.  As far as I can tell, it therefore does not prove the presentation axiom.

If you are willing to accept the presentation axiom, then you can define a notion of preset internal to a given theory of sets: as a [[projective set]].  (With the full axiom of choice, therefore, a preset is simply a set.)  Alternatively, you might forgo presets as such but define a prefunction between sets to be an entire relation; although not everything translates, some of the properties are similar.


## Applications

To make the [[principle of equivalence]] hold automatically, a [[category]] should have only a preset of [[objects]] and only its [[hom-sets]] as sets.  Then a category whose set of objects *is* a set may be called a [[strict category]], which is really a special case of a [[strict ∞-category]].  Alternatively, one may keep sets as sets but adopt pre[[class]]es; then a [[small category]] is strict but a large category is not.

In [[constructive mathematics]], we want the [[real numbers]] to form a [[linearly ordered set|linearly ordered]] [[Heyting field]] $R$ with completeness for located [[Dedekind cuts]].  Using [[power sets]] and a set $N$ of [[natural numbers]], one may form $R$ directly as a [[subset]] of $\mathcal{P}N$ (or something equivalent), but what if you wish to be (at least weakly) [[predicative mathematics|predicative]]?  Using [[function sets]], one may form the Cauchy reals as a [[subquotient]] of $N^N$, but these are complete in the desired sense only if a weak form of [[countable choice]] (which follows from either the presentation axiom or [[excluded middle]]) holds.  (Essentially, there may not be enough [[sequences]] of natural numbers.)  Alternatively, if you have them, you can use prefunction sets and form $R$ as a subquotient of the set of _presequences_ of natural numbers.

The construction of $R$ above may also be done with entire relations if the [[axiom of fullness]] holds (see also [[real numbers object]]).  Conversely, the axiom of fullness follows from the existence of presets of prefunctions; in addition to defining a functional entire prerelation, a prefunction between sets also defines an entire relation, and the set of these satisfies fullness.  (This is related to the idea that prefunctions between sets may be formalised as entire relations.)

See also the discussion at [[net]] about how to force the domain of a net to be [[partially ordered|partial order]], by using either entire relations or prefunctions as nets.


## Fixing inadequate foundations

Sometimes one finds a [[foundation]] of [[predicative mathematics]] in which it appears to be impossible to construct [[quotient sets]], leading to much hand-wringing.  (For a simple example, simply remove the axiom of [[power sets]] from [[ZFC]] as normally presented.)  However, if you reinterpret the nominal 'sets' as presets and define a set as a preset equipped with an equivalence prerelation, then quotient sets exist after all.  (In impredicative mathematics, there is a more familiar construction of a quotient set available, as a subset of a power set.)

Assuming (as usual) that the original foundation had equality relations on its sets, there will be identity prerelations on the presets, leading to a special class of sets (those which arise from equipping a preset with its identity prerelation) which we may again call the __completely presented sets__.

When you do this, the new kind of set is usually called a '[[setoid]]', and then there may be hand-wringing about the need to use setoids instead of sets as one would like.  But if you didn\'t have quotient sets originally, then you shouldn\'t have been talking about 'sets' in the first place; theories of sets without quotient sets are really theories of presets.  (You can also use the term '[[type]]' if it seems appropriate.)

In general, the [[category]] of sets is the [[ex/lex completion]] of the original category of presets (at least assuming certain structure in the original theory).


## Related concepts

* [[type theory]]

* [[Bishop set]], [[predicative topos]]


[[!include types and logic - table]]


[[!redirects preset]]
[[!redirects presets]]
[[!redirects pre-set]]
[[!redirects pre-sets]]

[[!redirects prefunction]]
[[!redirects prefunctions]]
[[!redirects pre-function]]
[[!redirects pre-functions]]

[[!redirects extensional function]]
[[!redirects extensional functions]]
[[!redirects extensional operation]]
[[!redirects extensional operations]]
[[!redirects extensional prefunction]]
[[!redirects extensional prefunctions]]
[[!redirects extensional pre-function]]
[[!redirects extensional pre-functions]]

[[!redirects prerelation]]
[[!redirects prerelations]]
[[!redirects pre-relation]]
[[!redirects pre-relations]]

[[!redirects completely presented set]]
[[!redirects completely presented sets]]
