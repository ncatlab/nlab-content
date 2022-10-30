
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Super-Algebra and Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Deligne's theorem on tensor categories ([Deligne 02](#Deligne02)) establishes [[Tannaka duality]] between sufficiently well-behaved linear [[tensor categories]] in [[characteristic zero]] and [[supergroups]] ("[[supersymmetries]]"), realizing these tensor categories as [[categories of representations]] of these supergroups.

The theorem hence gives a purely mathematical "reason" for the relevance of [[superalgebra]] and [[supergeometry]]. 

For instance one may wonder why of all possible generalizations of [[commutative algebra]], it is supercommutative superalgebras that are to be singled out (from alternatives such as plain $\mathbb{Z}_2$-[[graded algebras]], or in fact $\mathbb{Z}_n$-graded algebras or general [[noncommutative algebras]] or, the like), as they are singled out notably in theoretical [[physics]] ("[[supersymmetry]]"), but also in mathematical fields such as [[spin geometry]] and [[K-theory]]. On the other hand $k$-linear [[tensor categories]] need little extra motivation, they are on general abstract ground the canonical structure to consider in [[representation theory]]. Hence Deligne's theorem serves to base supercommutative superalgebra on this same general abstract foundation, showing that this is precisly the context in which full $k$-linear tensor categories exhibit full [[Tannaka duality]].

More concretely, in [[quantum field theory]], under the [[Wigner classification]], [[fundamental particles]] are identified with [[irreducible representations]] of the [[isometry group]] of the local model of [[spacetime]]. Forming the [[tensor product]] of two such representations corresponds to combining them as two [[subsystems]] of a joint system. Therefore it is natural to demand that physical particle species should form complex-linear [[tensor categories]]. Deligne's theorm then gives that [[supersymmetry]] is the most general context in which this works out. (In physics the irreducible representation in this context here are called the _[[supermultiplets]]_.)




## Statement

Let $k$ be an [[algebraically closed field]] of [[characteristic zero]] (for instance the [[complex numbers]]).

+-- {: .num_defn #TensorCategory}
###### Definition

A _$k$-[[tensor category]]_ $\mathcal{A}$ is a [[rigid monoidal category|rigid]] [[symmetric monoidal category|symmetric]] [[braided monoidal category]] [[enriched category|enriched]] over $k$[[Mod]].

=--

+-- {: .num_defn #SchurFunctor}
###### Definition

For $(\mathcal{A},\otimes)$ a $k$-[[tensor category]] as in def.\ref{TensorCategory}, for $X \in \mathcal{A}$ an [[object]], for $n \in \mathbb{N}$ and $\lamba$ a [[partition]] of $n$, say that the value of the [[Schur functor]] $S_\lambda$ on $X$ is

$$
  S_{\lambda}(X) \coloneqq (V_\lambda \otimes X^{\otimes_n})^{S_2}
  \coloneqq 
  \left(
    \underset{g\in S_n}{\sum}
    \rho(g)
  \right)
  \left(
    V_\lambda \otimes X^{\otimes_n}
  \right)
$$

where

* $S_n$ is the [[symmetric group]] on $n$ elements;

* $V_\lambda$ is the [[irreducible representation]] of $S_n$ corresponding to $\lambda$;

* $\rho$ is the diagional [[action]] of $S_n$ on $V_\lambda \otimes X^{\otimes_n}$, coming from the canonical [[permutation]] action on $X^{\otimes_n}$.

=--

+-- {: .num_defn #Regularity}
###### Definition

A $k$-[[tensor category]] $(\mathcal{A}, \otimes)$  as in def.\ref{TensorCategory}
is _regular_ if 

1. it _[[finitely generated object|finitegy generated]]_ in that there exsists an [[object]] $E \in \mathcal{A}$ such that every other object is a [[subquotient]] of a [[direct sum]] $E^{\otimes_n}$, for some $n \in \mathbb{N}$;

1. for every [[object]] $X\in \mathcal{A}$ there exists $n \in \mathbb{N}$ and a [[partition]] $\lambda$ of $n$ such that the corresponding value of the [[Schur functor]], def. \ref{SchurFunctor}, vanishes: $S_\lambda(X) = 0$.

=--

+-- {: .num_defn #Supergroup}
###### Definition

An (algebraic) _[[supergroup]]_ $G$ is the [[formal dual]] of a supercommutative [[superalgebra|super]] [[Hopf algebra]] $\mathcal{O}(G)$.

=--

+-- {: .num_defn #Superrepresentation}
###### Definition

A super-pointing of such $G$ is an element $\epsilon \in G_{even}$ (i.e. an algebra homomorphism $\mathcal{O}(G) \to k$), which is [[involution|involutive]] i.e. $\epsilon^2 = 1$ and such that its [[adjoint action]] on $G$ is the parity involution.

Say that a super-[[representation]] of $(G,\epsilon)$ is a superrepresentation of $G$ on a [[finite number|finite]] [[dimension|dimensional]] [[super vector space]] over $k$ such that $\epsilon$ is taken to the parity endomorphism which is the identity on even graded vectors and multiplication with $(-1)$ on odd-graded vectors.

=--

+-- {: .num_example}
###### Example

For $H$ a supergroup and $\mathbb{Z}_2 = \{id,\epsilon\}$ acting on it by parity incolution, then the [[semidirect product]] $\mathbb{Z}_2 \ltimes G$ equipped with $\epsilon \in \mathbb{Z}_2 \hookrightarrow \mathbb{Z}_2 \ltimes G$.

=--


+-- {: .num_example #RegularTensorCategoriesOfSuperrepresentations}
###### Example

The super-[[representation category]] $Rep(G,\epsilon)$, def. \ref{Superrepresentation} of an algebraic [[supergroup]] $G$, def. \ref{Supergroup}, with superpointing $\epsilon$ is a regular $k$-[[tensor category]], def.\ref{Regularity}.

=--

+-- {: .num_theorem}
###### Theorem

Every regular $k$-tensor category $\mathcal{A}$, def. \ref{Regularity} is [[equivalence of categories|equivalent]] to one of the form $Rep(G,\epsilon)$, example \ref{RegularTensorCategoriesOfSuperrepresentations}, for some [[supergroup]] $G$.

=--



## References

The theorem is due to

* {#Deligne02} [[Pierre Deligne]], _Cat&#233;gorie Tensorielle_, Moscow Math. Journal 2 (2002) no. 2, 227-248. ([pdf](https://www.math.ias.edu/files/deligne/Tensorielles.pdf))

building on

* [[Pierre Deligne]], _[[Catégories Tannakiennes]]_, Grothendieck Festschrift, vol. II, Birkh&#228;user Progress in Math. 87 (1990) pp.111-195.

Review includes

* [[Pavel Etingof]], [[Shlomo Gelaki]], _The classification of finite-dimensional triangular Hopf algebras over an algebraically closed field of characteristic 0_ ([arXiv:0202258](http://de.arxiv.org/abs/math/0202258))

* {#Ostrik04} [[Victor Ostrik]], _Tensor categories (after P. Deligne)_ ([arXiv:math/0401347](http://arxiv.org/abs/math/0401347))




[[!redirects Deligne reconstruction theorem]]