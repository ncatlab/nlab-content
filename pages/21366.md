\tableofcontents

\section{Idea}

The notion of a cofiltered category is dual to that of a [[filtered category]]. We refer to the latter page for the general theory; here we simply spell out a few things explicitly. 

\section{Details}

\begin{defn} A category $\mathcal{C}$ is _cofiltered_ if its [[opposite category]] $\mathcal{C}^{op}$ is [[filtered category|filtered]]. \end{defn}

\begin{rmk} In other words, a cofiltered category is one in which every finite [[diagram]] in $\mathcal{C}$ has a [[cone]]. \end{rmk}

\begin{rmk} \label{RemarkExplicitDefinition} Explicitly, a cofiltered category $\mathcal{C}$ is one for which the following hold.

1. $\mathcal{C}$ has at least one object.
1. For every pair of objects $c_{1}$ and $c_{2}$ of $\mathcal{C}$, there is an object $c_{3}$ of $\mathcal{C}$ such that there exists an arrow $c_{3} \rightarrow c_{1}$ and there exists an arrow $c_{3} \rightarrow c_{2}$.
1. For every pair of objects $c_{1}$ and $c_{2}$ of $\mathcal{C}$, and every pair of arrows $f, g: c_{1} \rightarrow c_{2}$, there is an arrow $h: c \rightarrow c_{1}$ such that $f \circ h = g \circ h$.

\end{rmk}

\begin{rmk} In the final condition of Remark \ref{RemarkExplicitDefinition}, note that $h$ is not required to satisfy any uniqueness condition with regard to the stated property. In particular, it is not necessarily an equaliser of $f$ and $g$. \end{rmk}

\section{Related concepts}

* [[pro-object]]


[[!redirects cofiltered categories]]
[[!redirects cofiltrant category]]
[[!redirects cofiltrant categories]]
[[!redirects cofiltered diagram]]
[[!redirects cofiltered diagrams]]
[[!redirects co-filtered category]]
[[!redirects co-filtered categories]]
[[!redirects co-filtrant category]]
[[!redirects co-filtrant categories]]
[[!redirects co-filtered diagram]]
[[!redirects co-filtered diagrams]]