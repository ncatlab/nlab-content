* table of contents
{:toc}

# Idea

A **structural set theory** is a [[set theory]] which describes structural mathematics.  As conceived by the structuralist, mathematics is the study of structures whose form is independent of the particular attributes of the things that make them up.  For instance, in [[ZF]] set theory, "the natural numbers" can be defined as the von Neumann ordinals $\emptyset, \{\emptyset\}, \{\emptyset, \{\emptyset\}\}, \dots$ or alternately as $\emptyset, \{\emptyset\}, \{\{\emptyset\}\}, \dots$, but either definition has all the necessary properties (namely, the properties making it a [[natural numbers object]] in [[Set|the category of sets]]).  The structuralist says, essentially, that the number "$3$" should denote "the third place in a natural numbers object" rather than some particular set such as $\{\emptyset, \{\emptyset\}, \{\emptyset, \{\emptyset\}\}\}$ as it does in any definition of "the natural numbers" in ZF.

*Structural set theory* provides a foundation for mathematics which is free of this "superfluous baggage" attendant on theories such as ZF, in which there is lots of information such as whether or not $3\in 17$ which is never used in mathematics.  In a structural set theory, the elements (such as $3$) of a set (such as $\mathbb{N}$) *have* no identity apart from their existence as elements of that set, and whatever structure is given to that set by the functions and relations placed upon it.  That is, sets (together with other attendant concepts such as [[element]]s, [[functions]], and [[relations]]) are the "raw material" from which mathematical structures are built.

Thus, somewhat paradoxically, it turns out that one of the primary attributes of a structural set theory is that the *elements* of a set have *no* "internal" structure; they are only given structure by means of functions and relations.  In particular, they are not themselves sets, and by default cannot be elements of any other set, so that elements of different sets cannot be compared (unless and until extra structure is imposed).  Structural set theory thus looks very much like [[type theory]].  We contrast it with [[material set theory|material set theories]] such as ZF, in which the elements of sets can have internal structure, and are often themselves sets.

Among category theorists, it's popular to state the axioms of a structural set theory by specifying elementary properties of [[Set|the category of sets]]; the orthodoxy here (to the extent that there is one) is probably Bill Lawvere's [[ETCS]].  It is weaker than ZFC and must be supplemented to handle some esoteric parts of modern mathematics, although it suffices for most everyday uses.  Another structural set theory, which is stronger than ETCS and less closely tied to category theory, is [[SEAR]].


# Semiformal Definition

The following is an attempted formal definition of when a set theory is structural.  It should be regarded as extremely tentative.

## Notions of set

First of all, in order to give a definition pertaining to all set theories, we need to know: what is a set theory?  Probably no theory can *intrinsically* be called a set theory; it is only given that distinction by our intent to regard some of its objects of study as "sets" and others as their "elements."  Thus we make the following definition.

+-- {: .un_defn}
###### Definition
A **notion of set** in a typed first-order theory consists of:

* A type $\mathbb{S}$ called the *type of potential sets*.
* A unary predicate $set(-)$ on $\mathbb{S}$ called *being a set*.
* A type $\mathbb{E}_A$, possibly depending on $A\in\mathbb{S}$, called the *type of potential elements of $A$*.
* A unary predicate $in_A(-)$ on $\mathbb{E}_A$ called *being an element of $A$*.
=--

We have split the notions of sethood and elementhood into both a type and a predicate to allow for variation in theories which model them by one or the other method or a combination.  Here are some examples.

* [[ZF]] is a one-typed theory; we call the objects in the one type  "ZF-sets" for clarity.  The type of ZF-sets is the type of potential sets, and we take the predicate $set(-)$ to be $\top$ (every potential set is a set).  For such a set $A$, the type of potential elements of $A$ must once again be the type of ZF-sets, and the elementhood predicate is simply $in_A(x) \equiv (x\in A)$.

* ZF can be augmented by the presence of [[urelement|urelements]] or atoms.  One way to represent this is with two types, the type of ZF-sets and the type of ZF-atoms.  Again we take the type of ZF-sets to be the type of potential sets, and the sethood predicate $set(-)$ is $\top$.  The type of potential elements of $A$ is now the sum type (ZF-sets + ZF-atoms), with the membership predicate again being the ordinary membership predicate of $A$.

