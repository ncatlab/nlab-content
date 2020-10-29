+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _differentiable manifold_ is a [[topological space]] which is _locally_ [[homeomorphism|homeomorphic]] to a [[Euclidean space]] (a [[topological manifold]]) and such that the [[gluing functions]] which relate these Euclidean [[local charts]] to each other are [[differentiable functions]], for a fixed degree of differentiability. If one considers arbitrary differentiablity then one speaks of _[[smooth manifolds]]_ and if one demands [[analytic function|analytic]] gluing functions then one speaks of _[[analytic manifolds]]_. For a general discussion see at _[[manifold]]_.

Accordingly, a differentiable manifold is a space to which the tools of ([[infinitesimal analysis|infinitesimal]]) [[analysis]] may be applied _locally_.
Notably we may ask whether a [[continuous function]] between differentiable manifolds is [[differentiation|differentiable]]
by computing its [[derivatives]] pointwise in any of the Euclidean [[coordinate charts]].

In particular one may consider smooth functions from the [[real line]] into any smooth manifold $X$, "smooth curves" in $X$. The [[equivalence classes]] of these that have the same first [[derivative]] at a given point capture the idea of "infinitsimal smooth paths" through that point in the manifold, called its _[[tangent vectors]]_. All the tangent vectors at one point $x \in X$ constitute the [[tangent space]] $T_x X$, and the collection of all these tangent spaces yields another differentiable manifold, called the _[[tangent bundle]]_ $T X$. This happens to be a [[vector bundle]] which is [[associated bundle|associated]] to a [[principal bundle]], called the _[[frame bundle]]_ $Fr(X)$.

By equipping the [[tangent bundle]] or [[frame bundle]] of a differentiable manifold with [[extra properties]] or [[extra structure]] one encodes _[[geometry]]_ on the manifold. For example equipping them with [[orthogonal structure]] encodes [[Riemannian geometry]] on manifolds. More generally one may consider any _[[G-structure]]_ on the frame bundle and thereby equip the manifold with the corresponding _[[Cartan geometry]]_, for instance _[[complex geometry]]_, _[[conformal geometry]]_ etc.

This way differential and smooth manifolds are the basis for [[differential geometry]]. They are the analogs in differential geometry of what [[schemes]] are in [[algebraic geometry]]. In fact both of these concepts are unified within _[[synthetic differential geometry]]_.

If one relaxes the condition on differentiable manifold from it being locally isomorphic to a Euclidean space to it just admitting local smooth maps from a Euclidean space, then one obtains the more general concept of [[diffeological spaces]] or even [[smooth sets]], see at _[[generalized smooth space]]_ for more on this. If one generalizes here [[differentiable functions]] to [[simplicial algebra|simplicial]] differentiable functions one obtains concepts of _[[derived smooth manifold]]_.

The generalization of differentiable manifolds to [[higher differential geometry]] are [[orbifolds]] and more generally [[differentiable stacks]]. If one combines this with the generalization to [[smooth sets]] then one obtains the concept of [[smooth stacks]] and eventually [[smooth infinity-stacks]].


## Definition

For convenience, we first recall the basic definition of

