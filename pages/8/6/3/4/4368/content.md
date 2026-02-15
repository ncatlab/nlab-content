

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{: toc}


## The idea

### Plain case

**Gabriel--Ulmer duality** says that there is an [[biequivalence]] of [[2-categories]]  

$$ 
\begin{matrix}
Lex^{op} & \to &  LFP \\
  C      & \mapsto & Lex(C, Set) 
\end{matrix}
$$

where [[Lex]] is the 2-category of:

* [[small category|small]]$\:$ [[finitely complete categories]], 

* [[finite limit]]$\:$ [[preserved limit|preserving]] [[functors]], and 

* [[natural transformations]], 

and LFP is the 2-category of 

* [[locally finitely presentable categories]], 

* finitary [[right adjoint|right]] [[adjoint functors]] and 

* [[natural transformations]].

The idea is that an [[object]] $C \in Lex$ can be thought of as an [[essentially algebraic theory]], which has a category of [[model|models]] $Lex(C,Set)$.  
Gabriel--Ulmer duality says that this category of models is locally finitely presentable, all LFP categories arise in this way, and that we can recover the theory $C$ from its category of models. 

This duality may be exhibited as the 2-[[Chu construction]] $Chu(Cat,Set)$.

There are similar dualities for other classes of theory such as [[regular theories]]. 

### Enriched case

