
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

## Definition

A [[subspace]] $A$ of a [[space]] $X$ is __open__ if the [[inclusion function|inclusion map]] $A \hookrightarrow X$ is an [[open map]].

For a point-based notion of space such as a [[topological space]], an open subspace is the same thing as an __open subset__.

In [[locale]] theory, every open $U$ in the locale defines an open subspace which is given by the __open [[nucleus]]__
$$ j_{U}\colon V \mapsto U \Rightarrow V .$$
The idea is that this subspace is the part of $X$ which involves only $U$, and we may identify $V$ with $U \Rightarrow V$ when we are looking only at $U$.

The __[[topological interior|interior]]__ of any subspace $A$ is the largest open subspace contained in $A$, that is the [[union]] of all open subspaces of $A$.  The interior of $A$ is variously denoted $Int(A)$, $Int_X(A)$, $A^\circ$, $\overset{\circ}A$, etc.

(There is a lot more to say, about [[convergence spaces]], [[smooth spaces]], [[schemes]], etc.)

## In synthetic topology {#SynTop}

In [[synthetic topology]], we interpret 'space' as meaning simply 'set' (or [[type]], i.e. the basic objects of our foundational system).  There are then multiple ways to define "open subset".

One is to use a [[dominance]], which specifies the open subsets representably by a set of "open truth values".

Another possibility is the following definition due to Penon: $U\subseteq X$ is open if for any $x\in U$ and $y\in X$, either $x\neq y$ or $y\in U$.  This definition does not require a choice of dominance, but it is generally only correct for [[Hausdorff spaces]]; for instance, the open point in the [[Sierpinski space]] is not open in this sense.  However, in various [[gros toposes]] of topological, smooth, or algebraic spaces it does induce the correct notion of open subsets for Hausdorff spaces; see [Dubuc-Penon](#DubucPenon).

## Related concepts

* [[closed subset]], [[clopen subset]]

* [[open cover]]

* [[open map]]

* [[overt space]]

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
