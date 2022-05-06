

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An abstractly defined $n$-dimensional [[quantum field theory]] is a consistent assignment of [[state]]-space and correlators to $n$-dimensional [[cobordism]]s with certain structure (topological structure, conformal structure, Riemannian structure, etc. see [[FQFT]]/[[AQFT]]). In an _open-closed QFT_ the cobordisms are allowed to have [[boundary CFT|boundaries]]. 

In this abstract formulation of QFT a **D-brane** is a type of data assigned by the QFT to boundaries of cobordisms. 

For a broader perspective see at _[[brane]]_.

### In $2d$ rational CFT

A well understood class of examples is this one: among all 2-dimensional [[conformal field theory]] that case of _full rational 2d CFT_ has been understood completely, using [[FFRS-formalism]]. It is then a theorem that full 2-rational CFTs are classified by 

1. a [[modular tensor category]] $\mathcal{C}$ (to be thought of as being the category of representations of the [[vertex operator algebra]] of the 2d CFT);

1. a special symmetric [[Frobenius algebra]] object $A$ [[internalization|internal]] to $\mathcal{C}$.

In this formulation a type of **brane** of the theory is precisely an $A$-[[module]] in $\mathcal{C}$ (an $A$-[[bimodule]] is a [[bi-brane]] or _defect line_ ):

the 2d cobordisms with [[boundary CFT|boundary]] on which the theory defined by $A \in \mathcal{C}$ carry as extra structure on their connected boundary pieces a label given by an equivalence class of an $A$-module in $\mathcal{C}$. The assignment of the CFT to such a cobordism with boundary is obtained by

* triangulating the cobordism, 

* labeling all internal edges by $A$

* labelling all boundary pieces by the $A$-module

* all vertices where three internal edges meet by the multiplication operation 

* and all points where an internal edge hits a boundary by the corresponding [[action]] morphism 

* and finally evaluating the resulting [[string diagram]] in $\mathcal{C}$.

So in this abstract algebraic formulation of QFT on the worldvolume, a brane is just the datum assigned by the QFT to the boundary of a cobordism. But abstractly defined QFTs may arise from [[quantization]] of [[sigma model]]s. This gives these boundary data a geometric interpretation in some space. This we discuss in the next section.

<img src="https://ncatlab.org/nlab/files/BraneAndOpenString.jpg" width="700">

