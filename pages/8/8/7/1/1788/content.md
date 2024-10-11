[[lift]]

**A notorious bug:**

The code 

"<nowiki>[[Set]] [[topos]]</nowiki>"

renders as:

[[Set]] [[topos]]

(lacking the whitespace).

Similarly the code

"<nowiki>[[Set]] &dollar;topos&dollar;</nowiki>"

renders without the whitespace:

[[Set]] $topos$ 

This issue goes away when we are not at the beginning of a line. For instance

"<nowiki>A [[Set]] [[topos]]</nowiki>"

renders correctly as

A [[Set]] [[topos]]

and 

"<nowiki>A [[Set]] &dollar;topos&dollar;</nowiki>"

renders correctly as

A [[Set]] $topos$

\linebreak

\linebreak

\linebreak

***

\linebreak

\linebreak

\linebreak

[[test2.txt:file]]

\linebreak

\linebreak

\linebreak


***

\linebreak

\linebreak

\linebreak


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
 The Barratt nerve of the "simplicial $n$-sphere" $\Delta^n/\partial \Delta^n$ is [[contractible homotopy type|contractible]]:
$$
  Ba\big(\Delta^n/\partial \Delta^n\big)
  \;\underset{iso}{\simeq}\;
  \Delta^n
  \,.
$$
\end{example}
&lbrack;[WJR13 p 28](#WaldhausenJahrenRognes13)&rbrack;

But on "non-singular" simplicial sets such as produced by [[subdivision]] $Sd \,\colon\, sSet \xrightarrow{\;} sSet$, the Barratt nerve produces a [[weak homotopy equivalence|weakly homotopy equivalent]] type

The composite 
$$
  Ba \circ Sd \,\colon\, sSet \xrightarrow{\;} sSet
$$
is called the *improvement functor* in [WJR13 Thm 2.5.2](#WaldhausenJahrenRognes13).

\begin{proposition}\label{BaSdIsHomotopyGood}
  The [[natural transformation]]
  $$
    Ba Sd (X) \xrightarrow{\;} X
  $$
  is a [[weak homotopy equivalence]] and in fact a [[triangulation]] in that its [[topological realization]] is [[homotopy|homotopic]] to a [[homeomorphism]].
\end{proposition}
&lbrack;[Fjellbo 2020](#Fjellbo20)&rbrack;



## References

* {#WaldhausenJahrenRognes13} [[Friedhelm Waldhausen]], Bjørn Jahren, [[John Rognes]]: *Spaces of PL Manifolds and Categories of Simple Maps*, Annals of Mathematics Studies, Princeton University Press (2013) &lbrack;[jstor:j.ctt24hqsv](https://www.jstor.org/stable/j.ctt24hqsv), [pdf](https://sma.epfl.ch/~hessbell/topsem/WaldhausenJahrenRognes.pdf)&rbrack;

* Rune Vegard Fjellbo, p. 21 of: *Non-singular simplicial sets*, PhD thesis (2018) &lbrack;[URN:NBN:no-75277](http://urn.nb.no/URN:NBN:no-75277)&rbrack;

* {#Fjellbo20} Rune Vegard Fjellbo: *Optimal Triangulation of Regular Simplicial Sets* &lbrack;[arXiv:2001.04339](https://arxiv.org/abs/2001.04339)&rbrack;



***



$$
  \sigma(r)
  \;\coloneqq\;
  (-1)^{r(r+1)/2}
$$

$$
  \sigma(r+1)
  \;=\;
  (-1)^{
    (r+1)(r+2)/2
  }
  \;=\;
  (-1)^{
    (r^2 + r + 2r + 2)/2
  }
  \;=\;
  \sigma(r)
  \cdot
  (-1)^{
    (2r + 2)/2
  }
  \;=\;
  -(-1)^r \cdot \sigma(r)
$$

$$
  \sigma(r-1)
  \;=\;
  (-1)^{
    (r-1)r/2
  }
  \;=\;
  (-1)^{
    (r^2 + r - 2r)/2
  }
  \;=\;
  (-1)^r \, \sigma(r)
$$

## Sugimoto string theory


The *Sugimoto string theory* is a non-[[supersymmetry|supersymmetric]] version of [[type I string theory]], given by 10d [[type IIB string theory]] on an $O9^+$ [[orientifold]] (instead of $O9^-$), hence with [[RR-field tadpole cancellation]] by 32 *[[anti-brane|anti]]* [[D9-branes]] (instead of plain D9-branes), whose [[gauge group]] is the [[symplectic group]] $USp(32)$.

## References

The original article:

* {#Sugimoto99} [[Shigeki Sugimoto]]: *Anomaly Cancellations in the Type I D9-anti-D9 System and the $USp(32)$ String Theory*, Prog. Theor. Phys. **102** (1999) 685-699 &lbrack;[arXiv:hep-th/9905159](https://arxiv.org/abs/hep-th/9905159), [doi:10.1143/PTP.102.685](https://doi.org/10.1143/PTP.102.685)&rbrack;

Further discussion:

* Sanefumi Moriyama: *$USp(32)$ String as Spontaneously Supersymmetry Broken Theory*, Phys. Lett. B **522** (2001) 177-180 &lbrack;[arXiv:hep-th/0107203](https://arxiv.org/abs/hep-th/0107203), <a href="https://doi.org/10.1016/S0370-2693(01)01278-3">doi:10.1016/S0370-2693(01)01278-3</a>&rbrack;

* Hector Parra de Freitas, p. 166 of: *String Compactifications with Half-maximal Supersymmetry*, PhD thesis, Université Paris-Saclay (2023) &lbrack;[hal/tel-04234221](https://theses.hal.science/tel-04234221), [pdf](https://theses.hal.science/tel-04234221v1/file/133300_PARRA_DE_FREITAS_2023_archivage.pdf)&rbrack;




