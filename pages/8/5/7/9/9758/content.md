

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
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

Given an [[irreducible representation|irreducible]] [[spinor representation]] $S$ equipped with a [spinor metric](spin+representation#SpinorMetric), what are called _Fierz identities_ are the [[equations]] that express the composite [[isomorphism]]

$$
  S \otimes S \simeq S \otimes S^\ast \simeq End(S) \simeq Cl(S)
$$

where 

1. $S \otimes S$  is the [[tensor product]] of the [[vector space]] $S$ with itself;

1. the first isomorphism is induced by the [spinor metric](spin+representation#SpinorMetric), which is equivalently an identification $S \simeq S^\ast$ of $S$ with its [[dual vector space]];

1.  the second isomorphism is the canonical one to the [[endomorphism ring]] of $S$ (using that [[FinVect]] is a [[compact closed category]] );

1. the last one uses the fact that on an [[irreducible representation|irreducible]] [[spinor representation]] the [[endomorphism ring]] is in fact identified with the [[Clifford algebra]].

The traditional way to express this in terms of components is the following.

Given a [[spinor]] $\psi$, write $\overline{\psi}$ for its image under the identification $S \simeq S^\ast$  ("charge conjugation", see [here](spin+representation#PairingToVectorByChargeConjugationMatrix)).
Let $\{\Gamma^a\}$ be a [[basis]] for the give [[Clifford algebra]] [[representation]] and writee as usual $\{\Gamma^{a_1 \cdots a_p}\}$ for the skew-symmetrized [[matrix product]] of $p$ such basis elements. Then under the above [[isomorphism]] there will be for all pairs $\psi_1, \psi_2 \in S$ of [[spinors]] an [[equation]] of the form

$$
  \psi_1 \otimes \overline{\psi}_2
  =
  \sum_p c_p   \left(\overline{\psi_2}\Gamma^{a_1 \cdots a_p} \psi_1\right)
  \,
  \Gamma_{a_1 \cdots a_p}
  \,,
$$

where $c_p \in \mathbb{R}$ is some [[coefficient]], expressing the [[endomorphism]] of pairing with $\psi_2$ and then spitting out $\psi_1$ as a [[linear combination]] of the [[endomorphisms]] $\Gamma^{a_1 \cdots a_p}$.

This equation is, once the [[coefficients]] $c_p$ have been determined, the _Fierz identity_.

Sometimes this is moreover expressed after acting with the endomorphisms on a third chosen [[spinor]] $\psi_3$, in which case the Fierz identity reads

$$
  \left(\overline{\psi}_2 \psi_3\right) \psi_1  
  =
  \sum_p c_p   \left(\overline{\psi_2}\Gamma^{a_1 \cdots a_p} \psi_1\right)
  \,
  \Gamma_{a_1 \cdots a_p}\psi_3
  \,.
$$

## Applications

### Expression of spinor quadrilinears

The Fierz identities are typically used in order to re-express
quadrilinear terms of four [[spinors]] of the form

$$
  \left(
    \overline{\psi_1}\Gamma^{a_1 \cdots a_{p_1}} \psi_2
  \right)
  \left(
    \overline{\psi_3}\Gamma^{b_1 \cdots b_{p_2}} \psi_4
  \right) 
$$

by applying the idenity to the pair $\psi_2 \otimes \overline{\psi_3}$ in the middle.

### Computation of cocycles of super-translation cocycles

Given $S$ a suitable real [[spinor representation]]
which induces a [[super Poincaré Lie algebra]] $\mathfrak{siso}_S(d-1,1)$ with corresponding [[super translation Lie algebra]] $\mathbb{R}^{d-1,1; S}$ then a degree $(2,p)$-element of its [[Chevalley-Eilenberg algebra]] which is [[Lorentz group|Lorentz]] invariant is of the form

$$
  \mu \coloneqq \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p}\psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
  \,.
$$

The CE-[[differential]] sends this to

$$
  \begin{aligned}
  d_{CE}\mu 
  &= 
  d_{CE}
  \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p}\psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_p}
   \\
   & \propto
  \left(\overline{\psi} \wedge \Gamma^{a_1 \cdots a_p}\psi \wedge e_{a_1} \wedge \cdots \wedge e_{a_{p-1}}\right)
  \wedge
  \left(
    \overline{\psi}\wedge \Gamma_{a_p} \psi
  \right)   
  \,.
  \end{aligned}
$$

If the right hand side vanishes, then $\mu$ is a [[super Lie algebra|super]] [[Lie algebra cocycle]], and this is entirely controled by the Fierz identity applied the middle term $\psi \wedge \overline{\psi}$ and the symmetry properties of the [[Clifford algebra]] elements.

These computations control the existence of [[Green-Schwarz action functionals]] and hence [[schreiber:The brane bouquet]]. See there for more.

## Related concepts

* [[Clebsch-Gordan coefficient]]

## References

Traditional accounts of Fierz identities include


* C. C. Nishi, _Simple derivation of general Fierz-type identities_,  	Am. J. Phys. 73 (2005) 1160-1163 ([arXiv:hep-ph/0412245](http://arxiv.org/abs/hep-ph/0412245))

The Fierz identities that give the vanishing of trilinear and of quadratic terms in spinors in certain dimensions are discussed from the point of view of [[division algebras and supersymmetry]] in section 2.4 of

* [[John Huerta]], _Division Algebras, Supersymmetry and Higher Gauge Theory_ ([arXiv:1106.3385](http://arxiv.org/abs/1106.3385))

The Fierz identities for $Spin(9,1)$ (relevant in [[heterotic supergravity]] and [[type II supergravity]]) are discussed in appendix C of 

* [[José Figueroa-O'Farrill]], Emily Hackett-Jones, George Moutsopoulos, _The Killing superalgebra of ten-dimensional supergravity backgrounds_, Class.Quant.Grav.24:3291-3308,2007 ([arXiv:hep-th/0703192](http://arxiv.org/abs/hep-th/0703192))

The full Fierz identities for $Spin(10,1)$ (relevant in [[11-dimensional supergravity]]) are tabulated in pages 12, 13 of 

* [[Riccardo D'Auria]], [[Pietro Fré]], _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982)


[[!redirects Fierz identities]]