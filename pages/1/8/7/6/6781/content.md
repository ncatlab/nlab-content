
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

[[quasitriangular Hopf algebra|Quasitriangular Hopf algebras]] appear as the symmetries of some models in rational [[conformal field theory]]. 

Representations of a 
[[Hopf algebra]] make a [[braided monoidal category]]. Thus the [[Hilbert space]] is a [[representation]] of a Hopf algebra. This framework allows for natural class of weakenings by changing [[associativity]] [[coherence]], what amounts to the twist by a nonabelian [[bialgebra cocycle|bialgebra 3-cocycle]] and yields the notion of a quasi-Hopf algebra as introduced in

* [[Vladimir Drinfel'd]], _&#1050;&#1074;&#1072;&#1079;&#1080;&#1093;&#1086;&#1087;&#1092;&#1086;&#1074;&#1099; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;&#1099;_, Algebra i Analiz __1__ (1989), no. 6, 114--148, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=aa&paperid=53&what=fullt&option_lang=rus); translation _Quasi-Hopf algebras_, Leningrad Math. J. __1__ (1990), no. 6, 1419&#8211;1457 [MR1047964](http://www.ams.org/mathscinet-getitem?mr=1047964)

## Definition

A __quasibialgebra__ is a unital [[associative algebra]] $(A,m,\eta)$ with a structure of not necessarily coassociative coalgebra $(A,\Delta,\epsilon)$ and an invertible element $\phi \in A\otimes A\otimes A$ such that 

$$
(1\otimes\Delta)\Delta(a) = \phi\left((1\otimes\Delta)\Delta(a)\right)\phi^{-1},\,\,\,\,\,\forall a\in A,
$$
$$
(1\otimes 1\otimes\Delta)(\phi)(\Delta\otimes 1\otimes 1)(\phi) =
(1\otimes\phi)(1\otimes\Delta\otimes 1)(\phi)(\phi\otimes 1)
$$

and some identities involving unit $\eta$ and counit $\epsilon$ hold.

A __quasi-Hopf algebra__ is a quasibialgebra with a suitable notion of an antipode.

## Related concepts

* [[hopfish algebra]]

## References

Other articles

* &#1042;. &#1043;. &#1044;&#1088;&#1080;&#1085;&#1092;&#1077;&#1083;&#1100;&#1076;, _&#1054; &#1089;&#1090;&#1088;&#1091;&#1082;&#1090;&#1091;&#1088;&#1077; &#1082;&#1074;&#1072;&#1079;&#1080;&#1090;&#1088;&#1077;&#1091;&#1075;&#1086;&#1083;&#1100;&#1085;&#1099;&#1093; &#1082;&#1074;&#1072;&#1079;&#1080;&#1093;&#1086;&#1087;&#1092;&#1086;&#1074;&#1099;&#1093; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;_, &#1060;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;. __26__:1 (1992), 78&#8211;80, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=768&what=fullt&option_lang=rus); transl. V. G. Drinfeld, _Structure of quasitriangular quasi-hopf algebras_, Funct. Anal. Appl., 26:1 (1992), 63&#8211;65
* V. G. Drinfel&#697;d, _&#1054; &#1082;&#1074;&#1072;&#1079;&#1080;&#1090;&#1088;&#1077;&#1091;&#1075;&#1086;&#1083;&#1100;&#1085;&#1099;&#1093; &#1082;&#1074;&#1072;&#1079;&#1080;&#1093;&#1086;&#1087;&#1092;&#1086;&#1074;&#1099;&#1093; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;&#1072;&#1093; &#1080; &#1086;&#1076;&#1085;&#1086;&#1081; &#1075;&#1088;&#1091;&#1087;&#1087;&#1077;, &#1090;&#1077;&#1089;&#1085;&#1086; &#1089;&#1074;&#1103;&#1079;&#1072;&#1085;&#1085;&#1086;&#1081; &#1089; $\mathrm{Gal}(\overline{\mathbf{Q}}/\mathbf {Q})$_, Algebra i Analiz 2 (1990), no. 4, 149--181, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=aa&paperid=199&volume=2&year=1990&issue=4&fpage=149&what=fullt&option_lang=eng); translation _On quasitriangular quasi-Hopf algebras and on a group that is closely connected with $\mathrm{Gal}(\overline{\mathbf{Q}}/\mathbf {Q})$_, Leningrad Math. J. __2__ (1991), no. 4, 829&#8211;860, [MR1080203](http://www.ams.org/mathscinet-getitem?mr=1080203)
* V. G. Drinfel&#697;d, _Quasi-Hopf algebras and Knizhnik-Zamolodchikov equations_, Problems of modern quantum field theory (Alushta, 1989), 1&#8211;13, Res. Rep. Phys., Springer 1989.
* R. Dijkgraaf, V. Pasquier, P. Roche, _QuasiHopf algebras, group cohomology and orbifold models_, Nucl. Phys. B Proc. Suppl. __18B__ (1990), 60-72; _Quasi-quantum groups related to orbifold models_, Modern quantum field theory (Bombay, 1990), 375&#8211;383, World Sci. 1991

* [[Shahn Majid]], _Quantum double for quasi-Hopf algebras_, Lett. Math. Phys. __45__ (1998), no. 1, 1&#8211;9, [MR2000b:16077](http://www.ams.org/mathscinet-getitem?mr=1631648), [doi](http://dx.doi.org/10.1023/A:1007450123281), [q-alg/9701002](http://arxiv.org/abs/q-alg/9701002)

[[!redirects quasibialgebra]]
[[!redirects quasihopf algebra]]
[[!redirects quasiHopf algebra]]
[[!redirects quasi-bialgebra]]