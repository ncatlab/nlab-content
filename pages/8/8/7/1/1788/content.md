
\begin{proposition}
  [[internalization|Internal to]] some 
  ambient [[category]] $\mathcal{C}$
  with [[finite limits]], let 

  * $G \,\in\, Grp(\mathcal{C})$ be a [[group object]], 
  * $P \,\in\, G Act(\mathcal{C})$ an [[action object]],
  * $(P \to X) \,\in\, G PsTor(\mathcal{C}_{/X})$ a [[formally principal bundle]].

Then the following are equivalent:

1. $P \to X$ is the $G$-[[quotient]] [[coprojection]];

1. $P \to X$ is an [[effective epimorphism]].


\end{proposition}
\begin{proof}
  The first condition is equivalent to 
  $$
    P \times_X P \rightrightarrows P \to X
  $$
  being a [[coequalizer]], the second to
  $$
    P \times G \rightrightarrows P \to X
  $$
  being a coequalizer. But the pseudo-principality condition 
  says that we have an [[isomorphism]] (the [[shear map]])
  $$
    P \times_X P \simeq P \times G
  $$
  which identifies these two [[diagrams]].
\end{proof}


\begin{tikzcd}
  \mathrm{Grpd}
  \ar[
    rr,
    shift left=26pt,
    "{
      \pi_0
    }"{description}
  ]
  \ar[
    rr,
    "{
      (-)_0
    }"{description}
  ]
  &&
  \mathrm{Set}
  \ar[
    ll,
    shift right=13pt,
    "{
      \mathrm{Disc}
    }"{description}
  ]
  \ar[
    ll,
    shift left=13pt,
    "{
      \mathrm{Codisc}
    }"{description}
  ]
\end{tikzcd}


$$
  Maps
  \big(
    \mathcal{X}
    ,\,
    \mathbf{E}G
  \big)
  \;=\;
  \Big(
  Fnctr
  \big(
    \mathcal{X}
    ,\,
    \mathbf{E}G
  \big)
  \times
  Fnctn
  \big(
    X_0
    ,\,
    G
  \big)
  \rightrightarrows
  Fnctr
  \big(
    \mathcal{X}
    ,\,
    \mathbf{E}G
  \big)
  \Big)
$$

$$
  Fnctr
  \big(
    \mathcal{X}
    ,\,
    \mathbf{E}G
  \big)
  \;\;
  \simeq
  \;\;  
  Fnctr
  \big(
    \mathcal{X}
    ,\,
    \mathbf{B}G
  \big)
  \times
  G^{\pi_0(\mathcal{X})}
$$


