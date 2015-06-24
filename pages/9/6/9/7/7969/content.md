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
Expressed in [[coordinates]] $\mathbf{z}$ on the [[covering]] $\mathbb{C}^g$ of the [[complex torus]] $\mathbb{C}^g/\mathbb{Z}^g$, a $\theta$-function appears as an actual function $\mathbf{z} \mapsto \theta(\mathbf{z})$ satisfying certain transformation properties, and this is how theta functions are considered.

Those theta functions encoding sections of line bundles on a [[Jacobian variety]] $J(\Sigma)$ of a [[Riemann surface]] $\Sigma$ ([[determinant line bundles]], [Freed 87, pages 30-31](#Freed87)) typically vary in a controlled way with the [[complex structure]] modulus $\mathbf{\tau}$ of $\Sigma$ and are hence really functions also of this variable $(\mathbf{z},\mathbf{\tau}) \mapsto \theta(\mathbf{z}, \mathbf{\tau})$ with certain transformation properties. These are the _[[Riemann theta functions]]_. They are the expressions in local coordinates of the covariantly constant sections of the [[Hitchin connection]] on the [[moduli space of Riemann surfaces]] $\mathcal{M}_\Sigma$ ([Hitchin 90, remark 4.12](#Hitchin90)).  In the special case that $\Sigma$ is complex 1-dimensional of [[genus]] $g = 1$ (hence a complex [[elliptic curve]]) then such a function $(z,\tau) \mapsto \theta(z,\tau)$ of two variables with the pertinent transformation properties is a _[[Jacobi theta function]]_. Notice that in their dependency not only on $\tau$ but also on $z$ these are properly called _[[Jacobi forms]]_. Finally notice that these line bundles on [[Jacobian varieties]] have non-abelian generalizations to line bundles on [[moduli stacks of vector bundles]] of [[rank]] higher than one, whose sections may then be thought of as _generalized theta functions_ ([Beauville-Laszlo 93](#BeauvilleLaszlo93)).

Specifically in the context of [[number theory]]/[[arithmetic geometry]], by _the_ theta function one usually means the _[[Jacobi theta function]]_ (see there for more) for $z = 0$. While this is the historically first and archetypical function from which all modern generalizations derive their name, notice that at fixed $z$ as a function in $\tau$ the "theta function" is not actually a section of a line bundle anymore. The generalization in number theory of the Jacobi theta function that does again have a dependence on a twisting is the _[[Dirichlet theta function]]_ depending on a [[Dirichlet character]] (which by [[Artin reciprocity]] corresponds to a [[Galois representation]]).

Certain integrals of theta functions yield [[zeta functions]], see also at _[[function field analogy]]_.

[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

### In quantization

Theta functions are naturally thought of as being the [[space of states (in geometric quantization)|states]] in the [[geometric quantization]] of the given complex space, the given holomorphic line bundle being the [[prequantum line bundle]] and the condition of holomorphicity of the section being the [[polarization]] condition. See for instance ([Tyurin 02](#Tyurin02)). In this context they play a proming role specifically in the quantization of [[higher dimensional Chern-Simons theory]] and of [[self-dual higher gauge theory]]. See there for more.

Specifically the fact that in [[geometric quantization|geometric]] [[quantization of Chern-Simons theory]] in the abelian case, and the [[holographic principle|holographically]] dual [[partition functions]] of the [[WZW model]] the choice of polarization is induced from the choice of [[complex structure]] $\mathbf{\tau}$ on a given [[Riemann surface]] $\Sigma$ and for each such choice there is then a section/[[partition function]] depending on a coordinte $\mathbf{z}$ in the  [[Jacobian]] $J(\Sigma)$ is reflected in the double coordinate dependence of the theta function:

$$
  \theta(\mathbf{z},\mathbf{\tau})
  = 
  \theta\left(gauge\;field\;configuration\;on\;\Sigma\;, \; complex\;structure\;on\;\Sigma\right)
  \,.
$$

See e.g. ([AlvaresGaum&#233;-Moore-Vafa 86](#AlvaresGaumeMooreVafa86), [Freed 87, section 4](#Freed87), [Bunke-Olbrich 94, around def. 4.5](#BunkeOlbrich94)).

Since from the point of view of [[Chern-Simons theory]] this is a [[wavefunction]], one might rather want to write $\Psi(\mathbf{z},\mathbf{\tau})$.

For nonabelian CS/WZW theory the same story goes through and one may the elements of the corresponding [[conformal blocks]] "generalized theta functions" ([Beauville-Laszlo 93](#BeauvilleLaszlo93)).

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

e.g. ([Beauville, above prop. 2.2](#Beauville)), also ([Beauville, section 3.4](#Beauville))

## Examples

* [[Jacobi theta function]]

* [[Riemann theta function]]

* [[Ramanujan theta function]]

* [[Dedekind eta function]]

## Related concepts

* [[special functions]]

* [[cubical structure on a line bundle]]

* [[mock theta function]]

* [[elliptic function]]

[[!include square roots of line bundles - table]]


## References

Introductions to the traditional notion include

* D.H. Bailey et al, _The Miracle of Theta Functions_ ([web](http://www.cecm.sfu.ca/organics/papers/borwein/paper/html/node12.html))

* M. Bertola, _Riemann surfaces and theta  functions_ ([pdf](http://www.mathstat.concordia.ca/faculty/bertola/ThetaCourse/ThetaCourse.pdf))

Modern textbook accounts include

* {#Mumford83} [[David Mumford]], _Tata Lectures on Theta_, Birkh&#228;user 1983

* {#Polishchuk03} [[Alexander Polishchuk]], section 17 of _Abelian varieties, Theta functions and the Fourier transform_, Cambridge University Press (2003) ([review pdf](http://math1.unice.fr/~beauvill/pubs/poli.pdf))


Further discussion with an emphasis of the origin of theta functions in [[geometric quantization]] is in 

* {#Beauville} [[Arnaud Beauville]], _Theta functions, old and new_, Open Problems and Surveys of Contemporary Mathematics SMM6, pp. 99&#8211;131 ([pdf](http://math.unice.fr/~beauvill/pubs/thetaon.pdf))

* {#Tyurin02} [[Andrei Tyurin]], _Quantization, Classical and quantum field theory and theta functions_, AMS 2003 ([arXiv:math/0210466v1](http://arxiv.org/abs/math/0210466))

* {#Nohara} Yuichi Nohara, _Independence of polarization in geometric quantization_ ([pdf](http://geoquant.mi.ras.ru/nohara.pdf))
 

* Gerard Lion, Michele Vergne, _The Weil representation, Maslov index and theta series_

* Razvan Gelca, [[Alejandro Uribe]], _From classical theta functions to topological quantum field theory_  ([pdf](http://www.math.ttu.edu/~rgelca/berk.pdf))

Specifically the theta functions appearing in [[2d CFT]] as [[conformal blocks]] and as [[prequantum line bundles]] in [[quantization of Chern-Simons theory]] are discussed for instance in

* {#AlvaresGaumeMooreVafa86} [[Luis Alvarez-Gaumé]], [[Gregory Moore]], [[Cumrun Vafa]], _Theta functions, modular invariance, and strings_, Communications in Mathematical Physics Volume 106, Number 1 (1986), 1-4 ([Euclid](http://projecteuclid.org/euclid.cmp/1104115581))

* {#AlvaresGaumeBostMooreNelsonVafa87} [[Luis Alvarez-Gaumé]], [[Jean-Benoit Bost]], [[Gregory Moore]], Philip Nelson, [[Cumrun Vafa]], _Bosonization on higher genus Riemann surfaces_, Communications in Mathematical Physics, Volume 112, Number 3 (1987), 503-552 ([Euclid](http://projecteuclid.org/euclid.cmp/1104159982))

* {#Freed87} [[Daniel Freed]], around p. 30-31 of _On determinant line bundles_, Math. aspects of [[string theory]], ed. S. T. Yau, World Sci. Publ. 1987,  (revised [pdf](http://www.math.utexas.edu/~dafr/Index/determinants.pdf), [dg-ga/9505002](http://arxiv.org/abs/dg-ga/9505002))


* {#Andersen11} Johan Martens [[Jørgen Andersen]], notes by S&#248;ren J&#248;rgensen, p. 53 of _Topological quantum field theories and moduli spaces_, 2011 ([pdf](http://maths.fuglede.dk/noter/tqftms.pdf))

and more generally the [[partition functions]] of connection-twisted Dirac operators on even-dimensional locally symmetric spaces is discussed in

* {#BunkeOlbrich94}  [[Ulrich Bunke]], [[Martin Olbrich]], _Theta and zeta functions for locally symmetric spaces of rank one_ ([arXiv:dg-ga/9407013](http://arxiv.org/abs/dg-ga/9407013))

Generalization of this from abelian to non-abelian [[conformal blocks]] to "generalized theta functions" appears in

* {#BeauvilleLaszlo93} [[Arnaud Beauville]], [[Yves Laszlo]], _Conformal blocks and generalized theta functions_, Comm. Math. Phys. __164__ (1994), 385 - 419, [euclid](http://projecteuclid.org/euclid.cmp/1104270837), [alg-geom/9309003](http://arxiv.org/abs/alg-geom/9309003), [MR1289330](http://www.ams.org/mathscinet-getitem?mr=1289330)


That the Riemann zeta functions are the local coordinate expressions of the covariantly constant sections of the [[Hitchin connection]] is due to 

* {#Hitchin90} [[Nigel Hitchin]], remark 4.12 in _Flat connections and geometric quantization_, : Comm. Math. Phys. Volume 131, Number 2 (1990), 347-380. ([Euclid](http://projecteuclid.org/euclid.cmp/1104200841))
 

Relation to [[elliptic genera]] (see also at _[[Jacobi form]]_)

* {#KL95} [[Kefeng Liu]], section 2.4 of _On modular invariance and rigidity theorems_, J. Differential Geom. Volume 41, Number 2 (1995), 247-514 ([EUCLID](http://projecteuclid.org/euclid.jdg/1214456221), [pdf](http://www.math.ucla.edu/~liu/Research/loja.pdf))


Theta functions for higher dimensional varieties and their relation to [[automorphic forms]] is due to 

* [[André Weil]], _Sur certaines groups d'operateur unitaires_, Acta. Math.  111 (1964), 143-211

see [Gelbhart 84, page 35 (211)](Langlands+program#Gelbhart84) for review.

Further developments here include

* {#Kudla77} [[Stephen Kudla]], _Relations between automorphic forms produced by theta-functions_, in _Modular Functions of One Variable VI_, Lecture Notes in Math. 627, Springer, 1977, 277&#8211;285.

* {#Kudla78} [[Stephen Kudla]], _Theta functions and Hilbert modular forms_,Nagoya Math. J. 69 (1978) 97-106


* {#Stopple95} [[Jeffrey Stopple]], _Theta and $L$-function splittings_, Acta Arithmetica LXXII.2 (1995) ([pdf](http://matwbn.icm.edu.pl/ksiazki/aa/aa72/aa7221.pdf))

* Yum-Tong Siu, _Theta functions in higher dimensions_ ([[SiuHigherTheta.pdf:file]])

[[!redirects theta functions]]
[[!redirects theta-function]]
[[!redirects theta-functions]]

[[!redirects Theta function]]
[[!redirects Theta functions]]
[[!redirects Theta-function]]
[[!redirects Theta-functions]]

[[!redirects theta-line bundle]]
[[!redirects theta-line bundles]]
[[!redirects theta line bundle]]
[[!redirects theta line bundles]]
[[!redirects theta line-bundle]]
[[!redirects theta line-bundles]]