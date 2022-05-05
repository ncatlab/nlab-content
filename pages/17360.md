# Contents
* table of contents
{: toc}

## Definition

We shall make use of notions introduced at [[cubical set]], and of the notation of this page.

\begin{defn} A [[cubical Kan complex]] is a [[cubical set]] $X$ equipped with the following structure: for every integer $n \geq 1$, every integer $1 \leq i \leq n$, every integer $0 \leq \epsilon \leq 1$, and every morphism $f : \sqcap^{n,i,\epsilon} \rightarrow X$ of cubical sets, there is a morphism $g : \square^{n} \rightarrow X$ of cubical sets such that the following diagram in $\mathsf{Set}^{\square^{op}}$ commutes. 

$$
   \array{
      \sqcap^{n,i,\epsilon}                         &                                            & \\
      \mathllap{i_{i,\epsilon}} \downarrow  & \overset{f}{\searrow}    & \\
      \square^{n}                        & \underset{g}{\rightarrow} & X
   }
$$
\end{defn}

## Homotopy groups

Cubical Kan complexes admit a notion of homotopy group. The theory of these homotopy groups can be developed analogously to the theory of homotopy groups of a topological space. See [[homotopy groups of a cubical Kan complex]].

[[!redirects cubical kan complex]]
