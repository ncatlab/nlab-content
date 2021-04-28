
\begin{defn}
  For $G$ a [[discrete group]] and $(\Gamma,\alpha)$ a $G$-[[equivariant group|equivariant]] [[topological group]] (hence a [[topological group]] equipped with an [[action]] $\alpha$ of $G$ by continuous [[group automorphisms]]), consider the [[topological groupoid]] which is the [[functor groupoid]] from the [[pair groupoid]] of $G$ to the [[delooping groupoid]] of $\Gamma$:

\[
  \label{HomGroupoidFromPairGroupoidOfGToDeloopingGroupoidOfGamma}
  \mathcal{B}\Gamma
  \;\coloneqq\;
  Groupoids(TopSpaces)
  \big(
    G \times G 
      \underoverset{pr_2}{pr_1}{\rightrightarrows}
    G,
    \;
    \Gamma \rightrightarrows \ast
  \big)
\]

but regarded as an [[internal groupoid]] in [[topological G-spaces]] 

$$
  \mathcal{B}\Gamma
  \;\in\;
  Groupoids
  \big(
    G Actions(TopologicalSpaces)
  \big)
$$

by equipping it with the $G$-[[group action|action]] given on [[functors]] $F$ and [[natural transformations]] $\eta$ in (eq:HomGroupoidFromPairGroupoidOfGToDeloopingGroupoidOfGamma) by:

$$
  (g \cdot F)
  (g_1, g_2)  
  \;\coloneqq\;
  \alpha(g)
  \big(
    F(g_1 g, g_2 g)
  \big)
  \,,
  {\phantom{AAA}}
  (g \cdot \eta)
  (g_1)
  \;\coloneqq\;
  \alpha(g)(\eta(g_1))
  \,.
$$

\end{defn}




$$
  \array{
    g h 
    &&
    \ast 
    &\overset{ a_g }{\longrightarrow}&
    \ast
    \\
    \big\downarrow
    &&
    \big\downarrow
    &&    
    \big\downarrow
    {}^{ \mathrlap{ a_{h' h^{-1}} } }
    \\
    g' h'
    &&
    \ast 
    &\overset{ a_{g'} }{\longrightarrow}&
    \ast
  }
$$

\linebreak

$$
  \array{
    g 
    &\overset{}{\longrightarrow}&
    e
    \\  
    \big\downarrow
    &&
    \big\downarrow
    \\
    g' h' h^{-1}
    &\overset{}{\longrightarrow}&
    e
  }
$$

\linebreak


$$
  \array{
    g 
    &\overset{}{\longrightarrow}&
    e
    \\  
    \big\downarrow
    &&
    \big\downarrow
    \\
    g h 
    &\overset{}{\longrightarrow}&
    e
  }
$$

\linebreak



$$
  \array{
    g h 
    &&
    \ast 
    &\overset{ a_g }{\longrightarrow}&
    \ast
    \\
    \big\downarrow
    &&
    \big\downarrow
    &&    
    \big\downarrow
    {}^{ \mathrlap{ a_{h} } }
    \\
    g
    &&
    \ast 
    &\overset{ a_{g} }{\longrightarrow}&
    \ast
  }
$$

\linebreak


$$
  \array{
    g h 
    &\overset{}{\longrightarrow}&
    e
    \\  
    \big\downarrow
    &&
    \big\downarrow
    \\
    h
    &\overset{}{\longrightarrow}&
    e
  }
$$

