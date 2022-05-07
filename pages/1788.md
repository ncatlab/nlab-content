
In formulas in [[thermodynamics]] it is often the (multiplicative) inverse of the [[temperature]] $T$ that is the natural [[variable]], then traditionally abbreviated

$$
  \beta
  \;\coloneqq\;
  \frac{1}{k T}
  \,,
$$

where $k$ denotes the [[Boltzmann constant]], a [[physical unit]] which for purposes of pure mathematics may be identified with unity and hence omitted from the formula.

This inverse temperature appears, in particular, in the formula for the [[Boltzmann distribution]], which is the [[probability distribution]] such that the [[probability density]] for a [[physical system]] to be in a [[state]] with [[energy]] $E$ is proportional to the [[exponential]] of $E$ weighted by minus the inverse temperature:

$$
  d p \;=\; e^{- \beta E} \, d E
  \,.
$$

Essentially a special case of this is the formula for the [[heat kernel]] on a [[Riemannian manifold]], which is an [[integral kernel]] proportial to the [[exponential]] of the Riemannian [[distance]] squared and again weightted by minus the inverse temperature.

$$
  K_{Heat}(x,y) \;\propto\; e^{  - \beta d(x,y)^2 }
  \,.
$$

Extrapolating from this case, the scale of the exponent in various [[kernel method|kernels]] may often be understood as akin to inverse temperature.

Finally, when understanding [[thermal field theory|thermal]]/[[Euclidean field theory]] as the result of [[Wick rotation]] of [[relativistic field theory]] (when possible), the inverse temperature $\beta$ is proportional to the [[radius]] of the "thermal circle" on which the [[Euclidean field theory]] must be understood to be [[Kaluza-Klein compactification|KK-compactified]], see [there](Euclidean+field+theory#TemporalCompactificationToThermalRelativisticFieldTheory) for more.

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





