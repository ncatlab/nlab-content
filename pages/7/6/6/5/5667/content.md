
> under construction

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

KK-theory is a "bivariant" version of [[operator K-theory]]: for $A, B$ two [[operator algebras]], the _KK-group_ $KK(A,B)$ is a natural [[homotopy]] [[equivalence class]] of $(A,B)$-[[Hilbert bimodules]] equipped with an additional left weak [[Fredholm module]] structure. These KK-groups $KK(A,B)$ behave in the first argument as [[K-homology]] of $A$ and in the second as [[K-cohomology]] of $B$.

There is a [[stable (infinity,1)-category]] and in particular a [[triangulated category]] of operator algebras such that $KK(-,-)$ is the [[hom-set]] of the corresponding [[homotopy category]] ([Meyer](#Meyer)).

Accordingly, the groups $KK(A,B)$ are now viewed as a "correct" hom-set among noncommutative operator algebras for the purpose of various homotopy-invariant functors. 

## Definition

Let $A,B$ be two [[C-star algebras]].

Say a _KK-bimodule_ is a $\mathbb{Z}_2$-[[graded vector space|graded]] $(A,B)$-[[Hilbert bimodules]] $\mathcal{H}$ equipped with an adjointable odd-graded bounded operator $F \in \mathcal{B}_A(\mathcal{H})$ such that $\pi(a)(F^2 - 1) \in \mathcal{K}_A(\mathcal{H})$ and $[\pi(a), F] \in \mathcal{K}_A(\mathcal{H})$ for all $a \in A$. 

(...)

For $B = \mathbb{C}$ this is equivalently an $A$-[[Fredholm module]].

A [[homotopy]] between two $(A,B)$-KK-bimodules is an $(A, C([0,1],B))$-bimodule which interpolates between then two.

Then one writes $KK(A,B)$ for the [[quotient]] of $(A,B)$-KK-bimodules under homotopy. This is naturally an [[abelian group]] under [[direct sum]] of bimodules and operators.

Here $KK(A,\mathbb{C}) \simeq K_0(A)$ is the [[algebraic K-theory]] group of $A$. (...)

## Properties

### Relation to extensions

There is an [[isomorphism]]

$KK(A,B) \simeq Ext^1(A,B)$

to a suitable group of suitable [[extensions]] of $A$ by $B$. ([Kasparov 80](#Kasparov80), reviewed in [Inassaridze](#Inassaridze)).

### Relation to homotopy-classes of $\ast$-homomorphisms

Theorem (Cuntz)

If $A,B$ are [[C-star-algebras]] with $A$ separable and $B$ $\sigma$-unital, then 

$$
  KK(A,B) \simeq [q A, B \otimes \mathcal{K}]
  \,,
$$

where

* $q A$ is the [[kernel]] of the [[codiagonal]] $A \star A \to A$,

* $\mathcal{K}$ is the $C^\ast$-algebra of [[compact operators]].

* $[-,-]$ is the set of [[homotopy]] [[equivalence classes]] of $\ast$-[[homomorphisms]].

(reviewed in ([Joachim-Johnson07](#JoachimJohnson07))).

## Theorems

* The [[Baum-Connes conjecture]] is naturally formulated within KK-theory.

* The [[Novikov conjecture]] has been verified in many cases using KK-theory.

## Related concepts

* [[operator K-theory]]

  * [[E-theory]]

## References

### General

KK-theory was introduced by [[Gennady Kasparov]] in 

* [[Gennady Kasparov]], _The operator $K$-functor and extensions of $C^{\ast}$-algebras_, Izv. Akad. Nauk SSSR Ser. Mat. __44__  (1980), no. 3, 571&#8211;636, 719, [MR81m:58075](http://www.ams.org/mathscinet-getitem?mr=582160), [Zbl](http://www.zentralblatt-math.org/zmath/search/?an=Zbl%200464.46054%7CZbl%200448.46051), [abstract](http://www.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=im&paperid=1739&option_lang=eng), [english doi](http://dx.doi.org/10.1070%2FIM1981v016n03ABEH001320), free Russian original: [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=im&paperid=1739&volume=44&year=1980&issue=3&fpage=571&what=fullt&option_lang=eng)
 {#Kasparov80}

prompted by the advances in [[Brown-Douglas-Fillmore theory]], especially in the last 1977 article.

A textbook account is in 

* B. Blackadar, _K-theory for Operator Algebras_, 2nd ed. Cambridge University Press, Cambridge (1999)

Introductions and surveys include

* [[Nigel Higson]], _A primer on KK-theory_. Proc. Sympos. Pure Math. 51, Part 1, 239&#8211;283. (1990) ([pdf](http://www.math.psu.edu/higson/math/Papers_files/Higson%20-%201990%20-%20A%20primer%20on%20KK-theory.pdf))

* [[G. Skandalis]], _Kasparov's bivariant K-theory and applications_ Exposition. Math. 9, 193&#8211;250 (1991) ([pdf](http://www.math.vanderbilt.edu/~bisch/ncgoa08/talks/skandalis2.pdf))

### In geometric quantization

Discussion of KK-theory with an eye towards [[representation of a C-star algebra|C-star representations]] of [[groupoid convolution 

algebras]] in the context of [[geometric quantization]] [[geometric quantization by push-forward|by push-forward]] is in 

* [[Klaas Landsman]], _Quantization as a functor_ ([arXiv:math-ph/0107023](http://arxiv.org/abs/math-ph/0107023))

* [[Klaas Landsman]], _Functorial quantization and the Guillemin-Sternberg conjecture_ ([arXiv:math-ph/0307059](http://arxiv.org/abs/math-ph/0307059))

* [[Rogier Bos]], _Groupoids in geometric quantization_ PhD Thesis (2007) ([pdf](http://www.math.ist.utl.pt/~rbos/ProefschriftA4.pdf))
 {#Bos}

### Homotopy theory

KK-theory is naturally understood in terms of [[homotopy theory]].

Characterization of KK-theory as the [[satellites]] of a functor is in 

* [[Hvedri Inassaridze]], _Universal property of Kasparov bivariant K-theory_ ([[InassaridzeOnKK.pdf:file]], [ps](http://www.math.uni-bielefeld.de/~bak/kasp.ps))
 {#Inassaridze}

A [[triangulated category]] structure for KK-theory is discussed in 

* [[Ralf Meyer]], _Categorical aspects of bivariant K-theory_, ([arXiv:math/0702145](http://arxiv.org/abs/math/0702145))
 {#Meyer}

* [[Ralf Meyer]], [[Ryszard Nest]], _Homological algebra in bivariant K-theory and other triangulated categories_ ([arXiv:math/0702146](http://arxiv.org/abs/math/0702146))

* [[Ralf Meyer]], _KK-theory as a triangulated category_, Lecture notes (2009) ([pdf](http://wwwmath.uni-muenster.de/u/echters/Focused-Semester/lecturenotes/Meyer_--_KK-theory_as_a_triangulated_category.pdf))
 {#Meyer}

A [[model category]] realization of KK-theory is discussed in 

* [[Michael Joachim]], [[Mark Johnson]], _Realizing Kasparov's KK-theory groups as the homotopy classes of maps of a Quillen model category_ ([arXiv:0705.1971](http://arxiv.org/abs/0705.1971))
 {#JoachimJohnson07}


### In D-brane theory

KK-theory also descrives [[charges]] and sources in [[D-brane]] theory.

A review is in

* [[Richard Szabo]], _D-branes and bivariant K-theory_ ([arXiv:0809.3029](http://arxiv.org/abs/0809.3029))


[[!redirects Kasparov K-theory]]
[[!redirects bivariant K-theory]]
