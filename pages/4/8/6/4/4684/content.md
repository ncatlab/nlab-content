
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Manifolds and cobordisms
+-- {: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _topological manifold_ is a [[topological space]] (usually required to be [[Hausdorff topological space|Hausdorff]] and [[paracompact topological space|paracompact]]) which is _locally_ [[homeomorphism|homeomorphic]] to a [[Euclidean space]] $\mathbb{R}^n$ equipped with its [[metric topology]].

Often one is interested in extra structure on topological manifolds, that make them for instance into [[differentiable manifolds]] or [[smooth manifolds]] or [[analytic manifolds]] or [[complex manifolds]], etc. See at _[[manifold]]_ for more on the general concept.

Topological manifolds form a category [[TopMfd]].

## Definition

### Locally Euclidean topological spaces
 {#LocallyEuclideanTopologicalSpace}


+-- {: .num_defn #LocallyEuclideanSpace}
###### Definition
**([[locally Euclidean topological space]])**

A [[topological space]] $X$ is _[[locally Euclidean topological space|locally Euclidean]]_ if every point $x \in X$ has an [[open neighbourhood]] $U_x \supset \{x\}$ which is [[homeomorphism|homeomorphic]] to the [[Euclidean space]] $\mathbb{R}^n$ with its [[metric topology]]:

$$
  \mathbb{R}^n
    \overset{\phantom{AA} \simeq \phantom{AA}}{\longrightarrow}
  U_x
    \subset
  X
  \,.
$$


=--

The "local" [[topological properties]] of Euclidean space are inherited by locally Euclidean spaces:

+-- {: .num_prop #LocalPropertiesOfLocallyEuclideanSpace}
###### Proposition
**([[locally Euclidean spaces]] are $T_1$-[[separation axiom|separated]], [[sober topological space|sober]], [[locally connected topological space|locally connected]], [[locally compact topological space|locally compact]])**

Let $X$ be a [[locally Euclidean space]] (def. \ref{LocallyEuclideanSpace}). Then

1. $X$ satisfies the $T_1$ [[separation axiom]];

1. $X$ is [[sober topological space|sober]];

1. $X$ is [[locally connected topological space|locally connected]];

1. $X$ is [[locally compact topological space|locally compact]] in the sense that every open neighbourhood of a point contains a [[compact topological space|compact]] neighbourhood.

=--

+-- {: .proof}
###### Proof

Regarding the first statement:

Let $x \neq y$ be two distinct points in the locally Euclidean space. We need to show that there is an open neighbourhood $U_x$ around $x$ that does not contain $y$.

By definition, there is a Euclidean open neighbourhood $\mathbb{R}^n \underoverset{\simeq}{\phi}{\to} U_x \subset X$ around $x$. If $U_x$ does not contain $y$, then it already is an open neighbourhood as required. If $U_x$ does contain $y$, then $\phi^{-1}(x) \neq \phi^{-1}(y)$ are equivalently two distinct points in $\mathbb{R}^n$. But Euclidean space, as every [[metric space]], is $T_1$, and hence we may find an open neighbourhood $V_{\phi^{-1}(x)} \subset \mathbb{R}^n $ not containing $\phi^{-1}(y)$. By the nature of the [[subspace topology]], $\phi(V_{\phi^{-1}(x)}) \subset X$ is an open neighbourhood as required.

Regarding the second statement:

We need to show that the map

$$
  Cl(\{-\}) \;\colon\; X \to IrrClSub(X)
$$

that sends points to the [[topological closure]] of their singleton sets is a [[bijection]] with the set of [[irreducible closed subsets]]. By the first statement above the map is [[injective function|injective]] (via [this lemma](separation+axioms#T1InTermsOfClosureOfPoints)).

Hence it remains to see that every irreducible closed subset is the topological closure of a singleton. We will show something stronger: every irreducible closed subset is a singleton.

Let $P \subset X$ be an open proper subset such that if there are two open subsets $U_1, U_2 \subset X$ with $U_1 \cap U_2 \subset P$ then $U_1 \subset P$ or $U_2 \subset P$. By [this prop.](irreducible+closed+subspace#OpenSubsetVersionOfClosedIrreducible) we need to show that there exists a point $x \in X$ such that $P = X \setminus \{x\}$ it its [[complement]].

Now since $P \subset X$ is a proper subset, and since the locally Euclidean space $X$ is covered by Euclidean neighbourhoods, there exists a Euclidean neighbourhood $\mathbb{R}^n \underoverset{\simeq}{\phi}{\to} U \subset X$ such that $P \cap U \subset U$ is a proper subset. In fact this still satisfies the condition that for $U_1, U_2 \underset{\text{open}}{\subset} U$ then $U_1 \cap U_2 \subset P \cap U$ implies $U_1 \subset P \cap U$ or $U_2 \subset P \cap U$. Accordingly, by [that prop.](irreducible+closed+subspace#OpenSubsetVersionOfClosedIrreducible) it follows that $\mathbb{R}^n \setminus \phi^{-1}(P \cap U)$ is an irreducible closed subset of [[Euclidean space]]. Sine [[metric spaces]] are [[sober topological space]] as well as $T_1$-[[separation axiom|separated]], this means that there exists $x \in \mathbb{R}^n$ such that $\phi^{-1}(P \cap U) = \mathbb{R}^n \setminus \{x\}$.

In conclusion this means that the restriction of an irreducible closed subset in $X$ to any Euclidean chart is either empty or a singleton set. This means that the irreducible closed subset must be a disjoint union of singletons that are separated by Euclidean neighbourhoods. But by irreducibiliy, this union has to consist of just one point.

Regarding the third statement:

Let $x \in X$ be a point and $U_x \supset \{x\}$ a neighbourhood. We need to find a [[connected topological space|connected]] open neighbourhood $Cn_x \subset U_x$.

By local Euclideanness, there is also a Euclidean neighboruhood $\mathbb{R}^n \underoverset{\simeq}{\phi}{\to} V_x \subset X$. Since $\phi$ is a [[homeomorphism]], and since $U_x \cap V_x$ is open, also $\phi^{-1}(U_x \cap V_x) \subset \mathbb{R}^n$ is open. This means that there exists an [[open ball]] $B_{\phi^{-1}(x)}^\circ(\epsilon) \subset \phi^{-1}(U_x \cap V_x)$. This is open and connected, and hence so is its homeomorphic image $\phi(B^\circ_{\phi^{-1}(x)}(\epsilon)) \subset X$. This is a connected open neighbourhood of $x$ as required.

Regarding the fourth statement:

Let $x \in X$ be a point and let $U_x \supset \{x\}$ be an open neighbourhood. We need to find a compact neighbourhood $K_x \subset U_x$.

By assumption there exists a Euclidean open neighbourhood $\mathbb{R}^n \underoverset{\simeq}{\phi}{\to} V_x \subset X$. By definition of the [[subspace topology]] the intersection $U_x \cap V_x$ is still open as a subspace of $V_x$ and hence $\phi^{-1}(U_x \cap V_x)$ is an open neighbourhood of $\phi^{-1}(x)  \in \mathbb{R}^n$.

Since Euclidean spaces are locally compact, there exists a compact neighbourhood $K_{\phi^{-1}(x)} \subset \mathbb{R}^n$ (for instance a sufficiently small [[closed ball]] around $x$, which is compact by the [[Heine-Borel theorem]]). Now since [[continuous images of compact spaces are compact]], it follows that also $\phi(K) \subset X$ is a compact neighbourhood.

=--

But the "global" topological properties of Euclidean space are not generally inherited by locally Euclidean spaces. This sounds obvious, but notice that also Hausdorff-ness is a "global property":

+-- {: .num_remark}
###### Remark
**(locally Euclidean spaces are not necessarily $T_2$)**

It might superficially seem that every locally Euclidean space (def. \ref{LocallyEuclideanSpace}) is necessarily a [[Hausdorff topological space]], since [[Euclidean space]], like any [[metric space]], is Hausdorff, and since by definition the neighbourhood of every point in a locally Euclidean spaces looks like Euclidean space.

But this is not so, Hausdorffness is a "non-local condition".

=--

+-- {: .num_example #NonHausdorffManifolds}
###### Nonexample
**([[non-Hausdorff locally Euclidean spaces]])**

An example of a [[locally Euclidean space]] (def. \ref{LocallyEuclideanSpace}) which is a [[non-Hausdorff topological space]], is the [[line with two origins]].

=--

+-- {: .num_lemma #PathConnectedFromConnectedLocallyEuclideanSpace}
###### Lemma
**(connected locally Euclidean spaces are path-connected)**

A locally Euclidean space which is [[connected topological space|connected]] is also [[path-connected topological space|path-connected]].

=--

+-- {: .proof}
###### Proof

Fix any $x \in X$. Write $PConn_x(X) \subset X$ for the subset of all those points of $x$ which are connected to $x$ by a path, hence

$$
  PConn_x(X)
  \;\colon\;
  \left\{
    y \in X
   \;\vert\;
   \underset{[0,1] \underoverset{cts}{\gamma}{\to} X }{\exists}
   \left(
      \left(\gamma(0) = x\right)
      \phantom{A} \text{and} \phantom{a}
      \left(
        \gamma(1) = y
      \right)
   \right)
  \right\}
  \,.
$$

Observe now that both $PConn_x(X) \subset X$ as well as its [[complement]] are [[open subsets]]:

To see this it is sufficient to find for every point $y \on PConn_x(X)$ an [[open neighbourhood]] $U_y \supset \{y\}$ such that $U_y \subset PConn_x(X)$, and similarly for the complement.

Now by assumption every point $y \in X$ has a Euclidean neighbourhood $\mathbb{R}^n \overset{\simeq}{\to} U_y \subset X$. Since Euclidean space is path connected, there is for every $z \in U_y$ a path $\tilde \gamma \colon [0,1] \to X$ connecting $y$ with $z$, i.e. with $\tilde \gamma(0) = y$ and $\tilde \gamma(1) = z$. Accordingly the composite path

$$
  \array{
     [0,1] &\overset{\tilde \gamma\cdot\gamma}{\longrightarrow}& X
     \\
     t &\overset{\phantom{AAA}}{\mapsto}&
    \left\{
      \array{
         \gamma(2t) &\vert& t \leq 1/2
         \\
         \tilde(2t-1/2) &\vert& t \geq 1/2
      }
    \right.
  }
$$

connects $x$ with $z \in U_y$. Hence $U_y \subset PConn_x(X)$.

Similarly, if $y$ is not connected to $x$ by a path, then also all point in $U_y$ cannot be connected to $x$ by a path, for if they were, then the analogous concatenation of paths would give a path from $x$ to $y$, contrary to the assumption.

It follows that

$$
  X = PConn_x(C) \sqcup (X \setminus PConn_x(X))
$$

is a decomposition of $X$ as the [[disjoint union]] of two open subsets. By the assumption that $X$ is connected, exactly one of these open subsets is empty. Since $PConn_x(X)$ is not empty, as it contains $x$, it follows that its compement is empty, hence that $PConn_x(X) = X$, hence that $(X,\tau)$ is path connected.

=--


+-- {: .num_prop #RegularityConditionsForTopologicalManifoldsComparison}
###### Proposition
**(equivalence of regularity conditions for Hausdorff  locally Euclidean spaces)**

Let $X$ be a [[locally Euclidean space]] (def. \ref{LocallyEuclideanSpace}) which is [[Hausdorff topological space|Hausdorff]].

Then the following are equivalent:

1. $X$ is [[sigma-compact topological space|sigma-compact]],

1. $X$ is [[second-countable topological space|second-countable]],

1. $X$ is [[paracompact topological space|paracompact]] and has a [[countable set]] of [[connected components]],



=--

+-- {: .proof}
###### Proof

Generally, observe that $X$ is [[locally compact]]:
By prop. \ref{LocalPropertiesOfLocallyEuclideanSpace} every locally Euclidean space is locally compact in the sense that every point has a [[neighbourhood base]] of compact neighbourhoods, and since $X$ is assumed to be Hausdorff, this implies all the other variants of definition of local compactness, by [this prop.](locally+compact+topological+space#InHausdorffSpacesDefinitionsOfLocalCompactnessAgree).

**1) $\Rightarrow$ 2)**

Let $X$ be sigma-compact. We show that then $X$ is [[second-countable topological space|second-countable]]:

By sigma-compactness there exists a [[countable set]] $\{K_i \subset X\}_{i \in I}$ of compact subspaces. By $X$ being locally Euclidean, each admits an [[open cover]] by restrictions of [[Euclidean spaces]]. By their compactness, each of these has a subcover $\{ \mathbb{R}^n \overset{\phi_{i,j}}{\to} X \}_{j \in J_i}$ with $J_i$ a finite set. Since [[countable unions of countable sets are countable]], we have obtained  a countable cover by Euclidean spaces $\{ \mathbb{R}^n  \overset{\phi_{i,j}}{\to} X\}_{i \in I, j \in J_i}$. Now Euclidean space itself is second countable (by [this example](second-countable+space#SecondCountableEuclideanSpace)), hence admits a countable set $\beta_{\mathbb{R}^n}$ of base open sets. As a result the union $\underset{{i \in I} \atop {j \in J_i}}{\cup} \phi_{i,j}(\beta_{\mathbb{R}^n})$ is a base of opens for $X$. But this is a countable union of countable sets, and since [[countable unions of countable sets are countable]] we have obtained a countable base for the topology of $X$. This means that $X$ is second-countable.

**1) $\Rightarrow$ 3)**

Let $X$ be sigma-compact. We show that then $X$ is paracompact with a countable set of connected components:

Since [[locally compact and sigma-compact spaces are paracompact]], it follows that $X$ is paracompact. By [[locally connected topological space|local connectivity]] (prop. \ref{LocalPropertiesOfLocallyEuclideanSpace}) $X$ is the [[disjoint union space]] of its [[connected components]] ([this prop.](locally+connected+topological+space#AlternativeCharacterizationsOfLocalConnectivity)). Since, by the previous statement, $X$ is also second-countable it cannot have an uncountable set of connected components.

**2)$\Rightarrow$ 1)** Let $X$ be second-countable, we need to show that it is sigma-compact.

This follows since [[locally compact and second-countable spaces are sigma-compact]].

**3) $\Rightarrow$ 1)**

Now let $X$ be paracompact with countably many connected components. We show that $X$ is sigma-compact.

Since $X$ is locally compact, there exists a cover $\{K_i = Cl(U_i) \subset X\}_{i \in I}$ by [[compact topological space|compact]] [[subspaces]].
By paracompactness there is a locally finite refinement of this cover. Since [[paracompact Hausdorff spaces are normal]], the [[shrinking lemma]] applies to this refinement and yields a locally finite open cover

$$
  \mathcal{V} \coloneqq \{V_j \subset X \}_{j \in J}
$$

as well as a locally finite cover $\{Cl(V_j) \subset X\}_{j \in J}$ by closed subsets. Since this is a refinement of the orignal cover, all the $Cl(V_j)$ are contained in one of the compact subspaces $K_i$. Since [[subsets are closed in a closed subspace precisely if they are closed in the ambient space]], the $Cl(V_j)$ are also closed as subsets of the $K_i$. Since [[closed subsets of compact spaces are compact]] it follows that the $Cl(V_j)$ are themselves compact and hence form a locally finite cover by compact subspaces.

Now fix any $j_0 \in J$.

We claim that for every $j \in J$ there is a finite sequence of indices $(j_0, j_1, \cdots, j_n = j)$ with the property
that $V_{j_k} \cap V_{j_{k+1}} \neq \emptyset$.

To see this, first observe that it is sufficient to show sigma-compactness for the case that $X$ is [[connected topological space|connected]]. From this the general statement follows since [[countable unions of countable sets are countable]]. Hence assume that $X$ is connected.
It follows from lemma \ref{PathConnectedFromConnectedLocallyEuclideanSpace} that  $X$ is [[path-connected topological space|path-connected]].

Hence for any $x \in V_{j_0}$ and $y \in V_{j}$ there is a path $\gamma \colon [0,1] \to X$ connecting $x$ with $y$. Since the [[closed interval]] is compact and since [[continuous images of compact spaces are compact]], it follows that there is a finite subset of the $V_i$ that covers the image of this path. This proves the claim.

It follows that there is a function

$$
  f \;\colon\; \mathcal{V} \longrightarrow \mathbb{N}
$$

which sends each $V_j$ to the [[minimum]] natural number as above.

We claim now that for all $n \in \mathbb{N}$ the [[preimage]] of $\{0,1, \cdots, n\}$ under this function is a [[finite set]]. Since [[countable unions of countable sets are countable]] this implies that $\{ Cl(V_j) \subset X\}_{j \in J}$ is a countable cover of $X$ by compact subspaces, hence that $X$ is sigma-compact.

We prove this last claim by [[induction]]. It is true for $n = 0$ by construction. Assume it is true for some $n \in \mathbb{N}$, hence that $f^{-1}(\{0,1, \cdots, n\})$ is a finite set. Since finite unions of compact subspaces are again compact ([this prop.](compact+space#UnionsAndIntersectionOfCompactSubspaces)) it follows that

$$
  K_n
    \coloneqq
  \underset{V \in f^{-1}(\{0,\cdots, n\})}{\cup} V
$$

is compact. By local finiteness of the $\{V_j\}_{j \in J}$, every point $x \in K_n$ has an open neighbourhood $W_x$ that intersects only a finite set of the $V_j$. By compactness of $K_n$, the cover $\{W_x \subset X\}_{x \in K_n}$ has a finite subcover. In conclusion this implies that only a finite number of the $V_j$ intersect $K_n$.

Now by definition $f^{-1}(\{0,1,\cdots, n+1\})$ is a subset of those $V_j$ which intersect $K_n$, and hence itself finite.

=--


### Topological manifold


+-- {: .num_defn #TopologicalManifold}
###### Definition
**([[topological manifold]])**

A _topological manifold is a [[topological space]] which is

1. [[locally Euclidean topological space|locally Euclidean]] (def. \ref{LocallyEuclideanSpace}),

1. [[paracompact Hausdorff topological space|paracompact Hausdorff]].


If the local [[Euclidean spaces|Euclidean]] neighbourhoods $\mathbb{R}^n \overset{\simeq}{\to} U \subset X$ are all of [[dimension]] $n$
for a fixed $n \in \mathbb{N}$, then the topological manifold is said to be a _$n$-dimensional manifold_ or _$n$-fold_. This is usually assumed to be the case.

=--

+-- {: .num_remark}
###### Remark
**(varying terminology)**

Often a topological manifold (def. \ref{TopologicalManifold}) is required to be [[sigma-compact]]. But by prop. \ref{RegularityConditionsForTopologicalManifoldsComparison} this is not an extra condition as long as there is a [[countable set]] of [[connected components]].

=--



### Differentiable manifolds

+-- {: .num_defn #Charts}
###### Definition
**([[local chart]] and [[atlas]] and [[gluing function]])

Given an $n$-dimensional topological manifold $X$ (def. \ref{TopologicalManifold}), then

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/ChartsOfAManifold.png" width="400">
</div>


1. an [[open subset]] $U \subset X$ and a [[homeomorphism]] $\phi \colon \mathbb{R}^n \overset{\phantom{A}\simeq\phantom{A}}{\to} U$ is also called a _[[local coordinate chart]]_ of $X$.

1. an [[open cover]] of $X$ by local charts $\left\{ \mathbb{R}^n \overset{\phi_i}{\to} U \subset X \right\}_{i \in I}$ is called an _[[atlas]]_ of the topological manifold.

1. denoting for each $i,j \in I$ the [[intersection]] of the $i$th chart with the $j$th chart in such an atlas by

   $$
     U_{i j} \coloneqq U_i \cap U_j
   $$

   then the induced homeomorphism

   $$
     \mathbb{R}^n
       \supset
        \phantom{AA}
     \phi_i^{-1}(U_{i j})
       \overset{\phantom{A}\phi_i\phantom{A}}{\longrightarrow}
     U_{i j}
       \overset{\phantom{A}\phi_j^{-1}\phantom{A}}{\longrightarrow}
     \phi_j^{-1}(U_{i j})
       \phantom{AA}
       \subset
     \mathbb{R}^n
   $$

   is called the _[[gluing function]]_ from chart $i$ to chart $j$.

> graphics grabbed from [[The Geometry of Physics - An Introduction|Frankel]]


=--


+-- {: .num_defn #Differentiable manifold}
###### Definition
**([[differentiable manifold|differentiable]] and [[smooth manifolds]])**

For $p \in \mathbb{N} \cup \{\infty\}$ then a $p$-fold _[[differentiable manifold]]_ is

1. a [[topological manifold]] $X$ (def. \ref{TopologicalManifold});

1. an [[atlas]] $\{\mathbb{R}^n \overset{\phi_i}{\to} X\}$ (def. \ref{Charts}) all whose [[gluing functions]]  are $p$ times continuously [[differentiable function|differentiable]].

A $p$-fold [[differentiable function]] between $p$-fold differentiable manifolds

$$
  (X, \{\mathbb{R}^{n} \overset{\phi_i}{\to} U_i \subset X\}_{i \in I})
   \overset{\phantom{AA}f\phantom{AA}}{\longrightarrow}
  (Y, \{\mathbb{R}^{n'} \overset{\psi_j}{\to} V_j \subset Y\}_{j \in J})
$$

is

* a [[continuous function]] $f \colon X \to Y$

such that

* for all $i \in I$ and $j \in J$ then

  $$
     \mathbb{R}^n
     \supset
      \phantom{AA}
     (f\circ \phi_i)^{-1}(V_j)
       \overset{\phi_i}{\longrightarrow}
     f^{-1}(V_j)
      \overset{f}{\longrightarrow}
     V_j
       \overset{\psi_j^{-1}}{\longrightarrow}
     \mathbb{R}^{n'}
  $$

  is a $p$-fold [[differentiable function]] between open subsets of [[Euclidean space]].

=--

Notice that this in in general  a non-trivial condition even if $X = Y$ and $f$ is the identity function. In this case the above exhibits a passage to a different, but equivalent, differentiable atlas.

## Properties

+-- {: .num_prop #OpenSubsetsOfDifferentiableManifoldsAreDifferentiableManifolds}
###### Proposition

Let $X$ be a $k$-fold differentiable manifold and let $S \subset X$
be an [[open subset]] of the underlying [[topological space]] $(X,\tau)$.

Then $S$ carries the structure of a $k$-fold differentiable manifold such that the
inclusion map $S \hookrightarrow X$ is an [[open embedding|open]]
[[embedding of differentiable manifolds]].

=--

+-- {: .proof}
###### Proof


Since the underlying [[topological space]] of $X$ is [[locally connected topological space|locally connected]] ([this prop.](topological+manifold#LocalPropertiesOfLocallyEuclideanSpace)) it is the [[disjoint union space]] of its [[connected components]] ([this prop.](locally+connected+topological+space#AlternativeCharacterizationsOfLocalConnectivity)).

Therefore we are reduced to showing the statement for the case that $X$ has a single [[connected component]]. By [this prop](topological+manifold#RegularityConditionsForTopologicalManifoldsComparison) this implies that $X$ is [[second-countable topological space]].

Now a [[subspace]] of a second-countable Hausdorff space is clearly itself second countable and Hausdorff.

Similarly it is immediate that $S$ is still [[locally Euclidean space|locally Euclidean]]: since $X$ is locally Euclidean every point $x \in S \subset X$ has a Euclidean neighbourhood in $X$ and since $S$ is open there exists an open ball in that (itself [[homeomorphism|homeomorphic]] to Euclidean space) which is a Euclidean neighbourhood of $x$ contained in $S$.

For the differentiable structure we pick these Euclidean neighbourhoods from the given atlas.
Then the [[gluing functions]] for the Euclidean charts on $S$ are $k$-fold differentiable follows since these are restrictions of the gluing functions for the atlas of $X$.

=--




## Examples

See the examples at _[[differentiable manifold]]_.


## References

Textbook accounts:

* [[John M. Lee]], _Introduction to topological manifolds_. Graduate Texts in Mathematics 202 (2000), Springer.  ISBN: 0-387-98759-2, 0-387-95026-5.
Second edition: Springer, 2011.  ISBN: 978-1-4419-7939-1 ([doi:10.1007/978-1-4419-7940-7](https://doi.org/10.1007/978-1-4419-7940-7), errata [pdf](https://sites.math.washington.edu/~lee/Books/ITM/errata.pdf))

See also

* Wikipedia, _[Topological manifold](https://en.wikipedia.org/wiki/Topological_manifold)_


[[!redirects topological manifolds]]

[[!redirects locally Euclidean topological space]]
[[!redirects locally Euclidean topological spaces]]

[[!redirects locally Euclidean space]]
[[!redirects locally Euclidean spaces]]

