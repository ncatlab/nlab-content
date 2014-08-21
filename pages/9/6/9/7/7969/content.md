
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

### General

Generally, a _theta function_ ($\theta$-function, $\Theta$-function) is a [[holomorphic section]] of a ([[polarized variety|principally polarizing]]) [[holomorphic line bundle]] over a [[complex torus]] / [[abelian variety]].
(e.g. [Polishchuk 03, section 17](#Polishchuk03)) and in particular over a [[Jacobian variety]] ([Beauville](#Beauville)) such as [[prequantum line bundles]] for (abelian) [[gauge theory]]. The line bundle being principally polarizing means that its space of holomorphic sections is 1-dimensional, hence that it determines the $\theta$-function up to a global complex scale factor. Typically these line bundles themselves are [[Theta characteristics]].
Expressed in local [[coordinates]] on $\mathbb{C}^g$ a $\theta$-function appears as an actual function, satisfying certain transformation properties. 

Specifically in the context of [[number theory]]/[[arithmetic geometry]], by _the_ theta function one usually means the _[[Jacobi theta function]]_ (see there for more), which is the historically first and archetypical function from which all modern generalizations derive their name.

Certain integrals of theta functions yield [[zeta functions]], see also at _[[function field analogy]]_.

### In quantization

Theta functions are naturally thought of as being the [[space of states (in geometric quantization)|states]] in the [[geometric quantization]] of the given complex space, the given holomorphic line bundle being the [[prequantum line bundle]] and the condition of holomorphicity of the section being the [[polarization]] condition. See for instance ([Tyurin 02](#Tyurin02)). In this context they play a proming role specifically in the quantization of [[higher dimensional Chern-Simons theory]] and of [[self-dual higher gauge theory]]. See there for more.

## Definition
 {#Definition}

Consider a [[complex torus]] $T \simeq V/\Gamma$ for given [[finite group]] $\Gamma$. 

Say that a _system of multipliers_ is a system of invertible [[holomorphic functions]] 

$$
  e_\gamma \colon V \longrightarrow \mathbb{C}^\times \hookrightarrow \mathbb{C}
$$

satisfying the cocycle condition

$$
  e_{\gamma + \delta}(z) = e_\gamma(z + \delta) e_\delta(z)
  \,.
$$

Then a _theta function_ is a [[holomorphic function]]

$$
  \theta \colon V \longrightarrow \mathbb{C}
$$

for which there is a system of multipliers $\{e_\gamma\}$ satisfying the [[functional equation]] which says that for each $z \in V$ and $\gamma \in \Gamma \hookrightarrow V$ we have

$$
  \theta(z + \gamma) = e_\gamma(z) \theta(z)
  \,.
$$

e.g. ([Beauville, above prop. 2.2](#Beauville))

## Examples

* [[Jacobi theta function]]

* [[Riemann theta function]]

* [[Ramanujan theta function]]

* [[Dedekind eta function]]

## Related concepts

* [[special functions]]

* [[cubical structure on a line bundle]]

* [[mock theta function]]

[[!include square roots of line bundles - table]]


## References

Introductions to the traditional notion include

* D.H. Bailey et al, _The Miracle of Theta Functions_ ([web](http://www.cecm.sfu.ca/organics/papers/borwein/paper/html/node12.html))

* M. Bertola, _Riemann surfaces and theta  functions_ ([pdf](http://www.mathstat.concordia.ca/faculty/bertola/ThetaCourse/ThetaCourse.pdf))

A modern textbook account is

* {#Polishchuk03} [[Alexander Polishchuk]], section 17 of _Abelian varieties, Theta functions and the Fourier transform_, Cambridge University Press (2003) ([review pdf](http://math1.unice.fr/~beauvill/pubs/poli.pdf))

Further discussion with an emphasis of the origin of theta functions in [[geometric quantization]] is in 

* {#Beauville} [[Arnaud Beuville]], _Theta functions, old and new_, Open Problems and Surveys of Contemporary Mathematics SMM6, pp. 99&#8211;131 ([pdf](http://math.unice.fr/~beauvill/pubs/thetaon.pdf))

* {#Tyurin02} [[Andrei Tyurin]], _Quantization, Classical and quantum field theory and theta functions_ ([arXiv:math/0210466v1](http://arxiv.org/abs/math/0210466))

* Yuichi Nohara, _Independence of polarization in geometric quantization_ ([pdf](http://geoquant.mi.ras.ru/nohara.pdf))
 {#Nohara}

* Gerard Lion, Michele Vergne, _The Weil representation, Maslov index and theta series_

Relation to [[conformal blocks]]:

* [[Arnaud Beauville]], [[Yves Laszlo]], _Conformal blocks and generalized theta functions_ ([arXiv:alg-geom/9309003](http://arxiv.org/abs/alg-geom/9309003))
 {#BeauvilleLaszlo93}

Relation to [[elliptic genera]] (see also at _[[Jacobi form]]_)

* {#KL95} [[Kefeng Liu]], section 2.4 of _On modular invariance and rigidity theorems_, J. Differential Geom. Volume 41, Number 2 (1995), 247-514 ([EUCLID](http://projecteuclid.org/euclid.jdg/1214456221), [pdf](http://www.math.ucla.edu/~liu/Research/loja.pdf))


[[!redirects theta functions]]
[[!redirects theta-function]]
[[!redirects theta-functions]]

[[!redirects Theta function]]
[[!redirects Theta functions]]
[[!redirects Theta-function]]
[[!redirects Theta-functions]]

[[!redirects Riemann theta function]]
[[!redirects Riemann theta functions]]
[[!redirects Jacobi theta function]]
[[!redirects Jacobi theta functions]]
[[!redirects Ramanujan theta function]]
[[!redirects Ramanujan theta functions]]