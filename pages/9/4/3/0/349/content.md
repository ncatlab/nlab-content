#Idea#

A _Grothendieck topology_ on a category is a choice of morphisms in that category which are regarded as [[cover|covers]].

A category equipped with a Grothendieck topology is a [[site]].  Sometimes all sites are required to be [[small category|small]].

Probably the main point of having a site is so that one can define [[sheaf|sheaves]], or more generally [[stack|stacks]], on it.  In particular, the category of sheaves on a (small) site is a [[Grothendieck topos]].


#Definition#

A **Grothendieck topology** $J$ on a category $C$ assigns to each object $c$ a collection of [[sieve|sieves]] on $c$ which are called _covering sieves_, satisfying the following axioms: 

*  If $F$ is a [[sieve]] that covers $c$ and $g: d \to c$ is any morphism, then the pullback sieve $g^* F$ covers $d$. 

* The maximal [[sieve]] $id: \hom(-, c) \hookrightarrow \hom(-, c)$ is always a covering sieve; 

* Two [[sieve|sieves]] $F, G$ of $c$ cover $c$ if and only if their intersection $F \cap G$ covers $c$. (Here the saturation condition is important.) 

* If $F$ is a sieve on $c$ such that the sieve 
    $\bigcup_d \{g: d \to c| g^* F \; covers \; d\}$
    is a covering sieve of $c$, then $F$ itself covers $c$. 

The set of covering sieves of an object $c$ is denoted $J(c)$, and the first axiom guarantees that we have a functor $J: C^{op} \to Set$.


# Related notions #

A more general notion is simply a collection of "covering families," not necessarily sieves, satisfying only pullback-stability; this suffices to define an equivalent notion of sheaf.  Following the [[Elephant]], we call such a system a [[coverage]].  A Grothendieck topology may then be defined as a coverage that consists of sieves and satisfies certain extra saturation conditions; see [[coverage]] for details.

Grothendieck topologies on a small category $C$ are also in bijective correspondence with [[Lawvere-Tierney topology|Lawvere-Tierney topologies]] on the [[presheaf]] [[topos]] $[C^{op},Set]$.  See [[Lawvere-Tierney topology]] for a description of the correspondence.


#Terminology#

The term "topology" for this concept is hallowed by tradition and the name of Grothendieck, but some people consider it to be somewhat unfortunate. While "a category equipped with a (Grothendieck) topology" is, in fact, sort of a generalization of "a set equipped with an (ordinary) topology," the relationship between a category and its topology is quite different from the relationship between a set and its topology.  In particular, when we construct a site from a topological space, the objects of the category are the _open sets_, not the points, of the space.

This use of "topology" can also lead to confusion since for a topologist, there is a completely different and very natural meaning of "topology on a category:" namely, topologies on its sets of objects and morphisms making it into an [[internal category]] in [[Top]].  The topologist's definition is, of course, a conservative extension of the classical notions of "topology on a set" and even "topology on a group," while there are no nontrivial Grothendieck topologies on a group considered as a 1-object category.

