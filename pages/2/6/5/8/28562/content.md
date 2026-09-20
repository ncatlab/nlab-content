
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

A [[large cardinal]] that is inconsistent with [[ZFC]]. In order to remove the inconsistency, one can either choose to remove the [[axiom of choice]] to get [[ZF]] + a Reinhardt cardinal, or one can choose to remove the [[axiom of replacement]] and restrict to the [[axiom of bounded separation]] to get [[BZC]] + a Reinhardt cardinal. 

In [[constructive set theory]], one typically uses Reinhardt sets instead of Reinhardt cardinals, since cardinals are not well behaved in the absence of [[excluded middle]].

One also has the notion of a super Reinhardt cardinal or a super Reinhardt set as generalizations of Reinhardt cardinals or Reinhardt sets. 

## Definition

### In ZF

A **Reinhardt cardinal** in a model $V$ of ZF is a critical point of a non-trivial elementary embedding $j:V \to V$ of the model into itself. Reinhardt cardinals in ZF are one of the largest [[large cardinal axioms]] possible.

### In IZF and CZF

A **Reinhardt set** in a model of [[IZF]] or [[CZF]] $V$ with an [[elementary embedding]] $J:V \to V$ is a [[inaccessible set|inaccessible]] and [[transitive set]] $K$ such that $K \in J(K)$ and $j(x) = x$ for all $x \in K$. 

Meanwhile there are multiple inequivalent definitions of a *super Reinhardt set* in constructive mathematics, which only coincide in the presence of [[excluded middle]]. See section 4.2 of [Jeon & Matthews 2024](#JeonMatthews24) for more details. 

### In BZC

In BZC, the definition of a Reinhardt cardinal is the same as the definition of a Reinhardt cardinal in ZF. However, without the [[axiom of replacement]], a Reinhardt cardinal is a much weaker large cardinal axiom; it cannot even construct the large cardinal $\aleph_\omega$ in the absence of replacement. Furthermore, unlike [[ZF]], it is consistent to have a Reinhardt cardinal and [[V = L]] or [[V = Ultimate L]] in [[BZC]]. 

One only needs to add the $I_3$ axiom to a meta-theory in order to describe BZC + a Reinhardt cardinal. 

## Related concepts

* [[large cardinal]]

* [[elementary embedding]]

* [[Berkeley cardinal]]

## References

* {#JeonMatthews24} [[Hanul Jeon]], [[Richard Matthews]], *Very large set axioms over constructive set theories*, The Bulletin of Symbolic Logic. 2024;30(4):455-535. &lbrack;[doi:10.1017/bsl.2024.8](https://doi.org/10.1017/bsl.2024.8), [arXiv:2204.05831](https://arxiv.org/abs/2204.05831)&rbrack;

* [[Hanul Jeon]], *Is BZC inconsistent with Reinhardt cardinals*, Mathematics Stackexchange ([web](https://math.stackexchange.com/a/4009228))

* Wikipedia, *[Reinhardt cardinal](https://en.wikipedia.org/wiki/Reinhardt_cardinal)*

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
