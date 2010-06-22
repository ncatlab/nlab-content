
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _fat simplex functor_ is a [[cosimplicial object|cosimplicial]] [[simplicial set]]

$$
  \mathbf{\Delta} : \Delta \to sSet
$$

whose value $\mathbf{\Delta}[n]$ at $n \in \mathbb{N}$ is a [[simplicial set]] that models the $n$-[[simplex]] but is much bigger than the standard $n$-simplex $\Delta[n] = Hom_{\Delta}(-,[n])$. This is such that $\mathbf{\Delta}[-]$ is a cofibrant replacement of $*$ and of $\Delta[-] = Hom_\Delta(-,-)$ in the projective [[model structure on functors]] $\Delta \to sSet_{Quillen}$.

The fat simplex can be used to express the [[homotopy colimit]] over [[simplicial object|simplicial]] [[diagram]]s in terms of [[coend]]s of the form $\int^{[n] \in \Delta} \mathbf{\Delta}[n] \cdot F_n$. This construction is originally due to Bousfield and Kan. 

## Definition

Write $\Delta$ for the [[simplex category]]. For $[n] \in \Delta$ write $\Delta/[n]$ for the corresponding [[overcategory]]. Finally write $

$$
  \mathbf{\Delta}[n] :=
  N(\Delta/[n]) 
$$ 

(in [[sSet]]) for the [[nerve]] of this overcategory. 


This construction is [[functor]]ial in  $[n]$:

$$
  \mathbf{\Delta}(-) =  N(\Delta/(-)) : \Delta \to sSet
  \,.
$$

## Examples

* The fat 0-simplex is $\mathbf{\Delta}[0] = N(\Delta)$, the [[nerve]] of 
  the [[simplex category]] (because $[0] \in \Delta$ is the 
  [[terminal object]]).


## Properties

There is a canonical morphism

$$
  \mathbf{\Delta} \to \Delta
$$

of [[cosimplicial object|cosimplicial]] [[simplicial set]], called the
[[Bousfield-Kan map]].

This exhibits $\mathbf{\Delta}$ as a cofibrant replacement of $\Delta$ and of $*$ in the projective [[model structure on functors]] on $[\Delta, sSet_{Quillen}]$.


[[!redirects fat simplices]]