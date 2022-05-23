e finito

\linebreak

\linebreak

\linebreak


***


\section{Idea}

Expositions of [[topological data analysis]] traditionally invoke *point clouds* -- [[discrete space|discrete]] [[subsets]] of some [[metric space]] --  as the generic mathematical incarnation of datasets to be analyzed. 

Maybe a more realistic and more encompassing model for sets of observed data -- namely for *measurement results* -- is the time-honored notion of a tuple of (values of) *[[real number|real]] [[observables]]*, namely a [[continuous function]]

$$
  Obs
  \;\colon\;
  X 
  \xrightarrow{\phantom{---}}
  \mathbb{R}^n
$$

to the [[one-point compactification]] of $n$-[[dimension of a vector space|dimensional]] [[Cartesian space]].

A feature in the data as seen by such an observable is then an [[isosurface]] of $Obs$, hence the [[pre-image]] 

$$
  Obs^{-1}(\vec v) 
  \;\coloneqq\;
  \Big\{
    x \in X
    \,\big\vert\,
    Obs(x) = \vec v
  \Big\}
  \;\subset\; X
$$ 

of a [[tuple]] $\vec v \in \mathbb{R}^n$ of observed values.

Without restriction of generality we may assume that the observed value of interest is the origin $0 \in \mathbb{R}^n$, for if it is instead some $\vec v \in \mathbb{R}^n$ then we may instead pass to the observable $Obs \coloneqq Obs - const_{\vec v}$ without changing the essence of the situation.

In practice, the value of an observable can never be determined with the accuracy of a mathematical point in $\mathbb{R}^n$, instead there will be some [[positive number|positive]] [[real number]] $r \in \mathbb{R}_{\gt 0}$ such that one may hope (or wish) to measure $Obs$ up to measurement errors within a [[radius]] $r$. In this case, the desired [[isosurface]] could be any element in the set

$$
  \Big\{
    f^{-1}(0)
    \subset 
    X
    \,\vert\,
    f \in C^0(X,\mathbb{R}^n)
    ,\,
    \Vert f - Obs \Vert_\infty \lt r
  \Big\}
$$



For example, $X$ might model the interior of a plasma container (say a fusion reactor) and $Ob = (T, p) : X \to \mathbb{R}^2$ could be the combined [[temperature]]- and [[pressure]]-observable (say as seen by laser probes into the plasma). Its [[isosurfaces]] are the [[intersections]] of given [[isobars]] with [[isotherms]].


***

