
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

A family of [[axioms]] in [[constructive mathematics]] which are provable from the [[principle of excluded middle]]. They imply their respective versions of the [[fan theorem]], since bar induction is about [[Baire space of sequences]] while the fan theorem is about [[Cantor space]], which is a subspace of Baire space. 

> This page should contain the classical proof of full bar induction, as well as Brouwer’s reasoning for why bar induction should hold. 

## Definition

Let $\mathbb{N}^*$ denote the [[list]] of [[natural numbers]]. A [[bar]] is a subset $P \subseteq \mathbb{N}^*$ such that for all sequences $\alpha$ of natural numbers, there exists a natural number $n$ such that the list of all $\alpha(i)$ for all $i \lt n$ is in $P$. A bar $P$ is *inductive* if for all lists $a \in \mathbb{N}^*$ and all natural numbers $n \in \mathbb{N}$, if the concatenation of $a$ with $n$ is in $P$, then $a$ is in $P$. Finally, a bar $P$ is *monotone* if for all lists $a, b \in \mathbb{N}^*$, if $a$ is in $P$, then the concatenation of $a$ and $b$ is in $P$. 

* The principle of **decidable bar induction** or **decidable bar theorem** states that every bar which is a [[detachable subset]] of $\mathbb{N}^*$ is inductive. 

* The principle of **monotone bar induction** or **monotone bar theorem** states that every monotone bar is inductive. 

* The principle of **$\Sigma_1^0$ bar induction** or **$\Sigma_1^0$ bar theorem** states that every bar which is a semi-decidable subset of $\mathbb{N}^*$ is inductive. 

* The principle of **full bar induction** or **full bar theorem** states that every bar is inductive. 

## Properties

$\Sigma_1^0$ bar induction and thus the full bar induction implies the [[limited principle of omniscience]] for the [[natural numbers]] $\mathrm{LPO}_\mathbb{N}$. 

Monotone bar induction is equivalent to [[Baire space of sequences|Baire space]] being [[spatial locale|spatial]] as a [[locale]]. 

## Related concepts

* [[bar]]

* [[fan theorem]]

## References

* L. E. J. Brouwer. Uber Definitionsbereiche von Funktionen. Mathematische Annalen, 97:60–75, 1927.

* W. A. Howard and G. Kreisel. Transfinite induction and bar induction of types zero and one, and the
role of continuity in intuitionistic analysis. J. Symb. Log., 31(3):325–358, 1966.

* W. W. Tait. Constructive reasoning. In B. V. Rootselaar and J. Staal, editors, Logic, Methodology
and Philosophy of Science III, Studies in Logic and the Foundations of Mathematics, pages 185–200,
Amsterdam, 1968. North-Holland.

* [[Michael Fourman]], [[Martin Hyland]], _Sheaf Models for Analysis_ , pp.280-301 in Fourman, Mulvey, Scott (eds.), _Applications of Sheaves_ , LNM **753** Springer Heidelberg 1979. ([draft](https://www.dpmms.cam.ac.uk/~jmeh1/Research/Oldpapers/analysis79.pdf), 6.64 MB)

* [[Anne Sjerp Troelstra]], [[Dirk van Dalen]]: *Constructivism in Mathematics -- An introduction*, Volume I, Studies in Logic and the Foundations of Mathematics **121**, North Holland (1988) &lbrack;[ISBN:9780444702661](https://www.elsevier.com/books/constructivism-in-mathematics-vol-1/troelstra/978-0-444-70266-1)&rbrack;

* [[Nicola Gambino]], [[Peter Schuster]], *Spatiality for formal topologies* Mathematical Structures in Computer Science. 2007;17(1):65-80. ([doi:10.1017/S0960129506005810](https://doi.org/10.1017/S0960129506005810)) 

* [[Benno van den Berg]], [[Ieke Moerdijk]], *Derived rules for predicative set theory: an application of sheaves* ([arXiv:1009.3553](https://arxiv.org/abs/1009.3553))

* [[Michael Rathjen]], [[Pedro Francisco Valencia Vizcaino]], *Well ordering principles and bar induction* ([arXiv:1405.4485](https://arxiv.org/abs/1405.4485))

* [[Tatsuji Kawai]], [[Giovanni Sambin]], *The principle of pointfree continuity*, Logical Methods in Computer Science, Volume 15, Issue 1 (March 5, 2019). ([doi:10.23638/LMCS-15%281%3A22%292019](https://doi.org/10.23638/LMCS-15%281%3A22%292019), [arXiv:1802.04512](https://arxiv.org/abs/1802.04512))

* [[Tatsuji Kawai]], *Principles of bar induction and continuity on Baire space* ([arXiv:1808.04082](https://arxiv.org/abs/1808.04082))

* [[Tatsuji Kawai]], *Representing definable functions of $\mathrm{HA}^\omega$ by neighbourhood functions* ([arXiv:1901.11270](https://arxiv.org/abs/1901.11270))

* [[Joan Rand Moschovakis]], *Solovay's Relative Consistency Proof for FIM and BI* ([arXiv:2101.05878](https://arxiv.org/abs/2101.05878))

* [[Nuria Brede]], [[Hugo Herbelin]], *On the logical structure of choice and bar induction principles*, LICS 2021 - 36th Annual Symposium on Logic in Computer Science, Jun 2021, Rome / Virtual, Italy. ([arXiv:2105.08951](https://arxiv.org/abs/2105.08951))

[[!redirects bar theorem]]

[[!redirects decidable bar induction]]
[[!redirects decidable bar theorem]]

[[!redirects monotone bar induction]]
[[!redirects monotone bar theorem]]

[[!redirects monotonic bar induction]]
[[!redirects monotonic bar theorem]]

[[!redirects full bar induction]]
[[!redirects full bar theorem]]
