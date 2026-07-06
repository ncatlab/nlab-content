\begin{tikzpicture}[scale=2, >=latex]
  \usetikzlibrary{decorations.markings}
  \tikzset{mid->/.style={
    decoration={markings, mark=at position 0.6 with {\arrow[scale=1.5]{>}}},
    postaction={decorate}
  }}

  % border
  \draw[gray] (-1,-1) rectangle (1,1);

  % central lines (no arrowheads)
  \draw[line width=0.6pt] (-1,0) -- (1,0);
  \draw[line width=0.6pt] (0,-1) -- (0,1);

  % central node
  \node[circle,draw,fill=white,inner sep=1.5pt] at (0,0) {$\pi$};

  % edge labels
  \node[above] at (0,  1) {$\pi_A$};
  \node[below] at (0, -1) {$g$};
  \node[left]  at (-1, 0) {$\pi_B$};
  \node[right] at ( 1, 0) {$f$};

  % area labels
  \node at (-0.5,  0.5) {$f/g$};
  \node at ( 0.5,  0.5) {$A$};
  \node at (-0.5, -0.5) {$B$};
  \node at ( 0.5, -0.5) {$C$};

\end{tikzpicture}

\begin{tikzpicture}[scale=2, >=latex]
  \usetikzlibrary{decorations.markings}
  \tikzset{mid->/.style={
    decoration={markings, mark=at position 0.6 with {\arrow[scale=1.5]{>}}},
    postaction={decorate}
  }}

  % --- LEFT DIAGRAM ---
  % border
  \draw[gray] (-1,-1) rectangle (1,1);

  % central lines
  \draw[line width=0.6pt] (-1,0) -- (1,0);
  \draw[line width=0.6pt] (0,-1) -- (0,1);

  % central node
  \node[circle,draw,fill=white,inner sep=1.5pt] at (0,0) {$\phi$};

  % edge labels
  \node[above] at (0,  1) {$\phi_A$};
  \node[below] at (0, -1) {$g$};
  \node[left]  at (-1, 0) {$\phi_B$};
  \node[right] at ( 1, 0) {$f$};

  % area labels
  \node at (-0.5,  0.5) {$W$};
  \node at ( 0.5,  0.5) {$A$};
  \node at (-0.5, -0.5) {$B$};
  \node at ( 0.5, -0.5) {$C$};

  % equal sign
  \node at (1.5, 0) {$=$};

  % --- RIGHT DIAGRAM ---
  \begin{scope}[xshift=3cm]

    % node positions
    \coordinate (PHI) at (-0.35,  0.35);
    \coordinate (PI)  at ( 0.35, -0.35);

    % border
    \draw[gray] (-1,-1) rectangle (1,1);

    % lines from phi' to edges
    \draw[line width=0.6pt] (-1,   0.35) -- (PHI);
    \draw[line width=0.6pt] (-0.35, 1)   -- (PHI);

    % lines from pi to edges
    \draw[line width=0.6pt] (PI) -- ( 1, -0.35);
    \draw[line width=0.6pt] (PI) -- ( 0.35, -1);

    % curved arcs between phi' and pi (strongly curved)
    \draw[line width=0.6pt] (PHI) to[out=0,  in=90] (PI);  % upper arc, bulges up-right
    \draw[line width=0.6pt] (PHI) to[out=270, in=180] (PI);  % lower arc, bulges down-left
    % arc labels shifted outward
    \node at ( 0.3,  0.2) {$\pi_A$};
    \node at (-0.3, -0.2) {$\pi_B$};

    % f/g label between circles
    \node at (0, 0) {$f/g$};

    % nodes
    \node[circle,draw,fill=white,inner sep=1.5pt] at (PHI) {$\phi'$};
    \node[circle,draw,fill=white,inner sep=1.5pt] at (PI)  {$\pi$};

    % edge labels
    \node[above] at (-0.35,  1) {$\phi'_A$};
    \node[below] at ( 0.35, -1) {$g$};
    \node[left]  at (-1,  0.35) {$\phi'_B$};
    \node[right] at ( 1, -0.35) {$f$};

    % area labels
    \node at (-0.7,  0.7) {$W$};
    \node at ( 0.7,  0.7) {$A$};
    \node at (-0.7, -0.7) {$B$};
    \node at ( 0.7, -0.7) {$C$};

  \end{scope}

\end{tikzpicture}


***


\begin{tikzpicture}[scale=2, >=latex]
  \usetikzlibrary{decorations.markings}
  \tikzset{mid->/.style={
    decoration={markings, mark=at position 0.6 with {\arrow[scale=1.5]{>}}},
    postaction={decorate}
  }}

  % --- THIRD DIAGRAM (left) ---
  \coordinate (C) at (-0.5, 0);

  % fills
  \fill[blue!15]   (-1,1) to[out=270, in=130] (C) to[out=50,  in=270] (0,1)  -- cycle;
  \fill[orange!20] (-1,-1) to[out=90, in=230]  (C) to[out=310, in=90]  (0,-1) -- cycle;
  \fill[teal!20]   (0,1)  to[out=270, in=50]  (C) -- (1,0) -- (1,1)   -- cycle;
  \fill[violet!15] (C) to[out=310, in=90] (0,-1) -- (1,-1) -- (1,0)   -- cycle;

  % borders
  \draw[gray] (-2,-1) rectangle (1,1);
  \draw[gray] (-2, 0) -- (-1, 0);

  % arrows
  \draw[mid->, line width=0.6pt] (-1, 1) to[out=270, in=130] (C);
  \draw[mid->, line width=0.6pt] (C) to[out=230, in=90] (-1,-1);
  \draw[mid->, line width=0.6pt] (0,  1) to[out=270, in=50]  (C);
  \draw[mid->, line width=0.6pt] (C) to[out=310, in=90] (0, -1);
  \draw[line width=0.6pt] (-2, 0) -- (C);
  \draw[line width=0.6pt] (C) -- (1, 0);

  % node
  \node[circle,draw,fill=white,inner sep=1.5pt] at (C) {$\psi$};

  % labels
  \node[left]  at (-2, 0) {$L$};
  \node[right] at ( 1, 0) {$J$};
  \node[above] at (-1, 1) {$h$};
  \node[below] at (-1,-1) {$k$};
  \node[above] at ( 0, 1) {$f$};
  \node[below] at ( 0,-1) {$g$};
  \node at (-1.5,  0.5) {$X$};
  \node at (-1.5, -0.5) {$Y$};
  \node at (-0.5,  0.6) {$A$};
  \node at (-0.5, -0.6) {$C$};
  \node at ( 0.5,  0.5) {$B$};
  \node at ( 0.5, -0.5) {$D$};
  % equal sign
  \node at (1.5, 0) {$=$};

  % --- SECOND DIAGRAM (right) ---
  \begin{scope}[xshift=4cm]

    \coordinate (psi) at (-1, 0);
    \coordinate (alpha) at (0, 0);

    % fills
    \fill[blue!15]   (-1,0) rectangle (0,1);
    \fill[teal!20]   (0,0)  rectangle (1,1);
    \fill[orange!20] (-1,-1) rectangle (0,0);
    \fill[violet!15] (0,-1)  rectangle (1,0);
    % borders
    \draw[gray] (-2,-1) rectangle (1,1);
    \draw[gray] (-2, 0) -- (-1, 0);

    % arrows
    \draw[mid->, line width=0.6pt] (-1, 1) -- (psi);
    \draw[mid->, line width=0.6pt] (psi) -- (-1,-1);
    \draw[mid->, line width=0.6pt] (0,  1) -- (alpha);
    \draw[mid->, line width=0.6pt] (alpha) -- (0,-1);
    \draw[line width=0.6pt] (-2, 0) -- (psi);
    \draw[line width=0.6pt] (psi) -- (alpha);
    \draw[line width=0.6pt] (alpha) -- (1, 0);

    % nodes
    \node[circle,draw,fill=white,inner sep=1.5pt] at (psi)   {$\psi'$};
    \node[circle,draw,fill=white,inner sep=1.5pt] at (alpha) {$\alpha$};

    % labels
    \node[left]  at (-2, 0) {$L$};
    \node[right] at ( 1, 0) {$J$};
    \node[above] at (-1, 1) {$h$};
    \node[below] at (-1,-1) {$k$};
    \node[above] at ( 0, 1) {$f$};
    \node[below] at ( 0,-1) {$g$};
    \node at (-1.5,  0.5) {$X$};
    \node at (-1.5, -0.5) {$Y$};
    \node at (-0.5,  0.5) {$A$};
    \node at ( 0.5,  0.5) {$B$};
    \node at (-0.5, -0.5) {$C$};
    \node at ( 0.5, -0.5) {$D$};

  \end{scope}

\end{tikzpicture}



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

  \coordinate (Cu) at (-0.7, 0);
  \coordinate (Cc) at ( 0.7, 0);

  % fills
  \fill[colorA] (-1.5,-1) rectangle (-0.7, 1);
  \fill[colorA] (-0.7, 0) rectangle ( 0.7, 1);
  \fill[colorB] (-0.7,-1) rectangle ( 0.7, 0);
  \fill[colorB] ( 0.7,-1) rectangle ( 1.5, 1);

  % border
  \draw[gray] (-1.5,-1) rectangle (1.5,1);

  % f arrows
  \draw[mid<-] (-0.7,-1) -- (Cu);
  \draw[mid->] ( 0.7, 1) -- (Cc);

  % horizontal arrow pointing left
  \draw[mid->] (Cc) -- (Cu);

  % nodes
  \node[circle, draw, fill=white, inner sep=1.5pt] at (Cu) {$\eta_p$};
  \node[circle, draw, fill=white, inner sep=1.5pt] at (Cc) {$\epsilon_p$};

  % edge labels
  \node[below] at (-0.7,-1) {$f$};
  \node[above] at ( 0.7, 1) {$f$};

  % area labels
  \node at (-1.1, 0.5) {$A$};
  \node at ( 1.1,-0.5) {$B$};

  % equal sign
  \node at (2.0, 0) {$=$};

  % --- RIGHT DIAGRAM ---
  \begin{scope}[xshift=3.2cm]

    % fills
    \fill[colorA] (-0.7,-1) rectangle (0,1);
    \fill[colorB] (0,-1)    rectangle (0.7,1);

    % border
    \draw[gray] (-0.7,-1) rectangle (0.7,1);

    % vertical arrow
    \draw[mid->] (0,1) -- (0,-1);

    % edge labels
    \node[above] at (0, 1) {$f$};

    % area labels
    \node at (-0.4, 0) {$A$};
    \node at ( 0.4, 0) {$B$};

  \end{scope}

\end{tikzpicture}


<table>
<tr>
<td style="border: none;">
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

beautiful rainbow sand
___

The multivariable inverse function theorem is typically associated with the operators
$$
N_{f,x_0,y}  :  \mathbb{R}^n  \rightarrow \mathbb{R}^n, x  \mapsto x + Df(x_0)^{-1} (y - f(x)) 
$$
and to an approach in which a Lipschitz function is used, to the effect that this operator is a contraction within a certain set specified by a small distance:
$$
\parallel N_{f,x_0,y}(x_1) - N_{f,x_0,y}(x_2) \parallel_2 \le C \cdot \parallel x_1 - x_2 \parallel_2
$$
This is the approach used in [[#Rudin1976]].

This requires ...
https://ncatlab.org/nlab/show/Lipschitz+map

\begin{theorem}\label{continuouslydifferentiableLipschitzfunction} (an equivalent condition for a continuously differentiable function defined on an open ball to be Lipschitz) fix $x_0 \in \mathbb{R}^n$ and a positive real number $\delta$. 

Let $f = (f_1,...,f_n) : B_{\delta}(x_0) \rightarrow \mathbb{R}^n$ be a continuously differentiable function. Then $f = (f_1,...,f_n)$ is Lipschitz with Lipschitz constant $C$ if and only if, for each $x \in B_{\delta}(x_0)$, the Jacobian derivative $Df(x)$ of $f$ at $x$ satisfies $  \parallel Df(x)  \parallel_2 \leq C$.
\end{theorem}

\begin{proof} for each $x_1, x_2 \in \mathbb{R}^n$ such that $  \parallel x_1 - x_0  \parallel_2 \le \delta$ and $  \parallel x_2 - x_0  \parallel_2 \le \delta$, there is an inequality of

$$
\begin{aligned}
\|y_1+t(y_2-y_1)\|_2
&=\|(1-t)y_1+ty_2\|_2\\
&\le \|(1-t)y_1\|_2+\|ty_2\|_2\\
&=(1-t)\|y_1\|_2+t\|y_2\|_2\\
&=(1-t)\delta+t\delta\\
&=\delta.
\end{aligned}
$$

from this it follows that $  \parallel y_1 + t \cdot (y_2 - y_1)  \parallel  \leq $
let $\gamma_{x_0,\delta, x_1,  x_2} : [0,1] \rightarrow B_{\delta}(x_0)$ be the continuously differentiable function sending $t$ to $x_1 + t \cdot (x_2 - x_1)$.

By the chain rule for continuously differentiable functions, $D(f \circ \gamma_{x_0,\delta,x_1,x_2})(t) = Df(\gamma_{x_0,\delta,x_1,x_2}(t)) \circ D\gamma_{x_0,\delta,x_1,x_2}(t)$.

If $  \parallel Df(x)  \parallel _2 \leq C$ for each $x \in \mathbb{R}^n$, then we have

$$
\begin{aligned}
 &   \parallel  D(f \circ \gamma_{x_0,\delta,x_1,x_2})(t)   \parallel _2 \\
 =\ &   \parallel  Df(\gamma_{x_0,\delta,x_1,x_2}(t)) \circ D\gamma_{x_0,\delta,x_1,x_2}(t)   \parallel _2 \\
 \leq \ &    \parallel  Df(\gamma_{x_0,\delta,x_1,x_2}(t))  \parallel _2 \cdot   \parallel  D\gamma_{x_0,\delta,x_1,x_2}(t)   \parallel _2 \\ 
 \leq \ & C  \cdot   \parallel x_2 - x_1  \parallel _2
\end{aligned}
$$

so

$$
\begin{aligned}
\ &   \parallel f(x_2) - f(x_1)  \parallel _2\  \\
=\ & \left| \left| \int_0^1 D(f \circ \gamma_{x_0,\delta,x_1,x_2})(t) dt \right| \right|_2 \\
\leq \ & \int_0^1 \left| \left|  D(f \circ \gamma_{x_0,\delta,x_1,x_2})(t) dt \right| \right|_2 \\
\ \leq \ & \int_0^1 C \cdot \left| \left| x_2 - x_1  \right| \right|_2 dt  \\
\ = \ & C \cdot   \parallel x_2 - x_1   \parallel _2 
\end{aligned}
$$

where we have used that, for the continuous function 

$$
D(f \circ \gamma_{x_0,\delta,x_1,x_2}) = \left( D(f \circ \gamma_{x_0,\delta,x_1,x_2})_1,...,D(f \circ \gamma_{x_0,\delta,x_1,x_2})_n \right) : \text{[0,1]} \rightarrow \mathbb{R}^n
$$

that

$$
\parallel \int_0^1 D(f \circ \gamma_{x_0,\delta,x_1,x_2}) dt \parallel_2 \leq \int_0^1   \parallel D(f \circ \gamma_{x_0,\delta,x_1,x_2})  \parallel_2 dt
$$

This proves that $f$ is Lipschitz with Lipschitz constant $C$.

Conversely, if $f$ is Lipschitz with Lipschitz constant $C$, then fixing $x \in \mathbb{R}^n$ such that $  \parallel x - x_0  \parallel _2  \le  \delta$ and any positive real number $\epsilon$, there is a positive real number $\delta'$ such that $B_{\delta'}(x) \subseteq B_{\delta}(x_0)$ and 

$$
\begin{aligned}
\forall y \in B_{\delta'}(x), \left| \left| \frac{f(y) - f(x)}{  \parallel y - x  \parallel _2} - \frac{Df(x)(y-x)}{  \parallel y - x  \parallel _2} \right| \right|_2  \le  \epsilon
\end{aligned}
$$

Since $f$ is Lipschitz with Lipschitz constant $C$, 

$$
\frac{  \parallel f(y) - f(x)  \parallel _2}{  \parallel y - x  \parallel _2}  \leq C
$$

From this calculate that

$$
\begin{aligned}
&  \frac{ \left| \left| Df(x)(y-x) \right| \right|_2 }{   \parallel y-x  \parallel _2 }   \\
\leq\ &   \frac{  \parallel  f(y) - f(x)  \parallel _2 }{  \parallel y - x  \parallel _2 }  + \left| \left| \frac{f(y) - f(x)}{  \parallel y - x  \parallel _2} - \frac{Df(x)(y-x)}{  \parallel y - x  \parallel _2} \right| \right|_2  \\
\leq\ & C + \epsilon
\end{aligned}
$$

Since this holds for each positive real number $\epsilon$, it follows that

$$
  \parallel Df(x)  \parallel _2 = \mathrm{sup} \left\{ \frac{  \parallel Df(x)(y-x)  \parallel_2}{  \parallel y-x  \parallel_2} : y \in \mathbb{R}^n - \{ x \} \right\} \leq C
$$

for each $y \in B_{\delta'}(x)$. This is (2) of the claim.
\end{proof}



\begin{definition} (the Newton approximator) fix $n \in \mathbb{N}$ and let $f : \mathbb{R}^n \rightarrow \mathbb{R}^n$ be a continuously differentiable function. Suppose that the Jacobian derivative $Df(x_0)$ of $f$ at some fixed $x_0 \in \mathbb{R}^n$ is invertible.

For each $y \in \mathbb{R}^n$, define the function 

$$
\begin{aligned}
N_{f,x_0,y} : \mathbb{R}^n & \rightarrow \mathbb{R}^n \\
x & \mapsto x + Df(x_0)^{-1}(y - f(x))
\end{aligned}
$$

$N_{f,x_0,y}$ is continuously differentiable. Indeed, $N_{f,x_0,y}$ can be constructed from the continuously differentiable functions of:

* the identity map $\mathrm{Id}_{\mathbb{R}^n} : \mathbb{R}^n \rightarrow \mathbb{R}^n$

* the continuously differentiable function $f : \mathbb{R}^n \rightarrow \mathbb{R}^n$

* the linear map $Df(x_0)^{-1} : \mathbb{R}^n \rightarrow \mathbb{R}^n$
\item the constant function $c_y : \mathbb{R}^n \rightarrow \mathbb{R}^n$ sending $x$ to $y$ for each $x \in \mathbb{R}^n$

Using composition, summation, and additive negation.
\end{definition}

Since summation 
$$
+ : \mathbb{R}^n \times \mathbb{R}^n \rightarrow \mathbb{R}^n
$$
\noindent and additive negation
$$
- : \mathbb{R}^n \rightarrow \mathbb{R}^n
$$
are continuous functions, we can rephrase the above as reducing the property of $N_{f,x_0,y}$ that it be continuously differentiable to the property that the following are continuously differentiable:

*  the identity map $\mathrm{Id}_{\mathbb{R}^n} : \mathbb{R}^n \rightarrow \mathbb{R}^n$

* the continuously differentiable function $f : \mathbb{R}^n \rightarrow \mathbb{R}^n$

* the linear map $Df(x_0)^{-1} : \mathbb{R}^n \rightarrow \mathbb{R}^n$
\item the constant function $c_y : \mathbb{R}^n \rightarrow \mathbb{R}^n$ sending $x$ to $y$ for each $x \in \mathbb{R}^n$

* binary addition of elements of $\mathbb{R}^n$, $+ : \mathbb{R}^n \times \mathbb{R}^n \rightarrow \mathbb{R}^n$

* additive negation of elements of $\mathbb{R}^n$, $- : \mathbb{R}^n \rightarrow \mathbb{R}^n$

and the theorem that the composition of continuously differentiable functions $f_1 : \mathbb{R}^{n_1} \rightarrow \mathbb{R}^{n_2}$ and $f_2 : \mathbb{R}^{n_2} \rightarrow \mathbb{R}^{n_3}$ that $f_2 \circ f_1 : \mathbb{R}^{n_1} \rightarrow \mathbb{R}^{n_3}$ is continuously differentiable.

\begin{lemma} (fixed points of the Newton approximator are preimages of $y$ under $f$) fix $n \in \mathbb{N}$ and let $f : \mathbb{R}^n \rightarrow \mathbb{R}^n$ be a continuously differentiable function. Suppose that the Jacobian derivative $Df(x_0)$ of $f$ at some fixed $x_0 \in \mathbb{R}^n$ is invertible. For each $x \in \mathbb{R}^n$, the following are equivalent:

* $N_{f,x_0,y}(x) = x$, where $N_{f,x_0,y} : \mathbb{R}^n \rightarrow \mathbb{R}^n$ is the continuously differentiable function defined in 

* $f(x) = y$

\end{lemma}

\begin{proof} for each $x \in \mathbb{R}^n$, we calculate that

$$
\begin{aligned}
&\Leftrightarrow N_{f,x_0,y}(x)=x \\
&\Leftrightarrow x + Df(x_0)^{-1}(y - f(x)) = x \\
&\Leftrightarrow Df(x_0)^{-1}(y - f(x)) = 0 \\
&\Leftrightarrow Df(x_0)\, \left( Df(x_0)^{-1}(y - f(x)) \right) = 0 \\
&\Leftrightarrow y - f(x) = 0 \\
&\Leftrightarrow f(x) = y
\end{aligned}
$$

\end{proof}

\begin{lemma} (the derivative of the Newton approximator) fix $n \in \mathbb{N}$ and let $f : \mathbb{R}^n \rightarrow \mathbb{R}^n$ be a continuously differentiable function. Suppose that the Jacobian derivative $Df(x_0)$ of $f$ at some fixed $x_0 \in \mathbb{R}^n$ is invertible. Then the derivative $DN_{f,x_0,y}(x)$ of the continuously differentiable function $N_{f,x_0,y} : \mathbb{R}^n \rightarrow \mathbb{R}^n$ is 

$$
DN_{f,x_0,y}(x) = \mathrm{Id}_{\mathbb{R}^n} - Df(x_0)^{-1} \circ Df(x)
$$

\end{lemma}

\begin{proof} using the summation rule for continuously differentiable functions, we have for each $x \in \mathbb{R}^n$ that

$$
D N_{f,x_0,y}(x)  = \left( D \mathrm{Id}_{\mathbb{R}^n} + D \left( Df(x_0)^{-1} (y) \right) - D \left( Df(x_0)^{-1} \circ f \right) \right)(x)
$$

The first summand is the identity morphism for each $x \in \mathbb{R}^n$:

$$
D\mathrm{Id}_{\mathbb{R}^n}(x) = \mathrm{Id}_{\mathbb{R}^n}
$$

The second summand is zero for each $x \in \mathbb{R}^n$ as it is the Jacobian derivative of a constant function 

$$
Df(x_0)^{-1} (y) = c_{Df(x_0)^{-1} (y)} : \mathbb{R}^n \rightarrow \mathbb{R}^n
$$

evaluated at $x \in \mathbb{R}^n$, which is $0$:

$$
D \left( Df(x_0)^{-1} (y) \right)(x) = 0
$$

\noindent the third summand is 

$$
  - D \left( Df(x_0)^{-1}  \circ f \right)(x) = D \left( -Df(x_0)^{-1} \right)(f(x)) \circ Df(x)  
$$

\noindent by the chain rule for Jacobian derivatives of continuously differentiable functions. Since the Jacobian derivative $DA(x)$ of the linear map $A : \mathbb{R}^n \rightarrow \mathbb{R}^n$ at any point $x \in \mathbb{R}^n$ is $A$, we have

$$
 D \left(-Df(x_0)^{-1} \circ f \right)(x) = - Df(x_0)^{-1} \circ Df(x) 
$$

$$
DN_{f,x_0,y} = \mathrm{Id}_{\mathbb{R}^n} - Df(x_0)^{-1} \circ Df(x) 
$$

\end{proof}

Note that, in the context above, 
$$
\mathrm{Id}_{\mathbb{R}^n} - Df(x_0)^{-1} \circ Df(x) = Df(x_0)^{-1} \left( Df(x_0) - Df(x) \right)
$$
\noindent and that $f$ is continuously differentiable implies that, for any positive real number $\epsilon$, there is an open subset $U$ of $\mathbb{R}^n$ containing $x_0$ such that, for each $x \in U$,

$$
 \left| \left| Df(x_0) - Df(x) \right| \right|_2   \le  \frac{\epsilon}{  \parallel Df(x_0)^{-1}   \parallel _2}
$$

which implies that, for each $x \in U$

$$
\begin{aligned}
     & \left| \left| \mathrm{Id}_{\mathbb{R}^n} - Df(x_0)^{-1} \circ Df(x) \right| \right|_2 \\
\leq\ & \left| \left| Df(x_0)^{-1} \cdot (Df(x_0) - Df(x)) \right| \right|_2 \\
\leq\ & \left| \left| Df(x_0)^{-1} \right| \right|_2 \cdot \left| \left| Df(x_0) - Df(x) \right| \right|_2  \\
 \le \ &   \left| \left| Df(x_0)^{-1} \right| \right|_2 \cdot \frac{\epsilon}{ \left| \left| Df(x_0)^{-1} \right| \right|_2} \\
=\ & \epsilon
\end{aligned}
$$



\begin{lemma} let $C$ a positive real number. Then $C$ is strictly smaller than $\frac{1}{2}$ if and only if
$$
\sum_{i=1}^{\infty} C^i  \le  1
$$
\end{lemma}

\begin{proof} let $C$ be a positive real number. For each $n \in \mathbb{N}$, we have
$$
\begin{aligned}
  & (1-C) \cdot \sum_{i = 1}^{n} C^{i}  \\
= & \sum_{i = 1}^n C^{i} - C \cdot \sum_{i=1}^n C^{i} \\
= & \sum_{i=1}^n C^{i} - \sum_{i=2}^{n+1} C^{i}  \\
= & C \cdot (1 - C^{n})
\end{aligned}
$$
If $C$ is $1$, then $\sum_{i =1}^{\infty} C^i = \sum_{i= 1}^{\infty} 1 = \infty$ does not converge and $C$ is not strictly less than $1/2$. 

To proceed, assume $C \neq 1$. Dividing by $1 - C$, one obtains 
$$
\sum_{i= 1}^n C^i =  \frac{C - C^{n}}{1 - C}
$$
\noindent and from this one obtains 
$$
\sum_{i= 1}^{\infty} C^i = \frac{C}{1 - C} 
$$
We calculate
$$
\begin{aligned}
 & \sum_{i= 1}^{\infty} C^i  \le  1 \\
\leftrightarrow\ & \frac{C}{1 - C}   \le  1 \\
\leftrightarrow\ & C  \le  1-C \\
\leftrightarrow\ & 2C  \le  1 \\
\leftrightarrow\ & C  \le  \frac{1}{2}
\end{aligned}
$$
\end{proof}


\begin{theorem} (inverse function theorem) let $f : \mathbb{R}^n \rightarrow \mathbb{R}^n$ be a continuously differentiable function. Fix $x_0 \in \mathbb{R}^n$ and write $y_0$ for $f(x_0)$. If the Jacobian derivative $Df(x_0) : \mathbb{R}^n \rightarrow \mathbb{R}^n$ of $f$ at $x_0 \in \mathbb{R}^n$ is invertible, then there are positive real numbers $\delta$ and $\epsilon$ such that
\begin{enumerate}
\item for each $x_1, x_2 \in \mathbb{R}^n$ such that $  \parallel x_1 - x_0  \parallel _2  \le  \delta$ and $  \parallel x_2 - x_0  \parallel _2  \le  \delta$, $f(x_1) = f(x_2)$ implies $x_1 = x_2$
\item for each $y \in \mathbb{R}^n$ such that $  \parallel y - y_0  \parallel _2  \le  \epsilon$, there is $x \in \mathbb{R}^n$ such that $  \parallel  x - x_0  \parallel _2   \le  \delta$ and $y = f(x)$
\end{enumerate}
Note that (1) and (2) imply the resulting $C^1$-function $f|_{f^{-1}(B_{\epsilon}(y_0))} : f^{-1}(B_{\epsilon}(y_0)) \rightarrow B_{\epsilon}(y_0)$ is both injective and surjective.
\end{theorem}

\begin{proof} fix a positive real number $C  \le  1$ such that 
$$
\sum_{i = 1}^{\infty} C^i  \le  1
$$
\noindent equivalently, a positive real number $C$ such that $C  \le  \frac{1}{2}$.

Pick positive real numbers $\delta$ and $\epsilon$ as follows:

* pick $\delta$ to be a positive real number such that  
$$
\forall x \in \mathbb{R}^n,   \parallel x - x_0  \parallel _2  \le  \delta \rightarrow   \parallel Df(x) - Df(x_0)  \parallel _2  \le    \parallel Df(x_0)^{-1}  \parallel _2^{-1} \cdot C
$$
where to do this we use that $f$ is continuously differentiable at $x_0$
* pick $\epsilon$ to be $  \parallel Df(x_0)^{-1}  \parallel _2^{-1} \cdot  C \cdot \delta$

We will show the first and second claims for these particular choices of $\delta$ and $\epsilon$.

We first show the first of these, that for each $x_1, x_2 \in \mathbb{R}^n$ such that $  \parallel x_1 - x_0  \parallel _2  \le  \delta$ and $  \parallel x_2 - x_0  \parallel _2  \le  \delta$, $f(x_1) = f(x_2)$ implies $x_1 = x_2$. Recall that in definition \ref{theNewtonapproximator}, we defined a $C^1$-function $N_{f,x_0,y} : \mathbb{R}^n \rightarrow \mathbb{R}^n$ which satisfies $N_{f,x_0,y}(x) = x + Df(x_0)^{-1}(y - f(x))$.

In the above it was demonstrated that $DN_{f,x_0,y}(x) = \mathrm{Id}_{\mathbb{R}^n} -  Df(x_0)^{-1} \circ Df(x)$. This implies that 

$$
\begin{aligned}
       &   \parallel DN_{f,x_0,y}(x)  \parallel _2  \\
=\     &   \parallel \mathrm{Id} - Df(x_0)^{-1} \circ Df(x)  \parallel _2 \\
=\     &   \parallel Df(x_0)^{-1} \cdot Df(x_0) - Df(x_0)^{-1} \circ Df(x)  \parallel _2 \\
=\     &   \parallel Df(x_0)^{-1} \cdot ( Df(x_0) - Df(x) )  \parallel _2 \\
\leq\  &   \parallel Df(x_0)^{-1}   \parallel _2  \cdot   \parallel  Df(x_0) - Df(x)   \parallel _2 \\
 \le  \    &   \parallel Df(x_0)^{-1}   \parallel _2 \cdot   \parallel Df(x_0)^{-1}  \parallel _2^{-1} \cdot C \\
= \ & C
\end{aligned}
$$

In lemma \ref{continuouslydifferentiableLipschitzfunction}, it was demonstrated that this implies that, for each $x_1, x_2 \in \mathbb{R}^n$ such that $  \parallel x_1 - x_0  \parallel _2  \le  \delta$ and $  \parallel x_2 - x_0  \parallel _2  \le  \delta$, $  \parallel N_{f,x_0,y}(x_1) - N_{f,x_0,y}(x_2)  \parallel _2 \leq C \cdot   \parallel x_1 - x_2  \parallel _2$. 

Suppose for a contradiction that $x_1, x_2 \in \mathbb{R}^n$ with $x_1 \neq x_2$ are such that $  \parallel x_1 - x_0  \parallel _2  \le  \delta$ and $  \parallel x_2 - x_0  \parallel _2  \le  \delta$, and satisfy $f(x_1) = f(x_2)$. Writing $y$ for this value, we have $N_{f,x_0,y}(x_1) = x_1$ and $N_{f,x_0,y}(x_2) = x_2$ by lemma \ref{fixedpointoftheNewtonapproximator}.

We calculate that

$$
\begin{aligned}
   &   \parallel x_1 - x_2  \parallel _2 \\
=\ &   \parallel N_{f,x_0,y}(x_1) - N_{f,x_0,y}(x_2)   \parallel _2  \\
\leq \ & C  \cdot   \parallel  x_1 - x_2   \parallel _2   \\
 \le \ &   \parallel x_1 - x_2  \parallel _2 
\end{aligned}
$$

which is is a contradiction. We conclude that $  \parallel x_1 - x_2  \parallel _2 = 0$, and also that this implies $x_1 = x_2$. 

This argument shows the first claim (1).


Recall that we have defined $\epsilon =   \parallel Df(x_0)^{-1}  \parallel _2^{-1} \cdot C \cdot \delta$, a positive real number. We next demonstrate that for each $y \in \mathbb{R}^n$ such that $  \parallel y - y_0  \parallel _2  \le  \epsilon$, there is $x \in \mathbb{R}^n$ such that $  \parallel x - x_0  \parallel _2   \le  \delta$ and $y = f(x)$. To do this, fix $y \in \mathbb{R}^n$ such that $  \parallel y - y_0  \parallel _2  \le  \epsilon$. Fix $y \in \mathbb{R}^n$ with $  \parallel y - y_0  \parallel _2  \le  \epsilon$.

In the above, we showed that 

$$
D N_{f,x_0,y}(x) = \mathrm{Id}_{\mathbb{R}^n} - (Df(x_0)^{-1} \cdot Df(x))
$$

The positive real number $\delta$ was chosen so that, for each $x \in \mathbb{R}^n$ such that $  \parallel x - x_0  \parallel _2  \le  \delta$, $  \parallel Df(x) - Df(x_0)  \parallel _2  \le  C$. We calculated in the proof of (1) that

$$
\begin{aligned}
 &   \parallel DN_{f,x_0,y}(x)  \parallel_2 \\
=\ &   \parallel \mathrm{Id}_{\mathbb{R}^n} - (Df(x_0)^{-1} \cdot Df(x))  \parallel _2 \\
=\ &   \parallel Df(x_0)^{-1} \cdot (Df(x_0) - Df(x))  \parallel _2 \\
=\ &   \parallel Df(x_0)^{-1}  \parallel _2 \cdot   \parallel Df(x_0) - Df(x)  \parallel _2 \\
 \le  \ &   \parallel Df(x_0)^{-1}  \parallel _2 \cdot   \parallel Df(x_0)^{-1}  \parallel _2^{-1} \cdot C \\
= \ & C
\end{aligned}
$$

We here apply theorem \ref{continuouslydifferentiableLipschitzfunction} as in the proof of (1) to conclude that, for each $x_1, x_2 \in \mathbb{R}^n$ such that $  \parallel x_1 - x_0  \parallel _2  \le  \delta$ and $  \parallel x_2 - x_0  \parallel _2  \le  \delta$, $  \parallel N_{f,x_0,y}(x_2) - N_{f,x_0,y}(x_1)  \parallel _2  \le  C \cdot   \parallel x_2 - x_1  \parallel _2$.

Define a sequence of real vectors $x : \mathbb{N} \rightarrow \mathbb{R}^n$ by induction. Set $x(0)$ as $x_0$, and set $x(n+1)$ as $N_{f,x_0,y}(x(n))$. Write $\{ x_n \}_{n = 0}^{\infty}$ for this sequence.

We show by induction on $n \in \mathbb{N}$ that 

* $  \parallel x_n - x_0  \parallel _2  \le  \sum_{i=1}^n C^{i} \cdot \delta$

* $  \parallel x_{n+1} - x_n   \parallel _2  \le  C^{n+1} \cdot \delta$


For the base step, set $n = 0$. That $  \parallel x_0 - x_0  \parallel _2  \le  \sum_{i=0}^0 C^{i} \cdot \delta$ is immediate as $  \parallel x_0 - x_0  \parallel _2 = 0$ and the right hand side is $\delta$, which is positive.

To see (2), we calculate that:

$$
\begin{aligned}
      &   \parallel N_{f,x_0,y}(x_0) - x_0  \parallel _2 \\
=\    &   \parallel Df(x_0)^{-1}(y-y_0)  \parallel _2 \\
\leq\ &   \parallel Df(x_0)^{-1}  \parallel _2 \cdot   \parallel y - y_0  \parallel _2 \\
=\ &    \parallel Df(x_0)^{-1}  \parallel _2 \cdot \epsilon \\
 \le \ &   \parallel Df(x_0)^{-1}  \parallel _2 \cdot \delta \cdot   \parallel Df(x_0)^{-1}  \parallel _2^{-1} \\
= \ & C \cdot \delta
\end{aligned}
$$

This completes the base case.

For the induction step, fix $n \in \mathbb{N}$ and assume that 

* $  \parallel x_n - x_0  \parallel _2  \le  \sum_{ i = 1 }^{n} C^{i} \cdot \delta$

* $  \parallel x_{n+1} - x_n   \parallel _2  \le   C^{n+1} \cdot \delta$


By the triangle inequality, we have

$$
\begin{aligned}
     \ &   \parallel x_{n+1} - x_0   \parallel _2 \\
\leq \ &   \parallel x_n - x_0  \parallel _2 +   \parallel x_{n+1} - x_n   \parallel _2\\
\leq \ & \left( \sum_{ i = 1}^{n} C^{i} \cdot \delta \right) +  C^{n+1} \cdot \delta \\
    \le  \ & \sum_{i = 1}^{n+1}  C^{i} \cdot \delta
\end{aligned}
$$

This implies (1). 

For each $n \in \mathbb{N}$,

$$
  \parallel x_{n+1} - x_0  \parallel _2  \le  \sum_{i = 1}^{n+1} C^{i} \cdot \delta  \le  \delta
$$

For each $x_1, x_2 \in \mathbb{R}^n$ such that $  \parallel x_1 - x_0  \parallel _2  \le  \delta$ and $  \parallel x_2 - x_0  \parallel _2  \le  \delta$, 

$$
  \parallel N_{f,x_0,y} (x_2) - N_{f,x_0,y} (x_1)   \parallel _2   \le  C \cdot   \parallel x_2 - x_1  \parallel _2
$$

Using this we calculate:

$$
\begin{aligned}
     &   \parallel  x_{n+2} - x_{n+1}   \parallel _2  \\
\leq\ &   \parallel x_{n+1} - x_{n}  \parallel _2 \cdot C \\
\leq\ & C^{n+1} \cdot C \cdot \delta \\
=\    & C^{n+2} \cdot \delta
\end{aligned}
$$

This implies (2).
\end{proof}

Take note that this proof does not demonstrate that $f(B_{\delta}(x_0))$ is open. Instead, it shows that there is a bijective $C^1$-function $f|_{f^{-1}(B_{\epsilon}(y_0)) } : f^{-1}(B_{\epsilon}(y_0)) \rightarrow B_{\epsilon}(y_0)$. 

* {#Rudin1976} [[Walter Rudin]], _Principles of Mathematical Analysis_, 3rd edition, International Series in Pure and Applied Mathematics, McGraw-Hill (1976).


