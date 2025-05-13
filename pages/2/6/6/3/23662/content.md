+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A *modulus of convergence* is a function that tells how quickly a convergent [[sequence]] or [[net]] converges inside of a suitable [[Cauchy space]], such as a [[metric space]] or [[uniform space]]. 

## Definition 

The precise definition varies with the context.

In the [[real numbers]], a __modulus of convergence__ for a [[sequence]] or [[net]] $(x_i)_i$  is a function $\alpha$ from the positive numbers to the [[natural numbers]] (for sequences) or the [[directed set]] (for nets) such that almost all terms are within $\epsilon$ of one another. Explicitly:
$$ \forall \epsilon,\; \forall i, j \geq \alpha(\epsilon),\; |x_i - x_j| \lt \epsilon .$$

In a [[metric space]], a __modulus of convergence__ for a sequence or net $(x_i)_i$ is a function $\alpha$ from the positive numbers to the natural numbers (for sequences) or the directed set (for nets) that satisfies the same condition, now relative to the metric $d$ on that space.  Explicitly:
$$ \forall \epsilon,\; \forall i, j \geq \alpha(\epsilon),\; d(x_i,x_j) \lt \epsilon .$$

In a [[gauge space]], a __modulus of convergence__ for a sequence or net $(x_i)_i$ is a function $\alpha$ from the positive numbers to the natural numbers (for sequences) or the directed set (for nets) that satisfies this condition for each gauging distance separately. Explicitly:
$$ \forall d,\; \forall \epsilon,\; \forall i, j \geq \alpha(\epsilon),\; d(x_i,x_j) \lt \epsilon .$$

In a [[premetric space]], a __modulus of convergence__ for a sequence or net $(x_i)_i$ is a function $\alpha$ from the positive numbers to the natural numbers (for sequences) or the directed set (for nets) that satisfies the same condition, now relative to the premetric. Explicitly:
$$ \forall \epsilon,\; \forall i, j \geq \alpha(\epsilon),\; x_i \sim_\epsilon x_j .$$

In a [[uniform space]], a __modulus of convergence__ for a sequence or net $(x_i)_i$ is a function $\alpha$ from the set of entourages to the natural numbers (for sequences) or the directed set (for nets) if an analogous condition is satisfied for each [[entourage]] $U$. Explicitly:
$$ \forall U,\; \forall i, j \geq \alpha(U),\; x_i \approx_U x_j .$$

The most general space for which a modulus of convergence can be defined is a set $X$ with an auxiliary set $T$ and a ternary relation $R(x, y, t)$ for $x, y \in X$ and $t \in T$. In such a space, a __modulus of convergence__ for a sequence or net $(x_i)_i$ is a function $\alpha$ from the auxiliary set to the natural numbers (for sequences) or the directed set (for nets) that satisfies the same condition for each element of the auxiliary set, now relative to the ternary relation. Explicitly:
$$ \forall t,\; \forall i, j \geq \alpha(t),\; R(x_i, x_j, t) .$$

## Related concepts

* [[sequence]], [[net]]
* [[Cauchy sequence]], [[Cauchy net]]
* [[limit of a sequence]], [[limit of a net]]
* [[metric space]], [[gauge space]], [[uniform space]]
* [[Cauchy structure]]
* [[Cauchy approximation]]
* [[HoTT book real numbers]]

## References 

* Wikipedia, *[Modulus of convergence](https://en.wikipedia.org/wiki/Modulus_of_convergence)*

* {#Booij20} [[Auke Booij]], *Analysis in Univalent Type Theory* (2020) &lbrack;[etheses:10411](http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf), [[Booij-AnalysisInUF.pdf:file]]&rbrack;

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

[[!redirects modulus of convergence]]
[[!redirects moduli of convergence]]

[[!redirects modulus of Cauchy convergence]]
[[!redirects moduli of Cauchy convergence]]