
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
  A_k \otimes A_{n-k} \stackrel{\otimes}{\to} A^n \stackrel{\epsilon}{\to} k
$$

are non-degenerate.

=--

e.g. ([Lambrechst-Stanley 07](#LambrechstStanley07))

### For $C^\ast$-algebras
 {#ForCStarAlgebras}

For [[C*-algebras]] hence in [[noncommutative topology]] there is the following notion of Poincar&#233; duality, which is really Poincar&#233; with respect not to [[ordinary cohomology]] but [[K-theory]] ([[operator K-theory]]).

+-- {: .num_defn #PDAlgebra}
###### Definition

A [[separable C*-algebra]] $A \in $ [[C*Alg]] is a **Poincar&#233; duality algebra** (or _PD algebra_, for short ) if it is [[dualizable object]] when regarded as an object of the [[KK-theory]]-category, with [[dual object]] its [[opposite algebra]].

=--

([BMRS 07, def. 2.1](#BMRS07), following [Connes, p. 601](#Connes))


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

+-- {: .num_remark}
###### Remark

The element $\Delta$ in def. \ref{PDAlgebra} is called a **[[fundamental class]]** of $A$. 

=--

+-- {: .num_remark}
###### Remark

For $C^\ast$-algebras which are [[groupoid convolution algebras]] $C^\ast(\mathcal{G})$ the [[opposite algebra]] is [[Morita equivalence|Morita equivlant]] (since a [[groupoid]] $\mathcal{G}$ is [[equivalence of categories|equivalent]] to its [[opposite category|opposite groupoid]] $\mathcal{G}^{op}$, the equivalence being induced by the [[functor]] which sends a morphism to its [[inverse]]). But given a [[circle 2-bundle]] $\chi \colon \mathcal{G} \to \mathbf{B}^2 U(1)$ the corresponding [[twisted groupoid convolution algebra]] is such that passing to the opposite corresponds to passing to the inverse twist $- chi$. (...)

=--

## Properties

### For dg-Algebras

### For $C^\ast$-algebras

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


+-- {: .num_prop}
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

[[!redirects Poincaré duality algebras]]

[[!redirects Poincare duality algebra]]
[[!redirects Poincare duality algebras]]

[[!redirects Poincaré duality C*-algebra]]
[[!redirects Poincaré duality C*-algebras]]

[[!redirects Poincare duality C*-algebra]]
[[!redirects Poincare duality C*-algebras]]

