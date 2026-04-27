
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Eilenberg-Watts theorem_ identifies colimit-preserving [[functors]] between [[categories of modules]] with the operations of forming [[tensor product of modules|tensor products]] with [[bimodules]].

## Statement

### For ordinary rings and modules

+-- {: .num_theorem}
<b>Eilenberg-Watts Theorem</b>

Given unital [[rings]] $R$ and $S$ and an $R$-$S$-[[bimodule]] $N$, the [[tensor product of modules|tensor product]] [[functor]]

$$ 
  (-) \otimes_R N  
   \;\colon\; 
  Mod_R \to Mod_S 
$$

between the [[categories of modules]] is [[additive functor|additive]] and [[cocontinuous functor|cocontinuous]].  Conversely, if $F \colon Mod_R \to Mod_S$ is additive and cocontinuous, then it is naturally isomorphic to tensoring with a bimodule.

=--

This theorem was more or less simultaneously proved in ([Watts](#Watts)) and ([Eilenberg](#Eilenberg)).

+-- {: .num_remark}
###### Remark

Given an additive cocontinuous functor $F \colon Mod_R \to Mod_S$, the reconstructed $R$-$S$-bimodule is given as follows:

* the underlying right $S$-module is $F(R)$, where $R$ is regarded as a right module over itself in the canonical way;

* the left $R$-module structure on $F(R)$ is given for $r \in R$ and $n \in N$ by

  $$
    r \cdot n \coloneqq F(r\cdot(-))n
    \,,
  $$

  where $r \cdot (-) \colon R \to R$ denotes the right $R$-module homomorphism given by left multiplication by $r$.
=--

+-- {: .num_remark}
###### Remark

The theorem holds for nonunital rings as well, but then $N$ reconstructs as $F(R_1)$ where $R_1$ is the extension of $R$ by adjoining the unit element (the tensor product is still over the original $R$). If $F$ is a [[flat functor]] then $F(R_1)$ is a [[flat module]] over $R$. 

=--

+-- {: .num_remark}
###### Remark

There are various equivalent ways to state the hypotheses of the theorem:

* $F$ is additive and [[cocontinuous functor|cocontinuous]] (i.e. preserves [[small category|small]]  [[colimits]]).
* $F$ is additive, [[right exact functor|right exact]] and preserves [[small category|small]] [[coproducts]].  
* $F$ is additive and [[left adjoint]].

=--

The theorem is stated in the last form, for instance, in ([Hovey, Theorem 0.1](#Hovey)).

In fact both bimodules and [[intertwiners]] as well as [[functors]] and [[natural transformations]] form a [[category]]. In more detail the theorem is:

+-- {: .num_theorem}
###### Theorem

For $R$ and $S$ two [[rings]], the [[functor]]

$$
  {}_R Mod_{S} \stackrel{\simeq}{\to} Func_{coc}(Mod_R, Mod_S)
$$

from the category of bimodules to that of colimit-preserving additive functors between their [[categories of modules]] is an [[equivalence of categories]].

=--

### For enriched categories

Rings can be seen as one-object $V$-enriched categories where $V = Ab$ is the category of abelian groups made symmetric monoidal with the usual tensor product of abelian groups.   Similarly, bimodules between rings are the same as $V$-enriched [[distributors]] between one-object $V$-enriched categories.  The category of right modules of a ring $R$ is the category of $V$-enriched presheaves on the corresponding one-object $V$-enriched category. Thus, we can ask if the Eilenberg-Watts theorem generalizes to $V$-enriched categories.  And indeed it does!  

Suppose that $\mathscr{V}$ is a complete and cocomplete right-[[closed monoidal category]]. (More generally, we can consider enrichment in a locally complete and locally cocomplete [[bicategory]] $\mathscr{W}$ with [[Kan lift|right lifts]]: see [[enrichment in a bicategory]] for more details.) Then there is a bicategory $\mathscr{V}\text{-}Dist$ where:

* objects are small $\mathscr{V}$-enriched categories,
* morphisms are $\mathscr{V}$-enriched distributors,
* 2-morphisms are $\mathscr{V}$-enriched natural transformations between distributors.

There is also a bicategory $\mathscr{V}\text{-}Cocont$ where:

* objects are the $\mathscr{V}$-enriched [[presheaf categories]] on small $\mathscr{V}$-enriched categories
* morphisms are cocontinuous $\mathscr{V}$-functors, i.e. $\mathscr{V}$-functors preserving all [[weighted colimits]]
* 2-morphisms are $\mathscr{V}$-enriched natural transformations between cocontinuous $\mathscr{V}$-functors.

The following then exhibits a generalized Eilenberg–Watts Theorem:

\begin{theorem}(Theorem 10.13 of [Arkor & McDermott 2026](#AM26))
Given a locally complete and locally cocomplete bicategory $\mathscr{W}$ with right lifts, the bicategories $\mathscr{W}\text{-}Dist$ and $\mathscr{W}\text{-}Cocont$ are [[biequivalence|biequivalent]].
\end{theorem}

(The theorem ibid. is actually even more general, as it parameterised by the class of colimits.)

(When $\mathscr{V}$ is a [[symmetric monoidal category]], the bicategories in question are furthermore [[symmetric monoidal bicategories]], relative to the [[tensor product of enriched categories]], and this biequivalence is symmetric monoidal. However, there does not appear to be an explicit reference for this in the literature yet.)


### For other internal monoids and internal modules

The standard Eilenberg-Watts theorem is a statement about [[monoids]] and their [[actions]] in [[Ab]]. More generally one may ask for generalizations of the theorem to other internalization contexts, and in particular to [[homotopy theory]]. See the introduction of ([Hovey](#Hovey)).

### For $\infty$-algebras and $\infty$-modules
 {#ForInfinityAlgebrasAndInfinityModules}

In particular Eilenberg-Watts theorems hold true in the [[homotopy theory]] following [[model categories]] (see at [[model structure on modules over an algebra over an operad]])

* [[model structure on topological spaces]]

* [[model structure on simplicial sets]]

* [[model structure on chain complexes]]

* [[model structure on spectra]] (symmetric, orthogonal, $\mathbb{S}$-modules).

This is the main theorem in ([Hovey](#Hovey)).

More generally, we have the first half of the Eilenberg-Watts theorem in [[(∞,1)-category theory]]:

+-- {: .num_prop }
###### Proposition

For $(\mathcal{C}, \otimes)$ a [[monoidal (∞,1)-category]] with [[geometric realization]] of [[simplicial objects in an (∞,1)-category]] such that the [[tensor product]] $\otimes$ preserves this in each variable, then for all [[A-∞ algebra]] $A,B,C$ in $\mathcal{C}$, the tensor product of [[∞-bimodules]] 

$$
  (-) \otimes_B (-) \;\colon\; {}_A Mod_{B} \times {}_B Mod_{C} \to {}_{A} Mod_{C}
$$

preserves [[(∞,1)-colimits]] separately in each argument.

=--

This is ([Lurie, cor. 4.3.5.15](#Lurie)).

## Related concepts

* [[Morita equivalence]]

* [[additive functor]], [[Tor]]

## References
 {#References}

The original articles are

* Charles E. Watts, _Intrinsic characterizations of some additive functors_,  Proc. Amer. Math. Soc. __11__, 1960, 5&#8211;8, [MR118757](https://mathscinet.ams.org/mathscinet/article?mr=118757), [doi](http://dx.doi.org/10.2307/2032707)
 {#Watts}

* [[Samuel Eilenberg]], _Abstract description of some basic functors_, J. Indian Math. Soc. (N.S.) __24__, 1960, 231&#8211;234 (1961), [MR0125148](http://www.ams.org/mathscinet-getitem?mr=0125148)
 {#Eilenberg}

A generalized statement in which the codomain is not assumed to be a category of modules is discussed in

* A. Nyman, S. Paul Smith, _A generalization of Watts's Theorem: Right exact functors on module categories_, 
Communications in Algebra __44__:7 (2016) 3160-3170 [arxiv/0806.0832](http://arxiv.org/abs/0806.0832) [doi](https://doi.org/10.1080/00927872.2015.1065873)

Generalization to [[categories enriched in bicategories]] is given in section 10.4 of

* {#AM26} [[Nathanael Arkor]], [[Dylan McDermott]], *Presheaves and cocompletions in formal category theory* &lbrack;[arXiv:2604.22370](https://arxiv.org/abs/2604.22370)&rbrack;

Generalization to [[homotopy theory]]/[[higher algebra]] is discussed in 

* [[Mark Hovey]], _The Eilenberg-Watts theorem in homotopical algebra_ ([pdf](https://arxiv.org/pdf/0910.3842.pdf))
 {#Hovey}

and 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}


[[!redirects Watts theorem]]
[[!redirects Eilenberg-Watts' Theorem]]
[[!redirects Eilenberg-Watts Theorem]]