> graphics grabbed from [Ibanez-Uranga 12](#IbanezUranga12)


### In $2d$ TFT

Another case where the branes of a QFT are under good mathematical control is [[TCFT]]: the [[(infinity,1)-category]]-version of a 2d [[TQFT]].

Particularly the [[A-model]] and the [[B-model]] are well understood.

* the branes of the B-model ("B-branes") form the the [[stable (infinity,1)-category]] of [[chain complex]]es of [[quasicoherent sheaves]] on the target space (often considered just in terms of its [[homotopy category of an (infinity,1)-category]], the [[derived category]] of quasicoherent sheaves);

*  the branes of the A-model form the [[Fukaya category]] of the target space.



* the category of D-branes of the A-model on a symplectic [[Landau-Ginzburg model]], is a [[Fukaya-Seidel category]];

* the category of D-branes of the B-model on a complex Landau-Ginzburg model is a category of [[matrix factorization]]s.



There is also a mathematical structure called _[[string topology]]_  with D-branes. At present this is more "string inspired" than actually derived from string theory, though.

### In terms of geometric data of the $\sigma$-model background 

An abstractly defined QFT (as a consistent assignment of state spaces and propagators to cobordisms as in [[FQFT]]) may be obtained by [[quantization]] from _geometric data_ :

Such a _[[sigma-model]] QFT_ is the [[quantization]] of an [[action functional]] on a space of maps $\Sigma \to X$ from a cobordism ("worldvolume") $\Sigma$ to some target space $X$ that may carry further geometric data such as a [[Riemannian metric]],  or other background [[gauge field]]s.

One may therefore try to match the geometric data on $X$ that encodes the $\sigma$-model with the algebraic data of the [[FQFT]] that results after quantization. This gives a geometric interpretation to many of the otherwise purely abstract algebraic properties of the worldvolume QFT.

It turns out that if one checks which geometric data corresponds to the $A$-modules in the above discussion, one finds that these tend to come from structures that look at least roughly like _submanifolds_ of the target space $X$. And typically these submanifolds themselves carry their own background [[gauge field]] data.

A well-understood case is the [[Wess-Zumino-Witten model]]: for this the target space $X$ is a simple [[Lie group]] $X = G$ and the background field is a [[circle n-bundle with connection|circle 2-bundle with connection]] (a [[bundle gerbe]]) on $G$, representing the background field that is known as the [[Kalb-Ramond field]].

In this case it turns out that branes for the sigma model on $X$ are given in the simplest case by conjugacy classes $D \subset G$ inside the group, and that these carry [[twisted bundle|twisted vector bundle]] with the twist given by the Kalb-Ramond background bundle. These vector bundles are known in the [[string theory]] literature as _[[Chan-Paton vector bundles]]_ . The geometric intuition is that a QFT with certain [[boundary CFT|boundary condition]] comes from a quantization of spaces of maps $\Sigma \to G$ that are restricted to take the boundary of $\Sigma$ to these submanifolds.

More generally, one finds that the geometric data that corresponds to the branes in the algebraically defined 2d QFT is given by cocycles in the twisted [[differential K-theory]] of $G$. These may be quite far from having a direct interpretation as submanifolds of $G$.

The case of rational 2d CFT considered so far is only the best understood of a long sequence of other examples. Here the collection of all [[D-branes]] -- identified with the collection of all internal modules over an internal frobenius algebra, forms an ordinary [[category]].

More generally, at least for 2-dimensional [[TQFT]]s analogous considerations yield not just categories but [[stable (∞,1)-categories]] of boundary condition objects. For instance, for what is called the [[B-model]] 2-d [[TQFT]] the category of [[D-branes]] is the [[derived category]] of [[coherent sheaves]] on some Calabi-Yau space.

Starting with Kontsevich's [[homological algebra]] reformulation of [[homological mirror symmetry|mirror symmetry]] the study of (derived) D-brane categories has become a field in its own right in pure mathematics.

... lots of further things to say ...

### As black branes
 {#AsBlackBranes}

In [[perturbative string theory]], hence for small [[string coupling constant]] the D-branes are incarnated as boundary conditions for the string's [[worldsheet]] [[2d CFT]], exhibiting submanifolds in [[spacetime]]. As the string [[coupling constant]] increases and becomes non-perturbative, this picture of [[perturbative string theory]] breaks down, but at low energy (large scales) now [[supergravity]] becomes a good description, and now the D-branes are incarnated as [[black branes]].

<img src="https://ncatlab.org/nlab/files/BlackBrane.png" />

> graphics grabbed from [Ibanez-Uranga 12](#IbanezUranga12)

This transition is also the key to understanding [[black holes in string theory]].


[[!include black branes in supergravity -- table]]


## Examples

### Various dimensions

In [[type IIA supergravity]]

* [[D0-brane]], [[D2-brane]], [[D4-brane]], [[D6-brane]], [[D8-brane]].

In [[type IIB supergravity]]

* [[D1-brane]], [[D3-brane]], [[D5-brane]], [[D7-brane]]

### In the WZW model

For D-branes in the [[WZW-model]] see _[WZW-model -- D-branes](Wess-Zumino-Witten+model#DBranes)_.

## Properties

### As F-branes originating from M-branes

[[!include F-branes -- table]]

### Characterization in terms of Dirac structures

D-branes may be identified with [[Dirac structures]] on 
a [[Courant Lie 2-algebroid]] over spacetime related to the [[type II geometry]] ([Asakawa-Sasa-Watamura](#AsakawaSasaWatamura)). See at _[[Dirac structure]]_ for more on this.

### D-brane charge
 {#DBraneCharge}

In analogy to how in [[electromagnetism]] [[magnetic charge]] is given by a class in [[ordinary cohomology]], so D-brane charge is given in ([[twisted K-theory|twisted]]) [[K-theory]], or, if preferred, in its image under the [[Chern character]].


The [[Chan-Paton bundle]] carried by a D-brane defines a class in [[twisted K-theory]] on the D-brane [[worldvolume]] and the D-brane charge is the push-forward ([[Umkehr map]]) of this class to [[spacetime]], using a [[K-orientation]] of the embedding of the D-brane (a [[spin^c structure]]).

See at _[[K-theory classification of D-brane charge]]_

#### General


More in detail this means the following ([BMRS2](#BMRS2)).

Let $X$ be a manifold regarded as [[spacetime]] and $i \colon Q \hookrightarrow X$ a [[submanifold]] regarded as the [[worldvolume]] of a D-brane. For 
$\nabla_B \colon X \to \mathbf{B}^2 U(1)_{conn}$ the [[circle 2-bundle with connection]] which models the [[background gauge field|background]] [[B-field]], write $\chi_B \colon X \to \mathbf{B}^2 U(1)$ for the underlying [[circle 2-group]]-[[principal 2-bundle]]. 

The corresponding [[Chan-Paton bundle]] (a [[twisted bundle|twisted]] [[line bundle]] for the case of a single D-brane) is the trivialization $\xi$ in 

$$
  \array{
    && Q
    \\
    & \swarrow && \searrow^{\mathrlap{i}}
    \\
    \ast && \swArrow_{\xi} && X
    \\
    & \searrow && \swarrow_{\mathrlap{\chi_B}}
    \\
    && \mathbf{B}^2 U(1)
  }
  \;\;\;\;\;
  \simeq 
  \;\;\;\;\;
  \array{
    && Q
    \\
    & \swarrow &\downarrow& \searrow^{\mathrlap{i}}
    \\
    \ast &\swArrow_{\xi}& \downarrow^{\mathrlap{i^\ast \chi_B}} &\swArrow_{id}& X
    \\
    & \searrow &\downarrow& \swarrow_{\mathrlap{\chi_B}}
    \\
    && \mathbf{B}^2 U(1)
  }
  \,.
$$

Assuming that $i \colon Q \to X$ is [[K-orientation|K-oriented]] in that for instance $X$ has a [[spin-structure]] and $Q$ a [[spin^c-structure]], then under the [[groupoid convolution algebra]] [[functor]] $C^\ast$ this is incarnated as a [[Hilbert bimodule]] which defines a class in [[twisted K-theory|twisted]] [[operator K-theory]], realized as the following comoposite in [[KK-theory]]

$$
  \mathbb{C}
   \stackrel{\Gamma(\xi)}{\to}
  C(Q)_{i^\ast \chi_B}
   \stackrel{i_!}{\to}
  C(X)_{\chi_B}
  \,,
$$

where 

* $C(Q)$ and $C(X)$ are the [[C*-algebra|C*-]][[algebras of functions]] ([[vanishing at infinity]]) on the D-brane and on [[spacetime]], respectively;

* $C(X)_{\chi_B}$ is the [[groupoid convolution algebra]] of [[sections]] of $\chi_B$ regarded as a [[centrally extended groupoid]] over a [[Cech groupoid]] [[resolution]] of $X$ which supports a [[Cech cohomology|Cech cocycle]] for $\chi_B$, and similarly for $C(Q)_{i^\ast \chi B}$ and the pullback/restriction $i^\ast \chi_B$ of the background B-field to the brane;

* $i!$ is the push-forward ([[Umkehr map]]) dual to $i^\ast \colon C(X)_{\chi_B} \to C(Q)_{i^\ast \chi_B}$, realizes as a [[KK-theory]] class

  $$
    D_Q = i! = \in KK(C(Q), C(X)_{\chi_B})
    \,.
  $$

The corresponding **D-brane charge** in KK-theory is the resulting composite (relative [[index]])

$$
  i_!(\xi) =  D_Q(\xi) \in KK(\mathbb{C}, C(X)_{\chi_B}) \simeq K^{[\chi_b]}(X)
$$

in [[twisted K-theory]]. Traditionally only the image of this under the [[Chern character]] 

$$
  ch \colon KK \to HL
$$

in real cohomology/[[cyclic cohomology]] is considered, $ch(D_Q(\xi))$. Moreover, traditonally one thinks of first applying $ch$ to $\xi$ and then pushing forward in $HL$. By the [[C*-algebra|C*-algebraic]] [[Grothendieck-Riemann-Roch theorem]] this gives the [[isomorphism|isomorphic]] expression 

$$
  ch(D_Q(\xi)) 
  \otimes_{C(X)_{\chi_B}} 
  \sqrt{Todd}
  \in HL
  \,,
$$

where on the right we have the relative [[Todd class]]. This is the form the D-brane charge was originally found in the physics literature and in which it is still often given.

(In ([BMRS2, Section 4](#BMRS2)) this is discussed for the untwisted case.)

For more general discussion see at _[Freed-Witten anomaly -- Details](Freed-Witten+anomaly#Details)_ as well as at _[Poincar&#233; duality algebra -- Properties -- K-Orientation and Umkehr maps](Poincar%C3%A9+duality+algebra#PropertiesKOrientationAndUmkehrMaps)_.

#### Via the Atiyah-Hirzebruch spectral sequence
 {#DBraneChargeViaAtiyahHirzebruchSpectralSequence}

The [[Atiyah-Hirzeburch spectral sequence]] expresses, starting from  its $E_2$ pages, [[K-theory]] classes on [[spacetime]] $X$ as [[kernels]] of certain differential acting on ordinary cohomology in all even degrees (for type IIA strings) or all odd degrees (for type IIB strings)

$$
  E_2^{p,q} = H^p(X, KU^q(\ast)) \Rightarrow KU^\bullet(X)
  \,.
$$

Discussion of D-brane charge this way is in ([Maldacena-Moore-Seiberg 01](#MaldacenaMooreSeiberg01), [Evslin-Sati 06](#EvslinSati06)).

## Related concepts

* [[boundary conformal field theory]]

* [[fractional D-brane]], 

  [[permutation D-brane]]

* [[color branes and flavor branes]]

* [[Chan-Paton bundle]], [[twisted bundle]], [[twisted K-theory]], [[Chan-Paton gauge field]]

* [[Freed-Witten anomaly cancellation]]

* [[Dirac-Born-Infeld action]]

* [[black brane]], [[black hole in string theory]]

* [[intersecting D-brane model]]

* [[K-homology]], [[KK-theory]]

* [[O-plane]], [[KR-theory]]

* [[D-brane geometry]]

* [[anti D-brane]]

* [[Myers effect]]

* [[Bridgeland stability condition]]

[[!include table of branes]]

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]


## References

### General

The original article is

* {#Polchinski95} [[Joseph Polchinski]], _Dirichlet-Branes and Ramond-Ramond Charges_, Phys. Rev. Lett. 75:4724-4727, 1995 ([arXiv:hep-th/9510017](https://arxiv.org/abs/hep-th/9510017))

  from p.7:

> although it appears that we have modified the type II theory by adding something new to it, we are now arguing that these objects are actually intrinsic to any nonperturbative formulation of the type II theory; presumably one should think of them as an alternate representation of the black $p$-branes  

General review includes

* [[Joseph Polchinski]], _TASI Lectures on D-Branes_ ([arXiv:hep-th/9611050](https://arxiv.org/abs/hep-th/9611050))

* [[Koji Hashimoto]], _D-Brane -- Superstrings and New Perspective of Our World_, Springer 2012 ([doi:10.1007/978-3-642-23574-0](https://link.springer.com/book/10.1007%2F978-3-642-23574-0), [spire:1188897](http://inspirehep.net/record/1188897))

* [[Pietro Fre]], _The Branes: Three Viewpoints_,  In: _Gravity, a Geometrical Course_ Springer 2013 ([spire:1242195](http://inspirehep.net/record/1242195), [doi:10.1007/978-94-007-5443-0_7](https://doi.org/10.1007/978-94-007-5443-0_7))


A classical text describing how the physics way to think of D-branes leads to seeing that they are objects in derived categories is

* [[Paul Aspinwall]], _D-Branes on Calabi-Yau Manifolds_ ([arXiv:hep-th/0403166](http://arxiv.org/abs/hep-th/0403166)) 

Discussion with an eye towards [[string phenomenology]] is in

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012

This can to a large extent be read as a dictionary from [[homological algebra]] terminology to that of D-brane physics.

More recent similar material with the emphasis on the [[K-theory]] aspects is

* [[Richard Szabo]], _[[Szabo09.pdf:file]]_

Comments on the role of D-branes in [[mathematical physics]] and [[mathematics]] is in 


* [[Gregory Moore]], _[[The Impact of D-Branes on Mathematics]]_ (2014)

### On orbifolds

Review includes

* Frederik Roose, _Strings and D-branes on orbifolds: from boundary states to geometry_, 2001 ([pdf](https://fys.kuleuven.be/itf/groups/hep/files/phd/fredrroose.pdf))

* Nikolas Prezas, _Aspects of branes and orbifolds in string theory_, 2002 ([pdf](https://dspace.mit.edu/bitstream/handle/1721.1/8486/50759455-MIT.pdf?sequence=2), [web](http://hdl.handle.net/1721.1/8486))

See also the references at _[[orientifold]]_.

### As higher super-GS-WZW type $\sigma$-models
  {#ReferencesAsGSsigmaModels}

The [[Green-Schwarz sigma model]] with [[DBI action]] for D-branes is discussed in

* {#CGNSW97} [[Martin Cederwall]], Alexander von Gussich, [[Bengt Nilsson]], Per Sundell, Anders Westerberg, _The Dirichlet Super-p-Branes in Ten-Dimensional Type IIA and IIB Supergravity_, Nucl.Phys. B490 (1997) 179-201 ([arXiv:hep-th/9611159](http://arxiv.org/abs/hep-th/9611159))

* {#APPS97b} [[Mina Aganagic]], [[Jaemo Park]], Costin Popescu, [[John Schwarz]], _Dual D-Brane Actions_, Nucl. Phys. B496 (1997) 215-230 ([arXiv:hep-th/9702133](https://arxiv.org/abs/hep-th/9702133))

Discussion of [[Green-Schwarz action functionals]] for super D-branes and 
the interpretation of the WZW cocycles for the [[D-branes]] as cocycles on "[[extended super-Minkowski spacetime]]" is due to

* {#CAIB99} C. Chryssomalakos, [[José de Azcárraga]], J. M. Izquierdo and C. P&#233;rez Bueno, _The geometry of branes and extended superspaces_, Nuclear Physics B Volume 567, Issues 1&#8211;2, 14 February 2000, Pages 293&#8211;330 ([arXiv:hep-th/9904137](http://arxiv.org/abs/hep-th/9904137))

* {#Sakaguchi00} Makoto Sakaguchi, _IIB-Branes and New Spacetime Superalgebras_, JHEP 0004 (2000) 019 ([arXiv:hep-th/9909143](https://arxiv.org/abs/hep-th/9909143))


* {#AzcarragaIzquierdo01} [[José de Azcárraga]], J. M. Izquierdo, _Superalgebra cohomology, the geometry of extended superspaces and superbranes_ ([arXiv:hep-th/0105125](http://arxiv.org/abs/hep-th/0105125))


See also _[[division algebras and supersymmetry]]_.

A corresponding discussion as [[schreiber:∞-Wess-Zumino-Witten theory]] and refinement of the brane scan to a "brane bouquet" of [[super L-∞ algebra]] [[infinity-Lie algebra cohomology|extensions]] (hence in [[infinity-Lie theory]] via [[schreiber:∞-Wess-Zumino-Witten theory]]) is discussed in

* {#FiorenzaSatiSchreiber13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_, International Journal of Geometric Methods in Modern Physics Volume 12, Issue 02 (2015) 1550018 ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))

* {#FiorenzaSatiSchreiber15} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]] _[[schreiber:The WZW term of the M5-brane and differential cohomotopy]]_, J. Math. Phys. 56, 102301 (2015) ([arXiv:1506.07557](http://arxiv.org/abs/1506.07557))


* {#FiorenzaSatiSchreiber16} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Rational sphere valued supercocycles in M-theory and type IIA string theory]]_ ([arXiv:1606.03206](http://arxiv.org/abs/1606.03206))

* [[Vincent Braunack-Mayer]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Gauge enhancement of Super M-Branes]]_ ([arXiv:1806.01115](https://arxiv.org/abs/1806.01115))



### K-theoretic description and D-brane charge
 {#ReferencesKTheoryDescription}

> See at _[[K-theory classification of D-brane charge]]_

The idea that D-branes have [[Dirac charge quantization]] in [[topological K-theory]] originates in 

* [[Ruben Minasian]], [[Gregory Moore]], _K-theory and Ramond-Ramond charge_, JHEP9711:002,1997 ([arXiv:hep-th/9710230](http://arxiv.org/abs/hep-th/9710230))

* {#Witten98} [[Edward Witten]], _D-Branes And K-Theory_, JHEP 9812:019,1998 ([arXiv:hep-th/9810188](http://arxiv.org/abs/hep-th/9810188))

* {#FreedHopkins00} [[Daniel Freed]], [[Michael Hopkins]], _On Ramond-Ramond fields and K-theory_, JHEP 0005 (2000) 044 ([arXiv:hep-th/0002027](http://arxiv.org/abs/hep-th/0002027))

See also at _[[anti-D-brane]]_.

Discussion of full-blown [[twisted K-theory|twisted]] [[differential K-theory|differential]] [[topological K-theory|K-theory]] and its relation to [[D-brane charge]] in [[type II string theory]] 

* {#GradySati19a} Daniel Grady, [[Hisham Sati]], _Ramond-Ramond fields and twisted differential K-theory_ ([arXiv:1903.08843](https://arxiv.org/abs/1903.08843))

Discussion of full-blown [[twisted K-theory|twisted]] [[differential K-theory|differential]] [[KO-theory|orthogonal]] [[topological K-theory|K-theory]] and its relation to [[D-brane charge]] in [[type I string theory]] (on [[orientifolds]]):

* {#GradySati19b} Daniel Grady, [[Hisham Sati]], _Twisted differential KO-theory_ ([arXiv:1905.09085](https://arxiv.org/abs/1905.09085))



{#KTheorySubtleties} But there remain conceptual issues with the proposal that D-brane  charge is in K-theory, as highlighted for in

* {#BDHKMMS01} [[Jan de Boer]], [[Robbert Dijkgraaf]], [[Kentaro Hori]], [[Arjan Keurentjes]], [[John Morgan]], [[David Morrison]], [[Savdeep Sethi]], section 4.5 and 4.6.5 of  _Triples, Fluxes, and Strings_, Adv.Theor.Math.Phys. 4 (2002) 995-1186 ([arXiv:hep-th/0103170](https://arxiv.org/abs/hep-th/0103170))

* {#Evslin06} [[Jarah Evslin]], section 8 of _What Does(n't) K-theory Classify?_, Second Modave Summer School in Mathematical Physics ([arXiv:hep-th/0610328](https://arxiv.org/abs/hep-th/0610328))

In particular, actual checks of the proposal that D-brane charge is given by K-theory, via concrete computation in [[boundary conformal field theory]], have revealed some subtleties:

* [[Stefan Fredenhagen]], [[Thomas Quella]], _Generalised permutation branes_, JHEP0511:004, 2005 ([arXiv:hep-th/0509153](https://arxiv.org/abs/hep-th/0509153))

  > It might surprise that despite all the progress that has been made in understanding branes on group manifolds, there are usually not enough D-branes known to explain the whole charge group predicted by (twisted) K-theory.

Further review and discussion of D-brane charge in K-theory includes the following

* {#OlsenSzabo00} Kasper Olsen, [[Richard Szabo]], _Brane Descent Relations in K-theory_, Nucl.Phys. B566 (2000) 562-598 ([arXiv:hep-th/9904153](https://arxiv.org/abs/hep-th/9904153))

* Kasper Olsen, [[Richard Szabo]], _Constructing D-Branes from K-Theory_, Adv.Theor.Math.Phys. 3 (1999) 889-1025 ([arXiv:hep-th/9907140](https://arxiv.org/abs/hep-th/9907140))

* [[John Schwarz]], _TASI Lectures on Non-BPS D-Brane Systems_ ([arXiv:hep-th/9908144](https://arxiv.org/abs/hep-th/9908144))

* {#Witten00} [[Edward Witten]], _Overview Of K-Theory Applied To Strings_, Int.J.Mod.Phys.A16:693-706,2001 ([arXiv:hep-th/0007175](https://arxiv.org/abs/hep-th/0007175))

* [[Greg Moore]], _K-Theory from a physical perspective_ ([arXiv:hep-th/0304018](http://arxiv.org/abs/hep-th/0304018))

* [[Juan José Manjarín]], _Topics on D-brane charges with B-fields_, Int.J.Geom.Meth.Mod.Phys. 1 (2004) ([arXiv:hep-th/0405074](http://arxiv.org/abs/hep-th/0405074))

A textbook account of D-brane charge in ([[twisted K-theory|twisted]]) [[topological K-theory]] is 

* [[Dale Husemoeller]], [[Michael Joachim]], [[Branislav Jurco]], [[Martin Schottenloher]], _[[Basic Bundle Theory and K-Cohomology Invariants]]_, Lecture Notes in Physics, Springer 2008  ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726corr1.pdf))

See also for instance

* [[Ilka Brunner]], [[Jacques Distler]], _Torsion D-Branes in Nongeometrical Phases_ ([arXiv:hep-th/0102018](https://arxiv.org/abs/hep-th/0102018))

Discussion of D-branes in [[KK-theory]] is reviewed in

* {#Szabo} [[Richard Szabo]], _D-branes and bivariant K-theory_, Noncommutative Geometry and Physics 3 1 (2013): 131. ([arXiv:0809.3029](http://arxiv.org/abs/0809.3029))
 

based on

* {#ReisSzabo05} Rui Reis, [[Richard Szabo]], _Geometric K-Homology of Flat D-Branes_ ,Commun.Math.Phys. 266 (2006) 71-122 ([arXiv:hep-th/0507043](https://arxiv.org/abs/hep-th/0507043))

* [[Jacek Brodzki]], [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], _D-Branes, RR-Fields and Duality on Noncommutative Manifolds_, Commun. Math. Phys. 277:643-706,2008 ([arXiv:hep-th/0607020](http://arxiv.org/abs/hep-th/0607020))

* {#BMRS2} [[Jacek Brodzki]], [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]],  _Noncommutative correspondences, duality and D-branes in bivariant K-theory_, Adv. Theor. Math. Phys.13:497-552,2009 ([arXiv:0708.2648](http://arxiv.org/abs/0708.2648))
 

* [[Jacek Brodzki]], [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]],  _D-branes, KK-theory and duality on noncommutative spaces_, J. Phys. Conf. Ser. 103:012004,2008 ([arXiv:0709.2128](http://arxiv.org/abs/0709.2128))

In particular ([BMRS2](#BMRS2)) discusses the definition and construction of D-brane charge as a generalized [[index]] in [[KK-theory]]. The discussion there focuses on the untwisted case. Comments on the generalization of this to topologicall non-trivial [[B-field]] and hence [[twisted K-theory]] is in

* [[Richard Szabo]], _D-Branes, Tachyons and K-Homology_,  	Mod. Phys. Lett. A17 (2002) 2297-2316 ([arXiv:hep-th/0209210](http://arxiv.org/abs/hep-th/0209210))


Specifically for D-branes in [[WZW models]] see

* [[Peter Bouwknegt]], _A note on equality of algebraic and geometric D-brane charges in WZW models_ ([pdf](http://people.physics.anu.edu.au/~drt105/papers/BR0312259.pdf))

More on this, with more explicit relation to [[noncommutative motives]], is in 

* {#Mahanta09} [[Snigdhayan Mahanta]], _Noncommutative correspondence categories, simplicial sets and pro $C^\ast$-algebras_ ([arXiv:0906.5400](http://arxiv.org/abs/0906.5400))
 

* {#Mahanta11} [[Snigdhayan Mahanta]], _Higher nonunital Quillen $K'$-theory, KK-dualities and applications to topological $\mathbb{T}$-duality_, Journal of Geometry and Physics, Volume 61, Issue 5 2011, p. 875-889.   ([pdf](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KQ.pdf))
 
Discussion of D-brane [[matrix models]] taking these K-theoretic effects into account ([[K-matrix model]]) is in

* {#AsakawaSugimotoTerashima01} T. Asakawa, S. Sugimoto, S. Terashima, _D-branes, Matrix Theory and K-homology_, JHEP 0203 (2002) 034 ([arXiv:hep-th/0108085](https://arxiv.org/abs/hep-th/0108085))

{#ChargeInEquivariantKTheory} The proposal that D-brane charge on [[orbifolds]] is measured in [[equivariant K-theory]] goes back to 

* [Witten 98, section 5.1](#Witten98) 

but it was pointed out that only a subgroup of equivariant K-theory can be physically relevant in

* {#BDHKMMS01} [[Jan de Boer]], [[Robbert Dijkgraaf]], [[Kentaro Hori]], [[Arjan Keurentjes]], [[John Morgan]], [[David Morrison]], [[Savdeep Sethi]], around (137) of  _Triples, Fluxes, and Strings_, Adv.Theor.Math.Phys. 4 (2002) 995-1186 ([arXiv:hep-th/0103170](https://arxiv.org/abs/hep-th/0103170))

Further discussion of [[equivariant K-theory]] for D-branes on [[orbifolds]] includes the following:

* Hugo García-Compeán, _D-branes in orbifold singularities and equivariant K-theory_, Nucl.Phys. B557 (1999) 480-504 ([arXiv:hep-th/9812226](https://arxiv.org/abs/hep-th/9812226))

* [[Matthias Gaberdiel]], [[Bogdan Stefanski]], _Dirichlet Branes on Orbifolds_, Nucl.Phys.B578:58-84, 2000 ([arXiv:hep-th/9910109](https://arxiv.org/abs/hep-th/9910109))

* [[Igor Kriz]], Leopoldo A. Pando Zayas, Norma Quiroz, _Comments on D-branes on Orbifolds and K-theory_, Int.J.Mod.Phys.A23:933-974, 2008 ([arXiv:hep-th/0703122](https://arxiv.org/abs/hep-th/0703122))

* [[Richard Szabo]], [[Alessandro Valentino]], _Ramond-Ramond Fields, Fractional Branes and Orbifold Differential K-Theory_, Commun.Math.Phys.294:647-702, 2010 ([arXiv:0710.2773](https://arxiv.org/abs/0710.2773))

Discussion of [[real K-theory]] for D-branes on [[orientifolds]] includes the following:

The original observation that [[D-brane charge]] for [[orientifolds]] should be in [[KR-theory]] is due to

* [Witten 98, section 5](#Witten98)

and was then re-amplified in

* {#Gukov99} [[Sergei Gukov]], _K-Theory, Reality, and Orientifolds_, Commun.Math.Phys. 210 (2000) 621-639 ([arXiv:hep-th/9901042](https://arxiv.org/abs/hep-th/9901042))

* {#BergmanGimonSugimoto01} [[Oren Bergman]], E. Gimon, [[Shigeki Sugimoto]], _Orientifolds, RR Torsion, and K-theory_, JHEP 0105:047, 2001 ([arXiv:hep-th/0103183](https://arxiv.org/abs/hep-th/0103183))

With further developments in 

* [[Varghese Mathai]], [[Michael Murray]], [[Daniel Stevenson]], _Type I D-branes in an H-flux and twisted KO-theory_, JHEP 0311 (2003) 053 ([arXiv:hep-th/0310164](https://arxiv.org/abs/hep-th/0310164))

Discussion of orbi-orienti-folds using [[equivariant K-theory|equivariant]] [[KO-theory]] is in

* N. Quiroz, [[Bogdan Stefanski]], _Dirichlet Branes on Orientifolds_, Phys.Rev. D66 (2002) 026002 ([arXiv:hep-th/0110041](https://arxiv.org/abs/hep-th/0110041))

* [[Volker Braun]], [[Bogdan Stefanski]], _Orientifolds and K-theory_ ([arXiv:hep-th/0206158](https://arxiv.org/abs/hep-th/0206158))

* H. Garcia-Compean, W. Herrera-Suarez, B. A. Itza-Ortiz, O. Loaiza-Brito, _D-Branes in Orientifolds and Orbifolds and Kasparov KK-Theory_, JHEP 0812:007, 2008 ([arXiv:0809.4238](https://arxiv.org/abs/0809.4238))

An elaborate proposal for the correct flavour of real equivariant K-theory needed for [[orientifolds]] is sketched in

* {#Precis} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))

Discussion of the alleged K-theory classification of D-brane charge in relation to the [[M-theory]] [[supergravity C-field]] is in

* {#DMW00} D. Diaconescu, [[Gregory Moore]], [[Edward Witten]], _$E_8$ Gauge Theory, and a Derivation of K-Theory from M-Theory_, Adv.Theor.Math.Phys.6:1031-1134,2003 ([arXiv:hep-th/0005090](http://arxiv.org/abs/hep-th/0005090)), summarised in _A Derivation of K-Theory from M-Theory_ ([arXiv:hep-th/0005091](http://arxiv.org/abs/hep-th/0005091))

See also

* {#GarciaUranga05} Inaki Garcia-Etxebarria, [[Angel Uranga]], _From F/M-theory to K-theory and back_, JHEP 0602:008,2006 ([arXiv:hep-th/0510073](https://arxiv.org/abs/hep-th/0510073))


For more on this perspective as 10d type II as a [[self-dual higher gauge theory]] in the boudnary of a kind of [[higher dimensional Chern-Simons theory|11-d Chern-Simons theory]] is in

* {#BelovMooreII} Dmitriy Belov, [[Greg Moore]], _Type II Actions from 11-Dimensional Chern-Simons Theories_ ([arXiv:hep-th/0611020](http://arxiv.org/abs/hep-th/0611020))

More complete discussion of the decomposition of the [[supergravity C-field]] as one passes from 11d to 10d is in 

* {#MathaiSati03} [[Varghese Mathai]], [[Hisham Sati]], _Some Relations between Twisted K-theory and E8 Gauge Theory_, JHEP0403:016,2004 ([arXiv:hep-th/0312033](http://arxiv.org/abs/hep-th/0312033))


### Via the Atiyah-Hirzebruch spectral sequence

Expression of these D-brane K-theory classes via the [[Atiyah-Hirzebruch spectral sequence]] is discussed in

* {#MaldacenaMooreSeiberg01} [[Juan Maldacena]], [[Gregory Moore]], [[Nathan Seiberg]], _D-Brane Instantons and K-Theory Charges_, JHEP 0111:062,2001 ([arXiv:hep-th/0108100](http://arxiv.org/abs/hep-th/0108100))

* {#EvslinSati06} [[Jarah Evslin]], [[Hisham Sati]], _Can D-Branes Wrap Nonrepresentable Cycles?_, JHEP0610:050,2006 ([arXiv:hep-th/0607045](http://arxiv.org/abs/hep-th/0607045))

Detailed review of this is in 

* [[Fabio Ruffino]], _Topics on topology and superstring theory_ ([arXiv:0910.4524](http://arxiv.org/abs/0910.4524))



### For rational CFT

For exhaustive details on D-branes in 2-dimensional rational [[CFT]] see the references given at 

* [[FFRS-formalism]]

### Branes within branes

* [[Michael Douglas]], _Branes within Branes_ ([arXiv:hep-th/9512077](http://arxiv.org/abs/hep-th/9512077))

### For topological strings

A discussion of topological D-branes in the context of [[higher category theory]] is in

* [[Anton Kapustin]], _Topological Field Theory, Higher Categories, and Their Applications_ ([arXiv:1004.2307](http://arxiv.org/abs/1004.2307))

### Open string worldsheet Anomaly cancellation

The need for [[twisted spin^c structures]] as [[quantum anomaly]]-cancellaton condition on the [[worldvolume]] of D-branes was first discussed in

* [[Daniel Freed]], [[Edward Witten]], _Anomalies in String Theory with D-Branes_ ([arXiv:hep-th/9907189](http://arxiv.org/abs/hep-th/9907189))

More details are in 

* [[Anton Kapustin]], _D-branes in a topologically nontrivial B-field_ , Adv. Theor. Math. Phys.
4, no. 1, pp. 127&#8211;154 (2000), ([arXiv:hep-th/9909089](http://arxiv.org/abs/hep-th/9909089))

A clean review is provided in

* Kim Laine, _Geometric and topological aspects of Type IIB D-branes_ ([arXiv:0912.0460](http://arxiv.org/abs/0912.0460))

For more see at _[[Freed-Witten anomaly cancellation]]_.


### Relation to Dirac structures

* {#AsakawaSasaWatamura} Tsuguhiko Asakawa, Shuhei Sasa, Satoshi Watamura, _D-branes in Generalized Geometry and Dirac-Born-Infeld Action_ ([arXiv:1206.6964](http://arxiv.org/abs/1206.6964))
 



[[!redirects D-branes]]

[[!redirects D-brane charge]]
[[!redirects D-brane charges]]