
# Short maps
* table of contents
{: toc}

## Idea

A _short map_ is a well-behaved sort of [[morphism]] of [[metric spaces]] (or a generalisation of metric spaces, such as the extended quasi-pseudo-versions, or [[gauge spaces]] or [[prometric spaces]]).  Short maps go by many names in the literature, often ad hoc, such as _distance-nonincreasing maps_ and _weak contractions_, but 'short map' seems to be increasing in popularity.


## Definition

A [[function]] $f\colon X \to Y$ is __short__ if $d(f(a),f(b)) \leq e(a,b)$ for every $a,b \in X$.  Here $d$ and $e$ are (respectively) the [[metrics]] (or generalisations of metrics) on $X$ and $Y$.  If $X$ and $Y$ are (or may be) [[gauge spaces]] and so have several (pseudo)metrics on them, then we require that, for every gauging distance $d$ on $X$, there exists a gauging distance $e$ on $Y$ such that the above inequality holds for all $a$ and $b$.


## The category of metric spaces

We define $Met$ to be the [[category]] whose [[objects]] are [[Lawvere metric spaces]] and whose [[morphisms]] are short maps.

$Met$ is [[complete category|complete]] and admits a [[faithful functor]] from [[Ban]] (the category of [[Banach spaces]] and short [[linear operators]]).

$Met$ may be made into an $\mathcal{M}$-[[M-category|category]] by taking short maps as the tight morphisms and some more generous notion of maps (such as [[continuous maps]]) as the loose morphisms. 

If instead we use ordinary metric spaces, which includes the axioms of finiteness $d(x, y) \lt \infty$, symmetry $d(x, y) = d(y, x)$, and separability ($d(x, y) = 0$ implies $x = y$), then the category $Met_{ord}$ (with short maps as morphisms) is not so [[dichotomy between nice objects and nice categories|nice]] as $Met$. For example, $Met_{ord}$ fails to have arbitrary products $\prod_{i \in I} X_i$, on account of the finiteness axiom where the putative distance 

$$d((x_i), (y_i)) = \sup_i d(x_i, y_i)$$ 

may not exist as a finite number. However, if all the ordinary metric spaces $X_i$ are uniformly bounded in diameter, then this formula does give the product. Note well though that the topology induced by this product will not be the same as the product topology (cf. the discussion below). 


## Justification

There are many other kinds of maps between metric spaces; [[continuous maps]] and [[uniformly continuous map]]s are more general, while [[isometries]] and contractions are more restrictive.  What\'s so special about short maps that we consider them the proper morphisms between metric spaces?

One answer is to look at [[Lawvere]]\'s characterisation of metric spaces as certain [[enriched categories]]; see [[Lawvere metric space]].  Then the short maps are precisely the [[enriched functors]] between metric spaces.

Another answer is to consider what the category-theoretic [[isomorphisms]] between metric spaces are; by the definition of metric spaces as [[structured sets]], these are the [[global isometries]].  So for a good notion of morphism, we need to recover global isometries as isomorphisms.  Using continuous or uniformly continuous maps, we recover [[homeomorphisms]] or uniform homeomorphisms as isomorphisms, which are too general; this really gives us the category of [[metrisable topological spaces]] or of [[metrisable]] [[uniform spaces]] rather than the category of metric spaces.  Using contractions, we do not even get a category; the [[identity function]] is not a contraction.  We could still use global isometries themselves as morphisms, but since this defines a [[groupoid]], we should look for a more general notion of morphism that still gives global isometries as isomorphism.  And short maps do that.

Short maps give the [[Met|category of metric spaces]] some nice properties.  In particular, $Met$ is [[complete category|complete]], which does not hold using either global isometries or distance-preserving maps as morphisms.  This interacts with the properties of the category of [[Banach spaces]]; as a Banach space may be defined as a set with compatible vector-space and metric-space structures, so a Banach space morphism is a function that is both linear and short: the [[short linear maps]].

## Injective objects in $Met_{ord}$

In $Met_{ord}$ every object $X$ admits an [[injective hull]] $\varepsilon(X)$. The space $\varepsilon(X)$ is [[compact topological space|compact]] if $X$ is [[compact topological space|compact]]. Furthermore every [[compact topological space|compact metric space]] has an __injective boundary__ that is the smallest subspace $A$ of $X$ such that $\varepsilon(A) = X$.

## Related pages

* [[Lipschitz map]]
* [[metric space]]

## References

Injective objects $Met_{ord}$ have been studied in

* Aronszajn, Nachman, and Prom Panitchpakdi. "Extension of uniformly continuous transformations and hyperconvex metric spaces." _Pacific Journal of Mathematics_ 6.3 (1956): 405-439.

* Isbell, John R. "Six theorems about injective metric spaces." _Commentarii Mathematici Helvetici_ 39.1 (1964): 65-76.

* [[Anton Petrunin]], "Lectures on metric geometry" 2020, [PDF](https://anton-petrunin.github.io/metric-geometry/tex/lectures.pdf).


An overview of results is included in

* Culbertson, Jared, Dan P. Guralnik, and Peter F. Stiller. "Injective metrizability and the duality theory of cubings." Expositiones Mathematicae 37.4 (2019): 410-453. [arXiv: 1502.00126](https://arxiv.org/abs/1502.00126).



[[!redirects short map]]
[[!redirects short maps]]
[[!redirects short function]]
[[!redirects short functions]]
[[!redirects distance-nonincreasing map]]
[[!redirects distance-nonincreasing maps]]
[[!redirects distance-nonincreasing function]]
[[!redirects distance-nonincreasing functions]]
[[!redirects weak contraction]]
[[!redirects weak contractions]]
[[!redirects contractive map]]
[[!redirects contractive maps]]

[[!redirects category of metric spaces]]
[[!redirects the category of metric spaces]]
[[!redirects Met]]
