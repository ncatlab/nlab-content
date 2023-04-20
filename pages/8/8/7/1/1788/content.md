
Consider

* $k$ a [[field]];

* $Ch_\bullet(k)$ its [[category of chain complexes]] (unbounded) of $k$-[[vector spaces]] equipped with its projective [[model category]] [[structure]] ([here](model+structure+on+chain+complexes#StandardModelStructureOnUnboundedComplexes));

* $sCh_\bullet(k)$ the corresponding [[category of simplicial objects]] equipped with the [[Bousfield localization of model categories|left Bousfield localization]] of the corresponding [[Reedy model structure]] which makes it (by [this Prop.](model+structure+on+chain+complexes#LocalizedReedyModelStructureOnSimplicialUnboundedChainComplexes)) a [[simplicial model category]] whose [[underlying]] model category is [[Quillen equivalence|Quillen equivalent]] to $Ch_\bullet(k)$;

* $sGrpd$ the category of Dwyer-Kan [[simplicial groupoids]] equipped with the projective [[model structure on simplicial groupoids]];

* $sFunc\big(\mathcal{X}, sCh_\bullet(k)\big)$, for $\mathcal{X} \in sGrpd$, the [[sSet]]-[[enriched functor category]] from the [[sSet-enriched category]] [[underlying]] $\mathcal{X}$ and equipped with the injective [[model structure on functors]];

* $sFunc\big(-,sCh_\bullet(k)\big) \colon sGrpd \to Cat$ the [[pseudofunctor]] to [[Cat]] which on [[morphisms]] $f \colon \mathcal{X} \to \mathcal{Y}$ is given by [[left Kan extension]] $f_! \,\colon\, sFunc\big(\mathcal{X},sCh_\bullet(k)\big) \to sFunc\big(\mathcal{Y},sCh_\bullet(k)\big)$;

* $\underset{\mathcal{X} \in sGrpd}{\int} sFunc\big( \mathcal{X} ,\, sCh_\bullet(k)  \big)$ the [[Grothendieck construction]] on this pseudofunctor.

\begin{proposition}
  The category $\underset{\mathcal{X} \in sGrpd}{\int} sFunc\big( \mathcal{X} ,\, sCh_\bullet(k)  \big)$ admits the corresponding [[model structure on the Grothendieck construction]].
\end{proposition}

