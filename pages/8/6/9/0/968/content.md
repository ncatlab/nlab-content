A **cyclic set** is a [[presheaf]] on a particular category $\Lambda$ defined by Connes (which we might call the [[cycle category]]), which is intermediate between a [[symmetric set]] and a [[simplicial set]].

The [[geometric shapes for higher structures|shape]] category for simplicial sets (the [[simplex category]]) can be identified with the full subcategory of $Cat$ on the finite nonempty ordinals $[n]$.  Likewise, the shape category for symmetric sets ([[FinSet]]) can be identified with the full subcategory of $Cat$ on their [[localization]]s $[n]^{-1}[n]$.  The shape category $\Lambda$ is the full subcategory on the categories obtained by localizing each $[n]$ by only inverting the full cycle, that is the composition $0\to 1\to\ldots\to n$.

+--{: .query}
[[Mike Shulman|Mike]]: I copied (and attempted to clarify) the above from [[symmetric set]], but I don't think I believe it.  If you invert the composite $0\to 1\to 2$ in $[2]$, then the objects $0$ and $2$ become isomorphic and are both a retract of $1$.  This localization has exactly one nondegenerate, nonidentity self-map, which exchanges $0$ and $2$.  But shouldn't the object "$2$" in $\Lambda$ have a $\mathbb{Z}/3$ worth of self-maps?
=--
