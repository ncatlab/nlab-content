
> This article is about premetric spaces as defined by [Gilbert 2017](#Gilbert17). For other notions of premetric spaces, see *[[premetric space]]*.

***

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

## Idea

A notion of space that is more general than [[metric space]], but not so general as to be the notion of [[premetric space (Booij)|premetric space defined by Auke Booij]] as just a set equipped with a bare ternery relation. 

## Definition 

A **premetric space** is a [[set]] $S$ with a ternary [[relation]] $a \sim_\epsilon b$ for $a \in S$, $b \in S$, and $\epsilon \in \mathbb{Q}_+$, where $\mathbb{Q}_+$ represent the positive [[rational numbers]] in $\mathbb{Q}$, satisfying the five conditions:

* reflexivity: for all elements $a \in S$ and positive rational numbers $\epsilon$, $a \sim_\epsilon a$

* symmetry: for all elements $a, b \in S$ and positive rational numbers $\epsilon$, $a \sim_\epsilon b$ implies $b \sim_\epsilon a$

* triangularity: for all elements $a, b, c \in S$ and positive rational numbers $\epsilon$, $\delta$, $a \sim_\epsilon b$ and $b \sim_\delta c$ implies $a \sim_{\epsilon + \delta} c$

* roundedness: for all elements $a, b \in S$ and positive rational numbers $\epsilon$, $a \sim_\epsilon b$ implies that there exists a positive rational number $\delta$ such that $a \sim_\delta b$

* separateness: for all elements $a, b \in S$, if $a \sim_\epsilon b$ for all positive rational numbers $\epsilon$, then $a = b$

The ternary relation itself is called a **premetric** or a **closeness relation**. 

## Examples

* Every [[Archimedean ordered field]] is a premetric space

* Every [[metric space]] is a premetric space

## The category of premetric spaces and Lipschitz functions

Given a positive rational number $\delta$ and two premetric spaces $S$ and $T$, a function $f:S \to T$ is a *[[Lipschitz function]]* if for all elements $a, b \in S$ and positive rational numbers $\epsilon$, $a \sim_\epsilon b$ implies $f(a) \sim_{\delta \cdot \epsilon} f(b)$. 

Premetric spaces and Lipschitz functions between premetric spaces form a category $\mathrm{PrSpace}$. 

Lipschitz functions are particularly notable because any Lipschitz function $f:S \to T$ can be lifted up to a function $f':\mathcal{C}(S) \to T$, where $\mathcal{C}(S)$ is the [[sequential Cauchy completion]] of the premetric space $S$. This allows the sequential Cauchy completion $S \mapsto \mathcal{C}(S)$ to be extended to an [[idempotent monad|idempotent monadic]] [[endofunctor]] on $\mathrm{PrSpace}$. 

## Generalizations

The usual notion of a [[metric space]] uses the [[real numbers]] rather than the [[rational numbers]] in the metric inequalities. This means that to generalize from metric spaces, one can use the positive [[real numbers]] instead of the positive [[rational numbers]] as the indexing set of the ternary relation (i.e. $a \sim_\epsilon b$ for $a \in S$, $b \in S$, and $\epsilon \in \mathbb{R}_+$), yielding a notion of a *real premetric space*. The original notion of a premetric space by Gilbert can then be called a *rational premetric space*.

More generally, the notion of a premetric space can be generalized from the positive rationals to the [[positive cone]] $R_+$ of any [[dense relation|densely ordered]] [[Archimedean ordered integral domain]] $R$. Examples of such $R$ include the [[real numbers]], the [[dyadic rational numbers]] and the [[decimal numbers]], as well as any other extension $\mathbb{Z}[1/b]$ of the integers, for positive integer $b \geq 2$. The mutliplicative structure of the integral domain is still needed to define Lipschitz functions between these generalized premetric spaces. 

Thus, a **generalized premetric space** is a [[set]] $S$ with a ternary [[relation]] $a \sim_\epsilon b$ for $a \in S$, $b \in S$, and $\epsilon \in R_+$, satisfying the five conditions:

* reflexivity: for all elements $a \in S$ and positive elements $\epsilon \in R_+$, $a \sim_\epsilon a$

* symmetry: for all elements $a, b \in S$ and positive elements $\epsilon \in R_+$, $a \sim_\epsilon b$ implies $b \sim_\epsilon a$

* triangularity: for all elements $a, b, c \in S$ and positive elements $\epsilon, \delta \in R_+$, $a \sim_\epsilon b$ and $b \sim_\delta c$ implies $a \sim_{\epsilon + \delta} c$

* roundedness: for all elements $a, b \in S$ and positive elements $\epsilon \in R_+$, $a \sim_\epsilon b$ implies that there exists a positive element $\delta \in R_+$ such that $a \sim_\delta b$

* separateness: for all elements $a, b \in S$, if $a \sim_\epsilon b$ for all positive elements $\epsilon \in R_+$, then $a = b$

## Related concepts

* [[premetric space]]

* [[metric space]]

* [[Lipschitz function]]

* [[Cauchy sequence]]

* [[sequentially complete space]]

* [[HoTT book real numbers]]

## References

* {#Gilbert17} [[Gaëtan Gilbert]]: *Formalising real numbers in homotopy type theory*, In: CPP’17, Proceedings of the 6th ACM SIGPLAN Conference on Certified Programs and Proofs (2017) 112--124 &lbrack;[doi:10.1145/3018610.3018614](https://doi.org/10.1145/3018610.3018614)&rbrack;

* Lorenzo Molena: *A Cubical Path from Algebra to Analysis*, talk at TYPES 2026, 8 May 2026 &lbrack;[abstract](https://types2026.cse.chalmers.se/abstracts/51.pdf), [slides](https://types2026.cse.chalmers.se/slides/51.pdf)&rbrack;

[[!redirects closeness relation]]
[[!redirects closeness relations]]

[[!redirects premetric (Gilbert)]]
[[!redirects premetrics (Gilbert)]]
[[!redirects premetric space (Gilbert)]]
[[!redirects premetric spaces (Gilbert)]]

[[!redirects Gilbert premetric]]
[[!redirects Gilbert premetrics]]
[[!redirects Gilbert premetric space]]
[[!redirects Gilbert premetric spaces]]

[[!redirects generalized premetric]]
[[!redirects generalized premetrics]]
[[!redirects generalized premetric space]]
[[!redirects generalized premetric spaces]]

[[!redirects generalised premetric]]
[[!redirects generalised premetrics]]
[[!redirects generalised premetric space]]
[[!redirects generalised premetric spaces]]