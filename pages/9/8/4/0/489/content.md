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
=--

...the $0$-category of $(-1)$-groupoids to be a $(0,1)$-category, or $1$-[[poset]]; this is simply a [[poset]], and indeed truth values do always form a poset.  Classically this is ($\bot \leq \top$), while in a general topos it the [[subobject classifier]] $\Omega$ equipped with its canonical internal partial order.  (This is not to be confused with the poset of [[subobject|subobjects]] of $\Omega$, which of course is $\Omega^\Omega$ internally.)

If we equip the category of $(-1)$-groupoids with the monoidal structure of [[conjunction]] (the logical AND operation), then a [[enriched category|groupoid enriched]] over this is an [[equivalence relation]].  (This is true both classically and internally in a topos.)  An enriched functor is a function that respects the equivalences, and an enriched natural transformation relates two such functions if they are pointwise equivalent.  Therefore, classically every equivalence relation is equivalent (as a groupoid enriched over truth values) to its quotient, so the collection of such enriched categories is equivalent to the category of sets; this fits the patterns of the periodic table.  Internally in a topos, the same argument works as long as we use enriched [[anafunctors]] instead of functors.

See [[(-1)-category]] for more on this sort of 'negative thinking'.