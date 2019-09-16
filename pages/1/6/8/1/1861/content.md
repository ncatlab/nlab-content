
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Where [[homotopy groups]] are groups of [[homotopy classes]] of maps  out [[spheres]], $\pi_n(X)\coloneqq [S^n \to X]$, cohomotopy groups are groups of homotopy classes _into_ spheres, $\pi^n(X) \coloneqq [X \to S^n]$.

If instead one considers mapping into the [[stabilization]] of the spheres, hence into (some [[suspension spectrum|suspension]] of) the [[sphere spectrum]], then one speaks of _[[stable cohomotopy]]_. In other words, the [[generalized (Eilenberg-Steenrod) cohomology]] theory which is [[Brown representability theorem|represented]] by the [[sphere spectrum]] is _stable cohomotopy_.

In this vein, regarding terminology: the concept of [[cohomology]] (as discussed there) in the very general sense of [[non-abelian cohomology]], is about [[homotopy classes]] of maps _into_ any object $A$ (in some [[(∞,1)-topos]]). In this way, general non-abelian cohomology is sort of dual to homotopy, and hence might generally be called co-homotopy. This is the statement of _[[Eckmann-Hilton duality]]_. The duality between homotopy (groups) and co-homotopy proper may then be thought of as being the special case of this where $A$ is taken to be a sphere. 

## Properties

### Hopf degree theorem

+-- {: .num_prop}
###### Proposition
**([[Hopf degree theorem]])**

Let $n \in \mathbb{N}$ be a [[natural number]] and $X \in Mfd$ be a [[connected topological space|connected]] [[orientation|orientable]] [[closed manifold]] of [[dimension]] $n$. Then the $n$th [[cohomotopy]] classes $\left[X \overset{c}{\to} S^n\right] \in \pi^n(X)$ of $X$ are in [[bijection]] to the [[degree of a continuous function|degree]] $deg(c) \in \mathbb{Z}$ of the representing functions, hence the canonical function

$$
  \pi^n(X) 
    \underoverset{\simeq}{S^n \to K(\mathbb{Z},n)}{\longrightarrow}
   H^n(X,\mathbb{Z}) 
     \;\simeq\;   
   \mathbb{Z}
$$

from $n$th [[cohomotopy]] to $n$th [[integral cohomology]] is a [[bijection]].

=--

