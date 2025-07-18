
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The assumption that every [[set]] has a **Weakly Initial Set of Covers**, or $WISC$, is a weak form of the [[axiom of choice]].  Like the [[axiom of multiple choice]] and the axiom of [[small violations of choice]] (which both imply it), it says intuitively that "$AC$ fails to hold only in a small way" (i.e. not in a [[proper class|proper-class]] way).


## Statement (for Sets)

Precisely, $WISC$ is the statement that for any [[set]] $X$, the [[full subcategory]] $(Set/X)_{surj}$ of the [[slice category]] $Set/X$ consisting of the [[surjections]] has a [[weakly initial set]].  In other words, there is a family of surjections $\{f_i\colon P_i \twoheadrightarrow X\}_{i\in I}$ such that for any surjection $Q\twoheadrightarrow X$, there exists some $f_i$ which factors through $Q$.


## Relationships to other axioms

* WISC is implied by [[COSHEP]], since any surjection $P\twoheadrightarrow X$ such that $P$ is projective is necessarily a weakly initial (singleton) set in $(Set/X)_{surj}$.

* WISC is also implied by the [[axiom of multiple choice]] (which is in turn implied by COSHEP).  For if $X$ is in some collection family $\{D_c\}_{c\in C}$, then the family of all surjections of the form $D_c \twoheadrightarrow X$ is weakly initial in $(Set/X)_{surj}$.

* A [[ΠW-pretopos]] satisfying WISC is a _[[predicative topos]]_.

* Since [[Michael Rathjen]] proves that [[SVC]] implies [[AMC]] (at least in [[ZF]]), SVC therefore also implies WISC.

* WISC also follows from the assertion that the [[free exact completion]] of $Set$ is [[well-powered category|well-powered]], which in turn follows from assertion that $Set$ has a [[generic proof]] (so that $Set_{ex/lex}$ is a [[topos]]).  Both of these can also be regarded as saying that choice is only violated "in a small way."

