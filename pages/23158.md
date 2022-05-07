

### In terms of lifting properties
 {#SeparationAxiomInTermsOfLiftingProperties}


The [[separation conditions]] $T_0$ to $T_4$ may equivalently be understood as [[lifting properties]] against certain maps of [[finite topological spaces]]. 

This is discussed at *[[separation axioms in terms of lifting properties]]*, to which we refer for further details. Here we just briefly indicate the corresponding lifting diagrams.

In the following diagrams, the relevant [[finite topological spaces]] are indicated explicitly by illustration of their [[underlying]] point set and their [[open subsets]]:

* points (elements) are denoted by $\bullet$ with subscripts indicating where the points map to; 

* boxes are put around [[open subsets]], 

* an arrow $\bullet_u \to \bullet_c$  means that $\bullet_c$ is in the [[topological closure]] of $\bullet_u$. 


In the lifting diagrams for $T_2-T_4$ below, the solid arrow out of the given [[topological space]] $X$ is a [[map]] that  determines (classifies) a decomposition of $X$  into a [[union]] of [[subsets]] with properties indicated by the picture of the finite space.  

Notice that the diagrams for $T_2$-$T_4$ below do not in themselves imply [[T1|$T_1$]].


\begin{proposition}
**(Lifting property encoding $T_0$)**
\linebreak
The following [[lifting property]] in [[Top]] equivalently encodes the [[separation axiom]] [[T0|$T_0$]]:

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

\end{proposition}

\begin{proposition}
**(Lifting property encoding $T_1$)**
\linebreak
The following [[lifting property]] in [[Top]] equivalently encodes the [[separation axiom]] [[T1|$T_1$]]:


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
\end{proposition}


\begin{proposition}
**(Lifting property encoding $T_2$)**
\linebreak
The following [[lifting property]] in [[Top]] equivalently encodes the [[separation axiom]] [[T2|$T_2$]]:


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
\end{proposition}


\begin{proposition}
**(Lifting property encoding $T_3$)**
\linebreak
The following [[lifting property]] in [[Top]] equivalently encodes the [[separation axiom]] [[T3|$T_3$]]:


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
\end{proposition}

\begin{proposition}
**(Lifting property encoding $T_4$)**
\linebreak
The following [[lifting property]] in [[Top]] equivalently encodes the [[separation axiom]] [[T4|$T_4$]]:

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
\end{proposition}


