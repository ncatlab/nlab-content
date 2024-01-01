
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+--{: .hide}
[[!include mathematicscontents]]
=--
=--
=--

# Predicative mathematics
* table of contents
{: toc}

## Idea

__Predicative mathematics__ is a way of doing [[mathematics]] without allowing impredicative definitions.

Informally, a definition is _impredicative_ if it refers to a totality which includes the thing being defined.  For example, the definition of a particular real number $x$ as the least upper bound of a given set $A$ is impredicative, because it characterizes $x$ as a particular element of some set (the upper bounds of $A$) which includes $x$.  Possibly $x$ can be defined in some other way and then proved to be the least upper bound of $A$, but to define it thus by fiat is impredicative.

There are (at least) two broad schools of the [[foundations]] of predicative mathematics that don\'t talk much to each other: one school that uses lower-order forms of [[higher-order logic]] (or the [[set theory]] that this justifies) and [[classical logic]], and a [[constructive mathematics|constructive]] school that uses first-order [[type theory]] (or the set theory that this justifies) and [[intuitionistic logic]]. The common ground is that both schools reject [[power sets]]; other axioms may vary. Here we tend to think of what predicative mathematics allows [[Set|the category of sets]] to be. 

Constructive predicativists sometimes accept principles (such as [[function sets]] and the [[axiom of replacement]]) that classical predicativists must reject because they imply impredicative results using [[excluded middle]].  Such mathematics may be called _weakly predicative_.

### Power classes vs no power sets at all

Another division within predicative mathematics is whether [[power sets]] can be formed but are [[proper classes]] instead of sets or [[large sets]] instead of [[small sets]], or whether [[power sets]] simply cannot be formed at all. 

In the former case, almost everything which could be done in impredicative mathematics could be done in predicative mathematics, only with the requirement that size issues have to be taken into consideration at all times. This is the case with predicative constructive [[dependent type theories]] which have [[type universes]], where given the type universe $U$ one could construct a large [[type of propositions]] by $\Omega \coloneqq \sum_{A:U} \mathrm{isProp}(A)$ with power sets as function sets with codomain $\Omega$, as well as various notions of [[class theory]] such as [[Morse-Kelley class theory]], where power sets exist as [[power classes]]. Sometimes, one would have an entire hierarchy of power sets $\mathcal{P}_n(S)$ for hierarchy level $n$, as is common in [[dependent type theory]] with a cumulative hierarchy of universes, with $\mathcal{P}_{n + 1}(S)$ larger than $\mathcal{P}_n(S)$ for all $n$. This is also the case with [[Bertrand Russell]]'s original predicative ramified hierarchy of types in [[Principia Mathematica]]. 

When power sets don't exist at all, whether as a set or a proper class, this results in strictly weaker foundations, since in this case one simply cannot form various mathematical structures which require the use of [[power sets]], such as the [[Dedekind real numbers]], [[topological spaces]], [[frames]], and [[locales]]. This is usually the case for predicative mathematics done internally in a [[Heyting pretopos|Heyting]] or [[Boolean pretopos]], as well as for predicative [[material set theories]] like [[Kripke–Platek set theory]] which do not have an internal notion of [[class]]. In [[dependent type theory]], this notion of predicativity requires not having any [[type universes]] in the type theory itself, since otherwise $\sum_{A:U} \mathrm{isProp}(A)$ is a large [[type of propositions]]. In addition, unlike for [[set theory]], not having power sets in [[dependent type theory]] results in additional structure like [[formal topologies]] or [[inductive covers]] not being definable in the type theory, since without universes or types of propositions one cannot define relations between elements and subtypes. 

## Impredicative axioms

Not all of these axioms are rejected by all predicativists, but they at least come under some suspicion.

### Infinity

The [[axiom of infinity]] is not usually considered impredicative, but we list it anyway, as it is needed for the others to have force.  Mathematics that does not require this axiom, [[finite mathematics]], can be interpreted in a predicative framework even if it uses many of the axioms below.

