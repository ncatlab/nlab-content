
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

Modular forms are also often called _classical [[automorphic forms]]_, see [below]()



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



### As sections of a line bundle over the moduli stack
 {#AsSections}

More abstractly, for $\mathcal{M}_{ell}$ the [[moduli stack of elliptic curves]] (or rather its [[Deligne-Mumford compactification]]) and $A \to \mathcal{M}_{ell}$ the corresponding universal bundle, write $\Omega^1_{A/S}$ for the [[line bundle]] of fiberwise [[Kähler differential forms]]. Write $e$ for the 0-[[section]] of this line bundle. Then

$$
  \omega \coloneqq e^\ast \Omega^1_{A/S}
$$ 

is a [[line bundle]] over the [[moduli stack of elliptic curves]]. A modular form of weight $k$  is a [[section]] of $\omega^{\otimes k}$


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

* [[Jacobi form]]

* [[elliptic genus]], [[Witten genus]]

* [[topological modular form]], [[tmf]]

* generalization to functions on moduli of higher dimensional [[abelian varieties]]: [[Hilbert modular form]], [[Siegel modular forms]]

* [[modularity theorem]]
* [[Rankin-Cohen bracket]]

## References

A basic and handy reference is

* [[Pierre Deligne]], _Courbes elliptiques: formulaire d'apres J. Tate_, In _Modular functions of one variable_, IV (Proc. Internat. Summer School, Univ. Antwerp, Antwerp, 1972), pages 53{73. Lecture Notes in Math., Vol. 476. Springer, Berlin, 1975 ([web](http://modular.math.washington.edu/Tables/antwerp/deligne/))

Textbook accounts include

* N. Koblitz, _Introduction to Elliptic Curves and Modular Forms_, Graduate Texts in Math, vol. 97, Springer-Verlag, 1984, 1993 (2nd ed.).

Lecture notes and reviews include

* {#Hain08} Richard Hain, section 4 of _Lectures on Moduli Spaces of Elliptic Curves_ ([arXiv:0812.1803](http://arxiv.org/abs/0812.1803))


* [[Charles Rezk]], section 10 of [pdf](http://www.math.uiuc.edu/~rezk/512-spr2001-notes.pdf)

* {#Litt} [[Daniel Litt]], _Automorphic forms notes, part I_ ([pdf](http://math.stanford.edu/~dlitt/Talks/automorphicformspt1.pdf))


* Jan Hendrik Bruinier, Gerard van der Geer, [[Günter Harder]], Don Zagier, _The 1-2-3 of modular forms_, Lectures at a Summer School 2004 in Nordfjordeid, Norway; Universitext, Springer 2008.

* [[Nora Ganter]], _[Topological modular forms literature list](http://www.ms.unimelb.edu.au/~nganter/talbot/index.html)_

* {#Martin13} Kimball Martin, _A brief overview of modular and automorphic forms_, 2013 [pdf](http://www2.math.ou.edu/~kmartin/papers/mfs.pdf)


* Wikipedia, _[Modular form](http://en.wikipedia.org/wiki/Modular_form)_

Original discussion in the context of [[elliptic genera]] and [[elliptic cohomology]] includes

* {#LandweberRavenelStong93} [[Peter Landweber]], [[Douglas Ravenel]], [[Robert Stong]], _Periodic cohomology theories defined by elliptic curves_, in [[Haynes Miller]] et. al. (eds.), _The Cech centennial: A conference on homotopy theory_, June 1993, AMS (1995) ([pdf](http://www.math.sciences.univ-nantes.fr/~hossein/GdT-Elliptique/Landweber-Ravenel-Stong.pdf))

* {#Landweber88} [[Peter Landweber]], _Elliptic Cohomology and Modular Forms_, in _Elliptic Curves and Modular Forms in Algebraic Topology_, Lecture Notes in Mathematics Volume 1326, 1988, pp 55-68 ([[LandweberEllipticModular.pdf:file]])

Reviews of this include

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