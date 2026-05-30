> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.

***

\linebreak




For $C \subset X$ a [[compact subset]], write $cof(X\setminus C \to X)$ for the result of collapsing its [[complement]]. 

Let $X$ be a [[locally compact topological space]] with [[one-point compactification]] $X_{cpt}$. Then we have a canonical [[homeomorphism]]
$$
  cof\big(
    X_{cpt} \setminus C
    \to 
    X_{cpt}
  \big)
  \simeq
  cof\big(
    X \setminus C 
    \to 
    X
  \big)
$$
and hence a system of comparison maps, natural in $C$, of the form:
\[
  \label
  {CollapsingComplementOfCompactinOnePointCompactification}
  X_{cpt} 
    \longrightarrow
  cof(X \setminus C \to X)
  \mathrlap{\,.}
\]

For a [[pointed topological space]] $A$, the *compactly supported mapping space* from $X$ to $A$ is the following [[colimit]] of [[pointed mapping spaces]]:
$$
  Map^c(X,A)
  \colon
  \underset{\underset{C}{\longrightarrow}}{\lim}
  Map\big(
    cof(X \setminus C \to X)
    ,
    A
  \big)
  \mathrlap{\,.}
$$

By (eq:CollapsingComplementOfCompactinOnePointCompactification) this has a canonical comparison map to the [[pointed mapping space]] out of the [[one-point compactification]]:

\[
  \label{ComparisonMapFromCompactToPointedMappingSpace}
  Map^c(X,A)
  \longrightarrow
  Map^\ast\big(
    X_{cpt} , A
  \big)
\]

\begin{proposition}
  A sufficient condition for the comparison map (eq:ComparisonMapFromCompactToPointedMappingSpace) to be a [[weak homotopy equivalence]] is that

* $X$ is a [[manifold]] which is finitary in that it is the [[complement]] of some [[faces]] ([[codimension]]=1 [[stratified space|strata]]) of a [[compact topological space|compact]] [[manifold with corners]].

\end{proposition}

---


$\esh$



$$
  J 
    \;=\;
    \sum_i f_i \theta_i 
      + 
    \sum_j g_j d \theta_j 
    f_i, g_j \in C^\infty(X)
  \,.
$$


\begin{xymatrix}
Q B \ar[d] \ar[r] & Q A \sqcup Q B \ar[d] \ar[r] & A \sqcup Q B \ar[d]\cr
  B        \ar[r] & Q A \sqcup   B        \ar[r] & A \sqcup   B       \cr
\end{xymatrix}