
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
(due to [Eells & Sampson 1964, §1-§2](#EellsSampson64); review includes [Baird & Wood 2003, §3.3](#BairdWood03); [Lin & Wang 2008, Def. 1.1.1](#LinWang08); [Jost 2017, Def. 9.1.2](#Jost17))

\begin{remark}
The analogous formula makes sense for [[pseudo-Riemannian manifolds]] where (eq:EnergyFunctional) is the  standard [[kinetic action]] [[action functional]] -- the _[[Polyakov action]]_ -- for [[relativistic field theory|relativistic]] non-linear [[sigma models]] (such as for the [[relativistic particle]], [[string]] or [[membrane]], etc.)
\end{remark}

## Properties
 {#Properties}

In the terminology discussed at *[[Riemannian immersion]] -- [Properties](Riemannian+immersion#Properties)* we have:

\begin{theorem}\label{HarmonicEquation}
**(harmonic equation)**
\linebreak
A [[Riemannian immersion]] $\phi \colon \Sigma \to X$ is a harmonic map if and only if it has vanishing *[tension field](Riemannian+immersion#TensionField)*, hence iff its [second fundamental form](Riemannian+immersion#TensionField) has vanishing trace.
\end{theorem}
([Eells & Sampson 1964 pp. 116](#EellsSampson64), [Baird & Wood 2003 Thm. 3.3.3](#BairdWood03))



## Related concepts

* [[harmonic function]]

* [[second fundamental form]]

## References

Original discussion:

* {#EellsSampson64} [[James Eells]], [[Joseph H. Sampson]], *Harmonic Mappings of Riemannian Manifolds*, American Journal of Mathematics **86** 1 (1964) 109-160 &lbrack;[doi:10.2307/2373037](https://doi.org/10.2307/2373037), [jstor:2373037](https://www.jstor.org/stable/2373037)&rbrack;



On the history of the concept:

* Yuan-Jen Chiang, Andrea Ratto: *Paying Tribute to James Eells and Joseph H. Sampson: In Commemoration of the Fiftieth Anniversary of Their Pioneering Work on Harmonic Maps*, Notices of the AMS **62** 4 (2015) &lbrack;[pdf](https://www.ams.org/notices/201504/rnoti-p388.pdf), full issue: [pdf](http://www.ams.org/notices/201504/201504FullIssue.pdf)&rbrack;

Review and textbooks:

* {#BairdWood03} [[Paul Baird]], [[John C. Wood]]: *Harmonic Morphisms Between Riemannian Manifolds*, Oxford University Press (2003) &lbrack;[doi:10.1093/acprof:oso/9780198503620.001.0001](https://doi.org/10.1093/acprof:oso/9780198503620.001.0001)&rbrack;

* {#LinWang08} Fanghua Lin,  Changyou Wang: *The Analysis of Harmonic Maps and Their Heat Flows*, World Scientific (2008) &lbrack;[doi:10.1142/6679](https://doi.org/10.1142/6679)&rbrack;

* [[Frédéric Hélein]], [[John C. Wood]]: *Harmonic maps*, in: *Handbook of Global Analysis*, Elsevier (2008) 417-491 \[<a href="https://doi.org/10.1016/B978-044452833-9.50009-7">doi:10.1016/B978-044452833-9.50009-7</a>, [pdf](https://math.jhu.edu/~js/Math748/helein.harmonic.pdf)\]

* {#Jost17} [[Jürgen Jost]], Ch. 9 in: *Riemannian Geometry and Geometric Analysis*, Springer (2017) &lbrack;[doi:10.1007/978-3-319-61860-9](https://doi.org/10.1007/978-3-319-61860-9)&rbrack;

* Wikipedia, _[Harmonic map](https://en.wikipedia.org/wiki/Harmonic_map)_

Extensive bibliography:

* *Harmonic Maps Bibliography* &lbrack;[people.bath.ac.uk/feb/harmonic.html](https://people.bath.ac.uk/feb/harmonic.html)&rbrack;

Discussion in the context of [[action functionals]] for [[theory (physics)|theories of physics]] (nonlinear [[sigma models]]):

* [[Charles Misner]], _Harmonic maps as models for physical theories_, Phys. Rev. D **18** 4510 (1978) &lbrack[spire:137431](http://inspirehep.net/record/137431)&rbrack;

Discussion in the context of [[integrable systems]]:

* [[Shabnam Beheshti]], A. Shadi Tahvildar-Zadeh, _Integrability and Vesture for Harmonic Maps into Symmetric Spaces_ &lbrack;[arXiv:1209.1383](http://arxiv.org/abs/1209.1383)&rbrack;



[[!redirects harmonic maps]]

[[!redirects Dirichlet energy]]
[[!redirects Dirichlet energies]]