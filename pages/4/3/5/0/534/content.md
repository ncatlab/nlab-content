> **Under Construction**

#Contents#
* automatic table of contents goes here
{:toc}



## Definition

### Lorentzian manifold

A _Lorentzian manifold_ $(X, \eta)$ of dimension $(d+1)$ is a smooth [[manifold]] equipped with a [[pseudo-Riemannian metric]] $\eta$ of signature $[+--\cdots -]$ (but note that the complementary choice $[-++\cdots +]$ is also used in the literature). This equips the [[tangent bundle|tangent space]] $T_x X$ at every point $x \in X$ canonically with the structure of a $(d+1)$-dimensional [[Minkowski space]].  Accordingly, tangent vectors $v \in T_x X$ of $X$ are called _timelike_ , _lightlike_ or _spacelike_ , if their norm-square $\mu_x(v,v)$ is positive, zero or negative, respectively. 


### Causal structure

A **time orientation** on a Lorentzian manifold $X$ is a smooth (or, depending on the author, continuous) [[vector field]] $\nu \in \Gamma(T X)$ such that at all points $x \in X$ the vector $\nu_x$ is timelike. In general, a Lorentzian manifold does not have globally defined timelike continuous vector fields. Sometimes only Lorentzian manifolds admitting a time orientation are also called [[spacetime]]s.

Given a time orientation $\nu$, a vector $v \in T_x X$ is **future directed** if it is timelike or light-like and its inner product with the time orientation vector at that point is positive, $\mu_x(\nu,v_x) \gt 0$.

Since $\nu$ itself is smooth, it follows that it is future directed with respect to itself at every point.


A smooth curve in $X$, i.e. a smooth map $\gamma : [0,1] \to X$ is called a **timelike curve** or a **lightlike curve** or a **spacelike curve** or a **future-directed curve** precisely if all of its tangent vectors $(\gamma_* \partial_s) \in T_{\gamma(s)} X$ are. 

We say that a point $y \in X$ **lies in the future** of a point $x \in X$ if $y = x$ or if there exists a future-directed curve $\gamma : [0,1] \to X$ with $\gamma(0) = x$ and $\gamma(1) = y$. Equivalently, in this case $x$ **lies in the past** of $y$.

#### Notions of causality

We say that $(X,\mu)$ has **closed timelike curves** (closed future-directed curves) if there exists a non-constant timelike (future-dierected) curve starting and ending at some point $x$. Spacetimes which do not contain closed timelike curves are called **chronological**, spacetimes which do not contain closed future directed (i.e. non-spacelike) curves are called **causal**. 

Examples of non-chronological Lorentzian manifolds are the [[anti de Sitter space]] and the [[Kerr spacetime]]. 

While the former is more of a theoretical interest due to the maximality of the symmetry group, the latter is usually seen as a solution with relevance to actual _physics_, despite the fact that causality does not hold everywhere.

