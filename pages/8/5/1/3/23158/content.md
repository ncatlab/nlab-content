The [[separation axioms in terms of lifting properties|following lifting diagrams involving finite topological spaces]]
represent the definitions of separation axioms $T_0-T_4$. 
In the pictures above, 
points are denoted by $\bullet$ with subscripts indicating where the points map to; 
boxes are put around open subsets, and 
an arrow $\bullet_u\to \bullet_c$  means that $\bullet_c$ is in the closure of $\bullet_u$. 
These diagrams for $T_2-T_4$ omit the condition $T_1$ that points are closed. 
In $T_2-T_4$, an arrow from $X$ determines a decomposition of $X$ 
into a union of subsets with properties indicated by the picture
of the finite space.  


\begin{tikzcd}
[
  column sep={between origins, 40pt},
  row sep={between origins, 40pt}
]
    \{\boxed{\bullet_0\leftrightarrow \bullet_1}\}
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[dd]
  &&
  X
  \ar[dd,"{ (T_0) }"]
  \\
  \\
  \bullet_{0=1}
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \bullet
\end{tikzcd}
\begin{tikzcd}
[
  column sep={between origins, 40pt},
  row sep={between origins, 40pt}
] 
\{\boxed{ \overset{\boxed{\bullet_{0}}}{}\searrow\underset{\bullet_1}{} }\}
%    \{\boxed{ \boxed{ {\bullet_0} }\rightarrow{\bullet_1} }\}
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[dd]
  &&
  X
  \ar[dd,"{ (T_1) }"]
  \\
  \\
  \bullet_{0=1}
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \bullet
\end{tikzcd}

\begin{tikzcd}
[
  column sep={between origins, 80pt},
  row sep={between origins, 40pt}
]
  \boxed{\{\boxed{\bullet_x}, \boxed{\bullet_y}\}}
  \ar[
    rr,
    "{ }"
  ]
  \ar[dd, hook, "{ \forall  }"{left}, ,"{ (T_2) }"{right} ]
  &&
  \boxed{
    \overset{
      \boxed{
        \boxed{\bullet_x}
        \;\;
        \,
        \;\;
        \boxed{\bullet_y}}
      }{
        \underset{
           \bullet_X
        }
        {
          \searrow \;\, \swarrow
        }
      }
  }
  \ar[dd]
  \\
  \\
  X
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
   \{\boxed{\bullet_{x=X=y}}\}
\end{tikzcd}
\begin{tikzcd}
[
  column sep={between origins, 60pt},
  row sep={between origins, 40pt}
]
  \{\boxed{\bullet_x} \}
  \ar[dd,"{ \forall }"{left}, "{ (T_3) }"{right}]
  \ar[rr]
  &&
\{
\boxed{
 \boxed{
\overset{\boxed{\bullet_x}}{}
\searrow
\underset{\bullet_X}{} \swarrow
\overset{\boxed{\bullet_U}}{}
}\!\!\!\!\!\!\!
{\,\,\,\,\,\,\searrow\underset{\bullet_F}{} }
}
\}
  \ar[dd]
  \\
  \\
  X
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
      \{\boxed{ \overset{\boxed{\bullet_{x=X=U}}}{}\searrow\underset{\bullet_F}{} }\}
\end{tikzcd}
\begin{tikzcd}
[
  column sep={between origins, 60pt},
  row sep={between origins, 40pt}
]
  \varnothing
  \ar[dd, "{ (T_4) }"{right}]
  \ar[rr]
  &&
\boxed{
\boxed{\underset{\bullet_x}{}\swarrow
\,\,\,\,\,\,\,}
\!\!\!\!\!\!\!\!
\,\,\,\,\,\,\,\,
\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,
\,\,\,\,
\,\,\,\,\,}
\!\!\!\!\!\!\!
\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
\!\!\!\!\!\!\!\!
\!\!\!\!\!\!\!\!
\!\!\!\!
\boxed{
\boxed{
\overset{\boxed{\bullet_u}}{}
\searrow
\underset{\bullet_X}{} \swarrow
\boxed{
\overset{\boxed{\bullet_v}}{}
\!\!\!\!\!\!\!
{\,\,\,\,\,\,\searrow\underset{\bullet_y}{} }
}\!\!\!\!\!\!\!%%%%%%%%
\!\!\!\!\!}
%\,\,\,\,\,\,\,\,\,
\,\,\,\,\,\,\,\,\,}
  \ar[dd]
  \\
  \\
  X
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \{
\boxed{
\underset{\bullet_x}{}{\swarrow}             
\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,\,
%\,\,
%\,\,\,\,\,\,\,
}
\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
%\!\!%\!\!\!\!\!\!\!
\boxed{\overset{\boxed{\bullet_{U=X=V}}}{}
{\searrow}
\underset{\bullet_y}{}
}
\}
\end{tikzcd}
