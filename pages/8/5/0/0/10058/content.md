

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[quantum field theory]] of the [[scalar field]] $\Phi$, the canonical [[local observable|local]] [[interaction]] term is a [[Lagrangian density]] of the form

$$
  \mathbf{L}_{int}
  \;=\;
  \phi^n \, dvol_\Sigma
$$

(with notation as at _[[A first idea of quantum field theory]]_).

For $g_{sw} \in C^\infty_{cp}(\Sigma)$ any [[bump function]] on [[spacetime]], the corresponding [[adiabatic switching|adiabatically switched]] [[local observable]] is

$$
  \begin{aligned}
  S_{int}
  & =
  \underset{\Sigma}{\int}
  \underset{
     n \, \text{factors}
  }{
  \underbrace{
    \mathbf{\Phi}(x)
     \cdot
    \mathbf{\Phi}(x)
     \cdots
    \mathbf{\Phi}(x)
     \cdot
    \mathbf{\Phi}(x)
  }
  }
  \, 
  dvol_\Sigma(x)
  \\
  & =
  \underset{\Sigma}{\int}
  :
  \underset{
     n \, \text{factors}
  }{
  \underbrace{
    \mathbf{\Phi}(x)
    \mathbf{\Phi}(x)
      \cdots
    \mathbf{\Phi}(x)
    \mathbf{\Phi}(x)
  }
  }
  :
  \,
  dvol_\Sigma(X)
  \end{aligned}
  \,,
$$

where in the first line we have the [[integral]] over a pointwise product ([this def.](A+first+idea+of+quantum+field+theory#Observable)) of $n$ [[field observables]] ([this def.](A+first+idea+of+quantum+field+theory#PointEvaluationObservables)), which in the second line we write equivalently as a [[normal ordered product]], by the discusssion at _[[Wick algebra]]_ ([this def.](Wick+algebra#NormalOrderedProductNotation)).

The [[interacting field theory]] with [[Lagrangian density]] that of the [[free field|free]] [[scalar field]] plus interactions of the form $\phi^k$ as above, up to order $n$, is often called simply "$\Phi^n$-theory". 

## Examples


The [[mass]] term of the [[free field theory|free]] [[scalar field]] is a $\Phi^2$-interaction. 

The [[Higgs field]] involves a quadratic and quartic interaction of this form.

The potential for the [[inflaton field]] in [[chaotic cosmic inflation]] is a $\Phi^2$-interaction.

## Related concepts

* [[perturbative quantum field theory]]

* [[Higgs field]]

* [[inflaton field]]

## References

An introduction to $\Phi^4$ theory could be found in lecture 13 of

* Sourav Chatterjee, _Introduction to Quantum Field Theory for Mathematicians_, [pdf](https://statweb.stanford.edu/~souravc/qft-lectures-combined.pdf)

The [[weak adiabatic limit]] for [[mass]]-less $\Phi^4$ theory was established in 

* {#BlanchardSeneor75} P. Blanchard and R. Seneor, _Green’s functions for theories with massless particles (in perturbation theory)_, Ann. Inst. H. Poincaré Sec. A
23 (2), 147–209 (1975) ([Numdam](http://www.numdam.org/item?id=AIHPA_1975__23_2_147_0))

See also

* Wikipedia, _[Quartic interaction](http://en.wikipedia.org/wiki/Quartic_interaction)_

[[!redirects phi^n interactions]]

[[!redirects Phi^n interaction]]
[[!redirects Phi^n interactions]]

[[!redirects phi^2 interaction]]
[[!redirects phi^2 interactions]]

[[!redirects Phi^2 interaction]]
[[!redirects Phi^2 interactions]]

[[!redirects phi^3 interaction]]
[[!redirects phi^3 interactions]]

[[!redirects Phi^3 interaction]]
[[!redirects Phi^3 interactions]]

[[!redirects phi^n theory]]
[[!redirects phi^n theory]]

[[!redirects Phi^n theory]]
[[!redirects phi^n theory]]

[[!redirects phi^4 theory]]
[[!redirects phi^4 theory]]

[[!redirects Phi^4 theory]]
[[!redirects phi^4 theory]]

