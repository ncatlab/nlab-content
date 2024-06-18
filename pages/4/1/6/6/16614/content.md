
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

\begin{definition}
A _harmonic map_ is a [[smooth function]] $f \colon X \longrightarrow Y$ between a [[pair]] $(X,g_X)$, $(Y,g_Y)$ of  [[Riemannian manifolds]] which is a [[critical point]] of the Dirichlet [[kinetic energy]] [[functional]]

\[
  \label{EnergyFunctional}
  E(f) 
    \;\coloneqq\; 
  \tfrac{1}{2}
  \textstyle{\int_{X}} \Vert \mathrm{d} f\Vert^2 dVol_X
  \,,
\]

where 

* $\mathrm{d} f \in \Gamma \big(T^\ast X \otimes \phi^\ast T Y\big)$ is the ([[exterior derivative|exterior]]) [[derivative]],

* the [[norm]] $\Vert-\Vert$ is given jointly by the metrics of $X$ and $Y$,

* the [[volume form]] $dVol$ is that of $X$.

\end{definition}
(e.g. [Lin & Wang 2008, Def. 1.1.1](#LinWang08); [Jost 2017, Def. 9.1.2](#Jost17))

\begin{remark}
The analogous formula makes sense for [[pseudo-Riemannian manifolds]] where (eq:EnergyFunctional) is the  standard [[kinetic action]] [[action functional]] -- the _[[Polyakov action]]_ -- for [[relativistic field theory|relativistic]] non-linear [[sigma models]] (such as for the [[relativistic particle]], [[string]] or [[membrane]], etc.)
\end{remark}


## Related concepts

* [[second fundamental form]]

## References

* {#LinWang08} Fanghua Lin,  Changyou Wang: *The Analysis of Harmonic Maps and Their Heat Flows*, World Scientific (2008) &lbrack;[doi:10.1142/6679](https://doi.org/10.1142/6679)&rbrack;

* {#Jost17} [[Jürgen Jost]], Ch. 9 in: *Riemannian Geometry and Geometric Analysis*, Springer (2017) &lbrack;[doi:10.1007/978-3-319-61860-9](https://doi.org/10.1007/978-3-319-61860-9)&rbrack;

* Wikipedia, _[Harmonic map](https://en.wikipedia.org/wiki/Harmonic_map)_

Discussion in the context of [[action functionals]] for [[theory (physics)|theories of physics]] (nonlinear [[sigma models]]):

* [[Charles Misner]], _Harmonic maps as models for physical theories_, Phys. Rev. D **18** 4510 (1978) &lbrack[spire:137431](http://inspirehep.net/record/137431)&rbrack;

Discussion in the context of [[integrable systems]]:

* [[Shabnam Beheshti]], A. Shadi Tahvildar-Zadeh, _Integrability and Vesture for Harmonic Maps into Symmetric Spaces_ &lbrack;[arXiv:1209.1383](http://arxiv.org/abs/1209.1383)&rbrack;



[[!redirects harmonic maps]]

[[!redirects Dirichlet energy]]
[[!redirects Dirichlet energies]]