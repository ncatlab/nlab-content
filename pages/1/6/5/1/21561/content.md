\tableofcontents

\section{Idea} 

A _equifibration_ or _equiv-fibration_ is a [[categorification]] of the notion of an [[isofibration]] to the setting of [[2-category|2-categories]]. Roughly speaking, a [[2-functor|functor]] $p:E \rightarrow B$ between 2-categories is an equifibration if equivalences in $B$ can be 'lifted' to equivalences in $E$. However, there are some subtleties to the precise definition, as will be discussed below. 

\section{Explicit definition}

The following works for both weak and strict 2-categories and weak and strict 2-functors. 

\begin{defn} \label{DefinitionEquifibration} A _equifibration_ is a [[2-functor|functor]] $p: E \rightarrow B$ between [[2-category|2-categories]] such that, for every object $e$ of $E$, and every 1-arrow $f: p(e) \rightarrow b$ of $B$ which is an [[equivalence]], the following hold.

1. There is an object $e'$ of $E$ and an equivalence $g: e \rightarrow e'$ in $E$ such that $p(g) = f$.
1. For every 1-arrow $h: e \rightarrow e'$ of $E$ and every [[2-isomorphism]] $\phi: f \rightarrow p(h)$ in $B$, there is a 2-isomorphism $\psi: g \rightarrow h$ in $E$ such that $p(\psi) = \phi$.    

\end{defn} 

\begin{rmk} \label{RemarkFirstConditionInLackFibrationAsLiftingCondition} Let $Q$ be the [[free-standing equivalence]]. Then condition 1. in Definition \ref{DefinitionEquifibration} is equivalent to saying that for every (strictly!) commutative diagram of 1-arrows

\begin{tikzcd}
1 \ar[r, "e"] \ar[d, swap, "0"] & E \ar[d, "p"] \\
Q \ar[r, swap, "f"] & B
\end{tikzcd}

in $\mathsf{2-Cat}$, the [[2Cat|2-category of 2-categories]], there is a functor $l: Q \rightarrow E$ such that the following diagram of 1-arrows in $\mathsf{2-Cat}$ (strictly!) commutes. 

\begin{tikzcd}
1 \ar[r, "e"] \ar[d, swap, "0"] & E \ar[d, "p"] \\
Q \ar[r, swap, "f"] \ar[ur, "l"] & B
\end{tikzcd}

The same is true if $Q$ is the [[free-standing adjoint equivalence]], due to the fact that any equivalence can be improved to an [[adjoint equivalence]].

\end{rmk}

\begin{rmk} Remark \ref{RemarkFirstConditionInLackFibrationAsLiftingCondition} can be compared with the definition of an [[isofibration]] of 1-categories as expressed by a lifting condition: the condition is exactly the same, with the [[free-standing isomorphism]] replaced by the [[free-standing equivalence]].   \end{rmk}

\begin{rmk} Let us explore the second condition in Definition \ref{DefinitionEquifibration} a little. Note that any 1-arrow which is 2-isomorphic to an equivalence is itself an equivalence. Thus $p(h)$ is an equivalence, and condition 1. then ensures that $p(h)$ lifts to an equivalence $g'$ in $E$ such that $p\left(g'\right) = p(h)$. Condition 2. expresses that $g'$ must be 2-isomorphic to $h$. This implies in particular that $h$ is an equivalence.

Putting everything together, condition 2. is equivalent to: any 1-arrow of $E$ which maps to $f$ under $p$ up to 2-isomorphism is an equivalence, and all equivalences of $E$ which map to $f$ under $p$ up to 2-isomorphism are  2-isomorphic to one another, in such a way that, given 1-arrows $g$ and $g'$ of $E$, a 2-isomorphism $\phi_{g}: f \rightarrow p(g)$ in $B$, and a 2-isomorphism $\phi_{g'}:  f \rightarrow p\left(g'\right)$ in $B$, the 2-isomorphism $\psi : g \rightarrow g'$ in $E$ has the property that $p(\psi) = \phi_{g}^{-1} \circ \phi_{g'}$.

\end{rmk}

\section{References}

The following was where efibrations were introduced.

Equifibrations (there called equiv-fibrations) were introduced in:

* [[Stephen Lack]], _A Quillen model structure for 2-categories_, K-Theory 26, No. 2, 171-205 (2002). [Zentralblatt review](https://zbmath.org/?q=an%3A1017.18005) [author's webpage](http://maths.mq.edu.au/~slack/papers/qmc2cat.html) 

However, it contains an error, not pertaining directly to the definition of a equifibration itself, but to obtaining a model structure on the [[2Cat|category of strict 2-categories]] with this definition. The aforementioned error was fixed in the following paper by using the [[free-standing adjoint equivalence]] rather than the free-standing equivalence in the generating acyclic cofibrations.

* [[Stephen Lack]], _A Quillen model structure for bicategories_, K-Theory 33, No. 3, 185-197 (2004). [Zentralblatt review](https://zbmath.org/?q=an%3A1069.18008) [author's webpage](http://maths.mq.edu.au/~slack/papers/qmcbicat.html)

In the paper above, equifibrations were unnamed (and simply referred to as *fibrations*). The term "equifibration" was used in the following paper:

* [[Alexander Campbell]]. _A homotopy coherent cellular nerve for bicategories_, Advances in Mathematics 368 (2020): 107138.

Equifibrations are called **Lack fibrations** in:

* L. Moser, M. Sarazola, P. Verdugo, _A 2Cat-inspired model structure for double categories_, 2020. [arXiv:2004.14233](https://arxiv.org/abs/2004.14233)

[[!redirects equifibrations]]
[[!redirects equiv-fibration]]
[[!redirects equiv-fibrations]]
[[!redirects Lack fibration]]
[[!redirects Lack fibrations]]