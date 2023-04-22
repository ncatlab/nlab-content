
Consider

* $k$ a [[field]];

* $Ch_\bullet(k)$ its [[category of chain complexes]] (unbounded) of $k$-[[vector spaces]] equipped with its projective [[model category]] [[structure]] (this is a [[proper model category|proper]] [[combinatorial model category]], by [this Prop.](model+structure+on+chain+complexes#StandardModelStructureOnUnboundedComplexes))

* $sCh_\bullet(k)$ the corresponding [[category of simplicial objects]] equipped with a [[Bousfield localization of model categories|left Bousfield localization]] of the corresponding [[Reedy model structure]] which makes it (by [this Prop.](model+structure+on+chain+complexes#LocalizedReedyModelStructureOnSimplicialUnboundedChainComplexes)) a [[simplicial model category]] whose [[underlying]] model category is [[Quillen equivalence|Quillen equivalent]] to $Ch_\bullet(k)$;

  ($sCh_\bullet(k)$ is, besides being [[simplicial model category|simplicial]], a [[left proper model category|left proper]] [[combinatorial model category]] by [this Prop.](Reedy+model+structure#LeftProperness) and [this Prop.](Bousfield+localization+of+model+categories#ExistenceForLeftProperCombinatorialSimplicialModelCategories))

* $sGrpd$ the category of Dwyer-Kan [[simplicial groupoids]] equipped with the projective [[model structure on simplicial groupoids]];

* $sFunc\big(\mathcal{X}, sCh_\bullet(k)\big)$, for $\mathcal{X} \in sGrpd$, the [[sSet]]-[[enriched functor category]] from the [[sSet-enriched category]] [[underlying]] $\mathcal{X}$ and equipped with the injective [[model structure on functors]]

  (this exists and is [[combinatorial model category|combinatorial]], by discussion [there](model+structure+on+functors#CombinatorialCase), because $sCh_\bullet(k)$ is combinatorial);

* $sFunc\big(-,sCh_\bullet(k)\big) \colon sGrpd \to Cat$ the [[pseudofunctor]] to [[Cat]] which on [[morphisms]] $f \colon \mathcal{X} \to \mathcal{Y}$ is given by [[left Kan extension]] $f_! \,\colon\, sFunc\big(\mathcal{X},sCh_\bullet(k)\big) \to sFunc\big(\mathcal{Y},sCh_\bullet(k)\big)$

  > mistake here: $f_!$ is left Quillen on the projective but not on the injective model structure...

* $\underset{\mathcal{X} \in sGrpd}{\int} sFunc\big( \mathcal{X} ,\, sCh_\bullet(k)  \big)$ the [[Grothendieck construction]] on this pseudofunctor.

\begin{proposition}
  The category $\underset{\mathcal{X} \in sGrpd}{\int} sFunc\big( \mathcal{X} ,\, sCh_\bullet(k)  \big)$ admits the corresponding [[integral model structure]].
\end{proposition}
\begin{proof}
  By the discussion [there](Grothendieck+construction+for+model+categories#Definition), it is sufficient to check that $sFunc\big(-,sCh_\bullet(k)\big)$

1. is "*relative*" as a functor to [[Ho(CombModCat)]] in that it sends weak equivalences in $sGrpd$ to [[Quillen equivalences]];

1. is "*proper*" in that

   1. for $f$ an [[acyclic fibration]] in $sGrpd$ the induced [[right Quillen functor]] $f^\ast$ preservers weak equivalences.

   1. for $f$ an [[acyclic cofibration]] in $sGrpd$ the induced [[left Quillen functor]] $f_!$ preservers weak equivalences,


We discuss these conditions in turn:

1. To see relative-ness:

   By general facts in *[[Higher Topos Theory]]* and using the [[stable Dold-Kan correspondence]], our functor [[presentable (infinity,1)-category|presents]] the [[(infinity,1)-functor|$\infty$-functor]] $Func_\infty\big(-; (H k) Mod\big) \,\colon\, Grpd_\infty \to (H k) Mod$ assigning to base-[[infinity-groupoids|$\infty$-groupoids]] their [[stable (infinity,1)-categories|stable $\infty$-categories]] of [[parameterized spectra|parameterized]] [[Eilenberg-MacLane spectrum|$H \mathbb{C}$]]-[[module spectra]] ("[[infinity-local system|$\infty$-local systems]]"). By $\infty$-functoriality, this preserves [[equivalence in an (infinity,1)-category|$\infty$-equivalences]] which here means that weak equivalences $f$ in $sGrpd$ are sent to [[derived functors]] $\mathbb{L} f_!$ that, in particular, induce [[equivalence of categories|equivalences]] on the [[homotopy category of an (infinity,1)-category|homotopy categories of $\infty$-catgories]], hence of [[homotopy category of a model category|homotopy categories of model categories]]. But this  means that [[Quillen adjunction]] $f_! \dashv f^\ast$ induced by an equivalence $f$ is indeed a [[Quillen equivalence]].

1. To see properness:

   1. Recall that the weak equivalences in [[model structure on functors]] are objectwise in $sGrpd$ the weak equivalences in $sCh_\bullet$. This immediately implies that $f^\ast$ (given by precomposition of functors) preserves weak equivalences (no matter the nature of $f$).

   1. We will show that $f_!$ preserves weak equivalences (again independently of the nature of $f$, even) by arguing that it essentially acts as its own derived functor already.

This last argument occupies the remainder of the proof:

> The following is besides the point, since it is referring to the injective model structure where it should be referring to the projective one. Will fix...

First observe that, while not all chain complexes are cofibrant ([this remark](model+structure+on+chain+complexes#NotAllUnboundedComplexesAreProjectivelyCofibrant)), *all [[bounded-below chain complexes]] are cofibrant* (by [this Prop.](model+structure+on+chain+complexes#BoundedBelowComplexesOfProjectivesAreProjectivelyCofibrant) and using that we are working over a [[field]] all whose [[modules]], namely [[vector spaces]], are [[projective module|projective]], by [this Prop.](projective+module#ModuleOverAFieldIsProjective) ).

But every chain complex $V_\bullet \,\in\, Ch_\bullet(k)$ is the [[colimit]] over its [[cotower]] of $n$-[[connective covers]] 

$$
  V_\bullet
  \;\simeq\;
  \underset{\longrightarrow}{lim}
  \big(
  \cdots
  \hookrightarrow
  cn_{\geq n+1} V_\bullet
  \hookrightarrow
  cn_{\geq n} V_\bullet
  \hookrightarrow
  cn_{\geq n-1} V_\bullet
  \cdots
  \big)
  \,,
$$
and since [[colimits]] of [[simplicial objects]] are computed degreewise (by [[limits of presheaves are computed objectwise|general facts]]), the same holds for any functor of simplicial chain complexes $V^\bullet_\bullet(-) \in sFunc\big(\mathcal{X}, sCh_\bullet(k)\big)$:
$$
  V^\bullet_\bullet(-)
  \;\simeq\;
  \underset{\longrightarrow}{lim}
  \big(
  \cdots
  \hookrightarrow
  cn_{\geq n+1} V^\bullet_\bullet(-)
  \hookrightarrow
  cn_{\geq n} V^\bullet_\bullet(-)
  \hookrightarrow
  cn_{\geq n-1} V^\bullet_\bullet(-)
  \cdots
  \big)
$$
(where the [[connective cover]]-constructions now act objectwise as before, for each $\mathcal{X} \in sGrpd$ and $[k] \in \Delta$).

With this and since [[left adjoints preserve colimits]], we find that 

$$
  f_! V^\bullet_\bullet(-)
  \;\simeq\;
  \underset{\longrightarrow}{lim}
  \Big(
  \cdots
  \hookrightarrow
  f_! \big(cn_{\geq n+1} V^\bullet_\bullet(-)\big)
  \hookrightarrow
  f_! \big(cn_{\geq n} V^\bullet_\bullet(-)\big)
  \hookrightarrow
  f_!\big(cn_{\geq n-1} V^\bullet_\bullet(-)\big)
  \cdots
  \Big)
  \,.
$$

Now we claim that each $cn_{\geq n} V^\bullet_\bullet(-)$ is a [[cofibrant object]] in $sFunc\big(sGrpd, sCh_\bullet(k)\big)$. Because:

Since we are using the injective [[model structure on functors]], we need to see that for $\mathcal{X} \in sGrpd$ the object $cn_{\geq n} V^\bullet_\bullet(\mathcal{X})$ is cofibrant in the Bousfield localized Reedy model structure. Since left Bousfield localization does not change the class of [[cofibrations]] ([by definition](Bousfield+localization+of+model+categories#DefinitionOfLeftBousfieldLocalizations)) we are reduced to arguing this for plain [[Reedy model structure|Reedy cofibrancy]]. 
Here, again [by definition](Reedy+model+structure#ReedyModelStructure),
this means that we need to show that the [comparison maps](Reedy+model+structure#eq:ComparisonMapsFromLatchingToMatchingObject) $L_r(-) \to (-)_r$ from its [[latching objects]] are cofibrations in $Ch_\bullet(k)$.

But since $Ch_\bullet(k)$ is an [[abelian category]] (see [there](category+of+chain \+complexes#AbelianCategoryStructure)), it follows (by [this prop.](Reedy+model+structure#LatchingInAbelianCategoryIsDegeneracySubobject)) that $L_r(-) \to (-)_r$ is a monomorphism on our objects. Monomorphisms are cofibrations in the [[model structure on chain complexes]] over a [[field]] (where all injections are split) iff their [[cokernel]] is cofibrant (by [this Prop.](model+structure+on+chain+complexes#StandardModelStructureOnUnboundedComplexes)). But since we are dealing with maps between $n$-connective covers, also the cokernels are $n$-connective and hence cofibrant by the above argument. QED.

It follows that the [[left Quillen functor]] $f_!$ on the right hand side in the above formula is applied to cofibrant objects and hence coincides with its [[derived functor]] there, thus sending weak equivalences to weak equivalences ([Ken Brown's lemma](Introduction+to+Homotopy+Theory#KenBrownLemma)). 

So far this means that $f_!$ sends any weak equivalence to a colimit, in the [[arrow category]], of weak equivalences between stages in the [[connective cover]]-[[cotowers]] of the given objects. But, by the same cofibrancy argument just invoked, the structure morphisms in these cotowers are (monomorphisms and hence) cofibrations, so that this colimit is a [[homotopy colimit]] (see [there](homotopy+limit#CotowerColimits)) and hence preserves weak equivalences. 
This concludes the proof that also $f_!$ preserves weak equivalences. 
\end{proof}



