
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

\tableofcontents

\section{Idea}

In a [[higher category theory|higher category]], [[inverse|invertibility]] of [[n-morphisms]] in its highest dimension is always considered strictly. Thus in an ordinary [[category]], we have [[1-morphisms]] which can be [[isomorphism|isomorphisms]]. In a [[2-category]], it is the [[2-morphisms]] for which, when it comes to invertibility, we always ask for a strict inverse, whereas for [[1-morphisms]] we typically ask only for an [[equivalence]]. These 2-morphisms which admit an inverse are known as _2-isomorphisms_.

\section{Definition}

\begin{defn} Let $\mathcal{A}$ be a [[2-category]]. A _2-isomorphism_ in $\mathcal{A}$ is a 2-arrow $\phi : f \rightarrow f'$ of $\mathcal{A}$ which admits a (strict) inverse, that is to say, there is a 2-arrow $\phi^{-1}: f' \rightarrow f$ of $\mathcal{A}$ such that $\phi^{-1} \circ \phi = id(f)$ and $\phi \circ \phi^{-1} = id\left(f' \right)$. \end{defn}

\section{Related concepts}

A 2-category in which every 2-arrow is a 2-isomorphism is known as a [[(2,1)-category]].

[[!redirects 2-isomorphisms]]

