# Restricted Yoneda embedding

* table of contents
{: toc}

## Definition

For any [[functor]] $i:A\to C$ (often the inclusion of a [[full subcategory]]), the **restricted Yoneda embedding** is the composite

$$ C \hookrightarrow [C^{op},Set] \xrightarrow{i^\ast} [A^{op},Set] $$

of the ordinary [[Yoneda embedding]] of $C$ with the restriction functor $i^\ast$ along $i$.

When $C$ is cocomplete, the restricted Yoneda embedding has a left adjoint: the [[nerve and realization|realization]].

One important example of a restricted Yoneda embedding is that of the fully faithful inclusion $i : \Delta \hookrightarrow Cat$, where $\Delta$ is the [[simplex category]]. This is known as the [[nerve functor]].

## Related pages

* [[Yoneda embedding]]
* [[dense subcategory]]
* [[nerve]]
