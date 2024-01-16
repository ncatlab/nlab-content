
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

An [[8-manifold]] of [[special holonomy]] [[Spin(7)]].

Equivalently: an [[8-manifold]] equipped with a globalization of the [[Cayley 4-form]].

## Properties

### As part of the Berger classification

[[!include special holonomy table]]

### As $\mathbb{O}$-Riemannian manifolds

[[!include normed division algebra Riemannian geometry -- table]]

### As exceptional geometry

[[!include Spin(8)-subgroups and reductions -- table]]

### Relation to J-twisted Cohomotopy
 {#RelationToJTwistedCohomotopy}

On a [[spin-manifold]] [[8-manifold|of dimension 8]] a choice of topological [[Spin(7)]]-[[G-structure|structure]] is equivalently a choice of [[cocycle]] in [[J-homomorphism|J-]][[twisted Cohomotopy cohomology theory]]. This follows ([[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation|FSS 19, 3.4]]) from 

1. the standard [[coset space]]-[[structures]] on the [[7-sphere]] (see [here](7-sphere#CosetSpaceRealization)) 

1. the fact that [[coset spaces]] $G/H$ are the [[homotopy fibers]] of the maps $B H \to B G$ of the corresponding [[classifying spaces]] (see [here](coset#ForInfinityGroups))

\begin{imagefromfile}
  "file_name": "ExceptionalSpheres.jpg",
  "width": 730
\end{imagefromfile}

### Characteristic classes

+-- {: .num_prop #CharacteristicClassesForSpinStructure}
###### Proposition

Let $X$ be a  [[closed manifold|closed]] [[smooth manifold]] of [[dimension]] 8 with [[Spin structure]]. If the [[frame bundle]] moreover admits [[G-structure]] for 

$$
  G = Spin(7) \hookrightarrow Spin(8)
$$ 

then the [[Euler class]] $\chi$, the [[second Pontryagin class]] $p_2$ and the [[cup product]]-square $(p_1)^2$ of the [[first Pontryagin class]] (the combination proportional to the [[I8]]-term) of the [[frame bundle]]/[[tangent bundle]] are related by

\[
  \label{EulerClassInTermsOfPontryagin}
  8 \chi
  \;=\;
  4 p_2 - (p_1)^2
  \,.
\]


=--

([Isham-Pope 88 (3.36)](#IshamPope88))

+-- {: .num_remark}
###### Remark

The same conclusion (eq:EulerClassInTermsOfPontryagin) also holds for [[Spin(5).Spin(3)]]-structure, see [there](quaternion-Kähler+manifold#CharacteristicClassesForSpin5Spin3Structure).

=--

See also at _[[C-field tadpole cancellation]]_.

\linebreak

## Related concepts

* [[Spin(7)-instanton]]

* [[M-theory on Spin(7)-manifolds]]

* [[F-theory on Spin(7)-manifolds]]

* [[8-manifold]]



## References

### General

The concept goes back to:

* E. Bonan, (1966), _Sur les vari&#233;t&#233;s riemanniennes &#224; groupe d'holonomie G2 ou Spin(7)_, C. R. Acad. Sci. Paris 262: 127&#8211;129.  

Characterization in terms of the [[Euler class|Euler 8-class]] and the [[I8]]-[[invariant polynomial]] of the [[tangent bundle]]:

* [[H. Blaine Lawson]], [[Marie-Louise Michelsohn]], Thm. 10.7 in: _Spin geometry_, Princeton University Press (1989) &lbrack;[ISBN 9780691085425](https://press.princeton.edu/books/hardcover/9780691085425/spin-geometry-pms-38-volume-38)&rbrack;

       
Construction of [[compact topological space|compact]] [[Spin(7)-manifolds]]:

* Christine Taylor, _Compact Manifolds with Holonomy Spin(7)_ (1996) ([pdf](https://people.maths.ox.ac.uk/joyce/theses/TaylorMSc.pdf))

* [[Dominic Joyce]], _A new construction of compact 8-manifolds with holonomy $Spin(7)$_, J. Differential Geom. Volume 53, Number 1 (1999), 89-130 ([euclid:jdg/1214425448](https://projecteuclid.org/euclid.jdg/1214425448))

* [[Dominic Joyce]], _Compact Manifolds with Special Holonomy_, Oxford Mathematical Monographs, Oxford University Press (2000) ([ISBN:9780198506010](https://global.oup.com/academic/product/compact-manifolds-with-special-holonomy-9780198506010?cc=de&lang=en&))

In terms of [[G-structure]]:

* [[Robert Bryant]], _Metrics with Exceptional Holonomy_, Annals of Mathematics Second Series, Vol. 126, No. 3 (Nov., 1987), pp. 525-576 ([jstor:1971360](https://www.jstor.org/stable/1971360))


and motivated from special [[supersymmetry]] (such as in [[M-theory on Spin(7)-manifolds]]):

* {#IshamPope88} [[Chris Isham]], [[Christopher Pope]], _Nowhere Vanishing Spinors and Topological Obstructions to the Equivalence of the NSR and GS Superstrings_, Class. Quant. Grav. 5 (1988) 257 ([spire:251240](http://inspirehep.net/record/251240), [doi:10.1088/0264-9381/5/2/006](https://doi.org/10.1088/0264-9381/5/2/006))

* {#IshamPopeWarner88} [[Chris Isham]], [[Christopher Pope]], [[Nicholas Warner]], _Nowhere-vanishing spinors and triality rotations in 8-manifolds_,  Classical and Quantum Gravity, Volume 5, Number 10, 1988 ([cds:185144](http://cds.cern.ch/record/185144), [doi:10.1088/0264-9381/5/10/009](https://iopscience.iop.org/article/10.1088/0264-9381/5/10/009))

  (focus on [[Spin(7)-structure]])

On [[Spin(7)-orbifolds]]:

* Ya. V. Bazaikin, _On the new examples of complete noncompact Spin(7)-holonomy metrics_,  Sib Math J **48**, 8–25 (2007) ([doi:10.1007/s11202-007-0003-7](https://doi.org/10.1007/s11202-007-0003-7))

### Relation to Higgs bundles

Relating [[M-theory on Spin(7)-manifolds]] with [[F-theory on Spin(7)-manifolds]] via [[Higgs bundles]]:

* {#CHRTZ20} [[Mirjam Cvetic]], [[Jonathan Heckman]], Thomas B. Rochais, Ethan Torres, [[Gianluca Zoccarato]], _Geometric Unification of Higgs Bundle Vacua_ ([arXiv:2003.13682](https://arxiv.org/abs/2003.13682))


[[!redirects Spin(7) manifolds]]

[[!redirects Spin(7)-manifold]]

[[!redirects Spin(7)-manifolds]]

[[!redirects Spin7-manifold]]
[[!redirects Spin7-manifolds]]

[[!redirects Spin(7)-structure]]
[[!redirects Spin(7)-structures]]

[[!redirects Spin(7)-orbifold]]
[[!redirects Spin(7)-orbifolds]]


[[!redirects Spin(7) structure]]
[[!redirects Spin(7) structures]]

[[!redirects Spin7-structure]]
[[!redirects Spin7-structures]]

[[!redirects Spin7 structure]]
[[!redirects Spin7 structures]]

