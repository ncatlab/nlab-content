
\tableofcontents

## Definition

A [[proposition]] or [[truth value]] $P$ is **semi-decidable** or **semidecidable** if and only if [[existential quantifier|there exists]] a [[sequence]] of [[booleans]] $f \in 2^\mathbb{N}$ such that $P$ if and only if there exists a natural number $x \in \mathbb{N}$ such that $f(x) = 1$. 

$$\mathrm{isSemiDecidable}(P) \coloneqq \exists f \in 2^\mathbb{N}.P \iff \exists x \in \mathbb{N}.f(x) = 1$$

The set of all semi-decidable propositions is typically called the **[[Rosolini dominance]]**, though it may not be a [[dominance]] without certain assumptions such as [[countable choice]]. 

If the [[foundations of mathematics]] has the [[Cauchy real numbers]] $\mathbb{R}_C$ as well, then $P$ is semideciable if and only if there exists a Cauchy real number $x \in \mathbb{R}_C$ such that $P$ if and only if $x \gt 0$.

$$\mathrm{isSemiDecidable}(P) \coloneqq \exists x \in \mathbb{R}_C.P \iff x \gt 0$$

The [[limited principle of omniscience]] for the [[natural numbers]] $\mathrm{LPO}_\mathbb{N}$ implies that every semi-decidable proposition is a [[decidable proposition]]. 

## Related concepts

* [[decidable proposition]]

* [[proposition]], [[truth value]]

* [[synthetic topology]], [[dominance]]

## References

* [[Andrej Bauer]], [[Davorin Lešnik]], _Metric Spaces in Synthetic Topology_, 2010 ([pdf](http://math.andrej.com/wp-content/uploads/2010/01/csms_in_synthtop.pdf))

[[!redirects semi-decidable]]

[[!redirects semidecidable]]

[[!redirects semi-decidable proposition]]
[[!redirects semi-decidable propositions]]

[[!redirects semidecidable proposition]]
[[!redirects semidecidable propositions]]

[[!redirects semi-decidable truth value]]
[[!redirects semi-decidable truth values]]

[[!redirects semidecidable truth value]]
[[!redirects semidecidable truth values]]
