+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An **exponentiable morphism** (sometimes called a **powerful morphism**) $f \colon A \to B$ in a [[category]] $\mathcal{C}$ is a [[morphism]] that is [[exponentiable object|exponentiable]] as an [[object]] of the [[slice category]] $\mathcal{C}/B$. When [[pullbacks]] along $f$ exist, giving rise to a [[base change]] functor $f^* : \mathcal{C}/B \to \mathcal{C}/A$, this is equivalent to asking for $f^*$ to have a [[right adjoint]] $\Pi_f : \mathcal{C}/A \to \mathcal{C}/B$ (called the *[[dependent product]]*), whose [[universal property]] is explicitly described by that of a [[distributivity pullback]]. However, one can consider exponentiability even in the absence of pullbacks.

## Relation to exponentiable objects

If $\mathcal{C}$ has a [[terminal object]] and $X$ is an object in $\mathcal{C}$, then if the unique morphism $!_X : X \to 1$ is exponentiable, then, for every object $Y$ for which the [[product]] $X \times Y$ exists, the [[exponentiable object]] $Y^X$ exists and is given by $\Pi_{!_X} (\pi_1 \colon X \times Y \to X)$.

Conversely, suppose $\mathcal{C}$ has a terminal object and $X$ is an [[exponentiable object]] in $\mathcal{C}$. Let $f \colon Z \to X$ be a morphism. If the following pullback exists, it exhibits the exponential morphism $\Pi_{!_X} f$.
\begin{tikzcd}
	{\Pi_{!_X} A} & {Z^X} \\
	1 & {X^X}
	\arrow[from=1-1, to=1-2]
	\arrow["{\Pi_{!_X} f}"', from=1-1, to=2-1]
	\arrow["\lrcorner"{anchor=center, pos=0.125}, draw=none, from=1-1, to=2-2]
	\arrow["{f^X}", from=1-2, to=2-2]
	\arrow["{\lambda(1_X)}"', from=2-1, to=2-2]
\end{tikzcd}

Consequently, in a category with [[finite limits]], an object $X$ is an [[exponentiable object]] if and only if $!_X : X \to 1$ is an exponentiable morphism.

## Properties

- If $C$ has equalizers of coreflexive pairs, then any pullback of an exponentiable morphism is exponentiable.  This follows from the [[adjoint triangle theorem]], since the left adjoint $\Sigma_f$ of pullback is [[comonadic functor|comonadic]].

## Examples

- [[Conduche functor|Exponentiable functors]] are characterised by a factorisation property.

- The exponentiable morphisms in $Top$ were characterized by [Niefield](#Niefield82). In particular, a subspace inclusion $C \to D$ is exponentiable if and only if $C$ is [[locally closed]].

- The exponentiable morphisms in $Locale$ and $Topos$ which are embeddings were also characterized by [Niefield](#Niefield81). It seems that no complete characterization of exponentiable morphisms in $Locale$ or $Topos$ appears in the literature.

## Related concepts

- A category is [[locally cartesian closed]] precisely when it has all [[pullbacks]] and in which every morphism is exponentiable.

- The [[universal property]] of $\Pi_f$ is described by a [[distributivity pullback]], at least when pullbacks along $f$ exist.

- The [[type theory|type theoretic]] interpretation of exponential morphisms is the [[dependent product]].

- [[exponentiable object]]

## References

* [[Susan Niefield]], *Cartesianness*, PhD thesis, Rutgers 1978 ([proquest:302920643](https://www.proquest.com/docview/302920643))

* {#Niefield81} [[Susan Niefield]], _Cartesian inclusion: locales and toposes._, Communications in Algebra, 9.16, 1981, pp. 1639-1671  ([doi:10.1080/00927878108822672](https://doi.org/10.1080/00927878108822672))

* {#Niefield82} [[Susan Niefield]], _Cartesianness: topological spaces, uniform spaces, and affine schemes._, Journal of Pure and Applied Algebra, 23.2, 1982, pp. 147-167.(<a href="https://doi.org/10.1016/0022-4049(82)90004-4">doi:10.1016/0022-4049(82)90004-4</a>, [pdf](https://core.ac.uk/download/pdf/81936509.pdf))

* {#Weber} [[Mark Weber]], _Polynomials in categories with pullbacks_, [arXiv](http://arxiv.org/abs/1106.1983), [TAC](http://tac.mta.ca/tac/volumes/30/16/30-16abs.html)
 

[[!redirects exponentiable morphisms]]
[[!redirects exponential morphism]]
[[!redirects exponential morphisms]]
[[!redirects powerful morphism]]
[[!redirects powerful morphisms]]