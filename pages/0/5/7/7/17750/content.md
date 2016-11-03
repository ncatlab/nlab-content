
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of _length_ of an [[object]] in an [[abelian category]] $\mathcal{C}$ is akin to the concept of [[dimension]] of [[vector spaces]], to which it reduces in the case that $\mathcal{C} = $ [[Vect]]. The 1-dimensional vector space is a [[simple object]] in [[Vect]], and the [[dimension]] of a vector space $V$, if it is finite, may be thought of as the number of times that one may split off such a simple object from $V$. The definition of _length_ generalizes this concept, notably to [[modules]] over some [[ring]].

## Definition

Let $\mathcal{C}$ be an [[abelian category]].

+-- {: .num_defn #FiniteLength}
###### Definition

Given an [[object]] $X \in \mathcal{C}$, then a _Jordan-H&#246;lder sequence_ or _[[composition series]]_ for $X$ is a finite [[filtration]], i.e. a finite sequence of [[subobject]] unclusions into $X$, starting with the [[zero objects]]

$$
  0 = X_0 \hookrightarrow X_1 \hookrightarrow \cdots \hookrightarrow X_{n-1} \hookrightarrow X_n = X
$$

such that at each stage $i$ the [[quotient]] $X_i/X_{i-1}$ (i.e. the [[coimage]] of the [[monomorphism]] $X_{i-1} \hookrightarrow X_i$) is a [[simple object]] of $\mathcal{C}$.

If a Jordan-H&#246;lder sequence for $X$ exists at all, then $X$ is said to be of _finite length_. 

=--

(e.g. [EGNO 15, def. 1.5.3](#EGNO15))

+-- {: .num_prop #JordanHolderSequenceHasDefiniteLength}
###### Proposition
**([[Jordan-Hölder theorem]])**

If $X \in \mathcal{C}$ has finite length according to def. \ref{FiniteLength}, then in fact all Jordan-H&#246;lder sequences for $X$ have the same length $n \in \mathbb{N}$.

=--

(e.g. [EGNO 15, theorem 1.5.4](#EGNO15))

+-- {: .num_defn #LengthOfAnObject}
###### Definition

If an object $X \in \mathcal{C}$ has finite length according to def. \ref{FiniteLength}, then the length $n \in \mathbb{N}$ of any of its Jordan-H&#246;lder sequences, which is uniquely defined according to prop. \ref{JordanHolderSequenceHasDefiniteLength}, is called the _length of the object_ $X$.

=--

(e.g. [EGNO 15, def. 1.5.5](#EGNO15))

## Properties

### Relation to Schur functors
 {#RelationToSchurFunctors}

In [[abelian categories]] that are also $k$-linear [[tensor categories]] over a [[field]] $k$ of [[characteristic zero]], then objects have finite length precisely if they are annihilated by some [[Schur functor]] for the [[symmetric group]].

This is a (considerable) generalization of the familiar fact that for every [[finite dimensional vector space]] $V$ there exists an [[symmetric algebra|exterior power]] that vanishes, $\wedge^n V = 0$ (namely for all $n \gt dim(V)$). Similarly, if $V$ is a [[super vector space]] of dimension $(d,p)$, then the combined $(d+1)$st skew-symmetric tensor power and $(p+1)$st symmetric tensor power annihilates it. In this way prop. \ref{LenghtOfObjectIsBounded} below goes in the direction of establishing that in a $k$-linear tensor category all objects of bounded length , in the sense of def. \ref{LenghtOfObjectIsBounded}, behave like having underlying [[super vector spaces]]. The completion of this statement is [[Deligne's theorem on tensor categories]], see there for more.

First we need to fix the precise meaning of "[[tensor category]]":

+-- {: .num_defn #TensorCategory}
###### Definition

For $k$ an [[algebraically closed field]] of [[characteristic zero]], then a _$k$-[[tensor category]]_ $\mathcal{A}$ is an 

1. [[abelian category|abelian]] 

1. [[rigid monoidal category|rigid]] 

1. [[symmetric monoidal category|symmetric]] 

1. [[braided monoidal category|braided]]

1. [[monoidal category]] 

1. [[enriched category|enriched]] over $k$[[Mod]] = $k$[[Vect]] (i.e. $k$-linear), 

such that 

1. the [[tensor product]] functor $\otimes \colon \mathcal{A} \times \mathcal{A} \longrightarrow \mathcal{A}$ is 

   1. $k Mod$-[[enriched functor|enriched]] (i.e. $k$-linear);

   1. [[exact functor|exact]]

   in both arguments;

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

+-- {: .num_defn #SubexponentialGrowth}
###### Definition

A [[tensor category]] $\mathcal{A}$ (def. \ref{TensorCategory}) is said to have _subexponential growth_ if for every [[object]] $X$ there exists a [[natural number]] $N$ such that $X$ is of length (def. \ref{LengthOfAnObject}) at most $N$, and that also all [[tensor product]] powers of $X$ are of length bounded by the corresponding powers of $N$:

$$
  \underset{X \in \mathcal{A}}{\forall}
  \underset{N \in \mathbb{N}}{\exists}
  \underset{n \in \mathbb{N}}{\forall}
    \;
   length(N^{\otimes^n}) \leq N^n
  \,.
$$

=--

(e.g. [EGNO 15, def. 9.11.1](#EGNO15))


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

+-- {: .num_prop #LenghtOfObjectIsBounded}
###### Proposition

For a [[tensor category]] $\mathcal{A}$ the following are equivalent:

1. the category has subexponential growth (def. \ref{SubexponentialGrowth}).

1. For every object $X \in \mathcal{A}$ there exists $n \in \mathbb{N}$ and a [[partition]] $\lambda$ of $n$ such that the corresponding value of the [[Schur functor]], def. \ref{SchurFunctor}, on $X$ vanishes: $S_\lambda(X) = 0$. 


=--

([Deligne 02, prop. 05](#Deligne02))


## References

* {#EGNO15} [[Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[Victor Ostrik]], section 1.5 in _Tensor categories_, Mathematical Surveys and Monographs, Volume 205, American Mathematical Society, 2015 ([pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf
))

* Wikipedia, _[Composition series](https://en.wikipedia.org/wiki/Composition_series)_

The relation to [[Schur functors]] is discussed in

* {#Deligne02} [[Pierre Deligne]], _Cat&#233;gorie Tensorielle_, Moscow Math. Journal 2 (2002) no. 2, 227-248. ([pdf](https://www.math.ias.edu/files/deligne/Tensorielles.pdf))

For more on this see at _[[Deligne's theorem on tensor categories]]_.

[[!redirects lengths of objects]]

[[!redirects Jordan-Hölder series]]
[[!redirects Jordan-Holder series]]

[[!redirects Jordan-Hölder sequence]]
[[!redirects Jordan-Holder sequence]]


[[!redirects object of finite length]]
[[!redirects objects of finite length]]

