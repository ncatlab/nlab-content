
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Idea

A [[large cardinal]] that is inconsistent with [[ZFC]] due to [[Kunen's inconsistency theorem]]. In order to remove the inconsistency, one can either choose to remove the [[axiom of choice]] to get [[ZF]] + a Reinhardt cardinal, or one can choose to remove the [[axiom of replacement]] to get [[ZC]] + a Reinhardt cardinal. 

In [[constructive set theory]], one typically uses Reinhardt sets instead of Reinhardt cardinals, since cardinals are not well behaved in the absence of [[excluded middle]].

One also has the notion of a super Reinhardt cardinal or a super Reinhardt set as generalizations of Reinhardt cardinals or Reinhardt sets. 

If one tries to remove the [[axiom of infinity]] from the [[set theory]], a Reinhardt cardinal is sufficient to prove the axiom of infinity. 

## Definition

### In ZF

A **Reinhardt cardinal** in a model $V$ of ZF is a critical point of a non-trivial elementary embedding $j:V \to V$ of the model into itself. Reinhardt cardinals in ZF are one of the largest [[large cardinal axioms]] possible.

### In IZF and CZF

A **Reinhardt set** in a model of [[IZF]] or [[CZF]] $V$ with an [[elementary embedding]] $J:V \to V$ is a [[inaccessible set|inaccessible]] and [[transitive set]] $K$ such that $K \in J(K)$ and $j(x) = x$ for all $x \in K$. 

Meanwhile there are multiple inequivalent definitions of a *super Reinhardt set* in constructive mathematics, which only coincide in the presence of [[excluded middle]]. See section 4.2 of [Jeon & Matthews 2024](#JeonMatthews24) for more details. 

### In BZC and ZC

In [[BZC]] and [[ZC]], the definition of a Reinhardt cardinal is the same as the definition of a Reinhardt cardinal in ZF. However, the absence of the [[axiom of replacement]] makes a Reinhardt cardinal consistent with the [[axiom of choice]]. 

Moreover, Reinhardt cardinals in [[BZC]] do not imply large cardinals such as Ramsey cardinals in the absence of the [[axiom of full separation]]. 

One only needs to add the $I_3$ axiom to a meta-theory in order to describe [[BZC]] + a Reinhardt cardinal. 

In the presence of the [[axiom of choice]], Reinhardt cardinals are inconsistent with [[Vopěnka's principle]], since Vopěnka's principle implies the [[axiom of replacement]]. 

## Related concepts

* [[large cardinal]]

* [[elementary embedding]]

* [[Berkeley cardinal]]

## References

* [[Hanul Jeon]]: *How strong is a Reinhardt set over extensions of CZF?*, &lbrack;[arXiv:2101.07455](https://arxiv.org/abs/2101.07455)&rbrack;

* Rohan Srivastava: *The Landscape of Large Cardinals* &lbrack;[arXiv:2205.01787](https://arxiv.org/abs/2205.01787)&rbrack;

* {#JeonMatthews24} [[Hanul Jeon]], [[Richard Matthews]]: *Very large set axioms over constructive set theories*, The Bulletin of Symbolic Logic. 2024;30(4):455-535. &lbrack;[doi:10.1017/bsl.2024.8](https://doi.org/10.1017/bsl.2024.8), [arXiv:2204.05831](https://arxiv.org/abs/2204.05831)&rbrack;

* [[Hanul Jeon]]: *Is BZC inconsistent with Reinhardt cardinals*, Mathematics Stackexchange ([web](https://math.stackexchange.com/a/4009228))

* Wikipedia, *[Reinhardt cardinal](https://en.wikipedia.org/wiki/Reinhardt_cardinal)*

On [[large cardinal axioms]] without the [[axiom of replacement]]:

* *Large cardinals without replacement*, MathOverflow ([web](https://mathoverflow.net/questions/383978/large-cardinals-without-replacement))

On [[realizability]] models for [[Reinhardt cardinals]]:

* [[Laura Fontanella]], [[Guillaume Geoffroy]], [[Richard Matthews]]: *Realizability Models for Large Cardinals*, In 32nd EACSL Annual Conference on Computer Science Logic (CSL 2024). Leibniz International Proceedings in Informatics (LIPIcs), Volume 288, pp. 28:1-28:18, Schloss Dagstuhl – Leibniz-Zentrum für Informatik (2024) &lbrack;[10.4230/LIPIcs.CSL.2024.28](https://doi.org/10.4230/LIPIcs.CSL.2024.28)&rbrack;

[[!redirects Reinhardt cardinal]]
[[!redirects Reinhardt cardinals]]

[[!redirects Reinhardt set]]
[[!redirects Reinhardt sets]]

[[!redirects Reinhardt object]]
[[!redirects Reinhardt objects]]

[[!redirects super Reinhardt cardinal]]
[[!redirects super Reinhardt cardinals]]

[[!redirects super Reinhardt set]]
[[!redirects super Reinhardt sets]]
