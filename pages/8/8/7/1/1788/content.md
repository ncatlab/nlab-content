
$$
  \begin{array}{ll}  
    xx
    \\
    \hline
    yy
  \end{array}
$$

§



\begin{tikzcd}
b_{ij}
\;\;
  :=
\;\;
\color{orange}
\left[
\color{black}
\raisebox{5pt}{
\begin{tikzpicture}[yscale=1, xscale=1.3]

\draw[line width=1.4]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);


\begin{scope}[shift={(-1.4,0)}]
\draw[line width=1.4]
  (-.3,1) to (-.3,-1);
\draw[line width=1.4]
  (+.4,1) to (+.4,-1);
\draw
  (+.05,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\begin{scope}[shift={(-0,0)}]
\draw[line width=1.4]
  (-.6,1) to (-.6,-1);
\draw[line width=1.4]
  (-.4,1) to (-.4,-1);
\draw[line width=4, white]
  (+.4,1) to (+.4,-1);
\draw[line width=1.4]
  (+.4,1) to (+.4,-1);
\draw[line width=4, white]
  (+.2,1) to (+.2,-1);
\draw[line width=1.4]
  (+.2,1) to (+.2,-1);
\draw
  (-.1,-.1) node {$\mathclap{\cdots}$};
\end{scope}


\begin{scope}[shift={(+.8,0)}]
\draw[line width=1.4]
  (-.4,1) to (-.4,-1);
\draw[line width=1.2]
  (+.3,1) to (+.3,-1);
\draw
  (-.01,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\draw[line width=4, white]
  (-.8,-1)
  .. controls   (-.8, -.5)  and (.55, -.5)  ..
  (.55,0);
\draw[line width=1.4]
  (-.8,-1)
  .. controls   (-.8, -.5)  and (.55, -.5)  ..
  (.55,0);

\begin{scope}
\clip
  (-.9,0) rectangle (+.3,1.2); 
\draw[line width=4, white]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);
\draw[line width=1.4]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);
\end{scope}

\draw
  (-.8,-1.3) node {
    \scalebox{.7}{
      \color{blue}
      $i$
    }
  };

\draw
  (+.4,-1.3) node {
    \scalebox{.7}{
      \color{blue}
      $j$
    }
  };

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\;\;
=
\;\;
\color{orange}
\left[
\color{black}
\raisebox{5pt}{
\begin{tikzpicture}[yscale=-1, xscale=-1.3]

\draw[line width=1.4]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);


\begin{scope}[shift={(-1.4,0)}]
\draw[line width=1.4]
  (-.3,1) to (-.3,-1);
\draw[line width=1.4]
  (+.4,1) to (+.4,-1);
\draw
  (+.05,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\begin{scope}[shift={(-0,0)}]
\draw[line width=1.4]
  (-.6,1) to (-.6,-1);
\draw[line width=1.4]
  (-.4,1) to (-.4,-1);
\draw[line width=4, white]
  (+.4,1) to (+.4,-1);
\draw[line width=1.4]
  (+.4,1) to (+.4,-1);
\draw[line width=4, white]
  (+.2,1) to (+.2,-1);
\draw[line width=1.4]
  (+.2,1) to (+.2,-1);
\draw
  (-.1,-.1) node {$\mathclap{\cdots}$};
\end{scope}


\begin{scope}[shift={(+.8,0)}]
\draw[line width=1.4]
  (-.4,1) to (-.4,-1);
\draw[line width=1.2]
  (+.3,1) to (+.3,-1);
\draw
  (-.01,-.1) node {$\mathclap{\cdots}$};
\end{scope}

\draw[line width=4, white]
  (-.8,-1)
  .. controls   (-.8, -.5)  and (.55, -.5)  ..
  (.55,0);
\draw[line width=1.4]
  (-.8,-1)
  .. controls   (-.8, -.5)  and (.55, -.5)  ..
  (.55,0);

\begin{scope}
\clip
  (-.9,0) rectangle (+.3,1.2); 
\draw[line width=4, white]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);
\draw[line width=1.4]
  (.55,0)
  .. controls (.55, +.5) and (-.8, +.5) ..
  (-.8,+1);
\end{scope}

\draw
  (-.8,+1.3) node {
    \scalebox{-.7}{
      \color{blue}
      $j$
    }
  };

\draw
  (+.4,+1.3) node {
    \scalebox{-.7}{
      \color{blue}
      $i$
    }
  };

\end{tikzpicture}
}
\color{orange}
\right]
\color{black}
\end{tikzcd}



## Definition in an additive category

Let $\mathcal{C}$ be an [[additive category]]; that is, $\mathcal{C}$ is enriched over [[abelian groups]]. For $A, B$ a [[pair]] of objects in $\mathcal{C}$, a biproduct ((#MacLane) p.194) is an object $A \oplus B$ together with maps

\begin{tikzcd}
A \arrow[rr, "i_{1}"', shift right] &  & A \oplus B \arrow[ll, "p_{1}"', shift right] \arrow[rr, "p_{2}", shift left] &  & B \arrow[ll, "i_{2}", shift left]
\end{tikzcd}

which satisfy the identities

$$
i_{1};p_{1}=1_{a}, \quad i_{2};p_{2}=1_{b}, \quad p_{1};i_{1} + p_{2};i_{2}
$$