## Idea

A _preset_ is a [[set]] without an [[equality relation]].  Conversely, a set may be defined as a preset $X$ equipped with an equality relation (technically an [[equivalence relation|equivalence]] _prerelation_ on $X$).


In his seminal work _The Foundations of Constructive Analysis_ (1967), [[Errett Bishop]] explained what you must do to define a _set_ in three steps:

1. You must state what one must do to construct an element of the set;
2. Given two elements constructed as in (1), you must state what one must do to prove that the elements are equal;
3. You must prove that the relation defined in (2) is reflexive, symmetric, and transitive (which can be phrased in similar 'what one must do' terms, but that\'s kind of wordy).

If you only do (1), then you don\'t have a set, according to Bishop; you only have a _preset_.


A given preset may define many different sets, depending on the equality relation.  For example, the set $\dot{Q}^+$ of positive rational numbers may be defined using the same preset as the set $\dot{Z}^+ \times \dot{Z}^+$ of ordered pairs of positive integers, but the equality relation is different; two pairs $(a,b)$ and $(c,d)$ of integers are equal iff $a = c$ and $b = d$, while two rational numbers $a/b$ and $c/d$ are equal iff $a d = b c$.  (Of course, these definitions require that one already have the set $\dot{Z}^+$ of positive integers, including its equality relation, and the operation of multiplication on it.)


+-- {: .standout}
Everything after this is pretty speculative.
=--


## Prefunctions and prerelations

As [[functions]] go between sets, so __prefunctions__ go between presets.  Even if $X$ and $Y$ are sets, a prefunction from $X$ to $Y$ is not the same as a function from $X$ to $Y$, because a prefunction need not preserve equality; that is, we may have $a = b$ without $f(a) = f(b)$.  Conversely, we may define a function as a prefunction that preserves equality.

For example, consider the identity prefunction on the underlying preset of both $\dot{Q}^+$ and $\dot{Z}^+ \times \dot{Z}^+$, as defined above.  From $\dot{Z}^+ \times \dot{Z}^+$ to $\dot{Q}^+$, this is a function, since $a/b = c/d$ if $(a,b) = (c,d)$.  But from $\dot{Q}^+$ to $\dot{Z}^+ \times \dot{Z}^+$, it is not a function, since (for example) $2/4 = 3/6$ but $(2,4) \neq (3,6)$.

In general, the prefunctions from $X$ to $Y$ form a preset, since there is no way to compare them for equality.  (Of course, it is still [[predicative mathematics|impredicative]] to form this preset.)  However, if $Y$ is a set, then these prefunctions do form a set, with $f = g$ defined to mean that $f(a) = g(a)$ for every $a$ in $X$.

A (say binary) __prerelation__ between $X$ and $Y$ may be thought of as a prefunction from $X \times Y$ to [[truth values]].  Even if one is too predicative to allow a (pre)set of truth values, still one may have a notion of prerelation, by fiat if nothing else.  Note that one *can* compare prerelations for equality; $R = S$ means that $a \sim_R b$ if and only if $a \sim_S b$.  (In other words, a preset of truth values becomes a set under the biconditional, so we can compare functions to it.)  We define a [[relation]] between sets to be a prerelation that respects equality.

Many properties of relations can also be predicated of prerelations, but not all.  In particular, prerelations may be [[reflexive relation|reflexive]], [[symmetric relation|symmetric]], and [[transitive relation|transitive]], so we have a notion of equivalence prerelation, which completes the definition of sets in terms of presets.  A prerelation may also be [[entire relation|entire]], but it makes no sense to ask if it is [[functional relation|functional]] ... unless $Y$ is a set.  In that case, there is a correspondence between prefunctions and functional entire prerelations as usual.  In general, however, there is no way define the prerelation corresponding to a given prefunction.


## Formalisation

Many [[foundations]] based on [[type theory]], such as those of Per Martin-L&#246;f and Thierry Coquand, use [[type|types]] (sometimes called 'sets', but they don\'t have [[quotient set|quotients]]) which behave something like presets (and are sometimes even called 'presets').  A [[set]] (sometimes called '[[setoid]]') is defined as above, as a type with an equality relation.  However, these usually (always?) come equipped with 'identity' relations, which are equality relations in all but name; this amounts to saying that every preset has a [[free object|free]] set, a [[completely presented set]].  (Note that the cofree set on a preset always exists; it is a [[subsingleton]].)  They usually (always?) also adopt an [[axiom of choice]] for prefunctions that, together with the identity relations, proves [[COSHEP]] (a weak form of the full axiom of choice) for general sets.

I ([[Toby Bartels]]) have developed type-theoretic foundations in which presets are *not* equipped with identity relations (only metamathematical identity or interconvertibilty *judgements*).  I probably should finish writing that up now; but see [[tobybartels:preset]] for some discussion.  COSHEP is not provable in the base theory, although it is provable in the impredicative version (where identity relations can be defined).  A similar result holds for [[SEAR+?]].

The sorts in [[Michael Makkai]]\'s [[FOLDS]] are presets.  FOLDS is very different from the other foundations considered above, since it is based strictly on prerelations and has no notion of prefunction.  Does it have any flaws?  Maybe not!  I should learn more about it.

If you are willing to accept COSHEP, then you can define a preset to be a [[projective set]].  (With the full axiom of choice, therefore, a preset is simply a set.)  Alternatively, you might forgo presets as such but define a prefunction between sets to be an entire relation; although not everything translates, some of the properties are similar.


## Applications

To avoid [[evil]], a [[category]] should have a preset of [[objects]] and only its [[hom-sets]] as sets.  Then a category whose set of objects *is* a set may be called a [[strict category]], which is as evil as (and really a special case of) a [[strict ∞-category]].  Alternatively, one may keep sets as sets but adopt pre[[class]]es; then a [[small category]] is strict but a large category is not.

In [[constructive mathematics]], we want the [[real numbers]] to form a [[linearly ordered set|linearly ordered]] [[Heyting field]] $R$ with completeness for located Dedekind cuts.  Using [[power sets]] and a set $N$ of [[natural numbers]], one may form $R$ directly as a [[subset]] of $\mathcal{P}N$, but what if you wish to be predicative?  Using [[function sets]], one may form the Cauchy reals as a [[subquotient]] of $N^N$, but these are complete in the desired sense only if a weak form of [[countable choice]] (which follows from either COSHEP or [[excluded middle]]) holds.  (Essentially, there may not be enough [[sequences]] of natural numbers.)  Alternatively, use prefunction sets and form $R$ as a subquotient of the set of _presequences_ of natural numbers.

The construction of $R$ above may also be done with entire relations if the [[axiom of fullness]] holds.  Conversely, the axiom of fullness follows from the existence of presets of prefunctions; in addition to defining a functional entire prerelation, a prefunction between sets also defines an entire relation, and the set of these satisfies fullness.  (This is related to the idea that prefunctions between sets may be formalised as entire relations.)

See also the discussion at [[net]] about how to force the domain of a net to be [[partially ordered|partial order]], by using either entire relations or prefunctions as nets.


[[!redirects pre-set]]
[[!redirects presets]]
[[!redirects pre-sets]]
[[!redirects prefunction]]
[[!redirects prerelation]]
[[!redirects pre-function]]
[[!redirects pre-relation]]
[[!redirects prefunctions]]
[[!redirects prerelations]]
[[!redirects pre-functions]]
[[!redirects pre-relations]]