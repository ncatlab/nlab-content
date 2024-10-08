

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
=--
=--

> under construction

#Contents#
* table of contents
{:toc}

## Idea

### General

Given a suitable [[Lie algebra]] $\mathfrak{g}$ a __Knizhnik-Zamolodchikov equation__ is the [[equation]] expressing [[flat connection|flatness]] of certain class of [[vector bundles]] [[connection on a bundle|with connection]] on the [[configuration space of points]] of $N$ distinct points in the [[plane]] $\mathbb{C}$. It appeared in the study of [[Wess-Zumino-Novikov-Witten model]] (WZNW model) of [[2d CFT]] in ([Knizhnik-Zamolodchikov 84](#KnizhnikZamolodchikov84)).

The Knizhnik-Zamolodchikov equation involves what is called the __Knizhnik-Zamolodchikov connection__ and it is related to [[monodromy]] representations of Artin's [[braid group]].

In the standard variant, the basic data involves a given complex [[simple Lie algebra]] $\mathfrak{g}$ with a fixed bilinear  [[invariant polynomial]] $(-,-)$ (the _[[Killing form]]_) and $N$ (not necessarily [[finite-dimensional vector space|finite-dimensional]]) [[representations]] $V_1,\ldots, V_n$ of $\mathfrak{g}$. Let $V \,=\, V_1 \otimes \ldots \otimes V_N$.

(...)

### From geometric quantization of Chern-Simons theory
 {#FromGeometicQuantization}

The existence of the Knizhnik-Zamolodchikov connection can naturally be understood from the [[holographic principle|holographic]] [[quantization]] of the [[WZW model]] on the Lie group $G$ by [[geometric quantization]] of $G$-[[Chern-Simons theory]]:

As discussed there, for a 2-dimensional [[manifold]] $\Sigma$, a choice of [[polarization]] of the [[phase space]] of 3d [[Chern-Simons theory]] on $\Sigma$ is naturally induced by a choice $J$ of [[conformal structure]] on $\Sigma$. Once such a choice is made, the resulting [[space of quantum states]] $\mathcal{H}_\Sigma^{(J)}$ of the Chern-Simons theory over $\Sigma$ is naturally identified with the space of [[conformal blocks]] of the [[WZW model]] [[2d CFT]] on the [[Riemann surface]] $(\Sigma, J)$. 

But since, from the point of view of the 3d Chern-Simons theory, the [[polarization]] $J$ is an arbitrary choice, the [[space of quantum states]] $\mathcal{H}_\Sigma^{(J)}$ should not depend on this choice, up to specified [[equivalence]]. Formally this means that as $J$ varies (over the [[moduli space of conformal structures]] on $\Sigma$) the $\mathcal{H}_{\Sigma}^{(J)}$ should form a [[vector bundle]] on this [[moduli space of conformal structures]] which is equipped with a [[flat connection]] whose [[parallel transport]] hence provides equivalences between between the [[fibers]] $\mathcal{H}_{\Sigma}^{(J)}$ of this vector bundle. 

This flat connection is the Knizhnik-Zamolodchikov connection. This was maybe first realized and explained in ([Witten 89](#Witten89)).

## Definition

[[!include Knizhnik-Zamolodchikov-Kontsevich construction -- definition]]


## Related entries

* [[Kohno-Drinfeld theorem]]

* [[Hitchin connection]]

* [[Pochhammer loop]]


## References
 {#References}

### General

The original articles:

* {#KnizhnikZamolodchikov84} [[Vadim Knizhnik]], [[Alexander Zamolodchikov]], _Current algebra and Wess&#8211;Zumino model in two-dimensions_, Nucl. Phys. __B247__, 83&#8211;103 (1984) <a href="http://dx.doi.org/10.1016%2F0550-3213%2884%2990374-2">doi</a>, [MR87h:81129](http://www.ams.org/mathscinet-getitem?mr=87h:81129)
 

* [[Alexander Belavin]], [[Alexander Polyakov]], [[Alexander Zamolodchikov]], _Infinite conformal symmetry in two-dimensional quantum field theory_ (1984) Nucl. Phys. B 241 (2): 333&#8211;80. 

* [[Daniel Friedan]], [[Stephen Shenker]], *The analytic geometry of two-dimensional conformal field theory*, Nuclear Physics B281 (1987) ([pdf](http://www.physics.rutgers.edu/~friedan/papers/Nucl_Phys_B281_509_1987.pdf))

Textbook account, specifically for the [[su(2)|$\mathfrak{su}(2)$]]/[[sl(2)|$\mathfrak{sl}(2,\mathbb{Z})$]]-[[WZW model]]:

* [[Philippe Di Francesco]], Pierre Mathieu, David Sénéchal: §15.3.2, §15.4 in: *Conformal field theory*, Springer (1997) &lbrack;[doi:10.1007/978-1-4612-2256-9](https://doi.org/10.1007/978-1-4612-2256-9)&rbrack;


Relation to [[braid representations]]:

* {#TodorovHadjiivanov01} [[Ivan Todorov]], [[Ludmil Hadjiivanov]], *Monodromy Representations of the Braid Group*, Phys. Atom. Nucl. **64** (2001) 2059-2068; Yad.Fiz. **64** (2001) 2149-2158 &lbrack;[arXiv:hep-th/0012099](https://arxiv.org/abs/hep-th/0012099), [doi:10.1134/1.1432899](https://doi.org/10.1134/1.1432899)&rbrack;

* [[Ivan Marin]], *Sur les représentations de Krammer génériques*, Annales de l'Institut Fourier, **57** 6 (2007) 1883-1925 &lbrack;[numdam:AIF_2007__57_6_1883_0](http://www.numdam.org/item/AIF_2007__57_6_1883_0)&rbrack;

* [[Anton Alekseev]], Florian Naef, Muze Ren. *Generalized Pentagon Equations* (2024). ([arXiv:2402.19138](https://arxiv.org/abs/2402.19138)).

and understood in terms of [[anyon statistics]]:

* {#GuHaghighatLiu21} Xia Gu, [[Babak Haghighat]], Yihua Liu, *Ising- and Fibonacci-Anyons from KZ-equations*, J. High Energ. Phys. **2022** 15 (2022) &lbrack;[arXiv:2112.07195](https://arxiv.org/abs/2112.07195), <a href="https://doi.org/10.1007/JHEP09(2022)015">doi:10.1007/JHEP09(2022)015</a>&rbrack;


The generalization to higher [[genus of a surface|genus]] [[surfaces]]: 

* D. Bernard, _On the Wess-Zumino-Witten models on the torus_, Nucl. Phys. B 303 77-93 (1988)

* D. Bernard, _On the Wess-Zumino-Witten models on Riemann surfaces, Nucl. Phys. B 309 145-174 (1988)

The interpretation of this connection in terms of the [[geometric quantization]] of [[Chern-Simons theory]]/[[Wess-Zumino-Witten model]]:

* {#Witten89} [[Edward Witten]], p. 20 of: *Quantum Field Theory and the Jones Polynomial*, Commun. Math. Phys. **121** 3 (1989) 351&#8211;399. $[$[euclid.cmp/1104178138](http://projecteuclid.org/euclid.cmp/1104178138), MR0990772$]$

Review:

* [[Ivan Cherednik]], *Lectures on Knizhnik-Zamolodchikov equations and Hecke algebras*, Mathematical Society of Japan Memoirs **1998** (1998) 1-96 $[$[doi:10.2969/msjmemoirs/00101C010](https://doi.org/10.2969/msjmemoirs/00101C010)$]$

  > (in relation to [[Hecke algebras]])

* [[Toshitake Kohno]], §1.5 and §2.1 in: *Conformal field theory and topology*, transl. from the 1998 Japanese original by the author. Translations of Mathematical Monographs __210__. Iwanami Series in Modern Mathematics. Amer. Math. Soc. 2002 $[$[AMS:mmono-210](https://bookstore.ams.org/mmono-210)$]$

  > (relating to [[conformal blocks]] and [[braid representations]])


* [[Ralph Blumenhagen]], [[Erik Plauschinn]], §3.5 of: *Introduction to Conformal Field Theory -- With Applications to String Theory*, Lecture Notes in Physics **779**, Springer (2009) &lbrack;[doi:10.1007/978-3-642-00450-6](https://doi.org/10.1007/978-3-642-00450-6)&rbrack;

  > (in view of [[2d CFT]] and [[string theory]])


A quick review of the Knizhnik-Zamolodchikov equation in the context of an introduction to [[WZW model]] [[CFT]] is in  

* [[Krzysztof Gawędzki]], section 5.6 of: _Conformal field theory: a case study_ ([arXiv:hep-th/9904145](http://arxiv.org/abs/hep-th/9904145))

A review of the definition of the Knizhnik-Zamolodchikov connection on the moduli space of [[genus of a surface|genus]]=0 surfaces with $n$ marked points:

* Shu Oi, Kimio Ueno, section 2 of: _Connection Problem of Knizhnik-Zamolodchikov Equation on Moduli Space $\mathcal{M}_{0,5}$_ ([arXiv:1109.0715](http://arxiv.org/abs/1109.0715))


In relation to [[hypergeometric functions]] and [[quantum groups]] (for more see the references [below](#BraidRepresentationsViaTwisteddRCohomologyOfConfigurationSpaces)):

* [[Alexander Varchenko]], _Multidimensional hypergeometric functions and representation theory of Lie algebras and quantum groups_, Adv. Ser. in Math. Phys. __21__, World Sci. Publ. 1995. x+371 pp. ([doi:10.1142/2467](https://doi.org/10.1142/2467))

* V. Tarasov, [[Alexander Varchenko]], _Geometry of $q$-hypergeometric functions, quantum affine algebras and elliptic quantum groups_, Ast&#233;risque __246__ (1997), vi+135 pp. ([arXiv:q-alg/9703044](https://arxiv.org/abs/q-alg/9703044), [numdam:AST_1997__246__R1_0](http://www.numdam.org/item/AST_1997__246__R1_0))

On KZ-equations controlling [[codimension]]$=2$ [[defect QFT|defects]] in [[D=4 super Yang-Mills theory]]:

* [[Nikita Nekrasov]], *BPS/CFT correspondence V: BPZ and KZ equations from $q q$-characters* &lbrack;[arXiv:1711.11582](https://arxiv.org/abs/1711.11582)&rbrack;

* [[Nikita Nekrasov]], Alexander Tsymbaliuk, *Surface defects in gauge theory and KZ equation*, Letters in Mathematical Physics **112** 28 (2022) &lbrack;[arXiv:2103.12611](https://arxiv.org/abs/2103.12611), [doi:10.1007/s11005-022-01511-8](https://doi.org/10.1007/s11005-022-01511-8)&rbrack;

* Saebyeok Jeong, Norton Lee, [[Nikita Nekrasov]], *Intersecting defects in gauge theory, quantum spin chains, and Knizhnik-Zamolodchikov equations*,  J. High Energ. Phys. **2021** 120 (2021) &lbrack;[arXiv:2103.17186](https://arxiv.org/abs/2103.17186), <a href="https://doi.org/10.1007/JHEP10(2021)120">doi:10.1007/JHEP10(2021)120</a>&rbrack;




See also

* Wikipedia, *[Knizhnik-Zamolodchikov equations](http://en.wikipedia.org/wiki/Knizhnik&#8211;Zamolodchikov_equations)*


* I. B. Frenkel, N. Yu. Reshetikihin, _Quantum affine algebras and holonomic diference equations_, Comm. Math. Phys. __146__ (1992), 1-60, [MR94c:17024](http://www.ams.org/mathscinet-getitem?mr=94c:17024)

* [[Valerio Toledano-Laredo]], _Flat connections and quantum groups_, Acta Appl. Math. 73 (2002), 155-173, [math.QA/0205185](http://arxiv.org/abs/math.QA/0205185)

* [[Toshitake Kohno]], _Conformal field theory and topology_, transl. from the 1998 Japanese original by the author. Translations of Mathematical Monographs __210__. Iwanami Series in Modern Mathematics. Amer. Math. Soc. 2002 $[$[AMS:mmono-210](https://bookstore.ams.org/mmono-210)$]$

* [[P. Etingof]], N. Geer, _Monodromy of trigonometric KZ equations_, [math.QA/0611003](http://arxiv.org/abs/math.QA/0611003)

* [[Valerio Toledano-Laredo]], _A Kohno-Drinfeld theorem for quantum Weyl groups_, [math.QA/0009181](http://arxiv.org/abs/math.QA/0009181)

* A. Tsuchiya, Y. Kanie, _Vertex operators in conformal field theory on $\mathbf{P}^1$ and monodromy representations of braid group_, Adv. Stud. Pure Math. __16__, pp. 297&#8211;372 (1988); Erratum in vol. 19, 675&#8211;682

* C. Kassel, _Quantum groups_, Grad. Texts in Math. __155__, Springer 1995

* V. Chari, , A. Pressley, _A guide to quantum groups_, Camb. Univ. Press 1994&#1042;. 

* &#1040;. &#1043;&#1086;&#1083;&#1091;&#1073;&#1077;&#1074;&#1072;, &#1042;. &#1055;. &#1051;&#1077;&#1082;&#1089;&#1080;&#1085;, _&#1040;&#1083;&#1075;&#1077;&#1073;&#1088;&#1072;&#1080;&#1095;&#1077;&#1089;&#1082;&#1072;&#1103; &#1093;&#1072;&#1088;&#1072;&#1082;&#1090;&#1077;&#1088;&#1080;&#1079;&#1072;&#1094;&#1080;&#1103; &#1084;&#1086;&#1085;&#1086;&#1076;&#1088;&#1086;&#1084;&#1080;&#1080; &#1086;&#1073;&#1086;&#1073;&#1097;&#1077;&#1085;&#1085;&#1099;&#1093; &#1091;&#1088;&#1072;&#1074;&#1085;&#1077;&#1085;&#1080;&#1081; &#1050;&#1085;&#1080;&#1078;&#1085;&#1080;&#1082;&#1072;&#8211;&#1047;&#1072;&#1084;&#1086;&#1083;&#1086;&#1076;&#1095;&#1080;&#1082;&#1086;&#1074;&#1072; &#1090;&#1080;&#1087;&#1072; $B_n$_, &#1052;&#1086;&#1085;&#1086;&#1076;&#1088;&#1086;&#1084;&#1080;&#1103; &#1074; &#1079;&#1072;&#1076;&#1072;&#1095;&#1072;&#1093; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;&#1072;&#1080;&#1095;&#1077;&#1089;&#1082;&#1086;&#1081; &#1075;&#1077;&#1086;&#1084;&#1077;&#1090;&#1088;&#1080;&#1080; &#1080; &#1076;&#1080;&#1092;&#1092;&#1077;&#1088;&#1077;&#1085;&#1094;&#1080;&#1072;&#1083;&#1100;&#1085;&#1099;&#1093; &#1091;&#1088;&#1072;&#1074;&#1085;&#1077;&#1085;&#1080;&#1081;, &#1057;&#1073;&#1086;&#1088;&#1085;&#1080;&#1082; &#1089;&#1090;&#1072;&#1090;&#1077;&#1081;, &#1058;&#1088;. &#1052;&#1048;&#1040;&#1053;, 238, &#1053;&#1072;&#1091;&#1082;&#1072;, &#1052;., 2002, 124&#8211;143, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=tm&paperid=349&what=fullt&option_lang=rus); V. A. Golubeva, V. P. Leksin, "Algebraic Characterization of the Monodromy of Generalized Knizhnik&#8211;Zamolodchikov Equations of Bn Type", Proc. Steklov Inst. Math., 238 (2002), 115&#8211;133

* V. A. Golubeva, V. P. Leksin, _Rigidity theorems for multiparametric deformations of algebraic structures, associated with the Knizhnik-Zamolodchikov equations_, Journal of Dynamical and Control Systems, 13:2 (2007), 161&#8211;171, [MR2317452](http://www.ams.org/mathscinet-getitem?mr=2317452)

* V. A. Golubeva, _Integrability conditions for two&#8211;parameter Knizhnik&#8211;Zamolodchikov equations of type $B_n$ in the tensor and spinor cases_, Doklady Mathematics, 79:2 (2009), 147&#8211;149 

* V. G. Drinfel&#697;d, _Quasi-Hopf algebras and Knizhnik-Zamolodchikov equations_, Problems of modern quantum field theory (Alushta, 1989), 1&#8211;13, Res. Rep. Phys., Springer 1989.

* R. Rim&#225;nyi, V. Tarasov, A. Varchenko, P. Zinn-Justin, _Extended Joseph polynomials, quantized conformal blocks, and a $q$-Selberg type integral_, [arxiv/1110.2187](http://arxiv.org/abs/1110.2187)

* E. Mukhin, V. Tarasov, A. Varchenko, _KZ characteristic variety as the zero set of classical Calogero-Moser Hamiltonians_, [arxiv/1201.3990](http://arxiv.org/abs/1201.3990)

On the [[flat vector bundles]] underlying the KZ-equation:

* [[Ivan Marin]], *Knizhnik-Zamolodchikov bundles are topologically trivial* ([arXiv:0809.3590](https://arxiv.org/abs/0809.3590))


A 2-dimensional [[higher structure|higher]] variant ([[categorification]]) of the Knizhnik-Zamolodchikov connection via [[higher parallel transport]]:

* Lucio Simone Cirio, [[João Faria Martins]]: *Categorifying the Knizhnik–Zamolodchikov connection*, Differential Geometry and its Applications **30** 3 (2012) 238-261 \[<a href="https://doi.org/10.1016/j.difgeo.2012.03.004">doi:10.1016/j.difgeo.2012.03.004</a>, [arXiv:1106.0042](https://arxiv.org/abs/1106.0042)\]



[[!include hypergeometric KZ-solutions -- references]]






[[!redirects Knizhnik-Zamolodchikov equations]]

[[!redirects Knizhnik-Zamolodchikov form]]
[[!redirects Knizhnik-Zamolodchikov forms]]

[[!redirects Knizhnik-Zamolodchikov connection]]
[[!redirects Knizhnik-Zamolodchikov connections]]


[[!redirects KZ equation]]
[[!redirects KZ equations]]
[[!redirects KZ-equation]]
[[!redirects KZ-equations]]



[[!redirects KZ connection]]
[[!redirects KZ connections]]

[[!redirects KZ-connection]]
[[!redirects KZ-connections]]


