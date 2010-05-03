#Contents#
* automatic table of contents goes here
{:toc}

## Definition

Let $G$ be a [[abelian group|commutative]] ([[Hausdorff space|Hausdorff]]) [[topological group]]. A (continuous) *[[character]]* of $G$ is any continuous homomorphism $\chi:G\to S^1$. The __Pontrjagin dual group__ $\hat{G}$ is the commutative group of all characters of $G$ with pointwise multiplication (that is multiplication induced by multiplication in the [[circle group]], the multiplication of norm-$1$ complex numbers in $S^1\subset\mathbb{C}$) and with the topology of [[uniform convergence]] on each [[compact space|compact]] $K\subset G$ (this is equivalent to the [[compact-open topology]]). 

For example, the Pontrjagin dual of the additive group of [[integer]]s $\mathbb{Z}$ is the circle group $S^1$, and conversely, $\mathbb{Z}$ is the Pontrjagin dual of $S^1$. This pairing of dual topological groups, given by $(n,z) \mapsto z^n$, is related to the subject of [[Fourier series]]. In general, the dual of a [[discrete space|discrete]] group is a [[compact space|compact]] group and conversely. The group $\hat{\mathbb{R}}$ is isomorphic again to $\mathbb{R}$ (the additive group of [[real numbers]]), with the pairing given by $(x,p) \mapsto \mathrm{e}^{\mathrm{i} x p}$; similarly, $\hat{\mathbb{R}^n}$ is isomorphic to the [[Cartesian space]] $\mathbb{R}^n$.

## Pontrjagin duality theorem

+-- {: .un_theorem}
###### Pontrjagin duality theorem
For every [[locally compact space|locally compact]] (Hausdorff) topological abelian group $G$, the natural function $G\mapsto \widehat{\widehat{G}}$ of $G$ into the Pontrjagin dual of the Pontrjagin dual of $G$, assigning to every $g\in G$ the continuous character $f_g$ given by $f_g(\chi)=\chi(g)$, is an [[isomorphism]] of topological groups (that is a group isomorophism that is also a [[homeomorphism]]). 
=--

Thus, the functor 

$$LocCompAb^{op} \to LocCompAb: G \to \widehat{G}$$ 

is an equivalence, in fact an adjoint equivalence whose unit 

$$G \to \widehat{\widehat{G}}: g \mapsto f_g$$ 

and whose counit (the same arrow read in the opposite category) are isomorphisms. This contravariant self-equivalence restricts to equivalences 

$$Ab^{op} \to CompAb$$

[ ] 

$$CompAb^{op} \to Ab$$ 

where $Ab$ is the category of (discrete topological) groups and $CompAb$ is the category of compact Hausdorff topological abelian groups, each embedded in $LocCompAb$ in the evident way. 

The [[Fourier transform]] on locally compact abelian groups is formulated in terms of Pontrjagin duals (see below). 

There is a recent categorification of the Pontrjagin duality theorem by U. Bunke and T. Schick, motivated by applications to topological [[T-duality]]. 

## Applications

Pontrjagin duality underlies the abstract framework of [[Fourier analysis]] on locally compact Hausdorff abelian groups $G$: by [[Fourier duality]] on $G$, there is a Hilbert space isomorphism (Fourier transform)

$$\mathcal{F}_G: L^2(G, d\mu) \to L^2(\hat{G}, d\hat{\mu})$$

where $d\mu$ is a suitable choice of [[Haar measure]] on $G$, and $d\hat{\mu}$ is a suitable choice of Haar measure on the dual group. Fourier duality is compatible with Pontrjagin duality in the sense that if $\hat{\hat{G}}$ is identified with $G$, then $\mathcal{F}_{\hat{G}}$ is the inverse of $\mathcal{F}_G$.

[[!redirects Pontrjagin duality]]
[[!redirects Pontryagin dual]]
[[!redirects Pontryagin duality]]
[[!redirects Pontrjagin duality]]
[[!redirects Pontriagin dual]]
[[!redirects Pontriagin duality]]
[[!redirects Понтрягин dual]]
[[!redirects Понтрягин duality]]