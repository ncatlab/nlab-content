
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

### General

The notion of a _quasi-Hopf algebra_ generalizes this of a [[Hopf algebra]] by weakening the [[associativity]] [[coherence]] ([Drinfeld 89](#Drinfeld89)). 

In particular, quasi-Hopf algebras may be obtained from ordinary Hopf algebras by twisting by a [[Drinfeld associator]], i.e. a nonabelian [[bialgebra cocycle|bialgebra 3-cocycle]].

### Motivation from quantum field theory

Drinfel'd was motivated by study of [[monoidal categories]] in [[rational CFT|rational]] 2d [[conformal field theory]] (RCFT) as well as by an idea from [[Grothendieck]]'s _[[Esquisse d'un programme|Esquisse]]_ namely the [[Grothendieck-Teichmüller tower]] and its modular properties. In RCFT, the [[monoidal categories]] appearing can be, by [[Tannaka duality|Tannaka reconstruction]] considered as [[categories of modules]] of [[Hopf algebra]]-like objects where the flexibility of associativity coherence in building a theory were natural thus leading to quasi-Hopf algebras. 

A special case of the motivation in RCFT has a toy example of [[Dijkgraaf-Witten theory]] which can be quite geometrically
explained. Namely, where the [[groupoid convolution algebra]] of the [[delooping]] [[groupoid]] $\mathbf{B}G$ of a [[finite group]] $G$ naturally has the structure of a Hopf algebra, the [[twisted groupoid convolution algebra]] of $\mathbf{B}G$ equipped with a 3-[[cocycle]] $c \colon \mathbf{B}G \to \mathbf{B}^3 U(1)$ is naturally a quasi-Hopf algebra.
Since such a 3-cocycle is precisely the [[background gauge field]] of the 3d [[TFT]] called [[Dijkgraaf-Witten theory]], and hence quasi-Hopf algebras arise there ([Dijkgraaf-Pasquier-Roche 91](#DijkgraafPasquierRoche)).

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

* [[quasitriangulated quasi-Hopf algebra]]

## References

The notion was introduced in 

* [[Vladimir Drinfel'd]], _&#1050;&#1074;&#1072;&#1079;&#1080;&#1093;&#1086;&#1087;&#1092;&#1086;&#1074;&#1099; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;&#1099;_, Algebra i Analiz __1__ (1989), no. 6, 114--148, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=aa&paperid=53&what=fullt&option_lang=rus); translation _Quasi-Hopf algebras_, Leningrad Math. J. __1__ (1990), no. 6, 1419&#8211;1457 [MR1047964](http://www.ams.org/mathscinet-getitem?mr=1047964)
 {#Drinfeld89}

The relation to [[Dijkgraaf-Witten theory]] appeared in

* [[Robbert Dijkgraaf]], V. Pasquier, P. Roche, _QuasiHopf algebras, group cohomology and orbifold models_, Nucl. Phys. B Proc. Suppl. __18B__ (1990), 60-72; _Quasi-quantum groups related to orbifold models_, Modern quantum field theory (Bombay, 1990), 375&#8211;383, World Sci. 1991
 {#DijkgraafPasquierRoche}



Other articles include 

* &#1042;. &#1043;. &#1044;&#1088;&#1080;&#1085;&#1092;&#1077;&#1083;&#1100;&#1076;, _&#1054; &#1089;&#1090;&#1088;&#1091;&#1082;&#1090;&#1091;&#1088;&#1077; &#1082;&#1074;&#1072;&#1079;&#1080;&#1090;&#1088;&#1077;&#1091;&#1075;&#1086;&#1083;&#1100;&#1085;&#1099;&#1093; &#1082;&#1074;&#1072;&#1079;&#1080;&#1093;&#1086;&#1087;&#1092;&#1086;&#1074;&#1099;&#1093; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;_, &#1060;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;. __26__:1 (1992), 78&#8211;80, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=768&what=fullt&option_lang=rus); transl. V. G. Drinfeld, _Structure of quasitriangular quasi-hopf algebras_, Funct. Anal. Appl., 26:1 (1992), 63&#8211;65
* V. G. Drinfel&#697;d, _&#1054; &#1082;&#1074;&#1072;&#1079;&#1080;&#1090;&#1088;&#1077;&#1091;&#1075;&#1086;&#1083;&#1100;&#1085;&#1099;&#1093; &#1082;&#1074;&#1072;&#1079;&#1080;&#1093;&#1086;&#1087;&#1092;&#1086;&#1074;&#1099;&#1093; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;&#1072;&#1093; &#1080; &#1086;&#1076;&#1085;&#1086;&#1081; &#1075;&#1088;&#1091;&#1087;&#1087;&#1077;, &#1090;&#1077;&#1089;&#1085;&#1086; &#1089;&#1074;&#1103;&#1079;&#1072;&#1085;&#1085;&#1086;&#1081; &#1089; $\mathrm{Gal}(\overline{\mathbf{Q}}/\mathbf {Q})$_, Algebra i Analiz 2 (1990), no. 4, 149--181, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=aa&paperid=199&volume=2&year=1990&issue=4&fpage=149&what=fullt&option_lang=eng); translation _On quasitriangular quasi-Hopf algebras and on a group that is closely connected with $\mathrm{Gal}(\overline{\mathbf{Q}}/\mathbf {Q})$_, Leningrad Math. J. __2__ (1991), no. 4, 829&#8211;860, [MR1080203](http://www.ams.org/mathscinet-getitem?mr=1080203)
* V. G. Drinfel&#697;d, _Quasi-Hopf algebras and Knizhnik-Zamolodchikov equations_, Problems of modern quantum field theory (Alushta, 1989), 1&#8211;13, Res. Rep. Phys., Springer 1989.

* [[Shahn Majid]], _Quantum double for quasi-Hopf algebras_, Lett. Math. Phys. __45__ (1998), no. 1, 1&#8211;9, [MR2000b:16077](http://www.ams.org/mathscinet-getitem?mr=1631648), [doi](http://dx.doi.org/10.1023/A:1007450123281), [q-alg/9701002](http://arxiv.org/abs/q-alg/9701002)
* Peter Schauenburg, _Hopf modules and the double of a quasi-Hopf algebra_, Trans. Amer. Math. Soc. __354__ (2002), 3349-3378 [pdf](http://www.ams.org/journals/tran/2002-354-08/S0002-9947-02-02980-X/S0002-9947-02-02980-X.pdf)

[[!redirects quasibialgebra]]
[[!redirects quasihopf algebra]]
[[!redirects quasiHopf algebra]]
[[!redirects quasi-bialgebra]]
[[!redirects quasi-Hopf algebras]]
