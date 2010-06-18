
<div class="rightHandSide toc">
[[!include topos theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Definition

For $\mathbf{H}$ a [[topos]] (or [[(∞,1)-topos]], etc.) and for $X \in \mathbf{H}$ an [[object]], also the [[overcategory]] $\mathbf{H}_{/X}$ is a topos ($(\infty,1)$-topos, etc). This is sometimes called the [[gros topos]] associated to $X \in \mathbf{H}$.

The canonical projection $\pi_! : \mathbf{H}_{/X} \to \mathbf{H}$ is part of an [[essential geometric morphism]]

$$
  \pi = (\pi_! \dashv \pi^* \dashv \pi_*) : 
  \mathbf{H}_{/X}
   \stackrel{\overset{\pi_!}{\to}}{\stackrel{\overset{\pi^*}{\leftarrow}}{\underset{\pi_*}{\to}}}
  \mathbf{H}
  \,.
$$

**Definition**

A [[geometric morphism]] $\mathbf{K} \to \mathbf{H}$ that factors as $\mathbf{K} \to \mathbf{H}_{/X} \stackrel{\pi}{\to} \mathbf{H}$ for some $X \in \mathbf{H}$ is called an **etale geometric morphism**.

The terminology is motivated from the special case that $\mathbf{H}$ is a [[localic topos]] $Sh(S)$ over a [[topological space]] $S$ we have that $X \in Sh(S)$ corresponds to an [[etale space]] over $X$.

## References

For [[(infinity,1)-topos]]es this is in section 6.3.5 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects etale geometric morphism]]
[[!redirects etale geometric morphisms]]
[[!redirects étale geometric morphism]]
[[!redirects étale geometric morphisms]]
