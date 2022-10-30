
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **L&#246;wenheim-Skolem theorem** is a basic result in the _[[model theory]]_ of [[first-order logic]] and is part of a family of closely related theorems that concern the relation between structures or [[models]] of [[first-order theories]] of different cardinality. 

One idea behind it is that finitary first-order logic by itself cannot pin down the cardinality of infinite structures or models: roughly speaking, L&#246;wenheim-Skolem says that given a such structure $M$, one can construct elementary substructures or elementary extensions $N$ of different cardinalities. This gives an elementary reason why one cannot expect absolute [[categoricity]] for first-order theories; after this theorem was introduced, attention shifted to the question of categoricity in powers $\kappa$ (i.e., how many models there are of a given cardinality $\kappa$), leading up eventually to Morley's categoricity results and, further down the road and in much greater generality, to Shelah's introduction of [[stability theory]]. 

Historically, the theorem was one of the first results in model theory with papers published by Leopold L&#246;wenheim (1915) and [[Thoralf Skolem]] (1920) which helped establishing first-order logic in the center of [[mathematical logic]]. It was however conceived by Skolem in view of a problem he saw with first-order set theory, now called "Skolem's [[paradox]]", where one could construct a *countable* model of ZFC, with the paradoxical consequence that (externally speaking) the model admits no uncountable sets but yet (internally speaking) it has them. As usually happens with "paradoxes" (cf. [[Banach-Tarski paradox]]), this phenomenon was over time digested and accepted as the ordinary fact of the matter without qualms, and just one more illustration of how one must simply retrain one's intuition to fit the facts. 

Although the theorem fails in [[second-order logic]] (for example, note one has absolute categoricity for the concept of complete ordered field), variants hold in infinitary logic with countably infinite disjunctions and in [[categorical logic]] for [[sketches]]. The theorem plays an important role in [[abstract model theory]] e.g. in [[Lindström's theorems]] on the characterization of standard [[first-order logic]].[^fine]

[^fine]: As a theorem that fails to hold is hardly a theorem at all, one prefers in the context of abstract model theory to speak of the _L&#246;wenheim-Skolem property_.

## Statements and proofs 

One frequently sees the L&#246;wenheim-Skolem theorem separated into an "upward" version (which produces [[elementary embedding|elementary extensions]]) and a "downward" part (producing elementary substructures). The upward version can be derived just by a clever application of the [[compactness theorem]]; the downward version involves a construction called "Skolemization". Both proofs involve modifying the language. 

Let $\Sigma$ be a first-order [[signature]], 

## Related entries

* [[Skolem's paradox]]

* [[compactness theorem]]

* [[Lindström's theorem]]

* [[Craig interpolation theorem]]

* [[Thoralf Skolem]]

## Link

* Wikipedia, _[L&#246;wenheim-Skolem theorem](https://en.wikipedia.org/wiki/L&#246;wenheim&#8211;Skolem_theorem)_

## References

* {#AdamekRosicky94}[[Jiří Adámek]], [[Jiří Rosický]], _Locally presentable and accessible categories_ ,  Cambridge UP 1994.

* J. van Heijenoort (ed.), _From Frege to G&#246;del - A Source Book in Mathematical Logic 1879-1931_ , Harvard UP 1967.

* L. L&#246;wenheim, _&#220;ber die M&#246;glichkeiten im Relativkalk&#252;l_ , Math. Ann. **76** (1915) pp.447-470. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/pdf/?PPN=GDZPPN002266121); English transl. in van Heijenoort (1967) pp.228-251)

* [[Michael Makkai]], [[Robert Paré]], _Accessible categories: The foundations of categorical model theory_ , Contemporary Mathematics 104. American Mathematical
Society, Rhode Island, 1989. 
{#MakkaiPare}

* [[Thoralf Skolem]], *[[Some remarks on axiomatized set theory|Einige Bemerkungen zur axiomatischen Begründung der Mengenlehre]]*, Mathematikerkongressen i Helsingfor 4-7 Juli 1922. English transl. pp.290-301 of van Heijenoort (ed.), _From Frege to G&#246;del_ , Harvard UP 1967.

* M. Zawadowski, _The Skolem-L&#246;wenheim theorem in toposes_ , Studia Logica **42** (1983) pp.461-475.

* M. Zawadowski, _The Skolem-L&#246;wenheim theorem in toposes II_ , Studia Logica **44** (1985) pp.25-38.


[[!redirects Lowenheim-Skolem theorem]]
[[!redirects Löwenheim-Skolem property]]
[[!redirects Lowenheim-Skolem property]]