
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

Deligne's theorem on tensor categories ([Deligne 02](#Deligne02), recalled as theorem \ref{TheTheorem} below) establishes [[Tannaka duality]] between linear [[tensor categories]] in [[characteristic zero]] subject to mild size constraint, and [[supergroups]] ("[[supersymmetries]]"), realizing these tensor categories as [[categories of representations]] of these supergroups.

## Relevance

### For supersymmetry

The theorem hence gives a purely mathematical "reason" for the relevance of [[superalgebra]] and [[supergeometry]]. 

For instance one may wonder why of all possible generalizations of [[commutative algebra]], it is supercommutative superalgebras that are to be singled out (from alternatives such as plain $\mathbb{Z}_2$-[[graded algebras]], or in fact $\mathbb{Z}_n$-graded algebras or general [[noncommutative algebras]] or, the like), as they are singled out notably in theoretical [[physics]] ("[[supersymmetry]]"), but also in mathematical fields such as [[spin geometry]] and [[K-theory]]. On the other hand $k$-linear [[tensor categories]] need little extra motivation, they are on general abstract ground the canonical structure to consider in [[representation theory]]. Hence Deligne's theorem serves to base supercommutative superalgebra on this same general abstract foundation, showing that this is precisely the context in which full $k$-linear tensor categories exhibit full [[Tannaka duality]].

More concretely, in [[quantum field theory]], under the [[Wigner classification]], [[fundamental particles]] are identified with [[irreducible representations]] of the [[isometry group]] of the local model of [[spacetime]]. Forming the [[tensor product]] of two such representations corresponds to combining them as two [[subsystems]] of a joint system. Therefore it is natural to demand that physical particle species should form complex-linear [[tensor categories]]. Deligne's theorem then gives that [[supersymmetry]] is the most general context in which this works out. (In physics the irreducible representation in this context here are called the _[[supermultiplets]]_.)

