
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
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

## Double negation stability 

### In intuitionistic logic

In [[intuitionistic logic]], the default notion of stability is the [[double negation]] modality $\neg\neg$.  Since $p \Rightarrow \neg\neg{p}$ regardless, $p$ is stable iff $\neg\neg{p} \Rightarrow p$.  Being stable is weaker than being [[decidable proposition|decidable]]; however, if every proposition is stable, then every proposition is decidable and the logic becomes [[classical logic|classical]].  (This is because $p$ is decidable iff $p \vee \neg{p}$ is stable.)  Double negation is monadic, so by the previous paragraph, $p$ is stable iff $p \equiv \neg\neg{q}$ for some $q$; in fact, $p$ is stable iff $p \equiv \neg{q}$ for some $q$.  (I guess that this has to do with [[negation]] forming a [[monadic adjunction]] with itself, or something like that.)  In the [[topological semantics]] of intuitionistic logic (where propositions correspond to [[open sets]]), the stable propositions correspond to the [[regular open sets]].

In the [[internal language]] of a [[sheaf topos|category of sheaves]] $Sh(X)$, a proposition $p$ is $\neg\neg$-stable iff it is enough for $p$ to hold on a dense open subset of $X$ to be able to conclude that $p$ holds on the whole of $X$. For instance, the proposition $f = 0$ about a section $f$ of the sheaf of real functions on $X$ is $\neg\neg$-stable.

### In the antithesis interpretation

In the [[antithesis interpretation]] of [[intuitionistic logic]] into [[affine logic]], there are two notions of propositions: the usual intuitionistic propositions, and the affine propositions, which are pairs of [[mutually exclusive propositions]]. 

Every affine proposition is already double negation stable via the [[affine negation]] $P^\bot$, since the affine negation is defined as swapping the two component intuitionistic [[propositions]] of the pair of intuitionistic propositions around, and swapping of pairs is an [[involution]]. 

On the other hand, stability of intuitionistic double negation in the sense above is a little more complicated since there always exists affine propositions, such as the never provably true and never provably false affine proposition $(\bot, \bot)$, whose intuitionistic propositions are not the negation of the other in the pair. Instead, given an affine proposition $P = (P^+, P^-)$, one has to use the [[exponential conjunction]] $!P = (P^+, \neg P^+)$ and [[exponential disjunction]] $?P = (\neg P^-, P^-)$, which are the [[modalities]] in the antithesis interpretation which gets the intutionistic negation out of the affine logic. In the antithesis interpretation of intuitionistic logic into affine logic, we have the equations 

$$!P = P \boxtimes P \qquad ?P = P \boxplus P$$

that say that exponential conjunction and [[multiplicative conjunction]] coincide with each other and exponential disjunction and [[multiplicative disjunction]] coincide with each other, so one can use either one in the formulation of intuitionistic double negation stability of affine propositions. 

Now, in order for an affine proposition $P$ to be stable, we want $P^+$ to be equivalent to $\neg P^-$ and $P^-$ to be equivalent to $\neg P^+$. In both cases, we already have intutionistic non-contradiction 
$$P^+ \Rightarrow \neg P^- = P^- \Rightarrow \neg P^+ = \neg (P^+ \wedge P^-)$$
by the definition of an affine proposition. In affine logic, this is equivalent to the following always true statements:
$$P \multimap ?P \quad P \multimap P \boxplus P \quad !P \multimap P \quad P \boxtimes P \multimap P \quad P \boxplus P^\bot$$

Thus, it suffices for the reverse implications in the intuitionistic logic: 
$$\neg P^- \Rightarrow P^+ \qquad \neg P^+ \Rightarrow P^-$$
The first implication says that a proposition $P$ is *refutative*, and is defined in the affine logic by $?P \multimap P$ or equivalently $P \boxplus P \multimap P$. The second implication says that a proposition $P$ is *affirmative*, and is defined in the affine logic by $P \multimap !P$ or equivalently $P \multimap P \boxtimes P$. Thus, an affine proposition is intuitionistically double negation stable if it is both affirmative and refutative. 

## Related concepts

* [[stable relation]]

* [[stable equality]]

## References

* [[Andrew Swan]], *Double negation stable h-propositions in cubical sets*, ([arXiv:2209.15035](https://arxiv.org/abs/2209.15035))

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))

[[!redirects stable proposition]]
[[!redirects stable propositions]]

[[!redirects stable property]]
[[!redirects stable properties]]

[[!redirects stable predicate]]
[[!redirects stable predicates]]
