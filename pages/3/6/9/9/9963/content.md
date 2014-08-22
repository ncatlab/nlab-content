
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _augmented $A_\infty$-algebra_ is the analogue in [[higher algebra]] of the notion of _[[augmented algebra]]_ in ordinary algebra: an [[A-∞ algebra]] euipped with a [[homomorphism]] to the base [[E-∞ ring]] (which might be a plain [[commutative ring]]).

## Definition 
 {#Definition}


Let $R$ be an [[E-∞ ring]] and $A$ an [[A-∞ algebra]] over $R$.

+-- {: .num_defn}
###### Definition

An **augmentation** of $A$ is an $R$-[[A-∞ algebra]] [[homomorphism]]

$$
  \epsilon \colon A \to R
 \,.
$$

=--

+-- {: .num_remark}
###### Remark

In as far as one considers [[A-∞ algebras]] are presented by [[simplicial objects]] or similar, there might also be a (less intrinsic) notion of [[augmentation]] as in _[[augmented simplicial sets]]_. This is _not_ what the above defines.

=--

Fully generally, a definition of augmentation of [[∞-algebras over an (∞,1)-operad]] is in ([Lurie, def. 5.2.3.14](#Lurie)).

## Examples

+-- {: .num_example}
###### Example

An augmentation of an [[E-∞ ring]] $R$, being an [[E-∞ algebra]] over the [[sphere spectrum]] $\mathbb{S}$, is a homomorphism 

$$
  \epsilon \colon R \to \mathbb{S}
$$

to the [[sphere spectrum]], regarded as an [[E-∞ ring]].

Forming [[augmentation ideals]] constitutes an [[equivalence of (∞,1)-categories]]

$$
  E_\infty Ring_{/\mathbb{S}}
  \stackrel{\simeq}{\longrightarrow}
  E_\infty Ring^{nu}
$$

of $\mathbb{S}$-augmented $E_\infty$-rings and [[nonunital E-∞ rings]] ([Lurie, prop. 5.2.3.15](#Lurie)).

=--

+-- {: .num_example}
###### Example

A [[bipermutative category]] $\mathcal{C}$ induces (as discussed there) an [[E-∞ ring]] $\vert \mathcal{C}\vert$. If $\mathcal{C}$ is equipped with a bi-[[monoidal functor]] $\mathcal{C} \to \mathcal{Z}$ then this induces an augmentation of $\vert \mathcal{C}\vert$ over $H \mathbb{Z}$, the [[Eilenberg-MacLane spectrum]] of the [[integers]].

=--

See for instance ([Arone-Lesh](#AroneLesh))

## Related concepts

* [[augmented algebra]], [[augmentation ideal]]

* [[augmentation]], [[augmented simplicial set]]

* [[augmented ∞-group]]

## References

For $A_\infty$-algebras in [[characteristic]] 0 (in chain complexes) augmentation appears for instance as def. 2.3.2.2 on p. 81 in 

* Kenji Lef&#232;vre-Hasegawa, _Sur les A-infini cat&#233;gories_ ([arXiv:math/0310337](http://arxiv.org/abs/math/0310337))

augmentation of $\mathbb{F}_p$ [[E-∞ algebras]] is considered in definition 7.1 of

* [[Michael Mandell]], _$E_\infty$-Algebras and $p$-adic homotopy theory_ ([pdf](hopf.math.purdue.edu/Mandell/einffinal.pdf))


The following articles discuss (just) [[augmented ∞-groups]].

Augmentation (of [[∞-groups of units]] of [[E-∞ rings]]) over the [[sphere spectrum]]  appears in

* Steffen Sagave, _Spectra of units for periodic ring spectra_ ([arXiv:1111.6731](http://arxiv.org/abs/1111.6731))

Augmentation over the [[Eilenberg-MacLane spectrum]] $H\mathbb{Z}$ appears in

* Gregory Arone, Kathryn Lesh, _Augmented $\Gamma$-spaces, the stable rank filtration, and a $b u$-analogue of the Whitehead conjecture_ ([pdf](http://www.math.union.edu/~leshk/papers/FilteredGammaSpaces-revision.pdf))
 {#AroneLesh}

See also 

* {#Fresse06} [[Benoit Fresse]], _The Bar Complex of an E-infinity Algebra_, Adv. Math.  223 (2010), pages 2049-2096 ([arXiv:math/0601085](http://arxiv.org/abs/math/0601085))

and 

* {#Schwede01} [[Stefan Schwede]], section 7.8 of _Stable Homotopy of Algebraic Theories_, 2001 ([pdf](http://www.math.uni-bonn.de/people/schwede/stable.pdf))

with comments on the relation to [[nonunital algebras]].

Fully general discussion in [[higher algebra]] is in 

* {#Lurie} [[Jacob Lurie]], section 5.2.3 in _[[Higher Algebra]]_

[[!redirects augmented A-infinity-algebras]]

[[!redirects augmented A-∞ algebra]]
[[!redirects augmented A-∞ algebras]]

[[!redirects augmented E-∞ algebra]]
[[!redirects augmented E-∞ algebras]]

[[!redirects augmented E-∞ ring]]
[[!redirects augmented E-∞ rings]]

