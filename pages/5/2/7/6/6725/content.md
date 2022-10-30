
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

There is an observation by [Ho&#345;ava--Witten](#HoravaWitten) that suggests that quantum [[11-dimensional supergravity]] on an  $\mathbb{Z}_2$-[[orbifold]] (actually a [[higher orientifold]]) of the form $X_{10} \times /(S^1//\mathbb{Z}_2))$ induces on its [[boundary]] "[[M9-brane]]" (the $\mathbb{Z}_2$-fixed point manifold) [[heterotic string theory]].

The orbifold equivariance condition of the [[supergravity C-field]] is that discussed at _[[orientifold]]_ (there for the [[B-field]]). Therefore it has to vanish at the two fixed fixed points of the $\mathbb{Z}_2$-action. Thereby the quantization condition

$$
  [2G_4] = 2 [c_2] - [\frac{1}{2} p_1]
$$ 

on the [[supergravity C-field]] becomes the condition for the [[Green-Schwarz mechanism]] of the [[heterotic string theory]] on the "boundary" (the orbifold fixed points).

## Properties

### Boundary conditions
 {#BoundaryConditions}

The [[supergravity C-field]] $\hat G_4$ is supposed to vanish, and _differentially_ vanish at the boundary in the HW model, meaning that also the local connection 3-form $C_3$ vanishes there. The argument is roughly as follows (similar for as in [Falkowski, section 3.1](#Falkowski)).


The [[higher dimensional Chern-Simons theory|higher Chern-Simons term]] 

$$
  C_3 \mapsto C_3 \wedge G_4 \wedge G_4
$$

in the [[Lagrangian]] of [[11-dimensional supergravity]] is supposed to be well-defined on fields on the [[orbifold]] and hence is to be $\mathbb{Z}_2$-invariant. 

Let $\iota_{11}$ be the canonical vector field along the circle factor. Then the component of $G \wedge G$ which is annihilated by the contraction $\iota_{11}$ is necessarily even, so the component $d x^{11}\wedge \iota_11 C_3$ is also even. It follows that also $d x^{11}\wedge \iota_11 G_4$ is even. 

Moreover, the kinetic term

$$
  C \mapsto G \wedge \star G
$$

is to be invariant. With the above this now implies that the components of $G$ annihiliated by $\iota_{11}$ is odd, because so is the mixed component of the [[metric]] tensor.

This finally implies that the restriction of $C_3$ to the orbifold fixed points has to be closed.

## Related concepts

* [[11-dimensional supergravity]]

* [[M-theory]], [[heterotic string theory]]

* [[M9-brane]]


## References

The original articles are

* [[Petr Hořava]], [[Edward Witten]], _Heterotic and Type I string dynamics from eleven dimensions_, Nucl. Phys. B460 (1996) 506 ([arXiv:hep-th/9510209](http://arxiv.org/abs/hep-th/9510209))

  _Eleven dimensional supergravity on a manifold with boundary_, Nucl. Phys. B475 (1996) 94 ([arXiv:hep-th/9603142](http://arxiv.org/abs/hep-th/9603142))
 {#HoravaWitten} 

Reviews are in 

* Piyush Kumar, _Ho&#345;ava-Witten theory_ (2004) ([pdf](http://theory.uchicago.edu/~sethi/Teaching/P484-W2004/hwitten.pdf))

* [[Paul Townsend]], _Four Lectures on M-Theory_ ([arXiv:hep-th/9612121](http://arxiv.org/abs/hep-th/9612121)). 

* [[Burt Ovrut]], _Lectures on Heterotic M-Theory_ ([arXiv:hep-th/0201032](http://arxiv.org/abs/hep-th/0201032))

* {#Falkowski} [[Adam Falkowski]], section 3 of _Five dimensional locally supersymmetric theories with branes_, Master Thesis, Warsaw ([[FalkowskiLecture.pdf:file]])

Explicit discussion of [[M2-branes]] ending on the HW fixed points and becoming [[heterotic strings]] there is discussed, via the [[BLG model]], in 

* {#Lambert15} [[Neil Lambert]], _Heterotic M2-branes_ ([arXiv:1507.07931](http://arxiv.org/abs/1507.07931))

After [[KK-reduction]] to [[5d supergravity]] there is a corresponding 5d mechanism, see the references [there](5-dimensional+supergravity#ReferencesHWCompactification).

[[!redirects Hořava-Witten theory]]
[[!redirects Hořava–Witten theory]]
[[!redirects Hořava--Witten theory]]
[[!redirects Horava-Witten theory]]
[[!redirects Horava–Witten theory]]
[[!redirects Horava--Witten theory]]