Furthermore, the use of "topology" for a category with a system of covers also leads to the use of "continuous" for a functor which preserves covers.  This is (in some people's opinion) doubly unfortunate, since "continuous functor" is used not only by topologists to mean an internal or [[enriched category|enriched]] functor over Top, but also by many category-theorists to mean a functor that preserves all small [[limit|limits]].  This is especially confusing since covers are more akin to colimits than limits. Moreover, while a continuous function between topological spaces does induce a a cover-preserving functor between categories of open sets, the function and the functor go in opposite directions.

In [[Elephant|Sketches of an Elephant]], Peter Johnstone introduced the term __coverage__ used above for a system of covers on a category, with "Grothendieck coverage" as a proposed replacement for "Grothendieck topology."  See [[coverage]] for his definitions.  Proposed replacements for "Lawvere-Tierney topology" include:

* _Local operator_ (used by Johnstone).

* _Local modality_ or _geometric modality_, since in the [[internal logic]] of the topos, it represents a [[modal operator]] with the intutive meaning of "it is locally the case that...".

* _Lawvere-Tierney operator_ or _Lawvere-Tierney modality_ to avoid possible conflict with other uses of "local" or "geometric" in modal logic.

The following discussion is about this terminological issue:


+--{.query}
So what\'s stopping us from going with Johnstone? &#8212;Toby (And how about 'Lawvere&#8211;Tierney operator'?)

Well, I was hesitant to make such a change without getting some support from other people.  "Lawvere-Tierney operator" would work.  At the nCafe, Todd suggested "local modal operator" and I countersuggested the shorter "local modality." -Mike

Toby says: I like eponyms, because they\'re less likely to be overloaded. Of course, it\'s important that a Lawvere&#8211;Tierney operator is a locality modality (speaking of cute names ...), but there may be others. In a similar vein, I don\'t really like using 'coverage' for a basis for a Grothendieck coverage. (What is such a basis, by the way? Is it anything like a Grothendieck pretopology?, which we may call 'Grothendeick precoverage' of course.)

_Mike_: Does "local" have an existing meaning in modal logic?  If not, I would be inclined to essentially take Lawvere-Tierney operators as a definition of a "local modality."

I am not as fond of eponyms because they are not descriptive unless you already know what they mean.  Saying something is a "Grothendieck foo" or "Lawvere-Tierney foo" conveys no information to the reader beyond "foo," unless they are already aware that there are different types of foo and know what each eponym refers to.

A coverage in Johnstone's sense is even weaker than a Grothendieck pretopology: it's a set of covering families satisfying only stability under pullback (which can be defined even without required the underlying category to have pullbacks).  Perhaps I was mistook and there is no classical notion of "basis," or else this is not it?  Johnstone makes the point that this is really the essential aspect of a coverage that makes sheaves behave the way we are used to; all the other conditions Grothendieck imposed are just "closure" conditions that are there because they might as well be.  Do you have any objection to "coverage" other than its lack of eponymity?

_Toby_: Isn\'t stability under pullback also a closure condition? I dislike using basic terms for anything between an arbitrary collection and a collection closed under everything.

As long as you think that 'local' doesn\'t have any other meaning in modal logic (in particular, if it\'s the same as the one [here](http://homepages.mcs.vuw.ac.nz/~rob/papers/modalhist.pdf)), then 'local modality' or 'local operator' is OK; one can always restore 'Lawvere&#8212;Tierney' afterwards if necessary.

_Mike_: Stability under pullback is a closure condition in the formal sense, but unlike the others, it makes a difference to the notion of sheaf whether or not we impose it.  If I have a class of covering families satisfying pullback-stability, I can close it up under the other properties without changing the notion of "sheaf," but that is not true for pullback-stability.  There is an example somewhere in the Elephant of a collection of "covering families" that is not pullback-stable and whose category of "sheaves" is not a topos.

Section 7.6 of the paper you link to is all about "geometric modalities" with reference to local operators on a topos, which implies that there is no other modal-logic notion of "local."

_Toby_: OK, I see that Johnstone\'s notion of 'coverage' is good because you can write down a simple (the usual) definition of 'sheaf', whereas the definition would be more complicated if you started with an arbitrary collection.

I remembered that paper as having a couple of different kinds of local modalities, but now I see that really it had a couple of different kinds of 'geometric logic' instead, so that\'s all right.

_Mike_: Another thing worth mentioning ... moved to [[predicativism]].

In the other conversation we seem to be having simultaneously, now I think I might actually prefer _geometric modality_ over "local modality."  It's not really the modality that's local, so "locality modality" would be more correct, if it didn't have an unfortunate rhyme.  But "geometric modality" doesn't have that problem and also suggests that they induce geometric morphisms.

_Toby_: Ah, but now you run into conflicts with other meanings of 'geometric logic' in modal logic! It\'s wrong to favour 'locality modality' for the cute rhyme, but we shouldn\'t reject it if it\'s really correct.

_Mike:_ What are the other meanings of "geometric"?  I didn't notice any in the paper you linked to but maybe I didn't look hard enough.

_Toby_: See Sections 3.2 and 4.5. I think that you can argue that the former should really be called 'topological', while the latter seems to refer (it\'s not clear to me) to an outdated understand of 'geometry' as meaning Euclid\'s axioms; but they do show that 'geometric modality' could be misconstrued by at least some people. Thus I would still prefer 'Lawvere&#8211;Tierney modality', at least when inventing a new term.

_Mike_: Actually, I think the one in section 3.2 is actually a special case of what we're doing here--I think there's a coverage on the poset $P(X)$ of all subsets of a topological space whose covers are the families with topologically-dense image.  As for the one in 4.5, I don't think that a single speculative sentence in a paper in 1957, if it was never pursued or made precise, prevents us from using "geometric modality" to mean something different that it is evidently well-suited for.

_Toby_: OK, fair enough; I prefer the eponym only on general grounds of safety.

_David Roberts_: A coverage in Johnstone's sense is even weaker than requiring pullbacks of covers to exist, just that there exists some cover which fills the role of pullback, but doesn't have to be universal.

_Mike_: Yes, that's what I intended by "stability under pullback (which can be defined even without required the underlying category to have pullbacks)."  But what you said is more correct.

_Zoran_ "relationship between a category and its topology is quite different from the relationship between a set and its topology. In particular, when we construct a site from a topological space, the objects of the category are the open sets, not the points, of the space."

I do not understand guys what is the complaint here. Classically topology is a FAMILY of open sets, not family of points. Who cares what kind of data determine open sets,
this can always be generalized. But in any case, any proper generalization of topology of a top space is a collection of local windows into the space, which you call open sets.
If they are determined by more than just points that means you have to give some orientation about where they lie. That is why you put the morphisms into the game. In noncommutative geometry there are other generalizations and nobody complains against word topology. For example the lattice of hereditary torsion theories. Over there one does not have stability axiom, pullback of cover will not be necessarily a cover. Van Oystaeyen has axiomatized this situation. There are oter approaches like Q-categories, where sheaf theory looks more like in Lawvere-Tierney approach. 

_Toby_:  I agree with your approach to topology (the field of mathematics), but the complaint is more about the grammar of the word 'topology'.  That is, traditionally one talks of 'a toplogy on' a set of points; now one talks of 'a topology on' a category of objects and morphisms, but the elements of this set and category don\'t correspond.  In noncommutative geometry, does one ever put 'a topology on' something that consists of local windows in some sense?

_Zoran_ Topology is in any case on a space of some kind. The fact that in differential geometry space is given by local coordinate charts, in set-theoretic topology by a set
with the topology itself, in noncommutative geometry on a hypothetical object locally behaving like dual to a ring etc. does not change anything. Topology is on a 'space', not on points; whether a concrete example is defined by collection of sets, and sets are made of points does not matter. At least the second view is very faint in my memory. Poincare had worked with manifolds which had much more rich struture than just topological space, the fact that the extension of open sets is determined by the points is accidental. Open subschemes of a scheme for example are not deteremined by underlying reduced scheme, infinitesimal neighborhoods of different order have the same underlying set, and both are open windows of a sort. Topology is a structured collection of open windows on a space this or that way in my view.  

[[Mike Shulman|Mike]]: All I can say is to essentially repeat what Toby said.  A site is, certainly, a type of space (or, at least, the topos of sheaves on it is a space).  But to me "a topology" is a structure that one puts onto a set of points to make it _into_ a space.  I never call, for instance, the real line "a topology;" I call it "a topological space," meaning a set _equipped with_ a topology.  Grothendieck decided that "a topology" should also mean a different structure that one puts onto a category to make it into a space.  The problem is that these two meanings are in conflict.

[[Zoran Skoda]]: My point was that the topology as a subject existed BEFORE Hausdorff, and was dealing mainly with some examples, which were manifolds embedded in Eucledean space,
polyhedra and so on. When Hausdorff defined a topology on a set, it was just an abstraction of situation where he was considering what part is essential from topological point of view and made axioms for "topology" on a set. So space he started looking at was already there, and only in his particular abstraction he said well, I can STILL call it space, though I have neglected fine structure of the metric and just left this assembly out of it...topology. 
On the other hand, I do not consider "site" a "space"; for many reasons not the least being that Grothendieck considered topos more invariant than a site. From the point of view of algebraic geometer, the site of interest is the category of affine schemes with some subcanonical Grothendieck (pre)topology, and an algebraic kind of SPACE is NOT that site, but rather any sheaf in that topology.
Thus such sheaf is a space, site is not (any 'affine' site is just a toolbox having pieces and scissors for assemblying such a space out of "pieces' via descent). The objects are of course representable sheaves, hence representable spaces. 

[[Mike Shulman|Mike]]: I view that as reaching pretty far back.  Hausdorff was writing in 1914, nearly a century ago.  In modern mathematics, "topology" is always used is Hausdorff's sense, until Grothendieck decided it should also mean something different.

I did remark that probably the topos of sheaves should be considered the space rather than the site.  Certainly a topos is not always considered a "space," but sometimes it is.  Anyway I don't think the question of what is, or isn't, a "space" is really relevant.

_Harry_: I feel like grothendieck topology is fine, since the condition of continuity is actually a condition about the function's behavior with respect to the contravariant open set functor. It's in this sense that a Grothendieck topology generalizes a classical topology.
=--


[[!redirects Grothendieck topologies]]