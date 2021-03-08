

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The effective bosonic exponentiated [[action functional]] of the [[type II superstring]] [[sigma-model]] for [[open strings]] ending on [[D-branes]] has three factors:

1. the [[higher holonomy]] of the background [[B-field]] over the string 2-dimensional worldsheet;

1. the ordinary [[holonomy]] of the [[Chan-Paton bundle]] on the D-brane along the boundary of the string;

1. the [[Berezin integral|Berezinian]] [[path integral]] over the fermions.

Each single contribution is in general not a globally well defined function on the space of string configurations, instead each is a [[section]] of a possibly non-trivial [[line bundle]] over the configuration space (the last one for instance of the [[Pfaffian bundle]]). Therefore the total action functional is a section of the [[tensor product]] of these three line bundles.

The non-triviality of this tensor product line bundle (as a line bundle [[connection on a bundle|with connection]]) is the _Freed-Witten-Kapustin [[quantum anomaly]]_. The necessary conditions for this anomaly to vanish, hence for this line bundle to be trivializable, is the _Freed-Witten anomaly cancellation condition_.

More precisely, the naive holonomy of an ordinary Chan-Paton [[principal connection]] would be globally well defined. But in order to cancel the anomaly contribution from the other two factors, one may take the Chan-Paton bundle to be a [[twisted bundle]], the twist being the [[B-field]] restricted to the brane. Then its holonomy becomes anomalous, too, but there are then interesting configurations where the product of all three anomalies cancels. This refined argument has been made precise by Kapustin, and so one should probably speak of the _Freed-Witten-Kapustin anomaly cancellation_.

