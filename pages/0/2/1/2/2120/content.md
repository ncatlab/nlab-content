
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Continuous maps
* table of contents
{: toc}

## Idea

A [[function]] $f \colon X \to Y$ is called _continuous_ if its values $f(x)$ do not "jump" with variation of its argument $x$, unless $x$ itself "jumps".  Roughly speaking, if $x_1 \approx x_2$, then $f(x_1) \approx f(x_2)$.  (This can be made into a precise definition in [[nonstandard analysis]] if care is taken about the domains of these variables.)

In order to make this precise (in standard analysis) one needs some concept of [[neighbourhoods]] of elements of $X$ and $Y$. 

For instance if $X$ and $Y$ carry structure of [[metric spaces]], then one may say that $f$ is continuous if for every point $x \in X$ and for every small [[open ball]] around its image $f(x)$ in $Y$, there exists a sufficiently small open ball around $x \in X$  which is still mapped by $f$ into that target open ball.  This definition turns out to have more elegant formulation that needs to mention neither the points of $x$ nor the radii of open balls around points: the [[metric]] induces a concept of [[open subsets]] and $f$ is continuous precisely if [[preimages]] under $f$ of [[open subsets]] in $Y$ are still open subsets in $X$.

This then is the general definition of continuity of a function $f$ between [[topological spaces]]: 

A function between [[topological spaces]] is _continuous_ precisely if its [[preimages]] of [[open subsets]] are again open subsets.

Continuous maps are the [[homomorphisms]] between [[topological spaces]].
In other words, the collection of [[topological spaces]] forms a [[category]], often denoted _[[Top]]_, whose [[morphisms]] are the continuous functions.

Further generalization of the concept of continuity exists, for instance to 
_[[locales]]_ (and then to [[toposes]]) or to _[[convergence spaces]]_.  (See also at _[[continuous space]]_.)


## Definitions

