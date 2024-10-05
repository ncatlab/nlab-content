
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


\tableofcontents

## Definition

\begin{definition}\label{BarrattNerve}
Given a [[simplicial set]] $X \in sSet$, let $ndg(X)$ denote its [[set]] of non-degenerate [[simplices]], regarded as a [[partially ordered set]] ([[poset]]) where $\sigma \leq \sigma'$ iff $\sigma$ is a face of $\sigma'$.

With [[posets]] regarded (see [there](partial+order#AsACategoryWithExtraProperties)) as [[categories]], let $N(ndg(X)) \,\in\, sSet$ be the [[nerve of a category|simplicial nerve]] of the poset of non-degenerate simplices. This is also called the **Barratt nerve** of $X$ (in honor of [[Michael Barratt]]):
\[
  \label{BarrattNerve}
  Ba(X) \,\coloneqq\, N\big(ndg(X)\big)
  \,.
\]
\end{definition}
&lbrack;[Waldhausen, Jahren & Rognes 2013 Def. 2.2.3](#WaldhausenJahrenRognes13)&rbrack;


## Properties

In general (namely on simplicial sets which are "singular"), the Barratt nerve (eq:BarrattNerve) is not [[simplicial homotopy theory|homotopically]] well-behaved. For instance:

\begin{example}
 The Barratt nerve of the "simplicial [[n-sphere|$n$-sphere]]" $\Delta^n/\partial \Delta^n$ is the [[1-simplex]] and hence [[contractible homotopy type|contractible]]:
$$
  Ba\big(\Delta^n/\partial \Delta^n\big)
  \;\underset{iso}{\simeq}\;
  \Delta^1
  \,.
$$
\end{example}
&lbrack;[WJR13 p 28](#WaldhausenJahrenRognes13)&rbrack;

But on "non-singular" simplicial sets such as produced by [[subdivision]] $Sd \,\colon\, sSet \xrightarrow{\;} sSet$, the Barratt nerve produces [[weak homotopy equivalence|weakly homotopy equivalent]] types:

\begin{proposition}\label{BaSdIsHomotopyGood}
  The [[natural transformation]]
  $$
    Ba \circ Sd (X) \xrightarrow{\;} X
  $$
  is a [[weak homotopy equivalence]] and in fact a [[triangulation]] in that its [[topological realization]] is [[homotopy|homotopic]] to a [[homeomorphism]].
\end{proposition}
&lbrack;[Fjellbo 2020](#Fjellbo20)&rbrack;

Hence the Barratt nerve of the subdivision models the [[homotopy type]] of any simplicial set by the [[nerve]] of a [[poset]]. This composite
$$
  Ba \circ Sd \,\colon\, sSet \xrightarrow{\;} sSet
$$
is called the *improvement functor* in [WJR13 Thm 2.5.2](#WaldhausenJahrenRognes13).



## References

* {#WaldhausenJahrenRognes13} [[Friedhelm Waldhausen]], Bjørn Jahren, [[John Rognes]]: *Spaces of PL Manifolds and Categories of Simple Maps*, Annals of Mathematics Studies, Princeton University Press (2013) &lbrack;[jstor:j.ctt24hqsv](https://www.jstor.org/stable/j.ctt24hqsv), [pdf](https://sma.epfl.ch/~hessbell/topsem/WaldhausenJahrenRognes.pdf)&rbrack;

* Rune Vegard Fjellbo, p. 21 of: *Non-singular simplicial sets*, PhD thesis (2018) &lbrack;[URN:NBN:no-75277](http://urn.nb.no/URN:NBN:no-75277)&rbrack;

* {#Fjellbo20} Rune Vegard Fjellbo: *Optimal Triangulation of Regular Simplicial Sets* &lbrack;[arXiv:2001.04339](https://arxiv.org/abs/2001.04339)&rbrack;

[[!redirects Barratt nerves]]

