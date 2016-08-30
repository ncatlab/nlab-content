
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A _pro-manifold_ is a [[pro-object]] in a [[category]] of [[manifolds]], i.e. a formal [[projective limit]] of [[manifolds]].

Details depend on what exactly is understood by "[[manifold]]", i.e. whether [[topological manifolds]] or [[smooth manifold]], etc. 

Typically one wants to mean [[pro-objects]] in manifolds of [[finite number|finite]] [[dimensions]], the point being then that a pro-manifold is like an [[infinite-dimensional manifold]] but with "mild" infinite dimensionality, expressed by the very fact that it may be presented as a formal projective limit of finite dimensional manifolds.

To amplify this specification, one should properly speak of "pro-(finite dimensional smooth manifolds)", but beware that people often abbreviate to "pro-manifold" regardless. Also "pro-finite manifold" is in use, which however, strictly speaking, is a misnomer since a "finite manifold" is one with a [[finite number]] of points.

An important example of pro-objects in finite-dimensional smooth manifolds are infinite [[jet bundles]]. These are the formal projective limits of the underlying finite-order jet bundles.


## Properties

+-- {: .num_defn }
###### Definition

Write [[CartSp]] for the [[full subcategory]] of that of [[smooth manifolds]] on the [[Cartesian spaces]], i.e. on those of the form $\mathbb{R}^n$, for $n \in \mathbb{N}$. Write $Pro(CartSp)$ for its category of [[pro-objects]].

=--

+-- {: .num_prop #ProCartSpFullyFaithfulInSmoothLoc}
###### Proposition

The functor which sends a formal cofiltered limit of Cartesian spaces to its actual [[cofiltered limit]] of [[smooth loci]] is a [[fully faithful functor]].

$$
  Pro(CartSp) \hookrightarrow SmthLoc
  \,.
$$

=--

+-- {: .proof}
###### Proof

Since $Pro(\mathcal{C}) \simeq (Ind(\mathcal{C}^{op}))^{op}$ ([remark](pro-object#ProObjectAsFormalDualOfIndObject)) it is sufficient to show that the functor in question is on opposite categories a fully faithful functor of the form

$$
  Ind(CartSp^{op})
    \hookrightarrow
  SmthLoc^{op} = SmthAlg_{\mathbb{R}}
  \,,
$$

where $SmothAlg_{\mathbb{R}}$ is the category of [[smooth algebras]].

Now, there is the [[fully faithful functor]] 

$$
  i \;\colon\; CartSp \hookrightarrow SmthLoc 
$$ 

([prop.](smooth+locus#SmoothManifoldsFullSubcategoryOfSmoothLoci)) hence a fully faithful functor

$$
  i^{op} \colon CartSp^{op} \hookrightarrow SmthAlg_{\mathbb{R}}
  \,.
$$ 

Moreover, the image of the latter is in [[compact objects]] $i^{op} \colon CartSp^{op} \hookrightarrow (SmthAlg_{\mathbb{R}})_{cpt} \hookrightarrow SmthAlg$, because

$$
  C^\infty(\mathbb{R}^n) \simeq y(\mathbb{R}^n)
  \in 
  SmthAlg_{\mathbb{R}} \simeq Func_\times(CartSp,Set)
$$

is [[representable functor|co-representable]], hence [[compact object|compact]] (by the [[Yoneda lemma]] and since colimits are computed objectwise [prop.](limits+and+colimits+by+example#LimitsOfPresheaves)).

This implies that the composite

$$
  Ind(CartSp^{op})
   \overset{Ind(i^{op})}{\hookrightarrow}
  Ind(SmthAlg_{\mathbb{R}})
    \overset{L}{\longrightarrow}
  SmthAlg_{\mathbb{R}}
$$

is also fully faithful ([prop.](ind-object#JFIsFullyFaithful)).

Here $Ind(i^{op})$ takes formal filtered colimits in $CartSp^{op}$ to the corresponding formal colimits in $SmthAlg_{\mathbb{R}}$ ([prop.](ind-object#FunctorialityOfInd)), while $L$ takes formal filtered colimits to actual [[filtered colimits]] ([prop.](ind-object#ReflectionToYonedaEmbedding)). Hence this is indeed the functor in question.

=--

[[!redirects pro-manifolds]]