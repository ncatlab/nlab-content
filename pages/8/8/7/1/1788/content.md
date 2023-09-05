
$\curvearrowright$

Given [[small categories]] $I$ and $K$, for any [[diagram]] 

$$
  D \,\colon\, I \times K \longrightarrow C
$$ 

in a [[category]] $C$ that admits all necessary [[limits]] and [[colimits]] we have a [[morphism]]


[xxx](https://github.com/CQTS/summer23-homework)

$$
  \big(
  \vert w \rangle
  +
  \langle w \vert
  \big)
  \otimes
  \big(
  \vert w \rangle
  +
  \langle w \vert
  \big)
$$


quantum measurement on density matrices is

\begin{tikzcd}[row sep=-2pt] 
  \mathrm{Q}W
  &&
  \underset{W}{\bigcirc}
  \big(
    1\!\!1
    \oplus
    1\!\!1
  \big)
  \\
  \otimes
  \ar[
    rr,
    "{
      \mathrm{collapse}
    }",
    "{
      \otimes
    }"{description},
    "{
      \mathrm{collapse}
    }"{swap}
  ]
  &&
  \otimes
  \ar[
    rr,
    "{
      \mathrm{pair}
    }"
  ]
  &&
  \underset{W}{\bigcirc}
  \Big(
    \big(
    1\!\!1
    \oplus
    1\!\!1
    \big)
    \otimes
    \big(
    1\!\!1
    \oplus
    1\!\!1
    \big)
  \Big)
  \ar[
    rr,
    "{
      \bigcirc_w \mathrm{ev}
    }"
  ]
  &&
  \underset{W}{\bigcirc}
  1\!\!1
  \\
  \mathrm{Q}W
  &&
  \underset{W}{\bigcirc}
  \big(
    1\!\!1
    \oplus
    1\!\!1
  \big)
\end{tikzcd}

\begin{tikzcd}
  & 
  1\!\!1
  \ar[
    dl,
    "{
       \epsilon^{\mathcal{E}}_{\mathcal{E}(1\!\!1)}
       \circ
       \epsilon^{\mathcal{E}}_{1\!\!1}
    }"{description}
  ]
  \ar[
    dr,
    "{
      \epsilon^{\mathcal{E}}_{\mathcal{E}(1\!\!1)}
    }"
  ]
  \\
  \mathcal{E}\circ\mathcal{E}(1\!\!1)
  \ar[
    rr,
    "{
      \mathrm{join}^{\mathcal{E}}_{1\!\!1}
    }"{swap}
  ]
  &&
  \mathcal{E}(1\!\!1)
\end{tikzcd}


\begin{tikzcd}
  &
  W \times (1\!\!1 \oplus 1\!\!1)
  \ar[dr]
  \ar[dl]
  \\
  W \times I
  \ar[dr]
  &&
  1\!\!1 /\!\!/ \mathbb{Z}_2
  \ar[dl]
  \\
  & 
  \mathbf{B}\mathbb{Z}_2
\end{tikzcd}


* [[Saunders Mac Lane]], pp. 1045 of: *An Algebra of Additive Relations*, Proceedings of the National Academy of Sciences of the United States of America **47** 7 (1961) 1043-1051 &lbrack;[jstor:71127](https://www.jstor.org/stable/71127)&rbrack;

* [[Dieter Puppe]], §1 in *Korrespondenzen in abelschen Kategorien*, Mathematische Annalen **148** (1962) 1–30 &lbrack;[doi:10.1007/BF01438388](https://doi.org/10.1007/BF01438388)&rbrack;

