+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analysis
+--{: .hide}
[[!include analysis - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _weighted category_ or _normed category_ can be viewed as:

* A [[category]] where each [[morphism]] has a [[number]] (for example a "cost" or "length"), and [[composition]] comes with a [[triangle inequality]]; 
* A structure which is to a [[category]] as a [[metric space#LawvereMetricSpace|Lawvere metric space]] is to a [[preorder]];
* Like a [[weighted graph]] or [[multigraph]], but equipped with [[identity]] and [[composition]] (and a [[triangle inequality]]);
* Like a [[metric space]] or [[metric space#LawvereMetricSpace|Lawvere metric space]], but with many arrows or "paths with length" between any two objects;
* A category enriched in the [[free coproduct completion]] of the monoidal category of real numbers used to define [[metric space#LawvereMetricSpace|Lawvere metric spaces]] (compare [[locally graded category]]).

Depending on the author, the precise definitions vary slightly, see below as well as the [references](#references).

## Definition

A **weighted category** or **normed category** is a [[category]], where to each [[morphism]] $f:A\to B$ we assign a non-negative [[real number]] (or possibly infinite) $w(f)$ called the **weight** or **norm**, such that

* For all [[identity morphisms]], $w(id_X)=0$;
* for all [[composition|composite morphisms]], the following [[triangle inequality]] holds:
$$
w(g\circ f) \;\le\; w(g) + w(f) . 
$$

The assignment $f\mapsto w(f)$ is sometimes called a **weighting**.

### Variations on the definition

Sometimes one wants the triangle inequality to be multiplicative rather than additive, and the identity to have weight one. (One can imagine for example exchange rates between different currencies.)
Alternatively, one can take the logarithm of the weights (but then one needs to allow negative weights).

Similarly, sometimes one wants to replace the sum by a maximum or minimum.

There are additional axioms one can assume on the norm, see the references for more.

## Examples

* If $(X,d)$ is a [[metric space]] (or [[metric space#LawvereMetricSpace|Lawvere metric space]]), there is a weighted category whose objects are the [[points]] of $X$, and whose morphisms are [[curves]] in $X$, weighted by their [[length]].

* The category of [[metric spaces]] and [[Lipschitz functions]] is multiplicatively weighted by the Lipschitz constants (or one can take the logarithm, see above). If one allows infinite weights, one can extend this to all functions (or all continuous functions, etc). 

* The example above restricts to [[Banach spaces]] and [[bounded]] (or also unbounded) linear maps. 

* Every [[metric space#LawvereMetricSpace|Lawvere metric space]] is a weighted category with a single morphism (whose weight is the distance) between any two objects.

* Every ordinary [[category]] can be seen as a weighted category where each morphism has weight zero.

(...)

## As an enriched category

Similarly to [[metric space#LawvereMetricSpace|Lawvere metric spaces]], weighted categories can be considered [[enriched categories]], where the enriching category is a "many-point version" of the interval $[0,\infty]$, the [[free coproduct completion]] of this interval considered as a monoidal category:

* Define a **weighted set** to be a set $X$ equipped with a function $w:X\to [0,\infty]$;
* Call a function $f:(X,w_X)\to (Y,w_Y)$ **short** (in analogy with [[short maps]]) if and only if for all $x\in X$,
$$
w_Y\big( f(x) \big) \;\le\; w_X(x) .
$$
* Define the [[tensor product]] of weighted sets to be the [[cartesian product]] of the sets, with the sum of the weights: given $(X,w_X)$ and $(Y,w_Y)$, and for all $(x,y)\in X\otimes Y$,
$$
w_{X\otimes Y} \big((x,y)\big) \;=\; w_X(x) + w_Y(y) .
$$

Weighted sets and short functions, this way, form a [[closed monoidal category]], which we denote $WSet$.
Weighted categories are precisely $WSet$-enriched categories in this sense.


## Constructions

### From weighted categories to metrics

Given a weighted category $C$, we can canonically construct a [[metric space#LawvereMetricSpace|Lawvere metric]] between the objects of $C$ as follows:
$$
d(X,Y) \;\coloneqq\; \inf_{f:X\to Y} w(f) .
$$

This is analogous to how often, in geometry as well as in ordinary life, [[length#length_and_geodesic_spaces|the distance is the length of the shortest path]].

### Weighted limits and colimits

(Note that "weighted" in this context may refer to the weighting of the category, or to the usual [[weighted limits]].)

(...)

## See also

* [[metric space]], [[metric space#LawvereMetricSpace|Lawvere metric space]]
* [[weighted graph]]
* [[locally graded category]]
* [[enriched category theory]]


## References

* [[William Lawvere]], _Metric spaces, generalized logic and closed categories_, Rendiconti del seminario matematico e fisico di Milano 43, 1973.

* [[Renato Betti]] and Massimo Galuzzi, _Categorie normate_, Bollettino dell'Unione Matematia Italiana 11.1, 1975.

* [[Marco Grandis]], _Categories, norms and weights_, Journal of Homotopy and Related Structures 2(2), 2007.

* Wiesław Kubiś, _Categories with norms_, 2017. ([arXiv](https://arxiv.org/abs/1705.10189))

* Peter Bubenik, Vin de Silva and Jonathan Scott, _Interleaving and Gromov-Hausdorff distance_, 2017. ([arXiv](https://arxiv.org/abs/1707.06288))

* Daniel Luckhardt and Matt Insall, _Norms on Categories and Analogs of the Schroeder-Bernstein Theorem_, 2021. ([arXiv](http://arxiv.org/abs/2105.06832))

* [[Paolo Perrone]], _Lifting couplings in Wasserstein spaces_, 2021. ([arXiv](https://arxiv.org/abs/2110.06591))

* Maria Manuel Clementino, Dirk Hofmann, and Walter Tholen, _Cauchy convergence in V-normed categories_, [arXiv:2404.09032](https://arxiv.org/abs/2404.09032) (2024).


[[!redirects weighted categories]]
[[!redirects normed category]]
[[!redirects normed categories]]