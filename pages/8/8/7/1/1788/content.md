
**Clifford theory**

* Richard Roth: *On restricting irreducible characters to normal subgroups*, Pacific J. Math. **59** 1 (1975)

* Wikipedia: *[Clifford theory](https://en.wikipedia.org/wiki/Clifford_theory)*

***

Suppose
$$f,g\colon(X,M,N)\to(X',M',N')$$
are [[measurable maps]] that are equal almost everywhere.
Suppose that
$$h\colon(X',M',N')\to(\{0,1\},2^{\{0,1\}},\{\emptyset\})$$
is a measurable map.
Such measurable maps are in bijection with elements of $M'$: the bijection sends $h$ to $h^{-1}\{1\}$, and the inverse bijection sends a subset $m'\in M'$ to its [[characteristic function]] $\chi_{m'}$.

We have
$$[h\circ f\ne h\circ g]=f^{-1}m'\oplus g^{-1}m',$$
where $m'=h^{-1}\{1\}$ is as above.
Since
$$f^{-1}m'\oplus g^{-1}m' \subset [f\ne g],$$
the set $f^{-1}m'\oplus g^{-1}m'$ is subnegligible.

The condition stating that the set $f^{-1}m'\oplus g^{-1}m'$ is subnegligible for all $m'\in M'$,
is very much compatible with the ideology of [[measure theory]]: it says that the preimages of an arbitrary measurable subset under the maps $f$ and $g$ are the same almost everywhere.

It is quite natural to ask whether the converse holds.
For example, two continuous maps $f,g\colon X\to X'$ of [[T_0|T_0-topological spaces]] are equal if and only if for every open subset $U'\subset X'$ we have $f^{-1}U'=g^{-1}U'$.
In measure theory, equality of sets should be replaced with equality almost everywhere,
meaning for every $m'\in M'$ the symmetric difference $f^{-1}m'\oplus g^{-1}m'$ is subnegligible.

However, [Fremlin](#Fremlin) (Example 343I) constructs an example of a measurable negligibility-reflecting map $f:(X,M,\mu)\to(X,M,\mu)$ (where $(X,M,\mu)=\{0,1\}^{\mathfrak{c}}$ is a product of continuum many discrete measurable spaces $\{0,1\}$) such that for every $x\in X$ we have $f(x)\ne x$, but for every $m\in M$, the set $f^{-1}m\oplus m$ is negligible.
Thus, the identity map $id_X$ is not equal to $f$ almost everywhere and yet, $id_X$ and $f$ have the same preimage maps, up to subnegligible sets.

Such a situation is pathological, and is it turns out, it is the condition of having the same preimages up to subnegligible sets that produces nonpathological theory when the two conditions differ (they do coincide for many spaces, as we will see below).

These considerations naturally lead us to a coarser equivalence relation.

\begin{definition}
Two measurable maps
$$f,g\colon(X,M,N)\to(X',M',N')$$
are __weakly equal almost everywhere__ if for every $m'\in M'$ the set
$$f^{-1}m'\oplus g^{-1}m'$$
is a subnegligible set.
\end{definition}

Equality almost everywhere implies weak equality almost everywhere.
The converse is true if $(X',M',N')$ is __countably separated__ (Fremlin, Proposition 343F), i.e., there is a countable subset $M''\subset M'$ that covers $X'$ and for any two points of $X'$ there is an element of $M''$ that contains exactly one of them.

An enhanced measurable space is countably separated if and only if it admits an injective measurable map into real numbers.  Most measurable spaces (other than some counterexamples) in an introductory real analysis book are countably separated, which explains why the finer equivalence relation of equality almost everywhere is sufficient for many practical purposes.

### The category of enhanced measurable spaces

We collect what we have learned so far.

* Measurable spaces $(X,M)$ do not have enough information: they lack the data of sets of measure 0.

* Measure spaces $(X,M,\mu)$ have too much information: they require us to make arbitrary unnecessary choices of measures $\mu$.

* Enhanced measurable spaces $(X,M,N)$ have just the right amount of information.

* The condition of measurability of maps, i.e., reflection of measurable sets, must be strengthened to also require reflection of negligible sets, to ensure its compatibility with precomposition.

* The equivalence relation of equality almost everywhere must be coarsened to weak equality almost everywhere to ensure morphisms are fully determined by their preimages up to subnegligible sets.

* Optionally, if we want to incorporate enhanced measurable spaces that are not complete or locally determined, instead of requiring maps to reflect measurable and negligible sets, we must require them to reflect σ-subnegligible sets and symmetric differences of σ-subnegligible sets and σ-measurable sets.  The resulting category is equivalent to the category of complete locally determined enhanced measurable spaces.

Assembling these properties together, we arrive at the following definition.

\begin{definition}
The __category of enhanced measurable spaces__ is constructed as a [[quotient category]].
Objects are enhanced measurable spaces $(X,M,N)$, where $X$ is a set, $M$ is a [[σ-algebra]], $N$ is a [[σ-ideal]].  Morphisms are maps of sets that reflect measurable sets and negligible sets.  Two morphisms are equivalent if they are weakly equal almost everywhere.
\end{definition}

## Localizability

The category of enhanced measurable spaces captures the desired properties of measurable spaces and measurable maps as they are used in real analysis.

To complete the construction, we must eliminate pathological objects that invalidate the main theorems of measure theory.  In traditional textbooks on measure theory, this is accomplished by restricting to σ-finite measure spaces and/or [[Radon measures]].

We consider a simple generalization of σ-finiteness known as _strict localizability_, as well as an abstract formulation of Radon measures, known as _compactness_ (introduced by Marczewski; not to be confused with compactness of [[topological spaces]], to which it is closely related).

### Localizability as a necessary prerequisite for measure theory

We review some classic results due to Irving E. Segal and John L. Kelley.
As explained in the next section, the localizability property is still not quite enough to eliminate all the pathologies.
However, it does explain the Boolean algebra side of the story.

\begin{theorem}
(Irving E. Segal, 1951; John L. Kelley, 1966.)
The following properties are equivalent for an enhanced measurable space $(X,M,N)$ that admits a faithful semifinite measure.

* The [[Boolean algebra]] $M/N$ is complete.

* The Lebesgue decomposition for σ-ideals holds.

* The [[Hahn decomposition theorem]] holds for signed measures.

* The [[Radon–Nikodym theorem]] holds.

* The [[Riesz representation theorem]] holds: the canonical map $L^\infty\to(L^1)^*$ is an isomorphism.

* $L^\infty(X,M,N)$ is a [[commutative von Neumann algebra]].

A __localizable enhanced measurable space__ is an enhanced measurable space that admits a faithful semifinite measure and satisfies any of the above equivalent properties.
\end{theorem}

The takeaway from this result is that without the localizability property much of the [[measure theory]] as we know is false,
so it is completely reasonable to require it from the start.

We can also establish an analogue of the above theorem for morphisms.

\begin{theorem}
(The relative Kelley–Segal theorem.)
The following properties are equivalent for a morphism of localizable enhanced measurable spaces $f\colon(X,M,N)\to(X',M',N')$.

* The induced homomorphism of [[Boolean algebras]] $f^{-1}\colon M'/N'\to M/N$ is complete, i.e., preserves suprema.

* The map $f^{-1}$ preserves the generator of σ-ideals provided by the Lebesgue decomposition.

* The pushforward map $f_*$ on measures preserves the Hahn decomposition.

* The relative [[Radon–Nikodym theorem]] holds: $f_*(f^* h\cdot \mu)=h\cdot f_*\mu$.

* The induced map $f_*\colon L^1(X,M,N)\to L^1(X',M',N')$ is a bounded linear map of Banach spaces.

* The induced \*-homomorphism $f^*$ of [[*-algebras]] of bounded real-valued functions on $X$ is a normal \*-homomorphism of [[commutative von Neumann algebras]].

A __localizable map__ of enhanced measurable spaces is a morphism of enhanced measurable spaces that satisfies any of these equivalent properties.
\end{theorem}

Again, the takeaway here is that we really want to only use localizable maps if we want to avoid a complete breakdown of measure theory as we know it.

Surprisingly, once we impose conditions on objects (namely, strict localizability and compactness) that eliminate pathological objects,
it turns out that _all_ maps between such objects are localizable.
This is a deep theorem essentially due to [Fremlin](#Fremlin) (implicitly contained in §451Q).

### Enhanced measurable spaces and complete Boolean algebras

In the previous section we constructed (essentially by definition) a functor
$$LEMS \to CBAlg^{op}$$
from the category of localizable enhanced measurable spaces and localizable maps
to the opposite category of [[complete Boolean algebras]] and complete homomorphisms of Boolean algebras.

This functor lands inside complete Boolean algebras $A$ that admit a faithful semifinite measure,
i.e., a map of sets $\mu\colon A\to[0,\infty]$ that is completely additive, vanishes only on 0,
and $1=\sup \mu^{-1}[0,\infty)$.
We refer to such Boolean algebras as __localizable Boolean algebras__.

Thus, the above functor descends to a functor
$$LEMS \to LBAlg^{op}.$$

The opposite category of $LBAlg$ is known as the __category of [[measurable locales]]__,
since every complete morphism of complete Boolean algebras is a morphism of [[frames]],
so localizable Boolean algebras form a [[full subcategory]] of [[frames]].

### Stone and Gelfand dualities for localizable Boolean algebras

The [[Stone duality]] is an equivalence of categories from the opposite category of [[Boolean algebras]]
to the category of [[Stone spaces]] (or [[Stone locales]]).
It restricts to an equivalence of categories from the opposite category of [[complete Boolean algebras]] and complete homomorphisms of Boolean algebras
to the category of [[Stonean spaces]] (or [[Stonean locales]]) and open maps.
Restricting further to the full category of localizable Boolean algebras, the essential image of the Stonean duality functor
is precisely the full subcategory of [[hyperstonean spaces]] (or [[hyperstonean locales]]) and open maps ([Pavlov](#Pavlov), Propositions 2.72, 2.73).

The [[Gelfand duality]] is an equivalence of categories from the opposite category of (unital) [[commutative C*-algebras]] and (unital) \*-homomorphisms
and the category of [[compact Hausdorff spaces]] (or [[compact regular locales]]).
It restricts to an equivalence of categories from the opposite category of [[commutative von Neumann algebras]] and (unital) normal \*-homomorphisms
to the category of [[hyperstonean spaces]] (or [[hyperstonean locales]]) and open maps.
Furthermore, this equivalence factors through the opposite category of localizable Boolean algebras:
the relevant functor sends a [[commutative von Neumann algebra]] to the localizable Boolean algebra of its projections
and a (unital) normal \*-homomorphism of [[commutative von Neumann algebras]] to the induced complete homomorphism of Boolean algebras of projections ([Pavlov](#Pavlov), Theorem 3.20).

\begin{theorem}
([Pavlov](#Pavlov), Propositions 2.72, 2.73; Theorem 3.20.)
The following four categories are equivalent.

* The opposite category of [[commutative von Neumann algebras]] and unital normal \*-homomorphisms.

* The opposite category of localizable Boolean algebras and complete homomorphisms.

* The category of [[hyperstonean locales]] and open maps.

* The category of [[hyperstonean spaces]] and open maps.

\end{theorem}

We take this theorem as a strong evidence that whatever good category of enhanced measurable spaces
we end up constructing, it better be equivalent to the above four categories.

We have already constructed a functor
$$LEMS \to LBAlg^{op}.$$
In the next section, we construct a functor
$$LBAlg^{op}\to LEMS$$
that exhibits $LBAlg^{op}$ as a [[retract]] (in particular, a [[full subcategory]]) of $LEMS$.

### The Loomis–Sikorski construction

The functor
$$LBAlg^{op}\to LEMS$$
is constructed as the composition of functors
$$LBAlg^{op}\to HStonean\to LEMS,$$
where the first functor is the [[hyperstonean duality]] functor explained in the previous section.

The second functor is known as the __Loomis–Sikorski construction__ ([Loomis](#Loomis), 1947; [Sikorski](#Sikorski), 1948; see also [Pavlov](#Pavlov), Definition 5.2) and is defined as follows.
Send a [[hyperstonean topological space]] $(X,U)$ to the enhanced measurable space $(X,M,N)$,
where $N$ is the [[σ-ideal]] of [[nowhere dense sets]] (equivalently in the case of [[hyperstonean spaces]]: [[meager sets]])
and $M$ is the [[σ-algebra]] of subsets with the property of Baire, i.e., [[symmetric differences]] of [[clopen subsets]] and [[nowhere dense sets]].

The quotient [[Boolean algebra]] $M/N$ is easily seen to be precisely the [[complete Boolean algebra]] of [[clopen subsets]] of $X$
and the latter is precisely the inverse of the [[Stone spectrum]] functor evaluated on $(X,U)$.
Thus, the Loomis–Sikorski construction indeed exhibits $LBAlg^{op}$ as a retract of $LEMS$.

### Summary

We have seen that in order to have a theory resembing conventional measure theory,
we have to work with localizable enhanced measurable spaces and localizable morphisms.

As it turns out, the essential image of the Loomis–Sikorski functor
is the full subcategory of enhanced measurable spaces
comprising precisely compact and strictly localizable enhanced measurable spaces, defined in the next section.

In particular (and rather surprisingly), all morphisms of compact strictly localizable enhanced measurable spaces
are automatically localizable, even though there are examples (one of which is given below) of nonlocalizable morphisms from a σ-finite enhanced measurable space
to a completely atomic (i.e., discrete) enhanced measurable space, both of which are localizable.

Thus, if one finds the necessity of extending the above equivalence of four categories to include some form of enhanced measurable spaces
convincing enough, one can skip the next section and proceed directly to the summary.
Below, we provide additional independent motivation for strict localizability and compactness that does not rely on the above reasoning.

## The subtle points: strict localizability and compactness

### Strict localizability

We already established in the previous section that it is highly desirable (e.g., for Gelfand duality)
to be able to lift complete homomorphisms of Boolean algebras $M'/N'\to M/N$
to morphisms of enhanced measurable spaces $(X,M,N)\to(X',M',N')$.

Consider the simplest case when $(X',M',N')=(X',2^{X'},\{\emptyset\})$ is a discrete enhanced measurable space.

Then complete homomorphisms $2^{X'}\to M/N$ can be identified
with $X'$-indexed families of elements $p_i\in M/N$ ($p\in X'$)
such that $i\ne j$ implies $p_i p_j=0$
and $\sup_i p_i=1$.
That is to say, the elements $p_i$ form a partition of 1 in the complete Boolean algebra $M/N$.

Likewise, measurable maps $(X,M,N)\to(X',2^{X'},\{\emptyset\})$
can be identified with $X'$-indexed families of elements $P_i\in M$
such that $i\ne j$ implies $P_i\cap P_j=\emptyset$
and $\bigcup_i P_i=X$.
That is to say, the sets $P_i$ form a (disjoint) partition of $X$.

Lifting complete homomorphisms $2^{X'}\to M/N$
to morphisms of enhanced measurable spaces $(X,M,N)\to(X',2^{X'},\{\emptyset\})$
amounts to constructing $P_i$ such that the equivalence class of $P_i$ in $M/N$ equals $p_i$.

Pick some arbitrary representative $Q_i$ for every $p_i$.
For every $i\ne j$ we have $p_i p_j = 0$, hence $Q_i \cap Q_j \in N$.
Furthermore, $X$ is the essential supremum of $Q_i$.
The question is then whether it is possible to find $P_i$ such that $P_i\oplus Q_i\in N$
and $P_i$ are disjoint.

Surprisingly, the answer is negative in general.

An enhanced measurable space $(X,M,N)$ is __strictly localizable__
if it is isomorphic to the coproduct of a set-indexed family of σ-finite enhanced measurable spaces.

Coproducts of enhanced measurable spaces are computed in the expected manner:
$$\coprod_i (X_i,M_i,N_i)=\left(\coprod_i X_i,\prod_i M_i,\prod_i N_i\right),$$
i.e., a subset of $\coprod_i X_i$ is measurable or negligible
if and only if its intersection with every $X_i$ is measurable or negligible, respectively.

A rather delicate example of a complete locally determined localizable measure space that is not strictly localizable can be found in [Fremlin](#Fremlin) (§216E).

It is not difficult to see that a localizable enhanced measurable space $(X,M,N)$
admits liftings of complete homomorphisms $2^{X'}\to M/N$
if and only if it is strictly localizable.
Indeed, if $(X,M,N)$ is localizable and admits liftings,
then the lifting of a σ-finite partition $p_i\in M/N$ of $1\in M/N$
is a strictly localizable partition of $X$.
Conversely, if $(X,M,N)$ is strictly localizable,
then any lifting problem for $p_i$ can be solved separately for every σ-finite $(X_i,M_i,N_i)$,
with individual solutions combined using disjoint unions.
In the σ-finite case, only countably many $Q_i$ can be nonnegligible, which allows us to take $P_i=\emptyset$
for all $i$ such that $Q_i$ is negligible, whereas for the remaining $Q_i$ we take
$P_i=Q_i\setminus \bigcup_{j\lt i}Q_j$, for some fixed well-ordering of indices $i$.

Surprisingly, the lifting property for complete homomorphisms out of complete atomic Boolean algebras
implies the lifting property for complete homomorphisms out of arbirary localizable Boolean algebras.
Thus, the latter property holds if and only if the enhanced measurable space is strictly localizable.

This is the rather deep __von Neumann–Maharam theorem__, an exposition of which can be found in [Fremlin](#Fremlin) (§341M).

Thus, if we want to be able to lift complete homomorphisms of Boolean algebras
(or, equivalently, normal unital \*-homomorphisms of commutative von Neumann algebras)
to measurable maps of measurable spaces, we have to assume strict localizability.

### Compactness

Suppose
$$f\colon(X,M,N)\to(X',M',N')$$
is a morphism of enhanced measurable spaces.

What subset of $X'$ should we take as the __image of $f$__?

The ordinary image of $f$ as a map of sets does not result in a useful notion.
Indeed, suppose $M=N$, i.e., $X\in N$.
Then every map of sets $X\to X'$ defines a morphism of enhanced measurable spaces,
since every subset of $X$ is a subnegligible set.
If the cardinality of $X$ is at least the cardinality of $X'$,
then every subset of $X'$ is the image of some measurable map $f\colon X\to X'$.
In particular, such a subset need not be measurable.

On the other hand, we have already seen that the enhanced measurable space $(X,M,N)$
is isomorphic to the empty space $(\emptyset,\{\emptyset\},\{\emptyset\})$.
It is reasonable to assume that the notion of the image of a morphism
should be invariant under isomorphisms of enhanced measurable spaces.
In particular, we expect the image of $f$ to be empty, or equivalent to the empty set, i.e., negligible.

To resolve the contradiction, we modify the definition to allow for images-up-to-a-subnegligible subset.

\begin{definition}
Suppose
$$f\colon(X,M,N)\to(X',M',N')$$
is a morphism of enhanced measurable spaces.
The __essential image__ of $f$ (if it exists)
is an element $A\in M'$ such that $f^{-1}(X'\setminus A)\in N$
and for every $B\in M'$ such that $f^{-1}(X'\setminus B)\in N$
we have $A\setminus B\in N'$.
\end{definition}

All essential images of $f$ taken together form a (unique) equivalence class in $M'/N'$.

For example, in the above example, the essential image of $f$ is always negligible,
even if the ordinary image coincides with $X$.

However, the essential image of $f$ does not always exist.
Consider a set $X$ together with a probability measure $\mu\colon 2^X\to[0,1]$
such that for every $x\in X$ we have $\mu(\{x\})=0$.
Such measures exist if and only if $X$ has the cardinality of a [[real-valued-measurable cardinal]], a type of a [[large cardinal]].
The identity map of sets $X\to X$ defines a morphism of enhanced measurable spaces
$$f\colon(X,2^X,N_\mu)\to(X,2^X,\{\emptyset\}).$$

Given any $A\in 2^X$ such that $X\setminus A\in N$,
for every $a\in A$ we have $X\setminus B\in N$, where $B=A\setminus\{a\}$.
Thus, if $A$ is the essential image of $f$, then we must have $A=\emptyset$,
a contradiction since $X\setminus A\notin N$.

To eliminate pathological examples such as the one given above, we need to require $(X,M,N)$ to be a __compact enhanced measurable space__.
Compactness is the “abstract essence” of the notion of Radon measure that is not affixed to any particular topology on the underlying set.
It was first introduced by [Marczewski](#Marczewski).

\begin{definition}
An enhanced measurable space $(X,M,N)$ is __compact__
if there is a compact class $K\subset M$ such that for any $m\in M\setminus N$ there is $k\in K\setminus N$ such that $k\subset m$.
A collection $K\subset 2^X$ of subsets of a set $X$ is a __compact class__ if for any $K'\subset K$ the following [[finite intersection property]] holds:
if for any finite $K''\subset K'$ we have $\bigcap K''\ne\emptyset$, then also $\bigcap K'\ne\emptyset$.
\end{definition}

To connect to the notion of a [[compact topological space]], observe ([Fremlin](#Fremlin), Lemma 342D(a))
that $K\subset 2^X$ is a compact class 
if and only if there is a compact topology on the set $X$
such that every element of $K$ is a closed (and hence compact) subset of $X$.
Thus, an enhanced measurable space is compact if and only if it admits
a compact topology such that every nonnegligible measurable set contains a nonnegligible subset that is closed ([Fremlin](#Fremlin), Corollary 342F).

A __Radon enhanced measurable space__ is an enhanced measurable space
equipped with a structure of a Hausdorff topological space such that
the [[σ-algebra]] of measurable sets contains open sets and there is a faithful measure
that is locally finite (every point has a neighborhood of finite measure)
and inner regular with respect to compact subsets (the measure of any measurable subset is the supremum of measures of its compact subsets).
(See [Fremlin](#Fremlin) Definition 411H(b).)
Every Radon enhanced measurable space is compact and strictly localizable by [Fremlin](#Fremlin) (Proposition 416W(a), Theorem 414J).

The following theorem answers the question of existence of the essential image in the affirmative
in the case when the domain of $f$ is a __compact__ enhanced measurable space.
The crucial ingredient is a deep result of [Fremlin](#Fremlin) (§451Q)
that shows that a compact enhanced measurable space whose σ-ideal of negligible sets is induced by a faithful semifinite measure
cannot be partitioned into an uncountable family of negligible sets whose arbitrary unions are measurable subsets.

\begin{theorem}
([Pavlov](#Pavlov), Proposition 4.65.)
Suppose $(X, M, N)$ is a compact enhanced measurable space that admits a faithful 
semifinite measure, $(X',M',N')$ is a strictly localizable enhanced measurable space, and $f\colon (X, M, N) \to (X', M', N')$ is a morphism of enhanced measurable spaces.
Then $f$ admits an essential image.
\end{theorem}

It is easy to see that the essential image of $f$ (if it exists) must be the complement of the essential supremum $p$ of all $m'\in M'$ such that $f^{-1}m'\in N$.
The difficult part is to show that $f^{-1}p\in N$, and this is exactly what Fremlin's theorem achieves.

As an added bonus, we obtain the following counterpart to the von Neumann–Maharam co-lifting theorem for strictly localizable spaces.

\begin{theorem}
(von Neumann 1932; C. Ionescu Tulcea 1965; Vesterstrøm–Wils 1969; Edgar 1976; Graf 1980; see also [Fremlin](#Fremlin), Theorem 343B(iv).)
Suppose $(X,M,N)$ is an enhanced measurable space that admits a faithful semifinite measure.
Assume $X\notin N$.
The following two conditions are equivalent.

* For every $m\in M\setminus N$ there is $a\in M\setminus N$ such that $a\subset m$ and $a$ is compact.
(If $(X,M,N)$ is strictly localizable, this condition implies compactness of $X$.)

* For every strictly localizable enhanced measurable space $(X',M',N')$ and complete homomorphism of localizable Boolean algebras $\phi\colon M/N\to M'/N'$
there is a morphism of enhanced measurable spaces $(X',M',N')\to(X,M,N)$ that induces $\phi$.

\end{theorem}

### Equivalence to the four other categories

Previously, we constructed a functor
$$LBAlg \to CSLEMS$$
from localizable Boolean algebras and complete homomorphisms
to enhanced measurable spaces.
The Loomis–Sikorski construction applied to [[hyperstonean spaces]]
produces compact and strictly localizable spaces, thus landing in the category $CSLEMS$
of compact strictly localizable enhanced measurable spaces.

We also constructed a functor
$$LEMS \to LBAlg, \qquad (X,M,N)\mapsto M/N,$$
which we can now restrict to a functor
$$CSLEMS \to LBAlg.$$

Previously, we saw that the compustion
$$LBAlg \to CSLEMS \to LBAlg$$
is isomorphic to the identity functor.

Showing that the composition
$$CSLEMS \to LBAlg \to CSLEMS$$
is isomorphic to the identity functor is much more difficult.
Indeed, the construction of the isomorphism and its inverse
requires the properties of compactness and strict localizability
and uses deep theorems due to von Neumann–Maharam and Ionescu Tulcea.

\begin{theorem}
([Pavlov](#Pavlov), Theorem 5.19.)
The category $CSLEMS$ is equivalent to the following four categories:

* opposite category of [[commutative von Neumann algebras]]

* opposite category of localizable Boolean algebras (i.e., [[measurable locales]])

* [[hyperstonean locales]]

* [[hyperstonean spaces]]

\end{theorem}

## Summary

The following category is suitable for [[measure theory]] in the sense that it matches the existing practice of [[real analysis]], [[probability theory]], [[stochastic processes]], etc.

* Objects are (complete) compact strictly localizable enhanced measurable spaces $(X,M,N)$.

* Morphisms $(X,M,N)\to(X',M',N')$ are equivalence classes of maps of sets $X\to X'$ that reflect measurable and negligible sets.

* Two morphisms $f$ and $g$ are equivalent if they are weakly equivalent almost everywhere for every $m'\in M'$ we have $f^{-1}m'\oplus g^{-1}m'\in N$.

The following remarks are in order.

* Enhanced measurable spaces $(X,M,N)$ have just the right amount of information: enough to define (weak) equality almost everywhere, not too much to require constructions of noncanonical measures.

* However, one could use conventional [[measure spaces]] $(X,M,\mu)$ instead, using $N_\mu$ as the [[σ-ideal]] of negligible sets.

* To ensure that composition descends to the quotient category, measurable maps must reflect negligible sets.

* The equivalence relation of equality almost everywhere must be coarsened to weak equality almost everywhere to ensure morphisms are fully determined by their preimages up to subnegligible sets.

* Completeness is optional, but simplifies some aspects of the presentation.  Local determinacy is implied by strict localizability.

* The property of strict localizability is a straightforward generalization of the notion of a σ-finite space.

* The property of compactness is an abstraction of the definition of a [[Radon measure]].

These properties eliminate pathologies and ensure the following desirable properties of objects and morphisms.

* The resulting category is equivalent to four other categories: opposite of commutative von Neumann algebras, opposite of localizable Boolean algebras (i.e., [[measurable locales]]), [[hyperstonean locales]], [[hyperstonean spaces]].

* Compact strictly localizable spaces are localizable and hence satisfy the traditional theorems of elementary measure theory: the [[Radon–Nikodym theorem]], the Hahn and Jordan decomposition theorems, the [[Riesz representation theorem]], bounded measurable functions form a [[von Neumann algebra]], the Boolean algebra $M/N$ of equivalence classes of measurable sets is complete.

* Morphisms of compact strictly localizable enhanced measurable spaces induce _complete_ homomorphisms of localizable Boolean algebras.

* Morphisms of enhanced measurable spaces admit essential images.

## Categorical properties

The category $CSLEMS$ has excellent categorical properties: it is complete and cocomplete, admits a [[closed monoidal structure]] whose product is the measure-theoretic product, is comonadic over sets and over [[compact Hausdorff spaces]].  It also admits a commutative Giry-type [[probability monad]] ([Furber](#Furber)).


## Related concepts

* [[Stone duality]], [[Gelfand duality]]

* [[commutative von Neumann algebra]]

* [[hyperstonean locale]], [[hyperstonean space]]

* [[enhanced measurable spaces]], [[measurable space]], [[measure space]], [[measure theory]]

## References

* {#Segal} [[Irving E. Segal]],  Equivalences of Measure Spaces.  American Journal of Mathematics 73:2 (1951), 275.  [doi](http://dx.doi.org/10.2307/2372178).

* {#Marczewski} [[Edward Marczewski]], _On compact measures_, Fundamenta Mathematicae 40 (1) (1953) 113–124.  [doi](https://doi.org/10.4064/fm-40-1-113-124).

* {#Kelley} [[John L. Kelley]],  Decomposition and representation theorems in measure theory.  Mathematische Annalen 163:2 (1966), 89-94.  [doi](http://dx.doi.org/10.1007/bf02052840).

* {#Fremlin} [[David H. Fremlin]], _[[Measure Theory]]_.

* {#Pavlov} [[Dmitri Pavlov]], _Gelfand-type duality for commutative von Neumann algebras_, Journal of Pure and Applied Algebra 226:4 (2022), 106884, 1–53.  [doi](https://doi.org/10.1016/j.jpaa.2021.106884).

* [[Robert Furber]], _A Probability Monad on Measure Spaces_, [PDF](https://robertfurber.com/preprints/cemonad-preprint.pdf).

* {#Furber} [[Robert Furber]], _Commutative W\*-algebras as a Markov Category (Extended Abstract)_, [PDF](https://robertfurber.com/abstracts/mcabs.pdf).
