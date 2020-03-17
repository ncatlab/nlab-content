+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Pfaffian_ of a [[skew-symmetric matrix]] is a [[square root]] of its [[determinant]].

## Definition

Let $A = (A_{i,j})$ be a skew-symmetric $(2n \times 2n)$-[[matrix]]  with entries in some [[field]] (or [[ring]]) $k$.

+-- {: .num_defn}
###### Definition

The _Pfaffian_ $Pf(A) \in k$ is the element

\[
  \label{PfaffianViaSignatureOfPermutations}
  Pf(A)
  \;\coloneqq\;
  \frac{1}{2^n n!}  
  \sum_{\sigma \in Sym_{2n}} 
   sgn(\sigma) 
   \prod_{i = 1}^n 
     A_{\sigma(2i -1), \sigma(2i)}
  \,,
\]

where 

* $\sigma$ runs over all [[permutation]]s of $2n$ elements;

* $sgn(\sigma)$ is the [[signature of a permutation]].

Expressed equivalently in terms of the [[Levi-Civita symbol]] $\epsilon$ and using the [[Einstein summation convention]] the Pfaffian is

\[
  \label{PfaffianInTermsOfLCTensor}
  Pf(A)
  \;\coloneqq\;
  \frac{1}{2^n n!}  
  A_{i_1 j_1}
  A_{i_2 j_2}
  \cdots
  A_{i_n j_n}
  \epsilon^{ i_1 j_1 i_2 j_2 \cdots  i_n j_n }
  \,.
\]


=--



## Properties

### Relation to the determining

