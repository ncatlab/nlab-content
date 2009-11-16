#Contents#
* automatic table of contents goes here
{:toc}

##Idea##

The _horn_ $\Lambda_k[n] = \Lambda^n_k \hookrightarrow \Delta^n$ is the [[simplicial set]] obtained from the [[boundary of a simplex|boundary of the n-simplex]] $\partial \Delta^n$ of the standard simplicial $n$-[[simplex]] $\Delta^n$ by discarding the $k$th face.

##Definition##

Let 

$$
  \Delta[n] = \mathbf{\Delta}( -, [n]) \in  Simp Set
$$

be the standard simplicial $n$-[[simplex]] in [[SimpSet]].

Then, for each $i$, $0 \leq i \leq n$, we can form, within $\Delta[n] $, a subsimplicial set, $\Lambda^i[n]$, called the **$(n,i)$-horn** or **$(n,i)$-box**, by discarding the top dimensional non-degenerate $n$-simplex (given by the identity map on $[n]$) and its $i^{th}$ face.  We must also discard all the degeneracies of those simplices.

The horn $\Lambda^k[n]$ is an **outer horn** if $k = 0$ or $k = n$.

##Examples##

The inner horn of the 2-simplex 

$$\Delta^2 =    
  \left\{
      \array{
        && 1
        \\
        & \nearrow &\Downarrow& \searrow
        \\
        0 &&\to&& 2
      } 
     \right\}
$$

with boundary 

$$\partial \Delta^2 =   \left\{
      \array{
        && 1
        \\
        & \nearrow && \searrow
        \\
        0 &&\to&& 2
      } 
     \right\}
$$ 

looks like

$$ 
\Lambda^2_1
  =
   \left\{
      \array{
        && 1
        \\
        & \nearrow && \searrow
        \\
        0 &&&& 2
      } 
     \right\}
$$

The two outer horns look like

$$\Lambda^2_0 =   
\left\{
      \array{
        && 1
        \\
        & \nearrow && 
        \\
        0 &&\to&& 2
      } 
     \right\}
$$ 

and

$$\Lambda^2_2 =   
\left\{
      \array{
        && 1
        \\
        & && \searrow
        \\
        0 &&\to&& 2
      } 
     \right\}
$$ 

respectively. 

##Relation to other concepts##

* A [[Kan fibration]] is a morphism of simplicial sets which has the right [[lifting property]] with respect to all horn inclusions $\Lambda^k[n] \hookrightarrow \Delta^n$.

* A [[Kan complex]] is a simplicial set in which "*all horns have fillers*": a simplicial set for which the morphism to the point is a Kan fibration.

* A [[quasi-category]] is a simplicial set in which *all inner* horns have fillers*.

[[!redirects horns]]