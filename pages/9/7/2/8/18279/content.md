
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context###
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


It is not generally true that a [[topological space]] is the [[disjoint union space]] ([[coproduct]] in [[Top]]) of its [[connected components]]. The spaces such that this is true for all open subspaces are the _locally connected topological spaces_.


## Definition
  {#Definition}

+-- {: .num_defn #LocallyConnected}
###### Definition 
**(locally connected topological space)**

A [[topological space]] $X$ is **locally connected** if  every point has a [[neighborhood basis]] of [[connected topological space|connected]] [[open subsets]]. 

=-- 


+-- {: .num_prop #AlternativeCharacterizationsOfLocalConnectivity}
###### Proposition
**(alternative characterizations of local connectivity)**

For $X$ a [[topological space]], then the following are equivalent:

1. $X$ is locally connected (def. \ref{LocallyConnected});

1. every [[connected component]] of every open [[subspace]] of $X$ is open;

1. every [[open subset]], as a [[topological subspace]], is the [[disjoint union space]] ([[coproduct]] in [[Top]]) of its [[connected components]].

In particular, in a locally connected space, every connected component $S$ is a [[clopen subset]]; hence connected components and quasi-components coincide. 


=--

+-- {: .proof}
###### Proof

$\,$

1) $\Rightarrow$ 2)

Assume $X$ is locally connected, and let $U \subset X$ be an open subset with $U_0 \subset U$ a connected component. We need to show that $U_0$ is open.

Consider any point $x \in U_0$. Since then also $x \in U$, the defintion of local connectedness, def. \ref{LocallyConnected}, implies that there is a connected open neighbourhood $U_{x,0}$ of $X$. Observe that this must be contained in $U_0$, for if it were not then $U_0 \cup U_{x,0}$ were a larger open connected open neighbourhood, contradicting the maximality of the connected component $U_0$. 

Hence $U_0 = \underset{x \in U_0}{\cup} U_{x,0}$ is a union of open  subsets, and hence itself open.

2) $\Rightarrow$ 3)

Now assume that every connected component of every open subset $U$ is open. Since the connected components generally consitute a [[cover]] of $X$ by [[disjoint subsets]] this means that now they for an [[open cover]] by disjoint subsets. But by forming intersections with the cover this implies that every open subset of $U$ is the disjoint union of open subsets of the connected components (and of course every union of open subsets of the connected components is still open in $U$), which is the definition of the topology on the [[disjoint union space]] of the connected components.

3) $\Rightarrow$ 1)

Finally assume that every open subspace is the disjoint union of its connected components. Let $x$ be a point and $U_x \supset \{x\}$ a neighbourhood. We need to show that $U_x$ contains a connected neighbourhood of $x$.

But, by definition, $U_x$ contains an open neighbourhood of $x$ and by assumption this decomposes as the disjoint union of its connected components. One of these contains $x$. Since in a [[disjoint union space]] all summands are open, this is the required connected open neighbourhod.

=--


## Examples

* Trivially, [[every discrete topological space is locally connected]].