### The epsilontic definition for metric spaces
 {#EpsilonticDefinition}

We state the definition of continuity in terms of [[epsilontic analysis]], definition \ref{EpsilonDeltaDefinitionOfContinuity} below. First recall the relevant concepts:

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

This definition is equivalent to a more abstract one, which does not explicitly refer to points or radii anymore:

+-- {: .num_defn #OpenSubsetsOfAMetricSpace}
###### Definition

Let $(X,d)$ be a [[metric space]] (def. \ref{MetricSpace}). Say that

1. A _[[neighbourhood]]_ of a point $x \in X$ is a [[subset]] $x \in U \subset X$ which contains some [[open ball]] $B_x^\circ(\epsilon)$ around $x$ (def. \ref{OpenBalls}).

1. An _[[open subset]]_ of $X$ is a [[subset]] $U \subset X$ such that for every for $x \in U$ it also contains a [[neighbourhood]] of $x$.

=--

+-- {: .num_remark}
###### Remark

The collection of open subsets in def. \ref{OpenSubsetsOfAMetricSpace} constitutes a _[[topological space|topology]]_ on the set $X$, making it a _[[topological space]]_. This is called the _[[metric topology]]_. Stated more concisely: the [[open balls]] in a metric space constitute the [[basis of a topology]] for the [[metric topology]].

=--


+-- {: .num_prop}
###### Proposition

A [[function]] $f \colon X \to Y$ between [[metric spaces]] (def. \ref{MetricSpace}) is continuous in the [[epsilontic analysis|epsilontic]] sense of def. \ref{EpsilonDeltaDefinitionOfContinuity} precisely if it has the property that its [[pre-images]] of [[open subsets]] of $Y$ (in the sense of def. \ref{OpenSubsetsOfAMetricSpace}) are open subsets of $X$.

=--

+-- {: .proof}
###### Proof

First assume that $f$ is continuous in the epsilontic sense. Then for $O_Y \subset Y$ any [[open subset]] and $x \in f^{-1(O_Y)}$ any point in the pre-image, we need to show that there exists a [[neighbourhood]] of $x$ in $U$. But by assumption there exists an [[open ball]] $B_x^\circ(\epsilon)$ with $f(B_X^\circ(\epsilon)) \subset O_Y$. Since this is true for all $x$, by definition this means that $f^{-1}(O_Y)$ is open in $X$.

Conversely, assume that $f^{-1}$ takes open subsets to open subsets. Then for every $x \in X$ and $B_{f(x)}^\circ(\epsilon)$ an [[open ball]] around its image, we need to produce an open ball $B_x^\circ(\delta)$ in its pre-image. But by assumption $f^{-1}(B_{f(x)}^\circ(\epsilon))$ contains a [[neighbourhood]] of $x$ which by definition means that it contains such an open ball around $x$.


=--


### For topological spaces

+-- {: .num_defn #topological}
###### Definition

A [[function]] $f \;\colon\; X\to Y$ between [[topological spaces]] is a __continuous map__ (or is said to be *continuous*) if for every [[open subset]] $U \subset Y$, the [[preimage]] $f^{-1}(U)$ is an open subset $X$.

=--

In [[nonstandard analysis]], this is equivalent to

+-- {: .num_defn #nonstandard}
###### Definition

A [[function]] $f \;\colon\; X\to Y$ between [[topological spaces]] is a __continuous map__ (or is said to be *continuous*) if for every [[standard point]] $x_1$ and every [[hyperpoint]] $x_2$, if $x_1$ and $x_2$ are [[adequality|adequal]] (infinitely close, or in other words if $x_2$ is in the [[halo]] of $x_1$), then $f(x_1)$ and $\multiscripts{^*}f{}(x_2)$ are adequal (where $\multiscripts{^*}f{}$ is the [[nonstandard extension]] of $f$).  Equivalently, $f$ is continuous iff $\multiscripts{^*}f{}$ is [[microcontinuous function|microcontinuous]].

=--



### Further variants

A function $f$ between [[convergence spaces]] is __continuous__ if for any [[filter]] $F$ such that $F \to x$, it follows that $f(F) \to f(x)$, where $f(F)$ is the filter generated by the filterbase $\{F(A) \;|\; A \in F\}$.

A __continuous map__ between [[locales]] is simply a [[frame]] [[homomorphism]] in the opposite direction.  Equivalently (via the [[adjoint functor theorem]]), it may be defined as a homomorphism of [[inflattices]] whose [[left adjoint]] preserves finitary [[meets]] (and hence is a frame homomorphism).


## Properties

Since continuity is defined in terms of *preservation of property* (namely preserving "openness" under preimages), it is natural to ask what other properties they preserve.  
Also, when a property is not always preserved it is useful to label those maps which do preserve it for closer study.


### Properties preserved

\begin{prop}\label{PropertiesPreservedByAContinuousFunction}

Under a [[continuous function]]:

1. the [[preimage]] of an [[open subset]] is open;

1. the [[preimage]] of an [[closed subset]] is closed;

1. the [[image]] of a [[connected space|connected subset]] is again connected;

1. theimage of a [[compact space|compact subset]] is again compact (see at _[[continuous images of compact spaces are compact]]_).

\end{prop}

### Special maps

1. The preimage of a compact set need not be compact; a continuous map for which this is true is known as a __[[proper map]]__.

2. The image of an open set need not be open; a continuous map for which this is true is said to be an __[[open map]]__.  (Technically, an open map is any [[function]] with just this property.)

3. The image of an closed set need not be closed; a continuous map for which this is true is said to be an __[[closed map]]__.  (Technically, a closed map is any function with just this property.)

4. A continuous map of topological spaces which is invertible as a function of sets is a __[[homeomorphism]]__ if the [[inverse function]] is a continuous map as well.


### Special cases in specific contexts

Although these don't make sense for arbitrary topological spaces (convergence spaces, locales, etc), they are special kinds of continuous maps in contexts such as [[metric spaces]]:

* [[uniformly continuous maps]],
* [[Lipschitz maps]],
* [[short maps]],
* [[differentiable maps]],
* [[smooth maps]].


## In constructive mathematics

Various notions of continuous function are used in [[constructive mathematics]].  A function $f$ (say [[real number|real]]-valued and defined on a real [[interval]]) is:

* _pointwise-continuous_ if it continuous in the usual [[epsilon-delta]] (or equivalently [[open-subset]]) sense;
* _uniformly continuous_ if it [[uniformly continuous map|uniformly continuous]] in the usual epsilon-delta (or equivalently [[entourage]]-theoretic) sense;
* _Bishop-continuous_ if it is pointwise continuous and furthermore, the restriction to any closed and bounded interval is uniformly continuous;
* _Bridges-continuous_ if ... (this one\'s kind of complicated).

In [[classical mathematics]], these are all equivalent when the domain is itself a closed and bounded interval, and all of them except for uniform continuity are equivalent in general.  The same equivalences hold in [[intuitionistic mathematics]], thanks to the [[fan theorem]].  But no two of these are equivalent in [[Russian constructivism]].

In fact, assuming that $\mathbb{R}$ is defined as the set of located [[Dedekind cuts]], there is the following negative result by [[Frank Waaldijk]] ([Waaldijk2003](#Waaldijk2003)): Without the [[fan theorem]], there is no notion of continuity for set-theoretic functions in [[constructive mathematics]], spelled "kontinuity" in the following, such that all of the following desiderata are met:

* A function $[0,1] \to \mathbb{R}$ is kontinuous if and only if it is [[uniformly continuous]] in the usual sense.
* The composition of kontinuous functions is kontinuous.
* The function $\mathbb{R}^+ \to \mathbb{R}, x \mapsto 1/x$ is kontinuous.

The key problem is that a uniformly continuous, [[positive number|positive]]-valued function defined on $[0,1]$ might fail to be bounded below by a positive number, since the interval $[0,1]$ might fail to be [[compact space|compact]], yet its reciprocal (if also uniformly continuous) must be bounded above.

Waaldijk's negative result can be circumvented by dropping the insistence on points and instead working with maps between [[locales]], [[toposes]], or formal spaces as studied in [[formal topology]].


## Related concepts

* [[degree of a continuous function]]

* [[equicontinuous family of functions]]

* [[analytic function]]

* [[differentiable function]]

* [[smooth function]]

* [[convex function]]

* [[integrable function]], [[square-integrable function]]

* [[bounded function]]

* [[compactly supported function]]

* [[measurable function]]

* [[rapidly decreasing function]]

* [[function with rapidly decreasing partial derivatives]]

## References

* {#Waaldijk2003} [[Frank Waaldijk]], _On the foundations of constructive mathematics &#8211; especially in relation to the theory of continuous functions_, 2003 ([pdf](http://www.fwaaldijk.nl/foundations%20of%20constructive%20mathematics.pdf))



[[!redirects continuous map]]
[[!redirects continuous maps]]
[[!redirects continuous function]]
[[!redirects continuous functions]]

[[!redirects continuity]]
