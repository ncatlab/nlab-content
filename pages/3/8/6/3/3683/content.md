
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Overview

To some extent, [[quantum mechanics]] and [[quantum field theory]] are a [[deformation theory|deformation]] of [[classical mechanics]] and [[classical field theory]], with the deformation parameterized by [[Planck's constant]] $\hbar$. The _semiclassical approximation_ or _quasiclassical approximation_ to [[quantization]]/[[quantum mechanics]] is the restriction of this deformation to just first order (or some finite order) in $\hbar$.

[[!include classical-to-quantum notions - table]]

Applied to [[path integral]] [[quantization]], the semiclassical approximation is meant to approximate the [[path integral]] 
$\int_{\phi \in \mathbf{Fields}} D\phi\; F(\phi) e^{iS(\phi)/\hbar}$ by an expansion in $\hbar$ about the [[critical points]] of the [[action functional]] $S$ (hence the solutions of the [[Euler-Lagrange equations]], hence to the classical trajectories of the system). As usual for the [[path integral]] in [[physics]], this often requires work to make precise, but at a heuristic level the idea is famous as the _[[rotating phase approximation]]_: the idea is that in regions of [[field (physics)|field]]-space where $S$ varies fast as measured in units of [[Planck's constant]], the [[complex number|complex phases]] of the integrand $\exp(i S / \hbar )$ tend to cancel each other in the integral so that substantial contributions to the integral come only from the vicininity of critical points of $S$ (classical [[trajectories]]).

But semiclassical approximations can be applied to most other formulations of [[quantum physics]], where they often lead to precise and powerful mathematical tools.

Notably in the [[Schrödinger picture]] of quantum evolution, solutions to the [[Schrödinger equation]] $i \hbar \frac{d}{d t} \psi = \hat H \psi$ (which characterizes [[quantum states]] given by [[wave functions]] $\psi$ for [[Hamiltonian mechanics|Hamiltonian dynamics]] induced by a [[Hamilton operator]] $\hat H$) are usefully considered to first (or any finite) order in $\hbar$.
This method, known after (some of) its inventors as the **[[WKB method]]** or similar, amounts to expressing the [[wave function]] in the form $\psi = exp(S)$ where $S$ is a slowly varying function and solving the equation for $S$. 
Globally consistent such solutions to first order lead to what are called [[Bohr-Sommerfeld leaf|Bohr-Sommerfeld quantization conditions]]. 
For the formalization of this method in [[symplectic geometry]]/[[geometric quantization]] see at _[[semiclassical state]]_.

This [[WKB method]] makes sense for a more general class of 
[[wave equations]]. For instance in [[wave mechanics|wave]] [[optics]] this yields the short-[[wavelength]] limit of the [[geometrical optics]] approximation. Here $S$ is called the **[[eikonal]]**. 

Multidimensional generalization of the [[WKB method]] appear to be rather nontrivial; they have been pioneered by [[Victor Maslov]] who introduced a topological invariant to remove ambiguities of the naive version of the method, called the _[[Maslov index]]_.

## Related phenomena

### Equivariant localization

In some special cases (most often in the presence of supersymmetry) the main contribution (the first term in expansion) amounts to the true result; the quantum correction sometimes leads however to an overall scalar factor. This is the case of so-called localization (related directly in some cases to the equivariant localization in cohomology and Lefshetz-type fixed point formulas). Most of well known examples of integrable systems and TQFTs lead to localization. 

### Large $N$-limit in gauge theories

The [[large N limit]] of gauge theories, which is of importance in [[collective field theory]] and in the study of relation between gauge and string theories is formally very similar to semiclassical expansion, where the role of Planck constant is played by $1/N^2$. 

### In radiation theory

In the theory of radiation there is a different meaning of semiclassical treatment: one considers particles in a sorrounding electromagnetic field and the particles are treated as in finite-dimensional quantum mechanics, with the electromagnetic field as an external classical field coupled to the particles via an interaction term. 

## Literature

* M.V. Fedoryuk, _Semi-classical approximation_, Springer [Online](http://eom.springer.de/S/s083990.htm) Enc. of Math.

* Sean Bates, Alan Weinstein, _Lectures on the geometry of quantization_, [pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf)

* [[Victor Maslov]], _Stationary-phase method for Feynman's continual integral_, Theoret. and Math. Phys., 2:1 (1970), 21&#8211;25; Russian original: &#1058;&#1052;&#1060;, 2:1 (1970), 30&#8211;35 [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=tmf&paperid=3986&what=fullt&option_lang=rus).

* [[Victor Maslov]], _Theory of perturbations and asymptotic methods_ (Russian), Izdat. Moskov. Gos. Univ. 1965.

* [[Vladimir Arnold]], _Characteristic class entering in quantization conditions_, Funct. Anal. its Appl. 1967, 1:1, 1&#8211;13, [doi](http://dx.doi.org/10.1007/BF01075861) (&#1042;. &#1048;. &#1040;&#1088;&#1085;&#1086;&#1083;&#1100;&#1076;, "&#1054; &#1093;&#1072;&#1088;&#1072;&#1082;&#1090;&#1077;&#1088;&#1080;&#1089;&#1090;&#1080;&#1095;&#1077;&#1089;&#1082;&#1086;&#1084; &#1082;&#1083;&#1072;&#1089;&#1089;&#1077;, &#1074;&#1093;&#1086;&#1076;&#1103;&#1097;&#1077;&#1084; &#1074; &#1091;&#1089;&#1083;&#1086;&#1074;&#1080;&#1103; &#1082;&#1074;&#1072;&#1085;&#1090;&#1086;&#1074;&#1072;&#1085;&#1080;&#1103;", &#1060;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;., 1:1 (1967), 1&#8211;14, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=2802&what=fullt&option_lang=rus)) 

* [[Victor Guillemin]], [[Shlomo Sternberg]], _Geometric asymptotics_, AMS 1977, [online](http://www.ams.org/online_bks/surv14);  _Semi-classical analysis_, 499 pages, [pdf](http://www-math.mit.edu/~vwg/semistart.pdf)

* A. S. Mishchenko, B. Yu. Sternin, V. E. Shatalov, _Lagrangian manifolds
and the canonical operator method_, Nauka, Moscow, 1978. 
(in Russian). English transl.: _Lagrangian manifolds and the Maslov operator_, Springer, Berlin, 1990.

* [[Richard Szabo]], _Equivariant cohomology and localization of path integrals_, Lecture Notes in Physics, N.S. Monographs __63__. Springer  2000. xii+315 pp. (early version: _Equivariant localization of path integrals_, [hep-th/9608068](http://arxiv.org/abs/hep-th/9608068))

* [[Michael Atiyah]], _Circular symmetry and stationary phase approximation_, Asterisque __131__ (1985) 43--59

* [[Nicole Berline]], [[Ezra Getzler]],  [[Michèle Vergne]], _Heat kernels and Dirac operators_, Grundlehren __298__, Springer 1992, "Text Edition" 2003. 

* [[Albert Schwarz]], Oleg Zaboronsky, _Supersymmetry and localization_, Comm. Math. Phys. __183__, 2 (1997), 463-476, [euclid](http://projecteuclid.org/euclid.cmp/1158328185)

* [[Albert Schwarz]], _Semiclassical approximation in [[Batalin-Vilkovisky quantization|Batalin-Vilkovisky formalism]]_, Comm. Math. Phys.  __158__ (1993), no. 2, 373--396, [euclid](http://projecteuclid.org/euclid.cmp/1104254246). 
* A. Laptev, I.M. Sigal, _Global Fourier integral operators and semiclassical asymptotics_, Review of Math. Physics, __12__:5 (2000) 749--766 [pdf](http://www.math.kth.se/~laptev/Research/Papers/LSig.pdf)
* Maurice A. de Gosson, _Symplectic geometry, Wigner-Weyl-Moyal calculus, and quantum mechanics in phase space_, 385 pp. [pdf](http://opus.kobv.de/ubp/volltexte/2009/3021/pdf/2006_06.pdf)
* Semyon Dyatlov, _Semiclassical Lagrangian distributions_, [pdf](http://math.mit.edu/~dyatlov/files/2012/hlagrangians.pdf); _Hoermander&#8211;Kashiwara and Maslov indices_, [pdf](http://math.berkeley.edu/~dyatlov/files/2009/maslov.pdf)
* Shanzhong Sun, _Gutzwiller's semiclassical trace formula and Maslov-type index theory for symplectic paths_, [arxiv/1608.08294](https://arxiv.org/abs/1608.08294)
 

Borel summability may make sense of the semiclassical expansion to all orders; this approach is sometimes called exact WKB method:

* A. Voros, _The return of the quartic oscillator. The complex WKB method_, Annales de l'institut Henri Poincar&#233; A39:3, 211-338 (1983) [euclid](http://eudml.org/doc/76217)

* Alexander Getmanenko, Dmitry Tamarkin, _Microlocal properties of sheaves and complex WKB_, [arxiv/1111.6325](http://arxiv.org/abs/1111.6325)

* Kohei Iwaki, Tomoki Nakanishi, _Exact WKB analysis and cluster algebras_, J. Phys. A 47 (2014) 474009 [arxiv/1401.7094](http://arxiv.org/abs/1401.7094); _Exact WKB analysis and cluster algebras II: simple poles, orbifold points, and generalized cluster algebras_, [arXiv:1409.4641](http://arxiv.org/abs/1409.4641)

Relation to quantum [[integrable system]]s is in a series of works of V&#361; Ng&#7885;c, e.g.

* San V&#361; Ng&#7885;c, _Bohr-Sommerfeld conditions for integrable systems with critical manifolds of focus-focus type_, Preprint Institut Fourier 433, 1998 15 [pdf](http://perso.univ-rennes1.fr/san.vu-ngoc/articles/focus-tout.pdf); _Quantum monodromy in integrable systems_,  Comm. Math. Phys. 203 (1999), no. 2, 465&#8211;479 [doi](http://dx.doi.org/10.1007/s002200050621)

For large N-limit compared to semiclassical expansion see

*  L. G. Yaffe, _Large N limits as classical mechanics_, Rev. Mod. Phys. __54__, 407&#8211;435 (1982), [pdf](http://rmp.aps.org/pdf/RMP/v54/i2/p407_1)

For the semiclassical method in [[superstring theory]] see 

* J. Maldacena, G. Moore, N. Seiberg, D. Shih, _Exact vs. semiclassical target space of the minimal string_, [hep-th/0408039](http://arxiv.org/abs/hep-th/0408039)

* K. Hori, A. Iqbal, C. Vafa, _D-Branes and mirror symmetry_, [hep-th/0005247](http://arxiv.org/abs/hep-th/0005247) 


[[!redirects quasiclassical approximation]]
[[!redirects quasi-classical approximation]]
[[!redirects semiclassical expansion]]
[[!redirects semiclassical analysis]][[!redirects semi-classical analysis]]

[[!redirects semiclassical quantization]]

[[!redirects semiclassical limit]]
[[!redirects semiclassical limits]]
