#Contents#
* automatic table of contents goes here
{:toc}

##Idea##

In as far as the simplicial $n$-[[simplex]] $\Delta^n$ (a [[simplicial set]]) is a combinatorial model for the $n$-ball, its _boundary_ $\partial \Delta^n$ is a combinatorial model for the $(n-1)$-[[sphere]].

##Definition##

The **boundary** $\partial \Delta^n$ of the simplicial $n$-[[simplex]] $\Delta^n$ is the simplicial set _generated_ from the simplicial set $\Delta^n$ minus its unique non-degenerate cell in dimension $n$.

Regarding $\Delta^n$ as the [[presheaf]] on on the [[simplex category]] that is [[representable functor|represented]] by $[n] \in Obj(\Delta)$, then this means that $\partial \Delta^n$ is the simplicial set generated from $\Delta$ minus the identity morphism $Id_{[n]}$.

There is a canonical [[monomorphism]]

$$
  i_n : \partial \Delta^n \hookrightarrow \Delta^n
  \,,
$$

the _boundary inclusion_ .

The [[geometric realization]] of this is the inclusion of the $(n-1)$-sphere as the boundary of the $n$-disk.

Simplicial boundary inclusions are one part of the [[cofibrantly generated model category|cofibrant generation]] of the classical [[model structure on simplicial sets]].


##Examples##

For low $n$ the boundaries of $n$-simplices look like (see also the illustrations at [[oriental]])

* $\partial \Delta^0 = \emptyset$;

* $\partial \Delta^1 = \partial\{0 \to 1\} = \{0, 1\} = \Delta^0 \sqcup \Delta^0$;

* $\partial \Delta^2 = 
   \partial\left\{
      \array{
        && 1
        \\
        & \nearrow &\Downarrow& \searrow
        \\
        0 &&\to&& 2
      } 
     \right\}
    =
   \left\{
      \array{
        && 1
        \\
        & \nearrow && \searrow
        \\
        0 &&\to&& 2
      } 
     \right\}    
  $


##Remarks##

* the closely related concept is that of [[horn]].