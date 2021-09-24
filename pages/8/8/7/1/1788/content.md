
\linebreak


The property

* *$X \xrightarrow{f} Y$ is a [[surjective function]]*.

means equivalently that $f$ has the [[right lifting property]]
against the unique map from the [[empty space]] to the [[point space]]:

\begin{tikzcd}
[
  column sep={between origins, 40pt}, 
  row sep={between origins, 40pt}
]
  \varnothing 
  \ar[rr]
  \ar[dd]
  &&
  X
  \ar[
    dd,
    "{ f }"
  ]
  \\
  \\
  \ast
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  Y
\end{tikzcd}



\linebreak



The property

* *$X \xrightarrow{f} Y$ is an [[injective function]]*.

means equivalently that $f$ has the [[right lifting property]]
against the unique map from the [[discrete space]] with two elements to the [[point space]]:

\begin{tikzcd}
[
  column sep={between origins, 40pt}, 
  row sep={between origins, 40pt}
]
  \mathrm{Dsc}
  \big( 
    \{0,1\} 
  \big)
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[dd]
  &&
  X
  \ar[
    dd,
    "{ f }"
  ]
  \\
  \\
  \ast
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  Y
\end{tikzcd}



\linebreak


The property

* *$X \xrightarrow{f} Y$ is [[injective function|injective]] on [[connected components]].

means equivalently that $f$ has the [[left lifting property]]
against the unique map from the [[discrete space]] with two elements to the [[point space]]:

\begin{tikzcd}
[
  column sep={between origins, 40pt}, 
  row sep={between origins, 40pt}
]
  X
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[
    dd,
    "{ f }"
  ]
  &&
  \mathrm{Disc}
  \big( 
    \{0,1\} 
  \big)
  \ar[dd]
  \\
  \\
  Y
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \ast
\end{tikzcd}


\linebreak




In particular, the property

* *$X$ is a [[connected space]].

means equivalently that its unique map $X \to \ast$ to the [[point space]] has the [[left lifting property]]
against the unique map from the [[discrete space]] with two elements to the [[point space]]:

\begin{tikzcd}
[
  column sep={between origins, 40pt}, 
  row sep={between origins, 40pt}
]
  X
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[dd]
  &&
  \mathrm{Disc}
  \big( 
    \{0,1\} 
  \big)
  \ar[dd]
  \\
  \\
  \ast
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \ast
\end{tikzcd}



\linebreak


The property

* *$X$ is a [[T0-space|$T_0$-space]].

means equivalently that its unique map $X \to \ast$ to the [[point space]] has the [[right lifting property]]
against the unique map from the [[Sierpinski space]] to the [[point space]]:

\begin{tikzcd}
[
  column sep={between origins, 40pt}, 
  row sep={between origins, 40pt}
]
  \mathrm{Sierp}
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[dd]
  &&
  X
  \ar[dd]
  \\
  \\
  \ast
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \ast
\end{tikzcd}





\linebreak


The property

* *$X$ is a [[T1-space|$T_1$-space]].

means equivalently that its unique map $X \to \ast$ to the [[point space]] has the [[right lifting property]]
against the unique map from the [[codiscrete space]] with two elements to the [[point space]]:

\begin{tikzcd}
[
  column sep={between origins, 40pt}, 
  row sep={between origins, 40pt}
]
  \mathrm{CoDsc}
  \big( 
    \{0,1\} 
  \big)
  \ar[
    rr,
    "{ \forall }"
  ]
  \ar[dd]
  &&
  X
  \ar[dd]
  \\
  \\
  \ast
  \ar[
    rr
  ]
  \ar[
    uurr,
    dashed,
    "{ \exists }"
  ]
  &&
  \ast
\end{tikzcd}


\linebreak

(...)



