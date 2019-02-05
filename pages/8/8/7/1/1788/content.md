


+-- {: .num_example #ASimpleExample}
###### Example
**(equivariant degree-1 Cohomotopy of the circle)**

Let $G = \mathbb{Z}_2$ be the [[cyclic group]] of [[order of a group|order]] 2. Consider the [[circle]] 

$$
  S^1 
  \simeq 
  S(\mathbb{R}^2)
$$ 

equipped with the $\mathbb{Z}_2$-[[action]] whose [[involution]] element $\sigma$ [[reflection|reflects]] one of the two [[coordinate functions|coordinates]] of the ambient [[Cartesian space]] 

$$
  \sigma \;\colon\; (x_1,x_2) \mapsto (x_1, -x_2)
  \,.
$$

Equivalently, if we identify 

\[
  \label{CircleAsQuaotientOfRByZ}
  S^1
  \;\simeq\;
  \mathbb{R}/\mathbb{Z}
\]

then the involution action is

$$
  \begin{aligned}
    \sigma
    \;\colon\;
    t 
    \mapsto
    &
    \phantom{\sim}
    1 - t 
    \\
    & \sim
    \phantom{1} - t
  \end{aligned} 
  \,.
$$

This means that the [[fixed point space]] is the [[0-sphere]]

$$
  \big( S^1\big)^{\mathbb{Z}_2}
  \;\simeq\;
  S^0
$$

being two antipodal points on the circle, which in the presentation (eq:CircleAsQuaotientOfRByZ) are labeled $\{0,1/2\} \simeq S^0$.

Notice that the map

$$
  \array{
    S^1 &\overset{n}{\longrightarrow}& S^1
    \\
    t &\mapsto& n\cdot t
  }
$$

of constant parameter speed and [[winding number]] $n \in \mathbb{N}$ is equivariant for this $\mathbb{Z}_2$-[[action]] on both sides:

\begin{center}
\begin{xymatrix}
  t 
    \ar@{|->}[r] 
    \ar@{|->}[d]_{\sigma}
    & 
  n\cdot t
    \ar@{|->}[d]^{\sigma}
  \\
  -t 
    \ar@{|->}[r] 
    & 
  -n \cdot t
\end{xymatrix}
\end{center}

Take this circle to be both the [[domain]] space $X$ as well as the [[coefficient]] [[n-sphere|1-sphere]].

By Prop. \ref{EquivariantPT} the equivariant homotopy classes of maps $S^1 \to S^1$ correspond to [[submanifolds]] of $S^0$ of [[codimension]] 0 with respect to $S^0$, but equivariantly framed with respect to the ambient $S^1$ -- hence in lowest degree simply of [[subsets]] of $S^0$. 

Indeed, under passage to [[fixed points]] any

$$
  S^1 \overset{f}{\longrightarrow} S^1 
$$

induces a map

$$
  S^0 
    \overset{
      \big( f\big)^{\mathbb{Z}_2}
    }{\longrightarrow} 
  S^0
  \simeq \{0,1\}
$$

and we may regard this as encoding the [[subset]] of $S^0$ which is the [[preimage]] of the chosen non-[[basepoint]] $1 \in S^0$.

Hence

1. the [[empty set|empty]] subset $\varnothing \subset S^0$ corresponds to the [[constant function]] $S^1 \to \{0\} \hookrightarrow S^1$;

1. the full subset $S^0 = S^0$ corresponds to the [[constant function]] $S^1 \to \{1\} \hookrightarrow S^1$;

1. the intermediate subset $\{1\} \subset S^0$ corresponds to the [[identity function]] $S^1 \overset{id}{\longrightarrow} S^1$.

Notice that it is only the last case that is homotopically non-trivial after forgetting the equivariance.

(...)

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
