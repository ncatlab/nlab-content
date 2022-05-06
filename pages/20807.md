
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A _fuzzy sphere_ is a variant of an [[n-sphere]] in [[noncommutative geometry]]. Often the fuzzy _[[2-sphere]]_ is meant by default, but there are also fuzzy spheres of higher dimension.

## Definition

### Fuzzy 2-sphere
 {#Fuzzy2SphereDefinition}

For $N \in \mathbb{N}$, $N \geq 2$, the _fuzzy 2-sphere_ of $N$ bits is the [[formal duality|formal dual]] to the [[associative algebra]] which is the sub-algebra in the [[matrix algebra]] $Mat_{N \times N}$ generated from the elements of the $N$-dimensional [[complex numbers|complex]] [[irreducible representation|irreducible]] [[Lie algebra representation]] of [[su(2)]].

We now say this more in detail:

#### Conventions and Normalizations
 {#ConventionsAndNormalizations}

First to introduce relevant notation and to set out the proper choices of normalizations. 

\linebreak

With $\mathfrak{su}(2)$ the [[Lie algebra]] [[su(2)]] of [[SU(2)]], with [[complexification]] the [[special linear Lie algebra]] [[sl(2)]] (see [here](su2#Complexification))

$$
  \mathfrak{su}(2) \otimes_{\mathbb{R}} \mathbb{C}
  \;\simeq\;
  \mathfrak{sl}(2,\mathbb{C})
$$

write

\[
  \label{CanonicalBasisOfsu2C}
  \sigma_i 
    \;\in\; 
  \mathfrak{su}(2) \otimes_{\mathbb{R}} \mathbb{C}
  ,
  \phantom{AAA}
  i \in \{1,2,3\}
\]

for a choice of [[linear basis]] such that the [[Lie bracket]] takes the form

\[
  \label{CommutationRelationsu2}
  [\sigma_i, \sigma_j]
  \;=\;
  i \underset{k}{\sum} \epsilon_{i j k} \sigma_k
  \,.
\]

(Here $\epsilon$ is the [[Levi-Civita symbol]], hence $\epsilon_{\sigma(1), \sigma(2)\sigma(3)} \in \{\pm 1\}$ is the [[signature of a permutation|signature]] of the [[permutation]] $\sigma \in Sym(3)$.)

Notice that the element

\[
  \label{TheUnrepresentedR2}
  \underset{i}{\sum}
  \sigma_i \cdot \sigma_i
  \;\in\;
  U(\mathfrak{su}(2))
\]

is a [[Casimir element]] in the [[universal enveloping algebra]].

Let then 

\[
  \label{TheNDimensionalRepresentation}
  \rho
  \;\colon\;
  \mathfrak{su}(2)
  \longrightarrow
  Mat_{N \times N}
\]

denote [[generalized the|the]] [[complex numbers|complex]] $N$-[[dimension|dimensional]] [[complex numbers|complex]] [[irreducible representation|irreducible]] [[Lie algebra representation]] of [[su(2)]] (hence of $\mathfrak{sl}(2,\mathbb{C})$).


In the discussion of [[angular momentum]] in [[quantum mechanics]] the image  

\[
  \label{TheUnnormalizedR2}
  \underset{i}{\sum}
  \rho_i \circ \rho_i
  \;\in\;
  Mat_{N \times N}
\]

of the [[Casimir element]] (eq:TheUnrepresentedR2) under the representation (eq:TheNDimensionalRepresentation) is traditionally denoted $J^2$, and the canonical [[linear basis]] for the N-dimensional representation $\rho$ (eq:TheNDimensionalRepresentation) is then traditionally denoted $\{\vert j, m \rangle\}_{m = -j}^{m = +j}$ with

\[
  \label{EigenvaluesOfCasimir}
  J^2 \vert j,m\rangle \;=\; j(j+1)
  \phantom{AAA}
  m \in \{-j, -j+1, \cdots, j-1, j\}
  \,.
\]

hence with 

$$
  N(j) = 2 j + 1  
  \;\;
  \Leftrightarrow
  \;\;
  j(N) = \tfrac{1}{2}(N - 1)
  \,.
$$

This means that the [[eigenvalues]] of (eq:TheUnnormalizedR2) as a function not of the [[angular momentum]] $j$ but of the [[dimension]] $N$ of the given [[irreducible representation]] are:

\[
  \label{EigenvaluesOfCasimir}
  \begin{aligned}
    j(N)\big(j(N)+1\big)
    & =
    \phantom{+\;}
    (j(N))^2 + j(N)
    \\
    & =
    \phantom{+\;}
    \tfrac{1}{4}(N-1)^2 + \tfrac{1}{2}(N-1)
    \\
    & =
    \phantom{+\;}  
    \tfrac{1}{4}N^2 - \tfrac{1}{2}N + \tfrac{1}{4}
    \\
    & 
    \phantom{=\;}
    + \tfrac{1}{2}N - \tfrac{1}{2}
    \\
    &
    =
    \phantom{+\;}
    \tfrac{1}{4}N^2 - \tfrac{1}{4}
    \\
    &
    =
    \phantom{+\;}
    \tfrac{1}{4}
    (N^2 - 1)
  \end{aligned}
\]


#### Algebra of functions

Write now

\[
  \label{BasisFunctionsOnFuzzy2Sphere}
  X_i 
    \;\coloneqq\;
  \tfrac
    {2}
    {\sqrt{N^2-1}}
    \rho_N(\sigma_i)
\]

for the [[square matrices]] representing the generators $\sigma_i$ (eq:CanonicalBasisOfsu2C) in the $N$-dimensional complex irrep (eq:TheNDimensionalRepresentation), suitably normalized in view of (eq:EigenvaluesOfCasimir).

(It is here that we need the assumption $N \geq 2$, hence excluding the complex 1-dimensional [[trivial representation|trivial]] [[irrep]].)

Due to the normalization, the commutation relation (eq:CommutationRelationsu2) in this representation reads

\[
  \label{NormalizedCommutationforsu2}
  [X_i, X_j]
  \;=\;
  i 
  \tfrac
    {2}
    {\sqrt{N^2-1}}
  \underset{k}{\sum} \epsilon_{i j k} X_k
\]

and, by (eq:EigenvaluesOfCasimir), the image of the [[Casimir element]] (eq:TheUnrepresentedR2) under this representation is the [[identity matrix]]:

\[
  \label{RadiusOfFuzzy2Sphere}
  \begin{aligned}
    R^2
    & 
    \coloneqq
    \underset{i}{\sum}
    X_i \cdot X_i
    \\
    & =
    I
    \,.
  \end{aligned}
\]

Equation (eq:NormalizedCommutationforsu2) shows that in the [[large N limit]] $N \to \infty$, the algebra generated by the $X_i$ becomes commutative, and (eq:RadiusOfFuzzy2Sphere) says that for any $N$, the algebra generated by the $X_i$ satisfies the same relation as the [[smooth algebra]] on generators $x_i$ restricted to the actual [[2-sphere]] of unit [[radius]]:

$$
  C^\infty
  \big(
    S^2
  \big)
  \;\simeq\;
  SmoothAlg\big( \{x_1, x_2,x_3\}\big)
  \big/
  \Big( 
     \underset{i}{\sum} x_i \cdot x_i   = 1
  \Big)
$$

#### Integration

With the above, the [[volume]] density of the fuzzy 2-sphere scales with 
$\tfrac{1}{\sqrt{N^2-1}}$

$$
  \begin{aligned}
   \tfrac{4\pi i}{3!}
   \epsilon^{i j k } 
    X_i \cdot X_j \cdot X_k
    & =
    \tfrac{4\pi i}{3!}
    \tfrac{1}{2}
    \epsilon^{i j k } 
    [X_i, X_j] \cdot X_k
    \\
    & =
    \tfrac{4\pi i}{3!}
    \tfrac
      {i}
      {\sqrt{N^2-1}}
    \epsilon^{i j k } 
    \epsilon_{i j l} 
    X^l \cdot X_k
    \\
    & =
    \tfrac{4\pi i}{3!}
    \tfrac
      {2i}
      {\sqrt{N^2-1}}
    X^k \cdot X_k
    \\
    & =
    \tfrac{4\pi i}{3!}
    \tfrac
      {2i}
      {\sqrt{N^2-1}}
    \, I
    \\
    & =
    -
    \tfrac{4\pi}{3}
    \tfrac
      {1}
      {\sqrt{N^2-1}}
    \, I
  \end{aligned}   
$$

In this vein, one defines the fuzzy refinement of the [[integral]] of functions over the [[2-sphere]], against its canonical [[volume form]], to be given by the matrix [[trace]], normalized as follows

\[
  \label{FuzzyS2Integration}
  \array{
    \langle X_1, X_2, X_3\rangle
    &\overset{\int_{S^2_N}}{\longrightarrow}&
    \mathbb{C}
    \\
    M &\mapsto& 4 \pi \tfrac{1}{ \sqrt{N^2 -1 } }  tr(M)
  }
\]

With this definition the [[volume]] of the fuzzy 2-sphere of $N$ bits comes out as

$$
  vol(S^2_N)
  \;=\;
  \int_{S^2_N} I
  \;=\;
  \tfrac{4 \pi}{ \sqrt{N^2 - 1 } }  \underset{N}{\underbrace{tr(I)}}
  \;=\;
  4 \pi \tfrac{ N }{ \sqrt{N^2 -1} }
  \,.
$$

This indeed goes to the volume of the actual [[2-sphere]] in the [[limit of a sequence|limit]] $N \to \infty$:

$$
  \underset{N \to \infty}{\lim}
  vol(S^2_N)
  \;=\;
  4 \pi
  \;=\;
  vol(S^2)
  \,.
$$



## Properties

### Shape observables as weight systems on chord diagrams
 {#ShapeObservablesAsVassilievInvariants}


We discuss how the "shape observables" on the fuzzy 2-sphere ([above](#Fuzzy2SphereDefinition)) are given by [[single trace observables]] which are [[Lie algebra weight systems]]
on [[chord diagrams]] (following [Ramgoolam-Spence-Thomas 04](#RamgoolamSpenceThomas04), [McNamara-Papageorgakis 05](#McNamaraPapageorgakis05), see [McNamara 06, Section 4](#McNamara06) for review).

For more see at _[[weight systems on chord diagrams in physics]]_.


<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/WeightSystemsAsShapeObservabesOnFuzzySphere.jpg" width="400">
</div>

\linebreak


While in the commutative [[large N limit]], all powers of the [[radius]] function are equal

$$
  \underset{N\to \infty}{\lim}
  \int_{S^2_N} R^{2 k}
  \;=\;  
  4 \pi 
  \,;
$$

for [[finite number|finite]] $N$ there is an ordering ambiguity: In fact, the number of functions on the fuzzy 2-sphere at finite $N$ that all go to the same function $R^{2k}$ in the [[large N limit]] grows rapidly with $k$.

At $k = 1$ there is the single radius observable (eq:RadiusOfFuzzy2Sphere)

$$
  \int_{S^2_N} R^2 
  \;=\; 
  \int_{S^2_N}
  \underset{i}{\sum} X_i \cdot X_i
  \;=\;
  4 \pi \tfrac{ N }{ \sqrt{N^2 -1} }
$$

At $k = 2$ there are, under the integral (eq:FuzzyS2Integration), two radius observables:

1. $ \int_{S^2_N} \underset{i,j}{\sum} X_i X_i X_j X_j$

1. $\int_{S^2_N} \underset{i,j}{\sum} X_i X_j X_j X_i$

(Here we are using that under the integral/trace, a [[cyclic permutation]] of the factors in the integrand does not change the result).

Similarly for higher $k$, where the number of possible orderings increases rapidly. The [[combinatorics]] that appears here is familiar in [[knot theory]]:

Every ordering of operators, up to cyclic permutation, in the [[single trace observable]] $Tr(R^2)^n$ is encoded in a [[chord diagram]] and the value of the corresponding [[single trace observable]] is the value of the [[su(2)]]-[[Lie algebra weight system]] on this chord diagram.

> from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


## Appearance in D-brane geometry

The [[fuzzy spheres]] appear in [[D-brane geometry]]:

1. the [[fuzzy funnels]] of [[Dp-D(p+2)-brane intersections]] have [[fuzzy 2-sphere]] slices

1. the [[fuzzy funnels]] of [[Dp-D(p+4)-brane intersections]] have [[fuzzy 4-sphere]] slices

1. the [[supersymmetry|supersymmetric]] [[classical field theory|classical]] solutions of the [[BMN matrix model]] are precisely [[fuzzy 2-sphere]] configurations ([BMN 02 (5.4)](BMN+matrix+model#BerensteinMaldacenaNastase02)).


## Related concepts

* [[fuzzy funnel]]

* [[noncommutative torus]]

## References

### General

Review in the context of [[D-brane geometry]], [[matrix models]] of [[string theory]]/[[M-theory]] ([[BFSS matrix model]], [[BMN matrix model]], [[IKKT matrix model]]):

* {#Ydri18} [[Badis Ydri]], _Review of M(atrix)-Theory, Type IIB Matrix Model and Matrix String Theory_ ([arXiv:1708.00734](https://arxiv.org/abs/1708.00734)), published as: _Matrix Models of String Theory_, IOP 2018 ([ISBN:978-0-7503-1726-9](https://iopscience.iop.org/book/978-0-7503-1726-9))


### Fuzzy 2-sphere

On the [[fuzzy 2-sphere]]:

#### General

The [[fuzzy 2-sphere]] was introduced in:

* [[John Madore]], _The Fuzzy sphere_, Class. Quant. Grav. 9 (1992) 69-88 ([spire:314358](http://inspirehep.net/record/314358))

Discussion of the [[spectral triple|spectral]] [[Riemannian geometry]] of the [[fuzzy 2-sphere]]:

* [[Francesco D'Andrea]], [[Fedele Lizzi]], [[Joseph Várilly]], _Metric Properties of the Fuzzy Sphere_, Lett. Math. Phys.103 (2013), 183-205 ([arXiv:1209.0108](https://arxiv.org/abs/1209.0108))

In the context of the [[IKKT matrix model]]:


* [[Harold Steinacker]], _Non-commutative geometry and matrix models_, PoS QGQGS2011 (2011) 004 ([arXiv:1109.5521](https://arxiv.org/abs/1109.5521))



See also:

* Wikipedia, _[Fuzzy sphere](https://en.wikipedia.org/wiki/Fuzzy_sphere)_

#### Observables via weight systems on chord diagrams

Relation of [[Dp-D(p+2)-brane bound states]] ([hence](Dp-Dp+2-brane+bound+states#ReferencesRelationToMonopoles)
[[Yang-Mills monopoles]]) to [[su(2)]]-[[Lie algebra weight systems]] on [[chord diagrams]] computing [[radii]] averages of [[fuzzy spheres]]:

* {#RamgoolamSpenceThomas04} [[Sanyaje Ramgoolam]], [[Bill Spence]], S. Thomas, Section 3.2 of: _Resolving brane collapse with $1/N$ corrections in non-Abelian DBI_, Nucl. Phys. B703 (2004) 236-276 ([arxiv:hep-th/0405256](https://arxiv.org/abs/hep-th/0405256))

* {#McNamaraPapageorgakis05} [[Simon McNamara]], [[Constantinos Papageorgakis]], [[Sanyaje Ramgoolam]], [[Bill Spence]], Appendix A of: _Finite $N$ effects on the collapse of fuzzy spheres_, JHEP 0605:060, 2006 ([arxiv:hep-th/0512145](https://arxiv.org/abs/hep-th/0512145))

* {#McNamara06} [[Simon McNamara]], Section 4 of: _Twistor Inspired Methods in Perturbative FieldTheory and Fuzzy Funnels_, 2006 ([spire:1351861](http://inspirehep.net/record/1351861), [pdf](https://strings.ph.qmul.ac.uk/sites/default/files/Mcnamaraphd.pdf), [[McNamara06.pdf:file]])

* [[Constantinos Papageorgakis]], p. 161-162 of: _On matrix D-brane dynamics and fuzzy spheres_, 2006 ([[Papageorgakis06.pdf:file]])

### Fuzzy 3-sphere

The [[fuzzy 3-sphere]] was first discussed (in the context of [[D0-brane]]-systems) in 

* Z. Guralnik, [[Sanyaje Ramgoolam]], _On the Polarization of Unstable D0-Branes into Non-Commutative Odd Spheres_, JHEP 0102:032, 2001 ([arXiv:hep-th/0101001](https://arxiv.org/abs/hep-th/0101001))

Discussion in the context of [[M2-M5-brane bound states]]/[[E-strings]]:

* {#BasuHarvey05} [[Anirban Basu]], [[Jeffrey Harvey]], _The M2-M5 Brane System and a Generalized Nahm's Equation_, Nucl.Phys. B713 (2005) 136-150 ([arXiv:hep-th/0412310](https://arxiv.org/abs/hep-th/0412310))

### Fuzzy 4-sphere

The [[fuzzy 4-sphere]]:

* [[Harald Grosse]], [[Ctirad Klimcik]], P. Presnajder, _On Finite 4D Quantum Field Theory in Non-Commutative Geometry_, Commun. Math. Phys.180:429-438, 1996 ([arXiv:hep-th/9602115](https://arxiv.org/abs/hep-th/9602115))

* Judith Castelino, Sangmin Lee, [[Washington Taylor]], _Longitudinal 5-branes as 4-spheres in Matrix theory_, Nucl. Phys. B526:334-350, 1998 ([arXiv:hep-th/9712105](https://arxiv.org/abs/hep-th/9712105))

  (via [[D5-branes]])

### Fuzzy 6-sphere and higher

The [[fuzzy 6-sphere]] and higher:

* [[Sanjaye Ramgoolam]], Section 5 of: _On spherical harmonics for fuzzy spheres in diverse dimensions_, Nucl. Phys. B610: 461-488, 2001 ([arXiv:hep-th/0105006](https://arxiv.org/abs/hep-th/0105006))

* Yusuke Kimura, _On Higher Dimensional Fuzzy Spherical Branes_,  	Nucl. Phys. B664 (2003) 512-530 ([arXiv:hep-th/0301055](https://arxiv.org/abs/hep-th/0301055))

* Francesco Pisacane, _$O(D)$-equivariant fuzzy spheres_ ([arXiv:2002.01901](https://arxiv.org/abs/2002.01901))

[[!redirects fuzzy spheres]]

[[!redirects fuzzy sphere]]
[[!redirects fuzzy spheres]]

[[!redirects fuzzy 2-sphere]]
[[!redirects fuzzy 2-spheres]]

[[!redirects fuzzy 3-sphere]]
[[!redirects fuzzy 3-spheres]]

[[!redirects fuzzy 4-sphere]]
[[!redirects fuzzy 4-spheres]]

[[!redirects fuzzy 6-sphere]]
[[!redirects fuzzy 6-spheres]]