* WISC implies that the category of [[anafunctors]] between any two [[small categories]] is [[essentially small category|essentially small]]; see [here](/nlab/show/anafunctor#SizeQuestions), or below.

* WISC implies (in [[ZF]]) that there exist arbitrarily large [[regular cardinals]].  Therefore, WISC is not provable in ZF, as Moti Gitik constructed a model of ZF with only one regular cardinal, using large cardinal assumptions. A proof without large cardinals was given in  ([Karagila](#Karagila14)).


### Applications

#### Local smallness of anafunctor categories

+-- {: .num_prop} 
######Proposition
WISC implies the local essential smallness of $Cat_ana$, the bicategory of categories and [[anafunctors]].
=-- 

+-- {: .proof} 
######Proof 
Let $X,Y$ be small categories and consider the category $Cat_{ana}(X,Y)$, with objects which are spans
$$
(j,f) : X \stackrel{j}{\leftarrow} X[U] \stackrel{f}{\to} Y
$$
where $X[U] \to X$ is a surjective-on-objects, [[fully faithful]] functor. The underlying map on object sets is $U \to X_0$. By WISC there is a surjection $V \to X_0$ and a map $V\to U$ over $X_0$. We can thus define a commuting triangle of functors
$$
  \array{ 
    X[V] &  \to  &  X[U]    \\ 
    & k \searrow & \downarrow j\\ 
    && X 
  }
$$
where $X[V] \to X$ is the canonical fully faithful functor arising from $V\to X_0$ (the arrows of $X[V]$ are given by $V^2 \times_{X_0^2} X_1$). This gives rise to a transformation from $(j,f)$ to a span with left leg $k$. Thus $Cat_{ana}(X,Y)$ is equivalent to the [[full subcategory]] of anafunctors where the left leg has as object component an element of the weakly initial set of surjections. Since there is only a set of functors $X[V] \to Y$ for each $V\to X_0$, this subcategory is small.
=--

#### Existence of higher inductive types

[Swan](#Swan18) showed that WISC implies the existence of [[W-types with reductions]], a kind of simple [[higher inductive type]].


## In other sites - external version

Let $(C,J)$ be a [[site]] with a singleton [[Grothendieck pretopology]] $J$. It makes sense to consider a version of WISC for $(C,J)$, along the lines of the following: Let $(C/a)_{cov}$ be the full subcategory of the slice category $C/a$ consisting of the covers. WISC then states that

* For all objects $a$ of $C$, $(C/a)_{cov}$ has a weakly initial set.

This definition is called _external_ because it refers to an external category of sets. This is to be contrasted with the _internal_ version of WISC, discussed below.

+-- {: .num_example}
###### Example
Assuming AC for $Set$, the category $Top$ with any of its usual pretopologies satisfies \'internal WISC\'.  Consider, for instance, the pretopology in which the covers are the maps admitting local sections, i.e. those $p\colon Y\to X$ such that for any $x\in X$ there exist an open set $U\ni x$ such that $p^{-1}(U)\to U$ is split epic.  If $Set$ satisfies AC, then a weakly initial set in $Top/_{cov}X$ is given by the set of all maps $\coprod_{U\in \mathcal{U}} U \to X$ where $\mathcal{U}\subset \mathcal{P}(X)$ is an open cover of $X$.  For if $p\colon Y\to X$ admits local sections, then for each $x\in X$ we can choose an $U_x \ni x$ over which $p$ has a section, resulting in an open cover $\mathcal{U} = \{U_x \mid x\in X\}$ of $X$ for which $\coprod_{U\in \mathcal{U}} U \to X$ factors through $p$.  (If $Set$ merely satisfies WISC itself, then a more involved argument is required.)
=--

And now a non-example

+-- {: .num_example}
###### Example
The category of [[affine schemes]] can be equipped with the [[fpqc topology]] (so this is the [[fpqc site]] over $Spec(\mathbb{Z})$). This does not satisfy WISC. Namely, given any set of fpqc covers of $Spec(R)$, there is a surjective fpqc map which is refined by none of the given covering families ([Stacks Project Tag 0BBK](#Stacks0BBK)).
=--

More generally, for a non-singleton pretopology on $C$, we can reformulate WISC along the lines of \'there is a set of covering families weakly initial in the category of all covering families of any object\'.

Given a site $(C,J)$ with $J$ subcanonical, and $C$ finitely complete, we can define a (weak) 2-category $Ana(C,J)$ of internal categories, anafunctors and transformations. If WISC holds for $(C,J)$, then $Ana(C,J)$ is locally essentially small.


## In other categories - internal version

To consider an _internal_ version of WISC, which doesn't refer to an external notion of set, one needs to assume that the ambient category $C$ has a strong enough [[internal logic]], such as a pretopos (this is the context in which van den Berg and Moerdijk work). Then the ordinary statement of WISC in set can be written in the internal logic, using the [[stack semantics]], as a statement about the objects and arrows of $C$. It is in this form that WISC is useful as a replacement choice principle in intuitionistic, constructive or predicative set theory, as these are modelled on various topos-like categories (or in the case of [van den Berg and Moerdijk](#vdBM12), a [[algebraic set theory|category of classes]], although this is not necessary for the approach).

Importantly, the internal form of WISC is stable under many more categorical constructions than other forms of choice.  For instance, any [[Grothendieck topos]] or [[realizability topos]] inherits WISC from its base topos of sets (even if the latter is constructive or even predicative); see [van den Berg](#vdBerg12).  This is in contrast to nearly all other choice principles, including weaker forms such as [[COSHEP]] and [[SVC]], which fail in at least some Grothendieck toposes even when the base is a model of ZFC.

## References
 {#References}

* {#vdBM12} [[Benno van den Berg]], [[Ieke Moerdijk]], *The Axiom of Multiple Choice and Models for Constructive Set Theory*, [arXiv](http://arxiv.org/abs/1204.4045).  In this paper WISC is called the "axiom of multiple choice".

* [[Thomas Streicher]], *Realizability Models for $CZF + \neg Pow$*, [unpublished note](http://www.mathematik.tu-darmstadt.de/~streicher/CIZF/rmczfnp.pdf).  In this note WISC is called $TTCA_f$ ($TTCA$ stands for "type-theoretic collection axiom).

* [[Benno van den Berg]], *WISC is independent from ZF*, [PDF](http://www.staff.science.uu.nl/~berg0002/papers/WISC.pdf)

* {#vdBerg12} [[Benno van den Berg]], _Predicative toposes_ ([arXiv:1207.0959](http://arxiv.org/abs/1207.0959)).  In this paper WISC is called the "axiom of multiple choice".

* {#Swan18} [[Andrew Swan]], *W-Types with Reductions and the Small Object Argument*, 2018, [arxiv:1802.07588](https://arxiv.org/abs/1802.07588)

The following two papers give models of set theory (without large cardinals) in which WISC fails.

* {#Karagila14} Asaf Karagila, *Embedding Orders Into Cardinals With $DC_\kappa$*, Fund. Math. 226 (2014), 143-156, doi:[10.4064/fm226-2-4](http://dx.doi.org/10.4064/fm226-2-4), [arXiv:1212.4396](http://arxiv.org/abs/1212.4396).
{#Karagila}

* {#Roberts15} [[David Michael Roberts]], _The weak choice principle WISC may fail in the category of sets_, [Studia Logica](http://link.springer.com/journal/11225) Volume 103 (2015) Issue 5, pp 1005-1017, doi:[10.1007/s11225-015-9603-6](http://dx.doi.org/10.1007/s11225-015-9603-6) [arXiv:1311.3074](http://arxiv.org/abs/1311.3074)


The Stacks Project shows how to construct a counterexample to WISC from any set of fpqc covers of an affine scheme.

* {#Stacks0BBK} [[The Stacks Project]], [Tag 0BBK](http://stacks.math.columbia.edu/tag/0BBK)



category: foundational axiom

[[!redirects WISC]]
[[!redirects WISCs]]
[[!redirects weakly initial set of covers]]
[[!redirects weakly initial sets of covers]]
[[!redirects axiom of weakly initial sets of covers]]

[[!redirects SOSHWIS]]