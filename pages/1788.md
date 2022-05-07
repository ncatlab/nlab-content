
\linebreak


To warm up, first notice the following two simple examples of [[lifting properties]]:

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

Namely, a [[commuting diagram]] of the outer form is equivalently just the choice of a single point in $Y$ (this being the [[image]] of the bottom map), and the existence of the dashed lift means that any such point has a [[preimage]] through $f$. This is the very definition of [[surjective function|surjectivity]].

\linebreak


Similarly, the property

* *$X \xrightarrow{f} Y$ is an [[injective function]]*.

means equivalently that $f$ has the [[right lifting property]]
against the unique map from the [[discrete space]] with two elements $Dsc(\{0,1\})$

$$
  Opens
  \Big(
    Dsc
    \big( 
      \{0,1\}
    \big)
  \Big)
  \;\;
  \coloneqq
  \;\;
  \Big\{
    \varnothing 
    ,\,
    \{0\}
    ,\,
    \{1\}
    ,\,
    \{0,1\}
  \Big\}
$$

to the [[point space]]:

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

Namely, that such a lift exists means that the two points in the [[image]] of the top map -- which may be any two points $x_1, x_2 \,\in\, X$ (by the nature of the [[discrete topology]]) such that (by [[commuting diagram|commutativity of the diagram]]) their images are equal, $f(x_1) \,=\, f(x_1) \;\in\; Y$ -- must already have been equal themselves. This is the very definition of [[injective function|injectivity]].


\linebreak


Now consider the variant of the previous example where the 2-element set is equipped instead with the [[codiscrete topology]], whose only [[open subsets]] are the [[empty set]] and the set containing both elements

\[
  \label{OpenSubsetsOfTheCodiscreteSpaceOnTwoElements}
  Opens
  \Big(
    CoDsc
   \big(    
      \{0,1\} 
   \big)
  \Big)
  \;\coloneqq\;
  \big\{
    \begin{array}{l}
      \varnothing, \{0,1\}
    \end{array}
  \big\}
  \,.
\]

In terms of this, the property

* *$X$ is a [[T0-space|$T_0$-space]].

means equivalently that its unique map $X \to \ast$ to the [[point space]] has the [[right lifting property]]
against the unique map from the [[codiscrete space]] with two [[elements]] 
to the [[point space]]:

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

Namely, now [[continuous function|continuity]] restricts the top map to be such that neither $x_i \in\; X$ is contained in an [[open subset]] that does not contain the other: For it were, the [[pre-image]] of that open subset were $\{x_i\} \,\subset\, CoDsc\big( \{0,1\} \big)$, which however is *not* open (eq:OpenSubsetsOfTheCodiscreteSpaceOnTwoElements). This means that if $X_1$ is a [[T0-space|$T_0$-space]] then any such top map must be the [[constant function]], and this is equivalent to the existence of a lift in the diagram.

\linebreak


Proceeding in this manner, one sees that the property

* *$X$ is a [[T1-space|$T_1$-space]].

means equivalently that its unique map $X \to \ast$ to the [[point space]] has the [[right lifting property]]
against the unique map from the [[Sierpinski space]] $Sierp$ 

$$
  Set
  \big(
    Sierp
  \big)
  \;\coloneqq\;
  \{0,1\}
  \,,
  \;\;\;\;\;\; 
  Opens
  \big(
    Sierp
  \big)
  \;\coloneqq\;
  \big\{  
    \varnothing 
    ,\,
    \{1\}
    ,\,
    \{0,1\}
  \big\}
$$

to the [[point space]]:

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

Namely, the previous argument applies, but only to the point $0 \in Sierp$, while now $\{1\} \,\subset\, Sierp$ *is* [[open subset|open]]. Therefore the existence of lifts now means that any two points must *both* have an [[open neighbourhhood]] not containing the other, which is the definition of a [[T1-space|$T_1$-space]].



\linebreak

(...)





\linebreak

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



