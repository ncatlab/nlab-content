#Idea#

A _skyscraper sheaf_ is a [[sheaf]] supported at a single point.

This is not unlike the Dirac $\delta$-distribution.

#Definition#

For $X$ a [[topological space]], $x \in X$ a point of $x$ and $S \in Set$ a [[set]], the **skyscraper sheaf** $skyscr_x(S) \in Sh(X)$ in the [[category of sheaves]] on the [[category of open subsets]] $Op(X)$ of $X$ supported at $x$ with value $S$ is the [[sheaf]] of sets given by the assignment

$$
  skysc_x(S) : (U \subset X) \mapsto
  \left\{
    \array{
      S & if x \in U
      \\
      {*} & otherwise
    }
  \right.
$$

## Remarks ##

* The skyscraper sheaf $skysc_x(S)$ is the [[direct image]] of $S$ under the [[geometric morphism]] $x : Set \to Sh(X)$ which defines the [[point of a topos]] given by $x \in X$ (see there for more details on this perspective).

