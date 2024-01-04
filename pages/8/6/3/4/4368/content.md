

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

* table of contents
{: toc}


## The idea

**Gabriel--Ulmer duality** says that there is an [[equivalence of categories|equivalence]] of [[2-categories]] (or in other words, a [[biequivalence]]) 

$$ 
\begin{matrix}
Lex^{op} & \to &  LFP \\
  C      & \mapsto & Lex(C, Set) 
\end{matrix}
$$

where [[Lex]] is the 2-category of:

* small [[finitely complete categories]], 

* [[finite limit]]$\:$ [[preserved limit|preserving]] [[functors]], and 

* [[natural transformations]], 

and LFP is the 2-category of 

* [[locally finitely presentable categories]], 

* finitary [[right adjoint|right]] [[adjoint functors]] and 

* [[natural transformations]].

The idea is that an object $C \in Lex$ can be thought of as an [[essentially algebraic theory]], which has a category of [[model|models]] $Lex(C,Set)$.  Gabriel--Ulmer duality says that this category of models is locally finitely presentable, all LFP categories arise in this way, and we can recover the theory $C$ from its category of models. There are similar dualities for other classes of theory such as [[regular theories]]. 

A version of Gabriel--Ulmer duality for [[enriched category theory]] was proved by [[Max Kelly]] (see [LackTendas](#LackTendas)). Let $\mathcal{V}$ be a symmetric monoidal closed complete and cocomplete category which is locally finitely presentable as a closed category. Then let $\mathcal{V}$-$Lex$ be the 2-category of finitely complete $\mathcal{V}$-categories ($\mathcal{V}$-categories with finite weighted limits), finite limit preserving $\mathcal{V}$-functors, and $\mathcal{V}$-natural transformations, and $\mathcal{V}$-$LFP$ the 2-category of locally finitely presentable $\mathcal{V}$-categories, right adjoint $\mathcal{V}$-functors that preserve filtered colimits, and $\mathcal{V}$-natural transformations. Then there is a biequivalence
$$ 
\begin{matrix}
\mathcal{V}-Lex^{op} & \to &  \mathcal{V}-LFP \\
  C      & \mapsto & Lex(C, \mathcal{V}). 
\end{matrix}
$$

For instance, in the [[truth value]]-enriched case, the duality is between [[meet semilattices]] and [[algebraic lattices]]. 

Gabriel-Ulmer duality is a duality exhibited by the 2-[[Chu construction]], $Chu(Cat,Set)$.

## References

The original source is:

* [[Peter Gabriel]], [[Friedrich Ulmer]], _Lokal Praesentierbare Kategorien_, Springer Lecture Notes in Mathematics **221**, Berlin, 1971. 

A careful discussion and proof of the biequivalence is in

* [[Jiri Adamek]], Hans-Eberhard Porst, _Algebraic Theories of Quasivarieties_ ,  J. Algebra **208** (1998) pp.379-398.

Some other general treatments of Gabriel-Ulmer duality (and generalizations to other [[doctrine|doctrines]]):

* C. Centazzo, [[E. M. Vitale]], _A duality relative to a limit doctrine_, Theory and Appl. of Categories __10__, No. 20, 2002, 486&#8211;497, [pdf](http://www.tac.mta.ca/tac/volumes/10/20/10-20.pdf)

* [[Stephen Lack]], [[John Power]], _Gabriel--Ulmer duality and Lawvere Theories enriched over a general base_, [pdf](http://maths.mq.edu.au/~slack/papers/jfp.pdf)

* [[M. Makkai]], [[A. Pitts]], _Some results on locally finitely presentable categories_, Trans. Amer. Math. Soc. __299__ (1987), 473-496, [MR88a:03162](http://www.ams.org/mathscinet-getitem?mr=869216), [doi](http://dx.doi.org/10.2307/2000508), [pdf](http://www.ams.org/journals/tran/1987-299-02/S0002-9947-1987-0869216-2/S0002-9947-1987-0869216-2.pdf)

For a 2-dimensional analogue see the slides from a 2010 talk by Makkai: [pdf](http://www.math.mcgill.ca/makkai/scans/2010Washington0001.pdf)

A formal-categorical account using [[KZ-doctrines]] can be found in

* {#DL18} [[Ivan Di Liberti]], [[Fosco Loregian]], _Accessibility and Presentability in 2-Categories_, Journal of Pure and Applied Algebra 227.1 (2023)([arXiv:1804.08710](https://arxiv.org/abs/1804.08710))

For a discussion of Gabriel--Ulmer duality and related dualities in the context of [[enriched category theory]] see 

* {#LackTendas} [[Stephen Lack]], [[Giacomo Tendas]], _Enriched regular theories_, J. Pure Appl. Alg. __226__, n. 6 (2020) 106268, ([arXiv:1907.02301](https://arxiv.org/abs/1907.02301), [doi:10.1016/j.jpaa.2019.106268](https://doi.org/10.1016/j.jpaa.2019.106268))

This discusses (see Theorem 2.1) Kelly's original result for $V$-[[enriched categories]], where $V$ is a closed symmetric monoidal category whose underlying category $V_0$ is locally small, complete and cocomplete, in section 9 (cf. theorem 9.8) of

* [[Max Kelly]], _Structures defined by finite limits in the enriched context_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle cat&#233;goriques, **23** no. 1 (1982), pp. 3-42, [MR648793](http://www.ams.org/mathscinet-getitem?mr=648793),[numdam](http://www.numdam.org/item?id=CTGDC_1982__23_1_3_0)

For an extension of Gabriel--Ulmer duality to a duality between [[Cauchy-complete]] [[clans]] and [[locally finitely presentable categories]] equipped with a well-behaved kind of [[weak factorization system]] see

* [[Jonas Frey]], _Duality for Clans: a Refinement of Gabriel-Ulmer Duality_ ([arXiv:2308.11967](https://arxiv.org/abs/2308.11967))

For a connection to [[Tannaka duality]] theory see

* nCaf&eacute; discussion [here](http://golem.ph.utexas.edu/category/2011/07/doctrinal_and_tannakian_recons.html)

* [[Brian Day]], _Enriched Tannaka duality_, JPAA __108__ (1996) pp.17-22, [MR97d:18008](http://www.ams.org/mathscinet-getitem?mr=1382240) <a href="http://dx.doi.org/10.1016/0022-4049(95)00039-9">doi</a>

For a discussion of an $\infty$-version of Gabriel-Ulmer duality between finitely complete and idempotent complete $(\infty, 1)$-categories and locally finitely presentable $(\infty, 1)$-categories see this [MO discussion](https://mathoverflow.net/q/293031/447).



[[!redirects Gabriel-Ulmer duality]]
[[!redirects Gabriel–Ulmer duality]]
[[!redirects Gabriel--Ulmer duality]]
