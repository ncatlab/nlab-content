> **Under Construction**

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}



## Definition

### Lorentzian manifold

A _Lorentzian manifold_ $(X, \eta)$ of dimension $(d+1)$ is a [[smooth manifold]] equipped with a [[pseudo-Riemannian metric]] $\eta$ of signature $[+--\cdots -]$ (but note that the complementary choice $[-++\cdots +]$ is also used in the literature). This equips the [[tangent bundle|tangent space]] $T_x X$ at every point $x \in X$ canonically with the structure of a $(d+1)$-dimensional [[Minkowski space]].  Accordingly, tangent vectors $v \in T_x X$ of $X$ are called _[[timelike]]_ , _[[lightlike]]_ or _[[spacelike]]_ , if their norm-square $\mu_x(v,v)$ is positive, zero or negative, respectively.  See also at _[[causal structure]]_.


### Causal structure

A **time orientation** on a Lorentzian manifold $X$ is a smooth (or, depending on the author, continuous) [[vector field]] $\nu \in \Gamma(T X)$ such that at all points $x \in X$ the vector $\nu_x$ is timelike. In general, a Lorentzian manifold does not have globally defined timelike continuous vector fields. Sometimes only Lorentzian manifolds admitting a time orientation are also called [[spacetime]]s.

Given a time orientation $\nu$, a vector $v \in T_x X$ is **future directed** if it is timelike or light-like and its inner product with the time orientation vector at that point is positive, $\mu_x(\nu,v_x) \gt 0$.

Since $\nu$ itself is smooth, it follows that it is future directed with respect to itself at every point.


A smooth curve in $X$, i.e. a smooth map $\gamma : [0,1] \to X$ is called a **timelike curve** or a **lightlike curve** or a **spacelike curve** or a **future-directed curve** precisely if all of its tangent vectors $(\gamma_* \partial_s) \in T_{\gamma(s)} X$ are. 

We say that a point $y \in X$ **lies in the future** of a point $x \in X$ if $y = x$ or if there exists a future-directed curve $\gamma : [0,1] \to X$ with $\gamma(0) = x$ and $\gamma(1) = y$. Equivalently, in this case $x$ **lies in the past** of $y$.

#### Notions of causality

We say that $(X,\mu)$ has **closed timelike curves** (closed future-directed curves) if there exists a non-constant timelike (future-dierected) curve starting and ending at some point $x$. Spacetimes which do not contain closed timelike curves are called **chronological**, spacetimes which do not contain closed future directed (i.e. non-spacelike) curves are called **causal**. 


+-- {: .un_def}
###### Definition
Given a time orientated spacetime L, the **chronological future** $I^+(p)$ of a point $p \in L$ is the set of events that can be reached by a future directed timelike curve starting from p:
$$
I^+(p) := \{ q \in L | \text{there exists a future directed timelike curve} \lambda(t) \text{with} \lambda(0) = p and \lambda(1)=q \}
$$ 

The **causal future** $J^+(p)$ of $p$ is defined in the same way with future directed timelike replaced by future directed causal aka non-spacelike.
=--

+-- {: .un_def}
###### Definition
A subset S of a time orientated spacetime L is said to be **achronal** if no two points in S can be connected by a future directed timelike curve, i.e. for all $p, q \in L$ we have $q \notin I^+(p)$.
=--


+-- {: .un_theorem}
###### Theorem
**boundary of chronological future**
Let L be a time orientated spacetime and $S \subset L$. Then the boundary of $I^+(S)$ is either empty or an achronal, three-dimensional, embedded, $C^0$-submanifold of L.
=--
This is theorem 8.1.3 in the book of Wald.

Examples of non-chronological Lorentzian manifolds are the [[anti de Sitter space]] and the [[Kerr spacetime]]. 

While the former is more of a theoretical interest due to the maximality of the symmetry group, the latter is usually seen as a solution with relevance to actual _physics_, despite the fact that causality does not hold everywhere.

