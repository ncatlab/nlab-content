
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Bundles#
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

A _topological vector bundle_ is a [[vector bundle]] in the context of _[[topology]]_: a continuously varying collection of [[vector space]] over a given [[topological space]].

For more survey and motivation see at _[[vector bundle]]_. Here we discuss the details of the general concept in [[topology]].
See also _[[differentiable vector bundle]]_ and _[[algebraic vector bundle]]_.



## Definition

We first give the more abstract definiton
in terms of slice categories (def. \ref{TopologicalVectorBundleInTermsOfSliceCategories} below) and then unwind this to the traditional definition (def \ref{TopologicalVectorBundle} below).

In the following

* $k$ is either the [[topological field]]

  * $k = \mathbb{R}$ of [[real numbers]]

  * or $k = \mathbb{C}$ of [[complex numbers]]

  equipped with the [[Euclidean space|Euclidean]] [[metric topology]].

* _[[vector space]]_ means _[[finite dimensional vector space]]_.


### In terms of slice categories
 {#InTermsOfSliceCategories}

+-- {: .num_defn #TopologicalVectorBundleInTermsOfSliceCategories}
###### Definition
**(topological vector bundles in terms of slice categories)**

Write [[Top]] for the [[category]] of [[topological spaces]], and for $X \in Top$ a space, write $Top_{/X}$ for its [[slice category]] over $X$. The [[Cartesian product]] in $Top_{/X}$ is the [[fiber product]] over $X$ in $Top$, which we denote by $(-) \times_X (-)$.
Observe $[X \times k \to X] \in Top_{/X}$ is canonically a [[field]] [[internalization|internal]] to $Top_{/X}$

A _topological vector bundle_ over $X \in Top$ is

1. an [[object ]] $[E \overset{\pi}{\to} X]$ of $Top_{/X}$

1. with the [[structure]] of an $X \times k$-[[vector space]]-object [[internalization|internal]] to $Top_{/X}$, hence

   1. a [[morphism]] $ (-)+(-) \;\colon\; E \times_X E \to E$

   1. a morphism $(-)\cdot(-) \;\colon\;  k \times E \to E$

   which satisfy the vector space axioms

such that

* ([[local trivialization|local triviality]]) there exists

  1. an [[open cover]] $\{U_i \subset X\}_{i \in I}$, regarded via the [[disjoint union space]] $U \coloneqq \underset{i \in I}{\sqcup} U_i$ of the patches as the object $ [U \to X] \in Top_{/X}$,

  1. an [[isomorphism]] of vector space objects in $Top_{/U}$

     $$
       U \times \mathbb{R}^n
         \overset{\simeq}{\longrightarrow}
       U \times_X E
       \,,
     $$

     for some $n \in \mathbb{N}$, where  $[U \times k^n \overset{pr_1}{\to} X]$ and $[U \times_X E \overset{pr_1}{\to} U]$ are regarded as a vector space objects in $Top_{U}$ in the canonical way.

It follows that $n \in \mathbb{N}$ is constant on [[connected components]]. Often this is required to be constant on all of $X$ and then called the _[[rank]]_ of the vector bundle.

A _[[homomorphism]]_ of topological vector bundles is simple a homomorphism of vector space objects in $Top_{/X}$.

Topological vector bundles over $X$ and homomorphisms between them constitutes a [[category]], usually denoted [[Vect(X)]].

=--

Notice that viewed in [[Top]], the last condition means that there is a [[diagram]] of the form

$$
  \array{
    U \times k^n
      &\overset{\simeq}{\longrightarrow}&
    U \times_X E
      &\overset{}{\longrightarrow}&
    E
    \\
    & \searrow & \downarrow &(pb)& \downarrow^{\mathrlap{\pi}}
    \\
    && U &\longrightarrow& X
  }
$$

where the square is a [[pullback square]] and the [[homeomorphism]] in the top left is fiber-wise linear.

If we say this yet more explicitly, it yields the definition as found in the traditional textbooks:


### In components


+-- {: .num_defn #TopologicalVectorBundle}
###### Definition
**(topological vector bundle in components)**

Let $X$ be a [[topological space]]. Then a _topological vector bundle_ over $X$ is

1. a [[topological space]] $E$;

1. a [[continuous function]] $E \overset{\pi}{\to} X$

1. for each $x \in X$ the stucture of a [[finite-dimensional vector space|finite-dimensional]] $k$-[[vector space]] on the [[pre-image]]

   $$E_x \coloneqq \pi^{-1}(\{x\}) \subset E$$

such that this is [[local trivialization|locally trivial]] in that there exists

1. an [[open cover]] $\{U_i \subset X\}_{i \in I}$,

1. for each $i \in I$ an $n_i \in \mathbb{N}$ and a [[homeomorphism]]

   $$
     \phi_i \;\colon\; U_i \times k^{n_i} \overset{\simeq}{\longrightarrow} \pi^{-1}(U_i) \subset E
   $$

   from the [[product topological space]] of $U_i$ with the [[real numbers]] (equipped with their [[Euclidean space]] [[metric topology]]) to the restriction of $E$ over $U_i$, such that

   1. $\phi_i$ is a map over $U_i$ in that $\pi \circ \phi_i = pr_1$, hence in that $\phi_i(\{x\} \times k^{n_i}) \subset \pi^{-1}(\{x\})$

   1. $\phi_i$ is a [[linear map]] in each fiber in that

      $$
        \underset{x \in U_i}{\forall}
        \left(
          \phi_i(x) \;\colon\;
             k^{n_i} \overset{\text{linear}}{\longrightarrow}
            E_x = \pi^{-1}(\{x\})
        \right)
        \,.
      $$

Often, but not always, it is required that the numbers $n_i$ are all equal
to some $n \in \mathbb{N}$, for
all $i \in I$, hence that the vector space fibers all have the same [[dimension]].
In this case one says that the vector bundle has _[[rank of a vector bundle|rank]]_ $n$.
(Over a [[connected topological space]] this is automatic, but the fiber dimension
may be distinct over distinct [[connected components]].)

For $[E_1 \overset{\pi_1}{\to} X]$ and $[E_2 \overset{\pi_2}{\to} X]$ two topological vector bundles over the same base space, then a _[[homomorphism]]_
between them is

* a [[continuous function]] $f \colon E_1 \longrightarrow E_2$

such that

1. $f$ respects the [[projections]]: $\pi_2 \circ f = \pi_1$;

1. for each $x \in X$ we have that $f|_x \colon (E_1)_x \to (E_2)_x$ is a [[linear map]].



=--

+-- {: .num_remark #TopologicalVectorBundlesCategory}
###### Remark
**([[Vect(X)|category of topological vector bundles]])**

For $X$ a [[topological space]], there is the [[category]] whose

* [[objects]] are the topological vector bundles over $X$,

* [[morphisms]] are the topological vector bundle homomorphisms

according to def. \ref{TopologicalVectorBundle}. This category usually denoted [[Vect(X)]].

We write $Vect(X)_{/\sim}$ for the [[set]] of [[isomorphism classes]] of this category.

=--














+-- {: .num_remark #TerminologyVectorBundles}
###### Remark
**(some terminology)**

Let $k$ and $n$ be as in def. \ref{TopologicalVectorBundle}. Then:

For $k = \mathbb{R}$ one speaks of _[[real vector bundles]]_.

For $k = \mathbb{C}$ one speaks of _[[complex vector bundles]]_.

For $n = 1$ one speaks of _[[line bundles]]_,
in particular of _[[real line bundles]]_ and of _[[complex line bundles]]_.

=--


+-- {: .num_remark #CommonOpenCoverLocalTrivialization}
###### Remark
**(any two topologial vector bundles have [[local trivialization]] over a common [[open cover]])**

Let $[E_1 \to X]$ and $[E_2 \to X]$ be two topological vector bundles (def. \ref{TopologicalVectorBundle}).
Then there always exists an [[open cover]] $\{U_i \subset X\}_{i \in I}$ such that both bundles
have a [[local trivialization]] over this cover.

=--

+-- {: .proof}
###### Proof

By definition we may find two possibly different
open covers $\{U^1_{i_1} \subset X\}_{{i_1} \in I_1}$ and $\{U^2_{i_2} \subset X\}_{i_2 \in I_2}$
with local tivializations
$\{ U^1_{i_1} \underoverset{\simeq}{\phi^1_{i_1}}{\to} E_1\vert_{U^1_{i_1}} \}_{i_1 \in I_1}$
and
$\{ U^2_{i_2} \underoverset{\simeq}{\phi^2_{i_2}}{\to} E_2\vert_{U^2_{i_2}} \}_{i_2 \in I_2}$.

The _joint [[refinement]]_ of these two covers is the open cover

$$
  \left\{
    U_{i_1, i_2}
      \coloneqq
    U^1_{i_1} \cap U^2_{i_2}
      \subset
    X
  \right\}_{(i_1, i_2) \in I_1 \times I_2}
  \,.
$$

The original local trivializations restrict to local trivializations on this finer cover

$$
  \left\{
    U_{i_1, i_2}
      \underoverset{\simeq}{\phi^1_{i_1}\vert_{U^2_{i_2}}}{\longrightarrow}
    E_1\vert_{U_{i_1, i_2}}
  \right\}_{(i_1, i_2) \in I_1 \times I_2}
$$

and

$$
  \left\{
    U_{i_1, i_2}
      \underoverset{\simeq}{\phi^2_{i_2}\vert_{U^1_{i_1}}}{\longrightarrow}
    E_2\vert_{U_{i_1, i_2}}
  \right\}_{(i_1, i_2) \in I_1 \times I_2}
  \,.
$$

=--


+-- {: .num_example #TrivialTopologicalVectorBundle}
###### Example
**(trivial topological vector bundle and (local) trivialization)**

For $X$ any [[topological space]], and $n \in \mathbb{N}$,
we have that the [[product topological space]]

$$
  X \times k^n \overset{pr_1}{\to} X
$$

canonically becomes a topological vector bundle over $X$ (def. \ref{TopologicalVectorBundle}). This is called the _[[trivial vector bundle]]_ of [[rank]] $n$ over $X$.

Given any topological vector bundle $E \to X$, then a choice of [[isomorphism]] to a trivial bundle (if it exists)

$$
  E \overset{\simeq}{\longrightarrow} X \times k^n
$$

is called a _trivialization_ of $E$. A vector bundle for which a trivialization exists is called _trivializable_.

Accordingly, the [[local trivialization|local triviality]] condition in the definition of topological vector bundles (def. \ref{TopologicalVectorBundle}) says that they are locally isomorphic to the trivial vector bundle. One also says that the data consisting of an open cover $\{U_i \subset X\}_{i \in I}$ and the [[homeomorphisms]]

$$
  \left\{
     U_i \times k^n
       \overset{\simeq}{\to}
     E|_{U_i}
  \right\}_{i \in I}
$$

as in def. \ref{TopologicalVectorBundle} constitute a _[[local trivialization]]_ of $E$.

=--

+-- {: .num_example #VectorBundleSections}
###### Example
**([[section]] of a [[topological vector bundle]])**

Let $E \overset{\pi}{\to} X$ be a topological vector bundle (def. \ref{TopologicalVectorBundle}).

Then a [[homomorphism]] of vector bundles from the [[trivial vector bundle|trivial]] [[line bundle]]
(example \ref{TrivialTopologicalVectorBundle}, remark \ref{TerminologyVectorBundles})

$$
  f \;\colon\; X \times k \longrightarrow E
$$

is, by fiberwise linearity, equivalently a [[continuous function]]

$$
  \sigma \;\colon\;  X \longrightarrow E
$$

such that $\pi \circ \sigma = id_X$;

$$
  f(x, c) = c \sigma(x)
$$

Such functions $\sigma \colon X \to E$ are called _[[sections]]_ (or _cross-sections_)
of the vector bundle $E$.

=--

+-- {: .num_example #TopologicalVetorSubbundle}
###### Example
**(topological vector sub-bundle)**

Given a topological vector bundel $E \to X$ (def. \ref{TopologicalVectorBundle}), then a _sub-bundle_ is a homomorphism of topological vector bundles over $X$

$$
  i\;\colon\; E' \hookrightarrow E
$$

such that for each point $x \in X$ this is a linear embedding of fibers

$$
  i|_x \;\colon\; E'_x \hookrightarrow E_x
  \,.
$$

(This is a [[monomorphism]] in the [[category]] $Vect(X)$ of topological vector bundles over $X$.)

=--


### Transition functions and Cech cohomology
 {#TransitionFunctionsAndCechCohomology}

We discuss how topological vector bundles are equivalently given by [[cocycles]] in [[Cech cohomology]]
constituted by their [[transition functions]].

+-- {: .num_defn #ContinuousFunctionWithValuesInGLn}
###### Definition
**([[continuous functions]] on [[open subsets]] with values in the [[general linear group]])**

For $n \in \mathbb{N}$, regard the [[general linear group]] $GL(n,k)$
as a [[topological group]] with its standard [[topological space|topology]],
given as the [[Euclidean space|Euclidean]] [[subspace topology]]
via $GL(n,k) \subset Mat_{n \times n}(k) \simeq k^{(n^2)}$ or as the
or as the subspace topology $GL(n,k) \subset Maps(k^n, k^n)$ of the [[compact-open topology]] on the [[mapping space]].
(That these topologies coincide is the statement of [this prop.](general+linear+group#AsSubspaceOfTheMappingSpace).

For $X$ a [[topological space]], we write

$$
  \underline{GL(n,k)}
    \;\colon\;
  U \mapsto Hom_{Top}(U, GL(n,k) )
$$

for the assignment that sends an [[open subset]] $U \subset X$ to the [[set]] of [[continuous functions]]
$g \colon U \to GL(n,k)$ (for $U \subset X$ equipped with its [[subspace topology]]), regarded as a
[[group]] via the pointwise group operation in $GL(n,k)$:

$$
   g_1 \cdot g_2 \;\colon\; x \mapsto g_1(x) \cdot g_2(x)
   \,.
$$

Moreover, for $U' \subset U \subset X$ an inclusion of open subsets, and for
$g \in \underline{GL(n,k)}(U)$, we write

$$
  g|_{U'} \in \underline{GL(n,k)}(U')
$$

for the restriction of the continuous function from $U$ to $U'$.

=--

+-- {: .num_remark}
###### Remark
**([[sheaf]] of [[groups]])**

In the language of [[category theory]] the assignment $\underline{GL(n,k)}$
from def. \ref{ContinuousFunctionWithValuesInGLn} of continuous functions to open subsets
and the restriction operations between these is called a _[[sheaf]] of groups
on the [[site of open subsets]]_ of $X$.

=--

+-- {: .num_defn #TransitionFunctions}
###### Definition
**([[transition functions]])

Given a topological vector bundle $E \to X$ as in def. \ref{TopologicalVectorBundle} and a choice of [[local trivialization]]
$\{\phi_i \colon U_i \times k^n \overset{\simeq}{\to} E|_{U_i}\}$ (example \ref{TrivialTopologicalVectorBundle})
there are for $i,j \in I$ induced [[continuous functions]]

$$
  \left\{
    g_{i j} \;\colon\; (U_i \cap U_j) \longrightarrow GL(n, k)
  \right\}_{i,j \in I}
$$

to the [[general linear group]] (as in def. \ref{ContinuousFunctionWithValuesInGLn})
given by composing the local trivialization isomorphisms:

$$
  \array{
    (U_i \cap U_j) \times k^n
      &\overset{ \phi_i|_{U_i \cap U_j} }{\longrightarrow}&
    E|_{U_i \cap U_j}
      &\overset{ \phi_j^{-1}\vert_{U_i \cap U_j} }{\longrightarrow}&
    (U_i \cap U_j) \times k^n
    \\
    (x,v) && \overset{\phantom{AAA}}{\mapsto} && \left( x, g_{i j}(x)(v) \right)
  }
  \,.
$$

These are called the _[[transition functions]]_ for the given local trivialization.

=--

These functions satisfy a special property:

+-- {: .num_defn #CocycleCech}
###### Definition
**([[Cech cohomology|Cech]] [[cocycles]])**

Let $X$ be a [[topological space]].

A _normalized [[Cech cohomology|Cech cocycle]] of degree 1 with [[coefficients]]_
in $\underline{GL(n,k)}$ (def. \ref{ContinuousFunctionWithValuesInGLn})  is

1. an [[open cover]] $\{U_i \subset X\}_{i \in I}$

1. for all $i,j \in I$ a continuous function $g_{i j} \colon U_i \cap U_j \to GL(n,k)$ as in def. \ref{ContinuousFunctionWithValuesInGLn}

such that

1. (normalization) $\underset{i \in I}{\forall}\left( g_{i i} = const_1  \right)  $ (the [[constant function]] on the [[neutral element]] in $GL(n,k)$),

1. (cocycle condition) $\underset{i,j \in I}{\forall}\left(  g_{j k} \cdot g_{i j}  = g_{i k}\;\;\text{on}\, U_i \cap U_j \cap U_k\right)$.


Write

$$
  C^1(X, \underline{GL(n,k)}  )
$$

for the set of all such cocycles for given $n \in \mathbb{N}$ and write

$$
  C^1( X, \underline{GL}(k) )
    \;\coloneqq\;
  \underset{n \in \mathbb{N}}{\sqcup}
   C^1(X, \underline{GL(n,k)})
$$

for the [[disjoint union]] of all these cocycles as $n$ varies.



=--


+-- {: .num_example #CocycleCechTransitionFunction}
###### Example
**([[transition functions]] are [[Cech cohomology|Cech]] [[cocycles]])**

Let $E \to X$ be a topological vector bundle (def. \ref{TopologicalVectorBundle}) and let $\{U_i \subset X\}_{i \in I}$, $\{\phi_i \colon U_i \times k^n \overset{\simeq}{\to} E|_{U_{i}}\}_{i \in I}$ be a local trivialization (example \ref{TrivialTopologicalVectorBundle}).

Then the set of induced [[transition functions]] $\{g_{i j} \colon U_i \cap U_j \to GL(n)\}$ according to def. \ref{TransitionFunctions}
is a _normalized Cech cocycle on $X$ with coefficients in $\underline{GL(k)}$_, according to def. \ref{CocycleCech}.

=--

+-- {: .proof}
###### Proof

This is immediate from the definition:

$$
  \begin{aligned}
    g_{i i }(x)
      & =
      \phi_i^{-1} \circ \phi_i(x,-)
      \\
      & = id_{k^n}
  \end{aligned}
$$

and

$$
  \begin{aligned}
    g_{j k}(x) \cdot g_{i j}(x)
      & =
    \left(\phi_k^{-1} \circ \phi_j\right) \circ \left(\phi_j^{-1}\circ \phi_i\right)(x,-)
    \\
      & =
    \phi_k^{-1} \circ \phi_i(x,-)
    \\
    & =
    g_{i k}(x)
  \end{aligned}
  \,.
$$

=--


Conversely:

+-- {: .num_example #TopologicalVectorBundleFromCechCocycle}
###### Example
**(topological vector bundle constructed from a [[Cech cohomology|Cech]] [[cocycle]])

Let $X$ be a [[topological space]]
and let $c \in C^1(X, \underline{GL(k)})$ a Cech cocycle on $X$ according to def. \ref{CocycleCech},
with open cover $\{U_i \subset X\}_{i \in I}$ and component functions $\{g_{i j}\}_{i,j \in I}$.

This induces an [[equivalence relation]] on the [[product topological space]]

$$
  \left(
    \underset{i \in I}{\sqcup} U_i
  \right)
  \times
  k^n
$$

(of the [[disjoint union space]] of the patches $U_i \subset X$ regarded as [[topological subspaces]]
with the [[product space]] $k^n = \underset{\{1,\cdots, n\}}{\prod} k$) given by

$$
  \big(
    ((x,i), v)
     \;\sim\;
    ((y,j), w)
  \big)
   \;\Leftrightarrow\;
  \left(
     (x = y)
       \;\text{and}\;
     (g_{i j}(x)(v) = w)
  \right)
  \,.
$$

Write

$$
  E(c)
   \;\coloneqq\;
  \left(
    \left(
      \underset{i \in I}{\sqcup} U_i
    \right)
      \times
    k^n
  \right)
  /
  \left(
     \left\{
        g_{i j}
     \right\}_{i,j \in I}
  \right)
$$

for the resulting [[quotient topological space]]. This comes with the evident projection

$$
  \array{
    E(c) &\overset{\phantom{AA}\pi \phantom{AA}}{\longrightarrow}& X
    \\
    [(x,i,),v] &\overset{\phantom{AAA}}{\mapsto}& x
  }
$$

which is a [[continuous function]] (by the [[universal property]] of the [[quotient topological space]] construction, since the corresponding continuous [[function]] on the un-quotientd disjoint union space respects the equivalence relation). Moreover, each [[fiber]] of this map is identified with $k^n$, and hence canonicaly carries the structure of a [[vector space]].

Finally, the quotient co-projections  constitute a local trivialization of this vector bundle over the given open cover.

Therefore $E(c) \to X$ is a topological vector bundle (def. \ref{TopologicalVectorBundle}). We say it is the topological vector bundle _glued from the transition functions_.

=--

+-- {: .num_remark}
###### Remark
**(bundle glued from [[Cech cohomology|Cech]] [[cocycle]] is a [[coequalizer]])**

Stated more [[category theory|category theoretically]], the constructure of a topological vector bundle from Cech cocycle data in example \ref{TopologicalVectorBundleFromCechCocycle} is a [universal construction in topological spaces](Top#UniversalConstructions), namely the [[coequalizer]] of the two morphisms

$$i, \mu: \underset{i j}{\sqcup} (U_i \cap U_j) \times V \overset{\to}{\to} \underset{i}{\sqcup} U_i \times V$$

in the category of vector space objects in the slice category $Top/X$. Here the restriction of $i$ to the coproduct summands is induced by inclusion:

$$(U_i \cap U_j) \times V \hookrightarrow U_i \times V \hookrightarrow \underset{i}{\sqcup} U_i \times V$$

and the restriction of $\mu$ to the coproduct summands is
via the action of the transition functions:

$$(U_i \cap U_j) \times V \overset{(\langle incl, g_{i j} \rangle) \times V}{\to} U_j \times GL(V) \times V \overset{action}{\to} U_j \times V \hookrightarrow \underset{j}{\sqcup} U_j \times V$$

=--

In fact, extracting transition functions from a vector bundle by def. \ref{TransitionFunctions} and constructing a vector bundle from Cech coycle data as above are operations that are inverse to each other, up to [[isomorphism]].

+-- {: .num_prop #FromTransitionFunctionsReconstructVectorBundle}
###### Proposition
**(topological vector bundle reconstructed from its [[transition functions]])**

Let $[E \overset{\pi}{\to} X]$ be a [[topological vector bundle]] (def. \ref{TopologicalVectorBundle}),
let $\{U_i \subset X\}_{i \in I}$ be an [[open cover]] of the base space, and
let $\left\{  U_i \times k^n \underoverset{\simeq}{\phi_i}{\longrightarrow} E|_{U_i}  \right\}_{i \in I}$
be a [[local trivialization]].

Write

$$
  \left\{ g_{i j} \coloneqq  \phi_j^{-1}\circ \phi_i  \colon U_i \cap U_j \to GL(n,k) \right\}_{i,j \in I}
$$

for the corresponding [[transition functions]] (def. \ref{TransitionFunctions}). Then there is an
[[isomorphism]] of vector bundles over $X$

$$
  \left(
    \left(
      \underset{i \in I}{\sqcup} U_i
    \right)
      \times
    k^n
  \right)
  /
  \left(
     \left\{
        g_{i j}
     \right\}_{i,j \in I}
  \right)
    \;\underoverset{\simeq}{(\phi_i)_{i \in I}}{\longrightarrow}\;
  E
$$

from the vector bundle glued from the transition functions according to def. \ref{TransitionFunctions} to the original bundle $E$,
whose components are the original local trivialization isomorphisms.

=--

+-- {: .proof}
###### Proof

By the [[universal property]] of the [[disjoint union space]] ([[coproduct]] in [[Top]]),
continuous functions out of them are equivalently sets of continuous functions out of every
summand space. Hence the set of local trivializations $\{U_i \times k^n \underoverset{\simeq}{\phi_i}{\to} E|_{U_i} \subset E\}_{i \in I}$
may be collected into a single [[continuous function]]

$$
    \underset{i \in I}{\sqcup} U_i
     \times
   k^n
   \overset{(\phi_i)_{i \in I}}{\longrightarrow }
   E
   \,.
$$

By construction this function respects the [[equivalence relation]] on the disjoint union space given by
the transition functions, in that for each $x \in U_i \cap U_j$ we have

$$
  \phi_i((x,i),v)
  =
  \phi_j \circ \phi_j^{-1} \circ \phi_i((x,i),v)
  =
  \phi_j \circ ((x,j),g_{i j}(x)(v))
  \,.
$$

By the [[universal property]] of the [[quotient space]] coprojection this means that $(\phi_i)_{i \in I}$
uniquely [[extension|extends]] to a [[continuous function]] on the quotient space such that the
following [[commuting diagram|diagram commutes]]

$$
  \array{
    \left(
      \underset{i \in I}{\sqcup} U_i
    \right)
      \times
    k^n
    &\overset{(\phi_i)_{i \in I}}{\longrightarrow}&
  E
  \\
  \downarrow  & \nearrow_{\exists !}
  \\
  \left(
    \left(
      \underset{i \in I}{\sqcup} U_i
    \right)
      \times
    k^n
  \right)
  /
  \left(
     \left\{
        g_{i j}
     \right\}_{i,j \in I}
  \right)
  }
  \,.
$$

It is clear that this continuous function is a [[bijection]]. Hence to show that it is a
[[homeomorphism]], it is now sufficient to show that this is an [[open map]] (by [this prop.](Introduction+to+Topology+--+1#HomeoContinuousOpenBijection)).

So let $O$  be an subset in the quotient space which is open. By definition of the
[[quotient topology]] this means equivalently that its restriction $O_i$ to $U_i \times k^n$
is open for each $i \in I$. Since the $\phi_i$ are homeomorphsms, it follows that the
images $\phi_i(O_i)  \subset  E\vert_{U_ i}$ are open.
By the nature of the [[subspace topology]], this means that these images are open also in $E$.
Therefore also the union $f(O) = \underset{i \in I}{\cup} \phi_i(O_i)$ is open.

=--

+-- {: .num_defn #CoboundaryCech}
###### Definition
**([[coboundary]] between [[Cech cohomology|Cech]] [[cocycles]] )

Let $X$ be a [[topological space]] and let $c_1, c_2 \in C^1(X, \underline{GL(k)})$ be two [[Cech cohomology|Cech]] [[cocycles]]
(def. \ref{CocycleCech}), given by

1. $\{U_i \subset X\}_{i \in I}$ and $\{U'_i \subset X\}_{i' \in I'}$ two [[open covers]],

1. $\{g_{i j} \colon U_i \cap U_j \to GL(k,n_)\}_{i,j \in I}$ and $\{g_'_{i',j'} \colon U'_{i'} \cap U'_{j'} \to GL(n',k) \}_{i', j'}$  the corrsponding component functions.


Then a _[[coboundary]]_  between these two cocycles is

1. the condition that $n = n'$,

1. an [[open cover]] $\{V_\alpha \subset X\}_{\alpha \in A}$,

1. [[functions]] $\phi \colon A \to I$ and $\phi' \colon A \to J$ such that $\underset{\alpha \in A}{\forall}\left( \left( V_\alpha \subset U_{\phi(\alpha)} \right) \,\text{and}\, \left( V_\alpha \subset U'_{\phi'(\alpha)} \right) \right)$

1. a set $\{ \kappa_\alpha \colon V_\alpha \to  GL(n,k) \}$ of continuous functions as in def. \ref{CocycleCech}

such that

* $\underset{ \alpha, \beta \in A }{\forall} \left(  \kappa_{\beta} \cdot g_{\phi(\alpha) \phi(\beta)}  = g'_{\phi'(\alpha) \phi'(\beta)} \cdot \kappa_{\alpha} \,\, \text{on}\,\, V_\alpha \cap V_\beta \right) $,

  hence such that the following [[diagrams]] of [[linear maps]] [[commuting diagram|commute]] for all $\alpha, \beta \in A$ and $x \in V_{\alpha} \cap V_\beta$:

  $$
    \array{
      k^n  &\overset{ g_{\phi(\alpha) \phi(\beta)}(x) }{\longrightarrow}& k^n
      \\
      {}^{\mathllap{\kappa_{\alpha}(x)} }\downarrow && \downarrow^{\mathrlap{ \kappa_{\beta}(x) }}
      \\
      k^n  &\underset{ g'_{\phi'(\alpha) \phi'(\beta)}(x) }{\longrightarrow}& k^n
    }
    \,.
  $$


Say that two Cech cocycles are _cohomologous_ if there exists a coboundary between them.


=--

+-- {: .num_example #FinerCoverCech}
###### Example
**([[refinement]] of a [[Cech  cohomology|Cech]] [[cocycle]] is a [[coboundary]])**

Let $X$ be a [[topological space]] and let $c \in C^1(X, \underline{GL(k)})$ be a Cech cocycle as in def. \ref{CocycleCech},
with respect to some open cover $\{U_i \subset X\}_{i \in I}$ given by component functions $\{g_{i j}\}_{i,j \in I}$.

Then for $\{V_\alpha \subset X\}_{\alpha \in A}$ a [[refinement]] of the given open cover, hence an open cover such that
there exists a [[function]] $\phi \colon A \to I$ with $\underset{\alpha \in A}{\forall}\left( V\alpha \subset U_{\phi(\alpha)}  \right)$,
then

$$
  g'_{ \alpha \beta }
  \coloneqq g_{\phi(\alpha) \phi(\beta)}
  \colon V_\alpha \cap V_\beta
    \longrightarrow
  GL(n,k)
$$

are the components of a Cech cocycle $c'$ which is cohomologous to $c$.


=--

+-- {: .num_prop #CechCoboundaryFromIsomorphismBetweenVectoreBundles}
###### Proposition
**([[isomorphism]] of topological vector bundles induces [[Cech cohomology|Cech]] [[coboundary]] between their [[transition functions]])**

Let $X$ be a topological space, and let $c_1, c_2 \in C^1(X, \underline{GL(n,k)}  )$ be two Cech cocycles as in def. \ref{CocycleCech}.

Every [[isomorphism]] of topological vector bundles

$$
  f
    \;\colon\;
  E(c_1)
    \overset{\simeq}{\longrightarrow}
  E(c_2)
$$

between the vector bundles glued from these cocycles according to def. \ref{TopologicalVectorBundleFromCechCocycle}
induces a coboundary between the two cocycles,

$$
  c_1 \sim c_2
  \,,
$$

according to def. \ref{CoboundaryCech}.

=--

+-- {: .proof}
###### Proof

By example \ref{FinerCoverCech} we may assume without restriction that the two Cech cocycles are
defined with respect to the same open cover $\{U_i \subset X\}_{i \in I}$ (for if they are not, then both are cohomologous to
cocycles on a joint refinement of the original covers and we may argue with these).

Accordingly, by example \ref{TopologicalVectorBundleFromCechCocycle} the two bundles $E(c_1)$ and $E(c_2)$
both have local trivializations of the form

$$
  \{ U_i \times k^n \underoverset{\simeq}{\phi^1_i}{\longrightarrow} E(c_1)\vert_{U_i}\}
$$

and

$$
  \{ U_i \times k^n \underoverset{\simeq}{\phi^2_i}{\longrightarrow} E(c_2)\vert_{U_i}\}
$$

over this cover.  Consider then for $i \in I$ the function

$$
  f_i \coloneqq  (\phi_i^2)^{-1}\circ f\vert_{U_i} \circ  \phi^1_i
  \,,
$$

hence the unique function making the following [[commuting diagram|diagram commute]]:

$$
  \array{
    U_i \times k^n &\underoverset{\simeq}{\phi^1_i}{\longrightarrow}& E(c_1)\vert_{U_i}
    \\
    {}^{\mathllap{f_i}}\downarrow && \downarrow^{\mathrlap{ f }}
    \\
    U_i \times k^n &\underoverset{\phi^2_i}{\simeq}{\longrightarrow}& E(c_2)\vert_{U_i}
  }
  \,.
$$

This induces for all $i,j \in I$ the following composite commuting diagram

$$
  \array{
    (U_i \cap U_j) \times k^n
      &\underoverset{\simeq}{\phi^1_i}{\longrightarrow}&
    E(c_1)\vert_{U_i \cap U_j}
      & \underoverset{\simeq}{(\phi^1_j)^{-1}}{\longrightarrow}  &
    (U_i \cap U_j) \times k^n
    \\
    {}^{\mathllap{f_i}}\downarrow
      &&
    \downarrow^{\mathrlap{ f }}
      &&
    \downarrow^{\mathrlap{ f_j }}
    \\
    (U_i \cap U_j) \times k^n
      &\underoverset{\phi^2_i}{\simeq}{\longrightarrow}&
    E(c_2)\vert_{U_1 \cap U_2}
      &\underoverset{(\phi^2_j)^{-1}}{\simeq}{\longrightarrow}&
    (U_i \cap U_j) \times k^n
  }
  \,.
$$

By construction, the two horizonal composites of this diagram are pointwise
given by the components $g^1_{i j}$ and $g^2_{i j}$of the cocycles $c_1$ and $c_2$, respectively.
Hence the commutativity of this
diagram is equivalently the commutativity of these diagrams:

  $$
    \array{
      k^n  &\overset{ g^1_{i j}(x) }{\longrightarrow}& k^n
      \\
      {}^{\mathllap{ f_i(x) } }\downarrow && \downarrow^{\mathrlap{ f_j(x) }}
      \\
      k^n  &\underset{ g^2_{ i j }(x) }{\longrightarrow}& k^n
    }
    \,.
  $$

for all $i,j \in I$ and $x  \in U_i \cap U_j$. By def. \ref{CoboundaryCech} this exhibits the required coboundary.

=--

+-- {: .num_defn #CohomologyCech}
###### Definition
**([[Cech cohomology]])**

Let $X$ be a [[topological space]]. The relation $\sim$ on [[Cech cohomology|Cech cocycles]]
of being cohomologous (def. \ref{CoboundaryCech})
is an [[equivalence relation]] on the set $C^1( X, \underline{GL(k)} )$ of [[Cech cohomology|Cech]] [[cocycles]] (def. \ref{CocycleCech}).

Write

$$
  H^1(X, \underline{GL(k)} )
   \;\coloneqq\;
  C^1(X, \underline{GL(k)} )/\sim
$$

for the resulting set of [[equivalence classes]]. This is called the
_[[Cech cohomology]] of $X$ in degree 1 with [[coefficients]] in $\underline{GL(k)}$.


=--

+-- {: .num_prop}
###### Proposition
**(degree-1 [[Cech cohomology]] computes [[topological vector bundles]])

Let $X$ be a [[topological space]].

The construction of gluing a topological vector bundle from a Cech cocycle (example \ref{TopologicalVectorBundleFromCechCocycle})
constitutes a [[natural bijection|bijection]]
between the degree-1 Cech cohomology of $X$ with coefficients in $GL(n,k)$ (def. \ref{CohomologyCech})
and the set of [[isomorphism classes]] of topological vector bundles on $X$ (def. \ref{TopologicalVectorBundle}, remark \ref{TopologicalVectorBundlesCategory}):

$$
  \array{
    H^1(X,\underline{GL(k)})
      &\overset{\phantom{AA}\simeq \phantom{AA}}{\longrightarrow}&
    Vect(X)_{/\sim}
    \\
    c &\overset{\phantom{AAA}}{\mapsto}& E(c)
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

First we need to see that the function is well defined, hence that if
cocycles $c_1, c_2 \in C^1(X,\underline{GL(k)})$ are
related by a coboundary, $c_1 \sim c_2$ (def. \ref{CoboundaryCech}),
then the vector bundles $E(c_1)$ and $E(c_2)$ are related by an isomorphism.

Let $\{V_\alpha \subset X\}_{\alpha \in A}$ be the open cover with respect to which the coboundary
$\{\kappa_\alpha \colon V_\alpha \to GL(n,k)\}_{\alpha}$ is defined, with refining functions
$\phi \colon A \to I$ and $\phi' \colon A \to I'$.  Let
$\left\{ \mathbb{R}^n \underoverset{\simeq}{\psi_{\phi(\alpha)}\vert_{V_\alpha}  }{\to} E(c_1)\vert_{V_\alpha} \right\}_{\alpha \in A}$
and $\left\{ V_\alpha \times k^n \underoverset{\simeq}{\psi'_{\phi'(\alpha)}\vert_{V_\alpha}  }{\to} E(c_2)\vert_{V_\alpha} \right\}_{\alpha \in A}$
be the corresponding restrictions of the canonical local trivilizations of the two glued bundles.

For $\alpha \in A$ define

$$
  f_\alpha \coloneqq \psi'_{\phi'(\alpha)}\vert_{V_\alpha}  \circ \kappa_\alpha \circ (\psi_{\phi(\alpha)}\vert_{V_\alpha}  )^{-1}
  \phantom{AAAA}
    \text{hence:}
  \phantom{AAA}
  \array{
    V_\alpha \times k^n
     &\overset{ \psi_{\phi(\alpha)}\vert_{V_\alpha} }{\longrightarrow}&
    E(c_1)\vert_{V_\alpha}
    \\
    {}^{\mathllap{\kappa_\alpha}}\downarrow && \downarrow^{\mathrlap{f_\alpha}}
    \\
    V_\alpha \times k^n
     &\overset{ (\psi'_{\phi'(\alpha)}\vert_{V_\alpha})^{-1} }{\longleftarrow}&
    E(c_1)\vert_{V_\alpha}
  }
  \,.
$$

Observe that for $\alpha, \beta \in A$ and $x \in V_\alpha \cap V_\beta$ the coboundary condition
implies that

$$
  f_\alpha\vert_{V_\alpha \cap V_\beta}
  \;=\;
  f_\beta\vert_{V_\alpha \cap V_\beta}
$$

because in the diagram

$$
  \array{
    k^n &\overset{ g_{\phi(\alpha) \phi(\beta) }(x) }{\longrightarrow}& k^n
    \\
    {}^{\mathllap{\kappa_\alpha(x)}}\downarrow
      &&
    \downarrow^{\mathrlap{\kappa_{\beta}(x)}}
    \\
    k^n &\underset{g'_{\phi'(\alpha) \phi'(\beta)}(x)  }{\longrightarrow}& k^n
  }
  \phantom{AAAAA}
    =
  \phantom{AAAAA}
  \array{
    k^n
      &\overset{ \psi_{\phi(\alpha)}(x) }{\longrightarrow}&
    E(c_1)_x
      &\overset{ (\psi_{\phi(\beta)})^{-1}(x) }{\longrightarrow}&
    k^n
     \\
    {}^{\mathllap{\kappa_\alpha(x)}}\downarrow
      &&
    \downarrow^{\mathrlap{\exists !} }
      &&
    \downarrow^{\mathrlap{\beta_\alpha(x)}}
    \\
    k^n
      &\overset{ \psi'_{\phi'(\alpha)}(x) }{\longrightarrow}&
    E(c_2)_x
      &\overset{ (\psi'_{\phi'(\beta)})^{-1}(x) }{\longrightarrow}&
    k^n
 }
$$

the vertical morphism in the middle on the right is unique, by the fact that all other
morphisms in the diagram on the right are invertible.

Therefore there is a unique vector bundle homomorphism

$$
  f\;\colon\; E(c_1) \to E(c_2)
$$

given for all $\alpha \in A$ by $f\vert_{V_\alpha} = f_\alpha$. Similarly there is a unique vector bundle
homomorphism

$$
  f^{-1}\;\colon\; E(c_2) \to E(c_1)
$$

given for all $\alpha \in A$ by $f^{-1}\vert_{V_\alpha} = f^{-1}_\alpha$.
Hence this is the required vector bundle isomorphism.

Finally to see that the function from Cech cohomology classes to isomorphism classes of vector
bundles thus defined is a bijection:

By prop. \ref{FromTransitionFunctionsReconstructVectorBundle} the function is [[surjective function|surjective]],
and by prop. \ref{CechCoboundaryFromIsomorphismBetweenVectoreBundles} it is injective.

=--

$\,$


## Examples
 {#Examples}

+-- {: .num_example #TautologicalLineBundle}
###### Example
**([[tautological line bundle]])**

For $n \in \mathbb{N}$ then the [[projective space]] $k P^n$
carries the _[[tautological line bundle]]_ whose fiber over the $k$-line $[v] \in k P^n$
is that $k$-line.

For details see [there](tautological+line+bundle#AsAtopologicalLieBundle)

=--


+-- {: .num_example}
###### Example
**([[cylinder]])**

Let

$$
  S^1
    =
  \left\{
    (x,y)
     \;\vert\;
     x^2 + y^2 = 1
  \right\}
  \;\subset\,
  \mathbb{R}^2
$$

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/cylinder.jpg" width="190">
</div>

be the [[circle]] with its  [[Euclidean space|Euclidean]] [[subspace]] [[metric topology]].

Then the [[trivial vector bundle|trivial]] [[real vector bundle|real]] [[line bundle]] on the circle is the the [[cylinder]]

$$
  S^1 \times \mathbb{R}
$$


=--

+-- {: .num_example #MoebiusStrip}
###### Example
**([[Moebius strip]])**

Let

$$
  S^1
    =
  \left\{
    (x,y)
     \;\vert\;
     x^2 + y^2 = 1
  \right\}
  \;\subset\,
  \mathbb{R}^2
$$

be the  [[circle]] with its  [[Euclidean space|Euclidean]] [[subspace]] [[metric topology]].
Consider the [[open cover]]

$$
  \left\{
    U_n \subset S^1
  \right\}_{n \in \{0,1,2\}}
$$

with

$$
  U_n \coloneqq \left\{ (cos(\alpha), sin(\beta)) \;\vert\; n \frac{2 \pi }{3} - \epsilon \lt \alpha \lt (n+1) \frac{2\pi }{3} + \epsilon  \right\}
$$

for any $\epsilon \in (0,2\pi/6)$.


Define a [[Cech cohomology]] cocycle (remark \ref{CechCoycleCondition}) on this cover by

$$
  g_{n_1 n_2} =
  \left\{
    \array{
      const_{-1} & \vert & (n_1,n_2) = (0,2)
      \\
      const_{-1} &\vert& (n_1,n_2) = (2,0)
      \\
      const_1 &\vert& \text{otherwise}
    }
  \right.
$$

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/moebiusstrip.jpg" width="200">
</div>

Since there are no non-trivial triple intersections, all cocycle conditions are
evidently satisfied.

Accordingly by example \ref{TopologicalVectorBundleFromCechCocycle} these functions define a vector bundle.
This is the _[[Moebius strip]]_

=--

+-- {: .num_example }
###### Example
**([[basic complex line bundle on the 2-sphere]])**

Let

$$
  S^2
    \coloneqq
  \left\{
    (x,y,z)
    \;\vert\;
    x^2 + y^2 + z^2 = 1
  \right\}
    \subset
  \mathbb{R}^3
$$

be the [[2-sphere]] with its [[Euclidean space|Euclidean]] [[subspace]] [[metric topology]].
Let

$$
  \left\{
    U_{i} \subset S^2
  \right\}_{i \in \{+,-\}}
$$

be the two [[complements]] of antipodal points

$$
  U_\pm \coloneqq S^2 \setminus \{(0, 0, \pm 1)\}
  \,.
$$

Define continuous functions

$$
  \array{
    U_+ \cap U_-
      &\overset{g_{\pm \mp}}{\longrightarrow}&
    GL(1,\mathbb{C})
    \\
    ( \sqrt{1-z^2} \, cos(\alpha), \sqrt{1-z^2} \, sin(\alpha), z)
      &\mapsto&
    \exp(\pm 2\pi i \alpha)
  }
  \,.
$$

Since there are no non-trivial triple intersections, the only cocycle condition is

$$
  g_{\mp \pm} g_{\pm \mp} = g_{\pm \pm} = id
$$

which is clearly satisfied.

The [[complex line bundle]] this defined is called the _[[basic complex line bundle on the 2-sphere]]_.

With the 2-sphere identified with the [[complex projective space]] $\mathbb{C} P^1$
(the [[Riemann sphere]]),
the basic complex line bundle is the [[tautological line bundle]] (example \ref{TautologicalLineBundle}) on $\mathbb{C}P^1$.

=--

+-- {: .num_example #ClutchingConstruction}
###### Example
**([[clutching construction]])**

Generally, for $n \in \mathbb{N}$, $n \geq 1$ then the [[n-sphere]]
$S^n$ may be covered by two open [[hemispheres]] intersecting in an
[[equator]] of the form $S^{n-1} \times (-\epsilon, \epsilon)$.
A vector bundle is then defined by specifying a single function

$$
  g_{+-}
  \;\colon\;
  S^{n-1} \longrightarrow GL(n,k)
  \,.
$$

This is called the _[[clutching construction]]_ of vector bundles over [[n-spheres]].

=--


+-- {: .num_example}
###### Example
**([[tangent bundle]])**

For $X$ the [[topological space]] underlyithe ng a [[differentiable manifold]] then its [[tangent bundle]]
$T X$ is a [[real vector bundle]] over $X$ whose [[rank of a vector bundle|rank]] is the [[dimension]] of $X$.

=--

+-- {: .num_example}
###### Example
**([[normal bundle]])**

For $i X \hookrightarrow Y$ an [[embedding of differentiable manifolds]], then
the _[[normal bundle]]_

$$
  N_i X \coloneqq T Y/T X
$$

is the real vector bundle over $Y$ whose [[fiber]] at $x \in X$ is the [[quotient vector space]]
$(N_i X)_x \coloneqq T_{i(x)} Y / T_x X$.

=--


## Properties



### Basic properties
 {#BasicProperties}

+-- {: .num_lemma #FiberwiseIsoisIsomorphismOfVectorBundles}
###### Lemma
**(homomorphism of vector bundles is isomorphism as soon as it is a fiberwise isomorphism)**

Let $[E_1 \to X]$ and $[E_2 \to X]$ be two topological vector bundles (def. \ref{TopologicalVectorBundle}).

If a [[homomorphism]] of vector bundles $f \colon E_1 \longrightarrow E_2$
restricts on the [[fiber]] over each point to a linear isomorphism

$$
  f\vert_x \;\colon\; (E_1)_x \overset{\simeq}{\longrightarrow} (E_2)_x
$$

then $f$ is already an isomorphism of vector bundles.

=--


+-- {: .proof}
###### Proof

It is clear that $f$ has an [[inverse function]]
of underlying sets $f^{-1} \colon E_2 \to _E_1$ which is a function over $X$: Over each $x \in X$
it it the linear inverse $(f\vert_x)^{-1} \colon (E_2)_x \to (E_1)_x$.

What we need to show is that this is a continuous function.

By remark \ref{CommonOpenCoverLocalTrivialization} we find an open cover $\{U_i \subset X\}_{i \in I}$ over which
both bundles have a local trivialization.


$$
  \left\{ U_i \underoverset{\simeq}{\phi^1_i}{\to} (E_1)\vert_{U_i}\right\}_{i \in I}
  \phantom{AA}
  \text{and}
  \phantom{AA}
  \left\{ U_i \underoverset{\simeq}{\phi^2_i}{\to} (E_2)\vert_{U_i} \right\}_{i \in I}
  \,.
$$

Restricted to any patch $i \in I$ of this cover, the homomorphism $f|_{U_i}$ induces a homomorphism
of  [[trivial vector bundles]]

$$
  f_i \coloneqq \phi^2_j^{-1} \circ f \circ \phi^1_i
   \phantom{AAAAAA}
  \array{
    U_i \times k^n &\underoverset{\simeq}{\phi^1_i}{\longrightarrow}& (E_1)\vert|_{U_i}
    \\
    {}^{f_i}\downarrow && \downarrow^{\mathrlap{f\vert_{U_i}}}
    \\
    U_i \times k^n &\underoverset{\phi^2_i}{\simeq}{\longrightarrow}& (E_2)\vert_{U_j}
  }
  \,.
$$

Also the $f_i$ are fiberwise invertible, hence are
continuous bijections. We claim that these are [[homeomorphisms]], hence that their
inverse functions $(f_i)^{-1}$ are also continuous.

To this end we re-write the $f_i$ a little. First observe that by the [[universal property]]
of the [[product topological space]] and since they fix the base space $U_i$, the $f_i$ are equivalently given by
a continuous function

$$
   h_i \;\colon\; U_i \times k^n \longrightarrow k^n
$$

as

$$
  f_i(x,v) = (x, h_i(x,v))
  \,.
$$

Moreovern since $k^n$ is [[locally compact topological space|locally compact]] (like every [[finite dimensional vector space]], by the [[Heine-Borel theorem]]),
the [[mapping space]] [[adjunction]] says (by [this prop.](Introduction+to+Topology+--+1#UniversalPropertyOfMappingSpace)) that there is a continuous function

$$
  \tilde h_i
    \;\colon\;
  U_i \longrightarrow Maps(k^n, k^n)
$$

(with $Maps(k^n,k^n)$ the set of continuous functions $k^n \to k^n$ equipped with the [[compact-open topology]])
which factors $h_i$ via the [[evaluation]] map as

$$
  h_i
    \;\colon\;
  U_i \times k^n
    \overset{\tilde h_i \times id_{k^n}}{\longrightarrow}
  Maps(k^n, k^n) \times k^n
    \overset{ev}{\longrightarrow}
  k^n
  \,.
$$

By assumption of fiberwise
linearity the functions $\tilde h_i$ in fact take values in the [[general linear group]]

$$
  GL(n,k) \subset Maps(k^n, k^n)
$$

and this inclusion is a [[homeomorphism]] onto its image (by [this prop.](general+linear+group#AsSubspaceOfTheMappingSpace)).

Since passing to [[inverse matrices]]

$$
  (-)^{-1} \;\colon\; GL(n,k) \longrightarrow GL(n,k)
$$

is a [[rational function]] on its domain $GL(n,k) \subset Mat_{n \times n}(k) \simeq k^{(n^2)}$ inside [[Euclidean space]]
and since [[rational functions are continuous]] on their domain of definition,
it follows that the inverse of $f_i$

$$
  (f_i)^{-1}
    \;\colon\;
  U_i \times k^n
    \overset{(id  , \tilde h_i )  }{\longrightarrow}
  U_i \times k^n \times GL(n,k)
    \overset{ id  \times (-)^{-1} }{\longrightarrow}
  U_i \times k^n \times GL(n,k)
    \overset{id  \times ev}{\longrightarrow}
  U_i \times k^n
$$

is a continuous function.

To conclude that also $f^{-1}$ is a continuous function we make use prop. \ref{FromTransitionFunctionsReconstructVectorBundle}
to find an isomorphism between $E_2$ and a [[quotient topological space]] of the form

$$
  E_2 \simeq \left(\underset{i \in I}{\sqcup} (U_i \times k^n) \right) / \left(  \left\{ g_{i j}\right\}_{i,j\in I} \right)
  \,.
$$

Hence $f^{-1}$ is equivalently a function on this quotient space, and we need to show that as such it is continuous.

By the [[universal property]] of the [[disjoint union space]] (the [[coproduct]] in [[Top]]) the set of continuous functions

$$
  \{ U_i \times k^n \overset{f_i^{-1}}{\to} U_i \times k^n \overset{\phi^1_i}{\to} E_1 \}_{i \in I}
$$

corresponds to a single continuous function of the form

$$
  (\phi^1_i \circ f_i^{-1})_{i \in I}
    \;\colon\;
  \underset{i \in I}{\sqcup} U_i \times k^n
    \longrightarrow
  E_1
  \,.
$$

These functions respect the equivalence relation, since for each $x \in U_i \cap U_j$ we have

$$
  (\phi^1_i \circ f_i^{-1})((x,i),v)
    =
  (\phi^1_j \circ f_j^{-1})( (x,j), g_{i j}(x)(v) )
  \phantom{AAAA}
  \text{since:}
  \phantom{AAAA}
  \array{
    && E_1
    \\
     & {}^{\mathllap{\phi^1_i \circ f_i^{-1}}}\nearrow
     &
       \uparrow^{\mathrlap{f^{-1}}}
     & \nwarrow^{\mathrlap{ \phi^1_j \circ f_j^{-1} }}
    \\
    U_i \times k^n
      &\underset{\phi^2_i}{\longrightarrow}&
    (E_2)\vert_{U_i \cap U_i}
      &\underset{(\phi^2_j)^{-1}}{\longrightarrow}&
    U_i \times k^n
  }
  \,.
$$

Therefore by the [[universal property]] of the [[quotient topological space]] $E_2$, these functions
[[extension|extend]] to a unique continuous function $E_2 \to E_1$ such that the following
[[commuting diagram|diagram commutes]]:

$$
  \array{
    \underset{i \in i}{\sqcup} U_i \times k^n
      &\overset{( \phi^1_i \circ f_i^{-1} )_{i \in I}}{\longrightarrow}&
    E_1
    \\
    \downarrow & \nearrow_{\mathrlap{\exists !}}
    \\
    E_2
  }
  \,.
$$

This unique function is clearly $f^{-1}$ (by pointwise inspection) and therefore $f^{-1}$ is continuous.


=--

+-- {: .num_example #FiberwiseLinearlyIndependentSectionsTrivialize}
###### Example
**(fiberwise linearly independent sections trivialize a vector bundle)**

If a topological vector bundle $E \to X$ of [[rank of a vector bundle|rank]] $n$
admits $n$ [[sections]] (example \ref{VectorBundleSections})

$$
  \{\sigma_k \;\colon\; X \longrightarrow E\}_{k \in \{1, \cdots, n\}}
$$

that are linearly independent at each point $x \in X$, then $E$ is trivializable (example \ref{TrivialTopologicalVectorBundle}).
In fact, with the sections regarded as vector bundle homomorphisms out of the trivial vector bundle
of rank $n$ (according to example \ref{VectorBundleSections}), these sections _are_ the trivialization

$$
  (\sigma_1, \cdots, \sigma_n)
  \;\colon\;
  (X \times k^n)
    \overset{\simeq}{\longrightarrow}
  E
  \,.
$$

This is because their linear independence at each point means precisely that this
morphism of vector bundles is a fiber-wise linear isomorphsm
and therefore an isomorphism of vector bundles by lemma \ref{FiberwiseIsoisIsomorphismOfVectorBundles}.

=--


### Direct summand bundles
 {#DirectSummandBundles}

We discuss properties of the [[direct sum of vector bundles]] for topological vector bundles.

+-- {: .num_prop #TopologicalSubBundlesOverParacompactHausdorffSpacesAreDirectSummands}
###### Proposition
**(sub-bundles over [[paracompact spaces]] are [[direct sum of vector bundles|direct summands]])**

Let

1. $X$ be a [[paracompact Hausdorff space]],

1. $E \to X$ a [[topological vector bundle]] (def. \ref{TopologicalVectorBundle}).

Then every topological vector sub-bundle $E_1 \hookrightarrow E$ (example \ref{TopologicalVetorSubbundle}) is a direct vector bundle summand, in that there exists another vector sub-bundle $E_2 \hookrightarrow E$ (example \ref{TopologicalVetorSubbundle}) such that their [[direct sum of vector bundles]] is $E$:

$$
  E_1 \oplus E_2 \simeq E
  \,.
$$

=--

([e.g. Hatcher, prop. 1.3](#Hatcher))

+-- {: .proof}
###### Proof

Since $X$ is assumed to be paracompact Hausdorff, there exists an [[inner product on vector bundles]]

$$
  \langle -,-\rangle
  \;\colon\;
  E \oplus_X E
    \longrightarrow
  X \times k
$$

(by [this prop.](inner+product+of+vector+bundles#ExistenceOfInnerProductOfTopologicalVectorBundlesOverParacompactHausdorffSpaces)). This defines at each $x \in X$ the [[orthogonal complement]] $(E'_x)^\perp \subset E_x$ of $E'_x \hookrightarrow E$. The [[subspace]] of these orthogonal complements is readily checked to be a [[topological vector bundle]] $(E')^\perp \to X$. Hence by construction we have

$$
  E \;\simeq\; E' \oplus_X (E')^\perp
  \,.
$$

=--


+-- {: .num_prop #TopologicalVectorbundleOverCompactHausdorffSpaceIsDirectSummandOfTrivialBundle}
###### Proposition
**(vector bundles over a [[compact Hausdorff space]] are [[direct sum of vector bundles|direct summands]] of a [[trivial vector bundle]])**

Let

1. $X$ be a [[compact Hausdorff space]];

1. $E \to X$ a [[topological vector bundle]] (def. \ref{TopologicalVectorBundle}).

Then there exists another topological vector bundle $\tilde E \to X$ such that the [[direct sum of vector bundles]] of the
two is [[isomorphism|isomorphic]] to a [[trivial vector bundle]] $X \times k^n$:

$$
  E \oplus \tilde E
   \;\simeq\;
  X \times k^n
  \,.
$$

=--


+-- {: .proof}
###### Proof

Let $\{U_i \subset X\}_{i \in I}$ be an [[open cover]] of $X$ over which $E \to X$ has a [[local trivialization]]

$$
  \left\{
    \phi_i
      \;\colon\;
     U_i \times k^n
       \overset{\simeq}{\longrightarrow}
     E\vert_{U_i}
  \right\}_{i \in I}
  \,.
$$

By compactness of $X$, there is a [[finite cover|finite sub-cover]], hence a [[finite set]] $J \subset I$ such tat

$$
  \{U_i \subset X\}_{i \in J \subset I}
$$

is still an open cover over which $E$ trivializes.

Since [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]] there exists a [[partition of unity]]

$$
  \left\{
    f_i \;\colon\; X \to [0,1]
  \right\}_{i \in J}
$$

with [[support]] $supp(f_i) \subset U_i$. Hence the functions

$$
  \array{
    E\vert_{U_i}
     &\overset{\phantom{AAAA}}{\longrightarrow}&
    U_i \times k^n
    \\
    v
       &\overset{\phantom{AAA}}{\mapsto}&
    f_i(x) \cdot \phi_i^{-1}(v)
  }
$$

extend by 0 to vector bundle homomorphism of the form

$$
  f_i \cdot \phi^{-1}_i
  \;\colon\;
  E
    \longrightarrow
  X \times k^n
  \,.
$$

The finite pointwise [[direct sum]] of these yields a vector bundle homomorphism
of the form

$$
  \underset{i \in J}{\oplus} f_i \cdot \phi_i
  \;\colon\;
  E
    \longrightarrow
  X \times \left(
    \underset{i \in J}{\oplus}
       k^n
  \right)
  \simeq
  X \times k^{n \dot {\vert J\vert}}
  \,.
$$

Observe that, as opposed to the single $f_i \cdot \phi^{-1}_i$, this is a fiber-wise injective, because at each point at least one of the $f_i$ is non-vanishing. Hence this is an injection of $E$ into a trivial vector bundle.

With this the statement follows by prop. \ref{TopologicalSubBundlesOverParacompactHausdorffSpacesAreDirectSummands}.

=--


+-- {: .num_remark}
###### Remark

Prop. \ref{TopologicalVectorbundleOverCompactHausdorffSpaceIsDirectSummandOfTrivialBundle} is key in the analysis of [[topological K-theory]] groups on [[compact Hausdorff spaces]]. See [there](topological+K-theory#DirectSumHasInverseUpToTrivialBundle) for more.

=--





### Concordance
 {#ConcordanceOfTopolgicslVectorBundles}

We discuss that every [[concordance]] of topological vector bundles over a [[paracompact topological space]] makes the restriction of the vector bundle over the endpoints of the interval isomorphic (prop. \ref{ConcondanceOfTopologicalVectorBundles} below). In particular this implies tht the [[pullbacks of vector bundles]] along two [[homotopy|homotopic]] [[continuous functions]] are [[isomorphism|isomorphic]] (corollary \ref{PullbackOfvectorBundlesAlongHomotopicMapsAreIsomorphic} below). The proof below follows [Hatcher, theorem 1.6](#Hatcher).

For $X$ a [[topological space]] write $X \times I$ for the [[product topological space]] with the [[closed interval]] $[0,1]$ equipped with its [[Euclidean space|Euclidean]] [[metric topology]].

Write

$$
  X \overset{p_X}{\longleftarrow} X \times [0,1] \overset{p_{[0,1]}}{\longrightarrow} [0,1]
$$

for the two continuous [[projections]] out of the product space.



+-- {: .num_lemma #TrivilizationOfVectorBundleOverProductSpaceWithInterval}
###### Lemma

For $X$ a [[topological space]], then a vector bundle $E \to X \times [0,1]$ is trivializable (example \ref{TrivialTopologicalVectorBundle})
if its restrictions to $X \times [0,1/2]$ and to $X \times [1/2,1]$ are trivializable.

=--

+-- {: .num_lemma #CoverForProductSpaceWithIntrval}
###### Lemma

For $X$ a [[topological space]], then for every topological vector bundle $E \to X \times I$ there exists an [[open cover]] $\{U_i \subset X\}_{i \in I}$ of $X$ such that the vector bundle trivializes over $U_i \times [0,1] \subset X \times [0,1]$, for each $i \in I$.

=--

+-- {: .proof}
###### Proof

By [[local trivialization|local trvializability]] of the vector bundle, there exists an open cover $\{V_j \subset X \times I\}_{j \in J}$ over which the bundle trivializes. For each point $x \in X$ this induces a cover of $\{x\} \times [0,1]$. This is a [[compact topological space]] (for instance by the [[Heine-Borel theorem]]) and hence there exists a [[finite set|finite]] [[subset]] $J_x \subset I$ such that $\{V_i \subset X \times I\}_{i \in J_x}$ still covers $\{x\} \times [0,1]$.

By finiteness of $J_x$, the [[intersection]]

$$
  U_x \coloneqq \underset{i \in J_x}{\cap} p_X(V_i)
$$

is an open neighbourhood of $x$ in $X$. Moreover

$$
  \{ p_{[0,1]}(V_i) \subset I \}_{i \in J_x}
$$

is an open cover of $[0,1]$ such that the given vector bundle trivializes over each element of $\{U_x \times p_{[0,1]}(V_i)\}_{i \in J_x}$.

By the nature of the Euclidean [[metric topology]] each [[open subset]] of $[0,1]$ is a union of intervals. So we may pass to a [[refinement]] of this cover of $[0,1]$ such that each element is a single interval. Again by compactness of $[0,1]$, this refinement has a finite subcover

$$
  \{W_{x,k} \subset [0,1]\}_{k \in K_x}
$$

each element of which is an [[interval]]. Since this is a finite cover, we may find numbers $\{0 = t_0 \lt t_1 \lt t_2 \lt \cdots \lt t_{n_x} = 1\}$ such that

$$
  \{ [t_k, t_{k+1}] \subset [0,1] \}_{0 \leq k \lt n_x}
$$

is a cover of $[0,1]$, and such that the given vector bundle still trivializes over $V_x \times [t_k, t_{k+1}]$ for all $0 \leq k \lt n_x$.

By lemma \ref{TrivilizationOfVectorBundleOverProductSpaceWithInterval} this implies that the vector bundle in fact trivializes over $U_x \times [0,1]$.

Applying this procedure for all points $x \in X$ yields a cover

$$
  \{ U_x \subset X  \}_{x \in X}
$$

with the required property.

=--


+-- {: .num_prop #ConcondanceOfTopologicalVectorBundles}
###### Proposition
**([[concordance]] of [[topological vector bundles]])**

Let $X$ be a [[paracompact Hausdorff space]]. If $E \to X \times [0,1]$ is a [[topological vector bundle]] over the [[product space]] of $X$ with the [[closed interval]] (hence a _[[concordance]]_ of topological vector bundles on $X$), then the two endpoint-restrictions

$$
  E|_{X \times \{0\}}
  \phantom{AA}
  \text{and}
  \phantom{AA}
  E|_{X \times \{1\}}
$$

are [[isomorphism|isomorphic]] vector bundles over $X$.

=--

+-- {: .proof}
###### Proof

By lemma \ref{CoverForProductSpaceWithIntrval} there exists an open cover $\{U_i \subset X\}_{i \in I}$ of $X$ such that the vector bundle $E$ trivializes over $U_i \times [0,1]$ for each $i \in I$. By [this lemma](paracompact+topological+space#CountableCoverOfUnionsofOpenSubsetsInsideGivenCover) there exists a [[countable cover]]

$$
  \{V_n \subset X\}_{n \in \mathbb{N}}
$$

such that each element is a [[disjoint union]] of open subsets that each are contained in one of the $U_i$. This means that the vector bundle $E$ still trivializes over $V_n \times [0,1]$, for each $n \in \mathbb{N}$.

Moreover, since [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]], there
exists a [[partition of unity]] $\left\{f_n \colon X \to [0,1] \right\}_{n \in \mathbb{N}}$ subordinate to this countable cover.

For $n \in \mathbb{N}$ define

$$
  \psi_n \coloneqq \underoverset{k = 0}{n}{\sum} f_n
$$

(so $\psi_0 = 0$ and by local finiteness there is for each $x \in X$ an $n_x$ such that $\psi_{n \gt n_x} = 1$.)

Now write

$$
  X_n \coloneqq graph( \psi_n ) \subset X \times [0,1]
$$

for the [[graph]] of the function $\psi_n$ equipped with its [[subspace topology]], and write

$$
  E_n
   \coloneqq
  \psi_n^\ast E
$$

for the restriction of $E$ to that subspace

$$
  \array{
    E_n &\longrightarrow& E
    \\
    \downarrow && \downarrow
    \\
    X_n = graph(\psi_n) &\hookrightarrow& X
  }
$$

Observe that the projection functions

$$
  \array{
   p_{n+1,n} \colon &  X_{n+1} &\overset{}{\longrightarrow}& X_n
    \\
    & (x,\psi_{n+1}(x)) &\overset{\phantom{AA}}{\mapsto}& (x, \psi_n(x)) = (x,  \psi_{n+1}(x) - f_{n+1}(x))
  }
$$

are [[continuous functions]]: By the nature of the [[product topology]] and the [[subspace topology]] it is sufficient to check for $U \subset X$
and $V \subset \mathbb{R}$ open subsets, that every point $(x,c)$ in the preimage
$p_n^{-1}( U \times V ) \subset X \times [0,1]$ is contained in an open subset of the form $U_x \times V_x \subset X \times [0,1]$
such that every point of $X_{n+1}$ that is also in $U_x \times V_x$ is still mapped to $U \times V$. Such an open subset is
$\left( U \cap \psi_n^{-1}(V) \right) \times [0,1]$.

Also observe that the composites

$$
  E_n \longrightarrow X_n \overset{p_{n,0}}{\longrightarrow} X_0 = 0
$$

make each $E_n$ a vector bundle over $X$: To see local trivializability over $X$ choose a local
trivialization of $E$ over some open cover $\{U_i \subset X\}_{i \in I}$
and observe that then $E_n$ is trivial over the [[fiber product]]$X_n \times_X U_n$ and hence over $U_n$.


Now by the pullback definition of the $E_n$, the [[pasting law]] says that for each $n \in \mathbb{N}$ we have a
pullback square of vector bundles of the form

$$
  \array{
    E_{n+1}
      && \overset{h_n}{\longrightarrow} &&
    E_n
    \\
    \downarrow && (pb) && \downarrow
    \\
    X_{n+1} && \longrightarrow && X_n
    \\
    & \searrow && \swarrow
    \\
    && X
  }
  \,.
$$

By the nature of pullbacks, the top horizontal function $h_n$ in this diagram is on each fiber a linear isomorphism.
Therefore prop. \ref{FiberwiseIsoisIsomorphismOfVectorBundles} implies that each $h_n$ is in
fact an isomorphism of vector bundles over $X$

By local finiteness, each point $x \in X$ has a neighbourhood $U_x$ such that only a finite number $n_x$ of these $h_n$ are non-trivial, and so it makes sense to consider the infinite composition

$$
  h \coloneqq h_1 \circ h_2 \circ h_3 \circ \cdots
$$

understood to be on each $U_x$ the finite composite

$$
  h(x) \coloneqq h_1 \circ \cdots \circ h_{n_x}
  \,.
$$

Since all the $h_k$ are vector bundle isomorphisms, so are all their composites. Thus $h$ is an isomorphism of the required form

$$
  h
  \;\colon\;
  E|_{X \times \{0\}}
   \overset{\simeq}{\longrightarrow}
  E|_{X \times \{1\}}
  \,.
$$

=--

+-- {: .num_cor #PullbackOfvectorBundlesAlongHomotopicMapsAreIsomorphic}
###### Corollary

Let $X$ be a [[paracompact Hausdorff space]], let $E \to Y$ be a topological [[vector bundle]], let $f,g \colon X \to Y$ be two [[continuous functions]], and let $\eta \colon f \to g$ be a [[left homotopy]] between them. Then there is an [[isomorphism]] of vector bundles over $X$ between the [[pullback of vector bundles]] of $E$ along $f$ and along $g$, respectively:

$$
  f^\ast E \simeq g^\ast E
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition, the [[left homotopy]] $\eta$ is a [[continuous function]] of the form

$$
  \eta
  \;\colon\;
  X \times [0,1] \longrightarrow Y
  \,.
$$

For $t \in [0,1]$ write $i_t$ for the continuous function

$$
  \array{
     X &\overset{\phantom{AA}i_t\phantom{AA}}{\longrightarrow}& X \times [0,1]
     \\
     x &\overset{\phantom{AAAA}}{\mapsto}& (x,t)
  }
  \,.
$$

By the [[pasting law]] for pullbacks we have that

$$
  f^\ast E = (\eta \circ i_0)^\ast E
  \simeq i_0^\ast (\eta^\ast E) \simeq (\eta^\ast E)|_{X \times \{0\}}
$$

and

$$
  g^\ast E = (\eta \circ i_1)^\ast E
  \simeq i_1^\ast (\eta^\ast E) \simeq (\eta^\ast E)|_{X \times \{1\}}
$$

With this the statement follows by prop. \ref{ConcondanceOfTopologicalVectorBundles}.

=--

+-- {: .num_example #HomotopyInvarianceOfIsomorphismClassesOfVectorBundles}
###### Example
**([[homotopy invariance]] of isomorphism classes of vector bundles)**

Let $X$ and $Y$ be [[paracompact Hausdorff spaces]] and let

$$
  f \;\colon\; X \longrightarrow Y
$$

be a [[continuous function]] which is a [[homotopy equivalence]]. Then
pullback along $f$ constitutes a [[bijection]] on sets of isomorphism classes
of topological vector bundles:

$$
  f^\ast
   \;\colon\;
  Vect(Y)/_\sim
    \overset{\simeq}{\longrightarrow}
  Vect(X)/_\sim
  \,.
$$

=--

+-- {: .proof}
###### Proof

By definition of homotopy equivalence, there is a continuous function
$g \colon Y \longrightarrow X$ and [[left homotopies]]

$$
  g \circ f \Rightarrow id
  \phantom{AAAA}
  f \circ g \Rightarrow id
  \,.
$$

Hence corollary \ref{PullbackOfvectorBundlesAlongHomotopicMapsAreIsomorphic} implies that

$$
  f^\ast \circ g^\ast = (g \circ f)^\ast = id
  \phantom{AAAAA}
  g^\ast \circ f^\ast = (g \circ g)^\ast = id
  \,.
$$

This mean that $g^\ast$ is the [[inverse function]] to $f^\ast$, and hence both are bijections.

=--

+-- {: .num_example #TopologicalVectorBundleOverContractibleSpaceIsTrivializable}
###### Example
**(topological vector bundle on contractible topological space is trivializable)**

If $X$ is a [[contractible topological space]], then every topological vector bundle over $X$
is isomorphic to a [[trivial vector bundle]].

=--

+-- {: .proof}
###### Proof

That $X$ is contractible means by definition that there is a [[left homotopy]] of the form

$$
  \array{
    X &\longrightarrow& \ast
    \\
    \mathllap{i_0}\downarrow & & \downarrow
    \\
    X \times [0,1]
      &\overset{\eta}{\longrightarrow}&
    X
    \\
    \mathllap{i_1}\uparrow & \nearrow_{\mathrlap{id}}
    \\
    X &
  }
  \,.
$$

By cor \ref{PullbackOfvectorBundlesAlongHomotopicMapsAreIsomorphic} it follows that for
$E \to X$ any topological vector bundle that there is an isomorphism between
$id^\ast E = E$ and the result of first restricting the bundle to the point, and then
forming the [[pullback bundle]] along $X \to \ast$. But the latter operation precisely produces
the [[trivial vector bundles]] over $X$.

=--



### Over closed subspaces
 {#OverClosedSubspaces}

We discuss the behavour of vector bundles with respect to [[closed subspaces]] $A \subset X$
of [[compact Hausdorff spaces]].

+-- {: .num_lemma #IsomorphismOfVectorBundlesOnClosedSubsetOfCompactHausdorffSpaceExtendsToOpenNeighbourhoods}
###### Lemma
**([[isomorphism]] of vector bundles on [[closed subset]] of [[compact Hausdorff spaces]] [[extension|extends]] to [[open neighbourhood]])**

Let $k \in \{\mathbb{R}, \mathbb{C}\}$, let $X$ be a [[compact Hausdorff space]] and let $A \subset X$ a [[closed subset|closed]] [[subspace]].
Let $E_i \overset{p_i}{\to} X$ be two topological vector bundles over $X$, $i \in \{1,2\}$.

If there exists an [[isomorphism]]

$$
  E_1\vert_A \overset{\simeq}{\longrightarrow} E_2\vert_A
$$

of the restricted vector bundles over $A$, then there also exists an [[open subset]] $U \subset X$
with $A \subset U$ such that there is also an isomorphism

$$
  E_1\vert_U \overset{\simeq}{\longrightarrow} E_2\vert_U
$$

of the vector bundles restricted to $U$.

=--

+-- {: .proof}
###### Proof

A bundle isomorphism $E_1\vert_A \simeq E_2\vert_A$ is equivalently a trivializing section
(example \ref{FiberwiseLinearlyIndependentSectionsTrivialize}) of the
[[tensor product of vector bundles]] $(E_1\vert_A)^\ast \otimes_A E_2\vert_A$ of $E_2\vert_A$ with the [[dual vector bundle]] $(E_2\vert_A)^\ast$.
(by [this prop.](tensor+product+of+vector+bundles#FinitrRankBundleHomomorphismIsSectionOfTensorProductWithDual)).

Let $\{V_i \subset X\}_{i \in I}$ be an [[open cover]] of $X$ over which this tensor product bundle trivializes with
trivializations

$$
  \left\{
    V_i \times \mathbb{R}^{(n^2)}
     \underoverset{\simeq}{\phi_i}{\longrightarrow}
    (E_1^\ast \otimes_X E_2)\vert_{U_i}
  \right\}
  \,.
$$


Since [[compact Hausdorff spaces are normal]], the [[shrinking lemma]] applies and gives a refinement of this
by a cover $\{U_i \subset X\}_{i \in I}$ by _closed_ subsets $U_i \subset X$.

Then a trivializing section $\sigma \in \Gamma_A\left( (E_1\vert_A)^\ast \otimes_A E_2 \vert_A \right)$ as above is on each $U_i \cap A$
a [[continuous function]]

$$
 \sigma_i
 \;\colon\;
 U_i \cap A \longrightarrow GL(n,k)
$$

to the [[general linear group]] $GL(n,k) \subset Mat_{n \times n}(k)$, such that

$$
  \sigma\vert_{U_i \cap A} = \phi_i \circ \sigma_i
  \,.
$$

Regarded as a function
to the $n \times n$ [[matrices]], this is a set of $n^2$ [[continuous function]] $((\sigma_i)_{a b})$

Now since $U_i \subset X$ is closed by construction, and $A \subset X$ is closed by assumption,
also the intersections $U_i \cap X$ are closed.
Since [[compact Hausdorff spaces are normal]] the [[Tietze extension theorem]] therefore applies to these component functions and yields
[[extensions]] of each $\sigma_i$ to a [[continuous function]] of the form

$$
  \hat \sigma_i \;\colon\; U_i \longrightarrow Mat_{n \times n}(k)
  \,.
$$

Moreover, since compact Hausdorff spaces are evidently [[paracompact Hausdorff spaces]], and since
[[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]], it follows that we find a
[[partition of unity]] $\{f_i \colon U_i \to \mathbb{R} \}_{i \in I}$.

Consider then the functions $f_i \cdot \hat \sigma_i$ given by pointwise multiplication and regarded, via extension by
zero, as continuous functions on all of $X$

$$
  f_i \cdot \hat \sigma_i \;\colon\; X \longrightarrow \mathbb{R}
  \,.
$$

Summing these up yields a single section $\hat \sigma$ of $E_1^\ast \otimes_X E_2$

$$
  \hat \sigma
    \coloneqq
  \sum_{i \in I}
  \phi_i(f_i \cdot \hat \sigma_i)
  \in
  \Gamma_X(E_1^\ast \otimes_X E_2)
  \,,
$$

which by construction is an [[extension]] of the original section, in that

$$
  \hat \sigma\vert_A = \sigma
  \,.
$$

This is because for each $a \in A \subset X$ we have, using the above definitions,

$$
 \begin{aligned}
   \left(\underset{i \in I}{\sum} \phi_i(f_i \cdot \hat \sigma_i)\right)(a)
   & =
   \underset{i \in I}{\sum} (\phi_i (\hat \sigma_i(a)))
   \\
   & = \underset{i \in I}{\sum} \phi_i( f_i(a) \sigma_i(a) )
   \\
   & = \underset{i \in I}{\sum} f_i(a) \cdot (\phi_i \circ \sigma_i)(a)
   \\
   & = \underset{i \in I}{\sum} f_i(a) \cdot \sigma(a)
   \\
   & = \left( \underset{i \in I}{\sum} f_i(a)\right) \cdot \sigma(a)
   \\
   & = \sigma(a)
 \end{aligned}
$$

Here the last step uses the nature of the partition of unity.

Now while $\hat \sigma$ is an extension of the section $\sigma$ to $X$, it will in general
not be a trivializing section on $X$.

But since the [[general linear group]] $GL(n,k) = det^{-1}(k \setminus \{0\}) \subset Mat_{n \times n}(k)$
is an [[open subset]] of the [[Euclidean space]] $Mat_{n \times n}(k) \simeq k^{(n^2)}$, it follows that
each point $x \in A$ has an open neighbourhood $U_x \subset X$ such that $\hat \sigma\vert_{U_x}$
is still a trivializing section, namely choosing $i_x \in I$ such that $x \in U_{i_x}$ set

$$
  U_x \coloneqq (\hat \sigma_{i_x})^{-1}( GL(n,k) )
  \,.
$$

The union of these

$$
  U \coloneqq \underset{x \in A}{\cup} U_x
$$

is hence an open subset containing $A$ such that $(E_1^\ast \otimes_X E_2)\vert_U$ has a trivializing section,
extending $\sigma$, hence such that there is an isomorphism $E_1\vert_U \simeq E_2 \vert_U$ extending the
original isomorphism on $A$.


=--

As a consequence:

+-- {: .num_prop #VectorBundleOnClosedSubsetOfCompactHausdorffSpaceIsPullbackOfBundeOnQuotientSpace}
###### Proposition
**([[vector bundle]] [[trivial vector bundle|trivial]] over [[closed subspace]] of [[compact Hausdorff space]] is [[pullback bundle|pullback]] of bundle on [[quotient space]])**

Let $X$ be a [[compact Hausdorff space]] and let $A \subset X$ be a [[closed subspace]].

If a topological vector bundle $E \overset{p}{\to} X$ is such that its restriction $E\vert_A$
is [[trivializable vector bundle|trivializable]], then $E$ is [[isomorphism|isomorphic]] to
the [[pullback bundle]] $q^\ast E'$ of a topological vector bundle $E' \to X/A$
over the [[quotient space]].

=--

+-- {: .proof}
###### Proof

Let

$$
  A \times k^n
    \underoverset{\simeq}{\phi}{\longrightarrow}
  E\vert_A
$$

be an isomorphism of vector bundles over $A$, which exists by assumption.
Consider then on the total space $E\vert_A$ the [[equivalence relation]] given by

$$
  \phi^{-1}(x,v) \sim \phi^{-1}(x',v)
$$

for all $x,x' \in A$ and $v \in k^n$. Let

$$
  E' \coloneqq E/\sim
$$

be the corresponding [[quotient topological space]]. Observe that for $x \in X$
we have $E'_x = E_x$ while for $x \in A$ we have a canonical identification $E'_{x/A} \simeq k^n$,
and over these points quotient coprojection is identified with $\phi^{-1}$:

$$
  \array{
    E
      &\overset{}{\longrightarrow}&
    E'
    \\
    (x,v) &\mapsto& \left\{ \array{ (x,v) &\vert& x \in X \setminus A  \\ \phi^{-1}_x(v) &\vert& x\in A }  \right.
  }
  \,.
$$

Since the composite continuous function

$$
  E \overset{p}{\longrightarrow} X \overset{q}{\longrightarrow} X/A
$$

respects the equivalence relation (in that it sends any two equivalent points to the same image point)
the [[universal property]] of the quotient space yields
a continuous function

$$
  p' \;\colon\; E' \to X/A
$$

such that the following [[commuting diagram|diagram commutes]]

$$
  \array{
    E &\longrightarrow& E'
    \\
    {}^{\mathllap{p}}\downarrow && \downarrow^{\mathrlap{p'}}
    \\
    X &\overset{q}{\longrightarrow}& X/A
  }
  \,.
$$

We claim that this is a [[pullback]] diagram in [[Top]]:

By the above description of the top horizontal function, it is a pullback diagram
of underlying sets. Hence we need to see that the topology on $E$
has a [[base for a topology|base]] given by the pre-images
of the open subsets in $X$ and in $E'$. Now by definition of the quotient space
topology on $E'$, its open subsets are those of $E$ that either do not
contain a point $(x,v)$ with $x \in A$ or if they do, then they also
contain all the points of the form $(x', \phi_{x'}^{-1}(\phi_x(v)))$ for
$x' \in A$. Moreover, if $(x,v)$ is in the open subset for $x \in A$,
then also $(x,v')$ for all $v'$ in some open ball in $k^n$ containing $v$.
Hence intersecing these pre-images with pre-images of open subsets of $X$ under $p$
yields a basis for the topology.

Hence it only remains to see that $E' \overset{p'}{\longrightarrow} X/A$ is a vector bundle. The
fiberwise linearity is clear, we need to show that it is locally trivializable.

To that end, let $\{U_i \subset X\}_{i \in I}$ be an open cover over which $E \overset{p}{\to} X$
has a local trivialization. Since $A \subset X$ is assumed to be closed, it follows that

$$
  \left\{ U_i \setminus A \subset X \setminus A\right\}_{i \in I}
$$

is an open cover of the complement of $A$ in $X$. By the nature of the [[quotient space topology]], this
induces an open cover of $X\setminus A$. If we adjoin the quotient $U/A$  of an open neighbourhood $U \subset X$ of $A$ in $X$,
then

$$
  \{ U_i \setminus A \subset X/A \} \sqcup \{ U/A \subset X/A \}
$$

is an open cover of $X/A$. Moreover, by the construction of $E' \overset{p'}{\to} X/A$ it is clear that
this bundle has a local trivialization over $U_i$, since $E \overset{p}{\to} X$ does,
and similarly $E'$ trivializes over $U/A$ if $E$ trivializes over $U$. But such a $U$ does indeed exist by
lemma \ref{IsomorphismOfVectorBundlesOnClosedSubsetOfCompactHausdorffSpaceExtendsToOpenNeighbourhoods}.

=--


+-- {: .num_remark}
###### Remark

Prop \ref{VectorBundleOnClosedSubsetOfCompactHausdorffSpaceIsPullbackOfBundeOnQuotientSpace} is the reason why [[reduced K-theory|reduced]] [[topological K-theory]]
satisfies the [[long exact sequences in cohomology]] that make it a [[generalized (Eilenberg-Steenrod) cohomology theory]].
See

=--


+-- {: .num_prop #VectorBundlesOverQuotientByContractibleSubspaceAreEquivalentToVectorBundlesOnTotalSpace}
###### Proposition

Let $X$ be a [[compact Hausdorff space]] and $A \subset X$ a [[closed subset|closed]] [[subspace]]
and write $X/A$ for the corresponding [[quotient topological space]] ([this example](quotient+space#QuotientBySubspace))
with quotient coprojection denoted
$q \colon X \longrightarrow X/A$.

If $A$ is a [[contractible topological space]] then the [[pullback bundle]] construction

$$
  q^\ast \;\colon\; Vect(X/A)_{/\sim} \longrightarrow Vect(X)_{/\sim}
$$

is an [[isomorphism]].

=--


+-- {: .proof}
###### Proof

By example \ref{TopologicalVectorBundleOverContractibleSpaceIsTrivializable} every vector bundle
$E \overset{p}{\to} X$ is trivializable over the contractible subspace $A$.
Therefore prop. \ref{VectorBundleOnClosedSubsetOfCompactHausdorffSpaceIsPullbackOfBundeOnQuotientSpace}
implies that it is in the image of the pullback bundle map $q^\ast$. This says that $q^\ast$
is surjective. Finally, it is clear that it is injective. Therefore it is bijective.

=--

+-- {: .num_example }
###### Example

Let $(X,x)$ be a [[pointed topological space|pointed]] [[compact topological space]].

For $[0,1] \subset \mathbb{R}$ the [[closed interval]] with its [[Euclidean space|Euclidean]] [[metric topology]].

There is

1. the ordinary [[cylinder]], being the [[product space]] $X \times I$

1. the [[reduced cylinder]] $X \wedge I_+ = (X \times I)/( \{x\} \times I )$
   which is the [[smash product]] with the interval that has a base point freely adjoined

and

1. the ordinary [[suspension]] $S X \coloneqq (X \times I)/( X \times \{0,1\} )$;

1. the [[reduced suspension]] $\Sigma X \coloneqq (S X)/( \{x\} \times I )$.

In both cases the reduced space is obtained from the unreduced space by quotienting out the
contractible closed subspace $I \simeq \{x\} \times I$ and hence topological vector bundles
do not see the difference between the reduced and the unreduced spaces, by prop. \ref{VectorBundlesOverQuotientByContractibleSubspaceAreEquivalentToVectorBundlesOnTotalSpace}.


=--





## Related concepts

* [[algebraic vector bundle]]

* [[differentiable vector bundle]]

* [[topological K-theory]]

## References


Textbook accounts include

* Glenys Luke, Alexander S. Mishchenko, _Vector bundles and their applications_, Math. and its Appl. __447__, Kluwer 1998. viii+254 pp. [MR99m:55019](http://www.ams.org/mathscinet-getitem?mr=99m:55019)

* [[Dale Husemoeller]], [[Michael Joachim]], [[Branislav Jurco]], [[Martin Schottenloher]], _[[Basic Bundle Theory and K-Cohomology Invariants]]_, Lecture Notes in Physics, Springer 2008 ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726corr1.pdf))

Lecture notes with an eye towards [[topological K-theory]] is in

* {#Wirthmuller12} [[Klaus Wirthmüller]], _Vector bundles and K-theory_, 2012 ([[wirthmueller-vector-bundles-and-k-theory.pdf:file]])

* {#Hatcher} [[Allen Hatcher]], chapter 1 of _Vector bundles and K-Theory_, (partly finished book) [web](http://www.math.cornell.edu/~hatcher/VBKT/VBpage.html)


[[!redirects topological vector bundles]] 

