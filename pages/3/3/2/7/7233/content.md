
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _$G_2$-structure_ on a [[manifold]] $X$ of [[dimension]] 7 is a choice of [[G-structure]] on $X$, for $G$ the [[exceptional Lie group]] [[G2]]. Hence it is a reduction of the structure group]] of the [[frame bundle]] of $X$ along the canonical (the defining) inclusion $G_2 \hookrightarrow GL(\mathbb{R}^7)$ into the [[general linear group]].

Given that $G_2$ is the [[subgroup]] of the [[general linear group]] on the [[Cartesian space]] $\mathbb{R}^7$ which preserves the [[associative 3-form]] on $\mathbb{R}^7$, a $G_2$ structre is a higher analog of an  [[almost symplectic structure]] under lifting from [[symplectic geometry]] to [[2-plectic geometry]] ([Ibort](#Ibort)).

A _$G_2$-manifold_ is a manifold equipped with $G_2$-structure that is integrable/torsion free to first order. This is equivalently a [[Riemannian manifold]] of [[dimension]] 7 with [[special holonomy]] group being the [[exceptional Lie group]] [[G2]]. 

$G_2$-manifolds may be understood as 7-dimensional [[analogs]] of real 6-dimensional [[Calabi-Yau manifolds]].

## Definition

### $G_2$-structure
 {#G2Structure}

+-- {: .num_defn #G2Structure}
###### Definition

For $X$ a [[smooth manifold]] of [[dimension]] $7$ a **$G_2$-structure** on $X$ is a [[G-structure]] for $G = $ [[G2]] $\hookrightarrow GL(7)$.

=--

+-- {: .num_remark #CanonicalRiemannianMetric}
###### Remark

A $G_2$-structure in particular implies an [[orthogonal structure]], hence a [[Riemannian metric]].

=--

Given the definition of [[G2]] as the [[stabilizer group]] of the [[associative 3-form]] on $\mathbb{R}^7$, there is accordingly an equivalent formulation of def. \ref{G2Structure} in terms of [[differential forms]]:


+-- {: .num_defn #Definite3Forms}
###### Definition

Write $\Lambda^3_+(\mathbb{R}^7)^\ast \hookrightarrow \Lambda^3(\mathbb{R}^7)^\ast $ for the [[orbit]] of the [[associative 3-form]] $\phi$ under the canonical $GL(7)$-[[action]]. Similarly for $X$ a [[smooth manifold]] of [[dimension]] 7, write 

$$
  \Omega^3_+(X) \hookrightarrow \Omega^3(X)
$$

for the subset of the set of [[differential 3-forms]] on those that, as [[sections]] to the exterior power of the [[cotangent bundle]], are pointwise in $\Lambda^3_+(\mathbb{R}^7)^\ast$. 

These are also called the _positive forms_ ([Joyce 00, p. 243](Joyce00)) or the _definite forms_ ([Bryant 05, section 3.1.1](#Bryant05)) on $X$.

=--

(e.g. [Bryant 05, definition 2](#Bryant05))

+-- {: .num_prop #G2StructureViaDefinite3Form}
###### Proposition

A $G_2$-structure on $X$, def. \ref{G2Structure}, is equivalently 
a choice of definite 3-form $\sigma$ on $X$, def. \ref{Definite3Forms}.

=--

(e.g. [Joyce 00, p. 243](Joyce00), [Bryant 05, section 3.1.1](#Bryant05))

The following is important for the analysis:

+-- {: .num_remark #Definition3FormsGiveOpenSubset}
###### Remark

The subset $\Lambda^3_+(\mathbb{R}^7)^\ast \hookrightarrow \Lambda^3(\mathbb{R}^7)^\ast $ in def. \ref{Definite3Forms} is an [[open subset]].

=--

(e.g. [Joyce 00, p. 243](#Joyce00), [Bryant 05, 2.8](#Bryant05))

+-- {: .proof}
###### Proof

By definition of $G_2$ as the [[stabilizer group]] of the [[associative 3-form]], the [[orbit]] it generates under the $GL_+(7)$-action is the [[coset]] $GL_+(7)/G_2$. The [[dimension]] of this as a [[smooth manifold]] is 49-14 = 35. This is however already the full dimension $\left(7 \atop 3\right) = 35$ of the space of 3-forms in 7d that the orbit sits in. Therefore (since $G_+(7)/G_2$ does not have a [[manifold with boundary|boundary]]) the orbit must be an open subset.

=--

### Closed $G_2$-structure
 {#ClosedG2Structure}


+-- {: .num_defn #ClosedG2Structure}
###### Definition

A $G_2$-structure, def. \ref{G2Structure}, is called _closed_ if the definite 3-form $\sigma$ corresponding to it via prop. \ref{G2StructureViaDefinite3Form} is a closed differential form, $\mathbf{d}\sigma = 0$.

=--

(e.g. [Bryant 05, (4.31)](#Bryant05))

+-- {: .num_prop #ClosedG2StructureByAtlas}
###### Proposition

For a closed $G_2$-structure, def. \ref{ClosedG2Structure}, on a manifold $X$ there exists an [[atlas]] by [[open subsets]] 

$$\mathbb{R}^7 \underoverset{et}{f}{\leftarrow} U \underset{et}{\rightarrow} X$$ 

such that the globally defined 3-form $\sigma \in \Omega^3_+(X)$ is locally gauge equivalent to the canonical [[associative 3-form]] $\phi$

$$
  \sigma|_U = f^\ast \phi + \mathbf{d}\beta
$$

via a 2-form $\beta$ on $U$.

=--

(e.g. [Bryant 05, p. 21](#Bryant05))

This follows from the fact, remark \ref{Definition3FormsGiveOpenSubset}, that the definite 3-forms are an [[open subset]] inside all 3-forms: given a chart centered around any point then there is $\beta$ with $\mathbf{d}\beta$ vanishing at that point such that $\sigma|_U \simeq f^\ast \phi + \mathbf{d}\beta$ at that point. But since the $GL(7)$-action on $\phi$ is open, there is an open neighbourhood around that point where this is still the case.

+-- {: .num_remark #AtlasForClosedG2tructureInTermsOfHigherGeometry}
###### Remark

When regarding [[smooth manifolds]] in the wider context of [[higher differential geometry]], then the situation of prop. \ref{ClosedG2StructureByAtlas} corresponds to a diagram of [[formal smooth infinity-groupoids]] of the following form:

$$
  \array{
    && U
    \\
    & {}^{\mathllap{f}}\swarrow && \searrow
    \\
    \mathbb{R}^7 && \swArrow_{\mathrlap{\beta}} && X
    \\
    & {}_{\mathllap{\phi}}\searrow && \swarrow_{\mathrlap{\sigma}}
    \\
    && \flat_{dR}\mathbf{B}^3\mathbb{R}
  }
  \,,
$$

where $\flat_{dR}\mathbf{B}^3\mathbb{R}$ is the [[moduli infinity-stack|higher moduli stack]] of flat 3-forms with 2-form gauge transformations between them (and 1-form gauge transformation between these). The diagram expresses the 3-form $\sigma$ as a map to this moduli stack, which when restricted to the cover $U$ becomes gauge equivalent to the pullback of the [[associative 3-form]] $\phi$, similarly regarded as a map, to the cover, where the gauge equivalence is exhibited by a [[homotopy]]  (of maps of formal smooth $\infty$-groupoids) which is the 2-form $\beta$ on $U$.

=--

Since the GL-transformations in questions define a [[vielbein]] field $E$, one may also ask for $\sigma$ to be locally of the form $\phi_{a_1 a_2 a_3}E^{a_1}\wedge E^{a_2}\wedge E^{a_3}$ (...) (e.g. [BGGG 01 (2.9)](#BGGG01))


### $G_2$-holonomy
 {#G2Holonomy}

+-- {: .num_defn #G2manifold}
###### Definition

A manifold equipped with a $G_2$-structure, def. \ref{G2Structure}, is called a **$G_2$-manifold** if the 3-form $\omega$ corresponding to it via prop. \ref{G2StructureViaDefinite3Form} satisfies 

1. $\mathbf{d} \omega = 0$ 

1. $\mathbf{d} \star \omega = 0$

(where $d$ is the [[de Rham differential]] and $\star$ is the [[Hodge star operator]] of the canonical [[Riemannian metric]] of remark \ref{CanonicalRiemannianMetric}).

Equivalently this means that $\omega$ is [[covariant derivative|covariantly constant]]

$$
  \nabla \omega = 0
  \,.
$$

=--

For instance ([Joyce, p. 4](#Joyce)).


The [[holonomy]] of the [[Levi-Civita connection]] on a $G_2$-manifold is contained in $G_2$.

### Weak $G_2$-holonomy
 {#WeakG2Holonomy}

There is a useful weakened notion of $G_2$-holonomy. 

+-- {: .num_defn #WeakG2Holonomy}
###### Definition

A 7-dimensional manifold is said to be of _weak $G_2$-holonomy_ if it carries a 3-form $\omega$ with the relation of def. \ref{G2manifold} generalized to

$$
  d \omega = \lambda \star \omega
$$

and hence

$$
  d \star \omega = 0
$$

for $\lambda \in \mathbb{R}$. For $\lambda = 0$ this reduces to strict $G_2$-holonomy, by \ref{G2manifold}. 

=--

(See for instance ([Bilal-Derendinger-Sfetsos 02](#BilalDerendingerSfetsos), [Bilal-Metzger 03](#BilalMetzger03)).)



## Properties

### Existence

+-- {: .num_prop }
###### Proposition

A 7-manifold admits a $G_2$-structure, def. \ref{G2Structure}, precisely if it admits a [[spin structure]].

=--

### Metric structure

The canonical [[Riemannian metric]] $G_2$ manifold is [[Ricci tensor|Ricci flat]]. More generally a manifold of weak $G_2$-holonomy, def. \ref{WeakG2Holonomy}, with weakness parameter $\lambda$ is an [[Einstein manifold]] with [[cosmological constant]] $\lambda$. 

## Applications

### In supergravity 

In [[string phenomenology]] [[model (in particle phyiscs)|models]] obtained from [[Kaluza-Klein mechanism|compactification]] of [[11-dimensional supergravity]]/[[M-theory on G2-manifolds]] (see for instance [Duff](#Duff)) can have attractive [[phenomenology|phenomenological]] properties, see for instance the _[[G2-MSSM]]_. 

## Related concepts

[[!include special holonomy table]]

* [[Hitchin functional]]

* [[M-theory on G2-manifolds]], [[G2-MSSM]]

* [[topological M-theory]], [[topological membrane]]

* [[generalized G2-manifold]]

* [[Calabi-Yau manifold]]

* [[exceptional generalized geometry]]

## References

### General

The concept goes back to 

* E. Bonan, (1966), _Sur les vari&#233;t&#233;s riemanniennes &#224; groupe d'holonomie G2 ou Spin(7)_, C. R. Acad. Sci. Paris 262: 127&#8211;129.

Non-compact $G_2$-manifolds were constructed in

* [[Robert Bryant]], ; S.M. Salamon,  (1989), _On the construction of some complete metrics with exceptional holonomy_, Duke Mathematical Journal 58: 829&#8211;850.

[[compact topological space|Compact]] $G_2$-manifolds were first found in 

* {#Joyce}[[Dominic Joyce]], _Compact Riemannian 7-manifolds with holonomy $G_2$_, Journal of Differential Geometry vol 43, no 2 ([Euclid](https://projecteuclid.org/euclid.jdg/1214458109))
 
* {#Joyce00} [[Dominic Joyce]], _Compact Manifolds with Special Holonomy_, Oxford Mathematical Monographs, Oxford University Press (2000)

Surveys include

* Spiro Karigiannis, _What is... a $G_2$-manifold_ ([pdf](http://www.ams.org/notices/201104/rtx110400580p.pdf))

* Spiro Karigiannis, _$G_2$-manifolds -- Exceptional structures in geometry arising from exceptional algebra_ ([pdf](http://www.math.uwaterloo.ca/~karigian/talks/waterloo.pdf)) 


* {#Bryant05} [[Robert Bryant]], _Some remarks on $G_2$-structures_, Proceedings of the 12th G&#246;kova Geometry-Topology Conference 2005, pp. 75-109 [pdf](http://gokovagt.org/proceedings/2005/ggt05-bryant.pdf)


The relation to [[multisymplectic geometry]]/[[2-plectic geometry]] is mentioned explicitly in 

* {#Ibort} Alberto Ibort, _Multisymplectic geometry: generic and exceptional_, _[Proceedings of the IX Fall workshop on geometry and physics](http://rsme.es/public/publi3.htm)_ ([[IbortMultisymplectic.pdf:file]])
 

(but beware of some mistakes in that article...)

For more see the references at _[[exceptional geometry]]_.
 


### Application in supergravity

The following references discuss the role of $G_2$-manifolds in [[M-theory on G2-manifolds]]:

* [[Mike Duff]], _M-theory on manifolds of G2 holonomy: the first twenty years_ ([arXiv:hep-th/0201062](http://arxiv.org/abs/hep-th/0201062))
 {#Duff}

A survey of the corresponding [[string phenomenology]] for [[M-theory on G2-manifolds]] (see there for more) is in

* [[Bobby Acharya]], _$G_2$-manifolds at the CERN Large Hadron collider and in the Galaxy_, talk at _$G_2$-days_ (2012) ([pdf](http://www.mth.kcl.ac.uk/~tbmadsen/acharya.pdf))

See also

* {#BGGG01} Andreas Brandhuber, Jaume Gomis, Steven S. Gubser, [[Sergei Gukov]], _Gauge Theory at Large N and New G_2 Holonomy Metrics_, Nucl.Phys. B611 (2001) 179-204 ([arXiv:hep-th/0106034](http://arxiv.org/abs/hep-th/0106034))

Weak $G_2$-holonomy is discussed in

* [[Adel Bilal]], J.-P. Derendinger, K. Sfetsos, _(Weak) $G_2$ Holonomy from Self-duality, Flux and Supersymmetry_, Nucl.Phys. B628 (2002) 112-132 ([arXiv:hep-th/0111274](http://arxiv.org/abs/hep-th/0111274))
 {#BilalDerendingerSfetsos}

* {#BilalMetzger03} [[Adel Bilal]], Steffen Metzger, _Compact weak $G_2$-manifolds with conical singularities_ ([arXiv:hep-th/0302021](http://arxiv.org/abs/hep-th/0302021))

* {#HouseMicu04} Thomas House, Andrei Micu, _M-theory Compactifications on Manifolds with $G_2$ Structure_ ([arXiv:hep-th/0412006](http://arxiv.org/abs/hep-th/0412006))

For more on this see at _[[M-theory on G2-manifolds]]_

[[!redirects G2 manifolds]]
[[!redirects G2-manifold]]
[[!redirects G2-manifolds]]

[[!redirects G2 structure]]
[[!redirects G2-structure]]
[[!redirects G2 structures]]
[[!redirects G2-structures]]

[[!redirects weak G2-holonomy]]
[[!redirects weak G2 holonomy]]