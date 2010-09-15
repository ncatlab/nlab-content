#Contents#
* automatic table of contents goes here
{:toc}

## Definition

Let $A$ be a [[abelian group|commutative]] ([[Hausdorff space|Hausdorff]]) [[topological group]]. A (continuous) *[[character]]* of $A$ is any continuous homomorphism $\chi: A\to S^1$. The __Pontrjagin dual group__ $\widehat{A}$ is the commutative group of all characters of $G$ with pointwise multiplication (that is multiplication induced by multiplication in the [[circle group]], the multiplication of norm-$1$ complex numbers in $S^1\subset\mathbb{C}$) and with the topology of [[uniform convergence]] on each [[compact space|compact]] $K\subset A$ (this is equivalent to the [[compact-open topology]]). 

For example, the Pontrjagin dual of the additive group of [[integer]]s $\mathbb{Z}$ is the circle group $S^1$, and conversely, $\mathbb{Z}$ is the Pontrjagin dual of $S^1$. This pairing of dual topological groups, given by $(n,z) \mapsto z^n$, is related to the subject of [[Fourier series]]. In general, the dual of a [[discrete space|discrete]] group is a [[compact space|compact]] group and conversely. The group $\hat{\mathbb{R}}$ is isomorphic again to $\mathbb{R}$ (the additive group of [[real numbers]]), with the pairing given by $(x,p) \mapsto \mathrm{e}^{\mathrm{i} x p}$; similarly, $\hat{\mathbb{R}^n}$ is isomorphic to the [[Cartesian space]] $\mathbb{R}^n$.

## Pontrjagin duality theorem

+-- {: .un_theorem}
###### Pontrjagin duality theorem
For every [[locally compact space|locally compact]] (Hausdorff) topological abelian group $A$, the natural function $A \mapsto \widehat{\widehat{A}}$ from $A$ into the Pontrjagin dual of the Pontrjagin dual of $A$, assigning to every $g\in A$ the continuous character $f_g$ given by $f_g(\chi)=\chi(g)$, is an [[isomorphism]] of topological groups (that is a group isomorophism that is also a [[homeomorphism]]). 
=--

Thus, the functor 

$$LocCompAb^{op} \to LocCompAb: G \to \widehat{G}$$ 

is an equivalence, in fact an adjoint equivalence whose unit 

$$A \to \widehat{\widehat{A}}: g \mapsto f_g$$ 

and whose counit (the same arrow read in the opposite category) are isomorphisms. This contravariant self-equivalence restricts to equivalences 

$$Ab^{op} \to CompAb$$

[ ] 

$$CompAb^{op} \to Ab$$ 

where $Ab$ is the category of (discrete topological) groups and $CompAb$ is the category of compact Hausdorff topological abelian groups, each embedded in $LocCompAb$ in the evident way. 

The [[Fourier transform]] on locally compact abelian groups is formulated in terms of Pontrjagin duals (see below). 

Also see:

* Michael Barr, On duality of topological abelian groups. ([PDF](ftp://ftp.math.mcgill.ca/pub/barr/pdffiles/abgp.pdf))

which provides a perhaps better context for Pontryagin duality than the category of locally compact Hausdorff abelian groups (also known as 'LCA groups').  Barr explains:

<blockquote>
Did you know that there is a [[star-autonomous category|*-autonomous category]] of topological abelian groups that includes all the LCA groups and whose duality extends that of Pontrjagin?  The groups are characterized by the property that among all topological groups on the same underlying abelian group and with the same set of continuous homomorphisms to the circle, these have the finest topology.  It is not obvious that such a finest exists, but it does and that is the key.
</blockquote>

## Properties of groups and their duals

There are many properties of locally compact Hausdorff abelian groups that implies properties of their Pontrjagin duals.  For example:

* If $A$ is finite, $\widehat{A}$  is finite.

* If $A$ is compact, $\widehat{A}$ is discrete.

* If $A$ is discrete, $\widehat{A}$  is compact.

* If $A$ is torsion-free and discrete, $\widehat{A}$ is connected and compact.

* If $A$ is connected and compact, $\widehat{A}$ is torsion-free and discrete.

* If $A$ is a Lie group, $\widehat{A}$ has finite rank.

* If A has finite rank, $\widehat{A}$ is a Lie group.

* If $A$ is second countable, $\widehat{A}$ is second countable.

* If $A$ is separable, $\widehat{A}$ is metrizable.

For a discussion of these facts, with some references, try:

* Variations on Pontryagin duality, ([nCafe](http://golem.ph.utexas.edu/category/2008/11/variations_on_pontryagin_duali.html))

* Sidney A. Morris, _Pontryagin Duality and the Structure of Locally Compact Abelian Groups_, London Math. Soc. Lecture Notes 29, Cambridge U. Press, 1977.

and this more advanced text:

* David A. Armacost, _The Structure of Locally Compact Abelian Groups_, Dekker, New York, 1981.

## Applications

Pontrjagin duality underlies the abstract framework of [[Fourier analysis]] on locally compact Hausdorff abelian groups $A$: by [[Fourier duality]] on $A$, there is a Hilbert space isomorphism (Fourier transform)

$$\mathcal{F}_A: L^2(A, d\mu) \to L^2(\hat{A}, d\hat{\mu})$$

where $d\mu$ is a suitable choice of [[Haar measure]] on $A$, and $d\hat{\mu}$ is a suitable choice of Haar measure on the dual group. Fourier duality is compatible with Pontrjagin duality in the sense that if $\hat{\hat{A}}$ is identified with $A$, then $\mathcal{F}_{\hat{A}}$ is the inverse of $\mathcal{F}_A$.

There is a recent categorification of the Pontrjagin duality theorem, motivated by applications to topological [[T-duality]]:

* Ulrich Bunke, Thomas Schick, Markus Spitzweck and Andreas Thom, Duality for topological abelian group stacks and T-duality.  ([arXiv](http://arxiv.org/abs/math/0701428))



[[!redirects Pontrjagin duality]]
[[!redirects Pontryagin dual]]
[[!redirects Pontryagin duality]]
[[!redirects Pontrjagin duality]]
[[!redirects Pontriagin dual]]
[[!redirects Pontriagin duality]]
[[!redirects Понтрягин dual]]
[[!redirects Понтрягин duality]]