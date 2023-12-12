[[!redirects fibred transformation]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Fibred category theory
+-- {: .hide}
[[!include fibred category theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
**Fibred natural transformations** are natural transformations between [[fibred functors]].
They are 2-cells in the [[2-category]] $\mathbf{Fib}$.

## Definition
Given [[fibred category|fibrations]] $p$ and $p'$ and [[fibred functors]] $F,G:p \to p'$, a **fibred natural transformation** $\alpha=(\alpha_1,\alpha_0):F \Rightarrow G$ is a pair of 2-cells as follows:
\begin{tikzcd}
	{\mathcal{E}} && {\mathcal{E}'} \\
	{\mathcal{B}} && {\mathcal{B}'}
	\arrow[""{name=0, anchor=center, inner sep=0}, "{F_0}"{pos=0.45}, bend left=20, from=2-1, to=2-3]
	\arrow[""{name=1, anchor=center, inner sep=0}, "{F_1}"{pos=0.45}, bend left=20, from=1-1, to=1-3]
	\arrow[""{name=2, anchor=center, inner sep=0}, "{G_1}"'{pos=0.55}, bend right=20, from=1-1, to=1-3]
	\arrow[""{name=3, anchor=center, inner sep=0}, "{G_0}"'{pos=0.55}, bend right=20, from=2-1, to=2-3]
	\arrow["p"', from=1-1, to=2-1]
	\arrow["{p'}", from=1-3, to=2-3]
	\arrow[shorten <=2pt, shorten >=2pt, Rightarrow, from=1, to=2]
	\arrow[shorten <=2pt, shorten >=2pt, Rightarrow, from=0, to=3]
\end{tikzcd}
This means $\alpha_0:F_0 \Rightarrow G_0$, $\alpha_1:F_1 \Rightarrow G_1$ and $p'(\alpha_1) = \alpha_0 p$.

When looking at fibrations over a fixed base $\mathcal{B}$, then $F_0=G_0=1_{\mathcal{B}}$, and also $\alpha_0$ is the identity natural transformation.
In that case, $\alpha$ reduces to a natural transformation between the functor $F_1$ and $G_1$ whose components are vertical, i.e. stay in the fibers.

## See also
* [[fibred category]], [[fibred functor]]

* [[natural transformation]]

[[!redirects fibred transformation]]
[[!redirects fibred transformations]]
[[!redirects fibered transformations]]
[[!redirects fibered natural transformation]]
[[!redirects fibered natural transformations]]
[[!redirects fibred natural transformations]]

[[!redirects transformation of fibred functors]]
[[!redirects transformations of fibred functors]]
[[!redirects transformation of fibered functors]]
[[!redirects transformations of fibered functors]]

[[!redirects natural transformation of fibrations]]
[[!redirects natural transformations of fibrations]]

[[!redirects 2-cell of fibrations]]
[[!redirects 2-cells of fibrations]]