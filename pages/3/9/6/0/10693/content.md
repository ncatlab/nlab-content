
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $p$ a [[prime number]] and $X$ a [[topological space]], 
an _Adams resolution_ is a [[free resolution]] of the [[cohomology ring]] $H^\bullet(X,\mathbb{Z}_p)$ by a [[chain complex]] of [[free modules]] over the [[Steenrod algebra]] $A_p$. Specifically it is such a resolution of the form

$$
  \array{
    H^\bullet(K_0) &\leftarrow& H^\bullet(\Sigma K_1) &\leftarrow& H^\bullet(\Sigma^2 K_2)  &\leftarrow& \cdots
    \\
    \downarrow && \downarrow && \downarrow
    \\
    H^\bullet(X)
    &\leftarrow& 0
    &\leftarrow& 0    
   &\leftarrow&  \cdots  
  }
$$

where each $K_i$ is a wedge product/[[smash product]] of [[suspensions]] of $E = H \mathbb{Z}/(p)$, the mod $p$ [[Eilenberg-MacLane spectrum]].

The computaton of the [[cohomology]] of $X$ by means of this resolution is given by the [[Adams spectral sequence]].

## Related concepts

* [[Whitehead tower]]

## References

Around Chapter 2, def. 2.1.3 of 

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_

[[!redirects Adams resolutions]]