\begin{tikzcd}
A \otimes A \otimes N
  \arrow[r, "id_A \otimes \lambda"]
  \arrow[d, "\cdot \otimes id_N"']
& A \otimes N
  \arrow[d, "\lambda"]
\\
A \otimes N
  \arrow[r, "\lambda"]
& N
\end{tikzcd}

\begin{tikzcd}
I \otimes N
  \arrow[rr, "e \otimes id_N"]
  \arrow[dr]
&& A \otimes N
  \arrow[dl, "\lambda"]
\\
& N
\end{tikzcd}

***


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
  \coordinate (NW)  at (-1,  1);
  \coordinate (NE)  at ( 1,  1);
  \coordinate (SW)  at (-1, -1);
  \coordinate (SE)  at ( 1, -1);
  \coordinate (W)   at (-1,  0);
  \coordinate (E)   at ( 1,  0);
  \coordinate (C)   at ( 0,  0);
  \coordinate (NNW) at (-0.6,  1);
  \coordinate (N)   at ( 0,    1);
  \coordinate (NNE) at ( 0.6,  1);
  \coordinate (SSW) at (-0.6, -1);
  \coordinate (S)   at ( 0,   -1);
  \coordinate (SSE) at ( 0.6, -1);

  % fills
  \fill[colorA0] (NW)  -- (NNW) to[out=270, in=130] (C) to[out=180, in=0] (W)   -- cycle;
  \fill[colorA1] (NNW) to[out=270, in=130] (C) to[out=90,  in=270] (N)   -- cycle;
  \fill[colorA2] (N)   to[out=270, in=90]  (C) to[out=50,  in=270] (NNE) -- cycle;
  \fill[colorA3] (NNE) to[out=270, in=50]  (C) to[out=0,   in=180] (E)   -- (NE) -- cycle;
  \fill[colorB0] (SW)  -- (W)   to[out=0,   in=180] (C) to[out=230, in=90]  (SSW) -- cycle;
  \fill[colorB1] (SSW) to[out=90,  in=230] (C) to[out=270, in=90]  (S)   -- cycle;
  \fill[colorB2] (S)   to[out=90,  in=270] (C) to[out=310, in=90]  (SSE) -- cycle;
  \fill[colorB3] (SSE) to[out=90,  in=310] (C) to[out=0,   in=180] (E)   -- (SE) -- cycle;

  % border
  \draw[gray] (SW) rectangle (NE);

  % arrows
  \draw[mid->] (NNW) to[out=270, in=130] (C);
  \draw[mid->] (N)   to[out=270, in=90]  (C);
  \draw[mid->] (NNE) to[out=270, in=50]  (C);
  \draw[mid->] (C) to[out=230, in=90] (SSW);
  \draw[mid->] (C) to[out=270, in=90] (S);
  \draw[mid->] (C) to[out=310, in=90] (SSE);
  \draw (W) -- (C);
  \draw (C) -- (E);

  % central node
  \node[circle, draw, fill=white, inner sep=3pt] at (C) {};

  % edge labels
  \node[above] at (NNW) {$f_1$};
  \node[above] at (N)   {$f_2$};
  \node[above] at (NNE) {$f_3$};
  \node[below] at (SSW) {$g_1$};
  \node[below] at (S)   {$g_2$};
  \node[below] at (SSE) {$g_3$};
  \node[left]  at (W)   {$H$};
  \node[right] at (E)   {$J$};

  % area labels
  \node at ($(NW)!0.5!(NNW)+(0,-0.25)$) {$A_0$};
  \node at ($(NNW)!0.5!(N) +(0,-0.25)$) {$A_1$};
  \node at ($(N)!0.5!(NNE) +(0,-0.25)$) {$A_2$};
  \node at ($(NNE)!0.5!(NE)+(0,-0.25)$) {$A_3$};
  \node at ($(SW)!0.5!(SSW)+(0, 0.25)$) {$B_0$};
  \node at ($(SSW)!0.5!(S) +(0, 0.25)$) {$B_1$};
  \node at ($(S)!0.5!(SSE) +(0, 0.25)$) {$B_2$};
  \node at ($(SSE)!0.5!(SE)+(0, 0.25)$) {$B_3$};

  % isomorphism symbol
  \node at (1.7, 0) {$\cong$};

  % --- RIGHT SQUARE ---
  \begin{scope}[xshift=4cm]

    \coordinate (NW)  at (-1,  1);
    \coordinate (NE)  at ( 1,  1);
    \coordinate (SW)  at (-1, -1);
    \coordinate (SE)  at ( 1, -1);
    \coordinate (W)   at (-1,  0);
    \coordinate (E)   at ( 1,  0);
    \coordinate (C)   at ( 0,  0);
    \coordinate (N)   at ( 0,  1);
    \coordinate (S)   at ( 0, -1);
    \coordinate (WNW) at (-1,  0.6);
    \coordinate (WSW) at (-1, -0.6);
    \coordinate (ENE) at ( 1,  0.6);
    \coordinate (ESE) at ( 1, -0.6);

    % fills
    \fill[colorA1] (NW)  -- (N)   to[out=270, in=90]  (C) to[out=140, in=0] (WNW) -- cycle;
    \fill[colorA0] (W)   -- (WNW) to[out=0,   in=140] (C) to[out=180, in=0] (W)   -- cycle;
    \fill[colorA2] (N)   -- (NE)  -- (ENE) to[out=180, in=40]  (C) to[out=90,  in=270] (N)   -- cycle;
    \fill[colorA3] (C) to[out=40,  in=180] (ENE) -- (E)   to[out=180, in=0]   (C) -- cycle;
    \fill[colorB0] (W)   to[out=0,   in=180] (C) to[out=220, in=0]   (WSW) -- cycle;
    \fill[colorB1] (SW)  -- (S)   to[out=90,  in=270] (C) to[out=220, in=0]   (WSW) -- cycle;
    \fill[colorB3] (C) to[out=320, in=180] (ESE) -- (E)   to[out=180, in=0]   (C) -- cycle;
    \fill[colorB2] (S)   -- (SE)  -- (ESE) to[out=180, in=320] (C) to[out=270, in=90]  (S)   -- cycle;

    % border
    \draw[gray] (SW) rectangle (NE);

    % arrows
    \draw[mid->] (N)   to[out=270, in=90]  (C);
    \draw[mid->] (C)   to[out=270, in=90]  (S);
    \draw[mid->] (WNW) to[out=0,   in=140] (C);
    \draw        (W)   to[out=0,   in=180]  (C);
    \draw[mid<-] (WSW) to[out=0,   in=220] (C);
    \draw[mid<-] (C) to[out=40,  in=180] (ENE);
    \draw        (C) to[out=0,   in=180]  (E);
    \draw[mid->] (C) to[out=320, in=180] (ESE);

    % central node
    \node[circle, draw, fill=white, inner sep=3pt] at (C) {};

    % edge labels
    \node[above] at (N)   {$f_2$};
    \node[below] at (S)   {$g_2$};
    \node[left]  at (WNW) {$A_1(f_1, 1)$};
    \node[left]  at (W)   {$H$};
    \node[left]  at (WSW) {$B_1(1, g_1)$};
    \node[right] at (ENE) {$A_3(1, f_3)$};
    \node[right] at (E)   {$J$};
    \node[right] at (ESE) {$B_3(g_3, 1)$};

    % area labels
    \node at ($(NW)!0.5!(WNW)+(0.3, 0)$)  {$A_1$};
    \node at ($(W)!0.5!(WNW) +(0.3, 0)$)  {$A_0$};
    \node at ($(NE)!0.5!(ENE)+(-0.3,0)$)  {$A_2$};
    \node at ($(E)!0.5!(ENE) +(-0.3,0)$)  {$A_3$};
    \node at ($(W)!0.5!(WSW) +(0.3, 0)$)  {$B_0$};
    \node at ($(SW)!0.5!(WSW)+(0.3, 0)$)  {$B_1$};
    \node at ($(E)!0.5!(ESE) +(-0.3,0)$)  {$B_3$};
    \node at ($(SE)!0.5!(ESE)+(-0.3,0)$)  {$B_2$};

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
