[[!redirects comodule spectra]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Dual to the concept of a [[module spectrum]] over a [[ring spectrum]] is a _comodule spectrum_ over a [[coring spectrum]], the analog in [[stable homotopy theory]] of the concept of [[comodules]] in [[algebra]] and [[homological algebra]].

## Properties

### Over suspension spectra
 {#OverSuspensionSpectra}

The [[suspension spectrum]] $\Sigma^\infty X = \mathbb{S}[X]$ of any [[∞-groupoid]] ([[homotopy type]] of a  [[topological space]]) $X$ is canonically a [[coring spectrum]] by the fact that every $X$, is uniquely a [[coalgebra object]] in the [[Cartesian monoidal (∞,1)-category]] [[∞Grpd]] via the [[codiagonal]] ([here](cartesian+monoidal+infinity%2C1-category#CoalgebraObjects)), and using that $\Sigma^\infty$ is a [[strong monoidal functor]].

If $X$ is [[connected object in an (∞,1)-topos]] (the homotopy type of a [[connected topological space]]) then $\mathbb{S}[X]$-comodule spectra are equivalently [[module spectra]] over the [[∞-group ∞-ring]] $\mathbb{S}[\Omega X]$ of the [[loop space]] [[∞-group]] of $X$.

$$
   CoModSpectra_{\mathbb{S}[X]}
  \;\simeq\;
   ModSpectra_{\mathbb{S}[\Omega X]}
$$


([Hess-Shipley 14, theorem 1.2 with prop. 5.18](#HessShipley14))

See also at _[[A-theory]]_.


## Related concepts


## References

* {#HessShipley14} [[Kathryn Hess]], [[Brooke Shipley]], _Waldhausen K-theory of spaces via comodules_, Advances in Mathematics 290 (2016): 1079-1137 ([arXiv:1402.4719](https://arxiv.org/abs/1402.4719))
 