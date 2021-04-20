
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In the original sense, _microlocal analysis_ (e.g. [Strohmaier 09](#Strohmaier09)) is the study of the [[functional analysis]] of [[generalized functions]]/[[distributions]] with attention paid not just to their [[singular support]], i.e. to the points around which they are singular as generalized functions, but also the directions of [[propagation of singularities theorem|propagation of their singularities]] at each singular point, which is the set of [[covectors]] known as their [[wave front set]]. This extra directional ("microlocal") information governs the basic operations on distributions, notably the [[pullback of distributions]] and the [[product of distributions]].

Since the wave front set is the set of (co-)directions along which, locally, the [[Fourier transform of distributions]] is not rapidly decreasing (the set of "[[UV divergences]]" in applications to [[perturbative quantum field theory]]), much of microlocal analysis is concerned with constructions related to Fourier transformation, such as the discussion of [[pseudodifferential operators]].

Microlocal analysis in this sense was introduced by ([Sato 70](#Sato70)),  soon  followed  by  ([H&#246;rmander 71](#Hoermander71), [H&#246;rmander 83](#Hoermander83)) who  both  introduced the notion of [[wave front set]].
This microlocal point of  view was then extended to [[sheaf  theory]]  by
[Kashiwara-Schapira 82](#KashiwaraSchapira82), [Kashiwara-Schapira 82](#KashiwaraSchapira85)) who  introduced  the  notion  of _[[microsupport]]_  of  sheaves giving rise to _[[microlocal sheaf theory]]_ (see [Schapira 17](#Schapira17)). Beware that some authors still use the term "microlocal analysis" for this sheaf theoretic concept.


## Overview

To accommodate an intuitive notion of a "function of differential operators" there is a simple trick used: consider the [[Fourier transform]]. Then the [[differential operators]] become polynomials. This correspondence of operators and their [[symbol of a differential operator|symbols]] may, with some analytic care, be extended to define generalizations of differential operators by suitably extending a notion of symbols. Thus the [[pseudodifferential operator]]s of Kohn and Nirenberg appeared in 1965 with soon following  revolution in harmonic analysis and analysis in [[PDE]]. This includes a  further generalization, the Fourier integral operators of [[Lars Hörmander]] and V. Maslov. A part of harmonic analysis involving geometric aspects in the cotangent bundles of such methods is called **microlocal analysis**. The geometric aspects include the support, wavefront set, characteristics...of distributions, pseudodifferential operators and their symbols. There are more technical definitions (involving [[wavefront set]]s, supports and filtrations on the algebras of symbols) of various "microlocal" properties of symbols: [[microlocalization]], microhypoellipticity, microparametrix etc.). In addition to the analytic microlocalization there is a formal microlocalization; and a version of filtered localization theory in noncommutative algebra, so called [[algebraic microlocalization]], which is however not used in operator theory. While local aspect of a differential operator is about its behaviour around a point in coordinate space, the microlocal aspect is about a point in the cotangent bundle, hence it also localizes around the fixed covector direction, hence "micro". 

This is clearly related to the general study of oscillating integrals, including the stationary phase method and WKB-method (and generalizations) in particular. These kind of approximations and related estimates are of importance to the study of the propagation of singularities of differential equations, wave fronts, eikonal equations, and so on.

As oscillating integrals are involved in the analysis of various [[Green functions]] like the [[heat kernel]] there is also a connection to [[index theorems]] for [[elliptic differential operators]], see [H&#246;rmander 83](#Hoermander83).

## In perturbative quantum field theory

In [[perturbative quantum field theory]] microlocal analysis is used to define [[Wick algebras]] of [[quantum observables]] on [[free fields]]: The product on these algebras is a [[Moyal star-product]] induced from the [[Peierls-Poisson bracket]], whose [[integral kernel]] is the [[causal propagator]] on the given [[globally hyperbolic spacetime]]. But the [[wave front set]] of this propagator is such that its [[UV-divergences]] in general collide with those of [[local functionals]] ([here](Wick+algebra#CompactlySupportedPolynomialLocalDensities)). This is fixed by modifying the causal propagator to a [[Hadamard propagator]]. The resulting change of the algebra structure is known as [[normal ordering]] of quantum fields. It yields the properly defined _[[Wick algebras]]_ of free quantum fields.

As the name suggests, normal ordering was originally an operation implementd simply by re-arranging the order of [[Fourier transform|Fourier]] modes of quantum fields. The desire to generalize this procedure from [[Minkowski spacetime]] to general [[globally hyperbolic Lorentzian manifolds]] was what required use of tools from microlocal analysis. See at _[[locally covariant perturbative AQFT]]_ and at _[[S-matrix]]_ for more.
 
## Related concepts

* [[wave front set]], [[microsupport]]

* [[microlocal sheaf theory]]

* [[propagation of singularities theorem]]

* [[microformal morphism]]

## References

Microlocal analysis of [[distributions]] in terms of [[wave front sets]] was introduced in

* {#Sato70} [[Mikio Sato]], _Regularity of hyperfunctions solutions of partial differential equations 2 (1970), 785&#8211;794.

* {#Hoermander71} [[Lars Hörmander]], _Fourier integral operators_ I. Acta Math. 127 (1971)


* {#Hoermander83} [[Lars Hörmander]], _The analysis of linear partial differential operators_, in 4 vols.: _I. Distribution theory and Fourier analysis_, _II. Differential operators with constant coefficients_, _III. Pseudo-differential operators_, _IV. Fourier integral operators_, Grundlehren der mathematischen Wissenschaften 256, Springer 1983, 1990 

Survey is in

* {#Strohmaier09} Alexander Strohmaier, chapter _Microlocal analysis_ ([web](https://link.springer.com/chapter/10.1007%2F978-3-642-02780-2_4)) in [[Christian Bär]], [[Klaus Fredenhagen]] _Quantum Field Theory on Curved Spacetime_, 2009 ([web](https://link.springer.com/book/10.1007
/978-3-642-02780-2))

* A. Kaneko, _[Microlocal analysis](http://eom.springer.de/M/m063760.htm)_, Springer Online Enc. Of Math.

Comprehensive lecture notes are in

* {#Melrose03} [[Richard Melrose]], _Introduction to microlocal analysis_, 2003 ([pdf](http://www-math.mit.edu/~rbm/iml90.pdf))


See also

* C. Bardos, L. Boutet de Monvel, _From atomic hypothesis to microlocal analysis_ (lecture notes) [pdf](www.math.jussieu.fr/~boutet/Micro_equations.pdf)

* A. Grigis, J. Sj&#246;strand, _Microlocal analysis for differential operators: an introduction_,   Cambridge U.P. 1994. 

* [[Hans Duistermaat]], _Fourier integral operators_, Progress in Mathematics, Birkh&#228;user 1995.

* [[Victor Guillemin]], [[Masaki Kashiwara]], Takahiro Kawai, _Seminar on micro-local analysis_, Ann. of Math. Studies 93 (1979), [googlebooks](books.google.hr/books?isbn=0691082324)

* Yu. V. Egorov,  _Microlocal analysis_, &#1070;. &#1042;. &#1045;&#1075;&#1086;&#1088;&#1086;&#1074;, _&#1052;&#1080;&#1082;&#1088;&#1086;&#1083;&#1086;&#1082;&#1072;&#1083;&#1100;&#1085;&#1099;&#1081; &#1072;&#1085;&#1072;&#1083;&#1080;&#1079;_, &#1044;&#1080;&#1092;&#1092;&#1077;&#1088;&#1077;&#1085;&#1094;&#1080;&#1072;&#1083;&#1100;&#1085;&#1099;&#1077; &#1091;&#1088;&#1072;&#1074;&#1085;&#1077;&#1085;&#1080;&#1103; &#1089; &#1095;&#1072;&#1089;&#1090;&#1085;&#1099;&#1084;&#1080; &#1087;&#1088;&#1086;&#1080;&#1079;&#1074;&#1086;&#1076;&#1085;&#1099;&#1084;&#1080; &#8211; 4, &#1048;&#1090;&#1086;&#1075;&#1080; &#1085;&#1072;&#1091;&#1082;&#1080; &#1080; &#1090;&#1077;&#1093;&#1085;. &#1057;&#1077;&#1088;. &#1057;&#1086;&#1074;&#1088;&#1077;&#1084;. &#1087;&#1088;&#1086;&#1073;&#1083;. &#1084;&#1072;&#1090;. &#1060;&#1091;&#1085;&#1076;&#1072;&#1084;. &#1085;&#1072;&#1087;&#1088;&#1072;&#1074;&#1083;&#1077;&#1085;&#1080;&#1103;, 33, &#1042;&#1048;&#1053;&#1048;&#1058;&#1048;, &#1052;., 1988, 5-&#8211;156, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=intf&paperid=116&what=fullt&option_lang=rus), [MR93e:35002](http://www.ams.org/mathscinet-getitem?mr=1175403), Eng. translation in Partial Differential Equations IV (Egorov, Shubin eds.), Springer 1993 [doi](https://dx.doi.org/10.1007/978-3-662-09207-1)

* Yu. Safarov, _Distributions, Fourier transforms and microlocal analysis_ (course online notes), [pdf](https://nms.kcl.ac.uk/yuri.safarov/Lectures/LTCC2014a/pdos-2014a1.pdf)


Application in [[perturbative quantum field theory]]:

* Christian Gérard, *Microlocal Analysis of Quantum Fields on Curved Spacetimes* ([arXiv:1901.10175](https://arxiv.org/abs/1901.10175))