+-- {: .num_example #LocallyConnectedEuclideanSpace}
###### Example
**([[Euclidean space]] is locally connected)

For $n \in \mathbb{N}$ the [[Euclidean space]] $\mathbb{R}^n$ (with its [[metric topology]]) is locally connected.

=--

+-- {: .proof}
###### Proof

By nature of the Euclidean metric topology, every neighbourhood $U_x$ of a point $x$ contains an [[open ball]] containing $x$. Moreover, every open ball clearly contains an open cube, hence a [[product space]] $\underset{i \in \{1, \cdots, n\}}{\prod} (x_i-\epsilon, x_i + \epsilon)$ of [[open intervals]] which is still a neighbourhood of $x$. 

Now intervals are connected (by [this example](connected+space#ConnectedSubspacesOfRealLineAreTheIntervals)) and products of connected spaces are connected (by [this example](connected+space#ProductSpaceOfConnectedSpacesIsConnected)). This shows that ever open neighbourhood contains a connected neighbourhood.

=--

+-- {: .num_prop #LocallyConnectedOpenSubspaceOfLocallyConnectedSpace}
###### Proposition
**([[open subset|open]] [[subspace]] of locally connected space is locally connected)**

Every [[open subset|open]] [[subspace]] of a locally connected space is itself locally connected
 
=--

+-- {: .proof}
###### Proof

This is immediate from def. \ref{LocallyConnected}.

=--

+-- {: .num_remark}
###### Remark
**Warning**

A [[connected topological space]] need not be locally connected. 

=--

+-- {: .num_example}
###### Example

The [[topologist's sine curve]] is connected but not locally connected. 

=--

Examples of locally connected spaces include [[manifold|topological manifolds]]. 


Finally, 

+-- {: .num_defn} 
###### Definition 
A space $X$ is **[[totally disconnected topological space]]** if its [[connected components]] are precisely the [[singletons]] of $X$. 

=-- 

In other words, a space is totally disconnected if its coreflection into $LocConn$ is discrete. Such spaces recur in the study of [[Stone spaces]]. 

The category of totally disconnected spaces is a reflective subcategory of $Top$. The reflector sends a space $X$ to the space $X/\sim$ whose points are the connected components of $X$, endowed with the quotient topology induced by the projection $q: X \to X/\sim$. Details may be found at [[totally disconnected space]]. 

## Properties

### The category of locally connected spaces

Let $i \colon LocConn \hookrightarrow Top$ be the [[full subcategory]] inclusion of locally connected spaces into all of [[Top]]. The following result is straightforward but useful. 

+-- {: .num_theorem #coref} 
###### Theorem 

$LocConn$ is a [[coreflective subcategory]] of $Top$, i.e., the inclusion $i$ has a [[right adjoint]] $R$. For $X$ a given space, $R(X)$ has the same underlying set as $X$ and the coarsest locally connected topology that is finer than the original topology on $X$. 

=-- 

Being a coreflective category of a complete and cocomplete category, the category $LocConn$ is also complete and cocomplete. Of course, limits and particularly _infinite_ products in $LocConn$ are not calculated as they are in $Top$; rather one takes the limit in $Top$ and _then_ retopologizes it according to Theorem \ref{coref}. (For _finite_ products of locally connected spaces, we can just take the product in $Top$ -- the result will be again locally connected.) 

### Cohesion over sets

Let $\Gamma \colon LocConn \to Set$ be the underlying set functor, and let $\nabla, \Delta \colon Set \to LocConn$ be the functors which assign to a set the same set equipped with the codiscrete and discrete topologies, respectively. Let $\Pi_0 \colon LocConn \to Set$ be the functor which assigns to a locally connected space the set of its connected components. 

+-- {: .num_theorem} 
###### Theorem 
There is an [[adjoint quadruple]] of [[adjoint functors]]

$$
  \Pi_0 \dashv \Delta \dashv \Gamma \dashv \nabla \colon Set \to LocConn
$$ 

and moreover, the functor $\Pi_0$ preserves finite products. 

=-- 

The proof is largely straightforward; we point out that the continuity of the unit $X \to \Delta \Pi_0 X$ is immediate from a locally connected space's being the coproduct of its connected components. As for $\Pi_0$ preserving finite products, write locally connected spaces $X$, $Y$ as coproducts of connected spaces 

$$X = \sum_i C_i; \qquad Y = \sum_j D_j;$$ 

then their product in $LocConn$ coincides with their product in $Top$, and is 

$$X \times Y \cong \sum_{i, j} C_i \times D_j$$ 

where each summand $C_i \times D_j$ is connected by Result \ref{3}. From this it is immediate that $\Pi_0$ preserves finite products. 

Accordingly the [[category of sheaves]] on a locally connected space is a [[locally connected topos]]. For related discussions, see also [[cohesive topos]]. 



### Quotients of locally connected spaces 


+-- {: .num_lemma #quot} 
###### Lemma 

A [[quotient space]] of a locally connected space $X$ is also locally connected. 

=-- 

+-- {: .proof} 
###### Proof 
Suppose $q: X \to Y$ is a quotient map, and let $V \subseteq Y$ be an open neighborhood of $y \in Y$. Let $C(y)$ be the connected component of $y$ in $V$; we must show $C(y)$ is open in $Y$. For that it suffices that $C = q^{-1}(C(y))$ be open in $X$, or that each $x \in C$ is an interior point. Since $X$ is locally connected, the connected component $U_x$ of $x$ in $q^{-1}(V)$ is open, and the subset $q(U_x) \subseteq V$ is connected, and therefore $q(U_x) \subseteq C(y)$ (as $C(y)$ is the maximal connected subset of $V$ containing $q(x)$). Hence $U_x \subseteq q^{-1}(C(y)) = C$, proving that $x$ is interior to $C$, as desired. 
=-- 

The conclusion does not follow if $q: X \to Y$ is merely surjective; e.g., there is a surjective (continuous) map from $\mathbb{R}$ to (a version of) the [[Warsaw circle]], but the latter is not locally connected. 

## Related concepts

* [[totally disconnected topological space]]

* [[locally connected topos]]


[[!redirects locally connected space]]
[[!redirects locally connected spaces]]
[[!redirects locally connected topological space]]
[[!redirects locally connected topological spaces]]
