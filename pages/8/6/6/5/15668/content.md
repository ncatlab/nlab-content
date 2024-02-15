
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[arithmetic geometry]] over a [[finite field]] a _shtuka_ on an [[arithmetic scheme]] is essentially an [[equivariant bundle|equivariant]] [[algebraic vector bundle]] on the [[product]] of the scheme with a given [[arithmetic curve]], where equivariance is with respect to the [[action]] of the [[Frobenius endomorphism]] (e.g. [Scholze-Weinstein, def. 1](#ScholzeWeinstein14)).

(*Shtuka* is a Russian word colloquially meaning "thing".)


## Definition
\begin{definition} (Definition 7.1 in [#Scholze17](#Scholze17))

Let $X$ be a smooth projective curve over $\mathbb{F}_{p}$ and let $S$ be a scheme over $\mathbb{F}_{p}$. A shtuka over $S$ relative to $X$ with legs at $x_{1},\ldots,x_{n}:S\to X$ is a [[vector bundle]] $\mathcal{E}$ over $S\times_{\mathbb{F}_{p}}X$ together with an isomorphism

$$\mathrm{Frob}_{S}^{\ast}\mathcal{E}\vert_{S\times_{\mathbb{F}_{p}} X\setminus \bigcup_{i=1}^{n}\Gamma_{x_{i}}}\cong\mathcal{E}\vert_{S\times_{\mathbb{F}_{p}} X\setminus \bigcup_{i=1}^{n}\Gamma_{x_{i}}}$$

\end{definition}

## Related concepts

* [[Rapoport-Zink space]]


##References


Reviews of the basic definition include

* [[David Goss]], *What is ... a Shtuka?*, Notices of the AMS **50** 1 (2003) 36-37 &lbrack;[pdf](http://www.ams.org/notices/200301/what-is.pdf), full issue:[pdf](http://www.ams.org/notices/200301/200301FullIssue.pdf)&rbrack;

* Wikipedia, _[Drinfeld module -- Shtuka](http://en.wikipedia.org/wiki/Drinfeld_module#Shtukas)_

Definition 1 in 

* {#ScholzeWeinstein14} [[Jared Weinstein]], notes from lecture by [[Peter Scholze]], _Peter Scholze's lectures on $p$-adic geometry_, MSRI 2014 ([pdf](http://math.bu.edu/people/jsweinst/Math274/ScholzeLectures.pdf))

More conceptual discussion, in the context of the [[function field analogy]], is in 

* {#Hartl06} [[Urs Hartl]], _A Dictionary between Fontaine-Theory and its Analogue in Equal Characteristic_ ([arXiv:math/0607182](http://arxiv.org/abs/math/0607182))

* {#Scholze17} [[Peter Scholze]], _p-adic geometry_, [arXiv:1712.03708](https://arxiv.org/abs/1712.03708)

[[!redirects shtukas]]

