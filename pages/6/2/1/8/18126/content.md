

{:principle: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em
;"}






***

This page is a detailed introduction to basic [[topology]].
Starting from scratch (required background is just a basic concept of _[[sets]]_), and amplifying motivation from [[analysis]],
it first develops standard [[point-set topology]] ([[topological spaces]]).
In passing, some basics of [[category theory]] make an informal appearance,
used to transparently summarize some conceptually important aspects of the theory, such as
[[initial topology|initial]] and [[final topologies]] and the [[reflective subcategory|reflection]] into
[[Hausdorff topological space|Hausdorff]] and [[sober topological spaces]].
The second part introduces some basics of [[homotopy theory]], mostly the [[fundamental group]],
and ends with their first application to the classification of [[covering spaces]].

$\,$

main page: _[[Introduction to Topology]]_

**this chapter:** _Introduction to Topology 1 -- Point-set topology_

next chapter: _[[Introduction to Topology -- 2|Introduction to Topology 2 -- Basic Homotopy Theory]]_

$\,$

For introduction to more general and abstract _[[homotopy theory]]_ see instead
at _[[Introduction to Homotopy Theory]]_.


***

$\,$

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Point-set Topology#
* table of contents
{:toc}

$\,$

The idea of _[[topology]]_ is to study "[[spaces]]" with "[[continuous functions]]" between them.
Specifically one considers [[functions]] between [[sets]] (whence "[[point-set topology]]", see [below](#PointSetTopology))
such that there is a concept for what it means that these functions depend
continuously on their arguments, in that that their values do not "jump".
Such a concept of [[continuous function|continuity]] is familiar from [[analysis]] on [[metric spaces]],
(recalled [below](#Continuity)) but the definition in topology generalizes this analytic concept
and renders it more foundational, generalizing the concept of [[metric spaces]] to that of _[[topological spaces]]_.
(def. \ref{TopologicalSpace} below).

Hence [[topology]] is the study of the [[category]] whose [[objects]] are [[topological spaces]], and whose
[[morphisms]] are [[continuous functions]] (see also remark \ref{TopCategory} below).
This category is much more flexible than that of [[metric spaces]], for example it admits the construction of
arbitrary [[quotients]] and [[intersections]] of spaces.
Accordingly, topology underlies or informs many and diverse areas of mathematics, such as
[[functional analysis]], [[operator algebra]], [[manifold]]/[[scheme]] theory, hence [[algebraic geometry]] and [[differential geometry]],
and the study of [[topological groups]], [[topological vector spaces]], [[local  rings]], etc.. Not the least, it gives rise to
the field of [[homotopy theory]], where one considers also continuous deformations of
continuous functions themselves ("[[homotopies]]").
Topology itself has many branches,
such as _[[low-dimensional topology]]_ or _[[topological domain theory]]_.

A popular imagery for the concept of a [[continuous function]] is provided by deformations of [[elasticity|elastic]]
physical bodies, which may be deformed by stretching them without tearing. The canonical illustration is
a continous [[bijection|bijective]] function from the [[torus]] to the surface of a coffee mug, which maps half of the torus to the
handle of the coffee mug, and continuously deforms parts of the other half in order to form the actual cup.
Since the [[inverse function]] to this function is itself continuous,
the torus and the coffee mug, both regarded as [[topological spaces]], are "[[isomorphism|the same]]"
for the purposes of [[topology]], one says they are _[[homeomorphic]]_.

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/Surfaces.png" width="400">
</div>

On the other hand, there is _no_ [[homeomorphism]] from the [[torus]] to, for instance, the [[sphere]], signifying that these
represent two topologically distinct spaces. Part of topology is concerned with studying [[homeomorphism]]-[[invariants]]
of topological spaces ("[[topological properties]]") which allow to detect by means of [[algebra|algebraic]] manipulations
whether two topological spaces are homeomorphic
(or more generally [[homotopy equivalence|homotopy equivalent]]) or not. This is called _[[algebraic topology]]_.
A basic algebraic invariant is the [[fundamental group]] of a topological space (discussed [below](#FundamentalGroups)),
which measures how many ways there are to wind loops inside a topological space.

Beware that the popular imagery of "[[rubber-sheet geometry]]" only captures part of the full scope of topology,
in that it invokes spaces that _locally_ still look like [[metric spaces]].
But the concept of topological spaces is a good bit more general.
Notably [[finite topological spaces]] are either [[discrete topological space|discrete]] or very much unlike
[[metric spaces]] (example \ref{FiniteT1SpacesAreDiscrete} below), they play a role in [[categorical logic]]. Also in [[geometry]] exotic topological spaces frequently arise when  forming non-free [[quotients]].
In order to gauge just how many of such "exotic" examples of topological  spaces beyond locally [[metric spaces]] one wishes
to admit in the theory,
extra "[[separation axioms]]" are imposed on topological spaces (see [below](#SeparationAxioms)), and the flavour of topology as a field
depends on this choice.

Among the separation axioms, the _[[Hausdorff topological space|Hausdorff space]]_ axiom is most popular
(see [below](#TnTopologicalSpaces)). But the weaker axiom of [[sober topological space|soberity]] (see [below](#SoberSpaces)) stands out, on the one
hand because this is the weakest axiom that is still naturally satisfied in applications to [[algebraic geometry]] ([[schemes are sober]])
and [[computer science]] ([Vickers 89](#Vickers89)) and on the other hand because it fully realizes the strong roots that
topology has in [[formal logic]]: [[sober topological spaces]] are entirely characterized by the
union-, intersection- and inclusion-relations
(logical [[conjunction]], [[disjunction]] and [[implication]]) among their [[open subsets]] ([[propositions]]).
This leads to a natural
and fruitful generalization of [[topology]] to more general "purely logic-determined spaces", called _[[locales]]_
and in yet more generality _[[toposes]]_ and _[[higher topos theory|higher toposes]]_. While the latter are beyond
the scope of this introduction, their rich theory and relation to the [[foundations]] of mathematics and geometry
provides an outlook on the relevance of the basic ideas of [[topology]].


$\,$



In this first part we discuss the foundations of the concept of "sets equipped with topology"
([[topological spaces]]) and of [[continuous functions]] between them.


$\,$

+-- {: principle}
**([[classical logic]])**

The [[proofs]] in the following freely use the [[principle of excluded middle]], hence [[proof by contradiction]],
and in a few places they also use the [[axiom of choice]]/[[Zorn's lemma]].

Hence we discuss [[topology]] in its traditional form with [[classical logic]].

We do however highlight the role of [[frame]] homomorphisms (def. \ref{HomomorphismOfFramesOfOpens} below) and that of [[sober topological spaces]] (def. \ref{Sober} below). These concepts pave the way to a [[constructive mathematics|constructive]]
formulation of [[topology]] in terms not of [[topological spaces]] but in terms of _[[locales]]_,
see remark \ref{Locales} below.
The reader interested in questions of [[intuitionistic mathematics]] in topology may benefit from looking at ([Waaldijk 96](topology#Waaldijk96)).

=--


$\,$

## Metric spaces
 {#Continuity}

The concept of continuity was first made precise  in [[analysis]], in terms of [[epsilontic analysis]] on [[metric spaces]], recalled as def. \ref{EpsilonDeltaDefinitionOfContinuity} below. Then it was realized that this has a more elegant formulation in terms of the more general concept of _[[open sets]]_, this is prop. \ref{ContinuityBetweenMetricSpacesInTermsOfOpenSets} below. Adopting the latter as the definition leads to a more abstract concept of "continuous space", this is the concept of _[[topological spaces]]_, def. \ref{TopologicalSpace} below.

Here we briefly recall the relevant basic concepts from [[analysis]], as a motivation for various definitions in
[[topology]]. The reader who either already recalls these concepts in analysis
or is content with ignoring the motivation coming from analysis should skip right away to the section _[Topological spaces](#TopologicalSpaces)_.

+-- {: .num_defn #MetricSpace}
###### Definition
**([[metric space]])**

A _[[metric space]]_ is

1. a [[set]] $X$ (the "underlying set");

1. a [[function]] $d \;\colon\; X \times X \to [0,\infty)$ (the "distance function") from the [[Cartesian product]] of the set with itself to the [[nonnegative number|non-negative]] [[real numbers]]

such that for all $x,y,z \in X$:

1. (symmetry) $d(x,y) = d(y,x)$

1. ([[triangle inequality]]) $d(x,z) \leq d(x,y)+ d(y,z)$.

1. (non-degeneracy) $d(x,y) = 0 \;\;\Leftrightarrow\;\; x = y$

=--

+-- {: .num_defn #OpenBalls}
###### Definition
**([[open balls]])**

Let $(X,d)$, be a [[metric space]]. Then for every element $x \in X$ and every  $\epsilon \in \mathbb{R}_+$ a [[positive number|positive]] [[real number]], we write

$$
  B^\circ_x(\epsilon)
    \;\coloneqq\;
  \left\{
    y \in X \;\vert\; d(x,y) \lt \epsilon
  \right\}
$$

for the [[open ball]] of [[radius]] $\epsilon$ around $x$. Similarly we write

$$
  B_x(\epsilon)
    \;\coloneqq\;
  \left\{
    y \in X \;\vert\; d(x,y) \leq \epsilon
  \right\}
$$

for the _closed ball_ of [[radius]] $\epsilon$ around $x$. Finally we write

$$
  S_x(\epsilon)
    \;\coloneqq\;
  \left\{
    y \in X \;\vert\; d(x,y) = \epsilon
  \right\}
$$

for the [[sphere]] of [[radius]] $\epsilon$ around $x$.

For $\epsilon = 1$ we also speak of the _unit open/closed ball_ and the _unit sphere_.

=--

+-- {: .num_defn #MetricSpaceBoundedSubset}
###### Definition

For $(X,d)$ a [[metric space]] (def. \ref{MetricSpace}) then a [[subset]] $S \subset X$
is called a _[[bounded subset]]_ if $S$ is contained in some [[open ball]] (def. \ref{OpenBalls})

$$
  S \subset B^\circ_x(r)
$$

around some $x \in X$ of some [[radius]] $r \in \mathbb{R}$.

=--

A key source of metric spaces are [[norm|normed]] _[[vector spaces]]_:

+-- {: .num_defn #NormedVectorSpace}
###### Dedfinition
**(normed vector space)**

A _[[normed vector space]]_ is

1. a [[real vector space]] $V$;

1. a [[function]] (the _[[norm]]_)

   $$
     {\Vert {-} \Vert} \;\colon\; V \longrightarrow \mathbb{R}_{\geq 0}
   $$

   from the underlying [[set]] of $V$ to the [[non-negative number|non-negative]] [[real numbers]],

such that for all $c \in \mathbb{R}$ with [[absolute value]] ${\vert c \vert}$ and all $v , w \in V$ it holds true that

1. (linearity) ${\Vert c v \Vert} = {\vert c \vert} {\Vert v \Vert }$;

1. ([[triangle inequality]]) ${\Vert v+w \Vert} \leq {\Vert v \Vert } + {\Vert w \Vert}$;

1. (non-degeneracy) if ${\Vert v \Vert} = 0$ then $v = 0$.

=--



+-- {: .num_prop #MetricSpaceFromNormedVectorSpace}
###### Proposition

Every [[normed vector space]] $(V, {\Vert {-} \Vert})$
becomes a [[metric space]] according to def. \ref{MetricSpace} by setting

$$
  d(x,y) \coloneqq {\Vert x-y \Vert}
  \,.
$$

=--

Examples of [[normed vector spaces]] (def. \ref{NormedVectorSpace}) and hence, via prop. \ref{MetricSpaceFromNormedVectorSpace},
of [[metric spaces]] include the following:

+-- {: .num_example #EuclideanNorm}
###### Example

For $n \in \mathbb{N}$, the [[Cartesian space]]

$$
  \mathbb{R}^n
    =
   \left\{
     \vec x
     =
     (x_i)_{i = 1}^n
     \vert
      x_i \in \mathbb{R}
   \right\}
$$

carries a [[norm]] (the _Euclidean norm_ ) given by the [[square root]] of the [[sum]] of the [[squares]] of the components:

   $$
     {\Vert \vec x \Vert}
       \;\coloneqq\;
     \sqrt{
     \underoverset{i = 1}{n}{\sum}
       (x_i)^2
     }
     \,.
   $$

Via prop. \ref{MetricSpaceFromNormedVectorSpace} this gives $\mathbb{R}^n$ the structure of a
[[metric space]], and as such it is called the _[[Euclidean space]]_ of [[dimension]] $n$.

=--

+-- {: .num_defn #pNorm}
###### Example

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d4/Vector-p-Norms_qtl1.svg/220px-Vector-p-Norms_qtl1.svg.png" width="200">
</div>

More generally, for $n \in \mathbb{N}$, and $p \in \mathbb{R}$, $p \geq 1$, then the [[Cartesian space]] $\mathbb{R}^n$ carries the _[[p-norm]]_

   $$
     {\Vert \vec x \Vert}_p  \coloneqq \root p {\sum_i {|x_i|^p}}
   $$

One also sets

$$
  {\Vert \vec x \Vert}_\infty \coloneqq \underset{i \in I}{max} \, {\vert x_i \vert}
$$

and calls this the _[[supremum norm]]_.

The graphics on the right (grabbed from Wikipedia) shows unit circles (def. \ref{OpenBalls}) in $\mathbb{R}^2$ with respect to various [[p-norms]].

By the [[Minkowski inequality]],
the [[p-norm]] generalizes to non-[[finite dimensional vector spaces]] such as [[sequence spaces]] and [[Lebesgue spaces]].

=--


$\,$

### Continuity
 {#ContinuityInAnalysis}

The following is now the fairly obvious definition of continuity for functions between metric spaces.

+-- {: .num_defn #EpsilonDeltaDefinitionOfContinuity}
###### Definition
**(epsilontic definition of continuity)**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/EpsilonDeltaBalls.png" width="250">
</div>

For $(X,d_X)$ and $(Y,d_Y)$ two [[metric spaces]] (def. \ref{MetricSpace}), then a [[function]]

$$
  f \;\colon\; X \longrightarrow Y
$$

is said to be _continuous at a point $x \in X$_ if for
every [[positive number|positive]] [[real number]] $\epsilon$
there exists a [[positive number|positive]] [[real number]] $\delta$ such that
for all $x' \in X$ that are a [[distance]] smaller than $\delta$ from $x$ then their image $f(x')$
is a distance smaller than $\epsilon$ from $f(x)$:

$$
  \left(
    f\,\, \text{continuous at}\, x
  \right)
  \;\coloneqq\;
  \underset{{\epsilon \in \mathbb{R}} \atop {\epsilon \gt 0}}{\forall}
  \left(
    \underset{{\delta \in \mathbb{R}} \atop {\delta \gt 0}}{\exists}
      \left(
        \left(
          d_X(x,x') \lt \delta
        \right)
           \;\;\Rightarrow\;\;
        \left(
          d_Y(\,f(x), f(x')\,) \lt \epsilon
        \right)
      \right)
  \right)
  \,.
$$

The function $f$ is said to be _continuous_ if it is continuous at every point $x \in X$.

=--

+-- {: .num_example #DistanceFunctionFromsubset}
###### Example
**(distance function from a subset is continuous)**

Let $(X,d)$ be a [[metric space]] (def. \ref{MetricSpace})
and let $S \subset X$ be a [[subset]] of the underlying set.
Define then the function

$$
  d(S,-) \;\colon\; X \to \mathbb{R}
$$

from the underlying set $X$ to the [[real numbers]] by assigning to a point $x \in X$ the [[infimum]] of the [[distances]] from $x$ to $s$, as
$s$ ranges over the elements of $S$:

$$
  d(S,x) \coloneqq inf \left\{ d(s,x) \,\vert\,  s\in S  \right\}
  \,.
$$

This is a continuous function, with $\mathbb{R}$ regarded as a [[metric space]] via its [[Euclidean norm]] (example \ref{EuclideanNorm}).

In particular the original distance function $d(x,-) = d(\{x,-\})$ is continuous in both its arguments.

=--

+-- {: .proof}
###### Proof

Let $x \in X$ and let $\epsilon$ be a positive real number. We need to find a positive real number
$\delta$ such that for $y \in X$ with $d(x,y) \lt \delta$ then ${\vert d(S,x) - d(S,y) \vert} \lt \epsilon$.

For $s \in S$ and $y \in X$, consider the [[triangle inequalities]]

$$
  \begin{aligned}
    d(s,x) & \leq d(s,y) + d(y,x)
    \\
    d(s,y) & \leq d(s,x) + d(x,y)
  \end{aligned}
  \,.
$$

Forming the [[infimum]] over $s \in S$ of all terms appearing here yields

$$
  \begin{aligned}
    d(S,x) & \leq d(S,y) + d(y,x)
    \\
    d(S,y) & \leq d(S,x) + d(x,y)
  \end{aligned}
$$

which implies

$$
  {\vert d(S,x) - d(S,y) \vert} \leq d(x,y)
  \,.
$$

This means that we may take for instance $\delta \coloneqq \epsilon$.

=--


+-- {: .num_example #PolynoialsAreContinuous}
###### Example
**([[polynomials are continuous functions]])**

Consider the [[real line]] $\mathbb{R}$ regarded as the
1-dimensional [[Euclidean space]] $\mathbb{R}$ from example \ref{EuclideanNorm}.

For $P \in \mathbb{R}[X]$ a [[polynomial]], then the function

$$
  \array{
    f_P &\colon& \mathbb{R} &\longrightarrow& \mathbb{R}
    \\
    && x &\mapsto& P(x)
  }
$$

is a [[continuous function]] in the sense of def. \ref{EpsilonDeltaDefinitionOfContinuity}.

Similarly for instance

* forming the [[square root]] is a continuous function $\sqrt(-) \colon \mathbb{R}_{\geq 0} \to \mathbb{R}_{\geq 0}$;

* forming the multiplicativ inverse is a continuous function $1/(-) \;\colon\; \mathbb{R}_{\gt 0} \to \mathbb{R}_{\gt 0}$.

=--

On the other hand, a [[step function]] is continuous everywhere except at the [[finite number]] of points
at which it changes its value, see example \ref{StepFunction} below.


We now reformulate the analytic concept of continuity from def. \ref{EpsilonDeltaDefinitionOfContinuity} in terms of the simple but important concept of _[[open sets]]_:


+-- {: .num_defn #OpenSubsetsOfAMetricSpace}
###### Definition
**(neighbourhood and open set)**

Let $(X,d)$ be a [[metric space]] (def. \ref{MetricSpace}). Say that:

1. A _[[neighbourhood]]_ of a point $x \in X$ is a [[subset]] $U_x \subset X$ which contains some [[open ball]] $B_x^\circ(\epsilon) \subset U_x$ around $x$ (def. \ref{OpenBalls}).

1. An _[[open subset]]_ of $X$ is a [[subset]] $U \subset X$ such that for every $x \in U$ it also contains an [[open ball]] $B^\circ_x(\epsilon)$ around $x$ (def. \ref{OpenBalls}).

1. An _[[open neighbourhood]]_ of a point $x \in X$ is a [[neighbourhood]] $U_x$ of $x$ which is also an open subset, hence equivalently this is any open subset of $X$ that contains $x$.

=--


The following picture shows a point $x$, some [[open balls]] $B_i$ containing it, and two of its [[neighbourhoods]] $U_i$:

<img src="https://ncatlab.org/nlab/files/NeighbourhoodsAndOpenBalls.png" width="500">

> graphics grabbed from [Munkres 75](#Munkres75)


+-- {: .num_example #OpenEmptySet}
###### Example
**(the empty subset is open)**

Notice that for $(X,d)$ a [[metric space]], then the [[empty set|empty]] [[subset]] $\emptyset \subset X$
is always an [[open subset]] of $(X,d)$ according to def. \ref{OpenSubsetsOfAMetricSpace}.
This is because the clause for open subsets $U \subset X$ says that "for every point $x \in U$ there exists...",
but since there is no $x$ in $U = \emptyset$, this clause is always satisfied in this case.

Conversely, the entire set $X$ is always an open subset of $(X,d)$.

=--

+-- {: .num_example #OpenAndClosedIntervals}
###### Example
**(open/closed [[intervals]])**

Regard the [[real numbers]] $\mathbb{R}$ as the 1-dimensional [[Euclidean space]] (example \ref{EuclideanNorm}).

For $a \lt b \in \mathbb{R}$ consider the following [[subsets]]:

1. $(a,b) \coloneqq \left\{ x \in \mathbb{R} \vert a \lt x \lt b \right\}$ $\phantom{AA}$ (*open interval*)

1. $(a,b] \coloneqq \left\{ x \in \mathbb{R} \vert a \lt x \leq b \right\}$ $\phantom{AA}$ (*half-open interval*)

1. $[a,b) \coloneqq \left\{ x \in \mathbb{R} \vert a \leq x \lt b \right\}$ $\phantom{AA}$ (*half-open interval*)

1. $[a,b] \coloneqq \left\{ x \in \mathbb{R} \vert a \leq x \leq b \right\}$ $\phantom{AA}$ (*closed interval*)

The first of these is an open subset according to def. \ref{OpenSubsetsOfAMetricSpace}, the other three are not.
The first one is called an _[[open interval]]_, the last one a _[[closed interval]]_
and the middle two are called _[[half-open intervals]]_.

Similarly for $a,b \in \mathbb{R}$ one considers

1. $(-\infty,b) \coloneqq \left\{ x \in \mathbb{R} \vert x \lt b  \right\}$ $\phantom{AA}$ (*unbounded open interval*)

1. $(a,\infty) \coloneqq \left\{ x \in \mathbb{R} \vert a \lt x  \right\}$ $\phantom{AA}$ $\,\,$ (*unbounded open interval*)

1. $(-\infty,b] \coloneqq \left\{ x \in \mathbb{R} \vert x \leq b  \right\}$ $\phantom{AA}$ (*unbounded half-open interval*)

1. $[a,\infty) \coloneqq \left\{ x \in \mathbb{R} \vert a \leq x  \right\}$ $\phantom{AA}$ $\,\,$ (*unbounded half-open interval*)

The first two of these are open subsets, the last two are not.

For completeness we may also consider

* $(-\infty , \infty) = \mathbb{R}$

* $(a,a) = \emptyset$

which are both open, according to def. \ref{TopologicalSpace}.

=--

We may now rephrase the analytic definition of continuity entirely in terms of open subsets (def. \ref{OpenSubsetsOfAMetricSpace}):

+-- {: .num_prop #ContinuityBetweenMetricSpacesInTermsOfOpenSets}
###### Proposition
**(rephrasing continuity in terms of open sets)**

Let $(X,d_X)$ and $(Y,d_Y)$ be two [[metric space]] (def. \ref{MetricSpace}).
Then a [[function]] $f \colon X \to Y$ is [[continuous function|continuous]] in the [[epsilontic analysis|epsilontic]] sense of def. \ref{EpsilonDeltaDefinitionOfContinuity} precisely if it has the property that its [[pre-images]] of [[open subsets]] of $Y$ (in the sense of def. \ref{OpenSubsetsOfAMetricSpace}) are open subsets of $X$:

$$
  \left(
    f \,\, \text{continuous}
  \right)
    \;\;\Leftrightarrow\;\;
  \left(
    \left(
      O_Y \subset Y \,\, \text{open}
    \right)
      \,\Rightarrow\,
    \left(
      f^{-1}(O_Y) \subset X \,\, \text{open}
    \right)
  \right)
  \,.
$$

=--


$\,$

+-- {: principle}
**principle of continuity**

$\,$ $\,$ _Continuous pre-Images of open subsets are open._

=--


+-- {: .proof}
###### Proof

Observe, by direct unwinding the definitions,
that the epsilontic definition of continuity (def. \ref{EpsilonDeltaDefinitionOfContinuity}) says equivalently in
terms of [[open balls]] (def. \ref{OpenBalls}) that
$f$ is continous at $x$ precisely if for every open ball $B^\circ_{f(x)}(\epsilon)$ around an image
point, there exists an open ball $B^\circ_x(\delta)$ around the corresponding pre-image
point which maps into it:

$$
  \array{
    \left(
      f \,\,\text{continuous at}\,\, x
    \right)
    & \Leftrightarrow \;
    \underset{\epsilon \gt 0}{\forall}
    \left(
      \underset{\delta \gt 0}{\exists}
      \left(
        f(\;B_x^\circ(\delta)\;) \;\subset\; B^\circ_{f(x)}(\epsilon)
      \right)
    \right)
    \\
    & \Leftrightarrow \;
    \underset{\epsilon \gt 0}{\forall}
    \left(
      \underset{\delta \gt 0}{\exists}
      \left(
        B^\circ_x(\delta) \subset f^{-1}\left( B^\circ_{f(x)}(\epsilon) \right)
      \right)
    \right)
  }
  \,.
$$

With this observation the proof immediate. For the record, we spell it out:

First assume that $f$ is continuous in the epsilontic sense. Then for $O_Y \subset Y$ any [[open subset]] and $x \in f^{-1}(O_Y)$ any point in the pre-image, we need to show that there exists an [[open neighbourhood]] of $x$ in $f^{-1}(O_Y)$.

That $O_Y$ is open in $Y$ means by definition that there exists an [[open ball]] $B^\circ_{f(x)}(\epsilon)$ in $O_Y$ around $f(x)$
for some radius $\epsilon$. By the assumption that $f$ is continuous and using the above observation, this implies that there exists an
open ball $B^\circ_x(\delta)$ in $X$ such that $f(B^\circ_x(\delta)) \subset B^\circ_{f(x)}(\epsilon) \subset Y$,
hence such that $B^\circ_x(\delta) \subset f^{-1}\left(B^{\circ}_{f(x)}(\epsilon)\right) \subset f^{-1}(O_Y)$.
Hence this is an open ball of the required kind.

Conversely, assume that the pre-image function $f^{-1}$ takes open subsets to open subsets. Then for every $x \in X$ and $B_{f(x)}^\circ(\epsilon) \subset Y$ an [[open ball]] around its image, we need to produce an open ball $B_x^\circ(\delta) \subset X$ around $x$
such that $f(B_x^\circ(\delta)) \subset B^\circ_{f(x)}(\epsilon)$.

But by definition of open subsets, $B^\circ_{f(x)}(\epsilon) \subset Y$ is open, and therefore by assumption on $f$
its pre-image $f^{-1}(B^\circ_{f(x)}(\epsilon)) \subset X$ is also an open subset of $X$. Again by definition of
open subsets, this implies that it contains an open ball as required.


=--

+-- {: .num_example #StepFunction}
###### Example
**([[step function]])**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/HeavisideFunction.png" width="300>
</div>

Consider $\mathbb{R}$ as the 1-dimensional [[Euclidean space]] (example \ref{EuclideanNorm}) and consider the [[step function]]

$$
  \array{
    \mathbb{R} &\overset{H}{\longrightarrow}& \mathbb{R}
    \\
    x
      &\mapsto&
    \left\{
      \array{
        0 & \vert \, x \leq 0
        \\
        1 & \vert \, x \gt 0
      }
    \right.
  }
  \,.
$$

> graphics grabbed from [Vickers 89](#Vickers89)

Consider then for $a \lt b \in \mathbb{R}$ the [[open interval]] $(a,b) \subset \mathbb{R}$,
an [[open subset]] according to example \ref{OpenAndClosedIntervals}.
The [[preimage]] $H^{-1}(a,b)$ of this open subset is

$$
  H^{-1} \;\colon\;
  (a,b)
    \mapsto
  \left\{
     \array{
       \emptyset & \vert \,  a \geq 1 \;\;\text{or} \;\; b \leq 0
       \\
       \mathbb{R} & \vert \, a \lt 0 \;\;\text{and}\;\; b \gt 1
       \\
       \emptyset & \vert \, a \geq 0 \;\;\text{and}\;\; b \leq 1
       \\
       (0,\infty) & \vert \, 0 \leq a \lt 1 \;\;\text{and}\;\; b \gt 1
       \\
       (-\infty, 0] & \vert \, a \lt 0 \;\;\text{and}\;\; b \leq 1
    }
  \right.
  \,.
$$

By example \ref{OpenAndClosedIntervals}, all except the last of these pre-images listed are open subsets.

The failure of the last of the pre-images to be open
witnesses that the step function is not continuous at $x = 0$.

=--



$\,$


### Compactness
 {#CompactMetricSpaces}

A key application of [[metric spaces]] in [[analysis]] is that they allow a formalization of what it means
for an infinite [[sequence]] of elements in the metric space (def. \ref{Sequences} below)
to _[[convergence|converge]]_ to a _[[limit of a sequence]]_ (def. \ref{Convergence} below).
Of particular interest are therefore those metric spaces for which each sequence has a converging subsequence:
the _[[sequentially compact metric spaces]]_ (def. \ref{MetricSpaceSequentiallyCompact}).

We now briefly recall these concepts from [[analysis]]. Then, in the above spirit, we reformulate
their epsilontic definition in terms of [[open subsets]].
This gives a useful definition that generalizes to [[topological spaces]], the _[[compact topological spaces]]_
discussed further [below](#CompactSpaces).




+-- {: .num_defn #Sequences}
###### Definition
**([[sequence]])**

Given a [[set]] $X$, then a _[[sequence]]_ of elements in $X$ is a [[function]]

$$
  x_{(-)}
    \;\colon\;
  \mathbb{N}
    \longrightarrow
  X
$$

from the [[natural numbers]] to $X$.

A _[[sub-sequence]]_ of such a sequence is a sequence of the form

$$
  x_{\iota(-)}
   \;\colon\;
  \mathbb{N}
    \overset{\iota}{\hookrightarrow}
  \mathbb{N}
    \overset{x_{(-)}}{\longrightarrow}
  X
$$

for some [[injection]] $\iota$.

=--

+-- {: .num_defn #Convergence}
###### Definition
**([[convergence]] to [[limit of a sequence]])**

Let $(X,d)$ be a [[metric space]] (def. \ref{MetricSpace}).
Then a [[sequence]]

$$
  x_{(-)}
    \;\colon\;
  \mathbb{N}
    \longrightarrow
  X
$$

in the underlying set $X$ (def. \ref{Sequences}) is said to _[[convergence|converge]]_ to a point $x_\infty \in X$, denoted

$$
  x_i \overset{i \to \infty}{\longrightarrow} x_\infty
$$

if for every [[positive number|positive]] [[real number]] $\epsilon$, there exists a [[natural number]] $n$, such that
all elements in the sequence after the $n$th one have [[distance]] less than $\epsilon$ from $x_\infty$.

$$
  \left(
    x_i \overset{i \to \infty}{\longrightarrow} x_\infty
  \right)
   \,\Leftrightarrow\,
  \left(
    \underset{ {\epsilon \in \mathbb{R}}  \atop {\epsilon \gt 0} }{\forall}
    \left(
    \underset{n \in \mathbb{N}}{\exists}
    \left(
    \underset{ {i \in \mathbb{N}} \atop {i \gt n} }{\forall}
    \;
    d(x_i, x_\infty) \leq \epsilon
    \right)
    \right)
  \right)
  \,.
$$

Here the point $x_\infty$ is called the _[[limit of a sequence|limit of the sequence]]_.
Often one writes $\underset{i \to \infty}{\lim}x_i$ for this point.

=--

+-- {: .num_defn #CauchySequence}
###### Definition
**([[Cauchy sequence]])**

Given a [[metric space]] $(X,d)$ (def. \ref{MetricSpace}), then a [[sequence]] of points in $X$ (def. \ref{Sequences})

$$
  x_{(-)} \;\colon\;  \mathbb{N}  \longrightarrow X
$$

is called a _[[Cauchy sequence]]_ if for every [[positive number|positive]] [[real number]] $\epsilon$
there exists a [[natural number]] $n \in \mathbb{N}$ such that the [[distance]] between any two elements
of the sequence beyond the $n$th one is less than $\epsilon$

$$
  \left(
    x_{(-)} \,\, \text{Cauchy}
  \right)
  \,\Leftrightarrow\,
  \left(
    \underset{{\epsilon \in \mathbb{R}} \atop {\epsilon \gt 0}}{\forall}
    \left(
    \underset{N \in \mathbb{N}}{\exists}
    \left(
    \underset{{i,j \in \mathbb{N}} \atop {i,j \gt N }}{\forall}
    \;
    d(x_i, x_j) \leq \epsilon
    \right)
    \right)
  \right)
  \,.
$$

=--

+-- {: .num_defn #CompleteMetricSpace}
###### Definition
**([[complete metric space]])**

A [[metric space]] $(X,d)$ (def. \ref{MetricSpace}), for which every [[Cauchy sequence]] (def. \ref{CauchySequence})
[[convergence|converges]] (def. \ref{Convergence}) is called a _[[complete metric space]]_.

A [[normed vector space]], regarded as a metric space via prop. \ref{MetricSpaceFromNormedVectorSpace} that
is complete in this sense is called a _[[Banach space]]_.

=--


Finally recall the concept of _[[compactness]]_ of [[metric spaces]] via [[epsilontic analysis]]:

+-- {: .num_defn #MetricSpaceSequentiallyCompact}
###### Definition
**([[sequentially compact metric space]])**

A [[metric space]] $(X,d)$ (def. \ref{MetricSpace}) is called _[[sequentially compact space|sequentially compact]]_
if every [[sequence]] in $X$ has a subsequence (def. \ref{Sequences}) which [[convergence|converges]] (def. \ref{Convergence}).

=--

The key fact to translate this [[epsilontic analysis|epsilontic]] definition of compactness to a concept that
makes sense for general [[topological spaces]] ([below](#CompactSpaces)) is the following:

+-- {: .num_prop #CompactnessImpliedBySequentialCompactnessForMetricSpace}
###### Proposition
**([[sequentially compact metric spaces are equivalently compact metric spaces]])**

For a [[metric space]] $(X,d)$ (def. \ref{MetricSpace}) the following are equivalent:

1. $X$ is [[sequentially compact space|sequentially compact]];

1. for every [[set]] $\{U_i \subset X\}_{i \in I}$ of [[open subsets]] $U_i$ of $X$ (def. \ref{OpenSubsetsOfAMetricSpace})
   which [[open cover|cover]] $X$ in that $X = \underset{i \in I}{\cup} U_i$, then
   there exists a [[finite set|finite]] [[subset]] $J \subset I$ of these open subsets which still covers
   $X$ in that also $X = \underset{i \in J \subset I}{\cup} U_i$.

=--

The **proof** of prop. \ref{CompactnessImpliedBySequentialCompactnessForMetricSpace}
is most conveniently formulated with some of the terminology of topology in hand, which we introduce now.
Therefore we postpone the proof to [below](#ProofOfSequentiallyCompactMetricSpacesAreEquivCompact).


$\,$

In **summary** prop. \ref{ContinuityBetweenMetricSpacesInTermsOfOpenSets} and prop. \ref{CompactnessImpliedBySequentialCompactnessForMetricSpace}
show that the purely combinatorial
and in particular non-[[epsilontic analysis|epsilontic]] concept of _[[open subsets]]_ captures a substantial part of the nature of
[[metric spaces]] in [[analysis]]. This motivates to reverse the logic and consider more general "[[spaces]]" which are
_only_ characterized by what counts as their open subsets. These are the _[[topological spaces]]_
which we turn to now in def. \ref{TopologicalSpace} (or, more generally, these are the "[[locales]]", which we briefly
consider below in remark \ref{Locales}).


$\,$




## Topological spaces
 {#TopologicalSpaces}

Due to prop. \ref{ContinuityBetweenMetricSpacesInTermsOfOpenSets}
we should pay attention to [[open subsets]] in [[metric spaces]]. It turns out that the following closure
property, which follow directly from the definitions, is at the heart of the concept:


+-- {: .num_prop #OpenSubsetsOfMetricSpaceClosureProperties}
###### Proposition
**(closure properties of open sets in a metric space)**

The collection of [[open subsets]] of a [[metric space]] $(X,d)$ as in def. \ref{OpenSubsetsOfAMetricSpace} has the following properties:

1. The [[union]] of any [[set]] of open subsets is again an open subset.

1. The [[intersection]] of any [[finite number]] of open subsets is again an open subset.

=--

+-- {: .num_remark #EmptyIntersection}
###### Remark
**(empty union and empty intersection)**

Notice the degenerate case of [[unions]] $\underset{i \in I}{\cup} U_i$
and [[intersections]] $\underset{i \in I}{\cap} U_i$ of [[subsets]] $U_i \subset X$ for the case that they
are indexed by the [[empty set]] $I = \emptyset$:

1. the _empty union_ is the empty set itself;

1. the _empty intersection_ is all of $X$.

(The second of these may seem less obvious than the first. We discuss the general logic behind these kinds of phenomena [below](#UniversalConstructions).)

This way prop. \ref{OpenSubsetsOfMetricSpaceClosureProperties}
is indeed compatible with the degenerate cases of examples of open subsets in example \ref{OpenEmptySet}.

=--


Proposition \ref{OpenSubsetsOfMetricSpaceClosureProperties} motivates
the following generalized definition, which abstracts away from the concept of [[metric space]]
just its system of [[open subsets]]:


+-- {: .num_defn #TopologicalSpace}
###### Definition
**([[topological spaces]])**

Given a [[set]] $X$, then a _topology_ on $X$ is a collection $\tau$ of [[subsets]] of $X$ called the _[[open subsets]]_, hence a [[subset]] of the [[power set]] $P(X)$

$$
  \tau \subset P(X)
$$

such that this is closed under forming

1. finite [[intersections]];

1. arbitrary [[unions]].

In particular (by remark \ref{EmptyIntersection}):

* the [[empty set]] $\emptyset \subset X$ is in $\tau$ (being the union of no subsets)

and

* the whole set $X \subset X$ itself is in $\tau$ (being the intersection of no subsets).


A set $X$ equipped with such a [[topology]] is called a _[[topological space]]_.

=--

+-- {: .num_remark}
###### Remark

In the field of [[topology]] it is common to eventually simply say "[[space]]" as shorthand for "[[topological space]]".
This is especially so as further qualifiers are added, such as "Hausdorff  space" (def. \ref{HausdorffTopologicalSpace} below).
But beware that there are other kinds of [[spaces]] in mathematics.

=--

+-- {: .num_remark}
###### Remark

The simple definition of [[open subsets]] in def. \ref{TopologicalSpace} and the simple
implementation of the _principle of continuity_ below in def. \ref{ContinuousMaps}
gives the field of [[topology]] its fundamental and universal flavor. The combinatorial nature of these definitions makes
[[topology]] be closely related to [[formal logic]]. This becomes more manifest still for the "[[sober topological space]]"
discussed [below](#SoberSpaces). For more on this perspective see the remark on _[[locales]]_ below, remark \ref{Locales}.
An introductory textbook amplifying this perspective is ([Vickers 89](#Vickers89)).

=--

$\,$

Before we look at first examples [below](#TopologicalSpacesExamples),
here is some common **further terminology** regarding topological spaces:

There is an evident [[partial ordering]] on the set of topologies that a given set may carry:

+-- {: .num_defn #TopologyFinerCoarser}
###### Definition
**([[finer topology|finer/coarser topologies]])**

Let $X$ be a [[set]], and let $\tau_1, \tau_2 \in P(X)$ be two [[topological space|topologies]] on $X$,
hence two choices of [[open subsets]] for $X$, making it a [[topological space]]. If

$$
  \tau_1 \subset \tau_2
$$

hence if every open subset of $X$ with respect to $\tau_1$ is also regarded as open by $\tau_2$, then
one says that

* the topology $\tau_2$ is _[[finer topology|finer]]_ than the topology $\tau_2$

* the topology $\tau_1$ is _[[coarser topology|coarser]]_ than the topology $\tau_1$.

=--

With any kind of [[mathematical structure|structure]] on [[sets]], it is of interest how to
"[[generators and relations|generate]]" such structures from a small amount of data:

+-- {: .num_defn #TopologyBase}
###### Definition
**([[basis for the topology]])**

Let $(X, \tau)$ be a [[topological space]], def. \ref{TopologicalSpace},
and let

$$
  \beta \subset \tau
$$

be a [[subset]] of its set of [[open subsets]]. We say that

1. $\beta$ is a _[[topological base|basis for the topology]]_ $\tau$ if every open subset $O \in \tau$ is a [[union]] of elements of $\beta$;

1. $\beta$ is a _[[topological base|sub-basis for the topology]]_ if every open subset $O \in \tau $ is a [[union]] of [[finitary intersections|finite intersections]] of elements of $\beta$.


=--

Often it is convenient to _define_ topologies by defining some (sub-)basis as in def. \ref{TopologyBase}. Examples are the
the [[metric topology]] below, example \ref{MetricTopology},
the [[product topological space|binary product topology]] in def. \ref{BinaryProductTopologicalSpace} below,
and the [[compact-open topology]] on [[mapping spaces]] below in def. \ref{CompactOpenTopology}.
To make use of this, we need to recognize sets of open subsets that serve as the basis for some topology:

+-- {: .num_lemma #RecognizingTopologicalBasis}
###### Lemma
**(recognition of topological bases)**

Let $X$ be a set.

1. A collection $\beta \subset P(X)$ of [[subsets]] of $X$ is a [[basis of a topology|basis]]
for some topology $\tau \subset P(X)$ (def. \ref{TopologyBase}) precisely if

   1. every point of $X$ is contained in at least one element of $\beta$;

   1. for every two subsets $B_1, B_2 \in \beta$ and for every point $x \in B_1 \cap B_2$ in their intersection, then there exists
   a $B \in \beta$ that contains $x$ and is contained in the intersection: $x \in B \subset B_1 \cap B_2$.

1. A subset $B \subset \tau$ of opens is a sub-basis for a topology $\tau$ on $X$ precisely if $\tau$ is the coarsest topology (def. \ref{TopologyFinerCoarser}) which contains $B$.


=--


$\,$

### Examples
 {#TopologicalSpacesExamples}

We discuss here some basic examples of [[topological spaces]] (def. \ref{TopologicalSpace}), to get a feeling for
the scope of the concept. But topological spaces are ubiquituous in [[mathematics]], so that there are many more examples
and many more classes of examples than could be listed. As we further develop the theory below, we encounter more examples,
and more classes of examples. Below in _[Universal constructions](#UniversalConstructions)_ we discuss a very general construction
principle of new topological space from  given ones.

First of all, our motivating example from [above](#Continuity) now reads as follows:

+-- {: .num_example #MetricTopology}
###### Example
**([[metric topology]])**

Let $(X,d)$ be a [[metric space]] (def. \ref{MetricSpace}). Then the collection of its [[open subsets]] in def. \ref{OpenSubsetsOfAMetricSpace} constitutes a _[[topological space|topology]]_ on the set $X$, making it a _[[topological space]]_ in the sense of def. \ref{TopologicalSpace}. This is called the _[[metric topology]]_.

The [[open balls]] in a metric space constitute a [[basis of a topology]] (def. \ref{TopologyBase}) for the [[metric topology]].



=--



While the example of [[metric space]] topologies (example \ref{MetricTopology}) is the motivating example
for the concept of [[topological spaces]], it is important to notice that the concept
of topological spaces is considerably more general, as some of the following examples show.


The following simplistic example of a (metric) topological space is important for the theory
(for instance in prop. \ref{FrameHomomorphismsToPointAreIrrClSub}):


+-- {: .num_example #Point}
###### Example
**([[empty space]] and [[point space]])**

On the [[empty set]] there exists a unique topology $\tau$ making it a [[topological space]] according to def. \ref{TopologicalSpace}.
We write also

$$
  \emptyset
    \;\coloneqq\;
   \left(
     \emptyset, \tau_{\emptyset} = \{ \emptyset  \}
   \right)
$$

for the resulting [[topological space]],
which we call the _[[empty topological space]]_.

On a [[singleton]] set $\{1\}$ there exists a unique topology $\tau$
making it a [[topological space]] according to def. \ref{TopologicalSpace},
namely

$$
  \tau
    \coloneqq
  \left\{
    \emptyset , \{1\}
  \right\}
  \,.
$$

We write

$$
  \ast
    \coloneqq
  \left(
    \left\{1\right\}, \tau \coloneqq \left\{ \emptyset, \left\{1\right\}\right\}
  \right)
$$

for this topological space and call it _the [[point topological space]]_.

This is equivalently the [[metric topology]] (example \ref{MetricTopology}) on $\mathbb{R}^0$,
regarded as the 0-dimensional [[Euclidean space]] (example \ref{EuclideanNorm}).

=--

+-- {: .num_example #SierpinskiSpace}
###### Example

On the 2-element set $\{0,1\}$ there are (up to [[permutation]] of elements) three distinct topologies:

1. the _[[codiscrete topology]]_ (def. \ref{CoDiscreteTopology}) $\tau = \left\{   \emptyset, \{0,1\}  \right\}$;

1. the _[[discrete topology]]_ (def. \ref{CoDiscreteTopology}), $\tau = \left\{   \emptyset, \{0\}, \{1\}, \{0,1\}  \right\}$;

1. the _[[Sierpinski space]]_ topology $\tau = \left\{\emptyset, \{1\}, \{0,1\}  \right\}$.

=--

+-- {: .num_example}
###### Example

The following shows all the topologies on the 3-element set (up to [[permutation]] of elements)

<img src="https://ncatlab.org/nlab/files/TopologiesOn3ElementSet.png" width="400">

> graphics grabbed from [Munkres 75](#Munkres75)

=--


+-- {: .num_example #CoDiscreteTopology}
###### Example
**(discrete and co-discrete topology)**

Let $S$ be any [[set]]. Then there are always the following two extreme
possibilities of equipping $X$ with a topology $\tau \subset P(X)$ in the sense of
def. \ref{TopologicalSpace}, and hence making it a [[topological space]]:

1. $\tau \coloneqq P(S)$ the set of _all_ open subsets;

   this is called the _[[discrete topology]]_ on $S$, it is the [[finer topology|finest topology]] (def. \ref{TopologyFinerCoarser}) on $X$,

   we write $Disc(S)$ for the resulting topological space;

1. $\tau \coloneqq \{ \emptyset, S \}$ the set contaning only the [[empty set|empty]] subset of $S$ and all of $S$ itself;

   this is called the _[[codiscrete topology]]_ on $S$, it is the [[coarser topology|coarsest topology]] (def. \ref{TopologyFinerCoarser}) on $X$,

   we write $CoDisc(S)$ for the resulting topological space.

The reason for this terminology is best seen when considering [[continuous functions]] into or out of these (co-)discrete topological spaces, we come to this in example \ref{ContinuousFunctionsIntoCoDiscreteTopologicalSpaces} below.

=--

+-- {: .num_example #TopologyCofinite}
###### Example
**([[cofinite topology]])**

Given a [[set]] $X$, then the _[[cofinite topology]]_ or _finite complement topology_ on $X$ is the [[topological space|topology]]
(def. \ref{TopologicalSpace}) whose [[open subsets]] are precisely

1. all [[cofinite subsets]] $S \subset X$ (i.e. those such that the [[complement]] $X \backslash S$ is a [[finite set]]);

1. the [[empty set]].

If $X$ is itself a [[finite set]] (but not otherwise) then the cofinite topology on $X$ coincides with the [[discrete topological space|discrete topology]] on $X$ (example \ref{CoDiscreteTopology}).

=--


$\,$

{#BasicConstructions} We now consider basic construction principles of new topological spaces from given ones:

1. [[disjoint union spaces]] (example \ref{DisjointUnionOfTopologicalSpaces})

1. [[subspaces]] (example \ref{SubspaceTopology}),

1. [[quotient spaces]] (example \ref{QuotientTopologicalSpace})

1. [[product spaces]] (example \ref{BinaryProductTopologicalSpace}).

Below in _[Universal constructions](#UniversalConstructions)_ we will recognize these
as simple special cases of a general construction principle.


+-- {: .num_example #DisjointUnionOfTopologicalSpaces}
###### Example
**([[disjoint union space]])**

For $\{(X_i, \tau_i)\}_{i \in I}$ a [[set]] of topological spaces, then their _[[disjoint union]]_

$$
  \underset{i \in I}{\sqcup} (X_i, \tau_i)
$$

is the topological space whose underlying set is the [[disjoint union]] of the underlying sets of the summand spaces,
and whose open subsets are precisely the disjoint unions of the open subsets of the summand spaces.

In particular, for $I$ any index set, then the disjoint union
of $I$ copies of the [[point space]] (example \ref{Point}) is equivalently the [[discrete topological space]] (example \ref{CoDiscreteTopology})
on that index set:

$$
  \underset{i \in I}{\sqcup} \ast
  \;=\;
  Disc(I)
  \,.
$$


=--


+-- {: .num_example #SubspaceTopology}
###### Example
**([[topological subspace|subspace topology]])**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/OpenSubsetsOfSquareInsidePlane.png" width="200">
</div>

Let $(X, \tau_X)$ be a [[topological space]], and let $S \subset X$ be a [[subset]] of the underlying set. Then the corresponding _[[topological subspace]]_ has $S$ as its underlying set, and its open subsets are those subsets of $S$ which arise as restrictions of open subsets of $X$.

$$
  \left(
    U_S \subset S\,\,\text{open}
  \right)
    \,\Leftrightarrow\,
  \left(
     \underset{U_X \in \tau_X}{\exists} \left( U_S = U_X \cap S \right)
  \right)
  \,.
$$

(This is also called the _[[initial topology]]_ of the inclusion map. We come back to this below in def. \ref{InitialAndFinalTopologies}.)


The picture on the right shows two open subsets inside the [[square]], regarded as a [[topological subspace]] of the [[plane]] $\mathbb{R}^2$:

> graphics grabbed from [Munkres 75](#Munkres75)


=--


+-- {: .num_example #QuotientTopologicalSpace}
###### Example
**([[quotient topological space]])**

Let $(X,\tau_X)$ be a [[topological space]] (def. \ref{TopologicalSpace}) and let

$$
  R_\sim \subset X \times X
$$

be an [[equivalence relation]] on its underlying set. Then the _[[quotient topological space]]_  has

* as underlying set the [[quotient set]] $X/\sim$, hence the set of [[equivalence classes]],

and

* a subset $O \subset X/\sim$ is declared to be an [[open subset]] precisely if its [[preimage]] $\pi^{-1}(O)$ under the canonical [[projection map]]

  $$
    \pi \;\colon\; X \to X/\sim
  $$

  is open in $X$.

(This is also called the _[[final topology]]_ of the projection $\pi$. We come back to this below in def. \ref{InitialAndFinalTopologies}. )

Often one considers this with input datum not the equivalence relation, but any [[surjection]]

$$
  \pi \;\colon\; X \longrightarrow Y
$$

of sets. Of course this identifies $Y = X/\sim$ with $(x_1 \sim x_2) \Leftrightarrow (\pi(x_1) = \pi(x_2)) $.
Hence the _quotient topology_ on the codomain set of a function out of any topological space has as open subsets
those whose pre-images are open.

To see that this indeed does define a topology on $X/\sim$ it is sufficient to observe that taking pre-images
commutes with taking unions and with taking intersections.

=--


+-- {: .num_example #BinaryProductTopologicalSpace}
###### Example
**([[product topological space|binary product topological space]])**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/ProductTopology.png" width="300">
</div>

For $(X_1,\tau_{X_1})$ and $(X_2, \tau_{X_2})$ two [[topological spaces]], then their _[[product topological space|binary product topological space]]_
has as underlying set the [[Cartesian product]] $X_1 \times X_2$ of the corresponding two underlying sets,
and its topology is generated from the [[basis for a topology|basis]] (def. \ref{TopologyBase})
given by the Cartesian products $U_1 \times U_2$ of the opens $U_i \in \tau_i$.

> graphics grabbed from [Munkres 75](#Munkres75)

Beware that for non-[[finite set|finite]] products, the descriptions of the product topology is not as simple.
This we turn to below in example \ref{InfiniteProductTopologicalSpace}, after inroducing the general concept
of [[limits]] in the [[category of topological spaces]].

=--

The following examples illustrate how all these ingredients and construction principles
may be combined.

The following example we will examine in more detail below in example \ref{HomeomorphismBetweenTopologicalAndCombinatorialCircle},
after we have introduced the concept of _[[homeomorphisms]]_ [below](#Homeomorphisms).

+-- {: .num_example }
###### Example

Consider the [[real numbers]] $\mathbb{R}$ as the 1-dimensional [[Euclidean space]] (example \ref{EuclideanNorm})
and hence as a [[topological space]] via the corresponding [[metric topology]] (example \ref{MetricTopology}).
Moreover, consider the [[closed interval]] $[0,1] \subset \mathbb{R}$ from example \ref{OpenAndClosedIntervals},
regarded as a [[subspace]] (def. \ref{SubspaceTopology}) of $\mathbb{R}$.

The [[product space]] (example \ref{BinaryProductTopologicalSpace}) of this interval with itself

$$
  [0,1] \times [0,1]
$$


is a topological space modelling the closed square. The [[quotient space]] (example \ref{QuotientTopologicalSpace}) of that
by the relation which identifies a pair of opposite sides is a model for the [[cylinder]].
The further quotient by the relation that identifies the remaining pair of sides yields a model for the [[torus]].

<img src="https://ncatlab.org/nlab/files/QuotientOfSquareIsCylinderAndTorus.png" width="660">


> graphics grabbed from [Munkres 75](#Munkres75)


=--

+-- {: .num_example #SpheresAndDisks}
###### Example
**([[spheres]] and disks)**

For $n \in \mathbb{N}$ write

* $D^n$ for the [[n-disk]], the [[closed ball|closed unit ball]] (def. \ref{OpenBalls}) in the $n$-dimensional [[Euclidean space]] $\mathbb{R}^n$ (example \ref{EuclideanNorm}) and equipped with the induced [[subspace topology]] (example \ref{SubspaceTopology}) of the corresponding [[metric topology]] (example \ref{MetricTopology});

* $S^{n-1}$ for the [[n-sphere|(n-1)-sphere]] (def. \ref{OpenBalls}) also equipped with the corresponding [[subspace topology]];

* $i_n \;\colon\; S^{n-1} \hookrightarrow D^n$ for the [[continuous function]] that exhibits this [[boundary]] inclusion.

Notice that

* $S^{-1} = \emptyset$ is the [[empty topological space]] (example \ref{Point});

* $S^0 = \ast \sqcup \ast$ is the [[disjoint union space]] (example \ref{DisjointUnionOfTopologicalSpaces}) of the [[point topological space]] (example \ref{Point}) with itself, equivalently the [[discrete topological space]] on two elements (example \ref{SierpinskiSpace}).

=--


The following important class of [[topological spaces]] form the foundation of [[algebraic geometry]]:

+-- {: .num_example}
###### Example
**([[Zariski topology]] on [[affine space]])**

Let $k$ be a [[field]], let $n \in \mathbb{N}$, and write $k[X_1, \cdots, X_n]$ for the [[set]] of [[polynomials]] in $n$ [[variables]] over $k$.

For $\mathcal{F} \subset k[X_1, \cdots, X_n]$ a subset of polynomials, let the  subset $V(\mathcal{P}) \subset k^n$ of the $n$-fold [[Cartesian product]] of the underlying set of $k$ (the _vanishing set_ of $\mathcal{F}$) be the subset of points on which all these polynomials jointly vanish:

$$
  V(\mathcal{F})
    \coloneqq
  \left\{
     (a_1, \cdots, a_n) \in k^n
     \,\vert\,
     \underset{f \in \mathcal{F}}{\forall} f(a_1, \cdots, a_n) = 0
  \right\}
  \,.
$$

These subsets are called the _Zariski [[closed subsets]]_.

Write

$$
  \tau_{\mathbb{A}^n_k}
  \;\coloneqq\;
  \left\{
    k^n \backslash V(\mathcal{F}) \subset k^n
    \,\vert\,
    \mathcal{F} \subset k[X_1, \cdots, X_n]
  \right\}
$$

for the set of [[complements]] of subsets the Zariski closed subsets. These are called the _Zariski [[open subsets]]_ of $k^n$.

The Zariski open subsets of $k^n$  form a [[topological space|topology]] (def. \ref{TopologicalSpace}),
called the _[[Zariski topology]]_. The resulting [[topological space]]

$$
  \mathbb{A}^n_k
  \;\coloneqq\;
  \left(
     k^n, \tau_{\mathbb{A}^n_k}
  \right)
$$

is also called the $n$-dimensional _[[affine space]]_ over $k$.


=--

More generally

+-- {: .num_example}
###### Example
**([[Zariski topology]] on the [[prime spectrum of a commutative ring]])**

Let $R$ be a [[commutative ring]]. Write $PrimeIdl(R)$ for its set of [[prime ideals]]. For $\mathcal{F} \subset R$ any subset of elements of the ring, consider the subsets of those prime ideals that contain $\mathcal{F}$:

$$
  V(\mathcal{F})
   \;\coloneqq\;
  \left\{
    p \in PrimeIdl(R) \,\vert\, \mathcal{F} \subset p
  \right\}
  \,.
$$

These are called the _Zariski [[closed subsets]]_ of $PrimeIdl(R)$. Their [[complements]] are called the _Zariski open subsets_.

Then the collection of Zariski open subsets in its set of [[prime ideals]]

$$
  \tau_{Spec(R)} \subset P(PrimeIdl(R))
$$

satisfies the axioms of a [[topological space|topology]] (def. \ref{TopologicalSpace}), the _[[Zariski topology]]_.

This [[topological space]]

$$
  Spec(R) \coloneqq (PrimeIdl(R), \tau_{Spec(R)})
$$

is called (the space underlying) the _[[prime spectrum of a commutative ring|prime spectrum of the commutative ring]]_.


=--



$\,$








### Closed subsets
 {#ClosedSubsets}

The [[complements]] of [[open subsets]] in a [[topological space]] are called _[[closed subsets]]_
(def. \ref{ClosedSubset} below).
This simple definition indeed captures the concept of closure in the [[analysis|analytic]]
sense of [[convergence]] of [[sequences]] (prop. \ref{ConvergenceInClosedSubspace} below). Of particular interest for the theory of topological spaces in the discussion of [[separation axioms]] [below](#SeparationAxioms) are those closed subsets which are
"[[irreducible closed subset|irreducible]]" (def. \ref{ClosedIrreducible} below). These happen to be equivalently the
"[[frame]] homomorphisms" (def. \ref{HomomorphismOfFramesOfOpens}) to the [[frame of opens]] of the point
(prop. \ref{FrameHomomorphismsToPointAreIrrClSub} below).


+-- {: .num_defn #ClosedSubset}
###### Definition
**([[closed subsets]])**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/ClosedAndOpenSubsets.png" width="300">
</div>

Let $(X,\tau)$ be a [[topological space]] (def. \ref{TopologicalSpace}).


1. A [[subset]] $S \subset X$ is called a _[[closed subset]]_ if its [[complement]] $X \backslash S$ is an  _[[open subset]]_:

   $$
     \left(
       S \subset X\,\, \text{is closed}
     \right)
     \phantom{AA}
       \Leftrightarrow
     \phantom{AA}
     \left(
       X\backslash S \, \subset X \,\, \text{is open}
     \right)
     \,.
   $$

   > graphics grabbed from [Vickers 89](#Vickers89)

1. If a [[singleton]] subset $\{x\} \subset X$ is closed, one says that $x$ is a _closed point_ of $X$.

1. Given any subset $S \subset X$, then its _[[topological closure]]_ $Cl(X)$ is the smallest closed subset containing $S$:

   $$
     Cl(S)
       \;\coloneqq\;
     \underset{ {C \subset X\, \text{closed}  }   \atop {S \subset C }  }{\cap} \left( C \right)
     \,.
   $$

1. A subset $S \subset X$ such that $Cl(S) = X$ is called a _[[dense subset]]_ of $(X,\tau)$.

=--



+-- {: .num_remark #deMorgan}
###### Remark
**([[de Morgan's law]])**

In reasoning about [[closed subsets]] in [[topology]] we are concerned with [[complements]] of [[unions]] and
[[intersections]] as well as with [[unions]]/[[intersections]] of [[complements]]. Recall therefore
that taking [[complements]] of [[subsets]] exchanges [[unions]] with [[intersections]]
([[de Morgan's law]]):

Given a [[set]] $X$ and a set of subsets

$$
  \{S_i \subset S\}_{i \in I}
$$

then

$$
  X \backslash
  \left(
     \underset{i \in I}{\cup}  S_i
  \right)
  \;\;=\;\;
   \underset{i \in I}{\cap}
   \left(
      X \backslash S_i
   \right)
$$

and

$$
  X \backslash
  \left(
     \underset{i \in I}{\cap}  S_i
  \right)
  \;\;=\;\;
   \underset{i \in I}{\cup}
   \left(
      X \backslash S_i
   \right)
  \,.
$$

Also notice that taking complements reverses inclusion relations:

$$
  \left(
    S_1 \subset S_2
  \right)
  \;\;\Leftrightarrow\;\,
  \left(
    X\backslash S_2 \subset X \backslash S_1
  \right)
  \,.
$$

=--


Often it is useful to reformulate def. \ref{ClosedSubset} of [[closed subsets]] as follows:

+-- {: .num_lemma #UnionOfOpensGivesClosure}
###### Lemma
**(alternative characterization of closed subsets)**

Let $(X,\tau)$ be a [[topological space]] and let $S \subset X$ be a [[subset]] of its underlying
set. Then a point $x \in X$ is contained in the [[topological closure]] $Cl(S)$ (def. \ref{ClosedSubset})
precisely if every [[open neighbourhood]] $U_x \subset X$ of $x$ [[intersection|intersects]] $S$:

$$
  \left(
     x \in Cl(S)
  \right)
   \phantom{AA}
     \Leftrightarrow
   \phantom{AA}
   \not\left(
     \underset{ {U \subset X \backslash S}  \atop  { U \subset X \, \text{open}  } }{\exists}
      \left(
        x \in U
      \right)
   \right)
   \,.
$$

=--

+-- {: .proof}
###### Proof

In view of remark \ref{deMorgan} we may rephrase the definition of the [[topological closure]]
as follows:

$$
  \begin{aligned}
    Cl(S)
    & \coloneqq
    \underset{ {S \subset C }  \atop { C \subset X\,\text{closed} } }{\cap}
    \left(C \right)
    \\
    & =
    \underset{ { U \subset X \backslash S } \atop {U \subset X\, \text{open}}  }{\cap} \left( X \backslash U \right)
    \\
    & = X \backslash
    \left(
       \underset{ {U \subset X \backslash S} \atop { U \subset X\, \text{open} }}{\cup} U
    \right)
  \end{aligned}
  \,.
$$



=--


+-- {: .num_defn #IntSubset}
###### Definition
**([[topological interior]] and [[boundary]])**

Let $(X,\tau)$ be a [[topological space]] (def. \ref{TopologicalSpace}) and let $S \subset X$ be a [[subset]].
Then the _[[topological interior]]_ of $S$ is the largest [[open subset]] $Int(S) \in \tau$ still contained in $S$,
$Int(S) \subset S \subset X$:

$$
  Int(S) \coloneqq \underset{{O \subset S} \atop {O \subset X\, \text{open}}}{\cup} \left( U \right)
  \,.
$$

The _[[boundary]]_ $\partial S$ of $S$ is the [[complement]] of its interior inside its [[topological closure]] (def. \ref{ClosedSubset}):

$$
  \partial S \;\coloneqq\; Cl(S) \backslash Int(S)
  \,.
$$

=--


+-- {: .num_lemma #RelationClAndInt}
###### Lemma
**(duality between closure and interior)**

Let $(X,\tau)$ be a [[topological space]] and let $S \subset X$ be a [[subset]].
Then the [[topological interior]] of $S$ (def. \ref{IntSubset}) is the same as the [[complement]] of the
[[topological closure]] $Cl(X\backslash S)$ of the complement of $S$:

$$
  X \backslash Int(S)
  \, = \,
  Cl(\, X \backslash S \,)
$$

and conversely

$$
  X \backslash Cl(S)
  \, = \,
  Int(\, X \backslash S \,)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Using remark \ref{deMorgan}, we compute as follows:

$$
  \begin{aligned}
    X \backslash Int(S)
    & =
    X \backslash \left(  \underset{ {U \subset S} \atop {U \subset X \, open} }{\cup}U \right)
    \\
    & = \underset{ {U \subset S} \atop {U \subset X \, \text{open}}  }{\cap} \left( X \backslash U \right)
    \\
    & = \underset{ {C \supset X \backslash S} \atop {C\, closed}  }{\cap} \left( C \right)
    \\
    & = Cl(X \backslash S)
  \end{aligned}
$$

Similarly for the other case.

=--

+-- {: .num_example }
###### Example
**([[topological closure]] and [[interior]] of [[closed interval|closed]] and [[open intervals]])**

Regard the [[real numbers]] as the 1-dimensional [[Euclidean space]] (example \ref{EuclideanNorm}) and equipped with the
corresponding [[metric topology]] (example \ref{MetricTopology}) . Let $a \lt b \in \mathbb{R}$. Then the [[topological interior]]
(def. \ref{IntSubset}) of the [[closed interval]] $[a,b] \subset \mathbb{R}$
(example \ref{OpenAndClosedIntervals}) is the [[open interval]] $(a,b) \subset \mathbb{R}$,
moreover the closed interval is its own [[topological closure]] (def. \ref{ClosedSubset})
and the converse holds (by lemma \ref{RelationClAndInt}):

$$
  \array{
    Cl\left( \,(a,b)\, \right)
     \,=\,
    [a,b]
    &&
    Int\left( \, (a,b) \,  \right)
    \,=\,
    (a,b)
    \\
    \\
    Cl\left( \,[a,b]\, \right)
     \,=\,
    [a,b]
    &&
    Int\left(\,[a,b]\,\right)
    \,=\,
    (a,b)
  }
  \,.
$$

Hence the  [[boundary]] of the closed interval is its endpoints, while the boundary of the open interval is
empty

$$
  \array{
    \partial [a,b] = \{a\} \cup \{b\}
    &&
    \partial(a,b) = \emptyset
  }
  \,.
$$

=--


The terminology "closed" subspace for complements of opens is justified by the following statement,
which is a further example of how the combinatorial concept of open subsets captures key phenomena in [[analysis]]:

+-- {: .num_prop #ConvergenceInClosedSubspace}
###### Proposition
**([[convergence]] in [[closed subspaces]])**

Let $(X,d)$ be a [[metric space]] (def. \ref{MetricSpace}), regarded as a [[topological space]] via example \ref{MetricTopology},
and let $V \subset X$ be a [[subset]]. Then the following are equivalent:

1. $V \subset X$ is a [[closed subspace]] according to def. \ref{ClosedSubset}.

1. For every [[sequence]] $x_i \in V \subset X$ (def. \ref{Sequences}) with elements in $V$, which [[convergence|converges]]
   as a sequence in $X$ (def. \ref{Convergence}) to some $x_\infty \in X$, then $x_\infty \in V \subset X$.

=--

+-- {: .proof}
###### Proof

First assume that $V \subset X$ is closed and that $x_i \overset{i \to \infty}{\longrightarrow} x_{\infty}$ for some
$x_\infty \in X$. We need to show that then $x_\infty \in V$. Suppose it were not, hence that
$x_\infty \in X\backslash V$. Since, by assumption on $V$, this [[complement]] $X \backslash V \subset X$ is an [[open subset]],
it would follow that there exists a [[real number]] $\epsilon \gt 0$ such that the [[open ball]]
around $x$ of radius $\epsilon$ were still contained in the complement: $B^\circ_x(\epsilon) \subset X \backslash V$.
But since the sequence is assumed to converge in $X$, this would mean that there exists $N_\epsilon$ such that all
$x_{i \gt N_{\epsilon}}$ are in $B^\circ_x(\epsilon)$, hence in $X\backslash V$. This contradicts the assumption that
all $x_i$ are in $V$, and hence we have [[proof by contradiction|proved by contradiction]] that $x_\infty \in V$.

Conversely, assume that for all sequences in $V$ that converge to some $x_\infty \in X$ then $x_\infty \in V \subset X$.
We need to show that then $V$ is closed, hence that $X \backslash V \subset X$ is an open subset, hence that for every
$x \in X \backslash V$ we may find a real number $\epsilon \gt 0$ such that the [[open ball]] $B^\circ_x(\epsilon)$ around $x$
of radius $\epsilon$ is still contained in
$X \backslash V$. Suppose on the contrary that such $\epsilon$ did not exist. This would mean that for each $k \in \mathbb{N}$
with $k \geq 1$ then the [[intersection]] $B^\circ_x(1/k) \cap V$ were [[inhabited|non-empty]]. Hence then we could [[axiom of choice|choose]]
points $x_k \in B^\circ_x(1/k) \cap V$ in these intersections. These would form a sequence which clearly converges to
the original $x$, and so by assumption we would conclude that $x \in V$, which violates the assumption that $x \in X \backslash V$.
Hence we [[proof by contradiction|proved by contradiction]] $X \backslash V$ is in fact open.

=--

A special role in the theory is played by the "irreducible" closed subspaces:

+-- {: .num_defn #ClosedIrreducible}
###### Definition
**([[irreducible closed subspace]])**

A [[closed subset]] $S \subset X$ (def. \ref{ClosedSubset}) of a [[topological space]] $X$ is called _[[irreducible closed subspace|irreducible]]_ if it is
[[inhabited|non-empty]] and not the [[union]] of two closed proper (i.e. smaller) subsets. In other words,
a [[inhabited|non-empty]] closed subset $S \subset X$ is irreducible if whenever
$S_1, S_2 \subset X$ are two [[closed subspace]] such that

$$
  S = S_1 \cup S_2
$$

then $S_1 = S$ or $S_2 = S$.

=--

+-- {: .num_example #IrreducibleClosureOfPoint}
###### Example
**(closures of points are irreducible)**

For $x \in X$ a [[point]] inside a [[topological space]], then
the [[topological closure|closure]] $Cl(\{x\})$ of the [[singleton]] [[subset]] $\{x\} \subset X$
is [[irreducible closed subset|irreducible]] (def. \ref{ClosedIrreducible}).

=--

+-- {: .num_example }
###### Example
**(no nontrivial closed irreducibles in metric spaces)**

Let $(X,d)$ be a [[metric space]], regarded as a [[topological space]] via its [[metric topology]] (example \ref{MetricTopology}).
Then every point $x \in X$ is closed (def \ref{ClosedSubset}),
hence every singleton subset $\{x\} \subset X$ is irreducible according to def. \ref{IrreducibleClosureOfPoint}.

Let $\mathbb{R}$ be the 1-dimensional [[Euclidean space]] (example \ref{EuclideanNorm})
with its [[metric topology]] (example \ref{MetricTopology}). Then for $a \lt c \subset \mathbb{R}$
the closed interval $[a,c] \subset \mathbb{R}$ (example \ref{OpenAndClosedIntervals} ) is _not_
irreducible, since for any $b \in \mathbb{R}$ with $a \lt b \lt c$ it is the union of two smaller closed subintervals:

$$
  [a,c] \,=\, [a, b] \cup [b, c]
  \,.
$$

In fact we will see below (prop. \ref{SoberFromHausdorff}) that in a metric space the singleton subsets are precisely the only
irreducible closed subsets.

=--

Often it is useful to re-express the condition of irreducibility of closed subspaces
in terms of complementary open subsets:

+-- {: .num_prop #OpenSubsetVersionOfClosedIrreducible}
###### Proposition
**(irreducible closed subsets in terms of prime open subsets)**

Let $(X, \tau)$ be a [[topological space]], and let $P \in \tau $ be a proper [[open subset]] of $X$,
hence so that the [[complement]] $F \coloneqq X\backslash P$ is a [[inhabited|non-empty]] [[closed subspace]]. Then $F$
is [[irreducible closed subspace|irreducible]] in the sense of def. \ref{ClosedIrreducible} precisely if whenever $U_1,U_2 \in \tau$ are open subsets
with $U_1 \cap U_2 \subset P$ then $U_1 \subset P$ or $U_2 \subset P$:

$$
  \left(
    X \backslash P \,\,\text{irreducible}
  \right)
  \;\Leftrightarrow\;
  \left(
    \underset{U_1, U_2 \in \tau}{\forall }
    \left(
      \left(
        U_1 \cap U_2 \subset P
      \right)
      \;\Rightarrow\;
      \left(U_1 \subset P \;\text{or}\; U_2 \subset P\right)
    \right)
  \right)
  \,.
$$

The open subsets $P \subset X$ with this property are also called the _prime open subsets_ in $\tau_X$.

=--

+-- {: .proof}
###### Proof

Observe that every [[closed subset]] $F_i \subset F$ may be exhibited as the [[complement]]

$$
  F_i = F \backslash U_i
$$

of some open subset $U_i \in \tau$ with respect to $F$. Observe that under this identification the condition
that $U_1 \cap U_2 \subset P$ is equivalent to the condition that $F_1 \cup F_2 = F$,
because it is equivalent to the equation labeled $(\star)$ in the following sequence of equations:

$$
\begin{aligned}
  F_1 \cup F_2
  & =
  (F \backslash U_1) \cup (F \backslash U_2)
  \\
  &
  = \left( X \backslash (P \cup U_1) \right) \cup \left( X \backslash P \cup U_2 \right)
  \\
  & = X \backslash
  \left(
    \left(
      P \cup U_1
    \right)
    \cap
    \left(
      P \cup U_2
    \right)
  \right)
  \\
  & = X \backslash ( P \cup (U_1 \cap U_2)  )
  \\
  & \stackrel{(\star)}{=}   X \backslash P
  \\
  & = F
  \,.
\end{aligned}
\,.
$$

Similarly, the condition that $U_i \subset P$ is equivalent to the condition that $F_i = F$,
because it is equivalent to the equality $(\star)$ in the following sequence of equalities:

$$
  \begin{aligned}
    F_i &= F \backslash U_i
    \\
    & = X \backslash ( P \cup U_i )
    \\
    & \stackrel{(\star)}{=} X \backslash P
    \\
    & =
    F
  \end{aligned}
  \,.
$$

Under these identifications, the two conditions are manifestly the same.

=--

We consider yet another equivalent characterization of irreducible closed subsets,
prop. \ref{FrameHomomorphismsToPointAreIrrClSub} below, which will be needed in the
discussion of the [[separation axioms]] further [below](#SeparationAxioms).
Stating this requires the following concept of "[[frame]]" [[homomorphism]],
the natural kind of [[homomorphisms]] between [[topological spaces]] if we were to forget the
underlying set of points of a topological space, and only remember the set $\tau_X$ with its
operations induced by taking finite intersections and arbitrary unions:

+-- {: .num_defn #HomomorphismOfFramesOfOpens}
###### Definition
**([[frame]] homomorphisms)**

Let $(X,\tau_X)$ and $(Y,\tau_Y)$ be [[topological spaces]] (def. \ref{TopologicalSpace}).
Then a function

$$
  \tau_X \longleftarrow \tau_Y \;\colon\; \phi
$$

between their [[frame of opens|sets of open subsets]] is called a _[[frame]] [[homomorphism]]_
if it preserves

1. arbitrary [[unions]];

1. [[finite number|finite]] [[intersections]].

In other words, $\phi$ is a frame homomorphism precisely if

1. for every [[set]] $I$ and every $I$-indexed set $\{U_i \in \tau_Y\}_{i \in I}$ of elements of $\tau_Y$, then

   $$
     \phi\left(\underset{i \in I}{\cup} U_i\right) \;=\; \underset{i \in I}{\cup} \phi(U_i)\;\;\;\;\in \tau_X
     \,,
   $$

1. for every [[finite set]] $J$ and every $J$-indexed set $\{U_j \in \tau_Y\}_{j \in J}$ of elements in $\tau_Y$, then

   $$
     \phi\left(\underset{j \in J}{\cap} U_j\right)
       \;=\;
     \underset{j \in J}{\cap} \phi(U_j)
     \;\;\;\;\in \tau_X
     \,.
   $$

=--

+-- {: .num_remark #PreservationOfInclusionsByFrameHomomorphism}
###### Remark
**(frame homomorphisms preserve inclusions)**

A [[frame]] [[homomorphism]] $\phi$ as in def. \ref{HomomorphismOfFramesOfOpens}
necessarily also preserves inclusions in that

* for every inclusion $U_1 \subset U_2$ with $U_1, U_2 \in \tau_Y \subset P(Y)$ then

  $$
    \phi(U_1) \subset \phi(U_2) \;\;\;\;\;\;\; \in \tau_X
    \,.
  $$

This is because inclusions are witnessed by unions

$$
  (U_1 \subset U_2)
    \;\Leftrightarrow\;
  \left( U_1 \cup U_2 = U_2 \right)
$$

or alternatively because inclusions are witnessed by finite intersections:

$$
  (U_1 \subset U_2)
    \;\Leftrightarrow\;
  \left(
    U_1 \cap U_2 = U_1
  \right)
  \,.
$$

=--

+-- {: .num_example #ContinuousFunctionGivesFrameHomomorphism}
###### Example
**(pre-images of continuous functions are frame homomorphisms)**

Let $(X,\tau_X)$ and $(Y,\tau_Y)$ be two [[topological spaces]].
One way to obtain a function between their sets of open subsets

$$
  \tau_X \longleftarrow \tau_Y \;\colon\; \phi
$$

is to specifiy a function

$$
  f \colon X \longrightarrow Y
$$

of their underlying sets, and take $\phi \coloneqq f^{-1}$ to be the
[[pre-image]] operation. A priori this is a function of the form

$$
  P(Y) \longleftarrow P(X) \;\colon\; f^{-1}
$$

and hence in order for this to co-restrict to $\tau_X \subset P(X)$ when restricted to $\tau_Y \subset P(Y)$
we need to demand that, under $f$, pre-images of open subsets of $Y$ are open subsets of $Z$.
Below in def. \ref{ContinuousMaps} we highlight these as the _[[continuous functions]]_ between toopological spaces.

$$
  f \;\colon\; (X,\tau_X) \longrightarrow (Y, \tau_Y)
$$

In this case then

$$
  \tau_X \longleftarrow \tau_Y \;\colon\; f^{-1}
$$

is a frame homomorphism in the sense of def. \ref{HomomorphismOfFramesOfOpens}.

=--

For the following recall from example \ref{Point}
the [[point topological space]]  $\ast = (\{1\}, \tau_\ast = \left\{\emptyset, \{1\}\right\})$.


+-- {: .num_prop #FrameHomomorphismsToPointAreIrrClSub}
###### Proposition
**(irreducible closed subsets are equivalently frame homomorphisms to opens of the point)**

For $(X,\tau)$ a [[topological space]], then there is a [[natural bijection|natural]] [[bijection]] between
the [[irreducible closed subspaces]] of $(X,\tau)$ (def. \ref{ClosedIrreducible}) and the
[[frame]] [[homomorphisms]] from $\tau_X$ to $\tau_\ast$, and this bijection is given by

$$
  \array{
    FrameHom(\tau_X, \tau_\ast)
      &\underoverset{}{\simeq}{\longrightarrow}&
    IrrClSub(X)
    \\
    \phi
      &\mapsto&
    X \backslash \left( U_\emptyset(\phi) \right)
  }
$$

where $U_\emptyset(\phi)$ is the [[union]] of all elements $U \in \tau_x$ such that $\phi(U) = \emptyset$:

$$
  U_{\emptyset}(\phi)
    \coloneqq
  \underset{{U \in \tau_X} \atop {\phi(U) = \emptyset} }{\cup}
   \left( U \right)
  \,.
$$

=--

See also ([Johnstone 82, II 1.3](#Johnstone82)).

+-- {: .proof}
###### Proof

First we need to show that the function is well defined in that given
a frame homomorphism $\phi \colon \tau_X \to \tau_\ast$ then  $X \backslash U_\emptyset(\phi)$
is indeed an irreducible closed subspace.

To that end observe that:

$(\ast)$ _If there are two elements $U_1, U_2 \in \tau_X$ with $U_1 \cap U_2 \subset U_{\emptyset}(\phi)$
then $U_1 \subset U_{\emptyset}(\phi)$ or $U_2 \subset U_{\emptyset}(\phi)$._

This is because

$$
  \begin{aligned}
    \phi(U_1) \cap \phi(U_2)
    & =
    \phi(U_1 \cap U_2)
    \\
    & \subset \phi(U_{\emptyset}(\phi))
    \\
    & =
    \emptyset
  \end{aligned}
  \,,
$$

where the first equality holds because $\phi$ preserves finite intersections by def. \ref{HomomorphismOfFramesOfOpens}, the inclusion holds because $\phi$ respects
inclusions by remark \ref{PreservationOfInclusionsByFrameHomomorphism}, and the second equality holds because $\phi$ preserves arbitrary unions
by def. \ref{HomomorphismOfFramesOfOpens}.
But in $\tau_\ast = \{\emptyset, \{1\}\}$ the intersection of two open subsets is empty precisely if at least one of them is empty,
hence $\phi(U_1) = \emptyset$ or $\phi(U_2) = \emptyset$. But this means that $U_1 \subset U_{\emptyset}(\phi)$ or $U_2 \subset U_{\emptyset}(\phi)$, as claimed.

Now according to prop. \ref{OpenSubsetVersionOfClosedIrreducible}
the condition $(\ast)$ identifies the [[complement]]
$X \backslash U_{\emptyset}(\phi)$ as an [[irreducible closed subspace]] of $(X,\tau)$.

Conversely, given an irreducible closed subset $X \backslash U_0$, define $\phi$ by

$$
  \phi
    \;\colon\;
  U
    \mapsto
  \left\{
    \array{
      \emptyset & \vert \, \text{if} \, U \subset U_0
      \\
      \{1\} & \vert \, \text{otherwise}
    }
  \right.
  \,.
$$

This does preserve

1. arbitrary unions

   because $\phi(\underset{i}{\cup} U_i) = \{\emptyset\}$ precisely if $\underset{i}{\cup}U_i \subset U_0$ which is the
   case precisely if all $U_i \subset U_0$, which means that all $\phi(U_i) = \emptyset$ and because $\underset{i}{\cup}\emptyset = \emptyset$;

   while $\phi(\underset{i}{\cup}U_1) = \{1\}$ as soon as one of the $U_i$ is not contained in $U_0$, which means that
   one of the $\phi(U_i) = \{1\}$ which means that $\underset{i}{\cup} \phi(U_i) = \{1\}$;

1. finite intersections

   because if $U_1 \cap U_2 \subset U_0$, then by $(\ast)$ $U_1 \in U_0$ or $U_2 \in U_0$, whence $\phi(U_1) = \emptyset$
   or $\phi(U_2) = \emptyset$, whence with $\phi(U_1 \cap U_2) = \emptyset$ also $\phi(U_1) \cap \phi(U_2) = \emptyset$;

   while if $U_1 \cap U_2$ is not contained in $U_0$ then neither $U_1$ nor $U_2$ is contained in $U_0$ and hence with
   $\phi(U_1 \cap U_2) = \{1\}$ also $\phi(U_1) \cap \phi(U_2) = \{1\} \cap \{1\} = \{1\}$.

Hence this is indeed a frame homomorphism $\tau_X \to \tau_\ast$.

Finally, it is clear that these two operations are inverse to each other.

=--



$\,$



## Continuous functions
 {#ContinuousFunctions}

With the concept of [[topological spaces]] in hand (def. \ref{TopologicalSpace})
it is now immediate to formally implement in abstract generality the
statement of prop. \ref{ContinuityBetweenMetricSpacesInTermsOfOpenSets}:

+-- {: principle}
**principle of continuity**

$\,$ $\,$ _Continuous pre-Images of open subsets are open._

=--

+-- {: .num_defn #ContinuousMaps}
###### Definition
**(continuous function)**

A _[[continuous function]]_ between [[topological spaces]] (def. \ref{TopologicalSpace})

$$
  f \colon (X, \tau_X) \to (Y, \tau_Y)
$$

is a [[function]] between the underlying sets,

$$
  f \colon X \longrightarrow Y
$$

such that [[pre-images]] under $f$ of open subsets of $Y$ are open subsets of $X$.

=--



We may equivalently state this in terms of [[closed subsets]]:

+-- {: .num_prop #ClosedSubsetContinuity}
###### Proposition

Let $(X_1, \tau_X)$ and $(Y,\tau_Y)$ be two [[topological spaces]] (def. \ref{TopologicalSpace}).
Then a [[function]]

$$
  f \;\colon\; X \longrightarrow Y
$$

between the underlying [[sets]] is [[continuous function|continuous]] in the sense of def. \ref{ContinuousMaps}
precisely if [[pre-images]] under $f$ of [[closed subsets]] of $Y$ (def. \ref{ClosedSubset}) are
closed subsets of $X$.

=--

+-- {: .proof}
###### Proof

This follows since taking [[pre-images]] commutes with taking [[complements]].

=--

$\,$

Before looking at first examples of continuous functions [below](#ContinuousFunctionsExamples)
we consider now an informal remark
on the resulting global structure, the "[[category of topological spaces]]", remark \ref{TopCategory} below.
This is a language that serves to make transparent key phenomena in [[topology]]
which we encounter further below, such as the [Tn-reflection](#HausdorffReflections) (remark \ref{ReflectiveSubcategory} below),
and the [universal constructions](#UniversalConstructions).

+-- {: .num_remark #TopCategory}
###### Remark
**([[concrete category|concrete]] [[category of topological spaces]])**

For $X_1, X_2, X_3$ three [[topological spaces]] and for

$$
  X_1 \overset{f}{\longrightarrow} X_2
  \phantom{AA}\text{and}\phantom{AA}
  X_2 \overset{g}{\longrightarrow} X_3
$$

two [[continuous functions]] (def. \ref{ContinuousMaps}) then their [[composition]]

$$
  f_2 \circ f_1
  \;\colon\;
  X_1 \overset{f}{\longrightarrow} X_2 \overset{f_2}{\longrightarrow} X_3
$$

is clearly itself again a continuous function from $X_1$ to $X_3$.
Moreover, this composition operation is clearly _[[associativity|associative]]_, in that for

$$
  X_1 \overset{f}{\longrightarrow} X_2
  \phantom{AA}\text{and}\phantom{AA}
  X_2 \overset{g}{\longrightarrow} X_3
  \phantom{AA}\text{and}\phantom{AA}
  X_3 \overset{h}{\longrightarrow} X_4
$$

three [[continuous functions]], then

$$
  f_3 \circ (f_2 \circ f_1)
   =
  (f_3 \circ f_2) \circ f_1
  \;\colon\;
  X_1 \longrightarrow X_3
  \,.
$$

Finally, the composition operation is also clearly _[[unitality|unital]]_, in that for
each topological space $X$ there exists the [[identity]] function $id_X \colon X \to X$
and for $f \colon X_1 \to X_2$ any continuous function then

$$
  id_{X_2} \circ f  \;=\; f \;=\; f \circ id_{X_1}
  \,.
$$

One summarizes this situation by saying that:

1. [[topological spaces]] constitute the _[[objects]]_,

1. [[continuous functions]] constitute the _[[morphisms]]_ ([[homomorphisms]])

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/AssociativityDiagram.png" width="400">
</div>

of  a _[[category]]_, called the _[[category of topological spaces]]_ ("[[Top]]" for short).

It is useful to depict collections of [[objects]] with [[morphisms]] between them
by [[diagrams]], like this one:

$\,$

$\,$

$\,$

> graphics grabbed from [Lawvere-Schanuel 09](#category+theory#LawvereSchanuel09).

There are other categories. For instance there is the [[category of sets]] ("[[Set]]" for short) whose

1. [[objects]] are [[sets]],

1. [[morphisms]] are plain [[functions]] between these.

The two categories [[Top]] and [[Set]] are different, but related. After all,

1. an [[object]] of [[Top]] (hence a [[topological space]]) is an [[object]] of [[Set]] (hence a [[set]])
equipped with [[extra structure]] (namely with a [[topological space|topology]]);

1. a [[morphism]] in [[Top]] (hence a [[continuous function]]) is a [[morphism]] in [[Set]] (hence a plain [[function]])
   with the [[extra property]] that it preserves this extra structure.

Hence we have the _underlying set assigning function_

$$
  \array{
    Top &\overset{U}{\longrightarrow}& Set
    \\
    \\
    (X,\tau) &\overset{\phantom{AAa}}{\mapsto}& X
  }
$$

from the [[class]] of [[topological spaces]] to the [[class]] of [[sets]]. But more is true:
every [[continuous function]] between topological spaces is, by definition,
in particular a function on underlying sets:

$$
  \array{
    Top &\overset{U}{\longrightarrow}& Set
    \\
    \\
    (X,\tau_X) &\overset{\phantom{AAA}}{\mapsto}& X
    \\
    {}^{\mathllap{f}}\downarrow &\overset{}{\mapsto}& \downarrow^{\mathrlap{f}}
    \\
    (Y, \tau_Y) &\underset{\phantom{AAA}}{\mapsto}& Y
  }
$$

and this assignment (trivially) respects the [[composition]] of morphisms and the [[identity morphisms]].

Such a [[function]] between [[classes]] of [[objects]] of [[categories]], which is extended to a
function on the [[sets]] of [[homomorphisms]] between these objects in a way that respects [[composition]]
and [[identity morphisms]] is called a _[[functor]]_.  If we write an arrow between categories

$$
  U \;\colon\; Top \longrightarrow Set
$$

then it is understood that we mean not just a [[function]] between their [[classes]] of [[objects]],
but a [[functor]].

The functor $U$ at hand has the special property that it does not do
much except _[[stuff, structure, property|forgetting extra structure]]_, namely the extra structure on a
set $X$ given by a choice of topology $\tau_X$. One also speaks of a _[[forgetful functor]]_.

This is intuitively clear, and we may easily formalize it: The [[functor]] $U$ has the special property
that as a [[function]] between [[sets]] of [[homomorphisms]] ("[[hom sets]]", for short) it is [[injective function|injective]].
More in detail, given topological spaces $(X,\tau_X)$ and $(Y,\tau_Y)$ then the component function of $U$
from the set of [[continuous function]] between these spaces to the set of plain functions between their underlying sets

$$
  \array{
    \left\{
      (X,\tau_X)
        \underoverset{\text{function}}{\text{continuous}}{\longrightarrow}
      (Y,\tau_Y)
    \right\}
      &\;\overset{\phantom{AA}U\phantom{AA}}{\mapsto}\;&
    \left\{
      X
        \underset{\text{function}}{\longrightarrow}
      Y
    \right\}
  }
$$

is an [[injective function]], including the continuous functions among all functions of underlying sets.

A [[functor]] with this property, that its component functions
between all [[hom-sets]] are injective, is called a _[[faithful functor]]_.

A [[category]] equipped with a [[faithful functor]] to [[Set]] is called a _[[concrete category]]_.

Hence [[Top]] is canonically a [[concrete category]].



=--

+-- {: .num_example #FunctorialProductSpace}
###### Example
**([[product topological space]] construction is [[functor|functorial]])**

For $\mathcal{C}$ and $\mathcal{D}$ two [[categories]] as in remark \ref{TopCategory}
(for instance [[Top]] or [[Set]]) then we obtain a new category denoted $\mathcal{C} \times \mathcal{D}$
and called their _[[product category]]_ whose

1. [[objects]] are [[pairs]] $(c,d)$ with $c$ an object of $\mathcal{C}$ and $d$ an object of $\mathcal{D}$;

* [[morphisms]] are [[pairs]] $(f,g) \colon (c,d) \to (c', d')$ with $f \colon c \to d$ a morphism of $\mathcal{C}$
and $g \colon d \to d'$ a morphisms of $\mathcal{D}$,

* [[composition]] of morphisms is defined pairwise $(f', g') \circ (f,g) \coloneqq ( f' \circ f, g' \circ g )$.

This concept secretly underlies the construction of [[product topological spaces]]:

Let $(X_1,\tau_{X_1})$, $(X_2, \tau_{X_2})$, $(Y_1, \tau_{Y_1})$ and $(Y_2, \tau_{Y_2})$ be [[topological spaces]].
Then for all [[pairs]] of [[continuous functions]]

$$
  f_1 \;\colon\; (X_1, \tau_{X_1}) \longrightarrow (Y_1, \tau_{Y_1})
$$

and

$$
  f_2 \;\colon\; (X_2, \tau_{X_2}) \longrightarrow (Y_2, \tau_{Y_2})
$$

the canonically induced function on [[Cartesian products]] of sets

$$
  \array{
    X_1 \times X_2 & \overset{  f_1 \times f_2 }{\longrightarrow} & Y_1 \times Y_2
    \\
    (x_1, x_2) &\mapsto& ( f_1(x_1), f_2(x_2) )
  }
$$

is a [[continuous function]] with respect to the [[product topological spaces|binary product space topologies]]
(def. \ref{BinaryProductTopologicalSpace})

$$
  f_1 \times f_2
    \;\colon\;
  (X_1 \times X_2, \tau_{X_1 \times X_2})
    \longrightarrow
  (Y_1, \times Y_2, \tau_{Y_1 \times Y_2})
  \,.
$$

Moreover, this construction respects [[identity functions]] and [[composition]] of functions
in both arguments.

In the language of [[category theory]] (remark \ref{TopCategory}), this is summarized
by saying that the [[product topological space]] construction $(-) \times (-)$ extends to a _[[functor]]_
from the [[product category]] of the [[category]] [[Top]] with itself to itself:

$$
  (-) \times (-)
    \;\colon\;
  Top \times Top
    \longrightarrow
  Top
  \,.
$$

=--

$\,$

### Examples
 {#ContinuousFunctionsExamples}

We discuss here some basic examples of [[continuous functions]] (def. \ref{ContinuousMaps}) between [[topological spaces]] (def. \ref{TopologicalSpace}) to get a feeling for the nature of the concept.
But as with topological spaces themselves, continuous functions between them
are ubiquituous in mathematics, and no list will exhaust all classes of examples. Below in the section
_[Universal constructions](#UniversalConstructions)_ we discuss a general principle that serves to
produce examples of continuous functions with prescribed "[[universal properties]]".


+-- {: .num_example #TerminalityOfThePoint}
###### Example
**(point space is [[terminal object|terminal]])**

For $(X,\tau)$ any [[topological space]], then there is a unique continuous function

$$
  X \longrightarrow \ast
$$

from $X$ to the [[point topological space]] (def. \ref{Point}).


In the language of [[category theory]] (remark \ref{TopCategory}), this
says that the point $\ast$ is the _[[terminal object]]_ in the [[category]] [[Top]] of topological spaces.

=--

+-- {: .num_example #PointsViaContinuousFunctions}
###### Example
**([[constant functions|constant]] [[continuous functions]])**

For $(X, \tau)$ a [[topological space]] then for $x \in X$ any element of the underlying set,
there is a unique continuous function (which we denote by the same symbol)

$$
  x \;\colon\; \ast \longrightarrow X
$$

from the [[point topological space]] (def. \ref{Point}), whose image in $X$ is that element. Hence there is a [[natural bijection]]

$$
  \left\{
    \ast \overset{f}{\to} X
    \,\vert\, f \,\,\text{continuous}
  \right\}
    \;\simeq\;
  X
$$

between the continuous functions from the point to any topological space, and the underlying set of that topological space.

More generally, for $(X,\tau_X)$ and $(Y,\tau_Y)$ two topological spaces, then a continuous
function $X \to Y$ between them is called a _[[constant function]]_ with value some point $y \in Y$ if it
factors through the point spaces as

$$
  const_y
    \;\colon\;
  X \overset{\exists !}{\longrightarrow} \ast \overset{y}{\longrightarrow} Y
  \,.
$$

=--


+-- {: .num_defn #FunctionLocallyConstant}
###### Definition
**([[locally constant function]])**

For $(X.\tau_X)$, $(Y,\tau_Y)$ two [[topological spaces]], then a
a [[continuous function]] $f \colon (X,\tau_X) \to (Y,\tau_Y)$ (def. \ref{ContinuousMaps}) is called
_[[locally constant function|locally constant]]_ if every point $x \in X$ has a [[neighbourhood]]
on which the function is constant.

=--


+-- {: .num_example #ContinuousFunctionsIntoCoDiscreteTopologicalSpaces}
###### Example
**([[continuous functions]] into and out of [[discrete space|discrete]] and [[codiscrete spaces]])**

Let $S$ be a [[set]] and let $(X,\tau)$ be a [[topological space]]. Recall from example \ref{CoDiscreteTopology}

1. the [[discrete topological space]] $Disc(S)$;

1. the [[co-discrete topological space]] $CoDisc(S)$

on the underlying set $S$. Then [[continuous functions]] (def. \ref{ContinuousMaps}) into/out of these satisfy:

1. every [[function]] (of sets) $Disc(S) \longrightarrow X$ out of a discrete space is [[continuous function|continuous]];

1. every [[function]] (of sets) $X \longrightarrow CoDisc(S)$ into a codiscrete space is [[continuous function|continuous]].

Also:

* every [[continuous function]] $(X,\tau) \longrightarrow Disc(S)$ into a discrete space is [[locally constant function|locally constant]] (def. \ref{FunctionLocallyConstant}).


=--


+-- {: .num_example #Diagonal}
###### Example
**([[diagonal]])**

For $X$ a [[set]], its _[[diagonal]]_ $\Delta_X$ is the [[function]] from $X$
to the [[Cartesian product]] of $X$ with itsef, given by

$$
  \array{
     X &\overset{\Delta_X}{\longrightarrow}& X \times X
     \\
     x &\mapsto& (x,x)
  }
$$



For $(X,\tau)$ a [[topological space]], then the diagonal is a [[continuous function]]
to the [[product topological space]] (def. \ref{BinaryProductTopologicalSpace}) of $X$ with itself.

$$
  \Delta_X \;\colon\; (X, \tau) \longrightarrow (X \times X, \tau_{X \times X})
  \,.
$$

To see this, it is sufficient to see that the [[preimages]] of [[basis for a topology|basic opens]] $U_1 \times U_2$
in $\tau_{X \times X}$ are in $\tau_X$. But these pre-images are the [[intersections]] $U_1 \cap U_2 \subset X$,
which are open by the axioms on the topology $\tau_X$.

=--


+-- {: .num_example #ImageFactorization}
###### Example
**([[image factorization]])**

Let $f \;\colon\; (X, \tau_X) \longrightarrow (Y,\tau_Y)$ be a [[continuous function]].

Write $f(X) \subset Y$ for the [[image]] of $f$
on underlying sets, and consider the resulting factorization of $f$ through $f(X)$ on underlying sets:

$$
  f
  \;\colon\;
  X
    \overset{\text{surjective}}{\longrightarrow}
  f(X)
    \overset{\text{injective}}{\longrightarrow}
  Y
  \,.
$$

There are the following two ways to topologize the [[image]] $f(X)$ such as to make this a sequence of
two continuous functions:

1. By example \ref{SubspaceTopology} $f(X)$ inherits a [[topological subspace|subspace topology]] from $(Y,\tau_Y)$
which evidently makes the inclusion $f(X) \longrightarrow Y$ a [[continuous function]].

   Observe that this also makes $X \to f(X)$ a continuous function: An open subset of $f(X)$
   in this case is of the form $U_Y \cap f(X)$ for $U_Y \in \tau_Y$, and $f^{-1}( U_Y \cap f(X) ) = f^{-1}(U_Y)$,
   which is open in $X$ since $f$ is continuous.

1. By example \ref{QuotientTopologicalSpace} $f(X)$ inherits a [[quotient topological space|quotient topology]] from $(X,\tau_X)$
   which evidently makes the surjection $X \longrightarrow f(X)$ a [[continuous function]].

   Observe that this also makes $f(X) \longrightarrow Y$ a continuous function: The preimage under this map of an
   open subset $U_Y \in \tau_Y$ is the restriction $U_Y \cap f(X)$, and the pre-image of that under $X \to f(X)$ is
   $f^{-1}(U_Y)$, as before, which is open since $f$ is continuous, and therefore $U_Y \cap f(X)$ is open in the
   quotient topology.

=--

$\,$

Beware that in general a continuous function itself (as opposed to its [[pre-image]] function) neither
preserves [[open subsets]], nor [[closed subsets]], as the following examples show:

+-- {: .num_example}
###### Example

Regard the [[real numbers]] $\mathbb{R}$ as the 1-dimensional [[Euclidean space]] (example \ref{EuclideanNorm})
equipped with the [[metric topology]] (example \ref{MetricTopology}).
For $a \in \mathbb{R}$ the [[constant function]] (example \ref{PointsViaContinuousFunctions})

$$
  \array{
    \mathbb{R} &\overset{const_a}{\longrightarrow}& \mathbb{R}
    \\
    x &\mapsto& a
  }
$$

maps every [[open subset]] $U \subset \mathbb{R}$ to the [[singleton set]] $\{a\} \subset \mathbb{R}$, which is not open.

=--

+-- {: .num_example}
###### Example

Write $Disc(\mathbb{R})$ for the set of [[real numbers]] equipped with its [[discrete topology]] (def. \ref{CoDiscreteTopology})
and $\mathbb{R}$ for the set of [[real numbers]] equipped with its [[Euclidean space|Euclidean]] [[metric topology]]
(example \ref{EuclideanNorm}, example \ref{MetricTopology}). Then the [[identity function]] on the underlying sets

$$
  id_{\mathbb{R}} \;\colon\; Disc(\mathbb{R}) \longrightarrow \mathbb{R}
$$

is a [[continuous function]] (a special case of example \ref{ContinuousFunctionsIntoCoDiscreteTopologicalSpaces}).
A [[singleton set|singleton]] [[subset]] $\{a\} \in Disc(\mathbb{R})$ is open, but regarded as a subset
$\{a\} \in \mathbb{R}$ it is not open.


=--

+-- {: .num_example}
###### Example

Consider the set of [[real numbers]] $\mathbb{R}$ equipped with its [[Euclidean space|Euclidean]] [[metric topology]]
(example \ref{EuclideanNorm}, example \ref{MetricTopology}). The [[exponential function]]

$$
  \exp(-) \;\colon\; \mathbb{R} \longrightarrow \mathbb{R}
$$

maps all of $\mathbb{R}$ (which is a closed subset, since $\mathbb{R} = \mathbb{R} \backslash \emptyset$) to
the [[open interval]] $(0,\infty) \subset \mathbb{R}$, which is not closed.

=--

Those continuous functions that do happen to preserve
open or closed subsets get a special name:

+-- {: .num_defn #OpenMap}
###### Definition
**([[open maps]] and [[closed maps]])**

A [[continuous function]] $f \colon (X,\tau_X) \to (Y, \tau_Y)$ (def. \ref{ContinuousMaps}) is called

*  an _[[open map]]_ if the [[image]] under $f$ of an [[open subset]] of $X$ is an open subset of $Y$;

* a _[[closed map]]_ if the [[image]] under $f$ of a [[closed subset]] of $X$ (def. \ref{ClosedSubset}) is a closed subset of $Y$.

=--

+-- {: .num_example}
###### Example
**([[projections]] are open)**

For $(X_1,\tau_{X_1})$ and $(X_2,\tau_{X_2})$ two [[topological spaces]], then the projection maps

$$
  \pi_i \;\colon\; (X_1 \times X_2, \tau_{X_1 \times X_2}) \longrightarrow (X_i, \tau_{X_i})
$$

out of their [[product topological space]] (def. \ref{BinaryProductTopologicalSpace})

$$
  \array{
    X_1 \times X_2 &\overset{\pi_1}{\longrightarrow}& X_1
    \\
    (x_1, x_2) &\overset{\phantom{AAA}}{\mapsto}& x_1
  }
$$

$$
  \array{
    X_1 \times X_2 &\overset{\pi_2}{\longrightarrow}& X_2
    \\
    (x_1, x_2) &\overset{\phantom{AAA}}{\mapsto}& x_2
  }
$$


are [[open maps]] (def. \ref{OpenMap}).

=--

Below in prop. \ref{MapsFromCompactSpacesToHausdorffSpacesAreClosed} we find a large supply of [[closed maps]].



$\,$


Sometimes it is useful to recognize [[quotient topological space]] projections via [[saturated subsets]]
(essentially another term for pre-images of underlying sets):

+-- {: .num_defn #SubsetSaturated}
###### Definition
**([[saturated subset]])**

Let $f \;\colon\; X \longrightarrow Y$ be a [[function]] of [[sets]].
Then a [[subset]] $S \subset X$ is called an _$f$-[[saturated subset]]_ (or just _saturated subset_, if $f$ is understood)
if $S$ is the [[pre-image]] of its [[image]]:

$$
  \left(S \subset X \,\, f\text{-saturated} \right)
    \,\Leftrightarrow\,
  \left(
    S = f^{-1}(f(S))
  \right)
  \,.
$$

Here $f^{-1}(f(S))$ is also called the _$f$-saturation_ of $S$.

=--

+-- {: .num_example #PreImagesAreSaturatedSubsets}
###### Example
**(pre-images are saturated subsets)**

For $f \;\colon\; X \to Y$ any [[function]] of [[sets]], and $S_Y \subset Y$ any [[subset]] of $Y$, then the
[[pre-image]] $f^{-1}(S_Y) \subset X$ is an $f$-[[saturated subset]] of $X$ (def. \ref{SubsetSaturated}).

=--

Observe that:

+-- {: .num_lemma #ComplementOfSaturatedSubsetIsSaturated}
###### Lemma

Let $f \colon X \longrightarrow Y$ be a [[function]]. Then a [[subset]] $S \subset X$
is $f$-saturated (def. \ref{SubsetSaturated}) precisely if its [[complement]]
$X \backslash S$ is saturated.

=--


+-- {: .num_prop #DetectViaSaturatedSubsetsContinuousQuotientMap}
###### Proposition
**(recognition of quotient topologies)**

A [[continuous function]] (def. \ref{ContinuousMaps})

$$
  f \;\colon\; (X, \tau_X) \longrightarrow (Y,\tau_Y)
$$

whose underlying function $f \colon X \longrightarrow Y$ is [[surjective function|surjective]]
exhibits $\tau_Y$ as the corresponding [[quotient topological space|quotient topology]] (def. \ref{QuotientTopologicalSpace})
precisely if $f$ sends open and $f$-[[saturated subsets]] in $X$ (def. \ref{SubsetSaturated}) to open subsets of $Y$.
By lemma \ref{ComplementOfSaturatedSubsetIsSaturated} this is the case precisely if it sends
closed and $f$-saturated subsets to closed subsets.

=--

We record the following technical lemma about saturated subspaces, which we will need below
to prove prop. \ref{QuotientProjectionsOutOfCompactHausdorffSpacesAreClosedPreciselyIfTheCodomainIsHausdorff}.

+-- {: .num_lemma #SaturatedOpenNeighbourhoodsOfSaturatedClosedSubsets}
###### Lemma
**(saturated open neighbourhoods of saturated closed subsets under closed maps)**

Let

1. $f \;\colon\; (X, \tau_X) \longrightarrow (Y, \tau_Y)$ be a [[closed map]] (def. \ref{OpenMap});

1. $C \subset X$ be a [[closed subset]] of $X$ (def. \ref{ClosedSubset}) which is $f$-[[saturated subset|saturated]] (def. \ref{SubsetSaturated});

1. $U \supset C$ be an [[open subset]] containing $C$;

then there exists a smaller open subset $V$ still containing $C$

$$
  U \supset V \supset C
$$

and such that $V$ is still $f$-[[saturated subset|saturated]].

=--

+-- {: .proof}
###### Proof

We claim that the [[complement]] of $X$ by the $f$-saturation (def. \ref{SubsetSaturated}) of the complement of $X$ by $U$

$$
  V \coloneqq X \backslash \left(  f^{-1}\left( f\left(  X \backslash U \right)  \right) \right)
$$

has the desired properties. To see this, observe first that

1. the [[complement]] $X \backslash U$ is closed, since $U$ is assumed to be open;

1. hence the image $f(X\backslash U)$ is closed, since $f$ is assumed to be a closed map;

1. hence the pre-image $f^{-1}\left( f\left(  X \backslash U \right)\right)$ is closed, since $f$ is continuous
   (using prop. \ref{ClosedSubsetContinuity}), therefore its complement $V$ is indeed open;

1. this pre-image $f^{-1}\left( f\left(  X \backslash U \right) \right)$ is saturated (by example \ref{PreImagesAreSaturatedSubsets})
   and hence also its complement $V$ is saturated (by lemma \ref{ComplementOfSaturatedSubsetIsSaturated}).

Therefore it now only remains to see that $U \supset V \supset C$.

By [[de Morgan's law]] (remark \ref{deMorgan}) the inclusion $U \supset V$ is equivalent to the inclusion $f^{-1}\left( f\left(  X \backslash U \right)\right) \supset X \backslash U$,
which is clearly the case.

The inclusion $V \supset C$ is equivalent to
$f^{-1}\left( f\left(  X \backslash U \right) \right) \,\cap \, C = \emptyset$.
Since $C$ is saturated by assumption, this is
equivalent to $f^{-1}\left( f\left(  X \backslash U \right)\right) \,\cap \, f^{-1}(f(C)) = \emptyset$.
This in turn holds precisely if $f\left(  X \backslash U \right) \,\cap \, f(C)  = \emptyset$.
Since $C$ is saturated, this holds precisely if $X \backslash U \cap C = \emptyset$, and this is true by the assumption
that $U \supset C$.

=--



$\,$


### Homeomorphisms
 {#Homeomorphisms}


With the [[objects]] ([[topological spaces]]) and the [[morphisms]] ([[continuous functions]]) of the [[category]] [[Top]] thus defined
(remark \ref{TopCategory}), we obtain the concept of "sameness" in topology. To make this precise, one says that a [[morphism]]

$$
  X \overset{f}{\to} Y
$$

in a [[category]] is an _[[isomorphism]]_ if there exists a morphism going the other way around

$$
  X \overset{g}{\longleftarrow} Y
$$

which is an [[inverse]] in the sense that both its [[compositions]] with $f$ yield an [[identity morphism]]:

$$
  f \circ g = id_Y \;\;\;\;\; and \;\;\;\;\; g \circ f = id_X
  \,.
$$

Since such $g$ is unique if it exsist, one often writes "$f^{-1}$" for this [[inverse morphism]]. However, in the context
of [[topology]] then $f^{-1}$ usually refers to the [[pre-image]] function of a given [[function]] $f$, and in these
notes we will stick to this usage and never use "$(-)^{-1}$" to denote [[inverses]].

+-- {: .num_defn #Homeomorphism}
###### Definition
**([[homeomorphisms]])**


An [[isomorphism]] in the [[category]] [[Top]] (remark \ref{TopCategory})
of [[topological spaces]] (def. \ref{TopologicalSpace}) with [[continuous functions]] between them (def. \ref{ContinuousMaps})
is called a _[[homeomorphism]]_.

Hence a _[[homeomorphism]]_ is a [[continuous function]]

$$
  f \;\colon\; (X, \tau_X) \longrightarrow (Y, \tau_Y)
$$

between two [[topological spaces]] $(X,\tau_X)$, $(Y,\tau_Y)$
such that there exists another continuous function the other way around

$$
  (X, \tau_X) \longleftarrow (Y, \tau_Y) \;\colon\; g
$$

such that their [[composition|composites]] are the [[identity functions]] on $X$ and $Y$,
respectively:

$$
  f \circ g = id_{Y} \;\;\;and\;\;\; g \circ f = id_{X}
  \,.
$$


<img src="https://ncatlab.org/nlab/files/Homeomorphism.png" width="560">

> graphics grabbed from [Munkres 75](#Munkres75)

We notationally indicate that a continuous function is a homeomorphism by the symbol "$\simeq$".

$$
  f \;\colon\; (X,\tau_X) \overset{\simeq}{\longrightarrow} (Y,\tau_Y)
  \,.
$$

If there is _some_, possibly unspecified, homeomorphism between topological spaces $(X,\tau_X)$ and $(Y,\tau_Y)$,
then we also write

$$
  (X,\tau_X) \,\simeq\, (Y,\tau_Y)
$$

and say that the two topological spaces _are homeomorphic._

A [[property]]/[[predicate]] $P$ of [[topological spaces]] which is [[invariant]] under homeomorphism in that

$$
  \left(
     (X, \tau_X)
     \,
       \simeq
     \,
     (Y,\tau_Y)
  \right)
  \;\Rightarrow\;
  \left(
    P(X,\tau_X)
     \,\Leftrightarrow\,
    P(Y,\tau_Y)
  \right)
$$

is called a _[[topological property]]_ or _topological invariant_.

=--


+-- {: .num_remark }
###### Remark

If $f \colon (X, \tau_X) \to (Y, \tau_Y)$ is a [[homeomorphism]] (def. \ref{Homeomorphism}) with inverse coninuous function $g$, then


1. also $g$ is a homeomophism, with inverse continuous function $f$;

1. the underlying function of sets $f \colon X \to Y$ of a homeomorphism $f$ is necessarily a [[bijection]], with inverse bijection $g$.

=--

But beware that not every [[continuous function]] which is [[bijection|bijective]] on underlying sets
is a homeomorphism. While an [[inverse function]] $g$ will exists on the level of functions of sets, this inverse may fail
to be continuous:

+-- {: .num_example #ExponentialMapFromHalfOpenIntervalToCircle}
###### Counter Example

Consider the [[continuous function]]

$$
  \array{
    [0,2\pi) &\longrightarrow& S^1 \subset \mathbb{R}^2
    \\
    t &\mapsto& (cos(t), sin(t))
  }
$$

from the [[half-open interval]] (def. \ref{OpenAndClosedIntervals}) to the unit circle $S^1 \coloneqq S_0(1) \subset \mathbb{R}^2$ (def. \ref{OpenBalls}), regarded as a [[topological subspace]] (example \ref{SubspaceTopology})
of the [[Euclidean plane]] (example \ref{EuclideanNorm}).

The underlying function of sets of $f$ is a [[bijection]]. The [[inverse function]] of sets however fails to be continuous
at $(1,0) \in S^1 \subset \mathbb{R}^2$. Hence this $f$ is _not_ a [[homeomorphism]].

Indeed, below we see that the two topological spaces $[0,2\pi)$ and $S^1$ are distinguished by
[[topological invariants]], meaning that they cannot be homeomorphic via _any_ (other) choice of homeomorphism.
For example $S^1$ is a [[compact topological space]]
(def. \ref{CompactTopologicalSpace})
while $[0,2\pi)$ is not, and $S^1$ has a non-trivial [[fundamental group]], while that of $[0,2\pi)$
is trivial ([this prop.](Introduction+to+Topology+--+2#FundamentalGroup)).

=--

Below in example \ref{ContinuousBijectionFromClosedIntervalToCircle} we discuss a practical criterion under which continuous bijections are homeomorphisms after all. But immediate from the definitions is the following characterization:

+-- {: .num_prop }
###### Proposition
**([[homeomorphisms]] are the [[continuous function|continuous]] and [[open map|open]] [[bijections]])

Let $f \;\colon\; (X, \tau_X) \longrightarrow (Y,\tau_Y)$ be a [[continuous function]]
between [[topological spaces]] (def. \ref{ContinuousMaps}). Then the following are equivalence:

1. $f$ is a [[homeomorphism]];

1. $f$ is a [[bijection]] and an [[open map]] (def. \ref{OpenMap});

1. $f$ is a [[bijection]] and a [[closed map]] (def. \ref{OpenMap}).

=--

+-- {: .proof}
###### Proof

It is clear from the definition that a homeomorphism in particular has to be a bijection.
The condition that the [[inverse function]] $Y \leftarrow X \colon g$ be continuous means
that the [[pre-image]] function of $g$ sends open subsets to open subsets. But by $g$ being the inverse to
$f$, that pre-image function is equal to $f$, regarded as a function on subsets:

$$
  g^{-1} = f \;\colon\; P(X) \to P(Y)
  \,.
$$

Hence $g^{-1}$ sends opens to opens precisely if $f$ does, which is the case precisely if $f$ is an open map,
by definition.
This shows the equivalence of the first two items. The equivalence between the first and the third follows
similarly via prop. \ref{ClosedSubsetContinuity}.

=--


$\,$


Now we consider some actual **examples** of [[homeomorphisms]]:


+-- {: .num_example #ConcreteAndAbstractPoint}
###### Example
**(concrete point homeomorphic to abstract point space)**

Let $(X,\tau_X)$ be a [[inhabited|non-empty]] [[topological space]], and let $x \in X$ be any point.
Regard the corresponding [[singleton]] [[subset]] $\{x\} \subset X$ as equipped with its
[[topological subspace|subspace topology]] $\tau_{\{x\}}$ (example \ref{SubspaceTopology}). Then this is
[[homomorphism|homeomorphic]] (def. \ref{Homeomorphism}) to the abstract [[point space]] from example \ref{Point}:

$$
  (\{x\}, \tau_{\{x\}} ) \,\simeq\, \ast
  \,.
$$

=--


+-- {: .num_example #OpenBallsHomeomorphicToRn}
###### Example
**(open interval homeomorphic to the real line)**

Regard the [[real line]] as the 1-dimensional [[Euclidean space]] (example \ref{EuclideanNorm}) with its [[metric topology]] (example \ref{MetricTopology}).

Then the open [[interval]] $(-1,1) \subset \mathbb{R}$ (def. \ref{OpenAndClosedIntervals})
regarded with its [[subspace topology]] (example \ref{SubspaceTopology}) is [[homeomorphic]] (def.\ref{Homeomorphism}) to all of the [[real line]]

$$
  (-1,1) \,\simeq\, \mathbb{R}^1
  \,.
$$

An [[inverse]] pair of [[continuous functions]] is for instance given (via example \ref{PolynoialsAreContinuous}) by


$$
  \array{
    f &\colon&  \mathbb{R}^1 &\longrightarrow& (-1,+1)
    \\
    && x &\mapsto& \frac{x}{\sqrt{1+ x^2}}
  }
$$

and

$$
  \array{
    g &\colon&  (-1,+1) &\longrightarrow& \mathbb{R}^1
    \\
    && x &\mapsto& \frac{x}{\sqrt{1 - x^2}}
  }
  \,.
$$

But there are many other choices for $f$ and $g$ that yield a homeomorphism.

Similarly, for all $a \lt b \in \mathbb{R}$

1. the [[open intervals]] $(a,b) \subset \mathbb{R}$
(example \ref{OpenAndClosedIntervals}) equipped with their [[topological subspace|subspace topology]]
are all homeomorphic to each other,

1. the closed intervals $[a,b]$ are all homeomorphic to each other,

1. the half-open intervals of the form $[a,b)$ are all homeomophic to each other;

1. the half-open intervals of the form $(a,b]$ are all homeomophic to each other.

Generally, every [[open ball]] in $\mathbb{R}^n$ (def. \ref{OpenBalls}) is [[homeomorphic]] to all of $\mathbb{R}^n$:

$$
  \left(
    B^\circ_0(\epsilon) \subset \mathbb{R}^n
  \right)
   \,\simeq\,
  \mathbb{R}^n
  \,.
$$

=--

While mostly the interest in a given homeomorphism is in it being
non-obvious from the definitions, many homeomorphisms that appear
in practice exhibit "obvious re-identifications" for which it is
of interest to leave them _consistently implicit_:


+-- {: .num_example #CartesianSymmetricMonoidalTop}
###### Example
**(homeomorphisms between iterated product spaces)**


Let $(X,\tau_X)$, $(Y,\tau_Y)$ and $(Z, \tau_Z)$ be [[topological spaces]].

Then:

1. There is an evident [[homeomorphism]] between the two ways of bracketing the three factors when forming their
   [[product topological space]] (def. \ref{BinaryProductTopologicalSpace}), called the _[[associator]]_:

   $$
     \alpha_{X,Y,Z}
       \;\colon\;
     \left(
       (X, \tau_X) \times (Y, \tau_Y)
     \right)
     \times
     (Z, \tau_Z)
       \overset{\phantom{AA}\simeq\phantom{AA}}{\longrightarrow}
     (X,\tau_X)
      \times
     \left(
       (Y,\tau_Y)
        \times
       (Z, \tau_Z)
     \right)
     \,.
   $$

1. There are evident [[homeomorphism]] between $(X,\tau)$ and its [[product topological space]] (def. \ref{BinaryProductTopologicalSpace}) with the [[point space]] $\ast$ (example \ref{Point}), called the left and right _[[unitors]]_:

   $$
     \lambda_X \;\colon\; \ast \times (X, \tau_X)  \overset{\phantom{AA}\simeq\phantom{AA}}{\longrightarrow} (X,\tau_X)
   $$

   and

   $$
     \rho_X \;\colon\; (X, \tau_X) \times \ast \overset{\phantom{AA}\simeq\phantom{AA}}{\longrightarrow} (X, \tau_X)
     \,.
   $$

1. There is an evident [[homeomorphism]] between the results of the two orders in which to form their [[product topological spaces]] (def. \ref{BinaryProductTopologicalSpace}), called the _[[braiding]]_:

   $$
     \beta_{X,Y}
       \;\colon\;
     (X,\tau_X) \times (Y,\tau_Y)
       \overset{\phantom{AA}\simeq\phantom{AA}}{\longrightarrow}
     (Y,\tau_Y) \times (X, \tau_X)
     \,.
   $$

Moreover, all these homeomorphisms are compatible with each other, in that they make the
following [[commuting diagram|diagrams commute]] (recall remark \ref{TopCategory}):

1. (triangle identity)
   $$
     \array{
        & (X \times \ast ) \times Y &\stackrel{\alpha_{X,\ast,Y}}{\longrightarrow} & X \times (\ast \times Y)
         \\
         & {}_{\rho_x \times id_Y}\searrow
         && \swarrow_{id_X \times \lambda_Y}
         &
        \\
        &&
        X \times Y
     }
   $$

1. {#PentagonIdentity} ([[pentagon identity]])
   $$
     \array{
       && (W \times X) \times (Y \times Z)
       \\
       & {}^{\mathllap{\alpha_{W \times X, Y, Z}}}\nearrow
        &&
       \searrow^{\mathrlap{\alpha_{W,X,Y \times Z}}}
       \\
       ((W \times X ) \times Y) \times Z
        && &&
       (W \times (X \times (Y \times Z)))
       \\
       {}^{\mathllap{\alpha_{W,X,Y}} \times id_Z }\downarrow
        && &&
       \uparrow^{\mathrlap{ id_W \times \alpha_{X,Y,Z} }}
       \\
       (W \times (X \times Y)) \times Z
         && \underset{\alpha_{W,X \times Y, Z}}{\longrightarrow} &&
       W \times ( (X \times Y) \times Z )
     }
   $$

1. (hexagon identities)
   $$
     \array{
       (X \times Y) \times Z
         &\stackrel{\alpha_{X,Y,Z}}{\longrightarrow}&
       X \times (Y \times Z)
       &\stackrel{\beta_{X,Y \times Z}}{\longrightarrow}&
       (Y \times Z) \times X
       \\
       \downarrow^{\beta_{X,Y} \times id_Z}
       &&&&
       \downarrow^{\alpha_{Y,Z,X}}
       \\
       (Y \times X) \times Z
       &\stackrel{\alpha_{Y,X,Z}}{\longrightarrow}&
       Y \times (X \times Z)
       &\stackrel{id_Y \times \beta_{X,Y}}{\longrightarrow}&
       Y \times (Z \times X)
     }
   $$

   and

   $$
     \array{
        X \times (Y \times Z)
          &\stackrel{\alpha^{inv}_{X,Y,Z}}{\longrightarrow}&
        (X \times Y) \times Z
         &\stackrel{\beta_{X \times Y, Z}}{\longrightarrow}&
        Z \times (X \times Y)
        \\
          \downarrow^{id_X \times \beta_{Y,Z}}
        &&&&
          \downarrow^{\alpha^{inv}_{Z,X,Y}}
        \\
        X \times (Z \times Y)
          &\stackrel{\alpha^{inv}_{X,Z,Y}}{\longrightarrow}&
        (X \times Z) \times Y
          &\stackrel{\beta_{X,Z} \times id}{\longrightarrow}&
        (Z \times X) \times Y
       }
     \,,
   $$

1. (symmetry)

   $$
     \beta_{Y,X} \circ \beta_{X,Y}
      \;=\;
     id \;\colon\; (X_1 \times X_2 \tau_{X_1 \times X_2}) \to (X_1 \times X_2 \tau_{X_1 \times X_2})
     \,.
   $$

In the language of [[category theory]] (remark \ref{TopCategory}), all this is summarized by
saying that the the [[functor|functorial]] construction $(-) \times (-)$ of [[product topological spaces]]
(example \ref{FunctorialProductSpace})
gives the [[category]] [[Top]] of [[topological spaces]] the [[structure]] of a
_[[monoidal category]]_ which moreover is _[[symmetric monoidal category|symmetrically]] [[braided monoidal category|braided]]_.

From this, a basic result of [[category theory]], the _[[coherence theorem for monoidal categories|MacLane coherence theorem]]_, guarantees that there is
no essential ambiguity re-backeting arbitrary iterations of the binary product topological space construction,
as long as the above homeomorphsims are understood.

Accordingly, we may write

$$
  (X_1, \tau_1)
    \times
  (X_2, \tau_2)
    \times
  \cdots
    \times
  (X_n, \tau_n)
$$

for iterated [[product topological spaces]] without putting parenthesis.


=--

$\,$


The following are a sequence of examples all of the form that an abstractly
constructed topological space is homeomorphic to a certain subspace of a Euclidean space.
These examples are going to be useful in further developments below, for example
in the [proof below](#BorelHeineProof) of the [[Heine-Borel theorem]] (prop. \ref{BorelHeine}).

* _[[product topological space|Products]] of [[intervals]] are homeomorphic to [[cube|hypercubes]]_ (example \ref{ClosedIntervalsProduct}).

* _The [[closed interval]] glued at its endpoints is homeomorphic to the [[circle]]_ (example \ref{HomeomorphismBetweenTopologicalAndCombinatorialCircle}).

* _The [[cylinder]], the [[Möbius strip]] and the [[torus]] are all homeomorphic to [[quotient spaces|quotients]] of the square_ (example \ref{SquareToCyclinderTorusAndMoebius}).



+-- {: .num_example #ClosedIntervalsProduct}
###### Example
**(product of closed intervals homeomorphic to hypercubes)**

Let $n \in \mathbb{N}$, and let $[a_i, b_i] \subset \mathbb{R}$ for $i \in \{1, \cdots, n\}$
be $n$ [[closed intervals]] in the [[real line]] (example \ref{OpenAndClosedIntervals}), regarded as [[topological subspaces]] of the
1-dimensional [[Euclidean space]] (example \ref{EuclideanNorm}) with its [[metric topology]]
(example \ref{MetricTopology}). Then the [[product topological space]]
(def. \ref{BinaryProductTopologicalSpace}, example \ref{CartesianSymmetricMonoidalTop})
of all these intervals is [[homeomorphism|homeomorphic]] (def. \ref{Homeomorphism})
to the corresponding [[topological subspace]] of the $n$-dimensional [[Euclidean space]] (example \ref{EuclideanNorm}):

$$
  [a_1, b_1] \times [a_2, b_2] \times \cdots \times [a_n, b_n]
   \;\simeq\;
  \left\{
    \vec x \in \mathbb{R}^n
    \,\vert\,
    \underset{i}{\forall}
      (a_i \leq x_i \leq b_i)
  \right\}
    \subset
  \mathbb{R}^n
  \,.
$$

=--

+-- {: .proof}
###### Proof

There is a canonical [[bijection]] between the underlying sets.
It remains to see that this, as well and its inverse, are [[continuous functions]].
For this it is sufficient to see that under this bijection the defining [[basis of a topology|basis]] (def. \ref{TopologyBase})
for the [[product topological space|product topology]] is also a basis for the [[topological subspace|subspace topology]].
But this is immediate from lemma \ref{RecognizingTopologicalBasis}.

=--


+-- {: .num_example #HomeomorphismBetweenTopologicalAndCombinatorialCircle}
###### Example
**(closed interval glued at endpoints homeomorphic circle)**

As topological spaces, the [[closed interval]] $[0,1]$ (def. \ref{OpenAndClosedIntervals}) with its two endpoints identified is [[homeomorphic]] (def. \ref{Homeomorphism}) to the standard [[circle]]:

$$
  [0,1]_{/(0 \sim 1)} \;\; \simeq \;\; S^1
  \,.
$$

More in detail: let

$$
  S^1 \hookrightarrow \mathbb{R}^2
$$

be the unit [[circle]] in the [[plane]]

$$
  S^1 = \{(x,y) \in \mathbb{R}^2, x^2 + y^2 = 1\}
$$

equipped with the [[subspace topology]] (example \ref{SubspaceTopology}) of the plane $\mathbb{R}^2$,
which is itself equipped with its standard [[metric topology]] (example \ref{MetricTopology}).

Moreover, let

$$
  [0,1]_{/(0 \sim 1)}
$$

be the [[quotient topological space]] (example \ref{QuotientTopologicalSpace}) obtained from the [[interval]] $[0,1] \subset \mathbb{R}^1$ with its [[subspace topology]] by applying the [[equivalence relation]] which identifies the two endpoints (and nothing else).

Consider then the function

$$
  f \;\colon\; [0,1] \longrightarrow S^1
$$

given by

$$
  t \mapsto (cos(t), sin(t))
  \,.
$$

This has the property that $f(0) = f(1)$, so that it descends to the [[quotient topological space]]

$$
  \array{
    [0,1] &\overset{}{\longrightarrow}& [0,1]_{/(0 \sim 1)}
    \\
    & {}_{\mathllap{f}}\searrow & \downarrow^{\mathrlap{\tilde f}}
    \\
    && S^1
  }
  \,.
$$

We claim that $\tilde f$ is a [[homeomorphism]] (definition \ref{Homeomorphism}).

First of all it is immediate that $\tilde f$ is a [[continuous function]]. This follows immediately from the fact that $f$ is a [[continuous function]] and by definition of the [[quotient topology]] (example \ref{QuotientTopologicalSpace}).

So we need to check that $\tilde f$ has a continuous inverse function. Clearly the restriction of $f$ itself to the open interval $(0,1)$ has a continuous inverse. It fails to have a continuous inverse on $[0,1)$ and on $(0,1]$ and fails to have an inverse at all on [0,1], due to the fact that $f(0) = f(1)$. But the relation quotiented out in $[0,1]_{/(0 \sim 1)}$ is exactly such as to fix this failure.

=--

+-- {: .num_defn #SquareToCyclinderTorusAndMoebius}
###### Example
**(cylinder, M&#246;bius strip and torus homeomorphic to quotients of the square)**

The [[square]] $[0,1]^2$ with two of its sides identified is the [[cylinder]], and with also the other two sides
identified is the [[torus]]:

<img src="https://ncatlab.org/nlab/files/TorusAsQuotientOfSquare.png" width="500">

If the sides are identified with opposite orientation, the result is the _[[Möbius strip]]_:

<img src="https://ncatlab.org/nlab/files/MoebiusStripAsQuotientOfSquare.png" width="400">

> graphics grabbed from [Lawson 03](#Lawson03)

=--

$\,$

Important examples of pairs of spaces that are _not_ homeomorphic include the following:


+-- {: .num_theorem #TopologicalInvarianceOfDimension}
###### Theorem
**([[topological invariance of dimension]])**

For $n_1, n_2 \in \mathbb{N}$ but $n_1 \neq n_2$, then the
 [[Euclidean spaces]] $\mathbb{R}^{n_1}$ and $\mathbb{R}^{n_2}$ (example \ref{EuclideanNorm}, example \ref{MetricTopology})
 are _not_ [[homeomorphic]].

More generally, an [[open subset]] in $\mathbb{R}^{n_1}$ is never homeomorphic to an open subset in $\mathbb{R}^{n_2}$ if $n_1 \neq n_2$.

=--

The proofs of theorem \ref{TopologicalInvarianceOfDimension} are not elementary, in contrast to how obvious the statement seems to be intuitively.
One approach is to use tools from _[[algebraic topology]]_:
One assigns [[topological invariants]] to topological spaces, notably classes in [[ordinary cohomology]]  or in [[topological K-theory]]),
quantities that are [[invariant]] under [[homeomorphism]],
and then shows that these classes coincide for $\mathbb{R}^{n_1} - \{0\}$ and for $\mathbb{R}^{n_2} - \{0\}$ precisely only
if $n_1 = n_2$.

One indication that [[topological invariance of dimension]] is not an _elementary_ consequence of the axioms of topological spaces
is that a related "intuitively obvious" statement is in fact false: One might think that there is no
_[[surjective function|surjective]]_ [[continuous function]] $\mathbb{R}^{n_1} \to  \mathbb{R}^{n_2}$ if $n_1 \lt n_2$.
But there are: these are called the _[[Peano curves]]_.



$\,$



## Separation axioms
 {#SeparationAxioms}

The plain definition of _[[topological space]]_ ([above](#TopologicalSpaces)) happens to admit examples where distinct points or distinct subsets of the underlying set appear as more-or-less unseparable as seen by the topology on that set.

The extreme class of examples of topological spaces in which the open subsets do not distinguish
distinct underlying points, or in fact any distinct subsets, are the [[codiscrete spaces]] (example \ref{CoDiscreteTopology}).
This does occur in practice:

+-- {: .num_example #RQuotientedByQ}
###### Example
**([[real numbers]] quotiented by [[rational numbers]])**

Consider the [[real line]] $\mathbb{R}$ regarded
as the 1-dimensional [[Euclidean space]] (example \ref{EuclideanNorm}) with its [[metric topology]] (example \ref{MetricTopology})
and consider the [[equivalence relation]] $\sim$ on $\mathbb{R}$ which identifies two [[real numbers]] if they
differ by a [[rational number]]:

$$
  \left(
    x \sim y
  \right)
    \;\Leftrightarrow\;
  \left(
    \underset{p/q \in \mathbb{Q} \subset \mathbb{R}}{\exists}
    \left(
      x = y + p/q
    \right)
  \right)
  \,.
$$

Then the [[quotient topological space]] (def. \ref{QuotientTopologicalSpace})

$$
  \mathbb{R}/\mathbb{Q}
    \;\coloneqq\;
  \mathbb{R}/\sim
$$

is a [[codiscrete topological space]] (def. \ref{CoDiscreteTopology}),
hence its topology does not distinguish any distinct proper subsets.

=--

Here are some less extreme examples:

+-- {: .num_example #SierpinskiNonSeparated}
###### Example
**(open neighbourhoods in the Sierpinski space)**

Consider the [[Sierpinski space]] from example \ref{SierpinskiSpace}, whose underlying set consists of
two points $\{0,1\}$, and whose open subsets form the set $\tau = \{ \emptyset, \{1\}, \{0,1\} \}$.
This means that the only (open) neighbourhood of the point $\{0\}$ is the entire space.
Incidentally, also the [[topological closure]] of $\{0\}$  (def. \ref{ClosedSubset}) is the entire space.
=--

+-- {: .num_example #LineWithTwoOrigins}
###### Example
**([[line with two origins]])**

Consider the [[disjoint union space]] $\mathbb{R} \sqcup \mathbb{R}$ (example \ref{DisjointUnionOfTopologicalSpaces}) of two copies of the [[real line]] $\mathbb{R}$ regarded as the 1-dimensional [[Euclidean space]] (example \ref{EuclideanNorm}) with its [[metric topology]] (example \ref{MetricTopology}), which is equivalently the [[product topological space]] (example \ref{BinaryProductTopologicalSpace})
of $\mathbb{R}$ with the [[discrete topological space]] on the 2-element set (example \ref{CoDiscreteTopology}):

$$
  \mathbb{R} \sqcup \mathbb{R} \;\simeq\; \mathbb{R} \times Disc(\{0,1\})
$$

Moreover, consider the [[equivalence relation]] on the underlying set which identifies every
point $x_i$ in the $i$th copy of $\mathbb{R}$ with the corresponding point in the other, the $(1-i)$th copy, except when $x = 0$:

$$
  \left(
    x_i \sim y_j
  \right)
   \;\Leftrightarrow\;
  \left(
    \left(
      x = y
    \right)
    \,\text{and}\,
    \left(
      \left(
        x \neq 0
      \right)
      \,\text{or}\,
      \left(
        i = j
      \right)
    \right)
  \right)
  \,.
$$

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/LineWithTwoOrigins.png" width="300">
</div>

The [[quotient topological space]] by this equivalence relation (def. \ref{QuotientTopologicalSpace})

$$
  \left(
    \mathbb{R} \sqcup \mathbb{R}
  \right)/\sim
$$

is called the **line with two origins**. These "two origins" are the points $0_0$ and $0_1$.

We claim that in this space _every neighbourhood of $0_0$ intersects every neighbouhood of $0_1$.

Because, by definition of the [[quotient topological space|quotient space topology]], the [[open neighbourhoods]] of $0_i \in   \left( \mathbb{R} \sqcup \mathbb{R} \right)/\sim$ are precisely those that contain subsets of the form

$$
 (-\epsilon, \epsilon)_i
  \;\coloneqq\;
 (-\epsilon,0) \cup \{0_i\} \cup (0,\epsilon)
 \,.
$$

But this means that the "two origins" $0_0$ and $0_1$ may not be [separated by neighbourhoods](separation+axioms#SeparatedByNeighbourhoods), since the intersection of
$(-\epsilon, \epsilon)_0$ with $(-\epsilon, \epsilon)_i$ is always non-empty:

$$
  (-\epsilon, \epsilon)_0
   \cap
  (-\epsilon, \epsilon)_1
  \;=\;
  (-\epsilon, 0) \cup (0, \epsilon)
  \,.
$$

=--


In many applications one wants to exclude at least some such exotic examples
of topologial spaces from the discussion and instead concentrate on those examples for which
the topology recognizes the separation of distinct points, or of more general
[[disjoint subsets]].
The relevant conditions to be imposed on top of the plain [[axioms]] of a [[topological space]] are hence known as _[[separation axioms]]_
which we discuss in the following.

These axioms are all of the form of saying that two subsets (of certain kinds) in the topological space are 'separated' from each other in one sense if they are 'separated' in a (generally) weaker sense. For example the weakest axiom (called $T_0$) demands that if two points are distinct as elements of the underlying set of points, then there exists at least one [[open subset]] that contains one but not the other.

In this fashion one may impose a hierarchy of stronger axioms. For example demanding that given two distinct points, then each of them is contained in some open subset not containing the other ($T_1$) or that such a pair of open subsets around two distinct points may in addition be chosen to be [[disjoint subsets|disjoint]] ($T_2$). Below in _[Tn-spaces](TnTopologicalSpaces)_ we discuss the following hierarchy:

{#TableOfMainSeparationAxioms}
[[!include main separation axioms -- table]]

The condition, $T_2$, also called the _[[Hausdorff topological space|Hausdorff condition]]_ is the most common among all separation axioms. Historically this axiom was originally taken as part of the definition of topological spaces,
and it is still often (but by no means always) considered by default.

However, there are respectable areas of mathematics that involve topological spaces where the Hausdorff axiom fails, but
a weaker axiom is still satisfied, called [[sober topological spaces|soberity]].
This is the case notably in [[algebraic geometry]] ([[schemes are sober]]) and in [[computer science]] ([Vickers 89](#Vickers89)).
These _[[sober topological spaces]]_ are singled out by the fact that they are entirely characterized by their
[[frame of opens|sets of open subsets]] with their union and intersection structure (as in def. \ref{HomomorphismOfFramesOfOpens})
and may hence be understood independently from their underlying sets of points. This we discuss [further below](#SoberSpaces).

| hierarchy of [[separation axioms]]                 |
|---------------------------------------|
| $\array{ &&&\text{metric space}  \\ &&& \Downarrow \\ &&& \vdots \\ &&& \Downarrow \\ &&& T_4  = \text{normal Hausdorff} \\ &&& \Downarrow \\ &&& T_3 = \text{regular Hausdorff} \\ &&& \Downarrow \\ &&& T_2 = \text{Hausdorff}  \\ && \swArrow && \seArrow \\ \, & T_1 && && \text{sober} & \, \\ && \seArrow && \swArrow \\ &&& T_0 = \text{Kolmogorov} \\ }  $ |

All separation axioms are satisfied by [[metric spaces]] (example \ref{HausdorffMetricSpace}, example \ref{MetricSpacesAreNormal} below), from whom the concept of topological space was originally abstracted [above](#TopologicalSpaces). Hence imposing some of them may also be understood as gauging just how far one allows topological spaces to generalize away from metric spaces




### $T_n$ spaces
 {#TnTopologicalSpaces}

There are many variants of separation axims. The classical ones are labeled $T_n$
(for German "Trennungsaxiom") with $n \in \{0,1,2,3,4,5\}$ or higher. These we now introduce in def. \ref{HausdorffTopologicalSpace} and def. \ref{NormalSpace}.

+-- {: .num_defn #HausdorffTopologicalSpace}
###### Definition
**(the first three [[separation axioms]])**

Let $(X,\tau)$ be a [[topological space]] (def. \ref{TopologicalSpace}).

For $x \neq y \in X$ any two points in the underlying set of $X$ which are not [[equality|equal]] as elements of this set,
consider the following [[propositions]]:

<div style="float:left;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/HausdorffProperty.png" width="190">
</div>


* **(T0)** *There exists a [[neighbourhood]] of one of the two points which does not contain the other point.*

* **(T1)** *There exist [[neighbourhoods]] of both points which do not contain the other point.*

* **(T2)** *There exists [[neighbourhoods]]_ of both points which do not intersect each other.*

> graphics grabbed from [Vickers 89](#Vickers89)

The topological space $X$ is called a _$T_n$-topological space_ or just _$T_n$-space_, for short,
if it satisfies condition $T_n$ above for all pairs of distinct points.

A $T_0$-topological space is also called a _[[Kolmogorov space]]_.

A $T_2$-topological space is also called a _[[Hausdorff topological space]]_.

For definiteness, we re-state these conditions formally. Write $x,y \in X$ for points in $X$, write $U_x, U_y \in \tau$ for open [[neighbourhoods]] of these points. Then:

* **(T0**) $\underset{x \neq y}{\forall} \left(
    \left( \underset{U_y}{\exists} \left( \{x\} \cap U_y = \emptyset \right) \right)
      \,\text{or}\,
    \left( \underset{U_x}{\exists} \left( U_x \cap \{y\} = \emptyset  \right) \right) \right)$

* **((T1)** $\underset{x \neq y}{\forall} \left(\underset{U_x,U_y}{\exists} \left(\left( \{x\} \cap U_y = \emptyset\right)
  \, \text{and} \, \left( U_x \cap \{y\}  = \emptyset \right)\right) \right)$

* **(T2)** $\underset{x \neq y}{\forall} \left( \underset{U_x, U_y}{\exists} \left( U_x \cap U_y = \emptyset\right) \right)$

=--

The following is evident but important:

+-- {: .num_prop #TnImplications}
###### Proposition
**($T_n$ are [[topological properties]] of increasing strength)**

The separation properties $T_n$ from def. \ref{HausdorffTopologicalSpace} are
_[[topological properties]]_ in that if two topological spaces
are [[homeomorphism|homeomorphic]] (def. \ref{Homeomorphism}) then
one of them satisfies $T_n$ precisely if the other does.

Moreover, these properties imply each other as

$$
  T2 \Rightarrow T1 \Rightarrow T0
  \,.
$$


=--


+-- {: .num_example #TnCounter}
###### Example

Examples of topological spaces that are _not_ [[Hausdorff topological spaces|Hausdorff]] (def. \ref{HausdorffTopologicalSpace})
include

1. the [[Sierpinski space]] (example \ref{SierpinskiNonSeparated}),

1. the [[line with two origins]] (example \ref{LineWithTwoOrigins}),

1. the [[quotient topological space]] $\mathbb{R}/\mathbb{Q}$ (example \ref{RQuotientedByQ}).


=--

+-- {: .num_example #FiniteT1SpacesAreDiscrete}
###### Example
**(finite $T_1$-spaces are discrete)**

For a [[finite topological space]] $(X,\tau)$, hence one for which the underlying set $X$ is a [[finite set]],
the following are equivalent:

1. $(X,\tau)$ is $T_1$ (def. \ref{HausdorffTopologicalSpace});

1. $(X,\tau)$ is a [[discrete topological space]] (def. \ref{CoDiscreteTopology}).

=--

+-- {: .num_example #HausdorffMetricSpace}
###### Example
**([[metric spaces]] are [[Hausdorff topological space|Hausdorff]])**

Every [[metric space]] (def \ref{MetricSpace}), regarded as a [[topological space]] via its [[metric topology]] (example \ref{MetricTopology})
is a [[Hausdorff topological space]] (def. \ref{HausdorffTopologicalSpace}).

Because for $x \neq y \in X$ two distinct points, then the [[distance]] $d(x,y)$ between them is [[positive number]],
by the non-degeneracy axiom in def. \ref{MetricSpace}. Accordingly the [[open balls]] (def. \ref{OpenBalls})

$$
  B^\circ_x(d(x,y)) \supset \{x\}
  \phantom{AA}
  \text{and}
  \phantom{AA}
  B^\circ_y(d(x,y)) \supset \{y\}
$$

are disjoint open neighbourhoods.


=--



+-- {: .num_example #TiSubspaces}
###### Example
**(subspace of $T_n$-space is $T_n$)**

Let $(X,\tau)$ be a [[topological space]] satisfying the $T_n$ [[separation axiom]] for some $n \in \{0,1,2\}$ according to
def. \ref{HausdorffTopologicalSpace}. Then also every [[topological subspace]] $S \subset X$ (example \ref{SubspaceTopology}) satisfies $T_n$.

=--




$\,$

**Separation in terms of topological closures**

The conditions $T_0$, $T_1$ and $T_2$ have the following equivalent formulation in terms of [[topological closures]] (def. \ref{ClosedSubset}).


+-- {: .num_prop #T0InTermsOfClosureOfPoints}
###### Proposition
**($T_0$ in terms of topological closures)**

A [[topological space]] $(X,\tau)$ is $T_0$ (def. \ref{HausdorffTopologicalSpace})
precisely if the function $Cl(\{-\})$ that forms [[topological closures]] (def. \ref{ClosedSubset}) of [[singleton]] [[subsets]]
from the underlying set of $X$ to the set of [[irreducible closed subsets]] of $X$ (def. \ref{ClosedIrreducible},
which is well defined according to example \ref{IrreducibleClosureOfPoint}), is [[injective function|injective]]:

$$
  Cl(\{-\}) \;\colon\; X \overset{\phantom{AAA}}{\hookrightarrow} IrrClSub(X)
$$


=--

+-- {: .proof}
###### Proof

Assume first that $X$ is $T_0$. Then we need to show that if $x,y \in X$ are such that
$Cl(\{x\}) = Cl(\{y\})$ then $x = y$. Hence assume that $Cl(\{x\}) = Cl(\{y\})$.
Since the closure of a point is the [[complement]] of the union of the open subsets not containing the point
(lemma \ref{UnionOfOpensGivesClosure}),
this means that the union of open subsets that do not contain $x$
is the same as the union of open subsets that do not contain $y$:

$$
  \underset{ {U \subset X \, \text{open}} \atop { U \subset X\backslash \{x\} } }{\cup} \left( U \right)
  \;=\;
  \underset{ {U \subset X \, \text{open}} \atop { U \subset X\backslash \{y\} } }{\cup} \left( U \right)
$$

But if the two points were distinct, $x \neq y$, then by $T_0$ one of the above unions would contain $x$ or $y$, while the other would not, in contradiction to the above equality. Hence we have a [[proof by contradiction]].

Conversely, assume that $\left( Cl\{x\} = Cl\{y\}\right) \Rightarrow \left( x = y\right)$, and assume that $x \neq y$.
Hence by [[contraposition]] $\mathrm{Cl}(\{x\}) \neq \mathrm{Cl}(\{y\})$. We need to show that there exists
an open set which contains one of the two points, but not the other.

Assume there were no such open subset, hence that every open subset containing one of the two points would
also contain then other. Then by lemma \ref{UnionOfOpensGivesClosure} this would mean
that $x \in \mathrm{Cl}(\{y\})$ and that $y \in \mathrm{Cl}(\{x\})$. But this would imply that
$Cl(\{x\}) \subset \mathrm{Cl}(\{y\})$ and that $\mathrm{Cl}(\{y\}) \subset \mathrm{Cl}(\{x\})$,
hence that $\mathrm{Cl}(\{x\}) = \mathrm{Cl}(\{y\})$. This is a [[proof by contradiction]].

=--

+-- {: .num_prop #T1InTermsOfTopologicalClosure}
###### Proposition
**($T_1$ in terms of topological closures)**

A [[topological space]] $(X,\tau)$ is $T_1$ (def. \ref{HausdorffTopologicalSpace}) precisely if
all its points are [[closed points]] (def. \ref{ClosedSubset}).

=--

+-- {: .proof}
###### Proof

We have

$$
  \begin{aligned}
    \text{all points in}\, (X, \tau)\, \text{are closed}
    &\coloneqq\,
    \underset{x \in X}{\forall}
    \left(
        Cl(\{x\}) = \{x\}
    \right)
    \\
    & \Leftrightarrow\,
      X \backslash
      \left(
      \underset{ { U \subset X\, \text{open} } \atop { x \notin U }  }{\cup} \left( U \right)
      \right)
       \;=\;
      \{x\}
    \\
    & \Leftrightarrow\,
      \left(
      \underset{ { U \subset X\, \text{open} } \atop { x \notin U }  }{\cup} \left( U \right)
      \right)
       \;=\;
      X \backslash \{x\}
    \\
    & \Leftrightarrow
    \underset{y \in Y}{\forall}
    \left(
      \left(
        \underset{  { U \subset X \, \text{open} } \atop { x \notin U }  }{\exists}
        \left(
          y \in U
        \right)
      \right)
      \Leftrightarrow
      (y \neq x)
    \right)
    \\
    & \Leftrightarrow\,
    (X,\tau)\, \text{is}\, T_1
  \end{aligned}
  \,.
$$

Here the first step is the reformulation of closure from lemma \ref{UnionOfOpensGivesClosure}, the second is another application of the [[de Morgan law]] (remark \ref{deMorgan}), the third is the definition of union and complement, and the last one is manifestly
by definition of $T_1$.

=--

+-- {: .num_prop #T2InTermsOfClosedDiagonal}
###### Proposition
**($T_2$ in terms of topological closures)**

A [[topological space]] $(X,\tau_X)$ is $T_2$=[[Hausdorff topological space|Hausdorff]]
precisely if the [[image]] of the [[diagonal]]

$$
  \array{
     X &\overset{\Delta_X}{\longrightarrow}& X \times X
     \\
     x &\overset{\phantom{AAA}}{\mapsto}& (x,x)
  }
$$

is a [[closed subset]] in the [[product topological space]]
$(X \times X, \tau_{X \times X})$.

=--

+-- {: .proof}
###### Proof

Observe that the Hausdorff condition is equivalently rephrased in terms of the product topology as: _Every point $(x,y) \in X$ which is not on the diagonal has an open neighbourhood $U_{(x,y)} \times U_{(x,y)}$ which still does not intersect the diagonal_, hence:

$$
  \begin{aligned}
    & (X,\tau)\,\text{Hausdorff}
    \\
    \Leftrightarrow
    &
  \underset{(x,y) \in (X \times X) \backslash \Delta_X(X) }{\forall}
  \left(
      \underset{ { U_{(x,y)} \times V_{(x,y)} \in \tau_{X \times Y} } \atop { (x,y) \in U_{(x,y)} \times V_{(x,y)} } }{\exists}
      \left(
           U_{(x,y)} \times V_{(x,y)} \cap \Delta_X(X) = \emptyset
      \right)
  \right)
  \end{aligned}
$$

Therefore if $X$ is Hausdorff, then the diagonal $\Delta_X(X) \subset X \times X$ is the complement of a union of such open sets, and hence is closed:


$$
  (X, \tau)\, \text{Hausdorff}
  \;\;\;\Rightarrow \;\;\;
  \Delta_X(X)
  =
  X \backslash
  \left(
    \underset{(x,y) \in (X \times X) \backslash \Delta_X(X)}{\cup}
    U_{(x,y)} \times V_{(x,y)}
  \right)
  \,.
$$

Conversely, if the diagonal is closed, then (by lemma \ref{UnionOfOpensGivesClosure}) every point $(x,y) \in X \times X$ not on the diagonal, hence with $x \neq y$, has an open neighbourhood $U_{(x,y)} \times V_{(x,y)}$ still not intersecting the diagonal, hence so that $U_{(x,y)} \cap V_{(x,y)} = \emptyset$. Thus $(X,\tau)$ is Hausdorff.

=--


$\,$

**Further separation axioms**

Clearly one may and does consider further variants of the
separation axioms $T_0$, $T_1$ and $T_2$ from def. \ref{HausdorffTopologicalSpace}.
Here we discuss two more:


+-- {: .num_defn #NormalSpace}
###### Definition

Let $(X,\tau)$ be [[topological space]] (def. \ref{HausdorffTopologicalSpace}).

Consider the following conditions

* **(T3)** The space $(X,\tau)$ is $T_1$ (def. \ref{HausdorffTopologicalSpace}) and for $x \in X$ a point and $C \subset X$ a [[closed subset]] (def. \ref{ClosedSubset}) not containing $x$, then there exist [[disjoint subsets|disjoint]] [[open neighbourhoods]] $U_x \supset \{x\}$ and $U_C \supset C$.

* **(T4)** The space $(X,\tau)$ is $T_1$ (def. \ref{HausdorffTopologicalSpace}) and for $C_1, C_2 \subset X$ two disjoint [[closed subsets]] (def. \ref{ClosedSubset}) then there exist [[disjoint subsets|disjoint]] [[open neighbourhoods]] $U_{C_i} \supset C_i$.

If $(X,\tau)$ satisfies $T_3$ it is said to be a _$T_3$-space_ also called a _[[regular Hausdorff topological space]]_.

If $(X,\tau)$ satisfies $T_4$ it is to be a _$T_4$-space_ also called a _[[normal Hausdorff topological space]]_.

=--

+-- {: .num_example #MetricSpacesAreNormal}
###### Example
**([[metric spaces]] are [[normal Hausdorff space|normal Hausdorff]])**

Let $(X,d)$ be a [[metric space]] (def. \ref{MetricSpace}) regarded as a [[topological space]]
via its [[metric topology]] (example \ref{MetricTopology}). Then this is a [[normal Hausdorff space]] (def. \ref{NormalSpace}).

=--

+-- {: .proof}
###### Proof

By example \ref{HausdorffMetricSpace} metric spaces are $T_2$, hence in particular $T_1$.
What we need to show is that given two [[disjoint subsets|disjoint]] [[closed subsets]] $C_1, C_2 \subset X$
then their exists [[disjoint subset|disjoint]] [[open neighbourhoods]] $U_{C_1} \subset C_1$
and $U_{C_2} \supset C_2$.

Recall the function

$$
  d(S,-) \colon X \to \mathbb{R}
$$


computing distances from a subset $S \subset X$ (example \ref{DistanceFunctionFromsubset}). Then the
[[unions]] of [[open balls]] (def. \ref{OpenBalls})

$$
  U_{C_1}
    \coloneqq
  \underset{x_1 \in C_1}{\cup} B^\circ_{x_1}( d(C_2,x_1)/2 )
$$

and

$$
  U_{C_2}
    \coloneqq
  \underset{x_2 \in C_2}{\cup} B^\circ_{x_2}( d(C_1,x_2)/2 )
  \,.
$$

have the required properties.

=--




Observe that:

+-- {: .num_prop #ImplicationsAmongTheSeparationAxioms}
###### Proposition
**($T_n$ are topological properties of increasing strength)**

The separation axioms from def. \ref{HausdorffTopologicalSpace}, def. \ref{NormalSpace}
are [[topological properties]] (def. \ref{Homeomorphism}) which imply each other as

$$
  T_4 \Rightarrow T_3 \Rightarrow T_2 \Rightarrow T_1 \Rightarrow T_0
  \,.
$$

=--

+-- {: .proof}
###### Proof

The implications

$$
  T_2 \Rightarrow T_1 \Rightarrow T_0
$$

and

$$
  T_4 \Rightarrow T_3
$$

are immediate from the definitions. The remaining implication $T_3 \Rightarrow T_2$
follows with prop. \ref{T1InTermsOfTopologicalClosure}: This says that by assumption of $T_1$
then all points in $(X,\tau)$ are closed, and with this the condition $T_2$ is manifestly
a special case of the condition for $T_3$.

=--

Hence instead of saying "$X$ is $T_1$ and ..." one could just as well phrase
the conditions $T_3$ and $T_4$ as "$X$ is $T_2$ and ...", which would render
the proof of prop. \ref{ImplicationsAmongTheSeparationAxioms} even more trivial.

The following shows that not every $T_2$-space/Hausdorff space is $T_3$/regular

+-- {: .num_example #KTopology}
###### Example
**(K-topology)**

Write

$$
  K \coloneqq \{1/n \,\vert\, n \in \mathbb{N}_{\geq 1}\} \subset \mathbb{R}
$$

for the [[subset]] of [[natural number|natural]] [[fractions]] inside the [[real numbers]].

Define a [[topological basis]] $\beta \subset P(\mathbb{R})$ on $\mathbb{R}$ consisting of all the [[open intervals]] as well as the [[complements]] of $K$ inside them:

$$
  \beta
    \;\coloneqq\;
  \left\{
    (a,b),
    \,\vert\,
    a\lt b \in \mathbb{R}
  \right\}
   \,\cup\,
  \left\{
    (a,b) \backslash K,
    \,\vert\,
    a\lt b \in \mathbb{R}
  \right\}
  \,.
$$

The [[topological space|topology]] $\tau_{\beta} \subset P(\mathbb{R})$ which is generated from this [[topological basis]] is called the _K-topology_.

We may denote the resulting [[topological space]] by

$$
  \mathbb{R}_K
   \;\coloneqq\;
  ( \mathbb{R}, \tau_{\beta}\}
  \,.
$$

This is a [[Hausdorff topological space]] (def. \ref{HausdorffTopologicalSpace}) which is not a [[regular Hausdorff space]],
hence (by prop. \ref{ImplicationsAmongTheSeparationAxioms}) in particular not a [[normal Hausdorff space]] (def. \ref{NormalSpace}).

=--




$\,$


**Further separation axioms in terms of topological closures**

As before we have equivalent reformulations of the further separation axioms.


+-- {: .num_prop #T3InTermsOfTopologicalClosures}
###### Proposition
**($T_3$ in terms of topological closures)**

A [[topological space]] $(X,\tau)$ is a [[regular Hausdorff space]] (def. \ref{NormalSpace}), precisely if
all points are closed and for all points $x \in X$ with [[open neighbourhood]] $U \supset \{x\}$ there exists a smaller open neighbourhood $V \supset \{x\}$ whose [[topological closure]] $Cl(V)$ is still contained in $U$:

$$
  \{x\} \subset V \subset Cl(V) \subset U
  \,.
$$

=--

The **proof** of prop. \ref{T3InTermsOfTopologicalClosures} is the direct  specialization of the following proof for prop. \ref{T4InTermsOfTopologicalClosures} to the case that $C = \{x\}$ (using that by $T_1$, which is part of the definition of $T_3$, the singleton subset is indeed closed, by prop. \ref{T1InTermsOfTopologicalClosure}).


+-- {: .num_prop #T4InTermsOfTopologicalClosures}
###### Proposition
**($T_4$ in terms of topological closures)**

A [[topological space]] $(X,\tau)$ is [[normal Hausdorff space]] (def. \ref{NormalSpace}), precisely if all points are closed and for all [[closed subsets]] $C \subset X$ with [[open neighbourhood]] $U \supset C$ there exists a smaller open neighbourhood $V \supset C$ whose [[topological closure]] $Cl(V)$ is still contained in $U$:

$$
  C \subset V \subset Cl(V) \subset U
  \,.
$$

=--

+-- {: .proof}
###### Proof

In one direction, assume that $(X,\tau)$ is normal, and consider

$$
  C \subset U
  \,.
$$

It follows that the [[complement]] of the open subset $U$ is closed and disjoint from $C$:

$$
  C \cap X \backslash U = \emptyset
  \,.
$$

Therefore by assumption of normality of $(X,\tau)$, there exist open neighbourhoods  with

$$

  V \supset C
  \,, \phantom{AA}
  W \supset X \backslash U
  \phantom{AA}
    \text{with}
  \phantom{AA}
  V \cap W = \emptyset
  \,.
$$

But this means that

$$
  V \subset X \backslash W
$$

and since the [[complement]] $X \backslash W$ of the open set $W$ is closed, it still contains the closure of $V$, so that we have

$$
  C \subset V \subset Cl(V) \subset X \backslash W \subset U
$$

as required.

In the other direction, assume that for every open neighbourhood $U \supset C$ of a closed subset $C$ there exists a smaller open neighbourhood $V$ with

$$
  C \subset V \subset Cl(V) \subset U
  \,.
$$

Consider disjoint closed subsets

$$
  C_1, C_2 \subset X
  \,,
  \phantom{AAA}
  C_1 \cap C_2 = \emptyset
  \,.
$$

We need to produce disjoint open neighbourhoods for them.

From their disjointness it follows that

$$
  X \backslash C_2 \supset C_1
$$

is an open neighbourhood. Hence by assumption there is an open neighbourhood $V$ with

$$
  C_1 \subset V \subset Cl(V) \subset X \backslash C_2
  \,.
$$

Thus

$$
  V \supset C_1
    \,, \phantom{AAAA}
  X \backslash Cl(V) \supset C_2
$$

are two disjoint open neighbourhoods, as required.

=--

But the $T_4$/normality axiom has yet another equivalent reformulation, which is of a different nature,
and will be important when we discuss [[paracompact topological spaces]] [below](#ParacompactSpaces):

The following concept of _[[Urysohn functions]]_ is another approach of thinking about separation
of subsets in a topological space, not in terms of their neighbourhoods, but in terms of
continuous real-valued "indicator functions" that take different values on the subsets.
This perspective will be useful when we consider [[paracompact topological spaces]] [below](#ParacompactSpaces).

But the [[Urysohn lemma]] (prop. \ref{UrysohnLemma} below) implies that this concept of separation
is in fact equivalent to that of normality of Hausdorff spaces.

+-- {: .num_defn #UrysohnFunction}
###### Definition
**([[Urysohn function]])**

Let $(X,\tau)$ be a [[topological space]], and let $A,B \subset X$ be disjoint [[closed subsets]]. Then an _Urysohn function separating $A$ from $B$_  is

* a [[continuous function]] $f \colon X \to [0,1]$

to the [[closed interval]] equipped with its [[Euclidean space|Euclidean]] [[metric topology]] (example \ref{EuclideanNorm}, example \ref{MetricTopology}), such that

* it takes the value 0 on $A$ and the value 1 on $B$:

  $$
    f(A) = \{0\}
    \phantom{AAA}
    \text{and}
    \phantom{AAA}
    f(B) = \{1\}
    \,.
  $$

=--


+-- {: .num_prop #UrysohnLemma}
###### Proposition
**([[Urysohn's lemma]])**

Let $X$ be a [[normal Hausdorff topological space]] (def. \ref{NormalSpace}), and let $A,B \subset X$
be two [[disjoint subset|disjoint]] [[closed subsets]] of $X$. Then there exists an [[Urysohn function]] separating $A$ from $B$ (def. \ref{UrysohnFunction}).


=--

+-- {: .num_remark}
###### Remark

Beware that the Urysohn function in prop. \ref{UrysohnLemma} may take the values 0 or 1 even outside of the two subsets. The condition that the function takes value 0 or 1, respectively, _precisely_ on the two subsets corresponds to "[[perfectly normal spaces]]".

=--


+-- {: .proof}
###### Proof
of [[Urysohn's lemma]], prop. \ref{UrysohnLemma}

Set

$$
  C_0 \coloneqq A
  \phantom{AAA}
  U_1 \coloneqq X \backslash B
  \,.
$$

Since by assumption

$$
  A \cap B = \emptyset
  \,.
$$

we have

$$
  C_0 \subset U_1
  \,.

$$

That $(X,\tau)$ is normal implies, by lemma \ref{T4InTermsOfTopologicalClosures}, that every open neighbourhood $U \supset C$ of a closed subset $C$ contains a smaller neighbourhood $V$ together with its [[topological closure]] $Cl(V)$

$$
  U \subset V \subset Cl(V) \subset C
  \,.
$$

Apply this fact successively to the above situation to obtain the following infinite sequence of nested open subsets $U_r$ and closed subsets $C_r$

$$
  \array{
    C_0 &&  &&  &&  &\subset&  &&  &&  && U_1
    \\
    C_0 &&  &\subset&  && U_{1/2} &\subset& C_{1/2} &&  &\subset&  && U_1
    \\
    C_0 &\subset& U_{1/4} &\subset& C_{1/4} &\subset& U_{1/2} &\subset& C_{1/2} &\subset& U_{3/4} &\subset& C_{3/4} &\subset& U_1
  }
$$

and so on, labeled by the [[dyadic rational numbers]] $\mathbb{Q}_{dy} \subset \mathbb{Q}$ within $(0,1]$

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/UrysohnConstruction.png" width="400">
</div>


$$
 \{ U_{r} \subset X \}_{r \in (0,1] \cap \mathbb{Q}_{dy}}
$$

with the property

$$
  \underset{r_1 \lt r_2 \, \in (0,1] \cap \mathbb{Q}_{dy}}{\forall}
  \left(
      U_{r_1} \subset Cl(U_{r_1}) \subset U_{r_2}
  \right)
  \,.
$$

Define then the function

$$
  f \;\colon\; X \longrightarrow [0,1]
$$

to assign to a point $x \in X$ the [[infimum]] of the labels of those open subsets in this sequence that contain $x$:

$$
  f(x)
     \coloneqq
  \underset{U_r \supset \{x\}}{\lim} r
$$

Here the [[limit of a net|limit]] is over the [[directed set]] of those $U_r$ that contain $x$, ordered by reverse inclusion.


This function clearly has the property that $f(A) = \{0\}$  and $f(B) = \{1\}$. It only remains to see that it is continuous.

To this end, first observe that

$$
  \array{
    (\star)
    &&
    \left(
      x \in Cl(U_r)
    \right)
      &\Rightarrow&
    \left(
       f(x) \leq r
    \right)
    \\
    (\star\star)
    &&
    \left(
      x \in U_r
    \right)
      &\Leftarrow&
    \left(
      f(x) \lt r
    \right)
  }
  \,.
$$

Here it is immediate from the definition that $(x \in U_r) \Rightarrow (f(x) \leq r)$ and that $(f(x) \lt r) \Rightarrow (x \in U_r \subset Cl(U_r))$. For the remaining implication, it is sufficient to observe that

$$
  (x \in \partial U_r) \Rightarrow (f(x) = r)
  \,,
$$

where $\partial U_r \coloneqq Cl(U_r) \backslash U_r$ is the [[boundary]] of $U_r$.

This holds because the [[dyadic numbers]] are [[dense subset|dense]] in $\mathbb{R}$. (And this would fail if we stopped the above decomposition into $U_{a/2^n}$-s at some finite $n$.) Namely, in one direction, if $x \in \partial U_r$ then for every small positive real number $\epsilon$ there exists a dyadic rational number $r'$ with $r \lt r' \lt r + \epsilon$, and by construction $U_{r'} \supset Cl(U_r)$ hence  $x \in U_{r'}$. This implies that $\underset{U_r \supset \{x\}}{\lim} = r$.


{#PreimagesOfTheSubbaseOpens} Now we claim that for all $\alpha \in [0,1]$ then

1. $f^{-1}(\,(\alpha, 1]\,) = \underset{r \gt \alpha}{\cup} \left( X \backslash Cl(U_r) \right)$

1. $f^{-1}(\,[0,\alpha)\,) = \underset{r \lt \alpha}{\cup} U_r$

Thereby $f^{-1}(\,(\alpha, 1]\,)$ and $f^{-1}(\,[0,\alpha)\,)$ are exhibited as unions of open subsets, and hence they are open.


Regarding the first point:

$$
  \begin{aligned}
     & x \in f^{-1}( \,(\alpha,1]\, )
     \\
     \Leftrightarrow\,
     &
     f(x) \gt \alpha
     \\
     \Leftrightarrow\,
     &
     \underset{r \gt \alpha}{\exists} (f(x) \gt r)
     \\
     \overset{(\star)}{\Rightarrow}\,
     &
     \underset{r \gt \alpha}{\exists}
     \left( x \notin Cl(U_r) \right)
     \\
     \Leftrightarrow\,
     &
     x  \in \underset{r \gt \alpha}{\cup} \left(X \backslash Cl(U_r)\right)
  \end{aligned}
$$

and

$$
  \begin{aligned}
     & x  \in \underset{r \gt \alpha}{\cup} \left(X \backslash Cl(U_r)\right)
     \\
     \Leftrightarrow\,
     &
     \underset{r \gt \alpha}{\exists}
     \left( x \notin Cl(U_r) \right)
     \\
     \Rightarrow\,
     &
     \underset{r \gt \alpha}{\exists}
     \left( x \notin U_r \right)
     \\
     \overset{(\star \star)}{\Rightarrow}\,
     &
     \underset{r \gt \alpha}{\exists}
     \left(
       f(x) \geq r
     \right)
     \\
     \Leftrightarrow\,
     &
     f(x) \gt \alpha
     \\
     \Leftrightarrow\,
     &
     x \in f^{-1}(\, (\alpha,1] \,)
  \end{aligned}
  \,.
$$




Regarding the second point:

$$
  \begin{aligned}
    &
    x \in f^{-1}(\, [0,\alpha) \,)
    \\
    \Leftrightarrow\,
    &
    f(x) \lt \alpha
    \\
    \Leftrightarrow\,
    &
    \underset{r \lt \alpha}{\exists}( f(x) \lt r )
    \\
    \overset{(\star \star)}{\Rightarrow}\,
    &
    \underset{r \lt \alpha}{\exists }( x \in U_r )
    \\
    \Leftrightarrow\,
     &
    x \in \underset{r \lt \alpha}{\cup} U_r
  \end{aligned}
$$

and

$$
  \begin{aligned}
     &
    x \in \underset{r \lt \alpha}{\cup} U_r
    \\
    \Leftrightarrow\,
    &
    \underset{r \lt \alpha}{\exists }( x \in U_r )
    \\
    \overset{}{\Rightarrow}\,
    &
    \underset{r \lt \alpha}{\exists }( x \in Cl(U_r) )
    \\
    \overset{(\star)}{\Rightarrow}\,
     &
    \underset{r \lt \alpha}{\exists }( f(x) \leq r )
    \\
    \Leftrightarrow\,
     &
    f(x) \lt \alpha
    \\
    \Leftrightarrow\,
    &
    x \in f^{-1}(\, [0,\alpha) \,)
  \end{aligned}
 \,.
$$

(In these derivations we repeatedly use that $(0,1] \cap \mathbb{Q}_{dy}$ is [[dense subset|dense]] in $[0,1]$ (def. \ref{ClosedSubset}), and we use the [[contrapositions]] of $(\star)$ and $(\star \star)$.)


Now since the subsets $\{ [0,\alpha), (\alpha,1]\}_{\alpha \in [0,1]}$
form a [[topological subbase|sub-base]] (def. \ref{TopologyBase}) for the Euclidean metric topology on $[0,1]$, it follows that all pre-images of $f$ are open, hence that $f$ is continuous.

=--

As a corollary of [[Urysohn's lemma]] we obtain yet another equivalent reformulation of the normality of topological spaces,
this one now of a rather different character than the re-formulations in terms of explicit topological closures
considered above:

+-- {: .num_prop #NormalityEquivalentToUrysohnFunctionsExsist}
###### Proposition
**(normality equivalent to existence of Urysohn functions)**

A $T_1$-space (def. \ref{HausdorffTopologicalSpace}) is [[normal topological space|normal]] (def. \ref{NormalSpace}) precisely if it admits [[Urysohn functions]] (def \ref{UrysohnFunction}) separating every pair of
disjoint closed subsets.

=--

+-- {: .proof}
###### Proof

In one direction this is the statement of the [[Urysohn lemma]], prop. \ref{UrysohnLemma}.

In the other direction, assume the existence of [[Urysohn functions]] (def. \ref{UrysohnFunction})
separating all disjoint closed subsets. Let $A, B \subset X$ be disjoint closed subsets, then we need
to show that these have disjoint open neighbourhoods.

But let $f \colon X \to [0,1]$ be an Urysohn function with $f(A) = \{0\}$ and $f(B) = \{1\}$ then the [[pre-images]]

$$
  U_A \coloneqq f^{-1}([0,1/3)
  \phantom{AAA}
  U_B \coloneqq f^{-1}((2/3,1])
$$

are disjoint open neighbourhoods as required.

=--












$\,$

### $T_n$ reflection
 {#HausdorffReflections}

While the [[topological subspace]] construction preserves the $T_n$-property  for $n \in \{0,1,2\$
(exmaple \ref{TiSubspaces}) the construction of [[quotient topological spaces]] in general does not,
as shown by examples \ref{RQuotientedByQ} and \ref{LineWithTwoOrigins}.

Further [below](#UniversalConstructions) we will see that, generally, among all [[universal constructions]]
in the [[category]] [[Top]] of all  [[topological spaces]] those
that are [[limits]] preserve the $T_n$ property, while those that are [[colimits]] in general do not.

But at least for $T_0$, $T_1$ and $T_2$  there is a  universal way, called _[[reflective subcategory|reflection]]_ (prop. \ref{HausdorffReflection} below),
to approximate any topological space "from the left" by a $T_n$ topological spaces

Hence if one wishes to work within the [[full subcategory]] of the $T_n$-spaces
among all [[topological space]], then the correct way to construct quotients and other _[[colimits]]_
(see [below](#UniversalConstructions)) is to first construct them as usual [[quotient topological spaces]] (example \ref{QuotientTopologicalSpace}), and then apply the $T_n$-reflection to the result.


+-- {: .num_prop #HausdorffReflection}
###### Proposition
**($T_n$-reflection)**

Let $n \in \{0,1,2\}$. Then for every [[topological space]] $X$ there exists


1. a $T_n$-topological space $T_n X$

1. a [[continuous function]]

   $$
     t_n(X)
       \;\colon\;
     X \longrightarrow T_n X
   $$

   called the _$T_n$-reflection_ of $X$,

which is the  "closest approximation from the left" to $X$ by a $T_n$-topological space, in that
for $Y$ any $T_n$-space, then [[continuous functions]] of the form

$$
  f \;\colon\; X \longrightarrow Y
$$

are in [[bijection]] with [[continuous function]] of the form

$$
  \tilde f \;\colon\; T_n X \longrightarrow Y
$$

and such that the bijection is constituted by

$$
  f = \tilde f \circ t_n(X)
  \;\colon\;
    X
      \overset{ t_n(X)}{\longrightarrow}
    T_n X
      \overset{\tilde f}{\longrightarrow}
    Y
  \phantom{AAAA}i.e.: \phantom{AAA}
  \array{
    X && \overset{f}{\longrightarrow} && Y
    \\
    & {}_{\mathllap{t_n(X)}}\searrow && \nearrow_{\mathrlap{\tilde f}}
    \\
    && T_n X
  }
  \,.
$$


* For $n = 0$ this is known as the _[[Kolmogorov quotient]]_ construction (see prop. \ref{KolmogorovQuotient} below).

* For $n = 2$
this is known as _[[Hausdorff reflection]]_ or _Hausdorffication_ or similar.



Moreover, the operation $T_n(-)$ extends to [[continuous functions]] $f \colon X \to Y$

$$
  (X \overset{f}{\to} Y)
    \;\mapsto\;
  (T_n X \overset{T_n f}{\to} T_n Y)
$$

such as to preserve [[composition]] of functions as well as [[identity functions]]:

$$
  T_n g \circ T_n f = T_n(g \circ f)
  \phantom{AA}
  \,,
  \phantom{AA}
  T_n id_X = id_{T_n X}
  \,
$$

Finally, the comparison map is compatible with this in that

$$
  t_n(Y) \circ f
    =
  T_n(f) \circ t_n(X)
  \phantom{AAAA}
  i.e.:
  \phantom{AAAA}
  \array{
      X &\overset{f}{\longrightarrow}& Y
      \\
      {}^{\mathllap{t_n(X)}}\downarrow && \downarrow^{\mathrlap{t_n(Y)}}
      \\
      T_n X &\underset{T_n(f)}{\longrightarrow}& T_n Y
  }
  \,.
$$


=--

We **prove** this via a concrete construction of $T_n$-reflection in prop. \ref{HausdorffReflectionViaHomsIntoAllHausdorffSpaces} below.
But first we pause to comment on the bigger picture of the $T_n$-reflection:


+-- {: .num_remark #ReflectiveSubcategory}
###### Remark
**([[reflective subcategories]])**

In the language of [[category theory]] (remark \ref{TopCategory}) the $T_n$-reflection of prop. \ref{HausdorffReflection}
says that

1. $T_n(-)$ is a _[[functor]]_ $T_n \;\colon\; Top \longrightarrow Top_{T_n}$ from the [[category]] [[Top]] of [[topological spaces]] to the [[full subcategory]] $Top_{T_n} \overset{\iota}{\hookrightarrow} Top$ of Hausdorff topological spaces;

1. $t_n(X) \colon X \to T_n X$ is a _[[natural transformation]]_ from the [[identity functor]] on [[Top]] to the functor $\iota \circ T_n$

1. $T_n$-topological spaces form a [[reflective subcategory]] of all [[topological spaces]] in that $T_n$ is [[left adjoint]] to the inclusion functor $\iota$; this situation is denoted as follows:

   $$
     Top_{T_n}
       \underoverset{\underset{\phantom{A}\iota\phantom{A}}{\hookrightarrow}}{\overset{\phantom{A}H\phantom{A}}{\longleftarrow}}{\bot}
     Top
     \,.
   $$

Generally, an _[[adjoint functor|adjunction]]_ between two [[functors]]

$$
  L \;\colon\; \mathcal{C} \leftrightarrow \mathcal{D} \;\colon\; R
$$

is for all pairs of objects $c \in \mathcal{C}$, $d \in \mathcal{D}$ a [[bijection]] between sets of [[morphisms]] of the form

$$
  \left\{
     L(c) \longrightarrow d
  \right\}
  \phantom{A}
    \leftrightarrow
  \phantom{A}
  \left\{
    c \longrightarrow R(d)
  \right\}
  \,.
$$

i.e.

$$
  Hom_{\mathcal{D}}(L(c), d)
  \underoverset{\phantom{AA}\simeq \phantom{AA}}{\phi_{c,d}}{\longrightarrow}
  Hom_{\mathcal{C}}(c, R(d))
$$

and such that these bijections are "[[natural bijection|natural]]" in that they for all pairs of morphisms $f \colon c' \to c$ and $g \colon d \to d'$ then the folowing [[commuting diagram|diagram commutes]]:

$$
  \array{
    Hom_{\mathcal{D}}(L(c), d)
      &\underoverset{\phantom{AA}\simeq\phantom{AA}}{\phi_{c,d}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c, R(d))
    \\
    {\mathllap{g \circ (-) \circ L(f)}}\downarrow
       &&
    \downarrow{\mathrlap{ R(g) \circ (-) \circ f }}
    \\
    Hom_{\mathcal{C}}(L(c'), d')
     &\underoverset{\phantom{AA}\simeq\phantom{AA}}{\phi_{c',d'}}{\longrightarrow}&
    Hom_{\mathcal{D}}(c', R(d'))
  }
  \,.
$$

One calls the image under $\phi_{c,L(c)}$ of the [[identity morphism]] $id_{L(x)}$ the
_[[unit of an adjunction|unit of the adjunction]]_, written

$$
  \eta_x \;\colon\; c \longrightarrow R(L(c))
  \,.
$$

One may show that it follows that the image $\tilde under $\phi_{c,d}$ of a general morphism $f \colon c \to d$
(called the _[[adjunct]]_ of $f$) is given by this [[composition|composite]]:

$$
  \tilde f
    \;\colon\;
  c \overset{\eta_c}{\longrightarrow} R(L(c)) \overset{R(f)}{\longrightarrow} R(d)
  \,.
$$

In the case of the [[reflective subcategory]] inclusion $(T_n \dashv \iota)$ of the category of $T_n$-spaces into
the category [[Top]] of all topological spaces this adjunction unit is precisely the $T_n$-reflection
$t_n(X) \colon X \to \iota( T_n(X))$ (only that we originally left the re-embedding $\iota$ notationally implicit).

=--

$\,$

There are various ways to see the existence and to construct the $T_n$-reflections. The following is the quickest way to see the existence, even though it leaves the actual construction rather implicit.

+-- {: .num_prop #HausdorffReflectionViaHomsIntoAllHausdorffSpaces}
###### Proposition
**($T_n$-reflection via explicit quotients)**


Let $n \in \{0,1,2\}$. Let $(X,\tau)$ be a [[topological space]] and consider the [[equivalence relation]] $\sim$ on the underlying set $X$
for which $x_1 \sim x_2$ precisely if for every [[surjective function|surjective]] [[continuous function]] $f \colon X \to Y$ into any
$T_n$-topological space $Y$ (def. \ref{HausdorffTopologicalSpace}) we have $f(x_1) = f(x_2)$:

$$
  (x_1 \sim x_2)
    \;\coloneqq\;
  \underset{ { Y \in Top_{T_n} } \atop { X \underoverset{\text{surjective}}{f}{\to} Y  }  }{\forall}
  \left(
    f(x) = f(y)
  \right)
  \,.
$$

Then

1. the set of [[equivalence classes]]

   $$
     T_n X \coloneqq X /{\sim}
   $$

   equipped with the [[quotient topology]] (example \ref{QuotientTopologicalSpace}) is a $T_n$-topological space,

1. the quotient projection

   $$
     \array{
       X & \overset{t_n(X)}{\longrightarrow} &  X/{\sim}
       \\
       x &\overset{\phantom{AAA}}{\mapsto}& [x]
     }
   $$

   exhibits the $T_n$-reflection of $X$, according to prop. \ref{HausdorffReflection}.

=--

+-- {: .proof}
###### Proof

First we observe that every continuous function $f \colon X \longrightarrow Y$ into a $T_n$-topological space $Y$
factors uniquely, via $t_n(X)$ through a continuous function $\tilde f$
(this makes use of the "[[universal property]]" of the quotient topology, which we dwell on a bit more below in example \ref{UniversalPropertyOfQuotientSpace}):

$$
  f = \tilde f \circ t_n(X)
$$

Clearly this continuous function $\tilde f$ is unique if it exists, because its underlying function of sets
must be given by

$$
  \tilde f \colon [x] \mapsto f(x)
  \,.
$$

First observe that this is indeed well defined as a function of underlying sets.
To that end, factor $f$ through its [[image]] $f(X)$

$$
  f \;\colon\; X \longrightarrow f(X) \hookrightarrow Y
$$

equipped with its [[topological subspace|subspace topology]] as a subspace of $Y$ (example \ref{ImageFactorization}). By
prop. \ref{TiSubspaces} also the image $f(X)$ is a $T_n$-topological space, since $Y$ is.
This means that if two elements $x_1, x_2 \in X$ have the same equivalence class, then, by definition of the
equivalence relation, they have the same image under _all_ comntinuous surjective functions into a $T_n$-space,
hence in particular they have the same image under $f \colon X \overset{\text{surjective}}{\longrightarrow} f(X) \hookrightarrow Y$:

$$
  \begin{aligned}
    ( [x_1] = [x_2]) & \Leftrightarrow\, (x_1 \sim x_2)
    \\
    & \Rightarrow\, ( f(x_1) = f(x_2) )
    \,.
  \end{aligned}
$$

This shows that $\tilde f$ is well defined as a function between sets.

To see that $\tilde f$ is also continuous, consider $U \in Y$ an open subset. We need to show that
the pre-image $\tilde f^{-1}(U)$ is open in $X/\sim$. But by definition of the [[quotient topological space|quotient topology]] (example \ref{QuotientTopologicalSpace}), this is open precisely if its pre-image under the quotient projection $t_n(X)$ is open, hence precisely if

$$
  \begin{aligned}
    (t_n(X))^{-1} \left( \tilde f^{-1}\left(U\right)  \right)
    & =
    \left( \tilde f \circ t_n(X) \right)^{-1}(U)
    \\
    & =
    f^{-1}(U)
  \end{aligned}
$$

is open in $X$. But this is the case by the assumption that $f$ is continuous. Hence $\tilde f$ is indeed the unique
continuous function as required.

What remains to be seen is that $T_n X$ as constructed is indeed a $T_n$-topological space.
Hence assume that $[x] \neq [y] \in T_n X$ are two distinct points. Depending on the value of $n$,  need to produce open neighbourhoods
around one or both of these points not containing the other point and possibly disjoint to each other.

Now by definition of $T_n X$ the assumption $[x] \neq [y]$ means that there exists a $T_n$-topological space $Y$ and a surjective continuous function
$f \colon X \overset{surjective}{\longrightarrow} Y$ such that $f(x) \neq f(y) \in Y$:

$$
  ( [x_1] \neq [x_2] )
  \;\Leftrightarrow\;
  \underset{ { Y \in Top_{T_m}  \atop { X \underoverset{\text{surjective}}{f}{\longrightarrow} Y } } }{\exists}
  \left(
    f(x_1) \neq f(x_2)
  \right)
  \,.
$$

Accordingly, since $Y$ is $T_n$,
there exist the respective kinds of neighbourhoods around $f(x_1)$ and $f(x_2)$ in $Y$. Moreover, by the previous statement there
exists the continuous function $\tilde f \colon T_n X \to Y$ with $\tilde f([x_1]) = f(x_1)$ and $\tilde f([x_2]) = f(x_2)$.
By the nature of continuous functions,
the pre-images of these open neighbourhoods in $Y$ are still open in $X$ and still
satisfy the required disjunction properties. Therefore $T_n X$ is a $T_n$-space.

=--

Here are alternative constructions of the reflections:

+-- {: .num_prop #KolmogorovQuotient}
###### Proposition
**([[Kolmogorov quotient]])**

Let $(X,\tau)$ be a [[topological space]]. Consider the [[relation]] on the underlying set
by which $x_1 \sim x_2$ precisely if neither $x_i$ has an [[open neighbourhood]] not containing the other.
This is an [[equivalence relation]]. The [[quotient topological space]] $X \to X/\sim$ by this
equivalence relation (def. \ref{QuotientTopologicalSpace}) exhibits the $T_0$-reflection of $X$ according to prop. \ref{HausdorffReflection}.

=--

A more explicit construction of the Hausdorff quotient than given by prop. \ref{HausdorffReflectionViaHomsIntoAllHausdorffSpaces}
is rather more involved. The issue is that the relation "$x$ and $y$ are not separated by disjoint open neighbourhoods"
is not [[transitive transitive|transitive]];

+-- {: .num_prop #HausdorffReflectionViaTransitiveClosureOfDiagonal}
###### Proposition
**(more explicit [[Hausdorff reflection]])**

For $(Y,\tau_Y)$ a [[topological space]], write $r_Y \subset Y \times Y$
for the [[transitive relation|transitive closure]] of the [[relation]] given by the [[topological closure]] $Cl(\Delta_Y)$ of the [[image]] of the [[diagonal]] $\Delta_Y \colon Y \hookrightarrow Y \times Y$.

$$
  r_Y \coloneqq Trans(Cl(Delta_Y))
  \,.
$$

Now for $(X,\tau_X)$ a [[topological space]], define by [[induction]] for each [[ordinal number]] $\alpha$ an [[equivalence relation]] $r^\alpha$ on $X$ as follows, where we write $q^\alpha \colon X \to H^\alpha(X)$ for the corresponding [[quotient topological space]] projection:

We start the induction with the trivial equivalence relation:

* $r^0_X \coloneqq \Delta_X$;

For a [[successor ordinal]] we set

* $r_X^{\alpha+1} \coloneqq \left\{ (a,b) \in X \times X  \,\vert\, (q^\alpha(a), q^\alpha(b)) \in r_{H^\alpha(X)} \right\}$

and for a [[limit ordinal]] $\alpha$ we set

* $r_X^\alpha \coloneqq \underset{\beta \lt \alpha}{\cup} r_X^\beta$.

Then:

1. there exists an ordinal $\alpha$ such that $r_X^\alpha = r_X^{\alpha+1}$

1. for this $\alpha$ then $H^\alpha(X) = H(X)$ is the Hausdorff reflection from prop. \ref{HausdorffReflectionViaHomsIntoAllHausdorffSpaces}.


=--

A detailed **proof** is spelled out in ([vanMunster 14, section 4](#vanMunster14)).



+-- {: .num_example}
###### Example
**([[Hausdorff reflection]] of the [[line with two origins]])**

The [[Hausdorff reflection]] ($T_2$-reflection, prop. \ref{HausdorffReflection})

$$
  T_2 \;\colon\; Top \longrightarrow Top_{Haus}
$$

of the [[line with two origins]] from example \ref{LineWithTwoOrigins} is the [[real line]] itself:

$$
  T_2\left(
    \left(
      \mathbb{R} \sqcup \mathbb{R}
    \right)/\sim
  \right)
  \;\simeq\;
  \mathbb{R}
  \,.
$$

=--



$\,$

## Sober spaces
 {#SoberSpaces}

While the original formulation of the [[separation axioms]] $T_n$ from def. \ref{HausdorffTopologicalSpace} and def. \ref{NormalSpace}
clearly does follow some kind of pattern, its equivalent reformulation in terms of closure conditions in
prop. \ref{T0InTermsOfClosureOfPoints}, prop. \ref{T1InTermsOfTopologicalClosure}, prop \ref{T2InTermsOfClosedDiagonal},
prop. \ref{T3InTermsOfTopologicalClosures} and prop. \ref{T4InTermsOfTopologicalClosures} suggests rather different patterns.
Therefore it is worthwhile to also consider separation-like axioms that are not among the original list.

In particular, the alternative characterization of the $T_0$-condition in prop. \ref{T0InTermsOfClosureOfPoints}
immediately suggests the following strengthening, different from the $T_1$-condition (see example \ref{T1AndSoberIncomparable} below):

+-- {: .num_defn #Sober}
###### Definition
**([[sober topological space]])**

A [[topological space]] $(X,\tau)$ is called a _[[sober topological space]]_
precisely if every [[irreducible closed subspace]] (def. \ref{IrreducibleClosureOfPoint})
is the [[topological closure]] (def. \ref{ClosedSubset}) of a unique point, hence precisely if the function

$$
  Cl(\{-\}) \;\colon\; X \longrightarrow IrrClSub(X)
$$

from the underlying set of $X$ to the set of [[irreducible closed subsets]] of $X$ (def. \ref{ClosedIrreducible},
well defined according to example \ref{IrreducibleClosureOfPoint}) is [[bijective function|bijective]].

=--

+-- {: .num_prop #T0FromSober}
###### Proposition
**(sober implies $T_0$)**

Every [[sober topological space]] (def. \ref{Sober}) is $T_0$ (def. \ref{HausdorffTopologicalSpace}).

=--

+-- {: .proof}
###### Proof

By prop. \ref{T0InTermsOfClosureOfPoints}.

=--



+-- {: .num_prop #SoberFromHausdorff}
###### Proposition
**([[Hausdorff spaces are sober]])**

Every [[Hausdorff topological space]] (def. \ref{HausdorffTopologicalSpace}) is
a [[sober topological space]] (def. \ref{Sober}).

More specifically, in a Hausdorff topological space
the [[irreducible closed subspaces]] (def. \ref{ClosedIrreducible})
are precisely the [[singleton]] [[subspaces]] (def. \ref{SubspaceTopology}).

Hence, by example \ref{HausdorffMetricSpace}, in particular
every [[metric space]] with its [[metric topology]] (example \ref{MetricTopology}) is sober.

=--

+-- {: .proof}
###### Proof

The second statement clearly implies the first. To see the second
statement, suppose that $F$ is an irreducible closed subspace which
contained two distinct points $x \neq y$. Then by the Hausdorff property
there would be disjoint neighbourhoods $U_x, U_y$, and hence it would follow that
the relative [[complements]] $F \backslash U_x$ and $F \backslash U_y$ were distinct closed proper subsets of
$F$ with

$$
  F = (F \backslash U_x) \cup (F \backslash U_y)
$$

in contradiction to the assumption that $F$ is irreducible.

This [[proof by contradiction|proves by contradiction]] that every irreducible closed subset is a singleton.
Conversely, generally the [[topological closure]] of every singleton is irreducible closed, by example \ref{IrreducibleClosureOfPoint}.

=--

By prop. \ref{T0FromSober} and prop. \ref{SoberFromHausdorff} we have the implications on the right of the following diagram:

| [[separation axioms]]                 |
|---------------------------------------|
| $\array{\\ &&& T_2 = \text{Hausdorff}  \\ && \swArrow && \seArrow \\ \, & T_1 && && \text{sober} & \, \\ && \seArrow && \swArrow \\ &&& T_0 = \text{Kolmogorov} \\ }  $ |

But there there is no implication betwee $T_1$ and sobriety:

+-- {: .num_defn }
###### Proposition

The [[intersection]] of the [[classes]] of [[sober topological spaces]] (def. \ref{Sober}) and $T_1$-topological spaces (def. \ref{HausdorffTopologicalSpace}) is not [[empty set|empty]], but neither class is contained within the other.

=--

That the intersection is not empty follows from prop. \ref{SoberFromHausdorff}.
That neither class is contained in the other is shown by the following counter-examples:

+-- {: .num_example #T1AndSoberIncomparable}
###### Example
**($T_1$ neither implies nor is implied by soberity)**

* The [[Sierpinski space]] (def. \ref{SierpinskiSpace}) is sober, but not $T_1$.

* The [[cofinite topology]] (example \ref{TopologyCofinite}) on a non-[[finite set]] is $T_1$ but not sober.

=--






### Frames of opens


What makes the concept of [[sober topological spaces]] special is that
for them the concept of [[continuous functions]] may be expressed entirely in terms
of the relations between their [[open subsets]], disregarding the underlying
set of points of which these opens are in fact subsets.

Recall from example \ref{ContinuousFunctionGivesFrameHomomorphism}
that for every [[continuous function]] $f \colon (X, \tau_X) \to (Y, \tau_Y)$
the [[pre-image]] function $f^{-1} \colon \tau_Y \to \tau_X$ is a [[frame]] [[homomorphism]]
(def. \ref{HomomorphismOfFramesOfOpens}).

For sober topological spaces the converse holds:

+-- {: .num_prop #FrameMorphismsBetweenOpensOfSoberSpaces}
###### Proposition

If $(X,\tau_X)$ and $(Y,\tau_Y)$ are [[sober topological spaces]] (def. \ref{Sober}), then
for every [[frame]] [[homomorphism]] (def. \ref{HomomorphismOfFramesOfOpens})

$$
  \tau_X \longleftarrow \tau_Y \;\colon\; \phi
$$

there is a unique [[continuous function]] $f \colon X \to Y$ such that $\phi$ is the function
of forming [[pre-images]] under $f$:

$$
  \phi = f^{-1}
  \,.
$$

=--


+-- {: .proof #ProofOfFrameMorphismsBetweenOpensOfSoberSpaces}
###### Proof

We first consider the special case of frame homomorphisms of the form

$$
  \tau_\ast \longleftarrow \tau_X \;\colon\; \phi
$$

and show that these are in bijection to the underlying set $X$, identified with the continuous functions
$\ast \to (X,\tau)$ via example \ref{PointsViaContinuousFunctions}.

By prop. \ref{FrameHomomorphismsToPointAreIrrClSub}, the frame homomorphisms $\phi \colon \tau_X \to \tau_\ast$
are identified with the irreducible closed subspaces $X \backslash U_\emptyset(\phi)$ of $(X,\tau_X)$.
Therefore by assumption of [[sober topological space|sobriety]] of $(X,\tau)$ there is a unique point
$x \in X$ with $X \backslash U_{\emptyset} = Cl(\{x\})$. In particular this means that for $U_x$ an open
neighbourhood of $x$, then $U_x$ is not a subset of $U_\emptyset(\phi)$, and so it follows that $\phi(U_x) = \{1\}$.
In conclusion we have found a unique $x \in X$ such that

$$
  \phi
    \;\colon\;
  U \mapsto
  \left\{
    \array{
      \{1\} & \vert \,\text{if}\, x \in U
      \\
      \emptyset & \vert \, \text{otherwise}
    }
  \right.
  \,.
$$

This is precisely the [[inverse image]] function of the continuous function $\ast \to X$ which sends $1 \mapsto x$.

Hence this establishes the bijection between frame homomorphisms of the form $\tau_\ast \longleftarrow \tau_X$
and continuous functions of the form $\ast \to (X,\tau)$.

With this it follows that a general frame homomorphism of the form $\tau_X \overset{\phi}{\longleftarrow} \tau_Y$
defines a function of sets $X \overset{f}{\longrightarrow} Y$ by [[composition]]:

$$
  \array{
    X &\overset{f}{\longrightarrow}& Y
    \\
    (\tau_\ast \leftarrow \tau_X)
    &\mapsto&
    (\tau_\ast \leftarrow \tau_X \overset{\phi}{\longleftarrow} \tau_Y)
  }
  \,.
$$

By the previous analysis, an element $U_Y \in \tau_Y$ is sent to $\{1\}$ under this composite precisely if
the corresponding point $\ast \to X \overset{f}{\longrightarrow} Y$ is in $U_Y$, and similarly for
an element $U_X \in \tau_X$. It follows that $\phi(U_Y) \in \tau_X$ is precisely that subset of
points in $X$ which are sent by $f$ to elements of $U_Y$, hence that $\phi = f^{-1}$ is the [[pre-image]]
function of $f$. Since $\phi$ by definition sends open subsets of $Y$ to open subsets of $X$, it follows
that $f$ is indeed a continuous function. This proves the claim in generality.

=--


+-- {: .num_remark #Locales}
###### Remark
**([[locales]])**

Proposition \ref{FrameMorphismsBetweenOpensOfSoberSpaces}
is often stated as saying that sober topological spaces are [[equivalence of categories|equivalently]] the
"[[locales with enough points]]" ([Johnstone 82, II 1.](#Johnstone82)). Here "[[locale]]" refers to a concept akin to topological spaces where one considers
_just_ a "[[frame of open subsets]]" $\tau_X$, without requiring that its elements be actual [[subsets]] of some ambient set.
The natural notion of [[homomorphism]] between such generalized topological spaces are clearly the [[frame]] homomorphisms
$\tau_X \leftarrow \tau_Y$ from def. \ref{HomomorphismOfFramesOfOpens}.

From this perspective, prop. \ref{FrameMorphismsBetweenOpensOfSoberSpaces} says that
sober topological spaces $(X, \tau_X)$ are entirely characterized by their [[frames of opens]] $\tau_X$ and just so happen to
"have enough points" such that these are actual open subsets of some ambient set, namely of $X$.

=--




### Sober reflection

We saw above in prop. \ref{HausdorffReflection} that every $T_n$-toopological space for $n \in \{0,1,2\}$ has a "best approximation from the left" by a $T_n$-topological space (for $n = 2$: "[[Hausdorff reflection]]"). We now discuss the analogous statement for [[sober topological spaces]].


Recall again the [[point topological space]]  $\ast \coloneqq ( \{1\}, \tau_\ast = \left\{ \emptyset, \{1\}\right\} )$
(example \ref{Point}).


+-- {: .num_defn #SoberificationConstruction}
###### Definition
**([[sober reflection]])**

Let $(X,\tau)$ be a [[topological space]].

Define $S X$ to be the set

$$
  S X \coloneqq FrameHom( \tau_X, \tau_\ast )
$$

of [[frame]] [[homomorphisms]] (def. \ref{HomomorphismOfFramesOfOpens}) from the [[frame of opens]] of $X$ to that of the point. Define a [[topological space|topology]] $\tau_{S X} \subset P(S X)$ on this set by declaring it to have one element $\tilde U$ for each element $U \in \tau_X$ and given by

$$
  \tilde U
    \;\coloneqq\;
  \left\{
    \phi \in S X
    \,\vert\,
    \phi(U) = \{1\}
  \right\}
  \,.
$$

Consider the function

$$
  \array{
    X &\overset{s_X}{\longrightarrow}& S X
    \\
    x &\mapsto& (const_x)^{-1}
  }
$$

which sends an element $x \in X$ to the function which assigns [[inverse images]] of the [[constant function]] $const_x \;\colon\; \{1\} \to X$ on that element.

We are going to call this function the _[[sober reflection]]_ of $X$.

=--

+-- {: .num_lemma #SoberificationConstructionWellDefined}
###### Lemma
**([[sober reflection]] is well defined)**

The construction $(S X, \tau_{S X})$ in def. \ref{SoberificationConstruction} is a [[topological space]], and the function $s_X \colon X \to S X$ is a [[continuous function]]

$$
  s_X \colon (X, \tau_X) \longrightarrow (S X, \tau_{S X})
$$

=--

+-- {: .proof #ProofOfSoberificationConstructionWellDefined}
###### Proof

To see that $\tau_{S X} \subset P(S X)$ is closed under arbitrary unions and finite intersections, observe that the function

$$
  \array{
    \tau_X &\overset{\widetilde{(-)}}{\longrightarrow}& \tau_{S X}
    \\
    U &\mapsto& \tilde U
  }
$$

in fact preserves arbitrary unions and finite intersections. Whith this the statement follows by the fact that $\tau_X$ is closed under these operations.

To see that $\widetilde{(-)}$ indeed preserves unions, observe that (e.g. [Johnstone 82, II 1.3 Lemma](#Johnstone82))

$$
  \begin{aligned}
    p \in \underset{i \in I}{\cup} \widetilde{U_i} \;
    & \Leftrightarrow
    \underset{i \in I}{\exists} p(U_i) = \{1\}
    \\
    & \Leftrightarrow \underset{i \in I}{\cup} p(U_i) = \{1\}
    \\
    & \Leftrightarrow p\left(\underset{i \in I}{\cup} U_i\right) = \{1\}
    \\
    & \Leftrightarrow p \in \widetilde{ \underset{i \in I}{\cup} U_i }
  \end{aligned}
  \,,
$$

where we used that the frame homomorphism $p \colon \tau_X \to \tau_\ast$ preserves unions. Similarly for intersections, now with $I$ a [[finite set]]:

$$
  \begin{aligned}
    p \in \underset{i \in I}{\cap} \widetilde{U_i} \;
    & \Leftrightarrow
    \underset{i \in I}{\forall} p(U_i) = \{1\}
    \\
    & \Leftrightarrow \underset{i \in I}{\cap} p(U_i) = \{1\}
    \\
    & \Leftrightarrow p\left(\underset{i \in I}{\cap} U_i\right) = \{1\}
    \\
    & \Leftrightarrow p \in \widetilde{ \underset{i \in I}{\cap} U_i }
  \end{aligned}
  \,,
$$

where we used that the frame homomorphism $p$ preserves finite intersections.

To see that $s_X$ is continuous, observe that $s_X^{-1}(\tilde U) = U$, by construction.

=--

+-- {: .num_lemma #UnitIntoSXDetectsT0AndSoberity}
###### Lemma
**([[sober reflection]] detects $T_0$ and soberity)**

For $(X, \tau_X)$ a [[topological space]],
the function $s_X \colon X \to S X$ from def. \ref{SoberificationConstruction} is

1. an [[injection]] precisely if $(X,\tau_X)$ is $T_0$ (def. \ref{HausdorffTopologicalSpace});

1. a [[bijection]] precisely if $(X,\tau_Y)$ is [[sober topological space|sober]] (def. \ref{Sober}), in which  case $s_X$ is in fact a [[homeomorphism]] (def. \ref{Homeomorphism}).

=--

+-- {: .proof}
###### Proof

By lemma \ref{FrameHomomorphismsToPointAreIrrClSub} there is an identification $S X \simeq IrrClSub(X)$ and via this $s_X$ is identified with the map $x \mapsto Cl(\{x\})$.

Hence the second statement follows by definition, and the first statement by prop. \ref{T0InTermsOfClosureOfPoints}.

That in the second case $s_X$ is in fact a homeomorphism follows from the definition of the opens $\tilde U$: they are identified with the opens $U$ in this case (...expand...).

=--


+-- {: .num_lemma #SoberificationIsIndeedSober}
###### Lemma
**([[soberification]] lands in [[sober spaces]], e.g. [Johnstone 82, lemma II 1.7](#Johnstone82))**

For $(X,\tau)$ a [[topological space]], then the topological space $(S X, \tau_{S X})$ from def. \ref{SoberificationConstruction}, lemma \ref{SoberificationConstructionWellDefined} is sober.

=--

+-- {: .proof}
###### Proof

Let $S X \backslash \tilde U$ be an [[irreducible closed subspace]] of $(S X, \tau_{S X})$. We need to show that it is the [[topological closure]] of a unique element $\phi \in S X$.

Observe first that also $X \backslash U$ is irreducible.

To see this use prop. \ref{OpenSubsetVersionOfClosedIrreducible}, saying that irreducibility of $X \backslash U$ is equivalent to $U_1 \cap U_2 \subset U \Rightarrow (U_1 \subset U) or (U_2 \subset U)$. But if $U_1 \cap U_2 \subset U$ then also $\tilde U_1 \cap \tilde U_2 \subset \tilde U$ (as in the [proof](#ProofOfSoberificationConstructionWellDefined) of lemma \ref{SoberificationConstructionWellDefined}) and hence by assumption on $\tilde U$ it follows that $\tilde U_1 \subset \tilde U$ or $\tilde U_2 \subset \tilde U$. By lemma \ref{FrameHomomorphismsToPointAreIrrClSub} this in turn implies $U_1 \subset U$ or $U_2 \subset U$.  In conclusion, this shows that also $X \backslash U$ is irreducible .

By lemma \ref{FrameHomomorphismsToPointAreIrrClSub} this irreducible closed subspace corresponds to a point $p \in S X$. By that same lemma, this frame homomorphism $p \colon \tau_X \to \tau_\ast$ takes the value $\emptyset$ on all those opens which are inside $U$. This means that the [[topological closure]] of this point is just $S X \backslash \tilde U$.

This shows that there exists at least one point of which $X \backslash \tilde U$ is the topological closure. It remains to see that there is no other such point.

So let $p_1 \neq p_2 \in S X$ be two distinct points. This means that there exists $U \in \tau_X$ with $p_1(U) \neq p_2(U)$. Equivalently this says that $\tilde U$ contains one of the two points, but not the other. This means that $(S X, \tau_{S X})$ is [[separation axiom|T0]].
By prop. \ref{T0InTermsOfClosureOfPoints} this is equivalent to there being no two points with the same topological closure.

=--

+-- {: .num_prop}
###### Proposition
**(unique factorization through soberification)**

For $(X, \tau_X)$ any [[topological space]], for $(Y,\tau_Y^{sob})$ a sober topological space, and for $f \colon (X, \tau_X) \longrightarrow (Y, \tau_Y)$ a [[continuous function]], then it factors uniquely through the [[soberification]] $s_X \colon (X, \tau_X) \longrightarrow (S X, \tau_{S X})$ from def. \ref{SoberificationConstruction}, lemma \ref{SoberificationConstructionWellDefined}

$$
  \array{
    (X, \tau_X) &\overset{f}{\longrightarrow}& (Y, \tau_Y^{sob})
    \\
    {}^{\mathllap{s_X}}\downarrow & \nearrow_{\exists !}
    \\
    (S X , \tau_{S X})
  }
  \,.
$$

=--


+-- {: .proof}
###### Proof

By the construction in def. \ref{SoberificationConstruction}, we find that the outer part of the following square [[commuting square|commutes]]:

$$
  \array{
    (X, \tau_X) &\overset{f}{\longrightarrow}& (Y, \tau^{sob}_Y)
    \\
    {}^{\mathllap{s_X}}\downarrow & \nearrow& \downarrow^{\mathrlap{s_{S X}}}
    \\
    (S X, \tau_{S X})
     &\underset{S f}{\longrightarrow}&
    (S S X, \tau_{S S X})
  }
  \,.
$$

By lemma \ref{SoberificationIsIndeedSober} and lemma \ref{UnitIntoSXDetectsT0AndSoberity}, the right vertical morphism $s_{S X}$ is an isomorphism (a [[homeomorphism]]), hence has an [[inverse morphism]]. This defines the diagonal morphism, which is the desired factorization.

To see that this factorization is unique, consider two factorizations $\tilde f, \overline{f} \colon \colon (S X, \tau_{S X}) \to (Y, \tau_Y^{sob})$ and apply the soberification construction once more to the triangles

$$
  \array{
    (X, \tau_X) &\overset{f}{\longrightarrow}& (Y, \tau_Y^{sob})
    \\
    {}^{\mathllap{s_X}}\downarrow & \nearrow_{ \tilde f, \overline{f}}
    \\
    (S X , \tau_{S X})
  }
  \phantom{AAA}
    \mapsto
  \phantom{AAA}
  \array{
    (S X, \tau_{S X}) &\overset{S f}{\longrightarrow}& (Y, \tau_Y^{sob})
    \\
    {}^{\simeq}\downarrow & \nearrow_{ \tilde f, \overline{f}}
    \\
    (S X , \tau_{S X})
  }
  \,.
$$

Here on the right we used again lemma \ref{UnitIntoSXDetectsT0AndSoberity} to find that the vertical morphism is an isomorphism, and that $\tilde f$ and $\overline{f}$ do not change under soberification, as they already map between sober spaces. But now that the left vertical morphism is an isomorphism, the commutativity of this triangle for both $\tilde f$ and $\overline{f}$ implies that $\tilde f = \overline{f}$.

=--

In **summary** we have found

+-- {: .num_prop #SoberReflection}
###### Proposition
**([[sober reflection]])**

For every [[topological space]] $X$ there exists

1. a [[sober topological spaces]] $S X$;

1. a [[continuous function]] $s_n \colon X \longrightarrow S X$

such that ...

=--

As before for the $T_n$-reflection in remark \ref{ReflectiveSubcategory},
the statement of prop. \ref{SoberReflection} may neatly be re-packaged:

+-- {: .num_remark #SobertopologicalSpacesFormReflectiveSubcategory}
###### Remark
**([[sober topological spaces]] are a [[reflective subcategory]])**

In the language of [[category theory]] (remark \ref{TopCategory})
and in terms of the concept of [[adjoint functors]] (remark \ref{ReflectiveSubcategory}),
proposition \ref{SoberReflection} simply says that [[sober topological spaces]]
form a [[reflective subcategory]] $Top_{sob}$ of the category [[Top]] of all topological spaces

$$
  Top_{sob}
    \underoverset
      {\underset{}{\hookrightarrow}}
      {\overset{s}{\longrightarrow}}
      {\bot}
  Top
  \,.
$$

=--


$\,$

## Universal constructions
 {#UniversalConstructions}

We have seen [above](#BasicConstructions) various construction principles for [[topological spaces]] [above](#BasicConstructions),
such as [[topological subspaces]] and [[topological quotient spaces]]. It turns out that
these constructions enjoy certain
"[[universal properties]]" which allow us to find [[continuous functions]] into or out of these
spaces, respectively (example \ref{UniversalPropertyOfQuotientSpace} below).
Since this is useful for handling topological spaces (we secretly used the universal property of the
quotient space construction already in the proof of prop. \ref{HausdorffReflectionViaHomsIntoAllHausdorffSpaces}), we next consider,
in def. \ref{LimitingCone} below, more general
"[[universal constructions]]" of topological spaces, called _[[limits]]_ and _[[colimits]]_ of topological spaces
(and to be distinguished from limits _in_ topological spaces, in the sense of [[convergence]]
of [[sequences]] as in def. \ref{Convergence}).

Moreover, we have seen [above](#HausdorffReflections) that the [[quotient space]] construction in general does not
preserve the $T_n$-[[separation axiom|separation]] property or [[sober space|soberity]] property
of topological spaces, while the [[topological subspace]] construction does. The same turns out
to be true for the more general "colimiting" and "limiting" universal constructions. But we have also seen
that we may universally "reflect" any topological space to becomes a $T_n$-space or sober space.
The remaining question then is whether this reflection breaks the desired universal property.
We discuss that this is not the case, that instead the universal construction in all topological spaces
followed by these reflections gives the correct universal constructions in $T_n$-separated and sober topological
spaces, respectively (remark \ref{CoLimitsInNiceTopologicalSpaces} below).

After these general considerations, we finally discuss a [list of examples](#UniversalConstructionsExamples) of universal constructions in topological spaces.

$\,$

Here is a motivating example of a [[universal property]]:

+-- {: .num_example #UniversalPropertyOfQuotientSpace}
###### Example
**([[universal property]] of [[quotient topological spaces]])**

Let $X$ be a [[topological space]], and let $\sim$ be an [[equivalence relation]] on its
underlying set. Then the corresponding [[quotient topological space]] $X/\sim$
together with the corresponding qutient [[continuous function]]
$p \colon X \to X/\sim$ has the following [[universal property]]:

Given $f \colon X \longrightarrow Y$ any [[continuous function]] out of $X$
with the property that it respects the given [[equivalence relation]], in that

$$
  (x_1 \sim x_2)
    \;\Rightarrow\;
  \left(
    f(x_1) = f(x_2)
  \right)
$$

then there is a unique [[continuous function]] $\tilde f \colon X/\sim \longrightarrow Y$
such that

$$
  f = \tilde f\circ p
  \phantom{AAAA}
  i.e.
  \phantom{Aaaa}
  \array{
    X &\overset{f}{\longrightarrow}& Y
    \\
    {}^{\mathllap{p}}\downarrow & \nearrow_{\exists ! \tilde f}
    \\
    X/\sim
  }
  \,.
$$

(This universal property is often useful, for instance we already used it in the construction of the
$T_n$-reflection in prop. \ref{HausdorffReflectionViaHomsIntoAllHausdorffSpaces}.)

=--

+-- {: .proof}
###### Proof

First observe that there is a unique function $\tilde f$ as claimed on the level of
functions of the underlying sets:
In order for $f = \tilde f \circ p$ to hold, $\tilde f$ must send an equivalence class in $X/\sim$
to one of its members

$$
  \tilde f \;\colon\; [x] \mapsto x
$$

and that this is well defined and independent of the choice of representative $x$ is guaranteed by
the condition on $f$ above.

Hence it only remains to see that $\tilde f$ defined this way is continuous, hence that for
$U \subset Y$ an open subset, then its pre-image $\tilde f^{-1}(U) \subset X/\sim$ is open
in the quotient topology. By definition of the quotient topology (example \ref{QuotientTopologicalSpace}),
this is the case precisely if its further pre-image under $p$ is open in $X$. But by the
fact that $f = \tilde f \circ p$, this is the case by the continuity of $f$:

$$
  \begin{aligned}
    p^{-1}
    \left(
       \tilde f^{-1}
       \left(
         U
       \right)
    \right)
    & =
    \left(
      \tilde f \circ p
    \right)^{-1}(U)
    \\
    & = f^{-1}(U)
  \end{aligned}
  \,.
$$

=--

This kind of example we now generalize.

$\,$

### Limits and colimits
 {#LimitsAndColimits}

We consider now the general definition of [[diagrams]] of [[topological spaces]] (def. \ref{Diagram} below),
their [[cones]] and [[co-cones]] (def. \ref{Cone}) as well as [[limit|limiting cones]] and [[colimit|colimiting cocones]] (def. \ref{LimitingCone} below). Then we use these concepts to see generally why [[limits]] (such as [[product spaces]] and [[subspaces]])
of $T_{n \leq 2}$-spaces and of [[sober spaces]] are again $T_n$ or sober, respectively, and to see that the
correct [[colimits]] (such as [[disjoint union spaces]] and [[quotient spaces]]) of $T_n$- or sober spaces
are instead the _$T_n$-reflection_ (prop. \ref{HausdorffReflection}) or sober reflection (prop. \ref{SoberReflection}), respectively, of these
colimit constructions performed in the context of unconstrained topological spaces.


$\,$


+-- {: .num_defn #Diagram}
###### Definition
**([[diagram]] in a [[category]])**

A _[[diagram]]_ $X_\bullet$ of [[sets]] or of [[topological spaces]] is

1. a [[set]] $\{ X_i \}_{i \in I}$ of [[objects]] (i.e. of sets or topological spaces)

1. for every [[pair]] $(i,j) \in I \times I$ of labels of objects a [[set]]
   $\{ X_i \overset{ f_\alpha }{\longrightarrow} X_j\}_{\alpha \in I_{i,j}}$ of [[morphisms]] between these objects (i.e. [[functions]] or [[continuous functions]]);

1. for each [[triple]] $i,j,k \in I$ a [[function]]

   $$
     comp_{i,j,k} \;\colon\; I_{i,j} \times I_{j,k} \longrightarrow I_{i,k}
   $$

such that

1. for every $i \in I$ the [[identity morphisms]] $f_i = id_{X_i} \colon X_i \to X_i$ is part of the diagram;

1. $comp$ is [[associativity|associative]] and [[unital]] in in the evident sense

1. for every composable pair of morphisms

  $$
    X_i
      \overset{f_{\alpha} }{\longrightarrow}
    X_j
      \overset{ f_{\beta} }{\longrightarrow}
    X_k
  $$

  then the [[composition|composite]] of these two morphisms equals the morphism of the diagram that is
  labeled by the value of $comp_{i,j,k}$ on their labels:

  $$
    f_{\beta} \circ f_\alpha
    \,=\,
    f_{comp_{i,j,k}( \alpha, \beta )}
    \,.
  $$

The last condition we depict as follows:

$$
  \array{
    && X_j
    \\
    & {}^{\mathllap{f_{\alpha}}}\nearrow && \searrow^{\mathrlap{f_{\beta}}}
    \\
    X_i && \underset{ comp_{i,j,k}(\alpha,\beta) }{\longrightarrow} && X_k
  }
  \,.
$$

=--

On the face of it the definition \ref{Diagram} may look a little baroque, but we see in remark \ref{FunctorialDefinitionOfDiagrams}
below how it has a convenient re-packaging. More importantly for our purposes, all concrete examples of diagrams
that we will be concerned with here are fairly simplistic examples of the general definition:


+-- {: .num_example #DiscreteDiagram}
###### Example
**([[discrete category|discrete]] [[diagram]] and [[empty diagram]])**

Let $I$ be any [[set]], and for each $(i,j) \in I \times I$ let $I_{i,j}$
either by the [[empty set]] if the indices do not agree, or else [[generalized the|the]]
[[singleton set]], whose unique element we denote by $id_i$:

$$
  I_{i,j}
    \coloneqq
  \left\{
    \array{
      \emptyset & \vert \, i \neq j
      \\
      \{id_i\} & \,\vert\, I = j
    }
  \right.
  \,.
$$

There is a unique choice for the composition function for these sets to
index a [[diagram]] according to def. \ref{Diagram}.

The corresponding diagrams
are simply a set of sets/topological spaces with no non-trivial morphisms between them.
This is called a _[[discrete category|discrete]] [[diagram]]_.


Notice that here the index set may be [[empty set]], $I = \emptyset$, in which case the
corresponding diagram consists of no data. This is also called the _[[empty diagram]]_.

=--

+-- {: .num_defn #ParallelMorphisms}
###### Definition
**([[parallel morphisms]] [[diagram]])**

Let $I = \{a, b\}$ be the [[set]] with two elements, and consider the sets


$$
  I_{i,j}
    \;\coloneqq\;
  \left\{
    \array{
      \{id_i\} &\vert\, i = j
      \\
      \{ 1,2 \} &\vert\, (i = a) \,\text{and}\, (j = b)
      \\
      \emptyset & \vert \, (i=b) \,\text{and}\, (j = a)
    }
  \right\}
  \,.
$$

Again there is a unique composition function that makes this the index data of a diagram according to
def. \ref{Diagram}.

Such a diagram is called a _pair of [[parallel morphisms]]_:

$$
  X_a
    \underoverset
      {\underset{f_2}{\longrightarrow}}
      {\overset{f_1}{\longrightarrow}}
      {\phantom{AAAAA}}
  X_b
  \,.
$$

=--


+-- {: .num_example #SpanDiagram}
###### Example
**([[span]] and [[cospan]] [[diagram]])**

Let $I = \{a,b,c\}$ and

$$
  I_{i ,j}
   =
  \left\{
    \array{
      \{id_i\} & \vert \, i = j
      \\
      \{f_1\} & \vert \, (i = c) \,\text{and}\, (j = a)
      \\
      \{f_2\} & \vert \, (i = c) \,\text{and}\, (j = b)
      \\
      \emptyset & \vert \, \text{otherwise}
    }
  \right.
$$


Again there is a unique composition function for this. The corresponding diagrams look like this:

$$
  \array{
    && X_c
    \\
    & {}^{\mathllap{f_1}}\swarrow && \searrow^{\mathrlap{f_2}}
    \\
    X_a && && X_b
  }
  \,.
$$

This is called a _[[span]] [[diagram]]_.

Similary, there is the _[[cospan]]_ diagram of the form

$$
  \array{
    && X_c
    \\
    & {}^{\mathllap{f_1}}\nearrow && \nwarrow^{\mathrlap{f_2}}
    \\
    X_a && && X_b
  }
  \,.
$$

=--

+-- {: .num_example}
###### Example
**([[tower]] [[diagram]])**

Let $I = \mathbb{N}$ be the set of [[natural numbers]] and consider

$$
  I_{i,j}
   \;\coloneqq\;
  \left\{
    \array{
      \{f_{i,j}\} & \vert \, i \leq j
      \\
      \emptyset & \vert \, \text{otherwise}
    }
  \right.
$$

Once more, there is a unique choice of composition function for this to index
diagrams according to def. \ref{Diagram}. These are called _[[tower]] [[diagrams]]_


$$
   X_0
     \overset{f_{0,1}}{\longrightarrow}
   X_1
     \overset{f_{1,2}}{\longrightarrow}
   X_2
     \overset{f_{2,3}}{\longrightarrow}
   X_3
     \overset{}{\longrightarrow}
   \cdots
   \,.
$$


Similarly there are co-tower diagram

$$
   X_0
     \overset{f_{0,1}}{\longleftarrow}
   X_1
     \overset{f_{1,2}}{\longleftarrow}
   X_2
     \overset{f_{2,3}}{\longleftarrow}
   X_3
     \overset{}{\longleftarrow}
   \cdots
   \,.
$$


=--


+-- {: .num_defn #FunctorialDefinitionOfDiagrams}
###### Remark
**([[diagrams]] are [[functors]])**

Of course the definition of a _[[diagram]]_ of sets or topological space in def. \ref{Diagram}
has a succint reformulation in the language of [[category theory]] (remark \ref{TopCategory}) above:

A glance at definition \ref{Diagram} shows that the data

$$
  \mathcal{I} \coloneqq (I, (I_{i,j})_{i,j \in I}, \{comp_{i,j,k}\}_{i,j,k \in I} )
$$

itself defines a [[category]]: its

* set of [[objects]] is $I$;

* set of [[morphisms]] between objects $(i,j) \in I \times I$ is $I_{i,j}$;

* [[identity morphisms]] are the $f_i \in I_{i,j}$;

* [[composition]] operation is given by the functions $c_{i, j ,j}$.

One difference between this category $\mathcal{I}$ and the categories [[Set]] of sets or [[Top]]
of topological spaces is that the collection of objects in $\mathcal{I}$ is an actual [[set]]
instead of a proper [[class]]. To amplify this one also says that $\mathcal{I}$ is a "[[small category]]".

Moreover, with this identification made, then it is clear that all the data that makes up the diagram in
def. \ref{Diagram} is equivalently re-formulated simply by saying that a diagram in a
category $\mathcal{C}$ is a [[functor]]

$$
  X_\bullet \;\colon\; \mathcal{I} \longrightarrow \mathcal{C}
  \,.
$$

Here the choice of $\mathcal{I}$ is also called the "shape" of the diagram, and one speaks of an
_$\mathfrak{I}$-shaped diagram in $\\mathcal{C}$_.

So for example an _$\mmathcal{I}$-shaped diagram of sets_ is a choice of a [[small category]] $\mathcal{I}$
and of a [[functor]] of the form

$$
  X_\bullet
    \;\colon\;
  \mathcal{I} \longrightarrow Set
  \,,
$$

while an $\mathcal{I}$-shaped diagram of topological spaces is a functor of the form

$$
  X_\bullet
   \;\colon\;
  \mathcal{I}
    \longrightarrow
  Top
$$

and so on.

=--

+-- {: .num_defn #Cone}
###### Definition
**([[cone]] over a [[diagram]])**

Consider a [[diagram]] of sets or of topological spaces (def. \ref{Diagram})

$$
  X_\bullet
    \,=\,
  \left(
     \left\{
       X_i \overset{f_\alpha}{\longrightarrow} X_j
     \right\}_{i,j \in I, \alpha \in I_{i,j}}
     \,,\,
     \mathrm{comp}
  \right)
  \,.
$$

Then

1. a _[[cone]]_ over this diagram is

   1. an [[object]] $\tilde X$ (i.e. a set or a topological space)

   1. for each $i \in I$ a morphism $\tilde X \overset{p_i}{\longrightarrow} X_i$ (i.e. a function or a continuous function)

   such that

   * for all $(i,j) \in I \times I$ and all $\alpha \in I_{i,j}$ then the condition

     $$
       f_{\alpha} \circ p_i = p_j
     $$

     holds, which we depict as follows:

     $$
       \array{
         && \tilde X
         \\
         & {}^{\mathllap{p_i}}\swarrow && \searrow^{\mathrlap{p'_j}}
         \\
         X_i
           && \underset{f_\alpha}{\longrightarrow} &&
         X_j
       }
     $$

1. a _[[co-cone]]_ over this diagram is

   1. an [[object]] $\tilde X$ in the category;

   1. for each $i \in I$ a morphism $q_i \colon X_i \longrightarrow \tilde X$ in the category

   such that

   * for all $(i,j) \in I \times I$ and all $\alpha \in I_{i,j}$ then the condition

     $$
       q_j \circ f_{\alpha} = q_i
     $$

     holds, which we depict as follows:

     $$
       \array{
         X_i && \overset{f_\alpha}{\longrightarrow} && X_j
         \\
         & {}_{\mathllap{q_i}}\searrow && \swarrow_{\mathrlap{q_j}}
         \\
         && \tilde X
       }
       \,.
     $$

=--


+-- {: .num_remark #ConesAreNaturalTransformations}
###### Remark
**([[cones]] are [[natural transformations]])**


In the language of [[category theory]] (remark \ref{TopCategory})
and in view of the interpretation of [[diagrams]] as [[functors]]  (remark \ref{FunctorialDefinitionOfDiagrams})
then the definition of [[cone]] in def. \ref{Cone} simply says that a [[cone]]
is a [[natural transformation]] from a _[[constant functor]]_ to the [[functor]] that exbits the
given diagram.


=--


+-- {: .num_example}
###### Example
**([[solutions]] to [[equations]] are [[cones]])**

Let $f,g \colon \mathbb{R} \to \mathbb{R}$ two [[functions]], and consider the
corresponding [[parallel morphism]] [[diagram]] of sets (example \ref{ParallelMorphisms}):

$$
  \mathbb{R}
    \underoverset
      {\underset{f_2}{\longrightarrow}}
      {\overset{f_1}{\longrightarrow}}
      {\phantom{AAAAA}}
  \mathbb{R}
  \,.
$$

Then a [[cone]] over this diagram with tip the [[singleton]] set $\ast$ is a _[[solution]]_ to
the [[equation]] $f(x) = g(x)$

$$
  \array{
    && \ast
    \\
    & \swarrow && \searrow
    \\
    \mathbb{R}
      &&
      \underoverset
        {\underset{f_2}{\longrightarrow}}
        {\overset{f_1}{\longrightarrow}}
        {\phantom{AAAAA}}
      &&
    \mathbb{R}
  }
  \,.
$$


=--


+-- {: .num_defn #LimitingCone}
###### Definition
**([[limit|limiting cone]] over a [[diagram]])**

Consider a [[diagram]] of sets or of topological spaces (def. \ref{Diagram}):

$$
  X_\bullet
    \,=\,
  \left(
     \left\{
       X_i \overset{f_\alpha}{\longrightarrow} X_j
     \right\}_{i,j \in I, \alpha \in I_{i,j}}
     \,,\,
     \mathrm{comp}
  \right)
$$

 Then

1. its _[[limit|limiting cone]]_ (or just _[[limit]]_ for short) is, if it exists,
   [[generalized the|the]] [[cone]]

   $$
     \left\{
     \array{
       && \underset{\longleftarrow}{\lim}_i X_i
       \\
       & {}^{\mathllap{p_i}}\swarrow && \searrow^{\mathrlap{p_j}}
       \\
       X_i
         && \underset{f_\alpha}{\longrightarrow} &&
       X_j
     }
     \right\}
   $$

   over this diagram (def. \ref{Cone}) which is _universal_ or _initial_ among all
   possible cones,
   in that it has the property that for

   $$
     \left\{
     \array{
       && \tilde X
       \\
       & {}^{\mathllap{p'_i}}\swarrow && \searrow^{\mathrlap{p'_j}}
       \\
       X_i
         && \underset{f_\alpha}{\longrightarrow} &&
       X_j
     }
     \right\}
   $$

   any other [[cone]], then there is a unique morphism

   $$
     \phi \;\colon\; \tilde X \overset{}{\longrightarrow} \underset{\longrightarrow}{\lim}_i X_i
   $$

   that factors the given cone through the limiting cone, in that for all $i \in I$ then

   $$
     p'_i = p_i \circ \phi
   $$

   which we depict as follows:

   $$
     \array{
       \tilde X
       \\
       {}^{\mathllap{\phi}}\downarrow & \searrow^{\mathrlap{p_i}}
       \\
       \underset{\longrightarrow}{\lim}_i X_i
       &\underset{p_i}{\longrightarrow}&
       X_i
     }
   $$

1. its _[[colimit|colimiting cocone]]_ (or just _[[colimit]]_ for short) is, if it exists,
   [[generalized the|the]] [[cocone]]

   $$
     \left\{
     \array{
       X_i
         && \underset{f_\alpha}{\longrightarrow} &&
       X_j
       \\
       & {}^{\mathllap{q_i}}\searrow && \swarrow^{\mathrlap{q_j}}
       \\
       \\
       && \underset{\longrightarrow}{\lim}_i X_i
     }
     \right\}
   $$

   under this diagram (def. \ref{Cone}) which is _universal_ or _terminal_ among all
   possible co-cones,
   in that it has the property that for

   $$
     \left\{
     \array{
       X_i
         && \underset{f_\alpha}{\longrightarrow} &&
       X_j
       \\
       & {}^{\mathllap{q'_i}}\searrow && \swarrow_{\mathrlap{q'_j}}
       \\
       && \tilde X
     }
     \right\}
   $$

   any other [[cocone]], then there is a unique morphism

   $$
     \phi \;\colon\;  \underset{\longrightarrow}{\lim}_i X_i \overset{}{\longrightarrow} \tilde X
   $$

   that factors the given co-cone through the co-limiting cocone, in that for all $i \in I$ then

   $$
     q'_i = \phi \circ q_i
   $$

   which we depict as follows:

   $$
     \array{
       X_i
       &\overset{q_i}{\longrightarrow}&
       \underset{\longrightarrow}{\lim}_i X_i
       \\
       {}^{\mathllap{\phi}}\downarrow & \swarrow^{\mathrlap{q'_i}}
       \\
       \tilde X
     }
   $$

=--

Here is a key property of (co-)limits:

+-- {: .num_prop #HomFunctorPreservesLimits}
###### Proposition
**(homomorphisms into a limit cone are the limit of the homomorphisms into the diagram)**

Let $\mathcal{C}$ be a [[category]] (such as [[Set]] or [[Top]]) and let
$$
  X_\bullet \colon \mathcal{I} \longrightarrow \mathcal{C}
$$

be a [[diagram]] in $\mathcal{C}$.

1. If the [[limit]] $\underset{\longleftarrow}{\lim}_i X_i \in \mathcal{C}$ exists, then
   the [[set]] of [[homomorphisms]] into this limiting object os the limit over the sets of morphisms into the
   components $X_i$:

   $$
     Hom_{\mathcal{C}}(Y, \underset{\longleftarrow}{\lim}_i X_i )
      \simeq
     \underset{\longleftarrow}{\lim}_i Hom_{Set}(Y, X_i)
   $$


1. If the [[colimit]] $\underset{\longrightarrow}{\lim}_i X_i \in \mathcal{C}$ exists, then
   the [[set]] of [[homomorphisms]] out of this colimiting object is the colimit over the sets of
   morphisms out of the components of $X_i$

   $$
     Hom_{\mathcal{C}}(\underset{\longrightarrow}{\lim}_i X_i, Y)
       \simeq
     \underset{\longrightarrow}{\lim} Hom_{Set}( X_i, Y )
     \,.
   $$

=--



This concludes the general definition of universal constructions. Before we consider explicit
examples [below](#UniversalConstructionsExamples) we now first consider a more explicit
description of these limits of colimits of diagrams of sets and of topological spaces.

$\,$


+-- {: .num_prop #SetLimits}
###### Proposition
**([limits and colimits of sets](limits+and+colimits+by+example#limcoliminset))**

Let

$$
  X_\bullet
    \,\colon\,
  \mathcal{I}
    \longrightarrow
  Set
$$

be a [[diagram]] of [[sets]] (def. \ref{Diagram}, using the notation from remark \ref{FunctorialDefinitionOfDiagrams}). Then

1. its [[limit|limit cone]] (def. \ref{LimitingCone}) exists and is given by the following [[subset]] of the [[Cartesian product]]
   $\underset{i \in I}{\times} X_i$
   of all the [[sets]] $X_i$ appearing in the diagram

   $$
     \underset{\longleftarrow}{\lim}_i X_i
     \,\overset{\phantom{AAA}}{\hookrightarrow}\,
     \underset{i \in I}{\times} X_i
   $$

   on those [[tuples]] of elements which match the [[graphs]] of the functions appearing in the diagram:

   $$
     \underset{\longleftarrow}{\lim}_{i} X_i
     \;\simeq\;
     \left\{
       (x_i)_{i \in I} \in \underset{i \in I}{\times} X_i
       \,\vert\,
       \underset{ {i,j \in I} \atop { \alpha \in I_{i,j} } }{\forall}
       \left(
         f_{\alpha}(x_i) = x_j
       \right)
     \right\}
   $$

1. its [[colimit|colimiting co-cone]] (def. \ref{LimitingCone}) exists and is given by the [[quotient set]] of the [[disjoint union]] $\underset{i \in I}{\sqcup} X_i$ of all the [[sets]] $X_i$ appearing in the diagram

   $$
     \underset{i \in I}{\sqcup} X_i
       \,\overset{\phantom{AAA}}{\longrightarrow}\,
     \underset{\longrightarrow}{\lim}_{i \in I} X_i
   $$

   with respect to the [[equivalence relation]] which is generated from the [[graphs]] of the functions in the diagram:

   $$
     \underset{\longrightarrow}{\lim}_i X_i
     \;\simeq\;
     \left(
       \underset{i \in I}{\sqcup} X_i
     \right)/
     \left(
       (x \sim x')
         \Leftrightarrow
       \left(
         \underset{ {i,j \in I} \atop { \alpha \in I_{i,j} } }{\exists}
         \left(
           f_\alpha(x) = x'
         \right)
       \right)
     \right)
   $$

=--

It will turn out below in prop. \ref{DescriptionOfLimitsAndColimitsInTop} that limits and colimits
of diagrams of topological spaces are computed by first applying prop. \ref{SetLimits} to the underlying diagram
of underlying sets, and then equipping the result with a topology as follows:

+-- {: .num_defn #InitialAndFinalTopologies}
###### Definition
**([[initial topology]] and [[final topology]])**

Let $\{X_i = (S_i,\tau_i) \in Top\}_{i \in I}$ be a [[class]] of [[topological spaces]], and let $S \in Set$ be a bare [[set]]. Then

* For $\{S \stackrel{f_i}{\to} S_i \}_{i \in I}$ a set of [[functions]] out of $S$, the _[[initial topology]]_ $\tau_{initial}(\{f_i\}_{i \in I})$ is the topology on $S$ with the [[minimum]] collection of [[open subsets]] such that all $f_i \colon (S,\tau_{initial}(\{f_i\}_{i \in I}))\to X_i$ are [[continuous function|continuous]].

* For $\{S_i \stackrel{f_i}{\to} S\}_{i \in I}$ a set of [[functions]] into $S$, the _[[final topology]]_ $\tau_{final}(\{f_i\}_{i \in I})$ is the topology on $S$ with the [[maximum]] collection of [[open subsets]] such that all $f_i \colon X_i \to (S,\tau_{final}(\{f_i\}_{i \in I}))$ are [[continuous function|continuous]].

Other terminology used is shown in this table:

| $\,$ [[limit]]  of [[topological spaces]]$\,$ | $\,$ [[colimit]] of [[topological spaces]] $\,$ |
|-------------------------------|------------------------------|
| $\,$ [[initial topology]]$\,$ | $\,$ [[final topology]] $\,$ |
| $\,$ weak topology  $\,$     | $\,$ strong  topology $\,$   |
| $\,$ coarse topology  $\,$    | $\,$ fine topology $\,$      |

=--

We have already seen [above](#BasicConstructions) simple examples of initial and final topologies:

+-- {: .num_example #TopologicalSubspaceInitial}
###### Example
**([[subspace topology]] as an [[initial topology]])**

For $X$ a single [[topological space]], and $\iota_S \colon S \hookrightarrow U(X)$ a subset of its underlying set, then the [[initial topology]] $\tau_{intial}(\iota_S)$, def. \ref{InitialAndFinalTopologies}, is the [[subspace topology]] from example \ref{SubspaceTopology}, making

$$
  \iota_S
  \;\colon\;
  (S, \tau_{initial}(\iota_S))
  \hookrightarrow
  X
$$

a [[topological subspace]] inclusion.

=--

+-- {: .num_example #QuotientTopologyFinal}
###### Example
**([[quotient topology]] as a [[final topology]])**

Conversely, for $p_S \colon U(X) \longrightarrow S$ an [[epimorphism]], then the [[final topology]] $\tau_{final}(p_S)$ on $S$,
from def. \ref{InitialAndFinalTopologies}, is the [[quotient topology]] from example \ref{QuotientTopologicalSpace}.

=--

Now we have all the ingredients to compute limits and colimits of diagrams of topological spaces:

+-- {: .num_prop #DescriptionOfLimitsAndColimitsInTop}
###### Proposition
**([limits and colimits of topological spaces](limits+and+colimits+by+example#OfTopologicalSpaces))**

Let

$$
  X_\bullet \;\colon\; \mathcal{I} \longrightarrow Top
$$

be a [[diagram]] of [[topological spaces]] (def. \ref{Diagram}, using the notation from remark \ref{FunctorialDefinitionOfDiagrams}).

1. The [[limit]] of $X_\bullet$ exists and is given by [[generalized the|the]] topological space whose underlying set is [[generalized the|the]] limit in [[Set]] of the underlying sets in the diagram, and whose topology is the [[initial topology]], def. \ref{InitialAndFinalTopologies}, for the functions $p_i$ which are the limiting [[cone]] components:

   $$
     \array{
       && \underset{\longleftarrow}{\lim}_{i \in I} S_i
       \\
       & {}^{\mathllap{p_i}}\swarrow && \searrow^{\mathrlap{p_j}}
       \\
       S_i && \underset{}{\longrightarrow} && S_j
     }
     \,.
   $$

   Hence

   $$
     \underset{\longleftarrow}{\lim}_{i \in I} X_i
     \simeq
     \left(\underset{\longleftarrow}{\lim}_{i \in I} S_i,\; \tau_{initial}(\{p_i\}_{i \in I})\right)
   $$

1. The [[colimit]] of $X_\bullet$ exists and is the topological space whose underlying set is the colimit in [[Set]] of the underlying diagram of sets, and whose topology is the [[final topology]], def. \ref{InitialAndFinalTopologies} for the component maps $\iota_i$ of the colimiting [[cocone]]

   $$
     \array{
       S_i && \longrightarrow && S_j
       \\
       & {}_{\mathllap{\iota_i}}\searrow && \swarrow_{\mathrlap{\iota_j}}
       \\
       && \underset{\longrightarrow}{\lim}_{i \in I} S_i
     }
     \,.
   $$

   Hence

   $$
     \underset{\longrightarrow}{\lim}_{i \in I} X_i
     \simeq
     \left(\underset{\longrightarrow}{\lim}_{i \in I} S_i,\; \tau_{final}(\{\iota_i\}_{i \in I})\right)
   $$

=--

(e.g. [Bourbaki 71, section I.4](#Bourbaki71))

+-- {: .proof}
###### Proof

The required [[universal property]] of $\left(\underset{\longleftarrow}{\lim}_{i \in I} S_i,\; \tau_{initial}(\{p_i\}_{i \in I})\right)$ is immediate: for

$$
  \array{
    && (S,\tau)
    \\
    & {}^{\mathllap{f_i}}\swarrow && \searrow^{\mathrlap{f_j}}
    \\
    X_i && \underset{}{\longrightarrow} && X_i
  }
$$

any [[cone]] over the diagram, then by construction there is a unique function of underlying sets $S \longrightarrow \underset{\longleftarrow}{\lim}_{i \in I} S_i$ making the required diagrams commute, and so all that is required is that this unique function is always [[continuous function|continuous]]. But this is precisely what the initial topology ensures.

The case of the colimit is [[formal dual|formally dual]].

=--

We discuss a list of examples of (co-)limits of topological spaces in a moment [below](#UniversalConstructionsExamples),
but first we conclude with the main theoretical impact of the concept of topological (co-)limits for our our purposes.



+-- {: .num_remark #CoLimitsInNiceTopologicalSpaces}
###### Remark
**(limits and colimits in categories of [[nice topological spaces]])**

Recall from remark \ref{ReflectiveSubcategory} the concept of [[adjoint functors]]

$$
  L \colon \mathcal{C} \leftrightarrow \mathcal{D} \colon R
$$

witnessed by [[natural isomorphisms]]

$$
  Hom_{\mathcal{D}}(L(c),d)
    \simeq
  Hom_{\mathcal{C}}(c,R(d))
  \,.
$$

Observe that with prop. \ref{HomFunctorPreservesLimits} it follows that

1. [[left adjoint functors]] preserve [[colimits]]

1. [[right adjoint fucntors]] preserve [[limits]]

This implies that if we have a [[reflective subcategory]] of topological spaces

$$
  Top_{nice}
    \underoverset
      {\underset{\iota}{\hookrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  Top
$$

(where $Top_{nice}$ is for instance $Top_{T_n}$ for $n \in \{0,1,2\}$ or $Top_{sob}$)

then

1. limits in $Top_{nice}$ are computed as limits in $Top$;

1. colimits in $Top_{nice}$ are computed as the reflection $L$ of the colimit in $Top$.

(...)

=--


$\,$

### Examples
 {#UniversalConstructionsExamples}

We now discuss a list of examples of [[universal constructions]] of [[topological spaces]]
as introduced in generality [above](#UniversalConstructions).

$\,$

[[!include universal constructions of topological spaces -- table]]

$\,$

+-- {: .num_example #PointTopologicalSpaceAsEmptyLimit}
###### Example
**([[empty space]] and [[point space]] as empty [[colimit]] and [[limit]])**

Consider the [[empty diagram]] (example \ref{DiscreteDiagram}) as a diagram of [[topological spaces]].

1. The [[limit]] over the [[empty diagram]] is the [[point space]] $\ast$ (example \ref{Point}).

1. The [[colimit]] over the [[empty diagram]] is the [[empty topological space]] $\emptyset$ (example \ref{Point}).

=--

+-- {: .num_example #DisjointUnionOfTopologicalSpacesIsCoproduct}
###### Example
**(binary [[product topological space]] and [[disjoint union space]] as [[limit]] and [[colimit]])**

Consider a [[discrete category|discrete]] [[diagram]] consisting of two objects $X, Y$ (example \ref{DiscreteDiagram}).

Its [[limit]] is called the _[[Cartesian product]]_ $X \times Y$.

Its [[colimit]] is called the _[[coproduct]]_ $x \sqcup Y$.

In topological spaces this yields the binary product topological space (example \ref{BinaryProductTopologicalSpace})
and the [[disjoint union space]] (example \ref{DisjointUnionOfTopologicalSpaces}).


=--

+-- {: .num_example #InfiniteProductTopologicalSpace}
###### Example
**([[product spaces]] with [[Tychonoff topology]])**

For $\{X_i\}_{i \in I}$ a set of topological spaces, their [[product]] $\underset{i \in I}{\prod} X_i \in Top$ is the [[Cartesian product]] of the underlying sets equipped with the _[[product topology]]_, also called the _[[Tychonoff product]]_.

In the case that $S$ is a [[finite set]], such as for binary product spaces $X \times Y$, then a [[basis for a topology|sub-basis]] for the Tychonoff product topology is given by the [[Cartesian products]] of the open subsets of (a basis for) each factor space.
Hence in this case the Tychonoff topology coincides with that of the binary product space topology in example \ref{BinaryProductTopologicalSpace}.

=--


+-- {: .num_example #EqualizerInTop}
###### Example

The [[equalizer]] of two [[continuous functions]] $f, g \colon X \stackrel{\longrightarrow}{\longrightarrow} Y$ in $Top$ is the equalizer of the underlying functions of sets

$$
  eq(f,g)
   \hookrightarrow
  S_X
    \stackrel{\overset{f}{\longrightarrow}}{\underset{g}{\longrightarrow}}
  S_Y
$$

(hence the largets subset of $S_X$ on which both functions coincide) and equipped with the [[subspace topology]], example \ref{TopologicalSubspace}.

=--


+-- {: .num_example #CoequalizerInTop}
###### Example

The [[coequalizer]] of two [[continuous functions]] $f, g \colon X \stackrel{\longrightarrow}{\longrightarrow} Y$ in $Top$ is the coequalizer of the underlying functions of sets

$$
  S_X
    \stackrel{\overset{f}{\longrightarrow}}{\underset{g}{\longrightarrow}}
  S_Y
    \longrightarrow
  coeq(f,g)
$$

(hence the [[quotient set]] by the [[equivalence relation]] generated by $f(x) \sim g(x)$ for all $x \in X$)  and equipped with the [[quotient topology]], example \ref{QuotientTopology}.

=--

+-- {: .num_example #PushoutInTop}
###### Example

For

$$
  \array{
     A &\overset{g}{\longrightarrow}& Y
     \\
     {}^{\mathllap{f}}\downarrow
     \\
     X
  }
$$

two [[continuous functions]] out of the same [[domain]], then the [[colimit]] under this diagram is also called the _[[pushout]]_, denoted

$$
  \array{
     A &\overset{g}{\longrightarrow}& Y
     \\
     {}^{\mathllap{f}}\downarrow && \downarrow^{\mathrlap{g_\ast f}}
     \\
     X &\longrightarrow& X \sqcup_A Y
     \,.
  }
  \,.
$$

(Here $g_\ast f$ is also called the pushout of $f$, or the _[[base change|cobase change]]_ of $f$ along $g$.) If $g$ is an inclusion, one also write $X \cup_f Y$ and calls this the _[[attaching space]]_.

<div style="float:left;margin:0 10px 10px 0;"><img src="http://ncatlab.org/nlab/files/AttachingSpace.jpg" width="450"></div>

By example \ref{CoequalizerInTop} the [[pushout]]/[[attaching space]] is the [[quotient topological space]]

$$
  X \sqcup_A Y \simeq (X\sqcup Y)/\sim
$$

of the [[disjoint union]] of $X$ and $Y$ subject to the [[equivalence relation]] which identifies a point in $X$ with a point in $Y$ if they have the same pre-image in $A$.

(graphics from [Aguilar-Gitler-Prieto 02](#AguilarGitlerPrieto02))

=--






+-- {: .num_example #TopologicalnSphereIsPushoutOfBoundaryOfnBallInclusionAlongItself}
###### Example

As an important special case of example \ref{PushoutInTop},  let

$$
  i_n \colon S^{n-1}\longrightarrow D^n
$$

be the canonical inclusion of the standard [[n-sphere|(n-1)-sphere]] as the [[boundary]] of the standard [[n-disk]]
from example \ref{SpheresAndDisks}.


<div style="float:left;margin:0 10px 10px 0;">
<img src="http://ncatlab.org/nlab/files/GluingHemispheres.jpg" width="400"></div>

Then the colimit in [[Top]] under the diagram, i.e. the [[pushout]] of $i_n$ along itself,

$$
  \left\{
     D^n \overset{i_n}{\longleftarrow} S^{n-1} \overset{i_n}{\longrightarrow}
     D^n
  \right\}
  \,,
$$

is the [[n-sphere]] $S^n$:

$$
  \array{
    S^{n-1} &\overset{i_n}{\longrightarrow}& D^n
    \\
    {}^{\mathllap{i_n}}\downarrow &(po)& \downarrow
    \\
    D^n &\longrightarrow& S^n
  }
  \,.
$$

(graphics from Ueno-Shiga-Morita 95)

=--



+-- {: .num_defn #SingleCellAttachment}
###### Definition
**(single cell [[space attachment|attachment]])**

For $X$ any [[topological space]] and for $n \in \mathbb{N}$, then an _$n$-cell [[attaching space|attachment]]_ to $X$ is the result of gluing an [[n-disk]] to $X$, along a prescribed image of its bounding [[n-sphere|(n-1)-sphere]] (def. \ref{SpheresAndDisks}):

Let

$$
  \phi \;\colon\; S^{n-1} \longrightarrow X
$$

be a [[continuous function]], then the "[[attaching space]]"

$$
  X \cup_\phi D^n \,\in Top
$$

is the topological space which is the [[pushout]] of the boundary inclusion of the $n$-sphere along $\phi$, hence the universal space that makes the following [[commuting diagram|diagram commute]]:

$$
  \array{
    S^{n-1} &\stackrel{\phi}{\longrightarrow}& X
    \\
    {}^{\mathllap{\iota_n}}\downarrow &(po)& \downarrow
    \\
    D^n &\longrightarrow& X \cup_\phi D^n
  }
  \,.
$$

=--


+-- {: .num_example }
###### Example

A single cell [[attaching space|attachment]] of a 0-cell, according to example \ref{SingleCellAttachment} is the same as forming the [[disjoint union space]] $X \sqcup \ast$ with the [[point]] space $\ast$:

$$
  \array{
     (S^{-1} = \emptyset) &\overset{\exists !}{\longrightarrow}&  X
     \\
     \downarrow &(po)& \downarrow
     \\
     (D^0 = \ast) &\longrightarrow& X \sqcup \ast
  }
  \,.
$$

In particular if we start with the [[empty topological space]] $X = \emptyset$ itself (example \ref{Point}), then by [[attaching space|attaching]] 0-cells we obtain a [[discrete topological space]]. To this then we may attach higher dimensional cells.


=--


+-- {: .num_defn #CellAttachments}
###### Definition
**([[space attachment|attaching]] many cells at once)**


If we have a [[set]] of [[attaching maps]] $\{S^{n_i-1} \overset{\phi_i}{\longrightarrow} X\}_{i \in I}$ (as in def. \ref{SingleCellAttachment}), all to the same space $X$, we may think of these as one single continuous function out of the [[disjoint union space]] of their [[domain]] spheres

$$
  (\phi_i)_{i \in I}
    \;\colon\;
  \underset{i \in I}{\sqcup}
  S^{n_i-1}
   \longrightarrow
  X
  \,.
$$

Then the result of attaching _all_ the corresponding $n$-cells to $X$ is the pushout of the corresponding [[disjoint union]] of boundary inclusions:

$$
  \array{
    \underset{i \in I}{\sqcup} S^{n_i - 1}
      &\overset{(\phi_i)_{i \in I}}{\longrightarrow}&
    X
    \\
    \downarrow
      &(po)&
    \downarrow
    \\
    \underset{i \in I}{\sqcup} D^n
      &\longrightarrow&
    X \cup_{(\phi_i)_{i \in I}} \left(\underset{i \in I}{\sqcup} D^n\right)
  }
  \,.
$$

=--

Apart from attaching a set of cells all at once to a fixed base space, we may "attach cells to cells" in that after forming a given cell attachment, then we further attach cells to the resulting attaching space, and ever so on:

+-- {: .num_defn #RelativeCellComplexes}
###### Definition
**([[relative cell complexes]] and [[CW-complexes]])


Let $X$ be a topological space, then
A _topological [[relative cell complex]]_ of countable height based on $X$ is a [[continuous function]]

$$
  f \colon X \longrightarrow Y
$$

and a [[sequential diagram]] of [[topological space]] of the form

$$
  X = X_0 \hookrightarrow X_1 \hookrightarrow X_2 \hookrightarrow X_3 \hookrightarrow \cdots
$$

such that

1. each $X_k \hookrightarrow X_{k+1}$ is exhibited as a cell attachment according to def. \ref{CellAttachments}, hence presented by a [[pushout]] diagram of the form

   $$
     \array{
       \underset{i \in I}{\sqcup} S^{n_i - 1}
         &\overset{(\phi_i)_{i \in I}}{\longrightarrow}&
       X_k
       \\
       \downarrow
         &(po)&
       \downarrow
       \\
       \underset{i \in I}{\sqcup} D^{n_i}
         &\longrightarrow&
      X_{k+1}
     }
     \,.
   $$

1. $Y = \underset{k\in \mathbb{N}}{\cup} X_k$ is the [[union]] of all these cell attachments, and $f \colon X \to Y$ is the canonical inclusion; or stated more abstractly: the map $f \colon X \to Y$ is the inclusion of the first component of the diagram into its [[colimit|colimiting cocone]] $\underset{\longrightarrow}{\lim}_k X_k$:

   $$
     \array{
       X = X_0 &\longrightarrow& X_1 &\longrightarrow& X_2 &\longrightarrow& \cdots
       \\
       & {}_{\mathllap{f}}\searrow & \downarrow & \swarrow && \cdots
       \\
       && Y = \underset{\longrightarrow}{\lim} X_\bullet
     }
   $$

If here $X = \emptyset$ is the [[empty space]] then the result is a map $\emptyset \hookrightarrow Y$, which is equivalently just a space $Y$ built form "attaching cells to nothing". This is then called just a _topological [[cell complex]]_ of countable hight.

Finally, a topological (relative) cell complex of countable hight is called a **CW-complex** is the $(k+1)$-st cell attachment $X_k \to X_{k+1}$ is entirely by $(k+1)$-cells, hence exhibited specifically by a pushout of the following form:

$$
  \array{
    \underset{i \in I}{\sqcup} S^{k}
      &\overset{(\phi_i)_{i \in I}}{\longrightarrow}&
    X_k
    \\
    \downarrow
      &(po)&
    \downarrow
    \\
    \underset{i \in I}{\sqcup} D^{k+1}
      &\longrightarrow&
    X_{k+1}
  }
  \,.
$$

A _[[finite CW-complex]]_ is one which admits a presentation in which there are only finitely many attaching maps, and similarly a _countable CW-complex_ is one which admits a presentation with countably many attaching maps.

Given a CW-complex, then $X_n$ is also called its $n$-[[skeleton]].

=--





## Compact spaces
 {#CompactSpaces}


From the discussion of [[compact topological space|compact]] [[metric spaces]] in
def. \ref{MetricSpaceSequentiallyCompact} and prop. \ref{CompactnessImpliedBySequentialCompactnessForMetricSpace}
it immediate how to generalize the concept to [[topological spaces]]
to obtain a notion of _[[compact topological spaces]]_ (def. \ref{SequentiallyCompactTopologicalSpace}
and def. \ref{CompactTopologicalSpace} below). These compact spaces play a special role in [[topology]],
much like [[finite dimensional vector spaces]] do in [[linear algebra]].


The most naive version of the definition directly generalizes the concept via converging
sequences from def. \ref{MetricSpaceSequentiallyCompact}:

+-- {: .num_defn #TopologicalSpaceSequeneConverging}
###### Definition
**(converging sequence in a topological space)**

Let $(X,\tau)$ be a [[topological space]] (def. \ref{TopologicalSpace}) and let
$(x_n)_{n \in \mathbb{N}}$ be a [[sequence]] of points $(x_n)$ in $X$ (def. \ref{Sequences}).
We say that this sequence _[[convergence|converges]]_ in $(X,\tau)$ to a point $x_\infty \in X$,
denoted

$$
  x_n \overset{n \to \infty}{\longrightarrow} x_\infty
$$

if for each open [[neighbourhood]] $U_{x_\infty}$ of $x_\infty$ there exists a $k \in \mathbb{N}$ such that
for all $n \geq k$ then $x_n \in U_{x_\infty}$:

$$
  \left(
    x_n \overset{n \to \infty}{\longrightarrow} x_\infty
  \right)
   \;\Leftrightarrow\;
  \underset{{U_{x_\infty} \in \tau_X} \atop {x_\infty \in U_{X_\infty}}}{\forall}
  \left(
    \underset{k \in \mathbb{N}}{\exists}
    \left(
      \underset{n \geq k}{\forall}
        \, x_n \in U_{x_\infty} \,
    \right)
  \right)
  \,.
$$

=--

+-- {: .num_defn #SequentiallyCompactTopologicalSpace}
###### Definition
**([[sequentially compact topological space]])**

Let $(X,\tau)$ be a [[topological space]] (def. \ref{TopologicalSpace}). It is called
_[[sequentially compact topological space|sequentially compact]]_ if for every [[sequence]]
of points $(x_n)$ in $X$ (def. \ref{Sequences}) there exists a sub-sequence $(x_{n_k})_{k \in \mathbb{N}}$
which [[convergence|converges]] acording to def. \ref{TopologicalSpaceSequeneConverging}.

=--

But prop. \ref{CompactnessImpliedBySequentialCompactnessForMetricSpace} suggests to consider
also another definition of compactness for topological spaces:

+-- {: .num_defn #OpenCover}
###### Definition
**([[open cover]])**

An _[[open cover]]_ of a [[topological space]] $X$ (def. \ref{TopologicalSpace})
is a [[set]] $\{U_i \subset X\}_{i \in I}$ of [[open subsets]] $U_i$ of $X$,
indexed by some [[set]] $I$, such that their [[union]] is all of $X$:

$$
  \underset{i \in I}{\cup} U_i \;=\; X
  \,.
$$

=--

+-- {: .num_defn #CompactTopologicalSpace}
###### Definition
**([[compact topological space]])**

A [[topological space]] $X$ (def. \ref{TopologicalSpace}) is called a
 _[[compact topological space]]_ if every [[open cover]] $\{U_i \to X\}_{i \in I}$ (def. \ref{OpenCover}) has
 a _finite subcover_ in that there is a [[finite set|finite]] [[subset]] $J \subset I$ such that
 $\{U_i \to X\}_{i \in J}$ is still a cover of $X$ in that  $\underset{i \in J}{\cup} U_i = X$.

=--

+-- {: .num_remark #CompactTerminology}
###### Remark
**(terminology issue regarding "compact")**

Beware that the following terminology issue persists in the literature:

Some authors use "compact" to mean "[[compact Hausdorff space|Hausdorff and compact]]". To disambiguate this,
some authors (mostly in [[algebraic geometry]], but also for instance [Waldhausen](#Waldhausen)) say "quasi-compact" for what we call
"compact" in prop. \ref{CompactTopologicalSpace}.

=--

There are several equivalent reformulation of the compactness condition:

+-- {: .num_prop #ClosedSubsetFormulationOfCompactness}
###### Proposition
**([[compact topological space|compactness]] in terms of closed subsets)**

Let $(X,\tau)$ be a [[topological space]]. Then the following are equivalent:

1. $(X,\tau)$ is [[compact topological space|compact]] in the sense of def. \ref{CompactTopologicalSpace}.

1. Let $\{C_i \subset X\}_{i \in I}$ be a set of [[closed subsets]] (def. \ref{ClosedSubset}) such that their [[intersection]]
   is [[empty set|empty]] $\underset{i \in I}{\cap} C_i = \emptyset$, then there is a [[finite set|finite]] [[subset]]
   $J \subset I$ such that the corresponding finite intersection is still empty $\underset{i \in  J \subset i}{\cap} C_i = \emptyset$.

1. Let $\{C_i \subset X\}_{i \in I}$ be a set of [[closed subsets]] (def. \ref{ClosedSubset}) such that it enjoys the
   _[[finite intersection property]]_, meaning that for every [[finite set|finite]] [[subset]] $J \subset I$ then
   the corresponding finite intersection is [[inhabited set|non-empty]] $\underset{i \in J \subset I}{\cap} C_i \neq \emptyset$.
   Then also the total intersection is [[inhabited set|non-empty]], $\underset{i \in I}{\cap} C_i \neq \emptyset$.

=--

+-- {: .proof}
###### Proof

The equivalence between the first and the second statement is immediate by [[de Morgan's law]] (remark \ref{deMorgan}).
The equivalence between the first and the third proceeds similarly, via a [[proof by contradiction]].

=--

+-- {: .num_example }
###### Example
**(finite discrete spaces are compact)**

A [[discrete topological space]] (def. \ref{CoDiscreteTopology}) is [[compact topological space|compact]] (def. \ref{CompactTopologicalSpace})
precisely if its underlying set is [[finite set|finite]].

=--

+-- {: .num_example #CompactClosedInterval}
###### Example
**(closed intervals are compact)**

For any $a \lt b \in \mathbb{R}$ the [[closed interval]] (example \ref{OpenAndClosedIntervals})

$$
  [a,b] \subset \mathbb{R}
$$

regarded with its [[topological subspace|subspace topology]] is a [[compact topological space]] (def. \ref{CompactTopologicalSpace}).

=--

+-- {: .proof}
###### Proof

Since all the closed intervals are [[homeomorphism|homeomorphic]] (by example \ref{OpenBallsHomeomorphicToRn})
it is sufficient to show the statement for $[0,1]$. Hence let $\{U_i \subset [0,1]\}_{i \in I}$ be an
open cover. We need to show that it has an open subcover.

Say that an element $x \in [0,1]$ is _admissible_ if the closed sub-interval $[0,x]$ is covered by
finitely many of the $U_i$. In this terminlogy, what we need to show is that $1$ is admissible.

Observe from the definition that

1. 0 is admissible,

1. if $y \lt x \in [0,1]$ and $x$ is admissible, then also $y$ is admissible.

This means that the set of admissible $x$ forms either an [[open interval]] $[0,g)$ or a [[closed interval]]
$[0,g]$, for some $g \in [0,1]$. We need to show that the latter is true, and for $g = 1$.
We do so by observing that the alternatives lead to contradictions:

1. Assume that the set of admissible values were an open interval $[0,g)$. By assumption there would be
   a finite subset $J \subset I$ such that $\{U_i \subset [0,1] \}_{i \in J \subset I}$ were a finite
   open cover of $[0,g)$. Accordingly, since there is some $i_g \in I$ such that $g \in U_{i_g}$, the union
   $\{U_i\}_{i \in J } \sqcup \{U_{i_g}\}$ were a finite cover of the closed interval $[0,g]$,
   contradicting the assumption that $g$ itself is not admissible (since it is not contained in $[0,g)$).

1. Assume that the set of admissible values were a closed interval $[0,g]$ for $g \lt 1$.
   By assumption there would then be a finite set $J \subset I$ such that $\{U_i \subset [0,1]\}_{i \in J \subset I}$
   were a finite cover of $[0,g]$. Hence there would be an index $i_g \in J$ such that $g \in U_{i_g}$.
   But then by the nature of open subsets in the Euclidean space $\mathbb{R}$, this $U_{i_g}$ would also
   contain an open ball $B^\circ_g(\epsilon) = (g-\epsilon, g + \epsilon)$. This would mean that
   the set of admissible values includes the open interval $[0,g+ \epsilon)$, contradicting the assumption.

This gives a [[proof by contradiction]].

=--



+-- {: .num_prop #BinaryTychonoffTheorem}
###### Proposition
**(binary [[Tychonoff theorem]])**

Let $(X,\tau_X)$ and $(Y,\tau_Y)$ be two [[compact topological spaces]] (def. \ref{CompactTopologicalSpace}).
Then also their [[product topological space]] (def. \ref{BinaryProductTopologicalSpace}) $(X \times Y, \tau_{X \times Y})$ is compact.

=--

+-- {: .proof}
###### Proof

Let $\{ U_i \subset X \times Y \}_{i \in I}$ be an [[open cover]] of the product space. We need to show that
this has a finite subcover.

By definition of the product space topology, each $U_i$ is the union, indexed by some set $K_i$, of [[Cartesian products]]
of open subsets of $X$ and $Y$:

$$
  U_i
    \;=\;
  \underset{k_i \in K_i}{\cup} \left(
     V_{k_i} \times W_{k_i}
  \right)
  \phantom{AAAA}
  V_{k_i} \in \tau_{X} \,\phantom{A}\text{and} \phantom{A}\, W_{k_i} \in \tau_{Y}
  \,.
$$

Consider then the [[disjoint union]] of all these index sets

$$
   K
    \,\coloneqq\,
  \underset{i \in I}{\sqcup}
  K_i
  \,.
$$

This is such that

$$
  (\star)
  \phantom{AA}
  \left\{
    V_{k_i} \times W_{k_i}
      \subset
    X \times Y
  \right\}_{k_i \in K}
$$

is again an open cover of $X \times Y$.

But by construction, each element $V_{k_i} \times W_{k_i}$ of this new cover is contained in at least one
$U_{j(k_i)}$ of the original cover.
Therefore it is now sufficient to show that there is
a finite subcover of $(\star)$, consisting of elements indexed by $k_i \in K_{fin} \subset K$ for some
[[finite set]] $K_{fin}$. Because then the corresponding $U_{j(k_i)}$ for $k_i \in K_{fin}$ form a finite subcover
of the original cover.

In order to see that $(\star)$ has a finite subcover, first fix a point $x \in X$ and
write $\{x\} \subset X$ for the corresponding [[singleton]] [[topological subspace]].
By example \ref{ConcreteAndAbstractPoint} this is [[homeomorphism|homeomorphic]] to the abstract
[[point space]] $\ast$.
By example \ref{CartesianSymmetricMonoidalTop} there is thus a [[homeomorphism]] of the form

$$
  \{x\} \times Y \simeq Y
  \,.
$$

Therefore, since $(Y,\tau_Y)$ is assumed to be [[compact topological space|compact]], the open cover

$$
  \left\{
    \left(
      (V_{k_1} \times W_{k_1}) \cap (\{x\} \times Y)
    \right)
      \;\subset\;
    \{x\}\times Y
  \right\}_{k_i \in K}
$$

has a finite subcover, indexed by a [[finite set|finite]] [[subset]] $J_x \subset K$.

Here we may assume without restriction of generality that $x \in V_{k_i}$ for all $k_i \in J_x \subset K$,
because if not then we may simply remove that index and still have a (finite) subcover.

By finiteness of $J_x$ it now follows that the intersection

$$
  V_x
    \;\coloneqq\;
  \underset{k_i \in J_x}{\cap} V_{k_i}
$$

is still an open subset, and by the previous remark we may assume without restriction that

$$
  x \in V_x
  \,.
$$

Now observe that by the nature of the above cover of $\{x\} \times Y$ we have

$$
  \{x\} \times Y
    \subset
  \underset{k_i \in J_x \subset K}{\cup}  V_{k_i} \times W_{k_i}
$$

and hence

$$
  \{x\} \times Y \subset \{x\} \times \underset{k_i \in J_x \subset K}{\cup} W_{k_i}
  \,.
$$

Since by construction $V_x \subset V_{k_i}$ for all $k_i \in J_x \subset K$, it follows
that we have found a finite cover not just of $\{x\} \times Y$ but of $V_x \times Y$

$$
  V_x \times Y
    \subset
  \underset{k_i \in J_x \subset K}{\cup} \left( V_{k_i} \times W_{k_i} \right)
  \,.
$$

To conclude, observe  that $\{V_x \subset X\}_{x \in X}$ is clearly an open cover of $X$,
so that by the assumption that also $X$ is compact there is a finite set of points $S \subset X$
so that $\{V_x \subset X\}_{x \in S \subset X}$ is still a cover.
In summary then

$$
  \left\{
    V_{k_i} \times W_{k_i}
    \subset X \times Y
  \right\}_{{x \in S \subset X} \atop { k_i \in J_x \subset K }}
$$

is a finite subcover as required.


=--

In terms of the topological incarnation of the definitions of compactness, the familiar statement about metric spaces from prop. \ref{CompactnessImpliedBySequentialCompactnessForMetricSpace} now equivalently says the following:


+-- {: .num_prop #SequentiallyCompactMetricSpacesAreEquivCompact}
###### Proposition
**([[sequentially compact metric spaces are equivalently compact metric spaces]])**

If $(X,d)$ is a [[metric space]], regarded as a [[topological space]] via its [[metric topology]] (example \ref{MetricTopology}), then the following are equivalent:

1. $(X,d)$ is a [[compact topological space]] (def. \ref{CompactTopologicalSpace}).

1. $(X,d)$ is a [[sequentially compact topological space]] (def. \ref{SequentiallyCompactTopologicalSpace}).

=--

+-- {: .proof #ProofOfSequentiallyCompactMetricSpacesAreEquivCompact}
###### Proof
of prop. \ref{CompactnessImpliedBySequentialCompactnessForMetricSpace} and  prop. \ref{SequentiallyCompactMetricSpacesAreEquivCompact}

Assume first that $(X,d)$ is a [[compact topological space]]. Let $(x_k)_{k \in \mathbb{N}}$ be a [[sequence]] in $X$. We need to show that it has a sub-sequence which [[convergence|converges]].

Consider the [[topological closures]] of the sub-sequences that omit the first $n$ elements of the sequence

$$
  F_n
   \;\coloneqq\;
  Cl(\left\{
    x_k \,\vert\, k \geq n
  \right\})
$$

and write

$$
  U_n \coloneqq X \backslash F_n
$$

for their [[open subset|open]] [[complements]].

Assume now that the [[intersection]] of all the $F_n$ were [[empty set|empty]]

$$
  (\star)
  \phantom{AA}
  \underset{n \in \mathbb{N}}{\cap} F_n \;= \; \emptyset
$$

or equivalently that the [[union]] of all the $U_n$ were all of $X$

$$
  \underset{n \in \mathbb{N}}{\cup} U_n
  \;=\;
  X
  \,,
$$

hence that $\{U_n \to X\}_{n \in \mathbb{N}}$ were an [[open cover]]. By the assumption that $X$ is compact, this would imply that there is a [[finite set|finite]] [[subset]] $\{i_1 \lt i_2 \lt  \cdots \lt i_k\} \subset \mathbb{N}$ with

$$
  \begin{aligned}
    X & = U_{i_1} \cup U_{i_2} \cup \cdots \cup U_{i_k}
    \\
    & = U_{i_k}
  \end{aligned}
  \,.
$$

This in turn would mean that $F_{i_k} = \empty$, which contradicts the construction of $F_{i_k}$. Hence we have a [[proof by contradiction]] that assumption $(\ast)$ is wrong, and hence that there must exist an element

$$
  x \in \underset{n \in \mathbb{N}}{\cap} F_n
  \,.
$$

By definition of [[topological closure]] this means that for all $n$ the [[open ball]] $B^\circ_x(1/(n+1))$ around $x$ of [[radius]] $1/(n+1)$ must intersect the $n$th of the above subsequence:

$$
  B^\circ_x(1/(n+1))
  \,\cap\,
  \{x_k \,\vert\, k \geq n \}
  \;\neq\;
  \emptyset
  \,.
$$

Picking one point $(x'_n)$ in the $n$th such intersection for all $n$ hence defines a sub-sequence, which converges to $x$.

This proves that compact implies sequentially compact for metric spaces.

For the converse, assume now that $(X,d)$ is sequentially compact. Let $\{U_i \to X\}_{i \in I}$ be an [[open cover]] of $X$. We need to show that there exists a finite sub-cover.

Now by the [[Lebesgue number lemma]], there exists a positive real number $\delta \gt 0$ such that for each $x \in X$ there is $i_x \in I$ such that $B^\circ_x(\delta) \subset U_{i_x}$.
Moreover, since [[sequentially compact metric spaces are totally bounded]], there exists then  a [[finite set]] $S \subset X$ such that

$$
   X
     \;=\;
   \underset{s \in S}{\cup}
   B^\circ_s(\delta)
   \,.
$$

Therefore $\{U_{i_s} \to X\}_{s \in S}$ is a finite sub-cover as required.

=--

+-- {: .num_remark}
###### Remark
**(neither compactness nor sequential compactness implies the other)**

Beware that, in contrast to prop. \ref{SequentiallyCompactMetricSpacesAreEquivCompact}, for
general topological spaces being [[sequentially compact space|sequentially compact]] neither implies nor is implied by being
[[compact topological space|compact]]. The corresponding counter-examples are maybe beyond the scope of this
note, but see for instance [Vermeeren 10, prop. 17 and prop. 18](sequentially+compact+topological+space#Vermeeren10).

=--

$\,$

In [[analysis]], the [[extreme value theorem]] asserts that a [[real number|real]]-valued [[continuous function]]
on the [[bounded subset|bounded]] [[closed interval]] (def. \ref{OpenAndClosedIntervals}) attains its
[[maximum]] and [[minimum]]. The following is the generalization of this statement to general topological spaces:

+-- {: .num_lemma #ContinuousSurjectionOutOfCompactSpaceHasCompactCodomain}
###### Lemma
**([[continuous surjections out of compact spaces have compact codomain]])**

Let $f \colon (X,\tau_X) \longrightarrow (Y,\tau_Y)$ be a [[continuous function]] between [[topological spaces]] such that

1. $(X,\tau_X)$ is a [[compact topological space]];

1. $f \colon X \to Y$ is a [[surjective function]].

Then also $(Y,\tau_Y)$ is [[compact topological space|compact]].

=--

+-- {: .proof}
###### Proof

Let $\{U_i \subset Y\}_{i \in I}$ be an [[open cover]] of $Y$. We need show that this has a finite sub-cover.

By the continuity of $f$ the [[pre-images]] $f^{-1}(U_i)$ are [[open subsets]] of $X$, and by the surjectivity of $f$ they form an [[open cover]] $\{f^{-1}(U_i) \subset X\}_{i \in I}$ of $X$. Hence by compactness of $X$, there exists a [[finite set|finite]] [[subset]] $J \subset I$ such that
$\{f^{-1}(U_i) \subset X\}_{i \in J \subset I}$ is still an open cover of $X$. Finall, using again that $f$ is assumed to be surjective, it follows that

$$
  \begin{aligned}
    Y
      & = f(X)
    \\
      & = f\left( \underset{i \in J}{\cup} f^{-1}(U_i) \right)
    \\
      & = \underset{i \in J}{\cup} U_i
  \end{aligned}
$$

which means that also $\{U_i \subset Y\}_{i \in J \subset I}$ is still an open cover of $Y$, and in particular a finite subcover of the original cover.

=--


+-- {: .num_cor #ContinuousImageOfACompactSpaceIsCompact}
###### Corollary
**([[continuous images of compact spaces are compact]])**

If $f \colon X \longrightarrow Y$ is a [[continuous function]] out of a [[compact topological space]] $X$ which is not necessarily [[surjective function|surjective]], then we may consider its [[image factorization]]

$$
  f \;\colon\; X \longrightarrow f(X) \hookrightarrow Y
$$

as in example \ref{ImageFactorization}. Now by construction $X \to f(X)$ is surjective, and so lemma \ref{ContinuousSurjectionOutOfCompactSpaceHasCompactCodomain} implies that $f(X)$ is compact.

=--

The converse to cor. \ref{ContinuousImageOfACompactSpaceIsCompact} does not hold in general: the
pre-image of a compact subset under a continuous function need not be compact again. If this is
the case, then we speak of _[[proper maps]]_:

+-- {: .num_defn #ProperContinuous}
###### Definition
**([[proper maps]])**

A [[continuous function]] $f  \colon (X, \tau_X) \to (Y, \tau_Y)$
is called _[[proper map|proper]]_ if for $C \in Y$ a [[compact topological space|compact]] [[topological subspace]]
of $Y$, then also its [[pre-image]] $f^{-1}(C)$ is [[compact topological space|compact]] in $X$.

=--


There are various variants of the concept of compact spaces.

+-- {: .num_defn #LocallyCompactSpace}
###### Definition
**([[locally compact topological space]])**

A [[topological space]] is called _[[locally compact topological space|locally compact]]_
if every point has a [[neighbourhood]] which is [[compact topological space|compact]] (def. \ref{CompactTopologicalSpace}).

=--

+-- {: .num_remark}
###### Remark
**(terminology issue regarding "locally compact")**

On top of the terminology issue inherited from that of "compact" (remark \ref{CompactTerminology}),
the definition of "locally compact" is subject to further ambiguity in the literature.
There are various definitions of locally compact spaces alternative to def. \ref{LocallyCompactSpace}.
For [[Hausdorff topological spaces]] all thse definitions used
happen to be equivalent, but in general they are not.
The version we state in def. \ref{LocallyCompactSpace} is the one that makes prop. \ref{ExponentialObjectCompactOpen}
below work _without_ requiring the Hausdorff property.

=--



+-- {: .num_defn #CompactOpenTopology}
###### Definition
**([[mapping space]] with [[compact-open topology]])**

For $X$ a [[topological space]] and $Y$ a [[locally compact topological space]] (def. \ref{LocallyCompactSpace})
then the **[[mapping space]]**

$$
  \left(
    X^Y , \tau_{(X^Y)}
  \right)
$$

is the [[topological space]]

* whose underlying set $X^Y$ is the set of [[continuous functions]] $Y \to X$,

* whose topology $\tau_{(X^Y)}$ is generated from the [[topological basis|sub-basis for the topology]] (def. \ref{TopologyBase})
  which is given by subsets denoted

  $U^K \subset Hom_{Top}(Y,X)$ for

  * $K \hookrightarrow Y$ a [[compact topological space|compact]] subset

  * $U \hookrightarrow X$ an [[open subset]]

  and defined to be those subsets of all those [[continuous functions]] $f$ that fit into a [[commuting diagram]] of the form

  $$
    \array{
       K &\hookrightarrow& Y
       \\
       \downarrow && \downarrow^{\mathrlap{f}}
       \\
       U &\hookrightarrow& X
    }
    \,.
  $$

Accordingly this $\tau_{(X^Y)}$ is called the _[[compact-open topology]]_ on the set of functions.

The construction extends to a [[functor]]

$$
  (-)^{(-)} \;\colon\; Top_{lcomp}^{op} \times Top \longrightarrow Top
  \,.
$$

=--

+-- {: .num_prop #ExponentialObjectCompactOpen}
###### Proposition

For $X$ a [[topological space]] and $Y$ a [[locally compact topological space]],
then then [[mapping space]] $X^Y$ with its [[compact-open topology]] from def. \ref{CompactOpenTopology}
is an [[exponential object]] in [[Top]].

=--



$\,$



### Relation to Hausdorff spaces

We discuss some important relations between the concepts of compact spaces and of [[Hausdorff topological spaces]].




+-- {: .num_prop}
###### Proposition
**([[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]])**

Let $(X,\tau)$ be a [[compact topological space|compact]] [[Hausdorff topological space]]
(def. \ref{HausdorffTopologicalSpace}, def. \ref{CompactTopologicalSpace}) and let $Y \subset X$
be a [[topological subspace]]. Then the following are equivalent:

1. $Y \subset X$ is a [[closed subspace]] (def. \ref{ClosedSubset});

1. $Y$ is a [[compact topological space]].

=--

+-- {: .proof}
###### Proof

By  lemma \ref{ClosedSubsetsOfCompactSpacesAreCompact} and lemma \ref{CompactSubspacesOfHausdorffSpacesAreClosed}
below.

=--


+-- {: .num_lemma #ClosedSubsetsOfCompactSpacesAreCompact}
###### Lemma
**([[closed subspaces of compact spaces are compact]])**

Let $(X,\tau)$ be a [[compact topological space]] (def. \ref{CompactTopologicalSpace}), and let $Y \subset X$ be a
[[closed subspace|closed]] [[topological subspace]]. Then also $Y$ is [[compact topological space|compact]].

=--

+-- {: .proof}
###### Proof

Let $\{V_i \subset Y\}_{i \in I}$ be an [[open cover]] of $Y$. We need to show that this has a finite sub-cover.

By definition of the [[topological subspace|subspace topology]], there exist open subsets $U_i$ of $X$ with

$$
  V_i = U_i \cap Y
  \,.
$$

By the assumption that $Y$ is closed, the [[complement]] $X \backslash Y$ is an open subset of $X$, and therefore

$$
  \{ X \backslash Y \subset X\} \cup \{ U_i \subset X \}_{i \in I}
$$

is an [[open cover]] of $X$. Now by the assumption that $X$ is compact, this latter cover has a finite subcover,
hence there exists a [[finite set|finite]] [[subset]] $J \subset I$ such that

$$
  \{ X \backslash Y \subset X\} \cup \{ U_i \subset X \}_{i \in J \subset I}
$$

is still an oopen cover of $X$, hence in particular intersects to a finite open cover of $Y$.
But since $Y \cap ( X \backsalsh Y ) = \empty$, it follows that indeed

$$
  \{V_i \subset Y\}_{i \in J \subset I}
$$

is a cover of $Y$, and in indeed a finite subcover of the original one.

=--

+-- {: .num_lemma #SeparationByNeighbourhoodsOfPointsFromCompactSubsetsInHausdorffSpaces}
###### Lemma
**(separation by neighbourhoods of points from compact subspaces in Hausdorff spaces)**

Let

1. $(X,\tau)$ be a [[Hausdorff topological space]];

1. $Y \subset X$ a [[compact topological space|compact]] [[subspace]].


Then for every $x \in X \backslash Y$ there exists

1. an [[open neighbourhood]] $U_x \supset \{x\}$;

1. an open neighbourhood $U_Y \supset Y$

such that

* they are still disjoint: $U_x \cap U_Y = \emptyset$.

=--

+-- {: .proof}
###### Proof

By the assumption that $(X,\tau)$ is Hausdorff, we find for every point $y \in Y$ disjoint open neighbourhoods $U_{x,y} \supset \{x\}$ and $U_y \supset \{y\}$. By the nature of the [[subspace topology]] of $Y$, the restriction of all the $U_y$ to $Y$ is an [[open cover]] of $Y$:

$$
  \left\{
    (U_y \cap Y) \subset Y
  \right\}_{y \in Y}
  \,.
$$

Now by the assumption that $Y$ is compact, there exists a finite subcover, hence a [[finite set]] $S \subset Y$ such that

$$
  \left\{
    (U_y \cap Y) \subset Y
  \right\}_{y \in S \subset Y}
$$

is still a cover.

But the finite intersection

$$
  U_x \coloneqq \underset{s \in S \subset Y}{\cap} U_{x,s}
$$

of the corresponding open neighbourhoods of $x$ is still open, and by construction it is disjoint from all the $U_{s}$, hence in particular from their union

$$
  U_Y \coloneqq \underset{s \in S \subset Y}{\cup}  U_s
  \,.
$$


Therefore $U_x$ and $U_Y$ are two open subsets as required.

=--

Lemma \ref{SeparationByNeighbourhoodsOfPointsFromCompactSubsetsInHausdorffSpaces} immediately implies the following:

+-- {: .num_lemma #CompactSubspacesOfHausdorffSpacesAreClosed}
###### Lemma
**([[compact subspaces of Hausdorff spaces are closed]])**

Let $(X,\tau)$ be a [[Hausdorff topological space]] (def. \ref{HausdorffTopologicalSpace})
and let $C \subset X$ be a [[compact topological space|compact]] (def. \ref{CompactTopologicalSpace})
[[topological subspace]] (example \ref{SubspaceTopology}). Then $C \subset X$ is also a [[closed subspace]] (def. \ref{ClosedSubset}).

=--

+-- {: .proof}
###### Proof

Let $x \in X \backslash C$ be any point of $X$ not contained in $C$. We need to show that there exists an [[open neighbourhood]] of $x$ in $X$ which does not [[intersection|intersect]] $C$.
This is implied by lemma \ref{SeparationByNeighbourhoodsOfPointsFromCompactSubsetsInHausdorffSpaces}.

=--


+-- {: .num_prop #BorelHeine}
###### Proposition
**([[Heine-Borel theorem]])**

For $n \in \mathbb{N}$, regard $\mathbb{R}^n$ as the $n$-dimensional [[Euclidean space]] via example \ref{EuclideanNorm},
regarded as a [[topological space]] via its [[metric topology]] (example \ref{MetricTopology}).

Then for a [[topological subspace]] $S \subset \mathbb{R}^n$ the following are equivalent:

1. $S$ is  [[compact topological space|compact]] (def. \ref{CompactTopologicalSpace});

1. $S$ is [[closed subset|closed]] (def. \ref{ClosedSubset}) and [[bounded subset|bounded]] (def. \ref{MetricSpaceBoundedSubset}).

=--

+-- {: .proof #BorelHeineProof}
###### Proof

First consider a [[subset]] $S \subset \mathbb{R}^n$ which is closed and bounded. We need to show that
regarded as a [[topological subspace]] it is [[compact topological space|compact]].

The assumption that $S$ is bounded by (hence contained in) some [[open ball]] $B^\circ_x(\epsilon)$ in $\mathbb{R}^n$
implies that it is contained in $\{ (x_i)_{i = 1}^n \in \mathbb{R}^n \,\vert\, -\epsilon \leq x_i \leq \epsilon \}$.
By example \ref{ClosedIntervalsProduct}, this  topological subspace is homeomorphic to the $n$-cube
$[-\epsilon, \epsilon]^n$. Since the closed interval $[-\epsilon, \epsilon]$
is compact by example \ref{CompactClosedInterval}, the binary [[Tychonoff theorem]] (prop. \ref{BinaryTychonoffTheorem})
implies that this $n$-cube is compact. Since [[closed subspaces of compact spaces are compact]]
(lemma \ref{ClosedSubsetsOfCompactSpacesAreCompact}) this implies that $S$ is compact.

Conversely, assume that $S \subset \mathbb{R}^n$ is a compact subspace. We need to show that it is closed and bounded.

The first statement follows since
the [[Euclidean space]] $\mathbb{R}^n$ is [[Hausdorff topological space|Hausdorff]] (example \ref{HausdorffMetricSpace})
and since [[compact subspaces of Hausdorff spaces are closed]] (prop. \ref{CompactSubspacesOfHausdorffSpacesAreClosed}).

Hence what remains is to show that $S$ is bounded.

To that end, choose any [[positive number|positive]] [[real number]] $\epsilon \in \mathbb{R}_{\gt 0}$
and consider the [[open cover]] of all of $\mathbb{R}^n$ by the open [[n-cubes]]

$$
  (k_1-\epsilon, k_1+1+\epsilon)
    \times
  (k_2-\epsilon, k_2+1+\epsilon)
    \times
      \cdots
    \times
  (k_n-\epsilon, k_n+1+\epsilon)
$$

for [[n-tuples]] of [[integers]] $(k_1, k_2 , \cdots, k_n ) \in \mathbb{Z}^n$.
The restrictions of these to $S$ hence form an open cover of the subspace $S$. By the assumption that
$S$ is compact, there is then a finite subset of $n$-tuples of integers such that the
corresponding $n$-cubes still cover $S$. But the union of any finite number of bounded closed $n$-cubes
in $\mathbb{R}^n$ is clearly a bounded subset, and hence so is $S$.


=--



+-- {: .num_prop #MapsFromCompactSpacesToHausdorffSpacesAreClosed}
###### Proposition
**([[maps from compact spaces to Hausdorff spaces are closed and proper]])**

Let $f \colon (X, \tau_X) \longrightarrow (Y, \tau_Y)$ be a [[continuous function]] between [[topological spaces]] such that

1. $(X,\tau_X)$ is a [[compact topological space]];

1. $(Y,\tau_Y)$ is a [[Hausdorff topological space]].

Then $f$ is

1. a [[closed map]] (def. \ref{OpenMap});

1. a [[proper map]] (def. \ref{ProperContinuous}).)

=--

+-- {: .proof}
###### Proof

For the first statement, we need to show that if $C \subset X$ is a [[closed subset]] of $X$, then also $f(C) \subset Y$ is a closed subset of $Y$.

Now

1. since [[closed subsets of compact spaces are compact]] (lemma \ref{ClosedSubsetsOfCompactSpacesAreCompact}) it follows that $C \subset X$ is also compact;

1. since [[continuous images of compact spaces are compact]] (cor. \ref{ContinuousImageOfACompactSpaceIsCompact}) it then follows that $f(C) \subset Y$ is compact;

1. since [[compact subspaces of Hausdorff spaces are closed]] (prop. \ref{CompactSubspacesOfHausdorffSpacesAreClosed}) it finally follow that $f(C)$ is also closed in $Y$.

For the second statement we need to show that if $C \subset Y$ is a [[compact topological space|compact subset]], then also its [[pre-image]] $f^{-1}(C)$ is compact.

Now

1. since [[compact subspaces of Hausdorff spaces are closed]] (prop. \ref{CompactSubspacesOfHausdorffSpacesAreClosed}) it follows that $C \subse Y$ is closed;

1. since [[pre-images]] under continuous of closed subsets are closed (prop. \ref{ClosedSubsetContinuity}), also $f^{-1}(C) \subset X$ is closed;

1. since [[closed subsets of compact spaces are compact]] (lemma \ref{ClosedSubsetsOfCompactSpacesAreCompact}), it follows that $f^{-1}(C)$ is compact.

=--


+-- {: .num_prop #ContinuousBijectionsFromCompactSpacesToHausdorffSpacesAreHomeomorphisms}
###### Proposition ######
**([[continuous bijections from compact spaces to Hausdorff spaces are homeomorphisms]])**

Let $f \colon (X, \tau_X) \longrightarrow (Y, \tau_Y)$ be a [[continuous function]] between [[topological spaces]] such that

1. $(X,\tau_X)$ is a [[compact topological space]];

1. $(Y,\tau_Y)$ is a [[Hausdorff topological space]].

1. $f \;\colon\; X \longrightarrow Y$ is a [[bijection]] of [[sets]].

Then $f$ is a [[homeomorphism]], i. e. its [[inverse function]] $Y \to X$ is also a [[continuous function]].

In particular then both $(X,\tau_X)$ and $(Y, \tau_Y)$ are [[compact Hausdorff spaces]].

=--

+-- {: .proof}
###### Proof

Write $g \colon Y \to X$ for the [[inverse function]] of $f$.

We need to show that $g$ is continuous, hence that for $U \subset X$ an [[open subset]], then also its [[pre-image]] $g^{-1}(U) \subset Y$ is open in $Y$.
By prop. \ref{ClosedSubsetContinuity} this is equivalent to the statement that for $ \subset X$ a [[closed subset]] then the [[pre-image]] $g^{-1}(C) \subset Y$ is also closed in $Y$.

But since $g$ is the [[inverse function]] to $f$, its [[pre-images]] are the [[images]] of $f$. Hence the last statement above equivalently says that $f$ sends closed subsets to closed subsets. This is true by prop. \ref{MapsFromCompactSpacesToHausdorffSpacesAreClosed}.

=--


+-- {: .num_defn #CompactHausdorffSpacesAreNormal}
###### Proposition
**([[compact Hausdorff spaces are normal]])**

Every [[compact Hausdorff topological space]] is a [[normal topological space]] (def. \ref{NormalSpace}).

=--

+-- {: .proof}
###### Proof

First we claim that $(X,\tau)$ is [[regular topological space|regular]]. To show this, we need to find for each point $x \in X$ and each disjoint closed subset $Y \in X$ dijoint open neighbourhoods $U_x \supset \{x\}$ and $U_Y \supset Y$. But since [[closed subspaces of compact spaces are compact]] (lemma \ref{ClosedSubsetsOfCompactSpacesAreCompact}), the subset $Y$ is in fact compact, and hence this is in fact the statement of lemma \ref{SeparationByNeighbourhoodsOfPointsFromCompactSubsetsInHausdorffSpaces}.

Next to show that $(X,\tau)$ is indeed normal, we apply the idea of the proof of lemma \ref{SeparationByNeighbourhoodsOfPointsFromCompactSubsetsInHausdorffSpaces} once more:

Let $Y_1, Y_2 \subset X$ be two disjoint closed subspaces. By the previous statement then for every point $y_1 \in Y$ we find disjoint open neighbourhoods $U_{y_1} \supset \{y_1\}$ and $U_{Y_2,y_1} \supset Y_2$. The union of the $U_{y_1}$ is a cover of $Y_1$, and by compactness of $Y_1$ there is a finite subset $S \subset Y$ such that

$$
  U_{Y_1} \coloneqq \underset{s \in S \subset Y_1}{\cup} U_{y_1}
$$

is an open neighbourhood of $Y_1$ and

$$
  U_{Y_2} \coloneqq \underset{s \in S \subset Y}{\cap} U_{Y_2,s}
$$

is an open neighbourhood of $Y_2$, and both are disjoint.

=--




$\,$



### Relation to quotient spaces


+-- {: .num_prop}
###### Proposition
**(continuous surjections from compact spaces to Hausdorff spaces are quotient projections)**

Let

$$
  \pi \;\colon\; (X, \tau_X) \longrightarrow (Y, \tau_Y)
$$

be a [[continuous function]] between [[topological spaces]] such that

1. $(X,\tau_X)$ is a [[compact topological space]] (def. \ref{CompactTopologicalSpace});

1. $(Y, \tau_Y)$ is a [[Hausdorff topological space]] (def. \ref{HausdorffTopologicalSpace});

1. $\pi \;\colon\; X \longrightarrow Y$ is a [[surjective function]].

Then $\tau_X$ is the [[quotient topological space|quotient topology]] inherited from $\tau_X$ via the surjection $f$
(def. \ref{QuotientTopologicalSpace}).

=--

+-- {: .proof}
###### Proof

We need to show that an subset $U \subset Y$ is an [[open subset]] $(Y , \tau_Y)$ precisely if its [[pre-image]] $\pi^{-1}(U) \subset X$
is an open subset in $(X,\tau_X)$. Equivalenty, as in prop. \ref{ClosedSubsetContinuity}, we need to show that $U$ is a [[closed subset]]
precisely if $\pi^{-1}(U)$ is a closed subset. The implication

$$
  \left( U \, \text{closed}\right) \,\Rightarrow\, \left( f^{-1}(U) \,\text{closed}\right)
$$

follows via prop. \ref{ClosedSubsetContinuity} from the continuity of $\pi$. The implication

$$
  \left( f^{-1}(U) \,\text{closed}\right)
   \,\Rightarrow\,
  \left( U \, \text{closed}\right)
$$

follows since $\pi$ is a [[closed map]] by prop. \ref{MapsFromCompactSpacesToHausdorffSpacesAreClosed}.

=--


The following proposition allows to recognize when a [[quotient space]] of a compact Hausdorff space is
itself still Hausdorff.

+-- {: .num_prop #QuotientProjectionsOutOfCompactHausdorffSpacesAreClosedPreciselyIfTheCodomainIsHausdorff}
###### Proposition
**(quotient projections out of compact Hausdorff spaces are closed precisely if the codomain is Hausdorff)**

Let

$$
  \pi \;\colon\; (X, \tau_X) \longrightarrow (Y, \tau_Y)
$$

be a [[continuous function]] between [[topological spaces]] such that

1. $(X, \tau)$ is a [[compact Hausdorff topological space]] (def. \ref{CompactTopologicalSpace}, def. \ref{HausdorffTopologicalSpace});

1. $\pi$ is a [[surjection]] and $\tau_Y$ is the corresponding [[quotient topological space|quotient topology]] (def. \ref{QuotientTopologicalSpace}).

Then the following are equivalent

1. $(Y, \tau_Y)$ is itself a [[Hausdorff topological space]] (def. \ref{HausdorffTopologicalSpace});

1. $\pi$ is a [[closed map]] (def. \ref{OpenMap}).

=--

+-- {: .proof}
###### Proof

The implicaton $\left( (Y, \tau_Y)\, \text{Hausdorff} \right) \Rightarrow \left( \pi \, \text{closed}  \right)$
is given by prop. \ref{MapsFromCompactSpacesToHausdorffSpacesAreClosed}. We need to show the converse.

Hence assume that $\pi$ is a closed map. We need to show that for every pair of
distinct point $y_1 \neq y_2 \in Y)$ there exist [[open neighbourhoods]] $U_{y_1}, U_{y_2} \in \tau_Y$
which are disjoint, $U_{y_1} \cap U_{y_2} = \emptyset$.

Therefore consider the [[pre-images]]

$$
  C_1 \coloneqq \pi^{-1}(\{y_1\})
  \phantom{AA}
  C_2 \coloneqq \pi^{-1}(\{y_2\})
  \,.
$$

Observe that these are [[closed subsets]], because in the Hausdorff space $(Y, \tau_Y)$
(which is hence in particular $T_1$) the singleton subsets $\{y_i\}$ are closed
by prop. \ref{T1InTermsOfTopologicalClosure}, and since pre-images under continuous functions preserves closed subsets by
prop. \ref{ClosedSubsetContinuity}.

Now since [[compact Hausdorff spaces are normal]]  it follows (by def. \ref{NormalSpace}) that we may find disjoint open subset $U_1, U_2 \in \tau_X$
such that

$$
  C_1 \subset U_1 \phantom{AAA} C_2 \subset U_2
  \,.
$$

Moreover, by lemma \ref{SaturatedOpenNeighbourhoodsOfSaturatedClosedSubsets} we may find these $U_i$ such that they
are both [[saturated subsets]] (def. \ref{SubsetSaturated}). Therefore finally lemma \ref{SaturatedOpenNeighbourhoodsOfSaturatedClosedSubsets}
says that the images $\pi(U_i)$ are open in $(Y,\tau_Y)$. These are now clearly disjoint open neighbourhoods of $y_1$ and $y_2$.

=--


+-- {: .num_example #ContinuousBijectionFromClosedIntervalToCircle}
###### Example

<div style="float:right;margin:0 10px 10px 0;">
<img src="http://ncatlab.org/nlab/files/ClosedIntervalQuotientedToCircle.pdf" width="300>
</div>


Consider the function

$$
  \array{
     [0,2\pi]/\sim &\longrightarrow& S^1 \subset \mathbb{R}^2
     \\
     t &\mapsto& (cos(t), sin(t))
  }
$$

* from the [[quotient topological space]] (def. \ref{QuotientTopologicalSpace}) of the [[closed interval]] (def. \ref{OpenAndClosedIntervals})
  by the [[equivalence relation]] which identifies the two endpoints

  $$
    (x \sim y) \;\Leftrightarrow\; \left( \left( x = y\right) \,\text{or}\, \left( \left( x \in \{0,2\pi\} \,\text{and}\, \left( y\in \{0, 2pi\} \right)  \right)  \right) \right)
  $$

* to the unit [[circle]] $S^1 = S_0(1) \subset \mathbb{R}^2$ (def. \ref{OpenBalls})
regarded as a [[topological subspace]] of the 2-dimensional [[Euclidean space]] (example \ref{EuclideanNorm}) equipped with its
[[metric topology]] (example \ref{MetricTopology}).

This is clearly a [[continuous function]] and a [[bijection]] on the underlying sets.
Moreover, since [[continuous images of compact spaces are compact]] (cor. \ref{ContinuousImageOfACompactSpaceIsCompact})
and since the closed interval $[0,1]$ is compact (example \ref{CompactClosedInterval}) we also obtain another proof that
the [[circle]] is compact.

Hence by prop. \ref{ContinuousBijectionsFromCompactSpacesToHausdorffSpacesAreHomeomorphisms}
the above map is in fact a [[homeomorphism]]

$$
  [0,2\pi]/\sim \;\simeq\; S^1
  \,.
$$


Compare this to the counter-example \ref{ExponentialMapFromHalfOpenIntervalToCircle}, which observed that
the analogous function

$$
  \array{
    [0,2\pi) &\longrightarrow& S^1 \subset \mathbb{R}^2
    \\
    t &\mapsto& (cos(t), sin(t))
  }
$$

is _not_ a homeomorphism, even though this, too, is a bijection on the the underlying sets.
But the [[half-open interval]] $[0,2\pi)$ is not compact, and hence prop. \ref{ContinuousBijectionsFromCompactSpacesToHausdorffSpacesAreHomeomorphisms}
does not apply.

=--









## Paracompact spaces
 {#ParacompactSpaces}


The concept of [[compact topological space|compactness]] in topology ([above](#CompactSpaces))
has several evident weakenings of interest. One is that of _[[paracompact topological space|paracompactness]]_
(def. \ref{ParacompactSpace} below). This property is important in applications to [[algebraic topology]],
where it guarantees notably that the [[abelian sheaf cohomology]] of a topological space may be computed in terms of
[[Cech cohomology]].

A key fact is that [[paracompact topological spaces]] and [[normal topological space|normal]]
spaces are equivalently those (prop. \ref{ParacompactHausdorffEquivalentToexistenceOfParititionsOfUnity}) all whose [[open covers]] admit a subordinate [[partition of unity]] (def. \ref{PartitionOfUnity} below), namely a set of [[real number|real]]-valued [[continuous functions]]
each of which is [[support|supported]] in only one patch of the cover, but whose [[sum]] is the unit function.
Existence of such partitions imply that structures on topological spaces which are glued together via [[linear maps]]
(such as [[vector bundles]]) are well behaved.



+-- {: .num_defn #LocallyFiniteCover}
###### Definition
**([[locally finite cover]])**

Let $(X,\tau)$ be a [[topological space]].

An [[open cover]] $\{U_i \subset X\}_{i \in I}$ of $X$ is called  _locally finite_ if for all point $x \in X$, there exists a  [[neighbourhood]] $U_x \supset \{x\}$ such that it [[intersection|intersects]] only finitely many elements of the cover, hence such that  $U_x \cap U_i \neq \emptyset$ for only a [[finite number]] of $i \in I$.

=--



+-- {: .num_defn #RefinementOfOpenCovers}
###### Definition
**([[refinement]] of [[open covers]])


Let $(X,\tau)$ be a [[topological space]], and let $\{U_i \subset X\}_{i \in I}$ be a [[open cover]].

Then a _[[refinement]]_ of this open cover is a set of open subsets $\{V_j \subset X\}_{j \in J}$ which is still an [[open cover]] in itself and such that for each $j \in J$ there exists an $i \in I$ with $V_j \subset U_i$.

=--

+-- {: .num_defn #ParacompactSpace}
###### Definition
**([[paracompact topological space]])**

A [[topological space]] $(X,\tau)$ is called _[[paracompact topological space|paracompact]]_ if every [[open cover]] of $X$ has a [[refinement]] (def. \ref{RefinementOfOpenCovers}) by a [[locally finite open cover]] (def. \ref{LocallyFiniteCover}).

=--

$\,$


We consider a couple of technical lemmas related to [[locally finite covers]]
which will be needed in the proof of prop. \ref{ParacompactHausdorffEquivalentToexistenceOfParititionsOfUnity} below:

1. [every locally finite refinement induces one with the original index set](#LocallyFiniteRefinementInducesLocallyFiniteWithSameIndexSet)

1. [every locally finite cover of a normal space contains the closure of one with smaller patches](#PatchesOfOpenCoverOfNormalSpaceMayBeMadeSmallerSoThatTheirClosuresAreContained) ("[[shrinking lemma]]")

+-- {: .num_lemma #LocallyFiniteRefinementInducesLocallyFiniteWithSameIndexSet}
###### Lemma
**(every locally finite refinement induces one with the original index set)**

Let $(X,\tau)$ be a [[topological space]], let $\{U_i \subset X\}_{i \in I}$ be an [[open cover]], and let $(\phi \colon J \to I, \{V_j \subset X\}_{j \in J})$, be a [[refinement]] to a [[locally finite cover]].

Then  $\left\{ W_i \subset X \right\}_{i \in I}$ with

$$
  W_i
    \;\coloneqq\;
  \left\{
    \underset{j \in \phi^{-1}(\{i\})}{\cup} V_j
  \right\}
$$

is still a [[refinement]] of $\{U_i \subset X\}_{i \in I}$ to a [[locally finite cover]].

=--


+-- {: .proof}
###### Proof

It is clear by construction that $W_i \subset U_i$, hence that we have a [[refinement]]. We need to show local finiteness.

Hence consider $x \in X$. By the assumption that $\{V_j \subset X\}_{j \in J}$ is locally finite, it follows that there exists an [[open neighbourhood]] $U_x \supset \{x\}$ and a [[finite set|finitee]] [[subset]] $K \subset J$ such that

$$
  \underset{j \in J\backslash K}{\forall} \left( U_x \cap V_j = \emptyset \right)
  \,.
$$

Hence by construction

$$
  \underset{I \in I\backslash \phi(K)}{\forall} \left( U_x \cap W_i = \emptyset \right)
  \,.
$$

Since the [[image]] $\phi(K) \subset I$ is still a [[finite set]], this shows that $\{W_i \subset X\}_{i \in I}$ is locally finite.

=--


+-- {: .num_lemma #PatchesOfOpenCoverOfNormalSpaceMayBeMadeSmallerSoThatTheirClosuresAreContained}
###### Lemma
**([[shrinking lemma]] for locally finite covers)**

Let $X$ be a [[topological space]] which is [[normal topological space|normal]] and let $\{U_i \subset X\}_{i \in I}$ be a [[locally finite cover|locally finite]] [[open cover]].

Then there exists another open cover $\{V_i \subset X\}_{i \in I}$ such that the [[topological closure]] $Cl(V_i)$ of its elements is cotained in the original patches:

$$
  \underset{i \in I}{\forall}
  \left(
     V_i \subset Cl(V_i) \subset U_i
  \right)
  \,.
$$

=--

We now prove this in  increasing generality, for  binary open covers (lemma \ref{ShrinkingLemmaForBinaryCover} below), then for finite covers (lemma \ref{ShrinkinglemmaForFiniteCovers}), then for locally finite countable covers (lemma \ref{ShrinkingLemmaForLocallyFiniteCountableCovers}), and finally for general locally finite covers (lemma \ref{PatchesOfOpenCoverOfNormalSpaceMayBeMadeSmallerSoThatTheirClosuresAreContained}, proof [below](#PatchesOfOpenCoverOfNormalSpaceMayBeMadeSmallerSoThatTheirClosuresAreContained)). The last statement needs the [[axiom of choice]].

+-- {: .num_lemma #ShrinkingLemmaForBinaryCover}
###### Lemma
**([[shrinking lemma]] for binary covers)**

Let $(X,\tau)$ be a [[normal topological space]] and let $\{U \subset X\}_{i \in \{1,2\}}$ an [[open cover]] by two [[open subsets]].

Then there exists an open set $V_1 \subset X$ whose [[topological closure]] is contained in $U_1$

$$
  V_1 \subset Cl(V_1) \subset U_1
$$

and such that $\{V_1,U_2\}$ is still an open cover of $X$.

=--

+-- {: .proof}
###### Proof

Since $U_1 \cup U_2 = X$ it follows (by [[de Morgan's law]]) that their [[complements]] $X \backslash U_i$ are [[disjoint subset|disjoint]] [[closed subsets]]. Hence by normality of $(X,\tau)$ there exist disjoint open subsets

$$
  V_1 \supset X \backslash U_2
  \phantom{AAA}
  V_2 \supset X \backslash U_1
  \,.
$$

By their disjointness, we have the following inclusions:

$$
  V_1 \subset X \backslash V_2 \subset U_1
  \,.
$$

In particular, since $X \backslash V_2$ is closed, this means that $Cl(V_1) \subset X \backslash(V_2)$.

Hence it only remains to observe that $V_1 \cup U_2 = X$, by definition of $V_1$.


=--

+-- {: .num_lemma #ShrinkinglemmaForFiniteCovers}
###### Lemma
**([[shrinking lemma]] for finite covers)**

Let $(X,\tau)$ be a [[normal topological space]], and let $\{U_i \subset X\}_{i \in \{1, \cdots, n\}}$ be an [[open cover]] with a [[finite number]] $n \in \mathbb{N}$ of patches. Then there exists another open cover $\{V_i \subset X\}_{i \in I}$ such that $Cl(V_i) \subset U_i$ for all $i \in I$.

=--


+-- {: .proof}
###### Proof

By [[induction]] using lemma \ref{ShrinkingLemmaForBinaryCover}.

To begin with, consider $\{ U_1, \underoverset{i = 2}{n}{\cup} U_i\}$. This is a binary open cover, and hence lemma \ref{ShrinkingLemmaForBinaryCover} gives an open subset $V_1 \subset X$ with $V_1 \subset Cl(V_1) \subset U_1$ such that $\{V_1, \underoverset{i = 2}{n}{\cup} U_i\}$ is still an open cover, and accordingly so is

$$
  \{ V_1  \} \cup \left\{ U_i \right\}_{i \in \{2, \cdots, n\}}
  \,.
$$

Similarly we next find an open subset $V_2 \subset X$ with $V_2 \subset Cl(V_2) \subset U_2$ and such that

$$
  \{ V_1, ,V_2  \} \cup \left\{ U_i \right\}_{i \in \{3, \cdots, n\}}
$$

is an open cover. After $n$ such steps we are left with an open cover $\{V_i \subset X\}_{i \in \{1, \cdots, n\}}$ as required.

=--

+-- {: .num_remark}
###### Remark

Beware that the [[induction]] in lemma \ref{ShrinkinglemmaForFiniteCovers} does _not_ give the statement for infinite [[countable covers]]. The issue is that it is not guaranteed that $\underset{i \in \mathbb{N}}{\cup} V_i$ is a cover.

And in fact, assuming the [[axiom of choice]], then there exists a  counter-example of a countable cover on a normal spaces for which the shrinking lemma fails (a [[Dowker space]] due to [Beslagic 85](#Beslagic85)).

=--

This issue is evaded if we consider [[locally finite covers]]:

+-- {: .num_lemma #ShrinkingLemmaForLocallyFiniteCountableCovers}
###### Lemma
**([shrinking lemma]] for locally finite countable covers)**

Let $(X,\tau)$ be a [[normal topological space]] and $\{U_i \subset X\}_{i \in \mathbb{N}}$ a [[locally finite cover|locally finite]] [[countable cover]]. Then there exists [[open subsets]] $V_i \subset X$ for $i \in \mathbb{N}$ such that $V_i \subset Cl(V_i) \subset U_i$ and such that $\{V_i \subset X\}_{i \in \mathbb{N}}$ is still a cover.

=--

+-- {: .proof}
###### Proof

As in the proof of lemma \ref{ShrinkinglemmaForFiniteCovers}, there exist $V_i$ for $i \in \mathbb{N}$ such that $V_i \subset Cl(V_i) \subset U_i$ and such that for every finite number, hence every $n \in \mathbb{N}$, then

$$
  \underoverset{i = 0}{n}{\cup} V_i
  \;=\;
  \underoverset{i = 0}{n}{\cup} U_i
  \,.
$$

Now the extra assumption that $\{U_i \subset X\}_{i \in I}$ is [[locally finite cover|locally finite]] implies that every $x \in X$ is contained in only finitely many of the  $U_i$, hence that for every $x \in X$ there exists $n_x \in \mathbb{N}$ such that

$$
  x \in \underoverset{i = 0}{n_x}{\cup} U_i
  \,.
$$

This implies that for every $x$ then

$$
  x \in \underoverset{i = 0}{n_x}{\cup} V_i
  \subset \underset{i \in \mathbb{N}}{\cup} V_i
$$

hence that $\{V_i \subset X\}_{i \in \mathbb{N}}$ is indeed a cover of $X$.

=--

We now invoke [[Zorn's lemma]] to generalize the shrinking lemma for finitely many patches (lemma \ref{ShrinkinglemmaForFiniteCovers}) to arbitrary sets of patches:

+-- {: .proof}
###### Proof
of the general [[shrinking lemma]] \ref{PatchesOfOpenCoverOfNormalSpaceMayBeMadeSmallerSoThatTheirClosuresAreContained}

Let $\{U_i \subset X\}_{i \in I}$ be the given locally finite cover of the normal space $(X,\tau)$. Consider the set $S$ of [[pairs]] $(J, \mathcal{V})$ consisting of

1. a [[subset]] $J \subset I$;

1. an $I$-indexed set of open subsets $\mathcal{V} = \{V_i \subset X\}_{i \in I}$

with the property that

1. $(i \in J \subset I) \Rightarrow ( Cl(V_i) \subset U_i )$;

1. $(i \in I \backslash J) \Rightarrow ( V_i = U_i )$.

1. $\{V_i \subset X\}_{i \in I}$ is an open cover of $X$.

Equip the set $S$ with a [[partial order]] by setting

$$
  \left(
    (J_1, \mathcal{V})
    \leq
    (J_2, \mathcal{V})
  \right)
    \Leftrightarrow
  \left(
    \left(
      J_1 \subset J_2
    \right)
    \,\text{and}\,
    \left(
      \underset{i \in J_1}{\forall}
      \left(
         V_i = W_i
      \right)
    \right)
  \right)
  \,.
$$

By definition, an element of $S$ with $J = I$ is an open cover of the required form.

We claim now that a [[maximal element]] $(J, \mathcal{V})$ of $(S,\leq)$ has $J = I$.

For assume on the contrary that there were $i \in I \backslash J$. Then we could apply the construction in lemma \ref{ShrinkingLemmaForBinaryCover} to replace that single $V_i$ with a smaller open subset $V'_i$ to obtain $\mathcal{V}'$ such that $Cl(V'_i) \subset V_i$ and such $\mathcal{V}'$ is still an open cover. But that would mean that $(J,\mathcal{V}) \lt (J \cup \{i\}, \mathcal{V}')$, contradicting the assumption that $(J,\mathcal{V})$ is maximal. This [[proof by contradiction|proves by contradiction]] that a maximal element of $(S,\leq)$ has $J = I$ and hence is an open cover as required.

We are reduced now to showing that a maximal element of $(S,\leq)$ exists. To achieve this we invoke [[Zorn's lemma]]. Hence we have to check that every [[chain]] in $(S,\leq)$, hence every [[total order|totally ordered]] [[subset]] has an [[upper bound]].

So let $T \subset S$ be a [[total order|totally ordered]] subset. Consider the union of all the index sets appearing in pairs in this subset:

$$
  K
    \;\coloneqq\;
  \underset{(J,\mathcal{V}) \in T  }{\cup} J
  \,.
$$

Now define open subsets $\mathcal{W}_i$ for $i \in K$ picking any $(J,\mathcal{V})$ in $T$ with $i \in J$ and setting

$$
  W_i \coloneqq V_i \phantom{AAA} i \in K
  \,.
$$

This is independent of the choice of $(J,\mathcal{V})$, hence well defined, by the assumption that $(T,\leq)$ is totally ordered.

Moreover, for $i \in I\backslash K$ define

$$
  W_i \coloneqq U_i  \phantom{AAA} i \in I \backslash K
  \,.
$$

We claim now that $\{W_i \subset X\}_{i \in I}$ thus defined is a cover of $X$. Because by assumption that $\{U_i \subset X\}_{i \in I}$ is locally finite, also all the $\{V_i \subset X\}_{i \in I}$ are locally finite, hence for every point $x \in X$ there exists a finite set $J_x \subset I$ such that $(i \in I \backslash J_x) \Rightarrow (i \notin U_i)$. Since $(T,\leq)$ is a total order, it must contain an element $(J, \mathcal{V})$ such that $J_x \cap K \subset J$. Since that $\mathcal{V}$ is a cover, it follows that $x \in \underset{i \in I}{\cup} V_i$, hence in $\underset{i \in I}{\cup} W_i$.

This shows that $(K,\mathcal{W})$ is indeed an element of $S$. It is clear by construction that it is an upper bound for $(T ,\leq )$. Hence we have shown that every [[chain]] in $(S,\leq)$ has an upper bound, and so Zorn's lemma implies the claim.



=--




### Partitions of unity
 {#PartitionsOfUnity}


+-- {: .num_defn #PartitionOfUnity}
###### Definition
**([[partition of unity]])**

Let $(X,\tau)$ be a [[topological space]], and let $\{U_i \subset X\}_{i \in I}$ be an [[open cover]]. Then a _[[partition of unity]] subordinate to the cover_ is

* a [[set]] $\{f_i\}_{i \in I}$ of [[continuous functions]]

  $$
    f_i \;\colon\; U_i \longrightarrow [0,1]
  $$

  (where $U_i \subset X$ and $[0,1] \subset \mathbb{R}$ are equipped with their [[subspace topology]], the [[real numbers]] $\mathbb{R}$ is regarded as the 1-dimensional [[Euclidean space]] equipped with its [[metric topology]]);

such that with

$$
  Supp(f_i) \coloneqq Cl\left( f_i^{-1}( (0,1] ) \right)
$$

denoting the [[support]] of $f_i$ (the [[topological closure]] of the subset of points on which it does not vanish) then

1. $\underset{i \in I}{\forall} \left( Supp(f_i) \subset U_i \right)$;

1. $\left\{ Supp(f_i) \subset X \right\}_{i \in I}$  is a [[locally finite cover]] (def. \ref{LocallyFiniteCover});

1. $\underset{x \in X}{\forall} \left(  \underset{i \in I}{\sum} f_i(x) = 1 \right)$.

=--

+-- {: .num_remark }
###### Remark

Due to the second clause in def. \ref{PartitionOfUnity}, the [[sum]] in the third clause involves only a [[finite number]] of elements not equal to zero, and therefore is well defined.

=--

+-- {: .num_prop #ParacompactHausdorffEquivalentToexistenceOfParititionsOfUnity}
###### Proposition
**([[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]])**

Let $(X,\tau)$ be a [[topological space]]. Then the following are equivalent:

1. $(X,\tau)$ is a [[paracompact Hausdorff space]] (def. \ref{HausdorffTopologicalSpace}, def. \ref{ParacompactSpace}).

1. Every [[open cover]] of $(X,\tau)$ admits a subordinate [[partition of unity]] (def. \ref{PartitionOfUnity}).

=--


+-- {: .proof #OpenCoverOfParacompactHausdorffSpaceAdmitsPartitionOfUnityProof}
###### Proof

One direction is immediate: Assume that every open cover $\{U_i \subset X\}_{i \in I}$ admits a subordinate partition of unity $\{f_i\}_{i \in I}$. Then by definition (def. \ref{PartitionOfUnity}) $\{ Int(Supp(f)_i)  \subset X\}_{i \in I}$ is a locally finite open cover refining the original one.

We need to show the converse: If $(X,\tau)$ is a [[paracompact topological space]], then for every [[open cover]] $\{U_i \subset X\}_{i \in I}$ there is a subordinate [[partition of unity]] (def. \ref{PartitionOfUnity}).

To that end, first apply the [[shrinking lemma]] \ref{PatchesOfOpenCoverOfNormalSpaceMayBeMadeSmallerSoThatTheirClosuresAreContained} to the given locally finite open cover $\{U_i \subset X\}$, to obtain a smaller locally finite open cover $\{V_i \subset X\}_{i \in I}$, and then apply the lemma once more to that result to get a yet small open cover  $\{W_i \subset X\}_{i \in I}$, so that now

$$
  \underset{i \in I}{\forall}
  \left(
     W_i \subset Cl(W_i) \subset V_i \subset Cl(V_i) \subset U_i
  \right)
  \,.
$$

It follows that for each $i \in I$ we have two disjoint [[closed subsets]], namely the [[topological closure]] $Cl(W_i)$ and the [[complement]] $X \backslash V_i$

$$
  Cl(W_i) \cap X\backslash V_i = \emptyset
  \,.
$$

Now since [[paracompact Hausdorff spaces are normal]], [[Urysohn's lemma]] says that there exist [[continuous functions]]

$$
  h_i \;\colon\; X \longrightarrow [0,1]
$$

with the property that

$$
  h_i( Cl(W_i) ) = \{1\}
  \,,
  \phantom{AAA}
  h_i( X \backslash V_i ) = \{0\}
  \,.
$$

This means in particular that $h_i^{-1}((0,1]) \subset V_i$ and hence that

$$
  Supp(h_i) =  Cl(h_i^{-1}((0,1])) \subset Cl(V_i) \subset U_i
  \,.
$$

By construction, the set of function $\{h_i\}_{i \in I}$ already satisfies two of the three conditions on a partition of unity subordinate to $\{U_i \subset X\}_{i \in I}$ from def. \ref{PartitionOfUnity}.
It just remains to normalize these functions so that they indeed sum to unity. To that end, consider the continuous function

$$
  h \;\colon\; X \longrightarrow [0,1]
$$

defined on $x \in X$

$$
  h(x) \coloneqq \underset{i \in I}{\sum} h_i(x)
  \,.
$$

Notice that the [[sum]] on the right has only a [[finite number]] of non-zero summands, due to the local finiteness of the cover, so that this is well-defined.


Then set

$$
  f_i \;\coloneqq\;  g_i/g
  \,.
$$

This is now manifestly such that $\underset{i \in I}{\sum} f_i = 1$, and so

$$
  \left\{
     f_i
  \right\}_{i \in I}
$$

is a partition of unity as required.


=--





### Manifolds

* [[topological manifold]]

* [[smooth manifold]]

* [[tangent space]]

* [[tangent bundle]]

* [[frame bundle]]

* [[G-structure]]





$\,$

$\,$

$\,$

(...)

$\,$


***

$\,$

This concludes _Section 1 [[point-set topology|Point-set topology]]_.

For the next section see _[[Introduction to Topology -- 2|Secton 2 -- Basic homotopy theory]]_.

$\,$

***





## References


### General

A canonical compendium is

* {#Bourbaki71} [[Nicolas Bourbaki]], chapter 1 _Topological Structures_ in _Elements of Mathematics III: General topology_,  Springer (1971, 1990)

Introductory textbooks include

* {#Kelley55} [[John Kelley]] _General Topology_, Graduate Texts in Mathematics, Springer (1955)

* {#Munkres75} [[James Munkres]], _Topology_, Prentice Hall (1975, 2000)

Lecture notes include

* {#Waldhausen} [[Friedhelm Waldhausen]], _Topologie_ ([pdf](https://www.math.uni-bielefeld.de/~fw/ein.pdf))

See also the references at _[[algebraic topology]]_.

### Special topics

The standard literature typically omits the following important topics:

Discussion of [[sober topological spaces]] is briefly in

* {#Johnstone82} [[Peter Johnstone]], section II 1. of _[[Stone Spaces]]_, Cambridge Studies in Advanced Mathematics __3__, Cambridge University Press 1982. xxi+370 pp. [MR85f:54002](http://www.ams.org/mathscinet-getitem?mr=698074), reprinted 1986.

An introductory textbook that takes sober spaces, and their relation to logic, as the starting point for toplogy is

* {#Vickers89} [[Steven Vickers]], _Topology via Logic_, Cambridge University Press (1989)


Detailed discussion of the [[Hausdorff reflection]] is in

* {#vanMunster14} Bart van Munster, _The Hausdorff quotient_, 2014 ([pdf](https://www.math.leidenuniv.nl/scripties/BachVanMunster.pdf))

