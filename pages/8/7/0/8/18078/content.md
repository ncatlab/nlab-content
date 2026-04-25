<table>
<tr>
<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.25 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}

  \def\yT{1}
  \def\yU{0.3}
  \def\yL{-1.3}
  \def\yB{-2}

  \coordinate (Cp) at (0, \yU);
  \coordinate (Cj) at (0, \yL);

  % fills: A covers everything, B is the region bordered by the three arrows
  \fill[colorA] (-1,\yB) rectangle (1,\yT);
  \fill[colorB] (0,\yU) -- (1,\yU) -- (1,\yL) -- (0,\yL) -- cycle;

  % border
  \draw[gray] (-1,\yB) rectangle (1,\yT);

  % f arrow between circles
  \draw[mid->] (Cp) -- (Cj);

  % horizontal arrows
  \draw[mid->] (1,\yU) -- (Cp);
  \draw[mid<-] (1,\yL) -- (Cj);

  % nodes
  \node[circle, draw, fill=white, inner sep=1.5pt] at (Cp) {$\eta_p$};
  \node[circle, draw, fill=white, inner sep=1.5pt] at (Cj) {$\eta_j$};

  % edge labels
  \node[right] at (1,\yU) {$B(1,f)$};
  \node[right] at (1,\yL) {$B(f,1)$};
  \node[left]  at (0,-0.5) {$f$};

  % area labels
  \node at (-0.8, 0.8) {$A$};
  \node at ( 0.5,-0.5) {$B$};

\end{tikzpicture}
</td>
<td style="border: none;">

\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.25 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}

  \def\yT{1}
  \def\yU{0.3}
  \def\yL{-1.3}
  \def\yB{-2}

  \coordinate (Cj) at (0, \yU);   % epsilon_j on top (conjoint counit: N->C, C->E)
  \coordinate (Cp) at (0, \yL);   % epsilon_p on bottom (companion counit: N->C, C->W)

  % fills: B covers everything, A is the region bordered by the three arrows
  \fill[colorB] (-1,\yB) rectangle (1,\yT);
  \fill[colorA] (-1,\yU) -- (0,\yU) -- (0,\yL) -- (-1,\yL) -- cycle;

  % border
  \draw[gray] (-1,\yB) rectangle (1,\yT);

  % f arrow between circles
  \draw[mid->] (Cj) -- (Cp);

  % horizontal arrows sticking out to the left
  \draw[mid<-] (-1,\yU) -- (Cj);   % B(f,1) out of epsilon_j to W
  \draw[mid->] (-1,\yL) -- (Cp);   % B(1,f) into epsilon_p from W

  % nodes
  \node[circle, draw, fill=white, inner sep=1.5pt] at (Cj) {$\epsilon_j$};
  \node[circle, draw, fill=white, inner sep=1.5pt] at (Cp) {$\epsilon_p$};

  % edge labels
  \node[left] at (-1,\yU) {$B(f,1)$};
  \node[left] at (-1,\yL) {$B(1,f)$};
  \node[right] at (0,-0.5) {$f$};

  % area labels
  \node at ( 0.8, 0.8) {$B$};
  \node at (-0.5,-0.5) {$A$};

\end{tikzpicture}
</td>
</tr></table>




\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset
  {
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.25 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}
  \coordinate (W) at (-1, 0);
  \coordinate (E) at ( 1, 0);
  \coordinate (N) at (0, 1);
  \coordinate (S) at (0, -1);
  % fills
  \fill[colorA] (-1,1) rectangle (0,-1);
  \fill[colorB] (0,1) rectangle (1,-1);
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrow points W
  \draw[mid->] (N) -- (S);
  % area labels
  \node at (-0.5,  0) {$A$};
  \node at (0.5, 0) {$B$};
  % edge label
  \node[above] at (N) {$f$};
\end{tikzpicture}


\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset
  {
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.25 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}
  \coordinate (W) at (-1, 0);
  \coordinate (E) at ( 1, 0);
  % fills
  \fill[colorA] (-1,0) rectangle (1,1);
  \fill[colorB] (-1,0) rectangle (1,-1);
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  \draw[line width=0.6pt] (E) -- (W);
  % area labels
  \node at (0,  0.5) {$A$};
  \node at (0, -0.5) {$B$};
  % edge label
  \node[left] at (W) {$P$};
\end{tikzpicture}




