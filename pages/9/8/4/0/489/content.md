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
=--

...the $0$-category of 
$(-1)$-groupoids to be a $(0,1)$-category, or $1$-[[poset]]; this is simply a [[poset]], and indeed truth values do form a poset, the poset of [[subobject|subobjects]] of the [[subobject classifier]].
Classically this is
($\bot \leq \top$), while in a general topos it is $Subobjects(\Omega)$.

+--{.query}
  _[[Urs Schreiber|Urs]]:_ I added into the above paragraphs the remarks about $\Omega$ and subobjects of $\Omega$. Hope I got it right. In fact, I am not sure: how do we make the partially ordered _set_ of subobjects of $\Omega$ into something internal to the topos?
=--

If we equip the category of $(-1)$-groupoids with the monoidal structure of [[conjunction]] (the logical AND operation), then a [[enriched category|groupoid enriched]] over this is a [[set]], which fits the patterns of the periodic table.

+--{.query}
 _[[Urs Schreiber|Urs]]:_ How do we make this last statement internal to an arbitrary topos?
=--

See [[(-1)-category]] for more on this sort of 'negative thinking'.