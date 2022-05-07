
> This entry is about [[tangent vectors]] on [[differentiable manifolds]] and the [[bundle]] they form. For the [[tangent function]] see there.

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

* The _tangent space_ of $X$ at a point $x$ is the [[fiber]] $T_x(X)$ of $T X$ over $x$;.

* A _tangent vector field_ on $X$ is a [[section]] of $T X$.

The precise definition of tangent bundle depends on the nature of the ambient category of [[space]]s. Below we give first the traditional definitions in ordinary [[differential geometry]]. Then we discuss the construction in more general context of [[smooth toposes]] in [[synthetic differential geometry]] and other categories of [[generalized smooth spaces]].

## Definitions

### Traditional definition
 {#TraditionalDefinition}


We discuss the tangent bundle of a differentiable manifold by first defining tangent vectors as equivalence classes
of differentiable curves in the manifold, then analyzing this construction locally over an atlas, and then gluing these
local constructions together via transition functions.

+-- {: .num_defn #TangencyRelationOnSmoothCurves}
###### Definition
**(tangency relation on differentiable curves)**


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

First to see that they coincide, we need to show that if the derivatives in question coincide in one chart $\mathbb{R}^n \underoverset{\simeq}{\phi_i}{\to} U_i \subset X$, that then they coincide also in any other chart $\mathbb{R}^n \underoverset{\simeq}{\phi_j}{\to} U_j \subset X$.

For brevity, write

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
  \gamma_n^i
  \;\coloneqq\;
  (\phi_i^{-1}\vert_{U_{i j}} \circ \gamma_n\vert_{V}) \;\colon\; V \longrightarrow \phi_i^{-1}(U_{i j}) \subset \mathbb{R}^n
$$

and

$$
  \gamma_n^j
  \;\coloneqq\;
  (\phi_j^{-1}\vert_{U_{i j}} \circ \gamma_n \vert _{V}) \;\colon\; V \longrightarrow \phi_j^{-1}(U_{i j}) \subset \mathbb{R}^n
  \,.
$$

But then by definition of the differentiable [[atlas]], there is the differentiable gluing function

$$
  \alpha
  \;\coloneqq\;
  \phi_i^{-1}(U_{i j})
    \underoverset{\simeq}{\phi_i}{\longrightarrow}
  U_{i j}
    \underoverset{\simeq}{\phi_j^{-1}}{\longrightarrow}
  \phi_j^{-1}(U_{i j})
$$

such that


$$
  \gamma_n^j = \alpha \circ \gamma_n^i
$$

for $n \in \{1,2\}$. The [[chain rule]] now relates the derivatives of these functions as

$$
  \frac{d}{d t} \gamma_n^j
    \;=\;
  (D \alpha) \circ \left(\frac{d}{d t} \gamma_n^i  \right)
  \,.
$$

Since $\alpha$ is a [[diffeomorphism]] and since derivatives of diffeomorphisms are linear isomorphisms, this says that the derivative of $\gamma_n^j$ is related to that of $\gamma_n^i$ by a linear isomorphism , and hence

$$
  \left(
   \frac{d}{d t} \gamma_1^i  = \frac{d}{d t} \gamma_2^i
  \right)
    \;\Leftrightarrow\;
  \left(
   \frac{d}{d t} \gamma_1^j = \frac{d}{d t} \gamma_2^j
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

from the $n$-dimensional [[Cartesian space]] to the set of tangent vectors at $x$ (def. \ref{TangentVector}) given by sending $\vec v \in \mathbb{R}^n$ to the equivalence class of the following differentiable curve:

$$
  \array{
    \gamma^\phi_{\vec v}
    \colon
    &
    \mathbb{R}^1
      &\overset{ \phi^{-1}(x) + (-)\cdot \vec v }{\longrightarrow}&
   \mathbb{R}^n
      &\underoverset{\simeq}{\phi}{\longrightarrow}&
    U_i
    \subset X
    \\
    &
    t
      &\overset{\phantom{AAA}}{\mapsto}&
    \phi^{-1}(x) +  t \vec v
      &\overset{\phantom{AAA}}{\mapsto}&
    \phi(\phi^{-1}(x) + t \vec v)
  }
  \,.
$$

For $\mathbb{R}^n \underoverset{\simeq}{\phi'}{\longrightarrow} U' \subset X$
another chart with $x \in U' \subset X$, then the linear isomorphism relating these two identifications is
the [[derivative]]

$$
  d \left((\phi')^{-1} \circ \phi  \right)_{ \phi^{-1}(x) }
  \in
  GL(n,\mathbb{R})
$$

of the [[gluing function]] of the two charts at the point $x$:

$$
  \array{
    \mathbb{R}^n
    &&
    \overset{
       d \left((\phi')^{-1} \circ \phi\right)_{\phi^{-1}(x)}}{\longrightarrow} &&
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
    d( \phi_j^{-1} \circ \phi_i )_{\phi_i^{-1}(-)}
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
  d \left( (\phi')^{-1} \circ \phi( \phi^{-1}(x) + (-) \vec v )   \right)_0
  =
  d \left( (\phi')^{-1} \circ \phi \right)_{\phi^{-1}(x)} \circ \underset{ =(-)\vec v }{\underbrace{ d ( \phi^{-1}(x) +(-)\vec v )_0 }}
  \,.
$$

Similarly the Cech cocycle condition follows by the [[chain rule]]:

$$
  \begin{aligned}
    g_{j k} \circ g_{i j}(x)
     & =
    d( \phi_k^{-1} \circ \phi_j )_{\phi_j^{-1}(x)}
    \circ
    d( \phi_j^{-1} \circ \phi_i )_{\phi_i^{-1}(x)}
    \\
    & =
    d( \phi_k^{-1} \circ \phi_j \circ \phi_j^{-1} \circ \phi_i )_{\phi_i^{-1}(x)}
    \\
    & =
    d( \phi_k^{-1} \circ \phi_i )_{\phi_i^{-1}(x)}
    \\
    &=
    g_{i k}(x)
  \end{aligned}
  \,.
$$

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
  \phi_{x,y} \colon T_x X \overset{\simeq}{\longrightarrow} T_y X
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
    & {}^{\mathllap{\simeq}}\swarrow && \searrow^{\mathrlap{\simeq}}
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

+-- {: .num_remark #EuclideanTangentSpaceFunctoriality}
###### Remark
**([[chain rule]] is [[functor|functoriality]] of [[tangent space]] construction on [[Euclidean spaces]])**

Consider the assignment that sends

1. every [[Euclidean space]] $\mathbb{R}^n$ to its [[tangent bundle]] $T \mathbb{R}^n$ according to def. \ref{EuclideanSpaceTangentBundle};

1. every [[differentiable function]] $f \colon \mathbb{R}^{n_1} \longrightarrow \mathbb{R}^{n_2}$ to the
   function on [[tangent vectors]] (def. \ref{TangentVector}) induced by postcomposition with $f$

   $$
     \array{
       T \mathbb{R}^{n_1}
         &\overset{f \circ (-)}{\longrightarrow}&
       T \mathbb{R}^{n_2}
       \\
       \left[
         \mathbb{R}^1
           \overset{\gamma}{\longrightarrow}
         \mathbb{R}^{n_1}
       \right]
         &\mapsto&
       \left[
         \mathbb{R}^1
           \overset{ f \circ \gamma}{\longrightarrow}
         \mathbb{R}^{n_2}
       \right]
     }
   $$

By the [[chain rule]] we have that the [[derivative]] of the composite curve $f \circ \gamma$ is

$$
  d (f \circ \gamma)_t
  =
  (d f_{\gamma(x)}) \circ d\gamma
$$

and hence that under the identification $T \mathbb{R}^n \simeq \mathbb{R}^n \times \mathbb{R}^n$ of example \ref{EuclideanSpaceTangentBundle}
this assignment takes $f$ to its [[derivative]]

   $$
     \array{
       \mathbb{R}^{n_1} \times \mathbb{R}^{n_1}
         &\overset{ d f }{\longrightarrow}&
       \mathbb{R}^{n_2} \times \mathbb{R}^{n_2}
       \\
       (x,\vec v)
         &\mapsto&
       (f(x), d f_x(\vec v))
     }
     \,,
   $$

Conversely, in the first form above the assignment $f \mapsto f \circ (-)$ manifestly
respects [[composition]] (and [[identity functions]]). Viewed from the second perspective
this respect for composition is once again the [[chain rule]] $d(g \circ f) = (d f)\circ (d g)$:

$$
  \array{
    && Y
    \\
    & {}^{\mathllap{f}}\nearrow  && \searrow^{\mathrlap{g}}
    \\
    X && \underset{ g\circ  f}{\longrightarrow} && Z
  }
  \phantom{AAA}
    \mapsto
  \phantom{AAA}
  \array{
    && T Y
    \\
    & {}^{\mathllap{d f}}\nearrow && \searrow^{\mathrlap{d g}}
    \\
    T X &&  \underset{d(g \circ f)}{\longrightarrow} && T Z
  }
  \,.
$$

In the language of [[category theory]] this says that the assignment

$$
  \array{
    CartSp &\overset{T}{\longrightarrow}& CartSp
    \\
    X &\mapsto& T X
    \\
    {}^{\mathllap{ f }}\downarrow && \downarrow^{\mathrlap{d f}}
    \\
    Y &\mapsto& T Y
  }
$$

is an [[endofunctor]] on the [[category]] [[CartSp]] whose

1. [[objects]] are the [[Euclidean spaces]] $\mathbb{R}^n$ for $n \in \mathbb{N}$;

1. [[morphisms]] are the [[differentiable functions]] between these (for any chosen differentiability class $C^k$ with $k \gt 0$).

=--

We may now globalize the tangent bundle of Euclidean space to tangent bundles of general differentiable manifolds:

+-- {: .num_defn #TangentBundle}
###### Definition
**([[tangent bundle]] of a [[differentiable manifold]])**

Let $X$ be a [[differentiable manifold]] with [[atlas]] $\left\{ \mathbb{R}^n \underoverset{\simeq}{\phi_i}{\to} U_i \subset X\right\}_{i \in I}$.

Equip the set of all [[tangent vectors]] (def. \ref{TangentVector}), i.e. the [[disjoint union]] of the sets of tangent vectors

$$
  T X
  \;\coloneqq\;
  \underset{x \in X}{\sqcup} T_x X
  \phantom{AAA}
  \text{as underlying sets}
$$

with a [[topological space|topology]] $\tau_{T X}$ by declaring a [[subset]] $U \subset T X$ to be an [[open subset]] precisely if for all [[charts]] $\mathbb{R}^n \underoverset{\simeq}{\phi_i}{\to} U_i \subset X$ we have that its [[preimage]] under

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
    [ t \mapsto \phi(\phi^{-1}(x) + t \vec v) ]
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
[[transition functions]] $g_{i j} \coloneqq d(\phi_j^{-1} \circ \phi_i)_{\phi^{-1}(-)}$ from lemma \ref{LinearTangentSpace}:

$$
  T X
  \;\coloneqq\;
  \left(
    \underset{i \in I}{\sqcup}
    U_i \times \mathbb{R}^n
  \right)/\left( \left\{  d( \phi_j^{-1} \circ \phi_i )_{\phi^{-1}_i(-)} \right\}_{i, j \in I} \right)
  \,.
$$

(Notice that, by examples \ref{EuclideanSpaceTangentBundle}, each $U_i \times \mathbb{R}^n \simeq T U_i$ is the tangent bundle
of the chart $U_i \simeq \mathbb{R}^n$.)

The co-projection maps of this [[quotient topological space]] construction constitute an [[atlas]]

$$
  \left\{
    \mathbb{R}^{2n}
      \underoverset{\simeq}{}{\to}
    T U_i
     \subset
    T X
  \right\}_{i \in I}
  \,.
$$



=--

+-- {: .num_lemma #DifferentiableTangentBundle}
###### Lemma
**([[tangent bundle]] is [[differentiable vector bundle]])**

If $X$ is a $(p+1)$-times [[differentiable manifold]], then the total space
of the tangent bundle def. \ref{TangentBundle} is a $p$-times [[differentiable manifold]] in that

1. $(T X, \tau_{T X})$ is a [[paracompact Hausdorff space]];

1. The [[gluing functions]] of the atlas $\left\{ \mathbb{R}^{2n} \underoverset{\simeq}{d \phi_i}{\to} T U_i \subset  T X \right\}_{i \in I}$ are $p$-times continuously differentiable.

Moreover, the projection $\pi \colon T X \to X$ is a $p$-times continuously [[differentiable function]].

In summary this makes $T X \to X$ a _[[differentiable vector bundle]]_.

=--

+-- {: .proof}
###### Proof

First to see that $T X$ is Hausdorff:

Let $(x,\vec v), (x', \vec v') \in T X$ be two distinct points. We need to produce
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

Finally the statement about the differentiability of the [[gluing functions]] and of the projections is immediate from the definitions

=--

+-- {: .num_prop #FunctionsBetweenDifferentiableManifoldsDifferentials}
###### Proposition
**([[differentials]] of [[differentiable functions]] between [[differentiable manifolds]])**

Let $X$ and $Y$ be [[differentiable manifolds]] and let $f \;\colon\; X \longrightarrow Y$ be a [[differentiable function]]. Then the operation of postcomposition, which takes differentiable curves in $X$ to differentiable curves in $Y$,

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

descends at each point $x \in X$ to the tangency [[equivalence relation]] (def. \ref{TangencyRelationOnSmoothCurves}, lemma \ref{TangencyIsEquivalenceRelation}) to yield a function on
sets of [[tangent vectors]] (def. \ref{TangentVector}), called the _[[differential]]_ $d f_x$ of $f$ at $x$

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

1. ([[differentiable function|differentiable dependence]] on the base point) globally they
yield a [[homomorphism]] of real [[differentiable vector bundles]]  between the [[tangent bundles]] (def. \ref{TangentBundle}, lemma \ref{DifferentiableTangentBundle}), called the global _[[differential]]_ $d f$ of $f$

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

All statements are to be tested on charts of an atlas for $X$ and for $Y$. On these charts the
statement reduces to that of example \ref{EuclideanSpaceTangentBundle}.

=--

+-- {: .num_remark}
###### Remark
**(tangent [[functor]])**

In the language of [[category theory]] the statement of prop. \ref{FunctionsBetweenDifferentiableManifoldsDifferentials} says that forming [[tangent bundles]] $T X$ of [[differentiable manifolds]] $X$ and [[differentials]] $d f$  of [[differentiable functions]] $f \colon X \to Y$ constitutes a [[functor]]

$$
  T \;\colon\; Diff \longrightarrow Vect(Diff)
$$

from the [[category]] [[Diff]] of [[differentiable manifolds]] to the category of differentiable real vector bundles.


=--


+-- {: .num_defn #VectorField}
###### Definition
**([[vector field]])**

Let $X$ be a [[differentiable manifold]] with differentiable tangent bundle $T X \to X$ (def. \ref{TangentBundle}).

A differentiable [[section]] $v \colon X \to T X$ of the tangent bundle is called a (differentiable)
_[[vector field]]_ on $X$.


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

Sometimes, notably in texts on [[thermodynamics]], one augments this notation to indicate the chart being used by listing the remaining coordinate functions as subscripts. For instance if two functions $f,g$ on a 2-dimensional manifold are used as coordinate functions for a local chart (i.e. so that $x^1 = f$ and $x^2 = g$ ), then one writes

$$
  (\partial/\partial f)_g
  \phantom{AA}
  (\partial/\partial g)_f
$$

for the tangent vectors $\frac{\partial}{\partial x^1}$ and $\frac{\partial}{\partial x^2}$, respectively.

=--



### Via derivations of smooth functions
 {#ViaDerivationsOfSmoothFunctions}

+-- {: .num_remark #AlgebraicDefinition}
###### Remark
**([[derivations of smooth functions are vector fields]])**

Let $X$ be a [[smooth manifold]] and write $C^\infty(X)$ for the [[associative algebra]] over the [[real numbers]]
of  [[smooth functions]] $X \longrightarrow \mathbb{R}$.

Then every smooth [[vector field]] $v \in \Gamma_X(T X)$ (def. \ref{VectorField}) induces a [[function]]


$$
  \partial_v
    \;\colon\;
  C^\infty(X) \longrightarrow C^\infty(X)
$$

by

$$
  \partial f \;\colon\; x \mapsto \frac{d}{d t} (f \circ \gamma_{v_x})_0
$$

where $\gamma_{v_x} \colon \mathbb{R}^1 \to X$ is a smooth curve which represents the [[tangent vector]] $v(x) \in T_x X$ according to def. \ref{TangentVector}.

The linearity of [[derivatives]] and the [[product rule]] of [[differentiation]]
imply that this function $\partial_v$ is a [[derivation]] on the algebra of smooth functions. Hence there is a function

$$
  \array{
    \Gamma_X(T X)
      &\longrightarrow&
    Der(C^\infty(X))
    \\
    v &\mapsto& \partial_v
  }
  \,.
$$

It turns out that this function is in fact a [[bijection]]: every derivation of the algebra of smooth functions
on a smooth manifold arises uniquely from a smooth tangent vector in this way.



For more on this see at _[[derivations of smooth functions are vector fields]]_.

=--

\begin{remark}

For manifolds of the class $C^k$, $0\lt k\lt \infty$,
the definition of a tangent vector as a [[derivation]] of the algebra
of functions ([[derivations of smooth functions are vector fields]]) remains valid if one strengthens the definition of a [[derivation]] $D$ by adjoining, on top of the algebraic condition of the [[product]] rule 

$$
  D (f \cdot g) = (D f) g + f (D g)
$$

also the algebraic incarnation of the [[chain rule]]:

$$
  D(f(g_1,\ldots,g_m))
  \;=\;
  \sum_i (\partial_i f)(g_1,\ldots,g_m)D(g_i).
$$

See [Newns-Walker 56](#NewnsWalker56).

\end{remark}




### In synthetic differential geometry
 {#InSDG}

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

A [[smooth topos]] $\mathcal{T}$ is called a _well-adapted model_ for [[synthetic differential geometry]] if there is a [[full and faithful functor|full and faithful]] embedding [[Diff]] $\hookrightarrow \mathcal{T}$ of the category of [[manifold]]s into $\mathcal{T}$.

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


### In supergeometry

The tangent bundle of a manifold $X$ may be interpreted as a [[supermanifold]] in which $X$ has degree $0$ and the tangent vectors have degree $1$.  See [[shifted tangent bundle]].

### For other generalized smooth spaces

There are useful categories of [[generalized smooth space]]s which are neither categories of manifolds nor [[smooth topos]]es modeling [[synthetic differential geometry]]. But most of them admit useful notions of tangent bundles, too, sometimes more than one.

See [[Frölicher space]] and [[diffeological space]] for the definitions in their context.

## Related concepts

* [[synthetic tangent bundle]], [[kinematic tangent bundle]], [[operational tangent bundle]]

* [[cotangent bundle]]

* [[normal bundle]]

* [[G-structure]]

* [[stable tangent bundle]]

* [[tangent cone]]

* [[Lie algebra]]

[[!include infinitesimal and local - table]]

* in [[homotopy theory]]/[[Goodwillie calculus]]: [[tangent (∞,1)-category]]

## References

An early account of  [[derivations of smooth functions are vector fields|tangent vectors as derivations]], including the $C^k$-case for $0\lt k\lt \infty$ is in

* {#NewnsWalker56} [[W. F. Newns]], [[A. G. Walker]],  _Tangent Planes To a Differentiable Manifold_.  Journal of the London Mathematical Society s1-31:4 (1956), 400–407 ([doi:10.1112/jlms/s1-31.4.400](https://doi.org/10.1112/jlms/s1-31.4.400))


A textbook account of tangent bundles in the context of [[synthetic differential geometry]]:

* [[Ieke Moerdijk]], [[Gonzalo Reyes|Gonzalo E. Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ Springer (1991)

Further discussion of axiomatizations in this context is in

* {#CockettCruttwell} [[J.R.B. Cockett]], [[Geoff Cruttwell]], _Differential structure, tangent structure, and SDG_ (2012) ([pdf](https://www.mta.ca/uploadedFiles/Community/Bios/Geoff_Cruttwell/sman3.pdf))


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

