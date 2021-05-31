

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A **total category** is a category with a well-behaved [[Yoneda embedding]] endowing the category with very good completeness and cocompleteness properties but still admitting most types of categories occurring "in practice".

## Definition

+-- {: .num_defn}
###### Definition

A [[locally small category]] $C$ is **total** if its [[Yoneda embedding]] $Y \;\colon \;C\longrightarrow [C^{op},Set]$ has a [[left adjoint]] $L$.  

If the [[opposite category]] $C^{op}$ is total, $C$ is called **cototal**.

=--

+-- {: .num_remark}
###### Remark

The definition above requires some [[set theory|set-theoretic]] assumption to ensure that the [[functor category]] $[C^{op},Set]$ exists, but it can be rephrased to say that the [[colimit]] of $Id_C:C\to C$ [[weighted limit|weighted]] by $W$ exists, for any $W:C^{op}\to Set$.  (This still involves [[quantification]] over large objects, however, so some foundational care is needed.)  This version has an evident generalization to [[enriched category|enriched]] categories.

=--

+-- {: .num_remark}
###### Remark

Since the [[Yoneda embedding]] is a [[full and faithful functor]], a total category $C$  induces an [[idempotent monad]] $Y \circ L$ on its [[category of presheaves]], hence a [[modality]].  One says that $C$ is a [[totally distributive category]] if this modality is itself the [[right adjoint]] of an [[adjoint modality]].

=--

+-- {: .num_remark}
###### Remark

The $(L \dashv Y)$-[[adjunction]] of a total category is closely related to the 
$(\mathcal{O} \dashv Spec)$-[[adjunction]] discussed at _[[Isbell duality]]_ and at _[[function algebras on ∞-stacks]]_. In that context the $L Y$-[[modality]] deserves to be called the _[[affine modality]]_.

=--

## Properties

