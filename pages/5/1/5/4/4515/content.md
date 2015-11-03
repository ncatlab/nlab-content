
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

### Original version for associative algebras

The **formality theorem** by [[Maxim Kontsevich]] (arXiv 1997) states that there is an [[L-∞-algebra]] [[quasi-isomorphism]] from the [[dg-Lie algebra]] of [[polyvector field]]s (with zero differential and [[Schouten-Nijenhuis bracket]]) to the [[dg-Lie algebra]] of the shifted [[Hochschild cohomology|Hochschild cochain complex]] (with Hochschild differential and Gerstenhaber bracket), whose first Taylor coefficient is the [[Hochschild-Kostant-Rosenberg theorem|HKR]] quasi-isomorphism.

Tamarkin alternatively proves the formality of the [[little disks operad]] (see also Kontsevich 1999) and proves that it implies the Kontsevich formality. 

The Kontsevich formality theorem implies that every [[Poisson manifold]] has a [[deformation quantization]], unique up to an element in the freely-acting piece of the [[automorphism infinity-group]] of the [[E1-operad]]. This is the [[Grothendieck-Teichmüller group]] (see there for more).

### General version for higher $E_n$-algebras

More generally, a result of Kontsevich and Tamarkin (...) says that over a [[field]] of [[characteristic]] 0 the canonical functor

$$
  E_n Algbras \stackrel{\simeq}{\longrightarrow} P_n Algebras
$$

from [[E-n algebras]] to [[Poisson n-algebras]] is an [[equivalence]] (since $P_n$ is the [[homology]] of $E_n$, this says that _The $E_n$" operad is formal_ over a field of characteristic 0. 

But of course the [[automorphism infinity-group]] of both $E_n$ and $P_n$ acts on both sides and makes the space of all possible such equivalences a [[torsor]] over this group. A $P_n$ algebra may be thought of as encoding a [[prequantum field theory]] of higher dimension, of sors, and so formality says that the [[deformation quantization]] of [[factorization algebras]] always exists and that the choices are being acted on by the corresponding higher analog of the [[Grothendieck-Teichmüller group]].



## Related entries

* [[graph complex]]

* [[deformation quantization]], [[Grothendieck-Teichmüller group]]

* [Hochschild cohomology -- Differential calculus](Hochschild+cohomology#DifferentialCalculus).

## References

* [[Maxim Kontsevich]], _Deformation quantization of Poisson manifolds_, [q-alg/9709040](http://arxiv.org/abs/q-alg/9709040), Lett. Math. Phys. __66__ (2003), no. 3, 157&#8211;216 [doi](http://dx.doi.org/10.1023/B:MATH.0000027508.00421.bf); _Operads and motives in deformation quantization_, Lett. Math. Phys. __48__ (1999), no. 1, 35&#8211;72.
* Dmitry E. Tamarkin, _Another proof of M. Kontsevich formality theorem_, [math.QA/9803025](http://arxiv.org/abs/math/9803025); _Formality of chain operad of little discs_, Lett. Math. Phys. __66__ (1-2):65&#8211;72, 2003.
* [[Bernhard Keller]], _Notes for an
Introduction to Kontsevich's quantization theorem_, [pdf](www.math.jussieu.fr/~keller/publ/emalca.pdf)
* Dan Petersen, _Minimal models, GT-action and formality of the little disk operad_, [arxiv/1303.1448](http://arxiv.org/abs/1303.1448)
* Damien Calaque, Carlo A. Rossi, _Lectures on Duflo isomorphisms in Lie algebra and complex geometry_, European Math. Soc. 2011 [MPI pdf](http://people.mpim-bonn.mpg.de/crossi/LectETHbook.pdf)
* [[Vladimir Hinich]], _Tamarkin's proof of Kontsevich's formality theorem_, [math.QA/0003052](http://arxiv.org/abs/math/0003052)
* Vasily Dolgushev, _All coefficients entering Kontsevich's formality quasi-isomorphism can be replaced by rational numbers_, [arxiv/1306.6733](http://arxiv.org/abs/1306.6733)
* [[Damien Calaque]], Thomas Willwacher, _Triviality of the higher Formality Theorem_, [arxiv/1310.4605](http://arxiv.org/abs/1310.4605)

In agreement with Tsygan's philosophy of noncommutative differential calculus and its relations to braces algebra, Willwacher extends the Kontsevich formality to a homotopy braces morphism and to a $G_\infty$-morphism in

* Thomas Willwacher, _A note on Br-infinity and KS-infinity formality_, [arxiv/1109.3520](http://arxiv.org/abs/1109.3520)


category: algebra, geometry

[[!redirects Kontsevich formality theorem]]
[[!redirects Tamarkin formality]]