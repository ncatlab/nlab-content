

## Geometry
 {#Geometry}

The [[geometry of physics]] is _[[differential geometry]]_. This is the flavor of [[geometry]] which is modeled on
[[Cartesian spaces]] $\mathbb{R}^n$ with [[smooth functions]] between them. Here we briefly review the basics of
[[differential geometry]] on [[Cartesian spaces]].

In principle the only **background** assumed of the reader here is

1. usual _[[structural set theory|naive set theory]]_ (e.g. [[Sets for Mathematics|Lawvere-Rosebrugh 03]]);

1. the concept of the _[[continuum]]_: the [[real line]] $\mathbb{R}$, the [[plane]] $\mathbb{R}^2$, etc.

1. the concepts of _[[differentiation]]_ and _[[integration]]_ of functions on such [[Cartesian spaces]];

hence essentially the content of multi-variable [[differential calculus]].

We now discuss:

* _[Abstract coordinate systems](#SmoothFunctions)_

* _[Fiber bundles](#BundlesAndSections)_

* _[Synthetic differential geometry](#SyntheticDifferentialGeometry)_

* _[Differential forms](#DifferentialFormsAndCartanCalculus)_


As we uncover [[Lagrangian field theory]] further below, we discover ever more general concepts of
"[[space]]" in differential geometry, such as
_[[smooth manifolds]]_, _[[diffeological spaces]]_, _[[infinitesimal neighbourhoods]]_, _[[supermanifolds]]_, _[[Lie algebroids]]_
and _[[super L-∞ algebra|super]] [[Lie ∞-algebroids]]_.
We introduce these incrementally as we go along:

**more general [[spaces]] in [[differential geometry]] introduced further below**
 {#NotionsOfGeometry}

| | |  |  |  |  |  |  |  |  |  | [[higher differential geometry]] |
|--|---|---|---|---|---|---|---|---|---|---|---|
| **[[differential  geometry]]** | [[smooth manifolds]] <br/> (def. \ref{SmoothManifoldInsideDiffeologicalSpaces}) | $\hookrightarrow$ | [[diffeological spaces]] <br/> (def. \ref{DiffeologicalSpace}) | $\hookrightarrow$ | [[smooth sets]] <br/> (def. \ref{SmoothSet}) | $\hookrightarrow$ | [[formal smooth sets]] <br/> (def. \ref{FormalSmoothSet}) | $\hookrightarrow$ | [[super formal smooth sets]] <br/> (def. \ref{SuperFormalSmoothSet}) | $\hookrightarrow$ | [[super formal smooth ∞-groupoids]] <br/> (not needed in fully [[perturbative QFT]]) |
| **[[infinitesimal]] [[formal geometry|geometry]], <br/> [[Lie theory]]** | |  |  |  |  |   | [[infinitesimally thickened points]] <br/> (def. \ref{InfinitesimallyThickendSmoothManifold}) |  | [[superpoints]] <br/> (def. \ref{SuperCartesianSpace}) |  | [[Lie ∞-algebroids]] <br/> (def. \ref{LInfinityAlgebroid}) |
| | |  |  |  |  |  |  |  |  |  | **[[higher Lie theory]]** |
| **needed in [[QFT]] for:** |  [[spacetime]] (def. \ref{MinkowskiSpacetime}) |  | [[space of field histories]] <br/> (def. \ref{DiffeologicalSpaceOfFieldHistories})  |  |  |  | [[Cauchy surface]] (def. \ref{CauchySurface}), <br/> [[perturbation theory]]  (def. \ref{LocalObservablesOnInfinitesimalNeighbourhood}) |  | [[Dirac field]] (expl. \ref{DiracFieldBundle}), [[Pauli exclusion principle]]  |  | [[infinitesimal gauge symmetry]]/[[BRST complex]] <br/> (expl. \ref{LocalOffShellBRSTComplex})  |


$\,$

**Abstract coordinate systems**
 {#SmoothFunctions}

What characterizes [[differential geometry]] is that it models [[geometry]] on _the [[continuum]]_,
namely the [[real line]] $\mathbb{R}$, together with its [[Cartesian products]] $\mathbb{R}^n$,
regarded with its canonical [[smooth structure]] (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem} below).
We may think of these _[[Cartesian spaces]]_ $\mathbb{R}^n$ as the "abstract [[coordinate systems]]"
and of the [[smooth functions]] between them as the "abstract [[coordinate transformations]]".

We will eventually consider [below](#FieldBundles) much more general "[[smooth spaces]]" $X$ than just the [[Cartesian spaces]] $\mathbb{R}^n$;
but all of them are going to be understood by "laying out abstract coordinate systems" inside them,
in the general sense of having smooth functions $f \colon \mathbb{R}^n \to X$ mapping a Cartesian space smoothly into them.
All structure on [[generalized smooth spaces]] $X$ is thereby reduced to _compatible systems_ of structures on just [[Cartesian spaces]],
one for each smooth "probe" $f\colon \mathbb{R}^n \to X$. This is called "[[functorial geometry]]".

Notice that the popular concept of a _[[smooth manifold]]_ (def./prop. \ref{SmoothManifoldInsideDiffeologicalSpaces} below)
is essentially that o a [[smooth space]] which _locally looks just like_ a [[Cartesian space]],
in that there exist sufficiently many $f \colon \mathbb{R}^n \to X$ which are ([[open map|open]]) _[[isomorphisms]]_
onto their [[images]]. Historically it was a long process to arrive at the insight that it is wrong to _fix_
such local coordinate identifications $f$, or to have any structure depend on such a choice. But it is useful
to go one step further:

In [[functorial geometry]] we do not even focus attention on those $f \colon \mathbb{R}^n \to X$ that are
isomorphisms onto their image, but consider _all_ "probes" of $X$ by "abstract coordinate systems".
This makes [[differential geometry]] both simpler as well as more powerful. The analogous insight
for [[algebraic geometry]] is due to [Grothendieck 65](functorial+geometry#Grothendieck65); it was transported
to [[differential geometry]] by [Lawvere 67](synthetic+differential+geometry#Lawvere67).

This allows to combine the best of two superficially disjoint worlds: On the one hand we may reduce
all constructions and computations to [[coordinates]], the way traditionally done in the [[physics]] literature;
on the other hand we have full conceptial control over the coordinate-free generalized spaces analyzed thereby.
What makes this work is that all [[coordinate]]-constructions are _[[functorial geometry|functorially]]_ considered
over all abstract coordinate systems.

$\,$

+-- {: .num_defn #CartesianSpacesAndSmoothFunctionsBetweenThem}
###### Definition
**([[Cartesian spaces]] and [[smooth functions]] between them)**

For $n \in \mathbb{N}$ we say that the set $\mathbb{R}^n$ of [[n-tuples]] of [[real numbers]]
is a _[[Cartesian space]]_. This comes with the canonical [[coordinate functions]]

$$
  x^k \;\colon\; \mathbb{R}^n \longrightarrow \mathbb{R}
$$

which send an [[n-tuple]] of real numbers to the $k$th element in the tuple, for $k \in \{1, \cdots, n\}$.

For

$$
  f \;\colon\; \mathbb{R}^{n} \longrightarrow \mathbb{R}^{n'}
$$

any [[function]] between [[Cartesian spaces]], we may ask whether its [[partial derivative]]
along the $k$th coordinate exists, denoted

$$
  \frac{\partial f}{\partial x^k}
  \;\colon\;
  \mathbb{R}^{n}
    \longrightarrow
  \mathbb{R}^{n'}
  \,.
$$

If this exists, we may in turn ask that the [[partial derivative]] of the partial derivative exists

$$
  \frac{\partial^2 f}{\partial x^{k_1} \partial x^{k_2}}
  \coloneqq
  \frac{\partial}{\partial x^{k_2}} \frac{\partial f}{\partial x^{k_1}}
$$

and so on.

A general higher [[partial derivative]] obtained this way is, if it exists, indexed by an [[n-tuple]]
of [[natural numbers]] $\alpha \in \mathbb{N}^n$ and denoted

$$
  \label{PartialDerivativeWithManyIndices}
  \partial^\alpha
    \;\coloneqq\;
  \frac{
    \partial^{\vert \alpha \vert} f
  }{
    \partial^{\alpha_1} x^1
    \partial^{\alpha_2} x^2
      \cdots
    \partial^{\alpha_n} x^n
  }
  \,,
$$

where ${\vert \alpha\vert} \coloneqq \underoverset{n}{i = 1}{\sum} \alpha_i$ is the total _order_ of the partial derivative.

If all partial derivative to all orders $\alpha \in \mathbb{N}^n$ of a [[function]] $f \colon \mathbb{R}^n \to \mathbb{R}^{n'}$
exist, then $f$ is called a _[[smooth function]]_.

=--

Of course the [[composition]] $g \circ f$ of two smooth functions is again a [[smooth function]].

$$
  \array{
    && \mathbb{R}^{n_2}
    \\
    & {}^{\mathllap{f}}\nearrow && \searrow^{\mathrlap{g}}
    \\
    \mathbb{R}^{n_1}
      && \underset{g \circ f}{\longrightarrow} &&
    \mathbb{R}^{n_3}
  }
  \,.
$$


The inclined reader may notice that this means that [[Cartesian spaces]] with [[smooth functions]]
between them constitute a _[[category]]_ ("[[CartSp]]"); but the reader not so inclined may ignore this.

For the following it is useful to think of each [[Cartesian space]] as an _abstract [[coordinate system]]_.
We will be dealing with various [[generalized smooth spaces]] (see the table [below](#NotionsOfGeometry)), but they will all be characterized by
a prescription for how to smoothly map abstract coordinate systems into them.



+-- {: .num_example #CoordinateFunctionsAreSmoothFunctions}
###### Example
**([[coordinate functions]] are [[smooth functions]])**

Given a [[Cartesian space]] $\mathbb{R}^n$, then all its [[coordinate functions]] (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem})

$$
  x^k \;\colon\; \mathbb{R}^n \longrightarrow \mathbb{R}
$$

are [[smooth functions]] (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}).

For

$$
  f \colon \mathbb{R}^{n_1} \longrightarrow \mathbb{R}^{n_2}
$$

any [[smooth function]] and $a \in \{1, 2, \cdots, n_2\}$ write

$$
  f^a \coloneqq x^k \circ f
  \;\colon\;
  \mathbb{R}^{n_1}
    \overset{f}{\longrightarrow}
  \mathbb{R}^{n_2}
    \overset{x^a}{\longrightarrow}
  \mathbb{R}
$$
.
for its [[composition]] with this [[coordinate function]].

=--


+-- {: .num_example #AlgebraOfSmoothFunctionsOnCartesianSpaces}
###### Example
**([[algebra of functions|algebra of]] [[smooth functions]] on [[Cartesian spaces]])**

For each $n \in \mathbb{N}$, the set

$$
  C^\infty(\mathbb{R}^n)
   \;\coloneqq\;
  Hom_{CartSp}(\mathbb{R}^n, \mathbb{R})
$$

of [[real number]]-valued [[smooth functions]] $f \colon \mathbb{R}^n \to \mathbb{R}$
on the $n$-dimensional [[Cartesian space]] (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem})
becomes a [[commutative algebra|commutative]] [[associative algebra]] over the [[ring]] of [[real numbers]]
by pointwise addition and multiplication in $\mathbb{R}$: for $f,g \in C^\infty(\mathbb{R}^n)$ and $x \in \mathbb{R}^n$

1. $(f + g)(x) \coloneqq f(x) + g(x)$

1. $(f \cdot g)(x) \coloneqq f(x) \cdot g(x)$.

The inclusion

$$
  \mathbb{R} \overset{const}{\hookrightarrow} C^\infty(\mathbb{R}^n)
$$

is given by the [[constant functions]].

We call this the _[[real numbers|real]] [[algebra of functions|algebra of]] [[smooth functions]]_ on $\mathbb{R}^n$:

$$
  C^\infty(\mathbb{R}^n)
  \;\in\;
  \mathbb{R} Alg
  \,.
$$

If

$$
  f \;\colon\; \mathbb{R}^{n_1} \longrightarrow \mathbb{R}^{n_2}
$$

is any [[smooth function]] (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}) then
[[composition|pre-composition]] with $f$ ("[[pullback of functions]]")

$$
  \array{
    C^\infty(\mathbb{R}^{n_2})
      &\overset{f^\ast}{\longrightarrow}&
    C^\infty(\mathbb{R}^{n_1})
    \\
    g &\mapsto& f^\ast g \coloneqq g \circ f
  }
$$

is an [[associative algebra|algebra]] [[homomorphism]]. Moreover, this is clearly compatible with [[composition]] in that

$$
  f_1^\ast(f_2^\ast g) = (f_2 \circ f_1)^\ast g
  \,.
$$

Stated more [[category theory|abstractly]], this means that assigning [[algebra of functions|algebras]] of [[smooth functions]]
is a [[functor]]

$$
  C^\infty(-)
  \;\colon\;
  CartSp \longrightarrow \mathbb{R} Alg^{op}
$$

from the [[category]] [[CartSp]] of [[Cartesian spaces]] and [[smooth functions]] between them (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}), to the
[[opposite category|opposite]] of the category $\mathbb{R}$[[Alg]] of $\mathbb{R}$-[[associative algebra|algebras]].

=--

+-- {: .num_defn #LocalDiffeomorphismBetweenCartesianSpaces}
###### Definition
**([[local diffeomorphisms]] and [[open embeddings]] of [[Cartesian spaces]])**

A [[smooth function]] $f \colon \mathbb{R}^{n} \to \mathbb{R}^{n}$ from one [[Cartesian space]] to itself
(def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}) is called a _[[local diffeomorphism]]_, denoted

$$
  f \;\colon\; \mathbb{R}^{n} \overset{et}{\longrightarrow} \mathbb{R}^n
$$

if the [[determinant]] of the [[matrix]] of [[partial derivatives]] (the "[[Jacobian]]" of $f$) is
everywhere non-vanishing

$$
  det
  \left(
   \array{
     \frac{\partial f^1}{\partial x^1}(x)
     &\cdots&
     \frac{\partial f^n}{\partial x^1}(x)
     \\
     \vdots && \vdots
     \\
     \frac{\partial f^1}{\partial x^n}(x)
     &\cdots&
     \frac{\partial f^n}{\partial x^n}(x)
   }
  \right)
  \;\neq\;
  0
  \phantom{AAAA}
  \text{for all} \, x \in \mathbb{R}^n
  \,.
$$

If the function $f$ is both a [[local diffeomorphism]], as above, as well as an [[injective function]] then
we call it an _[[open embedding]]_, denoted

$$
  f \;\colon\;
  \mathbb{R}^n \overset{\phantom{A}et\phantom{A}}{\hookrightarrow} \mathbb{R}^n
  \,.
$$

=--

+-- {: .num_defn #DifferentiablyGoodOpenCover}
###### Definition
**([[good open cover]] of [[Cartesian spaces]])**

For $\mathbb{R}^n$ a [[Cartesian space]] (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}),
a _[[differentiably good open cover]]_ is

*  an [[indexed set]]

   $$
      \left\{
        \mathbb{R}^n
          \underoverset{et}{\phantom{AA}f_i\phantom{AA}}{\hookrightarrow}
        \mathbb{R}^n
      \right\}_{i \in I}
   $$

   of [[open embeddings]]
   (def. \ref{LocalDiffeomorphismBetweenCartesianSpaces})

such that the [[images]]

$$
  U_i \coloneqq im(f_i) \subset \mathbb{R}^n
$$

satisfy:

1. ([[open cover]]) every point of $\mathbb{R}^n$ is contained in at least one of the $U_i$;

1. ([[good open cover|good]]) all [[finite set|finite]] [[intersections]] $U_{i_1} \cap \cdots \cap U_{i_k} \subset \mathbb{R}^n$ are either [[empty set]] or  themselves images of [[open embeddings]] according to def. \ref{LocalDiffeomorphismBetweenCartesianSpaces}.

The inclined reader may notice that the concept of [[differentiably good open covers]] from def. \ref{DifferentiablyGoodOpenCover}
is a _[[coverage]]_ on the [[category]] _[[CartSp]]_ of [[Cartesian spaces]] with [[smooth functions]] between them, making it a
_[[site]]_, but the reader not so inclined may ignore this.

=--

([[schreiber:Cech Cocycles for Differential characteristic Classes|Fiorenza-Schreiber-Stasheff 12, def. 6.3.9]])

$\,$


$\,$

**[[fiber bundles]]**
 {#BundlesAndSections}

Given any context of [[objects]] and [[morphisms]] between them, such as the [[Cartesian spaces]]
and [[smooth functions]] from def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}
it is of interest to fix one [[object]] $X$ and consider other objects _[[dependent type|parameterized over]]_
it. These are called _[[bundles]]_ (def. \ref{BundlesAndFibers}) below.
For reference, we briefly discuss here the basic concepts related to [[bundles]] in the context of
[[Cartesian spaces]].

Of course the theory of bundles is mostly trivial over Cartesian spaces;
it gains its main interest from its generalization to more general [[smooth manifolds]] (def./prop. \ref{SmoothManifoldInsideDiffeologicalSpaces} below).
It is still worthwhile for our development to first consider the relevant concepts in this simple case first.

For more exposition see at _[[fiber bundles in physics]]_.

$\,$

+-- {: .num_defn #BundlesAndFibers}
###### Definition
**([[bundles]])**

We say that a [[smooth function]] $E \overset{fb}{\to} X$ (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem})
is a _[[bundle]]_ just to amplify that we think of it as exhibiting $E$ as being a "space over $X$":

$$
  \array{
    E
    \\
    \downarrow\mathrlap{fb}
    \\
    X
  }
  \,.
$$

For $x \in X$ a point, we say that the _[[fiber]]_ of this [[bundle]] over $x$ is the [[pre-image]]

$$
  \label{FiberOfAFiberBundle}
  E_x \coloneqq fb^{-1}(\{x\}) \subset E
$$

of the point $x$ under the smooth function. We think of $fb$ as exhibiting a "smoothly varying" set of [[fiber]] spaces over $X$.

Given two [[bundles]] $E_1 \overset{fb_1}{\to} X$ and $E_2 \overset{fb_2}{\to} X$ over $X$,
a _[[homomorphism]] of bundles_ between them is a [[smooth function]]
$f \colon E_1 \to E_2$ (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}) between their
total spaces which respects the bundle projections, in that

$$
  fb_2  \circ f = fb_1
  \phantom{AAAA}
  \text{i.e.}
  \phantom{AAA}
  \array{
    E_1 && \overset{f}{\longrightarrow} && E_2
    \\
    & {}_{\mathllap{fb_1}}\searrow && \swarrow_{\mathrlap{fb_2}}
    \\
    && X
  }
  \,.
$$

Hence a bundle homomorphism is a smooth function that sends [[fibers]] to [[fibers]] over the same point:

$$
  f\left(
    (E_1)_x
  \right)
    \;\subset\;
  (E_2)_x
  \,.
$$

The inclined reader may notice that this defines a [[category]] of [[bundles]] over $X$,
which is in fact just the _[[slice category]]_ $CartSp_{/X}$; the reader not so inclined may ignore this.

=--


+-- {: .num_defn #Sections}
###### Definition
**([[sections]])**

Given a [[bundle]] $E \overset{fb}{\to} X$ (def. \ref{BundlesAndFibers})
a _[[section]]_ is a [[smooth function]] $s \colon X \to E$ such that

$$
  fb \circ s = id_X
  \phantom{AAAAA}
  \array{
    && E
    \\
    &
    {}^{\mathllap{s}}\nearrow
    & \downarrow\mathrlap{fb}
    \\
    X &=& X
  }
  \,.
$$

This means that $s$ sends every point $x \in X$ to an element in the [[fiber]] over that point

$$
  s(x) \in E_x
  \,.
$$

We write

$$
  \Gamma_X(E) \coloneqq
  \left\{
     \array{
        && E
        \\
        & {}^{\mathllap{s}}\nearrow & \downarrow^\mathrlap{fb}
        \\
        X &=& X
     }
     \phantom{fb}
  \right\}
$$

for the [[space of sections|set of sections]] of a bundle.

For $E_1 \overset{f_1}{\to} X$ and $E_2 \overset{f_2}{\to} X$ two [[bundles]] and for

$$
  \array{
    E_1
      && \overset{f}{\longrightarrow} &&
    E_2
    \\
    & {}_{\mathllap{fb_1}}\searrow && \swarrow_{\mathrlap{fb_2}}
    \\
    && X
  }
$$

a bundle [[homomorphism]] between them (def. \ref{BundlesAndFibers}), then [[composition]] with $f$ sends [[sections]] to [[sections]]
and hence yields a [[function]] denoted

$$
  \array{
    \Gamma_X(E_1)
      &\overset{f_\ast}{\longrightarrow}&
    \Gamma_X(E_2)
    \\
    s &\mapsto& f \circ s
  }
  \,.
$$

=--


+-- {: .num_example #TrivialBundleOnCartesianSpace}
###### Example
**([[trivial bundle]])**

For $X$ and $F$  [[Cartesian spaces]], then the [[Cartesian product]] $X \times F$ equipped with the [[projection]]

$$
  \array{
    X \times F
    \\
    \downarrow^\mathrlap{pr_1}
    \\
    X
  }
$$

to $X$ is a [[bundle]] (def. \ref{BundlesAndFibers}), called the _[[trivial bundle]]_
with [[fiber]] $F$. This represents the _constant_ smoothly varying set of [[fibers]], constant on $F$

If $F = \ast$ is the point, then this is the identity bundle

$$
  \array{
    X
    \\
    \downarrow\mathrlap{id}
    \\
    X
  }
  \,.
$$

Given any [[bundle]] $E \overset{fb}{\to} X$, then a bundle homomorphism (def. \ref{BundlesAndFibers})
from the identity bundle to $E \overset{fb}{\to} X$ is equivalently a [[section]] of $E \overset{fb}{\to} X$ (def. \ref{Sections})

$$
  \array{
     X && \overset{s}{\longrightarrow} && E
     \\
     & {}_{\mathllap{id}}\searrow && \swarrow_{\mathrlap{fb}}
     \\
     && X
  }
$$

=--

+-- {: .num_defn #FiberBundle}
###### Definition
**([[fiber bundle]])**

A [[bundle]] $E \overset{fb}{\to} X$ (def. \ref{BundlesAndFibers}) is called a _[[fiber bundle]]_ with _typical fiber_ $F$ if
there exists a [[differentiably good open cover]] $\{U_i \hookrightarrow X\}_{i \in I}$ (def. \ref{DifferentiablyGoodOpenCover})
such that the restriction of $fb$ to each $U_i$ is [[isomorphism|isomorphic]] to the [[trivial fiber bundle]] with
fiber $F$ over $U_i$. Such [[diffeomorphisms]] $f_i \colon U_i \times F \overset{\simeq}{\to} E\vert_{U_i}$
are called _[[local trivializations]]_ of the fiber bundle:

$$
  \array{
    U_i \times F &\underoverset{\simeq}{f_i}{\longrightarrow}& E\vert_{U_i}
    \\
    & {}_{\mathllap{pr_1}}\searrow & \downarrow\mathrlap{fb\vert_{U_i}}
    \\
    && U_i
  }
  \,.
$$


=--


+-- {: .num_defn #VectorBundle}
###### Definition
**([[vector bundle]])**

A _[[vector bundle]]_ is a [[fiber bundle]] $E \overset{vb}{\to} X$ (def. \ref{FiberBundle}) with typical fiber a [[vector space]] $V$ such that
there exists a [[local trivialization]] $\{U_i \times V \underoverset{\simeq}{f_i}{\to} E\vert_{U_i}\}_{i \in I}$
whose _gluing functions_

$$
  U_i \cap U_j \times V
    \overset{f_i\vert_{U_i \cap U_j}}{\longrightarrow}
  E\vert_{U_i \cap U_j}
    \overset{f_j^{-1}\vert_{U_i \cap U_j}}{\longrightarrow}
  U_i \cap U_j \times V
$$

for all $i,j \in I$ are [[linear functions]] over each point $x \in U_i \cap U_j$.

A [[homomorphism]] of [[vector bundle]] is a bundle morphism $f$ (def. \ref{BundlesAndFibers})
such that there exist [[local trivializations]] on both sides with respect to which $g$ is
[[fiber]]-wise a [[linear map]].

The inclined reader may notice that this makes vector bundles over $X$ a [[category]] (denoted $Vect_{/X}$);
the reader not so inclined may ignore this.

=--

+-- {: .num_example #ModuleOfSectionsOfAVectorBundle}
###### Example
**([[module]] of [[sections]] of a [[vector bundle]])**

Given a [[vector bundle]] $E \overset{vb}{\to} X$ (def. \ref{VectorBundle}),
then its [[space of sections|set of sections]] $\Gamma_X(E)$ (def. \ref{BundlesAndFibers})
becomes a [[real vector space]] by [[fiber]]-wise multiplication with [[real numbers]].
Moreover, it becomes a [[module]] over the [[algebra of functions|algebra of]] [[smooth functions]] $C^\infty(X)$
(example \ref{AlgebraOfSmoothFunctionsOnCartesianSpaces}) by the same [[fiber]]-wise multiplication:

$$
  \array{
     C^\infty(X) \otimes_{\mathbb{R}} \Gamma_X(E) &\longrightarrow& \Gamma_X(E)
     \\
     (f,s) &\mapsto& (x \mapsto f(x) \cdot s(x))
  }
  \,.
$$

For $E_1 \overset{fb_1}{\to} X$ and $E_2 \overset{fb_2}{\to} X$ two [[vector bundles]] and

$$
  \array{
    E_1 && \overset{f}{\longrightarrow} && E_2
    \\
    & {}_{\mathllap{fb_1}}\searrow && \swarrow_{\mathrlap{fb_2}}
    \\
    && X
  }
$$

a vector bundle homomorphism (def. \ref{VectorBundle}) then the induced function on sections (def. \ref{Sections})

$$
  f_\ast \;\colon\; \Gamma_X(E_1) \longrightarrow \Gamma_X(E_2)
$$

is compatible with this [[action]] by smooth functions and hence constitutes a [[homomorphism]] of $C^\infty(X)$-[[modules]].

The inclined reader may notice that this means that taking [[spaces of sections]] yields a [[functor]]

$$
  \Gamma_X(-)
  \;\colon\;
  Vect_{/X}
    \longrightarrow
  C^\infty(X) Mod
$$

from the [[category of vector bundles]] over $X$ to that over [[modules]] over $C^\infty(X)$.

=--


+-- {: .num_example #TangentVectorFields}
###### Example
**([[tangent vector fields]] and [[tangent bundle]])**

For $\mathbb{R}^n $ a [[Cartesian space]] (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem})
the [[trivial vector bundle]] (example \ref{TrivialBundleOnCartesianSpace}, def. \ref{VectorBundle})

$$
  \array{
    T \mathbb{R}^n &\coloneqq& \mathbb{R}^n \times \mathbb{R}^n
    \\
    \mathllap{tb}\downarrow && \downarrow\mathrlap{pr_1}
    \\
    \mathbb{R}^n &=& \mathbb{R}^n
  }
$$

is called the _[[tangent bundle]]_ of $\mathbb{R}^n$. With $(x^a)_{a = 1}^n$ the [[coordinate functions]]
on $\mathbb{R}^n$ (def. \ref{CoordinateFunctionsAreSmoothFunctions}) we write $(\partial_a)_{a = 1}^n$
for the corresponding [[linear basis]] of $\mathbb{R}^n$ regarded as a [[vector space]]. Then
a general [[section]] (def. \ref{Sections})

$$
  \array{
    && T \mathbb{R}^n
    \\
    & {}^{\mathllap{v}}\nearrow& \downarrow\mathrlap{tb}
    \\
    \mathbb{R}^n &=& \mathbb{R}^n
  }
$$

of the [[tangent bundle]] has a unique expansion of the form

$$
  v = v^a \partial_a
$$

where a sum over indices is understood ([[Einstein summation convention]]) and where
the components $(v^a \in C^\infty(\mathbb{R}^n))_{a = 1}^n$
are [[smooth functions]] on $\mathbb{R}^n$ (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}).

Such a $v$ is also called a smooth _[[tangent vector field]]_ on $\mathbb{R}^n$.

Each tangent vector field $v$ on $\mathbb{R}^n$ determines a [[partial derivative]]
on [[smooth functions]]

$$
  \array{
    C^\infty(\mathbb{R}^n) &\overset{D_v}{\longrightarrow}& C^\infty(\mathbb{R}^n)
    \\
    f &\mapsto& \mathrlap{ D_v f \coloneqq v^a \partial_a (f) \coloneqq  \sum_a v^a \frac{\partial f}{\partial x^a} }
  }
  \,.
$$

By the [[product law]] of [[differentiation]], this is a [[derivation]] on the [[algebra of functions|algebra of]] [[smooth functions]]
(example \ref{AlgebraOfSmoothFunctionsOnCartesianSpaces}) in that

1. it is an $\mathbb{R}$-[[linear map]] in that

   $$
     D_v( c_1 f_1 + c_2 f_2 ) = c_1 D_v f_1 + c_2 D_v f_2
   $$

1. it satisfies the [[Leibniz rule]]

   $$
     D_v(f_1 \cdot f_2) = (D_v f_1) \cdot f_2 + f_1 \cdot (D_v f_2)
   $$

for all $c_1, c_2 \in \mathbb{R}$ and all $f_1, f_2 \in C^\infty(\mathbb{R}^n)$.

Hence regarding [[tangent vector fields]] as [[partial derivatives]] constitutes a [[linear function]]

$$
  D \;\colon\; \Gamma_{\mathbb{R}^n}(T \mathbb{R}^n) \longrightarrow Der(C^\infty(\mathbb{R}^n))
$$

from the [[space of sections]] of the [[tangent bundle]]. In fact this is
a [[homomorphism]] of $C^\infty(\mathbb{R}^n)$-[[modules]] (example \ref{ModuleOfSectionsOfAVectorBundle}),
in that for $f \in C^\infty(\mathbb{R}^n)$ and $v \in \Gamma_{\mathbb{R}^n}(T \mathbb{R}^n)$ we have

$$
  D_{f v}(-) = f \cdot D_v(-)
  \,.
$$

=--


+-- {: .num_example #VerticalTangentBundle}
###### Example
**([[vertical tangent bundle]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[fiber bundle]]. Then its _[[vertical tangent bundle]]_ $T_\Sigma E \overset{T fb}{\to} \Sigma$ is the [[fiber bundle]] (def. \ref{FiberBundle}) over $\Sigma$ whose [[fiber]] over a point is the [[tangent bundle]] (def. \ref{TangentVectorFields}) of the fiber of $E \overset{fb}{\to}\Sigma$ over that point:

$$
  (T_\Sigma E)_x \coloneqq T(E_x)
  \,.
$$

If $E \simeq \Sigma \times F$ is a [[trivial fiber bundle]] with [[fiber]] $F$, then its vertical vector bundle is the trivial fiber bundle with fiber $T F$.

=--


+-- {: .num_defn #DualVectorBundle}
###### Definition
**([[dual vector bundle]])**

For $E \overset{vb}{\to} \Sigma$ a [[vector bundle]] (def. \ref{VectorBundle}), its
_[[dual vector bundle]]_ is the vector bundle whose [[fiber]] (eq:FiberOfAFiberBundle) over $x \in \Sigma$ is the
[[dual vector space]] of the corresponding fiber of $E \to \Sigma$:

$$
  (E^\ast)_x \;\coloneqq\; (E_x)^\ast
  \,.
$$

The defining pairing of [[dual vector spaces]] $(E_x)^\ast \otimes E_x \to \mathbb{R}$ applied
pointwise induces a pairing on the [[modules]] of [[sections]] (def. \ref{ModuleOfSectionsOfAVectorBundle})
of the original vector bundle and its dual with values in the [[smooth functions]] (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}):

$$
  \label{PairingOfDualSections}
  \array{
    \Gamma_\Sigma(E) \otimes_{C^\infty(X)} \Gamma_\Sigma(E^\ast)
      &\longrightarrow&
    C^\infty(\Sigma)
    \\
    (v,\alpha) &\mapsto& (v \cdot \alpha \colon x \mapsto \alpha_x(v_x) )
  }
$$


=--


$\,$

**[[synthetic differential geometry]]**
 {#SyntheticDifferentialGeometry}

Below we encounter generalizations of ordinary [[differential geometry]] that include
explicit "[[infinitesimals]]" in the guise of _[[infinitesimally thickened points]]_,
as well as "super-graded infinitesimals", in the guise of _[[superpoints]]_ (necessary for the
description of [[fermion fields]] such as the [[Dirac field]]). As we discuss [below](#FieldBundles), these structures are
naturally incorporated into [[differential geometry]] in just the same way as [[Grothendieck]]
introduced them into [[algebraic geometry]] (in the guise of "[[formal schemes]]"),
namely in terms of [[formal dual|formally dual]] [[rings of functions]] with [[nilpotent ideals]].
That this also works well for [[differential geometry]] rests on the following three
basic but important properties, which say that [[smooth functions]] behave "more algebraically"
than their definition might superficially suggest:


+-- {: .num_prop #AlgebraicFactsOfDifferentialGeometry}
###### Proposition
**(the three magic algebraic properties of [[differential geometry]])**

1. **[[embedding of smooth manifolds into formal duals of R-algebras|embedding of Cartesian spaces into formal duals of R-algebras]]**

   For $X$ and $Y$ two [[Cartesian spaces]], the [[smooth functions]] $f \colon X \longrightarrow Y$
   between them (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}) are in [[natural bijection]] with their
   induced algebra [[homomorphisms]] $C^\infty(X) \overset{f^\ast}{\longrightarrow} C^\infty(Y)$ (example \ref{AlgebraOfSmoothFunctionsOnCartesianSpaces}), so that
   one may equivalently handle [[Cartesian spaces]] entirely via their $\mathbb{R}$-algebras of smooth functions.

   Stated more [[category theory|abstractly]], this means equivalently that the [[functor]] $C^\infty(-)$ that
   sends a [[smooth manifold]] $X$ to its $\mathbb{R}$-[[associative algebra|algebra]]
   $C^\infty(X)$ of [[smooth functions]] (example \ref{AlgebraOfSmoothFunctionsOnCartesianSpaces}) is a _[[fully faithful functor]]_:

   $$
     C^\infty(-)
     \;\colon\;
     SmthMfd \overset{\phantom{AAAA}}{\hookrightarrow} \mathbb{R} Alg^{op}
     \,.
   $$

   ([Kolar-Slovak-Michor 93, lemma 35.8, corollaries 35.9, 35.10](embedding+of+smooth+manifolds+into+formal+duals+of+R-algebras#KolarSlovakMichor93))


1. **[[smooth Serre-Swan theorem|embedding of smooth vector bundles into formal duals of R-algebra modules]]**

   For $E_1 \overset{vb_1}{\to} X$ and $E_2 \overset{vb_2}{\to} X$ two [[vector bundle]] (def. \ref{VectorBundle})
   there is then a [[natural bijection]] between vector bundle [[homomorphisms]] $f \colon E_1 \to E_2$
   and the [[homomorphisms]] of [[modules]] $f_\ast \;\colon\; \Gamma_X(E_1) \to \Gamma_X(E_2)$
   that these induces between the [[spaces of sections]] (example \ref{ModuleOfSectionsOfAVectorBundle}).

   More [[category theory|abstractly]] this means that the [[functor]] $\Gamma_X(-)$ is a [[fully faithful functor]]

   $$
     \Gamma_X(-) \;\colon\; VectBund_X \overset{\phantom{AAAA}}{\hookrightarrow} C^\infty(X) Mod
   $$

   ([Nestruev 03, theorem 11.29](smooth+Serre-Swan theorem#Nestruev03))

   Moreover, the [[modules]] over the $\mathbb{R}$-algebra $C^\infty(X)$
   of [[smooth functions]] on $X$ which arise this way as [[sections]] of [[smooth vector bundles]] over
   a [[Cartesian space]] $X$
   are precisely the [[finitely generated module|finitely generated]] [[free modules]] over $C^\infty(X)$.

   ([Nestruev 03, theorem 11.32](smooth+Serre-Swan theorem#Nestruev03))


1. **[[derivations of smooth functions are vector fields|vector fields are derivations of smooth functions]]**.

   For $X$ a [[Cartesian space]] (example \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}),
   then any [[derivation]] $D \colon  C^\infty(X) \to C^\infty(X)$ on
   the $\mathbb{R}$-[[associative algebra|algebra]]
   $C^\infty(X)$ of [[smooth functions]] (example \ref{AlgebraOfSmoothFunctionsOnCartesianSpaces}) is given by [[differentiation]] with respect to a uniquely defined smooth [[tangent vector field]]: The function that regards [[tangent vector fields]]
   with [[derivations]] from example \ref{TangentVectorFields}

   $$
     \array{
       \Gamma_X(T X)
         &\overset{\phantom{A}\simeq\phantom{A}}{\longrightarrow}&
       Der(C^\infty(X))
       \\
       v &\mapsto& D_v
     }
   $$

   is in fact an [[isomorphism]].

   (This follows directly from the _[[Hadamard lemma]]_.)

=--

Actually all three statements in prop. \ref{AlgebraicFactsOfDifferentialGeometry}
hold not just for [[Cartesian spaces]], but generally for [[smooth manifolds]] (def./prop. \ref{SmoothManifoldInsideDiffeologicalSpaces} below; if only we generalize in the second statement from [[free modules]] to [[projective modules]].
However for our development here it is useful to first focus on just [[Cartesian spaces]] and then bootstrap
the theory of [[smooth  manifolds]] and much more from that, which we do [below](#FieldBundles).


$\,$


$\,$



**[[differential forms]]**
 {#DifferentialFormsAndCartanCalculus}

We introduce and discuss [[differential forms]] on [[Cartesian spaces]].

+-- {: .num_defn #Differential1FormsOnCartesianSpaces}
###### Definition
**([[differential 1-forms]] on [[Cartesian spaces]] and the [[cotangent bundle]])**

For $n \in \mathbb{N}$ a _[[smooth differential 1-form]]_ $\omega$ on a [[Cartesian space]] $\mathbb{R}^n$ (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}) is an [[n-tuple]]

$$
  \left(\omega_i \in CartSp\left(\mathbb{R}^n,\mathbb{R}\right)\right)_{i = 1}^n
$$

of [[smooth functions]] (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}), which we think of equivalently as the [[coefficients]] of a [[formal linear combination]]

$$
  \omega = \omega_i d x^i
$$

on a [[set]] $\{d x^1, d x^2, \cdots, d x^n\}$ of [[cardinality]] $n$.

Here a sum over repeated indices is tacitly understood ([[Einstein summation convention]]).

Write

$$
  \Omega^1(\mathbb{R}^k) \simeq CartSp(\mathbb{R}^k, \mathbb{R})^{\times k}\in Set
$$

for the set of smooth [[differential 1-forms]] on $\mathbb{R}^k$.

We may think of the expressions $(d x^a)_{a = 1}^n$ as a [[linear basis]] for the [[dual vector space]]
$\mathbb{R}^n$. With this the [[differential 1-forms]] are equivalently the [[sections]] (def. \ref{Sections})
of the [[trivial vector bundle]] (example \ref{TrivialBundleOnCartesianSpace}, def. \ref{VectorBundle})

$$
  \array{
    T^\ast \mathbb{R}^n &\coloneqq& \mathbb{R}^n \times (\mathbb{R}^n)^\ast
    \\
    \mathllap{cb}\downarrow && \downarrow\mathrlap{pr_1}
    \\
    \mathbb{R}^n &=& \mathbb{R}^n
  }
$$

called the _[[cotangent bundle]]_ of $\mathbb{R}^n$ (def. \ref{Differential1FormsOnCartesianSpaces}):

$$
  \Omega^1(\mathbb{R}^n) = \Gamma_{\mathbb{R}^n}(T^\ast \mathbb{R}^n)
  \,.
$$

This amplifies via example \ref{ModuleOfSectionsOfAVectorBundle} that $\Omega^1(\mathbb{R}^n)$
has the  [[structure]] of a [[module]] over the [[algebra of functions|algebra of]] [[smooth functions]] $C^\infty(\mathbb{R}^n)$,
by the evident multiplication of [[differential 1-forms]] with [[smooth functions]]:

1. The set $\Omega^1(\mathbb{R}^k)$ of [[differential 1-forms]] in a [[Cartesian space]] (def. \ref{Differential1FormsOnCartesianSpaces})
   is naturally an [[abelian group]] with addition given by componentwise addition

   $$
      \begin{aligned}
         \omega + \lambda & =
          \omega_i d x^i + \lambda_i d x^i
         \\
         & = (\omega_i + \lambda_i) d x^i
      \end{aligned}
      \,,
   $$

1. The abelian group $\Omega^1(\mathbb{R}^k)$ is naturally equipped with the structure of a [[module]] over the
   [[algebra of functions|algebra of]] [[smooth functions]] $C^\infty(\mathbb{R}^k)$ (example \ref{AlgebraOfSmoothFunctionsOnCartesianSpaces}), where the [[action]] $C^\infty(\mathbb{R}^k) \times\Omega^1(\mathbb{R}^k) \to \Omega^1(\mathbb{R}^k)$ is given by componentwise multiplication

   $$
     f \cdot \omega = ( f \cdot \omega_i) d x^i
     \,.
   $$


Accordingly there is a canonical pairing between [[differential 1-forms]] and [[tangent vector fields]] (example \ref{TangentVectorFields})

$$
  \label{PairingVectorFieldsWithDifferential1Forms}
  \array{
    \Gamma_{\mathbb{R}^n}(T \mathbb{R}^n)
    \otimes_{\mathbb{R}}
    \Gamma_{\mathbb{R}^n}(T \ast \mathbb{R}^n)
      &\overset{\iota_{(-)}(-) }{\longrightarrow}&
    C^\infty(\mathbb{R}^n)
    \\
    (v,\omega)
    &\mapsto&
    \mathrlap{
      \iota_v \omega \coloneqq v^a \omega_a
    }
  }
$$

With [[differential 1-forms]] in hand, we may collect all the first-order [[partial derivatives]] of a [[smooth function]]
into a single object: the _[[exterior derivative]]_ or _[[de Rham differential]]_ is the $\mathbb{R}$-[[linear function]]

$$
  \label{deRhamDifferentialOnFunctionsOnCartesianSpace}
  \array{
    C^\infty(\mathbb{R}^n) &\overset{d}{\longrightarrow}& \Omega^1(\mathbb{R}^n)
    \\
    f &\mapsto& \mathrlap{ d f \coloneqq \frac{\partial f}{ \partial x^a} d x^a }
  }
  \,.
$$

Under the above pairing with [[tangent vector fields]] $v$ this yields the particular [[partial derivative]] along $v$:

$$
  \iota_v d f = D_v f = v^a \frac{\partial f}{\partial x^a}
  \,.
$$

=--


We think of $d  x^i$ as a measure for [[infinitesimal space|infinitesimal]] displacements along the $x^i$-[[coordinate]] of a [[Cartesian space]]. If we have a measure of infintesimal displacement on some $\mathbb{R}^n$ and a smooth function $f \colon \mathbb{R}^{\tilde n} \to \mathbb{R}^n$, then this induces a measure for infinitesimal displacement on $\mathbb{R}^{\tilde n}$ by sending whatever happens there first with  $f$ to $\mathbb{R}^n$ and then applying the given measure there. This is captured by the following definition:

+-- {: .num_defn #PullbackOfDifferential1FormsOnCartesianSpaces}
###### Definition
**([[pullback of differential forms|pullback of differential 1-forms]])**

For $\phi \colon \mathbb{R}^{\tilde k} \to \mathbb{R}^k$ a [[smooth function]], the **[[pullback of differential forms|pullback of differential 1-forms]]** along $\phi$ is the [[function]]

$$
  \phi^* \colon \Omega^1(\mathbb{R}^{k}) \to \Omega^1(\mathbb{R}^{\tilde k})
$$

between sets of differential 1-forms, def. \ref{Differential1FormsOnCartesianSpaces}, which is defined on [[basis]]-elements by

$$
  \phi^* d  x^i
    \;\coloneqq\;
  \frac{\partial \phi^i}{\partial \tilde x^j} d \tilde x^j
$$

and then extended linearly by

$$
  \begin{aligned}
    \phi^* \omega & = \phi^* \left(  \omega_i d x^i \right)
    \\
    & \coloneqq
      \left(\phi^* \omega\right)_i  \frac{\partial \phi^i }{\partial \tilde x^j}  d  \tilde x^j
    \\
    & =
     (\omega_i \circ \phi) \cdot \frac{\partial \phi^i }{\partial \tilde x^j}  d  \tilde x^j
  \end{aligned}
  \,.
$$

This is compatible with [[identity morphisms]] and [[composition]] in that

$$
  \label{PullbackOfDifferentialFormsCompatibleWithComposition}
  (id_{\mathbb{R}^n})^\ast = id_{\Omega^1(\mathbb{R}^n)}
  \phantom{AAAA}
  (g \circ f)^\ast = f^\ast \circ g^\ast
  \,.
$$

Stated more [[category theory|abstractly]], this just means that [[pullback of differential forms|pullback of differential 1-forms]]
makes the assignment of sets of differential 1-forms to [[Cartesian spaces]] a [[contravariant functor|contravariant]] [[functor]]

$$
  \Omega^1(-) \;\colon\; CartSp^{op} \longrightarrow Set
  \,.
$$


=--


The following definition captures the idea that if $d  x^i$ is a measure for displacement along the $x^i$-[[coordinate]], and $d x^j$ a measure for displacement along the $x^j$ coordinate, then there should be a way to get a measure, to be called $d x^i \wedge d  x^j$, for [[infinitesimal]] _[[surfaces]]_ (squares) in the $x^i$-$x^j$-plane. And this should keep track of the [[orientation]] of these squares, with

$$
  d x^j \wedge d x^i = - d x^i \wedge d  x^j
$$

being the same infinitesimal measure with orientation reversed.

+-- {: .num_defn #DifferentialnForms}
###### Definition
**([[exterior algebra]] of [[differential n-forms]])**

For $k,n \in \mathbb{N}$, the **smooth [[differential forms]]** on a [[Cartesian space]] $\mathbb{R}^k$ (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}) is the [[exterior algebra]]

$$
  \Omega^\bullet(\mathbb{R}^k)
   \coloneqq
  \wedge^\bullet_{C^\infty(\mathbb{R}^k)} \Omega^1(\mathbb{R}^k)
$$

over the [[algebra of functions|algebra of]] [[smooth functions]] $C^\infty(\mathbb{R}^k)$ (example \ref{AlgebraOfSmoothFunctionsOnCartesianSpaces}) of the [[module]] $\Omega^1(\mathbb{R}^k)$ of smooth 1-forms.

We write $\Omega^n(\mathbb{R}^k)$ for the sub-module of degree $n$ and call its elements the _[[differential n-forms]]_.

Explicitly this means that a [[differential n-form]] $\omega \in \Omega^n(\mathbb{R}^k)$ on $\mathbb{R}^k$ is a [[formal linear combination]] over $C^\infty(\mathbb{R}^k)$ (example \ref{AlgebraOfSmoothFunctionsOnCartesianSpaces}) of [[basis]] elements of the form $d  x^{i_1} \wedge \cdots \wedge d x^{i_n}$ for $i_1 \lt i_2 \lt \cdots \lt i_n$:

$$
  \omega = \omega_{i_1, \cdots, i_n} d x^{i_1} \wedge \cdots \wedge d x^{i_n}
  \,.
$$

=--

Now all the constructions for [[differential 1-forms]] above extent naturally to [[differential n-forms]]:


+-- {: .num_defn #deRhamDifferential}
###### Definition
**([[exterior derivative]] or [[de Rham differential]])**

For $\mathbb{R}^n$ a [[Cartesian space]] (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem})
the [[de Rham differential]] $d \colon C^\infty(\mathbb{R}^n) \to \Omega^1(\mathbb{R}^n)$
(eq:deRhamDifferentialOnFunctionsOnCartesianSpace) uniquely extended as a [[derivation]]
of degree +1 to the [[exterior algebra]] of [[differential forms]] (def. \ref{DifferentialnForms})

$$
  d
    \;\colon\;
  \Omega^\bullet(\mathbb{R}^n)
    \longrightarrow
  \Omega^\bullet(\mathbb{R}^n)
$$

meaning that for $\omega_i \in \Omega^{k_i}(\mathbb{R})$ then

$$
  d(\omega_1 \wedge \omega_2)
  \;=\;
  (d \omega_1) \wedge \omega_2
  +
  \omega_1 \wedge d \omega_2
  \,.
$$

In components this simply means that

$$
  \begin{aligned}
    d \omega
    & =
    d \left(\omega_{i_1 \cdots i_k} d x^{i_1} \wedge \cdots \wedge d x^{i_k}\right)
    \\
    & =
    \frac{\partial \omega_{i_1 \cdots i_k}}{\partial x^{a}}
    d x^a \wedge d x^{i_1} \wedge \cdots \wedge d x^{i_k}
  \end{aligned}
  \,.
$$

Since [[partial derivatives]] commute with each other, while differential 1-form anti-commute, this implies
that $d$ is nilpotent

$$
  d^2 = d \circ d = 0
  \,.
$$

We say hence that [[differential forms]] form a _[[cochain complex]]_, the _[[de Rham complex]]_
$(\Omega^\bullet(\mathbb{R}^n), d)$.

=--


+-- {: .num_defn #ContractionOfFormsWithVectorFields}
###### Definition
**(contraction of [[differential n-forms]] with [[tangent vector fields]])**

The pairing $\iota_v \omega = \omega(v)$ of [[tangent vector fields]] $v$ with [[differential 1-forms]] $\omega$ (eq:PairingVectorFieldsWithDifferential1Forms) uniquely [[extension|extends]] to the [[exterior algebra]] $\Omega^\bullet(\mathbb{R}^n)$ of [[differential forms]] (def. \ref{DifferentialnForms}) as a [[derivation]] of degree -1

$$
  \iota_v \;\colon\; \Omega^{\bullet+1}(\mathbb{R}^n) \longrightarrow \Omega^\bullet(\mathbb{R}^n)
  \,.
$$

In particular for $\omega_1, \omega_2 \in \Omega^1(\mathbb{R}^n)$ two [[differential 1-forms]], then

$$
  \iota_{v} (\omega_1 \wedge \omega_2)
   \;=\;
  \omega_1(v) \omega_2 - \omega_2(v) \omega_1
  \;\in\;
  \Omega^1(\mathbb{R}^n)
  \,.
$$


=--

+-- {: .num_prop #PullbackOfDifferentialForms}
###### Proposition
**([[pullback of differential forms|pullback of differential n-forms]])**

For $f \colon \mathbb{R}^{n_1} \to \mathbb{R}^{n_2}$ a [[smooth function]] between [[Cartesian spaces]]
(def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem})
the operationf of  [[pullback of differential forms|pullback of differential 1-forms]] of def. \ref{Differential1FormsOnCartesianSpaces} extends as an $C^\infty(\mathbb{R}^k)$-[[associative algebra|algebra]] [[homomorphism]] to the [[exterior algebra]]
of [[differential forms]] (def. \ref{DifferentialnForms}),

$$
  f^\ast
  \;\colon\;
  \Omega^\bullet(\mathbb{R}^{n_2})
    \longrightarrow
  \Omega^\bullet(\mathbb{R}^{n_1})
$$

given on basis elements by

$$
  f^* \left(  dx^{i_1} \wedge \cdots \wedge dx^{i_n} \right)
  =
  \left(f^* dx^{i_1} \wedge \cdots \wedge f^* dx^{i_n} \right)
  \,.
$$


This commutes with the [[de Rham differential]] $d$ on both sides (def. \ref{deRhamDifferential}) in that

$$
  d \circ f^\ast
  =
  f^\ast \circ d
  \phantom{AAAAA}
  \array{
    \Omega^\bullet(X) &\overset{f^\ast}{\longleftarrow}& \Omega^\bullet(Y)
    \\
    \mathllap{d}\downarrow && \downarrow\mathrlap{d}
    \\
    \Omega^\bullet(X) &\underset{f^\ast}{\longleftarrow}& \Omega^\bullet(Y)
  }
$$

hence that [[pullback of differential forms]] is a _[[chain map]]_ of [[de Rham complexes]].

This is still compatible with [[identity morphisms]] and [[composition]] in that

$$
  \label{PullbackOfDiffereentialFormsCompatibleWithComposition}
  (id_{\mathbb{R}^n})^\ast = id_{\Omega^1(\mathbb{R}^n)}
  \phantom{AAAA}
  (g \circ f)^\ast = f^\ast \circ g^\ast
  \,.
$$

Stated more [[category theory|abstractly]], this just means that [[pullback of differential forms|pullback of differential n-forms]]
makes the assignment of sets of [[differential n-forms]] to [[Cartesian spaces]] a [[contravariant functor|contravariant]] [[functor]]

$$
  \Omega^n(-) \;\colon\; CartSp^{op} \longrightarrow Set
  \,.
$$


=--



+-- {: .num_prop #CartanHomotopyFormula}
###### Proposition
**([[Cartan's homotopy formula]])**

Let $X$ be a [[Cartesian space]] (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}), and let $v \in \Gamma(T X)$ be
a smooth [[tangent vector field]] (example \ref{TangentVectorFields}).

For $t \in \mathbb{R}$ write $\exp(t v) \colon X \overset{\simeq}{\to} X$ for the [[flow]] by [[diffeomorphisms]]
along $v$ of parameter length $t$.

Then the [[derivative]] with respect to $t$ of the [[pullback of differential forms]] along $\exp(t v)$, hence the [[Lie derivative]]
$\mathcal{L}_v \colon \Omega^\bullet(X) \to \Omega^\bullet(X)$,
 is given by the [[anticommutator]] of the contraction derivation $\iota_v$ (def. \ref{ContractionOfFormsWithVectorFields}) with the [[de Rham differential]] $d$ (def. \ref{deRhamDifferential}):

$$
  \begin{aligned}
    \mathcal{L}_v
      &\coloneqq
    \frac{d}{d t } \exp(t v)^\ast \omega \vert_{t = 0}
    \\
    & =
    \iota_v d \omega + d \iota_v \omega
    \,.
  \end{aligned}
$$

=--

Finally we turn to the concept of [[integration of differential forms]] (def. \ref{IntegrationOfDifferentialFormsOverSmoothSingularChainsInCartesianSpaces} below).
First we need to say what it is that differential forms may be integrated over:

+-- {: .num_defn #SingularSimplicesInCartesianSpaces}
###### Definition
**(smooth [[singular simplicial chains]] in [[Cartesian spaces]])**

For $n \in \mathbb{N}$, the _standard [[n-simplex]]_ in the [[Cartesian space]]
$\mathbb{R}^n$ (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem}) is the
[[subset]]

$$
  \Delta^n
  \;\coloneqq\;
  \left\{
    (x^i)_{i = 1}^n
    \;\vert\;
    0 \leq x^1 \leq \cdots \leq x^n
  \right\}
  \;\subset\;
  \mathbb{R}^n
  \,.
$$

More generally, a _smooth [[singular simplicial complex|singular n-simplex]]_ in a [[Cartesian space]]
$\mathbb{R}^k$ is a [[smooth function]] (def. \ref{CartesianSpacesAndSmoothFunctionsBetweenThem})

$$
  \sigma
    \;\colon\;
  \mathbb{R}^n
    \longrightarrow
  \mathbb{R}^k
  \,,
$$

to be thought of as a smooth extension of its restriction

$$
  \sigma\vert_{\Delta^n}
    \;\colon\;
  \Delta^n
    \longrightarrow
  \mathbb{R}^k
  \,.
$$

(This is called a _[[singular simplicial complex|singular]]_ simplex because there is no condition that
$\Sigma$ be an [[embedding]] in any way, in particular $\sigma$ may be a [[constant function]].)

A [[singular chain]] in $\mathbb{R}^k$ of [[dimension]] $n$ is a [[formal linear combination]] of singular $n$-simplices in $\mathbb{R}^k$.

In particular, given a singular $n+1$-simplex $\sigma$, then its _[[boundary of a simplex|boundary]]_
is a [[singular chain]] of singular $n$-simplices $\partial \sigma$.


=--

+-- {: .num_defn #IntegrationOfDifferentialFormsOverSmoothSingularChainsInCartesianSpaces}
###### Definition
**([[fiber integration|fiber]]-[[integration of differential forms]]) over smooth [[singular chains]] in [[Cartesian spaces]])**

For $n \in \mathbb{N}$ and $\omega \in \Omega^n(\mathbb{R}^n)$ a [[differential n-form]] (def. \ref{DifferentialnForms}),
which may be written as

$$
  \omega = f d x^1 \wedge \cdots d x^n
  \,,
$$

then its [[integration of differential forms|integration]] over the standard [[n-simplex]] $\Delta^n \subset \mathbb{R}^n$ (def. \ref{SingularSimplicesInCartesianSpaces}) is the ordinary [[integral]] (e.g. [[Riemann integral]])

$$
  \int_{\Delta^n} \omega
  \;\coloneqq\;
  \underset{0 \leq x^1 \leq \cdots \leq x^n \leq 1}{\int} f(x^1, \cdots, x^n) \, d x^1 \cdots d x^n
  \,.
$$

More generally, for

1. $\omega \in \Omega^n(\mathbb{R}^k)$ a [[differential n-forms]];

1. $C = \underset{i}{\sum} c_i \sigma_i $ a singular $n$-chain (def. \ref{SingularSimplicesInCartesianSpaces})

in any [[Cartesian space]] $\mathbb{R}^k$. Then the _[[integration of differential forms|integration]]_
of $\omega$ over $x$ is the [[sum]] of the integrations, as above, of the [[pullback of differential forms]] (def. \ref{PullbackOfDifferentialForms}) along all the singular [[n-simplices]] in the chain:

$$
  \int_C \omega
  \;\coloneqq\;
  \underset{i}{\sum}
  c_i
  \int_{\Delta^n} (\sigma_i)^\ast \omega
  \,.
$$

Finally, for $U$ another Cartesian space, then _[[fiber integration]] of differential forms along $U \times C \to U$_
is the linear map

$$
  \int_C \;\colon\; \Omega^{\bullet + dim(C)}(U \times C) \longrightarrow \Omega^\bullet(U)
$$

which on differential forms of the form $\omega_U \wedge \omega$ is given by

$$
  \int_C \omega_U \wedge \omega
   \;\coloneqq\;
  (-1)^{\vert \omega_U\vert} \int_C \omega
  \,.
$$

=--

+-- {: .num_prop #StokesTheorem}
###### Proposition
**([[Stokes theorem]] for [[fiber integration|fiber]]-[[integration of differential forms]])**

For $\Sigma$ a smooth [[singular simplicial chain]] (def. \ref{IntegrationOfDifferentialFormsOverSmoothSingularChainsInCartesianSpaces})
the operation of [[fiber integration|fiber]]-[[integration of differential forms]] along
$U \times \Sigma \overset{pr_1}{\longrightarrow} U$ (def. \ref{IntegrationOfDifferentialFormsOverSmoothSingularChainsInCartesianSpaces})
is compatible with the [[exterior derivative]] $d_U$ on $U$ (def. \ref{deRhamDifferential}) in that

$$
  \begin{aligned}
    d \int_\Sigma \omega
     & =
    (-1)^{dim(\Sigma)} \int_\Sigma d_U \omega
    \\
    & =
    (-1)^{dim(\Sigma)}
    \left(
      \int_\Sigma d \omega
      -
      \int_{\partial \Sigma} \omega
    \right)
  \end{aligned}
  \,,
$$

where $d = d_U + d_\Sigma$ is the [[de Rham differential]] on $U \times \Sigma$ (def. \ref{deRhamDifferential}) and where the second
equality is the _[[Stokes theorem]]_ along $\Sigma$:

$$
  \int_\Sigma d_\Sigma \omega = \int_{\partial \Sigma} \omega
  \,.
$$

=--




$\,$

This concludes our review of the basics of ([[synthetic differential geometry|synthetic]]) [[differential geometry]] on which the following development of quantum field theory is based.
In the [next chapter](#Spacetime) we consider _[[spacetime]]_ and _[[spin]]_.
