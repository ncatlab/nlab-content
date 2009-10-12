<div class="rightHandSide toc">
[[!include mathematicscontents]]
</div>


#Category theory and foundations#

There are two big questions about category theory and the logical foundations of mathematics:

 1. What foundations are adequate to formulate category theory?
 2. How can category theory provide a foundation for mathematics?

These questions also apply to [[higher category theory]], which also involves the relation between them. (Two-categories as a foundation for categories, for example.)

+--{.query}

_[[Urs Schreiber|Urs]] asks_: Concerning the last paranthetical remark: I suppose in this manner one could imagine $(n+1)$-categories as a foundation for $n$-categories? What happens when we let $n \to \infty$?

_[[Toby Bartels|Toby]] answers_: That goes in the last, as yet unwritten, section.

=--

For a philosophical treatment of category theoretic foundations see [[foundations and philosophy]]. 

# Mathematical foundations of category theory

The problem with mathematical foundations of category theory is that in category theory we frequently speak of [[large category|large categories]], which it is tricky to deal with rigorously in the usual sort of [[set theory|set theories]].

One common view seems to be to found category theory on a theory of sets and classes; see [the English Wikipedia\'s definition](https://secure.wikimedia.org/wikipedia/en/wiki/Category_%28mathematics%29#Definition), for example. But the standard reference, Saunders Mac Lane\'s _Categories for the Working Mathematician_, assumes the existence of a universe (an inaccessible cardinal) instead. Both of these approaches rely on a distinction between *small* and *large* categories. There is a category of all [[small category|small categories]], but this category is not itself small; there is no category of all categories.

Alexander Grothendieck needed more; he used what we now call [[Grothendieck universe]]s. He assumed that every set is contained within a universe; that is, for every cardinal number $\kappa$, there is a cardinal inaccessible from $\kappa$. (This is still a rather moderate axiom, compared to some of the large-cardinal axioms studied by set theorists.) Now one has a relative notion of small and large; the category of all $U$-small categories (where $U$ is some universe) is $U$-large but must be $U'$-small for some other universe $U'$, and there exists a category (which is both $U$-large and $U'$-large) of all $U'$-small categories.

If one does not accept the [[axiom of choice]], then there are additional complications in general category theory. In particular, one must distinguish between a universal *property* (for example, having all [[product]]s) and having a universal *structure* realising that property (in the example, a functor taking each pair $(x,y)$ of objects to a specific product cone $x \leftarrow x \times y \rightarrow y$). This difficulty was overcome by Michael Makkai using [[anafunctor]]s, but these have not been widely adopted, even by constructivists.

For a summary of the mathematical foundations of category theory, see Mike Shulman, _Set theory for category theory_, [arXiv:0810.1279](http://arxiv.org/abs/0810.1279).

+--{.query}

_[[Urs Schreiber|Urs]] asks_: More recently it seems that the concept of _accessible categories_ has found some 
supporters as a tool for conveniently dealing with size issues generally in (higher) category theory. Jacob Lurie discusses this from [p. 341](http://www-math.mit.edu/~lurie/papers/highertopoi.pdf#page=342) on in his [Higher Topos Theory](http://arxiv.org/abs/math.CT/0608040), where he says

<blockquote>

the theory of accessible 1-categories is a tool which allows us to
manipulate large 1-categories as if they were small, without fear of
encountering any set-theoretic paradoxes. This theory is quite useful
because the condition of accessibility is very robust

</blockquote>

I have only a vague understanding of accessible categories at the moment. It would be nice to have an entry [[accessible category]] explaining it. My main problem here is probably that I have no good idea of notions like "regular cardinal".

_[[Toby Bartels|Toby]] answers_: I understand all these large cardinals much better in terms of their categories of small sets. In particular, a cardinal number $\kappa$ is _regular_ if the category of $\kappa$-small sets is $\kappa$-cocomplete. That is, any $\kappa$-small coproduct (the other $\kappa$-small colimts follow) of $\kappa$-small sets is a $\kappa$-small set. Here a set is _$\kappa$-small_ if its cardinality is less than $\kappa$, but you can see that the real point is not the cardinal number $\kappa$ but rather the category of (relatively) small sets. So a subcategory $C$ of $\Set$ (say a full subcategory, and closed under taking subobjects) is _regular_ (in the cardinal sense) if $C$ has all colimits indexed by categories internal to itself. This generalises to indexed category theory, although I have only a vague understanding of that.

=--

##The concept of _identity_

One way to think of category theory is as a framework in which the idea is formalized that every kind of [[equality]] is really secretly a choice of [[isomorphism]] or [[equivalence]]. In some sense the notion of identity is potentially [[evil]], in a technical sense.

 [[Michael Makkai]] works on a language, [[FOLDS]] ('first-order logic with dependent sorts'), which is designed to make it impossible to formulate any [[evil]] statements.  To learn more, see his paper _[First Order Logic with Dependent Sorts, with Applications to Category Theory](http://www.math.mcgill.ca/makkai/)_.

# Categorial foundations of mathematics

Bill Lawvere proposed to found mathematics on a first-order axiomatisation of [[Cat|the category of categories]]. This has not been very successful, ...

+--{.query}

_[[Urs Schreiber|Urs]] asks_: Can you say what the problem is?

_[[Toby Bartels|Toby]] answers_: I\'d say that it proved to be overkill; ETCS is simpler and no less conceptual. In ETCC (or whatever you call it), you can neatly define a group (for example) as a category with certain properties rather than as a set with certain structure. But then you still have to define a topological space (for example) as a set with certain structure (where a set is defined to be a discrete category, of course). I think that Lawvere himself still wants an ETCC, but everybody else seems to have decided to stick with ETCS.

_Roger Witte_ asks:_ Surely in ETCC, you define complete Heyting algebras as particular kinds of category and then work with Frames and Locales (ie follow Paul Taylor's leaf and apply Stone Duality).  You can then get to Top by examining relationships between Frm and Set? Pullback the forgetful functor from loc to set op along the contravariant powerset fuctor?

=--

... but his other proposal, a first-order axiomatisation of [[Set|the category of sets]], works well. These and related approaches to foundations may be called _structural_ or _categorial_ (or _categorical_, which is more common but clashes with another sense of 'categorical' in logic).

+--{.query}

_[[Urs Schreiber|Urs]] says_: I like _categorial_. If we think we can improve on existing terminology we should feel free to introduce it here.

_[[Toby Bartels|Toby]] responds_: Once you use 'categorial' when discussing logic, it\'s hard to justify using 'categorical' in other contexts. I suppose that I could go through the whole wiki and change 'categorical' to 'categorial' ....

_[[Urs Schreiber|Urs]] says_: with respect to optimal terminology I think that one problem is that the very term "category" is not optimal.

_[[Toby Bartels|Toby]] responds_: I think that it\'s too late to play Bourbaki with that. Or do you want to say 'semigroupoid'? (which occasionally appears in groupoid literature but most properly would not have identity morphisms). I got a lot of stares over dinner at Groupoidfest when I said that that might be a better term after all (for categories as algebraic objects).

_[[Mike Shulman|Mike]] comments_: I think it is probably too late to play Bourbaki with "categorical" as well; too many people are using it who don't care about logic.  However, there is another option here: I like to call ETCS-like theories _structural set theories_ rather than "categori(c)al foundations".  As Lawvere and others have pointed out, ETCS is still a theory of sets; it merely differs from traditional set theories such as ZF in its lack of a global membership predicate and in what notions it takes as basic.

_Toby_: Can we at least say 'category-theoretic' instead of 'categorical'? It can be very disconcerting to read, for example on [[tensor product]], 'More categorically, this can be constructed as the coequalizer of the two maps [...]'. (If anything, this is *less* categorical than the explicit previous construction by modding out relations, since the previous can be formalised in a membership-based set theory in which it is defined up to set-theoretic identity, while the other, however formalised, is defined only up to unique isomorphism. Of course, that should not *really* be considered less categorical, but it\'s still hardly more categorical.) To be unambiguous, this should be 'More categorially, [...]' or, if you don\'t like that word, 'More category-theoretically [...]'. (Or do you think that 'More structurally [...]' will work here?)

[[Mike Shulman|Mike]]: At some point, I think one just has to accept that some words have more than one meaning, and learn to deal with it.  I appreciate that it can be disconcerting to a logician or philosopher to read "categorical" used to mean "category-theoretic," but it is of course just as confusing to a category-theorist when it is used to mean "having a unique model."  Undoubtedly the logicians were there first, but the time to have that argument was back when Eilenberg and Mac Lane chose the word "category."  And although I am of course biased, I think that "category-theoretic" is a more important notion in mathematics than "having a unique model."  And "categorial" looks to me like a misspelling.

_Toby_:  Erm, no, while the term 'category' may have some problems that one might have objected to in 1945, that was not the time to anticipate that people might later apply it to logic and then use the adjective 'categorical'.  I understand why you don\'t like 'categorial', so what\'s wrong with 'category-theoretic' or 'structural'? (when discussing logic, that is).

_Mike_: I didn't mean to say that anyone should have been able to anticipate the conflict of "categorical" related to categories with its use in logic back in 1945.  I just meant that by now, when "category" has a universally established meaning, I don't think it's reasonable to object to the use of "categorical" to mean "related to categories."  I like "structural" when it applies, but to me it has a different meaning than "categorical"---this is the point I'm trying to make with [[SEAR]], that structural set theory doesn't depend on category theory.  Finally, "category-theoretically" has almost twice as many syllables and letters as "categorically," and sounds awkward.

I am sort of starting to soften towards "categorial," at least when talking to logicians or about logic.  There's enough antagonism towards category theory in the logic/foundations community without adding to the perception that we're stealing established terminology.  But I'm not yet convinced that it's worth going on a crusade to eliminate "categorical" referring to category theory from everyday mathematical speech.

_Toby_:  I don\'t feel on a crusade, but I avoid using 'categorical'.  I often used 'categorial', or I\'ll use 'category-theoretic' or 'structural' if that seems more appropriate.  (In the case of the tensor product, for example, I think that using 'structural' gets across the idea perfectly well; if someone has already written 'categorical' on the wiki and its seems disconcerting, then I wouldn\'t change it to 'categorial' but might change it to 'category-theoretic'.)
=--

Lawvere\'s system [[ETCS]] (for 'the Elementary Theory of the Category of Sets') essentially states that the category of sets is a [[topos]] with certain properties, in particular a [[well-pointed topos]]. This can be stated in elementary (first-order) terms; indeed, Lawvere invented the now-default notion of *elementary* topos (in contrast to the original notion of [[Grothendieck topos]]) to do this.

It is also possible to found mathematics on the [[internal logic|internal language]] of a topos. In this case, the topos need *not* be well-pointed (and indeed, the condition that a topos be well-pointed cannot be stated in its own internal language; or if you prefer, *every* topos is well-pointed *internally*). This is equivalent to a certain formulation of type theory, so it is (in a sense) nothing new, although it leads to new perspectives, as in the next paragraph.

Categories (not just toposes) can serve as models of type theories, each type theory corresponding to a certain class of categories. Toposes correspond directly to a constructive but impredicative type theory; to make the theory predicative (in the constructivists\' sense) you generalise to a [[pretopos]] (maybe [[locally cartesian closed category|locally cartesian closed]]), to make the theory nonconstructive you specialise to a [[Boolean topos]], and so on. More specifically, every category\'s internal language is a type theory (with many odd constants), and every type theory (of appropriate form) defines a category (its free model); this is an [[adjunction]] between categories and type theories. Paul Taylor\'s book _[[Practical Foundations|Practical Foundations of Mathematics]]_ is essentially all about this subject, as is (at a more advanced level) most of the career of Michael Makkai.

Certain 'strong' axioms of [[set theory]] (those involving quantification over all sets) are difficult to state in category-theoretic (or type-theoretic) terms, but this can be overcome in a theory like ETCS; talk to Mike Shulman. (Ironically, this makes it harder to do foundations with categorial foundations!)

In contrast, many of the optional or controversial axioms of set theory (such as the [[axiom of choice]]) can be stated quite directly in ETCS. These can be examined quite well in a na&#239;ve set-theoretic language that never need be precise about whether one\'s foundations are traditional (membership-based), categorial, or whatever.

# Categorial foundations of category theory

...


#Other topics#

* There is also [[algebraic set theory]].

#Blog discussion#

* [Foundations](http://golem.ph.utexas.edu/category/2006/10/foundations.html)


[[!redirects Foundations]]
[[!redirects foundations of mathematics]]
[[!redirects foundation of mathematics]]