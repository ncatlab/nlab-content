\begin{definition}\label{TheAssociatedDoubleCategory}
Given a [[2-category]] $K$ equipped with proarrows according to Def. \ref{TheDefinitionAsA2Functor}, we can construct a [[double category]] having the same [[objects]] as $K$, whose [[vertical 1-cells]] are the arrows, whose [[horizontal 1-cells]] are the proarrows, and whose squares
\begin{tikzcd}
  A
  \arrow[r,  "H", ""{name=U, below}]
  \arrow[d, "f"']
  & C
  \arrow[d, "g"]
  \\
  B
  \arrow[r, "J"', ""{name=D, above}]
  & D
  \arrow[Rightarrow, from=U, to=D, "\alpha"]
\end{tikzcd}
are the [[2-cells]] $H \to J(g,f)$.  
\end{definition}

\begin{remark}

Dually, the 2-cells can be also represented as [[string diagram|string diagrams]] ([Myers 2016](#Myers16)).

\begin{tikzpicture}[scale=2, >=latex]
  \usetikzlibrary{decorations.markings}
\tikzset{mid->/.style={
  decoration={markings, mark=at position 0.6 with {\arrow[scale=1.5]{>}}},
  postaction={decorate}
}}

  % Quadrant fills (centered at origin)
  \fill[blue!15]   (-1,0) rectangle (0,1);
  \fill[teal!20]   (0,0) rectangle (1,1);
  \fill[orange!20] (-1,-1) rectangle (0,0);
  \fill[violet!15] (0,-1) rectangle (1,0);

  % Border
  \draw[gray] (-1,-1) rectangle (1,1);

  % Central node
  \node[circle,draw,fill=white,inner sep=1.5pt] at (0,0) (alpha) {$\alpha$};

  % Arrows
  \draw[line width=0.6pt] (-1,0) -- (alpha);
  \draw[line width=0.6pt] (alpha) -- (1,0);
  \draw[mid->, line width=0.6pt] (alpha) -- (0,-1);
  \draw[mid->, line width=0.6pt] (0,1) -- (alpha);

  % Labels
  \node[left]  at (-1,0) {$H$};
  \node[right] at (1,0)  {$J$};
  \node[above] at (0,1)  {$f$};
  \node[below] at (0,-1) {$g$};
  \node at (-0.5, 0.5) {$A$};
  \node at ( 0.5, 0.5) {$B$};
  \node at (-0.5,-0.5) {$C$};
  \node at ( 0.5,-0.5) {$D$};
\end{tikzpicture}
\end{remark}

***



\begin{lemma}\label{CentralLemma}
There is a [[natural bijection]] between squares of the form

<table>
<tr>
<td style="border: none;">
\begin{tikzcd}
  A_0
  \arrow[r,  "H", ""{name=U, below, yshift=-10pt}]
  \arrow[d, "f_1"']
  & B_0
  \arrow[d, "g_1"]
  \\
  A_1
  \arrow[d, "f_2"']
  & B_1
  \arrow[d, "g_2"]
  \\
  A_2
  \arrow[d, "f_3"']
   & B_2
 \arrow[d, "g_3"]
  \\
  A_3
 \arrow[r, "J"', ""{name=D, above, yshift=10pt}]
  & B_3
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
<td style="border: none;">
≅
</td>
<td style="border: none;">
\begin{tikzcd}
  A_1
  \arrow[r, "{A_1(f_1, 1)}"]
  \arrow[d, "f_2"']
  & A_0
  \arrow[r,  "H", ""{name=U, below}]
  & B_0
  \arrow[r, "{B_1(1, g_1)}"]
  & B_1
  \arrow[d, "g_2"]
  \\
  A_2
  \arrow[r, "{A_3(1, f_3)}"']
  & A_3
 \arrow[r, "J"', ""{name=D, above}]
  & B_3
  \arrow[r, "{B_3(g_3, 1)}"']
  & B_2
  \arrow[Rightarrow, from=U, to=D]
\end{tikzcd}
</td>
</tr>
</table>

\end{lemma}

Illustrated in terms of brane diagrams, this bijection is often called the spider lemma

\begin{tikzpicture}[scale=2.5, >=latex]
  \usetikzlibrary{decorations.markings}

  % color definitions
  \colorlet{colorA0}{red!20}
  \colorlet{colorA1}{orange!30}
  \colorlet{colorA2}{yellow!40}
  \colorlet{colorA3}{green!25}
  \colorlet{colorB0}{cyan!25}
  \colorlet{colorB1}{violet!20}
  \colorlet{colorB2}{red!10}
  \colorlet{colorB3}{green!15}

  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.55 with {\arrow[scale=1.5]{>}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.55 with {\arrowreversed[scale=1.5]{>}}},
      postaction={decorate}
    }
  }

% --- LEFT SQUARE ---
  \fill[colorA0] (-1,1) -- (-0.6,1) to[out=270, in=130] (0,0) to[out=180, in=0] (-1,0) -- cycle;
  \fill[colorA1] (-0.6,1) to[out=270, in=130] (0,0) to[out=90, in=270] (0,1) -- cycle;
  \fill[colorA2] (0,1) to[out=270, in=90] (0,0) to[out=50, in=270] (0.6,1) -- cycle;
  \fill[colorA3] (0.6,1) to[out=270, in=50] (0,0) to[out=0, in=180] (1,0) -- (1,1) -- cycle;
  \fill[colorB0] (-1,-1) -- (-1,0) to[out=0, in=180] (0,0) to[out=230, in=90] (-0.6,-1) -- cycle;
  \fill[colorB1] (-0.6,-1) to[out=90, in=230] (0,0) to[out=270, in=90] (0,-1) -- cycle;
  \fill[colorB2] (0,-1) to[out=90, in=270] (0,0) to[out=310, in=90] (0.6,-1) -- cycle;
  \fill[colorB3] (0.6,-1) to[out=90, in=310] (0,0) to[out=0, in=180] (1,0) -- (1,-1) -- cycle;

  \draw[gray] (-1,-1) rectangle (1,1);
  \draw[mid->] (-0.6, 1) to[out=270, in=130] (0,0);
  \draw[mid->] ( 0,   1) to[out=270, in=90]  (0,0);
  \draw[mid->] ( 0.6, 1) to[out=270, in=50]  (0,0);
  \draw[mid->] (0,0) to[out=230, in=90] (-0.6,-1);
  \draw[mid->] (0,0) to[out=270, in=90] ( 0,  -1);
  \draw[mid->] (0,0) to[out=310, in=90] ( 0.6,-1);
  \draw (-1,0) -- (0,0);
  \draw (0,0)  -- (1,0);

  \node[circle, draw, fill=white, inner sep=3pt] at (0,0) {};

  \node[above] at (-0.6, 1) {$f_1$};
  \node[above] at ( 0,   1) {$f_2$};
  \node[above] at ( 0.6, 1) {$f_3$};
  \node[below] at (-0.6,-1) {$g_1$};
  \node[below] at ( 0,  -1) {$g_2$};
  \node[below] at ( 0.6,-1) {$g_3$};
  \node[left]  at (-1,   0) {$H$};
  \node[right] at ( 1,   0) {$J$};
  \node at (-0.75, 0.75) {$A_0$};
  \node at (-0.2,  0.75) {$A_1$};
  \node at ( 0.2,  0.75) {$A_2$};
  \node at ( 0.75, 0.75) {$A_3$};
  \node at (-0.75,-0.75) {$B_0$};
  \node at (-0.2, -0.75) {$B_1$};
  \node at ( 0.2, -0.75) {$B_2$};
  \node at ( 0.75,-0.75) {$B_3$};

  \node at (1.7, 0) {$\cong$};

  % --- RIGHT SQUARE ---
  \begin{scope}[xshift=4cm]

    \fill[colorA1] (-1,1) -- (0,1) to[out=270, in=90] (0,0) to[out=140, in=0] (-1,0.6) -- cycle;
    \fill[colorA0] (-1,0) -- (-1,0.6) to[out=0, in=140] (0,0) to[out=180, in=0] (-1,0) -- cycle;
    \fill[colorA2] (0,1) -- (1,1) -- (1,0.6) to[out=180, in=40] (0,0) to[out=90, in=270] (0,1) -- cycle;
    \fill[colorA3] (0,0) to[out=40, in=180] (1,0.6) -- (1,0) to[out=180, in=0] (0,0) -- cycle;
    \fill[colorB0] (-1,0) to[out=0, in=180] (0,0) to[out=220, in=0] (-1,-0.6) -- cycle;
    \fill[colorB1] (-1,-1) -- (0,-1) to[out=90, in=270] (0,0) to[out=220, in=0] (-1,-0.6) -- cycle;
    \fill[colorB3] (0,0) to[out=320, in=180] (1,-0.6) -- (1,0) to[out=180, in=0] (0,0) -- cycle;
    \fill[colorB2] (0,-1) -- (1,-1) -- (1,-0.6) to[out=180, in=320] (0,0) to[out=270, in=90] (0,-1) -- cycle;

    \draw[gray] (-1,-1) rectangle (1,1);

    \draw[mid->] (0, 1) to[out=270, in=90]  (0,0);
    \draw[mid->] (0,0)  to[out=270, in=90]  (0,-1);
    \draw[mid->] (-1,  0.6) to[out=0, in=140] (0,0);
    \draw        (-1,  0)   to[out=0, in=180]  (0,0);
    \draw[mid<-] (-1, -0.6) to[out=0, in=220] (0,0);
    \draw[mid<-] (0,0) to[out=40,  in=180] (1,  0.6);
    \draw        (0,0) to[out=0,   in=180]  (1,  0);
    \draw[mid->] (0,0) to[out=320, in=180] (1, -0.6);

    \node[circle, draw, fill=white, inner sep=3pt] at (0,0) {};

    \node[above] at (0,  1) {$f_2$};
    \node[below] at (0, -1) {$g_2$};
    \node[left]  at (-1,  0.6) {$A_1(f_1, 1)$};
    \node[left]  at (-1,  0)   {$H$};
    \node[left]  at (-1, -0.6) {$B_1(1, g_1)$};
    \node[right] at (1,  0.6) {$A_3(1, f_3)$};
    \node[right] at (1,  0)   {$J$};
    \node[right] at (1, -0.6) {$B_3(g_3, 1)$};
    \node at (-0.6,  0.85) {$A_1$};
    \node at (-0.6,  0.3)  {$A_0$};
    \node at ( 0.6,  0.3)  {$A_3$};
    \node at ( 0.6,  0.85) {$A_2$};
    \node at (-0.6, -0.85) {$B_1$};
    \node at (-0.6, -0.3)  {$B_0$};
    \node at ( 0.6, -0.3)  {$B_3$};
    \node at ( 0.6, -0.85) {$B_2$};

  \end{scope}


\end{tikzpicture}

***

$$\displaystyle \underbrace{aaaaaaaaaaaaaaaaa}_{b}$$


| metric | Minkowski | Schwartzschild | Kerr |
|--------|-----------|----------------|------|
| $g_{tt}$ | -1 | $-1 + 2 \frac{m}{r}$ | $-1 + 2 \frac{mr}{\rho^2}$ |
| $g_{rr}$ | +1 | $\frac{r}{r - 2m}$ | $\frac{\rho^2}{\triangle}$ |
| $g_{\theta\theta}$ | $r^2$ | $r^2$ | $\rho^2$ |
| $g_{\phi\phi}$ | $r^2 \sin^2(\theta)$ | $r^2 \sin^2(\theta)$ | $(r^2 + a^2 + \frac{2 m r a^2 \sin^2(\theta)}{\rho^2}) \sin^2{\theta}$ |
| $g_{ij}$ $i \neq j$ | all zero | all zero | all zero except $g_{t \phi} = g_{\phi t} = - \frac{2 m r a \sin^2(\theta)}{\rho^2}$ |



* {#Myers16} [[David Jaz Myers]]: _String Diagrams For Double Categories and (Virtual) Equipments_ &lbrack;[arXiv:1612.02762](https://arxiv.org/abs/1612.02762)&rbrack;

