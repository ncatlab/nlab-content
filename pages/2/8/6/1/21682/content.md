


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Statement

+-- {: .num_prop } 
###### Proposition


Let $G$ be a [[finite number|finite]] [[dimension|dimensional]] [[simply connected topological space|simply connected]] [[compact Lie group]], with [[Lie algebra]] denoted $\mathfrak{g}$

Then the [[Sullivan minimal model]] of the [[classifying space]] $B G$ is the [[graded algebra]] 

$$
  inv^\bullet(\mathfrak{g})
  \; \coloneqq \;
  Sym 
  \big(
    \mathfrak{g}^\ast[2]
  \big)^G
$$

of [[invariant polynomials]] on $\mathfrak{g}$, equipped with vanishing [[differential]]:

$$
  \big(
    inv^\bullet(\mathfrak{g}), d = 0
  \big)
  \overset{\simeq}{\longrightarrow}
  CE
  \big(
    \mathfrak{l}
    B G
  \big)
  \,.
$$

=--

+-- {: .proof}
###### Proof

That the [[rational cohomology]] of $B G$ is given by $inv(\mathfrak{g})$ 

$$
  inv^\bullet(\mathfrak{g})
  \;\simeq\;
  H^\bullet
  \big(  
    B G,
    k
  \big)
$$

is due to [Chern 1950 (11)](#Chern50); [Bott 1973, p. 239 (5 of 15)](#Bott73).

(Here $k$ is the [[ground field]] of [[characteristic zero]]).

That the [[rational cohomology]] algebra of $B G$, with trivial differential, is the [[minimal Sullivan model]] for $B G$ is discussed for instance in [Félix, Oprea & Tanré 20 08](#FelixOpreaTanre08).

=--

## Related concepts

* [[Chern-Weil homomorphism]]

[[!include Sullivan models -- examples]]

## References

* {#Chern50} [[Shiing-shen Chern]], _Differential geometry of fiber bundles_, in: Proceedings of the International Congress of Mathematicians, Cambridge, Mass., (August-September 1950), vol. 2, pages 397-411,  Amer. Math. Soc., Providence, R. I. (1952) ([[Chern-DifferentialGeometryOfFiberBundles.pdf:file]], [full proceedings vol 2 pdf](https://www.mathunion.org/fileadmin/ICM/Proceedings/ICM1950.2/ICM1950.2.ocr.pdf))

* {#Bott73} [[Raoul Bott]], _On the Chern-Weil homomorphism and the continuous cohomology of Lie-groups_, Advances in Mathematics Volume 11, Issue 3, December 1973, Pages 289-303 (<a href="https://doi.org/10.1016/0001-8708(73)90012-1">doi:10.1016/0001-8708(73)90012-1</a>)

* {#FelixOpreaTanre08} [[Yves Félix]], [[John Oprea]], [[Daniel Tanré]], _Algebraic models in geometry_, Oxford University Press 2008 ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/tanre.pdf), [ISBN:9780199206520](https://global.oup.com/academic/product/algebraic-models-in-geometry-9780199206520))


[[!redirects Sullivan models of classifying spaces]]

[[!redirects Sullivan model of classifying space]]

