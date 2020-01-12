
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


# The Kontsevich Integral
* table of contents
{: toc}

## Idea

The _Kontsevich integral_ is the [[Dyson formula]] for the [[parallel transport]] or [[holonomy]] of the [[Knizhnik-Zamolodchikov connection]] on [[ordered configuration spaces of points]] in the [[plane]]. As such it is a ([[universal Vassiliev invariant|universal]]) [[Vassiliev invariant]] of [[braids]] and, with due care, of [[knots]] and [[links]], essentially coinciding with the [[Wilson loop observable]] of [[perturbative quantization of 3d Chern-Simons theory|perturbatively quantized]] [[Chern-Simons theory]]. 

The Kontsevich integral generalises the [[Gauss integral formula]] which computes the [[linking number]] of two [[embedding of topological spaces|embedded]] [[circles]] via [[integration]].  

## Definition

### On braids
 {#OnBraids}

For the following Definition \ref{KnizhnikZamolodchikovConnection} of the [[Knizhnik-Zamolodchikov connection]] we need the following notation:

1. **[[configuration spaces of points]]**

   For $N_{\mathrm{f}} \in \mathbb{N}$ write 

   \[
     \label{OrderedConfigurationSpaceofnPointsinC}
     \underset{{}^{\{1,\cdots,N_{\mathrm{f}}\}}}{Conf}(\mathbb{R}^2)
     \;\coloneqq\;
     (\mathbb{R}^2)^n \backslash FatDiagonal
   \]

   for the [[ordered configuration space of n points]] in the [[plane]], regarded as a [[smooth manifold]].

   Identifying the plane with the [[complex plane]] $\mathbb{C}$, we have canonical [[holomorphic function|holomorphic]] [[coordinate functions]]

   \[
     \label{CoordinateFunctionsOnConfC}
     (z_1, \cdots, z_{N_{\mathrm{f}}})
     \;\colon\;
     \underset{{}^{\{1,\cdots,n\}}}{Conf}(\mathbb{R}^2)
     \longrightarrow
     \mathbb{C}^{N_{\mathrm{f}}}
     \,.
   \]

1. **[[horizontal chord diagrams]]**

   \[
     \label{HorizontalChordDiagrams}
     \mathcal{A}^{{}^{pb}}_{N_{\mathrm{f}}}
     \;\coloneqq\;
     Span\big(\mathcal{D}^{{}^{pb}}_{N_{\mathrm{f}}}\big)/4T
   \]

   for the [[quotient vector space]] of the [[linear span]] of [[horizontal chord diagrams]] on $n$ strands by the [[4T relations]] ([[infinitesimal braid relations]]), regarded as an [[associative algebra]] under [[concatenation]] of strands ([here](horizontal+chord+diagram#AlgebraOfHorizontalChordDiagrams)).

+-- {: .num_defn #KnizhnikZamolodchikovConnection}
###### Definition
**([[Knizhnik-Zamolodchikov form]])**

The _universal [[Knizhnik-Zamolodchikov form]]_ is the [[horizontal chord diagram]]-[[Lie algebra valued differential form|algebra valued differential form]] (eq:HorizontalChordDiagrams) on the [[configuration space of points]]  (eq:OrderedConfigurationSpaceofnPointsinC)

\[
  \label{UniversalKnizhnikZamolodchikovForm}
  \omega_{KZ}
  \;\in\;
  \Omega
  \big(
    \underset{{}^{\{1,\cdots,N_{\mathrm{f}}\}}}{Conf}(\mathbb{C})
    \,,
    \mathcal{A}^{{}^{pb}}_{N_{\mathrm{f}}}
  \big)
\]

given in the canonical [[coordinates]] (eq:CoordinateFunctionsOnConfC) by:

\[
  \label{DefineUniversalKnizhnikZamolodchikovForm}
  \omega_{KZ}
  \;\coloneqq\;
  \underset{ i \lt j \in \{1, \cdots, n\} }{\sum}
  d_{dR} log\big( z_i - z_j \big)
  \otimes t_{i j}
  \,,
\]

where 

<center>
<img src="https://ncatlab.org/nlab/files/HorizontalChordGenerator.jpg" width="500>
</center>

is the horizontal chord diagram with exactly one chord, which stretches between the $i$th and the $j$th strand.

Regarded as a connection form for a [[connection on a vector bundle]], this defines the universal _[[Knizhnik-Zamolodchikov connection]]_ $\nabla_{KZ}$, with [[covariant derivative]]

$$
  \nabla \phi
  \;\coloneqq\;
  d \phi + \omega_{KV} \wedge \phi
$$

for any [[smooth function]]

$$
  \phi \;\colon\;
    \underset{{}^{\{1,\cdots,N_{\mathrm{f}}\}}}{Conf}(\mathbb{C})
  \longrightarrow
  \mathcal{A}^{{}^{pb}}_{N_{\mathrm{f}}} Mod 
$$

with values in [[modules]] over the algebra of [[horizontal chord diagrams]] [[quotient space|modulo]] [[4T relations]].

The condition of covariant constancy

$$
  \nabla_{KZ} \phi \;=\; 0
$$

is called the _Knizhnik-Zamolodchikov equation_.

Finally, given a [[metric Lie algebra]] $\mathfrak{g}$ and a [[tuple]] of [[Lie algebra representations]] 

$$
  (
    V_1, 
      \cdots,
    V_{N_{\mathrm{f}}}
  ) 
  \;\in\; (\mathfrak{g} Rep_{/\sim})^{N_{\mathrm{f}}}
  \,,
$$

the corresponding [[endomorphism]]-valued [[Lie algebra weight system]]

$$
  w_{V} 
  \;\colon\;
  \mathcal{A}^{{}^{pf}}_{N_{\mathrm{f}}}
  \longrightarrow
  End_{\mathfrak{g}}\big( V_1 \otimes \cdots V_{N_{\mathrm{f}}}  \big) 
$$

turns the universal [[Knizhnik-Zamolodchikov form]] (eq:UniversalKnizhnikZamolodchikovForm) into a [[endomorphism ring]]-[[Lie algebra valued differential form|valued differential form]]

\[
  \label{LieKnizhnikZamolodchikovForm}
  \omega_{KZ}
  \;\coloneqq\;
  \underset{ i \lt j \in \{1, \cdots, n\} }{\sum}
  d_{dR} log\big( z_i - z_j \big)
  \otimes w_V(t_{i j})
  \;\in\;
  \Omega
  \big(
    \underset{{}^{\{1,\cdots,N_{\mathrm{f}}\}}}{Conf}(\mathbb{C})
    \,,
    End\big(V_1 \otimes \cdot V_{N_{\mathrm{f}}} \big)
  \big)

  \,.
\]

=--

The universal formulation (eq:UniversalKnizhnikZamolodchikovForm) is highlighted for instance in [Lescop 00, p. 7](#Lescop00). Most authors state the version after evaluation in a [[Lie algebra weight system]], e.g. [Kohno 14, Section 5](#Kohno14).

+-- {: .num_prop #KnizhnikZamolodchikovConnectionIsFlat}
###### Proposition
**([[Knizhnik-Zamolodchikov connection]] is [[flat connection|flat]])**

The [[Knizhnik-Zamolodchikov connection]] $\omega_{ZK}$ (Def. \ref{KnizhnikZamolodchikovConnection}) is [[flat connection|flat]]:

$$
  d \omega_{ZK} + \omega_{ZK} \wedge \omega_{ZK}
  \;=\;
  0
  \,.
$$

=--

+-- {: .num_prop #KontsevichIntegralForBraids}
###### Proposition
**([[Kontsevich integral]] for [[braids]])**

The [[Dyson formula]] for the [[holonomy]] of the [[Knizhnik-Zamolodchikov connection]] (Def. \ref{KnizhnikZamolodchikovConnection}) is called the _[[Kontsevich integral]] on [[braids]]_.

=--

(e.g. [Lescop 00, side-remark 1.14](#Lescop00))

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

[[!include perturbative quantization of Chern-Simons theory -- references]]

[[!redirects Kontsevich integrals]]
