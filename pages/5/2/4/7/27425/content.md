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
* Like a [[metric space]] or [[metric space#LawvereMetricSpace|Lawvere metric space]], but with many arrows or "paths with length" between any two objects.

Depending on the author, the precise definitions vary slightly, see below as well as the [references](#references).

## Definition

A **weighted category** or **normed category** is a [[category]], where to each [[morphism]] $f:A\to B$ we assign a non-negative [[real number]] $w(f)$ called the **weight** or **norm**, such that

* For all [[identity morphisms]], $w(id_X)=0$;
* for all [[composition|composite morphisms]], the following [[triangle inequality]] holds:
$$
w(g\circ f) \;\le\; w(g) + w(f) . 
$$

### Variations on the definition

(...)

## Examples

(...)

## As an enriched category

(...)

## Constructions

(...)


## See also

* [[metric space]], [[metric space#LawvereMetricSpace|Lawvere metric space]]
* [[weighted graph]]
* [[enriched category theory]]


## References

* [[William Lawvere]], _Metric spaces, generalized logic and closed categories_, Rendiconti del seminario matematico e fisico di Milano 43, 1973.

* [[Renato Betti]] and Massimo Galuzzi, _Categorie normate_, Bollettino dell'Unione Matematia Italiana 11.1, 1975.

* [[Marco Grandis]], _Categories, norms and weights_, Journal of Homotopy and Related Structures 2(2), 2007.

* Wiesław Kubiś, _Categories with norms_, 2017. ([arXiv](https://arxiv.org/abs/1705.10189))

* Peter Bubenik, Vin de Silva and Jonathan Scott, _Interleaving and Gromov-Hausdorff distance_, 2017. ([arXiv](https://arxiv.org/abs/1707.06288))

* Daniel Luckhardt and Matt Insall, _Norms on Categories and Analogs of the Schroeder-Bernstein Theorem_, 2021. ([arXiv](http://arxiv.org/abs/2105.06832))

* [[Paolo Perrone]], _Lifting couplings in Wasserstein spaces_, 2021. ([arXiv](https://arxiv.org/abs/2110.06591))


[[!redirects weighted categories]]
[[!redirects normed category]]
[[!redirects normed categories]]