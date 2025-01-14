
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


\tableofcontents

## Idea

In [[linear logic]] and [[affine logic]], the **$?$-modality** or the **exponential disjunction** is the [[de Morgan dual]] of the [[exponential conjunction|!-modality]]. 

## Examples

### Antithesis interpretation

In the [[antithesis interpretation]] of [[affine logic]] into [[impredicative mathematics|impredicative]] [[constructive mathematics]], given the [[set of truth values]] $\Omega$, one can define a [[set]] of [[type of affine propositions|affine propositions]] by the set 

$$\Omega_\pm \coloneqq \{(P^+, P^-) \in \Omega \times \Omega \vdash \neg (P^+ \wedge P^-)\}$$

The ?-modality is a function $?:\Omega_\pm \to \Omega_\pm$ is defined for each affine proposition $(P^+, P^-) \in \Omega_\pm$ by 

$$?(P^+, P^-) \coloneqq (\neg P^-, P^-)$$

\begin{theorem}
The ?-modality is equal to the [[multiplicative disjunction]] of $(P^+, P^-)$ with itself

$$!(P^+, P^-) = (P^+, P^-) \invamp (P^+, P^-)$$
\end{theorem}

\begin{proof}
The multiplicative disjunction is given by 
$$(P^+, P^-) \invamp (P^+, P^-) = ((P^- \Rightarrow P^+) \wedge (P^- \Rightarrow P^+), P^- \wedge P^-)$$
Given two propositions $P^+$ and $P^-$ such that $\neg (P^+ \wedge P^-)$, we have $\neg P^+ = P^- \Rightarrow P^+$. Since intuitionistic [[conjunction]] is [[idempotent]], we have 
$$(P^+, P^-) \invamp (P^+, P^-) = ((P^- \Rightarrow P^+) \wedge (P^- \Rightarrow P^+), P^- \wedge P^-) = (\neg P^- \wedge \neg P^-, P^- \wedge P^-) = (\neg P^-, P^-) = ?(P^+, P^-)$$
\end{proof}

## Related concepts

* [[exponential conjunction|!-modality]]

[[!include logic symbols -- table]]

## References

The ?-modality in [[affine logic]] applied to [[constructive mathematics]]:

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

category: logic

[[!redirects why not]]
[[!redirects ?]]
[[!redirects ?-modality]]
[[!redirects %3F-modality]]
[[!redirects exponential disjunction]]
[[!redirects question mark modality]]
