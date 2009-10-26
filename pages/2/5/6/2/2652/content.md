This page is currently about ways to "complete" a [[category]].  (Possibly it should be renamed if we want a page about more general kinds of completion.)  The general idea is that given a category $C$, we construct from it a larger category, containing $C$ as a [[subcategory]], which moreover has certain properties that $C$ might have lacked.  This larger category is then called the _completion_ or _free completion_ of $C$ with respect to these properties.

Outside of category theory, "completion" is usually used mostly for *idempotent* operations.  That is, the completion of a thing with respect to some property is itself *complete* with respect to that property, and the completion process doesn't change an object that is already complete.  From the perspective of [[stuff, structure, property]] this makes sense because we complete with respect to a *property*.  Namely, according to the yoga of SSP, given some ambient category $K$, the subcategory of objects having a property $P$ should be a *full* subcategory, whose inclusion [[functor]] forgets that property.  A "completion" operation is then usually a left (or, occasionally, right) [[adjoint]] to that inclusion functor, making the category of objects with property $P$ [[reflective subcategory|reflective]] (or coreflective).  Note that a [[full and faithful functor]] with a left adjoint is always [[monadic functor|monadic]] and the monad is [[idempotent monad|idempotent]].

By contrast, when we add *structure* to objects, i.e. we consider an adjoint to a forgetful functor which is faithful but not necessarily full, we usually do not use the word "completion" but rather the word "free".  For example, the category of complete [[metric spaces]] is a full reflective subcategory of the category of metric spaces, and the reflection is called "completion."  By contrast, the forgetful functor from the category of groups to the category of sets has a left adjoint, but we call that left adjoint the "free group on a set" rather than the "completion of a set into a group."

(to be continued...)

## Idempotent completions

* [[Cauchy complete category|Cauchy completion]] of an enriched category: addition of all absolute limits.
* [[exact completion]]
* [[pretopos]] completion

## Lax-idempotent completions

* [[free completion]] 
* [[free cocompletion]]
* Ind-completion (should we say 'inductive completion'?): the "free cocompletion under filtered colimits" requiring all [[ind-object|ind-objects]].
* [[ideal completion]] of a category: the free cocompletion under filtered colimits of monomorphisms.
* 

+-- {: .query}
David: Are there (2)-functors forgetting various degrees of completeness with adjoints?

What happens in the $V$-enriched setting?
=--

* [[profinite completion of a group|profinite completion]] of a discrete group

+--{: .query}
Is this a case of profinite completion of a category, i.e., adding cofiltered limits?

[[Mike Shulman]]: No, I don't think so.  Are you thinking of viewing a group as a one-object groupoid?  The profinite completion of a group is not an ordinary group but a [[profinite group]], which is thus not a category, at least not in the same sense.
=--