* Total categories satisfy a very satisfactory [[adjoint functor theorem]]: any colimit-preserving functor from a total category to a locally small category has a [[right adjoint]].  (See [Wood 1982](#Wood82), Thm. 1 for a clear statement of this fact and [StreetWalters](#StreetWalters), p. 372 for a proof).

* Although the definition refers explicitly only to colimits, every total category is also [[complete category|complete]], i.e. has all small limits (this is a categorification of the fact that every cocomplete [[partial order]] is also complete).  It also has some large limits.  In fact, it has "all possible" large limits that a locally small category can have: if $F\colon D\to C$ is a functor such that $lim_d Hom_C(X,F d)$ is a small set for all $X\in C$, then $F$ has a limit.

* A total category $\mathcal{C}$ is [[cartesian closed category|cartesian closed]] iff $L$ preserves binary products (cf. [Wood 1982](#Wood82), Thm. 9).

## Examples

+-- {: .num_prop #Day} 
###### Proposition 
Any [[cocomplete category|cocomplete]] and [[epi-cocomplete category|epi-cocomplete]] category with a [[generator]] is total. More generally, any cocomplete and $E$-complete category with an $E$-generator is total, for a suitable class $E$.  
=-- 

See ([Day](#Day)), theorem 1, for a proof.  This includes:

* [[locally presentable category|locally presentable categories]], hence in particular [[Grothendieck toposes]], or the category of [[abelian sheaves]] on a small [[site]].

Also, totality lifts along [[solid functors]]; that is, if the [[codomain]] of a solid functor is total, then so is its domain.  See ([Tholen](#Tholen)) for a proof.  This implies that the following types of categories are total:

* any [[reflective subcategory]] of a total category

For example

* any category which is [[monadic]] over [[Set]] (see ([Kelly](#Kelly)) Thm. 6.17)

* any category admitting a [[topological functor]] to [[Set]]

* The category [[Grp]] of groups as a category monadic over $Set$ is total, but it is not cototal; see below.

* The category of [[topological groups]] is total as well since it is topological over the total category [[Grp]].

* If $C$ is total and $J$ is small, then $C^J$ is total, morally because it is a reflective subcategory of $Set^{C^{op} \times J}$; see section 6 of [Kelly](#Kelly). 

Thus, "most naturally-occurring" cocomplete categories are in fact total. 

In practice, i.e., in naturally occurring concrete cases, cototality is more rare. For example, it is frequently *not* the case that categories that are monadic over $Set$ are cototal. This is well-illustrated by the following two examples: 

* The category of groups [[Grp]] is not cototal; if it were, then any continuous functor $Grp \to Set$ would be representable. To see this is not the case, it suffices to produce a class of [[simple groups]] $G_\alpha$ of unbounded [[cardinality]] (for example, for any [[infinite set]] $X$, the [[alternating group]] $Alt(X)$, consisting of permutations of finite support that are even, is simple and of cardinality equal to that of $X$). For any group $G$, the hom-set $\hom(G_\alpha, G)$ consists of a single element (the trivial homomorphism) as soon as the cardinality of $G_\alpha$ exceeds that of $G$. Thus the class-indexed product $\prod_\alpha \hom(G_\alpha, G)$ is bounded in size, and defines a continuous functor $F = \prod_\alpha \hom(G_\alpha, -): Grp \to Set$. But it is clear this functor is not representable; e.g., for any group $G$, one can find $G_\alpha$ such that $F(G_\alpha)$ is much larger in size than $\hom(G, G_\alpha)$. This example is given in [Wood 1982](#Wood82). 

* By a similar construction, the category of commutative rings is not cototal. For each infinite cardinal $\alpha$, choose a field $F_\alpha$ of size $\alpha$, e.g., an algebraically closed field over $\mathbb{Q}$ of transcendence degree $\alpha$. Put $A_\alpha = \mathbb{Z} \times F_\alpha$. Then, for any commutative ring $R$, there is exactly one homomorphism $A_\alpha \to R$ as soon as $\alpha$ exceeds the cardinality of $R$. Then one argues that $\prod_\alpha \hom(A_\alpha, -): CRing \to Set$ is continuous but not representable. 


But cototal categories do occur:

* [[Set]] is cototal (as well as total). 

* By dualizing Proposition \ref{Day}, [[Ab]] is cototal (as well as total), because it is complete, well-powered, and has a cogenerator (e.g., $\mathbb{Q}/\mathbb{Z}$). Similarly, the category of [[modules]] $R Mod$ is cototal (and total) for any [[ring]] $R$. For that matter, any [[well-powered category|well-powered]] [[Grothendieck category]], such as the category of [[abelian sheaves]] on a small [[site]], is cototal. 

* Similarly, the category $CH$ of [[compact Hausdorff spaces]] is cototal (as well as total, being monadic over $Set$), because like $Ab$ it is complete, well-powered, and has a cogenerator $I = [0, 1]$ (cf. [[Urysohn's lemma]]). 

* If $C$ is cototal and $J$ is small, then $C^J$ is cototal. 

* Any [[presheaf category]] of a [[small category]] is cototal (as well as total). Indeed, any [[Grothendieck topos]] is both cototal and total. 

* Any category admitting a [[topological functor]] to [[Set]] is cototal (as well as total). 

* Any [[totally distributive category]] is cototal (as well as total).

* Any [[coreflective subcategory]] of a cototal category is cototal, e.g., the category of [[compactly generated spaces]] is cototal.

## Related pages

* [[totally distributive category]]

* [[lex total category]]

## References

* {#StreetWalters}[[Ross Street]], [[Bob Walters]], _Yoneda structures on 2-category_, (contains the original definition of total categories)

*  {#Kelly} [[Max Kelly]], _A survey of totality for enriched and ordinary categories_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 2 (1986), p. 109-132, [numdam](http://www.numdam.org/item?id=CTGDC_1986__27_2_109_0)

* [[Walter Tholen]], _Note on total categories_, Bulletin of the Australian Mathematical Society [cambridge journals](http://journals.cambridge.org/action/displayAbstract?fromPage=online&aid=4759056)
 {#Tholen}

* [[Brian Day]], _Further criteria for totality_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 28 no. 1 (1987), p. 77-78, [numdam](http://www.numdam.org/item?id=CTGDC_1987__28_1_77_0)
 {#Day}

* {#Garner13} [[Richard Garner]], _Topological=Total_  ([arXiv:1310.0903](https://arxiv.org/abs/1310.0903))

* {#Street84} [[Ross Street]], _The family approach to total cocompleteness and toposes_ , Trans. A. M. S. **284** (1984) pp.355-369, (<a href="https://www.ams.org/journals/tran/1984-284-01/S0002-9947-1984-0742429-3/S0002-9947-1984-0742429-3.pdf">AMS</a>)

* {#Wood82} [[Richard J. Wood]], _Some remarks on total categories_, J. Algebra **75**:2, 1982, 538&#8211;545 <a href="http://dx.doi.org/10.1016/0021-8693(82)90055-2">doi</a>

[[!redirects total categories]]
[[!redirects cototal category]]
[[!redirects cototal categories]]