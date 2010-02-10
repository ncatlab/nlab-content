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

category: foundational axiom
