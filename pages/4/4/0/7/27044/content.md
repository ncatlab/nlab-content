
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $G$ be a group, $\mathcal{O}_G$ its [[orbit category]], and $\mathcal{C}$ an [[∞-category]] (or, in particular, a [[category|1-category]]). 
\begin{definition}
  A **G-coefficient system valued in $\mathcal{C}$** is a functor $\mathcal{O}_G^{op} \rightarrow \mathcal{C}$.

\end{definition} 

## Examples

1. A version of [[Elmendorf's theorem]] states that the $\infty$-category of [[G-spaces]] is equivalent to $G$-coefficient systems in the $\infty$-category $\mathcal{S}$ of spaces. 

2. [[G-∞-categories]] are simply coefficient systems of [[∞-categories]].

3. Coefficient systems of sets and Abelian groups play a prominent role in [[equivariant homotopy theory]]; for instance, the [[equivariant homotopy groups]] $\pi_n^{\bullet}(-)$ form a coefficient system of [[set|sets]], for all $n$, which may be upgraded to [[groups]] when $n \geq 1$ and to [[abelian groups]] when $n \geq 2$. 

4. Coefficient systems of [[spectra]] are the [[stabilization]] of [[G-spaces]].

5. [[Mackey functors]] have underlying coefficient systems, given by pullback along the embedding $\mathcal{O}_G^{\op} \hookrightarrow \mathbb{F}_G^{\op} \hookrightarrow \mathrm{Span}(\mathbb{F}_G)$, the latter inclusion being the wide subcategory of backwards maps.