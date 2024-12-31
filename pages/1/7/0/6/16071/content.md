
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

* [[torsion of a metric connection]]


## References

### General

Historical origin of the notion in [[Cartan geometry]]:

* {#Cartan22} [[Élie Cartan]], *Sur une généralisation de la notion de courbure de Riemann et les espaces á torsion*, C. R. Acad. Sci. **174** (1922) 593-595 .

* {#Cartan23} [[Élie Cartan]], *Sur les variétés à connexion affine et la théorie de la relativité généralisée (première partie)*, Annales scientifiques de l’École Normale Supérieure, Sér. 3, **40** (1923) 325-412 \[<a href="http://www.numdam.org/item?id=ASENS_1923_3_40__325_0">doi:ASENS_1923_3_40__325_0</a>\]

Historical review:

* [[Erhard Scholz]], *E. Cartan’s attempt at bridge-building between Einstein and the Cosserats – or how translational curvature became to be known as "torsion"*, The European Physics Journal H **44** (2019) 47-75 \[<a href="https://doi.org/10.1140/epjh/e2018-90059-x">doi:10.1140/epjh/e2018-90059-x</a>\]


Monographs:

* {#Sharpe97} [[Richard W. Sharpe]], *Differential geometry -- Cartan's generalization of Klein's Erlagen program*, Graduare Texts in Mathematics **166**, Springer (1997) &lbrack;[ISBN:9780387947327](https://link.springer.com/book/9780387947327)&rbrack;

* {#CapSlovak09} [[Andreas Čap]], [[Jan Slovák]], chapter 1 of: _Parabolic Geometries I -- Background and General Theory_, AMS (2009) &lbrack;[ISBN:978-1-4704-1381-1](http://bookstore.ams.org/surv-154)&rbrack;

Basic exposition:

* [[Adam Marsh]], §3.4 in: *Riemannian Geometry: Definitions, Pictures, and Results* &lbrack;[arXiv:1412.2393](https://arxiv.org/abs/1412.2393)&rbrack;


Discussion of torsion in [[gravity|gravitational]] [[classical field theory]]:

* [[Friedrich W. Hehl]], [[Yuri N. Obukhov]], *Élie Cartan’s torsion in geometry and in field theory, an essay*, Annales de la Fondation Louis de Broglie, **32** 2-3 (2007) 157-194 &lbrack;[pdf](https://fondationlouisdebroglie.org/AFLB-322/aflb322m595.pdf), [arXiv:0711.1535](https://arxiv.org/abs/0711.1535)&rbrack; 


Discussion with an eye towards [[torsion constraints in supergravity]]:

* {#Lott01} [[John Lott]], _The Geometry of Supergravity Torsion Constraints_ &lbrack;[arXiv:0108125](http://arxiv.org/abs/math/0108125)&rbrack;

  following:

  [[John Lott]], *Torsion constraints in supergeometry*, Comm. Math. Phys. **133** (1990) 563-615 &lbrack;[doi:10.1007/BF02097010](https://doi.org/10.1007/BF02097010)&rbrack;


[[!include Cartan structural equations and Bianchi identities -- references]]


[[!redirects torsion of Cartan connections]]
