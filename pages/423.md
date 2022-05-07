

{:principle: .num_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


> This page is about topology as a **field of [[mathematics]]**.  For topology as a **[[structured set|structure]]** on a [[set]], see _[[topological space]]_.

> Parts of this page exists also in a German language version, see at _[[Topologie]]_.

***

#Contents#
* table of contents
{:toc}

## Idea

__Topology__ is one of the basic fields of [[mathematics]].  The term is also used for a particular structure in a [[topological space]]; see [[topological structure]] for that.

The subject of topology deals with the expressions of [[continuous map|continuity]] and [[boundary]], and studying the geometric properties of (originally: [[metric space|metric]]) [[spaces]] and relations of subspaces, which do not change under continuous deformations, regardless to other (such as in their metric properties).

Topology as a structure enables one to model [[continuity]] and [[convergence]] locally. More recently, in metric spaces, topologists and geometric group theorists started looking at asymptotic properties at large, which are in some sense dual to the standard topological structure and are usually referred to as _coarse topology_.

There are many cousins of the concept of [[topological spaces]], e.g. [[sites]], [[locales]], [[topoi]], [[higher topoi]], [[uniformity spaces]] and so on, which specialize or generalize some aspect or structure usually found in [[Top]].

One of the tools of topology, [[homotopy theory]], has long since crossed the boundaries of topology and applies to many other areas, thanks to many examples and motivations as well as of abstract categorical frameworks for homotopy like Quillen [[model categories]], Brown's [[category of fibrant objects|categories of fibrant objects]] and so on.


## Introduction
 {#Introduction}

The following gives a quick introduction to some of the core concepts and tools of topology:

* _[Continuity](#Continuity)_

* _[Topological spaces](#TopologicalSpaces)_

* _[Homeomorphism](#Homeomorphisms)_

* _[Homotopy](#Homotopy)_

* _[Connected components](#ConnectedComponents)_

* _[Fundamental group](#FundamentalGroups)_

* _[Covering spaces](#CoveringSpaces)_

A detailed introduction is going to be at _[[Introduction to Topology]]_.



### Continuity
 {#Continuity}

The key idea of topology is to study [[spaces]] with "[[continuous maps]]" between them. The concept of continuity was made precise first in [[analysis]], in terms of [[epsilontic analysis]] of [[open balls]], recalled as def. \ref{EpsilonDeltaDefinitionOfContinuity} below. Then it was realized that this has a more elegant formulation in terms of the more general concept of _[[open sets]]_, this is prop. \ref{ContinuityBetweenMetricSpacesInTermsOfOpenSets} below. Adopting the latter as the definition leads to the concept of [[topological spaces]], def. \ref{TopologicalSpace} below.


First recall the basic concepts from [[analysis]]:

+-- {: .num_defn #MetricSpace}
###### Definition
**(metric space)**

A _[[metric space]]_ is

1. a [[set]] $X$ (the "underlying set");

1. a [[function]] $d \;\colon\; X \times X \to [0,\infty)$ (the "distance function") from the [[Cartesian product]] of the set with itself to the [[nonnegative number|non-negative]] [[real numbers]]

such that for all $x,y,z \in X$:

1. $d(x,y) = 0 \;\;\Leftrightarrow\;\; x = y$

1. (symmetry) $d(x,y) = d(y,x)$

1. ([[triangle inequality]]) $d(x,y)+ d(y,z) \geq d(x,z)$.

=--


+-- {: .num_example #NormedVectorSpaceBecomesMetricSpace}
###### Example

Every [[normed vector space]] $(V, {\vert - \vert})$
becomes a [[metric space]] according to def. \ref{MetricSpace} by setting

$$
  d(x,y) \coloneqq {\vert x-y \vert}
  \,.
$$

=--


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

The function $f$ is called just _continuous_ if it is continuous at every point $x \in X$.

=--

We now reformulate this analytic concept in terms of the simple but important concept of _[[open sets]]_:

+-- {: .num_defn #OpenBalls}
###### Definition
**(open ball)**

Let $(X,d)$, be a [[metric space]]. Then for every element $x \in X$ and every  $\epsilon \in \mathbb{R}_+$ a [[positive number|positive]] [[real number]], write

$$
  B^\circ_x(\epsilon)
    \;\coloneqq\;
  \left\{
    y \in X \;\vert\; d(x,y) \lt \epsilon
  \right\}
$$

for the [[open ball]] of [[radius]] $\epsilon$ around $x$.

=--



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



+-- {: .num_prop #ContinuityBetweenMetricSpacesInTermsOfOpenSets}
###### Proposition
**(rephrasing continuity in terms of open sets)**

A [[function]] $f \colon X \to Y$ between [[metric spaces]] (def. \ref{MetricSpace}) is continuous in the [[epsilontic analysis|epsilontic]] sense of def. \ref{EpsilonDeltaDefinitionOfContinuity} precisely if it has the property that its [[pre-images]] of [[open subsets]] of $Y$ (in the sense of def. \ref{OpenSubsetsOfAMetricSpace}) are open subsets of $X$.

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



### Topological spaces
 {#TopologicalSpaces}

Therefore we should pay attention to [[open subsets]]. It turns out that the following closure
property is what _characterizes_ the concept:

+-- {: .num_prop }
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

This motivates the following generalized definition:

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

A _[[topological space]]_ is a set $X$ equipped with such a [[topology]].

=--

The following shows all the topologies on the 3-element set (up to permutation of elements)

<img src="https://ncatlab.org/nlab/files/TopologiesOn3ElementSet.png" width="400">

> graphics grabbed from [Munkres 75](#Munkres75)

It is now immediate to formally implement the

+-- {: principle}
**principle of continuity**

$\,$ $\,$ _Pre-Images of open subsets are open._

=--

+-- {: .num_defn #ContinuousMaps}
###### Definition
**(continuous maps)**

A _[[continuous function]]_ between [[topological spaces]]

$$
  f \colon (X, \tau_X) \to (Y, \tau_Y)
$$

is a [[function]] between the underlying sets,

$$
  f \colon X \longrightarrow Y
$$

such that [[pre-images]] under $f$ of open subsets of $Y$ are open subsets of $X$.


=--


The simple definition of [[open subsets]] and the simple _principle of continuity_ gives topology its fundamental and universal flavor. The combinatorial nature of these definitions makes
topology closely related to [[formal logic]] (for more on this see at _[[locale]]_).


+-- {: .num_remark}
###### # Remark
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



Our motivating example now reads:

+-- {: .num_example #MetricTopology}
###### Example
**(metric topology)**

Let $(X,d)$ be a [[metric space]]. Then the collection of open subsets in def. \ref{OpenSubsetsOfAMetricSpace} constitutes a _[[topological space|topology]]_ on the set $X$, making it a _[[topological space]]_ in the sense of def. \ref{TopologicalSpace}. This is called the _[[metric topology]]_.

Stated more concisely: the [[open balls]] in a metric space constitute a "[[basis of a topology|basis]]" for the [[metric topology]].

=--


One point of the general definition of "[[topological space]]" is that it admits constructions which intuitively should exist on "continuous spaces", but which do not in general exist, for instance, as metric spaces:

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



### Homeomorphism
 {#Homeomorphisms}

With the [[objects]] ([[topological spaces]]) and the [[morphisms]] ([[continuous maps]]) of the [[category]] [[Top]] of topology thus defined, we obtain the concept of "sameness" in topology.

To make this precise, one says that a [[morphism]]

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

Hence this is a [[continuous function]]

$$
  f \;\colon\; X \longrightarrow Y
$$

such that there exists an [[inverse]] [[morphism]], namely a [[continuous function]] the other way around

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

The open [[interval]] $(-1,1)$ is [[homeomorphic]] to all of the [[real line]]

$$
  (-1,1) \underset{homeo}{\simeq} \mathbb{R}^1
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

As topological spaces, the [[interval]] with its two endpoints identified is [[homeomorphic]] (def. \ref{Homeomorphism}) to the standard [[circle]]:

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
  t \mapsto (cos(2\pi t), sin(2\pi t))
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
###### # Theorem
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

$\,$


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
 {#FundamentalGroups}


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



## Basic facts
 {#BasicFacts}

* [[Hausdorff spaces are sober]], [[schemes are sober]]

* [[CW-complexes are Hausdorff]]

* [[compact Hausdorff spaces are normal]]

* [[continuous image of a compact space is compact]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

* [[quotient projections out of compact Hausdorff spaces are closed precisely if the codomain is Hausdorff]]




## Central theorems
 {#CentralTheorems}

* [[Tietze extension theorem]]

* [[Tychonoff theorem]]

* [[Heine-Borel theorem]]

* [[topological invariance of dimension]]

* [[Brouwer's fixed point theorem]]

* [[Jordan curve theorem]]



## Related entries
 {#RelatedEntries}

The following is an (incomplete) list of available $n$Lab entries related to topology.


### Topological spaces

* [[Top]] [[CW-complex]], [[general topology]]
* [[induced topology]], [[subspace]], [[interior]], [[boundary]], [[closure]]

* [[product topological space]], [[disjoint union topological space]]

* [[sphere]], [[metric space]], [[metrizable space]]
* [[topological space]], [[continuous map]], [[homeomorphism]], [[neighborhood]]
* [[pointed space]], [[contractible space]], [[connected space]], [[second countable space]]
* [[convergence space]], [[pretopological space]], [[pseudotopological space]], [[coarse topology]]
* [[metric space]], [[filtered space]], [[connected filtered space]], [[complete space]], [[net]], [[Polish space]]
* [[separation axioms]], [[Hausdorff space]], [[regular space]], [[normal space]]
* [[noetherian topological space]], [[irreducible topological space]]
* [[compact space]], [[locally compact space]], [[compactum]], [[paracompact space]]
* [[Frechet-Uryson space]], [[sequential space]], [[uniform space]]
* [[convenient category of topological spaces]], [[compactly generated space]]
* [[nice topological space]], [[nice category of spaces]]
* [[pointless topology]], [[locale]], [[cover]], [[site]], [[ringed space]]
[[sphere]]
* [[Sierpinski space]], [[Warsaw circle]]

See also [[examples in topology]].

### Manifolds and generalizations

* [[manifold]], [[smooth manifold]], [[generalized smooth space]], [[diffeological space]], [[smooth space]], [[Froelicher space]]
* [[differential topology]], [[microbundle]], [[cobordism]], [[derived smooth manifold]]

* [[low-dimensional topology]], [[3-manifold]]

### Algebraic topology and homotopy theory

* [[homotopy]], [[homotopy inverse]], [[homotopy theory]], [[homotopy equivalence]], [[rational homotopy theory]]
* [[shape theory]], [[algebraic topology]], [[basic problems of algebraic topology]]

* [[model category]], [[category of fibrant objects]], [[Quillen adjunction]], [[Quillen equivalence]], [[category with weak equivalences]],

* [[model 2-category]], [[model stack]]

* [[Reedy category]], [[Reedy model structure]], [[generalized Reedy category]]
* [[model structure on chain complexes]], [[model structure on crossed complexes]]
* [[homotopy hypothesis]], [[homotopy theory of Grothendieck]], [[test category]]

* [[homotopy limit]], [[homotopy colimit]], [[homotopy pullback]], [[homotopy image]], [[homotopy coherent category theory]], [[homotopy coherent nerve]], [[Brown representability theorem]]
* [[homotopy type]], [[homotopy 1-type]], [[homotopy 2-type]], [[homotopy 3-type]], [[homotopy n-type]]
* [[deformation retract]], [[neighborhood retract]], [[Postnikov system]]
* [[fundamental group]], [[homotopy group]], [[suspension]], [[Freudenthal suspension theorem]], [[delooping]]
* [[loop space]], [[free loop space object]],
* [[cup product]], [[Dold-Thom theorem]]

#### Topological homotopy theory

* [[classical model structure on topological spaces]]

* [[topological group]], [[H-space]], [[co-H-space]]
* [[principal bundle]], [[fiber bundle]], [[vector bundle]], [[principal 2-bundle]], [[trivial bundle]]
* [[fibration]], [[Hurewicz fibration]], [[Hurewicz connection]], [[homotopy lifting property]], [[Dold fibration]]
* [[homotopy extension property]], [[Hurewicz cofibration]], [[deformation retract]], [[model structure on topological spaces]], [[Strøm's theorem]]
* [[cocylinder]], [[cylinder object]], [[path object]], [[mapping cone]], [[path groupoid]], [[path n-groupoid]], [[fundamental groupoid]]
* [[classifying space]], [[Eilenberg-MacLane space]],[[Moore space]], [[Moore path category]]
* [[spectrum]], [[smash product of spectra]], [[symmetric spectrum]], [[stable (infinity,1)-category]], [[commutative ring spectrum]]

#### Simplicial homotopy theory

* [[classical model structure on simplicial sets]]

* [[simplicial set]], [[simplex category]], [[simplicial identities]], [[simplicial object]], [[cosimplicial object]]
* [[simplicial complex]], [[singular simplicial complex]],
* [[boundary of a simplex]], [[simplicial skeleton]], [[category of simplices]]
* [[combinatorial spectrum]], [[simplicial groupoid]], [[simplicial model category]]
* [[simplicially enriched category]], [[quasicategory]], [[Segal category]], [[complete Segal space]]
* [[Kan fibration]], [[Kan complex]], [[nerve]], [[nerve and realization]], [[simplicial homotopy]], [[simplicial homotopy group]], [[simplicial local system]]
* [[simplicial presheaf]], [[local model structure on simplicial presheaves]], [[local model structure on simplicial sheaves]]
* [[marked simplicial set]], [[model structure on marked simplicial over-sets]], [[infinity topos]], [[Higher Topos Theory]]
* [[dendroidal set]], [[model structure on dendroidal sets]], [[cubical set]], [[cellular set]], [[cyclic object]], [[Theta space]]




### Sheaves, stacks, cohomology

* [[site]], [[sheaf]], [[flabby sheaf]], [[local epimorphism]], [[etale space]], [[hypercover]]
* [[topos]]
* [[cohomology]], [[sheaf cohomology]], [[abelian sheaf cohomology]], [[local system]], [[category of sheaves]]
* [[Čech cohomology]], [[Bredon cohomology]], [[twisted cohomology]], [[twisting cochain]]
* [[nonabelian algebraic topology]], [[nonabelian cocycle]], [[nonabelian cohomology]]
* [[principal infinity-bundle]], [[BrownAHT]], [[category of fibrant objects]]
* [[topological K-theory]], [[gerbe]], [[twisted K-theory]], [[Karoubi K-theory]], [[differential K-theory]], [[K-theory spectrum]]
* [[de Rham cohomology]], [[string topology]]
* [[Thom space]], [[Thom bundle]], [[fiber integration]], [[equivariant cohomology]]
* [[Poincaré duality]], [[Spanier-Whitehead duality]]
* [[generalized cohomology]], [[generalized (Eilenberg-Steenrod) cohomology]], [[generalized (Eilenberg-Steenrod) homotopy]]
* [[topological stack]], [[orbispace]]
* [[topological quantum field theory]], [[tmf]], [[cobordism hypothesis]], [[topological T-duality]]
* [[characteristic class]], [[Chern-Weil theory]]

### Non-commutative topology

* [[noncommutative topology]]

  * [[C-star-algebra]], [[KK-theory]]

### Computational Topology

* [[computational topology]]
* [[topological data analysis]]
* [[sources in computational topology]]

## References

A canonical compendium is

* {#Bourbaki71} [[Nicolas Bourbaki]], chapter 1 _Topological Structures_ of _Elements of Mathematics III: General topology_, Springer 1971, 1990

Textbook accounts:

* {#Kelley55} [[John Kelley]], _General Topology_, Graduate Texts in Mathematics, Springer 1955

* {#Munkres75} [[James Munkres]], _Topology_, Prentice Hall 1975 (2000)

* {#Lawson03} Terry Lawson, _Topology: A Geometric Approach_, Oxford University Press (2003) ([pdf](http://users.metu.edu.tr/serge/courses/422-2014/supplementary/TGeometric.pdf))

* {#Vickers89} [[Steven Vickers]], _Topology via Logic_, Cambridge University Press (1989) ([pdf](https://pdfs.semanticscholar.org/6da4/9fba6462a5c3e6b528a8b3e8be3a1c1e743d.pdf))

* {#BradleyBrysonTerilla20} [[Tai-Danae Bradley]], [[Tyler Bryson]], [[John Terilla]], _Topology -- A categorical approach_, MIT Press 2020 ([ISBN:9780262539357](https://mitpress.mit.edu/books/topology), [web version](https://topology.pubpub.org/))

  > (with emphasis on tools from [[category theory]])

See also

* [[Alan Hatcher]], _[Algebraic Topology](https://www.math.cornell.edu/~hatcher/AT/ATpage.html)_

and see also the references at _[[algebraic topology]]_.

Lecture notes include

* [[Friedhelm Waldhausen]], _Topologie_ ([pdf](https://www.math.uni-bielefeld.de/~fw/ein.pdf))

* Alex Kuronya, _Introduction to topology_, 2010 ([pdf](https://www.uni-
frankfurt.de/64271720/TopNotes_Spring10.pdf))

* Anatole Katok, Alexey Sossinsky, _Introduction to modern topology and geometry_ ([pdf](http://www.personal.psu.edu/axk29/MASS-07/Background-forMASS.pdf))

* {#Schreiber17} [[Urs Schreiber]], _[[Introduction to Topology]]_, Bonn 2017

* {#Mueger18} [[Michael Müger]], _Topology for the working mathematician_, Nijmegen 2018 ([pdf](https://www.math.ru.nl/~mueger/topology.pdf))

Basic topology set up in [[intuitionistic mathematics]] is discussed in

* {#Waaldijk96} [[Frank Waaldijk]], _modern intuitionistic topology_, 1996 ([pdf](http://www.fwaaldijk.nl/modern%20intuitionistic%20topology.pdf))

See also

* [[Topospaces]], a Wiki with basic material on topology.
