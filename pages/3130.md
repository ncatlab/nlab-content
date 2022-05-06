+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Traditionally, in the strict sense of the term, the _Chern character_ is a [[universal characteristic class]] of [[vector bundles]] or equivalently of their [[topological K-theory]] classes, which is a [[rational number|rational]] combination of all [[Chern classes]].

This is a special case of the following more general construction ([[Quadratic Functions in Geometry, Topology,and M-Theory|Hopkins-Singer 02, section 4.8]]):

for $E$ a [[spectrum]] [[Brown representability theorem|representing]] a [[generalized (Eilenberg-Steenrod) cohomology theory]] there is a canonical [[localization of spectra|localization]] map

$$
  ch_E \;\colon\; E \longrightarrow E \wedge H\mathbb{R}
$$

to the [[smash product]] with the [[Eilenberg-MacLane spectrum]] over the [[real numbers]]. This represents the $E$-Chern character (see also [Bunke-Gepner 13, around def. 2.1](#BunkeGepner13)).

In the case that $E = $ [[KU]] this reproduces the traditional Chern character. (In which case this is a map from a [[complex oriented cohomology theory]] of [[chromatic level]] 1 to chromatic level 0. More generally one can also consider [[higher chromatic Chern characters]] that take values not in [[ordinary cohomology]] but in some cohomology theory of higher [[chromatic level]]. See at _[[higher chromatic Chern character]]_ for more on this.)

The Chern character $ch_E$ may be used to define [[differential cohomology]] refinements $\hat E$ of the [[cohomology theory]] $E$ by choosing a [[differential form]]-model for $E \wedge H\mathbb{R}$ ([Hopkins-Singer 02](#HopkinsSinger02), see also at _[[differential function complex]]_). In that case $ch_E$ is the [[real cohomology]] class associated to a _chern character differential form_ $CH_E$ via the [[de Rham theorem]]. Here $CH_E$ has the interpretation of being the [[curvature forms]] of the [[differential cohomology]] [[cocycles]] thought of as [[connection on a principal ∞-bundle|∞-connections]].

This may be turned around ([Bunke-Nikolaus-V&#246;lkl 13, prop. .3.5](#BunkeNikolausVoelkl13)): given any refinement $\hat E$ of $E$ in a [[tangent cohesive (∞,1)-topos]] $T \mathbf{H}$, then it is induced from homotopy pullback of its [de Rham coefficients](cohesive+%28infinity%2C1%29-topos+--+structures#deRhamCohomology) along a Chern character map 

$$
  ch_E = \Pi \theta_{\hat E} \;\colon\; E \simeq \Pi(\hat E) \longrightarrow \Pi \flat_{dR} \hat E
  \,,
$$

where $\Pi$ is the [[shape modality]] and $\theta_E$ the [[Maurer-Cartan form]] of $E$. This reproduces the above definition for ordinary differential form models, see at _[differential cohomology diagram -- Hopkins-Singer coefficients](#differential+cohomology+diagram#HopkinsSingerCoefficients)_. 

But more generally, given for instance a [[K(n)-local spectrum|K(n)-localization]] $E \longrightarrow L_{K(n)} E$ then any choice of [[cohesion|cohesive]] refinement of $L_{K(n)} E$ (i.e. lift through the [[unit of a monad|unit]] of the [[shape modality]] $\Pi$) which is in the kernel of $\flat$ yields a generalized differential cohomology theory $\hat E$ whose intrinsic Chern-character $\Pi \theta_{\hat E}$ is the $K(n)$-localization. See at _[differential cohomology diagram -- Chern character and differential fracture](differential+cohomology+diagram#ChernCharacterAndFractureSquares)_.

In words this is summarized succintly as: _The Chern character is the [[shape modality|shape]] of the [[Maurer-Cartan form]]._

In the context of [[algebraic K-theory]] Chern characters appear at _[[Beilinson regulators]]_.
There are analogues in algebraic geometry (e.g. a Chern character between [[Chow groups]] and [[algebraic K-theory]]) and in [[noncommutative geometry]] (Chern-Connes character) where the role of usual cohomology is taken by some variant of cyclic cohomology.  

## Examples

### For vector bundles and topological K-theory 
 {#KTheory}

The classical theory of the Chern character applies to the [[spectrum]] of complex [[K-theory]], $E = KU$. In this case, the Chern character is made up from Chern classes: each characteristic class is by Chern-Weil theory in  the image of a certain element in the Weil algebra via taking the class of evaluation at the [[curvature]] operator for some choice of a connection. Consider the symmetric functions in $n$ variables $t_1,\ldots, t_n$ and let the Chern classes of a complex vector bundle $\xi$ (representing a complex K-theory class) be $c_1,\ldots, c_n$. Define the formal power series 

$$
\phi = \phi^n(t_1,\ldots, t_n) = e^{t_1}+\ldots+e^{t_n}= \sum_{k=0}^\infty \frac{1}{k!} (t_1^k+\ldots+t_n^k)
$$

Then $ch(\chi) = \phi(c_1,\ldots,c_n)$. 

Let us describe this a bit differently. The cocycle $H^0(X,KU)$ may be represented by a complex [[vector bundle]], and the image of this cocycle under the Chern-character is the class in even-graded real cohomology that is represented (under the [[deRham theorem]] isomorphism of deRham cohomology with real cohomology) by the even graded closed [[differential form]]


$$
 ch(\nabla) \coloeqq \sum_{j \in \mathbb{N}}
   k_j
   tr( F_\nabla \wedge \cdots \wedge F_\nabla)
  \;\;
  \in \Omega^{2 \bullet}(X)
  \,,
$$

where

* $\nabla$ is any chosen [[connection on a bundle|connection]] on the vector bundle;

* $F = F_\nabla \in \Omega^2(X,End(V))$ is the [[curvature]] of this connection;

* $k_j \in \mathbb{R}$ are normalization constants, $k_j = \frac{1}{j!} \left( \frac{1}{2\pi i}\right)^j$;

* the trace of the wedge products produces the [[curvature characteristic form]]s.

The Chern character applied to the [[Whitney sum]] of two vector bundles is a sum of the Chern characters for the two: $ch(\xi\oplus \eta) = ch(\chi)+ch(\eta)$ and it is multiplicative under the tensor product of vector bundles: $ch(\xi\otimes\eta)=ch(\chi)ch(\eta)$. Therefore we get a ring homomorphism. 


### For spectra and generalized cohomology theories
 {#ForSpectraAndGeneralizedCohomology}

For $E$ a [[spectrum]] and $E^\bullet$ the [[generalized (Eilenberg-Steenrod) cohomology theory|generalized cohomology theory]] it [[Brown representability theorem|represents]]

$$
  E^\bullet(X) \;\simeq\; \pi_{-\bullet} Maps(X,E)
$$

the _[[Chern-Dold character]] for $E$_ ([Buchstaber 70](#Buchstaber70)) is the map induced by [[rationalization]] over the [[real numbers]]

$$
  E \overset{L_{\mathbb{R}}}{\longrightarrow} E_{\mathbb{R}}
$$

i.e. is

\[
  \label{ChernDoldCharacter}
  chd
  \;\colon\;
  E^\bullet(X)
  \;\simeq\;
  \pi_{-\bullet}Maps(X,E)
  \overset{
    \pi_{-\bullet}Maps(X,L_{\mathbb{R}})
  }{\longrightarrow}
  \pi_{-\bullet}Maps(X,E_{\mathbb{R}})
  \;\simeq\;
  E^\bullet_{\mathbb{E}}(X)
  \;\simeq\;
  H^\bullet(X, \pi_{\bullet}(E)\otimes_{\mathbb{Z}}\mathbb{R})
  \,.
\]

The very last equivalence in (eq:ChernDoldCharacter) is due to [Dold 56, Cor. 4](#Dold56) (reviewed in detail in [Rudyak 98, II.3.17](#Rudyak98), see also  [Gross 19, Def. 2.5](#Gross19)).

One place where this neat state of affairs (eq:ChernDoldCharacter) is made fully explicit is [Lind-Sati-Westerland 16, Def. 2.1](#LindSatiWesterland16). Many other references leave this statement somewhat in between the lines (e.g. [Buchstaber 70](#Buchstaber70), [Upmeier 14](#Upmeier14)) and, in addition, often without reference to Dold (e.g. [Hopkins-Singer 02, Sec. 4.8](#HopkinsSinger02), [Bunke 12, Def. 4.45](#Bunke12), [Bunke-Gepner 13, Def. 2.1](#BunkeGepner13), [Bunke-Nikolaus 14, p. 17](#BunkeNikolaus14)).

Beware that some authors say _Chern-Dold character_ for the full map in (eq:ChernDoldCharacter) (e.g. 
[Buchstaber 70](#Buchstaber70), 
[Upmeier 14](#Upmeier14), [Lind-Sati-Westerland 16, Def. 2.1](#LindSatiWesterland16)), while other authors mean by this only that last equivalence in (eq:ChernDoldCharacter) (e.g. [Rudyak 98, II.3.17](#Rudyak98), [Gross 19, Def. 2.5](#Gross19)).

Examples of Chern-Dold characters: 

* [[Chern character]] on [[KU]];

* [[Pontrjagin character]] on [[KO]].

### For cohesive stable homotopy types

More generally, for $\hat E$ a [[stable homotopy type]] in a [[cohesive (∞,1)-topos]], then the underlying bare homotopy type is $E \coloneqq \Pi(\hat E)$ and the corresponding Chern character is

$$
  ch \coloneqq \Pi \theta_{\hat E} \;\colon\; E \simeq \Pi(\hat E) \longrightarrow \Pi \flat_{dR} \hat E
  \,.
$$

For more on this see at _[[differential cohomology diagram]]_.

### In terms of cyclic homology

Generalizing in another direction, generalized Chern characters are given by passage to [[derived loop spaces]] and their [[cyclic homology]] or, more generally,  [[topological cyclic homology]] ([Toen-Vezzosi 08](#ToenVezzosi08), [Hoyois-Scherotzke-Sibilla 15](#HoyoisScherotzkeSibilla15)).

## Properties

### Push-forward and Grothendieck-Riemann-Roch theorem

The behaviour of the Chern-character under [[fiber integration in generalized cohomology]] along [[proper maps]] is described by the [[Grothendieck-Riemann-Roch theorem]].

## Related concepts

* [[odd Chern character]]

* [[twisted Chern character]]

* [[equivariant Chern character]]

* for [[algebraic K-theory]]:

  * [[cyclotomic trace]]

  * [[regulator]], [[Beilinson regulator]]

* [[Grothendieck-Riemann-Roch theorem]]

* [[higher chromatic Chern character]]

  * [[elliptic Chern character]]

  * [[Morava E-theoretic Chern character]]

* [[transchromatic character]]

* [[group character]]



## References

### Chern character on K-theory

Original Discussion of the Chern character on complex [[topological K-theory]]:

* {#Hirzebruch56} [[Friedrich Hirzebruch]], Section 12.1 of: _Neue topologische Methoden in der Algebraischen Geometrie_, Ergebnisse der Mathematik und Ihrer Grenzgebiete. 1. Folge, Springer 1956 ([doi:10.1007/978-3-662-41083-7](https://www.springer.com/de/book/9783662406052))

* {#BorelHirzebruch58} [[Armand Borel]], [[Friedrich Hirzebruch]], Section 9.1 in: _Characteristic Classes and Homogeneous Spaces, I_, American Journal of Mathematics Vol. 80, No. 2 (Apr., 1958), pp. 458-538 ([jstor:2372795](https://www.jstor.org/stable/2372795))

* {#AtiyahHirzebruch61} [[M. F. Atiyah]], [[F. Hirzebruch]], Section 1.10 in: _Vector bundles and homogeneous spaces_, 1961, Proc. Sympos. Pure Math., Vol. III pp. 7&#8211;38 American Mathematical Society, Providence, R.I. ([web](http://hirzebruch.mpim-bonn.mpg.de/87/), <a href="https://doi.org/10.1142/9789814401319_0008">doi:10.1142/9789814401319_0008</a>, [MR 0139181](http://www.ams.org/mathscinet-getitem?mr=0139181))

* {#Hilton71} [[Peter Hilton]], _General cohomology theory and K-theory_, London Mathematical Society Lecture Note Series 1, Cambridge University Press (1971) ([doi:10.1017/CBO9780511662577](https://doi.org/10.1017/CBO9780511662577))


Further discussion 

* Helge Maakestad, _Notes on the Chern-character_ ([arXiv:math/0612060](https://arxiv.org/abs/math/0612060))

* [[Goncalo Tabuada]], _A universal characterization of the Chern character maps_ ([arXiv/1002.3276](http://arxiv.org/abs/1002.3726))

Discussion of the [[equivariant Chern character]] in [[equivariant K-theory]]:

* {#Stefanich} German Stefanich, _Chern Character in Twisted and Equivariant K-Theory_ ([pdf](https://math.berkeley.edu/~germans/Chern2.pdf))




### Chern-Dold character on generalized cohomology

The identification of rational [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology]] as [[ordinary cohomology]] with [[coefficients]] in the rationalized [[stable homotopy groups]] is due to

* {#Dold56} [[Albrecht Dold]], _Relations between ordinary and extraordinary homology_, Matematika, 9:2 (1965), 8–14; Colloq. algebr. Topology, Aarhus Universitet, 1962, 2–9 ([mathnet:mat350](http://mi.mathnet.ru/eng/mat350)), reprinted in: J. Adams & G. Shepherd (Authors), _Algebraic Topology: A Student's Guide_ (London Mathematical Society Lecture Note Series, pp. 166-177). Cambridge: Cambridge University Press 1972 ([doi:10.1017/CBO9780511662584.015](https://doi.org/10.1017/CBO9780511662584.015)) 

reviewed in

* [Hilton 71, Theorem 3.18](#Hilton71)

* {#Rudyak98} [[Yuli Rudyak]], II.7.13 in: _On Thom Spectra, Orientability, and Cobordism_, Springer 1998 ([doi:10.1007/978-3-540-77751-9](https://doi.org/10.1007/978-3-540-77751-9))


* {#Gross19} Jacob Gross, _The homology of moduli stacks of complexes_ ([arXiv:1907.03269](https://arxiv.org/abs/1907.03269))


The combination of [Dold 56](#Dold56) to the Chern-Dold character on [[generalized (Eilenberg-Steenrod) cohomology theory]] is due (for [[complex cobordism cohomology]]) to

* {#Buchstaber70} [[Victor Buchstaber]], _The Chern–Dold character in cobordisms. I_, 

  Russian original: Mat. Sb. (N.S.), 1970 Volume 83(125), Number 4(12), Pages 575–595 ([mathnet:3530](http://m.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=sm&paperid=3530&option_lang=eng))

  English translation: Mathematics of the USSR-Sbornik, Volume 12, Number 4, AMS 1970 ([doi:10.1070/SM1970v012n04ABEH000939](https://iopscience.iop.org/article/10.1070/SM1970v012n04ABEH000939))

Review in 

* [Hilton 71, p. 50](#Hilton71)

That the Chern-Dold character reduces to the original Chern character on K-theory is

* [Hilton 71, Theorem 5.8](#Hilton71).


That the Chern-Dold character is given by rationalization of representing spectra is made fully explicit in 

* {#LindSatiWesterland16} [[John Lind]], [[Hisham Sati]], [[Craig Westerland]], Section 2.1: _Twisted iterated algebraic K-theory and topological T-duality for sphere bundles_, Ann. K-Th. 5 (2020) 1-42 ([arXiv:1601.06285](https://arxiv.org/abs/1601.06285))

This rationalization construction appears also (without attribution to [#Hilton 71](#Hilton71) or [Buchstaber 70](#Buchstaber70) or [Dold 56](#Dold56)) in the following articles (all in the context of [[differential cohomology]]):

* {#HopkinsSinger02} [[Mike Hopkins]], [[Isadore Singer]], Section [4.8, page 47](http://arxiv.org/PS_cache/math/pdf/0211/0211216v2.pdf#page=47) of _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_, ([math.AT/0211216](http://arxiv.org/abs/math.AT/0211216)).

* {#Bunke12} [[Ulrich Bunke]], _Differential cohomology_ ([arXiv:1208.3961](http://arxiv.org/abs/1208.3961))

* {#BunkeGepner13} [[Ulrich Bunke]], [[David Gepner]], around def. 2.1 of: _Differential function spectra, the differential Becker-Gottlieb transfer, and applications to differential algebraic K-theory_ ([arXiv:1306.0247](http://arxiv.org/abs/1306.0247))

* {#Upmeier14} Markus Upmeier, _Refinements of the Chern-Dold Character: Cocycle Additions in Differential Cohomology_,  J. Homotopy Relat. Struct. 11, 291–307 (2016). ([arXiv:1404.2027](https://arxiv.org/abs/1404.2027), [doi:10.1007/s40062-015-0106-y](https://doi.org/10.1007/s40062-015-0106-y))

* {#BunkeNikolaus14} [[Ulrich Bunke]], [[Thomas Nikolaus]], _Twisted differential cohomology_, Algebr. Geom. Topol. Volume 19, Number 4 (2019), 1631-1710. ([arXiv:1406.3231](http://arxiv.org/abs/1406.3231), [euclid:euclid.agt/1566439272](https://projecteuclid.org/euclid.agt/1566439272))

More on the Chern-Dold character on [[complex cobordism cohomology]]:

* [[Victor Buchstaber]], A. P. Veselov, _Chern-Dold character in complex cobordisms and abelian varieties_ ([arXiv:2007.05782](https://arxiv.org/abs/2007.05782))

The observation putting this into the general context of [[differential cohomology diagrams]] (see there) of [[stable homotopy types]] in [[cohesion]] is due to

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], section 4.4. of _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

based on [Bunke-Gepner 13](#BunkeGepner13).


The Chern-Dold character in [[equivariant cohomology]]:

* [[Wolfgang Lück]], _Chern characters for proper equivariant homology theories and applications to K- and L-theory_, Journal für die reine und angewandte Mathematik, Volume 2002: Issue 543 ([doi:10.1515/crll.2002.015](https://doi.org/10.1515/crll.2002.015), [pdf](https://www.him.uni-bonn.de/lueck/data/eh.pdf))

* [[Wolfgang Lück]], _Equivariant Chern characters_, 2006 ([pdf](https://www.him.uni-bonn.de/lueck/data/goettingen_equi_Chern061130trans.pdf), [[LuckEquivariantChernCharacters.pdf:file]])




### In derived algebraic geometry

Discussion of Chern characters in terms of [[free loop space objects]] in [[derived geometry]]:

* {#ToenVezzosi08} [[Bertrand Toën]], [[Gabriele Vezzosi]], _A note on Chern character, loop spaces and derived algebraic geometry_ ([arXiv:0804.1274](http://arxiv.org/abs/0804.1274))

which conjectures a construction that is fully developed in 

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Caract&#232;res de Chern, traces &#233;quivariantes et g&#233;om&#233;trie alg&#233;brique d&#233;riv&#233;e_ ([arXiv:0903.3292](http://arxiv.org/abs/0903.3292))

See also

* [[Marc Hoyois]], _Chern character and derived algebraic geometry_ (2009) ([pdf](http://math.mit.edu/~hoyois/papers/chern.pdf))

* {#HoyoisScherotzkeSibilla15} [[Marc Hoyois]], [[Sarah Scherotzke]], [[Nicolò Sibilla]], _Higher traces, noncommutative motives, and the categorified Chern character_ ([arXiv:1511.03589](http://arxiv.org/abs/1511.03589))



[[!redirects Chern characters]]

[[!redirects Chern character map]]
[[!redirects Chern character maps]]

[[!redirects Chern-Dold character]]
[[!redirects Chern-Dold characters]]

[[!redirects Chern-Dold character map]]
[[!redirects Chern-Dold character maps]]


[[!redirects Dold-Chern character]]
[[!redirects Dold-Chern characters]]

[[!redirects Dold-Chern character map]]
[[!redirects Dold-Chern character maps]]

