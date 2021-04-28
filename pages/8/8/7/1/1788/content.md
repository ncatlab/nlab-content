
\begin{defn}\label{calBGammaForDiscreteG}
  For $G$ a [[discrete group]] and $(\Gamma,\alpha)$ a $G$-[[equivariant group|equivariant]] [[topological group]] (hence a [[topological group]] equipped with an [[action]] $\alpha$ of $G$ by continuous group [[automorphisms]]), consider the [[topological groupoid]] which is the [[functor groupoid]] from the [[pair groupoid]] of $G$ to the [[delooping groupoid]] of $\Gamma$:

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

\begin{remark}
  This is the groupoid in $G$-spaces which is indicated  oin
\end{remark}

\begin{prop}
  Let $H \subset G$ any [[subgroup]], there is an [[equivalence]] of [[topological groupoids]] between the $H$-[[fixed locus]] of the $G$-groupoid from Def. \ref{calBGammaForDiscreteG} and

1. for trivial $\alpha$: the [[functor groupoid]] between the [[delooping groupoids]] of $G$ and $\Gamma$:

   $$
     \big(
       \mathcal{B}\Gamma
     \big)^H
     \;\;
     \simeq
     \;\;
     Groupoids(TopSpaces)
     \big(
       G \rightrightarrows \ast,
       \,,
       \Gamma \rightrightarrows \ast
     \big)
   $$

1. for general $\alpha$: the [[action groupoid]] of the [[conjugation action]] of $\Gamma \overset{\gamma \mapsto (\gamma,e)}{\hookrightarrow} \Gamma \rtimes_\alpha G$ on [[group homomorphisms]] $\phi \colon G \to \Gamma \rtimes_\alpha G$ which are [[sections]] ($pr_2 \circ \phi = id_G$) of $pr_2 \colon \Gamma \rtimes_\alpha G \to G$:

   $$
     \big(
       \mathcal{B}\Gamma
     \big)^H
     \;\;
     \simeq
     \;\;
     \Big(
       Groups(TopSpaces)_{/G}
       \big(
         G, \, \Gamma \rtimes_\alpha G
       \big)
     \Big)
     \sslash
     \Gamma
     \,.
   $$

\end{prop}


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

