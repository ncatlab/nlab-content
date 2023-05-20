
\begin{example}
  The pushout product of two [[maps]] of sets
$$
  \array{
    f \; \colon & X &\longrightarrow& X'
    \\
    f \; \colon & Y &\longrightarrow& Y'
  }
$$
may be described as the [[quotient set]]
$$ 
  f \,\widehat{\times}\, g
  \;\;
  \simeq
  \;\;
  \big\{
  (x,y'),
  \,
  (x',y)
  \big\}_{
    \bigg/ 
    \Big(
      \big(x,\,g(y)\big) \,\sim\, \big(f(x),\,y\big)  
    \Big)
  }
$$
(where each variable ranges over the set denoted by the corresponding capital symbol).

Moreover, if we denote the equivalence class of $(x,y')$ by $[x,y']$, etc. then the pushout-product map itself is given as follows:
\[
  \label{ThePushoutProductMapForSets}
  \array{
    f \widehat{\times} g
    &\longrightarrow&
    X' \times Y'
    \\
    [x',\, y] &\mapsto& \big(x',\, g(y)\big)
    \\
    [x,\, y'] &\mapsto& \big(f(x),\, y' \big)
    \mathrlap{\,.}
  }
\]
More informatively, the [[fibers]] of this map over any $(x',y') \,\in\, X' \times Y'$ look as follows:
\[
  \label{FibersOfPushoutProductOfMapsOfSets}
  \big(
    f \widehat{\times} g
  \big)_{(x',y')}
  \;\;
  = 
  \;\;
  \left\{
  \array{
    \ast &\vert& (x',y') \;\in\; im(f) \times im(g)
    \\
    f^{-1}\big(\{x'\}\big)  &\vert& y' \;\in\; Y' \setminus im(g)
    \\
    g^{-1}\big(\{y'\}\big)  &\vert& x' \;\in\; X' \setminus im(f)
  }
  \right.
\]
\end{example}
\begin{proof}
We discuss in more detail how to obtain the fibers (eq:FibersOfPushoutProductOfMapsOfSets)

To see the first case: By the assumption that $x' \,\in\, im(f)$ we find $x_1 \in f^{-1}(\{x'\})$ and hence by (eq:ThePushoutProductMapForSets) we find $[x_1,y'] \,\in\, \big(f \widehat{\times} g\big)_{(x',y')}$. 

But since also $y' \,\in\, im(g)$ there is also $y \in g^{-1}(\{y'\})$ and hence
$$
  \big[x_1,\, y'\big] 
    \,=\, 
  \big[x_1,\, g(y)\big] 
    \,=\, 
  \big[f(x_1),\, y\big] 
    \,=\, 
  \big[x',\, y\big] 
  \,.
$$
So all elements of the form $[x,y']$ in the fiber are in fact equal, and also equal to $[x', y]$, which, by the symmetric argument, are in turn equal for all choices of $y$. Therefore there is one single element in the fiber.

To see the second case: Since $y'$ is not in the image of $g$, by (eq:ThePushoutProductMapForSets) the elements in the fiber can only be of the form $[x,y']$ with $x \in f^{-1}(\{x'\})$. None of these is contained in the relation, again by the assumption that $y'$ is not in the image of $g$, and hence they are all distinct.

The third case works the same way, under swapping $X \leftrightarrow Y$.
\end{proof}


