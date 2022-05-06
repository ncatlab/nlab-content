

Let $G$ be a [[finite group]]. For $H \subset G$ a [[subgroup]], write $W_G H \coloneqq (N_G H) / H $ for its [Weyl group](Weyl+group#in_equivariant_homotopy_theory).


Let 

1. $X$ be a [[G-CW complex]]

   such that for all [[subgroups]] $H \subset G$

   1. the [[fixed point space]] $X^H$ is a $W_G H = (N_G H) / H $-complex, 

      we write $dim\big( X^H\big)$ for its [[dimension]];

   1. $dim(X^H) \geq 1$;

   1. $H^{dim(X^H)}\Big( X^H , \mathbb{Z}\Big) \simeq \mathbb{Z}$ ([[integral cohomology]] of the [[fixed point space]]),

      this implies that the [[action]] of $W_G(H)$ on cohomology induces a [[group homomorphism]]

      $$
        e_{H,X}
        \;\colon\;
        W_G(H) 
          \longrightarrow 
        Aut_{Ab}(\mathbb{Z}) 
          \simeq 
        \mathbb{Z}^\times
      $$

      to be called the _orientation behaviour_ of $H$ on $X$;

1. $Y$ be a [[G-space]]

   such that for all [[subgroups]] $H \subset G$

   1. $Y^H$ is $dim(X^H)$-[[n-connected topological space|connected]];

   1. $\pi_{dim(X^H)}\big( Y^H\big) \simeq \mathbb{Z}$ ([[homotopy groups]] of [[fixed point space]]),

      with the previous point this implies (by the [[Hurewicz theorem]]) that  $H^{dim(X^H)}\Big( Y^H , \mathbb{Z}\Big) \simeq \mathbb{Z}$ and hence orientation behaviour $e_{H,Y} \;\colon\; W_G(H) \to \mathbb{Z}^\times$

   1. $e_{H,X} = e_{H,Y}$.

Choose generators in each $H^{dim(X^H)}\big(X^H, \mathbb{Z} \big) \simeq \mathbb{Z}$ ([[orientations]]) and $H^{dim(X^H)}\big(Y^G, \mathbb{Z} \big) \simeq \mathbb{Z}$ This implies that for each equivariant $f \colon X \to Y$ each $f^H \;\colon\; X^H \to Y^H$ has a well-defined [[degree of a continuous function|degree]] $deg(f^H) \in \mathbb{Z}$.

+-- {: .num_prop}
###### Proposition
**([[equivariant Hopf degree theorem]])**

Under the above assumptions, the fixed-point-wise degree map

$$
  deg
  \;\colon\;
  \pi_0 \mathrm{Maps}\big( X,Y \big)^G
  \hookrightarrow
  \mathbb{Z}^{ Sub(G) }
$$

(from $G$-[[equivariant homotopy theory|equivariant]] [[homotopy classes]] to [[tuples]] of degrees labeled by [[subgroups]]) is an [[injective function|injection]].

Moreover, for each $[f] \in \pi_0 \mathrm{Maps}\big( X,Y \big)^G$ and for each $H \subset G$ 

1. the $H$-degree modulo the [[order of a group|order]] of the [[Weyl group]]

   $$
     deg\left( f^H\right) \,mod\, {\vert W_G(H)\vert}
     \;\in\;
     \mathbb{Z}/{\vert W_G(H)\vert}
   $$

   is fixed by the degrees $deg\big( f^K\big)$ for all $K \gt H$;


1. there exists $f'$ with these specified degrees $deg\big( (f')^H\big) = deg\big( f^H\big)$ for $K \gt H$ and realizing any of the degrees $deg\big( (f')^H\big) \in \mathbb{Z}$ that satisfy the previous constraint.

=--

***

\begin{centre}

\begin{tikzpicture}

\fill (0,0) circle[radius=2em];

\end{tikzpicture}

\end{centre}

An XY-Matrix diagram:

\begin{centre}

\begin{xymatrix}

A \ar[r] \ar[dr] & B^{2} \ar[d] \\ & C

\end{xymatrix}

\end{centre}

\begin{centre}

\begin{xymatrix[font = \large]@C+2pc}

A \rtwocell^f_g{\alpha} & B

\end{xymatrix}

\end{centre}

\begin{centre}

\begin{xymatrix[border = 2pc]}

A \ar@/^2.0pc/[r] \ar@/_2.0pc/[r] & B

\end{xymatrix}

\end{centre}

    <nowiki>
    \begin{tikzpicture}

    \draw (0,0) -- (2,0) -- (2,-2);

    \end{tikzpicture}
    </nowiki>

[[cellular model]]