Note that the property of being chronological is not strong enough to enforce causality as understood in everyday life: Even if there are no _closed_ future-directed curves, there still may be e.g. nonclosed _ergodic_ future-directed curves (they come close to every point they already passed in the "past"). An often used stronger condition that models the everyday notion of causality is that the manifold has to be [[globally hyperbolic]] ([globally hyperbolic] (http://en.wikipedia.org/wiki/Globally_hyperbolic)), which, as already mentioned, excludes certain solutions modelling e.g. black holes. 

#### Being causal means being a poset

Precisely if the Lorentzian space is causal in that there are _no_ closed future-directed curves is the [[relation]]

* $(x \leq y) \Leftrightarrow$ "$y$ is in the future of $x$" 

a [[poset]], hence a [[category]] with at most a single morphism between any two objects:

The [[object]]s of this category are the points of $X$. A [[morphism]] $x \to y$ is a pair of points $x \leq y$ with $y$ in the future of $x$. Composition of morphisms is transitivity of the relation. The identity morphism on $x$ is the reflexivity $x \leq x$.

The _anti-symmetry_ $(x \leq y \leq x) \Rightarrow (x = y)$ is precisely the absence of closed future-directed curves in $X$.

Conversely, from just knowing $X$ as a smooth manifold and knowing this [[poset]] structure on $X$, one can reeconstruct the **light cone structure** of $(X,\mu)$, i.e. the information about which tangent vectors are timelike, lightlike, etc. 

One can see 

> (...reference...)

that the pseudo-Riemannian metric $\mu$ may be reconstructed from the lightcone structure and the [[volume density]] that it induces. In this sense a Lorentzian manifold without future-directed curves is equivalently a smooth [[poset]] equipped with a smooth [[measure]] on its space of objects.



### Generalized smooth Lorentzian spaces

...

> A **smooth Lorentzian space** is supposed to be like a Lorentzian manifold, but whose underlying space is not necesarily a smoth manifold, but a  [[generalized smooth space]].  

> So this is "something like" a [[partial order|poset]] [[internal category|internal]] to a category of measure spaces, or a [[poset]]-valued 2-[[stack]] on something like [[CartSp]] or the like.

...

## Construction in a smooth Lorentzian space

### Causal subsets

Let $(X,\mu,\nu)$ be a time-oriented Lorentzian space regarded as a smooth [[category]] that is a [[poset]].

A **causal subset** of a $X$ is one of its  [[under-over category|under-over categories]] $x \downarrow X \downarrow y$ for a pair $x,y \in X$ of points in $X$.

Its objects form the collection of all points $z \in X$ that are both in the future of $x$ as well as in the past of $y$.


## References

A textbook dedicated to the classical [[differential geometry|diffential geometric]] aspects Lorentzian manifolds is

* John K. Beem; Paul E. Ehrlich, ; Kevin L. Easley, _Global Lorentzian geometry_ ([ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0846.53001&format=complete))

The relation between causality and [[poset]]-structure is reviewed for instance in 

* Ettore Minguzzi, _Time and Causality in General Relativity_ , talk notes, Ponta Delgada, July 2009 ([pdf](http://fqxi.org/data/documents/Minguzzi%20%20Azores%20Talk.pdf))

There is also

* [[Keye Martin]] and [[Prakash Panangaden]], <a href="http://www.springerlink.com/content/m3x4h1l6g64mu753/">	
Domain Theory and the Causal Structure of Space-Time</a>

* Roger Penrose, Wolfgang Rindler, _Spinors and space time_, in 2 vols. Cambridge Univ. Press 1984/1988.  

Some vaguely related blog discussion is at

* <a href="http://golem.ph.utexas.edu/category/2008/10/the_nature_of_time.html#c019330">The Nature of Time</a>

* <a href="http://golem.ph.utexas.edu/category/2007/03/canonical_measures_on_configur_1.html">Canonical Measures on Configuration Spaces</a>


## Discussion

A previous version of this entry started the following discussion.

+-- {: .query}

_[[Toby Bartels|Toby]] asked_: How does this relate to a (smooth) Lorentzian manifold? if at all.

_[[Eric Forgy|Eric]] says_: Good question. I took the statement from a comment Urs made [[Discrete Causal Spaces|here]]. I chose to use the word "space" instead of "manifold" simply because it seemed to fit into a theme here about [[generalized smooth space|generalized smooth "spaces"]]. The definition definitely needs fleshing out, but its a start.

_[[Urs Schreiber|Urs]]_: 

The point is: there is a theorem 

* see [Wikipedia: causal sets](http://en.wikipedia.org/wiki/Causal_sets#cite_note-Malament-0)

that says that a map between two Lorentzian manifolds which preserves the causal structure, i.e. which is a functor of the underlying posets, is automatically a conformal isometry. There is, I think, another related theorem which says that from just the lightcone structure of a Lorentzian manifold, one can reconstruct its Lorentzian metric up to a conformal rescaling.

Both theorems suggest that a Lorentzian metric on a manifold is in a way equivalent to a pair consisting of a measure on the manifold and lightcone structure. The latter in turn can be encoded in a poset structure on the manifold. If true, it would seem to suggest that a good foundational model for relativistic physics _might_ be posets [[internal category|internal to]] [[Meas]].

Somebody should sort this out.

_[[Eric Forgy|Eric]] says_: I like this idea. The measure could be the Leinster measure, which would be neat. We discussed this before at the nCafe I think.

_[[Urs Schreiber|Urs]]_: Yes, exactly. There was the idea that, since many finite categories come with a _canonical_ measure on their space (set) of objects, maybe we somehow need to merge this idea of Leinster measure with the idea of modelling a Lorentzain spacetime by something like a poset. Playing around with this observation was the content of [this](http://golem.ph.utexas.edu/category/2007/03/canonical_measures_on_configur_1.html) blog entry.  But I am not sure if it works out...

=--




[[!redirects Lorentzian manifold]]
[[!redirects smooth Lorentzian manifold]]

[[!redirects smooth Lorentzian spaces]]
[[!redirects Lorentzian manifolds]]
[[!redirects smooth Lorentzian manifolds]]
