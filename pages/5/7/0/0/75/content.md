

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+--{: .hide}
[[!include mathematicscontents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Category theory and foundations

There are two big questions about [[category theory]] and the logical foundations of mathematics:

 1. What foundations are adequate to formulate category theory?
 2. How can category theory provide a foundation for mathematics?

These questions also apply to [[higher category theory]], which also involves the relation between them. (Two-categories as a foundation for categories, for example.)

+--{.query}

_[[Urs Schreiber|Urs]] asks_: Concerning the last paranthetical remark: I suppose in this manner one could imagine $(n+1)$-categories as a foundation for $n$-categories? What happens when we let $n \to \infty$?

_[[Toby Bartels|Toby]] answers_: That goes in the last, as yet unwritten, section.

=--

For a philosophical treatment of category theoretic foundations see [[foundations and philosophy]]. 

### Mathematical foundations of category theory

The problem with mathematical foundations of category theory is that in category theory we frequently speak of [[large category|large categories]], which it is tricky to deal with rigorously in the usual sort of [[set theory|set theories]].

One common view seems to be to found category theory on a theory of sets and classes; see [the English Wikipedia\'s definition](), for example. But the standard reference, Saunders Mac Lane\'s _Categories for the Working Mathematician_, assumes the existence of a universe (an inaccessible cardinal) instead. Both of these approaches rely on a distinction between *small* and *large* categories. There is a category of all [[small category|small categories]], but this category is not itself small; there is no category of all categories.

Alexander Grothendieck needed more; he used what we now call [[Grothendieck universe]]s. He assumed that every set is contained within a universe; that is, for every cardinal number $\kappa$, there is a cardinal inaccessible from $\kappa$. (This is still a rather moderate axiom, compared to some of the large-cardinal axioms studied by set theorists.) Now one has a relative notion of small and large; the category of all $U$-small categories (where $U$ is some universe) is $U$-large but must be $U'$-small for some other universe $U'$, and there exists a category (which is both $U$-large and $U'$-large) of all $U'$-small categories.

If one does not accept the [[axiom of choice]], then there are additional complications in general category theory. In particular, one must distinguish between a universal *property* (for example, having all [[product]]s) and having a universal *structure* realising that property (in the example, a functor taking each pair $(x,y)$ of objects to a specific product cone $x \leftarrow x \times y \rightarrow y$). This difficulty was overcome by Michael Makkai using [[anafunctor]]s, but these have not been widely adopted, even by constructivists.

For a summary of the mathematical foundations of category theory, see Mike Shulman, _Set theory for category theory_, [arXiv:0810.1279]().

### The concept of _identity_

One way to think of category theory is as a framework in which the idea is formalized that every kind of [[equality]] is really secretly a choice of [[isomorphism]] or [[equivalence]]. In some sense the notion of identity is potentially [[evil]], in a technical sense.

[[Michael Makkai]] works on a language, [[FOLDS]] ('first-order logic with dependent sorts'), which is designed to make it impossible to formulate any [[evil]] statements.

# Categorial foundations of mathematics

Bill Lawvere proposed to found mathematics on a first-order axiomatisation of [[Cat|the category of categories]]. This has not been very successful, ...
+--{.query}

_[[Urs Schreiber|Urs]] asks_: Can you say what the problem is?

_[[Toby Bartels|Toby]] answers_: I\'d say that it proved to be overkill; ETCS is simpler and no less conceptual. In ETCC (or whatever you call it), you can neatly define a group (for example) as a category with certain properties rather than as a set with certain structure. But then you still have to define a topological space (for example) as a set with certain structure (where a set is defined to be a discrete category, of course). I think that Lawvere himself still wants an ETCC, but everybody else seems to have decided to stick with ETCS.

_Roger Witte_ asks: Surely in ETCC, you define complete Heyting algebras as particular kinds of category and then work with Frames and Locales (ie follow Paul Taylor's leaf and apply Stone Duality).  You should be able to get to Top by examining relationships between Loc and Set.  I thought Top might be the the comma category of forgetful functor from loc to set op and the contravariant powerset functor.  Thus a Topological space would consist of a triple S, L, f where S is a set, L is a locale and f is a function from the objects of the locale to the powerset of S.  A continuous function from S, L, f to S', L', f' is a pair g, h where g is a function from the powerset of S' to the powerset of S and g is a frame homomorphism from L' to L and _(I don't know how to draw the commutation square)_.  However I think this has too many spaces since lattice structures other than the inclusion lattice can be used to define open sets. 

_Toby_:  It\'s straightforward to define a topological space as a set equipped with a subframe of its power set.  So you can define it as a set $S$, a frame $F$, and a frame monomorphism $f\colon F \to P(S)$, or equivalently as a set $S$, a locale $L$, and an epimorphism $f\colon L \to Disc(S)$ of locales, where $Disc(S)$ is the [[discrete space]] on $S$ as a locale.  (Your 'However, [...]' sentence is because you didn\'t specify epimorphism/monomorphism.)  This is a good perspective, but I don\'t think that it\'s any cleaner in ETCC than in ETCS.

_Roger Witte_ says
Thanks, Toby.  I agree with your last sentence but my point is that this approach is equally clean and easy in both systems.  The clean thing about ETCC is the uniformity of meta theory and model theory as category theory.  The clean thing about ETCS is that we have just been studying sets for 150 years, so we have a good intuition for them.

I was responding to your point 'ETCC is less clean because you have to define some things (eg topological spaces) as sets with a structure'.  But you can define and study the structure without referring to the sets and then 'bolt on' the sets (almost like an afterthought).

[[Mike Shulman]]: In particular cases, yes.  I thought the point Toby was trying to make is that only some kinds of structure lend themselves to this naturally.  Groups obviously do.  Perhaps topological spaces were a poorly chosen example of something that doesn't, since as you point out they can naturally be defined via frames.  But consider, for instance, a [[metric space]].  Or a [[graph]].  Or a [[uniform space]].  Or a [[semigroup]].  All of these structures can be easily defined in terms of sets, but I don't see a natural way to define them in terms of categories without going through discrete categories = sets.

_Toby_:  Roger, I don\'t understand how you intend to bolt on sets at the end.  If I define a topological space as a set $S$, a frame $F$, and a frame monomorphism from $F$ to the power frame of $S$, how do I remove the set from this to get something that I can bolt the set onto afterwards?  With semigroups, I can see how, from a certain perspective, it\'s just as well to study the [[Lawvere theory]] of semigroups as a cartesian category, but I don\'t see what to do with topological spaces.

_Roger Witte_ says
If we want to found mathematics in ETCC we want to work on nice categories rather than nice objects.  Nice objects in not nice categories are hard work (and probably 'evil' to somke extent).  Thus the answer to Toby is that to do topology in ETCC you do as much as possible in Locale theory (ie pointless topology) and then when you finally need to do stuff with points, you create Top as a comma like construction (ie you never take away the points but you avoid introducing them as long as possible).  Is it not true that the only reason you want to introduce points is so that you can test them for equality/inequality (as opposed to topological separation)?

Mike, I spent about two weeks trying to figure out how to get around Toby's objection 'topology' and now you chuck four more examples at me.  My gut feeling is that the category of directed graphs is found by taking the skeleton of CAT, that metric locales are regular locales with some extra condition to ensure a finite basis, that Toby can make semigraphs etc.

Since the world of categories (about 50 years old) is currently less familiar than the world of sets (about 150 years old) ETCS is bound to be easier in the short term.  However, if we didn't want a new perspective on existing maths, we wouldn't be investigating alternative foundations.  To my mind, ETCC offers better chances of revealing something in an unexpected new light.

_Toby_:  Ah well, I agree that one should do locale theory!  OK, if your point is that, however convenient ETCS may be as a foundation of *existing* mathematics, working in ETCC is likely to be convenient for useful *future* mathematics, then you may be right!

_Roger Witte_ says
Mike, [A new look at pointfree metrization theorems]().  Two down, Three to go?

Toby
Yes - we already know how to do maths in ETCS but we need to learn how to do it in ETCC.

[[Mike Shulman]]: Roger, I think you're missing the point.  Set theory provides a unifying framework in which to define *all* of these things.  You may be able to come up with *ad hoc* ways of recovering some of them from ETCC, but in ETCS you can define them all in the *same* way, rather than needing to come up with new tricks to deal with each type of structure.

Moreover, something which I think a lot of people don't think about is that just because you can define, in some limited framework, a notion of "X" which can be proven equivalent to the usual way that people think about X's, doesn't mean that your limited framework is completely sufficient for all the mathematical study of X's.  In particular, what about the very theorem that your notion of X is equivalent to the usual notion of X?  Foundations should suggest new ways of thinking, yes, but they should also accomodate the ways in which people already think, and should not throw out good existing mathematics.

I do, however, like the idea of defining, say, "the category of semigroups" via constructions in $Cat$ out of the category $Set$.  That's the sort of thing I've always envisioned that [[michaelshulman:2-categorical logic|elementary 2-topos theory]] would give us.  But that has a very different feel, to me, from ETCC, because it recognizes that ordinary mathematical structures *themselves* are built out of sets, even if we build them by way of building the categories *of* such structures out of the category *of* sets.

_Roger Witte_ Says
No I don't think we do define everything the same way in Set.  I think it feels that way because we have spent 150+ years finding the ad hoc ways of building things with sets followed by unifying the underlying commonalities.  It all feels natural and unified now but it wasn't nearly so obvious that it was so when Frege and Cantor etc. were doing the underlying hard work.

If we want to discover whether using the category of categories we have to find the ad hoc solutions for everything, then assemble them into a logical order and abstract out the commonalities and then see whether we have a beautiful natural and coherent whole - a completely new perspective is inevitably messy initially.

Sometimes our experience with sets helps us find the new way of thinking, sometimes it hinders.  But until we have undertaken the whole effort of providing a good story for how to found mathematics on categories of categories, we won't know whether we have thrown the baby out with the bathwater or whether we have put a new baby in the bath!

_Toby_:  Yeah, I think Mike\'s last comment is unfair ... although it depends on which point he thinks Roger is missing.  ETCC is impractical for existing mathematics; it\'s pretty much immediate how to interpret almost all of 20th-century mathematics within ETCS, which is not exactly the case for ETCC.  Of course, we can do it ---ETCC includes ETCS, after all---, but then it is, as I said, 'overkill'.  But then again, some mathematics is easier to express in ETCC than in ETCS.  If Lawvere\'s vision is that *this* is the more fundamental and important mathematics, then Roger has a point, that it is not fair to judge their relative practicality by 20th-century standards.

_Roger Witte_ Says 
The universal in which we study maths as 'structured sets' is by having forgetful functors to Set that forget structure.  The 150+ years of experience makes it seem natural and obvious which functor to choose.  The yoneda lemma (talking about functors representable in set) is also relevant.

To make ETCC a practical foundation we need to replace these ideas.  We need a generalised theory describing representability and adjunction in cat (similar to yoneda) and we need to find for each kind of structured set, a natural forgetful functor to cat that remembers the structure and forgets the underlying set. This is alraedy intuitive and natural for algebra (although there are exceptions, like field).  This is equally natural for topology (via frames) albeit not yet as intuitive.  If we could address the representatable functor issue, the search for the correct forgetful functors would become much less ad hoc(= more systematic).

[[Mike Shulman]]: To me, anything called a *foundation* should, in particular, suffice as a foundation for *existing* mathematics.  If someone has a "vision" and wants to go off into their own world and invent some new universe of mathematics based on its own foundation, that's their prerogative, but I don't think that justifies calling ETCC a foundation for mathematics.  And I thought that was the point being made: that we don't (currently) know how to describe much ordinary mathematics cleanly in ETCC (without going via ETCS), and so it is not really suitable as a foundation for mathematics.

By the way, one can give a general definition of "structure" in set theory which includes basically everything people study.  Bourbaki did this in one way using material set theory, and versions for structural set theory are also easy to come up with.  So it really is true that we can define everything "in the same way" based on sets.

_Toby_:  ETCC *is* a foundation for existing mathematics, via ETCS, as you note.  It is not a *convenient* foundation for existing mathematics, which explains my answer to Urs up above.  But Roger responds that the mathematics that we should work on in the future is mathematics for which ETCC *is* convenient.  I don\'t see anything contradictory or wrong here, even though Roger\'s position is at least controversial.

BTW, I wouldn\'t say that Bourbaki\'s theory of structure is 'using' material set theory.  Bourbaki dealt with relations, functions, and the like; like their other work, it\'s already structural.  The only reason that you know that their sets are material is because you\'ve read the earlier sections.  (^_^)

[[Mike Shulman]]: What Roger said was that "this approach is equally clean and easy in both systems."  I thought the point of the examples was to show that there are many things that are clean and easy in ETCS but not (at least, not obviously) so in ETCC.  Thus justifying that ETCC is not a convenient foundation for existing mathematics.  I didn't mean to say that ETCC *can't* be a foundation for existing mathematics, just that, as you say, it is not a convenient one.  If Roger agrees with that, then I'm happy.

Re: Bourbaki, I just finished reading (or, rather, skimming) chapter IV of "Theory of Sets".  They define structures using their ZFC-like set theory, and are careful to consider only structures that are defined by "transportable" relations, i.e. which are invariant under isomorphism.  They have to impose this condition explicitly because their set theory is material and would otherwise allow "structure" such as "the structure of being a set that contains $\{\emptyset\}$".  I'm sure that once they get into talking about *particular* structures they use the ordinary mathematical language of relations, functions, and so on, but their general theory of structures seems to me to be very much phrased explicitly in material set theory.
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

It is also possible to found mathematics on the [[internal logic|internal language]] of a topos. In this case, the topos need *not* be well-pointed (and indeed, the condition that a topos be well-pointed cannot be stated in its own internal language; or if you prefer, *every* topos is well-pointed *internally*). This is equivalent to a certain formulation of [[type theory]], so it is (in a sense) nothing new, although it leads to new perspectives, as in the next paragraph.

Categories (not just toposes) can serve as models of [[type theory|type theories]], each type theory corresponding to a certain class of categories. Toposes correspond directly to a constructive but impredicative type theory; to make the theory predicative (in the constructivists\' sense) you generalise to a [[pretopos]] (maybe [[locally cartesian closed category|locally cartesian closed]]), to make the theory nonconstructive you specialise to a [[Boolean topos]], and so on. More specifically, every category\'s internal language is a type theory (with many odd constants), and every type theory (of appropriate form) defines a category (its free model); this is an [[adjunction]] between categories and type theories. Paul Taylor\'s book _[[Practical Foundations|Practical Foundations of Mathematics]]_ is essentially all about this subject, as is (at a more advanced level) most of the career of Michael Makkai.

Certain 'strong' axioms of [[set theory]] (those involving [[quantification]] over all sets) are difficult to state in category-theoretic (or type-theoretic) terms, but this can be overcome in a theory like ETCS; talk to Mike Shulman. (Ironically, this makes it harder to do foundations with categorial foundations!)

In contrast, many of the optional or controversial axioms of set theory (such as the [[axiom of choice]]) can be stated quite directly in ETCS. These can be examined quite well in a na&#239;ve set-theoretic language that never need be precise about whether one\'s foundations are traditional (membership-based), categorial, or whatever.

## Categorial foundations of category theory

...


## Other topics

* There is also [[algebraic set theory]].

### Effect of foundations on concrete problems

It may seem on first sight that foundational questions in mathematics are remote from "real mathematics". This is not quite so. For a list of "real world" problems that do depend on foundations see

* [[effects of foundations on "real" mathematics]]



[[!redirects Foundations]]
[[!redirects foundations of mathematics]]
[[!redirects foundation of mathematics]]
[[!redirects foundation]]
