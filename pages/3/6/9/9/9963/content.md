
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

The notion of _augmented $A_\infty$-algebra_ is the analogue in [[higher algebra]] of the notion of _[[augmented algebra]]_ in ordinary algebra: an [[A-∞ algebra]] euipped with a [[homomorphism]] to the bas [[E-∞ ring]].

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

## Examples

+-- {: .num_example}
###### Example

An augmentation of an [[E-∞ ring]] $R$ itself, being an [[A-∞ algebra]] over the [[sphere spectrum]] $\mathbb{S}$, is a homomorphism 

$$
  \epsilon \colon R \to \mathbb{S}
$$

to the [[sphere spectrum]], regarded as an [[E-∞ ring]].

=--

+-- {: .num_example}
###### Example

A [[bipermutative category]] $\mathcal{C}$ induces (as discussed there) an [[E-∞ ring]] $\vert \mathcal{C}\vert$. If $\mathcal{C}$ is equipped with a bi-[[monoidal functor]] $\mathcal{C} \to \mathcal{Z}$ then this induces an augmentation of $\vert \mathcal{C}\vert$ over $H \mathbb{Z}$, the [[Eilenberg-MacLane spectrum]] of the [[integers]].

=--

See for instance ([Arone-Hess](#AroneHess))

## Related concepts

* [[augmented algebra]], [[augmentation ideal]]

* [[augmentation]], [[augmented simplicial set]]

* [[augmented ∞-group]]

## References

For $A_\infty$-algebras in [[characteristic]] 0 (in chain complexes) augmentation appears for instance as def. 2.3.2.2 on p. 81 in 

* Kenji Lef&#232;vre-Hasegawa, _Sur les A-infini cat&#233;gories_ ([arXiv:math/0310337](http://arxiv.org/abs/math/0310337))


The following articles discuss (just) [[augmented ∞-groups]].

Augmentation (of [[∞-groups of units]] of [[E-∞ rings]]) over the [[sphere spectrum]]  appears in

* Steffen Sagave, _Spectra of units for periodic ring spectra_ ([arXiv:1111.6731](http://arxiv.org/abs/1111.6731))

Augmentation over the [[Eilenberg-MacLane spectrum]] $H\mathbb{Z}$ appears in

* Fregory Arone, [[Kathryn Hess]], _Augmented $\Gamma$-spaces, the stable rank filtration, and a $b u$-analogue of the Whitehead conjecture_ ([pdf](http://www.math.union.edu/~leshk/papers/FilteredGammaSpaces-revision.pdf))
 {#AroneHess}

[[!redirects augmented A-infinity-algebras]]

[[!redirects augmented A-∞ algebra]]
[[!redirects augmented A-∞ algebras]]