\begin{tikzpicture}[scale=2, >=latex]
  \usetikzlibrary{decorations.markings}
  \tikzset{mid->/.style={
    decoration={markings, mark=at position 0.6 with {\arrow[scale=1.5]{>}}},
    postaction={decorate}
  }}

  % x coordinates
  \def\XW{-1}
  \def\XC{0}
  \def\XE{1}

  % y coordinates
  \def\yO{1}   % y0 = top
  \def\yi{0}   % y1
  \def\yii{-1} % y2
  \def\yiii{-2}% y3

  % Quadrant fills
  \fill[blue!15]   (\XW,\yi)  rectangle (\XC,\yO);
  \fill[teal!20]   (\XC,\yi)  rectangle (\XE,\yO);
  \fill[orange!20] (\XW,\yii) rectangle (\XC,\yi);
  \fill[violet!15] (\XC,\yii) rectangle (\XE,\yi);
  \fill[red!20]    (\XW,\yiii) rectangle (\XC,\yii);
  \fill[orange!15] (\XC,\yiii) rectangle (\XE,\yii);

  % Border
  \draw[gray] (\XW,\yiii) rectangle (\XE,\yO);

  % Nodes
  \node[circle,draw,fill=white,inner sep=1.5pt] at (\XC,\yi)  (alpha) {$\alpha$};
  \node[circle,draw,fill=white,inner sep=1.5pt] at (\XC,\yii) (beta)  {$\beta$};

  % Arrows
  \draw[line width=0.6pt] (\XW,\yi)  -- (alpha);
  \draw[line width=0.6pt] (alpha) -- (\XE,\yi);
  \draw[line width=0.6pt] (\XW,\yii) -- (beta);
  \draw[line width=0.6pt] (beta)  -- (\XE,\yii);
  \draw[mid->, line width=0.6pt] (\XC,\yO)   -- (alpha);
  \draw[mid->, line width=0.6pt] (alpha) -- (beta);
  \draw[mid->, line width=0.6pt] (beta)  -- (\XC,\yiii);

  % Labels
  \node[left]  at (\XW,\yi)  {$P$};
  \node[right] at (\XE,\yi)  {$R$};
  \node[left]  at (\XW,\yii) {$Q$};
  \node[right] at (\XE,\yii) {$S$};
  \node[above] at (\XC,\yO)  {$f$};
  \node[left]  at (\XC,-0.5) {$g$};
  \node[below] at (\XC,\yiii){$h$};
  \node at (-0.5, 0.5) {$A$};
  \node at ( 0.5, 0.5) {$B$};
  \node at (-0.5,-0.5) {$C$};
  \node at ( 0.5,-0.5) {$D$};
  \node at (-0.5,-1.5) {$E$};
  \node at ( 0.5,-1.5) {$F$};
\end{tikzpicture}



This can be illustrated using [[string diagrams]], as follows. The companion and conjoint of $f$ are the horizontal arrows

<table>
<tr>
<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.25 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}
  \coordinate (W) at (-1, 0);
  \coordinate (E) at ( 1, 0);
  % fills
  \fill[colorA] (-1,0) rectangle (1,1);
  \fill[colorB] (-1,0) rectangle (1,-1);
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrow points W
  \draw[mid->] (E) -- (W);
  % area labels
  \node at (0,  0.5) {$A$};
  \node at (0, -0.5) {$B$};
  % edge label
  \node[left] at (W) {$B(f, 1)$};
\end{tikzpicture}
</td>
<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{orange!20}
  \colorlet{colorB}{teal!20}
  \coordinate (W) at (-1, 0);
  \coordinate (E) at ( 1, 0);
  % fills
  \fill[colorA] (-1,0) rectangle (1,1);
  \fill[colorB] (-1,0) rectangle (1,-1);
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrow points E
  \draw[mid->] (W) -- (E);
  % area labels
  \node at (0,  0.5) {$B$};
  \node at (0, -0.5) {$A$};
  % edge label
  \node[right] at (E) {$B(1, f)$};
\end{tikzpicture}
</td>
</tr>
</table>

equipped with 2-cells

<table>
<tr>
<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.25 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}
  \coordinate (SE) at ( 1, -1);
  \coordinate (S)  at ( 0, -1);
  \coordinate (E)  at ( 1,  0);
  \coordinate (C)  at ( 0,  0);
  % fills
  \fill[colorA] (-1,-1) rectangle (1,1);
  \fill[colorB] (SE) -- (S) -- (C) -- (E) -- cycle;
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrows
  \draw[mid<-] (S) -- (C);
  \draw[mid->] (E) -- (C);
  % central node
  \node[circle, draw, fill=white, inner sep=1.5pt] at (C) {$\eta_p$};
  % area labels
  \node at (-0.5, 0.5) {$A$};
  \node at ( 0.5,-0.5) {$B$};
  % real edge labels
  \node[below] at (S) {$f$};
  \node[right] at (E) {$B(f,1)$};
  % phantom edge labels for alignment
  \node[above, opacity=0] at (0, 1) {$f$};
  \node[left,  opacity=0] at (-1, 0) {$B(f,1)$};