### Power set

The axiom that any set has a [[power set]] is perhaps the fundamental feature missing from predicative mathematics.  In particular, the sequence
$$ \mathbf{N}, \mathcal{P}\mathbf{N}, \mathcal{P}\mathcal{P}\mathbf{N}, \ldots $$
may be accepted in part, but not forever.

The failure of the power set axiom means that the category of sets is not an [[elementary topos]].

### Unbounded separation

The constructive school generally accepts the [[axiom of replacement]] but not unbounded forms of the [[axiom of separation]].  (This choice is not available to the classical school, since replacement and [[excluded middle]] together imply full separation.)

Na&#239;vely, the axiom of separation says that, if $A$ is a set and $P$ is a [[function]] from $A$ to the set of [[truth value]]s, then there is a set
$$ \{ A | P \} = \{ x \in A \;|\; P(x) \} .$$
To be precise, however, this $P$ should be written as a [[predicate]] in the language of set theory.  The form of separation justified by type theory and such structural set theories as [[ETCS]] requires the [[quantifiers]] in this predicate to be guarded by sets; unbounded separation is the generalisation of this to arbitrary quantifiers.

Arguably, the impredicative core of both separation and power sets (in the presence of bounded separation) is [[limited separation]]: separation in which the quantifiers in $P$ may be guarded by power classes.

*We need more on this, particularly with regards to the classical school and replacement.*

### Function sets

One sometimes speaks of forbidding [[function set]]s instead of power sets.  That is, it is the sequence
$$ \mathbf{N}, \mathbf{N}^{\mathbf{N}}, \mathbf{N}^{\mathbf{N}^{\mathbf{N}}}, \ldots $$
that is avoided.

Of course, function sets can be constructed out of power sets (using *bounded* separation), so forbidding function sets certainly forbids power sets.  The converse holds if there is a set $\Omega$ of [[truth value]]s.

With [[excluded middle]], the set of truth values is easy to achieve, as $\{0,1\}$; in particular, if you have $\mathbf{N}$, then you certainly have $\Omega$.  So the classical school of predicativism rejects function sets.

The constructive school, however, often accepts function sets (thus being *weakly* predicative).  In this school, the sequence above is fine.  Actually, the slightly stronger axiom of [[subset collection]] is adopted by [[Peter Aczel]]\'s $CZF$ and justified by [[Per Martin-Löf]]\'s $ITT$.

[[Brouwer]], on the other hand, did not accept the sequence above, although his followers differ on when (if ever) it stops.

### Excluded middle

Classical predicativists of course accept [[excluded middle]]; otherwise they would be [[constructivism|constructivists]].  But from the perspective of weakly predicative constructive mathematics, excluded middle is impredicative, since it implies power sets (given function sets) and unbounded separation (given replacement).

### Choice operators

Some classical predicativists accept [[choice operators]]. This includes [[dependent type theories]] which include [[choice operators]] but reject [[dependent function types]]. But from the perspective of weakly predicative constructive mathematics, choice operators is impredicative, since it implies excluded middle, and thus power sets (given function sets) and unbounded separation (given replacement). 

### Bijection sets

In predicative mathematics with choice operators, having [[bijection sets]] implies power sets, since choice operators imply the [[axiom of choice]], which in turn implies power sets. 

### Propositional resizing

In the constructive school, one would sometimes have multiple sets of propositions, but those only represent the set of $U$-small [[propositions]] or [[subsingletons]] $\Omega_U$, given a [[universe]] $U$, rather than the set of all propositions $\Omega$. In general, given any two universes $U$ and $V$, one cannot prove that $\Omega_U$ is equivalent to $\Omega_V$. This is common in type theoretic models of constructive mathematics. 

The axiom of [[propositional resizing]] is then statement that given any two universes $U$ and $V$, the sets $\Omega_U$ and $\Omega_V$ of propositions in $U$ and $V$ respectively are in [[bijection]] with each other $\Omega_U \cong \Omega_V$. This axiom implies that there is only one set of propositions up to bijection, which in combination with the existence of [[function sets]] imply [[power sets]], so is impredicative. 

