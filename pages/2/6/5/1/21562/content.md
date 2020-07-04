\tableofcontents

\section{Idea}

The _walking equivalence_ or _free-standing equivalence_ is the [[2-category]] (in fact a [[(2,1)-category]]) which 'represents' [[equivalence|equivalences]] in a 2-category. It is a categorification of the [[free-standing isomorphism]], though not the only one: the [[walking adjoint equivalence]] is another.

\section{Definition}

\begin{defn} The _free-standing equivalence_ is the unique (up to isomorphism) strict 2-category with exactly two objects $0$ and $1$, exactly one arrow $i: 0 \rightarrow 1$, exactly one arrow $i^{-1}: 1 \rightarrow 0$, exactly one 2-arrow $\iota_{0}: i^{-1} \circ i \rightarrow id(0)$, exactly one 2-arrow $\iota_{0}^{-1}: id(0) \rightarrow i^{-1} \circ i$, exactly one 2-arrow $\iota_{1}: i \circ i^{-1} \rightarrow id(1)$, exactly one 2-arrow $\iota_{1}^{-1}: id(1) \rightarrow i^{-1} \circ i$, and no 1-arrows $0 \rightarrow 0$ or $1 \rightarrow 1$ except those which are identity arrows or compositions of $i$ and $i^{-1}$. \end{defn}

\begin{rmk} The arrow $i: 0 \rightarrow 1$ is an [[equivalence]], whose inverse-up-to-isomorphism is the arrow $i^{-1}:1 \rightarrow 0$. \end{rmk}

\begin{rmk} The 2-arrows $\iota_{0}: i^{-1} \circ i \rightarrow id(0)$ and $\iota_{1}: i \circ i^{-1} \rightarrow id(1)$ are [[2-isomorphism|2-isomorphisms]], whose inverses are the 2-arrows $\iota_{0}^{-1}$ and $\iota_{1}^{-1}$. \end{rmk}

\begin{rmk} The free-standing equivalence is a [[(2,1)-category]]. \end{rmk}

\section{Representing of equivalences}

\begin{prpn} Let $\mathcal{A}$ be a 2-category (weak or strict). Let $\mathcal{E}$ denote the free-standing equivalence. Let $f$ be a 1-arrow of $\mathcal{A}$ which is an [[equivalence]]. Then there is a unique [[2-functor|functor]] $F: \mathcal{E} \rightarrow \mathcal{A}$ such that the arrow $i:0 \rightarrow 1$ of $\mathcal{I}$ maps under $F$ to $f$. \end{prpn}

\begin{proof} Immediate from the definitions. \end{proof}

[[!redirects free-standing equivalence]]