* [Topological manifolds](#TopologicalManifolds)

and of

* [Differentiable functions between Euclidean spaces](#DifferentiableFunctionsBetweenCartesianSpaces)

and then turn to the actual definition of

* [Differentiable manifolds](#DifferentiableManifolds).


### Topological manifolds
 {#TopologicalManifolds}

For convenience, we first recall here some background on [[topological manifolds]]:


+-- {: .num_defn #TopologicalManifold}
###### Definition
**(topological manifold)**

A _topological manifold is a [[topological space]] which is

1. [[locally Euclidean topological space|locally Euclidean]],

1. [[paracompact Hausdorff topological space|paracompact Hausdorff]].

If the local [[Euclidean spaces|Euclidean]] neighbourhoods $\mathbb{R}^n \overset{\simeq}{\to} U \subset X$ are all of [[dimension]] $n$
for a fixed $n \in \mathbb{N}$, then the topological manifold is said to be a _$n$-dimensional manifold_ or _$n$-fold_. This is usually assumed to be the case.


=--

+-- {: .num_remark}
###### Remark
**(varying terminology)**

Often a topological manifold (def. \ref{TopologicalManifold}) is required to be [[sigma-compact]]. But by [this prop.](topological#manifold#RegularityConditionsForTopologicalManifoldsComparison) this is not an extra condition as long as there is a [[countable set]] of [[connected components]].
Moreover, manifolds with uncountably many connected components are rarely considered in practice.

=--


+-- {: .num_defn #Charts}
###### Definition
**([[local chart]], [[atlas]] and [[gluing function]])

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


### Differentiable functions between Cartesian spaces
 {#DifferentiableFunctionsBetweenCartesianSpaces}

For convenience we recall the definition of [[differentiable functions]]
between [[Euclidean spaces]].

+-- {: .num_defn #DifferentiableFunctionBetweenCartesianSpaces}
###### Definition
**([[differentiable functions]] between [[Euclidean spaces]])**

Let $n \in \mathbb{N}$ and let $U \subset \mathbb{R}^n$ be an [[open subset]].

Then a [[function]] $f \;\colon\; U \longrightarrow \mathbb{R}$ is called  **differentiable** at $x\in U$
if there exists a [[linear map]] $d f_x : \mathbb{R}^n \to \mathbb{R}$ such that the following [[limit of a sequence|limit]]
exists as $h$ approaches zero "from all directions at once":

$$
  \lim_{h\to 0} \frac{f(x+h)-f(x) - d f_x(h)}{\Vert h\Vert} = 0.
$$

This means that for all $\epsilon \in (0,\infty)$ there exists an [[open subset]] $V\subseteq U$ containing $x$ such that whenever $x+h\in V$ we have $\frac{f(x+h)-f(x) - d f_x(h)}{\Vert h\Vert} \lt \epsilon$.

We say that $f$ is _differentiable on_ a [[subset]] $I$ of $U$ if $f$ is differentiable at every $x\in I$, and _differentiable_ if $f$ is differentiable on all of $U$. We say that $f$ is *continuously differentiable* if it is differentiable and  $d f$ is a [[continuous function]].

The map $d f_x$ is called the **derivative** or **differential of $f$ at $x$**.

More generally, let $n_1, n_2 \in \mathbb{N}$ and let $U\subseteq \mathbb{R}^{n_1}$ be an [[open subset]].

Then a [[function]] $f \;\colon\; U \longrightarrow \mathbb{R}^{n_2}$ is _differentiable_  if for all $i \in \{1, \cdots, n_2\}$ the component function

$$
  f_i \;\colon\; U \overset{f}{\longrightarrow} \mathbb{R}^{n_2} \overset{pr_u}{\longrightarrow}  \mathbb{R}
$$

is differentiable in the previous sense

In this case, the derivatives $d f_i \colon \mathbb{R}^n \to \mathbb{R}$ of the $f_i$ assemble into a linear map  of the form

$$
  d f_x \;\colon\; \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}
  \,.
$$

If the derivative exists at each $x \in U$, then it defines itself a function

$$
  d f \;\colon\; U \longrightarrow Hom_{\mathbb{R}}(\mathbb{R}^{n_1} , \mathbb{R}^{n_2}) \simeq \mathbb{R}^{n_1 \cdot n_2}
$$

to the space of [[linear maps]] from $\mathbb{R}^{n_1}$ to $\mathbb{R}^{n_2}$, which is canonically itself a [[Euclidean space]]. We say that $f$ is _twice continuously differentiable_ if $d f$ is continuously differentiable.

Generally then, for $k \in \mathbb{N}$ the function $f$ is called _$k$-fold continuously differentiable_ or _of class $C^k$_ if the $k$-fold differential $d^k f$ exists and is a continuous function.

Finally, if $f$ is $k$-fold continuously differentiable for all $k \in \mathbb{N}$ then it is called a _[[smooth function]]_
or _of class $C^\infty$_.

=--

Of the various properties satisfied by [[differentiation]], the following plays a special role in the theory of
differentiable manifolds (notably in the discussion of their [[tangent bundles]]):

+-- {: .num_prop #ChainRuleOnEuclideanSpace}
###### Proposition
**([[chain rule]] for [[differentiable functions]] between [[Euclidean spaces]])**

Let $n_1, n_2, n_3 \in \mathbb{N}$ and let

$$
  \mathbb{R}^{n_1}
    \overset{f}{\longrightarrow}
  \mathbb{R}^{n_2}
    \overset{g}{\longrightarrow}
  \mathbb{R}^{n_3}
$$

be two [[differentiable functions]] (def. \ref{DifferentiableFunctionBetweenCartesianSpaces}). Then the
[[derivative]] of their [[composition|composite]] is the composite of their derivatives:

$$
  d(g \circ f) = (d g) \circ (d f)
$$

hence for all $x \in \mathbb{R}^{n_1}$ we have

$$
  d(g \circ f)_x = d g_{f(x)} \circ d f_x
  \,.
$$

=--




### Differentiable manifolds
 {#DifferentiableManifolds}


+-- {: .num_defn #DifferentiableManifold}
###### Definition
**([[differentiable manifold]] and [[smooth manifold]])**

For $p \in \mathbb{N} \cup \{\infty\}$ then a $p$-fold _[[differentiable manifold]]_ or _$C^p$-manifold_ for short is

1. a [[topological manifold]] $X$ (def. \ref{TopologicalManifold});

1. an [[atlas]] $\{\mathbb{R}^n \overset{\phi_i}{\to} X\}$ (def. \ref{Charts}) all whose [[gluing functions]]  are $p$ times continuously [[differentiable function|differentiable]].

A $p$-fold [[differentiable function]] between $p$-fold differentiable manifolds

$$
  \left(X,\, \{\mathbb{R}^{n} \overset{\phi_i}{\to} U_i \subset X\}_{i \in I} \right)
   \overset{\phantom{AA}f\phantom{AA}}{\longrightarrow}
  \left(Y,\, \{\mathbb{R}^{n'} \overset{\psi_j}{\to} V_j \subset Y\}_{j \in J} \right)
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

(Notice that this in in general  a non-trivial condition even if $X = Y$ and $f$ is the identity function. In this case the above exhibits a passage to a different, but equivalent, differentiable atlas.)

If a manifold is $C^p$ differentiable for all $p$, then it is called a _[[smooth manifold]]_.
Accordingly a continuous function between differentiable manifolds which is $p$-fold differentiable
for all $p$ is called a _[[smooth function]]_,



=--

+-- {: .num_remark #CategoryDiff}
###### Remark
**([[category]] [[Diff]] of [[differentiable manifolds]])**

In analogy to remark \ref{TopCategory} there is a [[category]] called [[Diff]]${}_p$ (or similar) whose [[objects]] are $C^p$-[[differentiable manifolds]] and whose [[morphisms]] are $C^p$-[[differentiable functions]], for given $p \in \mathbb{N} \cup \{\infty\}$.

=--

The analog of the concept of [[homeomorphism]] (def. \ref{Homeomorphism}) is now this:

+-- {: .num_defn #Diffeomorphism}
###### Definition
**([[diffeomorphism]])**

Given [[smooth manifolds]] $X$ and $Y$ (def. \ref{DifferentiableManifold}), then a [[smooth function]]

$$
  f \;\colon\; X \longrightarrow Y
$$

is called a _[[diffeomorphism]]_, if there is an [[inverse function]]

$$
  X \longleftarrow Y \;\colon\; g
$$

which is also a [[smooth function]] (hence if $f$ is an [[isomorphism]] in the [[category]] [[Diff]]${}_\infty$
from remark \ref{CategoryDiff}).

=--

Here it is important to note that while being a [[topological manifold]] is just a [[property]]
of a [[topological space]], a [[differentiable manifold]] carries [[extra structure]] encoded in the
[[atlas]]:

+-- {: .num_defn #SmoothStructure}
###### Definition
**([[smooth structure]])**

Let $X$ be a [[topological manifold]] (def. \ref{TopologicalManifold}) and let

$$
  \left(
    \mathbb{R}^n \underoverset{\simeq}{\phi_i}{\longrightarrow} U_i \subset X
  \right)_{i \in I}
  \phantom{AAA}
   \text{and}
  \phantom{AAA}
  \left(
    \mathbb{R}^{n} \underoverset{\simeq}{\psi_j}{\longrightarrow} V_j \subset X
  \right)_{j \in J}
$$

be two [[atlases]] (def. \ref{Charts}), both making $X$ into a [[smooth manifold]] (def. \ref{DifferentiableManifold}).

Then there is a [[diffeomorphism]] (def. \ref{Diffeomorphism}) of the form

$$
  f
  \;\colon\;
  \left(
    X
      \;,\;
    \left(
      \mathbb{R}^n \underoverset{\simeq}{\phi_i}{\longrightarrow} U_i \subset X
    \right)_{i \in I}
  \right)
    \overset{\simeq}{\longrightarrow}
  \left(
    X\;,\;
    \left(
      \mathbb{R}^{n} \underoverset{\simeq}{\psi_j}{\longrightarrow} V_j \subset X
    \right)_{j \in J}
  \right)
$$

precisely if the [[identity function]] on the underlying set of $X$ constitutes such a diffeomorphism.
(Because if $f$ is a diffeomorphism, then also $f^{-1}\circ f = id_X$ is a diffeomorphism.)

That the identity function is a diffeomorphism between $X$ equipped with these two atlases means,
by definition \ref{DifferentiableManifold}, that

$$
  \underset{{i \in I} \atop {j \in J}}{\forall}
  \left(
    \phi_i^{-1}(V_j) \overset{\phi_i}{\longrightarrow} V_j \overset{\psi_j^{-1}}{\longrightarrow} \mathbb{R}^n
    \phantom{AA}
    \text{is smooth}
  \right)
  \,.
$$

Notice that the functions on the right may equivalently be written as

$$
  \mathbb{R}^n \supset
   \,
   \phi_i^{-1}(U_i \cap U_j)
     \overset{\phi_i}{\longrightarrow}
    U_i \cap V_j \overset{\psi_j^{-1}}{\longrightarrow} \psi_j^{-1}(U_i \cap V_j) \; \subset \mathbb{R}^n
$$

showing their analogy to the glueing functions within a single atlas spring.

Hence diffeomorphism induces an [[equivalence relation]] on the set of
smooth atlases that exist on a given [[topological manifold]] $X$. An [[equivalence class]]
with respect to this equivalence relation is called a _[[smooth structure]]_ on $X$.

=--

## As Étale Spaces

Differentiable manifolds can be viewed as akin to [[étale spaces]], very much in alignment with the language of [[algebraic geometry]]. For [[smooth manifolds]] and [[complex manifolds]] the requisite atlas conditions can be stated in terms of a particular structure sheaf.  More precisely, this definition yields an [[equivalence of categories]] between the category of smooth manifolds as in \ref{Charts} and the category of locally ringed spaces modeled on domains of $\mathbf{R}^n$ with a sheaf of germs of smooth functions. The same goes for topological and complex manifolds, where the local models are domains with sheafs of germs of continuous and holomorphic functions respectively. Here we illustrate the differentiable case. For any $A \subset {\mathbf R}^n$, we write $\mathcal{D}_A$ for the sheaf of germs of functions $f \in C^{\infty}(A, \mathbf{R} )$. That is, $\mathcal{D}_A$ is the functor $ \mathcal{D}_A :  \text{Open} (A) \rightarrow {\mathbf Ring}^{\text{op}}$ s.t. $ \mathcal{D}_A  : B \mapsto C^{\infty}(B, {\mathbf R})$ and $ \mathcal{D}_A  : B \subset B' \mapsto  C^{\infty}(B, {\mathbf R}) \hookrightarrow C^{\infty}(B', {\mathbf R})$. This turns $ (A, \mathcal{D}_A)$ into a ringed space, and any ringed space modeled on one of this kind can be regarded as a differentiable (by which is always meant "real") manifold. More precisely, given a ringed space $(X, D_X)$, there must an open set $A \subset {\mathbf R}^n$ and local isomorphism $(f, f_*)$  where $f: A \rightarrow X$ is a continuous function with sheaf pushfoward $f_* : (\mathcal{O}_A \rightarrow \mathcal{O}_X )$. The following property, which holds at the continuous level, is essential.

+-- {: .num_lemma} 
###### Lemma

Let $F : X \rightarrow Y$ be a continuous surjection. Let $P$ be a sheaf of $R$-valued functions on $X$ (here we let $R$ be any ring). Consider an open $U \subset Y$ and define $Q(U) \subset R^U$ to be $\{ f : U \rightarrow R  | F^{*} f = f \circ F|_{f^{-1}(U)} \in P(F^{-1}(U)) \}$ i.e. those $f$ s.t. the pullback of each $f$ by $F$ belongs to $P(F^{-1}(U))$. Then $Q$ is a sheaf on $Y$.
=-- 

We can phrase the example of $\mathbf{R}P^n$ in this language.

+-- {: .num_example #DifferentiableManifoldCartesianSpace}
###### Example
**([[real projective space]] as a [[smooth manifold]] in this [[étale map]] sense)

We need only show that the functions $f : V \subset {\mathbf R}P^n \rightarrow {\mathbf R}^n$ which are smooth when composed with the canonical projection $\pi : {\mathbf R}^{n+1}/\{ 0 \} \rightarrow {\mathbf R }P^n$ form a sheaf on ${\mathbf R}^n$. Denote these $\mathcal{O}_{{\mathbf R}P^n}$. Certainly they form a presheaf, and checking the pullback as in the lemma confirms that they are a sheaf. So far this only confirms that ${\mathbf R}P^n$ is a real topological manifold. To establish its differentiable structure we take for each chart $(U, \varphi)$ of ${\mathbf R}P^n$ the ringed space $(\varphi(U), \varphi_* \mathcal{O}_{{\mathbf R}P^n}|_U )$ obtained from restriction and then pushforward, a local isomorphism of locally ringed spaces by construction. Hence $({\mathbf R}P^n, \mathcal{O}_{{\mathbf R}P^n})$ is a smooth manifold.

=--

## Examples
 {#Examples}

+-- {: .num_example #DifferentiableManifoldCartesianSpace}
###### Example
**([[Cartesian space]] as a [[smooth manifold]])

For $n \in \mathbb{N}$ then the [[Cartesian space]] $\mathbb{R}^n$ equipped with the [[atlas]] consisting of the single [[chart]] $\mathbb{R}^n \overset{id}{\to} \mathbb{R}^n$ is a [[smooth manifold]], in particularly a $p$-fold differentiable manifold for every $p \in \mathbb{N}$ according to def. \ref{DifferentiableManifold}.

Similarly the [[open disk]] $D^n$ becomes a [[smooth  manifold]] when equipped with the atlas whose single chart is the [[homeomorphism]] $\mathbb{R}^n \to D^n$.

This defines a [[smooth structure]] (def. \ref{SmoothStructure}) on $\mathbb{R}^n$ and $D^n$.
Strikingly, precisely for $n = 4$ there are _other_ smooth structures on $\mathbb{R}^4$,
hence called _[[exotic smooth structures]]_.

=--

+-- {: .num_example}
###### Example
**([[n-spheres]] as [[smooth manifolds]])**

For all $n \in \mathbb{N}$, the [[n-sphere]] $S^n$ becomes a smooth manfold, with [[atlas]] consisting of the two [[local charts]] that are given by the [[inverse functions]] of the [[stereographic projection]] from the two poles of the sphere onto the [[equator|equatorial]] hyperplane

$$
  \left\{
     \mathbb{R}^n
       \underoverset{\simeq}{\sigma^{-1}_i}{\longrightarrow}
     S^n
  \right\}_{i \in \{+,-\}}
  \,.
$$

By the formulas given in [this prop.](stereographic+projection#StandardStereographicProjection) the induced [[gluing function]] $\mathbb{R}^n \backslash \{0\} \to \mathbb{R}^n \backslash \{0\}$ is a [[rational function]], and hence a [[smooth function]].

Finally the $n$-sphere is a [[paracompact Hausdorff topological space]]. Ways to see this include:

1. $S^n \subset \mathbb{R}^{n+1}$ is a [[compact subspace]] by the [[Heine-Borel theorem]]. Compact spaces are evidently also paracompact. Moreover, [[Euclidean space]], like any [[metric space]], is Hausdorff, and [[subspaces]] of Hausdorff spaces are Hausdorff;

1. The $n$-sphere has an evident structure of a [[CW-complex]] and [[CW-complexes are paracompact Hausdorff spaces]].

=--

+-- {: .num_example}
###### Example
**([[real projective space]] and [[complex projective space]])**

For $n \in \mathbb{N}$

1. the [[real projective space]] $\mathbb{R}P^n$ has the structure of a [[smooth manifold]]
of [[dimension]] $n$;

1. the [[complex projective space]] $\mathbb{C}P^n$ has the structure of a [[smooth manifold]] of (real) [[dimension]] $2n$.

where in both cases the [[atlas]] is given by the standard open cover ([this def.](projective+space#TopologicalProjectiveSpaceStandardOpenCover)).

=--

By [this prop.](projective+space#SmoothManifoldRealComplexProjectiveSpace).

We now discuss some general mechanisms by which new differentiable manifolds arise from given ones:

+-- {: .num_example #ProductManifold}
###### Example
**(product manifold)**

Let $X$ any $Y$ be two differentiable manifolds with [[atlases]] $\{\mathbb{R}^n\underoverset{\simeq}{\phi_i}{\to} U_i \subset X\}$
and $\{\mathbb{R}^{n'}\underoverset{\simeq}{\psi_j}{\to} V_j \subset Y\}$. Then their [[product topological space]] $X \times Y$
becomes an differentiable manifold with respect to the atlas

$$
  \left\{
    \mathbb{R}^{n \cdot n'}
      \underoverset{\simeq}{\phi_i \times \psi_j}{\to}
    U_i \times V_j
      \subset
    X \times Y
  \right\}_{(i,j) \in I \times J}
$$

=--




+-- {: .num_example #OpenSubsetsOfDifferentiableManifoldsAreDifferentiableManifolds}
###### Example
**([[open subsets]] of differentiable manifolds are differentiable manifolds)**

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

+-- {: .num_example }
###### Example
**([[general linear group]])**

For $n \in \mathbb{N}$, the [[general  linear group]] $Gl(n,\mathbb{R})$
is a smooth manifold
(as an [[open subspace]] of [[Euclidean space]] $GL(n,\mathbb{R}) \subset Mat_{n \times n}(\mathbb{R}) \simeq \mathbb{R}^{(n^2)}$,
via example \ref{OpenSubsetsOfDifferentiableManifoldsAreDifferentiableManifolds} and example \ref{DifferentiableManifoldCartesianSpace}).

The group operations are [[smooth functions]] with respect to this smooth manifold structure, and thus $GL(n,\mathbb{R})$
is a [[Lie group]].

=--


## Related concepts

* [[smooth manifold]]

* [[diffeological space]], [[smooth set]]

* [[orbifold]]

* [[differentiable stack]], [[smooth stack]], [[smooth infinity-stack]]


## References

Textbook accounts include

* {#Kosinski93} [[Antoni Kosinski]], _Differential manifolds_, Academic Press 1993 ([pdf](http://www.maths.ed.ac.uk/~v1ranick/papers/kosinski.pdf))


* [[Theodore Frankel]], chapter 1 of _[[The Geometry of Physics - An Introduction]]_, Cambridge University Press (1997, 2004, 2012)

Lecture notes include

* Claudio Gorodski, _Notes on smooth manifolds_, 2013 ([pdf](https://www.ime.usp.br/~gorodski/teaching/mat5799-2013/ch1.pdf))

* {#Schlichtkrull08} [[Henrik Schlichtkrull]], _Differentiable manifolds_, 2008 ([pdf](http://www.math.ku.dk/~jakobsen/geom2/manusgeom2.pdf))

See also

* Wikipedia, _[Differentiable manifold](https://en.wikipedia.org/wiki/Differentiable_manifold)_



[[!redirects differential manifold]]
[[!redirects differential manifolds]]
[[!redirects differentiable manifold]]
[[!redirects differentiable manifolds]]
