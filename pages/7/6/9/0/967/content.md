
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

* Total categories satisfy a very satisfactory [[adjoint functor theorem]]: any colimit-preserving functor from a total category to a locally small category has a [[right adjoint]].

* Although the definition refers explicitly only to colimits, every total category is also [[complete category|complete]], i.e. has all small limits.  It also has some large limits.  In fact, it has "all possible" large limits that a locally small category can have: if $F\colon D\to C$ is a functor such that $lim_d Hom_C(X,F d)$ is a small set for all $X\in C$, then $F$ has a limit.


## Examples

Any [[cocomplete category|cocomplete]] and [[epi-cocomplete category|epi-cocomplete]] category with a [[generator]] is total.  (And more generally, any cocomplete and $E$-complete category with an $E$-generator is total, for a suitable class $E$.)  See ([Day](#Day)), theorem 1, for a proof.  This includes:

* [[locally presentable category|locally presentable categories]], hence in particular [[Grothendieck toposes]].

Also, totality lifts along [[solid functors]]; that is, if the [[codomain]] of a solid functor is total, then so is its domain.  See ([Tholen](#Tholen)) for a proof.  This implies that the following types of categories are total:

* any [[reflective subcategory]] of a total category

* any category which is [[monadic]] over [[Set]]

* any category admitting a [[topological functor]] to [[Set]]

Thus, "most naturally-occurring" cocomplete categories are in fact total.  However, cototality is more rare.  But cototal categories do occur:

* [[Set]] is cototal (as well as total).

* Any [[presheaf category]] of a [[small category]] is cototal (as well as total). Indeed, any [[Grothendieck topos]] is both cototal and total. 

* Any category admitting a [[topological functor]] to [[Set]] is cototal (as well as total).

* Any [[totally distributive category]] is cototal (as well as total).

* Any [[coreflective subcategory]] of a cototal category is cototal.

## Related pages

* [[totally distributive category]]

## References

* [[Ross Street]], [[Bob Walters]], _Yoneda structures on 2-category_, (contains the original definition of total categories)

* [[Max Kelly]], _A survey of totality for enriched and ordinary categories_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 2 (1986), p. 109-132, [numdam](http://www.numdam.org/item?id=CTGDC_1986__27_2_109_0)
 {#Kelly}

* [[Walter Tholen]], _Note on total categories_, Bulletin of the Australian Mathematical Society [cambridge journals](http://journals.cambridge.org/action/displayAbstract?fromPage=online&aid=4759056)
 {#Tholen}

* [[Brian Day]], _Further criteria for totality_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 28 no. 1 (1987), p. 77-78, [numdam](http://www.numdam.org/item?id=CTGDC_1987__28_1_77_0)
 {#Day}

* R.J Wood, _Some remarks on total categories_, J. Algebra __75_:2, 1982, 538&#8211;545 <a href="http://dx.doi.org/10.1016/0021-8693(82)90055-2">doi</a>

[[!redirects total categories]]
[[!redirects cototal category]]
[[!redirects cototal categories]]