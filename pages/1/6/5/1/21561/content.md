

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

\tableofcontents

\section{Idea} 

The notion referred to as _equiv-fibrations_ &lbrack;[Lack 2002](#Lack02)&rbrack; or *equifibrations* &lbrack;[Campbell 2020, Def. 4.1](#Campbell20)&rbrack; (both meant to be short fort *equivalence-fibrations*) or *Lack fibrations* &lbrack;[Moser, Sarazola & Verdugo 2022](#MoserSarazolaVerdugo22)&rbrack;
is a [[categorification]] of that of [[isofibrations]], from [[category theory]] to [[2-category theory]]. Roughly speaking, a [[2-functor]] $p \colon E \rightarrow B$ between [[2-categories]] is an equifibration if [[equivalence in a 2-category|equivalences]] in $B$ can be 'lifted' to equivalences in $E$. However, there are some subtleties to the precise definition, discussed below. 

Beware that there is unrelated terminology of *[[equifibered natural transformation|equifibered]]* [[natural transformations]].

\section{Explicit definition}

The following works for both [[weak 2-category|weak]] and [[strict 2-categories]] and [[weak 2-functor|weak]] and [[strict 2-functors]]. 

\begin{defn} \label{DefinitionEquifibration} A _equifibration_ is a [[2-functor]] $p \colon E \rightarrow B$ between [[2-categories]] such that, for every [[object]] $e$ of $E$, and every [[1-morphism]] $f \colon p(e) \rightarrow b$ of $B$ which is an [[equivalence]], the following hold:

1. There is an [[object]] $e'$ of $E$ and an [[equivalence in a 2-category|equivalence]] $g: e \rightarrow e'$ in $E$ such that $p(g) = f$.

1. For every [[1-morphism]] $h \colon e \rightarrow e'$ of $E$ and every [[2-isomorphism]] $\phi \colon f \rightarrow p(h)$ in $B$, there is a 2-isomorphism $\psi \colon g \rightarrow h$ in $E$ such that $p(\psi) = \phi$.    

\end{defn} 

\begin{rmk} \label{RemarkFirstConditionInLackFibrationAsLiftingCondition} Let $Q$ be the [[free-standing equivalence]]. Then condition (1.) in Definition \ref{DefinitionEquifibration} is equivalent to saying that for every (strictly!) [[commutative diagram]] of 1-morphismd

\begin{tikzcd}
1 \ar[r, "e"] \ar[d, swap, "0"] & E \ar[d, "p"] \\
Q \ar[r, swap, "f"] & B
\end{tikzcd}

in [[2Cat|$\mathsf{2-Cat}$]], the [[2Cat|2-category of 2-categories]], there is a functor $l \colon Q \rightarrow E$ such that the following diagram of 1-morphisns in $\mathsf{2-Cat}$ (strictly!) commutes. 

\begin{tikzcd}
1 \ar[r, "e"] \ar[d, swap, "0"] & E \ar[d, "p"] \\
Q \ar[r, swap, "f"] \ar[ur, "l"] & B
\end{tikzcd}

The same is true if $Q$ is the [[free-standing adjoint equivalence]], due to the fact that any equivalence can be improved to an [[adjoint equivalence]].

\end{rmk}

\begin{rmk} Remark \ref{RemarkFirstConditionInLackFibrationAsLiftingCondition} can be compared with the definition of an [[isofibration]] of [[1-categories]] as expressed by a [[lifting]] condition: the condition is exactly the same, with the [[free-standing isomorphism]] replaced by the [[free-standing equivalence]].   \end{rmk}

\begin{rmk} Let us explore the second condition in Definition \ref{DefinitionEquifibration} a little. Note that any 1-morphism which is 2-isomorphic to an equivalence is itself an equivalence. Thus $p(h)$ is an equivalence, and condition 1. then ensures that $p(h)$ lifts to an equivalence $g'$ in $E$ such that $p\left(g'\right) = p(h)$. Condition 2. expresses that $g'$ must be 2-isomorphic to $h$. This implies in particular that $h$ is an equivalence.

Putting everything together, condition 2. is equivalent to: any 1-arrow of $E$ which maps to $f$ under $p$ up to 2-isomorphism is an equivalence, and all equivalences of $E$ which map to $f$ under $p$ up to 2-isomorphism are  2-isomorphic to one another, in such a way that, given 1-arrows $g$ and $g'$ of $E$, a 2-isomorphism $\phi_{g}: f \rightarrow p(g)$ in $B$, and a 2-isomorphism $\phi_{g'}:  f \rightarrow p\left(g'\right)$ in $B$, the 2-isomorphism $\psi : g \rightarrow g'$ in $E$ has the property that $p(\psi) = \phi_{g}^{-1} \circ \phi_{g'}$.

\end{rmk}


\section{References}



The original article, speaking of *equiv-fibrations*:

* {#Lack02} [[Stephen Lack]], _A Quillen model structure for 2-categories_, K-Theory **26** 2 (2002) 171-205 &lbrack; [author's webpage](http://maths.mq.edu.au/~slack/papers/qmc2cat.html), [zbmath:3A1017.18005](https://zbmath.org/?q=an%3A1017.18005)&rbrack;

Beware that [Lack 2002](#Lack02) contains an error, not pertaining directly to the definition of a equifibration itself, but to obtaining a [[model category]] [[structure]] on the [[2Cat|category of strict 2-categories]] with this definition (cf. *[[canonical model structure on 2-categories]]*). This was fixed in the following paper [Lack 2004](#Lack04) by using the [[free-standing adjoint equivalence]] rather than the free-standing equivalence in the generating acyclic cofibrations:

* {#Lack04} [[Stephen Lack]], _A Quillen model structure for bicategories_, K-Theory **33** 3 (2004) 185-197 &lbrack;[Zentralblatt review](https://zbmath.org/?q=an%3A1069.18008) [author's webpage](http://maths.mq.edu.au/~slack/papers/qmcbicat.html)&rbrack;

In [Lack 2004](#Lack04), equifibrations were unnamed (and simply referred to as *fibrations*). 

The term *equifibrations* is used in:

* {#Campbell20} [[Alexander Campbell]]. _A homotopy coherent cellular nerve for bicategories_, Advances in Mathematics **368** (2020) 107138 &lbrack;[arXiv:1907.01999](https://arxiv.org/abs/1907.01999), [doi;10.1016/j.aim.2020.107138](https://doi.org/10.1016/j.aim.2020.107138)&rbrack;

The term *Lack fibrations* is used in:

* {#MoserSarazolaVerdugo22} [[Lyne Moser]], Maru Sarazola, Paulo Verdugo, _A 2Cat-inspired model structure for double categories_, [[Cahiers]] LXIII-2 **63** 2 (2022) 184-236 &lbrack;[arXiv:2004.14233](https://arxiv.org/abs/2004.14233)&rbrack;

[[!redirects equifibrations]]
[[!redirects equiv-fibration]]
[[!redirects equiv-fibrations]]
[[!redirects Lack fibration]]
[[!redirects Lack fibrations]]