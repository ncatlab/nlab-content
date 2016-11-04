
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

Deligne's theorem on tensor categories ([Deligne 02](#Deligne02), recalled as theorem \ref{TheTheorem} below) establishes [[Tannaka duality]] between linear [[tensor categories]] in [[characteristic zero]] subject to just a mild size constraint (subexponential growth, def. \ref{SubexponentialGrowth} below), and [[supergroups]] ("[[supersymmetries]]"), realizing these tensor categories as [[categories of representations]] of these supergroups.

## Relevance

### For supersymmetry

Since the concept of linear tensor categories arises very naturally in mathematics, the theorem gives a purely mathematical "reason" for the relevance of superalgebra and supergeometry. It is reasonable to wonder why of all possible generalizations of [[commutative algebra]], it is supercommutative superalgebras that are singled out (from alternatives such as plain $\mathbb{Z}_2$-[[graded algebras]], or in fact $\mathbb{Z}_n$-graded algebras or general [[noncommutative algebras]] or, the like), as they are notably in theoretical [[physics]] ("[[supersymmetry]]"), but also in mathematical fields such as [[spin geometry]] and [[K-theory]]. 

But with $k$-linear [[tensor categories]] appearing on general abstract grounds as the canonical structure to consider in [[representation theory]], Deligne's theorem serves to base supercommutative superalgebra on this same general abstract foundation, showing that this is precisely the context in which full $k$-linear tensor categories exhibit full [[Tannaka duality]].

More concretely, in [[quantum field theory]], under the [[Wigner classification]], [[fundamental particles]] are identified with [[irreducible representations]] of the [[isometry group]] of the local model of [[spacetime]]. Forming the [[tensor product]] of two such representations corresponds to combining them as two [[subsystems]] of a joint system. Therefore it is natural to demand that physical particle species should form complex-linear [[tensor categories]]. Deligne's theorem then gives that [[supersymmetry]] is the most general context in which this works out. (In physics the irreducible representation in this context here are called the _[[supermultiplets]]_.)

