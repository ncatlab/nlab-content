
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

Given a [[separable Hilbert space]] $\mathcal{H}$, such as the [[sequence space]] $\mathcal{l}_2$, write $B(\mathcal{H})$ for its [[C*-algebra]] of [[bounded linear operators]] and $D(\mathcal{H})$ for the subalgebra of diagonal operators.

The _Kadison-Singer problem_ is the question:

_Does every [[pure state]] $\psi$ on $D(\mathcal{H})$ [[extension|extend]] to a [[state]] $\rho$ on $B(\mathcal{H})$?_



$$
  \array{
     D(\mathcal{H}) &\overset{\psi}{\longrightarrow}& \mathbb{C}
     \\
     \downarrow  & \nearrow_{\mathrlap{\exists \rho}}
     \\
     B(\mathcal{H}) 
  }
$$

This was proven to be the case in [Marcus-Spielman-Srivastava 13](#MarcusSpielmanSrivastava13).

## Related entries


Other theorems about the foundations and [[interpretation of quantum mechanics]] include:

* [[order-theoretic structure in quantum mechanics]]

  * [[Kochen-Specker theorem]]

  * [[Alfsen-Shultz theorem]]

  * [[Harding-Döring-Hamhalter theorem]]

* [[Fell's theorem]]

* [[Gleason's theorem]]

* [[Wigner theorem]]

* [[Bell's theorem]]

* [[Bub-Clifton theorem]]


## References

The problem was stated in

* [[Richard V. Kadison]], [[Isadore Singer]], _Extensions of pure states_, American Journal of Mathematics, 81(2):383&#8211;400, 1959 ([jstor:2372748](https://www.jstor.org/stable/2372748))

and its solution was proven in

* {#MarcusSpielmanSrivastava13} Adam Marcus, Daniel A. Spielman, and Nikhil Srivastava, _Interlacing Families II: Mixed Characteristic Polynomials and The Kadison-Singer Problem, 2013. ([arXiv:1306.3969](https://arxiv.org/abs/1306.3969))

Review includes

* Nicholas Harvey, _An introduction to the Kadison-Singer conjecture and the paving conjecture_ ([pdf](http://www.cs.ubc.ca/~nickhar/Publications/KS/KS.pdf))

