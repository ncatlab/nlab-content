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

\begin{tikzpicture}[scale=2.5]
  \usetikzlibrary{decorations.markings, arrows.meta, calc}
  \tikzset{
    >=Latex,
    mid->/.style={
      decoration={markings, mark=at position 0.55 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.55 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  
  \colorlet{colorA0}{red!20}
  \colorlet{colorA1}{orange!30}
  \colorlet{colorA2}{yellow!40}
  \colorlet{colorA3}{green!25}
  \colorlet{colorB0}{cyan!25}
  \colorlet{colorB1}{violet!20}
  \colorlet{colorB2}{red!10}
  \colorlet{colorB3}{green!15}

  % --- LEFT SQUARE ---
  % corners
  \coordinate (LTL) at (-1, 1);
  \coordinate (LTR) at ( 1, 1);
  \coordinate (LBL) at (-1,-1);
  \coordinate (LBR) at ( 1,-1);
  % edge midpoints
  \coordinate (LW) at (-1, 0);
  \coordinate (LE) at ( 1, 0);
  % central node
  \coordinate (L) at (0,0);
  % arrow endpoints
  \coordinate (Lf1) at (-0.6, 1);
  \coordinate (Lf2) at ( 0,   1);
  \coordinate (Lf3) at ( 0.6, 1);
  \coordinate (Lg1) at (-0.6,-1);
  \coordinate (Lg2) at ( 0,  -1);
  \coordinate (Lg3) at ( 0.6,-1);

  % fills
  \fill[colorA0] (LTL) -- (Lf1) to[out=270, in=130] (L) to[out=180, in=0] (LW) -- cycle;
  \fill[colorA1] (Lf1) to[out=270, in=130] (L) to[out=90, in=270] (Lf2) -- cycle;
  \fill[colorA2] (Lf2) to[out=270, in=90] (L) to[out=50, in=270] (Lf3) -- cycle;
  \fill[colorA3] (Lf3) to[out=270, in=50] (L) to[out=0, in=180] (LE) -- (LTR) -- cycle;
  \fill[colorB0] (LBL) -- (LW) to[out=0, in=180] (L) to[out=230, in=90] (Lg1) -- cycle;
  \fill[colorB1] (Lg1) to[out=90, in=230] (L) to[out=270, in=90] (Lg2) -- cycle;
  \fill[colorB2] (Lg2) to[out=90, in=270] (L) to[out=310, in=90] (Lg3) -- cycle;
  \fill[colorB3] (Lg3) to[out=90, in=310] (L) to[out=0, in=180] (LE) -- (LBR) -- cycle;

  % border
  \draw[gray] (LBL) rectangle (LTR);

  % arrows
  \draw[mid->] (Lf1) to[out=270, in=130] (L);
  \draw[mid->] (Lf2) to[out=270, in=90]  (L);
  \draw[mid->] (Lf3) to[out=270, in=50]  (L);
  \draw[mid->] (L) to[out=230, in=90] (Lg1);
  \draw[mid->] (L) to[out=270, in=90] (Lg2);
  \draw[mid->] (L) to[out=310, in=90] (Lg3);
  \draw (LW) -- (L);
  \draw (L)  -- (LE);

  % central node
  \node[circle, draw, fill=white, inner sep=3pt] at (L) {};

  % edge labels
  \node[above] at (Lf1) {$f_1$};
  \node[above] at (Lf2) {$f_2$};
  \node[above] at (Lf3) {$f_3$};
  \node[below] at (Lg1) {$g_1$};
  \node[below] at (Lg2) {$g_2$};
  \node[below] at (Lg3) {$g_3$};
  \node[left]  at (LW)  {$H$};
  \node[right] at (LE)  {$J$};

  % area labels
  \node at ($(LTL)!0.5!(Lf1)+(0,-0.25)$) {$A_0$};
  \node at ($(Lf1)!0.5!(Lf2)+(0,-0.25)$) {$A_1$};
  \node at ($(Lf2)!0.5!(Lf3)+(0,-0.25)$) {$A_2$};
  \node at ($(Lf3)!0.5!(LTR)+(0,-0.25)$) {$A_3$};
  \node at ($(LBL)!0.5!(Lg1)+(0, 0.25)$) {$B_0$};
  \node at ($(Lg1)!0.5!(Lg2)+(0, 0.25)$) {$B_1$};
  \node at ($(Lg2)!0.5!(Lg3)+(0, 0.25)$) {$B_2$};
  \node at ($(Lg3)!0.5!(LBR)+(0, 0.25)$) {$B_3$};

  % isomorphism symbol
 \node at (1.7, 0) {$\cong$};
 
  % --- RIGHT SQUARE ---
 \begin{scope}[xshift=4cm]
    % corners
    \coordinate (RTL) at (-1, 1);
    \coordinate (RTR) at ( 1, 1);
    \coordinate (RBL) at (-1,-1);
    \coordinate (RBR) at ( 1,-1);
    % edge midpoints
    \coordinate (RW)  at (-1, 0);
    \coordinate (RE)  at ( 1, 0);
    % central node
    \coordinate (R) at (0,0);
    % arrow endpoints
    \coordinate (Rf2) at ( 0,    1);
    \coordinate (Rg2) at ( 0,   -1);
    \coordinate (RWt) at (-1,  0.6);
    \coordinate (RWb) at (-1, -0.6);
    \coordinate (REt) at ( 1,  0.6);
    \coordinate (REb) at ( 1, -0.6);

    % fills
    \fill[colorA1] (RTL) -- (Rf2) to[out=270, in=90] (R) to[out=140, in=0] (RWt) -- cycle;
    \fill[colorA0] (RW) -- (RWt) to[out=0, in=140] (R) to[out=180, in=0] (RW) -- cycle;
    \fill[colorA2] (Rf2) -- (RTR) -- (REt) to[out=180, in=40] (R) to[out=90, in=270] (Rf2) -- cycle;
    \fill[colorA3] (R) to[out=40, in=180] (REt) -- (RE) to[out=180, in=0] (R) -- cycle;
    \fill[colorB0] (RW) to[out=0, in=180] (R) to[out=220, in=0] (RWb) -- cycle;
    \fill[colorB1] (RBL) -- (Rg2) to[out=90, in=270] (R) to[out=220, in=0] (RWb) -- cycle;
    \fill[colorB3] (R) to[out=320, in=180] (REb) -- (RE) to[out=180, in=0] (R) -- cycle;
    \fill[colorB2] (Rg2) -- (RBR) -- (REb) to[out=180, in=320] (R) to[out=270, in=90] (Rg2) -- cycle;

    % border
    \draw[gray] (RBL) rectangle (RTR);

    % arrows
    \draw[mid->] (Rf2) to[out=270, in=90]  (R);
    \draw[mid->] (R)   to[out=270, in=90]  (Rg2);
    \draw[mid->] (RWt) to[out=0, in=140] (R);
    \draw        (RW)  to[out=0, in=180]  (R);
    \draw[mid<-] (RWb) to[out=0, in=220] (R);
    \draw[mid<-] (R) to[out=40,  in=180] (REt);
    \draw        (R) to[out=0,   in=180]  (RE);
    \draw[mid->] (R) to[out=320, in=180] (REb);

    % central node
    \node[circle, draw, fill=white, inner sep=3pt] at (R) {};

    % edge labels
    \node[above] at (Rf2) {$f_2$};
    \node[below] at (Rg2) {$g_2$};
    \node[left]  at (RWt) {$A_1(f_1, 1)$};
    \node[left]  at (RW)  {$H$};
    \node[left]  at (RWb) {$B_1(1, g_1)$};
    \node[right] at (REt) {$A_3(1, f_3)$};
    \node[right] at (RE)  {$J$};
    \node[right] at (REb) {$B_3(g_3, 1)$};

    % area labels
    \node at ($(RTL)!0.5!(RWt)+( 0.3, 0)$) {$A_1$};
    \node at ($(RW)!0.5!(RWt) +( 0.3, 0)$) {$A_0$};
    \node at ($(RTR)!0.5!(REt)+(-0.3, 0)$) {$A_2$};
    \node at ($(RE)!0.5!(REt) +(-0.3, 0)$) {$A_3$};
    \node at ($(RW)!0.5!(RWb) +( 0.3, 0)$) {$B_0$};
    \node at ($(RBL)!0.5!(RWb)+( 0.3, 0)$) {$B_1$};
    \node at ($(RE)!0.5!(REb) +(-0.3, 0)$) {$B_3$};
    \node at ($(RBR)!0.5!(REb)+(-0.3, 0)$) {$B_2$};

  \end{scope}

\end{tikzpicture}


***


| metric | Minkowski | Schwartzschild | Kerr |
|--------|-----------|----------------|------|
| $g_{tt}$ | -1 | $-1 + 2 \frac{m}{r}$ | $-1 + 2 \frac{mr}{\rho^2}$ |
| $g_{rr}$ | +1 | $\frac{r}{r - 2m}$ | $\frac{\rho^2}{\triangle}$ |
| $g_{\theta\theta}$ | $r^2$ | $r^2$ | $\rho^2$ |
| $g_{\phi\phi}$ | $r^2 \sin^2(\theta)$ | $r^2 \sin^2(\theta)$ | $(r^2 + a^2 + \frac{2 m r a^2 \sin^2(\theta)}{\rho^2}) \sin^2{\theta}$ |
| $g_{ij}$ $i \neq j$ | all zero | all zero | all zero except $g_{t \phi} = g_{\phi t} = - \frac{2 m r a \sin^2(\theta)}{\rho^2}$ |



* {#Myers16} [[David Jaz Myers]]: _String Diagrams For Double Categories and (Virtual) Equipments_ &lbrack;[arXiv:1612.02762](https://arxiv.org/abs/1612.02762)&rbrack;

