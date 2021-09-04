

\begin{tikzcd}
    c_X^\ast(W G)
    \ar[rr]
    \ar[
      d,
      "p_X \,\in\, \mathrm{Fib}"
    ]
    &&
    c_Y^\ast(W G)
    \ar[
      d,
      "p_Y \,\in\, \mathrm{Fib}"
    ]
    \ar[rr]
    &&
    W G
    \ar[
      d,
      "\in \mathrm{Fib}"
    ]
    \\
    X
    \ar[
      rr,
      "f"{below}
    ]
    \ar[
      rrrr,
      rounded corners,
      to path={
         -- ([yshift=-7pt]\tikztostart.south)
         --node[below]{\scalebox{.7}{$
               c_Y
             $}} ([yshift=-7pt]\tikztotarget.south)
         -- (\tikztotarget.south)}
    ]
    &&
    Y
    \ar[
      rr,
      "c_Y"{below}
    ]
    &&
    \overline{W}G
\end{tikzcd}



$U(\mathcal{H})$

[[U(ℋ)]]

Let $\phi \;\colon\; G \xrightarrow{\;} \Gamma$ be a [[crossed homomorphism]], hence equivalently a plain group homomorphism
$(\phi(-),\,(-)) \,\colon\, G \xrightarrow{\;} \Gamma \rtimes G$.
Say that another crossed homomorphism $\phi'$ is nearby if it is so as a plain homomorphism $(\phi'(-),(-))$. 

Then the above theorem says that there is an element $(\gamma,\,h) \,\in\, \Gamma \rtimes G$ such that

$$
  \big(
    \phi'(g),\,g
  \big)
  \;\;
  =
  \;\;
  \big(
    \gamma, \, h
  \big)^{-1}
  \cdot
  \big(
    \phi'(g),\,g
  \big)
  \cdot
  \big(
    \gamma, \, h
  \big)
  \,.
$$

In order for such a conjugation to be a crossed conjugation of the original morphism, we need $h = \mathrm{e}$. 

Notice that we know already that $h \in C(G)$ is in the [[center of a group|center]] of $G$, since the projection of both sides of the equation to $G$ must be the identity, by construction of crossed homomorphisms.

Hence the further conjugation of the above equation by $\big(\mathrm{e},\,h^{-1}\big)$ yields:

$$
  \Big(
    \alpha(h^{-1})
    \big(
      \phi'(g),\, g
    \big)
  \Big)
  \;\;
  =
  \;\;
  \big(
    \mathrm{e},\, h 
  \big)
  \cdot
  \big(
    \gamma, \, h
  \big)^{-1}
  \cdot
  \big(
    \phi'(g),\,g
  \big)
  \cdot
  \big(
    \gamma, \, h
  \big)
  \cdot
  \big(
    \mathrm{e},\, h^{-1} 
  \big)
  \,.
$$

Therefore, if the action of $G$ on $\Gamma$ restricts along the inclusion $C(G) \xhookrightarrow{\;} G$ to the [[trivial action]], then

$$
  \big(
    \gamma, \, h
  \big)
  \cdot
  \big(
    \mathrm{e},\, h^{-1} 
  \big)
  \;\;
  =
  \;\;
  \big(
    \gamma, \, \mathrm{e}
  \big)  
$$

corresponds to a crossed conjugation

$$
  \phi'(-) \;=\;  \gamma^{-1} \cdot \phi(-) \cdot \alpha(-)(\gamma)
  \,.
$$

[[CrossedHomomorphismsAsSlicedFunctors210831.jpg:file]]

\begin{tikzcd}
      &&
      \mathbf{B}(\Gamma \rtimes G)
      \ar[
        d,
        "\mathbf{B}\mathrm{pr}_2"
      ]
      \\
      \mathbf{B}G
      \mathrlap{\,.}
      \ar[
        rr,-,
        shift right=1pt
      ]
      \ar[
        rr,-,
        shift left=1pt
      ]
      \ar[
        urr,
        dashed,
        bend left=30,
        "\ "{right, name=s}
      ]
      \ar[
        urr,
        dashed,
        bend right=10,
        "\ "{left, name=t}
      ]
      &&
      \mathbf{B}G
      %
      \ar[
        from=s,
        to=t,
        dashed,
        Rightarrow
      ]
\end{tikzcd}



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

***

\linebreak

- $G$-fixed-wise contractibility of $Maps(\mathbf{E}G,\mathbf{E}\Gamma)$ follows from $G$-equivariant contraction of $\mathbf{E}\Gamma$

- the universal equivariant principal $\infty$-bundle is $\ast \longrightarrow Maps(\mathbf{E}G, \mathbf{B}\Gamma)$ and the point is that the base space is pointed, but no longer pointed connected -- but the universal bundle is still that point inclusion (meaning that all other fibers are empty, as admissible for a formally principal bundle)


\linebreak

***

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


