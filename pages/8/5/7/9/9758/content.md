

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What are called _Fierz identities_ in [[physics]] are the relations that hold between [[multilinear map|multilinear]]  expression in [[spinors]]. For example for all [[Majorana spinors]] $\psi$ in Lorentzain spacetime dimension 4,5,6, 11, then the following identity holds

$$
  \left(\overline{\psi} \wedge \Gamma_{a b} \psi\right)
  \wedge
  \left(\overline{\psi} \wedge \Gamma^b \psi\right)
  \;=\;
  0  
  \,.
$$

(Here $\overline{(-)}$ denotes the Majorana conjugate, $\Gamma_a$ are a Clifford representations, the "$\wedge$"-signs denotes symmetrization in the spinor components and summation over repeated indices is understood. The details of this are discussed below.)

In [D'Auria-Fr&#233;-Maina-Regge 82](#DAuriaFreMainaRegge82) it was pointed out that all Fierz identities may be understood as expressing the product operation in the [[representation ring]] of the [[spin group]] (in some given dimension): for $\{S_i\}_{i \in I}$ denoting [[isomorphism classes]] of [[irreducible representations|irreducible]] [[spin representations]], then, by definition of [[irreps]], their [[tensor product of representations]] decomposes again as a [[direct sum]] of [[irreducible representations]]

$$
  S_i \otimes S_j  = \underset{k}{\oplus} C_{i j}{}^k S_k
$$

with "[[Clebsch-Gordan coefficients]]" $C_{i j}{}^k$. These coefficients are effectively the Fierz identities.

For example for Lorentzian dimension 11 with $(\tfrac{1}{2})^5$ denoting the unique irreducible [[Majorana spinor]] representation, then one finds ([D'Auria-Fr&#233; 82b, section 3](#DAuriaFre82b)) that the symmetric part in the quadruple tensor product of this representation with itself decomposes as a direct sum of irreps as follows

$$
  \left\{
    (\tfrac{1}{2})^5 
      \otimes
    (\tfrac{1}{2})^5 
      \otimes
    (\tfrac{1}{2})^5 
      \otimes
    (\tfrac{1}{2})^5 
  \right\}_{sym}
   \;\simeq\;
  (0)^5
    \;\oplus\;
  (1)^3 (0)^2
    \;\oplus\;
  (1)^4 (0)
    \;\oplus\;
  (1)^5 
    \;\oplus\;
  (2) (0)^4
    \;\oplus\;
  (2)(1)(0)^3
    \;\oplus\;
  (2)^2 (0)^3
    \;\oplus\;
  (2)^2 (1)^3
    \;\oplus\;
  (2)^5
$$

where the symbols refer to [[Young diagrams]] canonically labeling representations. The point is that the expression $  \left(\overline{\psi} \wedge \Gamma_{a b} \psi\right) \wedge \left(\overline{\psi} \wedge \Gamma^b \psi\right)$ from above is a spinor quadrilinear which transforms in the vector representation $(1)(0)^4$ (due to its one free spacetime index). But that vector representation $(1)(0)^4$ is missing from the [[direct sum]] above, meaning that the spinor quadrilinear has vanishing components in this vector representation, hence that this expression vanishes identically.



## Related concepts

* [[Clebsch-Gordan coefficient]]

## References

Named after [[Markus Fierz]].

The interpretation of Fierz identities as relations satisfied by [[Clebsch-Gordan coefficients]] in the [[representation ring]] of the [[spin group]] originates in

* {#DAuriaFreMainaRegge82} [[Riccardo D'Auria]], [[Pietro Fré]],  E. Maina, [[Tullio Regge]]  _A New Group Theoretical Technique for the Analysis of Bianchi Identities and Its Application to the Auxiliary Field Problem of $D=5$ Supergravity_, Annals Phys. 139 (1982) 93 ([doi:10.1016/0003-4916(82)90007-0](http://dx.doi.org/10.1016/0003-4916(82)90007-0), [spire](http://inspirehep.net/record/167640/))

where it was applied to $Spin(4,1)$ (relevant in [[5-dimensional supergravity]]).

By this method the Fierz identities for $Spin(9,1)$ (relevant in [[heterotic supergravity]] and [[type II supergravity]]) are discussed in

* {#DAuriaFre82a} [[Riccardo D'Auria]], [[Pietro Fré]], _Geometric Structure of $N=1, D=10$ and $N=4, D=4$ Super Yang-Mills Theory_, Nucl. Phys. B196 (1982) 205 ([spire](http://inspirehep.net/record/167639))
  
see also appendix C of 

* [[José Figueroa-O'Farrill]], Emily Hackett-Jones, George Moutsopoulos, _The Killing superalgebra of ten-dimensional supergravity backgrounds_, Class.Quant.Grav.24:3291-3308,2007 ([arXiv:hep-th/0703192](http://arxiv.org/abs/hep-th/0703192))

and the Fierz identities for $Spin(10,1)$ (relevant in [[11-dimensional supergravity]]) were tabulated in 

* {#DAuriaFre82b} [[Riccardo D'Auria]], [[Pietro Fré]], pages 12, 13 o _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982)
 
see also

* S. Naito, K. Osada, T. Fukui, _Fierz Identities and Invariance of Eleven-dimensional Supergravity Action_, Phys.Rev. D34 (1986) 536-552 ([spire](http://inspirehep.net/record/236376/?ln=de))

A textbook account of the representation ring method and summary of these results is in

* {#CDF} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], chapter II.8 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

See also

* C. C. Nishi, _Simple derivation of general Fierz-type identities_,  	Am. J. Phys. 73 (2005) 1160-1163 ([arXiv:hep-ph/0412245](http://arxiv.org/abs/hep-ph/0412245))


From the point of view of [[division algebras and supersymmetry]]
the Fierz identities that give the vanishing of trilinear and of quadratic terms in spinors in certain dimensions are discussed in

* [[John Huerta]], section 2.4 _Division Algebras, Supersymmetry and Higher Gauge Theory_ ([arXiv:1106.3385](http://arxiv.org/abs/1106.3385))


[[!redirects Fierz identities]]