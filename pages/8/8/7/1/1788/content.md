

[link]( https://en.wikipedia.org/wiki/Draft:Funding_Sources_for_American_Mathematicians)

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



# Separation axioms as lifting properties

It is easy to see that the definitions of separation axioms $T_0-T_4$ are represented by the following lifting diagrams
involving finite topological spaces. In the pictures above,
boxes are put around open subsets, and 
 an arrow $\bullet_u\to \bullet_c$  means that $\bullet_c$ is in the closure of $\bullet_u$; the indices of $\bullet$ indicate 
 where points are sent by the morphisms. These diagrams for $T_2-T_4$ omit the conditions $T_1$ that points are closed. 



\begin{tikzcd}
[
  column sep={between origins, 40pt},
  row sep={between origins, 40pt}
]
  \mathrm{CoDsc}
  \big(
    \boxed{\{\bullet_0\leftrightarrow \bullet_1\}}
  \big)
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
  \mathrm{Sierp}
  \big(
    \{\boxed{ {\bullet_0} }\rightarrow{\bullet_1} \}
  \big)
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
   \{\bullet_{x=X=y}\}
\end{tikzcd}
\begin{tikzcd}
[
  column sep={between origins, 60pt},
  row sep={between origins, 40pt}
]
  \{\bullet_x\}
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
      \{\overset{\boxed{\bullet_{x=X=U}}}{}\searrow\underset{\bullet_F}{}\}
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
