#Contents#
* automatic table of contents goes here
{:toc}

## Overview

Semiclassical or quasiclassical approximation to [[quantum mechanics]] (including infinitely many degrees of freedom, e.g. QFT) in most general sense is the series expansion of the transition amplitudes in Planck constant. However more specifically one considers the Feynman path integral $\int D\phi F(\phi) e^{iS(\phi)/h}$ and develops it by a stationary phase method about the critical points of the action functional $S$ (the critical points of $S$ correspond to the solutions of the [[Euler-Lagrange equation]]s, hence to the classical trajectories of the system). Namely $S$ is assumed to be large and change fast in comparison to the Planck constant, so the increments of $i\pi$ in the phase of the exponent appear very often leading to mutual cancellation, except in the regions close to the critical points. 

Semiclassical method in more traditional Schroedinger wave equation approach due to Wentzel, Kramers and Brillouin (WKB or WKBJ method, see [wikipedia](http://en.wikipedia.org/wiki/WKB_approximation)), amounts to the expression of the wave function in the form $\phi = exp(S)$ where $S$ is a slowly varying function and solving the equation for $S$. This makes sense for a more general class of wave equations, and in wave optics this short-wave limit is the approximation of [[geometrical optics]] where $S$ is called the **eikonal**. Globally consistent solutions in first order lead to so-called Bohr-Sommerfeld quantization conditions. Multidimensional generalization of WKB method appear to be rather nontrivial; it has been pioneered by V. Maslov who introduced a topological invariant to remove ambiguities of the naive version of the method ([[Maslov index]]). 

## Semiclassical approximation and equivariant localization

In some special cases (most often in the presence of supersymmetry) the main contribution (the first term in expansion) amounts to the true result; the quantum correction sometimes leads however to an overall scalar factor. This is the case of so-called localization (related directly in some cases to the equivariant localization in cohomology and Lefshetz-type fixed point formulas). Most of well known examples of integrable systems and TQFTs lead to localization. 

## Large N-limit 

Large N-limit of gauge theories, which is of importance in [[collective field theory]] and in the study of relation between gauge and string theories is formally very similar to semiclassical expansion, where the role of Planck constant is played by $1/N^2$. 

## Terminology

In the theory of radiation there is a different meaning of semiclassical treatment: one considers particles in a sorrounding electromagnetic field and the particles are treated as in finite-dimensional quantum mechanics, with the electromagnetic field as an external classical field coupled to the particles via an interaction term. 

## Literature

* M.V. Fedoryuk, _Semi-classical approximation_, Springer [Online](http://eom.springer.de/S/s083990.htm) Enc. of Math.

* Sean Bates, Alan Weinstein, _Lectures on the geometry of quantization_, [pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf)

* V. P. Maslov, _Stationary-phase method for Feynman's continual integral_, Theoret. and Math. Phys., 2:1 (1970), 21&#8211;25; Russian original: &#1058;&#1052;&#1060;, 2:1 (1970), 30&#8211;35 [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=tmf&paperid=3986&what=fullt&option_lang=rus).

* V. P. Maslov, _Theory of perturbations and asymptotic methods_ (Russian), Izdat. Moskov. Gos. Univ. 1965.

* V. I. Arnol'd, _Characteristic class entering in quantization conditions_, Funct. Anal. its Appl. 1967, 1:1, 1&#8211;13, [doi](http://dx.doi.org/10.1007/BF01075861) (&#1042;. &#1048;. &#1040;&#1088;&#1085;&#1086;&#1083;&#1100;&#1076;, "&#1054; &#1093;&#1072;&#1088;&#1072;&#1082;&#1090;&#1077;&#1088;&#1080;&#1089;&#1090;&#1080;&#1095;&#1077;&#1089;&#1082;&#1086;&#1084; &#1082;&#1083;&#1072;&#1089;&#1089;&#1077;, &#1074;&#1093;&#1086;&#1076;&#1103;&#1097;&#1077;&#1084; &#1074; &#1091;&#1089;&#1083;&#1086;&#1074;&#1080;&#1103; &#1082;&#1074;&#1072;&#1085;&#1090;&#1086;&#1074;&#1072;&#1085;&#1080;&#1103;", &#1060;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;., 1:1 (1967), 1&#8211;14, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=2802&what=fullt&option_lang=rus)) 

* V. Guillemin, S. Sternberg, _Geometric asymptotics_, AMS 1977, [online](http://www.ams.org/online_bks/surv14)

* A. S. Mishchenko, B. Yu. Sternin, V. E. Shatalov, _Lagrangian manifolds
and the canonical operator method_, Nauka, Moscow, 1978. 
(in Russian). English transl.: _Lagrangian manifolds and the Maslov operator_, Springer, Berlin, 1990.

* Richard J. Szabo, _Equivariant cohomology and localization of path integrals_, Lecture Notes in Physics, N.S. Monographs __63__. Springer  2000. xii+315 pp. (early version: _Equivariant localization of path integrals_, [hep-th/9608068](http://arxiv.org/abs/hep-th/9608068))

* M. F. Atiyah, _Circular symmetry and stationary phase approximation_, Asterisque __131__ (1985) 43--59

* N. Berline, [[Ezra Getzler]], M. Vergne, _Heat kernels and Dirac operators_, Grundlehren __298__, Springer 1992, "Text Edition" 2003. 

* Albert Schwarz, Oleg Zaboronsky, _Supersymmetry and localization_, Comm. Math. Phys. __183__, 2 (1997), 463-476, [euclid](http://projecteuclid.org/euclid.cmp/1158328185)

* [[Albert Schwarz]], _Semiclassical approximation in [[Batalin-Vilkovisky quantization|Batalin-Vilkovisky formalism]]_, Comm. Math. Phys.  __158__ (1993), no. 2, 373--396, [euclid](http://projecteuclid.org/euclid.cmp/1104254246). 

For large N-limit compared to semiclassical expansion see

*  L. G. Yaffe, _Large N limits as classical mechanics_, Rev. Mod. Phys. __54__, 407&#8211;435 (1982), [pdf](http://rmp.aps.org/pdf/RMP/v54/i2/p407_1)

For the semiclassical method in [[superstring theory]] see 

* J. Maldacena, G. Moore, N. Seiberg, D. Shih, _Exact vs. semiclassical target space of the minimal string_, [hep-th/0408039](http://arxiv.org/abs/hep-th/0408039)

* K. Hori, A. Iqbal, C. Vafa, _D-Branes and mirror symmetry_, [hep-th/0005247](http://arxiv.org/abs/hep-th/0005247) 


[[!redirects quasiclassical approximation]]
[[!redirects quasi-classical approximation]]
[[!redirects semiclassical expansion]]
[[!redirects WKB method]]
[[!redirects WKB approximation]]