
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}

## Idea ##

The _shifted tangent bundle_ or _odd tangent bundle_ $\Pi T X$ of a [[manifold]] $X$ is an incarnation of the ordinary [[tangent bundle]] of $X$ as a [[supermanifold]] with the underlying manifold in even degree and the tangent vectors in odd degree.

## Definition ##

For $X$ a smooth [[manifold]] the [[supermanifold]] $\Pi T X$ is defined to be the one specified by the fact that its [[superalgebra]] of functions is the graded-commutative [[exterior algebra]] of [[differential forms]]

$$
  C^\infty(\Pi T X) := \Omega^\bullet(X)
  = \wedge^\bullet_{C^\infty(X)} \Gamma(T^* X)
  \,.
$$

More precisely, for each open $U \subset X$ the value of the [[structure sheaf]] of $\Pi T X$ is $\Omega^\bullet(U)$.

For more details see at _[[geometry of physics -- supergeometry]]_.

## Alternative characterizations ##

### As an NQ-supermanifold ###

In the context of [[supergeometry]] the algebra $\Omega^\bullet(X)$ is regarded as a $\mathbb{Z}_2$-graded algebra, but of course this $\mathbb{Z}_2$-grading lifts to an $\mathbb{N}$-grading in the obvious way.

Moreover, there is a canonical odd vector field $v_d$ on $\Pi T X$, which as an odd derivation on the function algebra $\Omega^\bullet(X)$ is just the [[deRham complex|deRham differential]].

Equipped with this structure $\Pi T X$ is naturally an [[NQ-supermanifold]]. 

### As the tangent Lie algebroid ###

The [[dg-algebra]] $(\Omega^\bullet(X), d_{dR})$ may also be regarded as the [[Chevalley-Eilenberg algebra]] of the [[tangent Lie algebroid]] of $X$, which identifies the shifted tangent bundle in its refinement to an [[NQ-supermanifold]] with the [[tangent Lie algebroid]] of $X$.

From this perspective, the fact that the vectors are regarded as being in degree one in $\Pi T X$ corresponds to the fact that these are the tangents to the [[k-morphism|1-morphism]]s of the [[fundamental groupoid]] of $X$. (Which is denoted $\Pi(X)$ but with the "$\Pi$" of completely different meaning than the "$\Pi$" as used here, which just indicates degree shift).


### As an internal hom object ###

With $\mathbb{R}^{0|1}$ denoting the [[odd line]], i.e. the [[supermanifold]] with function algebra the algebra of [[dual number]]s, one finds that 

$$
  \Pi T X = [\mathbb{R}^{0|1}, X]
$$

is the [[internal hom]] object in the category of [[supermanifold]]s of maps from $\mathbb{R}^{0|1}$ to $X$. More precisely this means that the [[internal hom]] which exists in the [[closed monoidal structure on presheaves]] on the category of supermanifolds, between the presheaves [[representable functor|represented by]] $\mathbb{R}^{0|1}$ and $X$, is itself [[representable functor|representable]] and is represented by $\Pi T X$.

The existence of the structure of an [[NQ-supermanifold]] is from this point of view a consequence of the fact that $[\mathbb{R}^{0|1},X]$ naturally carries an action of the [[endomorphism]] object $End(\mathbb{R}^{0|1})$.  For more on this see [[NQ-supermanifold]].

## References

* {#KochanSevera03} Denis Kochan, [[Pavol Ševera]], §3.1 in: _Differential gorms, differential worms_, Mathematical Physics, World Scientific (2005) 128-130  &lbrack;[arXiv:math/0307303](http://arxiv.org/abs/math/0307303), [doi:10.1142/9789812701862_0034](https://doi.org/10.1142/9789812701862_0034)&rbrack;

* [[Henning Hohnhold]], [[Matthias Kreck]], [[Stephan Stolz]], [[Peter Teichner]]: Ex. 2.1 & Prop. 3.1 in: _Differential forms and 0-dimensional supersymmetric field theories_, Quantum Topology **2** 1 (2011) 1–41 &lbrack;[doi:10.4171/QT/12](http://dx.doi.org/10.4171/QT/12), [pdf](https://www.math.sciences.univ-nantes.fr/%7Ehossein/GdT-Elliptique/Hohnholdt-Kreck-Stolz-Teichner.pdf)&rbrack;

* {#CarchediRoytenberg12} [[David Carchedi]], [[Dmitry Roytenberg]]: Ex. 5.3 in: _Homological Algebra for Superalgebras of Differentiable Functions_ &lbrack;[arXiv:1212.3745](http://arxiv.org/abs/1212.3745)&rbrack;
 
* [[Urs Schreiber]]: *[Super mapping spaces](geometry+of+physics+--+supergeometry#SuperMappingSpaces)* , section of: *[[geometry of physics -- supergeometry]]* (2016) 

* [[Simone Noja]]: §3 in: *On the Geometry of Forms on Supermanifolds* &lbrack;[arXiv:2111.12841](https://arxiv.org/abs/2111.12841)&rbrack;



[[!redirects shifted tangent bundles]]


[[!redirects odd tangent bundle]]
[[!redirects odd tangent bundles]]