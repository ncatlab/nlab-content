
# Partitions
* table of contents
{: toc}

## Idea

A _partition_ is any of various ways of dividing a mathematical object into nontrivial _parts_ that (in some sense) cover the object while being mutually disjoint.


## Definitions

Each of the following definitions is a special case of a general concept to follow.


### Partitions of sets

Given a [[set]] $S$, a __partition__ of $S$ is a collection $\pi$ of [[inhabited subsets]] of $S$ (called _blocks_) such that

*  For $A, B \in \pi$, if $A \cap B$ is inhabited, then $A = B$;
*  The [[union]] $\bigcup \pi$ is all of $S$ (the [[improper subset]]).

A partition $\pi$ __refines__ a partition $\rho$ (of the same set) if every block of $\pi$ is contained in some block of $\rho$:
$$ \forall A \in \pi,\; \exists B \in \rho,\; A \subseteq B .$$
Refinement is a [[partial order]] on the class of partitions of $S$.

Partitions of $S$ are in [[bijective correspondence]] with [[equivalence relations]] on $S$; a partition is precisely a collection of [[equivalence classes]].  Refinement corresponds to implication between relations.

Partitions of $S$ are also closely related to [[surjections]] out of $S$.
Any partition $\pi$ of $S$ induces a surjection $S \to \pi$ that assigns each element of $S$ to a unique block, and, conversely, any surjection $f : S \to B$ induces a partition of $S$ by taking the blocks to be the [[fiber]]s $\{f^{-1}(x) \mid x \in B\}$.
In general, many different surjections can map to the same partition under this correspondence. However, there is a natural [[preorder]] on surjections defined by taking $f \le g$ just in case there exists a (necessarily unique) $h$ such that $g = h \circ f$.
Then the operations we have just described give an [[equivalence of categories|equivalence]]
$$ Part(S) \rightleftarrows S \downarrow Surj $$
between the partial order of partitions ordered by refinement and the preorder of surjections ordered by factorization.

### Partitions of natural numbers

Given a [[natural number]] $n$, 

1. a __composition__ of $n$ is a [[list]] of [[positive number|positive]] natural numbers whose [[sum]] is $n$, 

1. a __partition__ of $n$ is an unordered list, or [[multiset]], of such numbers.  

That is, different compositions define the same partition if the compositions differ only by order. A partition may also be defined as a [[monotone function|monotone]] composition.

In practice, notably in the [[representation theory of the symmetric group]]/[[representation theory of the general linear group|general linear group]], partitions of natural numbers $n \in \mathbb{N}$ are often given as anti-monotone sequences, denoted as

$$
  \lambda
  \;=\;
  (\lambda_1 \geq \lambda_2 \geq \cdots \geq \lambda_{rows(\lambda)})
  \,,
  \;\;\;\;
  \underoverset
    {rows(\lambda)}
    {i = 1}
    {\sum}  
    \lambda_i
  \;=\;
  n
  \,.
$$

#### Young diagrams

Often, especially in [[representation theory]] ([[representation theory of the symmetric group|of the symmetric group]]/[[representation theory of the general linear group|general linear group]]), partitions of a natural number $n$ appear as *[[Young diagrams]]* with $n$ boxes. While Young diagrams in themselves are just an equivalent way of thinking of or depicting partitions, they are used to indicate ("[[concept with an attitude]]") that decorations of partitions to [[Young tableaux]] play a role in a given discussion.

#### Partition function

