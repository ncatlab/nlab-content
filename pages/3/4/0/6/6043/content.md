
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### On an abelian group

For $(A,+)$ an [[abelian group]], then a _norm_ on the group is a [[function]]

$$
  {\vert-\vert} \;\colon\; G \longrightarrow \mathbb{R}
$$

to the [[real numbers]], such that 

1. (positivity) $(g \neq 0) \Rightarrow (\vert g\vert \gt 0)$

1. ([[triangle inequality]])  ${\vert g + h\vert}\leq {\vert g\vert} + {\vert h\vert}$ 

1. (linearity) ${\vert k g\vert} = {\vert k\vert} {\vert g\vert}$ for all $k \in \mathbb{Z}$.

Here ${\vert k\vert} \in \mathbb{N}$ denotes the [[absolute value]].

A group with a norm is a _[[normed group]]_, see there for more.

### On a vector space

For $k$ a [[field]] equipped with a [[valuation]] (most usually, a [[local field]] such as $\mathbb{R}$, $\mathbb{C}$, or a [[p-adic field|p-adic]] [[complete field|completion]] of a [[number field]]), a **norm** on a $k$-[[vector space]] $V$ is a [[function]] 

$$
  {\vert-\vert} \colon V \to \mathbb{R}
$$ 

such that for all $\lambda \in k$, $v,w \in V$ we have

1.  ${\vert \lambda v \vert} = {\vert \lambda\vert} {\vert v \vert}$ (where $\vert \lambda \vert$ denotes the [[valuation]])

1.  ${\vert v + w\vert } \leq {\vert v \vert } + {\vert w \vert}$ ("[[triangle inequality]]")

1.  if ${\vert v\vert} = 0$ then $v = 0$.

If the third property is not required, one speaks of a **seminorm**.

If the triangle identity is strengthened to 

* ${\vert v + w\vert } \leq max ({\vert v\vert}, {\vert w\vert})$

one speaks of a **[[non-archimedean]]** seminorm, otherwise of an [[archimedean]] one.

A vector space equipped with a norm is a **normed vector space**. A vector of norm 1 is a [[unit vector]].

Each seminorm determines a [[topology]], which is [[Hausdorff space|Hausdorff]] precisely if it is a norm.

A [[topological vector space]] is called **(semi-)normed** if its [[topology]] can be induced by a (semi-)norm.

Two seminorms ${\vert - \vert}_1$ and ${\vert - \vert}_2$ are called **equivalent** if there are $0 \lt C, C' \in \mathbb{R}$ such that for all $v$ we have

$$
  C {\vert v \vert}_1 \leq {\vert v \vert}_2
  \leq C' {\vert v \vert}_1
  \,.
$$

Equivalent seminorms determine the same [[topology]].

The collection of (bounded) multiplicative seminorms on a ([[Banach space|Banach]]) [[ring]] is called its [[analytic spectrum]] (see there for details).


## Examples

### General

* The standard [[absolute value]] is a norm on the [[real numbers]].

* More generally, on any [[Cartesian space]] $\mathbb{R}^n$ the **Euclidean norm** is given by

   $$
     \vert \vec x\vert
       \;\coloneqq\;
     \sqrt{
     \underoverset{i = 1}{n}{\sum}
       (x_i)^2
     }
     \,.
   $$

1. more generally, for $n \in \mathbb{N}$, and $p \in \mathbb{N}$, $p \geq 1$, then the [[Cartesian space]] $\mathbb{R}^n$ carries the _[[p-norm]]_

   $$ 
     {\vert \vec x \vert}_p  \coloneqq \root p {\sum_i {|x_i|^p}} 
   $$

1. The [[p-norm]] generalizes to [[sequence spaces]] and [[Lebesgue spaces]]. 

* [[operator norm]] in [[operator algebra]]/[[functional analysis]]

### Minkowski Functionals

Let $V$ be a vector space and $B \subseteq V$ an [[absorbing]] [[absolutely convex]] subset.  The **Minkowski functional** of $B$ is the function $\mu_B \colon V \to \mathbb{R}$ defined by:

$$
\mu_B(v) = \inf\{t \gt 0 : v \in t B\}
$$

This is a semi-norm on $V$.


## Properties

* [[Hahn-Banach theorem]]

The (open or closed) [[unit ball]] of a seminormed vector space is a [[convex set]], a [[balanced set]] and an [[absorbing set]]. The first two of these properties make the unit ball (or even any ball of positive radius) an [[absolutely convex set]]. 


### Uniqueness {#dreamUnique}

In [[dream mathematics]], a given real [[vector space]] (with no topological structure) can have at most one complete norm, up to topological equivalence ([[homeomorphism]] of the [[identity function]]).  It can have multiple inequivalent complete seminorms and incomplete norms, but their Hausdorff quotients and completions must be different.  For example, the various [[Lebesgue norms]] on a [[Cartesian space]] $\mathbb{R}^n$ for finite $n$ are complete and equivalent; on $\mathbb{R}^\infty$, they are inequivalent but incomplete.

As dream mathematics includes [[excluded middle]] and [[dependent choice]], the existence of inequivalent complete norms on a given vector space cannot be proved without a stronger form of the [[axiom of choice]], enough to disprove the [[Baire property]] (which is the only classically false axiom needed in the proof of uniqueness).  In _[[HAF]]_, it is argued that this explains why, in [[applied mathematics]], there tends to be only one norm considered on any particular vector space (after Hausdorff completion).

This theorem applies more generally to [[F-norms]] but not to [[G-norms]] (even on a real vector space).


## Related concepts

* [[metric]]

* [[quotient norm]]

* [[F-norm]], [[G-norm]]

* in [[representation theory]]: [[norm map]]

[[!include analytic geometry ingredients -- table]]


## References

* Wikipedia, _[Normed vector space](https://en.wikipedia.org/wiki/Normed_vector_space)_

* {#BoschGuntzerRemmert84} [[Siegfried Bosch]], [[Ulrich Güntzer]], [[Reinhold Remmert]], _[[Non-Archimedean Analysis]] -- A systematic approach to rigid analytic geometry_, 1984 ([pdf](http://math.arizona.edu/~cais/scans/BGR-Non_Archimedean_Analysis.pdf))

* _[[HAF]]_, &#167;27.47.b (for uniqueness in dream mathematics)


[[!redirects norms]]
[[!redirects seminorm]]
[[!redirects seminorms]]
[[!redirects semi-norm]]
[[!redirects semi-norms]]
[[!redirects Minkowski functional]]
[[!redirects Minkowski functionals]]
[[!redirects normed vector space]]
[[!redirects normed vector spaces]]

[[!redirects normed vector space]]
[[!redirects normed vector spaces]]
[[!redirects normable vector space]]
[[!redirects normable vector spaces]]
[[!redirects pseudonormed vector space]]
[[!redirects pseudonormed vector spaces]]
[[!redirects seminormed vector space]]
[[!redirects seminormed vector spaces]]

[[!redirects normed space]]
[[!redirects normed spaces]]
[[!redirects normable space]]
[[!redirects normable spaces]]
[[!redirects pseudonormed space]]
[[!redirects pseudonormed spaces]]
[[!redirects seminormed space]]
[[!redirects seminormed spaces]]

[[!redirects vector measure]]
[[!redirects vector measures]]

