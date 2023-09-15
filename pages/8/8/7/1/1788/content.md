
a coKleisli morphism

$$
  \array{
    S
    &
    \overset{
      \big(
        get
        ,\, 
        \widetilde{put}
      \big)
    }{\longrightarrow}
    &
    V \times [V, S]    
    \\
    s
    &\mapsto&
    \big(
      get(s)
      ,\,
      put(-,s)
    \big)
  }
$$

counitality

$$
  \array{
    S
    &
    \overset{
      \big(
        get
        ,\, 
        \widetilde{put}
      \big)
    }{\longrightarrow}
    &
    V \times [V, S]    
    &
    \overset{\;\; ev \;\;}{\longrightarrow}
    &
    S
    \\
    s 
    &\mapsto&
    \big(
      get(s)
      ,\,
      put(-,s)
    \big)
    &\mapsto&
    put\big(
      get(s)
      ,\,
      s
    \big)
  }
$$


\begin{tikzcd}[  
  column sep=4pt
]
  V \times [V,S]
  \ar[
    rrrrr,
    "{
      \mathrm{dupl}^{ V\mathrm{Sotr} }_S
    }"
  ]
  &[-5pt]
  &&&[-150pt]
  &[-30pt]
  V \times \Big[ 
    V 
    ,\,
    \big[
      V 
      \times 
      [V,S] 
    \big]
  \Big]
  \\
  &
  \big(
    \mathrm{get}(s)
    ,\,
    \mathrm{put}(-,s)
  \big)
  \ar[rr, phantom, "{ \mapsto }"]
  &&
  \Big(
    \mathrm{get}(s)
    ,\,
    v' \mapsto \big(v', \mathrm{put}(-,s)\big) 
  \Big)
  \\
  &&&& 
  \bigg(
    \mathrm{get}(s)
    ,\,
    v'
    \mapsto
    \Big(
      \mathrm{get}\big(\mathrm{put}(v',s)\big)
      ,\,
      \mathrm{put}\big(-, \mathrm{put}(v',s)\big)      
    \Big)
  \bigg)
  \ar[ul, equals]
  \\
  & 
  &&& 
  \\
  & 
  s 
  \ar[rrr, phantom, "{ \mapsto }"]
  \ar[uuu, phantom, "{ \mapsto }"{sloped}]
  &&& 
  \big(
    \mathrm{get}(s)
    ,\,
    v' \mapsto \mathrm{put}(v',s)
  \big)
  \ar[uu, phantom, "{ \mapsto }"{sloped}]
  \\
  S 
  \ar[
    rrrrr,
    "{
      \big(
        \mathrm{get}
        ,\,
        \widetilde{\mathrm{put}}
      \big)
    }"{swap}
  ]
  \ar[
    uuuuu,
    "{
      \big(
        \mathrm{get}
        ,\,
        \widetilde{\mathrm{put}}
      \big)
    }"
  ]
  &&&&&
  V \times [V, S]
  \ar[
    uuuuu,
    "{
      V \times \Big[
        V
        ,\,
        \big(
          \mathrm{get}
          ,\,
          \widetilde{\mathrm{put}}
        \big)       
      \Big]
    }"{swap}
  ]
\end{tikzcd}
