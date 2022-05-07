
#Contents#
* table of contents
{:toc}

## Idea

What is called _resurgence theory_ is a mathematical formalization of what in [[quantum field theory]] is known as reading off [[non-perturbative effects]] from the [[Feynman perturbation series]] ([[S-matrix]]) in [[perturbative quantum field theory]]. It tries to regard this non-converging [[formal power series]] in the [[coupling constant]] $g$ as an [[asymptotic series]] of a function involving [[analytic function|non-analytic]] contributions such as $e^{-1/g^2}$.

In [[quantum mechanics]] and [[quantum field theory]], [[renormalization|renormalized]] [[pQFT|perturbation theory]] produces expansions in powers of the [[coupling constant]] $g$. By appropriate [[resummation]] using the [[renormalization group]] one can also capture terms involving [[logarithm|logarithmic]] contributions of the form $\log (g/g_0)$. However, it is well-known that, e.g., [[instantons]] contribute terms of order $e^{-c/g}$ or $e^{-c/g^2}$, whose [[Taylor expansion]] is identically zero at $g = 0$, so that they do not contribute at all to the power series expansion. These contributions are therefore intrinsically [[non-perturbative effect|nonperturbative]].

A [[transseries]] is an expansion of a function $f(x)$ as a [[power series]] in a [[vector]] $z$ whose components are fixed functions of $x$. In [[quantum mechanics]] and [[quantum field theory]], the relevant case is $x=g$ or $x=g^2$ and $z_1=x$, $z_2=e^{-c/x}$, and in QFT usually also $z_3=\log(x/x_0)$. Clearly, transseries are more flexible than ordinary power series.

Resurgent functions are functions arising in the analysis of singular points of [[germs]] of [[analytic functions]]. Resurgent transseries are [[transseries]] that arise in methods for [[resummation]] that generalize [[Borel summation]] by looking at the [[obstructions]] for Borel summability such as [[renormalons]].

It turns out that using resurgent transseries, one can obtain under certain conditions information from the [[non-perturbative quantum field theory|nonperturbative sector]], starting from the [[Feynman perturbation series]] alone. The basic idea is to construct from the perturbative series the terms appearing in the [[renormalization group]] equation (RGE) by Callan and Symanzik, to substitute into it the leading terms of an appropriate transseries, and to determine the coefficients so that they match the RGE to the order specified.

To check that the method really works one can apply it to simple examples form quantum mechanics where other methods can be used to compute nonperturbative information. For example, for the double well potential, this was done by [Jentschura & Zinn-Justin 04](#JentschuraZinnJustin04) , and for some other cases by ([Dunne-Unsal 14](#DunneUnsal14)). For applications to [[gauge theories]] and to [[string theory]], see ([Marino 12](#Marino12)); of course, in the latter cases there is no known alternative way of checking the results. A more mathematically oriented overview is presented in ([Dorigoni 14](#Dorigoni14))

Thus it seems possible (and sometimes is claimed) that the perturbative series already contains all nonperturbative information. The future will tell.

## Related concepts

* [[resummation]]

* [[Borel resummation]]

## References

### General

Original articles include

* {#JentschuraZinnJustin04} Jentschura, [[Jean Zinn-Justin]], Phys. Lett. B 596 (2004), 138-144

* {#DunneUnsal14} [[Gerald Dunne]], Mithat Unsal, _Uniform WKB, Multi-instantons, and Resurgent Trans-Series_, Phys. Rev. D 89, 105009 (2014) ([arXiv:1401.5202](https://arxiv.org/abs/1401.5202))

A clear account is in 


* M. V. Berry, C. J. Howls, _Hyperasymptotics for Integrals with Saddles_, Proceedings: Mathematical and Physical Sciences Vol. 434, No. 1892 (Sep. 9, 1991), pp. 657-675 ([jstor:51890](https://www.jstor.org/stable/51890))

See p. 9 of https://arxiv.org/abs/1206.1890


Review includes


* {#Marino12} [[Marcos Marino]], _Lectures on non-perturbative effects in large N gauge theories, matrix models and strings_ ([arXiv:1206.6272](https://arxiv.org/abs/1206.6272))

* {#Dorigoni14} Daniele Dorigoni, _An Introduction to Resurgence, Trans-Series_ ([arXiv:1411.3585](https://arxiv.org/abs/1411.3585))

* {#Costin17} Ovidiu Costin, _The Mathematical Theory of Resurgence and Resummation, and Their Applications in Mathematics and Physics_, 2017 ([web](http://online.kitp.ucsb.edu/online/resurgent_c17/costin/))

* [[Gerald Dunne]], _Introduction to Resurgence, Trans-series and Non-perturbative Physics_, 2018 ([pdf](https://www.icts.res.in/sites/default/files/NUMSTRINGS2018-2018-01-27-Gerald-Dunne.pdf))


Part of the above text is taken from

* {#Neumaier16} [[Arnold Neumaier]], [PO comment](https://physicsoverflow.org/36857/what-are-resurgent-transseries?show=36859#a36859), 2016

See also

* Marco Serone, Gabriele Spada, Giovanni Villadoro, _Instantons from Perturbation Theory_ ([arXiv:1612.04376](https://arxiv.org/abs/1612.04376))

* Itzykson seminar at IHES,  _Resurgence and Quantization_, April 2017 ([web](https://www.fondation-hadamard.fr/fr/lmh-mathematiques-et-physique/seminaire-itzykson))

### In string theory

* [[Ricardo Schiappa]], _Resurgence Asymptotics in String Theory_, talk at IHES 2017 ([video](https://www.youtube.com/watch?v=8tw4MaBwTEA))

In the [[SYK model]] and [[AdS2-CFT1 duality]]:

* [[Paolo Gregori]], [[Ricardo Schiappa]], *From Minimal Strings towards Jackiw-Teitelboim Gravity: On their Resurgence, Resonance, and Black Holes* ([arXiv:2108.11409](https://arxiv.org/abs/2108.11409))


[[!redirects resurgence]]
