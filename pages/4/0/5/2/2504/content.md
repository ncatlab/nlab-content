
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

The _supergravity Lie 3-algebra_ $\mathfrak{sugra}(10,1)$ is a super [[∞-Lie algebra]] that is a shifted [[∞-Lie algebra cohomology|extension]]

$$
  0 \to b^2 \mathbb{R} \to 
  \mathfrak{sugra}(10,1) \to
  \mathfrak{siso}(10,1)
  \to
  0
$$

of the [[super Poincare Lie algebra]] $\mathfrak{siso}(10,1)$ in 10+1 dimensions induced by a degree 4-[[∞-Lie algebra cocycle]] $\mu_4$.

$$
  \mu = \bar \psi \wedge \Gamma^{a b} \psi \wedge e_a \wedge e_b
  \;\;
  \in CE(\mathfrak{siso}(10,1))
  \,.
$$

This is the same mechanism by which the [[String Lie 2-algebra]] is a shifted central extensiono of $\mathfrak{so}(n)$.

## Properties

+-- {: .num_prop }
###### Proposition


Let $\mathfrak{der}(\mathfrak{sugra}(10,1))$ be the [[automorphism ∞-Lie algebra]] of $\mathfrak{sugra}(10,1)$. This is a [[dg-Lie algebra]]. Write
$\mathfrak{der}(\mathfrak{sugra}(10,1))_0$ for the ordinary [[Lie algebra]] in degree 0.

This is [[isomorphic]] to the polyvector-extension of the [[super Poincaré Lie algebra]] (see there) in $d = 10+1$, the Lie algebra spanned by generators
$\{P_a, Q_\alpha, J_{a b}, Z^{a b}\}$ and graded Lie brackets those of the [[super Poincaré Lie algebra]] as well as

$$
  [Q_\alpha, Q_\beta] = i (C \Gamma^a)_{\alpha \beta} P_a + (C \Gamma_{a b})Z^{a b} 
$$

$$
  [Q_\alpha, Z^{a b}] = 2 i (C \Gamma^{[a}))_{\alpha \beta}Q^{b]\beta}
$$

etc.

=--

This computation is in ([Castellani05, section 3.1](#Castellani05)).


## Applications

The field configurations of 11-dimensional [[supergravity]] may be identified with [[∞-Lie algebra-valued forms]] with values in $\mathfrak{sugra}(10,1)$.
See [[D'Auria-Fre formulation of supergravity]].

## Related concepts

[[supergravity Lie 6-algebra]] $\to$ **supergravity Lie 3-algebra** $\to$ [[super Poincaré Lie algebra]]


## References

The [[Chevalley-Eilenberg algebra]] of $\mathfrak{sugra}(10,1)$ first appears in 

* R. D'Auria, P. Fr&#233; _Geometric supergravity in $D = 11$ and its hidden supergroup_ [[GeometricSupergravity.pdf:file]]

and later in the textbook

* [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fre]], _[[Supergravity and Superstrings - A Geometric Perspective]]_
{#CastellaniDAuriaFre}

The manifest interpretation of this as a [[Lie 3-algebra]] and the supergravity field content as [[∞-Lie algebra valued forms]] with values in this is mentioned in 

* Hisham Sati, Urs Schreiber, Jim Staasheff, _$L_\infty$-algebra valued connections_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">web</a>)

A systematic study of the super-[[Lie algebra cohomology]] involved is in

* [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry I_ ([arXiv:0909.0551](http://arxiv.org/abs/0909.0551))

* [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry II_ ([arXiv:1003.34360](http://arxiv.org/abs/1003.3436))

See also [[division algebra and supersymmetry]].

The computation of the automorphism Lie algebra of $\mathfrak{sugra}(10,1)$ is in 

* [[Leonardo Castellani]], _Lie derivatives along antisymmetric tensors and the M-theory superalgebra_ ([pdf](http://arxiv.org/PS_cache/hep-th/pdf/0508/0508213v2.pdf))
{#Castellani05}