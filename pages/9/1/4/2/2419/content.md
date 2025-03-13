
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _modular form_  is a [[holomorphic function]] on the [[upper half-plane]] that satisfies certain transformation property under the [[action]] of the [[modular group]]. Abstractly this transformation property makes the function a [[section]] of a certain [[line bundle]] on the [[quotient]] of the [[upper half plane]] that makes it the [[moduli stack of elliptic curves]] (over the [[complex numbers]]) or more generally a [[modular curve]].

Modular forms are also often called _classical [[automorphic forms]]_, see [below](). As automorphic forms, they are related to Galois representations as part of the [[Langlands program]].

Modular forms appear as the [[coefficient]] ring of the [[Witten genus]] on manifolds with rational [[string structure]]. For manifolds with actual [[string structure]] this refines to [[topological modular forms]], which are the [[homotopy groups]] of the [[spectrum]] [[tmf]].


## Definition

### In components

+-- {: .num_defn}
###### Definition

An **(integral) [[modular form]]** of weight $w$ is a [[holomorphic function]] on the [[upper half-plane]]

$$
  f : (\mathbb{R}^2)_+ \hookrightarrow \mathbb{C}
$$

(complex numbers with strictly positive imaginary part) 

such that

1. if $A = \left( \array{a & b \\ c& d}\right) \in SL_2(\mathbb{Z})$ acting by $A : \tau \mapsto = \frac{a \tau + b }{c \tau + d}$ we have
 
   $$
     f(A(\tau)) = (c \tau + d)^w f(\tau)
   $$

   (notice that for $A = \left( \array{1 & 1 \\ 0& 1}\right)$ then  $f(\tau + 1) = f(\tau)$)

1. $f$ has at worst a pole at $\{0\}$ (for _weak_ modular forms this condition is relaxed)

   it follows that $f = f(q)$ with $q = e^{2 \pi i \tau}$ is a meromorphic funtion on the open disk.


1. **integrality** $\tilde f(q) = \sum_{k = -N}^\infty a_k \cdot q^k$ then $a_k \in \mathbb{Z}$

=--

