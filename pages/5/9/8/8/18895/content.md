

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Given [[Lagrangian field theory]] with [[field bundle]] $E \overset{fb}{\to} \Sigma$ over some [[spacetime]] $\Sigma$, so that a [[field history]] is a smooth [[section]] $\Phi \in \Gamma_\Sigma(E)$, then for every point $x \in \Sigma$ (every [[event]]) and every [[coordinate function]] $\phi^a \in C^\infty(E\vert_{U_x}$) on the [[fibers]] of $E$ over a [[neighbourhood]] of $X$ there is the [[observable]]

$$ 
  \mathbf{\Phi}^a(x)
  \;\colon\;
  \Gamma_\Sigma(E)
    \longrightarrow
  \mathbb{C}
$$

which reads out the value of that component of the [[field history]] $\Phi$ at that point ([[event]]) 

$$
  \mathbf{\Phi}^a(x) \;\colon\; \Phi \mapsto \Phi^a(x)
  \,.
$$

Hence in the case that $E$ is a [[vector bundle]], then under the identification of [[linear observables]] with [[distributions]] ([this prop.](geometry+of+physics+--+A+first+idea+of+quantum+field+theory#LinearObservablesAreTheCompactlySupportedDistributions)), these field observable are the [[Dirac delta distributions]].

[[!include perturbative observables -- table]]

In general such $\mathbf{\Phi}^a(x)$ itself is far from being [[on-shell]] [[gauge invariance|gauge invariant]] and hence far from being an element in the [[BV-BRST cohomology]] of the theory. But since most observables that are may be expressed as algebraic combinations of these "point evaluation observables" they are of particular interest. Since they manifestly reflect the value of [[field histories]], it is common to terminologically conflate the field observables $\mathbf{\Phi}^a(x)$ with "the fields" of the field theory.

## Related entries

* [[operator product expansion]]

* [[A first idea of quantum field theory]], [this example](geometry+of+physics+--+A+first+idea+of+quantum+field+theory#PointEvaluationObservables)

[[!redirects field observables]]

[[!redirects point-evaluation observable]]
[[!redirects point-evaluation observables]]

[[!redirects point-evaluation field observable]]
[[!redirects point-evaluation field observables]]

