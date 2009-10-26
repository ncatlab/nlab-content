The general idea of completion is that given an object of some sort $C$, we construct from it a larger object, containing $C$ as a subobject, which moreover has certain properties that $C$ might have lacked.  This larger object is then called the _completion_ of $C$ with respect to these properties.

* table of contents
{:toc}

# Completion and idempotence

Outside of category theory (see below), "completion" is usually used mostly for *idempotent* operations.  That is, the completion of a thing with respect to some property is itself *complete* with respect to that property, and the completion process doesn't change an object that is already complete.  From the perspective of [[stuff, structure, property]] this makes sense because we complete with respect to a *property*.  Namely, according to the yoga of SSP, given some ambient category $K$, the subcategory of objects having a property $P$ should be a *full* subcategory, whose inclusion [[functor]] forgets that property.  A "completion" operation is then usually a left (or, occasionally, right) [[adjoint functor|adjoint]] to that inclusion functor, making the category of objects with property $P$ [[reflective subcategory|reflective]] (or coreflective).  Note that a [[full and faithful functor]] with a left adjoint is always [[monadic functor|monadic]] and the monad is [[idempotent monad|idempotent]].

By contrast, when we add *structure* to objects, i.e. we consider an adjoint to a forgetful functor which is faithful but not necessarily full, we usually do not use the word "completion" but rather the word "free".  For example, the category of complete [[metric spaces]] is a full reflective subcategory of the category of metric spaces, and the reflection is called "completion."  By contrast, the forgetful functor from the category of groups to the category of sets has a left adjoint, but we call that left adjoint the "free group on a set" rather than the "completion of a set into a group."

Additionally, we tend not to use the term 'completion' unless the [[reflector]] is a [[monomorphism]] (perhaps even a [[regular monomorphism|regular]] one?).  For example, the left adjoint of the forgetful functor from groups to [[abelian groups]] is called 'abelianisation' and may even be called 'free abelian group on a group' but is not normally called 'abelian completion' or anything like that.

# List of completions

* Cauchy completion of a [[metric space]], or more generally a [[uniform space]]
* [[Dedekind completion]] of a [[linear order]] (or sometimes a more general [[preorder]])
* [[profinite completion of a group|profinite completion]] of a discrete group 
  +--{: .query}
  Is this a case of profinite completion of a category, i.e., adding cofiltered limits?

  [[Mike Shulman]]: No, I don't think so.  Are you thinking of viewing a group as a one-object groupoid?  The profinite completion of a group is not an ordinary group but a [[profinite group]], which is thus not a category, at least not in the same sense.
  =--
* Field of fractions of an [[integral domain]]

# Free completion and lax-idempotence

The general contrast between "completion" for adding a property and "free" for adding structure applies to operations on [[category|categories]] as well.  For instance, since [[split idempotents]] are preserved by any functor, the 2-category of categories with split idempotents is a full sub-2-category of [[Cat]].  Therefore, it makes perfect sense to call the left adjoint of its inclusion a "completion," in this case the (Set-enriched) [[Cauchy completion]] or [[Karoubi envelope]].  By contrast, the forgetful functor from the 2-category of [[monoidal categories]] to $Cat$ forgets structure, rather than properties, so its left adjoint should be called a "free" construction rather than a "completion."

However, in this case there is an intermediate notion between properties and structure, namely [[property-like structure]].  Intuitively, property-like structure is "structure which, when it exists, is essentially unique" or "a property which is not necessarily preserved by morphisms."  The canonical example is the existence of [[limits]] and [[colimits]] in a category: when they exist they are unique up to unique canonical isomorphism (so that "having limits" is intuitively a property of a category), but not every functor preserves limits, so the forgetful functor from  categories-with-limits to categories is not full.  (Left) adjoints to functors which forget property-like structure are usually called *free completions*.  The monads they induce are not idempotent, but they are often [[lax-idempotent monad|lax-idempotent]] or colax-idempotent.  (For example, when we freely add limits to a category that already had limits, the old limits are no longer limits and the new ones take their place.)

Property-like structure is most common in category theory, but it does occur elsewhere as well.  For instance, a [[monoid]] is a [[semigroup]] with property-like structure: a semigroup has at most one identity element, but that identity element is not necessarily preserved by semigroup homomorphisms.  Thus the adjoining of a new formal identity element to a semigroup (which is not an idempotent operation) might be called its "free completion into a monoid".  Notice that if the original semigroup is already a monoid, then its free completion into a monoid will be a *different* monoid (with a new identity); this shows the distinction between free completion and mere completion.

# List of completions in category theory

## Idempotent completions

The following completions add a *property* in the strictest sense, and as such are idempotent.

* [[Cauchy complete category|Cauchy completion]] of an enriched category: addition of all absolute limits.
* [[exact completion]] of a [[regular category]] (the "ex/reg" completion)
* [[extensive category|extensive]] completion
* [[pretopos]] completion of a [[coherent category]]

## Non-idempotent completions

These completions add a property-like structure, are often lax-idempotent or colax-idempotent.

* [[free cocompletion]]: the [[presheaf category]] of a [[small category]] is its free cocompletion under all small colimits.
* [[free completion]]: the dual (the opposite of the free cocompletion of the opposite).
* Ind-completion: the "free cocompletion under filtered colimits," consisting of all [[ind-object|ind-objects]].
* [[ideal completion]]: the free cocompletion under filtered colimits of monomorphisms.

Note that these completions take small categories to large categories.  Free completions and cocompletions of large categories can be obtained using categories of [[accessible functor|accessible presheaves]].  However, if we only want to add limits and/or colimits for a given *set* of diagram shapes, the free completion process will preserve smallness.  For example we have:

* the free completion under finite products or coproducts
* the free completions under finite limits or colimits

All these sorts of completions work just as well in an [[enriched category|enriched]] setting, as long as the enriching category $V$ is nice enough ([[locally presentable category|locally presentable]] is certainly enough).

Some other non-idempotent completions:

* The [[regular category|reg/lex]] and [[exact category|ex/lex]] completions of a category with finite limits.
