
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

## Definition

A [[Riemannian manifold]] of [[dimension]] $4n$ for $n \geq 2$ is called a _quaternion-Kähler manifold_ if its [[holonomy group]] is a [[subgroup]] of [[Sp(n).Sp(1)]] (where [[Sp(n)]] is the $n$th [[quaternionic unitary group]], and in particular $Sp(1) \simeq SU(2) \simeq $ [[Spin(3)]], and the product is the [[quotient group]] of the [[direct product group]] by the [[diagonal]] [[center]] $\mathbb{Z}/2$). 

If the [[holonomy]] group is in fact a [[subgroup]] of just the $Sp(n)$-factor, one speaks of a _[[hyperkähler manifold]]_.

\linebreak

## Properties

### As part of the Berger classification

[[!include special holonomy table]]

### As $\mathbb{H}$-Riemannian manifolds

[[!include normed division algebra Riemannian geometry -- table]]

### As quaternionic manifolds


+-- {: .num_example #QuaternionKaehlermanifoldsAreQuaternionicManifolds}
###### Example
**([[quaternion-Kähler manifolds]] are [[quaternionic manifolds]])**

By definition, a [[quaternion-Kähler manifold]] $M$ has [[holonomy group]] contained in the [[direct product group]] [[Sp(n)]]$\times$[[Spin(3)|Sp(1)]], admitting an extension of the [[Levi-Civita connection]] $\nabla$ on the holonomy bundle as [[torsion of a G-structure|torsion]]-free. Thus a quaternion-Kähler manifold is automatically a [[quaternionic manifold]]. 

Such extension $\nabla_\text{quat}$ of $\nabla$ however is not unique, since $\nabla_\text{quat} + \mathcal{S}$ is another Sp(n)Sp(1)-preserving connection, where $\mathcal{S}$ is a (1, 2)-tensor such that for every $p \in M$, $\mathcal{S}(p)$ takes values in the first [[prolongation]] of the [[Lie algebra]] for the [[G-structure]]. 

=--


### As Einstein manifolds
 {#AsEinsteinManifolds}

[[quaternion-Kähler manifolds]] are [[Einstein manifolds]] (e.g. [Cortés 05, slide 22](#Cortes05))

### Characteristic classes

+-- {: .num_prop #CharacteristicClassesForSpin5Spin3Structure}
###### Proposition

Let $X$ be a  [[closed manifold|closed]] [[smooth manifold]] of [[dimension]] 8 with [[Spin structure]]. If the [[frame bundle]] moreover admits [[G-structure]] for 

$\;\;G = $ [[Sp(n).Sp(1)|Sp(2).Sp(1)]] $\hookrightarrow$ [[SO(8)]] 

then the [[Euler class]] $\chi$, the [[second Pontryagin class]] $p_2$ and the [[cup product]]-square $(p_1)^2$ of the [[first Pontryagin class]] of the [[frame bundle]]/[[tangent bundle]] are related by

\[
  \label{EulerClassInTermsOfPontryagin}
  8 \chi
  \;=\;
  4 p_2 - (p_1)^2
  \,.
\]

=--

([Čadek-Vanžura 98, Theorem 8.1 with Remark 8.2](#CadekVanzura98))

+-- {: .num_remark}
###### Remark

The same conclusion (eq:EulerClassInTermsOfPontryagin) also holds for $Spin(7)$-structure, see [there](Spin7-manifold#CharacteristicClassesForSpinStructure)

=--

See also at _[[C-field tadpole cancellation]]_.

## Related concepts

* [[quaternionic manifold]], [[Kähler manifold]], [[hyper-Kähler manifold]]

## References

Original articles:

* {#Salamon82} [[Simon Salamon]], _Quaternionic Kähler manifolds_, Invent Math (1982) 67: 143. ([doi:10.1007/BF01393378](https://doi.org/10.1007/BF01393378))

Exposition

* {#Cortes05} [[Vicente Cortés]], _Quaternionic Kähler manifolds_, 2005 ([pdf](https://www2.math.hu-berlin.de/gradkoll/Cortes_vorlesung1_handout.pdf))

Textbook references include:

* {#Besse}[[Arthur Besse]], _Einstein Manifolds_, Springer-Verlag 1987.

* {#Joyce} [[Dominic Joyce]], _Compact Manifolds with Special Holonomy_, Oxford University Press, 2000.

See also

* Wikipedia, _[Quaternion-K&#228;hler manifold](https://en.wikipedia.org/wiki/Quaternion-K&#228;hler_manifold)_


Articles discussing quaternion-Kähler [[holonomy]], [[connection]], and relation to other [[hypercomplex]] structures:

* {#Moroianu} Andrei Moroianu, [[Uwe Semmelmann]], "Killing Forms on Quaternion-Kähler Manifolds", Annals of Global Analysis and Geometry, November 2005, Volume 28, Issue 4, pp 319–335.

* {#PerdersonSwannPoon} Pedersen, Poon, and Swann. "Hypercomplex structures associated to quaternionic manifolds",  Differential Geometry and its Applications (1998) 273-293 North-Holland.

* {#Verbitsky} [[Misha Verbitsky]], "Hyperkähler manifolds with torsion, supersymmetry and Hodge theory", Asian J. Math, V. 6 No. 4, pp. 679-712, Dec. 2002.

* {#Salamon86} [[Simon Salamon]], _Differential Geometry of Quaternionic Manifolds-, Annales scientifiques de l’É.N.S. 4e série, tome 19, no 1 (1986), p. 31-55.

See also

* Claude LeBrun, _On complete quaternionic-Kähler manifolds_, Duke Math. J. Volume 63, Number 3 (1991), 723-743 ([euclid:1077296077](https://projecteuclid.org/euclid.dmj/1077296077))

* Simon G. Chiossi, Óscar Maciá, _SO(3)-Structures on 8-manifolds_, Ann. Glob. Anal. Geom. 43 (1) (2013), 1--18 ([arXiv:1105.1746](https://arxiv.org/abs/1105.1746))

On quaternion-Kähler manifold with [[positive number|positive]] [[scalar curvature]]:

* Amann, _Positive Quaternion Kähler Manifolds_ ([pdf](https://d-nb.info/996176438/34))

* Amann, _Partial Classification Results for Positive Quaternion Kaehler Manifolds_ ([arXiv:0911.4587](https://arxiv.org/abs/0911.4587))

Discussion of [[characteristic classes]]:

* {#CadekVanzura98} [[Martin Čadek]], [[Jiří Vanžura]], _Almost quaternionic structures on eight-manifolds_, Osaka J. Math. Volume 35, Number 1 (1998), 165-190 ([euclid:1200787905](https://projecteuclid.org/euclid.ojm/1200787905))


[[!redirects quaternion-Kähler manifolds]]

[[!redirects quaternion Kähler manifold]]
[[!redirects quaternion Kähler manifols]]


[[!redirects quaternion-Kaehler manifold]]
[[!redirects quaternion-Kaehler manifolds]]


[[!redirects quaternion Kaehler manifold]]
[[!redirects quaternion Kaehler manifolds]]
             
[[!redirects quaternionic Kähler manifold]]
[[!redirects quaternionic Kähler manifolds]]

[[!redirects quaternionic-Kähler manifold]]
[[!redirects quaternionic-Kahler manifold]]
[[!redirects quaternionic-Kähler manifolds]]
[[!redirects quaternionic-Kahler manifolds]]

[[!redirects quternionic-Kähler manifold]]
[[!redirects quternionic-Kähler manifolds]]

[[!redirects quaternion-Kähler structure]]
[[!redirects quaternion-Kähler structures]]

[[!redirects quaternion-Kaehler structure]]
[[!redirects quaternion-Kaehler structures]]

[[!redirects quaternion Kähler structure]]
[[!redirects quaternion Kähler structures]]

[[!redirects quaternion Kaehler structure]]
[[!redirects quaternion Kaehler structures]]

[[!redirects Spin(3) x Spin(5)-structure]]
[[!redirects Spin(3) x Spin(5)-structures]]

[[!redirects Spin(3) x Spin(5) structure]]
[[!redirects Spin(3) x Spin(5) structures]]


