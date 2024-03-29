[[!redirects pseudo-metric space]]
[[!redirects pseudo-metric]]
[[!redirects pseudo-metric spaces]]
[[!redirects pseudo-metrics]]
[[!redirects proxi-metric]]
[[!redirects proxi-metric spaces]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The category of [[metric spaces]] with Lipschitz maps between them is not good enough from a categorical viewpoint: it has finite limits (the max metric on the product) but not all finite colimits: the coproduct doesn't always exist. To overcome this difficulty, one needs to enlarge this category in various ways.

The first enlargement is obtained by replacing the usual triangular inequality
$d(x,y)\leq d(x,z)+d(z,y)$ by the proxi-metric inequality: there exists $C\geq 1$ such that
$$d(x,y)\leq C\cdot \max(d(x,z),d(z,y)).$$
If $C=1$, we get back the ultrametric inequality, and the usual triangular inequality corresponds to the case $C=2$.

This gives a category of so-called proxi-metric spaces stable by the $\mathbb{R}_+^*$-flow given by
$$d\mapsto d^t:=e^{t\log(d)}.$$

To get enough finite colimits, one needs to restrict to bounded proximetric spaces, and then, one may take an ind-pro or an ind-completion to get a good category of generalized metric spaces, i.e., a convenient setting for the development of a metric stable homotopy theory, based on the use of the interval $[0,1]$
or a normed version of it.

The aim of this normed/metrized stable homotopy theory is to develop topological cohomological invariants for [[proxi-normed rings]].

## Related subjects

[[global analytic geometry]]

[[spectral global analytic geometry]]