+-- {: .num_prop #PfaffianIsSquareRootOfDeterminant}
###### Proposition
([[Pfaffian]] is [[square root]] of [[determinant]])

Let $A = (A_{i,j})$ be a skew-symmetric $(2n \times 2n)$-[[matrix]]  with entries in some [[field]] (or [[ring]]) $k$.

Then the Pfaffian of $A$ (eq:PfaffianViaSignatureOfPermutations) is a [[square root]] of the [[determinant]] of $A$:

\[
  \label{DeterminantIsPfaffianSquared}
  \big(
    Pf(A)
  \big)^2
  \;=\;
  det(A)
  \,.
\]

=--

Proofs are spelled out for instance in [Haber 15, Sections 2 and 3](#Haber15)

### In terms of Berezinian integrals

+-- {: .num_prop}
###### Proposition


Let $\Lambda_{2n}$ be the [[Grassmann algebra]] on $2n$ generators $\{\theta_i\}$, which we think of as a [[vector]] $\vec \theta$

Then the Pfaffian $Pf(A)$ is the [[Berezinian integral]]

$$
  Pf(A)
  =
  \int   
    \exp( \langle \vec \theta, A \cdot \vec \theta \rangle )
  d \theta_1 d \theta_2 \cdots d \theta_{2n}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Compare this to the Berezinian integral representation of the [[determinant]], which is 

$$
  det(A)
  \propto
  \int   
    \exp( \langle \vec \theta, A \cdot \vec \psi \rangle )
  d \theta_1 d \theta_2 \cdots d \theta_{2n}
  d \psi_1 d \psi_2 \cdots d \psi_{2n}
  \,.
$$

=--

## Pfaffian state

Pfaffians appear in the expression of certain multiparticle wave functions. Most notable is the pfaffian state of $N$ spinless electrons

$$
\Psi_{Pf}(z_1,\ldots,z_N) = pfaff\left(\frac{1}{z_k-z_l}\right)\prod_{i\lt j}(z_i-z_j)^q
exp(-\frac{1}{4}\sum |z|^2)
$$
where $pfaff(M_{k l})$ denotes the Pfaffian of the matrix whose labels are $k,l$ and $q= 1/\nu$ is the filling fraction, which is an even integer. For Pfaffian state see

* [[Gregory Moore]], N. Read, _Nonabelions in the fractional quantum hall effect_, Nucl. Phys. 360B(1991)362 [pdf](http://www.physics.rutgers.edu/~gmoore/MooreReadNonabelions.pdf)

## Related entries

* [[determinant]], 

* [[Pfaffian line bundle]], 

* [[hafnian]]

## References

### General

Basics:

* {#Haber15} Howard E. Haber, _Notes on antisymmetric matrices and the pfaffian_, 2015 ([pdf](http://scipp.ucsc.edu/~haber/webpage/pfaffian2.pdf), [[HaberPfaffian.pdf:file]])

See also

* J.-G. Luque, J.-Y. Thibon, _Pfaffian and hafnian identities in shuffle algebras_, [math.CO/0204026](http://arxiv.org/abs/math.CO/0204026)

* Claudiu Raicu, Jerzy Weyman, _Local cohomology with support in ideals of symmetric minors and Pfaffians_, [arxiv/1509.03954](http://arxiv.org/abs/1509.03954)

* Haber, _Notes on antisymmetric matrices and the pfaffian_, [pdf](http://scipp.ucsc.edu/~haber/webpage/pfaffian.pdf)

There is also a deformed noncommutative version of Pfaffian related to [[quantum linear group]]s:

* Naihuan Jing, Jian Zhang, _Quantum Pfaffians and hyper-Pfaffians_, Adv. Math. 265 (2014), 336--361, [arxiv/1309.5530](http://arxiv.org/abs/1309.5530)

Pfaffian variety is subject of 4.4 in

* Alexander Kuznetsov, _Semiorthogonal decompositions in algebraic geometry_, [arxiv/1404.3143](http://arxiv.org/abs/1404.3143)

Relation to $\tau$-functions is discussed in 

* J. W. van de Leur, A. Yu. Orlov, _Pfaffian and determinantal tau functions I_, [arxiv/1404.6076](http://arxiv.org/abs/1404.6076)

Other articles:

* Andr&#225;s C. L&#337;rincz, Claudiu Raicu, Uli Walther, Jerzy Weyman, _Bernstein-Sato polynomials for maximal minors and sub-maximal Pfaffians_, [arxiv/1601.06688](http://arxiv.org/abs/1601.06688)
* M. Spera, _A C*–algebraic approach to determinants and Pfaffians, Acta Cosmologica Fasc. XXI-2, (1995) 203–208.

### Euler forms


Discussion of _[[Euler forms]]_ ([[differential form]]-representatives of [[Euler classes]] in [[de Rham cohomology]]) as [[Pfaffians]] of [[curvature forms]]:

* {#Chern44} [[Shiing-Shen Chern]], _A simple intrinsic proof of the Gauss-Bonnet formula for closed Riemannian manifolds_, Annals of Mathematics Second Series __45__:4 (1944) 747-752 ([jstor:1969302](https://www.jstor.org/stable/1969302))


* {#MathaiQuillen86} [[Varghese Mathai]], [[Daniel Quillen]], below (7.3) of _Superconnections, Thom classes, and equivariant differential forms_, Topology Volume 25, Issue 1, 1986 (<a href="https://doi.org/10.1016/0040-9383(86)90007-8">10.1016/0040-9383(86)90007-8</a>)

* {#Wu05} Siye Wu, Section 2.2 of _Mathai-Quillen formalism_, pages 390-399 in _Encyclopedia of Mathematical Physics_ 2006 ([arXiv:hep-th/0505003](https://arxiv.org/abs/hep-th/0505003))

* {#Walschap04} Gerard Walschap, ch. 6.3 of _Metric structures in differential deometry_, Graduate Texts in Mathematics, Springer 2004 

* [[Hiro Lee Tanaka]], _Pfaffians and the Euler class_, 2014 ([pdf](http://www.hiroleetanaka.com/pdfs/2014-fall-230a-lecture-26-gauss-bonnet-chern.pdf))

* {#Nicolaescu18} [[Liviu Nicolaescu]], Section 8.3.2 of _Lectures on the Geometry of Manifolds_, 2018 ([pdf](https://www3.nd.edu/~lnicolae/Lectures.pdf), [MO comment](https://mathoverflow.net/a/117982/381))


category: algebraic geometry, representation theory
[[!redirects Pfaffians]]
[[!redirects pfaffian]]
