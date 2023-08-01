


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

__Adic spaces__ are the basic objects in Huber's approach to [[non-archimedean analytic geometry]]. They are built by gluing [[valuation spectra]] of a certain class of [[topological rings]]. Unlike [[Berkovich analytic spectra]] the points of adic spaces correspond to valuations of arbitrary rank, not only rank one. If a [[Berkovich space]] is corresponding to a separated [[rigid analytic space]] then it can be obtained as the largest Hausdorff quotient of the corresponding adic space.

The framework of adic spaces are used to build [[perfectoid spaces]] out of perfectoid rings.

## Definitions

\begin{definition}
Let $(A,A^{+})$ be a Huber pair, i.e. $A$ is a Huber ring and $A^{+}\subseteq A$ is a ring of integral elements. The _adic spectrum_ $\mathrm{Spa}(A,A^{+})$ is the set of equivalence classes of continuous valuations $\vert\cdot\vert$ on $A$ such that $\vert A^{+}\vert\leq 1$. 
\end{definition}

## Examples

* The final object in the category of adic spaces is $\mathrm{Spa}(\mathbb{Z},\mathbb{Z})$.

* The adic closed disc over $\mathbb{Q}_{p}$ is given by $\mathrm{Spa}(A,A^{+})$ where $A=\mathbb{Q}_{p}\langle T\rangle$ and $A^{+}=\mathbb{Z}_{p}\langle T\rangle$.

* The adic open disc over $\mathbb{Q}_{p}$ is the generic fiber of $\mathrm{Spa}(A,A)\to\mathrm{Spa}(\mathbb{Z}_{p},\mathbb{Z}_{p})$, where $A=\mathbb{Z}_{p}[[T]]$.

## Related concepts

* [[perfectoid space]]

* [[p-adic geometry]]

* [[analytic geometry]]

## References

* R. Huber, _Étale cohomology of rigid analytic varieties and adic spaces_, Aspects of Mathematics, E30. Friedr. Vieweg & Sohn, Braunschweig, 1996. x+450 pp. ([MR2001c:14046](http://www.ams.org/mathscinet-getitem?mr=1734903))

* [[Sophie Morel]], _Adic spaces_ ([pdf](https://web.math.princeton.edu/~smorel/adic_notes.pdf))

* Torsten Wedhorn, _Adic spaces_ ([arXiv:1910.05934](https://arxiv.org/abs/1910.05934))

* [[Brian Conrad]], _A brief introduction to adic spaces_, [PDF](http://virtualmath1.stanford.edu/~conrad/papers/Adicnotes.pdf).

[[!redirects adic spaces]]