
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

# Serre functor
* table of contents
{: toc}


## Idea


A *Serre functor* on a [[triangulated category]] $\mathcal{A}$ is an [[exact functor]] such that for any [[pair]] of [[objects]] there is a [[natural isomorphism]] $\Hom(A,B) \simeq \Hom(B,S(A))^{\ast}$ from their [[hom-object]] to the [[linear dual]] of their reverse hom-object, "twisted" by the Serre functor. 

A Serre functor does not always exist, but when it does then it is unique up to graded natural isomorphism.

The notion of Serre functors was introduced by [Bondal & Kapranov 1989](#BondalKapranov89) to study [[admissible subcategories]] of [[triangulated categories]].  

Serre functors have become a powerful tool for working with the [[derived category]] of [[coherent sheaves]] on a [[variety]].

## Definition

In the original paper, the following definition was given.

+-- {: .num_defn}
###### Definition
Let $\mathcal{A}$ be a $k$-linear triangulated category with finite-dimensional [[Hom]]'s and $k$ algebraically closed.  A **Serre functor** $S : \mathcal{A} \to \mathcal{A}$ is an additive equivalence that commutes with the translation functor, with [[natural isomorphisms|natural]] (in both variables) [[isomorphisms]] $\phi_{A,B} \colon \Hom_\mathcal{A}(A,B) \stackrel{\sim}{\to} \Hom_{\mathcal{A}}(B,S(A))^*$ for any objects $A$ and $B$, such that the composite
  \[ (\phi^{-1}_{B, S(A)})^* \circ \phi_{A,B} : \Hom(A,B) \to \Hom(B,S(A))^* \to \Hom(S(A), S(B)) \]
coincides with the isomorphism induced by $S$.
=--

In fact, the last commutativity condition can be deduced from just the [[natural transformation|naturality]] of $\phi_{A,B}$, and commutativity with the translation functor also follows from a proposition below.  Hence, the following definition is seen in later papers.

+-- {: .num_defn}
###### Definition
Let $\mathcal{A}$ be a $k$-linear category with finite-dimensional [[Hom]]'s and $k$ an arbitrary field.  A **Serre functor** $S : \mathcal{A} \to \mathcal{A}$ is an additive equivalence with bi-functorial isomorphisms $\phi_{A,B} : \Hom_\mathcal{A}(A,B) \stackrel{\sim}{\to} \Hom_{\mathcal{A}}(B,S(A))^*$ for any objects $A$ and $B$.
=--

Of course, formally the definition could be used in categories enriched over a symmetric monoidal category with a sufficiently nice involution.

## Examples

+-- {: .num_example}
###### Example
In the [[derived category]] of [[finite-dimensional vector spaces]] over $k$, the identity functor is a Serre functor.
=--

+-- {: .num_example}
###### Example
In the derived category of [[coherent sheaves]] on a smooth projective [[variety]] $X$, the functor $(\cdot \otimes \omega_X)[n]$ is a Serre functor, in view of [[Serre-Grothendieck duality]], where $\omega_X$ is the [[canonical sheaf]] and $n$ is the dimension of $X$.
=--

## Properties

+-- {: .num_prop}
###### Proposition
Any autoequivalence $F : \mathcal{A} \to \mathcal{A}$ commutes with a Serre functor: there is a natural graded isomorphism of functors $F \circ S \stackrel{\sim}{\to} S \circ F$.
=--

+-- {: .num_prop}
###### Proposition
Any Serre functor in a [[graded category]] is [[graded]].
=--

+-- {: .num_prop}
###### Proposition
Any Serre functor in a [[triangulated category]] is [[exact]] (i.e. [[distinguished triangles]] are mapped to distinguished triangles).
=--

+-- {: .num_prop}
###### Proposition
Any two Serre functors are connected by a canonical graded functorial isomorphism that commutes with the isomorphisms $\phi_{A,B}$ in the definition of the Serre functor.
=--

## References

The original paper and English translation:

* {#BondalKapranov89}  &#1040;. &#1048;. &#1041;&#1086;&#1085;&#1076;&#1072;&#1083;, &#1052;. &#1052;. &#1050;&#1072;&#1087;&#1088;&#1072;&#1085;&#1086;&#1074;, _&#1055;&#1088;&#1077;&#1076;&#1089;&#1090;&#1072;&#1074;&#1080;&#1084;&#1099;&#1077; &#1092;&#1091;&#1085;&#1082;&#1090;&#1086;&#1088;&#1099;, &#1092;&#1091;&#1085;&#1082;&#1090;&#1086;&#1088;&#1099; &#1057;&#1077;&#1088;&#1088;&#1072; &#1080; &#1087;&#1077;&#173;&#1088;&#1077;&#1089;&#1090;&#1088;&#1086;&#1081;&#1082;&#1080;_, &#1048;&#1079;&#1074;. &#1040;&#1053; &#1057;&#1057;&#1057;&#1056;. &#1057;&#1077;&#1088;. &#1084;&#1072;&#1090;&#1077;&#1084;., 53:6 (1989), 1183&#8211;1205 [pdf](http://www.mathnet.ru/links/99950da8b286808c64286a2820235651/im1153.pdf)

* {#BondalKapranov90} [[Alexei I. Bondal]], [[Mikhail M. Kapranov]], _Representable functors, Serre functors, and mutations_, Mathematics of the USSR-Izvestiya **35** 3 (1990) 519-541 &lbrack;[doi:10.1070/IM1990v035n03ABEH000716](https://doi.org/10.1070/IM1990v035n03ABEH000716) [pdf](https://www.mathnet.ru/links/6ad8b932b7c8801d1b821034af7d08b2/im1153_eng.pdf)&rbrack;
 
The following paper gives the corrected definition and also demonstrates the utility of the Serre functor as a tool for working with the derived category of coherent sheaves on a variety (c.f. [[Bondal-Orlov reconstruction theorem]]):

* [[Aleksei Bondal]], [[Dmitri Orlov]], _[Reconstruction of a variety from the derived category and groups of autoequivalences](http://www.mi.ras.ru/~orlov/papers/Compositio2001.pdf)_, Compositio Mathematica 125 (03), 327-344.

See also:

* Oleksandr Manzyk, _A-infinity-bimodules and Serre A-infinity-functors_, dissertation [pdf](https://kluedo.ub.uni-kl.de/files/1910/dissertation.pdf), [djvu](https://kluedo.ub.uni-kl.de/files/1910/dissertation.djvu);  _Serre $A_\infty$ functors_, talk at Categories in geometry and math. physics, Split 2007, slides, [pdf](http://www.irb.hr/korisnici/zskoda/manzyukslides.pdf), work with [[Volodymyr Lyubashenko]]
* Volodymyr Mazorchuk, Vanessa Miemietz, _Serre functors for Lie algebras and superalgebras_
* [[Sefi Ladkani]], _Categorification of a linear algebra identity and factorization of Serre functors_,  Mathematische Zeitschrift __285__ (2017) 879--896 [doi](https://doi.org/10.1007/s00209-016-1731-9)

[[!redirects Serre functors]]