* Atoms can be added to ZF in another way: we maintain only a single type, say the type of "ZF-objects," but we add a "sethood" predicate which distinguishes the sets from the atoms.  Now the type of potential sets is of course the type of ZF-objects, and the predicate $set(-)$ is the ZF-sethood predicate.

* In [[NBG]] or [[MK]] set-class theory, there are two possible "notions of set": the sets and the classes.  The way to formalize this depends on how the set-class theory is stated.  For instance, one way to state NBG is with a single type of classes, defining a class $A$ to be an NBG-set when $A\in B$ for some class $B$.  In this case the sethood predicate (for the "NBG-set" notion of set) will be $set(A) \equiv (\exists B. A\in B)$.

* In [[SEAR]], which is a dependently typed theory, we take the type of potential sets to be the type of SEAR-sets, with the sethood predicate $set(-)$ being again $\top$.  For each set $A$, of course $\mathbb{E}_A$ is the type of SEAR-elements of $A$.  (In contrast to ZF, these types are now nontrivially dependent on $A$.)  The elementhood predicate is $\top$, since every object in the type of SEAR-elements of $A$ is an element of $A$ by definition (that is, in SEAR elementhood is a typing assertion).

* In the variant of SEAR without primitive equality (and thus also in [[SEAR+?]]), the type of potential sets is the type of "SEAR-sets equipped with an endo-relation" (a [[dependent sum]] type).  The sethood predicate $set(A,R)$ then asserts that $R$ is an equivalence pre-relation, with the other structure as in ordinary SEAR.

* Since [[ETCS]] is an extension of the first-order theory of a [[category]], it can be stated in several ways.

   * If ETCS is stated with two types (objects and arrows), then the type of potential sets is the type of objects (i.e. ETCS-sets) and the sethood predicate is $\top$.  The type of potential elements of each set $A$ is the type of arrows (i.e. ETCS-functions), and $in_A(x)$ holds when the target of $x$ is $A$ and its source is a [[terminal object]].

   * If ETCS is stated with [[single-sorted definition of a category|one type]], then the type of potential sets is that type, the sethood predicate is $set(A) \equiv (A=s(A))$, the type of potential elements is of course again the single type, and the elementhood predicate is as in the two-typed version.

   * If ETCS is stated with dependent types (a type $hom(A,B)$ for every pair of objects $A$ and $B$), then the type of potential sets is the type of objects, the sethood predicate is $\top$, the type of potential elements of $A$ is $hom(1,A)$, and the elementhood predicate is $\top$.

## Structural Presentation

Now we make the following definition.

+-- {: .un_defn}
###### Definition
A notion of set in a typed first-order theory is called **structurally presented** if for any first-order formula $\varphi$ containing free variables $A:\mathbb{S}$ and $x:\mathbb{E}_A$ (and possibly others), if the only free occurrances of $A$ in $\varphi$ is in the (possibly) dependent type $\mathbb{E}_A$ of the variable $x$, then
$$(\forall \vec{z})(\forall A:\mathbb{S})(\forall x,y:\mathbb{E}_A) \Big(in_A(x) \wedge in_A(y) \Rightarrow \big(\varphi \Leftrightarrow \varphi[y/x]\big)\Big) \qquad (\star)$$
holds (where $\vec{z}$ denotes all the other free variables of $\varphi$).
=--

Equation $(\star)$ says that all elements of any set $A$ are completely indistinguishable by the formula $\varphi$.  This is intended to approximate the idea of a structural set theory: the elements of $A$ have no independent structure (and thus cannot be distinguished from each other) apart from their identity as elements of $A$.  Of course, we can't do mathematics without some way to distinguish the elements of a set, but the idea of structural set theory is that this happens only through external structure imposed *on* the set, such as functions and relations, rather than through intrinsic properties of the elements themselves.  This is the idea behind the restrictions placed on $\varphi$.

