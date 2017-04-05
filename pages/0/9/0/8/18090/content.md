

{:principle: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

***

This page is going to contain a detailed introduction to basic [[topology]] ([[point-set topology]])
starting from scratch and ending with the first elementary application of [[homotopy theory]]: [[covering spaces]].

> Under construction.

For introduction to genuine _[[homotopy theory]]_ see at

* _[[Introduction to Stable homotopy theory -- P|Introduction to Homotopy theory]]_.

***

_[[topology|Topology]]_

#Contents#
* table of contents
{:toc}

$\,$


## Point-set topology



### Analytic continuity
 {#Continuity}

The key idea of topology is to study [[spaces]] with "[[continuous maps]]" between them. The concept of continuity was made precise first in [[analysis]], in terms of [[epsilontic analysis]] of [[open balls]], recalled as def. \ref{EpsilonDeltaDefinitionOfContinuity} below. Then it was realized that this has a more elegant formulation in terms of the more general concept of _[[open sets]]_, this is prop. \ref{ContinuityBetweenMetricSpacesInTermsOfOpenSets} below. Adopting the latter as the definition leads to a more
abstract concept of "continuous space", this is the concept of _[[topological spaces]]_, def. \ref{TopologicalSpace} below.
Topology is the study if the [[category]] of [[topological spaces]].


#### Via epsilontic analysis

First recall the basic concepts from [[analysis]]:

+-- {: .num_defn #MetricSpace}
###### Definition
**(metric space)**

A _[[metric space]]_ is

1. a [[set]] $X$ (the "underlying set");

1. a [[function]] $d \;\colon\; X \times X \to [0,\infty)$ (the "distance function") from the [[Cartesian product]] of the set with itself to the [[nonnegative number|non-negative]] [[real numbers]]

such that for all $x,y,z \in X$:

1. (symmetry) $d(x,y) = d(y,x)$

1. ([[triangle inequality]]) $d(x,y)+ d(y,z) \geq d(x,z)$.

1. (non-degeneracy) $d(x,y) = 0 \;\;\Leftrightarrow\;\; x = y$

=--

+-- {: .num_defn #OpenBalls}
###### Definition

Let $(X,d)$, be a [[metric space]]. Then for every element $x \in X$ and every  $\epsilon \in \mathbb{R}_+$ a [[positive number|positive]] [[real number]], we write

$$
  B^\circ_x(\epsilon)
    \;\coloneqq\;
  \left\{
    y \in X \;\vert\; d(x,y) \lt \epsilon
  \right\}
$$

for the [[open ball]] of [[radius]] $\epsilon$ around $x$.

=--


A key source of metric spaces are [[norm|normed]] _[[vector spaces]]_:

+-- {: .num_defn #NormedVectorSpace}
###### Dedfinition
**(normed vector space)**

A _[[normed vector space]]_ is

1. [[real vector space]] $V$;

1. a [[function]] (the _[[norm]]_)

   $$
     {\Vert - \Vert} \colon V \longrightarrow \mathbb{R}
   $$

   from the underlying [[set]] of $V$ to the [[real numbers]],

such that for all $c \in \mathbb{R}$, $v , w \in V$ it holds true that

1. (linearity) ${\Vert c v \Vert} = c {\Vert v \Vert }$;

1. ([[triangle inequality]]) ${\Vert v+w \Vert} \leq {\Vert v \Vert } + {\Vert w \Vert}$;

1. (non-degeneracy) if ${\Vert v \Vert} = 0$ then $v = 0$.

=--



+-- {: .num_prop #MetricSpaceFromNormedVectorSpace}
###### Proposition

Every [[normed vector space]] $(V, {\Vert - \Vert})$
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
     \Vert \vec x \Vert
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

More generally, for $n \in \mathbb{N}$, and $p \in \mathbb{N}$, $p \geq 1$, then the [[Cartesian space]] $\mathbb{R}^n$ carries the _[[p-norm]]_

   $$
     {\Vert \vec x \Vert}_p  \coloneqq \root p {\sum_i {|x_i|^p}}
   $$

The graphics on the right (grabbed from Wikipedia) shows unit circles in $\mathbb{R}^2$ with respect to various [[p-norms]].

By the [[Minkowski inequality]],
the [[p-norm]] generalizes to non-[[finite dimensional vector spaces]] such as [[sequence spaces]] and [[Lebesgue spaces]].

=--

The following now is the fairly obvious definition of continuity for functions between metric spaces.

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

is said to be _continuous at a point $x \in X$_ if for every $\epsilon \gt 0$ there exists $\delta\gt 0$ such that

$$
  d_X(x,y) \lt \delta \;\;\Rightarrow\;\; d_Y(f(x), f(y)) \lt \epsilon
$$

or equivalently such that

$$
  f(\;B_x^\circ(\delta)\;) \;\subset\; B^\circ_{f(x)}(\epsilon)
$$

where $B^\circ$ denotes the [[open ball]] (definition \ref{OpenBalls}).

The function $f$ is said to be _continuous_ if it is continuous at every point $x \in X$.

=--

+-- {: .num_example}
###### Example

Consider the [[real line]] $\mathbb{R}$ regarded as the
1-dimensional [[Euclidean space]] $\mathbb{R}$ from example \ref{EuclideanNorm}.

For $P \in \mathbb{R}[X]$ a [[polynomial]], then the function

$$
  \array{
    f_P &\colon& \mathbb{R} &\longrightarrow& \mathbb{R}
    \\
    && x &\mapsto& P(X)
  }
$$

is a [[continuous function]] in the sense of def. \ref{EpsilonDeltaDefinitionOfContinuity}.

On the other hand, a [[step function]] is continuous everywhere except at the [[finite number]] of points
at which it changes its value.



=--





#### Via open subsets

We now reformulate the analytic concept of continuity from def. \ref{EpsilonDeltaDefinitionOfContinuity} in terms of the simple but important concept of _[[open sets]]_:


+-- {: .num_defn #OpenSubsetsOfAMetricSpace}
###### Definition
**(neighbourhood and open set)**

Let $(X,d)$ be a [[metric space]] (def. \ref{MetricSpace}). Say that

1. A _[[neighbourhood]]_ of a point $x \in X$ is a [[subset]] $x \in U \subset X$ which contains some [[open ball]] $B_x^\circ(\epsilon)$ around $x$ (def. \ref{OpenBalls}).

1. An _[[open subset]]_ of $X$ is a [[subset]] $U \subset X$ such that for every $x \in U$ it also contains a [[neighbourhood]] of $x$.

=--


The following picture shows a point $x$, some [[open balls]] $B_i$ containing it, and two of its [[neighbourhoods]] $U_i$:

<img src="https://ncatlab.org/nlab/files/NeighbourhoodsAndOpenBalls.png" width="500">

> graphics grabbed from [Munkres 75](#Munkres75)

+-- {: .num_example #OpenAndClosedIntervals}
###### Example

Regard the [[real numbers]] $\mathbb{R}$ as the 1-dimensional [[Euclidean space]] (example \ref{EuclideanNorm}).

For $a \lt b \in \mathbb{R}$ consider the following [[subsets]]:

1. $(a,b) \coloneqq \left\{ x \in \mathbb{R} \vert a \lt x \lt b \right\}$

1. $(a,b] \coloneqq \left\{ x \in \mathbb{R} \vert a \lt x \leq b \right\}$

1. $[a,b) \coloneqq \left\{ x \in \mathbb{R} \vert a \leq x \lt b \right\}$

1. $[a,b] \coloneqq \left\{ x \in \mathbb{R} \vert a \leq x \leq b \right\}$.

The first of these is an open subset according to def. \ref{OpenSubsetsOfAMetricSpace}, the other three are not.
The first one is called an _[[open interval]]_, the last one a _[[closed interval]]_
and the middle two are called _[[half-open intervals]]_.

Similarly for $a,b \in \mathbb{R}$ one considers

1. $(-\infty,b) \coloneqq \left\{ x \in \mathbb{R} \vert x \lt b  \right\}$

1. $(a,\infty) \coloneqq \left\{ x \in \mathbb{R} \vert a \lt x  \right\}$

1. $(-\infty,b] \coloneqq \left\{ x \in \mathbb{R} \vert x \leq b  \right\}$

1. $[a,\infty) \coloneqq \left\{ x \in \mathbb{R} \vert a \leq x  \right\}$

The first two of these are open subsets, the last two are not.

=--


+-- {: .num_prop #ContinuityBetweenMetricSpacesInTermsOfOpenSets}
###### Proposition
**(rephrasing continuity in terms of open sets)**

A [[function]] $f \colon X \to Y$ between [[metric spaces]] (def. \ref{MetricSpace}) is [[continuous function|continuous]] in the [[epsilontic analysis|epsilontic]] sense of def. \ref{EpsilonDeltaDefinitionOfContinuity} precisely if it has the property that its [[pre-images]] of [[open subsets]] of $Y$ (in the sense of def. \ref{OpenSubsetsOfAMetricSpace}) are open subsets of $X$.

=--

+-- {: principle}
**principle of continuity**

$\,$ $\,$ _Pre-Images of open subsets are open._

=--


+-- {: .proof}
###### Proof

First assume that $f$ is continuous in the epsilontic sense. Then for $O_Y \subset Y$ any [[open subset]] and $x \in f^{-1}(O_Y)$ any point in the pre-image, we need to show that there exists a [[neighbourhood]] of $x$ in $f^{-1}(O_Y)$. But by assumption there exists an [[open ball]] $B_x^\circ(\epsilon)$ with $f(B_x^\circ(\epsilon)) \subset O_Y$. Since this is true for all $x$, by definition this means that $f^{-1}(O_Y)$ is open in $X$.

Conversely, assume that $f^{-1}$ takes open subsets to open subsets. Then for every $x \in X$ and $B_{f(x)}^\circ(\epsilon)$ an [[open ball]] around its image, we need to produce an open ball $B_x^\circ(\delta)$ in its pre-image. But by assumption $f^{-1}(B_{f(x)}^\circ(\epsilon))$ contains a [[neighbourhood]] of $x$ which by definition means that it contains such an open ball around $x$.

=--

+-- {: .num_example}
###### Example

Consider $\mathbb{R}$ as the 1-dimensional [[Euclidean space]] (example \ref{EuclideanNorm}) and consider the [[step function]]

$$
  H \;\colon\; \mathbb{R} \longrightarrow \mathbb{R}
$$

$$
  H \colon x \mapsto 
  \left\{
    \array{
      0 & \vert \, x \leq 0
      \\
      1 & \vert \, x \gt 0
    }
  \right.
  \,.
$$

Consider then for $a \lt b \in \mathbb{R}$ the [[open interval]] $(a,b) \subset \mathbb{R}$, 
an [[open subset]] accordiing to example \ref{OpenAndClosedIntervals}.
The [[preimage]] of this open subset is

$$
  H^{-1} \;\colon\;
  (a,b)
    \mapsto
  \left\{
    \array{
      \emptyset & \vert \,  a \gt 1 \;\;\text{or} \;\; b \lt 0
      \\
      \mathbb{R} & \vert \, a \lt 0 \;\;\text{and}\;\; b \gt 1
      \\
      \emptyset & \vert \, a \geq 0 \;\;\text{and}\;\; b \leq 1
      \\
      (0,\infty) & \vert \, 0 \leq a \lt 1 \;\;\text{and}\;\; b \gt 1
      \\
      (-\infty, 0] & \vert \, a \lt 0 \;\;\text{and}\;\; b \leq 1
      \\       
    }
  \right.
  \,.
$$

By example \ref{OpenAndClosedIntervals}, the last of these preimages listed is not an open subset.

=--


### Topological spaces
 {#TopologicalSpaces}

Due to prop. \ref{ContinuityBetweenMetricSpacesInTermsOfOpenSets} 
we should pay attention to [[open subsets]]. It turns out that the following closure
property is what _characterizes_ the concept:

+-- {: .num_prop #OpenSubsetsOfMetricSpaceClosureProperties}
###### Proposition
**(closure properties of open sets in a metric space)**

The collection of [[open subsets]] of a [[metric space]] $(X,d)$ as in def. \ref{OpenSubsetsOfAMetricSpace} has the following properties:

1. The [[intersection]] of any [[finite number]] of open subsets is again an open subset.

1. The [[union]] of any [[set]] of open subsets is again an open subset.

In particular

* the [[empty set]] is open (being the union of no subsets)

and

* the whole set $X$ itself is open (being the intersection of no subsets).

=--

Proposition \ref{OpenSubsetsOfMetricSpaceClosureProperties} motivates 
the following generalized definition, which abstracts away from the concept of [[metric space]]
just its system of [[open subsets]]:

#### Topologies

+-- {: .num_defn #TopologicalSpace}
###### Definition
**(topological spaces)**

Given a [[set]] $X$, then a _topology_ on $X$ is a collection $\tau$ of [[subsets]] of $X$ called the _[[open subsets]]_, hence a [[subset]] of the [[power set]]

$$
  \tau \subset P(X)
$$

such that this is closed under forming

1. finite [[intersections]];

1. arbitrary [[unions]].

A set $X$ equipped with such a [[topology]] is called a _[[topological space]]_.

=--

+-- {: .num_remark}
###### Remark

In the field of [[topology]] it is common to eventually simply say "[[space]]" as shorthand for "[[topological space]]".
This is especially so as further qualifiers are added, such as "Hausdorff  space" (def. \ref{HausdorffTopologicalSpace} below).
But beware that there are other kinds of spaces in mathematics.

=--

+-- {: .num_remark}
###### Remark

The simple definition of [[open subsets]] in def. \ref{TopologicalSpace} and the simple 
implementation of the _principle of continuity_ below in def. \ref{ContinuousMaps}
gives the field of [[topology]] its fundamental and universal flavor. The combinatorial nature of these definitions makes
topology be closely related to [[formal logic]] (for more on this see at _[[locale]]_).

=--

Our motivating example now reads as follows:

+-- {: .num_example #MetricTopology}
###### Example
**(metric topology)**

Let $(X,d)$ be a [[metric space]] (def. \ref{MetricSpace}). Then the collection of its [[open subsets]] in def. \ref{OpenSubsetsOfAMetricSpace} constitutes a _[[topological space|topology]]_ on the set $X$, making it a _[[topological space]]_ in the sense of def. \ref{TopologicalSpace}. This is called the _[[metric topology]]_.

=--

Stated more concisely: the [[open balls]] in a metric space constitute a "[[basis of a topology|basis]]" for the [[metric topology]]:

+-- {: .num_defn #TopologyBase}
###### Definition

Let $(X, \tau)$ be a [[topological space]], def. \ref{TopologicalSpace},
and let

$$
  B \subset \tau
$$

be a [[subset]] of its set of [[open subsets]]. We say that

1. $B$ is a _[[topological base|basis for the topology]]_ if every open subset $O \in \tau$ is a [[union]] of elements of $B$;

1. $B$ is a _[[topological base|sub-basis for the topology]]_ if every open subset $O \in \tau $ is a [[union]] of [[finitary intersections]] of elements of $B$.

=--

Often it is convenient to define topologies by defining some (sub-)basis. An example is the definition of the
[[compact-open topology]] on [[mapping spaces]] below in def. \ref{CompactOpenTopology}.

Here is some common further terminology relating to topological spaces:

+-- {: .num_defn #ClosedSubset}
###### Definition
**(closed subsets)**

Let $(X,\tau)$ be a [[topological space]] (def. \ref{TopologicalSpace}). Then 
a [[subset]] $S$ of $X$ is called a _[[closed subset]]_ if its [[complement]] $X \backslash S$ is an  _[[open subset]]_:

$$
  S \subset X\,\, \text{is closed}
  \phantom{AAA}
    \Leftrightarrow
  \phantom
    X\backslash S\,\, \text{is open} 
  \,.
$$

If a [[singleton]] subset $\{x\} \subset X$ is closed, one says that _$x$ is a closed point of $X$_.

Given any subset $S \subset X$, then is _[[closure]]_ $Cl(X)$ is the smalled closed subset containing $S$.

=--

+-- {: .num_defn #TopologyFinerCoarser}
###### Definition
**(finer/coarser topologies)**

Let $X$ be a [[set]], and let $\tau_1, \tau_2 \in P(X)$ be two [[topological space|topologies]] on $X$,
hence two choices of [[open subsets]] for $X$, making it a [[topological space]]. If

$$
  \tau_1 \subset \tau_2
$$

hence if every open subset of $X$ with respect to $\tau_1$ is also regarded as open by $\tau_2$, then 
one says that

* the topology $\tau_2$ is _[[finer topology|finer]]_ than the topology $\tau_2$

* the topology $\tau_1$ is _[[coarser topology|corarser]]_ than the topology $\tau_1$.

=--




While the example of [[metric space]] topologies (example \ref{MetricTopology}) is the motivating example
for the concept of [[topological spaces]], it is important to notice that the concept
of topological spaces is considerably more general:


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

1. $\tau \coloneq P(S)$ the set of _all_ open subsets; 

   this is called the _[[discrete topology]]_ on $S$, it is the [[finer topology|finest topology]] (def. \ref{TopologyFinerCoarser}) on $X$,
   
   we write $Disc(S)$ for the resulting topological space;

1. $\tau \coloneqq \{ \emptyset, S \}$ the set contaning only the [[empty set|empty]] subset of $S$ and all of $S$ itself;

   this is called the _[[codiscrete topology]]_ on $S$, it is the [[coarser topology|coarsest topology]] (def. \ref{TopologyFinerCoarser}) on $X$
   
   we write $CoDisc(S)$ for the resulting topological space.
   
The reason for this terminology is best seen when considering [[continuous functions]] into these (co-)disctete topological spaces.
See example \ref{ContinuousFunctionsIntoCoDiscreteTopologicalSpaces} below.

=--


#### Continuous functions
 {#ContinuousFunctions}

With the concept of [[topological spaces]] (def. \ref{TopologicalSpace}) 
it is now immediate to formally implement in abstract generality the
statement of prop. \ref{ContinuityBetweenMetricSpacesInTermsOfOpenSets}:

+-- {: principle}
**principle of continuity**

$\,$ $\,$ _Pre-Images of open subsets are open._

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


+-- {: .num_remark #TopCategory}
###### Remark
**(the category of topological spaces)**

The [[composition]] of [[continuous functions]] is clearly [[associativity|associative]] and [[unitality|unital]].

One says that

1. [[topological spaces]] constitute the [[objects]]

1. [[continuous maps]] constitute the [[morphisms]] ([[homomorphisms]])

of  a _[[category]]_. The _[[category of topological spaces]]_ ("[[Top]]" for short).

It is useful to depict collections of [[objects]] with [[morphisms]] between them
by [[diagrams]], like this one:


<img src="https://ncatlab.org/nlab/files/AssociativityDiagram.png" width="400">

> graphics grabbed from [Lawvere-Schanuel 09](#category+theory#LawvereSchanuel09).

=--


+-- {: .num_defn #FunctionLocallyConstant}
###### Definition

A [[continuous function]] $f \colon X \to Y$ (def. \ref{ContinuousMaps}) is called
_[[locally constant function|locally constant]]_ if every point $x \in X$ has a [[neighbourhood]]
on which the function is constant.

=--



+-- {: .num_example #ContinuousFunctionsIntoCoDiscreteTopologicalSpaces}
###### Example

Let $S$ be a [[set]] and let $(X,\tau)$ be a [[topological space]]. Recall from example \ref{CoDiscreteTopology}

1. the [[discrete topological space]] $Disc(S)$;

1. the [[co-discrete topological space]] $CoDisc(S)$

on the underlying set $S$. Then [[continuous functions]] (def. \ref{ContinuousMaps}) into these satisfy:

1. every [[continuous function]] $(X,\tau) \longrightarrow Disc(S)$ is [[locally constant function|locally constant]] (def. \ref{FunctionLocallyConstant});

1. every [[function]] (of sets) $X \longrightarrow CoDisc(S)$ is [[continuous function|continuous]].

=--


#### Homeomorphism

With the [[objects]] ([[topological spaces]]) and the [[morphisms]] ([[continuous maps]]) of the [[category]] [[Top]] thus defined
(remark \ref{TopCategory}), we obtain the concept of "sameness" in topology. To make this precise, one says that a [[morphism]]

$$
  X \overset{f}{\to} Y
$$

in a [[category]] is an _[[isomorphism]]_ if there exists a morphism going the other way around

$$
  X \overset{f^{-1}}{\longleftarrow} Y
$$

which is an [[inverse]] in the sense that

$$
  f \circ f^{-1} = id_Y \;\;\;\;\; and \;\;\;\;\; f^{-1} \circ f = id_X
  \,.
$$

+-- {: .num_defn #Homeomorphism}
###### Definition
**(homeomorphisms)**

An [[isomorphism]] in the [[category]] [[Top]] of [[topological spaces]] with [[continuous functions]] between them is called a _[[homeomorphism]]_.

Hence a _[[homeomoprhism]]_ is a [[continuous function]]

$$
  f \;\colon\; X \longrightarrow Y
$$

such that there exists a [[continuous function]] the other way around

$$
  X \longleftarrow Y \;\colon\; f^{-1}
$$

such that

$$
  f \circ f^{-1} = id_{Y} \;\;\;and\;\;\; f^{-1} \circ f = id_{X}
  \,.
$$

=--


<img src="https://ncatlab.org/nlab/files/Homeomorphism.png" width="560">

> graphics grabbed from [Munkres 75](#Munkres75)

+-- {: .num_example #OpenBallsHomeomorphicToRn}
###### Example
**(open interval homeomorphic to the real line)**

Regard the [[real line]] as the 1-dimensional [[Euclidean space]] (example \ref{EuclideanNorm}).

The open [[interval]] $(-1,1)$ (def. \ref{OpenAndClosedIntervals}) is [[homeomorphic]] to all of the [[real line]]

$$
  (0,1) \underset{homeo}{\simeq} \mathbb{R}^1
  \,.
$$

An [[inverse]] pair of [[continuous functions]] is for instance given by

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
    f^{-1} &\colon&  (-1,+1) &\longrightarrow& \mathbb{R}^1
    \\
    && x &\mapsto& \frac{x}{\sqrt{1 - x^2}}
  }
  \,.
$$

Generally, every [[open ball]] in $\mathbb{R}^n$ (def. \ref{OpenBalls}) is [[homeomorphic]] to all of $\mathbb{R}^n$.

=--


+-- {: .num_example #HomeomorphismBetweenTopologicalAndCombinatorialCircle}
###### Example
**(interval glued at endpoints is homeomorphic to the circle)**

As topological spaces, the [[closed interval]] $[0,1]$ (def. \ref{OpenAndClosedIntervals}) with its two endpoints identified is [[homeomorphic]] (def. \ref{Homeomorphism}) to the standard [[circle]]:

$$
  [0,1]_{/(0 \sim 1)} \;\; \underset{homeo}{\simeq} \;\; S^1
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
which itself equipped with its standard [[metric topology]] (example \ref{MetricTopology}).

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

Similarly:

The [[square]] $[0,1]^2$ with two of its sides identified is the [[cylinder]], and with also the other two sides
identified is the [[torus]]:

<img src="https://ncatlab.org/nlab/files/TorusAsQuotientOfSquare.png" width="500">

If the sides are identified with opposite orientation, the result is the _[[Möbius strip]]_:

<img src="https://ncatlab.org/nlab/files/MoebiusStripAsQuotientOfSquare.png" width="400">

> graphics grabbed from [Lawson 03](#Lawson03)

$\,$

Important examples of pairs of spaces that are _not_ homeomorphic include the following:


+-- {: .num_theorem #TopologicalInvarianceOfDimension}
###### Theorem
**([[topological invariance of dimension]])**

For $n_1, n_2 \in \mathbb{N}$ but $n_1 \neq n_2$, then the [[Cartesian spaces]] $\mathbb{R}^{n_1}$ and $\mathbb{R}^{n_2}$ are _not_ [[homeomorphic]].

More generally, an [[open set]] in $\mathbb{R}^{n_1}$ is never homeomorphic to an open set in $\mathbb{R}^{n_2}$ if $n_1 \neq n_2$.

=--

The proof of theorem \ref{TopologicalInvarianceOfDimension} is surprisingly hard, given how obvious the statement seems intuitively. It requires tools from a field called _[[algebraic topology]]_ (notably [[Brouwer's fixed point theorem]]).

We showcase some basic tools of [[algebraic topology]] now and demonstrate the nature of their usage by proving two very simple special cases of the [[topological invariance of dimension]] (prop. \ref{TopologicalInvarianceOfDimensionFirstSimpleCase} and prop. \ref{topologicalInvarianceOfDimensionSecondSimpleCase} below).


+-- {: .num_example }
###### Example
**(homeomorphism classes of surfaces)**

The [[2-sphere]] $S^2 = \{(x,y,z) \in \mathbb{R}^3 \vert x^2 + y^2 + z^2 = 1\}$ is _not_ [[homeomorphic]] to the [[torus]] $T^2 = S^1 \times S^1$.

Generally the [[homeomorphism]] class of a [[closed manifold|closed]] [[orientable]] [[surface]] is determined by the number of "holes" it has, its _[[genus of a surface|genus]]_.

=--





### Separation axioms

The plain definition of _[[topological space]]_ happens to allow examples where distinct points or distinct subsets of the underlying set of a topological space appear as as more-or-less unseparable as seen by the topology on that set. In many applications one wants to exclude at least some of such degenerate examples from the discussion. The relevant conditions to be imposed on top of the plain [[axioms]] of a [[topological space]] are hence known as _[[separation axioms]]_.

These axioms are all of the form of saying that two subsets (of certain forms) in the topological space are 'separated' from each other in one sense if they are 'separated' in a (generally) weaker sense. For example the weakest axiom (called $T_0$) demands that if two points are distinct as elements of the underlying set of points, then there exists at least one [[open subset]] that contains one but not the other.

In this fashion one may impose a hierarchy of stronger axioms. For example demanding that given two distinct points, then each of them is contained in some open subset not containing the other ($T_1$) or that such a pair of open subsets around two distinct points may in addition be chosen to be disjoint ($T_2$). This last condition, $T_2$, also called the _[[Hausdorff topological space|Hausdorff condition]]_ is the most common among all separation axioms. Often (but by far not always) this is considered by default.

Originally there were four separation axioms $T_1, T_2, T_3, T_4$; nowadays one considers various more. Besides the extrapolation of the original sequence from $T_0$ through $T_6$ (with $T_{2\frac{1}{2}}$ and $T_{3\frac{1}{2}}$ interpolated), there is a similar sequence of axioms called $R_0, R_1, R_2, R_3$ (with their extrapolations and interpolations) of the same form, except that they do not start with mentioning two set-theoretically distinct points, but two points satisfying the conclusion of $T_0$. This and more is spelled out [below](#TheClassicalTheory).

There are also axioms that do not follow the pattern of "if certain two subsets are separated in some weak sense, then they are also separated in some stronger sense", but that still axiomatize some kind of separatedness. For example the condition on a [[topological space]] being [[sober topological space|sober]] is of a different nature, but is implied by $T_2$ and implies $T_0$. Notice that via their [[full subcategory|full embdding]] into [[locales]], [[sober topological spaces]] may be understood without reference to their underlying set pf points at all.

All separation axioms are satisfied by [[metric spaces]], from whom the concept of topological space was originally abstracted [above](#TopologicalSpaces). Hence imposing some of them may also be understood as gauging just how far one allows topological spaces to generalize away from metric spaces


#### $T_n$-Topological spaces



+-- {: .num_defn #HausdorffTopologicalSpace}
###### Definition

Let $(X,\tau)$ be a [[topological space]] (def. \ref{TopologicalSpace}).

For $x \neq y \in X$ any two points in the underlying set of $X$ which are not [[equality|equal]] as elements of this set, 
consider the following [[propositions]]:

* **(T0)** _There exists a [[neighbourhood]] of one of the two points which does not contain the other point._

* **(T1)** _There exist [[neighbourhoods]] of both points which do not contain the other point._

* **(T2)** _There exists [[neighbourhoods]]_ of both points which do not intersect each other._

Notice that these propositions imply each other as

$$
  T2 \Rightarrow T1 \Rightarrow T0
  \,.
$$

The topological space $X$ is called a _$T_n$-topological space_ or just _$T_n$-space_, for short, 
if it satisfies proposition $T_n$ above for
all pairs of distinct points.

A $T_2$-topological space is also called a _[[Hausdorff topological space]]_.

=--

+-- {: .num_prop}
###### Proposition

A [[topological space]] is $T_1$ (def. \ref{HausdorffTopologicalSpace}) precisely if 
all its points are [[closed points]] (def. \ref{ClosedSubset}). 

=--

+-- {: .num_prop}
###### Proposition

The category of Hausdorff topological spaces is a [[reflective subcategory]] of that of all topological spaces.

$$
  Top_{Haus}
    \underoverset{\bot}{\overset{H}{\longleftarrow}}{\hookrightarrow}
  Top
  \,.
$$

The [[reflector]] $H$ acts as follows: 

For $(X,\tau) \in Top$ any topological space. Consider the [[equivalence relation]] on the underlying set $X$
for which $x \sim y$ precisely if for every [[continuous function]] $f \colon X \to Y$ into a 
Hausdorff space $Y$ we have $f(x) = f(y)$. Then the set of [[equivalence classes]]

$$
  H X \coloneqq X /_{\sim}
$$

equipped with the [[quotient topology]] (example \ref{QuotientTopology}) is the Hausdorffification of $X$.

=--




### Compactness

A [[metric space]] is called _[[sequentially compact space|sequntially compact]]_ (recalled below as def. \ref{SequentiallyCompact})
if every [[sequence]] of points in it has a [[sub-sequence]] which [[convergence|converges]]. Here we discuss how
to generalize this concept of compactness from [[metric spaces]] to [[topological spaces]].

The right definition turns out to be this one:

+-- {: .num_defn #OpenCover}
###### Definition

An _[[open cover]]_ of a [[topological space]] $X$ (def. \ref{TopologicalSpace})
is a collection $\{U_i \subset X\}_{i \in I}$ of [[open subsets]] $U_i$ of $X$,
indexed by some [[set]] $I$, such that their [[union]] is all of $X$:

$$
  \underset{i \in I}{\cup} U_i \;=\; X
  \,.
$$

=--

+-- {: .num_defn #CompactTopologicalSpace}
###### Definition

A [[Hausdorff topological space|Hausdorff]] [[topological space]] $X$ (def. \ref{TopologicalSpace}) is
 _[[compact topological space]]_ if every [[open cover]] $\{U_i \to X\}_{i \in I}$ (def. \ref{OpenCover}) has
 a _finite subcover_ in that there is a [[finite set|finite]] [[subset]] $J \subset I$ such that
 $\{U_i \to X\}_{i \in J}$ is still a cover of $X$, i.e.  $\underset{i \in J}{\cup} U_i = X$.

=--

#### Compact metric spaces

We recall now how for [[metric spaces]] this concept of compactness is equivalent to the
one via [[convergence|converging]] [[sub-sequences]].
So recall the concept of [[convergence]] and [[compactness]] of [[metric spaces]] via [[epsilontic analysis]]:

+-- {: .num_defn #Sequences}
###### Definition

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

Let $(X,d)$ be a [[metric space]] (def. \ref{MetricSpace}).
Then a [[sequence]]

$$
  x_{(-)}
    \;\colon\;
  \mathbb{N}
    \longrightarrow
  X
$$

in the underlying set $X$ (def. \ref{Sequences}) is said to _[[convergence|converge]]_ to a point $y \in X$, denoted

$$
  x_i \overset{i \to \infty}{\longrightarrow} y
$$

if

$$
  \underset{ {\epsilon \in \mathbb{R}}  \atop {\epsilon \gt 0} }{\forall}
  \;
  \underset{N_\epsilon \in \mathbb{N}}{\exists}
  \;
  \underset{ {i \in \mathbb{N}} \atop {i \gt N_\epsilon} }{\forall}
  \;\colon\;
  d(x_i, y) \leq \epsilon
  \,.
$$

=--

+-- {: .num_defn #CauchySequence}
###### Definition

Given a [[metric space]] $(X,d)$ (def. \ref{MetricSpace}), then a [[sequence]] of points in $X$ (def. \ref{Sequences})

$$
  x_{(-)} \;\colon\;  \mathbb{N}  \longrightarrow X
$$

is called a _[[Cauchy sequence]]_ if

$$
  \underset{{\epsilon \in \mathbb{R}} \atop {\epsilon \gt 0}}{\forall}
  \;
  \underset{N_\epsilon \in \mathbb{N}}{\exists}
  \;
  \underset{{i,j \in \mathbb{N}} \atop {i,j \gt N_{\epsilon}}}{\forall}
  \;:\;
  d(x_i, x_j) \leq \epsilon
  \,.
$$

=--

+-- {: .num_defn #CompleteMetricSpace}
###### Definition

A [[metric space]] $(X,d)$ (def. \ref{MetricSpace}), for which every [[Cauchy sequence]] (def. \ref{CauchySequence})
[[convergence|converges]] (def. \ref{Convergence}) is called a _[[complete metric space]]_.

A [[normed vector space]], regarded as a metric space via prop. \ref{MetricSpaceFromNormedVectorSpace} that is
is complete in this sense is called a _[[Banach space]]_.

=--

+-- {: .num_defn #SequentiallyCompact}
###### Definition

A [[metric space]] $(X,d)$ (def. \ref{MetricSpace}) is called _[[sequentially compact space|sequentially compact]]_
if every [[sequence]] in $X$ has a subsequence (def. \ref{Sequences}) which [[convergence|converges]] (def. \ref{CIonvergence}).

=--

The key fact to translate this [[epsilontic analysis|epsilontic]] definition of comopactness to a concept that
makes sense for general [[topological space]] is the following:

+-- {: .num_prop}
###### Proposition

For a [[metric space]] $(X,d)$ (def. \ref{MetricSpace}) the following are equivalent:

1. $X$ is [[sequentially compact space|sequentially compact]];

1. every [[open cover]] $\{U_i \to X\}_{i \in I}$ of $X$ has
 a _finite subcover_ in that there is a [[finite set|finite]] [[subset]] $J \subset I$ such that
 $\{U_i \to X\}_{i \in J}$ is still a cover of $X$: $\underset{i \in J}{\cup} U_i = X$.


=--


+-- {: .num_prop }
###### Proposition

A compact [[Hausdorff space]] must be [[normal space|normal]].  That is, the [[separation axioms]] $T_2$ through $T_4$ (when interpreted as an increasing sequence) are equivalent in the presence of compactness.

=--


+-- {: .num_prop }
###### Proposition

The [[Heine-Borel theorem]] asserts that a subspace $S \subset \mathbb{R}^n$ of a [[Cartesian space]] is compact precisely if it is [[closed subset|closed]] and [[bounded subset|bounded]].

=--

+-- {: .num_prop }
###### Proposition

[[compact subspaces of Hausdorff spaces are closed]].

=--

+-- {: .num_prop }
###### Proposition

A [[discrete space]] is compact iff its underlying set is [[finite set|finite]].  In [[constructive mathematics]], a discrete space is compact iff its underlying set is [[Kuratowski-finite]].

=--


#### Compact-open topology

+-- {: .num_defn #CompactOpenTopology}
###### Definition

For $X$ a [[topological space]] and $Y$ a [[locally compact topological space]] (in that for every point, every [[neighbourhood]] contains a [[compact topological space|compact]] neighbourhood), the **[[mapping space]]**

$$
  X^Y \in Top
$$

is the [[topological space]]

* whose underlying set is the set $Hom_{Top}(Y,X)$ of [[continuous
functions]] $Y \to X$,

* whose [[open subsets]] are [[unions]] of [[finitary intersections]] of the following [[topological base|subbase]] elements of standard open subsets:

  the standard open subset $U^K \subset Hom_{Top}(Y,X)$ for

  * $K \hookrightarrow Y$ a [[compact topological space]] subset

  * $U \hookrightarrow X$ an [[open subset]]

  is the subset of all those [[continuous functions]] $f$ that fit into a [[commuting diagram]] of the form

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

Accordingly this is called the _[[compact-open topology]]_ on the set of functions.

The construction extends to a [[functor]]

$$
  (-)^{(-)} \;\colon\; Top_{lc}^{op} \times Top \longrightarrow Top
  \,.
$$

=--





### Universal constructions


One point of the general definition of "[[topological space]]" is that it admits constructions which intuitively should exist on "continuous spaces", but which do not in general exist, for instance, as metric spaces.

We discuss [[universal constructions]] in [[Top]], such as [[limits]]/[[colimits]], etc.

+-- {: .num_defn #InitialAndFinalTopologies}
###### Definition

Let $\{X_i = (S_i,\tau_i) \in Top\}_{i \in I}$ be a [[class]] of [[topological spaces]], and let $S \in Set$ be a bare [[set]]. Then

* For $\{S \stackrel{f_i}{\to} S_i \}_{i \in I}$ a set of [[functions]] out of $S$, the _[[initial topology]]_ $\tau_{initial}(\{f_i\}_{i \in I})$ is the topology on $S$ with the [[minimum]] collection of [[open subsets]] such that all $f_i \colon (S,\tau_{initial}(\{f_i\}_{i \in I}))\to X_i$ are [[continuous function|continuous]].

* For $\{S_i \stackrel{f_i}{\to} S\}_{i \in I}$ a set of [[functions]] into $S$, the _[[final topology]]_ $\tau_{final}(\{f_i\}_{i \in I})$ is the topology on $S$ with the [[maximum]] collection of [[open subsets]] such that all $f_i \colon X_i \to (S,\tau_{final}(\{f_i\}_{i \in I}))$ are [[continuous function|continuous]].

=--

+-- {: .num_example #TopologicalSubspace}
###### Example

For $X$ a single topological space, and $\iota_S \colon S \hookrightarrow U(X)$ a subset of its underlying set, then the initial topology $\tau_{intial}(\iota_S)$, def. \ref{InitialAndFinalTopologies}, is the [[subspace topology]], making

$$
  \iota_S
  \;\colon\;
  (S, \tau_{initial}(\iota_S))
  \hookrightarrow
  X
$$

a [[topological subspace]] inclusion.

=--

+-- {: .num_example #QuotientTopology}
###### Example

Conversely, for $p_S \colon U(X) \longrightarrow S$ an [[epimorphism]], then the final topology $\tau_{final}(p_S)$ on $S$ is the _[[quotient topology]]_.

=--




+-- {: .num_prop #DescriptionOfLimitsAndColimitsInTop}
###### Proposition

Let $I$ be a [[small category]] and let $X_\bullet \colon I \longrightarrow Top$ be an $I$-[[diagram]] in [[Top]] (a [[functor]] from $I$ to $Top$), with components denoted $X_i = (S_i, \tau_i)$, where $S_i \in Set$ and $\tau_i$ a topology on $S_i$. Then:

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




+-- {: .num_example #PointTopologicalSpaceAsEmptyLimit}
###### Example

The limit over the empty diagram in $Top$ is the [[point]] $\ast$ with its unique topology.

=--

+-- {: .num_example #DisjointUnionOfTopologicalSpacesIsCoproduct}
###### Example

For $\{X_i\}_{i \in I}$ a set of topological spaces, their [[coproduct]] $\underset{i \in I}{\sqcup} X_i \in Top$ is their _[[disjoint union]]_.

=--

In particular:

+-- {: .num_example #DiscreteTopologicalSpaceAsCoproduct}
###### Example

For $S \in Set$, the $S$-indexed [[coproduct]] of the point, $\underset{s \in S}{\coprod}\ast $,  is the set $S$ itself equipped with the [[final topology]], hence is the [[discrete topological space]] on $S$.

=--

+-- {: .num_example #ProductTopologicalSpace}
###### Example

For $\{X_i\}_{i \in I}$ a set of topological spaces, their [[product]] $\underset{i \in I}{\prod} X_i \in Top$ is the [[Cartesian product]] of the underlying sets equipped with the _[[product topology]]_, also called the _[[Tychonoff product]]_.

In the case that $S$ is a [[finite set]], such as for binary product spaces $X \times Y$, then a [[basis for a topology|sub-basis]] for the product topology is given by the [[Cartesian products]] of the open subsets of (a basis for) each factor space.

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

(Here $g_\ast f$ is also called the pushout of $f$, or the _[[base change|cobase change]]_ of $f$ along $g$.) If $g$ is an inclusion, one also write $X \cup_f Y$ and calls this the _attaching space_.

<div style="float:left;margin:0 10px 10px 0;"><img src="http://ncatlab.org/nlab/files/AttachingSpace.jpg" width="450"></div>

By example \ref{CoequalizerInTop} the pushout/attaching space is the [[quotient topological space]]

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

be the canonical inclusion of the standard [[n-sphere|(n-1)-sphere]] as the [[boundary]] of the standard [[n-disk]] (both regarded as [[topological spaces]] with their [[subspace topology]] as subspaces of the [[Cartesian space]] $\mathbb{R}^n$).


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



+-- {: .num_example #DiscreteTopologicalSpace}
###### Example
**(discrete topological space)**

For $S$ a bare [[set]], then the _[[discrete topology]]_ on $S$ regards _every_ subset of $S$ as an [[open subset]].

=--

+-- {: .num_example #SubspaceTopology}
###### Example
**(subspace topology)**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/OpenSubsetsOfSquareInsidePlane.png" width="200">
</div>

Let $(X, \tau_X)$ be a [[topological space]], and let $X_0 \hookrightarrow X$ be a [[subset]] of the underlying set. Then the corresponding _[[topological subspace]]_ has $X_0$ as its underlying set, and its open subsets are those subsets of $X_0$ which arise as restrictions of open subsets of $X$.

(Also called the _[[initial topology]]_ of the inclusion map.)

The picture on the right shows two open subsets inside the [[square]], regarded as a [[topological subspace]] of the [[plane]] $\mathbb{R}^2$:


> graphics grabbed from [Munkres 75](#Munkres75)

=--


+-- {: .num_example #QuotientTopologicalSpace}
###### Example
**(quotient topological space)**

Let $(X,\tau_X)$ be a [[topological space]] (def. \ref{TopologicalSpace}) and let

$$
  R_\sim \subset X \times X
$$

be an [[equivalence relation]] on its underlying set. Then the _[[quotient topological space]]_  has

* as underlying set the [[quotient set]] $X_{\sim}$, hence the set of [[equivalence classes]],

and

* a subset $O \subset X_{\sim}$ is declared to be an [[open subset]] precisely if its [[preimage]] $\pi^{-1}(O)$ under the canonical [[projection map]]

  $$
    \pi \colon X \to X_\sim
  $$

  is open in $X$.

(This is also called the _[[final topology]]_ of the projection $\pi$.)

=--

<img src="https://ncatlab.org/nlab/files/QuotientOfSquareIsCylinderAndTorus.png" width="660">


The above picture shows on the left the [[square]] (a [[topological subspace]] of the [[plane]]),
then in the middle the resulting [[quotient topological space]] obtained by
identifying two opposite sides (the _[[cylinder]]_), and on the right the further quotient obtained by
identifying the remaining sides (the _[[torus]]_).

> graphics grabbed from [Munkres 75](#Munkres75)

+-- {: .num_example #ProductTopologicalSpace}
###### Example
**(product topological space)**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/ProductTopology.png" width="300">
</div>

For $X$ and $Y$ two [[topological spaces]], then the [[product topological space]] $X \times Y$
has

* as underlying set the [[Cartesian product]] of the underlying sets of $X$ and $Y$,

and

* its [[open sets]] are those subsets $O \subset X \times Y$ of the Cartesian product such that for all point $(x,y) \in O$
there exists open sets $x \in O_x \subset X$ and $y \in O_Y \subset Y$ such that $O_x \times O_y \subset O$.


> graphics grabbed from [Munkres 75](#Munkres75)

=--





These constructions of [[discrete topological spaces]], [[quotient topological spaces]], [[topological subspaces]] and of [[product topological spaces]] are simple examples of **[[limits]]** and of **[[colimits]]** of topological spaces. The [[category]] [[Top]] of topological spaces has the convenient property that _all_ [[limits]] and [[colimits]] (over [[small diagrams]]) exist in it. (For more on this see at _[Top -- Universal constructions](Top#UniversalConstructions)_.)







## Basic homotopy theory


In order to handle topological spaces, to compute their properties and distinguish them, it
turns out to be useful to consider not just continuity within a topological space, but also
continuous deformations of [[continuous maps]] _between_ topological spaces. This is the
concept of _[[homotopy]]_, and its study is _[[homotopy theory]]_. We introduce the basic concept
and consider its most fundamental application: the [[fundamental group]] and its relation to the
classification of [[covering spaces]].


### Homotopy
  {#Homotopy}

We have seen above that for $n \geq 1$  then the [[open ball]] $B_0^\circ(1)$ in $\mathbb{R}^n$ is _not_ [[homeomorphic]] to, notably, the point $\ast = \mathbb{R}^0$ (example \ref{OpenBallsHomeomorphicToRn}, theorem \ref{TopologicalInvarianceOfDimension}). Nevertheless, intuitively the $n$-ball is a "continuous deformation" of the point, obtained as the radius of the $n$-ball tends to zero.

This intuition is made precise by observing that there is a [[continuous function]] out of the [[product topological space]]
(example \ref{ProductTopologicalSpace}) of the open ball with the closed [[interval]]

$$
  \eta \colon [0,1] \times B_0^\circ(1)  \longrightarrow \mathbb{R}^n
$$

which is given by rescaling:

$$
  (t,x) \mapsto t \cdot x
  \,.
$$

This continuously interpolates between the open ball and the point in that for $t = 1$ then it restricts to the defining inclusion $B_0^\circ(1)$, while for $t = 0$ then it restricts to the map constant on the origin.

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/ShrinkingBalls.png" width="200">
</div>

We may summarize this situation by saying that there is a
[[diagram]] of [[continuous functions]] of the form

$$
  \array{
    B_0^\circ(1) \times \{0\}
    \\
    \downarrow & \searrow^{\mathrlap{x \mapsto 0}}
    \\
    [0,1] \times B_0^\circ(1)
    &\overset{(t,x) \mapsto t \cdot x}{\longrightarrow}&
    \mathbb{R}^n
    \\
    \uparrow & \nearrow_{\mathrlap{inclusion}}
    \\
    B_0^\circ(1) \times \{1\}
  }
$$

Such "continuous deformations" are called _[[homotopies]]_:

+-- {: .num_defn #LeftHomotopy}
###### Definition
**(homotopy)**

For $f,g\colon X \longrightarrow Y$ two [[continuous functions]] between [[topological spaces]] $X,Y$, then a _[[left homotopy|(left) homotopy]]_

$$
  \eta \colon f \,\Rightarrow_L\, g
$$

is a [[continuous function]]

$$
  \eta \;\colon\; X \times I \longrightarrow Y
$$


out of the [[product topological space]] (example \ref{ProductTopologicalSpace})
of the open ball with the standard interval, such that this fits into a [[commuting diagram]] of the form

<div style="float:right;margin:0 10px 10px 0;">
<img src="http://www.ncatlab.org/nlab/files/AHomotopy.jpg" width="400">
</div>


$$
  \array{
     {0} \times X
     \\
     {}^{\mathllap{(id,\delta_0)}}\downarrow & \searrow^{\mathrlap{f}}
     \\
     [0,1] \times X  &\stackrel{\eta}{\longrightarrow}& Y
     \\
     {}^{\mathllap{(id,\delta_1)}}\uparrow & \nearrow_{\mathrlap{g}}
     \\
     \{1\} \times X
  }
  \,.
$$

> graphics grabbed from J. Tauber [here](http://jtauber.com/blog/2005/07/01/path_homotopy/)

=--


+-- {: .num_defn #HomotopyEquivalence}
###### Definition
**(homotopy equivalence)**

A [[continuous function]] $f \;\colon\; X \longrightarrow Y$
is called a _[[homotopy equivalence]]_ if

1. there exists a continuous function the other way around,
$g \;\colon\; Y \longrightarrow X$, and

1. [[left homotopies]], def. \ref{LeftHomotopy}, from the two composites to the identity:

  $$
    \eta_1 \;\colon\; f\circ g \Rightarrow_L id_Y
  $$

  and

  $$
    \eta_2 \;\colon\; g\circ f \Rightarrow_L id_X
    \,.

  $$

=--


+-- {: .num_example}
###### Example
**(open ball is contractible)**

Any [[open ball]] (or closed ball), hence (by example \ref{OpenBallsHomeomorphicToRn}) any [[Cartesian space]]
is [[homotopy equivalence|homotopy equivalent]] to the point

$$
  \mathbb{R}^n \underset{homotopy}{\simeq} \ast
  \,.
$$


=--

+-- {: .num_example}
###### Example


The following three [[graphs]]

<img src="https://ncatlab.org/nlab/files/ThreeNonHomeoButHomotopyEquivGraphs.png" width="400">

(i.e. the evident [[topological subspaces]] of the [[plane]] $\mathbb{R}^2$ that these pictures indicate) are not [[homeomorphic]]. But they are [[homotopy equivalence|homotopy equivalent]], in fact they are each homotopy equivalent to the [[disk]] with two points removed, by the homotopies indicated by the following pictures:

<img src="https://ncatlab.org/nlab/files/HomotopyEquivalentsToBiAnnulus.png" width="400">


> graphics grabbed from [Hatcher](homotopy+equivalence#Hatcher)

=--


$\,$


### Connected components
 {#ConnectedComponents}

Using the concept of [[homotopy]] one obtains the basic tool of [[algebraic topology]], namely the construction of algebraic [[homotopy invariants]] of topological spaces. We introduce the simplest and indicate their use.


+-- {: .num_example}
###### Example

A [[homotopy]] between two points

$x,y \;\colon\; \ast \to X$

is a continuous [[path]] between these points.

=--

+-- {: .num_defn #pi0}
###### Definition
**(connected components)**

The set of [[homotopy classes]] of points in a [[topological space]] $X$ is called its set of
_path-[[connected components]]_, denoted.

$$
  \pi_0(X) \in Set
  \,.
$$

If $\pi_0(X) \simeq \ast$ consists of a single element, we say that $X$ is a _[[path-connected topological space]]_.

If $f \colon X \to Y$ is a [[continuous map]] between [[topological spaces]], then on [[homotopy classes]] of points it induces a [[function]] between the corresponding connected components, which we denote by:

$$
  \pi_0(f) \;\colon\; \pi_0(X) \longrightarrow \pi_0(Y)
  \,.
$$

=--

This construction is evidently compatible with [[composition]], in that

$$
  \pi_0(g \circ f) = \pi_0(g) \circ \pi_0(f)
$$

and it evidently is [[unitality|unital]], in that

$$
  \pi_0(id_X) = id_{\pi_{0}(X)}
  \,.
$$

One summarizes this by saying that $\pi_0$ is a _[[functor]]_ from the [[category]] [[Top]] of [[topological spaces]] to the [[category]] [[Set]] of [[sets]], denoted

$$
  \pi_0 \;\colon\; Top \longrightarrow Set
  \,.
$$

An immediate but important consequence is this:

+-- {: .num_prop #ConnectedComponentsDistinctImpliesHeomeClassesDistinct}
###### Proposition

If two [[topological spaces]] have sets of [[connected components]] that are not in [[bijection]], then those spaces are not [[homeomorphic]] to each other:

$$
  \pi_0(X) \neq \pi_0(Y)
  \;\;\;
    \Rightarrow
  \;\;\,
  X \underset{homeo}{\neq} Y
$$

=--

+-- {: .proof}
###### Proof

Since $\pi_0$ is [[functor|functorial]], it immediately follows that it sends [[isomorphisms]] to [[isomorphisms]], hence [[homeomorphisms]] to [[bijections]]:

$$
  \begin{aligned}
     & f \circ g = id \;\;and\;\; g \circ f = id
    \\
    \Rightarrow \;\;\;\;\;\;&
    \pi_0(f \circ g) = \pi_0(id) \;\;and \;\; \pi_0(g \circ f) = \pi_0(id)
    \\
    \Leftrightarrow \;\;\;\;\;\;
    &
    \pi_0(f) \circ \pi_0(g) = id \;\;and \;\; \pi_0(g) \circ \pi_0(f) = id
  \end{aligned}
  \,.
$$

=--

This means that we may use path connected components as a first "topological invariant" that allows us to distinguish some topological spaces.

+-- {: principle}
**principle of algebraic topology**

$\,\,$ _Use topological invariants to distinguish topological spaces._

=--


As an example for how this is being used, we have the following proof of a simple special case of the [[topological invariance of dimension]] (theorem \ref{TopologicalInvarianceOfDimension}):


+-- {: .num_prop #TopologicalInvarianceOfDimensionFirstSimpleCase}
###### Proposition
**([[topological invariance of dimension]] -- first simple case)**

The [[Cartesian spaces]] $\mathbb{R}^1$ and $\mathbb{R}^2$ are not [[homeomorphic]] (def. \ref{Homeomorphism}).

=--

+-- {: .proof}
###### Proof

Assume there were a [[homeomorphism]]

$$
  f \colon \mathbb{R}^1 \longrightarrow \mathbb{R}^2
$$

we will derive a contradiction. If $f$ is a homeomorphism, then clearly so is its restriction to the [[topological subspaces]] (example \ref{SubspaceTopology}) obtained by removing $0 \in \mathbb{R}^1$ and $f(0) \in \mathbb{R}^2$.

$$
  f
    \;\colon\;
  (\mathbb{R}^1-\{0\})
    \longrightarrow
  (\mathbb{R}^2 - \{f(0)\})
  \,.
$$


It follows that we would get a bijection of [[connected components]] between $\pi_0(\mathbb{R}^1 - \{0\})$ and $\pi_0(\mathbb{R}^2  - \{f(0)\})$. But clearly the first set has two elements, while the second has just one:

$$
  \pi_0(\mathbb{R}^1-\{0\})
    \;\neq\;
  \pi_0(\mathbb{R}^2 - \{f(0)\})
  \,.
$$


=--

The key lesson of the proof of prop. \ref{TopologicalInvarianceOfDimensionFirstSimpleCase} is its strategy:


+-- {: principle}
**principle of algebraic topology**

$\,\,$ _Use topological invariants to distinguish topological spaces._

=--


Of course in practice one uses more sophisticated invariants than just $\pi_0$.

The next topological invariant after the [[connected components]] is the _[[fundamental group]]:


### Fundamental group
 {#FundamentalGroup}


+-- {: .num_defn #FundamentalGroup}
###### Definition
**(fundamental group)**

Let $X$ be a [[topological space]] and let $x \in X$ be a chosen point. Then write

$$
  \pi_1(X,x)
    \;\in\;
  Grp
$$

for, to start with, the set of [[homotopy classes]] of [[paths]] in $X$ that start and end at $x$. Such paths are also called the continuous [[loops]] in $X$ based at $x$.

1. Under concatenation of loops, $\pi_1(X,x)$ becomes a [[semi-group]].

1. The constant loop is a [[neutral element]] under this composition (thus making $\pi_1(X,x)$ a "[[monoid]]").

1. The  reverse of a loop is its [[inverse]] in $\pi_1(X,x)$, making $\pi_1(X,x)$ indeed into a [[group]].

This is called the _[[fundamental group]]_ of $X$ at $x$.

=--

The following picture indicates the four non-equivalent non-trivial generators of the [[fundamental group]] of the
oriented [[surface]] of [[genus of a surface|genus]] 2:

<img src="https://ncatlab.org/nlab/files/FundamentalGroupOfGenus2Surface.png" width="500">

> graphics grabbed from [Lawson 03](#Lawson03)




Again, this operation is [[functor|functorial]], now on the [[category]] $Top^{\ast/}$
of [[pointed topological spaces]], whose [[objects]] are
topological spaces equipped with a chosen point, and whose [[morphisms]] are [[continuous maps]]
$f \colon X \to Y$ that take the chosen basepoint of $X$ to that of $Y$:

$$
  \pi_1 \;\colon\; Top^{\ast/} \longrightarrow Grp
  \,.
$$

As $\pi_0$, so also $\pi_1$ is a topological invariant. As before, we may use this to prove a simple case of the theorem of the [[topological invariance of dimension]]:

+-- {: .num_defn #SimplyConnected}
###### Definition

A topological space $X$ for which

1. $\pi_0(X) \simeq \ast$ ([[path-connected topological space|path connected]], def. \ref{pi0})

1. $\pi_1(X,x) \simeq 1$ (the [[fundamental group]] is [[trivial group|trivial]], def. \ref{FundamentalGroup}),

is called _[[simply connected topological space|simply connected]]_.

=--


+-- {: .num_prop #topologicalInvarianceOfDimensionSecondSimpleCase}
###### Proposition
**([[topological invariance of dimension]] -- second simple case)**

There is _no_ [[homeomorphism]] between $\mathbb{R}^2$ and $\mathbb{R}^3$.

=--

+-- {: .proof}
###### Proof

Assume there were such a homeomorphism $f$; we will derive a contradiction.

If $f$ is a homeomorphism, then so is its restriction to removing the origin from $\mathbb{R}^2$
and $f(0)$ from $\mathbb{R}^3$:

$$
  (\mathbb{R}^2 - \{0\})
    \longrightarrow
  (\mathbb{R}^3 - \{f(0)\})
  \,.
$$

Thse two spaces are both path-connected, hence $\pi_0$ does not distiguish them.

But they do have different [[fundamental groups]] $\pi_1$:

1. The fundamental group of $\mathbb{R}^{2} - \{0\}$ is $\mathbb{Z}$ (counting the winding of loops around the removed point).
We discuss this further below in example \ref{FundamentalGroupOfTheCircle}.

1. The fundamental group of $\mathbb{R}^3 - \{f(0)\}$ is trivial: because the single removed point is
no obstruction to sliding loops past it and contracting them.

But since passing to fundamental groups is [[functor|functorial]], the same argument
as in the proof of prop. \ref{ConnectedComponentsDistinctImpliesHeomeClassesDistinct}
shows that $f$ cannot be an [[isomorphism]], hence not a [[homeomorphism]].


=--

We now discuss a "dual incarnation" of fundamental groups, which often helps to compute them.

### Covering spaces
 {#CoveringSpaces}

+-- {: .num_defn #CoveringSpace}
###### Definition
**(covering space)**

A _[[covering space]]_ of a [[topological space]] $X$ is a [[continuous map]]

$$
  p \colon E \to X
$$

such that there exists an [[open cover]] $\underset{i}{\sqcup}U_i \to X$, such that restricted
to each $U_i$ then $E \to X$ is [[homeomorphic]] over $U_i$
to the [[product topological space]] (example \ref{ProductTopologicalSpace}) of $U_i$
with the [[discrete topological space]] (example \ref{DiscreteTopologicalSpace}) on a [[set]] $F_i$

$$
  \array{
    \underset{i}{\sqcup} U_i \times F_i &\longrightarrow&  E
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{p}}
    \\
    \underset{i}{\sqcup} U_i &\underset{}{\longrightarrow}& X
  }
  \,.
$$

For $x \in U_i \subset X$ a point, then the elements in $F_x  = F_i$ are called the _leaves_ of the covering at $x$.

=--

+-- {: .num_example #kForlCovringOfCircle}
###### Example
**(covering of circle by circle)**

<div style="float:left;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/pFoldCoveringOfCircleB.png" width="180">
</div>

Regard the [[circle]] $S^1 = \{ z \in \mathbb{C}  \;\vert\; {\vert z\vert} = 1 \}$ as the [[topological subspace]]
of elements of unit [[absolute value]] in the [[complex plane]].
For $k \in \mathbb{N}$, consider the continuous function

$$
  p \coloneqq (-)^k \;\colon\; S^1 \longrightarrow S^1
$$

given by taking a complex number to its $k$th power. This may be thought of as the
result of "winding the circle $k$ times around itself".
Precisely, for $k \geq 1$ this is a [[covering space]]
(def. \ref{CoveringSpace}) with $k$ leaves at each point.

> graphics grabbed from [Hatcher](homotopy+equivalence#Hatcher)


=--

+-- {: .num_example #CoveringOfCircleByRealLine}
###### Example
**(covering of circle by real line)**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/UniversalCoveringOfCircle.png" width="150">
</div>

Consider the [[continuous function]]

$$
  \exp(2 \pi i(-)) \;\colon\; \mathbb{R}^1 \longrightarrow S^1
$$

from the [[real line]] to the [[circle]],
which,

1. with the circle regarded as the unit circle in the [[complex plane]] $\mathbb{C}$, is given by

   $$
     t \mapsto \exp(2\pi i t)
   $$

1. with the circle regarded as the unit circle in $\mathbb{R}^2$, is given by

   $$
     t \mapsto ( cos(2\pi t), sin(2\pi t) )
     \,.
   $$

We may think of this as the result of "winding the line around the circle ad infinitum".
Precisely, this is a [[covering space]] (def. \ref{CoveringSpace}) with the [[leaves]] at each point forming the
set $\mathbb{Z}$ of [[natural numbers]].

=--


+-- {: .num_defn #ActionOfFundamentalGroupOnFibersOfCovering}
###### Definition
**(action of fundamental group on fibers of covering)**

Let $E \overset{\pi}{\longrightarrow} X$ be a [[covering space]] (def. \ref{CoveringSpace})

Then for $x \in X$ any point, and any choice of element $e \in F_x$ of the [[leaf space]] over $x$,
there is, up to [[homotopy]], a unique way to lift a representative
path in $X$ of an element $\gamma$ of the the [[fundamental group]] $\pi_1(X,x)$ (def. \ref{FundamentalGroup}) to a
continuous path in $E$ that starts at $e$. This path necessarily ends at some (other) point $\rho_\gamma(e) \in F_x$
in the same [[fiber]]. This construction provides a [[function]]

$$
  \array{
    \rho &\colon& F_x \times \pi_1(X,x) &\longrightarrow& F_x
    \\
    && (e,\gamma) &\mapsto& \rho_\gamma(e)
  }
$$

from the [[Cartesian product]] of the [[leaf space]] with the [[fundamental group]]. This function
is compatible with the [[group]]-structure on $\pi_1(X,x)$, in that the following [[commuting diagram|diagrams commute]]:

$$
  \array{
    F_x \times \{const_x\} && \longrightarrow && F_x \times \pi_1(X,x)
    \\
    & {}_{\mathllap{id}}\searrow && \swarrow_{\mathrlap{\rho}}
    \\
    && F_x
  }
  \;\;\;\;\;\;
  \left(
  \array{
    \text{the neutral element,}
    \\
    \text{i.e. the constant loop,}
    \\
    \text{acts trivially}
  }
  \right)
$$

and

$$
  \array{
    F_x \times \pi_1(X,x) \times \pi_1(X,x)
      &\overset{\rho \times id}{\longrightarrow}&
    F_x \times \pi_1(X,x)
    \\
    {}^{\mathllap{id \times ((-)\cdot(-))}}\downarrow && \downarrow^{\mathrlap{\rho}}
    \\
    F_x \times \pi_1(X,x)
      &\underset{\rho}{\longrightarrow}&
    F_x
  }
  \;\;\;\;\;\;
  \left(
  \array{
    \text{acting with two group elements }
    \\
    \text{is the same as}
    \\
    \text{first multiplying them}
    \\
    \text{ and then acting with their product element}
  }
  \right)
  \,.
$$

One says that $\rho$ is an _[[action]]_ or _[[permutation representation]]_ of $\pi_1(X,x)$ on $F_x$.

For $G$ any [[group]], then there is a [[category]] $G Set$ whose [[objects]] are [[sets]]
equipped with an [[action]] of $G$, and whose [[morphisms]] are [[function|functions]] which respect
these actions. The above construction yields a [[functor]]

$$
  Cov(X) \longrightarrow \pi_1(X,x) Set
  \,.
$$

=--

+-- {: .num_example }
###### Example
**(three-sheeted covers of the circle)**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/The3SheetedCoveringsOfTheCircle.png" width="150">
</div>

There are, up to [[isomorphism]], three different 3-sheeted [[covering spaces]] of the [[circle]] $S^1$.

The one from example \ref{kForlCovringOfCircle} for $k = 3$. Another one. And the trivial one.
Their corresponding [[permutation actions]] may be seen from the pictures on the right.
> graphics grabbed from [Hatcher](homotopy+equivalence#Hatcher)

=--

We are now ready to state the main theorem about the [[fundamental group]]. Except that it
does require the following slightly technical condition on the base topological space.
This condition is satisfied for all "reasonable" topological spaces:

+-- {: .num_defn #SemiLocallySimplyConnected}
###### Definition
**(semi-locally simply connected)**

A [[topological space]] $X$ is called

1. _[[locally path-connected]]_ if for every point $x \in X$ and for every [[neighbourhood]] $x \in U \subset X$ there
   exists a neighbourhood $x \in V \subset U$ such that $V$ is [[path-connected topological space|path-connected]] (def. \ref{pi0});

1. _[[semi-locally simply connected topological space|semi-locally simply connected]]_ if every point $x \in X$ has a [[neighbourhood]] $x \in U \subset X$ such that the induced morphism of [[fundamental groups]] $\pi_1(U,x) \to \pi_1(X,x)$ is trivial (i.e. sends everything to the [[neutral element]]).

=--



+-- {: .num_theorem #FundamentalTheoremOfCoveringSpaces}
###### Theorem
**([[fundamental theorem of covering spaces]])**

Let $X$ be a [[topological space]] which is [[connected topological space|path-connected]] (def. \ref{pi0}),
[[locally path-connected topological space|locally path connected]] (def. \ref{SemiLocallySimplyConnected})
and [[semi-locally simply connected topological space|semi-locally simply connected]] (def. \ref{SemiLocallySimplyConnected}). Then
for any $x \in X$ the functor
$$
  Fib_x \;\colon\; Cov(X) \overset{}{\longrightarrow} \pi_1(X,x) Set
  \,.
$$
from def. \ref{ActionOfFundamentalGroupOnFibersOfCovering} that describes
the [[action]] of the [[fundamental group]] of $X$ on the set of [[leaves]] over $x$
has the following property:

1. every [[isomorphism class]] of $\pi_1(X,x)$-[[actions]] is in the image of the functor (one says: the functor is _[[essentially surjective functor|essentially surjective]]_);

1. for any two covering spaces $E_1, E_2$ of $X$ then the map on [[hom-sets|morphism sets]]

   $$
     Fib_x \;\colon\; Hom_{Cov(X)}(E_1, E_2) \longrightarrow Hom( Fib_x(E_1), Fib_x(E_2) )
   $$

   is a [[bijection]] (one says the functor is a _[[fully faithful functor]]_ ).


A functor with these two properties one calls an _[[equivalence of categories]]_:

$$
  Cov(X) \overset{\simeq}{\longrightarrow} \pi_1(X,x) Set
  \,.
$$

=--

This has some interesting implications:

Every sufficiently nice topological space $X$ as above has a covering which is [[simply connected topological space|simply connected]]
(def. \ref{SimplyConnected}). This is the covering corresponding, under the [[fundamental theorem of covering spaces]]
(theorem \ref{FundamentalTheoremOfCoveringSpaces}) to the action of $\pi_1(X)$ on itself.
This is called the _[[universal covering space]]_ $\hat X \to X$. The above theorem implies that the
[[fundamental group]] itself may be recovered as the [[automorphisms]] of the universal covering space:

$$
  \pi_1(X) \simeq Aut_{Cov_{/X}}(\hat X, \hat X)
  \,.
$$


+-- {: .num_example #FundamentalGroupOfTheCircle}
###### Example
**(computing the fundamental group of the circle)**

The covering $\exp(2\pi i(-)) \;\colon\; \mathbb{R}^1 \to S^1$ from example \ref{CoveringOfCircleByRealLine}
is [[simply connected topological space|simply connected]] (def. \ref{SimplyConnected}),  hence must be the [[universal covering space]], up to [[homeomorphism]].

It is fairly straightforward to see that the only [[homeomorphisms]] from $\mathbb{R}^1$ to itself
over $S^1$ are given by [[integer]] translations by $n \in \mathbb{N} \hookrightarrow \mathbb{R}$:

$$
  \array{
    \mathbb{R}^1
      &&
        \underoverset{\simeq}{t \mapsto t + n}{\longrightarrow}
      &&
    \mathbb{R}^1
    \\
    & {}_{\mathllap{\exp(2 \pi i(-))}}\searrow && \swarrow_{\mathrlap{\exp(2 \pi i(-))}}
    \\
    && S^1
  }
  \,.
$$

Hence

$$
  Aut_{Cov_{/S^1}}(\hat S^1, \hat S^1) \simeq \mathbb{Z}
$$

and hence the [[fundamental group]] of the [[circle]] is the additive group of [[integers]]:

$$
  \pi_1(S^1) \simeq \mathbb{Z}
  \,.
$$

=--

$\,$

***

$\,$



## References

Introductory textbooks to topology include

* {#Munkres75} [[James Munkres]], _Topology_, Prentice Hall 1975 (2000)

* {#Lawson03} Terry Lawson, _Topology: A Geometric Approach_, Oxford University Press (2003) ([pdf](http://users.metu.edu.tr/serge/courses/422-2014/supplementary/TGeometric.pdf))

See also

* [[Alan Hatcher]], _[Algebraic Topology](https://www.math.cornell.edu/~hatcher/AT/ATpage.html)_

and see also the references at _[[algebraic topology]]_.

Lecture notes include

* [[Friedhelm Waldhausen]], _Topologie_ ([pdf](https://www.math.uni-bielefeld.de/~fw/ein.pdf))

* Alex Kuronya, _Introduction to topology_, 2010 ([pdf](https://www.uni-
frankfurt.de/64271720/TopNotes_Spring10.pdf))

* Anatole Katok, Alexey Sossinsky, _Introduction to modern topology and geometry_ ([pdf](http://www.personal.psu.edu/axk29/MASS-07/Background-forMASS.pdf))

See also

* [[Topospaces]], a Wiki with basic material on topology.
