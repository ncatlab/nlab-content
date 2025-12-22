
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


\tableofcontents


## Idea

The _Kontsevich integral_ is the [[Dyson formula]] for the [[parallel transport]] or [[holonomy]] of the [[Knizhnik-Zamolodchikov connection]] on [[ordered configuration spaces of points]] in the [[plane]]. As such it is a ([[universal Vassiliev invariant|universal]]) [[Vassiliev invariant]] of [[braids]] and, with due care, of [[knots]] and [[links]], essentially coinciding with the [[Wilson loop observable]] of [[perturbative quantization of 3d Chern-Simons theory|perturbatively quantized]] [[Chern-Simons theory]]. 

The Kontsevich integral generalises the [[Gauss integral formula]] which computes the [[linking number]] of two [[embedding of topological spaces|embedded]] [[circles]] via [[integration]].  

## Definition

### On braids
 {#OnBraids}

[[!include Knizhnik-Zamolodchikov-Kontsevich construction -- definition]]




### On knots
 {#OnKnots}

+-- {: .num_definition #kint}
###### Definition

Let $K$ be a [[strict Morse knot]].  Let $\widehat{\mathcal{A}}$ be the [[graded completion]] of the [[algebra of chord diagrams]] with $1$-term relations.  The **Kontsevich integral** of $K$ is given by:

$$
  Z(K) 
  \;=\; 
  \sum_{m = 0}^\infty \frac{1}{(2 \pi i)^m} \int_{t_{\min} \lt t_m \lt \cdots \lt t_1 \lt t_{\max} \over t_j\; \text{non-critical}} \sum_{P = \{(z_j,z_j')\}} (-1)^{\downarrow P} D_p \bigwedge_{j=1}^m \frac{d z_j - d z_j'}{z_j - z_j'}
$$

=--

In this definition:

* $t_{\min}$ and $t_{\max}$ are the minimum and maximum of the $t$-coordinate in the [[Morse knot]] $K$.
* The integration is over the points in the simplex of $m$ points in the interval $[t_{\min},t_{\max}]$ where no coordinate is critical on $K$.
* Upon removing the critical values (note: _values_ not _points_, so we remove a point if it is on the same level as a critical point), the knot decomposes into a set of arcs which can be parametrised by height.  Each arc therefore defines a function $z \colon I \to \mathbb{C}$ where $I$ is the corresponding interval of height values.  In fact, $I$ must be the open interval between two successive critical values of the height function.  For a particular such interval, there must be an even number of arcs with that domain.  Given a point in the simplex (with no critical values), each coordinate in that point lies in an interval between critical values, and then for that interval we choose an unordered pair of arcs.  A choice of pair for each coordinate is called a **pairing**, and is written $P \coloneqq \{(z_j,z_j')\}$.
* For a pairing, $P$, the symbol $\downarrow P$ denotes the number of arcs that are oriented downwards when equipped with the inherited orientation from $K$.
* Putting the knot back together as a circle, we join the ends of the pairing to make a [[chord diagram]] with $m$ chords.  This defines an element in the [[algebra of chord diagrams]] which we denote by $D_P$.

## Invariance

The Kontsevich integral is an invariant of [[Morse knots]] but is not quite a [[knot invariant]].  When a "hump" is introduced to the knot then it is multiplied by $Z(H)$ where $H$ is the "humped" unknot.  Therefore, it can be made in to a genuine knot invariant via the formula
$$
I(K) = \frac{Z(K)}{Z(H)^{c/2}}
$$
where $c$ is the number of critical points of $K$.  To distinguish this from the Kontsevich integral, it is sometimes called the **final** Kontsevich integral (and the other the **preliminary** one).

## Related concepts

* [[Vassiliev invariant]]

* [[universal Vassiliev invariant]]

* [[graph complex]]

* [[Chern-Simons theory]]

## References

### General

Review:

* {#Lescop00} [[Christine Lescop]], _Introduction to the Kontsevich Integral of Framed Tangles_, 2000 ([[LescopKontsevichIntegral.pdf:file]])

* {#Kohno14} [[Toshitake Kohno]], Section 5 of: _Local Systems on Configuration Spaces, KZ Connections and Conformal Blocks_,  Acta Math Vietnam 39, 575–598 (2014)  ([doI;10.1007/s40306-014-0088-6](doi:10.1007/s40306-014-0088-6), [pdf](https://www.ms.u-tokyo.ac.jp/~kohno/papers/kohno_config.pdf))

Textbook account:

* {#Lescop20} [[Christine Lescop]], _Invariants of links and 3-manifolds from graph configurations_ ([arXiv:2001.09929](https://arxiv.org/abs/2001.09929))

[[!include perturbative quantization of Chern-Simons theory -- references]]

[[!redirects Kontsevich integrals]]
