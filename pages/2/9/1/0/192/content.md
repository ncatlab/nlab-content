# The category of sets
* table of contents
{: toc}

## Definition

__$Set$__ is the (or a) [[category]] with [[sets]] as [[objects]] and [[functions]] between sets as [[morphisms]].


## Properties

This category has many marvelous properties, which make it a common choice for serving as a '[[foundations|foundation]]' of mathematics.  For instance:

* It is a [[well-pointed category|well-pointed]] [[topos]], 

  So in particular it is [[locally cartesian closed category|locally cartesian closed]].

* It is [[locally small category|locally small]].

* It is [[complete category|complete]] and [[cocomplete category|cocomplete]], and therefore $\infty$-[[extensive category|extensive]] (as is any cocomplete topos).

At least assuming [[classical logic]], these properties suffice to characterize $Set$ uniquely up to equivalence among all categories; see [[cocomplete well-pointed topos]].  Note, however, that the definitions of "locally small" and "(co)complete" presuppose a notion of _small_ and therefore a knowledge of what a _set_ (as opposed to a [[proper class]]) is.

As a topos, $Set$ is also characterized by the fact that

* $Set$ is the [[terminal object]] in the [[category]] of [[Grothendieck topos]]es and [[geometric morphism]]s. The terminal morphism $\Gamma\colon E \to Set$ from any other topos $E$ is the [[global section]]s functor.

It is usually assumed that $Set$ satisfies the [[axiom of choice]] and has a [[natural numbers object]].  In Lawvere's theory [[ETCS]], which can serve as a foundation for much of mathematics, $Set$ is asserted to be a well-pointed topos that satisfies the axiom of choice and has a natural numbers object.  It follows that it is automatically "locally small" and "complete and cocomplete" relative to the notion of "smallness" defined in terms of itself (actually, this is true for any topos).

Conversely, $\Set$ in [[constructive mathematics]] cannot satisfy the axiom of choice (since this implies [[excluded middle]]), although constructivists might accept [[COSHEP]] (that $Set$ has [[projective object|enough projectives]]).  In [[predicative mathematics]], $\Set$ is not even a topos, although most predicativists would still agree that it is a [[pretopos]], and predicativists of the constructive school would even agree that it is a [[locally cartesian closed category|locally cartesian closed]] pretopos.


## Remarks 

* Above we considered $Set$ to be the category of _all_ sets, so that in particular $Set$ itself is a [[large category]].  Authors who assume a [[Grothendieck universe]] as part of their [[foundations]] often define $Set$ to be the category of *small* sets (those contained in the universe).  One often then writes $SET$ for the category of *large* sets, which is the [[universe enlargement]] of $Set$.


category: category

[[!redirects Set]]
[[!redirects SET]]
[[!redirects category of sets]]
[[!redirects the category of sets]]
