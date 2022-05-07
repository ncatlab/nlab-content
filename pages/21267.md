This page is to provide non-technical or maybe semi-technical discussion of the nature and role of [[homotopy theory]].
For more technical details and further pointers see at [[homotopy theory]].


#Contents#
* table of contents
{:toc}

## What is homotopy theory?

## Is homotopy theory a part of algebraic topology?
{#intro}

In one of the first textbooks on homotopy theory,
_An introduction to homotopy theory_ by [[Peter J. Hilton]] (1953),
one reads:

> Since the introduction of [[homotopy groups]] by [[Hurewicz]] in 1935, homotopy theory has been occupying an increasingly prominent place in the field of [[algebraic topology]]. Important new advances are continually being made in the subject by various workers; and the recent developments emanating from
the French school of topologists underline the desirability of having available a basic introduction to homotopy theory
suitable for those who wish to undertake research in the subject
and for those who wish to be in a position to understand the
modern techniques and results.

[[Sze-Tsen Hu]] writes in _Homotopy Theory_ (1959):

> The recognition of the branch of mathematics now called homotopy theory took place in the few years after the introduction of [[homotopy groups]] by [[Witold Hurewicz]] in 1935.
Since then, with numerous advances made by various workers, it has been playing an increasingly important role in the expanding field of algebraic topology. However, there exists no textbook on the subject at any level except the extremely condensed Cambridge tract of [[P. J. Hilton]] entitled “An Introduction to Homotopy Theory.”

Thus, at the time homotopy theory was clearly identified as a part
of [[algebraic topology]].

The 1995 _[[Handbook of Algebraic Topology]]_ (edited by [[Ioan M. James]]) is overwhelmingly devoted to [[homotopy theory]].

However, the attitudes have changed since then. [[Haynes Miller]] writes in the _[[Handbook of Homotopy Theory]]_ (2019):

> This volume may be regarded as a successor to the “[[Handbook of Algebraic Topology]],” edited by [[Ioan James]] and published a quarter of a century ago.
In calling it the “[[Handbook of Homotopy Theory]],” I am recognizing that the discipline has expanded and deepened, and traditional questions of [[topology]], as classically understood, are now only one of many distinct mathematical disciplines in which it has had a profound impact and which serve as sources of motivation for research directions within homotopy theory proper.

[[Clark Barwick]] writes in _[The future of homotopy theory](https://www.maths.ed.ac.uk/~cbarwick/papers/future.pdf)_ (2018):

> Neither our subject nor its interaction with other areas of inquiry is widely understood.
Some of us^4 call ourselves _algebraic topologists_, but this has the unhelpful effect of making the subject appear to be an area of [[topology]], which I think is profoundly inaccurate.
It so happens that one way (and historically the first way) to model homotopical thinking is to employ a very particular class of topological spaces.^5
Today, the praxis of homotopy theory interacts with [[topology]] no more often than it does with [[arithmetic geometry]] and [[category theory]], and the interactions with areas like [[representation theory]] are growing rapidly.
_Homotopy theory is not a branch of topology._ This is important, because as long as homotopy theory is classified under the umbrella of topology, there will be errors of judgement in who is considered competent to judge our work; the results of this at journals, on the job market, and in funding is real and lasting.

> 4 not me

> 5 I think of homotopy theory as an enrichment of the notion of equality, dedicated to the primacy of _structure over properties_. Simplistic and abstract though this idea is, it leads rapidly to a whole universe of nontrivial structures.

## What objects does homotopy theory study?

We list some [[mathematical objects]] that are undoubtedly studied by [[homotopy theory]]:

* The first object is known under various names: [[∞-groupoid]], (homotopy) space, [[homotopy type|(homotopy) type]], more recent (and so far exotic) names include “anima”. See the [section on “spaces”](#spaces) for an explanation of why so many different names are used for (essentially) the same concept.
These objects can be modeled by [[simplicial sets]] up to [[simplicial weak equivalence]], or [[topological spaces]] up to [[weak homotopy equivalence]],
or many other models.
See the [section on models](#models) for more details about models.

* [[Spectra]] or [[stable homotopy types]].
Specific [models](#models) include [[sequential spectra]] or [[symmetric spectra]] (valued in [[simplicial sets]] or [[topological spaces]]), [[orthogonal spectra]], [[reduced excisive functors]], etc.

* [[∞-categories]], also known as [[(∞,1)-categories]], [[homotopy theories]], etc.
Specific [models](#models) include [[relative categories]], [[quasicategories]], [[simplicial categories]], [[Segal categories]], [[complete Segal spaces]], etc.
See the [section on ∞-categories](#infinity) for more information.

* [[(∞,n)-categories]], which can be [modeled](#models) by [[globular n-fold complete Segal spaces]], Rezk's [[Theta-n spaces]], etc.

## What objects does algebraic topology study?

As already explained in the [introduction](#intro),
there is a recent tendency to separate [[homotopy theory]]
from [[algebraic topology]].
This leaves the question as to what exactly [[algebraic topology]] is once the separation happens.

We list some [[mathematical objects]] that are undoubtedly studied by [[algebraic topology]]:

* [[manifolds]], as studied in [[surgery theory]], [[bordism theory]], etc.
These include [[topological manifolds]], [[PL-manifolds]], and [[smooth manifolds]].

* [[knots]], [[tangles]], [[surfaces]], and other objects arising from [[manifolds]].

* [[Lie groups]] and [[characteristic classes]].

* [[polyhedra]].

## What are “spaces” in homotopy theory?

These are some of the first and most important objects
introduced in [[homotopy theory]].

This is witnessed by the many names given to them,
which all describe the same concept but have a slightly different emphasis:

* [[∞-groupoid]], which emphasizes the categorical point of view;
* (homotopy) space, which emphasizes the original [model](#models) using [[topological spaces]] up to [[weak homotopy equivalence]];
the adjective “homotopy” can be used to distinguish
this usage from [[topological spaces]];
* [[homotopy type|homotopy type]], which emphasizes that objects in a [model](#models) are only considered up to [[weak homotopy equivalence]];
* [[type]], which alludes to [[homotopy type theory]], which aims to treat such objects as first-class citizens without invoking specific models.

Yet even this large variety of viewpoints is sometimes deemed insufficient,
which leads mathematicians to introduce further names for such objects,
such as “anima” used by [[Dustin Clausen]] and [[Peter Scholze]],
alluding to the process of [[vertical categorification]],
in its specific incarnation as groupoidal categorification,
alias homotopification, which can be seen as “animating”
1-categorical objects by introducing higher homotopies into them.

We emphasize that these objects (except for [[types]] in [[homotopy type theory]])
come with an associated notion of [[weak equivalence]],
which is _not_ isomorphism.
For example, when using [[topological spaces]] as [models](#models)
for (homotopy) spaces, we are _not_ interested in invariants
under [[homeomorphisms]], but rather only under [[weak homotopy equivalences]].
See the [section on models](#models) for more details.

## What is a model in homotopy theory?
{#models}

Informal ideas of objects studied by [[homotopy theory]],
such as (homotopy) spaces or [[(∞,1)-categories]],
must be presented using rigorous mathematical definitions.
As of April 2020, this most likely means defining
them using some flavor of [[set theory]],
although [[homotopy type theory]] may emerge as an alternative in the future.

This process introduces artifacts that are not present
in the original informal idea and have no meaning in that context.
As an example, suppose we present a (homotopy) space
using a [[simplicial set]].
Then the [[set]] of 0-simplices or $n$-simplices for any $n\ge0$
is a piece of data specific to our chosen presentation.
Another presentation may have a set of 0-simplices of different cardinality, say.
On the other hand, if we take the set of [[connected components]]
of a [[simplicial set]], the resulting set describes
a property of the underlying (homotopy) space and not just some specific presentation.
This can be formalized by saying that the set of connected
components is invariant under [[simplicial weak equivalences]].

Thus [[simplicial sets]] up to [[simplicial weak equivalences]]
_model_ (homotopy) spaces.

One common way to encode models is to organize them
in a [[relative category]]: the underlying category encodes
the specific presentation, whereas weak equivalences
encode the relevant notion of “sameness”.

## Why do we need models in homotopy theory?

The short answer is: we do not know how to work without models.

A good example is the notion of an [[(∞,1)-category]],
which exists at the [[Platonic]] level,
and whose “shadows” (using Plato's terminology)
in the world of rigorous mathematics
have been exhibited as various models of [[(∞,1)-categories]]:
[[relative categories]], [[quasicategories]], [[Segal categories]],
[[complete Segal spaces]], [[simplicial categories]], etc.

However, the concept of [[(∞,1)-categories]] per se
resists formalization in a satisfactory way.
[[Homotopy type theory]] may succeed one day on this path,
but so far no working definition has been exhibited yet.

## What is an ∞-category or (∞,1)-category?
{#infinity}

An (∞,1)-category is a category [[enriched]] in (homotopy) spaces.

This can be formalized in many different ways.
For example, if we [model](#models) homotopy spaces
by [[simplicial sets]] with [[simplicial weak equivalences]],
then we can consider categories enriched in [[simplicial sets]],
equipped with [[Dwyer–Kan equivalences]],
which are [[enriched functors]] that induce a [[simplicial weak equivalence]]
on each mapping [[simplicial set]],
and after passing to the [[homotopy category]]
(which in this case amounts to replacing each mapping [[simplicial set]]
with its set of connected components),
we get an [[equivalence of categories]].

As one can see from this description, there are substantial
[modeling](#models) issues related to (∞,1)-categories.

Other [models](#models) for (∞,1)-categories include
[[relative categories]], [[quasicategories]], [[Segal categories]],
[[complete Segal spaces]], etc.

All these models are equivalent in a precise sense:
we can organize each of them into a [[Quillen model category]]
so that all resulting [[model categories]] are [[Quillen equivalent]].

The term “[[∞-category]]” has two different meanings:
it can either mean (∞,1)-category,
or (more recently) it can mean a [[quasicategory]] (as used in [[Lurie]]'s books,
for example).

## Are quasicategories model-independent?

No, for example, the cardinality of the set of 0-simplices of a small [[quasicategory]]
does not have any model-independent meaning,
although it is an [[isomorphism]] invariant.

Unfortunately, one often sees the adjective “model-independent”
(ab)used to mean that only constructions that
are meaningful on the level of underlying [[(∞,1)-categories]]
are used in a particular argument with [[quasicategories]].
Of course, there is nothing special about [[quasicategories]]
in this context: we often write “model-independent” arguments
of such type also using [[model categories]], for example.

## What is homotopy type theory?

See [[homotopy type theory FAQ]] for a detailed explanation.
Here we only offer a highly impressionistic description.

Consider the traditional mathematical setup for (homotopy) spaces
[modeled](#models) by [[simplicial sets]] and [[simplicial weak equivalences]]:
we start with [[first-order logic]], introduce [[Zermelo-Fraenkel axioms]],
then define [[simplicial sets]] and [[simplicial weak equivalences]].

[[Homotopy type theory]] replaces this entire stack with a flavor of [[type theory]] that aims to axiomatize
homotopy types (known in the field simply as types)
directly, without these intermediate steps.
In particular, [[first-order logic]] is subsumed
into [[type theory]].
The latter (very) roughly resembles [[ETCS]]
in how it chooses to formulate things like existence
of (co)products of sets etc., i.e., these concepts
are formulated in a categorical way rather than through
constructions like [[Kuratowski pairs]] etc.

More fundamentally, the meaning of equality sign $=$
is altered: now $A=B$ (very) roughly means the the space
of paths from the point $A$ to the point $B$ in whatever
ambient space contains the points $A$ and $B$.
Very roughly, if this space is empty, we could interpret this as $A\ne B$
and if it is nonempty, we could interpret this as $A=B$.
However, [[homotopy type theory]] preserves the whole homotopy type
of the path space and not just whether it is empty or not.
The (Platonic) meaning of the equality sign is thus fundamentally enhanced
and [[homotopy type theory]] explains how to manipulate such
enhanced equalities.

This setup allows us to talk about homotopy types directly,
without using models.
Furthermore, the analog of weak equivalences in this setting
behaves similar to [[isomorphisms]] (with a caveat that [[equality]]
is now understood in the enhanced sense).
In particular, every equivalence is invertible,
unlike (say) [[simplicial weak equivalences]], which need not be.

Much has been achieved on this path,
including a new proof of the [[Blakers-Massey theorem]] that
led to new classical consequences after being
instantiated in [[(∞,1)-toposes]].

However, one serious obstacle to adopting this approach
in mainstream [[homotopy theory]] is that there is currently (April 2020)
no working definition of an [[(∞,1)-category]],
although research is being conducted in this direction.

## What is homotopical algebra?
{#halg}

[[Homotopical Algebra]] is the title of a 1967 book by [[Daniel Quillen]] that introduced [[model categories]].

Ever since then this term has been used to describe
research in the area of [[model categories]].

It is often hard to separate homotopical algebra
from homotopy theory.
Typically, “homotopical algebra” is used
to refer to arguments that use notions from [[model categories]]
rather explicitly, as opposed to (say) [[quasicategorical]] arguments.
We do note that setting up the theory of [[quasicategories]]
relies heavily on [[homotopical algebra]] and much
of Lurie's [[Higher Topos Theory]] is devoted
to rather subtle aspects of [[homotopical algebra]].

## How are model categories related to other models of ∞-categories?

If we discard [[cofibrations]] and [[fibrations]]
from the data of a [[model category]],
we get a [[relative category]].
[[Relative categories]] are one of many equivalent [models](#models)
for [[(∞,1)-categories]], so any [[model category]]
has an underlying [[(∞,1)-category]].

Since the underlying [[(∞,1)-category]]
only depends on [[weak equivalences]] and not on [[cofibrations]] or [[fibrations]],
we deduce that two [[model categories]] with the same [[weak equivalences]],
but different [[cofibrations]] or [[fibrations]]
have the same underlying [[(∞,1)-category]].

Thus, the data of [[cofibrations]] and [[fibrations]]
merely enhances the given presentation of an [[(∞,1)-category]]
as a [[relative category]] with additional data
that helps to organize various computations,
e.g., to [derive functors](#derived).

However, the ultimate answer to any computation with [[model categories]]
that makes sense on the level of underlying [[(∞,1)-categories]]
does not depend on the choice of [[cofibrations]] and [[fibrations]],
although its specific [model](#models) certainly does.

Another important aspect of the relation between [[model categories]]
and [[(∞,1)-categories]] is that a [[model category]]
must satisfy additional (co)completeness conditions.
In the original definition by [[Quillen]],
a [[model category]] must be finitely (co)complete,
and its (co)fibrations need not be closed under [[retracts]].
In this case, the underlying [[(∞,1)-category]]
admits finite ∞-(co)limits.
In the revised definition by [[Kan]],
a [[model category]] must be (co)complete,
and its (co)fibrations must be closed under [[retracts]].
In this case, the underlying [[(∞,1)-category]]
admits small ∞-(co)limits.
Finally, Hovey's definition additionally requires factorizations
to be functorial.
This condition does not seem to alter the class of underlying [[(∞,1)-categories]].

## What is the relationship between (higher) category theory and homotopy theory?

[[homotopy theory|Homotopy theory]] serves as a foundation for much of modern (higher) [[category theory]].  For instance, the proof of equivalence of various models of [[(∞,n)-categories]] heavily relies on [homotopical algebra](#halg).  It is difficult to draw a sharp boundary between the two subjects; [[(∞,1)-categories]] could definitely be seen as being part of both, for example.

[[homotopy theory|Homotopy theory]] also somewhat implicitly permeates classical [[category theory]].  For example, the correct notion of a [[pullback]] for diagrams of [[categories]] is not the strict [[pullback]], but rather incorporates an additional isomorphism between the images of two given objects.
But this is precisely the [[homotopy pullback]] in the category of [[small categories]] equipped with the [[natural model structure]].

## What is a derived functor?
{#derived}

Just as [[relative categories]] [model](#models) [[(∞,1)-categories]],
we can expect functors between [[relative categories]]
to [model](#models) [[(∞,1)-functors]].

The easiest way to perform such [modeling](#models)
is to require functors to preserve [[weak equivalences]].
This indeed works perfectly well.
However, many functors arising in practice,
such as the tensor product of [[chain complexes]]
(with [[quasi-isomorphisms]] as [[weak equivalences]])
does not satisfy such a strong condition.

“Deriving” is a process that [models](#models) [[(∞,1)-functors]]
via functors between [[relative categories]] that need not
preserve [[weak equivalences]].

Multiple nonequivalent definitions of [[derived functors]]
exist in the literature,
and functors that can be derived in one of the definitions
need not be derivable in another.

Typically (in most definitions), deriving a [[functor]] $F\colon C\to D$ between [[relative categories]] $C$ and $D$
involves replacing $F$ with $F\circ R$,
where $R\colon C\to C$ is a [[resolution]] functor,
which is typically require to preserve [[weak equivalences]]
and be itself a [[weak equivalence]] of [[relative categories]]
(known as a [[Dwyer-Kan equivalence]] of [[relative categories]]).

A definition with rather good properties
was given recently by [[Hinich]]
and relies on converting a given functor $F\colon C\to D$
into a [[cocartesian fibration]] (or [[cartesian fibration]])
over the category $\{0\to1\}$, and
equipping the total category of this fibration
with an obvious notion of weak equivalence.
If the resulting functor of relative categories
is a (co)cartesian fibration of relative categories,
we can convert it to a functor $C\to D$ that preserves
[[weak equivalences]], which is the (left or right) [[derived functor]] of $F$.

Other (older) definitions involve [[Kan extensions]]
along [[localization]] functors to [[homotopy categories]].
These definitions do not have such nice theoretical properties
as the definition considered above.
For example, they tend to misbehave when we try to derive compositions of functors.

## What is the homotopy category of an (∞,1)-category?  What are its limitations?

The [[homotopy category]] $Ho(C)$ of an [[(∞,1)-category]] $C$
is obtained by replacing each of the hom [[∞-groupoids]] $hom(x,y)$
with its set of connected components: $hom_{Ho(C)}(x,y) := \pi_0(hom_C(x,y))$.

This informal description can be formalized in any [model](#models)
of (∞,1)-categories.
For instance, for [[relative categories]] we can formally
invert all [[weak equivalences]], the resulting [[localization]]
being the [[homotopy category]].
(We note that inverting morphisms _up to homotopy_
instead of strictly simply recovers the underlying [[(∞,1)-category]]
of a [[relative category]].)

The [[homotopy category]] is a useful tool
for extracting invariants from a given [[(∞,1)-category]].
For example, in the [[relative category]] of [[chain complexes]]
with [[quasi-isomorphisms]] we can compute
$$Ext^n(A,B)=Ho(Ch)(A,B[n]).$$

However, passing to the [[homotopy category]]
destroys a tremendous amount of information about the underlying [[(∞,1)-category]].
In particular, it is rarely possible to recover
any information about [[(∞,1)-limits]] and [[(∞,1)-colimits]]
from the [[homotopy category]], other than the case of [[products]] and [[coproducts]].
Thus, typically the passage to the [[homotopy category]]
happens near the end of an argument, where one no longer
needs categorical constructions like limits and colimits.

## What is a triangulated category?  What are its limitations?

A [[stable (∞,1)-category]] is an [[(∞,1)-category]]
that admits finite (∞,1)-(co)limits
and such that [[cartesian squares]] coincide with [[cocartesian squares]]
and there is a morphism from the [[terminal object]] to the [[initial object]].

As is clear from the definition, being a stable (∞,1)-category
is a _property_ of an (∞,1)-category.
Roughly speaking, a _triangulated category_ is the [[homotopy category]]
of a [[stable (∞,1)-category]] equipped with the additional
data of a [[homotopy cofiber]] of any morphism.

The above is not quite true.
In reality, one axiomatizes [[triangulated categories]]
as [[additive categories]] with additional data of distinguished triangles
(basically, [[homotopy cofiber]] sequences)
and suspension functor that satisfies a bunch of axioms.
A counterexample due to Muro, Schwede, and Strickland
constructs a triangulated category that does not arise
as the [[homotopy category]] of an (∞,1)-category.

[[triangulated category|Triangulated categories]] are a variation on the theme of [[homotopy categories]] and suffer from the same set of defects.
In particular, computations with [[homotopy limits]] or [[homotopy colimits]]
are extremely difficult or impossible beyond the simplest cases.

Much work was put into rectifying this defect of triangulated categories.
The resulting constructions are generically known as “enhancements”
and include notions such as [[pretriangulated dg-categories]]
and [[stable derivators]].

These definitions are rather complicated when compared
to [[stable (∞,1)-categories]], and [[derivators]] still suffer
from the same problems as [[homotopy categories]],
albeit on a higher level.

Thus, [[stable (∞,1)-categories]] due to their simplicity
and generality can be reasonably seen as an “ultimate enhancement”
of [[triangulated categories]] that does not suffer from their defects.

The most developed [models](#models) for [[stable (∞,1)-categories]]
are [[stable model categories]]
and stable [[quasicategories]].
The former are treated by [[Hovey]] in Chapter 7 of his book [[Model categories]]
and the latter are treated in Chapter 1 of [[Lurie]]'s [[Higher Algebra]].

## What is a derived category?  What are its limitations?

The [[derived (∞,1)-category]] of an [[abelian category]] $A$
is an [[(∞,1)-category]] presented by the [[relative category]]
whose underlying [[category]] is the category of [[chain complexes]]
in $A$ and [[weak equivalences]] are [[quasi-isomorphisms]].
The [[homotopy category]] of the [[derived (∞,1)-category]]
recovers the traditional [[derived category]],
which is a [[triangulated category]].

The [[derived category]] of $A$ must not be confused
with the [[homotopy category of chain complexes]] valued in $A$.
The latter category is also defined as the [[homotopy category]]
of the [[relative category]] of $A$-valued [[chain complexes]],
but with [[weak equivalences]] being
[[chain homotopy equivalences]] instead of [[quasi-isomorphisms]].

The [[derived category]] (as well as the [[homotopy category of chain complexes]]) suffers from the same limitations
as [[homotopy categories]] and [[triangulated categories]].
In particular, any theoretical constructions
that involve [[homotopy limits]] and [[homotopy colimits]]
beyond the case of [[homotopy products]] or [[homotopy coproducts]]
invariably run into severe difficulties, often insurmountable.

One way to resolve this issue is to work with
one of the models of the [[derived (∞,1)-category]] instead.
By far the most popular choice in the literature
amounts to working with the [[relative category]] described above,
often augmented by additional formalisms such as [[model categories]].

Under additional conditions on $A$,
the [[relative category]] of [[chain complexes]] with values in $A$
and [[quasi-isomorphisms]]
can be equipped with various [[model structures]],
of which the most important ones are the
[[projective model structure on chain complexes]]
and [[injective model structure on chain complexes]].
These model structures provide a convenient conceptual
framework for [[projective resolutions]] and [[injective resolutions]].

Another treatment of [[derived (∞,1)-categories]]
can be given using [[stable quasicategories]].
See Chapter 1 in [[Lurie]]'s [[Higher Algebra]].

## References

* [Do we still need model categories?](https://mathoverflow.net/questions/78400/do-we-still-need-model-categories)
* [Why do we need model categories?](https://mathoverflow.net/questions/287091/why-do-we-need-model-categories)
* [Is the ∞-category of spectra “convenient”?](https://mathoverflow.net/questions/322808/is-the-infty-category-of-spectra-convenient)
* [Do we still need models of spectra other than the ∞-category Sp?](https://mathoverflow.net/questions/322832/do-we-still-need-models-of-spectra-other-than-the-infty-category-mathrmsp)