\end{tikzpicture}
</td>

<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.25 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}
  \coordinate (NW) at (-1,  1);
  \coordinate (N)  at ( 0,  1);
  \coordinate (W)  at (-1,  0);
  \coordinate (C)  at ( 0,  0);
  % fills
  \fill[colorB] (-1,-1) rectangle (1,1);
  \fill[colorA] (NW) -- (N) -- (C) -- (W) -- cycle;
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrows
  \draw[mid->] (N) -- (C);
  \draw[mid<-] (W) -- (C);
  % central node
  \node[circle, draw, fill=white, inner sep=1.5pt] at (C) {$\epsilon_p$};
  % area labels
  \node at (-0.5, 0.5) {$A$};
  \node at ( 0.5,-0.5) {$B$};
  % real edge labels
  \node[above] at (N) {$f$};
  \node[left]  at (W) {$B(f,1)$};
  % phantom edge labels for alignment
  \node[below, opacity=0] at (0, -1) {$f$};
  \node[right, opacity=0] at (1,  0) {$B(f,1)$};
\end{tikzpicture}
</td>

<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.25 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}
  \coordinate (NE) at ( 1,  1);
  \coordinate (N)  at ( 0,  1);
  \coordinate (E)  at ( 1,  0);
  \coordinate (C)  at ( 0,  0);
  % fills
  \fill[colorA] (-1,-1) rectangle (1,1);
  \fill[colorB] (NE) -- (N) -- (C) -- (E) -- cycle;
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrows
  \draw[mid->] (N) -- (C);
  \draw[mid<-] (E) -- (C);
  % central node
  \node[circle, draw, fill=white, inner sep=1.5pt] at (C) {$\eta_j$};
  % area labels
  \node at (-0.5,-0.5) {$A$};
  \node at ( 0.5, 0.5) {$B$};
  % real edge labels
  \node[above] at (N) {$f$};
  \node[right] at (E) {$B(1,f)$};
  % phantom edge labels for alignment
  \node[below, opacity=0] at (0, -1) {$f$};
  \node[left,  opacity=0] at (-1, 0) {$B(f,1)$};
\end{tikzpicture}
</td>

<td style="border: none;">
\begin{tikzpicture}[scale=1]
  \usetikzlibrary{decorations.markings, arrows.meta}
  \tikzset{
    mid->/.style={
      decoration={markings, mark=at position 0.5 with {\arrow[scale=1.5]{Latex}}},
      postaction={decorate}
    },
    mid<-/.style={
      decoration={markings, mark=at position 0.25 with {\arrowreversed[scale=1.5]{Latex}}},
      postaction={decorate}
    }
  }
  \colorlet{colorA}{teal!20}
  \colorlet{colorB}{orange!20}
  \coordinate (SW) at (-1, -1);
  \coordinate (S)  at ( 0, -1);
  \coordinate (W)  at (-1,  0);
  \coordinate (C)  at ( 0,  0);
  % fills
  \fill[colorB] (-1,-1) rectangle (1,1);
  \fill[colorA] (SW) -- (S) -- (C) -- (W) -- cycle;
  % border
  \draw[gray] (-1,-1) rectangle (1,1);
  % arrows
  \draw[mid<-] (S) -- (C);
  \draw[mid->] (W) -- (C);
  % central node
  \node[circle, draw, fill=white, inner sep=1.5pt] at (C) {$\epsilon_j$};
  % area labels
  \node at (-0.5,-0.5) {$A$};
  \node at ( 0.5, 0.5) {$B$};
  % real edge labels
  \node[below] at (S) {$f$};
  \node[left]  at (W) {$B(1,f)$};
  % phantom edge labels for alignment
  \node[above, opacity=0] at (0,  1) {$f$};
\end{tikzpicture}
</td>
</tr>
</table>


***

Spider lemma (corrected)

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
    \node[left]  at (WNW) {$A_1(1, f_1)$};
    \node[left]  at (W)   {$H$};
    \node[left]  at (WSW) {$B_1(g_1, 1)$};
    \node[right] at (ENE) {$A_3(f_3, 1)$};
    \node[right] at (E)   {$J$};
    \node[right] at (ESE) {$B_3(1, g_3)$};

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
