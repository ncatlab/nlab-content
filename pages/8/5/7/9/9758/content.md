

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

We discuss Fierz identities as identities among multispinorial elements of the [[Chevalley-Eilenberg algebra]] $CE(\mathbb{R}^{d-1,1\vert N})$ of [[super-Minkowski spacetime]] $\mathbb{R}^{d-1,1\vert N}$, regarded as the super-translation [[supersymmetry]] [[super Lie algebra]]. In this form Fierz identities encode [[cocycles]] in the [[supersymmetry]] super-[[Lie algebra cohomology]], such as those which serve as [[higher WZW terms]] characterizing [[super p-branes]]. We follow [Castellani-D'Auria-Fr&#233; 82, section II.8](#CDF).


### Bilinear Fierz identities

Given a fixed [[real spin representation]] $N$, then the
the odd coordinates $\{\theta^\alpha\}_{\alpha = 1}^{dim_{\mathbb{R}}(N) }$ of the [[super Minkowski spacetime]]
$\mathbb{R}^{d-1,1\vert N}$ span, by construction, precisely that representation space, and hence so do the
spinorial components of the super-[[vielbein]] form

$$
  \psi^\alpha = \mathbf{d}\theta^\alpha
   \;\;\;
   \in \Omega^{\bullet}_{li}(\mathbb{R}^{d-1,1\vert N})
   \simeq
    CE(\mathbb{R}^{d-1,1\vert N})
  \,,
$$

since in the construction of [[super differential forms]] on $\mathbb{R}^{d-1,1\vert N}$, the de Rham operator
$\mathbf{d}$ acts on the odd coordinates just formally, by sending the generator $\theta^\alpha$ to the new generator
named $\mathbf{d} \theta^\alpha$.

Therefore we may identify the [[spin representation]] $N$ with the [[linear span]] (over $\mathbb{R}$) of these elements

$$
  N  \simeq \langle \mathbf{d}\theta^\alpha \rangle_{\alpha = 1}^{dim_{\mathbb{R}}(N) }
  \,,
$$

were the [[spin group]] acts on the elements on the right in the defining way (see at _[[geometry of physics -- supersymmetry]]_): a spinorial rotation in a plane $\omega = \{\omega^{a b}\}$ by an angle $\alpha$ acts by

$$
  R_\omega(\psi) \coloneqq \exp(\tfrac{\alpha}{4} \omega^{a b} \Gamma_{a b} ) \psi
  \,.
$$

We may build new [[spin representations]] from this one by forming multilinear expressions in the [[super vielbein]]. For example the elements in $CE(\mathbb{R}^{d-1,1\vert N})$ of the form

$$
  \begin{aligned}
    \overline{\psi} \wedge \Gamma_a \psi
    &=
    \left(C_{\alpha \alpha'} \Gamma_a{}^{\alpha'}_{\beta}\right) \, \psi^\alpha \wedge \psi^{\beta}
    \\
    & =
    \left(C_{\alpha \alpha'} \Gamma_a{}^{\alpha'}_{\beta}\right) \, \mathbf{d}\theta^\alpha \wedge \mathbf{d}\theta^\beta
  \end{aligned}
$$

span, as the spacetime index $a$ ranges in $\{0, 1, \cdots, d-1\}$, a $d$-dimensional [[real vector space]]

$$
  \left\langle
     \,\overline{\psi} \wedge \Gamma_a \psi\,
  \right\rangle_{a = 0}^{d-1}
$$

which still carries a linear [[action]] of the [[spin group]], induced from the spin action on the $\psi$-s:

$$
  \begin{aligned}
    R_\omega(\overline{\psi} \wedge \Gamma_a \psi)
    & =
    \overline{\left( \exp(\tfrac{\alpha}{4}\omega^{a b}\Gamma_{a b} ) \psi \right)}
      \wedge \Gamma_a
    \left( \exp(\tfrac{\alpha}{4}\omega^{a b}\Gamma_{a b} \psi ) \right)
    \\
    & =
    \overline{\psi} \wedge \exp(-\tfrac{\alpha}{4} \omega^{a b} \Gamma_{a b}) \Gamma_a \exp(\tfrac{\alpha}{2}\omega^{a b} \Gamma_{a b})
     \psi
    \\
    & =
    \overline{\psi}
      \wedge
      (R_\omega(\Gamma_a))
    \psi
    \end{aligned}
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

Now observe that we may say all this more abstractly as follows:

1. the elements $(\psi \wedge \overline{\psi})^{\alpha \beta}$ span the symmetrized [[tensor product of representations]]

   $$
     \{N \otimes N\}_{sym}
       \;\simeq\;
     \langle 
       \,  (\psi \wedge \overline{\psi})^\alpha{}_\beta \,
     \rangle_{\alpha,\beta = 1}^{dim_{\mathbb{R}}(N)}
   $$

1. for given $p \in \mathbb{N}$, then the elements of the form $\overline{\psi} \wedge \Gamma_{a_1 \cdots a_p} \psi$ form a [[subrepresentation]] thereof, equivalent to the vector representation $\wedge^p\mathbb{R}^{d}$

1. hence there is a [[direct sum]] decomposition

   $$
     \left\{N \otimes N\right\}_{sym}
       \;\simeq\;
      \underset{p \in \mathbb{N}}{\bigoplus}
      c_p \left(\wedge^p \mathbb{R}^d\right)
   $$

   in the [[category of representations]] of the [[spin group]], which expresses the (symmetrized) [[tensor product of representations]] of the [[Majorana spinor]] representation as a [[direct sum]] of skew-symmetrized tensor products of the vector representation.

Indeed this direct sum decomposition is exhaustive:

+-- {: .num_prop #BilinearFierzDecomposition}
###### Proposition

For $d \in \mathbb{N}$ and $N$ a [[Majorana spinor]] representation of $Spin(d-1,1)$, then the following identity holds:

$$
  (\psi \wedge \overline{\psi})^\alpha{}_\beta
   \;=\;
  \tfrac{1}{dim_{\mathbb{R}}(N)}
  \left(
     \left(
       \overline{\psi}\psi
     \right)
     +
     \left(
       \overline{\psi} \Gamma_a \psi
     \right)
     (\Gamma^a)^\alpha{}_\beta
     + 
     \tfrac{1}{2!}
     \left(
       \overline{\psi} \Gamma_{a_1 a_2} \psi
     \right)
     (\Gamma^{a_1 a_2})^\alpha{}_\beta
      + 
     \cdots
  \right)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the discussion there, the [[Majorana spinor]] representation is a real sub-representation of a complex _Dirac representation_ $\mathbb{C}^{(2^\nu)}$. The latter has the special property that

1. the [[Clifford algebra]] contains the full [[matrix algebra]];

1. for $p \geq 1$ the Clifford elements $\Gamma_{a_1 \cdots a_p}$ have vanishing [[trace]].

The first point implies that there exists coefficients $X^{a_1 \cdots a_p} \in \mathbb{C}$ for $p \in \mathbb{N}$ such that

$$
  \psi \wedge \overline{\psi}
    =
  \tfrac{1}{dim_{\mathbb{R}}(N)}
  \left(
    X
    +
    X^a \Gamma_a 
    +
    X^{a b} \Gamma_{a b} 
    +
    \cdots
  \right)
  \,.
$$

The second condition then implies that multiplying this expression with $\Gamma^{a_1 \cdots a_p}$ and taking the trace projects out the coefficient $X^{a_1 \cdots a_p}$:

$$
  \begin{aligned}
    X^{a_1 \cdots a_p}
      & = 
    \frac{1}{p! dim_{\mathbb{R}}(N)}
    tr_N
    \left(
      \left(
        X
        +
        X^a \Gamma_a 
        +
        X^{a b} \Gamma_{a b} 
        +
        \cdots
      \right)
      \Gamma^{a_1 \cdots a_p}
   \right)
   \\
   & = 
   \tfrac{1}{p!}
   tr_N
   \left(
     \psi \wedge \overline{\psi} \, \Gamma^{a_1 \cdots a_p}
   \right)
   \\
   & = 
   \tfrac{1}{p!}
   \left(
     \overline \psi \wedge \Gamma^{a_1 \cdots a_p} \psi
   \right)
  \end{aligned}
  \,.
$$

Notice that it is the last step, identifying the trace over $\psi \wedge \overline{\psi} \Gamma^{a_1 \cdots a_p}$ with the $\psi$-$\psi$ component of the matrix $\Gamma^{a_1 \cdots a_p}$, where we use the _symmetrization_ of the spinor tensor product, namely the identity $\psi^\alpha \wedge \overline{\psi}_\beta = \overline{\psi}_\beta \wedge \psi^\alpha$.  

=--


Some of the coefficients in prop. \ref{BilinearFierzDecomposition} may vanish identically. These are the _bilinear Fierz identities_, of the form

$$
  \overline{\psi} \Gamma_{a_1 \cdots a_p} \psi = 0
  \,.
$$

+-- {: .num_example}
###### Example

Let $d = 11$. Write $\mathbf{32}$ or $(\tfrac{1}{2})^5$ for the [[Majorana spinor]] representation of $Spin(d-1,1)$. Then 

$$
  \left\{
    (\tfrac{1}{2})^5
      \otimes
    (\tfrac{1}{2})^5
  \right\}_{sym}
     \;\simeq\;
  \underset{\simeq \mathbb{R}^d}{\underbrace{(1)^1 (0)^4}}
    \;\oplus\;
  \underset{\simeq \wedge^2 \mathbb{R}^d}{\underbrace{(1)^2 (0)^3}}
    \;\oplus\;
  \underset{\wedge^5 \mathbb{R}^d}{\underbrace{(1)^5}}
  \,.
$$

=--

([D'Auria-Fr&#233; 82b (3.1)](#DAuriaFre82b))


+-- {: .proof}
###### Proof

Since we know from prop. \ref{BilinearFierzDecomposition} that the right hand side has to be some direct sum of representations of the form $\wedge^p \mathbb{R}^d$, it is sufficient to check that there is only one choice of sum such that [[dimensions]] match on both sides of the equation.

Now the dimension of $\{N \otimes N\}_{sym}$ is that of the space of symmetric $32 \times 32$ matrices:

$$
  dim_{\mathbb{R}} 
  \left(
     \{\mathbf{32} \otimes \mathbf{32}\}_{sym}
  \right)
   \;=\;
  \frac{1}{2}
  \left(
    32 \times 33 
  \right)
   = 
  528
$$

while the dimension of $\wedge^p \mathbb{R}^d$ is the [[binomial coefficient]]

$$
  dim_{\mathbb{R}}(\wedge^p \mathbb{R}^d)
   \;=\;
  \left(
    11 \atop p
  \right)
  \,.
$$


Hence the claim follows from the fact that 

$$
  \begin{aligned}
    582 
     & = 11 + 55 + 462
    \\
    & =
  \left(11 \atop 1\right)
   +
  \left(11 \atop 2\right)
   +
  \left(11 \atop 5\right)
  \end{aligned}
  \,.
$$

=--





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

* {#DAuriaFre82b} [[Riccardo D'Auria]], [[Pietro Fré]], pages 12, 13 of _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982)
 
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