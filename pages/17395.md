# Relevance logics

* table of contents
{:toc}

## Idea

**Relevance logics**, also known as **relevant logics**, are non-[[classical logics]] designed to avoid what some consider to be paradoxical about classical [[implication]].  In particular, certain hypothetical propositions in which antecedent and consequent are irrelevant to one another occur as [[tautologies]] in [[classical logic]], whereas one might consider that a claim that '$P$ implies $Q$' suggests that the truth of $P$ gives us reason to accept the truth of $Q$.

## General description

There are a number of logics that have been considered in the context of "relevance".  Many of them can, at least roughly, be regarded as [[substructural logics]] like [[linear logic]].  Unlike linear logic, most relevance logics permit the [[contraction rule]], but not the [[weakening rule]].  Thus in a sense they are the "dual" of [[affine logic]] which permits weakening but not contraction.

Generally speaking, most relevance logics contain the following [[logical connectives]]:

* A [[logical conjunction]] and a [[logical disjunction]], usually written $\wedge$ and $\vee$.  These are *additive* connectives, like those written $\&$ and $\oplus$ in linear logic.
* An [[implication]], usually written $\to$.  This is a *multiplicative* or *intensional* connective, like the [[linear implication]] $\multimap$ of linear logic.
* A [[negation]], often written $\sim$ but sometimes $\neg$.  This is also a multiplicative/intensional connective.  Most relevance logics are "multiplicatively classical" in that the [[double negation law]] $\sim\sim A\to A$ holds.  It follows that $\wedge$ and $\vee$ satisfy all the [[de Morgan laws]] with respect to $\sim$.

Other connectives that sometimes appear in relevance logics include:

* A [[biconditional]] $A\leftrightarrow B$, usually defined as $(A\to B) \wedge (B\to A)$, combining the multiplicative implications with the additive conjunction.
* A multiplicative [[truth]], like linear logic's $\mathbf{1}$.  This can be defined as $A\to A$.
* An additive truth and an additive falsity, like linear logic's $\top$ and $\mathbf{0}$.  There does not appear to be any consensus in the relevance logic community on the notations for the nullary connectives, so on this page we will use the linear logic notations.
* A [[multiplicative conjunction]] like linear logic's $\otimes$, usually called *fusion* or *cotenability* and denoted by $\circ$ or $*$.  Assuming multiplicative classicality, this is definable from the relevant implication as $\sim (A\to\sim B)$.  It can also be characterized as an adjoint to $\to$, that is $A\circ B \to C$ if and only if $A\to (B\to C)$.
* More rarely, a [[multiplicative disjunction]] like linear logic's $\invamp$, sometimes called *fission* (but for which there does not seem to be a standard notation).  This is also classically definable from $\to$ as $\sim A \to B$.  Note that multiplicative DNE $\sim\sim A\to A$ is then equivalent to multiplicative [[excluded middle]] $A\invamp \sim A$.  The multiplicative falsity (linear logic $\bot$) seems to be rarely mentioned.
* Also rarely (and apparently controversially), an additive negation $\neg$, which might be "additively classical" in the sense that $A\vee \neg A$.
* A [[modal operator]] $\Box$ akin to [[necessity]].  The operation $\top \to A$ also sometimes behaves like necessity (note the mismatch of the additive $\top$ with the multiplicative $\to$).

This description may give the impression that relevance logics could be obtained from linear logic by adding contraction and perhaps removing some undesired connectives.  This is close to true, but many relevance logics have additional features that this would not capture.  One notable one is that the [[additive conjunction]] still [[distributive lattice|distributes]] over the [[additive disjunction]]:
$$ A \wedge (B\vee C) \leftrightarrow (A\wedge B) \vee (A\wedge C) $$
although this is not true in linear logic, and simply adding contraction does not make it true.  (It is true linearly --- and relevance-ly --- that the multiplicative conjunction distributes over additive disjunction, but adding contraction does not collapse the two conjunctions.)  It can of course be added as an [[axiom]], but it is often better to give a modified [[sequent calculus]] that makes it true automatically, by using [[bunches]].  One such sequent calculus can be found in ([Mints](#Mints)); see also [[bunched logic]] and [[display logic]].

Some relevance logics also do without contraction.  This has been found particularly helpful in making them [[paraconsistent logic|paraconsistent/nontrivial]] even in the presence of things like the [[comprehension rule]] of [[naive set theory]].

## Some relevance logics

Historically, relevance logics have usually been formulated first as [[Hilbert systems]], and only later have equivalent [[sequent calculus]] and [[natural deduction]] systems been found.

### The logic R

The logic R+ ("**positive R**") contains $\wedge,\vee,\to$ only, with contraction and the distributive law.  Fusion $\circ$ is sometimes added, since it can be characterized as an adjoint to $\to$, and likewise the nullary connectives.  This logic can be formalized by a [[sequent calculus]] with [[bunches]] on the left whose [[structural connectives]] represent $\wedge$ and $\circ$, and single formulas on the right; see ([Mints](#Mints)).

The logic R adds to R+ a multiplicative classical negation $\sim$.  It is not clear whether it has a good sequent calculus, although if we also include an additive classical negation $\neg$ (which can be shown to be a conservative extension) then it can be represented in [[display logic]].  It is also similar to "classical [[bunched implication]]" with contraction added, in which case it may be easier to omit the additive negation.   For a [[Hilbert system]], see [SEP](http://plato.stanford.edu/entries/logic-relevance/logicr.html).

## Categorical semantics

Just as linear logic (with the [[exchange rule]], but not contraction or weakening) has semantics in [[symmetric monoidal categories]], and ordinary logic has semantics in [[cartesian monoidal categories]] (both perhaps with extra structure, such as being [[closed monoidal category|closed]] or [[star-autonomous category|star-autonomous]]), affine logic has semantics in [[semicartesian monoidal categories]] while relevance logics (with contraction) have semantics in [[relevance monoidal categories]].  The monoidal product represents the [[multiplicative conjunction]]; of course, the other connectives then have to be added in an appropriately related way.

##Related concepts

* [[linear logic]]
* [[bunched logic]]
* Some relevance logics are also [[paraconsistent logic|paraconsistent]].

##References

* [Stanford Encyclopedia of Philosophy](http://plato.stanford.edu/entries/logic-relevance/)

* G. E. Mints. Cut-elimination theorem for relevant logics, Zap. Nauchn. Sem. LOMI, 1972,	Volume 32, Pages 90&#8211;97. ([math-net.ru](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=znsl&paperid=2569&option_lang=eng)).
An English translation appears in the Journal of Soviet Mathematics 6 (1976) pp.422-8. ([doi](http://doi.org/10.1007/BF01084083))
 {#Mints}

* Peter W. O'Hearn and David J. Pym. The Logic of Bunched Implications. _Bulletin of Symbolic Logic_ 5(2):215-244. ([pdf](http://www.lsv.ens-cachan.fr/~demri/OHearnPym99.pdf)) ([doi](https://dx.doi.org/10.2307%2F421090))

* Stephen Read, _Relevant Logic: A Philosophical Examination of Inference_, 2012, ([pdf](https://www.st-andrews.ac.uk/~slr/Relevant_Logic.pdf))


[[!redirects relevance logics]]
[[!redirects relevant logic]]
[[!redirects relevant logics]]
