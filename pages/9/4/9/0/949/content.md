

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


# Predicative mathematics
* tic
{: toc}


## Idea

__Predicative mathematics__ is a way of doing [[mathematics]] without allowing impredicative definitions.

Informally, a definition is _impredicative_ if it refers to a totality which includes the thing being defined.  For example, the definition of a particular real number $x$ as the least upper bound of a given set $A$ is impredicative, because it characterizes $x$ as a particular element of some set (the upper bounds of $A$) which includes $x$.  Possibly $x$ can be defined in some other way and then proved to be the least upper bound of $A$, but to define it thus by fiat is impredicative.

There are (at least) two broad schools of the [[foundations]] of predicative mathematics that don\'t talk much to each other: one school that uses lower-order forms of [[higher-order logic]] (or the [[set theory]] that this justifies) and [[classical logic]], and a [[constructive mathematics|constructive]] school that uses first-order [[type theory]] (or the set theory that this justifies) and [[intuitionistic logic]].  The common ground is that both schools reject [[power set]]s; other axioms may vary.  Here we tend to think of what predicative mathematics allows [[Set|the category of sets]] to be.


## Impredicative axioms

Not all of these axioms are rejected by all predicativists, but they at least come under some suspicion.

### Infinity

The [[axiom of infinity]] is not usually considered impredicative, but we list it anyway, as it is needed for the others to have force.  Mathematics that does not require this axiom, [[finite mathematics]], can be interpreted in a predicative framework even if it uses the axioms below.

### Power set

The axiom that any set has a [[power set]] is perhaps the fundamental feature missing from predicative mathematics.  In particular, the sequence
$$ \mathbf{N}, \mathcal{P}\mathbf{N}, \mathcal{P}\mathcal{P}\mathbf{N}, \ldots $$
may be accepted in part, but not forever.

