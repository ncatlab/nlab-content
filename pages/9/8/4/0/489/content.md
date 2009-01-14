A __(-1)-groupoid__ is a [[truth value]]. Compare the concept of [[0-groupoid]] (a [[set]]) and [[(-2)-groupoid]] (which is trivial). The point of (-1)-groupoids is that they complete some patterns in the [[periodic table]] of $n$-categories. (They also shed light on the theory of [[homotopy group]]s and [[n-stuff]].)

For example, there should be a $0$-[[0-category|category]] of $(-1)$-groupoids; a $0$-category is also a set, and this set is the set of [[truth value|truth values]]: classically (in the [[topos]] [[Set]])
$$
  (-1)Gpd := \{\bot, \top\}
$$
and in a more general topos 
$$
  (-1)Gpd := \Omega
  \,,
$$
where $\Omega$ is the [[subobject classifier]].

Actually, we should expect... 

+--{.query}
  _[[Urs Schreiber|Urs]]:_ Can't this be motivated more systematically?

  _[[Mike Shulman|Mike]]:_ There's a funny weirdness that happens at the bottom with the relationship between sets and posets.  I don't completely understand it, nor do I know any reason why "we should expect" the $0$-category of $(-1)$-groupoids to be a $(0,1)$-category, since the 1-category of 0-groupoids (sets) is not a $(1,2)$-category (except trivially).  On the other hand, the 1-category of $(0,1)$-categories is a $(1,2)$-category, so maybe the point is that every $(-1)$-groupoid is actually a $(-1,0)$-category?

I don't really understand why we have separate pages for $(-1)$-groupoids and $(-1)$-categories; has anyone ever come up with a way in which they are different?

_Toby_: There are separate pages [[truth value]], [[(-1)-groupoid]], [[(-1)-category]] and (eventually) [[0-poset]]. Partly it\'s that [[(-1)-category]] was written first, although it\'s the worst name. But I think that it will be good, given the nature of this wiki, to have pages organised more by term than subject (I will write a bit about this on the Caf&#233;). But this means that the pages will have different purposes.

As [[truth value]] is the most mundane and ordinary name for the concept, that page will have the most content. There we should discuss what a truth value is in a topos or other sort of category, or what it is to a constructivist or other sort of alternative mathematician; there we should discuss how truth values form a poset, and what structures and properties this poset has; there we should talk about what categories and groupoids enriched over this poset (with either of the two obvious monoidal structures) are.

At [[(-1)-category]], which exists only because we like $n$-categories so much and so wonder what an $(-1)$-category is, we explain why the concept is a little fishy but the best way to define it is as a truth value. And there we show how this fits the patterns of the periodic table to the extent that it does, and also poitn out those cases where it doesn\'t.

At [[(-1)-groupoid]], which again exists because that\'s our special thing, we explain why a $(-1)$-groupoid is a truth value, and how that fits the patterns of the periodic table.

At [[0-poset]], we\'ll do exactly the same thing, only thinking about $n$-posets rather than $n$-groupoids.

(If this were Wikipedia, we would not organise things this way. I\'ll discuss that at the Caf&#233;.)

In particular, I think that general facts about internalising the concept to categories other than $\Set$ work best at [[truth value]], while they would really fit in here only if we wanted to explain how that reproduces (or, conceivably, turns out to be different from) a general method for internalising the concept of $n$-groupoid. (Probably we will eventually want to talk about that, but as far as I know there\'s nothing to say about it now.)

By the way, here is the answer to Mike\'s question about what "we should expect": the $\infty$-category of $(n,r)$-categories is an $(n+1,r+1)$-category (which I should discuss on [[(n,r)-category]] but have not); accordinly, the $\infty$-category of $n$-groupoids is an $(n,1)$-category. In particular, the $\infty$-category of $(-1)$-groupoids is a $(0,1)$-category.
=--

...the $0$-category of $(-1)$-groupoids to be a $(0,1)$-category, or $1$-[[poset]]; this is simply a [[poset]], and indeed truth values do always form a poset.  Classically this is ($\bot \leq \top$), while in a general topos is it the [[subobject classifier]] $\Omega$ equipped with its canonical internal partial order.  (This is not to be confused with the poset of [[subobject|subobjects]] of $\Omega$, which of course is $\Omega^\Omega$ internally.)

If we equip the category of $(-1)$-groupoids with the monoidal structure of [[conjunction]] (the logical AND operation), then a [[enriched category|groupoid enriched]] over this is an [[equivalence relation]].  (This is true both classically and internally in a topos.)  An enriched functor is a function that respects the equivalences, and an enriched natural transformation relates two such functions if they are pointwise equivalent.  Therefore, classically every equivalence relation is equivalent (as a groupoid enriched over truth values) to its quotient, so the collection of such enriched categories is equivalent to the category of sets; this fits the patterns of the periodic table.  Internally in a topos, the same argument works as long as we use enriched [[anafunctor]]s instead of functors.

See [[(-1)-category]] for more on this sort of 'negative thinking'.