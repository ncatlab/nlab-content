
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

The notion of a quasibialgebra generalizes this of a 
[[bialgebra]][[Hopf algebra]] by introducing a nontrivial [[associativity]] [[coherence]] ([Drinfeld 89](#Drinfeld89)) isomorphisms (representable by multiplication with an element in triple tensor product) into axioms; a _quasi-Hopf algebra_ is a quasibialgebra with an antipode satisfying axioms which also involve nontrivial left and right unit coherences. 

In particular, quasi-Hopf algebras may be obtained from ordinary Hopf algebras by twisting by a [[Drinfeld associator]], i.e. a nonabelian [[bialgebra cocycle|bialgebra 3-cocycle]].

### Motivation from quantum field theory

Drinfel'd was motivated by study of [[monoidal categories]] in [[rational CFT|rational]] 2d [[conformal field theory]] (RCFT) as well as by an idea from [[Grothendieck]]'s _[[Esquisse d'un programme|Esquisse]]_ namely the [[Grothendieck-Teichmüller tower]] and its modular properties. In RCFT, the [[monoidal categories]] appearing can be, by [[Tannaka duality|Tannaka reconstruction]] considered as [[categories of modules]] of [[Hopf algebra]]-like objects where the flexibility of associativity coherence in building a theory were natural thus leading to quasi-Hopf algebras. 

A special case of the motivation in RCFT has a toy example of [[Dijkgraaf-Witten theory]] which can be quite geometrically
explained. Namely, where the [[groupoid convolution algebra]] of the [[delooping]] [[groupoid]] $\mathbf{B}G$ of a [[finite group]] $G$ naturally has the structure of a Hopf algebra, the [[twisted groupoid convolution algebra]] of $\mathbf{B}G$ equipped with a 3-[[cocycle]] $c \colon \mathbf{B}G \to \mathbf{B}^3 U(1)$ is naturally a quasi-Hopf algebra.
Since such a 3-cocycle is precisely the [[background gauge field]] of the 3d [[TFT]] called [[Dijkgraaf-Witten theory]], and hence quasi-Hopf algebras arise there ([Dijkgraaf-Pasquier-Roche 91](#DijkgraafPasquierRoche)).

## Definition (Drinfeld)

A __quasibialgebra__ is a unital [[associative algebra]] $(A,m,\eta)$ with a structure of not necessarily coassociative coalgebra $(A,\Delta,\epsilon)$, with multiplicative
comultiplication $\Delta$ and counit $\epsilon$, and an invertible element $\phi \in A\otimes A\otimes A$ such that 

(i) the coassociativity is modified by conjugation by $\phi$ in the sense

$$
(\Delta \otimes 1)\Delta(a) = \phi\left((1\otimes\Delta)\Delta(a)\right)\phi^{-1},\,\,\,\,\,\forall a\in A,
$$

(ii) the following pentagon identity holds 

$$
(1\otimes 1\otimes\Delta)(\phi)(\Delta\otimes 1\otimes 1)(\phi) =
(1\otimes\phi)(1\otimes\Delta\otimes 1)(\phi)(\phi\otimes 1)
$$

(iii) some identities involving unit $\eta$ and counit $\epsilon$ hold:

$$ (\epsilon\otimes A)\Delta(a) = a = (A\otimes\epsilon)\Delta(a), \,\,\,\,\,\,a\in A;$$
$$
(A\otimes\epsilon\otimes A)\phi = 1.
$$
It follows that $(\epsilon\otimes A\otimes A)\phi
 = 1 = (A\otimes A\otimes\epsilon)\phi$.

The category of left $A$-modules is a monoidal category, namely the coproduct is used to define the action of $A$ on the tensor product of modules $(M,\nu^M)$, $(N,\nu^N)$:

$$
A \otimes (M\otimes N) \stackrel{\Delta\otimes M\otimes N}\longrightarrow (A\otimes A)\otimes(M\otimes N)
\rightarrow (A\otimes M)\otimes (A\otimes N)\stackrel{\nu_M\otimes\nu_N}\longrightarrow M\otimes N
$$

Using the Sweedler-like notation $\phi = \sum \phi^1\otimes \phi^2\otimes \phi^3$, formulas

$$
\Phi_{M,N,P}: (M\otimes N)\otimes P\stackrel\cong\longrightarrow M\otimes (N\otimes P)
$$
$$
(m\otimes n)\otimes p\mapsto \sum (\phi^1\triangleright m)
\otimes ((\phi^2\triangleright n)\otimes (\phi^3\triangleright p))
$$
define a natural transformation $\Phi$ 
and the pentagon for $\phi$ yields the MacLane's pentagon for $\Phi$ understood as a new associator,
$$
(M\otimes\Phi_{N,P,Q})\Phi_{M,N\otimes P,Q}(\Phi_{M,N,P}\otimes Q)=\Phi_{M,N,P\otimes Q}\Phi_{M\otimes N,P,Q}
$$
For this reason, $\phi$ is sometimes called the associator of the quasibialgebra. While it is due Drinfeld, another variant of it, written as a formal power series and used in knot theory is often called the [[Drinfeld associator]] (see there).

A __quasi-Hopf algebra__ is a quasibialgebra $(A, \Delta, \varepsilon, \phi)$ equipped with elements $\alpha,\beta \in A$ and an antiautomorhphism $S$ of $A$ such that:
$$\sum_i S(b_i)\alpha c_i = \varepsilon (a) \alpha, \sum_i b_i\beta S(c_i) = \varepsilon(a)\beta$$
for $a \in A$ with $\Delta(a) = \sum_i b_i \otimes c_i$ in Sweedler notation. Further we require:
$$\sum_i X_i\beta S(Y_i)\alpha Z_i = 1, \quad where \sum_i X_i \otimes Y_i\otimes Z_i = \phi,$$
$$\sum_j S(P_j)\alpha Q_j\beta S(R_j) =1, \quad where \sum_j P_j \otimes Q_j \otimes R_j = \phi^{-1}.$$

### Twisting quasibialgebras by 2-cochains

The associator $\phi$ is a counital 3-cocycle in the sense of bialgebra cohomology theory of Majid. The 3-cocycle condition is the pentagon for $\phi$. The abelian cohomology would add a coboundary of 2-cochain to get a cohomologous 3-cocycle. In nonabelian case, however, the twist by an invertible 2-cochain is done in a nonabelian way, described by Drinfeld and generalized by Majid to $n$-cochains.

Thus, for a bialgebra $A$, and fixed $n$, the
$i$-th coface
$$
\partial^i  = id_{A^{\otimes (i-1)}}\otimes \Delta \otimes \id_{A^{\otimes (n-i)}} : A^{\otimes n}\to A^{\otimes (n+1)}, 
$$
for $1\leq i\leq n$, and $\partial^0 = 1\otimes id_{A^{\otimes n}}$, $\partial^n = 
id_{A^{\otimes n}}\otimes 1$. For $F\in A^{\otimes n}$, Majid defines
$$
\partial^+ F = \prod_{i\,\,\,\,even} (\partial^i F),\,\,\,\,\,\partial^- F = \prod_{i\,\,\,\,odd} (\partial^i F),
$$
where the products are in the order of ascending $i$. If $F\in A^{\otimes n}$ is a cochain then its coboundary is $\delta F = (\partial^+ F)(\partial^- F^{-1})$, which is automatically an $(n+1)$-cochain. 
If $F \in A^{\otimes n}$ is an $n$-cochain and $\phi\in A^{\otimes (n+1)}$ is an $(n+1)$-cochain then one defines a cochain twist $\phi^F$ of $\phi$ by $F$ by the formula
$$
\phi^F = (\partial^+ F)\phi(\partial^- F^{-1}).
$$
Drinfeld proved that for $n=2$ the following is true. Given a quasiabialgebra $A = (A,m,\eta,\Delta,\epsilon,\phi)$ and a 2-cochain $F$, the data
$A^F = (A,m,\eta,F\Delta(-)F^{-1},\epsilon,\phi^F)$ is also a quasibialgebra. Furthermore, categories of representations $A-mod$ and $A^F-mod$ are monoidally equivalent reflecting the idea that cohomologous cocycles lead to nonessential categorical effects. If $(A,R)$ is quasitriangular quasibialgebra then we can twist the
R-element $R\in H\otimes H$ to $R^F = F_{21} R F$ to obtain quasitriangular quasibialgebra $(A^F,R^F)$ and their braided monoidal categories of representations are braided monoidally equivalent. 

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

and some arguments about the general relevance of quasi-Hopf algebras is in

* Gerhard Mack, [[Volker Schomerus]], _Quasi Hopf quantum symmetry in quantum theory_,  Nuclear Physics B 370:1 (1992) 185--230 <a href="http://dx.doi.org/10.1016/0550-3213(92)90350-K">doi</a>

Recently a monograph appeared

* Daniel Bulacu, Stefaan Caenepeel, Florin Panaite, Freddy Van Oystaeyen, _Quasi-Hopf algebras: a categorical approach_, 544 pp., EMA 174 (2019)

Wikipedia article: [Quasi-Hopf algebra](https://en.wikipedia.org/wiki/Quasi-Hopf_algebra)

Other articles include 

* &#1042;. &#1043;. &#1044;&#1088;&#1080;&#1085;&#1092;&#1077;&#1083;&#1100;&#1076;, _&#1054; &#1089;&#1090;&#1088;&#1091;&#1082;&#1090;&#1091;&#1088;&#1077; &#1082;&#1074;&#1072;&#1079;&#1080;&#1090;&#1088;&#1077;&#1091;&#1075;&#1086;&#1083;&#1100;&#1085;&#1099;&#1093; &#1082;&#1074;&#1072;&#1079;&#1080;&#1093;&#1086;&#1087;&#1092;&#1086;&#1074;&#1099;&#1093; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;_, &#1060;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;. __26__:1 (1992), 78&#8211;80, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=768&what=fullt&option_lang=rus); transl. V. G. Drinfeld, _Structure of quasitriangular quasi-hopf algebras_, Funct. Anal. Appl., 26:1 (1992), 63&#8211;65
* V. G. Drinfel&#697;d, _&#1054; &#1082;&#1074;&#1072;&#1079;&#1080;&#1090;&#1088;&#1077;&#1091;&#1075;&#1086;&#1083;&#1100;&#1085;&#1099;&#1093; &#1082;&#1074;&#1072;&#1079;&#1080;&#1093;&#1086;&#1087;&#1092;&#1086;&#1074;&#1099;&#1093; &#1072;&#1083;&#1075;&#1077;&#1073;&#1088;&#1072;&#1093; &#1080; &#1086;&#1076;&#1085;&#1086;&#1081; &#1075;&#1088;&#1091;&#1087;&#1087;&#1077;, &#1090;&#1077;&#1089;&#1085;&#1086; &#1089;&#1074;&#1103;&#1079;&#1072;&#1085;&#1085;&#1086;&#1081; &#1089; $\mathrm{Gal}(\overline{\mathbf{Q}}/\mathbf {Q})$_, Algebra i Analiz 2 (1990), no. 4, 149--181, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=aa&paperid=199&volume=2&year=1990&issue=4&fpage=149&what=fullt&option_lang=eng); translation _On quasitriangular quasi-Hopf algebras and on a group that is closely connected with $\mathrm{Gal}(\overline{\mathbf{Q}}/\mathbf {Q})$_, Leningrad Math. J. __2__ (1991), no. 4, 829&#8211;860, [MR1080203](http://www.ams.org/mathscinet-getitem?mr=1080203)
* V. G. Drinfel&#697;d, _Quasi-Hopf algebras and Knizhnik-Zamolodchikov equations_, Problems of modern quantum field theory (Alushta, 1989), 1&#8211;13, Res. Rep. Phys., Springer 1989.

* [[Shahn Majid]], _Quantum double for quasi-Hopf algebras_, Lett. Math. Phys. __45__ (1998), no. 1, 1&#8211;9, [MR2000b:16077](http://www.ams.org/mathscinet-getitem?mr=1631648), [doi](http://dx.doi.org/10.1023/A:1007450123281), [q-alg/9701002](http://arxiv.org/abs/q-alg/9701002)
* Peter Schauenburg, _Hopf modules and the double of a quasi-Hopf algebra_, Trans. Amer. Math. Soc. __354__ (2002), 3349-3378 [pdf](http://www.ams.org/journals/tran/2002-354-08/S0002-9947-02-02980-X/S0002-9947-02-02980-X.pdf)
* M. Jimbo, H. Konno, S. Odake, J. Shiraishi, _Quasi-Hopf twistors for elliptic quantum groups_, Transformation Groups 4(4), 303–327 (1999) [doi](http://sci-hub.tw/10.1007/BF01238562)
* Ivan Kobyzev, Ilya Shapiro, _A categorical approach to cyclic cohomology of quasi-Hopf algebras and Hopf algebroids_, Applied Categorical Structures, __27__:1 (2019) 85–109 [doi](https://doi.org/10.1007/s10485-018-9544-0)
* L Frappat, D Issing, E Ragoucy, _The quantum determinant of the elliptic algebra $\mathcal{A}_{q, p}(\widehat{gl}_N)$_, J. Phys. __A51__:44, [doi](https://doi.org/10.1088/1751-8121/aae296)

[[!redirects quasibialgebra]]
[[!redirects quasihopf algebra]]
[[!redirects quasiHopf algebra]]
[[!redirects quasi-bialgebra]]
[[!redirects quasi-Hopf algebras]]