(e.g. [Kosinski 93, IX (5.8)](#Kosinski93))


### Poincaré–Hopf theorem

* [[Poincaré–Hopf theorem]]

### Relation to Freudenthal suspension theorem

relation to the [[Freudenthal suspension theorem]] ([Spanier 49, section 9](#Spanier49))

### Smooth representatives

For $X$ a [[compact topological space|compact]] [[smooth manifold]], there is a [[smooth function]] $X \to S^n$ representing every cohomotopy class (with respect to the standard [[smooth structure]] on the [[sphere]] [[manifold]]).

### PT-Construction and normally framed submanifolds
  {#RelationToCobordismGroup}

For $X$ a [[closed manifold|closed]] [[smooth manifold]] of [[dimension]] $D$, the [[Pontryagin-Thom construction]] (e.g. [Kosinski 93, IX.5](#Kosinski93)) identifies the [[set]] 

$$
  SubMfd_{/bord}^{d}(X)
$$

of [[cobordism classes]] of  [[closed manifold|closed]] and [[normally framed submanifolds]] $\Sigma \overset{\iota}{\hookrightarrow} X$ of [[dimension]] $d$ inside $X$ with the [[cohomotopy]] $\pi^{D-d}(X)$ of $X$ in degree $D- d$

$$
  SubMfd_{/bord}^{d}(X)
    \underoverset{\simeq}{\;\;\;PT\;\;\;}{\longrightarrow}
  \pi^{D-d}(X)
  \,.
$$

(e.g. [Kosinski 93, IX Theorem (5.5)](#Kosinski93))

In particular, by this [[bijection]] the canonical [[group]] [[structure]] on [[cobordism groups]] in sufficiently high [[codimension]] (essentially given by [[disjoint union]] of [[submanifolds]]) this way induces a group structure on the cohomotopy sets in sufficiently high degree.



{#PontrjaginThomConstructionGraphics}$\,$

<center>
<img src="https://ncatlab.org/nlab/files/PontrjaginThomConstructionI.jpg" width="800">
</center>

Here the [[normal framing]] of the submanifolds plays the role of the [[charge]] in [[Cohomotopy]] which they carry:

{#nCohomotopyChargeOfSubmanifoldsIsNormalFraming}$\,$

<center>
<img src="https://ncatlab.org/nlab/files/nCohomotopyChargeOfSubmanifoldsIsNormalFraming.jpg" width="800">
</center>

For example:

{#nCohomotopyOfEuclideanNSpaceIllustration}$\,$


<center>
<img src="https://ncatlab.org/nlab/files/nCohomotopyOfEuclideanNSpace.jpg" width="840">
</center>

This construction generalizes to [[equivariant cohomotopy]], see [there](equivariant+cohomotopy#PontryaginThomConstruction).

With the [[equivariant Hopf degree theorem]] the above example has the following $\mathbb{Z}_2$-[[equivariant homotopy theory|equivariant]] version (see [there](equivariant+Hopf+degree+theorem#EquivariantCohomotopyOfRepresentationSpheres)):

{#EquivariantnCohomotopyOfEuclideanNOrientifoldIllustration}$\,$


<center>
<img src="https://ncatlab.org/nlab/files/EquivariantNCohomotopyOfEuclideanNOrientifold.jpg" width="840">
</center>


Further by the [[equivariant Hopf degree theorem]] (see [there](equivariant+Hopf+degree+theorem#EquivariantCohomotopyOfRepresentationTori)), this example generalizes to [[equivariant cohomotopy]] of [[toroidal orbifold|toroidal]] [[orientifolds]]:


{#EquivariantnCohomotopyOfToroidalNOrientifoldIllustration}$\,$

<center>
<img src="https://ncatlab.org/nlab/files/EquivariantCohomotopyOfToroidalOrientifold.jpg" width="850">
</center>


\linebreak

### Relation to configuration spaces
  {#RelationToConfigurationSpaces}


+-- {: .num_remark }
###### Remark
**([[configuration space (mathematics)|configuration spaces]] and [[twisted cohomology|twisted]] cohomotopy)**

The [[scanning map equivalence]] ([this Prop.](scanning+map#ScanningMapEquivalence)) identifies the [[configuration space]] of points in $X$ with labels in an [[n-sphere]] with the [[cocycle]]-space/-[[infinity-groupoid]] of $\tau_X$-[[twisted cohomology|twisted]] cohomotopy in degree $\tau + n$, where $\tau_X \coloneqq [S_X(T X)]$ is the class of the [[spherical fibration]] of the tangent bundle.

In particular if $X$ is a [[parallelizable manifold]]/[[framed manifold]], then $\tau_X = dim(X)$ and the equivalence identifies the [[configuration space]] with the plain cohomotopy of $X$ in degree $dim(X) + n$:

$$
  Conf(X,S^n)
  \;\simeq\;
  Maps( X, S^{dim(X) + n} )
  \,.
$$


=--



## Examples

### Of 4-Manifolds
 {#On4Manifolds}

Let $X$ be a [[4-manifold]] which is [[connected topological space|connected]] and [[orientation|oriented]].

The [[Pontryagin-Thom construction]] as [above](#RelationToCobordismGroup) gives for $n \in \mathbb{Z}$ the [[commuting diagram]] of sets

$$
  \array{
     \pi^n(X) 
       &\overset{\simeq}{\longrightarrow}&
     \mathbb{F}_{4-n}(X)
     \\
     {}^{ \mathllap{h^n} }
     \downarrow
       &&
     \downarrow^{ h_{4-n} }
     \\
     H^n(X,\mathbb{Z})
       &\underset{\simeq}{\longrightarrow}&
     H_{4-n}(X,\mathbb{Z})
     \,,
  }
$$

where $\pi^\bullet$ denotes cohomotopy sets, $H^\bullet$ denotes [[ordinary cohomology]], $H_\bullet$ denotes [[ordinary homology]] and $\mathbb{F}_\bullet$ is [[normal bundle|normally]] [[framing|framed]] [[cobordism classes]] of [[normal bundle|normally]] [[framing|framed]] [[submanifolds]]. Finally $h^n$ is the operation of pullback of the generating integral cohomology class on $S^n$ (by the nature of [[Eilenberg-MacLane spaces]]):

$$
  h^n(\alpha) \;\colon\; X \overset{\alpha}{\longrightarrow} S^n \overset{generator}{\longrightarrow} B^n \mathbb{Z}
  \,.
$$

Now 

* $h^0$, $h^1$, $h^4$ are [[isomorphisms]]

* $h^3$ is an isomorphism if $X$ is "odd" in that it contains at least one closed oriented [[surface]] of odd self-intersection, otherwise $h^3$ becomes an isomorphism on a $\mathbb{Z}/2$-[[quotient group]] of $\pi^3(X)$ (which is a group via the [[group]]-[[structure]] of the [[3-sphere]] ([[special unitary group|SU(2)]]))

([Kirby-Melvin-Teichner 12](#KirbyMelvinTeichner12))


\linebreak

## Related concepts


[[!include flavours of cohomotopy -- table]]

$\,$

[[!include Segal completion -- table]]

## References

### General

Original articles include

* {#Borsuk36} [[K. Borsuk]], _Sur les groupes des classes de transformations continues_, CR Acad. Sci. Paris 202.1400-1403 (1936): 2 ([doi:10.24033/asens.603](https://doi.org/10.24033/asens.603))
 
* {#Spanier49} [[Edwin Spanier]], _Borsuk's Cohomotopy Groups_, Annals of Mathematics Second Series, Vol. 50, No. 1 (Jan., 1949), pp. 203-245 ([jstor:1969362](http://www.jstor.org/stable/1969362))

* Franklin P. Peterson, _Some Results on Cohomotopy Groups_, American Journal of Mathematics Vol. 78, No. 2 (Apr., 1956), pp. 243-258 ([jstor:2372514](https://www.jstor.org/stable/2372514))

* [[Jan Jaworowski]], _Generalized cohomotopy groups as limit groups_, Fundamenta Mathematicae 50 (1962), 393-402 ([doi:10.4064/fm-50-4-333-340](https://www.impan.pl/en/publishing-house/journals-and-series/fundamenta-mathematicae/all/50/4), [pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm50/fm50133.pdf))

The relation between cohomotopy classes of manifolds to the [[cobordism group]] is discussed for instance in 

* {#Kosinski93} [[Antoni Kosinski]], chapter IX of _Differential manifolds_, Academic Press 1993 ([pdf](http://www.maths.ed.ac.uk/~v1ranick/papers/kosinski.pdf))

Further discussion includes

* [[Laurence Taylor]], _The principal fibration sequence and the second cohomotopy set_, Proceedings of the Freedman Fest, 235251, Geom. Topol. Monogr., 18, Coventry, 2012 ([arXiv:0910.1781](https://arxiv.org/abs/0910.1781))

* {#KirbyMelvinTeichner12} [[Robion Kirby]], [[Paul Melvin]], [[Peter Teichner]], _Cohomotopy sets of 4-manifolds_, Geometry & Topology Monographs 18 (2012) 161–190 ([arXiv:1203.1608](https://arxiv.org/abs/1203.1608))

See also 

* Wikipedia, _[Cohomotopy group](http://en.wikipedia.org/wiki/Cohomotopy_group)_

* [[eom]], _[Cohomotopy group](https://www.encyclopediaofmath.org/index.php/Cohomotopy_group)_


### Equivariant Cohomotopy

Discussion of the [[stable cohomotopy|stable]] cohomotopy ([[framed manifold|framed]] [[cobordism cohomology theory]]) in the [[equivariant cohomology]]-version of cohomotopy ([[equivariant cohomotopy]]):

* {#Wasserman69} [[Arthur Wasserman]], section 3 of _Equivariant differential topology_, Topology Vol. 8, pp. 127-150, 1969 ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/wasserman.pdf))

* {#Cruickshank03} [[James Cruickshank]], _Twisted homotopy theory and the geometric equivariant 1-stem_, Topology and its Applications Volume 129, Issue 3, 1 April 2003, Pages 251-271 (<a href="https://doi.org/10.1016/S0166-8641(02)00183-9">arXiv:10.1016/S0166-8641(02)00183-9</a>)

and in the [[twisted cohomology]]-version ([[twisted cohomotopy]])

* {#Cruickshank03} [[James Cruickshank]], Section 7 of _Twisted homotopy theory and the geometric equivariant 1-stem_, Topology and its Applications Volume 129, Issue 3, 1 April 2003, Pages 251-271 (<a href="https://doi.org/10.1016/S0166-8641(02)00183-9">arXiv:10.1016/S0166-8641(02)00183-9</a>)


Discussion of [[M-brane]] physics in terms of [[equivariant rational homotopy theory|rational equivariant]] cohomotopy:

* [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_ ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987))

and in terms of [[twisted cohomotopy]]:

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 3 of _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization|Twisted Cohomotopy implies level quantization of the full 6d Wess-Zumino-term of the M5-brane]]_ ([arXiv:1906.07417](https://arxiv.org/abs/1906.07417))




[[!redirects cohomotopy group]]
[[!redirects cohomotopy groups]]

[[!redirects Cohomotopy]]
