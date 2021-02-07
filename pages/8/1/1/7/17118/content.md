
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

A [[Riemannian manifold]] $(X,g)$ of [[dimension]] $4n$ for $n \geq 2$ is called a _quaternion-Kähler manifold_ if its [[holonomy group]] is a [[subgroup]] of [[Sp(n).Sp(1)]] (where [[Sp(n)]] is the $n$th [[quaternionic unitary group]], and in particular $Sp(1) \simeq SU(2) \simeq $ [[Spin(3)]], and the [[central product]] is the [[quotient group]] of the [[direct product group]] by the [[diagonal]] [[center]] $\mathbb{Z}/2$). 

If the [[holonomy]] group is in fact a [[subgroup]] of just the $Sp(n)$-factor, one speaks of a _[[hyperkähler manifold]]_.


Quaternion-Kähler manifolds are necessarily [[Einstein manifolds]] (see [below](#AsEinsteinManifolds)). In particular their [[scalar curvature]] $R$ is [[constant function|constant]], and hence a [[real number]] $R \in \mathbb{R}$.  If the scalar curvature is [[positive number|positive]], then one speaks of a _positive quaternion-Kähler manifold_. 

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

### Reduction to hyper-Kähler structure

A quaternion-Kähler manifold $(X,g)$ is a [[hyper-Kähler manifold]], hence has $Sp(n) \hookrightarrow Sp(n)\cdot Sp(1)$-structure, precisely if its [[scalar curvature]], which is a [[constant function|constant]] by $(X,g)$ being an [[Einstein manifold]], vanishes: $R(g) = 0$.

(e.g. [Amann 09, below Def. 1.5](#Amann09))



### Positive quaternion-Kähler manifolds
 {#PositiveQuaternionKaehlerManifolds}


+-- {: .num_defn #PositiveQuaternionKaehlerManifold}
###### Definition

A quaternion-Kähler manifold $(X,g)$ is called _positive_ if 

1. it is a [[geodesically complete]]

1. its [[scalar curvature]], which is a [[constant function|constant]] by $(X,g)$ being an [[Einstein manifold]], is a [[positive number]], $R(g) \gt 0$.

=--

([Salamon 82, Section 6](#Salamon82), see e.g. [Amann 09, Def. 1.5](#Amann09))

+-- {: .num_prop}
###### Proposition

A [[connected topological space|connected]] [[positive quaternion-Kähler manifold]] (Def. \ref{PositiveQuaternionKaehlerManifold}) is necessarily [[compact topological space|compact]].

=--

([Salamon 82, p. 158 (16 of 29)](#Salamon82))

+-- {: .num_prop }
###### Proposition

A [[connected topological space|connected]] [[positive quaternion-Kähler manifold]] (Def. \ref{PositiveQuaternionKaehlerManifold}) is necessarily [[simply connected topological space|simply connected]].

=--

([Salamon 82, Theorem 6.6](#Salamon82))

+-- {: .num_prop}
###### Proposition

For each [[dimension]] $dim(X)$ there is a [[finite number]] of [[isometry]] [[isomorphism class|classes]] of [[positive quaternion-Kähler manifolds]] (Def. \ref{PositiveQuaternionKaehlerManifold}).

=--

([LeBrun-Salamon 94, Theorem 0.1](#LeBrunSalamon94))

+-- {: .num_prop #WoldSpacesArePositiveQuaternionKaehler}
###### Proposition
(**[[Wolf spaces]] are [[positive quaternion-Kähler manifolds]])**

Every [[Wolf space]] is a [[positive quaternion-Kähler manifold]].

=--

In fact the [[Wolf spaces]] are the only known examples  of [[positive quaternion-Kähler manifold]] (which is not hyper-Kähler ?!), as of today (e.g. [Salamon 82, Section 5](#Salamon82)).

This leads to the **conjecture** that in every dimension, the [[Wolf spaces]] are the only [[positive quaternion-Kähler manifolds]].

The conjecture has been proven for the following [[dimensions]]

* $d = 4$ (Hitchin)

* $d = 8 $ ([Poon-Salamon 91](#PoonSalamon91), [LeBrun-Salamon 94](#LeBrunSalamon94))


\linebreak


## Examples

The archetypical example is

* [[quaternionic projective plane]] $\,\mathbb{H}P^2$

This is the first of the list of examples  of spaces that are both [[quaternion-Kähler manifolds]]  as well as [[symmetric spaces]], called _[[Wolf spaces]]_.

See around Prop. \ref{WoldSpacesArePositiveQuaternionKaehler} above.

\linebreak

## Related concepts

* [[quaternionic manifold]], [[Kähler manifold]], [[hyper-Kähler manifold]]

## References

Original articles:

* {#Salamon82} [[Simon Salamon]], _Quaternionic Kähler manifolds_, Invent Math (1982) 67: 143. ([doi:10.1007/BF01393378](https://doi.org/10.1007/BF01393378))

* {#PoonSalamon91} Y. S. Poon, [[Simon Salamon]], _Quaternionic Kähler 8-manifolds with positive scalar curvature_, J. Differential Geom. Volume 33, Number 2 (1991), 363-378 ([euclid:1214446322](https://projecteuclid.org/euclid.jdg/1214446322))

* {#LeBrunSalamon94} Claude LeBrun, [[Simon Salamon]], _Strong rigidity of positive quaternion Kähler manifolds_, Inventiones Mathematicae 118, 1994, 109–132 ([dml:144231](https://eudml.org/doc/144231), [doi:10.1007/BF01231528](https://doi.org/10.1007/BF01231528))

Exposition:

* {#Cortes05} [[Vicente Cortés]], _Quaternionic Kähler manifolds_, 2005 ([pdf](https://www2.math.hu-berlin.de/gradkoll/Cortes_vorlesung1_handout.pdf))

Textbook accounts:

* {#Besse}[[Arthur Besse]], _Einstein Manifolds_, Springer-Verlag 1987.

* {#Joyce} [[Dominic Joyce]], _Compact Manifolds with Special Holonomy_, Oxford University Press, 2000.

See also

* Wikipedia, _[Quaternion-K&#228;hler manifold](https://en.wikipedia.org/wiki/Quaternion-Kaehler_manifold)_

In terms of [[G-structure]]:

* Edmond Bonan, _Sur les $G$-structures de type quaternionien_,  Cahiers de Topologie et Géométrie Différentielle Catégoriques, Volume 9 (1967) no. 4, p. 389-463 ([numdam:CTGDC_1967__9_4_389_0](http://www.numdam.org/item/CTGDC_1967__9_4_389_0))

* {#Salamon86} [[Simon Salamon]], _Differential Geometry of Quaternionic Manifolds_, Annales scientifiques de l’É.N.S. 4e série, tome 19, no 1 (1986), p. 31-55 ([numdam:ASENS_1986_4_19_1_31_0](http://www.numdam.org/item/ASENS_1986_4_19_1_31_0/))

* [[Dmitri V. Alekseevsky]], [[Stefano Marchiafava]], _Quaternionic-like structures on a manifold: Note I. 1-integrability and integrability conditions_, Atti della Accademia Nazionale dei Lincei. Classe di Scienze Fisiche, Matematiche e Naturali. Rendiconti Lincei. Matematica e Applicazioni (1993) Volume: 4, Issue: 1, page 43-52 ([dml:244082](https://eudml.org/doc/244082))

* [[Dmitri V. Alekseevsky]], [[Stefano Marchiafava]], _Quaternionic-like structures on a manifold: Note II. Automorphism groups and their interrelations_, Atti della Accademia Nazionale dei Lincei. Classe di Scienze Fisiche, Matematiche e Naturali. Rendiconti Lincei. Matematica e Applicazioni (1993) Volume: 4, Issue: 1, page 53-61 ([dml:244299](https://eudml.org/doc/244299))

* [[Dmitry V. Alekseevsky]], [[Stefano Marchiafava]], _Quaternionic structures on a manifold and subordinated structures_, Annali di Matematica pura ed applicata 171, 205–273 (1996) ([doi:10.1007/BF01759388](https://doi.org/10.1007/BF01759388))


* Joseph Thurman, _Quaternionic Geometry and Special Holonomy_, 2018 ([pdf](http://www.math.stonybrook.edu/alumni/2018-Joseph-Thurman.pdf))

Articles discussing quaternion-Kähler [[holonomy]], [[connection]], and relation to other [[hypercomplex manifold|hypercomplex structures]]:

* {#Moroianu} [[Andrei Moroianu]], [[Uwe Semmelmann]], _Killing Forms on Quaternion-Kähler Manifolds_, Annals of Global Analysis and Geometry, November 2005, Volume 28, Issue 4, pp 319–335 ([arXiv:math/0403242](https://arxiv.org/abs/math/0403242), [doi:10.1007/s10455-005-1147-y](https://doi.org/10.1007/s10455-005-1147-y))

* {#PerdersonSwannPoon} Pedersen, Poon, and Swann. "Hypercomplex structures associated to quaternionic manifolds",  Differential Geometry and its Applications (1998) 273-293 North-Holland.

* {#Verbitsky} [[Misha Verbitsky]], _Hyperkähler manifolds with torsion, supersymmetry and Hodge theory_, Asian J. Math, V. 6 No. 4, pp. 679-712, Dec. 2002.



See also

* Claude LeBrun, _On complete quaternionic-Kähler manifolds_, Duke Math. J. Volume 63, Number 3 (1991), 723-743 ([euclid:1077296077](https://projecteuclid.org/euclid.dmj/1077296077))

* Simon G. Chiossi, Óscar Maciá, _SO(3)-Structures on 8-manifolds_, Ann. Glob. Anal. Geom. 43 (1) (2013), 1--18 ([arXiv:1105.1746](https://arxiv.org/abs/1105.1746))

On [[positive quaternion-Kähler manifolds]]

* {#Amann09} Amann, _Positive Quaternion Kähler Manifolds_, 2009 ([pdf](https://d-nb.info/996176438/34))

* Amann, _Partial Classification Results for Positive Quaternion Kaehler Manifolds_ ([arXiv:0911.4587](https://arxiv.org/abs/0911.4587))

Discussion of [[characteristic classes]]:

* {#CadekVanzura98} [[Martin Čadek]], [[Jiří Vanžura]], _Almost quaternionic structures on eight-manifolds_, Osaka J. Math. Volume 35, Number 1 (1998), 165-190 ([euclid:1200787905](https://projecteuclid.org/euclid.ojm/1200787905))

On [[quaternion-Kähler orbifolds]]:

*  K. Galicki, [[H. Blaine Lawson]], _Quaternionic Reduction and Quaternionic Orbifolds_, Mathematische Annalen (1988) Volume: 282, Issue: 1, page 1-22 ([dml:164446](https://eudml.org/doc/164446))


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

[[!redirects quaternion-Kähler structure]]
[[!redirects quaternion-Kähler structures]]

[[!redirects quaternion-Kaehler structure]]
[[!redirects quaternion-Kaehler structures]]

[[!redirects quaternion Kähler structure]]
[[!redirects quaternion Kähler structures]]

[[!redirects quaternion Kaehler structure]]
[[!redirects quaternion Kaehler structures]]

[[!redirects quaternion-Kähler orbifold]]
[[!redirects quaternion-Kähler orbifolds]]

[[!redirects Sp(2).Sp(1)-structure]]
[[!redirects Sp(2).Sp(1)-structures]]

[[!redirects Sp(2).Sp(1) structure]]
[[!redirects Sp(2).Sp(1) structures]]



[[!redirects positive quaternion-Kähler manifolds]]

[[!redirects positive quaternion Kähler manifold]]
[[!redirects positive quaternion Kähler manifols]]

[[!redirects positive quaternion-Kähler manifold]]
[[!redirects positive quaternion-Kähler manifols]]

[[!redirects positive quaternion-Kaehler manifold]]
[[!redirects positive quaternion-Kaehler manifolds]]

[[!redirects positive quaternion Kaehler manifold]]
[[!redirects positive quaternion Kaehler manifolds]]
             
[[!redirects positive quaternionic Kähler manifold]]
[[!redirects positive quaternionic Kähler manifolds]]

[[!redirects positive quaternionic-Kähler manifold]]
[[!redirects positive quaternionic-Kahler manifold]]
[[!redirects positive quaternionic-Kähler manifolds]]
[[!redirects positive quaternionic-Kahler manifolds]]

[[!redirects positive quaternion-Kähler structure]]
[[!redirects positive quaternion-Kähler structures]]

[[!redirects quaternion-Kaehler structure]]
[[!redirects quaternion-Kaehler structures]]

[[!redirects quaternion Kähler structure]]
[[!redirects quaternion Kähler structures]]

[[!redirects quaternion Kaehler structure]]
[[!redirects quaternion Kaehler structures]]