Illustrating the main theorem of persistent Cohomotopy.
 {#MainTheoremPersistentCohomotopy}


\begin{tikzpicture}


\begin{scope}

\draw[line width=1pt]
  (-4, 0)
  to
  (4,0);

\draw
  (-4.3,0)
  node
  {
    \colorbox{white}{$X$}
  };

\begin{scope}

\draw[gray, densely dashed]
  (-4, .5)
  to
  (4,.5);
  
\draw[gray, densely dashed]
  (-4, 1)
  to
  (4,1);
  
\draw[gray, densely dashed]
  (-4, 1.5)
  to
  (4,1.5);  

\draw[gray, densely dashed]
  (-4, 2)
  to
  (4,2);   
  
\draw[gray, densely dashed]
  (-4, 2.5)
  to
  (4,2.5);    
  
\draw[red, line width=2pt, densely dashed]
  (-4, 3)
  to
  (4,3);    

\draw[fill=red, fill opacity=.3, draw opacity=0]
  (4,3)
  rectangle
  (-4,4);
  
\draw[gray, densely dashed]
  (-4, 3.5)
  to
  (4,3.5);      
 
\draw[gray, densely dashed]
  (-4, 4)
  to
  (4,4);      
  
\end{scope}  
 
 
\begin{scope}[yscale=-1]

\draw[gray, densely dashed]
  (-4, .5)
  to
  (4,.5);
  
\draw[gray, densely dashed]
  (-4, 1)
  to
  (4,1);
  
\draw[gray, densely dashed]
  (-4, 1.5)
  to
  (4,1.5);  

\draw[gray, densely dashed]
  (-4, 2)
  to
  (4,2);   
  
\draw[gray, densely dashed]
  (-4, 2.5)
  to
  (4,2.5);    
  
\draw[red, line width=2pt, densely dashed]
  (-4, 3)
  to
  (4,3);  
  
\draw[fill=red, fill opacity=.3, draw opacity=0]
  (4,3)
  rectangle
  (-4,4);
  
  
\draw[gray, densely dashed]
  (-4, 3.5)
  to
  (4,3.5);      
 
\draw[gray, densely dashed]
  (-4, 4)
  to
  (4,4);      
  
\end{scope}   

\draw[white, line width=7pt] 
  plot[smooth]
  coordinates
  {
    (-4,-3.9)
    (-3.5, -3.7)
    (-3.1, -3)
    (-2.5, -2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  
  
\draw plot[smooth]
  coordinates
  {
    (-4,-3.9)
    (-3.5, -3.7)
    (-3.1, -3)
    (-2.5, -2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  
\draw[gray, densely dashed]
 (2.7,-.1) to (2.7,1);

\draw
  (2.7,-.3)
  node
  {\scalebox{1}{$x$}};

\draw (4.4, 1)
 node
 {\scalebox{1}{$f(x)$}};

\draw (4.3, 3)
 node
 {\scalebox{1}{$r$}};

\draw (4.3, -3)
 node
 {\scalebox{1}{$-r$}};
 

\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (-4,-4) 
    rectangle
  (-3.05, 4);
  
\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (+4,-4) 
    rectangle
  (+3.7, 4);
  
\end{scope}



%%%%%%%%%%%%%%%


\begin{scope}[yshift=-9cm]


\begin{scope}
\clip
  (-3.05,3)
  rectangle
  (3.7, -2.98);






\draw[white, line width=7pt] 
  plot[smooth]
  coordinates
  {
    (-4,-3.9)
    (-3.5, -3.7)
    (-3.1, -3)
    (-2.5, -2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  
  
\draw plot[smooth]
  coordinates
  {
    (-4,-3.9)
    (-3.5, -3.7)
    (-3.1, -3)
    (-2.5, -2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  


\draw (4.4, 1)
 node
 {\scalebox{1}{$f(x)$}};

\draw (4.3, 3)
 node
 {\scalebox{1}{$r$}};

\draw (4.3, -3)
 node
 {\scalebox{1}{$-r$}};
 

\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (-4,-4) 
    rectangle
  (-3.05, 4);
  
\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (+4,-4) 
    rectangle
  (+3.7, 4);

\end{scope}  

\draw
  (.4, 3.5)
  node
  {$ 
    \color{blue}
    X/\mathrm{gray} \;=\; S^1
  $};

\draw
  (.4, -3.5)
  node
  {$ 
    \color{blue}
    X/\mathrm{gray} \;=\; S^1
  $};
  
\draw
  (4.2, .1)
  node[rotate=90]
  {$ 
    \color{blue}
    \mathbb{R}/\mathrm{red}
    \;=\; S^1
  $};  
  
\draw
  (-3.6, .1)
  node[rotate=90]
  {$ 
    \color{blue}
    \mathbb{R}/\mathrm{red}
    \;=\; S^1
  $};    

\draw[red, line width=2pt, draw opacity=.5]
  (-3.05,3)
  to
  (3.7, 3);

\draw[red, line width=2pt, draw opacity=.5]
  (-3.05,-2.98)
  to
  (3.7, -2.98);

\draw[line width=2pt]
  (-3.05, 3) to (-3.05, -2.98);

\draw[line width=2pt]
  (3.7, 3) to (3.7, -2.98);


\draw[red, ->, line width=2pt, draw opacity=.5]
  (.4-.1,3)
  to
  (.4+.1, 3);

\draw[red, ->, line width=2pt, draw opacity=.5]
  (.4-.1,-2.98)
  to
  (.4+.1, -2.98);

\draw[->, line width=2pt]
  (3.7,.3-.1)
  to
  (3.7,.3+.1);
  
\draw[->, line width=2pt]
  (-3.05,.3-.1)
  to
  (-3.05,.3+.1);
  
\draw
  (1.1,-1.2)
  node
  {$
    \underset{
      \raisebox{-2pt}{
        \small
        \color{blue}
        unit winding
      }
    }{
    [f] = {\color{purple}+1} \in \pi^1(S^1)
    }
  $};

\draw[fill=gray, draw=gray]
  (-3.05,3)
  circle (.08);

\draw[fill=gray, draw=gray]
  (-3.05,-2.98)
  circle (.08);
  
\draw[fill=gray, draw=gray]
  (3.7,3)
  circle (.08);  

\draw[fill=gray, draw=gray]
  (3.7,-2.98)
  circle (.08);
  


\end{scope}


\begin{scope}[xshift=10cm]

\draw[line width=1pt]
  (-4, 0)
  to
  (4,0);

\draw
  (-4.3,0)
  node
  {
    \colorbox{white}{$X$}
  };

\begin{scope}

\draw[gray, densely dashed]
  (-4, .5)
  to
  (4,.5);
  
\draw[gray, densely dashed]
  (-4, 1)
  to
  (4,1);
  
\draw[gray, densely dashed]
  (-4, 1.5)
  to
  (4,1.5);  

\draw[gray, densely dashed]
  (-4, 2)
  to
  (4,2);   
  
\draw[gray, densely dashed]
  (-4, 2.5)
  to
  (4,2.5);    
  
\draw[red, line width=2pt, densely dashed]
  (-4, 3)
  to
  (4,3);    

\draw[fill=red, fill opacity=.3, draw opacity=0]
  (4,3)
  rectangle
  (-4,4);
  
\draw[gray, densely dashed]
  (-4, 3.5)
  to
  (4,3.5);      
 
\draw[gray, densely dashed]
  (-4, 4)
  to
  (4,4);      
  
\end{scope}  
 
 
\begin{scope}[yscale=-1]

\draw[gray, densely dashed]
  (-4, .5)
  to
  (4,.5);
  
\draw[gray, densely dashed]
  (-4, 1)
  to
  (4,1);
  
\draw[gray, densely dashed]
  (-4, 1.5)
  to
  (4,1.5);  

\draw[gray, densely dashed]
  (-4, 2)
  to
  (4,2);   
  
\draw[gray, densely dashed]
  (-4, 2.5)
  to
  (4,2.5);    
  
\draw[red, line width=2pt, densely dashed]
  (-4, 3)
  to
  (4,3);  
  
\draw[fill=red, fill opacity=.3, draw opacity=0]
  (4,3)
  rectangle
  (-4,4);
  
  
\draw[gray, densely dashed]
  (-4, 3.5)
  to
  (4,3.5);      
 
\draw[gray, densely dashed]
  (-4, 4)
  to
  (4,4);      
  
\end{scope}   

\draw[white, line width=7pt] 
  plot[smooth]
  coordinates
  {
    (-4,+3.9)
    (-3.5, +3.7)
    (-3.1, +3)
    (-2.5, +2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  
  
\draw plot[smooth]
  coordinates
  {
    (-4,+3.9)
    (-3.5, +3.7)
    (-3.1, +3)
    (-2.5, +2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  
\draw[gray, densely dashed]
 (2.7,-.1) to (2.7,1);

\draw
  (2.7,-.3)
  node
  {\scalebox{1}{$x$}};

\draw (4.4, 1)
 node
 {\scalebox{1}{$f(x)$}};

\draw (4.3, 3)
 node
 {\scalebox{1}{$r$}};

\draw (4.3, -3)
 node
 {\scalebox{1}{$-r$}};
 

\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (-4,-4) 
    rectangle
  (-3.05, 4);
  
\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (+4,-4) 
    rectangle
  (+3.7, 4);
  
\end{scope}



%%%%%%%%%%%%%%%


\begin{scope}[xshift=10cm, yshift=-9cm]


\begin{scope}
\clip
  (-3.05,3)
  rectangle
  (3.7, -2.98);






\draw[white, line width=7pt] 
  plot[smooth]
  coordinates
  {
    (-4,+3.9)
    (-3.5, +3.7)
    (-3.1, +3)
    (-2.5, +2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  
  
\draw plot[smooth]
  coordinates
  {
    (-4,+3.9)
    (-3.5, +3.7)
    (-3.1, +3)
    (-2.5, +2.5)
    (-2,-1)
    (-1.6, 0)
    (-1.2, +.6)
    (-.7, +1)
    (-.1, -.7)
    (.8, -.2)
    (1.4, +.4)
    (2, +.7)
    (3,+1.2)
    (3.5, 2)
    (3.7, 3)
    (4,3.4)
  };
  


\draw (4.4, 1)
 node
 {\scalebox{1}{$f(x)$}};

\draw (4.3, 3)
 node
 {\scalebox{1}{$r$}};

\draw (4.3, -3)
 node
 {\scalebox{1}{$-r$}};
 

\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (-4,-4) 
    rectangle
  (-3.05, 4);
  
\draw[fill=gray, fill opacity=.3, draw opacity=0]
  (+4,-4) 
    rectangle
  (+3.7, 4);

\end{scope}  

\draw
  (.4, 3.5)
  node
  {$ 
    \color{blue}
    X/\mathrm{gray} \;=\; S^1
  $};

\draw
  (.4, -3.5)
  node
  {$ 
    \color{blue}
    X/\mathrm{gray} \;=\; S^1
  $};
  
\draw
  (4.2, .1)
  node[rotate=90]
  {$ 
    \color{blue}
    \mathbb{R}/\mathrm{red}
    \;=\; S^1
  $};  
  
\draw
  (-3.5, .1)
  node[rotate=90]
  {$ 
    \color{blue}
    \mathbb{R}/\mathrm{red}
    \;=\; S^1
  $};    

\draw[red, line width=2pt, draw opacity=.5]
  (-3.05,3)
  to
  (3.7, 3);

\draw[red, line width=2pt, draw opacity=.5]
  (-3.05,-2.98)
  to
  (3.7, -2.98);

\draw[line width=2pt]
  (-3.05, 3) to (-3.05, -2.98);

\draw[line width=2pt]
  (3.7, 3) to (3.7, -2.98);


\draw[red, ->, line width=2pt, draw opacity=.5]
  (.4-.1,3)
  to
  (.4+.1, 3);

\draw[red, ->, line width=2pt, draw opacity=.5]
  (.4-.1,-2.98)
  to
  (.4+.1, -2.98);

\draw[->, line width=2pt]
  (3.7,.3-.1)
  to
  (3.7,.3+.1);
  
\draw[->, line width=2pt]
  (-3.05,.3-.1)
  to
  (-3.05,.3+.1);
  
\draw
  (1.1,-1.2)
  node
  {$
    \underset{
      \raisebox{-2pt}{
        \small
        \color{blue}
        trivial winding
      }
    }{
    [f] = {\color{purple}0} \in \pi^1(S^1)
    }
  $};


\draw[fill=gray, draw=gray]
  (-3.05,3)
  circle (.08);

\draw[fill=gray, draw=gray]
  (-3.05,-2.98)
  circle (.08);
  
\draw[fill=gray, draw=gray]
  (3.7,3)
  circle (.08);  

\draw[fill=gray, draw=gray]
  (3.7,-2.98)
  circle (.08);


\end{scope}

\end{tikzpicture}

Suppose we want to know the zeros of the observable $f$. If the resolution/error bar of measuring $f$ is $r$, then we know 
that 

1. the zeros must be somewhere away from the gray region.

1. the homotopy class of $f$ on the quotient determines the number of zeros mod 2.


