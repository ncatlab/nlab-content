
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

A _complex analytic $\infty$-groupoid_ is an [[∞-groupoid]] equipped with [[higher geometry|geometric]] structure in the sense of [[complex analytic geometry]], such that [[complex analytic spaces]] constitute a [[full subcategory]] of the [[n-truncated object in an (∞,1)-topos|0-truncated]] complex analytic $\infty$-groupoids. Hence a complex analytic $\infty$-groupoid is an [[(∞,1)-sheaf]]/[[∞-stack]] on the [[site]] of [[complex manifolds]] (or some of its [[dense subsites]]). This is directly analogous to how [[(∞,1)-sheaves]] over the [[site]] of [[smooth manifolds]] may be regarded as _[[smooth ∞-groupoids]]_.


## Definition

+-- {: .num_defn #TheSites} 
###### Definition

Write $CplxMfd$ for the [[category]] of [[complex manifolds]], regarded as a [[site]] with the standard [[Grothendieck topology]].

Write 

$$
  \mathbb{C}Disc \hookrightarrow SteinSp \hookrightarrow CplxMfd
$$

for the [[full subcategories]] of [[Stein spaces]] and of complex [[polydiscs]], respectively, regarded as [[sites]] by equipping them with the induced [[coverages]].

=--

+-- {: .num_prop}
###### Proposition

The inclusions in def. \ref{TheSites} exhibit [[dense subsite]] inclusions.

=--

+-- {: .num_defn } 
###### Definition

Write

$$
  \mathbb{C}Analytic\infty Grpd \coloneqq Sh_\infty(CplxMfd)
$$

for the [[hypercomplete (∞,1)-topos|hypercomplete]] [[(∞,1)-sheaf (∞,1)-topos]]  over the sites of complex manifolds def. \ref{TheSites}.

=--

+-- {: .num_remark } 
###### Remark

By the discussion at _[[model structure on simplicial presheaves]]_ 
this means that $\mathbb{C}Analytic\infty Grpd$ is equivalently the [[simplicial localization]] of any of the hypercomplete local model structures on simplicial (pre-)sheaves, such as the Joyal [[model structure on simplicial sheaves]].

=--


This is considered in ([Hopkins-Quick 12, section 2.1](#HopkinsQuick12)).

## Properties

### Cohesion
 {#Cohesion}

+-- {: .num_prop #Cohesion} 
###### Proposition

The [[global section geometric morphism]]

$$
  \Gamma
  \;\colon\;
  \mathbb{C}Analytic\infty Grpd
  \longrightarrow
  \infty Grpd
$$

exhibits a [[cohesive (∞,1)-topos]]. 

=--

+-- {: .proof}
###### Proof

We discuss the existence of the extra left adjoint $\Pi$ (the [[shape modality]]). This proceeds essentially as in the discussion of the [[cohesion]] of [[Smooth∞Grpd]] (see there) only that where there one may choose [[good open covers]] here we have to choose genuine [[split hypercovers]] by [[polydiscs]]. The rest of the proof is verbatim as for [[Smooth∞Grpd]].

To start with, since the [[hypercompletion]] depends only on the underlying [[sheaf topos]] of a site we may represent

$$
  \mathbb{C}Analytic\infty Grpd
  \simeq
  L_{lwhe} sPSh(\mathbb{C}Discs)_{proj, loc}
$$

by the [[simplicial localization]] of the [[local model structure on simplicial presheaves]] over $\mathbb{C}Disc$, [[Bousfield localization of model categories|localized]] (by the [theorem of descent recognition along hypercovers](hypercover#DescentFromDescentAlongHypercovers)) at the [[hypercovers]] $U_\bullet\to X$ as seen over $CplxMfd$ restricted to $X$ a [[polydisc]] (this roundabout way since $\mathbb{C}Disc$ does not carry a [[Grothendieck topology]] but just a [[coverage]]).

Now before [[Bousfield localization of model categories|Bousfield localization]] we have a simplicially enriched [[Quillen adjunction]]

$$
  sPSh(\mathbb{C}Disc)_{proj, loc}
  \stackrel{\overset{\underset{\to}{\lim}}{\longrightarrow}}{\underset{\Delta}{\longleftarrow}}
  sSet_{Quillen}
$$

which is simplicial-degree wise just the defining [[adjunction]] of the [[colimit]] functor $\underset{\to}{\lim}$ [[left adjoint]] to the [[constant presheaf]] functor.

To see that this descends to a Quillen adjunction on the local model structure, by the [recognition theorem for simplicial Quillen adjunctions](Quillen+adjunction#RecognitionOfSimplicialQuillenAdjunctions) we hence need to check that $\Delta$ preserves fibrant objects with respect to the local model structure, hence that any constant simplicial presheaf $\Delta S$ for $S$ a [[Kan complex]] already satisfies [[descent]] with respect to [[hypercovers]] as seen over $CplxMfd$.

By the [theorem of descent recognition along hypercovers](hypercover#DescentFromDescentAlongHypercovers) $\Delta S$ satisfies descent precisely if for each [[hypercover]] $U_\bullet \to X$ of any [[polydisc]] $X$. the induced morphism of [[derived hom-spaces]]

$$
  RHom(X, \Delta S) \longrightarrow RHom(U_\bullet, \Delta S)
$$

in the global [[model structure on simplicial presheaves]] is a [[weak equivalence]]. This $RHom$ in turn may be computed as the $sSet$-enriched [[hom object]] out of a cofibrant resolution $\hat X \to X$ and $\hat U_\bullet \to U_\bullet$, respectively. By the [recognition of cofibrant objects in the projective model structure](model%20structure%20on%20simplicial%20presheaves#CofibrantObjects) the [[representable functor|representable]] $X$ is already cofibrant and a sufficient condition for a resolution $\hat U_\bullet \to U_\bullet$ to be cofibrant is that it is a [[split hypercover]].

Since $\mathbb{C}Disc \hookrightarrow CplxMfd$ is a [[dense subsite]], we may always choose such a split hypercover such that $\hat U_\bullet$ consists simplicial-degreewise of [[coproducts]] of [[polydiscs]]: by the proposition at _[hypercover -- Existence of split refinements](hypercover#ExistenceOfSplitRefinements)_

Since the [[colimit]] of a [[representable functor]] is the point, this means that with such a choice $\underset{\to}{\lim} \hat U_\bullet$ is the [[simplicial set]] obtained by replacing in the hypercover by polydiscs each polydisc by a point. Forgetting the [[complex structure]] on all manifolds involved, one sees that this is precisely the "[[etale homotopy type]]" of $X$ as seen by the site [[CartSp]] of [[Cartesian spaces]], by the discussion at _[[Smooth∞Grpd]]_, and this comes out as the ordinary [[homotopy type]] of the underlying [[topological space]] of $X$. But this is of course [[contractible homotopy type|contractible]]. 

In conclusion this means that

$$
  \begin{aligned}
     RHom(U_\bullet, \Delta S)
     &\simeq
     sPSh(\mathbb{C}Disc)(\hat U_\bullet, \Delta S)
     \\
     & \simeq 
     sSet(Sing(X), S)
     \\
     & \simeq 
     sSet(\ast, S)
     \\
     &\simeq S
  \end{aligned}
$$

Therefore the [[descent]] condition for $\Delta S$ is satisfied. (This is also the statement of ([Hopkins-Quick 12, lemma 2.3, prop. 2.4, lemma 2.5, prop. 2.6](#HopkinsQuick12))).

From here on the argument for the [[cohesion]] of $\mathbb{C}Analytic \infty Grpd$ proceeds as at _[[∞-cohesive site]]_ (which might just as well be adapted to the hyper-discussion here).

=--

+-- {: .num_cor #ShapeOfComplexManifold} 
###### Corollary

For $X\in CplxMfd \hookrightarrow \mathbb{C}Analytic\infty Grpd$ a [[complex manifold]], then the [[shape modality|shape]] $\Pi(X)$ is the [[homotopy type]] of its underlying [[topological space]].

=--

In ([Hopkins-Quick 12](#HopkinsQuick12))) this is part of prop. 2.6.

### Oka principle
 {#OkaPrinciple}

Discussion of the [[Oka principle]] in terms of $\mathbb{C}Analytic\infty Grpd$ is in ([Larusson 01](#Larusson01)).

+-- {: .num_defn #OkaManifold}
###### Definition

Say that a [[complex manifold]] $X$ is an _[[Oka manifold]]_ if for every [[Stein manifold]] $\Sigma$ the canonical inclusion

$$
  Maps_{hol}(\Sigma, X) \longrightarrow Maps_{top}(\Sigma, X)
$$


from the [[mapping space]] of [[holomorphic functions]] to that of [[continuous functions]] (both equipped with the [[compact-open topology]]) is a [[weak homotopy equivalence]].

=--

+-- {: .num_theorem}
###### Theorem

This is the case precisely if $Maps_{hol}(-,X) \in Psh_\infty(SteinSp)$ satisfies [[descent]] with respect to [[finite set|finite]] [[covers]].

=--

([Larusson 01, theorem 2.1](#Larusson01))

+-- {: .num_remark}
###### Remark

By corollary \ref{ShapeOfComplexManifold}, in terms of [[cohesion]], prop. \ref{Cohesion}, definition \ref{OkaManifold} should (...check...) read

$$
  \Pi[\Sigma,X] \simeq \flat [\Pi(\Sigma), \Pi(X)]
  \,.
$$

=--


### Complex analytic differential generalized cohomology
 {#DifferentialCohomology}

By prop. \ref{Cohesion} $\mathbb{C}Analytic \infty Grpd$ is [[cohesive (infinity,1)-topos|cohesive]] and hence by the discussion at
_[[differential cohomology hexagon]]_ the objects  $\hat E \in Stab(\mathbb{C}Analytic \infty Grpd)$ (hence the [[sheaves of spectra]] on $\mathbb{C}Mfd$ ) qualify as [[differential cohomology]] refinements of the  [[cohomology theories]] [[Brown representability theorem|represented]] by the [[shape modality|shapes]] $E\coloneqq \Pi \hat E \in $ [[Spectra]].

Discussion of such complex analytic differential generalized cohomology is in ([Hopkins-Quick 12, section 4](#HopkinsQuick12)),.

## Examples

### Multiplicative group and holomorphic line $n$-bundles

The [[multiplicative group]] is a canonical [[∞-group]] object

$$
  \mathbb{G}_m \in Grp(\mathbb{C}Analytic\infty Grpd)
$$

given as an [[(∞,1)-presheaf]] by the assignment

$$
  \mathbb{G}_m \;\colon\; \Sigma \mapsto \mathcal{O}_\Sigma^\times
$$

that sends a [[Stein manifold]] to the multiplicative [[abelian group]] of non-vanishing [[holomorphic functions]] on it.

The [[delooping]] $\mathbf{B}\mathbb{G}_m$ is the universal [[moduli stack]] for [[holomorphic line bundles]] (the [[Picard stack]]) and the double delooping $\mathbf{B}^2 \mathbb{G}_m$ that for [[holomorphic line 2-bundles]] (the [[Brauer stack]]).

## Related concepts

* [[smooth ∞-groupoid]]

* [[complex analytic stack]]

* [[holomorphic line n-bundle]]

## References


* {#Larusson01} [[Finnur Lárusson]], _Excision for simplicial sheaves on the Stein site and Gromov's Oka principle_ ([arXiv:math/0101103](http://arxiv.org/abs/math/0101103))

* [[Jacob Lurie]], section 4.4. of _[[Structured Spaces]]_

* [[Jacob Lurie]], sections 11 and 12 of _[[Closed Immersions]]_

* {#HopkinsQuick12} [[Michael Hopkins]], [[Gereon Quick]], _Hodge filtered complex bordism_, Journal of Topology, **8** 1 (2015) ([arXiv:1212.2173](http://arxiv.org/abs/1212.2173), [doi:10.1112/jtopol/jtu021](https://doi.org/10.1112/jtopol/jtu021))
 
[[!redirects complex analytic ∞-groupoids]]

[[!redirects complex analytic infinity-groupoid]]
[[!redirects complex analytic infinity-groupoids]]

[[!redirects ComplexAnalytic∞Grpd]]
[[!redirects ComplexAnalyticInfinityGrpd]]


[[!redirects complex analytic ∞-stack]]
[[!redirects complex analytic ∞-stacks]]
[[!redirects complex analytic infinity-stack]]
[[!redirects complex analytic infinity-stacks]]
