> **Under Construction**

#Contents#
* automatic table of contents goes here
{:toc}



## Definition

### Lorentzian manifold

A _Lorentzian manifold_ $(X, \eta)$ of dimension $(d+1)$ is a smooth [[manifold]] equipped with a [[pseudo-Riemannian metric]] $\eta$ of signature $[+--\cdots -]$. This equips the [[tangent bundle|tangent space]] $T_x X$ at every point $x \in X$ canonically with the structure of a $(d+1)$-dimensional [[Minkowski space]].  Accordingly, tangent vectors of $X$ are called _timelike_ , _lightlike_ or _spacelike_ , if their norm is positive, zero or negative, respectively. 


### Causal structure

A **time orientation** on a Lorentian manifold $X$ is a smooth [[vector field]] $\nu \in \Gamma(T X)$ such that at all points $x \in X$ the vector $\nu_x$ is non-vanishing and timelike.

Given a time orientation $\nu$, a vector $v \in T_x X$ is **future directed** if it is timelike or light-like and its inner product with the time orientation vector at that point is positive, $\mu_x(\nu,v_x) \gt 0$.

Since $\nu$ itself is smooth and non-vanishing, it follows that it is fututre directed with respect to itself at every point.


A smooth curve in $X$, i.e. a smooth map $\gamma : [0,1] \to X$ is called a **timelike curve** or a **lightlike curve** or a **spacelike_curve** or a **future-directed_ curve** precisely if all of its tangent vectors $(\gamma_* \partial_s) \in T_{\gamma(s)} X$ are. 

We say that a point $y \in X$ **lies in the future** of a point $x \in X$ if $y = x$ or if there exists a future-directed curve $\gamma : [0,1] \to X$ with $\gamma(0) = x$ and $\gamma(1) = y$. 

We say that $(X,\mu)$ has **closed timelike curves** (closed future-directed curves) if there exists a non-constant timelike (future-dierected) curve starting and ending at some point $x$.

For applications to physics, where $X$ models [[spacetime]], the existence of closed future-directed curves is usually regarded as unphysical (not corresponding to a model of real physics). 

Notice that precisely if there are _no_ closed future-directed curves is the [[relation]]

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


## Discussion

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



## References

* From nCafe: <a href="http://golem.ph.utexas.edu/category/2008/10/the_nature_of_time.html#c019330">The Nature of Time</a>

* From nCafe: <a href="http://golem.ph.utexas.edu/category/2007/03/canonical_measures_on_configur_1.html">Canonical Measures on Configuration Spaces</a>

* Martin and Panangaden, <a href="http://www.springerlink.com/content/m3x4h1l6g64mu753/">	
Domain Theory and the Causal Structure of Space-Time</a>

[[!redirects Lorentzian manifold]]