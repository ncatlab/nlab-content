
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

Neutral constructive mathematics is a branch of [[constructive mathematics]] which simply removes the [[axiom of choice]] and [[excluded middle]] from the [[axioms]] of the [[foundations]], and does not replace it either with weaker versions of the axiom of choice or with axioms which contradict the axiom of choice. Thus, neutral constructive mathematics is agnostic about the status of the [[axiom of choice]] and [[excluded middle]]. 

As a result, [[impredicative mathematics|impredicative]] neutral constructive mathematics is the [[internal logic]] of an [[elementary topos]] with [[natural numbers object]]. 

## Examples

Examples of mathematical foundations which one could do impredicative neutral constructive mathematics include:

* [[Martin-Löf type theory]], [[cubical type theory]], or ([[higher observational type theory|higher]]) [[observational type theory]] with a [[type of all propositions]]. 

* intuitionistic [[higher-order logic]]

* intuitionistic [[ETCS]]

* intuitionistic bounded [[SEAR]]

* [[intuitionistic Mostowski set theory]]

* the [[internal logic]] of any [[elementary topos]]

Examples of mathematical foundations which one could do predicative neutral constructive mathematics include:

* [[Martin-Löf type theory]], [[cubical type theory]], or ([[higher observational type theory|higher]]) [[observational type theory]]. 

* [[constructive Mostowski set theory]]

* the [[internal logic]] of any $\Pi$-$W$-pretopos. 

## Consequences

* In general, for any statement $P$ which is true in [[classical mathematics]], the statement that "the [[law of excluded middle]] implies $P$" is true in neutral constructive mathematics. 

* Furthermore, for any statement $P$ which is true in [[classical mathematics]] with the [[axiom of choice]], the statement that "the axiom of choice implies $P$" is true in neutral constructive mathematics. 

### Set theory

* [[classical sets]] only form a [[Heyting pretopos]] rather than an [[elementary topos]]. 

* sets with [[tight apartness relations]] only form a [[locally cartesian closed category]] rather than a [[elementary topos]]. 

### Real analysis

* In [[topology]], [[locales]] are usually better behaved than [[topological spaces]]. Thus, in [[real analysis]] one usually talks about the [[localic real numbers]] $\mathbb{R}_L$ rather than the [[Dedekind real numbers]] $\mathbb{R}_D$. Many statements, such as the [[Heine-Borel theorem]], the [[fundamental theorem of algebra]], et cetera, are true in the [[localic real numbers]], while they are not provable in the [[Dedekind real numbers]]. Nevertheless, the [[Dedekind real numbers]] are still of interest, being the spatial points of the [[localic real numbers]], and the two notions coincide with [[excluded middle]]. 

* Similarly, one usually talks about the localic complex numbers $\mathbb{C}_L$ or the localic real [[Clifford algebra]] $\mathrm{Cl}_{3, 0}(\mathbb{R}_L)$, et cetera, instead of the Dedekind [[complex numbers]] $\mathbb{C}_D$ or the Dedekind real Clifford algebra $\mathrm{Cl}_{3, 0}(\mathbb{R}_D)$. 

* The [[modulated Cantor real numbers]] or [[Eudoxus real numbers]] $\mathbb{R}_C$ are a subset of the [[Dedekind real numbers]], but cannot be proven to be equivalent to the [[Dedekind real numbers]], nor can they be proven to be [[sequentially Cauchy complete]]. Nevertheless, the modulated Cantor real numbers are of interest since they are defined using [[sequences]] of [[rational numbers]], [[locators]], or almost linear homomorphisms on the [[integers]], and thus are the ones which could be computed with in an algorithm, (see [[exact real arithmetic]]). 

* The [[HoTT book real numbers]] $\mathbb{R}_H$ are the minimum subset of the [[Dedekind real numbers]] for which [[analytic functions]] like the [[exponential function]], [[sine]], and [[cosine]] are well-defined, as well as the [[Jordan content]] and [[Riemann integration]]. They are defined as the sequential Cauchy completion of the [[rational numbers]].

* Unsigned decimal digits are not sufficient to represent the modulated Cantor real numbers, one has to use signed decimal digits instead. 

* Continuous functions on the localic real numbers are continuous maps between the locales. 

* If using the [[localic real numbers]], [[semidefinite integrals]] are fundamental and [[antiderivatives]] are a derived concept; additionally, the existence of a semidefinite integral must be proven directly in the [[fundamental theorem of calculus]], rather than indirectly through the existence of [[definite integrals]]

### Algebra

* Not every subset has an injection into the superset. Thus, subsets with an injection are usually better behaved than general subsets. 

* Not every vector space has a basis. Thus, free vector spaces are usually better behaved than vector spaces in general. 

## See also

* [[Jason Rute]], *What is neutral constructive mathematics*, ([MathOverflow](https://mathoverflow.net/questions/404270/what-is-neutral-constructive-mathematics))

* [[Fred Richman]], *Constructive Mathematics without Choice*,
in: *Reuniting the Antipodes -- Constructive and Nonstandard Views of the Continuum*, Synthese Library **306**, Springer (2001) 199-206 &lbrack;[doi:10.1007/978-94-015-9757-9_17](https://doi.org/10.1007/978-94-015-9757-9_17)&rbrack;

There was a seminar on neutral constructive mathematics:

* Mathematical Logic and Constructivity: *The Scope and Limits of Neutral Constructivism*, Stockholm, Sweden, August 20-23, 2019 ([website](http://logic.math.su.se/mloc-2019/))

[[!redirects neutral constructivism]]