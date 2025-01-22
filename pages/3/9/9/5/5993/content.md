
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
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

The *Pfaffian* $pf(A) \in k$ is the element

\[
  \label{PfaffianViaSignatureOfPermutations}
  pf(A)
  \;\coloneqq\;
  \frac{1}{2^n \, n!}  
  \textstyle{\sum_{\sigma \in Sym_{2n}}} 
   sgn(\sigma) 
   \textstyle{\prod_{i = 1}^n} 
     A_{\sigma(2i -1), \sigma(2i)}
  \,,
\]

where 

* $\sigma$ runs over all [[permutation]]s of $2n$ elements;

* $sgn(\sigma)$ is the [[signature of a permutation]].

Expressed equivalently in terms of the [[Levi-Civita symbol]] $\epsilon$ and using the [[Einstein summation convention]], the Pfaffian is

\[
  \label{PfaffianInTermsOfLCTensor}
  pf(A)
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

### Relation to the determinant

+-- {: .num_prop #PfaffianIsSquareRootOfDeterminant}
###### Proposition
([[Pfaffian]] is [[square root]] of [[determinant]])

Let $A = (A_{i,j})$ be a skew-symmetric $(2n \times 2n)$-[[matrix]]  with entries in some [[field]] (or [[ring]]) $k$.

Then the Pfaffian of $A$ (eq:PfaffianViaSignatureOfPermutations) is a [[square root]] of the [[determinant]] of $A$:

\[
  \label{DeterminantIsPfaffianSquared}
  \big(
    pf(A)
  \big)^2
  \;=\;
  det(A)
  \,.
\]

=--

Proofs are spelled out for instance by [Haber 2015, Sections 2 and 3](#Haber15).


### In terms of Berezinian integrals
 {#InTermOfBerezinianIntegrals}


\begin{proposition}
 \label{PfaffianAsBerezinianIntegral}

Let $\Lambda_{2n}$ be the [[Grassmann algebra]] on $2n$ generators $\{\theta_i\}$, which we think of as a [[vector]] $\vec \theta$

Then the Pfaffian $pf(A)$ is the [[Berezinian integral]]

$$
  pf(A)
  \;=\;
  \textstyle{\int}
  \,
  \left(
   \textstyle{\prod_{i=1}^{2n}}
   \mathrm{d}\theta_i
  \right)
  \,
    \exp\big( 
      \tfrac{1}{2}
      \langle \vec \theta, A \cdot \vec \theta \rangle 
    \big)
  \,.
$$

\end{proposition}

\begin{remark}

Compare this to the [[Berezinian integral]]-representation of the [[determinant]], which is instead:

$$
  det(A)
  \;\propto\;
  \textstyle{\int}   
  \left(
    \textstyle{\prod}_{i = 1}^{2n}
    \mathrm{d}\theta_i
  \right)
  \left(
    \textstyle{\prod}_{i = 1}^{2n}
    \mathrm{d}\psi_i
  \right)
  \,
  \exp\big( 
    \langle \vec \theta, A \cdot \vec \psi \rangle 
  \big)
  \,.
$$

The relation $Det(A) = \big(Pf(A)\big)^2$ follows readily (cf. [Math.SE:a/2705327](https://math.stackexchange.com/a/2705327/58526))

\end{remark}


## Applications

### Pfaffian state of fractional quantum Hall systems
 {#PfaffianStateOfFractionalQuantumHallEffect}

Pfaffians appear in the expression of certain multiparticle [[wave functions]] generalizing [[Laughlin wavefunctions]] modeling [[ground states]] of [[fractional quantum Hall systems]]. 

Prominent here is the *pfaffian state* &lbrack;[Moore & Read 1991 (5.1)](Laughlin+wavefunction#MooreRead91)&rbrack; of an [[even number]] $N$ 

> (In practice, $N$ is a humongous "macroscopic" number on the scale of the [[Avogadro constant]], and hence may be assumed to be [[even number|even]] without any conceivable restriction of practical generality.)

of spinless (or rather: spin-polarized) [[electrons]], which is the ("[[wavefunction|wave]]"-)[[function]] on the [[configuration space of points|configuration space of $N$ points]] in the ([[complex plane|complex]]) [[plane]] 

\[
  \label{MooreReadPfaffianState}
  \Psi_{Pf}(z_1,\ldots,z_{N}) 
  \;=\; 
   vd(z_\bullet)
   ^q
   \,
   pf\left(
    \frac{1}{z_{\bullet_1} - z_{\bullet_2}}
   \right)
   \,
   exp\Big(
     -\frac{1}{4}
     \textstyle{\sum}_i {|z_i|}^2
  \Big)
  \mathrlap{\,,}
\]
where 

* $vd(z_\bullet) \;\coloneqq\; \prod_{i \lt j} (z_i - z_j)$ is a *[[Vandermonde determinant]]*,

* $pf\left( \frac{1}{z_{\bullet_1} - z_{\bullet_2}} \right)$ is the Pfaffian of the inverse [[complex number|complex]] [[distances]] between the (electron) positions,

* $q = 1/\nu \,\in\, \mathbb{N}$ is the "filling fraction". 

Historically, (eq:MooreReadPfaffianState) was guessed as a deformation of the [[Laughlin wavefunction]], which is the same expression without the Pfaffian factor. But with the [above](#InTermOfBerezinianIntegrals) Berezinian integration method both expressions actually unify in the *super-Laughlin wavefunction*:

\[
  \label{SuperLaughlinWavefunction}
  \Psi_{super}\big(
    (z_1, \theta_1), 
    \cdots
    (z_N, \theta_N)
  \big)
  \;\coloneqq\;
  \textstyle{\prod_{i \lt j}}
  \,
  \big(
    z_i - z_j 
    - \theta_i \theta_j
  \big)^q
  \,
   exp\Big(
     -\frac{1}{4}
     \textstyle{\sum_i} {|z_i|}^2
  \Big)
  \,,
\]

of which the ordinary Laughlin wavefunction is the lowest component (the [[coefficient]] of $\theta_i = 0$ for all $i$), while the Pfaffian state is the top component (the [[coefficient]] of $\theta_1 \cdot \theta_2 \cdots \theta_N$) -- since, by Prop. \ref{PfaffianAsBerezinianIntegral}:

$$
  \begin{array}{l}
    \textstyle{\int}
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \underset{i \lt j}{\prod}
    ( z_i - z_j  - \theta_i \theta_j )^q
    \\
    \;=\;
    \textstyle{\int} 
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \textstyle{\underset{i \lt j}{\prod}}
    \Big(
      ( z_i - z_j )^q
      \,
      \exp\big(
        -q\, ( z_i - z_j )^{-1} \, \theta_i \theta_j
      \big)
      \,
    \Big)
    \\
    \;=\;
    \textstyle{\int} 
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      ( z_i - z_j )^q
    \Big)
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      \exp\big(
        -q\, ( z_i - z_j )^{-1} \, \theta_i \theta_j
      \big)
    \Big)
    \\
    \;=\;
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      ( z_i - z_j )^q
    \Big)
    \,
    \textstyle{\int} 
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      \exp\big(
        -q \, ( z_i - z_j )^{-1} \, \theta_i \theta_j
      \big)
    \Big)
    \\
    \;=\;
    \Big(
      \textstyle{\underset{i \lt j}{\prod}}
      ( z_i - z_j )^q
    \Big)
    \,
    \textstyle{\int} 
    \left(
      \textstyle{\prod_i} \mathrm{d}\theta_i
    \right)
    \,
    \exp\big(
      -q \, 
      \textstyle{\sum_{i \lt j}}
      ( z_i - z_j )^{-1} \, \theta_i \theta_j
    \big)
    \\
    \;=\;
    \left(-\tfrac{q}{2}\right)^{N/2}
    \,
    vd\big(z_\bullet\big)^q
    \,
    pf\left(
      \tfrac
        { 1 }
        { z_{\bullet_1} - z_{\bullet_2} }
    \right)
    \,.
  \end{array}
$$

This observation is due to [Hasebe 2008](Laughlin+wavefunction#Hasebe08), cf. [Gromov, Martinec & Ryu 2020 (13)](Laughlin+wavefunction#GromovMartinecRyu20).


\begin{remark}
The argument of the super-Laughlin wavefunction (eq:SuperLaughlinWavefunction) is indeed the difference of "super-positions" as seen in the [[super-translation group]], where (cf. [there](super-translation+group#eq:GroupLawIn1D)):

$$
  (z_i, \theta_i)
  -
  (z_j, \theta_j)
  \;=\;
  \big(
    z_i - z_j - \theta_i \theta_i
    ,\,
    \theta_i - \theta_j
  \big)
  \,.
$$
\end{remark}  

\begin{remark}
  The Pfaffian $pf\Big( (z_{\bullet_1} - z_{\bullet_2})^{-1} \Big)$ changes sign when swapping any pair of [[variables]] $z_r \leftrightarrow z_s$ (which is manifest in the Berezinian presentation, where it corresponds equivalently to instead swapping $\theta_r \leftrightarrow \theta_s$). 

But also the Vandermonde determinant changes sign when swapping pairs of variables (see [there](Vandermonde+determinant#SkewSymemtryUnderSwappingVariables)). This means that 

1. for odd filling fraction $q$:

   1. the ordinary [[Laughlin state]] is *skew-symmetric* in its arguments --- as befits the [[wavefunction]] of [[quantum many-body physics|multiple]] [[fermions]],

   1. the Pfaffian Moore-Read state is *symmetric* in its arguments --- as befits the [[wavefunction]] of [[quantum many-body physics|multiple]] [[bosons]].

1. for even filling fraction $q$ it is the other way around.
  
\end{remark}



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

* Andr&#225;s C. L&#337;rincz, Claudiu Raicu, Uli Walther, Jerzy Weyman, _Bernstein-Sato polynomials for maximal minors and sub-maximal Pfaffians_, [arxiv/1601.06688](https://arxiv.org/abs/1601.06688)
* [[Mauro Spera]], _A C*–algebraic approach to determinants and Pfaffians, Acta Cosmologica Fasc. XXI-2, (1995) 203--208.

* [[Donald E. Knuth]], _Overlapping Pfaffians_, Electronic Journal of Combinatorics __3__:2 (1996) [pdf](https://www.emis.de/journals/EJC/Volume_3/PDFFiles/v3i2r5.pdf)
  > "A combinatorial construction proves an identity for the product of the Pfaffian of a skew-symmetric matrix by the Pfaffian of one of its submatrices. Several applications
of this identity are followed by a brief history of Pfaffians."

* [[Jacques Distler]], Nathan Donagi, [[Ron Donagi]]: *On Generalized Pfaffians* &lbrack;[arXiv:2409.06871](https://arxiv.org/abs/2409.06871)&rbrack;


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
