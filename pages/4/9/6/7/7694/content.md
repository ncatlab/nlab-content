# Serre functor

* table of contents
{: toc}


## Idea

Serre functors were introduced by [[Aleksei Bondal]] and [[Mikhail Kapranov]] to study [[admissible subcategories]] of [[triangulated categories]].  A **Serre functor** on a triangulated category $\mathcal{A}$ is an exact functor such that for any objects $A$ and $B$, $\Hom(A,B) \simeq \Hom(B, S(A))^*$.  It does not always exist, but when it does it is unique up to graded natural isomorphism.

The Serre functor is a powerful tool for working with the [[derived category]] of [[coherent sheaves]] on a variety.

## Definition

In the original paper, the following definition was given.

+-- {: .un_defn}
###### Definition
Let $\mathcal{A}$ be a $k$-linear triangulated category with finite-dimensional [[Hom]]'s and $k$ algebraically closed.  A **Serre functor** $S : \mathcal{A} \to \mathcal{A}$ is an additive equivalence that commutes with the translation functor, with bi-functorial isomorphisms $\phi_{A,B} : \Hom_\mathcal{A}(A,B) \stackrel{\sim}{\to} \Hom_{\mathcal{A}}(B,S(A))^*$ for any objects $A$ and $B$, such that the composite
  \[ (\phi^{-1}_{S(A),S(B)})^* \circ \phi_{A,B} : \Hom(A,B) \to \Hom(B,S(A))^* \to \Hom(S(A), S(B)) \]
coincides with the isomorphism induced by $S$.
=--

In fact, the last commutativity condition can be deduced from just the bi-functoriality of $\phi_{A,B}$, and commutativity with the translation functor also follows from a proposition below.  Hence, the following definition is seen in later papers.

+-- {: .un_defn}
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

+-- {: .un_prop}
###### Proposition
Any two Serre functors are connected by a canonical graded functorial isomorphism that commutes with the isomorphisms $\phi_{A,B}$ in the definition of the Serre functor.
=--

## References

The original paper and English translation:

* &#1040;. &#1048;. &#1041;&#1086;&#1085;&#1076;&#1072;&#1083;, &#1052;. &#1052;. &#1050;&#1072;&#1087;&#1088;&#1072;&#1085;&#1086;&#1074;, _&#1055;&#1088;&#1077;&#1076;&#1089;&#1090;&#1072;&#1074;&#1080;&#1084;&#1099;&#1077; &#1092;&#1091;&#1085;&#1082;&#1090;&#1086;&#1088;&#1099;, &#1092;&#1091;&#1085;&#1082;&#1090;&#1086;&#1088;&#1099; &#1057;&#1077;&#1088;&#1088;&#1072; &#1080; &#1087;&#1077;&#173;&#1088;&#1077;&#1089;&#1090;&#1088;&#1086;&#1081;&#1082;&#1080;_, &#1048;&#1079;&#1074;. &#1040;&#1053; &#1057;&#1057;&#1057;&#1056;. &#1057;&#1077;&#1088;. &#1084;&#1072;&#1090;&#1077;&#1084;., 53:6 (1989), 1183&#8211;1205 [pdf](http://www.mathnet.ru/links/99950da8b286808c64286a2820235651/im1153.pdf)

* [[Alexei Bondal|Alexei I. Bondal]], [[Mikhail Kapranov|Mikhail M. Kapranov]], _Representable functors, Serre functors, and mutations_, Izv. Akad. Nauk SSSR Ser. Mat. 53 (1989), no. 6, 1183&#8211;1205, 1337.
 
The following paper gives the corrected definition and also demonstrates the utility of the Serre functor as a tool for working with the derived category of coherent sheaves on a variety (c.f. [[Bondal-Orlov reconstruction theorem]]):

* [[Aleksei Bondal]], [[Dmitri Orlov]], _[Reconstruction of a variety from the derived category and groups of autoequivalences](http://www.mi.ras.ru/~orlov/papers/Compositio2001.pdf)_, Compositio Mathematica 125 (03), 327-344.

See also:

* Oleksandr Manzyk, _A-infinity-bimodules and Serre A-infinity-functors_, dissertation [pdf](https://kluedo.ub.uni-kl.de/files/1910/dissertation.pdf), [djvu](https://kluedo.ub.uni-kl.de/files/1910/dissertation.djvu);  _Serre $A_\infty$ functors_, talk at Categories in geometry and math. physics, Split 2007, slides, [pdf](http://www.irb.hr/korisnici/zskoda/manzyukslides.pdf), work with [[Volodymyr Lyubashenko]]
* Volodymyr Mazorchuk, Vanessa Miemietz, _Serre functors for Lie algebras and superalgebras_