
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
###### Eilenberg-Watts' Theorem

Given unital [[rings]] $R$ and $S$ and an $R$-$S$-[[bimodule]] $N$, the [[tensor product of modules|tensor product]] [[functor]]

$$ 
  (-) \otimes_R N  
   \;\colon\; 
  Mod_R \to Mod_S 
$$

between the [[categories of modules]] is [[right exact functor|right exact]] and preserves [[small category|small]] [[coproducts]].  

Conversely, if $F \colon Mod_R \to Mod_S$ is right exact and preserves small coproducts, then it is naturally isomorphic to tensoring with a bimodule.

=--

This theorem was more or less simultaneously proved in ([Watts](#Watts)) and ([Eilenberg](#Eilenberg)).

+-- {: .num_remark}
###### Remark

Given a [[cocontinuous functor]] $F \colon Mod_R \to Mod_S$, the reconstructed $R$-$S$-bimodule is given as follows:

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

The theorem holds for nonunital rings as well, but then $B$ reconstructs as $F(R_1)$ where $R_1$ is the extension of $R$ by adjoining the unit element (the tensor product is still over the original $R$). If $F$ is a [[flat functor]] then $F(R_1)$ is a [[flat module]] over $R$. 

=--

+-- {: .num_remark}
###### Remark

In the statement of the theorem we can replace "additive, right exact and preserves direct sum" by "additive and [[left adjoint]]".

=--

In this form the theorem is stated for instance in ([Hovey, theorem 0.1](#Hovey)).

In fact both bimodules and [[intertwiners]] as well as [[functors]] and [[natural transformations]] form a [[category]]. In more detail the theorem is:

+-- {: .num_theorem}
###### Theorem

For $R$ and $S$ two [[rings]], the [[functor]]

$$
  {}_R Mod_{S} \stackrel{\simeq}{\to} Func_{coc}(Mod_R, Mod_S)
$$

from the category of bimodules to that of colimit-preserving functors between their [[categories of modules]] is an [[equivalence of categories]].

=--

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

* Charles E. Watts, _Intrinsic characterizations of some additive functors_,  Proc. Amer. Math. Soc. __11__, 1960, 5&#8211;8, [MR0806.0832](http://www.ams.org/mathscinet-getitem?mr=0806.0832), [doi](http://dx.doi.org/10.2307/2032707)
 {#Watts}

* [[Samuel Eilenberg]], _Abstract description of some basic functors_, J. Indian Math. Soc. (N.S.) __24__, 1960, 231&#8211;234 (1961), [MR0125148](http://www.ams.org/mathscinet-getitem?mr=0125148)
 {#Eilenberg}

A generalized statement in which the codomain is not assumed to be a category of modules is discussed in

* A. Nyman, S. Paul Smith, _A generalization of Watts's Theorem: Right exact functors on module categories_, 
Communications in Algebra __44__:7 (2016) 3160-3170 [arxiv/0806.0832](http://arxiv.org/abs/0806.0832) [doi](https://doi.org/10.1080/00927872.2015.1065873)

Generalization to [[homotopy theory]]/[[higher algebra]] is discussed in 

* [[Mark Hovey]], _The Eilenberg-Watts theorem in homotopical algebra_ ([pdf](http://hopf.math.purdue.edu/Hovey/watts.pdf))
 {#Hovey}

and 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}

[[!redirects Watts theorem]]
[[!redirects Eilenberg-Watts' Theorem]]
[[!redirects Eilenberg-Watts Theorem]]