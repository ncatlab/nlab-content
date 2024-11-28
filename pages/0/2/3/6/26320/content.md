+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **retromorphism** of [[monads]] is a [[retrocell]] between the carriers of the monads, which preserves the unit and multiplication.

## Monads in double categories

Recall that a [[monad]] $(A, t, \eta, \mu)$ in a [[double category]] consists of a loose morphism $t \colon A \nrightarrow A$ and cells 
\begin{tikzcd}
    	A & A \\
    	A & A
    	\arrow["{id_{A}}", "\shortmid"{marking}, from=1-1, to=1-2]
    	\arrow[""{name=0, anchor=center, inner sep=0}, Rightarrow, no head, from=1-1, to=2-1]
    	\arrow[""{name=1, anchor=center, inner sep=0}, Rightarrow, no head, from=1-2, to=2-2]
    	\arrow["t"', "\shortmid"{marking}, from=2-1, to=2-2]
    	\arrow["\eta"{description}, draw=none, from=0, to=1]
\end{tikzcd}
\begin{tikzcd}
    	A & A & A \\
    	A & & A
    	\arrow["t", "\shortmid"{marking}, from=1-1, to=1-2]
    	\arrow[""{name=0, anchor=center, inner sep=0}, Rightarrow, no head, from=1-1, to=2-1]
    	\arrow["t", "\shortmid"{marking}, from=1-2, to=1-3]
    	\arrow[""{name=1, anchor=center, inner sep=0}, Rightarrow, no head, from=1-3, to=2-3]
    	\arrow["t"', "\shortmid"{marking}, from=2-1, to=2-3]
    	\arrow["\mu"{description}, draw=none, from=0, to=1]
\end{tikzcd}
called the *unit* and *multiplication*, respectively, subject to the following axioms.

1.  **Left unitality**: $\mu \circ (\eta \odot 1_{t}) = 1_t$
2.  **Right unitality**: $\mu \circ (1_{t} \odot \eta) = 1_{t}$
3.  **Associativity**: $\mu \circ (\mu \odot 1_{t}) = \mu \circ (1_{t} \odot \mu)$

## Definition

Let $\mathbb{D}$ be a double category equipped with a choice of [[companions]] denoted $(-)_{\ast}$. 

\begin{definition}
A *monad retromorphism* $(f, \varphi) \colon (A, t) \nrightarrow (B, s)$ consists of a tight morphism $f \colon A \to B$ and a cell 
\begin{tikzcd}
	A & B & B \\
	A & A & B
	\arrow["{f_{\ast}}", "\shortmid"{marking}, from=1-1, to=1-2]
	\arrow[""{name=0, anchor=center, inner sep=0}, Rightarrow, no head, from=1-1, to=2-1]
	\arrow["s", "\shortmid"{marking}, from=1-2, to=1-3]
	\arrow[""{name=1, anchor=center, inner sep=0}, Rightarrow, no head, from=1-3, to=2-3]
	\arrow["t"', "\shortmid"{marking}, from=2-1, to=2-2]
	\arrow["{f_{\ast}}"', "\shortmid"{marking}, from=2-2, to=2-3]
	\arrow["\varphi"{description}, draw=none, from=0, to=1]
\end{tikzcd}
in $\mathbb{D}$ subject to the following axioms. 

1. **Respects units**: $\varphi \circ (1_{f_{\ast}} \odot \eta_{s}) = \eta_{t} \odot 1_{f_{\ast}}$
2. **Respects multiplication**: $(\mu_{t} \odot 1_{f_{\ast}}) \circ (1_{t} \odot \varphi) \circ (\varphi \odot 1_{s}) = \varphi \circ (1_{f_{\ast}} \odot \mu_{s})$

\end{definition}

Note that the cell $\varphi$ in the definition corresponds to a [[retrocell]] in $\mathbb{D}$ of the following shape. 
\begin{tikzcd}
	A & A \\
	B & B
	\arrow[""{name=0, anchor=center, inner sep=0}, "t", "\shortmid"{marking}, from=1-1, to=1-2]
	\arrow["f"', from=1-1, to=2-1]
	\arrow["f", from=1-2, to=2-2]
	\arrow[""{name=1, anchor=center, inner sep=0}, "s"', "\shortmid"{marking}, from=2-1, to=2-2]
	\arrow["\varphi"', draw={rgb,255:red,214;green,92;blue,92}, shorten <=20pt, shorten >=20pt, Rightarrow, from=1, to=0]
\end{tikzcd}

## Properties 

\begin{proposition}
\label{prop:module-from-retromorphism}
A monad retromorphism $(f, \varphi) \colon A \nrightarrow B$ induces a [[module over a monad|module]] $(A, t) \nrightarrow (B, s)$ consisting of the loose morphism $t \odot f_{\ast} \colon A \nrightarrow B$ and the cells 

\begin{tikzcd}
	A & A & A & B \\
	A && A & B
	\arrow["t", "\shortmid"{marking}, from=1-1, to=1-2]
	\arrow[""{name=0, anchor=center, inner sep=0}, Rightarrow, no head, from=1-1, to=2-1]
	\arrow["t", "\shortmid"{marking}, from=1-2, to=1-3]
	\arrow["{f_{\ast}}", "\shortmid"{marking}, from=1-3, to=1-4]
	\arrow[""{name=1, anchor=center, inner sep=0}, Rightarrow, no head, from=1-3, to=2-3]
	\arrow[""{name=2, anchor=center, inner sep=0}, Rightarrow, no head, from=1-4, to=2-4]
	\arrow["t"', "\shortmid"{marking}, from=2-1, to=2-3]
	\arrow["{f_{\ast}}"', "\shortmid"{marking}, from=2-3, to=2-4]
	\arrow["\mu"{description}, draw=none, from=0, to=1]
	\arrow["{1_{f_{\ast}}}"{description}, draw=none, from=1, to=2]
\end{tikzcd}

\begin{tikzcd}
	A & A & B & B \\
	A & A & A & B \\
	A && A & B
	\arrow["t", "\shortmid"{marking}, from=1-1, to=1-2]
	\arrow[""{name=0, anchor=center, inner sep=0}, Rightarrow, no head, from=1-1, to=2-1]
	\arrow["{f_{\ast}}", "\shortmid"{marking}, from=1-2, to=1-3]
	\arrow[""{name=1, anchor=center, inner sep=0}, Rightarrow, no head, from=1-2, to=2-2]
	\arrow["s", "\shortmid"{marking}, from=1-3, to=1-4]
	\arrow[""{name=2, anchor=center, inner sep=0}, Rightarrow, from=1-4, to=2-4]
	\arrow["t"', "\shortmid"{marking}, from=2-1, to=2-2]
	\arrow[""{name=3, anchor=center, inner sep=0}, Rightarrow, no head, from=2-1, to=3-1]
	\arrow["t"', "\shortmid"{marking}, from=2-2, to=2-3]
	\arrow["{f_{\ast}}"', "\shortmid"{marking}, from=2-3, to=2-4]
	\arrow[""{name=4, anchor=center, inner sep=0}, Rightarrow, no head, from=2-3, to=3-3]
	\arrow[""{name=5, anchor=center, inner sep=0}, Rightarrow, no head, from=2-4, to=3-4]
	\arrow["t"', "\shortmid"{marking}, from=3-1, to=3-3]
	\arrow["{f_{\ast}}"', "\shortmid"{marking}, from=3-3, to=3-4]
	\arrow["{1_{t}}"{description}, draw=none, from=0, to=1]
	\arrow["\varphi"{description}, draw=none, from=1, to=2]
	\arrow["\mu"{description}, draw=none, from=3, to=4]
	\arrow["{1_{f_{\ast}}}"{description}, draw=none, from=4, to=5]
\end{tikzcd}
determining *left action* and *right action*, respectively. 
\end{proposition}

## Examples

* A monad internal to the [[double category]] $\mathbb{S}\mathrm{pan}$ is a [[small category]]. A monad retromorphism is then a [[retrofunctor]]. 
That each retrofunctor determines a [[profunctor]] is a corollary of Proposition \ref{prop:module-from-retromorphism}. 

* A monad internal the double category of $\mathcal{V}$-matrices for a [[distributive monoidal category]] $(\mathcal{V}, \otimes, I)$ is an [[enriched category]]. A monad retromorphism is then an enriched retrofunctor, and each enriched retrofunctor determines an enriched profunctor. 

## References

The terminology is introduced in the following thesis, where the definition is alluded to:

* [[Matthew Di Meglio]], _The category of asymmetric lenses and its proxy pullbacks_. Master’s thesis. Macquarie University, 2021. doi: 10.25949/20236449, [pdf](https://mdimeglio.github.io/papers/The_category_of_asymmetric_lenses_and_its_proxy_pullbacks.pdf)

A definition is introduced in:

* {#Clarke2022} [[Bryce Clarke]], _The double category of lenses_, PhD thesis, Macquarie University, 2022. ([doi:10.25949/22045073.v1](https://doi.org/10.25949/22045073.v1))

Monad retromorphisms are further studied in:

* [[Robert Paré]], _Retrocells_, [arXiv:2306.06436](https://arxiv.org/abs/2306.06436)


[[!redirects monad retromorphisms]]