Note that the property of being chronological is not strong enough to enforce causality as understood in everyday life: Even if there are no _closed_ future-directed curves, there still may be e.g. nonclosed _ergodic_ future-directed curves (they come close to every point they already passed in the "past"). An often used stronger condition that models the everyday notion of causality is that the manifold has to be [[globally hyperbolic manifold|globally hyperbolic]] ([Wikipedia](http://en.wikipedia.org/wiki/Globally_hyperbolic)), which, as already mentioned, excludes certain solutions modelling e.g. black holes. 

#### Being causal means being a poset

Precisely if the Lorentzian space is causal in that there are _no_ closed future-directed curves is the [[relation]]

* $(x \leq y) \Leftrightarrow$ "$y$ is in the future of $x$" 

a [[poset]], hence a [[category]] with at most a single morphism between any two objects:

The [[object]]s of this category are the points of $X$. A [[morphism]] $x \to y$ is a pair of points $x \leq y$ with $y$ in the future of $x$. Composition of morphisms is transitivity of the relation. The identity morphism on $x$ is the reflexivity $x \leq x$.

The _anti-symmetry_ $(x \leq y \leq x) \Rightarrow (x = y)$ is precisely the absence of closed future-directed curves in $X$.

Conversely, from just knowing $X$ as a smooth manifold and knowing this [[poset]] structure on $X$, one can reconstruct the **light cone structure** of $(X,\mu)$, i.e. the information about which tangent vectors are timelike, lightlike, etc. 

One can see 

> (...reference...)

that the pseudo-Riemannian metric $\mu$ may be reconstructed from the lightcone structure and the [[volume density]] that it induces. In this sense a Lorentzian manifold without future-directed curves is equivalently a smooth [[poset]] equipped with a smooth [[measure]] on its space of objects.



### Generalized smooth Lorentzian spaces

...

> A **smooth Lorentzian space** is supposed to be like a Lorentzian manifold, but whose underlying space is not necessarily a smooth manifold, but a  [[generalized smooth space]].  

> So this is "something like" a [[partial order|poset]] [[internal category|internal]] to a category of measure spaces, or a [[poset]]-valued 2-[[stack]] on something like [[CartSp]] or the like.

...

## Construction on a smooth Lorentzian space

### Causal subsets

Let $(X,\mu,\nu)$ be a time-oriented Lorentzian space regarded as a smooth [[category]] that is a [[poset]].

A **causal subset** of a $X$ is one of its  [[under-over category|under-over categories]] $x \downarrow X \downarrow y$ for a pair $x,y \in X$ of points in $X$.

Its objects form the collection of all points $z \in X$ that are both in the future of $x$ as well as in the past of $y$.

### The path $(\infty,1)$-category of a Lorentzian space {#PathnCategory}

To every [[Lie ∞-groupoid]] $X$ is associated its [[schreiber:path ∞-groupoid]] $\mathbf{\Pi}(X)$. But more generally, to a smooth [[(∞,1)-category]] is associated a **path $(\infty,1)$-category**. See [[fundamental (infinity,1)-category]].

A causal Lorentzian manifold may naturally be regarded as a smooth category (a smooth [[poset]]) and as such has a path [[(n,r)-category|(2,1)]]-category. 
Its invertible [[morphism]]s are smooth spacelike curves, and its non-invertible morphisms contain future-directed paths. This $(2,1)$-category plays the role of the [[path groupoid]] of a plain manifold and is akin to the path 2-groupoid of paths in an [[orbifold]], only that where the latter has all morphisms invertible, crucially in the path 2-groupoid of a Lorentzian space, there are non-invertible morphisms, reflecting the causal structure of that space.

To put this construction into context, we therefore first recall the story for paths in an orbifold.

#### Prelude: the path 2-groupoid of an orbifold

To an ordinary [[smooth manifold]] or [[generalized smooth space]] $X$ is associated its [[fundamental groupoid]] $\Pi_1(X)$ and its smooth [[path groupoid]] $P_1(X)$: [[categories]] whose [[object]]s are the points of $X$ and whose [[morphism]]s are certain equivalence classes of smooth paths between these objects.

This construction generalizes from paths in plain spaces, to paths in spaces that are themselves smooth groupoids: notably to [[orbifold]]s $X$. 

Given an orbifold $X$ with space of objects $X_0$ and space of morphisms $X_1$, paths in it form a smooth [[2-groupoid]] $P_1(X)$ which looks as follows:

* objects of $P_1(X)$ are the points of $X_0$;

* the morphisms of $P_1(X)$ are formal composites of two types of morphisms

  1. the smooth paths $X_0$, i.e. the morphisms of $P_1(X_0)$;

     $\gamma : x \to y$

  1. the original morphisms of $X$, i.e. the elements of $X_1$. Since the orbifold is locally given by a [[group]] $G$, we may think of these morphisms as being of the form $x \to g\cdot x$, connecting a point $x \in X_0$ to the point $g\cdot x$ that it is [[isomorphism|isomorphic]] to under the orbifold action.

* the [[2-morphism]]s of $P_1(X)$ are paths in $X_1$, i.e. morphisms of $P_1(X_1)$. These we may picture as

  $$
    \array{
      x &\stackrel{\gamma}{\to}& y
      \\
      \downarrow &\swArrow& \downarrow
      \\
      g\cdot x &\underset{g\cdot \gamma}{\to}& g \cdot y
    }
    \,.
  $$

  This is a path $(\gamma, g\cdot \gamma)$ of pairs of points that are related under the orbifold action.

The path 2-groups $P_1(X)$ of the orbifold encodes the correct notion of trajectories in the orbifold: such a trajectory may proceed along smooth paths, and intermittently it may jump between the "orbifold sectors". Notably an [[automorphism]] in $P_1(X)$ on a point $x$ may be given by a smooth path $x \to g x$ that does not come back to $x$ but just to one of its mirror-images, composed with the jump-morphism $g x \to x$ back to $x$. Sometimes (notably in [[string theory]]) such loops are called _twisted sectors_ of loop configurations.

A detailed description of the smooth [[2-groupoid]] of paths in a smooth 2-groupoid may be found in [section 2.1](http://arxiv.org/PS_cache/arxiv/pdf/0808/0808.1923v1.pdf#page=19) of

* U.S., [[Konrad Waldorf]], _Connections on nonabelian gerbes and their holonomy_ ([arXiv:0808.1923](http://arxiv.org/abs/0808.1923))

There the groupoid $X$ is taken to be a [[Cech nerve|Cech groupoid]], but the general mechanism of the construction does not depend on this. A fully general description of paths in (higher) smooth groupoids is also at [[schreiber:path ∞-groupoid]].

It is immediate how this construction generalizes when the smooth groupoid $X$ is replaced by a smooth category. This we turn to now.

#### The path $(2,1)$-category of a Lorentzian space

Now we discuss the same as above, where now $X = (X_1 \stackrel{\to}{\to} X_0)$ is not a smooth groupoid, but a smooth category, notably the smooth [[poset]] determined by a smooth Lorentzian space.

So let $X$ be a smooth causal Lorentzian manifold, regarded as a [[poset]]. So $X_0$ is the underlying manifold and $X_1 \subset X_0 \times X_0$ is the collection of pairs of points with one in the future of the other.

We equip this with the structure of a [[internal category|category internal]] to [[diffeological space]]s, hence with the structure of a category-valued [[presheaf]] on the [[site]] [[CartSp]], by declaring that a plot $\phi : U \to X_0$  of the space of objects is a _spacelike_ smooth map $U \to X_0$: the push-forward along $\phi$ of every tangent vector of $U \in CartSp$ yields a spacelike vector in $X_0$.

Analogously, we declare a plot $\phi  : U \to X_1$ to be a pair of plots into $X_0$ such that pointwise this assigns a point and one point in its future.

From now on, by abuse of notation, by $X$ we shall mean this category internal to diffeological spaces, regarded as a category-valued presheaf on [[CartSp]].

Then the path $(2,1)$-category $P_1(X)$ is defined as follows:

* its space of objects is again the diffeological space $X_0$;

* the elements of its space of morphisms are generated from

  * morphisms $\gamma : x \to y$ 
    given by reparameterization or thin-hoimotopy 
    classes of smooth spacelike curves $\gamma : [0,1] \to X_0$;     
 
  * morphisms of the form $x \to y$ for every $x \leq y$ in the causal structure of $X$.

  There is an evident diffeology on this space (a quotient of a disjoint union of product diffeologies). This defines the diffeological space $(P_1(X))$.

* the elements of its space of 2-morphisms are generated from 2-morphisms

  $$
    \array{
      & \nearrow \searrow^{\mathrlap{[\gamma_1]}}
      \\
      x_1  && y_1
      \\
      \downarrow &\swArrow& \downarrow
      \\
      x_2  && y_2
      \\
      & \searrow \nearrow_{\mathrlap{[\gamma_2]}}  
    }
    \;\;\;\;
    \forall t \in [0,1] : \gamma_1(t) \leq \gamma_2(t)
  $$

  given from classes of smooth paths in $X_1$, i.e. from classes of paths of pairs of points, one in the future of the other.

  There is an evident diffeology and evident composition operations on this. Notice that the generating 2-cells are 2-isomorphisms, but that their source and target morphisms are not generally invertible. 

## Related concepts

* [[pseudo-Riemannian manifold]]

  * [[Lorentzian manifold]]

    * [[Lorentzian geometry]]

    * [[spacetime]]

  * [[globally hyperbolic Lorentzian manifold]]

* [[conal manifold]]

* [[Lorentzian orbifold]]

## References

Named after [[Hendrik Lorentz]].

A classic reference for general relativity is

* [[Robert Wald]], _General Relativity_

A textbook dedicated to the classical [[differential geometry|diffential geometric]] aspects Lorentzian manifolds is

* John K. Beem; Paul E. Ehrlich, ; Kevin L. Easley, _Global Lorentzian geometry_ ([ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0846.53001&format=complete))

A classical influential text on the nature of Lorentzian space is

* [[Roger Penrose]], [[Wolfgang Rindler]], _Spinors and space time_, in 2 vols. Cambridge Univ. Press 1984/1988.  

On Lorentz structure as [[G-structure]]:

* Leandro A. Lichtenfelz, [[Paolo Piccione]], Abdelghani Zeghib, _On the Isometry Group of Lorentz Manifolds_, in: Miguel Sanchez, Miguel Ortega, Alfonso Romero (eds.) _Recent Trends in Lorentzian
Geometry_, Springer 2013 ([doi:10.1007/978-1-4614-4897-6_12](https://doi.org/10.1007/978-1-4614-4897-6_12))

The relation between causality and [[poset]]-structure (see also [[causal set]]) is reviewed for instance in 

* Ettore Minguzzi, _Time and Causality in General Relativity_ , talk notes, Ponta Delgada, July 2009 ([pdf](http://fqxi.org/data/documents/Minguzzi%20%20Azores%20Talk.pdf))

More details are discussed in the context of [[domain theory]], see for instance 

* [[Keye Martin]] and [[Prakash Panangaden]], <a href="http://www.springerlink.com/content/m3x4h1l6g64mu753/">	
Domain Theory and the Causal Structure of Space-Time</a>


Some vaguely related blog discussion is at

* <a href="http://golem.ph.utexas.edu/category/2008/10/the_nature_of_time.html#c019330">The Nature of Time</a>

* <a href="http://golem.ph.utexas.edu/category/2007/03/canonical_measures_on_configur_1.html">Canonical Measures on Configuration Spaces</a>




[[!redirects smooth Lorentzian space]]
[[!redirects smooth Lorentzian spaces]]

[[!redirects Lorentzian manifold]]
[[!redirects Lorentzian manifolds]]
[[!redirects smooth Lorentzian manifold]]
[[!redirects smooth Lorentzian manifolds]]

[[!redirects Lorentzian space]]
[[!redirects Lorentzian spaces]]

[[!redirects Lorentzian spacetime]]
[[!redirects Lorentzian spacetimes]]


[[!redirects Lorentzian structure]]
[[!redirects Lorentzian structures]]
