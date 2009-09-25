+--{: .standout}
This page is (I believe) original research.  Suggestions, corrections, and additions are very welcome.  In particular, if you have suggestions for a better name than SEAR, or if you've seen a similar theory somewhere else, please mention it!  -- [[Mike Shulman]]
=--

# Table of contents

* a table of contents
{:toc}

# Discussions

+--{: .query}
[[Arnold Neumaier]]: 
To me this looks more like a theory of copies of cardinal numbers that like a set theory. I think you should change the name "set" to "universe" or "collection", or so. For your sets have *very* different properties from Cantor's sets, whose terminology surely has priority. Cantor's sets allow unions and intersections, your sets don't. You do not even have the set {0,1,2}. Thus it is impossible to rewrite standard
mathematics on your alternative foundation without 
changing the semantics of everything.

The name subset, on the other hand, is ok, since it shares enough properties of a set to be recognizable as a close relative. On the other hand, there are no functions from a subset to another subset, which again makes it quite cumbersome using this for ordinary mathematics.

How would you form something that substitutes for sets 
of relations, or subsets of subsets? What do you say 
in place of "A is a subset of A$\cup$B"? I think in SEAR,
expressing ordinary mathematics becomes exceedingly 
tedious.

SEAR and ZF, "This process is described at pure set".
This is a sham. There it says "A pure set is a set of pure sets". But with set understood as a SEAR-set, pure sets cannot be compared for equality. But this is an intrinsic part of ZF.

_Toby_:  It is very astute of you to say that this is really a theory of cardinal numbers!  

AN: I did not say that; it isn't. I said that SEAR is a theory of copies of cardinals. For there is a unique cardinal 1 in set theory. But if A,B are two SEAR sets with exactly one element, one is not able to conclude that A and B are the same SEAR set. Thus one can have many meta-distinct copies of the same cardinal around, although it is impossible to express this on the formal level.

*  _Toby_:  Lawvere\'s claim (if I understand him) is that Cantor also had a theory of *copies* of (what we now call) cardinal numbers.  Cantor started with a set $A$ of real numbers, abstracted away everything except the order relation to get the (not necessarily well-)ordinal number $\overline{A}$, then abstracted even the order (but not the equality relation) away to get the cardinal number $\overline{\overline{A}}$.  Of course, he said that $\overline{\overline{A}}$ and $\overline{\overline{B}}$ are equal cardinal numbers if (and only if) there is a bijection between $A$ and $B$, but that is a *definition*, not an axiomatic *identity*.

AN: I'd say this is abstracting away the equality relation
and replace it by isomorphy.

_Toby_ continues: Lawvere has long said that his 'abstract sets' and Cantor\'s 'Kardinalzahl' are the same thing.  But in fact the word 'set' ('Menge') is *not* only used in Cantor\'s original sense of a subset of some fixed universe (originally the collection of real numbers, eventually the entire von Neumann hierarchy) today.  Whenever someone says 'A group is a set equipped with [...]', the only thing that matters for group theory is the abstract set, the Kardinalzahl.  It is very easy to rewrite standard mathematics on this foundation; 

AN: If it were very easy, it would have been done already. 
I see many obstacles in actually doing that. 

*  _Toby_:  It *has* been done already, and has been since at least the \'60s.  

   AN: Then please show me the result in the form of a treatise comparable to Bourbaki's Elements of mathematics. Its existence would mean it has been done. But there is not 
   even a textbook on calculus that is rewritten on this foundation! 

   *  _Toby_:  There is no need to rewrite an ordinary calculus textbook on this foundation, any more than we needed to rewrite elementary geometry after Hilbert.  The material in basic calculus is mostly from the 19th century, after Weierstrass but before Dedekind and Cantor; more advanced material requires care (and indeed, led Dedekind and Cantor to develop set theory), but high school calculus does not.  You may as well rewrite a textbook on the history of the Soviet Union for all the difference that it would make; the latter might at least *mention* set theory if it went deep enough.  The 'sets' of calculus are subsets of $\mathbf{R}$ (or $\mathbf{R}^n$); the 'functions' are partial functions from $\mathbf{R}$ to $\mathbf{R}$, which may be formalised as functional relations.  They are not exactly the same as the 'sets' and 'functions' of either $\mathbf{SEAR}$ or $\mathbf{ZF}$, but we can understand them.

      All that said, calculus *has* been written down in an explicitly structural way, in Errett Bishop\'s book on constructive analysis.  However, the book that you want is probably _Sets for Mathematics_, by Lawvere & Rosebrugh.  Of course, it is not comparable to Bourbaki; nothing is.  You will find it far too brief, but it shows how to get started.

   _Toby_ continues: 
The point of $\mathbf{SEAR}$ is to do it in a less category-inspired, hopefully more familiar, way.  Show me an obstacle in applications of set theory to ordinary mathematics, if you have one.

   AN: The example of the exercise below shows that you need to