The failure of the power set axiom means that the category of sets is not an elementary [[topos]].  (Note that $Set$ is still a [[Grothendieck topos]], defined as a category of sheaves or in terms of Giraud\'s characterisation, since the theorem that such a category is an elementary topos requires the power set axiom.)

### Unbounded separation

The constructive school generally accepts the [[axiom of replacement]] but not unbounded forms of the [[axiom of separation]].  (This choice is not available to the classical school, since replacement and [[excluded middle]] together imply unbounded separation.)

Na&#239;vely, the axiom of separation says that, if $A$ is a set and $P$ is a [[function]] from $A$ to the set of [[truth value]]s, then there is a set
$$ \{ A | P \} = \{ x \in A \;|\; P(x) \} .$$
To be precise, however, this $P$ should be written as a [[predicate]] in the language of set theory.  The form of separation justified by type theory and such structural set theories as [[ETCS]] requires the [[quantifiers]] in this predicate to be guarded; unbounded separation is the generalisation of this to unguarded quantifiers.

(We need more on this, particularly with regards to the classical school and replacement.)

### Function sets

One sometimes speaks of forbidding [[function set]]s instead of power sets.  That is, it is the sequence
$$ \mathbf{N}, \mathbf{N}^{\mathbf{N}}, \mathbf{N}^{\mathbf{N}^{\mathbf{N}}}, \ldots $$
that is avoided.

Of course, function sets can be constructed out of power sets (using *bounded* separation), so forbidding function sets certainly forbids power sets.  The converse holds if there is a set $\Omega$ of [[truth value]]s.

With [[excluded middle]], the set of truth values is easy to achieve, as $\{0,1\}$; in particular, if you have $\mathbf{N}$, then you certainly have $\Omega$.  So the classical school of predicativism rejects function sets.

The constructive school, however, often accepts function sets.  In this school, the sequence above is fine.  Actually, the slightly stronger axiom of [[subset collection]] is adopted by Peter Aczel\'s $\mathbf{CZF}$ and justified by Per Martin-L&#246;f\'s $\mathbf{ITT}$.

Brouwer, on the other hand, did not accept the sequence above, although his followers differ on when (if ever) it stops.

### Ill-founded structures

Most foundations of mathematics are predicative in one sense: no set may belong to itself.  This (or rather, a certain strengthening of this) is the [[axiom of foundation]].  An alternative is the axiom of antifoundation, which explicitly allows for and tames such sets as $\bullet$, where $\bullet = \{\bullet\}$.  Indeed, this equation is a perfectly good way to *define* $\bullet$ using antifoundation, yet this is about as impredicative as a definition can get.

Once one accepts the [[axiom of infinity]], there\'s not much objection to accepting more general [[W-type]]s; these are sets that are defined recursively much like a [[natural numbers object]].  Categorially, we may see these as [[initial algebra]]s of certain functors on $Set$.  The [[terminal coalgebra|final coalgebra]]s of these functors also exist in impredicative theories, but not predicatively.


## The category of sets

So what is the category of sets in predicative mathematics?

At bottom, let us suppose that $Set$ is a [[Heyting category|Heyting]] [[pretopos]]; this is a category whose [[internal logic]] is first-order and contains only constructions that don\'t require any of the above axioms.

Since we\'re not doing finite mathematics, we may also include a [[natural numbers object]].  In fact, we could include more general [[W-type]]s, since these are no harder to justify philosophically than $\mathbf{N}$, although the proofs that these exist if $\mathbf{N}$ does rely on possibly impredicative axioms.  Then $Set$ is a Heyting $W$-pretopos.

If you accept function sets, then $Set$ is [[locally cartesian closed category|locally cartesian closed]].  In this case, $\mathbf{N}$ is enough to get all $W$-types, so we have a $\Pi$-$W$-pretopos.  If you accept excluded middle, then $Set$ is a [[Boolean category|Boolean]] pretopos or a Boolean $W$-pretopos.  But a Boolean $\Pi$-pretopos is necessarily a topos, which would make the theory impredicative.


## The real numbers

An important question in predicative mathematics is the status of the set $\mathbf{R}$ of [[real number]]s.  This set is often constructed as a subset $R_D$ of $\mathcal{P}\mathbf{N}$ or as a [[subquotient]] $R_C$ of $\mathbf{N}^{\mathbf{N}}$, neither of which can be formed in an arbitrary Heyting $W$-pretopos.  The latter can be formed in a $\Pi$-$W$-pretopos, but it is not necessarily correct.

The constructive school of predicativism can construct $\mathbf{R}$ in various ways.  One method is to use $R_C$ directly, but this will only go so far unless something is done to prove that it is Dedekind-complete.  This will follow from [[countable choice]], which is accepted by most constructive schools; it also follows from [[excluded middle]], but of course that is not an option here.  Using [[subset collection]], a variation on $R_C$ is possible which can be proved Dedekind-complete without countable choice; this is very natural from the perpective of type theory (but then, countable choice is also very natural from that perspective).

It is also possible to assert the existence of $\mathbf{R}$ by fiat, much like $\mathbf{N}$ exists by the axiom of infinity.  This is the approach taken by the classical school; they use $\mathcal{P}\mathbf{N}$ instead of $\mathbf{R}$ directly, but these are isomorphic by excluded middle.  This is natural from the perspective of predicative set theory as a weak form of higher-order logic; you assert the existence of $\mathbf{N}$, $\mathcal{P}\mathbf{N}$, and maybe $\mathcal{P}\mathcal{P}\mathbf{N}$, then stop.

There is also the question of what exactly it means to say that $\mathbf{R}$ exists; is it a set or a [[proper class]]?  Without function sets, the distinction between these is not clear-cut; higher order logic suggest a hierarchy of more and more proper (less and less [[small category|small]]) classes rather than a single unified notion of set.  If you allow $\mathbf{N}$ only as a proper class, then you are basically still doing [[finite mathematics]]; if you allow $\mathbf{R}$ only as a proper class, then you are doing predicative mathematics.


## Formalising mathematics

How much of mathematics can be done predicatively?

A surprisingly large amount of mathematics can be formalised, using various coding tricks, in a theory in which $\mathbf{N}$ is a set but $\mathcal{P}\mathbf{N}$ is a proper class.  This is somewhat easier in Nik Weaver\'s 'conceptualist' approach, which accepts $\mathcal{P}\mathcal{P}\mathbf{N}$ as a proper class; the encoding is not really more complicated than what is usually done in material set theory for ordered pairs and the like.  Note that these are conservative over Peano arithmetic; that is, anything expressible in $\mathbf{PA}$ and provable in these systems is provable in $\mathbf{PA}$ (which certainly cannot be said of <b>[[ZFC]]</b> or <b>[[ETCS]]</b>, which prove the consistency of $\mathbf{PA}$).

Constructive mathematics generally requires great care with anything other than basic discrete mathematics after the middle of the 19th century, but requiring it to be predicative does not usually add much difficulty, as long as function sets are allowed.  This even extends to [[category theory]], which is not usually contemplated in the classical approach.  (However, the internal logic of a $\Pi$-$W$-pretopos is certainly not conservative over $\mathbf{PA}$; it also proves consistency.)


## References

*  Sol Feferman; [Relationships between Constructive, Predicative and Classical Systems of Analysis](http://hlombardi.free.fr/FefermanRelationships.pdf) (PDF).
*  Nik Weaver; [papers on conceptualism](http://www.math.wustl.edu/~nweaver/conceptualism.html).
*  from the Standford Encyclopedia of Philosophy:
   *  [Predicativity in constructive set theory](http://plato.stanford.edu/entries/set-theory-constructive/#PreConSetThe).
   *  [Predicativism](http://plato.stanford.edu/entries/philosophy-mathematics/index.html#Pre)


## Discussion

_[[Mike Shulman|Mike]]_: Is there a formal definition of "impredicative" other than "whatever predicativists don't like?" In particular, I don't understand why exponentials are any less problematic than power sets.  If I have the set $B^A$, can't I then use it to define a new function $A\to B$ in terms of this set that contains the function being defined?

_Toby_: Arguably, Brouwer\'s school doesn\'t accept exponentiation, although they accept some cases of it (such as $N^N$). I\'ve never heard them call it 'impredicative', however. Someday I want to figure out how much can be done using both W-types and co-W-types (equivalently, final coalgebras of polynomial functors) but not exponentiation. (So far, I can construct $A^N$ as the final coalgebra of $X \mapsto A \times X$, but I can\'t prove that it *is* $A^N$!)

****

This discussion began at [[Grothendieck topology]]:

_Mike_: The passage from a collection of covering families ("coverage") to a collection of sieves ("Grothendieck coverage") is a higher-order construction.  One thing this means is that you can't do it if you happen to be a [[predicativism|predicativist]]; thus to study "predicative sheaves" you need to use covering families instead of sieves.  Another thing it means, which I care more about, is that many common coverages can be discussed in the first-order language of a category, while the corresponding Grothendieck coverages require an external set theory.  For instance, I can say "a [[pretopos]] is a [[stack]] for its [[coherent category|coherent]] coverage" in the first-order language of a category, but not if I replace "coverage" by "Grothendieck coverage."

_Toby_: If you\'re going to be a predicativist, then you really have to take the attitude that a structure is defined by an arbitrary family of sets, and the closure conditions can be used afterwards (if the concept is really susceptible to predicativist understanding) to define equivalence of structures. (Note that a '[[family of subsets]]' of $X$ is equivalent to an index set $I$ and a single subset of $I \times X$.)

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


[[!redirects predicativism]]