More generally there is such a definition for $SL(2,\mathbb{Z})$ replaced by any other arithmetic subgroup $\Gamma \subset SL(2,\mathbb{R})$ (e.g. [Litt, def.1](#Litt)), giving modular forms on [[modular curves]].

### As functions on lattices

The reference for this definition  is [Calegari13](#Calegari13).

A modular form $f$ of weight $k$ over $\mathbb{C}$ is a function on lattices $\Lambda=\mathbb{Z}+\tau\mathbb{Z}\subset \mathbb{C}$ such that

1. $f(\mathbb{Z}+\tau\mathbb{Z})$ is holomorphic as a function of $\tau$

2. $f(\mu \Lambda)=\mu^{-k} f(\Lambda)$ for all $\mu\in\mathbb{C}^{\times}$

3. $f(\mathbb{Z}+\tau\mathbb{Z})$ is bounded as $\tau\to i\infty$.

If $f(\mathbb{Z}+\tau\mathbb{Z})\to 0$ as $\tau\to i\infty$, we say that $f$ is a [[cusp form]].

### As functions on elliptic curves together with a choice of differential

Again the reference for this definition  is [Calegari13](#Calegari13).

Since [[elliptic curves]] over $\mathbb{C}$ can be defined in terms of lattices, the previous definition can also be expressed as follows.

A modular form $f$ of weight $k$ over $\mathbb{C}$ is a function on pairs $(E,\omega)$ where $E$ is an elliptic curve and $\omega\in H^{0}(E,\Omega_{E}^{1})$, such that

$$f(E,\mu\omega)=\mu^{-k}f(E,\omega)$$

and such that $f(\mathbb{C}/\mathbb{Z}+\tau\mathbb{Z})$ is bounded as $\tau\to i\infty$.

### As sections of a line bundle over the moduli stack
 {#AsSections}

More abstractly, for $\mathcal{M}_{ell}$ the [[moduli stack of elliptic curves]] (or rather its [[Deligne-Mumford compactification]]) and $A \to \mathcal{M}_{ell}$ the corresponding universal bundle, write $\Omega^1_{A/S}$ for the [[line bundle]] of fiberwise [[Kähler differential forms]]. Write $e$ for the 0-[[section]] of this line bundle. Then

$$
  \omega \coloneqq e^\ast \Omega^1_{A/S}
$$ 

is a [[line bundle]] over the [[moduli stack of elliptic curves]]. A modular form of weight $k$  is a [[section]] of $\omega^{\otimes k}$. Using the Kodaira-Spencer isomorphism one can show that the space of [[cusp forms]] of weight $2$ are the differentials on the corresponding modular curve.


### For congruence subgroups
 {#ForCongruenceSubgroups}

Similarly one considers modular forms for [[congruence subgroups]] of the full [[modular group]], hence on the space of [[elliptic curves with level structure]].

### As automorphic forms
 {#AsAutomorphicForms}

Instead of regarding, as [above](#AsSections), modular forms as [[sections]] of a [[line bundle]] on a [[quotient]] of the [[upper half plane]], one may regard them alternatively as plain functions, but on the ([[Möbius group|projective]]) [[special linear group]] $SL(2,\mathbb{R})$. (e.g. [Martin 13, section 2](Martin13), [Litt, section 2](#Litt)).

As such these functions are then invariant under the [[action]] of the [[modular group|modular]] [[subgroup]] $SL(2,\mathbb{Z})\hookrightarrow SL(2,\mathbb{R})$ and hence are really functions on the [[coset space]] $SL(2,\mathbb{R})/SL(2,\mathbb{Z})$ (for forms on moduli of elliptic curves) or more generally $\Gamma \backslash SL(2,\mathbb{Z})$ (for forms on more general [[modular curves]]).

This generalizes to the case of other [[congruence subgroups]] (as [above](ForCongruenceSubgroups)). Generally such functions on [[coset spaces]] like this are called _[[automorphic forms]]_. See there for more.

For the history of the terminology "modular form"/"automorphic form" see also [this MO comment](http://mathoverflow.net/a/124785/381).

## Properties

### Action by Hecke operators

Modular forms can be acted on by Hecke operators (related to [[Hecke correspondence]]). Viewing a modular form as a function on lattices, the most common kind of Hecke operator $T_{n}$ acts on a modular form $f$ as follows:

$$T_{n}f(\Lambda)=\sum_{\Lambda'}f(\Lambda')$$

where the sum runs over all lattices $\Lambda'$ which are index $n$ subgroups of $\Lambda$. A modular form which is a simultaneous eigenvector is also called a _Hecke eigenform_ or simply _eigenform_.

A modular form which vanishes at the cusps (equivalently, whose zeroth Fourier coefficient is equal to $0$) is called _cuspidal_, or a [[cusp form]]. A cusp form is _normalized_ if its first Fourier coefficient is equal to $1$. For normalized cuspidal eigenforms of integer weight, the eigenvalue of the Hecke operator $T_{n}$ is exactly the $n$-th Fourier coefficient.

Hecke operators were first developed by [[Louis Mordell]] to study the conjectures of [[Srinivasa Ramanujan]] on the tau function (the Fourier coefficients of the modular discriminant). They were later developed by (and named after) [[Erich Hecke]] who used them to study [[L-functions]].

### Analytic continuation of L-functions

Given a cusp form $f$ of weight $k$ with Fourier expansion

$$f(z)=\sum_{n=1}^{\infty}a_{n}e^{2\pi i n z}$$

we can associate to it its L-function $L(f,s)$, which is given by

$$L(f,s)=\sum_{n=1}^{\infty}a_{n}n^{-s}$$

Alternatively the L-function $L(f,s)$ can be defined via the [[Mellin transform]] of $f$:

$$\Lambda(f,s)=(2\pi)^{-s}\Gamma(s)L(f,s)=\int_{0}^{\infty}f(iy)y^{s}d^{\times}$$

The L-function $L(f,s)$ has an analytic continuation to all of $\mathbb{C}$.

This is important for instance to formulate conjectures such as the [[Birch and Swinnerton-Dyer conjecture]], which involves the special value of the [[Hasse-Weil L-function]] $L(E,s)$ of an elliptic curve at a value of $s$ where it is originally not defined (the series only converges for $s \gt 3/2$). But the [[modularity theorem]] tells us that this Hasse-Weil L-function $L(E,s)$ is equal to the L-function of some cusp form $f$, which we know has an analytic continuation to the entire complex plane.
 
### Relation to Galois representations

Modular forms can be used to construct [[Galois representations]]. For instance in the case of weight $2$ 
normalized eigenforms this is the Eichler-Shimura construction discussed in [DiamondShurman05, chapter 9](#DiamondShurman05). This was generalized to higher weight in [Deligne71](#Deligne71), and the case of weight $1$ comes from the work of [DeligneSerre74](#DeligneSerre74).

The problem of whether a Galois representation comes from some modular form is part of the problem of _modularity_. Known cases include the [[modularity theorem]] of [TaylorWiles95](#TaylorWiles95) and [BreuilConradDiamondTaylor2001](#BreuilConradDiamondTaylor2001). The former is notably an important part of [[Wiles' proof of Fermat's last theorem]]. 

On a more general level, as modular forms are a special case of automorphic forms, their relation to Galois representations is part of the [[Langlands program]].

### Relation of $MF_0(2)$ to the elliptic genus

Write $\Gamma_0(2) \hookrightarrow SL_2(\mathbb{Z})$ for the [[subgroup]] of the [[modular group]] on those elements $\left(\array{a & b \\ c & d}\right)$ for which $c = 0\, mod\, 2$.

A modular function for $\Gamma_0(2)$ is a [[meromorphic function]] on the [[upper half plane]] which transforms as a modular form under the action of $\Gamma_0(2) \hookrightarrow SL_2(\mathbb{Z})$. Write $MF_\bullet(\Gamma_0(2))$ for the ring of these.

There is a natural isomorphism

$$
  MF_\bullet(\Gamma_0(2)) \simeq \mathbb{C}[\epsilon, \delta]
$$

(see at [[elliptic genus]]) for the notation.

([Landweber-Ravenel-Stong 93, theorem 1.5 and sections 5.3, 5.8](#LandweberRavenelStong93))

### Relation to elliptic cohomology

For $E$ the [[elliptic cohomology theory]] associated to the [[elliptic curve]] $C$, then 

$$
  E_{2n} \simeq \omega(C)^{\otimes n}
$$

(where $\omega$ is the line bundle from [above ](#AsSections))

and 

$$
  E_{2n+1}\simeq 0
  \,.
$$


## Examples

* [[Eisenstein series]]

* [[j-invariant]]

* [[Weierstrass sigma-function]]

* [[Dedekind eta function]]


## Related concepts

* [[modular group]]

* [[elliptic curve]], [[moduli stack of elliptic curves]]

* [[Hecke correspondence]]

* [[Jacobi form]]

* [[elliptic genus]], [[Witten genus]]

* [[topological modular form]], [[tmf]]

* [[p-adic modular form]]

* generalization to functions on moduli of higher dimensional [[abelian varieties]]: [[Hilbert modular form]], [[Siegel modular forms]]

* [[modularity theorem]]

* [[Rankin-Cohen bracket]]

## References

A basic and handy reference is

* [[Pierre Deligne]], _Courbes elliptiques: formulaire d'apres J. Tate_, In _Modular functions of one variable_, IV (Proc. Internat. Summer School, Univ. Antwerp, Antwerp, 1972), pages 53{73. Lecture Notes in Math., Vol. 476. Springer, Berlin, 1975 ([web](http://modular.math.washington.edu/Tables/antwerp/deligne/))

Textbook accounts:

* [[Jean-Pierre Serre]], chapter VII of: *A Course in Arithmetic*, Graduate Texts in Mathematics **7**, Springer (1973) &lbrack;[doi:10.1007/978-1-4684-9884-4](https://doi.org/10.1007/978-1-4684-9884-4), [pdf](https://www.math.purdue.edu/~jlipman/MA598/Serre-Course%20in%20Arithmetic.pdf)&rbrack;


* N. Koblitz, _Introduction to Elliptic Curves and Modular Forms_, Graduate Texts in Math. **97** Springer (1984, 1993) 

* {#HirzebruchGergerJung92} [[Friedrich Hirzebruch]], Thomas Berger, Rainer Jung, Appendix I of: *Manifolds and Modular Forms*, Aspects of Mathematics **20**, Viehweg (1992), Springer (1994) &lbrack;[doi:10.1007/978-3-663-10726-2](https://doi.org/10.1007/978-3-663-10726-2), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/hirzjung.pdf)&rbrack;

* {#DiamondShurman05} [[Fred Diamond]], [[Jerry Shurman]], *A First Course in Modular Forms*, GTM **228**, Springer (2005) &lbrack;[doi:10.1007/978-0-387-27226-9](https://doi.org/10.1007/978-0-387-27226-9), ISBN-13: 978-0387232294&rbrack; 

* [[William Stein]]: *Modular Forms, a Computational Approach*, Graduate Studies in Mathematics **79**, AMS (2007) &lbrack;[doi:10.1090/gsm/079](https://doi.org/10.1090/gsm/079)&rbrack;

Lecture notes and reviews:

* {#Hain08} [[Richard Hain]], section 4 of: _Lectures on Moduli Spaces of Elliptic Curves_ &lbrack;[arXiv:0812.1803](http://arxiv.org/abs/0812.1803)&rbrack;

* [[Charles Rezk]], section 10 of [pdf](http://www.math.uiuc.edu/~rezk/512-spr2001-notes.pdf)

* {#Litt} [[Daniel Litt]], _Automorphic forms notes, part I_ ([pdf](http://math.stanford.edu/~dlitt/Talks/automorphicformspt1.pdf))

* Jan Hendrik Bruinier, Gerard van der Geer, [[Günter Harder]], Don Zagier, _The 1-2-3 of modular forms_, Lectures at a Summer School 2004 in Nordfjordeid, Norway; Universitext, Springer 2008.

* [[Nora Ganter]], _[Topological modular forms literature list](http://www.ms.unimelb.edu.au/~nganter/talbot/index.html)_

* {#Martin13} Kimball Martin, _A brief overview of modular and automorphic forms_, 2013 [pdf](http://www2.math.ou.edu/~kmartin/papers/mfs.pdf)

* {#Calegari13} Frank Calegari, _Congruences between modular forms_, 2013 [pdf](https://swc-math.github.io/aws/2013/2013CalegariLectureNotes.pdf)

* [[Joachim Wehler]]: *Modular Forms and Elliptic Curves* (2021) &lbrack;[pdf](https://www.mathematik.uni-muenchen.de/~wehler/ModularFormsScript.pdf)&rbrack;

* Wikipedia, _[Modular form](http://en.wikipedia.org/wiki/Modular_form)_

Introduction in relation to [[string theory]]:

* [[Eric D'Hoker]], [[Justin Kaidi]], *Lectures on modular forms and strings* &lbrack;[arXiv:2208.07242](https://arxiv.org/abs/2208.07242)&rbrack;



The work of Erich Hecke:

* [[Erich Hecke]], *Über Modulfunktionen und die Dirichletschen Reihen mit Eulerscher Produktentwicklung. I.*, Mathematische Annalen **114** (1937)  1–28 &lbrack;[doi:10.1007/BF01594160](https://doi.org/10.1007/BF01594160)&rbrack;

* [[Erich Hecke]], *Über Modulfunktionen und die Dirichletschen Reihen mit Eulerscher Produktentwicklung. II.*, Mathematische Annalen (in German), **114** (1937) 316–351 &lbrack;[doi:10.1007/BF01594180](https://doi.org/10.1007/BF01594180)&rbrack;

The construction of Galois representations associated to normalized eigenforms of weight $\geq 2$ comes from

* {#Deligne71}[[Pierre Deligne]], _Formes modulaires et représentations l-adiques_, Sém. Bourbaki 1968/69, exp. 355, Springer Lecture Notes 179 (1971), 139–172

The construction of Galois representations from weight $1$ modular forms comes from

* {#DeligneSerre74}[[Pierre Deligne]] and [[Jean-Pierre Serre]] _Formes modulaires de poids 1_ Ann. Sci. Ecole Norm. Sup. (4), 7:507–530 (1975), 1974.

References related to the modularity theorem are

* {#TaylorWiles95} [[Richard Taylor]], [[Andrew Wiles]], *Ring-Theoretic Properties of Certain Hecke Algebras*, Annals of Mathematics Second Series **141** 3 (1995) 553-572 $[$[doi:10.2307/2118560 ](https://doi.org/10.2307/2118560 )$]$

* {#BreuilConradDiamondTaylor2001} [[Christophe Breuil]], [[Brian Conrad]], [[Fred Diamond]], [[Richard Taylor]], *On the modularity of elliptic curves over $\mathbf{Q}$: Wild 3-adic exercises*, Journal of the American Mathematical Society **14** 4 (2001) 843–939 $[$[doi:10.1090/S0894-0347-01-00370-8](https://doi.org/10.1090/S0894-0347-01-00370-8)$]$

Original discussion in the context of [[elliptic genera]] and [[elliptic cohomology]] includes

* {#LandweberRavenelStong93} [[Peter Landweber]], [[Douglas Ravenel]], [[Robert Stong]], _Periodic cohomology theories defined by elliptic curves_, in [[Haynes Miller]] et. al. (eds.), _The Cech centennial: A conference on homotopy theory_, June 1993, AMS (1995) ([pdf](http://www.math.sciences.univ-nantes.fr/~hossein/GdT-Elliptique/Landweber-Ravenel-Stong.pdf))

* {#Landweber88} [[Peter Landweber]], *Elliptic Cohomology and Modular Forms*, in: _Elliptic Curves and Modular Forms in Algebraic Topology_, Lecture Notes in Mathematics **1326** (1988) 55-68 &lbrack;[doi:10.1007/BFb0078038](https://doi.org/10.1007/BFb0078038)&rbrack;

Reviewed in:

* [[Kefeng Liu]], _Modular forms and topology_, 1996 ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.130.9779))

[[!redirects modular forms]]

[[!redirects integral modular form]]
[[!redirects weak modular form]]
[[!redirects modular function]]
[[!redirects integral modular function]]
[[!redirects weak integral modular form]]

[[!redirects integral modular forms]]
[[!redirects weak modular forms]]
[[!redirects modular functions]]
[[!redirects integral modular functions]]
[[!redirects weak integral modular forms]]