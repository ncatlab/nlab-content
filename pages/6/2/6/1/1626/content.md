
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context###
#### Topology
+-- {: .hide}
[[!include topology - contents]]t
=--
=--
=--



# Contents
* table of contents
{:toc}

## Idea

A [[topological space]] is __connected__ if it can not be split up into two independent parts.

Every topological space may be decomposed into disjoint maximal connected [[subspaces]], called its __[[connected components]]__.  The underlying set of a topological space is the [[disjoint union]] of the underlying sets of its connected components, but the space itself is not necessarily the [[coproduct]] of its connected components in the category of spaces.

One often studies topological ideas first for connected spaces and then generalises to general spaces.  This is especially true if one is studying such [[nice topological space]]s that every space *is* a coproduct of connected components (such as for example _[[locally connected topological spaces]]_).


## Definitions

### Elementary definition

+-- {: .num_defn #ConnectedSpace}
###### Definition
**(connected topological space)**

A [[topological space]] $(X, \tau)$ is _connected_ if the following equivalent conditions hold:

1. For all pairs of topological spaces $(X_1, \tau_1), (X_2, \tau_2)$ such that $(X, \tau)$ is [[homeomorphism|homeomorphic]] to their [[disjoint union space]]

   $$
     (X,\tau) \simeq (X_1,\tau_1) \sqcup (X_2,\tau_2)
   $$

   then exactly one of the two spaces is the [[empty space]].

1. For all pairs of [[open subsets]] $U_1, U_2 \subset X$ if

   $$
     U_1 \cup U_2 = X \phantom{A}\text{and} \phantom{A} U_1 \cap U_2 = \emptyset
   $$

   then exactly one of the two subsets is the [[empty set]]. 


1. if a [[subset]] $CO \subseteq X$ is [[clopen set|clopen]] (both closed and open), then $ CO = X$ if and only if $CO$ is [[inhabited set|inhabited]].

=--

+-- {: .num_remark #ConnectedEmptySpace}
###### Remark

According to def. \ref{ConnectedSpace} the [[empty topological space]] is not regarded as connected. Some authors do want the empty space to count as a connected space. This means to change in the first item of def. \ref{ConnectedSpace} the "exactly one" to "at least one" and in the second item "if and only if" to "if".

=--

+-- {: .num_prop}
###### Proposition

The conditions in def. \ref{ConnectedSpace} are indeed equivalent.

=--

+-- {: .proof}
###### Proof

First consider the equivalence of the first two statements:

Suppose that in every disjoint union decomposition of $(X,\tau)$ then exactly one summand is empty. Now consider two disjoint open subsets $U_1, U_2 \subset X$ whose union is $X$ and whose intersection is empty. We need to show that exactly one of the two subsets is empty.

Write $(U_1, \tau_{1})$ and $(U_2, \tau_2)$ for the corresponding [[topological subspaces]]. Then observe that from the definition of [[subspace topology]] and the [[disjoint union space]] we have a [[homeomorphism]]

$$
  X \simeq (U_1, \tau_1) \sqcup (U_2, \tau_2)
$$

because by assumption every open subset $U \subset X$ is the disjoint union of open subsets of $U_1$ and $U_2$, respectively:

$$
  U = U \cap X = U \cap (U_1 \sqcup U_2) = (U \cap U_1) \sqcup (U \cap U_2)
  \,,
$$

which is the definition of the disjoint union topology.


Hence by assumption exactly one of the two summand spaces is the [[empty space]] and hence the underlying set is the empty set.

Conversely, suppose that for every pair of open subsets $U_1, U_2 \subset U$ with $U_1 \cup U_2 = X$ and $U_1 \cap U_2 = \emptyset$ then exactly one of the two is empty. Now consider a homeomorphism of the form $(X,\tau) \simeq (X_1, \tau_1) \sqcup (X_2,\tau_2)$. By the nature of the [[disjoint union space]] this means that $X_1, X_2 \subset X$ are disjoint open subsets of $X$ which cover $X$. So by asumption precisely one of the two subsets is the empty set and hence precisely one of the two topological spaces is the empty space.

Now regarding the equivalence to the third statement:

If a subset $CO \subset X$ is both closed and open, this means equivalently that it is open and that its [[complement]] $X \setminus CO$ is also open, hence equivalently that there are two open subsets $CO, X \backslash CO \subset X$ whose union is $X$ and whose intersection is empty. This way the third condition is equivalent to the second.

=--


### Category-theoretic definition

In the language of [[category theory]] def. \ref{ConnectedSpace} may be rephrased as follows:

Write [[Top]] for the [[category]] of all [[topological space]].

Then a topological space $X$ is connected precisely if the [[representable functor]]

$$
  hom(X, -) \;\colon\; Top \longrightarrow Set
$$

preserves [[coproducts]].


It is equivalent to just require that it preserves binary coproducts (a detailed proof in a more general setting is given at _[[connected object]]_ in [this proposition](connected+object#RespectForBinaryCoproductsIsSufficient). In that case, notice that we always have a map
$$ hom(X,Y) + hom(X,Z) \to hom(X,Y + Z) ,$$
so $X$ is connected if this is always a [[bijection]]. This definition generalises to the notion of [[connected object]] in an [[extensive category]].

The variant of the definition according to remark \ref{ConnectedEmptySpace}, which regards the empty space means in terms of category theoretic language that one
requires only that the maps
$$ hom(X,Y) + hom(X,Z) \to hom(X,Y + Z) $$
be [[surjections]].

However, many results come out more cleanly by disqualifying the empty space (much as one disqualifies $1$ when one defines the notion of [[prime number]]).  See also the discussion at [[empty space]] and [[too simple to be simple]].


### Connected components

Every topological space $X$ admits an [[equivalence relation]] $\sim$ where $x \sim y$ means that $x$ and $y$ belong to some subspace which is connected. The [[equivalence class]] $Conn(x)$ of an element $x$ is thus the union of all connected subspaces containing $x$; it follows readily from Result \ref{2} that $Conn(x)$ is itself connected. It is called the **connected component** of $x$. It is closed, by Result \ref{5}. A space is connected if and only if it has exactly one connected component (or at most one, if you allow the empty space to be connected).

+-- {: .num_defn #ComponentsConnected}
###### Definition
**(connected components)**

For $(X,\tau)$ a [[topological space]], its _[[connected components]]_
are the [[equivalence classes]] under the [[equivalence relation]] on $X$ which
regards two points as equivalent if they both sit in some [[open subset]] which, as a [[topological subspace]] (example \ref{SubspaceTopology}), is [[connected topological space|connected]] (def. \ref{ConnectedTopologicalSpace}):

$$
  (x \sim y)
    \;\coloneqq\;
  \left(
    \underset{ U \subset X \; \text{\open} }{\exists}
    \left(
       \left( x,y \in U \right)
        \phantom{A}\text{and}\phantom{A}
       \left( U \, \text{is connected} \right)
    \right)
  \right)
  \,.
$$

=--

+-- {: .num_defn #QuasiComponentsConnected}
###### Remark
**(quasi-components)**


There is another [[equivalence relation]] $\sim_q$ modelling a notion of connected components,  where $x \sim_q y$ iff $f(x) = f(y)$ for every [[continuous map]] $f \colon X \to D$ to a _[[discrete space]]_ $D$. 

The corresponding [[equivalence class]] of $x$ may alternatively be described as the [[intersection]] of all [[clopen set|clopen subsets]] that contain $x$. This is called the **quasi-component** of $x$, denoted here as $QConn(x)$. 

It is easy to prove that this relates to the equivalence classes $Conn(x)$ from Def. \ref{ComponentsConnected} as

$$Conn(x) \subseteq QConn(x)$$

and that equality holds if $X$ is [[compact Hausdorff space|compact Hausdorff]] or is [[locally connected topological space|locally connected]], but also in other circumstances (such as the space of [[rational numbers]] as a [[topological subspace|subspace]] of the [[real line]]).

=--

+-- {: .num_example #comb}
###### Example
For an example where $Conn(x) \neq QConn(x)$, take $X$ to be the following [[subspace]] of $[0, 1] \times [0, 1]$:

$$X = \{(0, 0), (0, 1)\} \cup \bigcup_{n \geq 1} \{1/n\} \times [0, 1]$$

In this example, $Conn((0, 1)) = \{(0, 1)\}$, but $QConn((0, 1)) = \{(0, 0), (0, 1)\}$.
=-- 

+-- {: .num_remark}
###### Remark
**Warning**

It is not generally true that a [[topological space]] is the [[disjoint union space]] ([[coproduct]] in [[Top]]) of its [[connected components]], nor of its quasi-components.

The spaces such that all their open subspaces are the disjoint union of their connected components are the _[[locally connected topological spaces]]_.

=--

+-- {: .num_example}
###### Example

The connected components in [[Cantor space]] $2^{\mathbb{N}}$ (with its topology as a product of 2-point discrete spaces) are just the [[singletons]], but the coproduct of the singleton subspaces carries the [[discrete topology]], which differs from that of Cantor space.

Similarly for set of [[rational numbers]] with its absolute-value topology (the one induced as a [[topological subspace]] of the [[real line]]).

=--




## Examples

### Basic examples {#basic}


+-- {: .num_example #ContinuousImagesOfConnectedSpacesAreConnected}
###### Example
**([[continuous function|continuous]] [[images]] of connected spaces are connected)**

The [[regular monomorphism|regular]] [[image]] of a connected space $X$ under a continuous map $f: X \to Y$ (i.e., the set-theoretic image with the subspace topology inherited from $Y$) is connected. Or, what is essentially the same: if $X$ is connected and $f: X \to Y$ is [[epimorphism|epic]], then $Y$ is connected:

Let $X$ be a connected topological space, let $Y$ be any [[topological space]], and let

$$
  f \;\colon\; X \longrightarrow Y
$$

be a [[continuous function]]. This factors via continuous functions through the [[image]]

$$
  f \;\colon\; X \underoverset{surjective}{p}{\longrightarrow} f(X) \underoverset{injective}{i}{\longrightarrow} Y
$$

for $f(X)$ equipped either with the [[subspace topology]] relative to $Y$ or the [[quotient topology]] relative to $X$. In either case:

If $X$ is a connected topological space, then so is $f(X)$.

=--

+-- {: .proof}
###### Proof

Let $U_1,U_2 \subset f(X)$ be two [[open subsets]] such that $U_1 \cup U_2 = f(X)$ and $U_1 \cap U_2 = \emptyset$.
We need to show that precisely one of them is the [[empty set]].

Since $p$ is a [[continuous function]], also the [[pre-images]] $p^{-1}(U_1), p^{-1}(U_2) \subset X$
are open subsets and are still disjoint. Since preimages preserve unions it also follows that
$p^{-1}(U_1) \cup p^{-1}(U_2) = X$. Since $X$ is connected, it follows that one of these two pre-images $p^{-1}(U_i)$ is
the empty set. Since $p$ is [[surjective function|surjective]], this implies that $U_i$ is empty,
which means that $f(X)$ is connected.

=--


+-- {: .num_example #2}
###### Example
[[pushout|Wide pushout]]s of connected spaces are connected. (This would of course be false if the empty space were considered to be connected.) This follows from the hom-functor definition of connectedness, plus the fact that coproducts in $Set$ commute with [[wide pullback]]s. More memorably: [[connected limit|connected colimits]] of connected spaces are connected.
=--

+-- {: .num_example #5}
###### Example
If $S \subseteq X$ is a connected subspace and $S \subseteq T \subseteq \overline{S}$ (i.e. if $T$ is between $S$ and its closure), then $T$ is connected. Or, what is essentially the same: if $T$ has a [[dense subspace|dense]] connected subspace $S$, then $T$ is connected.
=--

(see also prop. \ref{ClosureOfConnectedSubspaceIsConnected} below)

+-- {: .num_example #ProductSpaceOfConnectedSpacesIsConnected}
###### Example
**([[product space]] of connected spaces is connected)

Let $\{X_i\}_{i \in I}$ be a set of connected spaces. Then also their [[product topological space]]
$\underset{i \in I}{\prod}X_i$ (with the [[Tychonoff topology]]) is connected.

=--

+-- {: .proof}
###### Proof

This relies on some special features of [[Top]]. 
A general abstract proof is given at _[[connected object]]_ in [this theorem](connected+object#prod)
and [this remark](connected+object#prod2).

Here is an alternative elementary proof in [[point-set topology]]:

Let $U_1, U_2 \subset \underset{i \in I}{\prod}X_i$ be an [[open cover]]
of the product space by two disjoint open subsets. We need to show that precisely one of the two
is empty. Since each $X_i$ is connected and hence non-empty, the product space is not empty, and hence
it is sufficient to show that at lest one of the two is empty.

Assume on the contrary that both $U_1$ and $U_2$ are non-empty.

Observe first that if so, then we could find $x_1 \in U_1$ and $x_2 \in U_2$
whose coordinates differed only a a finite subset of $I$. This is since by the nature of the
[[Tychonoff topology]] $\pi_i(U_1) = X_i$ and $\pi_i(U_2) = X_i$ for all but a finite number of $i \in iI$.

Next observe that we then could even find $x'_1 \in U_1$ that differed only in a single coordinate from $x_2$:
Because pick one coordinate in which $x_1$ differs from $x_2$ and change it to the corresponding coordinate of $x_2$.
Since $U_1$ and $U_2$ are a cover, the resulting point is either in $U_1$ or in $U_2$. If it is in $U_2$, then
$x_1$ already differed in only one coordinate from $x_2$ and we may take $x'_1 \coloneqq x_1$.
If instead the new point is in $U_1$, then rename it to $x_1$ and repeat the argument. By [[induction]]
this finally yields an $x'_1$ as claimed.

Therefore it is now sufficient to see that it leads to a contradiction to assume
that there are points $x_1 \in U_1$ and $x_2 \in U_2$
that differ in only the $i_0$th coordinate, for some $i_0 \in I$ then $x_1 = x_2$.

Observe that the inclusion

$$
  \iota \colon X_{i_0} \longrightarrow \underset{i \in I}{\prod} X_i
$$

which is the identity on the $i_0$th component and is otherwise constant on the $i$th component of
$x_1$ or equivalently of $x_2$ is a continuous function, by the nature of the Tychonoff topology.

Therefore also the restrictions $\iota^{-1}(U_1)$ and $\iota^{-1}(U_2)$ are open subsets.
Moreover they are still disjoint and cover $X_i$. Hence by the connectedness of $X_i$,
precisely one of them is empty. This means that the $i_0$-component of both $x_1$ and $x_2$
must be in the other subset of $X_i$, and hence that $x_1$ and $x_2$ must both be in $U_1$
or both in $U_2$, contrary to the assumption.

=--

+-- {: .num_example #ConnectedSubspacesOfRealLineAreTheIntervals}
###### Example
**(connected subspaces of the real line are the intervals)

Regard the [[real line]] with its [[Euclidean space|Euclidean]] [[metric topology]]. Then a
[[subspace]] $S \subset \mathbb{R}$ is connected (def. \ref{ConnectedSpace})
precisely if it is an [[interval]], hence precisely if

$$
  \underset{x,y \in S \subset \mathbb{R}}{\forall}
  \underset{ r \in \mathbb{R}  }{\forall}
  \left(
   \left(
      x \lt r \lt y
   \right)
     \Rightarrow
   \left(
     r \in S
   \right)
  \right)
  \,.
$$

In particular for $\{ I_i \subset \mathbb{R} \}_{i \in I}$ a set of [[disjoint subset|disjoint]] intervals,
then $I$ is the set of connected components of the union $\underset{i \in I}{\cup} I_i$.

=--

+-- {: .proof}
###### Proof

Suppose on the contrary that we have $x \lt r \lt y$ but $r \notin S$. Then by the
nature of the [[subspace topology]] there would be a decomposition of $S$ as a [[disjoint union]]
of [[disjoint subset|disjoint]] [[open subsets]]:

$$
  S
    =
  \left(
    S \cap (r,\infty)
  \right)
    \sqcup
  \left(
    S \cap (-\infty,r)
  \right)
  \,.
$$

But since $x \lt r$ and $r \lt y$ both these open subsets were [[inhabited set|non-empty]], thus contradicting the
assumption that $S$ is connected. This yields a [[proof by contradiction]].

=--




### Exotic examples

The [basic results](basic) above give a plethora of ways to construct connected spaces. More exotic examples are sometimes useful, especially for constructing counterexamples.

+-- {: .num_example}
###### Example
The following, due to [Bing](#Bing), is a countable connected [[Hausdorff space]]. Let $Q = \{(x, y) \in \mathbb{Q} \times \mathbb{Q}: y \geq 0\}$, topologized by defining a basis of neighborhoods $N_{\epsilon, a, b}$ for each point $(a, b) \in Q$ and $\epsilon \gt 0$:

$$N_{a, b} \coloneqq \{(a, b)\} \cup \{(s, 0) \in Q: {|a + b/\theta - s|} \lt \epsilon\} \cup \{(s, 0) \in Q: {|a - b/\theta - s|} \lt \epsilon\}$$

where $\theta \lt 0$ is some chosen fixed irrational number. It is easy to see this space is Hausdorff (using the fact that $\theta$ is irrational). However, the _closure_ of $N_{\epsilon, a, b}$ consists of points $(x, y)$ of $Q \times Q$ with either $(x-a) - \epsilon \leq (y-b)/\theta \leq (x-a) + \epsilon$ or $(x-a) - \epsilon \leq -(y-b)/\theta \leq (x-a) + \epsilon$, in other words, the union of two infinitely long strips of width $2\epsilon$ and slopes $\theta$, $-\theta$. Clearly any two such closures intersect, and therefore the space is connected.
=--

+-- {: .num_example}
###### Example 
This example is due to [Golomb](#Golomb). Topologize the set of natural numbers $\mathbb{N}$ by taking a basis to consist of sets $A_{a,b} \coloneqq \{a k + b | k = 1,2, \ldots\}$, where $a, b \in \mathbb{N}$ are relatively prime. The space is Hausdorff, but the intersection of the closures of two non-empty open sets is never empty, so this space is connected.
=--



## Properties 

+-- {: .num_example #LocallyConstantFunctionsOnConnectedSpaces}
###### Example
**([[locally constant function]] on [[connected topological spaces]] are [[constant functions]])**

If $X$ is a connected topological space and $f \colon X \to Y$ is a [[locally constant function|locally constant]] [[continuous function]], then $f$ is in fact a [[constant function]].

=--

+-- {: .proof}
###### Proof

By definition of locally constant functions, every point $x \in X$ has an [[open neighborhood]] $U_x$ such that the restriction $f\vert_{U_x}$ is a constant function. The [[unions]] of these neighborhoods for a fixed constant value hence are disjoint open subsets that constitute a cover of $X$. By connectedness this cover must consist of a single non-empty element. But by construction this means that $f$ is constant.

=--


## Path-connectedness

An important variation on the theme of connectedness is path-connectedness.

+-- {: .num_defn #TopologicalSpacePath}
###### Definition
**(continuous path in a topological space)**

Let $(X,\tau)$ be a [[topological space]], Then a _continuous path_ (or just _path_, for short) in $(X,\tau)$ is a [[continuous function]] of the form

$$
  \gamma
   \;\colon\;
  [0,1]
    \longrightarrow
  (X,\tau)
$$

where the domain is the [[closed interval]] equipped with its [[Euclidean space|Euclidean]] [[subspace topology]].

One says that the path connects the point $\gamma(0) \in X$ with the point $\gamma(1) \in X$.

For $x \in X$ a fixed point, then the subset

$$
  PConn_x(X)
   \;\coloneqq\;
  \left\{
     y \in X
     \;\vert\;
    \underset{\text{path}\, \gamma}{\exists}
    \left(
      \left(
        \gamma(0) = x
      \right)
      \phantom{}
      \text{and}
      \phantom{A}
      \left(
        \gamma(1) = y
      \right)
    \right)
  \right\}
$$

is called the _path-connected component_ of $x$.

The set of path connected components of $X$ is denoted

$$
  \pi_0(X)
  \,.
$$

=--

The set $\pi_0(X)$ of path components (the 0th "[[homotopy group]]") is thus the [[coequalizer]] in

$$ 
  \hom([0, 1], X) 
    \underoverset
    {ev_1}
    {ev_0}
    {\rightrightarrows}
  \hom(1, X) \to \pi_0(X) .
$$

Observe that this is a [[reflexive coequalizer]], as witnessed by the mutual right inverse $\hom(!, X): \hom(1, X) \to \hom([0, 1], X)$.

(We can even topologize $\pi_0(X)$ by taking the coequalizer in $Top$ of

$$X^{[0, 1]} \stackrel{\overset{ev_0}{\to}}{\underset{ev_1}{\to}} X,$$

taking advantage of the fact that the locally compact Hausdorff space $[0, 1]$ is [exponentiable](http://ncatlab.org/nlab/show/exponential+law+for+spaces). The resulting quotient space will be [[discrete space|discrete]] if $X$ is [[locally path-connected space|locally path-connected]].)

We say $X$ is **path-connected** if it has exactly one path component.

It follows easily from the basic results [above](basic) that:

+-- {: .num_lemma #ConnectedPathConnectedSpace}
###### Lemma

A path connected space $X$ is connected.

=--

+-- {: .proof}
###### Proof

Assume it were not, then it would be covered by two disjoint inhabited open subsets $U_1, U_2 \subset X$. But by path connectedness there were a continuous path $\gamma \colon [0,1] \to X$ from a point in one of the open subsets to a point in the other. The continuity would imply that $\gamma^{-1}(U_1), \gamma^{-1}(U_2) \subset [0,1]$ were a disjoint open cover of the interval. This would be in contradiction to the fact that intervals are connected. Hence we have a [[proof by contradiction]].

=--


However, it need not be closed (and therefore need not be the connected component of $x$); see the following example. The path components and connected components do coincide if $X$ is [[locally path-connected space|locally path-connected]].

+-- {: .num_example #sine}
###### Example
The **topologist's sine curve**
$$ \{ (x, y) \in \mathbb{R}^2 \;:\; (0 \lt x \leq 1 \;\wedge\; y = sin(1/x)) \;\vee\; (0 = x \;\wedge\; -1 \leq y \leq 1) \} $$
provides a classic example where the path component of a point need not be closed. (Specifically, consider a point on the locus of $y = \sin(1/x)$.)
=--

The basic categorical Results \ref{ContinuousImagesOfConnectedSpacesAreConnected}, \ref{2}, and \ref{ProductSpaceOfConnectedSpacesIsConnected} above carry over upon replacing "connected" by "path-connected". (As of course does
example \ref{ConnectedSubspacesOfRealLineAreTheIntervals}, trivially.)

Finally, as a contrast to a path-connected space, a **totally path-disconnected** space is a space such that its set of path components is equal to the underlying set of the space. Equivalently, that there are no non-constant paths. This by far does not mean that the space is discrete!

### Arc-connectedness

A refinement of the notion of path-connected space is that of arc-connected (or arcwise-connected) space:

+-- {: .num_defn}
###### Definition
A space $X$ is **arc-connected** if for any two distinct $x, y \in X$ there exists an _injective_ continuous map $\alpha: I \to X$ such that $\alpha(0) = x$ and $\alpha(1) = y$.
=--

Arc-connected spaces are of course path-connected, but there are trivial examples (using an [[indiscrete topology]]) that the converse fails to hold. A rather nontrivial theorem is the following:

+-- {: .num_theorem #arc}
###### Theorem
A path-connected [[Hausdorff space]] $X$ is arc-connected.
=--

This immediately generalizes to the statement that in a Hausdorff space $X$, any two points that can be connected by a path $\alpha: I \to X$ can be connected by an arc: just apply the theorem to the image $\alpha(I)$.

For a proof of this theorem, see [Willard](#Willard), theorem 31.2. More precisely, that result states that a _Peano space_, i.e., a [[compact space|compact]], [[connected topological space|connected]], [[locally connected topological space|locally connected]], and [[metrizable space]], is arc-connected if it is path-connected. It then suffices to observe that the continuous image $\alpha(I) \subseteq X $ of a path is in fact a Peano space, so that the path $\alpha: I \to \alpha(I)$ can be replaced by an arc.

+-- {: .num_lemma}
###### Lemma
If $X$ is Hausdorff and there is a continuous surjection $f: I \to X$, then $X$ is a [[Peano space]].
=--

+-- {: .proof}
###### Proof
Obviously $X$ is compact (Hausdorff) and connected. $X$ is a [[quotient space]] of $I$, since $f$ is a closed surjection (using compactness of $I$ and Hausdorffness of $X$), and therefore $X$ is locally connected by [this lemma](https://ncatlab.org/nlab/show/locally+connected+topological+space#quot). Being compact Hausdorff, $X$ is [[separation axiom|regular]], so to show metrizability it suffices by the [[Urysohn metrization theorem]] to show $X$ is second-countable.

Let $\mathcal{B}$ be a countable base for $I$ and let $\mathcal{C}$ be the collection consisting of finite unions of elements of $\mathcal{B}$. We claim $\forall_f(\mathcal{C}) \coloneqq \{\forall_f(C) = \neg f(\neg C): C \in \mathcal{C}\}$ is an (evidently countable) base for $X$. Indeed, suppose $U \subseteq X$ is open and $p \in U$; then $f^{-1}(p)$ is compact, so there exist finitely many $B_1, \ldots, B_n \in \mathcal{B}$ with

$$f^{-1}(p) \subseteq B_1 \cup \ldots \cup B_n \subseteq f^{-1}(U).$$

Put $C = B_1 \cup \ldots \cup B_n$. The first inclusion is equivalent to $p \in \forall_f(C)$ by the adjunction $f^{-1} \dashv \forall_f$. The second inclusion implies $\forall_f(C) \subseteq \forall_f f^{-1}(U) = U$, where the equality $\forall_f f^{-1} = id$, equivalent to $\exists_f f^{-1} = id$, follows from surjectivity of $f$. Thus we have shown $\forall_f(\mathcal{C})$ is a base.
=--

The converse of this lemma is the celebrated [[Hahn-Mazurkiewicz theorem]]:

+-- {: .num_theorem}
###### Theorem
Let $X$ be a nonempty Hausdorff space. Then there exists a continuous surjection $\alpha: [0, 1] \to X$ if $X$ is a Peano space. In particular, a nonempty Peano space is path-connected.
=--

(The terminology "Peano space" is given in recognition of Peano's discovery of space-filling curves, as for example the unit square.)

### Path-components functor

As above, let $\pi_0 \colon Top \to Set$ be the functor which assigns to each space $X$ its set of path components $\pi_0(X)$.

+-- {: .un_prop}
###### Proposition
The functor $\pi_0 \colon Top \to Set$ preserves arbitrary products.
=--

+-- {: .proof}
###### Proof
Let $X_i$ be a family of spaces; we must show that the comparison map

$$\pi_0(\prod_i X_i) \to \prod_i \pi_0(X_i)$$

is invertible. Injectivity: suppose $(x_i), (y_i) \in \prod_i X_i$ are tuples that map to the same tuple of path-components $(c_i)$; we must show that $(x_i)$ and $(y_i)$ belong to the same path component. For each $i$, both $x_i$ and $y_i$ belong to $c_i$, so we may choose a path $\alpha_i: I \to X_i$ connecting $x_i$ to $y_i$. Then $\langle \alpha_i \rangle \colon I \to \prod_i X_i$ connects $(x_i)$ to $(y_i)$. (Note this uses the [[axiom of choice]].) Surjectivity: for any tuple $(c_i) \in \prod_i \pi_0(X_i)$, the component $c_i$ is nonempty for each $i$, so we may choose an element $x_i$ therein. Then $(x_i)$ maps to $(c_i)$. Again this uses the axiom of choice.
=--

An elegant proof of the previous proposition but for preservation of _finite_ products is as follows: both $\hom(I, -)$ and $\hom(1, -)$ preserve products, and a [[reflexive coequalizer]] of product-preserving functors $C \to Set$, being a [[sifted colimit]], is also product-preserving.

+-- {: .un_prop}
###### Proposition
The functor $\pi_0 \colon Top \to Set$ preserves arbitrary coproducts.
=--

+-- {: .proof}
###### Proof
The functor $\hom(I, -) \colon Top \to Set$ preserves coproducts since $I$ is connected, and similarly for $\hom(1, -)$. The coequalizer of a pair of natural transformations between coproduct-preserving functors is also a coproduct-preserving functor.
=--

### Pseudo-arcs

Point-set topology is filled with counterexamples. An unusual type of example is that of pseudo-arc:

+-- {: .num_defn}
###### Definition
A _pseudo-arc_ is a [[continuum|metric continuum]] with more than one point such that every subcontinuum (a subspace that is a continuum) cannot be expressed as a union of two proper subcontinua.
=--

A pseudo-arc $X$ is necessarily totally path-disconnected: two distinct points $x, y$ of $X$ cannot be connected by a path in $X$. Indeed, the image of such a# path would be a path-connected Hausdorff space, hence arc-connected by Theorem \ref{arc}. Letting $\alpha: [0, 1] \to X$ be an arc from $x$ to $y$, we have that the continuum $\alpha([0, 1])$ is a union of proper subcontinua $\alpha([0, 1/2])$ and $\alpha([1/2, 1])$, a contradiction. Thus, a pseudo-arc is an example of a compact connected metrizable space that is totally path-disconnected.

Remarkably, all pseudo-arcs are homeomorphic, and a pseudo-arc is a [[homogeneous space]]. Perhaps also remarkable is the fact that the collection of pseudo-arcs in the [[Hilbert cube]] $Q$ (or in any Euclidean space) is a dense $G_\delta$ set (see [[G-delta set]]) in the [[Polish space]] of all nonempty compact subsets of $Q$ under the [[Hausdorff metric]]; see [Bing2](#Bing2), theorem 2.

A typical way in which pseudo-arcs arise is through [[inverse limits]] of [[dynamical systems]]. One of the original constructions is due to Henderson:

+-- {: .num_theorem}
###### Theorem
There is a $C^\infty$ function $f: I \to I$ such that the limit of the diagram

$$\ldots \stackrel{f}{\to} I \stackrel{f}{\to} I \stackrel{f}{\to} I$$

is a pseudo-arc.
=--

Roughly speaking, Henderson's $f$ is a small "notched" perturbation of the squaring function $[0, 1] \to [0, 1]: x \mapsto x^2$, as illustrated on page 38 (of 58) [here](http://www.akasimikrasna.sk/uploads/1/4/1/0/14106449/spitalsky2014.pdf).

## Properties
 {#Properties}


+-- {: .num_prop}
###### Corollary
**([[intermediate value theorem]])**

Regard the [[real numbers]] $\mathbb{R}$ with their [[Euclidean space|Euclidean]] [[metric topology]],
and consider a [[closed interval]] $[a,b] \subset \mathbb{R}$ equipped with its [[subspace topology]].

Then a [[continuous function]]

$$
  f \colon [a,b] \longrightarrow \mathbb{R}
$$

takes every value in between $f(a)$ and f(b).

=--


+-- {: .proof}
###### Proof

By example \ref{ConnectedSubspacesOfRealLineAreTheIntervals} the interval $[a,b]$ is connected.
By example \ref{ContinuousImagesOfConnectedSpacesAreConnected} also its image $f([a,b]) \subset \mathbb{R}$
is connected. By example \ref{ConnectedSubspacesOfRealLineAreTheIntervals} that image is hence
itself an interval. This implies the claim.

=--

+-- {: .num_prop #ClosureOfConnectedSubspaceIsConnected}
###### Proposition
**([[topological closure]] of connected subspace is connected)**

Let $(X,\tau)$ be a [[topological space]] and let $S \subset X$ be a [[subset]] which, as a [[subspace]], is connected. Then also the [[topological closure]] $Cl(S) \subset X$ is connected


=--

+-- {: .proof}
###### Proof

Suppose that $Cl(S) = A \sqcup B$ with $A,B \subset X$ [[disjoint subsets|disjoint]] [[open subsets]]. We need to show that one of the two is empty.

But also the intersections $A \cap S\,,B \cap S \subset S$ are disjoint subsets, open as subsets of the subspace $S$ with $S = (A \cap S) \sqcup (B \cap S)$. Hence by the connectedness of $S$, one of $A \cap S$ or $B \cap S$ is empty. Assume $B \cap S$ is empty, otherwise rename. Hence $A \cap S = S$, or equivalently: $S \subset A$. By disjointness of $A$ and $B$ this means that  $S \subset Cl(S) \setminus B$. But since $B$ is open, $Cl(S) \setminus B$ is still closed, so that

$$
  (S \subset Cl(S) \setminus B)
  \Rightarrow
  (Cl(S) \subset Cl(S) \setminus B)
  \,.
$$

This means that $B = \emptyset$, and hence that $Cl(S)$ is connected.

=--

+-- {: .num_prop #ConnectedComponentsAreClosed}
###### Proposition
**(connected components are closed)**

Let $(X,\tau)$ be a [[topological space]]. Then its connected components (def. \ref{ComponentsConnected}) are [[closed subsets]].


=--

+-- {: .proof}
###### Proof

By definition, the connected components are [[maximal elements]] in the set of connected subspaces [[preorder|pre-ordered]] by inclusion. By prop. \ref{ClosureOfConnectedSubspaceIsConnected} this means that they must contain their closures, hence they must equal their closures.

=--

+-- {: .num_remark}
###### Remark

Prop. \ref{ConnectedComponentsAreClosed} implies that when a space has a [[finite set]] of connected components, then they are not just closed but also open, hence [[clopen subsets]] (because then each is the [[complement]] of a finite union of closed subspaces).

For a non-finite set of connected components this remains true if the space is [[locally connected topological space|locally connected]]. See [this prop.](locally+connected+topological+space#AlternativeCharacterizationsOfLocalConnectivity)

=--



## Related concepts

* [[locally connected topological space]]

* [[connected topos]], [[locally connected topos]]

* [[cohesive topos]]

* [[contractible topological space]]

* [[almost connected topological group]]

* A space in which the only connected subspaces are the singletons and the empty set is called [[totally disconnected space]].

* The connected subsets of a space form a [[connectology]].

\linebreak

* [[simply connected topological space]]

* [[simple topological space]]

* [[nilpotent topological space]]

## References

Examples of countable connected Hausdorff spaces were give in

* {#Bing} R.H. Bing, A connected countable Hausdorff space, Proc. Amer. Math. Soc. 4 (1953), 474.


* {#Golomb} Solomon W. Golomb, _A Connected Topology for the Integers_, Amer. Math. Monthly, Vol. 66 No. 8 (Oct. 1959), 663-665.


Material on arc-connected spaces and the Hahn-Mazurkiewicz theorem can be found in Chapter 31 of

* {#Willard} Stephen Willard, _General Topology_, Addison-Wesley 1970. ([online](http://www.scribd.com/doc/132023793/44283132-General-Topology-Stephen-Willard#scribd))


Material on pseudo-arcs can be found in

* {#Bing2} R.H. Bing, _Concerning hereditarily indecomposable continua_, Pacific J. Math. Volume 1, Number 1 (1951), 43-51. ([Project Euclid](http://projecteuclid.org/euclid.pjm/1102613150))



[[!redirects connected space]]
[[!redirects connected spaces]]
[[!redirects connected topological space]]
[[!redirects connected topological spaces]]


[[!redirects path-connected space]]
[[!redirects path-connected space]]
[[!redirects path-connected spaces]]

[[!redirects path connected space]]
[[!redirects path connected topological space]]
[[!redirects path connected spaces]]


[[!redirects pathwise connected space]]
[[!redirects pathwise connected spaces]]
[[!redirects pathwise connected topological space]]
[[!redirects pathwise connected topological spaces]]
[[!redirects path-connected topological space]]
[[!redirects path-connected topological spaces]]
[[!redirects pathwise connected]]


[[!redirects connected component]]
[[!redirects connected components]]

[[!redirects path component]]
[[!redirects path components]]

[[!redirects path-component]]
[[!redirects path-components]]