### For Tannaka duality of Hopf algebras
 {#RelevanceForHopfAlgebras}

By [[Tannaka duality]] rigid symmetric monoidal categories in general are [[categories of modules]] of [[triangular Hopf algebras]]. Hence Deligne's theorem here implies that those triangular Hopf algebras whose category of representation has subexponential growth (def. \ref{SubexponentialGrowth} below) are equivalent to supercommutative Hopf algebras. See ([Etingof-Gelaki 02](#EtingofGelaki02)) for more.

[[!include structure on algebras and their module categories - table]]




## Statement
 {#Statement}

Throughout, let $k$ be an [[algebraically closed field]] of [[characteristic zero]] (for instance the [[complex numbers]]).


### Tensor categories

There are slight variants of what people mean by a "[[tensor category]]". Here we mean precisely the following: 

+-- {: .num_defn #TensorCategory}
###### Definition

For $k$ an [[algebraically closed field]] of [[characteristic zero]], then a _$k$-[[tensor category]]_ $\mathcal{A}$ is an 

1. [[essentially small category|essentially small]]

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

=--

([Deligne 02, 0.1](#Deligne02))

We consider now various types of size constraints on tensor categories. The main theorem (theorem \ref{TheTheorem} below) only assumes one of them (subexponential growth, def. \ref{SubexponentialGrowth}), but the others appear in the course of the proof of the theorem.

1. finiteness (def. \ref{FiniteTensorCategory})

1. finite $\otimes$-generation (def. \ref{FiniteTensorGeneration})

1. subexponential growth (def. \ref{SubexponentialGrowth})

Recall the concept of [[length of an object]] in an [[abelian category]], a generalization of the concept of [[dimension]] of a [[free module]]/[[vector space]]. 


+-- {: .num_defn #FiniteTensorCategory} 
###### Definition

A $k$[[tensor category]] (def. \ref{TensorCategory}) is called **finite** (over $k$) if 

1. There are only [[finite number|finitely many]] [[simple objects]] in $C$ (hence it is a [[finite abelian category]]), and each of them admits a [[projective presentation]]. 

1. Each object $a$ is of [[object of finite length|finite length]]; 

1. For any two [[objects]] $a$, $b$ of $C$, the [[hom-object]] ($k$-[[vector space]]) $\hom(a, b)$ has [[finite]] [[dimension]]; 

=--

+-- {: .num_example} 
###### Example

The category of [[finite dimensional vector spaces]] over $k$ is a finite tensor category according to def. \ref{FiniteTensorCategory}. It has a single isomorphism class of [[simple objects]], namely $k$ itself.

Also category of finite dimensional [[super vector spaces]] is a finite tensor category. This has two isomorphism classes of simple objects, $k = k^{1 \vert 0}$ regarded in even degree, and $k^{0\vert 1}$ regarded in odd degree.

=--


The following finiteness condition is useful in the proof of the main theorem, but not necessary for its statement (according to [Deligne 02, bottom of p. 3](#Deligne02)):

+-- {: .num_defn #FiniteTensorGeneration}
###### Definition

A $k$-[[tensor category]] (def. \ref{TensorCategory}) is called _finitely $\otimes$-generated_ if there exists an [[object]] $E \in \mathcal{A}$ such that every other object $X \in \mathcal{A}$ is a [[subquotient]] of a [[direct sum]] of [[tensor products]] $E^{\otimes^n}$, for some $n \in \mathbb{N}$:

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


The following is the main size constraint needed in the theorem. Notice that it is a "mild" constraint at least in the intuitive sense that it states just a minimum assumption on the expected behaviour of dimension ([[lengh of an object|lengh]]) under tensor powers.

+-- {: .num_defn #SubexponentialGrowth}
###### Definition

A [[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) is said to have _subexponential growth_ if the [[length]] of tensor exponentials is no larger than the exponential of the length: for every [[object]] $X$ there exists a [[natural number]] $N_X$ such that $X$ is of [[length of an object|length]] at most $N_X$, and that also all [[tensor product]] powers of $X$ are of length bounded by the corresponding powers of $N_X$:

$$
  \underset{X \in \mathcal{A}}{\forall}
  \underset{N_X \in \mathbb{N}}{\exists}
  \underset{n \in \mathbb{N}}{\forall}
    \;\;
   length(X^{\otimes^n}) \leq (N_X)^n
  \,.
$$

=--

(e.g. [EGNO 15, def. 9.11.1](#EGNO15))

The evident example is the following:

+-- {: .num_example}
###### Example

The tensor category $k$[[FinVect]] of [[finite dimensional vector spaces]] has subexponential growth (def. \ref{SubexponentialGrowth}), for $N_X = dim(X)$ the [[dimension]] of a vector space $X$, we have

$$
  dim(X^{\otimes^n}) = (dim(X))^n
  \,.
$$

=--

Of coure the assumption of the existence of [[dual objects]] ([[rigid monoidal category|rigidity]]) in def. \ref{TensorCategory} is already a finiteness condition itself. The following construction lifts that condition:

+-- {: .num_prop #IndObjectsInATensorCategory} 
###### Proposition

Let $\mathcal{A}$ a [[tensor category]] (def. \ref{TensorCategory}), such that 

1. all [[object of finite length|objects have finite length]];

1. all [[hom spaces]] are of [[finite number|finite]] [[dimension]] over $k$

then for its [[category of ind-objects]] $Ind(\mathcal{A})$ the following holds

1. $Ind(\mathcal{A})$ is an [[abelian category]]

1. $\mathcal{A} \hookrightarrow Ind(\mathcal{A})$ is a [[full subcategory]] 

   1. which stable under forming [[subquotients]]

   1. such that that every [[object]] $X \in Ind(\mathcal{A})$ is the [[filtered colimit]] of those of its [[subobjects]] that are in $\mathcal{A}$;

1. $\Ind(\mathcal{A})$ inherits a [[tensor product]] by 

   $$
     \begin{aligned}
       X \otimes Y
         & \simeq 
       (\underset{\longrightarrow}{\lim}_i X_i)
       \otimes
       (\underset{\longrightarrow}{\lim}_i Y_i)
       \\
       & \simeq
       \underset{\longrightarrow}{\lim}_{i,j} (X_i \otimes X_j)
     \end{aligned}
   $$

   where $X_i,X_j \in \mathcal{A}$, by the above.

1. $Ind(\mathcal{A})$ satisfies all the axioms of def. \ref{TensorCategory} except that it fails to be [[essentially small category|essentially small]] and [[rigid category]]. In detail

   1. an object in $Ind(\mathcal{A})$ is [[dualizable object|dualizable]] precisely if it is in $\mathcal{A}$.

=--

### Fiber functors

The first step in exhibiting a given [[tensor category]] $\mathcal{A}$ as being a [[category of representations]] is to exhibit its objects as having an [[forgetful functor|underlying]] representation space, and then an [[action]] represented on that space. Hence a necessary condition on $\mathcal{A}$ is that there exists a [[forgetful functor]]

$$
   \omega \;\colon\; \mathcal{A} \longrightarrow \mathcal{V}
$$

to another [[tensor category]] of sorts, such that $\omega$ satisfies a list of properties, in particular it should be a [[symmetric monoidal functor|symmetric]] [[strong monoidal functor]].

Such functors are called _[[fiber functors]]_. The idea is that we think of $\mathcal{A}$ as a [[bundle]] over $\mathcal{V}$, and over each $V \in \mathcal{V}$ we find the [[fiber]] $\omega^{-1}(V)$ of that "bundle", consisting of all those objects in $\mathcal{A}$ whose underlying object in the given $V$.

The main point of [[Tannaka duality]] of tensor categories is the observation that if $\mathcal{A}$ is a [[category of representations]] of some [[group]] $G$, then $G$ also [[action|acts]] by [[automorphisms]] on that [[fiber functor]] (i.e. via [[natural isomorphisms]] of functors). In good cases then this may be turned around, and the full [[automorphism group]] of a fiber functor identified with the group $G$ for which the objects in its fibers are [[representations]], this is the process of [[Tannaka reconstruction]].

There are slight variants on what one requires of a fiber functor. For the present purpose we fix the following definition

+-- {: .num_defn #FiberFunctor} 
###### Definition

Let $\mathcal{A}$ and $\mathcal{T}$ be two $k$[[tensor categories]] (def. \ref{TensorCategory}) such that 

1. all [[object of finite length|objects have finite length]];

1. all [[hom spaces]] of [[finite number|finite]] [[dimension]] over $k$.

Let $R \in CMon(Ind(\mathcal{T}))$ be a [[commutative monoid in a symmetric monoidal category|in]] in the category of [[ind-objects]] in $\mathcal{T}$ (prop. \ref{IndObjectsInATensorCategory}).  

Then a **[[fiber functor]] on $\mathcal{A}$ over $R$** is a [[functor]]

$$
  \omega \;\colon\; \mathcal{A} \longrightarrow R Mod(Ind(\mathcal{T}))
$$ 

from $\mathcal{A}$ to the category of [[module objects]] over $R$ in the [[category of ind-objects]] $Ind(\mathcal{T})$ (def. \ref{IndObjectsInATensorCategory}), which is

1. a [[braided monoidal functor|braided]] [[strong monoidal functor]];

1. an [[exact functor]] in both variables.

If here $\mathcal{T} = $ [[sVect]], then this is called a **super fiber functor**.

=--

([Deligne 02, 3.1](#Deligne02))

+-- {: .num_prop #MonoidalTransformationBetweenFiberFunctorIsIso} 
###### Proposition

Ever [[monoidal natural transformation]] between two [[fiber functors]] (def. \ref{FiberFunctor}) is an [[isomorphism]] (i.e. a [[natural isomorphism]]).

=--

([Deligne 02, lemma 3.2](#Deligne02))


### Schur functors

A [[finite dimensional vector space]] $V$ has the property that a high enough [[alternating power]] of it vanishes $\wedge^n V = 0$, namely this is the case for all $n \gt dim(V)$, and hence this vanishing is just another reflection of the finiteness of the [[dimension]] of $V$. For a [[super vector space]] $V$ of degreewise finite dimension an analog statement is still true, but one needs to form not just alternating powers but also [[symmetric powers]] (prop. \ref{SchurFunctorAnnihilatingFiniteDimensionalSuperVectorSpace} below), in fact one needs to apply a generalization of both of these constructions, a _[[Schur functor]]_. 


The operation of forming [[symmetric powers]] and [[alternating powers]] makes sense in every [[tensor category]]. Moreover, these operations are the two extreme cases of the more general concept of [[Schur functors]]: Given any [[object]] $X$ and given any choice of [[irreducible representation]] $V_\lambda$ of the [[symmetric group]] $\Sigma_n$, then one consider the [[subobject]] $S_\lambda(X^{\otimes^n})$ of the $n$-fold [[tensor power]] that is [[invariant]] under this action.

The first step in the proof of the main theorem (theorem \ref{TheTheorem} below) is the proposition (prop. \ref{LengthOfObjectIsBounded} below) that all objects that have subexponential growth of length (def. \ref{SubexponentialGrowth}) are actually annihilated by some [[Schur functor]] for the [[symmetric group]]. 


+-- {: .num_defn #SchurFunctor}
###### Definition

For $(\mathcal{A},\otimes)$ a $k$-[[tensor category]] as in def.\ref{TensorCategory}, for $X \in \mathcal{A}$ an [[object]], for $n \in \mathbb{N}$ and $\lambda$ a [[partition]] of $n$, regarded as a [[Young diagram]] and hence as a [[representation]] of the [[symmetric group]] $V_\lambda$, say that the value of the [[Schur functor]] $S_\lambda$ on $X$ is 

$$
  \begin{aligned}
    S_{\lambda}(X) 
      & \coloneqq 
    (V_\lambda \otimes X^{\otimes_n})^{S_n}
    \\
    & = 
    \left(
      \frac{1}{n!}
      \underset{g\in S_n}{\sum}
      \rho(g)
    \right)
    \left(
      V_\lambda \otimes X^{\otimes_n}
    \right)
  \end{aligned}
$$

where

* $(-)^{S_n}$ is the subobject of [[invariants]];

* $S_n$ is the [[symmetric group]] on $n$ elements;

* $V_\lambda$ is the [[irreducible representation]] of $S_n$ corresponding to $\lambda$;

* $\rho$ is [[diagonal action]] of $S_n$ on $V_\lambda \otimes X^{\otimes_n}$, coming from the canonical [[permutation]] action on $X^{\otimes_n}$;

* $(-)^{S_n}$ denotes the subspace of [[invariants]] under the action $\rho$ 

* the second expression just rewrites the invariants as the image of all elements under [[group averaging]].

=--

([Deligne 02, 1.4](#Deligne02))

+-- {: .num_example}
###### Example

For $\lambda = (n)$, then $V_{(n)} = k$ equipped with the trivial action of the symmetric group. In this case the corresponding [[Schur functor]] (def. \ref{SchurFunctor}) forms the $n$th [[symmetric power]]

$$
  S_{(n)}(X) = Sym^n(X)
  \,.
$$

For the dual case where $\lambda = (1,1, \cdots, 1)$ then $V_{(1,1,\cdots, 1)} = k$ equipped with the action by multiplication with the [[signature of a permutation]] and the corresponding [[Schur functor]] forms the [[alternating power]]

$$
  S_{(1,1, \cdots, 1)}(X) = \wedge^n X
  \,.
$$

=--

+-- {: .num_prop #SchurFunctorAnnihilatingFiniteDimensionalSuperVectorSpace} 
###### Proposition

Let $V = V_{even} \oplus V_{odd}$ be a [[super vector space]] of degreewise finite dimension $d_{even}, d_{odd} \in \mathbb{N}$. Then there exists a [[Schur functor]] $S_\lambda$ (def. \ref{SchurFunctor}) that annihilated $V$:

$$
  S_\lambda(V) \simeq 0
  \,.
$$

Speicifically, this is the case precisely if the corresponding [[Young tableau]] $[\lambda]$ satifies

$$
  [\lambda] \subset \left\{ (i,j)\;\vert\; i \leq d_{even}, j \leq d_{odd} \right\}
  \,.
$$

=--

([Deligne 02, corollary 1.9](#Deligne02))

Generally:

+-- {: .num_prop #LengthOfObjectIsBounded}
###### Proposition

For [[tensor category]], then the following are equivalent:

1. it has subexponential growth (def. \ref{SubexponentialGrowth});

1. for every object $X$ there exists $n \in \mathbb{N}$ and a [[partition]] $\lambda$ of $n$ such that the corresponding value of the [[Schur functor]], def. \ref{SchurFunctor}, on $X$ vanishes: $S_\lambda(X) = 0$. 

=--

([Deligne 02, prop. 05](#Deligne02))




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

The super-[[representation category]] $Rep(G,\epsilon)$, def. \ref{Superrepresentation} of an algebraic [[supergroup]] $G$, def. \ref{Supergroup}, with inner parity $\epsilon$ is a $k$-[[tensor category]] (def. \ref{TensorCategory}) of subexponential growth (def. \ref{SubexponentialGrowth}).
 
=--

([Deligne 02, 1.21](#Deligne02))

Any finite dimensional [[faithful representation]] (which always exists, [prop.](faithful+representation#AlgebraicGroupHasFinDimFaithfulRepresentations)) serves as a generator ([prop.](faithful+representation#AnyFinDimRepOfAffineAlgebraicGroupOverFieldIsSubquotientsOfFaithfulRep)).

+-- {: .num_theorem #TheTheorem}
###### Theorem

Every $k$-[[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}), of subexponential growth (def. \ref{SubexponentialGrowth}) is [[equivalence of categories|equivalent]] to a [[category of representations]] $Rep(G,\epsilon)$, according to example \ref{RegularTensorCategoriesOfSuperrepresentations}, for some [[supergroup]] $G$.

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