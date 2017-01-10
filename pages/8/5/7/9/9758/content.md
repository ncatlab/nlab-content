

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

## In terms of cochains on super-Minkowski spacetimes

Given a fixed [[real spin representation]] $N$, then the
the odd coordinates $\{\theta^\alpha\}_{\alpha = 1}^{dim_{\mathbb{R}}(N) }$ of the [[super Minkowski spacetime]]
$\mathbb{R}^{d-1,1\vert N}$ span by construction precisely that representation space, and hence so to the
spinorial component of the super-[[vielbein]] form

$$
  \psi^\alpha = \mathbf{d}\theta^\alpha
  \,,
$$

since in the construction of [[super differential forms]] on $\mathbb{R}^{d-1,1\vert N}$, the de Rham operator
$\mathbf{d}$ acts on the odd coordinates just formally, by sending the generator $\theta^\alpha$ to the new generator
named $\mathbf{d} \theta^\alpha$.

Hence as [[spin representations]] we may identify

$$
  N  \simeq \langle \mathbf{d}\theta^\alpha \rangle_{\alpha = 1}^{dim_{\mathbb{R}}(N) }
  \,.
$$

Now we may build new [[spin representations]] from this one by forming multilinear expressions
in the [[super vielbein]]. For example the elements in $CE(\mathbb{R}^{d-1,1\vert N})$ of the form

$$
  \begin{aligned}
    \overline{\psi} \wedge \Gamma_a \psi
    &=
    \left(C_{\alpha \alpha'} \Gamma_a{}^{\alpha'}{\beta}\right) \psi^\alpha \wedge \psi^{\beta}
    \\
    & =
    \left(C_{\alpha \alpha'} \Gamma_a{}^{\alpha'}{\beta}\right) \mathbf{d}\theta^\alpha \wedge \mathbf{d}\theta^\beta
  \end{aligned}
$$

span, as the spacetime index $a$ ranges in $\{0, 1, \cdots, d-1\}$ a $d$-dimensional [[real vector space]]

$$
  \langle
     \overline{\psi} \wedge \Gamma_a \psi
  \rangle_{a = 0}^{d-1}
$$

which still carries a linear [[action]] of the [[spin group]], induced from the spin action on the $\psi$-s:

$$
  \overline{\left( \exp(\tfrac{\alpha}{4}\omega^{a b}\Gamma_{a b} ) \right)}
    \wedge \Gamma_a
  \left( \exp(\tfrac{\alpha}{4}\omega^{a b}\Gamma_{a b} ) \right)
  =
  \overlne{\psi} \wedge \exp(-\tfrac{\alpha}{4} \omega^{a b} \Gamma_{a b}) \Gamma_a \exp(\tfrac{\alpha}{2}\omega^{a b} \Gamma_{a b})
   \psi
  =
  R(\omega)_a{}^b \left(\overline{\psi} \wedge \Gamma_b \psi\right)
  \,.
$$

Of course similarly we obtain elements

$$
  \overline{\psi} \Gamma_{a_1 \cdots a_p} \psi
$$

which, if they are non-vanishing at all, span the representation

$$
  \wedge^p \mathbb{R}^d
$$

More abstractly this says that

1. the elements $(\psi \wedge \overline{\psi})^{\alpha \beta}$ span the symmetrized [[tensor product of representations]]

   $$
     \{N \otimes N\}_{sym}
   $$

1. the elements $\overline{\psi} \wedge \Gamma_a \psi$ form a [[subrepresentation]] thereof, equivalent to
   the vector representation $\mathbb{R}^{d}$

1. hence there is a [[direct sum]] decomposition

   $$
     \left\{N \otimes N\right\}_{sym}
       \;\simeq\;
     \mathbb{R}^d \oplus \cdots
   $$

   in the [[category of representations]] of the [[spin group]]




This direct sum decomposition induces a [[projection]] map

$$
   \left\{
    N \otimes N
  \right\}_{sym}
    \longrightarrow
  \mathbb{R}^d
$$


In components this projection must be of the form


$$
  (\psi \wedge \overline{\psi})^{\alpha{}_{\beta}
     \;\mapsto\;
  \propto
  \tfrac{1}{dim_{\mathbb{R}}}(n)
  \left(
    \overline{\psi}\wedge \Gamma_a \psi
  \right)
  K^{a \alpha}{}_\beta
$$

for some coefficients $K^{a \alpha}{}_\beta$. We claim that these must be proportional to the Clifford elements.

Because by the construction of the Dirac representation, all the $\Gamma_{a_1 \cdots \Gamma_{a_p}}$ are traceless.

In the Dirac representation, the Dirac matices span the endomorphisms, hence there is some expansion of the form

$$
  \psi \wedge \overline{\psi}
    =
  \frac{1}{dim_{\mathbb{R}}(N)}
  \left(
    1 X
    +
    \Gamma_a X^a
    +
    \Gamma_{a b} X^n
    +
    \cdots
  \right)
$$

for some coefficients $X^{a_1 \cdots a_p}$. Moreover, in the Dirac representation all
$\Gamma_{a_1 \cdots a_p}$ for $p \geq 1$ are traceless, only for $p = 0$ then $tr(1) = dim_{\mathbb{R}}(N)$ is non-vanishing.
It follows that

$$
  \begin{aligned}
    \overline{\psi} \wedge \Gamma^{a_1 \cdots a_p} \psi
    & =
  \mathrm{tr}_N\left(
    \psi \wedge \overline{\psi} \Gamma^{a_1 \cdots a_p}
  \right)
   \\
   & =
   tr_N
   \left(
   \frac{1}{dim_{\mathbb{R}}(N)}
   \left(
     1 X
     +
     \Gamma_a X^a
     +
     \Gamma_{a b} X^n
     +
     \cdots
    \right)
     \Gamma^{a_1 \cdots a_p}
    \right)
    \\
    &
    =
    p! X^{a_1 \cdots a_p}
  \end{aligned}
$$




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