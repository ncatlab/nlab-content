

\begin{example}\label{GActionsAndGOrbits}
**([[G-sets]] and [[orbits]])**
\linebreak
  Let $G \,\in\, Grp(Set)$ be a [[discrete group]]. Write

* [[G-set|$G Set$]] for its category of [[group actions]] on [[sets]], 

* $G Orbt \xhookrightarrow{\;} G Set$ for its [[orbit category]], the [[full subcategory]] on the [[transitive actions]], hence the [[coset space|sets of cosets]] $G/H$, for [[subgroups]] $H \subset G$.

Since every [[G-set]] $X$ decomposes as a [[disjoint union]] of [[transitive actions]], namely of [[orbits]] of [[elements]] of $X$, this inclusion exhibits $G Set$ as the [[free coproduct completion]] of [[orbit category|G Orbt]].
\end{example}

$$
  B H \to B G
$$

$\simeq$

$$
  H \backslash\!\!\backslash G \sslash G
$$


$$
\{
\boxed{
\boxed{\underset{x}{}\swarrow
\,\,\,\,\,\,\,}
\!\!\!\!\!\!\!\!
\,\,\,\,\,\,\,\,
\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,
}\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
\!\!\!\!\!\!\!\!
\boxed{
 \boxed{
\overset{\boxed{U}}{}
\searrow
\underset{X}{} \swarrow
\overset{\boxed{V}}{}
}\!\!\!\!\!\!\!
{\,\,\,\,\,\,\searrow\underset{y}{} }
}
\}
$$


\begin{tikzcd}[column sep=20pt]
     \mathrm{PSh}(\mathcal{C})_{/y_{\mathcal{C}}(X)}
     \big(
       (y_{\mathcal{C}})_{/X}(U \xrightarrow{\phi} X)
       ,\,
       (E \xrightarrow{p} y_{\mathcal{C}}(X) )
     \big)
     \ar[
       rr
     ]
     \ar[d]
     &&
     \mathrm{PSh}(\mathcal{C})
     \big(
        y_{\mathcal{C}}(U)
        ,\,
        E
     \big)
     \ar[d]
     \\
     \big\{
        y_{\mathcal{C}}(\phi)
     \big\}
     \ar[rr]
     &&
     \mathrm{PSh}(\mathcal{C})
     \big(
        y_{\mathcal{C}}(U)
        ,\,
        y_{\mathcal{C}}(X)
     \big)              
\end{tikzcd}



\begin{prop}
  Given a pair of [[adjoint functors]], $L \dashv R$, if there is any [[natural isomorphism]] $L \circ R \underoverset{\sim}{\phi}{\longrightarrow} id$ then the [[adjunction counit]] is an isomorphism: $L \circ R \underoverset{\epsilon}{\sim}{\longrightarrow} id$.
\end{prop}


$$
  id
  \underoverset
    {\sim}
    {\phi^{-1}}
    {\longrightarrow}
  L \circ R
  \underoverset
    {}
    {L \circ \eta \circ R}
    {\longrightarrow}
  L \circ R \circ L \circ R
  \underoverset
    {\sim}
    {\phi \phi}
    {\longrightarrow}
  id \circ id
    \simeq
  id
$$