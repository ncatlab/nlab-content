The assumption that **Surjection-slices Of Set Have Weakly Initial Sets**, or SOSHWIS, is a weak form of the [[axiom of choice]].  Like the [[axiom of multiple choice]] and the axiom of [[small violations of choice]] (which both imply it), it says intuitively that "AC fails to hold only in a small way" (i.e. not in a [[proper class|proper-class]] way).

+--{: .query}
[[Mike Shulman]]: I think SOSHWIS is a terrible name, but I didn't want to not create this page because I couldn't think of a good name for it.
=--

## Statement

Precisely, SOSHWIS is the statement that for any set $X$, the full subcategory $(Set/X)_{surj}$ of the [[slice category]] $Set/X$ consisting of the [[surjections]] has a [[weakly initial set]].  In other words, there is a family of surjections $\{f_i\colon P_i \twoheadrightarrow X\}_{i\in I}$ such that for any surjection $Q\twoheadrightarrow X$, there exists some $f_i$ which factors through $Q$.

## Relationships to other axioms

* SOSHWIS is implied by [[COSHEP]], since any surjection $P\twoheadrightarrow X$ such that $P$ is projective is necessarily a weakly initial (singleton) set in $(Set/X)_{surj}$.

* SOSHWIS is also implied by the [[axiom of multiple choice]] (which is in turn implied by COSHEP).  For if $X$ is in some collection family $\{D_c\}_{c\in C}$, then the family of all surjections of the form $D_c \twoheadrightarrow X$ is weakly initial in $(Set/X)_{surj}$.

* Since Rathjen proves that [[SVC]] implies [[AMC]] (at least in [[ZF]]), SVC therefore also implies SOSHWIS.

* SOSHWIS also follows from the assertion that the [[free exact completion]] of $Set$ is [[well-powered category|well-powered]], which in turn follows from assertion that $Set$ has a [[generic proof]] (so that $Set_{ex/lex}$ is a [[topos]]).  Both of these can also be regarded as saying that choice is only violated "in a small way."

* SOSHWIS implies that the category of [[anafunctors]] between any two [[small categories]] is [[essentially small category|essentially small]]; see [here](/nlab/show/anafunctor#SizeQuestions).


## In other sites

Let $(C,J)$ be a [[site]] with a singleton Grothendieck pretopology $J$. It makes sense to consider a version of SOSHWIS for $(C,J)$, along the lines of the following: Let $C/_{cov}a$ be the full subcategory of the slice category $C/a$ consisting of the covers. Internal SOSHWIS is then

* For all objects $a$ of $C$, $C/_{cov}a$ has a weakly initial set.

For example, assuming SOSHWIS for $Set$, the category $Top$ with any of its usual pretopologies satisfies \'internal SOSHWIS\'.

+--{: .query}
[[David Roberts]]: I propose the name Weakly Initial Set of Covers (WISC) for the general case, and a fortiori to the case of $Set$.
=--

More generally, for a non-singleton pretopology on $C$, we can reformulate SOSHWIS/WISC along the lines of \'there is a set of covering families weakly initial in the category of all covering families of any object\'. ([[David Roberts]]: obviously this needs to be written better, and in a nicer format. Perhaps it needs it own page.)

Given a site $(C,J)$ with $J$ subcanonical, and $C$ finitely complete, we can define a (weak) 2-category $Ana(C,J)$ of internal categories, anafunctors and transformations. If WISC holds for $(C,J)$, $Ana(C,J)$ is locally essentially small.

category: foundational axiom
