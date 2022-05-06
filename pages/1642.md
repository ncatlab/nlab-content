
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A semigroup is like a [[monoid]] where there might not be an [[identity element]].  

The term "semigroup" is standard, but _semi-monoid_ would be more systematic.

## Definition

A __semigroup__ is, equivalently,

*  a [[set]] equipped with an [[associativity|associative]] binary operation.  

*  an associative [[magma]];

*  the [[hom-set]] of a [[semicategory]] with a single object.


## Properties

Some semigroups happen to be [[monoid]]s; even then, a semigroup [[homomorphism]] might not be a monoid homomorphism (because it might not preserve the identity element).  Nevertheless, semigroup [[isomorphisms]] must be monoid isomorphisms.  Thus, the identity element of a monoid forms a [[property-like structure]] on the underlying semigroup.

This should be contrasted with the phenomenon that a semigroup homomorphism between two semigroups that happens to be [[group]]s does, in fact, happen to be a group homomorphism, since in this special case one can show a semigroup homomorphism must preserve the identity and inverses.

As a monoid is a [[category]] with one object, so a semigroup is a [[semicategory]] with one object.

Any [[small category]] $\mathcal{C}$ can be thought of as a semigroup by defining $S = \text{Mor}(\mathcal{C})\cup \{0\}$ and taking $f*g = f \circ g$ for any composable morphisms $f, g$, and $f*g = 0$ otherwise. Then the semigroup $(S, *)$ fully describes $\mathcal{C}$.

Generalizing this, any [[category]] can be thought of as a semigroup which isn't necessarily defined on a set.


## Attitudes toward semigroups 

Some mathematicians consider semigroups to be a case of [[centipede mathematics]].  [[category theory|Category theorists]] sometimes look with scorn on semigroups, because unlike a monoid, a semigroup is not an example of a [[category]].    

However, a semigroup can be promoted to a monoid by adjoining a new element and decreeing it to be the identity.  This gives a [[fully faithful functor]] from the category of semigroups to the category of monoids.  So, a semigroup can actually be seen as a monoid with extra property.

+-- {: .un_example}
###### Exercise  

Describe this property. 
=--

On the other hand, analysts run across semigroups often in the wild, and don\'t always want to add formal identities just to turn them into monoids.

Another variant with strong links with category theory is that of [[inverse semigroups]], which [[Charles Ehresmann]] showed were closely related to [[ordered groupoid]]s. Inverse semigroups naturally occur when considering partial symmetries of an object.

+-- {: .query}
_AnonymousCoward_: In _Categories of Symmetries and Infinite-Dimensional Groups_ by Yu. A. Neretin (London Mathematical Society Monographs, New Series 16, Oxford Science Publications 1996), the author points out that if we consider an infinite-dimensional group $G$ can be realized in the following way: there is some category $C$ with an object $X$ such that 
$$
Aut(X)=G.
$$
Then we have this special semigroup 
$$
\Gamma=End(X)
$$
which is called the **Mantle** of $G$. Neretin insists it is a semigroup.

I am at a loss as to why this is a semigroup, and not a monoid...

[[David Roberts]]: Well, we can realise $G = Aut_{\mathbf{B}G}(*)$, where $*$ is the single object of the one-object groupoid associated to $G$. Then $End(*) = Aut(*)$ in this category, so this 'Mantle' is nowhere near being uniquely defined. Is Neretin using the same definition of semigroup as here (it's the obvious first question - a bit like 'is your computer plugged in and turned on at the wall?'). Unless I've got the wrong end of the stick, and this category $C$ is defined up to equivalence from $G$. And maybe $C$ isn't a category, but only a [[semicategory]]? 

Edit: Having a look, I find his book: Semigroups in algebra, geometry, and analysis, by Karl Heinrich Hofmann, Jimmie D. Lawson, &#278;rnest Borisovich Vinberg. They talk about Ol'shanski&#301; semigroups associated to groups - this might be a place to get started. From the examples discussed, it seems like some of the semigroups they consider are monoids, but that was only after I flicked quickly through the book online.

_Toby_:  When Neretin insists that the mantle is a semigroup, does he also insist that it\'s not a monoid, or is he just silent about that?  After all, it *is* a semigroup.

We category theorists are strongly attracted to monoids, since they come from categories and semigroups don\'t.  But others consider monoids to be just a special kind of semigroup; as long as it\'s not a group, they\'re not going to bother worrying about whether a semigroup is a monoid or not.

I agree with David that the mantle doesn\'t seem to be well defined; a group should have several mantles (the smallest of which is itself).  But if he\'s talking about a particular way of constructing certain groups, then this way may well come about by first constructing a monoid (the mantle) and then taking the mantle\'s group of invertible elements.

_AnonymousCoward_: The notion of a semigroup is (as best as I can tell from closely reading the first chapters) left undefined. I assumed that the endomorphism monoid here is also a semigroup, so there is really nothing lost here (well...partially true; I think viewing the Mantle as a semigroup **does** play a role when considering morphisms!). 

After looking a bit more into Neretin's writings (e.g. "Infinite-dimensional groups, their mantles, trains, and representations" in Kirillov's book _Topics in Representation Theory_) it does seem clear that the mantle of an infinite-dimensional group is not well-defined (there are apparently two different ways to consider it that produce not necessarily equal mantles --- one is by considering the group $G$ as the automorphism of an object $H$ in some category and thereby obtaining the mantle as the endomorphism monoid of this object; the other is to consider the closure of sequences of $G$ under a weak-operator norm, or something to that effect).

I was just worried that I was forgetting some special situation when the endomorphisms form a semigroup instead of a monoid.

Also, thank you both Toby and David for your quick and informative replies, I really appreciate it :) 
=--


## Internalization 

We can [[internalization|internalize]] the concept of semigroup in any [[monoidal category]] (or even [[multicategory]]) $V$ to get a __semigroup object__ in $V$.

## Related topics

*  There is a strong connection between semigroups and finite automata; see e.g. [[Krohn-Rhodes theory]].

* [[inverse semigroups]]

* [[cancellative semigroup]]

* [[weakly reductive semigroup]]

* [[semiring]]

* [[semi-category]], [[semi-simplicial set]], [[semi-Segal space]]


## References

Semicategories and semigroups are mentioned for instance in section 2 in

* W. Dale Garraway, _Sheaves for an involutive quantaloid_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 46 no. 4 (2005), p. 243-274  ([numdam](http://www.numdam.org/item?id=CTGDC_2005__46_4_243_0))


[[!redirects semigroup]]
[[!redirects semigroups]]
[[!redirects semigroup object]]
[[!redirects semigroup objects]]

[[!redirects semi-group]]
[[!redirects semi-groups]]
[[!redirects semi-monoid]]
[[!redirects semi-monoids]]
[[!redirects semimonoid]]
[[!redirects semimonoids]]

