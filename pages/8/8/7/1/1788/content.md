
# Contents
* table of contents
{: toc}

## Idea

A [[map]] $f$ between [[spaces]] (say, a [[continuous map]] between [[topological spaces]]) _vanishes at infinity_ if $f(x)$ gets arbitrarily close to [[zero]] as $x$ gets sufficiently close to infinity.

For a map $f\colon X \to Y$, we need a notion of being close to $0$ in $Y$, so take $Y$ to be a [[pointed space]]; then getting arbitrarily close to $0$ means entering any [[neighbourhood]] of the basepoint.  We also need a notion of being close to infinity in $X$, so take $X$ to be a [[locally compact Hausdorff space]]; then getting sufficiently close to infinity means entering the [[exterior]] of some [[compact subspace]].  (To interpret 'getting', of course, we may use [[nets]].)  It is likely, however, that further generalisations are possible.


## Definitions

Consider:

* $X$ a [[locally compact Hausdorff space]],

* $A$ a [[pointed topological space|point]] [[topological spaces]], with basepoint to be denoted 

  $0 \in A$,

* $f \,\colon\, X \longrightarrow A$ a [[continuous map]].

\begin{definition}\label{TheDefinition}

The [[map]] $f\colon X \to A$ *vanishes at infinity* if for every [[neighbourhood]] $N$ of the [[basepoint]] $0 \in A$, there is a [[compact subspace]] $K_N$ of $X$ such that for all $x \in Ext_X(K)$ in the [[exterior]] of $K$, we have $f(x) \in N$.

\end{definition}

\begin{remark}
In case $A$ is a pointed [[metric space]] (such as a [[Banach space]], in particular the [[real line]]), then Def. \ref{TheDefinition} is equivalent to:

* For every [[positive number|positive]] [[real number]] $\epsilon$, there is a [[compact subspace]] $K$ of $X$ such that ${\|f(x)\|} \lt \epsilon$ whenever $x$ lies in the [[exterior]] of $K$ in $X$.

Here, ${\|{-}\|}$ denotes the [[distance]] from the basepoint in the metric space, such as the [[norm]] in the case of Banach spaces.

\end{remark}

## Properties 

### Relation to one-point compactification

One way of considering this definition is that one can adjoin to $X$ a point "at infinity", denoted $\infty$, by declaring that the [[open neighborhoods]] of $\infty$ are sets of the form $\{\infty\} \cup Ext(K)$ for $K \subset X$ compact. This is called the [[one-point compactification]], denoted $X^{cpt}$. Then:

\begin{proposition}
\label{CharacterizationViaOnePointCompactification}

A [[continuous function]] $f \colon X \to A$ vanishes at infinity equivalently if it [[extension|extends]] $f$ to a map $X^{cpt} \to A$, continuous at $\infty$ (at least) that sends $\infty$ to $0$ -- thus _literally- "vanishing at $\infty$". 

\end{proposition}


For applications of this equivalence to [[physics]] see:

* at _[[one-point compactification]] -- [Relevance for Monopoles and Instantons](one-point+compactification#RelevanceForMonopolesAndInstantons)_

* at _[Yang-Mills instanton -- SU(2)-instantons from the correct maths to the traditional physics story](Yang-Mills+instanton#FromTheMathsToThePhysicsStory)_.



