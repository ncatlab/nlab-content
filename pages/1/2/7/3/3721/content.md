
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An **open subspace** $U$ of a [[space]] $X$ is a [[subspace]] of $X$ whose elements are "stable to small perturbations", or can be "observed to belong to $U$ by measurements with finite precision".

When ordered by inclusion the open subspaces form a poset, the [[frame of opens]].

## Definition

Depending on what sort of "space" $X$ is, this may be defined in different ways.

### For topological spaces

If $X$ is a [[topological space]] in the classical sense, then it is *defined* by specifying a collection of subsets to be called "open" (that are closed under finite intersections and arbitrary joins, i.e. are a sub-[[frame]] of the [[power set]] of $X$).

### For convergence spaces

If $X$ is a [[convergence space]] (or some variation such as a [[subsequential space]]), we define a subset $U\subseteq X$ to be **open** if any filter/net/sequence converging to a point of $U$ must be eventually in $U$.  This defines an "underlying topological space" of $X$.

### For locales

In [[locale]] theory, every open $U$ in the locale defines an "open [[sublocale]]" which is given by the __open [[nucleus]]__
$$ j_{U}\colon V \mapsto U \Rightarrow V .$$
The idea is that this subspace is the part of $X$ which involves only $U$, and we may identify $V$ with $U \Rightarrow V$ when we are looking only at $U$.  If $X$ is a ([[sober space|sober]]) topological space regarded as a locale, then any such open sublocale is spatial and coincides with the subspace determined by the subset $U$ (and this is true even in [[constructive mathematics]]).

### For toposes

See [[open subtopos]].

### In synthetic topology {#SynTop}

In [[synthetic topology]], we interpret 'space' as meaning simply 'set' (or [[type]], i.e. the basic objects of our foundational system).  There are then multiple ways to define "open subset".

One is to use a [[dominance]], which specifies the open subsets representably by a set of "open truth values".

Another possibility is the following definition due to Penon: $U\subseteq X$ is open if for any $x\in U$ and $y\in X$, either $x\neq y$ or $y\in U$.  This definition does not require a choice of dominance, but it is generally only correct for [[Hausdorff spaces]]; for instance, the open point in the [[Sierpinski space]] is not open in this sense.  However, in various [[gros toposes]] of topological, smooth, or algebraic spaces it does induce the correct notion of open subsets for Hausdorff spaces; see [Dubuc-Penon](#DubucPenon).  For more information, see the article [[Penon open]].

## Properties

A [[subspace]] $A$ of a [[space]] $X$ is __open__ if the [[inclusion function|inclusion map]] $A \hookrightarrow X$ is an [[open map]].

The __[[topological interior|interior]]__ of any subspace $A$ is the largest open subspace contained in $A$, that is the [[union]] of all open subspaces of $A$.  The interior of $A$ is variously denoted $Int(A)$, $Int_X(A)$, $A^\circ$, $\overset{\circ}A$, etc.

## Related concepts

* [[closed subset]], [[clopen subset]]

* [[open point]]

* [[open cover]]

* [[open map]]

* [[overt space]]

* [[saturated subset]]

* [[Penon open]]

## References

* [[Jacques Penon]], *Topologie et intuitionnisme*

* [[Eduardo Dubuc]] and [[Jacques Penon]], *Objets compactes dans les topos*
 {#DubucPenon}

[[!redirects open subspace]]
[[!redirects open subspaces]]
[[!redirects open subset]]
[[!redirects open subsets]]
[[!redirects open set]]
[[!redirects open sets]]

[[!redirects open sublocale]]
[[!redirects open sublocales]]
[[!redirects open nucleus]]
[[!redirects open nuclei]]

[[!redirects open]]
[[!redirects opens]]
[[!redirects open subobject]]
[[!redirects open subobjects]]