## Details
 {#Details}

We interpret the Freed-Witten-Kapustin mechanism in terms of [[push-forward in generalized cohomology]] in [[topological K-theory]] interpreted in terms of [[KK-theory]] with push-forward maps given by [[dual morphisms]] between [[Poincaré duality C*-algebras]] (based on [Brodzki-Mathai-Rosenberg-Szabo 06, section 7](#BrodzkiMathaiRosenbergSzabo06), [Tu 06](#Tu06)):

Let $i \colon Q \to X$ be a map of [[compact topological space|compact]] [[manifolds]] and let $\chi \colon X \to B^2 U(1)$ modulate a [[circle 2-bundle]] regarded as a [[twisted K-theory|twist for K-theory]]. Then forming [[twisted groupoid convolution algebras]] yields a [[KK-theory]] morphism of the form

$$
  C_{i^\ast \chi}(Q)
  \stackrel{i^\ast}{\longleftarrow}
  C_{\chi}(X)
  \,,
$$

with notation as in [this definition](Poincar&#233;+duality+algebra#CStarAlgebraOf2BundleOnManifold). By [this proposition](Poincar&#233;+duality+algebra#DualOfCompactManifoldWithTwist) the [[dual morphism]] is of the form

$$
  C_{\frac{1}{i^\ast \chi \otimes W_3(T Q)}}(Q)
  \stackrel{i_!}{\longrightarrow}
  C_{\frac{1}{\chi \otimes W_3(T X)}}(X)
  \,.
$$

If we redefine the twist on $X$ to absorb this "quantum correction" as $\chi \mapsto \frac{1}{\chi \otimes W_3(T X)}$ then this is

$$
  C_{i^\ast \chi\frac{W_3(i^\ast T X)}{W_3(T Q)}}(Q)
  \stackrel{i_!}{\longrightarrow}
  C_{\chi}(X)
  \,,
$$

where now we may interpret $\frac{W_3(i^\ast \tau_X)}{W_3(\tau_Q)}$ as the third [[integral Stiefel-Whitney class]] of the [[normal bundle]] $N Q$ of $i$ (see [Nuiten](#Nuiten)).

Postcomposition with this map in [[KK-theory]] now yields a map from the $i^\ast \chi \otimes W_3(N Q)$-[[twisted K-theory]] of $Q$ to the $\chi$-[[twisted K-theory]] of $X$:

$$
  i_! \colon K_{\bullet + W_3(N Q) + i^\ast \chi}(Q) \to K_{\bullet +\chi}(X)
  \,.
$$

If we here think of $i \colon Q \hookrightarrow X$ as being the inclusion of a [[D-brane]] [[worldvolume]], then $\chi$ would be the class of the [[background gauge field|background]] [[B-field]] and an element 

$$
  [\xi] \in K_{\bullet + W_3(N Q) + i^\ast \chi}(Q)
$$ 

is called (the K-class of) a _[[Chan-Paton gauge field]]_ on the D-brane satisfying the **Freed-Witten-Kapustin anomaly cancellation** mechanism. (The orginal **Freed-Witten anomaly cancellation** assumes $\xi$ given by a [[twisted unitary bundle|twisted line bundle]] in which case it exhibits a [[twisted spin^c structure]] on $Q$.) Finally its [[fiber integration|push-forward]]

$$
  [i_! \xi] \in K_{\bullet + \chi}(X)
$$

is called the corresponding _[[D-brane charge]]_.




## Related concepts

* [[D-brane]], [[D-brane charge]], [[fractional D-brane]]

* [[twisted spin^c structure]]

* [[Spin^c Dirac operator]]

* [[Green-Schwarz mechanism]]

[[!include orientations in higher quantization - table]]



## References
 {#References}

### General

The special case where the class of the restriction of the [[B-field]] to the D-brane _equals_ the third [[integral Stiefel-Whitney class]] of the D-brane was discussed in

* [[Daniel Freed]], [[Edward Witten]], _Anomalies in String Theory with D-Branes_ ([arXiv:hep-th/9907189](http://arxiv.org/abs/hep-th/9907189))

The generalization to the case that the two classes differ by a [[torsion]] class was considered in

* {#Kapustin99} [[Anton Kapustin]], _D-branes in a topologically nontrivial B-field_, Adv. Theor. Math. Phys. 4, no. 1, pp. 127&#8211;154 (2000), ([arXiv:hep-th/9909089](http://arxiv.org/abs/hep-th/9909089))

Aspects of the interpretation of this by [[push-forward in generalized cohomology]] in [[twisted K-theory]] are formalized in 

* [[Alan Carey]], [[Bai-Ling Wang]], _Thom isomorphism and Push-forward map in twisted K-theory_ ([arXiv:math/0507414](http://arxiv.org/abs/math/0507414))
 {#CareyWang05}

and section 10 of

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 {#AndoBlumbergGepner10}

(which discusses twists as [[(infinity,1)-module bundles]]).

The formulation by postcomposition with [[dual morphisms]] in [[KK-theory]] which we use above is based on the observations in section 7 of 

* Jacek Brodzki, [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], _D-Branes, RR-Fields and Duality on Noncommutative Manifolds_, Commun. Math. Phys. 277:643-706,2008 ([arXiv:hep-th/0607020](http://arxiv.org/abs/hep-th/0607020))
 {#BrodzkiMathaiRosenbergSzabo06}

and generalized to equivariant [[KK-theory]] in

* [[Jean-Louis Tu]], _Twisted K-theory and Poincar&#233; duality_ ([arXiv:math/0609556](http://arxiv.org/abs/math/0609556))
 {#Tu06}



A clean formulation and review is provided in

* Loriano Bonora, Fabio Ferrari Ruffino, Raffaele Savelli, _Classifying A-field and B-field configurations in the presence of D-branes_ ([arXiv:0810.4291](http://arxiv.org/abs/0810.4291))

* Fabio Ferrari Ruffino, _Topics on topology and superstring theory_ ([arXiv:0910.4524](http://arxiv.org/abs/0910.4524))

* Fabio Ferrari Ruffino, _Classifying A-field and B-field configurations in the presence of D-branes - Part II: Stacks of D-branes_ ([arXiv:1104.2798](http://arxiv.org/abs/1104.2798))

* Raffaele Savelli, _On Freed-Witten Anomaly and Charge/Flux quantization in String/F Theory_, Phd thesis (2011) ([pdf](http://digitallibrary.sissa.it/bitstream/handle/1963/4999/PhDthesisSavelli.pdf?sequence=1))

and

* Kim Laine, _Geometric and topological aspects of Type IIB D-branes_, Master thesis ([arXiv:0912.0460](http://arxiv.org/abs/0912.0460))
 {#Laine}

In ([Laine](#Laine)) the discussion of FW-anomaly cancellation with finite-rank gauge bundles is towards the very end, culminating in equation (3.41).

A discussion from the point of view of [[higher geometric quantization]] or [[extended prequantum field theory]] is at the end of

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_ . 

Lecture notes along these lines are in _[Lagrangians and Action functionals -- 3d Chern-Simons theory](#3dCSTheory)_ of

* _[[geometry of physics]]_ .

The [[KK-theory]]-description of the FEK anomaly used above is discussed in 

* [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_, master thesis, August 2013
 {#Nuiten}

### Relation to shifted C-field flux

On relating the [[Freed-Witten anomaly]] to the [[shifted C-field flux quantization]]:

On [[D4-branes]]:

* [[Edward Witten]], Section 2 of: _Duality Relations Among Topological Effects In String Theory_, JHEP 0005:031, 2000 ([arXiv:hep-th/9912086](https://arxiv.org/abs/hep-th/9912086))

On [[D6-branes]]:

* [[Sergei Gukov]], [[James Sparks]], p. 21 of: _M-Theory on $Spin(7)$ Manifolds_, Nucl. Phys. B625 (2002) 3-69 ([arXiv:hep-th/0109025](https://arxiv.org/abs/hep-th/0109025))

* [[James Sparks]], _Global Worldsheet Anomalies from M-Theory_, JHEP 0408:037, 2004 ([arXiv:hep-th/0310147](https://arxiv.org/abs/hep-th/0310147))



[[!redirects Freed-Witten anomaly cancellation]]

[[!redirects Freed-Witten quantum anomaly]]
[[!redirects Freed-Witten quantum anomaly cancellation]]

[[!redirects Freed-Witten-Kapustin anomaly]]
[[!redirects Freed-Witten-Kapustin anomaly cancellation]]

[[!redirects Freed-Witten-Kapustin quantum anomaly]]
[[!redirects Freed-Witten-Kapustin quantum anomaly cancellation]]

