[[!redirects Beilinson regulator]]

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

In the context of [[arithmetic geometry]] a _higher regulator_, or just _regulator_ for short, is a [[homomorphism]] from [[algebraic K-theory]] to a suitable [[ordinary cohomology]] theory. (It makes sense to think that it "regulates" [[cocycles]] in [[algebraic K-theory]], which tend to be hard to analyze, to become cocycles in ordinary cohomology, about which typically more may be said.) This generalizes the original concept of a [[regulator of a number field]] which is a measure for the [[group of units]] of the [[ring of integers]] of the number field, in view of the fact that the [[determinant]] function provides a canonical homomorphism $K_1 \to GL_1$ from the first [[algebraic K-theory]] to the [[group of units]].

Regulators are used in the study of [[L-functions]] for instance in the context of the [[Beilinson conjectures]] and the [[Bloch-Kato conjecture]].

The simplest example of such regulators are

* the [[analytic class number formula]];

* the [[Dedekind zeta-function]] of $K$;

* the Dirichlet regulator map, discussed below.

These regulators may be understood as essentially being the [[Chern characters]] in [[algebraic K-theory]] ([Deninger Scholl (2.6)](#DeningerScholl), [Tamme 12](#Tamme12)).  Based on this observation they serve to define [[differential cohomology]]-refinements of algebraic K-theory, namely _[[differential algebraic K-theory]]_ ([Bunke-Tamme 12](#BunkeTamme12)).

## Definition

### Dirichlet and Borel regulator
 {#BorelRegulator}

For $R$ a [[ring]], $K R$ denoting its [[algebraic K-theory]] [[spectrum]] and $\Sigma^n H \mathbb{R}$ a [[suspension]] of the [[Eilenberg-MacLane spectrum]] of the [[real numbers]], then a regulator of $K R$-[[cohomology theory]] is a [[homomorphism]] of [[spectra]]

$$
  r_{\sigma,p} \;\colon\; K R \longrightarrow \Sigma^p H \mathbb{R}
$$

or equivalently is the induced [[cohomology operations]]. e.g. ([Bunke-Tamme 12, 1.2](#BunkeTamme12))

If here $R$ is the [[ring of integers]] of a [[number field]] and $\sigma \colon R \hookrightarrow \mathbb{C}$ is a choice of embedding into the [[complex numbers]], then the _Borel regulator_ ([Borel 74](#Borel74)) is of this form, for odd $p$, such that its induced [[cohomology operation]]

$$
  r_{\sigma,p} \;\colon\; K_1(R) \longrightarrow \mathbb{R}
$$

is the _Dirichlet regulator_ given by

$$
  u \mapsto log {\vert \sigma(u) \vert}
  \,.
$$

A description of this in [[differential algebraic K-theory]] is in ([Bunke-Tamme  12, 1.2](#BunkeTamme12)):

for $X$ a [[smooth manifold]], then a class in $K R^0(X)$ is represented by  a [[finitely generated module|finitely generated]] [[projective module|projective]] $R$-[[module bundle]] $V \to X$. Write

$$
  cycl(V) \in K R^0(X)
$$

for this class. 

Under the chosen embedding $\sigma$ we have the [[complexification]] $V \otimes_\sigma \mathbb{C}$ of this [[module bundle]], which is a [[complex vector bundle]] with (because $R$ is geometrically [[discrete object|discrete]]) a [[flat connection]] $\nabla_{V_\sigma}$.  

The choice of hermitean structure on $V_\sigma$, hence a [[reduction of the structure group]] to the [[unitary group]] induces an adjoint connection $\nabla_{V_\sigma}^\ast$. Write then 

$$
  CS_p(\nabla_{V_\sigma}^\ast, \nabla_{V_\sigma})
$$

for the relative [[Chern-Simons form]] between these two connections, hence for the [[transgression]] of the relative [[Chern character]] in degree $p+1$. 

This is a closed differential form, (the Kamber-Tondeur form, see [Bismut-Lott 95](#BismutLott95)).

This differential form represents, via the [[de Rham theorem]] [[isomorphism]], the Dirichlet regulator above

$$
  r_{\sigma,p}(cycl(V))
  \simeq
  [CS_p(\nabla_{V_\sigma}^\ast, \nabla_{V_\sigma})]
  \in 
  H_{dR}^p(X) \simeq H^p(X,\mathbb{R})
  \,.
$$

In [[differential algebraic K-theory]] this construction can be refined from landing in [[de Rham cohomology]] to landing in genuine [[ordinary differential cohomology]] ([[higher prequantization]]), hence with $CS_p(\nabla_{V_\sigma}^\ast, \nabla_{V_\sigma})$ itself realized as the [[curvature]] of a [[circle n-bundle with connection|circle (p-1)-bundle with connection]].

### Regulators of generalized algebraic K-theories
 {#ForGeneralizedAlgebraicKTheories}

Based on the [above](#BorelRegulator) abstract formulation of 
the classical Beilinson- and Borel-regulators, the following
general definition suggests itsef:

+-- {: .num_defn}
###### Definition

Consider the following data:

1. For $\mathcal{C}^\otimes$ a [[symmetric monoidal (∞,1)-category]] write $\mathcal{K}(\mathcal{C})$ for its [[algebraic K-theory of a symmetric monoidal (∞,1)-category]]. 

1. For $A \in Ch_\bullet(Ab)$ any [[chain complex]] write $H A$ for its [[Eilenberg-MacLane spectrum]] given by the [[stable Dold-Kan correspondence]].

Then a _regulator_ with [[coefficients]] in $A$ of the [[algebraic K-theory]] [[Brown representability theorem|represented]] by $\mathcal{K}(\mathcal{C})$ is a [[homomorphism]] of [[spectra]] (hence a [[cohomology operation]])

$$
  r \;\colon\; \mathcal{K}(\mathcal{C}) \longrightarrow H A
  \,.
$$

Accordingly the [[spectrum]] of $A$-regulators of $\mathcal{K}(\mathcal{C})$ is the [[mapping spectrum]] $[\mathcal{K}(\mathcal{C}), H A]$.
 
=--

([Bunke-Tamme 12, def. 23](#BunkeTamme12)).

### Beilinson regulators

(...)

## Examples

### Constructions in terms of line $n$-bundles ($n-1$-bundle gerbes)
 {#GeometricConstruction}

Some special cases of Beilinson regulators have known "geometric" constructions in terms of maps relating [[holomorphic line n-bundles]] for various $n$.

The regulator

$$
  c_{2,2} \colon K_2(X) \longrightarrow H^2(X, \mathbb{Z}(2)_{\mathcal{D}})
$$

is given by sending pairs of non-vanising [[holomorphic functions]] to the [[holomorphic line bundle]] which is their [[Beilinson-Deligne cup product]] (the "[[Deligne line bundle]]") ([Bloch 78](#Bloch78)).

Moreover, the regulator 

$$
  c_{1,2} \colon K_1(X) \longrightarrow H^3(X, \mathbb{Z}(2)_{\mathcal{D}})
$$

or rather its component

$$
  c_{1,2} \colon H^1(X, \mathbf{K}_2) \longrightarrow H^3(X, \mathbb{Z}(2)_{\mathcal{D}})
$$

is given by sending functions constituing a [[cocycle]] in the relevant [[Gersten complex]] to a [[bundle gerbe]] whose transition line bundles are [[Deligne line bundles]] built from these functions ([Brylinski 94, theorem 3.3](#Brylinski94)).

Notice that $c_{2,1}$ is the regulator that interpolates the [[string 2-group]]/[[universal Chern-Simons line 3-bundle]] for a [[reductive algebraic group]] from the algebraic to the complex-analytic realm, see at _[universal Chern-Simons line 3-bundles -- For reductive algebraic groups](universal+Chern-Simons+line+3-bundle#ForReductiveAlgebraicGroups)_.




## Properties

### Becker-Gottlieb transfer and GRR for algebraic K-theory

 {#BeckerGottliebTransfer}

For $\pi \colon X \to B$ a [[proper map|proper]] [[submersion]] of [[smooth manifolds]], there is a variant of [[fiber integration in generalized cohomology]] given by the [[Becker-Gottlieb transfer]] in some $E$-[[cohomology theory]]

$$
  tr_\pi \;\colon\; E^\ast(X) \longrightarrow E^\ast(B)
  \,.
$$

Moreover, for the above [[sheaves]] of $R$-[[modules]] $cycl(V)$ we have the [[direct image]] sheaves $\pi_\ast V$ and there is an identity

$$
  \underset{i \geq 0}{\sum} (-1)^i cycl(R^i \pi_\ast(V))
  \simeq
  tr_\pi(cycl(V))
$$ 

in $K R(B)$. The [above](#BorelRegulator) Borel-Dirichlet regulator $r_{\sigma,p}$ is such that it preseves this as an identity in $H(X,\mathbb{R})$. Hence it plays a role here analogous that of the [[Chern character]] in the [[Grothendieck-Riemann-Roch theorem]].

The [[Becker-Gottlieb transfer]] refines in turn to [[differential cohomology]], hence [[differential algebraic K-theory]] mapping to [[ordinary differential cohomology]], according to ([Bunke-Gepner 13](BunkeGepner13)). 

However, the above relation between direct image of sheaves and push-forward in cohomology receives a correction when refined to [[differential algebraic K-theory]], a correction by a term in the image of the inclusion $a(-)$ of differential forms into [[differential cohomology]], by the [[transfer index conjecture]] one has


$$
  \underset{i \geq 0}{\sum} (-1)^i \widehat{cycl}(R^i \pi_\ast(V))
   + a(something)
  \simeq
  \widehat{tr}_\pi(\widehat{cycl}(V))
$$ 

where the hats denote the [[differential cohomology]] refinement.


See at _[[Becker-Gottlieb transfer]]_.

### Relation to complex volumes and Bloch group
 {#RelationToComplexVolumes}

> under construction

There is some relation betwee the Borel regulators and [[complex volumes]] of [[hyperbolic manifolds]] via maps out of the [[Bloch group]] ([Suslin 90](#Suslin90), [Neumann-Yang 97, p. 17](#NeumannYang97), [Zickert 07, p. 3](#Zickert07), [Zickert 09](#Zickert09)).

For $k$ an [[algebraic number field]] and $\sigma_1, \cdots, \sigma_{r_2}\colon k \to \mathbb{C}$ its complex embeddings up to [[conjugation]], then write

$$
  vol_j \coloneqq vol \circ (\sigma_j)\colon H_3(PSL(2,k), \mathbb{Z})
  \to \mathbb{R}
$$

Then then map

$$
  (vol_1, \cdots, vol_{r_2}) \colon H_3(PSL(2,k),\mathbb{Z}) \longrightarrow \mathbb{R}^{r_2}
$$

is the Borel regulator  ([Neumann 11, p. 6](#Neumann11)).


## Related concepts

* [[Beilinson conjecture]]

## References

The Borel regulator is due to 

* {#Borel74} [[Armand Borel]], _Stable real cohomology of arithmetic groups_, Ann. Sci. Ecole Norm. Sup. (4) 7 (1974), 235-272 (1975). MR 0387496 
  
The Beilinson regulator with values in [[Deligne cohomology]] is due to 

* {#Bloch78} [[Spencer Bloch]], _Applications of the dilogarithm function in algebraic Ktheory and algebraic geometry_, in: Proc. of the International Symp. on Alg. Geometry, Kinokuniya, Tokyo, 1978

* {#Bloch81} [[Spencer Bloch]], _The dilogarithm and extensions of Lie algebras_, Algebraic K-Theory Evanston 1980, Lecture Notes in Mathematics Volume 854, 1981, pp 1-23

* {#Beilinson85} [[Alexander Beilinson]] _Higher regulators and values of L-functions_, Journal of Soviet Mathematics 30 (1985), 2036-2070, ([mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=intd&paperid=73&option_lang=eng), [DOI](http://dx.doi.org/10.1007%2FBF02105861))

* {#Beilinson80} [[Alexander Beilinson]], _Higher regulators of curves_, Funct. Anal. Appl. 14 (1980), 116-118, [mathnet (Russian)](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=faa&paperid=1800&option_lang=eng).

* {#Beilinson87} [[Alexander Beilinson]], _Height pairing between algebraic cycles_, in _K-Theory, Arithmetic and Geometry_, Lecture Notes in Mathematics Volume 1289, 1987, pp 1-26, [DOI](http://dx.doi.org/10.1007/BFb0078364).

reviewed in

* {#Soule84} [[Christophe Soulé]], _R&#233;gulateurs_ S&#233;minaire Bourbaki, 27 (1984-1985), Exp. No. 644, 17 p. ([Numdam](http://www.numdam.org/item?id=SB_1984-1985__27__237_0))

* {#EsnaultViehweg88} [[Hélène Esnault]], [[Eckart Viehweg]], _Deligne-Beilinson cohomology_ in Rapoport, Schappacher, Schneider (eds.) _Beilinson's Conjectures on Special Values of L-Functions_ . Perspectives in Math. 4, Academic Press (1988) 43 - 91 ([pdf](http://www.uni-due.de/~mat903/preprints/ec/deligne_beilinson.pdf))

* {#Goncharov04} [[Alexander Goncharov]], _Regulators_, Algebraic K-theory Handbook ([arXiv:0407308](http://arxiv.org/abs/math/0407308))

A discussion of the Beilinson regulator on $K_2$ in terms of [[bundle gerbes]] is in

* {#Brylinski94} [[Jean-Luc Brylinski]], _Holomorphic gerbes and the Beilinson regulator_, Ast&#233;risque 226 (1994): 145-174 ([[Brylinski94.pdf:file]])

See also

* [[Christophe Soulé]], _On higher p-adic regulators_, Algebraic K-Theory Evanston 1980 Lecture Notes in Mathematics Volume 854, 1981, pp 372-401_ ([publisher page](http://link.springer.com/chapter/10.1007%2FBFb0089530))

The relation to [[Chern characters]] is made very explicit in

* {#Tamme12} [[Georg Tamme]], _Karoubi's relative Chern character and Beilinson's regulator_, Ann. Sci. Ec. Norm. Super. (4) 45 (2012), no. 4, 601-636. ([[TammeRegulator.pdf:file]])

see also

* {#DeningerScholl} [[Christopher Deninger]], [[Anthony Scholl]], section 2.6 of _The Beilinson conjectures_ ([pdf](https://www.dpmms.cam.ac.uk/~ajs1005/preprints/d-s.pdf)) 

The interpretation of these regulator Chern characters in [[differential algebraic K-theory]] is due to


* {#BunkeGepner13} [[Ulrich Bunke]], [[David Gepner]], _Differential function spectra, the differential Becker-Gottlieb transfer, and applications to differential algebraic K-theory_ ([arXiv:1306.0247](http://arxiv.org/abs/1306.0247))
 

* {#BunkeTamme12} [[Ulrich Bunke]], [[Georg Tamme]], _Regulators and cycle maps in higher-dimensional differential algebraic K-theory_ ([arXiv:1209.6451](http://arxiv.org/abs/1209.6451))
 

based on 


* {#BismutLott95} [[Jean-Michel Bismut]], [[John Lott]], _Flat vector bundles, direct images and
higher real analytic torsion_, J. Amer. Math. Soc. 8 (1995), no. 2, 291-363.
 

See also

* {#Weibel84} [[Charles Weibel]], _Algebraic K-theory and the Adams e-invariant_, in _Algebraic K-theory, number theory, geometry and analysis _(Bielefeld, 1982), volume 1046 of Lecture Notes in Math., pages 442-450. Springer, Berlin, 1984. 61 [pdf](http://www.math.illinois.edu/K-theory/handbook/1-139-190.pdf)

* {#Suslin84} A.A. Suslin, _On the K-theory of local fields_, In Proceedings of the Luminy conference on algebraic K-theory (Luminy, 1983), volume 34, pages 301-318, 1984.

* Wikipedia, _[Beilinson regulator](http://en.wikipedia.org/wiki/Beilinson_regulator)_

Formore references see also at _[[Beilinson conjecture]]_.

Relation of the Borel regulator to the [[Bloch group]], the [[Cheeger-Simons class]]/[[complex volumes]] of [[hyperbolic manifolds]] is discussed in

* {#Suslin90} [[Andrei Suslin]]. _$K_3$ of a field, and the Bloch group_. Trudy Mat. Inst. Steklov., 183:180&#8211;199, 229, 1990. Translated in Proc. Steklov Inst. Math. 1991, no. 4, 217&#8211;239, Galois theory, rings, algebraic groups and their applications (Russian).

* {#NeumannYang97} [[Walter Neumann]], Jun Yang, _Bloch invariants of hyperbolic 3-manifolds_, Duke Math. J. Volume 96, Number 1 (1999), 29-59. ([arXiv:math/9712224](http://arxiv.org/abs/math/9712224), [Euclid](http://projecteuclid.org/euclid.dmj/1077228942))

* {#Zickert07} [[Christian Zickert]], _The volume and Chern-Simons invariant of a representation_, Duke Math. J., 150 (3):489-532, 2009 ([arXiv:0710.2049](http://arxiv.org/abs/0710.2049), [Euclid](http://projecteuclid.org/euclid.dmj/1259332507))

* {#Zickert09} [[Christian Zickert]], _The extended Bloch group and algebraic K-theory_ ([arXiv:0910.4005](http://arxiv.org/abs/0910.4005))


* {#Neumann11} [[Walter Neumann]], _Realizing arithmetic invariants of hyperbolic 3-manifolds_, Contemporary Math 541 (Amer. Math. Soc. 2011), 233--246 ([arXiv:1108.0062](http://arxiv.org/abs/1108.0062))

[[!redirects Beilinson regulators]]

[[!redirects Beilinson's regulator]]
[[!redirects Beilinson's regulators]]

[[!redirects Borel regulator]]
[[!redirects Borel regulators]]

[[!redirects Dirichlet regulator]]
[[!redirects Dirichlet regulators]]

[[!redirects regulator]]
[[!redirects regulators]]

[[!redirects regulator in algebraic K-theory]]
[[!redirects regulators in algebraic K-theory]]

[[!redirects higher regulators]]