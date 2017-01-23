

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


This page is about topology as a **field of [[mathematics]]**.  For topology as a **[[structured set|structure]]** on a [[set]], see _[[topological space]]_.

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

The following gives a basic introduction to some core concepts of topology.

* _[Continuity](#Continuity)_

* _[Topological spaces](#TopologicalSpaces)_

* _[Homeomorphism](#Homeomorphism)_


### Continuity
 {#Continuity}

The key idea of topology is to study [[spaces]] with "[[continuous maps]]" between them. The concept of continuity was made precise first in [[analysis]], in terms of [[epsilontic analysis]] of [[open balls]], recalled as def. \ref{EpsilonDeltaDefinitionOfContinuity} below. Then it was realized that this has a more elegant formulation in terms of more general [[open sets]], this is prop. \ref{ContinuityBetweenMetricSpacesInTermsOfOpenSets} below.


First recall the basic concepts from [[analysis]]:

+-- {: .num_defn #MetricSpace}
###### Definition

A _[[metric space]]_ is 

1. a [[set]] $X$ (the "underlying set");

1. a [[function]] $d \;\colon\; X \times X \to [0,\infty)$ (the "distance function") from the [[Cartesian product]] of the set with itself to the [[nonnegative number|non-negative]] [[real numbers]] 

such that for all $x,y,z \in X$:

1. $d(x,y) = 0 \;\Leftrightarrow\; x = y$

1. (symmetry) $d(x,y) = d(y,x)$

1. ([[triangle inequality]]) $d(x,y)+ d(y,z) \geq d(x,z)$.

=--


+-- {: .num_example}
###### Example

Every [[normed vector space]] $(V, {\Vert -\Vert})$
becomes a [[metric space]] according to def. \ref{MetricSpace} by setting

$$
  d(x,y) \coloneqq {\Vert x-y\Vert}
  \,.
$$

=--


+-- {: .num_defn #OpenBalls}
###### Definition

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


+-- {: .num_defn #EpsilonDeltaDefinitionOfContinuity}
###### Definition
**(epsilontic definition of continuity)**

For $(X,d_X)$ and $(Y,d_Y)$ two [[metric spaces]] (def. \ref{MetricSpace}), then a [[function]]

$$
  f \;\colon\; X \longrightarrow Y
$$

is said to be _continuous at a point $x \in X$_ if for every $\epsilon \gt 0$ there exists $\delta\gt 0$ such that 

$$
  d_X(x,y) \lt \delta \;\Rightarrow\; d_Y(f(x), f(y)) \lt \epsilon 
$$

or equivalently such that 

$$
  f(B_x^\circ(\delta)) \subset B^\circ_{f(x)}(\epsilon)
$$

where $B^\circ$ denotes the [[open ball]] (definition \ref{OpenBalls}).

The function $f$ is called just _continuous_ if it is continuous at every point $x \in X$.

=--

+-- {: .num_defn #OpenSubsetsOfAMetricSpace}
###### Definition

Let $(X,d)$ be a [[metric space]] (def. \ref{MetricSpace}). Say that

1. A _[[neighbourhood]]_ of a point $x \in X$ is a [[subset]] $x \in U \subset X$ which contains some [[open ball]] $B_x^\circ(\epsilon)$ around $x$ (def. \ref{OpenBalls}).

1. An _[[open subset]]_ of $X$ is a [[subset]] $U \subset X$ such that for every for $x \in U$ it also contains a [[neighbourhood]] of $x$.

=--


+-- {: .num_prop #ContinuityBetweenMetricSpacesInTermsOfOpenSets}
###### Proposition
**(rephrasing continuity in terms of open sets)**

A [[function]] $f \colon X \to Y$ between [[metric spaces]] (def. \ref{MetricSpace}) is continuous in the [[epsilontic analysis|epsilontic]] sense of def. \ref{EpsilonDeltaDefinitionOfContinuity} precisely if it has the property that its [[pre-images]] of [[open subsets]] of $Y$ (in the sense of def. \ref{OpenSubsetsOfAMetricSpace}) are open subsets of $X$.

=--

+-- {: .proof}
###### Proof

First assume that $f$ is continuous in the epsilontic sense. Then for $O_Y \subset Y$ any [[open subset]] and $x \in f^{-1(O_Y)}$ any point in the pre-image, we need to show that there exists a [[neighbourhood]] of $x$ in $U$. But by assumption there exists an [[open ball]] $B_x^\circ(\epsilon)$ with $f(B_X^\circ(\epsilon)) \subset O_Y$. Since this is true for all $x$, by definition this means that $f^{-1}(O_Y)$ is open in $X$.

Conversely, assume that $f^{-1}$ takes open subsets to open subsets. Then for every $x \in X$ and $B_{f(x)}^\circ(\epsilon)$ an [[open ball]] around its image, we need to produce an open ball $B_x^\circ(\delta)$ in its pre-image. But by assumption $f^{-1}(B_{f(x)}^\circ(\epsilon))$ contains a [[neighbourhood]] of $x$ which by definition means that it contains such an open ball around $x$.


=--



### Topological spaces
 {#TopologicalSpaces}


The collection of [[open subsets]] of a [[metric space]] in the sense of definition \ref{OpenSubsetsOfAMetricSpace} is readily seen to have the following property

+-- {: .num_prop }
###### Proposition

The collection of [[open subsets]] of a [[metric space]] $(X,d)$ as in def. \ref{OpenSubsetsOfAMetricSpace} has the following properties:

1. The [[intersection]] of any [[finite number]] of open subsets is again an open subset.

1. the [[union]] of any [[set]] of open subsets is again an open subset.

In particular the [[empty set]] is open (being the union of no subsets) and the whole set $X$ itself is open (being the intersection of no subsets).

=--

This motivates the following generalized definition:

+-- {: .num_defn #TopologicalSpaces}
###### Definition
**(topological spaces)**

Given a [[set]] $X$, then a _topology_ on $X$ is a collection of [[subsets]] of $X$ called the _[[open subsets]]_, hence a [[subset]] of the [[power set]]

$$
  \tau \subset P(X)
$$

such that this is closed under forming

1. finite [[intersections]];

1. arbitrary [[unions]].

A _[[topological space]]_ is a set $X$ equipped with a [[topology]].

A _[[continuous function]]_ between topological spaces $f \colon (X, \tau_X) \to (Y, \tau_Y)$ is a [[function]] between the underlying sets, such that [[pre-images]] under $f$ of open subsets of $Y$ are open subsets of $X$.

The [[composition]] of [[continuous functions]] is clearly [[associativity|associative]] and [[unitality|unital]], hence there is a [[category]] [[Top]] whose [[objects]] are [[topological spaces]] and whose [[morphisms]] are [[continuous functions]].

=--

Our motivating example now reads:

+-- {: .num_example #MetricTopology}
###### Example

Let $(X,d)$ be a [[metric space]]. Then the collection of open subsets in def. \ref{OpenSubsetsOfAMetricSpace} constitutes a _[[topological space|topology]]_ on the set $X$, making it a _[[topological space]]_ in the sense of def. \ref{TopologicalSpaces}. This is called the _[[metric topology]]_. Stated more concisely: the [[open balls]] in a metric space constitute the [[basis of a topology]] for the [[metric topology]].

=--


One point of the general definition of "[[topological space]]" is that it admits constructions which intuitively should exist on "continuous spaces", but which do not in general exist, for instance, as metric spaces:


+-- {: .num_defn #QuotientTopologicalSpace}
###### Definition
**(quotient topological space)**

Let $(X,\tau_X)$ be a [[topological space]] (def. \ref{TopologicalSpaces}) and let "$R_\sim \subset X \times X$" be an [[equivalence relation]] on its underlying set. Then the _[[quotient topological space]]_  has as underlying set the [[quotient set]] $X_{\sim}$, hence the set of [[equivalence classes]], and a subset $O \subset X_{\sim}$ is declared to be an [[open subset]] precisely if its [[preimage]] $\pi^{-1}(O)$ under the canonical [[projection map]]

$$
  \pi \colon X \to X_\sim
$$

is open on $X$.

(Also called the _[[final topology]]_ of the projection $\pi$.)

=--


+-- {: .num_defn #SubspaceTopology}
###### Definition
**(subspace topology)**

Let $(X, \tau_X)$ be a [[topological space]], and let $X_0 \hookrightarrow X$ be a [[subset]] of the underlying set. Then the corresponding _[[topological subspace]]_ has $X_0$ as its underlying set, and its open subsets are those subsets of $X_0$ which arise as restrictions of open subsets of $X$. 

(Also called the _[[initial topology]]_ of the inclusion map.)

=--

These two constructions of [[quotient topological spaces]] and of [[topological subspaces]] are in fact simple examples of [[colimits]] and of [[limits]] of topological spaces. The [[category]] [[Top]] of topological spaces has the convenient property that _all_ [[limits]] and [[colimits]] (over [[small diagrams]]) exist in it.



### Homeomorphism
 {#Homeomorphism}

With the [[objects]] ([[topological spaces]]) and the [[morphisms]] ([[continuous maps]]) of the [[category]] [[Top]] of topology thus defined, we obtain the concept of "sameness" in topology: 


+-- {: .num_defn #Homeomorphism}
###### Definition

An [[isomorphism]] in the [[category]] [[Top]] of [[topological spaces]] with [[continuous functions]] between them is called a [[homeomorphism]]. Hence this is a [[continuous function]]

$$
  f \;\colon\; X \longrightarrow Y
$$

such that there exists an [[inverse]] [[morphism]], namely a [[continuous function]] 

$$
  X \longleftarrow Y \;\colon\; f^{-1}
$$

such that 

$$
  f \circ f^{-1} = id_{Y} \;\;\;\;\; f^{-1} \circ f = id_{X}
  \,.
$$

=--


+-- {: .num_example #HomeomorphismBetweenTopologicalAndCombinatorialCircle}
###### Example

As topological spaces, the [[interval]] with its two endpoints identified is [[homeomorphism|homeomorphic]] (def. \ref{Homeomorphism}) to the standard [[circle]]:

$$
  [0,1]_{/(0 \sim 1)} \underset{homeo}{\simeq} S^1
  \,.
$$

More in detail: let

$$
  S^1 \hookrightarrow \mathbb{R}^2
$$

be the unit [[circle]] in the [[plane]] ($S^1 = \{(x,y) \in \mathbb{R}^2, x^2 + y^2 = 1\}$) equipped with the [[subspace topology]] (def. \ref{SubspaceTopology}) of $\mathbb{R}^2$ equipped with its standard [[metric topology]] (example \ref{MetricTopology}).

Moreover, let 

$$
  [0,1]_{/(0 \sim 1)}
$$

be the [[quotient topological space]] (def. \ref{QuotientTopologicalSpace}) obtained from the [[interval]] $[0,1] \subset \mathbb{R}^1$ with its [[subspace topology]] by applying the [[equivalence relation]] which identifies the two endpoints (and nothing else).

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

First of all it is immediate that $\tilde f$ is a [[continuous function]]. This follows immediately from the fact that $f$ is a [[continuous function]] and by definition of the [[quotient topology]] (def. \ref{QuotientTopologicalSpace}).

So we need to check that $\tilde f$ has a continuous inverse function. Clearly the restriction of $f$ itself to the open interval $(0,1)$ has a continuous inverse. It fails to have a continuous inverse on $[0,1)$ and on $(0,1]$ and fails to have an inverse at all on [0,1], due to the fact that $f(0) = f(1)$. But the relation quotiented out in $[0,1]_{/(0 \sim 1)}$ is exactly such as to fix this failure.

=--

+-- {: .num_example #OpenBallsHomeomorphicToRn}
###### Example

The open [[interval]] $(-1,1)$ is [[homeomorphism|homeomorphic]] to all of the [[real line]]

$$
  (0,1) \simeq_{homeo} \mathbb{R}^1
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

Generally, every [[open ball]] in $\mathbb{R}^n$ (\ref{OpenBalls}) is [[homeomorphism|homeomorphic]] to all of $\mathbb{R}^n$.


=--


Important examples of pairs of spaces that are _not_ homeomorphic include the following:


+-- {: .num_example }
###### Example

The [[2-sphere]] $S^2 = \{(x,y,z) \in \mathbb{R}^3 \vert x^2 + y^2 + z^2 = 1\}$ is _not_ homeomorphic to the [[torus]] $T^2 = S^1 \times S^1$.

Generally the [[homeomorphism]] class of a [[closed manifold|closed]] [[orientable]] [[surface]] is determined by the number of "holes" it has, its _[[genus of a surface|genus]]_.

=--



+-- {: .num_example #TopologicalInvarianceOfDimension}
###### Example
**([[topological invariance of dimension]])**

For $n_1, n_2 \in \mathbb{N}$ but $n_1 \neq n_2$, then the [[Cartesian spaces]] $\mathbb{R}^{n_1}$ and $\mathbb{R}^{n_2}$ are _not_ [[homeomorphism|homeomorphic]].

More generally, an [[open set]] in $\mathbb{R}^{n_1}$ is never homeomorphic to an open set in $\mathbb{R}^{n_2}$ if $n_1 \neq n_2$.

=--

The proof of example \ref{TopologicalInvarianceOfDimension} is surprisingly hard, given how obvious the statement seems intuitively. It requires tools from a field called _[[algebraic topology]]_ (notably [[Brouwer's fixed point theorem]]). We turn to some basics of [[algebraic topology]] now.


### Homotopy

We have seen above that for $n \geq 1$  then the [[open ball]] $B_0^\circ(1)$ in $\mathbb{R}^n$ is _not_ [[homeomorphism|homeomorphic]] to, notably, the point $\ast = \mathbb{R}^0$ (example \ref{OpenBallsHomeomorphicToRn}, example \ref{TopologicalInvarianceOfDimension}). Nevertheless, intuitively the $n$-ball is a "continuous deformation" of the point, obtained as the radius of the $n$-ball tends to zero.

This intuition is made precise by observing that there is a [[continuous function]] out of the [[product topological space]] with the closed interval

$$
  \eta \colon [0,1] \times B_0^\circ(1)  \longrightarrow \mathbb{R}^n
$$

which is given by rescaling:

$$
  (t,x) \mapsto t \cdot x
  \,.
$$

This continuously interpolates between the open ball and the point in that for $t = 1$ then it restricts to the defining inclusion $B_0^\circ(1)$, while for $t = 0$ then it restricts to the map constant on the origin.

We may summarize this situation by saying that there is a
[[diagram]] of [[continuous function]] of the form

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

Such "continuous deformations" are called _[[homotopies]]_.

+-- {: .num_defn #LeftHomotopy}
###### Definition

For $f,g\colon X \longrightarrow Y$ two [[continuous functions]] between [[topological spaces]] $X,Y$, then a **[[left homotopy]]** 

$$
  \eta \colon f \,\Rightarrow_L\, g
$$ 

is a [[continuous function]]

$$
  \eta \;\colon\; X \times I \longrightarrow Y
$$


out of [[product topological space]] with the standard interval, such that this fits into a [[commuting diagram]] of the form

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

(graphics grabbed from J. Tauber [here](http://jtauber.com/blog/2005/07/01/path_homotopy/))

=--

+-- {: .num_defn #HomotopyEquivalence}
###### Definition

A [[continuous function]] $f \;\colon\; X \longrightarrow Y$
is called a **[[homotopy equivalence]]** if there exists a 
continuous function the other way around,
$g \;\colon\; Y \longrightarrow X$, and [[left homotopies]], def. \ref{LeftHomotopy}, from the two composites to the identity:

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

Any [[open ball]] or closed ball, hence any [[Cartesian space]] is homotopy equivalent to the point

$$
  \mathbb{R}^n \underset{homotopy}{\simeq} \ast
  \,.
$$



=--

+-- {: .num_example}
###### Example

The following are three homotopy equivalences to the disk with two points removed:

<img src="https://ncatlab.org/nlab/files/HomotopyEquivalentsToBiAnnulus.png" width="400">

> graphics grabbed from [Hatcher](#Hatcher)

=--




### Fundamental group


## Related entries
 {#RelatedEntries}

Here we exclude the entries on [[topos theory]] which may also be viewed as an approach to topology (but also geometry, logic...) as it is comprehensively linked from entries [[topos]], [[topos theory]], [[infinity topos]], [[Grothendieck topology]], [[site]]. 

### Topological spaces

* [[Top]] [[CW-complex]], [[general topology]]
* [[induced topology]], [[subspace]], [[interior]], [[boundary]], [[closure]]
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

* [[low-dimensional topology]]

### Algebraic topology and homotopy theory in general

* [[homotopy]], [[homotopy inverse]], [[homotopy theory]], [[homotopy equivalence]], [[rational homotopy theory]]
* [[shape theory]], [[algebraic topology]], [[basic problems of algebraic topology]]
* [[homotopy limit]], [[homotopy colimit]], [[homotopy pullback]], [[homotopy image]], [[homotopy coherent category theory]], [[homotopy coherent nerve]], [[Brown representability theorem]]
* [[homotopy type]], [[homotopy 1-type]], [[homotopy 2-type]], [[homotopy 3-type]], [[homotopy n-type]]
* [[deformation retract]], [[neighborhood retract]], [[Postnikov system]]
* [[fundamental group]], [[homotopy group]], [[suspension]], [[Freudenthal suspension theorem]], [[delooping]]
* [[loop space]], [[free loop space object]],
* [[cup product]], [[Dold-Thom theorem]]
* [[topological group]], [[H-space]], [[co-H-space]]
* [[principal bundle]], [[fiber bundle]], [[vector bundle]], [[principal 2-bundle]], [[trivial bundle]]
* [[fibration]], [[Hurewicz fibration]], [[Hurewicz connection]], [[homotopy lifting property]], [[Dold fibration]]
* [[homotopy extension property]], [[Hurewicz cofibration]], [[deformation retract]], [[model structure on topological spaces]], [[Strøm's theorem]]
* [[cocylinder]], [[cylinder object]], [[path object]], [[mapping cone]], [[path groupoid]], [[path n-groupoid]], [[fundamental groupoid]]
* [[classifying space]], [[Eilenberg-MacLane space]],[[Moore space]], [[Moore path category]]
* [[spectrum]], [[smash product of spectra]], [[symmetric spectrum]], [[stable (infinity,1)-category]], [[commutative ring spectrum]]
* [[model category]], [[model 2-category]], [[model stack]], [[Quillen adjunction]], [[Quillen equivalence]], [[category with weak equivalences]], [[category of fibrant objects]]
* [[Reedy category]], [[Reedy model structure]], [[generalized Reedy category]]
* [[model structure on chain complexes]], [[model structure on crossed complexes]]
* [[homotopy hypothesis]], [[homotopy theory of Grothendieck]], [[test category]]

#### Simplicial sets and related notions

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

* [[sheaf]], [[flabby sheaf]], [[local epimorphism]], [[etale space]], [[hypercover]]
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

See also the references at _[[algebraic topology]]_.

Introductions to topology:

* [[Friedhelm Waldhausen]], _Topologie_ ([pdf](https://www.math.uni-bielefeld.de/~fw/ein.pdf))

* Terry Lawson, _Topology: A Geometric Approach_, Oxford University Press (2003) ([pdf](http://users.metu.edu.tr/serge/courses/422-2014/supplementary/TGeometric.pdf))

* Alex Kuronya, _Introduction to topology_, 2010 ([pdf](https://www.uni-
frankfurt.de/64271720/TopNotes_Spring10.pdf))

* Anatole Katok, Alexey Sossinsky, _Introduction to modern topology and geometry_ ([pdf](http://www.personal.psu.edu/axk29/MASS-07/Background-forMASS.pdf))


See also

* [[Topospaces]], a Wiki with basic material on topology.