interpret all sets of which unions or intersections are taken as subsets of a more universal set. Thus the SEAR notion of set is in fact that of a universe (and nothing like the standard concept of a set), while the notion 
of a SEAR subset is more or less that of an ordinary set. 

   *  _Toby_:  If by 'universe' you mean set&#178; and by 'ordinary set' you mean set&#185;, then you are right.  But you are wrong about what is the standard conception among mathematicians.  There are many of us structural mathematicians; we find each other on the Internet (and found each other before, but I am too young for that); how did that happen? are we suffering from a mass delusion? or perhaps we are not really mathematicians (we have a tendency to work on category theory, after all)?

   Of course, one can embed all mathematics into SEAR (with the right existence axioms) by doing everything inside a
   single universe (= a SEAR set whose cardinality is inaccessible). This is what I would do if I were forced to work in SEAR (which fortunately I am not); then I have materiasl equality of sets (= subsets of the universe).
   Then one can use standard language and standard notation
   without difficulty and doesn't have to rewrite anything, except perhaps add to the strength of SEAR a condition that allows this universe to exists and the collection of its subsets to satisfy the ZF axioms.

   But you'd have to rewrite _everything_ if you want to
   enforce the terminology of SEAR upon mathematics (relabel
   lots of sttandard sets as subsets or tabulations, etc..
   I don't believe mathematical language will take this turn.

   *  _Toby_:  No, you wouldn\'t!  There is no need to strengthen $\mathbf{SEAR}$ to include an uncountable inaccessible cardinal and then talk only about subsets of a universe with that cardinality; indeed, it would be foolish to, since then more things would be true than you had wanted.  Instead, you just write normally, with the abuses of language being slightly different abuses.  See below, where I am more radical than Mike, for more on this.

_Toby_ continues: while in a sense the semantics has changed, it is the claim of structural set theorists that we are getting at what was the real meaning all along.  You might as well say that Dedekind changed the semantics of algebra and analysis when he identified ideal numbers and real (possibly irrational) numbers with certain sets, and in a way he did, but he also clarified those ideas.  And it is not just us, coming along more than a hundred years after Cantor to change the language; people have been doing structural set theory for some time, and it pops up in many places.  Errett Bishop, for example, who wanted a constructive theory (not particularly a structural theory), wrote down a structural theory in his handbook of analysis all the same, even defining a subset of $X$ as a set $A$ equipped with an injection to $X$ (an unfamiliarity which the point of $\mathbf{SEAR}$ is largely to avoid).  Any application of set theory in which we do not care what our sets\' elements\' elements are is inherently structural and translates directly into structural terms.  Any time that someone says 'Relabel the element of $B$ if necessary so that $B$ will be disjoint from $A$, then consider $A \cup B$.', they really mean 'Consider the [[disjoint union]] of $A$ and $B$.' in a structural set theory.  Very rarely do applications of set theory *ever* call for the hierarchy of [[pure sets]].

As for that ... I\'ll assume that you don\'t know the strength of 'sham' in English, so I won\'t feel insulted.  

AN: Sorry. I meant that the pure set page is a caricature of what was promised by the context of the link. (I hope 
this is acceptable language.) No argument was given for 
why the ZF axioms should hold; everything beyond the heditarily finite sets (which is the trivial part of ZF) 
is far too sketchy to support the strong claim that SEAR 
is equivalent to ZF.

*  _Toby_:  This is all fairly well known; see (for example) [Mac Lane & Moerdijk](http://www.amazon.com/Sheaves-Geometry-Logic-Introduction-Universitext/dp/3540977104) (I think Section VI.5) for details (although this does not deal with Replacement/Collection),

   AN:  so it is *not* a verification of the ZF axioms, which is what I had claimed is missing. 

   _Toby_ continues: or Chapter 8 of Mike\'s paper Unbounded Quantifiers and Strong Axioms in Topos Theory (is that available yet, Mike?).  Of course, these start with an explicitly categorial approach, but the equivalence of that with the approach of $\mathbf{SEAR}$ is fairly straightforward.

   [[Mike Shulman]]: No, it's not available yet, sorry.  I got sidetracked with other things.  But it's back near the top of the to-do list.

   AN: Then this should be mentioned in the main text rather thaan left for the reader to discover for himself or to wonder whether this is really true. Mathematics has a healthy convention that nontrivial claims are supported either by proofs or references to such proofs. Without these one is entitled to mistrust the claim.

   _Toby_:  You may mistrust it if you like.  It is mentioned up top that this is all original; if there were papers to cite that we knew of, then we would cite them.  If what you really want is to be certain that mathematics can be founded on a structural theory, then you should look at the established literature on $\mathbf{ETCS}$ or the type theory of Per Martin-L&#246;f and Thierry Coquand.

_Toby_ continues: But if you want precision, look at the **Definition** section, not the vague **Idea**.  Equality of pure sets is also defined.  
(There\'s still an error in that which I haven\'t fixed, but it\'s correct for well-founded pure sets, which are the ones that $\mathbf{ZFC}$ has.)

AN: I only saw a definition of equivalence. Now I realize that this should substitute for the nonexistence equality. 
I'll comment more on the pure set page.

_Toby_ continues: If you want a set of sets, you should consider whether it matters whether any of these sets happen to be equal, and how (for purposes of your application) you would now.  In general, you take a [[family of sets]] (note to self: write an article there), that is an index set $I$ and, for each element $k$ of $I$, a set $S_k$.  There is a handy trick for encoding this sort of thing as a set $\mathcal{S}$ and a function $\pi: \mathcal{S} \to I$; let $S_k$ be the preimage of $\pi^*(k)$ (which is a subset of $\mathcal{S}$.  The purpose of the axiom of collection is to allow you to construct this set $\mathcal{S}$ (maybe I should write that down there for its motivation!).  If you want, say, a family of groups, then you take $\pi: \mathcal{S} \to I$ and additionally a function $M: I \times \mathcal{S} \times \mathcal{S} \to \mathcal{S}$ such that, for each $k$, $M$ restricts to a function $m_k: S_k \times S_k \to S_k$ that satisfies the group axioms.  And so on.

In this situation, you can\'t ask whether $S_k = S_{k'}$, or try $S_k \cap S_{k'}$, etc.  If the structural perspective is valid, then you should only ever want to do that if the various $S_k$ are all subsets of some previously given ambient set $T$.  There are two ways to do this; either define an $I$-indexed family of injections $S_k \to T$, or skip all of the above and instead consider a binary relation on $I$ and $T$; let $S_k$ be the set of elements of $T$ that $k$ is related to.  This is a family of unary relations on $T$; you can do a set of binary relations in a similar way.  (By the way, in this case you don\'t need the axiom of collection to define $\mathcal{S}$, since you can make it a subset of $I \times T$.  This is the idea, possibly familiar to you, that replacement/collection is not needed wherever it na&#239;vely applies, but only for relatively high-powered stuff.)

[[David Roberts]]: I was going to ask something about the claim that after axioms 0,1 and 2 we have a category of sets (which I think is very cool), but I convinced myself that this was a metacategory with a collection of arrows between a pair of objects and a composite for each pair of (composable) arrows one is given. However, from Mike's reply to my question, we can use the definition of the set of functions to then define a metacategory  with a set of arrows between any two objects (this I must admit requires more than just a sweeping statement) but still only a collection of objects. Once one has defined universes, then - as much as I understand it - things can proceed much as with any other category $U-Set$ one might define with a universe $U$. We then have the universal family that the axiom of collection is a virtual shadow of.

In response to Toby's comment about forming the union of sets above: it always annoyed me that people worry whether sets just happen to have elements in common. It is very much a \'is $\sqrt{2} \in \pi$?\' type thing. 

[[Mike Shulman]]: I agree with pretty much everything Toby said, except that I don't think I would go so far as to claim that structural set theory gets at *what was the real meaning all along*.  Maybe it's what Cantor meant, maybe it isn't (probably he wouldn't even have understood the question as we ask it today).  Instead, I would say that over the course of the 20th century, it *emerged* that sets in mathematics were only ever really *used* structurally. 

AN: only ever?? Undergraduate mathematics is always conceived of materially. It can hardly be taught from a strictly structural point of view. Even many of the most exercises for undergraduates would have to be rewritten completely, and to avoid that things would get completely confusing, utmost care is needed.

SEAR cannot even define the elementary sets {a,b,c} and {a,b,d} and take their union {a,b,c,d}. These objects exist in SEAR only as subsets, but they are different objects depending on the set a,b,c,d are elements of. But it doesn't matter which set this is, and a purely 
structural view should take that into account! 
Thus one needs to assume a universal set from which all objects of discourse are taken that one might want to have as element in some set. (For maybe one will later introduce an element e....) The subsets of this universal set then form a proxy of the sets of standard set theory. 
But having that (and augmenting the universal set to contain power sets, which is a natural next step), 
one can do all standard mathematics in this universal set, obviating the need for SEAR. 

*  _Toby_:  I have taught na&#239;ve set theory in a structural way.  

   AN: I's like to get a copy of the lecture notes!

   *  _Toby_:  No lecture notes, I\'m afraid, but you can look at the [homework assignments](http://www.ugcs.caltech.edu/~toby/MATH11/2006/homework/).  I\'m not sure if you\'ll like it, since it\'s not very formal; I\'ll probably still have to convince you that everything can be formalised in $\mathbf{SEAR}$ (which is fine, just ask).  The assignment for July 10 makes it particularly clear that the set theory is structural, and it shows you how to intepret in a structural framework some of the most basic questions of na&#239;ve set theory; the assignment for July 13 is also a good one for featuring the disjoint union.  But really, the point to get is that you normally *can\'t* tell whether someone thinks of set theory materially or structurally; the ideas are almost always almost exactly the same.  So if you\'re not sure how to formalise, say, July 11 in $\mathbf{SEAR}$, then perhaps we should talk about that.

   _Toby_ continues: 
Not that I made a big point about that, but then I didn\'t need to!  The only thing unusual that I had to do was to introduce the concept of disjoint union, which actually made the applications in that course (which were to combinatorics) a little easier.  Of course, a course in axiomatic set theory would have to be rewritten.

   For the exercise 'What is the union of $\{a,b,c\}$ and $\{a,b,d\}$?', there is no need to change that in the na&#239;ve course.  But formally, it means 'Let $U$ be a set, and let $a,b,c,d$ be elements of $U$.  Then (by previous results) we have subsets $\{a,b,c\}$ and $\{a,b,d\}$ of $U$.  Find a similar expression for the union of these subsets.'.

   AN: And you are not allowed to claim that {a,b,c} are sets!
   I am quite sure you didn't go that far in your course on naive set theory!

   _Toby_:  I don\'t understand what you\'re saying that I\'m not allowed to claim here.  There is a technical distinction between $\{a,b,c\}$ as a subset of $U$ and $\{a,b,c\}$ as a $3$-element set in its own right, one which is usually glossed over.  But you can think of it as either, if you wish.  The subset comes first; in $\mathbf{SEAR}$ it is a relation $1 \looparrowright U$; then its tabulation is a $3$-element set, which by abuse of notation we also write $\{a,b,c\}$.

Mike Shulman continues:
 The reason I believe in structural set theory is not out of a philosophy that this is the "real" meaning of sets; in fact I think that ZF-theorists are studying a very real and interesting world!  But when I look at most mathematics as it is done by most mathematicians, what I see is sets treated structurally---so I think we should have a foundational account of sets which treats them that way.

AN: And when I look at most mathematics as it is done by most mathematicians, what I see is sets treated materially.

Clearly, this is not inherent in the mathematical writings but in the view. One needs both the material and the structural view, and foundations should provide both in an easy way. 

To start with the material point of view has many advantages: It is easy to motivate, makes for easy language, and most textbooks are already written in 
that style.

[[Mike Shulman]]: Can you cite some example of mathematics outside of ZF-theory which really treats sets materially?

AN:  In analysis, the vector space of real n-dimensional 
column vectors is probably universally treated as material.

*  _Toby_:  How can you tell?

The material point of view is even clearly visible in books on abstract algebra that use category theory, such as 

:  Serge Lang, Algebra, second printing 1970 

(which I happen to have at hand; sorry - my books on elementary math are all 40 years old, but all mathematics done then is still valid mathematics today!)

He begins in the first paragraph of the prerequisites 
with the assumption that a set may be contained in another set. This is actually heavily used; for example, a subgroup is for him clearly a group contained in another group, and not a group isomorphic to a such a group.

[This is also the case in modern text; the first algebra lecture notes I found with Google was 
[by Wilkins](http://www.maths.tcd.ie/~dwilkins/Courses/311/311S1_0708.pdf) has the same terminology for subgroups.

In Section I.7 on categories, he explicitly uses the formula A=B comparing two objects of a category for equality. Since Lang explicitly defines each allowed abuse of language, e.g., "By abuse of language, we sometimes refer to the collection of objects [of a category] as the category itself", it is clear that he doesn't consider A=B as an abuse of language, and hence adheres to a material point of view.

*  _Toby_:  If $A$ and $B$ are objects in the same category, then writing $A = B$ is perfectly structural.  It\'s [[evil]], but that\'s a somewhat different matter.  In category theory founded on $\mathbf{SEAR}$, comparing objects of a small category for equality is perfectly legitimate, because we have a set of objects.  It gets messier when you talk about *large* categories; since you can\'t write $A = B$ for sets in $\mathbf{SEAR}$, you can\'t do it for objects of the category of sets either.  (On the other hand, this is still not a matter of structural set theory exactly; for example $\mathbf{ETCS}$ admits a notion of equality of sets.)

One can probably rewrite everything in a way that avoids all material issues, but 
(i) it hasn't be done, and 
(ii) it would read quite different from what Lang actually writes.

[[Mike Shulman]]: I think the claim is not that existing mathematics doesn't use the *language* of material set theory (after all, for decades that was the only language there was), but rather that its *essence* does not.  Show me a result using the fact that a subgroup is a group literally contained in another group, but which would not work just as well for any injective group homomorphism.

AN: Maybe, but this cannot be discussed objectively since essence is not well-defined. 

_Toby_:  I *do* claim that existing mathematics uses the language of material set theory only a little more than it uses the language of structural set theory; for the most part, it is simply indifferent between them.  In both cases, it is rife with little abuses of terminology and notation; if (like Lang) one is careful about that sort of thing, then it will be clear whether one thinks of sets materially or structurally.  But if Lang had written the prerequisite set theory structurally, then the definition of 'subgroup' could still have been written with exactly the same words (from my copy, 1993 edition)

>Let $G$ be a group.  A __subgroup__ $H$ of $G$ is a subset of $G$ containing the unit element, and such that $H$ is closed under the law of composition and inverse.

In the prerequisites, he might(\*) mention the abuse of language in which a subset is conflated with its underlying set (what Mike calls its 'tabulation'), which we need in order to think of $H$ as a set (and then a group) in its own right.  But that is all in the set theory; the language of algebra is *the same*.

(\*)  On the other hand, there are other things that he did not mention.  For a map $f : A \to B$, he defined the preimage $f^{-1}(B')$ of a subset $B'$ of $B$, but never defined the image $f(A')$ of a subset of $A$, even though this is used in the text.  (He only mentioned $f(A)$ itself.)  If he had, then he would have had to note the ambiguity in the case that $A'$ is also an element of $A$; this doesn\'t come up structurally.  (Even for $f(A)$, it\'s hard to imagine that really intended to rely on the axiom of foundation to rule out the possibility that $A \in A$.)  He took care to define what a 'family of elements' of a given set is, but not a 'family of sets', even though he mentions the concept.  That is harder to formalise, both materially and structurally.  Basically, he seems to avoid things that are tricky to state precisely.

The most common exception that I admit to my thesis is the [[disjoint union]], or rather the reluctance to see this as one of the basic operations of set theory.  It is actually easier (although not much) to construct a disjoint union materially than structurally (unless you take its existence as an axiom), but many people don\'t bother.  What I do see is a lot of broad abuse of language to get around this, such as 'Take two disjoint copies of $A$.' or 'If $A$ and $B$ are not disjoint, then relabel the elements of $B$ so that they are, and consider $A \cup B$.'.  Structurally, you would not be tempted to say such things; although if we had all grown up with structural set theory, I\'m afraid that we might have a tendency write '$A \cup B$' for the disjoint union when $A$ and $B$ bear no relation, and that would also be an abuse of notation.

[[Mike Shulman]]: I'm actually basically in agreement with you, Toby, but I didn't feel like getting into detail about the sorts of "abuses" (i.e. definitions of terminology/notation) that are necessary to read existing mathematics in a structural way.  But you make a good point that reading it in a material way requires different "abuses," some of which people tend to make explicit and some of which they don't.

BTW, in a more leisurely pedagogical treatment of SEAR, I would be tempted to include an axiom of disjoint unions early on, and only remark later, after powersets are introduced, that they imply the existence of disjoint unions.
=--


# Introduction #

**SEAR**, short for **Sets, Elements, And Relations**, is a [[structural set theory]] with the following properties:

* It is equivalent in strength to the [[material set theory]] [[ZF]].  (It can be augmented by an [[axiom of choice]] to produce *SEAR-C*, which is strongly equivalent to [[ZFC]].)
* It contains a subtheory called **bounded SEAR** which (when augmented by choice) is strongly equivalent to [[ETCS]].  Conversely, ETCS can be augmented by a replacement axiom to become equivalent to SEAR-C.

Being a structural set theory, SEAR differs from ZF in the following ways (which are also ways in which it is similar to ETCS):

* There is a type distinction between *sets* and *elements*; a set is never an element of another set.  Every element is an element *of some set*.
* The elements of a set have no "internal structure;" they are merely featureless points.
* The "elementhood" relation $x\in A$ only makes sense when $x$ is known to be an element of some ambient set $X$ and $A$ is known to be a subset of $X$.

A good description of the difference between material and structural set theory can be found at [[Trimble on ETCS I]].  However, ZFC and ETCS also differ along another axis than the material-structural.  At [[Trimble on ETCS III]] the following metaphor is proposed for this dimension:

> with ZFC it's more as if you can just hop in the car and go; with ETCS you build the car engine from smaller parts with your bare hands, but in the process you become an expert mechanic, and are not so rigidly attached to a particular make and model.

Using this metaphor, SEAR can be thought of as an ETCS-car which comes preassembled with a nice slick control panel.  Or, using an alternate metaphor, ZFC is like Windows, ETCS is like UNIX, and SEAR is like OS X (or maybe Ubuntu).  With SEAR you get a nice familiar interface with which it is easy to do standard things, there is less cruft than you get with ZFC, and behind the scenes you have all the power of ETCS (and more).  (Of course, if you like Microsoft products, then this metaphor probably does not appeal to you.)

Note that experts will probably always prefer to build their own car/OS; the goal of SEAR is to make structural set theory accessible to a wider audience.  In particular, SEAR is intended to demonstrate the complete independence of [[structural set theory]] from [[category theory]].  Thus, apart from being (by default) stronger than ETCS, SEAR differs from it in the following ways:

* It includes the notion of an *element* of a set as a primitive concept, rather than defining it as a particular sort of function.
* It does *not* include the notion of a [[function]] as a primitive concept (instead it includes the notion of a [[binary relation]], with functions defined via their [[graph of a function|graphs]] in a familiar way).
* It does not include the notions of composition or identities (of either functions or relations) as primitive concepts.  In particular, it does not require the user to know what a [[category]] is, even implicitly.
* As a corollary, its axioms do not require knowledge of categorical concepts such as [[limits]] and [[natural numbers objects]] (although these concepts can be very naturally introduced while learning SEAR).
* The property of [[axiom of separation|separation]] (one of the most important facts in the everyday use of set theory) is a direct consequence of the axioms of SEAR.  Compare how in ETCS, the property of bounded separation follows from the theorem that a [[topos]] is a [[Heyting category]], which requires [[Trimble on ETCS II|substantial work]].


# Description of SEAR #

## Types ##

SEAR is a theory about three kinds of things: **sets**, **elements**, and **relations**.  Every element, and every variable that ranges over elements, is always associated to something denoting a set (which might be a constant or a variable); we say it is an element **of** that set.  If $x$ is an element of $A$ we write $x\in A$; note that this is not an *assertion* which may be true or false, but a *typing* declaration.  In formal terms, this means that SEAR is a [[dependent type theory]], with a type of sets, a type of elements for each set term, and a type of relations for each pair of set terms. 
+--{: .query}
[[Arnold Neumaier]]: 
After the discussion on the n-Cafe, I understand this better and would appreciate rewording, either:

SEAR is a theory about infinitely many types of things: **sets**, **elements of $S$** for any set $S$, and **relations between $S$ and $T$** for any set $S$ and any set $T$. Every element...

or:

SEAR is a theory about three kinds of things: **sets**, **elements**, and **relations**.  ... In formal terms, this means that SEAR is a [[dependent type theory]] whose types are **sets**, **elements of $S$** for any set $S$, and **relations between $S$ and $T$** for any set $S$ and any set $T$. 

_Toby_:  Yes, you\'re right; I like the second, which I incorporated and rephrased slightly.

[[Mike Shulman]]: Yes, this is good.
=--
One consequence of this is that whenever we quantify over elements we must always quantify over elements *of some set*; thus we can say "for all elements $x\in A$" but not "for all elements $x$."  Another consequence is that the assertion $x=y$ is only well-formed (a precondition to its being true _or_ false) if $x$ and $y$ are elements of the same set.

In a similar manner, every relation is always associated to an ordered pair of sets, the first called its **[[source]]** and the second its **[[target]]** (thus the fundamental relations in SEAR are binary relations).  If $\varphi$ is a relation from $A$ to $B$ we write $\varphi:A\looparrowright B$.  As with elements, the assertion $\varphi=\psi$ is only well-formed if $\varphi$ and $\psi$ have the same source and the same target.

Implicit in the existence of three types of things is that nothing is both a set and an element, etc., so in particular a statement such as $x=A$ is not well-formed if $x$ is an element and $A$ a set.  Furthermore, SEAR does not include an equality relation between sets: even if $A$ and $B$ are both sets we do not consider $A=B$ to be well-formed.  (Thus SEAR adheres to the philosophy of "speak no [[evil]].")

The final piece of data that we have is a notion of when a relation $\varphi:A\looparrowright B$ **holds** of a pair of elements $x\in A$ and $y\in B$.  We write $\varphi(x,y)$ when $\varphi$ holds of $x$ and $y$.


## Basic axioms ##

Now we can state the axioms of SEAR, beginning with the most basic ones.

**Axiom 0 (Nontriviality):** _There exists a set which contains an element._

**Axiom 1 (Relational comprehension):** _For any two sets $A$ and $B$, and any property $P$ that can obtain of an element of $A$ and an element of $B$, there exists a unique relation $\varphi:A\looparrowright B$ such that $\varphi(x,y)$ if and only if $P$ obtains of $x$ and $y$._

Here "property" is interpreted formally as "first-order formula", which makes the axiom (like later the axiom of collection) in fact an axiom scheme.

+--{: .query}
[[Arnold Neumaier]]: 
I think some details should be added in the beginning (rather than late in the text) for how SEAR cooperates with logic.
Aopparently, the logic presupposed is first order logic, although the comment on Axiom 1 is too vague since there is no clear commitment to the meaning of a property. 
Later it says that the ambient logic may be classical or constructive. I take the latter to be intuitionistic. 
(The link offered gives no clear definition of what a constructive logic is.)

[[Mike Shulman]]:  Unfortunately, most mathematicians aren't that conversant with the language of logic, so my thought was not to frighten them off with too much of it.  Of course, the logic is first order logic.  Likewise, I think most mathematicians have little appreciation of constructive (=intuitionistic) logic, so the theory is presented as classical by default (but, unlike some of the more common presentations of ZF, the axioms as stated are still correct intuitionistically).

[[Arnold Neumaier]]: Changing the first sentence after Axiom 1 to
"Here "property" is interpreted formally as "first-order formula", which makes the axiom (like later the axiom of collection) in fact an axiom scheme.
Axiom 1 basically says that relations are what we expect them to be intuitively. It should remind the reader of the axiom of separation."
is not more frightening but makes things perfectly precise.
If you don't explain clearly waht a property is, you effectively have "property" as another type in your theory, and since no axioms are given for it, it is incomprehensible.

_Toby_:  I think that I\'ve fixed these somewhat, in part using your phrasing above.

[[Mike Shulman]]: Thanks for the suggestion; I think it reads better now.  But there is probably still room for improvement.
=--

Axiom 1 basically says that relations are what we expect them to be intuitively.  It should remind the reader of the [[axiom of separation]].  The two important differences are (1) the presence of two sets and two variables, rather than one, and (2) the fact that what is produced is not a *set*, but a *relation* (a different kind of thing). The to-be-introduced Axiom 2 will enable us to make relations into (sub)sets, but first we need some terminology.

+-- {: .num_defn #function}
###### Definition
A relation $\varphi:A\looparrowright B$ is called a **[[function]]** from $A$ to $B$ if for any $x\in A$, there exists exactly one $y\in B$ with $\varphi(x,y)$.
=--

We write $f:A\to B$ for such a function, and for $x\in A$ we write $f(x)$ for the resulting unique $y\in B$.  Note that the uniqueness clause in Axiom 1 implies that functions are extensional: if $f,g:A\to B$ and $f(x)=g(x)$ for all $x\in A$, then $f=g$.

**Axiom 2 (Tabulations):** _For any relation $\varphi:A\looparrowright B$, there exists a set $|\varphi|$ and functions $p:{|\varphi|}\to A$ and $q:{|\varphi|}\to B$ such that: (1) for any $x\in A$ and $y\in B$, we have $\varphi(x,y)$ if and only if there exists $r\in {|\varphi|}$ with $p(r)=x$ and $q(r)=y$, and (2) for any $r\in {|\varphi|}$ and $s\in{|\varphi|}$, if $p(r)=p(s)$ and $q(r)=q(s)$, then $r=s$._

A set $|\varphi|$ equipped with $p$ and $q$ as in Axiom 2 is called a **tabulation** of the relation $\varphi$.  We think of $|\varphi|$ as "the set of pairs $(x,y)$ such that $\varphi(x,y)$ holds," with $p$ and $q$ projecting $(x,y)$ to $x$ and $y$, respectively.  Note that by Axiom 1, any set $R$ equipped with functions $p:R\to A$ and $q:R\to B$ satisfying (2) determines a unique relation $\varphi:A\looparrowright B$ such that $\varphi(x,y)$ holds iff there is an $r\in R$ with $p(r)=x$ and $q(r)=y$; then $R$ is a tabulation of $\varphi$.


## Consequences of the basic axioms ##

Axioms 0, 1, and 2 alone are very powerful!  Here are some things we can do with them.

+-- {: .num_theorem #emptyset}
###### Theorem
There exists a set $\emptyset$ which has no elements.
=--
+--{: .proof}
###### Proof
By Axiom 0, there exists a set $A$.  By Axiom 1, there exists a relation $\varphi:A\looparrowright A$ such that $\varphi(x,y)$ holds *never*.  Using Axiom 2, let $\emptyset$ be a tabulation of $\varphi$.
=--

From now on we fix a particular set $\emptyset$ having no elements.  By Axiom 1, for any set $A$ there is exactly one relation $\emptyset\looparrowright A$ and exactly one relation $A\looparrowright\emptyset$.

+-- {: .num_theorem #terminalset}
###### Theorem
There exists a set $1$ which has exactly one element.
=--
+--{: .proof}
###### Proof
By Axiom 0, there exists a set $A$ containing an element $x$.  By Axiom 1, there exists a relation $\varphi:A\looparrowright A$ such that $\varphi(y,z)$ holds iff $y=x$ and $z=x$.  Using Axiom 2, let $1$ be a tabulation of $\varphi$.
=--

From now on we fix a particular set $1$ having exactly one element;
we usually denote this element by $\star$.  By Axiom 1, for every set $A$ there exists a unique function $f:A\to 1$, defined by $f(x)=\star$ for every $x\in A$.  Likewise, to every function $g:1\to A$ there corresponds a unique element $x\in A$, by $g(\star)=x$.

We define a **subset** of a set $A$ to be a relation $S:1\looparrowright A$.  By Axiom 1, a subset $S$ of $A$ is determined by precisely those $x\in A$ such that $S(\star,x)$.  If $S(\star,x)$ we write $x\in S$.  Note that this is an *overloading* of the notation $\in$; it can be distinguished from the previous usage because here $S$ is a relation, not a set.  Note also that the previous usage $x\in A$ was a typing declaration (it says what kind of thing $x$ is when we introduce it), whereas $x\in S$ is a statement which can be either true or false.

Now Axiom 2 implies that from any subset $S$ of $A$ we can construct a set $|S|$ with a function $i:{|S|}\to A$ such that (1) $x\in S$ iff there is an $x'\in {|S|}$ with $i(x')=x$, and (2) for $x',x''\in {|S|}$, if $i(x')=i(x'')$ then $x'=x''$.  A function $i$ with property (2) is called **injective**; in this way we set up a correspondence between subsets and injective functions.  (Likewise, a function $f:A\to B$ is **surjective** if for any $y\in B$ there is an $x\in A$ with $f(x)=y$.)  Combined with Axiom 1, this implies the following *separation property*.

+-- {: .num_theorem #sep}
###### Theorem
For any property $P$ of elements of a set $A$, there exists a set $B$ and an injective function $i:B\to A$ such that for $a\in A$, we have $P(a)$ iff $a=i(b)$ for some $b\in B$.
=--

Although the set $|S|$ is not determined uniquely by the subset $S$, it is determined up to [[bijection]].  We define an **bijection** to be a relation $\psi:A\looparrowright B$ such that for every $x\in A$ there is a unique $y\in B$ with $\psi(x,y)$, and for every $y\in B$ there is a unique $x\in A$ with $\psi(x,y)$.  Clearly any bijection is a function, as is its opposite (defined by $\psi^o(y,x) \Leftrightarrow \psi(x,y)$), and these two properties characterize bijections.  It is also easy to see that a function is a bijection iff it is both injective and surjective.

For example, it is easy to see that if $A$ and $B$ both have no elements, there is a unique bijection between them; thus an empty set $\emptyset$ is determined up to unique bijection.  Likewise, if $A$ and $B$ both contain a unique element, then there is a unique bijection between them; thus a set $1$ with one element is also determined up to unique bijection.

+-- {: .num_theorem #tabuniq}
###### Theorem
If $|\varphi|$ and ${|\varphi|}'$ are two tabulations of the same relation $\varphi:A\looparrowright B$, then there is a bijection between $|\varphi|$ and ${|\varphi|}'$.
=--
+--{: .proof}
###### Proof
By Axiom 1, define $B:{|\varphi|} \looparrowright {|\varphi|}'$ such that $B(x,y)$ holds precisely when $p(x)=p'(y)$ and $q(x)=q'(y)$.  The properties of tabulations immediately imply that $B$ is a bijection.
=--

+-- {: .num_cor #sstabuniq}
###### Corollary
If $|S|$ and ${|S|}'$ are two tabulations of the same subset $S\subseteq A$, then there is a bijection between $|S|$ and ${|S|}'$.
=--

+--{: .query}
_AN_: I dont understand why this is a particular case of Theorem \ref{tabuniq}; if true, it should be a corollary. You didn't asssume that the empty set is a tabulation, so this remains to be proved.

_Toby_: Yes, the empty set *was* defined as a tabulation, as were $|S|$ (for $S$ some subset) and $1$.

AN: No. I read "From now on we fix a particular set &#8709; having no elements." and "From now on we fix a particular set 1 having exactly one element."
No tabulation is mentioned. Thus (and this is desirable even if you change these two sentences to refer to tabulations only) you need to prove somewhere that 
any two empty sets and any two sets of cardinality one are isomorphic.

[[Mike Shulman]]: Toby is right, but actually it was extremely silly to conclude the uniqueness of $\emptyset$ and $1$ from this theorem, since those are both much more obvious.  I've also restated the version for subsets as a corollary; is this better?

AN: You were too quick in giving Toby right. 
But the corollary is ok, 

_Toby_:  Ah, I see your point!  It would be better to define $\empty$ and $1$ as given by the tabulations in the proofs of the theorems (which is what I looked at to decide if there was a problem), then prove that every empty set is isomorphic to $\empty$ and every singleton set is isomoprhic to $1$.  That really is easy; the corollaries after those theorems that begin 'By Axiom 1' will do the job.  Perhaps I will write that up today.
=--

The **composite** of two relations $\varphi:A\looparrowright B$ and $\psi:B\looparrowright C$ is defined to be the relation $\psi\varphi:A\looparrowright C$ (also written $\psi\circ\varphi$) such that $\psi\varphi(x,z)$ holds of $x\in A$ and $z\in C$ iff there is a $y\in B$ with $\varphi(x,y)$ and $\psi(y,z)$.  The **identity** relation $id_A:A\looparrowright A$ is defined by $id_A(x,y) \Leftrightarrow x=y$.

+-- {: .num_theorem #category}
###### Theorem
Composition of relations is associative ($\chi(\psi\varphi)=(\chi\psi)\varphi$), and identity relations are identities for composition ($\id_B\circ \varphi = \varphi = \varphi\circ\id_A$).  The composite of functions is a function, and the identity relation is a function.  The composite of bijections is a bijection, and a relation $\varphi:A\looparrowright B$ is a bijection iff there is a relation $\psi:B\looparrowright A$ such that $\psi\varphi = id_A$ and $\varphi\psi=id_B$.
=--
+--{: .proof}
###### Proof
Just as in naive set theory.
=--

Informally speaking, we have two [[categories]] whose objects are the sets: in [[Rel]] the morphisms are the relations, while in [[Set]] the morphisms are the functions.  Formally, all we can say is that these are "meta-categories," in the sense that from any model of the first-order axioms of SEAR we can construct them as models of the first-order axioms of a category.  (This is not that different from the status of large categories such as $Set$ in material set theories such as ZF.  We could also speak about "proper classes" as is done in ZF using first-order formulas.)  See also the section on Universes, below.

In both of these (meta-)categories, the [[isomorphisms]] are the bijections.  We have also already observed that $\emptyset$ and $1$ are an [[initial object]] and a [[terminal object]] in $Set$, respectively, and that $\emptyset$ is both initial and terminal in $Rel$.

For sets $A$ and $B$, let $\top:A\looparrowright B$ denote the relation such that $\top(x,y)$ holds always.  A tabulation of $\top$ is denoted $A\times B$; it is a set equipped with functions $p:A\times B \to A$ and $q:A\times B\to B$ such that for any $x\in A$ and $y\in B$, there exists a unique $z\in A\times B$ with $p(z)=x$ and $q(z)=y$.  It is called the **cartesian product** of $A$ and $B$.

+-- {: .num_theorem #product}
###### Theorem
For any sets $A$ and $B$, $A\times B$ is a [[product]] of $A$ and $B$ in the category $Set$, and a [[coproduct]] in the category $Rel$.
=--
+--{: .proof}
###### Proof
Just as in naive set theory.
=--

In particular, $Set$ has products.

+-- {: .num_theorem #lex}
###### Theorem
The category $Set$ has finite limits.
=--
+--{: .proof}
###### Proof
It remains to construct the [[equalizer]] of two functions $f,g:A\to B$.  Let $S$ be the subset of $A$ so that $x\in S$ just when $f(x)=g(x)$; then ${|S|}\to A$ is easily shown to be an equalizer of $f$ and $g$.
=--

+-- {: .num_theorem #imfact}
###### Theorem
For any function $f:A\to B$ we have $f = m e$, where $m:im(f)\hookrightarrow B$ is an injection and $e:A\twoheadrightarrow im(f)$ is a surjection.  A set $im(f)$ equipped with such $m$ and $e$ is unique up to bijection and is called the **image** of $f$.
=--
+--{: .proof}
###### Proof
Let $im(f)$ be $|S|$ where $S$ is defined by $y\in S$ iff there exists an $x\in A$ with $f(x)=y$.  By definition, we have an injection $m:im(f)\hookrightarrow B$.  And for any $x\in A$, clearly $f(x)\in S$, so there is a unique $y\in im(f)$ with $m(y)=f(x)$; we define $e(x)=y$.  It is easy to verify the rest.
=--

Similarly, we can define the union and intersection of subsets of $A$ in the usual way: we have $x\in S\cup T$ iff $x\in S$ or $x\in T$, and $x\in S\cap T$ iff $x\in S$ and $x\in T$.

+-- {: .num_theorem #heyting}
###### Theorem
$Set$ is a [[well-pointed category|well-pointed]] [[Heyting category]] and $Rel$ is a [[division allegory]].
=--
+--{: .proof}
###### Proof
Left to the reader.
=--


## Power sets and colimits ##

In structural set theory, sets cannot contain other sets (or relations), so we cannot strictly speaking have "the set of subsets of a set $A$."  What we generally do instead is have a set $P A$ each of whose elements is *associated to* a subset of $A$ in a bijective way.  This association happens via a specified relation between $A$ and $P A$.

**Axiom 3 (power sets):** _For any set $A$, there exists a set $P A$ and a relation $\epsilon:A\looparrowright P A$ such that for any subset $S$ of $A$, there exists a unique $s\in P A$ with the property that for any $x\in A$, we have $x\in S$ iff $\epsilon(x,s)$._

As in both material set theory and ETCS, many useful consequences flow from this axiom.  We first observe that the property of $P A$ stated for subsets actually implies an analogous property for all relations.


+-- {: .num_theorem #topos}
###### Theorem
For any relation $R:B\looparrowright A$, there exists a unique function $f_R:B\to P A$ such that $R(y,x)$ if and only if $\epsilon(x,f_R(y))$.  It follows that $Set$ is a [[topos]] (and $Rel$ is a power allegory).
=--
+--{: .proof}
###### Proof
We simply define $f_R$ elementwise; for each $y$ we define $f_R(y)$ to be the unique element of $P A$ such that $\epsilon(x,f_R(y))$ holds iff $R(y,x)$ holds.  Extensionality of functions implies that it is unique.
=--

As usual, power sets also imply the existence of function sets.

+-- {: .num_theorem #ccc}
###### Theorem
For any two sets $A$ and $B$, there exists a set $B^A$ and a function $ev:B^A \times A\to B$ such that for any function $f:A\to B$ there exists a unique element $s_f\in B^A$ such that $ev(s_f,a)=f(a)$ for all $a\in A$.  It follows that $Set$ is a [[cartesian closed category]].
=--
+--{: .proof}
###### Proof
We take $B^A$ to be a tabulation of the subset of $P(A\times B)$ containing only the functions.  More precisely, define $F\subseteq P(A\times B)$ such that $s\in F$ iff for every $x\in A$, there exists a unique $y\in B$ such that $\epsilon((x,y),s)$, and let $B^A = {|F|}$.
=--

The correspondences in Theorems \ref{topos} and \ref{ccc} are "meta-bijections," but by a standard Yoneda lemma argument they can be converted into actual bijections as defined above in SEAR.  This produces bijections such as $C^{A\times B} \cong (C^A)^B$ and $P(A\times B) \cong (P A)^B$.

We now construct [[quotient set]]s.  Of course, by an **[[equivalence relation]]** on a set $A$ we mean a relation $R:A\looparrowright A$ which is reflexive, transitive, and symmetric.

+-- {: .num_theorem #quotients}
###### Theorem
If $R$ is an equivalence relation on $A$, then there is a surjective function $q:A\twoheadrightarrow B$ such that $R(x,y)$ holds iff $q(x)=q(y)$.
=--
+--{: .proof}
###### Proof
$R$ induces a function $f_R:A\to P A$ as above; let $B$ be $im(f_R)$ and $q$ the surjective part of the image factorization.  If $R(x,y)$ holds, then by symmetry and transitivity, $R(x,z)\Leftrightarrow R(y,z)$ for all $z$; hence $f_R(x)=f_R(y)$ and so $q(x)=q(y)$.  Conversely, if $q(x)=q(y)$, then $f_R(x)=f_R(y)$; but $y\in f_R(y)$ by reflexivity, hence $y\in f_R(x)$ and thus $R(x,y)$ holds.
=--

Such a $B$, which is easily seen to be unique up to bijection, is called a **quotient** of $R$ and often written $A/R$.

Likewise, given sets $A$ and $B$, let $A\sqcup B={|S|}$, where $S$ is the subset of $P A \times P B$ consisting of the pairs $(\{x\},\{\})$ for $x\in A$ and $(\{\},\{y\})$ for $y\in B$.  (Of course, here we are identifying elements of $P A \times P B$ with ordered pairs of subsets of $A$ and $B$ via the projections of the product and the defining relations $\epsilon_A$ and $\epsilon_B$.)  We have evident injections $A\to A\sqcup B$ and $B\to A\sqcup B$ which are jointly surjective and have disjoint image; we call $A\sqcup B$ the **disjoint union** of $A$ and $B$.

In particular, it follows that $Set$ is a [[pretopos]] (as is any topos).


## Infinity ##

**Axiom 4 (Infinity):** _There exists a set $N$, containing an element $o$, and a function $s:N\to N$ such that $s(n)\neq o$ for any $n\in N$ and $s(n) = s(m)$ only if $n = m$ for any $n, m\in N$._

It is easy to deduce any of the usual consequences of the axiom of infinity.  The set $N$ is not asserted to be minimal, but it is easy to cut it down to be so using separation.  In particular, this axiom implies that $Set$ has a [[natural numbers object]].  We can then proceed to construct the set $\mathbb{Q}$ of rational numbers and the set $\mathbb{R}$ of real numbers in any of the usual ways.

Note also that Axiom 4 implies Axiom 0.

We can however [[natural numbers in SEAR|define sets]] with $n$ elements for each natural number $n$ directly axioms 0, 1, 2 and 3.
 
## Collection ##

The final axiom of SEAR is somewhat trickier to motivate.  It corresponds to the [[axiom of replacement]] (or more precisely collection; see [Wikipedia](http://en.wikipedia.org/wiki/Axiom_schema_of_replacement) until we get around to writing our own article) in $\mathbf{ZFC}$, and the reasons that we need it are the same as the reasons that $\mathbf{ZFC}$ needs it.

Suppose for the sake of argument that there existed a *universal set*, meaning a set containing all other sets.  Now in structural set theory this is meaningless, since no set can contain other sets, but there is an easy fix: we consider instead *indexed families* of sets.  There are multiple ways to make this precise, but here is a very simple one: an $A$-indexed family of sets is simply a relation $M:A\looparrowright X$.  The set indexed by each element $a\in A$ is $M_a = \{x\in X | M(a,x)\}$.  (Often one requires the $M_a$ to be a disjoint decomposition of $X$, so that $M^o$ is a function $X\to A$, but this is unnecessary.  In fact, if $M:A\looparrowright X$ is a general family, then ${|M|} \to A$ is a function that represents a family in this stronger sense which is equivalent to $M$.)

With this definition, a *universal family of sets* would be a set $U$ with a $U$-indexed family of sets $E:U\looparrowright Y$ such that for any set $A$, there exists a unique $u\in U$ and a bijection $A\cong E_u$.  The existence of such a universal set is inconsistent, but the collection axiom can be thought of as the "ghost" of what *would be implied* by Axioms 1 and 2 if a universal set *did* exist.  Let's now unravel that.

If $U$ were a universal set, then any $A$-indexed family $M:A\looparrowright X$ would induce a unique function $f:A\to U$ such that $E_{f(x)} \cong M_x$ for all $x\in A$.  Conversely, any function $f:A\to U$ would induce an $A$-indexed family of sets with this property: just take the composite relation $E \circ f$.  (This family would not be unique, but it would be unique up to a suitable notion of [[equivalence]] between indexed families.)  Thus it is reasonable to consider the "ghost" of a function $f:A\to U$ to be simply an $A$-indexed family of sets.

The ghost of a relation $A\looparrowright U$ is even easier.  By Axiom 1, to give such a relation would be equivalent to describing a property $P$ that can obtain of an element of $A$ and a set.  Thus, the ghost of a relation $A\looparrowright U$ is simply such a property.

If $U$ existed, Axiom 2 would imply that any relation $A\looparrowright U$ had a tabulation consisting of a set $B$ and functions $p:B\to A$ and $q:B\to U$.  We now kill $U$ and inspect the ghostly remnants of this tabulation.

**Axiom 5 (Collection):** _For any set $A$ and any property $P$ which can obtain of an element of $A$ and a set, there exists a set $B$, function $p:B\to A$, and a $B$-indexed family of sets $M:B\looparrowright Y$ such that (1) $P(p(b),M_b)$ holds for any $b\in B$, and (2) for any $a\in A$, if there exists a set $X$ with $P(a,X)$, then $a\in im(p)$._

What this axiom asserts is actually a bit weaker than the precise ghost of a tabulation of $P$; that would require instead of (2) that for any $a\in A$ and any set $X$ with $P(a,X)$, there exists a $b\in B$ with $p(b)=a$ and $M_b\cong X$.  However, this stronger statement is still inconsistent, because if we took $A=1$ and $P=\top$ it would resurrect $U$ in the form of $B$!  The form given above is weak enough to keep the dead in their graves, yet strong enough to be useful (though we will not go into its uses here).

+--{: .query}
_AN_: "weak enough to keep the dead in their graves" - another piece of wishful thinking,
unless you give a proof of this highly nontrivial statement.

_Toby_:  Assuming the consistency of $\mathbf{ZFC}$, this follows from the equiconsistency of $\mathbf{SEAR}$ and $\mathbf{ZF}$.  (Of course, that has not been done in detail, so you can doubt it if you like.)

AN: yes, I doubt that. It has not even been outlined.

[[Mike Shulman]]: Moreover, it doesn't really need the full equiconsistency; it only needs the easier direction that $Con(ZF)\Rightarrow Con(SEAR)$.

AN: I think you'd put this piece of information into the main text. 

Mike Shulman continues:
This direction is sketched below, and I think anyone should be able to fill in the details.

AN: Regarding this axiom, I find there no sketch, but only the nearly empty statement "The least obvious SEAR axiom is Collection, whose proof requires the axiom of replacement in ZF." In fact, giving the details of this derivation here (instead of later) would seem to me a better justification than the ghost justification below,
as it would provide intuition in its validity. 
(Then there is no question at all about ghosts.)

_Toby_:  I\'m sure that it can\'t be proved by the others, which have a model in $V_{\omega + \omega}$ (the universe of well-founded pure sets of hereditary rank less than $\omega + \omega$), the same as provides a model for $\mathbf{ZC}$ (which is $\mathbf{ZFC}$ with unbounded Separation but without Replacement/Collection).

I would like to see detailed proofs, if Mike has written them up.  I have not yet completely convinced myself that Collection is properly formulated (although I\'m certain that it could be fixed if necessary by writing it in a more function-theoretic way, since I know how to do that myself).

[[Mike Shulman]]: I've added some more detail below regarding the proof of the SEAR Collection axiom from ZF.  When I have time I will add more about the other direction as well, for which I do have something written down (sort of), but in different terminology than is used at [[pure set]].
=--


_Exercise: why is adherence to "speak no evil" necessary for Axiom 5 to be reasonable as stated?_

+--{: .query}
[[Arnold Neumaier]]: The concept of a ghost of an inconsistent assumption employed to motivate Collection is not really useful, since the inconsistency axiom 0=1 is also such a ghost.

[[Mike Shulman]]: 
I really don't see what 0=1 being a consequence of an inconsistent assumption has to do with using other, less stupid, consequences of such an assumption to motivate a (believed to be) non-inconsistent axiom.  The point is, you (or someone else) *might want* axiom X.  Unfortunately, axiom X is inconsistent.  But *why* would you want axiom X?  Not to prove 0=1, certainly!  Your goal in introducing axiom X was to prove something else that is a "more direct" consequence of axiom X than 0=1 is (or, at least, a consequence of it along a different path).  So it makes sense to try to modify axiom X to make it consistent, yet maintain its direct connection to what you wanted it for.  Of course, none of that has any precise meaning, but it's *motivation*, so it doesn't need to.

AN: I had meant to convey that a better motivation is needed. Why not demonstrate that it is needed to achieve some useful purpose?

[[Mike Shulman]]: Yes, demonstrating its uses is a good thing too!  My favorite structural application of collection is to construct sets recursively; I'll write a bit about that when I get a chance.

AN: For example, I'd like to understand its role in the 
proof that SEAR and ZF are logically equivalent. 
For if it is not needed there, it seems (though I am not completely sure if this is a cogent conclusion) that one should be able to prove the axiom from the others.

[[Mike Shulman]]: If $Con(SEAR-Collection)\Rightarrow Con(ZF)$ but $Con(ZF)\Rightarrow Con(SEAR)$, then it would of course follow that $Con(SEAR-Collection)\Rightarrow Con(SEAR)$.  But it wouldn't necessarily be true that Collection itself, rather than merely its consistency, follows from the other axioms.

Regardless, there is no hope of $Con(SEAR-Collection)\Rightarrow Con(ZF)$, since as Toby says $V_{\omega+\omega}$ (or more generally any model of Zermelo set theory) models $SEAR-Collection$, but is strictly weaker than $ZF$.
=--


# Variants and Comparisons #

## The Axiom of Choice ##

We obtain a theory called **SEAR-C** (SEAR with Choice) by adding the following axiom:

**Axiom 6 (Choice):** _If $\varphi:A\looparrowright B$ is a relation such that for any $a\in A$, there exists a $b\in B$ with $\varphi(a,b)$, then there exists a function $f:A\to B$ with $\varphi(a,f(a))$ for all $a\in A$._

This is easily seen to be equivalent to asserting that all surjections are [[split epimorphism|split]] in $Set$, which is a more common categorical form of the [[axiom of choice]].

## Constructive SEAR ##

Axioms 1-5 of SEAR make perfect sense whether the ambient logic is [[classical logic|classical]] or [[intuitionistic logic|constructive]].  By Diaconescu's argument, Choice implies the logic is classical.

To obtain a [[predicative mathematics|predicative]] theory, Axiom 3 can be replaced by an appropriate weaker axiom, such as the existence of [[disjoint union]]s, [[quotient set]]s, and/or [[function sets]], or a structural version of the axiom of [[subset collection]].

## Bounded SEAR and ETCS ##

By **bounded SEAR** we mean the subtheory consisting of axioms 2-4 of SEAR plus

**Axiom 1B (Bounded relational comprehension):** _The same as Axiom 1, but the property $P$ must be bounded (it can only involve quantifiers over elements, not sets or relations)._

All the theorems cited above remain true with Axiom 1 replaced by Axiom 1B, so bounded SEAR still implies that $Set$ is a well-pointed topos with a NNO.  Therefore, *bounded SEAR-C* implies [[ETCS]].  Conversely, it is not hard to show that given any [[well-pointed topos]], if we interpret "set" as "object of the topos", "element of $A$" as "[[global element]] $1\to A$", and "relation $A\looparrowright B$" as "[[subobject]] of $A\times B$," then Axioms 0, 1B, 2, and 3 are satisfied.  It follows that ETCS also implies bounded SEAR-C, so the two are equivalent.

ETCS can also be augmented with additional axioms to make it equivalent to full SEAR-C, but that is beyond our scope at the moment.

## SEAR and ZF ##

It is fairly straightforward to construct a model of SEAR from a model of ZF.  Given a model of ZF, we define the SEAR-sets to be the ZF-sets, and the SEAR-elements of $A$ to be the ZF-elements of $A$.  If we prefer, we can take the SEAR-elements of $A$ to be pairs $(x,A)$ where $x\in_{ZF} A$, so that the elements of distinct sets will be disjoint---but this is not necessary, since in SEAR the question of whether two distinct sets have elements in common is not even well-posed.  Finally, we of course take the SEAR-relations $A\looparrowright B$ to be the ZF-subsets of $A\times B$, and we let $\varphi(x,y)$ hold in SEAR iff $(x,y)\in_{ZF} \varphi$.  It is then easy to prove Axioms 0, 1, 2, 3, and 4 from the axioms of ZF, and likewise Axiom 6 follows easily from the axiom of choice in ZFC.  (In fact, Z and ZC, where the replacement axiom is omitted, suffice for these conclusions.)  The only axiom which requires some thought is Collection, and it is here that we use replacement.

+-- {: .num_theorem #zf-coll}
###### Theorem
The sets, elements, and relations in a model of ZF satisfy the Collection axiom of SEAR.
=--
+--{: .proof}
###### Proof
Let $A$ be a set and $P$ a property as in Axiom 5.  As given, $P$ is a first-order statement in the language of SEAR, but we can easily translate it into a statement in the language of ZF; from now on we work in ZF.  Define
$$A' = \{a\in A | \exists X. P(a,X)\}.$$
By the [[axiom of foundation]], for each $a\in A'$ there exists an [[ordinal]] $\lambda$ and an $X\in V_{\lambda}$ such that $P(a,X)$; let $\lambda_a$ be the *smallest* such $\lambda$.  Then $a\mapsto V_{\lambda_a}$ is a class function, so by the axiom of replacement, the set $\{V_{\lambda_a} | a\in A'\}$ exists.  Let $Y$ be the union of this set.  Define
$$B = \{ (a,X)\in A\times Y | P(a,X)\},$$
let $p:B\to A$ be the projection onto the first factor, and let $M:B\looparrowright Y$ be defined by
$$M((a,X),x) \Leftrightarrow x\in X.$$
Then $M_{(a,X)} = X$, since each $V_\lambda$ is a transitive set, so $P((a,X), M_{(a,X)})$ holds for any $(a,X)\in B$.  Finally, by construction, if there exists $X$ with $P(a,X)$ then $a\in im(p)$; thus the SEAR axiom of collection is satisfied.
=--

Note the use of the axiom of foundation in addition to the axiom of replacement.  This can be avoided if we use instead the ZF version of the [axiom of collection](http://en.wikipedia.org/wiki/Axiom_of_collection#Axiom_schema_of_collection), which is equivalent to the axiom of replacement over the other ZF axioms (including foundation), by an argument like that above.

Conversely, from any model of SEAR one can *construct* a model of ZF, by taking the sets in ZF to be the "internal well-founded extensional relations."  The basic idea of this process is described at [[pure set]]; more details remain to be filled in.


+--{: .query}
[[Arnold Neumaier]]: See the remarks on this in the initial discussion box.

=--

Thus, SEAR and SEAR-C are at least equiconsistent with ZF and ZFC, respectively. In fact, SEAR-C and ZFC are equivalent, in the sense that passage back and forth in either direction yields an equivalent model.  However, passage from SEAR to ZF and back again can lose information, if there are sets in the model of SEAR which do not admit any well-founded extensional relation (this doesn't happen in the presence of choice, since then every set can be well-ordered).

## Type theory and internalization

Every topos has an [[internal logic]], which is a [[type theory]].  However, the line between type theory and structural set theory is fine and sometimes hard to see; the main difference is that structural set theory can involve quantifiers over sets (= types), while type theory only allows ("bounded") quantifiers over elements of types.  Through this correspondence, *Intuitionistic Bounded SEAR* can be treated as a type theory and interpreted internally in any topos with a NNO.  Of course, if the topos is [[boolean topos|boolean]], then the logic can be classical.

One can also write down stronger axioms on a topos such that if they are satisfied, then full Intuitionistic SEAR can be interpreted "internally" in that topos, extending the usual internal logic.


# Making alternate primitive choices #

## SEPS: Using pairs and subsets instead of relations

+-- {: .query}
This looks nice, and I think that it probably matches pretty closely the way that I usually think when reading ordinary mathematics.  I haven\'t read it very carefully yet, so take this with a grain of salt, but I think that it would be even more user-friendly to use sets, elements, and *subsets* (rather than binary relations) as the basic concepts.  Presumably you have to throw in ordered pairs too, but I think that this matches 'ordinary' language *very* closely.  ---Toby

_Mike_: Yes, you're right, and I did think of something like that.  However, I haven't managed to find a good way to "throw in ordered pairs."  I'd like an axiom like "for any sets $A$ and $B$, there exists a set $A\times B$ such that ..." but what comes after "such that?"  With only sets, elements, and subsets as the other data, there's no way to relate the elements of $A\times B$ to the elements of $A$ and $B$.

I guess one possible approach would be to make the construction of products an *operation*, rather than an existential axiom.  Then for every pair of sets $A$ and $B$ there would be a *specified* set $A\times B$, and for every pair of elements $x\in A$ and $y\in B$ there would be a *specified* element $(x,y)\in A\times B$, with an axiom asserting that every element of $A\times B$ is of the form $(x,y)$ for a unique $x$ and $y$.  I suppose we do tend to think more in terms like that, but it's less aesthetically pleasing to me because it's not really "structural" to specify a particular $A\times B$.  So now I'm undecided.

_Toby_:  I don\'t see what\'s unstructural about that!  Although I think that we\'ve had this conversation before ....

[[Mike Shulman]]: It feels unstructural because the element $(x,y)$ is no longer internally featureless; it has the intrinsic property of being the pair of $x$ and $y$.  I see "structural" as meaning that, among other things, isomorphic objects are indistinguishable; but with that approach, the selected product $A\times B$ is distinguishable from any other product.  (Additionally, in some metatheories it requires choice to get from one to the other.)

I also feel that maybe viewing relations $A\looparrowright B$ as subsets of $A\times B$ is merely a habit ingrained in us by material set theory over the course of the 20th century, and thus something that structural set theory should try to wean us from.

_Toby_:  I don\'t see how you would distinguish $A \times B$ from any other isomorphic object if you have no way to express that it equals *the* $A \times B$ in question.  More generally, strucuturalism to me isn\'t about using existential quantifiers all the time instead of operations.  In fact, I don\'t see how this is any different from your set $|\varphi|$.  (Possibly I should write SESAP out in full to make sure it does all work the same way.)  And the metatheories that think that they require choice to get an operation out of an existential statement have formalised things wrong; they should be using meta-anafunctors between the (syntactic or model) meta-categories.

I also don\'t see what\'s material about conflating $A \looparrowright B$ with $\mathcal{P}(A \times B)$.  It\'s no different, really, from making $A \to B$ a part of $A \looparrowright B$.  Personally, I *prefer* to take sets and functions as the basic concepts; I saw $\mathbf{SEAR}$ as an attempt to make a structural theory that looks more like the na&#239;ve set theory that mathematicians use (but perhaps I misjudged the idea), and I think that making unary relations basic will be even more like that.  Really, any of these concepts (function, binary relation, unary relation) have a good claim for being a basic concept that should be axiomatised directly, rather than defined in terms of one of the others, and it\'s a fairly arbitrary choice which one we use.

[[David Roberts]]: ...it makes sense to me that we probe the interior of a set by how it relates to other sets, and that we find out about the elements of a set by how it relates to the one-point set. But the aim seems to be useability by everyday mathematicians. That being said, this material seems easier to learn as a first approach to foundations (for undergraduates/early postgrads) than ZF or NBG, requiring less cruft to get to proving theorems.


[[Mike Shulman]]: You're right that the given $A\times B$ couldn't be distinguished *in the theory itself* from any other product, but I think it would still clearly have a special status.  Also, it is definitely different from $|\varphi|$.   The tabulation axiom is a purely existential statement; it could be viewed as an "operation" from relations to tabulations, but nothing forces you to view it this way.  (And you can only avoid meta-choice by calling such an operation an anafunctor once you've *proven*, in the theory, that tabulations are unique up to unique isomorphism.)  By contrast, the product axiom would be irreducibly an operation; you can't (at least, I don't see how to) make it purely existential, because it is the *only* part of the theory that relates elements of different sets.  The product can only be characterized uniquely using "projection" functions, but in order to have functions you need relations, hence you need products....

My original idea with SEAR was merely to give a proof-of-concept that structural set theory can be formalized with elements and without functions or categories.  But it does turn out looking much more like the set theory that mathematicians actually use, and making it even more so would definitely be a plus to getting structural set theory adopted more widely, which I'm all about.  Moreover, David's comment about it being easier to learn as a first approach to foundations is also an interesting point that I hadn't really thought about, and for that purpose subsets and pairs might also be better.  And I do admit that the tabulation axiom looks a little cumbersome; breaking it down into pairing and separation does feel cleaner.

It also makes it look much more like type theory!  Which I suppose is not a bad thing.  Bounded SESAP will basically *be* the internal type theoretic language of a topos with NNO, and that's actually a really *good* thing; it will make internal logic feel more natural to anyone who is familiar with structural-set-theory foundations.

I went ahead and had a go at a formalization using products down at the bottom of the page.  I have to say that "SESAP" doesn't ring as well.  (-:  But I think we could still call it SEAR even if the "relations" aren't quite a fundamental concept.  (Although if someone has a better name to suggest, I'm still listening.)  Actually, we could probably use the same name for all the different formalizations, explicitly allowing people the choice of whether to take functions or binary-relations or subsets+products as primary.  Everyone says "ZF" despite variations in the phrasing of the axioms, so the name of a theory doesn't have to be rigidly tied to a specific way of stating it.

_Toby_:  I was going to call my version 'SEAPS' until I realised that the 'A' was in the wrong place ...

[[David Roberts]]: How about SER and SEPS? And then SER-C and SEPS-C.

[[Mike Shulman]]: I like SEAR better than SER, but SEPS isn't too bad.  Although I'd also still rather not make a big deal about the difference between the two.
=--

An alternate formulation of the theory, suggested by Toby, has four primitive notions: sets, elements, subsets, and a pairing operation.  Sets and elements are as before.  A *subset* is, like an element, attached to a certain set; it is always a subset *of* some set.  Thus we have a typing declaration $S\subseteq A$.  We also have a primitive notion of when an element $x\in A$ *belongs to* a subset $S\subseteq A$; thus now we have $x\in S$ as a possible assertion of the theory (analogous to $R(x,y)$ before).  We allow a typed equality predicate for subsets.  Finally, there is an operation which assigns to every pair of sets $A$ and $B$ a set $A\times B$, and to every pair of elements $x\in A$ and $y\in B$ an element $(x,y)\in A\times B$.

**Axiom 0** is the same as before.

**Axiom $\frac{1}{2}$ (Pairing):** _For every pair of sets $A$ and $B$ and every element $z\in A\times B$, there exists a unique pair of elements $x\in A$ and $y\in B$ such that $z=(x,y)$._

**Axiom $1\frac{1}{2}$ (Subset comprehension):** _For every property $P$ that can obtain of elements $x$ of some set $A$, there exists a unique subset $S\subseteq A$ such that $x\in S$ precisely when $P$ obtains of $x$_

We now define a **relation** $A\looparrowright B$ to be a subset of $A\times B$.  With this definition, Axiom $1\frac{1}{2}$ clearly implies Axiom 1 (relational comprehension).  We define **functions** and their properties as before.  Axiom $\frac{1}{2}$ implies that there are projection functions $A\times B\to A$ and $A\times B\to B$ which make $A\times B$ into a product in $Set$.

**Axiom $2\frac{1}{2}$ (Separation):** _For every set $A$ and every subset $S\subseteq A$, there exists a set $|S|$ and an injective function $i:{|S|}\to A$ such that for any $x\in A$, we have $x\in S$ if and only if there is a $z\in {|S|}$ with $i(z)=x$._

Applying separation to subsets of $A\times B$ and composing $i$ with the product projections, we recover Axiom 2 (tabulations).  We can now go on with the subsequent axioms stated in the same way as before.


## Eliminating equality

As stated SEAR includes a fundamental "equality" relation on elements of a given set.  However, we can also make equality into *structure*.  This is definitely not along the "more accessible to undergraduates" direction!  But it may sometimes be technically helpful.

Consider a theory of *pre-sets*, *elements*, and *pre-relations* as in SEAR, with "pre-sets" replacing sets, except that there is no given equality relation on *anything*.  Axiom 0 requires no modification. In Axiom 1, we reinterpret the "uniqueness" clause as a *definition* of what it means for two parallel pre-relations to be equal, i.e. $\varphi=\psi$ if $\varphi(x,y)\Leftrightarrow\psi(x,y)$ for all $x$ and $y$ in the source and target of $\varphi$ and $\psi$.

Before stating the version of Axiom 2 we need some definitions.  We define a **set** to be a preset $A$ equipped with an [[equivalence relation|equivalence pre-relation]] $=_A$.  A **relation** between sets $(A,{=_A})$ and $(B,{=_B})$ is a pre-relation $\varphi:A\looparrowright B$ which is *extensional* in the sense that if $\varphi(x,y)$, $x'=_A x$, and $y'=_B y$, then $\varphi(x',y')$.  Finally, a **function** $f:(A,{=_A}) \to (B,{=_B})$ is a relation which is (a) *total:* for any $x\in A$, there is a $y\in B$ with $f(x,y)$, and (b) *functional:* if $f(x,y)$ and $f(x',y')$ and $y=_B y'$, then $x=_A x'$.

Now Axiom 2 reads: for any sets $(A,{=_A})$ and $(B,{=_B})$ and any relation $\varphi:(A,{=_A})\looparrowright (B,{=_B})$, there exists a set $({|\varphi|},{=_{|\varphi|}})$ and functions $p:{|\varphi|}\to A$ and $q:{|\varphi|}\to B$ such that: (1) for any $x\in A$ and $y\in B$, we have $\varphi(x,y)$ if and only if there exists $r\in {|\varphi|}$ with $p(r,x)$ and $q(r,y)$, and (2) for any $r\in {|\varphi|}$ and $s\in{|\varphi|}$, if $p(r)=_A p(s)$ and $q(r)=_B q(s)$, then $r=_{|\varphi|}s$.  Note that it is sufficient to assert merely that $|\varphi|$ is a pre-set and $p$ and $q$ are total relations satisfying (1), since (2) can then be used to define $=_{|\varphi|}$ in such a way as to make it a set and $p$ and $q$ functions.

The construction of $\emptyset$ is just as in ordinary SEAR.  The construction of $1$ in ordinary SEAR used equality, but we now have a simple replacement for it: let $1$ be any pre-set containing an element, equipped with the equivalence relation such that $x=y$ always for any $x,y\in 1$.  Similarly, in this variant we can construct quotient sets without needing powersets; we simply enlarge the equivalence relation on the underlying pre-set of a set.

Of course, if $(A,{=_A})$ is a set, a **subset** of $A$ is a relation $1\looparrowright (A,{=_A})$.  Axiom 3 can now be translated as-is, or it can be simplified to assert merely the existence of a pre-set $P A$ such that any subset of $A$ is represented by some element of $P A$, with the uniqueness clause turned into a definition of $=_{P A}$.
The same idea applies to all the other axioms.


# Universes in SEAR

+--{: .query}
[[David Roberts]]: Can we talk about Grothendieck universes or analogous size-related mechanisms? (this is a naive question, since there may be (no need for/obvious way to do) this in a structural set theory that I am unaware of.

[[Mike Shulman]]: Universes can be defined in any structural set theory in a fairly straightforward way, modulo the usual translation from "set of sets" to "family of sets."  There is some stuff from a more ETCS-like perspective at [[universe in a topos]]; I'm sure that this can be rephrased in SEAR (if you want to take a shot, feel free!).

[[David Roberts]]: I'd certainly like to, subject to real-world time constraints. It seems to me that something could be done to the axiom of collection if we had a axiom of universes (for every set there is a universe acting as a universal family for it, or similar).

[[Mike Shulman]]: I'm not sure that Collection can really be eliminated using universes, but maybe it can.
=--

## Using families

+--{: .query}
[[David Roberts]]: Some sketchy thoughts - a universe will be a relation $U \looparrowright E$ satisfying axioms analogous to those at [[universe in a topos]]. There are few points that need translating into SEAR-language first so we can define smallness of a family of sets $I \looparrowright A$

* Pullback - unless I am mistaken, the appropriate version is this: Given a function $I \to U$, the family $I \looparrowright E$ should be regarded as the \'pullback\' family. This family should be isomorphic to the family $I \looparrowright A$. This leads us to wonder how to define two families to be isomorphic.

* Dependent product - this is tricker and I'm not going to do that right now. 
=--

Fix a family of sets $U \looparrowright E$.

**Definition:** A family $a:I \looparrowright A$ is called _$U$-small_ if there is a function $f:I \to U$ such that for the composite relation $I \looparrowright E$ ...

A set $A$ is called $U$-small if the relation $\mathbf{1}\looparrowright A$, which holds of $*$ and $a$ for all elements $a$ of $A$, is a $U$-small family.

For ease of language, we define a composite of families to be the composite relation of the two relations defining the families.

**Definition:** A family of sets $U \looparrowright E$ is called a _universe_ if the following axioms are satisfied:

  * The composite of two $U$-small families is $U$-small
  * The relation $f^o:B\looparrowright A$ opposite to an injective function $f:A \to B$ is a $U$-small family
  * $P\mathbf{1}$ is a $U$-small set
  * (Something about dependent products, once these are defined)

There is an optional axiom, given the axiom of infinity from before:

  * The [[natural numbers object]] is a $U$-small set

Without this axiom we do not have that universes contain infinite sets.
  
Given a universe $U \looparrowright E$, we want to define a (meta-)category $U-Set$...


## Using mere sets

+--{: .query}
[[Mike Shulman]]: The main idea of SEAR is that in a well-pointed topos, global elements suffice for everything.  In particular, we can usually dispense with families of things and consider only single ones.  So here's a formulation that I think is more in the spirit of SEAR.
=--

Given a family $E:U\looparrowright X$, recall that for $u\in U$ we let $E_u$ be a tabulation of $\{x\in X | E(u,x) \}\subseteq X$.  We say that a set $A$ is **$U$-small** (although really, it would be more appropriate to say "$E$-small") if there exists a $u\in U$ with $A\cong E_u$.  Now we say that $U$ (equipped with $E$) is a **universe** if it satisfies:

* There exists an inhabited $U$-small set.
* The tabulation of any relation between two $U$-small sets is $U$-small.
* If $A$ is $U$-small, then so is $P A$.
* (Replacement) If $f:A\to B$ is a function such that $B$ is $U$-small and for each $b\in B$, the set $f^{-1}(b)$ is $U$-small, then $A$ is $U$-small.
* (Collection) If $p:B\twoheadrightarrow A$ is a surjective function where $A$ is $U$-small, then there exists a $U$-small set $C$, a surjection $q:C\twoheadrightarrow A$ and a function $f:C\to B$ such that $q = p\circ f$.

The optional axiom is the same:

* There exists an infinite $U$-small set (in the sense of Axiom 4).

The first two properties of a universe clearly imply that the $U$-small sets satisfy Axioms 0--2 of SEAR all by themselves.  In particular, $\emptyset$ and $1$ are $U$-small, any subset of a $U$-small set is $U$-small, and if $A$ and $B$ are small then so is $A\times B$.  Thus from the additional assumption of the smallness of powersets, we can conclude that if $A$ and $B$ are small, so is the set $B^A$ of functions from $A$ to $B$.  It also follows that coproducts and quotient sets preserve smallness.  (For a notion of "predicative universe" we would replace the smallness of powersets with the smallness of function sets, and we might have to separately assume smallness of coproducts and quotients, I'm not sure.)

In order to show that the $U$-small sets model SEAR all by themselves, it remains to show:

+-- {: .num_theorem #univ-coll}
###### Theorem
The $U$-small sets for a universe $U$ satisfy the Collection axiom of SEAR.
=--
+--{: .proof}
###### Proof
Let $A$ be a $U$-small set and $P$ a property as in the Collection axiom.  Let $P'$ be a property such that $P'(a,X)$ holds iff $P(a,X)$ holds *and* $X$ is $U$-small.  By the Collection axiom for all sets applied to $P'$, there exists a set $B$, a function $p:B\to A$, and a $B$-indexed family of sets $M:B\looparrowright Y$ satisfying the desired properties: (1) for any $b\in B$, we have $P(p(b),M_b)$ *and* $M_b$ is $U$-small, and (2) for any $a\in A$, if there exists a $U$-small set $X$ with $P(a,X)$, then $a\in im(p)$.  Our goal is to replace $B$ and $Y$ by $U$-small sets $B'$ and $Y'$ with a relation $M':B'\looparrowright Y'$ maintaining the truth of these statements.

Now the induced function $\overline{p}:B\to im(p)$ is surjective, and since $im(p)$ is a subset of $A$ it is $U$-small.  Thus, by the "Collection" property of a universe, there exists a $U$-small set $C$, a surjection $q:C\twoheadrightarrow im(p)$ and a function $f:C\to B$ such that $q = \overline{p} \circ f$.  We take $B'=C$ and the composite $C \to im(p)\to A$ as the function $p'$; we claim that the composite relation $M\circ f$ still satisfies (1) and (2) above.  (We have not replaced $Y$ yet, so this is still an intermediate step.)  Property (1) follows since $p'(c) = p(f(c))$ and $(M\circ f)_c \cong M_{f(c)}$, while property (2) follows since $im(p) = im(p')$ by construction.

Now consider a tabulation $B' \overset{r}{\leftarrow} Z \overset{s}{\to} Y$ of $M\circ f$.  Note that for any $b\in B'$ we have $r^{-1}(b) \cong (M\circ f)_b$, and therefore in particular $r^{-1}(b)$ is $U$-small by (1).  Since $B'$ is also $U$-small, the "Replacement" property of a universe implies that $Z$ is also $U$-small.  But the family $r^o:B'\looparrowright Z$ is equivalent to $M\circ f$, in the sense that $(r^o)_b \cong (M\circ f)_b$ for all $b\in B'$, so it also satisfies (1) and (2); thus we can take $Y'=Z$ and $M'=r^o$.
=--

Note that both the "Replacement" and "Collection" properties of a universe are required to show the SEAR Collection axiom for $U$-small sets.  The naming of these two properties appears to be traditional, however.  See in particular the book _Algebraic Set Theory_ by Joyal and Moerdijk.

What about families and dependent products?  We define a function, considered as a family of sets, to be **$U$-small** if each of its fibers is.  Note that then we can state the Replacement property as "the composite of $U$-small functions is $U$-small."  Now for functions $g:C\to B$ and $f:B\to A$, the fiber of the dependent product $\Pi_f g$ over $a\in A$ is the subset of the function set $\Big((f g)^{-1}(a)\Big)^{f^{-1}(a)}$ consisting of functions $s: f^{-1}(a) \to (f g)^{-1}(a)$ such that $g\circ s = \id$.  Thus, if $f$ and $g$ are $U$-small, so is $f g$ (by the "Replacement" property), and thus so is this fiber.  Hence $U$-small functions are closed under dependent products.

Also of interest is the following, which should be compared to the "descent" axiom in Joyal-Moerdijk.

+-- {: .num_theorem #univ-descent}
###### Theorem
The following are equivalent for a function $f:B\to A$.
1. $f$ is $U$-small.
1. There exist a surjection $p:C\to A$ and a function $g:C\to U$ and two pullback squares
$$\array{B &\overset{q}{\leftarrow} & P & \overset{k}{\to} & {|E|}\\
  ^f\downarrow && \downarrow^j && \downarrow\\
  A &\underset{p}{\twoheadleftarrow} & C & \underset{g}{\to} & U}$$
1. (If the axiom of choice holds) There exists a function $g:A\to U$ and a pullback square
$$\array{B & \overset{}{\to} & {|E|}\\
  ^f\downarrow && \downarrow\\
  A & \underset{g}{\to} & U}$$
=--
+--{: .proof}
###### Proof
Clearly the third condition implies the second.  The second implies the first, since pullbacks have isomorphic fibers.  And in the presence of AC, the second implies the third, since the surjection $p$ has a section.  Thus the difficulty is in showing that the first implies the second.

Suppose that $f:B\to A$ is $U$-small.  This means that for any $a\in A$, there exists a $u\in U$ and a bijection $f^{-1}(a)\cong E_u$.  Let $C$ be the subset of $A\times U\times P(B\times |E|)$ consisting of those triples $(a,u,h)$ such that $h$ is a bijection $f^{-1}(a) \overset{\cong}{\to} E_{u}$, and let $p:C\to A$ and $g:C\to U$ be the projections.  Since $f$ is $U$-small, $p$ is surjective.  Define $P$ to be a pullback of $f$ along $p$, with projections $q:P\to B$ and $j:P\to C$, and define $k:P\to {|E|}$ by (informally speaking) $k(x) = h(q(x))$ where $j(x) = (a,u,h)$.  Since each $h$ is a bijection, $k$ makes $P$ a pullback of ${|E|}$.
=--