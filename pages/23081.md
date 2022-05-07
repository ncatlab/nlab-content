
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A [[pointed topological space]] $(X,x)$ is called *well-pointed* if the base-point inclusion $\{x\} \xhookrightarrow{\;} X$ is a [[Hurewicz cofibration]] (e.g. [Bredon 1993, VII, Def. 1.8](#Bredon93)).

A [[topological group]] is called well-pointed if it is so at its [[neutral element]], hence if $\{\mathrm{e}\} \xhookrightarrow{\;} G$ is a [[Hurewicz cofibration]].

A [[simplicial topological group]] is well-pointed if all its component groups are.

A key property of well-pointed topological groups (in the [[convenient category of topological spaces|convenient]] context of [[compactly generated weak Hausdorff spaces]]) is that the [[nerves]] of their [[delooping groupoids]] are [[good simplicial topological spaces]] (by [this Ex.](Hurewicz+cofibration#KifiedProductsOfCofibrationsWithCompactlyGeneratedSpaces)). Similarly, the underlying simplicial topological spaces of well-pointed simplicial topological groups are [[good simplicial topological space|good]] ([this Prop.](simplicial+topological+group#RealizationOfWellPointedIsWellPointed)). These facts explain the key role of well-pointedness in [[classifying space]]-theory, where it ensures that plain [[topological realization of simplicial topological spaces]] coincides, up to [[weak homotopy equivalence]], with [[fat geometric realization]] and hence with the [[homotopy colimits]].

## Examples


\begin{example}\label{ParacompactBanachManifoldsAreWellPointed}
  Every [[locally Euclidean topological space|locally Euclidean]] [[Hausdorff space]] is well-pointed, in particular every [[topological manifold]] is well pointed. In fact, every [[paracompact topological space|paracompact]] [[Banach manifold]] is well-pointed.
\end{example}
(Immediate by the discussion of [examples of Hurwicz cofibrations](Hurewicz+cofibration#Examples)).

\begin{example}\label{PointInclusionIntoPUH}
**(the [[projective unitary group]] [[PU(ℋ)]])**
\linebreak
  The [[projective unitary group]] [[PU(ℋ)]] on an infinite-dimensional [[separable Hilbert space|separable]] [[Hilbert space]] is:

* a [[Banach Lie group]] in its [[norm topology]], and as such [[well-pointed topological group|well-pointed]] by Ex.\ref{ParacompactBanachManifoldsAreWellPointed};

* no longer a Banach space in its weak/strong [[operator topology]], but nevertheless still [[well-pointed topological group|well-pointed]] in this case, by [this Prop.](projective+unitary+group+on+a+Hilbert+space#WellPointedInOperatorTopology).

\end{example}

## References

Textbook accounts:

* {#Bredon93} [[Glen Bredon]], Section VII.1 of: _Topology and Geometry_, Graduate texts in mathematics **139**, Springer 1993 ([doi:10.1007/978-1-4757-6848-0](https://link.springer.com/book/10.1007/978-1-4757-6848-0),  [pdf](http://virtualmath1.stanford.edu/~ralph/math215b/Bredon.pdf))




[[!redirects well-pointed topological spaces]]

[[!redirects well pointed topological space]]
[[!redirects well pointed topological spaces]]

[[!redirects well-pointed topological group]]
[[!redirects well pointed topological group]]
[[!redirects well-pointed topological groups]]
[[!redirects well pointed topological groups]]

[[!redirects well-pointed simplicial topological group]]
[[!redirects well pointed simplicial topological group]]
[[!redirects well-pointed simplicial topological groups]]
[[!redirects well pointed simplicial topological groups]]

[[!redirects well-sectioned simplicial topological group]]
[[!redirects well sectioned simplicial topological group]]
[[!redirects well-sectioned simplicial topological groups]]
[[!redirects well sectioned simplicial topological groups]]
