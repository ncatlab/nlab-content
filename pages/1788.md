
\begin{definition}
Given 

* $k$ be a separably closed field,

* $\kappa$ be an uncountable [[strong limit cardinal]]

write

* $Sch^{\leq \kappa}_{/Spec(k)}$ for the category of $\kappa$-small [[schemes]] over $Spec(k)$, 

* $Sch^{\leq \kappa}_{/_{pet} Spec(k)}$ for its [[full subcategory]] of those that are [[pro-étale morphism of schemes|pro-étale]] over $Spec(k)$, 

  [[equivalence of categories|equivalently]] this is the category of $\kappa$-small [[profinite sets]],

both regarded as [[sites]] via the [[pro-étale site|pro-étale topology]] and write

\[
  \label{TheGeometricMorphism}
  Sh\big( Sch^{\leq \kappa}_{/Spec(k)}\big) 
  \underoverset{\underset{i_\ast}{\longrightarrow}}{\overset{i^\ast}{\longleftarrow}}{\;\; \bot \;\;} 
  Sh\big( Sch^{\leq \kappa}_{/Spec(k)}\big) 
\]

for the canonical [[geometric morphism]].
\end{definition}

\begin{remark}
\label{TerminologyOfCondensedSets}
  The [[base topos]] in (eq:TheGeometricMorphism) is equivalently called the category of $\kappa$-*[[condensed sets]]*.
\end{remark}

The following seems to be claimed:
\begin{prop}
  The geometric morphism (eq:TheGeometricMorphism) has the following properties:

* $i^\ast$ is [[fully faithful functor|fully faithful]];

* $i_\ast$ is a [[left adjoint]]

and

* $i^\ast$ is a [[right adjoint]].

\end{prop}
The first two claims are fairly standard, the last one would make the topos of pro-étale schemes be [[locally connected topos|locally connected]] and hence *almost* [[cohesive topos|cohesive]] over $\kappa$-[[condensed sets]] (by Rem. \ref{TerminologyOfCondensedSets}).

# Horizontal Composition

Would be nice if someone could put this into the articles for [[Godement product]] and [[horizontal composition]]. Spam detection won't let me.


\begin{tikzcd}[column sep=small]
\textbf{A}
 \arrow[to=1-5, bend left=50]{r}[name=F1]{F_1}
 \arrow[to=1-5, bend right=50]{r}[name=G1,label=below:$\scriptstyle G_1$]{}
 \arrow[phantom,Rightarrow,to path={(F1) -- node[] {$\big\Downarrow\normalsize\alpha$} (G1)}]{}
 &&&& \textbf{B}
 \arrow[to=1-9, bend left=50]{r}[name=F2]{F_2}
 \arrow[to=1-9, bend right=50]{r}[name=G2,label=below:$\scriptstyle G_2$]{}
 \arrow[phantom,Rightarrow,to path={(F2) -- node[] {$\big\Downarrow\normalsize\beta$} (G2)}]{}
 &&&& \textbf{C}
 \arrow[to=1-10, mapsto]
 & \textbf{A}
 \arrow[to=1-14, bend left=50]{r}[name=F3]{F_2 \circ F_1}
 \arrow[to=1-14, bend right=50]{r}[name=G3,label=below:$\scriptstyle G_2 \circ G_1$]{}
 \arrow[phantom,Rightarrow,to path={(F3) -- node[] {$\big\Downarrow\normalsize\beta\circ\alpha$} (G3)}]{}
 &&&& \textbf{C}
\end{tikzcd}