A version of Gabriel-Ulmer duality for [[enriched category theory]] was proved by [[Max Kelly]] (see [Lack & Tendas 2020](#LackTendas20)):

For [[base of enrichment]] $\mathcal{V}$ which is  a [[symmetric monoidal closed category]] which is [[complete and cocomplete category|complete and cocomplete]] and [[locally finitely presentable category|locally finitely presentable]] as a [[closed category]], consider:

1. $\mathcal{V}$-$Lex$ the 2-category of 

   * finitely complete [[enriched category|$\mathcal{V}$-categories]] ($\mathcal{V}$-categories with finite [[weighted limits]]), 

   * [[finite limit]] [[preserved limit|preserving]] [[enriched functor|$\mathcal{V}$-functors]], 

   * [[enriched natural transformation|$\mathcal{V}$-natural transformations]], 

1. $\mathcal{V}$-$LFP$ the 2-category of 

   * [[locally finitely presentable category|locally finitely presentable]] [[enriched category|$\mathcal{V}$-categories]],

   *  [[right adjoint|right]] [[enriched adjoint functor|adjoint $\mathcal{V}$-functors]] that preserve [[filtered colimits]],

   * [[enriched natural transformations|$\mathcal{V}$-natural transformations]]. 

Then there is a [[biequivalence]]
$$ 
  \begin{matrix}
    \mathcal{V}-Lex^{op} 
      & \longrightarrow&  
    \mathcal{V}-LFP 
    \\
    C & \mapsto & Lex(C, \mathcal{V})
    \,.
  \end{matrix}
$$

For instance, in the [[truth value]]-[[enriched category theory|enriched]] case, the duality is between [[meet semilattices]] and [[algebraic lattices]]. 

## References

The original source is:

* [[Peter Gabriel]], [[Friedrich Ulmer]], _Lokal präsentierbare Kategorien_, Lecture Notes in Mathematics **221**, Springer (1971) &lbrack;[doi:10.1007/BFb0059396](https://doi.org/10.1007/BFb0059396)&rbrack;

A careful discussion and proof of the biequivalence is in

* [[Jiří Adámek]], [[Hans-Eberhard Porst]], *Algebraic Theories of Quasivarieties*,  J. Algebra **208** (1998) 379-398 &lbrack;[doi:10.1006/jabr.1998.7499](https://doi.org/10.1006/jabr.1998.7499), [pdf](https://user.math.uni-bremen.de/porst/dvis/AlgTheocorr.pdf)&rbrack;

Some other general treatments of Gabriel-Ulmer duality (and generalizations to other [[doctrines]]):

* C. Centazzo, [[Enrico M. Vitale]], *A duality relative to a limit doctrine*, Theory and Appl. of Categories __10__ 20 (2002) 486-497 lbrack;[tac:10-20](http://www.tac.mta.ca/tac/volumes/10/20/10-20abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/10/20/10-20.pdf)&rbrack;

* [[Stephen Lack]], [[John Power]], _Gabriel-Ulmer duality and Lawvere Theories enriched over a general base_, Journal of Functional Programming **19** 3-4 (2009) 265-286 &lbrack;[doi:10.1017/S0956796809007254]( https://doi.org/10.1017/S0956796809007254), [pdf](https://web.archive.org/web/20210506214016/http://maths.mq.edu.au/~slack/papers/jfp.pdf)&rbrack;

* [[Michael Makkai]], [[Andrew Pitts]], *Some results on locally finitely presentable categories*, Trans. Amer. Math. Soc. **299** (1987) 473-496 &lbrack;[doi:10.2307/2000508](http://dx.doi.org/10.2307/2000508), [pdf](http://www.ams.org/journals/tran/1987-299-02/S0002-9947-1987-0869216-2/S0002-9947-1987-0869216-2.pdf), [MR88a:03162](http://www.ams.org/mathscinet-getitem?mr=869216)&rbrack;

Note that the above claims that Gabriel–Ulmer duality can be formulated as a 2-equivalence, rather than a biequivalence, but this is false, as clarified in:

* [[Jiřı́ Adámek]] and [[Hans-E. Porst]], _Algebraic theories of quasivarieties_, Journal of Algebra 208.2 (1998): 379-398.

A [[2-category theory|2-category theoretic]] analogue:

* [[Michael Makkai]], *Gabriel-Ulmer duality*, talk at ASL annual meeting (2010) &lbrack;scan: [pdf](http://www.math.mcgill.ca/makkai/scans/2010Washington0001.pdf), [[Makkai-GabrielUlmerDuality.pdf:file]]&rbrack;

A [[formal category theory|formal category theoretic]] account using [[KZ-doctrines]]:

* {#DL18} [[Ivan Di Liberti]], [[Fosco Loregian]], *Accessibility and Presentability in 2-Categories*, Journal of Pure and Applied Algebra **227** 1 (2023) &lbrack;[arXiv:1804.08710](https://arxiv.org/abs/1804.08710), [doi:10.1016/j.jpaa.2022.107155](https://doi.org/10.1016/j.jpaa.2022.107155)&rbrack;

Discussion the context of [[enriched category theory]]:

* {#LackTendas20} [[Stephen Lack]], [[Giacomo Tendas]], _Enriched regular theories_, J. Pure Appl. Alg. __226__, n. 6 (2020) 106268, ([arXiv:1907.02301](https://arxiv.org/abs/1907.02301), [doi:10.1016/j.jpaa.2019.106268](https://doi.org/10.1016/j.jpaa.2019.106268))

This discusses (see Theorem 2.1) Kelly's original result for $V$-[[enriched categories]], where $V$ is a closed symmetric monoidal category whose underlying category $V_0$ is locally small, complete and cocomplete, in section 9 (cf. theorem 9.8) of

* [[Max Kelly]], _Structures defined by finite limits in the enriched context_, [[Cahiers]] de Topologie et G&#233;om&#233;trie Diff&#233;rentielle cat&#233;goriques, **23** 1 (1982) 3-42 &lbrack;[numdam](http://www.numdam.org/item?id=CTGDC_1982__23_1_3_0), [MR648793](http://www.ams.org/mathscinet-getitem?mr=648793)&rbrack;

For an extension of Gabriel--Ulmer duality to a duality between [[Cauchy-complete]] [[clans]] and [[locally finitely presentable categories]] equipped with a well-behaved kind of [[weak factorization system]] see

* [[Jonas Frey]], _Duality for Clans: a Refinement of Gabriel-Ulmer Duality_ ([arXiv:2308.11967](https://arxiv.org/abs/2308.11967))

For a connection to [[Tannaka duality]] theory see

* nCaf&eacute; discussion [here](http://golem.ph.utexas.edu/category/2011/07/doctrinal_and_tannakian_recons.html)

* [[Brian Day]], _Enriched Tannaka duality_, JPAA __108__ (1996) pp.17-22, [MR97d:18008](http://www.ams.org/mathscinet-getitem?mr=1382240) <a href="http://dx.doi.org/10.1016/0022-4049(95)00039-9">doi</a>

For a discussion of an $\infty$-version of Gabriel-Ulmer duality between finitely complete and idempotent complete $(\infty, 1)$-categories and locally finitely presentable $(\infty, 1)$-categories see this [MO discussion](https://mathoverflow.net/q/293031/447).


[[!redirects Gabriel-Ulmer dualities]]

[[!redirects Gabriel-Ulmer duality]]
[[!redirects Gabriel–Ulmer duality]]
[[!redirects Gabriel--Ulmer duality]]




