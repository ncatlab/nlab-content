
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[continuous map]] $f : X \to Y$ between [[topological spaces]] is called a _local homeomorphism_ if restricted to a [[neighbourhood]] of every point in its [[domain]] it becomes a [[homeomorphism]] onto its image which is required
to be open.

One also says that this exhibits $X$ as an [[étale space]] over $Y$.

Notice that, despite the similarity of terms, local homeomorphisms are, in general, _not_ [[local isomorphisms]] in any natural way. See the [examples](#Examples) below.

## Definition

\begin{definition}
A *local homeomorphism*  is a [[continuous map]] $p \colon E \to B$ between [[topological spaces]] (a [[morphism]] in [[Top]]) such that

* for every [[element]] $e \in E$, there is an [[open subset]] $U \ni e$ whose [[image]] $p_*(U)$ is open in $B$ and the restriction of $p$ to $U$ is a [[homeomorphism]] $p|_U \colon U \to p_*(U)$,

or equivalently

* for every $e \in E$, there is a [[neighbourhood]] $U$ of $e$ such that the image $p_*(U)$ is a neighbourhood of $p(e)$ and $p|_U: U \to p_*(U)$ is a homeomorphism.

\end{definition}

See also at *[[étale space]]*.

## Examples
 {#Examples}

For $X$ any [[topological space]] and  for $S$ any [[set]] regarded as a [[discrete space]], the [[projection]]

$$
  X \times S \to X
$$

is a local homeomorphism.

For $\{U_i \to Y\}$ an [[open cover]], let 

$$
  X := \coprod_i U_i
$$

be the [[disjoint union]] space of all the pathches. Equipped with the canonical projection

$$
  \coprod_i U_i \to Y
$$

this is a local homeomorphism.

In general, for every [[sheaf]] $A$ of sets on $Y$; there is a local homeomorphism $X \to Y$ such that over any open $U \hookrightarrow X$ the set $A(U)$ is naturally identified with the set of [[sections]] of $Y \to X$. See [[étale space]] for more on this.

## Properties
 {#Properties}

\begin{proposition}\label{LocalHomeosAreOpenMaps}
  A [[local homeomorphism]] is an [[open map]].
\end{proposition}
\begin{proof}
  Let $f \colon X \to Y$ be a [[local homeomorphism]] and $U \subset X$ an [[open subset]]. We need to see that the [[image]] $f(U) \subset Y$ is an open subset of $Y$. 
For this we may equivalently show that each $y \in f(U)$ has an [[open neighbourhood]] inside $f(U)$.

But since any function is [[surjection|surjective]] onto its [[image]], there exists $x \in U$ with $f(x) = y$.
By local homeomorphy of $f$, this $x \in X$ has an  [[open neighbourhood]] $U_x \subset X$ with $f_{|U_x} \colon U_x \to f(U_x)$ a [[homeomorphism]]. Since $U \cap U_x \subset U_x$ is an [[open neighbourhood]] of $x$ in $U_x$, the homeomorphy of $f_{|U_x}$ implies that $f(U \cap U_x) \subset f(U)$ is an open neighbourhood of $f(x) = y$.
\end{proof}


## Related concepts

* [[étale map]], [[étale morphism]]

* [[locally homeomorphic geometric morphism]]


[[!redirects local homeomorphisms]]