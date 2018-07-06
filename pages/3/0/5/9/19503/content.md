

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Dugger's theorem identifies [[combinatorial model categories]] as the [[model category]]-presentations of [[locally presentable (infinity,1)-categories]].


## Statement

+-- {: .num_theorem }
###### Theorem 
**(Dugger's theorem)**

Every [[combinatorial model category]] $C$ is [[Quillen equivalence|Quillen equivalent]] to a left [[Bousfield localization of model categories|Bousfield localization]] $L_S SPSh(K)_{proj}$ of the global projective [[model structure on simplicial presheaves]] $SPSh(K)_{proj}$ on a [[small category]] $K$

$$
  L_S SPSh(K)_{proj} \stackrel{\simeq_{Quillen}}{\to}
  C
  \,.
$$


=--

This is ([Dugger 01, theorem 1.1](#Dugger01)) building on results in ([DuggerUniversalHomotopy](#DuggerUniversalHomotopy)).


+-- {: .proof}
###### Proof


The proof proceeds (the way Dugger presents it, at least) in roughly three steps:

1. Use that $[C^{op}, sSet_{Quillen}]_{proj}$ is in some precise sense the _homotopy-_ [[free cocompletion]] of $C$. This means that every functor $\gamma : C \to B$ from a plain category $C$ to a model category $B$ factors in an essentially unique way through the [[Yoneda embedding]] $j : C \to [C^{op},sSet]$ by a [[Quillen adjunction]] 

   $$
     (\hat \gamma \dashv R) : 
     B
     \stackrel{\overset{\hat \gamma}{\leftarrow}}
      {\underset{R}{\to}}
     [C^{op}, sSet_{Quillen}]_{proj}  
     \,.
   $$

   The detailed definitions and detailed proof of this are discussed at [[(∞,1)-category of (∞,1)-presheaves]].

1. For a given combinatorial model category $B$, choose $C := B_\lambda^{cof}$ the full [[subcategory]] on a [[small set]] (guaranteed to exist since $B$ is [[locally presentable category|locally presentable]]) of cofibrant $\lambda$-[[compact object]]s, for some [[regular cardinal]] $\lambda$, and show that the induced Quillen adjunction 

   $$
     B \stackrel{\overset{\hat i}{\leftarrow}}{\underset{R}{\hookrightarrow}}
     [(B_\lambda^{cof})^{op}, sSet]_{proj} 
   $$


   induced by the above statement from the inclusion $i : B_\lambda^{cof} \hookrightarrow B$ exhibits $B$ as a homotopy-[[reflective subcategory]] in that the [[derived functor|derived]] counit $ \hat i \circ Q \circ R \stackrel{\simeq}{\to} Id$ ($Q$ some cofibrant replacement functor) is a [[natural transformation|natural]] weak equivalence on fibrant objects (recall from [[adjoint functor]] the characterization of adjoints to full and faithful functors).

1. Define $S$ to be the set of morphisms in $[(C_\lambda^{cof})^{op}, sSet]$ that the left [[derived functor]] $\hat i \circ Q$ of $\hat i$ (here $Q$ is some cofibrant replacement functor) sends to weak equivalences in $B$. Then form the left [[Bousfield localization of model categories|Bousfield localization]] $L_S [(C_\lambda^{cof})^{op},sSet]_{proj}$ with respect to this set of morphisms and prove that this is [[Quillen equivalence|Quillen equivalent]] to $B$.

Carrying this program through requires the following intermediate results.

First recall from the discussion at [[(∞,1)-category of (∞,1)-presheaves]] that to produce the Quilen adjunction $(\hat i \dashv R)$ from $i$, we are to choose a [[cofibrant resolution]] functor

$$
  I : C \to [\Delta,B]
$$

of $i : C= B_\lambda^{cof} \to B$.

The [[adjunct]] of this is a functor $\tilde I : C \times \Delta \to B$. For each object $b \in B$ write $(C \times \Delta \downarrow b)$ for the [[slice category]] induced by this functor. 


**Lemma** (Dugger, prop. 4.2) 

For every fibrant object $b \in B$ we have that the [[homotopy colimit]] $hocolim (C \times \Delta \downarrow b) \to B)$
is weakly equivalent to $\hat i \circ Q\circ R (b)$.

**Corollary** (Dugger, cor. 4.4) The induced Quillen adjunction

$$
  B \stackrel{\leftarrow}{\to}
  [C^{op}, sSet]
$$

is a homotopy-reflective embedding precisely if the canonical morphisms

$$
  hocolim (C \times \Delta \downarrow b) \to b
$$

are weak equivalences for every fibrant object $b \in B$.

...


=--

Notice that the theorem just mentions plain combinatorial model categories, not [[simplicial model category|simplicial model categories]]. But of course by basic facts of [[enriched category theory]] $Funct(C^{op}, SSet)$ is an [[SSet]]-[[enriched category]] and its projective [[global model structure on functors]] $Func(C^{op}, SSet)_{proj}$ is compatibly a [[simplicial model category]], as are all its [[Bousfield localization of model categories|Bousfield localizations]]. (See [[model structure on simplicial presheaves]] for more details.) Therefore an immediate but very useful corollary of the above statement is

+-- {: .num_corollary }
###### Corollary 

Every combinatorial model category is [[Quillen equivalence|Quillen equivalent]] to one which is

* a [[simplicial model category]]

* a left [[proper model category]].

=--

## Related concepts

[[!include locally presentable categories - table]]


## References

Dugger's theorem is due to

* {#Dugger01} [[Daniel Dugger]], _[[Combinatorial model categories have presentations]]_, Adv. Math. 164 (2001), no. 1, 177-201 ([arXiv:math/0007068](http://arxiv.org/abs/math/0007068))

based on results in

* {#DuggerUniversalHomotopy} [[Dan Dugger]], _[[Universal homotopy theories]]_

The interpretation in terms of [[locally presentable (infinity,1)-categories]] is due to

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_