### For Tannaka duality of Hopf algebras
 {#RelevanceForHopfAlgebras}

By [[Tannaka duality]] rigid symmetric monoidal categories in general are [[categories of modules]] of [[triangular Hopf algebras]]. Hence Deligne's theorem here implies that those triangular Hopf algebras whose category of representation in addition satisfies a certain regularity condition (def. \ref{Regularity} below) are equivalent to supercommutative Hopf algebras. See ([Etingof-Gelaki 02](#EtingofGelaki02)) for more.

[[!include structure on algebras and their module categories - table]]




## Statement
 {#Statement}

Let $k$ be an [[algebraically closed field]] of [[characteristic zero]] (for instance the [[complex numbers]]).

### Tensor categories

+-- {: .num_defn #TensorCategory}
###### Definition

A _$k$-[[tensor category]]_ $\mathcal{A}$ is a [[rigid monoidal category|rigid]] [[symmetric monoidal category|symmetric]] [[braided monoidal category]] [[enriched category|enriched]] over $k$[[Mod]].

=--

+-- {: .num_defn #SchurFunctor}
###### Definition

For $(\mathcal{A},\otimes)$ a $k$-[[tensor category]] as in def.\ref{TensorCategory}, for $X \in \mathcal{A}$ an [[object]], for $n \in \mathbb{N}$ and $\lambda$ a [[partition]] of $n$, say that the value of the [[Schur functor]] $S_\lambda$ on $X$ is

$$
  S_{\lambda}(X) \coloneqq (V_\lambda \otimes X^{\otimes_n})^{S_n}
  \coloneqq 
  \left(
    \frac{1}{n!}
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

* $\rho$ is the diagional [[action]] of $S_n$ on $V_\lambda \otimes X^{\otimes_n}$, coming from the canonical [[permutation]] action on $X^{\otimes_n}$;

* $(-)^{S_n}$ denotes the subspace of [[invariants]] under the action $\rho$ 

* the last expression just rewrites this as a [[group averaging]].

=--

([Deligne 02, 1.4](#Deligne02))

+-- {: .num_defn #Regularity}
###### Definition

A $k$-[[tensor category]] $(\mathcal{A}, \otimes)$  as in def.\ref{TensorCategory}
is _regular_ if 

1. it _[[finitely generated object|finitely generated]]_ in that there exsists an [[object]] $E \in \mathcal{A}$ such that every other object is a [[subquotient]] of a [[direct sum]] $E^{\otimes_n}$, for some $n \in \mathbb{N}$;

1. for every [[object]] $X\in \mathcal{A}$ there exists $n \in \mathbb{N}$ and a [[partition]] $\lambda$ of $n$ such that the corresponding value of the [[Schur functor]], def. \ref{SchurFunctor}, vanishes: $S_\lambda(X) = 0$.

=--

### Supergroups

+-- {: .num_defn #Supergroup}
###### Definition

An affine algebraic _[[supergroup]]_ $G$ is the [[formal dual]] of a [[super-commutative Hopf algebra]] $\mathcal{O}(G)$.

=--

We will just say "supergroup" for short in all of the following.

+-- {: .num_defn #ParityAutomorphism}
###### Definition

Given a [[superalgebra]] such as $\mathcal{O}(G)$, its _parity involution_ is the algebra [[automorphism]] which on homogeneously graded elements $a$ of degree $deg(a) \in \{even,odd\} = \mathbb{Z}/2\mathbb{Z}$ is multiplication by the dgeree

$$
  a \mapsto (-1)^{deg(a)}a
  \,.
$$

(e.g. [arXiv:1303.1916, 7.5](http://arxiv.org/abs/1303.1916)). On [[formal duals]] $G$ this induces correspondingly an involutive _parity automorphism_

$$
  par \colon G \stackrel{\simeq}{\longrightarrow} G
  \,.
$$ 

=--

It is convenient in the following to assume that parity involution is an [[inner automorphism]]:

+-- {: .num_defn #InnerParity}
###### Definition

An _inner parity_ of a [[supergroup]] $G$, def. \ref{Supergroup} is an element $\epsilon \in G_{even}$ (i.e. an algebra homomorphism $\mathcal{O}(G) \to k$), which is [[involution|involutive]] i.e. $\epsilon^2 = 1$ and such that its [[adjoint action]] on $G$ is the parity involution of def. \ref{ParityAutomorphism}.

=--

([Deligne 02, 0.3](#Deligne02))

+-- {: .num_example}
###### Example

For $G$ an ordinary (affine algebraic) group, regarded as a supergroup with trivial odd-graded part, then every element $\epsilon \in Z(G)$ in the [[center]] defines an inner parity, def. \ref{InnerParity}. 

=--

([Deligne 02, 0.4 i)](#Deligne02))

+-- {: .num_remark}
###### Remark

In this sense, specifying an involutive central element in an ordinary group is a faint shadow of genuine supergroup structure. In fact such pairs are being referred to as "supergroups" in ([M&#252;ger 06](#Mueger06)).

=--

Demanding the existence of inner parity is not actually a restriction of the theory:

+-- {: .num_example}
###### Example

For $H$ any supergroup, def. \ref{Supergroup}, and $\mathbb{Z}_2 = \{id,par\}$ acting on it by parity involution, def. \ref{ParityAutomorphism}  then the [[semidirect product]] $\mathbb{Z}_2 \ltimes G$ has inner parity, def. \ref{InnerParity}, given by $\epsilon \coloneqq par \in \mathbb{Z}_2 \hookrightarrow \mathbb{Z}_2 \ltimes G$.

=--

([Deligne 02, 0.4 ii)](#Deligne02))

### Representation categories

+-- {: .num_defn #Superrepresentation}
###### Definition


A _super-[[representation]]_ of a [[supergroup]] $G$, def. \ref{Supergroup}, with inner parity $\epsilon$, def.\ref{InnerParity}, is a superrepresentation of $G$ on a [[finite number|finite]] [[dimension|dimensional]] [[super vector space]] $V$ over $k$ such that $\epsilon$ is taken to the parity endomorphism of $V$ (which is the identity on even graded vectors and multiplication with $(-1)$ on odd-graded vectors).

=--

+-- {: .num_example}
###### Example

For $G$ an ordinary (affine algebraic) group regarded as a supergroup with trivial odd-graded part, and for $\epsilon = 1$ its neutral element taken as the inner parity, then $Rep(G,\epsilon)$ in the sense of def. \ref{Superrepresentation} is just the ordinary [[category of representations]] of $G$.

=--

([Deligne 02, 0.4 i)](#Deligne02))

+-- {: .num_prop #RegularTensorCategoriesOfSuperrepresentations}
###### Proposition

The super-[[representation category]] $Rep(G,\epsilon)$, def. \ref{Superrepresentation} of an algebraic [[supergroup]] $G$, def. \ref{Supergroup}, with inner parity $\epsilon$ is a regular $k$-[[tensor category]], def.\ref{Regularity}.

=--

([Deligne 02, 1.21](#Deligne02))

+-- {: .num_theorem #TheTheorem}
###### Theorem

Every regular $k$-tensor category $\mathcal{A}$, def. \ref{Regularity} is [[equivalence of categories|equivalent]] to one of the form $Rep(G,\epsilon)$, example \ref{RegularTensorCategoriesOfSuperrepresentations}, for some [[supergroup]] $G$.

=--

([Deligne 02, theorem 0.6](#Deligne02))


## References

The theorem is due to

* {#Deligne02} [[Pierre Deligne]], _Cat&#233;gorie Tensorielle_, Moscow Math. Journal 2 (2002) no. 2, 227-248. ([pdf](https://www.math.ias.edu/files/deligne/Tensorielles.pdf))

building on

* [[Pierre Deligne]], _[[Catégories Tannakiennes]]_, Grothendieck Festschrift, vol. II, Birkh&#228;user Progress in Math. 87 (1990) pp.111-195.

A review is in 

* {#Ostrik04} [[Victor Ostrik]], _Tensor categories (after P. Deligne)_ ([arXiv:math/0401347](http://arxiv.org/abs/math/0401347))

Further discussion in view of the theory of [[triangular Hopf algebras]] is in 

* {#EtingofGelaki02} [[Pavel Etingof]], [[Shlomo Gelaki]], _The classification of finite-dimensional triangular Hopf algebras over an algebraically closed field of characteristic 0_ ([arXiv:0202258](http://de.arxiv.org/abs/math/0202258))


Tannaka duality for ordinary compact groups regarded as supergroups (hence equipped with "inner parity", def. \ref{InnerParity}, here just being an involutive central element) is discussed in

* {#Mueger06} [[Michael Müger]], _Abstract Duality Theory for Symmetric Tensor $\ast$-Categories_ appendix ([pdf](http://www.math.ru.nl/~mueger/PDF/16.pdf)), in [[Hans Halvorson]],  _Algebraic quantum field theory_ ([arXiv:math-ph/0602036](http://arxiv.org/abs/math-ph/0602036)), in J. Butterfield & J. Earman (eds.) _Handbook of Philosophy and Physics_ 

as a proof of [[Doplicher-Roberts reconstruction]]

[[!redirects Deligne theorem on tensor categories]]

[[!redirects Deligne reconstruction theorem]]