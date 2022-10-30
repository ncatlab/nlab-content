

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _tangent bundle_ $T X \to X$ of a (sufficiently [[differentiation|differentiable]]) [[space]] $X$ is a [[bundle]] over $X$ whose [[fiber]] over a [[point]] $x \in X$ is the [[tangent space]] at that point, namely the collection of [[infinitesimal space|infinitesimal]] curves in $X$ emanating at $x$: "[[tangent vectors]]".

For nice enough [[spaces]] such as [[differentiable manifolds]] or more generally [[microlinear spaces]], the tangent bundle of $X$ is a [[vector bundle]] over $X$.

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/TangentSpaceToSphere.png" width="250">
</div>

For example the graphics on the right shows the [[2-sphere]] with one of its [[tangent spaces]]. The tangent bundle of the sphere is the union of all these [[tangent spaces]], regarded as a [[topological space|topological]] [[bundle]] of [[vector space]] (a [[vector bundle]]) over the 2-sphere.

> graphics grabbed from [Hatcher](vector+bundle#Hatcher)



With a notion of tangent bundle comes the following terminology

* A _tangent vector_ on $X$ at $x \in X$ is an element of $T_x X$.

* The _tangent space_ of $X$ at a point $x$ is the [[fiber]] $T_x(X)$ of $T_*(X)$ over $x$;.

* A _tangent vector field_ on $X$ is a [[section]] of $T X$.

The precise definition of tangent bundle depends on the nature of the ambient category of [[space]]s. Below we give first the traditional definitions in ordinary [[differential geometry]]. Then we discuss the construction in more general context of [[smooth toposes]] in [[synthetic differential geometry]] and other categories of [[generalized smooth spaces]].

## Definitions in ordinary differential geometry

Here we define the notion of tangent bundle in the [[category]] [[Diff]] of [[smooth manifold]]s

There are three standard definitions of tangent vector known as

* [algebraic](#AlgebraicDefinition) (via derivations of algebras of smooth functions),

* [geometric](#GeometricDefinition) (via equivalence class of germs of curves)

* [physical](#DefinitionByGluing) (via components in local coordinate system with prescribed behaviour under change of coordinates).


### Algebraic definition
 {#AlgebraicDefinition}

Algebraically, we may define a __tangent vector__ $v$ at $a$ on $X$ as a [[scalar]]-valued [[derivation]] on the space of [[germs]] of  [[differentiable functions]] defined on $X$ near $a$, augmented by evaluation at $a$.  That is, given [[partial functions]] $f$ and $g$, each defined on some [[neighbourhood]] of $a$, we have:

1.  $v[f] = v[g]$ if $f = g$ on some (perhaps smaller) neighbourhood of $a$,
2.  $v[f + g] = v[f] + v[g]$,
3.  $v[c f] = c\, v[f]$ for $c$ a scalar,
4.  $v[f g] = f(a)\, v[g] + v[f]\, g(a)$;

In light of (4), (3) is equivalent to:

*  $v[k] = 0$ for $k$ a [[constant function]] (or indeed, for any function constant on any neighbourhood of $a$).

Globally, we may define a __tangent vector field__ $v$ as an ordinary (unaugmented) derivation on the space of differentiable functions defined on all of $X$.  (This works for differentiable manifolds and smooth manifolds, but not for [[analytic manifold]]s and [[algebraic manifold]]s; we need to be able to change functions locally.)  That is, given [[functions]] $f$ and $g$, we have:

1.  $v[f] = v[g]$ if $f = g$ (so really, the only reason to list this is to keep the numbering the same),
2.  $v[f + g] = v[f] + v[g]$,
3.  $v[c f] = c\, v[f]$ for $c$ a scalar,
4.  $v[f g] = f\, v[g] + v[f]\, g$;

In light of (4), (3) is again equivalent to:

*  $v[k] = 0$ for $k$ a [[constant function]].


Given a differentiable [[curve]] $c: \mathbf{R} \to X$, the __derivative__ $\dot{c}$ of $c$ is a curve in the tangent bundle; given an argument $t$ and a function $f$ defined near $c(t)$, the action is given by
$$ \dot{c}[f](t) = (f \circ c)'(t) ,$$
where $'$ indicates the usual derivative on the real line, so that $\dot{c}(t)$ is a tangent vector at $c(t)$.  (We really only need $c$ to be defined on a neighbourhood of $t$, of course.)



### Geometric definition
 {#GeometricDefinition}

We discuss the tangent bundle of a differentiable manifold by first defining tangent vectors as equivalence classes
of smooth curves in the manifold, then analyzing this construction locally over an atlas, and then gluing these
local constructions together via transition functions.

+-- {: .num_defn #TangencyRelationOnSmoothCurves}
###### Definition
**(tangency relation on smooth curves)**


Let $X$ be a [[differentiable manifold]] of [[dimension]] $n$ and let $x \in X$ be a point. On the set of [[smooth functions]] of the form

$$
  \gamma \;\colon\; \mathbb{R}^1 \longrightarrow X
$$

such that

$$
  \gamma(0) = x
$$

define the [[relations]]

$$
  (\gamma_1 \sim \gamma_2)
   \coloneqq
   \underset{
      {  { \mathbb{R}^n  \underoverset{}{\phi \, \text{chart}}{\to} U_i \subset X } } \atop { U_i \supset \{x\} }
      }{
        \exists
      }
   \left(
      \frac{d}{d t}(\phi^{-1}\circ \gamma_1)(0)
      =
      \frac{d}{d t}(\phi^{-1}\circ \gamma_2)(0)
   \right)
$$

and

$$
  (\gamma_1 \sim' \gamma_2)
   \coloneqq
   \underset{
      {  { \mathbb{R}^n  \underoverset{}{\phi \, \text{chart}}{\to} U_i \subset X } } \atop { U_i \supset \{x\} }
      }{
        \forall
      }
   \left(
      \frac{d}{d t}(\phi^{-1}\circ \gamma_1)(0)
      =
      \frac{d}{d t}(\phi^{-1}\circ \gamma_2)(0)
   \right)
$$

saying that two such functions are related precisely if either there exists a chart around $x$ such that (or else for all charts around $x$ it is true that) the first [[derivative]] of the two functions regarded via the given chart as functions $\mathbb{R}^1 \to \mathbb{R}^n$, coincide at $t = 0$ (with $t$ denoting the canonical [[coordinate]] function on $\mathbb{R}$).

=--

+-- {: .num_lemma #TangencyIsEquivalenceRelation}
###### Lemma
**(tangency is equivalence relation)**

The two relations in def. \ref{TangencyRelationOnSmoothCurves} are [[equivalence relations]] and they coincide.

=--

+-- {: .proof}
###### Proof

First to see that they conincide, we need to show that if the derivatives in question coincide in one chart $\mathbb{R}^n \underoverset{\simeq}{\phi}{\to} U_i \subset X$, that then they coincide also in any other chart $\mathbb{R}^n \underoverset{\simeq}{\psi}{\to} U_j \subset X$.

Write

$$
  U_{i j} \coloneqq U_i \cap U_j
$$

for the intersection of the two charts.

First of all, since the derivative may be computed in any [[open neighbourhood]] around $t = 0$, and since the differentiable functions $\gamma_i$ are in particular [[continuous functions]], we may restrict to the open neighbourhood

$$
  V \coloneqq \gamma_1^{-1}( U_{i j} ) \cap \gamma_2^{-1}(U_{i j})
  \;\subset\; \mathbb{R}
$$

of $0 \in \mathbb{R}$ and consider the derivatives of the functions

$$
  \gamma_i^{\phi}
  \;\coloneqq\;
  (\phi\vert_{U_{i j}} \circ \gamma_i\vert_{V}) \;\colon\; V \longrightarrow \phi^{-1}(U_{i j}) \subset \mathbb{R}^n
$$

and

$$
  \gamma_i^{\psi}
  \;\coloneqq\;
  (\psi\vert_{U_{i j}} \circ \gamma_i \vert _{V}) \;\colon\; V \longrightarrow \psi^{-1}(U_{i j}) \subset \mathbb{R}^n
  \,.
$$

But then by definition of the differentiable [[atlas]], there is the differentiable function

$$
  \alpha
  \;\coloneqq\;
  \phi^{-1}(U_{i j})
    \underoverset{\simeq}{\phi}{\longrightarrow}
  U_{i j}
    \underoverset{\simeq}{\psi^{-1}}{\longrightarrow}
  \psi^{-1}(U_i j)
$$

such that


$$
  \gamma_i^\psi = \alpha \circ \gamma_i^\phi
$$

for $i \in \{1,2\}$. The [[chain rule]] now relates the derivatives of these functions as

$$
  \frac{d}{d t} \gamma_i^\psi
    \;=\;
  (D \alpha) \circ \left(\frac{d}{d t} \gamma_i^\phi\right)
  \,.
$$

Since $\alpha$ is a [[diffeomorphism]] and since derivatives of diffeomorphisms are linear isomorphisms, this says that the derivative of $\gamma_i^\phi$ is related to that of $\gamma_i^\psi$ by a linear isomorphism, and hence

$$
  \left(
   \frac{d}{d t}(\gamma_1)^\phi = \frac{d}{d t}(\gamma_2^\phi)
  \right)
    \;\Leftrightarrow\;
  \left(
   \frac{d}{d t}(\gamma_1)^\psi = \frac{d}{d t}(\gamma_2^\psi)
  \right)
  \,.
$$

Finally, that either relation is an equivalence relation is immediate.


=--



+-- {: .num_defn #TangentVector}
###### Definition
**([[tangent vector]])

Let $X$ be a [[differentiable manifold]] and $x \in X$ a point. Then a _tangent vector_ on $X$ at $x$ is an [[equivalence class]] of the the tangency equivalence relation (def. \ref{TangencyRelationOnSmoothCurves}, lemma \ref{TangencyIsEquivalenceRelation}).

The set of all tangent vectors at $x \in X$ is denoted $T_x X$.

=--

+-- {: .num_lemma #LinearTangentSpace}
###### Lemma
**([[real vector space]] structure on [[tangent vectors]])**

For $X$ a [[differentiable manifold]] of [[dimension]] $n$ and $x \in X$ any point,  let $\mathbb{R}^n \underoverset{\simeq}{\phi}{\to} U \subset X$ be a [[chart]] with $x \in U \subset X$.

Then there is induced a [[bijection]] of sets

$$
  \mathbb{R}^n \overset{\simeq}{\longrightarrow}  T_x X
$$

from the $n$-dimensional [[Cartesian space]] to the set of tangent vectors at $x$ (def. \ref{TangentVector}) given by sending $\vec v \in \mathbb{R}^n$ to the equivalence class of the following smooth curve:

$$
  \array{
    \gamma^\phi_{(-)}
    &
    \mathbb{R}^1
      &\overset{  }{\longrightarrow}&
   \mathbb{R}^n
      &\underoverset{\simeq}{\phi}{\longrightarrow}&
    U_i
    \subset X
    \\
    &
    t
      &\overset{\phantom{AAA}}{\mapsto}&
    t \vec v 
      &\overset{\phantom{AAA}}{\mapsto}&
    \phi(\phi^{-1}(x) + t \vec v)
  }
  \,.
$$

For $\mathbb{R}^n \underoverset{\simeq}{\phi'}{\longrightarrow} U' \subset X$
another chart with $x \in U' \subset X$, then the linear isomorphism relating these two identifications is
the [[differential]]

$$
  D \left((\phi')^{-1} \circ \phi  \right)(x)
  \in GL(n,\mathbb{R})
$$

of the [[gluing function]] of the two charts at the point $x$:

$$
  \array{
    \mathbb{R}^n
    && 
    \overset{
       D \left((\phi')^{-1} \circ \phi\right) (x)}{\longrightarrow} &&
    \mathbb{R}^n
    \\
    & {}_{\mathllap{\simeq}}\searrow && \swarrow_{\mathrlap{\simeq}}
    \\
    && T_x X
  }
  \,.
$$

This is also called the _[[transition function]]_ between the two local identifications of the tangent space.

If $\left\{ \mathbb{R}^n \underoverset{\simeq}{\phi_i}{\to} U_i \subset X \right\}_{i \in I}$
is an [[atlas]] of the [[differentiable manifold]] $X$, then the transition functions

$$
  \left\{
    g_{i j}
    \coloneqq
    d( \phi_j^{-1} \circ \phi_i )
    \colon
    U_i \cap U_j
      \longrightarrow
    GL(n,\mathbb{R})
  \right\}_{i,j \in I}
$$

defined this way satisfy the following [[Cech cohomology|Cech cocycle]] conditions for all $i,j \in I$, $x \in U_i \cap U_j$

1. $g_{i i}(x) = id_{\mathbb{R}^n}$;

1. $g_{j k}\circ g_{i j}(x) = g_{i k}(x)$.

=--

+-- {: .proof}
###### Proof

The bijectivity of the map is immediate from the fact that the first derivative of $\phi^{-1}\circ \gamma^\phi_{\vec v}$
at $\phi^{-1}(x)$ is $\vec v$. 

The formula for the transition function now follows with the [[chain rule]]:

$$  
  \frac{d}{d t} \left(  (\phi')^{-1}\phi(\phi^{-1}(x) + t \vec v ) \right)
  =
  d\left( (\phi')^{-1} \circ \phi \right)(\vec v)
  \,.
$$

Similarly the Cech cocycle condition follows by the [[chain rule]]:

$$
  \begin{aligned}
    g_{j k} \circ g_{i j}(x)
     & =
    d( \phi_k^{-1} \circ \phi_j )
    \circ
    d( \phi_j^{-1} \circ \phi_i )(x)
    \\
    & =
    d( \phi_k^{-1} \circ \phi_j \circ \phi_j^{-1} \circ \phi_i )(x)
    \\
    & =
    d( \phi_k^{-1} \circ \phi_i )(x)
    \\
    &=
    g_{i k}(x)
  \end{aligned}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark
**(notation for tangent vectors in a chart)**

Under the bijection of lemma \ref{LinearTangentSpace} one often denotes the tangent vector  corresponding to the the $i$-th canonical [[linear basis|basis]] vector of $\mathbb{R}^n$ by

$$
  \frac{\partial}{\partial x^i}
  \phantom{AA} \text{or just } \phantom{AA}
  \partial_i
$$

because under the identification of tangent vectors with [[derivations]] on the algebra of [[differentiable functions]] on $X$ as [above](#AlgebraicDefinition) then it acts as the operation of taking the $i$th [[partial derivative]]. The general tangent vector corresponding to $v \in \mathbb{R}^n$ is then denoted by

$$
  \underoverset{i = 1}{n}{\sum}
  v^i
  \frac{\partial}{\partial x^i}
  \phantom{AA} \text{or just } \phantom{AA}
  \underoverset{i = 1}{n}{\sum} v^i \partial_i
  \,.
$$


Notice that this identification depends on the choice of [[chart]], which is left implicit in this notation.

Sometimes, notably in texts on [[thermodynamics]], one augments this notation to indicate the chart being used by listing the remaining coordinate functions as subscripts. For instance if two functions $f,g$ on a 2-dimensional manifold are used as coordinate functions for a local chart (i.e. so that $x^1 = f$ and $x^2 = g$ ), then one write

$$
  (\partial/\partial f)_g
  \phantom{AA}
  (\partial/\partial g)_f
$$

for the tangent vectors $\frac{\partial}{\partial x^1}$ and $\frac{\partial}{\partial x^2}$, respectively.

=--

+-- {: .num_defn #TangentSpace}
###### Definition
**([[tangent space]])**

For $X$ a [[differentiable manifold]] and $x \in X$ a point, then the _[[tangent space]]_ of $X$ at $x$ is the set $T_x X$ of [[tangent vectors]] at $x$ (def. \ref{TangentVector}) regarded as a [[real vector space]] via lemma \ref{LinearTangentSpace}.

=--

+-- {: .num_example #EuclideanSpaceTangentBundle}
###### Example
**([[tangent bundle]] of [[Euclidean space]])

If $X = \mathbb{R}^n$ is itself a [[Euclidean space]], then 
for any two points $x,y \in X$ the [[tangent spaces]] $T_x X$ and $T_y X$ (def. \ref{TangentSpace})
are canonically identified with each other: 

Using the [[vector space]] (or just [[affine space]]) structure of $X = \mathbb{R}^n$ we may send every
smooth function $\gamma \colon \mathbb{R} \to X$ to the smooth function

$$
  \gamma' \colon t \mapsto \gamma(t) + (x-y)
  \,.
$$

This gives a linear bijection

$$
  \phi_{x,y} \colon T_x X \simeq T_y X
$$

and these linear bijections are compatible, in that for $x,y,z \in \mathbb{R}^n$ any three points,
then

$$
  \phi_{y,z} \circ \phi_{x,y} = \phi_{x,z} \;\colon\; T_x X \longrightarrow T_y Y
  \,.
$$

Moreover, by lemma \ref{LinearTangentSpace}, each tangent space is identified with $\mathbb{R}^n$ itself, 
and this identification in turn is compatible with all the above identifications:

$$
  \array{
    && \mathbb{R}^n
    \\
    & \swarrow && \searrow
    \\
    T_x X && \underoverset{\phi_{x,y}}{\simeq}{\longrightarrow} && T_y Y
  }
  \,.
$$

Therefore it makes sense to canonically identify all the tangent spaces of Euclidean space with that Euclidean space
itself. As a result, the collection of all the tangent spaces of Euclidean space is naturally identified 
with the [[Cartesian product]]

$$
  T \mathbb{R}^n = \mathbb{R}^n \times \mathbb{R}^n
$$

equipped with the [[projection]] on the first factor

$$
  \array{
    T \mathbb{R}^n = \mathbb{R}^n \times \mathbb{R}^n
    \\
    \downarrow^{\mathrlap{\pi = pr_1}}
    \\
    \mathbb{R}^n
  }
  \,,
$$

because then the [[pre-image]] of a [[singleton]] $\{x\} \subset \mathbb{R}^n$ under this projection are 
canonically identified with the above tangent spaces:

$$
  \pi^{-1}(\{x\}) \simeq T_x \mathbb{R}^n
  \,.
$$

This way, if we equip $T \mathbb{R}^n = \mathbb{R}^n \times \mathbb{R}^n$ with the [[product space|product space topology]], 
then  $T \mathbb{R}^n \overset{\pi}{\longrightarrow} \mathbb{R}^n$ becomes a [[trivial vector bundle|trivial]] [[topological vector bundle]].
This is called the _[[tangent bundle]]_ of the [[Euclidean space]] $\mathbb{R}^n$ regarded as a [[differentiable manifold]].


=--

We may now globalize the tangent bundle of Euclidean space to tangent bundles of general differentiable manifolds:

+-- {: .num_defn #TangentBundle}
###### Definition
**([[tangent bundle]])**

Let $X$ be a [[differentiable manifold]] with [[atlas]] $\left\{ \mathbb{R}^n \underoverset{\simeq}{\phi_i}{\to} U_i \subset X\right\}_{i \in I}$.

Equip the set of all tangent vectors (def. \ref{TangentVector})

$$
  T X
  \;\coloneqq\;
  \underset{x \in X}{\sqcup} T_x X
$$

with a [[topological space|topology]] $\tau_{T X}$ by declaring a [[subset]] $U \subset T X$ to be an [[open subset]] precisely if for all [[charts]] $\mathbb{R}^n \underoverset{\simeq}{\phi_i}{\to} U_i \subset X$ then its [[preimage]] under

$$
  \array{
    \mathbb{R}^{2n}
      \simeq
    \mathbb{R}^n \times \mathbb{R}^n
      & \overset{d \phi}{\longrightarrow} &
    T X
    \\
    (x, \vec v)
      &\overset{\phantom{AAA}}{\mapsto}&
    \frac{d}{d t} \phi( \phi^{-1}(x) + t \vec v  )
  }
$$

is open in the [[Euclidean space]] $\mathbb{R}^{2n}$ with its [[metric topology]].

Equipped with the [[function]]

$$
  \array{
     T X &\overset{\phantom{AA}p_x \phantom{AA}}{\longrightarrow}& X
     \\
     (x,v) &\overset{\phantom{AAAA}}{\mapsto}& x
  }
$$

this is called the _tangent bundle_ of $X$.

Equivalently this means that the tangent bundle $T X$ is the [[topological vector bundle]] which 
is glued (via [this example](topological+vector+bundle#TopologicalVectorBundleFromCechCocycle)) from the 
[[transition functions]] $g_{i j} \coloneqq d(\phi_j^{-1} \circ \phi_i)$ from lemma \ref{LinearTangentSpace}:

$$
  T X
  \;\coloneqq\;
  \left(
    \underset{i \in I}{\sqcup}
    U_i \times \mathbb{R}^n
  \right)/\left( \left\{  d( \phi_j^{-1} \circ \phi_i ) \right\}_{i, j \in I} \right)
  \,.
$$

(Notice that, by examples \ref{EuclideanSpaceTangentBundle}, each $U_i \times \mathbb{R}^n \simeq T U_i$ is the tangent bundle
of the chart $U_i \simeq \mathbb{R}^n$.)

The co-projection maps of this [[quotient topological space]] construction constitute an [[atlas]] 

$$
  \left\{
    \mathbb{R}^{2n}
      \underoverset{\simeq}{d \phi_i}{\to}
    T (U_i)
     \subset
    T X
  \right\}_{i \in I}
  \,.
$$



=--

+-- {: .num_lemma #DifferentiableTangentBundle}
###### Lemma
**(tangent bundle is differentiable vector bundle)**

If $X$ is a $(p+1)$-times [[differentiable manifold]], then the total space 
of the tangent bundle def. \ref{TangentBundle} is a $p$-times [[differentiable manifold]] in that

1. $(T X, \tau_{T X})$ is a [[paracompact Hausdorff space]];

1. The [[gluing functions]] of the atlas $\left\{ \mathbb{R}^{2n} \underoverset{\simeq}{d \phi_i}{\to} T U_i \subset  T X \right\}_{i \in I}$ are $p$-times continuously differentiable.

Moreover, the projection $\pi \colon T X \to X$ is a $p$-times continuously [[differentiable function]].

=--

+-- {: .proof}
###### Proof

First to see that $T X$ is Hausdorff: 

Let $(x,\vec v), (x', \vec v') \in T X$ be two distinct points. We need to product 
disjoint openneighbourhoods of these points in $T X$. Since in
particular $x,x' \in X$ are distinct, and since $X$ is Hausdorff, there exist disjoint open neighbourhoods
$U_x \supset \{x\}$ and $U_{x'} \supset \{x'\}$. Their pre-images $\pi^{-1}(U_x)$ and $\pi^{-1}(U_{x'})$
are disjoint open neighbourhoods of $(x,\vec v)$ and $(x',\vect v')$, respectively.

Now to see that $T X$ is paracompact. 

Let $\{U_i \subset T X\}_{i \in I}$ be an open cover. We need to find a [[locally finite cover|locally finite]]
[[refinement]]. Notice that $\pi \colon T X \to X$ is an [[open map]] (by [this example](open+map#ProjectionsAreOpenContinuousFunctions))
so that $\{\pi(U_i) \subset X\}_{i \in I}$ is an open cover of $X$. 

Let now $\{\mathbb{R}^n \underoverset{\simeq}{\phi_j}{\to} V_j \subset X\}_{j \in J}$ be an [[atlas]] for $X$ and consider the 
open common refinement

$$
  \left\{ \pi(U_i) \cap V_j \subset X  \right\}_{i \in I, j \in J}
  \,.
$$

Since this is still an open cover of $X$ and since $X$ is paracompact, this has a locally finite refinement

$$
  \left\{ V'_{j'} \subset X\right\}_{j' \in J'}
$$

Notice that for each $j' \in J'$ the product topological space $V'_{j'} \times \mathbb{R}^n \subset \mathbb{R}^{2n}$ 
is paracompact (as a [[topological subspace]] of [[Euclidean space]] it is itself [[locally compact topological space|locally compact]]
and [[second countable topological space|second countable]] and since [[locally compact and second-countable spaces are paracompact]]).
Therefore the cover 

$$
  \{ \pi^{-1}(V'_{j'}) \cap U_i \subset V'_{j'} \times \mathbb{R}^n \}_{(i,j') \in I \times J'}
$$ 

has a locally finite refinement

$$
  \{W_{k_{j'}} \subset V'_{j'} \times \mathbb{R}^n \}_{k_{j'} \in K_{j'}}
  \,.
$$

We claim now that 

$$
  \{ W_{k_{j'}}  \subset T X \}_{j' \in J',  k_{j'} \in K_{j'}}
$$ 

is a locally finite refinement of the original cover.
That this is an open cover refining the original one is clear. We need to see that it is locally finite.

So let $(x,\vec v) \in T X$. By local finiteness of $\{ V'_{j'}  \subset X\}_{j' \in J'}$ there is an open neighbourhood
$V_x \supset \{x\}$ which intersects only finitely many of the $V'_{j'} \subset X$. 
Then by local finiteness of $\{ W_{k_{j'}}  \subset V'_{j_'}\}$, for each such $j'$ the point $(x,\vec v)$ 
regarded in $V'_{j'} \times \mathbb{R}^n$ has an open neighbourhood $U_{j'}$ that intersects only finitely many of the $W_{k_{j'}}$. Hence the
intersection $\pi^{-1}(V_x) \cap \left( \underset{j'}{\cap}  U_{j'} \right)$ is a finite intersection of open subsets, hence still open,
and by construction it intersects still only a finite number of the $W_{k_{j'}}$.

This shows that $T X$ is paracompact.

Finally the statement about the differentiability of the glung functions and of the projections is immediate from the definitions

=--

+-- {: .num_prop #FunctionsBetweenDifferentiableManifoldsDifferentials}
###### Proposition
**([[differentials]] of [[differentiable functions]] between [[differentiable manifolds]])**

Let $X$ and $Y$ be [[differentiable manifolds]] and let $f \;\colon\; X \longrightarrow Y$ be a [[differentiable function]]. Then the operation of postcomposition which takes differentiable curves in $X$ to differentiable curves in $Y$

$$
  \array{
     Hom_{Diff}(\mathbb{R}^1, X)
       &\overset{f \circ (-)}{\longrightarrow}&
     Hom_{Diff}(\mathbb{R}^1, Y)
     \\
     \left(
       \mathbb{R}^1 \overset{\gamma}{\to} X
     \right)
     &\overset{\phantom{AAA}}{\mapsto}&
     \left(
       \mathbb{R}^1 \overset{f \circ \gamma}{\to} Y
     \right)
  }
$$

descends at each point $x \in X$ to the tangency [[equivalence relation]] (def. \ref{TangencyRelationOnSmoothCurves}, lemma \ref{TangencyIsEquivalenceRelation}) to yield a function on sets of [[tangent vectors]] (def. \ref{TangentVector}), called the _[[differential]]_ $d f|_{x}$ of $f$ at $x$

$$
  d f|_{x}
    \;\colon\;
  T_x X
   \longrightarrow
  T_{f(x)} Y
  \,.
$$

Moreover:

1. ([[linear function|linear dependence]] on the tangent vector) these differentials are [[linear functions]] with respect to the vector space structure on the [[tangent spaces]] from lemma \ref{LinearTangentSpace}, def. \ref{TangentSpace};

1. ([[differentiable function|differentiable dependence]] on the base point) globally they yield a [[homomorphism]] of differentiable real vector bundles  between the [[tangent bundles]] (def. \ref{TangentBundle}, lemma \ref{DifferentiableTangentBundle}), called the global _[[differential]]_ $d f$ of $f$

   $$
     d f \;\colon\; T X \longrightarrow T Y
     \,.
   $$

1. ([[chain rule]]) The assignment $f \mapsto d f$ respects [[composition]] in that for $X$, $Y$, $Z$ three [[differentiable manifolds]] and for

   $$
     X
       \overset{\phantom{A}f\phantom{A}}{\longrightarrow}
     Y
       \overset{\phantom{A}g\phantom{A}}{\longrightarrow}
     Z
   $$

   two [[composition|composable]] [[differentiable functions]] then their [[differentials]] satisfy

   $$
     d(g \circ f) = (d g) \circ (d f)
     \,.
   $$

=--

+-- {: .proof}
###### Proof


=--

+-- {: .num_remark}
###### Remark

In the language of [[category theory]] the statement of prop. \ref{FunctionsBetweenDifferentiableManifoldsDifferentials} says that forming [[tangent bundles]] $T X$ of [[differentiable manifolds]] $X$ and [[differentials]] $d f$  of [[differentiable functions]] $f \colon X \to Y$ constitutes a [[functor]]

$$
  T \;\colon\; Diff \longrightarrow Vect(Diff)
$$

from the [[category]] [[Diff]] of [[differentiable manifolds]] to the category of differentiable real vector bundles.

=--



### Definition by gluing construction
 {#DefinitionByGluing}

If $M$ is a smooth $n$-manifold, then we know the tangent space at each point is isomorphic to $\mathbb{R}^n$. We can exploit this fact to construct the tangent space by gluing many copies of $\mathbb{R}^n$ together. However, one drawback is that it is not immediately obvious that the result is independent of the atlas chosen.

Let $M$ be a smooth $n$-manifold defined by an atlas $(U_\alpha, \phi_\alpha)$. Then we may define its tangent bundle $T M$ by a gluing construction in $Top$, taking $T M$ to be the quotient of the disjoint sum

$$\sum_\alpha U_\alpha \times \mathbb{R}^n$$

obtained by dividing by the equivalence relation

$$(p \in U_\alpha, v) \sim (p \in U_\beta, g_{\alpha\beta}(p) v)$$

where $p \in U_\alpha \cap U_\beta$, and $g_{\alpha\beta}(p) \in GL(\mathbb{R}^n)$ is the result of differentiating the transition function $\phi_{\alpha\beta}$ at the point $\phi_\alpha(p)$. We thus obtain a covering $U_\alpha \times \mathbb{R}^n$ of $T M$, and these form coordinate charts of a smooth manifold structure on $T M$ in a more or less evident way, and the projection map is given by
$$
  p: (x, v) \mapsto x.
$$

In the above construction, the charts $\phi_\alpha$ were not used directly; Instead, the transition maps

$$g_{\alpha \beta}: U_\alpha \cap U_\beta \to GL(\mathbb{R}^n)$$

are what were needed to construct the tangent bundle. These maps satisfy &#268;ech 1-cocycle relations

$$g_{\alpha \gamma} = g_{\beta\gamma} \circ g_{\alpha\beta}: U_{\alpha} \cap U_\beta \cap U_\gamma \to GL(\mathbb{R}^n)$$

$$\qquad g_{\alpha\alpha} = 1: U_{\alpha} \to GL(\mathbb{R}^n)$$

In general, given any collection of transition maps that satisfy these cocycle conditions, we can construct a [[vector bundle]] in the same manner (which may be different from the tangent bundle).

## Definition in synthetic differential geometry {#InSDG}

The above definitions in ordinary [[differential geometry]] suggest the slogan

+-- {: .standout}

Tangent vectors are infinitesimal curves in a space.

=--

One of the central motivations for [[synthetic differential geometry]] is the desire to provide a context in which this slogan becomes literally formally true.

+-- {: .un_defn}
###### Definition
**(tangent bundle in smooth toposes)**

Let $(\mathcal{T},(R,+,\cdot))$ be a [[smooth topos]] and write  $D = \{\epsilon \in R| \epsilon^2 = 0\}$ for the standard [[infinitesimal space|infinitesimal interval]]. For $X \in \mathcal{T}$ any object (any [[space]] in $\mathcal{T}$), the **tangent bundle** of $X$ is the morphism

$$
  p : T X \to X
$$

with

* $T X \coloneq X^D$ the [[internal hom]] of $D$ into $X$;

* $p = ev_0$ the evaluation map at the origin of $D$

  $ev_0 : (U \stackrel{v}{\to} X^D) \mapsto
  (U \times {*} \stackrel{Id \times 0}{\to} U \times D
  \stackrel{\bar v}{\to} X)$,

  where $\bar v$ is the hom-[[adjunct]] of $v$.

=--

This definition captures elegantly and usefully the notion of tangent vectors as infinitesimal curves. But it is not guaranteed that the fibers of a synthetic tangent bundle $X^D$ are fiberwise linear, i.e. are fiberwise $R$-modules the way one expects. Objects $X$ for which this is true are [[microlinear space]]s in $\mathcal{T}$. See there for more details.

A [[smooth topos]] $\mathcal{T}$ is called a _well-adapted model_ for [[synthetic differential geometry]] if there is a [[full and faithful functor|full and faithful]] embedding [[Diff]] $\hookrightarrow \mathcal{T}$ of the cageory of [[manifold]]s into $\mathcal{T}$.

Typically, for well adapted models, under this embedding

* manifolds are [[microlinear space]]s

* the synthetic definition of tangent bundle $X^D$ for $X$ a manifold does coincide with the ordinary notion of $T X$.

Let $\mathbb{L} = (C^\infty Ring^{fin})^{op}$ be the category of [[generalized smooth algebra|smooth loci]]. For $M$ a [[manifold]], the exponential $M^D$ does exist in $\mathbb{L}$ and is isomorphic to the ordinary tangent bundle $T X$ of $X$. (For instance  [[Models for Smooth Infinitesimal Analysis|MSIA, chapter II, prop 1.12]].

There are well-adapted [[smooth topos]]es $\mathcal{Z}$ and $\mathcal{B}$ presented as [[category of sheaves|categories of sheaves]] on $\mathbb{L}$: the first for the [[Grothendieck topology]] where covers are _finite_ open covers, the second where covers are finite open covers and projections ([[Models for Smooth Infinitesimal Analysis|MSIA, chapter VI]]). Both topologies are [[subcanonical coverage|subcanonical]], hence the [[Yoneda embedding]] $Y : \mathbb{L} \to Sh(\mathbb{L})$ does preserve the above property.

Hence in these models for $X \in Diff$ a [[manifold]], $T X \in Diff$ its ordinary tangent bundle and $s : Diff \to Sh(\mathbb{L})$ the full and faithful embedding, we have isomorphisms

$$
  (s(X))^D  \simeq s(T X)
$$

which respect the bundle maps.

## As a supermanifold

The tangent bundle of a manifold $X$ may be interpreted as a [[supermanifold]] in which $X$ has degree $0$ and the tangent vectors have degree $1$.  See [[shifted tangent bundle]].

## Definition for other generalized smooth spaces

There are useful categories of [[generalized smooth space]]s which are neither categories of manifolds nor [[smooth topos]]es modeling [[synthetic differential geometry]]. But most of them admit useful notions of tangent bundles, too, sometimes more than one.

See [[Frölicher space]] and [[diffeological space]] for the definitions in their context.

## Related concepts

* [[synthetic tangent bundle]], [[kinematic tangent bundle]], [[operational tangent bundle]]

* [[cotangent bundle]]
* [[normal bundle]]
* [[G-structure]]
* [[tangent cone]]

* [[Lie algebra]]

[[!include infinitesimal and local - table]]

* in [[homotopy theory]]/[[Goodwillie calculus]]: [[tangent (∞,1)-category]]

## References

A textbook account of tangent bundles in the context of [[synthetic differential geometry]] is in

* [[Ieke Moerdijk]], [[Gonzalo Reyes|Gonzalo E. Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ Springer (1991)

Further discussion of axiomatizations in this context is in

* {#CockettCruttwell} [[J.R.B. Cockett]], [[Geoff Cruttwell]], _Differential structure, tangent structure, and SDG_ (2012) ([pdf](http://www.mta.ca/~gcruttwell/publications/sman3.pdf))


Discussion for [[diffeological spaces]] is in

* Carlos Torre, _A tangent bundle for diffeological spaces_ ([arXiv:math/9801046](http://arxiv.org/abs/math/9801046))

[[!redirects tangent vector]]
[[!redirects tangent space]]
[[!redirects tangent vector space]]
[[!redirects tangent vector field]]
[[!redirects tangent bundles]]
[[!redirects tangent vectors]]
[[!redirects tangent spaces]]
[[!redirects tangent vector spaces]]
[[!redirects tangent vector fields]]

[[!redirects tangent]]
[[!redirects tangents]]
