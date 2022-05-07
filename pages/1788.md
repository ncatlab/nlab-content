

Notice that every [[permutation]] $\sigma$ has a *unique* representative in cycle notation 

\[
  \label{NormalizedCycleNotation}
  \begin{aligned}
    \sigma
    & = \;
    (h_1 t_{11} t_{12} \cdots)
    (h_2 t_{21} t_{22} \cdots)
    (h_3 t_{31} t_{32} \cdots)
    \cdots 
    \\
    & =
    \vert
    h_1 t_{11} t_{12} \vert
    h_2 t_{21} t_{22} \vert
    h_3 t_{31} t_{32} \vert \cdots 
  \end{aligned}
\]

with the property that the following two conditions hold:

1. heads are smallest in their cycle: $h_i \lt t_{i j}$,

1. cycles are ordered by their heads: $h_i \lt h_{i + 1}$. 

This way we get a [[bijection]] between the set of permutations and the set of [[sections]] $sec$ of the following [[indexed family]] of sets

$$
  \array{
    \underset{
      k \in \{1, \cdots, n\}  
    }{\sqcup}
    \{0, \cdots, k-1\}
    \\
    {}^{\mathllap{p_n}}
    \big\downarrow
    \;
    \big\uparrow {}^{\mathrlap{sec}}
    \\
    \{1, \cdots, n\}
  }
$$

as follows:

To a given section $sec$, assign the permutation whose normalized cycle notation (eq:NormalizedCycleNotation) has underlying it the list obtained by setting

$$
  list_0
  \;\coloneqq\;
  \varnothing
$$

and then recursively adding the element $k+1$ to the list at stage $k$ by 

* either appending it on the right if $sec(k+1) = 0$;

* or inserting it *after* the $sec(k+1)$-st element already in the list:

$$
  list_{k+1}
  \;\coloneqq\;
  \left\{
  \array{
    [ list_k, k+1 ] &if& sec(k+1) = 0
    \\
    [ list_k^{ \leq sec(k+1)}, k+1 , list_k^{\gt sec(k+1)} ]
    & if & sec(k+1) \gt 0 
  }
  \right.
$$

The resulting $list_n$ with a bar "$\vert$" inserted right before each element $k$ with $sec(k) = 0$ is a normalized cycle notation (eq:NormalizedCycleNotation) for a permutation, and every such arises this way uniquely.

Now the number of cycles of the permutation is the number of times that the corresponding section $sec$ takes the value 0. Therefore we have:

$$
  \begin{aligned}
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  e^{\beta \cdot \left\vert Cycles(\sigma) \right\vert}
  & = \;
  \underset{
    sec \in \Gamma(p_n)
  }{\sum}
  e^{ \beta \cdot \left\vert sec^{-1}(0) \right\vert }
  \\
  & = \;
  \underset{
    sec \in \Gamma(p_n)
  }{\sum}
  \underoverset
    {k = 1}
    {n}
    {\prod} 
  \left\{
  \array{
    e^{\beta} &\vert& sec(k) = 0
    \\
    1 &\vert& otherwise
  }  
  \right.
  \\
  & = \;
  \underoverset
    {k = 1}
    {n }
    {\prod}
  \;
  \underset{
    sec(k) \in \{0, \cdots, k-1\}
  }{\sum}
  \;
  \left\{
  \array{
    e^{\beta} &\vert& sec(k) = 0
    \\
    1 &\vert& otherwise
  }  
  \right.
  \\
  & = \;
  \underoverset
    {k = 1}
    {n  }
    {\prod}
  \;
  \big(
     e^{\beta}
     +
     (k-1)
  \big)
  \\
  & =
  \underoverset
    {k = 0}
    {n -1 }
    {\prod}
  \;
  \big(
     e^{\beta}
     +
     k
  \big)
  \end{aligned}
$$





