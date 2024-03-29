> this entry is about the notion of _genus_ in [[algebraic topology]]/[[cohomology]]. For classification of [[surfaces]] see instead the (related) entry _[[genus of a surface]]_, _[[genus of a curve]]_. There is also [[genus of a lattice]].

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

### Basic

For $R$ a ([[commutative ring|commutative]]) [[ring]], an $R$-valued **genus** is a ring [[homomorphism]] into $R$

$$
  \sigma : \Omega_\bullet  \to R
$$

from a [[cobordism ring]] for [[cobordisms]] with specified structure; typical choices being [[orientation]] or [[stable complex structure]]. Often the rationalization of such a morphism is meant, see below at _[Properties -- Rationalization](#Rationalization)_.

To emphasize that this is indeed a ring homomorphism and hence in particular respects the multiplicative structure, a genus is sometimes (especially in older literature) synonymously called a _multiplicative genus_.


### In stable homotopy theory and generalized cohomology theory
 {#InStableHomotopyTheory}


Since the [[cobordism ring]] is the ring of coefficients of the corresponding universal [[Thom spectrum]], e.g $M U$, $M SO$, so a genus may also be written as a ring homomorphism of the form

$$
  M SO_\ast \longrightarrow R
$$

or

$$
  M U_\ast \longrightarrow R
$$

respectively. Written this way it is immediate that genera arise naturally as the value on [[homotopy groups]] (the "[[decategorification]]" or "de-homotopification") of homomorphisms of [[E-∞ ring]] [[spectra]] from an actual universal [[Thom spectrum]] to some [[E-∞ ring]] $E$ with [[coefficient]] ring $R$

$$
  M SO \longrightarrow E
$$

or

$$
  M U \longrightarrow E
  \,.
$$

This in turn induces multiplicative morphisms of the [[cohomology theories]] [[Brown representability theorem|represented]] by these spectra (the domain being hence [[cobordism cohomology theory]]), and these multiplicative maps are the "families version" of the given genus/[[index]] ([Hopkins 94, section 3](#Hopkins94)).

Such homomorphisms in turn arise naturally from [[orientation in generalized cohomology|universal orientations in generalized E-cohomology]]. Namely such an orientation is a [[homotopy]] of the form

$$
  \array{
     \ast && \longleftarrow && B SO
     \\
       & {}_{\mathllap{0}}\searrow & \swArrow_\sigma  & \swarrow_{\mathrlap{J}}
     \\
     && B GL_1(E)
     \\
     && \downarrow
     \\
     && E Mod
  }
$$

(a trivialization of the $E$-[[(∞,1)-module bundle]] [[associated ∞-bundle|associated]] to the [[spherical fibration]] given by the [[J-homomorphism]]) and under forming [[homotopy colimits]] in $E$[[(∞,1)Mod]] this becomes an $E$-linear map

$$
  M SO \wedge E  \longleftarrow E
$$


hence a map

$$
  M SO  \longleftarrow E
  \,.
$$


At least in some important cases, genera seem to be naturally understood as encoding [[sigma-model]] [[quantum field theories]]. For $G$ some structure, the [[Thom spectrum]] $M G$ is the classifying space of [[manifolds]] with [[G-structure]], and hence may be thought of as classifying [[target spaces]] for [[sigma-models]]. The codomain spectrum $R$ itself may then be thought of as a classifying space for a certain class of QFTs, and hence the genus $\sigma : M G \to R$ can be thought of as assigning to any target space the corresponding [[sigma-model]]. 

This is for instance the case at least over the point for the [[A-hat genus]] $M Spin \to K O$, which may be thought of as sending manifolds with [[spin structure]] to the corresponding [[(1,1)-dimensional Euclidean field theories and K-theory|(1,1)-supersymmetric EFT]] ("[[spinning particle]]"); and for the [[Witten genus]] $M String \to tmf$, which can be thought of as sending a manifold with [[string structure]] to the corresponding [[(2,1)-dimensional Euclidean field theories and tmf|(2,1)-supersymmetric EFT]] ("[[heterotic string]]").

## Properties

### Rationalization
 {#Rationalization}

When the [[coefficient]] [[ring]] $R$ does not have additive [[torsion]], then any ring homomorphism

$$
  \phi \colon \Omega^{U/SO}_\bullet \longrightarrow R
$$

is determined already by its rationalization

$$
  \phi \colon \Omega^{U,SO}_\bullet\otimes \mathbb{Q} \longrightarrow R \otimes \mathbb{Q}
$$

which is traditionally denoted by the same symbol. The rational [[cobordism rings]] in turn are known to be [[polynomial rings]]

$$
  \Omega^U_\bullet\otimes \mathbb{Q} \simeq \mathbb{Q}[\mathbb{C}P^1,\mathbb{C}P^2, \cdots ]
$$

$$
  \Omega^{SO}_\bullet\otimes \mathbb{Q} \simeq \mathbb{Q}[\mathbb{C}P^2,\mathbb{C}P^4, \cdots ]
$$

whose generators are identified with the cobordism classes of the manifolds which are the complex [[projective spaces]], as indicated.

### Logarithm and Characteristic series 
 {#LogarithmAndCharacteristicSeries}

#### Definition in components

Given a (rational) genus $\phi \colon \Omega^{U,SU}_\bullet\otimes \mathbb{Q} \to R \otimes \mathbb{Q}$ one defines (we follow ([Hopkins 94](#Hopkins94)))

1. its _logarithm_ to be the [[formal power series]] over $R \otimes \mathbb{Q}$ given by

   $$
     log_\phi(z) \coloneqq \sum_{n \in \mathbb{N}} \phi(\mathbb{C}P^n) \frac{z^{n+1}}{n+1};
   $$

1. its _characteristic series_ (or _Hirzebruch series_) to be the formal power series over $R \otimes \mathbb{Q}$

   $$
     K_\phi(z) \coloneqq \frac{z}{\exp_\phi(z)}
     \,,
   $$

   where $\exp_\phi$ is the inverse of the logarithm;

1. its _characteristic class_ as the [[universal characteristic class]] which via the [[splitting principle]] is fixed by its value on the universal line bundle as

   $$
     K_\phi(c_1) \in H^\bullet(B U(1),R \otimes \mathbb{Q})
   $$

   where $c_1 \in H^2(B U(1), \mathbb{Z})$ denotes the universal [[first Chern class]]; hence its value on a [[direct sum]]  $L_1 \oplus \cdots \oplus L_k$ of [[complex line bundles]] is

   $$
     \prod_{i} K_\phi(c_1(L_i))
     \,.
   $$

#### Definition via orientations in generalized cohomology
 {#HirzebruchSeriesViaOrientationsInGeneralizedCohomology}

Suppose that the given genus $\Omega_\bullet^{SO} \longrightarrow R$ indeed comes from an [[orientation in generalized cohomology]] (as discussed [above](#InStableHomotopyTheory)) hence from a [[homomorphism]] of [[E-∞ rings]]

$$
  \beta \;\colon\;  M SO \longrightarrow E
$$

for an [[E-∞ ring]] $E$ with [[homotopy groups]] $R\simeq \pi_\bullet(E)$.
(And suppose that $E$ defines a [[complex oriented cohomology theory]].)


This defines ([Ando-Hopkins-Rezk 10, prop. 2.11](#AndoHopkinsRezk10))
a universal [[orientation in generalized cohomology|orientation]] of real vector bundles and hence of [[complex vector bundles]] and hence of [[complex line bundles]] in $E$-cohomology

$$

  \beta \;\colon\; M U \longrightarrow M SO \stackrel{\beta}{\longrightarrow} E
  \,.
$$

Now rationally, i.e. for $E\otimes \mathbb{Q}$, there is a canonical such orientation, given by the composite

$$
  \alpha \;\colon\; M U \longrightarrow M SO \longrightarrow H \mathbb{Q} \simeq \mathbb{S}\otimes \mathbb{Q} \stackrel{}{\longrightarrow} E \otimes \mathbb{Q}
  \,.
$$

Thus, given any orientation $\beta$, its rationalization may be compared to $\alpha$. Since these rational orientations are equivalently trivializations of maps to $B GL_1(E \otimes \mathbb{R})$, their difference is a class $\beta/\alpha$ with coefficients in $GL_1(E\otimes R)$, hence over any space $X$ the difference is a class in $H^0(X, \pi_\bullet E\otimes \mathbb{Q})^\times$.

Specifically consider the [[delooping]] $X= B U(1)$ of the [[circle group]].
For this the [[cohomology ring]] is the [[power series]] ring in a single [[variable]] (the universal [[first Chern class]] $c_1(L)$).
Under the canonical inclusion $B U(1)\to B U$ both the above orientations $\beta$ and $\alpha$ pull back, so that we have a difference 

$$
  K_\beta \coloneqq \beta/\alpha \in (E_\bullet \otimes \mathbb{Q})[ [ c_1(L) ] ]
  \,.
$$

This is the Hirzebruch series of $\beta$ ([Ando-Hopkins-Rezk 10, def. 3.10](#AndoHopkinsRezk10)).

If $F$ denotes the [[formal group law]] classified via $MU_\bullet \to M SO_\bullet \stackrel{\beta_\bullet}{\to} E_\bullet$ then 

$$
  K_\beta(z) = \frac{z}{\exp_F(z)}
$$


### The Hirzebruch formula
 {#HirzebruchFormula}

The central theorem of ([Hirzebruch 66](#Hirzebruch66)) expresses the genus of an arbitrary ([[cobordism class]] of a) manifold $X$ of [[dimension]] $2n$ via the formula

$$
  \phi(X)
  =
  \langle \prod_{i = 1}^n K_\phi(x_i(T X)), [X] \rangle
$$

in terms of the Hirzebruch characteristic series $K_\phi$ discussed [above](#LogarithmAndCharacteristicSeries), and via the [[splitting principle]]:

This means that $\prod_{i = 1}^n K_\phi(x_i(T X))$ is the function of [[Chern classes]] $c_k$ (i.e. [[Pontryagin classes]] $P_{2k}$ and [[Euler classes]] $\chi$) obtained by rewriting the [[polynomial]] in the $x_i$ (the "[[Chern roots]]") as a polynomial in [[elementary symmetric polynomials]] $\sigma_k(x_1,\cdots, x_n)$ and then substituting for each of these by $c_k(T X)$.

(see also e.g. [ManifoldAtlas -- Genera -- 4.1 Construction](http://www.map.mpim-bonn.mpg.de/Formal_group_laws_and_genera#Construction)).

## Examples

### Todd genus

The [[Todd genus]] is the genus with logarithm

$$
  -log_{Todd}(1-x) = \sum_{n \in \mathbb{N}} \frac{x^n}{n}
$$


### Signature genus

The [[signature genus]];

### $\hat A$-genus
 {#AhatGenus}

The [[A-hat genus]] is the [[index of a Dirac operator]] coming from a [[spin bundle]] in KO-theory. It is given by the characteristic series

The [characteristic series](genus#LogarithmAndCharacteristicSeries) of the $\hat A$-genus is

$$
  \begin{aligned}
    K_{\hat A}(e)
     & =
    \frac{z}{e^{z/2} - e^{-z/2}}
    \\
     &= 
    \exp\left(
       - \sum_{k \geq 2} \frac{B_k}{k} \frac{z^k}{k!}
     \right)
  \end{aligned}
  \,,
$$

where $B_k$ is the $k$th [[Bernoulli number]] ([Ando-Hopkins-Rezk 10, prop. 10.2](#AndoHopkinsRezk10)).

The $\hat A$-genus is an [[integer]] on manifolds with [[spin structure]].


### Elliptic genus 

An [[elliptic genus]] is one whose logarithm is given by

$$
  log_{ell}(z) = \int_0^z (1-2 \delta t^2 + \epsilon t^4)^{-1/2} d t
$$

for constants $\delta, \epsilon$ with non-degenerate values $\delta^2 \neq \epsilon$ and $\epsilon = 0$. 

For degenerate choices this reproduces the [[signature genus]] and the [[A-hat genus]] above, see at _[[elliptic genus]]_ for more. For non-degenerate values one may regard $\epsilon$ and $\delta$ as values of [[modular forms]] of the same name and hence regard all elliptic genera together as one single genus with [[coefficients]] in $MF_\bullet(\Gamma_0(2))$. This "universal" elliptic genus is the _[[Witten genus]]_.

### Witten genus

The  [[Witten genus]] 

$$
  w \colon \Omega^{SO}_\bullet \longrightarrow \mathbb{Q}[ [q] ]
$$

is the genus with [[coefficients]] in
the [[power series]] ring $\mathbb{Q}[ [ q ] ]$ 
with characteristic series given by

$$
  \begin{aligned}
    K_w(z)
    & =
    \frac{z/2}{sinh(z/2)}
    \prod_{n \geq 1}
    \frac{(1-q^n)^2}{(1-q^n e^z)(1-q^n e^{-z})}
    \\
    & = 
    \exp\left(
      \sum_{k \geq 2} G_k \frac{z^k}{k!}
    \right)
  \end{aligned}
  \,,
$$

where $G_k$ are the [[Eisenstein series]] ([Ando-Hopkins-Strickland 01](AndoHopkinsStrickland01), [Ando-Hopkins-Rezk 10, prop. 10.9](#AndoHopkinsRezk10)). (Notice that the constant term in $G_k$ is proportional to the $k$th [[Bernoulli number]], so that indeed the exponential expression matches that for the [A-hat genus above](#AhatGenus).)


On [[manifolds]] with [[spin structure]] the Witten genus takes values in $\mathbb{Z}[ [ q ] ]$ 

On manifolds with rational [[string structure]] it takes values in (the $q$-expansion of) [[modular forms]] for $SL_2(\mathbb{Z})$, meaning that setting $q = e^{2 \pi i \tau}$ then as a function $f$ of the parameter $\tau$ taking values in the [[upper half plane]] the Witten genus satisfies

$$
  f(-1/\tau) = (-\tau)^n f(\tau)
  \,.
$$

Finally on manifolds with actual [[string structure]] it takes values in [[topological modular forms]]. See at _[[Witten genus]]_ for more.

## Non-examples 

### Euler characteristic

The [[Euler characteristic]] $X \mapsto \chi(X)$ is close to being  a genus, but is _not_ [[cobordism]] invariant
  
  (this is the [[index]] of the [[Dirac operator]] $D = d + d^\dagger$)


## Related concepts
 {#RelatedConcepts}

[[!include genera and partition functions - table]]


## References

The abstract concept of genus is due to [[Friedrich Hirzebruch]]. It had evolved out of the older concept of (arithmetic) [[genus of a surface]] via the concept of [[Todd genus]] introduced in

* [[John Arthur Todd]], _The arithmetical invariants of algebraic loci_, Proc. London Math. Soc. (2), Ser. 43, 1937,
190&#8211;225.

An review of the history is at the beginning of ([Hirzebruch-Kreck 09](#HirzebruchKreck09))

The theory of multiplicative sequences and characteristic series of genera is due to

* {#Hirzebruch56} [[Friedrich Hirzebruch]], *Neue topologische Methoden in der algebraischen Geometrie*, Ergebnisse der Mathematik und ihrer Grenzgebiete **9**, Springer (1956) &lbrack;[doi:10.1007/978-3-662-41083-7](https://doi.org/10.1007/978-3-662-41083-7)&rbrack;

* {#Hirzebruch66} [[Friedrich Hirzebruch]], *Topological methods in algebraic geometry*, Grundlehren **131**, Springer (1966) &lbrack;[doi:10.1007/978-3-642-62018-8](https://doi.org/10.1007/978-3-642-62018-8), MR0202713 (34 #2573) Zbl 0843.14009&rbrack;

Early review:

* {#HirzebruchGergerJung92} [[Friedrich Hirzebruch]], Thomas Berger, Rainer Jung, chapter 2 of: *Manifolds and Modular Forms*, Aspects of Mathematics **20**, Viehweg (1992), Springer (1994) &lbrack;[doi:10.1007/978-3-663-10726-2](https://doi.org/10.1007/978-3-663-10726-2), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/hirzjung.pdf)&rbrack;


Further review:

* [[Serge Ochanine]], _What is... an elliptic genus_?, Notices of the AMS, volume 56, number 6 (2009) ([pdf](http://www.ams.org/notices/200906/rtx090600720p.pdf))

* {#HirzebruchKreck09} [[Friedrich Hirzebruch]], [[Matthias Kreck]], _On the concept of genus in topology and complex analysis_, Notices of the AMS, volume 56, number 6 (2009) [pdf](http://www.ams.org/notices/200906/rtx090600713p.pdf)

* {#Hopkins94} [[Michael Hopkins]], section 2 of _Topological modular forms, the Witten Genus, and the theorem of the cube_, Proceedings of the International Congress of Mathematics, Z&#252;rich 1994 ([pdf](http://www.mathunion.org/ICM/ICM1994.1/Main/icm1994.1.0554.0565.ocr.pdf))

* Manifold Atlas, _[Formal group laws and genera](http://www.map.mpim-bonn.mpg.de/Formal_group_laws_and_genera)_

* Wikipedia, _[Genus of a multiplicative series](http://en.wikipedia.org/wiki/Genus_of_a_multiplicative_sequence)_

* [](wwwmath.uni-muenster.de/reine/inst/lueck/lehre/.../summary6.)

Discussion in terms of [[orientations in generalized cohomology]] and specifically for the [[A-hat genus]] and the [[Witten genus]] is in

* {#AndoHopkinsStrickland01} [[Matthew Ando]], [[Michael Hopkins]], [[Neil Strickland]], _Elliptic spectra, the Witten genus and the theorem of the cube_, Invent. Math. 146 (2001) 595&#8211;687 MR1869850

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))

[[!redirects genera]]

[[!redirects Hirzebruch series]]