Before we go on, let's first see that ZF is definitely *not* structurally presented.  Let $A=\{\emptyset, \{\emptyset\}\}$ be the von Nemuann numeral $2$, and let $\varphi \equiv (x = \emptyset)$.  Clearly there are some $x\in A$ such that $\varphi$ holds and others such that it fails, so $(\star)$ is false.  Moreover, $\varphi$ satisfies the condition: $A$ does not occur in it at all.  For the same reasons, NBG and MK are not structurally presented.

Now, why can't we do the same thing in a structural set theory?  Consider SEAR, and let $A$ be a set containing two distinct elements $a$ and $a'$.  By analogy to what we did in ZF, we'd like to take $\varphi \equiv (x = a)$, but in SEAR this violates the required condition: $a$ must also be an element of $\mathbb{E}_A$, so $A$ appears elsewhere in $\varphi$ than in the type of $x$ (namely, in the type of $a$).  In fact, we can show:

+-- {: .un_theorem}
###### Theorem
SEAR is structurally presented.
=--
+-- {: .proof}
###### Proof
Let $\varphi$ be a formula as in the above definition.  Since it does not contain $A$ free (except in the type of $x$), it cannot contain any variables (free *or* bound) denoting elements of $A$ (other than $x$) or relations whose source or target is $A$.  But the only atomic formulas in the language of SEAR are equalities of set-elements, equalities of relations, and assertions that a relation holds of a pair of set-elements, and SEAR has no term constructors that could produce an element of some other set from an element of $A$.  Thus, the only atomic formula involving $x$ that can appear in $\varphi$ is $x=x$, whose truth is clearly independent of the value of $x$.  It follows that the truth value of $\varphi$ must also be so.
=--

For similar reasons, we have:

+-- {: .un_theorem}
###### Theorem
When ETCS is written with dependent hom-types, it is structurally presented.
=--
+-- {: .proof}
###### Proof
Let $\varphi$ be a formula as above.  Similarly to the case of SEAR, $\varphi$ cannot contain any variables other than $x$ that denote functions whose source or target is $A$.  Since the only term-constructor in ETCS is function composition, the only terms containing $x$ that can occur in $\varphi$ are composites ending in $x:1\to A$ followed by zero or more applications of $id_A$, such as $x$ itself, $x\circ f$, $\id_A\circ x$, $(x\circ g)\circ h$, or $(id_A\circ x)\circ (i\circ j)$.  Note that all of these terms denote functions with target $A$.  Moreover, the only possible terms denoting functions of target $A$ are terms of this sort, or else composites of some number of copies of $id_A$ (and nothing else).

Now the only atomic formulas of ETCS are equality between parallel function terms.  Since the source of a composite involving $x$ cannot be $A$ (otherwise $A$ would have to occur as the source of the first function-variable in that composite), the only possible such formulas involving $x$ will be equality between two composites containing $x$.  But since $1$ is a terminal object, any two functions that factor through it will always be equal.  Thus, the truth value of such an atomic formula is independent of the value of $x$, and so the truth value of $\varphi$ must also be so.
=--

However, if ETCS is written using a two-sorted or one-sorted definition of a category, then it is not structurally presented.  For instance, we can take the formula
$$\varphi \equiv \big((s(f)=t(x)) \wedge (f\circ x = z)\big)$$
for variables $f$ and $z$ of type "arrow".  This formula does not contain $A$ at all, yet its truth value (for a fixed $f$ and $z$) is not independent of $x$.  This is why we have defined "structurally presented" rather than "structural"---the presentation matters.

It is, however, easy to modify the two- or one-sorted version of ETCS to make it structurally presented: we simply require the equality relation on functions to be decorated by the source and target sets, and the composition operation on functions to be decorated with the set along which composition occurs.  That is, instead of $f=g$ we write $equal(f,g,A,B)$ (which can only hold when $s(f)=s(g)=A$ and $t(f)=t(g)=B$), and instead of $g\circ f$ we write $g\circ_B f$ where $t(f)=s(g)=B$.  Now the same argument as for the dependently-typed version applies.

It would be nice to have a definition according to which any "presentation" of ETCS would be structural; intuitively, a theory should be structural if it is "equivalent" in some sense to a structurally presented one.  However, I haven't yet been able to come up with a notion of "equivalence" which includes the above modifications of ETCS, yet excludes the equivalence between ETCS and BZC (or ZFC and ETCS+R / SEARC).