The __[[partition function (number theory)|partition function]]__ $p$ gives the number of partitions of $n$ as a [[function]] of $n$; this is [OEIS A000041](https://oeis.org/A000041).  Its (ordinary) [[generating function]] is 

$$ 
  \sum_{n=0}^\infty p(n) x^n = \prod_{k=1}^\infty (1 - x^k)^{-1} 
  \,.
$$

#### Relation to partitions of sets

Every [[natural number]] $n$ corresponds to a [[finite set]] $[n]$, and every partition of $[n]$ (as defined above) gives a partition of $n$, but different partitions of $[n]$ may give the same partition of $n$.  Conversely, a composition of $n$ defines a partition of $[n]$, but not every partition of $[n]$ arises in this way.

More precisely, we have the following, where $\rightarrowtail$ indicates an [[injection]] and $\twoheadrightarrow$ indicates a [[surjection]]:
$$ Comp(n) \rightarrowtail Part([n]) \twoheadrightarrow Part(n) ;$$
the [[composite]] of this is also a surjection, which is [[split surjection|split]] by the definition of a partition as a monotone composition.


One may also speak of __multiplicative__ compositions and partitions of $n$ for positive $n$ (where the above are _additive_), also called (ordered and unordered) __factorizations__; these are (ordered and unordered) lists of natural numbers greater than $1$ whose product is $n$.


### Of intervals

Given [[real numbers]] $a$ and $b$, a __partition__ $\pi$ of the [[interval]] $[a,b]$ is an inhabited finite [[list]] $c_0, \ldots, c_n$ such that:
* $c_0 = a$,
* $c_i \leq c_{i+1}$ for $i \lt n$,
* $c_n = b$.

A partition $\pi$ __refines__ a partition $\rho$ if every element of the list $\rho$ belongs to the list $\pi$.  The __mesh__ (or __norm__) of $\pi$ is
$$ {\|\pi\|} \coloneqq \max_i (c_{i+1} - c_i) .$$
A __tag__ of $\pi$ is a list $t_0, \ldots, t_{n-1}$ such that $c_i \leq t_i \leq c_{i+1}$ for $i \lt n$.  Tagged partitions are used to define the [[Riemann integral]], the [[Darboux integral]], and the [[gauge integral]].


### Of measure spaces

Given a [[measure space]] $S$ (or more generally a [[measurable space]] equipped with a notion of [[null sets]]), a __partition__ of $S$ is a collection $\pi$ of [[positive subset|positive]] (non-null) [[measurable subsets]] of $S$, such that:
*  For $A, B \in \pi$, if $A \cap B$ is positive, then $A$ and $B$ are equal;
*  The [[union]] $\bigcup \pi$ is [[full subset|full]].

(One might merely allow $A$ and $B$ to be equivalent, meaning that their [[symmetric difference]] is null, when $A \cap B$ is positive, but this does not give a good notion of tagged partition; really, we should think of 

so insist that $\pi$ be _saturated_: if $A$ and $B$ are equivalent and $A \in \pi$, then $B \in \pi$.  Alternatively, especially if one views the partition an _[[indexed subset|indexed]]_ collection of subsets, then one would still require $A = B$ when $A \cap B$ is positive.)

Then a partition of a set is simply a partition of the measure space given by [[counting measure]].

Partitions in this sense can be used to define the [[Lebesgue integral]] in analogy to the definition of the Riemann integral using partitions of intervals.


### Of unity on topological spaces

Given a [[topological space]] $S$, a __[[partition of unity]]__ on $S$ is a collection $U$ of [[continuous maps]] from $S$ to the [[unit interval]] such that, for each point $x$ in $S$:
* $f(x) \gt 0$ for only finitely many $f$ in $U$;
* $\sum_f f(x) = 1$ (where this sum is defined by the previous clause).


### General

Let $M$ be an [[abelian monoid]] (written additively) with the property that $a + b = 0$ only if $a, b = 0$.  (In other words, the nonzero elements form an [[ideal]]; there\'s probably a name for this kind of monoid, but I don\'t know it.)  For purposes of [[constructive mathematics]], we should start with an ideal of elements of $M$ declared _nonzero_, then require that $\{0\}$ be its [[complement]].  Then a __finite composition__ of an element $x$ of $M$ is a finite [[list]] of nonzero elements of $M$ whose sum is $x$, and a __finite partition__ of $x$ is the same thing without regard to order (so a [[multiset]] instead of a list, which is why $M$ must be abelian).  If we now equip $M$ with some notion of sum of some infinite [[series]], we can generalise to (not necessarily finite) __partitions__ (and even compositions, for ordered series), which really should be viewed as [[indexed families]] of elements of $M$.

Composititions and partitions of natural numbers are immediate examples of the finite notion, using the monoid $\{0, 1, 2, \ldots\}$ under addition; multiplicative compositions and partitions use instead $\{1, 2, \ldots\}$ under multiplication.

A partition of unity is a partition of the [[constant function]] with value $1$ in the monoid of continuous maps to the nonnegative [[real line]].  Here we define an infinite sum of functions when only finitely many of the functions are nonzero at each point.  (We could in principle define more infinite sums than these, which would give a notion more general than the usual one of partition of unity.)

A partition of a set [or measure space] $S$ is a partition of $S$ itself in the monoid of [measurable] multisubsets of $S$ [modulo equivalence almost everywhere].  This monoid has all infinite sums, so there is no finiteness requirement.  (Every multisubset in a partition is in fact a subset, but working in the monoid of subsets under [[union]], rather than multisubsets under multi-union, would allow the parts to overlap.)

Finally, a partition of an interval is a finite partition in the monoid [[generators and relations|generated by]] the compact intervals subject to the relations
$$ [a,b] + [b,c] = [a,c] .$$

In the last few examples, each part of a partition is an [[inhabited set]].  In such cases, a __tagged partitition__ is a partition in which each part has been equipped with one of its elements.

## The lattice of partitions of a finite set

For any finite set $S$ with $n$ elements, the partially ordered set of partitions of $S$ forms a [[lattice]] (called $\Pi_n$). Viewing partitions as equivalence relations on $S$, this lattice structure may be described as follows [(Birkhoff)](#Birkhoff):

* the [[bottom]] element is the [[diagonal relation]] on $S$
* the [[top]] element is the total relation on $S$
* the [[meet]] of two equivalence relations $\pi$ and $\rho$ on $S$ is the equivalence relation $\pi \wedge \rho$ defined by $x(\pi\wedge \rho)y$ iff $x\pi y$ and $x\rho y$
* the [[join]] of two equivalence relations $\pi$ and $\rho$ is the meet of all equivalence relations $\sigma$ such that $\pi \subseteq \sigma$ and $\rho \subseteq \sigma$ (this is well-defined since $\Pi_n$ is finite)

Dually, viewing partitions as surjections from $S$, the lattice structure may be described as follows:

* the [[bottom]] element is the identity function $S \to S$
* the [[top]] element is the unique function $S \to 1$ to the 1-element set
* the [[join]] of two surjections $\pi : S \to B$ and $\rho : S \to C$ is their [[pushout]]
* the [[meet]] of two surjections $\pi : S \to B$ and $\rho : S \to C$ is the join of all surjections $\sigma : S \to A$ for which there exist functions $f : A \to B$ and $g : A \to C$ such that $\pi = f \circ \sigma$ and $\rho = g \circ \sigma$

## References

* {#Birkhoff} [[Garrett Birkhoff]], _Lattice Theory_, AMS, third edition, 1973.

* [[Marcelo Aguiar]] and [[Swapneel Mahajan]]. [[Monoidal Functors, Species and Hopf Algebras]], 2010.

[[!redirects partition]]
[[!redirects partitions]]

[[!redirects tagged partition]]
[[!redirects tagged partitions]]
