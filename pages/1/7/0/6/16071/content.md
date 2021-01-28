
> for disambiguation see at [[torsion]]

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definiton

Given an $(H \stackrel{i}{\to} G)$-_[[Cartan connection]]_ $\nabla$ on a manifold $X$, its _torsion_ is the component of its [[curvature]] in the [[coimage]] of $i_\ast : \mathfrak{h}\to \mathfrak{g}$.

So if $U \to X$ is a [[cover]] over which the underlying $G$-[[principal bundle]] trivializes (for instance the total space of the $G$-[[principal bundle]] itself if one models the Cartan connection by an [[Ehresmann connection]]) and 

$$
  \omega \in \Omega^1(U,\mathfrak{g})
$$

is the Lie algebra valued [[curvature]] form, then the torsion form is

$$
  \tau \coloneqq coim(i)_\ast \omega \in \Omega^1(U,\mathfrak{g}/\mathfrak{h})
  \,.
$$

e.g. ([Sharpe 97, section 5.3, below def 3.1](#Sharpe97), [Cap-Slov&#225;k 09, section 1.5.7, p. 85](#CapSlovak09))

## Properties

### Integrability of local charts

If the torsion of a Cartan connection vanishes, then it has [[flat connection|flat]] $\mathfrak{g}/\mathfrak{h}$-valued [[parallel transport]]. In partciular then every point in the base manifold has a neighbourhood $U_x$ over which the given $G$-[[principal bundle]] trivializes and then this parallel trasport gives an identification $U_x \simeq U_{\sigma(x)}(G/H)$ with an open subset in the [[Klein geometry]] $G/H$.

### Relation to integrability of $G$-structure

If the [[Cartan connection]] is regarded as providing, in particular, a [[G-structure]], then the condition that its torsion vanishes is the [[integrability of G-structures]].

## Examples

### (Pseudo-)Riemannian geometry

For $(H \to G)$ being the inclusion $O(d)\hookrightarrow Iso(\mathbb{R}^d)$ of the [[orthogonal group]] into the [[Euclidean group]] or the inclusion $O(d-1,1)\hookrightarrow Iso(\mathbb{R}^{d-1,1})$ of the [[Lorentz group]] into the [[Poincare group]], then an $(H\to G)$-[[Cartan connection]] encodes a ([[pseudo-Riemannian geometry|pseudo]]-)[[Riemannian geometry]] with metric connection. Its torsion then is the [[torsion of a metric connection]]. See also at _[[first-order formulation of gravity]]_.

## Related concepts

* [[torsion of a G-structure]]

## References

Textbook accounts include

* {#Sharpe97} R. Sharpe, _Differential Geometry -- Cartan's Generalization of Klein's Erlagen program_ Springer (1997)

* {#CapSlovak09} [[Andreas Cap]], [[Jan Slovák]], chapter 1 of _Parabolic Geometries I -- Background and General Theory_, AMS 2009

Discussion with an eye towards [[torsion constraints in supergravity]] is in

* {#Lott01} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_ Comm. Math. Phys. 133 (1990), 563&#8211;615, (exposition in [arXiv:0108125](http://arxiv.org/abs/math/0108125))

[[!redirects torsion of Cartan connections]]