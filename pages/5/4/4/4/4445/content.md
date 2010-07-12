
> under construction

#Contents#
* automatic table of contents goes here
{:toc}

## Definition

For $X_\bullet : \Delta^{op} \to $ [[Top]] a [[simplicial object]] [[topological space]], write $Sh(X_n)$ for the [[category of sheaves]] on (the [[category of open subsets]]) $X_n$.

The [[category]] $Sh(X_\bullet)$ of sheaves on the simplicial space is defined to be the category whose

* objects are 

  * collections $(S_n \in Sh(X_n))_n$

  * equipped for each $\alpha : [n] \to [m]$ with morphisms  

    $$
      S(\alpha) : Y(\alpha)^* S_n \to S_m
    $$ 

  * such that 

    * $S(Id_{[n]}) = Id_{S_n}$;

    * for every $\alpha : [n] \to [m]$ and $\beta : [m] \to [k]$
      the diagram

      $$
        \array{
          Y(\beta)^* Y(\alpha)^* S_n 
          &\stackrel{Y(\beta)^* S(\alpha)}{\to}& 
          Y(\beta)^* S_m
          \\
          {\mathllap{\simeq}}\downarrow && \downarrow^{\mathrlap{S(\beta)}}
          \\
          Y(\beta \alpha)^* S_m &\underset{S(\beta \alpha)}{\to}&
          S_k
        }
      $$

      [[commuting diagram|commutes]];

* morphisms are collections $(S_n \to T_n)$ of morphisms of sheaves, 
  compatible with all structure maps.


## Examples

For $C$ a [[topological category]] and $N C : \Delta^{op} \to Top$ its [[nerve]], $Sh(N_\bullet C)$ is the [[classifying topos]] for $C$-torsors. see [[classifying topos of a localic groupoid]].
