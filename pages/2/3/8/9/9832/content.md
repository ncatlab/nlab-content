
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Noncommutative geometry
+--{: .hide}
[[!include noncommutative geometry - contents]]
=--
#### Operator algebra
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Generally, a _Poincar&#233; duality dg-algebra_ is a [[dg-algebra]] with structure mimicking [[Poincaré duality]] in [[ordinary cohomology]].

On the other hand a _Poincar&#233; duality $C^\ast$-algebra_
is a [[C*-algebra]] which represents a [[space]] in [[noncommutative topology]] for which there is a sensible notion of [[Poincaré duality]] in [[K-theory]] ([[operator K-theory]]/[[K-homology]]).

## Definition

### For graded-commutative algebras
 {#ForGradedCommutativeAlgebras}

+-- {: .num_defn }
###### Definition

The structure of a Poincar&#233; duality algebra in [[dimension]] $n$
on a graded-commutative [[graded vector space|graded]] [[associative algebra]] $A$ is a [[linear function]] $\epsilon \colon A_n \to k$ to the ground field such that all the induced [[bilinear forms]]

$$
  A_k \otimes A_{n-k} \stackrel{\otimes}{\to} A_n \stackrel{\epsilon}{\to} k
$$

are non-degenerate.

=--

e.g. ([Lambrechst-Stanley 07](#LambrechstStanley07))

### For $C^\ast$-algebras
 {#ForCStarAlgebras}

For [[C*-algebras]] hence in [[noncommutative topology]] there is the following notion of Poincar&#233; duality, which is really Poincar&#233; with respect not to [[ordinary cohomology]] but [[K-theory]] ([[operator K-theory]]).

We start with the definition of Poincar&#233; _self_-duality and then generalize to Poincar&#233; dual pairs.

+-- {: .num_defn #PDAlgebra}
###### Definition

A [[separable C*-algebra]] $A \in $ [[C*Alg]] is a **Poincar&#233; duality algebra** (or _PD algebra_, for short ) if it is [[dualizable object]] when regarded as an object of the [[KK-theory]]-category, with [[dual object]] its [[opposite algebra]].

The element $\Delta$ in def. \ref{PDAlgebra} is called a **[[fundamental class]]** of $A$. 

=--

This appears as ([BMRS 07, def. 2.1](#BMRS07), following [Connes, p. 601](#Connes)) following ([Connes](#Connes)).


+-- {: .num_remark}
###### Remark

Explicitly def. \ref{PDAlgebra} says that $A$ is a PD algebra if there exists $\Delta \in KK(A \otimes A^{op}, \mathbb{C})$ and $\Delta^\vee \in KK(\mathbb{C}, A \otimes A^{op})$ such that 

$$
  \Delta^\vee \otimes_{A^{op}} \Delta = id_A \in KK(A,A)
$$

and

$$
  \Delta^\vee \otimes_A \Delta = id_{A^{op}} \in KK(A^{op}, A^{op})
  \,. 
$$

=--


+-- {: .num_prop}
###### Definition/Proposition

For $A$ $B$ two Poincar&#233; duality algebras, def. \ref{PDAlgebra\}, and for $f \colon A \to B$ a [[homomorphism]] between them, regarded as a morphism $f^\ast \colon B \to A$ in [[KK-theory]], the correspondung [[dual morphism]] $f! \colon A \to B$ is the one such that postcomposition in $KK$ with this corresponds to the [[Umkehr map]]/[[push forward in generalized cohomology]] in [[KK-theory]].

=--

For more on this see below at _[Properties -- K-Orientation and Umkehr mpas](#PropertiesKOrientationAndUmkehrMaps)_.


+-- {: .num_remark #OppositeConvolutionAlgebraAndInverseTwist}
###### Remark

For $C^\ast$-algebras which are [[groupoid convolution algebras]] $C^\ast(\mathcal{G})$ the [[opposite algebra]] is [[Morita equivalence|Morita equivlant]] (since a [[groupoid]] $\mathcal{G}$ is [[equivalence of categories|equivalent]] to its [[opposite category|opposite groupoid]] $\mathcal{G}^{op}$, the equivalence being induced by the [[functor]] which sends a morphism to its [[inverse]]). But given a [[circle 2-bundle]] $\chi \colon \mathcal{G} \to \mathbf{B}^2 U(1)$ the corresponding [[twisted groupoid convolution algebra]] is such that passing to the opposite corresponds to passing to the inverse twist $-\chi$. 

=--

Therefore it makes sense to consider more generally

+-- {: .num_defn}
###### Definition

For $A$ a [[C*-algebra]] a _Poincar&#233; dual_ for $A$ is a [[dual object]] $B \in C^\ast Alg \to KK$ in [[KK-theory]].  

=--


Below in the [Proposition-Section](#PropertiesForCStarAlgebras) is discussed how under Poincar&#233;-duality the [[twisted K-theory|twist]] changes.



## Properties

### For dg-Algebras

### For $C^\ast$-algebras
 {#PropertiesForCStarAlgebras}

#### Duals and twists
 {#PropertiesCAstDualsAndTwists}

+-- {: .num_prop}
###### Proposition

Let $X$ be a [[closed manifold]] with [[spin^c-structure]]. Then there is a Poincar&#233; duality [[isomorphism]]

$$
  K^\bullet(X) \simeq K_\bullet(X)
  \,.
$$

=--

For instance ([Connes, chapter 2.7, prop. 5](#Connes)).

(...) The relaton between Poincar&#233; duality on algebras of functions and [[spin^c-structure]] is discussed in ([Connes, around p. 603](#Connes)). (...)

Notice that the [[obstruction]] to [[spin^c structure]] is the third [[integral Stiefel-Whitney class]] $W_3 \colon B SO \to B^2 U(1)$. If this does not vanish on a [[manifold]], then a Poincar&#233; dual/[[dual object]] in [[KK-theory]] still exists, but is the same manifold equipped with a [[twisted K-theory|twist]] _shifted_ by $W_3(\tau_X)$, where $\tau_X$ denotes the ([[cotangent bundle|co]])[[tangent bundle]] of $X$.

+-- {: .num_defn #CStarAlgebraOf2BundleOnManifold}
###### Definition/Notation

For $X$ a ([[compact topological space|compact]]) [[manifold]] and $c \in H^3(X,\mathbb{Z})$ the class of a [[circle 2-bundle]]/[[bundle gerbe]] $\mathcal{G}$ on $X$, write 

$$
  C_c(X) \in C^\ast Alg \to KK
$$

for the corresponding [[twisted groupoid convolution algebra]], the one whose [[operator K-theory]] is the $c$-[[twisted K-theory]] of $X$:

$$
  KK_\bullet(\mathbb{C}, C_c(X)) \simeq K_{\bullet + c}(X)
  \,.
$$


=--

+-- {: .num_prop #DualOfCompactManifoldWithTwist}
###### Proposition

Let $X$ be a [[compact topological space|compact]] [[manifold]] with [[tangent bundle]] $\tau_X$ and let $c \in H^3(X,\mathbb{Z})$ be a [[twisted K-theory|twist]]. Then the [[C*-algebra]] $C_{c}(X)$ of def. \ref{CStarAlgebraOf2BundleOnManifold} has a [[dual object]] in the [[full subcategory]] of [[KK-theory]] on [[separable C*-algebras]], given by

$$
  (C_c(X))^\vee
  \simeq
  C_{\frac{1}{c\otimes W_3(\tau_X)}}(X)
  \,,
$$

hence by the same manifold but with twist the inverse of the third [[integral Stiefel-Whitney class]] and the original twist.

The same remains true in $G$-equivariant KK-theory, for $G$ a [[locally compact topological space|locally compact]] [[topological group]].

=--

The non-equivariant case is in ([Brodzki-Mathai-Rosenberg-Szabo 06, section 7.3](#BrodzkiMathaiRosenbergSzabo06)) and the generalization to the equivariant case in ([Tu 06, theorem 3.1](#Tu06)) (where we use remark \ref{OppositeConvolutionAlgebraAndInverseTwist} in order to interpret the opposite twisted convolution algebra up to equivalence as inducing the inverse twist).


#### K-Orientation and Umkehr maps
 {#PropertiesKOrientationAndUmkehrMaps}

We discuss [[Umkehr maps]]/[[fiber integration in generalized cohomology]] in [[K-theory]] using Poincar&#233; duality algebras / [[dual objects]] in [[KK-theory]].

+-- {: .num_prop }
###### Proposition

Every homomorphism $f \colon A \to B$ between PD $C^\ast$-algebras is [[K-orientation|K-orientable in KK-theory]]. The [[K-orientation]] is given by the corresponding [[dual morphism]], hence the element $f! \colon B \to A$ given as the composite

$$
  f!
  \coloneqq
  \Delta^\vee_A \otimes_{A^{op}} f^{op} \otimes_{B^{op}} \Delta_B
  \,.
$$

=--

([BMRS 07, 3.3](#BMRS07))

More generally we have the following.

+-- {: .num_example #PushAlongInclusionOfManifoldsAndDBraneCharge}
###### Example

Let $i \colon Q \to X$ be a map of [[compact topological space|compact]] [[manifolds]] and let $\chi \colon X \to B^2 U(1)$ modulate a [[circle 2-bundle]] regarded as a [[twisted K-theory|twist for K-theory]]. Then forming [[twisted groupoid convolution algebras]] yields a [[KK-theory]] morphism of the form

$$
  C_{i^\ast \chi}(Q)
  \stackrel{i^\ast}{\longleftarrow}
  C_{\chi}(X)
  \,,
$$

with notation as in def. \ref{CStarAlgebraOf2BundleOnManifold}. By prop. \ref{DualOfCompactManifoldWithTwist} the [[dual morphism]] is of the form

$$
  C_{\frac{1}{i^\ast \chi \otimes W_3(T Q)}}(Q)
  \stackrel{i_!}{\longrightarrow}
  C_{\frac{1}{\chi \otimes W_3(T X)}}(X)
  \,.
$$

If we redefine the twist on $X$ to absorb this "quantum correction" as $\chi \mapsto \frac{1}{\chi \otimes W_3(T X)}$ then this is

$$
  C_{i^\ast \chi\frac{W_3(i^\ast T X)}{W_3(T Q)}}(Q)
  \stackrel{i_!}{\longrightarrow}
  C_{\chi}(X)
  \,,
$$

Postcomposition with this map in [[KK-theory]] now yields a map from the $i^\ast \chi \otimes W_3(N Q)$-[[twisted K-theory]] of $Q$ to the $\chi$-[[twisted K-theory]] of $X$:

$$
  i_! \colon K_{\bullet + W_3(N Q) + i^\ast \chi}(Q) \to K_{\bullet +\chi}
  \,.
$$

This is the _[[twisted Umkehr map]]_ in this context.

If we here think of $i \colon Q \hookrightarrow X$ as being the inclusion of a [[D-brane]] [[worldvolume]], then $\chi$ would be the class of the [[background gauge field|background]] [[B-field]] and an element 

$$
  [\xi] \in K_{\bullet + W_3(N Q) + i^\ast \chi}(Q)
$$ 

is called (the K-class of) a _[[Chan-Paton gauge field]]_ on the D-brane satisfying the [[Freed-Witten-Kapustin anomaly cancellation]] mechanism. (The orginal [[Freed-Witten anomaly cancellation]] assumes $\xi$ given by a [[twisted unitary bundle|twisted line bundle]] in which case it exhibits a [[twisted spin^c structure]] on $Q$.)
Finally its [[fiber integration|push-forward]]

$$
  [i_! \xi] \in K_{\bullet- \chi}(X)
$$

is called the corresponding _[[D-brane charge]]_.


=--

See ([Nuiten 13](#Nuiten13)).


## Examples

+-- {: .num_example}
###### Example

For $A = C_0(X)$ the [[algebra of functions]] on a [[compact topological space|compact]] [[complex manifold]] $X$, then $A$ is a PD algebra with fundamental class $\Delta$ in [[K-homology]] given by the [[Dolbeault operator]] on $X \times X$.

=--

([BMRS 07, example 3.2](#BMRS07))


+-- {: .num_example}
###### Example

For $A = C_0(X)$ the [[algebra of functions]] [[vanishing at infinity]] of a [[manifold]] $X$ with [[spin^c structure]]. Take $B = C_0(T^\ast X) \simeq_{KK} A^{op} \simeq A$. Then $\Delta$ constructed from the [[Dirac operator]] on the [[Clifford algebra bundle]] over $T^\ast X$ is a fundamental class.

=--

([BMRS 07, proof of theorem 2.9](#BMRS07))

## Related concepts

* [[fundamental class]]

* [[virtual fundamental class]]

* [[Poincaré duality complex]]

## References

### For graded associative algebras

* Pascal Lambrechts, Don Stanley, _Poincar&#233; duality and commutative differential graded algebras_ ([arXiv:math/0701309](http://arxiv.org/abs/math/0701309))
 {#LambrechstStanley07}

### For $C^\ast$-algebras

For [[C*-algebras]]/in [[noncommutative topology]]:

* [[Henri Moscovici]], _Eigenvalue inequalities and Poincar&#233; duality in noncommutative geometry_, Commun. Math. Phys. 184 , 3 (1997) 619

Chapter 6.4 $\beta$ (starting p. 601) in

* [[Alain Connes]], _[[Noncommutative Geometry]]_
 {#Connes}

Def. 2.1 in 

* Jacek Brodzki, [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], _Noncommutative correspondences, duality and D-branes in bivariant K-theory_, Adv. Theor. Math. Phys.13:497-552,2009 ([arXiv:0708.2648](http://arxiv.org/abs/0708.2648))
 {#BMRS07}

Duality including the [[twisted K-theory]] induced by [[twisted spin^c structure]] over [[manifolds]] is discussed in section 7 of

* Jacek Brodzki, [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]], _D-Branes, RR-Fields and Duality on Noncommutative Manifolds_, Commun. Math. Phys. 277:643-706,2008 ([arXiv:hep-th/0607020](http://arxiv.org/abs/hep-th/0607020))
 {#BrodzkiMathaiRosenbergSzabo06}

and generalized to equivariant [[KK-theory]] in

* [[Jean-Louis Tu]], _Twisted K-theory and Poincar&#233; duality_ ([arXiv:math/0609556](http://arxiv.org/abs/math/0609556))
 {#Tu06}

More on dual objects in KK is in 

* [[Heath Emerson]], [[Ralf Meyer]], _Bivariant K-theory via correspondences_, Adv. Math. 225 (2010), 2883-2919 ([arXiv:0812.4949](http://arxiv.org/abs/0812.4949))

* [[Heath Emerson]], [[Ralf Meyer]], _Dualities in equivariant Kasparov theory_ ([arXiv:0711.0025](http://arxiv.org/abs/0711.0025))


Discussion of the [[twisted Umkehr map]] and the [[Freed-Witten-Kapustin anomaly]] in this context is in

* [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_, master thesis, August 2013
 {#Nuiten13}



[[!redirects Poincaré duality algebras]]

[[!redirects Poincare duality algebra]]
[[!redirects Poincare duality algebras]]

[[!redirects Poincaré duality C*-algebra]]
[[!redirects Poincaré duality C*-algebras]]

[[!redirects Poincare duality C*-algebra]]
[[!redirects Poincare duality C*-algebras]]

