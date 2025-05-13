[[!redirects Cauchy approximations]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

\tableofcontents

## Idea

A *Cauchy approximation* is a [[function]] which behaves as the [[composition]] of a [[regular Cauchy sequence]] with its [[modulus of convergence]]. 

## Definition 

The original notion of a *Cauchy approximation* first defined in [Booij 2020](#Booij20) uses the rational numbers. 

A function $x$ from the positive rational numbers to the [[real numbers]] is a __Cauchy approximation__ if for all positive rational numbers $\delta$ and $\epsilon$, the distance between $x_\delta$ and $x_\epsilon$ is less than $\delta + \epsilon$. Explicitly: 
$$ \forall \delta, \epsilon,\; |x_\delta - x_\epsilon| \lt \delta + \epsilon .$$

In a [[metric space]] $S$, a function $x$ from the positive rational numbers to $S$ is a __Cauchy approximation__ under the same condition, now relative to the metric $d$ on that space. Explicitly:
$$ \forall \delta, \epsilon,\; d(x_\delta,x_\epsilon) \lt \delta + \epsilon .$$

In a [[gauge space]] $S$, a function $x$ from the positive rational numbers to $S$ is a __Cauchy approximation__ if this condition is satisfied for each gauging distance separately. Explicitly:
$$ \forall d,\; \forall \delta, \epsilon,\; d(x_\delta,x_\epsilon) \lt \delta + \epsilon .$$

In a [[rational premetric space|rational]] or [[real premetric space]] $S$, a function $x$ from the positive rational numbers to $S$ is a __Cauchy approximation__ if this condition is satisfied for the premetric. Explicitly:
$$ \forall \delta, \epsilon,\; x_\delta \sim_{\delta + \epsilon} x_\epsilon .$$

## Properties 

Every Cauchy approximation is a [[Cauchy net]] indexed by the positive rational numbers $\mathbb{Q}_{+}$. 

A Cauchy approximation is the composition $x \circ M$ of a [[net]] $x$ and a rational [[modulus of convergence]] $M$. 

## Real Cauchy approximations

For [[metric spaces]] and [[gauge spaces]], since the [[modulus of convergence]] of [[regular Cauchy sequences]] usually uses the positive real numbers rather than the positive rational numbers, one can use the positive [[real numbers]] instead of the positive [[rational numbers]] as the domain of the Cauchy approximation, yielding a notion of a _real Cauchy approximation_. The original notion of a Cauchy approximation can then be called a _rational Cauchy approximation_.

A function $x$ from the positive real numbers to the [[real numbers]] is a __real Cauchy approximation__ if for all positive rational numbers $\delta$ and $\epsilon$, the distance between $x_\delta$ and $x_\epsilon$ is less than $\delta$ and $\epsilon$. Explicitly: 
$$ \forall \delta, \epsilon,\; |x_\delta - x_\epsilon| \lt \delta + \epsilon .$$

In a [[metric space]] $S$, a function $x$ from the positive real numbers to $S$ is a __real Cauchy approximation__ under the same condition, now relative to the metric $d$ on that space. Explicitly:
$$ \forall \delta, \epsilon,\; d(x_\delta,x_\epsilon) \lt \delta + \epsilon .$$

In a [[gauge space]] $S$, a function $x$ from the positive real numbers to $S$ is a __real Cauchy approximation__ if this condition is satisfied for each gauging distance separately. Explicitly:
$$ \forall d,\; \forall \delta, \epsilon,\; d(x_\delta,x_\epsilon) \lt \delta + \epsilon .$$

In a [[real premetric space]] $S$, a function $x$ from the positive real numbers to $S$ is a __real Cauchy approximation__ if this condition is satisfied for the ternary relation. Explicitly:
$$ \forall \delta, \epsilon,\; x_\delta \sim_{\delta + \epsilon} x_\epsilon .$$

## Limits of Cauchy approximations

Similar to limits of [[Cauchy sequences]], one can define the limit of Cauchy approximations. The definition of a limit are the same for both rational and real Cauchy approximations. 

Given a Cauchy approximation $x$, a [[real number]] $c$ is a __limit__ of $x$ if for all positive rational numbers $\epsilon$ and $\theta$, the distance between $x_\epsilon$ and $c$ is less than $\epsilon + \theta$. Explicitly: 
$$ \forall \epsilon, \theta,\; |x_\epsilon - c| \lt \epsilon + \theta .$$

In a [[metric space]] $S$, given a Cauchy approximation $x$, an element $c$ in $S$ is a __limit__ of $x$ under the same condition, now relative to the metric $d$ on that space. Explicitly:
$$ \forall \epsilon, \theta,\; d(x_\epsilon,c) \lt \epsilon + \theta .$$

In a [[gauge space]] $S$, given a Cauchy approximation $x$, an element $c$ in $S$ is a __limit__ of $x$ if this condition is satisfied for each gauging distance separately. Explicitly:
$$ \forall d,\; \forall \epsilon, \theta,\; d(x_\epsilon,c) \lt \epsilon + \theta .$$

In a [[rational premetric space|rational]] or [[real premetric space]] $S$, given a Cauchy approximation $x$, an element $c$ in $S$ is a __limit__ of $x$ if this condition is satisfied for the premetric. Explicitly:
$$ \forall \epsilon, \theta,\; x_\epsilon \sim_{\epsilon + \theta} c .$$

## Related concepts

* [[Booij premetric space]]
* [[Cauchy structure]]
* [[modulus of convergence]]
* [[Cauchy real numbers]]
* [[HoTT book real numbers]]

## References 

* {#Booij20} [[Auke Booij]], *Analysis in Univalent Type Theory* (2020) &lbrack;[etheses:10411](http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf), [[Booij-AnalysisInUF.pdf:file]]&rbrack;

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

[[!redirects Cauchy approximation]]
[[!redirects Cauchy approximations]]

[[!redirects real Cauchy approximation]]
[[!redirects real Cauchy approximations]]

[[!redirects rational Cauchy approximation]]
[[!redirects rational Cauchy approximations]]

[[!redirects limit of a Cauchy approximation]]
[[!redirects limits of a Cauchy approximation]]