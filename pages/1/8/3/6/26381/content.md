

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea
A **monoidal actegory** is a [[pseudoaction]] in the [[2-category]] $\mathbf{MonCat}$ of [[monoidal categories]], [[strong monoidal functors]] and [[monoidal natural transformations]].
Roughly, it is an [[actegory]] whose _actee_ is monoidal and such that the action is compatible with this structure.

## Definition
Since pseudoactions are actions of [[pseudomonoids]], and since a pseudomonoid in $\mathbf{MonCat}$ is a [[braided monoidal category]], monoidal actegories are always actions of braided monoidal categories.

The following comes from Definition 5.1.1 in ([Capucci and Gravranovic 2022](#CG22)):

\begin{definition}
Let $(\mathcal{M}, j, \otimes)$ be a braided monoidal category.
A left *monoidal $\mathcal{M}$-actegory* is a monoidal category $(\mathcal{C}, i,\boxtimes)$ together with a strong monoidal functor, called **action**, $\odot:\mathcal{M} \times \mathcal{C} \to \mathcal{C}$, and monoidal natural transformations $\eta_x : j \odot x \to x$, $\mu_{m,n,x} : (m \otimes n) \odot x \to m \odot (n \odot x)$ satisfying the coherence laws of unitor and multiplicator of an [[actegory]].
\end{definition}

All the coherence laws of a monoidal actegory are spelled out in Appendix A of ([Capucci and Gravranovic 2022](#CG22)).

The fact $\odot$ is strong monoidal means it comes equipped with a structural morphism called **mixed interchanger**:
\[
\iota_{m,x,n,y} : (m \otimes n) \odot (x \boxtimes y) \to (m \odot x) \boxtimes (n \odot y).
\]
It would also come with $\upsilon : i \to j \odot i$, but the monoidality of $\eta$ makes it so that $\upsilon = \eta_i$, making the first redundant.

### Braiding
Consider pseudoactions in $\mathbf{BrMonCat}$ and $\mathbf{SymMonCat}$. Now carriers of the action are braided functors, and the actee are braided monoidal categories.

The following appear as 5.4.1 and 5.4.3 in ([Capucci and Gravranovic 2022](#CG22)):

\begin{definition}
Let $(\mathcal{M}, j, \otimes, \sigma)$ be a symmetric monoidal category.
A left **braided monoidal $\mathcal{M}$-actegory** is a braided monoidal category $(\mathcal{C}, i, \boxtimes, \beta)$ equipped with a braided monoidal functor $\odot: \mathcal{M} \times \mathcal{C} \to \mathcal{C}$ and two monoidal natural transformations $\eta$ and $\mu$ as above.
Thus it satisfies the axioms of monoidal actegory and an additional compatibility axiom with the braided structure of $\mathcal{M}$ and $\mathcal{C}$:

\begin{tikzcd}
	{(m \otimes n) \odot (x \boxtimes y)} && {(m \odot x) \boxtimes (n \odot y)} \\
	{(n \otimes m) \odot (y \boxtimes x)} && {(n \odot y) \boxtimes (m \odot x)}
	\arrow["\iota", from=1-1, to=1-3]
	\arrow["\beta", from=1-3, to=2-3]
	\arrow["\iota"', from=2-1, to=2-3]
	\arrow["{\sigma \odot \beta}"', from=1-1, to=2-1]
\end{tikzcd}

If $\mathcal{C}$ is symmetric, then we call $(\mathcal{C}, \odot)$ a **symmetric monoidal actegory**.
\end{definition}

## Classifying objects
Actegories are famously equivalent to monoidal functors $\mathcal{M} \to [\mathcal{C},\mathcal{C}]$. We can thus say that $[\mathcal{C},\mathcal{C}]$ *classifies* actions on $\mathcal{C}$.

When the action is monoidal, braided or symmetric monoidal, the classifier is different:

* Monoidal actions are classified by $Z(\mathcal{C})$, i.e. the [[Drinfeld center]] of $\mathcal{C}$.
* Braided monoidal actions are classified by $\Sigma(\mathcal{C})$, i.e. the [[symmetric center]] of $\mathcal{C}$, which is the full subcategory of $\mathcal{C}$ spanned by those objects $x:\mathcal{C}$ such that $\beta_{x,-}\beta_{-,x} = 1$.
* Symmetric monoidal actions are classified by $\mathcal{C}$ itself. In fact a symmetric monoidal action $\odot$ of $\mathcal{M}$ on $\mathcal{C}$ gives a symmetric monoidal functor $- \odot i : \mathcal{M} \to \mathcal{C}$, and viceversa $F(-) \boxtimes -$ is a symmetric monoidal action whenever $\mathcal{M} \to \mathcal{C}$ is a [[braided monoidal functor]] between [[symmetric monoidal categories]].

This is all proven in Section 5.5 of [Capucci & Gravranovic 2022](#CG22).

## See also
* [[actegories]], [[pseudoaction]]
* [[para construction]] ($\mathbf{Para}(\odot)$ is monoidal iff $\odot$ is)
* [[periodic table]]

## References

* {#CG22} [[Matteo Capucci]], Bruno Gavranović, _Actegories for the working amthematician_, [arXiv:2203.16351](https://arxiv.org/abs/2203.16351)

[[!redirects monoidal actions of a monoidal category]]
[[!redirects monoidal actions of monoidal categories]]

[[!redirects monoidal actegory]]
[[!redirects braided actegory]]
[[!redirects symmetric actegory]]

[[!redirects braided monoidal actegory]]
[[!redirects symmetric monoidal actegory]]

[[!redirects monoidal action]]
[[!redirects braided monoidal action]]
[[!redirects symmetric monoidal action]]

[[!redirects monoidal actegories]]
[[!redirects braided monoidal actegories]]
[[!redirects symmetric monoidal actegories]]
