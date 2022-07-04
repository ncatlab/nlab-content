Write 

* $kTop$ for the category of [[compactly generated topological spaces]];

\begin{assumption}\label{GeneralInputData}
**(general input data)**
\linebreak
Let 

* $G \,\in\, Grp(kTop)$ be *any* [[topological group]],

* $\mathcal{F} \,\subset\,  Sub(G)$ be *any* [[set]] of [[subgroups]] of $G$.

\end{assumption}

\begin{proposition}\label{FProjectiveModelStructureOnGSpaces}
**($\mathcal{F}$-projective model structure on $G$-spaces)**
\linebreak
  In the generality of Assumption \ref{GeneralInputData},
  the category of [[topological G-spaces]] carries the [[mathematical structure|structure]] of a  [[simplicial model category]] $G Act(kTop)_{\mathcal{F} proj}$ whose

* [[hom-objects]] are the [[singular simplicial complexes]] of [[compact-open topology|mapping spaces]]:

  \[
    \label{SimplicialHomComplexBetweenGTopologicalSpaces}
    [X,Y] 
      \,\coloneqq\,
    Sing
    \,
    Map(X,Y)
    \;\;\;
    \in
    \;
    sSet
  \]

* [[weak equivalences]] and [[fibrations]] are $\mathcal{F}$-[[fixed point space]]-wise those of the [[classical model structure on topological spaces]]

* [[cofibrations]] include the relative [[G-CW complexes|$G$-CW complexes]] which are build (only) from [[orbits]] of the form $G/H$ for $H \,\in\, \mathcal{F} \subset Sub(G)$.

\end{proposition}
([Dwyer & Kan 1984, §1.2 and Thm. 2.2](#DwyerKan84))
