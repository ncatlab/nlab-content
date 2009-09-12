This entry is about a theorem by [[Dominic Verity]] that characterizes the [[descent]] condition for [[infinity-stack]]s that take values not in arbitrary [[infinity-groupoid]]s, but just in [[strict omega-groupoid]]s.

The details are here:

* [[Dominic Verity]], _[[VerityDescent.pdf:file]]_ (pdf)

Here is an abstract that served as an abstract for a talk on this at the _Australian Category Seminar_ at Macquarie University on Wednesday 27th of May 2009.

<strong>Abstract</strong>

>In the literature one can find a number of different [[limit]] notions which one might refer to as a "[[descent]] construction". Generally speaking, these may all be regarded as a kind of [[weak limit|lax, pseudo]] or [[homotopy limit]] of a [[simplicial object|co-simplicial diagram]] of objects in some theory of "spatially-enriched" categories. While each of these notions certainly deserves to bear the [[descent]] name, it is not necessarily immediately clear how they may be related in any more specific mathematical sense.

>Recently I was asked by [[Urs Schreiber]] if I knew how a couple of these descent notions might be related formally, and so spent a little time contemplating this problem. My hope is that this talk might achieve two things, firstly I hope to provide a little of the intuition which leads us to define and study such descent constructions. Then I would like to discuss a specific answer to Urs' question, which gives a precise relationship between [[Ross Street]]'s [descent construction](http://arxiv.org/abs/math.CT/0303175) for [[strict omega-category|strict omega-categories]] (or more precisely [[strict omega-groupoid]]s in this case) and the [[descent for simplicial presheaves|simplicial descent construction]] used to characterise the fibrant objects in [[model structure on simplicial presheaves|model categories of simplicial sheaves]].

#Idea#

Generally, [[models for infinity-stack (infinity,1)-toposes]] are provided by a [[model structure on simplicial presheaves|model structure on presheaves with values in simplicial sets]].

As for all [[combinatorial simplicial model category|combinatorial simplicial model categories]] the $(\infty,1)$-topos [[presentable (infinity,1)-category|presented]] by this model structure is the full [[SSet]]-[[enriched category|enriched subcategory]] on fibrant and cofibrant objects.

By a theorem by Dugger-Isaksen-Hollander on the projective [[local model structure on simplicial presheaves]] the _fibrant_ simplicial presheaves are those that 

* take values in [[infinity-groupoid]]s (i.e. the [[simplicial set]]s assigned by them are [[Kan complex]]es) 

* and satisfy [[descent]].

While general [[infinity-groupoid]]s are useful due to their generality and conceptual simplicity, for many concrete computations it is useful to get a more concrete [[algebraic definition of higher category|algebraic model]] and consider just [[strict omega-groupoid]]s. Under the [[oriental]]-[[nerve]] 

$$
  Str \omega Grpd \stackrel{N}{\hookrightarrow} \infty Grpd
$$

the strict $\omega$-groupoids form a [[subcategory]] of all [[infinity-groupoid]]s. This is to be regarded as a refinement of the [[Dold-Kan correspondence]] which embeds strict $\omega$-groupoids _with abelian group structure_ equivalently modeled as [[chain complex]]es into all $\infty$-groupoids

$$
  Ch_+
  \stackrel{\simeq}{\to} StrAb \omega Grpd
  \hookrightarrow
  Str \omega Grpd \stackrel{N}{\hookrightarrow} \infty Grpd
  \,.
$$

It is a familiar process to restrict general [[infinity-stack]]s to those that factor through the entire inclusion: this is the topic of [[homological algebra]] and restricts the general notion of [[cohomology]] to that of [[abelian sheaf cohomology]].

What we are interested in here is a notion in between the fully strictly abelian context and the fully general context: that of strict $\omega$-groupoid valued $\infty$-stacks inside all $\infty$-stacks. This may be thought of as [[nonabelian algebraic topology|nonabelian homological algebra]] that uses not [[chain complex]]es of sheaves but [[crossed complex]]es.

In his work

* [[Ross Street]], _Categorical and combinatorial aspects of descent theory_ ([arXiv](http://arxiv.org/abs/math.CT/0303175))

Ross Street had proposed a formulation of the [[descent]] condition for such $Str \omega Grpd$-valued $\infty$-stacks (see the corresponding section at [[descent]] for the details).

The question remained open how that definition of descent on $Str \omega Grpd$-valued presheaves relates to the general one of $\infty Grpd$-valued presheaves under the above inclusion.

It is this question that Dominic Verity's theorem answers.

In words, Verity's theorem says that Ross Street's descent conditon on a $Str \omega Grpd$-valued presheaf $A$ is the correct one if the [[hypercover]] $\pi : Y \to X$  along which one checks descent is sufficiently well behaved -- in that the [[simplicial object|cosimplicial]] $\infty$-groupoid $A(Y)$ is [[Reedy category|Reedy fibrant]]. 


[[!redirects Verity on descent for strict omega-groupoid valued presheave]]