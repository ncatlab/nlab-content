
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
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

In ([[modal logic|modal]]) [[logic]], a [[proposition]] $p$ is __stable__ under a [[modality]] $\diamond$ if $p \equiv \diamond{p}$.  If $\diamond$ is [[monadic modality|monadic]], then $p$ is stable iff $p \equiv \diamond{q}$ for some $q$.

(In terms of [[modal type theory]] and [[propositions as types]] this means that $p$ is a _[[modal type]]_.)

## Examples

In [[intuitionistic logic]], the default is the [[double negation]] modality $\neg\neg$.  Since $p \Rightarrow \neg\neg{p}$ regardless, $p$ is stable iff $\neg\neg{p} \Rightarrow p$.  Being stable is weaker than being [[decidable proposition|decidable]]; however, if every proposition is stable, then every proposition is decidable and the logic becomes [[classical logic|classical]].  (This is because $p$ is decidable iff $p \vee \neg{p}$ is stable.)  Double negation is monadic, so by the previous paragraph, $p$ is stable iff $p \equiv \neg\neg{q}$ for some $q$; in fact, $p$ is stable iff $p \equiv \neg{q}$ for some $q$.  (I guess that this has to do with [[negation]] forming a [[monadic adjunction]] with itself, or something like that.)  In the [[topological semantics]] of intuitionistic logic (where propositions correspond to [[open sets]]), the stable propositions correspond to the [[regular open sets]].

In the [[internal language]] of a [[sheaf topos|category of sheaves]] $Sh(X)$, a proposition $p$ is $\neg\neg$-stable iff it is enough for $p$ to hold on a dense open subset of $X$ to be able to conclude that $p$ holds on the whole of $X$. For instance, the proposition $f = 0$ about a section $f$ of the sheaf of real functions on $X$ is $\neg\neg$-stable.

[[!redirects stable proposition]]
[[!redirects stable propositions]]

[[!redirects stable property]]
[[!redirects stable properties]]

[[!redirects stable predicate]]
[[!redirects stable predicates]]
