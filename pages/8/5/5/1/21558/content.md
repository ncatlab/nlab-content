\tableofcontents

\section{Idea}

The _walking isomorphism_ or _free-standing isomorphism_ or _interval groupoid_ is the [[category]] (in fact a [[groupoid]]) which 'represents' [[isomorphism|isomorphisms]] in a category.

The word "walking" is because it's a "[[walking structure]]".

The walking isomorphism can be [[categorified]] in a number of ways: to the [[walking equivalence]], to the [[walking adjoint equivalence]], or to the [[walking 2-isomorphism]]. Related, though not quite a categorification in one of the usual senses, is the [[walking 2-isomorphism with trivial boundary]]. 

\section{Definition}

\begin{defn} The _free-standing isomorphism_ is the unique (up to isomorphism) category with exactly two objects $0$ and $1$, exactly one arrow $0 \rightarrow 1$, exactly one arrow $1 \rightarrow 0$, and no other arrows which are not identity arrows. \end{defn}

\begin{rmk} The arrow $0 \rightarrow 1$ is an isomorphism, whose inverse is the arrow $1 \rightarrow 0$. \end{rmk}

\begin{rmk} The free-standing isomorphism is a groupoid. \end{rmk}

\begin{rmk} The free-standing isomorphism can also be described as the [[free groupoid]] on the [[interval category]], that is to say, the walking arrow. Because it is an [[interval object]] for [[Cat]] and [[Grpd]], it is also known as the _interval groupoid_.\end{rmk}

\section{Representing of isomorphisms}

\begin{prpn}
Let $\mathcal{A}$ be a category. Let $\mathcal{I}$ denote the free-standing isomorphism.
Evaluation at the arrow $0\to 1$ establishes a natural bijective
correspondence between functors $\mathcal{I}\to\mathcal{A}$
and isomorphisms in $\mathcal{A}$.
Thus, for any isomorphism $f$ of $\mathcal{A}$ there is a unique [[functor]] $F: \mathcal{I} \rightarrow \mathcal{A}$ such that the arrow $0 \rightarrow 1$ of $\mathcal{I}$ maps under $F$ to $f$.
\end{prpn}

\begin{proof} Immediate from the definitions. \end{proof}

\section{Properties}

\begin{prpn} $\{ 1 \} \subseteq \mathcal{I}$ is the full subcategory classifier of the 1-category $Cat$. That is, for any small category $\mathcal{A}$, there is a bijective correspondence between full subcategories of $\mathcal{A}$ and functors $\mathcal{A} \to \mathcal{I}$, with the reverse direction given by taking the pullback of the inclusion $\{ 1 \} \subseteq \mathcal{I}$.
\end{prpn}
\begin{proof} Functors into $\mathcal{I}$ are uniquely determined by functions on the sets of objects. $\{ 1 \}$ is a full subcategory of $\mathcal{I}$, and any pullback of a full subcategory can be given as a full subcategory. 
\end{proof}

In fact, this generalizes. If $X$ is a simplicial set, say that a _full subspace_ of $X$ is a subsimplicial set $S \subseteq X$ with the property there is some subset $S_0 \subseteq X_0$ such that $S$ contains exactly the simplices whose vertices are all contained in $S_0$.

\begin{prpn} The nerve $N(\mathcal{I})$ is the full subspace classifier for $sSet$,
and thus $N(\mathcal{I})$ represents the subpresheaf $FullSub \subseteq Sub$ of full subspaces. \end{prpn}
\begin{proof} This can be determined from the explicit description of $N_n(\mathcal{I}) \cong \{ 0, 1 \}^{n+1}$ given by listing the vertices of a path. However, it's more informative to observe that $N(\mathcal{I}) = indisc(\{ 0, 1 \})$, where $indisc$ is the _indiscrete space_ functor, which is the direct image part of the geometric embedding $Set \subseteq sSet$ whose inverse image is $X \mapsto X_0$. 
\end{proof}

\begin{rmk} This also implies $N(\mathcal{I})$ is the full subcategory classifier of $qCat$, the 1-category of [[quasi-category|quasi-categories]], since those are given by full subspaces of simplicial sets. \end{rmk}

[[!redirects free-standing isomorphism]]
[[!redirects interval groupoid]]