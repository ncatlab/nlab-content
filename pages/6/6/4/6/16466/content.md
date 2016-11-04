
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

Throughout, let $k$ be an [[algebraically closed field]] of [[characteristic zero]] (for instance the [[complex numbers]]).

### Tensor categories

There are slight variants of what people mean by a "[[tensor category]]". Here we mean precisely the following: 

+-- {: .num_defn #TensorCategory}
###### Definition

For $k$ an [[algebraically closed field]] of [[characteristic zero]], then a _$k$-[[tensor category]]_ $\mathcal{A}$ is an 

1. [[abelian category|abelian]] 

1. [[rigid monoidal category|rigid]] 

1. [[symmetric monoidal category|symmetric]] 

1. [[braided monoidal category|braided]]

1. [[monoidal category]] 

1. [[enriched category|enriched]] over $k$[[Mod]] = $k$[[Vect]] (i.e. $k$-linear), compatible with the [[Ab-enriched category|Ab-enrichment]] implied from [[abelian category|abelianness]] under $U \colon k Vect \to Ab$

such that 

1. the [[tensor product]] functor $\otimes \colon \mathcal{A} \times \mathcal{A} \longrightarrow \mathcal{A}$ is in both arguments separately

   1. $k Mod$-[[enriched functor|enriched]] (i.e. $k$-linear);

   1. [[exact functor|exact]]


1. $End(1) \simeq k$ (the [[endomorphism ring]] of the [[tensor unit]] coincides with $k$).

Such a $k$-tensor category is called _finitely $\otimes$-generated_ if there exists an [[object]] $E \in \mathcal{A}$ such that every other object $X \in \mathcal{A}$ is a [[subquotient]] of a [[direct sum]] of [[tensor products]] $E^{\otimes^n}$, for some $n \in \mathbb{N}$:

$$
  \array{
    && \underset{i}{\oplus} E^{\otimes^{n_i}}
    \\
    && \downarrow
    \\
    X &\hookrightarrow& (\underset{i}{\oplus} E^{\otimes^{n_i}})/Q
  }
  \,.
$$

Such $E$ is called an _$\otimes$-generator_ for $\mathcal{A}$.

=--

([Deligne 02, 0.1](#Deligne02))

The following is a mild size constraint on tensor categories:

Recall the concept of [[length of an object]] in an [[abelian category]], a generalization of the concept of [[dimension]] of a [[free module]]/[[vector space]]. 

+-- {: .num_defn #SubexponentialGrowth}
###### Definition

A [[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) is said to have _subexponential growth_ if the [[length]] of tensor exponentials is no larger than the exponential of the lenght: for every [[object]] $X$ there exists a [[natural number]] $N_X$ such that $X$ is of [[length of an object|length]] at most $N_X$, and that also all [[tensor product]] powers of $X$ are of length bounded by the corresponding powers of $N_X$:

$$
  \underset{X \in \mathcal{A}}{\forall}
  \underset{N_X \in \mathbb{N}}{\exists}
  \underset{n \in \mathbb{N}}{\forall}
    \;
   length(X^{\otimes^n}) \leq (N_X)^n
  \,.
$$

=--

(e.g. [EGNO 15, def. 9.11.1](#EGNO15))

+-- {: .num_example}
###### Example

The tensor category $k$[[FinVect]] of [[finite dimensional vector spaces]] has subexponential growth (def. \ref{SubexponentialGrowth}), for $N_X = dim(X)$ the [[dimension]] of a vector space $X$, we have

$$
  dim(X^{\otimes^n}) = (dim(X))^n
  \,.
$$

=--


+-- {: .num_defn #Regularity}
###### Definition

A $k$-[[tensor category]] $(\mathcal{A}, \otimes)$  as in def.\ref{TensorCategory} is _regular_ if 

1. it is finitely $\otimes$-generated (in the sense of def. \ref{TensorCategory});

1. it is of subexponential growth (def. \ref{SubexponentialGrowth}).

=--

### Schur functors

The first step in the proof of the theorem is the proposition (prop. \ref{LenghtOfObjectIsBounded} below) that all objects that have bounded length according to def. \ref{Regularity} are actually annihilated by some [[Schur functor]] for the [[symmetric group]]. This is a (considerable) generalization of the familiar fact that for every [[finite dimensional vector space]] $V$ there exists an [[symmetric algebra|exterior power]] that vanishes, $\wedge^n V = 0$ (namely for all $n \gt dim (V)$). Similarly, if $V$ is a [[super vector space]] of dimension $(d,p)$, then the combined $(d+1)$st skew-symmetric tensor power and $(p+1)$st symmetric tensor power annihilates it. In this way prop. \ref{LenghtOfObjectIsBounded} below already goes a good way in the direction of establishing that all objects of bounded length, in the sense of def. \ref{LenghtOfObjectIsBounded}, behave like having underlying super-vector spaces.


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

* $\rho$ is [[diagonal action]] of $S_n$ on $V_\lambda \otimes X^{\otimes_n}$, coming from the canonical [[permutation]] action on $X^{\otimes_n}$;

* $(-)^{S_n}$ denotes the subspace of [[invariants]] under the action $\rho$ 

* the last expression just rewrites this as a [[group averaging]].

=--

([Deligne 02, 1.4](#Deligne02))

+-- {: .num_prop #LenghtOfObjectIsBounded}
###### Proposition

For [[tensor category]], then the following are equivalent:

1. it has subexponential growth (def. \ref{SubexponentialGrowth});

1. for every object $X$ there exists $n \in \mathbb{N}$ and a [[partition]] $\lambda$ of $n$ such that the corresponding value of the [[Schur functor]], def. \ref{SchurFunctor}, on $X$ vanishes: $S_\lambda(X) = 0$. 


=--

([Deligne 02, prop. 05](#Deligne02))

+-- {: .num_example}
###### Example

For $V \in SuperVect_k$ a [[super vector space]] of super-dimension $(p\vert q)$, then it is annihilated by the Schur functor corresponding to forming the $p$th antisymmetric and the $q$th symmetric tensor power.

=--



### Supergroups

+-- {: .num_defn #Supergroup}
###### Definition

An affine algebraic _[[supergroup]]_ $G$ is the [[formal dual]] of a [[super-commutative Hopf algebra]] $\mathcal{O}(G)$.

=--

We will just say "supergroup" for short in all of the following. We assume throughout that $\mathcal{O}(G)$ is a finitely generated $k$-algebra.

+-- {: .num_defn #ParityAutomorphism}
###### Definition

Given a [[superalgebra]] such as $\mathcal{O}(G)$, its _parity involution_ is the algebra [[automorphism]] which on homogeneously graded elements $a$ of degree $deg(a) \in \{even,odd\} = \mathbb{Z}/2\mathbb{Z}$ is multiplication by the degree

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

A _super-[[representation]]_ of a [[supergroup]] $G$, def. \ref{Supergroup}, with inner parity $\epsilon$, def. \ref{InnerParity}, is a [[linear representation]] of $G$ on a [[finite number|finite]] [[dimension|dimensional]] [[vector space]] $V$ over $k$ such that when $V$ is equipped with the grading by $\pm1$-[[eigenspaces]] of $\epsilon$, even/odd elements of $G$ act with even/odd parity on $V$.

=--

+-- {: .num_defn #Superrepresentation_Deligne_def}
###### Remark

In ([Deligne 02, p. 3, above 0.4)](#Deligne02)) a super-representation of a supergroup $G$ is defined in a different but equivalent way. The vector space $V$ is considered to come equipped a priori with a grading, making it a [[super vector space]], and the following conditions are required to hold:

1. even/odd elements of $G$ act with even/odd parity on $V$

1. in addition such that $\epsilon$ is taken to the parity endomorphism of $V$ (which is the identity on even graded vectors and multiplication with $(-1)$ on odd-graded vectors).
=--

The given definition \ref{Superrepresentation} is preferable to this one as it doesn't ask for extra [[structure]] on $V$ and then for a property relative to that structure. Also in the following example, one _naturally_ finds that the super vector space on which the ordinary group is represented contains no odd part, and is hence merely an ordinary vector space.

+-- {: .num_example}
###### Example

For $G$ an ordinary (affine algebraic) group regarded as a supergroup with trivial odd-graded part, and for $\epsilon = 1$ its neutral element taken as the inner parity, then $Rep(G,\epsilon)$ in the sense of def. \ref{Superrepresentation} is just the ordinary [[category of representations]] of $G$.

=--

([Deligne 02, 0.4 i)](#Deligne02))

+-- {: .num_prop #RegularTensorCategoriesOfSuperrepresentations}
###### Proposition

The super-[[representation category]] $Rep(G,\epsilon)$, def. \ref{Superrepresentation} of an algebraic [[supergroup]] $G$, def. \ref{Supergroup}, with inner parity $\epsilon$ is a regular $k$-[[tensor category]] according to def.\ref{Regularity}.

=--

([Deligne 02, 1.21](#Deligne02))

Any finite dimensional [[faithful representation]] (which always exists, [prop.](faithful+representation#AlgebraicGroupHasFinDimFaithfulRepresentations)) serves as a generator ([prop.](faithful+representation#AnyFinDimRepOfAffineAlgebraicGroupOverFieldIsSubquotientsOfFaithfulRep)).

+-- {: .num_theorem #TheTheorem}
###### Theorem

Every regular $k$-tensor category $\mathcal{A}$, def. \ref{Regularity} is [[equivalence of categories|equivalent]] to one of the form $Rep(G,\epsilon)$, example \ref{RegularTensorCategoriesOfSuperrepresentations}, for some [[supergroup]] $G$.

=--

([Deligne 02, theorem 0.6](#Deligne02))


## References

The theorem is due to

* {#Deligne02} [[Pierre Deligne]], _Cat&#233;gorie Tensorielle_, Moscow Math. Journal 2 (2002) no. 2, 227-248. ([pdf](https://www.math.ias.edu/files/deligne/Tensorielles.pdf))

building on the more general work on [[Tannakian categories]]

* [[Pierre Deligne]], _[[Catégories Tannakiennes]]_, Grothendieck Festschrift, vol. II, Birkh&#228;user Progress in Math. 87 (1990) pp.111-195.

Review is in 

* {#Ostrik04} [[Victor Ostrik]], _Tensor categories (after P. Deligne)_ ([arXiv:math/0401347](http://arxiv.org/abs/math/0401347))

* {#EGNO15} [[Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[Victor Ostrik]], section 9.11 in _Tensor categories_, Mathematical Surveys and Monographs, Volume 205, American Mathematical Society, 2015 ([pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf
))

Further discussion in view of the theory of [[triangular Hopf algebras]] is in 

* {#EtingofGelaki02} [[Pavel Etingof]], [[Shlomo Gelaki]], _The classification of finite-dimensional triangular Hopf algebras over an algebraically closed field of characteristic 0_ ([arXiv:0202258](http://de.arxiv.org/abs/math/0202258))


Tannaka duality for ordinary compact groups regarded as supergroups (hence equipped with "inner parity", def. \ref{InnerParity}, here just being an involutive central element) is discussed in

* {#Mueger06} [[Michael Müger]], _Abstract Duality Theory for Symmetric Tensor $*$-Categories_ appendix ([pdf](http://www.math.ru.nl/~mueger/PDF/16.pdf)), in [[Hans Halvorson]],  _Algebraic quantum field theory_ ([arXiv:math-ph/0602036](http://arxiv.org/abs/math-ph/0602036)), in J. Butterfield & J. Earman (eds.) _Handbook of Philosophy and Physics_ 

as a proof of [[Doplicher-Roberts reconstruction]]

[[!redirects Deligne theorem on tensor categories]]

[[!redirects Deligne reconstruction theorem]]