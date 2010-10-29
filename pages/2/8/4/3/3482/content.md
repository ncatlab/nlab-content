
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--



# Contents

* toc
{: toc}

The assumption that every set has a **Weakly Initial Set of Covers**, or WISC, is a weak form of the [[axiom of choice]].  Like the [[axiom of multiple choice]] and the axiom of [[small violations of choice]] (which both imply it), it says intuitively that "AC fails to hold only in a small way" (i.e. not in a [[proper class|proper-class]] way).

## Statement (for Sets)

Precisely, WISC is the statement that for any set $X$, the full subcategory $(Set/X)_{surj}$ of the [[slice category]] $Set/X$ consisting of the [[surjections]] has a [[weakly initial set]].  In other words, there is a family of surjections $\{f_i\colon P_i \twoheadrightarrow X\}_{i\in I}$ such that for any surjection $Q\twoheadrightarrow X$, there exists some $f_i$ which factors through $Q$.

## Relationships to other axioms

* WISC is implied by [[COSHEP]], since any surjection $P\twoheadrightarrow X$ such that $P$ is projective is necessarily a weakly initial (singleton) set in $(Set/X)_{surj}$.

* WISC is also implied by the [[axiom of multiple choice]] (which is in turn implied by COSHEP).  For if $X$ is in some collection family $\{D_c\}_{c\in C}$, then the family of all surjections of the form $D_c \twoheadrightarrow X$ is weakly initial in $(Set/X)_{surj}$.

* Since Rathjen proves that [[SVC]] implies [[AMC]] (at least in [[ZF]]), SVC therefore also implies WISC.

* WISC also follows from the assertion that the [[free exact completion]] of $Set$ is [[well-powered category|well-powered]], which in turn follows from assertion that $Set$ has a [[generic proof]] (so that $Set_{ex/lex}$ is a [[topos]]).  Both of these can also be regarded as saying that choice is only violated "in a small way."

* WISC implies that the category of [[anafunctors]] between any two [[small categories]] is [[essentially small category|essentially small]]; see [here](/nlab/show/anafunctor#SizeQuestions).


## In other sites

Let $(C,J)$ be a [[site]] with a singleton [[Grothendieck pretopology]] $J$. It makes sense to consider a version of WISC for $(C,J)$, along the lines of the following: Let $C/_{cov}a$ be the full subcategory of the slice category $C/a$ consisting of the covers. Internal WISC then states that

* For all objects $a$ of $C$, $C/_{cov}a$ has a weakly initial set.

+-- {: .un_example}
###### Example
Assuming WISC for $Set$, the category $Top$ with any of its usual pretopologies satisfies \'internal WISC\'.  Consider, for instance, the pretopology in which the covers are the maps admitting local sections, i.e. those $p\colon Y\to X$ such that for any $x\in X$ there exist an open set $U\ni x$ such that $p^{-1}(U)\to U$ is split epic.  If $Set$ satisfies AC, then a weakly initial set in $Top/_{cov}X$ is given by the set of all maps $\coprod_{U\in \mathcal{U}} U \to X$ where $\mathcal{U}\subset \mathcal{P}(X)$ is an open cover of $X$.  For if $p\colon Y\to X$ admits local sections, then for each $x\in X$ we can choose an $U_x \ni x$ over which $p$ has a section, resulting in an open cover $\mathcal{U} = \{U_x \mid x\in X\}$ of $X$ for which $\coprod_{U\in \mathcal{U}} U \to X$ factors through $p$.  (If $Set$ merely satisfies WISC itself, then a more involved argument is required.)
=--

More generally, for a non-singleton pretopology on $C$, we can reformulate WISC along the lines of \'there is a set of covering families weakly initial in the category of all covering families of any object\'.

Given a site $(C,J)$ with $J$ subcanonical, and $C$ finitely complete, we can define a (weak) 2-category $Ana(C,J)$ of internal categories, anafunctors and transformations. If WISC holds for $(C,J)$, then $Ana(C,J)$ is locally essentially small.

category: foundational axiom
