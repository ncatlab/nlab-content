+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}

## Idea 

_Twisted K-theory_ is a [[twisted cohomology]] version of ([[topological K-theory|topological]]) [[K-theory]]. 

The most famous twist is by a class in degree 3 [[ordinary cohomology]] (geometrically a $U(1)$-[[bundle gerbe]] or [[circle 2-group]]-[[principal 2-bundle]]), but there are various other twists. 


## Definition 

### By sections of associated $K U$-bundles

Write [[KU]] for the [[spectrum]] of complex [[topological K-theory]]. Its degree-0 space is, up to [[weak homotopy equivalence]],  the space 

$$
  B U \times \mathbb{Z} = {\lim_\to}_n B U(n) \times \mathbb{Z}
$$

or the space $Fred(\mathcal{H})$ of  [[Fredholm operator]]s on some separable [[Hilbert space]] $\mathcal{H}$.

$$
  (K U)_0 \simeq B U \times \mathbb{Z} \simeq Fred(\mathcal{H})
  \,.
$$

The ordinary [[topological K-theory]] of a suitable [[topological space]] $X$ is given by the set of [[homotopy classes]] of maps from (the [[suspension spectrum]] of) $X$ to $KU$:

$$
  K(X)_\bullet \simeq [X, (K U)_\bullet]
  \,.
$$

