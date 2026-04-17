
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

## Generalizations

Semi-decidable propositions, which are not closed under [[existential quantification]] over the [[natural numbers]], can be generalized to **quasi-decidable propositions** ([Escardo 2020](#Escardo20)) or **Sierpiński-semidecidable propositions** ([de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)), which are the closure of semi-decidable propositions under the logical operations of finite [[conjunctions]] and [[existential quantification]] over the [[natural numbers]]. 

The set of Sierpiński-semidecidable propositions is thus given by the [[Sierpinski space#Predicative|predicative version of Sierpinski space]] $\Sigma$, which, unlike the [[Rosolini dominance]], is always a [[dominance]]. This is in turn used to construct a version of the [[Dedekind real numbers]] using only Sierpiński-semidecidable subsets ($\mathrm{Q}^\Sigma \times \mathrm{Q}^\Sigma)$ of the rational numbers, which coincides with the [[Cauchy real numbers]] [[if and only if]] every Sierpiński-semidecidable proposition is (Rosolini) semidecidable in the usual sense. 

## Related concepts

* [[decidable proposition]]

* [[proposition]], [[truth value]]

* [[synthetic topology]], [[dominance]]

## References

* [[Andrej Bauer]], [[Davorin Lešnik]], _Metric Spaces in Synthetic Topology_, 2010 ([pdf](http://math.andrej.com/wp-content/uploads/2010/01/csms_in_synthtop.pdf))

* {#EK17} [[Martín Escardó]], [[Cory Knapp]]. *Partial Elements and Recursion via Dominances in Univalent Type Theory.* In 26th EACSL Annual Conference on Computer Science Logic (CSL 2017). Leibniz International Proceedings in Informatics (LIPIcs), Volume 82, pp. 21:1-21:16, Schloss Dagstuhl – Leibniz-Zentrum für Informatik (2017) &lbrack;[10.4230/LIPIcs.CSL.2017.21](https://doi.org/10.4230/LIPIcs.CSL.2017.21)&rbrack;

* {#Escardo20} [[Martin Escardo]]. *Quasidecidable propositions*. [[Agda]] code with comments, 2020. ([URL](https://cs.bham.ac.uk/~mhe/TypeTopology/NotionsOfDecidability.QuasiDecidable.html)).

* {#JKMF26} [[Tom de Jong]], [[Nicolai Kraus]], [[Aref Mohammadzadeh]], [[Fredrik Nordvall Forsberg]], *Generalized Decidability via Brouwer Trees* ([arXiv:2602.10844](https://arxiv.org/abs/2602.10844))

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

[[!redirects quasi-decidable]]

[[!redirects quasidecidable]]

[[!redirects quasi-decidable proposition]]
[[!redirects quasi-decidable propositions]]

[[!redirects quasidecidable proposition]]
[[!redirects quasidecidable propositions]]

[[!redirects quasi-decidable truth value]]
[[!redirects quasi-decidable truth values]]

[[!redirects quasidecidable truth value]]
[[!redirects quasidecidable truth values]]

[[!redirects Sierpinski-semidecidable]]
[[!redirects Sierpinski-semi-decidable]]
[[!redirects Sierpiński-semidecidable]]
[[!redirects Sierpiński-semi-decidable]]

[[!redirects Sierpinski-semi-decidable proposition]]
[[!redirects Sierpinski-semi-decidable propositions]]
[[!redirects Sierpiński-semi-decidable proposition]]
[[!redirects Sierpiński-semi-decidable propositions]]

[[!redirects Sierpinski-semidecidable proposition]]
[[!redirects Sierpinski-semidecidable propositions]]
[[!redirects Sierpiński-semidecidable proposition]]
[[!redirects Sierpiński-semidecidable propositions]]

[[!redirects Sierpinski-semi-decidable truth value]]
[[!redirects Sierpinski-semi-decidable truth values]]
[[!redirects Sierpiński-semi-decidable truth value]]
[[!redirects Sierpiński-semi-decidable truth values]]

[[!redirects Sierpinski-semidecidable truth value]]
[[!redirects Sierpinski-semidecidable truth values]]
[[!redirects Sierpiński-semidecidable truth value]]
[[!redirects Sierpiński-semidecidable truth values]]