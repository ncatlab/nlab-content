
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[diffeological space]], the _D-topology_ ("diffeological topology") is a natural [[topological space|topology]] on its underlying [[set]] of [[points]], namely the [[final topology]] which makes all its [[plots]] be [[continuous functions]].

## Definition
 {#Definition}

\begin{definition}
  Given a [[diffeological space]] $(X, plots)$, with set of $plots \,\subset\, \underset{n \in \mathbb{N}}{\coprod} Set(\mathbb{R}^n,\, X)$, 
the *D-topology* $\tau_D$ on the [[underlying]] [[set]] $X$ is the [[final topology]] on $X$ with respect to the $plots$.

This means that $\tau_D \,\subset\, Sub(X)$ is the topology in which a [[subset]] $U \subset X$ is [[open subset|open]] if and only if under each $\big(\mathbb{R}^n \xrightarrow{\phi} X \big) \,\in\, plots$
its [[preimage]] $\phi^{-1}(U) \subset \mathbb{R}^n$ is open in the [[Euclidean space|Euclidean topology]] on the plot's [[domain]].
\end{definition}

([Iglesias-Zemmour 1985, Def. 1.2.3](#IglesiasZemmour85), review in [IglesiasZemmour 2013, Sec. 2.8](#IglesiasZemmour13), [CSW 2013, Sec. 3](#CSW13))


## Properties

[[!include adjunction between topological spaces and diffeological spaces]]


## Related concepts

* [[D-topological space]]

## References

The concept originates with:

* {#IglesiasZemmour85} [[Patrick Iglesias-Zemmour]], Def. 1.2.3 in: _Fibrations diff&#233;ologiques et Homotopie_,  Doctoral thesis (1985) ([web](http://math.huji.ac.il/~piz/Site/The%20Articles/D9DD15EE-6993-4CA3-8B9B-4FC1DEF4A418.html), [pdf](http://math.huji.ac.il/~piz/documents/TheseEtatPI.pdf), [[IglesiasZemmourFibrationsDiffeologiques1985.pdf:file]])

* {#IglesiasZemmour13} [[Patrick Iglesias-Zemmour]], Section 2.8 of: _Diffeology_, Mathematical Surveys and Monographs, AMS (2013) ([web](http://math.huji.ac.il/~piz/Site/The%20Book.html), [ ISBN:978-0-8218-9131-5](https://bookstore.ams.org/surv-185))

The relation to [[Delta-generated topological spaces]]:

* {#SYH10} [[Kazuhisa Shimakawa]], K. Yoshida, [[Tadayuki Haraguchi]], _Homology and cohomology via enriched bifunctors_, Kyushu Journal of Mathematics, 2018 Volume 72 Issue 2 Pages 239-252 ([arXiv:1010.3336](https://arxiv.org/abs/1010.3336), [doi:10.2206/kyushujm.72.239]( https://doi.org/10.2206/kyushujm.72.239))

Discussion of the D-topology for [[mapping spaces]]:

* {#CSW13} [[J. Daniel Christensen]], [[Gord Sinnamon]], [[Enxin Wu]], _The $D$-topology for diffeological spaces_, Pacific Journal of Mathematics 272 (1), 87-110, 2014 ([arXiv:1302.2935](http://arxiv.org/abs/1302.2935), [doi:10.2140/pjm.2014.272.87](https://msp.org/pjm/2014/272-1/p04.xhtml))

[[!redirects D-topologies]]

[[!redirects diffeological topology]]
[[!redirects diffeological topologies]]

[[!redirects continuous diffeology]]
[[!redirects continuous diffeologies]]

