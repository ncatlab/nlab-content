
\begin{tikzcd}
  X
  \ar[d, "{\sim}"{xshift=-6pt, yshift=-2pt, sloped}]
  \\
  Y
\end{tikzcd}


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