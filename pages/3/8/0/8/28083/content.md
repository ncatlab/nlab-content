
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


\tableofcontents



## Idea

The analogue of [[equalizers]] in [[dagger categories]]. 

## Definition

For two [[parallel morphisms]] $f \colon x \to y$ and $g \colon x \to y$ in a [[dagger category]] $(\mathcal{C}, \dagger)$, a **dagger equalizer** is a [[dagger monomorphism]] $e \colon \mathrm{eq} \to x$ from an [[object]] $\mathrm{eq} \in \mathcal{C}$ such that
\begin{centre}
    \begin{tikzcd}
\mathrm{eq} \arrow[r, "e"] & x \arrow[r, shift right=4pt, "g"'] \arrow[r, shift left=4pt, "f"] & y
    \end{tikzcd}
\end{centre}
[[commuting diagram|commutes]] (i.e., $f \circ e = g \circ e$), and every morphism $h \colon z \to x$ so that $f \circ h = g \circ h$ factors through $e$:

\begin{centre}
    \begin{tikzcd}
\mathrm{eq} \arrow[r, "e"] & x \arrow[r, shift right=4pt, "g"'] \arrow[r, shift left=4pt, "f"] & y. \\ z \arrow[u, "\exists"] \arrow[ur, "h"']
    \end{tikzcd}
\end{centre}

If $(\mathcal{C}, \dagger)$ also has a [[zero object]] $0$, then when $g=0_!: x \to 0 \to y$ is the unique [[zero morphism]], the dagger equalizer $e \colon \mathrm{eq} \to x$ is called the **dagger kernel**. This is the analogue of [[kernels]] in ordinary [[category theory]].


## References

An exposition of dagger categories that discusses dagger equalizers and dagger kernels in their relation to [[algebroid | linear structure]] and [[quantum measurement]]:

* {#HeunenVicary19} [[Chris Heunen]], [[Jamie Vicary]]: *Categories for Quantum Theory*, Oxford University Press (2019) \[<a href="https://global.oup.com/academic/product/categories-for-quantum-theory-9780198739616">ISBN:9780198739616</a>\]

based on:

* {#HeunenVicary12} [[Chris Heunen]], [[Jamie Vicary]], *Lectures on categorical quantum mechanics* (2012) \[<a href="https://www.cs.ox.ac.uk/files/4551/cqm-notes.pdf">pdf</a>, [[HeunenVicary-QuantumLectures.pdf:file]]\]

Dagger equalizers and dagger kernels used to axiomatize the category [[Hilb]] of [[Hilbert spaces]]: 

* [[Chris Heunen]], [[Andre Kornell]], *Axioms for the category of Hilbert spaces* ([arXiv:2109.07418](https://arxiv.org/abs/2109.07418))


[[!redirects dagger equalizers]]

[[!redirects dagger equaliser]]
[[!redirects dagger equalisers]]


[[!redirects dagger kernel]]
[[!redirects dagger kernels]]