## Consequences of structural presentation

From our definition of structural presentation we can deduce some of the other standard properties of structural set theories.  The first is that "elements of different sets cannot be compared for equality."

+-- {: .un_theorem}
###### Theorem
If a structurally presented notion of set includes a basic notion of equality between the elements of distinct sets, which is symmetric and transitive, then all of its sets are [[subsingletons]].
=--
+-- {: .proof}
###### Proof
Suppose that we have a basic equality relation that can relate elements of two distinct sets $A$ and $B$.  Thus, for variables $x$ of type $A$ and $z$ of type $B$, we would have an atomic formula $x=z$.  By symmetry and transitivity, if $x=z$ and $x'=z$, then $x=x'$.  But then $(\star)$ applied to $\varphi\equiv (x=z)$ implies that for any $x,y\in A$ we have $x=y$, so $A$ must be a subsingleton.  Since $A$ was arbitrary, all sets must be subsingletons.
=--

The second is "elements of sets are not themselves sets."

+-- {: .un_theorem}
###### Theorem
Suppose that a structurally presented notion of set includes relations $is:\mathbb{E}_A\looparrowright\mathbb{S}$, which we regard as giving a way to interpret some elements as sets.  Suppose moreover that each $\mathbb{E}_A$ has an equality relation, and that $is(x,B)$ and $is(y,B)$ imply $x=y$.  Then for any set $A$, if there exist $a:\mathbb{E}_A$ and $B:\mathbb{S}$ such that $is(a,B)$, then $A$ must be a subsingleton.
=--
+-- {: .proof}
###### Proof
Suppose that $is(a,B)$ and choose $\varphi\equiv is(x,B)$.  By $(\star)$ it follows that $is(x,B)$ holds for all $x:\mathbb{E}_A$, hence $x=y$ for all $x,y:\mathbb{E}_A$, i.e. $A$ is a subsingleton.
=--

Note that the assumption about equality is quite reasonable if we want to interpret "$is$" as asserting that a given element *is* a given set (rather than merely being related to one in some way).



# Discussions

This discussion originally took place at [[SEAR]], but it is more appropriate here.

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

   AN: Then this should be mentioned in the main text rather than left for the reader to discover for himself or to wonder whether this is really true. Mathematics has a healthy convention that nontrivial claims are supported either by proofs or references to such proofs. Without these one is entitled to mistrust the claim.

   _Toby_:  You may mistrust it if you like.  It is mentioned up top that this is all original; if there were papers to cite that we knew of, then we would cite them.  If what you really want is to be certain that mathematics can be founded on a structural theory, then you should look at the established literature on $\mathbf{ETCS}$ or the type theory of Per Martin-L&#246;f and Thierry Coquand.