### Ill-founded structures

Most foundations of mathematics are predicative in one sense: no set may belong to itself.  This (or rather, a certain strengthening of this) is the [[axiom of foundation]].  An alternative is the axiom of antifoundation, which explicitly allows for and tames such sets as $\bullet$, where $\bullet = \{\bullet\}$.  Indeed, this equation is a perfectly good way to *define* $\bullet$ using antifoundation, yet this is about as impredicative as a definition can get.

Once one accepts the [[axiom of infinity]], there\'s not much objection to accepting more general [[inductive type]]s such as [[inductive-inductive types]] and [[quotient inductive types]]; these are sets that are defined recursively much like a [[natural numbers object]].  Categorially, we may see these as [[initial algebra]]s of certain functors on $Set$.  [[coinductive type|Coinductive types]], which are the [[terminal coalgebra|final coalgebra]]s of these functors, also exist in impredicative theories, but not predicatively.

### Polymorphic definitions

A different sort of impredicativity is to be found in some [[type theory|type theories]], in which, roughly speaking, one is allowed to define "functions" whose "domain" is the class of all types.  For instance, one might be able to form a type called $\forall \alpha:Type, \alpha\to\alpha$, which has the property that an inhabitant of that type is a "function" which assigns to *every* type $\alpha$, an endomorphism of $\alpha$.  This is clearly impredicative, since the type $\forall \alpha:Type, \alpha\to\alpha$ is also a possible value of $\alpha$.

The philosophy behind this sort of impredicative definition is that any inhabitant of such a type must be defined "uniformly" enough that it uses no details about the type $\alpha$, and thus can equally well be applied to any $\alpha$.  For instance, consider the operation which assigns to every $\alpha$ the identity $id\colon \alpha\to\alpha$; this is defined in exactly the same way for every $\alpha$, and hence inhabits the type $\forall \alpha:Type, \alpha\to\alpha$.

