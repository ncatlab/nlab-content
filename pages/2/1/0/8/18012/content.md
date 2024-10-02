
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _curved $L_\infty$-algebra_ (e.g. [Markl 11, p. 100](#Markl11)) is just like an ordinary _[[L-∞ algebra]]_, but possibly including also a 0-ary bracket, i.e. a constant. Conversely, an ordinary [[L-∞ algebra]] is a curved $L_\infty$-algebra for which the 0-ary operation happens to be zero.

Accordingly, a "strong homotopy [[homomorphism]]" of curved $L_\infty$-algebras is defined just as for ordinary $L_\infty$-algebras, but allowing also for a 0-ary component. Notice that such "curved sh-maps" may be non-trivial even between ordinary $L_\infty$-algebras (amplified e.g. in [Mehta & Zambon 12, below (2)](#MehtaZambon12)).

The dual [[Chevalley-Eilenberg algebras]] automatically capture curved $L_\infty$-algebras unless one imposes a constraint: the non-curved $L_\infty$-algebras correspond to the [[augmented algebra|augmented]] CE-algebras. Similarly in the [[dg-coalgebra]] description the restriction to non-curved $L_\infty$-algebras requires co-augmentation or else (this is what is commonly used) non-unital dg-coalgebras. 


## Definition


Where an ordinary _[[L-infinity algebra]]_ is a $\mathbb{Z}$-[[graded vector space]] $\mathfrak{g}$ equipped for all $n \in \mathbb{N}$, $n \geq 1$ with $n$-ary brackets:

$$
  l_n \;\colon\; \mathfrak{g}^{\otimes^n} \longrightarrow \mathfrak{g}
$$

out of the [[tensor product]] of $n$-copies of $\mathfrak{g}$,
subject to some conditions,  for a curved $L_\infty$-algebra also a component

$$
  l_0 \;\colon\; \mathfrak{g}^{\otimes^0} \simeq \mathbb{R} \to \mathfrak{g}
$$

is allowed. Since an $\mathbb{R}$-linear map out of $\mathbb{R}$ is uniquely fixed by a single element (the image of $1 \in \mathbb{R}$), this is "a constant", called the _curvature_ of the curved $L_\infty$-algebra.

Now the strong homotopy Jacobi identity 

\[
  \label{LInfinityJacobiIdentity}
  \sum_{{i,j \in \mathbb{N}} \atop {i+j = n+1}} 
  \sum_{\sigma \in UnShuff(i,j)}
  \chi(\sigma,v_1, \cdots, v_{n})
  (-1)^{i(j-1)}
   l_{j} \left(
     l_i \left( v_{\sigma(1)}, \cdots, v_{\sigma(i)} \right),
     v_{\sigma(i+1)} , \cdots , v_{\sigma(n)}
   \right)
  = 0
  \,,
\]

implies in particular that 

$$
  l_1 \circ l_1 = \pm l_2(l_0, -)
$$

hence that the unary operation $l_1$ no longer necessarily squares to zero (no longer defines a [[chain complex]] $(\mathfrak{g}, l_1)$) but to the binary bracket with the curvature.

## Related concepts

* [[curved A-infinity algebra]]

* [[curved dg-algebra]]

## References

* {#Markl11} [[Martin Markl]], _Deformation Theory of Algebras and Their Diagrams_, Regional Conference Series in Mathematics Number 116, American Mathematical Society (2011)

* [[Andrey Lazarev]], [[Travis Schedler]], _Curved infinity-algebras and their characteristic classes_, J Topology (2012) 5 (3): 503-528 ([arXiv:1009.6203](https://arxiv.org/abs/1009.6203))

* {#MehtaZambon12} [[Rajan Mehta]], [[Marco Zambon]], _$L_\infty$-Actions_, Differential Geometry and its Applications 30 (2012), 576-587 ([arXiv:1202.2607](https://arxiv.org/abs/1202.2607))

[[!redirects curved L-infinity algebras]]

[[!redirects curved L-∞ algebra]]
[[!redirects curved L-∞ algebras]]

[[!redirects curved sh-map]]
[[!redirects curved sh-maps]]

[[!redirects curved L-infinity homomorphism]]
[[!redirects curved L-infinity homomorphisms]]


[[!redirects curved L-∞ homomorphism]]
[[!redirects curved L-∞ homomorphisms]]
