This page is to provide non-technical or maybe semi-technical discussion of the nature and role of [[homotopy theory]].
For more technical details and further pointers see at [[homotopy theory]].


#Contents#
* table of contents
{:toc}

## Is homotopy theory a part of algebraic topology?
{#intro}

In one of the first textbooks on homotopy theory,
_An introduction to homotopy theory_ by [[Peter J. Hilton]] (1953),
one reads:

> Since the introduction of -[[homotopy groups]] by [[Hurewicz]] in 1935, homotopy theory has been occupying an increasingly prominent place in the field of [[algebraic topology]]. Important new advances are continually being made in the subject by various workers; and the recent developments emanating from
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

## What is homotopy theory?

We list some [[mathematical objects]] that are undoubtedly studied by [[homotopy theory]]:

* The first object is known under various names: [[∞-groupoid]], (homotopy) space, [[homotopy type|(homotopy) type]], more recent (and so far exotic) names include “anima”. See the [section on “spaces”](#spaces) for an explanation of why so many different names are used for (essentially) the same concept.
These objects can be modeled by [[simplicial sets]] up to [[simplicial weak equivalence]], or [[topological spaces]] up to [[weak homotopy equivalence]],
or many other models.
See the [section on models](#models) for more details about models.

* [[Spectra]] or [[stable homotopy types]].
Specific [models](#models) include [[sequential spectra]] or [[symmetric spectra]] (valued in [[simplicial sets]] or [[topological spaces]]), [[orthogonal spectra]], [[reduced excisive functors]], etc.

* [[∞-categories]], also known as [[(∞,1)-categories]], [[homotopy theories]], and other names.
Specific [models](#models) include [[relative categories]], [[quasicategories]], [[simplicial categories]], [[Segal categories]], [[complete Segal spaces]], etc.
See the [section on ∞-categories](#infinity) for more information.

* [[(∞,n)-categories]], which can be [modeled](#models) by [[globular n-fold complete Segal spaces]], Rezk's [[Theta-n spaces]], etc.

## What is algebraic topology?

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

## What is homotopy type theory?

## What is an ∞-category or (∞,1)-category?
{#infinity}

## How are model categories related to other models of ∞-categories?

## What is homotopical algebra?

## What is the relationship between category theory and homotopy theory?

## What is a derived functor?

## What is the homotopy category of an ∞-category?  What are its limitations?

## What is a triangulated category?  What are its limitations?