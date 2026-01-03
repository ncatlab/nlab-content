
\tableofcontents

## Definition

A [[proposition]] or [[truth value]] $P$ is **semi-decidable** or **semidecidable** if and only if [[existential quantifier|there exists]] a [[sequence]] of [[booleans]] $f \in 2^\mathbb{N}$ such that $P$ if and only if there exists a natural number $x \in \mathbb{N}$ such that $f(x) = 1$. 

$$\mathrm{isSemiDecidable}(P) \coloneqq \exists f \in 2^\mathbb{N}.P \iff \exists x \in \mathbb{N}.f(x) = 1$$

The set of all semi-decidable propositions is typically called the **[[Rosolini dominance]]**, though it may not be a [[dominance]] without certain assumptions such as [[countable choice]] or [[excluded middle]]. 

If the [[foundations of mathematics]] has the [[Cauchy real numbers]] $\mathbb{R}_C$ as well, then $P$ is semideciable if and only if there exists a Cauchy real number $x \in \mathbb{R}_C$ such that $P$ if and only if $x \gt 0$.

$$\mathrm{isSemiDecidable}(P) \coloneqq \exists x \in \mathbb{R}_C.P \iff x \gt 0$$

The [[limited principle of omniscience]] for the [[natural numbers]] $\mathrm{LPO}_\mathbb{N}$ implies that every semi-decidable proposition is a [[decidable proposition]]. 

### In dependent type theory

In dependent type theory, the definition of semi-decidable makes sense for any type, not just the mere propositions. However, like many other definitions in [[dependent type theory]], one has to make sure to use an [[equivalence of types]] instead of [[logical equivalence]] in the definition of a semi-decidable type; this ensures that, like for decidable types, all semi-decidable types are propositions. 

\begin{definition}
A type $P$ is semi-decidable if [[existential quantifier|there exists]] a [[sequence]] of [[booleans]] $f:\mathbb{N} \to \mathrm{bool}$ such that $P$ is equivalent to that there exists a natural number $x:\mathbb{N}$ such that $f(x) = 1$. 

$$\mathrm{isSemiDecidable}(P) \coloneqq \left[\sum_{f:\mathbb{N} \to \mathrm{bool}} P \simeq \left[ \sum_{x:\mathbb{N}}f(x) =_{\mathrm{bool}} 1\right]\right]$$
\end{definition}

where $[A]$ is the [[bracket type]] of the type $A$. 

There is also a partially untruncated version of this, which is the type 

$$\sum_{f:\mathbb{N} \to \mathrm{bool}} P \simeq \left[\sum_{x:\mathbb{N}}f(x) =_{\mathrm{bool}} 1\right]$$

of all boolean sequences $f$ for which $P$ is equivalent to there exists a natural number $x:\mathbb{N}$ such that $f(x) = 1$. 

## Related concepts

* [[decidable proposition]]

* [[proposition]], [[truth value]]

* [[synthetic topology]], [[dominance]]

* [[quasidecidable proposition]]

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

[[!redirects semi-decidable type]]
[[!redirects semi-decidable types]]

[[!redirects semidecidable type]]
[[!redirects semidecidable types]]
