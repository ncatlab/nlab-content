
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

A _K-orientation_ is an [[orientation in generalized cohomology]] for [[K-theory]] (typically: [[topological K-theory]]).

## Definition

### In topological K-theory

#### K-Orientation of oriented manifolds

For ordinary [[topological K-theory]] a [[smooth function]] between [[smooth manifolds]] $f \colon X \to Y$ is K-oriented if $T X \oplus f^\ast(T Y)$ has a [[spin^c structure]].

In this case there is an [[Umkehr map]]

$$
  f_! \colon K^\bullet(X) \to K^{\bullet + dim(Y) - dim(X)}(Y)
  \,.
$$

#### The universal Atiyah-Bott-Shapiro orientation
 {#UniversalAtiyahBottShapiroOrientation}


There is a universal [[orientation in generalized cohomology]] of

* [[complex K-theory]] [[KU]] over [[spin^c structures]];

* [[KO]] over [[spin structure]]

hence [[E-infinity ring]] homomorphisms out of the [[Thom spectrum]] [[MSpin]]

 [[MSpin]] $\longrightarrow$ [[KO]]


and

[[MSpin^c|MSpin<sup><i>c</i></sup>]] $\longrightarrow$ [[KU]]

These are (both) referred to as the _Atiyah-Bott-Shapiro orientation_ (after [Atiyah-Bott-Shapiro](#AtiyahBottShapiro)); the $E_\infty$-structure is due to ([Joachim 04](#Joachim04)).

The [[genus]] induced by $M Spin \to KO$ is the [[A-hat genus]], that induced by $M Spin^c \to KU$ is the [[Todd genus]].

Of course $KU$ is also a [[complex oriented cohomology theory]] and as such canonically comes with an $E_\infty$-map $MU \to KU$ (see at [spin^c structure -- from almost complex structure](spin%5Ec+structure#FromAlmostComplexStructures)).

On this level there is also the [[real oriented cohomology|real orientation]] of [[real K-theory]] given by a map 

$$
  M \mathbb{R} \longrightarrow K \mathbb{R}
$$

from [[MR-theory]] ([Kriz 01, (3.20)](#Kriz01)).


### In KK-theory

In the context of [[KK-theory]], a morphism $f \colon A \to B$ of [[C*-algebra]], a _K-orientation_ of this morphism is a map

$$
  f! \in KK_d(B,A)
$$

such that (...). The corresponding [[fiber integration]]/[[Gysin map]] on [[operator K-theory]] is then the postcomposition operation

$$
  f_! \colon K_\bullet(B) \simeq KK_\bullet(\mathbb{C}, B) \stackrel{f! \circ (-)}{\to} KK_\bullet(\mathbb{C}, A) \simeq K_{\bullet + d}(A)
  \,.
$$

([BMRS 07](#BMRS07))

## Properties

### As the relation between cobordisms cohomology and K-theory

The Atiyah-Bott-Shapiro orientation $M Spin^c \to KU$ induces an equivalence

$$
  M Spin^c_\bullet(-)\otimes_{M Spin^c_\bullet} KU_\bullet \simeq KU_\bullet(-)
$$

and $M Spin \to KO$ similarly induces

$$
  M Spin_\bullet(-)\otimes_{M Spin_\bullet} KO_\bullet \simeq KO_\bullet(-)
$$

This is due to ([Hopkins-Hovey 92](#HopkinsHovey92)), a variation of the [[Conner-Floyd isomorphism]]. See at _[[cobordism theory determining homology theory]]_ for more.

## Related concepts


* [[spin^c structure]]

* [[Conner-Floyd isomorphism]], [[cobordism theory determining homology theory]]

* [[Grothendieck-Riemann-Roch theorem]]



[[!include genera and partition functions - table]]

## References

### In topological K-theory

The $Spin$/$Spin^c$-orientation of [[KO]]/[[KU]] [[topological K-theory]] is attributed to

* {#AtiyahBottShapiro} [[Michael Atiyah]], [[Raoul Bott]], [[Arnold Shapiro]], _Clifford modules_, Topology 3(Suppl 1):3&#8211;38 ([pdf](http://dell5.ma.utexas.edu/users/dafr/Index/ABS.pdf))

That the map of spectra $M Spin^c\to KU$  extendes to a homomorphism of [[E-infinity rings]] is due to

* {#Joachim04} [[Michael Joachim]], _Higher coherences for equivariant K-theory_, in _Structured ring spectra_, volume 315 of London Math. Soc. Lecture Note Ser., pages 87&#8211;114. Cambridge Univ. Press, Cambridge, 2004 ([pdf](http://mat.uab.es/~aguade/bcat02/slides/joachim.pdf))

Discussion for [[real K-theory]] includes

* {#Kriz01} [[Igor Kriz]], _Real-oriented homotopy theory and an analogue of the
Adams-Novikov spectral sequence_, Topology 40 (2001) 317-399 ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/hukriz.pdf))

The discussion of [[cobordism theory determining homology theory]] for the K-orientation is due to

* {#HopkinsHovey92} [[Michael Hopkins]], [[Mark Hovey]], _Spin cobordism determines real K-theory_, Mathematische Zeitschrift 210.1 (1992): 181-196. ([[HopkinsHoveyCobordismK.pdf:file]])

### In KK-theory

Discussion in [[noncommutative topology]]/[[KK-theory]] is in 

* [[Alain Connes]], , [[Georges Skandalis]], _The longitudinal index theorem for foliations_. Publ. Res. Inst. Math. Sci. 20,
no. 6, 1139&#8211;1183 (1984)
 {#ConnesSkandalis84}

* Jacek Brodzki, [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], _Noncommutative correspondences, duality and D-branes in bivariant K-theory_, Adv. Theor. Math. Phys.13:497-552,2009 ([arXiv:0708.2648](http://arxiv.org/abs/0708.2648))
 {#BMRS07}


[[!redirects K-orientations]]

[[!redirects KU-orientation]]
[[!redirects KU-orientations]]

[[!redirects orientation in K-theory]]
[[!redirects orientations in K-theory]]

[[!redirects K-theory orientation]]
[[!redirects K-theory orientations]]


[[!redirects Atiyah-Bott-Shapiro orientation]]
[[!redirects Atiyah-Bott-Shapiro orientations]]


[[!redirects Spin orientation of KO]]
[[!redirects Spin^c orientation of KU]]