This sort of impredicativism can be shown to be incompatible with impredicative set-theoretic axioms such as power sets; see [this paper](https://www.cl.cam.ac.uk/~amp12/papers/nontpt/nontpt.pdf) of Andy Pitts.  Since such type theories generally do have function types, it follows that they cannot be classical.


## The category of sets

So what is the category of sets in predicative mathematics?

At bottom, let us suppose that $Set$ is a [[Heyting category|Heyting]] [[pretopos]]; this is a category whose [[internal logic]] is first-order and contains only constructions that don\'t require any of the above axioms.

Since we\'re not doing finite mathematics, we may also include a [[natural numbers object]].  In fact, we could include more general [[inductive type]]s, since these are no harder to justify philosophically than $\mathbf{N}$, although the proofs that these exist if $\mathbf{N}$ does rely on possibly impredicative axioms.  Then $Set$ is a Heyting $W$-pretopos.

If you accept function sets, then $Set$ is [[locally cartesian closed category|locally cartesian closed]] and thus a $\Pi$-pretopos.  In this case, $\mathbf{N}$ is enough to get all $W$-[[W-type|types]], so we have a $\Pi$-$W$-pretopos.  If you accept excluded middle, then $Set$ is a [[Boolean category|Boolean]] pretopos or even a Boolean $W$-pretopos.  But a Boolean $\Pi$-pretopos is necessarily a [[topos]], which would make the theory impredicative.

However, $Set$ is still a [[Grothendieck topos]], defined as a category of sheaves or in terms of Giraud\'s characterisation.  We require the existence of power sets to prove the theorem that such a category is an elementary topos, so predicatively a Grothendieck topos may not be an elementary topos at all.


## The real numbers

An important question in predicative mathematics is the status of the set $\mathbf{R}$ of [[real number]]s.  This set is often constructed as a subset $R_D$ of $\mathcal{P}\mathbf{N}$ or as a [[subquotient]] $R_C$ of $\mathbf{N}^{\mathbf{N}}$, neither of which can be formed in an arbitrary Heyting $W$-pretopos.  The latter can be formed in a $\Pi$-$W$-pretopos, but it is not necessarily correct.

The constructive school of predicativism can construct $\mathbf{R}$ in various ways. One method is to use $R_C$ directly, but this will only go so far unless something is done to prove that it is Dedekind-complete. This will follow from [[weak countable choice]] ($WCC$), which is accepted by most constructive schools.  Using [[subset collection]], a variation on $R_C$ is possible which can be proved Dedekind-complete *without* $WCC$.

However, not all constructive predicative mathematics accept [[subset collection]] or [[weak countable choice]]. Another method is to use a predicative version of $R_D$, where given a [[sigma-frame|$\sigma$-frame]] $\Sigma$, $\Sigma$-[[Dedekind cuts]] are defined as pairs of functions $L, U$ from the [[rational numbers]] $\mathbb{Q}$ to $\Sigma$, which represent the open subsets of $\mathbb{Q}$, rather than pairs of functions into the class of propositions. $R_D$ is defined as the set of all $\Sigma$-Dedekind cuts, or as the [[sigma-Dedekind complete|$\Sigma$-Dedekind complete]] [[archimedean field]]. This will ensure that the set of real numbers is a set rather than a [[proper class]], at the cost of Dedekind completeness, which always results in a proper class in constructive predicative mathematics. Nevertheless, a significant portion of [[real analysis]] could be developed using this approach, such as [[differential calculus]], [[integral calculus]], and [[differential geometry]].

It is also possible to assert the existence of $\mathbf{R}$ by fiat, much like $\mathbf{N}$ exists by the axiom of infinity.  This is the approach taken by the classical school; they use $\mathcal{P}\mathbf{N}$ instead of $\mathbf{R}$ directly, but these are isomorphic by excluded middle.  This is natural from the perspective of predicative set theory as a weak form of higher-order logic; you assert the existence of $\mathbf{N}$, $\mathcal{P}\mathbf{N}$, and maybe $\mathcal{P}\mathcal{P}\mathbf{N}$, then stop. 

One could also assert $\mathbf{R}$ by fiat via the [[universal property]] of the real numbers as the [[terminal object|terminal]] [[Archimedean ordered field]]. From this characterization, the real numbers are a [[terminal coalgebra]] of the [[identity functor|identity endofunctor]] $X \mapsto X$ on the [[category]] of [[Archimedean ordered fields]], and in a sense is impredicative, since coinductively defined sets are impredicative. 

If [[quotient sets]] exist and [[sequence algebras]] of Archimedean ordered fields exist, then it is provable that $\mathbf{R}$ is Cauchy complete. From the definition of terminal object, $\mathbf{R}$ is an algebra of the endofunctor $X \mapsto \mathcal{C}(X)$ in the category of Archimedean ordered fields which takes Archimedean ordered fields $X$ to the Archimedean ordered field $\mathcal{C}(X)$ of equivalence classes of Cauchy sequences in $X$. Every algebra of the endofunctor $X \mapsto \mathcal{C}(X)$ in the category of Archimedean ordered fields is a Cauchy complete Archimedean ordered field. 

Similarly, if [[power sets]] of Archimedean ordered fields exist, then it is provable that $\mathbf{R}$ is Dedekind complete. From the definition of terminal object, $\mathbf{R}$ is an algebra of the endofunctor $X \mapsto \mathcal{D}(X)$ in the category of Archimedean ordered fields which takes Archimedean ordered fields $X$ to the Archimedean ordered field $\mathcal{C}(X)$ of two-sided Dedekind cuts in $X$. Every algebra of the endofunctor $X \mapsto \mathcal{D}(X)$ in the category of Archimedean ordered fields is a Dedekind complete Archimedean ordered field. 

There is also the question of what exactly it means to say that $\mathbf{R}$ exists; is it a set or a [[proper class]]? Without function sets, the distinction between these is not clear-cut; higher-order logic suggests a hierarchy of more and more proper (less and less [[small category|small]]) classes rather than a single unified notion of set and class, which is similar to the concept of a [[universe in a topos]] for impredicative set theory. If you allow $\mathbf{R}$ only as a proper class, then you are doing predicative mathematics so long as you don't have [[power classes]], if you allow $\mathbf{R}$ as a set, then as long as you don't allow all [[power sets]] or [[power classes]], you are still doing predicative mathematics in the same sense that foundations in which only the [[limited principle of omniscience]] holds but not full [[excluded middle]] is still constructive mathematics. 

## Formalising mathematics

How much of mathematics can be done predicatively?

A surprisingly large amount of mathematics can be formalised, using various coding tricks, in a theory in which $\mathbf{N}$ is a set but $\mathcal{P}\mathbf{N}$ is a proper class.  This is somewhat easier in [[Nik Weaver]]\'s 'conceptualist' approach, which accepts $\mathcal{P}\mathcal{P}\mathbf{N}$ as a proper class (so that $\mathcal{P}N$ and $\mathbb{R}$ are small); the encoding is not really more complicated than what is usually done in [[material set theory]] for ordered pairs and the like.  Note that these are conservative over [[Peano arithmetic]] ($PA$); that is, anything expressible in $PA$ and provable in these systems is provable in $PA$ (which certainly cannot be said of [[ZFC]] or [[ETCS]], which prove the consistency of $PA$).

Constructive mathematics generally requires great care with anything after the middle of the 19th century other than basic [[discrete mathematics]], but requiring it to be predicative does not usually add much difficulty, as long as function sets are allowed.  This even extends to [[category theory]], which is not usually contemplated in the classical approach.  (However, the internal logic of a $\Pi$-$W$-pretopos is certainly not conservative over $PA$; it already proves consistency of the latter.)


## Related concepts

* [[predicative topos]]


## References

*  [[Solomon Feferman]]; [Relationships between Constructive, Predicative and Classical Systems of Analysis](http://hlombardi.free.fr/FefermanRelationships.pdf) (PDF).

*  Nik Weaver; [papers on conceptualism](https://web.archive.org/web/20100616093000/https://www.math.wustl.edu/~nweaver/conceptualism.html).

*  from the Standford Encyclopedia of Philosophy:
   *  [Predicativity in constructive set theory](http://plato.stanford.edu/entries/set-theory-constructive/#PreConSetThe).
   *  [Predicativism](http://plato.stanford.edu/entries/philosophy-mathematics/index.html#Pre)

Discussion of [[predicative toposes]] is in 

* [[Ieke Moerdijk]], [[Erik Palmgren]], _Type theories, toposes and constructive set theory: predicative aspects of [[algebraic set theory]]_ Ann. Pure Appl. Logic, 114(1-3):155&#8211;201, 2002

* [[Benno van den Berg]], _Predicative toposes_ ([arXiv:1207.0959](http://arxiv.org/abs/1207.0959))
 {#vdBerg}

Constructive predicative definitions of the real numbers are discussed in

*  [[Paul Taylor]]\'s [page on Dedekind cuts](http://www.paultaylor.eu/ASD/dedras/classical)

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

## Discussion

A discussion was had on this page, now [archived at the nForum](https://nforum.ncatlab.org/discussion/15265/predicative-mathematics/?Focus=103587#Comment_103587)

[[!redirects weakly predicative]]
[[!redirects weakly predicative mathematics]]

[[!redirects strongly predicative]]
[[!redirects strongly predicative mathematics]]

[[!redirects predicative mathematics]]
[[!redirects predicative logic]]
[[!redirects predicativism]]

[[!redirects impredicative mathematics]]
[[!redirects impredicative logic]]

[[!redirects predicative]]
[[!redirects impredicative]]

[[!redirects predicativity]]
[[!redirects impredicativity]]
