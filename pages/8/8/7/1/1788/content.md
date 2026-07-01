> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.


***


\linebreak

\linebreak


Let $A$ be a ring. Its [[maximal spectrum]], denoted $Spm A$ in EGA (and sometimes $Spec_m A$ by some authors), is the set of the maximal ideals of $A$. As a subset of the topological space $Spec A$, it inherits a topology. The structure sheaf on $Spm A$ is $\mathcal{O}_{Spm A}\coloneqq i^{-1}\mathcal{O}_{Spec A}$, where $i\colon Spm A\hookrightarrow Spec A$ is the inclusion. An *affine ultra-scheme* is a locally ringed space $X$ isomorphic to $(Spm A,\mathcal{O}_{Spm A})$, for some [[Jacobson ring]] $A$ (one also says that $X$ is *ultra-affine*). An **ultra-scheme** is a locally ringed space that has a cover by ultra-affine open subsets.

The mutual quasi-inverse functors that give the equivalence are the following. The functor to the left sends a Jacobson scheme $X$ and sends it to its subset of closed points $X_0$ with the restriction topology and structure sheaf $\mathcal{O}_{X_0}\coloneqq i^{-1}\mathcal{O}_X$, where $i\colon X_0\hookrightarrow X$ is the inclusion. The functor to the right sends an ultra-scheme $U$ to its [[sober topological space|sobrification]] $SU$, with structure sheaf $\mathcal{O}_{SU}\coloneqq i_*\mathcal{O}_U$, where $i:U\to SU$ is the canonical morphism.

* Mark Haiman, *[Varieties as Schemes](https://math.berkeley.edu/~mhaiman/math256-fall18-spring19/varieties-as-schemes-v2.pdf)*

$$
  \left(
  \begin{matrix}
    A & B 
    \\
    0 & C
  \end{matrix}
  \right)
  \left(
  \begin{matrix}
    A^{-1}
    & 
    - A^{-1} B C^{-1}
    \\
    0 & C^{-1}
  \end{matrix}
  \right)
  =
  \begin{matrix}
    1 & 
    \\
  \end{matrix}
$$

\begin{conjecture}
Test conjecture. 
\end{conjecture}


[[Notation]]