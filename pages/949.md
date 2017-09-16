# Idea #

**Predicative mathematics** is a version of [[constructive mathematics]] which, in addition to rejecting the [[axiom of choice]] and the principle of [[excluded middle]], rejects _impredicative definitions_.

Informally, a definition is _impredicative_ if it refers to a totality which includes the thing being defined.  For example, the definition of a particular real number $x$ as the least upper bound of a given set $A$ is impredicative, because it characterizes $x$ as a particular element of some set (the upper bounds of $A$) which includes $x$.

# Impredicative axioms #

Two [[set theory|set-theoretic]] axioms which are commonly rejected by predicativists as leading to impredicative definitions are the axiom of unbounded [[separation]] and the axiom that any set has a power set.  In particular, the rejection of the latter means that predicativists do not believe the category of sets is a [[topos]], and that conversely predicative mathematics is naturally interpreted in the [[internal logic]] of categories more general than toposes, such as [[Heyting category|Heyting]] [[pretopos]]es.

However, many predicativists do accept the existence of the [[function set]] $B^A$ for any sets $A,B$ (that is, the set of functions $A\to B$).  These predicativists believe that the category of sets is [[locally cartesian closed category|locally cartesian closed]], and their mathematics can be interpreted in any locally cartesian closed pretopos (sometimes called a $\Pi$-pretopos).  Some predicativists also assume stronger axioms, such as the "fullness" or "[[subset collection]]" axiom of Aczel's theory CZF, or the existence of [[W-type|W-types]] (equivalently, [[initial algebra]]s of polynomial functors, a strong form of the axiom of infinity).

It is worth noting that [[excluded middle]] together with the existence of function sets implies the existence of power sets, or equivalently that any cartesian closed [[Boolean category|Boolean]] pretopos is a topos.  (In fact, any Boolean pretopos has a [[subobject classifier]], namely $2=1\sqcup 1$.)

# Discussion #

_[[Mike Shulman|Mike]]_: Is there a formal definition of "impredicative" other than "whatever predicativists don't like?" In particular, I don't understand why exponentials are any less problematic than power sets.  If I have the set $B^A$, can't I then use it to define a new function $A\to B$ in terms of this set that contains the function being defined?

_Toby_: Arguably, Brouwer\'s school doesn\'t accept exponentiation, although they accept some cases of it (such as $N^N$). I\'ve never heard them call it 'impredicative', however. Someday I want to figure out how much can be done using both W-types and co-W-types (equivalently, final coalgebras of polynomial functors) but not exponentiation. (So far, I can construct $A^N$ as the final coalgebra of $X \mapsto A \times X$, but I can\'t prove that it *is* $A^N$!)

****

This discussion began at [[Grothendieck topology]]:

_Mike_: The passage from a collection of covering families ("coverage") to a collection of sieves ("Grothendieck coverage") is a higher-order construction.  One thing this means is that you can't do it if you happen to be a [[predicativism|predicativist]]; thus to study "predicative sheaves" you need to use covering families instead of sieves.  Another thing it means, which I care more about, is that many common coverages can be discussed in the first-order language of a category, while the corresponding Grothendieck coverages require an external set theory.  For instance, I can say "a [[pretopos]] is a [[stack]] for its [[coherent category|coherent]] coverage" in the first-order language of a category, but not if I replace "coverage" by "Grothendieck coverage."

_Toby_: If you\'re going to be a predicativist, then you really have to take the attitude that a structure is defined by an arbitrary family of sets, and the closure conditions can be used afterwards (if the concept is really susceptible to predicativist understanding) to define equivalence of structures. (Note that a 'family of subsets' of $X$ is equivalent to an index set $I$ and a single subset of $I \times X$.)

For example, define a topological space to be a set equipped with an arbitrary family of subsets, called 'subbasic open sets'. Define an 'open set' to be a subset whose every point belongs to the intersection of some finite family of subbasic open sets. Define two topologies on a given set to be equivalent if every subbasic open set in either is open in the other. All of this is predicative.

Actually, if you want to be finitist (in the sense that you have no axiom of infinity and hence no language to state that a family is 'finite') as well, then you must be subtler. Define a topological space to be a set equipped with a family of subsets (now called 'basic open sets') such that nullary and binary intersections of basic open sets are basic open sets (or at least always contain one). Define an 'open set' to be a subset whose every point belongs to some basic open set. Define equivalence as before.

These justify the importance of the concepts of 'basis' and 'subbasis' for a topology, taught in schools today. Perhaps there is a similar justification for 'coverage'? (Or for 'Grothendieck pretopology', for that matter?)