The [[projective unitary group]] $P U(\mathcal{H})$ (a [[topological group]]) acts canonically by [[automorphism]]s on $(K U)_0$. (This follows by the identification of $K U_0$ with the space of [[Fredholm operators]], see [below](#ByBundlesOfFredholmOperators)) Therefore for $P \to X$ any $PU(\mathcal{H})$-[[principal bundle]], we can form the [[associated bundle]] $P \times_{P U(\mathcal{H})} (K U)_0$.

Since the [[homotopy type]] of $P U(\mathcal{H})$ is that of an [[Eilenberg-MacLane space]] $K(\mathbb{Z},2)$, there is precisely one isomorphism class of such bundles representing a class $\alpha \in H^3(X, \mathbb{Z})$.

+-- {: .num_defn #SpectrumBundDefinition}
###### Definition

The **twisted K-theory** with twist $\alpha \in H^3(X, \mathbb{Z})$ is the set of [[homotopy]]-classes of [[section]]s of such a bundle

$$
  K_\alpha(X)^0
  \coloneqq
  \Gamma_X(P^\alpha \times_{P U(\mathcal{H})} (K U)_0)
  \,.
$$

Similarily the reduced $\alpha$-twisted K-theory is the subset

$$
  \tilde K_\alpha(X)^0
  \coloneqq
  \Gamma_X(P^\alpha \times_{P U(\mathcal{H})} B U)
  \,.
$$


=--

### By bundles of Fredholm operators
 {#ByBundlesOfFredholmOperators}

The following is due to [Atiyah & Singer 1969](#AtiyahSinger69), [Atiyah & Segal 2004](#AtiyahSegal04), in generalization of the [[Atiyah-Jänich theorem]].

Write

* $Cl_n \coloneqq Cl^{\mathbb{C}}(\mathbb{R}^n,\langle -,-\rangle)$

  for the [[complexification]] of the [[Clifford algebra]] of the [[Cartesian space]] $\mathbb{R}^n$ with its standard [[inner product]];

* $S_n$ for its $\mathbb{Z}/2\mathbb{Z}$-[[graded module|graded]] [[irreducible module]] (see at _[[spin representation]]_);

* $H_0$ for [[generalized the|the]] $\mathbb{Z}/2\mathbb{Z}$-graded [[separable Hilbert space]] whose even and odd part are both infinite-dimensional.

+-- {: .num_defn #Fredn}
###### Definition

For $n \in \mathbb{N}$, the [[topological space]] $Fred^{(n)}$ of [[Fredholm operators]] on $S_n \otimes H_0$ is the [[set]]

$$
  Fred^{(n)}
  \coloneqq
  \left\{
    F \in \mathcal{B}(S_n \otimes H_0)
    \;|\;
    F \, odd\,,
    F^\ast = F \,,
    F^2 - 1 \in \mathcal{K}(S_n \otimes H_0)\,,
    [F,\gamma] = 0 \, for\, \gamma \in Cl_n
  \right\}
$$

(where $\mathcal{B}$ denotes [[bounded operators]] and $\mathcal{K}$ denotes [[compact operators]] and where $[-,-]$ denotes the [[graded commutator]]) and the [[topological space|topology]] on this set is the [[subspace topology]] induced by the embedding

$$
  Fred^{(n)}
  \hookrightarrow
  \mathcal{B}(S_n \otimes H_0)
  \times
  \mathcal{K}(S_n \otimes H_0)
$$

given by

$$
  F\mapsto (F, F^2 - 1)
  \,,
$$

where $\mathcal{B}$ is equipped with the [[compact-open topology]] and $\mathcal{K}$ with the [[norm topology]].

=--

([Atiyah-Singer 69, p. 7](#AtiyahSinger69), [Atiyah-Segal 04, p. 21](#AtiyahSegal04), [Freed-Hopkins-Teleman 11, def. A.40](#FreedHopkinsTeleman11))

These spaces indeed form a model for the [[KU]] [[spectrum]]:

+-- {: .num_prop }
###### Proposition

For all $n \in \mathbb{N}$ there are [[natural equivalence|natural]] [[weak homotopy equivalences]]

$$
  Fred^{(n+1)} \stackrel{\simeq}{\longrightarrow} \Omega Fred^{(n)}
$$

and 

$$
  Fred^{(n+2)} \stackrel{\simeq}{\longrightarrow} Fred^{(n)}
$$

between the spaces of graded [[Fredholm operators]] of def. \ref{Fredn} and their [[loop spaces]].

=--

([Atiyah-Singer 69, theorem B(k)](#AtiyahSinger69), [Atiyah-Segal 04 (4.2)](#AtiyahSegal04), [Freed-Hopkins-Teleman 11, below def. A.40](#FreedHopkinsTeleman11))



Regard the [[stable unitary group]] $U(H_0)$ as equipped with the [[subspace topology]] induced by the inclusion

$$
  U(H_0) \stackrel{(id,(-)^{-1})}{\hookrightarrow} \mathcal{B}(H_0)\times\mathcal{B}(H_0)
$$

from the [[compact-open topology]] on the [[bounded linear operators]].

+-- {: .num_prop }
###### Proposition

The [[conjugation action]] of the [[stable unitary group]] $U(H_0)$ on $Fred^{(n)}$, def. \ref{Fredn}, is [[continuous functions|continuous]].

=--

This follows with ([Atiyah-Segal 04, prop. A1.1](#AtiyahSegal04)).


+-- {: .num_defn }
###### Definition

Given a class $\chi \in H^3(X,\mathbb{Z})$ represented by a $PU(H_0)$-bundle $P \to X$ with [[associated bundle|associated]] Fredholm bundle 

$$
  Fred^{(n)+ \chi} \coloneqq P \underset{PU(H_0)}{\times} Fred^{(n)}
  \,,
$$

then the corresponding $\chi$-twisted [[cohomology]] [[spectrum]] is that consisting of the [[spaces of sections]]

$$
  \Gamma(X, Fred^{(n)+ \chi})
  \,.
$$

=--

([Freed-Hopkins-Teleman 11, def. 3.14](#FreedHopkinsTeleman11))

### By twisted vector bundles (gerbe modules)

+-- {: .num_defn #TwBundDefinition}
###### Definition

Let $\alpha \in H^3(X, \mathbb{Z})$ be a class in degree-3 [[integral cohomology]] and let $P \in \mathbf{H}^3(X, \mathbf{B}^2 U(1))$ be any [[cocycle]] representative, which we may think of either as giving a 
[[circle n-bundle with connection|circle 2-bundle]] or a [[bundle gerbe]]. 

Write $TwBund(X, P)$ for the [[groupoid]] of [[twisted bundle]]s on $X$ with twist given by $P$. Then let

$$
  \tilde K_\alpha(X) \coloneqq TwBund(X,P)
$$

be the set of [[isomorphism]] classes of twisted bundles. Call this the **twisted K-theory** of $X$ with twist $\alpha$.
=--

> (Some technical details need to be added for the non-torsion case.)

+-- {: .num_prop}
###### Proposition

This definition of twisted $K_0$ is equivalent to that of prop. \ref{SpectrumBundDefinition}.

=--

This is ([CBMMS, prop. 6.4, prop. 7.3](#CBMMS)).

### By KK-theory of twisted convolution algebras

A [[circle 2-group]] [[principal 2-bundle]] is also incarnated as a [[centrally extended Lie groupoid]]. The corresponding [[twisted groupoid convolution algebra]] has as its [[operator K-theory]] the twisted K-theory of the base space (or base-[[stack]]). See at _[[KK-theory]]_ for more on this.

## Other constructions

Let $Vectr$ be the [[stack]] of [[vectorial bundles]]. (If we just take [[vector bundle]]s we get a notion of twisted K-theory that only allows twists that are finite order elements in their [[cohomology group]]).

There is a canonical morphism

$$
  \rho : \mathbf{B} U(1) \to Vect \hookrightarrow Vectr
$$

coming from the standard [[representation]] of the [[group]] $U(1)$.

Let $\mathbf{B}_{\otimes} Vectr$ be the [[delooping]] of $Vectr$ with respect to the [[tensor product]] [[monoidal category|monoidal structure]] (not the additive structure).

Then we have a [[fibration sequence]]

$$
  Vectr \to {*} \to \mathbf{B}_\otimes Vectr
$$

of [[(infinity,1)-category|(infinity,1)-categories]] (instead of [[infinity-groupoid]]s).

The entire morphism above deloops

$$
  \mathbf{B}\rho : \mathbf{B}^2 U(1) \to \mathbf{B}_\otimes Vect \hookrightarrow \mathbf{B}_{\otimes} Vectr
$$

being the standard representation of the [[2-group]] $\mathbf{B}U(1)$.

From the general nonsense of [[twisted cohomology]] this induces canonically now for every $\mathbf{B}^2 U(1)$-[[cohomology|cocycle]] $c$ (for instance given by a [[bundle gerbe]]) a notion of $c$-twisted $Vectr$-cohomology:

$$
 \array{
   \mathbf{H}^c(X, Vectr)
   &\to&
   {*}
   \\
   \downarrow
   &&
   \downarrow^{\mathbf{B}\rho \circ c}
   \\
   {*} &\to& \mathbf{H}(X,\mathbf{B}_\otimes Vectr)
 }
  \,.
$$

After unwrapping what this means, the result of ([Gomi](#Gomi))
shows that [[concordance]] classes in $\mathbf{H}^c(X,Vectr)$ yield twisted K-theory.

## Twists

By the general discussion of [[twisted cohomology]] the [[moduli space]] for the twists of [[periodic complex K-theory]] $KU$ is the [[Picard ∞-group]] in $KU Mod$. The "geometric" twists among these have as moduli space the non-connected delooping $bgl_1^\ast(KU)$ of the [[∞-group of units]] of $KU$.

A model for this in 4-truncation is given by [[super line 2-bundles]]. For the moment see there for further discussion and further references.



## Related concepts

* [[K-theory]]

* [[topological K-theory]], [[KR-theory]]

* **twisted K-theory**

  * [[twisted equivariant K-theory]]

    * [[twisted ad-equivariant K-theory]]

  * [[differential K-theory]]

  * [[twisted differential K-theory]]

  * [[fiber integration in K-theory]]

* [[twisted ordinary cohomology]]

* [[twisted Bredon cohomology]]

* [[twisted Cohomotopy]]


## References 

### General

The concept of twisted K-theory originates in 

* {#Karoubi68} [[Max Karoubi]], _Alg&#232;bres de Clifford et K-th&#233;orie._ Ann. Sci. Ecole Norm. Sup. (4), pp. 161-270 (1968) ([numdam:ASENS_1968_4_1_2_161_0](http://www.numdam.org/item/ASENS_1968_4_1_2_161_0))

* {#DonovanKaroubi70} [[Peter Donovan]], [[Max Karoubi]], _Graded Brauer groups and $K$-theory with local coefficients_, Publications Math&#233;matiques de l'IH&#201;S, 38 (1970), p. 5-25  ([numdam:PMIHES_1970__38__5_0](http://www.numdam.org/item?id=PMIHES_1970__38__5_0))

which discusses twists of $KO$ and $KU$ over some $X$ by elements in $H^0(X,\mathbb{Z}_2) \times H^1(X,\mathbb{Z}_2) \times H^3(X, \mathbb{Z})$.

Including the twist in degree 1 (see also at *[[PU(ℋ)]]*):

* {#Parker88} [[Ellen Maycock Parker]], around Prop. 2.2 of: *The Brauer Group of Graded Continuous Trace $C^\ast$-Algebras*, Transactions of the American Mathematical Society **308** 1 (1988) &lbrack;[jstor:2000953](https://www.jstor.org/stable/2000953)&rbrack;

reviewed in 

* [[Alan Carey]], [[Bai-Ling Wang]], p. 5 of: *Thom isomorphism and Push-forward map in twisted K-theory*, Journal of K-Theory **1** 2 (2008) 357-393  ([arXiv:math/0507414](https://arxiv.org/abs/math/0507414), [doi:10.1017/is007011015jkt011](https://doi.org/10.1017/is007011015jkt011))




The formulation in terms of sections of Fredholm bundles seems to go back to 

* {#Rosenberg89} [[Jonathan Rosenberg]], _Continuous-trace algebras from the bundle theoretic point of view_, J. Austral. Math. Soc. Ser. A 47 (1989), no. 3, 368-381 ([doi:10.1017/S1446788700033097](https://doi.org/10.1017/S1446788700033097)) 

and is expanded on in:

* {#FreedHopkinsTeleman02} [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], Diagram (2.6) in: _Twisted equivariant K-theory with complex coefficients_, Journal of Topology, Volume 1, Issue 1, 2007 ([arXiv:math/0206257](https://arxiv.org/abs/math/0206257), [doi:10.1112/jtopol/jtm001](https://doi.org/10.1112/jtopol/jtm001))

* {#AtiyahSegal04} [[Michael Atiyah]], [[Graeme Segal]], _Twisted K-theory_, Ukrainian Math. Bull. **1** 3 (2004) &lbrack;[arXiv:math/0407054](http://arxiv.org/abs/math/0407054), [journal page](http://iamm.su/en/journals/j879/?VID=10), [published pdf](http://iamm.su/upload/iblock/45e/t1-n3-287-330.pdf)&rbrack;
  > (beware of the false claim in [AS04 p 39](#AtiyahSegal04) that [[U(H)|$U(\mathcal{H})$]] in the [[compact open topology]] is not a [[topological group]], corrected by [Schottenloher 2013](UH#Schottenloher13), [Espinoza & Uribe 2014](UH#EspinozaUribe14), going back to [Schottenloher 1995](UH#Schottenloher95))

* [[Peter May]], [[Johann Sigurdsson]], Section 22.3 of: _[[Parametrized Homotopy Theory]]_,  Mathematical Surveys and Monographs, vol. 132, AMS 2006 ([ISBN:978-0-8218-3922-5](https://bookstore.ams.org/surv-132), [arXiv:math/0411656](https://arxiv.org/abs/math/0411656), [pdf](http://www.math.uchicago.edu/~may/EXTHEORY/MaySig.pdf))

* {#AtiyahSegal05} [[Michael Atiyah]], [[Graeme Segal]], _Twisted K-theory and cohomology_ ([arXiv:math/0510674](http://arxiv.org/abs/math/0510674))

* {#AndoBlumbergGepner10} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], sections 2.1 and 7 of: _Twists of K-theory and TMF_, in [[Jonathan Rosenberg]] et al. (eds.), _Superstrings, Geometry, Topology, and $C^\ast$-algebras_, volume 81 of _Proceedings of Symposia in Pure Mathematics_, 2009 ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004), [doi:10.1090/pspum/081](https://doi.org/10.1090/pspum/081))



A comprehensive account of twisted K-theory with twists in $H^3(X, \mathbb{Z})$ is in:

* {#AtiyahSinger69} [[Michael Atiyah]], [[Isadore Singer]]: *Index theory for skew-adjoint Fredholm operators*,  Publications Mathématiques de l’Institut des Hautes Scientifiques **37** 1 (1969) 5-26 &lbrack;[doi:10.1007/BF02684885](https://doi.org/10.1007/BF02684885), [pdf](http://www.maths.ed.ac.uk/~aar/papers/askew.pdf)&rbrack;


and for more general twists in 


* {#FreedHopkinsTeleman11} [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]]: *[[Loop Groups and Twisted K-Theory]] I*, J. Topology **4** (2011) 737-789  &lbrack;[arXiv:0711.1906](http://arxiv.org/abs/0711.1906), [doi:10.1112/jtopol/jtr019](https://doi.org/10.1112/jtopol/jtr019)&rbrack;



See also:

* [[Max Karoubi]], _Twisted bundles and twisted K-theory_, in:  Guillermo Cortiñas (ed.) _Topics in Noncommutative Geometry_ ([arXiv:1012.2512](https://arxiv.org/abs/1012.2512), [ISBN:978-0-8218-6864-5](https://bookstore.ams.org/cmip-16))

Textbook accounts:

* [[Dale Husemöller]], [[Michael Joachim]], [[Branislav Jurčo]], [[Martin  Schottenloher]], Part IV of: _[[Basic Bundle Theory and K-Cohomology Invariants]]_, Springer Lecture Notes in Physics __726__, 2008, ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726.pdf), [doi:10.1007/978-3-540-74956-1](https://link.springer.com/book/10.1007/978-3-540-74956-1))

Discussion of [[twisted ad-equivariant K-theory]] and relation to [[loop group]] [[representations]] and the [[Verlinde ring]], now again with twists in $H^0(X,\mathbb{Z}_2) \times H^1(X,\mathbb{Z}_2) \times H^3(X, \mathbb{Z})$, is in the series of articles

* [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], _Twisted K-theory and loop group representations_ [arXiv:math/0312155](http://arxiv.org/abs/math/0312155);  _[[Loop Groups and Twisted K-Theory]] I_ ([arXiv:0711.1906](http://arxiv.org/abs/0711.1906)) {#FHT07}; _[[Loop Groups and Twisted K-Theory]] II_ ([arXiv:math/0511232](http://arxiv.org/abs/math/0511232))

The result on twisted K-groups has been lifted to an equivalence of categories in

* [[Daniel Freed]], [[Constantin Teleman]], _Dirac families for loop groups as matrix factorizations_, [arxiv/1409.6051](http://arxiv.org/abs/1409.6051)

Discussion in terms of [[Karoubi K-theory]]/[[Clifford module bundles]] is in 

* [[Max Karoubi]], _Clifford modules and twisted K-theory_, Proceedings of the International Conference on Clifford algebras (ICCA7) ([arXiv:0801.2794](http://arxiv.org/abs/0801.2794))


 

See the references at _[[(infinity,1)-vector bundle]]_ for more on this.

Discussion in terms of [[twisted bundles]]/[[bundle gerbe modules]] is in 

* {#CBMMS}  [[Peter Bouwknegt]], [[Alan Carey]], [[Varghese Mathai]], [[Michael Murray]], [[Danny Stevenson]], _Twisted K-theory and K-theory of bundle gerbes_,  Commun Math Phys, 228 (2002) 17-49 ([arXiv:hep-th/0106194](http://arxiv.org/abs/hep-th/0106194), [doi:10.1007/s002200200646](https://doi.org/10.1007/s002200200646))
  
but apparently contains a mistake, as pointed out in 

* [[Alan Carey]], [[Bai-Ling Wang]], top of p. 10 in _Thom isomorphism and Push-forward map in twisted K-theory_, Journal of K-Theory **1** 2 (2008) 357-393 ([arXiv:math/0507414](https://arxiv.org/abs/math/0507414), [doi:10.1017/is007011015jkt011](https://doi.org/10.1017/is007011015jkt011))

The generalization of this to [[groupoid K-theory]] is in ([FHT 07, around p. 26](#FHT07)) and 

* {#TuXuLG03} [[Jean-Louis Tu]], [[Ping Xu]], [[Camille Laurent-Gengoux]], _Twisted K-theory of differentiable stacks_ ([arXiv:math/0306138](http://arxiv.org/abs/math/0306138))
 

(which establishes the relation to [[KK-theory]]).

* {#Karoubi} [[Max Karoubi]], _Twisted bundles and twisted K-theory_, [arxiv/1012.2512](http://arxiv.org/abs/1012.2512) 
 

* {#Pennig} [[Ulrich Pennig]], _Twisted K-theory with coefficients in $C^\ast$-algebras_, ([arXiv:1103.4096](http://arxiv.org/abs/1103.4096))
 
Comparison between [[homotopy theory|homotopy theoretic]] and [[operator algebra|operator algebraic]] constructions:

* {#HebestreitSagave19} [[Fabian Hebestreit]], [[Steffen Sagave]], *Homotopical and operator algebraic twisted K-theory*, Mathematische Annalen **378** (2020) 1021-1059 ([arXiv:1904.01872](https://arxiv.org/abs/1904.01872), [doi:10.1007/s00208-020-02066-6](https://doi.org/10.1007/s00208-020-02066-6))




Discussion in terms of [[vectorial bundles]] is in

* {#Gomi} [[Kiyonori Gomi]], _Twisted K-theory and finite-dimensional approximation_ ([arXiv:0803.2327](http://arxiv.org/abs/0803.2327))
 
* {#GomiTerashima} [[Kiyonori Gomi]], [[Yuji Terashima]], _Chern-Weil Construction for Twisted K-Theory_, Communication ins Mathematical Physics, Volume 299, Number 1, 225-254 ([doi:10.1007/s00220-010-1080-1](https://doi.org/10.1007/s00220-010-1080-1))
 
Discussion of combined [[twisted K-theory|twisted]] [[equivariant K-theory|equivariant]] [[KR-theory]] on [[orbifold|orbi-]] [[orientifolds]]:

* [[El-kaïoum M. Moutuou]], _Twistings of KR for Real groupoids_ ([arXiv:1110.6836](http://arxiv.org/abs/1110.6836))

* [[El-kaïoum M. Moutuou]], _Graded Brauer groups of a groupoid with involution_, J. Funct. Anal. 266 (2014), no.5 ([arXiv:1202.2057](https://arxiv.org/abs/1202.2057))

* {#Freed12} [[Daniel Freed]], _Lectures on twisted K-theory and orientifolds_, lectures at ESI Vienna, 2012 ([[FreedESI2012.pdf:file]])

* [[Daniel Freed]], [[Gregory Moore]], Section 7 of: _Twisted equivariant matter_,  Ann. Henri Poincaré (2013) 14: 1927 ([arXiv:1208.5055](https://arxiv.org/abs/1208.5055))

* {#Gomi17} [[Kiyonori Gomi]], _Freed-Moore K-theory_ ([arXiv:1705.09134](https://arxiv.org/abs/1705.09134), [spire:1601772](http://inspirehep.net/record/1601772))

Review:

* [[Jonathan Rosenberg]], *Twisted cohomology*, in *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2401.03966](https://arxiv.org/abs/2401.03966)&rbrack;


Discussion of twisted [[K-homology]]:

* [[Bai-Ling Wang]], _Gemometric cycles, index theory and twisted K-homology_ ([arXiv:0710.1625](https://arxiv.org/abs/0710.1625))

* [[Eckhard Meinrenken]], _Twisted K-homology and group-valued moment maps_,  International Mathematics Research Notices 2012 (20) (2012), 4563--4618 ([arXiv:1008.1261](https://arxiv.org/abs/1008.1261))

* Bei Liu, _Twisted K-homology,Geometric cycles and T-duality_ ([arXiv:1411.1575](https://arxiv.org/abs/1411.1575))

Discussion of combined [[twisted K-theory|twisted]] and [[equivariant K-theory|equivariant]] and [[real K-theory|real]] K-theory

* {#Gomi17} [[Kiyonori Gomi]], _Freed-Moore K-theory_ ([arXiv:1705.09134](https://arxiv.org/abs/1705.09134))


Discussion of [[twisted K-theory|twisted]] [[differential K-theory|differential]] [[topological K-theory|K-theory]] and its relation to [[D-brane charge]] in [[type II string theory]] (see at *[[K-theory classification of D-brane charge]]*):

* {#GradySati19a} [[Daniel Grady]], [[Hisham Sati]], _Ramond-Ramond fields and twisted differential K-theory_ ([arXiv:1903.08843](https://arxiv.org/abs/1903.08843))

Discussion of [[twisted K-theory|twisted]] [[differential K-theory|differential]] [[KO-theory|orthogonal]] [[topological K-theory|K-theory]] and its relation to [[D-brane charge]] in [[type I string theory]] (on [[orientifolds]]):

* {#GradySati19b} [[Daniel Grady]], [[Hisham Sati]], _Twisted differential KO-theory_ ([arXiv:1905.09085](https://arxiv.org/abs/1905.09085))


### Higher twists
 {#ReferencesHigherTwists}

Discussion of higher twists of K-theory (above degree 3):

* [[Ib Madsen]], [[Victor Snaith]], [[Jørgen Tornehave]], *Infinite loop maps in geometric topology*, Mathematical Proceedings of the Cambridge Philosophical Society, Volume 81, Issue 3, (1977)([doi:10.1017/S0305004100053482](https://doi.org/10.1017/S0305004100053482))

* [[Constantin Teleman]], Section 3 of: *K-theory of the moduli of bundles over a Riemann surface and deformations of the Verlinde algebra* ([arXiv:math/0306347](https://arxiv.org/abs/math/0306347)), in [[Ulrike Tillmann]] (ed.) *Topology, Geometry and Quantum Field Theory*, Cambridge University Press 2004 ([doi:10.1017/CBO9780511526398](https://doi.org/10.1017/CBO9780511526398))

Via [[C-star algebras|$C^\ast$-algebras]]:

* {#Pennig16} [[Ulrich Pennig]], *A noncommutative model for higher twisted K-Theory*, J Topology (2016) 9 (1): 27-50 ([arXiv:1502.02807](https://arxiv.org/abs/1502.02807))

* {#DardalatPennig16} [[Marius Dadarlat]], [[Ulrich Pennig]], *A Dixmier-Douady theory for strongly self-absorbing $C^\ast$-algebras*, J. Reine Angew. Math. 718 (2016) 153-181 ([arXiv:1302.4468](https://arxiv.org/abs/1302.4468), [doi:10.1515/crelle-2014-0044](https://doi.org/10.1515/crelle-2014-0044))

* {#DardalatPennig15} [[Marius Dadarlat]], [[Ulrich Pennig]], *Unit spectra of K-theory from strongly self-absorbing $C^\ast$-algebras*, Algebr. Geom. Topol. 15 (2015) 137-168 &lbrack;[arXiv:1306.2583](https://arxiv.org/abs/1306.2583), [doi:10.2140/agt.2015.15.137](http://dx.doi.org/10.2140/agt.2015.15.137)&rbrack;

* [[David Brook]], *Computations in higher twisted K-theory*  ([arXiv:2007.08964A](https://arxiv.org/abs/2007.08964A))

* [[David Brook]], *Higher twisted K-theory* ([dspace:2440/125740](https://digital.library.adelaide.edu.au/dspace/handle/2440/125740))

* [[David E. Evans]], [[Ulrich Pennig]], *Spectral Sequence Computation of Higher Twisted K-Groups of $SU(n)$* &lbrack;[arXiv:2307.00423](https://arxiv.org/abs/2307.00423)&rbrack;

see also:

* [[Ulrich Pennig]], *Equivariant Higher Twisted K-Theory of $SU(n)$ via Exponential Functors*, [talk at](CQTS#PennigSep2023) [[CQTS]] (20 Sep 2023) &lbrack;video:[YT](https://youtu.be/JXO-owcJgTE)&rbrack;

Discussion of the [[twisted Chern character]] for higher twisted K-theory:

* Lachlan Macdonald, [[Varghese Mathai]], Hemanth Saratchandran, *On the Chern character in Higher Twisted K-theory and spherical T-duality*, Commun. Math. Phys. 385, 331-368 (2021) ([arXiv:2007.02507](https://arxiv.org/abs/2007.02507))



[[!redirects twisted K-theories]]

[[!redirects twisted topological K-theory]]
[[!redirects twisted topological K-theories]]

[[!redirects higher twisted K-theory]]
[[!redirects higher twisted K-theories]]