_Toby_ continues: But if you want precision, look at the **Definition** section, not the vague **Idea**.  Equality of pure sets is also defined.  
(There\'s still an error in that which I haven\'t fixed, but it\'s correct for well-founded pure sets, which are the ones that $\mathbf{ZFC}$ has.)

AN: I only saw a definition of equivalence. Now I realize that this should substitute for the nonexistence equality. 
I'll comment more on the pure set page.

_Toby_ continues: If you want a set of sets, you should consider whether it matters whether any of these sets happen to be equal, and how (for purposes of your application) you would know.  In general, you take a [[family of sets]] (note to self: write an article there), that is an index set $I$ and, for each element $k$ of $I$, a set $S_k$.  There is a handy trick for encoding this sort of thing as a set $\mathcal{S}$ and a function $\pi: \mathcal{S} \to I$; let $S_k$ be the preimage of $\pi^*(k)$ (which is a subset of $\mathcal{S}$.  The purpose of the axiom of collection is to allow you to construct this set $\mathcal{S}$ (maybe I should write that down there for its motivation!).  If you want, say, a family of groups, then you take $\pi: \mathcal{S} \to I$ and additionally a function $M: I \times \mathcal{S} \times \mathcal{S} \to \mathcal{S}$ such that, for each $k$, $M$ restricts to a function $m_k: S_k \times S_k \to S_k$ that satisfies the group axioms.  And so on.

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

_Toby_:  Also [[quotient set]]s and (in a constructive theory) [[function set]]s make good axioms; one may want these constructions even if one drops power sets.  But for people weaned on $\mathbf{ZFC}$\'s pairing and union axioms, disjoint unions are particularly important!
=--

The following discussion is about the appropriateness of the word "structural."

+--{: .query}
[[Arnold Neumaier]]: Both descriptors ''structural'' and ''material'' sound misnomers. 
The name ''nonstructural'' for ''a set theory in which the elements of a set have no structure apart from their identity as elements of that set'' seems more to the point.

[[Mike Shulman]]: The intended meaning is that structural set theory provides a clean framework for structural mathematics, which is about structures that are built from sets.  This use of the word "structuralism" is quite common, as I'm sure you know.

AN: Yes, I know. But the latter is not captured by your formal definition below.

Your use of ''material'' and ''structural'' is an inappropriate, intuitively misleading use of language, 

There is nothing material about the assertion that [[set theory|currently]] characterizes your term ''material set theory'', namely that the same element can be in two distinct sets.

There is also nothing structural in a set theory that eliminates all structure from sets. What you call ''structural set theory'' deserves to be called a ''theory of structureless sets'', which means essentially the opposite of the name you chose. What you call ''structurally presented'' is much more naturally called ''structureless''. For it is a condition for the absence of structure, rather than one for a structural presentation.

A concept of structural presentation would need to be applicable not just to the notion of set, but to mathematical notions in general, since this is where structure is used.

Do you need to redefine the concept of structural presentation for every kind of notion, or is there a universal formal notion of structural presentation?
What is a formal definition of a structural presentation of a group, or of the natural numbers?

Your defence above does not support your choice of naming. 
Instead, it backfires.

The set theory of Bourbaki fails your axiom for being structurally presented.
But it provides a widely accepted, exceptionally clean framework for structural mathematics, by any reasonable standard.

Mathematics as practiced is both structural and material, no matter into which formal framework it is forced.

To introduce an artificial split, and to introduce it with notions whose formal meaning flies in the face of the informal reading of the words is no service to mathematics.

_Toby_:  I can only speak for myself, but I\'m beyond caring what you think is of service to mathematics.  However, I still have a pathological urge to explain, so ...

What you say about a 'theory of structureless sets' is quite right, as far as it goes.  (I would say that they are not quite structureless, since they have an equality relation, but they\'re close!)  So what\'s structural about a theory of structureless sets?  It\'s that structural set theory thinks of sets in the same way as most mathematicians think about groups, topological spaces, and other abstract structures: up to isomorphism.  Or to put it another way, we only care what the category of sets is like, just as pure group theorists (not that anybody is purely a group theorist) only care what the category of groups is like, not what the structures of the individual groups\' individual elements are.  Most of the structures that people study have a lot of structure; that\'s why they\'re called 'structures'.  Abstract sets, on the other hand, don\'t have very much structure at all; in a sense, they have the least structure possible.  But in structural set theory, we still think of them *as structures*.

I\'m pretty sure that something like that is the origin of the phrase, although I didn\'t invent it and don\'t know for certain.  Whether it is the best phrase to use is another matter.

[[Mike Shulman]]: If this formal definition doesn't capture the intended meaning, then what is wrong is the definition, not the intended meaning.  I said explicitly that it was a *tentative* definition.  However, formal definitions often look somewhat different from the intuitive meaning they are intended to capture; nothing in the intuitive notion of "continuity" tells me that I need open sets to define a topological space!

The set theory of Bourbaki is material.  The fact that it can be used for structural mathematics says nothing about that; after all ZFC can also be used for structural mathematics.  In fact the argument of the structuralist is that *all* mathematics is structural, and the only distinction between set theories is in how well they reflect this fact, not in whether or not they are adequate to describe it.  I would not call Bourbaki's treatment of structure clean, not as clean as a structural set theory; they have to explicitly exclude "non-structural" axioms in their definition of structure, whereas in a structual set theory "non-structural" axioms are impossible to express.
=--


[[!redirects structural set theories]]