_Mike_: Okay, well, I retract my comment about predicativism, since it is clear that I don't understand (nor, really, care much about) predicative math.  But my other comment about being first-order still stands.

_Toby_: I\'d hoped that my example might give predicatvism (at least in the sense of not having a small set of truth value) some interest. I expect that it\'s related to being first-order and internalisable; after all, the internal logic of many categories is predicative, and rejecting power sets may be seen as an attempt to do all of mathematics in a first-order way. Ah, well.

_Mike_: Perhaps we should move the discussion about predicativity to [[predicativism]]?  (Feel free to do so, snipping out the relevant paragraphs of my responses, if you like.)  I also once had the thought that predicative math was interesting because of the internal logic of non-toposes.  However, I have not encountered any naturally occurring examples (relative to classical mathematics) of, say, locally cartesian closed pretoposes which are not actually toposes.  I am not a philosophical constructivist.  I like constructive proofs for the same reason I like to prove things about arbitrary rings rather than about the integers: the result is more general and applies in more contexts.  Toposes (of sheaves, usually) arise naturally in classical mathematics, so it is a good thing to know what proofs can be interpreted internally in a topos.  If I knew a similar class of locally cartesian closed pretoposes that arose naturally in classical mathematics, I would be more favorably inclined towards predicativism.

_Toby_: Philosophically, I\'m a pluralist, so I also like constructivism (in the sense of Bishop, without classically false axioms) for its wider applicability. And I even like mathematics *with* classically false axioms as much (potentially) as classical mathematics and wish it were more fully developed. But while you might be interested in such mathematics only if the categories that it can be internalised in come up in actual mathematical practice, it\'s enough for me if it comes up in actual *philosophical* practice; that is, if there is a school of constructivists interested in working with certain restrictions and axioms, then I\'m interested in knowing what mathematics might apply there, and I try to do mathematics so that it will apply there.

(To be honest, I almost convinced myself that I\'m interested, for their own sake as the 'right' way to do things, in foundations that amount to working in a locally cartesian closed pretopos whose category of lex endofunctors has enough injectives, but as soon as I got as far as figuring that out, I got onto something else.)

I hope that predicativism can still tell us something about how "a pretopos is a stack for its coherent coverage" works where "a pretopos is a stack for its coherent Grothendieck coverage" doesn\'t. But it\'s already enough to interest me in predicativism that there are predicativists.

_Mike_: Fair enough.  I can understand that, even if it's not my philosophy.

Actually, on further reflection, it's not really accurate to say that I don't care about predicativism.  It's the specific variety of predicativism that accepts things like exponentials, W-types, fullness, and/or collection, but not power sets, that I have trouble justifying. Because I do care about what can be made first-order, I care about the internal logic of a Heyting category, which could be called "even more" predicative; I'm just not used to giving it that label.  And the category of classes in a membership-based set theory is a good example of a positive Heyting category that doesn't even have exponentials.

_Toby_: I care about that too, and since predicativism in practice is a vague term that might not allow exponentials either (as Brouwer didn\'t), the practice might still be wroth examining for that purpose. But that is not something that can be established theoretically, so I\'ll just use any useful examples that I see, and leave it at that.

_Mike_: I realized that there is a class of [[locally cartesian closed category|locally cartesian closed]] [[extensive category|extensive]] [[Heyting category|Heyting categories]] that I care about: extensive [[quasitopos|quasitoposes]].  I used to believe that the correct [[internal logic]] of a quasitopos used the fibration of regular subobjects, rather than the fibration of all subobjects, but that logic is kind of poorly behaved, for instance it doesn't satisfy function comprehension (if you prove that for all $a\in A$ there exists a unique $b\in B$ such that blah, then all you get is a span $A\leftarrow C\to B$ where $C\to A$ is monic and epic).  Quasitoposes are always locally cartesian closed Heyting categories, and I think it's fair to say that all the interesting ones are extensive as well.

Any quasitopos that is a [[pretopos]] is in fact a topos, so I still don't know any interesting locally cartesian closed pretoposes that aren't toposes.  One could take the ex/reg completion of an extensive quasitopos to get an interesting pretopos, but I don't know whether it would still be locally cartesian closed.  But any locally cartesian closed Heyting category has an internal logic which is predicative with exponentials.  I wonder which quasitoposes have W-types and stuff like that.

_Mike_: Also, the [[exact category|ex/lex completion]] takes extensive categories to pretoposes and preserves local cartesian closedness.  So, in particular, the ex/lex completion of a topos is locally cartesian closed pretopos which is not, in general, a topos.  I'm not sure what interesting categories of this sort there are.